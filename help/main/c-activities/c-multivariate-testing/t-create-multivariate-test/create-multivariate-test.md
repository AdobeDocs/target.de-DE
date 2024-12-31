---
keywords: MVT;Multivariater Test;Multivariater Test erstellen;Erstellen von Multivariater Tests;MVT-Erstellung;Erstellen von MVT;wie MVT;wie Multivariater Tests
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in verwenden [!DNL Adobe Target]  um einen [!UICONTROL Multivariate Test] (MVT) zu erstellen.
title: Wie erstelle ich ein [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 7853d8c5934e40d1026e067dfa413f520ecba931
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 56%

---

# Erstellen eines Multivarianz-Tests

Der [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] erleichtert das Erstellen eines [!UICONTROL Multivariate Test] und das Ändern von Teilen der Seite innerhalb von [!DNL Target].

Mit dem [!DNL Target] Point-and-Click-Editor können Sie eine beliebige Stelle auswählen und mehrere Angebote hinzufügen.

Der [!UICONTROL Multivariate Test] (MVT) erstellt einen Seitenbericht. Anders ausgedrückt bedeutet das, dass der Test auf einer spezifischen URL ausgeführt wird, mit den Erlebnissen, die Sie für diese Seite entwerfen.

1. Klicken Sie auf **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   ![Erstellen eines Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. (Bedingt) Wählen Sie den Versandtyp aus: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email] oder [!UICONTROL Other/API].

1. (Bedingt) Wenn Sie [Target Premium](/help/main/c-intro/intro.md#premium)-Kunde sind, wählen [einen Arbeitsbereich aus](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Geben Sie die URL](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) für die Seite an, die Sie testen möchten, und klicken Sie dann auf **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >Verwenden Sie eine vollständige URL, einschließlich HTTP oder HTTPS, am Anfang.

   Wenn eine Nachricht eingeblendet wird, die Sie dazu auffordert, Ihren Browser für gemischte Inhalte zu aktivieren, folgen Sie den Anweisungen in der Nachricht. Nachdem Sie Ihren Browser für gemischte Inhalte aktiviert haben, beginnen Sie erneut mit Schritt 1.

   Die [!UICONTROL Visual Experience Composer] wird geöffnet.

1. Geben Sie einen Namen für die Aktivität ein.

   ![Feld für Aktivitätsname](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

   Der Aktivitätsname darf nicht mit einem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichenfolgen enthalten:

   | Zeichenfolge | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, at-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, at-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. [Erstellen Sie die Angebote an jedem Ort](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![Dialogfeld „Text/HTML bearbeiten“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Sie können folgende Angebotsarten hinzufügen:

   * HTML
   * Bild
   * Text

1. Klicken Sie auf **[!UICONTROL Preview]** , [ eine Vorschau Ihrer Erlebnisse ](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Vorschau von Erlebnissen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   Sie können jedes Erlebnis ansehen und diejenigen, die Sie nicht in Ihren Test aufnehmen möchten, ausschließen. Um ein oder mehrere Erlebnisse auszuschließen, aktivieren Sie die gewünschten Kontrollkästchen und klicken Sie dann auf **[!UICONTROL Exclude]** .

   ![Erlebnisse ausschließen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Verwenden Sie die Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um die Umsetzbarkeit Ihres Testplans zu überprüfen.

   ![Traffic-Anzeige](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   Die folgende Abbildung zeigt an, dass die Aktivität über zu wenig Traffic verfügt.

   ![Schätzbild](assets/estimator.png)

   Die folgende Abbildung zeigt an, dass die Aktivität über zu wenig Traffic verfügt.

   ![Bild Estimator2](assets/estimator2.png)

1. Klicken Sie auf **[!UICONTROL Next]** , um zur Seite [!UICONTROL Targeting] zu gelangen.

1. Wählen Sie die Zielgruppe und den Prozentsatz qualifizierter Besucher aus, die an der Aktivität teilnehmen sollen.

   ![Targeting-Seite in der MVT-Aktivität](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Überprüfen Sie die Testzusammenfassung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) nehmen Sie die gewünschten Änderungen vor und klicken Sie dann auf **[!UICONTROL Next]**.

1. [Legen Sie Ziele und Einstellungen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für den Test fest.

1. Klicken Sie auf **[!UICONTROL Save and Close]** , um die Aktivität zu erstellen.

## Schulungsvideo: Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Sie mit dem [!DNL Target] dreistufigen Workflow einen Multivarianz-Test planen und erstellen.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395)
