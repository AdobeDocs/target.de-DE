---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Classifications; Classification; Classifications Importer; Post-TNT-Aktion; Ereigniscodes
description: Antworten auf Fragen zu Classifications und zur Verwendung von [!UICONTROL Analytics for Target] (A4T).
title: Wo finde ich Informationen über Classifications mit A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 29%

---

# Classifications - Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu Klassifizierungen und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T).

## Nach Verwendung der [!UICONTROL Classifications Importer] Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, um Klassifizierungen herunterzuladen? {#section_6045DAC488B248418F430E663C38D001}

Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste unter „TNT“ geführt. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Lookup-Datei ist für Kunden nützlich, die [!DNL Adobe]Clickstream-Daten-Feed. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Für Standard [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) -Aktivitäten, lautet das Format der TNT-Zeichenfolge:

```
activityID:experienceID:targettype|event
```

Für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] -Aktivitäten verwenden, lautet das Format der TNT-Zeichenfolge:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` und `algorithmId` sind interne Kennungen, die von [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] Aktivitäten.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Ereignis = 3-32766 steht für die Analytics-Erfolgsmetrik-ID.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.
* Ereignis -1 oder 65535 bedeutet, dass der Benutzer aus der Aktivität oder dem Erlebnis entfernt wird. Diese Situation tritt oft auf, wenn der Besucher konvertiert. Der Besucher wird aus dem Erlebnis freigelassen und kann sich jetzt für jedes andere Erlebnis qualifizieren.

Sie können die Classification-Datei häufig über die Benutzeroberfläche importieren, indem Sie eine [Browser-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) oder [FTP-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en). Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.
