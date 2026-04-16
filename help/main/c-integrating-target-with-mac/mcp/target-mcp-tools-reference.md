---
solution: Target
product: target
title: Adobe Target MCP Server Tools-Referenz
description: Vollständiger Parameterverweis für alle 39 öffentlichen Tools, die vom Adobe Target MCP-Server bereitgestellt werden.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
hide: true
source-git-commit: 782256b734068075795d5e9c1f3f552ca48918e6
workflow-type: tm+mt
source-wordcount: '2688'
ht-degree: 15%

---

# [!DNL Adobe Target] MCP Server Tools-Referenz {#target-mcp-tools-reference}

>[!BEGINSHADEBOX]

Inhaltsverzeichnis:

* [Arbeiten mit MCP-Clients](target-mcp.md)
* **[MCP Server Tools-Referenz](target-mcp-tools-reference.md)**
* [MCP-Server selbst hosten](target-mcp-self-hosted.md)

>[!ENDSHADEBOX]

Diese Seite ist eine vollständige Referenz für alle öffentlichen Tools, die vom [!DNL Adobe Target] MCP-Server verfügbar gemacht werden. Für jedes Tool finden Sie eine Beschreibung, Parameterdetails, einen Rückgabewert und eine Beispielaufforderung in natürlicher Sprache. Anweisungen zum Setup und Anwendungsfälle finden Sie unter [Arbeiten mit MCP-Clients](target-mcp.md).

>[!NOTE]
>
>Hier sind nur öffentliche Tools dokumentiert. Interne und reine Agententools sind ausgeschlossen. Lesetools stehen allen verbundenen Benutzern mit der Rolle **Beobachter** oder höher zur Verfügung. Schreibtools erfordern die Rolle **Bearbeiter** oder **Genehmiger**.

## Aktivitäts-Tools {#tools-activities}

### list_target_activities

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

### get_ab_activity

Detaillierte Informationen zu A/B-Aktivitäten.

Ruft die vollständige Konfiguration eines bestimmten A/B-Tests ab, einschließlich Erlebnissen, Standorten, Metriken und Zielgruppenbestimmungsregeln.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der A/B-Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten (Name, Status, Priorität, Daten), Erlebnisse, Standorte und Angebote, Ziele und Metriken sowie Zielgruppenbestimmungsregeln.

**Beispielaufforderung:** „Details für A/B-12345 abrufen“

### get_xt_activity

Hier erhalten Sie detaillierte Informationen zu einer Experience Targeting(XT)-Aktivität.

Ruft die vollständige Konfiguration einer bestimmten XT-Aktivität ab, einschließlich Zielgruppen-Erlebnis-Mappings, Standorten und Metriken.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der XT-Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten, Erlebnissen mit Zielgruppen-Mappings, Standorten und Angeboten sowie Zielen und Metriken.

**Beispielaufforderung:** „Abrufen von Details für Experience Targeting-12345“

### get_abt_activity

Erhalten Sie detaillierte Informationen zu einer Automated Personalization-Aktivität (AP).

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der AP-Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten, Erlebnisse, Speicherorte und algorithmische Einstellungen.

**Beispielaufforderung:** „Abrufen von Details für automatische Personalization-12345“

### create_ab_activity

Erstellen Sie eine neue A/B-Test -Aktivität.

Erstellt einen neuen A/B-Test mit der angegebenen Konfiguration, einschließlich Erlebnissen, Angeboten und Targeting.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name der Aktivität |
| `state` | string | Nein | Anfangsstatus: `approved`, `deactivated` oder `saved` (Standard: `saved`) |
| `priority` | Ganzzahl | Nein | Aktivitätspriorität (0-999, Standard: 0) |
| `starts_at` | string | Nein | Startdatum der Aktivität (ISO 8601) |
| `ends_at` | string | Nein | Enddatum der Aktivität (ISO 8601) |
| `experiences` | Array | Ja | Liste der Erlebniskonfigurationen |
| `locations` | Array | Ja | Liste der Standort-/Mbox-Konfigurationen |
| `goals` | Objekt | Nein | Primäre und sekundäre Zielmetriken |
| `audiences` | Array | Nein | Konfigurationen der Zielgruppe |
| `workspace_id` | string | Nein | Workspace-ID für die Aktivität |

