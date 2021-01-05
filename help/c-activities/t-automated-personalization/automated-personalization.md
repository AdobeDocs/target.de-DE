---
keywords: automated personalization;ap;audiences;ensemble;random forest;multi-armed bandit;thompson sampling;ml;machine learning
description: Automated Personalization (AP)Aktivitäten in Adobe Target kombinieren Angebot oder Nachrichten und verwenden fortschrittliches maschinelles Lernen, um den verschiedenen Besuchern je nach Profil des jeweiligen Kunden verschiedene Varianten des Angebots zuzuordnen, um Inhalte zu personalisieren und die Steigerung zu fördern.
title: Automatisierte Personalisierung
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 89%

---


# ![](/help/assets/premium.png) PREMIUMAutomated Personalization (AP)

[!UICONTROL Automated Personalization] (AP)-Aktivitäten  [!DNL Adobe Target] kombinieren Angebot oder Nachrichten und verwenden fortschrittliches maschinelles Lernen, um den verschiedenen Angebot-Varianten je nach Profil des jeweiligen Kunden anzupassen, um Inhalte zu personalisieren und die Steigerung zu fördern.

>[!NOTE]
>
>Die Funktion [!UICONTROL Automatisierte Personalisierung] steht als Bestandteil der [!DNL Target Premium]-Lösung zur Verfügung. Sie ist nicht in [!DNL Target Standard] ohne [!DNL Target Premium]-Lizenz enthalten. Wenn Sie über eine [!DNL Target Premium]-Lizenz verfügen, ersetzt die [!DNL Target Premium]-Karte die [!DNL Target Standard]-Karte in der [!DNL Adobe Experience Cloud].

Ähnlich wie bei [!UICONTROL Automatisches Targeting] verwendet [!UICONTROL Automatisierte Personalisierung] einen Random Forest-Algorithmus, also eine führende Methode in der Datenwissenschaft, als wichtigsten Personalisierungsalgorithmus zum Ermitteln des besten Erlebnisses, das einem Besucher angezeigt werden kann. [!UICONTROL Automatisierte Personalisierung] kann während der Entdeckungsphase des Testens sehr hilfreich sein. Es ist zudem nützlich, maschinelles Lernen zu ermöglichen, um den effektivsten Inhalt zu bestimmen, wenn man unterschiedliche Besucher anspricht. Im Lauf der Zeit lernt der Algorithmus, die effektivsten Inhalte vorherzusagen, und zeigt die Inhalte an, die am wahrscheinlichsten zum Erreichen Ihrer Ziele beitragen.

Weitere Informationen darüber, wie [!UICONTROL Automated Personalization] sich von [!UICONTROL Auto-Zielgruppe] unterscheidet, finden Sie unter [Automatische Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md).

Marketer implementieren eine Datei auf ihrer Website, dank der sie beliebige Inhalte anklicken und dann mit Hilfe des VEC ([!UICONTROL Visual Experience Composer]) visuell zusätzliche Inhaltsoptionen für diesen Bereich erstellen und auswählen können. Dann bestimmt der Algorithmus auf Basis aller Verhaltensdaten, die das System über diesen Besucher hat, automatisch, welche Inhalte jedem einzelnen Besucher gezeigt werden sollen, und liefert so eine personalisierte Erfahrung. Da sich die [!UICONTROL automatisierte Personalisierung] an Veränderungen beim Besucherverhalten anpasst, kann sie ohne ein festgelegtes Enddatum ausgeführt werden und ermöglicht dennoch eine kontinuierliche Weiterentwicklung der Personalisierung. Dies wird manchmal auch als „Always-on“-Modus bezeichnet. Der Marketer muss keine Tests durchführen, keine Ergebnisse analysieren und keinen sich daraus ergebenen Gewinner ermitteln, bevor er erkennen kann, welche Steigerung sich aus der Optimierung ergibt. Das übernimmt eine festgelegte Reihenfolge von Operationen, die dann das Ergebnis einer standardmäßigen A/B-Aktivität implementiert.

Die folgenden Begriffe und Definitionen sind hilfreich, wenn es um die [!UICONTROL automatisierte Personalisierung] geht:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Random Forest ist ein führender Ansatz beim maschinellen Lernen. In der Sprache der Datenwissenschaftler ist dies eine Ensemble-Classification- oder Regressionsmethode, die auf der Grundlage von Besuchern und Besuchsattributen eine große Anzahl von Entscheidungsbäumen erstellt. Random Forest wird von Target eingesetzt, um zu bestimmen, welches Erlebnis die höchste Wahrscheinlichkeit einer Konversion (oder den höchsten Umsatz pro Besuch) für jeden einzelnen Besucher hat. Weitere Informationen zu Random Forest in Target finden Sie unter  [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md). |
| Thompson Sampling | Ziel des Thompson Samplings ist es, festzustellen, welches (nicht personalisierte) Erlebnis insgesamt das beste ist, während gleichzeitig die „Kosten“ für die Auffindung dieses Erlebnisses minimiert werden. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

