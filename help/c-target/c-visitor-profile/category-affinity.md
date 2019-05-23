---
description: Die Kategorieaffinitätsfunktion erfasst automatisch alle Kategorien, die ein Benutzer besucht, und berechnet die Affinität des Benutzers für diese Kategorien, sodass diese zielgerichtet und segmentiert eingesetzt werden können. Hierdurch wird gewährleistet, dass Inhalte zielgerichtet auf Besucher angewendet werden, die mit großer Wahrscheinlichkeit aufgrund dieser Informationen handeln.
keywords: Affinität; Kategorieaffinität
seo-description: Die Kategorieaffinitätsfunktion erfasst automatisch alle Kategorien, die ein Benutzer besucht, und berechnet die Affinität des Benutzers für diese Kategorien, sodass diese zielgerichtet und segmentiert eingesetzt werden können. Hierdurch wird gewährleistet, dass Inhalte zielgerichtet auf Besucher angewendet werden, die mit großer Wahrscheinlichkeit aufgrund dieser Informationen handeln.
seo-title: Kategorieaffinität
solution: Target
title: Kategorieaffinität
topic: Standard
uuid: b81d9c91-a222-4768-9ac8-359f9ab9ca2d
translation-type: tm+mt
source-git-commit: 7e06b77a552749578c487a8f5a6e079c48e0a44e

---


# Kategorieaffinität{#category-affinity}

Die Kategorieaffinitätsfunktion erfasst automatisch alle Kategorien, die ein Benutzer besucht, und berechnet die Affinität des Benutzers für diese Kategorien, sodass diese zielgerichtet und segmentiert eingesetzt werden können. Hierdurch wird gewährleistet, dass Inhalte zielgerichtet auf Besucher angewendet werden, die mit großer Wahrscheinlichkeit aufgrund dieser Informationen handeln.

## Übergeben von Kategorieaffinitätsinformationen an Target {#section_B0C8E46EEBAC4549AD90352A47787D04}

Wenn ein Benutzer Ihre Site besucht, werden besucherspezifische Profilparameter in der [!DNL Target]-Datenbank aufgezeichnet. Diese Daten sind an das Cookie des Benutzers gebunden. Ein besonders nützlicher Parameter ist `categoryId`, ein Mbox-Parameter, der auf einer Produktseite zugewiesen wird. Wenn der Besucher weiter auf der Site surft oder für eine andere Sitzung zurückkehrt, können die Produktkategorien aufgezeichnet werden, die sich ein bestimmter Benutzer ansieht. Kategoriedaten können auch aufgezeichnet werden, indem sie als Mbox-Parameter `user.categoryId` in einer beliebigen Mbox (einschließlich verschachtelter Mboxes), als URL-Parameter `user.categoryId` oder mit globaler Mbox als Target-Seitenparameter übermittelt werden. Weitere Informationen erhalten Sie von Ihrem Kundenbetreuer.

Trennen Sie Kategorien durch ein Komma, um separate Kategorien zu erstellen. Beispiel:

* `categoryId=clothing,shoes,nike,running,shox,nike shox turbo,nike shox turbo VI`
* `entity.categoryId=clothing,shoes,nike,running,shox,nike shox turbo,nike shox turbo VI`

Auf Grundlage der Häufigkeit und Neuigkeit der Besuche Ihrer Produktkategorien wird die Kategorieaffinität (falls vorhanden) eines Besuchers erfasst. Kategorieaffinität kann zur zielgerichteten Anwendung auf Zielgruppen für Ihre Aktivitäten verwendet werden.

Sie können `user.categoryAffinities[]` in einem Profilskript benutzen, um ein Array der Präferenzen auszugeben, die ein Besucher ausgefüllt hat.

## Geschäftsfall für Kategorieaffinität {#section_D6FF913E88E6486B8FBCE117CA8B253B}

Die Besucheraktivität in einer Sitzung, z. B. welche Kategorie sie am häufigsten besuchen, kann bei darauffolgenden Besuchen zum Targeting verwendet werden. Jede Kategorieseite, die sich ein Besucher während seiner Sitzung anzeigen lässt, wird erfasst und seine „Lieblingskategorie“ wird auf Grundlage eines Neuigkeits- und Häufigkeitsmodells berechnet. Anschließend kann bei jedem erneuten Aufrufen der Startseite durch den Besucher der Hero-Image-Bereich angesprochen werden, um Inhalte anzuzeigen, die zu ihrer bevorzugten Kategorie gehören.

## Beispiel für die Verwendung der Kategorieaffinität {#section_A4AC0CA550924CB4875F4F4047554C18}

Stellen Sie sich vor, dass Sie online Musikinstrumente verkaufen und zielgerichtete Verkaufs-Promo-Aktionen für Bassgitarren bei Besuchern durchführen möchten, die bereits in der Vergangenheit Interesse an Gitarren gezeigt haben. Mithilfe der Kategorieaffinität können Sie Angebote erstellen, die ausschließlich Besuchern mit der entsprechenden Kategorieaffinität angezeigt werden.

## Kategorieaffinitätsalgorithmus {#section_8B86C7FF50294208866ABF16F07D5EB9}

