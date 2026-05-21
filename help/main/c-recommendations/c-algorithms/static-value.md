---
keywords: Einschlussregeln; Einschlusskriterien; Recommendations; Promotion; Promotions; dynamische Filterung; statisch; statischer Filter
description: Erfahren Sie, wie Sie in Adobe-Recommendations einen oder mehrere statische Werte manuell eingeben, um mithilfe von Einschlussregeln  [!DNL Target]  filtern.
title: Wie kann ich in Recommendations-Aktivitäten nach statischen Werten filtern?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
TQID: https://experienceleague.adobe.com/-HTJO4YFi0-isyA-5LbVUaEPu7YX1WFgPy-OexMSXFY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 43%

---

# [!UICONTROL Static Filter]

Geben Sie manuell einen oder mehrere statische Werte ein, um mithilfe von Einschlussregeln in [!DNL Adobe Target Recommendations] zu filtern.

Empfehlen Sie beispielsweise nur Inhalte mit der Bewertung „G“ oder „PG“ für die Motion Picture Association (MPA).

Sie können so viele Einschlussregeln wie benötigt erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

>[!NOTE]
>
>Wenn Sie wissen, wie die Einschlussregeln vor der Target 17.6.1-Version (Juni 2017) konfiguriert waren, werden Sie bemerken, dass einige der Optionen und Operatoren sich geändert haben. Es werden nur die Operatoren angezeigt, die auf die ausgewählte Option angewendet werden können. Zudem wurden einige Operatoren umbenannt („stimmt überein“ heißt jetzt „gleich“), um die Konsistenz und die Intuitivität zu erhöhen. Alle vorhandenen Ausschlussregeln, die vor dieser Version erstellt worden sind, wurden automatisch in die neue Struktur migriert. Es ist keine Neustrukturierung Ihrerseits nötig.

## Empfohlene Inhalte mit G oder PG

Um eine Einschlussregel mit statischen Werten zu erstellen, um Inhalte mit einer MPA-Bewertung von nur „G“ oder „PG“ zu empfehlen (ausschließen von „R“- und „NC17“-Inhalten), können Sie die folgenden Filterregeln erstellen: „Filmbewertung entspricht einem von g-bewerteten“ und „Filmbewertung entspricht einem von pg-bewerteten“.
