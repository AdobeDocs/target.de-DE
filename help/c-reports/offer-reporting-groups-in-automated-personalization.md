---
description: Informationen zur Verwendung von Berichtsgruppen in AP-(Automated Personalization-)Aktivitäten.
keywords: Automatisierte Personalisierung; Angebot; Berichterstellung; Gruppe;Berichtsgruppe
seo-description: Informationen zur Verwendung von Berichtsgruppen in automatisierten Personalisierungsaktivitäten (AP) in Adobe Target.
seo-title: Berichtgruppen in Aktivitäten mit automatisierter Personalisierung (AP) in Adobe Target anbieten
solution: Target
title: Berichtsgruppen für Angebote in Automated Personalization
title-outputclass: premium
topic: Advanced
uuid: 5b111a68-bd05-4ef1-8156-d064f2c7e257
badge: premium
translation-type: tm+mt
source-git-commit: 1df7fbf78f9e20d8a907809b228ed591036c1a24

---


# ![PREMIUM](/help/assets/premium.png) Angebotsberichtsgruppen in der automatisierten Personalisierung{#offer-reporting-groups-in-automated-personalization}

Information about using reporting groups in [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activities.

Berichtsgruppen erfüllen zwei grundlegende Funktionen:

* Über sie können Sie Angebote gruppiert in AP-Aktivitätsberichten anzeigen.
* They play a key role with how the [!DNL Target] personalization models function.

When you use reporting groups, [!DNL Target] creates only one personalization model for each reporting group instead of each offer in your AP activity using the data from all offers in that group.

Wenn Ihr Aktivitäts-Setup nicht genügend Daten für die Erstellung eines Personalisierungsmodells pro Angebot bietet, können Berichtsgruppen die Datenanforderungen für die Verwendung von Automated Personalization reduzieren. Berichtsgruppen können auch das Problem des „Kaltstarts“ für neue Angebote beheben, indem ähnliche Angebote gruppiert werden, damit jedes Modell mit mehr Daten arbeiten kann. Modellierungsgruppen können auch für Aktivitäten verwendet werden, in denen regelmäßig neue Angebote in Ihre AP-Aktivität eingeführt werden.

Dieser Ansatz funktioniert gut, wenn Besucher auf alle Angebote in einer Gruppe gleich reagieren. Best Practice ist es, Angebote zu gruppieren, auf die ähnliche Besuchergruppen auf ähnliche Weise reagieren. Anders ausgedrückt: Gruppieren Sie Angebote mit ähnlichen Konversionsraten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben. Grouping all offers or grouping offers with very different conversion rates likely reduces the effectiveness of the [!DNL Target] personalization models.

>[!NOTE]
>
>Wenn ein Angebot aus einer bestimmten Modellgruppe entfernt oder ersetzt wird, wird der historische Traffic mit diesem spezifischen Angebot auch aus der Modellgruppe gelöscht. In other words, deleted offers do not contribute to what data is used for the [!DNL Target] personalization models to learn.

**So richten Sie Berichtsgruppen ein:**

1. On the [!UICONTROL Experiences] page of an AP activity, click the **[!UICONTROL Manage Content]** icon.

   ![](assets/ap_manage_content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Angebote]** oben im Dialogfeld [!UICONTROL Inhalt verwalten].
1. (Optional) Fügen Sie bestimmte Erlebnisse zu einer Berichtsgruppe hinzu, indem Sie mit dem Mauszeiger über das gewünschte Angebot fahren und auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]klicken.**

   ![](assets/ap_manage_content_2.png)

1. (Optional) Fügen Sie Erlebnisse stapelweise zu einer Berichtsgruppe hinzu, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]klicken.**

   ![](assets/ap_manage_content_3.png)

1. (Conditional) To assign the selected offer to an existing reporting group, select **[!UICONTROL Existing]**, select the desired reporting group from the drop-down list, then click **[!UICONTROL Apply]**.

   Oder

   Um eine neue Berichtsgruppe zu erstellen, der Sie das ausgewählte Angebot zuweisen können, wählen Sie **[!UICONTROL Neu]** aus, geben Sie den Namen der neuen Berichtsgruppe ein und klicken Sie auf **[!UICONTROL Übernehmen]**.

   ![](assets/ap_reporting_groups.png)

