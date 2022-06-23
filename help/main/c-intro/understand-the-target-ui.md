---
keywords: Benutzeroberfläche von Target; Benutzeroberfläche; uiAnkündigungen; Ereignisse
description: Machen Sie sich mit der Benutzeroberfläche vertraut und finden Sie Links zu ausführlicheren Informationen, die Ihnen helfen, das Beste aus den [!DNL Target].
title: 'Wie verwende ich die Benutzeroberfläche von  [!DNL Target] '
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
source-git-commit: 3a180f083436b88cdf5953a1d5c6d590a9b2613a
workflow-type: tm+mt
source-wordcount: '1373'
ht-degree: 43%

---

# Die Benutzeroberfläche von [!DNL Target]

Die Benutzeroberfläche ist logisch und übersichtlich angeordnet. Sie finden dort schnell, was Sie zur optimalen Nutzung von [!DNL Adobe Target] benötigen. Die folgende kurze Übersicht hilft Ihnen, sich mit [!DNL Target] und bietet Links für detailliertere Informationen und schrittweise Anweisungen.

Die Kopfzeile oben im [!DNL Target] Die Benutzeroberfläche enthält Registerkarten und Optionen, mit denen Sie durch die verschiedenen Funktionen der Lösung navigieren können. Sie können auch zwischen Organisationen wechseln und [!DNL Adobe Experience Cloud] Lösungen, Hilfe und Benachrichtigungen abrufen, Ihre [!DNL Adobe] Profil erstellen und sich von [!DNL Target].

![Kopfzeile von Target](/help/main/c-intro/assets/target-header.png)

Über die Registerkarten auf der linken Seite können Sie auf die verschiedenen Funktionen von [!DNL Target], der später besprochen wird. Zuvor sehen wir uns aber die Optionen auf der rechten Seite an.

## Organisationen

Eine *Organisation* ist die Entität, die es einem Administrator ermöglicht, Gruppen und Benutzer zu konfigurieren und Single Sign-on für die [!DNL Adobe Experience Cloud] zu steuern. Die Organisation agiert als zentrale Anmeldestelle, die sämtliche [!DNL Experience Cloud]-Produkte und -Lösungen umfasst. In den meisten Fällen entspricht die Organisation dem Namen Ihres Unternehmens. Ein Unternehmen kann aber auch aus mehreren Organisationen bestehen.

Wählen Sie die gewünschte Organisation in der Dropdown-Liste [!UICONTROL Organisation] aus, wenn Ihr Unternehmen aus mehreren Organisationen besteht:

![Dropdown-Liste „Organisation“](/help/main/c-intro/assets/organizations.png)

## Apps

Mit dem Apps Switcher können Sie schnell zwischen den [!DNL Adobe Experience Cloud]-Lösungen wechseln, auf die Sie Zugriff haben.

![Apps Switcher](/help/main/c-intro/assets/apps.png)

## Hilfe

Über das Hilfesymbol können Sie auf Informationen, Videos, Blogs und andere Ressourcen zugreifen, die Ihnen helfen, [!DNL Target] effektiver zu verwenden. Sie können ein Support-Ticket erstellen, Support-Telefonnummern finden, Fragen über Twitter stellen oder Feedback zu [!DNL Target] um uns mitzuteilen, wie die [!DNL Target] Team tut es.

![Hilfe ](/help/main/c-intro/assets/help.png)

## Benachrichtigungen und Ankündigungen

Über die Bedienfelder [!UICONTROL Benachrichtigungen] und [!UICONTROL Ankündigungen] bleiben Sie stets über alles Wissenswerte zu [!DNL Adobe Target] informiert. Proaktive Benachrichtigungen helfen Ihnen dabei, den Status von [!DNL Adobe Experience Cloud] Lösungen und [!DNL Target] -Ereignisse. Proaktive Ankündigungen informieren Sie über geplante Ausfallzeiten (z. B. aufgrund von Systemwartungen).

>[!NOTE]
>
>Informationen über die erweiterten [!UICONTROL Benachrichtigungen und Mitteilungen] Bereich in diesem Abschnitt gilt derzeit für die Auswahl von [!DNL Target] -Kunden und in den kommenden Monaten allen Kunden bereitgestellt werden.

