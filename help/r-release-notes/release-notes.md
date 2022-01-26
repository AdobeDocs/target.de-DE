---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 8d252255499dd8ece5e1de1220a97723659a4bf8
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 75%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs, der [!DNL Adobe Experience Platform Web SDK] und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## [!DNL Target Standard/Premium] 22.1.2 (26. Januar 2022)

| Funktion | Details |
| --- | --- |
| [!DNL Adobe Experience Platform] Zielgruppen in [!DNL Target] | Sie können jetzt verwenden und [!DNL Adobe Experience Platform] Zielgruppen in [!DNL Target]. Die [!DNL Target] Team, [!DNL Experience Platform] [!DNL Destinations] und [!DNL Unified Profile Service] -Team freut sich, die allgemeine Verfügbarkeit der Anwendungsfälle &quot;Gleiche Seite/Nächste Seitenpersonalisierung&quot;bekannt geben zu können.<br>Verwenden von in erstellten Zielgruppen [!DNL Adobe Experience Platform] bietet umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen. Die [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCP), basierend [!DNL Adobe Experience Platform] hilft Unternehmen dabei, bekannte und anonyme Daten aus verschiedenen Unternehmensquellen zusammenzuführen, um Kundenprofile zu erstellen, mit denen in Echtzeit personalisierte Kundenerlebnisse auf allen Kanälen und Geräten bereitgestellt werden können.<br>Weitere Informationen finden Sie unter [Verwenden von Zielgruppen aus Adobe Experience Platform](/help/c-target/c-audiences/audiences.md#aep) in *Erstellen von Zielgruppen*. |
| Aktualisierung der [!UICONTROL Audiences]-Benutzeroberfläche | Im Rahmen der ständigen Bemühungen des [!DNL Adobe Target]-Teams, die Benutzerfreundlichkeit für [!DNL Target]-Anwender zu verbessern, wurden in dieser Version die Seiten [!UICONTROL Audiences] und [!UICONTROL Profilskripte] in der [!DNL Target]-Benutzeroberfläche aktualisiert. Dieses Update vereinheitlicht und standardisiert Designmuster, die zuvor nicht konsistent waren, und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:<ul><li>Die Möglichkeit, mehrere Zielgruppen gleichzeitig auszuwählen und zu löschen</li><li>Ein überarbeitetes [Design für den Audience Builder](/help/c-target/c-audiences/create-audience.md)</li><li>Unterstützung von Ausschlussregeln im Rule Builder für [!UICONTROL Zielgruppe] nbibliotheken</li><li>Ein neuer „Zielgruppe-Quelle“-Filter, der eine schnellere Zielgruppenfindung ermöglicht</li><li>Optionen für dauerhafte Suche und Filter in Sitzungen</li><li>Die Möglichkeit, Zielgruppen zwischen Arbeitsbereichen zu verschieben für [!DNL Target Premium] -Kunden.</li></ul>Weitere Informationen finden Sie unter [Zielgruppen](/help/c-target/target.md).<br>**NOTE**: Diese Funktion wird in den nächsten sechs Wochen für Kunden in verschiedenen Regionen eingeführt. |
| Aktualisierung der [!UICONTROL Profilskript]-Benutzeroberfläche | Die [!UICONTROL Profilskripte]-Bibliothek wurde ebenfalls aktualisiert und enthält eine aktualisierte Benutzeroberfläche sowie mehrere Produktivitätsaktualisierungen:<ul><li>Die Möglichkeit, mehrere Profilskripte gleichzeitig auszuwählen und zu löschen</li><li>Ein neuer Codeeditor für Profilskripte</li><li>Syntaxhervorhebung und Fehlerprüfung im Code-Editor</li><li>Token-Parameter („mbox“ oder „profile“) über Tastaturbefehle automatisch ausfüllen</li></ul>Weitere Informationen finden Sie unter [Besucherprofile](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**NOTE**: Diese Funktion wird in den nächsten sechs Wochen für Kunden in verschiedenen Regionen eingeführt. |

## [!DNL Target Standard/Premium] 22.1.1 (12. Januar 2022)

Diese Version umfasst Fehlerbehebungen und erforderliche Funktionen für zukünftige Integrationen.

## at.js-Version 2.8.0 (7. Januar 2022)

Die at.js-JavaScript-Bibliothek von [!DNL Target] erfasst jetzt Daten zur Nutzung von Funktionen und Daten der Leistungsmessung. Personenbezogene Daten werden nicht erfasst. Eine Abwahl dieser Funktion ist verfügbar, indem `telemetryEnabled` in `targetGlobalSettings` auf „false“ gesetzt wird. Weitere Informationen finden Sie unter [telemetryEnabled in targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#telemetry).

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
