---
keywords: Arbeitsbereiche;Eigenschaft verwalten;Berechtigungen;Produktkonfiguration;Produktprofil;Rollen;Projekt;Beobachter;Editor;Genehmiger;Publisher
description: Erfahren Sie, wie Sie separate Arbeitsbereiche (Produktprofile) erstellen und dann Benutzern verschiedene Rollen und Berechtigungen für einzelne Seiten, Eigenschaften oder Websites zuweisen.
title: Was sind Enterprise-Benutzerberechtigungen und wie verwende ich sie?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 838abe87-dba7-4274-97b4-31a7905846dc
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '3165'
ht-degree: 48%

---

# Berechtigungen für Unternehmensbenutzer

Enterprise-Benutzerberechtigungen sind eine Möglichkeit, den unternehmensweiten Benutzerzugriff auf [!DNL Adobe Target] formell zu verwalten. Fügen Sie Benutzer zu [!DNL Target] hinzu, weisen Sie Berechtigungen basierend auf deren Rollen zu und erstellen Sie Arbeitsbereiche für Teams basierend auf verschiedenen Abteilungen, globalen Standorten, Kanälen und anderen logischen Gruppierungen. Sie können Benutzern die Rollen [!UICONTROL Observer], [!UICONTROL Editor], [!UICONTROL Approver] oder [!UICONTROL Publisher] zuweisen.

## Ermitteln, ob Sie Zugriff auf Enterprise-Benutzerberechtigungen haben

>[!NOTE]
>
>[!UICONTROL Properties and Permissions] Funktion ist als Teil der [!DNL Target] Premium-Lösung verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>
>Ihre [!DNL Target] kann jede Version von at.js oder [!DNL Adobe Experience Platform Web SDK] verwenden.

Sie können feststellen, ob Ihr Unternehmen über eine Standard- oder Premium-Lizenz verfügt, indem Sie auf den [!UICONTROL Administration]-Link oben in der [!DNL Target] Benutzeroberfläche klicken.

* **[!DNL Target Standard]Kunden**: Wenn Sie die Registerkarte &quot;[!UICONTROL Users]&quot; ([!UICONTROL Administration > Users]) sehen (und nicht die Registerkarte &quot;[!UICONTROL Properties]„), verfügt Ihr Unternehmen über eine [!DNL Target Standard]. [!DNL Target Standard] Kunden sollten die Anweisungen in [Benutzer](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) befolgen, um in der [!DNL Adobe Admin Console] Benutzer hinzuzufügen und Berechtigungen zuzuweisen.

* **[!DNL Target Premium]Kunden**: Wenn Sie die Registerkarte &quot;[!UICONTROL Properties]&quot; ([!UICONTROL Administration > Properties]) und die Registerkarte &quot;[!UICONTROL Users]&quot; sehen, verfügt Ihr Unternehmen über eine [!DNL Target Premium]. [!DNL Target Premium]-Kunden sollten die Anweisungen in diesem Artikel und in [Konfigurieren von Unternehmensberechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) folgen.

## Bevor Sie mit Enterprise-Berechtigungen beginnen

>[!IMPORTANT]
>
>Lesen Sie den Abschnitt [Einschränkungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) unten, bevor Sie mit den Unternehmensberechtigungen fortfahren.

## In diesem Abschnitt verwendete Begriffe und Definitionen {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

Die folgenden Begriffe werden in diesem Abschnitt verwendet und sind möglicherweise für Benutzende neu, die die Funktionen „Eigenschaften“ und „Berechtigungen“ in [!DNL Target] Premium verwenden möchten.

### Eigenschaft

Eigenschaften ähneln Eigenschaften in [!DNL Adobe Experience Platform] insofern, als sie ein eindeutiges Code-Fragment zur Unterscheidung verwenden.

Eine Webeigenschaft besteht aus einer Bibliothek von Regeln und einem Einbettungscode. Es kann sich bei einer Webeigenschaft um eine beliebige Gruppierung einer oder mehrerer Domänen bzw. Subdomänen handeln.

