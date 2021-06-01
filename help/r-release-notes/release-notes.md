---
keywords: Versionshinweise; neue Funktionen; Versionen; Updates; Update; Version; Verbesserungen; Erweiterungen; Fehlerbehebungen; Fehlerkorrekturen; Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Versionshinweise
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: ea5a451e71f390ddacc6ccea583112dd831184dc
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 50%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**&quot;mbox.js&quot;-Einstellung**: Ab dem 31. März 2021 wird die mbox.js -Bibliothek  [!DNL Adobe Target] nicht mehr unterstützt. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
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

* [Unterstützung von ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) Entscheidungen auf dem Gerät für at.js.
* [Vorschau der ](/help/c-activities/c-activity-qa/activity-qa.md) Linkunterstützung für Automated Personalization-Aktivitäten

Mit dieser Version wird auch die Unterstützung für Microsoft Internet Explorer 10, Internet Explorer 11 und alle älteren Versionen entfernt. Microsoft Edge wird in at.js 2.5.0 und höher weiterhin unterstützt.

## Target Standard/Premium 21.4.1 (19. April 2021)

Diese Version enthält die folgenden neuen Funktionen und Erweiterungen. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| Unterstützung von Entscheidungen auf dem Gerät für at.js<br>(Datum der Bekanntgabe) | Mit der geräteübergreifenden Entscheidungsfindung können Marketingexperten und Entwickler Experimentierungen und Personalisierungen im Browser eines Benutzers bei nahezu null Latenz bereitstellen.<br>Weitere Informationen finden Sie unter  [On-Device Decisioning für at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![](/help/assets/premium.png) PremiumList-basierte Operatoren für Entitätsfilterregeln | [!DNL Target Recommendations] unterstützt neue listenbasierte Operatoren für Entitätsfilterregeln. (TGT-39234)<br>Zu den neu hinzugefügten Operatoren gehören:<br><ul><li>Ist in der Liste enthalten</li><li>ist nicht in der Liste enthalten</li><li>Liste enthält ein Element in</li><li>Liste enthält kein Element in</li><li>Liste enthält alle Elemente in</li><li>Liste enthält nicht alle Elemente in</li></ul>Weitere Informationen finden Sie unter &quot;Verfügbare Operatoren&quot;in [Verwenden dynamischer und statischer Einschlussregeln](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Diese Version enthält die folgenden Fehlerbehebungen.

* Fehlerkorrektur - Aktivitäten können jetzt synchronisiert werden, nachdem die Zielgruppe in [!UICONTROL Alle Besucher] geändert wurde. (TGT-40259)
* Fehlerkorrektur - Angebote können jetzt dupliziert werden, wenn sie an verschiedenen Stellen in [!UICONTROL Automated Personalization] -Aktivitäten verwendet werden, auch wenn die Option [!UICONTROL Duplikate nicht zulassen] aktiviert ist. (TGT-39567)
* Fehlerkorrektur - Die Seite [!UICONTROL Administration] > [!UICONTROL Scene7-Konfiguration] wird jetzt ordnungsgemäß geladen. (TGT-39918)
* Es wurde ein Fehler behoben, der dazu führte, dass Eigenschaften dem falschen Arbeitsbereich zugeordnet wurden. (TGT-39869)
* Es wurde ein Problem behoben, das zu unbegrenztem Laden führte, wenn die Anfrage nach dem Ändern der Umgebung beim Erstellen eines Empfehlungsausschlusses fehlschlug. (TGT-39948)

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
