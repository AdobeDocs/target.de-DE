---
description: Informationen zu den erforderlichen Aufgaben für das Hinzufügen von Benutzern zur Target-Implementierung; Erstellen von Arbeitsbereichen, Benutzergruppen und Eigenschaften; Aktualisieren der Target-Implementierung, um den Parameter „at_property“ hinzuzufügen; Festlegen von Rollen und Berechtigungen.
keywords: Benutzer hinzufügen;Projekt;Benutzergruppe;Eigenschaften;Arbeitsbereich;Eigenschaft verwalten;Eigenschaft;at_property;Rollen;Berechtigungen
seo-description: Informationen über die erforderlichen Aufgaben zum Hinzufügen von Benutzern zu Ihrer Adobe Target-Implementierung Erstellen von Arbeitsbereichen, Benutzergruppen und Eigenschaften; Aktualisieren Sie Ihre Target-Implementierung, um den Parameter at_ property einzuschließen. und Rollen und Berechtigungen angeben.
seo-title: Konfigurieren von Unternehmensberechtigungen
solution: Target
subtopic: Erste Schritte
title: Konfigurieren von Unternehmensberechtigungen
title-outputclass: Premium
topic: Premium
uuid: 2f44ecd5-5c43-49c3-b1c3-58d28531c859
badge: Premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Konfigurieren von Unternehmensberechtigungen{#configure-enterprise-permissions}

Informationen zu den erforderlichen Aufgaben für das Hinzufügen von Benutzern zur Target-Implementierung; Erstellen von Arbeitsbereichen, Benutzergruppen und Eigenschaften; Aktualisieren der Target-Implementierung, um den Parameter „at_property“ hinzuzufügen; Festlegen von Rollen und Berechtigungen.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [!DNL Target Premium] verfügbar. Für [!DNL Target Standard] sind sie nicht ohne [!DNL Target Premium]-Lizenz verfügbar.

In der folgenden Tabelle sind alle Aufgaben aufgeführt, die Sie zur Erstellung von Eigenschaften und der Zuweisung von Benutzerrollen und Berechtigungen ausführen sollten. Weitere Informationen zu den einzelnen Aufgaben finden Sie in den nachfolgenden Abschnitten.

| Aufgabe | Durchgeführt in |
|--- |--- |
| 1. Benutzer hinzufügen (optional) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Arbeitsbereich (Produktprofil) erstellen | [!DNL Adobe Admin Console for Enterprise] |
| 3. Benutzergruppen erstellen (optional) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Eigenschaften erstellen | [!DNL Target] Benutzeroberfläche |
| 5: Implementierung aktualisieren, sodass der Parameter `at_property` enthalten ist | [!DNL Target]-Benutzeroberfläche, Funktionen „at.js“, [!DNL Adobe Launch] oder [!DNL Dynamic Tag Management] |
| 6: Rollen und Berechtigungen festlegen | [!DNL Adobe Admin Console for Enterprise] |

Greifen Sie für diese in der Adobe Admin Console for Enterprise ausgeführten Aufgaben auf die Konsole zu, indem Sie die folgenden Schritte durchführen:

1. Navigieren Sie zu [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) und melden Sie sich mit Ihrer Adobe ID an, falls Sie noch nicht angemeldet sein sollten.

   Oder

   Wenn Sie bereits bei der Experience Cloud angemeldet sind, rufen Sie [https://www.marketing.adobe.com](https://www.marketing.adobe.com/)auf und klicken Sie dann in der oberen Navigationsleiste auf das [!UICONTROL App] -Symbol. Klicken **[!UICONTROL Sie dann rechts auf Administration und]** anschließend auf **[!UICONTROL Admin-Konsole starten]**.

1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Schritt 1. Benutzer hinzufügen (optional) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wenn Sie mit der Verwendung der neuen Funktion [!UICONTROL Eigenschaften] beginnen, müssen alle Benutzer in der [!DNL Adobe Admin Console for Enterprise] verwaltet werden. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der Admin Console](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE) auf die Registerkarte **[!UICONTROL Benutzer]** oben auf der Seite und anschließend auf **Benutzer], um neue Benutzer zu erstellen oder vorhandene Benutzer zu bearbeiten.[!UICONTROL **
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in der Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) im *Enterprise-Benutzerhandbuch*.

## Schritt 2: Arbeitsbereich (Produktprofil) erstellen{#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Mithilfe eines Arbeitsbereichs (Produktprofil) können Organisationen bestimmte Benutzergruppen bestimmten Eigenschaftsgruppen zuweisen. Arbeitsbereiche ähneln auf vielerlei Weise den Report Suites in [!DNL Analytics].

