---
keywords: Erlebnis;Kontrolle;automatisierte Personalisierung;automatisches Targeting
description: Erfahren Sie, wie Sie beim Erstellen einer [!UICONTROL Automated Personalization] (AP) oder [!UICONTROL Auto-Target] Aktivität in ein Erlebnis als Steuerelement auswählen [!DNL Adobe Target].
title: Wie kann ich ein bestimmtes Erlebnis als Kontrolle in einer [!UICONTROL Automated Personalization] verwenden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 39%

---

# Wählen Sie das Steuerelement für Ihre [!UICONTROL Automated Personalization] oder [!UICONTROL Auto-Target] Aktivität aus

Sie können beim Erstellen einer [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT)-Aktivität ein zufällig bereitgestelltes Erlebnis oder ein bestimmtes Erlebnis als Kontrolle auswählen.

Mit dieser Funktion können Sie den Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu den entsprechenden Erlebnissen leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem Kontrollerlebnis vergleichen und auswerten.

Die Optionen zum Festlegen eines Steuerelements in [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] Aktivitäten unterscheiden sich geringfügig von anderen Aktivitätstypen. In einem manuellen [!UICONTROL A/B Test] können Sie ändern, was in Berichten als Steuerelement angezeigt wird. Die Steigerung wird basierend auf der Konversionsrate dieses Steuerelementerlebnisses berechnet. Sie können diese Änderung einfach vornehmen, da der Traffic per Zufall an jedes der Erlebnisse geleitet wird, die Sie in Ihre Aktivität eingeschlossen haben, unabhängig davon, wie die Kontrolle ursprünglich eingestellt ist. Mit anderen Worten: Die Auswahl des Steuerelements hat keine Auswirkungen darauf, wie der Traffic bereitgestellt wird. Bei [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target]-Aktivitäten wirkt sich Ihre Entscheidung darüber, was ausgewählt werden soll, da das Steuerelement Auswirkungen darauf hat, wie der Besucher-Traffic bereitgestellt wird. Daher müssen Sie sorgfältiger über Ihre Entscheidung nachdenken.

In Ihren [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target]-Aktivitäten stehen zwei Optionen für das Steuerelement zur Verfügung:

* **Zufällig bereitgestellt**: Für eine zufällige Kontrolle stellt der Kontrollprozentsatz des Traffics nach dem Zufallsprinzip alle Erlebnisse in der Aktivität bereit, ohne das Besucherprofil zu berücksichtigen. Sie können sich das Steuerelement als hilfreich bei der Beantwortung der Frage vorstellen: „Wenn ich Besuchern ein Erlebnis (oder ein Angebot) nach dem Zufallsprinzip bereitstelle und deren Profile nicht berücksichtige, wie hoch ist dann die Konversionsrate für dieses Erlebnis (oder Angebot)?“ Die Steuerung ist wie eine [!UICONTROL A/B Test] innerhalb Ihrer KI-Aktivität. Diese Informationen der nicht personalisierten Konversionsrate für jedes Erlebnis oder Angebot können bei der Analyse der Aktivitätsergebnisse hilfreich sein.

* **Spezifisches Erlebnis**: Mit einem speziellen Erlebnissteuerelement können Sie Ihren Traffic, der von [!DNL Target] Personalisierungsmodellen bereitgestellt wird, mit einem bestimmten von Marketing-Experten definierten Erlebnis vergleichen (z. B. Ihrer standardmäßigen Homepage). Mit dieser Option wird Traffic gemäß dem Kontrollprozentsatz zufällig für ausschließlich dieses eine Erlebnis bereitgestellt.

## Festlegen eines bestimmten Erlebnisses als Kontrollelement

1. Konfigurieren Sie beim Erstellen oder Bearbeiten einer [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) oder [[!UICONTROL Auto-Target] -](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) die Erlebnisse nach Bedarf.
1. Klicken Sie auf der Seite [!UICONTROL Targeting] (Schritt 2 des dreiteiligen geleiteten Workflows) auf das Steuerelement, um [!UICONTROL Control] Optionen im rechten Bereich anzuzeigen.

   ![Systemsteuerung](/help/main/c-activities/t-automated-personalization/assets/control.png)

