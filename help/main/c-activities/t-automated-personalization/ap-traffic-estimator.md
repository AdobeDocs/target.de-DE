---
keywords: Traffic-Schätzung;automatisierte Personalisierung;App;Traffic schätzen
description: Verwenden Sie die [!DNL Adobe Target] [!UICONTROL Traffic-Schätzung] , um festzustellen, ob Sie über ausreichend Traffic für Ihre [!UICONTROL Automated Personalization] Aktivität erfolgreich zu sein.
title: Wie viel Traffic für eine erfolgreiche [!UICONTROL Automated Personalization] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: eacee6f353aa685d17b781ac82d3f79574384dfe
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 11%

---

# Schätzen des für einen erfolgreichen Test erforderlichen Traffics

Die [!DNL Adobe Target] [!UICONTROL Traffic-Schätzung] liefert Feedback, der Ihnen mitteilt, ob Sie über ausreichend Traffic für Ihre [!UICONTROL Automated Personalization] Aktivität (AP) erfolgreich sein.

weil [!UICONTROL Automated Personalization] -Aktivitäten mehrere Angebotskombinationen verwenden, ist es wichtig zu wissen, wie viel Traffic erforderlich ist, um aussagekräftige Ergebnisse zu erzielen. Die [!UICONTROL Traffic-Schätzung] verwendet Statistiken über Ihre Seite und die Anzahl der getesteten Erlebnisse, um das Traffic-Aufkommen und die Testdauer zu schätzen, die für eine erfolgreiche Aktivität erforderlich sind.

Die [!UICONTROL Traffic-Schätzung] ermittelt, ob ausreichend Traffic vorhanden ist, um personalisierte Modelle zu generieren, indem die geschätzten Seitenimpressionen und die typische Konversionsrate für die Seiten verglichen werden. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dieser Prozess bietet ausreichend Zeit, um personalisierte Inhalte zu erhalten und zu lernen, welche Inhalte bereitgestellt werden sollen.

Beachten Sie Folgendes: [!DNL Target] stellt zufällig Erlebnisse bereit, bis die Personalisierungsalgorithmen erstellt wurden. Das Häkchen-Symbol neben jedem Angebot zeigt an, wann das Modell für dieses Angebot bereit ist, und [!DNL Target] kann mit der Bereitstellung personalisierter Inhalte beginnen. Da eine Steigerung erst erwartet wird, wenn die Modelle fertig sind, können Sie mit der visuellen Anzeige die richtige Erwartung festlegen. Verwenden Sie die [!UICONTROL Traffic-Schätzung] im [!UICONTROL Visual Experience Composer] (VEC), um eine Richtlinie zu erhalten, wann die Modelle fertig sind.

## Traffic-Schätzung verwenden

1. Aus dem [!UICONTROL Erlebnisse] der [!UICONTROL Visual Experience Composer] in einer [!UICONTROL Automated Personalization] -Aktivität, klicken Sie auf die  **[!UICONTROL Traffic]** Symbol.

   ![Traffic-Symbol](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Die [!UICONTROL Traffic-Schätzung] geöffnet. Sie können erneut auf **[!UICONTROL Traffic]**[!UICONTROL  klicken, um die Traffic-Schätzung auszublenden].

   ![Traffic-Schätzung-Benutzeroberfläche](assets/ap_est.png)

1. Geben Sie die typische Konversionsrate (oder die Konversionsrate, die Sie von dieser Aktivität erwarten), die geschätzten Aktivitätsimpressionen pro Tag und die Testdauer an.

   | Metrik | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Anzahl der Angebote]** | Diese Metrik wird nach etwaigen Ausschlüssen automatisch anhand der Anzahl der Erlebnisse berechnet, die im Rahmen Ihrer Aktivität erstellt werden. |
   | **[!UICONTROL Typische Konversionsrate]** | Diese Metrik wird als Prozentsatz ausgedrückt und basiert auf Ihrer Schätzung oder auf historischen Daten aus Ihrem Analysesystem. |
   | **[!UICONTROL Geschätzte Besuche pro Tag]** | Diese Metrik ist die Anzahl der Besuche pro Tag von Besuchern, die die Aktivität anhand der Targeting-Kriterien anzeigen können. Diese Metrik kann auf Ihren Analysedaten basieren. Bei dieser Anzahl muss es sich um Besuche und nicht um Unique Visitors handeln. |
   | **[!UICONTROL Testdauer]** | Die Anzahl der Tage, binnen derer Sie die Aktivität ausführen möchten. |

   Die [!UICONTROL Traffic-Schätzung] verwendet diese Metriken, um zu bestimmen, welche Anpassungen für einen erfolgreichen Test erforderlich sind.

   Oben am [!UICONTROL Traffic-Schätzung], werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

   ![Traffic-Schätzung mit angezeigten Werten und Ergebnissen](assets/ap_est_no.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie beispielsweise viele Kombinationen testen und Ihre Konversionsrate und Impressionen zu niedrig sind, wird die [!UICONTROL Traffic-Schätzung] zeigt an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic gering ist, wird die [!UICONTROL Traffic-Schätzung] kann eine geringere Anzahl von Angebotskombinationen vorschlagen, sodass Sie den Test über die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, beachten Sie Folgendes:

   * Erwägen Sie die Verwendung eines [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) -Aktivität anstelle von [!UICONTROL Automated Personalization] , um Erlebnisse mit mehreren Angebotsänderungen in einer Erlebnisvariante zu erstellen.
   * Reduzieren Sie die Anzahl der Angebotskombinationen in Ihrer [!UICONTROL Automated Personalization] -Aktivität.
   * Erhöhen Sie die Dauer der Aktivität.

   Passen Sie die Zahlen bis zum [!UICONTROL Traffic-Schätzung] gibt an, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.

   ![Traffic-Schätzung mit ausreichender Traffic-Meldung](assets/ap_est_yes.png)

   Wenn der Traffic ausreicht, wird die [!UICONTROL Traffic] zeigt eine grüne Prüfung an. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.

## Häufig gestellte Fragen zur Traffic-Schätzung

Beachten Sie die folgenden häufig gestellten Fragen bei der Arbeit mit dem [!UICONTROL Traffic-Schätzung]:

### Warum werden personalisierte Modelle nicht erstellt, obwohl meine AP-Aktivität über ausreichend Traffic verfügt?

Unter bestimmten Umständen ist Ihr Traffic groß genug, um ein personalisiertes Modell erstellen zu können. Dieser Traffic könnte jedoch [!DNL Target] dass es keinen sinnvollen Unterschied zwischen dem personalisierten Modell und dem zufälligen Modell gibt. Obwohl das Modell in [!DNL Target] und getestet wird, wird sie nicht bereitgestellt, da das Modell nicht besser als zufällig ist.

Ein möglicher Grund dafür, dass das Modell nicht besser als zufällig ist, könnte sein, dass die Angebote nicht voneinander abweichen. Wenn dies der Fall ist, können Sie versuchen, die Angebote visueller zu verändern, wenn die Nachricht ähnlich ist, oder Sie können versuchen, die Nachricht selbst zu ändern.
