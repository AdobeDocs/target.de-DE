---
description: Verwenden Sie Entitätsattribute mit einzelnen oder mehreren Werten zur Festlegung weiterer Informationen zu Artikeln in Ihrem Katalog.
keywords: Entitätsattribute mit mehreren Werten; benutzerdefinierte Entitätsattribute; Gültiges JSON; Entitätsattributwert; JSON-Array; mehrere Werte; mehrwertig
seo-description: Verwenden Sie Entitätsattribute mit einzelnen oder mehreren Werten zur Festlegung weiterer Informationen zu Artikeln in Ihrem Katalog.
seo-title: Benutzerdefinierte Entitätsattribute
solution: Target
title: Benutzerdefinierte Entitätsattribute
title-outputclass: premium
topic: Premium
uuid: ccebcd16-7d8f-468f-8474-c89b0f029bdb
badge: premium
translation-type: tm+mt
source-git-commit: d563d1de4768ad896bd468f995ee22a10cfa9f46

---


# ![PREMIUM](/help/assets/premium.png) Personalisierte Entitätsattribute{#custom-entity-attributes}

Verwenden Sie Entitätsattribute mit einzelnen oder mehreren Werten zur Festlegung weiterer Informationen zu Artikeln in Ihrem Katalog.

## Beschränkungen {limits}

