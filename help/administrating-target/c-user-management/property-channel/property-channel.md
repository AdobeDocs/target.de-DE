---
description: Informationen zur Erstellung von Eigenschaften und zur Verwendung der Funktionalität für Eigenschaften und Berechtigungen, mit deren Hilfe Target-Administratoren in Target verschiedene Arbeitsbereiche (Produktprofile) erstellen und anschließend Benutzern basierend auf diesen Arbeitsbereichen unterschiedliche Rollen und Berechtigungen für einzelne Seiten, Eigenschaften oder Websites zuweisen können.
keywords: Arbeitsbereiche;Eigenschaft verwalten;Berechtigungen;Produktkonfiguration;Produktprofil;Rollen;Projekt
seo-description: Informationen zur Erstellung von Eigenschaften und zur Verwendung der Funktionalität für Eigenschaften und Berechtigungen, mit deren Hilfe Target-Administratoren in Target verschiedene Arbeitsbereiche (Produktprofile) erstellen und anschließend Benutzern basierend auf diesen Arbeitsbereichen unterschiedliche Rollen und Berechtigungen für einzelne Seiten, Eigenschaften oder Websites zuweisen können.
seo-title: Berechtigungen für Unternehmensbenutzer
solution: Target
subtopic: Erste Schritte
title: Berechtigungen für Unternehmensbenutzer
title-outputclass: Premium
topic: Premium
uuid: 1961730d-2357-406f-acac-a36b7a63bd35
badge: Premium
translation-type: tm+mt
source-git-commit: 8c9da94d7589d54b205c1387d25515a962f98235

---


# ![PREMIUM](/help/assets/premium.png) Berechtigungen für Unternehmensbenutzer{#enterprise-user-permissions}

Informationen zur Erstellung von Eigenschaften und zur Verwendung der Funktionalität für Eigenschaften und Berechtigungen, mit deren Hilfe Target-Administratoren in Target verschiedene Arbeitsbereiche (Produktprofile) erstellen und anschließend Benutzern basierend auf diesen Arbeitsbereichen unterschiedliche Rollen und Berechtigungen für einzelne Seiten, Eigenschaften oder Websites zuweisen können.

## Stellen Sie fest, ob Sie Zugriff auf die Berechtigungen für Unternehmensbenutzer haben

>[!NOTE]
>
>Die Funktionalitäten für Eigenschaften und Berechtigungen sind als Bestandteil der Lösung Target Premium verfügbar. Ohne Target Premium-Lizenz sind sie nicht für Target Standard verfügbar.
>
>Sie können für Ihre Target-Implementierung eine beliebige Version von at.js oder mbox.js verwenden.

Sie können feststellen, ob Ihr Unternehmen über eine Standard- oder Premium-Lizenz verfügt, indem Sie oben in der Benutzeroberfläche auf den Link [!UICONTROL Einrichten] [!DNL Target] klicken.

* **[!DNL Target Standard]/Kunden**: Wenn die Registerkarte [!UICONTROL Benutzer] ([!UICONTROL Einrichtung &gt; Benutzer]) angezeigt wird, verfügt Ihr Unternehmen über eine [!DNL Target Standard]-Lizenz. [!DNL Target Standard]-Kunden sollten die Anweisungen in [Benutzer](/help/administrating-target/c-user-management/c-user-management/user-management.md) befolgen, um Benutzer hinzuzufügen und Berechtigungen in der Adobe Admin Console zuzuweisen.

   [!DNL Target Standard]Benutzer von sehen die folgende Fehlermeldung, wenn sie auf die Registerkarte [!UICONTROL Eigenschaften] klicken. Mit [!DNL Target] ist alles in Ordnung. [!DNL Target Standard]Benutzer haben keinen Zugriff auf die [!DNL Target Premium]-Funktionalität [!UICONTROL Unternehmensberechtigungen].

   ![Fehlermeldung](/help/administrating-target/c-user-management/property-channel/assets/sorry.png)

