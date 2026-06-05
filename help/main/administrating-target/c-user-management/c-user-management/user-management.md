---
keywords: Benutzer hinzufügen;Benutzer verwalten;Benutzerberechtigungen
description: Erfahren Sie, wie Sie mit der  [!DNL Adobe Admin Console]  Benutzende und deren Berechtigungen in  [!DNL Adobe Target Standard] verwalten können.
title: Wie kann ich für ein  [!DNL Target Standard] -Konto Benutzende hinzufügen und Berechtigungen verwalten?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
TQID: https://experienceleague.adobe.com/DdNQ81TpmyIRuPkmy4OIOq43CXwaMtm-uH2HtPjdx10
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
subfeature_v2: id: c011fe9c-b94b-4a88-93d8-f2acece55112id: cd7b6938-5837-4ee0-9790-5840997133d9id: cf6b8469-14d0-4c0e-90ee-fb54066a035eid: faed1c89-faf7-4df1-910d-a88263e03b15id: fc9c2184-9102-403f-bd6c-0055021e4bea
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 925
ht-degree: 60%

---

# Benutzende

Fügen Sie Benutzende hinzu und verwalten Sie ihre Berechtigungen in der [!DNL Adobe Admin Console] für ein [!DNL Target Standard]-Konto.

>[!NOTE]
>
>Die Funktionen [!UICONTROL Eigenschaften] und [!UICONTROL Berechtigungen] sind als Teil der [!DNL Target Premium] verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>
>Sie können feststellen, ob Ihr Unternehmen über eine [!UICONTROL Standard]- oder [!UICONTROL Premium]-Lizenz verfügt, indem Sie auf den Link [!UICONTROL Administration] oben in der [!DNL Target]-Benutzeroberfläche klicken.
>
>* **[!DNL Target][!UICONTROL Standard] Kunden**: Wenn Sie die Registerkarte [!UICONTROL Benutzer] ([!UICONTROL Administration > Benutzer]) sehen (und nicht die Registerkarte **[!UICONTROL Eigenschaften]**), verfügt Ihr Unternehmen über eine [!DNL Target] [!UICONTROL Standard]-Lizenz. [!DNL Target] [!UICONTROL Standard]-Kunden sollten die Anweisungen in diesem Artikel befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>* **[!DNL Target]Premium-**: Wenn Sie die Registerkarte [!UICONTROL Benutzer] und die Registerkarte [!UICONTROL Eigenschaften] sehen ([!UICONTROL Administration > Eigenschaften]), verfügt Ihr Unternehmen über eine [!DNL Target] Premium-Lizenz. [!DNL Target] Premium-Kunden sollten die Anweisungen unter [Berechtigungen für Unternehmensbenutzer](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) und [Konfigurieren von Unternehmensberechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.
>
>Detaillierte Informationen zum Verwalten von Benutzern und Berechtigungen finden Sie im Abschnitt [Produkte und Profile verwalten](https://helpx.adobe.com/de/enterprise/using/manage-products-and-profiles.html) im *Benutzerhandbuch für Unternehmen und Teams*.

Wenn Sie [!DNL Adobe Target] zum ersten Mal verwenden, sind bereits IDs (mit der Endung Adobe.com) in Ihrem [!DNL Adobe Experience Cloud]-Konto vorhanden. Diese IDs sind für Mitglieder des [!DNL Adobe]-Teams gedacht, damit Ihnen diese bei Bedarf mit Ihrem neuen Konto und der Verwendung von [!DNL Adobe Target] helfen können. Wenn Sie Unterstützung benötigen, wenden Sie sich auf dem üblichen Weg an Ihre Teams von Adobe.

Neue Benutzer werden erst auf der Seite [!UICONTROL Benutzer] aufgeführt, wenn sie sich mit ihrem [!DNL Adobe Experience Cloud] Konto anmelden und sich anschließend bei [!DNL Target] anmelden.

Standardmäßig ist allen [!DNL Target]-Benutzern die Berechtigung [!UICONTROL Beobachter] zugewiesen.

Admin-Benutzer werden in der Liste [!UICONTROL Benutzer] identifiziert. Kontaktieren Sie einen dieser Systemadministratoren, wenn Sie Ihre Zugriffsebene ändern lassen möchten.

## Anzeigen von Benutzerinformationen in [!DNL Target]

Sie können eine Liste Ihrer aktuellen Benutzenden auf der [!DNL Target]-Benutzeroberfläche anzeigen, einschließlich der Rollen pro Arbeitsbereich und E-Mail-Adressen.

Um die Seite [!UICONTROL Benutzer] anzuzeigen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]**.

>[!NOTE]
>
>Um einen vorhandenen Benutzer zu verwalten oder neue Benutzer hinzuzufügen, müssen Sie den [!UICONTROL Adobe Admin Console] wie unten beschrieben verwenden.

## Zugreifen auf die [!DNL Adobe Admin Console] {#access}

Greifen Sie auf die [!DNL Adobe Admin Console] zu, indem Sie die folgenden Schritte durchführen:

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerverwaltung]**.

   Oder

   Navigieren Sie zu [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) und melden Sie sich mit Ihrer Adobe ID an, falls Sie dies noch nicht getan haben.

