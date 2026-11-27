---
keywords: Zielgruppenbestimmung;Kollisionen;Konflikte
description: Vermeiden Sie Konflikte bei der Inhaltsbereitstellung auf derselben Seite, indem Sie die Aktivitäten in Adobe Target korrekt konfigurieren.
title: Wie kann ich Aktivitätskollisionen vermeiden?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
TQID: 'https://experienceleague.adobe.com/R6cwp4KnoYPO9Wxr47HswtBX6jKPJ0i-UGdtA1ZHawU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 18%
---
# Aktivitätskollisionen {#activity-collisions}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Registerkarte **[!UICONTROL Kollisionen]** Aktivitäten finden, die möglicherweise Inhalte für dieselbe Seite bereitstellen.

>[!ENDSHADEBOX]

Eine Aktivitätskollision tritt auf, wenn mehrere Aktivitäten eingerichtet sind, die Inhalt für dieselbe Seite bereitstellen sollen. Wenn eine Aktivitätskollision auftritt, wird der erwartete Inhalt möglicherweise nicht auf der Seite angezeigt.

Auf der Registerkarte **[!UICONTROL Kollisionen]** auf der Seite **[!UICONTROL Aktivitätsübersicht]** in [!DNL Adobe Target] werden die Aktivitätskollisionen auf der Site aufgelistet und angezeigt, ob eine Aktivität potenzielle Kollisionen enthält. Die **[!UICONTROL Kollisionen]** hilft bei Folgendem:

* Ermitteln Sie, ob bereits ein Test auf einer Seite ausgeführt wird, bevor eine neue Aktivität eingerichtet wird.
* Fehlerbehebung bei einer Aktivität, wenn der erwartete Inhalt nicht angezeigt wird

## Zugriff auf die Registerkarte „Kollisionen“ {#access-collisions}

Klicken Sie **[!UICONTROL Aktivitäten]** auf die gewünschte Aktivität in der Liste und dann auf das Menü **[!UICONTROL Kollisionen]**.

![Symbol „Konfigurieren“](assets/collisions_1.png)

Dort werden unabhängig vom Zielgruppen-Targeting in den einzelnen Aktivität alle Aktivitäten auf der gleichen URL aufgelistet. Auf der Registerkarte werden die Aktivitäten aufgelistet, die möglicherweise kollidieren. Führt die Kollision zu einer Änderung des erwarteten Erlebnisses, muss die Aktivität bearbeitet werden.

## Kollisionsliste lesen {#collisions-list}

Die **[!UICONTROL Kollisionen]** Liste zeigt jedes [!DNL Target] Szenario, in dem die Mbox verwendet wird und das dieselbe URL verwendet. Für jede potenzielle Kollision zeigt die Liste die Aktivitäts-URL, den Mbox-Namen, in dem die Kollision auftreten könnte, und alle Aktivitäten, die diesen beiden Kriterien entsprechen. Sind mehrere Mboxes vorhanden, werden sie einzeln aufgelistet.

Die Liste zeigt auch den Status und die Priorität jeder potenziellen Kollision zusammen mit anderen Informationen. Der Status und die Priorität helfen bei der Bestimmung der Wahrscheinlichkeit, dass eine Kollision auftritt. Für zwei Aktivitäten, die kollidieren könnten:

* Wenn eine Aktivität derzeit nicht aktiv ist, kann keine Kollision auftreten. Eine Kollision ist nur möglich, wenn die inaktive Aktivität aktiv wird.
* Wenn es zu einer potenziellen Kollision zwischen zwei Live-Aktivitäten mit derselben Priorität und derselben Zielgruppe kommt, tritt eine Kollision auf. Die Priorität oder der Status kann geändert werden, um die Kollision zu verhindern.
* Wenn die Zielgruppen unterschiedlich sind, besteht weiterhin die Möglichkeit einer Kollision, da ein bestimmter Besucher mehreren Zielgruppen angehören kann.