**Gibt zurück** Das erstellte Aktivitätsobjekt mit der zugewiesenen ID.

**Beispielaufforderung:** „Erstellen Sie einen A/B-Test namens „Homepage Hero Test“ mit zwei Erlebnissen, indem Sie verschiedene Hero-Bilder auf der homepage-hero mbox testen.“

### create_xt_activity

Erstellen Sie eine neue Experience Targeting-(XT)-Aktivität.

Erstellt eine XT-Aktivität, die basierend auf Targeting-Regeln verschiedene Erlebnisse für unterschiedliche Zielgruppen bereitstellt.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name der Aktivität |
| `state` | string | Nein | Anfangsstatus: `approved`, `deactivated` oder `saved` (Standard: `saved`) |
| `priority` | Ganzzahl | Nein | Aktivitätspriorität (0-999, Standard: 0) |
| `starts_at` | string | Nein | Startdatum der Aktivität (ISO 8601) |
| `ends_at` | string | Nein | Enddatum der Aktivität (ISO 8601) |
| `experiences` | Array | Ja | Liste der Erlebniskonfigurationen mit Zielgruppenzuordnungen |
| `locations` | Array | Ja | Liste der Standort-/Mbox-Konfigurationen |
| `goals` | Objekt | Nein | Primäre und sekundäre Zielmetriken |
| `workspace_id` | string | Nein | Workspace-ID für die Aktivität |

**Gibt zurück** Das erstellte Aktivitätsobjekt mit der zugewiesenen ID.

**Beispielaufforderung:** „Erstellen Sie eine Experience Targeting-Aktivität namens „Geo Personalization&quot;, die Besuchern aus verschiedenen Regionen unterschiedliche Inhalte anzeigt.“

### update_ab_activity

Aktualisieren einer vorhandenen A/B-Aktivität.

Verwendet ein Lese-/Schreibmuster: ruft den aktuellen Status ab, führt Ihre Änderungen zusammen, validiert und sendet die Aktualisierung.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der zu aktualisierenden Aktivität |
| `activity` | Objekt | Ja | Zu aktualisierende Felder (Name, Priorität, Erlebnisse, Standorte, Ziele usw.) |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispiel-Eingabeaufforderung:** „Aktualisieren Sie die 12345, um die Traffic-Zuordnung auf 70/30 zu ändern.“

### update_xt_activity

Aktualisieren Sie eine vorhandene Experience Targeting-Aktivität.

Verwendet ein Lese-, Änderungs- und Schreibmuster.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der zu aktualisierenden XT-Aktivität |
| `activity` | Objekt | Ja | Zu aktualisierende Felder |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „XT-12345 aktualisieren, um mobilen Besuchern ein neues Erlebnis hinzuzufügen.“

### update_abt_activity

Aktualisieren einer bestehenden Automated Personalization-Aktivität.

Verwendet ein Lese-, Änderungs- und Schreibmuster.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der zu aktualisierenden AP-Aktivität |
| `activity` | Objekt | Ja | Zu aktualisierende Felder |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Aktualisieren Sie die 12345 der automatischen Personalization-Aktivität, um das Optimierungsziel zu ändern.“

### update_activity_schedule

Start- und Enddatum der Aktivität aktualisieren

