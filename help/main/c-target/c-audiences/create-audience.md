---
keywords: Zielgruppe; Zielgruppenregeln; Zielgruppe erstellen; Erstellen von Zielgruppen
description: Erfahren Sie, wie Sie benutzerdefinierte Zielgruppen erstellen und sie zur Verwendung in Aktivitäten in der Bibliothek [!DNL Adobe Target] [!UICONTROL Audiences] speichern.
title: Wie erstelle ich Zielgruppen?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
source-git-commit: a185edee86f6d07b488cf5dd3fe7e5dc3f4e87b3
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 58%

---

# Erstellen von Zielgruppen in [!DNL Target]

Sie können benutzerdefinierte Zielgruppen erstellen und sie zur Verwendung in Ihren Aktivitäten in der Bibliothek [!DNL Adobe Target] [!UICONTROL Audiences] speichern. Sie können auch eine vorhandene Zielgruppe kopieren und dann bearbeiten, um eine ähnliche Zielgruppe zu erstellen und mehrere Zielgruppen zu kombinieren.

## Zielgruppenüberblick

Zielgruppen werden durch Regeln definiert, die bestimmen, wer in eine [!DNL Target]-Aktivität eingeschlossen und wer davon ausgeschlossen wird. Eine Zielgruppendefinition kann mehrere Regeln enthalten, wobei die einzelnen Regeln wiederum mehrere Parameter aufweisen können. Komplexe Zielgruppendefinitionen greifen auf die booleschen Operatoren „AND“ und „OR“ zurück, um Regeln und Parameter zu kombinieren und Ihnen so weitreichende Kontrolle darüber zu geben, welche Websitebesucher als Aktivitätsteilnehmer gezählt werden.

Wenn Sie Regeln oder Parameter mit UND kombinieren, muss jedes potenzielle Zielgruppenmitglied die *Alle* definierten Bedingungen erfüllen, damit es als Teilnehmer aufgenommen wird. Wenn Sie zum Beispiel eine Betriebssystemregel und eine Browserregel definieren, werden nur die Besucher, die sowohl das definierte Betriebssystem *als auch* den definierten Browser verwenden, in die Aktivität aufgenommen.

Wenn Sie Regeln oder Parameter mit „OR“ kombinieren, müssen die Mitglieder der Zielgruppe nur eine der definierten Bedingungen erfüllen, damit sie als Teilnehmer gezählt werden. Wenn Sie zum Beispiel mehrere Regeln für Mobilgeräte definieren, die mit „OR“ verbunden sind, werden Besucher, die *ein beliebiges* Kriterium erfüllen, in die Aktivität eingeschlossen.

Sie können die beiden booleschen Operatoren auch mischen und so komplexe Regeln schaffen, allerdings müssen Operatoren auf derselben Regelebene übereinstimmen. Die Benutzeroberfläche wendet automatisch den richtigen Operator an.

Die folgende Regel nimmt eine Ausrichtung auf Besucher vor, die entweder Chrome *oder* Firefox auf einem Windows-Computer nutzen:

![Zielgruppe erstellen](assets/audience_create.png)

>[!NOTE]
>
>Achten Sie darauf, dass Ihre Regeln nicht alle Mitglieder der Zielgruppe ausschließen. So ist es beispielsweise nicht möglich, dass ein Besucher eine Seite mit Chrome *und* gleichzeitig mit Firefox besucht.

## Erstellen von Zielgruppen

1. Klicken Sie in der oberen Menüleiste auf **[!UICONTROL Audiences]** .

   ![Bild &quot;audiences_list&quot;](assets/audiences_list.png)

1. Klicken Sie in der Liste [!UICONTROL Audiences] auf **[!UICONTROL Create Audience]**.

   Oder

   Um eine vorhandene Zielgruppe zu kopieren, klicken Sie in der Liste [!UICONTROL Audiences] auf das Symbol **[!UICONTROL More Actions]** (das Auslassungssymbol) und dann auf **[!UICONTROL Duplicate]**. Sie können die Zielgruppe anschließend bearbeiten, um eine ähnliche Zielgruppe zu erstellen.

1. Geben Sie einen eindeutigen, beschreibenden Zielgruppennamen und eine optionale Beschreibung ein.

   Zielgruppennamen dürfen nicht mit den folgenden Zeichen beginnen:

   `=  +  -  !  @`

   Zielgruppennamen dürfen keine der folgenden Zeichensequenzen enthalten:

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. Ziehen Sie die gewünschten Attribute aus der Liste **[!UICONTROL Attributes]** rechts in den Bereich Audience Builder .

   ![Attribute per Drag-and-Drop verschieben](assets/drag-attribute.png)

   Jeder Regeltyp hat eigene Parameter. Weitere Informationen zum Konfigurieren der einzelnen Typen von Zielgruppenregeln finden Sie unter [Kategorien für Zielgruppen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D).

1. Definieren Sie die Regelparameter.

   Die folgende Zielgruppe beispielsweise richtet sich an Besucher aus Utah, die das Macintosh-Betriebssystem verwenden.

   ![Update/Macintosh audience](assets/adience-builder.png)

1. (Bedingt) Fahren Sie mit dem Hinzufügen und Definieren der gewünschten Attribute fort.

   Um einen weiteren Behälter zu erstellen, klicken Sie auf **[!UICONTROL Add container]** oder ziehen Sie einfach ein anderes Attribut in den Bereich Audience Builder . Der Operator (AND oder OR) kann dann über die Dropdown-Liste angepasst werden.

1. Klicken Sie auf **[!UICONTROL Done]**.

   Neu erstellte Zielgruppen werden erst nach einigen Sekunden Verarbeitungszeit in der Liste angezeigt. Falls die Zielgruppe nicht sofort in der Liste angezeigt wird, können Sie danach suchen oder die Liste aktualisieren.

## Schulungsvideo: Erstellen von Zielgruppen ![Badge &quot;Überblick&quot;](/help/main/assets/overview.png)

Dieses Video enthält Informationen zur Erstellung von Zielgruppen.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
