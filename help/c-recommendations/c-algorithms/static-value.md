---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;static;static filter
description: Geben Sie manuell einen oder mehrere statische Werte ein, um nach Einschlussregeln in Adobe Target Recommendations zu filtern.
title: Filtern nach statischen Werten in Einschlussregeln in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 75%

---


# ![PREMIUM](/help/assets/premium.png) Statischer Filter

Geben Sie manuell einen oder mehrere statische Werte ein, um nach Einschlussregeln in Adobe Target Recommendations zu filtern.

Beispielsweise nur empfohlene Inhalte mit der MPAA-Einstufung „G“ oder „PG“.

Verfügbare Operatoren:

* gleich
* ist nicht gleich
* enthält
* „Enthält nicht“
* beginnt mit
* endet mit
* Wert vorhanden
* Wert nicht vorhanden
* größer als oder gleich
* kleiner als oder gleich

>[!NOTE]
>
>Wenn Sie wissen, wie die Einschlussregeln vor der Target 17.6.1-Version (Juni 2017) konfiguriert waren, werden Sie bemerken, dass einige der Optionen und Operatoren sich geändert haben. Es werden nur die Operatoren angezeigt, die auf die ausgewählte Option angewendet werden können. Zudem wurden einige Operatoren umbenannt („stimmt überein“ heißt jetzt „gleich“), um die Konsistenz und die Intuitivität zu erhöhen. Alle vorhandenen Ausschlussregeln, die vor dieser Version erstellt worden sind, wurden automatisch in die neue Struktur migriert. Es ist keine Neustrukturierung Ihrerseits nötig.

Sie können so viele Einschlussregeln wie benötigt erstellen. Die Einschlussregeln werden mit einem Operator vom Typ „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.