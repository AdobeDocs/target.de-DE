---
keywords: Targeting;visual experience composer;whitelist;white list;allowlist;allow list;enhanced visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;eec;enhanced experience composer;tls;tls 1.2
description: Im Visual Experience Composer (VEC) und Enhanced Experience Composer (EEC) treten unter bestimmten Umständen mitunter Anzeigeprobleme auf.
title: Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer
feature: vec
uuid: 93f646d9-fcbc-43f0-9f84-0ce8e486ff7f
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1370'
ht-degree: 68%

---


# Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer{#troubleshooting-issues-related-to-the-visual-experience-composer-and-enhanced-experience-composer}

Anzeigeprobleme und andere Probleme treten manchmal im Visual Experience Composer (VEC) und im Enhanced Experience Composer (EEC) unter bestimmten Bedingungen auf.

## Wie wirken sich die kürzlich angekündigten Google Chrome SameSite-Cookie-Durchsetzungsrichtlinien auf VEC und EEC aus? {#samesite}

Mit den neuesten Änderungen (August 2020) haben alle Benutzer mit Chrome 80+-Browser-Versionen folgende Vorteile:

* Wird *nicht* in der Lage sein, VEC (mit oder ohne VEC Helper Extension installiert und aktiviert) in kennwortgeschützten Seiten ihrer Sites zu verwenden. Der Grund dafür ist, dass ihre Site-Login-Cookies als Drittanbieter-Cookie betrachtet werden und nicht mit der Anmeldeanforderung gesendet werden. Die einzige Ausnahme besteht darin, dass der SameSite-Anmeldecookie des Kunden bereits über den Parameter SameSite auf &quot;none&quot;gesetzt ist.
* Wird *nicht* in der Lage sein, [!DNL Target] Bibliotheken während der Bearbeitung einer Aktivität herunterzuladen (wenn diese nicht bereits auf der Site vorhanden sind). Dies liegt daran, dass der Download-Aufruf von der Kundendomäne zu einer gesicherten Adobe-Domäne erfolgt und als nicht authentifiziert abgelehnt wird.
* Die EWG wird *nicht* für alle Benutzer funktionieren, da sie nicht in der Lage ist, das Attribut SameSite für Cookies einzustellen `adobemc.com domain`. Ohne dieses Attribut lehnt der Browser diese Cookies ab, wodurch die EWG fehlschlägt.

