---
description: Informationen zur Verwendung von Berichtsgruppen in AP-(Automated Personalization-)Aktivitäten.
keywords: Automatisierte Personalisierung; Angebot; Berichterstellung; Gruppe
seo-description: Informationen zur Verwendung von Berichtsgruppen in AP-(Automated Personalization-)Aktivitäten.
seo-title: Berichtsgruppen für Angebote in Automated Personalization
solution: Target
title: Berichtsgruppen für Angebote in Automated Personalization
title-outputclass: premium
topic: Advanced
uuid: 5b111a68-bd05-4ef1-8156-d064f2c7e257
badge: premium
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![PREMIUM](/help/assets/premium.png) Angebotsberichtsgruppen in der automatisierten Personalisierung{#offer-reporting-groups-in-automated-personalization}

Informationen zur Verwendung von Berichtsgruppen in AP-(Automated Personalization-)Aktivitäten.

Berichtsgruppen erfüllen zwei grundlegende Funktionen:

* Über sie können Sie Angebote gruppiert in AP-Aktivitätsberichten anzeigen.
* Sie spielen eine wichtige Rolle für die Funktionalität der Personalisierungsmodelle von Target.

Wenn Sie Berichtsgruppen verwenden, erstellt Target nur ein Personalisierungsmodell für jede Berichtsgruppe anstatt für jedes Angebot in Ihrer AP-Aktivität und verwendet hierzu Daten aus allen Angeboten in der jeweiligen Gruppe.

Wenn Ihr Aktivitäts-Setup nicht genügend Daten für die Erstellung eines Personalisierungsmodells pro Angebot bietet, können Berichtsgruppen die Datenanforderungen für die Verwendung von Automated Personalization reduzieren. Berichtsgruppen können auch das Problem des „Kaltstarts“ für neue Angebote beheben, indem ähnliche Angebote gruppiert werden, damit jedes Modell mit mehr Daten arbeiten kann. Modellierungsgruppen können auch für Aktivitäten verwendet werden, in denen regelmäßig neue Angebote in Ihre AP-Aktivität eingeführt werden.

Dieser Ansatz funktioniert gut, wenn Besucher auf alle Angebote in einer Gruppe gleich reagieren. Best Practice ist es, Angebote zu gruppieren, auf die ähnliche Besuchergruppen auf ähnliche Weise reagieren. Anders ausgedrückt: Gruppieren Sie Angebote mit ähnlichen Konversionsraten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben. Die Gruppierung aller Angebote bzw. von Angeboten mit sehr unterschiedlichen Konversionsraten reduziert wahrscheinlich die Effektivität der Target-Personalisierungsmodelle.

>[!NOTE]
>
>Wenn ein Angebot aus einer bestimmten Modellgruppe entfernt oder ersetzt wird, wird der historische Traffic mit diesem spezifischen Angebot auch aus der Modellgruppe gelöscht. Anders ausgedrückt: Gelöschte Angebote tragen nicht zu den Daten bei, die die Target-Personalisierungsmodelle zum Lernen nutzen.

**So richten Sie Berichtsgruppen ein:**

1. Klicken Sie auf der Seite „Erlebnisse“ einer AP-Aktivität auf das Symbol **[!UICONTROL Inhalt verwalten].**

   ![](assets/ap_manage_content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Angebote]** oben im Dialogfeld [!UICONTROL Inhalt verwalten].
1. (Optional) Fügen Sie bestimmte Erlebnisse zu einer Berichtsgruppe hinzu, indem Sie mit dem Mauszeiger über das gewünschte Angebot fahren und auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]klicken.**

   ![](assets/ap_manage_content_2.png)

1. (Optional) Fügen Sie Erlebnisse stapelweise zu einer Berichtsgruppe hinzu, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]klicken.**

   ![](assets/ap_reporting_groups.png)

1. Um das ausgewählte Angebot zu einer bestehenden Berichtsgruppe hinzuzufügen, klicken Sie auf **[!UICONTROL Vorhanden]**, wählen Sie die gewünschte Berichtsgruppe aus der Dropdownliste aus und klicken Sie dann auf **[!UICONTROL Übernehmen]**.

   Oder

   Um eine neue Berichtsgruppe zu erstellen, der Sie das ausgewählte Angebot zuweisen können, wählen Sie **[!UICONTROL Neu]** aus, geben Sie den Namen der neuen Berichtsgruppe ein und klicken Sie auf **[!UICONTROL Übernehmen]**.

   ![](assets/ap_manage_content_3.png)

