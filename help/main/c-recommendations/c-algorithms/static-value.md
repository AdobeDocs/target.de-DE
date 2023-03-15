---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; statisch; statischer Filter
description: Erfahren Sie, wie Sie manuell einen oder mehrere statische Werte eingeben, um mithilfe von Einschlussregeln in Adobe zu filtern. [!DNL Target] Recommendations.
title: Wie kann ich in Recommendations-Aktivitäten nach statischen Werten filtern?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 47%

---

# Statischer Filter

Geben Sie einen oder mehrere statische Werte manuell ein, die mithilfe von Einschlussregeln gefiltert werden sollen in [!DNL Adobe Target] [!DNL Recommendations].

Beispielsweise nur empfohlene Inhalte mit einer Motion Picture Association (MPA)-Bewertung von &quot;G&quot;oder &quot;PG&quot;.

Sie können so viele Einschlussregeln wie benötigt erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

>[!NOTE]
>
>Wenn Sie wissen, wie die Einschlussregeln vor der Target 17.6.1-Version (Juni 2017) konfiguriert waren, werden Sie bemerken, dass einige der Optionen und Operatoren sich geändert haben. Es werden nur die Operatoren angezeigt, die auf die ausgewählte Option angewendet werden können. Zudem wurden einige Operatoren umbenannt („stimmt überein“ heißt jetzt „gleich“), um die Konsistenz und die Intuitivität zu erhöhen. Alle vorhandenen Ausschlussregeln, die vor dieser Version erstellt worden sind, wurden automatisch in die neue Struktur migriert. Es ist keine Neustrukturierung Ihrerseits nötig.

## Empfohlener Inhalt mit G oder PG

Um eine Einschlussregel mit statischen Werten zu erstellen, um Inhalte mit einer MPA-Bewertung von &quot;G&quot;oder &quot;PG&quot;zu empfehlen (ohne Inhalt von &quot;R&quot;und &quot;NC17&quot;), können Sie die folgenden Filterregeln erstellen: &quot;Filmerierung ist gleich g-bewertet&quot;und &quot;Filmerierung gleich pg-bewertet&quot;, wie unten dargestellt.

![Beispiel für Filmbewertung](/help/main/c-recommendations/c-algorithms/assets/movies.png)
