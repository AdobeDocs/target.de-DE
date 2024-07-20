---
keywords: Targeting;Visual Experience Composer;Whitelist;White List;Zulassungsliste;Zulassungsliste;Enhanced Visual Experience Composer;VEC;Fehlerbehebung Visual Experience Composer;Fehlerbehebung;EEC;Enhanced Experience Composer;TLS;TLS 1.2
description: Erfahren Sie, wie Sie unter bestimmten Bedingungen Probleme beheben können, die manchmal im Adobe [!DNL Target] Visual Experience Composer (VEC) und im Enhanced Experience Composer (EEC) auftreten.
title: Wie kann ich Probleme im Zusammenhang mit Visual Experience Composer und Enhanced Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 46%

---

# Beheben von Problemen im Zusammenhang mit dem [!UICONTROL Visual Experience Composer] und dem [!UICONTROL Enhanced Experience Composer]

Unter bestimmten Umständen treten im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) und im [!UICONTROL Enhanced Experience Composer] (EEC) manchmal Anzeigeprobleme und andere Probleme auf.

## Wie wirken sich die SameSite-Cookie-Richtlinien von Google Chrome auf VEC und EEC aus? {#samesite}

Beachten Sie die Änderungen, die sich auf VEC und EEC auswirken, wenn Sie die folgenden Chrome-Versionen verwenden:

>[!NOTE]
>
>Die folgende Änderung betrifft alle drei unten beschriebenen Aktualisierungen:
>
> * Kann *nicht* VEC verwenden, ohne dass die VEC Helper-Erweiterung für kennwortgeschützte Seiten Ihrer Sites installiert und aktiviert ist. Ihre Site-Anmelde-Cookies werden als Drittanbieter-Cookies betrachtet und nicht mit Anmeldeanfragen im VEC-Editor im Modus Durchsuchen gesendet. Die einzige Ausnahme besteht darin, dass für Ihre Site-Anmelde-Cookies bereits die Attribute `SameSite=None` und `Secure` festgelegt sind.

**Chrome 94 (21. September 2021)**: Mit den bevorstehenden Änderungen in der Chrome-Version 94 (21. September 2021) wirkt sich die folgende Änderung auf alle Benutzer mit Chrome 94+-Browserversionen aus:

* Die Befehlszeilenkennzeichnung `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wird entfernt.

**Chrome 91 (25. Mai 2021)**: Mit den für die Chrome-Version 91 implementierten Änderungen (25. Mai 2021) wirkt sich die folgende Änderung auf alle Benutzer mit Chrome 91+-Browserversionen aus:

* Die Flags `#same-site-by-default-cookies` und `#cookies-without-same-site-must-be-secure` wurden aus `chrome://flags` entfernt. Dieses Verhalten ist jetzt standardmäßig aktiviert.

**Chrome 80 (August 2020)**: Mit den im August 2020 implementierten Änderungen sind alle Benutzer mit Chrome 80+-Browserversionen:

* Kann *nicht* [!DNL Target] -Bibliotheken beim Bearbeiten einer Aktivität herunterladen (wenn diese noch nicht auf der Site vorhanden sind). Der Grund dafür ist, dass der Download-Aufruf von der Kundendomäne zu einer gesicherten [!DNL Adobe] -Domäne erfolgt und als nicht authentifiziert zurückgewiesen wird.
* Der EEC funktioniert für alle Benutzer *nicht* , da er das SameSite-Attribut für Cookies nicht auf `adobemc.com domain` setzen kann. Ohne dieses Attribut lehnt der Browser diese Cookies ab, wodurch der EEC fehlschlägt.

### Ermitteln, welche Cookies blockiert werden

Um festzustellen, welche Cookies aufgrund der SameSite-Cookie-Durchsetzungsrichtlinien blockiert werden, verwenden Sie die Entwicklertools in Chrome.

