---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: Dieses Thema enthält Antworten auf häufig zu Classifications und zur Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Classifications - Häufig gestellte Fragen zu A4T
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 65%

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
