---
keywords: Targeting; Kollisionen; Konflikte
description: Verhindern Sie Konflikte bei der Inhaltsbereitstellung auf derselben Seite, indem Sie Aktivitäten in Adobe Target korrekt konfigurieren.
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

Der Tab [!UICONTROL Collisions] ist auf der Aktivitätsübersichtsseite verfügbar und kann Sie darüber informieren, ob Ihre Aktivität mögliche Kollisionen enthält.

Um auf die Registerkarte [!UICONTROL Collisions] zuzugreifen, klicken Sie auf **[!UICONTROL Activities]** > wählen Sie die gewünschte Aktivität aus der Liste aus und klicken Sie dann in der linken Leiste auf **[!UICONTROL Collisions]** .

Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf dieser Registerkarte finden Sie eine Liste der möglicherweise kollidierenden Aktivitäten. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

Die Liste [!UICONTROL Collisions] hilft Ihnen bei Folgendem:

* Identifizieren, ob ein Test bereits auf einer Seite ausgeführt wird, bevor Sie eine neue Aktivität einrichten
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

Die Liste [!UICONTROL Collisions] zeigt jedes [!DNL Target]-Szenario an, in dem die Mbox verwendet wird und das dieselbe URL verwendet. Für jede mögliche Kollision zeigt die Liste die Aktivitäts-URL, den Mbox-Namen, in dem die Kollision auftreten könnte, sowie alle Aktivitäten, die beiden Kriterien entsprechen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt den Status und die Priorität jeder möglichen Kollision sowie weitere Informationen an. Mithilfe des Status und der Priorität können Sie bestimmen, wie wahrscheinlich es ist, dass eine Kollision auftritt. Betrachten Sie zwei Aktivitäten, die kollidieren könnten. Wenn eine Aktivität derzeit nicht aktiv ist, kann keine Kollision auftreten. Eine Kollision ist nur möglich, wenn die inaktive Aktivität aktiv wird. Wenn die mögliche Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe besteht, tritt eine Kollision auf. Sie können die Priorität oder den Status ändern, um die Kollision zu verhindern.

Bei unterschiedlichen Zielgruppen besteht weiterhin das Risiko einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
