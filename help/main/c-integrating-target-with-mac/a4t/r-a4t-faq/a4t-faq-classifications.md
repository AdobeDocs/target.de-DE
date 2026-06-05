---
keywords: FAQ;häufig gestellte Fragen;Analytics for Target;a4T;Klassifizierungen;Klassifizierung;Klassifizierungs-Importer;Post-TNT-Aktion;Ereignis-Codes
description: Hier finden Sie Antworten auf Fragen zur Klassifizierung und Verwendung von [!UICONTROL Analytics for Target] (A4T).
title: Wo finde ich Informationen zu Klassifizierungen mit A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
TQID: https://experienceleague.adobe.com/-BIklVbPaO9QGmnjN0eQdbLFXGA7c2sR-3s6OUli8BM
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 25%

---

# Classifications - Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zu Klassifizierungen und zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) gestellt werden.

## Wie kann ich nach der Verwendung [!UICONTROL Classifications Importer] zum Herunterladen von Klassifizierungen den post-tnt-action-Wert mit einem Aktivitätsnamen abgleichen? {#section_6045DAC488B248418F430E663C38D001}

+++Antwort
Die Classifications für die A4T/TNT-Zeichenfolge können mithilfe des [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) der Admin Tools heruntergeladen werden. Die Variable wird in der Exportliste als „TNT“ bezeichnet. In den heruntergeladenen Daten sind die Anzeigenamen der Aktivitäten, Erlebnisse usw. enthalten.

Diese Lookup-Datei ist nützlich für Kunden, die den Clickstream-Daten-Feed von [!DNL Adobe] erhalten. In der Tabelle sind die Anzeigenamen für die Spalten `post_tnt` und `post_tnt_action` angegeben.

Für standardmäßige [!UICONTROL A/B-]- und [!UICONTROL Erlebnis-Targeting]-Aktivitäten (XT) hat die TNT-Zeichenfolge folgendes Format:

```
activityID:experienceID:targettype|event
```

Bei [!UICONTROL automatischen Zuordnungs] und [!UICONTROL automatischen Targeting]-Aktivitäten lautet das Format der TNT-Zeichenfolge:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` und `algorithmId` sind interne Kennungen, die von Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] verwendet werden.
* Erlebnis = 0 steht für den Eintritt in ein Erlebnis.
* Erlebnis = 1 steht für einen Erlebnisbesuch.
* Erlebnis = 2 steht für eine Aktivitätsimpression.
* Ereignis = 3-32766 steht für die Analytics-Erfolgsmetrik-ID.
* Erlebnis = 32767 steht für eine Aktivitätskonversion.
* Ereignis -1 oder 65535 bedeutet, dass der/die Benutzende aus der Aktivität oder dem Erlebnis entfernt wird. Diese Situation tritt häufig auf, wenn der Besucher konvertiert. Der Besucher wird aus dem Erlebnis entlassen und kann sich jetzt für jedes andere Erlebnis qualifizieren.

Sie können die Classification-Datei häufig über die Benutzeroberfläche mit einem [Browser-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) oder einem [FTP-Import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en) importieren. Außerdem können Sie sich an den technischen Support werden, um die Datei als Nachschlagetabelle gemeinsam mit Clickstream-Daten-Feed zu beziehen.

+++
