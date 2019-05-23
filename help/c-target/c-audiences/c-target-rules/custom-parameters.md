---
description: Benutzerdefinierte Parameter sind Mbox-Parameter. Wenn Sie Mbox-Parameter an Mboxes übergeben oder die Funktion „targetPageParams“ verwenden, werden diese Parameter hier angezeigt und können in Zielgruppen verwendet werden.
keywords: benutzerdefinierte Parameter; Targeting von benutzerdefinierten Parametern; Targeting von Seitenparametern; Targeting von Mbox-Parametern
seo-description: Benutzerdefinierte Parameter sind Mbox-Parameter. Wenn Sie Mbox-Parameter an Mboxes übergeben oder die Funktion „targetPageParams“ verwenden, werden diese Parameter hier angezeigt und können in Zielgruppen verwendet werden.
seo-title: Benutzerdefinierte Parameter
solution: Target
title: Benutzerdefinierte Parameter
topic: Standard
uuid: a9eb62a6-e86a-4e7b-922c-ad87570435ba
translation-type: tm+mt
source-git-commit: f59e96cd5afcae9d27d730aecead9eb360f04026

---


# Benutzerdefinierte Parameter{#custom-parameters}

Benutzerdefinierte Parameter sind Mbox-Parameter. Wenn Sie Mbox-Parameter an Mboxes übergeben oder die Funktion „targetPageParams“ verwenden, werden diese Parameter hier angezeigt und können in Zielgruppen verwendet werden.

Weitere Informationen finden Sie im Abschnitt [Übergeben von Parameter an eine globale mbox](https://marketing.adobe.com/resources/help/en_US/target/ov/c_pass_parameters_to_global_mbox.html).

Wenn Sie eine benutzerdefinierte Zielgruppe basierend auf einem erstellen, erhalten Sie von `mboxParameter`mboxParameter keine Aufforderung mehr, `mboxName` einzugeben. Der Mbox-Name ist nun optional. Mit dieser Änderung können Sie Parameter aus mehreren Mboxes verwenden oder auf einen Parameter verweisen, der noch nicht am Rand aufgezeichnet wurde.

So wählen Sie den gewünschten Parameter aus:

* Wählen Sie beim Erstellen einer neuen Zielgruppe einen Parameter aus der Liste aus oder geben Sie die ersten Buchstaben des Parameternamens bzw. den gesamten Namen des gewünschten Parameters ein.
* Wenn Sie den Mbox-, aber nicht den Parameternamen kennen, filtern Sie mithilfe des Kontrollkästchens nach der bekannten Mbox, die den gewünschten Parameter übergibt.

Bei keiner der Methoden gibt es eine Verbindung zwischen Mbox und Parameter. Die Zielgruppe funktioniert basierend auf dem Parameter über alle Mboxes hinweg, die diesen Parameter übergeben.

Wenn Sie eine bestehende Zielgruppe bearbeiten, werden die Filterkriterien mit dem Mbox-Namen angezeigt, der bei der Erstellung angegeben wurde.

Die [Popupkarte mit Definitionsdetails](../../../c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) der Zielgruppe enthält den Parameternamen im Abschnitt „Regeln“. Auf die Mbox, die zum Filtern verwendet wird, wird nicht verwiesen.

>[!NOTE]
>
>Für benutzerdefinierte Zielgruppen, die vor der Target-Version 18.5.1 (22. Mai 2018) erstellt wurden, werden in der Popup-Karte für die Zielgruppendefinition keine Mbox-Namen angezeigt. Sie müssen die benutzerdefinierte Zielgruppe erneut speichern, damit der Mbox-Name auf der Karte angezeigt wird.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)