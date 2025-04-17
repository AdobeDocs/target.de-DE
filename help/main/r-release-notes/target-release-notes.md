---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cd25bda52b7a1b916a73ca5e531a7134ba8cef4e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 43%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Freitag, 17. April 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.4.4 (17. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde eine Fehlermeldung hinzugefügt, die Benutzende anleitet, wie doppelte Optionen in einer Aktivität aufgelöst werden können. (TGT-51927)
* Es wurde ein Problem behoben, bei dem `ClickTrack` Selektoren beim Löschen von Seiten oder Erlebnissen mit Umleitungsangeboten nicht entfernt wurden. (TGT-51952)
* Es wurde ein Problem behoben, das dadurch verursacht wurde, dass leere `ClickTrack` zugelassen wurden. [!DNL Target] erfordert jetzt, dass das Auswahlfeld nicht leer sein darf. (TGT-52107)
* Es wurde ein Problem behoben, durch das Metriken fälschlicherweise mit doppelten Namen zugelassen wurden. Metriken erfordern jetzt eindeutige Namen. (TGT-52201)
* Es wurde ein Problem behoben, bei dem Zielgruppendefinitionen beim Bearbeiten des Targeting auf Angebotsebene in [!UICONTROL Automated Personalization] (AP)-Aktivitäten nicht sichtbar waren. (TGT-52148)
* Es wurde ein Problem behoben, das Kunden mit [!UICONTROL Editor] daran hinderte, Aktivitäten zu speichern. (TGT-52227)
* `OptionLocalIDs` nicht mehr falsch inkrementiert, wenn die Option unverändert bleibt. (TGT-52139)
* Fehlerkorrektur - Beim Erstellen einer Aktivität wird jetzt nicht mehr die Meldung „Ungültiger `optionLocalIds`&quot; angezeigt. (TGT-52154)
* Die Diskrepanzen zwischen den für eine Aktivität definierten `OptionLocalIDs` und den für die Definition von Erlebnissen definierten Diskrepanzen wurden behoben. (TGT-52215)
* Fehlerkorrektur - Beim Erstellen einer A/B-Aktivität tritt jetzt kein Validierungsfehler mehr auf. (TGT-51923)

## Aktualisierung der Target-Berechtigungen (22. April 2025)

Diese zukünftige Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Product]- und [!UICONTROL Solutions]-Administratoren die Einstellungen in den [!UICONTROL Administration] Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die [!UICONTROL Administration].

Weitere Informationen finden Sie unter [Verwaltung von Target](/help/main/administrating-target/start-target.md).

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
