---
keywords: Einschlussregeln; Einschlusskriterien; Recommendations; Promotion; Promotions; dynamische Filterung; dynamisch; Profilattributübereinstimmung
description: Erfahren Sie, wie Sie  [!DNL Target Recommendations]  dynamisch filtern können, indem Sie Elemente (Entitäten) mit einem Wert im Benutzerprofil vergleichen.
title: Wie filtere ich nach der Zuordnung von Profilattributen in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Zuordnung von Profilattributen

Dynamisches Filtern in [!DNL Adobe Target Recommendations] durch Vergleichen von Elementen (Entitäten) mit einem Wert im Benutzerprofil.

Verwenden Sie [!UICONTROL Profile Attribute Matching], wenn Sie Empfehlungen anzeigen möchten, die einem im Besucherprofil gespeicherten Wert entsprechen, z. B. Größe oder Lieblingsmarke.

>[!NOTE]
>
>Der [Prozess zum Erstellen und Verwenden von &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) für Kriterien und Promotions ist ähnlich, ebenso wie die Anwendungsfälle und Beispiele.

Die folgenden Szenarien zeigen, wie Sie [!UICONTROL Profile Attribute Matching] verwenden können:

* Ein Unternehmen, das Brillen verkauft, speichert die Lieblingsrahmenfarbe eines Besuchers als „Walnuss“. Für diesen spezifischen Besucher werden Empfehlungen erstellt, die nur Brillenfassungen zurückgeben, die der Farbe „Walnuss“ entsprechen.
* Ein Profilparameter kann für die Kleidungsgröße (z. B. klein, Medium oder groß) eines Besuchers definiert werden, wenn dieser auf der Website Ihres Unternehmens navigiert. Es kann eine Empfehlung eingerichtet werden, die diesem Profilparameter entspricht und Produkte zurückgibt, die nur der bevorzugten Kleidungsgröße des Benutzers entsprechen.

## Beispiele für die Zuordnung von Profilattributen {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profile Attribute Matching] können Sie nur die Elemente empfehlen, die einem Attribut aus dem Besucherprofil entsprechen, wie in den Beispielen unten dargestellt.

### Empfohlene Artikel der Lieblingsmarke des Benutzers

Sie können beispielsweise die Option [!UICONTROL Profile Attribute Matching] verwenden, um eine Regel zu erstellen, die Elemente nur dann empfiehlt, wenn die Marke dem in `profile.favoritebrand` gespeicherten Wert oder Text entspricht. Mit einer solchen Regel werden bei einem Besucher, der Laufshorts von einer bestimmten Marke sucht, nur Empfehlungen angezeigt, die mit der Lieblingsmarke dieses Benutzers übereinstimmen (der Wert, der in `profile.favoritebrand` im Besucherprofil gespeichert ist).

![Lieblingsmarke](/help/main/c-recommendations/c-algorithms/assets/favorite-brand-new.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Abgleichen von Jobs mit Arbeitsuchenden

Angenommen, Sie versuchen, Jobs mit Arbeitsuchenden abzugleichen. Sie möchten nur Jobs empfehlen, die sich in derselben Stadt wie der Arbeitsuchende befinden.

Sie können Einschlussregeln verwenden, um den Standort eines Arbeitsuchenden aus dem Besucherprofil mit einer Auftragsliste abzugleichen, wie im folgenden Beispiel gezeigt:

![Stadt des Benutzers](/help/main/c-recommendations/c-algorithms/assets/city-new.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Empfohlene Elemente basierend auf der Größe

Ein visuelles Beispiel dafür, wie sich die Zuordnung von Profilattributen auf Empfehlungen auswirkt, finden Sie auf einer Website, die elektrische Lüfter verkauft.

Wenn ein Besucher auf verschiedene Bilder von Fans auf dieser Website klickt, legt jede Seite den Wert des `entity.size` fest, je nachdem, ob der Fan im Bild klein oder groß ist.

Angenommen, Sie haben ein Profilskript erstellt, um zu verfolgen und zu zählen, wie oft der Wert von `entity.size` auf „Klein“ oder „Groß“ gesetzt wird.

Wenn der Besucher dann zur Startseite zurückkehrt, sieht er gefilterte Empfehlungen, je nachdem, ob auf weitere kleine oder große Fans geklickt wurde.

Empfehlungen, die auf der Anzeige kleinerer Fans auf der Website basieren:

![Empfehlungen für kleine Fans](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Empfehlungen, die auf der Anzeige größerer Fans auf der Website basieren:

![Empfehlungen für große Fans](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
