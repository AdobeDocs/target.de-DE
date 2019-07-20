---
description: Wählen Sie ein Erlebnis, das bei der Erstellung einer automatisierten Personalisierung (AP) oder einer automatischen Targeting-Aktivität als Kontrolle verwendet werden soll.
keywords: Erlebnis; control; automatisierte Personalisierung; automatisches Targeting
seo-description: Wählen Sie ein Erlebnis, das beim Erstellen einer automatisierten Personalisierung (AP) oder einer automatischen Targeting-Aktivität in Adobe Target verwendet werden soll.
seo-title: Verwenden eines bestimmten Erlebnisses als Kontrolle in Adobe Target
solution: Target,Analytics
title: Verwenden Sie ein bestimmtes Erlebnis als Steuerelement
uuid: c67901d2-19cd-47d3-b8c4-abdcb046f404
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# ![PREMIUM](/help/assets/premium.png) Select the control for your Automated Personalization or Auto-Targeting activity

You can select a randomly served experience or a specific experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Mit dieser Funktion können Sie den Traffic auf Grundlage des in der Aktivität konfigurierten Prozentsatzes für den Traffic-Zuweisungsprozentsatz den relevanten Erlebnissen weiterleiten. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Steuerelement zu steuern.

Die Optionen zum Festlegen eines Steuerelements in AP- und AT-Aktivitäten unterscheiden sich geringfügig von anderen Aktivitätstypen. In einem manuellen A/B-Test können Sie ändern, welche Berichte als Ihre Steuerung angezeigt werden, und die Steigerung wird anhand der Konversionsrate dieses Kontrollerlebnisses berechnet. Sie können diese Änderung einfach vornehmen, da der Traffic per Zufall an jedes der Erlebnisse, die Sie in Ihrer Aktivität eingeschlagen haben, verteilt wird, unabhängig davon, auf welche Weise das Steuerelement anfänglich eingestellt ist. Das heißt, das Auswählen des Steuerelements wirkt sich nicht auf den Traffic aus. In AP- und AT-Aktivitäten hat Ihre Entscheidung darüber, wie der Besucher gesteuert wird, Auswirkungen darauf, wie der Besucher-Traffic bedient wird. Daher sollten Sie sich genauer über Ihre Entscheidung Gedanken machen.

Für Ihre AP- und AT-Aktivitäten stehen Ihnen zwei Optionen zur Verfügung: zufällig bereitgestellte Erlebnisse oder ein bestimmtes Erlebnis.

* **Zufällig bereitgestellt**: Bei zufälliger Kontrolle liefert der Steuerprozentsatz des Traffics alle Erlebnisse in der Aktivität ohne Berücksichtigung des Besucherprofils. Sie können sich das Steuerelement als Hilfe bei der Beantwortung der Frage vorstellen: "Wenn ich ein Erlebnis (oder ein Angebot) zufällig für Besucher bereitstellen und ihre Profile nicht berücksichtigen kann, wie hoch ist die Konversionsrate für dieses Erlebnis (oder Angebot)? » Das Steuerelement ist wie ein A/B-Test innerhalb Ihrer AI-Aktivität. Diese Informationen der nicht personalisierten Konversionsrate für jedes Erlebnis oder Angebot können hilfreich sein, um zu verstehen, wann Ihre Aktivitätsergebnisse analysiert werden.

* **Bestimmtes Erlebnis**: Mit einem spezifischen Erlebnis-Steuerelement können Sie den von den Personalisierungsmodellen von Target bereitgestellten Traffic mit einem bestimmten, vom Marketingexperten definierten Erlebnis (z. B. Ihrer standardmäßigen Homepage) vergleichen. Mit dieser Option erhält der Steuerprozentsatz des Traffics den Traffic nur für dieses ein Erlebnis.

## Festlegen eines bestimmten Erlebnisses als Steuerelement

1. While creating an [AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md) or [AT activity](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configure the experiences as desired.
1. On the [!UICONTROL Targeting] page (step 2 of the three-part guided workflow), select the desired experience as the control.
1. Geben Sie die gewünschte Traffic-Zuordnung für das Kontrollerlebnis und andere Erlebnisse an.

   Für ein bestimmtes Erlebnis-Steuerelement werden 10% bis 30% empfohlen.

1. Continue with the [!UICONTROL Goals &amp; Settings] page.

## Bekannte Einschränkungen und Überlegungen

Beachten Sie Folgendes, wenn Sie ein bestimmtes Erlebnis als Kontrolle verwenden:

* Das Ändern des Kontrollerlebnisses in einer bereits aktiven Aktivität wird nicht empfohlen. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten benannt (auch wenn ältere Berichte auf einem anderen Erlebnis basieren).
* Das Löschen des Kontrollerlebnisses wird nicht empfohlen.
* Es wird nicht empfohlen, eine große Anzahl neuer Angebote/Erlebnisse zu einer Live-Aktivität mit einem bestimmten Erlebnis hinzuzufügen.
* In AP-Aktivitäten, einschließlich des Targeting auf das Kontrollerlebnis, das weitere Einschränkungen für die Erkenntnis darstellt, dass dieses Erlebnis nicht empfohlen wird.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. Informationen zu Steigerung und Konfidenz sind auf der gesamten Zielgruppenebene "Zielgerichtet" im Vergleich zu" Kontroll-Traffic" für die AP-Aktivität verfügbar. Informationen zu Steigerung und Vertrauen sind verfügbar, wenn als Steuerung "random" ausgewählt ist. Dies liegt daran, dass das Vergleichen der Konversionsrate eines bestimmten Erlebnisses mit der Umrechnungsrate eines Angebots aufgrund der Unterschiede in den Einheiten nicht logisch ist. Die in einer AT-Aktivität verfügbaren Informationen sind gleich, unabhängig davon, welche Art von Kontrolle ausgewählt ist.
* Da der gesamte Traffic-Traffic zu einem einzelnen Erlebnis oder Angebotsset führt, wenn Sie das Erlebnis als Kontrolle auswählen (im Vergleich zu zufällig, wo der Traffic-Traffic-Betrag auf die Anzahl der Erlebnisse oder Angebote in Ihrer Aktivität aufgeteilt ist), benötigen Sie im Allgemeinen nicht so viel Traffic, um zur Kontrolle zu gelangen. 10% ist eine gute Anlaufstelle.
* Wenn Sie einer Live-Aktivität mit einem bestimmten Erlebnis als Steuerelement einen der folgenden Schritte ausführen, wird das Steuerelement automatisch auf die Erlebnisse zurückgesetzt (anstelle des zuvor ausgewählten spezifischen Erlebnisses):

   * Löschen eines Erlebnisses
   * Ort oder Angebot entfernen (nur AP)
   * Erlebnis manuell ausschließen, indem Sie doppelte Angebote oder über eine Ausschlussgruppe entfernen (nur AP)

