---
keywords: Erlebnis erstellen;Erlebniserstellung;Priorität;Zielgruppe;Erlebnis;Visual Experience Composer
description: Erfahren Sie, wie Sie die [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) zum Erstellen und Bearbeiten von Erlebnissen auf Ihrer Seite in einer [!UICONTROL Erlebnis-Targeting] (XT).
title: Erstellen von Erlebnissen in einer [!UICONTROL Erlebnis-Targeting] Aktivität?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 39%

---

# Erlebnis erstellen in [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten

Die [!UICONTROL Visual Experience Composer] (VEC) [!DNL Adobe Target] bietet eine visuelle Benutzeroberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer [!UICONTROL Erlebnis-Targeting] (XT).

1. Wählen Sie die Elemente aus, die Sie ändern möchten, und nehmen Sie die gewünschten Änderungen vor.

   while [Erstellen einer [!UICONTROL Erlebnis-Targeting] activity](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), Schritt 1 des aus drei Teilen bestehenden geführten Workflows ([!UICONTROL Erlebnisse]) zeigt die Standardeinstellung an [!UICONTROL Erlebnis A] mit einer [!UICONTROL Alle Besucher] Zielgruppe.

   ![Zielgruppe „Alle Besucher“](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Alle Änderungen, die Sie jetzt vornehmen, gelten für [!UICONTROL Erlebnis A]. In einem Schritt unten klicken Sie auf **[!UICONTROL Hinzufügen von Erlebnis-Targeting]** , um zusätzliche Erlebnisse zu erstellen.

   Wenn Sie den Mauszeiger über die Elemente auf Ihrer Seite bewegen, werden die Elemente hervorgehoben. Alle hervorgehobenen Elemente können mit dem VEC geändert werden. Eine Liste der Aktionen, die für ein Element durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können JavaScript deaktivieren, um diese Elemente mithilfe des VEC zu ändern.

1. Wenn Sie zusätzliche Erlebnisse erstellen möchten, klicken Sie auf **[!UICONTROL Erlebnis-Targeting hinzufügen]**.

   ![Link „Erlebnis-Targeting hinzufügen“](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Die [!UICONTROL Zielgruppe hinzufügen] angezeigt. Um ein Erlebnis auf eine Zielgruppe auszurichten, wählen Sie die Zielgruppe aus, bevor Sie das Erlebnis hinzufügen.

   Die Zielgruppenbibliothek enthält Zielgruppen, die bereits definiert wurden, einschließlich einiger häufiger Zielgruppen, die als Teil von [!DNL Target] vorgefertigt sind. Sie können eine Zielgruppe aus der Bibliothek auswählen oder [eine neue Zielgruppe erstellen](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Beim Erstellen einer Zielgruppe können Sie einen Ort auswählen und Parameter für diesen Ort angeben. under [!UICONTROL Benutzerdefiniert] ([!UICONTROL Zielgruppe erstellen] > [!UICONTROL Benutzerdefiniert]), wählen Sie den Ort aus und geben Sie dann die gewünschten Parameter an.

   >[!NOTE]
   >
   >Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als zehn Minuten sind.

1. Wählen Sie mindestens eine Zielgruppe für das Targeting aus und klicken Sie auf **[!UICONTROL Fertig]**.

   ![Erlebnis B](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Erlebnis B wird jetzt in der obigen Abbildung angezeigt und richtet sich an die Zielgruppe der US-Besucher.

1. Wählen Sie die Elemente aus, die Sie für dieses Erlebnis ändern möchten, und nehmen Sie die gewünschten Änderungen vor, wie oben in Schritt 1 erläutert.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf zusätzliche Target-Erlebnisse zu erstellen.

1. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie mit der Erstellung Ihrer Erlebnisse fertig sind.

   Das Aktivitätsdiagramm wird angezeigt:

   ![XT-Targeting-Diagramm](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Sie können ein Bild aus einer anderen Quelle als der Hauptseite bereitstellen (z. B. ein Bild, das auf gehostet wird) `akamai.net` und bereitgestellt auf `adobe.com`). An anderer Stelle gehostete Bilder werden nicht in der Miniaturansicht der Seite angezeigt, die im Flussdiagramm angezeigt wird.

1. (Bedingt) Drag-and-Drop von Zielgruppen- und Erlebnispaaren beim Erstellen oder Bearbeiten [!UICONTROL Erlebnis-Targeting] Aktivitäten , um die Paare in der gewünschten Reihenfolge anzuordnen.

   Die Besucher werden der Reihe nach von oben nach unten für Erlebnisse bewertet.

   ![Erlebnisse verschieben](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Beim Erlebnis-Targeting kommt es auf die Reihenfolge an. ] Wenn ein Besucher in das erste Zielgruppen- und Erlebnispaar fällt, wird das erste Erlebnis bereitgestellt.

   Angenommen, Sie waren sich nicht bewusst, dass die Reihenfolge beim Erstellen einer [!UICONTROL Erlebnis-Targeting] -Aktivität. Später im Verlauf des Tests stellen Sie fest, dass sich Besucher, die sich Ihrer Meinung nach eigentlich für Erlebnis B oder C qualifizieren müssten, stattdessen für Erlebnis A qualifizieren. Eine Ursache dafür könnte sein, dass sich die Zielgruppen nicht gegenseitig ausschließen und sich nicht in der richtigen Reihenfolge befinden (z. B. Erlebnis A = USA, Erlebnis B = San Francisco und Erlebnis C = Kalifornien). In diesem Szenario qualifizieren sich alle Benutzer aus den USA für Erlebnis A, auch wenn sie sich in San Francisco oder anderswo in Kalifornien befinden. Sie können die Zielgruppen- und Erlebnispaare von der restriktivsten zur am wenigsten restriktiven (San Francisco > Kalifornien > USA) neu anordnen, ohne die gesamte Aktivität neu zu erstellen.

   Wenn Ihre Zielgruppe [!UICONTROL Alle Besucher] lautet, stellen Sie sicher, dass es sich nicht um die erste Zielgruppe im Diagramm handelt. Ein Erlebnis, für das &quot;[!UICONTROL Alle Besucher]&quot; kann als das letzte Erlebnis im [!UICONTROL Erlebnis-Targeting] -Aktivität, um alle Besucher zu &quot;erfassen&quot;, die nicht in ein anderes Erlebnis gefallen sind.

## Umbenennen oder Bearbeiten eines Erlebnisses

Sie können auf die [!UICONTROL Bearbeiten] Symbol (die vertikale Ellipse) für ein Erlebnis in einem [!UICONTROL Erlebnis-Targeting] und wählen Sie bei Bedarf aus den folgenden Optionen aus:

* [!UICONTROL Umbenennen]
* [!UICONTROL Bearbeiten ]

![Umbenennen und Bearbeiten von Optionen](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Löschen eines Erlebnisses

Im **[!UICONTROL Erlebnisse]** (der erste Schritt im dreistufigen geführten Workflow), klicken Sie auf die vertikale Ellipse > **[!UICONTROL Löschen]**.

![Erlebnis löschen](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplizieren eines Erlebnisses

Sie können ein Erlebnis in eine [!UICONTROL Erlebnis-Targeting] -Aktivität, damit Sie kleinere Änderungen vornehmen können, ohne das gesamte Erlebnis neu erstellen zu müssen.

Im **[!UICONTROL Erlebnisse]** (der erste Schritt im dreistufigen geführten Workflow), klicken Sie auf die vertikale Ellipse > **[!UICONTROL Duplizieren]**.

![Erlebnis duplizieren](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Vom A/B-Test bis [!UICONTROL Erlebnis-Targeting]

In diesem Video wird beschrieben, wie Sie A/B-Tests mit [!UICONTROL Erlebnis-Targeting] (XT).

* Beschreiben Sie den dreistufigen geführten Workflow zum Konfigurieren eines [!UICONTROL Erlebnis-Targeting] activity
* Beschreiben Sie, wie Sie standortspezifische Inhalte für Zielgruppen in verschiedenen geografischen Bereichen bereitstellen.
* Neusortierung von Erlebnissen, um zu gewährleisten, dass der richtige Inhalt der richtigen Zielgruppe bereitgestellt wird

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Aktivitätstypen (9:03)

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Erlebnis-Targeting wird um 5:15 erläutert.]

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Verwenden der [!UICONTROL Visual Experience Composer]

In diesem Video erhalten Sie Informationen zur Verwendung der [!UICONTROL Erlebnis-Targeting] (VEC).

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)
