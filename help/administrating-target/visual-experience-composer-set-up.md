---
keywords: Visual Experience Composer;VEC;Standard-URL;Enhanced Experience Composer;EOC;Mixed Content;Experience Snapshots;Mobile Viewport;CSS;CSS-Selektoren
description: Erfahren Sie, wie Sie die Adobe [!DNL Target] Visual Experience Composer (VEC) konfigurieren, indem Sie ihre allgemeinen Einstellungen, die Konfiguration des mobilen Viewports und CSS-Selektoren angeben.
title: Wie konfiguriere ich den Visual Experience Composer (VEC)?
feature: Administration und Konfiguration
role: Administrator
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 49%

---

# Konfigurieren des Visual Experience Composer

Konfigurieren Sie den [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC), indem Sie seine allgemeinen Einstellungen, die Konfiguration des mobilen Viewports und die CSS-Selektoren angeben.

Um auf die Konfigurationsseite [!UICONTROL Visual Experience Composer] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer].**

>[!NOTE]
>
>Beachten Sie, dass die Einstellungen auf dieser Seite für das gesamte [!DNL Target]-Konto gelten.

![Konfigurationsseite von Visual Experience Composer](/help/administrating-target/assets/vec.png)

## Allgemeine Einstellungen

Sie können allgemeine Einstellungen für den Visual Experience Composer angeben.

![Abschnitt &quot;Allgemeine Einstellungen&quot;](/help/administrating-target/assets/general-settings.png)

Die folgenden Einstellungen sind verfügbar:

### Standard-URL

Die Standard-URL, die von [!UICONTROL Visual Experience Composer] verwendet wird. Dies ist die Standardseite, wie Ihre Startseite, die verwendet wird, wenn Sie ein Erlebnis für jede neue Aktivität einrichten. Sollten Sie keine Standard-URL festlegen, müssen Sie für jede Aktivität bei deren Erstellung eine eigene URL eingeben.

### Erweiterten Experience Composer aktivieren {#eec}

Ermöglicht die Bearbeitung auf Sites, die iFrames zerstören, sowie auf Seiten mit gemischten Inhalten. Einige Sites sind möglicherweise nicht mit der erweiterten Version kompatibel. Deaktivieren Sie diese Option, um zum ursprünglichen [!UICONTROL Visual Experience Composer] zurückzukehren. Die Aktivitätenbereitstellung auf Sites wird durch diese Auswahl nicht beeinträchtigt.

Weitere Informationen finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

Sie können den [!UICONTROL Enhanced Experience Composer] auch auf der Ebene der Aktivität aktivieren.

### Gemischte Inhalte laden

Aktivieren Sie gemischte Inhalte, während Sie eine Website mit dem [!UICONTROL Enhanced Experience Composer] (EEC) öffnen. Durch Aktivierung dieser Option wird der zusätzliche Aufwand beim Laden statischer Ressourcen über [!DNL Target]-Proxyserver vermieden.

Diese Option ist hilfreich, wenn Sie zum Beispiel:

* Ihre CSP-Header (Content Security Policy) ermöglichen das Laden von gemischten Inhalten ohne die Verwendung von Proxyservern mit aktivierter EWG.
* Ihre HTTP-Website hat in der EWG eine längere Ladezeit, wodurch JavaScript, Bilder usw. länger über einen Proxy geladen werden müssen.

### Generieren von Erlebnismomentaufnahmen im Flussdiagramm der Aktivität

Bei der Aktivierung von Erlebnismomentaufnahmen werden Miniaturen Ihrer Erlebnisse in der Übersicht des Aktivitätsarbeitsablaufs generiert. Die Deaktivierung von Momentaufnahmen kann bei einigen Benutzern zu einer Beschleunigung der Performance führen.

## ![Premium ](/help/assets/premium.png) badgeMobile Viewport-Konfiguration

Sie können Geräte hinzufügen, die für die Vorschau der Erlebnisse verwendet werden sollen. Jedem Gerät ist dabei eine Zielgruppe zugeordnet.

