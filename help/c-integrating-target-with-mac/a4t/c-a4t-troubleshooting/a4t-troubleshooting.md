---
keywords: analytics tracking server;A4T;analytics segments;report suites;incorrect data;orphaned;sdid;VisitorAPI.js;mboxMCSDID;phantom;unspecified
description: In diesem Thema werden einige allgemeine Probleme behandelt, die auftreten, wenn Analytics als Berichtsquelle für Target (A4T) verwendet wird.
title: Fehlerbehebung bei der Analytics- und Target-Integration (A4T)
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: bac88f7535afe31fd9882f56de0cd4b5ae8a730b
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 63%

---


# Fehlerbehebung bei der Analytics- und Target-Integration (A4T){#troubleshoot-the-analytics-and-target-integration-a-t}

In diesem Thema werden einige allgemeine Probleme behandelt, die auftreten, wenn Analytics als Berichtsquelle für Target (A4T) verwendet wird.

## Aktivitäten weisen keine Daten in Analytics auf, werden jedoch stattdessen als „unspezifisch“ aufgeführt.{#unspecified}

Hierfür gibt es verschiedene Gründe:

* Die Classification in [!DNL Target] wurde noch nicht vollständig verarbeitet.

   Die Klassifizierung von Berichten dauert normalerweise nach dem ersten Speichern zwischen 24 und 72 Stunden.

* Die Report Suite enthält in diesem Zeitraum keine Daten, [!DNL Target] versucht jedoch, Treffer zu klassifizieren. [!DNL Target] kann Daten so lange nicht klassifizieren, bis ein erster Treffer registriert wird.

   Stellen Sie sicher, dass in der Report Suite mindestens ein Treffer registriert wurde.

