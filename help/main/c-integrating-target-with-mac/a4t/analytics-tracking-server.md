---
keywords: Analytics-Tracking-Server;A4T;Adobe Experience Cloud-Debugger;Adobe Experience Platform-Debugger;Berichtsquelle;Entwicklertools
description: Erfahren Sie, wie Sie einen Analytics-Tracking-Server für Aktivitäten angeben, die Analytics für [!DNL Target] (A4T), wenn Sie eine ältere Version von at.js verwenden.
title: Wie verwende ich einen Analytics-Tracking-Server?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 22%

---

# Verwenden Sie eine [!DNL Analytics] Tracking-Server

Wenn Sie eine ältere Version von at.js verwenden, müssen Sie eine [!DNL Analytics] Tracking-Server für Aktivitäten, die [!DNL Adobe Analytics] für [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder höher) müssen Sie bei der Erstellung einer Aktivität keinen Tracking-Server angeben. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Ziele und Einstellungen] leer lassen.
>
>Die [!DNL Target] -Team unterstützt beide at.js 1.*x* und at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen finden Sie unter [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

Um sicherzustellen, dass Daten aus [!DNL Target] an die richtige Stelle in [!DNL Analytics], erfordert A4T eine [!DNL Analytics] Tracking-Server, der in allen Aufrufen von an Modstats gesendet wird [!DNL Target]. Verwenden Sie für Implementierungen mit mehreren Tracking-Servern die Variable [!DNL Adobe Experience Platform Debugger] oder in den Entwicklertools Ihres Browsers, um den richtigen Tracking-Server für Ihre Aktivität zu ermitteln.

## Rufen Sie die [!DNL Analytics] Tracking-Server mit [!DNL Adobe Experience Platform Debugger]

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Übersicht über Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. Klicken **[!UICONTROL Analytics]** im linken Navigationsmenü.

   ![Screen_DebuggerTrackServ-Bild](assets/Screen_DebuggerTrackServ.png)

   Die [!DNL Analytics] Der Tracking-Server befindet sich im [!UICONTROL Hostname] -Abschnitt des Debuggers.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise auf `adobe.com`, `adobe.com` ist der Erstanbieter-Tracking-Server.
   * **Tracking-Server von Drittanbietern**: Ein Trackingserver eines Drittanbieters ist normalerweise `[company].sc.omtrdc.net` wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net`.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Auswählen [!UICONTROL Analytics als Berichtsquelle] für Ihre -Aktivität [!UICONTROL Tracking-Server] -Feld verfügbar sein.

## Rufen Sie die [!DNL Analytics] Tracking-Server mit den Entwicklertools Ihres Browsers

Die Entwicklertools sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die Entwicklertools des Browsers (in Google Chrome klicken Sie auf die drei vertikalen Ellipsen oben rechts > Weitere Tools > Entwicklertools).

   ![Chrome-Entwicklertools](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klicken Sie auf **[!UICONTROL Netzwerk]** Registerkarte.

1. Filtern nach `/ss,` , um [!DNL Analytics] -Anfragen.

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
