---
keywords: Automated Personalization;App
description: Erfahren Sie, wie Sie eine [!UICONTROL Automated Personalization]-Aktivität (AP) mit dem [!UICONTROL Visual Experience Composer] erstellen.
title: Wie erstelle ich eine [!UICONTROL Automated Personalization]-Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
TQID: 'https://experienceleague.adobe.com/5eUFwob4BekIJP4SM2lrSDQam4h1AXIByJjM7-1RNL8'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: c86619f0c004279bf4d9b871c84bf2e37ba932b7
workflow-type: tm+mt
source-wordcount: '1963'
ht-degree: 18%
---
# Erstellen einer [!UICONTROL Automated Personalization]-Aktivität {#create-ap-activity}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine **[!UICONTROL Automated Personalization]** (AP)-Aktivität im **[!UICONTROL Visual Experience Composer]** (VEC) erstellen. Sie erstellen Ihre Erlebnisse, legen Zielgruppenbestimmungen und eine Kontrollgruppe fest und konfigurieren dann Ziele und Einstellungen.

>[!ENDSHADEBOX]

Der Workflow für die Aktivität **0&rbrace;Automated Personalization&quot; in [!DNL Target] unterscheidet sich vom Workflow der anderen Aktivitätstypen.** Es folgt dem angeleiteten dreistufigen Workflow im **[!UICONTROL Visual Experience Composer]**:

1. [Erstellen von Erlebnissen](#build-experiences)
1. [Zielgruppenbestimmung festlegen](#set-targeting)
1. [Ziele und Einstellungen konfigurieren](#configure-goals-and-settings)

## Bevor Sie beginnen {#before-you-begin}

Um eine optimale Leistung zu erzielen, sollten Sie Ihre **[!UICONTROL Automated Personalization]**- und **[!UICONTROL Automatisches Targeting]**-Aktivitäten innerhalb dieser Grenzen halten:

* 4-6 Standorte, mit 4-6 Angeboten pro Standort.
* Unter 5.000 Erlebnisse für beste Ergebnisse. Die feste Grenze beträgt 30.000, und dieselbe Grenze gilt, wenn die Option **[!UICONTROL Duplikate nicht zulassen]** aktiviert ist.

Die Gesamtzahl der Erlebnisse wächst aus der kartesischen Kombination von Standorten und Angeboten. Größere Konfigurationen können zu langsamem Laden oder Bearbeiten im **[!UICONTROL Visual Experience Composer“]**.

## Schritt 1: Erstellen Sie Erlebnisse {#build-experiences}

Den Pool von Inhaltsvarianten definieren, mit denen **[!UICONTROL Automated Personalization]** personalisiert werden kann. Je umfassender und differenzierter Ihre Erlebnisse und Angebote sind, desto besser kann der Algorithmus den richtigen Inhalt für jeden Besucher abgleichen.

### Erstellen der Aktivität {#create-activity}

Starten Sie die Aktivität und öffnen Sie die Seite, die Sie personalisieren möchten, im **[!UICONTROL Visual Experience Composer]** (VEC).

1. Klicken Sie in der Liste [!DNL Target] **[!UICONTROL Aktivitäten]** auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Automated Personalization]**.

   ![](../assets/ap-activities-2.png)

1. Wählen Sie Ihren Experience Composer:

   * Um den **[!UICONTROL Visual Experience Composer)]** verwenden, klicken Sie auf **[!UICONTROL Visual]**.

   * Um den **[!UICONTROL formularbasierten Experience Composer]** zu verwenden, wählen Sie stattdessen **[!UICONTROL Formular]** aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

     >[!NOTE]
     >
     >Zusätzlich zum VEC und **[!UICONTROL Form-Based Experience Composer]** bietet [!DNL Target] den **[!UICONTROL Single Page Application VEC]**. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md). Informationen zur Fehlerbehebung bei VEC finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

     ![](../assets/ap-activities-3.png)

1. (Bedingt) [Wählen Sie einen Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geben **[!UICONTROL im Feld]**-URL eingeben Ihre [Aktivitäts-URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md) an. Wenn Ihr Konto [mit einer Standard-URL konfiguriert wurde](/help/main/administrating-target/visual-experience-composer-set-up.md), dann wird diese URL standardmäßig angezeigt. Sie können bei Bedarf von der Standardeinstellung zu einer anderen URL wechseln.

   Beachten Sie, dass [!DNL Target] nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]) unterscheidet. Daher stimmen [!DNL `http://www.adobe.com/de`] und [!DNL `https://www.adobe.com/de`] überein.

