---
keywords: multi-value;attributes;recommendations;multi value;multivalue;multi-value
description: Informationen zum Arbeiten mit einem Multi-Value-Feld in Adobe Target Recommendations unter Verwendung spezieller Multi-Value-Operatoren.
title: Arbeiten mit Attributen mit mehreren Werten in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 381c405e55475f2474881541698d69b87eddf6fb
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---


# Arbeiten mit Attributen mit mehreren Werten

Manchmal möchten Sie mit einem Feld mit mehreren Werten arbeiten. Sehen Sie sich folgende Beispiele an:

* Sie können Angebote an Benutzer senden. Ein Film hat mehrere Schauspieler.
* Sie verkaufen Tickets für Konzerte. Ein Benutzer hat mehrere Lieblingsbands.
* Du verkaufst Kleidung. Ein Hemd ist in verschiedenen Größen erhältlich.

Um Empfehlungen in diesen Szenarien zu bearbeiten, können Sie Daten mit mehreren Werten an spezielle Operatoren weiterleiten [!DNL Target Recommendations] und diese verwenden.

Um Daten mit mehreren Werten [!DNL Recommendations] zu identifizieren, sollten diese wie in den folgenden Codebeispielen als JSON-Array gesendet werden.

## Übergeben eines Parameters mit mehreren Werten in JavaScript

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

Weitere Informationen finden Sie unter [Implementieren von Attributen](/help/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) mit mehreren Werten in *benutzerdefinierten Entitätsattributen*.

## Übergeben eines Entitätsattributs mit mehreren Werten in einer CSV-Datei

```
## RECSRecommendations Upload File,,,,,,,,,,,,,,,,,,,
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines.,,,,,,,,,,,,,,,,,,,
## RECS,,,,,,,,,,,,,,,,,,,
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left.,,,,,,,,,,,,,,,,,,,
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'.,,,,,,,,,,,,,,,,,,,
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations.,,,,,,,,,,,,,,,,,,,
## RECSentity.id ,entity.name,entity. categoryId ,entity. message ,entity.thumbnailUrl ,entity.value ,entity.pageUrl ,entity.inventory ,entity.margin ,entity.custom1 ,entity.custom2 ,entity.custom3 ,entity.custom4,entity.custom5,entity.custom6,entity.custom7,entity.custom8,entity.custom9,entity.custom10,
1,Sample Product 1,category1,Save 10%,http://sample.store/products/images/product1_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=1,1000,48,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
2,Sample Product 2,category1,Save 10%,http://sample.store/products/images/product2_th.jpg,369,http://sample.store/products/product_detail.jsp?productId=2,1000,52,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
3,Sample Product 3,category1,Save 10%,http://sample.store/products/images/product3_th.jpg,479,http://sample.store/products/product_detail.jsp?productId=3,1000,78,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
4,Sample Product 4,category1,Save 10%,http://sample.store/products/images/product4_th.jpg,409,http://sample.store/products/product_detail.jsp?productId=4,1000,66,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
5,Sample Product 5,category1,Save 10%,http://sample.store/products/images/product5_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=5,1000,45,a,"[ ""v1"", ""v2"" ]",,,,,,,,, 
```

Wenn ein Entitätsattribut, ein Profil- oder ein mbox-Parameter gemäß dem oben stehenden Format als Mehrwert bereitgestellt wird, deutet [!DNL Recommendations] dies automatisch darauf hin, dass es sich um ein Mehrwert handelt.

Die folgenden Operatoren stehen für Entitäts-, Profil- und Mbox-Attribute mit mehreren Werten zur Verfügung:

* [!UICONTROL in der Liste]
* [!UICONTROL ist nicht in der Liste enthalten]

## Arbeiten mit Attributen mit mehreren Werten in Einschlussregeln

>[!NOTE]
>
>Die Unterstützung für die dynamische Zuordnung zu Attributen mit mehreren Werten ist derzeit nur in Kriterien verfügbar, wenn beim Vergleich eines Profil-Attributzuweises oder einer Parameterzuordnungsregel (mbox) ein einzelner Wert links mit einem Mehrwert rechts verglichen wird. Attribute mit mehreren Werten werden derzeit nicht in Promotions, Entitätsattributzuordnung oder für Listen auf der linken Seite von Einschlussregeln unterstützt.

### Beispiel: Zuletzt überwachte Elemente ausschließen

Angenommen, Sie möchten verhindern, dass Filme, die sich in den letzten zehn überwachten Filmen des Benutzers befinden, empfohlen werden. Schreiben Sie zunächst ein Profil-Skript, das aufgerufen wird, um die letzten zehn angezeigten Filme als JSON-Array `user.lastWatchedMovies` zu verfolgen. Anschließend können Sie die Elemente mithilfe der folgenden Einschlussregel ausschließen:

```
`Profile Attribute Matching`
`id - is not contained in list - user.lastWatchedMovies`
```

JSON API-Darstellung der Einschlussregel:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": " user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### Beispiel: Artikel aus den Favoriten des Benutzers empfehlen

Angenommen, Sie möchten Tickets nur zu Konzerten empfehlen, wenn die Band, die spielt, eine der Lieblingsbands des Benutzers ist. Vergewissern Sie sich zunächst, dass Sie über eine Profil-Variable mit dem Namen `profile.favoriteBands` verfügen, die die Lieblingsbänder des Benutzers enthält. Stellen Sie dann sicher, dass Ihr Katalog ein Attribut enthält, `entity.artistPerforming` das den Künstler enthält, der im Konzert auftritt. Anschließend können Sie die folgende Einschlussregel verwenden:

```
`Profile Attribute Matching`
`artistPerforming - is contained in list - profile.favoriteBands`
```

JSON API-Darstellung der Einschlussregel:

```
{
    "attribute": "artistPerforming",
    "operation": "isContainedInList",
    "source": {
        "name": "profile.favoriteBands",
        "type": "PROFILE"
    }
}
```

### Beispiel: API-Erstellung von Kriterien, die Artikel aus den Favoriten eines Benutzers empfehlen

Kriterien mit Filterregeln mit mehreren Werten können wie alle Kriterien über Adoben-I/O-APIs erstellt werden. Ein Beispiel-API-Aufruf zum Erstellen eines Kriteriums, bei dem das Entitätsattribut in der Liste der mbox-Parameter enthalten `id` ist, finden Sie hier `favorites` :

```
curl -X POST \
  https://<serverhost>/api/recs/<client>/criteria/item \
  -H 'Accept: application/vnd.adobe.target.v1+json' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: <from API client>' \
  -H 'X-Target-user-email: <email address>' \
  -H 'cache-control: no-cache' \
  -d '{
    "name": "viewed criteria",
    "criteriaTitle": "test title",
    "type": "VIEWED_CF",
    "key": "CURRENT",
    "daysCount": "TWO_WEEKS",
    "aggregation": "NONE",
    "backupDisabled": false,
    "partialDesignAllowed": true,
    "configuration": {
        "inclusionRules": [
            {
                "attribute": "id",
                "operation": "isContainedInList",
                "source": {
                    "name": "mbox.favorites",
                    "type": "MBOX"
                }
            }
        ]
    }
}'
```

Dies würde mit JavaScript auf der Seite gepaart, um die Favoriteninhalte weiterzugeben:

```
<!-- pass in the value of mbox parameter “favorites” as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
