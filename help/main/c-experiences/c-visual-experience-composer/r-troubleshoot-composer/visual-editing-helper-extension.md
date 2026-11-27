---
keywords: VEC;Visual Experience Composer;VEC;iFrame;Erweiterung;Browser;Häufig gestellte Fragen
description: Finden Sie heraus, warum manche Websites nicht zuverlässig im [!UICONTROL Visual Experience Composer] (VEC) geöffnet werden. Mit [!UICONTROL &#x200B; Browser-Erweiterung &#x200B;]Visual Editing Helper) können Sie Websites zuverlässig im VEC laden.
title: Wie verwende ich die Erweiterung [!UICONTROL Visual Editing Helper]?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
TQID: 'https://experienceleague.adobe.com/wUWUT-FvVIAo52PDaBMfmT7vxv8VOR71hSGhxFvylus'
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
source-wordcount: '829'
ht-degree: 5%
---
# [!UICONTROL Visual Editing Helper]-Erweiterung {#visual-editing-helper}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie die **[!UICONTROL Visual Editing Helper]**-Browser-Erweiterung Websites zuverlässig im **[!UICONTROL Visual Experience Composer]** (VEC) lädt und wie Sie ihn installieren und verwenden.

>[!ENDSHADEBOX]

Die [!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper]** Browser-Erweiterung für [!DNL Google Chrome] [!DNL Adobe Target] lädt Websites zuverlässig im **[!UICONTROL Visual Experience Composer]** (VEC), wodurch das Erstellen und Überprüfen von Web-Erlebnissen beschleunigt wird.

>[!IMPORTANT]
>
>Diese Erweiterung ersetzt die vorherige [Target VEC Helper-Browser-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), wie in dem wichtigen Hinweis oben in diesem Artikel beschrieben. Manifest V3 führt Sicherheitsverbesserungen ein, sodass [!DNL Adobe] das Herunterladen dieser neuen Erweiterung erfordert, um Websites weiterhin in [!DNL Target] visuell erstellen zu können.

## Warum einige Websites nicht zuverlässig im VEC geöffnet werden

Eine Website wird möglicherweise aus den folgenden Gründen nicht zuverlässig im VEC geöffnet:

* Die Website hat strikte Sicherheitsrichtlinien.
* Die Website befindet sich in einem iFrame.
* Die QA- oder Staging-Site des Kunden ist intern und außerhalb des Netzwerks nicht verfügbar.

Die Erweiterung löst diese Probleme beim Laden von Websites, für die Kundinnen und Kunden andernfalls auf den [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) oder auf Erweiterungen von Drittanbietern wie Requestly angewiesen sind.

## Vorteile der Erweiterung

* **Iframe-Busting-Kopfzeilen entfernt:** die Erweiterung entfernt Kopfzeilen wie `X-Frame-Options` und `Content-Security-Policy` implizit von der Website, sodass keine komplizierten Requestly-Regeln erforderlich sind.
* **at.js-Injektion** Wenn eine Web-Seite noch nicht die [!DNL Target] at.js-Bibliothek enthält, kann sie von der Erweiterung eingefügt werden. Anschließend können Erlebnisse für die Website erstellt und die Aktivitäten mit Vorschau-Links erstellt und geprüft werden. Beim [Enhanced Experience Composer](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) (EEC) wird at.js von der Erweiterung zwar nicht eingefügt, aber die SameSite Cookie-Funktionalität bleibt erhalten. Um at.js auf der Webseite einzubinden, schalten Sie den EEC aus.
* **Mobile Viewports:** [mobile Viewports](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) werden auch ohne den **[!UICONTROL Enhanced Experience Composer]** (EEC) unterstützt.
* **Neue [!DNL Target]-Kunden:** Die Erweiterung ermöglicht es, mit [!DNL Target] zu experimentieren, auch wenn die IT-Entwickler [!DNL Target] noch nicht auf der Website implementiert haben.
* **Partner:** Partner, die die Websites und [!DNL Target]-Konten mehrerer Kunden betreuen, erhalten einen Mechanismus zur Unterstützung des VEC-Ladevorgangs anstelle mehrerer Regeln in Drittanbieter-Tools.

## Beziehen und installieren Sie die Erweiterung

Durch das Installieren der Erweiterung in [!DNL Chrome] können Websites zuverlässig in VEC geladen werden, einschließlich Websites, die iFrames blockieren oder auf denen at.js noch nicht implementiert ist.

1. Navigieren Sie zur [[!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper &#x200B;]**-Browser-Erweiterung im Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Klicken Sie **[!UICONTROL Zu Chrome hinzufügen]** > **[!UICONTROL Erweiterung hinzufügen]**.
1. Öffnen Sie den VEC in [!DNL Target].
1. Klicken Sie im VEC- oder QA-Modus auf das Symbol **[!UICONTROL Visual Editing Helper]** der Browser-Erweiterung ( ![Visual Editing Helper-Symbol](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) in der Symbolleiste von [!DNL Chrome].

   Die Erweiterung wird automatisch aktiviert, wenn eine Website im [!DNL Target] VEC geöffnet wird, um die Inhaltserstellung zu unterstützen. Es verfügt über keine bedingten Einstellungen und verarbeitet alle Einstellungen automatisch, einschließlich der SameSite-Cookie-Einstellungen. Weitere Informationen zur Browser-Fehlerbehebung für das `SameSite=None` finden Sie unter [Google Chrome SameSite-Cookie-Richtlinien](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Nutzungshinweise

* Die Erweiterung lädt die neueste Version von at.js, die in der [!DNL Target]-Benutzeroberfläche unter **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** verfügbar ist, und at.js lädt die Authoring-Bibliotheken herunter.
* Um at.js mithilfe der Erweiterung im [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) einzufügen, muss eine andere Chrome-Registerkarte geöffnet sein. Diese Registerkarte muss für dieselbe [!DNL Adobe Experience Cloud]-Organisation authentifiziert sein, in der die Aktivität erstellt wurde.
* In folgenden Fällen zeigt der VEC Meldungen an, die die Installation der Erweiterung empfehlen:

  * Eine Website kann nicht in VEC geladen werden.
  * at.js oder alloy.js ist noch nicht auf der Website implementiert.

* Wenn die neue Erweiterung versucht wurde und die [alte Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) erneut verwendet wird, aber [!DNL Target] die Website nicht laden kann, löschen Sie alle Browser-Daten und deaktivieren Sie die neue Erweiterung.

## Letzte Änderungen an der Verlängerung (17. Januar 2026)

Die Erweiterung fügt dem VEC Helper eine experimentelle Funktion zur Bereinigung von Startup-Cookies hinzu. Die Funktion bereinigt nicht partitionierte Cookies einmal pro Registerkarte, wenn mit der Bearbeitung begonnen wird, anstatt kontinuierlich, was die Leistung und Zuverlässigkeit verbessert. Es verfolgt den Verlauf der einzelnen Registerkarten, um redundante Bereinigungen zu verhindern, und löscht diesen Verlauf, wenn die Registerkarte geschlossen wird. Die Bereinigung verhält sich also korrekt, wenn die Registerkarte erneut geöffnet wird. Modultests stellen ein konsistentes Verhalten sicher.

![Optionen der VEC Helper-Erweiterung, einschließlich der Cookie-Verarbeitungsmodi, der erweiterten Protokollierungsoption und der experimentellen Funktionen Verzögertes Laden von Web-Seiten, Bereinigung von Cookies und Bereinigung von Startup-Cookies](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper.png)

## Häufig gestellte Fragen

+++ Hat die Erweiterung irgendeine Funktion, wenn sie außerhalb von [!DNL Adobe Target] oder [!UICONTROL Adobe Journey Optimizer] (AJO) verwendet wird?

Die Erweiterung wird nur aktiviert, wenn die Website innerhalb eines iFrames in [!DNL Adobe]-Produkten ([!DNL Target], [!DNL AJO]) geladen wird. Außerhalb dieses Flusses versucht die Erweiterung nicht, Kopfzeilen hinzuzufügen, zu entfernen oder zu ändern, und sie versucht auch nicht, Code in die Website einzufügen.

+++

+++ Was bewirkt die Erweiterung, wenn sie in der [!DNL Adobe Target] VEC aktiv ist?

Wenn eine Website innerhalb eines iFrames in [!DNL Adobe]-Produkten ([!DNL Target], [!DNL AJO]) geladen wird, fügt die Erweiterung Code, der mit der Erweiterung gebündelt ist, in die Website ein und lädt Hilfsdateien aus dem [!DNL Adobe] CDN herunter, um visuelles Authoring zu ermöglichen.

+++
