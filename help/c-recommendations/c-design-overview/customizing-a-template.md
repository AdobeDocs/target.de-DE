---
description: Verwenden Sie die Open Source-Entwurfssprache Velocity, um Empfehlungsvorlagen anzupassen.
keywords: Benutzerdefinierter Entwurf; Geschwindigkeit; Dezimal; Komma; Entwurf anpassen
seo-description: Verwenden Sie die Open Source-Entwurfssprache Velocity, um Empfehlungsvorlagen anzupassen.
seo-title: Anpassen eines Designs mithilfe von Velocity
solution: Target
title: Anpassen eines Designs mithilfe von Velocity
title-outputclass: premium
topic: Premium
uuid: 80701a15-c5eb-4089-a92e-117eda11faa2
badge: premium
translation-type: tm+mt
source-git-commit: a8bb6facffe6ca6779661105aedcd44957187a79

---


# ![PREMIUM](/help/assets/premium.png) Personalisieren Sie einen Entwurf mit Velocity{#customize-a-design-using-velocity}

Verwenden Sie die Open Source-Entwurfssprache Velocity, um Empfehlungsvorlagen anzupassen.

## Geschwindigkeitsübersicht {#section_C431ACA940BC4210954C7AEFF6D03EA5}

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
>Die maximale Anzahl von Entitäten, die in einem Entwurf referenziert werden können, egal ob hardcodiert oder in Schleife, beträgt 99. Die Länge des Vorlagenskripts kann bis zu 65.000 Zeichen betragen.

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

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Wenn Sie nach dem Variablenwert Informationen hinzufügen möchten, können Sie dies mit einer formalen Notation tun. Beispiel: `${entity1.thumbnailUrl}.gif`.

Sie können `algorithm.name` und `algorithm.dayCount` als Variablen in Entwürfen verwenden, sodass ein Design zum Testen mehrerer Kriterien verwendet und der Kriterienname dynamisch in dem Design angezeigt werden kann. Dies zeigt dem Besucher, dass er „Topverkäufe“ oder „Kunden, die diesen Artikel angesehen haben, haben folgende Artikel gekauft“ sieht. Sie können diese Variablen sogar dazu verwenden, den `dayCount` anzuzeigen (Anzahl der Tage, deren Daten vom Kriterium verwendet werden, z. B. „Topverkäufe während der beiden letzten Tage“ usw.).

## Szenario: Schlüsselelement mit empfohlenen Produkten anzeigen {#section_7F8D8C0CCCB0403FB9904B32D9E5EDDE}

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

## Szenario: Dezimaltrennzeichen durch Komma in einem Vertriebspreis ersetzen {#section_01F8C993C79F42978ED00E39956FA8CA}

Sie können Ihren Entwurf anpassen, um den Dezimalpunkt, der in den USA zum Einsatz kommt, durch ein Kommatrennzeichen zu ersetzen, wie es in Europa und anderen Ländern üblich ist.

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

## Szenario: Erstellen Sie ein standardmäßiges Recommendations-Design von 4 x 2 mit Null-Prüfungen. {#default}

Mithilfe eines Velocity-Skripts zur Steuerung der dynamischen Größe der Entitätsanzeige wird die folgende Vorlage für ein 1-zu-viele-Ergebnis verwendet, um leere HTML-Elemente zu vermeiden, wenn nicht genügend übereinstimmende Entitäten zurückgegeben [!DNL Recommendations]werden. Dieses Skript eignet sich optimal für Szenarios, wenn Reserveempfehlungen nicht sinnvoll sind und [!UICONTROL partielles Vorlagenrendering] aktiviert ist.

Der folgende HTML-Abschnitt ersetzt den vorhandenen HTML-Teil im Standardentwurf von 4 x 2 (die CSS wird hier aufgrund der Ähnlichkeit nicht berücksichtigt):

* Wenn eine fünfte Entität vorhanden ist, fügt das Skript ein schließendes div ein und öffnet eine neue Zeile mit `<div class="at-table-row">`.
* Mit 4 x 2 sind die maximal angezeigten Ergebnisse 8. Dies könnte jedoch für kleinere oder größere Listen angepasst werden, indem sie geändert `$count <=8`werden.
* Beachten Sie, dass die Logik die Entitäten in mehreren Zeilen nicht ausgewogen abgleicht. Wenn es beispielsweise fünf oder sechs anzuzeigende Entitäten gibt, wird sie nicht dynamisch drei und zwei am unteren Ende (oder drei oben und drei unten) angezeigt. Die oberste Zeile zeigt vier Elemente, bevor Sie eine zweite Zeile starten.

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
