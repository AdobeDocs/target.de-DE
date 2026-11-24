---
keywords: Einschlussregeln;Einschlusskriterien;Recommendations;Promotion;Promotions;dynamische Filterung;dynamische Parameterübereinstimmung
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Recommendations dynamisch filtern können, indem Sie Elemente (Entitäten) mit einem Wert in der Anfrage (API oder Mbox) vergleichen.
title: Parameterübereinstimmung
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
TQID: 'https://experienceleague.adobe.com/GTli-O1p4Gm2Fg9J-L0ukQ8dSw2t-da8OatFLP8Ks9g'
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
source-wordcount: '311'
ht-degree: 8%
---
# Parameterübereinstimmung {#parameter-matching}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Empfehlungen dynamisch in [!DNL Adobe Target Recommendations] filtern können, indem Sie Elemente (Entitäten) mit einem Wert in der Anfrage (API oder Mbox) vergleichen.

>[!ENDSHADEBOX]

**[!UICONTROL Parameterübereinstimmung]** empfiehlt nur den Inhalt, der den Seitenparametern oder den Parametern des Besuchers entspricht, z. B. Geräteabmessungen oder Geografie. Beispielsweise können nur Inhalte empfohlen werden, die dem Seitenparameter „Industry“ entsprechen. Der Prozess zum Erstellen und Verwenden von Einschlussregeln für Kriterien und Promotions ist ähnlich, genauso wie die Anwendungsfälle und Beispiele. Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

Weitere Beispiele:

* Mbox-Parameter für Bildschirmbreite und -höhe können verwendet werden, um mobile Besucher anzusprechen und nur Mobilgeräte und Zubehör zu empfehlen.
* Eine Recommendations-Regel kann nur die meistverkauften Mobiltelefone zurückgeben, die mit der Bildschirmhöhe des Mobilgeräts, das der Besucher zum Anzeigen der Seite verwendet, übereinstimmen oder diese überschreiten.
* Regionale Standortparameter können verwendet werden, um im Winter Empfehlungen für Werkzeuge zurückzugeben. Schneefräsen und andere Schneeminderungswerkzeuge können für Besucher in Gebieten empfohlen werden, in denen es schneit, aber nicht für Besucher in Gebieten, in denen es nicht schneit.

## Beispiele für Parameterübereinstimmung

[!DNL Recommendations] können mit Parameterwerten übereinstimmen, die im [!DNL Target] Aufruf gesendet werden. Im folgenden Beispiel erkennt [!DNL Target] anhand der im [!DNL Target]-Aufruf gesendeten Parameter Bildschirmhöhe und Breite, dass ein Besucher ein Mobilgerät verwendet, und empfiehlt nur Elemente, die Mobilgeräte sind.

Betrachten Sie das folgende [!DNL Target]:

![Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Auf der Seite, die eine Besucherin oder ein Besucher anzeigt, werden Produkte für Mobilgeräte angezeigt.

![Produkte für Mobilgeräte](/help/main/c-recommendations/c-algorithms/assets/phones.png)
