---
keywords: mehrseitig;Verlaufstests;mehrseitige Aktivität
description: Erfahren Sie, wie Sie in Adobe eine mehrseitige Aktivität erstellen, mit [!DNL Target] Sie eine Story über mehrere Seiten hinweg erstellen können, wobei das Design für jede Seite spezifisch ist.
title: Wie erstelle ich eine mehrseitige Aktivität?
feature: Visual Experience Composer (VEC)
exl-id: d000cc73-4729-4ce0-ab30-756dd3ca8545
TQID: 'https://experienceleague.adobe.com/ZFqgbNp-sLF-ahG-uXKvWY0XPcxO0oZScGkpNX8hDHY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
    internal-label: Mobile experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 13%
---
# Mehrseitige Aktivität {#multipage-activity}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Sie, wie Sie mit einer mehrseitigen Aktivität eine Story über mehrere Seiten mit einem für jede Seite spezifischen Design erstellen können.

>[!ENDSHADEBOX]

Eine mehrseitige Aktivität in [!DNL Adobe Target] erstellt eine Story über mehrere Seiten mit einem für jede Seite spezifischen Design.

Beispielsweise kann ein Angebot für den kostenlosen Versand mit Käufen über einem bestimmten Betrag getestet werden. Das Angebot kann auf der Landingpage, einer Kategorieseite und bestimmten Produktseiten mit unterschiedlicher Größe und an unterschiedlichen Positionen je nach Seitentyp angezeigt werden. Ein hervorgehobenes Angebot kann auf der Startseite angezeigt und dann durch kleinere Angebote auf anderen relevanten Seiten untermauert werden.

Eine mehrseitige Aktivität kann auch verschiedene Layouts für Desktop- und nicht-responsive Mobile-Sites definieren. Wenn die Site eine separate mobile Site wie [!DNL m.mysite.com] anstelle von [!DNL `www.mysite.com`] hat, erstellen Sie eine mehrseitige Aktivität, fügen Sie [!DNL m.mysite.com] als separate Seiten hinzu und wenden Sie dann die mobile Bearbeitung an, um entsprechende Änderungen an der Desktop-Version und der mobilen Version im selben Erlebnis vorzunehmen. Verwenden Sie für responsive mobile Sites die [Bearbeitung mobiler Erlebnisse](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

>[!NOTE]
>
>Mehrseitige Aktivitäten wurden für Aktivitäten entwickelt, bei denen das gleiche Angebot auf mehreren Seiten unterschiedlich erscheint. Wenn das Angebot auf allen Seiten gleich angezeigt wird, ist ein [Vorlagentest](/help/main/c-experiences/c-visual-experience-composer/temtest.md#similar-pages) effizienter.

Vorlagenregeln können für jede Seite im mehrseitigen Test festgelegt werden. Beispielsweise kann ein mehrseitiger Test auf der Startseite und allen Kategorieseiten ausgeführt werden, indem im mehrseitigen Test Vorlagenregeln auf die Kategorieseite angewendet werden. Siehe [Gleiches Erlebnis auf ähnlichen Seiten](/help/main/c-experiences/c-visual-experience-composer/temtest.md#similar-pages).

## Hinzufügen von Seiten zu einer Aktivität {#add-pages}

Jede zur Aktivität hinzugefügte Seite kann ein eigenes Design des Angebots aufweisen.

1. Klicken Sie auf das **[!UICONTROL Konfigurieren]**-Symbol ( ![Konfigurieren-Symbol](/help/main/assets/icons/Setting.svg) ).

1. Klicken Sie auf **[!UICONTROL Weitere Seiten hinzufügen]**.

   Ein **[!UICONTROL Seiten]**-Bereich wird auf der linken Bildschirmseite angezeigt.

   ![Symbol „Konfigurieren“](assets/vec_edit_4.png)

1. Legen Sie die Seiten und die Standardseite fest.

   Klicken Sie auf **[!UICONTROL Seite hinzufügen]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ), um eine zusätzliche Seite hinzuzufügen, geben Sie den Seitennamen und die URL an und klicken Sie dann auf **[!UICONTROL Speichern]**.

1. Verwenden Sie den [!UICONTROL Visual Experience Composer], um das Aussehen des Angebots auf jeder Seite zu gestalten.
