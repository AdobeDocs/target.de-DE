---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;Adobe Experience Cloud debugger;reporting source
description: Sollten Sie eine ältere Version von „at.js“ oder „mbox.js“ verwenden, müssen Sie einen Trackingserver für Aktivitäten angeben, bei denen Analytics for Target (A4T) zum Einsatz kommt.
title: Verwenden eines Analytics-Trackingservers
feature: a4t general
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 1957e67c8502c06be950c7dafdcc3f6878f87065
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 24%

---


# Verwenden eines Analytics-Trackingservers{#use-an-analytics-tracking-server}

If you are using an older version of at.js or mbox.js, you must specify an analytics tracking server for activities that use [!DNL Analytics] for [!DNL Target] (A4T).

>[!NOTE]
>
>If you use [!DNL Analytics] as your activity&#39;s reporting source, you do not need to specify a tracking server during activity creation if you are using mbox.js version 61 (or later) or at.js version 0.9.1 (or later). Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.
>
>Das [!DNL Target] Team unterstützt &quot;at.js 1&quot;.*x* und at.js 2.*x*. Bitte aktualisieren Sie auf das neueste Update einer der Hauptversionen von at.js, um sicherzustellen, dass Sie eine unterstützte Version ausführen. For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

To ensure that data from [!DNL Target] goes to the correct location in [!DNL Analytics], A4T requires an analytics tracking server to be sent in all calls to Modstats from [!DNL Target]. For implementations using multiple tracking servers you can use the [!DNL Adobe Experience Platform Debugger] or your browser&#39;s Developer Tools to determine the correct tracking server for your activity.

## Abrufen des Analytics-Trackingservers mit dem Adobe Experience Platform Debugger

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität wiedergegeben werden soll, damit gewährleistet ist, dass der richtige Trackingserver ausgewählt wird. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform Debugger](https://docs.adobe.com/content/help/en/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Klicken Sie im linken Navigationsmenü auf **[!UICONTROL Analytics]** .

   The analytics tracking server is found in the [!UICONTROL Hostname] section of the debugger.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anforderung mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie sich beispielsweise auf `adobe.com`befinden, `adobe.com` ist dies der Erstanbieter-Tracking-Server.
   * **Tracking-Server** von Drittanbietern: Ein Drittanbieter-Tracking-Server ist normalerweise `[company].sc.omtrdc.net` der Name Ihrer Firma, endet aber immer in der Firma `sc.omtrdc.net`.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anforderung (sichere Anforderung). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranforderung für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.
1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

## Abrufen des Analytics-Tracking-Servers mithilfe der Developer Tools Ihres Browsers

Die Entwicklerwerkzeuge sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Trackingserver auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die Entwicklerwerkzeuge des Browsers (in Google Chrome klicken Sie auf die drei vertikalen Auslassungspunkte oben rechts > Weitere Werkzeuge > Entwicklerwerkzeuge).

   ![Chrome-Entwicklerwerkzeuge](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Click the **[!UICONTROL Network]** tab.

1. Filtern Sie nach &quot;/ss&quot;, um die Analyseanforderungen anzuzeigen.

   ![Chrome-Entwicklerwerkzeuge](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools-2.png)

   Der Tracking-Server ist der Hostname der Anforderung.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anforderung mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie sich beispielsweise auf `adobe.com`befinden, `adobe.com` ist dies der Erstanbieter-Tracking-Server.
   * **Tracking-Server** von Drittanbietern: Ein Drittanbieter-Tracking-Server ist normalerweise `[company].sc.omtrdc.net` der Name Ihrer Firma, endet aber immer in der Firma `sc.omtrdc.net`.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anforderung (sichere Anforderung). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranforderung für eine http-Seite (nicht sicher).

