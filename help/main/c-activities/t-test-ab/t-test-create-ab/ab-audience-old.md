---
keywords: Zielgruppe;Zielgruppe auswählen;Zielgruppe wählen;Auswahl
description: Die Zielgruppe bestimmt, welche Site-Besuchenden in Ihre Adobe-Aktivität  [!DNL Target]  werden.
title: Wie wähle ich eine Zielgruppe in einer A/ [!DNL Target] -Aktivität aus?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 62%

---

# Zielgruppenauswahl

Die Zielgruppe bestimmt, welche Site-Besucher in Ihre [!DNL Adobe Target]-Aktivität eingegeben werden.

>[!NOTE]
>
>Zusätzlich zur Auswahl einer bestehenden Zielgruppe können Sie verschiedene Zielgruppen miteinander kombinieren, um anstelle neuer Zielgruppen eine Ad-hoc-Zielgruppe zu erstellen. Weitere Informationen finden Sie unter [Mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klicken Sie im [!UICONTROL Audience] auf das Symbol **[!UICONTROL Edit]** (das vertikale Auslassungszeichen) und dann auf **[!UICONTROL Replace Audience]**.

   ![Option „Zielgruppe ersetzen“](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/replace-audience.png)

   Standardeinstellung ist, dass alle Besucher Ihrer Zielgruppe angehören. Sie können die Zielgruppe jedoch anpassen. Zielgruppen werden aus der Zielgruppenbibliothek ausgewählt. Alternativ können Sie eine Zielgruppe „Nur Aktivität“ erstellen. Die Zielgruppenbibliothek enthält Zielgruppen, die zuvor definiert wurden, einschließlich einiger allgemeiner Zielgruppen, die als Teil von [!DNL Target] vorkonfiguriert sind.

1. Wählen oder erstellen Sie die gewünschte Zielgruppe:

   * Eine Zielgruppe aus der Bibliothek auswählen
   * [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)
   * [Neue Zielgruppe erstellen](/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1)
   * [Erstellen einer Zielgruppe „Nur Aktivität“](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

   Wählen Sie für einen A/B-Test ohne spezielle Zielgruppen-Zielgruppe den Standardwert [!UICONTROL All Visitors].

   Sie können eine Zielgruppe auch bearbeiten oder kopieren, indem Sie den Mauszeiger über die gewünschte Zielgruppe im Dialogfeld [!UICONTROL Add Audience] bewegen, wie unten dargestellt.

   Das Kopieren einer Zielgruppe ist hilfreich, wenn Sie für eine vorhandene Zielgruppe eine ähnliche Zielgruppe erstellen möchten. Sie können eine Kopie der Zielgruppe erstellen, Bearbeitungen vornehmen und sie dann als neue Zielgruppe speichern. Diese Mauszeigerfunktionalität existiert auch in anderen Aktivitätstypen.

   ![Symbol für Zielgruppe](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audience_picker_hover-new.png)

   Wenn Sie eine Zielgruppe erstellen, können Sie einen Standort (mbox) auswählen und Parameter für ihn festlegen. Wählen Sie unter [!UICONTROL Custom Parameters] die Mbox aus und geben Sie dann die gewünschten Parameter an.

   >[!NOTE]
   >
   >Zielgruppen werden automatisch im Hintergrund importiert, wenn Sie die Zielgruppenliste öffnen und die importierten Zielgruppen älter als 10 Minuten sind.

1. (Bedingt) Geben Sie den Prozentsatz der qualifizierten Besucher an, die in die Aktivität aufgenommen werden sollen.

   So können Sie zum Beispiel festlegen, dass 50 % aller Besucher berücksichtigt werden sollen.

   ![Prozentsatz für Zielgruppen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Sie können Target auch &quot;[ Traffic automatisch zuweisen“ ](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Verwenden von Zielgruppen in Adobe Target (6:21) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video wird erläutert, wie sich Zielgruppen in [!DNL Target Standard/Premium] einsetzen lassen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/29395?captions=ger)

### Aktivitäts-Workflow - Targeting (2:14) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video sind Informationen zur Einrichtung von Zielgruppen enthalten.

* Zuweisen einer Zielgruppe zur Aktivität
* Regulieren von Traffic nach oben oder unten
* Auswählen der Zuordnungsmethode für den Traffic
* Zuweisen von Traffic zu verschiedenen Erlebnissen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

Detaillierte Informationen finden Sie unter [Zielgruppen](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).
