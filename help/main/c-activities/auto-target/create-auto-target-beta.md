---
keywords: Erstellen Sie automatisches Targeting; A/B-Test; automatische Targeting-Aktivität; neue A/B-Aktivität; automatisches Targeting; automatisches Targeting für personalisierte Erlebnisse; personalisiert; Optimierung
description: Erfahren Sie, wie Sie mit dem VEC (0) eine A/B-Test-Aktivität vom Typ [!UICONTROL Auto-Target] erstellen.[!UICONTROL Visual Experience Composer]
title: Wie erstelle ich eine [!UICONTROL Auto-Target] -Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Auto-Target
hide: true
hidefromtoc: true
source-git-commit: 5fc18c6d3b493ea0a58048cc20ce3a6c2ffb7d14
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 18%

---

# Erstellen einer [!UICONTROL Auto-Target] -Aktivität

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um Ihre [!UICONTROL Auto-Target] [!UICONTROL A/B Test] -Aktivität direkt auf einer für [!DNL Target] aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu verändern.

>[!NOTE]
>
>[!UICONTROL Auto-Target] ist als Teil der [!DNL Target Premium] -Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).

So erstellen Sie eine [!UICONTROL Auto-Target] -Aktivität:

1. Klicken Sie in der Liste **[!UICONTROL Activities]** auf **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

