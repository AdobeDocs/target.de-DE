---
keywords: Analytics-Tracking-Server;A4T;Adobe Experience Cloud-Debugger;Adobe Experience Platform-Debugger;Berichtsquelle;Entwicklertools
description: 'Erfahren Sie, wie Sie einen Analytics-Tracking-Server für Aktivitäten angeben, die Analytics für [!DNL Target]  (A4T) verwenden, wenn Sie eine ältere Version von at.js verwenden. '
title: Wie verwende ich einen Analytics-Tracking-Server?
feature: 'Analytics for Target (A4T) '
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 19%

---

# Verwenden eines Analytics-Trackingservers

Wenn Sie eine ältere Version von at.js verwenden, müssen Sie einen Analytics-Trackingserver für Aktivitäten angeben, die [!DNL Adobe Analytics] für [!DNL Adobe Target] (A4T) verwenden.

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder neuer) müssen Sie bei der Erstellung einer Aktivität keinen Trackingserver angeben. Die at.js-Bibliothek sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.
>
>Das [!DNL Target]-Team unterstützt beide at.js 1.*x* und at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen finden Sie unter [at.js-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

Um sicherzustellen, dass Daten von [!DNL Target] an die richtige Stelle in [!DNL Analytics] gehen, muss für A4T ein Analytics-Tracking-Server in allen Aufrufen an Modstats von [!DNL Target] gesendet werden. Verwenden Sie bei Implementierungen mit mehreren Tracking-Servern [!DNL Adobe Experience Platform Debugger] oder die Entwicklertools Ihres Browsers, um den richtigen Tracking-Server für Ihre Aktivität zu ermitteln.

## Abrufen des Analytics-Tracking-Servers mit dem Adobe Experience Platform Debugger

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie die Aktivität erstellen, den [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform-Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Klicken Sie im linken Navigationsmenü auf **[!UICONTROL Analytics]** .

   Der Analytics-Tracking-Server befindet sich im Abschnitt [!UICONTROL Hostname] des Debuggers.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise `adobe.com` verwenden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Drittanbieter-Tracking-Server**: Ein Drittanbieter-Tracking-Server ist in der Regel  `[company].sc.omtrdc.net` der Name Ihres Unternehmens, endet aber immer in  `sc.omtrdc.net`.
   * **CNAME-Implementierungen**:  `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Wählen Sie [!UICONTROL Analytics als Berichtsquelle] für Ihre Aktivität aus, damit das Feld [!UICONTROL Tracking-Server] verfügbar ist.

## Rufen Sie den Analytics-Tracking-Server mit den Entwicklertools Ihres Browsers ab.

Die Entwicklertools sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die Entwicklertools des Browsers (klicken Sie in Google Chrome auf die drei vertikalen Ellipsen oben rechts > Weitere Tools > Entwicklertools).

   ![Chrome-Entwicklertools](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Netzwerk]** .

1. Filtern Sie nach `/ss,`, um die Analytics-Anforderungen anzuzeigen.

   ![Chrome-Entwicklertools mit /ss-Suche](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Der Tracking-Server ist der Hostname der Anfrage.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise `adobe.com` verwenden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Drittanbieter-Tracking-Server**: Ein Drittanbieter-Tracking-Server ist in der Regel  `[company].sc.omtrdc.net` der Name Ihres Unternehmens, endet aber immer in  `sc.omtrdc.net`.
   * **CNAME-Implementierungen**:  `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Wählen Sie [!UICONTROL Analytics als Berichtsquelle] für Ihre Aktivität aus, damit das Feld [!UICONTROL Tracking-Server] verfügbar ist.
