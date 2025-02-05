---
keywords: mehrere Werte;Attribute;Recommendations;mehrere Werte;mehrere Werte;mehrere Werte
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Recommendations mit einem Feld mit mehreren Werten arbeiten können, indem Sie bestimmte Operatoren für mehrere Werte verwenden, z. B. wenn Sie Filme mit mehreren Akteuren empfehlen.
title: Kann ich in Recommendations Attribute mit mehreren Werten verwenden?
feature: Recommendations
exl-id: 82018a9a-0983-458c-9387-3602dab4409b
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 9%

---

# Arbeiten mit Attributen mit mehreren Werten

Manchmal empfiehlt es sich, ein Feld mit mehreren Werten zu verwenden. Sehen Sie sich folgende Beispiele an:

* Sie bieten Benutzern Spielfilme an. In der Regel wirken an jedem Film mehrere Schauspieler mit.
* Sie verkaufen Konzerttickets. Die meisten Benutzer haben mehrere Lieblingsbands.
* Sie verkaufen Bekleidung. Jedes Hemd ist in verschiedenen Größen erhältlich.

Um Empfehlungen in diesen Szenarien zu verarbeiten, können Sie Daten mit mehreren Werten an [!DNL Target Recommendations] übergeben und spezielle Operatoren für mehrere Werte verwenden.

Damit [!DNL Recommendations] Daten mit mehreren Werten identifizieren können, sollten sie als JSON-Array gesendet werden, wie in den folgenden Code-Beispielen dargestellt.

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

Weitere Informationen finden Sie unter [Implementieren von Attributen mit mehreren Werten](/help/main/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Benutzerdefinierte Entitätsattribute*.

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

Wenn ein Entitätsattribut, ein Profilattribut oder ein Mbox-Parameter als Mehrfachwert gemäß dem oben genannten Format angegeben wird, leitet [!DNL Recommendations] automatisch davon ab, dass das Feld mehrwertig ist.

Die folgenden Operatoren sind für die Verwendung mit Entitäts-, Profil- und Mbox-Attributen mit mehreren Werten verfügbar:

* [!UICONTROL is contained in list]
* [!UICONTROL is not contained in list]

## Arbeiten mit Attributen mit mehreren Werten in Einschlussregeln

>[!NOTE]
>
>Die Unterstützung für die dynamische Zuordnung zu Attributen mit mehreren Werten ist derzeit nur in Kriterien verfügbar, wenn eine Regel für die Zuordnung von Profilattributen oder Parametern (Mbox)-Attributvergleiche beim Vergleich eines einzelnen Werts auf der linken Seite mit einer rechten Seite mit mehreren Werten verwendet wird. Attribute mit mehreren Werten werden derzeit nicht in Promotions, in der Zuordnung von Entitätsattributen oder für Listen auf der linken Seite von Einschlussregeln unterstützt.

### Beispiel: Ausschließen kürzlich angesehener Elemente

Angenommen, Sie möchten verhindern, dass Filme, die zu den zehn zuletzt angesehenen Filmen des Benutzers gehören, empfohlen werden. Schreiben Sie zunächst ein Profilskript mit dem Namen `user.lastWatchedMovies`, um die letzten zehn angezeigten Filme als JSON-Array zu verfolgen. Anschließend können Sie die Elemente mithilfe der folgenden Einschlussregel ausschließen:

```
`Profile Attribute Matching`
`id - is not contained in list - user.lastWatchedMovies`
```

JSON-API-Darstellung der Einschlussregel:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": "user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### Beispiel: Empfohlene Elemente aus den Favoriten des Benutzers

Angenommen, Sie möchten Tickets nur für Konzerte empfehlen, wenn die Band, die spielt, eine der Lieblingsbands des Benutzers ist. Stellen Sie zunächst sicher, dass Sie über eine Profilvariable mit dem Namen `profile.favoriteBands` verfügen, die die Lieblingsbands der Benutzenden enthält. Stellen Sie dann sicher, dass Ihr Katalog eine `entity.artistPerforming` enthält, die den Künstler enthält, der im Konzert auftritt. Anschließend können Sie die folgende Einschlussregel verwenden:

```
`Profile Attribute Matching`
`artistPerforming - is contained in list - profile.favoriteBands`
```

JSON-API-Darstellung der Einschlussregel:

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

### Beispiel: API-Erstellung von Kriterien, die Elemente aus den Favoriten eines Benutzers empfehlen

Kriterien, die Filterregeln mit mehreren Werten verwenden, können wie alle Kriterien über Adobe I/O-APIs erstellt werden. Ein Beispiel für einen API-Aufruf zum Erstellen eines Kriteriums, bei dem das Entitätsattribut `id` in der `favorites` der Mbox-Parameter enthalten ist:

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

Dieser würde mit JavaScript auf der Seite gepaart, um die Favoriteninhalte zu übergeben:

```
<!-- pass in the value of mbox parameter “favorites” as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
