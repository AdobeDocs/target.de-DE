---
keywords: Versionshinweise; neue Funktionen; Versionen; Updates; Update; Version; Verbesserungen; Erweiterungen; Fehlerbehebungen; Fehlerkorrekturen; Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Versionshinweise
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: bdf8fdc0c7d92cb59270518861693ec22eb596f2
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 50%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für clientseitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## Python SDK 1.0.0 (16. Juni 2021)

Das neue [!DNL Adobe Target] Python-SDK mit Funktionen zur geräteübergreifenden Entscheidungsfindung ist jetzt verfügbar. Diese neueste Erweiterung verstärkt die [!DNL Target]-Suite der Server-seitigen SDKs. Diese SDKS helfen Ihnen bei der Integration mit [!DNL Target] und beschleunigen Ihre Wertungszeit in der Sprache Ihrer Wahl. Serverseitige Integrationen werden immer beliebter, da sich der Markt in eine Cookie-lose Welt verlagert, in der Erstanbieterdaten wertvoll sind. Target-SDKs sind in den beliebtesten Programmiersprachen auf dem Markt verfügbar (Python, Java, JavaScript, C# / .Net).

Weitere Informationen finden Sie in der [Python SDK-Dokumentation](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/python-sdk) im Handbuch [Adobe Target SDKs](https://adobetarget-sdks.gitbook.io/docs/).

## Target Standard/Premium 21.5.1 (7. Juni 2021)  

Diese Version umfasst die folgenden Verbesserungen:

| Funktion | Details |
| --- | --- |
| ![Premium ](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL badgeCatalog ] SearchAPI | Durchsuchen Sie Ihren [!DNL Recommendations] Produkt- und Inhaltskatalog programmgesteuert per API, um Elemente zu identifizieren, die einem Suchkriterium entsprechen, und vereinfachen Sie die Verwaltung Ihres Katalogs.<br>**Einschränkungen und Hinweise**:<ul><li>Die Katalogsuche per API wird nicht für Umgebungen mit mehr als 2.000.000 Elementen unterstützt.</li><li>Katalogsuchergebnisse über API werden schneller aktualisiert als Katalogsuchergebnisse über die [!DNL Target] -Benutzeroberfläche. Die Katalogsuche in der Benutzeroberfläche [!DNL Target] kann länger dauern, bis die neuesten Ergebnisse angezeigt werden.</li></ul>Weitere Informationen finden Sie unter [Suchen nach Entitäten](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) im Handbuch *[!DNL Adobe Target][!DNL Recommendations] API* . |

Dieses Release Maintenance Release enthält die folgenden Fehlerbehebungen.

* Es wurde ein Fehler behoben, der dazu führte, dass der Standardarbeitsbereich beim Aktualisieren der Seite [!UICONTROL Zielgruppen] in einen anderen Arbeitsbereich geändert wurde. (TGT-38871)
* Es wurde ein Problem in [!UICONTROL Administration] > [!UICONTROL Implementierung] behoben, das manchmal eine Fehlermeldung verursachte, in der stand: &quot;Ihre globale Mbox ist möglicherweise nicht synchronisiert. Bitte versuchen Sie es zu retten.&quot;

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] badgeversion 2.5.0 (1. Juni 2021)

Diese Version von [!DNL Platform Web SDK] unterstützt Folgendes:

| Funktion | Details |
| --- | --- |
| Umleitungs-Unterstützung mit [!UICONTROL Analytics for Target] (A4T) | Das Platform Web SDK unterstützt jetzt [!DNL Target]-Umleitungen bei der Verwendung von [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Weitere Informationen finden Sie unter  [Analytics  [!DNL Target] für die Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## at.js-Version 2.5.0 (13. Mai 2021)

Diese Version von at.js umfasst die folgenden Verbesserungen und Änderungen:

* Unterstützung der [geräteinternen Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) für at.js.
* Unterstützung für [Vorschau-Links](/help/c-activities/c-activity-qa/activity-qa.md) für Automated Personalization-Aktivitäten

Mit dieser Version wird auch die Unterstützung für Microsoft Internet Explorer 10, Internet Explorer 11 und alle älteren Versionen entfernt. Microsoft Edge wird in at.js 2.5.0 und höher weiterhin unterstützt.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority-Produktaktualisierung | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