![Abschnitt zur Konfiguration von Mobile Viewport](/help/administrating-target/assets/mobile-viewport-configuration.png)

Klicken Sie auf **[!UICONTROL Hinzufügen]**, geben Sie einen beschreibenden Namen für den mobilen Viewport ein, geben Sie die Breite und Höhe an, wählen Sie das gewünschte Betriebssystem und klicken Sie dann auf [!UICONTROL Speichern].

Informationen zum Hinzufügen eines mobilen Viewports finden Sie unter [Mobile Viewport – Konfiguration](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## CSS-Selektoren {#css}

Geben Sie an, wie [!DNL Target] CSS-Selektoren generiert.

![Abschnitt &quot;CSS-Selektoren&quot;](/help/administrating-target/assets/css-selectors.png)

Diese Optionen helfen [!DNL Target] dabei, die Struktur Ihrer Site zu verstehen, um bessere CSS-Selektoren für die Bereitstellung von Inhalten zu erzeugen. Standardmäßig erstellt [!DNL Target] die Selektoren auf Basis der Element-IDs auf der Seite. Wenn auf Ihrer Site nur wenige IDs verwendet werden oder IDs auf derselben Seite dupliziert werden, ist die Verwendung von Klassen wahrscheinlich die bessere Option.

Sie können eine oder beide der folgenden Optionen verwenden:

### Element-IDs verwenden

Deaktivieren Sie diese Option, wenn die gleiche ID für mehrere Elemente verwendet wird oder sich die Element-ID beim Laden der Seite möglicherweise ändert.

### Elementklassen verwenden

Standardmäßig verwendet [!DNL Target] nur Element-IDs. Wenn Ihre Seite jedoch so entwickelt wurde, dass zur Identifizierung von Elementen Klassen verwendet werden (wie beispielsweise bei einer mit [!DNL Adobe Experience Manager] erstellten Seite), dann sollten Sie die Option [!UICONTROL Elementklassen verwenden] auswählen.

>[!NOTE]
>
>Obwohl alles unternommen wurde, um Genauigkeit zu gewährleisten, sollten Sie bedenken, dass die Verwendung von Klassen zu Fehlern führen kann. Wenn Sie keine der beiden Optionen auswählen, hat dies auch Auswirkungen auf die Genauigkeit. Die Reihenfolge für Genauigkeit lautet IDs > Klassen > keine der beiden Optionen. Sie sollten Ihre Seite immer testen, um sicherzustellen, dass die Selektoren korrekt sind.

Sie können diese Einstellung pro Aktivität außer Kraft setzen (klicken Sie dazu auf das Zahnradsymbol [!UICONTROL Einstellungen] und wählen Sie anschließend [!UICONTROL CSS-Selektoren] aus). Dies ist besonders dann nützlich, wenn Sie mehrere Sites haben, die unterschiedlich konfiguriert sind.

>[!NOTE]
>
>Das Überschreiben der Einstellung pro Aktivität ist in den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Multivariate Testing] nicht verfügbar.  Weitere Informationen zu Selektoren finden Sie im Abschnitt [Element-Selektoren, die im Visual Experience Composer verwendet werden](/help/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Schulungsvideo: Kontovoreinstellungen (7:33) ![Kennzeichen &quot;Überblick&quot;](/help/assets/overview.png)

In diesem Video finden Sie Informationen zu Kontovoreinstellungen.

* Beschreibung der in [!DNL Target Standard] verfügbaren Kontoeinstellungen

>[!NOTE]
>
>Die Menüoberfläche [!DNL Target] [!UICONTROL Administration] (ehemals [!UICONTROL Setup]) wurde überarbeitet, um eine verbesserte Leistung zu bieten, die Wartungszeit zu verkürzen, die bei der Veröffentlichung neuer Funktionen erforderlich ist, und die Benutzererfahrung im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind im Allgemeinen korrekt. Die Optionen befinden sich jedoch möglicherweise an etwas anderen Orten. Aktualisierte Videos werden demnächst veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
