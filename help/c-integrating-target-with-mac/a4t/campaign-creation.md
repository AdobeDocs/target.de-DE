---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: Sie können eine Aktivität in Target Standard/Premium erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
title: Aktivitätserstellung
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: cbab5b34475b279cf3c58530665f096943ecbf95
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 22%

---


# Aktivitätserstellung{#activity-creation}

You can configure an activity in [!DNL Target] to use [!DNL Adobe Analytics] as the reporting source (A4T).

Before you set up an activity that uses [!DNL Analytics] as the reporting source, establish the goal for the activity, such as improving revenue per visitor (RPV) or increasing clicks on your shopping cart. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Although you can select additional metrics at any time in [!DNL Analytics], you must still specify a particular metric you expect this test to affect.

## Erstellen einer Aktivität, die Analytics als Berichte-Quelle verwendet

Creating a [!DNL Target] activity that uses [!DNL Analytics] as the reporting source is similar to setting up a regular [!DNL Target] activity, with a few important differences. For example, you cannot select a segment for reporting while creating the activity because all segments available in [!DNL Analytics] can be applied when viewing a report.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >An activity name cannot include the &quot;%&quot; character if [!DNL Analytics] is used as the reporting source.

1. Wählen Sie den Aktivitätstyp aus und beginnen Sie mit der Einrichtung der Aktivität.
1. Wählen Sie in den **[!UICONTROL Einstellungen]** für die Aktivität **[!UICONTROL Adobe Analytics]** aus und geben Sie Ihr Unternehmen an.
1. Wählen Sie eine Report Suite aus.

   You can choose any report suite that is available to you in [!DNL Analytics]. Die Report Suite definiert, wo die erfassten Daten verfügbar sind. Virtuelle Report Suites werden nicht in der Liste der Report Suites aufgeführt.

   Beim Auswählen der Report Suite kann es vorkommen, dass Ihnen zwei Fehler gemeldet werden:

   * Sie erhalten die Fehlermeldung, dass keine Report Suites verfügbar sind, obwohl Ihr Konto korrekt eingerichtet ist.

      You might need to check your [!DNL Analytics] company. If your [!DNL Adobe Experience Cloud] account is tied to more than one [!DNL Analytics] company, log out of [!DNL Target], and log in to [!DNL Analytics] under the right company. Then return to [!DNL Target], and the report suites will load.

   * Ihnen wird nicht die Report Suite angezeigt, die Sie erwartet haben.

      Only report suites that are provisioned to connect to [!DNL Target] will be available for selection. If you don&#39;t see the report suite(s) you expect, first try logging out and logging back in to the [!DNL Adobe Experience Cloud] to try again.
   Wenn die Report Suite(s) weiterhin nicht in der Liste zu finden ist/sind, [wenden Sie sich an den Kundendienst](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Legen Sie den Trackingserver fest.

   Siehe [Verwenden eines Analytics-Tracking-Servers](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definieren Sie das Erlebnis.
1. Legen Sie das Aktivitätsziel fest.

   Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

   >[!NOTE]
   >
   >You can send a custom Target-based metric to [!DNL Analytics] rather than relying only on [!DNL Analytics] data. For example, you can monitor clicking on a page, which is usually not tracked by [!DNL Analytics]. This custom metric is sent to [!DNL Analytics] automatically from the [!DNL Target] server, and appears as the &quot;[!DNL Target] Conversion&quot; metric in the metrics selector in [!DNL Analytics]. The [!DNL Target] Conversion metric is empty if you choose to use [!DNL Analytics] metrics.

   Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch die Aktivität verbessern möchten.

   Der Besucher bleibt nach Erreichen des Ziels in der Aktivität. Der Besucher sieht weiterhin den Aktivitätsinhalt, wird jedoch nicht als neuer Aktivitätseintrag gezählt.

   >[!NOTE]
   >
   >When setting up an activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] Segmente sind im Bericht [!DNL Target] Aktivitäten verfügbar.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Analytics für Target (A4T)-Unterstützung für Aktivitäten mit automatisierter Zuordnung {#a4t-aa}

Wir haben die Analytics-Integration von Adobe Target zu Adobe aktualisiert, die als [Analytics zum Target](/help/c-integrating-target-with-mac/a4t/a4t.md)bezeichnet wird.

[!UICONTROL Aktivitäten mit automatisierter Zuordnung] unterstützen jetzt [!UICONTROL Analytics zum Target]. Mit dieser Integration können Sie die Multi-Armed Bandit-Funktion der automatischen Zuordnung verwenden, um Traffic zu erfolgreichsten Erlebnissen zu verhelfen, während Sie eine [!DNL Adobe Analytics] [!DNL Adobe Analytics] Zielmetrik und/oder Funktionen für Berichte und Analyse verwenden. Wenn Sie A4T bereits für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten [](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)implementiert haben, können Sie loslegen!

Erster Schritt:

1. Erstellen Sie eine A/B-Test-Aktivität und wählen Sie **[!UICONTROL Automatisch dem besten Erlebnis]** zuordnen wie die **[!UICONTROL Traffic-Zuordnungsmethode]** auf der [!UICONTROL Targeting] -Seite.
1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichte-Quelle]** auf der Seite &quot; **[!UICONTROL Ziele und Einstellungen]** &quot;und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.
1. Wählen Sie eine Metrik für das Primär-Ziel.

   Wählen Sie die **[!UICONTROL Konvertierung]** aus, [!DNL Adobe Target] um das Optimierungsziel festzulegen.

   Oder

   Wählen Sie &quot; **[!UICONTROL Eine Analytics-Metrik]** verwenden&quot;und wählen Sie dann eine Metrik aus, die als Optimierungsziel verwendet werden [!DNL Analytics] soll. Sie können eine vordefinierte [!DNL Analytics] Konversionsmetrik oder ein [!DNL Analytics] benutzerdefiniertes Ereignis verwenden.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Die automatisierte Zuordnung] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität und bringt Besucher zum Erlebnis, das Ihre Zielmetrik maximiert.

