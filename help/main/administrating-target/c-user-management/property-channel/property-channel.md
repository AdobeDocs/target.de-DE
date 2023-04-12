---
keywords: Arbeitsbereiche;Eigenschaft verwalten;Berechtigungen;Produktkonfiguration;Produktprofil;Rollen;Projekt;Beobachter;Editor;Genehmiger;Herausgeber
description: Erfahren Sie, wie Sie separate Arbeitsbereiche (Produktprofile) erstellen und dann Benutzern unterschiedliche Rollen und Berechtigungen für einzelne Seiten, Eigenschaften oder Websites zuweisen.
title: Was sind Unternehmensbenutzerberechtigungen und wie verwende ich sie?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 838abe87-dba7-4274-97b4-31a7905846dc
source-git-commit: 1b46d42e082b4f797064df1ff0c1b75907af4dd0
workflow-type: tm+mt
source-wordcount: '3215'
ht-degree: 57%

---

# Berechtigungen für Unternehmensbenutzer

Berechtigungen für Unternehmensbenutzer sind ein Mittel zur formalen Verwaltung des unternehmensweiten Benutzerzugriffs auf [!DNL Adobe Target]. Benutzer hinzufügen zu [!DNL Target], weisen Sie Berechtigungen basierend auf ihren Rollen zu und erstellen Sie Arbeitsbereiche für Teams basierend auf verschiedenen Abteilungen, globalen Standorten, Kanälen und anderen logischen Gruppierungen. Sie können Benutzern die Rollen von [!UICONTROL Beobachter], [!UICONTROL Editor], [!UICONTROL Genehmiger]oder [!UICONTROL Herausgeber].

## Bestimmen, ob Sie Zugriff auf Unternehmensbenutzerberechtigungen haben

>[!NOTE]
>
>Die Funktionalitäten für [!UICONTROL Eigenschaften und Berechtigungen] sind als Bestandteil der Lösung [!DNL Target] Premium verfügbar. Für [!DNL Target] Standard sind sie nicht ohne [!DNL Target] Premium-Lizenz verfügbar.
>
>Ihre [!DNL Target] -Implementierung kann jede Version von at.js verwenden.

Sie können feststellen, ob Ihr Unternehmen über eine Standard- oder Premium-Lizenz verfügt, indem Sie oben in der [!DNL Target]-Benutzeroberfläche auf den Link [!UICONTROL Administration] klicken.

* **[!DNL Target Standard]Kunden**: Wenn die Variable [!UICONTROL Benutzer] tab ([!UICONTROL Administration > Benutzer]) (und nicht das [!UICONTROL Eigenschaften] -Registerkarte), verfügt Ihre Organisation über eine [!DNL Target Standard] Lizenz. [!DNL Target Standard] -Kunden sollten die Anweisungen unter [Benutzer](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) , um Benutzer hinzuzufügen und Berechtigungen in der [!DNL Adobe Admin Console].

* **[!DNL Target Premium]Kunden**: Wenn die Variable [!UICONTROL Eigenschaften] tab ([!UICONTROL Administration > Eigenschaften]) und der [!UICONTROL Benutzer] -Registerkarte, verfügt Ihre Organisation über eine [!DNL Target Premium] Lizenz. [!DNL Target Premium]-Kunden sollten die Anweisungen in diesem Artikel und in [Konfigurieren von Unternehmensberechtigungen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) folgen.

## Erste Schritte mit Unternehmensberechtigungen

>[!IMPORTANT]
>
>Stellen Sie sicher, dass Sie die [Einschränkungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) unten beschrieben, bevor Sie mit den Unternehmensberechtigungen fortfahren.

## In diesem Abschnitt verwendete Begriffe und Definitionen {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

Die folgenden Begriffe werden in diesem Abschnitt verwendet und können für Benutzer, die die Funktion für Eigenschaften und Berechtigungen in [!DNL Target] Premium.

### Eigenschaft

Eigenschaften ähneln den Eigenschaften in [!DNL Adobe Experience Platform] , da sie einen eindeutigen Codeausschnitt verwenden, um sie zu unterscheiden.

