---
keywords: Targeting; Zielkategorien; Targeting-Bedingungen; Zielgruppenmanager; benutzerdefinierte Profilparameter; Besucherprofil; benutzerdefinierte Benutzerparameter; Zielregeln
description: Erfahren Sie, wie Sie mit Kategorien (wie Browser, Geo, Netzwerk, Betriebssystem, Besucherprofil) Inhalte gezielt ansprechen können.
title: Welche Kategorien gibt es für Zielgruppen?
feature: Zielgruppen
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 50%

---

# Kategorien für Zielgruppen

Mit [!DNL Adobe Target] können Sie ein Targeting für eine oder mehrere Kategorieattribute durchführen. Um Targeting-Regeln (oder Gruppen) für jedes Attribut zu erstellen, ziehen Sie die gewünschten Attribute in den Audience Builder .

![Attribute für Zielgruppen](/help/c-target/c-audiences/assets/attributes.png)

Wenn eine bestimmte Kategorie ausgewählt ist, können Sie eine oder mehrere Targeting-Bedingungen anwenden. In der Kategorie „Geo“ können Sie beispielsweise eine Regel wie „City=San Francisco“ definieren. Wenn Sie mehrere Werte eingeben, wird eine OR-Bedingung erstellt. Für den Besucher muss nur einer dieser Werte zutreffen, um die Targeting-Bedingung zu erfüllen. Für UND-Bedingungen desselben Parameters erstellen Sie ein benutzerspezifisches Ausdrucksziel.

Nachdem Sie eine Regel erstellt haben, klicken Sie auf **[!UICONTROL Fertig]**. Neben dem Targeting-Link für die Ebene, auf die sich das Targeting bezieht, wird eine Zusammenfassung der Regel angezeigt.

Sie können eine Regel verfeinern, indem Sie ihr zusätzliche Bedingungen hinzufügen oder zusätzliche Regeln in anderen Kategorien erstellen. Sie können beispielsweise nur Firefox-Benutzer aus San Francisco ansprechen, die über Google auf Ihre Site zugegriffen haben. Legen Sie die Kategorie [!UICONTROL Geo] fest, um Benutzer aus San Francisco als Ziel festzulegen, die Kategorie [!UICONTROL Browser] für Benutzer, die Firefox verwenden, und die Kategorie [!UICONTROL Traffic-Quellen] , um Benutzer anzusprechen, die von [!UICONTROL Google] kommen. Die kategorienübergreifenden Regeln werden mit dem UND -Operator kombiniert.

Erstellen Sie ein Ausdrucksziel, um komplexe Targeting-Regeln zu erstellen, die OR-Vorgänge über Kategorien hinweg enthalten.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Hinzufügen einer Zielgruppe **[!UICONTROL Besucherprofil]** in den Arbeitsbereich und wählen Sie dann den Parameter aus, den Sie zum Targeting Ihrer Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

Durchsuchen Sie die [!UICONTROL Zielgruppenliste] über das Suchfeld. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die Liste [!UICONTROL Zielgruppe] nach Zielgruppennamen oder dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