Aktualisiert den Zeitplan einer Aktivität ohne Änderung der anderen Einstellungen

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab`, `xt` oder `abt` |
| `starts_at` | string | Nein | Neues Startdatum (ISO 8601) |
| `ends_at` | string | Nein | Neues Enddatum (ISO 8601) |

**Gibt zurück** Bestätigung der Zeitplanaktualisierung.

**Beispiel-Eingabeaufforderung:** „Aktualisieren Sie den Zeitplan für die A/B-Aktivitäts-12345, die vom 1. Mai bis zum 31. Mai ausgeführt werden soll.“

### update_activity_state

Aktivitätsstatus ändern (aktivieren, deaktivieren oder pausieren).

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `state` | string | Ja | Neuer Status: `approved` (live/aktiv), `deactivated` (inaktiv), `paused` oder `saved` (Entwurf) |

**Gibt zurück** Der aktualisierte Aktivitätsstatus.

**Beispielaufforderung:** „Aktivitäts-12345 aktivieren“ oder „Homepage-Heldentest anhalten“.

### update_activity_name

Eine Aktivität umbenennen.

Aktualisiert nur den Namen, ohne die vollständige Konfiguration zu ändern.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `name` | string | Ja | Neuer Aktivitätsname |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Benennen Sie die Aktivität 12345 in „Heldentest der Sommerkampagne“ um.“

### update_activity_priority

Ändern der Aktivitätspriorität.

Aktivitäten mit höherer Priorität haben Vorrang, wenn mehrere Aktivitäten auf denselben Standort abzielen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `priority` | Ganzzahl | Ja | Neuer Prioritätswert (0-999; höher = höhere Priorität) |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Legen Sie die Priorität der Aktivität 12345 auf 100 fest.“

### add_activity_variant

Hinzufügen eines neuen Erlebnisses/einer neuen Variante zu einer Aktivität.

Übernimmt die gesamte strukturelle Koordinierung, einschließlich der Erstellung von Optionen, der Zuordnung zu Standorten und der Neugewichtung des Traffics.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die ID der zu ändernden Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab`, `xt` oder `abt` |
| `variant_name` | string | Ja | Name des neuen Erlebnisses/der neuen Variante |
| `offer_id` | Ganzzahl | Nein | (Formularbasiert) Vorhandene Angebots-ID zur Verwendung |
| `offer_content` | string | Nein | (Formularbasiert) HTML-Inhalte für ein neues Inline-Angebot |
| `traffic_percentage` | Ganzzahl | Nein | Traffic % für die neue Variante (1-99). Wenn ausgelassen, wird der Traffic gleichmäßig neu ausgerichtet |
| `audience_id` | Ganzzahl | Nein | Zielgruppen-ID für die Variante (XT-Aktivitäten) |
| `modifications` | Array | Nein | (VEC) Liste der CSS-Selektor-basierten Änderungen |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Fügen Sie 12345 mithilfe von 67890 eine neue Variante mit dem Namen „Feiertagsthema“ zur A/B-Aktivität hinzu.“

### update_traffic_split

Aktualisieren der Traffic-Zuordnung zu Varianten.

Die Prozentsätze müssen genau 100 betragen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die ID der zu ändernden Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab` oder `abt` (XT wird nicht unterstützt — Zielgruppen-spezifisch) |
| `splits` | Objekt | Ja | Name des Wörterbuchzuordnungserlebnisses zu Prozentsatz. Muss alle Erlebnisse enthalten und Summe auf 100 |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Ändern Sie die Traffic-Aufteilung für Aktivitäts-12345 in 70 % Kontrolle und 30 % Variante A.“

### update_variant_offer

Ändert das Angebot für eine bestimmte Variante.

Funktioniert sowohl für formularbasierte Aktivitäten (mit `offer_id`) als auch für VEC-Aktivitäten (mit `modifications`).

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die ID der zu ändernden Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab`, `xt` oder `abt` |
| `variant_name` | string | Ja | Name des zu aktualisierenden Erlebnisses/der zu aktualisierenden Variante |
| `offer_id` | Ganzzahl | Nein | (Formularbasiert) Neue Angebots-ID |
| `offer_content` | string | Nein | (Formularbasiert) HTML-Inhalte für ein neues Inline-Angebot |
| `modifications` | Array | Nein | (VEC) Neue Liste der CSS-selektorbasierten Änderungen |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Aktualisieren Sie das Erlebnis „Variante A“ in Activity 12345, um 99999 zu verwenden.“

### remove_activity_variant

Erlebnis/Variante aus einer Aktivität entfernen

