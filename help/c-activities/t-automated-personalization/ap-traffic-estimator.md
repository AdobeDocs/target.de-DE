---
keywords: traffic estimator;automated personalization;ap
description: Die Traffic-Schätzung liefert Feedback, aus dem hervorgeht, ob Sie über ausreichend Traffic verfügen, damit Ihre Adobe Target-Aktivität erfolgreich sein kann.
title: Schätzen des für einen erfolgreichen Test erforderlichen Traffics
feature: ap
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
translation-type: tm+mt
source-git-commit: fec7708ddb17ec5565bd3c5f00f0490c03ec0140
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 27%

---


# ![PREMIUM](/help/assets/premium.png) Schätzen des für einen erfolgreichen Test erforderlichen Traffics{#estimate-the-traffic-required-for-success}

The [!UICONTROL Traffic Estimator] provides feedback that lets you know whether you have sufficient traffic for your [!DNL Adobe Target] activity to succeed.

Because an [!UICONTROL Automated Personalization] activity uses multiple offer combinations, it is important to know how much traffic is required to provide meaningful results. The [!UICONTROL Traffic Estimator] uses statistics about your page and the number of experiences being tested to estimate the amount of traffic and the test duration needed to make the activity successful.

The [!UICONTROL Traffic Estimator] determines if there is enough traffic to generate personalized models, by comparing the estimated page impressions and typical conversion rate for the pages. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dies bietet ausreichend Zeit, um personalisierten Inhalt zu erhalten und zu verstehen, welcher Inhalt bereitgestellt werden sollte.

Remember that [!DNL Target] randomly serves experiences until the personalization algorithms are built. The checkmark icon beside each offer shows when the model for that offer is ready and [!DNL Target] is able to begin delivering personalized content. Da eine Steigerung erst erwartet wird, wenn die Modelle fertig sind, können Sie anhand der visuellen Angabe die richtige Erwartung festlegen. Use the [!UICONTROL Traffic Estimator] in the [!UICONTROL Visual Experience Composer] (VEC) to get a guideline of when the models will be ready.

## Traffic-Schätzung verwenden

1. From the [!UICONTROL Visual Experience Composer], click **[!UICONTROL Traffic]**.

   ![Traffic-Symbol](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   The [!UICONTROL Traffic Estimator] opens. Sie können erneut auf **[!UICONTROL Traffic]**[!UICONTROL  klicken, um die Traffic-Schätzung auszublenden].

   ![](assets/ap_est.png)

1. Geben Sie die typische Konversionsrate (oder die Konversionsrate, die Sie von dieser Aktivität erwarten), die geschätzten Aktivitätsimpressionen pro Tag und die Testdauer an.

   * **Anzahl der Angebot**: Wird automatisch basierend auf der Anzahl der Erlebnisse berechnet, die als Teil Ihrer Aktivität nach Ausschlüssen erstellt werden.
   * **Typische Konversionsrate**: Die Konversionsrate wird als Prozentsatz ausgedrückt und basiert auf Ihrer Schätzung oder auf historischen Daten aus Ihrem Analysesystem.
   * **Geschätzte Besuche pro Tag**: Dies ist die Anzahl der Besuche pro Tag von Besuchern, die die Aktivität auf der Grundlage der Targeting-Kriterien Ansicht haben. Dies kann auf Ihren Analytics-Daten basieren. Beachten Sie, dass es sich bei dieser Zahl um Besuche und nicht um Unique Visitors handeln sollte.
   * **Testdauer**: Die Anzahl der Tage, während derer die Aktivität ausgeführt werden soll.

   The [!UICONTROL Traffic Estimato]r uses these statistics to determine what adjustments are needed to run a successful test.

   Near the top of the [!UICONTROL Traffic Estimator], the values you entered are calculated and the results are shown.

   ![](assets/ap_est_no.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. For example, if you are testing a large number of combinations and your conversion rate and impressions are too low, the [!UICONTROL Traffic Estimator] shows how long the test will need to run to be successful. Or, if your traffic is low, the [!UICONTROL Traffic Estimator] might suggest a lower number of offer combinations so you can run the test the desired number of days.

   Wenn Sie nicht über ausreichend Traffic verfügen, können Sie eine oder alle der folgenden Maßnahmen ergreifen:

   * Consider using an [Auto-Target](/help/c-activities/auto-target-to-optimize.md) activity instead of [!UICONTROL Automated Personalization] to create experiences with several offer changes in one experience variation.
   * Reduce the number of offer combinations within your [!UICONTROL Automated Personalization] activity.
   * Erhöhen Sie die Dauer der Aktivität.

   Adjust the numbers until the [!UICONTROL Traffic Estimator] says you have sufficient traffic, then design your test accordingly.

   ![](assets/ap_est_yes.png)

   If the traffic is sufficient, the [!UICONTROL Traffic] icon shows a green check. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.

## Häufig gestellte Fragen zur Traffic-Schätzung

Beachten Sie bei der Arbeit mit der [!UICONTROL Traffic-Schätzung]die folgenden häufig gestellten Fragen:

### Warum werden [!DNL Target] keine personalisierten Modelle erstellt, wenn meine AP-Aktivität über ausreichend Traffic verfügt?

Unter bestimmten Umständen kann Ihr Traffic groß genug sein, um ein personalisiertes Modell zu erstellen, aber dieser Traffic kann darauf hinweisen, [!DNL Target] dass es keinen bedeutenden Unterschied zwischen dem personalisierten Modell und dem Zufallsprinzip gibt. Obwohl das Modell integriert [!DNL Target] und getestet wurde, wird es nicht bereitgestellt, da das Modell nicht wesentlich besser als zufällig ist.

Ein möglicher Grund dafür, dass das Modell nicht besser als zufällig ist, könnte sein, dass sich die Angebot nicht wesentlich voneinander unterscheiden. In diesem Fall können Sie versuchen, die Unterschiede in den Angeboten zu vergrößern, indem Sie sie visueller anders gestalten oder den Inhalt selbst ändern.
