---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: df7e28060a6add53e1aaed928351b4f399b19c17
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 34%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: 10. Juli 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.7.3 (Freitag, 24. Juli 2025)

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, enthält diese Version die folgenden Fehlerbehebungen und Aktualisierungen:

**Aktivitäten**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem die `buildViews`-Methode in der Builder-Klasse fälschlicherweise auf die Gesamtanzahl der Ansichten `viewMaxLocalId` wurde, anstatt auf die höchste zugewiesene `viewLocalId`. (TGT-53207)

**Formularbasierter Experience Composer**

+++Siehe Details
* Es wurde ein Problem in der [!UICONTROL Form-Based Experience Composer] behoben, das zum Absturz des Editors führte, nachdem auf das **[!UICONTROL Manage Content]** (![Symbol „Inhalt verwalten“](/help/main/assets/icons/Experience.svg) geklickt wurde, als eine [!UICONTROL Automated Personalization] (AP)-Aktivität erstellt oder bearbeitet wurde. (TGT-53047)

+++

**Recommendations**

+++Siehe Details
* Es wurde ein Problem behoben, das verhinderte, dass [!UICONTROL Catalog Search] beim Scrollen zum unteren Rand der Liste zusätzliche Ergebnisse laden konnten, wodurch das Verhalten der alten Benutzeroberfläche wiederhergestellt wurde. (TGT-53088)
* Es wurde ein Problem behoben, bei dem die Spalte [!UICONTROL Number of Products] auf der Seite [!UICONTROL Collections] in der aktualisierten [!DNL Target]-Benutzeroberfläche fehlte. Die Spalte wird jetzt korrekt angezeigt, sodass die erwartete Funktionalität wiederhergestellt wird. (TGT-53168)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Collection] Regeln nicht ordnungsgemäß nach Regeln filterten. (TGT-53254)
* Es wurde ein Problem behoben, durch das das Löschen von Elementen im [!UICONTROL Criteria Details]-Dialogfeld blockiert wurde. (TGT-53245)
* Es wurde ein Problem behoben, das das Öffnen oder Interagieren mit Produkten ohne Namen verhinderte. Dieses Problem trat auf, wenn Umgebungen ausgewählt wurden, die unbenannte Ergebnisse zurückgaben, wodurch der Zugriff auf Produktdetails verhindert wurde. (TGT-53007)
* Ein Problem wurde behoben, das dazu führte, dass die [!UICONTROL Catalog Search] abstürzte und bei der Auswahl bestimmter Produkte einen leeren Bildschirm anzeigte. (TGT-53087)

+++

**Visual Experience Composer (VEC)**

+++Siehe Details

* Fehlerkorrektur - Das Anwenden einer Änderung an einer Ansicht in VEC führt jetzt nicht mehr zu einer Duplizierung und löst den Fehler „Ungültige Benutzereingabe“ aus. (TGT-52886)
* Fehlerkorrektur - Bei der Konfiguration von Bildangeboten in Visual Experience Composer tritt jetzt kein Problem mehr mit [!UICONTROL Undo] Funktionen für die Optionen [!UICONTROL Insert Before] und [!UICONTROL Insert After] auf.

  Zuvor führte das Rückgängigmachen einer [!UICONTROL Insert Before]- oder [!UICONTROL Insert After]-Aktion bei Bildangeboten zu inkonsistentem Verhalten oder zum Fehlschlagen der korrekten Wiederherstellung der Änderung, insbesondere bei Aktivitäten, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. Dieses Problem wurde behoben, um sicherzustellen, dass die Rückgängigmachungen für diese Änderungen jetzt zuverlässig funktionieren. (TGT-52809)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