Folgendes sollte beim Einsatz der [!UICONTROL automatisierten Personalisierung] beachtet werden:

**[!UICONTROL Die automatisierte Personalisierung] verwendet einen Random Forest-Algorithmus.**

Random Forest ist ein führender Ansatz beim maschinellen Lernen. In der Sprache der Datenwissenschaftler ist dies eine Ensemble-Classification- oder Regressionsmethode, die auf der Grundlage von Besuchern und Besuchsattributen eine große Anzahl von Entscheidungsbäumen erstellt. Random Forest wird von Target eingesetzt, um zu bestimmen, welches Erlebnis die höchste Wahrscheinlichkeit einer Konversion (oder den höchsten Umsatz pro Besuch) für jeden einzelnen Besucher hat. Beispiel: Besucher, die Google Chrome verwenden, Mitglieder der Treuestufe „Gold“ sind und am Dienstag Ihre Website besuchen, konvertieren wahrscheinlicher bei Erlebnis A, während Besucher aus New York eher bei Erlebnis B konvertieren. Weitere Informationen zu Random Forest in Target finden Sie unter  [Random-Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md).

**Das Personalisierungsmodell wird bei jedem Besuch verbessert.**

* Der Algorithmus prognostiziert die Wahrscheinlichkeit der Konversion (oder der geschätzten Einnahmen aus der Konversion) eines Besuchers, um das beste Erlebnis anbieten zu können.
* Ein Besucher erhält am Ende eines Besuchs ein neues Erlebnis (es sei denn, er oder sie ist Mitglied einer Kontrollgruppe; in diesem Fall ist das Erlebnis, das der Besucher beim ersten Besuch sieht, das gleiche, das er oder sie bei späteren Besuchen sehen wird).
* Während eines Besuchs ändert sich das dargestellte Erlebnis nicht, um die visuelle Konsistenz aufrechtzuerhalten.

**Das Personalisierungsmodell passt sich an Änderungen beim Besucherverhalten an.**

* Multi-Armed Bandit gewährleistet, dass das Modell immer einen kleinen Anteil des Traffics darauf verwendet, während des gesamten Lebenszyklus der Aktivität weiter zu lernen, um so eine Übernutzung der zuvor erlernten Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden anhand der neuesten Daten zum Besucherverhalten überholt, um sicherzustellen, dass Target bei wechselnden Besucherpräferenzen immer auf dem neuesten Stand bleibt.
* Wenn der Algorithmus keine Gewinnererlebnisse für einzelne Besucher bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) ermittelt.

**Das Modell optimiert kontinuierlich eine einzige Zielmetrik.**

* Diese Metrik kann auf Konversionen oder Umsätzen (genauer gesagt: [!UICONTROL Umsatz pro Besucher]) basieren.

**Target sammelt automatisch Informationen über Besucher, um Personalisierungsmodelle zu erstellen.**

* Weitere Informationen zu den Attributen, die für [!UICONTROL automatisches Targeting] und [!UICONTROL automatisierte Personalisierung] verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/c-activities/t-automated-personalization/ap-data.md).

**Target verwendet automatisch alle[!DNL Adobe Experience Cloud] von gemeinsam genutzten Zielgruppen, um diese Personalisierungsmodelle zu erstellen.**

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md).

**Marketer können für die Erstellung von Personalisierungsmodellen Offline-Daten, Propensity Scores oder andere benutzerdefinierte Daten hochladen.**

Offline-Daten wie CRM-Informationen oder Propensity Scores zur Kundenabwanderung können beim Aufbau von Personalisierungsmodellen von unschätzbarem Wert sein. Es gibt verschiedene Möglichkeiten für die Dateneingabe in die Algorithmen zur [!UICONTROL automatisierten Personalisierung] (AP) und zum [!UICONTROL automatischen Targeting].

* [Mbox-Parameter](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Profilparameter](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Serverseitige APIs für das Profil-Update](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen der [!UICONTROL automatisierten Personalisierung] und des [!UICONTROL automatischen Targetings] gesammelt und verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/c-activities/t-automated-personalization/ap-data.md).

## ![Überblick ](/help/assets/overview.png) badgeSchulungsvideo: Aktivitäten

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Automatisierte Personalisierung wird ab 5:55 besprochen.]

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)