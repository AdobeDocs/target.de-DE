---
solution: Target
product: target
title: Arbeiten mit MCP-Clients
description: Erfahren Sie, wie Sie Adobe Target mithilfe des MCP-Servers mit MCP-Clients verbinden
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 6e7fa766f3da76f3e9d1f4527bfe50b9e703db4e
workflow-type: tm+mt
source-wordcount: '2376'
ht-degree: 1%

---

# Arbeiten mit MCP-Clients {#target-mcp}

>[!BEGINSHADEBOX]

Inhaltsverzeichnis:

* **[Arbeiten mit MCP-Clients](target-mcp.md)**
* [MCP Server Tools-Referenz](target-mcp-tools-reference.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server ist derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** verfügbar. In zukünftigen Versionen wird Unterstützung für weitere MCP-kompatible Anwendungen hinzugefügt.

Mit der [!DNL Adobe Target] MCP-Integration können Sie A/B-Tests, Personalisierungsaktivitäten und Recommendations-Kriterien direkt von Ihrem KI-Assistenten aus überprüfen, analysieren und verwalten. Verwandeln Sie die Lese- und Schreib-APIs von [!DNL Target] in Nur-Sprache-Workflows. Überprüfen Sie Ihr Experimentportfolio, überprüfen Sie Leistungsberichte, verwalten Sie Audiences und Angebote und führen Sie gesteuerte Aktionen durch, ohne die Benutzeroberfläche zu navigieren oder API-Aufrufe zu schreiben. Auf dieser Seite wird erläutert, wie die Integration funktioniert, was Sie damit tun können und wie Sie beginnen können.

>[!IMPORTANT]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration, und die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen vor der produktiven Verwendung in einer Sandbox-Umgebung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing- und Optimierungsteams verlassen sich zunehmend auf Chat-basierte Anwendungen und Entwickler-Tools - wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio - um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

[!DNL Adobe Target] bietet jetzt einen MCP-Server, der Experimentier-, Personalisierungs- und Recommendations-Vorgänge direkt in jeder MCP-kompatiblen Anwendung aufzeigt. [!DNL Adobe Target] fungiert als Entscheidungs- und Ausführungsebene, während der KI-Assistent Argumentation und Erläuterung verarbeitet. So erhalten Teams schneller Zugriff auf Optimierungseinblicke, ohne durch mehrere Produktbildschirme zu navigieren oder Abfragen für die [!DNL Adobe Target] REST-API zu schreiben.

## Wichtigste Funktionen {#mcp-capabilities}

Der [!DNL Adobe Target] MCP-Server bietet Lese- und Schreibzugriff auf Aktivitäten, Zielgruppen, Angebote, Empfehlungen und die Implementierungskonfiguration. Mit der Integration können Sie:

* **Experimente überprüfen und überprüfen** - Sie erhalten Links zu Status, Leistung, Änderungsverlauf und QA-Vorschau für jede Aktivität, ohne in der Benutzeroberfläche zu navigieren.
* **Ergebnisse analysieren** - Abrufen von Performance-, Umsatz- und A4T-Berichten für A/B-, XT-, AP- und Auto-Target-Aktivitäten.
* **Aktivitäten verwalten** - Erstellen, Aktualisieren und Aktivieren von A/B- und XT-Aktivitäten; Anpassen von Traffic-Aufspaltungen, Varianten, Zeitplänen und Prioritäten.
* **Audiences und Angebote verwalten** - Auflisten, Überprüfen und Erstellen von Audiences, HTML-Angeboten und JSON-Angeboten.
* **Explore Recommendations-**: Auflisten und Überprüfen von Kriterien und Warenkorb-basierten Algorithmen.
* **Audit-Implementierung** - Überprüfen Sie at.js-Einstellungen, Antwort-Token und den Revisionsverlauf pro Entität.

>[!NOTE]
>
>Schreibvorgänge (Erstellen, Aktualisieren, Aktivieren, Deaktivieren) schließen Sicherheitsanmerkungen ein. Ohne ausdrückliche Benutzerbestätigung werden keine Änderungen ausgeführt.

## Verfügbare Tools {#mcp-tools}

Der [!DNL Adobe Target] MCP-Server stellt 52 Tools bereit. Lese-Tools stehen allen verbundenen Benutzern mit Anzeigeberechtigungen zur Verfügung. Schreib-Tools erfordern die Rolle des Bearbeiters oder der genehmigenden Person.

### Aktivitäts-Tools - Lesen

| Tool | Beschreibung |
|---|---|
| `list_target_activities` | Auflisten von Aktivitäten mit Server-seitiger Filterung nach Status, Typ, Name, Datum, Priorität, Mbox und Arbeitsbereich |
| `list_all_target_activities` | Abrufen aller Aktivitäten, die mit Filtern übereinstimmen, automatisches Paginieren der Ergebnisse |
| `get_ab_activity` | Vollständige Details zu einer bestimmten A/B-Aktivität abrufen |
| `get_xt_activity` | Vollständige Details zu einer bestimmten Experience Targeting (XT)-Aktivität abrufen |
| `get_abt_activity` | Vollständige Details zu einer bestimmten Automated Personalization (AP)-Aktivität abrufen |

### Aktivitäts-Tools - Schreiben

| Tool | Beschreibung |
|---|---|
| `create_ab_activity` | Erstellen einer neuen A/B-Test -Aktivität |
| `create_xt_activity` | Erstellen einer neuen Experience Targeting-(XT)-Aktivität |
| `create_activity_from_modifications` | Erstellen einer XT-Aktivität aus JavaScript-Änderungen |
| `update_ab_activity` | Aktualisieren einer vorhandenen A/B-Aktivität |
| `update_xt_activity` | Vorhandene XT-Aktivität aktualisieren |
| `update_abt_activity` | Vorhandene Automated Personalization-Aktivität aktualisieren |
| `update_activity_state` | Aktivieren, Deaktivieren, Pausieren oder Archivieren einer Aktivität |
| `update_activity_schedule` | Start- und Enddatum einer Aktivität aktualisieren |
| `update_activity_priority` | Priorität einer Aktivität aktualisieren |
| `update_activity_name` | Eine Aktivität umbenennen |
| `add_activity_variant` | Hinzufügen einer neuen Variante (Erlebnis) zu einer Aktivität |
| `update_traffic_split` | Aktualisieren der Traffic-Zuordnung zwischen Varianten |
| `update_variant_offer` | Ändern des Angebots oder der VEC-Änderungen für eine Variante |
| `remove_activity_variant` | Entfernen einer Variante aus einer Aktivität |

### Angebotswerkzeuge

| Tool | Beschreibung |
|---|---|
| `list_target_offers` | Auflisten von Angeboten mit Server-seitiger Filterung und Sortierung |
| `list_all_target_offers` | Abrufen aller Angebote, die mit Filtern übereinstimmen, automatische Paginierung |
| `get_target_offer` | Abrufen von Details zu einem bestimmten Angebot |
| `create_target_offer` | Erstellen eines neuen HTML-Angebots |
| `create_target_json_offer` | Erstellen eines neuen JSON-Angebots |
| `update_target_offer` | Vorhandenes HTML-Angebot aktualisieren |

### Zielgruppen-Tools

| Tool | Beschreibung |
|---|---|
| `list_target_audiences` | Auflisten von Zielgruppen mit Server-seitiger Filterung und Sortierung |
| `create_target_audience` | Erstellen einer Audience mit optionalen Zielgruppenbestimmungsregeln |

### Mbox- und Orts-Tools

| Tool | Beschreibung |
|---|---|
| `list_target_mboxes` | Auflisten von Mboxes mit Filtern und Sortieren |
| `list_all_target_mboxes` | Alle Mboxes abrufen, die mit Filtern übereinstimmen, automatische Paginierung |
| `get_target_mbox` | Abrufen von Details zu einer bestimmten Mbox nach Namen |
| `list_target_mbox_profile_attributes` | Auflisten aller mit Mboxes verknüpften Profilattribute |

### Eigenschaften

| Tool | Beschreibung |
|---|---|
| `list_target_properties` | Alle Target-Eigenschaften auflisten |

### Reporting- und Insights-Tools

| Tool | Beschreibung |
|---|---|
| `get_ab_performance_report` | Abrufen eines Leistungsberichts für eine A/B-, automatische Zuordnungs- oder automatische Targeting-Aktivität |
| `get_ab_orders_report` | Abrufen von Bestellungen und Umsätzen für eine A/B- oder automatische Targeting-Aktivität |
| `get_xt_performance_report` | Abrufen eines Leistungsberichts für eine XT-Aktivität |
| `get_xt_orders_report` | Abrufen eines Berichts zu Bestellungen und Umsatz für eine XT-Aktivität |
| `get_apt_performance_report` | Abrufen eines Leistungsberichts für eine AP- oder automatische Targeting-Aktivität |
| `get_activity_insights` | Nach einer Aktivität mit Namen suchen und detaillierte Leistungseinblicke erhalten |
| `get_a4t_report` | Abrufen des Analytics for Target-(A4T)-Berichts für eine Aktivität |

### Recommendations-Tools

| Tool | Beschreibung |
|---|---|
| `list_target_criteria` | Auflisten aller Recommendations-Kriterien |
| `get_target_criteria` | Abrufen von Details zu bestimmten Recommendations-Kriterien |
| `update_target_criteria_cart` | Aktualisieren von auf dem Recommendations-Warenkorb basierenden Kriterien |

### Implementierungs- und Konfigurationstools

| Tool | Beschreibung |
|---|---|
| `get_atjs_settings` | Abrufen der AT.js-Einstellungen und -Konfiguration |
| `get_atjs_versions` | Verfügbare AT.js-Versionen abrufen |
| `list_target_response_tokens` | Auflisten aller Antwort-Token in Ihrem Target-Mandanten |
| `create_target_response_token` | Erstellen eines neuen benutzerdefinierten Antwort-Tokens |

### Audit- und Revisionswerkzeuge

| Tool | Beschreibung |
|---|---|
| `get_target_revisions` | Auditprotokoll für einen Ressourcentyp abrufen, gefiltert nach Autor |
| `get_target_entity_revisions` | Abrufen aller Revisionen einer bestimmten Entität nach ID |

### Hilfsprogramme

| Tool | Beschreibung |
|---|---|
| `preview_activity` | Erzeugen von QA-Vorschau-URLs für eine Target-Aktivität |
| `create_page_delivery_segment` | Erstellen eines Seitenbereitstellungssegments für VEC-Aktivitäts-Targeting |
| `list_target_templates` | Verfügbare MCP-Ressourcen und -Vorlagen auflisten |
| `debug_token_info` | Überprüfen der aktuellen OAuth-Token-Bereiche und -Ansprüche |

## Anwendungsszenarien {#mcp-use-cases}

Die folgenden Beispiele zeigen, wie Sie mit dem [!DNL Adobe Target] MCP-Server in natürlicher Sprache interagieren:

| Ziel | Beispiel-Eingabeaufforderung |
|---|---|
| **Experimentstatus-Audit** | „Welche A/B-Tests sind derzeit auf der Homepage aktiv? Anzeigen des Status, der Traffic-Zuordnung und der Ausführungsdauer jeder Aktivität.“ |
| **Leistungsüberprüfung** | „Zeigen Sie mir alle aktiven Tests, die statistische Signifikanz erreicht haben - welche Erlebnisse gewinnen?“ |
| **Umsatzanalyse** | „Rufen Sie den Bericht zu Bestellungen und Umsatz für die Aktivität AT4821 ab und fassen Sie zusammen, welches Erlebnis pro Besucher den meisten Umsatz generiert.“ |
| **A4T-Reporting** | „Rufen Sie den A4T-Bericht für meinen Checkout-Optimierungstest ab und fassen Sie die Analytics-seitigen Konversionsdaten zusammen.“ |
| **Aktivitätsverwaltung** | „Pausieren Sie die Aktivität 98765 und aktualisieren Sie die Priorität der Aktivität 11111 auf 200.“ |
| **Aktivitätserkenntnisse** | „Erhalten Sie Einblicke in meinen Test für „Summer Sale Banner“ - wie sieht die Leistung aus und gibt es Anomalien?“ |
| **Zielgruppen-Management** | „Listen Sie alle Audiences auf, die mobile Benutzende ansprechen, und zeigen Sie mir, welchen Aktivitäten sie zugeordnet sind.“ |
| **QS und Vorschau** | „Generieren Sie QA-Vorschau-URLs für die Aktivität 12345, damit ich vor der Aktivierung alle Varianten überprüfen kann.“ |
| **Überprüfung von Recommendations** | „Listen Sie alle in diesem Konto konfigurierten Recommendations-Kriterien auf und fassen Sie die verwendeten Algorithmustypen zusammen.“ |
| **Implementierungsprüfung** | „Welche Version von at.js ist konfiguriert und welche Antwort-Token sind derzeit aktiv?“ |
| **Audit ändern** | „Zeigen Sie mir alle Änderungen, die in den letzten 30 Tagen an der Aktivität 98765 vorgenommen wurden, und wer sie vorgenommen hat.“ |

## exemplarische Vorgehensweisen für Anwendungsfälle {#mcp-use-case-walkthroughs}

In den folgenden exemplarischen Vorgehensweisen wird beschrieben, wie Sie allgemeine Aufgaben mithilfe von Eingabeaufforderungen in natürlicher Sprache mit dem [!DNL Adobe Target] MCP-Server durchführen.

+++Erstellen von A/B-Tests

**Eingabeaufforderung:**
„Erstellen Sie einen A/B-Test namens „Homepage Hero Image Test“ mit zwei Erlebnissen: „Control“ zeigt den aktuellen Helden und „Variant“ zeigt ein neues Hero-Bild mit Sommerthema. Targeting der Homepage-Mbox.“

Der KI-Assistent verwendet das `create_ab_activity`-Tool, um die Aktivität mit der von Ihnen beschriebenen Konfiguration zu erstellen. Das Tool gibt die neue Aktivitäts-ID und eine Bestätigung der erstellten Erlebnisse zurück.

+++

+++Überprüfen der Aktivitätsleistung

**Eingabeaufforderung:**
„Zeigen Sie mir die Leistungsmetriken für meine Aktivität „Checkout-Flussoptimierung“ in den letzten 30 Tagen.“

Der KI-Assistent verwendet `get_ab_performance_report` oder `get_xt_performance_report` (je nach Aktivitätstyp), um Konversionsraten, Besucherzahlen und andere Metriken für das angegebene Zeitfenster abzurufen.

+++

+++Angebote verwalten

**Eingabeaufforderung:**
„Erstellen Sie ein HTML-Angebot mit dem Namen „Banner für den Sommerverkauf“ und einem Werbebanner, das „20 % Rabatt auf alle Sommerartikel“ enthält.“

Der KI-Assistent verwendet das `create_target_offer`-Tool, um das Angebot mit dem von Ihnen angegebenen HTML-Inhalt zu erstellen, und gibt eine Bestätigung mit der neuen Angebots-ID zurück.

+++

+++Erstellen einer Zielgruppe

**Eingabeaufforderung:**
„Erstellen Sie eine Zielgruppe namens „Mobile Besucher aus Kalifornien“, die Benutzende auf Mobilgeräten mit Standort in Kalifornien anspricht.“

Der KI-Assistent verwendet das `create_target_audience`-Tool mit den entsprechenden Zielgruppenbestimmungsregeln, die aus Ihrer Beschreibung abgeleitet wurden.

+++

+++QA-Vorschau-Links erzeugen

**Eingabeaufforderung:**
„Generieren Sie Vorschau-URLs für 12345, damit ich jedes Erlebnis testen kann.“

Der KI-Assistent verwendet das `preview_activity`-Tool, um anklickbare URLs zu generieren, die das Audience-Targeting umgehen, sodass Sie jedes Erlebnis direkt in Ihrem Browser anzeigen können.

+++

+++Experience Targeting-Aktivität erstellen

**Eingabeaufforderung:**
„Erstellen Sie eine Experience Targeting-Aktivität namens „Geo Personalization&quot;, die verschiedene Hero-Banner für Besuchende aus verschiedenen Regionen anzeigt.“

Der KI-Assistent verwendet `create_xt_activity`, um die Aktivität mit einer zielgruppenbasierten Erlebniszuordnung entsprechend den von Ihnen beschriebenen Regionen zu erstellen.

+++

+++Planen einer Aktivität

**Eingabeaufforderung:**
„Aktualisieren Sie den Zeitplan für die Aktivität 12345, die am 1. Mai beginnen und am 31. Mai enden soll.“

Der KI-Assistent verwendet das `update_activity_schedule`-Tool, um das neue Start- und Enddatum auf die Aktivität anzuwenden.

+++

## Voraussetzungen  {#mcp-prerequisites}

Bevor Sie den [!DNL Adobe Target] MCP-Server an Ihren MCP-Client anschließen, stellen Sie Folgendes sicher:

* Sie verfügen über eine aktive [!DNL Adobe Target] (Adobe Experience Cloud-Abonnement) mit einer Adobe Experience Platform-Organisation.
* Sie haben eine unterstützte MCP-kompatible Anwendung (derzeit Claude Web, Claude Desktop, Claude Code, Cursor oder ChatGPT).
* Sie haben [!DNL Adobe Target] Berechtigungen in Adobe Admin Console konfiguriert:
   * **Beobachterrolle** schreibgeschützte Tools
   * **Editor** Rolle: Lesen und Erstellen von Tools
   * **Genehmiger** Rolle: Lesen + Erstellen + Aktivieren/Deaktivieren von Tools

## MCP-Server [!DNL Adobe Target] {#mcp-connect}

>[!NOTE]
>
>Der [!DNL Adobe Target] MCP-Server verwendet OAuth 2.0 zur Authentifizierung. Wenn Sie ein Target-MCP-Tool zum ersten Mal verwenden, werden Sie zur Adobe Experience Cloud weitergeleitet, um sich anzumelden, Ihr Unternehmen auszuwählen und die angeforderten Berechtigungen zu erteilen. Es sind keine statischen Anmeldeinformationen erforderlich.

**Verbindung von Claude Desktop oder Claude Web herstellen:**

1. Öffnen Sie Ihre MCP-Client-Einstellungen und fügen Sie einen neuen MCP-Server hinzu.
1. Server-URL eingeben: `https://targetmcp.adobe.io/mcp`
1. Wenn Sie dazu aufgefordert werden, vervollständigen Sie die OAuth-Anmeldung bei Adobe IMS mit Ihren Adobe Experience Cloud-Anmeldeinformationen.
1. Nach der Authentifizierung sind alle Tools sofort verfügbar. „Alle aktiven Target-Aktivitäten auflisten“ versuchen, die Verbindung zu überprüfen.

**Verbindung von Claude Code herstellen:**

Fügen Sie Ihrer Claude Code-MCP-Konfiguration Folgendes hinzu:

```json
{
  "mcpServers": {
    "adobe-target": {
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

Schließen Sie den OAuth-Browser-Fluss ab, wenn Sie bei der ersten Verwendung dazu aufgefordert werden.

**Verbindung von Cursor:** herstellen

1. Öffnen Sie **Cursor** und navigieren Sie zu **Einstellungen** → **MCP** → **Neuen globalen MCP-Server hinzufügen**.
1. Fügen Sie die folgende Konfiguration hinzu:

```json
{
  "mcpServers": {
    "target": {
      "type": "streamable-http",
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

1. Speichern Sie die Konfiguration. Der [!DNL Target] MCP-Server wird auf den verfügbaren MCP-Servern angezeigt.

>[!TIP]
>
>Wenn Aktivitäten oder Daten aus der falschen Organisation angezeigt werden, melden Sie sich vollständig von Adobe Experience Cloud ab, verbinden Sie den MCP-Server erneut und wählen Sie während der erneuten Authentifizierung sorgfältig die richtige Organisation aus.

## Fehlerbehebung {#mcp-troubleshooting}

+++OAuth-Fluss schlägt fehl oder wird falsch umgeleitet

1. Melden Sie sich vollständig von Adobe Experience Cloud ab.
1. Löschen Sie Browser-Cookies für adobe.com Domains.
1. Wiederholen Sie den Authentifizierungsfluss.
1. Stellen Sie sicher, dass Sie bei Aufforderung die richtige Organisation auswählen.
+++

+++Aktivitäten oder Daten aus der falschen Organisation werden angezeigt

1. Melden Sie sich vollständig von Adobe Experience Cloud ab.
1. Trennen Sie die Verbindung zum MCP-Server und stellen Sie sie in den Client-Einstellungen wieder her.
1. Wählen Sie bei der erneuten Authentifizierung sorgfältig die richtige Organisation aus.
+++

+++Ein Tool gibt eine Fehlermeldung zurück

1. Stellen Sie sicher, dass Sie in [!DNL Adobe Target] über die erforderlichen Berechtigungen für den Vorgang verfügen (siehe [Voraussetzungen](#mcp-prerequisites)).
1. Überprüfen Sie, ob die referenzierten Ressourcen - Aktivitäten, Angebote, Zielgruppen - in Ihrer Organisation vorhanden sind.
1. Überprüfen Sie, ob Aktivitäts-IDs und andere Kennungen korrekt sind.
+++

+++Verbindung mit dem MCP-Server nicht möglich

1. Überprüfen Sie Ihre Internetverbindung.
1. Vergewissern Sie sich, dass die MCP-Server-URL in Ihrer Client-Konfiguration korrekt eingegeben wurde.
1. Versuchen Sie, den Server aus den MCP-Client-Einstellungen zu entfernen und erneut hinzuzufügen.
+++

## Sicherheit und Berechtigungen {#mcp-security}

Der [!DNL Adobe Target] MCP-Server kann nur auf Daten zugreifen, die Ihr Adobe-Benutzerkonto anzeigen oder ändern darf. Bei allen Vorgängen werden Ihre [!DNL Target] Rollenzuweisungen und Arbeitsbereichsberechtigungen berücksichtigt.

Der -Server fordert die folgenden OAuth-Bereiche an:

* `AdobeID` - Grundlegende Adobe-Identität
* `openid` - OpenID Connect-Authentifizierung
* `additional_info.projectedProductContext` - Mandantenerkennung
* `read_organizations` — Betrieb auf Organisationsebene
* `additional_info.roles` - Rollenbasierte Zugriffssteuerung

OAuth-Token werden bei jeder Anfrage anhand von Adobe IMS validiert, werden nicht dauerhaft vom MCP-Server gespeichert und die gesamte Kommunikation verwendet HTTPS.

## Häufig gestellte Fragen {#mcp-faq}

+++Welche MCP-Clients werden unterstützt?

Der [!DNL Adobe Target] MCP-Server ist derzeit verfügbar für **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT**. Die Unterstützung für weitere MCP-kompatible Anwendungen kann in zukünftigen Versionen hinzugefügt werden.
+++

+++Auf welche [!DNL Adobe Target] Objekte kann ich über MCP zugreifen?

Sie können auf Aktivitäten (A/B, XT, AP), Zielgruppen, Angebote, Eigenschaften, Mboxes, Recommendations-Kriterien, Antwort-Token, at.js-Konfiguration, A4T-Berichte und den Überarbeitungsverlauf der Entität zugreifen. Lese- und Schreibvorgänge werden in 52 Tools unterstützt - Schreibvorgänge erfordern die entsprechende Rolle und eine explizite Bestätigung.
+++

+++Kann der MCP-Server Aktivitäten erstellen oder ändern?

Ja. Zusätzlich zu Lesevorgängen stellt der Server Schreibvorgänge bereit, mit denen Sie Aktivitäten erstellen, anhalten, Prioritäten aktualisieren, Traffic-Aufspaltungen anpassen können und vieles mehr. Schreibvorgänge folgen demselben Berechtigungsmodell wie die [!DNL Adobe Target]-Benutzeroberfläche - Sie benötigen die entsprechende Rolle, um Änderungen vorzunehmen, und es wird keine Aktion ohne explizite Benutzerbestätigung ausgeführt.
+++

+++Benötige ich Entwicklerzugriff, um den MCP-Server zu verwenden?

Nein. Der MCP-Server ist sowohl für Marketing- als auch für technische Personas konzipiert. Marketing-Experten können damit interagieren, indem sie natürliche Spracheingaben in jedem unterstützten MCP-Client verwenden, während Entwickler sie in Tools wie Claude Code oder Cursor verwenden können.
+++

+++Werden meine [!DNL Adobe Target] an den MCP-Client-Anbieter gesendet?

Wenn Sie eine Eingabeaufforderung senden, kann der MCP-Client relevanten Kontext (einschließlich [!DNL Adobe Target] vom MCP-Server zurückgegebenen Daten) zur Verarbeitung an sein Modell senden. Überprüfen Sie die Datenschutz- und Datenverarbeitungsrichtlinien Ihres MCP-Client-Anbieters, bevor Sie eine Verbindung zu Produktionsdaten herstellen. Die Datenverarbeitung in Adobe unterliegt den [Datenschutzrichtlinien von Adobe ](https://www.adobe.com/de/privacy.html) den [Datenschutzbestimmungen](https://www.adobe.com/go/dpt-ww).
+++

+++Können Schreibvorgänge zu unbeabsichtigten Änderungen an Live-Aktivitäten führen?

Schreib-Tools umfassen Sicherheitsanmerkungen und Bestätigungsgates. Vor einer zustandsändernden Aktion - z. B. Aktivieren einer Aktivität, Ändern der Priorität oder Aktualisieren der Traffic-Zuordnung - zeigt der Server eine strukturierte Bestätigung mit dem betroffenen Objekt, der geschätzten Traffic-Auswirkung und dem erforderlichen expliziten Genehmigungsschritt an. Änderungen werden erst vorgenommen, wenn sie bestätigt wurden.
+++

+++Welche Berechtigungen benötige ich in [!DNL Adobe Target]?

Die Rolle **Beobachter** gewährt mindestens Zugriff auf alle Lesetools. **Editor**-Rolle ermöglicht das Erstellen von Aktivitäten, Audiences und Angeboten. **Genehmiger** zum Aktivieren, Deaktivieren oder Archivieren von Aktivitäten ist eine Rolle erforderlich. Wenden Sie sich an Ihren [!DNL Adobe Target], wenn Sie sich bezüglich Ihrer aktuellen Zugriffsebene nicht sicher sind.
+++

+++Kann ich den MCP-Server für mehrere Target-Organisationen oder -Eigenschaften verwenden?

Der MCP-Server führt Vorgänge für die Organisation durch, die mit Ihren authentifizierten Adobe IMS-Anmeldeinformationen verknüpft ist. Wenn Sie innerhalb dieser Organisation Zugriff auf mehrere Eigenschaften haben, können Sie mit dem `list_target_properties`-Tool eine Abfrage nach Eigenschaften durchführen und nachfolgende Anfragen entsprechend filtern.
+++

## Verwandte Ressourcen {#mcp-related}

* [MCP Server Tools-Referenz](target-mcp-tools-reference.md)
* [Dokumentation zum Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Admin-API-Referenz](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [Cursor-Dokumentation](https://docs.cursor.com/){target="_blank"}