Sie können bis zu 100 benutzerdefinierte Entitätsattribute festlegen, um weitere Informationen zu Artikeln in Ihrem Katalog bereitzustellen. Möglicherweise möchten Sie ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` erstellen, um damit ein Buch oder einen Film zu kategorisieren. Alternativ kann ein Ticketverkäufer Attribute zur Halle einrichten, um über einen zusätzlichen Auftritt, z. B. ein weiteres Team, das bei einer Sportveranstaltung mitwirkt, oder die Vorgruppe bei einem Konzert, zu informieren.

Die maximale Länge von benutzerdefinierten Attributen für Einzelwertentitäten beträgt 15.000 Zeichen (für ein- und zweibyte-UTF -8-kodierte Sprachen wie Englisch und andere lateinische Skriptbuchstaben) oder 10.000 Zeichen (für 3-Byte-UTF -8-kodierte Sprachen wie Chinesisch, Japanisch und Koreanisch).

Benutzerdefinierte Attribute mit mehreren Werten dürfen maximal 500 Werte enthalten. Jeder einzelne Wert ist auf 100 Zeichen begrenzt. Die Gesamtanzahl der Zeichen für alle Werte muss den Beschränkungen für die maximale Länge von benutzerdefinierten Attributen für Einzelwertentitäten entsprechen (siehe oben).

## Benutzerdefinierte Entitätsattributwerte   {#section_313331A9F8194A89B5EDD89363018651}

Benutzerdefinierte Entitätsattribute können einen oder mehrere Werte umfassen. Die Werte der Entitätsattribute werden in der Produktansicht dargestellt.

![](assets/multi-value_product.png)

Ein benutzerdefinierter Entitätswert mit einem einzelnen Wert ist genauso aufgebaut wie ein vordefiniertes Entitätsattribut mit nur einem Wert:

```
entity.genre=genre1
```

Ein benutzerdefiniertes Entitätsattribut mit mehreren Werten muss als gültiges JSON-Array festgelegt werden:

```
entity.genre=[“genre1”, “genre2”]
```

Beispiele für gültige JSON-Arrays, die von [!DNL Recommendations] unterstützt werden:

* `["AB","BC"]` alle Werte sind Zeichenfolgen
* `[1,2]` alle Werte sind numerisch

>[!NOTE]
>
>[!DNL Recommendations] unterstützt keine gemischten Werttypen in Attributen mit mehreren Werten `["AB",1,true, [1,2,3]]` ist beispielsweise ein gültiges JSON-Array, wird jedoch [!DNL Recommendations] nicht unterstützt, da es gemischte Werttypen enthält (Zeichenfolge, numerisch, boolesches Objekt, Objekt)

Wurde ein benutzerdefiniertes Attribut als gültiges JSON-Array übermittelt, wird das Attribut für alle Produkte im Katalog als Attribut mit mehreren Werten behandelt.

>[!NOTE]
>
>Um ein Attribut aus mehreren Werten zu einem einzelnen Wert zu ändern, müssen Sie Ihren Katalog löschen und die Produktdaten hochladen. Wird der Katalog gelöscht, bleiben die historischen Daten Ihrer Produkt-IDs jedoch erhalten. Weitere Informationen finden Sie unter [Löschen aller Artikel aus dem System](../../assets/adobe-recommendations-classic.pdf) in der Dokumentation von *Adobe Recommendations Classic*.

**Einschränkungen**:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden. (Siehe [Entitätsattribute](../../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F).)
* Das Attribut `entity.environment` ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, `entity.environment` mit `targetPageParams`, Feeds oder APIs zu übermitteln, werden ignoriert.
* Arrays müssen einen einzigen Werttyp enthalten. Arrays mit gemischten Werten (`["AB",1,true]`) werden nicht unterstützt.
* Ein Attribut mit mehreren Werten, das ein verschachteltes JSON-Array (`[10,12,[1,2,3]]`) enthält, wird als Attribut mit einem Wert behandelt.

## Implementieren von Attributen mit mehreren Werten {#section_80FEFE49E8AF415D99B739AA3CBA2A14}

Benutzerdefinierte Entitätsattribute mit mehreren Werten werden unterstützt, wenn Feeds (CSV), `targetPageParams` oder die APIs für Bereitstellung und Speicherung von Entitäten für das Hochladen von Produkten verwendet werden. Alte Werte werden durch neue Werte ersetzt, nicht ergänzt. Leere Arrays ([]) werden wie Arrays ohne Werte behandelt.

Doppelte Anführungszeichen müssen mit Escapezeichen angegeben werden. Zum Beispiel ist `"[""test"", ""value""]"` ein gültiges JSON-Array, das in CSV verwendet werden kann.

Sie können bis zu 500 Werte in einem Attribut mit mehreren Werten einbeziehen.

**Verwenden von targetPageParams**

Das folgende Beispiel zeigt, wie Sie Folgendes verwenden:  `targetPageParams`

```
function targetPageParams() { 
  return { 
    'entity.id':                   '123', 
    'entity.categoryId':            '["A", "A:B", "A:B:C", "A:B:C:D"]',        
    'entity.MultiValueAttribute':   '["X", "Y", "Z"]', 
    'entity.event.detailsOnly':     'true', 
    'excludedIds":                  '[123, 3232, 2323, 4344]', 
    'orderId":                      '123456', 
    'orderTotal":                   '195.32', 
    'productPurchaseId":            '[001,002,003]' 
  }; 
}
```

**Verwenden von CSV-Dateien**

Sie können Ihre CSV-Dateien im Rohformat verwalten, indem Sie einen Texteditor verwenden oder stattdessen mit einem Tabellenkalkulationsprogramm arbeiten.

Eine CSV-Datei im Rohformat sieht wie folgt aus:

![](assets/multi-value_example_raw.png)

Der gleiche Katalog sieht im Tabellenformat so aus:

![](assets/multi-value_example_excel.png)

Bei der Konvertierung in das [!DNL .csv]-Format fügt die Tabelle doppelte Anführungszeichen um Zellinhalte hinzu, um zu verhindern, dass Kommas in der Zelle als Spaltentrennzeichen fungieren. Außerdem werden doppelte Anführungszeichen um JSON-Zeichenfolgenwerte gelegt, die in benutzdefinierten Attributen mit mehreren Werten enthalten sind. Die Arbeit mit der Rohdatei erschwert sich hierdurch etwas. Beispiel:

* Tabelle: `["1","2","3"]`
* Rohformat: `"[""1"",""2"",""3""]"`

Gehen Sie bei der direkten Bearbeitung einer CSV-Katalogdatei im Rohformat vorsichtig vor.

**Verwenden von APIs**

Informationen zur
Verwendung der apis für die Bereitstellung und Speicherung von Entitäten finden Sie in der [Dokumentation](http://developers.adobetarget.com/api/recommendations) zu Adobe Recommendations API.

## Verwenden von Operatoren mit Attributen mit mehreren Werten {#section_83C2288A805242D9A02EBC4F07DEE945}

Wenden Sie Operatoren nur für benutzerdefinierte Attribute mit mehreren Werten in Algorithmuseinschlussregeln, Katalogregeln und Ausschlussregeln an, lautet das Ergebnis *true* (wahr), wenn mindestens ein Wert in der Liste die Operation (Boolesches *or*) erfolgreich durchläuft.

Im folgenden Beispiel lautet die Regel:   `message contains abc`.

1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte `abc`.

2. Fall: `entity.genre = ["abcde","de","ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte `abc`.

Im Falle negativer Operatoren müssen alle Attributwerte die Operation (Boolesches *and*) erfolgreich durchlaufen. Lautet der Operator beispielsweise   `notEquals`, lautet das Ergebnis *false* (falsch), wenn nur ein beliebiger Wert die Operation erfüllt.

In der Tabelle unten finden Sie Informationen zum Verhalten der Operatoren in Algorithmuseinschlussregeln, Katalogregeln und Ausschlussregeln.

| Operator | Verhalten | Beispiel  |
|--- |--- |--- |
| Gleich | Entspricht ein beliebiger Attributwert dem eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre equals abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte `abc`.<br>2. Fall: `entity.genre = ["abc", "de", "ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte `abc`.<br>3. Fall: `entity.genre = ["abcde", "de", "ef"]`. Das Ergebnis lautet „false“ (falsch), da `abc` keinem Element in der Liste entspricht. |
| Ist nicht gleich | Entspricht keiner der Attributwerte dem eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre not equals abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „true“ (wahr), da keiner der Werte `abc`.<br>2. Fall: `entity.genre = ["abc", "de", "ef"]`. Das Ergebnis lautet „false“ (falsch), da einer der Werte `abc`.<br>3. Fall: `entity.genre = ["abcde", "de", "ef"]`. Das Ergebnis lautet „true“ (wahr), da `abc` keinem Element in der Liste entspricht. |
| „Enthält“ | Enthält ein beliebiger Attributwert den eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre contains abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte `abc`.<br>2. Fall: `entity.genre = ["abcde", "de", "ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte `abc`. |
| Enthält nicht | Enthält keiner der Attributwerte den eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre does not contain abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „true“ (wahr), da keiner der Werte `abc`.<br>2. Fall: `entity.genre = ["abcde", "de", "ef"]`. Das Ergebnis lautet „false“ (falsch), da einer der Werte`abc`. |
| Beginnt mit | Beginnt ein beliebiger Attributwert mit dem eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre starts with abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte mit `abc`.<br>2. Fall: `entity.genre = ["abcde", "de", "ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte mit `abc`.<br>3. Fall: `entity.genre = ["ab", "de", "abc"]`. Das Ergebnis lautet „true“ (wahr), da ein Wert mit `abc` beginnt (nicht notwendigerweise das erste Element in der Liste). |
| Endet mit | Endet ein beliebiger Attributwert mit dem eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre ends with abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte mit `abc`.<br>2. Fall: `entity.genre = ["deabc", "de", "ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte mit `abc`. |
| Größer als oder gleich (ausschließlich numerische Werte) | Der Attributwert wird verdoppelt. Attribute, die nicht umgewandelt werden können, werden bei Ausführung der Regel übersprungen.<br>Nach der Verarbeitung lautet das Ergebnis true (wahr), wenn ein beliebiger Attributwert größer als die eingegebenen Werte oder gleich den eingegebenen Werten ist. | `price greater than or equal to 100`<br>1. Fall: `entity.price = ["10", "20", "45"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte größer als oder gleich 100 ist. Der Wert `de` wurde übersprungen, weil er nicht verdoppelt werden kann.<br>2. Fall: `entity.price = ["100", "101", "90", "80"]`. Das Ergebnis lautet „true“ (wahr), da zwei Werte größer als oder gleich 100 sind. |
| Kleiner als oder gleich (ausschließlich numerische Werte) | Der Attributwert wird verdoppelt. Attribute, die nicht umgewandelt werden können, werden bei Ausführung der Regel übersprungen.<br>Nach der Verarbeitung lautet das Ergebnis true (wahr), wenn ein beliebiger Attributwert kleiner als die eingegebenen Werte oder gleich den eingegebenen Werten ist. | `price less than or equal to 100`<br>1. Fall: `entity.price = ["101", "200", "141"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte kleiner als oder gleich 100 ist. Der Wert `de` wurde übersprungen, weil er nicht verdoppelt werden kann.<br>2. Fall: `entity.price = ["100", "101", "90", "80"]`. Das Ergebnis lautet „true“ (wahr), da zwei Werte kleiner als oder gleich 100 sind. |
| Dynamische Übereinstimmungen (nur für artikelbasierte Algorithmen verfügbar) | Entspricht ein beliebiger Attributwert dem eingegebenen Wert, lautet das Ergebnis true (wahr). | `genre matches abc`<br> 1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte `abc`.<br>2. Fall: `entity.genre = ["abc", "de", "ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte `abc`. |
| Dynamische Nichtübereinstimmung (nur für artikelbasierte Algorithmen verfügbar) | Entspricht ein beliebiger Attributwert dem eingegebenen Wert, lautet das Ergebnis false (falsch). | `genre does not match abc`<br>1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „true“ (wahr), da keiner der Werte `abc`.<br>2. Fall: `entity.genre = ["abc", "de", "ef"]`. Das Ergebnis lautet „false“ (falsch), da einer der Werte `abc`. |
| Dynamische Bereiche (nur für artikelbasierte Algorithmen verfügbar, ausschließlich numerische Werte) | Liegt einer der numerischen Attributwerte in einem festgelegten Bereich, lautet das Ergebnis true (wahr). | `price dynamically ranges in 80% to 120% of 100`<br>1. Fall: `entity.price = ["101", "200", "125"]`. Das Ergebnis lautet „true“ (wahr), da `101` im Bereich von 80% bis 120% von 100 liegt. Der Wert `de` wurde übersprungen, weil er nicht verdoppelt werden kann.<br>2. Fall: `entity.price = ["130", "191", "60", "75"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte im Bereich zwischen 80 und 120 % von 100 liegt. |

>[!NOTE]
>
>*Double* ist ein Java-Datentyp. Bei Operatoren, für die numerische Werte erforderlich sind, werden bei der Verdoppelung alle Werte aus der Ergebnisberechnung ausgeschlossen, die nicht numerisch sind.

## Attribute mit mehreren Werten in Entwürfen   {#section_F672E4F6E1D44B3196B7ADE89334ED4A}

Attribute mit mehreren Werten werden als kommagetrennte Liste aufgeführt, wenn sich in einem Entwurf darauf bezogen wird.

Beispiel:  

Wenn auf `entity.genre=["genre1","genre2"]` in einem Entwurf als `$entity<N>.genre` verwiesen wird, lautet das Ergebnis `genre1, genre2`.

>[!MORE_LIKE_THIS]
>
>* [Entitätsattribute](../../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F)