* **[!DNL Target Premium]Kunden**: Wenn die Registerkarte [!UICONTROL Eigenschaften] ([!UICONTROL Einrichtung &gt; Eigenschaften]) angezeigt wird, besitzt Ihr Unternehmen eine [!DNL Target Premium]-Lizenz. [!DNL Target Premium]-Kunden sollten die Anweisungen in diesem Artikel und in [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) folgen.

## Bevor Sie mit Unternehmensberechtigungen arbeiten

>[!IMPORTANT]
>
>Stellen Sie sicher, dass Sie den Abschnitt [Einschränkungen](../../../administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) unten gelesen haben, bevor Sie mit den Unternehmensberechtigungen fortfahren.

## In diesem Abschnitt verwendete Begriffe und Definitionen {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

In diesem Abschnitt werden die folgenden Begriffe verwendet, die Benutzern, die die Funktion für Eigenschaften und Berechtigungen in Target Premium verwenden möchten, möglicherweise noch nicht bekannt sind.

### Eigenschaft

Die Eigenschaften ähneln denen des Dynamic Tag Management (Activation) insofern, als sie sich durch einen einzigen Codeabschnitt unterscheiden lassen.

Eine Webeigenschaft besteht aus einer Bibliothek von Regeln und einem Einbettungscode. Es kann sich bei einer Webeigenschaft um eine beliebige Gruppierung einer oder mehrerer Domänen bzw. Subdomänen handeln.

Eigenschaften werden aktiviert, indem ein bestimmtes Name-Wert-Paar beliebigen Aufrufen (mbox, API usw.) an Target hinzugefügt wird.
Eigenschaften sind bestimmten Kanälen (Web, mobil, E-Mail oder API/Sonstige) zugeordnet.

### Arbeitsbereich (Produktprofil)

Mithilfe eines Arbeitsbereichs können Organisationen bestimmte Benutzergruppen bestimmten Eigenschaftsgruppen zuweisen. Arbeitsbereiche ähneln auf vielerlei Weise den Report Suites in Adobe Analytics.

Hinweis: Arbeitsbereiche erscheinen als Produktprofile in der Adobe Admin Console for Enterprise.

Wenn Sie Teil einer multinationalen Organisation sind, besitzen Sie eventuell einen Arbeitsbereich für Ihre europäischen Webseiten, Eigenschaften oder Sites und einen weiteren Arbeitsbereich für Ihre amerikanischen Webseiten, Eigenschaften oder Sites. Wenn Sie einer Organisation angehören, die mehrere Marken besitzt, haben Sie eventuell für jede Marke einen eigenen Arbeitsbereich.

Benutzer können mehreren Arbeitsbereichen angehören und in den verschiedenen Arbeitsbereichen sogar unterschiedliche Rollen einnehmen.

Benutzer können verschiedene Ansichten von Adobe Target verwenden, indem sie zwischen Arbeitsbereichen wechseln. Dies ähnelt dem Prinzip, dass Analytics-Benutzer über verschiedene Ansichten von Analytics verfügen, indem Sie zwischen Report Suites wechseln.

Arbeitsbereiche können vollständig verschiedene Zielgruppen, Codeangebote und Aktivitäten beinhalten.

Alle Zielgruppen und Aktivitäten, die vor der Migration des Modells für Unternehmensberechtigungen erstellt wurden, werden zusammen im „Standardarbeitsbereich“ gruppiert, der weiter unten erläutert wird.

Alle mit Adobe Experience Manager (AEM), Adobe Mobile Services und Adobe Target Classic erstellten Aktivitäten werden in das Projekt „Standardarbeitsbereich“ übernommen.

### Standardarbeitsbereich

Alle vorhandenen Arbeitsbereiche (Produktprofile) in der Admin Console werden bei der Migration Ihrer Organisation zu dem neuen Unternehmensberechtigungsmodell in einem einzelnen Arbeitsbereich mit der Bezeichnung „Standardarbeitsbereich“ zusammengeführt.

>[!IMPORTANT]
>
>Löschen Sie den Standardarbeitsbereich nicht.

Alle Benutzerrollen und der Zugriff auf die gesamte Target-Funktionalität bleiben exakt genau so wie vor der Migration zum neuen Unternehmensberechtigungsmodell.