1. Um auf die Entwicklertools zuzugreifen, während Sie den VEC in Chrome anzeigen, klicken Sie auf das Symbol &quot;**[!UICONTROL ellipsis]**&quot;oben rechts in Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]**.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Network]** > und suchen Sie dann nach blockierten Cookies.

   >[!NOTE]
   >
   >Verwenden Sie das Kontrollkästchen **[!UICONTROL Has blocked cookies]** , um das Auffinden von blockierten Cookies zu vereinfachen.

   Die folgende Abbildung zeigt ein blockiertes Cookie:

   ![Entwicklertools > Registerkarte &quot;Netzwerk&quot;mit einem blockierten Cookie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### [!DNL Adobe Target] VEC Helper-Erweiterung

Ab Version 0.7.1 fügt die Browsererweiterung [!DNL Adobe Target] VEC Helper die Attribute `SameSite=None` und `Secure` zu allen Cookies auf Antworten von Webseiten hinzu, die innerhalb des VEC bearbeitet werden, wenn der Umschalter &quot;Cookies&quot;in der Erweiterungs-Benutzeroberfläche aktiviert ist:

![Benutzeroberfläche der Adobe Target VEC Helper-Erweiterung UIAdobe Target VEC Helper-Erweiterung](assets/cookies-vec-helper.png)

### Alternativen und Problemumgehungen

Verwenden Sie eine der folgenden Optionen, um sicherzustellen, dass VEC und EEC weiterhin erwartungsgemäß funktionieren:

* Laden Sie die aktualisierte [VEC Helper-Erweiterung](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en) herunter und verwenden Sie sie.
* Verwenden Sie den Mozilla Firefox-Browser. Firefox erzwingt diese Richtlinie noch nicht.
* Verwenden Sie die folgenden Flags, um Google Chrome von der Befehlszeile bis zum 21. September 2021 auszuführen. Ab dem 21. September funktionieren Funktionen, für die Cookies erforderlich sind, im VEC nicht mehr, z. B. Anmelde- oder Cookie-Zustimmungs-Popup. Wenn Sie ein Update auf Chrome 94 durchführen, müssen Sie manuell Cookies mit `SameSite=none` und `Secure` auf Ihren Websites generieren.

  ```
  --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
  ```

## Unterstützt [!DNL Target] iFrames mit mehreren Ebenen?

[!DNL Target] unterstützt keine iFrames mit mehreren Ebenen. Wenn Ihre Website einen iframe lädt, der über einen untergeordneten iframe verfügt, interagiert at.js nur mit dem übergeordneten iframe. [!DNL Target] -Bibliotheken interagieren nicht mit dem untergeordneten iFrame.

Als Behelfslösung können Sie im Erlebnis eine Seite mit der URL des untergeordneten iFrame hinzufügen.

## Wenn ich versuche, eine Seite zu bearbeiten, sehe ich lediglich ein Netz anstelle meiner Seite. (VEC und EEC)   {#section_313001039F79446DB28C70D932AF5F58}

Dies kann vorkommen, wenn die URL ein #-Zeichen enthält. Um das Problem zu beheben, wechseln Sie im Visual Experience Composer in den Durchsuchen-Modus und anschließend wieder in den Erstellen-Modus. Das Netz sollte verschwinden und die Seite sollte angezeigt werden.

## Die Header der Content Security Policy (CSP) blockieren die [!DNL Target] -Bibliotheken auf meiner Website. (VEC und EEC)   {#section_89A30C7A213D43BFA0822E66B482B803}

Wenn die CSP-Header Ihrer Website Target-Bibliotheken blockieren und die Website anschließend geladen wird, die Bearbeitung aber nicht möglich ist, stellen Sie sicher, dass die Target-Bibliotheken nicht blockiert werden.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie auch die [Adobe Target VEC Helper-Browsererweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) für Google Chrome verwenden.

![cps_headers image](assets/cps_headers.png)

Als Problemumgehung können Sie eine Requestly-Regel zum Entfernen von CSP-Headern konfigurieren, wie unten dargestellt:

![cps_headers_2 image](assets/cps_headers_2.png)

Sie können eine ähnliche Requestly-Regel für beliebige Header konfigurieren, durch die eine Ressource im VEC nicht geladen wird.

Gehen Sie bei Requestly wie folgt vor, wenn Sie Header entfernen müssen:

* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.

## Der VEC oder EEC funktioniert scheinbar nicht oder wird beim erneuten Bearbeiten einer gespeicherten Aktivität nicht initialisiert. (VEC und EEC)   {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Wenn die Website nach Definition des Erlebnisses außerhalb von Visual Experience Composer geändert wurde, sind die Selektoren, auf denen zuvor Aktionen durchgeführt wurden, nicht auffindbar und die Aktivität wird zur erneuten Bearbeitung geöffnet. Die Seite erscheint beschädigt und es werden keine Warnungen eingeblendet.

## Der VEC oder EEC zeigt meine sich drehenden Banner oder anderen Inhalt mit JavaScript nicht an. (VEC und EEC)   {#section_8B5BE6EB050B42D6A14A054724C41330}

Der Visual Experience Composer blockiert standardmäßig JavaScript-Elemente. Sie können mit diesen Elementen arbeiten, wenn Sie JavaScript in den Visual Experience Composer-Einstellungen deaktivieren. Je nach Einrichtung der Site werden einige Elemente möglicherweise weiterhin falsch angezeigt oder sind nicht verfügbar.

## Wenn ich ein Element auf der Seite ändere, ändern sich mehrere Elemente. (VEC und EEC)   {#section_309188ACF34942989BE473F63C5710AF}

Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, sollte eine ID nur einmal auf jeder Seite verwendet werden. Dies ist eine gängige Best Practice für HTML. Weitere Informationen finden Sie unter [Szenarien für die Seitenmodifizierung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Bearbeitung von Erlebnissen für eine Site, die iFrames zerstört, ist nicht möglich. (VEC und EEC)   {#section_9FE266B964314F2EB75604B4D7047200}

Dieses Problem kann durch die Aktivierung des Enhanced Experience Composer behoben werden. Klicken Sie auf **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]** und aktivieren Sie dann das Kontrollkästchen, mit dem der Enhanced Experience Composer aktiviert wird. Der Enhanced Experience Composer verwendet ein von Adobe verwaltetes Proxy, um Ihre Seite zur Bearbeitung zu laden. Dieser Proxy ermöglicht die Bearbeitung auf iFrame-Busting-Sites und die Bearbeitung auf Sites und Seiten, auf denen Sie noch keinen Adobe Target-Code hinzugefügt haben. Solange kein Code hinzugefügt wurde, liefern die Aktivitäten nicht an die Site. Einige Websites werden in Enhanced Experience Composer möglicherweise nicht geladen. In diesem Fall können Sie diese Option deaktivieren, um Visual Experience Composer in einem iFrame zu laden. 

>[!NOTE]
>
>Ihre lokal gehosteten Seiten oder Seiten, auf die außerhalb Ihres Netzwerks nicht zugegriffen werden kann, sind für den Adobe-Proxyserver nicht zugänglich und können im EEC nicht geöffnet werden. Diese Seiten können Staging-URLs, Akzeptanztest-URLs (UAT) oder lokal gehostete Seiten enthalten.

## Ich möchte Tests auf Seiten einrichten, für die bisher noch keine Mbox-/Target-Implementierung vorgenommen wurde. (VEC und EEC)   {#section_DE63BCCB5B124E10A71FA579B582A80A}

Siehe oben unter „Ich kann keine Erlebnisse für eine iFrame-zerstörende Website bearbeiten“.

## Auf meiner Seite wird bei „Text/HTML bearbeiten“ oder „Text/HTML ändern“ kein fett und kursiv gedruckter Text angezeigt. Manchmal verschwindet der Text nach der Anwendung dieser Stiländerungen. (VEC und EEC)   {#section_7A71D6DF41084C58B34C18701E8774E5}

Wenn Sie **[!UICONTROL Edit Text/HTML]** im Visual Experience Composer für A/B- oder Erlebnis-Targeting-Aktivitäten oder **[!UICONTROL Change Text/HTML]** für Automated Personalization- oder Multivarianz-Test-Aktivitäten verwenden, um Text fett oder kursiv zu formatieren, werden diese Stile möglicherweise nicht auf der Seite angewendet oder der Text wird auf der Seite im Visual Experience Composer ausgeblendet. Dies geschieht aufgrund der Art und Weise, wie der Rich-Text-Editor diese Stile anwendet, möglicherweise mit dem Website-Markup.

Wenn Sie dieses Problem angezeigt bekommen, tun Sie Folgendes:

1. Klicken Sie im Rich-Text-Editor auf die Schaltfläche &quot;**[!UICONTROL HTML]**&quot;, um in den Quellbearbeitungsmodus zu wechseln.
1. Suchen Sie die Stiltextelemente.

   * Für fett gedruckten Text ändern Sie `<strong>`-Elemente zu `<b>`.

   * Für kursiv gedruckten Text ändern Sie `<em>`-Elemente zu `<i>`.

## Bei Aktivitäten mit automatisierter Personalisierung scheint der Bildtausch im VEC oder EEC nicht zu funktionieren. (VEC und EEC)   {#section_88AABFDFE6A3420299B0D508B12A3994}

Das Hinzufügen eines Bildangebots zu einem Pfad erfordert die vollständige Dimension des ursprünglichen Bildplatzes im VEC oder EEC. Bei der Bereitstellung wird das Bild nicht erweitert, sondern wie vorhanden angezeigt, sodass die Bereitstellung nicht beeinträchtigt wird.
