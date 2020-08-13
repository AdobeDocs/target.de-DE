---
keywords: Targeting;visual experience composer;whitelist;white list;allowlist;allow list;enhanced visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;eec;enhanced experience composer;tls;tls 1.2
description: Im Visual Experience Composer (VEC) und Enhanced Experience Composer (EEC) treten unter bestimmten Umständen mitunter Anzeigeprobleme auf.
title: Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer
feature: vec
uuid: 93f646d9-fcbc-43f0-9f84-0ce8e486ff7f
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 98%

---


# Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer{#troubleshooting-issues-related-to-the-visual-experience-composer-and-enhanced-experience-composer}

Im Visual Experience Composer (VEC) und Enhanced Experience Composer (EEC) treten unter bestimmten Umständen mitunter Anzeigeprobleme auf.

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

Wir empfehlen allen VEC-Benutzern ein Upgrade auf die [neueste Version von mbox.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A), zumindest aber auf Version 57. Sie sollten auch erwägen, [auf at.js umzustellen](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).

## Wenn ich ein Element auf der Seite ändere, ändern sich mehrere Elemente. (VEC und EEC) {#section_309188ACF34942989BE473F63C5710AF}

Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, sollte eine ID nur einmal auf jeder Seite verwendet werden. Dies ist eine übliche Best Practice für HTML. Weitere Informationen finden Sie unter  [Szenarien für die Seitenmodifizierung](../../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

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
