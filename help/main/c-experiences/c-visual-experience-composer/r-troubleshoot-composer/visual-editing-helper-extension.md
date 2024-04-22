---
keywords: VEC; Visual Experience Composer; VEC; iframe; Erweiterung; Browser; FAQ
description: Erfahren Sie, warum einige Websites möglicherweise nicht zuverlässig in der [!UICONTROL Visual Experience Composer] (VEC). Die [!UICONTROL Visual Editing Helper] Mit der Browsererweiterung können Sie Websites zuverlässig im VEC laden.
title: Wie verwende ich die [!UICONTROL Visual Editing Helper] Erweiterung?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: 8edae6a197a3ac82b85fcce4d99c8b0d5f45c712
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 64%

---

# [!UICONTROL Visual Editing Helper] Erweiterung

Die [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Browsererweiterung für [!DNL Google Chrome] ermöglicht das zuverlässige Laden von Websites innerhalb der [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) verwenden, um schnell Web-Erlebnisse zu erstellen und zu überprüfen.

>[!IMPORTANT]
>
>Diese neue Erweiterung ersetzt die frühere [Target VEC Helper-Browser-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Weitere Informationen finden Sie im wichtigen Hinweis oben in diesem Artikel. Aufgrund der Sicherheitsverbesserungen in Manifest v3, [!DNL Adobe] erfordert das Herunterladen dieser neuen Erweiterung, um Ihre Websites weiterhin visuell in [!DNL Target].

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die QA- oder Status-Site von Kundinnen und Kunden kann extern nicht abgerufen werden (interne Site).

Die [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Browsererweiterung für löst Probleme beim Laden von Sites, für die Kunden jetzt auf die [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder Drittanbietererweiterungen, z. B. Requestly.

## Vorteile der Verwendung der [!UICONTROL Visual Editing Helper] Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie `X-Frame-Options` und `Content-Security-Policy` werden implizit von der Website entfernt. Es ist nicht erforderlich, komplizierte Requestly-Regeln zu erstellen.
* Wenn eine Website noch nicht die at.js-Bibliothek für [!DNL Target] enthält, können Sie die Erweiterung zum Einspeisen der Bibliothek verwenden, damit Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

  Bei Verwendung des [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) wird at.js von der Erweiterung zwar nicht eingefügt, aber die SameSite Cookie-Funktionalität ist weiterhin vorhanden. Um at.js auf der Webseite einzubinden, schalten Sie den EEC aus.

* [Mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne die [!UICONTROL Enhanced Experience Composer] (EWG).
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Installieren Sie die [!UICONTROL Visual Editing Helper] Browsererweiterung

1. Navigieren Sie zum [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Browsererweiterung im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Klicks **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie auf die [!UICONTROL Visual Editing Helper] Symbol für Browsererweiterung ( ![Symbol &quot;Visual Editing Extension&quot;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) in der Symbolleiste Ihres Chrome-Browsers im VEC- oder QA-Modus.

   Die [!UICONTROL Visual Editing Helper] automatisch aktiviert wird, wenn eine Website im [!UICONTROL Target] VEC für die Bearbeitung. Die Erweiterung verfügt über keine bedingten Einstellungen. Die Erweiterung verarbeitet alle Einstellungen automatisch, einschließlich der SameSite Cookie-Einstellungen.

   Weitere Informationen zur Browser-Fehlerbehebung für das `SameSite=None`-Attribut finden Sie unter „Wie wirken sich die kürzlich angekündigten Richtlinien zur Durchsetzung von SameSite-Cookies in Google Chrome auf den VEC und EEC aus?“ in [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Hinweise

* Für [!DNL Target], lädt die -Erweiterung die neueste Version von at.js, die im Abschnitt [!DNL Target] Benutzeroberfläche in [!UICONTROL Administration] > [!UICONTROL Implementation] und at.js lädt die Authoring-Bibliotheken herunter.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, der nicht geladen werden kann, wird eine Meldung angezeigt, die empfiehlt, die [!UICONTROL Visual Editing Helper] Browsererweiterung.
   * Wenn at.js oder alloy.js noch nicht auf der Website implementiert ist, wird im VEC eine Meldung angezeigt, die Sie auffordert, die Erweiterung zu installieren.
* Wenn Sie versuchen, die neue Erweiterung zu verwenden und danach zur [alten Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) zurückkehren und [!DNL Target] Ihre Webseite nicht laden kann, löschen Sie alle Browser-Daten und deaktivieren Sie die neue Erweiterung.

## Häufig gestellte Fragen  

### Führt die Erweiterung, wenn sie aktiv ist, irgendetwas aus, wenn sie außerhalb von [!DNL Adobe Target] oder [!UICONTROL Adobe Journey Optimizer] (AJO)?

Die Erweiterung wird nur aktiviert, wenn die betreffende Website innerhalb eines iFrames in [!DNL Adobe]-Produkten ([!DNL Target], [!DNL AJO]) geladen wird. Außerhalb dieses Flusses versucht die Erweiterung nicht, Kopfzeilen hinzuzufügen, zu entfernen oder zu verändern, und sie versucht auch nicht, Code in die Website einzufügen.

### Was bewirkt die Erweiterung, wenn sie in der [!DNL Adobe Target] VEC aktiv ist?

Wenn eine Website innerhalb eines iFrames in [!DNL Adobe]-Produkten ([!DNL Target], [!DNL AJO]) geladen wird, fügt die Erweiterung Code (der mit der Erweiterung gebündelt ist) in die Website ein und lädt Hilfsdateien aus dem [!DNL Adobe] CDN herunter, um visuelles Authoring zu ermöglichen.
