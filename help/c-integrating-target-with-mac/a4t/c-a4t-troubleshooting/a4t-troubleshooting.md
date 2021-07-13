---
keywords: Analytics-Trackingserver; A4T; Analytics-Segmente; Report Suites; falsche Daten; verwaist; sdid; VisitorAPI.js; mboxMCSDID; Phantom; unspezifisch
description: Erfahren Sie mehr über häufige Probleme, die bei Kunden bei der Verwendung von Analytics for [!DNL Target] (A4T) aufgetreten sind.
title: Fehlerbehebung bei der Analytics- und [!DNL Target] Integration (A4T)
feature: 'Analytics for Target (A4T) '
exl-id: 7d155cbe-e799-43b5-afc2-1aea43f432ba
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 39%

---

# Fehlerbehebung bei der Analytics- und [!DNL Target]-Integration (A4T)

In diesem Thema werden einige häufige Probleme behandelt, die bei der Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) aufgetreten sind.

## Aktivitäten weisen keine Daten in Analytics auf, werden jedoch stattdessen als „unspezifisch“ aufgeführt. {#unspecified}

Es gibt verschiedene Gründe, warum Daten als &quot;nicht angegeben&quot;angezeigt werden:

* Die Classification in [!DNL Target] wurde noch nicht vollständig verarbeitet.

   Die Klassifizierung von Berichten dauert in der Regel 24 bis 72 Stunden, nachdem sie zum ersten Mal gespeichert wurden.

* Die Report Suite enthält in diesem Zeitraum keine Daten, [!DNL Target] versucht jedoch, Treffer zu klassifizieren. [!DNL Target] kann Daten so lange nicht klassifizieren, bis ein erster Treffer registriert wird.

   Stellen Sie sicher, dass in der Report Suite mindestens ein Treffer registriert wurde.

