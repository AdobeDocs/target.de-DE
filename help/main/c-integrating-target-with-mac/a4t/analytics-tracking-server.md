---
keywords: Analytics-Tracking-Server;A4T;Adobe Experience Cloud-Debugger;Adobe Experience Platform-Debugger;Berichtsquelle;Entwicklertools
description: Erfahren Sie, wie Sie einen Analytics-Tracking-Server für Aktivitäten angeben, die Analytics für [!DNL Target]  (A4T) verwenden, wenn Sie eine ältere Version von at.js verwenden.
title: Wie verwende ich einen Analytics-Tracking-Server?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 14%

---

# Verwenden eines [!DNL Analytics]-Tracking-Servers

Wenn Sie eine ältere Version von at.js verwenden, müssen Sie einen [!DNL Analytics]-Tracking-Server für Aktivitäten angeben, die [!DNL Adobe Analytics] für [!DNL Adobe Target] (A4T) verwenden.

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder höher) müssen Sie bei der Erstellung einer Aktivität keinen Tracking-Server angeben. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Goals & Settings] leer lassen.
>
>Das [!DNL Target]-Team unterstützt beide at.js 1.*x* und in at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen finden Sie unter [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.

Um sicherzustellen, dass Daten aus [!DNL Target] an den richtigen Speicherort in [!DNL Analytics] gelangen, muss für A4T ein [!DNL Analytics] -Tracking-Server in allen Aufrufen von [!DNL Target] an Modstats gesendet werden. Verwenden Sie bei Implementierungen mit mehreren Tracking-Servern [!DNL Adobe Experience Platform Debugger] oder die Entwicklertools Ihres Browsers, um den richtigen Tracking-Server für Ihre Aktivität zu ermitteln.

## Rufen Sie den [!DNL Analytics]-Tracking-Server mit dem [!DNL Adobe Experience Platform Debugger] ab.

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie die Aktivität erstellen, den [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Adobe Experience Platform Debugger - Übersicht](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. Klicken Sie im linken Navigationsmenü auf **[!UICONTROL Analytics]** .

   ![Screen_DebuggerTrackServ image](assets/Screen_DebuggerTrackServ.png)

   Der Trackingserver [!DNL Analytics] befindet sich im Abschnitt [!UICONTROL Hostname] des Debuggers.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise `adobe.com` verwenden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Tracking-Server von Drittanbietern**: Ein Tracking-Server von Drittanbietern ist in der Regel `[company].sc.omtrdc.net` , wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net` endet.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie im Abschnitt **[!UICONTROL Reporting Settings]** des Bildschirms **[!UICONTROL Goal & Settings]** Ihrer Aktivität die Tracking-Server-Informationen in das Feld **[!UICONTROL Tracking Server]** ein.

   >[!NOTE]
   >
   >Wählen Sie [!UICONTROL Analytics as the Reporting Source] für Ihre Aktivität aus, damit das Feld [!UICONTROL Tracking Server] verfügbar ist.

## Rufen Sie den [!DNL Analytics]-Tracking-Server mit den Entwicklertools Ihres Browsers ab.

Die Entwicklertools sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie Ihre Aktivität erstellen, die Entwicklertools des Browsers (in Google Chrome klicken Sie auf die drei vertikalen Ellipsen oben rechts > Weitere Tools > Entwicklertools).

   ![Chrome-Entwicklertools](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Network]** .

1. Filtern Sie nach &quot;`/ss,`&quot;, um die [!DNL Analytics] -Anforderungen anzuzeigen.

   ![Chrome-Entwicklertools mit /ss-Suche](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Der Tracking-Server ist der Hostname der Anfrage.

   * **Erstanbieter-Tracking-Server**: Wenn der Hostname der Anfrage mit der Domäne übereinstimmt, in der Sie sich befinden, ist es ein Erstanbieter-Tracking-Server. Wenn Sie beispielsweise `adobe.com` verwenden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Tracking-Server von Drittanbietern**: Ein Tracking-Server von Drittanbietern ist in der Regel `[company].sc.omtrdc.net` , wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net` endet.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-Erstanbieter-Tracking-Server für eine HTTPS-Anfrage (sicher). `stats.adobe.com` ist ein Beispiel für eine CNAME-Erstanbieteranfrage für eine http-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie im Abschnitt **[!UICONTROL Reporting Settings]** des Bildschirms **[!UICONTROL Goal & Settings]** Ihrer Aktivität die Tracking-Server-Informationen in das Feld **[!UICONTROL Tracking Server]** ein.

   >[!NOTE]
   >
   >Wählen Sie [!UICONTROL Analytics as the Reporting Source] für Ihre Aktivität aus, damit das Feld [!UICONTROL Tracking Server] verfügbar ist.
