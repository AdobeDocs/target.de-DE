---
keywords: Einschlussregeln;Einschlusskriterien;Empfehlungen;Promotion;Promotions;Dynamische Filterung;statisch;statischer Filter
description: Erfahren Sie, wie Sie manuell einen oder mehrere statische Werte eingeben, um mithilfe von Einschlussregeln in Adobe [!DNL Target] Recommendations zu filtern.
title: Wie kann ich in Recommendations-Aktivitäten nach statischen Werten filtern?
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 46%

---

# ![](/help/assets/premium.png) PREMIUMStatic Filter

Geben Sie manuell einen oder mehrere statische Werte ein, um mithilfe von Einschlussregeln in [!DNL Adobe Target] [!DNL Recommendations] zu filtern.

Empfehlen Sie zum Beispiel nur Inhalte mit einer MPA-Bewertung von &quot;G&quot;oder &quot;PG&quot;.

Sie können so viele Einschlussregeln wie benötigt erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

>[!NOTE]
>
>Wenn Sie wissen, wie die Einschlussregeln vor der Target 17.6.1-Version (Juni 2017) konfiguriert waren, werden Sie bemerken, dass einige der Optionen und Operatoren sich geändert haben. Es werden nur die Operatoren angezeigt, die auf die ausgewählte Option angewendet werden können. Zudem wurden einige Operatoren umbenannt („stimmt überein“ heißt jetzt „gleich“), um die Konsistenz und die Intuitivität zu erhöhen. Alle vorhandenen Ausschlussregeln, die vor dieser Version erstellt worden sind, wurden automatisch in die neue Struktur migriert. Es ist keine Neustrukturierung Ihrerseits nötig.

## Empfohlene Inhalte mit G oder PG

Um eine Einschlussregel mit statischen Werten zu erstellen, mit der Inhalte mit einer MPA-Bewertung von &quot;G&quot;oder &quot;PG&quot;empfohlen werden (ausschließen Sie &quot;R&quot;- und &quot;NC17&quot;-Inhalte), können Sie die folgenden Filterregeln erstellen: &quot;Filmbewertung gleich g-Bewertung&quot;und &quot;Filmbewertung gleich pg-bewertet&quot;, wie unten dargestellt.

![Beispiel für Filmbewertung](/help/c-recommendations/c-algorithms/assets/movies.png)
