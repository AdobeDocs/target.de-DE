---
description: Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Classifications; Classification; Classifications Importer; Post-TNT-Aktion
seo-description: Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
seo-title: Classifications - Häufig gestellte Fragen zu A4T
solution: Target
title: Classifications - Häufig gestellte Fragen zu A4T
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Classifications – Häufig gestellte Fragen zu A4T{#classifications-a-t-faq}

Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, nachdem ich Classifications mithilfe des Classifications Importer heruntergeladen habe? {#section_6045DAC488B248418F430E663C38D001}

Sie können die Classifications für die A4T-/TNT-Zeichenfolge aus dem Admin Tools [Classification Importer](https://marketing.adobe.com/resources/help/de_DE/reference/c_working_with_saint.html) herunterladen. Die Variable wird in der Exportliste unter „TNT“ geführt. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Nachschlagedatei ist besonders für Kunden nützlich, die den Clickstream-Feed von Adobe erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Das Zeichenfolgenformat der TNT-Variable lautet `activityID:experienceID:targettype|event`.

* Der „targettype“ ist in A4T stets 0.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.

Sie können die Classification-Datei regelmäßig mit dem [Browser Export](https://marketing.adobe.com/resources/help/de_DE/reference/browser_export.html) oder [FTP Export](https://marketing.adobe.com/resources/help/de_DE/reference/ftp_export.html) von der Benutzeroberfläche herunterladen. Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.
