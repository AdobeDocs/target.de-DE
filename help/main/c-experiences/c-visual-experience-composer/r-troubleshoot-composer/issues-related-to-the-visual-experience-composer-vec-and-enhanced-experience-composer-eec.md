---
keywords: Targeting;Visual Experience Composer;Whitelist;weiße Liste;Zulassungsliste;Enhanced Visual Experience Composer;VEC;Fehlerbehebung in Visual Experience Composer;Fehlerbehebung;EEC;Enhanced Experience Composer;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme beheben können, die unter bestimmten Bedingungen  [!DNL Target] [!UICONTROL &#x200B; Visual Experience &#x200B;] (VEC) und [!UICONTROL Enhanced Experience Composer] (EEC) auftreten.
title: Wie behebe ich Probleme mit dem [!UICONTROL Visual Experience Composer] und dem [!UICONTROL Enhanced Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
TQID: https://experienceleague.adobe.com/4v7Qe-Yzjke-GceUSRDO2SMZGkxvrkdsSXQt8TR-bic
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1271
ht-degree: 31%

---

# Beheben von Problemen mit [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] und [!UICONTROL Enhanced Experience Composer]

Anzeigeprobleme und andere Probleme treten unter bestimmten Bedingungen manchmal in [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) und [!UICONTROL Enhanced Experience Composer] (EEC) auf.

## Wie wirken sich die SameSite-Cookie-Richtlinien von Google Chrome auf VEC und EEC aus? {#samesite}

+++Details
Beachten Sie die Änderungen, die sich auf VEC und EEC auswirken, wenn Sie die folgenden [!DNL Chrome] Versionen verwenden:

>[!NOTE]
>
>Die folgende Änderung wirkt sich auf alle drei unten beschriebenen Aktualisierungen aus:
>
> * Kann *VEC* verwenden, ohne dass die [VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) installiert und für kennwortgeschützte Seiten Ihrer Sites aktiviert ist. Ihre Site-Anmelde-Cookies werden als Drittanbieter-Cookies betrachtet und werden nicht mit Anmeldeanfragen innerhalb des VEC-Editors im [!UICONTROL Durchsuchen]-Modus gesendet. Die einzige Ausnahme besteht, wenn für die Anmelde-Cookies Ihrer Site bereits die Attribute `SameSite=None` und `Secure` festgelegt sind.

**Chrome 94 (21. September 2021)**: Mit den für die Version Chrome 94 (21. September 2021) geplanten Änderungen wirkt sich die folgende Änderung auf alle Benutzenden mit Browser-Versionen von Chrome 94 oder höher aus:

* Das Befehlszeilen-Flag `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wird entfernt.

**Chrome 91 (25. Mai 2021)**: Mit den Änderungen, die für die Version Chrome 91 (25. Mai 2021) implementiert wurden, wirkt sich die folgende Änderung auf alle Benutzenden mit Browser-Versionen von Chrome 91 oder höher aus:

* Die Flags `#same-site-by-default-cookies` und `#cookies-without-same-site-must-be-secure` wurden aus `chrome://flags` entfernt. Dieses Verhalten ist jetzt standardmäßig aktiviert.

**Chrome 80 (August 2020)**: Mit den Änderungen, die im August 2020 implementiert wurden, haben alle Benutzenden Browser-Versionen von Chrome 80 oder höher:

* Kann *nicht* beim Bearbeiten einer Aktivität [!DNL Target] Bibliotheken herunterladen (wenn diese nicht bereits auf der Website vorhanden sind). Dies liegt daran, dass der Download-Aufruf von der Kunden-Domain an eine gesicherte [!DNL Adobe]-Domain erfolgt und als nicht authentifiziert zurückgewiesen wird.

* Der EEC wird *nicht* für alle Benutzer funktionieren, da er nicht das SameSite-Attribut für Cookies in `adobemc.com domain` festlegen kann. Ohne dieses Attribut lehnt der Browser diese Cookies ab, was dazu führt, dass der EEC fehlschlägt.

+++

### Bestimmen, welche Cookies blockiert werden

+++Details
Um festzustellen, welche Cookies aufgrund der SameSite-Cookie-Durchsetzungsrichtlinien blockiert werden, verwenden Sie die [!DNL Developer Tools] in [!DNL Chrome].

1. Wenn Sie auf die [!DNL Developer Tools] zugreifen möchten, während Sie den VEC in [!DNL Chrome] anzeigen, klicken Sie oben rechts in Chrome auf das **&#x200B;**&#x200B;Ellipsen“ > **[!UICONTROL Weitere Tools]** > **[!UICONTROL Entwickler-Tools]**.
1. Klicken Sie auf **[!UICONTROL Netzwerk]** und suchen Sie nach blockierten Cookies.

   >[!NOTE]
   >
   >Aktivieren Sie das **[!UICONTROL Hat blockierte Cookies]**, um das Auffinden blockierter Cookies zu vereinfachen.

+++

## Unterstützt [!DNL Target] iFrames mit mehreren Ebenen?

+++Details
[!DNL Target] unterstützt keine iFrames mit mehreren Ebenen. Wenn Ihre Website einen iframe lädt, der einen untergeordneten iframe hat, interagiert at.js nur mit dem übergeordneten iframe. [!DNL Target] Bibliotheken interagieren nicht mit dem untergeordneten iframe.

Als Behelfslösung können Sie im Erlebnis eine Seite mit der URL des untergeordneten iFrame hinzufügen.

+++

## Wenn ich versuche, eine Seite zu bearbeiten, sehe ich lediglich ein Netz anstelle meiner Seite. (VEC und EEC) {#section_313001039F79446DB28C70D932AF5F58}

+++Details
Dies kann vorkommen, wenn die URL ein #-Zeichen enthält. Um das Problem zu beheben, wechseln Sie im VEC oder EEC in den [!UICONTROL Durchsuchen]-Modus und wechseln Sie dann zurück in den [!UICONTROL Erstellen]-Modus. Das Netz sollte verschwinden und die Seite sollte angezeigt werden.

+++

## CSP-Header (Content Security Policy) blockieren die [!DNL Target] auf meiner Website. (VEC und EEC) {#section_89A30C7A213D43BFA0822E66B482B803}


+++Details
Wenn die CSP-Kopfzeilen Ihrer Website [!DNL Target] Bibliotheken blockieren und dann die Website lädt, aber die Bearbeitung verhindert, stellen Sie sicher, dass die [!DNL Target] Bibliotheken nicht blockiert werden.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen können Sie [!DNL Google Chrome] die [Adobe Target VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)Browsererweiterung verwenden.

![cps_headers-Bild](assets/cps_headers.png)

Als Problemumgehung können Sie eine [!DNL Requestly] konfigurieren, um CSP-Kopfzeilen zu entfernen, wie unten dargestellt:

![cps_headers_2 Bild](assets/cps_headers_2.png)

Sie können eine ähnliche [!DNL Requestly] für jede Kopfzeile konfigurieren, die dazu führt, dass eine Ressource nicht im VEC geladen wird.

Wenn [!DNL Requestly] Kopfzeilen entfernt werden müssen, sollten Sie einen der folgenden Schritte ausführen:

* Fügen Sie URL-Regeln für die URL hinzu, die Sie in VEC öffnen wollen, damit Header nur für diese URLs entfernt werden.
* Aktivieren Sie die Regel bei der Bearbeitung in VEC und deaktivieren Sie die Regel, wenn Sie VEC nicht verwenden.

+++

## Der VEC oder EEC funktioniert scheinbar nicht oder wird beim erneuten Bearbeiten einer gespeicherten Aktivität nicht initialisiert. (VEC und EEC) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

+++Details
Wenn sich die Website außerhalb von VEC geändert hat, nachdem das Erlebnis definiert wurde, können Selektoren, für die zuvor Aktionen durchgeführt wurden, nicht gefunden werden, wenn die Aktivität zur erneuten Bearbeitung geöffnet wird. Die Seite erscheint beschädigt und es werden keine Warnungen eingeblendet.

+++

## Der VEC oder EEC zeigt meine sich drehenden Banner oder anderen Inhalt mit JavaScript nicht an. (VEC und EEC) {#section_8B5BE6EB050B42D6A14A054724C41330}

+++Details
Standardmäßig blockiert der VEC JavaScript-Elemente. Sie können mit diesen Elementen arbeiten, wenn Sie JavaScript deaktivieren. Je nach Einrichtung der Site werden einige Elemente möglicherweise weiterhin falsch angezeigt oder sind nicht verfügbar.

+++

## Wenn ich ein Element auf der Seite ändere, ändern sich mehrere Elemente. (VEC und EEC) {#section_309188ACF34942989BE473F63C5710AF}

+++Details
Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, sollte eine ID nur einmal auf jeder Seite verwendet werden. Dies ist eine standardmäßige Best Practice für HTML. Weitere Informationen finden Sie unter [Szenarien für die Seitenmodifizierung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

+++

## Die Bearbeitung von Erlebnissen für eine Site, die iFrames zerstört, ist nicht möglich. (VEC und EEC) {#section_9FE266B964314F2EB75604B4D7047200}

+++Details
Um dieses Problem zu beheben, aktivieren Sie den [!UICONTROL Enhanced Experience Composer] (EEC). Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und aktivieren Sie dann das Kontrollkästchen, um den [!UICONTROL Enhanced Experience Composer] zu aktivieren. Der EEC verwendet einen [!DNL Adobe] verwalteten Proxy, um die Seite zur Bearbeitung zu laden. Dieser Proxy ermöglicht die Bearbeitung auf iFrame-Busting-Sites und die Bearbeitung auf Sites und Seiten, auf denen Sie noch keinen [!DNL Adobe Target]-Code hinzugefügt haben. Solange kein Code hinzugefügt wurde, liefern die Aktivitäten nicht an die Site. Einige Websites werden möglicherweise nicht über den EEC geladen. In diesem Fall können Sie diese Option deaktivieren, um den EEC über einen iFrame zu laden.

>[!NOTE]
>
>Die lokal gehosteten Seiten oder Seiten, auf die außerhalb des Netzwerks nicht zugegriffen werden kann, sind für den [!DNL Adobe]-Proxy-Server nicht zugänglich und können nicht in EEC geöffnet werden. Diese Seiten können Staging-URLs, Akzeptanztest-URLs (UAT) oder lokal gehostete Seiten enthalten.

+++

## Ich möchte Tests auf Seiten einrichten, auf denen die Mbox/[!DNL Target]-Implementierung noch nicht durchgeführt wurde. (VEC und EEC) {#section_DE63BCCB5B124E10A71FA579B582A80A}

+++Details
Siehe oben unter „Ich kann keine Erlebnisse für eine iFrame-zerstörende Website bearbeiten“.

+++

## Fett- und Kursiv-Textstile mit [!UICONTROL Text bearbeiten]/[!UICONTROL HTML bearbeiten] oder [!UICONTROL Text ändern]/[!DNL Change HTML] werden auf meiner Seite nicht angezeigt. Manchmal verschwindet der Text nach der Anwendung dieser Stiländerungen. (VEC und EEC) {#section_7A71D6DF41084C58B34C18701E8774E5}

+++Details
Wenn Sie **[!UICONTROL Text bearbeiten]/[!UICONTROL HTML bearbeiten]** im VEC für [!UICONTROL A/B-]- oder [!UICONTROL Experience Targeting]-Aktivitäten oder **[!UICONTROL Text ändern]/[!UICONTROL HTML ändern]** für [!UICONTROL Automated Personalization]- oder [!UICONTROL Multivarianz-Test]-Aktivitäten verwenden, um Text fett oder kursiv zu formatieren, werden diese Stile möglicherweise nicht auf der Seite angewendet oder der Text verschwindet von der Seite im VEC. Dies geschieht, weil die Art und Weise, wie der Rich-Text-Editor diese Stile anwendet, das Website-Markup beeinträchtigen kann.

Wenn Sie dieses Problem angezeigt bekommen, tun Sie Folgendes:

1. Klicken Sie im Richt-Text-Editor auf die Schaltfläche **[!UICONTROL HTML]**, um in den Quellbearbeitungsmodus zu wechseln.
1. Suchen Sie die Stiltextelemente.

   * Für fett gedruckten Text ändern Sie `<strong>`-Elemente zu `<b>`.

   * Für kursiv gedruckten Text ändern Sie `<em>`-Elemente zu `<i>`.

+++

## Bei Aktivitäten mit automatisierter Personalisierung scheint der Bildtausch im VEC oder EEC nicht zu funktionieren. (VEC und EEC) {#section_88AABFDFE6A3420299B0D508B12A3994}

+++Details
Das Hinzufügen eines Bildangebots zu einem Pfad erfordert die vollständige Dimension des ursprünglichen Bildplatzes im VEC oder EEC. Bei der Bereitstellung wird das Bild nicht erweitert, sondern wie vorhanden angezeigt, sodass die Bereitstellung nicht beeinträchtigt wird.

+++
