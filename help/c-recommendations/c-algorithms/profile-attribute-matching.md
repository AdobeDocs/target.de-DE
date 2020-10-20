---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Dynamische Filterung in Adobe Target Recommendations durch Vergleich von Elementen (Entitäten) mit einem Wert im Profil des Benutzers.
title: Filtern nach Profil-Attributübereinstimmung in Regeln für dynamische Inklusion in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 60b71c426b61bb16a23976da9a03926f8e73cf6c
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 7%

---


# ![PREMIUM](/help/assets/premium.png) Profil Attribute Match

Dynamisches Filtern in [!DNL Adobe Target] [!DNL Recommendations] durch Vergleich von Elementen (Entitäten) mit einem Wert im Profil des Benutzers.

Verwenden Sie die [!UICONTROL Profil-Attributübereinstimmung] , wenn Sie Empfehlungen anzeigen möchten, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. der Größe oder der Lieblingsmarke.

>[!NOTE]
>
>The [process for creating and using inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) for criteria and promotions is similar, as are the use cases and examples.

Die folgenden Szenarien zeigen, wie Sie [!UICONTROL Profil-Attributzuordnung]verwenden können:

* Eine Firma, die Brillen verkauft, speichert die bevorzugte Rahmenfarbe eines Besuchers als &quot;Walnuss&quot;. Für diesen bestimmten Besucher werden nur Blasen-Rahmen zurückgegeben, die mit &quot;Walnuss&quot;farblich übereinstimmen.
* Ein Profil-Parameter kann für die Bekleidungsgröße (z. B. klein, mittel oder groß) eines Besuchers beim Navigieren auf der Website Ihrer Firma definiert werden. Eine Empfehlung kann so eingestellt werden, dass sie mit diesem Profil-Parameter übereinstimmt und nur die vom Benutzer bevorzugten Bekleidungsgrößen zurückgibt.

## Beispiele für die Profil-Attributübereinstimmung {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profil Attribute Matching] ermöglicht es Ihnen, nur die Elemente zu empfehlen, die mit einem Attribut aus dem Profil des Besuchers übereinstimmen, wie in den folgenden Beispielen.

### Artikel von der Lieblingsmarke des Benutzers empfehlen

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. Wenn ein Besucher mit einer solchen Regel nach Laufshorts von einer bestimmten Marke sucht, werden nur Empfehlungen angezeigt, die mit der Lieblingsmarke des jeweiligen übereinstimmen (dem unter `profile.favoritebrand` im Profil des Benutzers gespeicherten Wert).

![Favoritenmarke](/help/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Zuordnen von Arbeitsplätzen zu Arbeitssuchenden

Angenommen, Sie versuchen, Arbeitsplätze mit Arbeitssuchenden zu verbinden. Sie möchten nur Arbeitsplätze empfehlen, die sich in derselben Stadt wie der Arbeitsuchende befinden.

Sie können Einschlussregeln verwenden, um den Standort eines Arbeitsuchenden vom Profil seines Besuchers zu einer Stellenauflistung zuzuordnen, wie im folgenden Beispiel dargestellt:

![Ort des Benutzers](/help/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Artikel nach Größe empfehlen

Sehen Sie sich eine Website an, auf der Profil-Attributzuordnungen Empfehlungen vertreiben.

Wenn ein Besucher auf verschiedene Fächerbilder auf dieser Website klickt, legt jede Seite den Wert des `entity.size` Parameters fest, je nachdem, ob die Größe des Fans im Bild klein oder groß ist.

Angenommen, Sie haben ein Profil-Skript erstellt, um zu verfolgen und zu zählen, wie oft der Wert auf klein oder groß eingestellt `entity.size` ist.

Wenn der Besucher dann zur Startseite zurückkehrt, werden ihm gefilterte Empfehlungen angezeigt, je nachdem, ob mehr kleine Fans oder große Fans angeklickt wurden.

Recommendations auf der Grundlage der Anzeige von mehr kleinen Fans auf der Website:

![Empfehlungen für kleine Fans](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations auf der Grundlage der Anzeige größerer Fans auf der Website:

![Empfehlungen für große Fans](/help/c-recommendations/c-algorithms/assets/large-fans.png)