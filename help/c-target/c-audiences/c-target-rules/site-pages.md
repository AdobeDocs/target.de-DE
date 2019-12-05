---
keywords: site pages;target site pages;targeting;current page;target current page;previous page;target previous page;landing page;target landing page;http header
description: Sie können Besucher, die sich auf einer bestimmten Seite Ihrer Site befinden, als Ziel auswählen.
title: Site-Seiten in Adobe Target
topic: Standard
uuid: 1cf9fa94-dbec-4719-9a0a-79c1eb91a233
translation-type: tm+mt
source-git-commit: 758ebad09d0e2ff267ee219519e63d6528b83491

---


# Seiten der Site{#site-pages}

Sie können Besucher, die sich auf einer bestimmten Seite Ihrer Site befinden, als Ziel auswählen.

1. Klicken Sie auf der [!DNL Target]-Benutzeroberfläche auf **[!UICONTROL Zielgruppen]** &gt; **[!UICONTROL Zielgruppe erstellen]**.
1. Nennen Sie die Zielgruppe.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** &gt; **[!UICONTROL Seiten der Site]**.

   ![Seiten der Site als Zielgruppe](assets/target_site_pages.png)

1. Klicken Sie auf die Dropdownliste **[!UICONTROL Auswählen]** , wählen Sie eine der folgenden Optionen und konfigurieren Sie dann die Regel wie gewünscht.

   Die verfügbaren Optionen und Auswerter in nachfolgenden Dropdownlisten in der Regel variieren je nach ausgewählter Option. Die folgende Abbildung zeigt die verfügbaren Optionen, wenn Sie " [!UICONTROL Aktuelle Seite]"auswählen:

   ![Aktuelle Seite](/help/c-target/c-audiences/c-target-rules/assets/current-page.png)

   Die folgenden Optionen stehen in der ersten Dropdown-Liste zur Verfügung, wenn Sie " [!UICONTROL Auswählen]"wählen.

   * **** Aktuelle Seite: Die Seite, auf der sich der Benutzer derzeit befindet.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * URL
      * Domäne
      * Abfrage
      * Subdomäne
      * Domäne auf oberster Ebene
      * Pfad
      * Hash (#)-Fragment
   * **Vorherige Seite:** Die Seite, die der Benutzer vor dem Anklicken der aktuellen Seite aufgerufen hat. (Der Benutzer muss von der letzten Seite auf die aktuelle Seite klicken, damit die Seite nachverfolgt wird. Die vorherige Seite wird nicht verfolgt, wenn der Benutzer eine neue URL in den Browser eingibt.) Der tatsächliche Inhalt auf dieser Seite hängt vom Design Ihrer Site ab. Wenn beispielsweise auf der aktuellen Seite Informationen zu einem bestimmten Produkt angezeigt werden, kann es sich bei der letzten Seite um eine Kategorieseite, auf der der Benutzer ein bestimmtes Element ausgewählt hat (zum Beispiel eine Seite, auf mehrere Kameras eines bestimmten Typs angezeigt werden) oder eine Homepage mit Verweis auf die Ausstiegsseite handeln.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * URL
      * Domäne
      * Abfrage
      * Subdomäne
      * Domäne auf oberster Ebene
      * Pfad
   * **Landingpage:** Die Landingpage ist die Seite, die Besuchern beim Zugriff auf Ihre Site zuerst angezeigt wird. Wenn der Besucher z. B. auf einen Link in Google klickt, der zu einer Kategorieseite führt, ist die Kategorieseite die Landingpage. Wenn der Link zu Ihrer Homepage führt, ist die Homepage die Landingpage. Die Landingpage wird während der Benutzersitzung gespeichert. Sie können Ihr Ziel tiefer in die Site richten, je nachdem, welche Seite die Landingpage des Benutzers in dieser Sitzung war.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * URL
      * Domäne
      * Abfrage
      * Subdomäne
      * Domäne auf oberster Ebene
      * Pfad
      * Hash (#)-Fragment
      >[!NOTE]
      >
      >Das `landing.url`-Objekt wird bei einer Änderung der Subdomäne oder einer direkten URL-Ersetzung zurückgesetzt.

   * **** HTTP-Kopfzeile: Diese Option bewertet die Informationen im HTTP-Header der Target-Anforderung. Wenn der HTTP-Header beispielsweise Sprachinformationen enthält, können Sie eine Regel erstellen, die die `Accept-Language: es` Bedingung für das Targeting von Besuchern enthält, die die Seite auf Spanisch aufrufen.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

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
      * Max. Vorwärts
      * Pragma
      * Proxy-Autorisierung
      * Bereich
      * Referer
      * TE
      * Aktualisierung
      * User-Agent
      * Via
      * Warnung
   Wenn Sie " [!UICONTROL Aktuelle Seite]", " [!UICONTROL Vorherige Seite]"oder " [!UICONTROL Einstiegsseite]"auswählen, stehen die Optionen " [!UICONTROL Domäne] "und " [!UICONTROL Abfrage] "zur Verfügung. Berücksichtigen Sie bei der Auswahl dieser Optionen Folgendes:

   * **Domäne:** Die vollständige Domäne der Seite Für das Festlegen einer Domäne wird die Versendung von „contains“ empfohlen. Beispiel: „Domain equals facebook.com“ wird `m.facebook.com` oder `www.facebook.com` nicht akzeptieren. „Domain contains facebook.com“ hingegen erfasst alle Varianten von „facebook.com“.
   * **Abfrage:** Der Inhalt der URL nach dem ersten Fragezeichen (?) 

      `foo.html?e0a72cb2a2c7`





1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und legen Sie zusätzliche Regeln für die Zielgruppe fest.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Sie können Website-Zielgruppen auch mit einem eigenen „benutzerdefinierten Abfrageparameter“ oder „benutzerdefinierten Header“ erstellen.

Verwenden Sie:

* Abfrageparameter, wenn die vom Benutzer ausgewählte Regel „Aktuelle Seite“, „Landingpage“ oder „Vorherige Seite“ lautet.
* Kopfzeile, wenn die vom Benutzer ausgewählte Regel ein HTTP-Header ist.

Siehe Abbildung unten:

![](assets/site_pages.png)

## Fehlerbehebung {#ts}

* Damit Zielgruppen von Einstiegsseiten ordnungsgemäß funktionieren, müssen für Anforderungen der `mboxReferrer` Parameter festgelegt sein (für die Auslieferungs-API der `context.address.referringUrl` Parameter), den die JavaScript-Bibliothek at.js mithilfe des `document.referrer` Attributs von der Seite nimmt. Dieses `HTMLDocument` Attribut gibt den URI der Seite zurück, von der der Benutzer navigiert hat. Der Wert dieses Attributs ist eine leere Zeichenfolge, wenn der Benutzer direkt zur Seite navigiert (nicht über einen Link, sondern z. B. über ein Lesezeichen).

   Wenn dieses Verhalten nicht Ihren Anforderungen entspricht, führen Sie einen der folgenden Schritte aus:

   * Übergeben Sie [Mbox-Parameter](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) , die für Targeting-Zwecke verwendet [!DNL Target] werden sollen.
   * Verwenden Sie eine [A/B-Testaktivität](/help/c-activities/t-test-ab/test-ab.md) anstelle einer Einstiegsseitenaktivität. A/B-Test-Aktivitäten wechseln nicht zwischen Erlebnissen für denselben Besucher.
   * Verwenden Sie stattdessen ein [Besucherprofil](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) .

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392?captions=ger)