1. Klicken Sie dann auf **[!UICONTROL Erstellen]**. Die Seite mit der angegebenen URL wird in VEC geöffnet.

1. Um die Aktivität zu benennen, klicken Sie auf das Symbol **[!UICONTROL Bearbeiten]** ( ![Bearbeiten-Symbol](/help/main/assets/icons/Edit.svg) ), geben Sie einen beschreibenden Namen für die Aktivität ein und klicken Sie dann auf **[!UICONTROL Speichern]**.

   {{activity-name-rules}}

   ![](../assets/ap-activities-1.png)

### Inhaltserstellung {#design-content}

Richten Sie den Inhalt ein, den der Algorithmus kombinieren kann, und schließen Sie alle Erlebnisse aus, die Sie nicht möchten.

1. Ändern Sie die Seitenelemente wie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) beschrieben.

   * Um schnell mehrere Bilder in der Vorschau anzuzeigen, wählen Sie im Asset-Manager mehrere Bilder gleichzeitig aus. Sie können dann die Seite mit jedem Bild anzeigen, das für die Aktivität konfiguriert wurde.
   * Um den Text in Ihren Angeboten zu ändern, bearbeiten Sie das Textelement direkt auf der Seite.

   Wenn Sie ein Element bearbeiten, werden bei diesem Element Balken angezeigt, die anzeigen, dass Sie es geändert haben.

1. Klicken Sie auf das **[!UICONTROL Inhalt verwalten]**-Symbol ( ![Symbol „Inhalt verwalten](/help/main/assets/icons/Experience.svg) ), um die verfügbaren Kombinationen zu konfigurieren.

   Das **[!UICONTROL Inhalt verwalten]** wird mit zwei Registerkarten geöffnet: **[!UICONTROL Erlebnisse]** und **[!UICONTROL Angebote]**.

   ![](../assets/ap-activities-4.png)

1. Überprüfen Sie **[!UICONTROL Registerkarte]** Erlebnisse“ die Liste der Inhaltselemente und den Speicherort, dem sie jeweils zugewiesen sind.

1. (Optional) Um Erlebnisse aus der Aktivität auszuschließen, aktivieren Sie das Kontrollkästchen für jedes Erlebnis, das Sie ausschließen möchten, und klicken Sie dann auf das Symbol **[!UICONTROL Ausschließen]**.

   Weitere Optionen finden Sie unter [Verwalten von Ausschlüssen](/help/main/c-activities/t-automated-personalization/managing-exclusions.md).

   ![](../assets/ap-activities-5.png)

1. (Bedingt) Klicken Sie auf die Registerkarte **[!UICONTROL Angebote]**, um die Angebote in der Aktivität zu verwalten.

   * Um die Angebote für das Reporting zu organisieren, wählen Sie Inhaltselemente aus und weisen Sie sie Berichtsgruppen zu. Weitere Informationen finden Sie unter [Berichtsgruppen für Angebote in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).
   * Um zu begrenzen, wer ein Angebot sieht, verwenden Sie Targeting , damit nur bestimmte Besucher dieses Angebot sehen können.

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the **[!UICONTROL Disallow Duplicates]** option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.
-->

1. Klicken **[!UICONTROL auf]** Fertig“, wenn Sie die Einrichtung des Inhalts Ihrer Aktivität abgeschlossen haben.

## Schritt 2: Zielgruppenbestimmung festlegen {#set-targeting}

Entscheiden Sie, welche Besucher in die Aktivität eintreten und wie viel Traffic offen gelegt wird. Kombinieren Sie sie mit einer Kontrollgruppe, damit [!DNL Target] die Ergebnisse der Aufstiegspersonalisierung messen können.