1. Verwenden Sie die Registerkarte &quot; **[!UICONTROL Berichte]** &quot;, um den Berichte Ihrer Aktivität anhand Ihrer [!DNL Adobe Analytics] Metriken Ansicht. Klicken Sie auf **[!UICONTROL Ansicht in Analytics]** , um tief in Ihre Berichte-Daten einzutauchen und sie weiter zu segmentieren.

### Unterstützte Zielmetriken

Mit A4T für die [!UICONTROL automatische Zuordnung] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

A4T für die [!UICONTROL automatische Zuordnung] erfordert die Auswahl einer Metrik, die auf einem binomialen Ereignis basiert, d. h. einem Ereignis, das entweder geschieht oder nicht, z. B. einem Klick, einer Konversion, einer Bestellung usw. (Diese Ereignisse werden manchmal auch als Bernoulli-, Binär- oder diskrete Ereignis bezeichnet.)

A4T für die [!UICONTROL automatische Zuordnung] unterstützt keine Optimierung für kontinuierliche Metriken wie Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Ansichten während der Sitzung usw. (Diese nicht unterstützten Metriktypen werden manchmal auch als nicht-binomielle oder nicht-Bernoulli-Metriken bezeichnet.)

Die folgenden Metriktypen werden nicht als primäre Zielmetriken unterstützt:

* [!DNL Adobe Target] Interaktions- und Umsatzmetriken
* [!DNL Adobe Analytics] Interaktions- und Umsatzmetriken

   >[!NOTE]
   >
   >Es ist möglicherweise möglich, Interaktions- und Umsatzmetriken als primäre Zielmetrik auszuwählen, da [!DNL Analytics] nicht alle Interaktions- und Umsatzmetriken identifiziert werden können [!DNL Target] [!DNL Analytics]. Gehen Sie vorsichtig vor, um nur binomielle Konversionsmetriken oder benutzerdefinierte Ereignis aus [!DNL Analytics]auszuwählen.

* Berechnete Adobe Analytics-Metriken

### Einschränkungen und Hinweise

* Die Berichte-Quelle kann nicht von [!DNL Analytics] zu [!DNL Target] oder umgekehrt geändert werden, sobald eine Aktivität aktiviert wurde.
* Obwohl errechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das angestrebte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerdefiniertes Ereignis als primäre Zielmetrik auswählen. Wenn Sie z. B. eine Metrik wie &quot;Formularabschlüsse pro Besucher&quot;optimieren möchten, wählen Sie ein benutzerdefiniertes Ereignis, das &quot;Formularabschlüsse&quot;als primäre Zielmetrik entspricht. [!DNL Target] normalisiert Konversionsmetriken automatisch pro Besuch, um eine ungleiche Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik für die Normalisierung zu verwenden.
* [!DNL Target] verwendet das Zuordnungsmodell &quot;Gleich Touch&quot;in der A4T-Implementierung für die automatische Zuordnung.

Weitere Informationen finden Sie unter Übersicht über die [Zuordnung](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) im Handbuch *Analytics Tools*.
