---
keywords: Create auto-allocate;A/B test;auto-allocate activity;new a/b activity;auto allocate;auto-allocate to best experience;allocate
description: Verwenden Sie den Visual Experience Composer in Adobe Target, um Ihre automatisch zugewiesene A/B-Test-Aktivität direkt auf einer Zielgruppe-aktivierten Seite zu erstellen und Teile der Seite innerhalb der Zielgruppe zu ändern.
title: Erstellen einer Aktivität mit automatisierter Zuordnung
feature: ab
topic: Advanced,Standard,Classic
uuid: 2a255cf9-91c7-4710-bfd7-a4d8797ef24c
translation-type: tm+mt
source-git-commit: 85dc58da0425bfbbea2b2892ab617152c0184d0b
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 61%

---


# Erstellen einer Aktivität mit automatisierter Zuordnung

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC), [!DNL Adobe Target] um Ihre [!UICONTROL automatisch zugewiesene] [!UICONTROL A/B-Test] -Aktivität direkt auf einer [!DNL Target]aktivierten Seite zu erstellen und Teile der Seite innerhalb [!DNL Target]zu ändern.

>[!NOTE]
>
>Zusätzlich zur [!UICONTROL Aktivität für die automatisierte Zuordnung] von [!UICONTROL A/B-Tests] (in diesem Artikel besprochen) [!DNL Target] stehen zwei weitere Typen von [!UICONTROL A/B-Test] -Aktivitäten zur Verfügung: [!UICONTROL Manuelle (Standard)] und [!UICONTROL automatische Zielgruppe].
>
>Siehe [Typen von A/B-Testing-Aktivitäten](/help/c-activities/t-test-ab/test-ab.md#types) in der Übersicht über *A/B-Tests*.

So erstellen Sie eine [!UICONTROL Aktivität mit automatisierter Zuordnung] :

1. Klicken Sie in der Liste **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL A/B-Test]**.

   ![Dropdownliste „Aktivität erstellen“](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist [!UICONTROL Recommendations] eine [Target Premium-Funktion](/help/c-intro/intro.md#premium).
   >
   >Informationen zu den verschiedenen Aktivitätstypen finden Sie unter [Aktivitäten](/help/c-activities/activities.md) und im [Target-Aktivitätshandbuch](/help/c-activities/target-activities-guide.md).

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Standard)]** aus.

   ![A/B-Test-Aktivität erstellen](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   If you prefer to use the [!UICONTROL Form-Based Experience Composer], select [!UICONTROL Form]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC- und [!UICONTROL Form-Based Experience Composer]wird der VEC für Einzelseitenanwendungen [!DNL Target] Angebot. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die Option [!UICONTROL „Arbeitsplatz auswählen“](/help/administrating-target/c-user-management/property-channel/property-channel.md) in der obigen Abbildung ist eine Funktion von [Target Premium](/help/c-intro/intro.md). Your organization has a [!UICONTROL Target Standard] license if you do not see this option.

1. (Abhängig von Ihrer Lizenz) Wenn Sie [Target Premium-Kunde ](/help/c-intro/intro.md#premium)sind, wählen Sie einen [Arbeitsbereich](/help/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie Ihre [Aktivitäts-URL](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) ein und klicken Sie dann auf **[!UICONTROL Weiter]**.

   Wenn Ihr Konto mit einer Standard-URL konfiguriert wurde, dann wird diese URL standardmäßig angezeigt. Sie können von der Standard-URL zu einer anderen URL wechseln.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die Seite an, auf die die URL verweist.

   ![VEC](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Geben Sie an der verfügbaren Stelle einen Namen für die Aktivität ein.

   ![Namensfeld](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   Folgende Zeichen sind im Aktivitätsnamen nicht zulässig:

   | Zeichen | Beschreibung |
   |--- |--- |
   | `/` | Vorwärtsschrägstrich |
   | `?` | Fragezeichen |
   | `#` | Raute |
   | `:` | Doppelpunkt |
   | `=` | Gleich |
   | `+` | Plus |
   | `-` | Minus |
   | `@` | At-Zeichen |

1. Erstellen Sie neue Erlebnisse, indem Sie die Elemente auf der Seite ändern.

   Im [!UICONTROL Visual Experience Composer] finden Sie nach der Erstellung einer Aktivität zwei Registerkarten auf der linken Seite: Erlebnis A und Erlebnis B. Erlebnis A ist hierbei das Kontrollerlebnis. Sie werden sich hauptsächlich mit der Registerkarte für Erlebnis B beschäftigen, die Sie nach Wunsch anpassen können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Bearbeiten von Erlebnissen finden Sie im Kapitel [!UICONTROL Visual Experience Composer], Abschnitt  [Erlebnis hinzufügen](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 3.

1. Klicken Sie oben im **[!UICONTROL Visual Experience Composer]** auf [!UICONTROL Targeting], um im geleiteten dreistufigen Workflow zum nächsten Schritt zu springen.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität und zum Einrichten der Erlebnisse.

1. Klicken Sie im Feld [!UICONTROL Audience] auf das Bearbeitungssymbol (drei vertikale Auslassungspunkte), klicken Sie auf Audience **** ersetzen und [wählen Sie dann die Audience](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für Ihre Aktivität aus.

   By default, the audience is set to [!UICONTROL All Visitors].

1. Wählen Sie den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   ![Prozentsatz für Zielgruppen](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Richten Sie die Traffic-Zuordnung ein.

   Sie können der gleichen Zielgruppe mehrere Erlebnisse zeigen. Es wird ein Diagramm mit der ausgewählten Zielgruppe und den Erlebnissen, die Sie zur Aktivität hinzugefügt haben, angezeigt.

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus. Um eine [!UICONTROL Aktivität für die automatische Zuordnung] zu erstellen, wählen Sie &quot; **[!UICONTROL Automatisierte Zuordnung zu bestem Erlebnis]**&quot;aus.

   Die drei Arten der Traffic-Zuordnung werden nachfolgend beschrieben:

   * **[!UICONTROL Manuell (Standard)]**: Geben Sie den Prozentsatz der Teilnehmer an, der jedes Erlebnis sehen kann. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen. For more information, see [Create an A/B Test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Automatisch dem besten Erlebnis zuordnen]**: Die meisten Aktivitätsteilnehmer werden automatisch zu leistungsstärkeren Erlebnissen weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen.

   * **[!UICONTROL Automatische Zielgruppe für personalisierte Erlebnisse]**: [!DNL Target] verwendet fortschrittliches maschinelles Lernen, um Inhalte zu personalisieren und Konversionen zu fördern, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden, und dann den Besuchern das maßgeschneiderte Erlebnis zu bieten, das auf ihren individuellen Profilen und früheren Verhaltensweisen ähnlicher Besucher basiert. For more information, see [Auto-Target](/help/c-activities/auto-target-to-optimize.md).
   You can also click **[!UICONTROL Add]** to add another experience to the activity.

1. When you are satisfied with your audience, experience choices, and traffic allocation choices, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

1. Legen Sie [Ziele und Einstellungen](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

   ![A/B-Aktivitätseinstellungen](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]** oder **[!UICONTROL Speichern]**.

After you create the activity, the [!UICONTROL Overview] tab shows information about the activity, including a diagram of your activity.

## Training video: Creating A/B Tests (8:36) ![Tutorial badge](/help/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird.

* Erstellen Sie eine [!UICONTROL A/B-Test] -Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)