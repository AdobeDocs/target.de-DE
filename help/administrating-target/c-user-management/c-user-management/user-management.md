---
description: In der Adobe Admin Console können Sie Benutzer hinzufügen und ihre Berechtigungen verwalten.
keywords: Benutzer hinzufügen;Benutzer verwalten;Benutzerberechtigungen
seo-description: In der Adobe Admin Console können Sie Benutzer hinzufügen und ihre Berechtigungen verwalten.
seo-title: Benutzer
solution: Target
subtopic: Erste Schritte
title: Benutzer
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: dda07f19bddb870b20dabc484a1b97d55bcc5775

---


# Benutzer{#users}

In der Adobe Admin Console können Sie Benutzer hinzufügen und ihre Berechtigungen verwalten.

>[!NOTE]
>
>Die Funktionalitäten für [!UICONTROL Eigenschaften] und [!UICONTROL Berechtigungen] sind als Bestandteil der Lösung [!DNL Target] Premium verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>Sie können feststellen, ob Ihre Organisation über eine Standard- oder Premium-Lizenz verfügt, indem Sie am oberen Rand der [!DNL Target]-Benutzeroberfläche auf den Link [!UICONTROL Einrichten] klicken.
>
>**[!DNL Target]Standard-Kunden:** Wenn die Registerkarte [!UICONTROL Benutzer] ([!UICONTROL Einrichten &gt; Benutzer]) angezeigt wird, hat Ihre Organisation eine [!DNL Target]-Standard-Lizenz. [!DNL Target Standard-Kunden sollten die Anweisungen in diesem Artikel befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen. 
>
>**[!DNL Target]Premium-Kunden:** Wenn die Registerkarte [!UICONTROL Eigenschaften] ([!UICONTROL Einrichten &gt; Eigenschaften]) angezeigt wird, hat Ihre Organisation eine [!DNL Target]-Premium-Lizenz. [!DNL Target] Premium-Kunden sollten den Anweisungen unter [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md) und [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) folgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.

Nur Systemadministratoren können Benutzer hinzufügen und deren Zugriffsrechte verwalten. Die Systemadministratorrolle wird auf der Ebene von [!DNL Experience Cloud] zugewiesen. [!DNL Experience Cloud]-Rollen sind separat von den in den einzelnen Lösungen verwalteten Rollen.

Wenn Sie [!DNL Adobe Target] zum ersten Mal verwenden, sind bereits IDs (mit der Endung Adobe.com) in Ihrem [!DNL Adobe Experience Cloud]-Konto vorhanden. Diese IDs sind für Mitglieder des Adobe-Teams gedacht, um Ihnen mit Ihrem neuen Konto und der Verwendung des neuen [!DNL Adobe Target] helfen zu können, sollte dies erforderlich sein. Wenn Sie Unterstützung benötigen, wenden Sie sich auf dem üblichen Weg an Ihre Teams von Adobe.

Die neuen Benutzer werden nicht in der [!UICONTROL Benutzerliste] aufgeführt, bis sich der jeweilige Benutzer bei seinem Adobe Experience Cloud-Konto anmeldet und sich anschließend in [!DNL Target Standard/Premium] anmeldet, indem er auf die [!DNL Target]-Karte klickt.

Standardmäßig ist allen [!DNL Target]-Benutzern die Berechtigung „Beobachter“ zugewiesen.

Systemadministratoren sind in der Liste der Benutzer aufgeführt. Kontaktieren Sie einen dieser Systemadministratoren, wenn Sie Ihre Zugriffsebene ändern lassen möchten.

## Auf die Adobe Admin Console zugreifen {#section_79796E0227D048F59BAE0AB02E544EBE}

Greifen Sie für in der Adobe Admin Console ausgeführte Aufgaben auf die Konsole zu, indem Sie die folgenden Schritte durchführen:

1. Navigieren Sie zu [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) und melden Sie sich mit Ihrer Adobe ID an, falls Sie noch nicht angemeldet sein sollten.

   Oder

   Wenn Sie bereits bei der Experience Cloud angemeldet sind, rufen Sie [https://www.experiencecloud.adobe.com](https://experiencecloud.adobe.com)auf und klicken Sie dann auf das [!UICONTROL App] -Symbol in der oberen Navigationsleiste &gt; Klicken **[!UICONTROL Sie rechts auf Admin]** .

1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Benutzer hinzufügen {#section_A92AF0F921B743FEB9E9033433BD816A}

Die gesamte Benutzerverwaltung muss in der [!DNL Adobe Admin Console for Enterprise] erfolgen. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der Admin-Konsole](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)auf **[!UICONTROL Benutzer]** &gt; **[!UICONTROL Benutzer]** , um neue Benutzer zu erstellen oder bestehende Benutzer zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in der Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) im *Enterprise-Benutzerhandbuch*.

## Benutzergruppen erstellen {#section_5F5CB9AA7A9F4D26953E22016DA59605}

Sie können Benutzergruppen wie Entwickler, Analytiker, Marketingexperten, Manager usw. erstellen und ihnen dann Benutzerrechte für verschiedene Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. [Klicken Sie in der Admin-Konsole](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)auf **[!UICONTROL Benutzer]** &gt; **[!UICONTROL Benutzergruppen]** , um neue Benutzergruppen zu erstellen oder bestehende Gruppen zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in der Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) im *Enterprise-Benutzerhandbuch*.

## Rollen und Berechtigungen festlegen {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

Benutzerrollen können in [!DNL Target] nur von Systemadministratoren festgelegt werden. Beispielsweise kann ein Standard-Benutzer mit der Rolle „Genehmigen“ keinen Beobachter zu einer genehmigenden Person ändern, ohne auch Experience Cloud-Administratorrechte zu haben.

Systemadministratoren müssen Benutzer zum System hinzufügen. Benutzer werden nicht automatisch hinzugefügt. Sie werden per E-Mail von Experience Cloud eingeladen und müssen ihre E-Mail-Adressen bestätigen, bevor ihre Konten registriert werden.

1. [Klicken Sie in der Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Registerkarte &quot;Produkte «](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Klicken Sie auf den Namen der gewünschten Konfiguration.
1. Klicken Sie auf **[!UICONTROL Benutzer]**.

   Auf der [!UICONTROL Registerkarte &quot;Benutzer] &quot; werden alle Benutzer in diesem Arbeitsbereich angezeigt.

   ![Konfigurationsbenutzer](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new.png)

1. Wählen Sie die gewünschte Berechtigungsrolle (Beobachter, Editor oder Genehmiger) aus, indem Sie in der Spalte [!UICONTROL Produktrolle] die entsprechende Dropdownliste nutzen.

   | Rolle | Beschreibung |
   |--- |--- |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Editor | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |

Weitere Informationen finden Sie unter [Verwalten von Produktberechtigungen und Rollen in der Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) im *Enterprise-Benutzerhandbuch*.

## Schulungsvideo: So konfigurieren Sie Target-Arbeitsflächen

Lernziele:

* Zugriff auf die Adobe Admin-Konsole über die Adobe Target-Oberfläche (drei Möglichkeiten)
* Arbeitsbereich in der Adobe Admin-Konsole konfigurieren
   * Hinzufügen von Benutzern zu Arbeitsbereichen
   * Hinzufügen von Eigenschaften zu Arbeitsbereichen
* Grundlegende Informationen zu Standardarbeitsbereichen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
