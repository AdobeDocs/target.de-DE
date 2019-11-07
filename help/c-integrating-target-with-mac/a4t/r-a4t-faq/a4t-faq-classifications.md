---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Classifications; Classification; Classifications Importer; Post-TNT-Aktion
description: Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Classifications - Häufig gestellte Fragen zu A4T
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Classifications – Häufig gestellte Fragen zu A4T{#classifications-a-t-faq}

Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, nachdem ich Classifications mithilfe des Classifications Importer heruntergeladen habe? {#section_6045DAC488B248418F430E663C38D001}

Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste unter „TNT“ geführt. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Nachschlagedatei ist besonders für Kunden nützlich, die den Clickstream-Feed von Adobe erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Das Zeichenfolgenformat der TNT-Variable lautet `activityID:experienceID:targettype|event`.

* Der „targettype“ ist in A4T stets 0.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.

You can import the classification file on a frequent basis from the UI using a [browser import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) or an [FTP import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.
