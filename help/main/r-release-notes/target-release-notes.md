---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 203c0ca94b198ee7ce8379731d31d32b27cb8a0d
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 31%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Donnerstag, 2. April 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Aktualisierung der Target-Berechtigungen (22. April 2025)

Diese zukünftige Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Product]- und [!UICONTROL Solutions]-Administratoren die Einstellungen in den [!UICONTROL Administration] Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die [!UICONTROL Administration].

Weitere Informationen finden Sie unter [Verwaltung von Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.3 (10. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem der [!UICONTROL Activity QA]-Link im [!UICONTROL Form-Based Experience Composer] fälschlicherweise zur [!DNL Adobe Experience Cloud] Homepage umgeleitet wurde. (TGT-52055)
* Es wurde eine Fehlermeldung hinzugefügt, die Benutzende anleitet, wie doppelte Optionen in einer Aktivität aufgelöst werden können. (TGT-51927)

## [!DNL Target Standard/Premium] 25.4.2 (8. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem zusätzliche Seiten, die zur [!UICONTROL A/B Test] hinzugefügt wurden, nach dem Speichern und erneuten Öffnen nicht beibehalten wurden. (TGT-51994)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Stile im Abschnitt Inline-Stil zu löschen. (TGT-52070)
* Der Zugriff auf [Karten für Zielgruppendefinitionen](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) im Dialogfeld &quot;[!UICONTROL Activity QA]&quot; wurde wiederhergestellt, ähnlich wie in der veralteten Benutzeroberfläche. (TGT-52056)
* Die aktualisierte Benutzeroberfläche hat Seiten oder Zielgruppen nicht ohne Änderungen gespeichert. Wenn Kundinnen und Kunden einer Aktivität neue Seiten oder Zielgruppen hinzugefügt, diese jedoch nicht geändert haben, haben [!DNL Target] die unveränderten Zielgruppen beim Speichern verworfen. An relevanten Stellen wurden Benachrichtigungen hinzugefügt, um Benutzer über dieses Verhalten zu informieren. (TGT-52104)

## [!DNL Target Standard/Premium] 25.4.1 (2. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der dazu führte, dass Erlebnis-Zielgruppen aus -Aktivitäten verschwanden. (TGT-52003)
* Fehlerkorrektur - Beim Versand treten jetzt keine unerwarteten Elemente mehr auf. (TGT-52011)
* Es wurde ein Problem behoben, durch das Kunden die Anzeige der Zielgruppe im Targeting-Diagramm auf der [!UICONTROL r]-Seite und während der Aktivitätsbearbeitung nicht sehen konnten. (TGT-52050)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Erlebnisse in [!UICONTROL Experience Targeting] (XT)-Aktivitäten nach Priorität neu anzuordnen. (TGT-52054)
* Es wurde ein Problem behoben, das beim Rückgängigmachen von Textstil-Änderungen zu falschem Rendering führte. (TGT-51876)
* Es wurde ein Problem behoben, durch das [!DNL Target] beim Ändern eines Umleitungsangebots auch alle [!UICONTROL ClickTrack] entfernt, die mit diesem Angebot verknüpft sind. (TGT-51936)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Target] beim Abbrechen von [!UICONTROL ClickTrack] die Auswahl fälschlicherweise speicherte. (TGT-51937)
* Es wurde ein Problem behoben, das nach dem Öffnen und Schließen der Mbox-Auswahl auf der [!UICONTROL Goals & Settings] ohne Änderungen zu einem Fehler wegen ungültigem Namen führte. (TGT-51983)
* Es wurde ein Problem behoben, das die Bearbeitung von Ad-hoc-Angeboten blockierte, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. (TGT-51984)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten blockierte, die Ad-hoc-Angebote mit benutzerdefiniertem Code enthielten. (TGT-51995)
* Es wurde ein Problem behoben, das dazu führte, dass Ausschlussregeln beim Bearbeiten kombinierter Zielgruppendefinitionen als Einschlussregeln angezeigt wurden. (TGT-51999)
* Ein Problem wurde behoben, das dazu führte, dass benutzerdefinierter Code während der Erlebnisbearbeitung nicht korrekt angezeigt wurde. (TGT-52005)
* Es wurde ein Problem behoben, durch das die [!UICONTROL Insert Before]-Option zum Einfügen von Inhalten vor der Navigationsleiste nicht mehr verfügbar war. (TGT-52031)
* Fehlerkorrektur - Das Standarderlebnis in Berichten wird jetzt korrekt hervorgehoben. (TGT-51716)
* Es wurde ein Problem behoben, das beim Erstellen einer Aktivität eine `default message [Invalid optionLocalIds: xx]]` auslöste. (TGT-52038)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
