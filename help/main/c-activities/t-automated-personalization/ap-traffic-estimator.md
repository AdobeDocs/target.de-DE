---
keywords: Traffic-Schätzung;Automated Personalization;App;Traffic schätzen
description: Verwenden Sie die  [!DNL Adobe Target] [!UICONTROL Traffic Estimator], um festzustellen, ob Sie über ausreichend Traffic verfügen, damit Ihre [!UICONTROL Automated Personalization]-Aktivität erfolgreich ist.
title: Wie viel Traffic wird für eine erfolgreiche [!UICONTROL Automated Personalization] benötigt?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: eacee6f353aa685d17b781ac82d3f79574384dfe
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 10%

---

# Schätzen des für einen erfolgreichen Test erforderlichen Traffics

Die [!DNL Adobe Target]-[!UICONTROL Traffic Estimator] bietet Feedback, mit dem Sie wissen, ob Sie über ausreichend Traffic verfügen, damit Ihre [!UICONTROL Automated Personalization] (AP)-Aktivität erfolgreich ist.

Da [!UICONTROL Automated Personalization] Aktivitäten mehrere Angebotskombinationen verwenden, ist es wichtig zu wissen, wie viel Traffic erforderlich ist, um aussagekräftige Ergebnisse zu erzielen. Der [!UICONTROL Traffic Estimator] verwendet Statistiken zu Ihrer Seite und der Anzahl der Erlebnisse, die getestet werden, um die Menge an Traffic und die Testdauer zu schätzen, die für den Erfolg der Aktivität erforderlich sind.

Die [!UICONTROL Traffic Estimator] bestimmt, ob ausreichend Traffic vorhanden ist, um personalisierte Modelle zu generieren, indem sie die geschätzten Seitenimpressionen und die typische Konversionsrate für die Seiten vergleicht. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dieser Prozess lässt ausreichend Zeit für den Erhalt personalisierter Inhalte und das Erlernen der bereitzustellenden Inhalte.

Denken Sie daran, dass [!DNL Target] Erlebnisse nach dem Zufallsprinzip bereitstellt, bis die Personalisierungsalgorithmen erstellt werden. Das Häkchensymbol neben jedem Angebot zeigt an, wenn das Modell für dieses Angebot bereit ist und [!DNL Target] mit der Bereitstellung personalisierter Inhalte beginnen kann. Da die Steigerung erst nach Fertigstellung der Modelle erwartet wird, können Sie mit der visuellen Anzeige die richtigen Erwartungen festlegen. Verwenden Sie die [!UICONTROL Traffic Estimator] im [!UICONTROL Visual Experience Composer] (VEC), um eine Richtlinie zu erhalten, wann die Modelle bereit sind.

## Traffic-Schätzung verwenden

1. Klicken Sie auf der [!UICONTROL Experiences] der [!UICONTROL Visual Experience Composer] in einer [!UICONTROL Automated Personalization] auf das Symbol **[!UICONTROL Traffic]** .

   ![Traffic-Symbol](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Die [!UICONTROL Traffic Estimator] wird geöffnet. Sie können erneut auf **[!UICONTROL Traffic]** klicken, um die [!UICONTROL Traffic Estimator] auszublenden.

   ![Benutzeroberfläche der Traffic-Schätzung](assets/ap_est.png)

1. Geben Sie die typische Konversionsrate (oder die von dieser Aktivität erwartete Konversionsrate), geschätzte Aktivitätsimpressionen pro Tag und die Testdauer an.

   | Metrik | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | Diese Metrik wird automatisch anhand der Anzahl der Erlebnisse berechnet, die im Rahmen Ihrer Aktivität nach allen Ausschlüssen erstellt werden. |
   | **[!UICONTROL Typical Conversion Rate]** | Diese Metrik wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem. |
   | **[!UICONTROL Estimated Visits Per Day]** | Diese Metrik stellt die Anzahl der Besuche pro Tag dar, die Besucherinnen und Besucher, die die Aktivität anzeigen können, auf der Grundlage der Targeting-Kriterien verzeichnen. Diese Metrik könnte auf Ihren Analysedaten basieren. Bei dieser Zahl muss es sich um Besuche und nicht um Unique Visitors handeln. |
   | **[!UICONTROL Test Duration]** | Die Anzahl der Tage, binnen derer Sie die Aktivität ausführen möchten. |

   Der [!UICONTROL Traffic Estimator] verwendet diese Metriken, um zu bestimmen, welche Anpassungen für die Ausführung eines erfolgreichen Tests erforderlich sind.

   Im oberen Bereich der [!UICONTROL Traffic Estimator] werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

   ![Traffic-Schätzung mit angezeigten Werten und Ergebnissen](assets/ap_est_no.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie beispielsweise viele Kombinationen testen und Ihre Konversionsrate und Impressions zu niedrig sind, zeigt die [!UICONTROL Traffic Estimator] an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic niedrig ist, kann der [!UICONTROL Traffic Estimator] eine niedrigere Anzahl von Angebotskombinationen vorschlagen, sodass Sie den Test die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, beachten Sie Folgendes:

   * Erwägen Sie die Verwendung [ Aktivität „Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) anstelle von [!UICONTROL Automated Personalization], um Erlebnisse mit mehreren Angebotsänderungen in einer Erlebnisvariante zu erstellen.
   * Verringern Sie die Anzahl der Angebotskombinationen innerhalb Ihrer [!UICONTROL Automated Personalization].
   * Erhöhen Sie die Dauer der Aktivität.

   Passen Sie die Zahlen an, bis die [!UICONTROL Traffic Estimator] anzeigt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.

   ![Traffic-Schätzung zeigt eine ausreichende Traffic-Meldung an](assets/ap_est_yes.png)

   Wenn der Traffic ausreichend ist, zeigt das [!UICONTROL Traffic]-Symbol einen grünen Haken an. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.

## Häufig gestellte Fragen zur Traffic-Schätzung

Beachten Sie bei der Arbeit mit dem [!UICONTROL Traffic Estimator] die folgenden häufig gestellten Fragen:

### Warum werden keine personalisierten Modelle erstellt, obwohl meine API-Aktivität über ausreichend Traffic verfügt?

Unter bestimmten Umständen ist Ihr Traffic groß genug, um ein personalisiertes Modell zu erstellen, aber dieser Traffic könnte [!DNL Target] darüber informieren, dass es keinen sinnvollen Unterschied zwischen dem personalisierten Modell und dem zufälligen Modell gibt. Obwohl das Modell in [!DNL Target] erstellt und getestet wurde, wird es nicht bereitgestellt, da das Modell nicht besser als zufällig ist.

Ein möglicher Grund dafür, dass das Modell nicht besser als zufällig ist, könnte darin bestehen, dass die Angebote nicht ausreichend voneinander abweichen. In diesem Fall können Sie versuchen, die Angebote visuell zu verändern, wenn die Nachricht ähnlich ist, oder Sie können versuchen, die Nachricht selbst zu ändern.
