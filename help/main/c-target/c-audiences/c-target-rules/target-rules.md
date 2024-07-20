---
keywords: Targeting; Zielkategorien; Targeting-Bedingungen; Zielgruppenmanager; benutzerdefinierte Profilparameter; Besucherprofil; benutzerdefinierte Benutzerparameter; Zielregeln
description: Erfahren Sie, wie Sie mit Kategorien (wie Browser, Geo, Netzwerk, Betriebssystem, Besucherprofil) Inhalte gezielt ansprechen können.
title: Welche Kategorien gibt es für Zielgruppen?
feature: Audiences
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 47%

---

# Kategorien für Zielgruppen

Mit [!DNL Adobe Target] können Sie ein Targeting für mehrere Kategorieattribute durchführen. Um Targeting-Regeln (oder Gruppen) für jedes Attribut zu erstellen, ziehen Sie die gewünschten Attribute in den Bereich Audience Builder .

![Attribute für Zielgruppen](/help/main/c-target/c-audiences/assets/attributes.png)

Wenn eine bestimmte Kategorie ausgewählt ist, können Sie eine oder mehrere Targeting-Bedingungen anwenden. In der Kategorie „Geo“ können Sie beispielsweise eine Regel wie „City=San Francisco“ definieren. Wenn Sie mehrere Werte eingeben, wird eine OR-Bedingung erstellt. Für den Besucher muss nur einer dieser Werte zutreffen, um die Targeting-Bedingung zu erfüllen. Für UND-Bedingungen desselben Parameters erstellen Sie ein benutzerspezifisches Ausdrucksziel.

Nachdem Sie eine Regel erstellt haben, klicken Sie auf **[!UICONTROL Done]**. Neben dem Targeting-Link für die Ebene, auf die sich das Targeting bezieht, wird eine Zusammenfassung der Regel angezeigt.

Sie können eine Regel verfeinern, indem Sie ihr zusätzliche Bedingungen hinzufügen oder zusätzliche Regeln in anderen Kategorien erstellen. Sie können beispielsweise nur Firefox-Benutzer aus San Francisco ansprechen, die über Google auf Ihre Site zugreifen. Legen Sie die Kategorie &quot;[!UICONTROL Geo]&quot; auf Benutzer aus San Francisco, die Kategorie &quot;[!UICONTROL Browser]&quot; auf Benutzer, die Firefox verwenden, und die Kategorie &quot;[!UICONTROL Traffic Sources]&quot;auf Benutzer ab [!UICONTROL From Google] fest. Die kategorienübergreifenden Regeln werden mit dem UND -Operator kombiniert.

Erstellen Sie ein Ausdrucksziel, um komplexe Targeting-Regeln zu erstellen, die OR-Vorgänge über Kategorien hinweg enthalten.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Hinzufügen einer Zielgruppe **[!UICONTROL Visitor Profile]** in den Arbeitsbereich und wählen Sie dann den Parameter aus, den Sie zum Targeting Ihrer Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

Benutzen Sie das Suchfeld, um Ihre [!UICONTROL Audiences] Liste zu durchsuchen. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die Liste [!UICONTROL Audience] nach Zielgruppennamen oder dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
