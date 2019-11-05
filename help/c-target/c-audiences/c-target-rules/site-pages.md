---
description: Targeting von Besuchern, die sich auf einer bestimmten Seite befinden oder die einen bestimmten Mbox-Parameter aufweisen.
keywords: Seiten der Site; Seiten der Target-Site; Targeting; aktuelle Seite; Targeting der aktuellen Seite; vorherige Seite; Targeting der vorherigen Seite; Zielseite; Targeting-Zielseite; mbox; Ziel-mbox
seo-description: Sie können mit Adobe Target auf Besucher abzielen, die sich auf einer bestimmten Seite befinden oder einen bestimmten mbox-Parameter haben.
seo-title: Site-Seiten in Adobe Target
solution: Target
title: Seiten der Site
topic: Standard
uuid: 1cf9fa94-dbec-4719-9a0a-79c1eb91a233
translation-type: tm+mt
source-git-commit: a1732632ad85a0f3742177663ee7d9a617098ff5

---


# Seiten der Site{#site-pages}

Sie können auf Besucher abzielen, die sich auf einer bestimmten Seite befinden oder einen bestimmten mbox-Parameter haben.

>[!NOTE]
>
>Die Zielgruppen-Website-Typen und Vergleichsoperatoren stimmen nun mit den Typen und Vergleichsoperatoren in Target Classic überein. Sie können Website-Zielgruppen auch mit einem eigenen „benutzerdefinierten Abfrageparameter“ oder „benutzerdefinierten Header“ erstellen.

1. Klicken Sie auf der [!DNL Target]-Benutzeroberfläche auf **[!UICONTROL Zielgruppen]** &gt; **[!UICONTROL Zielgruppe erstellen]**.
1. Nennen Sie die Zielgruppe.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]** &gt; **[!UICONTROL Seiten der Site]**.

   ![Seiten der Site als Zielgruppe](assets/target_site_pages.png)

1. Klicken Sie auf **[!UICONTROL Auswählen]** und wählen Sie anschließend eine der folgenden Optionen aus:

   * **Aktuelle Seite:** Die Seite, die der Benutzer gegenwärtig aufruft und die eine Mbox in der Aktivität enthält. Wenn Sie ein Ziel auf Aktivitätsebene auswählen, könnte dies eine Seite mit einer Mbox sein, die Sie verwenden, um Eintragsbedingungen zu definieren, oder eine Seite, die Inhalte anzeigt. Wenn Sie ein Ziel nach Erlebnis auswählen, ist die aktuelle Seite die Seite, auf der sich die Display-Mbox befindet. Für Erfolgsmetriken oder Konversions-Targeting ist es die Seite, auf der sich diese Mboxes befinden.
   * **Vorherige Seite:** Die Seite, die der Benutzer vor dem Anklicken der aktuellen Seite aufgerufen hat. (Der Benutzer muss von der letzten Seite auf die aktuelle Seite klicken, damit die Seite nachverfolgt wird. Die vorherige Seite wird nicht verfolgt, wenn der Benutzer eine neue URL in den Browser eingibt.) Der tatsächliche Inhalt auf dieser Seite hängt vom Design Ihrer Site ab. Wenn beispielsweise auf der aktuellen Seite Informationen zu einem bestimmten Produkt angezeigt werden, kann es sich bei der letzten Seite um eine Kategorieseite, auf der der Benutzer ein bestimmtes Element ausgewählt hat (zum Beispiel eine Seite, auf mehrere Kameras eines bestimmten Typs angezeigt werden) oder eine Homepage mit Verweis auf die Ausstiegsseite handeln.
   * **Landingpage:** Die Landingpage ist die Seite, die Besuchern beim Zugriff auf Ihre Site zuerst angezeigt wird. Wenn der Besucher z. B. auf einen Link in Google klickt, der zu einer Kategorieseite führt, ist die Kategorieseite die Landingpage. Wenn der Link zu Ihrer Homepage führt, ist die Homepage die Landingpage. Die Landingpage wird während der Benutzersitzung gespeichert. Sie können Ihr Ziel tiefer in die Site richten, je nachdem, welche Seite die Landingpage des Benutzers in dieser Sitzung war.

      >[!NOTE]
      >
      >Das `landing.url`-Objekt wird bei einer Änderung der Subdomäne oder einer direkten URL-Ersetzung zurückgesetzt.

   * **mbox:** Die mbox, die Gegenstand des Targeting ist. Wenn Sie z. B. Bestellungen mit einer Bestellsumme von 100 Euro oder mehr zählen möchten, geben Sie `orderTotal` als Mbox-Parameter mit dem hier angegebenen Targeting weiter.
   * **Domäne:** Die vollständige Domäne der Seite Für das Festlegen einer Domäne wird die Versendung von „contains“ empfohlen. Beispiel: „Domain equals facebook.com“ wird `m.facebook.com` oder `www.facebook.com` nicht akzeptieren. „Domain contains facebook.com“ hingegen erfasst alle Varianten von „facebook.com“.
   * **Abfrage:** Der Inhalt der URL nach dem ersten Fragezeichen (?) 

      `foo.html?e0a72cb2a2c7`

1. (Optional) Klicken Sie auf **[!UICONTROL Regel hinzufügen]** und legen Sie zusätzliche Regeln für die Zielgruppe fest.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Sie können Website-Zielgruppen auch mit einem eigenen „benutzerdefinierten Abfrageparameter“ oder „benutzerdefinierten Header“ erstellen.

Verwenden Sie:

* Abfrageparameter, wenn die vom Benutzer ausgewählte Regel „Aktuelle Seite“, „Landingpage“ oder „Vorherige Seite“ lautet.
* Header, wenn die von einem Benutzer ausgewählte Regel in einem HTTP-Header enthalten ist.

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
