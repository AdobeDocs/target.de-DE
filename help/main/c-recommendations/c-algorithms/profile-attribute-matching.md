---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; dynamisch; Profilattributübereinstimmung
description: Erfahren Sie, wie Sie in Adobe dynamisch filtern. [!DNL Target] Recommendations durch Vergleich von Elementen (Entitäten) mit einem Wert im Benutzerprofil.
title: Wie kann ich in Recommendations-Aktivitäten nach Profilattributübereinstimmung filtern?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 7%

---

# Profilattributübereinstimmung

Dynamisches Filtern in [!DNL Adobe Target] [!DNL Recommendations] durch Vergleich von Elementen (Entitäten) mit einem Wert im Profil des Benutzers.

Verwendung [!UICONTROL Profilattributübereinstimmung] wenn Sie Empfehlungen anzeigen möchten, die mit einem im Besucherprofil gespeicherten Wert übereinstimmen, z. B. Größe oder Lieblingsmarke.

>[!NOTE]
>
>Die [Verfahren zum Erstellen und Verwenden von Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) -Kriterien und -Promotions sind ähnlich, ebenso die Anwendungsfälle und -beispiele.

Die folgenden Szenarien zeigen, wie Sie [!UICONTROL Profilattributübereinstimmung]:

* Ein Unternehmen, das Brillen verkauft, speichert die bevorzugte Rahmenfarbe eines Besuchers als &quot;Walnut&quot;. Für diesen spezifischen Besucher sind Empfehlungen so eingerichtet, dass nur Frames der Augenklasse zurückgegeben werden, die mit &quot;Walnut&quot;in Farbe übereinstimmen.
* Ein Profilparameter kann für die Bekleidungsgröße (z. B. klein, mittel oder groß) eines Besuchers während der Navigation auf der Website Ihres Unternehmens definiert werden. Es kann eine Empfehlung eingerichtet werden, die diesem Profilparameter entspricht und Produkte zurückgibt, die nur der bevorzugten Kleidungsgröße des Benutzers entsprechen.

## Beispiele für Profilattributübereinstimmung {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profilattributübereinstimmung] ermöglicht es Ihnen, nur die Elemente zu empfehlen, die mit einem Attribut aus dem Profil des Besuchers übereinstimmen, wie in den Beispielen unten dargestellt.

### Artikel von der Lieblingsmarke des Benutzers empfehlen

Sie können beispielsweise die [!UICONTROL Profilattributübereinstimmung] -Option, um eine Regel zu erstellen, die Elemente nur empfiehlt, wenn die Marke dem Wert oder Text entspricht, der in gespeichert ist. `profile.favoritebrand`. Wenn ein Besucher mit einer solchen Regel nach Laufshorts von einer bestimmten Marke sucht, werden nur Empfehlungen angezeigt, die mit der Lieblingsmarke des jeweiligen übereinstimmen (dem unter `profile.favoritebrand` im Profil des Benutzers gespeicherten Wert).

![Lieblingsmarke](/help/main/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Zuordnung von Aufträgen zu Arbeitssuchenden

Angenommen, Sie versuchen, Arbeitsplätze mit Arbeitssuchenden zu verknüpfen. Sie möchten nur Arbeitsplätze empfehlen, die sich in derselben Stadt wie der Arbeitssuchende befinden.

Sie können Einschlussregeln verwenden, um den Standort eines Arbeitssuchenden aus dem Profil seines Besuchers mit einer Stellenausschreibung abzugleichen, wie im folgenden Beispiel gezeigt:

![Stadt des Benutzers](/help/main/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Artikel je nach Größe empfehlen

Ein visuelles Beispiel dafür, wie sich die Zuordnung von Profilattributen auf Empfehlungen auswirkt, finden Sie auf einer Website, auf der elektrische Fans verkauft werden.

Wenn ein Besucher auf verschiedene Fans-Bilder auf dieser Website klickt, legt jede Seite den Wert der `entity.size` -Parameter basierend darauf, ob die Größe des Lüfters im Bild klein oder groß ist.

Angenommen, Sie haben ein Profilskript erstellt, um die Häufigkeit der Werte von `entity.size` auf &quot;klein&quot;oder &quot;groß&quot;eingestellt ist.

Wenn der Besucher dann zur Startseite zurückkehrt, werden ihm gefilterte Empfehlungen angezeigt, je nachdem, ob mehr kleine Fans oder große Fans angeklickt wurden.

Recommendations auf der Grundlage der Anzeige von mehr kleinen Fans auf der Website:

![Empfehlungen für kleine Fans](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations basierend auf der Anzeige größerer Fans auf der Website:

![Empfehlungen für große Fans](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