### Benutzergruppen

Sie können Benutzergruppen wie Entwickler, Analytiker, Marketingexperten, Manager usw. erstellen und ihnen dann Benutzerrechte für verschiedene Adobe-Produkte und -Arbeitsbereiche zuweisen. Das Zuweisen der passenden Berechtigungen für ein Team-Mitglied für zwei Adobe-Produkte kann oft einfach durch Zuweisung zu einer einzigen Benutzergruppe vorgenommen werden.

### Rollen und Berechtigungen

Rollen und Berechtigungen bestimmen, welche Zugriffsebene Benutzer haben, um Aktivitäten in der Target-Implementierung zu erstellen und zu verwalten. In Target gibt es folgende Rollen:

* Beobachter: Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten.
* Bearbeiter: Kann Aktivitäten erstellen und bearbeiten, bevor sie aufgeschaltet werden, kann jedoch nicht den Start einer Aktivität genehmigen.
* Genehmiger: Kann Aktivitäten erstellen, bearbeiten, aktivieren und stoppen.

### Kanal

Der Kanal gibt den Content-Typ an, in dem Ihre Target-Aktivitäten bereitgestellt werden: Webseiten, mobile Apps, E-Mail-Nachrichten usw.

Bei Erstellung einer neuen Aktivität wird diese dem aktuell ausgewählten Arbeitsbereich zugewiesen. Optionen für die Kanalauswahl finden sich im ersten Dialogfeld, in dem Sie den gewünschten Aktivitätskanal festlegen können: Web, mobile App, E-Mail oder Sonstige/API.

## Übersicht über Berechtigungen   {#section_DC2172520DA84605B218A5E9FB6D187A}

Die folgenden Informationen erläutern, wie Berechtigungen zuvor in [!DNL Target] umgesetzt wurden und wie sie mit der neuen Funktion für [!UICONTROL Eigenschaften] und [!UICONTROL Berechtigungen] umgesetzt werden.

Mithilfe der neuen [!UICONTROL Berechtigungsfunktion] können Sie verschiedene Projekte (in der [!DNL Adobe Admin Console for Enterprise] als „Produktprofile“ bezeichnet) erstellen, die die Zuweisung bestimmter Rechte an einzelne Benutzer ermöglichen, sodass diese Benutzer Zugriff auf bestimmte Projekte erhalten. Diese voneinander unabhängigen Projekte funktionieren ähnlich wie Report Suites in [!DNL Adobe Analytics]. Jedes Projekt verfügt über bestimmte Benutzer mit bestimmten Rollen, die einer bestimmten Reihe Berechtigungen entsprechen. Somit können Kunden die Ansicht, die Bearbeitung und den Genehmigungszugriff der Benutzer basierend auf Region, Umgebung (Entwicklung, Test, Produktion), Kanal oder anderen Kriterien einschränken, wie unten dargestellt:

![](assets/permissions.png)

Ein bestimmter Benutzer verfügt beispielsweise über Genehmigungszugriff auf die Websites für Nord- und Südamerika, jedoch nur auf Ansichtszugriff auf die mobile App für Europa. Dieser Benutzer verfügt möglicherweise nicht über die nötigen Rechte, die in Web- und Mobileigenschaften angebotenen Aktivitäten der APAC-Region einzusehen.

Im aktuellen [!DNL Target] [!UICONTROL Berechtigungsmodell] von  gibt es drei Rollen (Beobachter, Bearbeiter und Genehmiger), die in folgender Abbildung dargestellt werden:

![](assets/permissions_1.png)

Jede Rolle verfügt über eigene Zugriffsniveaus:

| Rolle | Beschreibung |
|--- |--- |
| Beobachter | Verfügt ausschließlich über Lesezugriff auf Aktivitäten. Kann Aktivitäten anzeigen, aber nicht erstellen oder bearbeiten. |
| Editor | Kann Aktivitäten erstellen und bearbeiten, bevor sie live sind, kann aber nicht den Start einer Aktivität genehmigen. |
| Genehmiger | Kann Aktivitäten erstellen, bearbeiten, aktivieren oder stoppen. |

