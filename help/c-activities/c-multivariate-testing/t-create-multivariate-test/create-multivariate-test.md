---
description: Visual Experience Composer in Target ermöglicht Ihnen, Ihren Test einfach direkt auf einer targetfähigen Seite zu erstellen und Teile der Seite in Target zu verändern.
keywords: MVT;Multivariater Test;Multivariater Test erstellen;Erstellen von Multivariater Tests;MVT-Erstellung;Erstellen von MVT;wie MVT;wie Multivariater Tests
seo-description: Visual Experience Composer in Target ermöglicht Ihnen, Ihren Test einfach direkt auf einer targetfähigen Seite zu erstellen und Teile der Seite in Target zu verändern.
seo-title: Erstellen eines Multivarianz-Tests
solution: Target
title: Erstellen eines Multivarianz-Tests
uuid: 876441bd-d841-4974-b1ec-3ad7cb6ef3ee
translation-type: tm+mt
source-git-commit: c6085fae6428cb837eed6eadd778140687348817

---


# Erstellen eines Multivarianz-Tests{#create-a-multivariate-test}

Mit [!UICONTROL Visual Experience Composer] (VEC) ist [!DNL Target] es ganz einfach, Ihren Test direkt auf einer Target-fähigen Seite zu erstellen und Teile der Seite zu [!DNL Target]verändern.

Der Point-and-Click-Editor in Target ermöglicht Ihnen, einen beliebigen Ort auszuwählen und mehrere Angebote hinzuzufügen.

Der [!UICONTROL Multivarianz-Test] (MVT) akzeptiert einen Seitenbericht. Anders ausgedrückt bedeutet das, dass der Test auf einer spezifischen URL ausgeführt wird, mit den Erlebnissen, die Sie für diese Seite entwerfen.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]** &gt; **[!UICONTROL Multivarianz-Test]**.

   ![](assets/create_mvt.png)

1. (Bedingt) Wenn Sie Target Premium-Kunde sind, [wählen Sie eine Arbeitsfläche](/help/administrating-target/c-user-management/property-channel/property-channel.md)aus.

   >[!NOTE]
   >
   >Die Option [!UICONTROL &quot;Arbeitsplatz] auswählen&quot; in der obigen Abbildung ist eine [Target Premium](/help/c-intro/intro.md) -Funktion. Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.]

1. [Geben Sie die URL](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) für die Seite an, die Sie testen möchten, und klicken Sie auf **[!UICONTROL Weiter]**.

   >[!NOTE]
   >
   >Verwenden Sie eine vollständige URL einschließlich HTTP oder HTTPS am Anfang.

   Wenn eine Nachricht eingeblendet wird, die Sie dazu auffordert, Ihren Browser für gemischte Inhalte zu aktivieren, folgen Sie den Anweisungen in der Nachricht. Nachdem Sie Ihren Browser für gemischte Inhalte aktiviert haben, beginnen Sie erneut mit Schritt 1.

   Der Visual Experience Composer wird geöffnet.

   Informationen zur Problembehebung für den VEC finden Sie bei Bedarf unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

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

1. [Erstellen Sie die Angebote an jedem Ort](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![Text/HTML bearbeiten, Dialogfeld](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Sie können folgende Angebotsarten hinzufügen:

   * HTML
   * Bild
   * Text

1. Klicken **[!UICONTROL Sie auf Vorschau]** , um [eine Vorschau Ihrer Erlebnisse anzuzeigen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![](assets/preview.png)

   Sie können jedes Erlebnis ansehen und diejenigen, die Sie nicht in Ihren Test aufnehmen möchten, ausschließen.

1. [Verwenden Sie die Traffic-Schätzung](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um die Umsetzbarkeit Ihres Testplans zu überprüfen.

   ![](assets/estimator.png)  ![](assets/estimator2.png)

1. Klicken **Sie auf [! UICONTROL Next** , um auf [!UICONTROL die Targeting] -Seite zu gelangen.]

1. Wählen Sie die Zielgruppe und den Prozentsatz qualifizierter Besucher aus, die an der Aktivität teilnehmen sollen.

   ![Targeting-Seite in der MVT-Aktivität](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Prüfen Sie die Testzusammenfassung](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) und nehmen Sie etwaig gewünschte Änderungen vor. Klicken Sie dann auf **[!UICONTROL Weiter]**.

1. [Legen Sie Ziele und Einstellungen](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für den Test fest.

1. Klicken Sie auf **[!UICONTROL Speichern und Schließen]**, um die Aktivität zu erstellen.

## Schulungsvideo: Erstellen von multivarianten Tests (9:25)

In diesem Video wird gezeigt, wie mithilfe des geleiteten Target-Arbeitsablaufs mit drei Schritten ein Multivarianz-Test geplant und erstellt wird.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395?captions=ger)