1. Wählen Sie im Dialogfeld [!UICONTROL Create A/B Test Activity] ggf. **[!UICONTROL Visual]** aus.

   Wenn Sie lieber den [!UICONTROL Form-Based Experience Composer] verwenden möchten, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den VEC [!UICONTROL Single Page Application]. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung für VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie ein [Target Premium-Kunde](/help/main/c-intro/intro.md#premium) sind, wählen Sie aus der Dropdownliste **[!UICONTROL Choose Workspace]** einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

   Die Option [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) ist eine Funktion vom Typ [Target Premium](/help/main/c-intro/intro.md) und wird möglicherweise nicht angezeigt, wenn Ihr Unternehmen über eine [!UICONTROL Target Standard] -Lizenz verfügt.

1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

1. Klicken Sie auf **[!UICONTROL Create]**.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die in der URL angegebene Seite an.

1. Klicken Sie oben im VEC auf **[!UICONTROL Untitled Activity]** und geben Sie dann einen Namen für die Aktivität in der angegebenen Platzierung an.

   Der Aktivitätsname darf mit keinem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

   Der Aktivitätsname darf keine der folgenden Zeichensequenzen enthalten:

   | Zeichensequenz | Beschreibung |
   |--- |--- |
   | ;= | Semikolon, Gleich |
   | ;+ | Semikolon, Plus |
   | ;- | Semikolon, Minus |
   | ;@ | Semikolon, At-Zeichen |
   | ,= | Komma, gleich |
   | ,+ | Komma, Plus |
   | ,- | Komma, Minus |
   | ,@ | Komma, At-Zeichen |
   | `[`&quot; | Offene eckige Klammer, doppelte Anführungszeichen |
   | &quot;`]` | Doppelte Anführungszeichen, eckige Klammer schließen |

1. Erstellen Sie neue Erlebnisse, indem Sie die Elemente auf der Seite ändern.

   Im Tab [!UICONTROL Visual Experience Composer] werden nach der Erstellung einer neuen Aktivität auf der linken Seite zwei Registerkarten angezeigt: Erlebnis A und Erlebnis B. Erlebnis A ist das Kontrollerlebnis. Ihr Fokus liegt auf der Registerkarte Erlebnis B , die Sie nach Bedarf ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen, indem Sie auf das Symbol [!UICONTROL Add] ( ![Symbol Hinzufügen](/help/main/assets/icons/Add.svg) ) oben im Bereich [!UICONTROL Experiences] klicken. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Ändern von Erlebnissen in [!UICONTROL Visual Experience Composer] finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie oben im [!UICONTROL Visual Experience Composer] auf **[!UICONTROL Targeting]** , um im geleiteten Arbeitsablauf mit drei Schritten zum nächsten Schritt zu wechseln.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   Das Flussdiagramm führt Sie durch die Schritte zum Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, zum Auswählen der Traffic-Zuordnungsmethode und zum Angeben der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

1. (Bedingt) Klicken Sie auf das Steuerelement **[!UICONTROL All Visitors]** , um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die Audience [!UICONTROL All Visitors] wird als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Der rechte Rahmen wird angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Besucherprozentsatz für die Aktivität zuweisen können.

   1. Um die Zielgruppe zu ändern, klicken Sie im rechten Rahmen auf das Symbol **[!UICONTROL Replace]** ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ).
   1. Wählen Sie im Dialogfeld [!UICONTROL Add Audience] die gewünschte Zielgruppe aus [ und klicken Sie dann auf **[!UICONTROL Assign Audience]**.](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)

      Sie können auf **Zielgruppen kombinieren** klicken, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

      Wenn Sie eine neue Zielgruppe erstellen müssen, die noch nicht im [!UICONTROL Audience Library] enthalten ist, klicken Sie auf **Zielgruppe erstellen**. Während des [Workflows für die Audience-Erstellung](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen wählen:

      * Erstellen einer On-Demand-Zielgruppe, die im Ordner &quot;[!UICONTROL Audience Library]&quot;gespeichert ist und in anderen Aktivitäten wiederverwendet werden kann
      * Erstellen Sie eine [aktivitätsspezifische Audience](/help/main/c-target/creating-activity-only-audience.md), die nicht im [!UICONTROL Audience Library] gespeichert ist und nur in der aktuellen Aktivität verwendet werden kann.

   1. Klicken Sie im rechten Rahmen auf **[!UICONTROL Visitor Percentage]** und wählen Sie dann den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Klicken Sie auf das Steuerelement **[!UICONTROL Traffic Allocation]** und wählen Sie dann im rechten Bereich die gewünschte Traffic-Zuordnungsmethode aus. Klicken Sie in diesem Szenario auf **[!UICONTROL Auto-Taget for personalized experiences]**.

   ![Einstellungen für die Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

   Die folgenden Traffic-Zuordnungsmethoden sind verfügbar:

   * **[!UICONTROL Manual (Default)]**: Geben Sie den Prozentsatz der Teilnehmer an, der jedes Erlebnis sehen soll. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Auto-Allocate to best experience]**: Die meisten Aktivitätsteilnehmer werden automatisch zu leistungsstärkeren Erlebnissen geleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Auto-Allocate] Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] verwendet das erweiterte maschinelle Lernen, um Inhalte zu personalisieren und Konversionen zu fördern, indem mehrere von Marketingexperten definierte Erlebnisse mit hoher Leistung identifiziert und anschließend basierend auf ihren individuellen Kundenprofilen und früheren Verhaltensweisen ähnlicher Besucher das am besten angepasste Erlebnis für Besucher bereitgestellt wird. Weitere Informationen finden Sie unter [Überblick über das automatische Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Klicken Sie im rechten Bereich auf **[!UICONTROL Experiences]** und geben Sie dann die gewünschte Traffic-Zuordnung für jedes Erlebnis an.

1. Wenn Sie mit der Auswahl Ihrer Zielgruppe, Erlebnisoptionen und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Next]** , um zum dritten Schritt des geleiteten Arbeitsablaufs mit drei Schritten zu wechseln.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

   >[!NOTE]
   >
   >Wenn Sie [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) mit dieser Aktivität verwenden möchten, finden Sie wichtige Informationen unter [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klicken Sie auf **[!UICONTROL Save & Close]** oder **[!UICONTROL Save]**.

Nach Erstellung der Aktivität zeigt der Tab [!UICONTROL Overview] Informationen über die Aktivität an, einschließlich eines Diagramms zu Ihrer Aktivität.