---
keywords: MVT;Multivarianz-Test;Angebote;Kombinationen
description: Erfahren Sie, wie Sie mit [!UICONTROL Visual Experience Composer] (VEC) in Adobe [!DNL Target] die Angebote erstellen, die Sie in Ihren [!UICONTROL Multivarianz-Test] (MVT) aufnehmen möchten.
title: Wie erstelle ich Kombinationen in einem [!UICONTROL Multivarianz-Test] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
TQID: 'https://experienceleague.adobe.com/3vxuP07ZViE1etmmvBdYVHIOrtZqRZfL3nE5RMHo9rU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 29%
---
# Erstellen von Kombinationen {#create-combinations}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie das Bild und die HTML-Angebote erstellen, die die Kombinationen eines **[!UICONTROL Multivarianz-Tests“]**.

>[!ENDSHADEBOX]

In einem **[!UICONTROL Multivarianz-Test]** (MVT) enthält jeder Standort mehrere Angebote, und jede Kombination von Angeboten an den Standorten ist ein Erlebnis. Verwenden Sie den **[!UICONTROL Visual Experience Composer]** (VEC) in [!DNL Adobe Target], um die Angebote zu erstellen, die Sie in Ihren Test aufnehmen möchten.

Weitere Informationen zur Verwendung des VEC zum Erstellen und Bearbeiten von Angeboten finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>Sie können auf **[!UICONTROL Auswahl erweitern]** klicken, wenn Sie Objekte auf der Seite auswählen, um das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element auszuwählen. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.
>
>Sie können auch den [DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) zum Navigieren in Elementen verwenden.

## Bildangebote {#image-offers}

Testen Sie mehrere Bildangebote an einem Ort, um zu ermitteln, welches Bild am erfolgreichsten ist.

1. Klicken Sie auf ein Bild auf Ihrer Seite und wählen Sie **[!UICONTROL Bildangebot ändern]**.

   ![Menü „Bildangebot ändern“](../assets/multivariate-1.png)

1. Wählen **[!UICONTROL Dialogfeld „Bildangebot]** alle Bilder aus, die Sie in den Test einbeziehen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   ![Menü „Bildangebot ändern“](../assets/multivariate-3.png)

Jedes Bild wird zu einem eigenen Erlebnis an diesem Ort.

## HTML-Angebote {#html-offers}

Testen Sie mehrere HTML-Angebote an einem Ort, um zu ermitteln, welches Angebot am erfolgreichsten ist.

1. Klicken Sie auf Ihrer Seite auf ein HTML-Angebot und dann auf **[!UICONTROL HTML-Angebot]**.

   ![HTML-Angebotsmenü ändern](../assets/multivariate-2.png)

1. Wählen Sie Ihr HTML-Angebot aus und klicken Sie **[!UICONTROL Angebot erstellen]** und dann auf **[!UICONTROL HTML-Angebot]**.

   ![HTML-Angebotsmenü ändern](../assets/multivariate-4.png)

1. Benennen Sie das Angebot, geben Sie den Code für das HTML-Angebot ein, oder fügen Sie ihn ein. Klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Wiederholen Sie den Vorgang für alle weiteren HTML-Angebote, die Sie einbeziehen möchten.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Jedes HTML-Angebot wird zu einem eigenen Erlebnis an diesem Ort.

Empfehlungen dazu, wie viele Kombinationen einbezogen werden sollten und wie sie vor dem Start des Tests überprüft werden können, finden Sie unter [Best Practices für Multivarianz-Tests](/help/main/c-activities/c-multivariate-testing/best-practices.md#create).
