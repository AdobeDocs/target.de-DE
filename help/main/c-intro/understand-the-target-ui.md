---
keywords: Target-Benutzeroberfläche;Benutzeroberfläche;UI;Ankündigungen;Ereignisse;Benachrichtigungen
description: Machen Sie sich mit der Benutzeroberfläche vertraut und finden Sie Links zu ausführlicheren Informationen, die Ihnen helfen, [!DNL Target] optimal zu nutzen.
title: Wie verwende ich die Benutzeroberfläche von  [!DNL Target]
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
source-git-commit: 6bef27637c06f39ffc0e755f19e8a0870ec749e5
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 31%

---

# Die Benutzeroberfläche von [!DNL Target]

Die Benutzeroberfläche ist logisch und übersichtlich angeordnet. Sie finden dort schnell, was Sie zur optimalen Nutzung von [!DNL Adobe Target] benötigen. Die folgende kurze Übersicht hilft Ihnen, sich mit [!DNL Target] vertraut zu machen, bietet Links für ausführlichere Informationen und schrittweise Anweisungen.

Die Kopfzeile oben in der Benutzeroberfläche von [!DNL Target] enthält Registerkarten und Optionen, mit denen Sie durch die verschiedenen Funktionen der Lösung navigieren können. Sie können auch zwischen Organisationen und [!DNL Adobe Experience Cloud] Lösungen wechseln, Hilfe und Benachrichtigungen erhalten, Ihr [!DNL Adobe] Profil verwalten und sich bei [!DNL Target] abmelden.

![Kopfzeile von Target](/help/main/c-intro/assets/target-header.png)

Über die Registerkarten auf der linken Seite können Sie auf die verschiedenen Funktionen von [!DNL Target] zugreifen, die später besprochen werden. Zuvor sehen wir uns aber die Optionen auf der rechten Seite an.

## Organisationen

Eine *Organisation* ist die Entität, die es einem Administrator ermöglicht, Gruppen und Benutzer zu konfigurieren und Single Sign-on für die [!DNL Adobe Experience Cloud] zu steuern. Die Organisation agiert als zentrale Anmeldestelle, die sämtliche [!DNL Experience Cloud]-Produkte und -Lösungen umfasst. In den meisten Fällen entspricht die Organisation dem Namen Ihres Unternehmens. Ein Unternehmen kann aber auch aus mehreren Organisationen bestehen.

Wählen Sie die gewünschte Organisation aus der Dropdownliste [!UICONTROL Organization] aus, wenn Ihr Unternehmen über mehrere Organisationen verfügt:

![Dropdown-Liste „Organisation“](/help/main/c-intro/assets/organizations.png)

## Apps

Mit dem Apps Switcher können Sie schnell zwischen den [!DNL Adobe Experience Cloud]-Lösungen wechseln, auf die Sie Zugriff haben.

![Apps Switcher](/help/main/c-intro/assets/apps.png)

## Hilfe

Über das Hilfesymbol können Sie auf Informationen, Videos, Blogs und andere Ressourcen zugreifen, die Ihnen helfen, [!DNL Target] effektiver zu verwenden. Sie können ein Support-Ticket erstellen, Support-Telefonnummern finden, Fragen per Twitter stellen oder Feedback zu [!DNL Target] geben, um uns mitzuteilen, wie das [!DNL Target]-Team vorgeht.

![Hilfe ](/help/main/c-intro/assets/help.png)

## Benachrichtigungen und Ankündigungen {#notifications-announcements}

Die Bedienfelder [!UICONTROL Notifications] und [!UICONTROL Announcements] helfen Ihnen dabei, über alle Dinge auf dem Laufenden zu bleiben [!DNL Adobe Target]. Proaktive Benachrichtigungen helfen Ihnen dabei, den Status von [!DNL Adobe Experience Cloud] Lösungen und [!DNL Target] Ereignissen auf dem Laufenden zu halten. Proaktive Ankündigungen informieren Sie über geplante Ausfallzeiten (z. B. aufgrund von Systemwartungen).

Klicken Sie in der Kopfzeile auf das Glockensymbol , um Benachrichtigungen anzuzeigen:

![Glockensymbol für Benachrichtigungen und Mitteilungen](assets/bell-icon.png)

Das Bedienfeld enthält Registerkarten für [!UICONTROL Notifications] und [!UICONTROL Announcements].

![ Benachrichtigungen ](assets/notifications.png)

Die folgenden Abschnitte enthalten Informationen zu den einzelnen Registerkarten und zur Konfiguration von Benachrichtigungen und Mitteilungen:

### Benachrichtigungen {#notifications}

[!DNL Target] -Ereignisbenachrichtigungen beinhalten Folgendes:

