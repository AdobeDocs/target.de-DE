---
keywords: Automatische Zuordnung erstellen;A/B-Test;Aktivität automatisch zuweisen;neue A/B-Aktivität;Automatische Zuordnung;Automatische Zuordnung zu bestem Erlebnis;Zuordnung;Automatische Zuordnung
description: Erfahren Sie, wie Sie mit dem [!UICONTROL Visual Experience Composer] (VEC) in  [!DNL Adobe Target]  eine [!UICONTROL Auto-Allocate] A/B-Test -Aktivität erstellen.
title: Wie erstelle ich eine [!UICONTROL Auto-Allocate] Aktivität?
feature: Auto-Allocate
exl-id: 30bc95e0-4f5e-4d1f-bad2-7b20b8f3c7d2
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 37%

---

# [!UICONTROL Auto-Allocate] erstellen

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um Ihre [!UICONTROL Auto-Allocate] [!UICONTROL A/B Test]-Aktivität direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu ändern.

Zusätzlich zur Aktivität [!UICONTROL Auto-Allocate] [!UICONTROL A/B Test] (die in diesem Artikel behandelt wird) bietet [!DNL Target] zwei zusätzliche Arten von [!UICONTROL A/B Test]: [!UICONTROL Manual (Default)] und [!UICONTROL Auto-Target]. Siehe [Typen von A/B-Testaktivitäten](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B-Test - Übersicht*.

So erstellen Sie eine [!UICONTROL Auto-Allocate]:

1. Klicken Sie in der **[!UICONTROL Activities]** auf **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Dropdownliste „Aktivität erstellen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. [!UICONTROL Recommendations] ist beispielsweise eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium). Informationen zu den verschiedenen Aktivitätstypen finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md) und im [Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md).

1. Wählen Sie im Dialogfeld **[!UICONTROL Create A/B Test Activity]** bei Bedarf **[!UICONTROL Visual]** aus.

   Wenn Sie die [!UICONTROL Form-Based Experience Composer] bevorzugen, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den Single Page Application VEC. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Abhängig von Ihrer Lizenz) Wenn Sie [Target Premium-Kunde ](/help/main/c-intro/intro.md#premium)sind, wählen Sie einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an und klicken Sie dann auf **[!UICONTROL Create]**.

   Wenn Ihr Konto mit einer Standard-URL konfiguriert wurde, dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standardeinstellung zu einer anderen URL wechseln.

   Die [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die in der URL angegebene Seite an.

   ![VEC](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Geben Sie an der verfügbaren Stelle einen Namen für die Aktivität ein.

   ![Namensfeld](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   Der Aktivitätsname darf nicht mit einem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

1. Erstellen Sie alle Erlebnisse, indem Sie die Elemente auf der Seite ändern.

   Im [!UICONTROL Visual Experience Composer] werden nach dem Erstellen einer neuen Aktivität auf der linken Seite zwei Registerkarten angezeigt: Erlebnis A und Erlebnis B. Erlebnis A ist das Kontrollerlebnis. Der Fokus liegt auf der Registerkarte Erlebnis B , die Sie nach Bedarf ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Ändern von Erlebnissen in der [!UICONTROL Visual Experience Composer] finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie oben in der **[!UICONTROL Targeting]** auf [!UICONTROL Visual Experience Composer] , um mit dem nächsten Schritt im Drei-Schritte-Workflow fortzufahren.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität und zum Einrichten der Erlebnisse.

1. Klicken Sie im [!UICONTROL Audience] auf das Bearbeitungssymbol (das vertikale Auslassungszeichen), klicken Sie auf **[!UICONTROL Replace Audience]** und wählen [ die ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für Ihre Aktivität aus.

   Standardmäßig ist die Zielgruppe auf [!UICONTROL All Visitors] festgelegt.

1. Wählen Sie den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   ![Prozentsatz für Zielgruppen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Einrichten der Traffic-Zuordnungsmethode.

   Sie können der gleichen Zielgruppe mehrere Erlebnisse zeigen. Es wird ein Diagramm angezeigt, das Ihre ausgewählte Zielgruppe und die Erlebnisse zeigt, die Sie der Aktivität hinzugefügt haben.

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus. Um eine [!UICONTROL Auto-Allocate] Aktivität zu erstellen, wählen Sie **[!UICONTROL Auto-Allocate to best experience]** aus.

   Nachfolgend werden die drei Arten der Traffic-Zuordnung beschrieben:

   * **[!UICONTROL Manual (Default)]**: Geben Sie den Prozentsatz der Eintritte an, die für jedes Erlebnis angezeigt werden sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen. Weitere Informationen finden Sie unter [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Auto-allocate to best experience]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugewiesen, um die Erlebnisforschung aufrechtzuerhalten und Änderungen an Leistungstrends zu erkennen.

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] nutzt fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Anschließend wird Besuchern auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher das jeweils passendste Erlebnis bereitgestellt. Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Sie können auch auf **[!UICONTROL Add]** klicken, um der Aktivität ein weiteres Erlebnis hinzuzufügen.

1. Wenn Sie mit der Auswahl Ihrer Audience, Erlebnisoptionen und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Next]** , um zum dritten Schritt des Drei-Schritte-Workflows überzugehen.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

   >[!NOTE]
   >
   >Wenn Sie „Analytics [ Target“ (A4T](/help/main/c-integrating-target-with-mac/a4t/a4t.md) mit dieser Aktivität verwenden möchten, lesen Sie die wichtigen Informationen unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klicken Sie auf **[!UICONTROL Save & Close]** oder **[!UICONTROL Save]**.

Nachdem Sie die Aktivität erstellt haben, werden auf der Registerkarte [!UICONTROL Overview] Informationen zur Aktivität angezeigt, einschließlich eines Diagramms Ihrer Aktivität.

## Schulungsvideo: Erstellen von A/B-Tests (8:36)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird.

* Erstellen einer [!UICONTROL A/B Test] Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
