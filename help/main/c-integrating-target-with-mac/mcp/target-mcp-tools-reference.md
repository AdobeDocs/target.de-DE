---
solution: Target
product: target
title: Adobe Target MCP Server Tools-Referenz
description: Vollständige Parameterreferenz für alle 21 schreibgeschützten Tools, die vom Adobe Target MCP-Server bereitgestellt werden.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
source-git-commit: 7b0c8b18abe2db4e07e3ef979d6d194f4c4c81d6
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 11%

---

# [!DNL Adobe Target] MCP Server Tools-Referenz {#target-mcp-tools-reference}


>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt.

Diese Seite ist eine vollständige Referenz für alle schreibgeschützten Tools, die vom [!DNL Adobe Target] MCP-Server bereitgestellt werden. Für jedes Tool finden Sie eine Beschreibung, Parameterdetails, einen Rückgabewert und eine Beispielaufforderung in natürlicher Sprache. Anweisungen zum Setup und Anwendungsfälle finden Sie unter [Erste Schritte](target-mcp-get-started.md) und [Anwendungsfälle und exemplarische Vorgehensweisen](target-mcp-use-cases.md).

>[!IMPORTANT]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration, und die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen vor der produktiven Verwendung in einer Sandbox-Umgebung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Voraussetzungen {#tools-prerequisites}

Ihre [!DNL Adobe Target] bestimmt, welche Tools Ihnen zur Verfügung stehen:

* **Beobachter** Rolle oder höher: Zugriff auf alle Lesewerkzeuge
* **Editor**-Rolle: Zugriff auf Lese- und Schreib-Tools (Erstellen)
* **Genehmiger** Rolle: Zugriff auf das Lesen, Schreiben und Aktivieren/Deaktivieren von Tools

Vollständige Setup-Anweisungen finden Sie unter [Erste Schritte](target-mcp-get-started.md).

## Aktivitäts-Tools {#tools-activities}

+++Aktivitäten auflisten

**tool:** `list_target_activities`

Auflisten [!DNL Adobe Target] Aktivitäten mit Server-seitiger Filterung und Sortierung.

Ruft eine paginierte Liste von Aktivitäten ab. Alle Filter werden Server-seitig von der [!DNL Target] Admin-API angewendet. Der Server gibt maximal 200 Aktivitäten pro Seite zurück.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Aktivitäten (Server-Maximum: 200) |
| `offset` | Ganzzahl | Nein | Anzahl der für die Paginierung zu überspringenden Aktivitäten |
| `sort_by` | string | Nein | Feld zum Sortieren nach. Präfix mit `-` für absteigende Reihenfolge (z. B. `-modifiedAt`). Optionen: `id`, `name`, `state`, `priority`, `startsAt`, `endsAt`, `lifetimeStart`, `lifetimeEnd`, `createdAt`, `createdBy`, `modifiedAt`, `modifiedBy`, `type`, `thirdPartyId` |
| `state` | string | Nein | Nach Aktivitätsstatus filtern: `approved` (live/aktiv), `deactivated` (inaktiv), `paused`, `saved` (Entwurf) |
| `activity_type` | string | Nein | Filtern nach Typ: `ab` (A/B-Test), `xt` (Experience Targeting), `abt` (Automated Personalization) |
| `name_contains` | string | Nein | Filtern Sie Aktivitäten, deren Name diese Zeichenfolge enthält (ignoriert Groß-/Kleinschreibung). |
| `starts_after` | string | Nein | ISO 8601-Datum — Aktivitäten, die nach diesem Datum beginnen |
| `starts_before` | string | Nein | ISO 8601-Datum — Aktivitäten, die vor diesem Datum beginnen |
| `modified_after` | string | Nein | ISO 8601-Datum — nach diesem Datum geänderte Aktivitäten |
| `ends_after` | string | Nein | ISO 8601-Datum — Aktivitäten, die nach diesem Datum enden |
| `ends_before` | string | Nein | ISO 8601-Datum - Aktivitäten, die vor diesem Datum enden |
| `workspace` | string | Nein | Nach Arbeitsbereich-ID filtern |
| `segment_id` | string | Nein | Nach Zielgruppensegment-ID filtern |
| `profile_attribute_id` | string | Nein | Nach Profilattribut-ID filtern |
| `priority` | Ganzzahl | Nein | Filtern nach exaktem Prioritätswert (0-999) |
| `mbox` | string | Nein | Nach Mbox-/Standortnamen filtern |
| `offer_id` | string | Nein | Nach Angebots-ID filtern |
| `view_id` | string | Nein | Nach SPA-Ansicht-ID filtern |

**Gibt** JSON-Objekt mit `activities` (Liste der Objekte einschließlich `id`, `name`, `state`, `type`, `priority`, `modifiedAt`, `startsAt`, `endsAt`) und `total` (Gesamtanzahl, kann die zurückgegebene Seitengröße überschreiten) zurück.

**Beispielaufforderung:** „Listet alle aktiven A/B-Tests auf, sortiert nach der letzten Änderung.“

+++

+++Abrufen einer A/B-Aktivität

**tool:** `get_ab_activity`

Detaillierte Informationen zu A/B-Aktivitäten.

Ruft die vollständige Konfiguration eines bestimmten A/B-Tests ab, einschließlich Erlebnissen, Standorten, Metriken und Zielgruppenbestimmungsregeln.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der A/B-Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten (Name, Status, Priorität, Daten), Erlebnisse, Standorte und Angebote, Ziele und Metriken sowie Zielgruppenbestimmungsregeln.

**Beispielaufforderung:** „Details für A/B-12345 abrufen“

+++

+++Abrufen einer Experience Targeting-Aktivität

**tool:** `get_xt_activity`

Hier erhalten Sie detaillierte Informationen zu einer Experience Targeting(XT)-Aktivität.

Ruft die vollständige Konfiguration einer bestimmten XT-Aktivität ab, einschließlich Zielgruppen-Erlebnis-Mappings, Standorten und Metriken.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der XT-Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten, Erlebnissen mit Zielgruppen-Mappings, Standorten und Angeboten sowie Zielen und Metriken.

**Beispielaufforderung:** „Abrufen von Details für Experience Targeting-12345“

+++

+++Abrufen einer Automated Personalization-Aktivität

**tool:** `get_abt_activity`

Erhalten Sie detaillierte Informationen zu einer Automated Personalization-Aktivität (AP).

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der AP-Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten, Erlebnisse, Speicherorte und algorithmische Einstellungen.

**Beispielaufforderung:** „Abrufen von Details für automatische Personalization-12345“

+++

<!--
+++Create an A/B activity

**Tool:** `create_ab_activity`

Create a new A/B test activity.

Creates a new A/B test with the specified configuration including experiences, offers, and targeting.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `audiences` | array | No | Target audience configurations |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an A/B test called 'Homepage Hero Test' with two experiences testing different hero images on the homepage-hero mbox."

+++
-->

<!--
+++Create an Experience Targeting activity

**Tool:** `create_xt_activity`

Create a new Experience Targeting (XT) activity.

Creates an XT activity that delivers different experiences to different audiences based on targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations with audience mappings |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an Experience Targeting activity called 'Geo Personalization' that shows different content to visitors from different regions."

+++
-->

<!--
+++Update an A/B activity

**Tool:** `update_ab_activity`

Update an existing A/B activity.

Uses a read-modify-write pattern: fetches the current state, merges your changes, validates, and sends the update.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity to update |
| `activity` | object | Yes | Fields to update (name, priority, experiences, locations, goals, etc.) |

**Returns:** The updated activity object.

**Example prompt:** "Update activity 12345 to change the traffic allocation to 70/30."

+++
-->

<!--
+++Update an Experience Targeting activity

**Tool:** `update_xt_activity`

Update an existing Experience Targeting activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update XT activity 12345 to add a new experience for mobile visitors."

+++
-->

<!--
+++Update an Automated Personalization activity

**Tool:** `update_abt_activity`

Update an existing Automated Personalization activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the AP activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update Auto-Personalization activity 12345 to change the optimization goal."

+++
-->

<!--
+++Update activity schedule

**Tool:** `update_activity_schedule`

Update activity start and end dates.

Updates the schedule for an activity without modifying other settings.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `activity_type` | string | Yes | Type of activity: `ab`, `xt`, or `abt` |
| `starts_at` | string | No | New start date (ISO 8601) |
| `ends_at` | string | No | New end date (ISO 8601) |

**Returns:** Confirmation of the schedule update.

**Example prompt:** "Update the schedule for A/B activity 12345 to run from May 1st to May 31st."

+++
-->

<!--
+++Change activity state

**Tool:** `update_activity_state`

Change activity state (activate, deactivate, or pause).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `state` | string | Yes | New state: `approved` (live/active), `deactivated` (inactive), `paused`, or `saved` (draft) |

**Returns:** The updated activity state.

**Example prompt:** "Activate activity 12345" or "Pause the Homepage Hero Test."

+++
-->

<!--
+++Rename an activity

**Tool:** `update_activity_name`

Rename an activity.

Updates only the name without modifying the full configuration.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `name` | string | Yes | New activity name |

**Returns:** The updated activity object.

**Example prompt:** "Rename activity 12345 to 'Summer Campaign Hero Test'."

+++
-->

<!--
+++Change activity priority

**Tool:** `update_activity_priority`

Change activity priority.

Higher-priority activities take precedence when multiple activities target the same location.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `priority` | integer | Yes | New priority value (0–999; higher = higher priority) |

**Returns:** The updated activity object.

**Example prompt:** "Set the priority of activity 12345 to 100."

+++
-->

<!--
+++Add a variant to an activity

**Tool:** `add_activity_variant`

Add a new experience/variant to an activity.

Handles all structural coordination including creating options, mapping to locations, and rebalancing traffic.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name for the new experience/variant |
| `offer_id` | integer | No | (Form-based) Existing offer ID to use |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `traffic_percentage` | integer | No | Traffic % for the new variant (1–99). If omitted, traffic is rebalanced evenly |
| `audience_id` | integer | No | Audience ID for the variant (XT activities) |
| `modifications` | array | No | (VEC) List of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Add a new variant called 'Holiday Theme' to A/B activity 12345 using offer 67890."

+++
-->

<!--
+++Update traffic split

**Tool:** `update_traffic_split`

Update traffic allocation across variants.

The percentages must sum to exactly 100.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab` or `abt` (XT not supported — audience-targeted) |
| `splits` | object | Yes | Dictionary mapping experience name to percentage. Must include all experiences and sum to 100 |

**Returns:** The updated activity object.

**Example prompt:** "Change the traffic split for activity 12345 to 70% Control and 30% Variant A."

+++
-->

<!--
+++Change a variant's offer

**Tool:** `update_variant_offer`

Change the offer for a specific variant.

Works for both form-based activities (using `offer_id`) and VEC activities (using `modifications`).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to update |
| `offer_id` | integer | No | (Form-based) New offer ID |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `modifications` | array | No | (VEC) New list of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Update the 'Variant A' experience in activity 12345 to use offer 99999."

+++
-->

<!--
+++Remove a variant from an activity

**Tool:** `remove_activity_variant`

Remove an experience/variant from an activity.

Removes the experience, cleans up orphaned options, and rebalances traffic evenly across remaining variants.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to remove |

**Returns:** The updated activity object.

**Example prompt:** "Remove the 'Test Variant' experience from A/B activity 12345."

+++
-->

## Angebotswerkzeuge {#tools-offers}

+++Angebote auflisten

**tool:** `list_target_offers`

Auflisten aller Angebote in Ihrem [!DNL Target].

Ruft eine paginierte Liste von Inhaltsangeboten mit optionaler Filterung ab.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Angeboten |
| `offset` | Ganzzahl | Nein | Anzahl der für die Paginierung zu übersprungenen Angebote |
| `type` | string | Nein | Filtern nach Angebotstyp: `content` (HTML), `json` oder `redirect` |
| `name` | string | Nein | Nach Angebotsnamen filtern (teilweise Übereinstimmung) |

**Gibt** JSON-Objekt mit `offers` (Liste der Objekte einschließlich `id`, `name`, `type`, `content`, `modifiedAt`) und `total` zurück.

**Beispielaufforderung:** „Alle JSON-Angebote auflisten“

+++

+++Angebot abrufen

**tool:** `get_target_offer`

Erhalten Sie detaillierte Informationen zu einem bestimmten Angebot.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `offer_id` | Ganzzahl | Ja | Die eindeutige Kennung des Angebots |

**Rückgabe** Vollständige Angebotsdetails, einschließlich `id`, `name`, `type`, `content`, `workspace` und `modifiedAt`.

**Beispiel-Eingabeaufforderung:** „Abrufen von Details zur 67890“

+++

<!--
+++Create an HTML offer

**Tool:** `create_target_offer`

Create a new HTML content offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | string | Yes | HTML or text content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create an HTML offer called 'Summer Sale Banner' with a promotional banner."

+++

+++Create a JSON offer

**Tool:** `create_target_json_offer`

Create a new JSON offer for delivering structured data.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | object | Yes | JSON content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create a JSON offer called 'Feature Flags Config' with feature toggle settings."

+++

+++Update an offer

**Tool:** `update_target_offer`

Update an existing offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `offer_id` | integer | Yes | The unique identifier of the offer to update |
| `name` | string | No | Updated offer name |
| `content` | string or object | No | Updated offer content |

**Returns:** The updated offer object.

**Example prompt:** "Update offer 67890 with new promotional content."

+++
-->

## Zielgruppen-Tools {#tools-audiences}

+++Audiences auflisten

**tool:** `list_target_audiences`

Auflisten aller Zielgruppen in Ihrem [!DNL Target].

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Zielgruppen |
| `offset` | Ganzzahl | Nein | Anzahl der Zielgruppen, die für die Paginierung übersprungen werden sollen |

**Gibt** JSON-Objekt mit `audiences` (Liste der Objekte einschließlich `id`, `name`, `description`, `origin`, `modifiedAt`) und `total` zurück.

**Beispielaufforderung:** „Listen Sie alle Zielgruppen auf.“

+++

<!--
+++Create an audience

**Tool:** `create_target_audience`

Create a new audience with targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the audience |
| `description` | string | No | Description of the audience |
| `targetRule` | object | No | Targeting rules (geo, browser, custom attributes, etc.) |
| `workspace_id` | string | No | Workspace ID for the audience |

**Returns:** The created audience with its assigned ID.

**Example prompt:** "Create an audience called 'Mobile Visitors from California' targeting mobile users in CA."

+++
-->

## Mbox-Tools {#tools-mboxes}

+++Mboxes auflisten

**tool:** `list_target_mboxes`

Auflisten aller Mboxes in Ihrem [!DNL Target].

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Mboxes |
| `offset` | Ganzzahl | Nein | Anzahl der Mboxes, die für die Paginierung übersprungen werden sollen |
| `name` | string | Nein | Nach Mbox-Namen filtern (teilweise Übereinstimmung) |
| `status` | string | Nein | Filtern nach Status |

**Gibt** JSON-Objekt mit `mboxes` (Liste der Objekte einschließlich `name`, `status`, `lastRequestTime`) und `total` zurück.

**Beispielaufforderung:** „Alle Mboxes auflisten, die &#39;Homepage&#39; enthalten.“

+++

+++Abrufen einer Mbox

**tool:** `get_target_mbox`

Abrufen detaillierter Informationen zu einer bestimmten Mbox.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `mbox_name` | string | Ja | Der Name der Mbox |

**Gibt** Mbox-Details zurück, einschließlich `name`, `status` und Liste der Aktivitäten, die die Mbox verwenden.

**Beispielaufforderung:** „Details für mbox &#39;homepage-hero&#39; abrufen“.

+++

+++Mbox-Profilattribute auflisten

**tool:** `list_target_mbox_profile_attributes`

Listet alle für die Zielgruppenbestimmung verfügbaren Mbox-Profilattribute auf.

Keine Parameter erforderlich.

**Gibt** JSON-Array von Profilattributobjekten zurück.

**Beispielaufforderung:** „Welche Profilattribute sind für die Zielgruppenbestimmung verfügbar?“

+++

## Eigenschafts-Tools {#tools-properties}

+++Eigenschaften der Liste

**tool:** `list_target_properties`

Listet alle Eigenschaften in Ihrem [!DNL Target] auf.

Eigenschaften organisieren Aktivitäten und steuern den Zugriff.

Keine Parameter erforderlich.

**Gibt** Liste der Eigenschaftenobjekte einschließlich `id`, `name`, `description` und `channel` zurück.

**Beispielaufforderung:** „Alle Target-Eigenschaften auflisten“.

+++

## Reporting-Tools {#tools-reporting}

+++Abrufen eines A/B-Leistungsberichts

**tool:** `get_ab_performance_report`

Abrufen eines Leistungsberichts für eine A/B-Aktivität.

Ruft Konversionsraten, Steigerung und Konfidenzniveaus ab.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der A/B-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht (z. B. `last7days`, `last30days` oder benutzerdefinierter Datumsbereich) |

**Rückgaben:** Metriken auf Erlebnisebene (Besucher, Konversionen, Konversionsrate), Steigerungsberechnungen, statistische Konfidenzniveaus und Umsatzmetriken (falls konfiguriert).

**Beispielaufforderung:** „Anzeigen des Leistungsberichts für A/B-Test-12345 der letzten 30 Tage“

+++

+++Abrufen eines Berichts zu A/B-Bestellungen

**tool:** `get_ab_orders_report`

Abrufen eines Berichts zu Bestellungen/Umsatz für eine A/B-Aktivität.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der A/B-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Rückgabe:** Anzahl der Bestellungen, Umsatz und durchschnittlicher Bestellwert nach Erlebnis.

**Beispielaufforderung:** „Bericht zu Bestellungen für 12345 abrufen“

+++

+++Abrufen eines Experience Targeting-Leistungsberichts

**tool:** `get_xt_performance_report`

Abrufen eines Leistungsberichts für eine Experience Targeting-Aktivität.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der XT-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Gibt zurück** Leistungsmetriken auf Erlebnisebene.

**Beispielaufforderung:** „Leistung für meine Experience Targeting-54321 anzeigen“

+++

+++Abrufen eines Berichts zu Experience Targeting-Bestellungen

**tool:** `get_xt_orders_report`

Abrufen eines Berichts zu Bestellungen/Umsatz für eine Experience Targeting-Aktivität.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der XT-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Gibt zurück** Sortiert Metriken nach Erlebnis.

**Beispielaufforderung:** „Abrufen von Auftragsdaten für XT-54321“.

+++

+++Abrufen eines Leistungsberichts nach Aktivitätsname

**tool:** `get_activity_report_by_name`

Suchen Sie nach einer Aktivität anhand des Namens und rufen Sie ihren Leistungsbericht ab.

Nützlich, wenn Sie den Namen der Aktivität, aber nicht ihre ID kennen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_name` | string | Ja | Name der zu suchenden Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Gibt zurück** Aktivitätsdetails und Leistungsmetriken.

**Beispielaufforderung:** „Abrufen des Leistungsberichts für meine Aktivität „Startseiten-Heldentest“.“

+++

## Vorschau-Tools {#tools-preview}

+++Vorschau einer Aktivität anzeigen

**tool:** `preview_activity`

Generieren von Vorschau-URLs für die Browser-QA für eine [!DNL Target].

Erstellt anklickbare Vorschau-Links, die die Anzeige bestimmter Erlebnisse erzwingen, und umgeht dabei die Zielgruppen-Targeting-Regeln. Funktioniert für A/B-, XT- und Automated Personalization-Aktivitäten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die [!DNL Target] Aktivitäts-ID für die Vorschau |
| `experience_index` | Ganzzahl | Nein | Auf 0 basierender Erlebnisindex. Wenn ausgelassen, werden URLs für alle Erlebnisse zurückgegeben. |
| `url` | string | Nein | Seiten-URL für die Vorschau. Erforderlich für formularbasierte Aktivitäten. Für VEC-Aktivitäten überschreibt den erstellten Speicherort, sofern angegeben |

**Gibt** Aktivitätsinformationen (Name, Typ, Status), Vorschau-URLs für jedes Erlebnis sowie Erlebnisnamen und -indizes zurück.

**Beispielaufforderung:** „Generieren Sie Vorschau-URLs für die 12345, damit ich jedes Erlebnis in meinem Browser testen kann.“

+++

## Antwort-Token-Tools {#tools-response-tokens}

+++Auflisten von Antwort-Token

**tool:** `list_target_response_tokens`

Auflisten aller Antwort-Token in Ihrem [!DNL Target].

Ruft alle konfigurierten Antwort-Token ab, sowohl integrierte als auch benutzerdefinierte.

Keine Parameter erforderlich.

**Gibt** JSON-Array von Antwort-Token-Objekten mit `name`-, `type`- und `enabled` zurück.

**Beispielaufforderung:** „Alle Antwort-Token auflisten“

+++

<!--
+++Create a response token

**Tool:** `create_target_response_token`

Create a new custom response token for collecting additional data in [!DNL Target] responses.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `token_name` | string | Yes | Name of the response token |
| `token_type` | string | Yes | Type of token: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO`, or `CRS` |

**Returns:** The created response token object.

**Example prompt:** "Create a custom response token called 'campaign_id' of type ACTIVITY."

+++
-->

## Revisionswerkzeuge {#tools-revisions}

+++Auditprotokoll abrufen

**tool:** `get_target_revisions`

Auditprotokoll für einen Ressourcentyp abrufen.

Ruft Änderungen an [!DNL Target] Ressourcen mit optionaler Filterung nach Autor ab.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `revision_resource_type` | string | Ja | Ressourcentyp: `activity`, `offer` oder `audience` |
| `modified_by` | string | Nein | Nach Benutzer filtern, der Änderungen vorgenommen hat |
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Revisionen |
| `offset` | Ganzzahl | Nein | Anzahl der Revisionen, die für die Paginierung übersprungen werden sollen |

**Gibt**: Revisionsverlauf mit Zeitstempeln, Benutzern und Änderungsbeschreibungen zurück.

**Beispielaufforderung:** „Administratorprotokoll für Aktivitätsänderungen anzeigen“

+++

+++Abrufen von Revisionen für eine bestimmte Entität

**tool:** `get_target_entity_revisions`

Ruft alle Revisionen einer bestimmten Entität nach ID ab.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `revision_resource_type` | string | Ja | Ressourcentyp: `activity`, `offer` oder `audience` |
| `entity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Entität |

**Gibt** JSON-Array aller Revisionen für die angegebene Entität zurück.

**Beispiel-Eingabeaufforderung:** „Alle Änderungen anzeigen, die an Activity 12345 vorgenommen wurden.“

+++

## Vorlagenwerkzeuge {#tools-templates}

+++Verfügbare Vorlagen auflisten

**tool:** `list_target_templates`

Listen Sie die verfügbaren MCP-Ressourcen und Vorlagen für die Erstellung von Aktivitäten und Angeboten auf.

Keine Parameter erforderlich.

**Gibt** JSON-Objekt zurück, das die verfügbaren Vorlagen und Ressourcen auflistet.

**Beispielaufforderung:** „Welche Vorlagen sind für die Erstellung von Aktivitäten verfügbar?“

+++

## Tools-Zusammenfassung {#tools-summary}

| Kategorie | Count | Werkzeuge |
|---|---|---|
| Aktivität | 4 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity` |
| Angebot | 2 | `list_target_offers`, `get_target_offer` |
| Zielgruppe | 1 | `list_target_audiences` |
| mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Eigenschaft | 1 | `list_target_properties` |
| Berichterstellung | 5 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name` |
| Vorschau | 1 | `preview_activity` |
| Antwort-Token | 1 | `list_target_response_tokens` |
| Revision | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| Vorlage | 1 | `list_target_templates` |
| **Gesamt** | **21** | |

## Verwandte Ressourcen {#tools-related}

* [Arbeiten mit MCP-Clients](target-mcp.md)
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
