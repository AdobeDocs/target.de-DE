---
keywords: Benutzerdefinierter Entwurf;Geschwindigkeit;Dezimal;Komma;Entwurf anpassen
description: Erfahren Sie, wie Sie mit der Open-Source-[!DNL Velocity]-Entwurfssprache Empfehlungsentwürfe in [!DNL Target] Recommendations anpassen können.
title: Anpassen eines Designs mithilfe von Velocity
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 035d7988-80d8-4080-bb0d-1d0e9f8856d1
TQID: 'https://experienceleague.adobe.com/cccBRfwqqn-eL2hraSDAoJHPYSCkcA9tVne3OWDXxEU'
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
source-git-commit: f9c9c7b2b78ec020fcabae420686b8955e350a0e
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 21%
---
# Anpassen eines Designs mithilfe von [!DNL Velocity] {#customize-design}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Open-Source-[!DNL Velocity]-Entwurfssprache Empfehlungsentwürfe in [!DNL Adobe Target Recommendations] anpassen können.

>[!ENDSHADEBOX]

## Übersicht über [!DNL Velocity] {#velocity-overview}

Informationen zu [!DNL Velocity] finden Sie unter [https://velocity.apache.org](https://velocity.apache.org).

Alle [!DNL Velocity] Logik, Syntax usw. können für einen Empfehlungsentwurf verwendet werden. Das bedeutet, *for*-Schleifen, *if*-Anweisungen und anderer Code mit [!DNL Velocity] anstelle von JavaScript erstellt werden können.

Entitätsattribute, die an [!DNL Recommendations] in der `productPage`-Mbox oder im CSV-Upload gesendet werden, können in einem Design angezeigt werden, mit Ausnahme von Attributen mit mehreren Werten. Jeder Attributtyp kann gesendet werden. [!DNL Target] übergibt jedoch keine Attribute vom Typ „mehrwertig“ als Array, über das ein Design iterieren kann (z. B. `entityN.categoriesList`).

Folgende Syntax verweist auf diese Werte:

```
$entityN.variable
```

Entitätsattributnamen müssen [!DNL Velocity] Kurzschreibweise folgen, die aus einem führenden *$*-Zeichen gefolgt von einer Kennung für die [!DNL Velocity]-Vorlagensprache (VTL) besteht. Die VTL-Kennung muss mit einem Buchstaben (a-z oder A-Z) beginnen.

[!DNL Velocity] Entitätsattributnamen sind auf die folgenden Zeichentypen beschränkt:

* Buchstaben (a-z, A-Z)
* Ziffern (0-9)
* Bindestrich ( - )
* Unterstrich ( _ )

Die folgenden Attribute sind als [!DNL Velocity]-Arrays verfügbar. Daher können sie über einen Index iteriert oder durch einen Index referenziert werden.

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

Weitere Informationen zu [!DNL Velocity] (Attributen) finden Sie unter [Velocity-Dokumentation](https://velocity.apache.org/engine/releases/velocity-1.7/user-guide.html#variables).

Wenn ein Profilskript in einem Design verwendet wird, muss das $ vor dem Skriptnamen mit einem `\` (umgekehrter Schrägstrich) maskiert werden. Beispiel:

`\${user.script_name}`

>[!NOTE]
>
>Die maximale Anzahl von Entitäten, auf die in einem Entwurf verwiesen werden kann, egal ob hartcodiert oder in Schleife, beträgt 99. Das Design-Skript kann bis zu 65.000 Zeichen enthalten.

Ein Design, das in etwa der folgenden Abbildung entspricht:

![Beispiel eines 4 x 1-Designs mit dem Titel „Andere lustige Aktivitäten“, mit vier Elementen, die jeweils ein Foto, einen Namen, einen Preis, eine Bewertung und eine Entfernung zeigen](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

kann den folgenden Code verwenden:

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
>Um nach dem Wert eines Attributs und vor einem Tag, das anzeigt, dass der Attributname abgeschlossen ist, Text hinzuzufügen, verwenden Sie eine formale Notation, um den Namen des Attributs einzuschließen. Beispiel: `${entity1.thumbnailUrl}.gif`.

`algorithm.name` und `algorithm.dayCount` können auch als Entitätsattribute in Designs verwendet werden, sodass ein Design zum Testen mehrerer Kriterien verwendet werden kann und der Kriterienname im Design dynamisch angezeigt werden kann. Dies zeigt dem Besucher, dass er „Topverkäufe“ oder „Personen, die dies angesehen und gekauft haben“ betrachtet. Die `dayCount` (die Anzahl der Tage der in den Kriterien verwendeten Daten, z. B. „Topverkäufe über die letzten 2 Tage„) kann ebenfalls angezeigt werden.

## Arbeiten mit Zahlen in [!DNL Velocity] Designs {#numbers}

Standardmäßig behandeln [!DNL Velocity]-Designs alle Entitätsattribute als Zeichenfolgenwerte. Ein Entitätsattribut muss möglicherweise als numerischer Wert behandelt werden, um einen mathematischen Vorgang durchzuführen oder ihn mit einem anderen numerischen Wert zu vergleichen. Gehen Sie wie folgt vor, um ein Entitätsattribut als numerischen Wert zu behandeln:

1. Deklarieren Sie eine Platzhaltervariable und initialisieren Sie sie in eine beliebige Ganzzahl oder in einen doppelten Wert.
1. Stellen Sie sicher, dass das zu verwendende Entitätsattribut nicht leer ist (erforderlich für den Design-Parser von [!DNL Target Recommendations] zum Überprüfen und Speichern des Designs).
1. Übergeben Sie das Entitätsattribut an die Methode `parseInt` oder `parseDouble` für die in Schritt 1 erstellte Platzhaltervariable, um die Zeichenfolge in eine Ganzzahl oder in einen doppelten Wert umzuwandeln.
1. Führen Sie den mathematischen Vorgang oder Vergleich für den neuen numerischen Wert durch.

### Beispiel: Rabattpreis berechnen

Um den angezeigten Preis eines Artikels um 0,99 US-Dollar zu reduzieren und einen Rabatt anzuwenden, kann folgender Ansatz verwendet werden:

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

Um eine angemessene Anzahl von Sternen basierend auf der numerischen durchschnittlichen Kundenbewertung eines Artikels anzuzeigen, kann der folgende Ansatz verwendet werden:

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

Um die Länge eines Films in Stunden und Minuten anzuzeigen, wenn die Länge in Minuten gespeichert wird, kann der folgende Ansatz verwendet werden:

```
#if( $entity1.get('length_minutes') )
#set( $Integer = 1 )
#set( $nbr = $Integer.parseInt($entity1.get('length_minutes')) )
#set( $hrs = $nbr / 60)
#set( $mins = $nbr % 60)
#end
```

## Anzeigen eines Schlüsselelements mit empfohlenen Produkten {#key-item}

Ein Design kann das Schlüsselelement zusammen mit den anderen empfohlenen Produkten anzeigen. Beispielsweise kann das aktuelle Element als Referenz neben den Empfehlungen angezeigt werden.

Erstellen Sie dazu eine Spalte im Design, die das `$key` verwendet, auf dem die Empfehlung basiert, und nicht das `$entity`. Beispielsweise könnte der Code für die Schlüsselspalte wie folgt aussehen:

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

![Design mit vier Spalten, wobei die erste Spalte das als aktuelles Produkt markierte Schlüsselelement anzeigt](/help/main/c-recommendations/c-design-overview/assets/rec_key.png)

Wenn beim Erstellen einer [!DNL Recommendations] Aktivität der Schlüsselartikel aus dem Profil des Besuchers übernommen wird, z. B. „Zuletzt gekaufter Artikel“, zeigt [!DNL Target] ein zufälliges Produkt im **[!UICONTROL Visual Experience Composer]** (VEC) an. Dies liegt daran, dass während der Erstellung der Aktivität kein Profil verfügbar ist. Wenn Besucher die Seite aufrufen, sehen sie das erwartete Schlüsselelement.

## Ersetzungen in einem String-Wert durchführen {#replacements}

Ein Design kann Werte innerhalb einer Zeichenfolge ersetzen. Beispielsweise kann das Dezimalzeichen, das in den USA verwendet wird, durch das Kommatrennzeichen ersetzt werden, das in Europa und anderen Ländern verwendet wird.

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
</div>
```

## Anpassen der Designgröße und Überprüfen auf leere Werte {#default}

Ein [!DNL Velocity] kann die dynamische Größe der Entitätsanzeige steuern. Das folgende Design berücksichtigt ein 1:n-Ergebnis, um zu vermeiden, dass leere HTML-Elemente erstellt werden, wenn nicht genügend übereinstimmende Entitäten von [!DNL Recommendations] zurückgegeben werden. Dieses Skript eignet sich am besten für Szenarien, in denen Backup-Empfehlungen keinen Sinn machen und **[!UICONTROL Partielles Design-Rendering]** aktiviert ist.

Der folgende HTML-Abschnitt ersetzt den vorhandenen HTML-Teil im Standardentwurf von 4 x 2 (die CSS ist hier aus Platzgründen nicht enthalten):

* Wenn eine fünfte Entität vorhanden ist, fügt das Skript ein schließendes div ein und öffnet eine neue Zeile mit `<div class="at-table-row">`.
* Bei 4x2 beträgt die maximale Anzahl der angezeigten Ergebnisse acht, dies kann jedoch durch Ändern von `$count <=8` für kleinere oder größere Listen angepasst werden.
* Die Logik balanciert die Entitäten nicht in mehreren Zeilen aus. Wenn beispielsweise fünf oder sechs Entitäten angezeigt werden sollen, werden sie nicht dynamisch zu drei oben und zwei unten (oder drei oben und drei unten). In der oberen Zeile werden vier Elemente angezeigt, bevor eine zweite Zeile gestartet wird.

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
