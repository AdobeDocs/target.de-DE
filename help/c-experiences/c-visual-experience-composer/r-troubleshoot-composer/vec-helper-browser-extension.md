---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Informationen zur Verwendung der Adobe Target Visual Experience Composer (VEC) Helper-Browsererweiterung, um Websites zuverlässig innerhalb von VEC zu laden und so schnell Erlebnisse zu erstellen und zu überprüfen.
title: Adobe Target Visual Experience Composer (VEC) Helper-Erweiterung
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 94%

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
* Wenn eine Webseite noch nicht die [!DNL Target]-JavaScript-Bibliothek at.js enthält, können Sie die Erweiterung verwenden, um die Bibliothek einzufügen, sodass Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.
* Mobile Viewports werden auch ohne [!UICONTROL Enhanced Experience Composer] (EEC) unterstützt.
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und Installieren der VEC Helper-Browsererweiterung

1. Navigate to the [Adobe Target VEC Helper browser extension in the Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Klicken Sie auf [!UICONTROL Zu Chrome hinzufügen > Erweiterung hinzufügen].
1. Um die Erweiterung zu verwenden, klicken Sie in der Symbolleiste des Chrome-Browsers auf das VEC Helper-Symbol (![VEC Helper-Symbol](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)), während Sie sich im VEC oder [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) befinden.

Die folgende Abbildung zeigt den VEC Helper mit aktivierter Einstellung [!UICONTROL Target-Bibliotheken injizieren]:

![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

Die folgende Abbildung zeigt den VEC Helper an mit der Frage, ob Sie [!DNL Target]-Bibliotheken auf der Seite einfügen möchten, um Authoring zu ermöglichen:

![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

## Hinweise

* Ihre Implementierung muss die [!DNL Target]-at.js-Bibliothek verwenden. Sie können keine mbox.js-Implementierung mit der Erweiterung verwenden.
* Die Markierung [!UICONTROL Ziel-Bibliotheken einfügen] ist in der Erweiterung standardmäßig DEAKTIVIERT. Sie können diese Markierung aktivieren, wenn Sie VEC auf einer Site verwenden möchten, für die [!DNL Target] noch nicht implementiert wurde.

   Beachten Sie, dass diese Markierung eine globale Einstellung ist. Sie wird für alle im VEC geöffneten Websites aktiviert bzw. deaktiviert. Wenn Sie diese Markierung beispielsweise aktivieren und eine Webseite öffnen, auf der at.js bereits implementiert ist, erhalten Sie eine Meldung, dass at.js bereits geladen ist. Wir erwarten, dass die meisten Kunden bereits at.js auf ihren Seiten implementiert haben und die Standardeinstellung (deaktiviert) verwenden werden.

* The extension loads the latest version of at.js that is available from the [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, dies aber fehlschlägt, wird eine Meldung angezeigt, die empfiehlt, die VEC Helper-Browsererweiterung zu installieren.
   * Wenn at.js auf der Website noch nicht implementiert wurde, wird in VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.
   * Wenn die Erweiterung aktiviert ist und das Laden durchführt, werden Meldungen angezeigt, wenn die Erweiterung die at.js-Bibliothek einfügt (falls erforderlich) bzw. dabei hilft, die Website zuverlässig im VEC zu öffnen.