Eine Webeigenschaft besteht aus einer Bibliothek von Regeln und einem Einbettungscode. Es kann sich bei einer Webeigenschaft um eine beliebige Gruppierung einer oder mehrerer Domänen bzw. Subdomänen handeln.

Eigenschaften werden aktiviert, indem ein bestimmtes Name/Wert-Paar als Parameter mit einem beliebigen Aufruf (Target-Aufruf, API-Aufruf usw.) zu [!DNL Target].

Eigenschaften sind bestimmten Kanälen (Web, mobil, E-Mail oder API/Sonstige) zugeordnet.

### Arbeitsbereich (Produktprofil)

Mithilfe eines Arbeitsbereichs können Organisationen bestimmte Benutzergruppen bestimmten Eigenschaftsgruppen zuweisen. Arbeitsbereiche ähneln auf vielerlei Weise den Report Suites in [!DNL Adobe Analytics].

Hinweis: Arbeitsbereiche werden als [!UICONTROL Produktprofile] im [!DNL Adobe Admin Console for Enterprise].

Wenn Sie Teil einer multinationalen Organisation sind, besitzen Sie eventuell einen Arbeitsbereich für Ihre europäischen Webseiten, Eigenschaften oder Sites und einen weiteren Arbeitsbereich für Ihre amerikanischen Webseiten, Eigenschaften oder Sites. Wenn Sie einer Organisation angehören, die mehrere Marken besitzt, haben Sie eventuell für jede Marke einen eigenen Arbeitsbereich.

Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen sogar unterschiedliche Rollen einnehmen.

Benutzer können unterschiedliche Ansichten von [!DNL Adobe Target] durch Wechsel zwischen Arbeitsbereichen, ähnlich wie beim [!DNL Analytics] -Benutzer haben unterschiedliche Ansichten von [!DNL Analytics] durch Wechsel zwischen Report Suites.

Arbeitsbereiche können vollständig verschiedene Zielgruppen, Codeangebote und Aktivitäten beinhalten.

Alle Zielgruppen und Aktivitäten, die vor der neuen Migration des Unternehmensberechtigungsmodells erstellt wurden, werden im &quot;Standardarbeitsbereich&quot;gruppiert, wie nachfolgend beschrieben.

Alle über erstellten Aktivitäten [!DNL Adobe Experience Manager] AEM [!DNL Adobe Mobile Services]und [!DNL Adobe Target Classic] sind Teil des &quot;Standardarbeitsbereichs&quot;.

### Standardarbeitsbereich

Alle vorhandenen Arbeitsbereiche (Produktprofile) in [!DNL Admin Console] werden während der Migration Ihres Unternehmens zum neuen Unternehmensberechtigungsmodell in einen einzigen Arbeitsbereich namens &quot;Standardarbeitsbereich&quot;zusammengeführt.

>[!IMPORTANT]
>
>Löschen Sie den Standardarbeitsbereich nicht.

Alle Benutzerrollen und Zugriff auf alle [!DNL Target] Die -Funktion bleibt mit der vor der Migration zum neuen Unternehmensberechtigungsmodell identisch.

### Benutzergruppen

Sie können Benutzergruppen wie Entwickler, Analysten, Marketingexperten, Führungskräfte usw. erstellen. Anschließend können Sie Berechtigungen für mehrere Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

### Rollen und Berechtigungen

Rollen und Berechtigungen bestimmen, welche Zugriffsebene Benutzer haben, um Aktivitäten in der [!DNL Target]-Implementierung zu erstellen und zu verwalten. In [!DNL Target] gibt es folgende Rollen:

| Rolle | Beschreibung |
|--- |--- |
| [!UICONTROL Genehmiger] | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
| [!UICONTROL Bearbeiter] | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
| [!UICONTROL Beobachter] | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
| [!UICONTROL Publisher] | Ähnlich wie bei [!UICONTROL Beobachter] Rolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Rolle [!UICONTROL Publisher] zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

### Kanal

