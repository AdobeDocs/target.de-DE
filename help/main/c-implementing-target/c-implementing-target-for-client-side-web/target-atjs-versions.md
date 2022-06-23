---
keywords: at.js-Versionen;at.js-Versionen;Versionshinweise
description: Details zu Änderungen in den einzelnen Versionen der Adobe anzeigen [!DNL Target] at.js-JavaScript-Bibliothek.
title: Was ist in jeder Version von at.js enthalten?
feature: at.js
role: Developer
exl-id: ec1f1459-d539-4eac-a8f1-33a2d4910dec
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '4584'
ht-degree: 84%

---

# „at.js“-Versionsdetails

Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target]

>[!IMPORTANT]
>
>Das Target-Team unterstützt beide at.js 1.*x* und at.js 2.*x*. Führen Sie ein Upgrade auf die neueste Aktualisierung einer der beiden Hauptversionen von at.js durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen.
>
>Tags in [Adobe Experience Platform](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} ist die bevorzugte Methode zum Aktualisieren von at.js. Erweiterungsentwickler fügen ihren Erweiterungen kontinuierlich neue Funktionen hinzu und beheben häufig Fehler. Diese Aktualisierungen werden in neuen Versionen einer Erweiterung zusammengefasst und im Abschnitt [!DNL Adobe Experience Platform] Katalog als Upgrades. Weitere Informationen finden Sie unter [Erweiterungs-Upgrades](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/extension-upgrade.html) im *Übersicht über Tags* Handbuch.

## at.js-Version 2.9.0 (27. Mai 2022)

* Hinzugefügt [Benutzeragenten-Client-Hinweise](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/)Unterstützung von {target=_blank}.
* Es wurde ein Fehler behoben, durch den mehrere Mbox-Anfragen auf derselben Seite unterschiedliche Impressions-IDs erhielten.

## at.js-Version 2.8.1 (28. Januar 2022)

* Es wurde ein Problem behoben, wo `pageLoad` im hybriden Ausführungsmodus [!UICONTROL On Device Decisioning] (ODD) nicht auf target-global-mbox abgebildet wurde.
* Es wurde ein Problem mit Analysedetails für mbox-Anfragen behoben.
* Dev-Abhängigkeiten wurden aktualisiert, um Sicherheitslücken zu beheben.

## at.js-Version 2.8.0 (7. Januar 2022)

