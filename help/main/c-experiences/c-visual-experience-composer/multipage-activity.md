---
keywords: mehrseitig;Verlaufstests;mehrseitige Aktivität
description: Erfahren Sie, wie Sie in Adobe eine mehrseitige Aktivität erstellen [!DNL Target]  mit der Sie eine Story über mehrere Seiten hinweg erstellen können, wobei das Design für jede Seite spezifisch ist.
title: Wie erstelle ich eine mehrseitige Aktivität?
feature: Visual Experience Composer (VEC)
exl-id: d000cc73-4729-4ce0-ab30-756dd3ca8545
source-git-commit: f968ec45f015fa0b195007f5790b9efb743c8b65
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 54%

---

# Mehrseitige Aktivität

Mit einer mehrseitigen Aktivität in [!DNL Adobe Target] können Sie eine Story über mehrere Seiten hinweg erstellen. Das Design ist dabei für jede Seite spezifisch.

Sie möchten beispielsweise vielleicht ein Angebot für kostenlosen Versand bei Einkäufen über einem bestimmten Betrag testen. Dieses Angebot soll dann auf Ihrer Landingpage, einer Kategorieseite und bestimmten Produktseiten erscheinen, doch sie möchten es auf den verschiedenen Seitentypen in unterschiedlichen Größen und an unterschiedlichen Stellen haben. Sie könnten das Angebot auf Ihrer Startseite hervorheben und es mit kleineren Angeboten auf anderen relevanten Seiten verstärken.

Sie können eine mehrseitige Aktivität auch verwenden, um verschiedene Layouts für Ihren Desktop und nicht responsive Mobilgeräteseiten zu definieren. Wenn die Site eine separate mobile Site wie [!DNL m.mysite.com] anstelle von [!DNL `www.mysite.com`] hat, sollten Sie stattdessen eine [mehrseitige Aktivität](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) erstellen, [!DNL m.mysite.com] als separate Seiten hinzufügen und dann die mobile Bearbeitung anwenden, um entsprechende Änderungen an der Desktop-Version und der mobilen Version im selben Erlebnis vorzunehmen. Verwenden Sie für responsive mobile Sites die [Bearbeitung mobiler Erlebnisse](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5).

>[!NOTE]
>
>Mehrseitige Aktivitäten wurden für Aktivitäten entwickelt, bei denen das gleiche Angebot auf mehreren Seiten unterschiedlich erscheint. Wenn das Angebot auf allen Seiten gleich angezeigt wird, ist ein [Vorlagentest](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781) effizienter.

Sie können Vorlagenregeln für alle Seiten im mehrseitigen Test angeben. Sie können beispielsweise einen mehrseitigen Test auf der Startseite und allen Kategorieseiten ausführen, indem Sie Vorlagenregeln auf die Kategorieseite im mehrseitigen Test anwenden. Siehe [Gleiches Erlebnis auf ähnlichen Seiten](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

So fügen sie einem Test Seiten hinzu:

1. Klicken Sie auf das Symbol **[!UICONTROL Configure]** ( ![Symbol konfigurieren](/help/main/assets/icons/Setting.svg) ).
1. Klicken Sie auf **[!UICONTROL Add Additional Pages]**.

   Auf der linken Seite des Bildschirms wird ein [!UICONTROL Pages] angezeigt.

1. Geben Sie Ihre Seiten an und legen Sie die Standardseite fest.

   Klicken Sie auf **[!UICONTROL Add Page]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ), um eine zusätzliche Seite hinzuzufügen, geben Sie den Seitennamen und die URL an und klicken Sie dann auf **[!UICONTROL Save]**.

1. Verwenden Sie die [!UICONTROL Visual Experience Composer], um das Angebot auf jeder Seite so zu gestalten, wie es aussieht.