Der Kanal gibt den Content-Typ an, in dem Ihre [!DNL Target]-Aktivitäten bereitgestellt werden: Webseiten, mobile Apps, E-Mail-Nachrichten usw.

Wenn Sie eine Aktivität erstellen, wird sie im derzeit ausgewählten Arbeitsbereich erstellt. Im ersten Dialogfeld, in dem Sie den gewünschten Kanal für die Aktivität auswählen können, werden Optionen zur Kanalauswahl angezeigt: Web, mobile App, E-Mail oder Sonstige/API.

## Übersicht über Berechtigungen {#section_DC2172520DA84605B218A5E9FB6D187A}

Die folgenden Informationen erläutern, wie Berechtigungen zuvor in [!DNL Target] umgesetzt wurden und wie sie mit der neuen Funktion für [!UICONTROL Eigenschaften] und [!UICONTROL Berechtigungen] umgesetzt werden.

Die neue [!UICONTROL Berechtigungen] -Funktion können Sie verschiedene Projekte (die so genannten &quot;Produktprofile&quot;im [!DNL Adobe Admin Console for Enterprise]). Projekte ermöglichen es Ihnen, einem einzelnen Benutzer verschiedene Berechtigungen zuzuweisen, die die Zugriffsrechte dieses Benutzers für jedes Projekt vorschreiben. Diese voneinander unabhängigen Projekte funktionieren ähnlich wie Report Suites in [!DNL Adobe Analytics]. Jedes Projekt verfügt über bestimmte Benutzer mit bestimmten Rollen, die einer bestimmten Reihe Berechtigungen entsprechen. Das Ergebnis ist, dass Kunden den Ansichts-, Bearbeitungs- und Genehmigungszugriff auf ihre Benutzer anhand von Regionen, Umgebungen (Entwicklung/Staging/Produktion), Kanälen oder anderen benutzerdefinierten Kriterien einschränken können, wie unten dargestellt:

![Berechtigungsbild](assets/permissions.png)

Ein bestimmter Benutzer verfügt beispielsweise über Genehmigungszugriff auf die Websites für Nord- und Südamerika, jedoch nur auf Ansichtszugriff auf die mobile App für Europa. Dieser Benutzer verfügt möglicherweise nicht über die nötigen Rechte, die in Web- und Mobileigenschaften angebotenen Aktivitäten der APAC-Region einzusehen.

Im aktuellen [!DNL Target] [!UICONTROL Berechtigungsmodell] gibt es drei Rollen (Beobachter, Bearbeiter und Genehmiger), die in folgender Abbildung dargestellt werden:

![permissions_1 image](assets/permissions_1.png)

Jede Rolle verfügt über eigene Zugriffsniveaus:

| Rolle | Beschreibung |
|--- |--- |
| Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |
| Bearbeiter | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
| Beobachter | Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
| Publisher | Ähnlich wie die Beobachterrolle (kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten). Jedoch verfügt die Publisher-Rolle zusätzlich über die Berechtigung zum Aktivieren von Aktivitäten. |

Es muss dabei berücksichtigt werden, dass die Benutzerrolle für alle Seiten, Eigenschaften oder Sites Ihres Kontos gilt, die über [!DNL Target]-Tags verfügen, wie unten dargestellt:

![permissions_2 image](assets/permissions_2.png)

Das neue [!DNL Target][!UICONTROL -Berechtigungsmodell] verfügt über die gleichen drei Rollen (Beobachter, Bearbeiter und Genehmiger), einem Benutzer können jedoch verschiedene Rollen für einzelne Seiten, Eigenschaften oder Sites zugewiesen werden, wie unten dargestellt:

![permissions_3 image](assets/permissions_3.png)

In diesem Beispiel besitzt Jan Genehmigerrechte für die US-Homepage und die US-Site und Beobachterrechte für die französische Site.

Außerdem kann Jan keine Seiten, Eigenschaften oder Sites in [!DNL Target] dass sie nicht über die folgenden Berechtigungen zum Anzeigen verfügt:

![permissions_4 image](assets/permissions_4.png)