Organisationen können mit der Nutzung der Berechtigungsfunktionalität für Unternehmen beginnen, indem sie neue Arbeitsbereiche in Admin Console erstellen, diesen Arbeitsbereichen Target-Eigenschaften zuordnen und Benutzer aus der Konfiguration „Standardarbeitsbereich“ in diese neueren Arbeitsbereiche mit beschränktem Zugriff verschieben.

Kunden können diese Arbeitsbereiche verwenden, um den Zugriff auf verschiedene Teams nach Region, Abteilung, Standort oder anderen beliebigen Methoden aufzuteilen.

Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen sogar unterschiedliche Rollen einnehmen.

1. Klicken Sie in der Admin Console auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Arbeitsbereich](/help/administrating-target/c-user-management/c-user-management/assets/workspace.png)

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

### Workspace-ID {workspace-id} abrufen

Sie müssen die Workspace-ID weiterreichen, um in [Target-apis Unternehmensberechtigungen zu nutzen](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md).

1. Klicken Sie in der [Adobe Admin-Konsole](https://adminconsole.adobe.com)auf die Registerkarte [!UICONTROL Produkte] und dann auf das Produkt im linken Menü, um die Liste der PLC (Workspace) anzuzeigen.
1. Klicken Sie auf die gewünschte SD (Workspace) und suchen Sie dann die ID der &quot;Profile&quot; in der URL, wie unten dargestellt.

![Workspaceid](/help/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Schritt 3. Benutzergruppen erstellen (optional) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

Sie können Benutzergruppen wie Entwickler, Analytiker, Marketingexperten, Manager usw. erstellen und ihnen dann Benutzerrechte für verschiedene Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. Klicken Sie in der Admin Console auf die Registerkarte **[!UICONTROL Benutzer]** oben auf der Seite und anschließend auf **Benutzergruppen], um neue Benutzergruppen zu erstellen oder vorhandene Gruppen zu bearbeiten.[!UICONTROL **
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen einer Produktkonfiguration](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) im *Enterprise-Benutzerhandbuch*.

## Schritt 4. Erstellen von Eigenschaften {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschaften werden aktiviert, indem ein bestimmtes Name-Wert-Paar beliebigen Aufrufen (mbox, API usw.) an Target hinzugefügt wird.

Eigenschaften sind bestimmten Kanälen (Web, mobil, E-Mail und API/Sonstige) zugeordnet..

**Tipp:** Weitere Informationen zum Erstellen von Eigenschaften finden Sie im Schulungsvideo unten.

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Eigenschaften]**, um die Liste der [!UICONTROL Eigenschaften] aufzurufen.
1. Klicken Sie auf **Eigenschaft erstellen**.

   ![Neue Eigenschaft, Dialogfeld](/help/administrating-target/c-user-management/property-channel/assets/new_property1.png)

   Füllen Sie die Felder aus:

   * **Kanal:** Geben Sie den gewünschten Kanal für die Eigenschaft an: Web, mobile App, E-Mail oder Sonstige/API (beispielsweise für Set-Top-Box oder PlayStation-Konsole).
   * **Name: (erforderlich)** Geben Sie einen beschreibenden Namen für die Eigenschaft ein.
   * **Beschreibung:** Geben Sie eine optionale Beschreibung für die Eigenschaft an.

1. Klicken Sie auf **[!UICONTROL Code generieren]**, um den Code zu generieren, den Sie bei der Ausführung der Schritte in [5: Implementierung aktualisieren, sodass der Parameter at_property enthalten ist](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8) verwenden.
1. Kopieren Sie den Code in die Zwischenablage.
1. Klicken Sie auf **[!UICONTROL Speichern], wenn Sie fertig sind.**

>[!NOTE]
>Weitere Informationen zum Erstellen von Eigenschaften finden Sie im Schulungsvideo unten.

## Schritt 5: Implementierung aktualisieren, sodass der Parameter at_property enthalten ist {#section_9B17A59807A94712BE642942442EBBC8}

Möchten Sie die Benutzerberechtigungsfunktion in [!DNL Target] nutzen, müssen Sie jedem Aufruf an Target (mbox, API usw.) den Parameter `at_property` hinzufügen.

**So erhalten Sie den Parameter-Code für`at_property`:**

