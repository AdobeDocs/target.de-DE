---
keywords: mehrere Zielgruppen;Erlebnisversionen;Erlebnisversionen auswählen
description: Erfahren Sie, wie Sie in A/B-Aktivitäten verschiedene Zielgruppensegmente mit Versionen desselben Erlebnisses ansprechen können.
title: Kann ich in einer A/B-Aktivität mehrere Erlebnisversionen verwenden?
feature: A/B Tests
exl-id: 7afe36f0-ec46-4d63-bfff-45d2c8923a04
TQID: 'https://experienceleague.adobe.com/FleyH-u5cWI5vku9E4-RMWeIc95WgPy-VQ-eytxka18'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 8%
---
# Verschiedene Erlebniszielgruppen in A/B-Tests {#multiple-experience-audiences}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie in einer A/B-Aktivität verschiedene Zielgruppen mit Versionen desselben Erlebnisses ansprechen. Illustriert durch ein Anwendungsbeispiel mit den zu befolgenden Schritten und Best Practices.

>[!ENDSHADEBOX]

In [!DNL Adobe Target] A/B-Aktivitäten können Sie Versionen desselben Erlebnisses an verschiedene Zielgruppen senden. Im **[!UICONTROL Visual Experience Composer“ (VEC) oder im formularbasierten Experience Composer]** Sie mehrere Zielgruppen für ein Erlebnis einrichten.

Daten werden für das Erlebnis unabhängig von der Version erfasst, sodass der Bericht die Leistung des Erlebnisses anzeigt und nicht die jeder Version. Besuchende können auch zwischen Erlebnis-Audiences wechseln, wenn sich ihr Profil ändert. Sie bleiben während der Lebensdauer der Aktivität nicht im selben Erlebnis hängen.

## Anwendungsfall {#use-case}

Sie testen zwei Erlebnisse:

* Ein Geo-Targeting-Banner

* Ein generisches Banner.

Das Banner für jede Geografie muss unterschiedlich sein. Ziel des Tests ist es jedoch festzustellen, ob das Geotargeting besser funktioniert als generische Inhalte.

Wenn Sie für jeden Standort ein eigenes Erlebnis einrichten, messen Sie, wie sich jede Geografie im Vergleich zu den anderen entwickelt. Es wird nicht gemessen, ob Geotargeting im Vergleich zum generischen Banner zum Erreichen Ihrer Erfolgsziele beiträgt.

In diesem Fall benötigen Sie geospezifische Versionen des Erlebnisses, damit Sie das Erlebnis mit einem nicht geozielten Steuerelement testen können.

So richten Sie die geospezifischen Versionen ein:

1. [Erstellen Sie wie gewohnt eine A/B-Aktivität.](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)

   Wenn Sie das Erlebnis mit mehreren Versionen konfigurieren, wählen Sie die Zielgruppe für jede Version aus, wie in den folgenden Schritten beschrieben.

1. Wählen Sie das Erlebnis aus und klicken Sie dann auf **[!UICONTROL Konfigurieren]** > **[!UICONTROL Mehrere Zielgruppen]**.

1. Klicken Sie im **[!UICONTROL Erlebniszielgruppen]** auf das Symbol **[!UICONTROL Zielgruppe hinzufügen]** ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ) und wählen Sie dann die erste Zielgruppe aus, die Sie ansprechen möchten. Wiederholen Sie den Vorgang für alle weiteren Zielgruppen.

   Wenn die Zielgruppe noch nicht vorhanden ist, [ Sie „Zielgruppe erstellen](/help/main/c-target/c-audiences/create-audience.md) und richten Sie sie ein.

1. Fahren Sie mit der Einrichtung der Aktivität fort.

## Best Practices {#best-practices}

* Wählen Sie sich gegenseitig ausschließende Zielgruppen. Wenn sich ein Besucher für mehr als eine Zielgruppe qualifiziert, wird der Inhalt für alle diese Zielgruppen zurückgegeben und der Inhalt der zuletzt aufgeführten Zielgruppe wird auf der Seite angezeigt. Dies gilt für Aktivitäten, die in Visual Experience Composer erstellt wurden.
* Zielgruppen für den Aktivitätseintrag, die im Diagramm definiert sind, werden mithilfe einer AND-Bedingung mit den Erlebnis-Zielgruppen kombiniert. Um in die Aktivität einzutreten, muss sich ein Besucher für die Aktivitäts-Audience und für eine der Erlebnis-Audiences qualifizieren.
* Fügen Sie die gleichen Zielgruppen als Berichtsegmente hinzu. Dies hilft Ihnen, die Testergebnisse auf der hohen Ebene von Erlebnis A im Vergleich zu B und auf der niedrigeren Ebene von Erlebnis A im Vergleich zu B nur für „Browser lang_JP“ anzuzeigen. Dies funktioniert nur bei [!DNL Target] Berichten, nicht bei [!DNL Analytics].