1. Wählen Sie aus der Dropdown-Liste [!UICONTROL Control] die Option [!UICONTROL Random Experience] oder das gewünschte Erlebnis aus, das Sie für das Steuerelement verwenden möchten.

1. Klicken Sie auf das [!UICONTROL Traffic Allocation] und geben Sie dann die gewünschte Traffic-Zuordnung für das Kontrollerlebnis und die anderen Erlebnisse an.

   ![Traffic-Zuordnungsleiste](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation.png)

   Je nach Erlebniskontrollart sind 10 % bis 30 % empfehlenswert.

1. Fahren Sie mit der Seite [!UICONTROL Goals & Settings] fort.

## Bekannte Einschränkungen und Überlegungen

Beachten Sie bei der Verwendung eines bestimmten Erlebnisses als Steuerelement die folgenden Punkte:

* Es ist nicht empfehlenswert, das Kontrollerlebnis in einer bereits aktiven Aktivität zu ändern. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten aufgeführt (auch wenn ältere Berichte auf einem anderen Erlebnis basieren).
* Es wird nicht empfohlen, das Kontrollerlebnis zu löschen.
* Hinzufügen vieler neuer Angebote oder Erlebnisse zu einer Live-Aktivität mit einem bestimmten Erlebnis, da das Steuerelement nicht empfohlen wird.
* In [!UICONTROL Automated Personalization] Aktivitäten, einschließlich der Zielgruppenbestimmung für das Kontrollerlebnis, die weiter einschränken könnten, wer sehen kann, dass das Erlebnis nicht empfohlen wird.
* In [!UICONTROL Automated Personalization] Aktivitäten sind Steigerung und Konfidenzinformationen *NICHT* im Bericht auf Angebotsebene verfügbar, wenn ein bestimmtes Erlebnis ausgewählt wurde. Informationen zu Steigerung und Konfidenz stehen auf der Traffic-Ebene „Targeting“ im Vergleich zu „Kontrolle“ für die [!UICONTROL Automated Personalization] zur Verfügung. Informationen zu Steigerung und Konfidenz sind verfügbar, wenn als Kontrolle „zufällig“ ausgewählt ist. Dies liegt daran, dass das Vergleichen der Konversionsrate eines bestimmten Erlebnisses mit der Konversionsrate eines Angebots aufgrund der unterschiedlichen Einheiten nicht logisch ist. Die in einer [!UICONTROL Auto-Target] Aktivität verfügbaren Informationen sind identisch, unabhängig davon, welcher Steuerungstyp ausgewählt ist.
* Da der gesamte Kontroll-Traffic zu einem einzelnen Erlebnis oder Angebotsset geleitet wird, wenn Sie das Erlebnis als Kontrolle auswählen (im Vergleich zur zufälligen Methode, wo das Volumen des Kontroll-Traffics auf die Anzahl der Erlebnisse oder Angebote in Ihrer Aktivität aufgeteilt ist), benötigen Sie im Allgemeinen weniger Traffic, der zur Kontrolle geleitet wird. Es wird empfohlen, mit 10 % zu beginnen.
* Wenn Sie eine der folgenden Handlungen bei einer aktiven Aktivität mit einem bestimmten Erlebnis als Kontrollelement ausführen, wird die Kontrolle automatisch auf zufällig ausgelieferte Erlebnisse geändert (anstelle des zuvor ausgewählten bestimmten Erlebnisses):

   * Ein Erlebnis löschen
   * Standort oder Angebot entfernen (nur [!UICONTROL Automated Personalization])
   * Manuelles Ausschließen eines Erlebnisses, indem doppelte Angebote entfernt werden oder eine Ausschlussgruppe verwendet wird (nur [!UICONTROL Automated Personalization])
