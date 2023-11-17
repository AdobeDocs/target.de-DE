---
keywords: Benutzer hinzufügen;Benutzer verwalten;Benutzerberechtigungen
description: Erfahren Sie, wie Sie die [!DNL Adobe Admin Console] Verwalten von Benutzern und deren Berechtigungen in [!DNL Adobe Target Standard].
title: Wie kann ich Benutzer hinzufügen und Berechtigungen verwalten für eine [!DNL Target Standard] Konto?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: d40c25f75103327e749ad864b17df926cb323be0
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 73%

---

# Benutzer

Fügen Sie Benutzer hinzu und verwalten Sie ihre Berechtigungen in der [!DNL Adobe Admin Console] für [!DNL Target Standard] -Konto.

>[!NOTE]
>
>Die Funktionen für [!UICONTROL Eigenschaften] und [!UICONTROL Berechtigungen] sind als Bestandteil der [!DNL Target Premium]-Lösung verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>
>Sie können feststellen, ob Ihre Organisation über eine [!UICONTROL Standard] oder [!UICONTROL Premium] durch Klicken auf die [!UICONTROL Administration] -Link oben im [!DNL Target] Benutzeroberfläche.
>
>* **[!DNL Target] Standard-Kunden**: Wenn Sie die Registerkarte [!UICONTROL Benutzer] sehen ([!UICONTROL Administration > Benutzer]) (und nicht die Registerkarte **[!UICONTROL Eigenschaften]**), verfügt Ihr Unternehmen über eine [!DNL Target] Standard-Lizenz.  [!DNL Target] Standard-Kunden sollten die Anweisungen in diesem Artikel befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>* **[!DNL Target]Premium-Kunden**: Wenn Sie die Registerkarte [!UICONTROL Benutzer] und die Registerkarte [!UICONTROL Eigenschaften] sehen ([!UICONTROL Administration > Eigenschaften]), verfügt Ihr Unternehmen über eine [!DNL Target] Premium-Lizenz. [!DNL Target] Premium-Kunden sollten den Anweisungen unter [Berechtigungen für Unternehmensbenutzer](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) und [Konfigurieren von Unternehmensberechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) folgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>Detaillierte Informationen zum Verwalten von Benutzern und Berechtigungen finden Sie im Abschnitt [Produkte und Profile verwalten](https://helpx.adobe.com/de/enterprise/using/manage-products-and-profiles.html) im *Benutzerhandbuch für Unternehmen und Teams*.

Wenn Sie [!DNL Adobe Target] zum ersten Mal verwenden, sind bereits IDs (mit der Endung Adobe.com) in Ihrem [!DNL Adobe Experience Cloud]-Konto vorhanden. Diese IDs sind für Mitglieder des [!DNL Adobe]-Teams gedacht, damit Ihnen diese bei Bedarf mit Ihrem neuen Konto und der Verwendung von [!DNL Adobe Target] helfen können. Wenn Sie Unterstützung benötigen, wenden Sie sich auf dem üblichen Weg an Ihre Teams von Adobe.

Neue Benutzer werden nicht auf der Seite [!UICONTROL Benutzer] Seite hinzufügen, bis sie sich mit ihren [!DNL Adobe Experience Cloud] -Konto und melden Sie sich dann bei [!DNL Target].

Standardmäßig sind alle [!DNL Target] -Benutzer beginnen mit [!UICONTROL Beobachter] Berechtigungen.

Administratoren sind in der Liste der [!UICONTROL Benutzer] aufgeführt. Kontaktieren Sie einen dieser Systemadministratoren, wenn Sie Ihre Zugriffsebene ändern lassen möchten.

## Anzeigen von Benutzerinformationen in [!DNL Target]

Sie können eine Liste Ihrer aktuellen Benutzer im [!DNL Target] Benutzeroberfläche, einschließlich der Rollen pro Arbeitsbereich und E-Mail-Adressen.

So zeigen Sie die [!UICONTROL Benutzer] Seite, klicken **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]**.

![Benutzerliste in Target](/help/main/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Um einen vorhandenen Benutzer zu verwalten oder neue Benutzer hinzuzufügen, müssen Sie die [!UICONTROL Adobe Admin Console] wie unten beschrieben verwenden.

## Zugriff auf [!DNL Adobe Admin Console] {#access}

Für Aufgaben, die im [!DNL Adobe Admin Console], greifen Sie auf die Konsole zu, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerverwaltung]**.

   Oder

   Navigieren Sie zu [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) und melden Sie sich mit Ihrer Adobe ID an, falls Sie dies noch nicht getan haben.

1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Hinzufügen von Benutzern {#add-users}

Die gesamte Benutzerverwaltung muss in der [!DNL Adobe Admin Console for Enterprise] erfolgen. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. Klicken Sie [in der Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzer]**, um neue Benutzer zu erstellen oder vorhandene Benutzer zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Erstellen von Benutzergruppen {#user-groups}

Sie können Benutzergruppen wie Entwickler, Analysten, Marketingexperten, Manager usw. erstellen und dann Berechtigungen für mehrere [!DNL Adobe] Produkte und Arbeitsbereiche. Zuweisen neuer Teammitglieder zu allen entsprechenden Berechtigungen für verschiedene [!DNL Adobe] -Produkte können so einfach wie das Hinzufügen zu einer bestimmten Benutzergruppe sein.

1. Klicken Sie [in der Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzergruppen]**, um neue Benutzergruppen zu erstellen oder bestehende Gruppen zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Festlegen von Rollen und Berechtigungen {#roles-permissions}

Benutzerrollen können in [!DNL Target] nur von Systemadministratoren festgelegt werden. Beispiel: eine [!UICONTROL Standard] Benutzer mit Genehmiger können einen Beobachter nicht in einen Genehmiger ändern, ohne auch [!DNL Experience Cloud] Administratorrechte.

Systemadministratoren müssen Benutzer zum System hinzufügen. Benutzer werden nicht automatisch hinzugefügt. Sie werden per E-Mail über [!DNL Experience Cloud] eingeladen und müssen ihre E-Mail-Adressen bestätigen, damit ihre Konten registriert werden.

1. [Klicken Sie in der Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Registerkarte „Produkte“](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klicken Sie auf den gewünschten Arbeitsbereich (z. B. Standardarbeitsbereich).

   ![Standardarbeitsbereich](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Auf der Registerkarte [!UICONTROL Benutzer] werden alle Benutzer des Workspace aufgeführt.

   ![Konfigurationsbenutzer](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Wählen Sie die gewünschte Berechtigungsrolle ([!UICONTROL Genehmiger], [!UICONTROL Bearbeiter], [!UICONTROL Beobachter] oder [!UICONTROL Herausgeber]), indem Sie die Dropdownliste für jeden Benutzer im [!UICONTROL Produktrolle] Spalte.

   ![Dropdownliste „Produktrolle“](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rolle | Beschreibung |
   |--- |--- |
   | [!UICONTROL Genehmiger] | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | [!UICONTROL Bearbeiter] | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | [!UICONTROL Beobachter] | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | [!UICONTROL Publisher] | Ähnlich wie bei [!UICONTROL Beobachter] Rolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Rolle [!UICONTROL Publisher] zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

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
>Die Benutzeroberfläche des [!UICONTROL Administration]-Menüs von [!DNL Target] (früher [!UICONTROL Einrichten]) wurde überarbeitet, um eine verbesserte Leistung zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu reduzieren und das Benutzererlebnis im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind im Allgemeinen korrekt, allerdings können sich Optionen an etwas anderen Orten befinden. Aktualisierte Videos werden bald veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
