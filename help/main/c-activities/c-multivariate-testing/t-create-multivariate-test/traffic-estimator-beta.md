---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Erfahren Sie, wie Sie mit der Traffic-Schätzung wissen, ob Sie über ausreichend Traffic für Ihre - [!DNL Adobe Target] [!UICONTROL Multivariate Test] verfügen, um erfolgreich zu sein.
title: Wie viel Traffic wird für eine [!UICONTROL Multivariate Test] (MVT)-Aktivität benötigt?
feature: Multivariate Tests
hide: true
hidefromtoc: true
source-git-commit: 4805da617962e29794bd3af16138f3887ad250d0
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 21%

---

# Schätzen des für eine erfolgreiche [!UICONTROL Multivariate Test] erforderlichen Traffics

Da ein Multivariater Test mehrere Erlebnisse vergleicht, ist es wichtig zu wissen, wie hoch der erforderliche Traffic ist, um aussagekräftige Ergebnisse zu erzielen. Der [!UICONTROL Traffic Estimator] verwendet Statistiken zu Ihrer Seite und der Anzahl der Erlebnisse, die getestet werden, um die Menge an Traffic und die Testdauer zu schätzen, die für den Erfolg des Tests erforderlich sind.

Die [!UICONTROL Traffic Estimator] sagt den Stichprobenumfang voraus, der erforderlich ist, um Folgendes sicherzustellen:

* 95 % Konfidenz. Diese Statistik bedeutet, dass die Wahrscheinlichkeit, einen falsch positiven Wert zu melden, wenn es keine echte Steigerung gibt, 5 % beträgt (100 % - Konfidenzniveau).
* 80 % statistische Leistung. Diese Statistik bedeutet, dass der Test mit einer Wahrscheinlichkeit von 80 % eine tatsächliche Steigerung von 25 % oder mehr erkennt.
* 25% minimaler zuverlässig detektierbarer Anstieg. [!DNL Target] berechnet den Traffic, der erforderlich ist, um eine 80-prozentige Wahrscheinlichkeit zu haben, eine tatsächliche Steigerung von 25 % oder mehr zu erkennen.

Der Test verwendet die Bonferroni-Korrektur zur Korrektur von Mehrfachvergleichen. Diese Methode gilt als konservativ, was durch Erzwingen eines relativ hohen Wertes für die zuverlässig bestimmbare Mindeststeigerung kompensiert wird.

Die [!UICONTROL Traffic Estimator] bietet außerdem Feedback, mit dem Sie wissen, ob Sie über ausreichend Traffic für den Test verfügen, den Sie erfolgreich durchführen möchten.

1. Klicken Sie auf der [!UICONTROL Experiences] der [!UICONTROL Visual Experience Composer] in einer [!UICONTROL Multivariate] auf das **[!UICONTROL Traffic]**-Symbol ( ![Traffic-](/help/main/assets/icons/Gauge2.svg)) oben links auf der [!UICONTROL Experiences].

   Die [!UICONTROL Traffic Estimator] wird geöffnet.

   ![Benutzeroberfläche der Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   Sie können erneut auf das Symbol klicken, um die [!UICONTROL Traffic Estimator] auszublenden.

   Im oberen Bereich der [!UICONTROL Traffic Estimator] werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

1. (Bedingt) Geben Sie die typische Konversionsrate, die geschätzten Besucher pro Tag und die Testdauer an.

   * **[!UICONTROL Number of Content Combinations]**: Wird automatisch berechnet, basierend auf der Anzahl der Erlebnisse, die im Rahmen Ihrer Aktivität nach einem Ausschluss erstellt werden.
   * **[!UICONTROL Typical Conversion Rate]**: Die Konversionsrate wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem.
   * **[!UICONTROL Estimated Visitors Per Day]**: Dies ist die Anzahl der Besucherinnen und Besucher, die diese Seite anhand der Zielgruppenbestimmungskriterien wahrscheinlich anzeigen werden. Dies kann auf Ihren Analytics-Daten basieren.
   * **[!UICONTROL Test Duration]**: Die Anzahl der Tage, die die Aktivität ausgeführt werden soll.

   Der [!UICONTROL Traffic Estimator] verwendet diese Statistiken, um zu bestimmen, welche Anpassungen für die Ausführung eines erfolgreichen Tests erforderlich sind.

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie beispielsweise viele Erlebnisse testen und Ihre Konversionsrate und Impressions zu niedrig sind, zeigt die [!UICONTROL Traffic Estimator] an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic gering ist, kann der [!UICONTROL Traffic Estimator] eine niedrigere Anzahl von Erlebnissen vorschlagen, sodass Sie den Test die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, können Sie eine oder beide der folgenden Maßnahmen ergreifen:

   * Reduzieren Sie die Anzahl der Angebotskombinationen sowie die Anzahl der Orte.
   * Verlängern der Testdauer.

   Passen Sie die Zahlen an, bis die [!UICONTROL Traffic Estimator] anzeigt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.
