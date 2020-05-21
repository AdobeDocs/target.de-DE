---
keywords: analytics for target;a4t;analytics as the reporting source
description: Durch die Verwendung von Analytics als Berichtsquelle für Target (A4T) erhalten Sie Zugriff auf Analytics-Berichte für Ihre Target-Aktivitäten.
title: A4T-Reporting
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 68f356b0711abf9acf7ef631edf3656bd3dd49e3
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 41%

---


# A4T-Reporting{#a-t-reporting}

Using [!DNL Analytics] as your reporting source for [!DNL Target] (A4T) gives you access to [!DNL Analytics] reports for your [!DNL Target] activities.

You can view reports for your activities in both [!DNL Analytics] and [!DNL Target].

For reporting best practices using [!DNL Analytics] for [!DNL Target], [visit this Adobe Spark page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Überblick {#section_035A62D65608423285D8A5A54731E2C5}

Both [!DNL Analytics] and [!DNL Target] reports measure entrants (the people who enter the tests), rather than visitors to the site.

Every time a visitor sees activity content on the page, [!DNL Target] makes a direct server-to-server call to [!DNL Analytics], including which activity and experience the visitor saw. [!DNL Target] wird auch [!DNL Analytics] bei jeder Konvertierung aufgerufen. [!DNL Analytics] fügt die Konversion als spezifisches neues [!DNL Analytics] Ereignis mit dem Namen &quot;Aktivität Conversion&quot;hinzu, das zusammen mit anderen erfassten Daten verfolgt wird [!DNL Analytics].

When the [!UICONTROL Select] operation is used and you sort on *Entrants*, then only experiences that received entrants during the selected time period are displayed in the reports.

>[!NOTE]
>
>Reports powered by [!DNL Target] have a latency of four minutes. For activities powered by A4T, in both the [!DNL Target] and [!DNL Analytics] reports, it can take up to 24 hours after the activity is initially saved before the report data can be broken down by experiences. Die in den ersten 24 Stunden gesammelten Daten sind noch präzise und werden dem richtigen Erlebnis zugewiesen.

## Berichte in Analytics  {#section_F6884872DC864AE7913587FAED4CD11C}

In [!DNL Analytics], click **[!UICONTROL Target]** > **[!UICONTROL Target Activities]** in the left menu. In [!DNL Target], the activity&#39;s reports automatically show [!DNL Analytics] data, metrics, and segments. Daten erscheinen in diesen Berichten ca. eine Stunde nach der Erfassung auf der Site. Sämtliche Metriken, Zielgruppen und Werte in den Berichten stammen aus der Report Suite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

In [!DNL Analytics], use the [!UICONTROL Target Activities] report to view the results of your [!DNL Target] activity. Test&amp;Target (Legacy) Reports provides information about your old Test&amp;Target plug-in style page integrations and does not include [!DNL Analytics] for [!DNL Target] data. In the [!UICONTROL Activities] report, view information about your [!DNL Target] experiences. Klicken Sie auf **[!UICONTROL Metriken]** und wählen Sie dann den Metriktyp **[!UICONTROL Target.]** Für Ihren Bericht stehen zwei Metriken zur Verfügung:

* **Aktivitäten-Einträge:** Entspricht der Anzahl der Teilnehmer im [!DNL Target] Bericht.
* **Aktivitäten-Konversionen:** Entspricht der Nummer der benutzerdefinierten Konvertierung im [!DNL Target] Bericht.

>[!NOTE]
>
>[!DNL Target] Details zu Steigerung und Konfidenz finden Sie auch in [!DNL Analytics]. Weitere Informationen finden Sie unter Steigerung der [Zielgruppe und Vertrauen](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/report-target-lift-confidence.html) im *Analytics-Komponentenhandbuch*.

>[!IMPORTANT]
>
>If your [!UICONTROL Target Activities] report in [!DNL Analytics] lists &quot;unspecified&quot; instead of listing your activities, an update is required to your provisioned account. Wenden Sie sich an den Kundendienst, um dieses Problem zu beheben.

## Berichte in Target  {#section_C0D1F17F88374B6690BF904D7B83B42E}

When [!DNL Analytics] is used as the reporting source, reports in [!DNL Target] show the data gathered from [!DNL Analytics]. The report differs somewhat from other [!DNL Target] reports:

* The [!UICONTROL Audiences] list shows the audiences available to your [!DNL Analytics] report suite.
* The [!UICONTROL Metric] list shows every metric available through [!DNL Analytics].

   Every metric is available, including any custom or calculated metrics that are built-in in [!DNL Analytics].

   Beachten Sie, dass jede Zahl, die erhöht wird, im Bericht als positiv dargestellt wird, auch wenn eine Erhöhung eigentlich unerwünscht ist. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the test has completed. Es ist nicht erforderlich, dass Sie im Vorhinein genau wissen, was Sie messen möchten.

Click to view the full [!DNL Analytics] report directly from the activity report page.

## Berichte in Analysis Workspace {#reports-in-analysis-workspace}

Sie können mithilfe von [!DNL Adobe Analysis Workspace] tiefere Einblicke gewinnen, um die Daten zu visualisieren oder Einblicke zu finden, die unter der Oberfläche verborgen sind.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by [!DNL Adobe Experience League].

## Aktivitätserstellung {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Während der Erstellung einer Aktivität müssen Sie auf der Seite [!UICONTROL Einstellungen] ein spezifisches Ziel für diese Aktivität angeben. Dieses Ziel wird zur Standardmetrik für den Bericht und wird immer als erste Option in der Metrikauswahl aufgeführt. Sie können keine Segmente für die Berichterstellung auswählen, wie Sie es für eine reguläre Target-Aktivität tun würden. Ein Test mit [!DNL Analytics] Segmenten anstelle von [!DNL Adobe Analytics] [!DNL Target] Audiencen.

## Performing offline calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Weitere Informationen dazu finden Sie unter [Durchführen von Offline-Berechnungen für Analytics for Target (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