1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Hinzufügen von Benutzern {#add-users}

Die gesamte Benutzerverwaltung muss in der [!DNL Adobe Admin Console for Enterprise] erfolgen. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der ](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzer]**, um neue Benutzer zu erstellen oder bestehende Benutzer zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Erstellen von Benutzergruppen {#user-groups}

Sie können Benutzergruppen wie Entwickelnde, Analytiker, Marketing-Fachleute, Führungskräfte usw. erstellen und ihnen dann Benutzerrechte für verschiedene [!DNL Adobe]-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für mehrere [!DNL Adobe]-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. [Klicken Sie in der ](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzergruppen]**, um neue Benutzergruppen zu erstellen oder bestehende Gruppen zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Festlegen von Rollen und Berechtigungen {#roles-permissions}

Benutzerrollen können in [!DNL Target] nur von Systemadministratoren festgelegt werden. Beispielsweise kann ein [!UICONTROL Standard]Genehmiger einen Beobachter nicht in einen Genehmiger ändern, ohne zusätzlich über [!DNL Experience Cloud] Administratorrechte zu verfügen.

Systemadministratoren müssen Benutzer zum System hinzufügen. Benutzer werden nicht automatisch hinzugefügt. Sie werden per E-Mail über [!DNL Experience Cloud] eingeladen und müssen ihre E-Mail-Adressen bestätigen, damit ihre Konten registriert werden.

>[!NOTE]
>
>Um Aktivitäten in [!DNL Target] anzeigen zu können, müssen Benutzende mindestens einem Arbeitsbereich mit der Rolle [!UICONTROL Beobachter“ ] sein. Die Zuweisung über Benutzergruppen allein ist unzureichend. Es wird allgemein empfohlen, Benutzern Zugriff auf den Standardarbeitsbereich zu gewähren.

1. [Klicken Sie in der Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

1. Klicken Sie auf den gewünschten Arbeitsbereich (z. B. Standardarbeitsbereich).

   Auf [!UICONTROL  Registerkarte ]Benutzer“ werden alle Benutzenden in diesem Arbeitsbereich angezeigt.

1. Wählen Sie das gewünschte Berechtigungsniveau ([!UICONTROL Genehmiger], [!UICONTROL Editor], [!UICONTROL Beobachter] oder [!UICONTROL Publisher]) aus, indem Sie das entsprechende Dropdown-Menü in der Spalte [!UICONTROL Produktrolle] verwenden.

   | Rolle | Beschreibung |
   |--- |--- |
   | [!UICONTROL Genehmigende Person] | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | [!UICONTROL Editor] | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | [!UICONTROL Beobachter] | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | [!UICONTROL Herausgeber] | Ähnlich wie die Rolle [!UICONTROL Beobachter] (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Die Rolle [!UICONTROL Publisher] verfügt jedoch zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

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
