---
keywords: Site-Seiten; Target-Site-Seiten; Targeting; aktuelle Seite; Targeting der aktuellen Seite; vorherige Seite; Targeting der vorherigen Seite; Landingpage; Target-Landingpage; HTTP-Kopfzeile
description: Erfahren Sie, wie Sie Besucher mit [!DNL Adobe Target] die sich auf einer bestimmten Seite Ihrer Site befinden.
title: Kann ich ein Targeting von Besuchern auf Basis von Site-Seiten durchführen?
feature: Audiences
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 26%

---

# Seiten der Site

Sie können Besucher mithilfe von [!DNL Adobe Target] die auf eine bestimmte Seite Ihrer Site zugreifen.

1. Klicken Sie in der [!DNL Target]-Oberfläche auf **[!UICONTROL Zielgruppe]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Drag &amp; Drop **[!UICONTROL Seiten der Site]** in den Audience Builder-Bereich.

   ![Seiten der Site als Zielgruppe](assets/target_site_pages.png)

1. Klicken Sie auf **[!UICONTROL Auswählen]** eine der folgenden Optionen aus und konfigurieren Sie dann die Regel nach Bedarf.

   Die verfügbaren Optionen und Auswerter in nachfolgenden Dropdownlisten in der Regel variieren je nach ausgewählter Option. Die folgende Abbildung zeigt die verfügbaren Optionen bei Auswahl von [!UICONTROL Aktuelle Seite]:

   ![Aktuelle Seite](assets/current-page.png)

   Die folgenden Optionen stehen in der ersten Dropdown-Liste zur Verfügung, wenn Sie [!UICONTROL Auswählen].

   * **[!UICONTROL Aktuelle Seite]:** Die Seite, die der Benutzer anzeigt.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL URL] (Weitere Informationen zum [!DNL Target] bewertet URLs, siehe [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).
      * [!UICONTROL Domain]
      * [!UICONTROL Abfrage]
      * [!UICONTROL Subdomäne]
      * [!UICONTROL Domäne auf oberster Ebene]
      * [!UICONTROL Pfad]
      * [!UICONTROL Hash (#)-Fragment]
   * **[!UICONTROL Vorherige Seite]:** Die Seite, die der Benutzer vor dem Klicken auf die aktuelle Seite aufgerufen hat. Der Benutzer muss von der vorherigen Seite zur aktuellen Seite klicken, damit die Seite verfolgt werden kann. Die vorherige Seite wird nicht verfolgt, wenn der Benutzer eine neue URL in den Browser eingibt. Der tatsächliche Inhalt auf dieser Seite hängt vom Design Ihrer Site ab. Wenn die aktuelle Seite beispielsweise Informationen zu einem bestimmten Produkt anzeigt, kann die vorherige Seite eine Kategorieseite sein, auf der der Besucher das spezifische Element auswählt. Zum Beispiel eine Seite, die mehrere Kameras eines bestimmten Typs anzeigt, oder es kann die Homepage sein, die zur endgültigen Seite führt.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL URL] (Weitere Informationen zur Bewertung von URLs durch Target finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).
      * [!UICONTROL Domäne]
      * [!UICONTROL Abfrage]
      * [!UICONTROL Subdomäne]
      * [!UICONTROL Domäne auf oberster Ebene]
      * [!UICONTROL Pfad]
   * **Einstiegsseite:** Die Einstiegsseite ist die Seite, die Besuchern beim Zugriff auf Ihre Site zuerst angezeigt wird. Wenn der Besucher z. B. auf einen Link in Google klickt, der zu einer Kategorieseite führt, ist die Kategorieseite die Landingpage. Wenn der Link zu Ihrer Homepage führt, ist die Homepage die Landingpage. Die Landingpage wird während der Benutzersitzung gespeichert. Sie können Ihr Ziel tiefer in die Site richten, je nachdem, welche Seite die Landingpage des Benutzers in dieser Sitzung war.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL URL] (Weitere Informationen zur Bewertung von URLs durch Target finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).
      * [!UICONTROL Domäne]
      * [!UICONTROL Abfrage]
      * [!UICONTROL Subdomäne]
      * [!UICONTROL Domäne auf oberster Ebene]
      * [!UICONTROL Pfad]
      * [!UICONTROL Hash (#)-Fragment]

      >[!NOTE]
      >
      >Das `landing.url`-Objekt wird bei einer Änderung der Subdomäne oder einer direkten URL-Ersetzung zurückgesetzt.

   * **[!UICONTROL HTTP-Header]:** Diese Option bewertet die Informationen im HTTP-Header der [!DNL Target] -Anfrage. Wenn der HTTP-Header beispielsweise Sprachinformationen enthält, können Sie eine Regel erstellen, die die Variable `Accept-Language: es` -Bedingung, um Besucher anzusprechen, die auf die Seite in spanischer Sprache zugreifen.

      Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL Accept]
      * [!UICONTROL Accept-Charset]
      * [!UICONTROL Accept-Encoding]
      * [!UICONTROL Accept-Language]
      * [!UICONTROL Genehmigung]
      * [!UICONTROL Cache-Control]
      * [!UICONTROL Verbindung]
      * [!UICONTROL Content-Length]
      * [!UICONTROL Content-MDS]
      * [!UICONTROL Content-Type]
      * [!UICONTROL Date]
      * [!UICONTROL Expect]
      * [!UICONTROL Von]
      * [!UICONTROL Host]
      * [!UICONTROL If-Match]
      * [!UICONTROL If-Modified-Since]
      * [!UICONTROL If-None-Match]
      * [!UICONTROL If-Range]
      * [!UICONTROL If-Unmodified-Since]
      * [!UICONTROL Max-Forwards]
      * [!UICONTROL Pragma]
      * [!UICONTROL Proxy-Authorization]
      * [!UICONTROL Bereich]
      * [!UICONTROL Verweisende Stelle]
      * [!UICONTROL TE]
      * [!UICONTROL Aktualisierung]
      * [!UICONTROL User-Agent]
      * [!UICONTROL Via]
      * [!UICONTROL Warnung]

   Wenn Sie [!UICONTROL Aktuelle Seite], [!UICONTROL Vorherige Seite]oder [!UICONTROL Landingpage], die [!UICONTROL Domäne] und [!UICONTROL Abfrage] -Optionen verfügbar sind. Beachten Sie bei der Auswahl dieser Optionen Folgendes:

   * **Domain:** Die vollständige Domain der Seite Für das Festlegen einer Domain wird die Versendung von „contains“ empfohlen. Beispielsweise akzeptiert &quot;Domain equals facebook.com&quot;nicht `m.facebook.com` oder `www.facebook.com`. &quot;Domain contains facebook.com&quot;akzeptiert alle Varianten von facebook.com.
   * **Abfrage:** Der Inhalt der URL nach dem ersten Fragezeichen (?) 

      `foo.html?e0a72cb2a2c7`





1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

Sie können Website-Zielgruppen auch mit einem eigenen „benutzerdefinierten Abfrageparameter“ oder „benutzerdefinierten Header“ erstellen.

Verwenden Sie:

* Abfrageparameter, wenn die vom Benutzer ausgewählte Regel [!UICONTROL Aktuelle Seite], [!UICONTROL Landingpage]oder [!UICONTROL Vorherige Seite]
* Kopfzeile, wenn die vom Benutzer ausgewählte Regel eine HTTP-Kopfzeile ist

## Fehlerbehebung {#ts}

* Damit die Zielgruppen der Landingpage ordnungsgemäß funktionieren, müssen die Anforderungen die Variable `mboxReferrer` -Parameter festgelegt ist (für die Bereitstellungs-API ist das `context.address.referringUrl` -Parameter), den die at.js-JavaScript-Bibliothek von der Seite mit der `document.referrer` -Attribut. Diese `HTMLDocument` gibt den URI der Seite zurück, von der der Benutzer navigiert hat. Der Wert dieses Attributs ist eine leere Zeichenfolge, wenn der Benutzer direkt zur Seite navigiert (nicht über einen Link, sondern z. B. über ein Lesezeichen).

   Wenn dieses Verhalten nicht Ihren Anforderungen entspricht, sollten Sie eine der folgenden Aktionen durchführen:

   * Pass [Mbox-Parameter](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/){target=_blank} bis [!DNL Target] für Targeting-Zwecke verwendet werden.
   * Verwenden Sie eine [A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/test-ab.md) anstatt einer Landingpage-Aktivität. A/B-Test-Aktivitäten wechseln nicht zwischen Erlebnissen für denselben Besucher.
   * Verwenden Sie eine [Besucherprofil](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) anstatt.

* Bei Verwendung von Auswertern für Zeichenfolgen, die Kommas enthalten, werden diese Zeichenfolgen als Array von Werten ausgewertet, in denen jeder durch Kommas getrennte Wert ausgewertet wird. Wenn Sie beispielsweise den Wert für eine Kopfzeile haben: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` Sie ist für Bedingungen wie die folgenden qualifiziert:
   * beginnt mit zh,
   * beginnt mit en,
   * endet mit 0,7,
   * endet mit 0,8.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
