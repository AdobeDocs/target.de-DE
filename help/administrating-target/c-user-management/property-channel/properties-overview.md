---
keywords: add user;project;user group;properties;workspace;manage property;property;at_property;roles;permissions
description: Informationen zu den erforderlichen Aufgaben für das Hinzufügen von Benutzern zur Target-Implementierung; Erstellen von Arbeitsbereichen, Benutzergruppen und Eigenschaften; Aktualisieren der Target-Implementierung, um den Parameter „at_property“ hinzuzufügen; Festlegen von Rollen und Berechtigungen.
title: Konfigurieren von Unternehmensberechtigungen
feature: user management
subtopic: Getting Started
uuid: 2f44ecd5-5c43-49c3-b1c3-58d28531c859
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '1474'
ht-degree: 68%

---


# ![PREMIUM](/help/assets/premium.png) Konfigurieren von Unternehmensberechtigungen{#configure-enterprise-permissions}

Information about the tasks required to add users to your [!DNL Target] implementation; create workspaces, user groups, and properties; update your [!DNL Target] implementation to include the `at_property` parameter; and specify roles and permissions.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [Target Premium](/help/c-intro/intro.md#premium) verfügbar. In [!DNL Target Standard] sind sie nur mit einer [!DNL Target Premium]-Lizenz verfügbar.

In der folgenden Tabelle sind alle Aufgaben aufgeführt, die Sie zur Erstellung von Eigenschaften und der Zuweisung von Benutzerrollen und Berechtigungen ausführen sollten. Weitere Informationen zu den einzelnen Aufgaben finden Sie in den nachfolgenden Abschnitten.

| Aufgabe | Durchgeführt in |
|--- |--- |
| 1. Benutzer hinzufügen (optional) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Arbeitsbereich (Produktprofil) erstellen | [!DNL Adobe Admin Console for Enterprise] |
| 3. Benutzergruppen erstellen (optional) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Eigenschaften erstellen | [!DNL Target] Benutzeroberfläche |
| 5: Implementierung aktualisieren, sodass der Parameter `at_property` enthalten ist | [!DNL Target]-Benutzeroberfläche, Funktionen „at.js“, [!DNL Adobe Launch] oder [!DNL Dynamic Tag Management] |
| 6: Rollen und Berechtigungen festlegen | [!DNL Adobe Admin Console for Enterprise] |

For those tasks performed in the [!DNL Adobe Admin Console for Enterprise], access the console by following these steps:

1. Klicken Sie in Adobe Target auf **[!UICONTROL Administration]** > **[!UICONTROL Eigenschaften]** > Eigenschaften zu Arbeitsbereichen **[!UICONTROL zuweisen]**.

   Oder

   Go to [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) > sign in using your Adobe ID, if you have not already logged in.


1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Schritt 1. Add users (Optional) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wenn Sie mit der Verwendung der neuen Funktion [!UICONTROL Eigenschaften] beginnen, müssen alle Benutzer in der [!DNL Adobe Admin Console for Enterprise] verwaltet werden. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der Admin Console](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE) auf die Registerkarte **[!UICONTROL Benutzer]** oben auf der Seite und anschließend auf **[!UICONTROL Benutzer hinzufügen]**, um neue Benutzer zu erstellen oder vorhandene Benutzer zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in der Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) im *Enterprise-Benutzerhandbuch*.

## Schritt 2: Create a workspace (product profile) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Mit einem Arbeitsbereich (Produkt-Profil) kann eine Organisation einen bestimmten Benutzergruppe einem bestimmten Satz von Eigenschaften zuweisen. Arbeitsbereiche ähneln auf vielerlei Weise den Report Suites in [!DNL Analytics].

Organizations can begin taking advantage of Enterprise permissions functionality by creating new workspaces within [!DNL Admin Console], assigning [!DNL Target] properties to these workspaces, and moving users from the &quot;Default Workspace&quot; configuration to these newer, limited-access workspaces.

Kunden können diese Arbeitsbereiche verwenden, um den Zugriff auf verschiedene Teams nach Region, Abteilung, Standort oder anderen beliebigen Methoden aufzuteilen.

Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen sogar unterschiedliche Rollen einnehmen.

