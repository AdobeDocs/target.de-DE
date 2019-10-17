---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder kommenden Adobe Target-Versionen enthalten.
keywords: Versionshinweise;Versionen;Aktualisierungen;Zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen
seo-description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
seo-title: Versionshinweise zu Adobe Target
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 0a9cf0e98f5f833402b96f37df5513325222ad19

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert am: 17. Oktober 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target-Plattform

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Node.js SDK Version 1.0<br>(9. Oktober 2019) | Mit dem SDK "Target Node.js"können Sie Target serverseitig bereitstellen.<br>Dieses Node.js-SDK unterstützt Sie bei der einfachen Integration von Target in andere Experience Cloud-Lösungen, z. B. den Adobe Experience Cloud-Identitätsdienst, Adobe Analytics und Adobe Audience Manager.<br>Das Node.js-SDK stellt Best Practices vor und entfernt Komplexitäten, wenn es über unsere Bereitstellungs-API mit Adobe Target integriert wird, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können. Die folgenden bemerkenswerten Funktionen werden in der neuesten Version eingeführt:<ul><li>Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen.</li><li>Unterstützung für die Leistungsoptimierung, wenn Sie eine hybride Integration von Target sowohl auf Ihren Webseiten als auch serverseitig haben. Wir führen eine Einstellung ein, die von Erlebnissen aufgefüllt wird, die über den Server abgerufen werden, sodass at.js 2.2 keinen zusätzlichen Server-Aufruf mehr vornimmt, um die Erlebnisse abzurufen. `serverState` Dieser Ansatz optimiert die Seitenladeleistung.</li><li> Unterstützung für das Abrufen von VEC-erstellten Aktivitäten über das Node.js SDK, das durch die neue API für die Auslieferung ermöglicht wird.</li><li>Open Source, damit Ihre Entwickler zum Node.js SDK beitragen können.</li></ul>Weitere Informationen finden Sie unter [Versionshinweise - SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)für Target Node.js. |
| Auslieferungs-API<br>(9. Oktober 2019) | Ein vollständig neuer API-Endpunkt (/v1/delivery) wird in der Produktion verfügbar sein. Die wichtigsten Funktionen sind:<ul><li>Ein Endpunkt zum Abrufen von Erlebnissen für eine oder mehrere Mboxes.</li><li>Rufen Sie VEC-erstellte Aktivitäten über die API ab.</li><li>Unterstützung für ein völlig neues Objekt namens "Ansichten", das für Einzelseitenanwendungen (SPAs) und mobile Anwendungen verwendet wird.</li></ul>Weitere Informationen finden Sie unter [Versionshinweise - Serverseitige Target-APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md). |
| at.js Version 2.2<br><br>andat.js Version 1.8<br>(10. Oktober 2019) | Diese Versionen von at.js bieten:<ul><li>Verbesserte Leistung bei der Verwendung von Experience Cloud ID Service (ECID) Version 4.4 und at.js 2.2 oder at.js 1.8 auf Ihren Webseiten.</li><li>Zuvor führte die ECID zwei Sperraufrufe durch, bevor at.js Erlebnisse abrufen konnte. Dies wurde auf einen einzigen Aufruf reduziert, wodurch die Leistung deutlich verbessert wird.</li></ul> Um diese Leistungsverbesserungen nutzen zu können, bietet ein Upgrade auf at.js 2.2 oder at.js 1.8 zusammen mit ECID Library v4.4.<br>at.js 2.2 folgende Funktionen:<ul><li>**serverState**: Eine in at.js v2.2+ verfügbare Einstellung, die zur Optimierung der Seitenleistung verwendet werden kann, wenn eine Hybridintegration von Target implementiert wird. Hybrid-Integration bedeutet, dass Sie sowohl at.js v2.2+ auf Client-Seite als auch die Bereitstellungs-API oder ein Target-SDK auf Serverseite verwenden, um Erlebnisse bereitzustellen. `serverState` gibt at.js v2.2+ die Möglichkeit, Erlebnisse direkt aus Inhalten anzuwenden, die auf dem Server abgerufen und als Teil der bereitzustellenden Seite an den Client zurückgegeben werden.<br>Weitere Informationen finden Sie unter "serverState"in [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state).</li></ul> |


## Target Standard/Premium 19.10.1 (22. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) Benutzerbasierte Empfehlungen | Empfiehlt Artikel basierend auf dem Browsing, der Anzeige und dem Kaufverlauf jedes Besuchers. Diese Elemente werden allgemein als "Empfohlen für Sie"bezeichnet.<br>Mithilfe dieser Kriterien können Sie personalisierte Inhalte und Erlebnisse sowohl für neue als auch für wiederkehrende Besucher bereitstellen. Die Liste der Empfehlungen wird mit der neuesten Aktivität des Besuchers gewichtet und wird während der Sitzung aktualisiert und personalisiert, wenn der Besucher Ihre Site aufsucht. |

