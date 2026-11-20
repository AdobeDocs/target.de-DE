---
keywords: Entitätsattribute mit mehreren Werten; benutzerdefinierte Entitätsattribute; Gültiges JSON; Entitätsattributwert; JSON-Array; mehrere Werte; mehrwertig
description: Erfahren Sie, wie Sie benutzerdefinierte Entitätsattribute mit einem oder mehreren Werten verwenden können, um zusätzliche Informationen über Elemente in Ihrem Adobe [!DNL Target] Recommendations-Katalog zu definieren.
title: Wie verwende ich benutzerdefinierte Entitätsattribute?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: d7d0b04a-0f50-4d30-9cbe-c0347a3d3715
TQID: 'https://experienceleague.adobe.com/eFeg78-PswBCwtpzMR7j5c8FJ03MyQVcSdzo6ctZt3Q'
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
source-git-commit: 5ed511322cc9f04c349471f8ad84a17526d4925f
workflow-type: tm+mt
source-wordcount: '1347'
ht-degree: 55%
---
# Benutzerdefinierte Entitätsattribute {#custom-entity-attributes}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie benutzerdefinierte Entitätsattribute mit einem oder mehreren Werten, die die Elemente in Ihrem [!DNL Adobe Target Recommendations] beschreiben, definieren, senden und verwenden.

>[!ENDSHADEBOX]

Verwenden Sie benutzerdefinierte Entitätsattribute mit einem oder mehreren Werten in [!DNL Adobe Target Recommendations], um zusätzliche Informationen über Elemente in Ihrem Katalog zu definieren. Diese Informationen können dann in Algorithmus-Einschlussregeln, Katalogregeln und Ausschlussregeln verwendet und in Designs angezeigt werden.

## Beschränkungen {#limits}

Sie können bis zu 100 benutzerdefinierte Entitätsattribute festlegen, um weitere Informationen zu Artikeln in Ihrem Katalog bereitzustellen. Möglicherweise möchten Sie ein benutzerdefiniertes Attribut mit dem Namen `entity.genre` erstellen, um damit ein Buch oder einen Film zu kategorisieren. Alternativ kann ein Ticketverkäufer Attribute zum Veranstaltungsort einrichten, um über einen zusätzlichen Auftritt, z. B. ein weiteres Team, das bei einer Sportveranstaltung mitwirkt, oder die Vorgruppe bei einem Konzert, zu informieren.

Die maximale Länge von benutzerdefinierten Attributen für Einzelwert-Entitäten beträgt 15.000 Zeichen (für 1- und 2-Byte-UTF-8-kodierte Sprachen wie Englisch und andere lateinische Skriptbuchstaben) oder 10.000 Zeichen (für 3-Byte-UTF-8-kodierte Sprachen wie Chinesisch, Japanisch und Koreanisch).

Benutzerdefinierte Attribute mit mehreren Werten dürfen maximal 500 Werte enthalten. Jeder einzelne Wert ist auf 100 Zeichen begrenzt. Die Gesamtanzahl der Zeichen über alle Werte muss den Einschränkungen für die maximale Länge von benutzerdefinierten Einzelwert-Entitätsattributen entsprechen (siehe oben).

## Benutzerdefinierte Entitätsattributwerte {#section_313331A9F8194A89B5EDD89363018651}

Benutzerdefinierte Entitätsattribute können einen oder mehrere Werte umfassen. Die Werte der Entitätsattribute werden in der Produktansicht dargestellt.

![Multi-Value_Product Image](assets/multi-value_product.png)

Ein benutzerdefinierter Entitätswert mit einem einzelnen Wert ist genauso aufgebaut wie ein vordefiniertes Entitätsattribut mit nur einem Wert:

`entity.genre=genre1`

Ein benutzerdefiniertes Entitätsattribut mit mehreren Werten muss als gültiges JSON-Array festgelegt werden:

`entity.genre=["genre1", "genre2"]`

Beispiele für gültige JSON-Arrays, die von [!DNL Recommendations] unterstützt werden:

* `["AB","BC"]` alle Werte sind Zeichenfolgen
* `[1,2]` alle Werte sind numerisch

