---
keywords: Erlebnis;Kontrolle;automatisierte Personalisierung;automatisches Targeting
description: Erfahren Sie, wie Sie beim Erstellen einer [!UICONTROL Automated Personalization] (AP)- oder [!UICONTROL Auto-Target]-Aktivität in [!DNL Adobe Target] ein Erlebnis als Steuerelement auswählen.
title: Wie kann ich ein bestimmtes Erlebnis als Kontrolle in einer [!UICONTROL Automated Personalization]-Aktivität verwenden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
TQID: 'https://experienceleague.adobe.com/a-lIVDWxeAi-VCp7-lLD-zaClCDCKJGfa25XMKF0vZA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 3%
---
# Auswählen des Kontrollerlebnisses {#experience-as-control}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie das Steuerelement einer **[!UICONTROL Automated Personalization]**- oder **[!UICONTROL Automatisches Targeting]**-Aktivität auswählen und was Sie bei der Verwendung eines bestimmten Erlebnisses als Steuerelement beachten sollten.

>[!ENDSHADEBOX]

Sie können beim Erstellen einer [**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview) (AP)- oder [**[!UICONTROL Automatisches Targeting]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT)-Aktivität ein zufällig bereitgestelltes Erlebnis oder ein bestimmtes Erlebnis als Kontrolle. Der Kontroll-Traffic wird basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentsatz an die relevanten Erlebnisse weitergeleitet, damit Sie die Leistungsberichte des personalisierten Traffics mit dem Kontroll-Traffic vergleichen können.

