---
keywords: Erlebnis-Targeting;Landingpage-Test
description: Ein Elementselektor ist ein CSS-Ausdruck, mit dem ein oder mehrere Elemente identifiziert werden können. Erfahren Sie, wie Sie Elementauswahlen in Adobe [!DNL Target] Visual Experience Composer (VEC) verwenden.
title: Kann ich Elementauswahlen im Visual Experience Composer (VEC) verwenden?
feature: Visual Experience Composer (VEC)
exl-id: f4ddb30a-f599-4fe5-861c-2deeeb9a70dd
source-git-commit: 51e484d54f4d318ea59fdfdb16d1ed7014abdfdb
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 31%

---

# Element-Selektoren, die in Visual Experience Composer verwendet werden

Ein Elementselektor ist ein CSS-Ausdruck, mit dem ein oder mehrere Elemente identifiziert werden können.

Grundlegende Informationen zu CSS-Selektoren finden Sie im Dokument [Selektoren](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) auf der *[!DNL Mozilla Developer Network]* (MDN).

Sie können festlegen, ob Sie Elementklassen oder Element-IDs in Ihren Kontovoreinstellungen verwenden möchten. Klicken Sie auf **[!UICONTROL Administration > Visual Experience Composer]** und wählen Sie dann Ihre bevorzugten CSS-Selektoren aus.

* **Element-IDs verwenden**: Deaktivieren Sie diese Option, wenn dieselbe ID für mehrere Elemente verwendet wird, oder die Element-IDs können sich beim Laden der Seite ändern.
* **Elementklassen verwenden**: Deaktivieren Sie diese Option, wenn sich die Elementklassen auf einer Seite ändern könnten.
* **Bevorzugte Selektoren verwenden**: Aktivieren Sie diese Option, wenn Sie eindeutige Selektoren im VEC verwenden möchten, um Schlüsselbereiche Ihrer Website zu identifizieren.

>[!NOTE]
>
>Elementklassen sind als Selektoren in [!UICONTROL A/B Test]-, [!UICONTROL Automated Personalization]- und [!UICONTROL &#x200B; Multivariate Test] verfügbar.

Informationen dazu, wann CSS-Selektoren und wann eindeutige IDs verwendet werden sollen, finden Sie unter [Best Practices und Einschränkungen von Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#concept_E284B3F704C04406B174D9050A2528A6).

## Wie [!DNL Target] einen Selektor für ein Element erzeugt {#section_D89D954BCBFB486CA081BE183776A475}

[!DNL Target] erstellt einen Selektor mithilfe eines einfachen Algorithmus. Im Folgenden finden Sie eine kurze Erklärung der Generierungslogik:

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

1. Wenn ein Element ein Klassenattribut enthält, versucht [!DNL Target], die erste Klasse einer beliebigen Klasse im Element zu nutzen.

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

   In diesem Beispiel:

   Selektor: `#container` > `ul.navigation:eq(0)` > `li.item:eq(0)` („>“ gibt das unmittelbar untergeordnete Element an.)

   `eq` gibt für den Index an, dass es ein Element mit „tagName=UL“ gibt und die erste Klasse `navigation` lautet. Deshalb ist `index` = 0. Weitere Informationen finden Sie im Artikel [Selektoren](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) im MDN.

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

   Selektor: `#container` > `ul.navigation(0)` > `li:nth-of-type(4)`

Im oben dargestellten Prozess

* können Sie jeden beliebigen CSS-Selektor verwenden, solange er ein Element eindeutig im DOM identifiziert.
* Der obige Ansatz ist der von [!DNL Target] verwendete. [!DNL Target] schreibt nicht vor, diesen Ansatz zu verwenden. Sie können jeden beliebigen Selektor hinzufügen, vorausgesetzt Punkt 1 ist zutreffend.
* Sie können jedes beliebige Attribut im Selektor verwenden. In diesem Dokument wird nur ein Klassenname als Beispiel verwendet.
