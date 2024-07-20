---
keywords: automatisierte Personalisierung;Angebot;Berichterstellung;Gruppe;Berichtsgruppe;App
description: Erfahren Sie, wie Sie Angebotsberichtsgruppen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] -Aktivitäten verwenden.
title: Kann ich Berichtsgruppen für Angebote in [!UICONTROL Automated Personalization] -Aktivitäten verwenden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: b5f06878a6ca8b4c571bfe05a52bfb3f471a697e
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 15%

---

# Berichtsgruppen für Angebote in [!UICONTROL Automated Personalization]

Informationen zur Verwendung von Berichtsgruppen in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) -Aktivitäten (AP).

Berichtsgruppen erfüllen zwei grundlegende Funktionen:

* Mit Berichtsgruppen können Sie Ihre Angebote in AP-Aktivitätsberichten gruppiert anzeigen.
* Berichtsgruppen spielen eine Schlüsselrolle bei der Funktionsweise der [!DNL Target]-Personalisierungsmodelle.

Wenn Sie Berichtsgruppen verwenden, erstellt [!DNL Target] ein Personalisierungsmodell für jede Berichtsgruppe, das die Daten aller Angebote in dieser Gruppe verwendet. Ohne Berichtsgruppen erstellt [!DNL Target] ein Personalisierungsmodell für jedes Angebot in Ihrer AP-Aktivität.

Wenn Ihre Aktivitätseinrichtung nicht genügend Daten enthält, um ein Personalisierungsmodell pro Angebot zu erstellen, können Berichtsgruppen dazu beitragen, die Datenanforderungen zu reduzieren und [!UICONTROL Automated Personalization] zu verwenden. Berichtsgruppen können auch das Problem des „Kaltstarts“ für neue Angebote beheben, indem ähnliche Angebote gruppiert werden, damit jedes Modell mit mehr Daten arbeiten kann. Modellgruppen können auch für Aktivitäten verwendet werden, bei denen regelmäßig neue Angebote in Ihre AP-Aktivität eingeführt werden.

Dieser Ansatz funktioniert gut, wenn Besucher auf alle Angebote in einer Gruppe gleich reagieren. Best Practice ist es, Angebote zu gruppieren, auf die ähnliche Besuchergruppen auf ähnliche Weise reagieren. Anders ausgedrückt: Gruppieren Sie Angebote mit ähnlichen Konversionsraten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben. Die Gruppierung aller Angebote oder die Gruppierung von Angeboten mit unterschiedlichen Konversionsraten verringert wahrscheinlich die Effektivität der [!DNL Target] -Personalisierungsmodelle.

>[!NOTE]
>
>Wenn ein Angebot aus einer bestimmten Modellgruppe entfernt oder ersetzt wird, wird der historische Traffic mit diesem spezifischen Angebot auch aus der Modellgruppe gelöscht. Das heißt, gelöschte Angebote tragen nicht dazu bei, welche Daten verwendet werden, damit die [!DNL Target]-Personalisierungsmodelle lernen.

## Einrichten von Berichtsgruppen

1. Klicken Sie auf der Seite **[!UICONTROL Experiences]** einer AP-Aktivität auf das Symbol **[!UICONTROL Manage Content]** .

   ![Symbol &quot;Inhalt verwalten&quot;](/help/main/c-reports/assets/ap_manage_content.png)

1. Klicken Sie oben im Dialogfeld [!UICONTROL Manage Content] auf die Registerkarte **[!UICONTROL Offers]** .
1. (Bedingt) Fügen Sie bestimmte Erlebnisse zu einer Berichtsgruppe hinzu, indem Sie den Mauszeiger über das gewünschte Angebot bewegen und dann auf das Ordnersymbol **[!UICONTROL Reporting Group]** klicken.

   ![Symbol &quot;Berichtsgruppe&quot;](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Bedingt) Fügen Sie Erlebnisse stapelweise zu einer Berichtsgruppe hinzu, indem Sie die Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Ordnersymbol **[!UICONTROL Reporting Group]** klicken.

   ![Symbol &quot;Berichtsgruppe&quot;](/help/main/c-reports/assets/ap_manage_content_3.png)