Es muss dabei berücksichtigt werden, dass die Benutzerrolle für alle Seiten, Eigenschaften oder Sites Ihres Kontos gilt, die über [!DNL Target]-Tags verfügen, wie unten dargestellt:

![](assets/permissions_2.png)

Das neue [!DNL Target][!UICONTROL -Berechtigungsmodell] verfügt über die gleichen drei Rollen (Beobachter, Bearbeiter und Genehmiger), einem Benutzer können jedoch verschiedene Rollen für einzelne Seiten, Eigenschaften oder Sites zugewiesen werden, wie unten dargestellt:

![](assets/permissions_3.png)

In diesem Beispiel besitzt Jan Genehmigerrechte für die US-Homepage und die US-Site und Beobachterrechte für die französische Site.

Außerdem kann Jan keine Seiten, Eigenschaften oder Sites in [!DNL Target] anzeigen, für die sie nicht über entsprechende Berechtigungen verfügt, wie unten dargestellt:

![](assets/permissions_4.png)

In diesem Beispiel kann Jan die Produktseiten, die russische Site und die Karriere-Site nicht sehen.

## Anwendungsszenarien   {#section_F3CE8576959E4F4CB13BEEED38311DD8}

Die folgenden Anwendungsfälle zeigen wie Eigenschaften, Projekte, Rollen und Berechtigungen genutzt werden können, um Marketingziele mit [!DNL Target] zu erreichen:

### Multinationale Organisation

Wenn Sie Teil einer multinationalen Organisation sind, besitzen Sie eventuell einen Arbeitsbereich für Ihre europäischen Webseiten, Eigenschaften oder Sites und einen weiteren Arbeitsbereich für Ihre amerikanischen Webseiten, Eigenschaften oder Sites.
Nach einer Umstrukturierung richten Sie für die Personen aus der obigen Abbildung folgende Arbeitsbereiche und Berechtigungen ein:

* **Jan**: Jan leitet die Optimierungsabteilung im Center of Excellence für die US-Webseiten, -Objekte und -Sites ihrer Organisation. Sie besitzt Systemadministratorrechte in der Adobe Experience Cloud.

   In ihrer Rolle hat sie Genehmigerberechtigungen für die US-Homepage und die US-Site. Mit den Genehmigerberechtigungen kann sie Aktivitäten erstellen, bearbeiten und aktivieren oder stoppen.

   Jan berät außerdem das Optimierungsteam in Frankreich und besitzt daher Beobachterrechte für die französische Site, die ihr Leserechte für Aktivitäten gewähren. Jan kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

   Da Jan keine Rolle besitzt, für die sie die Produktseiten, die russische Site oder die Karriere-Site sehen muss, kann sie für diese Sites keine Aktivitäten sehen.

* **Ernie**: Ernie ist Marketingleiter der Organisation und für das Marketing in den USA zuständig.

   Da Ernie recht neu in der Organisation ist und noch wenig Erfahrung mit Target hat, besitzt er Bearbeiterrechte für die US-Homepage, die US-Site und für Produktseiten. Mit Bearbeiterrechten kann Ernie Aktivitäten erstellen und bearbeiten, bevor diese live sind, er kann den Start einer Aktivität jedoch nicht genehmigen. Den Start in die Produktion muss jemand mit Genehmigerrechten genehmigen, z. B. Jan.

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

   Da Ernie recht neu in der Organisation ist und noch wenig Erfahrung mit Target hat, besitzt er Bearbeiterrechte für die Endverbraucher-Site. Mit Bearbeiterrechten kann Ernie Aktivitäten erstellen und bearbeiten, bevor diese live sind, er kann den Start einer Aktivität jedoch nicht genehmigen. Den Start in die Produktion muss jemand mit Genehmigerrechten für die Endverbraucher-Site genehmigen, wobei es sich in diesem Szenario nicht um Jan handelt.

   Da Ernie keine Rolle besitzt, für die er die Krankenhaus-Site sehen muss, kann er für diese Site keine Aktivitäten sehen.