In diesem Beispiel kann Jan die Produktseiten, die russische Site und die Karriere-Site nicht sehen.

## Anwendungsfälle {#section_F3CE8576959E4F4CB13BEEED38311DD8}

Die folgenden Anwendungsfälle zeigen wie Eigenschaften, Projekte, Rollen und Berechtigungen genutzt werden können, um Marketingziele mit [!DNL Target] zu erreichen:

### Multinationale Organisation

Wenn Sie Teil einer multinationalen Organisation sind, besitzen Sie eventuell einen Arbeitsbereich für Ihre europäischen Webseiten, Eigenschaften oder Sites und einen weiteren Arbeitsbereich für Ihre amerikanischen Webseiten, Eigenschaften oder Sites.
Nach einer Umstrukturierung richten Sie für die Personen aus der obigen Abbildung folgende Arbeitsbereiche und Berechtigungen ein:

* **Jan**: Jan leitet die Optimierungsabteilung im Center of Excellence für die US-Webseiten, -Objekte und -Sites ihrer Organisation. Sie besitzt Systemadministratorrechte in der Adobe Experience Cloud.

   In ihrer Rolle hat sie Genehmigerberechtigungen für die US-Homepage und die US-Site. Mit den Genehmigerberechtigungen kann sie Aktivitäten erstellen, bearbeiten und aktivieren oder stoppen.

   Jan berät außerdem das Optimierungsteam in Frankreich und besitzt daher Beobachterrechte für die französische Site, die ihr Leserechte für Aktivitäten gewähren. Jan kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

   Da Jan keine Rolle besitzt, für die sie die Produktseiten, die russische Site oder die Karriere-Site sehen muss, kann sie für diese Sites keine Aktivitäten sehen.

* **Ernie**: Ernie ist Marketingleiter der Organisation und für das Marketing in den USA zuständig.

   Da Ernie recht neu in der Organisation ist und keine Erfahrung mit Target hat, besitzt er Editor-Berechtigungen für die US-Homepage, die US-Site und Produktseiten. Mit Bearbeiterberechtigungen kann Ernie Aktivitäten erstellen und bearbeiten, bevor sie live sind. Er kann den Start einer Aktivität nicht genehmigen. Jemand mit Genehmigungsberechtigungen, z. B. Jan, muss die Aktivität genehmigen, bevor sie in die Produktion aufgenommen werden kann.

   Da Ernie keine Rolle besitzt, für die er die russische Site, die französische Site oder die Karriere-Site sehen muss, kann er für diese Sites keine Aktivitäten sehen.

* **Diana**: Diana arbeitet jetzt als Analystin für die Organisation. Ihr wurden Beobachterberechtigungen für die US-Homepage, -Site, -Produktseiten und die russische und die französische Site zugewiesen, mit denen sie reinen Lesezugriff auf Aktivitäten hat. Diana kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

   Da Diana keine Rolle besitzt, für die sie die Karriere-Site sehen muss, kann sie für diese Site keine Aktivitäten sehen.

### Organisation mit mehreren Marken

Wenn Sie zu einer Organisation mit mehreren Marken gehören, besitzen Sie womöglich einen separaten Arbeitsbereich für die Webseiten, Eigenschaften oder Sites der einzelnen Marken.

Nach einer Umstrukturierung richten Sie für die Personen aus der obigen Abbildung folgende Projekte und Berechtigungen ein:

* **Jan**: Jan leitet die Optimierungsabteilung im Center of Excellence für eine Organisation im Gesundheitswesen, die getrennte Produktbereiche für Krankenhäuser und für Endverbraucher betreibt. Sie besitzt Systemadministratorrechte in der Adobe Experience Cloud.

   In ihrer Rolle besitzt sie Genehmigerrechte für die Krankenhaus-Site. Mit den Genehmigerberechtigungen kann sie Aktivitäten erstellen, bearbeiten und aktivieren oder stoppen.

   Jan berät außerdem das Optimierungsteam des Produktbereichs für Endverbraucher und besitzt daher Beobachterrechte für diese Site, die ihr Leserechte für Aktivitäten gewähren. Jan kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

