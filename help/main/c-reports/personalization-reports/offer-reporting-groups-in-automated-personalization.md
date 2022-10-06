---
keywords: automatisierte Personalisierung;Angebot;Berichterstellung;Gruppe;Berichtsgruppe
description: Erfahren Sie, wie Sie in Adobe Angebotsberichtsgruppen verwenden. [!DNL Target] Automated Personalization-Aktivitäten. Verwenden von Berichtsgruppen, [!DNL Target] erstellt nur ein Personalisierungsmodell für jede Berichtsgruppe.
title: Kann ich Berichtsgruppen für Angebote in Automated Personalization-Aktivitäten verwenden?
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 79d51e39b733ee13270f924912251e45c8597917
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 59%

---

# ![PREMIUM](/help/main/assets/premium.png) Angebotsberichtsgruppen in der automatisierten Personalisierung

Informationen zur Verwendung von Berichtsgruppen in [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) AP-Aktivitäten.

Berichtsgruppen erfüllen zwei grundlegende Funktionen:

* Über sie können Sie Angebote gruppiert in AP-Aktivitätsberichten anzeigen.
* Sie spielen eine Schlüsselrolle bei der Frage, wie die [!DNL Target] Personalisierungsmodelle verwenden.

Wenn Sie Berichtsgruppen verwenden, [!DNL Target] erstellt für jede Berichtsgruppe nur ein einziges Personalisierungsmodell anstelle jedes Angebots in Ihrer AP-Aktivität und verwendet dabei die Daten aller Angebote in dieser Gruppe.

Wenn Ihr Aktivitäts-Setup nicht genügend Daten für die Erstellung eines Personalisierungsmodells pro Angebot bietet, können Berichtsgruppen die Datenanforderungen für die Verwendung von Automated Personalization reduzieren. Berichtsgruppen können auch das Problem des „Kaltstarts“ für neue Angebote beheben, indem ähnliche Angebote gruppiert werden, damit jedes Modell mit mehr Daten arbeiten kann. Modellierungsgruppen können auch für Aktivitäten verwendet werden, in denen regelmäßig neue Angebote in Ihre AP-Aktivität eingeführt werden.

Dieser Ansatz funktioniert gut, wenn Besucher auf alle Angebote in einer Gruppe gleich reagieren. Best Practice ist es, Angebote zu gruppieren, auf die ähnliche Besuchergruppen auf ähnliche Weise reagieren. Anders ausgedrückt: Gruppieren Sie Angebote mit ähnlichen Konversionsraten. Sie sollten niemals alle Angebote in eine einzelne Berichtsgruppe verschieben. Die Gruppierung aller Angebote oder die Gruppierung von Angeboten mit sehr unterschiedlichen Konversionsraten verringert wahrscheinlich die Effektivität der [!DNL Target] Personalisierungsmodelle.

>[!NOTE]
>
>Wenn ein Angebot aus einer bestimmten Modellgruppe entfernt oder ersetzt wird, wird der historische Traffic mit diesem spezifischen Angebot auch aus der Modellgruppe gelöscht. Das heißt, gelöschte Angebote tragen nicht dazu bei, welche Daten für die [!DNL Target] zu lernende Personalisierungsmodelle.

**So richten Sie Berichtsgruppen ein:**

1. Im [!UICONTROL Erlebnisse] Seite einer AP-Aktivität, klicken Sie auf die **[!UICONTROL Inhalt verwalten]** Symbol.

   ![Symbol &quot;Inhalt verwalten&quot;](/help/main/c-reports/assets/ap_manage_content.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Angebote]** oben im Dialogfeld [!UICONTROL Inhalt verwalten].
1. (Optional) Fügen Sie bestimmte Erlebnisse zu einer Berichtsgruppe hinzu, indem Sie mit dem Mauszeiger über das gewünschte Angebot fahren und auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]** klicken.

   ![Symbol &quot;Berichtsgruppe&quot;](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Optional) Fügen Sie Erlebnisse stapelweise zu einer Berichtsgruppe hinzu, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann oben rechts im Dialogfeld auf das Ordnersymbol **[!UICONTROL Berichtsgruppe]** klicken.

   ![Symbol &quot;Berichtsgruppe&quot;](/help/main/c-reports/assets/ap_manage_content_3.png)

1. (Bedingt) Um das ausgewählte Angebot einer vorhandenen Berichtsgruppe zuzuweisen, wählen Sie **[!UICONTROL Bestehend]**, wählen Sie die gewünschte Berichtsgruppe aus der Dropdownliste aus und klicken Sie dann auf **[!UICONTROL Anwenden]**.

   Oder

   Um eine neue Berichtsgruppe zu erstellen, der Sie das ausgewählte Angebot zuweisen können, wählen Sie **[!UICONTROL Neu]** aus, geben Sie den Namen der neuen Berichtsgruppe ein und klicken Sie auf **[!UICONTROL Übernehmen]**.

   ![Neues Symbol zum Erstellen einer neuen Berichtsgruppe](/help/main/c-reports/assets/ap_reporting_groups.png)
