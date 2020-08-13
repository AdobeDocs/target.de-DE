---
keywords: site pages;target site pages;targeting;current page;target current page;previous page;target previous page;landing page;target landing page;http header
description: Sie können Besucher auf einer bestimmten Seite Ihrer Site Zielgruppe werden.
title: Site-Seiten in Adobe Target
feature: audiences
topic: Standard
uuid: 1cf9fa94-dbec-4719-9a0a-79c1eb91a233
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 43%

---


# Seiten der Site{#site-pages}

Sie können Besucher auf einer bestimmten Seite Ihrer Site Zielgruppe werden.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Nennen Sie die Zielgruppe.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** > **[!UICONTROL Seiten der Site]**.

   ![Seiten der Site als Zielgruppe](assets/target_site_pages.png)

1. Click the **[!UICONTROL Select]** drop-down list, select one of the following options, then configure the rule as desired.

   Die verfügbaren Optionen und Bewertungsfaktoren in den nachfolgenden Dropdown-Listen in der Regel variieren je nach ausgewählter Option. Die folgende Abbildung zeigt die verfügbaren Optionen, wenn Sie &quot; [!UICONTROL Aktuelle Seite]&quot;auswählen:

   ![Aktuelle Seite](/help/c-target/c-audiences/c-target-rules/assets/current-page.png)

   Die folgenden Optionen stehen in der ersten Dropdown-Liste zur Verfügung, wenn Sie &quot; [!UICONTROL Auswählen]&quot;wählen.

   * **Aktuelle Seite:** Die Seite, auf der sich der Benutzer derzeit befindet.

      Die folgenden Optionen stehen in der zweiten Dropdown-Liste zur Verfügung, wenn Sie diese Option wählen:

      * URL (Weitere Informationen zur Bewertung von URLs durch Zielgruppe finden Sie unter Häufig gestellte Fragen zu [Zielgruppen und Audiencen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Domäne
      * Abfrage
      * Subdomäne
      * Domäne auf oberster Ebene
      * Pfad
      * Hash (#)-Fragment
   * **Vorherige Seite:** Die Seite, die der Benutzer vor dem Anklicken der aktuellen Seite aufgerufen hat. (Der Benutzer muss von der letzten Seite auf die aktuelle Seite klicken, damit die Seite nachverfolgt wird. Die vorherige Seite wird nicht verfolgt, wenn der Benutzer eine neue URL in den Browser eingibt.) Der tatsächliche Inhalt auf dieser Seite hängt vom Design Ihrer Site ab. Wenn beispielsweise auf der aktuellen Seite Informationen zu einem bestimmten Produkt angezeigt werden, kann es sich bei der letzten Seite um eine Kategorieseite, auf der der Benutzer ein bestimmtes Element ausgewählt hat (zum Beispiel eine Seite, auf mehrere Kameras eines bestimmten Typs angezeigt werden) oder eine Homepage mit Verweis auf die Ausstiegsseite handeln.

      Die folgenden Optionen stehen in der zweiten Dropdown-Liste zur Verfügung, wenn Sie diese Option wählen:

      * URL (Weitere Informationen zur Bewertung von URLs durch Zielgruppe finden Sie unter Häufig gestellte Fragen zu [Zielgruppen und Audiencen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Domäne
      * Abfrage
      * Subdomäne
      * Domäne auf oberster Ebene
      * Pfad
   * **Landingpage:** Die Landingpage ist die Seite, die Besuchern beim Zugriff auf Ihre Site zuerst angezeigt wird. Wenn der Besucher z. B. auf einen Link in Google klickt, der zu einer Kategorieseite führt, ist die Kategorieseite die Landingpage. Wenn der Link zu Ihrer Homepage führt, ist die Homepage die Landingpage. Die Landingpage wird während der Benutzersitzung gespeichert. Sie können Ihr Ziel tiefer in die Site richten, je nachdem, welche Seite die Landingpage des Benutzers in dieser Sitzung war.

      Die folgenden Optionen stehen in der zweiten Dropdown-Liste zur Verfügung, wenn Sie diese Option wählen:

      * URL (Weitere Informationen zur Bewertung von URLs durch Zielgruppe finden Sie unter Häufig gestellte Fragen zu [Zielgruppen und Audiencen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Domäne
      * Abfrage
      * Subdomäne
      * Domäne auf oberster Ebene
      * Pfad
      * Hash (#)-Fragment

      >[!NOTE]
      >
      >Das `landing.url`-Objekt wird bei einer Änderung der Subdomäne oder einer direkten URL-Ersetzung zurückgesetzt.

   * **HTTP-Kopfzeile:** Mit dieser Option werden die Informationen im HTTP-Header der Anforderung &quot;Zielgruppe&quot;ausgewertet. Wenn der HTTP-Header beispielsweise Sprachinformationen enthält, können Sie eine Regel erstellen, die die `Accept-Language: es` Bedingung für Besucher der Zielgruppe enthält, die auf Spanisch zugreifen.

      Die folgenden Optionen stehen in der zweiten Dropdown-Liste zur Verfügung, wenn Sie diese Option wählen:

      * Accept
      * Accept-Charset
      * Accept-Encoding
      * Accept-Language
      * Genehmigung
      * Cache-Control
      * Verbindung
      * Content-Length
      * Content-MDS
      * Content-Type
      * Datum
      * Erwarten
      * Von
      * Host
      * If-Match
      * If-Modified-Since
      * If-none-match
      * If-Range
      * If-Unchanged-Since
      * Max-Forwards
      * Pragma
      * Proxy-Autorisierung
      * Bereich
      * Referer
      * TE
      * Aktualisierung
      * User-Agent
      * Via
      * Warnung

   If you chose [!UICONTROL Current Page], [!UICONTROL Previous Page], or [!UICONTROL Landing Page], the [!UICONTROL Domain] and [!UICONTROL Query] options are available. Consider the following when choosing these options:

   * **Domäne:** Die vollständige Domäne der Seite Für das Festlegen einer Domäne wird die Versendung von „contains“ empfohlen. Beispiel: „Domain equals facebook.com“ wird `m.facebook.com` oder `www.facebook.com` nicht akzeptieren. „Domain contains facebook.com“ hingegen erfasst alle Varianten von „facebook.com“.
   * **Abfrage:** Der Inhalt der URL nach dem ersten Fragezeichen (?) 

      `foo.html?e0a72cb2a2c7`





1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und legen Sie zusätzliche Regeln für die Zielgruppe fest.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Sie können Website-Zielgruppen auch mit einem eigenen „benutzerdefinierten Abfrageparameter“ oder „benutzerdefinierten Header“ erstellen.

Verwenden Sie:

* Abfrageparameter, wenn die vom Benutzer ausgewählte Regel „Aktuelle Seite“, „Landingpage“ oder „Vorherige Seite“ lautet.
* Header if the rule selected by the user is an HTTP header.

Siehe Abbildung unten:

![](assets/site_pages.png)

## Fehlerbehebung {#ts}

* For landing page audiences to function properly, requests must have the `mboxReferrer` parameter set (for the Delivery API the `context.address.referringUrl` parameter) that the at.js JavaScript library takes from the page using the `document.referrer` attribute. This `HTMLDocument` attribute returns the URI of the page the user has navigated from. The value of this attribute is an empty string when the user navigates to the page directly (not through a link, but, for example, via a bookmark).

   If this behavior does not match your requirements, consider performing one of the following actions:

   * Übergeben Sie [Mbox-Parameter](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) , die für Targeting-Zwecke verwendet [!DNL Target] werden sollen.
   * Use an [A/B Test activity](/help/c-activities/t-test-ab/test-ab.md) instead of a landing page activity. A/B-Test-Aktivitäten wechseln die Erlebnisse nicht für denselben Besucher.
   * Verwenden Sie stattdessen ein [Besucher-Profil](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) .

* When using &quot;starts/ends with&quot; evaluators on strings containing commas, be aware that these
are evaluated as an array of values, in which each value separated by comma is evaluated. For example if we have the value for a header: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` it will quaify for conditons like:
   * beginn mit Zh,
   * beginn mit en,
   * endet mit 0,7,
   * endet mit 0,8.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