Adobe hat eine aktualisierte VEC Helper-Erweiterung an den Google Chrome Store übermittelt. Diese Erweiterung überschreibt bei Bedarf die Cookie-Attribute, um das `SameSite="none"` Attribut festzulegen. Die [aktualisierte Erweiterung finden Sie hier](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en). Weitere Informationen zum Installieren und Verwenden der VEC Helper Extension finden Sie unter [Visual Experience Composer Helper Extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

Für Ihre eigenen Site-Cookies müssen Sie die Cookies anhand des Namens angeben. Schalten Sie den Schieberegler [!UICONTROL Cookie] auf die Position on um und geben Sie dann das Cookie anhand des Namens und der Cookie-Domäne an. Der Cookie-Name ist &quot;mbox&quot;und die Cookie-Domäne ist die zweite und oberste Ebene der Domänen, von denen Sie die mbox beliefern. Da die Belieferung von der Domäne Ihres Unternehmens stattfindet, handelt es sich um ein Erstanbieter-Cookie. Beispiel: `mycompany.com`. Weitere Informationen finden Sie unter [Adobe Target-Cookies](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-target.html) im *Experience Cloud-Interface-Benutzerhandbuch*.

![Cookies in der VEC Helper Extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

### Alternativen und Problemumgehungen

Verwenden Sie eine der folgenden Optionen, um sicherzustellen, dass VEC und EEC wie erwartet funktionieren:

* Laden Sie die aktualisierte [VEC Helper-Erweiterung herunter und verwenden Sie sie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en).
* Verwenden Sie den Mozilla Firefox-Browser. Firefox erzwingt diese Richtlinie noch nicht.
* Verwenden Sie weiterhin Chrome, setzen Sie das `chrome://flags/#same-site-by-default-cookies` Flag jedoch auf &quot;Deaktiviert&quot;.

   >[!NOTE]
   >
   >Dies reicht *nicht* aus, wenn für Cookies bereits das Attribut SameSite auf &quot;Lax&quot;oder &quot;Strict&quot;vom Server eingestellt ist.

## Unterstützt Target iFrames mit mehreren Ebenen?

Nein, Target unterstützt keine iFrames mit mehreren Ebenen. Wenn Ihre Website einen iFrame mit einem untergeordneten iFrame lädt, interagieren Target-Bibliotheken (at.js und mbox.js) nur mit dem übergeordneten iFrame. Target-Bibliotheken interagieren nicht mit dem untergeordneten iFrame.

Als Behelfslösung können Sie im Erlebnis eine Seite mit der URL des untergeordneten iFrame hinzufügen.

## Wenn ich versuche, eine Seite zu bearbeiten, sehe ich lediglich ein Netz anstelle meiner Seite. (VEC und EEC) {#section_313001039F79446DB28C70D932AF5F58}

Das kann vorkommen, wenn die URL ein #-Zeichen enthält. Um das Problem zu beheben, wechseln Sie im Visual Experience Composer in den Durchsuchen-Modus und anschließend wieder in den Erstellen-Modus. Das Netz sollte verschwinden und die Seite sollte angezeigt werden.

## Content Security Policy (CSP)-Header blockieren die Target-Bibliotheken auf meiner Website. (VEC und EEC) {#section_89A30C7A213D43BFA0822E66B482B803}

Wenn die CSP-Header Ihrer Website Target-Bibliotheken blockieren und die Website anschließend geladen wird, die Bearbeitung aber nicht möglich ist, stellen Sie sicher, dass die Target-Bibliotheken nicht blockiert werden.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie auch die [Adobe Target VEC Helper-Browsererweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) für Google Chrome verwenden.

![](assets/cps_headers.png)

Als Problemumgehung können Sie eine Requestly-Regel zum Entfernen von CSP-Headern konfigurieren, wie unten dargestellt:

![](assets/cps_headers_2.png)

Sie können eine ähnliche Requestly-Regel für beliebige Header konfigurieren, durch die eine Ressource im VEC nicht geladen wird.

Gehen Sie bei Requestly wie folgt vor, wenn Sie Header entfernen müssen:

* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.

## Der VEC oder EEC funktioniert scheinbar nicht oder wird beim erneuten Bearbeiten einer gespeicherten Aktivität nicht initialisiert. (VEC und EEC) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Wenn die Website nach Definition des Erlebnisses außerhalb von Visual Experience Composer geändert wurde, sind die Selektoren, auf denen zuvor Aktionen durchgeführt wurden, nicht auffindbar und die Aktivität wird zur erneuten Bearbeitung geöffnet. Die Seite erscheint beschädigt und es werden keine Warnungen eingeblendet.

## Der VEC oder EEC zeigt meine sich drehenden Banner oder anderen Inhalt mit JavaScript nicht an. (VEC und EEC) {#section_8B5BE6EB050B42D6A14A054724C41330}

Der Visual Experience Composer blockiert standardmäßig JavaScript-Elemente. Sie können mit diesen Elementen arbeiten, wenn Sie JavaScript in den Visual Experience Composer-Einstellungen deaktivieren. Je nach Einrichtung der Site werden einige Elemente möglicherweise weiterhin falsch angezeigt oder sind nicht verfügbar.

## Meine gehostete target.js-Datei wird bei folgenden Neuladungen der Seite nicht geladen. (VEC und EEC) {#section_87F6418C2CD142A7B4D1E7037935F81F}

Dieser Fehler tritt bei Kunden auf, die mit einer mbox.js-Version arbeiten, die älter ist als Version 57 (d. h. Version 56 oder älter).

Wir empfehlen allen VEC-Benutzern ein Upgrade auf die [neueste Version von mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A), zumindest aber auf Version 57. Sie sollten auch erwägen, [auf at.js umzustellen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).

## Wenn ich ein Element auf der Seite ändere, ändern sich mehrere Elemente. (VEC und EEC) {#section_309188ACF34942989BE473F63C5710AF}

Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, sollte eine ID nur einmal auf jeder Seite verwendet werden. Dies ist eine übliche Best Practice für HTML. Weitere Informationen finden Sie unter  [Szenarien für die Seitenmodifizierung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Bearbeitung von Erlebnissen für eine Site, die iFrames zerstört, ist nicht möglich. (VEC und EEC) {#section_9FE266B964314F2EB75604B4D7047200}

Dieses Problem kann durch die Aktivierung des Enhanced Experience Composer behoben werden. Click **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]**, then select the check box that enables the Enhanced Experience Composer. Der Enhanced Experience Composer verwendet ein von Adobe verwaltetes Proxy, um Ihre Seite zur Bearbeitung zu laden. Dies ermöglicht Ihnen die Bearbeitung von Sites, die iFrames zerstören, sowie die Bearbeitung auf Sites und Seiten, auf denen Sie noch keinen Adobe Target-Code hinzugefügt haben. Solange kein Code hinzugefügt wurde, liefern die Aktivitäten nicht an die Site. Einige Websites werden in Enhanced Experience Composer möglicherweise nicht geladen. In diesem Fall können Sie diese Option deaktivieren, um Visual Experience Composer in einem iFrame zu laden.  []

>[!NOTE]
>
>Ihre lokal gehosteten Seiten oder Seiten, auf die außerhalb Ihres Netzwerks nicht zugegriffen werden kann, sind für den Adobe-Proxyserver nicht zugänglich und können im EEC nicht geöffnet werden. Diese Seiten können Staging-URLs, Akzeptanztest-URLs (UAT) oder lokal gehostete Seiten enthalten.

## Ich möchte Tests auf Seiten einrichten, für die bisher noch keine Mbox-/Target-Implementierung vorgenommen wurde. (VEC und EEC) {#section_DE63BCCB5B124E10A71FA579B582A80A}

Siehe oben unter „Ich kann keine Erlebnisse für eine iFrame-zerstörende Website bearbeiten“.

## Auf meiner Seite wird bei „Text/HTML bearbeiten“ oder „Text/HTML ändern“ kein fett und kursiv gedruckter Text angezeigt. Manchmal verschwindet der Text nach der Anwendung dieser Stiländerungen. (VEC und EEC) {#section_7A71D6DF41084C58B34C18701E8774E5}

Wenn Sie **[!UICONTROL Text/HTML bearbeiten]** im Visual Experience Composer für A/B- oder Erlebniszielaktivitäten oder **[!UICONTROL Text/HTML ändern]** für automatisierte Personalisierungs- oder Multivarianztest-Aktivitäten verwenden, um den Text fett oder kursiv zu formatieren, werden diese Stile möglicherweise nicht auf der Seite übernommen, oder der Text wird auf der Seite im Visual Experience Composer ausgeblendet. Dies beruht darauf, dass die Art und Weise, wie der Rich-Text-Editor diese Stile anwendet, möglicherweise mit dem Markup der Website kollidiert.

Wenn Sie dieses Problem angezeigt bekommen, tun Sie Folgendes:

1. Klicken Sie im Richt-Text-Editor auf die Schaltfläche **[!UICONTROL HTML]**, um in den Quellbearbeitungsmodus zu wechseln.
1. Suchen Sie die Stiltextelemente.

   * Für fett gedruckten Text ändern Sie `<strong>`-Elemente zu `<b>`.

   * Für kursiv gedruckten Text ändern Sie `<em>`-Elemente zu `<i>`.

## Bei Aktivitäten mit automatisierter Personalisierung scheint der Bildtausch im VEC oder EEC nicht zu funktionieren. (VEC und EEC) {#section_88AABFDFE6A3420299B0D508B12A3994}

Das Hinzufügen eines Bildangebots zu einem Pfad erfordert die vollständige Dimension des ursprünglichen Bildplatzes im VEC oder EEC. Bei der Bereitstellung wird das Bild nicht erweitert, sondern wie vorhanden angezeigt, sodass die Bereitstellung nicht beeinträchtigt wird.
