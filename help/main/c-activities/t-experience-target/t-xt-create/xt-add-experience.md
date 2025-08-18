---
keywords: Erlebnis erstellen;Erlebniserstellung;Priorität;Zielgruppe;Erlebnis;Visual Experience Composer
description: Erfahren Sie, wie Sie mit dem  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer]VEC) Erlebnisse auf Ihrer Seite in einer [!UICONTROL Experience Targeting] (XT)-Aktivität erstellen und bearbeiten können.
title: Wie erstelle ich Erlebnisse in einer [!UICONTROL Experience Targeting] Aktivität?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 23%

---

# Erstellen von Erlebnissen in [!UICONTROL Experience Targeting] (XT)-Aktivitäten

Der [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] bietet eine visuelle Benutzeroberfläche zum Bearbeiten der Erlebnisse auf Ihrer Seite in einer [!UICONTROL Experience Targeting] (XT)-Aktivität.

1. Wählen Sie die zu ändernden Elemente aus und nehmen Sie die gewünschten Änderungen vor.

   Beim [Erstellen einer [!UICONTROL Experience Targeting] Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) zeigt Schritt 1 des dreiteiligen geführten Workflows ([!UICONTROL Experiences]) die [!UICONTROL Experience A] mit einer [!UICONTROL All Visitors] Zielgruppe an.

   ![Zielgruppe „Alle Besucher“](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors-new.png)

   Alle Änderungen, die Sie jetzt vornehmen, gelten für [!UICONTROL Experience A]. In einem Schritt unten klicken Sie auf **[!UICONTROL Add Experience Targeting]** , um zusätzliche Erlebnisse zu erstellen.

   Wenn Sie den Mauszeiger über die Elemente auf der Seite bewegen, werden die Elemente hervorgehoben. Alle hervorgehobenen Elemente können mit dem VEC geändert werden. Eine Liste der Aktionen, die für ein Element durchgeführt werden können, um das Erlebnis zu ändern, finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Standardmäßig gestattet der VEC das Ändern von Elementen mit JavaScript nicht (zum Beispiel sich drehende Banner). Sie können JavaScript deaktivieren, um diese Elemente mithilfe des VEC zu ändern.

1. Um weitere Erlebnisse zu erstellen, klicken Sie auf **[!UICONTROL Add]** ( ![Schaltfläche hinzufügen](/help/main/assets/icons/Add.svg) ).

   Das Dialogfeld [!UICONTROL Add Audience] wird angezeigt. Um ein Erlebnis für eine Audience auszuwählen, wählen Sie die Audience aus, bevor Sie das Erlebnis hinzufügen.

   Die Zielgruppenbibliothek enthält Zielgruppen, die bereits definiert wurden, einschließlich einiger häufiger Zielgruppen, die als Teil von [!DNL Target] vorgefertigt sind. Sie können eine Zielgruppe aus der Bibliothek auswählen oder [eine neue Zielgruppe erstellen](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie auch mehrere Zielgruppen kombinieren, um nach Bedarf kombinierte Zielgruppen zu erstellen, anstatt eine neue Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Beim Erstellen einer Zielgruppe können Sie einen Speicherort auswählen und Parameter für diesen Speicherort angeben. Wählen Sie unter [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom]) den Speicherort aus und geben Sie dann die gewünschten Parameter an.

   >[!NOTE]
   >
   >Audiences werden automatisch im Hintergrund importiert, wenn Sie die Audience-Liste öffnen. Die importierten Audiences sind älter als zehn Minuten.

1. Wählen Sie eine oder mehrere Zielgruppen aus, die Sie in das Erlebnis aufnehmen möchten, und klicken Sie dann auf **[!UICONTROL Assign Audience]**.

   Erlebnis B wird jetzt in der vorherigen Abbildung angezeigt und dieses Erlebnis ist auf die entsprechende Zielgruppe ausgerichtet.

1. Wählen Sie die Elemente aus, die Sie für dieses Erlebnis ändern möchten, und nehmen Sie die gewünschten Änderungen vor, wie in Schritt 1 oben beschrieben.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf zusätzliche Target-Erlebnisse zu erstellen.

1. Klicken Sie auf **[!UICONTROL Next]** , wenn Sie mit dem Entwerfen Ihrer Erlebnisse fertig sind.

   Das Aktivitätsdiagramm wird angezeigt:

   ![XT-Targeting-Diagramm](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-refresh.png)

   >[!NOTE]
   >
   >Sie können ein Bild aus einer anderen Quelle als der Hauptseite bereitstellen (z. B. ein auf `akamai.net` gehostetes und auf `adobe.com` bereitgestelltes Bild). An anderer Stelle gehostete Bilder werden nicht in der Miniaturansicht der Seite angezeigt, die im Flussdiagramm angezeigt wird.