>[!NOTE]
>
>[!DNL Recommendations] unterstützt keine gemischten Werttypen in Attributen mit mehreren Werten `["AB",1,true, [1,2,3]]` ist beispielsweise ein gültiges JSON-Array, wird jedoch [!DNL Recommendations] nicht unterstützt, da es gemischte Werttypen enthält (Zeichenfolge, numerisch, boolesches Objekt, Objekt)

Wurde ein benutzerdefiniertes Attribut als gültiges JSON-Array übermittelt, wird das Attribut für alle Produkte im Katalog als Attribut mit mehreren Werten behandelt.

>[!NOTE]
>
>Um ein Attribut aus mehreren Werten zu einem einzelnen Wert zu ändern, müssen Sie Ihren Katalog löschen und die Produktdaten hochladen. Wird der Katalog gelöscht, bleiben die historischen Daten Ihrer Produkt-IDs jedoch erhalten. Weitere Informationen finden Sie unter [Löschen aller Artikel aus dem System](/help/main/assets/adobe-recommendations-classic.pdf) in der Dokumentation von *Adobe Recommendations Classic*.

**Einschränkungen**:

* Sie können keine voreingestellten Entitätsattributnamen für benutzerdefinierte Entitätsattribute verwenden. (Siehe [Entitätsattribute](/help/main/c-recommendations/c-products/entity-attributes.md#entity-attributes).)
* Das Attribut `entity.environment` ist vom System reserviert und kann nicht für benutzerdefinierte Entitätsattribute verwendet werden. Versuche, `entity.environment` mit `targetPageParams`, Feeds oder APIs zu übermitteln, werden ignoriert.
* Arrays müssen einen einzigen Werttyp enthalten. Arrays mit gemischten Werten (`["AB",1,true]`) werden nicht unterstützt.
* Ein Attribut mit mehreren Werten, das ein verschachteltes JSON-Array (`[10,12,[1,2,3]]`) enthält, wird als Attribut mit einem Wert behandelt.

## Implementieren von Attributen mit mehreren Werten {#section_80FEFE49E8AF415D99B739AA3CBA2A14}

Benutzerdefinierte Entitätsattribute mit mehreren Werten werden unterstützt, wenn Feeds (CSV), `targetPageParams` und die Bereitstellungs-API zum Hochladen von Produkten verwendet werden. Alte Werte werden durch neue Werte ersetzt, nicht ergänzt. Leere Arrays ( [] ) werden so behandelt, als hätten sie keine Werte.

Doppelte Anführungszeichen müssen mit Escapezeichen angegeben werden. Zum Beispiel ist `"[""test"", ""value""]"` ein gültiges JSON-Array, das in CSV verwendet werden kann.

### Verwenden von targetPageParams

Das folgende Beispiel zeigt die Verwendung von `targetPageParams`:

```javascript
function targetPageParams() { 
  return { 
    'entity.id':                   '123', 
    'entity.categoryId':            '["A", "A:B", "A:B:C", "A:B:C:D"]',        
    'entity.MultiValueAttribute':   '["X", "Y", "Z"]', 
    'entity.event.detailsOnly':     'true', 
    'excludedIds':                  '[123, 3232, 2323, 4344]', 
    'orderId':                      '123456', 
    'orderTotal':                   '195.32', 
    'productPurchaseId':            '[001,002,003]' 
  }; 
}
```

### Verwenden von CSV

Sie können Ihre CSV-Dateien im Rohformat verwalten, indem Sie einen Texteditor verwenden oder stattdessen mit einem Tabellenkalkulationsprogramm arbeiten.

Eine CSV-Datei im Rohformat sieht wie folgt aus:

![Multi-value_example_raw Bild](assets/multi-value_example_raw.png)

Der gleiche Katalog sieht im Tabellenformat so aus:

![Multi-value_example_excel Bild](assets/multi-value_example_excel.png)

Wird eine Tabelle in das .csv-Format konvertiert, werden vom Programm automatisch doppelte Anführungzeichen um Zelleninhalte gelegt, damit Kommata in den Zellenwerten nicht als Spaltentrennzeichen interpretiert werden. Außerdem werden doppelte Anführungszeichen um JSON-Zeichenfolgenwerte gelegt, die in benutzerdefinierten Attributen mit mehreren Werten enthalten sind. Die Arbeit mit der Rohdatei erschwert sich hierdurch etwas. Beispiel:

* Tabelle: `["1","2","3"]`
* Rohformat: `"[""1"",""2"",""3""]"`

Gehen Sie bei der direkten Bearbeitung einer CSV-Katalogdatei im Rohformat vorsichtig vor.

### Verwenden von APIs

Sie können Attribute mit mehreren Werten mithilfe der Bereitstellungs-API in einem Mbox-Parameter als Zeichenfolgenwert übergeben, der ein JSON-Array mit Escape-Zeichen enthält.

```javascript
"execute": {
    "mboxes": [
      {
        "index": 0,
        "name": "first-mbox",
        "parameters": {
          "entity.id": "32323",
          "entity.categoryId": "My Category",
          "entity.MultiValueAttribute": "[\"X\", \"Y\", \"Z\"]"
        }
      }
    ]
  }
```

Weitere Informationen zur Verwendung der Bereitstellungs- und [&#128279;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}-Entitäten-APIs finden Sie in der Dokumentation zur Adobe Recommendations-API .

## Verwenden von Operatoren mit Attributen mit mehreren Werten {#section_83C2288A805242D9A02EBC4F07DEE945}

Wenden Sie Operatoren nur für benutzerdefinierte Attribute mit mehreren Werten in Algorithmuseinschlussregeln, Katalogregeln und Ausschlussregeln an, lautet das Ergebnis *true* (wahr), wenn mindestens ein Wert in der Liste die Operation (Boolesches *or*) erfolgreich durchläuft.

Im folgenden Beispiel wird die Regel `message contains abc`.

* &#x200B;1. Fall: `entity.genre = ["ab", "bc", "de"]`. Das Ergebnis lautet „false“ (falsch), da keiner der Werte `abc`.
* &#x200B;2. Fall: `entity.genre = ["abcde","de","ef"]`. Das Ergebnis lautet „true“ (wahr), da einer der Werte `abc`.

Im Falle negativer Operatoren müssen alle Attributwerte die Operation (Boolesches *and*) erfolgreich durchlaufen. Wenn beispielsweise der Operator `notEquals` ist, ist das Ergebnis *false* wenn ein Wert übereinstimmt.

In der folgenden Tabelle wird zusammengefasst, wie sich die einzelnen Operatoren verhalten, und es werden die Fälle für jede Beispielregel aufgeführt.

| Operator | Ergebnis ist wahr, wenn | Beispielregel | Attributwert | Ergebnis | Grund |
|---|---|---|---|---|---|
| Gleich | Jeder Attributwert entspricht dem Eingabewert. | `genre equals abc` | `["ab", "bc", "de"]` | Falsch | Kein Wert ist gleich `abc`. |
|  |  |  | `["abc", "de", "ef"]` | Wahr | Ein Wert ist gleich `abc`. |
|  |  |  | `["abcde", "de", "ef"]` | Falsch | `abc` entspricht keinem Element in der Liste. |
| Ist nicht gleich | Kein Attributwert entspricht dem Eingabewert. | `genre not equals abc` | `["ab", "bc", "de"]` | Wahr | Kein Wert ist gleich `abc`. |
|  |  |  | `["abc", "de", "ef"]` | Falsch | Ein Wert ist gleich `abc`. |
|  |  |  | `["abcde", "de", "ef"]` | Wahr | `abc` entspricht keinem Element in der Liste. |
| Enthält | Jeder Attributwert enthält den Eingabewert. | `genre contains abc` | `["ab", "bc", "de"]` | Falsch | Kein Wert enthält `abc`. |
|  |  |  | `["abcde", "de", "ef"]` | Wahr | Ein Wert enthält `abc`. |
| Enthält nicht | Kein Attributwert enthält den Eingabewert. | `genre does not contain abc` | `["ab", "bc", "de"]` | Wahr | Kein Wert enthält `abc`. |
|  |  |  | `["abcde", "de", "ef"]` | Falsch | Ein Wert enthält `abc`. |
| Beginnt mit | Jeder Attributwert beginnt mit dem Eingabewert. | `genre starts with abc` | `["ab", "bc", "de"]` | Falsch | Kein Wert beginnt mit `abc`. |
|  |  |  | `["abcde", "de", "ef"]` | Wahr | Ein Wert beginnt mit `abc`. |
|  |  |  | `["ab", "de", "abc"]` | Wahr | Ein Wert beginnt mit `abc` (nicht unbedingt das erste Element in der Liste). |
| Endet mit | Jeder Attributwert endet mit dem Eingabewert. | `genre ends with abc` | `["ab", "bc", "de"]` | Falsch | Kein Wert endet mit `abc`. |
|  |  |  | `["deabc", "de", "ef"]` | Wahr | Ein Wert endet mit `abc`. |
| Größer als oder gleich (ausschließlich numerische Werte) | Jeder Attributwert ist größer oder gleich dem Eingabewert. Jeder Wert wird in Double konvertiert, und Werte, die nicht konvertiert werden können, werden übersprungen, während die Regel ausgeführt wird. | `price greater than or equal to 100` | `["10", "20", "45", "de"]` | Falsch | Kein Wert ist größer oder gleich 100. Der Wert `de` wurde übersprungen, weil er nicht verdoppelt werden kann. |
|  |  |  | `["100", "101", "90", "80"]` | Wahr | Zwei Werte sind größer oder gleich 100. |
| Kleiner als oder gleich (ausschließlich numerische Werte) | Jeder Attributwert ist kleiner oder gleich dem Eingabewert. Jeder Wert wird in Double konvertiert, und Werte, die nicht konvertiert werden können, werden übersprungen, während die Regel ausgeführt wird. | `price less than or equal to 100` | `["101", "200", "141", "de"]` | Falsch | Kein Wert ist kleiner oder gleich 100. Der Wert `de` wurde übersprungen, weil er nicht verdoppelt werden kann. |
|  |  |  | `["100", "101", "90", "80"]` | Wahr | Zwei Werte sind kleiner oder gleich 100. |
| Dynamische Übereinstimmungen (nur für artikelbasierte Algorithmen verfügbar) | Jeder Attributwert entspricht dem Eingabewert. | `genre matches abc` | `["ab", "bc", "de"]` | Falsch | Kein Wert entspricht `abc`. |
|  |  |  | `["abc", "de", "ef"]` | Wahr | Ein Wert entspricht `abc`. |
| Dynamische Nichtübereinstimmung (nur für artikelbasierte Algorithmen verfügbar) | Kein Attributwert entspricht dem Eingabewert. Wenn ein Attributwert übereinstimmt, ist das Ergebnis falsch. | `genre does not match abc` | `["ab", "bc", "de"]` | Wahr | Kein Wert entspricht `abc`. |
|  |  |  | `["abc", "de", "ef"]` | Falsch | Ein Wert entspricht `abc`. |
| Dynamische Bereiche (nur für artikelbasierte Algorithmen verfügbar, ausschließlich numerische Werte) | Jeder numerische Attributwert liegt innerhalb des angegebenen Bereichs. | `price dynamically ranges in 80% to 120% of 100` | `["101", "200", "125", "de"]` | Wahr | `101` liegt im Bereich von 80 % bis 120 % von 100. Der Wert `de` wurde übersprungen, weil er nicht verdoppelt werden kann. |
|  |  |  | `["130", "191", "60", "75"]` | Falsch | Kein Wert liegt im Bereich von 80 % bis 120 % von 100. |

>[!NOTE]
>
>*Double* ist ein Java-Datentyp. Bei Operatoren, für die numerische Werte erforderlich sind, werden bei der Verdoppelung alle Werte aus der Ergebnisberechnung ausgeschlossen, die nicht numerisch sind.

## Attribute mit mehreren Werten in Designs {#section_F672E4F6E1D44B3196B7ADE89334ED4A}

Attribute mit mehreren Werten werden als kommagetrennte Liste angezeigt, wenn sie in einem Design referenziert werden.

Beispiel:

Wenn auf `entity.genre=["genre1","genre2"]` in einem Entwurf als `$entity<N>.genre` verwiesen wird, lautet das Ergebnis `genre1, genre2`.

## Verwandte Themen

* [Entitätsattribute](/help/main/c-recommendations/c-products/entity-attributes.md#entity-attributes)
