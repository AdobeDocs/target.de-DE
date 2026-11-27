---
keywords: Targeting;Visual Experience Composer;Whitelist;weiße Liste;Zulassungsliste;Enhanced Visual Experience Composer;VEC;Fehlerbehebung in Visual Experience Composer;Fehlerbehebung;EEC;Enhanced Experience Composer;TLS;TLS 1.2
description: Erfahren Sie, wie Sie Probleme beheben können, die unter bestimmten Bedingungen in [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) und [!UICONTROL Enhanced Experience Composer] (EEC) auftreten.
title: Wie behebe ich Probleme mit dem [!UICONTROL Visual Experience Composer] und dem [!UICONTROL Enhanced Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
TQID: 'https://experienceleague.adobe.com/4v7Qe-Yzjke-GceUSRDO2SMZGkxvrkdsSXQt8TR-bic'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1218'
ht-degree: 13%
---
# Beheben von Problemen mit [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] und [!UICONTROL Enhanced Experience Composer] {#vec-eec-issues}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie die Probleme beheben, die sowohl **[!UICONTROL Visual Experience Composer]** (VEC) als auch **[!UICONTROL Enhanced Experience Composer]** (EEC) betreffen.

>[!ENDSHADEBOX]

Anzeigeprobleme und andere Probleme treten unter bestimmten Bedingungen manchmal in [!DNL Target] **[!UICONTROL Visual Experience Composer]** (VEC) und **[!UICONTROL Enhanced Experience Composer]** (EEC) auf. In den folgenden Abschnitten werden die Probleme beschrieben, die sich auf beide Komponisten auswirken, und wie sie gelöst werden können.

## Browser und Sicherheit

### SameSite-Cookie-Richtlinien von Google Chrome {#samesite}

Die SameSite-Cookie-Richtlinien von [!DNL Google Chrome] wirken sich in den folgenden Versionen auf den VEC und EEC aus.

>[!NOTE]
>
>Die folgende Änderung gilt für alle drei Versionen. Der VEC kann auf kennwortgeschützten Seiten der Website nur verwendet werden, wenn die [VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) installiert und aktiviert ist. Die Anmelde-Cookies der Website werden als Drittanbieter-Cookies betrachtet, sodass sie nicht mit Anmeldeanfragen im VEC-Editor im **[!UICONTROL Durchsuchen]**-Modus gesendet werden. Die einzige Ausnahme besteht, wenn für die Anmelde-Cookies bereits die Attribute `SameSite=None` und `Secure` festgelegt sind.

* **Chrome 94 (21. September 2021):** Für alle Benutzer mit Chrome 94 und höher wurde das Befehlszeilen-Flag `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` entfernt.
* **Chrome 91 (25. Mai 2021):** Für alle Benutzer mit Chrome 91 und höher wurden die Flags `#same-site-by-default-cookies` und `#cookies-without-same-site-must-be-secure` aus `chrome://flags` entfernt. Dieses Verhalten ist jetzt standardmäßig aktiviert.
* **Chrome 80 (August 2020):** Für alle Benutzer mit Chrome 80 und höher:

  * [!DNL Target] Bibliotheken können nicht heruntergeladen werden, während eine Aktivität bearbeitet wird, wenn sie sich noch nicht auf der Website befinden. Der Download-Aufruf erfolgt von der Kunden-Domain an eine gesicherte [!DNL Adobe]-Domain und wird als nicht authentifiziert zurückgewiesen.
  * Der EEC funktioniert nicht, da er das SameSite-Attribut für Cookies in der `adobemc.com` Domain nicht festlegen kann. Ohne dieses Attribut lehnt der Browser diese Cookies ab, was dazu führt, dass der EEC fehlschlägt.

+++ Bestimmen, welche Cookies blockiert werden

Um festzustellen, welche Cookies durch die SameSite-Cookie-Richtlinien blockiert werden, verwenden Sie die [!DNL Developer Tools] in [!DNL Chrome].

1. Wenn Sie VEC in [!DNL Chrome] anzeigen, klicken Sie auf das Symbol **[!UICONTROL Auslassungspunkte]** oben rechts in Chrome > **[!UICONTROL Weitere Tools]** > **[!UICONTROL Entwickler-Tools]**.
1. Klicken Sie auf **[!UICONTROL Netzwerk]** und suchen Sie nach blockierten Cookies.

   >[!NOTE]
   >
   >Aktivieren Sie das Kontrollkästchen **[!UICONTROL Hat blockierte Cookies]**, um die Suche nach blockierten Cookies zu vereinfachen.

+++

+++ CSP-Header (Content Security Policy) blockieren die [!DNL Target] auf der Website

Wenn die CSP-Kopfzeilen der Website die [!DNL Target]-Bibliotheken blockieren, wird die Website geladen, aber die Bearbeitung wird verhindert. Stellen Sie sicher, dass die [!DNL Target] nicht blockiert sind.

>[!NOTE]
>
>Zusätzlich zu den folgenden Informationen kann die [Adobe Target VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)Browsererweiterung für [!DNL Google Chrome] verwendet werden.

![Browser-Konsole, die eine blockierte Anfrage für target.js mit der Meldung anzeigt, dass die Content Security Policy-Direktive verletzt wurde](assets/cps_headers.png)

Konfigurieren Sie als Problemumgehung eine [!DNL Requestly], um die CSP-Kopfzeilen zu entfernen, wie in der folgenden Abbildung dargestellt.

![Im Dialogfeld „Anfrage“ ändern Sie Kopfzeilen in HTTP-Anfrage und -Antwort mit einer Regel namens „Content-Security-Policy“, die die Kopfzeile „Content-Security-Policy“ aus der Antwort entfernt](assets/cps_headers_2.png)

Eine ähnliche [!DNL Requestly] kann für jede Kopfzeile konfiguriert werden, die dazu führt, dass eine Ressource nicht im VEC geladen wird. Führen Sie einen der folgenden Schritte aus, wenn Kopfzeilen mit [!DNL Requestly] entfernt werden müssen:

* Fügen Sie URL-Regeln für die URL hinzu, die in Visual Experience Composer geöffnet werden soll, sodass Header nur für diese URLs entfernt werden.
* Aktivieren Sie die Regel während der Bearbeitung im VEC und deaktivieren Sie die Regel, wenn der VEC nicht verwendet wird.

+++

+++ Multi-Level-iFrames werden nicht unterstützt

[!DNL Target] unterstützt keine iFrames mit mehreren Ebenen. Wenn die Website einen iframe lädt, der einen untergeordneten iframe hat, interagiert at.js nur mit dem übergeordneten iframe. [!DNL Target] Bibliotheken interagieren nicht mit dem untergeordneten iframe.

Fügen Sie als Problemumgehung eine Seite im -Erlebnis mit der URL des untergeordneten iFrames hinzu.

+++

+++ Erlebnisse können ohne die [!DNL Target] Implementierung nicht auf einer iFrame-Busting-Site oder auf Seiten bearbeitet werden

Aktivieren Sie **[!UICONTROL Enhanced Experience Composer (]**), um dieses Problem zu beheben. Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** und aktivieren Sie dann das Kontrollkästchen, um den **[!UICONTROL Enhanced Experience Composer]** zu aktivieren.

Der EEC verwendet einen [!DNL Adobe] verwalteten Proxy, um die Seite zur Bearbeitung zu laden. Dieser Proxy ermöglicht die Bearbeitung auf iFrame-Busting-Sites sowie auf Sites und Seiten, auf denen [!DNL Adobe Target] Code noch nicht hinzugefügt wurde. Solange kein Code hinzugefügt wurde, liefern die Aktivitäten nicht an die Site. Einige Websites werden möglicherweise nicht über den EEC geladen. In diesem Fall wird die Seite über einen iFrame geladen, wenn Sie diese Option deaktivieren.

>[!NOTE]
>
>Lokal gehostete Seiten und Seiten, die außerhalb des Netzwerks nicht zugänglich sind, sind für den [!DNL Adobe]-Proxy-Server nicht zugänglich und können nicht in EEC geöffnet werden. Diese Seiten können Staging-URLs, Akzeptanztest-URLs (UAT) oder lokal gehostete Seiten enthalten.

+++

## Laden und Anzeigen von Seiten

+++ Bei der Bearbeitung einer Seite wird anstelle der Seite ein Drehfeld angezeigt

Dies kann vorkommen, wenn die URL ein #-Zeichen enthält. Um das Problem zu beheben, wechseln Sie in VEC oder EEC in den **[!UICONTROL Durchsuchen]**-Modus und dann zurück in den **[!UICONTROL Erstellen]**-Modus. Das Netz sollte verschwinden und die Seite sollte angezeigt werden.

+++

+++ Der VEC oder EEC scheint fehlerhaft zu sein oder wird nicht initialisiert, wenn eine gespeicherte Aktivität erneut bearbeitet wird

Wenn sich die Website außerhalb von VEC geändert hat, nachdem das Erlebnis definiert wurde, können die Selektoren, für die zuvor Aktionen durchgeführt wurden, nicht gefunden werden, wenn die Aktivität zur erneuten Bearbeitung geöffnet wird. Die Seite erscheint beschädigt und es werden keine Warnungen eingeblendet.

+++

+++ Rotierende Banner und andere Inhalte, die JavaScript enthalten, werden in VEC oder EEC nicht angezeigt

Standardmäßig blockiert der VEC JavaScript-Elemente. Durch Deaktivieren von JavaScript können diese Elemente verwendet werden. Je nach Einrichtung der Site werden einige Elemente möglicherweise weiterhin falsch angezeigt oder sind nicht verfügbar.

+++

+++ Bei Automated Personalization-Aktivitäten scheint der Bildaustausch im VEC oder EEC fehlerhaft zu sein

Das Hinzufügen eines Bildangebots zu einem Pfad erfordert die vollständige Dimension des ursprünglichen Bildplatzes im VEC oder EEC. Bei der Bereitstellung wird das Bild nicht erweitert, sondern wie vorhanden angezeigt, sodass die Bereitstellung nicht beeinträchtigt wird.

+++

## Bearbeiten der Ergebnisse

+++ Durch Ändern eines Elements auf der Seite werden mehrere Elemente geändert

Wenn für mehrere Elemente auf der Seite die gleiche DOM-Element-ID verwendet wird, werden beim Ändern eines dieser Elemente alle Elemente mit dieser ID geändert. Um dies zu verhindern, verwenden Sie auf jeder Seite eine ID nur einmal. Dies ist eine übliche Best Practice für HTML. Weitere Informationen finden Sie unter [Szenarien für die Seitenmodifizierung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#vec-scenarios).

+++

+++ Textstile, die fett und kursiv formatiert sind, werden nach dem Anwenden von Text bearbeiten/HTML bearbeiten oder Text ändern/HTML ändern nicht angezeigt oder der Text verschwindet

Wenn **[!UICONTROL Text bearbeiten]**/**[!UICONTROL HTML bearbeiten]** im VEC für **[!UICONTROL A/B-Test]**- oder **[!UICONTROL Experience Targeting]**-Aktivitäten verwendet wird oder **[!UICONTROL Text ändern]**/**[!UICONTROL HTML ändern]** für **[!UICONTROL Automated Personalization]**- oder **[!UICONTROL Multivarianz-Test]**-Aktivitäten verwendet wird, um Text fett oder kursiv zu formatieren, werden die Stile möglicherweise nicht auf die Seite angewendet, oder der Text verschwindet auf der Seite im VEC. Dies geschieht, weil die Art und Weise, wie der Rich-Text-Editor diese Stile anwendet, das Website-Markup beeinträchtigen kann.

Wenn dieses Problem auftritt:

1. Klicken Sie im Richt-Text-Editor auf die Schaltfläche **[!UICONTROL HTML]**, um in den Quellbearbeitungsmodus zu wechseln.
1. Suchen Sie die formatierten Textelemente.

   * Für fett gedruckten Text ändern Sie `<strong>`-Elemente zu `<b>`.
   * Für kursiv gedruckten Text ändern Sie `<em>`-Elemente zu `<i>`.

+++