Eigenschaften werden aktiviert, indem ein bestimmtes Name/Wert-Paar als Parameter bei jedem Aufruf (Target-Aufruf, API-Aufruf usw.) an [!DNL Target] hinzugefügt wird.

Eigenschaften sind bestimmten Kanälen (Web, mobil, E-Mail oder API/Sonstige) zugeordnet.

### Arbeitsbereich (Produktprofil) {#workspace}

Mithilfe eines Arbeitsbereichs können Organisationen bestimmte Benutzergruppen bestimmten Eigenschaftsgruppen zuweisen. Arbeitsbereiche ähneln auf vielerlei Weise den Report Suites in [!DNL Adobe Analytics].

Hinweis: Arbeitsbereiche werden in der [!DNL Adobe Admin Console for Enterprise] als [!UICONTROL Product Profiles] bezeichnet.

Wenn Sie Teil einer multinationalen Organisation sind, besitzen Sie eventuell einen Arbeitsbereich für Ihre europäischen Webseiten, Eigenschaften oder Sites und einen weiteren Arbeitsbereich für Ihre amerikanischen Webseiten, Eigenschaften oder Sites. Wenn Sie einer Organisation angehören, die mehrere Marken besitzt, haben Sie eventuell für jede Marke einen eigenen Arbeitsbereich.

Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen sogar unterschiedliche Rollen einnehmen.

Benutzer können unterschiedliche Ansichten von [!DNL Adobe Target] haben, wenn sie zwischen Arbeitsbereichen wechseln. Dies ähnelt [!DNL Analytics] unterschiedlichen Ansichten von [!DNL Analytics] durch den Wechsel zwischen Report Suites.

Arbeitsbereiche können völlig unterschiedliche Zielgruppen, Code-Angebote und Aktivitäten enthalten.

Alle Zielgruppen und Aktivitäten, die vor der Migration des neuen Enterprise-Berechtigungsmodells erstellt wurden, werden in der unten beschriebenen „Standard-Workspace&quot; gruppiert.

Alle Aktivitäten, die über [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] und [!DNL Adobe Target Classic] erstellt wurden, sind Teil der „Standard-Workspace&quot;.

### Standardarbeitsbereich

Alle vorhandenen Arbeitsbereiche (Produktprofile) in [!DNL Admin Console] werden während der Migration Ihres Unternehmens zum neuen Enterprise-Berechtigungsmodell in einem einzigen Arbeitsbereich namens „Standard-Workspace&quot; zusammengeführt.

>[!IMPORTANT]
>
>Löschen Sie den Standardarbeitsbereich nicht.

Alle Benutzerrollen und der Zugriff auf alle [!DNL Target] bleiben unverändert wie vor der Migration auf das neue Enterprise-Berechtigungsmodell.

### Benutzergruppen

Sie können Benutzergruppen erstellen, z. B. Entwickler, Analysten, Marketing-Experten und Führungskräfte. Anschließend können Sie Berechtigungen für mehrere Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

### Rollen und Berechtigungen {#roles-permissions}

Rollen und Berechtigungen legen die Zugriffsebenen fest, über die Benutzer Aktivitäten in Ihrer [!DNL Target]-Implementierung erstellen und verwalten müssen. In [!DNL Target] umfassen die Rollen Folgendes:

