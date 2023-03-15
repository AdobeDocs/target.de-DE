---
keywords: Benutzerdefinierter Entwurf;Geschwindigkeit;Dezimal;Komma;Entwurf anpassen
description: Erfahren Sie, wie Sie mit der Open-Source-Entwurfssprache Velocity Empfehlungsentwürfe in Adobe  [!DNL Target]  Recommendations anpassen können.
title: Wie kann ich einen Entwurf mithilfe von Velocity anpassen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 76%

---

# Anpassen eines Designs mithilfe von Velocity

Verwenden Sie die Open Source-Entwurfssprache Velocity, um Empfehlungsvorlagen in [!DNL Adobe Target Recommendations] anzupassen.

## Velocity-Übersicht {#section_C431ACA940BC4210954C7AEFF6D03EA5}

Informationen über Velocity finden Sie unter [https://velocity.apache.org](https://velocity.apache.org).

Sie können die gesamte Velocity-Logik, -Syntax usw. für einen Empfehlungsentwurf verwenden. Dies bedeutet, dass Sie *for*-Schleifen, *if*-Aussagen und anderen Code statt mit JavaScript mit Velocity erstellen können.

Entitätsattribute, die an gesendet werden [!DNL Recommendations] im `productPage` Mbox oder CSV-Upload können in einem Design angezeigt werden, mit Ausnahme von Attributen mit mehreren Werten. Jede Art von Attribut kann gesendet werden. jedoch [!DNL Target] übergibt keine Attribute des Typs &quot;Multi-Wert&quot;als Array, über das eine Vorlage iterieren kann (z. B. `entityN.categoriesList`).

Folgende Syntax verweist auf diese Werte:

```
$entityN.variable
```

Entitätsattributnamen müssen der Velocity-Kurzschreibweise folgen, die aus einer führenden *$* gefolgt von einer Velocity Template Language (VTL)-Kennung. Die VTL-Kennung muss mit einem Buchstaben (a-z oder A-Z) beginnen.

Velocity-Entitätsattributnamen sind auf die folgenden Zeichentypen beschränkt:

* Buchstaben (a-z, A-Z)
* Ziffern (0-9)
* Bindestrich ( - )
* Unterstrich ( _ )

Die folgenden Attribute sind als Velocity-Arrays verfügbar. Demzufolge können sie iteriert oder über den Index referenziert werden.

* `entities`
* `entityN.categoriesList`

Beispiel:

```
#foreach ($category in $entity1.categoriesList) 
<br/>$category 
#end
```

Oder

```
#if ($entities[0].categoriesList.size() >= 3 ) 
$entities[0].categoriesList[2] 
#end
```

Weitere Informationen zu Velocity-Variablen (Attributen) finden Sie unter [https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

Wenn Sie in Ihrem Entwurf ein Profilskript verwenden, muss das $ vor dem Skriptnamen mit einem `\` (umgekehrter Schrägstrich). Beispiel:

`\${user.script_name}`

>[!NOTE]
>
>Die maximale Anzahl von Entitäten, die in einem Entwurf referenziert werden können, egal ob hartcodiert oder in Schleife, beträgt 99. Die Länge des Vorlagenskripts kann bis zu 65.000 Zeichen betragen.

Wenn Sie z. B. ein Design wünschen, das in etwa Folgendes anzeigen soll:

![Velocity-Beispielbild](assets/velocity_example.png)

verwenden Sie diesen Code:

```
<table style="border:1px solid #CCCCCC;"> 
<tr> 
<td colspan="3" style="font-size: 130%; border-bottom:1px solid  
#CCCCCC;"> You May Also Like... </td> 
</tr> 
<tr> 
<td style="border-right:1px solid #CCCCCC;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity1.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity1.id</a></div> 
By $entity1.message <a href="?x14=brand;q14=$entity1.message"> 
(More)</a><br/> 
sku: $entity1.prodId<br/> Price: $$entity1.value 
<br/><br/> 
</div> 
</td> 
<td style="border-right:1px solid #CCCCCC; padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;">  
<div class="search_title"><a href="$entity2.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity2.id</a></div> 
By $entity2.message <a href="?x14=brand;q14=$entity2.message"> 
(More)</a><br/> 
sku: $entity2.prodId<br/> 
Price: $$entity2.value 
<br/><br/> 
</div> 
</td> 
<td style="padding-left:10px;"> 
<div class="search_content_inner" style="border-bottom:0px;"> 
<div class="search_title"><a href="$entity3.pageUrl"  
style="color: rgb(112, 161, 0); font-weight: bold;"> 
$entity3.id</a></div> 
By $entity3.message <a href="?x14=brand;q14=$entity3.message"> 
(More)</a><br/> 
sku: $entity3.prodId<br/> Price: $$entity3.value 
<br/><br/> 
</div> 
</td> 
</tr>  
</table>
```

>[!NOTE]
>
>Wenn Sie Text nach dem Wert eines Attributs vor einem Tag hinzufügen möchten, das anzeigt, dass der Attributname abgeschlossen ist, können Sie dies mit einer formalen Notation tun, um den Namen des Attributs einzuschließen. Beispiel: `${entity1.thumbnailUrl}.gif`.

Sie können auch `algorithm.name` und `algorithm.dayCount` als Entitätsattribute in Designs verwenden, sodass ein Design zum Testen mehrerer Kriterien verwendet werden kann und der Kriterienname dynamisch im Entwurf angezeigt werden kann. Dies zeigt dem Besucher, dass er „Topverkäufe“ oder „Kunden, die diesen Artikel angesehen haben, haben folgende Artikel gekauft“ sieht. Sie können diese Attribute sogar verwenden, um die `dayCount` (Anzahl der Tage, für die in den Kriterien Daten verwendet werden, z. B. &quot;Topverkäufe während der letzten 2 Tage&quot;usw.

## Arbeiten mit Zahlen in Velocity-Vorlagen

Standardmäßig behandeln Velocity-Vorlagen alle Entitätsattribute als Zeichenfolgenwerte. Möglicherweise möchten Sie ein Entitätsattribut als numerischen Wert behandeln, um einen mathematischen Vorgang durchzuführen oder ihn mit einem anderen numerischen Wert zu vergleichen. Gehen Sie wie folgt vor, um ein Entitätsattribut als numerischen Wert zu behandeln:

1. Deklarieren Sie eine Platzhaltervariable und initialisieren Sie sie in eine beliebige Ganzzahl oder in einen doppelten Wert.
1. Stellen Sie sicher, dass das Entitätsattribut, das Sie verwenden möchten, nicht leer ist (erforderlich für [!DNL Target Recommendations]&#39; template parser to validate and save the template).
1. Übergeben Sie das Entitätsattribut an die Methode `parseInt` oder `parseDouble` für die Platzhaltervariable, die Sie in Schritt 1 erstellt haben, um die Zeichenfolge in eine Ganzzahl oder in einen doppelten Wert umzuwandeln.
1. Führen Sie den mathematischen Vorgang oder Vergleich für den neuen numerischen Wert durch.

### Beispiel: Rabattpreis berechnen

Angenommen, Sie möchten den angezeigten Preis eines Artikels um 0,99 USD reduzieren, um einen Rabatt anzuwenden. Sie können den folgenden Ansatz verwenden, um dieses Ergebnis zu erzielen:

```
#set( $double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### Beispiel: Auswahl der anzuzeigenden Sterne basierend auf der Bewertung eines Artikels

Angenommen, Sie möchten eine angemessene Anzahl von Sternen basierend auf der numerischen durchschnittlichen Kundenbewertung eines Artikels anzeigen. Sie können den folgenden Ansatz verwenden, um dieses Ergebnis zu erzielen:

```
#set( $double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $double.parseDouble($entity1.get('rating')) )
    #if( $rating >= 4.5 )
        <img src="5_stars.jpg">
    #elseif( $rating >= 3.5 )
        <img src="4_stars.jpg">
    #elseif( $rating >= 2.5 )
        <img src="3_stars.jpg">
    #elseif( $rating >= 1.5 )
        <img src="2_stars.jpg">
    #else
        <img src="1_star.jpg">
    #end
#else
    <img src="no_rating_default.jpg">
#end
```

### Beispiel: Zeit in Stunden und Minuten basierend auf der Länge eines Elements in Minuten berechnen

Angenommen, Sie speichern die Länge eines Films in Minuten, möchten aber die Länge in Stunden und Minuten anzeigen. Sie können den folgenden Ansatz verwenden, um dieses Ergebnis zu erzielen:

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## Anzeigen eines Schlüsselelements mit empfohlenen Produkten {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

Sie können Ihren Entwurf ändern, um Ihre Schlüsselelemente neben anderen empfohlenen Produkten anzuzeigen. Sie möchten zum Beispiel das aktuelle Element als Referenz neben den Empfehlungen anzeigen.

Erstellen Sie dazu eine Spalte in Ihrem Entwurf, die das `$key` Attribut verwendet, auf dem Ihre Empfehlung basiert, statt das `$entity` Attribut zu verwenden. Der Code für Ihre Schlüsselspalte kann zum Beispiel folgendermaßen aussehen:

```
<div class="at-table-column"> 
   <a href="$key.pageURL"> 
      <img src=$key.thumbnailUrl" class="at-thumbnail"/> 
      <br/><h3>$key.name</h3> 
      <br/><p class="at-light">$key.message</p> 
      <br/><p class="at-light">$key.value</p> 
   </a> 
</div>
```

Das Ergebnis ist ein Entwurf wie der folgende, in dem das Schlüsselelement in einer Spalte angezeigt wird.

![rec_key-Bild](assets/rec_key.png)

Wenn Sie Ihre [!DNL Recommendations]-Aktivität erstellen und das Schlüsselelement vom Benutzerprofil genommen wird, zum Beispiel „Zuletzt gekaufter Artikel“, zeigt [!DNL Target] ein zufällig ausgewähltes Produkt im [!UICONTROL Visual Experience Composer an]. Dies beruht darauf, dass ein Profil beim Erstellen der Aktivität nicht verfügbar ist. Wenn Besucher die Seite anzeigen, sehen sie das erwartete Schlüsselelement.

## Ersetzungen in einem String-Wert durchführen {#section_01F8C993C79F42978ED00E39956FA8CA}

Sie können Ihr Design ändern, um Werte in einer Zeichenfolge zu ersetzen. Ersetzen Sie beispielsweise das Dezimalzeichen, das in den USA verwendet wird, durch das Kommatrennzeichen, das in Europa und anderen Ländern verwendet wird.

Folgender Code zeigt eine einzelne Zeile in einem bedingten Verkaufspreis-Beispiel:

```
<span class="price">$entity1.value.replace(".", ",") &euro;</span><br>
```

Folgender Code stellt ein vollständiges bedingtes Beispiel eines Verkaufspreises dar:

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") &euro;</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") &euro;<br> #else 
    <span class="price">$entity1.value.replace(".", ",") &euro;</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
```

## Anpassen der Vorlagengröße und Überprüfen auf leere Werte {#default}

Mithilfe eines Velocity-Skripts zur Steuerung der dynamischen Größe der Entitätsanzeige wird die folgende Vorlage für ein 1-zu-viele-Ergebnis verwendet, um zu verhindern, dass leere HTML-Elemente erstellt werden, wenn von [!DNL Recommendations]nicht genügend übereinstimmende Entitäten zurückgegeben werden. Dieses Skript eignet sich optimal für Szenarios, bei denen Reserveempfehlungen nicht sinnvoll sind und [!UICONTROL Teilweises Vorlagen-Rendering] aktiviert ist.

Der folgende HTML-Abschnitt ersetzt den vorhandenen HTML-Teil im Standardentwurf von 4 x 2 (die CSS ist hier aus Platzgründen nicht enthalten):

* Wenn eine fünfte Entität vorhanden ist, fügt das Skript ein schließendes div ein und öffnet eine neue Zeile mit `<div class="at-table-row">`.
* Mit 4 x 2 werden maximal acht Ergebnisse angezeigt. Dies kann für kleinere oder größere Listen durch Ändern von `$count <=8` angepasst werden.
* Beachten Sie, dass die Logik die Entitäten in mehreren Zeilen nicht ausgleicht. Wenn es beispielsweise fünf oder sechs anzuzeigende Entitäten gibt, werden nicht drei oben und zwei am unteren Ende (oder drei oben und drei unten) dynamisch angezeigt. Die oberste Zeile zeigt vier Elemente und beginnt dann mit einer zweiten Zeile.

```
<div class="at-table">
  <div class="at-table-row">
    #set($count=1) 
    #foreach($e in $entities)  
        #if($e.id != "" && $count < $entities.size() && $count <=8) 
            #if($count==5) 
                </div>
                <div class="at-table-row">
            #end
            <div class="at-table-column">
                <a href="$e.pageUrl"><img src="$e.thumbnailUrl" class="at-thumbnail" />
                    <br/>
                    <h3>$e.name</h3>
                    <br/>
                    <p class="at-light">$e.message</p>
                    <br/>
                    <p class="at-light">$$e.value</p>
                </a>
            </div>
            #set($count = $count + 1) 
        #end 
    #end
  </div>
</div>
```
