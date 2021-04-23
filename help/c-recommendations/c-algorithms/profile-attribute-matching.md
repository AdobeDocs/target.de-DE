---
keywords: Einschlussregeln;Einschlusskriterien;Empfehlungen;Promotion;Promotions;Dynamische Filterung;Dynamische Suche;Zuordnung von Profil-Attributen
description: Erfahren Sie, wie Sie dynamisch in Adobe [!DNL Target] Recommendations filtern können, indem Sie Elemente (Entitäten) mit einem Wert im Profil des Benutzers vergleichen.
title: Wie filtere ich nach Profil-Attributübereinstimmung in Recommendations-Aktivitäten?
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 7%

---

# ![](/help/assets/premium.png) PREMIUMProfile Attribute Matching

Dynamisches Filtern in [!DNL Adobe Target] [!DNL Recommendations] durch Vergleichen von Elementen (Entitäten) mit einem Wert im Profil des Benutzers.

Verwenden Sie [!UICONTROL Profil-Attributzuordnung], wenn Sie Empfehlungen anzeigen möchten, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. der Größe oder der Lieblingsmarke.

>[!NOTE]
>
>Der [Prozess zum Erstellen und Verwenden von Inklusionsregeln](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) für Kriterien und Promotions ist ähnlich wie die Anwendungsfälle und Beispiele.

Die folgenden Szenarien zeigen, wie Sie [!UICONTROL Profil-Attributübereinstimmung] verwenden können:

* Eine Firma, die Brillen verkauft, speichert die bevorzugte Rahmenfarbe eines Besuchers als &quot;Walnuss&quot;. Für diesen bestimmten Besucher werden nur Blasen-Rahmen zurückgegeben, die mit &quot;Walnuss&quot;farblich übereinstimmen.
* Ein Profil-Parameter kann für die Bekleidungsgröße (z. B. klein, mittel oder groß) eines Besuchers beim Navigieren auf der Website Ihrer Firma definiert werden. Eine Empfehlung kann so eingestellt werden, dass sie mit diesem Profil-Parameter übereinstimmt und nur die vom Benutzer bevorzugten Bekleidungsgrößen zurückgibt.

## Profil-Attributzuordnungsbeispiele {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profil Attribute ] Matchingermöglicht es Ihnen, nur die Elemente zu empfehlen, die mit einem Attribut aus dem Profil des Besuchers übereinstimmen, wie in den folgenden Beispielen.

### Artikel von der Lieblingsmarke des Benutzers empfehlen

Beispielsweise können Sie mit der Option [!UICONTROL Profil-Attributübereinstimmung] eine Regel erstellen, die Elemente nur dann empfiehlt, wenn die Marke dem in `profile.favoritebrand` gespeicherten Wert oder Text entspricht. Wenn ein Besucher mit einer solchen Regel nach Laufshorts von einer bestimmten Marke sucht, werden nur Empfehlungen angezeigt, die mit der Lieblingsmarke des jeweiligen übereinstimmen (dem unter `profile.favoritebrand` im Profil des Benutzers gespeicherten Wert).

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

Wenn ein Besucher auf verschiedene Fächerbilder auf dieser Website klickt, legt jede Seite den Wert des Parameters `entity.size` fest, je nachdem, ob die Größe des Fans im Bild klein oder groß ist.

Angenommen, Sie haben ein Profil-Skript erstellt, um zu verfolgen und zu zählen, wie oft der Wert von `entity.size` auf klein oder groß eingestellt ist.

Wenn der Besucher dann zur Startseite zurückkehrt, werden ihm gefilterte Empfehlungen angezeigt, je nachdem, ob mehr kleine Fans oder große Fans angeklickt wurden.

Recommendations auf der Grundlage der Anzeige von mehr kleinen Fans auf der Website:

![Empfehlungen für kleine Fans](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations auf der Grundlage der Anzeige größerer Fans auf der Website:

![Empfehlungen für große Fans](/help/c-recommendations/c-algorithms/assets/large-fans.png)
