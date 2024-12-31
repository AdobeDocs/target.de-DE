---
keywords: Targeting; Zielkategorien; Targeting-Bedingungen; Zielgruppenmanager; benutzerdefinierte Profilparameter; Besucherprofil; benutzerdefinierte Benutzerparameter; Zielregeln
description: Erfahren Sie, wie Sie Kategorien (wie Browser, Geografie, Netzwerk, Betriebssystem, Besucherprofil) verwenden können, um Inhalte anzusprechen.
title: Welche Kategorien gibt es für Zielgruppen?
feature: Audiences
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 47%

---

# Kategorien für Zielgruppen

Mit [!DNL Adobe Target] können Sie auf jedes beliebige Kategorieattribut abstimmen. Um Targeting-Regeln (oder -Gruppen) für jedes Attribut zu erstellen, ziehen Sie die gewünschten Attribute per Drag-and-Drop in den Audience Builder-Bereich.

![Attribute für Zielgruppen](/help/main/c-target/c-audiences/assets/attributes.png)

Wenn eine bestimmte Kategorie ausgewählt ist, können Sie eine oder mehrere Targeting-Bedingungen anwenden. In der Kategorie „Geo“ können Sie beispielsweise eine Regel wie „City=San Francisco“ definieren. Wenn Sie mehrere Werte eingeben, wird eine OR-Bedingung erstellt. Für den Besucher muss nur einer dieser Werte zutreffen, um die Targeting-Bedingung zu erfüllen. Für UND-Bedingungen desselben Parameters erstellen Sie ein benutzerspezifisches Ausdrucksziel.

Nachdem Sie eine Regel erstellt haben, klicken Sie auf **[!UICONTROL Done]**. Neben dem Targeting-Link für die Ebene, auf die sich das Targeting bezieht, wird eine Zusammenfassung der Regel angezeigt.

Sie können eine Regel verfeinern, indem Sie ihr zusätzliche Bedingungen hinzufügen oder zusätzliche Regeln in anderen Kategorien erstellen. Sie können beispielsweise nur Firefox-Benutzer aus San Francisco ansprechen, die über Google auf Ihre Site zugreifen. Legen Sie die Kategorie [!UICONTROL Geo] fest, um Benutzende aus San Francisco anzusprechen, die Kategorie [!UICONTROL Browser], um Benutzende mit Firefox anzusprechen, und die Kategorie [!UICONTROL Traffic Sources], um Benutzende aus [!UICONTROL From Google] anzusprechen. Die kategorieübergreifend erstellten Regeln werden mit dem AND-Operator kombiniert.

Um komplexe Zielgruppenbestimmungsregeln zu erstellen, die OR-Vorgänge kategorieübergreifend enthalten, erstellen Sie ein Ausdrucksziel.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Hinzufügen einer Zielgruppe per Drag-and-Drop **[!UICONTROL Visitor Profile]** und wählen Sie dann den Parameter aus, den Sie für Ihre Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

Verwenden Sie das Suchfeld, um Ihre [!UICONTROL Audiences] zu durchsuchen. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Audience] nach Zielgruppenname oder nach dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
