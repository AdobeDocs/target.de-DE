---
keywords: custom design;velocity;decimal;comma;customize design
description: Verwenden Sie die Open-Source-Entwurfssprache Velocity, um Empfehlungsentwürfe in Adobe Target Recommendations anzupassen.
title: Anpassen eines Designs mithilfe von Velocity
feature: designs
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 61%

---


# ![PREMIUM](/help/assets/premium.png) Personalisieren Sie einen Entwurf mit Velocity{#customize-a-design-using-velocity}

Verwenden Sie die Open-Source-Entwurfssprache Velocity, um Empfehlungsentwürfe in [!DNL Adobe Target Recommendations] anzupassen.

## Velocity-Übersicht {#section_C431ACA940BC4210954C7AEFF6D03EA5}

Informationen über Velocity finden Sie unter [](https://velocity.apache.org)https://velocity.apache.org.

Sie können die gesamte Velocity-Logik, -Syntax usw. für einen Empfehlungsentwurf verwenden. Dies bedeutet, dass Sie *for*-Schleifen, *if*-Aussagen und anderen Code statt mit JavaScript mit Velocity erstellen können.

An [!DNL Recommendations] gesendete Variablen in der Mbox `productPage` oder dem CSV-Upload können in einem Design angezeigt werden. Folgende Syntax verweist auf diese Werte:

```
$entityN.variable
```

Variablennamen müssen der Velocity-Kurzschreibweise entsprechen, die aus einem vorangestellten *$*-Zeichen gefolgt von einer Velocity-Vorlagensprachen (VTL)-Kennung besteht. Die VTL-Kennung muss mit einem Buchstaben (a-z oder A-Z) beginnen.

Für Velocity-Variablennamen dürfen nur die folgenden Zeichen verwendet werden:

* Buchstaben (a-z, A-Z)
* Ziffern (0-9)
* Bindestrich ( - )
* Unterstrich ( _ )

Die folgenden Variablen sind als Velocity-Arrays verfügbar. Demzufolge können sie iteriert oder über den Index referenziert werden.

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

Weitere Informationen zu Velocity-Variablen finden Sie unter [https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

Wenn Sie in Ihrem Design ein Profilskript verwenden, muss auf das $ vor dem Skriptnamen ein \ folgen. Beispiel, `\${user.script_name}`.

>[!NOTE]
>
>Die maximale Anzahl von Entitäten, auf die in einem Entwurf verwiesen werden kann (fest codiert oder in Schleifen), beträgt 99. Die Länge des Vorlagenskripts kann bis zu 65.000 Zeichen betragen.

Wenn Sie z. B. ein Design wünschen, das in etwa Folgendes anzeigen soll:

![](assets/velocity_example.png)

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
>Wenn Sie Text nach dem Wert einer Variablen vor einem Tag hinzufügen möchten, das angibt, dass der Variablenname abgeschlossen ist, können Sie dies mit einer formalen Notation tun, um den Namen der Variablen einzuschließen. Beispiel: `${entity1.thumbnailUrl}.gif`.

Sie können `algorithm.name` und `algorithm.dayCount` als Variablen in Entwürfen verwenden, sodass ein Design zum Testen mehrerer Kriterien verwendet und der Kriterienname dynamisch in dem Design angezeigt werden kann. Dies zeigt dem Besucher, dass er „Topverkäufe“ oder „Kunden, die diesen Artikel angesehen haben, haben folgende Artikel gekauft“ sieht. Sie können diese Variablen sogar dazu verwenden, den `dayCount` anzuzeigen (Anzahl der Tage, deren Daten vom Kriterium verwendet werden, z. B. „Topverkäufe während der beiden letzten Tage“ usw.).

## Arbeiten mit Zahlen in Velocity-Vorlagen

Velocity-Vorlagen behandeln alle Entitätsattribute standardmäßig als Zeichenfolgenwerte. Möglicherweise möchten Sie ein Entitätsattribut als numerischen Wert behandeln, um einen mathematischen Vorgang auszuführen oder es mit einem anderen numerischen Wert zu vergleichen. Gehen Sie wie folgt vor, um ein Entitätsattribut als numerischen Wert zu behandeln:

1. Deklarieren Sie eine Platzhaltervariable und initialisieren Sie sie in eine beliebige Ganzzahl oder Dublette.
1. Stellen Sie sicher, dass das Entitätsattribut, das Sie verwenden möchten, nicht leer ist (erforderlich, damit der Vorlagenparser von Zielgruppe Recommendations die Vorlage validieren und speichern kann).
1. Übergeben Sie das Entitätsattribut an die `parseInt`- oder `parseDouble`-Methode für die Platzhaltervariable, die Sie in Schritt 1 erstellt haben, um die Zeichenfolge in eine Ganzzahl oder Dublette umzuwandeln.
1. Führen Sie den Mathematikvorgang oder -vergleich für den neuen numerischen Wert durch.

### Beispiel: Berechnen eines Rabattpreises

Angenommen, Sie möchten den angezeigten Preis eines Artikels um 0,99 USD reduzieren, um einen Rabatt zu erhalten. Sie können dieses Ergebnis mit dem folgenden Ansatz erzielen:

```
#set( $Double = 0.1 )

#if( $entity1.get('priceBeforeDiscount') != '' )
    #set( $discountedPrice = $Double.parseDouble($entity1.get('priceBeforeDiscount')) - 0.99 )
    Item price: $$discountedPrice
#else
    Item price unavailable
#end
```

### Beispiel: Auswahl der Anzahl der anzuzeigenden Sterne anhand der Bewertung eines Elements

Angenommen, Sie möchten eine angemessene Anzahl von Sternen basierend auf der numerischen durchschnittlichen Kundenbewertung eines Artikels anzeigen. Sie können dieses Ergebnis mit dem folgenden Ansatz erzielen:

```
#set( $Double = 0.1 )

#if( $entity1.get('rating') != '' )
    #set( $rating = $Double.parseDouble($entity1.get('rating')) )
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

### Beispiel: Zeit in Stunden und Minuten auf Grundlage der Länge eines Artikels in Minuten berechnen

Angenommen, Sie speichern die Länge eines Films in Minuten, möchten die Länge jedoch in Stunden und Minuten anzeigen. Sie können dieses Ergebnis mit dem folgenden Ansatz erzielen:

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

![](assets/rec_key.png)

Wenn Sie Ihre [!DNL Recommendations]-Aktivität erstellen und das Schlüsselelement vom Benutzerprofil genommen wird, zum Beispiel „Zuletzt gekaufter Artikel“, zeigt [!DNL Target] ein zufällig ausgewähltes Produkt im [!UICONTROL Visual Experience Composer an]. Dies beruht darauf, dass ein Profil beim Erstellen der Aktivität nicht verfügbar ist. Wenn Besucher die Seite anzeigen, sehen sie das erwartete Schlüsselelement.

## Ersetzen in einem Zeichenfolgenwert {#section_01F8C993C79F42978ED00E39956FA8CA}

Sie können Ihren Entwurf ändern, um Werte in einer Zeichenfolge zu ersetzen. Ersetzen Sie beispielsweise das in den USA verwendete Dezimalzeichen durch das in Europa und anderen Ländern verwendete Komma-Trennzeichen.

Folgender Code zeigt eine einzelne Zeile in einem bedingten Verkaufspreis-Beispiel:

```
<span class="price">$entity1.value.replace(".", ",") €</span><br>
```

Folgender Code stellt ein vollständiges bedingtes Beispiel eines Verkaufspreises dar:

```
<div class="price"> 
    #if($entity1.hasSalesprice==true) 
    <span class="old">Statt <s>$entity1.salesprice.replace(".", ",") €</s></span><br> 
    <span style="font-size: 10px; float: left;">jetzt nur</span> $entity1.value.replace(".", ",") €<br> #else 
    <span class="price">$entity1.value.replace(".", ",") €</span><br> #end 
    <span style="font-weight:normal; font-size:10px;"> 
                                        $entity1.vatclassDisplay 
                                        <br/> 
                                        $entity1.delivery 
                                        <br> 
                                    </span>
```

## Anpassen der Vorlagengröße und Prüfen auf leere Werte {#default}

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