Entfernt das Erlebnis, bereinigt verwaiste Optionen und gleicht den Traffic gleichmäßig über die verbleibenden Varianten aus.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die ID der zu ändernden Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab`, `xt` oder `abt` |
| `variant_name` | string | Ja | Name des zu entfernenden Erlebnisses/der zu entfernenden Variante |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Entfernen des Erlebnisses „Testvariante“ aus der A/B-12345.“

## Angebotswerkzeuge {#tools-offers}

### list_target_offers

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

### get_target_offer

Erhalten Sie detaillierte Informationen zu einem bestimmten Angebot.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `offer_id` | Ganzzahl | Ja | Die eindeutige Kennung des Angebots |

**Rückgabe** Vollständige Angebotsdetails, einschließlich `id`, `name`, `type`, `content`, `workspace` und `modifiedAt`.

**Beispiel-Eingabeaufforderung:** „Abrufen von Details zur 67890“

### create_target_offer

Erstellen Sie ein neues HTML-Inhaltsangebot.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name des Angebots |
| `content` | string | Ja | HTML oder Textinhalt für das Angebot |
| `workspace_id` | string | Nein | Workspace-ID für das Angebot |

**Gibt zurück** Das erstellte Angebot mit der zugewiesenen ID.

**Beispiel-Eingabeaufforderung:** „Erstellen Sie ein HTML-Angebot mit dem Namen „Banner für den Sommerverkauf“ und einem Werbebanner.“

### create_target_json_offer

Erstellen Sie ein neues JSON-Angebot für die Bereitstellung strukturierter Daten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name des Angebots |
| `content` | Objekt | Ja | JSON-Inhalt des Angebots |
| `workspace_id` | string | Nein | Workspace-ID für das Angebot |

**Gibt zurück** Das erstellte Angebot mit der zugewiesenen ID.

**Beispielaufforderung:** „Erstellen Sie ein JSON-Angebot mit dem Namen „Feature Flags Config“ und Umschalter für Funktionen.“

### update_target_offer

Vorhandenes Angebot aktualisieren.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `offer_id` | Ganzzahl | Ja | Die eindeutige Kennung des zu aktualisierenden Angebots |
| `name` | string | Nein | Aktualisierter Angebotsname |
| `content` | Zeichenfolge oder Objekt | Nein | Aktualisierter Angebotsinhalt |

**Gibt zurück** Das aktualisierte Angebotsobjekt.

**Beispielaufforderung:** „Aktualisieren der 67890 mit neuen Werbeinhalten.“

## Zielgruppen-Tools {#tools-audiences}

### list_target_audience

Auflisten aller Zielgruppen in Ihrem [!DNL Target].

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Zielgruppen |
| `offset` | Ganzzahl | Nein | Anzahl der Zielgruppen, die für die Paginierung übersprungen werden sollen |

**Gibt** JSON-Objekt mit `audiences` (Liste der Objekte einschließlich `id`, `name`, `description`, `origin`, `modifiedAt`) und `total` zurück.

**Beispielaufforderung:** „Listen Sie alle Zielgruppen auf.“

### create_target_audience

Erstellen Sie eine neue Audience mit Zielgruppenbestimmungsregeln.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name der Zielgruppe |
| `description` | string | Nein | Beschreibung der Zielgruppe |
| `targetRule` | Objekt | Nein | Zielgruppenbestimmungsregeln (Geografie, Browser, benutzerdefinierte Attribute usw.) |
| `workspace_id` | string | Nein | Workspace-ID für die Zielgruppe |

**Gibt zurück** Die erstellte Zielgruppe mit der zugewiesenen ID.

**Beispielaufforderung:** „Erstellen Sie eine Zielgruppe namens „Mobile Besucher aus Kalifornien“, die auf mobile Benutzer in Kalifornien abzielt.“

## Mbox-Tools {#tools-mboxes}

### list_target_mboxes

Auflisten aller Mboxes in Ihrem [!DNL Target].

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `limit` | Ganzzahl | Nein | Maximale Anzahl an zurückzugebenden Mboxes |
| `offset` | Ganzzahl | Nein | Anzahl der Mboxes, die für die Paginierung übersprungen werden sollen |
| `name` | string | Nein | Nach Mbox-Namen filtern (teilweise Übereinstimmung) |
| `status` | string | Nein | Nach Status filtern |

**Gibt** JSON-Objekt mit `mboxes` (Liste der Objekte einschließlich `name`, `status`, `lastRequestTime`) und `total` zurück.

**Beispielaufforderung:** „Alle Mboxes auflisten, die &#39;Homepage&#39; enthalten.“

### get_target_mbox

Abrufen detaillierter Informationen zu einer bestimmten Mbox.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `mbox_name` | string | Ja | Der Name der Mbox |

**Gibt** Mbox-Details zurück, einschließlich `name`, `status` und Liste der Aktivitäten, die die Mbox verwenden.

**Beispielaufforderung:** „Details für mbox &#39;homepage-hero&#39; abrufen“.

### list_target_mbox_profile_attributes

Listet alle für die Zielgruppenbestimmung verfügbaren Mbox-Profilattribute auf.

Keine Parameter erforderlich.

**Gibt** JSON-Array von Profilattributobjekten zurück.

**Beispielaufforderung:** „Welche Profilattribute sind für die Zielgruppenbestimmung verfügbar?“

## Eigenschafts-Tools {#tools-properties}

### list_target_properties

Listet alle Eigenschaften in Ihrem [!DNL Target] auf.

Eigenschaften organisieren Aktivitäten und steuern den Zugriff.

Keine Parameter erforderlich.

**Gibt** Liste der Eigenschaftenobjekte einschließlich `id`, `name`, `description` und `channel` zurück.

**Beispielaufforderung:** „Alle Target-Eigenschaften auflisten“.

## Reporting-Tools {#tools-reporting}

### get_ab_performance_report

Abrufen eines Leistungsberichts für eine A/B-Aktivität.

Ruft Konversionsraten, Steigerung und Konfidenzniveaus ab.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der A/B-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht (z. B. `last7days`, `last30days` oder benutzerdefinierter Datumsbereich) |

**Rückgaben:** Metriken auf Erlebnisebene (Besucher, Konversionen, Konversionsrate), Steigerungsberechnungen, statistische Konfidenzniveaus und Umsatzmetriken (falls konfiguriert).

**Beispielaufforderung:** „Anzeigen des Leistungsberichts für A/B-Test-12345 der letzten 30 Tage“

### get_ab_orders_report

Abrufen eines Berichts zu Bestellungen/Umsatz für eine A/B-Aktivität.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der A/B-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Rückgabe:** Anzahl der Bestellungen, Umsatz und durchschnittlicher Bestellwert nach Erlebnis.

**Beispielaufforderung:** „Bericht zu Bestellungen für 12345 abrufen“

### get_xt_performance_report

Abrufen eines Leistungsberichts für eine Experience Targeting-Aktivität.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der XT-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Gibt zurück** Leistungsmetriken auf Erlebnisebene.

**Beispielaufforderung:** „Leistung für meine Experience Targeting-54321 anzeigen“

### get_xt_orders_report

Abrufen eines Berichts zu Bestellungen/Umsatz für eine Experience Targeting-Aktivität.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der XT-Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Gibt zurück** Sortiert Metriken nach Erlebnis.

**Beispielaufforderung:** „Abrufen von Auftragsdaten für XT-54321“.

### get_activity_report_by_name

Suchen Sie nach einer Aktivität anhand des Namens und rufen Sie ihren Leistungsbericht ab.

Nützlich, wenn Sie den Namen der Aktivität, aber nicht ihre ID kennen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_name` | string | Ja | Name der zu suchenden Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Gibt zurück** Aktivitätsdetails und Leistungsmetriken.

