---
keywords: Visual Experience Composer;VEC;Standard-URL;Enhanced Experience Composer;EEC;gemischte Inhalte;Erlebnismomentaufnahmen;mobiler Viewport;CSS;CSS-Selektoren
description: Erfahren Sie, wie Sie die Adobe [!DNL Target] Visual Experience Composer (VEC) konfigurieren, indem Sie ihre allgemeinen Einstellungen, die Konfiguration mobiler Viewports und CSS-Selektoren angeben.
title: Wie konfiguriere ich Visual Experience Composer (VEC)?
feature: Administration und Konfiguration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
source-git-commit: be7b5478006af231aae2b78e4a8c0066e3cb4a5b
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 50%

---

# Konfigurieren des Visual Experience Composer

Konfigurieren Sie den [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC), indem Sie seine allgemeinen Einstellungen, die Konfiguration mobiler Viewports und CSS-Selektoren angeben.

Um auf die Konfigurationsseite [!UICONTROL Visual Experience Composer] zuzugreifen, klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer].**

>[!NOTE]
>
>Beachten Sie, dass die Einstellungen auf dieser Seite für das gesamte [!DNL Target]-Konto gelten.

![Konfigurationsseite für Visual Experience Composer](/help/administrating-target/assets/vec.png)

## Allgemeine Einstellungen

Sie können allgemeine Einstellungen für Visual Experience Composer angeben.

![Abschnitt &quot;Allgemeine Einstellungen&quot;](/help/administrating-target/assets/general-settings.png)

Die folgenden Einstellungen sind verfügbar:

### Standard-URL

Die Standard-URL, die von [!UICONTROL Visual Experience Composer] verwendet wird. Dies ist die Standardseite, wie Ihre Startseite, die verwendet wird, wenn Sie ein Erlebnis für jede neue Aktivität einrichten. Sollten Sie keine Standard-URL festlegen, müssen Sie für jede Aktivität bei deren Erstellung eine eigene URL eingeben.

### Erweiterten Experience Composer aktivieren {#eec}

Ermöglicht die Bearbeitung auf Sites, die iFrames zerstören, sowie auf Seiten mit gemischten Inhalten. Einige Websites sind möglicherweise nicht mit der erweiterten Version kompatibel. Deaktivieren Sie diese Option, um zum ursprünglichen [!UICONTROL Visual Experience Composer] zurückzukehren. Die Aktivitätenbereitstellung auf Sites wird durch diese Auswahl nicht beeinträchtigt.

Weitere Informationen finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

Sie können den [!UICONTROL Enhanced Experience Composer] auch auf Aktivitätsebene aktivieren.

### Gemischte Inhalte laden

Aktivieren Sie gemischte Inhalte beim Öffnen einer Website mit dem [!UICONTROL Enhanced Experience Composer] (EEC). Durch Aktivierung dieser Option wird der Mehraufwand für das Laden von statischen Ressourcen über [!DNL Target]-Proxyserver vermieden.

Diese Option ist beispielsweise hilfreich, wenn:

* Ihre CSP-Header (Content Security Policy) ermöglichen das Laden von gemischten Inhalten, ohne Proxy-Server mit aktiviertem EEC zu verwenden.
* Ihre HTTP-Website weist im EEC eine höhere Ladezeit auf, da das Laden von JavaScript, Bildern usw. über einen Proxy länger dauert.

### Generieren von Erlebnismomentaufnahmen im Aktivitätsflussdiagramm

Bei der Aktivierung von Erlebnismomentaufnahmen werden Miniaturen Ihrer Erlebnisse in der Übersicht des Aktivitätsarbeitsablaufs generiert. Die Deaktivierung von Momentaufnahmen kann bei einigen Benutzern zu einer Beschleunigung der Performance führen.

## ![Premium ](/help/assets/premium.png) badgeMobile Viewport-Konfiguration

Sie können Geräte hinzufügen, die für die Vorschau der Erlebnisse verwendet werden sollen. Jedem Gerät ist dabei eine Zielgruppe zugeordnet.

![Konfigurationsabschnitt für Mobile Viewport](/help/administrating-target/assets/mobile-viewport-configuration.png)

Klicken Sie auf **[!UICONTROL Hinzufügen]**, geben Sie einen beschreibenden Namen für den mobilen Viewport an, geben Sie die Breite und Höhe an, wählen Sie das gewünschte Betriebssystem aus und klicken Sie dann auf [!UICONTROL Speichern].

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
>Obwohl alles unternommen wurde, um Genauigkeit sicherzustellen, sollten Sie bedenken, dass die Verwendung von Klassen zu Fehlern führen kann. Wenn Sie keine der beiden Optionen auswählen, hat dies auch Auswirkungen auf die Genauigkeit. Die Reihenfolge für Genauigkeit lautet IDs > Klassen > keine der beiden Optionen. Sie sollten Ihre Seite immer testen, um sicherzustellen, dass die Selektoren korrekt sind.

Sie können diese Einstellung pro Aktivität außer Kraft setzen (klicken Sie dazu auf das Zahnradsymbol [!UICONTROL Einstellungen] und wählen Sie anschließend [!UICONTROL CSS-Selektoren] aus). Dies ist besonders dann nützlich, wenn Sie mehrere Sites haben, die unterschiedlich konfiguriert sind.

>[!NOTE]
>
>Das Außerkraftsetzen der Einstellung pro Aktivität ist nicht in den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Multivariate Testing] verfügbar.  Weitere Informationen zu Selektoren finden Sie im Abschnitt [Element-Selektoren, die im Visual Experience Composer verwendet werden](/help/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Schulungsvideo: Kontovoreinstellungen (7:33) ![Badge &quot;Überblick&quot;](/help/assets/overview.png)

In diesem Video finden Sie Informationen zu Kontovoreinstellungen.

* Beschreibung der in [!DNL Target Standard] verfügbaren Kontoeinstellungen

>[!NOTE]
>
>Die Menübenutzeroberfläche [!DNL Target] [!UICONTROL Administration] (ehemals [!UICONTROL Setup]) wurde überarbeitet, um eine verbesserte Leistung, eine Verkürzung der Wartungszeit bei der Veröffentlichung neuer Funktionen und eine produktübergreifende Verbesserung des Benutzererlebnisses zu erzielen. Die Informationen im folgenden Video sind im Allgemeinen korrekt. -Optionen können sich jedoch an etwas anderen Orten befinden. Aktualisierte Videos werden bald veröffentlicht.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
