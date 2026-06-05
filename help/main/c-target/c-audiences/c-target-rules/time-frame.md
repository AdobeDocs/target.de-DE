---
keywords: Zeitraum; Startdatum; Enddatum; Start-/Enddatum; Zeitrahmen; Zielzeitplan; Wochenaufteilung; Tagesaufteilung; Aufteilung
description: Erfahren Sie, wie Sie mit Start- und Enddaten und -zeiten Benutzerinnen und Benutzer ansprechen können, die Ihre Site während eines bestimmten Zeitraums besuchen.
title: Kann ich Besucherinnen und Besucher ansprechen, die meine Website zu bestimmten Zeiten besuchen?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
TQID: https://experienceleague.adobe.com/EilEXJtLuzmytW8OmhGbhOTfsVxx4WuTKfT6zgmFYdc
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 454
ht-degree: 24%

---

# [!UICONTROL Zeitrahmen]

Sie können Start- und Enddatum sowie -zeiten [!DNL Adobe Target] hinzufügen, um Benutzerinnen und Benutzer anzusprechen, die Ihre Site während eines bestimmten Zeitraums besuchen. Sie können außerdem Optionen für die Wochen- und Tagesaufteilung festlegen, um wiederkehrende Muster für das Zielgruppen-Targeting zu erstellen.

Beispielsweise können Sie mit der [kombinierten Ad-hoc-Zielgruppenfunktion](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) Low-Spender mit bestimmten Inhalten in den drei Tagen vor dem Black Friday und anderen Inhalten nach dem Black Friday ansprechen.

1. Klicken Sie in der [!DNL Target] auf **[!UICONTROL Zielgruppen]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie &quot;**[!UICONTROL &quot; per Drag-and]** Drop in den Audience Builder-Bereich.

   ![target_timeframe_dialog Bild](assets/target_timeframe_dialog.png)

1. Geben Sie die [!UICONTROL Start] und [!UICONTROL Ende] Datum und Uhrzeit für die Zielgruppe an.

   Lassen Sie das Startdatum frei, um das Targeting in Einklang mit dem Zeitplan der Aktivität zu beginnen. Lassen Sie das Enddatum frei, um so lange weiter Targeting zu betreiben, bis Enddatum und -zeit der Aktivität erreicht sind.

   Sie können das Start- oder Enddatum auch leer lassen. Mit dieser Funktion können Sie dieselbe Zielgruppe in mehreren Aktivitäten verwenden (ohne eine Kopie der Zielgruppe zu erstellen), während Sie das Start- und Enddatum auf der Aktivitätsebene steuern.

   >[!NOTE]
   >
   >Beachten Sie Folgendes:
   >
   >* Die Zeitzone für das Start-/Enddatum wird als GMT +/- NN:NN angezeigt, wobei NN:NN der Versatz zum GMT ist und die Zeitzone auf Kontoebene und nicht die Zeitzone des Besuchers widerspiegelt. Beispielsweise würde die Zeitzone Kaliforniens als GMT -08:00 angezeigt.
   >
   >* [!DNL Target]-Zielgruppen berücksichtigen keine Änderungen der Sommerzeit (Daylight Saving Time, DST). Zielgruppen müssen manuell neu gespeichert werden, um DST-Änderungen zu berücksichtigen.

1. (Bedingt) Klicken Sie auf **[!UICONTROL Häufigkeit festlegen]**, um wiederkehrende Muster festzulegen, einschließlich der Wochentage und Zeiten.

   ![Wochen- und Tagesaufteilung](assets/week_and_day_parting.png)

   Sie können [!UICONTROL Häufigkeit]-Optionen verwenden, um beispielsweise eine Option „Jetzt chatten“ nur während der Tage und Stunden anzuzeigen, an denen Ihr Callcenter besetzt ist.

   Wählen Sie einen oder mehrere Wochentage aus und legen Sie dann die Start- und Endzeiten fest. Klicken Sie **[!UICONTROL Häufigkeit hinzufügen]**, um nach Bedarf weitere Muster anzugeben.

   >[!NOTE]
   >
   >Die Zeitzone für [!UICONTROL Wochen- und &#x200B;]) wird als GMT +/- NN:NN angezeigt, wobei NN:NN der Versatz zum GMT ist und die Zeitzone auf Kontoebene und nicht die Zeitzone des Besuchers widerspiegelt. Beispielsweise würde die Zeitzone Kaliforniens für Pacific Daylight Time als GMT -07:00 angezeigt.

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.

   Sie können Schritt 5 für jede Regel wiederholen, falls gewünscht.

1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Schulungsvideo: Erstellen von Zielgruppen ![Übersichts-Badge](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
