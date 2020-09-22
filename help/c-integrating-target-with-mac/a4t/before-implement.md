---
keywords: Recommendations
description: Bei Ihrem Datenerfassungsprozess treten verschiedene Änderungen auf, wenn Sie Analytics als Berichtsquelle für Target (A4T) verwenden.
title: Vor der Implementierung von Adobe Analytics als Berichte-Quelle für Adobe Target (A4T)
feature: a4t implementation
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: 75fa021c00940c87cf4b2bfa0e2875bb396079a1
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 52%

---


# Vor der Implementierung{#before-you-implement}

Several changes occur in your data collection process when enabling [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

Bevor Sie sich für die Verwendung dieser Integration entscheiden, überprüfen Sie folgende Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Berichtsprozesse:

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie A4T verwenden können, müssen Sie eine Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie das [Marketing Cloud Integrations Provisioning-Formular](https://www.adobe.com/go/audiences) , um die Bereitstellung anzufordern.

Für diese A4T-Integration müssen Sie in Abhängigkeit davon, ob Sie Weiterleitungsangebote in A4T verwenden möchten oder nicht, die folgenden Bibliotheksversionen (oder neuere) implementieren:

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 1.8.0
* [!DNL Adobe Target] (je nach Implementierung): at.js, Version 0.9.1 oder mbox.js, Version 61
* Adobe Analytics: appMeasurement.js, Version 1.7.0

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 2.3.0
* [!DNL Adobe Target]: at.js, Version 1.6.2

   **Hinweis:** Die mbox.js-Bibliothek unterstützt keine Weiterleitungsangebote mit A4T. Ihre Implementierung muss at.js verwenden.

* Adobe Analytics: appMeasurement.js, Version 2.1

Download and deployment instructions are listed in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* This integration is enabled on new activities when you select to use [!DNL Analytics] as the reporting source. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* The process of setting up [!DNL Analytics] as the reporting source for [!DNL Target] includes several implementation steps, followed by a provisioning step. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. After you complete these steps, you will be ready to use [!DNL Analytics] as your reporting source as soon as it is enabled for you. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Das [!DNL Visitor ID service] erstellt eine freigegebene Datei [!DNL Visitor ID] über das [!DNL Adobe Experience Cloud]. Although it does not replace the [!DNL Target] mboxPC id or [!DNL Audience Manager] UUID, it does replace the way [!DNL Analytics] identifies new visitors. If set up properly, returning [!DNL Analytics] visitors should also be identified via their old [!DNL Analytics] ID to prevent visitor cliffing. Similarly, because the [!DNL Target] mboxPCid remains intact, no [!DNL Target] visitor profile data is lost when you upgrade to the [!DNL Visitor ID service].
* Die [!DNL Visitor ID service] Ausführung muss vor Ihrem [!DNL Analytics] und [!DNL Target] Seitencode erfolgen. Make sure that `VisitorAPI.js` appears above the tags for all other [!DNL Experience Cloud] solutions.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

After this integration is enabled, you will experience an additional 5-10 minutes of latency in [!DNL Analytics]. This latency increase allows data from [!DNL Analytics] and [!DNL Target] to be stored on the same hit, allowing you to break down activities by page and site section.

This increase is reflected in all [!DNL Analytics] services and tools, including the live-stream and real-time reporting, and applies in the following scenarios:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, endgültige Daten und Datenfeeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Be aware that the latency increase starts after you implement the [!DNL Experience Cloud] visitor ID service, even if you have not fully implemented this integration.

## Zusätzliche ID  {#section_2C1F745A2B7D41FE9E30915539226E3A}

All [!DNL Target] calls used by an A4T activity to deliver content or record the goal metric must have a corresponding [!DNL Analytics] hit that shares the same supplemental ID for A4T to work properly.

Hits that contain data from [!DNL Analytics] and [!DNL Target] contain a supplemental data ID. You can see this ID in the [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) as the `sdid` parameter. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.
* Eine Version von [!DNL mbox.js], die diese Integration unterstützt, wurde implementiert.

When troubleshooting, be sure to confirm that the supplemental ID is present on [!DNL Analytics] hits.

## Clientseitige Analytics-Protokollierung {#client-side}

Wenn sich at.js, die [!DNL Experience Cloud Visitor ID Service] und appMeasurement.js auf der Seite befinden, verknüpfen [!DNL Analytics]und [!DNL Target] standardmäßig Ereignisse für Reporting- und Analysezwecke im Backend, sofern die korrekte zusätzliche ID von der Seite wie oben erläutert einbezogen wird. Sie müssen keine weiteren Vorgänge für A4T verwalten und durchführen, damit sie ordnungsgemäß funktionieren.

In manchen Fällen könnten Sie aber mehr Kontrolle darüber haben wollen, wann und wie Analysedaten in Verbindung mit [!DNL Target] zu Berichtszwecken an [!DNL Analytics] gesendet werden sollen. Möglicherweise verfügen Sie über ein unternehmensinternes Analysetool, das Sie für interne Zwecke nutzen, und möchten auch die Analysedaten an [!DNL Analytics] über Ihr internes Analyseprodukt senden, damit andere Mitarbeiter weiterhin [!DNL Analytics] als visuelle Berichtsquelle nutzen können. Weitere Informationen finden Sie unter [Schritt 7: Verweisen auf at.js oder mbox.js auf allen Seiten der Website](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementieren von Analytics for Target*.

## Freigegebene Zielgruppen

Beachten Sie beim Ausfüllen des [Marketing Cloud Integrations-Bereitstellungsformulars](https://www.adobe.com/go/audiences)die folgenden wichtigen Informationen zur Option [!UICONTROL Freigegebene Audiencen] , die unter &quot;[!UICONTROL Für welche Funktionen wünschen Sie Bereitstellung]?&quot;aufgeführt ist.

![Anforderungsformular](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wenn Sie [!UICONTROL freigegebene Audiencen]anfordern, aktivieren Sie [!UICONTROL Zielgruppe] und [!UICONTROL Adobe Audience Manager] (AAM), um Informationen freizugeben, in diesem Fall Audiencen.

>[!IMPORTANT]
>
>Diese Integration von [!UICONTROL Zielgruppe] und AAM bringt zusätzliche Kosten mit sich. Sie werden für jede [!UICONTROL Zielgruppe] in AAM in Rechnung gestellt.