Die at.js-JavaScript-Bibliothek von [!DNL Target] erfasst jetzt Daten zur Nutzung von Funktionen und Daten der Leistungsmessung. Personenbezogene Daten werden nicht erfasst. Eine Abwahl dieser Funktion ist verfügbar, indem `telemetryEnabled` in `targetGlobalSettings` auf „false“ gesetzt wird. Weitere Informationen finden Sie unter [telemetryEnabled in targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

## at.js-Version 2.7.0 (28. Oktober 2021)

Diese Version enthält die folgende Verbesserung:

* Hinzugefügte Unterstützung für [Web-Komponenten](https://developer.mozilla.org/de/docs/Web/Web_Components). Diese Version von at.js ist erforderlich, um personalisierte Erlebnisse und Angebote für benutzerdefinierte Elemente und Elemente innerhalb von benutzerdefinierten Elementen zu erstellen und zu testen. Diese Funktion ist in der Version 21.10.5 von [!DNL Target Standard/Premium] enthalten.

## at.js 1.8.3 (21. September 2021) {#183}

Diese Version enthält die folgenden Änderungen:

* Entfernt die `reactor-window` und `reactor-document` [!DNL Adobe Experience Platform Launch] -Module, um sicherzustellen, dass [!DNL Platform Launch] Funktionen für Kunden, die `window.default` oder `document-default` gesetzt.
* at.js 1.8.3 setzt jetzt explizit `Samesite=None` und `Secure` , um sicherzustellen, dass Drittanbieter-Domain-Cookies ordnungsgemäß gesetzt werden.

## at.js 2.6.1 (16. August 2021)

* Fehlerbehebung für „Für den Hybrid-Modus ist kein zwischengespeichertes Artefakt verfügbar“ bei Verwendung der geräteinternen Entscheidungsfindung.

## at.js 2.6.0 (16. Juli 2021)

* Das Attribut „secure“ wurde zu Cookies hinzugefügt für alle Fälle, in denen die at.js-Einstellungen `secureOnly` auf `true` gesetzt sind.
* Bei Verwendung von `triggerView()` sind jetzt Antwort-Token verfügbar.
* Es wurde ein Problem im Zusammenhang mit dem Ereignis `CONTENT_RENDERING_NO_OFFERS` behoben. Jetzt wird dieses Ereignis korrekt ausgelöst, wenn kein Inhalt von [!DNL Target] zurückgegeben wird.
* Details zur Klickmetrik von [!DNL Anlytics for Target] (A4T) werden bei der Verwendung von `prefetch`-Anfragen korrekt zurückgegeben.
* Die UUID-Generierung verwendet nicht mehr `Math.random()`, sondern beruht auf `window.crypto`.
* Der Ablauf des `sessionId`-Cookies wird bei jedem Netzwerkaufruf korrekt verlängert.
* Die Ansichts-Cache-Initialisierung für die [!UICONTROL Einzelseiten-Anwendung] (SPA, Single Page Application) wird jetzt korrekt verarbeitet und berücksichtigt die Einstellungen `viewsEnable`.

## at.js 2.5.0 (13. Mai 2021)

Diese Version von at.js umfasst die folgenden Verbesserungen und Änderungen:

* [Entscheidung auf dem Gerät](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/on-device-decisioning/)Unterstützung von {target=_blank} für at.js.
* Unterstützung für [Vorschau-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) für Automated Personalization-Aktivitäten

Mit dieser Version endet auch die Unterstützung für Microsoft Internet Explorer 10 und höher.

## at.js 2.4.1 (23. März 2021)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

* Es wurde ein Problem behoben, bei dem `targetPageParams` in Mbox-Anfragen enthalten waren. `targetPageParams` sollten nur in `pageLoad`-Anfragen enthalten sein. (TNT-40247)
* Optimierte Fenster- und Dokumentglobal-Verweise im [!DNL Adobe Experience Platform] -Erweiterung. (TNT-37124)

## at.js 2.4.0 (14. Januar 2021)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Fehlerbehebungen enthält:

* Den Kunden-IDs (customerIds) der Bereitstellungs-API wurde Unterstützung für eine einheitliche Profil-/Platform-ID hinzugefügt.
* Die fehlerhafte Style-Tag-Injektion wurde behoben.

## at.js 2.3.3 (13. November 2020)

Diese Version von at.js ist eine Wartungsversion, die die folgende Fehlerbehebung enthält:

* Es wurde ein Problem im Zusammenhang mit mbox click tracking und A4T behoben. Mit 0n-Klick hat Target einen Bereitstellungs-API-Aufruf mit den richtigen Mbox- und Mbox-Parametern ausgelöst. Die SDID stimmte jedoch nicht mit der im [!DNL Analytics] -Aufruf, sodass keine Trefferzuordnung und -konvertierung erfolgte. (TNT-38372)

## at.js 2.3.2 (24. Juli 2020)

Diese Version von at.js ist eine Wartungsversion, die die folgende Fehlerbehebung enthält:

* Ein Fehler wurde behoben, der auftrat, wenn dem Fenster oder Dokument durch ein Skript oder Code eine Standardeigenschaft hinzugefügt wurde.

## at.js 1.8.2 (15. Juni 2020)

Diese Version von at.js ist eine Wartungsversion, die die folgende Fehlerbehebung enthält:

* Ein Problem wurde behoben, dass dazu führte, dass at.js 1.*x* bei Verwendung von CNAME und eines Edge-Override die Serverdomäne nicht korrekt erstellte, wodurch die [!DNL Target]-Anforderung fehl schlug. (TNT-35064)

## at.js 2.3.1-Versionen (15. Juni 2020)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

* Die Einstellung `deviceIdLifetime` kann nun mit [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) überschrieben werden. (TNT-36349)
* Ein Problem wurde behoben, dass dazu führte, dass at.js 2.*x* bei Verwendung von CNAME und eines Edge-Override die Serverdomäne nicht korrekt erstellte, wodurch die [!DNL Target]-Anforderung fehl schlug. (TNT-35065)
* Ein Problem wurde behoben, dass dazu führte, dass [!DNL Target] bei Verwendung von [!DNL Adobe Analytics]  Extension v2 und der [!DNL Launch] [!DNL Target]-Erweiterung den [!DNL Analytics]-Aufruf `sendBeacon` verzögerte. (TNT-36407, TNT-35990, TNT-36000)

## at.js-Version 2.3.0 (25. März 2020)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

* Unterstützung für das Festlegen von Content Security Policy-Nonces für SCRIPT- und STYLE-Tags, die beim Anwenden von bereitgestellten Target-Angeboten an das Seiten-DOM angehängt werden. Kunden können `targetGlobalSettings.cspScriptNonce` und `targetGlobalSettings.cspStyleNonce` damit at.js die entsprechenden Skript- und Stil-Tag-Nonces für angewendete Angebote festlegen kann. Siehe  [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank} für weitere Details.
* Es wurde ein Problem beim Kompilieren von at.js mit dem Google Closure-Compiler für die Implementierung von Google Tag Manager behoben.
* &quot;at.js&quot;-Cookie für die Prüfung von `check` nach `at_check` um Kollisionen mit den Implementierungen der Kunden zu vermeiden.

## at.js-Version 1.8.1 (25. März 2020)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

* &quot;at.js&quot;-Cookie für die Prüfung von `check` nach `at_check` um Kollisionen mit den Implementierungen der Kunden zu vermeiden.

## at.js-Version 2.2.0 (10. Oktober 2019)

Diese Version von at.js umfasst die folgenden Erweiterungen und Fehlerbehebungen:

* Es wurde ein Problem behoben, bei dem Klick-Tracking keine Konversionen in Analytics for Target (A4T) meldete, wenn in Seitenelementen kein Adobe Analytics-Code vorhanden war.
* Die Leistung bei der Verwendung von Experience Cloud ID Service (ECID) v4.4 und at.js 2.2 auf Ihren Webseiten wurde verbessert.
* Bislang führte ECID zwei Sperraufrufe durch, bevor at.js Erlebnisse abrufen konnte. Dies wurde auf einen Aufruf reduziert, wodurch die Leistung deutlich verbessert wurde.
* Fehlerkorrektur - Die Verarbeitung vorab abgerufener Ansichten funktioniert jetzt ordnungsgemäß, wenn Ereignis-Token aus Standardangeboten nicht in gesendeten Benachrichtigungen enthalten sind.

   >[!NOTE]
   >
   >Aktualisieren Sie Ihre ECID-Erweiterung auf Version 4.4, um diese Leistungsverbesserung nutzen zu können.

* at.js , Version 2.2 bietet außerdem eine neue Einstellung mit dem Namen `serverState`. Diese Einstellung kann zur Optimierung der Seitenleistung verwendet werden, wenn eine Hybridintegration von Target implementiert wird. Hybrid-Integration bedeutet, dass Sie zur Bereitstellung Ihrer Erlebnisse sowohl at.js v2.2+ auf der Client-Seite als auch die Bereitstellungs-API oder ein Target-SDK auf der Server-Seite verwenden. `serverState` ermöglicht at.js v2.2+, Erlebnisse direkt aus Inhalten anzuwenden, die auf Serverseite abgerufen und als Teil der bereitzustellenden Seite an den Client zurückgegeben wurden. Weitere Informationen finden Sie unter „serverState“ in [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

## at.js-Version 1.8.0 (10. Oktober 2019)

Diese Version von at.js umfasst die folgenden Erweiterungen und Fehlerbehebungen:

* Die Leistung bei der Verwendung von Experience Cloud ID Service (ECID) v4.4 und at.js 1.8 auf Ihren Webseiten wurde verbessert.
* Bislang führte ECID zwei Sperraufrufe durch, bevor at.js Erlebnisse abrufen konnte. Dies wurde auf einen Aufruf reduziert, wodurch die Leistung deutlich verbessert wurde.

>[!NOTE]
>
>Aktualisieren Sie Ihre ECID-Erweiterung auf Version 4.4, um diese Leistungsverbesserung nutzen zu können.

## at.js Version 2.1.1 (24. Juli 2019)

Diese Version von at.js ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

(Die Problemnummern in Klammern dienen internen Adobe-Benutzern.)

* Es wurde ein Problem behoben, durch das mehrere Beacons ausgelöst wurden, wenn die Klick-Tracking-Metrik auf der Seite „Ziele und Einstellungen“ im Visual Experience Composer (VEC) verwendet wurde. (TNT-32812)
* Es wurde ein Problem behoben, durch das `triggerView()` Angebote nicht öfter als einmal gerendert hat. (TNT-32780)
* Es wurde ein Problem mit `triggerView()` behoben, sodass Anfragen jetzt Experience Cloud ID (ECID)-Informationen enthalten. (TNT-32776)
* Es wurde ein Problem behoben, durch das die `triggerView()`-Benachrichtigung auch dann nicht ausgelöst wurde, wenn keine gespeicherten Ansichten vorhanden waren. (TNT-32614)
* Es wurde ein Fehler behoben, der aufgrund der Verwendung von decodeURIcomponent auftrat, wenn die URL einen falsch formatierten Abfragezeichenparameter enthielt. (TNT-32710)
* Das Beacon-Flag ist nun im Kontext von Versandanfragen, die über die `Navigator.sendBeacon()`-API gesendet werden, auf „true“ gesetzt. (TNT-32683)
* Es wurde ein Problem behoben, durch das Recommendations-Angebote für manche Kunden nicht auf Websites angezeigt wurden. Kunden konnten zwar den Angebotsinhalt im Bereitstellungs-API-Aufruf sehen, das Angebot wurde jedoch nicht auf der Website gezeigt. (TNT-32680)
* Es wurde ein Problem behoben, durch das Klick-Tracking erlebnisübergreifend nicht wie erwartet funktionierte. (TNT-32644)
* Es wurde ein Problem behoben, durch das at.js die zweite Metrik nicht mehr anwenden konnte, wenn die Darstellung der ersten Metrik fehlgeschlagen war. (TNT-32628)
* Es wurde ein Problem beim Weiterleiten der `mboxThirdPartyId` mit der Funktion `targetPageParams` behoben, was dazu geführt hatte, dass die Payload der Anfrage weder in den Abfrageparametern noch in der Payload der Anfrage vorhanden war. (TNT-32613)
* Es wurde ein Problem behoben, durch das die Antworten auf Anzeige- und Klick-Benachrichtigungen in Chromium-basierten Browsern blockiert wurden (einschließlich Google Chrome). (TNT-32290)

## at.js-Version 2.1.0 (3. Juni 2019)

Dieses Release umfasst die folgenden Funktionen und Erweiterungen:

* **Die Opt-In-Unterstützung von Adobe**: Die Opt-In-Unterstützung bietet die Möglichkeit, Adobe-Lösungsintegrationen mit Genehmigungsverwaltungsplattformen zu vereinfachen. Weitere Informationen zu Adobe Opt-In finden Sie unter [Privatsphäre und Datenschutz-Grundverordnung (DSGVO)](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/).

* **Kompatibel mit dem Branchenstandard CSP**: at.js verwendet nicht mehr eval(), um JavaScript auszuführen.

* **Client-seitige Analyseprotokollierung**: Damit hat der Kunden die volle Kontrolle darüber, wie Analysedaten an Adobe Analytics gesendet werden, ob Client- oder Server-seitig.

   Weitere Informationen finden Sie unter [Client-seitige Analyseprotokollierung](/help/main/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Vor der Implementierung*.

* **Benachrichtigungen senden**: Erlauben Entwicklern, Benachrichtigungen zu senden, wenn ein Erlebnis durch ihren Code statt über `applyOffer()` oder `applyOffers()` gerendert wird.

   Weitere Informationen finden Sie unter [adobe.target.sendNotifications(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-sendnotifications-atjs-21/).

* **at.js-Größe um ~ 24 % verringert**: Die Größe von at.js wurde um ~ 24 % verringert. Die kleinere Dateigröße verbessert die Seitenladeleistung und verringert die Ladedauer von at.js auf der Seite.

## at.js-Version 2.0.1 (19. März 2019)

Dies ist eine Wartungsversion, die die folgenden Erweiterungen und Fehlerbehebungen enthält:

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

* Es wurde eine Race-Bedingung im DOM-Polling-Code behoben, durch die JavaScript-Ausnahmen für bestimmte Kunden verursacht wurden. (TNT-31869)
* Benachrichtigungen, die angezeigt wurden, wurden von Click-Tracking-Ereignishandlern entkoppelt. Target hat zunächst keine Benachrichtigungen gesendet, wenn Click-Ereignis-Handler, die zu einer gerenderten Ansicht gehören, nicht angehängt werden konnten. Target sendet jetzt eine Ansichtsbenachrichtigung, auch wenn Klickelemente nicht gefunden werden. (TNT-31969)
* Es wurde ein Fehler behoben, der dazu führte, dass das Ereignisumleitungsflag „request-succeeded“ immer auf „true“ gesetzt wurde. (TNT-31907)
* Es wurde ein Problem behoben, durch das die VEC-Neuanordnungs-Aktion als Erfolg protokolliert wurde, selbst wenn Elemente fehlen. (TNT-31924)
* Es wurde ein Problem behoben, durch das Benachrichtigungen für bestimmte Kunden das Eigenschafts-Token für die Unternehmensberechtigungen nicht enthalten. (TNT-31999)

## at.js-Version 1.7.1 (19. März 2019)

Diese Version ist eine Wartungsversion und beinhaltet die folgenden Fehlerbehebungen:

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

* Es wurde eine Race-Bedingung im DOM-Polling-Code behoben, durch die JavaScript-Ausnahmen für bestimmte Kunden verursacht wurden. (TNT-31869)

## „at.js“-Version 2.0.0 {#at-js-200}

at.js 2.x bietet umfassende Funktionen mit denen Ihr Unternehmen mithilfe von Client-seitigen Technologien der neuesten Generation Personalisierungen ausführen kann. Diese neue Version konzentriert sich auf die Aktualisierung von at.js, um harmonische Interaktionen mit Einzelseitenanwendungen (SPAs) zu ermöglichen.

Hier einige Vorteile der Verwendung von at.js 2.x, die in früheren Versionen nicht verfügbar sind:

* Die Möglichkeit, alle Angebote beim Laden der Seite zwischenzuspeichern, um mehrere Server-Aufrufe auf einen einzelnen Server-Aufruf zu reduzieren.
* Drastische Verbesserung der Erlebnisse Ihrer Endbenutzer auf Ihrer Site, da Angebote sofort über den Cache angezeigt werden, ohne dass die herkömmlichen Server-Aufrufe verzögert werden.
* Einfache einzeilige Code- und Einmalentwickler-Einrichtung, um Ihren Marketingmitarbeitern die Erstellung und Ausführung von A/B- und Experience-Aktivitäten (XT) über Visual Experience Composer (VEC) auf Einzelseitenanwendungen zu ermöglichen.

at.js 2.x enthält die folgenden neuen Funktionen:

* getOffers()
* applyOffers()
* triggerView()

Die folgenden Funktionen sind mit der Einführung von at.js 2.x veraltet:

* mboxCreate()
* mboxDefine
* registerExtension()

Weitere Informationen finden Sie unter [Aktualisieren von at.js 1.x auf at.js 2.x](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} und [&quot;at.js&quot;-Funktionen](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/).

>[!NOTE]
>
>Wenn Sie Adobe Opt-in-Unterstützung für die [Die Datenschutz-Grundverordnung](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/){target=_blank} (DSGVO) verwenden, müssen Sie derzeit at.js 1.7.0 oder at.js 2.1.0 verwenden.

## „at.js“-Version 1.7.0 {#at-js-170}

at.js 1.7.0 bietet Adobe Opt-in-Unterstützung. Adobe Opt-In bietet die Möglichkeit, Adobe-Lösungsintegrationen mit Genehmigungsverwaltungsplattformen zu vereinfachen.

Weitere Informationen zur Adobe Opt-in finden Sie unter [Privatsphäre und Datenschutz-Grundverordnung](https://developer.adobe.com/target/before-implement/privacy/cmp-privacy-and-general-data-protection-regulation/){target=_blank} (DSGVO).

Diese Version behebt auch ein Problem, bei dem Target möglicherweise Umleitungs-URL-Parameter mit Parametern überschreiben konnte, die aus der Umleitungs-URL stammen.

>[!NOTE]
>
>Wenn Sie für die DSGVO Adobe Opt-In-Unterstützung benötigen, müssen Sie derzeit js 1.7.0 oder 2.1.0 verwenden. <br>Eine Liste aller Versionen finden Sie unter [at.js-Versionsdetails.](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/)

## „at.js“-Version 1.6.4 {#at-js-164}

at.js 1.6.4 ist eine Wartungsversion, die folgendes Problem behebt:

* Es wurde eine Race-Bedingung in Microsoft Internet Explorer 11 behoben, die dazu führte, dass doppelte Angebote angewendet wurden.

## „at.js“-Version 1.6.3 {#section_484A56774E004282B98FFFF851E4E670}

at.js, Version 1.6.3, enthält die folgenden Fehlerbehebungen und Verbesserungen:

* Selektoren sind jetzt CSS-escaped, wenn sie IDs oder CSS-Klassen enthalten, die mit einer Ziffer, zwei Bindestrichen oder einem Bindestrich, gefolgt von einer Ziffer (z. B. #-123), beginnen. (TNT-31061)
* Es wurde ein Problem behoben, das mit at.js 1.6.2 eingeführt wurde: Angebote von Visual Experience Composer (VEC) aus verschiedenen Aktivitäten, die für denselben CSS-Selektor gelten, berücksichtigten nicht die Aktivitätenpriorität. (TNT-31052)
* Es wurde ein Problem behoben, bei dem Zeitüberschreitungen für Zusagen in Umgebungen auftraten, in denen Zusagen nativ nicht unterstützt werden. (TNT-30974)
* Probleme werden jetzt korrekt erfasst und über das Ereignis „Inhaltswiedergabe fehlgeschlagen“ gemeldet. Zuvor wurde unter Umständen gemeldet, dass JavaScript erfolgreich ausgeführt wurde, selbst wenn dies nicht der Fall war. (TNT-30599)

## „at.js“-Version 1.6.2 {#section_88BE2F69943D4280B8170F377886B58E}

Dies ist eine Wartungsversion, die folgendes Problem behebt:

* Es wurde ein Problem behoben, das auf einigen Kundensites auftrat und bei dem eine „asynchrone“ Endlosschleife auftrat.

>[!IMPORTANT]
>
>Darüber hinaus enthält at.js, Version 1.6.2, auch alle Verbesserungen und Fehlerbehebungen der Versionen 1.6.1 und 1.6.0. Diese Versionen stehen nicht mehr zum Download zur Verfügung. Wenn Sie noch Version 1.6.1 oder 1.6.0 verwenden, empfehlen wir ein Upgrade auf Version 1.6.2

Im Folgenden finden Sie einige Verbesserungen und Fehlerbehebungen in „at.js“-Version 1.6.1:

* Es wurde ein Problem in Version 1.6.0 behoben, bei dem Recommendations-Erlebnisse in Microsoft Internet Explorer 11 dupliziert wurden. (TNT-30593)
* „at.js“ stellt jetzt sicher, dass die Edge Logikprüfungen hinsichtlich der Verfügbarkeit eines Edge-Cluster-Cookies überschreiben kann, um unterschiedliche Edge-Nummern zu verhindern, wenn Benutzer während einer Sitzung zwischen Edges wechseln. (TNT-30563)
* Es wurde ein Problem behoben, bei dem „at.js“ keine nachfolgenden Aktionen durchführte, wenn der HTML-Inhalt ungültigen JS-Code enthielt. „at.js“ protokolliert jetzt jeden Fehler und rendert die verbleibenden Aktionen ohne Probleme. (TNT-30546)
* Es wurden Änderungen vorgenommen, damit eine Ausnahme auftritt, wenn eine Umleitungsseite sich erneut für eine Umleitungsaktivität qualifiziert. (TNT-30532)
* Es wurde ein Problem behoben, bei dem über die API-Anfrage „getOffer()“ nicht das richtige Anfrage-Timeout abgerufen wurde. (TNT-30498)
* Es wurde ein Problem in „at.js“-Version 1.6.0 behoben, bei dem das Speichern von Cookies bei der Verwendung des Dateiprotokolls nicht möglich war. (TNT-30454)
* Es wurde ein Problem behoben, bei dem bei der Verwendung von Analytics for Target (A4T) bei Umleitungen scheinbar nicht alle Erlebnisse bereitgestellt wurden. (TNT-30444)
* Es wurde ein Problem behoben, bei dem die Seite nach einem erfolgreichen Target-Aufruf ausgeblendet wurde. (TNT-30358)

Im Folgenden finden Sie einige Verbesserungen und Fehlerbehebungen in „at.js“-Version 1.6.0:

* Umleitungsangebote werden jetzt automatisch in der A4T-Integration (Analytics for Target) unterstützt. Der clientseitige Workaround wurde entfernt. (TNT-30247)
* Das clientseitige Edge-Routing ist jetzt standardmäßig aktiviert. (TNT-30261)
* Es wurde ein Problem mit dem Rendering von VEC-Aktionen (Visual Experience Composer) behoben, das bei Abhängigkeiten zwischen den Aktionen auftrat. (TNT-30248)

## „at.js“-Version 1.5.0 {#section_128C6761884C4DA8AE50D6A605FF6F55}

at.js Version 1.5.0 ist verfügbar.

* Die Details des Ereignisses `at-request-succeeded` enthalten das Umleitungs-Flag. Mit diesem Flag lässt sich bestimmen, ob die Seite an eine andere URL umgeleitet wird. Die URL können Sie über `at-content-rendering-redirect` ermitteln. (TNT-29834)
* Es wurde ein Problem behoben, bei dem `window.targetGlobalSettings.enabled` mit einem Laufzeitfehler fehlschlug, wenn es auf „false“ festgelegt war. (TNT-29829)
* Es wurde ein Problem behoben, bei dem das Laden einer Seite im Visual Experience Composer (VEC) fehlschlug, wenn benutzerspezifischer Code verwendet wurde, um eine globale Mbox-Anfrage auszulösen, und der Body verborgen wurde. (TNT-29795)
* Unterstützung für `screenOrientation`, `devicePixelRatio` und `webGLRenderer` wurde hinzugefügt. Diese neuen Parameter für Target-Anfragen werden verwendet, um das iPhone X und andere moderne Geräte zu erkennen. Weitere Informationen finden Sie unter [Mobilgeräte](/help/main/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89). (TNT-29781)
* Es wurde ein Problem behoben, bei dem der Hinweis zum AAM-Standort (Adobe Audience Manager) nicht immer gesendet wurde. (TNT-29695)
* Bei Browsern, die diese Funktion unterstützen, wechselt at.js 1.5.0 für den Selektorabruf zu MutationObserver. Versionen vor at.js 1.0.0 nutzten einen MutationObserver-Polyfill, der sich als problematisch erwies. Um die Polyfill-Probleme zu vermeiden, verwendet Version 1.5.0 folgenden Pseudocode, um zu entscheiden, welcher Planungsmechanismus verwendet wird:

   ```
   if MutationObserver is supported
     scheduler = MutationObserver
   else if document is visible
     scheduler = requestAnimationFrame
   else
     scheduler = setTimeout
   ```

## „at.js“-Version 1.3.0 {#section_24EAAE1CFA814EF8B19E61842F4D8321}

at.js Version 1.3.0 ist verfügbar.

* Die folgenden neuen Ereignisse stehen für die Ablaufverfolgungs-, Debugging- und Anpassungsinteraktionen mit at.js zur Verfügung:

   * LIBRARY_LOADED
   * REQUEST_START
   * CONTENT_RENDERING_START
   * CONTENT_RENDERING_NO_OFFERS
   * CONTENT_RENDERING_REDIRECT

   Weitere Informationen finden Sie unter [at.js – benutzerdefinierte Ereignisse](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-custom-events/).

* Sie können eine at.js-Anfrage um zusätzliche Parameter erweitern, die von Datenanbietern stammen. Datenanbieter sollten zu `window.targetGlobalSettings` unter `dataProviders key` hinzugefügt werden.

   Weitere Informationen finden Sie unter [Datenanbieter](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

* at.js-Anfragen verwenden nun GET. Sie wechseln jedoch zu POST, wenn die URL-Größe 2048 Zeichen überschreitet. Es gibt eine neue Eigenschaft mit dem Namen `urlSizeLimit`, wo Sie die Größenbeschränkung bei Bedarf erhöhen können. Durch diese Änderung kann Target at.js an AppMeasurement ausrichten, das dieselbe Technik verwendet.
* Target erzwingt jetzt, dass der `mbox`-Schlüssel in der `adobe.target.applyOffer(options)`-Funktion verwendet wird. Dieser Schlüssel war früher erforderlich. Target erzwingt seine Verwendung jedoch nun, um sicherzustellen, dass Target ordnungsgemäß validiert ist und Kunden die Funktion richtig verwenden.
* at.js weist eine verbesserte Ereignis- und Klick-Tracking-Funktionalität auf. at.js verwendet `navigator.sendBeacon()` zum Senden von Ereignis-Tracking-Daten und weicht zur synchronen XHR aus, wenn `navigator.sendBeacon()` nicht unterstützt wird. Dies wirkt sich hauptsächlich auf Internet Explorer 10 und 11 und einige Safari-Versionen aus. Safari unterstützt `navigator.sendBeacon()` ab der kommenden iOS 11.3-Version.
* at.js kann Angebote nun sogar dann darstellen, wenn eine Seite auf Registerkarten im Hintergrund geöffnet wird. Einige Target-Kunden haben festgestellt, dass ein Problem besteht, wenn `requestAnimationFrame()` deaktiviert war, was am Browserdrosselungsverhalten für Hintergrundregisterkarten lag.
* Diese Version beinhaltet viele Leistungsverbesserungen, einschließlich kürzerer Callstacks, wenn ein Chrome-CPU-Profil untersucht wird.
* at.js 1.3.0 unterstützt die Bereitstellung von Inhalten in Microsoft Internet Explorer 9 nicht mehr. Eine Liste der unterstützten Browser finden Sie unter [Unterstützte Browser](https://developer.adobe.com/target/before-implement/supported-browsers/). Von jetzt an werden alle Anfragen über `XMLHttpRequest` mit CORS-Unterstützung ohne JSONP-Anfragen ausgeführt. Durch diese Änderung wird die Sicherheit erheblich verbessert.

## „at.js“-Version 1.2.3 {#section_CE4D14AF00D04F4C8A2F0513F5EA1A84}

[!DNL at.js] Version 1.2.3 ist verfügbar.

* Fügt Unterstützung für JSON-Angebote hinzu. JSON-Angebote werden nur bei Aktivitäten unterstützt, die mit dem formularbasierten Experience Composer erstellt wurden. Die einzige Möglichkeit, JSON-Angebote zu nutzen, läuft derzeit über direkte API-Aufrufe. Weitere Informationen finden Sie unter [Erstellen von JSON-Angeboten](/help/main/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D).

## „at.js“-Version 1.2.2 {#section_4E96D13F2DFE4F1F81A1089877D53649}

[!DNL at.js], Version 1.2.2 ist verfügbar.

* Dort wurde ein Problem behoben, das einen JavaScript-Fehler zurückgab, wenn die Target-Bibliothek im QUIRKS-Modus auf eine Seite geladen wurde. (TNT-28312)
* Es wurde ein Problem behoben, das dazu führte, dass die Target-Klickverfolgung die Anrufe zur Datensammlung von Analytics unterbrach. (TNT-28261)
* Es wurde ein Problem behoben, das dazu führte, dass `getOffer() params` fehlschlug, wenn `targetPageParams()` eine leere Zeichenfolge zurückgab. (TNT-28359)
* Es wurde ein Problem mit der Generierung von Sitzungs-IDs bei der Verwendung von x-only behoben. (TNT-28361)

## „at.js“-Version 1.2.1 {#section_F757C8174BBA4F68AC5524ADC3D9C5E3}

[!DNL at.js], Version 1.2.1 ist verfügbar.

* Es wurde ein Problem bei der Verfolgung per Klick auf einen Link mit target=&quot;_blank&quot; behoben, das das Öffnen des Links auf einer neuen Registerkarte in Target verhindert hat.

## „at.js“-Version 1.2.0 {#section_1C3A18C595C34B25A14A440D213F3B9C}

[!DNL at.js], Version 1.2 ist nun als Wartungsversion verfügbar, die größtenteils Fehlerkorrekturen enthält.

* Es wurde ein Problem behoben, das Standardaktionen zum Verfolgen von Sonderfällen per Klick verhindert hat. (TNT-28089)
* Es wurde ein Problem beim Klick-Tracking auf einen Link mit `target="_blank"` behoben, das das Öffnen des Links auf einer neuen Registerkarte in Target verhindert hat. (TNT-28072)
* IP-Adressen können als Cookie-Domäne verwendet werden. (TNT-28002)
* Es wurde ein Problem behoben, das in Weiterleitungsangeboten mit einer globalen Mbox oder anderen regionalen Mboxes ein Flackern verursacht hat. (TNT-27978)
* Es wurde ein Problem behoben, durch das die Einrichtung der Erlebnis-Targeting-Aktivität im VEC fehlschlägt, wenn ein Wechsel zwischen dem Durchsuchen und dem Erstellen erfolgt. (TNT-27942)
* Es wurde eine falsche Behandlung der Flackerstilklassen für klickbasierte Verfolgungselemente behoben. (TNT-27896)
* Es wurde ein Problem behoben, durch das globale Mbox-Parameter mit allen Mbox-Parametern gemischt wurden. (TNT-27846)
* Es wurden Änderungen vorgenommen, die sicherstellen, dass Handlebars, Mustache und andere clientseitige Vorlagenbibliotheken von [!DNL at.js] ordnungsgemäß verarbeitet werden. (TNT-27831)
* Es wurden Änderungen vorgenommen, die sicherstellen, dass `sdidParamExpiry` ordnungsgemäß initialisiert und an die Besucher-API übergeben wird. Dies ist eine Regression, die `at.js 1.1.0` hinzugefügt wurde. Vorherige [!DNL at.js]-Versionen sind nicht betroffen. Dies betrifft nur Clients, die Weiterleitungsangebote und A4T verwenden. (TNT-27791)
* Es wurden Änderungen vorgenommen, die sicherstellen, dass `SCRIPT` unabhängig vom verwendeten Typattribut ausgeführt wird. (TNT-27865)

## „at.js“-Version 1.1.0 {#section_8F494E1EA94E48A9B169F5CF9FE6DC56}

**Datum:** 2. August 2017

Folgende Verbesserungen und Fehlerbehebungen sind in Version 1.1 von [!DNL at.js] enthalten:

* Die Verarbeitung von Antwort-Token wurde hinzugefügt. Weitere Informationen finden Sie unter [Antwort-Token](/help/main/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4).
* Es wurde ein Problem behoben, damit `document.currentScript polyfill` nicht mit Angular 1.X in Konflikt gerät.
* Es wurden Änderungen vorgenommen, die sicherstellen, dass die Klick-Verfolgung nicht mit der Sichtbarkeitseigenschaft in Konflikt gerät. Klick-Verfolgungselemente sind mit der CSS-Klasse `at-element-click-tracking` statt mit `at-element-marker` markiert.

## „at.js“-Version 1.0.0 {#section_37A3D23FC4AD42A68AA831B89E03E725}

**Datum:** 7. Juli 2017

Folgende Verbesserungen und Fehlerbehebungen sind Version 1.0 von at.js enthalten:

* Unterstützung des asynchronen Ladens von at.js zum schnelleren Laden der Seite.
* Unterstützung zum Ausblenden von Seiteninhalten im Voraus, wenn at.js asynchron geladen wird.
* Bessere Fehlermeldungen bei deaktivierter Inhaltsbereitstellung.
* Leistungsoptimierungen beim Bereitstellen mehrerer Aktivitäten.
* Unterstützung der YUI-Komprimierung.
* Bug/Fehler-Berichterstellung für benutzerdefinierte Ereignisse während der Bereitstellung von Aktivitäten.
* Behebung von Leistungsproblemen in Microsoft Internet Explorer 11.
* Korrektur eines Fehlers der `getOffer()`-Funktion auf einigen Websites.
* Asynchrones Laden der Target-Bibliothek. Weitere Informationen finden Sie in den [häufig gestellten Fragen zu „at.js“](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-faq/target-atjs-faq/).

## „at.js“-Version 0.9.7 {#section_6C7B698BE21E40E495FD2850EFBF3E80}

**Datum:** 22. Mai 2017

Folgende Verbesserungen und Fehlerbehebungen sind in Version 0.9.7 von [!DNL at.js] enthalten:

* Es wurde ein Problem bezüglich eines Asset-Schlüssels behoben, der in den Aktionen `insertAfter` und `insertBefore` im Visual Experience Composer (VEC) gefehlt hat. Diese Probleme bezogen sich auf die Migration von visuellen Angeboten zu Angebotsvorlagen.

## „at.js“-Version 0.9.6 {#section_EEFA6413F2F947AD8C4A88128B90245D}

**Datum:** 13. April 2017

Folgende Verbesserungen und Fehlerbehebungen sind in Version 0.9.6 von [!DNL at.js] enthalten:

* Unterstützung für Umleitungsangebote für A4T. Nachdem Sie Version 0.9.6 von [!DNL at.js] heruntergeladen haben, können Sie Umleitungsangebote in Aktivitäten verwenden, die [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Target] (A4T) nutzen. Neben Version 0.9.6 von [!DNL at.js] bestehen weitere Mindestanforderungen für Ihre Implementierung, um Umleitungsangebote und A4T nutzen zu können. Weitere wichtige Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
* Vor [!DNL at.js] 0.9.6 galt: Wenn eine Besucher-API auf der Seite vorhanden und die Einstellung `visitorApiTimeout` zu aggressiv war, konnte dies dazu führen, dass in der [!DNL Target]-Anfrage keine MCID-Daten gesendet wurden. So konnte es bei der Verwendung von A4T zu Problemen wie z. B. aufgetrennten Treffern in [!DNL Analytics] kommen.

   Dieses Verhalten wurde in Version 0.9.6 von [!DNL at.js] geändert: Auch wenn `visitorApiTimeout` auf „1 ms“ festgelegt ist, versucht Target, Daten zu SDID, Tracking-Servern und Kunden-IDs zu erfassen und sie in der Target-Anfrage zu senden.

* Die Einstellung `selectorsPollingTimeout` wurde hinzugefügt. Weitere Informationen finden Sie unter [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).
* Das Antwortformat von `getOffer()` wurde geändert. Weitere Informationen finden Sie unter [adobe.target.getOffer(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/).
* Die Konsolenprotokollierung für nicht unterstützte `<!DOCTYPE>`-Deklarationen wurde hinzugefügt.
* Es wurde ein Problem behoben, bei dem [!DNL Target Classic]-Plug-ins nicht ordnungsgemäß angewendet wurden, wenn mehrere Standardangebote an eine Mbox gesendet wurden. (TGT-22664)
* Die Cookie-Einstellung für Domänen auf oberster Ebene mit zwei Buchstaben wurde verbessert, um zu gewährleisten, dass das Mbox-Cookie für entsprechende Domänen korrekt festgelegt wird (z. B. [!DNL test.no], [!DNL autodrives.ca] usw.).
* Der Algorithmus zum Extrahieren der Domain der obersten Ebene, die beim Speichern von Cookies verwendet werden sollte, hat sich in at.js-Version 0.9.6 geändert. Aufgrund dieser Änderung können keine Cookies für Adressen gespeichert werden, die IP verwenden. IP-Adressen werden größtenteils zu Testzwecken verwendet. Als Problemumgehung können Sie jedoch DNS-Einträge verwenden oder die Hosts-Datei auf einer lokalen Box anpassen.
* Die Verarbeitung von Aktionen zum Verschieben und Neuanordnen bei Zeichenfolgenwerten anstelle von Ganzzahlen als Eigenschaften wurde korrigiert.

## „at.js“-Version 0.9.4 {#section_A15B12F12CD94F07B3F56613A79A815F}

**Datum:** 19. Januar 2017

* Mbox-Namen können jetzt Sonderzeichen wie das kaufmännische Und (&amp;) enthalten. 

   Eine Liste der zulässigen Sonderzeichen finden Sie unter [„at.js“-Konfigurationen](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/).

* Die Funktion `secureOnly` wurde hinzugefügt, die anzeigt, ob at.js nur HTTPS verwenden soll oder ob es möglich ist, dass basierend auf dem Seitenprotokoll zwischen HTTP und HTTPS umgeschaltet wird. Es handelt sich hierbei um eine erweiterte Einstellung, deren Standardwert „false“ (falsch) lautet und die von `targetGlobalSettings` überschrieben werden kann.
* Die Option [!UICONTROL Unterstützung älterer Browser] ist in at.js, Version 0.9.3 und älter verfügbar. Diese Option wurde in at.js, Version 0.9.4 entfernt.

## „at.js“-Version 0.9.3 {#section_DF13BC1D7C994AE7A36B81937A699DF4}

**Datum:** 10. Oktober 2016

* Stellt sicher, dass Mbox-Aufrufe in Microsoft Internet Explorer 11 ausgelöst werden, wenn veraltete Browser in den at.js-Einstellungen deaktiviert sind.
* Stellt sicher, dass Standardinhalte wiedergegeben werden, wenn ein dynamisches Remote-Angebot fehlschlägt (wenn beispielsweise die URL nicht korrekt ist und eine 404-Fehlermeldung angezeigt wird).
* Stellt sicher, dass Elemente schnell angezeigt werden, wenn im DOM keine Selektoren für VEC-Clicktracking gefunden werden.

## „at.js“-Version 0.9.2 {#section_148549CBB4F046BAA8F79C79B64EC889}

**Datum:** 21. September 2016

* Es wurde die Einstellung `optoutEnabled` hinzugefügt, um die Abmeldung für Gerätediagramme zu ermöglichen. Ist diese Option als `true` eingestellt und hat sich der Besucher gegen eine Verfolgung entschieden, ruft der Browser des Benutzers die Mbox nicht auf. Gerätediagramme sind derzeit als Betaversion verfügbar. Diese Einstellung ist standardmäßig als `false` festgelegt, muss allerdings in `true` geändert werden, wenn Sie Gerätediagramme nutzen.
* Erweiterte Unterstützung für `CustomEvent` im Benachrichtigungsmechanismus. In der Vergangenheit konnte der Ereignis-Benachrichtigungsmechanismus von at.js nicht mit Standard-DOM-APIs wie `document.addEventListener()` () verwendet werden. Jetzt können Sie `document.addEventListener()` verwenden, um at.js-Ereignisse, z. B. Abfrage- und Inhaltswiedergabe-Ereignisse, zu abonnieren.
* Es wurde ein Problem im Zusammenhang mit Angeboten behoben, die im Visual Experience Composer (VEC) erstellt wurden. In älteren Versionen wurden Auswahlwerkzeuge von Target ausgeblendet und nur eingeblendet, wenn alle Auswahlen übereinstimmten. In at.js 0.9.2 werden einzelne Auswahlen von Target eingeblendet, sobald sie übereinstimmen.

## „at.js“-Version 0.9.1 {#section_DAFB99114D604CFB8416C1BC7DEEAEEE}

**Datum:** 14. Juli 2016

* Stellt für at.js eine Zeitüberschreitung des Besucher-ID-Diensts bereit, die von der Zeitüberschreitung des Diensts selbst unabhängig ist.
* Behebung eines Problems in Version 0.9.0, das sich auf Implementierungen mit at.js auf einigen Seiten und mbox.js (jetzt nicht mehr unterstützt) auf anderen Seiten auswirkte.
* Sollten Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität und bei der Verwendung von mbox.js Version 61 (oder neuer) oder at.js Version 0.9.1 (oder neuer) keinen Trackingserver angeben. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Ziele und Einstellungen] leer lassen.

## „at.js“-Version 0.9.0 {#section_2981CC9792F245389B39BB5B69F84C4E}

**Target-Version:** 16.6.1

**Datum:** 23. Juni 2016

* Behebung eines Whitescreen-Problems bei der Verwendung von VEC-Angeboten. Jeder, der [!DNL at.js] verwendet, sollte auf diese neue Version aktualisieren.
* Neue `registerExtension`-API.

   Mit dieser neuen API erhalten Entwickler Zugriff auf bestimmte jQuery-Module, die in [!DNL at.js] zur Entwicklung von Erweiterungen (Plug-ins) für die Bibliothek verwendet werden. Für diese Änderung gibt es verschiedene Gründe. Die Änderung wirkt sich nur auf Benutzer aus, die mit folgenden Funktionen arbeiten:

   * Die `getSettings()`-API wurde entfernt, die gleichen Funktionen sind aber über `registerExtension()` verfügbar.
   * Die `getTracking()`-API wurde entfernt, die gleichen Funktionen sind aber über `registerExtension()` verfügbar.

   * Bestehende Erweiterungen (z. B. Erweiterungen für AngularJS) müssen aktualisiert werden, damit `registerExtension()` verwendet werden kann.

* Neue at.js-Benachrichtigungs-API.

   Ziel dieses Benachrichtigungssystems ist es, bessere Einsichten in [!DNL at.js] und die zugehörigen Aktivitäten auf der Seite zu ermöglichen sowie aufzuzeigen, wenn Fehler auftreten. Ein häufig im VEC auftretendes Problem ist, dass sich bei einem IT-Release die Seite ändert. Somit wird ein VEC-Selektor beschädigt und der Test kann Inhalte nicht mehr ordnungsgemäß bereitstellen. Ziel dieses Benachrichtigungssystems ist es, die Seite auf dieses Bereitstellungsproblem aufmerksam zu machen, sodass Entwickler auf die Informationen zugreifen, sie an ein System wie [!DNL Adobe Analytics] weiterleiten und Nachrichten an den Geschäftsinhaber übermitteln können, um darüber zu informieren, dass der Test nicht mehr funktioniert.

* Neue `targetGlobalSettings()`-API-Methode.

   Sie können Einstellungen in der at.js-Bibliothek überschreiben, anstatt die Einstellungen in der [!DNL Target Standard/Premium UI] oder durch Verwendung von REST-APIs zu bearbeiten.

## „at.js“-Version 0.8.0 {#section_E1C7B08EC0494388A022C28A8B8FE807}

**Datum:** 5. Mai 2016.

Dies ist die erste offizielle Version der [!DNL at.js]-Bibliothek.

[!DNL at.js] ist eine neue Implementierungsbibliothek für [!DNL Target] und sowohl auf typische Webimplementierungen als auch auf Einzelseiten-Apps ausgelegt.

[!DNL at.js] ersetzt [!DNL mbox.js] bei [!DNL Adobe Target]-Implementierungen.

Neben anderen Vorteilen sorgt [!DNL at.js] für kürzere Ladezeiten von Seiten bei Webimplementierungen, erhöhte Sicherheit und bessere Implementierungsoptionen für Einzelseitenanwendungen.

[!DNL at.js] enthält die Komponenten, die sich in [!DNL target.js] befanden, weshalb kein Aufruf mehr an [!DNL target.js] erfolgt.

Achten Sie bei der Implementierung von [!DNL at.js] auf Folgendes:

* Versionen von Internet Explorer, die älter als Version 8 sind, werden nicht unterstützt.
* Aufgrund der asynchronen Implementierung funktionieren ältere Integrationen, wie das Plug-in von [!DNL Test&Target] zu [!DNL SiteCatalyst], möglicherweise nicht mehr.
* [!DNL Target]-Plug-ins, die [!DNL mbox.js]-Objekte und -Methoden referenzieren, werden nicht unterstützt.
* Alle [!DNL Target]-Aufrufe werden über XMLHTTPRequest getätigt und Inhalt wird über JSON zurückgegeben.
