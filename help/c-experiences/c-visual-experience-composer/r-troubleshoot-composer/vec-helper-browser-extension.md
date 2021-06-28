---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
description: Erfahren Sie, warum einige Websites im Visual Experience Composer (VEC) möglicherweise nicht zuverlässig geöffnet werden. Mit der VEC Helper-Browsererweiterung können Sie Websites zuverlässig in VEC laden.
title: Wie verwende ich die Visual Experience Composer (VEC) Helper-Erweiterung?
feature: 'Visual Experience Composer (VEC)  '
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 52%

---

# Visual Experience Composer Helper-Erweiterung

Mit der Browsererweiterung [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper für Google Chrome können Sie Websites zuverlässig im VEC laden, um schnell Web-Erlebnisse zu erstellen und zu überprüfen.

>[!NOTE]
>
>Der VEC Helper-Browser ist eine Chrome-Erweiterung. Diese Erweiterung ist bei Verwendung von Mozilla Firefox nicht erforderlich.

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die at.js-Bibliothek ist auf der Website noch nicht implementiert.
* Die QA- und/oder Test-Site des Kunden kann extern nicht abgerufen werden (interne Site).
* Sie verwenden Google Chrome 80+ mit verbesserten SameSite-Cookie-Durchsetzungsrichtlinien. Weitere Informationen finden Sie unter [Wie wirken sich die kürzlich angekündigten Google Chrome SameSite-Cookie-Durchsetzungsrichtlinien auf VEC und EEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite) aus?

Die VEC Helper-Browsererweiterung für Chrome löst Probleme beim Laden von Sites, für die Kunden jetzt die [!DNL Target] [Enhanced Experience Composer](/help/administrating-target/visual-experience-composer-set-up.md#eec) oder Drittanbietererweiterungen wie Requestly benötigen.

## Vorteile der Verwendung der VEC Helper-Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie X-Frame-Options und Content-Sicherheitsrichtlinien werden implizit von der Website entfernt. Es ist nicht mehr erforderlich, komplizierte Requestly-Regeln zu erstellen.
* Wenn eine Webseite noch nicht die [!DNL Target]-JavaScript-Bibliothek at.js enthält, können Sie die Erweiterung verwenden, um die Bibliothek einzufügen, sodass Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

   Beachten Sie, dass die Erweiterung mit dem Enhanced Experience Composer (EEC) at.js nicht injiziert, aber die SameSite-Cookie-Funktion weiterhin vorhanden ist. Um at.js auf die Webseite zu injizieren, deaktivieren Sie den EEC.

* [Mobile ](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) Viewports werden auch ohne  [!UICONTROL Enhanced Experience Composer]  (EEC) unterstützt.
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

1. Navigieren Sie zur Browsererweiterung [Adobe Target VEC Helper im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klicken Sie auf **[!UICONTROL Zu Chrome hinzufügen > Erweiterung hinzufügen]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie in der Symbolleiste des Chrome-Browsers auf das VEC Helper-Symbol (![VEC Helper-Symbol](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)), während Sie sich im VEC oder [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) befinden.
1. (Bedingt) Schieben Sie den Umschalter **[!UICONTROL Target-Bibliotheken einfügen]** an die Position &quot;Ein&quot;, wenn die Webseite noch nicht die JavaScript-Bibliothek [!DNL Target] at.js enthält.

   Die folgende Abbildung zeigt den VEC Helper mit aktivierter Einstellung [!UICONTROL Target-Bibliotheken injizieren]:

   ![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   Die folgende Abbildung zeigt den VEC Helper an mit der Frage, ob Sie [!DNL Target]-Bibliotheken auf der Seite einfügen möchten, um Authoring zu ermöglichen:

   ![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Bedingt) Schalten Sie den Umschalter **[!UICONTROL Cookies]** in die &quot;Ein&quot;-Position, um automatisch die Attributbrowser-Korrektur SameSite=None hinzuzufügen, und geben Sie dann den Cookie-Namen und die Domäne an.

   ![Umschalten von Cookies in der VEC Helper-Erweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Die folgenden Links bieten zusätzliche Informationen:

   * Weitere Informationen zur Fehlerbehebung beim Attributbrowser SameSite=None finden Sie unter &quot;Wie wirken sich die kürzlich angekündigten Richtlinien zur Durchsetzung von SameSite-Cookies in Google Chrome auf VEC und EEC aus?&quot; [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite) unter der Frage „Wie wirken sich die kürzlich von Google Chrome angekündigten Cookie-Durchsetzungsrichtlinien für SameSite auf VEC und EEC aus?“.

   * Der Cookie-Name ist &quot;mbox&quot;und die Cookie-Domäne ist die zweite und oberste Ebene der Domänen, von denen Sie die Mbox beliefern. Da die Belieferung von der Domäne Ihres Unternehmens stattfindet, handelt es sich um ein Erstanbieter-Cookie. Beispiel: `mycompany.com`. Weitere Informationen finden Sie unter [Adobe Target-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html?lang=de) im *Experience Cloud Interface-Benutzerhandbuch*.

## Hinweise

* Die Markierung [!UICONTROL Ziel-Bibliotheken einfügen] ist in der Erweiterung standardmäßig DEAKTIVIERT. Sie können diese Markierung aktivieren, wenn Sie VEC auf einer Site verwenden möchten, für die [!DNL Target] noch nicht implementiert wurde.

   Diese Markierung ist eine globale Einstellung. Sie wird für alle im VEC geöffneten Websites aktiviert bzw. deaktiviert. Wenn Sie diese Markierung beispielsweise auf &quot;ein&quot;setzen und eine Website öffnen, die bereits mit at.js implementiert ist, erhalten Sie eine Nachricht, dass at.js bereits geladen ist. Adobe geht davon aus, dass die meisten Kunden bereits at.js auf ihren Seiten implementiert haben, und verwendet die Standardeinstellung &quot;Aus&quot;.

* Die Erweiterung lädt die neueste Version von at.js, die unter [!DNL Target UI] unter [!UICONTROL Administration > Implementierung] verfügbar ist.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, dies aber fehlschlägt, wird eine Meldung angezeigt, die empfiehlt, die VEC Helper-Browsererweiterung zu installieren.
   * Wenn at.js auf der Website noch nicht implementiert wurde, wird in VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.
   * Wenn die Erweiterung aktiviert ist und das Laden durchführt, werden Meldungen angezeigt, wenn die Erweiterung die at.js-Bibliothek einfügt (falls erforderlich) bzw. dabei hilft, die Website zuverlässig im VEC zu öffnen.