* **Aktivitäten**: Benachrichtigungen für alle Aktivitätstypen, wenn eine Aktivität genehmigt oder deaktiviert wird, entweder manuell oder beim Erreichen des Start- oder Enddatums. Die Benachrichtigung enthält den Namen der Aktivität mit einem Link zur Übersichtsseite der Aktivität.

  Benachrichtigungen sind konfigurierbar und werden standardmäßig von Produktadministratoren, Herausgebern und Genehmigern im Arbeitsbereich der Aktivität für [!DNL Target Premium] -Konten empfangen. Bei [!DNL Target Standard] -Konten werden Benachrichtigungen von allen Herausgebern und Genehmigern empfangen.

  Benachrichtigungen sind wie die folgenden Beispiele formatiert:

   * `Activity {target.activity.name} has been activated`

   * `Activity {target.activity.name} has been deactivated`

* **Profilskripte**: Benachrichtigungen, wenn ein Profilskript entweder manuell oder durch [!DNL Target] aktiviert oder deaktiviert wird.

  Benachrichtigungen sind konfigurierbar und werden standardmäßig von Produktadministratoren und Genehmigern für sowohl [!DNL Target Premium]- als auch [!DNL Target Standard]-Konten empfangen.

  Benachrichtigungen sind wie die folgenden Beispiele formatiert:

   * `Profile Script {target.profileScript.name} has been activated`
   * `Profile Script {target.profileScript.name} has been deactivated`

* **Recommendations-Feeds**: Benachrichtigungen, wenn ein [!DNL Recommendations] -Feed entweder manuell oder durch [!DNL Target] aktiviert oder deaktiviert wird. Benachrichtigungen werden auch gesendet, wenn ein [!DNL Recommendations] -Feed fehlschlägt.

  Benachrichtigungen sind konfigurierbar und werden standardmäßig von Produktadministratoren und Genehmigern für [!DNL Target Premium] -Konten empfangen. [!DNL Recommendations] ist eine [!DNL Target Premium]-Funktion und nicht in [!DNL Target Standard] verfügbar.

  Benachrichtigungen sind wie die folgenden Beispiele formatiert:

   * `Feed  {target.feed.name} has been activated`
   * `Feed {target.feed.name} has been deactivated`
   * `Feed {target.feed.name} has failed`
   * `Feed {target.feed.name} has failed to import from source`

Sie können einzelne Benachrichtigungen als gelesen markieren, indem Sie den Mauszeiger über die gewünschte Benachrichtigung bewegen und dann auf das Häkchen klicken. Sie können alle Benachrichtigungen als gelesen markieren oder alle Benachrichtigungen anzeigen, indem Sie unten im Bedienfeld auf [!UICONTROL "Mark as Read"] oder [!UICONTROL "View All"] klicken.

Sie können auch eine Erinnerung festlegen, die erneut benachrichtigt werden soll, indem Sie den Mauszeiger über eine Benachrichtigung bewegen, auf das Symbol &quot;[!UICONTROL Remind me]&quot;klicken und auswählen, wann Sie benachrichtigt werden möchten: 5 Minuten, 15 Minuten, eine Stunde oder morgen.

### Mitteilungen

Proaktive Ankündigungen informieren Sie über geplante Ausfallzeiten (z. B. aufgrund von Systemwartungen).

