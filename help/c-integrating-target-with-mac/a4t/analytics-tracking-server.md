---
keywords: Analytics-Tracking-Server;A4T;Adobe Experience Cloud-Debugger;Adobe Experience Platform-Debugger;Berichte-Quelle;Entwicklerwerkzeuge
description: Sollten Sie eine ältere Version von „at.js“ oder „mbox.js“ verwenden, müssen Sie einen Trackingserver für Aktivitäten angeben, bei denen Analytics for Target (A4T) zum Einsatz kommt.
title: Analytics-Tracking-Server verwenden
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 25%

---


# Verwenden eines Analytics-Trackingservers

Wenn Sie eine ältere Version von at.js oder mbox.js verwenden, müssen Sie einen Analytics-Tracking-Server für Aktivitäten angeben, die [!DNL Analytics] für [!DNL Target] (A4T) verwenden.

>[!NOTE]
>
>Wenn Sie [!DNL Analytics] als Berichte Ihrer Aktivität verwenden, müssen Sie bei der Erstellung der Aktivität keinen Trackingserver angeben, wenn Sie &quot;mbox.js&quot;Version 61 (oder höher) oder &quot;at.js&quot;Version 0.9.1 (oder höher) verwenden. Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.
>
>Das [!DNL Target]-Team unterstützt beide &quot;at.js 1&quot;.*x* und at.js 2.*x*. Bitte aktualisieren Sie auf das neueste Update einer der Hauptversionen von at.js, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen finden Sie unter [at.js Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

Um sicherzustellen, dass Daten von [!DNL Target] an den richtigen Speicherort in [!DNL Analytics] gesendet werden, erfordert A4T, dass bei allen Aufrufen von [!DNL Target] ein Analytics-Tracking-Server an Modstats gesendet wird. Bei Implementierungen mit mehreren Tracking-Servern können Sie mit den [!DNL Adobe Experience Platform Debugger]- oder Developer Tools Ihres Browsers den richtigen Tracking-Server für Ihre Aktivität ermitteln.

## Analytics-Tracking-Server mit dem Adobe Experience Platform Debugger abrufen

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität wiedergegeben werden soll, damit gewährleistet ist, dass der richtige Trackingserver ausgewählt wird. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, das [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Klicken Sie im linken Navigationsmenü auf **[!UICONTROL Analytics]**.

   Der Analytics-Tracking-Server befindet sich im Abschnitt [!UICONTROL Hostname] des Debuggers.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anforderung mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise `adobe.com` verwenden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Tracking-Server** von Drittanbietern: Ein Tracking-Server eines Drittanbieters ist in der Regel  `[company].sc.omtrdc.net` der Name Ihrer Firma, endet aber immer in der Firma  `sc.omtrdc.net`.
   * **CNAME-Implementierungen**:  `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anforderung (sichere Anforderung). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranforderung für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Sie müssen [!UICONTROL Analytics als Berichte-Quelle] für Ihre Aktivität auswählen, damit das Feld [!UICONTROL Tracking-Server] verfügbar ist.

## Analytics-Tracking-Server mit den Developer Tools Ihres Browsers abrufen

Die Entwicklerwerkzeuge sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Trackingserver auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die Entwicklerwerkzeuge des Browsers (in Google Chrome klicken Sie auf die drei vertikalen Auslassungspunkte oben rechts > Weitere Werkzeuge > Entwicklerwerkzeuge).

   ![Chrome-Entwicklerwerkzeuge](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Netzwerk]**.

1. Filtern Sie nach `/ss,`, um die Analytics-Anforderungen anzuzeigen.

   ![Chrome-Entwicklerwerkzeuge mit /ss-Suche](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Der Tracking-Server ist der Hostname der Anforderung.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anforderung mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise `adobe.com` verwenden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Tracking-Server** von Drittanbietern: Ein Tracking-Server eines Drittanbieters ist in der Regel  `[company].sc.omtrdc.net` der Name Ihrer Firma, endet aber immer in der Firma  `sc.omtrdc.net`.
   * **CNAME-Implementierungen**:  `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anforderung (sichere Anforderung). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranforderung für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie die Daten im Abschnitt zu **[!UICONTROL Berichtseinstellungen]** im Bildschirm „**[!UICONTROL Ziele und Einstellungen]****[!UICONTROL “ in das Feld Trackingserver]** ein.

   >[!NOTE]
   >
   >Sie müssen [!UICONTROL Analytics als Berichte-Quelle] für Ihre Aktivität auswählen, damit das Feld [!UICONTROL Tracking-Server] verfügbar ist.

