---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser
description: Erfahren Sie, warum einige Websites möglicherweise nicht zuverlässig in der [!UICONTROL Visual Experience Composer] (VEC). Die [!UICONTROL Visual Editing Helper] Mit der Browsererweiterung können Sie Websites zuverlässig im VEC laden.
title: Wie verwende ich die [!UICONTROL Visual Editing Helper] Erweiterung?
feature: Visual Experience Composer (VEC)
source-git-commit: 0c6d2df47a9115bcbd3c0d8a5ea7d401df29d6c8
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 22%

---

# [!UICONTROL Visual Editing Helper] Erweiterung

Die [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Mit der Browsererweiterung für Google Chrome können Sie Websites zuverlässig innerhalb der [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) verwenden, um schnell Web-Erlebnisse zu erstellen und zu überprüfen.

>[!IMPORTANT]
>
>Diese neue Erweiterung ersetzt die vorherige [Target VEC Helper-Browsererweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

## Gründe, weshalb einige Websites im VEC möglicherweise nicht zuverlässig geöffnet werden

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die QA- oder Staging-Site des Kunden ist nicht für die Außenwelt verfügbar (die Site ist intern).

Die [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Die Browsererweiterung für Chrome löst Probleme beim Laden von Sites, für die Kunden jetzt auf die [!DNL Target] [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder Drittanbietererweiterungen, z. B. Requestly.

## Vorteile der Verwendung der [!UICONTROL Visual Editing Helper] Erweiterung

* Alle iFrame-Busting-Kopfzeilen wie `X-Frame-Options` und `Content-Security-Policy`, werden implizit aus der Website entfernt. Es ist nicht erforderlich, komplizierte Requestly-Regeln zu erstellen.
* Wenn eine Webseite noch nicht die Variable [!DNL Target] at.js -Bibliothek verwenden, können Sie die -Erweiterung verwenden, um die Bibliothek einzufügen, damit Sie Erlebnisse für die Website erstellen können. Anschließend können Sie Aktivitäten erstellen und diese mithilfe von Vorschau-Links überprüfen.

Beachten Sie, dass mithilfe der Variablen [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec)festgelegt ist, injiziert die Erweiterung at.js nicht, aber die SameSite-Cookie-Funktion ist weiterhin vorhanden. Um at.js auf die Webseite zu injizieren, deaktivieren Sie den EEC.

* [Mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne die [!UICONTROL Enhanced Experience Composer] (EWG).
* Kunden, für die [!DNL Target] noch ungewohnt ist, können mit der Erweiterung mit [!DNL Target] experimentieren, selbst wenn ihre IT-Entwickler [!DNL Target] noch nicht auf der Webseite implementiert haben.
* Partner, die Websites und [!DNL Target]-Konten mehrerer Kunden bedienen, verfügen jetzt über einen einfachen Mechanismus, durch den sie VEC laden, anstatt mehrere Regeln in Drittanbieter-Werkzeugen verwalten zu müssen.

## Besorgen und installieren Sie die [!UICONTROL Visual Editing Helper] Browsererweiterung

1. Navigieren Sie zum [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] Browsererweiterung im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Klicken **[!UICONTROL Hinzufügen zu Chrome]** > **[!UICONTROL Erweiterung hinzufügen]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Um die Erweiterung zu verwenden, klicken Sie auf die [!UICONTROL Visual Editing Helper] Symbol für Browsererweiterung ( ![Symbol &quot;Visual Editing Extension&quot;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) in der Symbolleiste Ihres Chrome-Browsers im VEC- oder QA-Modus.

   Die [!UICONTROL Visual Editing Helper] automatisch aktiviert wird, wenn eine Website im [!UICONTROL Target] VEC zur Unterstützung der Inhaltserstellung. Die Erweiterung verfügt über keine bedingten Einstellungen. Die Erweiterung verarbeitet alle Einstellungen automatisch, einschließlich der SameSite-Cookie-Einstellungen.

   Weitere Informationen über `SameSite=None` -Attribut-Browser-Korrektur finden Sie unter &quot;Wie wirken sich die kürzlich angekündigten Google Chrome SameSite-Cookie-Durchsetzungsrichtlinien auf VEC und EEC aus?&quot; [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) unter der Frage „Wie wirken sich die kürzlich von Google Chrome angekündigten Cookie-Durchsetzungsrichtlinien für SameSite auf VEC und EEC aus?“.

## Hinweise

* Für [!DNL Target], lädt die -Erweiterung die neueste Version von at.js, die im Abschnitt [!DNL Target] Benutzeroberfläche in [!UICONTROL Administration] > [!UICONTROL Implementierung] und at.js lädt die Authoring-Bibliotheken herunter.
* Wenn Sie die Erweiterung verwenden, um at.js im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Chrome-Registerkarte muss für denselben [!DNL Adobe Experience Cloud] -Organisation, in der Sie die Aktivität erstellt haben.
* Die folgenden Meldungen helfen Ihnen dabei, auf dem neuesten Stand zu bleiben:

   * Wenn Sie versuchen, eine Website mit dem VEC zu laden, der nicht geladen werden kann, wird eine Meldung angezeigt, die empfiehlt, die [!UICONTROL Visual Editing Helper] Browsererweiterung.
   * Wenn at.js oder legierte.js noch nicht auf der Website implementiert ist, wird im VEC eine Meldung angezeigt, die empfiehlt, die Erweiterung zu installieren.



