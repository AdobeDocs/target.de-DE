---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Erfahren Sie, wie Sie mit der Traffic-Schätzung wissen, ob Sie über ausreichend Traffic für eine erfolgreiche Aktivität  [!DNL Adobe Target] [!UICONTROL &#x200B; Multivarianz]Test verfügen.
title: Wie viel Traffic wird für eine Aktivität des Typs [!UICONTROL Multivariater Test] (MVT) benötigt?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
TQID: https://experienceleague.adobe.com/XHBXV7Jtvp87ve4NTd-016E2dFkHTbPu-8-nY8GE-VM
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 530
ht-degree: 19%

---

# Schätzen des für eine erfolgreiche Aktivität [!UICONTROL Multivarianz-Test] erforderlichen Traffics

Da ein Multivariater Test mehrere Erlebnisse vergleicht, ist es wichtig zu wissen, wie hoch der erforderliche Traffic ist, um aussagekräftige Ergebnisse zu erzielen. Die [!UICONTROL Traffic-Schätzung] nutzt Statistiken zu Ihrer Seite und der Anzahl der getesteten Erlebnisse, um die Menge an Traffic und die Testdauer zu schätzen, die für den Erfolg des Tests erforderlich sind.

Die [!UICONTROL Traffic-Schätzung] sagt die erforderliche Stichprobengröße voraus, um Folgendes sicherzustellen:

* 95 % Konfidenz. Diese Statistik bedeutet, dass die Wahrscheinlichkeit, einen falsch positiven Wert zu melden, wenn es keine echte Steigerung gibt, 5 % beträgt (100 % - Konfidenzniveau).
* 80 % statistische Leistung. Diese Statistik bedeutet, dass der Test mit einer Wahrscheinlichkeit von 80 % eine tatsächliche Steigerung von 25 % oder mehr erkennt.
* 25% minimaler zuverlässig detektierbarer Anstieg. [!DNL Target] berechnet den Traffic, der erforderlich ist, um eine 80-prozentige Wahrscheinlichkeit zu haben, eine tatsächliche Steigerung von 25 % oder mehr zu erkennen.

Der Test verwendet die Bonferroni-Korrektur zur Korrektur von Mehrfachvergleichen. Diese Methode gilt als konservativ, was durch Erzwingen eines relativ hohen Wertes für die zuverlässig bestimmbare Mindeststeigerung kompensiert wird.

Die [!UICONTROL Traffic-Schätzung] bietet außerdem Feedback, mit dem Sie wissen, ob Sie über ausreichend Traffic für den Test verfügen, den Sie für einen erfolgreichen Test entwickelt haben.

1. Klicken Sie auf der [!UICONTROL Erlebnisse] des [!UICONTROL Visual Experience Composer] in einer [!UICONTROL Multivariate]-Aktivität auf das Symbol **[!UICONTROL Traffic]** ( ![Traffic-Schätzsymbol](/help/main/assets/icons/Gauge2.svg) ) in der oberen linken Ecke der Seite [!UICONTROL Erlebnisse].

   Die [!UICONTROL Traffic-Schätzung] wird geöffnet.

   ![Benutzeroberfläche der Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   Sie können erneut auf das Symbol klicken, um die [!UICONTROL Traffic-Schätzung“ &#x200B;].

   In der Nähe des oberen Bereichs der [!UICONTROL Traffic-Schätzung] werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

1. (Bedingt) Geben Sie die typische Konversionsrate, die geschätzten Besucher pro Tag und die Testdauer an.

   * **[!UICONTROL Anzahl der Inhaltskombinationen]**: Wird automatisch berechnet, basierend auf der Anzahl der Erlebnisse, die als Teil Ihrer Aktivität nach einem Ausschluss erstellt werden.
   * **[!UICONTROL Typische Konversionsrate]**: Die Konversionsrate wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem.
   * **[!UICONTROL Geschätzte Besucherinnen und Besucher pro Tag]**: Dies ist die Anzahl der Besucherinnen und Besucher, die diese Seite wahrscheinlich basierend auf den Targeting-Kriterien anzeigen. Dies kann auf Ihren Analytics-Daten basieren.
   * **[!UICONTROL Testdauer]**: Die Anzahl der Tage, die die Aktivität ausgeführt werden soll.

   Die [!UICONTROL Traffic-Schätzung] verwendet diese Statistiken, um zu bestimmen, welche Anpassungen erforderlich sind, um einen erfolgreichen Test auszuführen.

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie beispielsweise viele Erlebnisse testen und Ihre Konversionsrate und Impressions zu niedrig sind, zeigt die [!UICONTROL Traffic-Schätzung] an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic niedrig ist, schlägt die [!UICONTROL Traffic-Schätzung] möglicherweise eine niedrigere Anzahl von Erlebnissen vor, sodass Sie den Test die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, können Sie eine oder beide der folgenden Maßnahmen ergreifen:

   * Reduzieren Sie die Anzahl der Angebotskombinationen sowie die Anzahl der Orte.
   * Verlängern der Testdauer.

   Passen Sie die Zahlen an, bis die [!UICONTROL Traffic-Schätzung] anzeigt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.