**Beispielaufforderung:** „Abrufen des Leistungsberichts für meine Aktivität „Startseiten-Heldentest“.“

## Vorschau-Tools {#tools-preview}

### preview_activity

Generieren von Vorschau-URLs für die Browser-QA für eine [!DNL Target].

Erstellt anklickbare Vorschau-Links, die die Anzeige bestimmter Erlebnisse erzwingen, und umgeht dabei die Zielgruppen-Targeting-Regeln. Funktioniert für A/B-, XT- und Automated Personalization-Aktivitäten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die [!DNL Target] Aktivitäts-ID für die Vorschau |
| `experience_index` | Ganzzahl | Nein | Auf 0 basierender Erlebnisindex. Wenn ausgelassen, werden URLs für alle Erlebnisse zurückgegeben. |
| `url` | string | Nein | Seiten-URL für die Vorschau. Erforderlich für formularbasierte Aktivitäten. Für VEC-Aktivitäten überschreibt den erstellten Speicherort, sofern angegeben |

**Gibt** Aktivitätsinformationen (Name, Typ, Status), Vorschau-URLs für jedes Erlebnis sowie Erlebnisnamen und -indizes zurück.

**Beispielaufforderung:** „Generieren Sie Vorschau-URLs für die 12345, damit ich jedes Erlebnis in meinem Browser testen kann.“