Der Algorithmus für die Kategorieaffinität funktioniert wie folgt:

* 10 Punkte für die erste angezeigte Kategorie
* 5 Punkte für jede Kategorie, auf die nach der ersten geklickt wurde
* Wenn auf eine neue Kategorie geklickt wird, wird 1 von allen zuvor angeklickten Kategorien subtrahiert
* Wenn bereits auf eine Kategorie geklickt wurde (gesehen), wird durch erneutes Klicken nicht 1 von allen anderen Kategorien subtrahiert
* Wenn auf eine sechste neue Kategorie geklickt wird, wird die als am niedrigsten eingestufte Kategorie der ersten fünf Kategorien aus der Berechnung entfernt
* Teilen Sie am Ende der Sitzung alle Werte durch 2

### Beispiel: Kategorieaffinitätsalgorithmus

Wenn Sie z. B. die `mens-clothing` Kategorie ansehen und dann `accessories``jewelry``accessories` erneut in einer Sitzung aufrufen, führt dies zu Affinitäten von:

* `accessories`: 9 (+5 – 1 + 5)

* `mens-clothing`: 8 (+10 – 1 – 1)

* `jewelry`: 5 (+5)

Wenn die Sitzung beendet wird und der Benutzer später zur Site zurückkehrt, werden die Ergebnisse halbiert:

* `accessories`: 4.5 (9/2)

* `mens-clothing`: 4 (8/2)

* `jewelry`: 2.5 (5/2)

Angenommen, der Benutzer sieht sich dann in der Reihenfolge, in der Reihenfolge, `jewelry``accessories``beauty`in `shoes`der folgenden Reihenfolge und `womens-clothing`an:

* `accessories`: 6.5 (4.5 + 5 – 1 – 1 - 1)

* `womens-clothing`: 5 (+5)

* `jewelry`: 4.5 (2.5 + 5 – 1 – 1 - 1)

* `shoes`: 4 (+5 – 1)

* `beauty`: 3 (+5 – 1 - 1)

* `mens-clothing` nach dem letzten Klick auf `womens-clothing` die Kategorie mit der niedrigsten Bewertung mit einem Wert von 1 (4 - 1 - 1 - 1)

Wenn die Sitzung beendet wird und der Benutzer später zur Site zurückkehrt, werden die Ergebnisse halbiert:

* `accessories`: 3.3 (6.5/2)

* `womens-clothing`: 2.5 (5/2)

* `jewelry`: 2.3 (4.5/2)

* `shoes`: 2 (4/2)

* `beauty`: 1.5 (3/2)

## Kategorieaffinität für Targeting verwenden {#concept_5750C9E6C97A40F8B062A5C16F2B5FFC}

Information darüber, wie Sie eine [!UICONTROL Kategorieaffinität]-Zielgruppe für das Targeting in einer Aktivität einsetzen können

Dieser Abschnitt enthält die folgenden Informationen:

* [Erstellen einer Kategorie zur Verwendung der Kategorieaffinität](../../c-target/c-visitor-profile/category-affinity.md#section_A27C600BBA664FE7A74F8FE076B78F40)
* [Verwenden der Kategorieaffinität für Aktivitäten](../../c-target/c-visitor-profile/category-affinity.md#section_91526B942D1B4AEBB8FCDF4EBFF931CF)

## Erstellen einer Zielgruppe zur Verwendung der Kategorieaffinität {#section_A27C600BBA664FE7A74F8FE076B78F40}

1. Klicken Sie in der Liste **[!UICONTROL Zielgruppen]** auf **[!UICONTROL + Zielgruppe erstellen]**.

   Oder

   Möchten Sie eine Zielgruppe kopieren, halten Sie in der Zielgruppenliste den Mauszeiger über die gewünschte Zielgruppe und klicken Sie auf das Kopiersymbol. Sie können die Zielgruppe anschließend bearbeiten, um eine ähnliche Zielgruppe zu erstellen.

1. Geben Sie einen beschreibenden Namen für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL + Regel hinzufügen]** &gt; **[!UICONTROL Besucherprofil]**.
1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Besucherprofil]** **[!UICONTROL die Option Kategorieaffinität]** aus.

   ![](assets/affinity.png)

1. Wählen Sie die gewünschte Kategorie aus:

   * Favoritenkategorie
   * Erste Kategorie
   * Zweite Kategorie
   * Dritte Kategorie
   * Vierte Kategorie
   * Fünfte Kategorie

1. Wählen Sie einen Auswerter aus:

   * enthält (Groß-/Kleinschreibung berücksichtigt)
   * enthält nicht (Groß-/Kleinschreibung nicht berücksichtigt)
   * Gleich

1. Geben Sie jeden neuen Wert in einer eigenen Zeile an (beispielsweise „Schuhe“).
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Verwenden der Kategorieaffinität in einer Aktivität {#section_91526B942D1B4AEBB8FCDF4EBFF931CF}

Sie können Zielgruppen mit Kategorieaffinität für beliebige Aktivitäten verwenden. Während des aus drei Schritten bestehenden Arbeitsablaufs können Sie im Schritt „Target“ die gewünschte Zielgruppe auswählen.
