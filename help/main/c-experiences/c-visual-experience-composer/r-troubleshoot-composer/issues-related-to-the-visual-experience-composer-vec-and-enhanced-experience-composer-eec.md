---
keywords: Auf die Zulassungsliste setzen Targeting;Visual Experience Composer;Whitelist;weiße Liste;Zulassungsliste;Enhanced Visual Experience Composer;VEC;Fehlerbehebung in Visual Experience Composer;Fehlerbehebung;EEC;Enhanced Experience Composer;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme beheben können, die unter bestimmten Bedingungen manchmal  [!DNL Target]  Adobe-Visual Experience Composer (VEC) und Enhanced Experience Composer (EEC) auftreten.
title: Wie behebe ich Probleme mit Visual Experience Composer und Enhanced Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 46%

---

# Fehlerbehebung bei Problemen im Zusammenhang mit der [!UICONTROL Visual Experience Composer] und der [!UICONTROL Enhanced Experience Composer]

Anzeigeprobleme und andere Probleme treten manchmal unter bestimmten Bedingungen im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) und im [!UICONTROL Enhanced Experience Composer] (EEC) auf.

## Wie wirken sich die SameSite-Cookie-Richtlinien von Google Chrome auf VEC und EEC aus? {#samesite}

Beachten Sie die Änderungen, die sich auf VEC und EEC auswirken, wenn Sie die folgenden Chrome-Versionen verwenden:

>[!NOTE]
>
>Die folgende Änderung wirkt sich auf alle drei unten beschriebenen Aktualisierungen aus:
>
> * Kann *nicht* VEC verwenden, ohne dass die VEC Helper-Erweiterung für kennwortgeschützte Seiten Ihrer Sites installiert und aktiviert ist. Ihre Site-Anmelde-Cookies werden als Drittanbieter-Cookies betrachtet und werden nicht mit Anmeldeanfragen innerhalb des VEC-Editors im Durchsuchen-Modus gesendet. Die einzige Ausnahme besteht, wenn für die Anmelde-Cookies Ihrer Site bereits die Attribute `SameSite=None` und `Secure` festgelegt sind.

**Chrome 94 (21. September 2021)**: Mit den für die Version Chrome 94 (21. September 2021) geplanten Änderungen wirkt sich die folgende Änderung auf alle Benutzenden mit Browser-Versionen von Chrome 94 oder höher aus:

* Das Befehlszeilen-Flag `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wird entfernt.

**Chrome 91 (25. Mai 2021)**: Mit den Änderungen, die für die Version Chrome 91 (25. Mai 2021) implementiert wurden, wirkt sich die folgende Änderung auf alle Benutzenden mit Browser-Versionen von Chrome 91 oder höher aus:

* Die Flags `#same-site-by-default-cookies` und `#cookies-without-same-site-must-be-secure` wurden aus `chrome://flags` entfernt. Dieses Verhalten ist jetzt standardmäßig aktiviert.

**Chrome 80 (August 2020)**: Mit den Änderungen, die im August 2020 implementiert wurden, haben alle Benutzenden Browser-Versionen von Chrome 80 oder höher:

* Kann *nicht* beim Bearbeiten einer Aktivität [!DNL Target] Bibliotheken herunterladen (wenn diese nicht bereits auf der Website vorhanden sind). Dies liegt daran, dass der Download-Aufruf von der Kunden-Domain an eine gesicherte [!DNL Adobe]-Domain erfolgt und als nicht authentifiziert zurückgewiesen wird.
* Der EEC wird *nicht* für alle Benutzer funktionieren, da er nicht das SameSite-Attribut für Cookies in `adobemc.com domain` festlegen kann. Ohne dieses Attribut lehnt der Browser diese Cookies ab, was dazu führt, dass der EEC fehlschlägt.

### Bestimmen, welche Cookies blockiert werden

Um festzustellen, welche Cookies aufgrund der SameSite-Cookie-Durchsetzungsrichtlinien blockiert werden, verwenden Sie die Entwickler-Tools in Chrome.

