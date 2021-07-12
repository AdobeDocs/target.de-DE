---
keywords: Benutzer hinzufügen;Benutzer verwalten;Benutzerberechtigungen
description: Erfahren Sie, wie Sie mit der Adobe Admin Console Benutzer und deren Berechtigungen in Adobe Target verwalten können.
title: Wie kann ich Benutzer hinzufügen und Berechtigungen verwalten?
feature: Administration und Konfiguration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: be7b5478006af231aae2b78e4a8c0066e3cb4a5b
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 48%

---

# Benutzer

Fügen Sie Benutzer hinzu und verwalten Sie ihre Berechtigungen im [!DNL Adobe Admin Console].

>[!NOTE]
>
>Die Funktionalitäten für [!UICONTROL Eigenschaften] und [!UICONTROL Berechtigungen] sind als Bestandteil der Lösung [!DNL Target] Premium verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>Sie können feststellen, ob Ihre Organisation über eine Standard- oder Premium-Lizenz verfügt, indem Sie oben in der [!DNL Target]-Benutzeroberfläche auf den Link [!UICONTROL Administration] klicken.
>
>* **[!DNL Target]Standardkunden**: Wenn die   Registerkarte &quot;Benutzer&quot;([!UICONTROL Administration > Benutzer]) (und nicht die Registerkarte &quot; **** Eigenschaften&quot;) angezeigt wird, verfügt Ihr Unternehmen über eine  [!DNL Target] Standardlizenz. [!DNL Target] Standard-Kunden sollten die Anweisungen in diesem Artikel befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
   >
   >
* **[!DNL Target]Premium-Kunden**: Wenn die Registerkarte   Benutzer und   Eigenschaften ([!UICONTROL Administration > Eigenschaften]) angezeigt werden, verfügt Ihr Unternehmen über eine  [!DNL Target] Premium-Lizenz. [!DNL Target] Premium-Kunden sollten den Anweisungen unter [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md) und [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) folgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>
Detaillierte Informationen zum Verwalten von Benutzern und Berechtigungen finden Sie unter [Verwalten von Produkten und Profilen](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) im *Benutzerhandbuch für Unternehmen und Teams*.

Wenn Sie [!DNL Adobe Target] zum ersten Mal verwenden, sind bereits IDs (mit der Endung Adobe.com) in Ihrem [!DNL Adobe Experience Cloud]-Konto vorhanden. Diese IDs sind für Mitglieder von [!DNL Adobe]-Teams gedacht, damit sie Sie bei Ihrem neuen Konto und bei der Verwendung von [!DNL Adobe Target] unterstützen können, falls Sie Hilfe benötigen. Wenn Sie Unterstützung benötigen, wenden Sie sich auf dem üblichen Weg an Ihre Teams von Adobe.

Der neue Benutzer wird nicht auf der Seite [!UICONTROL Benutzer] aufgeführt, bis sich der Benutzer mit seinem [!DNL Adobe Experience Cloud]-Konto anmeldet und sich anschließend bei [!DNL Target Standard/Premium] anmeldet.

Standardmäßig ist allen [!DNL Target]-Benutzern die Berechtigung „Beobachter“ zugewiesen.

Admin-Benutzer werden in der Liste [!UICONTROL Benutzer] identifiziert. Wenden Sie sich an einen Systemadministrator, wenn Sie Ihre Zugriffsstufe ändern müssen.

## Anzeigen von Benutzerinformationen aus Target

Sie können eine Liste Ihrer aktuellen Benutzer in Ihrer Target-Umgebung anzeigen, einschließlich ihrer Rollen pro Arbeitsbereich und E-Mail-Adressen direkt in Target.

Um die Seite &quot;Benutzer&quot;anzuzeigen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]**.

