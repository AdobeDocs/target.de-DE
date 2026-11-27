---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
description: Finden Sie heraus, warum manche Websites nicht zuverlässig im [!UICONTROL Visual Experience Composer] (VEC) geöffnet werden. Mit der VEC Helper-Browser-Erweiterung können Sie Websites zuverlässig innerhalb des VEC laden.
title: Wie verwende ich die [!UICONTROL Visual Experience Composer] (VEC) Helper-Erweiterung?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
TQID: 'https://experienceleague.adobe.com/lqZGGWG1NVtKDzNGPq5k2bDPzxDfNWqPtJ-bYfLCr3Q'
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
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
    internal-label: Web experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 5%
---
# [!UICONTROL Visual Experience Composer] Helper-Erweiterung {#vec-helper-extension}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie die veraltete Browser-Erweiterung „VEC Helper“ Websites in **[!UICONTROL Visual Experience Composer]** (VEC) lädt und wie Sie sie installieren und verwenden.

>[!ENDSHADEBOX]

Die [!DNL Adobe Target] **[!UICONTROL Visual Experience Composer]** (VEC) Helper-Browser-Erweiterung für [!DNL Google Chrome] lädt Websites zuverlässig im VEC, wodurch das Erstellen und Überprüfen von Web-Erlebnissen beschleunigt wird. Die Erweiterung ist in [!DNL Mozilla Firefox] nicht erforderlich.

>[!IMPORTANT]
>
>* Die in diesem Artikel dokumentierte veraltete [!DNL Target] VEC Helper-Erweiterung wurde mit Manifest V2 erstellt. [!DNL Google] kündigte an, ab Juni 2024 keine Erweiterungen mehr zuzulassen, die mit Manifest V2 erstellt wurden. Weitere Informationen finden Sie in der Ankündigung [Manifest v2-Unterstützung](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} von [!DNL Google] auf der *Chrome for Developers*-Site.
>
>* Ab Juni 2024 deaktiviert [!DNL Google] Erweiterungen, die mit Manifest V2 erstellt wurden, einschließlich der in diesem Artikel dokumentierten Erweiterung. [!DNL Adobe] empfiehlt, so bald wie möglich zur neueren [Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)Erweiterung zu wechseln.

## Warum einige Websites nicht zuverlässig im VEC geöffnet werden