1. Um auf die Entwickler-Tools zuzugreifen, während Sie den VEC in Chrome anzeigen, klicken Sie auf das **[!UICONTROL ellipsis]** oben rechts in Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]**.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Network]** und suchen Sie nach blockierten Cookies.

   >[!NOTE]
   >
   >Aktivieren Sie das Kontrollkästchen **[!UICONTROL Has blocked cookies]** , um das Auffinden blockierter Cookies zu vereinfachen.

   Die folgende Abbildung zeigt ein blockiertes Cookie:

   ![Entwickler-Tools > Registerkarte „Netzwerk“ mit einem blockierten Cookie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### [!DNL Adobe Target] VEC Helper-Erweiterung

Ab Version 0.7.1 fügt die [!DNL Adobe Target] VEC Helper-Browser-Erweiterung die `SameSite=None`- und `Secure`-Attribute allen Cookies in Antworten hinzu, die von innerhalb des VEC bearbeiteten Web-Seiten stammen, wenn der Umschalter „Cookies“ in der Erweiterungs-Benutzeroberfläche aktiviert ist:

![Adobe Target VEC Helper-Erweiterung - UIAdobe Target VEC Helper-Erweiterung - Benutzeroberfläche](assets/cookies-vec-helper.png)

### Alternativen und Problemumgehungen

Verwenden Sie eine der folgenden Optionen, um sicherzustellen, dass VEC und EEC weiterhin wie erwartet funktionieren:

* Laden Sie die aktualisierte VEC Helper[Erweiterung herunter und verwenden Sie sie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en).
* Verwenden Sie den Mozilla Firefox-Browser. Firefox setzt diese Richtlinie noch nicht durch.
* Verwenden Sie die folgenden Flags, um Google Chrome bis zum 21. September 2021 von der Befehlszeile aus auszuführen. Nach dem 21. September funktionieren Funktionen, die Cookies erfordern, in VEC nicht mehr, z. B. Popups zur Anmeldung oder zur Cookie-Zustimmung. Wenn Sie auf Chrome 94 aktualisieren, müssen Sie manuell Cookies mit `SameSite=none` und `Secure` auf Ihren Websites generieren.

  ```
  --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
  ```

## Unterstützt [!DNL Target] iFrames mit mehreren Ebenen?

[!DNL Target] unterstützt keine iFrames mit mehreren Ebenen. Wenn Ihre Website einen iframe lädt, der einen untergeordneten iframe hat, interagiert at.js nur mit dem übergeordneten iframe. [!DNL Target] Bibliotheken interagieren nicht mit dem untergeordneten iframe.

Als Behelfslösung können Sie im Erlebnis eine Seite mit der URL des untergeordneten iFrame hinzufügen.

## Wenn ich versuche, eine Seite zu bearbeiten, sehe ich lediglich ein Netz anstelle meiner Seite. (VEC und EEC)   {#section_313001039F79446DB28C70D932AF5F58}

Dies kann vorkommen, wenn die URL ein #-Zeichen enthält. Um das Problem zu beheben, wechseln Sie im Visual Experience Composer in den Durchsuchen-Modus und anschließend wieder in den Erstellen-Modus. Das Netz sollte verschwinden und die Seite sollte angezeigt werden.

## CSP-Header (Content Security Policy) blockieren die [!DNL Target] auf meiner Website. (VEC und EEC)   {#section_89A30C7A213D43BFA0822E66B482B803}

Wenn die CSP-Header Ihrer Website Target-Bibliotheken blockieren und die Website anschließend geladen wird, die Bearbeitung aber nicht möglich ist, stellen Sie sicher, dass die Target-Bibliotheken nicht blockiert werden.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie auch die [Adobe Target VEC Helper-Browsererweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) für Google Chrome verwenden.

![cps_headers-Bild](assets/cps_headers.png)

Als Problemumgehung können Sie eine Requestly-Regel zum Entfernen von CSP-Headern konfigurieren, wie unten dargestellt:

![cps_headers_2 Bild](assets/cps_headers_2.png)

Sie können eine ähnliche Requestly-Regel für beliebige Header konfigurieren, durch die eine Ressource im VEC nicht geladen wird.

Gehen Sie bei Requestly wie folgt vor, wenn Sie Header entfernen müssen:

* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.

## Der VEC oder EEC funktioniert scheinbar nicht oder wird beim erneuten Bearbeiten einer gespeicherten Aktivität nicht initialisiert. (VEC und EEC)   {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Wenn die Website nach Definition des Erlebnisses außerhalb von Visual Experience Composer geändert wurde, sind die Selektoren, auf denen zuvor Aktionen durchgeführt wurden, nicht auffindbar und die Aktivität wird zur erneuten Bearbeitung geöffnet. Die Seite erscheint beschädigt und es werden keine Warnungen eingeblendet.

## Der VEC oder EEC zeigt meine sich drehenden Banner oder anderen Inhalt mit JavaScript nicht an. (VEC und EEC)   {#section_8B5BE6EB050B42D6A14A054724C41330}

Der Visual Experience Composer blockiert standardmäßig JavaScript-Elemente. Sie können mit diesen Elementen arbeiten, wenn Sie JavaScript in den Visual Experience Composer-Einstellungen deaktivieren. Je nach Einrichtung der Site werden einige Elemente möglicherweise weiterhin falsch angezeigt oder sind nicht verfügbar.

## Wenn ich ein Element auf der Seite ändere, ändern sich mehrere Elemente. (VEC und EEC)   {#section_309188ACF34942989BE473F63C5710AF}

Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, sollte eine ID nur einmal auf jeder Seite verwendet werden. Dies ist eine standardmäßige Best Practice für HTML. Weitere Informationen finden Sie unter [Szenarien für die Seitenmodifizierung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Bearbeitung von Erlebnissen für eine Site, die iFrames zerstört, ist nicht möglich. (VEC und EEC)   {#section_9FE266B964314F2EB75604B4D7047200}

Dieses Problem kann durch die Aktivierung des Enhanced Experience Composer behoben werden. Klicken Sie auf **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]** und aktivieren Sie dann das Kontrollkästchen, um Enhanced Experience Composer zu aktivieren. Der Enhanced Experience Composer verwendet ein von Adobe verwaltetes Proxy, um Ihre Seite zur Bearbeitung zu laden. Dieser Proxy ermöglicht die Bearbeitung auf iFrame-Busting-Sites und die Bearbeitung auf Sites und Seiten, auf denen Sie noch keinen Adobe Target-Code hinzugefügt haben. Solange kein Code hinzugefügt wurde, liefern die Aktivitäten nicht an die Site. Einige Websites werden in Enhanced Experience Composer möglicherweise nicht geladen. In diesem Fall können Sie diese Option deaktivieren, um Visual Experience Composer in einem iFrame zu laden. 

>[!NOTE]
>
>Ihre lokal gehosteten Seiten oder Seiten, auf die außerhalb Ihres Netzwerks nicht zugegriffen werden kann, sind für den Adobe-Proxyserver nicht zugänglich und können im EEC nicht geöffnet werden. Diese Seiten können Staging-URLs, Akzeptanztest-URLs (UAT) oder lokal gehostete Seiten enthalten.

## Ich möchte Tests auf Seiten einrichten, für die bisher noch keine Mbox-/Target-Implementierung vorgenommen wurde. (VEC und EEC)   {#section_DE63BCCB5B124E10A71FA579B582A80A}

Siehe oben unter „Ich kann keine Erlebnisse für eine iFrame-zerstörende Website bearbeiten“.

## Auf meiner Seite wird bei „Text/HTML bearbeiten“ oder „Text/HTML ändern“ kein fett und kursiv gedruckter Text angezeigt. Manchmal verschwindet der Text nach der Anwendung dieser Stiländerungen. (VEC und EEC)   {#section_7A71D6DF41084C58B34C18701E8774E5}

Wenn Sie **[!UICONTROL Edit Text/HTML]** in Visual Experience Composer für A/B- oder Erlebnis-Targeting-Aktivitäten oder **[!UICONTROL Change Text/HTML]** für Automated Personalization- oder Multivarianz-Test-Aktivitäten verwenden, um Text fett oder kursiv zu formatieren, werden diese Stile möglicherweise nicht auf der Seite angewendet, oder der Text verschwindet im Visual Experience Composer von der Seite. Dies geschieht, weil die Art und Weise, wie der Rich-Text-Editor diese Stile anwendet, das Website-Markup beeinträchtigen kann.

Wenn Sie dieses Problem angezeigt bekommen, tun Sie Folgendes:

1. Klicken Sie im Rich-Text-Editor auf die Schaltfläche &quot;**[!UICONTROL HTML]**&quot;, um in den Modus zur Bearbeitung des Quell-Codes zu wechseln.
1. Suchen Sie die Stiltextelemente.

   * Für fett gedruckten Text ändern Sie `<strong>`-Elemente zu `<b>`.

   * Für kursiv gedruckten Text ändern Sie `<em>`-Elemente zu `<i>`.

## Bei Aktivitäten mit automatisierter Personalisierung scheint der Bildtausch im VEC oder EEC nicht zu funktionieren. (VEC und EEC)   {#section_88AABFDFE6A3420299B0D508B12A3994}

Das Hinzufügen eines Bildangebots zu einem Pfad erfordert die vollständige Dimension des ursprünglichen Bildplatzes im VEC oder EEC. Bei der Bereitstellung wird das Bild nicht erweitert, sondern wie vorhanden angezeigt, sodass die Bereitstellung nicht beeinträchtigt wird.
