---
keywords: Targeting; Kollisionen; Konflikte
description: Kollisionen treten auf, wenn mehrere Aktivitäten eingerichtet sind, um Inhalte auf derselben Seite bereitzustellen. Erfahren Sie, wie Sie bei der Verwendung von Adobe Target Konflikte vermeiden können.
title: Wie kann ich Aktivitätskollisionen vermeiden?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
source-git-commit: 430b2ebb053460ec04c01da53aadacaba9e99599
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 72%

---

# Aktivitätskollisionen

Die [!UICONTROL Kollisionen] auf der Registerkarte [!UICONTROL Aktivitätsübersicht] Seite in [!DNL Adobe Target] listet Aktivitätskollisionen auf Ihrer Site auf.

Eine Aktivitätskollision tritt auf, wenn mehrere Aktivitäten eingerichtet sind, die Inhalt für dieselbe Seite bereitstellen sollen. Tritt eine Aktivitätskollision auf, wird möglicherweise nicht der erwartete Inhalt auf Ihrer Seite angezeigt.

Enthält Ihre Aktivität mögliche Kollisionen, wird die Registerkarte [!UICONTROL Kollisionen] auf der Aktivitätsübersichtsseite angezeigt. Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf dieser Registerkarte finden Sie eine Liste der möglicherweise kollidierenden Aktivitäten. Klicken Sie in der Liste auf eine Aktivität, damit eine Übersichtsseite für die Aktivität angezeigt wird. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

Die [!UICONTROL Kollisionen] Die Liste hilft Ihnen bei Folgendem:

* Identifizieren, ob ein Test bereits auf einer Seite ausgeführt wird, bevor Sie eine neue Aktivität einrichten
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

Die [!UICONTROL Kollisionen] Liste zeigt jeden [!DNL Target] Szenario, in dem die Mbox verwendet wird und die dieselbe URL verwendet. Für jede mögliche Kollision zeigt die Liste die Aktivitäts-URL, den Mbox-Namen, in dem die Kollision auftreten könnte, sowie alle Aktivitäten, die beiden Kriterien entsprechen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt den Status und die Priorität jeder möglichen Kollision sowie weitere Informationen an. Mithilfe des Status und der Priorität können Sie bestimmen, wie wahrscheinlich es ist, dass eine Kollision auftritt. Wenn es beispielsweise eine mögliche Kollision zwischen zwei Aktivitäten gibt, von denen eine inaktiv ist, tritt diese erst auf, wenn die inaktive Aktivität aktiviert wird. Besteht die mögliche Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe, tritt eine Kollision auf. Sie können die Priorität oder den Status ändern, um die Kollision zu verhindern.

Bei unterschiedlichen Zielgruppen besteht weiterhin das Risiko einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
