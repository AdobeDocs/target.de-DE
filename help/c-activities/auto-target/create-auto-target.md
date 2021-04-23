---
keywords: Automatische Zielgruppe erstellen;A/B-Test;Aktivität der automatischen Zielgruppe;neue A/B-Aktivität;automatische Zielgruppe;automatische Zielgruppe für personalisierte Erlebnisse;Personalisiert;Optimierung
description: Erfahren Sie, wie Sie den Visual Experience Composer (VEC) in Adobe [!DNL Target] verwenden, um Ihre A/B-Test-Aktivität für die automatische Zielgruppe direkt auf einer  [!DNL Target]-aktivierten Seite zu erstellen.
title: Wie erstelle ich eine Aktivität für die automatische Zielgruppe?
feature: Automatisches Targeting
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 49%

---

# ![PREMIUMCreate ](/help/assets/premium.png) a Auto-Zielgruppe Aktivität

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um Ihre [!UICONTROL Auto-Zielgruppe] [!UICONTROL A/B-Test]-Aktivität direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu ändern.

>[!NOTE]
>
>[!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/c-intro/intro.md).
>
>Zusätzlich zur Aktivität [!UICONTROL Automatische Zielgruppe] [!UICONTROL A/B-Test] (in diesem Artikel besprochen) stellt [!DNL Target] zwei weitere Typen von [!UICONTROL A/B-Test]-Aktivitäten bereit: [!UICONTROL Manuell (Standard)] und [!UICONTROL Automatische Zuordnung].
>
>Siehe [Typen von A/B-Testing-Aktivitäten](/help/c-activities/t-test-ab/test-ab.md#types) in *A/B-Testübersicht*.

So erstellen Sie eine [!UICONTROL Auto-Zielgruppe]-Aktivität:

1. Klicken Sie in der Liste **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL A/B-Test]**.

   ![Dropdownliste „Aktivität erstellen“](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise sind [!UICONTROL Auto-Zielgruppe] und [!UICONTROL Recommendations] [Zielgruppe Premium-Funktionen](/help/c-intro/intro.md#premium).
   >
   >Informationen zu den verschiedenen Aktivitätstypen finden Sie unter [Aktivitäten](/help/c-activities/activities.md) und im [Target-Aktivitätshandbuch](/help/c-activities/target-activities-guide.md).

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Standard)]** aus.

   ![A/B-Test-Aktivität erstellen](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   Wenn Sie den [!UICONTROL Form-Based Experience Composer] verwenden möchten, wählen Sie [!UICONTROL Formular]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zu VEC und [!UICONTROL Form-Based Experience Composer] wird [!DNL Target] in der Einzelseitenanwendung VEC Angebot. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die Option [[!UICONTROL „Arbeitsplatz auswählen“]](/help/administrating-target/c-user-management/property-channel/property-channel.md) in der obigen Abbildung ist eine Funktion von [Target Premium](/help/c-intro/intro.md). Ihre Organisation verfügt über eine Lizenz für [!UICONTROL Target Standard], wenn diese Option nicht angezeigt wird.

1. Wählen Sie eine [Arbeitsfläche](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geben Sie Ihre [Aktivitäts-URL](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) ein und klicken Sie dann auf **[!UICONTROL Weiter]**.

   Wenn Ihr Konto mit einer Standard-URL konfiguriert wurde, dann wird diese URL standardmäßig angezeigt. Sie können von der Standard-URL zu einer anderen URL wechseln.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die Seite an, auf die die URL verweist.

   ![VEC](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Geben Sie an der verfügbaren Stelle einen Namen für die Aktivität ein.

   ![Namensfeld](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   Der Name der Aktivität darf nicht mit einem der folgenden Zeichen beginnen:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

1. Erstellen Sie Erlebnisse, indem Sie die Elemente auf der Seite ändern.

   Der [!UICONTROL Visual Experience Composer] zeigt zwei Registerkarten auf der linken Seite an, nachdem Sie eine Aktivität erstellt haben: Erlebnis A und Erlebnis B. Erlebnis A ist das Kontrollerlebnis. Ihr Fokus liegt auf der Registerkarte Erlebnis B, die Sie nach Wunsch ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Bearbeiten von Erlebnissen finden Sie im Kapitel [!UICONTROL Visual Experience Composer], Abschnitt  [Erlebnis hinzufügen](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 3.

1. Klicken Sie oben im **[!UICONTROL Visual Experience Composer]** auf [!UICONTROL Targeting], um im geleiteten dreistufigen Workflow zum nächsten Schritt zu springen.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität und zum Einrichten der Erlebnisse.

1. Klicken Sie im Feld [!UICONTROL Audience] auf das Bearbeitungssymbol (drei vertikale Auslassungspunkte), klicken Sie auf **[!UICONTROL Audience ersetzen]** und [wählen Sie die Audience](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für Ihre Aktivität aus.

   Standardmäßig ist die Audience auf [!UICONTROL Alle Besucher] eingestellt.

1. Wählen Sie den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   ![Prozentsatz für Zielgruppen](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Richten Sie die Traffic-Zuordnung ein.

   Sie können der gleichen Zielgruppe mehrere Erlebnisse zeigen. Es wird ein Diagramm mit der ausgewählten Zielgruppe und den Erlebnissen, die Sie zur Aktivität hinzugefügt haben, angezeigt.

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus. Um eine Aktivität [!UICONTROL Auto-Zielgruppe] zu erstellen, wählen Sie **[!UICONTROL Automatische Zielgruppe für personalisierte Erlebnisse]**.

   Die drei Arten der Traffic-Zuordnung werden nachfolgend beschrieben:

   * **[!UICONTROL Manuell (Standard)]**: Geben Sie den Prozentsatz der Teilnehmer an, der jedes Erlebnis sehen kann. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen. Weitere Informationen finden Sie unter [A/B-Test erstellen](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Automatische Zuordnung zum besten Erlebnis]**: Die meisten Teilnehmer der Aktivität werden automatisch zu leistungsstärkeren Erlebnissen weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [Übersicht über die automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL Automatische Zielgruppe für personalisierte Erlebnisse]**:  [!DNL Target] verwendet fortschrittliches maschinelles Lernen, um Inhalte zu personalisieren und Konversionen zu fördern, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden, und dann den Besuchern das maßgeschneiderte Erlebnis zu bieten, das auf ihren individuellen Profilen und früheren Verhaltensweisen ähnlicher Besucher basiert.
   Sie können auch auf **[!UICONTROL Hinzufügen]** klicken, um der Aktivität ein weiteres Erlebnis hinzuzufügen.

1. Wenn Sie mit Ihrer Audience, Ihren Erlebnisoptionen und den Optionen für die Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Weiter]**, um zum dritten Schritt des geleiteten Arbeitsablaufs zu wechseln.

1. Legen Sie [Ziele und Einstellungen](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

   ![A/B-Aktivitätseinstellungen](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

   >[!NOTE]
   >
   >Wenn Sie [Analytics für die Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) mit dieser Aktivität verwenden möchten, finden Sie wichtige Informationen unter [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischer Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klicken Sie auf **[!UICONTROL Speichern und Schließen]** oder **[!UICONTROL Speichern]**.

Nachdem Sie die Aktivität erstellt haben, werden auf der Registerkarte [!UICONTROL Übersicht] Informationen zur Aktivität einschließlich eines Diagramms Ihrer Aktivität angezeigt.

## Schulungsvideo: Erstellen von A/B-Tests (8:36) ![Tutorialzeichen](/help/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird.

* Erstellen einer [!UICONTROL A/B-Aktivität ] in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