| Rolle | Beschreibung |
|--- |--- |
| [!UICONTROL Approver] | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
| [!UICONTROL Editor] | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
| [!UICONTROL Observer] | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
| [!UICONTROL Publisher] | Ähnlich wie die Rolle [!UICONTROL Observer] (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Die Rolle [!UICONTROL Publisher] verfügt jedoch zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

### Kanal

Der Kanal bezieht sich auf den Inhaltstyp, über den Ihre [!DNL Target] bereitgestellt werden: Web-Seiten, Mobile Apps, E-Mail-Nachrichten usw.

Wenn Sie eine Aktivität erstellen, wird diese im aktuell ausgewählten Arbeitsbereich erstellt. Im ersten Dialogfeld werden Optionen zur Kanalauswahl angezeigt, über die Sie den gewünschten Kanal für die Aktivität auswählen können: Web, Mobile App, E-Mail oder Sonstige/API.

## Berechtigungen - Übersicht {#section_DC2172520DA84605B218A5E9FB6D187A}

In den folgenden Informationen wird erläutert, wie Berechtigungen zuvor in [!DNL Target] erzwungen wurden und wie sie mithilfe der Funktionen [!UICONTROL Properties] und [!UICONTROL Permissions] erzwungen werden.

Mit der neuen [!UICONTROL Permissions] können Sie verschiedene Projekte erstellen (in der [!DNL Adobe Admin Console for Enterprise] als „Produktprofile“ bezeichnet). In „Projekte“ können Sie einem einzelnen Benutzer unterschiedliche Berechtigungen zuweisen, die dessen Zugriffsrechte für jedes Projekt festlegen. Diese voneinander unabhängigen Projekte funktionieren ähnlich wie Report Suites in [!DNL Adobe Analytics]. Jedes Projekt verfügt über bestimmte Benutzer mit bestimmten Rollen, die einer bestimmten Reihe Berechtigungen entsprechen. Dies hat zur Folge, dass Kundinnen und Kunden in der Lage sind, die Anzeige-, Bearbeitungs- und Genehmigungs-Zugriffsrechte für ihre Benutzenden auf der Grundlage von Region, Umgebung (dev/stage/prod), Kanal oder anderen benutzerdefinierten Kriterien einzuschränken, wie unten dargestellt:

![Bild für Berechtigungen](assets/permissions.png)

Ein bestimmter Benutzer verfügt beispielsweise über Genehmigungszugriff auf die Websites für Nord- und Südamerika, jedoch nur auf Ansichtszugriff auf die mobile App für Europa. Dieser Benutzer verfügt möglicherweise nicht über die nötigen Rechte, die in Web- und Mobileigenschaften angebotenen Aktivitäten der APAC-Region einzusehen.

Das [!DNL Target] [!UICONTROL Permissions]-Modell verfügt über die folgenden Berechtigungsrollen (Beobachter, Bearbeiter, Genehmiger und Beobachter). Die Beobachterrolle wird in den Abbildungen in diesem Artikel nicht angezeigt.

![permissions_1 Bild](assets/permissions_1.png)

Jede Rolle verfügt über eigene Zugriffsniveaus:

| Rolle | Beschreibung |
|--- |--- |
| Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
| Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
| Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
| Publisher | Ähnlich wie die Beobachterrolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Publisher-Rolle zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

Es muss dabei berücksichtigt werden, dass die Benutzerrolle für alle Seiten, Eigenschaften oder Sites Ihres Kontos gilt, die über [!DNL Target]-Tags verfügen, wie unten dargestellt:

![permissions_2 Bild](assets/permissions_2.png)

Das neue [!DNL Target]-[!UICONTROL Permissions]-Modell verfügt über dieselben drei Berechtigungsrollen (Beobachter, Bearbeiter und Genehmiger). Sie können jedoch die Berechtigungsrollen eines Benutzers für einzelne Seiten, Eigenschaften oder Sites separat zuweisen, wie unten dargestellt:

![permissions_3 image](assets/permissions_3.png)

In diesem Beispiel besitzt Jan Genehmigerrechte für die US-Homepage und die US-Site und Beobachterrechte für die französische Site.

Darüber hinaus kann Jan keine Seiten, Eigenschaften oder Websites in [!DNL Target] sehen, für die sie keine Berechtigung hat, wie unten dargestellt:

![permissions_4 Bild](assets/permissions_4.png)

In diesem Beispiel kann Jan die Produktseiten, die russische Site und die Karriere-Site nicht sehen.

## Anwendungsfälle {#section_F3CE8576959E4F4CB13BEEED38311DD8}

Die folgenden Anwendungsfälle zeigen wie Eigenschaften, Projekte, Rollen und Berechtigungen genutzt werden können, um Marketingziele mit [!DNL Target] zu erreichen:

### Multinationale Organisation

Wenn Sie Teil einer multinationalen Organisation sind, besitzen Sie eventuell einen Arbeitsbereich für Ihre europäischen Webseiten, Eigenschaften oder Sites und einen weiteren Arbeitsbereich für Ihre amerikanischen Webseiten, Eigenschaften oder Sites.
Nach einer Umstrukturierung richten Sie für die Personen aus der obigen Abbildung folgende Arbeitsbereiche und Berechtigungen ein:

* **Jan**: Jan leitet die Optimierungsabteilung im Center of Excellence für die US-Webseiten, -Objekte und -Sites ihrer Organisation. Sie besitzt Systemadministratorrechte in der Adobe Experience Cloud.

  In ihrer Rolle hat sie Genehmigerberechtigungen für die US-Homepage und die US-Site. Mit der Berechtigung Genehmigende Person kann sie Aktivitäten erstellen, bearbeiten und aktivieren oder stoppen.

  Jan berät außerdem das Optimierungsteam in Frankreich und besitzt daher Beobachterrechte für die französische Site, die ihr Leserechte für Aktivitäten gewähren. Jan kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

  Da Jan keine Rolle besitzt, für die sie die Produktseiten, die russische Site oder die Karriere-Site sehen muss, kann sie für diese Sites keine Aktivitäten sehen.

* **Ernie**: Ernie ist Marketingleiter der Organisation und für das Marketing in den USA zuständig.

  Da Ernie recht neu in der Organisation ist und noch nicht mit Target vertraut ist, verfügt er über Editor-Berechtigungen für die US-Homepage, die US-Site und die Produktseiten. Mit Editor-Berechtigungen kann Ernie Aktivitäten erstellen und bearbeiten, bevor sie live sind. Er kann den Start einer Aktivität nicht genehmigen. Eine Person mit der Berechtigung „Genehmigung“, wie z. B. Jan, muss die Aktivität genehmigen, bevor sie in die Produktion aufgenommen werden kann.

  Da Ernie keine Rolle besitzt, für die er die russische Site, die französische Site oder die Karriere-Site sehen muss, kann er für diese Sites keine Aktivitäten sehen.

* **Diana**: Diana arbeitet jetzt als Analystin für die Organisation. Ihr wurden Beobachterberechtigungen für die US-Homepage, -Site, -Produktseiten und die russische und die französische Site zugewiesen, mit denen sie reinen Lesezugriff auf Aktivitäten hat. Diana kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

  Da Diana keine Rolle besitzt, für die sie die Karriere-Site sehen muss, kann sie für diese Site keine Aktivitäten sehen.

### Organisation mit mehreren Marken

Wenn Sie zu einer Organisation mit mehreren Marken gehören, besitzen Sie womöglich einen separaten Arbeitsbereich für die Webseiten, Eigenschaften oder Sites der einzelnen Marken.

Nach einer Umstrukturierung richten Sie für die Personen aus der obigen Abbildung folgende Projekte und Berechtigungen ein:

* **Jan**: Jan leitet die Optimierungsabteilung im Center of Excellence für eine Organisation im Gesundheitswesen, die getrennte Produktbereiche für Krankenhäuser und für Endverbraucher betreibt. Sie besitzt Systemadministratorrechte in der Adobe Experience Cloud.

  In ihrer Rolle besitzt sie Genehmigerrechte für die Krankenhaus-Site. Mit der Berechtigung Genehmigende Person kann sie Aktivitäten erstellen, bearbeiten und aktivieren oder stoppen.

  Jan berät außerdem das Optimierungsteam des Produktbereichs für Endverbraucher und besitzt daher Beobachterrechte für diese Site, die ihr Leserechte für Aktivitäten gewähren. Jan kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

* **Ernie**: Ernie ist Marketingleiter der Organisation für das Marketing des Produktbereichs für Endverbraucher.

  Da Ernie recht neu in der Organisation ist und noch nicht mit Target vertraut ist, hat er die Berechtigung zum Editor für die Consumer-Site. Mit Editor-Berechtigungen kann Ernie Aktivitäten erstellen und bearbeiten, bevor sie live sind. Er kann den Start einer Aktivität nicht genehmigen. Eine Person mit Berechtigungen zum Genehmigen für die Verbraucher-Site, in diesem Szenario jedoch nicht Jan, muss die Aktivität genehmigen, bevor sie in die Produktion aufgenommen werden kann.

  Da Ernie keine Rolle besitzt, für die er die Krankenhaus-Site sehen muss, kann er für diese Site keine Aktivitäten sehen.

* **Diana**: Diana arbeitet jetzt als Analystin für die Organisation. Ihr wurden Beobachterberechtigungen für die Krankenhaus- und die Endverbraucher-Sites zugewiesen, mit denen sie reinen Lesezugriff auf Aktivitäten hat. Diana kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

## Touchpoints der Target-Benutzeroberfläche für Eigenschaften und Berechtigungen {#section_3414371393BB42999A268628B5456EC9}

Die neue Berechtigungsfunktion findet sich in der Benutzeroberfläche von [!DNL Target] gleich an mehreren Orten.

* **Dropdown-Liste &quot;Workspace&quot; (Produktprofil):** Die Dropdown-Liste &quot;Workspace&quot; wird oben auf den Seiten &quot;[!UICONTROL Activities]&quot;, &quot;[!UICONTROL Audiences]&quot; und &quot;[!UICONTROL Offers]&quot; angezeigt. Wählen Sie den gewünschten Arbeitsbereich aus, um die Liste zu filtern und nur die Elemente des ausgewählten Arbeitsbereichs anzuzeigen.

* **Aktivitätserstellung** Wenn Sie eine Aktivität erstellen, wird sie im aktuell ausgewählten Arbeitsbereich erstellt. Im ersten Dialogfeld werden Optionen zur Kanalauswahl angezeigt, über die Sie den gewünschten Kanal für die Aktivität auswählen können: Web, Mobile App, E-Mail oder Sonstige/API.

* **Zielgruppenerstellung:** Sie eine Zielgruppe erstellen, wird sie im aktuell ausgewählten Arbeitsbereich erstellt.
* **Audience-Liste:** Mithilfe der Option [!UICONTROL More Actions] > [!DNL Move] auf der [!UICONTROL Audiences] können Sie Audiences zwischen Arbeitsbereichen verschieben.
* **Angebotserstellung:** Wenn Sie ein Angebot erstellen, wird es im aktuell ausgewählten Arbeitsbereich erstellt.
* **Eigenschaftenseite (Administration > Eigenschaften):** Sie können das [!UICONTROL Search] verwenden, um die [!UICONTROL Property] zu durchsuchen.

## Einschränkungen  {#section_9714311B1CD9497A86F4910F8AE635E2}

Beachten Sie bei der Verwendung oder Konfiguration von Eigenschaften und Berechtigungen in [!DNL Target] Premium Folgendes:

* **Wichtig**: Löschen Sie keine Arbeitsbereiche mit Aktivitäten. Wenn Sie einen Arbeitsbereich mit Aktivitäten löschen, wenden Sie sich an die Kundenunterstützung, um diese Aktivitäten wiederherzustellen.
* Bei der Verwendung der Ansicht „Alle meine Arbeitsbereiche“ gilt Folgendes:

   * Sie können Aktivitäten, Zielgruppen und Angebote für alle Arbeitsbereiche anzeigen, für die Sie über die erforderlichen Rollen und Zugriffsberechtigungen verfügen.
   * Wenn Sie die Ansicht [!UICONTROL All My Workspaces] auswählen, wird eine neue Spalte zur Seite Aktivitäten, Zielgruppen und Angebote hinzugefügt. In dieser Spalte werden der Arbeitsbereich des Elements und Ihre mit diesem Element verknüpfte Benutzerberechtigung (Beobachter, Bearbeiter oder Genehmiger) aufgeführt.
   * Wenn Sie eine Aktivität, eine Zielgruppe oder ein Angebot in der Ansicht „Alle meine Arbeitsbereiche“ erstellen, müssen Sie den Arbeitsbereich auswählen, in dem das Element erstellt werden soll. Hierbei können Sie nur Arbeitsbereiche auswählen, für die Sie über Editor- oder Genehmiger-Berechtigungen verfügen.
   * Wenn Sie eine Aktivität, eine Zielgruppe oder ein Angebot in der Ansicht „Alle meine Arbeitsbereiche“ kopieren, müssen Sie den Arbeitsbereich auswählen, in den das Element kopiert werden soll. Hierbei können Sie nur Arbeitsbereiche auswählen, für die Sie über Editor- oder Genehmiger-Berechtigungen verfügen.

* Jede Einstellung auf den folgenden [!UICONTROL Administration] kann von jedem [!UICONTROL Approver] in jedem Arbeitsbereich gesteuert werden:

   * Visual Experience Composer
   * Berichterstellung
   * Scene7-Konfiguration
   * Implementierung
   * Eigenschaften
   * Hosts
   * Umgebungen
   * Antwort-Token
   * Benutzende

* Benutzer können keine Ressourcen zwischen Arbeitsbereichen (Produktprofilen) verschieben. Das Kopieren wird jedoch unterstützt.
* Beim Anzeigen der Zielgruppen über die [!DNL Audiences]-Seite lädt die Seite langsamer als erwartet. Nutzen Sie das Suchfeld, werden die Zielgruppen schneller geladen. Dieses Problem ist bekannt und wird in einer kommenden Aktualisierung behoben. Das Problem wirkt sich nicht auf die Auswahl von Zielgruppen bei der Erstellung von Aktivitäten aus.
* Die folgenden Ressourcen sind Teil des neuen Unternehmensberechtigungsmodells:

   * In [!DNL Target Standard/Premium] erstellte Aktivitäten, Zielgruppen und Code-Angebote können verwendet werden, nachdem der Kunde die Berechtigungen aktiviert hat. (Hinweis: Kunden müssen Anspruch auf [!DNL Target Premium] haben.)
   * Eigenschaften können zu bestehenden Aktivitäten in der Standard-Workspace hinzugefügt werden. Dieser Ansatz kann sich jedoch ändern.
   * Nur neue Ressourcen (wie Aktivitäten, Code-Angebote und Zielgruppen), die in Target Premium erstellt wurden (nachdem Enterprise-Berechtigungen aktiviert wurden), können durch -Berechtigungen eingeschränkt werden.
   * Externe Ressourcen sind nur für Benutzer im Standardarbeitsbereich verfügbar. Die Rolle eines Benutzers im Standardarbeitsbereich ist global gültig (für alle Target-Anfragen und alle Taget-Ressourcen).

* Die folgenden Ressourcen sind *nicht* Teil des neuen Unternehmensberechtigungsmodells:

   * Bildangebote
   * Alle Recommendations-Ressourcen, einschließlich Kriterienbibliothek, Designbibliothek, Katalog, Recommendations-Einrichtung.
   * Vorhandene Ressourcen (z. B. Aktivitäten, Code-Angebote und Zielgruppen), die in Target Premium vor der Aktivierung von Enterprise-Berechtigungen erstellt wurden, können kopiert, aber nicht in andere Arbeitsbereiche verschoben werden.
   * Aktivitäten, Audiences, Codeangebote, Bildangebote oder andere Ressourcen, die mit den folgenden Lösungen oder Methoden erstellt wurden, können nicht mit dem Enterprise-Berechtigungsmodell gesteuert werden, sind jedoch Teil der Standard-Workspace: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services und Ressourcen, die über die API erstellt wurden. Unter über die API erstellte Ressourcen fallen Aktivitäten, Audiences, Codeangebote und Bildangebote).
   * Bildangebote (Assets), die unter `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` gespeichert werden, können derzeit nicht vom Enterprise-Berechtigungsmodell gesteuert werden.
   * clickTracking und Weiterleitungen funktionieren, wenn der Ziel-Link oder die Zielseite Teil einer Eigenschaft ist, die in der Aktivität enthalten ist. Außerdem funktioniert das clickTracking bei Verwendung der Funktion `targetPageParams()` möglicherweise nicht. `targetPageParamsAll()` ist die empfohlene Funktion.

  [!DNL Target] erfordert derzeit, dass auf jeder Seite, auf der Tracking stattfindet, ein `at_property`-Token vorhanden ist. Wenn das Token (1) nicht vorhanden ist, (2) zum Zeitpunkt der Aktivitätseinrichtung (innerhalb des VEC) nicht erkannt wurde oder (3) nicht über die Funktion `targetPageParamsAll()` an den Aufruf von ClickTracking Target übergeben wurde, wird die Metrik nicht inkrementiert und als „0“ angezeigt.

  Dasselbe gilt für Aktivitäten, die Umleitungen verwenden. Auf der Zielseite muss ein `at_property`-Token vorhanden sein, das beim Einrichten in VEC erkannt wird.

  In einer künftigen Version wird Target auf Seiten, auf denen kein `at_property`-Token existiert, oder auf Seiten, auf denen ein anderes `at_property`-Token vorhanden ist, funktionieren.

