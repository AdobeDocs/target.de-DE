---
keywords: Einschlussregeln; Einschlusskriterien; Recommendations; Promotion; Promotions; dynamische Filterung; statisch; statischer Filter
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Recommendations einen oder mehrere statische Werte manuell eingeben, um mithilfe von Einschlussregeln zu filtern.
title: Statischer Filter
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
TQID: 'https://experienceleague.adobe.com/-HTJO4YFi0-isyA-5LbVUaEPu7YX1WFgPy-OexMSXFY'
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
source-wordcount: '184'
ht-degree: 2%
---
# Statischer Filter {#static-filter}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Empfehlungen filtern können, indem Sie einen oder mehrere statische Werte in Einschlussregeln in [!DNL Adobe Target Recommendations] manuell eingeben.

>[!ENDSHADEBOX]

**[!UICONTROL Statischer Filter]** beschränkt die Elemente in einer Empfehlung auf die Elemente, die mit manuell eingegebenen statischen Werten übereinstimmen. Es können beliebig viele Einschlussregeln erstellt werden. Die Einschlussregeln sind mit einem AND-Operator verknüpft, sodass alle Regeln erfüllt sein müssen, damit ein Element in einer Empfehlung enthalten ist. Allgemeine Informationen zu Einschlussregeln finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Empfohlene Inhalte mit G oder PG

Um nur Inhalte mit einer MPA-Bewertung (Motion Picture Association) von „G“ oder „PG“ zu empfehlen (ausschließen von „R“- und „NC17“-Inhalten), erstellen Sie eine Filterregel mit dem Operator „Filmbewertung gleich einem von“ und geben Sie die Werte „g-Bewertung“ und „pg-Bewertung“ ein.
