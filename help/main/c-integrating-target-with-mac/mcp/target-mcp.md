---
solution: Target
product: target
title: Adobe Target MCP-Server - Übersicht
description: Erfahren Sie, was der Adobe Target MCP-Server ist, welche wichtigen Funktionen er bietet und wie er eine Verbindung zu Ihrem KI-Assistenten herstellt.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# [!DNL Adobe Target] MCP-Server {#target-mcp}

Mit der [!DNL Adobe Target] MCP-Integration können Sie A/B-Tests, Personalisierungsaktivitäten und Recommendations-Kriterien direkt von Ihrem KI-Assistenten aus überprüfen und analysieren. Verwandeln Sie die Experimentier- und Personalisierungsdaten von [!DNL Target] in Nur-Sprache-Workflows. Überprüfen Sie Ihr Experimentierportfolio, überprüfen Sie Leistungsberichte und erkunden Sie Zielgruppen und Angebote, ohne in der Benutzeroberfläche zu navigieren oder API-Aufrufe zu schreiben.

>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt. In zukünftigen Versionen wird Unterstützung für weitere MCP-kompatible Anwendungen hinzugefügt.


## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing- und Optimierungsteams verlassen sich zunehmend auf Chat-basierte Anwendungen und Entwickler-Tools - wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio - um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

[!DNL Adobe Target] bietet jetzt einen MCP-Server, der Experimentier-, Personalisierungs- und Recommendations-Vorgänge direkt in jeder MCP-kompatiblen Anwendung aufzeigt. [!DNL Adobe Target] fungiert als Entscheidungs- und Ausführungsebene, während der KI-Assistent Argumentation und Erläuterung verarbeitet. So erhalten Teams schneller Zugriff auf Optimierungseinblicke, ohne durch mehrere Produktbildschirme zu navigieren oder Abfragen für die [!DNL Adobe Target] REST-API zu schreiben.


