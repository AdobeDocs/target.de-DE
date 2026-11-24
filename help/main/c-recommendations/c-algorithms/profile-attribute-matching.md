---
keywords: Einschlussregeln; Einschlusskriterien; Recommendations; Promotion; Promotions; dynamische Filterung; dynamisch; Profilattributübereinstimmung
description: Erfahren Sie, wie Sie in [!DNL Target Recommendations] dynamisch filtern können, indem Sie Elemente (Entitäten) mit einem Wert im Benutzerprofil vergleichen.
title: Profilattributübereinstimmung
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
TQID: 'https://experienceleague.adobe.com/Gm91Mww5ylvNjUcmzp6KwxIG6LTibvI44LnW67KFzqk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 5%
---
# Profilattributübereinstimmung {#profile-attribute-matching}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Empfehlungen dynamisch in [!DNL Adobe Target Recommendations] filtern können, indem Sie Elemente (Entitäten) mit einem Wert im Profil des Besuchers vergleichen.

>[!ENDSHADEBOX]

Verwenden Sie **[!UICONTROL Profilattributabgleich]** um Empfehlungen anzuzeigen, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. Größe oder Lieblingsmarke. Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

Die folgenden Szenarien zeigen, wie **[!UICONTROL Profilattributübereinstimmung]** verwendet werden kann:

* Ein Unternehmen, das Brillen verkauft, speichert die bevorzugte Rahmenfarbe eines Besuchers als „Walnuss“. Für diesen Besucher werden Empfehlungen erstellt, die nur Brillenfassungen zurückgeben, die der Farbe „Walnuss“ entsprechen.
* Ein Profilparameter kann für die Kleidungsgröße (z. B. klein, Medium oder groß) eines Besuchers definiert werden, wenn der Besucher auf der Website des Unternehmens navigiert. Es kann eine Empfehlung eingerichtet werden, die diesem Profilparameter entspricht und nur die Produkte in der bevorzugten Bekleidungsgröße des Besuchers zurückgibt.

## Beispiele für übereinstimmende Profilattribute

**[!UICONTROL Profilattributabgleich]** empfiehlt nur die Elemente, die mit einem Attribut aus dem Profil des Besuchers übereinstimmen, wie in den folgenden Beispielen dargestellt.

### Empfohlene Artikel der Lieblingsmarke des Benutzers

Mit **[!UICONTROL Option „Profilattributabgleich]** kann eine Regel erstellt werden, die Elemente nur dann empfiehlt, wenn die Marke dem in `profile.favoritebrand` gespeicherten Wert oder Text entspricht. Mit einer solchen Regel werden, wenn ein Besucher Laufshorts von einer bestimmten Marke sucht, nur die Empfehlungen angezeigt, die mit der Lieblingsmarke dieses Besuchers übereinstimmen (der Wert, der in `profile.favoritebrand` im Profil des Besuchers gespeichert ist).

![Lieblingsmarke](/help/main/c-recommendations/c-algorithms/assets/favorite-brand-new.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Abgleichen von Jobs mit Arbeitsuchenden

Um Stellen mit Arbeitsuchenden abzugleichen, werden nur die Stellen empfohlen, die sich in derselben Stadt wie der Arbeitsuchende befinden. Einschlussregeln können mit dem Standort eines Arbeitsuchenden aus dem Profil des Besuchers in einer Auftragsliste übereinstimmen, wie im folgenden Beispiel gezeigt:

![Stadt des Benutzers](/help/main/c-recommendations/c-algorithms/assets/city-new.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Empfohlene Elemente basierend auf der Größe

Das folgende Beispiel zeigt, wie sich die Zuordnung von Profilattributen auf Empfehlungen auf einer Website auswirkt, auf der elektrische Lüfter verkauft werden.

Wenn ein Besucher auf verschiedene Bilder von Fans auf dieser Website klickt, legt jede Seite den Wert des `entity.size` fest, je nachdem, ob der Fan im Bild klein oder groß ist. Ein Profilskript verfolgt und zählt, wie oft der Wert von `entity.size` auf „Klein“ oder „Groß“ festgelegt wird.

Wenn der Besucher dann zur Startseite zurückkehrt, werden gefilterte Empfehlungen angezeigt, je nachdem, ob mehr kleine oder große Fans angeklickt wurden.

Empfehlungen, die auf der Anzeige kleinerer Fans auf der Website basieren:

![Empfehlungen für kleine Fans](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Empfehlungen, die auf der Anzeige größerer Fans auf der Website basieren:

![Empfehlungen für große Fans](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
