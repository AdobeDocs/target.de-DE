---
keywords: analytics tracking server;A4T;analytics segments;report suites;incorrect data;orphaned;sdid;VisitorAPI.js;mboxMCSDID;phantom;unspecified
description: In diesem Thema werden einige allgemeine Probleme behandelt, die auftreten, wenn Analytics als Berichtsquelle für Target (A4T) verwendet wird.
title: Fehlerbehebung bei der Analytics- und Target-Integration (A4T)
feature: a4t troubleshooting
subtopic: Multivariate Test
topic: Standard
uuid: a5aa3be5-68a2-4f12-8226-f32a76136bbd
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 80%

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

>[!NOTE]
>
>Manchmal werden Daten korrekt in Berichten angezeigt, dann jedoch erneut als „unspezifisch“ gekennzeichnet, da eine neue Aktivität hinzugefügt wurde, deren Classification noch nicht abgeschlossen wurde. Beachten Sie, dass die Klassifizierung von Berichten nach dem ersten Speichern normalerweise zwischen 24 und 72 Stunden dauert.
>
>Daten, die als „unspezifisch“ eingestuft werden, gehen nicht verloren. Die Daten werden nach erfolgreicher Classification den entsprechenden Aktivitäten oder Erlebnissen zugeordnet.

## In meinen Analytics-Daten tauchen zu hohe Besucherzahlen auf, seit ich A4T verwende.  {#section_4BE374E573D44FB7918611699B74F58E}

Weitere Informationen finden Sie unter [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Die geschätzte Steigerung der Umsatzmetriken zeigt keine korrekten Daten. {#section_35D766E5E4D347C39E15D08AA883FBB0}

Steigerungs- und Vertrauensdaten sind in Analytics nicht verfügbar. Sie stehen jedoch in den Target-Berichten zur Verfügung.

## Aktivitäten erscheinen nicht in Analytics-Berichten.  {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Für A4T-Aktivitäten ist ein Trackingserver erforderlich, der zuvor festgelegt werden muss. Weitere Informationen zu diesem Thema finden Sie unter [Verwenden eines Analytics-Trackingservers](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) zur Überprüfung der korrekten Einrichtung Ihres Analytics-Trackingservers.

>[!NOTE]
>
>Sollten Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität und bei der Verwendung von mbox.js Version 61 (oder neuer) oder at.js Version 0.9.1 (oder neuer) keinen Trackingserver angeben. Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

## Meine Analytics-Segmente werden nicht in Target angezeigt.  {#section_DEE87F1557834F448E99381D3D02EEEF}

Vergewissern Sie sich, dass Sie entsprechende Berechtigungen haben, bevor Sie A4T-Aktivitäten erstellen:

* Sie müssen zur Zugriffsgruppe für Webdienste in Adobe Analytics gehören, um Analytics als Berichtsquelle für Target nutzen zu können.
* Sie müssen Mitglied in mindestens einer Experience Cloud-Gruppe sein, die Zugriff auf Analytics und Target hat.
* Überprüfen Sie, ob Analytics und Target im Abschnitt Marketing-Apps in der linken Navigation angezeigt wird.

## Absprungraten, Absprünge und Ausstiegsmetriken erscheinen in Berichten als positiv.  {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Dieses Problem ist bekannt.

Obwohl diese Metriken negativ sind, wird die Steigerung in den Target-Berichten als positiv gezeigt. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

## The report suite I need does not display. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

The list of report suites that appears in [!DNL Target Standard/Premium] is the list of report suites that have been configured for [!DNL Analytics] as the reporting source for [!DNL Target] (A4T). Das bedeutet, dass Sie möglicherweise nicht alle vorhandenen Report Suites sehen.

Wenn Sie außerdem mehrere Berichte-Quellen verwenden, müssen die Report Suites [!DNL Target] auch im Standardquellensatz des Berichte vorhanden sein. Andernfalls werden die Report Suites nicht angezeigt.

If you still don&#39;t see the report suite you are looking for, contact [Client Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to get it enabled.

## In meinen Berichten sind weniger Daten vorhanden als erwartet. {#section_75002584FA63456D8D9086172925DD8D}

Überprüfen Sie Ihre Implementierung, insbesondere auf Seiten, auf denen Ihre Besucher die Kriterien für Erlebnisse erfüllen und stellen Sie sicher, dass die zusätzlichen Daten-IDs in den [!DNL Target]- und den [!DNL Analytics]-Aufrufen übereinstimmen.

* **at.js 1.x**: Im [!DNL Target] Aufruf ist die zusätzliche ID im Parameter enthalten `mboxMCSDID` . Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.
* **at.js 2.x**: Im [!DNL Target] Aufruf wird die zusätzliche ID im HTTP-Header als Wert für zurückgegeben `experienceCloud.analytics.supplementalDataId`. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.

Die zusätzliche ID lässt sich am einfachsten mit dem Adobe Experience Platform Debugger überprüfen.

Wenn Sie den Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in den Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

![Debugger](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

Falls im [!DNL Target]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob die Datei [!DNL VisitorAPI.js] vor [!DNL at.js] oder [!DNL mbox.js] geladen wird. Falls im [!DNL Analytics]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob der [!DNL Target]-Aufruf vor dem [!DNL Analytics]-Aufruf erfolgt.

Weitere Informationen finden Sie unter [Analytics für Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) oder wenden Sie sich an den [Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
