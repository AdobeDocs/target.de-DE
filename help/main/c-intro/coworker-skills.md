---
keywords: Adobe Target;Mitarbeiter;KI;Fähigkeiten;Experimentieren;Recommendations
title: Mitarbeiterqualifikationen für Adobe Target
description: Erfahren Sie mehr über die für Adobe Target verfügbaren Coworker-Fähigkeiten, einschließlich Aktivitätserkennung, Testerstellung, Analyse, Audience-Komposition und Empfehlungen zur Fehlerbehebung.
feature: Overview
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: cc4c6b77fa6c600723813b939ba1e5323836ebcc
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 2%
---

# Mitarbeiterqualifikationen für Adobe Target {#coworker-skills}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Entdecken Sie die für Adobe Target verfügbaren Kolleg-Kenntnisse, einschließlich der Kenntnisse zum Untersuchen von Aktivitäten und Zielgruppen, Erstellen und Konfigurieren von Tests, Analysieren der Leistung, Erstellen von Zielgruppen und Verwalten von Recommendations.

>[!ENDSHADEBOX]

Mitarbeiter können mit ihren Fähigkeiten Adobe Target-Experten natürliche Sprache verwenden, um ihre Test- und Personalisierungsprogramme zu erkunden, Aktivitäten zu erstellen und zu konfigurieren, Ergebnisse zu analysieren und Bereitstellungsprobleme zu lösen. Beschreiben Sie, was Sie im Coworker Chat tun möchten, und überprüfen Sie dann die zurückgegebenen Empfehlungen, Konfigurationen oder Analysen, bevor Sie Maßnahmen ergreifen.

[!DNL Adobe Target] MCP-Tools und Coworker werden separat dokumentiert und bieten verschiedene Funktionen:

