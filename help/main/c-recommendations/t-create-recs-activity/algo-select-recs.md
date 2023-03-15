---
keywords: Empfehlungen; Empfehlungsaktivität; Kriterien; Algorithmus
description: Erfahren Sie, wie Sie die Kriterien (Regeln, die bestimmen, welche Produkte oder Inhalte für Ihre Adobe empfohlen werden) auswählen [!DNL Target] Recommendations-Aktivität.
title: Wie wähle ich Kriterien für eine Recommendations-Aktivität aus?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 72%

---

# Kriterienauswahl

Wählen Sie die [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md) zur Verwendung in [!DNL Adobe Target Recommendations] Aktivität. Kriterien sind Regeln, die auf Basis vorab ermittelter Verhaltensweisen von Besuchern festlegen, welche Produkte empfohlen werden.

Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehr als ein Kriterium verwenden.

Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

* Um nach einem vorhandenen Kriterium zu suchen (zum Beispiel wenn viele Kriterienkarten angezeigt werden), geben Sie Text in das Suchfeld ein, bis das gewünschte Kriterium erscheint, wählen Sie dieses aus und klicken Sie auf **[!UICONTROL Fertig]**.

   Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

* Um ein neues Kriterium zu erstellen, klicken Sie auf **[!UICONTROL Erstellen von Kriterien]** > **[!UICONTROL Erstellen von Kriterien]** und geben Sie dann die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Neue Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**So wählen Sie Kriterien aus:**

1. while [Erstellen einer neuen Empfehlung](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)in der **[!UICONTROL Kriterien auswählen]** ein oder mehrere Kriterien auswählen.

   ![Dialogfeld „Kriterien auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/filters.png)

   Sie können zum Filtern der Kriterienliste den Filter [!UICONTROL Branchentyp], den Filter [!UICONTROL Seitentyp] und das Kontrollkästchen [!UICONTROL Kompatibel] verwenden. Diese Optionen helfen Ihnen bei der Suche nach den gewünschten Kriterien.

   * **Branchentyp:** Der Branchentyp wird verwendet, um bei der Kategorisierung Ihrer Kriterien in [!DNL Recommendations] zu helfen. Um den standardmäßigen vertikalen Markt zu ändern, klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]** und wählen Sie die gewünschte Standardeinstellung aus **[!UICONTROL Vertikaler Markt]** -Einstellung.
   * **Seitentyp:** Der Seitentyp hilft ihnen, Ihre Empfehlungen zu kategorisieren. Es gibt auch integrierte Kriterien, die für jeden Seitentyp gewählt werden können.
   * **Kompatibel:** Zeigt nur diejenigen Kriterien, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für das aktuelle Element/die aktuellen Kategorieempfehlungen übermitteln, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, heben Sie die Auswahl für die Option **[!UICONTROL Kompatibel]** auf. Diese Option kann in Ihren Einstellungen deaktiviert oder aktiviert werden: **[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]**.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um das Dialogfeld[Design auswählen](/help/main/c-recommendations/c-design-overview/design-overview.md) anzuzeigen.
