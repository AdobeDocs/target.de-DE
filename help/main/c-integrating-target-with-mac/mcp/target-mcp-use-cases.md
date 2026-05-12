---
solution: Target
product: target
title: Adobe Target MCP-Server - Anwendungsfälle und exemplarische Vorgehensweisen
description: Erkunden Sie häufige Anwendungsfälle und schrittweise Anleitungen für den Adobe Target MCP-Server.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 1%

---

# [!DNL Adobe Target] MCP-Server - Anwendungsfälle und exemplarische Vorgehensweisen {#target-mcp-use-cases}

>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt.

Auf dieser Seite erfahren Sie, was Sie mit dem [!DNL Adobe Target] MCP-Server mithilfe von Eingabeaufforderungen in natürlicher Sprache erreichen können, von Schnellsuchen bis hin zu mehrstufigen Analyse- und Berichtsaufgaben.

>[!IMPORTANT]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration, und die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen vor der produktiven Verwendung in einer Sandbox-Umgebung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Anwendungsszenarien {#mcp-use-cases}

Die folgenden Beispiele zeigen, wie Sie mit dem [!DNL Adobe Target] MCP-Server in natürlicher Sprache interagieren:

| Ziel | Beispiel-Eingabeaufforderung |
|---|---|
| **Experimentstatus-Audit** | „Welche A/B-Tests sind derzeit auf der Homepage aktiv? Anzeigen des Status, der Traffic-Zuordnung und der Ausführungsdauer jeder Aktivität.“ |
| **Leistungsüberprüfung** | „Zeigen Sie mir alle aktiven Tests, die statistische Signifikanz erreicht haben - welche Erlebnisse gewinnen?“ |
| **Umsatzanalyse** | „Rufen Sie den Bericht zu Bestellungen und Umsatz für die Aktivität AT4821 ab und fassen Sie zusammen, welches Erlebnis pro Besucher den meisten Umsatz generiert.“ |
| **A4T-Reporting** | „Rufen Sie den A4T-Bericht für meinen Checkout-Optimierungstest ab und fassen Sie die Analytics-seitigen Konversionsdaten zusammen.“ |
| **Aktivitätserkenntnisse** | „Erhalten Sie Einblicke in meinen Test für „Summer Sale Banner“ - wie sieht die Leistung aus und gibt es Anomalien?“ |
| **Zielgruppen-Management** | „Listen Sie alle Audiences auf, die mobile Benutzende ansprechen, und zeigen Sie mir, welchen Aktivitäten sie zugeordnet sind.“ |
| **QS und Vorschau** | „Generieren Sie QA-Vorschau-URLs für die Aktivität 12345, damit ich vor der Aktivierung alle Varianten überprüfen kann.“ |
| **Überprüfung von Recommendations** | „Listen Sie alle in diesem Konto konfigurierten Recommendations-Kriterien auf und fassen Sie die verwendeten Algorithmustypen zusammen.“ |
| **Implementierungsprüfung** | „Welche Version von at.js ist konfiguriert und welche Antwort-Token sind derzeit aktiv?“ |
| **Audit ändern** | „Zeigen Sie mir alle Änderungen, die in den letzten 30 Tagen an der Aktivität 98765 vorgenommen wurden, und wer sie vorgenommen hat.“ |

## exemplarische Vorgehensweisen für Anwendungsfälle {#mcp-use-case-walkthroughs}

In den folgenden exemplarischen Vorgehensweisen wird beschrieben, wie Sie allgemeine Aufgaben mithilfe von Eingabeaufforderungen in natürlicher Sprache mit dem [!DNL Adobe Target] MCP-Server durchführen.

<!--
+++Creating an A/B test

**Prompt:**
"Create an A/B test called 'Homepage Hero Image Test' with two experiences: 'Control' showing the current hero and 'Variant' showing a new summer-themed hero image. Target the homepage mbox."

The AI assistant uses the `create_ab_activity` tool to create the activity with the configuration you described. The tool returns the new activity ID and a confirmation of the created experiences.

+++
-->

+++Überprüfen der Aktivitätsleistung

**Aufforderung:**
„Zeigen Sie mir die Leistungsmetriken für meine Aktivität „Checkout-Flussoptimierung“ in den letzten 30 Tagen.“

Der KI-Assistent verwendet `get_ab_performance_report` oder `get_xt_performance_report` (je nach Aktivitätstyp), um Konversionsraten, Besucherzahlen und andere Metriken für das angegebene Zeitfenster abzurufen.

+++

<!--
+++Managing offers

**Prompt:**
"Create an HTML offer called 'Summer Sale Banner' with a promotional banner that says '20% off all summer items'."

The AI assistant uses the `create_target_offer` tool to create the offer with your specified HTML content and returns a confirmation with the new offer ID.

+++

+++Building an audience

**Prompt:**
"Create an audience called 'Mobile Visitors from California' that targets users on mobile devices located in California."

The AI assistant uses the `create_target_audience` tool with the appropriate targeting rules derived from your description.

+++
-->

+++QA-Vorschau-Links erzeugen

**Aufforderung:**
„Generieren Sie Vorschau-URLs für 12345, damit ich jedes Erlebnis testen kann.“

Der KI-Assistent verwendet das `preview_activity`-Tool, um anklickbare URLs zu generieren, die das Audience-Targeting umgehen, sodass Sie jedes Erlebnis direkt in Ihrem Browser anzeigen können.

+++

<!--
+++Creating an Experience Targeting activity

**Prompt:**
"Create an Experience Targeting activity called 'Geo Personalization' that shows different hero banners to visitors from different regions."

The AI assistant uses `create_xt_activity` to build the activity with audience-based experience mapping according to the regions you describe.

+++

+++Scheduling an activity

**Prompt:**
"Update the schedule for activity 12345 to start on May 1st and end on May 31st."

The AI assistant uses the `update_activity_schedule` tool to apply the new start and end dates to the activity.

+++
-->

## Verwandte Ressourcen {#mcp-use-cases-related}

* [Überblick](target-mcp.md)
* [Erste Schritte](target-mcp-get-started.md)
* [MCP Server Tools-Referenz](target-mcp-tools-reference.md)
* [Dokumentation zum Modellkontextprotokoll](https://modelcontextprotocol.io/introduction){target="_blank"}
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
