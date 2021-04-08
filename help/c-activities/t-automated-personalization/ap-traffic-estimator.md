---
keywords: Traffic-Schätzung;Automatisierte Personalisierung;App;Traffic-Schätzung;Auto-Zielgruppe
description: Verwenden Sie die Adobe Target Traffic-Schätzung, um zu ermitteln, ob Sie über ausreichend Traffic verfügen, damit Ihre Automated Personalization-Aktivität erfolgreich ist.
title: Wie viel Traffic wird für eine erfolgreiche Aktivität benötigt?
feature: Automatisierte Personalisierung
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
translation-type: tm+mt
source-git-commit: 6ba670ef69fa23c0023636a1920eed15dcd9dd06
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 14%

---

# ![PREMIUM](/help/assets/premium.png) Schätzen des für einen erfolgreichen Test erforderlichen Traffics

Die [!DNL Adobe Target] [!UICONTROL Traffic-Schätzung] liefert Feedback, mit dem Sie wissen können, ob Sie über ausreichend Traffic verfügen, damit Ihre [!UICONTROL Automated Personalization]-Aktivität erfolgreich ist.

Da eine [!UICONTROL Automated Personalization]-Aktivität mehrere Angebot-Kombinationen verwendet, ist es wichtig zu wissen, wie viel Traffic erforderlich ist, um aussagekräftige Ergebnisse zu erzielen. Die [!UICONTROL Traffic-Schätzung] verwendet Statistiken über Ihre Seite und die Anzahl der getesteten Erlebnisse, um die Traffic-Menge und die Testdauer zu schätzen, die für eine erfolgreiche Aktivität erforderlich ist.

Die [!UICONTROL Traffic-Schätzung] ermittelt, ob genügend Traffic vorhanden ist, um personalisierte Modelle zu generieren, indem die geschätzten Seitenimpressionen verglichen und die für die Seiten typischen Konversionsrat werden. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dieser Prozess bietet genügend Zeit, um personalisierte Inhalte zu erhalten und zu lernen, welche Inhalte bereitgestellt werden sollen.

Beachten Sie, dass [!DNL Target] nach dem Zufallsprinzip Erlebnisse bereitstellt, bis die Personalisierungsalgorithmen erstellt wurden. Das Häkchensymbol neben jedem Angebot zeigt an, wann das Modell für dieses Angebot fertig ist und [!DNL Target] mit der Bereitstellung personalisierter Inhalte beginnen kann. Da eine Steigerung erst erwartet wird, wenn die Modelle fertig sind, können Sie anhand der visuellen Angabe die richtige Erwartung festlegen. Verwenden Sie die [!UICONTROL Traffic-Schätzung] in [!UICONTROL Visual Experience Composer] (VEC), um eine Richtlinie darüber zu erhalten, wann die Modelle fertig sind.

## Traffic-Schätzung verwenden

1. Klicken Sie in [!UICONTROL Visual Experience Composer] auf **[!UICONTROL Traffic]**.

   ![Traffic-Symbol](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Die [!UICONTROL Traffic-Schätzung] wird geöffnet. Sie können erneut auf **[!UICONTROL Traffic]**[!UICONTROL  klicken, um die Traffic-Schätzung auszublenden].

   ![Benutzeroberfläche &quot;Traffic-Schätzung&quot;](assets/ap_est.png)

1. Geben Sie den typischen Konversionsrate (oder den Konversionsrate an, den Sie von dieser Aktivität erwarten), die geschätzten Aktivitäten pro Tag und die Testdauer an.

   | Metrik | Beschreibung |
   | --- | --- |
   | **[!UICONTROL Anzahl Angebot]** | Diese Metrik wird automatisch auf Grundlage der Anzahl der Erlebnisse berechnet, die als Teil Ihrer Aktivität nach etwaigen Ausnahmen erstellt werden. |
   | **[!UICONTROL Typische Konversionsrate]** | Diese Metrik wird als Prozentsatz ausgedrückt, basierend auf Ihrer Schätzung oder früheren Daten aus Ihrem Analysesystem. |
   | **[!UICONTROL Geschätzte Besuche pro Tag]** | Diese Metrik ist die Anzahl der Besuche pro Tag von Besuchern, die die Aktivität auf der Grundlage der Targeting-Kriterien Ansichten durchführen können. Diese Metrik kann auf Ihren Analysedaten basieren. Bei dieser Anzahl muss es sich um Besuche und nicht um individuelle Besucher handeln. |
   | **[!UICONTROL Testdauer]** | Die Anzahl der Tage, binnen derer Sie die Aktivität ausführen möchten. |

   Die [!UICONTROL Traffic-Schätzung] verwendet diese Metriken, um zu bestimmen, welche Anpassungen erforderlich sind, um einen erfolgreichen Test auszuführen.

   Oben im [!UICONTROL Traffic-Schätzung] werden die eingegebenen Werte berechnet und die Ergebnisse angezeigt.

   ![Traffic-Schätzung mit angezeigten Werten und Ergebnissen](assets/ap_est_no.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie z. B. viele Kombinationen testen und Ihre Konversionsrat- und Impressionen zu niedrig sind, zeigt die [!UICONTROL Traffic-Schätzung] an, wie lange der Test ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic gering ist, kann die [!UICONTROL Traffic-Schätzung] eine niedrigere Anzahl von Angebot-Kombinationen vorschlagen, damit Sie den Test in der gewünschten Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, sollten Sie Folgendes beachten:

   * Erwägen Sie, anstelle von [!UICONTROL Automated Personalization] eine [Auto-Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md)-Aktivität zu verwenden, um Erlebnisse mit mehreren Angebot-Änderungen in einer Erlebnisvariante zu erstellen.
   * Reduzieren Sie die Anzahl der Angebot-Kombinationen in Ihrer [!UICONTROL Automated Personalization]-Aktivität.
   * Erhöhen Sie die Dauer der Aktivität.

   Passen Sie die Zahlen an, bis die Traffic-Schätzung [!UICONTROL angibt, dass Sie über ausreichend Traffic verfügen, und entwerfen Sie dann Ihren Test entsprechend.]

   ![Traffic-Schätzung mit ausreichender Traffic-Meldung](assets/ap_est_yes.png)

   Wenn der Traffic ausreicht, wird auf dem Symbol [!UICONTROL Traffic] eine grüne Prüfung angezeigt. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.

## Häufig gestellte Fragen zur Traffic-Schätzung

Berücksichtigen Sie die folgenden häufig gestellten Fragen beim Arbeiten mit der [!UICONTROL Traffic-Schätzung]:

### Warum werden personalisierte Modelle nicht erstellt, obwohl meine AP-Aktivität über ausreichend Traffic verfügt?

Unter bestimmten Umständen ist Ihr Traffic groß genug, um ein personalisiertes Modell zu erstellen, aber dieser Traffic könnte [!DNL Target] darüber informieren, dass es keinen bedeutenden Unterschied zwischen dem personalisierten Modell und dem Zufallsprinzip gibt. Obwohl das Modell in [!DNL Target] erstellt und getestet wurde, wird es nicht bereitgestellt, da das Modell nicht besser als zufällig ist.

Ein möglicher Grund dafür, dass das Modell nicht besser als zufällig ist, könnte sein, dass die Angebot nicht voneinander abweichen. In diesem Fall können Sie versuchen, die Angebot visueller anders zu gestalten, wenn das Messaging ähnlich ist, oder Sie können versuchen, das Messaging selbst zu ändern.
