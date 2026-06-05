---
keywords: Analytics-Tracking-Server;A4T;Adobe Experience Cloud Debugger;Adobe Experience Platform Debugger;Berichtsquelle;Entwickler-Tools
description: Erfahren Sie, wie Sie einen Analytics-Tracking-Server für Aktivitäten angeben, die Analytics for [!DNL Target] (A4T) verwenden, wenn Sie eine ältere Version von at.js verwenden.
title: Wie verwende ich einen Analytics-Tracking-Server?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
TQID: https://experienceleague.adobe.com/mJM5kZPQfnWodzwQ3qDKxu1e1Oq2Y53fA2LpSB4SVSc
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 708
ht-degree: 17%

---

# Verwenden eines [!DNL Analytics] Trackingservers

Wenn Sie eine ältere Version von at.js verwenden, müssen Sie einen [!DNL Analytics]-Tracking-Server für Aktivitäten angeben, die [!DNL Adobe Analytics] für [!DNL Adobe Target] (A4T) verwenden.

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder höher) müssen Sie bei der Erstellung einer Aktivität keinen Tracking-Server angeben. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.
>
>Das [!DNL Target]-Team unterstützt sowohl at.js 1.*x* als auch at.js 2.*x*. Aktualisieren Sie auf die neueste Version einer der Hauptversionen von at.js, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen finden Sie unter [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.

Um sicherzustellen, dass Daten aus [!DNL Target] an den richtigen Speicherort in [!DNL Analytics] gelangen, muss bei allen Aufrufen von [!DNL Target] an Modstats ein [!DNL Analytics]-Trackingserver gesendet werden. Bei Implementierungen mit mehreren Tracking-Servern verwenden Sie die [!DNL Adobe Experience Platform Debugger] oder die Entwickler-Tools Ihres Browsers, um den richtigen Tracking-Server für Ihre Aktivität zu ermitteln.

## Abrufen des [!DNL Analytics] Tracking-Servers mithilfe der [!DNL Adobe Experience Platform Debugger]

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie eine Aktivität erstellen, die [!DNL Adobe Experience Platform Debugger].

   Wenn Sie den Debugger nicht installiert haben, lesen Sie [Übersicht über Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. Klicken **[!UICONTROL im]** Navigationsmenü auf „Analytics“.

   ![screen_debuggerTrackServ image](assets/Screen_DebuggerTrackServ.png)

   Der [!DNL Analytics]-Trackingserver befindet sich im [!UICONTROL Hostname] des Debuggers.

   * **Erstanbieter-Tracking-Server**: Wenn der Host-Name der Anfrage mit der Domain übereinstimmt, in der Sie sich befinden, handelt es sich um einen Erstanbieter-Tracking-Server. Wenn Sie sich beispielsweise in `adobe.com` befinden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Tracking-Server eines Drittanbieters**: Ein Tracking-Server eines Drittanbieters wird normalerweise `[company].sc.omtrdc.net`, wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net` endet.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-First-Party-Tracking-Server für eine (sichere) https-Anfrage. `stats.adobe.com` ist ein Beispiel für eine CNAME-First-Party-Anfrage für eine HTTP-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie **[!UICONTROL Abschnitt &quot;]**&quot; des Bildschirms **[!UICONTROL Ziel und Einstellungen]** Ihrer Aktivität die Tracking-Server-Informationen in das Feld **[!UICONTROL Tracking-Server]** ein.

   >[!NOTE]
   >
   >Wählen Sie [!UICONTROL Analytics als Reporting-Source] aus, damit Ihre Aktivität für das Feld [!UICONTROL Tracking-Server] verfügbar ist.

## Abrufen des [!DNL Analytics] Tracking-Servers mit den Entwickler-Tools Ihres Browsers

Die Entwickler-Tools sollten auf einer Seite angezeigt werden, auf der die Aktivität bereitgestellt wird, um sicherzustellen, dass Sie den richtigen Tracking-Server auswählen. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie eine Aktivität erstellen, die Entwickler-Tools des Browsers (klicken Sie in Google Chrome oben rechts auf die drei vertikalen Auslassungszeichen > Weitere Tools > Entwickler-Tools).

   ![Chrome-Entwickler-Tools](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klicken Sie auf **[!UICONTROL Registerkarte]** Netzwerk“.

1. Filtern Sie nach `/ss,`, um die [!DNL Analytics] anzuzeigen.

   ![Chrome-Entwicklertools mit der /ss-Suche](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Der Tracking-Server ist der Host-Name der Anfrage.

   * **Erstanbieter-Tracking-Server**: Wenn der Host-Name der Anfrage mit der Domain übereinstimmt, in der Sie sich befinden, handelt es sich um einen Erstanbieter-Tracking-Server. Wenn Sie sich beispielsweise in `adobe.com` befinden, ist `adobe.com` der Erstanbieter-Tracking-Server.
   * **Tracking-Server eines Drittanbieters**: Ein Tracking-Server eines Drittanbieters wird normalerweise `[company].sc.omtrdc.net`, wobei das Unternehmen der Name Ihres Unternehmens ist, aber immer in `sc.omtrdc.net` endet.
   * **CNAME-Implementierungen**: `sstats.adobe.com` ist ein Beispiel für einen CNAME-First-Party-Tracking-Server für eine (sichere) https-Anfrage. `stats.adobe.com` ist ein Beispiel für eine CNAME-First-Party-Anfrage für eine HTTP-Seite (nicht sicher).

1. Kopieren Sie den Inhalt des Felds vollständig.

1. Fügen Sie **[!UICONTROL Abschnitt &quot;]**&quot; des Bildschirms **[!UICONTROL Ziel und Einstellungen]** Ihrer Aktivität die Tracking-Server-Informationen in das Feld **[!UICONTROL Tracking-Server]** ein.

   >[!NOTE]
   >
   >Wählen Sie [!UICONTROL Analytics als Reporting-Source] aus, damit Ihre Aktivität für das Feld [!UICONTROL Tracking-Server] verfügbar ist.
