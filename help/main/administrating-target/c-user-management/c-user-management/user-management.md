---
keywords: Benutzer hinzufügen;Benutzer verwalten;Benutzerberechtigungen
description: Erfahren Sie, wie Sie mit der  [!DNL Adobe Admin Console]  Benutzende und deren Berechtigungen in  [!DNL Adobe Target Standard] verwalten können.
title: Wie kann ich für ein  [!DNL Target Standard] -Konto Benutzende hinzufügen und Berechtigungen verwalten?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 63%

---

# Benutzende

Fügen Sie Benutzende hinzu und verwalten Sie ihre Berechtigungen in der [!DNL Adobe Admin Console] für ein [!DNL Target Standard]-Konto.

>[!NOTE]
>
>[!UICONTROL Properties]- und [!UICONTROL Permissions] sind als Teil der [!DNL Target Premium]-Lösung verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>
>Sie können feststellen, ob Ihr Unternehmen über eine [!UICONTROL Standard] oder [!UICONTROL Premium] Lizenz verfügt, indem Sie auf den [!UICONTROL Administration] Link oben in der [!DNL Target] Benutzeroberfläche klicken.
>
>* **[!DNL Target]&#x200B;[!UICONTROL Standard] Kunden**: Wenn Sie die Registerkarte &quot;[!UICONTROL Users]&quot; ([!UICONTROL Administration > Users]) sehen (und nicht die Registerkarte &quot;**[!UICONTROL Properties]** [!DNL Target]„), verfügt Ihr Unternehmen über eine [!UICONTROL Standard]. [!DNL Target] [!UICONTROL Standard] Kunden sollten die Anweisungen in diesem Artikel befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>* **[!DNL Target]Premium-Kunden**: Wenn Sie die Registerkarte &quot;[!UICONTROL Users]&quot; und die Registerkarte &quot;[!UICONTROL Properties]&quot; ([!UICONTROL Administration > Properties]) sehen, verfügt Ihr Unternehmen über eine [!DNL Target] Premium-Lizenz. [!DNL Target] Premium-Kunden sollten den Anweisungen unter [Berechtigungen für Unternehmensbenutzer](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) und [Konfigurieren von Unternehmensberechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) folgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>Detaillierte Informationen zum Verwalten von Benutzern und Berechtigungen finden Sie im Abschnitt [Produkte und Profile verwalten](https://helpx.adobe.com/de/enterprise/using/manage-products-and-profiles.html) im *Benutzerhandbuch für Unternehmen und Teams*.

Wenn Sie [!DNL Adobe Target] zum ersten Mal verwenden, sind bereits IDs (mit der Endung Adobe.com) in Ihrem [!DNL Adobe Experience Cloud]-Konto vorhanden. Diese IDs sind für Mitglieder des [!DNL Adobe]-Teams gedacht, damit Ihnen diese bei Bedarf mit Ihrem neuen Konto und der Verwendung von [!DNL Adobe Target] helfen können. Wenn Sie Unterstützung benötigen, wenden Sie sich auf dem üblichen Weg an Ihre Teams von Adobe.

Auf der Seite [!UICONTROL Users] werden erst dann neue Benutzer angezeigt, wenn sie sich mit ihrem [!DNL Adobe Experience Cloud] Konto anmelden und sich anschließend bei [!DNL Target] anmelden.

Standardmäßig beginnen alle [!DNL Target] Benutzer mit [!UICONTROL Observer] Berechtigungen.

Admin-Benutzer sind in der [!UICONTROL Users]-Liste aufgeführt. Kontaktieren Sie einen dieser Systemadministratoren, wenn Sie Ihre Zugriffsebene ändern lassen möchten.

## Anzeigen von Benutzerinformationen in [!DNL Target]

Sie können eine Liste Ihrer aktuellen Benutzenden auf der [!DNL Target]-Benutzeroberfläche anzeigen, einschließlich der Rollen pro Arbeitsbereich und E-Mail-Adressen.

Um die [!UICONTROL Users] anzuzeigen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Users]**.

>[!NOTE]
>
>Um einen vorhandenen Benutzer zu verwalten oder neue Benutzer hinzuzufügen, müssen Sie den [!UICONTROL Adobe Admin Console] wie unten beschrieben verwenden.

## Zugreifen auf die [!DNL Adobe Admin Console] {#access}

