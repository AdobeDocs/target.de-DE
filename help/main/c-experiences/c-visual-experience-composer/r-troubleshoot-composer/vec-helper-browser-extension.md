---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
description: Finden Sie heraus, warum manche Websites in [!UICONTROL Visual Experience Composer] (VEC) möglicherweise nicht zuverlässig geöffnet werden. Mit der VEC Helper-Browser-Erweiterung können Sie Websites zuverlässig innerhalb des VEC laden.
title: Wie verwende ich die [!UICONTROL Visual Experience Composer] (VEC) Helper-Erweiterung?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: c41580bcbecf2eb2c14f13ce8e66e854c655d059
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 55%

---

# [!UICONTROL Visual Experience Composer] Helper-Erweiterung

Mit der Browser-Erweiterung [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper für [!DNL Google Chrome] können Sie Websites zuverlässig innerhalb des VEC laden, um Web-Erlebnisse schnell zu erstellen und zu prüfen.

Der VEC Helper-Browser ist eine [!DNL Chrome]. Diese Erweiterung ist bei Verwendung von [!DNL Mozilla Firefox] nicht erforderlich.

>[!IMPORTANT]
>
>* Die in diesem Artikel dokumentierte veraltete [!DNL Target] VEC Helper-Erweiterung wurde mit Manifest V2 erstellt. [!DNL Google] hat angekündigt, dass mit Manifest V2 erstellte Erweiterungen ab Juni 2024 nicht mehr zulässig sind. Weitere Informationen finden Sie in der Ankündigung [Manifest v2-Unterstützung](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} von [!DNL Google] auf der *Chrome for Developers*-Site.
>
>* Ab Juni 2024 werden [!DNL Google] mit der Deaktivierung von Erweiterungen beginnen, die mit Manifest V2 erstellt wurden, einschließlich der in diesem Thema dokumentierten Erweiterung. [!DNL Adobe] empfiehlt Kundinnen und Kunden, so schnell wie möglich auf die neuere [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) umzusteigen.

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die at.js-Bibliothek ist auf der Website noch nicht implementiert.
* Die QA- oder Status-Site von Kundinnen und Kunden kann extern nicht abgerufen werden (interne Site).
* Es gibt einige aktuelle Einschränkungen beim Versuch, VEC zum Öffnen einer Website zu verwenden, die [Service Workers](https://developer.mozilla.org/de/docs/Web/API/Service_Worker_API){target=_blank} (SW) verwendet.

Ein SW ist eine Web-Technologie, mit der Anforderungen durch eine Web-Seite für die Domain abgefangen werden können, auf der sie installiert sind. Der SW überlebt den Seitenbesuch und aktiviert sich selbst bei nachfolgenden Besuchen. Der SW entscheidet, welche Anforderungen durchlaufen werden und welche stattdessen abgefangen und aus einem Cache bereitgestellt werden.

Der SW kann die Zwischenspeicherung steuern und die Web-Seite selbst zwischenspeichern sowie auch statische Ressourcen wie JS, CSS, IMG, AJAX-Anfragen, deren Inhalte und deren Antwort-Header, einschließlich der Header, die unsere [Target VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) zu entfernen versucht, z. B. X-Frame-Optionen: SAMEORIGIN, CSP (Content-Security-Policy) oder Set-Cookie.

Leider erhalten die Chrome-Erweiterungs-APIs, die Web-Anfragen abfangen, nicht die Anfragen, die von einem SW abgefangen und verarbeitet wurden. Daher kann die Erweiterung die Kopfzeilen und Cookies nicht beheben, wenn die Web-Seitenanforderung von einem SW aus dem Cache bereitgestellt wurde, da die Web-Seite aufgrund der X-Frame-Options- oder CSP-Kopfzeilen, die ebenfalls zwischengespeichert wurden, nicht im VEC geladen wird.

Als potenzielle Problemumgehung können Sie Service Workers auf der Registerkarte &quot;Chrome Developer Tools“ > „Anwendung“ deaktivieren und dann das Kontrollkästchen „Für Netzwerk umgehen“ im Abschnitt „Service Workers“ aktivieren.

* Sie verwenden Google Chrome 80+ mit erweiterten SameSite-Cookie-Durchsetzungsrichtlinien. Weitere Informationen finden Sie unter [Wie wirken sich die kürzlich angekündigten SameSite-Cookie-Richtlinien von Google Chrome auf VEC und EEC aus](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

Die VEC Helper-Browser-Erweiterung für Chrome löst Probleme beim Laden von Websites, für die Kundinnen und Kunden jetzt auf den [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder Erweiterungen von Drittanbietern wie Requestly angewiesen sind.

## Vorteile der Verwendung der VEC Helper-Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie X-Frame-Options und Content-Sicherheitsrichtlinien werden implizit von der Website entfernt. Es besteht keine Notwendigkeit mehr, komplizierte Requestly-Regeln zu erstellen.
* Wenn eine Webseite noch nicht die [!DNL Target]-JavaScript-Bibliothek at.js enthält, können Sie die Erweiterung verwenden, um die Bibliothek einzufügen, sodass Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

  Beachten Sie, dass bei Verwendung des Enhanced Experience Composer (EEC) die Erweiterung at.js zwar nicht einbindet, aber die SameSite Cookie-Funktionalität weiterhin vorhanden ist. Um at.js auf der Webseite einzubinden, schalten Sie den EEC aus.

* [Mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne den [!UICONTROL Enhanced Experience Composer] (EEC) unterstützt. 
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

1. Navigieren Sie zur Browser-Erweiterung [Adobe Target VEC Helper im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klicken Sie auf **[!UICONTROL Add to Chrome > Add Extension]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie in der Symbolleiste des Chrome-Browsers auf das VEC Helper-Symbol (![VEC Helper-Symbol](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)), während Sie sich im VEC oder [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) befinden.
1. (Bedingt) Schieben Sie den **[!UICONTROL Inject Target Libraries]**-Umschalter an die Position „ein“, wenn die Web-Seite noch nicht die [!DNL Target] at.js-JavaScript-Bibliothek enthält.

   Die folgende Abbildung zeigt den VEC Helper mit aktivierter [!UICONTROL Inject Target Libraries]:

   ![VEC Helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   Die folgende Abbildung zeigt den VEC Helper an mit der Frage, ob Sie [!DNL Target]-Bibliotheken auf der Seite einfügen möchten, um Authoring zu ermöglichen:

   ![VEC Helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Bedingt) Schieben Sie den **[!UICONTROL Cookies]**-Umschalter auf die Position „ein“, um die Browser-Fehlerbehebung für das `SameSite=None`-Attribut automatisch hinzuzufügen.

   ![Cookies-Umschalter in der VEC Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Weitere Informationen zur Browser-Fehlerbehebung für das `SameSite=None`-Attribut finden Sie unter „Wie wirken sich die kürzlich angekündigten Richtlinien zur Durchsetzung von SameSite-Cookies in Google Chrome auf den VEC und EEC aus?“ in [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Hinweise

* Das [!UICONTROL Inject Target libraries]-Flag in der Erweiterung ist standardmäßig deaktiviert. Sie können diese Markierung aktivieren, wenn Sie VEC auf einer Site verwenden möchten, für die [!DNL Target] noch nicht implementiert wurde.

  Diese Markierung ist eine globale Einstellung. Sie wird für alle im VEC geöffneten Websites aktiviert bzw. deaktiviert. Wenn Sie beispielsweise diese Markierung auf „Ein“ setzen und eine Website öffnen, die bereits mit at.js implementiert ist, erhalten Sie eine Meldung, die Sie darüber informiert, dass at.js bereits geladen ist. Adobe geht davon aus, dass die meisten Kundinnen und Kunden auf ihren Seiten bereits at.js implementiert haben und die Standardeinstellung „off“ verwenden.

* Die Erweiterung lädt die neueste Version von at.js, die über die [!DNL Target UI] in [!UICONTROL Administration > Implementation] verfügbar ist.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, dies aber fehlschlägt, wird eine Meldung angezeigt, die empfiehlt, die VEC Helper-Browsererweiterung zu installieren.
   * Wenn at.js auf der Website noch nicht implementiert wurde, wird in VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.
   * Wenn die Erweiterung aktiviert ist und das Laden durchführt, werden Meldungen angezeigt, wenn die Erweiterung die at.js-Bibliothek einfügt (falls erforderlich) bzw. dabei hilft, die Website zuverlässig im VEC zu öffnen.
