---
keywords: recommendations;recommendations activity;criteria
description: Wählen Sie die Kriterien aus, die für Ihre Adobe Target-Recommendations-Aktivität verwendet werden sollen.
title: Kriterienauswahl
feature: recs creation
uuid: 1a1e13e0-7fbd-4f86-80da-cd4e96748d30
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Kriterienauswahl{#select-criteria}

Wählen Sie die [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md) aus, die für Ihre Recommendations-Aktivität verwendet werden sollen. Kriterien sind Regeln, die auf Basis vorab ermittelter Verhaltensweisen von Besuchern festlegen, welche Produkte empfohlen werden.

Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehr als ein Kriterium verwenden.

Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

* Um nach einem vorhandenen Kriterium zu suchen (zum Beispiel wenn viele Kriterienkarten angezeigt werden), geben Sie Text in das Suchfeld ein, bis das gewünschte Kriterium erscheint, wählen Sie dieses aus und klicken Sie auf **[!UICONTROL Fertig]**.

   Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

* Um ein neues Kriterium zu erstellen, klicken Sie auf **[!UICONTROL Kriterien erstellen]** und geben Sie dann die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Neue Kriterien erstellen](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**So wählen Sie Kriterien aus:**

1. Wählen Sie beim [Erstellen einer neuen Empfehlung](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F) im Dialogfeld **[!UICONTROL „Kriterien“]** ein oder mehrere Kriterien aus.

   ![Dialogfeld „Kriterien auswählen“](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   Sie können zum Filtern der Kriterienliste den Filter [!UICONTROL Branchentyp], den Filter [!UICONTROL Seitentyp] und das Kontrollkästchen [!UICONTROL Kompatibel] verwenden. Diese Optionen helfen Ihnen bei der Suche nach den gewünschten Kriterien.

   * **Branchentyp:** Der Branchentyp wird verwendet, um bei der Kategorisierung Ihrer Kriterien in [!DNL Recommendations] zu helfen. Möchten Sie den standardmäßigen vertikalen Markt ändern, klicken Sie auf **[!UICONTROL Einstellungen]** und wählen Sie die gewünschte Einstellung für den **[!UICONTROL vertikalen Markt]** aus.
   * **Seitentyp:** Der Seitentyp hilft ihnen, Ihre Empfehlungen zu kategorisieren. Es gibt auch integrierte Kriterien, die für jeden Seitentyp gewählt werden können.
   * **Kompatibel:** Zeigt nur diejenigen Kriterien, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für das aktuelle Element/die aktuellen Kategorieempfehlungen übermitteln, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, heben Sie die Auswahl für die Option **[!UICONTROL Kompatibel]** auf. Diese Option lässt sich in Ihren [!DNL Target][!UICONTROL -Einstellungen] aktivieren bzw. deaktivieren.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um das Dialogfeld[Design auswählen](/help/c-recommendations/c-design-overview/design-overview.md) anzuzeigen.