Detailliertere Informationen finden Sie auf der Seite [Adobe-Status](https://status.adobe.com/de) .

### Benachrichtigungen und Mitteilungen konfigurieren

So bearbeiten Sie Ihre Benachrichtigungseinstellungen:

1. Klicken Sie auf das Zahnradsymbol und dann auf **[!UICONTROL Notifications]**.
1. Klicken Sie unter **[!UICONTROL Target]** auf **[!UICONTROL Customize]**.
1. Wählen Sie die Kategorien aus oder heben Sie die Auswahl auf, für die Sie Benachrichtigungen erhalten möchten:

   * Anforderungen: Wenn Sie von einer Person angefordert werden, ein Objekt zu genehmigen oder Zugriff auf ein Objekt zu gewähren. Sie können sich nicht von dieser Kategorie abmelden.
   * Zugeordnet: Wenn Ihnen jemand ein Objekt zuweist.
   * Erwähnungen: Wenn jemand Sie in einem Kommentar erwähnt.
   * Neue Versionen: Wenn eine neue Version für ein Produkt oder einen Dienst verfügbar ist, auf das Sie Zugriff haben.
   * Für mich freigegeben: Wenn jemand ein Objekt für Sie freigegeben hat.
   * Aktualisierungen des Inhalts: Wenn ein Benutzer ein von Ihnen erstelltes oder befolgtes Objekt bearbeitet, löscht oder kommentiert.
   * Sonstige:

   >[!NOTE]
   >
   >&quot;Neue Versionen&quot;und &quot;Aktualisierungen des Inhalts&quot;sind die einzigen Benachrichtigungskategorien, die für [!DNL Target] gelten. Die anderen Kategorien gelten auch für andere Adobe-Lösungen.


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

Die Liste **[!UICONTROL Activities]** ist die Standardansicht beim Öffnen von [!DNL Target]. Sie können auf dieser Seite Aktivitäten erstellen und vorhandene Aktivitäten verwalten.

![Aktivitätenliste](/help/main/c-intro/assets/activities-list.png)

Detaillierte Informationen zu den in [!DNL Target] verfügbaren Aktivitätstypen und weitere Informationen zur Benutzeroberfläche der Liste [!UICONTROL Activity] finden Sie unter [Aktivitäten](/help/main/c-activities/activities.md) .

## Zielgruppen

Klicken Sie auf die Registerkarte **[!UICONTROL Audiences]** , um die Liste [!UICONTROL Audiences] anzuzeigen, in der Sie Zielgruppen erstellen und bestehende Zielgruppen verwalten können.

![Liste der Zielgruppen](/help/main/c-intro/assets/audience-list.png)

Eine Zielgruppe ist eine Gruppe ähnlicher Aktivitätsteilnehmer, für die eine zielgerichtete Aktivität angezeigt wird. Eine Zielgruppe ist eine Gruppe von Personen mit denselben Merkmalen, wie z. B. ein neuer Besucher, ein wiederkehrender Besucher oder wiederkehrende Besucher aus einer bestimmten Region. Mit der Funktion [!UICONTROL Audience] können Sie verschiedene Inhalte und Erlebnisse auf bestimmte Zielgruppen ausrichten, um Ihr digitales Marketing zu optimieren, indem Sie die richtigen Botschaften zum richtigen Zeitpunkt für die richtigen Personen anzeigen. Wird ein Besucher als Teil einer Zielgruppe identifiziert, bestimmt [!DNL Target] basierend auf den Kriterien, die bei der Erstellung der Aktivität festgelegt wurden, welches Erlebnis ihm angezeigt wird.

Detaillierte Informationen zu den Zielgruppentypen in [!DNL Target] finden Sie unter [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/create-audience.md) und weitere Informationen zur Benutzeroberfläche der Liste [!UICONTROL Audience] .

## Angebote

Klicken Sie auf die Registerkarte **[!UICONTROL Offers]** , um die Liste [!UICONTROL Offers] anzuzeigen, in der Sie Erlebnisse und Angebote erstellen und vorhandene Erlebnisse und Angebote verwalten können.

![Liste der Angebote](/help/main/c-intro/assets/offers.png)

Ein Erlebnis kann ein Angebot, ein Bild, ein Text, eine Schaltfläche, ein Video, eine Kombination dieser Elemente auf einer Seite, eine gesamte Webseite oder mehrere Seiten sein, die möglicherweise einen Kauftrichter oder eine andere logische Seitenfolge bilden. Ein Erlebnis kann auch die Antwort eines Sprachassistenten, ein Skript für den Kundendienst oder sogar ein personalisierter Geschmack in einem Getränkeautomaten sein. Sie können Erlebnisse in [!DNL Target] Aktivitäten testen oder personalisieren.

Detaillierte Informationen zu den Angebotstypen in [!DNL Target] finden Sie unter [Angebote](/help/main/c-experiences/c-manage-content/manage-content.md) und weitere Informationen zur Benutzeroberfläche der Liste [!UICONTROL Offer] .

## Recommendations

Klicken Sie auf die Registerkarte **[!UICONTROL Recommendations]** , um auf [!DNL Target Recommendations] zuzugreifen.

>[!NOTE]
>
>Recommendations-Aktivitäten sind als Teil der [!DNL Target Premium]-Lösung verfügbar. In [!DNL Target Standard] sind sie nur mit einer [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen finden Sie im Abschnitt *Einführung in Target* unter [Target Premium](/help/main/c-intro/intro.md#premium).

![Recommendations](/help/main/c-intro/assets/recommendations.png)

[!UICONTROL Recommendations] -Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten. Recommendations tragen dazu bei, Kundinnen und Kunden zu relevanten Elementen zu lenken, von denen sie andernfalls möglicherweise nichts wüssten.

Detaillierte Informationen zu [!UICONTROL Recommendations] in [!DNL Target] finden Sie unter [Recommendations](/help/main/c-recommendations/recommendations.md) und weitere Informationen zur Benutzeroberfläche von [!UICONTROL Recommendations].

## Administrations-

Klicken Sie auf die Registerkarte **[!UICONTROL Administration]** , um auf die Seiten [!UICONTROL Administration] zuzugreifen.

![Administrationsseiten](/help/main/c-intro/assets/administration.png)

Auf den [!UICONTROL Administration] -Seiten können Sie [!DNL Target] verwalten, einschließlich Konfigurationseinstellungen für [!UICONTROL Visual Experience Composer] (VEC), Berichterstellung, Konfiguration, Implementierung, Hosts, Umgebungen, Antwort-Token und Benutzer.[!DNL Scene7]

Unter [Verwaltung von Target – Überblick](/help/main/administrating-target/administrating-target.md) finden Sie detaillierte Informationen zur Verwaltung von Target und weitere Informationen zur Benutzeroberfläche der Administrationsseiten.
