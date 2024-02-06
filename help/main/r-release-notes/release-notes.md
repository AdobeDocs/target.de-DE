---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 4395caa7e40717c59067eaedff5e53776768eda9
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 92%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Einstellung der Unterstützung von iPad und iPhone für das Zielgruppenattribut „Browser“ (30. April 2024)

| Einstellung der Unterstützung | Details |
|--- |--- |
| [!DNL iPad] und [!DNL iPhone] werden bei der Erstellung von Zielgruppen im Attribut [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) nicht mehr unterstützt.<p>Einstellungsdatum:<P>30. April 2024 | Mit [!DNL Adobe Target] können Sie [Zielgruppen für eines von mehreren Kategorieattributen erstellen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich der Benutzerinnen und Benutzer, die zum Besuch Ihrer Seite einen [bestimmten Browser oder bestimmte Browser-Optionen](/help/main/c-target/c-audiences/c-target-rules/browser.md) verwenden.<P><B>Ab dem 30. April 2024 werden iPad und iPhone beim Erstellen von Zielgruppenkategorien angezeigten Dropdown-Liste der verfügbaren [!UICONTROL Browser] entfernt.</b><P>Integrierte Zielgruppen, die mithilfe der [!DNL Target] Die Benutzeroberfläche wie &quot;Browser: iPad&quot;und &quot;Browser: iPhone&quot;wird automatisch in die neue Zielgruppendefinition verschoben.<p>Beispiele für alternative Einstellungen, die manuell geändert werden müssen, finden Sie unter [Veraltung von iPad und iPhone vom Browserzielgruppenattribut (30. April 2024)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation). |

## [!DNL Target] Standard/Premium 24.1.1 (22., 23. und 25. Januar 2024)

Die Veröffentlichung dieser Version ist für die folgenden Tage geplant:

* **22. Januar**: Region Europa, Naher Osten und Afrika (EMEA)
* **23. Januar**: Region Asien-Pazifik (APAC)
* **25. Januar**: Region Nord- und Südamerika

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* [!UICONTROL Analytics for Target] (A4T)-Aktivitäten mit Umsatzzielmetriken zeigten nicht „Umsatz“ als Spaltennamen an und die Umsatzmetrik wurde im Reporting nicht im ($)-Format angezeigt. Dies war ein kosmetisches Problem, das behoben wurde. (TGT-46995)
* Ein Problem mit nicht ordnungsgemäßer Berichtsdatierung wurde behoben. (TGT-47396)
* Ein Problem mit der falschen Statusanzeige auf der Seite [!UICONTROL Alle Aktivitäten] nach Aktivierung oder Deaktivierung einer Aktivität über das Symbol [!UICONTROL Mehr Aktionen] wurde behoben. (TGT-47367)
* Ein Fehler, bei dem der Bericht [!UICONTROL Wichtige Attribute] nicht angezeigt wurde, wurde behoben. (TGT-47272)
* Ein Fehler, bei dem beim Versuch, die Option „Authentifizierung erfordern“ zu aktivieren, die Meldung „Ungültige Payload“ angezeigt wurde, wurde behoben. (TGT-47195)
* Verschiedene lokalisierte Zeichenfolgen in der [!DNL Target]-Benutzeroberfläche wurden aktualisiert.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md) | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind. |
| [Versionshinweise für vorherige Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Sehen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium an. |
| [Versionshinweise zu Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de){target=_blank} | Sehen Sie sich die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an. |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| [Vorrangiges Produkt-Update von Adobe](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
