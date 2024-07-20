---
keywords: MVT; Multivariater Test; Angebote; Kombinationen
description: Erfahren Sie, wie Sie mit dem VEC (0) in Adobe [!DNL Target] die Angebote erstellen, die Sie in Ihren [!UICONTROL Multivariate Test] (MVT) aufnehmen möchten.[!UICONTROL Visual Experience Composer]
title: Wie erstelle ich Kombinationen in einem [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
source-git-commit: 7853d8c5934e40d1026e067dfa413f520ecba931
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 56%

---

# Erstellen von Kombinationen

Verwenden Sie den VEC (0) in [!DNL Adobe Target], um die Angebote zu erstellen, die Sie in Ihren [!UICONTROL Multivariate Test] (MVT) aufnehmen möchten.[!UICONTROL Visual Experience Composer]

Weitere Informationen zur Verwendung des VEC zum Erstellen und Bearbeiten von Angeboten finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>Sie können bei der Auswahl von Objekten auf der Seite auf **[!UICONTROL Expand Selection]** klicken, um das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element auszuwählen. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.
>
>Sie können auch den [DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) zum Navigieren in Elementen verwenden.

## Bildangebote  {#section_A48333211DB149ED926AE467D0032914}

Testen Sie mehrere Bildangebote an einem Ort, um zu ermitteln, welches Bild am erfolgreichsten ist.

1. Klicken Sie auf ein Bild auf Ihrer Seite und wählen Sie dann **[!UICONTROL Change Image]** aus.

   ![Option „Bild ändern“](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changeimage.png)

1. Wählen Sie alle Bilder aus, die Sie in den Test aufnehmen möchten, und klicken Sie dann auf **[!UICONTROL Save]**.

   ![Dialogfeld „Inhalt auswählen“ zum Hinzufügen von Bildern](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/addimage.png)

Jedes Bild wird zu einem eigenen Erlebnis an diesem Ort.

## HTML-Angebote  {#section_DF016101AFA9412C9B99862C23DE77B1}

Testen Sie mehrere Text-/HTML-Angebote an einem Ort, um zu ermitteln, welches Angebot am erfolgreichsten ist.

1. Klicken Sie auf ein Text-/HTML-Angebot auf Ihrer Seite und dann auf **[!UICONTROL Change Text/HTML]**.

   ![Text/HTML ändern](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changehtml.png)

1. Klicken Sie auf &quot;**[!UICONTROL Add Text/HTML Offer]**&quot;, benennen Sie das Angebot und geben Sie dann den Code für das Text-/HTML-Angebot ein oder fügen Sie ihn ein.

   ![Angebote bearbeiten](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Wiederholen Sie diese Schritte für alle weiteren Text-/HTML-Angebote, die Sie einbeziehen möchten.

1. Klicken Sie auf **[!UICONTROL Save]**.

Jedes Text-/HTML-Angebot wird zu einem eigenen Erlebnis an diesem Ort.

## Best Practices   {#section_2E98C23D2F1A460FA732A31799CE6291}

* Vermeiden Sie die Einbeziehung von mehr Orten als für den Test notwendig. Jedes Erlebnis, das Sie in den Test einbeziehen, führt zu einer erheblichen Steigerung des Datenverkehrs und der erforderlichen Zeit für die Erreichung annehmbarer Ergebnisse. Wenn Sie zum Beispiel über Seitenelemente mit je drei Angeboten verfügen, entspricht dies neun möglichen Kombinationen (3 x 3). Drei Elemente, von denen zwei drei mögliche Angebote und eines zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Element und Angebot steigt die Anzahl erheblich.
* Bei der Erstellung von Multivarianz-Tests können Sie mehr als 10 Prozent der Erlebnisse aus dem Test ausschließen, vorausgesetzt Sie erkennen die Warnung an, dass Sie dann die Offline-Berichterstellung für die Analyse verwenden müssen.
* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden. Zum Beispiel kann es zwei Bilder geben, die verschiedene Rabatte für denselben Artikel oder Service anbieten. Wenn beide Bilder auf derselben Seite eingeblendet werden, ist dies unlogisch und sorgt wahrscheinlich für Verwirrung.
* Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) , um sicherzustellen, dass Ihr Test für das Datenverkehrsaufkommen konzipiert ist, das auf Ihrer Seite anfällt. Stellen Sie sicher, dass die Traffic-Schätzung Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten.
* Sie müssen mindestens drei Testelemente haben. Wenn die Anzahl der Elemente niedriger ist, führen Sie eine Reihe von A/B-Tests durch.
* Die Alternativen jedes Elements sollten sich deutlich voneinander unterscheiden.
* Eine bewährte, wenn auch nicht erforderliche Vorgehensweise besteht darin, für jedes Element die gleiche Anzahl von Alternativen zu verwenden.
