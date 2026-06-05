---
keywords: A/B erstellen;A/B-Test;A/B-Aktivität;neue A/B-Aktivität;A/B erstellen
description: Verwenden Sie den [!UICONTROL Visual Experience Composer] (VEC), um A/B-Test -Aktivitäten direkt auf einer  [!DNL Target] Seite zu erstellen.
title: Wie erstelle ich einen A/B-Test?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
TQID: https://experienceleague.adobe.com/3oJeJ1q8KeFLZhUJseG6hOe6xJqH4CKILIUglcL7E3M
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1019
ht-degree: 19%

---

# Erstellen einer A/B-Test -Aktivität

Nutzen Sie den [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target], um [!UICONTROL A/B-Test]-Aktivitäten direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Seitenabschnitte in [!DNL Target] zu ändern.

>[!NOTE]
>
>Zusätzlich zur Aktivität [!UICONTROL Manuell] (Standard) [!UICONTROL A/B-Test] (siehe Abschnitt in diesem Artikel) bietet [!DNL Target] zwei zusätzliche Typen von [!UICONTROL A/B-Test]-Aktivitäten: [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting].
>
>Siehe [Typen von A/B-Testaktivitäten](/help/main/c-activities/t-test-ab/test-ab.md#types) in *A/B-Test - Übersicht*.

So erstellen Sie eine manuelle [!UICONTROL A/B-Test]-Aktivität:

1. Klicken Sie in der **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL A/B-Test]**.

