---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;reporting source
description: Sollten Sie eine ältere Version von „at.js“ oder „mbox.js“ verwenden, müssen Sie einen Trackingserver für Aktivitäten angeben, bei denen Analytics for Target (A4T) zum Einsatz kommt.
title: Verwenden eines Analytics-Trackingservers
feature: null
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 39%

---


# Verwenden eines Analytics-Trackingservers{#use-an-analytics-tracking-server}

If you are using an older version of at.js or mbox.js, you must specify an analytics tracking server for activities that use [!DNL Analytics] for [!DNL Target] (A4T).

>[!NOTE]
>
>If you use [!DNL Analytics] as your activity&#39;s reporting source, you do not need to specify a tracking server during activity creation if you are using mbox.js version 61 (or later) or at.js version 0.9.1 (or later). Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

To ensure that data from [!DNL Target] goes to the correct location in [!DNL Analytics], A4T requires an analytics tracking server to be sent in all calls to Modstats from [!DNL Target]. For implementations using multiple tracking servers you can use the [!DNL Adobe Experience Cloud Debugger] to determine the correct tracking server for your activity.

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität wiedergegeben werden soll, damit gewährleistet ist, dass der richtige Trackingserver ausgewählt wird. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die [!DNL Adobe Experience Cloud Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/install-debugger.html)installieren.

   ![](assets/Screen_DebuggerTrackServ.png)

   The analytics tracking server is found in the [!UICONTROL SiteCatalyst Image] section of the debugger. The field is called *First Party Cookies* or *Third Party Cookies* depending on the implementation, and the [!DNL Analytics] tracking server value will be in one of these formats:

   * (für CNAME-Implementierungen)
   * (für Implementierungen ohne RDC)
   * (für RDC-Implementierung)

   *Firma* steht für den Namen der [!DNL Analytics] Firma, *Metriken* sind ein Beispiel für einen CNAME-Wert und *d1* ist ein Beispiel für ein [!DNL Analytics] Rechenzentrum.
1. Kopieren Sie den Inhalt des Felds vollständig.
1. Fügen Sie die Daten im Abschnitt zu [!UICONTROL Berichtseinstellungen] im Bildschirm „[!UICONTROL Ziele und Einstellungen]**[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

