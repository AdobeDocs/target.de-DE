---
keywords: Targeting;Kollisionen;Konflikte
description: Kollisionen treten auf, wenn mehrere Aktivitäten eingerichtet sind, um Inhalte auf derselben Seite bereitzustellen. Erfahren Sie, wie Sie bei der Verwendung von Adobe Target Kollisionen vermeiden können.
title: Wie kann ich Aktivitäten vermeiden?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 79%

---


# Aktivitätskollisionen

Die Registerkarte [!UICONTROL Kollisionen] auf der Seite [!UICONTROL Übersicht über die Aktivität] unter [!DNL Adobe Target] Listen Kollisionen der Aktivität auf Ihrer Site.

Eine Aktivitätskollision tritt auf, wenn mehrere Aktivitäten eingerichtet sind, die Inhalt für dieselbe Seite bereitstellen sollen. Tritt eine Aktivitätskollision auf, wird möglicherweise nicht der erwartete Inhalt auf Ihrer Seite angezeigt.

Enthält Ihre Aktivität mögliche Kollisionen, wird die Registerkarte [!UICONTROL Kollisionen] auf der Aktivitätsübersichtsseite angezeigt. Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf dieser Registerkarte finden Sie eine Liste der möglicherweise kollidierenden Aktivitäten. Klicken Sie in der Liste auf eine Aktivität, damit eine Übersichtsseite für die Aktivität angezeigt wird. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

Die Liste [!UICONTROL Kollisionen] hilft Ihnen:

* Identifizieren, ob ein Test bereits auf einer Seite ausgeführt wird, bevor Sie eine neue Aktivität einrichten
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

Die Liste [!UICONTROL Kollisionen] zeigt jedes [!DNL Target]-Szenario, in dem die mbox verwendet wird und das dieselbe URL verwendet. Die Liste zeigt für jede mögliche Kollision die Aktivitäts-URL, den Namen der mbox, in der die Kollision auftreten kann, sowie sämtliche Aktivitäten, auf die beide Kriterien zutreffen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt den Status und die Priorität jeder möglichen Kollision sowie weitere Informationen an. Mithilfe des Status und der Priorität können Sie bestimmen, wie wahrscheinlich es ist, dass eine Kollision auftritt. Wenn es beispielsweise eine mögliche Kollision zwischen zwei Aktivitäten gibt, von denen eine inaktiv ist, tritt diese erst auf, wenn die inaktive Aktivität aktiviert wird. Besteht die mögliche Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe, tritt eine Kollision auf. Sie können die Priorität oder den Status ändern, um die Kollision zu verhindern.

Bei unterschiedlichen Zielgruppen besteht weiterhin das Risiko einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
