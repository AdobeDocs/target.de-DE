---
keywords: MVT;Multivariater Test;Multivariater Test erstellen;Erstellen von Multivariater Tests;MVT-Erstellung;Erstellen von MVT;wie MVT;wie Multivariater Tests
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in verwenden [!DNL Adobe Target]  um einen [!UICONTROL Multivarianz-Test] (MVT) zu erstellen.
title: Wie erstelle ich einen [!UICONTROL Multivarianz-]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
TQID: https://experienceleague.adobe.com/gxrnY43A7OWsiW48Rlq1Orp7ZxBswdAPZEAbRQrCDZA
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 809
ht-degree: 23%

---

# Erstellen eines Multivarianz-Tests

Mit [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] können Sie einfach einen [!UICONTROL Multivarianz-Test] erstellen und Teile der Seite innerhalb von [!DNL Target] ändern.

Mit dem [!DNL Target] Point-and-Click-Editor können Sie eine beliebige Stelle auswählen und mehrere Angebote hinzufügen.

Der [!UICONTROL Multivarianz-Test] (MVT) erstellt einen Seitenerstbericht. Anders ausgedrückt bedeutet das, dass der Test auf einer spezifischen URL ausgeführt wird, mit den Erlebnissen, die Sie für diese Seite entwerfen.

1. Klicken Sie **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Multivarianz-Test]**.

   >[!NOTE]
   >
   >Weitere Informationen zu den verschiedenen in [!DNL Target] verfügbaren Aktivitätstypen und ihren Unterschieden finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md) können Sie festlegen, welche Aktivitätstypen Ihre Anforderungen am besten erfüllen.

1. (Bedingt) Wählen Sie den Versandtyp aus: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL E-Mail] oder [!UICONTROL Andere/API].

1. (Bedingt) Wenn Sie [Target Premium](/help/main/c-intro/intro.md#premium)-Kunde sind, wählen [einen Arbeitsbereich aus](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Geben Sie die URL für &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) Seite an, die Sie testen möchten, und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   >[!NOTE]
   >
   >Verwenden Sie eine vollständige URL, einschließlich HTTP oder HTTPS, am Anfang.

   Wenn eine Nachricht eingeblendet wird, die Sie dazu auffordert, Ihren Browser für gemischte Inhalte zu aktivieren, folgen Sie den Anweisungen in der Nachricht. Nachdem Sie Ihren Browser für gemischte Inhalte aktiviert haben, beginnen Sie erneut mit Schritt 1.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet.

1. Klicken Sie zum Benennen der Aktivität auf das Symbol **[!UICONTROL Bearbeiten]** ( ![Bearbeiten-Symbol](/help/main/assets/icons/Edit.svg) ) neben &quot;[!UICONTROL Nicht benannte Aktivität], geben Sie einen beschreibenden Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

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

   Sie können folgende Angebotsarten hinzufügen:

   * HTML
   * Bild
   * Text

1. Klicken Sie auf **[!UICONTROL Vorschau]**, um [eine Vorschau Ihrer Erlebnisse anzuzeigen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Klicken Sie auf **[!UICONTROL Erlebnisse anzeigen]** ( ![Symbol „Erlebnisse anzeigen](/help/main/assets/icons/WebPages.svg) ), um die Liste aller Erlebnisse im linken Rahmen anzuzeigen.

1. Klicken Sie auf ein bestimmtes Erlebnis in der Liste, um dieses Erlebnis anzuzeigen.

1. (Bedingt) Um ein oder mehrere Erlebnisse aus der Aktivität auszuschließen, klicken Sie auf das Symbol **[!UICONTROL Inhalt verwalten]** ( ![Symbol Erlebnisse verwalten](/help/main/assets/icons/Experience.svg) ), um das Dialogfeld [!UICONTROL Erlebnisse verwalten] anzuzeigen.

1. (Bedingt) Klicken Sie im [!UICONTROL Erlebnisse verwalten] auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Mehr Aktionen-Symbol](/help/main/assets/icons/MoreSmallList.svg) ) neben dem Erlebnis, das Sie ausschließen möchten, und klicken Sie dann auf **[!UICONTROL Ausschließen]**.

   Sie können Erlebnisse ausschließen, die widersprüchliche Varianten aufweisen oder optisch nicht ansprechend wirken.

1. (Bedingt) Um mehrere Erlebnisse auszuschließen, aktivieren Sie die Kontrollkästchen für die gewünschten Erlebnisse und klicken Sie dann auf **[!UICONTROL Ausschließen]**.

1. [Verwenden Sie die Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714), um die Umsetzbarkeit Ihres Testplans zu überprüfen.

1. Klicken Sie **[!UICONTROL Weiter]**, um zur Seite [!UICONTROL Targeting] zu gelangen.

   Der **Targeting**-Schritt kommt Ihnen bekannt vor, wenn Sie andere [!DNL Target] Aktivitätstypen verwendet haben. Hier können Sie eine Zielgruppe auswählen und den Prozentsatz der Besucher angeben, die die einzelnen Erlebnisse sehen.

   Das Flussdiagramm führt Sie durch die Schritte Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, Auswählen der Traffic-Zuordnungsmethode und Festlegen der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

1. (Bedingt) Klicken Sie auf das Steuerelement **[!UICONTROL Alle Besucher]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die [!UICONTROL Alle Besucher]-Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

   1. Um die Audience zu ändern, klicken Sie auf **[!UICONTROL Ersetzen]-Symbol** ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.
   1. Wählen Sie [!UICONTROL &#x200B; Dialogfeld &#x200B;]Zielgruppe hinzufügen[&#x200B; die gewünschte Zielgruppe aus &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Zielgruppe zuweisen]**.

      Sie können auf **Kombinieren von Zielgruppen** klicken, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

      Wenn Sie eine neue Zielgruppe erstellen müssen, die sich noch nicht in der [!UICONTROL Zielgruppenbibliothek“ befindet] klicken Sie auf **Zielgruppe erstellen**. Während des [Zielgruppen-Workflows erstellen](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

      * **[!UICONTROL Zielgruppenbibliothek]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der [!UICONTROL Zielgruppenbibliothek] gespeichert wird und in anderen Aktivitäten wiederverwendet werden kann.
      * **[!UICONTROL Nur diese Aktivität]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht in der [!UICONTROL Zielgruppenbibliothek] gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

   1. Klicken Sie **[!UICONTROL rechten Feld auf]** Besucherprozentsatz) und wählen Sie dann den Prozentsatz der qualifizierten Besucher aus, die Sie in die Aktivität eingeben möchten.

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. [Überprüfen Sie die Testzusammenfassung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) nehmen Sie die gewünschten Änderungen vor und klicken Sie dann auf **[!UICONTROL Weiter]**.

1. [Legen Sie Ziele und Einstellungen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) für den Test fest.

1. Klicken Sie auf **[!UICONTROL Speichern und schließen]** um die Aktivität zu erstellen.

## Schulungsvideo: Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Sie mit dem [!DNL Target] dreistufigen Workflow einen Multivarianz-Test planen und erstellen.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/30168?captions=ger)