* **Ernie**: Ernie ist Marketingleiter der Organisation für das Marketing des Produktbereichs für Endverbraucher.

   Da Ernie recht neu in der Organisation ist und keine Erfahrung mit Target hat, besitzt er Bearbeiterrechte für die Endverbraucher-Site. Mit Bearbeiterberechtigungen kann Ernie Aktivitäten erstellen und bearbeiten, bevor sie live sind. Er kann den Start einer Aktivität nicht genehmigen - jemand mit Genehmigungsberechtigungen für die Endverbraucher-Site, in diesem Szenario jedoch nicht Jan, muss die Aktivität genehmigen, bevor sie in die Produktion aufgenommen werden kann.

   Da Ernie keine Rolle besitzt, für die er die Krankenhaus-Site sehen muss, kann er für diese Site keine Aktivitäten sehen.

* **Diana**: Diana arbeitet jetzt als Analystin für die Organisation. Ihr wurden Beobachterberechtigungen für die Krankenhaus- und die Endverbraucher-Sites zugewiesen, mit denen sie reinen Lesezugriff auf Aktivitäten hat. Diana kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

## Touchpoints der Target-Benutzeroberfläche für Eigenschaften und Berechtigungen {#section_3414371393BB42999A268628B5456EC9}

Die neue Berechtigungsfunktion findet sich in der Benutzeroberfläche von [!DNL Target] gleich an mehreren Orten.

* **Dropdownliste „Arbeitsbereich“ (Produktprofil):** Die Dropdownliste „Arbeitsbereich“ wird am oberen Rand der Seiten [!UICONTROL Aktivitäten], [!UICONTROL Zielgruppen] und [!UICONTROL Angebote] angezeigt. Wählen Sie den gewünschten Arbeitsbereich aus, um die Liste zu filtern und nur die Elemente des ausgewählten Arbeitsbereichs anzuzeigen.

   ![workspace_drop-down-Bild](assets/workspace_drop-down.png)

* **Aktivitätserstellung:** Wenn Sie eine Aktivität erstellen, wird sie im derzeit ausgewählten Arbeitsbereich erstellt. Im ersten Dialogfeld, in dem Sie den gewünschten Kanal für die Aktivität auswählen können, werden Optionen zur Kanalauswahl angezeigt: Web, mobile App, E-Mail oder Sonstige/API.

   ![channel_options-Bild](assets/channel_options.png)

* **Zielgruppenerstellung:** Wenn Sie eine Zielgruppe erstellen, wird sie im derzeit ausgewählten Arbeitsbereich erstellt.
* **Zielgruppenliste:** Sie können Zielgruppen zwischen Arbeitsbereichen verschieben, indem Sie die [!UICONTROL Mehr Aktionen] > [!DNL Move] -Option auf [!UICONTROL Zielgruppen] Seite.
* **Erstellung von Angeboten:** Wenn Sie ein Angebot erstellen, wird es im derzeit ausgewählten Arbeitsbereich erstellt.
* **Eigenschaftenseite (Administration > Eigenschaften):** Sie können die [!UICONTROL Suche] zum Durchsuchen der [!UICONTROL Eigenschaft] Liste.

   ![properties_list-Bild](assets/properties_list.png)

## Einschränkungen  {#section_9714311B1CD9497A86F4910F8AE635E2}

Beachten Sie Folgendes bei der Verwendung oder Konfiguration von Eigenschaften und Berechtigungen in [!DNL Target] Premium:

