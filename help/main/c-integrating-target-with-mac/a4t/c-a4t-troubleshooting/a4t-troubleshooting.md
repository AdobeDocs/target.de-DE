---
keywords: Analytics-Trackingserver;A4T;Analytics-Segmente;Report Suites;falsche Daten;verwaist;sdid;VisitorAPI.js;mboxMCSDID;Phantom;Unspecified
description: Erfahren Sie mehr über häufige Probleme bei der Verwendung von Analytics für  [!DNL Target]  (A4T).
title: Fehlerbehebung bei der Analytics- und  [!DNL Target] -Integration (A4T)
feature: Analytics for Target (A4T)
exl-id: 7d155cbe-e799-43b5-afc2-1aea43f432ba
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 88%

---

# Fehlerbehebung bei der Analytics- und [!DNL Target]-Integration (A4T)

In diesem Abschnitt werden einige allgemeine Probleme behandelt, die auftreten, wenn [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) verwendet wird.

## Aktivitäten weisen keine Daten in Analytics auf, werden jedoch stattdessen als „Unspecified“ aufgeführt. {#unspecified}

Es gibt verschiedene Gründe, warum Daten als „Unspecified“ angezeigt werden:

* Die Classification in [!DNL Target] wurde noch nicht vollständig verarbeitet.

  Die Classification von Berichten dauert normalerweise nach dem ersten Speichern zwischen 24 und 72 Stunden.

* Die Report Suite enthält in diesem Zeitraum keine Daten, [!DNL Target] versucht jedoch, Treffer zu klassifizieren. [!DNL Target] kann Daten so lange nicht klassifizieren, bis ein erster Treffer registriert wird.

  Stellen Sie sicher, dass in der Report Suite mindestens ein Treffer registriert wurde.

* Der Classification-Aufruf von [!DNL Target] an [!DNL Analytics] ist fehlgeschlagen.

  [Wenden Sie sich für Unterstützung an den Kundendienst](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

Wenn Sie die Zeile „Unspecified“ mit der Dimension „Analytics for Target“ aufschlüsseln und sie keine Aktivitäts-IDs enthält, bedeutet dies, dass alles ordnungsgemäß klassifiziert wurde. Wenn dort Aktivitäts-IDs aufgelistet sind, ist dies ein Hinweis für ein Classification-Problem.

>[!NOTE]
>
>Manchmal werden Daten korrekt in Berichten angezeigt, dann jedoch erneut als „Unspezifiziert“ gekennzeichnet, da eine neue Aktivität hinzugefügt wurde, deren Klassifizierung noch nicht abgeschlossen ist. Beachten Sie, dass die Klassifizierung von Berichten nach dem ersten Speichern normalerweise zwischen 24 und 72 Stunden dauert.
>
>Daten, die als „unspezifisch“ eingestuft werden, gehen nicht verloren. Die Daten werden nach erfolgreicher Classification den entsprechenden Aktivitäten oder Erlebnissen zugeordnet.

## A4T-Aktivitätsberichte enthalten eine Zeile mit vielen „Unspecified“ Ereignissen. {#added_unspecified_events}

Abhängig von der Metrik, mit der Sie Ihre Daten anzeigen, kann Ihr Bericht eine Ereigniszeile aufweisen, in der &quot;[!UICONTROL Unspecified]&quot; angezeigt wird.

In der Regel wird diese Zeile angezeigt, wenn Sie eine allgemeine Metrik im Bericht auswählen, die nicht [!DNL Target] ist (z. B. [!UICONTROL Page Views], [!UICONTROL Visits], [!UICONTROL Unique Visitors] usw.). In diesem Fall enthält die [!UICONTROL "Unspecified"] alle [!UICONTROL Page Views], [!UICONTROL Visits] und [!UICONTROL Unique Visitors], die nicht mit [!DNL Target] Aktivitäten verbunden sind.

Diese Zeile enthält dann keine [!DNL Target]-zugehörigen Informationen (z. B. keine Besuchende, Besuche oder Impressionen). Weitere Informationen finden Sie unter [„Unspezifiziert“, „Keine“, „Andere“ und „Nicht bekannt“ in Berichten](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=de) in den *Technotes zu Analytics*.

Wenn Sie im Bericht eine [!DNL Target] Metrik auswählen, wird diese [!UICONTROL "Unspecified"] nicht angezeigt. Die einzige Möglichkeit, dies im Bericht ganz zu vermeiden, besteht darin, für jede von dieser Seite gesendete Anfrage einen [!DNL Target]-Aufruf einzurichten, was weder üblich noch erforderlich ist.

## Die geschätzte Steigerung der Umsatzmetriken zeigt keine korrekten Daten. {#section_35D766E5E4D347C39E15D08AA883FBB0}

Steigerungs- und Vertrauensdaten sind in Analytics nicht verfügbar. Sie stehen jedoch in den Target-Berichten zur Verfügung.

## Aktivitäten erscheinen nicht in Analytics-Berichten.  {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Für A4T-Aktivitäten ist ein Trackingserver erforderlich, der zuvor festgelegt werden muss. Siehe [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) um sicherzustellen, dass Ihr Analytics-Tracking-Server ordnungsgemäß eingerichtet ist.

>[!NOTE]
>
>Bei Verwendung von at.js Version 0.9.1 (oder höher) müssen Sie bei der Erstellung einer Aktivität keinen Tracking-Server angeben. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Goals & Settings] leer lassen.