* **Diana**: Diana arbeitet jetzt als Analystin für die Organisation. Ihr wurden Beobachterberechtigungen für die Krankenhaus- und die Endverbraucher-Sites zugewiesen, mit denen sie reinen Lesezugriff auf Aktivitäten hat. Diana kann Aktivitäten anzeigen, sie aber nicht erstellen oder bearbeiten.

## Touchpoints der Target-Benutzeroberfläche für Eigenschaften und Berechtigungen {#section_3414371393BB42999A268628B5456EC9}

Die neue Berechtigungsfunktion findet sich in der Benutzeroberfläche von [!DNL Target] gleich an mehreren Orten.

* **Dropdownliste „Arbeitsbereich“ (Produktprofil):** Die Dropdownliste „Arbeitsbereich“ wird am oberen Rand der Seiten [!UICONTROL Aktivitäten], [!UICONTROL Zielgruppen] und [!UICONTROL Angebote] angezeigt. Wählen Sie den gewünschten Arbeitsbereich aus, um die Liste zu filtern und nur die Elemente des ausgewählten Arbeitsbereichs anzuzeigen.

   ![](assets/workspace_drop-down.png)

* **Aktivitätserstellung:** Bei Erstellung einer neuen Aktivität wird diese dem aktuell ausgewählten Arbeitsbereich zugewiesen. Optionen für die Kanalauswahl finden sich im ersten Dialogfeld, in dem Sie den gewünschten Aktivitätskanal festlegen können: Web, mobile App, E-Mail oder Sonstige/API.

   ![](assets/channel_options.png)

* **Zielgruppenerstellung:** Bei Erstellung einer neuen Zielgruppe wird diese dem aktuell ausgewählten Arbeitsbereich zugewiesen.
* **Angebotserstellung:** Bei Erstellung eines neuen Angebots wird dieses dem aktuell ausgewählten Arbeitsbereich zugewiesen.
* **Eigenschaftenseite (Einrichtung &gt; Eigenschaften):** Es sind das [!UICONTROL Suchfeld] sowie die Optionen [!UICONTROL Kanal] und [!UICONTROL Produktprofil] verfügbar, anhand deren die [!UICONTROL Eigenschaftsliste] gefiltert werden kann.

   ![](assets/properties_list.png)

## Einschränkungen {#section_9714311B1CD9497A86F4910F8AE635E2}

Beachten Sie bei der Konfiguration von Eigenschaften und Berechtigungen in Target Premium Folgendes:

* **Wichtig**: Löschen Sie keine Arbeitsbereiche mit Aktivitäten. Wenn dies geschieht, stellen Sie diese Aktivitäten zusammen mit dem Kundendienst wieder her.
* Bei der Verwendung der Ansicht „Alle meine Arbeitsbereiche“ gilt Folgendes:

   * Sie können Aktivitäten, Zielgruppen und Angebote für alle Arbeitsbereiche anzeigen, für die Sie über die erforderlichen Rollen und Zugriffsberechtigungen verfügen.
   * Wenn Sie die Ansicht „Alle meine Arbeitsbereiche“ auswählen, wird eine neue Spalte zu den Seiten „Aktivitäten“, „Zielgruppen“ und „Angebote“ hinzugefügt, die den Arbeitsbereich des Elements sowie die mit diesem Element verknüpfte Benutzerberechtigung (Beobachter, Editor oder Genehmiger) aufführt.
   * Wenn Sie eine Aktivität, eine Zielgruppe oder ein Angebot in der Ansicht „Alle meine Arbeitsbereiche“ erstellen, müssen Sie den Arbeitsbereich auswählen, in dem das Element erstellt werden soll. Hierbei können Sie nur Arbeitsbereiche auswählen, für die Sie über Editor- oder Genehmiger-Berechtigungen verfügen.
   * Wenn Sie eine Aktivität, eine Zielgruppe oder ein Angebot in der Ansicht „Alle meine Arbeitsbereiche“ kopieren, müssen Sie den Arbeitsbereich auswählen, in den das Element kopiert werden soll. Hierbei können Sie nur Arbeitsbereiche auswählen, für die Sie über Editor- oder Genehmiger-Berechtigungen verfügen.

