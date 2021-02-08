---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Classifications; Classification; Classifications Importer; Post-TNT-Aktion
description: Hier finden Sie Antworten auf Fragen zu Klassifizierungen und zur Verwendung von Analytics für die Zielgruppe (A4T). Mit A4T können Sie Analytics-Berichte für Aktivitäten der Zielgruppe verwenden.
title: Wo finde ich Informationen zu Klassifizierungen mit A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 55%

---


# Classifications – Häufig gestellte Fragen zu A4T{#classifications-a-t-faq}

Dieses Thema enthält Antworten auf häufig gestellte Fragen zu Klassifizierungen und die Verwendung von [!DNL Analytics] als Berichte für [!DNL Target] (A4T).

## Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, nachdem ich Classifications mithilfe des Classifications Importer heruntergeladen habe? {#section_6045DAC488B248418F430E663C38D001}

Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste unter „TNT“ geführt. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Nachschlagedatei ist besonders für Kunden nützlich, die den Clickstream-Feed von Adobe erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Das Zeichenfolgenformat der TNT-Variable lautet `activityID:experienceID:targettype|event`.

* targetType = 0 (control/random) oder 1 (target) für [!UICONTROL Auto-Allokation] und [!UICONTROL Auto-Zielgruppe]-Aktivitäten.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Ereignis = 3-32766 stellt die Analytics-Erfolgsmetrik-ID dar.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.

Sie können die Classification-Datei häufig über die Benutzeroberfläche importieren, indem Sie einen [Browser-Import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) oder einen [FTP-Import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html) verwenden. Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.