* Die Enterprise-Benutzerberechtigungen werden in Adobe Developer-API-Aufrufen nicht unterstützt.

## Häufig gestellte Fragen   {#faqs}

Häufig gestellte Fragen zu Unternehmensberechtigungen:

### Was passiert, wenn eine Benutzerin oder ein Benutzer über mehrere Rollen und Berechtigungen verfügt? {#multiple-roles}

Wenn ein Benutzer über mehrere Rollen und Berechtigungen verfügt, wird die Rolle mit den höheren Berechtigungen angewendet. Wenn ein Benutzer beispielsweise über [!UICONTROL Observer] und [!UICONTROL Approver] Rollen verfügt, wird die [!UICONTROL Approver] Rolle angewendet.

### Kann ich eine Aktivität von einem Arbeitsbereich in einen anderen verschieben?

Leider ist es nicht möglich, Aktivitäten von einem Arbeitsbereich in einen anderen zu verschieben. Sie können jedoch eine Aktivität in einen beliebigen Arbeitsbereich kopieren, da Sie wissen, dass Berichtsdaten nicht übernommen werden. Weitere Informationen finden Sie unter „Kopieren/Bearbeiten einer Aktivität beim Verwenden von Arbeitsbereichen“ in [Kopieren/Bearbeiten einer Aktivität beim Verwenden von Arbeitsbereichen](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Aktivitäten, die vor der Migration angelegt wurden, laufen im Standardarbeitsbereich auf die gleiche Weise weiter, es sei denn, sie werden bearbeitet und mit Eigenschaften versehen. Aktivitäten in einem bestimmten Arbeitsbereich berücksichtigen die Eigenschaft, die diesem Arbeitsbereich zugewiesen wurde, und daher bleibt das Verhalten möglicherweise nicht dasselbe wie vor der Migration.

### Kann ich eine Zielgruppe von einem Arbeitsbereich in einen anderen verschieben? {#move-audience}

Ja, Sie können Zielgruppen zwischen Arbeitsbereichen verschieben, indem Sie die Option [!UICONTROL More Actions] auf der Seite [!UICONTROL Audiences] verwenden.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL More Actions]** (die drei Auslassungspunkte) und dann auf **[!UICONTROL Move]**.

   ![Weitere Aktionen > Verschieben](/help/main/administrating-target/c-user-management/property-channel/assets/move-audience.png)

