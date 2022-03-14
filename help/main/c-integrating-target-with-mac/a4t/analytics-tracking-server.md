---
keywords: Analytics-Tracking-Server;A4T;Adobe Experience Cloud-Debugger;Adobe Experience Platform-Debugger;Berichtsquelle;Entwicklertools
description: 'Erfahren Sie, wie Sie einen Analytics-Tracking-Server für Aktivitäten angeben, die Analytics für [!DNL Target] (A4T), wenn Sie eine ältere Version von at.js verwenden. '
title: Wie verwende ich einen Analytics-Tracking-Server?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 19%

---

# Verwenden eines Analytics-Trackingservers

Wenn Sie eine ältere Version von at.js verwenden, müssen Sie einen Analytics-Trackingserver für Aktivitäten angeben, die [!DNL Adobe Analytics] für [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder neuer) müssen Sie bei der Erstellung einer Aktivität keinen Trackingserver angeben. Die at.js-Bibliothek sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.
>
>Die [!DNL Target] -Team unterstützt beide at.js 1.*x* und at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen finden Sie unter [at.js-Versionsdetails](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

Um sicherzustellen, dass Daten aus [!DNL Target] an die richtige Stelle in [!DNL Analytics], erfordert A4T, dass bei allen Aufrufen von ein Analytics-Tracking-Server an Modstats gesendet wird. [!DNL Target]. Verwenden Sie für Implementierungen mit mehreren Tracking-Servern die Variable [!DNL Adobe Experience Platform Debugger] oder in den Entwicklertools Ihres Browsers, um den richtigen Tracking-Server für Ihre Aktivität zu ermitteln.

## Abrufen des Analytics-Tracking-Servers mit dem Adobe Experience Platform Debugger

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Klicken **[!UICONTROL Analytics]** im linken Navigationsmenü.

   Der Analytics-Tracking-Server befindet sich im [!UICONTROL Hostname] -Abschnitt des Debuggers.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise auf `adobe.com`, `adobe.com` ist der Erstanbieter-Tracking-Server.
   * **Tracking-Server von Drittanbietern**: Ein Trackingserver eines Drittanbieters ist normalerweise `[company].sc.omtrdc.net` wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net`.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Auswählen [!UICONTROL Analytics als Berichtsquelle] für Ihre -Aktivität [!UICONTROL Tracking-Server] -Feld verfügbar sein.

## Rufen Sie den Analytics-Tracking-Server mit den Entwicklertools Ihres Browsers ab.

Die Entwicklertools sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die Entwicklertools des Browsers (in Google Chrome klicken Sie auf die drei vertikalen Ellipsen oben rechts > Weitere Tools > Entwicklertools).

   ![Chrome-Entwicklertools](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klicken Sie auf **[!UICONTROL Netzwerk]** Registerkarte.

1. Filtern nach `/ss,` , um die Analytics-Anforderungen anzuzeigen.

   ![Chrome-Entwicklertools mit /ss-Suche](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Der Tracking-Server ist der Hostname der Anfrage.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise auf `adobe.com`, `adobe.com` ist der Erstanbieter-Tracking-Server.
   * **Tracking-Server von Drittanbietern**: Ein Trackingserver eines Drittanbieters ist normalerweise `[company].sc.omtrdc.net` wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net`.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Auswählen [!UICONTROL Analytics als Berichtsquelle] für Ihre -Aktivität [!UICONTROL Tracking-Server] -Feld verfügbar sein.
