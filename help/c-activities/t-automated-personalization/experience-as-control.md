---
keywords: experience;control;automated personalization;auto-target
description: Auswahl eines Kontrollerlebnisses bei der Erstellung einer automatisierten Personalisierung (AP) oder eines automatischen Targetings (AT) in Adobe Target.
title: Verwenden eines bestimmten Erlebnisses als Kontrolle in Adobe Target
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Auswahl des Kontrollelements für die Aktivität „Automatisierte Personalisierung“ oder „Automatisches Targeting“

Sie können beim Erstellen einer [automatisierten Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) auswählen, ob ein zufälliges oder ein bestimmtes Erlebnis als Kontrollelement verwendet werden soll.

Mit dieser Funktion können Sie den Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu den entsprechenden Erlebnissen leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem Kontrollerlebnis vergleichen und auswerten.

Die Optionen zum Festlegen eines Kontrollelements bei AP- und AT-Aktivitäten unterscheiden sich geringfügig von anderen Aktivitätstypen. In einem manuellen A/B-Test können Sie ändern, was in den Berichten als Ihre Kontrolle angezeigt wird, und die Steigerung wird anhand der Konversionsrate dieses Kontrollerlebnisses berechnet. Sie können diese Änderung einfach vornehmen, da der Traffic per Zufall an jedes der Erlebnisse geleitet wird, die Sie in Ihre Aktivität eingeschlossen haben, unabhängig davon, wie die Kontrolle ursprünglich eingestellt ist. Das heißt, dass die Auswahl der Kontrolle keine Auswirkung auf den Traffic hat. Bei AP- und AT-Aktivitäten hat Ihre Auswahl der Kontrolle sehr wohl Auswirkungen auf den Besucher-Traffic. Daher sollten Sie diese Entscheidung besonders gut überdenken.

Für die AP- und AT-Aktivitäten stehen zwei Optionen zur Verfügung: zufällig bereitgestellte Erlebnisse oder ein bestimmtes Erlebnis.

* **Zufällig bereitgestellt**: Bei einem zufälligen Kontrollerlebnis werden alle Erlebnisse der Aktivität über den Kontrollprozentsatz des Traffics zufällig ohne Berücksichtigung des Besucherprofils ausgeliefert. Diese Kontrolloption bietet eine Antwort auf etwa die Frage: „Wenn ich ein Erlebnis (oder ein Angebot) zufällig für Besucher bereitstelle, ohne ihre Profile zu berücksichtigen, wie hoch ist die Konversionsrate für dieses Erlebnis (oder Angebot)?“ Diese Kontrolloption ähnelt einem A/B-Test innerhalb Ihrer AI-Aktivität. Diese Informationen der nicht personalisierten Konversionsrate für jedes Erlebnis oder Angebot können bei der Analyse der Aktivitätsergebnisse hilfreich sein.

* **Bestimmtes Erlebnis**: Mit einem bestimmten Kontrollerlebnis können Sie den von den Personalisierungsmodellen von Target bereitgestellten Traffic mit einem bestimmten, vom Marketingexperten definierten Erlebnis vergleichen (z. B. Ihrer standardmäßigen Homepage). Mit dieser Option wird Traffic gemäß dem Kontrollprozentsatz zufällig für ausschließlich dieses eine Erlebnis bereitgestellt.

## Festlegen eines bestimmten Erlebnisses als Kontrollelement

1. Sie können beim Erstellen einer [AP-Aktivität](/help/c-activities/t-automated-personalization/create-ap-activity.md) oder einer [AT-Aktivität](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) die Erlebnisse nach Wunsch konfigurieren.
1. Wählen Sie auf der Seite [!UICONTROL Targeting] (Schritt 2 des dreistufigen geleiteten Workflows) das gewünschte Erlebnis als Kontrollelement aus.
1. Geben Sie die gewünschte Traffic-Zuordnung für das Kontrollerlebnis und die anderen Erlebnisse an.

   Je nach Erlebniskontrollart sind 10 % bis 30 % empfehlenswert.

1. Fahren Sie mit der Seite [!UICONTROL Ziele und Einstellungen] fort.

## Bekannte Einschränkungen und Überlegungen

Beachten Sie Folgendes, wenn Sie ein bestimmtes Erlebnis als Kontrolle verwenden:

* Es ist nicht empfehlenswert, das Kontrollerlebnis in einer bereits aktiven Aktivität zu ändern. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten aufgeführt (auch wenn ältere Berichte auf einem anderen Erlebnis basieren).
* Es wird nicht empfohlen, das Kontrollerlebnis zu löschen.
* Es wird nicht empfohlen, eine große Anzahl neuer Angebote/Erlebnisse zu einer aktiven Aktivität mit einem bestimmten Erlebnis hinzuzufügen.
* Es wird nicht empfohlen, in AP-Aktivitäten Targeting zum Kontrollerlebnis hinzuzufügen, durch das die Audience weiter eingeschränkt wird.
* Wenn ein bestimmtes Erlebnis ausgewählt ist, sind in Berichten auf Angebotsebene *KEINE* Steigerungs- und Konfidenzinformationen in AP-Aktivitäten verfügbar. Informationen zu Steigerung und Konfidenz sind für die AP-Aktivität auf der gesamten Traffic-Ebene „Zielgruppe“ verglichen mit „Kontrolle“ verfügbar. Informationen zu Steigerung und Konfidenz sind verfügbar, wenn als Kontrolle „zufällig“ ausgewählt ist. Dies liegt daran, dass das Vergleichen der Konversionsrate eines bestimmten Erlebnisses mit der Konversionsrate eines Angebots aufgrund der unterschiedlichen Einheiten nicht logisch ist. Die in einer AT-Aktivität verfügbaren Informationen sind gleich, unabhängig davon, welche Art von Kontrolle ausgewählt ist.
* Da der gesamte Kontroll-Traffic zu einem einzelnen Erlebnis oder Angebotsset geleitet wird, wenn Sie das Erlebnis als Kontrolle auswählen (im Vergleich zur zufälligen Methode, wo das Volumen des Kontroll-Traffics auf die Anzahl der Erlebnisse oder Angebote in Ihrer Aktivität aufgeteilt ist), benötigen Sie im Allgemeinen weniger Traffic, der zur Kontrolle geleitet wird. Es wird empfohlen, mit 10 % zu beginnen.
* Wenn Sie eine der folgenden Handlungen bei einer aktiven Aktivität mit einem bestimmten Erlebnis als Kontrollelement ausführen, wird die Kontrolle automatisch auf zufällig ausgelieferte Erlebnisse geändert (anstelle des zuvor ausgewählten bestimmten Erlebnisses):

   * Ein Erlebnis löschen
   * Einen Ort oder ein Angebot entfernen (nur AP)
   * Ein Erlebnis manuell durch das Entfernen doppelter Angebote oder über eine Ausschlussgruppe (nur AP) ausschließen

