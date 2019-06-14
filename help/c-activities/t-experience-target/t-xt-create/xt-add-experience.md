---
description: Visual Experience Composer (VEC) bietet eine visuelle Benutzeroberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite.
keywords: Erlebnis erstellen;Erlebniserstellung;Priorität;Zielgruppe;Erlebnis;Visual Experience Composer
seo-description: Der Visual Experience Composer (VEC) von Adobe Target bietet eine visuelle Benutzeroberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite.
seo-title: Erlebnis erstellen
solution: Target
title: Erlebnis erstellen
topic: Advanced,Standard,Classic
uuid: ce559c3c-5a16-46b8-b2a7-df696626c7c0
translation-type: tm+mt
source-git-commit: 5eb79fcd0407e0da841048bcd0a1b64393490fcf

---


# Erlebnis erstellen{#create-experience}

Visual Experience Composer (VEC) bietet eine visuelle Oberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer Erlebnis-Targeting (XT)-Aktivität.

1. Wählen Sie die Elemente, die Sie ändern möchten, und nehmen Sie die gewünschten Änderungen vor.

   Während [Sie eine XT-Aktivität](/help/c-activities/t-experience-target/t-xt-create/xt-create.md)erstellen, wird der Schritt eines der drei Teilformulare (Erlebnisse) standardmäßig mit [!UICONTROL der Zielgruppe] [!UICONTROL &quot;Alle Besucher] &quot; angezeigt.

   ![Zielgruppe für alle Besucher](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Alle Änderungen, die Sie vornehmen, gelten jetzt für Erlebnis A. In einem Schritt unten klicken Sie auf [!UICONTROL Erlebnis-Targeting] hinzufügen, um weitere Erlebnisse zu erstellen.

   Wenn Sie den Mauszeiger über die Elemente auf Ihrer Seite bewegen, werden diese Elemente hervorgehoben. Jedes hervorgehobene Element kann mithilfe des VEC geändert werden. Eine Liste der Aktionen, die für ein Element durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   Wenn Sie mit Target Classic (früher Test&amp;Target) eine Mbox auf der Seite erstellt haben, wird diese Mbox als Element mit dem Mbox-Namen angezeigt und kann wie jedes andere Element bearbeitet werden.

1. Klicken Sie auf **[!AErlebnis-Targeting, um weitere Erlebnisse zu erstellen]**.

   ![Link &quot;Erlebnis-Targeting hinzufügen «](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Das [!UICONTROL Dialogfeld Zielgruppe] auswählen wird angezeigt. Um ein Erlebnis auf eine Zielgruppe auszurichten, müssen Sie die Zielgruppe auswählen, bevor Sie ein Erlebnis hinzufügen können.

   Die Zielgruppenbibliothek enthält Zielgruppen, die bereits definiert wurden, einschließlich einiger häufiger Zielgruppen, die als Teil von Target vorgefertigt sind. Sie können entweder eine Zielgruppe aus der Bibliothek auswählen oder [eine neue Zielgruppe erstellen](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271). Wählen Sie „Alle Besucher“, um das gleiche Erlebnis für alle Teilnehmer anzuzeigen.

   >[!NOTE]
   >
   >Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Wenn Sie eine Zielgruppe erstellen, können Sie einen Standort (mbox) auswählen und Parameter für ihn festlegen. Wählen Sie unter „Benutzerdefinierte Parameter“ die Mbox und geben Sie dann die gewünschten Parameter an.

   >[!NOTE]
   >
   >Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als 10 Minuten sind.

1. Wählen Sie mindestens eine Zielgruppe für das Targeting aus und klicken Sie auf **[!UICONTROL Fertig]**.

   ![Erlebnis B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Beachten Sie, dass Erlebnis B jetzt in der obigen Abbildung angezeigt wird und dieses Erlebnis auf die Zielgruppe &quot;US-Besucher&quot; abzielt.

1. Wählen Sie die Elemente aus, die Sie für dieses Erlebnis ändern möchten, und nehmen Sie die gewünschten Änderungen vor, die in Schritt 1 erläutert werden.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf zusätzliche zielgerichtete Erlebnisse zu erstellen.

1. Klicken **[!UICONTROL Sie auf Weiter,]** wenn Sie die Entwerfen der Erlebnisse abgeschlossen haben.

   Das Aktivitätsdiagramm wird angezeigt:

   ![XT-Targeting-Diagramm](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

1. (Bedingt) Ziehen Sie Zielgruppen/Erlebnispaare per Drag &amp; Drop, während Sie XT-Aktivitäten erstellen oder bearbeiten, um Paare in der gewünschten Reihenfolge anzuordnen.

   Besucher werden von oben nach unten für Erlebnisse ausgewertet.

   ![Erlebnisse verschieben](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   Beim Erlebnis-Targeting kommt es auf die Reihenfolge an. Wenn ein Besucher unter das erste Zielgruppen-/Erlebnispaar fällt, wird das erste Erlebnis bereitgestellt.

   Nehmen wir beispielsweise an, Ihnen war nicht bewusst, dass es beim Erstellen einer XT-Aktivität auf die Reihenfolge ankommt. Später im Verlauf des Tests stellen Sie fest, dass sich Besucher, die sich Ihrer Meinung nach eigentlich für Erlebnis B oder C qualifizieren müssten, stattdessen für Erlebnis A qualifizieren. Eine Ursache dafür könnte sein, dass sich die Zielgruppen nicht gegenseitig ausschließen und sich nicht in der richtigen Reihenfolge befinden (z. B. Erlebnis A = USA, Erlebnis B = San Francisco und Erlebnis C = Kalifornien). In diesem Szenario qualifizieren sich alle Benutzer aus den USA für Erlebnis A, selbst wenn sie in San Francisco oder in einem anderen Ort in Kalifornien leben. Sie können die Reihenfolge der Zielgruppen-/Erlebnispaare von der stärksten Einschränkung zur geringsten Einschränkung ändern (San Francisco &gt; Kalifornien &gt; USA), ohne die gesamte Aktivität neu erstellen zu müssen.

## Umbenennen oder Bearbeiten eines Erlebnisses

Sie können auf das [!UICONTROL Bearbeitungssymbol] (drei vertikale Auslassungszeichen) eines Erlebnisses in einer XT-Aktivität klicken und nach Bedarf zwischen folgenden Optionen wählen:

* Umbenennen
* Bearbeiten

![Optionen umbenennen und bearbeiten](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Löschen eines Erlebnisses

Klicken Sie auf der Seite **[!UICONTROL Erlebnisse]** (der erste Schritt im geleiteten Arbeitsablauf mit drei Schritten) auf die drei vertikalen Auslassungszeichen &gt; **[!UICONTROL Löschen]**.

![Erlebnis löschen](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplizieren eines Erlebnisses

Sie können ein Erlebnis aus einer XT-Aktivität (Erlebnis-Targeting) kopieren, um kleinere Änderungen vorzunehmen, ohne das Erlebnis vollständig neu erstellen zu müssen.

Klicken Sie auf der Seite **[!UICONTROL Erlebnisse]** (der erste Schritt im Drei-Schritte-Workflow) auf die drei vertikalen Ellipsen und anschließend auf **[!UICONTROL Duplizieren]**.

![Duplizieren von Erlebnissen](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Schulungsvideo: Verwenden von Visual Experience Composer

In diesem Video erhalten Sie Informationen zum Verwenden der Optionen in Visual Experience Composer.

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399?captions=ger)