## Meine Analytics-Segmente werden nicht in Target angezeigt.  {#section_DEE87F1557834F448E99381D3D02EEEF}

Vergewissern Sie sich, dass Sie die entsprechenden Berechtigungen haben, bevor Sie A4T-Aktivitäten erstellen:

* Sie müssen zur Zugriffsgruppe für Webservices in Adobe Analytics gehören, um Analytics als Berichtsquelle für Target nutzen zu können
* Sie müssen Mitglied in mindestens einer Experience Cloud-Gruppe sein, die Zugriff auf Analytics und Target hat.
* Überprüfen Sie, ob Analytics und Target im Abschnitt Marketing-Apps in der linken Navigation angezeigt wird.

## Absprungraten, Absprünge und Ausstiegsmetriken erscheinen in Berichten als positiv.  {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Diese Metriken, die in Berichten als positiv erscheinen, sind ein bekanntes Problem.

Obwohl diese Metriken negativ sind, wird die Steigerung in den Target-Berichten als positiv gezeigt. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

## Die benötigte Report Suite wird nicht angezeigt. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

Die Liste der Report Suites, die in  angezeigt wird, ist die Liste der Report Suites, die für  als Berichtsquelle für  konfiguriert wurden.--Die Liste der Report Suites, die in [!DNL Target Standard/Premium] angezeigt wird, ist die Liste der Report Suites, die für [!DNL Analytics] als Berichtsquelle für [!DNL Target] (A4T) konfiguriert wurden. Möglicherweise sehen Sie nicht alle Report Suites, die Sie besitzen.

Wenn Sie mehrere Berichtsquellen verwenden, müssen die Report Suites in der standardmäßigen Berichtsquelle vorhanden sein, die auch in [!DNL Target] eingestellt ist. Wenn sich die Report Suites nicht in der Standard-Berichtsquelle befinden, werden die Report Suites nicht angezeigt.

Wenn Sie die Report Suite, nach der Sie suchen, nicht sehen, sollten Sie den [Kundendienst](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) kontaktieren und sie aktivieren lassen.

## In meinen Berichten sind weniger Daten vorhanden als erwartet. {#section_75002584FA63456D8D9086172925DD8D}

Überprüfen Sie Ihre Implementierung, insbesondere auf Seiten, auf denen Ihre Besucher die Kriterien für Erlebnisse erfüllen und stellen Sie sicher, dass die zusätzlichen Daten-IDs in den [!DNL Target]- und den [!DNL Analytics]-Aufrufen übereinstimmen.

* **at.js 1.x**: Im [!DNL Target]-Aufruf ist die zusätzliche ID im Parameter `mboxMCSDID` enthalten. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.
* **at.js 2.x**: Im [!DNL Target]-Aufruf wird die zusätzliche ID in der HTTP-Kopfzeile als der Wert für `experienceCloud.analytics.supplementalDataId` zurückgegeben. Im [!DNL Analytics]-Aufruf ist die zusätzliche ID im Parameter `sdid` enthalten.

Die einfachste Möglichkeit, die zusätzliche ID zu prüfen, besteht in der Verwendung von Adobe Experience Platform Debugger.

Wenn Sie Debugger nicht installiert haben, finden Sie weitere Informationen unter [Einführung in Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html?lang=de).

![Debugger](/help/main/c-integrating-target-with-mac/a4t/assets/debugger.png)

Falls im [!DNL Target]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob die Datei [!DNL VisitorAPI.js] vor [!DNL at.js] geladen wird. Falls im [!DNL Analytics]-Aufruf keine zusätzliche Daten-ID enthalten ist, prüfen Sie, ob der [!DNL Target]-Aufruf vor dem [!DNL Analytics]-Aufruf erfolgt.

Weitere Informationen finden Sie unter [Analytics for Target-Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) oder wenden Sie sich an den [Kundendienst](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
