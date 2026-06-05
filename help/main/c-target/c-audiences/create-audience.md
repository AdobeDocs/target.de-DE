---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen
description: Erfahren Sie, wie Sie benutzerdefinierte Zielgruppen erstellen und sie in der Bibliothek  [!DNL Adobe Target] [!UICONTROL Audiences] zur Verwendung in Aktivitäten speichern.
title: Wie erstelle ich Zielgruppen?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
TQID: https://experienceleague.adobe.com/-t5UqbGCl2EwCyScCq1B8X9bWxQQYWSd0e7RBoUoYQg
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 538
ht-degree: 50%

---

# Erstellen von Zielgruppen in [!DNL Target]

Erstellen Sie benutzerdefinierte Zielgruppen und speichern Sie sie in der [!DNL Adobe Target] [!UICONTROL Zielgruppen]-Bibliothek zur Verwendung in Ihren Aktivitäten. Sie können auch eine vorhandene Zielgruppe kopieren, die Sie dann bearbeiten können, um eine ähnliche Zielgruppe zu erstellen und mehrere Zielgruppen zu kombinieren.

## Zielgruppenüberblick

Zielgruppen werden durch Regeln definiert, die bestimmen, wer in eine [!DNL Target]-Aktivität eingeschlossen und wer davon ausgeschlossen wird. Eine Zielgruppendefinition kann mehrere Regeln enthalten, wobei die einzelnen Regeln wiederum mehrere Parameter aufweisen können. Komplexe Zielgruppendefinitionen greifen auf die booleschen Operatoren „AND“ und „OR“ zurück, um Regeln und Parameter zu kombinieren und Ihnen so weitreichende Kontrolle darüber zu geben, welche Websitebesucher als Aktivitätsteilnehmer gezählt werden.

Wenn Sie Regeln oder Parameter mit UND kombinieren, muss jedes potenzielle Mitglied der Zielgruppe *alle* definierten Bedingungen erfüllen, damit es als Teilnehmer aufgenommen werden kann. Wenn Sie zum Beispiel eine Betriebssystemregel und eine Browserregel definieren, werden nur die Besucher, die sowohl das definierte Betriebssystem *als auch* den definierten Browser verwenden, in die Aktivität aufgenommen.

Wenn Sie Regeln oder Parameter mit „OR“ kombinieren, müssen die Mitglieder der Zielgruppe nur eine der definierten Bedingungen erfüllen, damit sie als Teilnehmer gezählt werden. Wenn Sie zum Beispiel mehrere Regeln für Mobilgeräte definieren, die mit „OR“ verbunden sind, werden Besucher, die *ein beliebiges* Kriterium erfüllen, in die Aktivität eingeschlossen.

Sie können die beiden booleschen Operatoren auch mischen und so komplexe Regeln schaffen, allerdings müssen Operatoren auf derselben Regelebene übereinstimmen. Die Benutzeroberfläche wendet automatisch den richtigen Operator an.

Die folgende Regel richtet sich beispielsweise an Besucherinnen und Besucher, die [!DNL Chrome]- *-*-[!DNL Firefox] auf einem [!DNL Windows] verwenden:

![Zielgruppe erstellen](assets/audience_create.png)

>[!NOTE]
>
>Achten Sie darauf, dass Ihre Regeln nicht alle Mitglieder der Zielgruppe ausschließen. Beispielsweise ist es nicht möglich, dass jemand eine Seite gleichzeitig mit [!DNL Chrome] *und* [!DNL Firefox] besucht.

## Erstellen von Zielgruppen

1. Klicken Sie **[!UICONTROL Zielgruppen]** in der oberen Menüleiste.

   ![Audiences_list image](assets/audiences_list.png)

1. Klicken Sie in [!UICONTROL  Liste ]Zielgruppen“ auf **[!UICONTROL Zielgruppe erstellen]**.

   Oder

   Um eine vorhandene Zielgruppe zu kopieren, klicken Sie in der [!UICONTROL Zielgruppen] auf das Symbol **[!UICONTROL Mehr Aktionen]** ( ![Mehr Aktionen-Symbol](/help/main/assets/icons/MoreSmallListVert.svg) ) für die Zielgruppe, die Sie kopieren möchten, und klicken Sie dann auf **[!UICONTROL Duplizieren]**. Sie können die Zielgruppe anschließend bearbeiten, um eine ähnliche Zielgruppe zu erstellen.

1. Geben Sie einen eindeutigen, beschreibenden Zielgruppennamen und eine optionale Beschreibung ein.

   Zielgruppennamen können nicht mit den folgenden Zeichen beginnen:

   `=  +  -  !  @`

   Zielgruppennamen dürfen keine der folgenden Zeichensequenzen enthalten:

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. Ziehen Sie die gewünschten Attribute aus der Liste **[!UICONTROL Attribute]** auf der linken Seite in den Bereich Audience Builder .

   ![Attribute per Drag-and-Drop verschieben](assets/drag-attribute.png)

   Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Definieren Sie die Regelparameter.

   Die folgende Zielgruppe richtet sich beispielsweise unter dem Betriebssystem [!DNL Macintosh] an Besucher aus Utah.

   ![Zielgruppe Utah/Macintosh](assets/adience-builder.png)

1. (Bedingt) Fahren Sie mit dem Hinzufügen und Definieren der gewünschten Attribute fort.

   Um einen weiteren Container zu erstellen, klicken Sie auf **[!UICONTROL Container hinzufügen]** oder ziehen Sie einfach ein anderes Attribut in den Audience Builder-Bereich. Sie können dann den Operator (UND oder ODER) mithilfe der Dropdown-Liste anpassen.

1. Klicken Sie auf **[!UICONTROL Fertig]**.

   Neu erstellte Zielgruppen werden erst nach einigen Sekunden Verarbeitungszeit in der Liste angezeigt. Falls die Zielgruppe nicht sofort in der Liste angezeigt wird, können Sie danach suchen oder die Liste aktualisieren.

## Schulungsvideo: Erstellen von Zielgruppen ![Übersichts-Badge](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Erstellung von Zielgruppen.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
