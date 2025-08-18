---
keywords: Zeitraum; Startdatum; Enddatum; Start-/Enddatum; Zeitrahmen; Zielzeitplan; Wochenaufteilung; Tagesaufteilung; Aufteilung
description: Erfahren Sie, wie Sie mit Start- und Enddaten und -zeiten Benutzerinnen und Benutzer ansprechen können, die Ihre Site während eines bestimmten Zeitraums besuchen.
title: Kann ich Besucherinnen und Besucher ansprechen, die meine Website zu bestimmten Zeiten besuchen?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
source-git-commit: 0e4698935b90cc0236abe6a47a6183c7fd2a7b20
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 25%

---

# [!UICONTROL Time Frame]

Sie können Start- und Enddatum sowie -zeiten [!DNL Adobe Target] hinzufügen, um Benutzerinnen und Benutzer anzusprechen, die Ihre Site während eines bestimmten Zeitraums besuchen. Sie können außerdem Optionen für die Wochen- und Tagesaufteilung festlegen, um wiederkehrende Muster für das Zielgruppen-Targeting zu erstellen.

Beispielsweise können Sie mit der [kombinierten Ad-hoc-Zielgruppenfunktion](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) Low-Spender mit bestimmten Inhalten in den drei Tagen vor dem Black Friday und anderen Inhalten nach dem Black Friday ansprechen.

1. Klicken Sie in der [!DNL Target] auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Time Frame]** per Drag-and-Drop in den Bereich Audience Builder .

   ![target_timeframe_dialog Bild](assets/target_timeframe_dialog.png)

1. Geben Sie die [!UICONTROL Start] und [!UICONTROL End] Daten und Uhrzeiten für die Zielgruppe an.

   Lassen Sie das Startdatum frei, um das Targeting in Einklang mit dem Zeitplan der Aktivität zu beginnen. Lassen Sie das Enddatum frei, um so lange weiter Targeting zu betreiben, bis Enddatum und -zeit der Aktivität erreicht sind.

   Sie können das Start- oder Enddatum auch leer lassen. Mit dieser Funktion können Sie dieselbe Zielgruppe in mehreren Aktivitäten verwenden (ohne eine Kopie der Zielgruppe zu erstellen), während Sie das Start- und Enddatum auf der Aktivitätsebene steuern.

   >[!NOTE]
   >
   >Beachten Sie Folgendes:
   >
   >* Die Zeitzone für das Start-/Enddatum wird als GMT +/- NN:NN angezeigt, wobei NN:NN der Versatz zum GMT ist und die Zeitzone auf Kontoebene und nicht die Zeitzone des Besuchers widerspiegelt. Beispielsweise würde die Zeitzone Kaliforniens als GMT -08:00 angezeigt.
   >
   >* [!DNL Target]-Zielgruppen berücksichtigen keine Änderungen der Sommerzeit (Daylight Saving Time, DST). Zielgruppen müssen manuell neu gespeichert werden, um DST-Änderungen zu berücksichtigen.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Set frequency]** , um wiederkehrende Muster festzulegen, einschließlich der Wochentage und Uhrzeiten.

   ![Wochen- und Tagesaufteilung](assets/week_and_day_parting.png)

   Sie können [!UICONTROL Frequency] Optionen verwenden, um beispielsweise eine Option „Jetzt chatten“ nur während der Tage und Stunden anzuzeigen, an denen Ihr Callcenter besetzt ist.

   Wählen Sie einen oder mehrere Wochentage aus und legen Sie dann die Start- und Endzeiten fest. Klicken Sie auf **[!UICONTROL Add frequency]** , um nach Bedarf weitere Muster anzugeben.

   >[!NOTE]
   >
   >Die Zeitzone für [!UICONTROL Week and Day Parting] wird als GMT +/- NN:NN angezeigt, wobei NN:NN der Versatz zum GMT ist und die Zeitzone auf Kontoebene und nicht die Zeitzone des Besuchers widerspiegelt. Beispielsweise würde die Zeitzone Kaliforniens für Pacific Daylight Time als GMT -07:00 angezeigt.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.

   Sie können Schritt 5 für jede Regel wiederholen, falls gewünscht.

1. Klicken Sie auf **[!UICONTROL Done]**.

## Schulungsvideo: Erstellen von Zielgruppen ![Übersichts-Badge](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
