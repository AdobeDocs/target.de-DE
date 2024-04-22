---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
description: Erfahren Sie, warum einige Websites möglicherweise nicht zuverlässig in der [!UICONTROL Visual Experience Composer] (VEC). Mit der VEC Helper-Browsererweiterung können Sie Websites zuverlässig in VEC laden.
title: Wie verwende ich die [!UICONTROL Visual Experience Composer] (VEC) Helper Extension?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: 8edae6a197a3ac82b85fcce4d99c8b0d5f45c712
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 48%

---

# [!UICONTROL Visual Experience Composer] Helper-Erweiterung

Die [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper-Browsererweiterung für [!DNL Google Chrome] Sie können Websites zuverlässig im VEC laden, um schnell und einfach Web-Erlebnisse zu erstellen und zu überprüfen.

Der VEC Helper-Browser ist ein [!DNL Chrome] -Erweiterung. Diese Erweiterung ist bei Verwendung von [!DNL Mozilla Firefox].

>[!IMPORTANT]
>
>Die aktuelle [!DNL Target] Die in diesem Artikel dokumentierte VEC Helper-Erweiterung wurde mit Manifest v2 erstellt. Google hat kürzlich angekündigt, dass ab Juni 2024 keine neuen Erweiterungen mehr zugelassen werden, die mit Manifest v2 erstellt wurden. Weitere Informationen finden Sie unter [Mitteilung zur Unterstützung der Zeitleiste für Manifest V2](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} von [!DNL Google] auf *Chrome für Entwickler* Site.
>
>Die vorhandene Erweiterung funktioniert weiterhin in Google Chrome. Ab Juni 2024 [!DNL Adobe] beginnt mit der Deaktivierung der in diesem Thema dokumentierten Helper-Erweiterung und fordert von den Kunden den Wechsel zur neueren [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).
>
Sie werden über Versionshinweise, eine Produktankündigung und Text in diesem Artikel benachrichtigt, wenn diese Erweiterung nicht mehr funktioniert. Aufgrund von Sicherheitsverbesserungen in Manifest v3, [!DNL Adobe] erfordert das Herunterladen der neuen Erweiterung, um Ihre Websites weiterhin visuell in [!DNL Target].

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die at.js-Bibliothek ist auf der Website noch nicht implementiert.
* Die QA- oder Status-Site von Kundinnen und Kunden kann extern nicht abgerufen werden (interne Site).
* Es gibt einige aktuelle Einschränkungen beim Versuch, VEC zum Öffnen einer Website zu verwenden, die [Servicepersonal](https://developer.mozilla.org/de/docs/Web/API/Service_Worker_API){target=_blank} (SW)

Ein SW ist eine Web-Technologie, mit der Anforderungen durch eine Web-Seite für die Domain abgefangen werden können, auf der sie installiert sind. Der SW überlebt den Seitenbesuch und aktiviert sich selbst bei nachfolgenden Besuchen. Der SW entscheidet, welche Anforderungen durchlaufen werden und welche stattdessen abgefangen und aus einem Cache bereitgestellt werden.

Der SW kann die Zwischenspeicherung steuern und die Web-Seite selbst zwischenspeichern sowie auch statische Ressourcen wie JS, CSS, IMG, AJAX-Anfragen, deren Inhalte und deren Antwort-Header, einschließlich der Header, die unsere [Target VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) zu entfernen versucht, z. B. X-Frame-Optionen: SAMEORIGIN, CSP (Content-Security-Policy) oder Set-Cookie.

Leider erhalten die Chrome-Erweiterungs-APIs, die Webanfragen abfangen, nicht die Anfragen, die von einer SW abgefangen und verarbeitet wurden. Daher kann die Erweiterung die Kopfzeilen und Cookies nicht beheben, wenn die Webseitenanforderung von einer SW aus aus dem Cache bereitgestellt wurde, da die Web-Seite aufgrund der X-Frame-Options- oder CSP-Kopfzeilen, die ebenfalls zwischengespeichert wurden, nicht im VEC geladen wird.

Als potenzielle Problemumgehung können Sie Service Workers auf der Registerkarte Chrome Developer Tools > Anwendung deaktivieren und dann das Kontrollkästchen &quot;Für Netzwerk umgehen&quot;im Abschnitt Service Workers aktivieren.

* Sie verwenden Google Chrome 80+ mit verbesserten SameSite-Cookie-Durchsetzungsrichtlinien. Weitere Informationen finden Sie unter [Wie wirken sich die kürzlich angekündigten Durchsetzungsrichtlinien für Google Chrome SameSite-Cookies auf VEC und EEC aus?](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

Die VEC Helper-Browsererweiterung für Chrome löst Probleme beim Laden von Sites, für die Kunden jetzt die Funktion [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder Drittanbietererweiterungen, z. B. Requestly.

## Vorteile der Verwendung der VEC Helper-Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie X-Frame-Options und Content-Sicherheitsrichtlinien werden implizit von der Website entfernt. Es ist nicht mehr erforderlich, komplizierte Requestly-Regeln zu erstellen.
* Wenn eine Webseite noch nicht die [!DNL Target]-JavaScript-Bibliothek at.js enthält, können Sie die Erweiterung verwenden, um die Bibliothek einzufügen, sodass Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

  Beachten Sie, dass die Erweiterung mit dem Enhanced Experience Composer (EEC) at.js nicht injiziert, aber die SameSite-Cookie-Funktion weiterhin vorhanden ist. Um at.js auf der Webseite einzubinden, schalten Sie den EEC aus.

* [Mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne die [!UICONTROL Enhanced Experience Composer] (EWG).
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

1. Navigieren Sie zum [Adobe Target VEC Helper-Browsererweiterung im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klicken Sie auf **[!UICONTROL Add to Chrome > Add Extension]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie in der Symbolleiste des Chrome-Browsers auf das VEC Helper-Symbol (![VEC Helper-Symbol](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)), während Sie sich im VEC oder [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) befinden.
1. (Bedingt) Schieben Sie die **[!UICONTROL Inject Target Libraries]** wird zur Position &quot;Ein&quot;umgeschaltet, wenn die Webseite noch nicht enthält. [!DNL Target] at.js-JavaScript-Bibliothek.

   Die folgende Abbildung zeigt den VEC Helper mit der [!UICONTROL Inject Target Libraries] Einstellung aktiviert:

   ![VEC Helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   Die folgende Abbildung zeigt den VEC Helper an mit der Frage, ob Sie [!DNL Target]-Bibliotheken auf der Seite einfügen möchten, um Authoring zu ermöglichen:

   ![VEC Helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Bedingt) Schieben Sie die **[!UICONTROL Cookies]** Umschalten auf die Position &quot;Ein&quot;, um automatisch die `SameSite=None` -Attribut-Browser-Korrektur.

   ![Umschalten von Cookies in der VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Weitere Informationen zur Browser-Fehlerbehebung für das `SameSite=None`-Attribut finden Sie unter „Wie wirken sich die kürzlich angekündigten Richtlinien zur Durchsetzung von SameSite-Cookies in Google Chrome auf den VEC und EEC aus?“ in [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Hinweise

* Die [!UICONTROL Inject Target libraries] -Markierung in der -Erweiterung ist standardmäßig DEAKTIVIERT. Sie können diese Markierung aktivieren, wenn Sie VEC auf einer Site verwenden möchten, für die [!DNL Target] noch nicht implementiert wurde.

  Diese Markierung ist eine globale Einstellung. Sie wird für alle im VEC geöffneten Websites aktiviert bzw. deaktiviert. Wenn Sie diese Markierung beispielsweise auf &quot;ein&quot;setzen und eine Website öffnen, die bereits mit at.js implementiert ist, erhalten Sie eine Nachricht, dass at.js bereits geladen ist. Adobe geht davon aus, dass die meisten Kunden bereits at.js auf ihren Seiten implementiert haben, und verwendet die Standardeinstellung &quot;Aus&quot;.

* Die -Erweiterung lädt die neueste Version von at.js, die im Abschnitt [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, dies aber fehlschlägt, wird eine Meldung angezeigt, die empfiehlt, die VEC Helper-Browsererweiterung zu installieren.
   * Wenn at.js auf der Website noch nicht implementiert wurde, wird in VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.
   * Wenn die Erweiterung aktiviert ist und das Laden durchführt, werden Meldungen angezeigt, wenn die Erweiterung die at.js-Bibliothek einfügt (falls erforderlich) bzw. dabei hilft, die Website zuverlässig im VEC zu öffnen.
