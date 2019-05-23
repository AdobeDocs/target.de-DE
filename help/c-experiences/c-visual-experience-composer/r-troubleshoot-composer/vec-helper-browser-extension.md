---
description: Informationen zur Verwendung der Visual Experience Composer (VEC) Helper-Browsererweiterung, um Websites zuverlässig innerhalb von VEC zu laden und so schnell Erlebnisse zu erstellen und zu überprüfen.
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
seo-description: Informationen zur Verwendung der Adobe Target Visual Experience Composer (VEC) Helper-Browsererweiterung, um Websites zuverlässig innerhalb von VEC zu laden und so schnell Erlebnisse zu erstellen und zu überprüfen.
seo-title: Adobe Target Visual Experience Composer (VEC) Helper-Erweiterung
solution: Target
title: Visual Experience Composer Helper-Erweiterung
topic: Standard
translation-type: tm+mt
source-git-commit: 46f86cbcfb25efba2c71356fb2defc429535e706

---


# Visual Experience Composer Helper-Erweiterung

Mit der [!DNL Adobe Target] Visual Experience Composer-Erweiterung (VEC) Helper-Browsererweiterung für Google Chrome können Sie Websites zuverlässig im VEC laden, um schnell und einfach Web-Erlebnisse zu erstellen und zu überprüfen.

Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden:

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die at.js-Bibliothek ist auf der Website noch nicht implementiert.
* Die QA- und/oder Test-Site des Kunden kann extern nicht abgerufen werden (interne Site).

Die VEC Helper-Browsererweiterung für Chrome löst Probleme beim Laden von Sites, für die Kunden jetzt den [!DNL Target] [!UICONTROL Enhanced Experience Composer] oder die Erweiterungen von Drittanbietern, z. B. Requestly, verwenden.

Vorteile der Verwendung der VEC Helper-Erweiterung:

* Alle iFrame-Busting-Kopfzeilen wie X-Frame-Options und Content-Sicherheitsrichtlinien werden implizit von der Website entfernt. Hierfür müssen keine komplizierten Regeln für Requestly mehr erstellt werden.
* Wenn eine Website noch nicht die [!DNL Target]-JavaScript-Bibliothek at.js enthält, können Sie die Erweiterung verwenden, um die Bibliothek einzufügen, sodass Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.
* Mobile Viewports werden auch ohne [!UICONTROL Enhanced Experience Composer] (EEC) unterstützt.
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

1. Navigieren Sie zur Browsererweiterung [Adobe Target VEC Helper im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klicken Sie auf [!UICONTROL Zu Chrome hinzufügen &gt; Erweiterung hinzufügen].
1. Um die Erweiterung zu verwenden, klicken Sie in der Symbolleiste des Chrome-Browsers auf das VEC Helper-Symbol (![VEC Helper-Symbol](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)), während Sie sich im VEC oder [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) befinden.

Die folgende Abbildung zeigt den VEC Helper mit aktivierter Einstellung &quot;Target [!UICONTROL -Bibliotheken] Injizieren&quot; :

![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

Die folgende Abbildung zeigt den VEC Helper an, ob Sie Bibliotheken auf der Seite einfügen [!DNL Target] möchten, um Authoring zu ermöglichen:

![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

## Hinweise

* Ihre Implementierung muss die [!DNL Target]-at.js-Bibliothek verwenden. Sie können keine mbox.js-Implementierung mit der Erweiterung verwenden.
* Die Markierung [!UICONTROL Ziel-Bibliotheken einfügen] ist in der Erweiterung standardmäßig DEAKTIVIERT. Sie können diese Markierung aktivieren, wenn Sie VEC auf einer Site verwenden möchten, für die [!DNL Target] noch nicht implementiert wurde.

   Beachten Sie, dass diese Markierung eine globale Einstellung ist. Sie wird für alle im VEC geöffneten Websites aktiviert bzw. deaktiviert. Wenn Sie diese Markierung beispielsweise aktivieren und eine Webseite öffnen, auf der at.js bereits implementiert ist, erhalten Sie eine Meldung, dass at.js bereits geladen ist. Wir erwarten, dass die meisten Kunden bereits at.js auf ihren Seiten implementiert haben und die Standardeinstellung (deaktiviert) verwenden werden.

* Die Erweiterung lädt die neueste Version von at.js, die über [!DNL Target UI] [!UICONTROL Einrichtung &gt; Implementierung] verfügbar ist.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, dies aber fehlschlägt, wird eine Meldung angezeigt, die empfiehlt, die VEC Helper-Browsererweiterung zu installieren.
   * Wenn at.js auf der Website noch nicht implementiert wurde, wird in VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.
   * Wenn die Erweiterung aktiviert ist und das Laden durchführt, werden Meldungen angezeigt, wenn die Erweiterung die at.js-Bibliothek einfügt (falls erforderlich) bzw. dabei hilft, die Website zuverlässig im VEC zu öffnen.