* Der Classification-Aufruf von [!DNL Target] an [!DNL Analytics] ist fehlgeschlagen.

   [Wenden Sie sich für Unterstützung an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

Wenn Sie die Zeile &quot;Nicht angegeben&quot;durch die Dimension &quot;Analytics für Zielgruppe&quot;unterteilen und sie keine Aktivitäten-IDs enthält, bedeutet dies, dass alles korrekt klassifiziert wird.  Wenn dort Aktivitäten-IDs aufgeführt sind, dient sie als Indikator für ein Klassifizierungsproblem.

>[!NOTE]
>
>Manchmal werden Daten korrekt in Berichten angezeigt, dann jedoch erneut als „unspezifisch“ gekennzeichnet, da eine neue Aktivität hinzugefügt wurde, deren Classification noch nicht abgeschlossen wurde. Beachten Sie, dass die Klassifizierung von Berichten nach dem ersten Speichern normalerweise zwischen 24 und 72 Stunden dauert.
>
>Daten, die als „unspezifisch“ eingestuft werden, gehen nicht verloren. Die Daten werden nach erfolgreicher Classification den entsprechenden Aktivitäten oder Erlebnissen zugeordnet.


## Die Berichte zu A4T-Aktivitäten enthalten eine Zeile mit einer großen Anzahl von &quot;nicht angegebenen&quot;Ereignissen. {#added_unspecified_events}

Je nach der Metrik, mit der Sie Ihre Daten anzeigen, wird in Ihrem Bericht möglicherweise eine Zeile mit &quot;nicht angegebenen&quot;Ereignissen angezeigt.

In der Regel wird diese Zeile angezeigt, wenn Sie eine häufig verwendete Metrik im Bericht wählen, die nicht für die Zielgruppe spezifisch ist (z. B. Ansichten der Seite, Besuche, individuelle Besucher usw.).
In diesem Fall enthält die Zeile &quot;Nicht angegeben&quot;alle Ansichten, Besuche und individuellen Besucher, die nicht mit den Aktivitäten der Zielgruppe verknüpft sind.
Diese Zeile enthält keine mit der Zielgruppe verknüpften Informationen (z. B. keine Besucher, Besuche oder Impressionen). Weitere Informationen finden Sie unter [&quot;Nicht angegeben&quot;, &quot;Keine&quot;, &quot;Sonstige&quot;und &quot;Unbekannt&quot;in Berichte](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=en) in den *Analytics-technischen Hinweisen*.

Wenn Sie eine für die Zielgruppe spezifische Metrik im Bericht auswählen, wird diese Zeile &quot;Nicht angegeben&quot;nicht angezeigt.
Die einzige Möglichkeit, dies im Bericht ganz zu vermeiden, besteht darin, für jede von dieser Seite gesendete Anforderung einen Zielgruppe-Aufruf zu starten, was nicht üblich oder notwendig ist.

## In meinen Analytics-Daten tauchen zu hohe Besucherzahlen auf, seit ich A4T verwende.   {#section_4BE374E573D44FB7918611699B74F58E}

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Die geschätzte Steigerung der Umsatzmetriken zeigt keine korrekten Daten. {#section_35D766E5E4D347C39E15D08AA883FBB0}

Steigerungs- und Vertrauensdaten sind in Analytics nicht verfügbar. Sie stehen jedoch in den Target-Berichten zur Verfügung.

## Aktivitäten erscheinen nicht in Analytics-Berichten.   {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Für A4T-Aktivitäten ist ein Trackingserver erforderlich, der zuvor festgelegt werden muss. Weitere Informationen zu diesem Thema finden Sie unter [Verwenden eines Analytics-Trackingservers](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) zur Überprüfung der korrekten Einrichtung Ihres Analytics-Trackingservers.

>[!NOTE]
>
>Sollten Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität und bei der Verwendung von mbox.js Version 61 (oder neuer) oder at.js Version 0.9.1 (oder neuer) keinen Trackingserver angeben. Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

## Meine Analytics-Segmente werden nicht in Target angezeigt.   {#section_DEE87F1557834F448E99381D3D02EEEF}

Vergewissern Sie sich, dass Sie entsprechende Berechtigungen haben, bevor Sie A4T-Aktivitäten erstellen:

* Sie müssen zur Zugriffsgruppe für Webdienste in Adobe Analytics gehören, um Analytics als Berichtsquelle für Target nutzen zu können.
* Sie müssen Mitglied in mindestens einer Experience Cloud-Gruppe sein, die Zugriff auf Analytics und Target hat.
* Überprüfen Sie, ob Analytics und Target im Abschnitt Marketing-Apps in der linken Navigation angezeigt wird.

## Absprungraten, Absprünge und Ausstiegsmetriken erscheinen in Berichten als positiv.   {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Dieses Problem ist bekannt.

Obwohl diese Metriken negativ sind, wird die Steigerung in den Target-Berichten als positiv gezeigt. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

## Die benötigte Report Suite wird nicht angezeigt. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

Die Liste der Report Suites, die in [!DNL Target Standard/Premium] angezeigt wird, ist die Liste der Report Suites, die für [!DNL Analytics] als Berichte-Quelle für [!DNL Target] (A4T) konfiguriert wurden. Das bedeutet, dass Sie möglicherweise nicht alle vorhandenen Report Suites sehen.

Wenn Sie außerdem mehrere Berichte-Quellen verwenden, müssen die Report Suites auch in der Standardquelle des Berichte in [!DNL Target] vorhanden sein. Andernfalls werden die Report Suites nicht angezeigt.

Wenn die gesuchte Report Suite immer noch nicht angezeigt wird, wenden Sie sich an [Client Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C), um sie zu aktivieren.

## In meinen Berichten sind weniger Daten vorhanden als erwartet. {#section_75002584FA63456D8D9086172925DD8D}

Überprüfen Sie Ihre Implementierung, insbesondere auf Seiten, auf denen Ihre Besucher die Kriterien für Erlebnisse erfüllen und stellen Sie sicher, dass die zusätzlichen Daten-IDs in den [!DNL Target]- und den [!DNL Analytics]-Aufrufen übereinstimmen.

* **at.js 1.x**: Im  [!DNL Target] Aufruf ist die zusätzliche ID im  `mboxMCSDID` Parameter enthalten. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.
* **at.js 2.x**: Im  [!DNL Target] Aufruf wird die zusätzliche ID im HTTP-Header als Wert für zurückgegeben  `experienceCloud.analytics.supplementalDataId`. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.

Die zusätzliche ID lässt sich am einfachsten mit dem Adobe Experience Platform Debugger überprüfen.

Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

![Debugger](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

Falls im [!DNL Target]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob die Datei [!DNL VisitorAPI.js] vor [!DNL at.js] oder [!DNL mbox.js] geladen wird. Falls im [!DNL Analytics]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob der [!DNL Target]-Aufruf vor dem [!DNL Analytics]-Aufruf erfolgt.

Weitere Informationen finden Sie unter [Analytics für Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) oder wenden Sie sich an den [Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
