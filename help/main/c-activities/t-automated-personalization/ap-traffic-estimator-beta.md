---
keywords: Traffic-Schätzung;automatisierte Personalisierung;App;Traffic schätzen
description: Verwenden Sie den [!UICONTROL Traffic Estimator] , um zu bewerten, ob Sie über ausreichend Traffic verfügen, damit eine [!UICONTROL Automated Personalization] -Aktivität erfolgreich ist.
title: Wie viel Traffic wird für eine erfolgreiche [!UICONTROL Automated Personalization] -Aktivität benötigt?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
hide: true
hidefromtoc: true
source-git-commit: 144a0ff89d11f523cba0780f60db942ca5773105
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 9%

---

# Schätzen des für einen erfolgreichen Test erforderlichen Traffics

Der [!DNL Adobe Target] [!UICONTROL Traffic Estimator] liefert Feedback, der Ihnen mitteilt, ob Sie über ausreichend Traffic verfügen, damit Ihre [!UICONTROL Automated Personalization] -Aktivität (AP) erfolgreich ist.

Da [!UICONTROL Automated Personalization] -Aktivitäten mehrere Angebotskombinationen verwenden, ist es wichtig zu wissen, wie viel Traffic erforderlich ist, um aussagekräftige Ergebnisse zu liefern. Der [!UICONTROL Traffic Estimator] verwendet Statistiken über Ihre Seite und die Anzahl der getesteten Erlebnisse, um das Traffic-Aufkommen und die Testdauer zu schätzen, die für eine erfolgreiche Aktivität erforderlich sind.

Der [!UICONTROL Traffic Estimator] ermittelt, ob ausreichend Traffic vorhanden ist, um personalisierte Modelle zu generieren, indem die geschätzten Seitenimpressionen und die typische Konversionsrate für die Seiten verglichen werden. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dieser Prozess bietet ausreichend Zeit, um personalisierte Inhalte zu erhalten und zu lernen, welche Inhalte bereitgestellt werden sollen.

Beachten Sie, dass [!DNL Target] Erlebnisse zufällig bereitstellt, bis die Personalisierungsalgorithmen erstellt wurden. Das Häkchen-Symbol neben jedem Angebot zeigt an, wann das Modell für dieses Angebot bereit ist und [!DNL Target] mit der Bereitstellung personalisierter Inhalte beginnen kann. Da eine Steigerung erst erwartet wird, wenn die Modelle fertig sind, können Sie mit der visuellen Anzeige die richtige Erwartung festlegen. Verwenden Sie die [!UICONTROL Traffic Estimator] im [!UICONTROL Visual Experience Composer] (VEC), um eine Richtlinie dazu zu erhalten, wann die Modelle fertig sind.

## Traffic-Schätzung verwenden

1. Klicken Sie auf der Seite [!UICONTROL Experiences] des Felds [!UICONTROL Visual Experience Composer] in einer [!UICONTROL Automated Personalization] -Aktivität auf das Symbol **[!UICONTROL Traffic]** ( ![Traffic-Schätzung-Symbol](/help/main/assets/icons/Gauge2.svg) ) oben links auf der Seite &quot;Erlebnisse&quot;.

   Der [!UICONTROL Traffic Estimator] wird geöffnet.

   ![Benutzeroberfläche der Traffic-Schätzung](assets/ap-est.png)

   Sie können erneut auf das Symbol klicken, um den [!UICONTROL Traffic Estimator] auszublenden.

1. Geben Sie die typische Konversionsrate (oder die Konversionsrate, die Sie von dieser Aktivität erwarten), die geschätzten Aktivitätsimpressionen pro Tag und die Testdauer an.

   | Metrik | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | Diese Metrik wird nach etwaigen Ausschlüssen automatisch anhand der Anzahl der Erlebnisse berechnet, die im Rahmen Ihrer Aktivität erstellt werden. |
   | **[!UICONTROL Typical Conversion Rate]** | Diese Metrik wird als Prozentsatz ausgedrückt und basiert auf Ihrer Schätzung oder auf historischen Daten aus Ihrem Analysesystem. |
   | **[!UICONTROL Estimated Visits Per Day]** | Diese Metrik ist die Anzahl der Besuche pro Tag von Besuchern, die die Aktivität anhand der Targeting-Kriterien anzeigen können. Diese Metrik kann auf Ihren Analysedaten basieren. Bei dieser Anzahl muss es sich um Besuche und nicht um Unique Visitors handeln. |
   | **[!UICONTROL Test Duration]** | Die Anzahl der Tage, binnen derer Sie die Aktivität ausführen möchten. |

   Der [!UICONTROL Traffic Estimator] verwendet diese Metriken, um zu bestimmen, welche Anpassungen für einen erfolgreichen Test erforderlich sind.

   In der Nähe des oberen Bereichs von [!UICONTROL Traffic Estimator] werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

   ![Traffic-Schätzung mit angezeigten Werten und Ergebnissen](assets/ap-est-no.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie beispielsweise viele Kombinationen testen und Ihre Konversionsrate und die Impressionen zu niedrig sind, zeigt der [!UICONTROL Traffic Estimator] an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Oder wenn Ihr Traffic gering ist, könnte der [!UICONTROL Traffic Estimator] eine niedrigere Anzahl von Angebotskombinationen vorschlagen, sodass Sie den Test über die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, beachten Sie Folgendes:

   * Erwägen Sie die Verwendung einer [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) -Aktivität anstelle von [!UICONTROL Automated Personalization], um Erlebnisse mit mehreren Angebotsänderungen in einer Erlebnisvariante zu erstellen.
   * Reduzieren Sie die Anzahl der Angebotskombinationen innerhalb Ihrer [!UICONTROL Automated Personalization] -Aktivität.
   * Erhöhen Sie die Dauer der Aktivität.

   Passen Sie die Zahlen an, bis das [!UICONTROL Traffic Estimator] zeigt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.

   ![Traffic-Schätzung mit ausreichender Traffic-Meldung](assets/ap-est-yes.png)

   Wenn der Traffic ausreicht, wird für das Symbol &quot;[!UICONTROL Traffic]&quot;eine grüne Prüfung angezeigt. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.

## Häufig gestellte Fragen zur Traffic-Schätzung

Beachten Sie die folgenden häufig gestellten Fragen bei der Arbeit mit dem [!UICONTROL Traffic Estimator]:

### Warum werden personalisierte Modelle nicht erstellt, obwohl meine AP-Aktivität über ausreichend Traffic verfügt?

Unter bestimmten Umständen ist Ihr Traffic groß genug, um ein personalisiertes Modell zu erstellen. Dieser Traffic könnte jedoch [!DNL Target] darauf hinweisen, dass es keinen sinnvollen Unterschied zwischen dem personalisierten Modell und dem zufälligen Modell gibt. Obwohl das Modell in [!DNL Target] erstellt und getestet wurde, wird es nicht bereitgestellt, da das Modell nicht besser als zufällig ist.

Ein möglicher Grund dafür, dass das Modell nicht besser als zufällig ist, könnte sein, dass die Angebote nicht voneinander abweichen. Wenn dies der Fall ist, können Sie versuchen, die Angebote visueller zu verändern, wenn die Nachricht ähnlich ist, oder Sie können versuchen, die Nachricht selbst zu ändern.