---
keywords: Zielgruppenbestimmung;Kollisionen;Konflikte
description: Vermeiden Sie Konflikte bei der Inhaltsbereitstellung auf derselben Seite, indem Sie die Aktivitäten in Adobe Target korrekt konfigurieren.
title: Wie kann ich Aktivitätskollisionen vermeiden?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
TQID: https://experienceleague.adobe.com/R6cwp4KnoYPO9Wxr47HswtBX6jKPJ0i-UGdtA1ZHawU
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 49%

---

# Aktivitätskollisionen

Auf der Registerkarte [!UICONTROL Kollisionen] auf der Seite [!UICONTROL Aktivitätsübersicht] in [!DNL Adobe Target] werden Aktivitätskollisionen auf Ihrer Site aufgeführt.

Eine Aktivitätskollision tritt auf, wenn mehrere Aktivitäten eingerichtet sind, die Inhalt für dieselbe Seite bereitstellen sollen. Tritt eine Aktivitätskollision auf, wird möglicherweise nicht der erwartete Inhalt auf Ihrer Seite angezeigt.

Die Registerkarte [!UICONTROL Kollisionen] ist auf der Seite Aktivitätsübersicht verfügbar und kann Sie darüber informieren, ob Ihre Aktivität potenzielle Kollisionen enthält.

Um auf die Registerkarte [!UICONTROL Kollisionen] zuzugreifen, klicken Sie auf **[!UICONTROL Aktivitäten]** > in der Liste auf die gewünschte Aktivität und dann in der linken Leiste auf **[!UICONTROL Kollisionen]**.

Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf dieser Registerkarte finden Sie eine Liste der möglicherweise kollidierenden Aktivitäten. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

Die [!UICONTROL Kollisionen] hilft Ihnen bei Folgendem:

* Identifizieren, ob ein Test bereits auf einer Seite ausgeführt wird, bevor Sie eine neue Aktivität einrichten
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

Die [!UICONTROL Kollisionen] Liste zeigt jedes [!DNL Target] Szenario, in dem die Mbox verwendet wird und das dieselbe URL verwendet. Für jede potenzielle Kollision zeigt die Liste die Aktivitäts-URL, den Mbox-Namen, in dem die Kollision auftreten könnte, und alle Aktivitäten, die diesen beiden Kriterien entsprechen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt den Status und die Priorität jeder möglichen Kollision sowie weitere Informationen an. Mithilfe des Status und der Priorität können Sie bestimmen, wie wahrscheinlich es ist, dass eine Kollision auftritt. Erwägen Sie zwei Aktivitäten, die kollidieren könnten. Wenn eine Aktivität derzeit nicht aktiv ist, kann keine Kollision auftreten. Eine Kollision ist nur möglich, wenn die inaktive Aktivität aktiv wird. Wenn es zu einer potenziellen Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe kommt, tritt eine Kollision auf. Sie können die Priorität oder den Status ändern, um die Kollision zu verhindern.

Bei unterschiedlichen Zielgruppen besteht weiterhin das Risiko einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
