---
keywords: mehrere Werte;Attribute;Recommendations;mehrere Werte;mehrere Werte;mehrere Werte
description: Erfahren Sie, wie Sie in [!DNL Target Recommendations] mit einem Feld mit mehreren Werten arbeiten können, indem Sie spezielle Operatoren für mehrere Werte verwenden.
title: Arbeiten mit Attributen mit mehreren Werten
feature: Recommendations
exl-id: 82018a9a-0983-458c-9387-3602dab4409b
TQID: 'https://experienceleague.adobe.com/FrjVxvYfGh2o-qomXRbVh6WS6f65Mja41gBMhejEPlE'
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
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 2%
---
# Arbeiten mit Attributen mit mehreren Werten {#multi-value-attributes}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Daten mit mehreren Werten an [!DNL Adobe Target Recommendations] senden und in Einschlussregeln mit den Operatoren mit mehreren Werten verwenden können.

>[!ENDSHADEBOX]

Ein Feld mit mehreren Werten enthält mehrere Werte für dasselbe Element oder denselben Besucher. Beispiel:

* Filme, die Benutzern angeboten werden: Ein Film hat mehrere Schauspieler.
* Tickets für Konzerte: ein bestimmter Nutzer hat mehrere Lieblingsbands.
* Bekleidung verkauft: Ein Hemd ist in mehreren Größen erhältlich.

Um Empfehlungen in diesen Szenarien zu verarbeiten, können Daten mit mehreren Werten an [!DNL Target Recommendations] übergeben und mit speziellen Operatoren für mehrere Werte verwendet werden.

## Senden von Daten mit mehreren Werten {#send}

Damit [!DNL Recommendations] Daten mit mehreren Werten identifizieren können, sollten sie als JSON-Array gesendet werden.

Einen Parameter mit mehreren Werten in JavaScript (`targetPageParams`) finden Sie unter [Implementieren von Attributen mit mehreren Werten](/help/main/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Benutzerdefinierte Entitätsattribute*.

In einer CSV-Datei wird ein Entitätsattribut mit mehreren Werten als JSON-Array in der Zelle des Attributs gesendet, wie im folgenden Beispiel dargestellt.

+++ CSV-Beispieldatei mit einem Attribut mit mehreren Werten

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

+++

Wenn ein Entitätsattribut, ein Profilattribut oder ein Mbox-Parameter als Mehrfachwert in diesem Format angegeben wird, leitet [!DNL Recommendations] automatisch davon ab, dass das Feld mehrwertig ist.

## Verwenden von Attributen mit mehreren Werten in Einschlussregeln {#multi-value-inclusion-rules}

Die folgenden Operatoren sind für die Verwendung mit Entitäts-, Profil- und Mbox-Attributen mit mehreren Werten verfügbar:

* **[!UICONTROL Ist in Liste enthalten]**
* **[!UICONTROL ist nicht in der Liste enthalten]**

>[!NOTE]
>
>Die Unterstützung für die dynamische Zuordnung zu Attributen mit mehreren Werten ist derzeit nur bei Kriterien verfügbar, die eine Regel für die Zuordnung von Profilattributen oder Parametern (Mbox)-Attributen verwenden, die einen einzelnen Wert auf der linken Seite mit einem Mehrfachwert auf der rechten Seite vergleicht. Attribute mit mehreren Werten werden derzeit nicht in Promotions, in der Zuordnung von Entitätsattributen oder für Listen auf der linken Seite von Einschlussregeln unterstützt.

### Beispiel: Ausschließen kürzlich angesehener Elemente

Um zu verhindern, dass Filme aus den letzten zehn angezeigten Filmen des Benutzers empfohlen werden, schreiben Sie zunächst ein Profilskript namens `user.lastWatchedMovies`, das die letzten zehn angezeigten Filme als JSON-Array verfolgt. Die Elemente können dann mit der folgenden Einschlussregel ausgeschlossen werden:

```
Profile Attribute Matching
id - is not contained in list - user.lastWatchedMovies
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

Um Konzerttickets nur dann zu empfehlen, wenn das Bandspiel zu den Lieblingsbands des Benutzers gehört, sind zwei Elemente erforderlich: eine Profilvariable mit dem Namen `profile.favoriteBands`, die die Lieblingsbands des Benutzers enthält, und ein `entity.artistPerforming` im Katalog, das den im Konzert auftretenden Künstler enthält. Die folgende Einschlussregel kann dann verwendet werden:

```
Profile Attribute Matching
artistPerforming - is contained in list - profile.favoriteBands
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

Kriterien, die Filterregeln mit mehreren Werten verwenden, können wie alle Kriterien über die [!DNL Adobe Target]-APIs erstellt werden. Der folgende Beispiel-API-Aufruf erstellt ein Kriterium, bei dem das Entitätsattribut `id` in der `favorites` der Mbox-Parameter enthalten ist:

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

Dieser Aufruf ist mit JavaScript auf der Seite gepaart, die den Inhalt der Favoriten übergibt:

```
<!-- pass in the value of mbox parameter "favorites" as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