1. Wählen Sie im Dialogfeld [!UICONTROL A/B]Testaktivität erstellen **[!UICONTROL bei]** die Option „Visuell“ aus.

   Wenn Sie den [!UICONTROL formularbasierten Experience Composer) bevorzugen] wählen Sie [!UICONTROL Formular]. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] das [!UICONTROL Single Page Application] VEC. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wenn Sie [Target Premium-Kunde sind](/help/main/c-intro/intro.md#premium) wählen Sie aus der Dropdown-Liste **[!UICONTROL Workspace auswählen]** einen ([) &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Die Option [[!UICONTROL Arbeitsplatz auswählen]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) ist eine [Target Premium](/help/main/c-intro/intro.md)-Funktion und wird möglicherweise nicht angezeigt, wenn Ihr Unternehmen über eine [!UICONTROL Target Standard]-Lizenz verfügt.

1. Geben **[!UICONTROL im Feld]**-URL eingeben Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an.

   Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standardeinstellung zu einer anderen URL wechseln.

1. Klicken Sie **[!UICONTROL Erstellen]**.

   Der [!UICONTROL Visual Experience Composer] wird geöffnet und zeigt die Seite an, auf die die URL verweist.

1. Klicken Sie zum Benennen der Aktivität auf das Symbol **[!UICONTROL Bearbeiten]** ( ![Bearbeiten-Symbol](/help/main/assets/icons/Edit.svg) ) neben &quot;[!UICONTROL Nicht benannte Aktivität], geben Sie einen beschreibenden Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

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

   Im [!UICONTROL Visual Experience Composer] finden Sie nach der Erstellung einer Aktivität zwei Registerkarten auf der linken Seite: Erlebnis A und Erlebnis B. Erlebnis A ist hierbei das Kontrollerlebnis. Der Fokus liegt auf der Registerkarte Erlebnis B , die Sie nach Bedarf ändern können. Erlebnis B ist das alternative Erlebnis, das Sie Ihrem Test hinzufügen können. Sie können mehrere Erlebnisse zum Test hinzufügen, indem Sie auf das Symbol [!UICONTROL Hinzufügen] ( ![Symbol hinzufügen](/help/main/assets/icons/Add.svg) ) oben im Bereich [!UICONTROL Erlebnisse] klicken. Sie können Erlebnis A außerdem aus der Aktivität löschen, wenn Sie kein Standarderlebnis für die Site festlegen möchten.

   Weitere Informationen zum Hinzufügen und Ändern von Erlebnissen in [!UICONTROL Visual Experience Composer] finden Sie unter [Erlebnis hinzufügen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Möchten Sie Erlebnis B bearbeiten, beginnen Sie mit Schritt 2.

1. Klicken Sie **[!UICONTROL Targeting]** oben in [!UICONTROL Visual Experience Composer], um mit dem nächsten Schritt im dreistufigen Workflow fortzufahren.

   Das Flussdiagramm wird geöffnet.

   ![Targeting-Schritt im A/B-Test](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   Das Flussdiagramm führt Sie durch die Schritte Zuweisen einer Zielgruppe und ihres Traffic-Prozentsatzes, Auswählen der Traffic-Zuordnungsmethode und Festlegen der Traffic-Zuordnung für jedes Erlebnis in der Aktivität.

1. (Bedingt) Klicken Sie auf das Steuerelement **[!UICONTROL Alle Besucher]**, um eine andere Zielgruppe für die Aktivität auszuwählen.

   Die [!UICONTROL Alle Besucher]-Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt.

   Daraufhin wird der rechte Rahmen angezeigt, über den Sie eine Zielgruppe hinzufügen oder löschen und den Prozentsatz der Besuchenden für die Aktivität zuweisen können.

   1. Um die Audience zu ändern, klicken Sie auf **[!UICONTROL Ersetzen]-Symbol** ( ![Ersetzen-Symbol](/help/main/assets/icons/Retweet.svg) ) im rechten Rahmen.
   1. Wählen Sie [!UICONTROL &#x200B; Dialogfeld &#x200B;]Zielgruppe hinzufügen[&#x200B; die gewünschte Zielgruppe aus &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) klicken Sie dann auf **[!UICONTROL Zielgruppe zuweisen]**.

      Sie können auf **Kombinieren von Zielgruppen** klicken, um [eine Zielgruppe zu erstellen, die mehrere Zielgruppen kombiniert](/help/main/c-target/combining-multiple-audiences.md).

      Wenn Sie eine neue Zielgruppe erstellen müssen, die sich noch nicht in der [!UICONTROL Zielgruppenbibliothek“ befindet] klicken Sie auf **Zielgruppe erstellen**. Während des [Zielgruppen-Workflows erstellen](/help/main/c-target/c-audiences/audiences.md) können Sie aus den folgenden Optionen auswählen:

      * **[!UICONTROL Zielgruppenbibliothek]**: Erstellen Sie eine On-Demand-Zielgruppe, die in der [!UICONTROL Zielgruppenbibliothek] gespeichert wird und in anderen Aktivitäten wiederverwendet werden kann.
      * **[!UICONTROL Nur diese Aktivität]**: Erstellen Sie eine [aktivitätsspezifische Zielgruppe](/help/main/c-target/creating-activity-only-audience.md) die nicht in der [!UICONTROL Zielgruppenbibliothek] gespeichert wird und nur in der aktuellen Aktivität verwendet werden kann.

   1. Klicken Sie **[!UICONTROL rechten Feld auf]** Besucherprozentsatz) und wählen Sie dann den Prozentsatz der qualifizierten Besucher aus, die Sie in die Aktivität eingeben möchten.

   Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Klicken Sie auf **[!UICONTROL Traffic-]**) und wählen Sie dann im rechten Bereich die gewünschte Traffic-Zuordnungsmethode aus, wie unten dargestellt:

   ![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

   Wählen Sie die gewünschte Traffic-Zuordnungsmethode aus:

   * **[!UICONTROL Manuell (Standard)]**: Geben Sie den Prozentsatz der Teilnehmer an, die jedes Erlebnis sehen sollen. Sie können den Prozentsatz gleichmäßig auf alle Erlebnisse aufteilen oder für jedes Erlebnis einen höheren oder niedrigeren Prozentsatz festlegen. Die gesamte Anzahl aller Erlebnisse muss 100 % betragen.

   * **[!UICONTROL Automatische Zuordnung zur besten Erfahrung]**: Die meisten Aktivitätsteilnehmer werden automatisch zu Erlebnissen mit höherer Leistung weitergeleitet. Einige Besucher werden allen Erlebnissen zugeordnet, um die Erforschung von Erlebnissen beizubehalten und Änderungen an Leistungstrends zu erkennen. Weitere Informationen finden Sie unter [[!UICONTROL Automatische Zuordnung] - Übersicht](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]**: [!DNL Target] nutzt fortschrittliche Machine-Learning-Algorithmen zur Personalisierung von Inhalten und Förderung von Konversionen, indem mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse identifiziert werden und anschließend Besuchern auf der Grundlage ihrer individuellen Kundenprofile und früherer Verhaltensweisen ähnlicher Besucher ein optimal auf sie zugeschnittenes Erlebnis bereitgestellt wird. Weitere Informationen finden Sie unter [Automatisches Targeting - Übersicht](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Klicken Sie **[!UICONTROL rechten Bereich auf]** Erlebnisse“ und geben Sie dann für jedes Erlebnis die gewünschte Traffic-Zuordnung an.

1. Wenn Sie mit der Auswahl Ihrer Audience, Erlebnisoptionen und Traffic-Zuordnung zufrieden sind, klicken Sie auf **[!UICONTROL Weiter]**, um zum dritten Schritt des Drei-Schritte-Workflows überzugehen.

1. Legen Sie [Ziele und Einstellungen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) für die Aktivität fest.

1. Klicken Sie **[!UICONTROL Speichern und schließen]** oder **[!UICONTROL Speichern]**.

Nachdem Sie die Aktivität erstellt haben, zeigt [!UICONTROL &#x200B; Registerkarte &#x200B;]Übersicht“ Informationen zur Aktivität an, einschließlich eines Diagramms Ihrer Aktivität.