* **Wichtig**: Löschen Sie keine Arbeitsbereiche mit Aktivitäten. Wenn Sie einen Arbeitsbereich mit Aktivitäten löschen, wenden Sie sich an die Kundenunterstützung, um diese Aktivitäten wiederherzustellen.
* Bei der Verwendung der Ansicht „Alle meine Arbeitsbereiche“ gilt Folgendes:

   * Sie können Aktivitäten, Zielgruppen und Angebote für alle Arbeitsbereiche anzeigen, für die Sie über die erforderlichen Rollen und Zugriffsberechtigungen verfügen.
   * Wenn Sie die [!UICONTROL Alle meine Arbeitsbereiche] angezeigt, wird der Seite Aktivitäten, Zielgruppen und Angebote eine neue Spalte hinzugefügt. In dieser Spalte werden der Arbeitsbereich des Elements und Ihre mit diesem Element verknüpften Benutzerberechtigungen (Beobachter, Bearbeiter oder Genehmiger) aufgelistet.
   * Wenn Sie eine Aktivität, eine Zielgruppe oder ein Angebot in der Ansicht „Alle meine Arbeitsbereiche“ erstellen, müssen Sie den Arbeitsbereich auswählen, in dem das Element erstellt werden soll. Hierbei können Sie nur Arbeitsbereiche auswählen, für die Sie über Editor- oder Genehmiger-Berechtigungen verfügen.
   * Wenn Sie eine Aktivität, eine Zielgruppe oder ein Angebot in der Ansicht „Alle meine Arbeitsbereiche“ kopieren, müssen Sie den Arbeitsbereich auswählen, in den das Element kopiert werden soll. Hierbei können Sie nur Arbeitsbereiche auswählen, für die Sie über Editor- oder Genehmiger-Berechtigungen verfügen.

* Jede Einstellung für die folgenden [!UICONTROL Administration] Seiten können von jeder [!UICONTROL Genehmiger] in beliebigen Arbeitsbereichen:

   * Visual Experience Composer
   * Berichterstellung
   * Scene7-Konfiguration
   * Implementierung
   * Eigenschaften
   * Hosts
   * Umgebungen
   * Antwort-Token
   * Benutzer

* Benutzer können keine Ressourcen zwischen Arbeitsbereichen (Produktprofilen) verschieben. Das Kopieren wird jedoch unterstützt.
* Beim Anzeigen der Zielgruppen über die [!DNL Audiences]-Seite lädt die Seite langsamer als erwartet. Nutzen Sie das Suchfeld, werden die Zielgruppen schneller geladen. Dieses Problem ist bekannt und wird in einem kommenden Update behoben. Das Problem wirkt sich nicht auf die Auswahl von Zielgruppen bei der Erstellung von Aktivitäten aus.
* Die folgenden Ressourcen sind Teil des neuen Unternehmensberechtigungsmodells:

   * Aktivitäten, Zielgruppen und Codeangebote, die in [!DNL Target Standard/Premium] sind verfügbar, nachdem der Kunde für Berechtigungen aktiviert wurde. (Hinweis: -Kunden müssen [!DNL Target Premium].
   * Eigenschaften können vorhandenen Aktivitäten im Standardarbeitsbereich hinzugefügt werden. Dieser Ansatz kann sich jedoch ändern.
   * Für die Beschränkung durch Berechtigungen stehen nur neue Ressourcen (z. B. Aktivitäten, Codeangebote und Zielgruppen) zur Verfügung, die in Target Premium erstellt wurden (nachdem Unternehmensberechtigungen aktiviert wurden).
   * Externe Ressourcen sind nur für Benutzer im Standardarbeitsbereich verfügbar. Die Rolle eines Benutzers im Standardarbeitsbereich ist global gültig (für alle Target-Anfragen und alle Taget-Ressourcen).

* Die folgenden Ressourcen sind *nicht* Teil des neuen Unternehmensberechtigungsmodells:

   * Bildangebote
   * Alle Recommendations-Ressourcen, einschließlich Kriterienbibliothek, Designbibliothek, Katalog, Recommendations-Einrichtung.
   * Vorhandene Ressourcen (wie Aktivitäten, Codeangebote und Zielgruppen), die in Target Premium vor der Aktivierung von Unternehmensberechtigungen erstellt wurden, können zwar kopiert, aber nicht in andere Arbeitsbereiche verschoben werden.
   * Aktivitäten, Zielgruppen, Codeangebote, Bildangebote oder andere Ressourcen, die mit den folgenden Lösungen oder Methoden erstellt wurden, können nicht vom Unternehmensberechtigungsmodell gesteuert werden, sind jedoch Teil des Standardarbeitsbereichs: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services und über API erstellte Ressourcen. Unter über die API erstellte Ressourcen fallen Aktivitäten, Audiences, Codeangebote und Bildangebote).
   * Bildangebote (unter gespeicherte Assets) `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` kann derzeit nicht vom Unternehmensberechtigungsmodell gesteuert werden.
   * clickTracking und Umleitungen funktionieren, wenn der Ziellink oder die Zielseite Teil einer Eigenschaft sind, die in der Aktivität enthalten ist. Außerdem funktioniert clickTracking möglicherweise nicht bei Verwendung der Variablen `targetPageParams()` -Funktion. `targetPageParamsAll()` ist die empfohlene Funktion.

   [!DNL Target] erfordert zurzeit, dass auf allen Seiten, auf denen Tracking erfolgt, ein `at_property`-Token vorhanden ist. Wenn das Token (1) nicht vorhanden ist, (2) zum Zeitpunkt der Aktivitätseinrichtung (im VEC) nicht erkannt wird oder (3) nicht an den Aufruf &quot;clickTracking Target&quot;über die `targetPageParamsAll()` -Funktion, wird die Metrik nicht erhöht und als &quot;0&quot;angezeigt.

   Dasselbe gilt für Aktivitäten, die Umleitungen verwenden. Auf der Zielseite muss ein `at_property`-Token vorhanden sein, das beim Einrichten in VEC erkannt wird.

   In einer künftigen Version wird Target auf Seiten, auf denen kein `at_property`-Token existiert, oder auf Seiten, auf denen ein anderes `at_property`-Token vorhanden ist, funktionieren.

