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


# ![PREMIUM](/help/assets/premium.png) Ein bestimmtes Erlebnis als Kontrolle verwenden

You can select an experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern.

Die Kontrolloption für zufällig bereitgestellte Erlebnisse ist ebenfalls verfügbar.

Wenn wir ein bestimmtes Erlebnis als Kontrolle verwenden, können Ihre Berichte bei der Beantwortung der Frage helfen: &quot;Wird eine AP/AT-Aktivität besser ausgeführt als die Ausführung meiner Aktivitäten? « Ein Vorteil von AP/AT-Aktivitäten besteht darin, dass Sie weitere Optionen erstellen können, die für alle Benutzer nicht sinnvoll sind, aber für den richtigen Benutzer leistungsfähig sein können. Das bedeutet, dass das Vergleichen unseres Algorithmus mit zufällig nicht fair ist; nicht alle Optionen auf allen Besuchern Ihrer Site ausführen.

## Festlegen eines bestimmten Erlebnisses als Steuerelement

1. While creating an [AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md) or [AT activity](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configure the experiences as desired.
1. On the [!UICONTROL Targeting] page (step 2 of the three-part guided workflow), select the desired experience as the control.
1. Geben Sie die gewünschte Traffic-Zuordnung für das Kontrollerlebnis und andere Erlebnisse an.
1. Continue with the [!UICONTROL Goals &amp; Settings] page.

## Bekannte Einschränkungen

Bei Verwendung eines spezifischen Erlebnisses als Steuerung gelten bekannte Einschränkungen:

* Das Ändern des Kontrollerlebnisses in einer bereits aktiven Aktivität wird nicht empfohlen. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten benannt (auch wenn ältere Berichte auf einem anderen Erlebnis basieren).
* Das Löschen des Kontrollerlebnisses wird nicht empfohlen.
* In AP-Aktivitäten wird, einschließlich des Targeting auf das Kontrollerlebnis, nicht empfohlen, die weitere Einblicke in dieses Erlebnis erhalten.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. Informationen zu Steigerung und Vertrauen sind verfügbar, wenn als Steuerung &quot;random&quot; ausgewählt ist.

   Lift and confidence information *is* available at the overall &quot;targeted&quot; vs. &quot;control&quot; traffic level for the activity. Dies liegt daran, dass das Vergleichen der Konversionsrate eines bestimmten Erlebnisses mit der Umrechnungsrate eines Angebots aufgrund der Unterschiede in den Einheiten nicht logisch ist.

## Fehlerbehebung

Sollten Probleme auftreten, sollten Sie die folgenden Tipps zur Fehlerbehebung beachten:

* Da der gesamte Traffic-Traffic zu einem einzelnen Erlebnis oder Angebotsset führt, wenn Sie das Erlebnis als Kontrolle auswählen (im Vergleich zu zufällig, wo der Traffic-Traffic-Betrag auf die Anzahl der Erlebnisse/Angebote in Ihrer Aktivität aufgeteilt ist), benötigen Sie im Allgemeinen nicht so viel Traffic, um zur Kontrolle zu gelangen. 10% ist eine gute Anlaufstelle.
* Wenn Sie einer Live-Aktivität einen der folgenden Schritte ausführen, wird das Steuerelement automatisch auf zufällig bereitgestellte Erlebnisse zurückgesetzt (anstelle des zuvor ausgewählten Erlebnisses):

   * Löschen eines Erlebnisses
   * Ort oder Angebot entfernen (nur AP)
   * Erlebnis manuell ausschließen, indem Sie doppelte Angebote oder über eine Ausschlussgruppe entfernen (nur AP)
