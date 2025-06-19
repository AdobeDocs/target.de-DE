---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b1bde455f686c34e7a5184868ce63db0b74e2af7
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 29%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: 19. Juni 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.6.3 (Samstag, 20. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Der aktualisierten [!UICONTROL Visual Experience Composer] (VEC)-Benutzeroberfläche wurde die Option [!UICONTROL Rearrange] hinzugefügt, um sie an die im alten VEC verfügbaren Funktionen anzupassen. (TGT-46957)
* Fehlerkorrektur - Beim Kopieren einer Aktivität von einem Arbeitsbereich in einen anderen Arbeitsbereich treten jetzt keine Fehler mehr auf, z. B. „Darf nicht null sein“ oder „Irgendetwas ist schiefgelaufen“. (TGT-52474)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Automated Segments]- und [!UICONTROL Important Attributes]-Berichte für bestimmte Aktivitäten nicht generiert wurden. (TNT-52904)
* Fehlerkorrektur - Die standardmäßige Inhaltsverarbeitung in [!UICONTROL Automated Personalization] (AP)-Aktivitäten im aktualisierten VEC stimmt jetzt mit der veralteten Benutzeroberfläche überein. Das System fügt jetzt automatisch eine `optionGroup` mit dem Namen „Standardinhalt“ mit `optionGroupLocalId = 0` hinzu, wenn keine Gruppe explizit hinzugefügt wird. Diese Gruppe umfasst die Standardoption (z. B. `optionLocalId: 0`). Wenn der Standardinhalt entfernt wird, wird auch die entsprechende Optionsgruppe entfernt. (TGT-52651)
* Es wurde ein Problem in [!UICONTROL Multivariate Test] (MVT)-Aktivitäten behoben, bei dem die Wiederverwendung eines `experienceLocalId` aus zuvor entfernten Erlebnissen fälschlicherweise nicht zulässig war. (TNT-52672)
* Es wurde ein Problem behoben, bei dem URLs an Aktivitätspositionen Abfrageparameter aufgrund von ungültigen Zeichen, wie Schrägstrichen (/), nicht anzeigen konnten. (TNT52845)
* Die Validierungsfehlermeldung für [!DNL A/B Test] Aktivitätsaktualisierungen über die Backend-API wurde verbessert. Wenn doppelte Ortsnamen vorhanden sind, wird in der Meldung jetzt deutlich angegeben: „Doppelte Namen sind nicht zulässig“ für `locations.selectors`. (TGT-52589)
* Fehlerkorrektur - Beim Aktualisieren einer Live [!UICONTROL Recommendations]-Aktivität aufgrund einer nicht erkannten Eigenschaft in der Anfrage-Payload tritt jetzt kein Fehler mehr auf. Das System verarbeitet jetzt ordnungsgemäß die „Ungültige JSON. Fehler „Nicht erkannter Eigenschaftsname“. (TNT52723)
* Fehlerkorrektur - Beim Speichern einer [!UICONTROL Recommendations]-Aktivität tritt jetzt kein Backend-Validierungsfehler mehr auf, der den Fehler „400 Bad Request“ verursacht. (TNT-52716)
* Fehlerkorrektur - Beim Bewegen des Mauszeigers über eine Mbox mit Sonderzeichen in der Dropdown-Liste &quot;[!UICONTROL Location]&quot; in der [!UICONTROL Form-Based Experience Composer] wird der Editor jetzt nicht mehr leer angezeigt und die Meldung „Fehler beim Ausführen von „querySelector“ für „Element“ ausgegeben.“ angezeigt. (TGT-52717)
* Verbesserte Genauigkeit des Zufuhrstatus mit einem neuen „PARTIALLY_IMPORTED“-Indikator. Zuvor wurden Feeds als „Erfolg“ markiert, selbst wenn nicht alle Zeilen in einer Datei importiert wurden, was irreführend war.
* Fehlerkorrektur - Nach der Migration zu AP V2 `/admin/rest/ui/v1/campaigns` bei bestimmten API-Aufrufen an Client-seitige Fehler zurückgegeben (HTTP 4xx). (TGT-52721)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