1. Wählen Sie den gewünschten Arbeitsbereich aus der Dropdown-Liste **[!UICONTROL Workspace]** aus und klicken Sie dann auf **[!UICONTROL Move]**.

   ![Wählen Sie die gewünschte Zielgruppe aus, um zu einem neuen Arbeitsbereich zu wechseln](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-move.png)

>[!NOTE]
>
>Sie müssen über die entsprechenden Berechtigungen verfügen, um eine Zielgruppe zu bearbeiten. Darüber hinaus darf die Zielgruppe nicht in anderen Aktivitäten verwendet werden. Wenn die Zielgruppe für andere Aktivitäten verwendet wird und Sie die Zielgruppe dennoch an einen anderen Arbeitsplatz verschieben möchten, entfernen Sie die Zielgruppe aus den anderen Aktivitäten, in denen sie verwendet wird.

### Warum wird eine Fehlermeldung angezeigt, die besagt, dass keine Eigenschaft mit dieser Aktivität verknüpft ist, auch wenn eine Eigenschaft zugewiesen ist?

Wenn Sie [!DNL Target] mit Tags in [!DNL Adobe Experience Platform] implementiert haben und eine Fehlermeldung erscheint, die angibt, dass mit der Aktivität keine Eigenschaft verknüpft ist, übergeben Sie den `at_property` mit der `targetPageParams`.

