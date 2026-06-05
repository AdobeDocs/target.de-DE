---
keywords: Automated Personalization;Angebot;Reporting;Gruppe;Berichtsgruppe;Zuordnung
description: Erfahren Sie, wie Sie in  [!DNL Adobe Target] [!UICONTROL Automated Personalization]-Aktivitäten Berichtsgruppen für Angebote verwenden.
title: Kann ich Berichtsgruppen für Angebote in [!UICONTROL Automated Personalization]-Aktivitäten verwenden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 25%

---

# Berichtsgruppen für Angebote in [!UICONTROL Automated Personalization]

Informationen zur Verwendung von Berichtsgruppen in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP)-Aktivitäten.

Berichtsgruppen erfüllen zwei grundlegende Funktionen:

* Mit Berichtsgruppen können Sie Ihre Angebote in AP-Aktivitätsberichten gruppiert anzeigen.
* Berichtsgruppen spielen eine wichtige Rolle bei der Funktionsweise der [!DNL Target] Personalisierungsmodelle.

Wenn Sie Berichtsgruppen verwenden, erstellt [!DNL Target] für jede Berichtsgruppe ein Personalisierungsmodell, das die Daten aller Angebote in dieser Gruppe verwendet. Ohne Berichtsgruppen erstellt [!DNL Target] ein Personalisierungsmodell für jedes Angebot in Ihrer AP-Aktivität.

Wenn Ihre Aktivitätseinrichtung nicht über genügend Daten verfügt, um pro Angebot ein Personalisierungsmodell zu erstellen, helfen Berichtsgruppen, die Datenanforderungen für die Verwendung von [!UICONTROL Automated Personalization] zu reduzieren. Berichtsgruppen können auch das Problem des „Kaltstarts“ für neue Angebote beheben, indem ähnliche Angebote gruppiert werden, damit jedes Modell mit mehr Daten arbeiten kann. Modellierungsgruppen können auch für Aktivitäten verwendet werden, bei denen Ihrer AP-Aktivität regelmäßig neue Angebote hinzugefügt werden.

Dieser Ansatz funktioniert gut, wenn Besucher auf alle Angebote in einer Gruppe gleich reagieren. Best Practice ist es, Angebote zu gruppieren, auf die ähnliche Besuchergruppen auf ähnliche Weise reagieren. Anders ausgedrückt: Gruppieren Sie Angebote mit ähnlichen Konversionsraten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben. Das Gruppieren aller Angebote oder das Gruppieren von Angeboten mit unterschiedlichen Konversionsraten reduziert wahrscheinlich die Effektivität der [!DNL Target] Personalisierungsmodelle.

>[!NOTE]
>
>Wenn ein Angebot aus einer bestimmten Modellgruppe entfernt oder ersetzt wird, wird der historische Traffic mit diesem spezifischen Angebot auch aus der Modellgruppe gelöscht. Mit anderen Worten: Gelöschte Angebote tragen nicht dazu bei, welche Daten für das Lernen der [!DNL Target] Personalisierungsmodelle verwendet werden.

## Einrichten von Berichtsgruppen

1. Klicken Sie auf **[!UICONTROL Seite]** Erlebnisse“ einer AP-Aktivität auf das Symbol **[!UICONTROL Inhalt verwalten]**.

   ![Symbol „Inhalt verwalten“](/help/main/c-reports/assets/ap_manage_content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Angebote]** oben im Dialogfeld [!UICONTROL Inhalt verwalten].
1. (Optional) Fügen Sie bestimmte Erlebnisse zu einer Berichtsgruppe hinzu, indem Sie mit dem Mauszeiger über das gewünschte Angebot fahren und auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]** klicken.

   ![Symbol für Berichtsgruppe](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Bedingt) Schließen Sie Batch-Erlebnisse in eine Berichtsgruppe ein, indem Sie die Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]** in der oberen rechten Ecke des Dialogfelds klicken.

   ![Symbol für Berichtsgruppe](/help/main/c-reports/assets/ap_manage_content_3.png)

