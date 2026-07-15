---
title: Berichterstellung
description: Erfahren Sie, wie Sie Feature Flag-Berichte in Flags mithilfe von Customer Journey Analytics anzeigen.
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# Berichterstellung {#reporting}

Flags ermöglicht Berichte über **Customer Journey Analytics (CJA)**. Es gibt keine In-Console-Ergebnisse oder -Berichte. Stattdessen wird mit einer **Bericht**-Schaltfläche bei jedem Feature Flag oder jeder Feature Group ein CJA-Dashboard für dieses Element geöffnet.

## Voraussetzungen {#prerequisites}

Bevor Sie Berichte anzeigen können, stellen Sie Folgendes sicher:

1. Das Reporting ist für Ihre Anwendung eingerichtet - siehe [Einrichten des Reportings mit Customer Journey Analytics](#setup).
1. Das Feature Flag oder die Feature Group ist aktiv und enthält gesammelte Daten.

## Anzeigen eines Berichts {#view-report}

So öffnen Sie einen Bericht für ein Feature Flag oder eine Feature Group:

1. Navigieren Sie zur Feature Flag oder Feature Group in der Konsole.
1. Wählen Sie **Bericht** aus.

Ein umfassendes Customer Journey Analytics-Dashboard wird geöffnet, das Daten für dieses Flag oder diese Funktionsgruppe anzeigt. Das Dashboard umfasst:

* **Teilnehmer** - Gesamtzahl der Benutzer, die sich für die Funktion qualifiziert haben (Variante + Kontrollgruppe kombiniert)
* **Kontrollgruppe** - Anzahl der der Kontrollgruppe zugewiesenen Benutzer (Benutzer, die das Standarderlebnis erhalten haben)
* **Variantenaufschlüsselung** — Kumulative Anzahl der für jede Variante und die Kontrollgruppe registrierten Benutzer.
* **Tägliche Registrierung** - Diagramme auf Tagesebene, die die Registrierung für jede Variante und die Kontrollgruppe im Zeitverlauf anzeigen

## Einrichten von Berichten mit Customer Journey Analytics {#setup}

Für das Reporting ist ein Customer Journey Analytics-Datensatz erforderlich, der mit Ihrer Flags-Anwendung verbunden ist. Wenden Sie sich an den Flags-Support oder an Ihren Adobe-Support, um das Reporting für Ihre Anwendung zu aktivieren.

>[!NOTE]
>
>Die in der Funktionsanfrage übergebene Identität muss nicht mit einem Profil verknüpft sein. Die Auswertung erfolgt zur Laufzeit und das Ereignis wird an Customer Journey Analytics gesendet.

## Siehe auch {#see-also}

* [Erstellen des ersten Feature Flags](create-your-first-feature-flag.md)
* [A/B-Tests mit Feature Flags](a-b-testing.md)
* [Erstellen einer Funktionsgruppe](create-a-feature-group.md)

<!-- -->