### Werden Klick-Tracking-Konversionen aufgezeichnet, wenn eine umgeleitete Seite und die Aktivitäts-URL zu unterschiedlichen Eigenschaften gehören?

Klick-Tracking wird nicht auf Seiten aufgezeichnet, wo die Seite und die Aktivitäts-URL zu unterschiedlichen Präsenzen gehören.

Betrachten wir das folgende Szenario:

* Seite 1 gehört zu Präsenz1.
* Seite 2 gehört zu Präsenz2.
* In der Aktivität leitet Seite 1 auf Seite 2 weiter, die Klick-Tracks enthält.

Wenn ein Besucher Page1 in einem Browser öffnet, wird der Besucher zu Page2 weitergeleitet. Da Seite 2 nicht zur Bereitstellung der Aktivität berechtigt ist, enthält der Target-Aufruf keine Klick-Tracks in der Antwort.

Wenn die Weiterleitungsseite und die Aktivitäts-URL zu derselben Eigenschaft gehören, funktionieren die Klick-Tracks erwartungsgemäß. Weitere Informationen finden Sie unter [Klick-Tracking](/help/main/c-activities/r-success-metrics/click-tracking.md).

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Schulungsvideo: Schulungsvideo zu Enterprise-Berechtigungen ![Übersichts-Badge](/help/main/assets/overview.png)

Lernziele:

* Die drei möglichen Rollenebenen von Adobe Target-Benutzern
* Die Konzepte von Eigenschaften und Arbeitsbereichen und wie diese Grenzen und Gruppierungen funktionieren, um die Zugangsebenen der Benutzer steuern zu können
* Verschiedene Beispiele für Eigenschaften für Ihre Organisation

>[!VIDEO](https://video.tv.adobe.com/v/19042/)

### Office Hours: [!DNL Target] Premium-Arbeitsbereiche

Dieses Video ist eine Aufzeichnung von Office Hours, einer Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* Erstellen von Arbeitsbereichen (Produktprofilen)
* Erstellen von Eigenschaften
* Hinzufügen von Benutzern
* Aktualisieren der Implementierung

>[!NOTE]
>
>Die Benutzeroberfläche des [!DNL Target] [!UICONTROL Administration]-Menüs (früher [!UICONTROL Setup]) wurde überarbeitet, um eine verbesserte Leistung zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu reduzieren und das Benutzererlebnis im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind korrekt. Die Optionen können sich jedoch an etwas anderen Stellen befinden.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
