---
keywords: automatisierte Personalisierung;Angebot;Berichterstellung;Gruppe;Berichtsgruppe;App
description: Erfahren Sie, wie Sie in Adobe Angebotsberichtsgruppen verwenden. [!DNL Target] [!UICONTROL Automated Personalization] Aktivitäten.
title: Kann ich Berichtsgruppen für Angebote in Automated Personalization-Aktivitäten verwenden?
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: a4219573c1ce253b1c2e163483fb6d901176ed70
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 47%

---

# ![PREMIUM](/help/main/assets/premium.png)[!UICONTROL  Angebotsberichtsgruppen in der automatisierten Personalisierung]

Informationen zur Verwendung von Berichtsgruppen in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) AP-Aktivitäten.

Berichtsgruppen erfüllen zwei grundlegende Funktionen:

* Mit Berichtsgruppen können Sie Ihre Angebote in AP-Aktivitätsberichten gruppiert anzeigen.
* Berichtsgruppen spielen eine Schlüsselrolle bei der [!DNL Target] Personalisierungsmodelle verwenden.

Wenn Sie Berichtsgruppen verwenden, [!DNL Target] erstellt für jede Berichtsgruppe ein Personalisierungsmodell anhand der Daten aller Angebote in dieser Gruppe. Ohne Berichtsgruppen [!DNL Target] erstellt für jedes Angebot in Ihrer AP-Aktivität ein Personalisierungsmodell.

Wenn Ihre Aktivitätseinrichtung nicht genügend Daten enthält, um ein Personalisierungsmodell pro Angebot zu erstellen, können Berichtsgruppen dazu beitragen, die zu verwendenden Datenanforderungen zu reduzieren [!UICONTROL Automated Personalization]. Berichtsgruppen können auch das Problem des „Kaltstarts“ für neue Angebote beheben, indem ähnliche Angebote gruppiert werden, damit jedes Modell mit mehr Daten arbeiten kann. Modellgruppen können auch für Aktivitäten verwendet werden, bei denen regelmäßig neue Angebote in Ihre AP-Aktivität eingeführt werden.

Dieser Ansatz funktioniert gut, wenn Besucher auf alle Angebote in einer Gruppe gleich reagieren. Best Practice ist es, Angebote zu gruppieren, auf die ähnliche Besuchergruppen auf ähnliche Weise reagieren. Anders ausgedrückt: Gruppieren Sie Angebote mit ähnlichen Konversionsraten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben. Die Gruppierung aller Angebote oder die Gruppierung von Angeboten mit sehr unterschiedlichen Konversionsraten verringert wahrscheinlich die Effektivität der [!DNL Target] Personalisierungsmodelle.

>[!NOTE]
>
>Wenn ein Angebot aus einer bestimmten Modellgruppe entfernt oder ersetzt wird, wird der historische Traffic mit diesem spezifischen Angebot auch aus der Modellgruppe gelöscht. Das heißt, gelöschte Angebote tragen nicht dazu bei, welche Daten für die [!DNL Target] zu lernende Personalisierungsmodelle.

## Einrichten von Berichtsgruppen

1. Im **[!UICONTROL Erlebnisse]** Seite einer AP-Aktivität, klicken Sie auf die **[!UICONTROL Inhalt verwalten]** Symbol.

   ![Symbol &quot;Inhalt verwalten&quot;](/help/main/c-reports/assets/ap_manage_content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Angebote]** oben im Dialogfeld [!UICONTROL Inhalt verwalten].
1. (Optional) Fügen Sie bestimmte Erlebnisse zu einer Berichtsgruppe hinzu, indem Sie mit dem Mauszeiger über das gewünschte Angebot fahren und auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]** klicken.

   ![Symbol &quot;Berichtsgruppe&quot;](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Optional) Fügen Sie Erlebnisse stapelweise zu einer Berichtsgruppe hinzu, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]** klicken.

   ![Symbol &quot;Berichtsgruppe&quot;](/help/main/c-reports/assets/ap_manage_content_3.png)

1. Um das ausgewählte Angebot zu einer bestehenden Berichtsgruppe hinzuzufügen, klicken Sie auf **[!UICONTROL Vorhanden]**, wählen Sie die gewünschte Berichtsgruppe aus der Dropdownliste aus und klicken Sie dann auf **[!UICONTROL Übernehmen]**.

   Oder

   Um eine neue Berichtsgruppe zu erstellen, der Sie das ausgewählte Angebot zuweisen können, wählen Sie **[!UICONTROL Neu]** aus, geben Sie den Namen der neuen Berichtsgruppe ein und klicken Sie auf **[!UICONTROL Übernehmen]**.

   ![Neues Symbol zum Erstellen einer neuen Berichtsgruppe](/help/main/c-reports/assets/ap_reporting_groups.png)

## Angebote in einer Berichtsgruppe anzeigen

1. Klicken **[!UICONTROL Tätigkeiten]** klicken Sie auf die gewünschte [!UICONTROL Automated Personalization] aus der Liste aus und klicken Sie auf die Schaltfläche **[!UICONTROL Berichte]** zum Anzeigen der [Angebotsebene](/help/main/c-reports/personalization-reports/reports-ap.md) Bericht.

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie [!UICONTROL Automatisierte Personalisierung] in der Dropdownliste [!UICONTROL Typ] auswählen.

1. Klicken **[!UICONTROL Kontrolle]** oder **[!UICONTROL Targeting]** in der Tabelle, um die nicht gruppierten Angebote und Angebote in Berichtsgruppen anzuzeigen.

   ![Angebotsgruppen: Kontrolle und Zielgruppe](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Informationen zur Verwendung von [!UICONTROL Automated Personalization] Berichte (einschließlich [!UICONTROL Angebotsebene] ), siehe [Automated Personalization-Zusammenfassungsberichte](/help/main/c-reports/personalization-reports/reports-ap.md).


