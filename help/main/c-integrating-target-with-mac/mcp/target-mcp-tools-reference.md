---
solution: Target
product: target
title: Adobe Target MCP Server Tools-Referenz
description: Vollständiger Parameterverweis für alle Tools, die vom Adobe Target MCP-Server bereitgestellt werden, einschließlich Lese- und Schreibvorgängen.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
source-git-commit: 4b154f401cc9d31d99c169bf08781bcaa7ef5c8f
workflow-type: tm+mt
source-wordcount: '3804'
ht-degree: 14%
---
# [!DNL Adobe Target] MCP Server Tools-Referenz {#target-mcp-tools-reference}

>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt.

Diese Seite ist eine vollständige Referenz für alle Tools, die vom [!DNL Adobe Target] MCP-Server verfügbar gemacht werden. Für jedes Tool finden Sie eine Beschreibung, Parameterdetails, einen Rückgabewert und eine Beispielaufforderung in natürlicher Sprache. Anweisungen zum Setup und Anwendungsfälle finden Sie unter [Erste Schritte](target-mcp-get-started.md) und [Anwendungsfälle und exemplarische Vorgehensweisen](target-mcp-use-cases.md).

>[!IMPORTANT]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration, und die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen vor der produktiven Verwendung in einer Sandbox-Umgebung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Voraussetzungen {#tools-prerequisites}

Ihre [!DNL Adobe Target] bestimmt, welche Tools Ihnen zur Verfügung stehen:

* **Beobachterrolle** oder höher: Zugriff auf alle schreibgeschützten Tools
* **Editor** Rolle oder höher: Zugriff auf Lese- und Schreib-Tools (Erstellen, Aktualisieren)
* **Genehmiger** Rolle: Zugriff auf alle Tools, einschließlich Aktivierung und Deaktivierung

Vollständige Setup-Anweisungen finden Sie unter [Erste Schritte](target-mcp-get-started.md).

## Aktivitäts-Tools {#tools-activities}

>[!NOTE]
>
>Lese- und Schreibvorgänge haben unterschiedliche Bereiche. `get_activity` ruft Aktivitäten aller Typen ab (A/B-Tests, Erlebnis-Targeting, Automated Personalization, automatische Zuordnung, Multivarianz-Tests, Empfehlungen). `update_activity` unterstützt A/B-Tests, Erlebnis-Targeting und Automated Personalization. Automatische Zuordnungs-, Multivarianz-Test- und Recommendations-Aktivitäten sind über den MCP-Server schreibgeschützt.

| Funktion | A/B-Test | Erlebnis-Targeting | Automated Personalization | Automatische Zuordnung | Multivarianz-Test | Recommendations |
|---|---|---|---|---|---|---|
| `get_activity` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `list_target_activities` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `get_activity_performance_report` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `get_activity_orders_report` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `update_activity` | ✓ | ✓ | ✓ | — | — | — |
| Lebenszyklus-Bearbeitungen (Status, Priorität, Name, Zeitplan) | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Bearbeiten von Varianten und Traffic | ✓ | ✓ | ✓ | — | — | — |
| Erstellen | ✓ | ✓ | — | — | — | — |

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
| `activity_type` | string | Nein | Filtern nach Typ: `ab` (A/B-Test), `xt` (Erlebnis-Targeting), `abt` (Automated Personalization), `auto_allocate` (automatische Zuordnung), `mvt` (Multivarianz-Test), `recs` (Recommendations) |
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

+++Abrufen einer Aktivität

**tool:** `get_activity`

Hier erhalten Sie detaillierte Informationen zu Aktivitäten beliebigen Typs.

Ruft die vollständige Konfiguration einer bestimmten Aktivität ab und erkennt automatisch den Aktivitätstyp. Unterstützt A/B-Tests, Erlebnis-Targeting, Automated Personalization, automatische Zuordnung, Multivarianz-Tests und Recommendations-Aktivitäten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |

**Rückgabe** Vollständige Aktivitätsdetails einschließlich Metadaten (Name, Status, Priorität, Daten), Erlebnisse, Standorte und Angebote, Ziele und Metriken sowie Zielgruppenbestimmungsregeln.

**Beispiel-Eingabeaufforderung:** „Abrufen von Details zur 12345“

+++

+++Erstellen einer A/B-Aktivität

**tool:** `create_ab_activity`

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

+++

+++Erstellen einer Erlebnis-Targeting-Aktivität

**tool:** `create_xt_activity`

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

+++

+++Aktualisieren einer Aktivität

**tool:** `update_activity`

Aktualisieren vorhandener A/B-Tests, Erlebnis-Targeting- oder Automated Personalization-Aktivitäten

Verwendet ein Lese-/Schreibmuster: ruft den aktuellen Status ab, führt Ihre Änderungen zusammen, validiert und sendet die Aktualisierung. Unterstützt A/B-Test-, Erlebnis-Targeting- und Automated Personalization-Aktivitäten; automatische Zuordnungs-, Multivarianz-Test- und Recommendations-Aktivitäten sind schreibgeschützt. Die strukturierten `goal`-, `audience_ids`- und `additional_metrics` werden nur für A/B-Tests und Experience Targeting unterstützt. Automated Personalization-Aktivitäten akzeptieren Aktualisierungen über die reine Feldzusammenführung.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der zu aktualisierenden Aktivität |
| `activity` | Objekt | Ja | Zu aktualisierende Felder (Name, Priorität, Erlebnisse, Standorte, Ziele usw.) |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispiel-Eingabeaufforderung:** „Aktualisieren Sie die 12345, um die Traffic-Zuordnung auf 70/30 zu ändern.“

+++

+++Aktivitätsplanung aktualisieren

**tool:** `update_activity_schedule`

Start- und Enddatum der Aktivität aktualisieren

Aktualisiert den Zeitplan einer Aktivität ohne Änderung der anderen Einstellungen

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `starts_at` | string | Nein | Neues Startdatum (ISO 8601) |
| `ends_at` | string | Nein | Neues Enddatum (ISO 8601) |

**Gibt zurück** Bestätigung der Zeitplanaktualisierung.

**Beispiel-Eingabeaufforderung:** „Aktualisieren Sie den Zeitplan für die A/B-Aktivitäts-12345, die vom 1. Mai bis zum 31. Mai ausgeführt werden soll.“

+++

+++Aktivitätsstatus ändern

**tool:** `update_activity_state`

Aktivitätsstatus ändern (aktivieren, deaktivieren oder pausieren).

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `state` | string | Ja | Neuer Status: `approved` (live/aktiv), `deactivated` (inaktiv), `paused` oder `saved` (Entwurf) |

**Gibt zurück** Der aktualisierte Aktivitätsstatus.

**Beispielaufforderung:** „Aktivitäts-12345 aktivieren“ oder „Homepage-Heldentest anhalten“.

+++

+++Eine Aktivität umbenennen

**tool:** `update_activity_name`

Eine Aktivität umbenennen.

Aktualisiert nur den Namen, ohne die vollständige Konfiguration zu ändern.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `name` | string | Ja | Neuer Aktivitätsname |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Benennen Sie die Aktivität 12345 in „Heldentest der Sommerkampagne“ um.“

+++

+++Aktivitätspriorität ändern

**tool:** `update_activity_priority`

Ändern der Aktivitätspriorität.

Aktivitäten mit höherer Priorität haben Vorrang, wenn mehrere Aktivitäten auf denselben Standort abzielen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `priority` | Ganzzahl | Ja | Neuer Prioritätswert (0-999; höher = höhere Priorität) |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Legen Sie die Priorität der Aktivität 12345 auf 100 fest.“

+++

+++Hinzufügen einer Variante zu einer Aktivität

**tool:** `add_activity_variant`

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

+++

+++Traffic-Aufteilung aktualisieren

**tool:** `update_traffic_split`

Aktualisieren der Traffic-Zuordnung zu Varianten.

Die Prozentsätze müssen genau 100 betragen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die ID der zu ändernden Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab` oder `abt` (XT wird nicht unterstützt — Zielgruppen-spezifisch) |
| `splits` | Objekt | Ja | Name des Wörterbuchzuordnungserlebnisses zu Prozentsatz. Muss alle Erlebnisse enthalten und Summe auf 100 |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Ändern Sie die Traffic-Aufteilung für Aktivitäts-12345 in 70 % Kontrolle und 30 % Variante A.“

+++

+++Variantenangebot ändern

**tool:** `update_variant_offer`

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

+++

+++Entfernen einer Variante aus einer Aktivität

**tool:** `remove_activity_variant`

Erlebnis/Variante aus einer Aktivität entfernen

Entfernt das Erlebnis, bereinigt verwaiste Optionen und gleicht den Traffic gleichmäßig über die verbleibenden Varianten aus.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die ID der zu ändernden Aktivität |
| `activity_type` | string | Ja | Aktivitätstyp: `ab`, `xt` oder `abt` |
| `variant_name` | string | Ja | Name des zu entfernenden Erlebnisses/der zu entfernenden Variante |

**Gibt zurück** Das aktualisierte Aktivitätsobjekt.

**Beispielaufforderung:** „Entfernen des Erlebnisses „Testvariante“ aus der A/B-12345.“

+++

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

+++Erstellen eines HTML-Angebots

**tool:** `create_target_offer`

Erstellen Sie ein neues HTML-Inhaltsangebot.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name des Angebots |
| `content` | string | Ja | HTML oder Textinhalt für das Angebot |
| `workspace_id` | string | Nein | Workspace-ID für das Angebot |

**Gibt zurück** Das erstellte Angebot mit der zugewiesenen ID.

**Beispiel-Eingabeaufforderung:** „Erstellen Sie ein HTML-Angebot mit dem Namen „Banner für den Sommerverkauf“ und einem Werbebanner.“

+++

+++Erstellen eines JSON-Angebots

**tool:** `create_target_json_offer`

Erstellen Sie ein neues JSON-Angebot für die Bereitstellung strukturierter Daten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name des Angebots |
| `content` | Objekt | Ja | JSON-Inhalt des Angebots |
| `workspace_id` | string | Nein | Workspace-ID für das Angebot |

**Gibt zurück** Das erstellte Angebot mit der zugewiesenen ID.

**Beispielaufforderung:** „Erstellen Sie ein JSON-Angebot mit dem Namen „Feature Flags Config“ und Umschalter für Funktionen.“

+++

+++Aktualisieren eines Angebots

**tool:** `update_target_offer`

Vorhandenes Angebot aktualisieren.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `offer_id` | Ganzzahl | Ja | Die eindeutige Kennung des zu aktualisierenden Angebots |
| `name` | string | Nein | Aktualisierter Angebotsname |
| `content` | Zeichenfolge oder Objekt | Nein | Aktualisierter Angebotsinhalt |

**Gibt zurück** Das aktualisierte Angebotsobjekt.

**Beispielaufforderung:** „Aktualisieren der 67890 mit neuen Werbeinhalten.“

+++

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

+++Abrufen einer Zielgruppe

**tool:** `get_target_audience`

Abrufen von Zielgruppendetails, einschließlich Zielgruppenbestimmungsregeln.

Ruft die vollständige Konfiguration einer bestimmten Zielgruppe ab, einschließlich ihrer Zielgruppenbestimmungsregeln und -bedingungen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `audience_id` | Ganzzahl | Ja | Die eindeutige Kennung der Zielgruppe |

**Rückgabe** Vollständige Zielgruppendetails, einschließlich `id`, `name`, `description`, `origin`, Zielgruppenbestimmungsregeln und der Anzahl der zugehörigen Aktivitäten.

**Beispielaufforderung:** „Abrufen von Details für Zielgruppen-12345 und Anzeigen der Zielgruppenbestimmungsregeln.“

+++

+++Erstellen von Zielgruppen

**tool:** `create_target_audience`

Erstellen Sie eine neue Audience mit Zielgruppenbestimmungsregeln.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `name` | string | Ja | Name der Zielgruppe |
| `description` | string | Nein | Beschreibung der Zielgruppe |
| `targetRule` | Objekt | Nein | Zielgruppenbestimmungsregeln (Geografie, Browser, benutzerdefinierte Attribute usw.) |
| `workspace_id` | string | Nein | Workspace-ID für die Zielgruppe |

**Gibt zurück** Die erstellte Zielgruppe mit der zugewiesenen ID.

**Beispielaufforderung:** „Erstellen Sie eine Zielgruppe namens „Mobile Besucher aus Kalifornien“, die auf mobile Benutzer in Kalifornien abzielt.“

+++

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

+++Abrufen eines Berichts zur Aktivitätsleistung

**tool:** `get_activity_performance_report`

Rufen Sie einen Leistungsbericht für eine Aktivität beliebigen Typs ab.

Ruft Konversionsraten, Steigerung und Konfidenzniveaus ab. Unterstützt A/B-Tests, Erlebnis-Targeting, Automated Personalization, automatische Zuordnung, Multivarianz-Tests und Recommendations-Aktivitäten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht (z. B. `last7days`, `last30days` oder benutzerdefinierter Datumsbereich) |

**Rückgaben:** Metriken auf Erlebnisebene (Besucher, Konversionen, Konversionsrate), Steigerungsberechnungen, statistische Konfidenzniveaus und Umsatzmetriken (falls konfiguriert).

**Beispielaufforderung:** „Anzeigen des Leistungsberichts zur 12345 der letzten 30 Tage“

+++

+++Abrufen eines Berichts zu Aktivitätsaufträgen

**tool:** `get_activity_orders_report`

Abrufen eines Berichts zu Bestellungen/Umsatz für eine Aktivität beliebigen Typs.

Unterstützt A/B-Tests, Erlebnis-Targeting, Automated Personalization, automatische Zuordnung, Multivarianz-Tests und Recommendations-Aktivitäten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht |

**Rückgabe:** Anzahl der Bestellungen, Umsatz und durchschnittlicher Bestellwert nach Erlebnis.

**Beispielaufforderung:** „Bericht zu Bestellungen für 12345 abrufen“

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

+++Abrufen eines Analytics for Target-(A4T)-Berichts

**tool:** `get_a4t_report`

Abrufen eines Analytics for Target-(A4T)-Berichts für eine [!DNL Target].

Validiert die A4T-Konfiguration für die Aktivität und führt dann GraphQL-Abfragen für [!DNL Adobe Analytics] aus, um Analytics-seitige Metriken abzurufen. Nur für Aktivitäten verfügbar, für die A4T-Berichte konfiguriert sind.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `activity_id` | Ganzzahl | Ja | Die eindeutige Kennung der [!DNL Target] Aktivität |
| `report_interval` | string | Nein | Zeitraum für den Bericht (z. B. `last7days`, `last30days` oder benutzerdefinierter Datumsbereich) |

**Gibt** Analytics-seitige Metriken für die Aktivität zurück, einschließlich Besucherzahlen, Konversionen, Umsatz und Steigerung nach Erlebnis, die direkt aus [!DNL Adobe Analytics] bezogen werden.

**Beispielaufforderung:** „Ziehen Sie den A4T-Bericht für meinen Checkout-Optimierungstest ab und fassen Sie die Analytics-seitigen Konversionsdaten zusammen.“

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

+++Erstellen eines Antwort-Tokens

**tool:** `create_target_response_token`

Erstellen Sie ein neues benutzerdefiniertes Antwort-Token zum Erfassen zusätzlicher Daten in [!DNL Target].

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `token_name` | string | Ja | Name des Antwort-Tokens |
| `token_type` | string | Ja | Typ des Tokens: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO` oder `CRS` |

**Gibt zurück** Das erstellte Antwort-Token-Objekt.

**Beispielaufforderung:** „Erstellen Sie ein benutzerdefiniertes Antwort-Token namens „campaign_id“ vom Typ „ACTIVITY“.

+++

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

## Recommendations-Tools {#tools-recommendations}

>[!NOTE]
>
>* Für Recommendations-Tools ist ein Recommendations-aktivierter Mandant mit **Target Premium**. Bei Nicht-Premium-Konten werden diese Tools nicht in der Toolliste des Clients angezeigt und die zugrunde liegende API gibt einen 403-Fehler zurück.
>* Diese Tools unterstützen Vorgänge zum Auflisten, Abrufen, Erstellen und Aktualisieren von Kriterien, Sammlungen, Designs, Promotions und Ausschlüssen. Löschvorgänge werden nicht über den MCP-Server verfügbar gemacht.

+++Kriterien

**Tools:** `list_target_criteria`, `get_target_criteria`, `list_target_criteria_by_type`, `get_target_criteria_by_type`, `create_target_criteria`, `update_target_criteria`

Kriterien sind Regeln, die basierend auf einem vorab festgelegten Satz von Besucherverhalten bestimmen, welche Elemente empfohlen werden sollen. Die Kriterien sind in 9 Familien unterteilt: `category`, `custom`, `item`, `cart`, `popularity`, `profileattribute`, `recent`, `sequence`, `userhistory`.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `criteria_id` | Ganzzahl | Zum Abrufen/Aktualisieren | Die eindeutige Kennung der Kriterien |
| `criteria_type` | string | Für typisierte Vorgänge | Eine der 9 Kriterienfamilien |
| `limit` / `offset` | Ganzzahl | Nein | Seitenumbruch |
| `name` | string | Ja (erstellen) | Eindeutiger Name der Kriterien |
| `criteriaTitle` | string | Nein | Titel anzeigen, der im Design über `$criteria.title` verwendet wird |
| `description` | string | Nein | Beschreibung der Kriterien |
| `key` | string | Ja (erstellen/aktualisieren, die meisten Typen) | Empfehlungsschlüssel (z. B. `CURRENT`, `LAST_VIEWED`, `LAST_PURCHASED`, `MOST_VIEWED`, `PROFILE_ATTRIBUTE`) |
| `type` | string | Ja (erstellen/aktualisieren, die meisten Typen) | Empfehlungslogik (z. B. `VIEWED_BOUGHT`, `BOUGHT_CF`, `VIEWED_CF`, `SITE_AFFINITY`, `SIMILARITY`) |
| `configuration` | Objekt | Ja (erstellen/aktualisieren) | Einschlussregeln, Attributgewichtung, Preisfilter und andere familienspezifische Einstellungen |
| `daysCount` | string | Variiert | Berücksichtigter historischer Zeitraum (z. B. `ONE_DAY` bis `TWO_MONTHS`) |

`list_target_criteria` und `get_target_criteria` geben minimale Metadaten mit familienübergreifenden Kriterien zurück (`id`, `name`, `criteriaTitle`, `criteriaGroup`). Verwenden Sie `list_target_criteria_by_type` / `get_target_criteria_by_type` (oder `create_target_criteria` / `update_target_criteria`) mit einem `criteria_type`, um mit der vollständigen, typspezifischen Konfiguration zu arbeiten. Die Feldanforderungen sind je nach Familie unterschiedlich - siehe [!DNL Adobe] [Recommendations-API-Referenz](https://developer.adobe.com/target/administer/recommendations-api/){target="_blank"} für das vollständige Schema pro Typ.

**Gibt zurück** Das Kriterienobjekt oder eine paginierte Liste mit `offset`, `limit`, `total` und `list`.

**Beispielaufforderung:** „Listet alle in diesem Konto konfigurierten Recommendations-Kriterien auf und fasst die verwendeten Algorithmustypen zusammen.“

+++

+++Sammlungen

**Tools:** `list_target_collections`, `get_target_collection`, `create_target_collection`, `update_target_collection`

Sammlungen gruppieren Katalogentitäten nach übereinstimmenden Regeln zur Verwendung in Kriterien und Promotions.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `collection_id` | Ganzzahl | Zum Abrufen/Aktualisieren | Die eindeutige Kennung der Sammlung |
| `limit` / `offset` | Ganzzahl | Nein | Seitenumbruch |
| `name` | string | Ja | Eindeutiger Name der Sammlung (max. 250 Zeichen) |
| `description` | string | Nein | Beschreibung der Sammlung (max. 1000 Zeichen) |
| `rules` | Array | Ja | 1-1000 Regeln (`attribute` + Operator/Operand), die die Katalogmitgliedschaft bestimmen |

**Gibt zurück** Das Sammlungsobjekt, einschließlich `id`, `name`, `description`, `rules` und zuletzt geänderter Metadaten.

**Beispielaufforderung:** „Welche Sammlungen habe ich und nach welchen Katalogattributen filtern sie?“

+++

+++Designs

**Tools:** `list_target_designs`, `get_target_design`, `create_target_design`, `update_target_design`

Designs sind Velocity- oder HTML-Vorlagen, die steuern, wie empfohlene Entitäten gerendert werden.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `design_id` | Ganzzahl | Zum Abrufen/Aktualisieren | Die eindeutige Kennung des Designs |
| `limit` / `offset` | Ganzzahl | Nein | Seitenumbruch |
| `includeScript` | Boolescher Wert | Nein | Gibt an, ob der Vorlageninhalt des Designs einbezogen werden soll |
| `name` | string | Ja | Eindeutiger Name des Designs (max. 250 Zeichen) |
| `script` | string | Ja | Geschwindigkeitsvorlage, die auf mindestens ein Entitätsobjekt verweist (max. 65.000 Zeichen) |
| `type` | string | Nein | Inhaltstyp des Skripts: `HTML`, `JSON` oder `OTHER` (Standard) |

**Gibt zurück** Das Design-Objekt, einschließlich `id`, `name`, `script` und `type`.

**Beispielaufforderung:** „Welche Designs und Sammlungen habe ich für Recommendations konfiguriert?“

+++

+++Promotions

**Tools:** `list_target_promotions`, `get_target_promotion`, `create_target_promotion`, `update_target_promotion`

Promotions zwingen bestimmte Entitäten zu Recommendations-Ergebnissen, wobei sie den Kriterien und Backup-Recommendations vorgehen.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `promotion_id` | Ganzzahl | Zum Abrufen/Aktualisieren | Die eindeutige Kennung der Promotion |
| `limit` / `offset` | Ganzzahl | Nein | Seitenumbruch |
| `name` | string | Ja | Eindeutiger Name der Promotion (max. 250 Zeichen) |
| `type` | string | Ja | Derzeit wird nur `EXTERNAL` unterstützt |
| `key` | string | Nein | Promotion-Schlüssel: `CURRENT`, `LAST_VIEWED`, `LAST_PURCHASED`, `MOST_VIEWED` oder `PROFILE_ATTRIBUTE` |
| `attribute` | string | Nein | Name des Profilattributs, anwendbar, wenn `key` `PROFILE_ATTRIBUTE` ist |
| `schedule` | Objekt | Nein | Start-/Endzeitfenster, in dem die Promotion gilt |
| `order` | Objekt | Nein | Bestellkonfiguration für hochgestufte Entitäten |
| `configuration` | Objekt | Nein | Sammlungsreferenz für die hochgestuften Elemente (wird verwendet, wenn `rules` leer ist) |
| `rules` | Array | Nein | Einschlussregeln, die bestimmen, welche Entitäten gefördert werden sollen |

**Gibt zurück** Das Objekt der Promotion.

**Beispiel-Eingabeaufforderung:** „Erstellen Sie eine externe Promotion, die bis Ende August die Sammlung „Backpacking-Zelte“ enthält.“

+++

+++Ausnahmen

**Tools:** `list_target_exclusions`, `get_target_exclusion`, `create_target_exclusion`, `update_target_exclusion`

Ausschlüsse entfernen übereinstimmende Entitäten aus den Empfehlungen. Ausschlüsse gelten kontenweit, für alle Kriterien und Aktivitäten.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `exclusion_id` | Ganzzahl | Zum Abrufen/Aktualisieren | Die eindeutige Kennung des Ausschlusses |
| `name` | string | Ja | Eindeutiger Name des Ausschlusses (max. 250 Zeichen) |
| `description` | string | Nein | Beschreibung des Ausschlusses (max. 1000 Zeichen) |
| `rule` | Objekt | Nein | Eine einzelne Regel (`attribute` + Operator/Operand), die auszuschließende Entitäten identifiziert |

**Gibt zurück** Das Ausschlussobjekt.

**Beispielaufforderung:** „Sind derzeit alle kontoweiten Ausschlüsse konfiguriert, und wornach werden sie gefiltert?“

+++

+++Katalog

**Tools:** `get_target_entity`, `search_target_catalog`

Schreibgeschützte Tools zur Überprüfung des Produkt-/Inhaltskatalogs für Recommendations. Es gibt kein Tool zum Erstellen, Aktualisieren oder Löschen von Katalogentitäten über den MCP-Server.

| Parameter | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `catalog_entity_id` | string | Ja (GET) | Die Katalogentitäts-ID (z. B. SKU) |
| `environment_id` | string | Nein | Umgebung zum Suchen der Entität in |
| `query` | Objekt | Ja (Suche) | Ein `meta` Block (erfordert `environmentId`, optionale `displayFields`) plus ein `query` Block (`simple` oder `compound`); einfache Abfragen verwenden `queryFields`, ein `operator` (`eq`, `lt`, `gt`, `le`, `ge`, `contains`) und ein `matchValue` |

**Gibt zurück:** `get_target_entity` gibt die Katalogattribute der Entität zurück. `search_target_catalog` gibt Übereinstimmungen in einem `entities` Array zurück. Feldnamen in `query` müssen echte Katalogattribute sein, die für den Mandanten konfiguriert sind.

**Beispielaufforderung:** „Durchsuchen Sie den Katalog nach Produkten mit einem Bestand unter 1.000.“

+++

## Tools-Zusammenfassung {#tools-summary}

| Kategorie | Count | Werkzeuge |
|---|---|---|
| Aktivität | 13 | `list_target_activities`, `get_activity`, `create_ab_activity`, `create_xt_activity`, `update_activity`, `update_activity_schedule`, `update_activity_state`, `update_activity_name`, `update_activity_priority`, `add_activity_variant`, `update_traffic_split`, `update_variant_offer`, `remove_activity_variant` |
| Angebot | 5 | `list_target_offers`, `get_target_offer`, `create_target_offer`, `create_target_json_offer`, `update_target_offer` |
| Zielgruppe | 4 | `list_target_audiences`, `get_target_audience`, `create_target_audience`, `update_target_audience` |
| mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Eigenschaft | 1 | `list_target_properties` |
| Berichterstellung | 4 | `get_activity_performance_report`, `get_activity_orders_report`, `get_activity_report_by_name`, `get_a4t_report` |
| Vorschau | 1 | `preview_activity` |
| Antwort-Token | 2 | `list_target_response_tokens`, `create_target_response_token` |
| Revision | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| AT.js | 2 | `get_atjs_settings`, `get_atjs_versions` |
| Vorlage | 1 | `list_target_templates` |
| Recommendations | 24 | `list_target_criteria`, `get_target_criteria`, `list_target_criteria_by_type`, `get_target_criteria_by_type`, `create_target_criteria`, `update_target_criteria`, `list_target_collections`, `get_target_collection`, `create_target_collection`, `update_target_collection`, `list_target_designs`, `get_target_design`, `create_target_design`, `update_target_design`, `list_target_promotions`, `get_target_promotion`, `create_target_promotion`, `update_target_promotion`, `list_target_exclusions`, `get_target_exclusion`, `create_target_exclusion`, `update_target_exclusion`, `get_target_entity`, `search_target_catalog` |
| **Gesamt** | **62** | |

## Verwandte Ressourcen {#tools-related}

* [Arbeiten mit MCP-Clients](target-mcp.md)
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