Klicken Sie in der Kopfzeile auf das Glockensymbol , um Benachrichtigungen anzuzeigen:

![Glockensymbol für Benachrichtigungen und Mitteilungen](assets/bell-icon.png)

Das Bedienfeld enthält Registerkarten für [!UICONTROL Benachrichtigungen] und [!UICONTROL Mitteilungen].

![ Benachrichtigungen ](assets/notifications.png)

Die folgenden Abschnitte enthalten Informationen zu den einzelnen Registerkarten und zur Konfiguration von Benachrichtigungen und Mitteilungen.

###  Benachrichtigungen 

[!DNL Target] Ereignisbenachrichtigungen beinhalten Folgendes:

* **Tätigkeiten**: Benachrichtigungen für alle Aktivitätstypen, wenn eine Aktivität genehmigt oder deaktiviert wird, entweder manuell oder beim Erreichen des Start- oder Enddatums. Die Benachrichtigung enthält den Namen der Aktivität mit einem Link zur Übersichtsseite der Aktivität.

   Benachrichtigungen sind konfigurierbar und werden standardmäßig von Produktadministratoren, Herausgebern und Genehmigern im Arbeitsbereich der Aktivität empfangen für [!DNL Target Premium] Konten. Für [!DNL Target Standard] Konten, werden Benachrichtigungen von allen Herausgebern und Genehmigern empfangen.

   Benachrichtigungen sind wie die folgenden Beispiele formatiert:

   * `Activity {target.activity.name} has been activated`

   * `Activity {target.activity.name} has been deactivated`

* **Profilskripte**: Benachrichtigungen bei der Aktivierung oder Deaktivierung eines Profilskripts entweder manuell oder durch [!DNL Target].

   Benachrichtigungen sind konfigurierbar und werden standardmäßig von Produktadministratoren und Genehmigern für [!DNL Target Premium] und [!DNL Target Standard] Konten.

   Benachrichtigungen sind wie die folgenden Beispiele formatiert:

   * `Profile Script {target.profileScript.name} has been activated`
   * `Profile Script {target.profileScript.name} has been deactivated`

* **Recommendations Feeds**: Benachrichtigungen bei einem [!DNL Recommendations] Feed wird entweder manuell oder durch [!DNL Target]. Benachrichtigungen werden auch gesendet, wenn eine [!DNL Recommendations] Feed schlägt fehl.

   Benachrichtigungen sind konfigurierbar und werden standardmäßig von Produktadministratoren und Genehmigern für [!DNL Target Premium] Konten. [!DNL Recommendations] ist [!DNL Target Premium] und nicht verfügbar in [!DNL Target Standard].

   Benachrichtigungen sind wie die folgenden Beispiele formatiert:

   * `Feed  {target.feed.name} has been activated`
   * `Feed {target.feed.name} has been deactivated`
   * `Feed {target.feed.name} has failed to import from source`

Sie können einzelne Benachrichtigungen als gelesen markieren, indem Sie den Mauszeiger über die gewünschte Benachrichtigung bewegen und dann auf das Häkchen klicken. Sie können alle Benachrichtigungen als gelesen markieren oder alle Benachrichtigungen anzeigen, indem Sie auf [!UICONTROL &quot;Als gelesen markieren&quot;] oder [!UICONTROL &quot;Alle anzeigen&quot;] am unteren Rand des Bedienfelds.

Sie können auch eine Erinnerung festlegen, die erneut benachrichtigt werden soll, indem Sie den Mauszeiger über eine Benachrichtigung bewegen und auf die Schaltfläche[!UICONTROL Erinnern]&quot;, und wählen Sie dann aus, wann Sie benachrichtigt werden möchten: 5 Minuten, 15 Minuten, eine Stunde oder morgen.

### Mitteilungen

Proaktive Ankündigungen informieren Sie über geplante Ausfallzeiten (z. B. aufgrund von Systemwartungen).