Eine Website wird möglicherweise aus den folgenden Gründen nicht zuverlässig im VEC geöffnet:

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die at.js-Bibliothek ist auf der Website noch nicht implementiert.
* Die QA- oder Staging-Site des Kunden ist intern und außerhalb des Netzwerks nicht verfügbar.
* Die Website verwendet [Service Workers](https://developer.mozilla.org/de/docs/Web/API/Service_Worker_API){target=_blank} (SW), die der VEC derzeit nur mit Einschränkungen unterstützt. Siehe folgenden Abschnitt.
* Die Website wird ab [!DNL Chrome] 80 geöffnet. Dadurch werden die SameSite-Cookie-Richtlinien erzwungen. Weitere Informationen finden Sie unter [SameSite-Cookie-Richtlinien für Google Chrome](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

Die VEC Helper-Browser-Erweiterung für [!DNL Chrome] löst die Probleme beim Laden von Websites, für die Kundinnen und Kunden ansonsten auf den [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder auf Erweiterungen von Drittanbietern wie Requestly angewiesen sind.

### Servicemitarbeiter

Ein Service Worker (SW) ist eine Web-Technologie, die von einer Web-Seite installiert wird, um die Anforderungen für ihre Domain abzufangen. Der SW überlebt den Seitenbesuch und aktiviert sich selbst bei nachfolgenden Besuchen. Er entscheidet, welche Anforderungen durchlaufen werden und welche abgefangen und aus einem Cache bereitgestellt werden.

Ein SW kann die Web-Seite selbst zwischenspeichern sowie statische Ressourcen wie JS-, CSS-, IMG- und AJAX-Anfragen, deren Inhalte und deren Antwort-Header. Zu diesen Kopfzeilen gehören die Kopfzeilen, die die [Target VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) entfernen versucht, z. B. `X-Frame-Options: SAMEORIGIN`, CSP (`Content-Security-Policy`) und `Set-Cookie`.

Die [!DNL Chrome]-Erweiterungs-APIs, die Web-Anfragen abfangen, empfangen nicht die Anfragen, die ein SW abgefangen und verarbeitet hat. Wenn ein SW die Web-Seitenanfrage aus einem Cache bereitstellt, kann die Erweiterung daher die Header und Cookies nicht beheben, und die Seite wird aufgrund der zwischengespeicherten `X-Frame-Options`- oder CSP-Header nicht im VEC geladen.

Deaktivieren Sie als potenzielle Problemumgehung die Service Workers auf der Registerkarte &quot;[!DNL Chrome] Developer Tools“ > **Anwendung** und aktivieren Sie dann das Kontrollkästchen „Für Netzwerk umgehen“ im Abschnitt „Service Workers“.

## Vorteile der VEC Helper-Erweiterung

* **Iframe-Busting-Kopfzeilen entfernt:** die Erweiterung entfernt Kopfzeilen wie `X-Frame-Options` und `Content-Security-Policy` implizit von der Website, sodass keine komplizierten Requestly-Regeln erforderlich sind.
* **at.js-Injektion:** Wenn eine Webseite noch nicht die [!DNL Target] at.js-JavaScript-Bibliothek enthält, kann sie von der Erweiterung eingefügt werden. Anschließend können Erlebnisse für die Website erstellt und die Aktivitäten mit Vorschau-Links erstellt und geprüft werden. Beim Enhanced Experience Composer (EEC) wird at.js von der Erweiterung zwar nicht eingefügt, aber die SameSite Cookie-Funktionalität bleibt erhalten. Um at.js auf der Webseite einzubinden, schalten Sie den EEC aus.
* **Mobile Viewports:** [mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne den **[!UICONTROL Enhanced Experience Composer]** (EEC) unterstützt.
* **Neue [!DNL Target]-Kunden:** Die Erweiterung ermöglicht es, mit [!DNL Target] zu experimentieren, auch wenn die IT-Entwickler [!DNL Target] noch nicht auf der Website implementiert haben.
* **Partner:** Partner, die die Websites und [!DNL Target]-Konten mehrerer Kunden betreuen, erhalten einen Mechanismus zur Unterstützung des VEC-Ladevorgangs anstelle mehrerer Regeln in Drittanbieter-Tools.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

Durch das Installieren der Erweiterung in [!DNL Chrome] können Websites zuverlässig in VEC geladen werden, einschließlich Websites, die iFrames blockieren oder auf denen at.js noch nicht implementiert ist.

1. Wechseln Sie zur Browser-Erweiterung [Adobe Target VEC Helper im Chrome Web Store](https://chromewebstore.google.com/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca).
1. Klicken Sie **[!UICONTROL Zu Chrome hinzufügen]** > **[!UICONTROL Erweiterung hinzufügen]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Klicken Sie im VEC- oder [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) auf das Symbol der Browser-Erweiterung für VEC Helper ![VEC Helper-Symbol](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) ) in der Symbolleiste von [!DNL Chrome].
1. (Bedingt) Wenn die Web-Seite noch nicht die [!DNL Target] at.js-JavaScript-Bibliothek enthält, schalten Sie den **[!UICONTROL Target-Bibliotheken einfügen]** ein.

   Die folgende Abbildung zeigt den VEC Helper mit aktivierter Einstellung **[!UICONTROL Target-Bibliotheken]**:

   ![VEC Helper-Erweiterungsbedienfeld mit dem Umschalter Target-Bibliotheken einfügen und dem Umschalten von Cookies , was zeigt, dass die Cookie-Einstellung für alle Cookies für Anfragen innerhalb des VEC die Flags SameSite=None und Secure festlegt](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   Der VEC Helper fragt dann, ob die [!DNL Target] Bibliotheken in die Seite eingefügt werden sollen, um das Authoring zu ermöglichen:

   ![Inject Target Libraries zeigt an, dass die Target VEC Helper-Erweiterung Target-Bibliotheken mithilfe der Schaltflächen Abbrechen und Zulassen in die Seite einfügen möchte, um das Authoring zu aktivieren](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Bedingt) Schalten Sie den Umschalter **[!UICONTROL Cookies]** ein, um die Browser-Fehlerbehebung für das `SameSite=None`-Attribut automatisch hinzuzufügen.

   ![VEC Helper-Erweiterungsbedienfeld mit aktiviertem Umschalter „Cookies“ und hervorgehobener Option „Visual Experience Composer“ mit Beispielseite](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Weitere Informationen zur Browser-Fehlerbehebung für das `SameSite=None` finden Sie unter [Google Chrome SameSite-Cookie-Richtlinien](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Nutzungshinweise

* Das Flag **[!UICONTROL Target-Bibliotheken einfügen]** in der Erweiterung ist standardmäßig deaktiviert. Aktivieren Sie sie, um VEC auf einer Site zu verwenden, auf der [!DNL Target] noch nicht implementiert ist.

  Das Flag ist eine globale Einstellung, sodass es für alle im VEC geöffneten Websites aktiviert oder deaktiviert ist. Wenn das Flag beispielsweise eingeschaltet ist, wird beim Öffnen einer Website, auf der at.js bereits implementiert ist, eine Meldung angezeigt, dass at.js bereits geladen ist. [!DNL Adobe] erwartet, dass die meisten Kundinnen und Kunden auf ihren Seiten bereits at.js implementiert haben und die Standardeinstellung „off“ verwenden.

* Die Erweiterung lädt die neueste Version von at.js, die in der [!DNL Target]-Benutzeroberfläche unter **[!UICONTROL Administration]** > **[!UICONTROL Implementierung)]**.
* Um at.js mithilfe der Erweiterung im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der die Aktivität erstellt wurde.
* VEC zeigt Meldungen in den folgenden Fällen an:

  * Eine Website kann nicht in VEC geladen werden. In der Meldung wird vorgeschlagen, die Browser-Erweiterung VEC Helper zu installieren.
  * at.js ist noch nicht auf der Website implementiert. In der Meldung wird vorgeschlagen, die Erweiterung zu installieren.
  * Die Erweiterung ist aktiviert und sorgt für das Laden. Die Meldungen werden angezeigt, wenn die Erweiterung die at.js-Bibliothek bei Bedarf einfügt oder beim zuverlässigen Öffnen der Website in VEC hilft.
