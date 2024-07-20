---
keywords: Benutzer hinzufügen;Projekt;Benutzergruppe;Eigenschaften;Arbeitsbereich;Eigenschaft verwalten;Eigenschaft;at_property;Rollen;Berechtigungen
description: Erfahren Sie, wie Sie Benutzer zu Adobe Target hinzufügen, Arbeitsbereiche, Benutzergruppen und Eigenschaften erstellen, Ihre Implementierung aktualisieren und Rollen und Berechtigungen festlegen.
title: Wie konfiguriere ich Unternehmensberechtigungen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Administration & Configuration
role: Admin
exl-id: 6494fc86-d2d3-4382-9d2e-63be435ba935
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 54%

---

# Konfigurieren von Unternehmensberechtigungen

Informationen zu den erforderlichen Aufgaben für das Hinzufügen von Benutzern zur Implementierung von [!DNL Target]; Erstellen von Arbeitsbereichen, Benutzergruppen und Eigenschaften; Aktualisieren der Implementierung von [!DNL Target], um den Parameter `at_property` hinzuzufügen; Festlegen von Rollen und Berechtigungen.

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung [Target Premium](/help/main/c-intro/intro.md#premium) verfügbar. In [!DNL Target Standard] sind sie nur mit einer [!DNL Target Premium]-Lizenz verfügbar.

In der folgenden Tabelle sind alle Aufgaben aufgeführt, die Sie zur Erstellung von Eigenschaften und der Zuweisung von Benutzerrollen und Berechtigungen ausführen sollten. Weitere Informationen zu den einzelnen Aufgaben finden Sie in den nachfolgenden Abschnitten.

| Aufgabe | Durchgeführt in |
|--- |--- |
| 1. Benutzer hinzufügen (optional) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Erstellen eines Arbeitsbereichs (Produktprofil) | [!DNL Adobe Admin Console for Enterprise] |
| 3. Benutzergruppen erstellen (optional) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Eigenschaften erstellen | [!DNL Target]-Benutzeroberfläche |
| 5: Implementierung aktualisieren, sodass der Parameter `at_property` enthalten ist | [!DNL Target] Benutzeroberfläche, at.js-Funktionen oder Tags in [!DNL Adobe Experience Platform] |
| 6: Rollen und Berechtigungen festlegen | [!DNL Adobe Admin Console for Enterprise] |

Greifen Sie für die in [!DNL Adobe Admin Console for Enterprise] ausgeführten Aufgaben auf die Konsole zu, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie in Adobe Target auf **[!UICONTROL Administration]** > **[!UICONTROL Properties]** > **[!UICONTROL Assign Properties to Workspaces]**.

   Oder

   Navigieren Sie zu [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) > melden Sie sich mit Ihrer Adobe ID an, falls Sie noch nicht angemeldet sind.


1. (Bedingt) Sollten Sie über Zugriff auf die [!DNL Admin Console for Enterprise] für mehr als ein Unternehmen verfügen, klicken Sie rechts in der oberen Navigationsleiste auf den Benutzeravatar und wählen Sie die gewünschte Organisation aus.

## Schritt 1. Benutzer hinzufügen (optional) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wenn Sie mit der Verwendung der neuen [!UICONTROL Properties] -Funktion beginnen, muss die gesamte Benutzerverwaltung in der [!DNL Adobe Admin Console for Enterprise] durchgeführt werden. All Ihre bereits in [!DNL Target] angelegten Benutzer werden jedoch von [!DNL Target] in die [!DNL Admin Console for Enterprise] migriert.

1. [Klicken Sie in der Admin Console](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE) auf die Registerkarte **[!UICONTROL Users]** oben auf der Seite > **[!UICONTROL Add Users]** , um neue Benutzer zu erstellen oder bestehende zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen in Experience Cloud](https://helpx.adobe.com/de/enterprise/using/users.html) im *Enterprise-Benutzerhandbuch*.

## Schritt 2: Erstellen eines Arbeitsbereichs (Produktprofil) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Mit einem Arbeitsbereich (Produktprofil) kann eine Organisation bestimmte Benutzergruppen bestimmten Eigenschaftsgruppen zuweisen. Arbeitsbereiche ähneln auf vielerlei Weise den Report Suites in [!DNL Analytics].

Unternehmen können mit der Nutzung der Berechtigungsfunktion für Unternehmen beginnen, indem sie neue Arbeitsbereiche innerhalb von [!DNL Admin Console] erstellen, diesen Arbeitsbereichen [!DNL Target] -Eigenschaften zuweisen und Benutzer aus der Konfiguration &quot;Standard-Workspace&quot;in diese neueren Arbeitsbereiche mit beschränktem Zugriff verschieben.

Kunden können diese Arbeitsbereiche verwenden, um den Zugriff auf verschiedene Teams nach Region, Abteilung, Standort oder anderen beliebigen Methoden aufzuteilen.

Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen sogar unterschiedliche Rollen einnehmen.

1. Klicken Sie in der [!DNL Admin Console] auf **[!UICONTROL Products]** und wählen Sie dann den Namen des gewünschten Produkts aus.

   ![Arbeitsbereich](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

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

### Arbeitsbereichs-ID abrufen {#workspace-id}

Sie müssen die Arbeitsbereichs-ID übergeben, um Unternehmensberechtigungen in [Target-APIs](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=de){target=_blank} zu nutzen.

1. Klicken Sie in [Adobe Admin Console](https://adminconsole.adobe.com) auf die Registerkarte [!UICONTROL Products] und dann im linken Menü auf das Produkt, um die Liste PLC(Workspace) anzuzeigen.
1. Klicken Sie auf die gewünschte PLC (Workspace) und suchen Sie dann die ID für „profiles“ in der URL, wie unten dargestellt.

   ![workspaceID](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Schritt 3. Benutzergruppen erstellen (optional) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

Sie können Benutzergruppen wie Entwickler, Analytiker, Marketingexperten, Manager usw. erstellen und ihnen dann Benutzerrechte für verschiedene Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

1. Klicken Sie in der Admin Console auf die Registerkarte **[!UICONTROL Users]** oben auf der Seite > **[!UICONTROL User Groups]** , um neue Benutzergruppen zu erstellen oder bestehende zu bearbeiten.
1. Befolgen Sie die Anweisungen unter [Verwalten von Benutzern und Gruppen einer Produktkonfiguration](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) im *Enterprise-Benutzerhandbuch*.

## Schritt 4. Erstellen von Eigenschaften {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschaften werden aktiviert, indem ein bestimmtes Name/Wert-Paar als Parameter mit jedem Aufruf hinzugefügt wird (Target-Aufruf, API-Aufruf usw.) an Target hinzugefügt wird.

Eigenschaften gehören zu bestimmten Kanälen (Web, Mobile, E-Mail und API/Sonstige).

**Tipp:** Weitere Informationen zum Erstellen von Eigenschaften finden Sie im Schulungsvideo unten.

1. Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Properties]** , um die Liste [!UICONTROL Properties] anzuzeigen.
1. Klicken Sie auf **Eigenschaft erstellen**.

   Füllen Sie die Felder aus:

   * **Eigenschaftsname (erforderlich):** Geben Sie einen beschreibenden Namen für die Eigenschaft an.
   * **Beschreibung:** Geben Sie eine optionale Beschreibung für die Eigenschaft an.
   * **Kanal:** Wählen Sie den gewünschten Kanal für die Eigenschaft aus: Web, mobile App, E-Mail oder Sonstige/API (beispielsweise für Set-Top-Box oder PlayStation-Konsole).

1. Klicken Sie auf **[!UICONTROL Copy]** , um den Code in die Zwischenablage zu kopieren, den Sie bei der Ausführung der Schritte in [5: Implementierung aktualisieren, sodass der Parameter at_property](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8) enthalten ist.
1. Klicken Sie abschließend auf **[!UICONTROL Save]** .

>[!NOTE]
>Weitere Informationen zum Erstellen von Eigenschaften finden Sie im Schulungsvideo unten.

## Schritt 5: Implementierung aktualisieren, sodass der Parameter at_property enthalten ist {#section_9B17A59807A94712BE642942442EBBC8}

Um die Benutzerberechtigungsfunktion von [!DNL Target] zu verwenden, müssen Sie jedem Aufruf, der auf [!DNL Target] trifft (Target-Aufruf, API-Aufruf usw.), den Parameter `at_property` hinzufügen.

**So erhalten Sie den Parameter-Code für `at_property`:**

1. (Bedingt) Verwenden Sie den Implementierungs-Code, den Sie generiert und in Ihrer Zwischenablage gespeichert haben, während Sie die Schritte unter [4. Eigenschaften erstellen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) ausgeführt haben, und fahren Sie mit Schritt 2 fort.

   Oder

   Klicken Sie in [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Properties]** , um die Liste [!UICONTROL Properties] anzuzeigen.

   1. Bewegen Sie den Mauszeiger über die Spalte &quot;[!UICONTROL Last Updated]&quot;, um die gewünschte Eigenschaft anzuzeigen, und klicken Sie auf das Symbol &quot;[!UICONTROL Code]&quot;.

      ![Eigenschaften-Hover-Code](/help/main/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klicken Sie mit der rechten Maustaste auf den markierten Implementierungs-Code und kopieren Sie ihn in die Zwischenablage.

1. Aktualisieren Sie Ihre [!DNL Target] -Implementierung mit dem Implementierungscode, der im vorherigen Schritt abgerufen wurde.

   Die [!DNL Target]-Implementierung kann auf unterschiedliche Art aktualisiert werden. Für Webseiten können beispielsweise die folgenden Verfahren angewendet werden:

   * **Über einen &quot;benutzerdefinierten Parameter&quot;in Tags innerhalb von [!DNL Adobe Experience Platform]:**

     Weitere Informationen finden Sie unter [Mbox-Parameter hinzufügen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=en#add-mbox-params) in der Dokumentation *Tags - Übersicht* .

   * **Über die Funktion targetPageParamsAll():** Fügen Sie den folgenden Code in die `<head>` -Tags über der Referenz &quot;at.js&quot;ein.

     ```javascript
     <script>
      function targetPageParamsAll() {
       return {
        "at_property": "5f8bd98b-1456-a84c-2a96-11s9b8e2b112"
       };
      }
     </script>
     ```

     Weitere Informationen dazu, wie Sie dies mit at.js durchführen, finden Sie unter [targetPageParamsAll](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparamsall.html?lang=en){target=_blank}.

## Schritt 6: Rollen und Berechtigungen festlegen {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klicken Sie in der Admin Console auf **[!UICONTROL Products]** und wählen Sie dann den Produktnamen aus.

   ![Arbeitsbereich](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klicken Sie auf den Namen des gewünschten Profils (z. B. Default Workspace).

   ![Standardarbeitsbereich](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Klicken Sie auf **[!UICONTROL Users]**.

   Auf der Registerkarte [!UICONTROL Users] werden alle Benutzer in diesem Arbeitsbereich angezeigt.

   ![Konfigurationsbenutzer](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Wählen Sie die gewünschte Berechtigungsrolle (Genehmiger, Bearbeiter, Beobachter oder Herausgeber) mithilfe der Dropdownliste für jeden Benutzer in der Spalte [!UICONTROL Product Role] aus.

   ![Dropdownliste „Produktrolle“](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rolle | Beschreibung |
   |--- |--- |
   | Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
   | Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
   | Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
   | Publisher | Ähnlich wie die Beobachterrolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Publisher-Rolle zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

   Weitere Informationen finden Sie unter [Verwalten von Produktberechtigungen und Rollen in der Admin Console](https://helpx.adobe.com/de/enterprise/help/manage-permissions-and-roles.html) im *Enterprise-Benutzerhandbuch*.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

>[!NOTE]
>
>Die Menübenutzeroberfläche [!DNL Target] [!UICONTROL Administration] (ehemals [!UICONTROL Setup]) wurde neu gestaltet, um eine verbesserte Leistung, kürzere Wartungszeiten bei der Veröffentlichung neuer Funktionen und bessere Benutzererfahrung im gesamten Produkt zu erzielen. Die Informationen in den folgenden Videos sind im Allgemeinen korrekt. Optionen können sich jedoch an etwas anderen Orten befinden. Aktualisierte Videos werden bald veröffentlicht.

### Konfigurieren von Adobe Target-Arbeitsbereichen (6:55) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird das Erstellen von Arbeitsbereichen erläutert.

* Zugreifen auf die Adobe Admin Console über die Adobe Target-Schnittstelle (3 Methoden)
* Konfigurieren eines Arbeitsbereichs in Adobe Admin Console

   * Hinzufügen von Benutzern zu Arbeitsbereichen
   * Hinzufügen von Eigenschaften zu Arbeitsbereichen

* Grundlegende Informationen zu Standardarbeitsbereichen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Erstellen von Eigenschaften in Adobe Target (3:05) ![Tutorial-Badge](/help/main/assets/tutorial.png)

* Erstellen einer Eigenschaft auf der [!DNL Adobe Target]-Benutzeroberfläche
* Generieren eines Eigenschaftstokens zum Einfügen in die Eigenschaftenimplementierung
* Machen Sie sich mit den drei Implementierungsmethoden vertraut:

   * Web
   * Mobile App
   * E-Mail-, Set-Top-Box- oder API-Aufrufe

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