1. Klicken Sie **[!UICONTROL Targeting]** oben in **[!UICONTROL Visual Experience Composer]**, um mit dem nächsten Schritt im dreistufigen Workflow fortzufahren.

   ![AP-Test-Targeting-Schritt](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

1. (Bedingt) Klicken Sie auf das Steuerelement **[!UICONTROL Alle Besucher]**, um [eine andere Zielgruppe &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) die Aktivität auszuwählen und ihren Besucherprozentsatz festzulegen.

   Die **[!UICONTROL Alle Besucher]**-Zielgruppe ist als Standard festgelegt. Wenn Sie eine andere Zielgruppe auswählen, wird deren Name im Steuerelement ganz links angezeigt. Beispiel: Sie können Einträge auf 50 % aller Besucher oder 45 % der Zielgruppe aus Kalifornien begrenzen.

1. Klicken Sie auf **[!UICONTROL Steuerung „Traffic]** Zuordnung“ und wählen Sie eine der folgenden Optionen:

   ![Optionen für das Traffic-Zuordnungsziel](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   +++Optionen für das Traffic-Zuordnungsziel

   | Option | Einsatz |
   |--- |--- |
   | **[!UICONTROL Personalization-Algorithmus auswerten (50/50)]** | Ihr Ziel ist es, den Algorithmus zu testen. Besucher werden im Verhältnis 50/50 zwischen dem Steuerelement und dem Zielalgorithmus aufgeteilt. Diese Aufspaltung liefert die genaueste Schätzung der Steigerung. Sie ist die schnellste und genaueste Methode, um zu testen, ob der Algorithmus besser funktioniert als keine Personalisierung (z. B. eine zufällig bereitgestellte Kontrolle). Wird zur Verwendung mit „zufälligen Erlebnissen“ als Kontrolle vorgeschlagen. |
   | **[!UICONTROL Maximieren des Personalization-Traffics (90/10)]** | Ihr Ziel ist es, eine „Always on“-Aktivität zu erstellen. 10 % der Besucher gehen in die Steuerung, die sicherstellt, dass genügend Daten vorhanden sind, damit die Algorithmen im Laufe der Zeit weiterlernen können. Dies ist die schnellste und genaueste Methode, um den Umfang des Traffics zu maximieren, der personalisiert wird, wenn Sie weniger mit der exakten Steigerung beschäftigt sind. Der Nachteil ist, dass man weniger Präzision in der genauen Steigerung hat. Unabhängig von Ihrem Ziel ist diese Option die empfohlene Traffic-Aufteilung, wenn Sie ein bestimmtes Erlebnis als Kontrolle verwenden. |
   | **[!UICONTROL Zuordnung anpassen]** | Die Prozentsätze sollten manuell aufgeteilt werden. |

   +++

1. (Bedingt) Wählen Sie aus der **[!UICONTROL Kontrolle]** Dropdown-Liste [Bestimmtes Erlebnis, das als Kontrolle verwendet werden soll](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oder wählen Sie **[!UICONTROL Zufälliges Erlebnis]**.

   Das Kontrollerlebnis liefert einen Vergleich, um zu ermitteln, welche Steigerung der automatisierte Test ermöglicht. **[!UICONTROL Automated Personalization]** misst die Leistung immer an einer Kontrollgruppe. Es empfiehlt sich, mindestens 10 % der Teilnehmer in der Kontrollgruppe zu platzieren.

   >[!NOTE]
   >
   >In **[!UICONTROL Automated Personalization]** werden Einstiegskriterien (URL-Targeting, Vorlagenregeln und Zielgruppenziele) für jede Anfrage ausgewertet. In älteren Versionen wurden Eingabekriterien nur einmal pro Sitzung bewertet.

## Schritt 3: Ziele und Einstellungen konfigurieren {#configure-goals-and-settings}

Teilen Sie [!DNL Target] mit, wie der Erfolg aussieht. Das von Ihnen gewählte Optimierungsziel ist die Metrik, mit der der Personalisierungsalgorithmus trainiert, also wählen Sie das Ergebnis aus, das für diese Aktivität am wichtigsten ist.

1. Klicken Sie **[!UICONTROL Weiter]**, um die Seite **[!UICONTROL Ziele und Einstellungen]** anzuzeigen.

1. Konfigurieren Sie die Aktivität mit den folgenden Einstellungen und klicken Sie dann auf **[!UICONTROL Speichern und schließen]**.

   | Einstellung | Beschreibung |
   |--- |--- |
   | **[!UICONTROL Name]** | Benennen Sie die Aktivität. Geben Sie der Aktivität einen Namen, der aussagekräftig genug ist, damit die Team-Mitglieder sie in der Liste **[!UICONTROL Aktivitäten]** erkennen können. Befolgen Sie die in Schritt 1: [&#x200B; von Erlebnissen &#x200B;](#build-experiences) Aktivitätsnamenregeln. |
   | **[!UICONTROL Ziel]** | (Optional) Geben Sie das Ziel des Tests ein. Das Ziel hilft Ihnen, den Zweck der Aktivität zu verinnerlichen. |
   | **[!UICONTROL Priorität]** | Legt fest, welche Aktivität angezeigt wird, wenn mehrere Aktivitäten einen Standort und eine Zielgruppe gemeinsam haben. Siehe [Festlegen der Priorität](#set-priority). |
   | **[!UICONTROL Dauer]** | Legen Sie Start- und Enddatum für die Aktivität fest. Sie können **[!UICONTROL Bei Aktivierung]** auswählen oder ein bestimmtes Datum und eine bestimmte Uhrzeit angeben. |
   | **[!UICONTROL Optimierungsziel]** | Die Metrik, mit der der Personalisierungsalgorithmus trainiert. Siehe [Optimierungsziel festlegen](#set-optimization-goal). |
   | **[!UICONTROL Konversionsmetrik]** | Standardmäßig ist die Konversionsmetrik mit der Optimierungszielmetrik identisch. Sie können jedoch eine separate Konversionsmetrik definieren, indem Sie die Option **[!UICONTROL Wie Optimierungsziel]** deaktivieren. |
   | **[!UICONTROL Zusätzliche Metriken]** | Fügen Sie alle zusätzlichen Berichtsmetriken hinzu, die Sie verwenden möchten. Sie können Konversions- oder Umsatzmetriken hinzufügen.<P>**Hinweis**: Die Metrik **[!UICONTROL Interaktion]** wird nicht als zusätzliche Metrik unterstützt. Mit der [!DNL Target] Benutzeroberfläche können Sie möglicherweise die Metrik **[!UICONTROL Interaktion]** auswählen, aber die Daten werden in Berichten nicht genau angezeigt. |
   | **[!UICONTROL Zielgruppen für das Reporting]** | Fügen Sie Zielgruppen hinzu, um die Filterung nach Zielgruppen in Berichten zu ermöglichen. Standardmäßig zeigen die Berichte Ergebnisse für alle berechtigten Besucher. Fügen Sie Zielgruppen hinzu, um Ergebnisse nach spezifischeren Besucheruntergruppen zu filtern.<P>**Hinweis**: Im Gegensatz zu anderen Aktivitätstypen kann **[!UICONTROL Automated Personalization]** **[!UICONTROL Adobe Analytics]** nicht als Berichtsquelle (A4T) verwenden. |
   | **[!UICONTROL Hinweise]** | Geben Sie alle Informationen zu Ihrer Aktivität ein, die für Sie oder andere Team-Mitglieder nützlich sind. Die **[!UICONTROL Anmerkungen]** lässt sich in der Größe ändern. |

   Beim Benennen oder Umbenennen einer Metrik sind die folgenden Zeichen nicht zulässig: `/`, `?`, `#`, `:`, `=`, `+`, `-` und `@`.

### Festlegen der Priorität {#set-priority}

Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt.

Je nach Ihren Einstellungen variieren die [!DNL Target] Benutzeroberfläche und die Optionen für **[!UICONTROL Priorität]**:

* **Legacy-Prioritäten (Standard):** Wenn keine detaillierten Prioritäten aktiviert sind, geben Sie die Priorität **[!UICONTROL Niedrig]**, **[!UICONTROL Medium]** oder **[!UICONTROL Hoch]** an.
* **Detaillierte Prioritäten:** Geben Sie einen Wert zwischen 0 und 999 an, wobei 0 = Niedrig und 999 = Hoch sind. Um diese Option zu aktivieren **[!UICONTROL klicken Sie auf]** > **[!UICONTROL Berichterstellung]** und schalten Sie die Option **[!UICONTROL Aktivieren von]** auf „Ein“ um.

Für Aktivitäten, die in früheren Versionen von [!DNL Target Standard/Premium] erstellt wurden **[!UICONTROL wird die Priorität „Niedrig]** in 0, die Priorität **[!UICONTROL Medium]** in 5 und die Priorität **[!UICONTROL Hoch]** in 10 konvertiert. Diese Werte können nach Wunsch angepasst werden.

>[!NOTE]
>
>Bevor Sie nach der Verwendung feinkörnige Prioritäten deaktivieren können, müssen alle Prioritäten auf 0, 5 und 10 zurückgesetzt werden.

### Optimierungsziel festlegen {#set-optimization-goal}

Das Optimierungsziel besteht aus zwei Parametern:

* dem, was Sie mit der Aktivität messen möchten,
* Die von einem Aktivitätsteilnehmer durchgeführte Aktion, die zeigt, dass das Ziel erreicht wurde

Sie können das Optimierungsziel benennen, indem Sie die drei Punkte rechts von &quot;**[!UICONTROL Primäres Ziel“]**. **[!UICONTROL Automated Personalization]**-Aktivitäten können **[!UICONTROL Konversion]** oder (**[!UICONTROL )]**. Die Konvertierung kann durch Anzeigen einer Seite oder einer Mbox erreicht werden. Es können auch Klicks verfolgt werden.

Das primäre Ziel wird auch die Modellierungsmetrik, die vom Modellierungssystem zur Berechnung des Erfolgs des Erlebnisses verwendet wird.

Besucher können zu Tracking-Zwecken in der Aktivität beibehalten werden, nachdem Sie das Modellierungsziel erreicht haben. Beispielsweise wird oft eine **[!UICONTROL Automated Personalization]**-Aktivität verwendet, um die Klickraten zu verbessern, und dies wird als Modellierungsziel festgelegt. Es ist jedoch wichtig zu sehen, wie erhöhte Klickraten zu einer endgültigen Konversion führen, daher ist das Tracking durch die endgültige Konversion wichtig.

#### Eine Metrik von einer anderen abhängig machen {#add-dependency}

Sie können für mehrere Metriken Abhängigkeiten erstellen und die flexible Auswahl ermöglichen, ob die Metrik erreicht werden soll oder nicht, damit sich die Anzahl erhöht. Sie müssen beide (oder mehrere) Erfolgsmetriken definieren, bevor Sie eine Abhängigkeit voneinander festlegen können. Mithilfe der Option **[!UICONTROL Abhängigkeit hinzufügen]** kann die Erfolgsmetrik inkrementiert werden, wenn eine andere Erfolgsmetrik erreicht oder nicht erreicht wurde.

So fügen Sie eine Abhängigkeit hinzu:

1. Nachdem Sie zusätzliche Metriken hinzugefügt haben **[!UICONTROL klicken Sie]** das Dreipunkt-Menü rechts neben **[!UICONTROL Zusätzliches Ziel]**.

1. Klicken Sie auf **[!UICONTROL Option &quot;]** hinzufügen“ unten im Abschnitt **[!UICONTROL Reporting-Einstellungen]**.

1. Verschieben Sie die gewünschte Metrik per Drag-and-drop vom linken Bereich in den rechten Bereich. Klicken Sie dann auf **[!UICONTROL Erreicht]**, um die Einstellung zwischen **[!UICONTROL Erreicht]** und **[!UICONTROL Nicht erreicht]** zu wechseln.

Sie können Abhängigkeiten bearbeiten oder entfernen, nachdem Sie sie hinzugefügt haben.

## Erlebnisvorschau {#preview-experiences}

Überprüfen Sie, wie Ihre Erlebnisse auf Ihrer Site aussehen, bevor Sie die Aktivität starten.

1. Nachdem Sie auf **[!UICONTROL Speichern und schließen]** geklickt haben, wird die Seite **[!UICONTROL Übersicht]** der Aktivität angezeigt. Klicken Sie **Erlebnisse in der Vorschau**.

1. Im angezeigten Popup-Fenster können Sie Links zu Ihren API-Erlebnissen auf Ihrer Site anzeigen und freigeben. Diese Links geben Ihnen eine „echte Vorschau“ der Erlebnisse außerhalb des **[!UICONTROL Target]** **[!UICONTROL Visual Experience Composer]** (VEC).

   >[!NOTE]
   >
   >Sie müssen die Links in der Nachricht freigeben, um die Vorschau freigeben zu können. Das Klicken auf einen Link und das anschließende Kopieren der URL direkt aus dem Browser funktioniert nicht. Durch Kopieren des Links enthält die URL einen Parameter, der die Seite nur dann korrekt anzeigt, wenn Sie über den Link in der Nachricht auf die Seite zugreifen.

Weitere Informationen zur Berichterstellung finden Sie unter [Automatisierte Personalisierungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).
