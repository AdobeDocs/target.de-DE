---
keywords: create experience;experience create;priority;audience;experience;visual experience composer
description: Der Visual Experience Composer (VEC) von Adobe Target bietet eine visuelle Oberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer Erlebnis-Targeting-Aktivität (XT).
title: Erlebnis erstellen
feature: xt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 93%

---


# Erlebnis erstellen{#create-experience}

Der [!UICONTROL Visual Experience Composer] (VEC) bietet eine visuelle Oberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer [!UICONTROL Erlebnis-Targeting]-Aktivität (XT).

1. Wählen Sie die Elemente, die Sie ändern möchten, und nehmen Sie die gewünschten Änderungen vor.

   Beim [Erstellen einer XT-Aktivität](/help/c-activities/t-experience-target/t-xt-create/xt-create.md) erscheint in Schritt 1 des dreiteiligen Workflows ([!UICONTROL Erlebnisse]) das standardmäßige [!UICONTROL Erlebnis A] mit der Zielgruppe [!UICONTROL Alle Besucher].

   ![Zielgruppe „Alle Besucher“](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Alle Änderungen, die Sie hier vornehmen, gelten für Erlebnis A. Klicken Sie in einem Schritt weiter unten auf **[!UICONTROL Erlebnis-Targeting hinzufügen]**, um weitere Erlebnisse zu erstellen.

   Wenn Sie den Mauszeiger über die Elemente auf Ihrer Seite bewegen, werden diese Elemente hervorgehoben. Alle hervorgehobenen Elemente können mit dem VEC geändert werden. Eine Liste der Aktionen, die für ein Element durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   If you created a [!DNL Target] request on the page using [!DNL Target Classic], that [!DNL Target] request appears as an element that shows the request name, and can be modified like any other element.

   >[!NOTE]
   >
   >Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können JavaScript deaktivieren, um diese Elemente mithilfe des VEC zu ändern.

1. Wenn Sie zusätzliche Erlebnisse erstellen möchten, klicken Sie auf **[!UICONTROL Erlebnis-Targeting hinzufügen]**.

   ![Link „Erlebnis-Targeting hinzufügen“](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Das Dialogfeld [!UICONTROL Zielgruppe auswählen] wird angezeigt. Um mit einem Erlebnis eine Zielgruppe anzusprechen, müssen Sie die Zielgruppe auswählen, bevor Sie ein Erlebnis hinzufügen können.

   Die Zielgruppenbibliothek enthält Zielgruppen, die bereits definiert wurden, einschließlich einiger häufiger Zielgruppen, die als Teil von [!DNL Target] vorgefertigt sind. Sie können eine Zielgruppe aus der Bibliothek auswählen oder [eine neue Zielgruppe erstellen](/help/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Beim Erstellen einer Audience können Sie einen Ort auswählen und Parameter für diesen Ort angeben. Under [!UICONTROL Custom] (Create Audience > Add Rule > Custom), select the location, then specify the desired parameters.

   >[!NOTE]
   >
   >Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als 10 Minuten sind.

1. Wählen Sie mindestens eine Zielgruppe für das Targeting aus und klicken Sie auf **[!UICONTROL Fertig]**.

   ![Erlebnis B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Beachten Sie, dass Erlebnis B jetzt in der vorherigen Abbildung angezeigt wird und die Zielgruppe dieses Erlebnisses Besucher aus den USA ist.

1. Wählen Sie die Elemente aus, die Sie für dieses Erlebnis ändern möchten, und nehmen Sie die gewünschten Änderungen wie in Schritt 1 erläutert vor.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf zusätzliche Target-Erlebnisse zu erstellen.

1. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie mit der Erstellung Ihrer Erlebnisse fertig sind.

   Das Aktivitätsdiagramm wird angezeigt:

   ![XT-Targeting-Diagramm](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Wenn Sie ein Bild aus einer anderen Quelle als der Hauptseite bereitstellen (z. B. ein Bild, das auf `akamai.net` gehostet und auf `adobe.com` bereitgestellt wird), wird das Bild nicht in der Miniaturansicht der Seite, die auf dem Flussdiagramm zu sehen ist, angezeigt.

1. (Abhängig von Ihrer Lizenz) Sie können Zielgruppen-/Erlebnispaare beim Erstellen oder Bearbeiten von XT-Aktivitäten per Drag &amp; Drop verschieben, um die Paare in der gewünschten Reihenfolge anzuordnen.

   Die Besucher werden der Reihe nach von oben nach unten für Erlebnisse bewertet.

   ![Erlebnisse verschieben](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Beim Erlebnis-Targeting kommt es auf die Reihenfolge an. ] Wenn ein Besucher unter das erste Zielgruppen-/Erlebnispaar fällt, wird das erste Erlebnis bereitgestellt.

   Nehmen wir beispielsweise an, Ihnen war nicht bewusst, dass es beim Erstellen einer XT-Aktivität auf die Reihenfolge ankommt. Später im Verlauf des Tests stellen Sie fest, dass sich Besucher, die sich Ihrer Meinung nach eigentlich für Erlebnis B oder C qualifizieren müssten, stattdessen für Erlebnis A qualifizieren. Eine Ursache dafür könnte sein, dass sich die Zielgruppen nicht gegenseitig ausschließen und sich nicht in der richtigen Reihenfolge befinden (z. B. Erlebnis A = USA, Erlebnis B = San Francisco und Erlebnis C = Kalifornien). In diesem Szenario qualifizieren sich alle Benutzer aus den USA für Erlebnis A, selbst wenn sie in San Francisco oder in einem anderen Ort in Kalifornien leben. Sie können die Reihenfolge der Zielgruppen-/Erlebnispaare von der stärksten Einschränkung zur geringsten Einschränkung ändern (San Francisco > Kalifornien > USA), ohne die gesamte Aktivität neu erstellen zu müssen.

   Wenn Ihre Zielgruppe [!UICONTROL Alle Besucher] lautet, stellen Sie sicher, dass es sich nicht um die erste Zielgruppe im Diagramm handelt. Ein Erlebnis, das auf „Alle Besucher“ abzielt, kann als das letzte Erlebnis der entsprechenden Targeting-Aktivität eingesetzt werden, um auch die Besucher zu erfassen, die bei keinem anderen Erlebnis erfasst wurden.

## Umbenennen oder Bearbeiten eines Erlebnisses

Sie können in einem Erlebnis innerhalb einer XT-Aktivität (Erlebnis-Targeting) auf das Symbol [!UICONTROL Bearbeiten] klicken (drei vertikale Ellipsen) und folgende Optionen auswählen:

* Umbenennen
* Bearbeiten

![Umbenennen und Bearbeiten von Optionen](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Löschen eines Erlebnisses

Klicken Sie auf der Seite **[!UICONTROL Erlebnisse]** (der erste Schritt im dreistufigen Workflow) auf die drei vertikalen Ellipsen und anschließend auf **[!UICONTROL Löschen]**.

![Erlebnis löschen](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplizieren eines Erlebnisses

Sie können ein Erlebnis aus einer XT-Aktivität kopieren, um kleinere Änderungen vorzunehmen, ohne das Erlebnis vollständig neu erstellen zu müssen.

Klicken Sie auf der Seite **[!UICONTROL Erlebnisse]** (der erste Schritt im Drei-Schritte-Workflow) auf die drei vertikalen Ellipsen und anschließend auf **[!UICONTROL Duplizieren]**.

![Erlebnis duplizieren](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Vom A/B-Test zum Erlebnis-Targeting

Dieses Video beschreibt, wie Sie A/B-Tests mit Erlebnis-Targeting (XT) erweitern können.

* Drei-Schritte-Workflow zur Konfiguration einer XT-Aktivität
* Bereitstellung standortspezifischer Inhalte für Zielgruppen in unterschiedlichen Gebieten
* Neusortierung von Erlebnissen, um zu gewährleisten, dass der richtige Inhalt der richtigen Zielgruppe bereitgestellt wird

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Aktivitätstypen (9:03)

In diesem Video werden die in Target Standard/Premium verfügbaren Aktivitätstypen erläutert. Erlebnis-Targeting wird um 5:15 erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Verwenden des Visual Experience Composer

In diesem Video erhalten Sie Informationen zum Verwenden der Optionen in Visual Experience Composer.

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)