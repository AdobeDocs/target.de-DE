---
keywords: Produkt; Sammlungen
description: Erfahren Sie mehr über Entitäten in Adobe [!DNL Target] Recommendations. Entitäten beziehen sich auf die Elemente, die Sie für die Verwendung von [!DNL Target] empfehlen möchten, z. B. Artikel, Filme oder Produkte.
title: Wie verwende ich Entitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: ffe23eea-b914-4c86-ad54-c63c1cc1c0d7
TQID: 'https://experienceleague.adobe.com/zfISb59XJ5qrD1-FA0syglPPswIL8cA0N0pBpY4tgIE'
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
source-wordcount: '288'
ht-degree: 1%
---
# Erste Schritte mit Entitäten {#get-started-entities}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, welche Entitäten sich in [!DNL Adobe Target Recommendations] befinden und wo Sie sie verwalten können.

>[!ENDSHADEBOX]

Entitäten sind die Elemente, die [!DNL Recommendations] empfehlen können. Eine Entität kann ein Produkt, ein Inhaltselement (z. B. ein Artikel, eine Slideshow, ein Bild, ein Film oder eine TV-Show), eine Auftragsliste, ein Restaurant usw. sein.

[!DNL Recommendations] zeigt Elemente aus Ihren Sammlungen gemäß den von Ihnen festgelegten Kriterien an.

## So erreichen Entitäten Recommendations

Informationen zu Ihren Entitäten können auf verschiedene Weise an [!DNL Recommendations] übergeben werden, darunter:

* Mit [Entitätsattributen](/help/main/c-recommendations/c-products/entity-attributes.md) die von Ihren Seiten mithilfe einer Mbox oder eines `targetPageParams` gesendet werden.
* Mit [feeds](/help/main/c-recommendations/c-products/feeds.md) , das CSV-Dateien, das [!DNL Google Product Search]-Feed-Format oder [!DNL Adobe Analytics] Produktklassifizierungen verwenden kann.
* Mit der Bereitstellungs-API.

Wenn [!DNL Target] Daten für ein Element sowohl aus einem Feed als auch aus einer Mbox erfasst, werden die neuesten Daten verwendet.

Hochgeladene Entitäten und Entitätsattributwerte laufen nach 61 Tagen ab. Senden Sie jedes Element mindestens einmal alle 60 Tage erneut. Andernfalls betrachtet [!DNL Target] das Element als nicht mehr relevant und entfernt es aus dem Katalog.

## Verwalten von Entitäten

Verwenden Sie die folgenden Seiten, um mit Ihren Entitäten zu arbeiten:

* [Entitätsattribute](/help/main/c-recommendations/c-products/entity-attributes.md) und [Benutzerdefinierte Entitätsattribute](/help/main/c-recommendations/c-products/custom-entity-attributes.md): Definieren Sie die Produkt- oder Inhaltsinformationen, die Sie an [!DNL Recommendations] übergeben.
* [Feeds](/help/main/c-recommendations/c-products/feeds.md): Holen Sie Entitäts- oder Inhaltsinformationen in Ihre Empfehlungen.
* [Katalogsuche](/help/main/c-recommendations/c-products/catalog-search.md): Suchen Sie Elemente in Ihrem Katalog.
* [Sammlungen](/help/main/c-recommendations/c-products/collections.md): Richten Sie Ihre Sammlungen ein. Beim Erstellen einer [!DNL Recommendations]-Aktivität wird für jedes Erlebnis eine Sammlung ausgewählt.
* [Ausschlüsse](/help/main/c-recommendations/c-products/exclusions.md): Verhindern Sie, dass bestimmte Elemente in Ihren Empfehlungen angezeigt werden. Ausschlüsse gelten für alle Aktivitäten im Konto.
