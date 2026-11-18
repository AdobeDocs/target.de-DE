---
keywords: Traffic-Schätzung;Traffic-Schätzung;Schätzung;Traffic;Konfidenz;statistische Leistung;Steigerung;Bonferroni;Konversionsrate;Besucher pro Tag;Dauer
description: Erfahren Sie, wie Sie mit der Traffic-Schätzung wissen, ob Sie über ausreichend Traffic für eine erfolgreiche [!DNL Adobe Target] [!UICONTROL Multivarianz]Test) verfügen.
title: Wie viel Traffic wird für eine Aktivität des Typs [!UICONTROL Multivariater Test] (MVT) benötigt?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
TQID: 'https://experienceleague.adobe.com/XHBXV7Jtvp87ve4NTd-016E2dFkHTbPu-8-nY8GE-VM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 8%
---
# Schätzen des für eine erfolgreiche Aktivität [!UICONTROL Multivarianz-Test] erforderlichen Traffics {#traffic-estimator}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie mit der **[!UICONTROL Traffic-Schätzung]** überprüfen können, ob Ihre **[!UICONTROL Multivarianz-Test]**-Aktivität über ausreichend Traffic verfügt, um erfolgreich zu sein.

>[!ENDSHADEBOX]

Bei einem Multivarianz-Test werden mehrere Erlebnisse verglichen. Daher ist es wichtig zu wissen, wie viel Traffic erforderlich ist, um aussagekräftige Ergebnisse zu erzielen. Die **[!UICONTROL Traffic-Schätzung]** nutzt Statistiken zu Ihrer Seite und der Anzahl der getesteten Erlebnisse, um die Menge an Traffic und die Testdauer zu schätzen, die für den Erfolg des Tests erforderlich sind. Außerdem erhalten Sie Feedback, mit dem Sie wissen, ob Sie über ausreichend Traffic für den Test verfügen, den Sie für den Erfolg konzipiert haben.

Die **[!UICONTROL Traffic-Schätzung]** sagt die erforderliche Stichprobengröße voraus, um Folgendes sicherzustellen:

* **95 % Konfidenz.** Diese Statistik bedeutet, dass die Wahrscheinlichkeit, einen falsch positiven Wert zu melden, wenn es keine echte Steigerung gibt, 5 % beträgt (100 % - Konfidenzniveau).
* **80 % statistische Leistung.** Diese Statistik bedeutet, dass der Test mit einer Wahrscheinlichkeit von 80 % eine tatsächliche Steigerung von 25 % oder mehr erkennt.
* **25% minimaler zuverlässig detektierbarer Anstieg.** [!DNL Target] berechnet den Traffic, der erforderlich ist, um eine 80-prozentige Wahrscheinlichkeit zu haben, eine tatsächliche Steigerung von 25 % oder mehr zu erkennen.

Der Test verwendet die Bonferroni-Korrektur zur Korrektur von Mehrfachvergleichen. Diese Methode gilt als konservativ, was durch Erzwingen eines relativ hohen Wertes für die zuverlässig bestimmbare Mindeststeigerung kompensiert wird.

## Traffic-Schätzung verwenden {#use-traffic-estimator}

Beim Entwerfen eines **[!UICONTROL Multivarianz-Tests]** können Sie mit der **[!UICONTROL Traffic-Schätzung]** überprüfen, ob der Traffic auf Ihrer Seite für die Anzahl der Erlebnisse, die Sie testen möchten, ausreicht. Wenn Sie diese Prüfung vor dem Start des Tests ausführen, vermeiden Sie einen Test, der nicht ausreichend viele Besucher erreichen kann, um aussagekräftige Ergebnisse zu erzielen. Außerdem erfahren Sie, wie Sie die Anzahl der Kombinationen oder die Dauer des Tests anpassen können, wenn der Traffic nicht ausreicht.

1. Klicken Sie auf der **[!UICONTROL Erlebnisse]** des **[!UICONTROL Visual Experience Composer]** in einer **[!UICONTROL Multivarianz]**-Aktivität auf das Symbol **[!UICONTROL Traffic]** ( ![Traffic-Schätzsymbol](/help/main/assets/icons/Gauge2.svg) ) in der oberen linken Ecke der Seite.

   Die **[!UICONTROL Traffic-Schätzung]** wird geöffnet. Um sie auszublenden, klicken Sie erneut auf das Symbol.

   ![Benutzeroberfläche der Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   In der Nähe des oberen Bereichs der **[!UICONTROL Traffic-Schätzung]** werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

1. (Optional) Geben Sie die typische Konversionsrate, die geschätzten Besucher pro Tag und die Testdauer an.

   Die **[!UICONTROL Traffic-Schätzung]** verwendet diese Statistiken, um zu bestimmen, welche Anpassungen erforderlich sind, um einen erfolgreichen Test auszuführen.

   | Metrik | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Anzahl der Inhaltskombinationen]** | Diese Metrik wird automatisch berechnet, basierend auf der Anzahl der Erlebnisse, die im Rahmen Ihrer Aktivität nach allen Ausschlüssen erstellt werden. |
   | **[!UICONTROL Typische Konversionsrate]** | Diese Metrik wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem. |
   | **[!UICONTROL Geschätzte Besucherzahlen pro Tag]** | Diese Metrik stellt die Anzahl der Besucher dar, die diese Seite wahrscheinlich anzeigen werden, basierend auf den Targeting-Kriterien. Diese Zahl kann auf Ihren Analysedaten basieren. |
   | **[!UICONTROL Testdauer]** | Die Anzahl der Tage, an denen die Aktivität ausgeführt werden soll. |

1. Überprüfen Sie die Ergebnisse. Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte.

   Wenn Sie beispielsweise viele Erlebnisse testen und Ihre Konversionsrate und Impressions zu niedrig sind, zeigt die **[!UICONTROL Traffic-Schätzung]** an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic niedrig ist, schlägt die **[!UICONTROL Traffic-Schätzung]** möglicherweise eine niedrigere Anzahl von Erlebnissen vor, damit Sie den Test für die gewünschte Anzahl von Tagen ausführen können.

1. Wenn Sie nicht über ausreichend Traffic verfügen, führen Sie einen oder beide der folgenden Schritte aus:

   * Reduzieren Sie die Anzahl der Angebotskombinationen sowie die Anzahl der Orte.
   * Verlängern der Testdauer.

1. Passen Sie die Zahlen an, bis **[!UICONTROL Traffic-Schätzung]** anzeigt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.
