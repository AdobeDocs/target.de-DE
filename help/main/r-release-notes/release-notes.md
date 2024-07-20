---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 44445f269a69a3ac3e3bc88bab8abf9fc4d51663
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 100%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target]-Reporting in [!DNL Adobe Customer Journey Analytics] (8. Mai 2024)

Die Integration zwischen [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/customer-journey-analytics){target=_blank} und [!DNL Target] bietet leistungsstarke Analysen und zeitsparende Tools für Ihr Optimierungsprogramm.

Die wichtigsten Vorteile des Verwendens von [!DNL Customer Journey Analytics] als Berichtsquelle für [!DNL Target] sind folgende:

* Marketing-Fachleute können jederzeit dynamisch [!DNL Customer Journey Analytics]-Erfolgsmetriken auf [!DNL Target] Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Marketing-Fachleute können die Funktionen von [!DNL Customer Journey Analytics] wie z. B. das [Bedienfeld „Experimentieren“](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank} nutzen, um ihre Website-Personalisierung weitergehend zu analysieren.
* Marketing-Fachleute können eine einzige Quelle zum Reporting für [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/reporting/cja-ajo){target=_blank} und [!DNL Target] verwenden. Beide Personalisierungsprodukte können mit [!DNL Customer Journey Analytics] verbunden werden, um eine ganzheitlichere Ansicht Ihrer Web-Personalisierung zu erhalten.

Weitere Informationen finden Sie unter [Target-Reporting in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

## [!UICONTROL Visual Experience Composer]-Helper-Erweiterung (23. April 2024)

Die Vorgängerversion der [!DNL Target] Visual Experience Composer-Helper-Erweiterung wurde mit Manifest V2 erstellt. [!DNL Google] hat angekündigt, dass mit Manifest V2 erstellte Erweiterungen ab Juni 2024 nicht mehr zulässig sind. Weitere Informationen finden Sie unter [[!UICONTROL Visual Experience Composer]-Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] empfiehlt Kundinnen und Kunden, so schnell wie möglich auf die neuere [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) umzusteigen.

## Aktualisierungen für `Browser:iPad` und `Browser:iPhone` in [!UICONTROL Browser]-Zielgruppenattribute (30. April 2024)

| Aktualisierungen | Details |
|--- |--- |
| [!UICONTROL Browser:iPad] und [!UICONTROL Browser:iPhone] in beim Erstellen von Zielgruppen verwendeten [Browser-Attributen](/help/main/c-target/c-audiences/c-target-rules/browser.md) aktualisiert | Mit [!DNL Adobe Target] können Sie [Zielgruppen für eines von mehreren Kategorieattributen erstellen](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich der Besucherinnen und Besucher, die zum Besuch Ihrer Seite einen [bestimmten Browser oder bestimmte Browser-Optionen](/help/main/c-target/c-audiences/c-target-rules/browser.md) verwenden.<P>Ab der [!DNL Target] Standard/Premium-Version 24.3.1 (4.–6. März 2024) werden integrierte, über die Target-Benutzeroberfläche erstellte Zielgruppen wie `Browser:iPad` und `Browser:iPhone` aktualisiert, um ein korrektes Targeting für [!DNL iPad] und [!DNL iPhone] mit `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` und `profile.mobile.isTablet` durchzuführen.<P>Diese Aktualisierung erfordert keine Maßnahmen auf Kundenseite.<p><B>Wichtig</b>: Damit Kundinnen und Kunden eine korrekte Zielgruppenbestimmung für [!DNL iPad] und [!DNL iPhone] in Profilskripten (und JavaScript-Segmenten) durchführen können, müssen manuelle Änderungen auf Kundenseite bis zum **30. April 2024** vorgenommen werden. Beispiele für alternative Einstellungen, die manuell geändert werden müssen, finden Sie unter [Aktualisierungen für [!DNL iPad] und [!DNL iPhone] in [!UICONTROL Browser]-Zielgruppenattribute](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

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
