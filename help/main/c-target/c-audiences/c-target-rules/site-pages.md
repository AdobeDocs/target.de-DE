---
keywords: Site-Seiten; Target-Site-Seiten; Targeting; aktuelle Seite; Targeting der aktuellen Seite; vorherige Seite; Targeting der vorherigen Seite; Landingpage; Target-Landingpage; HTTP-Kopfzeile
description: Erfahren Sie, wie Sie Besucher, die sich auf einer bestimmten Seite Ihrer Site befinden, mit [!DNL Adobe Target] als Ziel auswählen.
title: Kann ich ein Targeting von Besuchern auf Basis von Site-Seiten durchführen?
feature: Audiences
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 19%

---

# Seiten der Site

Sie können Besucher mit &quot;[!DNL Adobe Target]&quot;als Ziel auswählen, die auf eine bestimmte Seite auf Ihrer Site zugreifen.

1. Klicken Sie in der [!DNL Target] -Oberfläche auf **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Site Pages]** in den Bereich Audience Builder .

   ![Seiten der Site als Zielgruppe](assets/target_site_pages.png)

1. Klicken Sie auf die Dropdownliste **[!UICONTROL Select]**, wählen Sie eine der folgenden Optionen aus und konfigurieren Sie dann die Regel nach Bedarf.

   Die verfügbaren Optionen und Auswerter in nachfolgenden Dropdown-Listen in der Regel variieren je nach ausgewählter Option. Die folgende Abbildung zeigt die verfügbaren Optionen bei Auswahl von [!UICONTROL Current Page]:

   ![Aktuelle Seite](assets/current-page.png)

   Die folgenden Optionen sind in der ersten Dropdown-Liste verfügbar, wenn Sie [!UICONTROL Select] auswählen.

   * **[!UICONTROL Current Page]:** Die Seite, die der Benutzer anzeigt.

     Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL URL] (Weitere Informationen dazu, wie [!DNL Target] URLs auswertet, finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]

   * **[!UICONTROL Previous Page]:** Die Seite, die der Benutzer vor dem Klicken auf die aktuelle Seite aufgerufen hat. Der Benutzer muss von der vorherigen Seite zur aktuellen Seite klicken, damit die Seite verfolgt werden kann. Die vorherige Seite wird nicht verfolgt, wenn der Benutzer eine neue URL im Browser eingibt. Der tatsächliche Inhalt auf dieser Seite hängt vom Design Ihrer Site ab. Wenn die aktuelle Seite beispielsweise Informationen zu einem bestimmten Produkt anzeigt, kann die vorherige Seite eine Kategorieseite sein, auf der der Besucher das spezifische Element auswählt. Zum Beispiel eine Seite, die mehrere Kameras eines bestimmten Typs anzeigt, oder es kann die Homepage sein, die zur endgültigen Seite führt.

     Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL URL] (Weitere Informationen dazu, wie Target URLs auswertet, finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]

   * **[!UICONTROL Landing Page]:** Die Landingpage ist die erste Seite, die Besucher beim Zugriff auf Ihre Site sehen. Wenn der Besucher z. B. auf einen Link in Google klickt, der zu einer Kategorieseite führt, ist die Kategorieseite die Landingpage. Wenn der Link zu Ihrer Homepage führt, ist die Homepage die Landingpage. Die Landingpage wird während der Benutzersitzung gespeichert. Sie können Ihr Ziel tiefer in die Site richten, je nachdem, welche Seite die Landingpage des Benutzers in dieser Sitzung war.

     Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL URL] (Weitere Informationen dazu, wie Target URLs auswertet, finden Sie unter [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]

     >[!NOTE]
     >
     >Das `landing.url`-Objekt wird bei einer Änderung der Subdomäne oder einer direkten URL-Ersetzung zurückgesetzt.

   * **[!UICONTROL HTTP Header]:** Diese Option bewertet die Informationen im HTTP-Header der [!DNL Target] -Anfrage. Wenn der HTTP-Header beispielsweise Sprachinformationen enthält, können Sie eine Regel erstellen, die die Bedingung `Accept-Language: es` enthält, um Besucher als Ziel auszuwählen, die auf die Seite auf Spanisch zugreifen.

     Die folgenden Optionen stehen in der zweiten Dropdownliste zur Verfügung, wenn Sie diese Option wählen:

      * [!UICONTROL Accept]
      * [!UICONTROL Accept-Charset]
      * [!UICONTROL Accept-Encoding]
      * [!UICONTROL Accept-Language]
      * [!UICONTROL Authorization]
      * [!UICONTROL Cache-Control]
      * [!UICONTROL Connection]
      * [!UICONTROL Content-Length]
      * [!UICONTROL Content-MDS]
      * [!UICONTROL Content-Type]
      * [!UICONTROL Date]
      * [!UICONTROL Expect]
      * [!UICONTROL From]
      * [!UICONTROL Host]
      * [!UICONTROL If-Match]
      * [!UICONTROL If-Modified-Since]
      * [!UICONTROL If-None-Match]
      * [!UICONTROL If-Range]
      * [!UICONTROL If-Unmodified-Since]
      * [!UICONTROL Max-Forwards]
      * [!UICONTROL Pragma]
      * [!UICONTROL Proxy-Authorization]
      * [!UICONTROL Range]
      * [!UICONTROL Referrer]
      * [!UICONTROL TE]
      * [!UICONTROL Upgrade]
      * [!UICONTROL User-Agent]
      * [!UICONTROL Via]
      * [!UICONTROL Warning]

   Wenn Sie [!UICONTROL Current Page], [!UICONTROL Previous Page] oder [!UICONTROL Landing Page] auswählen, sind die Optionen [!UICONTROL Domain] und [!UICONTROL Query] verfügbar. Beachten Sie bei der Auswahl dieser Optionen Folgendes:

   * **Domain:** Die vollständige Domain der Seite Für das Festlegen einer Domain wird die Versendung von „contains“ empfohlen. Beispielsweise akzeptiert &quot;Domain equals facebook.com&quot;nicht `m.facebook.com` oder `www.facebook.com`. &quot;Domain contains facebook.com&quot;akzeptiert alle Varianten von facebook.com.
   * **Abfrage:** Der Inhalt der URL nach dem ersten Fragezeichen (?).

     `foo.html?e0a72cb2a2c7`

1. (Optional) Richten Sie zusätzliche Regeln für die Zielgruppe ein.
1. Klicken Sie auf **[!UICONTROL Done]**.

Sie können Website-Zielgruppen auch mit einem eigenen „benutzerdefinierten Abfrageparameter“ oder „benutzerdefinierten Header“ erstellen.

Verwenden Sie:

* Abfrageparameter, wenn die vom Benutzer ausgewählte Regel [!UICONTROL Current Page], [!UICONTROL Landing Page] oder [!UICONTROL Previous Page] ist
* Kopfzeile, wenn die vom Benutzer ausgewählte Regel eine HTTP-Kopfzeile ist

## Fehlerbehebung {#ts}

* Damit Zielgruppen von Landingpages ordnungsgemäß funktionieren, muss für Anfragen der Parameter `mboxReferrer` festgelegt sein (für die Bereitstellungs-API der Parameter `context.address.referringUrl` ), den die JavaScript-Bibliothek at.js mithilfe des Attributs `document.referrer` von der Seite nimmt. Dieses Attribut `HTMLDocument` gibt den URI der Seite zurück, von der der Benutzer navigiert hat. Der Wert dieses Attributs ist eine leere Zeichenfolge, wenn der Benutzer direkt zur Seite navigiert (nicht über einen Link, sondern z. B. über ein Lesezeichen).

  Wenn dieses Verhalten nicht Ihren Anforderungen entspricht, sollten Sie eine der folgenden Aktionen durchführen:

   * Übergeben Sie [Mbox-Parameter](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html?lang=de){target=_blank} an [!DNL Target] , um sie für Targeting-Zwecke zu verwenden.
   * Verwenden Sie eine [A/B-Test-Aktivität](/help/main/c-activities/t-test-ab/test-ab.md) anstelle einer Landingpage-Aktivität. A/B-Test-Aktivitäten wechseln nicht zwischen Erlebnissen für denselben Besucher.
   * Verwenden Sie stattdessen ein [Besucherprofil](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md).

* Bei Verwendung von Auswertern für Zeichenfolgen, die Kommas enthalten, werden diese Zeichenfolgen als Array von Werten ausgewertet, in denen jeder durch Kommas getrennte Wert ausgewertet wird. Wenn Sie beispielsweise den Wert für eine Kopfzeile haben: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7`, ist er für Bedingungen wie die folgenden qualifiziert:
   * beginnt mit zh,
   * beginnt mit en,
   * endet mit 0,7,
   * endet mit 0,8.

## Schulungsvideo: Erstellen von Zielgruppen

Dieses Video enthält Informationen zur Verwendung von Zielgruppenkategorien.

* Erstellen von Zielgruppen
* Festlegen von Zielgruppenkategorien

>[!VIDEO](https://video.tv.adobe.com/v/17392)
