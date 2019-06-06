---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für die neuesten oder kommenden Target-Versionen.
keywords: Versionshinweise
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für die neuesten oder kommenden Adobe Target-Versionen
seo-title: Versionshinweise zu Adobe Target (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: e50ae8c95774716ea484f02b276b2d66cb228364

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert: 6. Juni 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungsdaten, Funktionen und andere Informationen können ohne vorherige Benachrichtigung geändert werden. Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 19.6.1 (25. Juni 2019) {#tgt-19-6-1}

Dieses Release umfasst die folgenden neuen Funktionen und Erweiterungen:

### Visual Experience Composer (VEC)

* **Neue VEC-Menüoptionen**: Wenn Sie im VEC auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt.

   * **Stile &gt; Hintergrund**: Sie können jetzt die Option [!UICONTROL &quot;Stile&quot; &gt;&quot; Hintergrund&quot;] verwenden, um das Hintergrundbild und die Hintergrundfarbe für das ausgewählte Element zu ändern. (TGT-15001)

   * **[!UICONTROL Ersetzen Sie durch &gt; HTML]und[!UICONTROL Ersetzen Sie Ersetzen durch &gt; Erlebnisfragment]**: Wenn Sie auf ein Bild klicken, klicken Sie [!UICONTROL auf Ersetzen,]und zwei neue Optionen werden angezeigt:

      * **HTML**: Sie können ein Bild durch HTML ersetzen, um das Element vollständig zu steuern, ohne das übergeordnete Element für den Zugriff auf die HTML-Option auszuwählen.
      * **Erlebnisfragment**: Sie können ein Bild durch ein Adobe Experience Manager (AEM) [-Erlebnisfragment](/help/c-experiences/c-manage-content/aem-experience-fragments.md) ersetzen, um in AEM erstellte Elemente schnell in Target-Aktivitäten einzufügen. (TGT-34097)

* **Verbesserungen** an Clicktracking: Wir haben den Prozess zur Konfiguration der Klick-Tracking im VEC und im Einzelseitenanwendung (SPA) verbessert.

   * Während Sie Elemente auswählen, die bei der Klick-Verfolgung verwendet werden sollen, werden die Namen aller verfügbaren Elemente im Bedienfeld &quot;Modifizierungen&quot; auf der rechten Seite angezeigt, sodass die gewünschten Elemente schnell und einfach ausgewählt werden können.
   * Auf der [!UICONTROL Seite Ziele und Einstellungen] des Arbeitsablaufs für die drei Teilaktivitäten wird eine Zahl angezeigt, die die Anzahl der für die Klick-Verfolgung ausgewählten Elemente darstellt. Sie können den Mauszeiger über diese Nummer bewegen, um die Namen aller ausgewählten Elemente anzuzeigen. (TGT-33878)

### SPA VEC

* **Geführter Arbeitsablauf**: Ein neuer geführter Arbeitsablauf hilft Ihnen, zu verstehen, wie die Einstellungen für die Seitenauslieferung konfiguriert werden sollen, um eine Aktivität für Ihre einzelne Seite-App erfolgreich auszuführen und auszuführen. (TGT-33718)

* **Änderungen klonen**: Sie können jetzt eine Änderung mithilfe der SPA VEC definieren und diese Änderung dann klonen, um sie in anderen Ansichten Ihrer Einzelseitenanwendung zu verwenden. (TGT-33882)

### Mobile VEC

* **Mehrere App-Versionen**: Sie können jetzt Aktivitäten für mehrere Versionen Ihrer mobilen App erstellen. Dadurch sparen Sie Zeit und Mühe, wenn die Versionen ähnlich sind, und Sie müssen die Benutzeroberfläche der App nicht wesentlich ändern. (TGT-34231)

### ![Premium-Badge](/help/assets/premium.png) Automatisierte Personalisierung (AP) und Automatisches Targeting

* **Spezifisches Erlebnis als Steuerung**: Sie können ein Erlebnis auswählen, das beim Erstellen einer AP- oder automatisch-Targeting-Aktivität als Kontrolle verwendet werden soll. Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern. Die aktuelle Kontrolloption (zufällig bereitgestellte Erlebnisse) ist weiterhin verfügbar. (TGT-32801 und TGT-26572)

### Weitere Verbesserungen, Fehlerbehebungen und Änderungen

* Das `<BODY>` Tag wird jetzt im DOM-Pfad angezeigt, der unten im VEC angezeigt wird, wenn Sie auf ein Element auf der Seite klicken, sodass Sie Aktionen am `<BODY>` Tag durchführen können. (TGT-33736)

## Informationen zur Vorabversion {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
