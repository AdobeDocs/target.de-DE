---
description: Visual Experience Composer (VEC) bietet eine visuelle Oberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer Erlebnis-Targeting (XT)-Aktivität.
keywords: Erlebnis erstellen;Erlebniserstellung;Priorität;Zielgruppe;Erlebnis;Visual Experience Composer
seo-description: Der Visual Experience Composer (VEC) von Adobe Target bietet eine visuelle Schnittstelle zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer Erlebnis-Targeting (XT)-Aktivität.
seo-title: Erlebnis erstellen
solution: Target
title: Erlebnis erstellen
topic: Advanced,Standard,Classic
uuid: ce559c3c-5a16-46b8-b2a7-df696626c7c0
translation-type: tm+mt
source-git-commit: 6911a91aba8505e8f91a7ab9723c54bd8e7082b7

---


# Create experience{#create-experience}

The [!UICONTROL Visual Experience Composer] (VEC) provides a visual interface for editing the experiences on your page in an [!UICONTROL Experience Targeting] (XT) activity.

1. Wählen Sie die Elemente, die Sie ändern möchten, und nehmen Sie die gewünschten Änderungen vor.

   While [creating an XT activity](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), step one of the three-part guided workflow ([!UICONTROL Experiences]) displays the default [!UICONTROL Experience A] with an [!UICONTROL All Visitors] audience.

   ![Zielgruppe für alle Besucher](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Any changes you make now apply to Experience A. In a step below, you'll click **[!UICONTROL Add Experience Targeting]** to create additional experiences.

   Wenn Sie den Mauszeiger über die Elemente auf Ihrer Seite bewegen, werden diese Elemente hervorgehoben. Jedes hervorgehobene Element kann mithilfe des VEC geändert werden. For a list of actions that can be performed on an element to change the experience, see [Visual Experience Composer Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   If you created an mbox on the page using [!DNL Target Classic], that mbox appears as an element that shows the mbox name, and can be modified like any other element.

   >[!NOTE]
   >
   >Standardmäßig lässt VEC keine Änderungen an Elementen zu, die javascript enthalten, wie zum Beispiel sich drehende Banner. Sie können javascript deaktivieren, um diese Elemente mithilfe des VEC zu ändern.

1. To create additional experiences, click **[!UICONTROL Add Experience Targeting]**.

   ![Link "Erlebnis-Targeting hinzufügen «](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   The [!UICONTROL Choose Audience] dialog box displays. Um ein Erlebnis auf eine Zielgruppe auszurichten, müssen Sie die Zielgruppe auswählen, bevor Sie ein Erlebnis hinzufügen können.

   The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of [!DNL Target]. You can select an audience from the library or [create a new audience](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Wenn Sie eine Zielgruppe erstellen, können Sie einen Standort (mbox) auswählen und Parameter für ihn festlegen. Under [!UICONTROL Custom] (Create Audience &gt; Add Rule &gt; Custom), select the mbox, then specify the desired parameters.

   >[!NOTE]
   >
   >Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als 10 Minuten sind.

1. Select one or more audiences to target with the experience, then click **[!UICONTROL Done]**.

   ![Erlebnis B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Beachten Sie, dass Erlebnis B jetzt in der obigen Abbildung angezeigt wird und dieses Erlebnis auf die Zielgruppe "US-Besucher" abzielt.

1. Wählen Sie die Elemente aus, die Sie für dieses Erlebnis ändern möchten, und nehmen Sie die gewünschten Änderungen vor, die in Schritt 1 erläutert werden.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf zusätzliche zielgerichtete Erlebnisse zu erstellen.

1. Click **[!UICONTROL Next]** when you are finished designing your experiences.

   Das Aktivitätsdiagramm wird angezeigt:

   ![XT-Targeting-Diagramm](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >If you deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `adobe.com`), that image does not display in the thumbnail of the page shown in the flow diagram.

1. (Bedingt) Ziehen Sie Zielgruppen/Erlebnispaare per Drag &amp; Drop, während Sie XT-Aktivitäten erstellen oder bearbeiten, um Paare in der gewünschten Reihenfolge anzuordnen.

   Besucher werden von oben nach unten für Erlebnisse ausgewertet.

   ![Erlebnisse verschieben](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Beim Erlebnis-Targeting kommt es auf die Reihenfolge an. ] Wenn ein Besucher unter das erste Zielgruppen-/Erlebnispaar fällt, wird das erste Erlebnis bereitgestellt.

   Nehmen wir beispielsweise an, Ihnen war nicht bewusst, dass es beim Erstellen einer XT-Aktivität auf die Reihenfolge ankommt. Später im Verlauf des Tests stellen Sie fest, dass sich Besucher, die sich Ihrer Meinung nach eigentlich für Erlebnis B oder C qualifizieren müssten, stattdessen für Erlebnis A qualifizieren. Eine Ursache dafür könnte sein, dass sich die Zielgruppen nicht gegenseitig ausschließen und sich nicht in der richtigen Reihenfolge befinden (z. B. Erlebnis A = USA, Erlebnis B = San Francisco und Erlebnis C = Kalifornien). In diesem Szenario qualifizieren sich alle Benutzer aus den USA für Erlebnis A, selbst wenn sie in San Francisco oder in einem anderen Ort in Kalifornien leben. Sie können die Reihenfolge der Zielgruppen-/Erlebnispaare von der stärksten Einschränkung zur geringsten Einschränkung ändern (San Francisco &gt; Kalifornien &gt; USA), ohne die gesamte Aktivität neu erstellen zu müssen.

   If you have an [!UICONTROL All Visitors] audience, ensure that it is not the first audience in the diagram. Ein Erlebnis, das auf „Alle Besucher“ abzielt, kann als das letzte Erlebnis der entsprechenden Targeting-Aktivität eingesetzt werden, um auch die Besucher zu erfassen, die bei keinem anderen Erlebnis erfasst wurden.

## Umbenennen oder Bearbeiten eines Erlebnisses

You can click the [!UICONTROL Edit] icon (three vertical ellipses) on an experience in an XT activity and choose from the following options, as necessary:

* Umbenennen
* Bearbeiten

![Optionen umbenennen und bearbeiten](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Löschen eines Erlebnisses

On the **[!UICONTROL Experiences]** page (the first step in the three-step guided workflow), click the three vertical ellipses &gt; **[!UICONTROL Delete]**.

![Erlebnis löschen](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplizieren eines Erlebnisses

Sie können ein Erlebnis in einer XT-Aktivität kopieren, damit Sie kleinere Änderungen daran vornehmen können, ohne das Erlebnis neu erstellen zu müssen.

Klicken Sie auf der Seite **[!UICONTROL Erlebnisse]** (der erste Schritt im Drei-Schritte-Workflow) auf die drei vertikalen Ellipsen und anschließend auf **[!UICONTROL Duplizieren]**.

![Duplizieren von Erlebnissen](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Vom A/B-Test zum Erlebnis-Targeting

Dieses Video beschreibt, wie Sie A/B-Tests mit Erlebnis-Targeting (XT) erweitern können.

* Drei-Schritte-Workflow zur Konfiguration einer XT-Aktivität
* Bereitstellung standortspezifischer Inhalte für Zielgruppen in unterschiedlichen Gebieten
* Neusortierung von Erlebnissen, um zu gewährleisten, dass der richtige Inhalt der richtigen Zielgruppe bereitgestellt wird

>[!VIDEO](https://video.tv.adobe.com/v/22418/?captions=ger)

### Aktivitätstypen (9:03)

In diesem Video werden die in Target Standard/Premium verfügbaren Aktivitätstypen erläutert. Erlebnis-Targeting wird um 5:15 erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386?captions=ger)

### Verwenden des Visual Experience Composer

In diesem Video erhalten Sie Informationen zum Verwenden der Optionen in Visual Experience Composer.

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399?captions=ger)