## Antwort-Token-Tools {#tools-response-tokens}

### list_target_response_tokens

Auflisten aller Antwort-Token in Ihrem [!DNL Target].

Ruft alle konfigurierten Antwort-Token ab, sowohl integrierte als auch benutzerdefinierte.

Keine Parameter erforderlich.

**Gibt** JSON-Array von Antwort-Token-Objekten mit `name`-, `type`- und `enabled` zurück.

**Beispielaufforderung:** „Alle Antwort-Token auflisten“

### create_target_response_token

Erstellen Sie ein neues benutzerdefiniertes Antwort-Token zum Erfassen zusätzlicher Daten in [!DNL Target].

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `token_name` | string | Ja | Name des Antwort-Tokens |
| `token_type` | string | Ja | Typ des Tokens: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO` oder `CRS` |

**Gibt zurück** Das erstellte Antwort-Token-Objekt.

**Beispielaufforderung:** „Erstellen Sie ein benutzerdefiniertes Antwort-Token namens „campaign_id“ vom Typ „ACTIVITY“.

## Revisionswerkzeuge {#tools-revisions}

### get_target_revisions

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

### get_target_entity_revisions

Ruft alle Revisionen einer bestimmten Entität nach ID ab.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `revision_resource_type` | string | Ja | Ressourcentyp: `activity`, `offer` oder `audience` |
| `entity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Entität |

**Gibt** JSON-Array aller Revisionen für die angegebene Entität zurück.

**Beispiel-Eingabeaufforderung:** „Alle Änderungen anzeigen, die an Activity 12345 vorgenommen wurden.“

## Vorlagenwerkzeuge {#tools-templates}

### list_target_templates

Listen Sie die verfügbaren MCP-Ressourcen und Vorlagen für die Erstellung von Aktivitäten und Angeboten auf.

Keine Parameter erforderlich.

**Gibt** JSON-Objekt zurück, das die verfügbaren Vorlagen und Ressourcen auflistet.

**Beispielaufforderung:** „Welche Vorlagen sind für die Erstellung von Aktivitäten verfügbar?“

## Tools-Zusammenfassung {#tools-summary}

| Kategorie | Count | Tools |
|---|---|---|
| Aktivität | 17 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity`, `create_ab_activity`, `create_xt_activity`, `update_ab_activity`, `update_xt_activity`, `update_abt_activity`, `update_activity_schedule`, `update_activity_state`, `update_activity_name`, `update_activity_priority`, `add_activity_variant`, `update_traffic_split`, `update_variant_offer`, `remove_activity_variant` |
| Angebot | 5 | `list_target_offers`, `get_target_offer`, `create_target_offer`, `create_target_json_offer`, `update_target_offer` |
| Zielgruppe | 2 | `list_target_audiences`, `create_target_audience` |
| mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Eigenschaft | 1 | `list_target_properties` |
| Berichterstellung | 5 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name` |
| Vorschau | 1 | `preview_activity` |
| Antwort-Token | 2 | `list_target_response_tokens`, `create_target_response_token` |
| Revision | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| Vorlage | 1 | `list_target_templates` |
| **Gesamt** | **39** | |

## Verwandte Ressourcen {#tools-related}

* [Arbeiten mit MCP-Clients](target-mcp.md)
* [Self-Host des  [!DNL Adobe Target] -MCP-Servers](target-mcp-self-hosted.md)
* [[!DNL Adobe Target] Admin-API-Referenz](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