1. Um das ausgewählte Angebot zu einer bestehenden Berichtsgruppe hinzuzufügen, klicken Sie auf **[!UICONTROL Vorhanden]**, wählen Sie die gewünschte Berichtsgruppe aus der Dropdownliste aus und klicken Sie dann auf **[!UICONTROL Übernehmen]**.

   Oder

   Um eine Berichtsgruppe zu erstellen, der das ausgewählte Angebot zugewiesen werden soll, wählen Sie **[!UICONTROL Neu]**, benennen Sie die neue Berichtsgruppe und klicken Sie dann auf **[!UICONTROL Anwenden]**.

   ![Neues Symbol zum Erstellen einer neuen Berichtsgruppe](/help/main/c-reports/assets/ap_reporting_groups.png)

Sie können die Liste [!UICONTROL Standort] verwenden, um Angebote nach Standort zu filtern. Mit der Liste [!UICONTROL Berichtsgruppe] können Sie Angebote nach Berichtsgruppe filtern. Sie können die Liste [!UICONTROL Berichtsgruppe] auch verwenden, um [!UICONTROL nicht zugewiesenen Angeboten] zu filtern und so ein Angebot, dem bisher noch keine Berichtsgruppe zugewiesen wurde, einer beliebigen Gruppe zuzuweisen.

Weitere Informationen zur Zielgruppenbestimmung eines Angebots für bestimmte Zielgruppen finden Sie unter [Target [!UICONTROL Automated Personalization]-Angebote](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Einschränkungen

* Es ist wichtig zu verstehen, dass Berichtsgruppen Einfluss darauf haben, wie [!DNL Target] Modelle erstellt. Daher empfiehlt [!DNL Adobe], Berichtsgruppen nur zu verwenden, wenn Sie neue Angebote ersetzen oder hinzufügen möchten, während eine Aktivität live ist. Wenn ein neues Angebot in eine Live-Aktivität eingeführt wird, kann das Gerät, indem es das neue Angebot in eine Gruppe mit vorhandenen ähnlichen Angeboten einfügt, die bereits für die anderen Angebote in seiner Gruppe erfassten Daten verwenden, um mehr über das neue Angebot zu erfahren. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben.

* AP-Aktivitäten verfügen über Kombinationen aus Standort + Angebot (Modellvariablen). Wenn [!DNL Target] Daten in Berichten aufzeichnet, berücksichtigt [!DNL Target] solche Kombinationen, damit klar ist, aus welchem Ereignis (Anzeige, Klick usw.) das Angebot stammt.

  Eine Aktivität kann beispielsweise über mehrere Standorte und Angebote verfügen, die sich überschneiden können. Wenn ein Besucher mehr als eines dieser Angebote an verschiedenen Orten sieht, zeichnet [!DNL Target] nur Daten für diese Angebote auf. Wenn derselbe Besucher später auf ein Angebot klickt, zeichnet [!DNL Target] nur ein Ereignis aus dieser Kombination auf (nicht für alle Kombinationen).

  Wenn der Klick von einem anderen Ort stammt, der in einer Metrik vorhanden ist, aber kein Angebot anzeigt, wird dieses Ereignis ebenfalls unter der Aktivität protokolliert, jedoch nicht für eine Kombination aus Angebot und Standort. Daher wird dieses Angebot nicht in der Berichtsgruppe für Angebote angezeigt.

  Dies liegt daran, dass der Klick möglicherweise von einer anderen Mbox stammt als von der Mbox, die das Angebot bereitgestellt hat. Aus diesem Grund ist die Metrik mit der Aktivität verknüpft, aber nicht mit dem Angebot.

## Anzeigen von Angeboten in einer Berichtsgruppe

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, klicken Sie in der Liste auf die gewünschte [!UICONTROL Automated Personalization]-Aktivität und dann auf die Registerkarte **[!UICONTROL Berichte]**, um den Bericht [Angebotsebene](/help/main/c-reports/personalization-reports/reports-ap.md) anzuzeigen.

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol [!UICONTROL Filter anzeigen] (funnel) und aktivieren Sie dann das Kontrollkästchen [!UICONTROL Automated Personalization], um die Liste so zu filtern, dass nur [!UICONTROL Automated Personalization-] angezeigt werden.

1. Klicken Sie **[!UICONTROL der Tabelle auf]** Kontrolle **[!UICONTROL oder Targeting]**, um die nicht gruppierten Angebote und Angebote innerhalb von Berichtsgruppen anzuzeigen.

   ![Angebotsgruppen: Kontrolle und Zielgruppe](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Informationen zur Verwendung von [!UICONTROL Automated Personalization]-Berichten (einschließlich des Berichts [!UICONTROL Angebotsebene] finden Sie unter [Automated Personalization-Zusammenfassungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).