* Die Einstellungen auf den folgenden Einrichtungsseiten können von jedem Genehmiger in einem beliebigen Arbeitsbereich gesteuert werden:

   * Voreinstellungen
   * Implementierung
   * Scene7-Einstellungen
   * Hosts

* Benutzer können keine Ressourcen zwischen Arbeitsbereichen (Produktprofilen) verschieben. Das Kopieren wird jedoch unterstützt.
* Beim Anzeigen der Zielgruppen über die [!DNL Audiences]-Seite lädt die Seite langsamer als erwartet. Nutzen Sie das Suchfeld, werden die Zielgruppen schneller geladen. Es handelt sich hierbei um ein bekanntes Problem, das in einer der folgenden Versionen behoben wird. Das Problem wirkt sich nicht auf die Auswahl von Zielgruppen bei der Erstellung von Aktivitäten aus.
* Die folgenden Ressourcen sind Teil des neuen Unternehmensberechtigungsmodells:

   * Aktivitäten, Zielgruppen und Codeangebote, die in Target Standard/Premium erstellt werden, nachdem der Kunde für Berechtigungen aktiviert wurde. (Hinweis: Kunden müssen über Berechtigungen für Target Premium verfügen.)
   * Eigenschaften können vorhandenen Aktivitäten im Standardarbeitsbereich hinzugefügt werden. Dies kann jedoch geändert werden.
   * Für die Beschränkung durch Berechtigungen sind nur neue Ressourcen verfügbar (z. B. Aktivitäten, Codeangebote und Zielgruppen), die in Target Premium erstellt wurden (nach dem Aktivierten von Unternehmensberechtigungen).
   * Externe Ressourcen sind nur für Benutzer im Standardarbeitsbereich verfügbar. Die Rolle eines Benutzers im Standardarbeitsbereich ist global gültig (für alle Target-Anfragen und alle Taget-Ressourcen).

* Die folgenden Ressourcen sind *nicht* Teil des neuen Unternehmensberechtigungsmodells:

   * Bildangebote
   * Alle Recommendations-Ressourcen, einschließlich Kriterienbibliothek, Designbibliothek, Katalog, Recommendations-Einrichtung.
   * Vorhandene Ressourcen (z. B. Aktivitäten, Codeangebote und Zielgruppen), die in Target Premium vor dem Aktivieren von Unternehmensberechtigungen erstellt wurden, können zwar kopiert, aber nicht in andere Arbeitsbereiche verschoben werden.
   * Aktivitäten, Zielgruppen, Codeangebote, Bildangebote oder andere mit den folgenden Lösungen oder Methoden erstellte Ressourcen können nicht durch das Unternehmensberechtigungsmodell gesteuert werden, werden jedoch Teil des Standardarbeitsbereichs sein: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services und Ressourcen, die über die API erstellt wurden. Unter über die API erstellte Ressourcen fallen Aktivitäten, Audiences, Codeangebote und Bildangebote).
   * Bildangebote (unter `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` gespeicherte Assets) können bisher nicht mithilfe des Unternehmensberechtigungsmodells gesteuert werden.
   * clickTracking und Weiterleitungen funktionieren nur dann, wenn der Ziellink oder die Zielseite Teil einer Eigenschaft sind, die in der Aktivität enthalten ist. Außerdem funktioniert clickTracking möglicherweise nicht, wenn die `targetPageParams()`-Funktion verwendet wird. `targetPageParamsAll()` ist die empfohlene Funktion.
   Target erfordert zurzeit, dass auf allen Seiten, auf denen Tracking erfolgt, ein `at_property`-Token vorhanden ist. Falls das Token (1) nicht vorhanden ist, (2) zum Zeitpunkt der Aktivitätseinrichtung (im VEC) nicht erkannt wird oder (3) nicht an die clickTracking-Mbox über die `targetPageParamsAll()`-Funktion weitergegeben wird, wird die Metrik nicht erhöht und als „0“ angezeigt.

   Dasselbe gilt für Aktivitäten, die Umleitungen verwenden. Auf der Zielseite muss ein `at_property`-Token vorhanden sein, das beim Einrichten in VEC erkannt wird.

   In einer künftigen Version wird Target auf Seiten, auf denen kein `at_property`-Token existiert, oder auf Seiten, auf denen ein anderes `at_property`-Token vorhanden ist, funktionieren.

