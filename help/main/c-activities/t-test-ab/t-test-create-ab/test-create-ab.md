---
keywords: A/B erstellen; A/B-Test; A/B-Aktivität; neue A/B-Aktivität; a/b-Aktivität erstellen
description: Erfahren Sie, wie Sie den Visual Experience Composer (VEC) in Adobe verwenden [!DNL Target] zur Erstellung Ihrer A/B-Test-Aktivität direkt in einer [!DNL Target]-aktivierte Seite.
title: Wie erstelle ich einen A/B-Test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: ec1041fd1823d1ab7f1af147af5825c3ae8662b5
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 44%

---

# Erstellen eines A/B-Tests

Verwenden Sie die [!UICONTROL Visual Experience Composer] (VEC) [!DNL Adobe Target] , um [!UICONTROL A/B-Test] direkt in einer Aktivität [!DNL Target]-aktivierte Seite verwenden und Teile der Seite in [!DNL Target].

>[!NOTE]
>
>Zusätzlich zum Handbuch (Standard) [!UICONTROL A/B-Test] Aktivität (in diesem Artikel besprochen), [!DNL Target] bietet zwei weitere Typen von [!UICONTROL A/B-Test] Aktivitäten: [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting].
>
>Siehe [Typen von A/B-Test-Aktivitäten](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B-Test - Überblick*.

So erstellen Sie ein Handbuch [!UICONTROL A/B-Test] Aktivität:

1. Klicken Sie in der Liste **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL A/B-Test]**.

   ![Dropdownliste „Aktivität erstellen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist [!UICONTROL Recommendations] eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium).
   >
   >Informationen zu den verschiedenen Aktivitätstypen finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) und im [Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md).

1. Wählen Sie im Dialogfeld A/B-Test-Aktivität erstellen die Option **[!UICONTROL Visuell (Standard)]**, falls erforderlich.

   Wenn Sie die [!UICONTROL Form-Based Experience Composer]auswählen [!UICONTROL Formular]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer], [!DNL Target] bietet den VEC für Einzelseiten-Apps an. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [Target Premium-Kunde](/help/main/c-intro/intro.md#premium), aus dem **[!UICONTROL Arbeitsbereich auswählen]** Dropdownliste, wählen Sie eine [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Die [[!UICONTROL Arbeitsplatz auswählen]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) -Option in der obigen Abbildung ist eine [Target Premium](/help/main/c-intro/intro.md) und wird möglicherweise nicht angezeigt, wenn Ihr Unternehmen über eine [!UICONTROL Target Standard] -Lizenz.

1. Im **[!UICONTROL Aktivitäts-URL eingeben]** und geben Sie Ihre [Aktivitäts URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md)Klicken Sie auf **[!UICONTROL Erstellen]**.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standard-URL zu einer anderen URL wechseln.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die Seite an, auf die die URL verweist.

1. Klicks **[!UICONTROL Unbenannte Aktivität]** am Anfang des VEC und geben Sie dann einen Namen für die Aktivität in der vorgesehenen Platzierung an.

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

   Im [!UICONTROL Visual Experience Composer] finden Sie nach der Erstellung einer Aktivität zwei Registerkarten auf der linken Seite: Erlebnis A und Erlebnis B. Erlebnis A ist hierbei das Kontrollerlebnis. Ihr Fokus liegt auf der Registerkarte Erlebnis B , die Sie nach Bedarf ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Bearbeiten von Erlebnissen finden Sie im Kapitel [!UICONTROL Visual Experience Composer], Abschnitt  [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie oben im **[!UICONTROL Visual Experience Composer]** auf [!UICONTROL Targeting], um im geleiteten dreistufigen Workflow zum nächsten Schritt zu springen.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität und zum Einrichten der Erlebnisse.

1. Im **[!UICONTROL Zielgruppe]** Klicken Sie auf das Bearbeitungssymbol (die vertikale Ellipse) und klicken Sie auf **[!UICONTROL Zielgruppe ersetzen]**, dann [Zielgruppe auswählen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für Ihre Aktivität.

   Standardmäßig ist die Audience auf [!UICONTROL Alle Besucher].

1. Wählen Sie den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   ![Prozentsatz für Zielgruppen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Richten Sie die Traffic-Zuordnung ein.

   Sie können der gleichen Zielgruppe mehrere Erlebnisse zeigen. Es wird ein Diagramm mit der ausgewählten Zielgruppe und den Erlebnissen angezeigt, die Sie der Aktivität hinzugefügt haben.

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus:

   * **[!UICONTROL Manuell (Standard)]**: Geben Sie den Prozentsatz der Teilnehmer an, der jedes Erlebnis sehen soll. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Automatisch dem besten Erlebnis zuordnen]**: Die meisten Aktivitätsteilnehmer werden automatisch zu leistungsstärkeren Erlebnissen weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Automatische Zuordnung] Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]**: [!DNL Target] verwendet fortschrittliches maschinelles Lernen, um Inhalte zu personalisieren und Konversionen zu fördern, indem mehrere von Marketingexperten definierte Erlebnisse mit hoher Leistung identifiziert und anschließend basierend auf ihren individuellen Kundenprofilen und früheren Verhaltensweisen ähnlicher Besucher das optimal auf sie zugeschnittene Erlebnis bereitgestellt wird. Weitere Informationen finden Sie unter [Überblick über Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Sie können auch auf **[!UICONTROL Hinzufügen]** , um der Aktivität ein weiteres Erlebnis hinzuzufügen.

1. Wenn Sie mit der Auswahl Ihrer Zielgruppen, Erlebnisse und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Nächste]** , um zum dritten Schritt des geleiteten Arbeitsablaufs mit drei Schritten zu gelangen.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

1. Klicks **[!UICONTROL Speichern und schließen]** oder **[!UICONTROL Speichern]**.

Nach Erstellung der Aktivität wird die [!UICONTROL Übersicht] enthält Informationen zur Aktivität, einschließlich eines Diagramms zu Ihrer Aktivität.

## Schulungsvideo: Erstellen von A/B-Tests (8:36) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Arbeitsablaufs mit drei Schritten ein A/B-Test erstellt wird.

* Erstellen Sie eine [!UICONTROL A/B-Test] Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
