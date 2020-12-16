---
keywords: custom parameters;target custom parameters;targetpageparams;targeting mbox parameters
description: Benutzerdefinierte Parameter sind Mbox-Parameter. Wenn Sie Mbox-Parameter an Mboxes übergeben oder die Funktion „targetPageParams“ verwenden, werden diese Parameter hier angezeigt und können in Zielgruppen verwendet werden.
title: Benutzerdefinierte Parameter in Adobe Target
feature: audiences
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 90%

---


# Benutzerdefinierte Parameter{#custom-parameters}

Benutzerdefinierte Parameter sind Mbox-Parameter. Wenn Sie Mbox-Parameter an Mboxes übergeben oder die Funktion „targetPageParams“ verwenden, werden diese Parameter hier angezeigt und können in Zielgruppen verwendet werden.

Weitere Informationen finden Sie unter [Parameter an eine globale Mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) weiterleiten.

Wenn Sie eine benutzerdefinierte Zielgruppe basierend auf einem erstellen, erhalten Sie von `mboxParameter`mboxParameter keine Aufforderung mehr, `mboxName` einzugeben. Der Mbox-Name ist nun optional. Mit dieser Änderung können Sie Parameter aus mehreren Mboxes verwenden oder auf einen Parameter verweisen, der noch nicht am Rand aufgezeichnet wurde.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Nennen Sie die Zielgruppe.
1. Klicken Sie auf **[!UICONTROL Hinzufügen Regel]** > **[!UICONTROL Benutzerdefiniert]**.

   So wählen Sie den gewünschten Parameter aus:

   * Wählen Sie beim Erstellen einer neuen Zielgruppe einen Parameter aus der Liste aus oder geben Sie die ersten Buchstaben des Parameternamens bzw. den gesamten Namen des gewünschten Parameters ein.
   * Wenn Sie den Mbox-, aber nicht den Parameternamen kennen, filtern Sie mithilfe des Kontrollkästchens nach der bekannten Mbox, die den gewünschten Parameter übergibt.

   Bei keiner der Methoden gibt es eine Verbindung zwischen Mbox und Parameter. Die Zielgruppe funktioniert basierend auf dem Parameter über alle Mboxes hinweg, die diesen Parameter übergeben.

   Wenn Sie eine bestehende Zielgruppe bearbeiten, werden die Filterkriterien mit dem Mbox-Namen angezeigt, der bei der Erstellung angegeben wurde.

1. Wählen Sie einen Auswerter:

   * enthält (nicht von Schreibweise abhängig)
   * enthält nicht (nicht von Schreibweise abhängig)
   * Gleich

   ![Benutzerdefinierte Parameter-Zielgruppe](/help/c-target/c-audiences/c-target-rules/assets/custom.png)

1. Geben Sie jeden Wert in eine neue Zeile ein.
1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und legen Sie zusätzliche Regeln für die Zielgruppe fest.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Die [Popupkarte mit Definitionsdetails](/help/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) der Zielgruppe enthält den Parameternamen im Abschnitt „Regeln“. Auf die Mbox, die zum Filtern verwendet wird, wird nicht verwiesen.

>[!NOTE]
>
>Für benutzerdefinierte Zielgruppen, die vor der Target-Version 18.5.1 (22. Mai 2018) erstellt wurden, werden in der Popup-Karte für die Zielgruppendefinition keine Mbox-Namen angezeigt. Sie müssen die benutzerdefinierte Zielgruppe erneut speichern, damit der Mbox-Name auf der Karte angezeigt wird.

## Zu beachten {#considerations}

* Zielgruppen und Aktivitäten werden für eine spezifische Mbox ausgewertet. Wenn die globale Mbox beispielsweise einen bestimmten Parameter übergibt, die regionale Mbox jedoch nicht, qualifiziert sich die mit diesem Parameter verknüpfte Aktivität/Zielgruppe nicht in der regionalen Mbox.
* Das Targeting wird nicht anhand interner Mbox-Parameter wie mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId und mboxVersion ausgewertet.

## Schulungsvideo: Erstellen von Audiencen ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
