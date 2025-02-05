---
keyword: traffic estimate;traffic estimator;estimate;traffic;confidence;statistical power;lift;bonferroni;conversion rate;visitors per day;duration
description: Erfahren Sie, wie Sie mit der Traffic-Schätzung wissen, ob Sie über ausreichend Traffic für Ihre - [!DNL Adobe Target] [!UICONTROL Multivariate Test] verfügen, um erfolgreich zu sein.
title: Wie viel Traffic wird für eine [!UICONTROL Multivariate Test] (MVT)-Aktivität benötigt?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 53%

---

# Schätzen des für eine erfolgreiche [!UICONTROL Multivariate Test] erforderlichen Traffics

Da ein Multivariater Test mehrere Erlebnisse vergleicht, ist es wichtig zu wissen, wie hoch der erforderliche Traffic ist, um aussagekräftige Ergebnisse zu erzielen. Die Traffic-Schätzung verwendet Statistiken über Ihre Seite und die Anzahl der getesteten Erlebnisse, um das Traffic-Aufkommen und die erforderliche Testdauer für einen erfolgreichen Test zu schätzen.

Die Traffic-Schätzung prognostiziert die erforderliche Stichprobengröße, um Folgendes zu gewährleisten:

* 95 % Konfidenz. Diese Statistik bedeutet, dass die Wahrscheinlichkeit, einen falsch positiven Wert zu melden, wenn es keine echte Steigerung gibt, 5 % beträgt (100 % - Konfidenzniveau).
* 80 % statistische Leistung. Diese Statistik bedeutet, dass der Test mit einer Wahrscheinlichkeit von 80 % eine tatsächliche Steigerung von 25 % oder mehr erkennt.
* 25% minimaler zuverlässig detektierbarer Anstieg. [!DNL Target] berechnet den Traffic, der erforderlich ist, um eine 80-prozentige Wahrscheinlichkeit zu haben, eine tatsächliche Steigerung von 25 % oder mehr zu erkennen.

Der Test verwendet die Bonferroni-Korrektur zur Korrektur von Mehrfachvergleichen. Diese Methode gilt als konservativ, was durch Erzwingen eines relativ hohen Wertes für die zuverlässig bestimmbare Mindeststeigerung kompensiert wird.

Die Traffic-Schätzung liefert auch Feedback, aus dem Sie erfahren, ob Sie über ausreichend Traffic verfügen, damit der von Ihnen entworfene Test erfolgreich ist.

1. Klicken Sie in der [!UICONTROL Visual Experience Composer] auf das Symbol **[!UICONTROL Traffic]** .

   Die Traffic-Schätzung wird geöffnet. Sie können erneut auf das Symbol **[!UICONTROL Traffic]** klicken, um die Traffic-Schätzung auszublenden.

   ![estimatedEmpty image](assets/estimatorempty.png)

1. Geben Sie die übliche Konversionsrate, den Schätzwert für die Besucher pro Tag und die Testdauer an.

   * **[!UICONTROL Number of Content Combinations]**: Wird automatisch berechnet, basierend auf der Anzahl der Erlebnisse, die im Rahmen Ihrer Aktivität nach einem Ausschluss erstellt werden.
   * **[!UICONTROL Typical Conversion Rate]**: Die Konversionsrate wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem.
   * **[!UICONTROL Estimated Visitors Per Day]**: Dies ist die Anzahl der Besucherinnen und Besucher, die diese Seite anhand der Zielgruppenbestimmungskriterien wahrscheinlich anzeigen werden. Dies kann auf Ihren Analytics-Daten basieren.
   * **[!UICONTROL Test Duration]**: Die Anzahl der Tage, die die Aktivität ausgeführt werden soll.

   Die Traffic-Schätzung verwendet diese Statistik, um zu ermitteln, welche Anpassungen erforderlich sind, um einen erfolgreichen Test auszuführen.

   Im oberen Bereich der Traffic-Schätzung werden die von ihnen eingegebenen Werte berechnet und die Ergebnisse werden angezeigt.

   ![Unzureichendes Bild](assets/estimatorinsufficient.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie beispielsweise viele Erlebnisse testen und Ihre Konversionsrate und Impressions zu niedrig sind, zeigt die Traffic-Schätzung an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Oder wenn Ihr Traffic langsam ist, kann die Traffic-Schätzung eine niedrigere Anzahl von Erlebnissen vorschlagen, sodass Sie den Test über die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, können Sie eine oder beide der folgenden Maßnahmen ergreifen:

   * Reduzieren Sie die Anzahl der Angebotskombinationen sowie die Anzahl der Orte.
   * Verlängern der Testdauer.

   Passen Sie die Zahlen so lange an, bis die Traffic-Schätzung Ihnen mitteilt, dass Sie über ausreichend Traffic verfügen. Dann können Sie Ihren Entwurf entsprechend entwerfen.

   ![Bild des Schätzers](assets/estimatorok.png)
