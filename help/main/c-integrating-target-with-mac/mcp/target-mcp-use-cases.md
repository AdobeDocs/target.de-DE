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
source-git-commit: 216b1103f501a3fcf955523d4bcc8254a8ea418d
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# [!DNL Adobe Target] MCP-Server - Anwendungsfälle und exemplarische Vorgehensweisen {#target-mcp-use-cases}

>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt.

Auf dieser Seite erfahren Sie, was Sie mit dem [!DNL Adobe Target] MCP-Server mithilfe von Eingabeaufforderungen in natürlicher Sprache erreichen können, von der Schnellsuche bis hin zu mehrstufigen Aktivitätsverwaltungsaufgaben.

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

**Aufforderung:**
„Erstellen Sie einen A/B-Test namens „Homepage Hero Image Test“ mit zwei Erlebnissen: „Control“ zeigt den aktuellen Helden und „Variant“ zeigt ein neues Hero-Bild mit Sommerthema. Targeting der Homepage-Mbox.“

Der KI-Assistent verwendet das `create_ab_activity`-Tool, um die Aktivität mit der von Ihnen beschriebenen Konfiguration zu erstellen. Das Tool gibt die neue Aktivitäts-ID und eine Bestätigung der erstellten Erlebnisse zurück.

+++

+++Überprüfen der Aktivitätsleistung

**Aufforderung:**
„Zeigen Sie mir die Leistungsmetriken für meine Aktivität „Checkout-Flussoptimierung“ in den letzten 30 Tagen.“

Der KI-Assistent verwendet `get_ab_performance_report` oder `get_xt_performance_report` (je nach Aktivitätstyp), um Konversionsraten, Besucherzahlen und andere Metriken für das angegebene Zeitfenster abzurufen.

+++

+++Angebote verwalten

**Aufforderung:**
„Erstellen Sie ein HTML-Angebot mit dem Namen „Banner für den Sommerverkauf“ und einem Werbebanner, das „20 % Rabatt auf alle Sommerartikel“ enthält.“

Der KI-Assistent verwendet das `create_target_offer`-Tool, um das Angebot mit dem von Ihnen angegebenen HTML-Inhalt zu erstellen, und gibt eine Bestätigung mit der neuen Angebots-ID zurück.

+++

+++Erstellen einer Zielgruppe

**Aufforderung:**
„Erstellen Sie eine Zielgruppe namens „Mobile Besucher aus Kalifornien“, die Benutzende auf Mobilgeräten mit Standort in Kalifornien anspricht.“

Der KI-Assistent verwendet das `create_target_audience`-Tool mit den entsprechenden Zielgruppenbestimmungsregeln, die aus Ihrer Beschreibung abgeleitet wurden.

+++

+++QA-Vorschau-Links erzeugen

**Aufforderung:**
„Generieren Sie Vorschau-URLs für 12345, damit ich jedes Erlebnis testen kann.“

Der KI-Assistent verwendet das `preview_activity`-Tool, um anklickbare URLs zu generieren, die das Audience-Targeting umgehen, sodass Sie jedes Erlebnis direkt in Ihrem Browser anzeigen können.

+++

+++Experience Targeting-Aktivität erstellen

**Aufforderung:**
„Erstellen Sie eine Experience Targeting-Aktivität namens „Geo Personalization&quot;, die verschiedene Hero-Banner für Besuchende aus verschiedenen Regionen anzeigt.“

Der KI-Assistent verwendet `create_xt_activity`, um die Aktivität mit einer zielgruppenbasierten Erlebniszuordnung entsprechend den von Ihnen beschriebenen Regionen zu erstellen.

+++

+++Planen einer Aktivität

**Aufforderung:**
„Aktualisieren Sie den Zeitplan für die Aktivität 12345, die am 1. Mai beginnen und am 31. Mai enden soll.“

Der KI-Assistent verwendet das `update_activity_schedule`-Tool, um das neue Start- und Enddatum auf die Aktivität anzuwenden.

+++

## Verwandte Ressourcen {#mcp-use-cases-related}

* [Überblick](target-mcp.md)
* [Erste Schritte](target-mcp-get-started.md)
* [MCP Server Tools-Referenz](target-mcp-tools-reference.md)
* [Dokumentation zum Modellkontextprotokoll](https://modelcontextprotocol.io/introduction){target="_blank"}
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
