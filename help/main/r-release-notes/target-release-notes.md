---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b103d912b1ae953c44f2ad35da8a7ae83e7be2ae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 64%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 11. September 2023**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 23.9.3 (18. September 2023)

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Der Visual Experience Composer (VEC) wurde erweitert und unterstützt jetzt BlitzDOM (Webkomponenten). (TGT-45422)
* Es wurde ein Fehler behoben, der dazu führte, dass VEC-Aktionen in der falschen Reihenfolge angewendet wurden. In einigen Fällen führte der VEC asynchron einige Änderungen durch und das Hinzufügen zusätzlicher Änderungen an einem Element verursachte Fehler, wenn dieses Element nach einem [!UICONTROL Einfügen] Aktion. (TGT-45983)
* Es wurde ein Problem mit dem VEC behoben [!UICONTROL Überlagerung] -Funktion, um Elemente in Shadow-DOMs zu unterstützen. (TGT-46217)
* Es wurde ein Fehler behoben, der dazu führte, dass beim Öffnen einer Einzelseiten-App (SPA)-Seite im VEC und anschließendem Wechseln in den Durchsuchen-Modus die Pfeile &quot;Zurück&quot;und &quot;Weiter&quot;nicht ordnungsgemäß funktionierten. (TGT-45956)
* Es wurde ein Fehler behoben, der dazu führte, dass einige Webseiten beim Laden in VEC fehlschlugen.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.corp.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
