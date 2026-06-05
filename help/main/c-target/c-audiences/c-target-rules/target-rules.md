---
keywords: Targeting; Zielkategorien; Targeting-Bedingungen; Zielgruppenmanager; benutzerdefinierte Profilparameter; Besucherprofil; benutzerdefinierte Benutzerparameter; Zielregeln
description: Erfahren Sie, wie Sie Kategorien (wie Browser, Geografie, Netzwerk, Betriebssystem, Besucherprofil) verwenden können, um Inhalte anzusprechen.
title: Welche Kategorien gibt es für Zielgruppen?
feature: Audiences
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
TQID: https://experienceleague.adobe.com/gdwPSImsbXfvaX2Z4bL9-hGyLwo0b0q-At0fokUfYN8
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 385
ht-degree: 50%

---

# Kategorien für Zielgruppen

Mit [!DNL Adobe Target] können Sie auf jedes beliebige Kategorieattribut abstimmen. Um Targeting-Regeln (oder -Gruppen) für jedes Attribut zu erstellen, ziehen Sie die gewünschten Attribute per Drag-and-Drop in den Audience Builder-Bereich.

![Attribute für Zielgruppen](/help/main/c-target/c-audiences/assets/attributes.png)

Wenn eine bestimmte Kategorie ausgewählt ist, können Sie eine oder mehrere Targeting-Bedingungen anwenden. In der Kategorie „Geo“ können Sie beispielsweise eine Regel wie „City=San Francisco“ definieren. Wenn Sie mehrere Werte eingeben, wird eine OR-Bedingung erstellt. Für den Besucher muss nur einer dieser Werte zutreffen, um die Targeting-Bedingung zu erfüllen. Für UND-Bedingungen desselben Parameters erstellen Sie ein benutzerspezifisches Ausdrucksziel.

Nachdem Sie eine Regel erstellt haben, klicken Sie auf **[!UICONTROL Fertig]**. Neben dem Targeting-Link für die Ebene, auf die sich das Targeting bezieht, wird eine Zusammenfassung der Regel angezeigt.

Sie können eine Regel verfeinern, indem Sie ihr zusätzliche Bedingungen hinzufügen oder zusätzliche Regeln in anderen Kategorien erstellen. Sie können beispielsweise nur Firefox-Benutzer aus San Francisco ansprechen, die über Google auf Ihre Site zugreifen. Legen Sie die Kategorie [!UICONTROL Geo] fest, um Benutzende aus San Francisco anzusprechen, die Kategorie [!UICONTROL Browser], um Benutzende mit Firefox anzusprechen, und die Kategorie [!UICONTROL Traffic-], um Benutzende aus [!UICONTROL Von Google] anzusprechen. Die kategorieübergreifend erstellten Regeln werden mit dem AND-Operator kombiniert.

Um komplexe Zielgruppenbestimmungsregeln zu erstellen, die OR-Vorgänge kategorieübergreifend enthalten, erstellen Sie ein Ausdrucksziel.

Sie können auch benutzerdefinierte Profilparameter und `user.`-Parameter als Ziel auswählen. Ziehen Sie beim Hinzufügen einer Zielgruppe **[!UICONTROL Besucherprofil]** und wählen Sie dann den Parameter aus, den Sie für Ihre Aktivität verwenden möchten. Wenn der gewünschte Parameter nicht angezeigt wird, wurde der Parameter nicht von einer Mbox ausgelöst.

Durchsuchen Sie die [!UICONTROL Zielgruppenliste] über das Suchfeld. Sie können nach einem beliebigen Teil des Zielgruppennamens suchen oder eine bestimmte Zeichenfolge in Anführungszeichen setzen.

Sie können die [!UICONTROL Audience]-Liste nach Zielgruppenname oder nach dem Datum der letzten Änderung sortieren. Wenn Sie eine Sortierung nach Name oder Datum vornehmen möchten, klicken Sie auf die Spaltenüberschrift und wählen Sie dann die Anzeige der Zielgruppen in aufsteigender oder absteigender Reihenfolge aus.

## Schulungsvideo: Erstellen von Zielgruppen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
