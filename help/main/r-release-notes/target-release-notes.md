---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 78bedce2134061edc48baf7023107e1dd48da2a1
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 50%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: Dienstag, 16. Januar 2023**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Veraltung von iPad und iPhone vom Browserzielgruppenattribut (30. April 2024)

| Veraltet | Details |
|--- |--- |
| [!DNL iPad] und [!DNL iPhone] nicht mehr unterstützt von der [Browserattribut](/help/main/c-target/c-audiences/c-target-rules/browser.md) wird beim Erstellen von Zielgruppen verwendet.<p>Veraltungsdatum:<P>Mittwoch, 30. April 2024 | [!DNL Adobe Target] ermöglicht [Zielgruppe für eines oder mehrere Kategorieattribute](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich der Benutzer, die eine bestimmte [Browser- oder Browseroptionen](/help/main/c-target/c-audiences/c-target-rules/browser.md) wenn sie Ihre Seite besuchen.<P><B>Ab dem 30. April 2024 werden iPad und iPhone aus der verfügbaren [!UICONTROL Browser] Typ Dropdown-Liste beim Erstellen von Kategorien für Zielgruppen.</b><P>Wenn Sie Zielgruppen haben, die iPads oder iPhones mit der [!UICONTROL Browser] müssen Sie diese Einstellungen vor dem 30. April 2024 ändern, um sicherzustellen, dass diese Zielgruppen weiterhin wie erwartet funktionieren.<P>Die folgenden Einstellungen sollten in Zukunft verwendet werden:<ul><li>[!UICONTROL Mobilnummer] > [!UICONTROL Tablette]<P>![Tablet](/help/main/r-release-notes/assets/is-tablet.png)</li><li>[!UICONTROL Mobilnummer] > [!UICONTROL Gerätemarketingname] [!UICONTROL matches] [!DNL iPad]<P>![iPad](/help/main/r-release-notes/assets/ipad.png)</li><li>[!UICONTROL Mobilnummer] > [!UICONTROL Gerätemarketingname] [!UICONTROL matches] [!DNL iPhone]<p>![iPhone](/help/main/r-release-notes/assets/iphone.png)</li></ul> |

## [!DNL Target] Standard/Premium 24.1.1 (22., 23. und 25. Januar 2024)

Diese Version ist für die folgenden Tage geplant:

* **22. Januar**: Region Europa, Naher Osten und Afrika (EMEA)
* **23. Januar**: Region Asien-Pazifik (APAC)
* **25. Januar**: Region Nord- und Südamerika

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde ein Fehler behoben, der dazu führte, dass Berichtdatumsintervalle nicht korrekt funktionierten. (TGT-47396)
* Es wurde ein Fehler behoben, der dazu führte, dass der falsche Status auf der Seite [!UICONTROL Alle Aktivitäten] Seite, nachdem Kunden eine Aktivität mithilfe der [!UICONTROL Mehr Aktionen] Symbol. (TGT-47367)
* Es wurde ein Fehler behoben, der dazu führte, dass [!UICONTROL Wichtige Attribute] nicht für einen Kunden angezeigt werden. (TGT-47272)
* Es wurde ein Fehler behoben, der dazu führte, dass die Meldung &quot;Ungültige Payload&quot;angezeigt wurde, wenn ein Kunde versuchte, &quot;Authentifizierung erforderlich&quot;zu aktivieren. (TGT-47195)
* Zahlreiche lokalisierte Zeichenfolgen in der [!DNL Target] Benutzeroberfläche.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
