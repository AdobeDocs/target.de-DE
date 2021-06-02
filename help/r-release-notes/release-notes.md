---
keywords: Versionshinweise; neue Funktionen; Versionen; Updates; Update; Version; Verbesserungen; Erweiterungen; Fehlerbehebungen; Fehlerkorrekturen; Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Versionshinweise
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: ea5a451e71f390ddacc6ccea583112dd831184dc
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 84%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für clientseitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] badgeversion 2.6.0 (1. Juni 2021)

Diese Version von [!DNL Platform Web SDK] unterstützt Folgendes:

| Funktion | Details |
| --- | --- |
| Umleitungs-Unterstützung mit [!UICONTROL Analytics for Target] (A4T) | Das Platform Web SDK unterstützt jetzt [!DNL Target]-Umleitungen bei der Verwendung von [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Weitere Informationen finden Sie unter  [Analytics  [!DNL Target] für die Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |
| Antwort-Token | Das Platform Web SDK unterstützt jetzt [!DNL Target] Antwort-Token.<br>Weitere Informationen finden Sie unter  [Antwort-Token](/help/administrating-target/response-tokens.md). |

## at.js-Version 2.5.0 (13. Mai 2021)

Diese Version von at.js umfasst die folgenden Verbesserungen und Änderungen:

* Unterstützung der [geräteinternen Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) für at.js.
* Unterstützung für [Vorschau-Links](/help/c-activities/c-activity-qa/activity-qa.md) für Automated Personalization-Aktivitäten

Mit dieser Version wird auch die Unterstützung für Microsoft Internet Explorer 10, Internet Explorer 11 und alle älteren Versionen entfernt. Microsoft Edge wird in at.js 2.5.0 und höher weiterhin unterstützt.

## Target Standard/Premium 21.4.1 (19. April 2021)

Diese Version beinhaltet die folgenden neuen Funktionen und Verbesserungen. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| Unterstützung von geräteinterner Entscheidungsfindung für at.js<br>(Datum wird noch bekannt gegeben) | Die geräteinterne Entscheidungsfindung ermöglicht es Marketing-Experten und Entwicklern, Experimente und Personalisierungen im Browser eines Benutzers mit einer Latenz von nahezu null durchzuführen.<br>Weitere Informationen finden Sie unter [Geräteinterne Entscheidungsfindung für at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![Premium](/help/assets/premium.png) Listenbasierte Operatoren für Entitätsfilterregeln | [!DNL Target Recommendations] unterstützt neue listenbasierte Operatoren für Entitätsfilterregeln. (TGT-39234)<br>Neu hinzugefügte Operatoren:<br><ul><li>Ist in Liste enthalten</li><li>Ist nicht in Liste enthalten</li><li>Liste enthält ein Element in</li><li>Liste enthält kein Element in</li><li>Liste enthält alle Elemente in</li><li>Liste enthält nicht alle Elemente in</li></ul>Weitere Informationen finden Sie in „Verfügbare Operatoren“ unter [Verwenden dynamischer und statischer Einschlussregeln](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Diese Version enthält die folgenden Fehlerbehebungen.

* Es wurde ein Fehler behoben, der dazu führte, dass eine Aktivität nach dem Ändern der Zielgruppe in [!UICONTROL Alle Besucher] nicht synchronisiert werden konnte. (TGT-40259)
* Es wurde ein Fehler behoben, der verhinderte, dass Angebote dupliziert wurden, wenn sie an verschiedenen Stellen in Aktivitäten vom Typ [!UICONTROL Automated Personalization] verwendet wurden, obwohl die Option [!UICONTROL Duplikat nicht zulassen] aktiviert war. (TGT-39567)
* Es wurde ein Fehler behoben, der verhinderte, dass die Seite [!UICONTROL Administration] > [!UICONTROL Konfiguration für Scene7] ordnungsgemäß geladen wurde. (TGT-39918)
* Es wurde ein Fehler behoben, der dazu führte, dass Eigenschaften dem falschen Arbeitsbereich zugeordnet wurden. (TGT-39869)
* Es wurde ein Problem behoben, das zu einem unbegrenzten Ladevorgang führte, wenn die Anfrage nach der Änderung der Umgebung beim Erstellen eines Ausschlusses für Empfehlungen fehlschlug. (TGT-39948)

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