Detailliertere Informationen finden Sie auf der Seite [Adobe-Status.](https://status.adobe.com/)

### Benachrichtigungen und Mitteilungen konfigurieren

So bearbeiten Sie Ihre Benachrichtigungseinstellungen:

1. Klicken Sie auf das Zahnradsymbol und dann auf **[!UICONTROL Benachrichtigungen]**.
1. under **[!UICONTROL Target]** klicken **[!UICONTROL Anpassen]**.
1. Wählen Sie die Kategorien aus oder heben Sie die Auswahl auf, für die Sie Benachrichtigungen erhalten möchten:

   * Anforderungen: Wenn Sie von einer Person angefordert werden, ein Objekt zu genehmigen oder Zugriff auf ein Objekt zu gewähren. Sie können sich nicht von dieser Kategorie abmelden.
   * Zugeordnet: Wenn Ihnen jemand ein Objekt zuweist.
   * Erwähnungen: Wenn jemand Sie in einem Kommentar erwähnt.
   * Neue Versionen: Wenn eine neue Version für ein Produkt oder einen Dienst verfügbar ist, auf den Sie Zugriff haben.
   * Für mich freigegeben: Wenn jemand ein Objekt mit Ihnen teilt.
   * Inhaltsaktualisierungen: Wenn jemand ein Objekt bearbeitet, löscht oder kommentiert, das Sie erstellt haben oder dem Sie folgen.
   * Sonstige:

   >[!NOTE]
   >
   >&quot;Neue Versionen&quot;und &quot;Aktualisierungen des Inhalts&quot;sind die einzigen Benachrichtigungskategorien, die für [!DNL Target]. Die anderen Kategorien gelten auch für andere Adoben.


1. Wählen Sie die Kategorien aus, die als vorrangig betrachtet werden sollen.
1. Wählen Sie die Benachrichtigungen aus, für die Warnhinweise in Ihrem Browser angezeigt werden sollen.

   Diese Warnungen werden einige Sekunden lang in der oberen rechten Ecke Ihres Browsers angezeigt. Sie können festlegen, dass Kategorien mit hoher Priorität, alle Kategorien oder alle Popup-Fenster für Benachrichtigungen angezeigt werden sollen. Sie können auch konfigurieren, ob die Benachrichtigungen so lange sichtbar bleiben sollen, bis Sie sie schließen, oder ob Sie die Benachrichtigungsdauer konfigurieren können.

1. Wählen Sie die Häufigkeit aus, mit der Sie Benachrichtigungs-E-Mails erhalten möchten:

   * E-Mails nicht senden
   * Sofortige Benachrichtigungen
   * Tägliche Zusammenfassung
   * Wöchentliche Digest

## Profil

Klicken Sie auf Ihren Profilavatar, um Ihre Voreinstellungen für [!DNL Adobe Experience Cloud] zu ändern oder sich von [!DNL Target] abzumelden. Sie können damit auch auf Ihr [!DNL Adobe]-Profil zugreifen und es bearbeiten.

![Profilavatar](/help/main/c-intro/assets/change-language.png)

Sehen wir uns nun aber die Registerkarten auf der linken Seite der [!DNL Target]-Kopfzeile an.

## Aktivitäten

Die Liste **[!UICONTROL Aktivitäten]** ist die Standardansicht beim Öffnen [!DNL Target]. Sie können auf dieser Seite Aktivitäten erstellen und vorhandene Aktivitäten verwalten.

![Aktivitätenliste](/help/main/c-intro/assets/activities-list.png)

Unter [Aktivitäten](/help/main/c-activities/activities.md) finden Sie detaillierte Informationen zu den in [!DNL Target] verfügbaren Aktivitäten und weitere Informationen zur Benutzeroberfläche der Liste [!UICONTROL Aktivitäten].

## Zielgruppen

Klicken Sie auf **[!UICONTROL Zielgruppen]** zum Anzeigen der [!UICONTROL Zielgruppen] Liste, in der Sie Zielgruppen erstellen und bestehende Zielgruppen verwalten können.

![Liste der Zielgruppen](/help/main/c-intro/assets/audience-list.png)

Eine Zielgruppe ist eine Gruppe ähnlicher Aktivitätsteilnehmer, für die eine zielgerichtete Aktivität angezeigt wird. Eine Zielgruppe ist eine Gruppe von Personen mit denselben Merkmalen, wie z. B. ein neuer Besucher, ein wiederkehrender Besucher oder wiederkehrende Besucher aus einer bestimmten Region. Mit der Funktion [!UICONTROL Zielgruppen] können Sie Ihre Inhalte und Erlebnisse speziell an bestimmte Zielgruppen anpassen. Durch geeignete Botschaften zum richtigen Zeitpunkt für die richtigen Personen können Sie so Ihr digitales Marketing optimieren. Wird ein Besucher als Teil einer Zielgruppe identifiziert, bestimmt [!DNL Target] basierend auf den Kriterien, die bei der Erstellung der Aktivität festgelegt wurden, welches Erlebnis ihm angezeigt wird.

Unter [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/create-audience.md) finden Sie detaillierte Informationen zu den Zielgruppentypen in [!DNL Target] und weitere Informationen zur Benutzeroberfläche der Liste [!UICONTROL Zielgruppen].

## Angebote

Klicken Sie auf **[!UICONTROL Angebote]** zum Anzeigen der [!UICONTROL Angebote] Liste, in der Sie Erlebnisse und Angebote erstellen und vorhandene Erlebnisse und Angebote verwalten können.

![Liste der Angebote](/help/main/c-intro/assets/offers.png)

Ein Erlebnis kann ein Angebot, ein Bild, ein Text, eine Schaltfläche, ein Video, eine Kombination dieser Elemente auf einer Seite, eine gesamte Webseite oder mehrere Seiten sein, die möglicherweise einen Kauftrichter oder eine andere logische Seitenfolge bilden. Ein Erlebnis kann auch die Antwort eines Sprachassistenten, ein Skript für den Kundendienst oder sogar ein personalisierter Geschmack in einem Getränkeautomaten sein. Sie können Erlebnisse in [!DNL Target] Aktivitäten testen oder personalisieren.

Unter [Angebote](/help/main/c-experiences/c-manage-content/manage-content.md) finden Sie detaillierte Informationen zu den Angebotstypen in [!DNL Target] und weitere Informationen zur Benutzeroberfläche der Liste [!UICONTROL Angebote].

## Recommendations

Klicken Sie auf die Registerkarte **[!UICONTROL Recommendations]**, um auf [!DNL Target Recommendations] zuzugreifen.

>[!NOTE]
>
>Recommendations-Aktivitäten sind als Teil der [!DNL Target Premium]-Lösung verfügbar. In [!DNL Target Standard] sind sie nur mit einer [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen finden Sie im Abschnitt *Einführung in Target* unter [Target Premium](/help/main/c-intro/intro.md#premium).

![Recommendations](/help/main/c-intro/assets/recommendations.png)

[!UICONTROL Recommendations]-Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten. Recommendations hilft Kunden, zu relevanten Artikeln weiterzuleiten, von denen sie womöglich noch nichts wissen.

Unter [Recommendations](/help/main/c-recommendations/recommendations.md) finden Sie detaillierte Informationen zu [!UICONTROL Recommendations] in [!DNL Target] und weitere Informationen zur Benutzeroberfläche von [!UICONTROL Recommendations].

## Administrations-

Klicken Sie auf die Registerkarte **[!UICONTROL Administration]**, um auf die Seiten der [!UICONTROL Administration] zuzugreifen.

![Administrationsseiten](/help/main/c-intro/assets/administration.png)

Auf den Seiten der [!UICONTROL Administration] können Sie [!DNL Target] einschließlich der Konfigurationseinstellungen für [!UICONTROL Visual Experience Composer] (VEC), der Berichterstellung, der Konfiguration von [!DNL Scene7], der Implementierung, Hosts, Umgebungen, Antwort-Token und Benutzern verwalten.

Unter [Verwaltung von Target – Überblick](/help/main/administrating-target/administrating-target.md) finden Sie detaillierte Informationen zur Verwaltung von Target und weitere Informationen zur Benutzeroberfläche der Administrationsseiten.