1. (Bedingt) Verwenden Sie den Implementierungs-Code, den Sie generiert und in Ihrer Zwischenablage gespeichert haben, während Sie die Schritte unter [4. Eigenschaften erstellen](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) ausgeführt haben, und fahren Sie mit Schritt 2 fort.

   Oder

   Klicken Sie in [!DNL Target] auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Eigenschaften]**, um die Liste der [!UICONTROL Eigenschaften] aufzurufen.

   1. Fahren Sie mit dem Mauszeiger über die Spalte [!UICONTROL „Zuletzt aktualisiert“] der gewünschten Eigenschaft und wählen Sie das [!UICONTROL Codesymbol] aus.

      ![Eigenschaftenhover-Code](/help/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klicken Sie mit der rechten Maustaste auf den markierten Implementierungs-Code und kopieren Sie ihn in die Zwischenablage.

      ![Eigenschaftencode](/help/administrating-target/c-user-management/property-channel/assets/code_property_2_new.png)

1. Aktualisieren Sie die Target-Implementierung mit dem Implementierungs-Code, der im vorangegangenen Schritt abgerufen wurde.

   Die [!DNL Target]-Implementierung kann auf unterschiedliche Art aktualisiert werden. Für Webseiten können beispielsweise die folgenden Verfahren angewendet werden:

   * **Über einen „globalen Parameter“ im[!DNL Dynamic Tag Management](Adobe Activation):**

      ![](assets/property_token_2.png)

      Weitere Informationen finden Sie unter [Globale Parameter - Adobe Target](https://marketing.adobe.com/resources/help/en_US/dtm/target_global_params.html) in der *Produktdokumentation des Dynamic Tag Management*.

   * **Mithilfe der Funktion targetPageParams():** Platzieren Sie den folgenden Code in die <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> Tags oberhalb Referenz „at.js“ oder „mbox.js“.

      ![](assets/property_token_1.png)

      Weitere Informationen zu diesem Verfahren unter „at.js“ finden Sie unter [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md).

   * **Mithilfe der Funktion „mboxCreate()“:**

      ![](assets/property_token_3.png)

      Weitere Informationen zu diesem Verfahren unter „at.js“ finden Sie unter   [Targetpageparams ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) und [mboxcreate (mbox, params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md).

## Schritt 6: Rollen und Berechtigungen festlegen {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klicken Sie in der Admin Console auf **[!UICONTROL Produkte]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Arbeitsbereich](/help/administrating-target/c-user-management/c-user-management/assets/workspace.png)

   >[!NOTE]
   >
   >Die Funktion für Eigenschaften und Berechtigungen gilt ausschließlich für [!DNL Target Standard/Premium]. Für [!DNL Target Classic] steht die Funktion nicht zur Verfügung.

1. Klicken Sie auf den Namen des gewünschten Profils.
1. Klicken Sie auf **[!UICONTROL Benutzer]**.

   Unter der Registerkarte [!UICONTROL Konfigurationsbenutzer] werden alle Benutzer des Arbeitsbereichs aufgeführt.

   ![Konfigurieren von Benutzern](/help/administrating-target/c-user-management/property-channel/assets/configuration_users_new.png)

1. Wählen Sie das gewünschte Berechtigungsniveau (Genehmiger, Editor oder Beobachter) aus, indem Sie in der Spalte [!UICONTROL Produktrolle] das entsprechende Dropdown-Menü nutzen.

   | Rolle | Beschreibung |
   |--- |--- |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Editor | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |

   Weitere Informationen finden Sie unter [Verwalten von Produktberechtigungen und Rollen in der Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) im *Enterprise-Benutzerhandbuch*.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Konfigurieren von Target-Arbeitsbereichen (6:55)

In diesem Video wird das Erstellen von Arbeitsbereichen erläutert.

* Zugreifen auf die Adobe Admin Console über die Adobe Target-Schnittstelle (3 Methoden)
* Konfigurieren eines Arbeitsbereichs in Adobe Admin Console

   * Hinzufügen von Benutzern zu Arbeitsbereichen
   * Hinzufügen von Eigenschaften zu Arbeitsbereichen

* Grundlegende Informationen zu Standardarbeitsbereichen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Erstellen von Eigenschaften in Adobe Target (3:05)

* Erstellen einer Eigenschaft auf der [!DNL Adobe Target]-Benutzeroberfläche
* Generieren eines Eigenschaftstokens zum Einfügen in die Eigenschaftenimplementierung
* Machen Sie sich mit den drei Implementierungsmethoden vertraut:

   * Web
   * Mobile App
   * E-Mail, Set-Top-Box oder API-Aufrufe

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
