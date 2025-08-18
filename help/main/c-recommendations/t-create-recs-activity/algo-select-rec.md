---
keywords: Recommendations; Recommendations-Aktivität; Kriterien; Algorithmus
description: Erfahren Sie, wie Sie die Kriterien (Regeln, die bestimmen, welche Produkte oder Inhalte empfohlen werden sollen) auswählen, die in Ihrer Adobe/Recommendations [!DNL Target] Aktivität verwendet werden sollen.
title: Wie wähle ich Kriterien für eine Recommendations-Aktivität aus?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 119227ec-88c3-4de9-b2cf-f7d5fa2e98f6
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 55%

---

# Kriterienauswahl

Wählen Sie die [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md) aus, die in Ihrer [!DNL Adobe Target Recommendations]-Aktivität verwendet werden sollen. Kriterien sind Regeln, die auf Basis vorab ermittelter Verhaltensweisen von Besuchern festlegen, welche Produkte empfohlen werden.

Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehr als ein Kriterium verwenden.

Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

* Um nach einem vorhandenen Kriterium zu suchen (z. B. wenn viele Kriterienkarten angezeigt werden), geben Sie im Suchfeld ein, bis das gewünschte Kriterium angezeigt wird. Wählen Sie dann das Kriterium aus und klicken Sie auf **[!UICONTROL Done]**.

  Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

* Um neue Kriterien zu erstellen, klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** und geben Sie die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Neue Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

**So wählen Sie Kriterien aus:**

1. Suchen [ beim Erstellen einer neuen ](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F) im Dialogfeld &quot;**[!UICONTROL Select Criteria]**&quot; nach einem oder mehreren Kriterien und wählen diese aus.

   Sie können die Kriterienliste mithilfe der Kontrollkästchen [!UICONTROL Industry Type], [!UICONTROL Page Type] und [!UICONTROL Compatible] filtern. Diese Optionen helfen Ihnen bei der Suche nach den gewünschten Kriterien.

   * **Branchentyp:** Der Branchentyp wird verwendet, um bei der Kategorisierung Ihrer Kriterien in [!DNL Recommendations] zu helfen. Um die Standardbrancheneinstellung für die vertikale Ausrichtung zu ändern, klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** und wählen Sie die gewünschte Standardeinstellung für die **[!UICONTROL Industry Vertical]** aus.
   * **Seitentyp:** Der Seitentyp hilft ihnen, Ihre Empfehlungen zu kategorisieren. Es gibt auch integrierte Kriterien, die für jeden Seitentyp gewählt werden können.
   * **Kompatibel:** Zeigt nur diejenigen Kriterien, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für das aktuelle Element/die aktuellen Kategorieempfehlungen übermitteln, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn für die Aktivität jedoch inkompatible Kriterien verfügbar sein sollen, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Compatible]** . Diese Option kann in Ihren Einstellungen deaktiviert oder aktiviert werden: **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

1. Klicken Sie auf **[!UICONTROL Next]**, um das Dialogfeld [Design auswählen](/help/main/c-recommendations/c-design-overview/design-overview.md) anzuzeigen.
