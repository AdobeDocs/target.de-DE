---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5d3e5a15a262d29bd1d95af71baae52ed288b33e
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 100%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs, der [!DNL Adobe Experience Platform Web SDK] und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## Target Standard/Premium 22.2.1 (1. Februar 2022)

Diese Wartungsversion enthält die folgenden Fehlerbehebungen und Verbesserungen für die neue Benutzeroberfläche [!UICONTROL Zielgruppen], die in der Version Target Standard/Premium 22.1.2 angekündigt wurde, die in den nächsten sechs Wochen an Kunden in allen Regionen ausgeliefert wird. Diese Korrekturen passen die Funktionalität der in [!DNL Adobe Target Standard/Premium] erstellten Zielgruppen an.

* Fehlerkorrektur – Importierte Zielgruppen können jetzt von [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud] und [!DNL Adobe Target Classic] als Berichterstellungs-Zielgruppen zugewiesen werden. (TGT-43140)
* Es wurde eine Option [!UICONTROL Löschen] in der Liste [!UICONTROL Zielgruppen] für importierte Zielgruppen aus [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud] und [!DNL Adobe Target Classic] hinzugefügt. Es wurde auch eine Funktion zum Massenlöschen hinzugefügt. (TGT-42914)

## at.js-Version 2.8.1 (28. Januar 2022)

* Es wurde ein Problem behoben, wo `pageLoad` im hybriden Ausführungsmodus [!UICONTROL On Device Decisioning] (ODD) nicht auf target-global-mbox abgebildet wurde.
* Es wurde ein Problem mit Analysedetails für mbox-Anfragen behoben.
* Dev-Abhängigkeiten wurden aktualisiert, um Sicherheitslücken zu beheben.

## [!DNL Target Standard/Premium] 22.1.2 (26. Januar 2022)

| Funktion | Details |
| --- | --- |
| [!DNL Adobe Experience Platform]-Zielgruppen in [!DNL Target] | Sie können jetzt [!DNL Adobe Experience Platform]-Zielgruppen in [!DNL Target] aufnehmen und verwenden. Die Teams von [!DNL Target], [!DNL Experience Platform] [!DNL Destinations] und [!DNL Unified Profile Service] freuen sich, die allgemeine Verfügbarkeit der Anwendungsfälle „Personalisierung gleiche Seite/nächste Seite“ bekannt geben zu können.<br>Die Verwendung der in [!DNL Adobe Experience Platform] erstellten Zielgruppen liefert umfassendere Kundendaten, die zu einer wirkungsvolleren Personalisierung führen. Die [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=de){target=_blank} (RTCDP), die auf [!DNL Adobe Experience Platform] basiert, hilft Unternehmen dabei, bekannte und anonyme Daten aus verschiedenen Unternehmensquellen zusammenzuführen, um Kundenprofile zu erstellen, mit denen in Echtzeit personalisierte Kundenerlebnisse auf allen Kanälen und Geräten bereitgestellt werden können.<br>Weitere Informationen finden Sie unter [Verwenden von Zielgruppen aus Adobe Experience Platform](/help/c-target/c-audiences/audiences.md#aep) in *Erstellen von Zielgruppen* und [Anwendungsfälle für die Personalisierung der gleichen Seite und der nächsten Seite](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} im Handbuch *Ziele – Übersicht*. |
| Aktualisierung der [!UICONTROL Audiences]-Benutzeroberfläche | Im Rahmen der ständigen Bemühungen des [!DNL Adobe Target]-Teams, die Benutzerfreundlichkeit für [!DNL Target]-Anwender zu verbessern, wurden in dieser Version die Seiten [!UICONTROL Audiences] und [!UICONTROL Profilskripte] in der [!DNL Target]-Benutzeroberfläche aktualisiert. Dieses Update vereinheitlicht und standardisiert Designmuster, die zuvor nicht konsistent waren, und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:<ul><li>Die Möglichkeit, mehrere Zielgruppen gleichzeitig auszuwählen und zu löschen</li><li>Ein überarbeitetes [Design für den Audience Builder](/help/c-target/c-audiences/create-audience.md)</li><li>Unterstützung von Ausschlussregeln im Rule Builder für [!UICONTROL Zielgruppe] nbibliotheken</li><li>Ein neuer „Zielgruppe-Quelle“-Filter, der eine schnellere Zielgruppenfindung ermöglicht</li><li>Optionen für dauerhafte Suche und Filter in Sitzungen</li><li>Die Möglichkeit, Zielgruppen zwischen Arbeitsbereichen für [!DNL Target Premium]-Kunden zu verschieben.</li></ul>Weitere Informationen finden Sie unter [Zielgruppen](/help/c-target/target.md).<br>**HINWEIS**: Diese Funktion wird in den nächsten acht Wochen für Kunden in verschiedenen Regionen eingeführt. |
| Aktualisierung der [!UICONTROL Profilskript]-Benutzeroberfläche | Die [!UICONTROL Profilskripte]-Bibliothek wurde ebenfalls aktualisiert und enthält eine aktualisierte Benutzeroberfläche sowie mehrere Produktivitätsaktualisierungen:<ul><li>Die Möglichkeit, mehrere Profilskripte gleichzeitig auszuwählen und zu löschen</li><li>Ein neuer Codeeditor für Profilskripte</li><li>Syntaxhervorhebung und Fehlerprüfung im Code-Editor</li><li>Token-Parameter („mbox“ oder „profile“) über Tastaturbefehle automatisch ausfüllen</li></ul>Weitere Informationen finden Sie unter [Besucherprofile](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**HINWEIS**: Diese Funktion wird in den nächsten acht Wochen für Kunden in verschiedenen Regionen eingeführt. |

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
