---
keywords: Erlebnis;Kontrolle;automatisierte Personalisierung;automatisches Targeting
description: Erfahren Sie, wie Sie beim Erstellen eines [!UICONTROL Automated Personalization] (AP) oder [!UICONTROL Automatisches Targeting] Aktivität in [!DNL Adobe Target].
title: Wie kann ich ein bestimmtes Erlebnis als Kontrolle in einem [!UICONTROL Automated Personalization] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 29f8c19e24443e84b8d900f630495d163530f80e
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 42%

---

# Wählen Sie das Steuerelement für Ihre [!UICONTROL Automated Personalization] oder [!UICONTROL Automatisches Targeting] activity

Sie können beim Erstellen eines [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder [[!UICONTROL Automatisches Targeting]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Mit dieser Funktion können Sie den Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu den entsprechenden Erlebnissen leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem Kontrollerlebnis vergleichen und auswerten.

Die Optionen zum Festlegen eines Steuerelements in [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] -Aktivitäten unterscheiden sich geringfügig von anderen Aktivitätstypen. In einem Handbuch [!UICONTROL A/B-Test]können Sie ändern, welche Berichte als Kontrolle angezeigt werden, und die Steigerung wird anhand der Konversionsrate des Kontrollerlebnisses berechnet. Sie können diese Änderung einfach vornehmen, da der Traffic per Zufall an jedes der Erlebnisse geleitet wird, die Sie in Ihre Aktivität eingeschlossen haben, unabhängig davon, wie die Kontrolle ursprünglich eingestellt ist. Mit anderen Worten: Die Auswahl der Kontrolle hat keine Auswirkungen auf die Art und Weise, wie Traffic bereitgestellt wird. In [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] -Aktivitäten hat Ihre Entscheidung, was als Kontrolle ausgewählt werden soll, Auswirkungen auf die Bereitstellung des Besucher-Traffics. Daher müssen Sie Ihre Entscheidung sorgfältiger überdenken.

Es stehen zwei Optionen zur Verfügung, mit denen Sie Ihre [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] Aktivitäten:

* **Zufällig bereitgestellt**: Bei einer zufälligen Kontrolle stellt der Kontrollprozentsatz des Traffics zufällig alle Erlebnisse in der Aktivität bereit, ohne das Profil des Besuchers zu berücksichtigen. Sie können sich das Steuerelement als Hilfe bei der Beantwortung der Frage vorstellen: &quot;Wenn ich ein Erlebnis (oder Angebot) nur zufällig an Besucher weitergebe und deren Profile nicht berücksichtige, wie hoch ist die Konversionsrate für dieses Erlebnis (oder Angebot)?&quot; Die Steuerung ist wie eine [!UICONTROL A/B-Test] innerhalb Ihrer KI-Aktivität. Diese Informationen der nicht personalisierten Konversionsrate für jedes Erlebnis oder Angebot können bei der Analyse der Aktivitätsergebnisse hilfreich sein.

* **Bestimmtes Erlebnis**: Ein spezifisches Erlebnissteuerelement ermöglicht den Vergleich des von [!DNL Target] Personalisierungsmodelle an ein bestimmtes Erlebnis anpassen, das von Marketingexperten definiert wurde (z. B. Ihre standardmäßige Startseite). Mit dieser Option wird Traffic gemäß dem Kontrollprozentsatz zufällig für ausschließlich dieses eine Erlebnis bereitgestellt.

## Festlegen eines bestimmten Erlebnisses als Kontrollelement

1. Beim Erstellen oder Bearbeiten einer [[!UICONTROL Automated Personalization] activity](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) oder [[!UICONTROL Automatisches Targeting] activity](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), konfigurieren Sie die Erlebnisse nach Bedarf.
1. Wählen Sie auf der Seite [!UICONTROL Targeting] (Schritt 2 des dreistufigen geleiteten Workflows) das gewünschte Erlebnis als Kontrollelement aus.
1. Geben Sie die gewünschte Traffic-Zuordnung für das Kontrollerlebnis und die anderen Erlebnisse an.

   Je nach Erlebniskontrollart sind 10 % bis 30 % empfehlenswert.

1. Fahren Sie mit der Seite [!UICONTROL Ziele und Einstellungen] fort.

## Bekannte Einschränkungen und Überlegungen

Beachten Sie beim Verwenden eines bestimmten Erlebnisses als Kontrolle die folgenden Punkte:

* Es ist nicht empfehlenswert, das Kontrollerlebnis in einer bereits aktiven Aktivität zu ändern. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten aufgeführt (auch wenn ältere Berichte auf einem anderen Erlebnis basieren).
* Es wird nicht empfohlen, das Kontrollerlebnis zu löschen.
* Hinzufügen vieler neuer Angebote oder Erlebnisse zu einer Live-Aktivität mit einem bestimmten Erlebnis, da das Steuerelement nicht empfohlen wird.
* In [!UICONTROL Automated Personalization] -Aktivitäten, einschließlich Targeting für das Kontrollerlebnis, das die Besucher, die dieses Erlebnis sehen können, weiter einschränken könnte, wird nicht empfohlen.
* In [!UICONTROL Automated Personalization] Aktivitäten, Steigerung und Konfidenzinformationen sind *NOT* im Bericht auf Angebotsebene verfügbar, wenn ein bestimmtes Erlebnis ausgewählt ist. Informationen zu Steigerung und Konfidenz sind auf der gesamten Traffic-Ebene &quot;Zielgruppe&quot;und &quot;Kontrolle&quot;für die Variable [!UICONTROL Automated Personalization] -Aktivität. Informationen zu Steigerung und Konfidenz sind verfügbar, wenn als Kontrolle „zufällig“ ausgewählt ist. Dies liegt daran, dass das Vergleichen der Konversionsrate eines bestimmten Erlebnisses mit der Konversionsrate eines Angebots aufgrund der unterschiedlichen Einheiten nicht logisch ist. Die in einer [!UICONTROL Automatisches Targeting] -Aktivität ist unabhängig vom gewählten Kontrolltyp identisch.
* Da der gesamte Kontroll-Traffic zu einem einzelnen Erlebnis oder Angebotsset geleitet wird, wenn Sie das Erlebnis als Kontrolle auswählen (im Vergleich zur zufälligen Methode, wo das Volumen des Kontroll-Traffics auf die Anzahl der Erlebnisse oder Angebote in Ihrer Aktivität aufgeteilt ist), benötigen Sie im Allgemeinen weniger Traffic, der zur Kontrolle geleitet wird. Es wird empfohlen, mit 10 % zu beginnen.
* Wenn Sie eine der folgenden Handlungen bei einer aktiven Aktivität mit einem bestimmten Erlebnis als Kontrollelement ausführen, wird die Kontrolle automatisch auf zufällig ausgelieferte Erlebnisse geändert (anstelle des zuvor ausgewählten bestimmten Erlebnisses):

   * Ein Erlebnis löschen
   * Ort oder Angebot entfernen ([!UICONTROL Automated Personalization] nur)
   * Ein Erlebnis manuell ausschließen, durch Entfernen doppelter Angebote oder über eine Ausschlussgruppe ([!UICONTROL Automated Personalization] nur)
