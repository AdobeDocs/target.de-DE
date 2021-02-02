---
keywords: Einschlussregeln;Einschlusskriterien;Empfehlungen;Promotion;Promotions;Dynamische Filterung;statisch;statischer Filter
description: Geben Sie manuell einen oder mehrere statische Werte ein, um nach Einschlussregeln in Adobe Target Recommendations zu filtern.
title: Filtern nach statischen Werten in Einschlussregeln in Adobe Target Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '225'
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

