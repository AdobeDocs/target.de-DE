---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Classifications - Häufig gestellte Fragen zu A4T
feature: null
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 66%

---


# Classifications – Häufig gestellte Fragen zu A4T{#classifications-a-t-faq}

This topic contains answers to questions that are frequently asked about classifications and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, nachdem ich Classifications mithilfe des Classifications Importer heruntergeladen habe? {#section_6045DAC488B248418F430E663C38D001}

Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste unter „TNT“ geführt. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Nachschlagedatei ist besonders für Kunden nützlich, die den Clickstream-Feed von Adobe erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Das Zeichenfolgenformat der TNT-Variable lautet `activityID:experienceID:targettype|event`.

* targetType = 0 (control/random) oder 1 (target) für [!UICONTROL Aktivitäten zur automatischen Zuordnung] und [!UICONTROL automatischen Zielgruppe] .
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.

You can import the classification file on a frequent basis from the UI using a [browser import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) or an [FTP import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.
