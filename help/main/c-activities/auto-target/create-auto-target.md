---
keywords: Automatisches Targeting erstellen;A/B-Test;automatische Targeting-Aktivität;neue A/B-Aktivität;automatisches Targeting;automatisches Targeting für personalisierte Erlebnisse;personalisierte Optimierung
description: Erfahren Sie, wie Sie mit dem [!UICONTROL Visual Experience Composer] (VEC) eine [!UICONTROL Auto-Target] A/B-Test -Aktivität erstellen.
title: Wie erstelle ich eine [!UICONTROL Auto-Target] Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 19%

---

# [!UICONTROL Auto-Target] erstellen

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um Ihre [!UICONTROL Auto-Target] [!UICONTROL A/B Test]-Aktivität direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu ändern.

>[!NOTE]
>
>[!UICONTROL Auto-Target] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).

So erstellen Sie eine [!UICONTROL Auto-Target]:

1. Klicken Sie in der **[!UICONTROL Activities]** auf **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

1. Wählen Sie im Dialogfeld [!UICONTROL Create A/B Test Activity] bei Bedarf **[!UICONTROL Visual]** aus.

   Wenn Sie die [!UICONTROL Form-Based Experience Composer] bevorzugen, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den [!UICONTROL Single Page Application] VEC an. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [Target Premium-Kunde sind](/help/main/c-intro/intro.md#premium) wählen Sie aus der Dropdown-Liste &quot;**[!UICONTROL Choose Workspace]**&quot; einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Die [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) ist eine [Target Premium](/help/main/c-intro/intro.md)-Funktion und wird möglicherweise nicht angezeigt, wenn Ihr Unternehmen über eine [!UICONTROL Target Standard]-Lizenz verfügt.

1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standardeinstellung zu einer anderen URL wechseln.

1. Klicken Sie auf **[!UICONTROL Create]**.

   Die [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die in der URL angegebene Seite an.

1. Klicken Sie auf das **[!UICONTROL Rename]** ( ![Umbenennungssymbol](/help/main/assets/icons/MoreSmallListVert.svg) ), klicken Sie auf **[!UICONTROL Rename]**, geben Sie einen Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Save]**.

   Der Aktivitätsname darf nicht mit einem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichenfolgen enthalten:

   | Zeichenfolge | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, at-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, at-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. Erstellen Sie neue Erlebnisse, indem Sie die Elemente auf der Seite ändern.

   Im [!UICONTROL Visual Experience Composer] werden nach dem Erstellen einer neuen Aktivität auf der linken Seite zwei Registerkarten angezeigt: [!UICONTROL Experience A] und [!UICONTROL Experience B]. [!UICONTROL Experience A] ist das Kontrollerlebnis. Der Fokus liegt auf der Registerkarte [!UICONTROL Experience B] , die Sie nach Bedarf ändern können. [!UICONTROL Experience B] ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen, indem Sie auf das [!UICONTROL Add] ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ) oben im [!UICONTROL Experiences] klicken. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Ändern von Erlebnissen in der [!UICONTROL Visual Experience Composer] finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie oben in der [!UICONTROL Visual Experience Composer] auf **[!UICONTROL Targeting]** , um mit dem nächsten Schritt im Drei-Schritte-Workflow fortzufahren.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   Das Flussdiagramm führt Sie durch die Schritte Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, Auswählen der Traffic-Zuordnungsmethode und Festlegen der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

1. (Bedingt) Klicken Sie auf das **[!UICONTROL All Visitors]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die [!UICONTROL All Visitors] Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

   1. Um die Audience zu ändern, klicken Sie auf das **[!UICONTROL Replace]-** ( ![Replace icon](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.
   1. Wählen Sie im Dialogfeld [!UICONTROL Add Audience] die [ Audience aus ](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Assign Audience]**.

      Sie können auf **Kombinieren von Zielgruppen** klicken, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

      Wenn Sie eine neue Zielgruppe erstellen müssen, die sich noch nicht in der [!UICONTROL Audience Library] befindet, klicken Sie auf **Zielgruppe erstellen**. Während des [Zielgruppen-Workflows erstellen](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

      * **[!UICONTROL Audience Library]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der [!UICONTROL Audience Library] gespeichert wird und in anderen Aktivitäten wiederverwendet werden kann
      * **[!UICONTROL This activity only]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht im [!UICONTROL Audience Library] gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann

   1. Klicken Sie im rechten Rahmen auf **[!UICONTROL Visitor Percentage]** und wählen Sie dann den Prozentsatz der qualifizierten Besucher aus, die Sie in die Aktivität eingeben möchten.

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Klicken Sie auf das **[!UICONTROL Traffic Allocation]** und wählen Sie dann im rechten Bereich die gewünschte Traffic-Zuordnungsmethode aus. Klicken Sie in diesem Szenario auf **[!UICONTROL Auto-Taget for personalized experiences]**.

   ![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/assets/auto-target.png)

   Die folgenden Traffic-Zuordnungsmethoden sind verfügbar:

   * **[!UICONTROL Manual (Default)]**: Geben Sie den Prozentsatz der Eintritte an, die für jedes Erlebnis angezeigt werden sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Auto-Allocate to best experience]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Auto-Allocate] - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] nutzt fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Anschließend wird Besuchern auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher das jeweils passendste Erlebnis bereitgestellt. Weitere Informationen finden Sie unter [Automatisches Targeting - Übersicht](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Klicken Sie im rechten Bereich auf **[!UICONTROL Experiences]** und geben Sie dann für jedes Erlebnis die gewünschte Traffic-Zuordnung an.

1. Wenn Sie mit der Auswahl Ihrer Audience, Erlebnisoptionen und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Next]** , um zum dritten Schritt des Drei-Schritte-Workflows überzugehen.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

   >[!NOTE]
   >
   >Wenn Sie „Analytics [ Target“ (A4T](/help/main/c-integrating-target-with-mac/a4t/a4t.md) mit dieser Aktivität verwenden möchten, lesen Sie die wichtigen Informationen unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klicken Sie auf **[!UICONTROL Save & Close]** oder **[!UICONTROL Save]**.

Nachdem Sie die Aktivität erstellt haben, werden auf der Registerkarte [!UICONTROL Overview] Informationen zur Aktivität angezeigt, einschließlich eines Diagramms Ihrer Aktivität.
