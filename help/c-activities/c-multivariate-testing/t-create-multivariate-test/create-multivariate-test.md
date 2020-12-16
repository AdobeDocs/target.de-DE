---
keywords: mvt;multivariate test;multivariate test create;multivariate test creating;mvt create;mvt creating;mvt how;multivariate test how
description: Visual Experience Composer (VEC) in Adobe Target ermöglicht Ihnen, einen Multivarianz-Test (MVT) direkt auf einer für Target aktivierten Seite zu erstellen und Teile der Seite in Target zu verändern.
title: Erstellen eines Multivarianz-Tests
feature: mvt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 97%

---


# Erstellen eines Multivarianz-Tests{#create-a-multivariate-test}

[!UICONTROL Visual Experience Composer ] (VEC) in [!DNL Target] ermöglicht Ihnen, Ihren Test einfach direkt auf einer für Target aktivierten Seite zu erstellen und Teile der Seite in [!DNL Target] zu verändern.

Der Point-and-Click-Editor in Target ermöglicht Ihnen, einen beliebigen Ort auszuwählen und mehrere Angebote hinzuzufügen.

Ein [!UICONTROL Multivariater Test] (MVT) benötigt einen Page-First-Bericht. Anders ausgedrückt bedeutet das, dass der Test auf einer spezifischen URL ausgeführt wird, mit den Erlebnissen, die Sie für diese Seite entwerfen.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Multivarianz-Test]**.

   ![Erstellen eines Multivarianz-Tests](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem Target-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist die [!UICONTROL automatisierte Personalisierung] eine [Target Premium-Funktion](/help/c-intro/intro.md#premium).
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Standard)]** aus.

   ![Erstellen des Dialogfeldes „Multivarianz-Test-Aktivität“](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-mvt-dialog.png)

   >[!NOTE]
   >
   >Informationen zur Problembehebung für den VEC finden Sie bei Bedarf unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die Option [!UICONTROL „Arbeitsplatz auswählen“] in der obigen Abbildung ist eine Funktion von [Target Premium](/help/c-intro/intro.md). Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.

1. (Abhängig von Ihrer Lizenz) Wenn Sie Target Premium-Kunde sind, [wählen Sie einen Arbeitsbereich](/help/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. [Geben Sie die URL](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) für die Seite an, die Sie testen möchten, und klicken Sie anschließend auf **[!UICONTROL Weiter]**.

   >[!NOTE]
   >
   >Verwenden Sie eine vollständige URL einschließlich HTTP oder HTTPS am Anfang.

   Wenn eine Nachricht eingeblendet wird, die Sie dazu auffordert, Ihren Browser für gemischte Inhalte zu aktivieren, folgen Sie den Anweisungen in der Nachricht. Nachdem Sie Ihren Browser für gemischte Inhalte aktiviert haben, beginnen Sie erneut mit Schritt 1.

   Der Visual Experience Composer wird geöffnet.

1. Geben Sie einen Namen für die Aktivität ein.

   ![Feld für Aktivitätsname](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

   Folgende Zeichen sind im Aktivitätsnamen nicht zulässig:

   | Zeichen | Beschreibung |
   |--- |--- |
   | / | Vorwärtsschrägstrich |
   | ? | Fragezeichen |
   | # | Raute |
   | : | Doppelpunkt |
   | = | Gleich |
   | + | Plus |
   | - | Minus |
   | @ | At-Zeichen |

1. [Erstellen Sie die Angebote an jedem Ort](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![Dialogfeld „Text/HTML bearbeiten“](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Sie können folgende Angebotsarten hinzufügen:

   * HTML
   * Bild
   * Text

1. Klicken Sie auf **[!UICONTROL Vorschau]**, um [eine Vorschau Ihrer Erlebnisse anzuzeigen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Vorschau von Erlebnissen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   Sie können jedes Erlebnis ansehen und diejenigen, die Sie nicht in Ihren Test aufnehmen möchten, ausschließen. Um ein oder mehrere Erlebnisse auszuschließen, wählen Sie die jeweiligen Kontrollkästchen aus und klicken Sie auf **[!UICONTROL Ausschließen]**.

   ![Erlebnisse ausschließen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Verwenden Sie die Traffic-Schätzung](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um die Umsetzbarkeit Ihres Testplans zu überprüfen.

   ![Traffic-Anzeige](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   Die folgende Abbildung zeigt an, dass die Aktivität über zu wenig Traffic verfügt.

   ![](assets/estimator.png)

   Die folgende Abbildung zeigt an, dass die Aktivität über zu wenig Traffic verfügt.

   ![](assets/estimator2.png)

1. Klicken Sie auf **[!UICONTROL Weiter]**, um zur Seite [!UICONTROL Targeting] fortzufahren.

1. Wählen Sie die Zielgruppe und den Prozentsatz qualifizierter Besucher aus, die an der Aktivität teilnehmen sollen.

   ![Targeting-Seite in der MVT-Aktivität](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Prüfen Sie die Testzusammenfassung](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) und nehmen Sie etwaige Änderungen vor. Klicken Sie dann auf **[!UICONTROL Weiter]**.

1. [Legen Sie Ziele und Einstellungen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für den Test fest.

1. Klicken Sie auf **[!UICONTROL Speichern und Schließen]**, um die Aktivität zu erstellen.

## Schulungsvideo: Erstellen von Multivarianz-Tests (9:25) ![Tutorialzeichen](/help/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten Target-Arbeitsablaufs mit drei Schritten ein Multivarianz-Test geplant und erstellt wird.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395)