1. (Bedingt) Ziehen Sie Zielgruppen- und Erlebnispaare per Drag-and-Drop, während Sie [!UICONTROL Experience Targeting] Aktivitäten erstellen oder bearbeiten, um die Paare in der gewünschten Reihenfolge anzuordnen.

   Klicken Sie auf das Symbol „Neu anordnen![ ( ](/help/main/assets/icons/Reorder.svg)Neu anordnen), um die [!UICONTROL Experiences] Spalte auf der rechten Seite anzuzeigen, und ordnen Sie dann die Erlebnisse wie gewünscht neu an.

   Die Besucher werden der Reihe nach von oben nach unten für Erlebnisse bewertet.

   [!UICONTROL Experience Targeting] geht davon aus, dass Ordnung wichtig ist. Wenn ein Besucher in das erste Zielgruppen- und Erlebnispaar fällt, wird das erste Erlebnis bereitgestellt.

   Angenommen, Ihnen war nicht bewusst, dass beim Erstellen einer [!UICONTROL Experience Targeting]-Aktivität die Reihenfolge wichtig ist. Später stellen Sie während des Tests fest, dass Besucher, die Ihrer Meinung nach sich für Erlebnis B oder C qualifizieren sollten, sich stattdessen für Erlebnis A qualifizieren. Dies könnte daran liegen, dass sich die Zielgruppen nicht gegenseitig ausschließen und nicht in der richtigen Reihenfolge sind (z. B. Erlebnis A = Vereinigte Staaten, Erlebnis B = San Francisco und Erlebnis C = Kalifornien). In diesem Szenario können alle Benutzer aus den USA die Kriterien für Erlebnis A erfüllen, auch wenn sie sich in San Francisco oder anderswo in Kalifornien befinden. Sie können die Audience-Erlebnis-Paare von der restriktivsten zur am wenigsten restriktiven (San Francisco > Kalifornien > USA) neu anordnen, ohne die gesamte Aktivität neu zu erstellen.

   Wenn Sie eine [!UICONTROL All Visitors] Zielgruppe haben, stellen Sie sicher, dass dies nicht die erste Zielgruppe im Diagramm ist. Ein Erlebnis, das auf &quot;[!UICONTROL All Visitors]&quot; ausgerichtet ist, kann als letztes Erlebnis in der [!UICONTROL Experience Targeting]-Aktivität verwendet werden, um alle Besucher zu „fangen“, die nicht in ein anderes Erlebnis gefallen sind.

## Umbenennen, Bearbeiten, Duplizieren oder Löschen eines Erlebnisses

Klicken Sie auf ein Erlebnis im Diagramm in einer [!UICONTROL Experience Targeting] Aktivität, um die Spalte [!UICONTROL Experiences] auf der rechten Seite anzuzeigen.

![Umbenennen und Bearbeiten von Optionen](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-refresh.png)

Wählen Sie nach Bedarf aus den folgenden Optionen:

* **[!UICONTROL Rename]**: Geben Sie den gewünschten Namen in das Feld [!UICONTROL Name] ein.
* **[!UICONTROL Edit]**: Klicken Sie auf das Symbol Bearbeiten ![Bearbeiten](/help/main/assets/icons/Edit.svg) ) und nehmen Sie dann die gewünschten Änderungen vor.
* **[!UICONTROL Duplicate]**: Kopieren Sie ein Erlebnis in einer [!UICONTROL Experience Targeting] Aktivität, um kleinere Änderungen daran vorzunehmen, ohne das gesamte Erlebnis neu erstellen zu müssen. Klicken Sie auf das [!UICONTROL Duplicate]-Symbol ![Duplikatsymbol](/help/main/assets/icons/Duplicate.svg) ) und bearbeiten Sie dann das Erlebnis nach Bedarf.
* **[!UICONTROL Delete]**: Klicken Sie auf das [!UICONTROL Delete] (![Löschsymbol](/help/main/assets/icons/Delete.svg) ) und bestätigen Sie dann den Löschvorgang.

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Von A/B-Tests zu [!UICONTROL Experience Targeting]

In diesem Video wird beschrieben, wie Sie A/B-Tests mit [!UICONTROL Experience Targeting] (XT) auf die nächste Stufe bringen.

* Beschreibung des dreistufigen Workflows zum Konfigurieren einer [!UICONTROL Experience Targeting] Aktivität
* Beschreiben Sie, wie Sie standortspezifische Inhalte für Zielgruppen in verschiedenen geografischen Bereichen bereitstellen
* Neusortierung von Erlebnissen, um zu gewährleisten, dass der richtige Inhalt der richtigen Zielgruppe bereitgestellt wird

>[!VIDEO](https://video.tv.adobe.com/v/38302?captions=ger)

### Aktivitätstypen (9:03)

In diesem Video werden die in [!DNL Target] verfügbaren Aktivitätstypen erläutert. [!UICONTROL Experience Targeting] wird ab 5 Uhr :15.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/29397?captions=ger)

### Verwenden der [!UICONTROL Visual Experience Composer]

In diesem Video finden Sie Informationen zur Verwendung der [!UICONTROL Experience Targeting] (VEC)-Optionen.

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/29396?captions=ger)
