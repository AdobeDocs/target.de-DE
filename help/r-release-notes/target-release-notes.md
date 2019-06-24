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
source-git-commit: a30f868c49bca7a0c017d272b435a6a351c6e9a6

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert: 7. Juni 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungsdaten, Funktionen und andere Informationen können ohne vorherige Benachrichtigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 19.6.1 (25. Juni 2019) {#tgt-19-6-1}

Dieses Release umfasst die folgenden neuen Funktionen und Erweiterungen:

| Funktion / Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer (VEC) | **Neue VEC-Menüoptionen**: Wenn Sie im VEC auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt.<ul><li>You can now use the [!UICONTROL Styles &gt; Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>**Verbesserungen** an Clicktracking: Wir haben den Prozess zur Konfiguration der Klick-Tracking im VEC und im Einzelseitenanwendung (SPA) verbessert.<ul><li>Während Sie Elemente auswählen, die bei der Klick-Verfolgung verwendet werden sollen, werden die Namen aller verfügbaren Elemente im Bedienfeld &quot;Modifizierungen&quot; auf der rechten Seite angezeigt, sodass die gewünschten Elemente schnell und einfach ausgewählt werden können.</li><li>The [!UICONTROL Goals &amp; Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. Sie können den Mauszeiger über diese Nummer bewegen, um die Namen aller ausgewählten Elemente anzuzeigen. (TGT-33878)</li></ul> |
| Visual Experience Composer für Einzelseiten-Apps (SPA VEC) | **Geführter Arbeitsablauf**: Ein neuer geführter Arbeitsablauf hilft Ihnen, zu verstehen, wie die Einstellungen für die Seitenauslieferung konfiguriert werden sollen, um eine Aktivität für Ihre einzelne Seite-App erfolgreich auszuführen und auszuführen. (TGT-33718)<br>**Clone modifications**: You can now define a modification using the SPA VEC and then clone that modification for use in other views in your Single Page App. (TGT-33882) |
| Mobile Visual Experience Composer | **Mehrere App-Versionen**: Sie können jetzt Aktivitäten für mehrere Versionen Ihrer mobilen App erstellen. Dadurch sparen Sie Zeit und Mühe, wenn die Versionen ähnlich sind, und Sie müssen die Benutzeroberfläche der App nicht wesentlich ändern. (TGT-34231) |
| ![Premium-Badge](/help/assets/premium.png) Automatisierte Personalisierung (AP) und Automatisches Targeting | **Spezifisches Erlebnis als Steuerung**: Sie können ein Erlebnis auswählen, das beim Erstellen einer AP- oder automatisch-Targeting-Aktivität als Kontrolle verwendet werden soll. Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern. Die aktuelle Kontrolloption (zufällig bereitgestellte Erlebnisse) ist weiterhin verfügbar. (TGT-32801 &amp; TGT-26572)<br>**Personalization Insights reports**: The marketer-friendly naming for attributes when a visitor sees a specific piece of content in a specific location provides more meaningful information. (TGT-33326 und TGT-34957) |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
