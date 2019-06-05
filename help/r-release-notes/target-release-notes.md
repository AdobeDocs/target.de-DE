---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für die neuesten oder kommenden Target-Versionen.
keywords: Versionshinweise
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für die neuesten oder kommenden Adobe Target-Versionen
seo-title: Target-Versionshinweise (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: dc51b94e88e8f0ef82066deb09a136925732c25f

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Letzte Aktualisierung: 28. Mai 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Änderungen an Release-Daten, Funktionen und anderen Informationen vorbehalten. Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.

## Target Standard/Premium 19.6.1 (25. Juni 2019) {#tgt-19-6-1}

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer (VEC) | Wenn Sie im VEC auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt. <ul><li>Sie können jetzt die [!DNL Styles > Background] Option zum Ändern des Hintergrundbilds und der Farbe für das ausgewählte Element verwenden. (TGT-15001)</li><li>Wenn Sie auf ein Bild klicken, werden [!DNL Replace With]zwei neue Optionen angezeigt: [!DNL HTML] und [Erlebnisfragment](/help/c-experiences/c-manage-content/aem-experience-fragments.md).<br> Durch das Ersetzen eines Bildes mit HTML können Sie das Element vollständig steuern, ohne das übergeordnete Element auszuwählen, um auf die HTML-Option zuzugreifen.<br>Mit Erlebnisfragmenten können Sie in Adobe Experience Manager (AEM) erstellte Elemente schnell in Target-Aktivitäten einfügen. (TGT-34097)</li><li>Wir haben den Prozess zur Konfiguration der Klick-Tracking im VEC und in der Einzelseitenanwendung VEC verbessert.<br>Während Sie Elemente auswählen, die bei der Klick-Verfolgung verwendet werden sollen, werden die Namen aller verfügbaren Elemente im Bedienfeld &quot;Modifizierungen&quot; auf der rechten Seite angezeigt, sodass die gewünschten Elemente schnell und einfach ausgewählt werden können.<br>Die [!DNL Goals & Settings] Seite des drei-teiligen Arbeitsablaufs für geführte Aktivitäten zeigt eine Zahl an, die die Anzahl der für die Klick-Verfolgung ausgewählten Elemente darstellt. Sie können den Mauszeiger über diese Nummer bewegen, um die Namen aller ausgewählten Elemente anzuzeigen. (TGT-33878) </li></ul> |
| Einzelseitenapp (SPA) Visual Experience Composer (VEC) | <ul><li>Ein neuer geführter Arbeitsablauf hilft Ihnen, zu verstehen, wie die Einstellungen für die Seitenauslieferung konfiguriert werden sollen, um eine Aktivität für Ihre einzelne Seite-App erfolgreich auszuführen und auszuführen. (TGT-33718)</li><li>Sie können jetzt eine Änderung mithilfe der SPA VEC definieren und diese Änderung dann klonen, um sie in anderen Ansichten Ihrer Einzelseitenanwendung zu verwenden. (TGT-33882)</li></ul> |
| Visual Experience Composer (VEC) von Mobile | <ul><li>Sie können jetzt Aktivitäten für mehrere Versionen Ihrer mobilen App erstellen. Dadurch sparen Sie Zeit und Mühe, wenn die Versionen sehr ähnlich sind und Sie die Benutzeroberfläche der App nicht wesentlich ändern müssen. (TGT-34231)</li></ul> |
| ![Premium badgeautomated](/help/assets/premium.png)<br>Personalisierung (AP) und automatisches Targeting von Aktivitäten: spezifisches Erlebnis als Kontrolle | <ul><li>Sie können beim Erstellen eines AP oder eines automatischen Targetings ein Control-Erlebnis auswählen. Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern. Die aktuelle Kontrolloption (zufällig bereitgestellte Erlebnisse) ist weiterhin verfügbar. (TGT-32801 und TGT-26572)</li></ul> |

### Verbesserungen, Fehlerbehebungen und Änderungen

* Das `<BODY>` Tag wird jetzt im DOM-Pfad angezeigt, der unten im VEC angezeigt wird, wenn Sie auf ein Element auf der Seite klicken, sodass Sie Aktionen am `<BODY>` Tag durchführen können. (TGT-33736)

## Informationen zur Vorabversion {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
