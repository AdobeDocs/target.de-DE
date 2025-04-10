---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 2e3191da2ac21f51fa6e08af615659db1ccdd2d9
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 28%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: Freitag, 10. April 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.4.3 (10. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der Kunden daran hinderte, das Popup-Fenster mit Zielgruppeninformationen für bestimmte [!UICONTROL Experience Targeting] (XT)-Aktivitäten zu öffnen. (TGT-52049)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine [!UICONTROL Experience Fragment] in den Standardarbeitsbereich einzufügen. (TGT-52073)
* Es wurde ein Problem behoben, bei dem ein Angebot als „Inhalt nicht gefunden“ angezeigt wurde und für eine [!UICONTROL Automated Personalization] (AP)-Aktivität nicht auf der [!UICONTROL Offers] angezeigt wurde. (TGT-52150)
* Es wurde die Möglichkeit hinzugefügt, innerhalb einer Aktivität doppelte Zielgruppen zuzulassen. (TGT-51200)
* Fehlerkorrektur - Nach der Bearbeitung wird für eine XT-Aktivität auf der Seite [!UICONTROL Goals & Settings] der falsche Mbox-Name angezeigt. (TGT-52026)
* Es wurde ein Problem behoben, bei dem `defaultContent` in Optionen angezeigt wurden, obwohl sie nicht in `experiences/optionLocations` waren. (TGT-52036)
* Es wurde ein Problem behoben, um sicherzustellen, dass leere Zeichenfolgen nicht in Nullwerte konvertiert werden. (TGT-52037)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden die [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] auf der [!UICONTROL Goals & Settings] Seite nach der Bearbeitung neu konfigurieren mussten. (TGT-52071)
* Es wurde ein Problem behoben, bei dem bei einer Aktivität ohne Seitenbereitstellungsregeln mehrere Regeln auf der [!UICONTROL Overview] angezeigt wurden. (TGT-52084)
* Es wurde eine Fehlermeldung für Benutzer hinzugefügt, die versuchen, ein Angebot mit Zeichen außerhalb der mehrsprachigen Basisebene wie Emojis zu speichern. (TGT-52105)
* Fehlerkorrektur - Beim Öffnen einer Aktivität wird jetzt nicht mehr die Fehlermeldung „Diese Aktivität verwendet eine oder mehrere Zielgruppen, die an der Quelle gelöscht wurden.“ (TGT-52120)
* Es wurde ein Problem behoben, bei dem ClickTrack-Metriken während der Bearbeitung nicht im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) angezeigt wurden. (TGT-52152)
* Es wurde ein Problem behoben, bei dem eine URL mit einem Abfrageparameter als Speicherort der Aktivität den Abfrageparameter auf der Seite [!UICONTROL Overview] der Aktivität nicht anzeigte. (TGT-51635)
* Es wurde ein Problem behoben, das die Anzeige der gesamten Erlebnis-URL in [!UICONTROL Browse mode] im [!UICONTROL Visual Experience Composer] (VEC) verhinderte. (TGT-52101)
* Es wurde ein Problem behoben, bei dem die Bearbeitung einer Aktivität dazu führte, dass die Seitenbereitstellung am Ende der URL ein &quot;/&quot; hinzufügte, wodurch sie ungültig wurde. (TGT-52114)
* Es wurde ein Problem behoben, bei dem der [!UICONTROL Activity QA]-Link im [!UICONTROL Form-Based Experience Composer] fälschlicherweise zur [!DNL Adobe Experience Cloud] Homepage umgeleitet wurde. (TGT-52055)
* Es wurde ein Problem behoben, bei dem zusätzliche Seiten, die zur [!UICONTROL A/B Test] hinzugefügt wurden, nach dem Speichern und erneuten Öffnen nicht beibehalten wurden. (TGT-51994)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Stile im Abschnitt Inline-Stil zu löschen. (TGT-52070)
* Der Zugriff auf [Karten für Zielgruppendefinitionen](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) im Dialogfeld &quot;[!UICONTROL Activity QA]&quot; wurde wiederhergestellt, ähnlich wie in der veralteten Benutzeroberfläche. (TGT-52056)
* Die aktualisierte Benutzeroberfläche hat Seiten oder Zielgruppen nicht ohne Änderungen gespeichert. Wenn Kundinnen und Kunden einer Aktivität neue Seiten oder Zielgruppen hinzugefügt, diese jedoch nicht geändert haben, haben [!DNL Target] die unveränderten Zielgruppen beim Speichern verworfen. An relevanten Stellen wurden Benachrichtigungen hinzugefügt, um Benutzer über dieses Verhalten zu informieren. (TGT-52104)

## [!DNL Target Standard/Premium] 25.4.4 (15. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde eine Fehlermeldung hinzugefügt, die Benutzende anleitet, wie doppelte Optionen in einer Aktivität aufgelöst werden können. (TGT-51927)
* Es wurde ein Problem behoben, bei dem ClickTrack-Selektoren beim Löschen von Seiten oder Erlebnissen mit Umleitungsangeboten nicht entfernt wurden. (TGT-51952)
* Es wurde ein Problem behoben, bei dem [!DNL Target] ein &quot;#&quot;-Zeichen in der Aktivitäts-URL nicht korrekt erkannte. (TGT-52093)
* Es wurde ein Problem behoben, bei dem Zielgruppendefinitionen beim Bearbeiten des Targeting auf Angebotsebene in [!UICONTROL Automated Personalization] (AP)-Aktivitäten nicht sichtbar waren. (TGT-52148)
* Es wurde ein Problem behoben, bei dem Zielgruppenverfeinerungen und Aktivitäts-Targeting-Zielgruppen in der Benutzeroberfläche umgekehrt wurden. (TGT-52158)

## Aktualisierung der Target-Berechtigungen (22. April 2025)

Diese zukünftige Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Product]- und [!UICONTROL Solutions]-Administratoren die Einstellungen in den [!UICONTROL Administration] Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die [!UICONTROL Administration].

Weitere Informationen finden Sie unter [Verwaltung von Target](/help/main/administrating-target/start-target.md).

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
