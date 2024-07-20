---
keywords: Erlebnis;Kontrolle;automatisierte Personalisierung;automatisches Targeting
description: Erfahren Sie, wie Sie beim Erstellen einer [!UICONTROL Automated Personalization] (AP)- oder [!UICONTROL Auto-Target]-Aktivität in  [!DNL Adobe Target] ein Kontrollerlebnis auswählen.
title: Wie kann ich ein bestimmtes Erlebnis als Kontrolle in einer [!UICONTROL Automated Personalization] -Aktivität verwenden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 29f8c19e24443e84b8d900f630495d163530f80e
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 42%

---

# Wählen Sie das Steuerelement für Ihre [!UICONTROL Automated Personalization] - oder [!UICONTROL Auto-Target] -Aktivität

Sie können beim Erstellen einer [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) - oder [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) -Aktivität ein zufällig bereitgestelltes Erlebnis oder ein bestimmtes Erlebnis als Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu den entsprechenden Erlebnissen leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem Kontrollerlebnis vergleichen und auswerten.

Die Optionen zum Festlegen eines Steuerelements in den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] unterscheiden sich geringfügig von anderen Aktivitätstypen. In einem manuellen [!UICONTROL A/B Test] können Sie ändern, was in Berichten als Kontrolle angezeigt wird, und die Steigerung wird anhand der Konversionsrate dieses Kontrollerlebnisses berechnet. Sie können diese Änderung einfach vornehmen, da der Traffic per Zufall an jedes der Erlebnisse geleitet wird, die Sie in Ihre Aktivität eingeschlossen haben, unabhängig davon, wie die Kontrolle ursprünglich eingestellt ist. Mit anderen Worten: Die Auswahl der Kontrolle hat keine Auswirkungen auf die Art und Weise, wie Traffic bereitgestellt wird. Bei den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] wirkt sich Ihre Entscheidung, was als Kontrolle ausgewählt werden soll, darauf aus, wie der Besucher-Traffic bereitgestellt wird. Daher müssen Sie Ihre Entscheidung sorgfältiger überdenken.

In Ihren [!UICONTROL Automated Personalization] - und [!UICONTROL Auto-Target] -Aktivitäten stehen Ihnen zwei Optionen zur Verfügung:

* **Zufällig bereitgestellt**: Für eine zufällige Kontrolle stellt der Kontrollprozentsatz des Traffics zufällig alle Erlebnisse in der Aktivität bereit, ohne das Profil des Besuchers zu berücksichtigen. Sie können sich das Steuerelement als Hilfe bei der Beantwortung der Frage vorstellen: &quot;Wenn ich ein Erlebnis (oder Angebot) nur zufällig an Besucher weitergebe und deren Profile nicht berücksichtige, wie hoch ist die Konversionsrate für dieses Erlebnis (oder Angebot)?&quot; Das Steuerelement entspricht einem [!UICONTROL A/B Test] innerhalb Ihrer KI-Aktivität. Diese Informationen der nicht personalisierten Konversionsrate für jedes Erlebnis oder Angebot können bei der Analyse der Aktivitätsergebnisse hilfreich sein.

* **Bestimmtes Erlebnis**: Mit einem bestimmten Erlebnissteuerelement können Sie Ihren von [!DNL Target]-Personalisierungsmodellen bereitgestellten Traffic mit einem bestimmten Erlebnis vergleichen, das von Marketingexperten definiert wurde (z. B. Ihrer standardmäßigen Homepage). Mit dieser Option wird Traffic gemäß dem Kontrollprozentsatz zufällig für ausschließlich dieses eine Erlebnis bereitgestellt.

## Festlegen eines bestimmten Erlebnisses als Kontrollelement

1. Konfigurieren Sie beim Erstellen oder Bearbeiten einer [[!UICONTROL Automated Personalization] -Aktivität ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) oder einer [[!UICONTROL Auto-Target] -Aktivität](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) die Erlebnisse nach Bedarf.
1. Wählen Sie auf der Seite [!UICONTROL Targeting] (Schritt 2 des dreiteiligen geführten Workflows) das gewünschte Erlebnis als Kontrolle aus.
1. Geben Sie die gewünschte Traffic-Zuordnung für das Kontrollerlebnis und die anderen Erlebnisse an.

   Je nach Erlebniskontrollart sind 10 % bis 30 % empfehlenswert.

1. Fahren Sie mit der Seite [!UICONTROL Goals & Settings] fort.

## Bekannte Einschränkungen und Überlegungen

Beachten Sie beim Verwenden eines bestimmten Erlebnisses als Kontrolle die folgenden Punkte:

* Es ist nicht empfehlenswert, das Kontrollerlebnis in einer bereits aktiven Aktivität zu ändern. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten aufgeführt (auch wenn ältere Berichte auf einem anderen Erlebnis basieren).
* Es wird nicht empfohlen, das Kontrollerlebnis zu löschen.
* Hinzufügen vieler neuer Angebote oder Erlebnisse zu einer Live-Aktivität mit einem bestimmten Erlebnis, da das Steuerelement nicht empfohlen wird.
* Bei [!UICONTROL Automated Personalization] -Aktivitäten, einschließlich Targeting für das Kontrollerlebnis, das die Besucher weiter einschränken könnte, die dieses Erlebnis sehen können, wird nicht empfohlen.
* Bei [!UICONTROL Automated Personalization] -Aktivitäten sind Steigerungs- und Konfidenzinformationen im Bericht auf Angebotsebene *NOT* verfügbar, wenn ein bestimmtes Erlebnis ausgewählt ist. Informationen zu Steigerung und Konfidenz sind auf der gesamten Traffic-Ebene &quot;Zielgruppe&quot;und &quot;Kontrolle&quot;für die Aktivität [!UICONTROL Automated Personalization] verfügbar. Informationen zu Steigerung und Konfidenz sind verfügbar, wenn als Kontrolle „zufällig“ ausgewählt ist. Dies liegt daran, dass das Vergleichen der Konversionsrate eines bestimmten Erlebnisses mit der Konversionsrate eines Angebots aufgrund der unterschiedlichen Einheiten nicht logisch ist. Die in einer [!UICONTROL Auto-Target] -Aktivität verfügbaren Informationen sind unabhängig vom ausgewählten Kontrolltyp identisch.
* Da der gesamte Kontroll-Traffic zu einem einzelnen Erlebnis oder Angebotsset geleitet wird, wenn Sie das Erlebnis als Kontrolle auswählen (im Vergleich zur zufälligen Methode, wo das Volumen des Kontroll-Traffics auf die Anzahl der Erlebnisse oder Angebote in Ihrer Aktivität aufgeteilt ist), benötigen Sie im Allgemeinen weniger Traffic, der zur Kontrolle geleitet wird. Es wird empfohlen, mit 10 % zu beginnen.
* Wenn Sie eine der folgenden Handlungen bei einer aktiven Aktivität mit einem bestimmten Erlebnis als Kontrollelement ausführen, wird die Kontrolle automatisch auf zufällig ausgelieferte Erlebnisse geändert (anstelle des zuvor ausgewählten bestimmten Erlebnisses):

   * Ein Erlebnis löschen
   * Einen Ort oder ein Angebot entfernen ([!UICONTROL Automated Personalization] nur)
   * Manuelles Ausschließen eines Erlebnisses durch Entfernen doppelter Angebote oder über eine Ausschlussgruppe ([!UICONTROL Automated Personalization] nur)