1. Um das ausgewählte Angebot einer vorhandenen Berichtsgruppe zuzuweisen, wählen Sie **[!UICONTROL Existing]**, wählen Sie die gewünschte Berichtsgruppe aus der Dropdownliste aus und klicken Sie dann auf **[!UICONTROL Apply]**.

   Oder

   Um eine Berichtsgruppe zu erstellen, der das ausgewählte Angebot zugewiesen werden soll, wählen Sie **[!UICONTROL New]**, geben Sie der neuen Berichtsgruppe einen Namen und klicken Sie dann auf **[!UICONTROL Apply]**.

   ![Neues Symbol zum Erstellen einer neuen Berichtsgruppe](/help/main/c-reports/assets/ap_reporting_groups.png)

Sie können die Liste [!UICONTROL Location] verwenden, um Angebote nach Ort zu filtern. Verwenden Sie die Liste &quot;[!UICONTROL Report Group]&quot;, um Angebote nach Berichtsgruppen zu filtern. Sie können auch die Liste [!UICONTROL Report Group] verwenden, um nach [!UICONTROL Unassigned Offers] zu filtern, sodass Sie eine Berichtsgruppe einem Angebot zuweisen können, das keiner Berichtsgruppe zugewiesen ist.

Informationen zum Targeting eines Angebots für bestimmte Zielgruppen finden Sie unter [Targeting [!UICONTROL Automated Personalization] von Angeboten](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Einschränkungen 

* Es ist wichtig zu verstehen, dass Berichtsgruppen Einfluss darauf haben, wie [!DNL Target] seine Modelle erstellt. Daher empfiehlt [!DNL Adobe], Berichtsgruppen nur dann zu verwenden, wenn Sie planen, während einer aktiven Aktivität neue Angebote zu ersetzen oder hinzuzufügen. Wenn ein neues Angebot in eine Live-Aktivität eingeführt wird, kann die Maschine durch die Unterteilung des neuen Angebots in eine Gruppe mit vorhandenen ähnlichen Angeboten die bereits für die anderen Angebote in der Gruppe erfassten Daten verwenden, um mehr über das neue Angebot zu erfahren. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben.

* AP-Aktivitäten verfügen über Kombinationen aus Standort+Angebot (modellables). Wenn [!DNL Target] Daten in Berichten aufzeichnet, berücksichtigt [!DNL Target] solche Kombinationen, sodass klar ist, von welchem Ereignis (Anzeige, Klick usw.) das Angebot stammte.

  Eine Aktivität kann beispielsweise mehrere Orte und mehrere Angebote haben, die sich überschneiden können. Wenn ein Besucher mehr als eines dieser Angebote an verschiedenen Orten sieht, zeichnet [!DNL Target] nur Daten für diese Angebote auf. Wenn derselbe Besucher später auf ein Angebot klickt, zeichnet [!DNL Target] nur ein Ereignis aus dieser Kombination auf (nicht für alle Kombinationen).

  Wenn der Klick von einer anderen Position kommt, die in einer Metrik vorhanden ist, aber kein Angebot anzeigt, wird dieses Ereignis unter der Aktivität protokolliert, jedoch nicht für eine Kombination aus Angebot und Position. Daher wird dieses Angebot nicht in der Angebotsberichtsgruppe angezeigt.

  Dies liegt daran, dass der Klick aus einer anderen Mbox und nicht aus der Mbox vorgenommen wurde, die das Angebot bereitgestellt hat. Aus diesem Grund ist die Metrik mit der Aktivität verknüpft, jedoch nicht mit dem Angebot.

## Angebote in einer Berichtsgruppe anzeigen

1. Klicken Sie auf &quot;**[!UICONTROL Activities]**&quot;, klicken Sie in der Liste auf die gewünschte [!UICONTROL Automated Personalization] -Aktivität und dann auf die Registerkarte &quot;**[!UICONTROL Reports]**&quot;, um den Bericht &quot;Angebotsstufe&quot;](/help/main/c-reports/personalization-reports/reports-ap.md) anzuzeigen.[

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol [!UICONTROL Show Filters] (Trichter) und aktivieren Sie dann das Kontrollkästchen [!UICONTROL Automated Personalization] , um die Liste so zu filtern, dass nur [!UICONTROL Automated Personalization] Aktivitäten angezeigt werden.

1. Klicken Sie in der Tabelle auf **[!UICONTROL Control]** oder **[!UICONTROL Targeted]** , um die nicht gruppierten Angebote und Angebote in Berichtsgruppen anzuzeigen.

   ![Angebotsgruppen: Kontrolle und Zielgruppe](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Informationen zur Verwendung von [!UICONTROL Automated Personalization] -Berichten (einschließlich des [!UICONTROL Offer Level] -Berichts) finden Sie unter [Automated Personalization-Zusammenfassungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).