1. Klicken Sie in der [!DNL Admin Console] auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Arbeitsbereich](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Erstellen Sie den gewünschten Arbeitsbereich (Produktprofil):

   * **Standardzugriff:** Sämtliche bestehenden Aktivitäten werden in einem einzigen Projekt mit der Bezeichnung „Standardzugriff“ vereinigt. Kunden sind von dieser Einstellung nicht betroffen. Sämtliche Benutzerrollen und Funktionen bleiben die gleichen und ändern sich nicht.

      Alle mit [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] und [!DNL Target Classic] erstellten Aktivitäten werden ebenfalls in den Arbeitsbereich „Standardzugriff“ übernommen. Zurzeit ist es nicht möglich, Projekte aus „Standardzugriff“ in ein anderes Projekt zu verschieben.

   * **Neue Arbeitsbereiche (Produktprofile):** Sie können die neue Berechtigungsfunktion wie folgt nutzen:

      * Neue Arbeitsbereiche in der [!DNL Admin Console for Enterprise] erstellen.
      * Arbeitsbereichen Target-Eigenschaften zuweisen.

   Mithilfe der Arbeitsbereiche können Sie den Zugriff auf verschiedene Teams nach Region, Abteilung, Standort oder anderen beliebigen Kategorien festlegen. Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen unterschiedliche Rollen einnehmen.

1. Befolgen Sie die Anweisungen unter [Erstellen und Verwalten von Produktkonfigurationen](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) im *Benutzerhandbuch für Unternehmen*.

>[!NOTE]
>Weitere Informationen zum Konfigurieren von Arbeitsbereichen finden Sie im Schulungsvideo unten.

### Obtain your workspace ID {#workspace-id}

Sie müssen die Workspace-ID weiterreichen, um in [Target-APIs Unternehmensberechtigungen zu nutzen](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md).

1. Klicken Sie in der [Adobe Admin Console](https://adminconsole.adobe.com) auf die Registerkarte [!UICONTROL Produkte] und anschließend auf das Produkt im linken Menü, um die Liste der PLC (Workspace) anzuzeigen.
1. Klicken Sie auf die gewünschte PLC (Workspace) und suchen Sie dann die ID für „profiles“ in der URL, wie unten dargestellt.

   ![workspaceID](/help/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Schritt 3. Create user groups (Optional) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

Sie können Benutzergruppen wie Entwickler, Analytiker, Marketingexperten, Manager usw. erstellen und ihnen dann Benutzerrechte für verschiedene Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. Klicken Sie in der Admin Console auf die Registerkarte **[!UICONTROL Benutzer]** oben auf der Seite und anschließend auf **[!UICONTROL Benutzergruppen]**, um neue Benutzergruppen zu erstellen oder vorhandene Gruppen zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen einer Produktkonfiguration](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) im *Enterprise-Benutzerhandbuch*.

## Schritt 4. Eigenschaften erstellen {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschaften werden aktiviert, indem ein bestimmtes Namens-/Wertpaar als Parameter bei jedem Aufruf hinzugefügt wird (Zielgruppe-Aufruf, API-Aufruf usw.) an Target hinzugefügt wird.

Eigenschaften sind bestimmten Kanälen (Web, mobil, E-Mail und API/Sonstige) zugeordnet..

**Tipp:** Weitere Informationen zum Erstellen von Eigenschaften finden Sie im Schulungsvideo unten.

1. In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Properties]** to display the [!UICONTROL Properties] list.
1. Klicken Sie auf **Eigenschaft erstellen**.

   ![Neue Eigenschaft, Dialogfeld](/help/administrating-target/c-user-management/property-channel/assets/new_property1.png)

   Füllen Sie die Felder aus:

   * **Eigenschaftsname (erforderlich):** Geben Sie einen beschreibenden Namen für die Eigenschaft an.
   * **Beschreibung:** Geben Sie eine optionale Beschreibung für die Eigenschaft an.
   * **Kanal:** Wählen Sie den gewünschten Kanal für die Eigenschaft aus: Web, mobile App, E-Mail oder Sonstige/API (beispielsweise für Set-Top-Box oder PlayStation-Konsole).

1. Klicken Sie auf **[!UICONTROL Kopieren]** , um den Code in die Zwischenablage zu kopieren, den Sie bei Ausführung der Schritte in [5 verwenden werden: Aktualisieren Sie Ihre Implementierung, um den Parameter](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8)at_property einzuschließen.
1. Klicken Sie auf **[!UICONTROL Speichern]**, wenn Sie fertig sind.

>[!NOTE]
>Weitere Informationen zum Erstellen von Eigenschaften finden Sie im Schulungsvideo unten.

## Step 5: Update your implementation to include the at_property parameter {#section_9B17A59807A94712BE642942442EBBC8}

To use the [!DNL Target] user-permissions functionality, you must add the `at_property` parameter to any call that is hitting [!DNL Target] (Target call, api call, etc.).

**So erhalten Sie den Parameter-Code für `at_property`:**

1. (Bedingt) Verwenden Sie den Implementierungs-Code, den Sie generiert und in Ihrer Zwischenablage gespeichert haben, während Sie die Schritte unter [4. Eigenschaften erstellen](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) ausgeführt haben, und fahren Sie mit Schritt 2 fort.

   Oder

   In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Properties]** to display the [!UICONTROL Properties] list.

   1. Fahren Sie mit dem Mauszeiger über die Spalte [!UICONTROL „Zuletzt aktualisiert“] der gewünschten Eigenschaft und wählen Sie das [!UICONTROL Codesymbol] aus.

      ![Eigenschaften-Hover-Code](/help/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klicken Sie mit der rechten Maustaste auf den markierten Implementierungs-Code und kopieren Sie ihn in die Zwischenablage.

      ![Eigenschaftencode](/help/administrating-target/c-user-management/property-channel/assets/code_property_2_new.png)

1. Update your [!DNL Target] implementation with the implementation code obtained in the previous step.

   Die [!DNL Target]-Implementierung kann auf unterschiedliche Art aktualisiert werden. Für Webseiten können beispielsweise die folgenden Verfahren angewendet werden:

   * **Über einen „globalen Parameter“ im [!DNL Adobe Launch]:**

      For more information, see [Add Global Target Params](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension#add-global-mbox-params) in the *Adobe Experience Platform Launch* documentation.

   * **Über einen „globalen Parameter“ im [!DNL Dynamic Tag Management]:**

      ![](assets/property_token_2.png)

      Weitere Informationen finden Sie unter [Globale Parameter - Adobe Target](https://experienceleague.adobe.com/docs/dtm/using/tools-reference/target.html#global-parameters---adobe-target) in der *Produktdokumentation des Dynamic Tag Management*.

   * **Über die Funktion targetPageParams():** Fügen Sie den folgenden Code in die `<head>` Tags oberhalb des Verweises auf at.js oder mbox.js ein.

      ![](assets/property_token_1.png)

      Weitere Informationen zu diesem Verfahren unter „at.js“ finden Sie unter [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md).

   * **Mithilfe der Funktion „mboxCreate()“:**

      ![](assets/property_token_3.png)

      Weitere Informationen zu diesem Verfahren mit at.js finden Sie unter  [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) und [mboxCreate(mbox, params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md).

## Step 6: Specify roles and permissions {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klicken Sie in der Admin Console auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Arbeitsbereich](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klicken Sie auf den Namen des gewünschten Profils (z. B. Standardarbeitsbereich).

   ![Standardarbeitsbereich](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Klicken Sie auf **[!UICONTROL Benutzer]**.

   Auf der Registerkarte [!UICONTROL Benutzer] werden alle Benutzer des Workspace aufgeführt.

   ![Konfigurationsbenutzer](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Select the desired permissions role (Approver, Editor, Observer, or Publisher) by using the drop-down list for each user in the [!UICONTROL Product Role] column.

   ![Dropdown-Liste &quot;Produktrolle&quot;](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rolle | Beschreibung |
   |--- |--- |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Publisher | Ähnlich wie bei der Rolle &quot;Beobachter&quot;(Aktivitäten können zwar Ansicht, aber nicht erstellt oder bearbeitet werden). Die Rolle &quot;Herausgeber&quot;verfügt jedoch über die zusätzliche Berechtigung zum Aktivieren von Aktivitäten. |

   Weitere Informationen finden Sie unter [Verwalten von Produktberechtigungen und Rollen in der Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) im *Enterprise-Benutzerhandbuch*.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

>[!NOTE]
>
>Die Benutzeroberfläche des [!DNL Target] Administrationsmenüs [!UICONTROL (früher] Setup ) wurde überarbeitet, um die Leistung zu verbessern, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu verkürzen und die Benutzerfreundlichkeit im gesamten Produkt zu verbessern. Die Informationen in den folgenden Videos sind im Allgemeinen korrekt. Die Optionen befinden sich jedoch möglicherweise an etwas anderen Orten. Aktualisierte Videos werden demnächst veröffentlicht.

### Konfigurieren von Zielgruppe Workspaces (6:55) - ![Tutorialzeichen](/help/assets/tutorial.png)

In diesem Video wird das Erstellen von Arbeitsbereichen erläutert.

* Zugreifen auf die Adobe Admin Console über die Adobe Target-Schnittstelle (3 Methoden)
* Konfigurieren eines Arbeitsbereichs in Adobe Admin Console

   * Hinzufügen von Benutzern zu Arbeitsbereichen
   * Hinzufügen von Eigenschaften zu Arbeitsbereichen

* Grundlegende Informationen zu Standardarbeitsbereichen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### How to Create Properties in Adobe Target (3:05) ![Tutorial badge](/help/assets/tutorial.png)

* Erstellen einer Eigenschaft auf der [!DNL Adobe Target]-Benutzeroberfläche
* Generieren eines Eigenschaftstokens zum Einfügen in die Eigenschaftenimplementierung
* Machen Sie sich mit den drei Implementierungsmethoden vertraut:

   * Web
   * Mobile App
   * E-Mail, Set-Top-Box oder API-Aufrufe

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
