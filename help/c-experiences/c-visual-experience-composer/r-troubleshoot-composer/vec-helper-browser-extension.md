---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
description: Informationen zur Verwendung der Adobe Target Visual Experience Composer (VEC) Helper-Browsererweiterung, um Websites zuverlässig innerhalb von VEC zu laden und so schnell Erlebnisse zu erstellen und zu überprüfen.
title: Visual Experience Composer (VEC) Helper Extension
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 56%

---


# Visual Experience Composer Helper-Erweiterung

Mit der Helper-Browser-Erweiterung [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) für Google Chrome können Sie Websites zuverlässig innerhalb des VEC laden, um Web-Erlebnisse schnell zu erstellen und zu überprüfen.

>[!NOTE]
>
>Der VEC Helper Browser ist eine Chrome-Erweiterung. Diese Erweiterung ist bei der Verwendung von Mozilla Firefox nicht erforderlich.

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die at.js-Bibliothek ist auf der Website noch nicht implementiert.
* Die QA- und/oder Test-Site des Kunden kann extern nicht abgerufen werden (interne Site).
* Sie verwenden Google Chrome 80+ mit erweiterten Richtlinien zur Durchsetzung von SameSite-Cookies. Weitere Informationen finden Sie unter [Wie wirken sich die kürzlich angekündigten Google Chrome SameSite-Cookie-Durchsetzungsrichtlinien auf VEC und EEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite) aus?

Die VEC Helper-Browsererweiterung für Chrome löst Site-Ladeprobleme, bei denen Kunden jetzt auf die Erweiterungen [!DNL Target] [Enhanced Experience Composer](/help/administrating-target/visual-experience-composer-set-up.md#eec) oder Drittanbieter wie Requestly angewiesen sind.

## Vorteile der Verwendung der VEC Helper-Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie X-Frame-Options und Content-Sicherheitsrichtlinien werden implizit von der Website entfernt. Hierfür müssen keine komplizierten Regeln für Requestly mehr erstellt werden.
* Wenn eine Webseite noch nicht die [!DNL Target]-JavaScript-Bibliothek at.js enthält, können Sie die Erweiterung verwenden, um die Bibliothek einzufügen, sodass Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

   Beachten Sie, dass bei der Verwendung des Enhanced Experience Composer (EEC) die Erweiterung &quot;at.js&quot;nicht injiziert, aber die Funktion &quot;SameSite-Cookie&quot;weiterhin vorhanden ist. Um at.js auf die Webseite zu injizieren, deaktivieren Sie die EWG.

* [Mobile ](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) Viewports werden auch ohne den  [!UICONTROL Enhanced Experience Composer]  (EEC) unterstützt.
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

1. Navigieren Sie zur Browsererweiterung [Adobe Target VEC Helper im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klicken Sie auf **[!UICONTROL Zu Chrome hinzufügen > Erweiterung hinzufügen]**.
1. Öffnen Sie die VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie in der Symbolleiste des Chrome-Browsers auf das VEC Helper-Symbol (![VEC Helper-Symbol](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)), während Sie sich im VEC oder [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) befinden.
1. (Bedingt) Schieben Sie den Umschalter **[!UICONTROL Zielgruppe-Bibliotheken einfügen]** an die &quot;on&quot;-Position, wenn die Webseite noch nicht die JavaScript-Bibliothek [!DNL Target] at.js enthält.

   Die folgende Abbildung zeigt den VEC Helper mit aktivierter Einstellung [!UICONTROL Target-Bibliotheken injizieren]:

   ![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   Die folgende Abbildung zeigt den VEC Helper an mit der Frage, ob Sie [!DNL Target]-Bibliotheken auf der Seite einfügen möchten, um Authoring zu ermöglichen:

   ![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Bedingt) Schieben Sie den Umschalter **[!UICONTROL Cookies]** zur &quot;on&quot;-Position, um automatisch die Fehlerbehebung für das Attribut &quot;SameSite=None&quot;hinzuzufügen, und geben Sie dann den Cookie-Namen und die Domäne an.

   ![Cookies in der VEC Helper Extension](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Die folgenden Links bieten zusätzliche Informationen:

   * Weitere Informationen zur Fehlerbehebung für den Browser des Attributs &quot;SameSite=None&quot;finden Sie unter Wie wirken sich die kürzlich angekündigten Google Chrome SameSite-Cookie-Durchsetzungsrichtlinien auf VEC und EEC aus? in [Fehlerbehebung bei Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

   * Der Cookie-Name ist &quot;mbox&quot;und die Cookie-Domäne ist die zweite und oberste Ebene der Domänen, von denen Sie die mbox beliefern. Da die Belieferung von der Domäne Ihres Unternehmens stattfindet, handelt es sich um ein Erstanbieter-Cookie. Beispiel: `mycompany.com`. Weitere Informationen finden Sie unter [Adobe Target Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html) im *Experience Cloud-Benutzeroberfläche Benutzerhandbuch*.

## Hinweise

* Ihre Implementierung muss die [!DNL Target]-at.js-Bibliothek verwenden. Sie können keine mbox.js-Implementierung mit der Erweiterung verwenden.
* Die Markierung [!UICONTROL Ziel-Bibliotheken einfügen] ist in der Erweiterung standardmäßig DEAKTIVIERT. Sie können diese Markierung aktivieren, wenn Sie VEC auf einer Site verwenden möchten, für die [!DNL Target] noch nicht implementiert wurde.

   Beachten Sie, dass diese Markierung eine globale Einstellung ist. Sie wird für alle im VEC geöffneten Websites aktiviert bzw. deaktiviert. Wenn Sie dieses Flag beispielsweise auf &quot;on&quot;setzen und eine Website öffnen, die bereits mit &quot;at.js&quot;implementiert ist, erhalten Sie eine Meldung, dass &quot;at.js&quot;bereits geladen ist. Wir gehen davon aus, dass die meisten Kunden at.js bereits auf ihren Seiten implementiert haben und die Standardeinstellung &quot;off&quot;verwenden werden.

* Die Erweiterung lädt die neueste Version von at.js, die unter [!DNL Target UI] unter [!UICONTROL Administration > Implementierung] verfügbar ist.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, dies aber fehlschlägt, wird eine Meldung angezeigt, die empfiehlt, die VEC Helper-Browsererweiterung zu installieren.
   * Wenn at.js auf der Website noch nicht implementiert wurde, wird in VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.
   * Wenn die Erweiterung aktiviert ist und das Laden durchführt, werden Meldungen angezeigt, wenn die Erweiterung die at.js-Bibliothek einfügt (falls erforderlich) bzw. dabei hilft, die Website zuverlässig im VEC zu öffnen.

