---
keywords: Zielgruppenbestimmung;Kollisionen;Konflikte
description: Vermeiden Sie Konflikte bei der Inhaltsbereitstellung auf derselben Seite, indem Sie die Aktivitäten in Adobe Target korrekt konfigurieren.
title: Wie kann ich Aktivitätskollisionen vermeiden?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
source-git-commit: 5c963e97dae11326396a5c1c5e32d19f4d463c74
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 50%

---

# Aktivitätskollisionen

Auf der Registerkarte [!UICONTROL Collisions] auf der Seite [!UICONTROL Activity Overview] in [!DNL Adobe Target] werden Aktivitätskollisionen auf Ihrer Site aufgelistet.

Eine Aktivitätskollision tritt auf, wenn mehrere Aktivitäten eingerichtet sind, die Inhalt für dieselbe Seite bereitstellen sollen. Tritt eine Aktivitätskollision auf, wird möglicherweise nicht der erwartete Inhalt auf Ihrer Seite angezeigt.

Die Registerkarte [!UICONTROL Collisions] befindet sich auf der Seite Aktivitätsübersicht und informiert Sie, wenn Ihre Aktivität potenzielle Kollisionen aufweist.

Um auf die Registerkarte [!UICONTROL Collisions] zuzugreifen, klicken Sie auf **[!UICONTROL Activities]** > in der Liste auf die gewünschte Aktivität und dann in der linken Leiste auf **[!UICONTROL Collisions]** .

Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf dieser Registerkarte finden Sie eine Liste der möglicherweise kollidierenden Aktivitäten. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

Die [!UICONTROL Collisions] Liste hilft Ihnen bei Folgendem:

* Identifizieren, ob ein Test bereits auf einer Seite ausgeführt wird, bevor Sie eine neue Aktivität einrichten
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

Die [!UICONTROL Collisions] Liste zeigt alle [!DNL Target] Szenarien an, in denen die Mbox verwendet wird und die dieselbe URL verwenden. Für jede potenzielle Kollision zeigt die Liste die Aktivitäts-URL, den Mbox-Namen, in dem die Kollision auftreten könnte, und alle Aktivitäten, die diesen beiden Kriterien entsprechen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt den Status und die Priorität jeder möglichen Kollision sowie weitere Informationen an. Mithilfe des Status und der Priorität können Sie bestimmen, wie wahrscheinlich es ist, dass eine Kollision auftritt. Erwägen Sie zwei Aktivitäten, die kollidieren könnten. Wenn eine Aktivität derzeit nicht aktiv ist, kann keine Kollision auftreten. Eine Kollision ist nur möglich, wenn die inaktive Aktivität aktiv wird. Wenn es zu einer potenziellen Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe kommt, tritt eine Kollision auf. Sie können die Priorität oder den Status ändern, um die Kollision zu verhindern.

Bei unterschiedlichen Zielgruppen besteht weiterhin das Risiko einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