In einem manuellen **[!UICONTROL A/B-Test]** können Sie ändern, was in Berichten als Kontrolle angezeigt wird. Die Steigerung wird aus diesem Erlebnis berechnet, da der Traffic nach dem Zufallsprinzip allen Erlebnissen bereitgestellt wird, unabhängig von der Kontrolle. In den Aktivitäten {]**}Automated Personalization und**[!UICONTROL  Automatisches Targeting ]**wirkt sich das Steuerelement nicht darauf aus, wie der Besucher-Traffic bereitgestellt wird. Wählen Sie ihn daher sorgfältig aus.**[!UICONTROL 

Für das Steuerelement stehen zwei Optionen zur Verfügung:

* **Zufällig bereitgestellt:** Der Kontrollprozentsatz des Traffics stellt nach dem Zufallsprinzip alle Erlebnisse in der Aktivität bereit, ohne das Profil des Besuchers zu berücksichtigen. Sie funktioniert wie ein **[!UICONTROL A/B-]** innerhalb Ihrer Aktivität und zeigt die nicht personalisierte Konversionsrate der einzelnen Erlebnisse oder Angebote an, wodurch Sie die Ergebnisse analysieren können.

* **Spezifisches Erlebnis:** Der Kontrollprozentsatz des Traffics dient nach dem Zufallsprinzip nur diesem einen Erlebnis. Mit dieser Option können Sie den von den [!DNL Target] Personalisierungsmodellen bereitgestellten Traffic mit einem bestimmten Erlebnis vergleichen, das Sie definieren, z. B. Ihre standardmäßige Homepage.

## Zu beachten {#considerations}

Beachten Sie bei der Verwendung eines bestimmten Erlebnisses als Steuerelement die folgenden Punkte:

* Es wird nicht empfohlen, das Kontrollerlebnis in einer bereits aktiven Aktivität zu ändern. Das zuletzt ausgewählte Kontrollerlebnis wird in Berichten benannt, auch wenn ältere Berichte auf einem anderen Erlebnis basieren.

* Das Löschen des Kontrollerlebnisses wird nicht empfohlen.

* Hinzufügen vieler neuer Angebote oder Erlebnisse zu einer Live-Aktivität mit einem bestimmten Erlebnis, da das Steuerelement nicht empfohlen wird.

* In **[!UICONTROL Automated Personalization]**-Aktivitäten, einschließlich der Zielgruppenbestimmung für das Kontrollerlebnis, die weiter einschränken könnte, wer sehen kann, dass das Erlebnis nicht empfohlen wird.

* In **[!UICONTROL Automated Personalization]**-Aktivitäten sind die Informationen über Steigerung *Konfidenz nicht* im Bericht auf Angebotsebene verfügbar, wenn ein bestimmtes Erlebnis ausgewählt wurde. Dies liegt daran, dass der Vergleich der Konversionsrate eines bestimmten Erlebnisses mit der Konversionsrate eines Angebots aufgrund des Unterschieds in den Einheiten nicht logisch ist. Informationen zu Steigerung und Konfidenz sind auf der gesamten Traffic-Stufe „Targeting“ im Vergleich zur Traffic-Stufe „Kontrolle“ für die Aktivität und auf allen Ebenen verfügbar, wenn „Zufällig“ als Kontrolle ausgewählt ist. Die in einer Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** verfügbaren Informationen sind identisch, unabhängig davon, welcher Kontrolltyp ausgewählt ist.

* Wenn Sie ein bestimmtes Erlebnis als Kontrolle auswählen, geht der gesamte Kontroll-Traffic an ein einzelnes Erlebnis oder an eine Gruppe von Angeboten. Mit einer zufälligen Steuerung wird der Kontroll-Traffic auf die Anzahl der Erlebnisse oder Angebote in Ihrer Aktivität aufgeteilt. Daher benötigen Sie im Allgemeinen nicht so viel Traffic, der zum Steuerelement mit einem bestimmten Erlebnis fließen soll. Es wird empfohlen, mit 10 % zu beginnen.

* Wenn Sie eine der folgenden Aktionen auf eine Live-Aktivität mit einem bestimmten Erlebnis als Kontrolle anwenden, wird das Kontrollerlebnis automatisch auf die zufällig bereitgestellten Erlebnisse zurückgesetzt (anstelle des zuvor ausgewählten spezifischen Erlebnisses):

  * Erlebnis löschen.
  * Einen Speicherort oder ein Angebot entfernen (nur **[!UICONTROL Automated Personalization]**).
  * Ein Erlebnis manuell ausschließen, indem doppelte Angebote entfernt werden, oder durch eine Ausschlussgruppe (nur **[!UICONTROL Automated Personalization]**).


## Festlegen eines bestimmten Erlebnisses als Kontrollelement {#specify-control}

Wenn Sie ein bestimmtes Erlebnis als Kontrolle angeben, erhält der personalisierte Traffic ein bekanntes Erlebnis, mit dem er in den Berichten der Aktivität verglichen werden kann, z. B. das aktuelle Standarderlebnis.

1. Konfigurieren Sie beim Erstellen oder Bearbeiten einer [**[!UICONTROL Automated Personalization ]**-](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) oder einer [**[!UICONTROL automatischen Targeting]**-](/help/main/c-activities/auto-target/create-auto-target.md#create-auto-target-activity) die Erlebnisse nach Bedarf.

1. Klicken Sie auf der **[!UICONTROL Targeting]**-Seite (Schritt 2 des dreiteiligen geleiteten Workflows) auf das Steuerelementerlebnis, um die **[!UICONTROL Kontrolle]**-Optionen im rechten Bereich anzuzeigen.

   ![Systemsteuerung](/help/main/c-activities/t-automated-personalization/assets/control.png)

1. Wählen Sie in **[!UICONTROL Dropdown]** Liste „Kontrolle“ die Option **[!UICONTROL Zufälliges Erlebnis]** oder wählen Sie das Erlebnis aus, das Sie als Steuerelement verwenden möchten.

1. Klicken Sie auf **[!UICONTROL Traffic-Zuordnungs]**-Steuerelement und geben Sie dann die Traffic-Zuordnung für das Kontrollerlebnis und die anderen Erlebnisse an.

   ![Traffic-Zuordnungsleiste](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation.png)

   Je nach Erlebniskontrollart sind 10 % bis 30 % empfehlenswert.

1. Fahren Sie mit der Seite **[!UICONTROL Ziele und Einstellungen]** fort.

Sobald die Aktivität live ist, wird in den Berichten der personalisierte Traffic mit dem von Ihnen ausgewählten Kontrollerlebnis verglichen. Beachten Sie die [Überlegungen](#considerations) bevor Sie eine Live-Aktivität ändern, da einige Änderungen das Steuerelement automatisch auf zufällig bereitgestellte Erlebnisse zurücksetzen.
