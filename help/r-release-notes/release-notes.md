---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Erweiterungen, Fehlerbehebungen und bekannten Problemen in jeder Target Standard- und Target Premium-Version.
keywords: Versionshinweise;Neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
seo-title: 'Adobe Target-Versionshinweise (aktuell) '
solution: Target
title: Target-Versionshinweise (aktuell)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 0d7d4666b5fc0d27ccdde812ef8f1182400dd3e8

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Target-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 19.10.1 (22. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) Benutzerbasierte Empfehlungen<br>(24. Oktober 2019) | Empfiehlt Artikel basierend auf dem Browsing, der Anzeige und dem Kaufverlauf jedes Besuchers. Diese Elemente werden allgemein als "Empfohlen für Sie"bezeichnet.<br>Mithilfe dieser Kriterien können Sie personalisierte Inhalte und Erlebnisse sowohl für neue als auch für wiederkehrende Besucher bereitstellen. Die Liste der Empfehlungen wird mit der neuesten Aktivität des Besuchers gewichtet und wird während der Sitzung aktualisiert und personalisiert, wenn der Besucher Ihre Site aufsucht.<br>Weitere Informationen finden Sie unter "Benutzerbasierte Empfehlungen"in [Kriterien/Algorithmen](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms). |

### Verbesserungen, Korrekturen von Problemen und Änderungen

