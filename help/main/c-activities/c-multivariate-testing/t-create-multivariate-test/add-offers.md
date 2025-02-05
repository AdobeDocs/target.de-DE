---
keywords: MVT;Multivarianz-Test;Angebote;Kombinationen
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in Adobe [!DNL Target]  verwenden, um die Angebote zu erstellen, die Sie in Ihr [!UICONTROL Multivariate Test] (MVT) aufnehmen möchten.
title: Wie erstelle ich Kombinationen in einem [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 54%

---

# Erstellen von Kombinationen

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um die Angebote zu erstellen, die Sie in Ihre [!UICONTROL Multivariate Test] (MVT) aufnehmen möchten.

Weitere Informationen zur Verwendung des VEC zum Erstellen und Bearbeiten von Angeboten finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>Sie können bei der Auswahl von Objekten auf der Seite auf **[!UICONTROL Expand Selection]** klicken, um das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element auszuwählen. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.
>
>Sie können auch den [DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) zum Navigieren in Elementen verwenden.

## Bildangebote  {#section_A48333211DB149ED926AE467D0032914}

Testen Sie mehrere Bildangebote an einem Ort, um zu bestimmen, welches Bild am erfolgreichsten ist.

1. Klicken Sie auf ein Bild auf Ihrer Seite und wählen Sie dann **[!UICONTROL Change Image Offer]** aus.

1. Wählen Sie im Dialogfeld [!UICONTROL Image Offer] alle Bilder aus, die Sie in den Test einbeziehen möchten, und klicken Sie dann auf **[!UICONTROL Add]**.

Jedes Bild wird zu einem eigenen Erlebnis an diesem Ort.

## HTML-Angebote  {#section_DF016101AFA9412C9B99862C23DE77B1}

Testen Sie mehrere HTML-Angebote an einem Ort, um zu ermitteln, welches Angebot am erfolgreichsten ist.

1. Klicken Sie auf Ihrer Seite auf ein HTML-Angebot und dann auf **[!UICONTROL Change HTML Offer]**.

1. Klicken Sie auf **[!UICONTROL Create Offer]**, klicken Sie auf **[!UICONTROL HTML Offer]**, benennen Sie das Angebot, geben Sie den Code für das HTML-Angebot ein, oder fügen Sie ihn ein, und klicken Sie dann auf **[!UICONTROL Create]**.

   Wiederholen Sie diese Schritte für alle weiteren HTML-Angebote, die Sie einbeziehen möchten.

1. Klicken Sie auf **[!UICONTROL Save]**.

Jedes HTML-Angebot wird zu einem eigenen Erlebnis an diesem Ort.

## Best Practices   {#section_2E98C23D2F1A460FA732A31799CE6291}

* Vermeiden Sie die Einbeziehung von mehr Orten als für den Test notwendig. Jedes Erlebnis, das Sie in den Test einbeziehen, führt zu einer erheblichen Steigerung des Datenverkehrs und der erforderlichen Zeit für die Erreichung annehmbarer Ergebnisse. Wenn Sie zum Beispiel über Seitenelemente mit je drei Angeboten verfügen, entspricht dies neun möglichen Kombinationen (3 x 3). Drei Elemente, von denen zwei drei mögliche Angebote und eines zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Element und Angebot steigt die Anzahl erheblich.
* Beim Erstellen Multivarianz-Tests können Sie mehr als 10 Prozent der Erlebnisse vom Test ausschließen, sofern Sie die Warnung bestätigen, dass Sie dann Offline-Berichte für die Analyse verwenden müssen.
* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden. Zum Beispiel kann es zwei Bilder geben, die verschiedene Rabatte für denselben Artikel oder Service anbieten. Wenn beide Bilder auf derselben Seite eingeblendet werden, ist dies unlogisch und sorgt wahrscheinlich für Verwirrung.
* Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) um sicherzustellen, dass Ihr Test für den Traffic entwickelt wurde, den Ihre Seite erhält. Stellen Sie sicher, dass die Traffic-Schätzung Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten.
* Sie müssen mindestens drei Testelemente haben. Wenn die Anzahl der Elemente niedriger ist, führen Sie eine Reihe von A/B-Tests durch.
* Die Alternativen der einzelnen Elemente sollten sich deutlich voneinander unterscheiden.
* Eine bewährte, wenn auch nicht erforderliche Vorgehensweise besteht darin, für jedes Element die gleiche Anzahl von Alternativen zu verwenden.
