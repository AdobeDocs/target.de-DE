---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: Dynamische Filterung in Adobe Target Recommendations durch Vergleich von Elementen (Entitäten) mit einem Wert im Profil des Benutzers.
title: Filtern nach Profil-Attributübereinstimmung in Regeln für dynamische Inklusion in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 5%

---


# ![PREMIUM](/help/assets/premium.png) Profil Attribute Match

Dynamisches Filtern in [!DNL Adobe Target] [!DNL Recommendations] durch Vergleich von Elementen (Entitäten) mit einem Wert im Profil des Benutzers.

Verwenden Sie [!UICONTROL Profil Attribute Matching] , wenn Sie Empfehlungen anzeigen möchten, die mit einem im Profil des Besuchers gespeicherten Wert übereinstimmen, z. B. der Größe oder der Lieblingsmarke.

Die folgenden Szenarien zeigen, wie Sie [!UICONTROL Profil-Attributzuordnung]verwenden können:

* Eine Firma, die Brillen verkauft, speichert die bevorzugte Rahmenfarbe eines Besuchers als &quot;Walnuss&quot;. Für diesen bestimmten Besucher werden nur Blasen-Rahmen zurückgegeben, die mit &quot;Walnuss&quot;farblich übereinstimmen.
* Ein Profil-Parameter kann für die Bekleidungsgröße (z. B. klein, mittel oder groß) eines Besuchers beim Navigieren auf der Website Ihrer Firma definiert werden. Eine Empfehlung kann so eingestellt werden, dass sie mit diesem Profil-Parameter übereinstimmt und nur die vom Benutzer bevorzugten Bekleidungsgrößen zurückgibt.

## Profil-Attributzuordnungsbeispiele {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL Profil Attribute Matching] ermöglicht es Ihnen, nur die Elemente zu empfehlen, die mit einem Attribut aus dem Profil des Besuchers übereinstimmen, wie in den folgenden Beispielen.

### Artikel von der Lieblingsmarke des Benutzers empfehlen

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. Wenn ein Besucher mit einer solchen Regel nach Laufshorts von einer bestimmten Marke sucht, werden nur Empfehlungen angezeigt, die mit der Lieblingsmarke des jeweiligen übereinstimmen (dem unter `profile.favoritebrand` im Profil des Benutzers gespeicherten Wert).

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### Zuordnen von Arbeitsplätzen zu Arbeitssuchenden

Angenommen, Sie versuchen, Arbeitsplätze mit Arbeitssuchenden zu verbinden. Sie möchten nur Arbeitsplätze empfehlen, die sich in derselben Stadt wie der Arbeitsuchende befinden.

Sie können Einschlussregeln verwenden, um den Standort eines Arbeitsuchenden vom Profil seines Besuchers zu einer Stellenauflistung zuzuordnen, wie im folgenden Beispiel dargestellt:

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### Bekleidung empfehlen, die der Größe eines Besuchers entspricht

Schauen wir uns ein Beispiel an, um Kleidungsstücke zu empfehlen, die der im Profil des Besuchers festgelegten Bekleidungsgröße entsprechen.

Die Produktseite sendet `entity.size` im mbox-Aufruf (roter Pfeil in der Abbildung unten).

Sie können ein [Profil-Skript](/help/c-target/c-visitor-profile/profile-parameters.md) erstellen, um die Profil und Werte des Besuchers von der letzten Seite zu erfassen, die der Besucher besucht hat.

Beispiel:

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

Das Profil-Skript erfasst den `entity.size` Wert aus der mbox mit dem Namen `target-global-mbox` und gibt ihn als Profil-Attribut mit dem Namen `user.size` (blauer Pfeil in unten stehender Abbildung) zurück.

![mbox-groß-Aufruf](/help/c-recommendations/c-algorithms/assets/size.png)

Klicken Sie beim Erstellen der Empfehlungskriterien auf [!UICONTROL Hinzufügen Filterregel]und wählen Sie [!UICONTROL Profil-Attributübereinstimmung].

![Profil-Attributübereinstimmung Abbildung](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

Wenn Ihr `user.size` Profil in geladen wurde, wird es in der Dropdown-Liste zur Übereinstimmung angezeigt, wenn Sie die Regel so einrichten, dass der im mbox-Aufruf ( [!DNL Target]) übergebene Wert mit dem Profil-Skriptnamen (`size``user.size`) übereinstimmt.

Sie können dann &quot;size&quot;als Wert/Profil auswählen, der in &quot;user.size&quot;gespeichert ist, um die Zuordnung Ihres Attributes zu ändern.

Nach der Erstellung der Profil-Attributregeln werden alle Empfehlungen mit Attributen herausgefiltert, die nicht mit dem gespeicherten Profil-Attribut des Besuchers übereinstimmen.

### Artikel nach Größe empfehlen

Sehen Sie sich eine Website an, auf der Fans verkauft werden, um ein Beispiel dafür zu erhalten, wie die Zuordnung von Profil-Attributen Empfehlungen beeinflusst.

Wenn ein Besucher auf verschiedene Fächerbilder auf dieser Website klickt, legt jede Seite den Wert des `entity.size` Parameters fest, je nachdem, ob die Größe des Fans im Bild klein oder groß ist.

Angenommen, Sie haben ein Profil-Skript erstellt, um zu verfolgen und zu zählen, wie oft der Wert auf klein oder groß eingestellt `entity.size` ist.

Wenn der Besucher dann zur Startseite zurückkehrt, werden ihm gefilterte Empfehlungen angezeigt, je nachdem, ob mehr kleine Fans oder große Fans angeklickt wurden.

Recommendations auf der Grundlage der Anzeige von mehr kleinen Fans auf der Website:

![Empfehlungen für kleine Fans](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations auf der Grundlage der Anzeige größerer Fans auf der Website:

![Empfehlungen für große Fans](/help/c-recommendations/c-algorithms/assets/large-fans.png)