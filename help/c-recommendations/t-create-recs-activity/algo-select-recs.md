---
description: Wählen Sie die Kriterien aus, die für Ihre Recommendations-Aktivität verwendet werden sollen.
keywords: Empfehlungen; Empfehlungs-Aktivität; Kriterien
seo-description: Wählen Sie die Kriterien aus, die für Ihre Recommendations-Aktivität verwendet werden sollen.
seo-title: Kriterienauswahl
solution: Target
title: Kriterienauswahl
title-outputclass: premium
topic: Premium
uuid: 1a1e13e0-7fbd-4f86-80da-cd4e96748d30
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Kriterienauswahl{#select-criteria}

Wählen Sie die Kriterien aus, die für Ihre Recommendations-Aktivität verwendet werden sollen.

Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehr als ein Kriterium verwenden.

Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

* Um nach einem vorhandenen Kriterium zu suchen (zum Beispiel wenn viele Kriterienkarten angezeigt werden), geben Sie Text in das Suchfeld ein, bis das gewünschte Kriterium erscheint, wählen Sie dieses aus und klicken Sie auf **[!UICONTROL Fertig]**.

   Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

* Um ein neues Kriterium zu erstellen, klicken Sie auf **[!UICONTROL Neu erstellen]** und geben Sie dann die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Neue Kriterien erstellen](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).

1. [Erstellen Sie eine neue Empfehlung](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F) oder suchen Sie die Empfehlung, deren Kriterien Sie einstellen möchten, und klicken Sie auf **[!UICONTROL Bearbeiten]**.
1. Wählen Sie einen Branchentyp und einen Seitentyp.

* **Branchentyp:** Der Branchentyp wird verwendet, um bei der Kategorisierung Ihrer Kriterien in [!DNL Recommendations] zu helfen. Möchten Sie den standardmäßigen vertikalen Markt ändern, klicken Sie auf **[!UICONTROL Einstellungen]** und wählen Sie die gewünschte Einstellung für den **vertikalen Markt]aus.[!UICONTROL **
* **Seitentyp:** Der Seitentyp hilft ihnen, Ihre Empfehlungen zu kategorisieren. Es gibt auch integrierte Kriterien, die für jeden Seitentyp gewählt werden können.
* **Kompatibel:** Zeigt nur diejenigen Kriterien, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die [!DNL entity.categoryId] für das aktuelle Element/die aktuellen Kategorieempfehlungen übermitteln, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, heben Sie die Auswahl für die Option **[!UICONTROL Kompatibel]auf.** Diese Option lässt sich in Ihren [!DNL Target][!UICONTROL -Einstellungen] aktivieren bzw. deaktivieren.

1. Klicken Sie auf **[!UICONTROL Hinzufügen]**.