Greifen Sie auf die [!DNL Adobe Admin Console] zu, indem Sie die folgenden Schritte durchführen:

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]**.

   Oder

   Navigieren Sie zu [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) und melden Sie sich mit Ihrer Adobe ID an, falls Sie dies noch nicht getan haben.

1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Hinzufügen von Benutzern {#add-users}

Die gesamte Benutzerverwaltung muss in der [!DNL Adobe Admin Console for Enterprise] erfolgen. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Users]** > **[!UICONTROL Users]** , um neue Benutzende zu erstellen oder bestehende Benutzende zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Erstellen von Benutzergruppen {#user-groups}

Sie können Benutzergruppen wie Entwickelnde, Analytiker, Marketing-Fachleute, Führungskräfte usw. erstellen und ihnen dann Benutzerrechte für verschiedene [!DNL Adobe]-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für mehrere [!DNL Adobe]-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. Admin Console [Klicken Sie in der &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Users]** > **[!UICONTROL User Groups]** , um neue Benutzergruppen zu erstellen oder bestehende Gruppen zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Festlegen von Rollen und Berechtigungen {#roles-permissions}

Benutzerrollen können in [!DNL Target] nur von Systemadministratoren festgelegt werden. Ein [!UICONTROL Standard] Genehmiger kann einen Beobachter beispielsweise nicht in einen Genehmiger ändern, ohne zusätzlich über [!DNL Experience Cloud] Administratorrechte zu verfügen.

Systemadministratoren müssen Benutzer zum System hinzufügen. Benutzer werden nicht automatisch hinzugefügt. Sie werden per E-Mail über [!DNL Experience Cloud] eingeladen und müssen ihre E-Mail-Adressen bestätigen, damit ihre Konten registriert werden.

>[!NOTE]
>
>Um Aktivitäten in [!DNL Target] anzeigen zu können, müssen Benutzende einem Arbeitsbereich direkt zugewiesen sein, der mindestens über die Rolle [!UICONTROL Observer] verfügt. Die Zuweisung über Benutzergruppen allein ist unzureichend. Es wird allgemein empfohlen, Benutzern Zugriff auf den Standardarbeitsbereich zu gewähren.

1. Admin Console [Klicken Sie in der &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Products]** und wählen Sie dann den Namen des gewünschten Produkts aus.

1. Klicken Sie auf den gewünschten Arbeitsbereich (z. B. Standardarbeitsbereich).

   Auf der Registerkarte [!UICONTROL Users] werden alle Benutzenden in diesem Arbeitsbereich angezeigt.

1. Wählen Sie das gewünschte Berechtigungsniveau ([!UICONTROL Approver], [!UICONTROL Editor], [!UICONTROL Observer] oder [!UICONTROL Publisher]) aus, indem Sie in der [!UICONTROL Product Role] Spalte das entsprechende Dropdown-Menü nutzen.

   | Rolle | Beschreibung |
   |--- |--- |
   | [!UICONTROL Approver] | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | [!UICONTROL Editor] | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | [!UICONTROL Observer] | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | [!UICONTROL Publisher] | Ähnlich wie die Rolle [!UICONTROL Observer] (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Die Rolle [!UICONTROL Publisher] verfügt jedoch zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

Weitere Informationen finden Sie unter [Verwalten von Produktberechtigungen und Rollen in der Admin Console](https://helpx.adobe.com/de/enterprise/help/manage-permissions-and-roles.html) im *Enterprise-Benutzerhandbuch*.

## Schulungsvideo: Konfigurieren von Adobe Target-Arbeitsbereichen ![Tutorial-Badge](/help/main/assets/tutorial.png)

Lernziele:

* Auf die Adobe Admin Console über die Adobe Target-Schnittstelle (3 Methoden) zugreifen
* Konfigurieren eines Workspace in Adobe Admin Console
   * Hinzufügen von Benutzern zu Arbeitsbereichen
   * Hinzufügen von Eigenschaften zu Arbeitsbereichen
* Grundlegende Informationen zu Standardarbeitsbereichen

>[!NOTE]
>
>Die Benutzeroberfläche des [!DNL Target] [!UICONTROL Administration]-Menüs (früher [!UICONTROL Setup]) wurde überarbeitet, um eine verbesserte Leistung zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu reduzieren und das Benutzererlebnis im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind im Allgemeinen korrekt, allerdings können sich Optionen an etwas anderen Orten befinden. Aktualisierte Videos werden bald veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
