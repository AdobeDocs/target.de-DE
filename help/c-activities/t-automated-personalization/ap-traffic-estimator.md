---
description: Die Traffic-Schätzung liefert Feedback, aus dem Sie erfahren, ob Sie über ausreichend Traffic verfügen, damit Ihre Aktivität erfolgreich ist.
title: Schätzen des für einen erfolgreichen Test erforderlichen Traffics
feature: ap
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Schätzen des für einen erfolgreichen Test erforderlichen Traffics{#estimate-the-traffic-required-for-success}

Die Traffic-Schätzung liefert Feedback, aus dem Sie erfahren, ob Sie über ausreichend Traffic verfügen, damit Ihre Aktivität erfolgreich ist.

Da eine Aktivität des Typs „Automatisierte Personalisierung“ mehrere Angebotskombinationen verwendet, ist es wichtig zu wissen, wie viel Traffic für aussagekräftige Testergebnisse erforderlich ist. Die Traffic-Schätzung verwendet Statistiken über Ihre Seite und die Anzahl der getesteten Erlebnisse, um das Traffic-Aufkommen und die erforderliche Testdauer für eine erfolgreiche Aktivität zu schätzen.

Die Traffic-Schätzung ermittelt anhand eines Vergleichs der geschätzten Seitenimpressionen und der typischen Konversionsrate für die Seiten, ob der Traffic ausreicht, um personalisierte Modelle zu generieren. Idealerweise gewährleistet die korrekte Stichprobengröße bei einer erfolgreichen Aktivität, dass personalisierter Inhalt innerhalb von 50 % der Dauer der Aktivität oder innerhalb von 14 Tagen bereit ist (je nachdem, welcher Fall zuerst eintritt). Dies bietet ausreichend Zeit, um personalisierten Inhalt zu erhalten und zu verstehen, welcher Inhalt bereitgestellt werden sollte.

Beachten Sie, dass Target zufällig so lange Erlebnisse verarbeitet, bis die Personalisierungsalgorithmen erstellt wurden. Das Häkchensymbol neben jedem Angebot zeigt, wann das Modell für dieses Angebot bereit ist und Target personalisierten Inhalt bereitstellen kann. Da eine Steigerung erst erwartet wird, wenn die Modelle fertig sind, können Sie anhand der visuellen Angabe die richtige Erwartung festlegen. Verwenden Sie die Traffic-Schätzung in Visual Experience Composer (VEC), um eine Vorstellung davon zu bekommen, wann die Modelle fertig sein werden.

1. Klicken Sie im Experience Composer auf **[!UICONTROL Traffic]**.

   ![Traffic-Symbol](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Die Traffic-Schätzung wird geöffnet. Sie können erneut auf **[!UICONTROL Traffic]** klicken, um die Traffic-Schätzung auszublenden.

   ![](assets/ap_est.png)

1. Geben Sie die typische Konversionsrate (oder die Konversionsrate, die Sie von dieser Aktivität erwarten), die geschätzten Aktivitätsimpressionen pro Tag und die Testdauer an.

   * Number of Content Combinations (Anzahl der Inhaltskombinationen): Wird automatisch anhand der Anzahl der erstellten Erlebnisse als Bestandteil Ihrer Aktivität nach etwaigen Ausschlüssen berechnet.
   * Typical Conversion Rate (Typische Konversionsrate): Die Konversionsrate wird als Prozentsatz ausgedrückt und basiert auf Ihrer Schätzung oder auf historischen Daten aus Ihrem Analytics-System.
   * Estimated Visits Per Day (Geschätzte Besuche pro Tag): Hierbei handelt es sich um die Anzahl der Besuche pro Tag von Besuchern, welche die Aktivität auf Basis von Targeting-Kriterien anzeigen können. Dies kann auf Ihren Analytics-Daten basieren. Beachten Sie, dass es sich bei dieser Zahl um Besuche und nicht um Unique Visitors handeln sollte.
   * Testdauer: Die Anzahl der Tage, während derer Sie die Aktivität ausführen möchten.

   Die Traffic-Schätzung verwendet diese Statistik, um zu ermitteln, welche Anpassungen erforderlich sind, um einen erfolgreichen Test auszuführen.

   Im oberen Bereich der Traffic-Schätzung werden die von ihnen eingegebenen Werte berechnet und die Ergebnisse werden angezeigt.

   ![](assets/ap_est_no.png)

   Wenn Sie die Zahlen ändern, ändern sich auch die Schätzwerte. Wenn Sie zum Beispiel eine große Anzahl von Kombinationen testen und Ihre Konversionsrate und die Impressionen zu niedrig sind, zeigt die Traffic-Schätzung an, wie lange der Test noch ausgeführt werden muss, um erfolgreich zu sein. Wenn Ihr Traffic langsam ist, kann die Traffic-Schätzung eine niedrigere Anzahl von Angebotskombinationen vorschlagen, sodass Sie den Test über die gewünschte Anzahl von Tagen ausführen können.

   Wenn Sie nicht über ausreichend Traffic verfügen, können Sie eine oder alle der folgenden Maßnahmen ergreifen:

   * Verwenden Sie ggf. „Automatisches Targeting“ anstelle von „Automatisierte Personalisierung“, um Erlebnisse mit verschiedenen Angebotsänderungen in einer Erlebnisvariation zu erstellen.
   * Reduzieren Sie die Anzahl der Angebotskombinationen in Ihrer Aktivität des Typs „Automatisierte Personalisierung“.
   * Erhöhen Sie die Dauer der Aktivität.

   Passen Sie die Zahlen so lange an, bis die Traffic-Schätzung Ihnen mitteilt, dass Sie über ausreichend Traffic verfügen. Dann können Sie Ihren Entwurf entsprechend entwerfen.

   ![](assets/ap_est_yes.png)

   Wenn der Traffic ausreicht, muss das Traffic-Symbol mit einem grünen Häkchen versehen sein. Wenn der Traffic nicht ausreicht, wird als Symbol ein roter Warnhinweis angezeigt.
