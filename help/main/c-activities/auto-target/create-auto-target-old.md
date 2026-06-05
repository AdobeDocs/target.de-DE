---
keywords: Automatisches Targeting erstellen;A/B-Test;automatische Targeting-Aktivität;neue A/B-Aktivität;automatisches Targeting;automatisches Targeting für personalisierte Erlebnisse;personalisierte Optimierung
description: Erfahren Sie, wie Sie mit [!UICONTROL Visual Experience Composer] (VEC) in  [!DNL Adobe Target]  eine A/BTest-Aktivität vom Typ Automatisches Targeting“ erstellen.
title: Wie erstelle ich eine Aktivität vom Typ [!UICONTROL Automatisches Targeting]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 39%

---

# Erstellen einer [!UICONTROL automatischen Targeting]-Aktivität

Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] [!UICONTROL A/B-Test] direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu ändern.

>[!NOTE]
>
>[!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).

So erstellen Sie eine [!UICONTROL Automatisches Targeting]-Aktivität:

1. Klicken Sie in der **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL A/B-Test]**.

   ![Dropdownliste „Aktivität erstellen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   Die verfügbaren Aktivitätstypen hängen von Ihrem [!DNL Target]-Konto ab. Einige Aktivitätstypen werden in Ihrer Liste eventuell nicht angezeigt. Beispielsweise ist [!UICONTROL Recommendations] eine [Target Premium-Funktion](/help/main/c-intro/intro.md#premium). Informationen zu den verschiedenen Aktivitätstypen finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md) und im [Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md).

1. Wählen Sie **[!UICONTROL Visual]** aus, falls erforderlich.

   Wenn Sie den [!UICONTROL formularbasierten Experience Composer) bevorzugen] wählen Sie [!UICONTROL Formular]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den Single Page Application VEC. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Abhängig von Ihrer Lizenz) Wenn Sie [Target Premium-Kunde &#x200B;](/help/main/c-intro/intro.md#premium)sind, wählen Sie einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an und klicken Sie dann auf **[!UICONTROL Weiter]**.

   Wenn Ihr Konto mit einer Standard-URL konfiguriert wurde, dann wird diese URL standardmäßig angezeigt. Sie können von der Standard-URL zu einer anderen URL wechseln.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die Seite an, auf die die URL verweist.

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

   Der [!UICONTROL Visual Experience Composer] zeigt nach dem Erstellen einer Aktivität auf der linken Seite zwei Registerkarten an: Erlebnis A und Erlebnis B. Erlebnis A ist das Kontrollerlebnis. Der Fokus liegt auf der Registerkarte Erlebnis B , die Sie nach Bedarf ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können dem Test mehrere Erlebnisse hinzufügen. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Ändern von Erlebnissen in [!UICONTROL Visual Experience Composer] finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie **[!UICONTROL Targeting]** oben in [!UICONTROL Visual Experience Composer], um mit dem nächsten Schritt im dreistufigen Workflow fortzufahren.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität und zum Einrichten der Erlebnisse.

1. Klicken Sie im Feld [!UICONTROL Zielgruppe] auf das Bearbeitungssymbol (das vertikale Auslassungszeichen), klicken Sie auf **[!UICONTROL Zielgruppe ersetzen]** und [die Zielgruppe auswählen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) für Ihre Aktivität.

   Standardmäßig ist die Zielgruppe auf &quot;[!UICONTROL &#x200B; Besucher“ &#x200B;].

1. Wählen Sie den Prozentsatz qualifizierter Besucher aus, der an der Aktivität teilnehmen soll.

   ![Prozentsatz für Zielgruppen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Richten Sie die Traffic-Zuordnung ein.

   Sie können der gleichen Zielgruppe mehrere Erlebnisse zeigen. Es wird ein Diagramm angezeigt, das Ihre ausgewählte Zielgruppe und die Erlebnisse zeigt, die Sie der Aktivität hinzugefügt haben.

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus. Um eine Aktivität [!UICONTROL Automatisches Targeting] zu erstellen, wählen Sie **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]** aus.

   Nachfolgend werden die drei Arten der Traffic-Zuordnung beschrieben:

   * **[!UICONTROL Manuell (Standard)]**: Geben Sie den Prozentsatz der Teilnehmer an, die jedes Erlebnis sehen sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen. Weitere Informationen finden Sie unter [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Automatische Zuordnung zur besten Erfahrung]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [Automatische Zuordnung - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]**: [!DNL Target] nutzt fortschrittliche Machine-Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden und anschließend Besuchern auf der Grundlage ihrer individuellen Kundenprofile und früherer Verhaltensweisen ähnlicher Besucher ein optimal auf sie zugeschnittenes Erlebnis bereitgestellt wird.

   Sie können auch auf **[!UICONTROL Hinzufügen]** klicken, um der Aktivität ein weiteres Erlebnis hinzuzufügen.

1. Wenn Sie mit der Auswahl Ihrer Audience, Erlebnisoptionen und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Weiter]**, um zum dritten Schritt des Drei-Schritte-Workflows überzugehen.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

   >[!NOTE]
   >
   >Wenn Sie „Analytics [&#x200B; Target“ (A4T](/help/main/c-integrating-target-with-mac/a4t/a4t.md) mit dieser Aktivität verwenden möchten, lesen Sie die wichtigen Informationen unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Klicken Sie **[!UICONTROL Speichern und schließen]** oder **[!UICONTROL Speichern]**.

Nachdem Sie die Aktivität erstellt haben, zeigt [!UICONTROL &#x200B; Registerkarte &#x200B;]Übersicht“ Informationen zur Aktivität an, einschließlich eines Diagramms Ihrer Aktivität.

## Schulungsvideo: Erstellen von A/B-Tests (8:36)

In diesem Video wird gezeigt, wie mithilfe des geleiteten [!DNL Target]-Workflows mit drei Schritten ein A/B-Test erstellt wird.

* Erstellen einer [!UICONTROL A/B-Test]-Aktivität in [!DNL Adobe Target]
* Zuordnen von Traffic mithilfe einer manuellen Aufteilung oder automatischen Traffic-Zuordnung

>[!VIDEO](https://video.tv.adobe.com/v/17391)
