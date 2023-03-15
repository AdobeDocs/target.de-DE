---
keywords: Erlebnis;Kontrolle;automatisierte Personalisierung;automatisches Targeting
description: Erfahren Sie, wie Sie ein Erlebnis auswählen, das beim Erstellen einer Automated Personalization- (AP) oder automatischen Targeting-Aktivität in Adobe Target als Kontrolle verwendet werden soll.
title: Wie kann ich ein bestimmtes Erlebnis als Kontrollelement in einer AP-Aktivität verwenden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 82%

---

# Wählen Sie das Steuerelement für Automated Personalization oder die automatische Targeting-Aktivität aus

Sie können beim Erstellen einer [automatisierten Personalisierung](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) auswählen, ob ein zufälliges oder ein bestimmtes Erlebnis als Kontrollelement verwendet werden soll.

Mit dieser Funktion können Sie den Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu den entsprechenden Erlebnissen leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem Kontrollerlebnis vergleichen und auswerten.

Die Optionen zum Festlegen eines Kontrollelements bei AP- und AT-Aktivitäten unterscheiden sich geringfügig von anderen Aktivitätstypen. In einem manuellen A/B-Test können Sie ändern, was in den Berichten als Ihre Kontrolle angezeigt wird, und die Steigerung wird anhand der Konversionsrate dieses Kontrollerlebnisses berechnet. Sie können diese Änderung einfach vornehmen, da der Traffic per Zufall an jedes der Erlebnisse geleitet wird, die Sie in Ihre Aktivität eingeschlossen haben, unabhängig davon, wie die Kontrolle ursprünglich eingestellt ist. Mit anderen Worten: Die Auswahl der Kontrolle hat keine Auswirkungen auf die Art und Weise, wie Traffic bereitgestellt wird. Bei AP- und AT-Aktivitäten hat Ihre Auswahl der Kontrolle sehr wohl Auswirkungen auf den Besucher-Traffic. Daher sollten Sie diese Entscheidung besonders gut überdenken.

Für die AP- und AT-Aktivitäten stehen zwei Optionen zur Verfügung: zufällig bereitgestellte Erlebnisse oder ein bestimmtes Erlebnis.

* **Zufällig bereitgestellt**: Für eine zufällige Kontrolle stellt der Kontrollprozentsatz des Traffics zufällig alle Erlebnisse in der Aktivität bereit, ohne das Profil des Besuchers zu berücksichtigen. Sie können sich das Steuerelement als Hilfe bei der Beantwortung der Frage vorstellen: &quot;Wenn ich ein Erlebnis (oder Angebot) nur zufällig an Besucher weitergebe und deren Profile nicht berücksichtige, wie hoch ist die Konversionsrate für dieses Erlebnis (oder Angebot)?&quot; Diese Kontrolloption ähnelt einem A/B-Test innerhalb Ihrer AI-Aktivität. Diese Informationen der nicht personalisierten Konversionsrate für jedes Erlebnis oder Angebot können bei der Analyse der Aktivitätsergebnisse hilfreich sein.

* **Bestimmtes Erlebnis**: Mit einem bestimmten Erlebnissteuerelement können Sie Ihren von den Target-Personalisierungsmodellen bereitgestellten Traffic mit einem bestimmten Erlebnis vergleichen, das vom Marketingexperten definiert wurde (z. B. Ihrer standardmäßigen Homepage). Mit dieser Option wird Traffic gemäß dem Kontrollprozentsatz zufällig für ausschließlich dieses eine Erlebnis bereitgestellt.

## Festlegen eines bestimmten Erlebnisses als Kontrollelement

1. Sie können beim Erstellen einer [AP-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) oder einer [AT-Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) die Erlebnisse nach Wunsch konfigurieren.
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