* Die Funktionalität „Berechtigungen für Unternehmensbenutzer“ wird in den [Aufrufen der Adobe I/O-API](https://developers.adobetarget.com) nicht unterstützt.

## Häufig gestellte Fragen {#faqs}

Häufig gestellte Fragen zu Unternehmensberechtigungen:

### Kann ich eine Aktivität von einem Arbeitsbereich in einen anderen verschieben?

Leider ist es nicht möglich, Aktivitäten von einem Arbeitsbereich in einen anderen zu verschieben. Sie können jedoch eine Aktivität in einen beliebigen Arbeitsbereich kopieren, müssen aber wissen, dass die Berichtsdaten nicht mitübertragen werden. Weitere Informationen finden Sie unter „Kopieren/Bearbeiten einer Aktivität beim Verwenden von Arbeitsbereichen“ in [Kopieren/Bearbeiten einer Aktivität beim Verwenden von Arbeitsbereichen](../../../c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Aktivitäten, die vor der Migration angelegt wurden, laufen im Standardarbeitsbereich auf die gleiche Weise weiter, es sei denn, sie werden bearbeitet und mit Eigenschaften versehen. Bei Aktivitäten in einem benannten Arbeitsbereich werden die Eigenschaften berücksichtigt, die diesem Arbeitsbereich zugewiesen wurden, sodass das Verhalten möglicherweise nicht mehr das gleiche ist wie vor der Migration.

### Warum wird eine Fehlermeldung angezeigt, die besagt, dass keine Eigenschaft mit dieser Aktivität verknüpft ist, auch wenn eine Eigenschaft zugewiesen ist?

Wenn Sie mit [!DNL Target] der Fehlermeldung implementiert [!DNL Adobe Launch] haben, dass der Aktivität keine Eigenschaft zugeordnet ist, geben Sie den `at_property` Parameter mit der `targetPageParams` Funktion an.

### Werden Clicktrack-Konversionen aufgezeichnet, wenn eine Umleitungsseite und die Aktivitäts-URL zu unterschiedlichen Eigenschaften gehören?

Klick-Tracking wird nicht auf Seiten aufgezeichnet, auf denen die Seite und die Aktivitäts-URL zu unterschiedlichen Eigenschaften gehören.

Betrachten Sie das folgende Szenario (gilt sowohl für at. js als auch für mbox. js):

* Seite 1 gehört zu Eigenschaft 1.
* Seite 2 gehört zu Eigenschaft 2.
* In der Aktivität leitet Seite 1 auf Seite 2 ein, die Clicktracks enthält.

Wenn ein Besucher Seite 1 in einem Browser öffnet, wird er zu Seite 2 umgeleitet. Da Seite 2 nicht zur Bereitstellung der Aktivität berechtigt ist, enthält der Target-Aufruf keine Clicktracks in der Antwort.

Wenn die Umleitungsseite und die Aktivitäts-URL zu derselben Eigenschaft gehören, funktionieren die Clicktracks erwartungsgemäß. Weitere Informationen finden Sie unter [Klick-Tracking](/help/c-activities/r-success-metrics/click-tracking.md).

## Schulungsvideo: Schulungsvideo für Unternehmensberechtigungen {#section_2FA080303A064242B63FF16CFA6DB31D}

Lernziele:

* Die drei möglichen Rollenebenen von Adobe Target-Benutzern
* Die Konzepte von Eigenschaften und Arbeitsbereichen und wie diese Grenzen und Gruppierungen funktionieren, um die Zugangsebenen der Benutzer steuern zu können
* Verschiedene Beispiele für Eigenschaften für Ihre Organisation

>[!VIDEO](https://video.tv.adobe.com/v/19042/)