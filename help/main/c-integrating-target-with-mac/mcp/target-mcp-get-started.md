---
solution: Target
product: target
title: Erste Schritte mit dem Adobe Target MCP-Server
description: Erfahren Sie, wie Sie den Adobe Target MCP-Server mit Ihrem KI-Assistenten verbinden, einschließlich Voraussetzungen, Client-Konfiguration und Fehlerbehebung.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Erste Schritte mit dem [!DNL Adobe Target] MCP-Server {#target-mcp-get-started}

>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt.

Diese Seite führt Sie durch alles, was Sie benötigen, um den [!DNL Adobe Target] MCP-Server mit Ihrem KI-Assistenten zu verbinden und Ihre Einrichtung zu überprüfen.

>[!IMPORTANT]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration, und die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen vor der produktiven Verwendung in einer Sandbox-Umgebung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Voraussetzungen {#mcp-prerequisites}

Bevor Sie den [!DNL Adobe Target] MCP-Server an Ihren MCP-Client anschließen, stellen Sie Folgendes sicher:

* Sie besitzen eine aktive [!DNL Adobe Target]-Lizenz (Adobe Experience Cloud-Abonnement) bei einem Adobe Experience Platform-Unternehmen.
* Sie haben eine unterstützte MCP-kompatible Anwendung (derzeit Claude Web, Claude Desktop, Claude Code, Cursor oder ChatGPT).
* Sie haben [!DNL Adobe Target] Berechtigungen in Adobe Admin Console konfiguriert. In Public Beta sind alle 23 verfügbaren Tools schreibgeschützt. **Beobachterrolle** oder höher ist ausreichend, um den MCP-Server zu verwenden.

>[!NOTE]
>
>Schreib-Tools (Erstellen, Aktualisieren, Aktivieren, Deaktivieren) werden nicht über den öffentlichen MCP-Katalog in Public Beta bereitgestellt. Mit den Rollenberechtigungen „Bearbeiter“ und „Genehmiger“ können derzeit keine zusätzlichen Tools entsperrt werden. Der Schreibzugriff wird in einer zukünftigen Version verfügbar sein.

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

1. Überprüfen Sie, ob **Beobachter** oder höher in [!DNL Adobe Target] ist (siehe [Voraussetzungen](#mcp-prerequisites)).
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

## Verwandte Ressourcen {#mcp-get-started-related}

* [Überblick](target-mcp.md)
* [Anwendungsbeispiele und exemplarische Vorgehensweisen](target-mcp-use-cases.md)
* [MCP Server Tools-Referenz](target-mcp-tools-reference.md)
* [Dokumentation zum Modellkontextprotokoll](https://modelcontextprotocol.io/introduction){target="_blank"}
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