* [Target MCP](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md) dokumentiert die einzelnen Tools, die vom direkten MCP-Server bereitgestellt werden, einschließlich unterstützter Aktivitätstypen, Parameter, Berechtigungen und Lese- oder Schreibbereich.
* [Coworker](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/overview#target-activities-and-audiences) bietet eine separate Orchestrierungsschicht für natürliche Sprachen, die Funktionen kombinieren und zusätzliche Workflows anwenden kann.

In der folgenden Tabelle finden Sie einen allgemeinen Vergleich der zugehörigen Funktionen.

| Funktion | Ziel-MCP | Coworker |
| --- | --- | --- |
| Auflisten von laufenden Experimenten, Zielgruppen, Angeboten oder kürzlich geänderten Elementen | Ja | Ja |
| Erstellen einer Automated Personalization-Aktivität | Nein | Nein |
| Erstellen einer Target-Zielgruppe | Ja | Ja |
| Erstellen einer VEC-Zielaktivität, einer Erlebnis-Targeting-Aktivität oder eines A/B-Tests | Ja | Ja |
| Erstellen einer Target Recommendations-Aktivität | Ja | Ja |
| Erstellen eines HTML- oder JSON-Angebots in Target | Ja | Ja |
| Verwenden eines AEM-Inhaltsfragments in einer Target-Aktivität | Nein | Ja |
| Empfehlung dessen, was funktioniert und was als Nächstes getestet werden soll | Keine oder allgemeine Ratschläge | Ja |


## Target-Modul

Die folgenden Fähigkeiten sind unter dem Plug-in **Target** verfügbar:

* **Target durchsuchen**

  Ermöglicht die schreibgeschützte Erkennung, Überprüfung und Zählung von Target-Entitäten, einschließlich Aktivitäten, Zielgruppen, Angeboten und zugehöriger Konfigurationen.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Meine aktiven Aktivitäten auflisten.“
  * „Wie viele Aktivitäten werden derzeit ausgeführt?“
  * „Zeigen Sie mir die von dieser Aktivität verwendeten Audiences und Angebote.“

  >[!ENDSHADEBOX]

* **Target-Aktivitäts-Urteil**

  Bestimmt mithilfe von Signifikanzberechnungen und Konfigurationsprüfungen, ob eine Aktivität versandbereit ist, auf weitere Daten warten soll, beendet werden soll oder eine Fehlerbehebung erfordert.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Soll ich diesen Test senden?“
  * „Ist diese Aktivität bereit zum Stoppen?“
  * „Gibt es Probleme mit der aktuellen Aktivitätskonfiguration?“

  >[!ENDSHADEBOX]

* **Target-Design**

  Erstellt und konfiguriert Aktivitäten und Angebote, generiert QA-URLs und verfasst oder optimiert Angebotsinhalte.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Erstellen Sie einen A/B-Test für die Homepage.“
  * „Erstellen Sie ein Angebot für das wiederkehrende Besuchererlebnis.“
  * „Generieren Sie eine QA-URL für diese Aktivität.“

  >[!ENDSHADEBOX]

* **Target VEC**

  Erstellt und bearbeitet Visual Experience Composer-Aktivitäten und deren Seitenbereitstellungs-Zielgruppen.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Erstellen Sie einen VEC A/B-Test für die Homepage.“
  * „Bearbeiten Sie die Hero-Überschrift in meiner VEC-Aktivität.“
  * „Erstellen Sie eine Zielgruppe für den Seitenversand für diese VEC-Aktivität.“

  >[!ENDSHADEBOX]

* **Target-Einrichtung**

  Handbücher zur vollständigen Erstellung von A/B-, Erlebnis-Targeting- oder Visual Experience Composer-Aktivitäten, einschließlich Voraussetzungen, Zeitplan, Qualitätssicherung und Aktivierung.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Helfen Sie mir, meinen ersten Test zu erstellen.“
  * „Was benötige ich, bevor ich eine Experience Targeting-Aktivität erstelle?“
  * „Einführung in Planung, QS und Aktivierung dieser Aktivität.“

  >[!ENDSHADEBOX]

* **Target Intelligence**

  Audits zielen auf Programme auf Risiken, Kollisionen, Fehlkonfigurationen, Hygieneprobleme und schnelle Erfolge ab.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Meine Target-Aktivitäten prüfen.“
  * „Kollisionen oder Konfigurationsrisiken in meinen Aktivitäten finden.“
  * „Welche schnellen Erfolge können die Hygiene meines Target-Programms verbessern?“

  >[!ENDSHADEBOX]

* **Target-Stratege**

  Analysiert historische Zielgruppendaten für erfolgreichste Muster und empfiehlt zukünftige Tests.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Was sollte ich als Nächstes auf der Grundlage früherer Ergebnisse testen?“
  * „Welche Muster erscheinen in meinen leistungsstärksten Tests?“
  * „Auf der Grundlage der Ergebnisse dieser Aktivität empfiehlt sich ein Folgetest.“

  >[!ENDSHADEBOX]

* **Target-Testrechner**

  Plant A/B/N-Stichprobengröße, -dauer und erkennbare Steigerung für Konversions- und Umsatzmetriken mit Bonferroni-Korrektur für mehrere Vergleiche.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Welche Stichprobengröße benötige ich?“
  * „Wie lange sollte ich diesen A/B-Test durchführen, um eine Steigerung von 5 % zu erkennen?“
  * „Welche nachweisbare Steigerung kann ich mit diesem Traffic messen?“

  >[!ENDSHADEBOX]

* **Target Portfolio-Bericht**

  Bietet schreibgeschützte, programmweite Performance-Rollups und Aktivitätstrend- und Momentum-Analysen.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Welches sind meine Top- und Worst-Tests?“
  * „Zeigen Sie mir Performance-Trends in meinen Aktivitäten.“
  * „Welche Aktivitäten haben in letzter Zeit an Dynamik gewonnen oder verloren?“

  >[!ENDSHADEBOX]

* **Target Audience Composer**

  Erstellt oder bearbeitet Target-native Zielgruppen aus Beschreibungen oder expliziten Regeln in natürlicher Sprache.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Erstellen Sie eine Zielgruppe für wiederkehrende mobile Besucher.“
  * „Bearbeiten Sie diese Zielgruppe, um Besucher aus der organischen Suche einzuschließen.“
  * „Erstellen Sie eine Target-Zielgruppe für Besucher, die die Preisseite aufgerufen haben.“

  >[!ENDSHADEBOX]

* **Target Recommendations**

  Verwaltet und verwendet Target Recommendations-Aktivitäten und -Konfigurationen.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Erstellen Sie eine Recommendations-Aktivität.“
  * „Meine Recommendations-Aktivitäten und -Konfigurationen anzeigen.“
  * „Aktualisieren Sie die Einstellungen für diese Recommendations-Aktivität.“

  >[!ENDSHADEBOX]

* **Target Recommendations-Diagnose**

  Diagnostiziert Bereitstellungs-, Konfigurations-, Katalog- und Feed-Probleme für Recommendations.

  >[!BEGINSHADEBOX]

  *Beispielaufforderungen:*

  * „Warum werden meine Empfehlungen nicht angezeigt?“
  * „Diagnose der Feed- und Katalogkonfiguration für diese Recommendations-Aktivität.“
  * „Wirken sich Versand- oder Konfigurationsprobleme auf meine Empfehlungen aus?“

  >[!ENDSHADEBOX]
