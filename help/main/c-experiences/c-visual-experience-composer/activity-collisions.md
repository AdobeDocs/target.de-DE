---
keywords: Targeting; Kollisionen; Konflikte
description: Kollisionen treten auf, wenn mehrere Aktivitäten eingerichtet sind, um Inhalte auf derselben Seite bereitzustellen. Erfahren Sie, wie Sie bei der Verwendung von Adobe Target Konflikte vermeiden können.
title: Wie kann ich Aktivitätskollisionen vermeiden?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
source-git-commit: b34701113ebdc9f539e5a3d7163aa3dd85368af3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 67%

---

# Aktivitätskollisionen

Auf der Registerkarte [!UICONTROL Collisions] auf der Seite [!UICONTROL Activity Overview] in [!DNL Adobe Target] werden Aktivitätskollisionen auf Ihrer Site aufgelistet.

Eine Aktivitätskollision tritt auf, wenn mehrere Aktivitäten eingerichtet sind, die Inhalt für dieselbe Seite bereitstellen sollen. Tritt eine Aktivitätskollision auf, wird möglicherweise nicht der erwartete Inhalt auf Ihrer Seite angezeigt.

Der Tab [!UICONTROL Collisions] ist auf der Aktivitätsübersichtsseite verfügbar und kann Sie darüber informieren, ob Ihre Aktivität mögliche Kollisionen enthält. Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf dieser Registerkarte finden Sie eine Liste der möglicherweise kollidierenden Aktivitäten. Klicken Sie in der Liste auf eine Aktivität, damit eine Übersichtsseite für die Aktivität angezeigt wird. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

Die Liste [!UICONTROL Collisions] hilft Ihnen bei Folgendem:

* Identifizieren, ob ein Test bereits auf einer Seite ausgeführt wird, bevor Sie eine neue Aktivität einrichten
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

Die Liste [!UICONTROL Collisions] zeigt jedes [!DNL Target]-Szenario an, in dem die Mbox verwendet wird und das dieselbe URL verwendet. Für jede mögliche Kollision zeigt die Liste die Aktivitäts-URL, den Mbox-Namen, in dem die Kollision auftreten könnte, sowie alle Aktivitäten, die beiden Kriterien entsprechen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt den Status und die Priorität jeder möglichen Kollision sowie weitere Informationen an. Mithilfe des Status und der Priorität können Sie bestimmen, wie wahrscheinlich es ist, dass eine Kollision auftritt. Wenn es beispielsweise eine mögliche Kollision zwischen zwei Aktivitäten gibt, von denen eine inaktiv ist, tritt diese erst auf, wenn die inaktive Aktivität aktiviert wird. Besteht die mögliche Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe, tritt eine Kollision auf. Sie können die Priorität oder den Status ändern, um die Kollision zu verhindern.

Bei unterschiedlichen Zielgruppen besteht weiterhin das Risiko einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
