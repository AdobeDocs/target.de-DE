---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: Sie können eine Aktivität in Target Standard/Premium erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
title: Aktivitätserstellung
feature: a4t general
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
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

   You are required to select a success metric to use as a goal for each activity. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. You can choose any [!DNL Analytics] metric available in the [!DNL Analytics] metric selector.

   >[!NOTE]
   >
   >You can send a custom Target-based metric to [!DNL Analytics] rather than relying only on [!DNL Analytics] data. For example, you can monitor clicking on a page, which is usually not tracked by [!DNL Analytics]. This custom metric is sent to [!DNL Analytics] automatically from the [!DNL Target] server, and appears as the &quot;[!DNL Target] Conversion&quot; metric in the metrics selector in [!DNL Analytics]. The [!DNL Target] Conversion metric is empty if you choose to use [!DNL Analytics] metrics.

   Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch die Aktivität verbessern möchten.

   Der Besucher bleibt nach Erreichen des Ziels in der Aktivität. Der Besucher sieht weiterhin den Aktivitätsinhalt, wird jedoch nicht als neuer Aktivitätseintrag gezählt.

   >[!NOTE]
   >
   >When setting up an activity after setting up [!DNL Analytics] as your reporting source, there is no option to set up audiences for reporting. [!DNL Analytics] Segmente sind im Bericht [!DNL Target] Aktivitäten verfügbar.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Unterstützung von Analytics for Zielgruppe (A4T) für Aktivitäten mit automatisierter Zuordnung {#a4t-aa}

Die Adobe Target-zu-Adobe Analytics-Integration, die als [Analytics for Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md)bezeichnet wird, wurde aktualisiert.

[!UICONTROL Aktivitäten mit automatisierter Zuordnung] unterstützen jetzt [!UICONTROL Analytics für die Zielgruppe]. Mit dieser Integration können Sie die Multi-Armed Bandit-Funktion der automatischen Zuordnung verwenden, um Traffic zu erfolgreichsten Erlebnissen zu verhelfen, während Sie eine [!DNL Adobe Analytics] [!DNL Adobe Analytics] Zielmetrik und/oder Funktionen für Berichte und Analyse verwenden. Wenn Sie A4T bereits für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten [](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)implementiert haben, können Sie loslegen!

Erster Schritt:

1. Erstellen Sie eine A/B-Test-Aktivität und wählen Sie **[!UICONTROL Automatisch dem besten Erlebnis]** zuordnen wie die **[!UICONTROL Traffic-Zuordnungsmethode]** auf der [!UICONTROL Targeting] -Seite.
1. Wählen Sie auf der Seite &quot; **[!UICONTROL Ziele und Einstellungen]** &quot; **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichte-Quelle]** aus und wählen Sie die Report Suite aus, die Ihrem Optimierungsziel entspricht.
1. Wählen Sie eine Metrik für das Primär-Ziel.

   Wählen Sie die **[!UICONTROL Konvertierung]** aus, [!DNL Adobe Target] um das Optimierungsziel festzulegen.

   Oder

   Choose **[!UICONTROL Use an Analytics metric]** and then select a metric from [!DNL Analytics] for use as the optimization goal. You can use an out-of-box [!DNL Analytics] conversion metric, or an [!DNL Analytics] custom event.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Die automatisierte Zuordnung] verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität und bringt Besucher zum Erlebnis, das Ihre Zielmetrik maximiert.

1. Verwenden Sie die Registerkarte &quot; **[!UICONTROL Berichte]** &quot;, um den Berichte Ihrer Aktivität anhand Ihrer [!DNL Adobe Analytics] Metriken Ansicht. Klicken Sie in Analytics **[!UICONTROL auf]** Ansicht, um tief greifende Daten zu segmentieren und Ihre Berichte weiter zu segmentieren.

### Unterstützte Zielmetriken

Mit A4T für die [!UICONTROL automatische Zuordnung] können Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung auswählen:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

A4T for [!UICONTROL Auto-Allocate] requires you to choose a metric that is based on a binomial event, that is, an event that either does or does not happen, for example a click, a conversion, an order, etc. (These types of events are also sometimes referred to as Bernoulli, binary, or discrete events.)

A4T for [!UICONTROL Auto-Allocate] does not support optimization for continuous metrics such as revenue, number of products ordered, session duration, number of page views in session, etc. (These unsupported types of metrics are also sometimes referred to as non-binomial or non-Bernoulli metrics.)

The following metric types are unsupported as primary goal metrics:

* [!DNL Adobe Target] engagement and revenue metrics
* [!DNL Adobe Analytics] engagement and revenue metrics

   >[!NOTE]
   >
   >It might be possible to select [!DNL Analytics] engagement and revenue metrics as your primary goal metric because [!DNL Target] cannot identify all engagement and revenue metrics from [!DNL Analytics]. Gehen Sie vorsichtig vor, um nur binomielle Konversionsmetriken oder benutzerdefinierte Ereignis aus [!DNL Analytics]auszuwählen.

* Adobe Analytics calculated metrics

### Limitations and notes

* The reporting source cannot be changed from [!DNL Analytics] to [!DNL Target] or vice versa once an activity has been activated.
* Although calculated metrics are not supported as primary goal metrics, it is often possible to achieve the intended result by instead selecting a custom event as the primary goal metric. Wenn Sie z. B. eine Metrik wie &quot;Formularabschlüsse pro Besucher&quot;optimieren möchten, wählen Sie ein benutzerdefiniertes Ereignis, das &quot;Formularabschlüsse&quot;als primäre Zielmetrik entspricht. [!DNL Target] automatically normalizes conversion metrics on a per-visit basis to account for uneven traffic distribution, so it is not necessary to use a calculated metric to perform normalization.
* [!DNL Target] verwendet das Zuordnungsmodell &quot;Gleich Touch&quot;in der A4T-Implementierung für die automatische Zuordnung.

Weitere Informationen finden Sie unter Übersicht über die [Zuordnung](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html) im Handbuch *Analytics-Tools*.
