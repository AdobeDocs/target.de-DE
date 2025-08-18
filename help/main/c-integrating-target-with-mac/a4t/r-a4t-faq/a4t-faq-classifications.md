---
keywords: FAQ;häufig gestellte Fragen;Analytics for Target;a4T;Klassifizierungen;Klassifizierung;Klassifizierungs-Importer;Post-TNT-Aktion;Ereignis-Codes
description: Hier finden Sie Antworten auf Fragen zur Klassifizierung und Verwendung von [!UICONTROL Analytics for Target] (A4T).
title: Wo finde ich Informationen zu Klassifizierungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 30%

---

# Classifications - Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zu Klassifizierungen und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) gestellt werden.

## Wie kann ich, nachdem ich die [!UICONTROL Classifications Importer] zum Herunterladen von Klassifizierungen verwendet habe, den post-tnt-action-Wert mit einem Aktivitätsnamen abgleichen? {#section_6045DAC488B248418F430E663C38D001}

+++Antwort
Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html?lang=de) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste als „TNT“ bezeichnet. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Lookup-Datei ist nützlich für Kunden, die den Clickstream-Daten-Feed von [!DNL Adobe] erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Für Aktivitäten des Typs [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting] (XT) hat die TNT-Zeichenfolge folgendes Format:

```
activityID:experienceID:targettype|event
```

Für [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten lautet das Format der TNT-Zeichenfolge:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` und `algorithmId` sind interne Kennungen, die von [!UICONTROL Auto-Allocate]- und [!UICONTROL Auto-Target]-Aktivitäten verwendet werden.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Ereignis = 3-32766 steht für die Analytics-Erfolgsmetrik-ID.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.
* Ereignis -1 oder 65535 bedeutet, dass der/die Benutzende aus der Aktivität oder dem Erlebnis entfernt wird. Diese Situation tritt häufig auf, wenn der Besucher konvertiert. Der Besucher wird aus dem Erlebnis entlassen und kann sich jetzt für jedes andere Erlebnis qualifizieren.

Sie können die Classification-Datei häufig über die Benutzeroberfläche mit einem [Browser-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=de) oder einem [FTP-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=de) importieren. Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.

+++
