---
keywords: A/B erstellen;A/B-Test;A/B-Aktivität;neue A/B-Aktivität;A/B erstellen
description: Erfahren Sie, wie Sie mit Visual Experience Composer (VEC) in Adobe [!DNL Target]  Ihre A/B-Testaktivität direkt auf einer  [!DNL Target] Seite erstellen.
title: Wie erstelle ich einen A/B-Test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 35%

---

# Erstellen eines A/B-Tests

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um Ihre [!UICONTROL A/B Test] Aktivität direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu ändern.

>[!NOTE]
>
>Zusätzlich zur manuellen [!UICONTROL A/B Test] (Standard) (siehe diesen Artikel) bietet [!DNL Target] zwei weitere Arten von [!UICONTROL A/B Test]: [!UICONTROL Auto-Allocate] und [!UICONTROL Auto-Target].
>
>Siehe [Typen von A/B-Testaktivitäten](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B-Test - Übersicht*.

So erstellen Sie eine manuelle [!UICONTROL A/B Test]:

1. Klicken Sie in der **[!UICONTROL Activities]** auf **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Dropdownliste „Aktivität erstellen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. [!UICONTROL Recommendations] ist beispielsweise eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium).
   >
   >Informationen zu den verschiedenen Aktivitätstypen finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) und im [Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md).

1. Wählen Sie bei Bedarf im Dialogfeld A/B-Test-Aktivität erstellen die Option **[!UICONTROL Visual (Default)]** .

   Wenn Sie die [!UICONTROL Form-Based Experience Composer] bevorzugen, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den Single Page Application VEC. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [Target Premium-Kunde sind](/help/main/c-intro/intro.md#premium) wählen Sie aus der Dropdown-Liste &quot;**[!UICONTROL Choose Workspace]**&quot; einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Die [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) Option in der vorherigen Abbildung ist eine [Target Premium](/help/main/c-intro/intro.md)-Funktion und wird möglicherweise nicht angezeigt, wenn Ihr Unternehmen über eine [!UICONTROL Target Standard]-Lizenz verfügt.

1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an und klicken Sie dann auf **[!UICONTROL Create]**.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standardeinstellung zu einer anderen URL wechseln.

   Die [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die in der URL angegebene Seite an.

1. Klicken Sie oben in VEC auf **[!UICONTROL Untitled Activity]** und geben Sie dann einen Namen für die Aktivität in den entsprechenden Bereich ein.

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

   Im [!UICONTROL Visual Experience Composer] werden nach dem Erstellen einer neuen Aktivität auf der linken Seite zwei Registerkarten angezeigt: Erlebnis A und Erlebnis B. Erlebnis A ist das Kontrollerlebnis. Der Fokus liegt auf der Registerkarte Erlebnis B , die Sie nach Bedarf ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Ändern von Erlebnissen in der [!UICONTROL Visual Experience Composer] finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie oben in der **[!UICONTROL Targeting]** auf [!UICONTROL Visual Experience Composer] , um mit dem nächsten Schritt im Drei-Schritte-Workflow fortzufahren.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität und zum Einrichten der Erlebnisse.

1. Klicken Sie im **[!UICONTROL Audience]** auf das Bearbeitungssymbol (das vertikale Auslassungszeichen), klicken Sie auf **[!UICONTROL Replace Audience]** und wählen [&#x200B; die &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für Ihre Aktivität aus.

   Standardmäßig ist die Zielgruppe auf [!UICONTROL All Visitors] festgelegt.

1. Wählen Sie den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   ![Prozentsatz für Zielgruppen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Richten Sie die Traffic-Zuordnung ein.

   Sie können der gleichen Zielgruppe mehrere Erlebnisse zeigen. Es wird ein Diagramm angezeigt, das Ihre ausgewählte Zielgruppe und die Erlebnisse zeigt, die Sie der Aktivität hinzugefügt haben.

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus:

   * **[!UICONTROL Manual (Default)]**: Geben Sie den Prozentsatz der Eintritte an, die für jedes Erlebnis angezeigt werden sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Auto-allocate to best experience]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Auto-Allocate] - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] nutzt fortschrittliche Machine Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden. Anschließend wird Besuchern auf der Grundlage ihrer individuellen Kundenprofile und des bisherigen Verhaltens ähnlicher Besucher das jeweils passendste Erlebnis bereitgestellt. Weitere Informationen finden Sie unter [Automatisches Targeting - Übersicht](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Sie können auch auf **[!UICONTROL Add]** klicken, um der Aktivität ein weiteres Erlebnis hinzuzufügen.

1. Wenn Sie mit der Auswahl Ihrer Audience, Erlebnisoptionen und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Next]** , um zum dritten Schritt des Drei-Schritte-Workflows überzugehen.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

1. Klicken Sie auf **[!UICONTROL Save & Close]** oder **[!UICONTROL Save]**.

Nachdem Sie die Aktivität erstellt haben, werden auf der Registerkarte [!UICONTROL Overview] Informationen zur Aktivität angezeigt, einschließlich eines Diagramms Ihrer Aktivität.

## Schulungsvideo: Erstellen von A/B-Tests (:36) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird.

* Erstellen einer [!UICONTROL A/B Test] Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/30169?captions=ger)