* Der Classification-Aufruf von [!DNL Target] an [!DNL Analytics] ist fehlgeschlagen.

   [Wenden Sie sich für Unterstützung an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

Wenn Sie die Zeile &quot;Nicht angegeben&quot;durch die Dimension &quot;Analytics for Target&quot;aufschlüsseln und sie keine Aktivitäts-IDs enthält, bedeutet dies, dass alles ordnungsgemäß klassifiziert ist. Wenn dort Aktivitäts-IDs aufgelistet sind, dient dies als Hinweis für ein Classification-Problem.

>[!NOTE]
>
>Manchmal werden Daten korrekt in Berichten angezeigt, dann aber wieder &quot;nicht angegeben&quot;, da eine neue Aktivität hinzugefügt wurde, deren Classification noch nicht abgeschlossen wurde. Beachten Sie, dass die Klassifizierung von Berichten nach dem ersten Speichern in der Regel zwischen 24 und 72 Stunden dauert.
>
>Daten, die als „unspezifisch“ eingestuft werden, gehen nicht verloren. Die Daten werden nach erfolgreicher Classification den entsprechenden Aktivitäten oder Erlebnissen zugeordnet.

## A4T-Aktivitätsberichte enthalten eine Zeile mit vielen &quot;nicht spezifizierten&quot;Ereignissen. {#added_unspecified_events}

Je nach der Metrik, mit der Sie Ihre Daten anzeigen, kann in Ihrem Bericht eine Ereigniszeile &quot;[!UICONTROL Nicht angegeben]&quot;angezeigt werden.

In der Regel wird diese Zeile angezeigt, wenn Sie eine allgemeine Metrik im Bericht auswählen, die nicht [!DNL Target]-spezifisch ist (z. B. [!UICONTROL Seitenansichten], [!UICONTROL Besuche], [!UICONTROL Unique Visitors] usw.). In diesem Fall enthält die Zeile [!UICONTROL &quot;Nicht angegeben&quot;] alle [!UICONTROL Seitenansichten], [!UICONTROL Besuche] und [!UICONTROL Unique Visitors], die nicht mit [!DNL Target] -Aktivitäten verknüpft sind.

Diese Zeile enthält keine [!DNL Target]-verknüpften Informationen (z. B. keine Besucher, Besuche oder Impressionen). Weitere Informationen finden Sie unter [&quot;Unspecified&quot;, &quot;None&quot;, &quot;Other&quot;und &quot;Unknown&quot;in der Berichterstellung](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=en) in den *Analytics-Tech-Notes*.

Wenn Sie eine [!DNL Target]-spezifische Metrik im Bericht auswählen, wird die Zeile [!UICONTROL &quot;Nicht angegeben&quot;] nicht angezeigt. Die einzige Möglichkeit, dies im Bericht zu vermeiden, besteht darin, einen [!DNL Target] -Aufruf für jede von dieser Seite gesendete Anfrage festzulegen, was nicht üblich oder notwendig ist.

## In meinen Analytics-Daten tauchen zu hohe Besucherzahlen auf, seit ich A4T verwende.  {#section_4BE374E573D44FB7918611699B74F58E}

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Die geschätzte Steigerung der Umsatzmetriken zeigt keine korrekten Daten. {#section_35D766E5E4D347C39E15D08AA883FBB0}

Steigerungs- und Vertrauensdaten sind in Analytics nicht verfügbar. Sie stehen jedoch in den Target-Berichten zur Verfügung.

## Aktivitäten erscheinen nicht in Analytics-Berichten.  {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Für A4T-Aktivitäten ist ein Trackingserver erforderlich, der zuvor festgelegt werden muss. Weitere Informationen zu diesem Thema finden Sie unter  [Verwenden eines Analytics-Tracking-](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) Servers, um sicherzustellen, dass Ihr Analytics-Tracking-Server korrekt eingerichtet ist.

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder neuer) müssen Sie bei der Erstellung einer Aktivität keinen Trackingserver angeben. Die at.js-Bibliothek sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

## Meine Analytics-Segmente werden nicht in Target angezeigt.  {#section_DEE87F1557834F448E99381D3D02EEEF}

Vergewissern Sie sich, dass Sie entsprechende Berechtigungen haben, bevor Sie A4T-Aktivitäten erstellen:

* Gehören Sie zur Zugriffsgruppe für Webdienste in Adobe Analytics, um Analytics als Berichtsquelle für Target verwenden zu können.
* Seien Sie Mitglied einer oder mehrerer Experience Cloud-Gruppen, die Zugriff auf Analytics und Target haben.
* Überprüfen Sie, ob Analytics und Target im Abschnitt Marketing-Apps in der linken Navigation angezeigt wird.

## Absprungraten, Absprünge und Ausstiegsmetriken erscheinen in Berichten als positiv.  {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Diese Metriken, die in Berichten als positiv erscheinen, sind ein bekanntes Problem.

Obwohl diese Metriken negativ sind, wird die Steigerung in den Target-Berichten als positiv gezeigt. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

## Die benötigte Report Suite wird nicht angezeigt. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

Die Liste der Report Suites, die in [!DNL Target Standard/Premium] angezeigt wird, ist die Liste der Report Suites, die für [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) konfiguriert wurden. Möglicherweise sehen Sie nicht alle Report Suites, die Sie besitzen.

Wenn Sie mehrere Berichtsquellen verwenden, müssen die Report Suites auch in der standardmäßigen Berichtsquelle vorhanden sein, die in [!DNL Target] festgelegt ist. Wenn sich die Report Suites nicht in der Standard-Berichtsquelle befinden, werden die Report Suites nicht angezeigt.

Wenn die gewünschte Report Suite immer noch nicht angezeigt wird, wenden Sie sich an [Kundenunterstützung](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um sie zu aktivieren.

## In meinen Berichten sind weniger Daten vorhanden als erwartet. {#section_75002584FA63456D8D9086172925DD8D}

Überprüfen Sie Ihre Implementierung, insbesondere auf Seiten, auf denen Ihre Besucher die Kriterien für Erlebnisse erfüllen und stellen Sie sicher, dass die zusätzlichen Daten-IDs in den [!DNL Target]- und den [!DNL Analytics]-Aufrufen übereinstimmen.

* **at.js 1.x**: Im  [!DNL Target] Aufruf ist die zusätzliche ID im  `mboxMCSDID` Parameter enthalten. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.
* **at.js 2.x**: Im  [!DNL Target] Aufruf wird die zusätzliche ID im HTTP-Header als Wert für  `experienceCloud.analytics.supplementalDataId`zurückgegeben. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.

Die einfachste Möglichkeit, die zusätzliche ID zu untersuchen, besteht in der Verwendung des Adobe Experience Platform Debuggers.

Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform-Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

![Debugger](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

Wenn im [!DNL Target] -Aufruf keine zusätzliche Daten-ID enthalten ist, überprüfen Sie, ob die [!DNL VisitorAPI.js] -Datei vor [!DNL at.js] geladen wird. Falls im [!DNL Analytics]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob der [!DNL Target]-Aufruf vor dem [!DNL Analytics]-Aufruf erfolgt.

Weitere Informationen finden Sie unter [Analytics für Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) oder wenden Sie sich an den [Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
