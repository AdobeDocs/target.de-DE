---
keywords: Erlebnis erstellen;Erlebniserstellung;Priorität;Zielgruppe;Erlebnis;Visual Experience Composer
description: Erfahren Sie, wie Sie mit dem VEC (0) Erlebnisse auf Ihrer Seite in einer [!UICONTROL Experience Targeting] -Aktivität (XT) erstellen und bearbeiten können. [!DNL Adobe Target] [!UICONTROL Visual Experience Composer]
title: Wie erstelle ich Erlebnisse in einer [!UICONTROL Experience Targeting] -Aktivität?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 36%

---

# Erlebnis in [!UICONTROL Experience Targeting] (XT)-Aktivitäten erstellen

Der [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] bietet eine visuelle Benutzeroberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer [!UICONTROL Experience Targeting] (XT)-Aktivität.

1. Wählen Sie die Elemente aus, die Sie ändern möchten, und nehmen Sie die gewünschten Änderungen vor.

   Beim [ Erstellen einer [!UICONTROL Experience Targeting] -Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) wird in Schritt 1 des dreiteiligen geführten Workflows ([!UICONTROL Experiences]) der Standardwert [!UICONTROL Experience A] mit einer [!UICONTROL All Visitors] -Zielgruppe angezeigt.

   ![Zielgruppe „Alle Besucher“](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Alle Änderungen, die Sie vornehmen, gelten nun für [!UICONTROL Experience A]. Klicken Sie in einem Schritt weiter unten auf **[!UICONTROL Add Experience Targeting]** , um weitere Erlebnisse zu erstellen.

   Wenn Sie den Mauszeiger über die Elemente auf Ihrer Seite bewegen, werden die Elemente hervorgehoben. Alle hervorgehobenen Elemente können mit dem VEC geändert werden. Eine Liste der Aktionen, die für ein Element durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können JavaScript deaktivieren, um diese Elemente mithilfe des VEC zu ändern.

1. Um weitere Erlebnisse zu erstellen, klicken Sie auf **[!UICONTROL Add Experience Targeting]**.

   ![Link „Erlebnis-Targeting hinzufügen“](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Das Dialogfeld [!UICONTROL Add Audience] wird angezeigt. Um ein Erlebnis auf eine Zielgruppe auszurichten, wählen Sie die Zielgruppe aus, bevor Sie das Erlebnis hinzufügen.

   Die Zielgruppenbibliothek enthält Zielgruppen, die bereits definiert wurden, einschließlich einiger häufiger Zielgruppen, die als Teil von [!DNL Target] vorgefertigt sind. Sie können eine Zielgruppe aus der Bibliothek auswählen oder [eine neue Zielgruppe erstellen](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Beim Erstellen einer Zielgruppe können Sie einen Ort auswählen und Parameter für diesen Ort angeben. Wählen Sie unter [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom]) den Standort aus und geben Sie dann die gewünschten Parameter an.

   >[!NOTE]
   >
   >Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als zehn Minuten sind.

1. Wählen Sie mindestens eine Zielgruppe für das Targeting mit dem Erlebnis aus und klicken Sie dann auf **[!UICONTROL Done]**.

   ![Erlebnis B](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   Erlebnis B wird jetzt in der obigen Abbildung angezeigt und richtet sich an die Zielgruppe der US-Besucher.

1. Wählen Sie die Elemente aus, die Sie für dieses Erlebnis ändern möchten, und nehmen Sie die gewünschten Änderungen vor, wie oben in Schritt 1 erläutert.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf zusätzliche Target-Erlebnisse zu erstellen.

1. Klicken Sie auf **[!UICONTROL Next]** , wenn Sie mit dem Entwurf Ihrer Erlebnisse fertig sind.

   Das Aktivitätsdiagramm wird angezeigt:

   ![XT-Targeting-Diagramm](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Sie können ein Bild aus einer anderen Quelle als der Hauptseite bereitstellen (z. B. ein Bild, das auf `akamai.net` gehostet und auf `adobe.com` bereitgestellt wird). An anderer Stelle gehostete Bilder werden nicht in der Miniaturansicht der Seite angezeigt, die im Flussdiagramm angezeigt wird.

1. (Bedingt) Ziehen Sie Zielgruppen- und Erlebnispaare per Drag-and-Drop beim Erstellen oder Bearbeiten von [!UICONTROL Experience Targeting] -Aktivitäten, um die Paare in der gewünschten Reihenfolge anzuordnen.

   Die Besucher werden der Reihe nach von oben nach unten für Erlebnisse bewertet.

   ![Erlebnisse verschieben](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Experience Targeting] geht davon aus, dass die Reihenfolge wichtig ist. Wenn ein Besucher in das erste Zielgruppen- und Erlebnispaar fällt, wird das erste Erlebnis bereitgestellt.

   Angenommen, Sie waren sich nicht bewusst, dass die Reihenfolge beim Erstellen einer [!UICONTROL Experience Targeting] -Aktivität wichtig ist. Später im Verlauf des Tests stellen Sie fest, dass sich Besucher, die sich Ihrer Meinung nach eigentlich für Erlebnis B oder C qualifizieren müssten, stattdessen für Erlebnis A qualifizieren. Eine Ursache dafür könnte sein, dass sich die Zielgruppen nicht gegenseitig ausschließen und sich nicht in der richtigen Reihenfolge befinden (z. B. Erlebnis A = USA, Erlebnis B = San Francisco und Erlebnis C = Kalifornien). In diesem Szenario qualifizieren sich alle Benutzer aus den USA für Erlebnis A, auch wenn sie sich in San Francisco oder anderswo in Kalifornien befinden. Sie können die Zielgruppen- und Erlebnispaare von der restriktivsten zur am wenigsten restriktiven (San Francisco > Kalifornien > USA) neu anordnen, ohne die gesamte Aktivität neu zu erstellen.

   Wenn Sie eine [!UICONTROL All Visitors] -Zielgruppe haben, stellen Sie sicher, dass es sich nicht um die erste Zielgruppe im Diagramm handelt. Ein Erlebnis, das auf &quot;[!UICONTROL All Visitors]&quot;abzielt, kann als das letzte Erlebnis in der [!UICONTROL Experience Targeting] -Aktivität verwendet werden, um alle Besucher zu erfassen, die nicht in ein anderes Erlebnis gefallen sind.

## Umbenennen oder Bearbeiten eines Erlebnisses

Sie können in einem Erlebnis in einer [!UICONTROL Experience Targeting] -Aktivität auf das Symbol [!UICONTROL Edit] (die vertikale Ellipse) klicken und aus den folgenden Optionen auswählen:

* [!UICONTROL Rename]
* [!UICONTROL Edit]

![Umbenennen und Bearbeiten von Optionen](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Löschen eines Erlebnisses

Klicken Sie auf der Seite &quot;**[!UICONTROL Experiences]**&quot;(der erste Schritt im dreistufigen geleiteten Workflow) auf die vertikale Ellipse > **[!UICONTROL Delete]**.

![Erlebnis löschen](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Duplizieren eines Erlebnisses

Sie können ein Erlebnis aus einer [!UICONTROL Experience Targeting] -Aktivität kopieren, um kleinere Änderungen vorzunehmen, ohne das gesamte Erlebnis neu erstellen zu müssen.

Klicken Sie auf der Seite &quot;**[!UICONTROL Experiences]**&quot;(der erste Schritt im dreistufigen geleiteten Workflow) auf die vertikale Ellipse > **[!UICONTROL Duplicate]**.

![Erlebnis duplizieren](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Von A/B-Tests bis [!UICONTROL Experience Targeting]

In diesem Video wird beschrieben, wie Sie A/B-Tests mit [!UICONTROL Experience Targeting] (XT) auf die nächste Ebene bringen.

* Beschreiben Sie den dreistufigen geführten Workflow zum Konfigurieren einer [!UICONTROL Experience Targeting] -Aktivität.
* Beschreiben Sie, wie Sie standortspezifische Inhalte für Zielgruppen in verschiedenen geografischen Bereichen bereitstellen.
* Neusortierung von Erlebnissen, um zu gewährleisten, dass der richtige Inhalt der richtigen Zielgruppe bereitgestellt wird

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Aktivitätstypen (9:03)

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Experience Targeting] wird ab 05:15 besprochen.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Verwenden des [!UICONTROL Visual Experience Composer]

In diesem Video erhalten Sie Informationen zur Verwendung der VEC-Optionen (0).[!UICONTROL Experience Targeting]

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)