### Verbesserungen, Korrekturen von Problemen und Änderungen

* Änderungen an der Adobe Unified Shell.

   Adobe aktualisiert die vorhandene Shell (die schwarze Leiste oben in den [!DNL Experience Cloud] Lösungen), um Ihr Erlebnis für alle [!DNL Adobe Experience Cloud] Lösungen zu vereinheitlichen und zu verbessern.

   Es gibt keine Änderungen an den aktuellen Arbeitsabläufen. Diese scheinbar einfachen Änderungen sind so konzipiert, dass Sie Ihr Leben auf kleine, aber wichtige Weise vereinfachen können.

   Wenn Sie sich bei der [!DNL Adobe Experience Cloud]anmelden, werden Sie zur neuen Unified Shell weitergeleitet. Es sieht sehr ähnlich wie die vorherige Shell mit der schwarzen Leiste oben aus, bietet jedoch folgende Verbesserungen:

   * Einfacherer Wechsel zwischen Identitäts-Management-Systemen (IMS) oder einer anderen [!EExperience Cloud] -Lösung.
   * Verbesserte Benutzerhilfe: Zu den Suchergebnissen gehören die Ergebnisse der [!DNL Target] Produktdokumentation sowie Community-Foren und weitere Videoinhalte, sodass Sie leichter auf weitere Inhalte zugreifen können, um das Beste zu erzielen [!DNL Target]. Wir haben auch einen Feedback-Mechanismus direkt im Menü Hilfe hinzugefügt, der es einfacher macht, Probleme zu melden oder Ideen auszutauschen.
   * Verbesserte NPS-Funktionen (Net Promoter Score). Manche Kunden sahen Umfragen manchmal häufiger, als wir es uns vorgestellt hatten. [!DNL Target] Darüber hinaus wurde das Umfragemodal verwendet, um Ihren Arbeitsablauf zu stören. Wir haben diese Funktion vollständig aktualisiert, sodass sie zu einer kleinen Umfrage wird, die nicht mehr aufdringlich ist. Darüber hinaus können wir mit dem neuen Design sicherstellen, dass die Häufigkeit der Umfrage besser kontrolliert wird.
   * Verbesserter Anmeldefluss. Bisher wurden alle [!DNL Target] Kunden auf die Target-Einstiegsseite gelandet, nachdem sie auf das [!DNL Target] Symbol in der Shell geklickt hatten. Diese Seite ermöglichte es Kunden dann, mit [!DNL Target Standard/Premium], [!DNl Recommendations Classic]oder [!DNL Search&Promote], wie unten gezeigt, fortzufahren:

      ![Landingpage](/help/r-release-notes/assets/landing.png)

      Wir haben diese Landingpage für alle unsere Kunden eliminiert. Sie gelangen jetzt immer direkt zur Seite [!UICONTROL Aktivitätenliste] , indem Sie auf das [!DNL Target] Symbol klicken.

      Wenn Sie [!DNL Recommendations Classic]diese verwenden, können Sie entweder direkt zur Lösung wechseln oder über den Kurzlink, der auf der Registerkarte " [!UICONTROL Recommendations] "erstellt wurde, wie nachfolgend gezeigt:

      ![Recs Classic Deep-Link](/help/r-release-notes/assets/recs-classic.png)

      Wenn Sie verwenden [!DNL Search&Promote], müssen Sie direkt zu dem Link gehen. Der Pfad zu Search&amp;Promote von innen von wurde vollständig entfernt [!DNL Adobe Target] .
   * Benachrichtigungen für [!DNL Target] sind derzeit nicht mehr in der Dropdown-Liste [!UICONTROL Benachrichtigungen] in Shell sichtbar.
   >[!NOTE]
   >
   >Diese Funktionen werden nicht sofort bereitgestellt und auch nicht für alle Kunden gemeinsam bereitgestellt. Wir werden diese Funktionen im Laufe der nächsten Tage ab der [!DNL Target Standard/Premium] Version vom 19.10.1 (22. Oktober 2019) herausgeben.
   >
   >Im Zuge der Einführung der neuen Shell werden Sie auch einige URL-Änderungen feststellen. Alle vorherigen mit Lesezeichen versehenen Links funktionieren weiterhin, aber wir empfehlen Ihnen, neue Links mit Lesezeichen zu versehen, um das Öffnen zu beschleunigen.

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
