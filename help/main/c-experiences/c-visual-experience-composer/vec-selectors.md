---
keywords: Erlebnis-Targeting;Landingpage-Test
description: Ein Elementselektor ist ein CSS-Ausdruck, mit dem ein oder mehrere Elemente identifiziert werden können. Erfahren Sie, wie Sie Elementauswahlen in Adobe [!DNL Target] Visual Experience Composer (VEC) verwenden.
title: Kann ich Elementauswahlen im Visual Experience Composer (VEC) verwenden?
feature: Visual Experience Composer (VEC)
exl-id: f4ddb30a-f599-4fe5-861c-2deeeb9a70dd
TQID: 'https://experienceleague.adobe.com/sqvUyLFddt7HPHH62jwpOZmwTIMSg-hyLIUr8w-x7vg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 4%
---
# Element-Selektoren, die im [!UICONTROL Visual Experience Composer“ verwendet &#x200B;] {#vec-selectors}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Elementauswahlen in [!UICONTROL Visual Experience Composer] (VEC) funktionieren, wie Sie auswählen, welche Selektoren verwendet werden und wie [!DNL Target] einen Selektor für ein Element generiert.

>[!ENDSHADEBOX]

Ein Elementselektor ist ein CSS-Ausdruck, mit dem ein oder mehrere Elemente identifiziert werden können. Grundlegende Informationen zu CSS-Selektoren finden Sie im Dokument [Selektoren](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) auf der *[!DNL Mozilla Developer Network]* (MDN).

Ob Elementklassen oder Element-IDs verwendet werden, ist in den Kontovoreinstellungen festgelegt. Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und wählen Sie dann die bevorzugten CSS-Selektoren aus:

* **[!UICONTROL Element-IDs verwenden]**: Deaktivieren Sie diese Option, wenn dieselbe ID für mehrere Elemente verwendet wird oder wenn sich die Element-IDs beim Laden der Seite ändern können.
* **[!UICONTROL Elementklassen verwenden]**: Deaktivieren Sie diese Option, wenn sich die Elementklassen auf einer Seite ändern könnten.
* **[!UICONTROL Bevorzugte Selektoren verwenden]**: Aktivieren Sie die Verwendung eindeutiger Selektoren in VEC, um wichtige Bereiche der Website zu identifizieren.

>[!NOTE]
>
>Elementklassen sind als Selektoren in den Aktivitäten **[!UICONTROL A/B-]**, **[!UICONTROL Automated Personalization]** und **[!UICONTROL Multivarianz]** verfügbar.

Informationen dazu, wann CSS-Selektoren verwendet werden und wann eindeutige IDs zu verwenden sind, finden Sie unter [Best Practices und Einschränkungen von Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#vec-best-practices).

## Wie [!DNL Target] einen Selektor für ein Element erzeugt {#generate-selector}

[!DNL Target] erstellt einen Selektor mithilfe eines einfachen Algorithmus. Die Generierungslogik lautet wie folgt:

1. Wenn ein Element eine ID aufweist, z. B. `id="container"`, wird der Selektor für das Element `#container`.

   Beispiel:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- Selector is computed for this element -->
       <ul class="navigation">
         <li class="item active"> Home </li>
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

1. Wenn ein Element ein Klassenattribut enthält, versucht [!DNL Target], die erste Klasse einer beliebigen Klasse zu verwenden, die im Element vorhanden ist.

   [!DNL Target] versucht, das übergeordnete Element zu analysieren, bis es das `<HTML>` Element oder ein Element mit einer ID findet. Wenn ein Element eine ID enthält und der Selektor für sein untergeordnetes Element berechnet wird, trägt die ID dieses Elements zum Selektor bei.

   Beispiel:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li class="item active"> Home </li> <!-- Selector is computed for this element -->
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

   In diesem Beispiel ist der Selektor `#container` > `ul.navigation:eq(0)` > `li.item:eq(0)` (“ > &quot; zeigt das unmittelbar untergeordnete Element an).

   `eq` gibt den Index des Elements an, das „tagName=UL“ hat, und die erste `navigation`. Deshalb ist `index` = 0. Weitere Informationen finden Sie im Artikel [Selektoren](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) im MDN.

1. Wenn ein Element keine Klasse enthält, verwendet [!DNL Target] `tagName` für das Element und durchläuft das übergeordnete Element, bis entweder das `<HTML>` Element oder ein Element mit einer ID gefunden wird.

   Beispiel:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li> Home </li>
         <li> Men </li>
         <li class="active"> Women </li>
         <li> Kids </li><!-- Selector is computed for this element -->
       </ul>
     </div>
   </div>
   ```

   Der Selektor ist `#container` > `ul.navigation:eq(0)` > `li:nth-of-type(4)`.

In diesem Prozess:

* Sie können einen beliebigen CSS-Selektor verwenden, sofern er ein Element im DOM eindeutig identifiziert.
* Der obige Ansatz ist der von [!DNL Target] verwendete. [!DNL Target] gibt diesen Ansatz nicht vor. Ein beliebiger Selektor kann hinzugefügt werden, sofern er das Element eindeutig identifiziert.
* Jedes Attribut kann im Selektor verwendet werden. In diesem Artikel wird nur ein Klassenname als Beispiel verwendet.
