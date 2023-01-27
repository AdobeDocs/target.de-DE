---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser;FAQs
description: Finden Sie heraus, warum manche Websites nicht zuverlässig im [!UICONTROL Visual Experience Composer] (VEC) geöffnet werden. Mit der Browser-Erweiterung [!UICONTROL Visual Editing Helper] können Sie Websites zuverlässig im VEC laden.
title: Wie verwende ich die [!UICONTROL Visual Editing Helper]-Erweiterung?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: 30ad6712d9722854384721ca20d38a605930c4d7
workflow-type: ht
source-wordcount: '712'
ht-degree: 100%

---

# [!UICONTROL Visual Editing Helper]-Erweiterung

Mit der Browser-Erweiterung [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] für Google Chrome können Sie Websites zuverlässig innerhalb des [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) laden, um Web-Inhalte schnell zu erstellen und zu prüfen.

>[!IMPORTANT]
>
>Diese neue Erweiterung ersetzt die frühere [Target VEC Helper-Browser-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Weitere Informationen finden Sie im wichtigen Hinweis oben in diesem Artikel.

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die QA- oder Status-Site von Kundinnen und Kunden kann extern nicht abgerufen werden (interne Site).

Die [!DNL Adobe Experience Cloud]-Browser-Erweiterung [!UICONTROL Visual Editing Helper] für Chrome löst Probleme beim Laden von Websites, für die Kundinnen und Kunden jetzt auf den [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder Erweiterungen von Drittanbietern wie Requestly angewiesen sind.

## Vorteile der Verwendung der [!UICONTROL Visual Editing Helper]-Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie `X-Frame-Options` und `Content-Security-Policy` werden implizit von der Website entfernt. Es ist nicht erforderlich, komplizierte Requestly-Regeln zu erstellen.
* Wenn eine Website noch nicht die at.js-Bibliothek für [!DNL Target] enthält, können Sie die Erweiterung zum Einspeisen der Bibliothek verwenden, damit Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

   Bei Verwendung des [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) wird at.js von der Erweiterung zwar nicht eingefügt, aber die SameSite Cookie-Funktionalität ist weiterhin vorhanden. Um at.js auf der Webseite einzubinden, schalten Sie den EEC aus.

* [Mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne den [!UICONTROL Enhanced Experience Composer] (EEC) unterstützt. 
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Beziehen und installieren Sie die Browser-Erweiterung [!UICONTROL Visual Editing Helper]

1. Navigieren Sie zu der [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Browser-Erweiterung im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Klicken Sie auf **[!UICONTROL Zu Chrome hinzufügen]** > **[!UICONTROL Erweiterung hinzufügen]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie auf das Symbol der Browser-Erweiterung [!UICONTROL Visual Editing Helper] ( ![Visual Editing-Erweiterungssymbol](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) in der Symbolleiste Ihres Chrome-Browsers, während Sie sich im VEC- oder QA-Modus befinden.

   Die [!UICONTROL Visual Editing Helper] wird automatisch aktiviert, wenn eine Website im VEC von [!UICONTROL Target] geöffnet wird, um die Bearbeitung zu unterstützen. Die Erweiterung verfügt über keine bedingten Einstellungen. Die Erweiterung verarbeitet alle Einstellungen automatisch, einschließlich der SameSite Cookie-Einstellungen.

   Weitere Informationen zur Browser-Fehlerbehebung für das `SameSite=None`-Attribut finden Sie unter „Wie wirken sich die kürzlich angekündigten Richtlinien zur Durchsetzung von SameSite-Cookies in Google Chrome auf den VEC und EEC aus?“ in [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Hinweise

* Für [!DNL Target] lädt die Erweiterung die neueste Version von at.js, die über die [!DNL Target]-Benutzeroberfläche unter [!UICONTROL Administration] > [!UICONTROL Implementierung] verfügbar ist, und at.js lädt die Authoring-Bibliotheken herunter.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, die sich nicht laden lässt, wird eine Meldung mit dem Vorschlag angezeigt, die Browser-Erweiterung [!UICONTROL Visual Editing Helper] zu installieren.
   * Wenn at.js oder alloy.js noch nicht auf der Website implementiert ist, wird im VEC eine Meldung angezeigt, die Sie auffordert, die Erweiterung zu installieren.
* Wenn Sie versuchen, die neue Erweiterung zu verwenden und danach zur [alten Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) zurückkehren und [!DNL Target] Ihre Webseite nicht laden kann, löschen Sie alle Browser-Daten und deaktivieren Sie die neue Erweiterung.

## Häufig gestellte Fragen  

### Hat die Erweiterung, wenn sie aktiv ist, irgendeine Funktion, wenn sie außerhalb von [!DNL Adobe Target] oder [!UICONTROL Adobe Journey Optimizer] (AJO) verwendet wird?

Die Erweiterung wird nur aktiviert, wenn die betreffende Website innerhalb eines iFrames in [!DNL Adobe]-Produkten ([!DNL Target], [!DNL AJO]) geladen wird. Außerhalb dieses Flusses versucht die Erweiterung nicht, Kopfzeilen hinzuzufügen, zu entfernen oder zu verändern, und sie versucht auch nicht, Code in die Website einzufügen.

### Was bewirkt die Erweiterung, wenn sie in der [!DNL Adobe Target] VEC aktiv ist?

Wenn eine Website innerhalb eines iFrames in [!DNL Adobe]-Produkten ([!DNL Target], [!DNL AJO]) geladen wird, fügt die Erweiterung Code (der mit der Erweiterung gebündelt ist) in die Website ein und lädt Hilfsdateien aus dem [!DNL Adobe] CDN herunter, um visuelles Authoring zu ermöglichen.
