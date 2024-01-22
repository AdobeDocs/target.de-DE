---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 99152f66217f66174e8b6a5a7319f11b22c74b8e
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 80%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: Dienstag, 22. Januar 2024**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Einstellung der Unterstützung von iPad und iPhone für das Zielgruppenattribut „Browser“ (30. April 2024)

| Einstellung der Unterstützung | Details |
|--- |--- |
| [!DNL iPad] und [!DNL iPhone] werden bei der Erstellung von Zielgruppen im Attribut [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) nicht mehr unterstützt.<p>Einstellungsdatum:<P>30. April 2024 | Mit [!DNL Adobe Target] können Sie [Zielgruppen für eines von mehreren Kategorieattributen erstellen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich der Benutzerinnen und Benutzer, die zum Besuch Ihrer Seite einen [bestimmten Browser oder bestimmte Browser-Optionen](/help/main/c-target/c-audiences/c-target-rules/browser.md) verwenden.<P><B>Ab dem 30. April 2024 werden iPad und iPhone beim Erstellen von Zielgruppenkategorien angezeigten Dropdown-Liste der verfügbaren [!UICONTROL Browser] entfernt.</b><P>Für Zielgruppen, die mit dem Attribut [!UICONTROL Browser] auf iPads oder iPhones abzielen, müssen Sie diese Einstellungen vor dem 30. April 2024 ändern, damit diese Zielgruppen weiterhin erwartungsgemäß funktionieren.<p>Beispiele für alternative Einstellungen finden Sie unter [Veraltung von iPad und iPhone vom Browserzielgruppenattribut (30. April 2024)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation). |

## [!DNL Target] Standard/Premium 24.1.1 (22., 23. und 25. Januar 2024)

Die Veröffentlichung dieser Version ist für die folgenden Tage geplant:

* **22. Januar**: Region Europa, Naher Osten und Afrika (EMEA)
* **23. Januar**: Region Asien-Pazifik (APAC)
* **25. Januar**: Region Nord- und Südamerika

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* [!UICONTROL Analytics for Target] (A4T)-Aktivitäten mit Umsatzzielmetriken zeigten nicht &quot;Umsatz&quot;an, da der Spaltenname und die Umsatzmetrik nicht im ($)-Format in der Berichterstellung angezeigt wurden. Dies war ein kosmetisches Problem, das behoben wurde. (TGT-46995)
* Ein Problem mit nicht ordnungsgemäßer Berichtsdatierung wurde behoben. (TGT-47396)
* Ein Problem mit der falschen Statusanzeige auf der Seite [!UICONTROL Alle Aktivitäten] nach Aktivierung oder Deaktivierung einer Aktivität über das Symbol [!UICONTROL Mehr Aktionen] wurde behoben. (TGT-47367)
* Es wurde ein Fehler behoben, der dazu führte, dass [!UICONTROL Wichtige Attribute] nicht für einen einzelnen Kunden angezeigt werden. (TGT-47272)
* Es wurde ein Fehler behoben, der dazu führte, dass die Meldung &quot;Ungültige Payload&quot;angezeigt wurde, wenn ein einzelner Kunde versuchte, &quot;Authentifizierung erforderlich&quot;zu aktivieren. (TGT-47195)
* Verschiedene lokalisierte Zeichenfolgen in der [!DNL Target]-Benutzeroberfläche wurden aktualisiert.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