>[!IMPORTANT]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration, und die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen vor der produktiven Verwendung in einer Sandbox-Umgebung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Wichtigste Funktionen {#mcp-capabilities}

Der [!DNL Adobe Target] MCP-Server bietet Lesezugriff auf Aktivitäten, Zielgruppen, Angebote, Empfehlungen und die Implementierungskonfiguration. Mit der Integration können Sie:

* **Experimente überprüfen und überprüfen** - Sie erhalten Links zu Status, Leistung, Änderungsverlauf und QA-Vorschau für jede Aktivität, ohne in der Benutzeroberfläche zu navigieren.
* **Ergebnisse analysieren** - Abrufen von Performance-, Umsatz- und A4T-Berichten für A/B-, XT-, AP- und Auto-Target-Aktivitäten.
* **Aktivitäten erkunden** - Auflisten, Überprüfen und Analysieren von A/B- und XT-Aktivitäten.
* **Erkunden von Zielgruppen und Angeboten** - Auflisten und Überprüfen von Zielgruppen, HTML-Angeboten und JSON-Angeboten.
* **Explore Recommendations-**: Auflisten und Überprüfen von Kriterien und Warenkorb-basierten Algorithmen.
* **Audit-Implementierung** - Überprüfen Sie at.js-Einstellungen, Antwort-Token und den Revisionsverlauf pro Entität.

>[!NOTE]
>
>Schreib-Tools (Erstellen, Aktualisieren, Aktivieren, Deaktivieren) werden nicht über den öffentlichen MCP-Katalog in **Public Beta&quot;**. Alle derzeit verfügbaren Tools sind schreibgeschützt. Der Schreibzugriff wird in einer zukünftigen Version verfügbar sein.

Der [!DNL Adobe Target] MCP-Server stellt 23 schreibgeschützte Tools in 10 Kategorien zur Verfügung - von der Aktivitätsprüfung und Berichterstellung bis zur Untersuchung von Zielgruppen und QS-Vorschauen. Die vollständige Parameterreferenz finden Sie unter [MCP Server Tools-Referenz](target-mcp-tools-reference.md).

Informationen zu den Funktionen des [!DNL Adobe Target] MCP-Servers, einschließlich schrittweiser Anleitungen zu Eingabeaufforderungen, finden Sie unter [Anwendungsfälle und Anleitungen](target-mcp-use-cases.md).

Informationen zum Verbinden des [!DNL Adobe Target] MCP-Servers mit Ihrem KI-Assistenten - einschließlich Voraussetzungen, Client-spezifischer Konfiguration und Fehlerbehebung - finden Sie unter [Erste Schritte](target-mcp-get-started.md).

## Häufig gestellte Fragen {#mcp-faq}

+++Welche MCP-Clients werden unterstützt?

Der [!DNL Adobe Target] MCP-Server ist derzeit verfügbar für **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT**. Die Unterstützung für weitere MCP-kompatible Anwendungen kann in zukünftigen Versionen hinzugefügt werden.
+++

+++Auf welche [!DNL Adobe Target] Objekte kann ich über MCP zugreifen?

Sie können auf Aktivitäten (A/B, XT, AP), Zielgruppen, Angebote, Eigenschaften, Mboxes, Recommendations-Kriterien, Antwort-Token, at.js-Konfiguration, A4T-Berichte und den Überarbeitungsverlauf der Entität zugreifen. Alle 23 derzeit verfügbaren Tools sind schreibgeschützt.
+++

+++Kann der MCP-Server Aktivitäten erstellen oder ändern?

Nicht in der öffentlichen Beta. Der öffentliche MCP-Katalog stellt derzeit 23 schreibgeschützte Tools bereit. Schreibvorgänge (Erstellen, Aktualisieren, Aktivieren, Deaktivieren) sind noch nicht über den öffentlichen MCP-Server verfügbar. Der Schreibzugriff wird in einer zukünftigen Version verfügbar sein.
+++

+++Benötige ich Entwicklerzugriff, um den MCP-Server zu verwenden?

Nein. Der MCP-Server ist sowohl für Marketing- als auch für technische Personas konzipiert. Marketing-Experten können damit interagieren, indem sie natürliche Spracheingaben in jedem unterstützten MCP-Client verwenden, während Entwickler sie in Tools wie Claude Code oder Cursor verwenden können.
+++

+++Werden meine [!DNL Adobe Target] an den MCP-Client-Anbieter gesendet?

Wenn Sie eine Eingabeaufforderung senden, kann der MCP-Client relevanten Kontext (einschließlich [!DNL Adobe Target] vom MCP-Server zurückgegebenen Daten) zur Verarbeitung an sein Modell senden. Überprüfen Sie die Datenschutz- und Datenverarbeitungsrichtlinien Ihres MCP-Client-Anbieters, bevor Sie eine Verbindung zu Produktionsdaten herstellen. Die Datenverarbeitung in Adobe unterliegt den [Datenschutzrichtlinien von Adobe &#x200B;](https://www.adobe.com/privacy.html) den [Datenschutzbestimmungen](https://www.adobe.com/go/dpt-ww).
+++

+++Können Schreibvorgänge zu unbeabsichtigten Änderungen an Live-Aktivitäten führen?

Schreib-Tools sind nicht über den öffentlichen MCP-Katalog in Public Beta verfügbar. Alle 23 derzeit verfügbaren Tools sind schreibgeschützt. Wenn Schreib-Tools in einer zukünftigen Version eingeführt werden, enthalten sie Sicherheitsanmerkungen und Bestätigungs-Gates, sodass keine zustandsändernde Aktion ohne explizite Benutzerbestätigung ausgeführt wird.
+++

+++Welche Berechtigungen benötige ich in [!DNL Adobe Target]?

**Beobachterrolle** oder höher gewährt Zugriff auf alle 23 schreibgeschützten Tools, die in Public Beta verfügbar sind. Schreibwerkzeuge werden noch nicht über den öffentlichen MCP-Katalog verfügbar gemacht, sodass die Berechtigungen für Editor und Genehmiger derzeit keine zusätzlichen MCP-Werkzeuge freischalten. Wenden Sie sich an Ihren [!DNL Adobe Target], wenn Sie sich bezüglich Ihrer aktuellen Zugriffsebene nicht sicher sind.
+++

+++Kann ich den MCP-Server für mehrere Target-Organisationen oder -Eigenschaften verwenden?

Der MCP-Server führt Vorgänge für die Organisation durch, die mit Ihren authentifizierten Adobe IMS-Anmeldeinformationen verknüpft ist. Wenn Sie innerhalb dieser Organisation Zugriff auf mehrere Eigenschaften haben, können Sie mit dem `list_target_properties`-Tool eine Abfrage nach Eigenschaften durchführen und nachfolgende Anfragen entsprechend filtern.
+++

## Verwandte Ressourcen {#mcp-related}

* [Erste Schritte](target-mcp-get-started.md)
* [Anwendungsbeispiele und exemplarische Vorgehensweisen](target-mcp-use-cases.md)
* [MCP Server Tools-Referenz](target-mcp-tools-reference.md)
* [Dokumentation zum Modellkontextprotokoll](https://modelcontextprotocol.io/introduction){target="_blank"}
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [Cursor-Dokumentation](https://docs.cursor.com/){target="_blank"}
