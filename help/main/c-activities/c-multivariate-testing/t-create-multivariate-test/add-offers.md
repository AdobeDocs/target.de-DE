---
keywords: MVT;Multivarianz-Test;Angebote;Kombinationen
description: Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) in Adobe verwenden [!DNL Target]  um die Angebote zu erstellen, die Sie in Ihren [!UICONTROL Multivarianz-Test] (MVT) aufnehmen möchten.
title: Wie erstelle ich Kombinationen in einem [!UICONTROL Multivarianz-Test] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
TQID: https://experienceleague.adobe.com/3vxuP07ZViE1etmmvBdYVHIOrtZqRZfL3nE5RMHo9rU
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 498
ht-degree: 55%

---

# Erstellen von Kombinationen

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um die Angebote zu erstellen, die Sie in Ihren [!UICONTROL Multivarianz-Test] (MVT) aufnehmen möchten.

Weitere Informationen zur Verwendung des VEC zum Erstellen und Bearbeiten von Angeboten finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>Sie können auf **[!UICONTROL Auswahl erweitern]** klicken, wenn Sie Objekte auf der Seite auswählen, um das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element auszuwählen. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.
>
>Sie können auch den [DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) zum Navigieren in Elementen verwenden.

## Bildangebote {#section_A48333211DB149ED926AE467D0032914}

Testen Sie mehrere Bildangebote an einem Ort, um zu bestimmen, welches Bild am erfolgreichsten ist.

1. Klicken Sie auf ein Bild auf Ihrer Seite und wählen Sie **[!UICONTROL Bildangebot ändern]**.

1. Wählen [!UICONTROL  Dialogfeld „Bildangebot] alle Bilder aus, die Sie in den Test einbeziehen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

Jedes Bild wird zu einem eigenen Erlebnis an diesem Ort.

## HTML-Angebote {#section_DF016101AFA9412C9B99862C23DE77B1}

Testen Sie mehrere HTML-Angebote an einem Ort, um zu ermitteln, welches Angebot am erfolgreichsten ist.

1. Klicken Sie auf Ihrer Seite auf ein HTML-Angebot und dann auf **[!UICONTROL HTML-Angebot]**.

1. Klicken Sie **[!UICONTROL Angebot erstellen]**, klicken Sie auf **[!UICONTROL HTML-]**, benennen Sie das Angebot, geben Sie den Code für das HTML-Angebot ein, oder fügen Sie ihn ein, und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Wiederholen Sie diese Schritte für alle weiteren HTML-Angebote, die Sie einbeziehen möchten.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Jedes HTML-Angebot wird zu einem eigenen Erlebnis an diesem Ort.

## Best Practices {#section_2E98C23D2F1A460FA732A31799CE6291}

* Vermeiden Sie die Einbeziehung von mehr Orten als für den Test notwendig. Jedes Erlebnis, das Sie in den Test einbeziehen, führt zu einer erheblichen Steigerung des Datenverkehrs und der erforderlichen Zeit für die Erreichung annehmbarer Ergebnisse. Wenn Sie zum Beispiel über Seitenelemente mit je drei Angeboten verfügen, entspricht dies neun möglichen Kombinationen (3 x 3). Drei Elemente, von denen zwei drei mögliche Angebote und eines zwei Angebote enthalten, entsprechen 18 Optionen (3 x 3 x 2). Mit jedem zusätzlichen Element und Angebot steigt die Anzahl erheblich.
* Beim Erstellen Multivarianz-Tests können Sie mehr als 10 Prozent der Erlebnisse vom Test ausschließen, sofern Sie die Warnung bestätigen, dass Sie dann Offline-Berichte für die Analyse verwenden müssen.
* Nutzen Sie die Vorschaufunktion, um unerwünschte Inhaltskombinationen zu vermeiden. Zum Beispiel kann es zwei Bilder geben, die verschiedene Rabatte für denselben Artikel oder Service anbieten. Wenn beide Bilder auf derselben Seite eingeblendet werden, ist dies unlogisch und sorgt wahrscheinlich für Verwirrung.
* Verwenden Sie die [Traffic-Schätzung](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md), um sicherzustellen, dass Ihr Test für das Datenverkehrsaufkommen konzipiert ist, das auf Ihrer Seite anfällt. Stellen Sie sicher, dass die Traffic-Schätzung Ihrer Testkonfiguration grünes Licht gibt, damit Sie die gewünschten Ergebnisse erhalten.
* Sie müssen mindestens drei Testelemente haben. Wenn die Anzahl der Elemente niedriger ist, führen Sie eine Reihe von A/B-Tests durch.
* Die Alternativen der einzelnen Elemente sollten sich deutlich voneinander unterscheiden.
* Eine bewährte, wenn auch nicht erforderliche Vorgehensweise besteht darin, für jedes Element die gleiche Anzahl von Alternativen zu verwenden.
