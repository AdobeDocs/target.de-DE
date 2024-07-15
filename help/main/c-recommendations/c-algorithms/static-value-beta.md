---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; statisch; statischer Filter
description: Erfahren Sie, wie Sie manuell einen oder mehrere statische Werte eingeben, um mithilfe von Einschlussregeln in Adobe [!DNL Target] Recommendations zu filtern.
title: Wie kann ich in Recommendations-Aktivitäten nach statischen Werten filtern?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6a55260fd49e07e2b217f6becfbc778251a5d0d
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 45%

---

# [!UICONTROL Static Filter]

Geben Sie manuell einen oder mehrere statische Werte ein, um mithilfe von Einschlussregeln in [!DNL Adobe Target Recommendations] zu filtern.

Beispielsweise nur empfohlene Inhalte mit einer Motion Picture Association (MPA)-Bewertung von &quot;G&quot;oder &quot;PG&quot;.

Sie können so viele Einschlussregeln wie benötigt erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

>[!NOTE]
>
>Wenn Sie wissen, wie die Einschlussregeln vor der Target 17.6.1-Version (Juni 2017) konfiguriert waren, werden Sie bemerken, dass einige der Optionen und Operatoren sich geändert haben. Es werden nur die Operatoren angezeigt, die auf die ausgewählte Option angewendet werden können. Zudem wurden einige Operatoren umbenannt („stimmt überein“ heißt jetzt „gleich“), um die Konsistenz und die Intuitivität zu erhöhen. Alle vorhandenen Ausschlussregeln, die vor dieser Version erstellt worden sind, wurden automatisch in die neue Struktur migriert. Es ist keine Neustrukturierung Ihrerseits nötig.

## Empfohlener Inhalt mit G oder PG

Um eine Einschlussregel mit statischen Werten zu erstellen, um Inhalte mit einer MPA-Bewertung von &quot;G&quot;oder &quot;PG&quot;zu empfehlen (ausgenommen Inhalt von &quot;R&quot;und &quot;NC17&quot;), können Sie die folgenden Filterregeln erstellen: &quot;Filmerierung entspricht einer g-bewerteten Version&quot;und &quot;Filmerierung entspricht einer der Pg-Bewertungen&quot;.
