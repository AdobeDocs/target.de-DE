---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Classifications; Classification; Classifications Importer; Post-TNT-Aktion; Ereigniscodes
description: Hier finden Sie Antworten auf Fragen zu Classifications und zur Verwendung von [!UICONTROL Analytics for Target] (A4T).
title: Wo finde ich Informationen über Classifications mit A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 24%

---

# Classifications - Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zu Klassifizierungen und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) gestellte Fragen.

## Wie passe ich den Wert post-tnt-action an einen Aktivitätsnamen an, nachdem ich die [!UICONTROL Classifications Importer] zum Herunterladen von Classifications verwendet habe? {#section_6045DAC488B248418F430E663C38D001}

+++Antwort
Sie können die Klassifizierungen für die A4T-/TNT-Zeichenfolge aus dem Admin Tools [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) herunterladen. Die Variable wird in der Exportliste als &quot;TNT&quot;bezeichnet. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Lookup-Datei ist nützlich für Kunden, die den Clickstream-Datenfeed von [!DNL Adobe] empfangen. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Bei standardmäßigen [!UICONTROL A/B Test] - und [!UICONTROL Experience Targeting] -Aktivitäten (XT) ist das Format der TNT-Zeichenfolge:

```
activityID:experienceID:targettype|event
```

Bei den Aktivitäten [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] ist das Format der TNT-Zeichenfolge:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` und `algorithmId` sind interne Bezeichner, die von den Aktivitäten [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target] verwendet werden.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Ereignis = 3-32766 steht für die Analytics-Erfolgsmetrik-ID.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.
* Ereignis -1 oder 65535 bedeutet, dass der Benutzer aus der Aktivität oder dem Erlebnis entfernt wird. Diese Situation tritt oft auf, wenn der Besucher konvertiert. Der Besucher wird aus dem Erlebnis freigelassen und kann sich jetzt für jedes andere Erlebnis qualifizieren.

Sie können die Classification-Datei häufig über einen [Browser-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) oder einen [FTP-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en) aus der Benutzeroberfläche importieren. Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.

+++