* Die Funktionalität „Berechtigungen für Unternehmensbenutzer“ wird in den [Aufrufen der Adobe I/O-API](https://developer.adobe.com/target/){target=_blank} nicht unterstützt.

## Häufig gestellte Fragen   {#faqs}

Häufig gestellte Fragen zu Unternehmensberechtigungen:

### Was passiert, wenn ein Benutzer über mehrere Rollen und Berechtigungen verfügt? [#multiple-roles]

Wenn ein Benutzer über mehrere Rollen und Berechtigungen verfügt, wird die Rolle mit den Berechtigungen des Benutzers angewendet. Wenn ein Benutzer beispielsweise [!UICONTROL Beobachter] und [!UICONTROL Genehmiger] Rollen, [!UICONTROL Genehmiger] Rolle angewendet wird.

### Kann ich eine Aktivität von einem Arbeitsbereich in einen anderen verschieben?

Leider ist es nicht möglich, Aktivitäten von einem Arbeitsbereich in einen anderen zu verschieben. Sie können jedoch eine Aktivität in einen beliebigen Arbeitsbereich kopieren, um zu wissen, dass die Berichtsdaten nicht übertragen werden. Weitere Informationen finden Sie unter „Kopieren/Bearbeiten einer Aktivität beim Verwenden von Arbeitsbereichen“ in [Kopieren/Bearbeiten einer Aktivität beim Verwenden von Arbeitsbereichen](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Aktivitäten, die vor der Migration angelegt wurden, laufen im Standardarbeitsbereich auf die gleiche Weise weiter, es sei denn, sie werden bearbeitet und mit Eigenschaften versehen. Aktivitäten in einem bestimmten Arbeitsbereich berücksichtigen die Eigenschaften, die diesem Arbeitsbereich zugewiesen sind, und daher bleibt das Verhalten möglicherweise nicht mehr so wie vor der Migration.

### Kann ich eine Zielgruppe von einem Arbeitsbereich in einen anderen verschieben? {#move-audience}

Ja, Sie können Zielgruppen mithilfe der [!UICONTROL Mehr Aktionen] -Option auf [!UICONTROL Zielgruppen] Seite.

1. Klicken Sie auf **[!UICONTROL Mehr Aktionen]** Schaltfläche (die drei Ellipsen) und klicken Sie auf **[!UICONTROL Verschieben]**.

   ![Mehr Aktionen > Verschieben](/help/main/administrating-target/c-user-management/property-channel/assets/move-audience.png)

1. Wählen Sie den gewünschten Arbeitsbereich aus dem **[!UICONTROL Arbeitsbereich]** Dropdown-Liste und klicken Sie auf **[!UICONTROL Verschieben]**.

   ![Wählen Sie die gewünschte Zielgruppe aus, um in den neuen Arbeitsbereich zu wechseln](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-move.png)

>[!NOTE]
>
>Sie müssen über die entsprechenden Berechtigungen zum Bearbeiten einer Zielgruppe verfügen. Darüber hinaus darf die Zielgruppe nicht in anderen Aktivitäten verwendet werden. Wenn die Zielgruppe in anderen Aktivitäten verwendet wird und Sie die Zielgruppe dennoch an einen anderen Arbeitsplatz verschieben möchten, entfernen Sie die Zielgruppe aus den anderen Aktivitäten, in denen sie verwendet wird.

### Warum wird eine Fehlermeldung angezeigt, die besagt, dass keine Eigenschaft mit dieser Aktivität verknüpft ist, auch wenn eine Eigenschaft zugewiesen ist?

Wenn Sie implementiert haben [!DNL Target] mit Tags in [!DNL Adobe Experience Platform] und erhalten Sie eine Fehlermeldung, die angibt, dass der Aktivität keine Eigenschaft zugeordnet ist. Übergeben Sie die `at_property` -Parameter mit der `targetPageParams` -Funktion.

### Werden Klick-Track-Konversionen aufgezeichnet, wenn eine Umleitungsseite und die Aktivitäts-URL zu unterschiedlichen Präsenzen gehören?

Klick-Tracking wird nicht auf Seiten aufgezeichnet, wo die Seite und die Aktivitäts-URL zu unterschiedlichen Präsenzen gehören.

Betrachten wir das folgende Szenario:

* Seite 1 gehört zu Präsenz1.
* Seite 2 gehört zu Präsenz2.
* In der Aktivität leitet Seite 1 auf Seite 2 weiter, die Klick-Tracks enthält.

Wenn ein Besucher Seite 1 in einem Browser öffnet, wird der Besucher zu Seite 2 umgeleitet. Da Seite 2 nicht zur Bereitstellung der Aktivität berechtigt ist, enthält der Target-Aufruf keine Klick-Tracks in der Antwort.

Wenn die Weiterleitungsseite und die Aktivitäts-URL zu derselben Eigenschaft gehören, funktionieren die Klick-Tracks erwartungsgemäß. Weitere Informationen finden Sie unter [Klick-Tracking](/help/main/c-activities/r-success-metrics/click-tracking.md).

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Schulungsvideo: Schulungsvideo zu Unternehmensberechtigungen ![Übersichtszeichen](/help/main/assets/overview.png)

Lernziele:

* Die drei möglichen Rollenebenen von Adobe Target-Benutzern
* Die Konzepte von Eigenschaften und Arbeitsbereichen und wie diese Grenzen und Gruppierungen funktionieren, um die Zugangsebenen der Benutzer steuern zu können
* Verschiedene Beispiele für Eigenschaften für Ihre Organisation

>[!VIDEO](https://video.tv.adobe.com/v/19042/)

### Bürozeiten: [!DNL Target] Premium-Arbeitsbereiche

Dieses Video ist eine Aufzeichnung von Office Hours, einer Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* Erstellen von Arbeitsbereichen (Produktprofilen)
* Erstellen von Eigenschaften
* Hinzufügen von Benutzern
* Aktualisieren der Implementierung

>[!NOTE]
>
>Die Benutzeroberfläche des [!UICONTROL Administration]-Menüs von [!DNL Target] (früher [!UICONTROL Einrichten]) wurde überarbeitet, um eine verbesserte Leistung zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu reduzieren und das Benutzererlebnis im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind korrekt. -Optionen können sich jedoch an etwas anderen Orten befinden.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
