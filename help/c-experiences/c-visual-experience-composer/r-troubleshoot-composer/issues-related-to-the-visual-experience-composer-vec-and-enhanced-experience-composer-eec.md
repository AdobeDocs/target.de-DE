---
keywords: Targeting;Visual Experience Composer;Whitelist;White List;Zulassungsliste;Zulassungsliste;Enhanced Visual Experience Composer;VEC;Fehlerbehebung Visual Experience Composer;Fehlerbehebung;EEC;Enhanced Experience Composer;TLS;TLS 1.2
description: Erfahren Sie, wie Sie unter bestimmten Bedingungen Probleme beheben können, die manchmal in der Adobe [!DNL Target] Visual Experience Composer (VEC) und im Enhanced Experience Composer (EEC) auftreten.
title: Wie kann ich Probleme im Zusammenhang mit Visual Experience Composer und Enhanced Experience Composer beheben?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 1da930f2dfe13fc7710da000f0d13d6aacd223b1
workflow-type: tm+mt
source-wordcount: '1545'
ht-degree: 48%

---

# Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer

Anzeigeprobleme und andere Probleme treten manchmal unter bestimmten Bedingungen im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) und im [!UICONTROL Enhanced Experience Composer] (EEC) auf.

## Wie wirken sich die Durchsetzungsrichtlinien für SameSite-Cookies in Google Chrome auf VEC und EEC aus? {#samesite}

Beachten Sie die Änderungen, die sich auf VEC und EEC auswirken, wenn Sie die folgenden Chrome-Versionen verwenden:

**Chrome 94 (21. September 2021)**: Da die bevorstehenden Änderungen für die Chrome-Version 94 (21. September 2021) geplant sind, wirkt sich die folgende Änderung auf alle Benutzer mit Chrome 94+-Browserversionen aus:

* Die Befehlszeilenkennzeichnung `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wird entfernt.

**Chrome 91 (25. Mai 2021)**: Nachdem die Änderungen für die Chrome-Version 91 (25. Mai 2021) implementiert wurden, wirkt sich die folgende Änderung auf alle Benutzer mit Chrome 91+-Browserversionen aus:

* Die Flags `#same-site-by-default-cookies` und `#cookies-without-same-site-must-be-secure` wurden aus `chrome://flags` entfernt. Dieses Verhalten ist jetzt standardmäßig aktiviert.

**Chrome 80 (August 2020)**: Nachdem die Änderungen im August 2020 implementiert wurden, sind alle Benutzer mit Chrome 80+-Browserversionen:

* Kann *not* VEC (mit oder ohne installierte und aktivierte VEC Helper-Erweiterung) auf kennwortgeschützten Seiten ihrer Sites verwenden. Ihre Site-Anmelde-Cookies werden als Drittanbieter-Cookie betrachtet und mit der Anmeldeanfrage gesendet. Die einzige Ausnahme besteht darin, dass für Ihr Site-Anmelde-Cookie bereits der SameSite-Parameter auf &quot;none&quot;gesetzt ist.
* Kann *not* [!DNL Target]-Bibliotheken beim Bearbeiten einer Aktivität herunterladen (wenn diese noch nicht auf der Site vorhanden sind). Der Grund dafür ist, dass der Download-Aufruf von der Kundendomäne zu einer gesicherten Adobe-Domäne erfolgt und als nicht authentifiziert zurückgewiesen wird.
* Der EEC funktioniert *nicht* für alle Benutzer, da er das SameSite-Attribut für Cookies nicht auf `adobemc.com domain` setzen kann. Ohne dieses Attribut lehnt der Browser diese Cookies ab, wodurch der EEC fehlschlägt.

### Ermitteln, welche Cookies blockiert werden

Um festzustellen, welche Cookies aufgrund der SameSite-Cookie-Durchsetzungsrichtlinien blockiert werden, verwenden Sie die Entwicklertools in Chrome.