* Wenn Sie sich beim [!DNL Adobe Experience Cloud]System anmelden, werden Sie zur neuen Kopfzeilennavigation geleitet. Es sieht sehr ähnlich wie die vorherige Navigation mit der schwarzen Leiste oben aus, bietet jedoch die folgenden Verbesserungen:

   * Einfacherer Wechsel zwischen [!DNL Identity Management System] (IMS-)Organisationen oder zu einer anderen Lösung.
   * Verbesserte Benutzerhilfe: Zu den Suchergebnissen gehören die Ergebnisse der [!DNL Target] Produktdokumentation sowie Community-Foren und weitere Videoinhalte, sodass Sie leichter auf weitere Inhalte zugreifen können, um das Beste zu erzielen [!DNL Target]. Wir haben auch einen Feedback-Mechanismus direkt im Menü [!UICONTROL Hilfe] hinzugefügt, der es einfacher macht, Probleme zu melden oder Ideen auszutauschen.

   * Verbesserte Feedback-Funktion für Net Promoter Score (NPS), sodass der Umfragemodus Ihren Arbeitsablauf nicht stört.
   * Verbesserter Anmeldefluss. Bisher wurden alle [!DNL Target] Kunden auf der Target-Einstiegsseite gelandet, nachdem sie auf das [!DNL Target] Symbol in der Kopfzeile geklickt hatten. Auf dieser Seite konnten Kunden dann fortfahren, [!DNL Target Standard/Premium], [!DNL Search&Promote]oder [!DNL Recommendations Classic], wie unten dargestellt:

      ![Landingpage](/help/r-release-notes/assets/landing.png)

      Wir haben diese Landingpage für alle unsere Kunden eliminiert. Sie gelangen jetzt immer direkt zur Seite " [!UICONTROL Aktivitätenliste] ", indem Sie auf das [!DNL Target] Symbol in der neuen Kopfzeile der Navigationsleiste klicken.

      Wenn Sie [!DNL Recommendations Classic]diese verwenden, können Sie entweder direkt zur Lösung wechseln oder über den Kurzlink, der auf der Registerkarte " [!UICONTROL Recommendations] "erstellt wurde, wie nachfolgend gezeigt:

      ![Recs Classic Deep-Link](/help/r-release-notes/assets/recs-classic.png)

      Wenn Sie [!DNL Search&Promote]diese verwenden, müssen Sie direkt zur [Search&amp;Promote-URL](https://center.atomz.com/center/?ims=1) (https://center.atomz.com/center/?ims=1) wechseln. Der Pfad, der von innen [!DNL Search&Promote] von [!DNL Adobe Target] zu erreichen ist, wurde vollständig entfernt.

   * Benachrichtigungen für [!DNL Target] sind derzeit nicht in der Dropdown-Liste [!UICONTROL Benachrichtigungen] in der Kopfzeile verfügbar.
   >[!NOTE]
   >
   >Diese Funktionen werden nicht sofort bereitgestellt und auch nicht für alle Kunden gemeinsam bereitgestellt. Wir werden diese Funktionen im Laufe der nächsten Tage ab der [!DNL Target Standard/Premium] Version vom 19.10.1 (22. Oktober 2019) herausgeben.
   >
   >Bei der Einführung der neuen Navigationsleiste werden Sie auch einige URL-Änderungen feststellen. Alle vorherigen mit Lesezeichen versehenen Links funktionieren weiterhin, aber wir empfehlen Ihnen, neue Links mit Lesezeichen zu versehen, um das Öffnen zu beschleunigen.

## "at.js"-Versionen 2.2 und 1.8 (10. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| at.js Version 2.2<br><br>andat.js Version 1.8 | Diese Versionen von at.js bieten:<ul><li>Verbesserte Leistung bei der Verwendung von Experience Cloud ID Service (ECID) Version 4.4 und at.js 2.2 oder at.js 1.8 auf Ihren Webseiten.</li><li>Zuvor führte die ECID zwei Sperraufrufe durch, bevor at.js Erlebnisse abrufen konnte. Dies wurde auf einen einzigen Aufruf reduziert, wodurch die Leistung deutlich verbessert wird.</li></ul> Um diese Leistungsverbesserungen nutzen zu können, bietet ein Upgrade auf at.js 2.2 oder at.js 1.8 zusammen mit ECID Library v4.4.<br>at.js 2.2 folgende Funktionen:<ul><li>**serverState**: Eine in at.js v2.2+ verfügbare Einstellung, die zur Optimierung der Seitenleistung verwendet werden kann, wenn eine Hybridintegration von Target implementiert wird. Hybrid-Integration bedeutet, dass Sie sowohl at.js v2.2+ auf Client-Seite als auch die Bereitstellungs-API oder ein Target-SDK auf Serverseite verwenden, um Erlebnisse bereitzustellen. `serverState` gibt at.js v2.2+ die Möglichkeit, Erlebnisse direkt aus Inhalten anzuwenden, die auf dem Server abgerufen und als Teil der bereitzustellenden Seite an den Client zurückgegeben werden.<br>Weitere Informationen finden Sie unter "serverState"in [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state).</li></ul> |

## Target-Plattform (9. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Node.js SDK Version 1.0 | Mit dem SDK "Target Node.js"können Sie Target serverseitig bereitstellen.<br>Dieses Node.js-SDK unterstützt Sie bei der einfachen Integration von Target in andere Experience Cloud-Lösungen, z. B. den Adobe Experience Cloud-Identitätsdienst, Adobe Analytics und Adobe Audience Manager.<br>Das Node.js-SDK stellt Best Practices vor und entfernt Komplexitäten, wenn es über unsere Bereitstellungs-API mit Adobe Target integriert wird, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können. Die folgenden bemerkenswerten Funktionen werden in der neuesten Version eingeführt:<ul><li>Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen.</li><li>Unterstützung für die Leistungsoptimierung, wenn Sie eine hybride Integration von Target sowohl auf Ihren Webseiten als auch serverseitig haben. Wir führen eine Einstellung ein, die von Erlebnissen aufgefüllt wird, die über den Server abgerufen werden, sodass at.js 2.2 keinen zusätzlichen Server-Aufruf mehr vornimmt, um die Erlebnisse abzurufen. `serverState` Dieser Ansatz optimiert die Seitenladeleistung.</li><li> Unterstützung für das Abrufen von VEC-erstellten Aktivitäten über das Node.js SDK, das durch die neue API für die Auslieferung ermöglicht wird.</li><li>Open Source, damit Ihre Entwickler zum Node.js SDK beitragen können.</li></ul><br>Weitere Informationen finden Sie unter [Versionshinweise - SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)für Target Node.js. |
| Auslieferungs-API | Ein vollständig neuer API-Endpunkt (/v1/delivery) ist in der Produktion verfügbar. Die wichtigsten Funktionen sind:<ul><li>Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.</li><li>Rufen Sie VEC-erstellte Aktivitäten über die API ab.</li><li>Unterstützung für ein völlig neues Objekt namens "Ansichten", das für Einzelseitenanwendungen (SPAs) und mobile Anwendungen verwendet wird.</li></ul><br>Weitere Informationen finden Sie unter [Versionshinweise - Serverseitige Target-APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - Target-serverseitige APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu den serverseitigen APIs von Adobe Target. |
| [Versionshinweise - SDK für Target Node.js](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK Node.js. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der JavaScript-Bibliothek von Adobe Target "at.js". |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek "mbox.js"nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
