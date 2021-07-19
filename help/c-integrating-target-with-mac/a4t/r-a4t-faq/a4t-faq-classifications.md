---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Classifications; Classification; Classifications Importer; Post-TNT-Aktion
description: Hier finden Sie Antworten auf Fragen zu Classifications und zur Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten.
title: Wo finde ich Informationen über Classifications mit A4T?
feature: 'Analytics for Target (A4T) '
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: cdb79c82fe1e7158a2f2014df661bd6fa852df92
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 51%

---

# Classifications - Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu Klassifizierungen und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) gestellte Fragen.

## Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, nachdem ich Classifications mithilfe des Classifications Importer heruntergeladen habe? {#section_6045DAC488B248418F430E663C38D001}

Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste unter „TNT“ geführt. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Nachschlagedatei ist besonders für Kunden nützlich, die den Clickstream-Feed von Adobe erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Das Zeichenfolgenformat der TNT-Variable lautet `activityID:experienceID:targettype|event`.

* targettype = 0 (Kontrolle/zufällig) oder 1 (Targeting) für [!UICONTROL Automatisierte Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Ereignis = 3-32766 steht für die Analytics-Erfolgsmetrik-ID.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.
* Ereignis -1 oder 65535 bedeutet, dass der Benutzer aus der Aktivität oder dem Erlebnis entfernt wird. Diese Situation tritt oft auf, wenn der Besucher konvertiert. Der Besucher wird aus dem Erlebnis freigelassen und kann sich jetzt für jedes andere Erlebnis qualifizieren.

Sie können die Classification-Datei häufig über die Benutzeroberfläche mit einem [Browser-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) oder [FTP-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en) importieren. Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.