1. Um auf die Entwicklertools zuzugreifen, während Sie den VEC in Chrome anzeigen, klicken Sie auf das Symbol **[!UICONTROL Auslassungspunkte]** in der oberen rechten Ecke von Chrome > **[!UICONTROL Weitere Tools]** > **[!UICONTROL Entwicklertools]**.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Netzwerk]** und suchen Sie dann nach blockierten Cookies.

   >[!NOTE]
   >
   >Verwenden Sie das Kontrollkästchen **[!UICONTROL Hat blockierte Cookies]** , um die Suche nach blockierten Cookies zu vereinfachen.

   Die folgende Abbildung zeigt ein blockiertes Cookie:

   ![Registerkarte &quot;Entwicklertools&quot;> &quot;Netzwerk&quot;mit einem blockierten Cookie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### Google VEC Helper-Erweiterung

Adobe hat eine aktualisierte VEC Helper-Erweiterung an den Google Chrome Store übermittelt. Diese Erweiterung überschreibt die Cookie-Attribute, um bei Bedarf das `SameSite="none"` -Attribut festzulegen. Die [aktualisierte Erweiterung finden Sie hier](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en). Weitere Informationen zur Installation und Verwendung der VEC Helper Extension finden Sie unter [Visual Experience Composer Helper Extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

Für Ihre eigenen Site-Cookies müssen Sie die Cookies anhand des Namens angeben.

>[!NOTE]
>
>Dieser Ansatz eignet sich nur, wenn alle Cookies in einer Domäne gesetzt sind. Der VEC-Helfer erlaubt [!DNL Target] nicht, Cookies für mehr als eine Domäne anzugeben.

Schalten Sie den Regler [!UICONTROL Cookie] auf die Position &quot;Ein&quot;um und geben Sie dann das Cookie nach Name und Cookie-Domäne an. Der Cookie-Name ist &quot;mbox&quot;und die Cookie-Domäne ist die zweite und oberste Ebene der Domänen, von denen Sie die Mbox beliefern. Da die Belieferung von der Domäne Ihres Unternehmens stattfindet, handelt es sich um ein Erstanbieter-Cookie. Beispiel: `mycompany.com`. Weitere Informationen finden Sie unter [Adobe Target-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html?lang=de) im *Experience Cloud Interface-Benutzerhandbuch*.

![Umschalten von Cookies in der VEC Helper-Erweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

### Alternativen und Problemumgehungen

Verwenden Sie eine der folgenden Optionen, um sicherzustellen, dass VEC und EEC weiterhin erwartungsgemäß funktionieren:

* Laden Sie die aktualisierte [VEC Helper-Erweiterung](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en) herunter und verwenden Sie sie.
* Verwenden Sie den Mozilla Firefox-Browser. Firefox erzwingt diese Richtlinie noch nicht.
* Verwenden Sie die folgenden Flags, um Google Chrome von der Befehlszeile bis zum 21. September 2021 auszuführen. Nach dem 21. September funktioniert Ihre Website nicht mehr im VEC. Wenn Sie auf Chrome 94 aktualisieren, müssen Sie manuell Cookies mit `SameSite=none` und `Secure` auf Ihren Websites generieren.

   ```
   --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
   ```

## Unterstützt [!DNL Target] iFrames mit mehreren Ebenen?

[!DNL Target]Nein,  unterstützt keine iFrames mit mehreren Ebenen. Wenn Ihre Website einen iframe lädt, der über einen untergeordneten iframe verfügt, interagiert at.js nur mit dem übergeordneten iframe. [!DNL Target] -Bibliotheken interagieren nicht mit dem untergeordneten iframe.

Als Behelfslösung können Sie im Erlebnis eine Seite mit der URL des untergeordneten iFrame hinzufügen.

## Wenn ich versuche, eine Seite zu bearbeiten, sehe ich lediglich ein Netz anstelle meiner Seite. (VEC und EEC)   {#section_313001039F79446DB28C70D932AF5F58}

Dies kann vorkommen, wenn die URL ein #-Zeichen enthält. Um das Problem zu beheben, wechseln Sie im Visual Experience Composer in den Durchsuchen-Modus und anschließend wieder in den Erstellen-Modus. Das Netz sollte verschwinden und die Seite sollte angezeigt werden.

## Die Header der Content Security Policy (CSP) blockieren die [!DNL Target]-Bibliotheken auf meiner Website. (VEC und EEC)   {#section_89A30C7A213D43BFA0822E66B482B803}

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

## Der VEC oder EEC funktioniert scheinbar nicht oder wird beim erneuten Bearbeiten einer gespeicherten Aktivität nicht initialisiert. (VEC und EEC)   {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Wenn die Website nach Definition des Erlebnisses außerhalb von Visual Experience Composer geändert wurde, sind die Selektoren, auf denen zuvor Aktionen durchgeführt wurden, nicht auffindbar und die Aktivität wird zur erneuten Bearbeitung geöffnet. Die Seite erscheint beschädigt und es werden keine Warnungen eingeblendet.

## Der VEC oder EEC zeigt meine sich drehenden Banner oder anderen Inhalt mit JavaScript nicht an. (VEC und EEC)   {#section_8B5BE6EB050B42D6A14A054724C41330}

Der Visual Experience Composer blockiert standardmäßig JavaScript-Elemente. Sie können mit diesen Elementen arbeiten, wenn Sie JavaScript in den Visual Experience Composer-Einstellungen deaktivieren. Je nach Einrichtung der Site werden einige Elemente möglicherweise weiterhin falsch angezeigt oder sind nicht verfügbar.

## Wenn ich ein Element auf der Seite ändere, ändern sich mehrere Elemente. (VEC und EEC)   {#section_309188ACF34942989BE473F63C5710AF}

Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, sollte eine ID nur einmal auf jeder Seite verwendet werden. Diese Vorgehensweise ist eine standardmäßige Best Practice für HTML. Weitere Informationen finden Sie unter [Szenarien für die Seitenmodifizierung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Die Bearbeitung von Erlebnissen für eine Site, die iFrames zerstört, ist nicht möglich. (VEC und EEC)   {#section_9FE266B964314F2EB75604B4D7047200}

Dieses Problem kann durch die Aktivierung des Enhanced Experience Composer behoben werden. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und aktivieren Sie dann das Kontrollkästchen, mit dem der Enhanced Experience Composer aktiviert wird. Der Enhanced Experience Composer verwendet ein von Adobe verwaltetes Proxy, um Ihre Seite zur Bearbeitung zu laden. Dieser Proxy ermöglicht die Bearbeitung auf iFrame-Busting-Sites und die Bearbeitung auf Sites und Seiten, auf denen Sie noch keinen Adobe Target-Code hinzugefügt haben. Solange kein Code hinzugefügt wurde, liefern die Aktivitäten nicht an die Site. Einige Websites werden in Enhanced Experience Composer möglicherweise nicht geladen. In diesem Fall können Sie diese Option deaktivieren, um Visual Experience Composer in einem iFrame zu laden. 

>[!NOTE]
>
>Ihre lokal gehosteten Seiten oder Seiten, auf die außerhalb Ihres Netzwerks nicht zugegriffen werden kann, sind für den Adobe-Proxyserver nicht zugänglich und können im EEC nicht geöffnet werden. Diese Seiten können Staging-URLs, Akzeptanztest-URLs (UAT) oder lokal gehostete Seiten enthalten.

## Ich möchte Tests auf Seiten einrichten, für die bisher noch keine Mbox-/Target-Implementierung vorgenommen wurde. (VEC und EEC)   {#section_DE63BCCB5B124E10A71FA579B582A80A}

Siehe oben unter „Ich kann keine Erlebnisse für eine iFrame-zerstörende Website bearbeiten“.

## Auf meiner Seite wird bei „Text/HTML bearbeiten“ oder „Text/HTML ändern“ kein fett und kursiv gedruckter Text angezeigt. Manchmal verschwindet der Text nach der Anwendung dieser Stiländerungen. (VEC und EEC)   {#section_7A71D6DF41084C58B34C18701E8774E5}

Wenn Sie **[!UICONTROL Text/HTML bearbeiten]** im Visual Experience Composer für A/B- oder Erlebniszielaktivitäten oder **[!UICONTROL Text/HTML ändern]** für automatisierte Personalisierungs- oder Multivarianztest-Aktivitäten verwenden, um den Text fett oder kursiv zu formatieren, werden diese Stile möglicherweise nicht auf der Seite übernommen, oder der Text wird auf der Seite im Visual Experience Composer ausgeblendet. Dies geschieht aufgrund der Art und Weise, wie der Rich-Text-Editor diese Stile anwendet, möglicherweise mit dem Website-Markup in Konflikt gerät.

Wenn Sie dieses Problem angezeigt bekommen, tun Sie Folgendes:

1. Klicken Sie im Richt-Text-Editor auf die Schaltfläche **[!UICONTROL HTML]**, um in den Quellbearbeitungsmodus zu wechseln.
1. Suchen Sie die Stiltextelemente.

   * Für fett gedruckten Text ändern Sie `<strong>`-Elemente zu `<b>`.

   * Für kursiv gedruckten Text ändern Sie `<em>`-Elemente zu `<i>`.

## Bei Aktivitäten mit automatisierter Personalisierung scheint der Bildtausch im VEC oder EEC nicht zu funktionieren. (VEC und EEC)   {#section_88AABFDFE6A3420299B0D508B12A3994}

Das Hinzufügen eines Bildangebots zu einem Pfad erfordert die vollständige Dimension des ursprünglichen Bildplatzes im VEC oder EEC. Bei der Bereitstellung wird das Bild nicht erweitert, sondern wie vorhanden angezeigt, sodass die Bereitstellung nicht beeinträchtigt wird.
