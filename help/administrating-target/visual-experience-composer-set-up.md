---
keywords: visual experience composer;vec;default url;enhanced experience composer;eec;mixed content;experience snapshots;mobile viewport;css;css selectors
description: Konfigurieren Sie den Adobe Target Visual Experience Composer (VEC), indem Sie seine allgemeinen Einstellungen, die Konfiguration des mobilen Viewports und CSS-Selektoren angeben.
title: Adobe Target Visual Experience Composer konfigurieren
feature: administration general
topic: Standard
translation-type: tm+mt
source-git-commit: ee618961faa12a7352aaf9ed1d869f9e5ab39cdd
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 51%

---


# Konfigurieren des Visual Experience Composer

Konfigurieren Sie den [!DNL Adobe Target] Visual Experience Composer  (VEC), indem Sie dessen allgemeine Einstellungen, die Konfiguration des mobilen Viewports und CSS-Selektoren angeben.

Um auf die Konfigurationsseite des [!UICONTROL Visual Experience Composer] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer].**

>[!NOTE]
>
>Beachten Sie, dass die Einstellungen auf dieser Seite für das gesamte [!DNL Target] Konto gelten.

![Konfigurationsseite von Visual Experience Composer](/help/administrating-target/assets/vec.png)

## Allgemeine Einstellungen

Sie können allgemeine Einstellungen für den Visual Experience Composer angeben.

![Abschnitt &quot;Allgemeine Einstellungen&quot;](/help/administrating-target/assets/general-settings.png)

Die folgenden Einstellungen sind verfügbar:

### Standard-URL

Die Standard-URL, die von [!UICONTROL Visual Experience Composer] verwendet wird. Dies ist die Standardseite, wie Ihre Startseite, die verwendet wird, wenn Sie ein Erlebnis für jede neue Aktivität einrichten. Sollten Sie keine Standard-URL festlegen, müssen Sie für jede Aktivität bei deren Erstellung eine eigene URL eingeben.

### Erweiterten Experience Composer aktivieren {#eec}

Ermöglicht die Bearbeitung auf Sites, die iFrames zerstören, sowie auf Seiten mit gemischten Inhalten. Einige Sites sind möglicherweise nicht mit der erweiterten Version kompatibel. Deselect this option to revert to the original [!UICONTROL Visual Experience Composer]. Die Aktivitätenbereitstellung auf Sites wird durch diese Auswahl nicht beeinträchtigt.

Weitere Informationen finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

You can also enable the [!UICONTROL Enhanced Experience Composer] at the activity level.

### Gemischte Inhalte laden

Enable mixed content while opening a website using the [!UICONTROL Enhanced Experience Composer] (EEC). Enabling this option avoids the extra overhead of loading static resources via [!DNL Target] proxy servers.

Diese Option ist hilfreich, wenn Sie zum Beispiel:

* Ihre CSP-Header (Content Security Policy) ermöglichen das Laden von gemischten Inhalten ohne die Verwendung von Proxyservern mit aktivierter EWG.
* Ihre HTTP-Website hat in der EWG eine längere Ladezeit, wodurch JavaScript, Bilder usw. länger über einen Proxy geladen werden müssen.

### Generieren von Erlebnismomentaufnahmen im Flussdiagramm der Aktivität

Bei der Aktivierung von Erlebnismomentaufnahmen werden Miniaturen Ihrer Erlebnisse in der Übersicht des Aktivitätsarbeitsablaufs generiert. Die Deaktivierung von Momentaufnahmen kann bei einigen Benutzern zu einer Beschleunigung der Performance führen.

## ![Premium-Badge](/help/assets/premium.png) Mobile Viewport-Konfiguration

Sie können Geräte hinzufügen, die für die Vorschau der Erlebnisse verwendet werden sollen. Jedem Gerät ist dabei eine Zielgruppe zugeordnet.

![Abschnitt zur Konfiguration von Mobile Viewport](/help/administrating-target/assets/mobile-viewport-configuration.png)

Click **[!UICONTROL Add]**, specify a descriptive name for the mobile viewport, specify the width and height, select the desired operating system, then click [!UICONTROL Save].

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
>Overriding the setting per activity is not available in [!UICONTROL Automated Personalization] and [!UICONTROL Multivariate Testing] activities.  Weitere Informationen zu Selektoren finden Sie im Abschnitt [Element-Selektoren, die im Visual Experience Composer verwendet werden](/help/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Schulungsvideo: Symbol &quot;Kontovoreinstellungen&quot;(7:33) ![Übersicht](/help/assets/overview.png)

In diesem Video finden Sie Informationen zu Kontovoreinstellungen.

* Beschreibung der in [!DNL Target Standard] verfügbaren Kontoeinstellungen

>[!NOTE]
>
>Die Benutzeroberfläche des [!DNL Target] Administrationsmenüs [!UICONTROL (früher] Setup ) wurde überarbeitet, um die Leistung zu verbessern, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu verkürzen und die Benutzerfreundlichkeit im gesamten Produkt zu verbessern. Die Informationen im folgenden Video sind im Allgemeinen korrekt. Die Optionen befinden sich jedoch möglicherweise an etwas anderen Orten. Aktualisierte Videos werden demnächst veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
