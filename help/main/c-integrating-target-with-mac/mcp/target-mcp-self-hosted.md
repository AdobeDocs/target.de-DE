---
solution: Target
product: target
title: Self-Host des Adobe Target MCP-Servers
description: Erfahren Sie, wie Sie Ihre eigene Instanz des Adobe Target MCP-Servers mit Python, Docker oder einer lokalen Entwicklungsumgebung ausführen.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer
level: Experienced
source-git-commit: 7b0c8b18abe2db4e07e3ef979d6d194f4c4c81d6
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%

---

# Self-Host des [!DNL Adobe Target] MCP-Servers {#target-mcp-self-hosted}


>[!AVAILABILITY]
>
>Der [!DNL Adobe Target] MCP-Server steht allen Kunden in **Public Beta** zur Verfügung. Es wird derzeit in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** und **ChatGPT** unterstützt.

Auf dieser Seite wird beschrieben, wie Sie Ihre eigene Instanz des [!DNL Adobe Target] MCP-Servers klonen, konfigurieren und ausführen. Das Self-Hosting ist nützlich, wenn Sie eine lokale Entwicklungsumgebung oder eine benutzerdefinierte Netzwerkkonfiguration benötigen oder zur Code-Basis des Servers beitragen möchten.

>[!AVAILABILITY]
>
>Die selbst gehostete Bereitstellung richtet sich an Entwickler und fortgeschrittene Benutzer, die die volle Kontrolle über die [!DNL Adobe Target] MCP-Server-Laufzeit benötigen. Für die meisten Benutzer wird der gehostete Endpunkt (`https://targetmcp.adobe.io/mcp`) empfohlen. Siehe [Arbeiten mit MCP-](target-mcp.md).



## Voraussetzungen {#self-hosted-prereqs}

Bevor Sie beginnen, stellen Sie Folgendes sicher:

* **Python 3.13 oder höher**
* **[uv](https://github.com/astral-sh/uv){target="_blank"}** — schnelles Python-Paket und Projekt-Manager

  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

* Eine aktive [!DNL Adobe Target] mit Zugriff auf Adobe Experience Cloud
* **Artifactory-Anmeldeinformationen** (nur für interne Adobe-Benutzer) - zum Installieren interner Abhängigkeiten erforderlich

## Installation {#self-hosted-install}

**1. Klonen Sie das Repository**

```bash
git clone https://github.com/Adobe-TnT/target-mcp.git
cd target-mcp
```

**2. Erstellen und Aktivieren einer virtuellen Umgebung:**

```bash
uv venv --python 3.13
source .venv/bin/activate
```

**3. Konfigurieren von Umgebungsvariablen:**

```bash
cp env.example .env
```

Öffnen Sie `.env` und ersetzen Sie die Platzhalterwerte durch Ihre Anmeldeinformationen und Unternehmenseinstellungen.

**4. Installieren von Abhängigkeiten:**

```bash
make uv-install
```

**5. Starten Sie den Server:**

Wählen Sie den Modus aus, der Ihrem Anwendungsfall entspricht:

| Modus | Befehl | Verwenden Sie wenn |
|---|---|---|
| Streamable HTTP (API-Server) | `make run-api-server` | Verbinden eines MCP-Clients über HTTP |
| STDIO (lokaler MCP-Client) | `make run-mcp-stdio` | Verwenden der direkten Prozesskommunikation |

## MCP-Client mit einem lokalen Server verbinden {#self-hosted-connect}

### Cursor

Fügen Sie der Cursor-MCP-Konfiguration Folgendes hinzu. Ersetzen Sie die Platzhalterwerte durch Ihr tatsächliches IMS-Token und Ihre Organisations-ID:

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp",
      "headers": {
        "Authorization": "Bearer {IMS_USER_TOKEN}",
        "x-gw-ims-org-id": "{IMS_ORGANIZATION_ID}"
      }
    }
  }
}
```

### Claude Code

Fügen Sie Ihrer Claude Code-MCP-Konfigurationsdatei einen Eintrag hinzu, der auf den lokalen Server verweist:

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp"
    }
  }
}
```

>[!NOTE]
>
>Beim Herstellen einer Verbindung zu einem lokalen Server müssen Authentifizierungs-Header manuell übergeben werden (wie im obigen Cursor-Beispiel gezeigt). Der OAuth-Browser-Fluss ist nur mit dem gehosteten `https://targetmcp.adobe.io/mcp`-Endpunkt verfügbar.

## Docker-Bereitstellung {#self-hosted-docker}

Das Repository enthält eine Docker-Compose-Konfiguration für Container-Bereitstellungen.

**Mit Docker Compose ausführen:**

```bash
make run-dc
```

**Erstellen und Ausführen des Docker-Images direkt:**

```bash
make build
make run-docker
```

## API-Endpunkte {#self-hosted-endpoints}

Der selbst gehostete Server stellt die folgenden HTTP-Endpunkte bereit:

| Endpunkt | Beschreibung |
|---|---|
| `/mcp` | MCP-Protokoll-Endpunkt für KI-Clients |
| `/ping` | Prüfung der Aktualität — gibt `"Pong"` zurück |
| `/health` | Konsistenzprüfung - gibt `{"status": "healthy"}` zurück |
| `/validate` | Eingabevalidierungs-Endpunkt |
| `/authorize` | OAuth-Autorisierungsendpunkt |
| `/token` | OAuth-Token-Endpunkt |

**Beispiel für eine Konsistenzprüfung:**

```bash
curl http://localhost:8080/health
# Response: {"status": "healthy"}
```

## Fehlerbehebung {#self-hosted-troubleshoot}

+++Server kann nicht gestartet werden

1. Überprüfen Sie, ob Python 3.13+ installiert ist: `python --version`
1. Bestätigen Sie, dass die virtuelle Umgebung aktiviert ist: `source .venv/bin/activate`
1. Überprüfen Sie, ob alle Umgebungsvariablen in `.env` korrekt festgelegt sind.
1. Führen Sie `make uv-install` erneut aus, um sicherzustellen, dass alle Abhängigkeiten vorhanden sind.

+++

+++Verbindung vom MCP-Client nicht möglich

1. Vergewissern Sie sich, dass der Server ausgeführt wird und der Port zugänglich ist: `curl http://localhost:8080/ping`
1. Überprüfen Sie, ob die Server-URL in Ihrer MCP-Client-Konfiguration mit der Adresse des laufenden Servers übereinstimmt.
1. Stellen Sie für den Cursor sicher, dass die `Authorization`-Kopfzeile ein gültiges, nicht abgelaufenes IMS-Token enthält.

+++

+++Die Installation der Abhängigkeit schlägt fehl (interne Adobe-Benutzer)

1. Bestätigen Sie, dass Ihre künstlich hergestellten Anmeldeinformationen korrekt konfiguriert sind.
1. Überprüfen Sie Ihre Netzwerkverbindung zur internen Artifactory-Instanz.
1. Wenden Sie sich an den DevOps- oder Plattform-Engineering-Kontakt Ihres Teams, um künstlichen Zugriff zu erhalten.

+++

## Verwandte Ressourcen {#self-hosted-related}

* [Arbeiten mit MCP-Clients](target-mcp.md) - Einrichtung gehosteter Endpunkte und Tool-Referenz
* [Dokumentation zum Modellkontextprotokoll](https://modelcontextprotocol.io/introduction){target="_blank"}
* [API-Referenz für [!DNL Adobe Target] Admin](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
