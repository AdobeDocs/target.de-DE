---
keywords: Zeitraum; Startdatum; Enddatum; Start-/Enddatum; Zeitrahmen; Zielzeitplan; Wochenaufteilung; Tagesaufteilung; Aufteilung
description: Erfahren Sie, wie Sie mit Start- und Enddaten und -zeiten Benutzer auswählen können, die Ihre Site während eines bestimmten Zeitraums besuchen.
title: Kann ich Besucher ansprechen, die meine Site zu bestimmten Zeiten besuchen?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
source-git-commit: 0e4698935b90cc0236abe6a47a6183c7fd2a7b20
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 35%

---

# [!UICONTROL Time Frame]

Sie können Start- und Enddaten und -zeiten in [!DNL Adobe Target] hinzufügen, um Benutzer anzusprechen, die Ihre Site während eines bestimmten Zeitraums besuchen. Sie können außerdem Optionen für die Wochen- und Tagesaufteilung festlegen, um wiederkehrende Muster für das Zielgruppen-Targeting zu erstellen.

Beispielsweise können Sie mit der Funktion [kombinierte Ad-hoc-Zielgruppen](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) wenig verbrauchte Personen in den drei Tagen vor Black Friday mit bestimmten Inhalten ansprechen und nach Black Friday andere Inhalte anzeigen.

1. Klicken Sie in der [!DNL Target] -Oberfläche auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Time Frame]** in den Bereich Audience Builder .

   ![target_timeframe_dialog image](assets/target_timeframe_dialog.png)

1. Geben Sie Datum und Uhrzeit für [!UICONTROL Start] und [!UICONTROL End] für die Zielgruppe an.

   Lassen Sie das Startdatum frei, um das Targeting in Einklang mit dem Zeitplan der Aktivität zu beginnen. Lassen Sie das Enddatum frei, um so lange weiter Targeting zu betreiben, bis Enddatum und -zeit der Aktivität erreicht sind.

   Sie können das Start- oder Enddatum auch leer lassen. Mit dieser Funktion können Sie dieselbe Zielgruppe in mehreren Aktivitäten verwenden (ohne eine Kopie der Zielgruppe zu erstellen) und gleichzeitig das Start- und Enddatum auf Aktivitätsebene steuern.

   >[!NOTE]
   >
   >Beachten Sie Folgendes:
   >
   >* Die Zeitzone für Start-/Enddatum wird als GMT +/- NN:NN angezeigt, wobei NN: NN den Offset von GMT darstellt und die Zeitzone auf Benutzerkontoebene und nicht die Zeitzone des Besuchers widerspiegelt. Die Zeitzone von Kalifornien wird z. B. als GMT -08:00 angezeigt.
   >
   >* [!DNL Target] Zeitzielgruppen berücksichtigen keine Änderungen der Sommerzeit (Daylight Saving Time, DST). Sie müssen Zielgruppen manuell neu speichern, um DST-Änderungen zu berücksichtigen.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Set frequency]** , um wiederkehrende Muster festzulegen, einschließlich Wochentage und Uhrzeiten.

   ![Wochen- und Tagesaufteilung](assets/week_and_day_parting.png)

   Sie können beispielsweise [!UICONTROL Frequency] -Optionen verwenden, um Besuchern nur während der Tage und Stunden, an denen Ihr Callcenter besetzt ist, die Option &quot;Jetzt chatten&quot;anzuzeigen.

   Wählen Sie einen oder mehrere Wochentage aus und legen Sie dann die Start- und Endzeiten fest. Klicken Sie auf **[!UICONTROL Add frequency]** , um nach Bedarf weitere Muster anzugeben.

   >[!NOTE]
   >
   >Die Zeitzone für [!UICONTROL Week and Day Parting] wird als GMT +/- NN:NN angezeigt, wobei NN:NN der Offset von GMT ist und die Zeitzone auf Kontoebene und nicht die Zeitzone des Besuchers widerspiegelt. Die Zeitzone von Kalifornien für die Pacific Daylight Time würde beispielsweise als GMT -07:00 angezeigt.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.

   Sie können Schritt 5 für jede Regel wiederholen, falls gewünscht.

1. Klicken Sie auf **[!UICONTROL Done]**.

## Schulungsvideo: Erstellen von Zielgruppen ![Badge &quot;Überblick&quot;](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
