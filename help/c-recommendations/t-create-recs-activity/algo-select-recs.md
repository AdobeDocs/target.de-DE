---
keywords: Recommendations;Recommendations-Aktivität;Kriterien;Algorithmus
description: Erfahren Sie, wie Sie die Kriterien (Regeln, die bestimmen, welche Produkte oder Inhalte Sie empfehlen) auswählen, die in Ihrer Adobe [!DNL Target] Recommendations-Aktivität verwendet werden sollen.
title: Wie wähle ich Kriterien für eine Recommendations-Aktivität aus?
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 72%

---

# ![PREMIUM](/help/assets/premium.png) Kriterienauswahl

Wählen Sie die [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md) aus, die in Ihrer [!DNL Adobe Target Recommendations]-Aktivität verwendet werden sollen. Kriterien sind Regeln, die auf Basis vorab ermittelter Verhaltensweisen von Besuchern festlegen, welche Produkte empfohlen werden.

Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehr als ein Kriterium verwenden.

Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

* Um nach einem vorhandenen Kriterium zu suchen (zum Beispiel wenn viele Kriterienkarten angezeigt werden), geben Sie Text in das Suchfeld ein, bis das gewünschte Kriterium erscheint, wählen Sie dieses aus und klicken Sie auf **[!UICONTROL Fertig]**.

   Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

* Um ein neues Kriterium zu erstellen, klicken Sie auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]** und geben Sie dann die Informationen für das neue Kriterium ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Neue Kriterien erstellen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**So wählen Sie Kriterien aus:**

1. Beim Erstellen einer neuen Empfehlung [suchen Sie im Dialogfeld **[!UICONTROL Kriterien auswählen]** nach einem oder mehreren Kriterien und wählen Sie diese aus.](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

   ![Dialogfeld „Kriterien auswählen“](/help/c-recommendations/t-create-recs-activity/assets/filters.png)

   Sie können zum Filtern der Kriterienliste den Filter [!UICONTROL Branchentyp], den Filter [!UICONTROL Seitentyp] und das Kontrollkästchen [!UICONTROL Kompatibel] verwenden. Diese Optionen helfen Ihnen bei der Suche nach den gewünschten Kriterien.

   * **Branchentyp:** Der Branchentyp wird verwendet, um bei der Kategorisierung Ihrer Kriterien in [!DNL Recommendations] zu helfen. Um die Standardeinstellung für die Branche zu ändern, klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]** und wählen Sie die gewünschte Standardeinstellung **[!UICONTROL Branche vertikal]** aus.
   * **Seitentyp:** Der Seitentyp hilft ihnen, Ihre Empfehlungen zu kategorisieren. Es gibt auch integrierte Kriterien, die für jeden Seitentyp gewählt werden können.
   * **Kompatibel:** Zeigt nur diejenigen Kriterien, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für das aktuelle Element/die aktuellen Kategorieempfehlungen übermitteln, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, heben Sie die Auswahl für die Option **[!UICONTROL Kompatibel]** auf. Diese Option kann in Ihren Einstellungen deaktiviert oder aktiviert werden: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um das Dialogfeld[Design auswählen](/help/c-recommendations/c-design-overview/design-overview.md) anzuzeigen.