![Benutzerliste aus Target](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Um einen vorhandenen Benutzer zu verwalten oder neue Benutzer hinzuzufügen, müssen Sie den [!UICONTROL Adobe Admin Console] verwenden, wie unten beschrieben.

## Auf die Adobe Admin Console zugreifen {#access}

Greifen Sie für in der Adobe Admin Console ausgeführte Aufgaben auf die Konsole zu, indem Sie die folgenden Schritte durchführen:

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerverwaltung]**.

   Oder

   Gehen Sie zu [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) und melden Sie sich dann mit Ihrer Adobe ID an, falls Sie noch nicht angemeldet sind.

1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Benutzer hinzufügen {#add-users}

Die gesamte Benutzerverwaltung muss in der [!DNL Adobe Admin Console for Enterprise] erfolgen. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf  **[!UICONTROL Benutzer]**  >  **** Benutzer , um neue Benutzer zu erstellen oder bestehende Benutzer zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in der Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) im *Enterprise-Benutzerhandbuch*.

## Benutzergruppen erstellen {#user-groups}

Sie können Benutzergruppen wie Entwickler, Analytiker, Marketingexperten, Manager usw. erstellen und ihnen dann Benutzerrechte für verschiedene Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. [Klicken Sie in der Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf  **[!UICONTROL Benutzer]**  >  **[!UICONTROL Benutzergruppen]** , um neue Benutzergruppen zu erstellen oder bestehende zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in der Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) im *Enterprise-Benutzerhandbuch*.

## Rollen und Berechtigungen festlegen {#roles-permissions}

Benutzerrollen können in [!DNL Target] nur von Systemadministratoren festgelegt werden. Beispielsweise kann ein Benutzer mit Standard-Genehmigern einen Beobachter nicht in einen Genehmiger ändern, ohne auch über [!DNL Experience Cloud] Administratorrechte zu verfügen.

Systemadministratoren müssen Benutzer zum System hinzufügen. Benutzer werden nicht automatisch hinzugefügt. Sie werden per E-Mail vom [!DNL Experience Cloud] eingeladen und müssen ihre E-Mail-Adressen bestätigen, bevor ihre Konten registriert werden.

1. [Klicken Sie in der Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Registerkarte „Produkte“](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klicken Sie auf den gewünschten Arbeitsbereich (z. B. Standardarbeitsbereich).

   ![Standardarbeitsbereich](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Auf der Registerkarte [!UICONTROL Benutzer] werden alle Benutzer des Workspace aufgeführt.

   ![Konfigurationsbenutzer](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Wählen Sie das gewünschte Berechtigungsniveau (Genehmiger, Editor oder Beobachter) aus, indem Sie in der Spalte [!UICONTROL Produktrolle] das entsprechende Dropdown-Menü nutzen.

   ![Dropdownliste &quot;Produktrolle&quot;](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rolle | Beschreibung |
   |--- |--- |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Publisher | Ähnlich wie die Beobachterrolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Rolle Publisher zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

Weitere Informationen finden Sie unter [Verwalten von Produktberechtigungen und Rollen in der Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) im *Enterprise-Benutzerhandbuch*.

## Schulungsvideo: Konfigurieren von Adobe Target-Arbeitsbereichen ![Tutorial-Badge](/help/assets/tutorial.png)

Lernziele:

* Auf die Adobe Admin Console über die Adobe Target-Schnittstelle (3 Methoden) zugreifen
* Konfigurieren eines Workspace in Adobe Admin Console
   * Hinzufügen von Benutzern zu Arbeitsbereichen
   * Hinzufügen von Eigenschaften zu Arbeitsbereichen
* Grundlegende Informationen zu Standardarbeitsbereichen

>[!NOTE]
>
>Die Menübenutzeroberfläche [!DNL Target] [!UICONTROL Administration] (ehemals [!UICONTROL Setup]) wurde überarbeitet, um eine verbesserte Leistung, eine Verkürzung der Wartungszeit bei der Veröffentlichung neuer Funktionen und eine produktübergreifende Verbesserung des Benutzererlebnisses zu erzielen. Die Informationen im folgenden Video sind im Allgemeinen korrekt. -Optionen können sich jedoch an etwas anderen Orten befinden. Aktualisierte Videos werden bald veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
