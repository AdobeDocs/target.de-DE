---
keywords: at.js-FAQ;häufig gestellte Fragen zu at.js;FAQ;flackern;Loader;Seiten-Loader;Cross Domain;Dateigröße;Datei-Größe;X-Domain;at.js und mbox.js;nur x;cross domain;Safari;Einzelseiten-App;fehlende Selektoren;Selektoren;Einzelseitenanwendung;tt.omtrdc.net;SPA;Adobe Experience Manager;AEM;IP-Adresse;httponly;HTTPonly;sicher;IP;Cookie-Domäne
description: Antworten auf häufig gestellte Fragen zur Adobe  [!DNL Target]  at.js-JavaScript-Bibliothek.
title: Was sind häufige Fragen und Antworten zu at.js?
feature: at.js
role: Developer
exl-id: 937f880a-1842-4655-be44-0a5614c2dbcc
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '2586'
ht-degree: 96%

---

# Häufig gestellte Fragen zu „at.js“

Antworten auf häufig gestellte Fragen über die [!DNL Adobe Target] zur at.js-JavaScript-Bibliothek.

## Welche Vorteile hat die Verwendung von at.js gegenüber mbox.js? {#section_FE30D01A577C46ACB0F787B85F5E0F6B}

Die Bibliothek [!DNL at.js] ersetzt [!DNL mbox.js]. Die Bibliothek [!DNL mbox.js] wird nicht mehr unterstützt. Für die meisten Benutzer birgt [!DNL at.js] allerdings mehr Vorteile als [!DNL mbox.js].

Neben anderen Vorteilen sorgt [!DNL at.js] für kürzere Ladezeiten von Seiten bei Webimplementierungen, bessere Sicherheit und bessere Implementierungsoptionen für Einzelseiten-Apps.

Im folgenden Diagramm wird die Seitenladeleistung von mbox.js und at.js verglichen.

![](assets/atjs_vesus_mboxjs.png)

Wie oben gezeigt, werden Seiteninhalte bei der Verwendung von mbox.js erst geladen, wenn der Aufruf von [!DNL Target] abgeschlossen wurde. Bei der Verwendung von at.js werden Seiteninhalte schon geladen, wenn der Aufruf von [!DNL Target] eingeleitet wird, nicht erst nach Abschluss des Vorgangs.

## Wie wirkt sich at.js und mbox.js auf Seitenladezeiten aus? {#page-load}

Viele Kunden und Berater möchten wissen, wie sich [!DNL at.js] und [!DNL mbox.js] auf die Seitenladezeit auswirken, insbesondere beim Vergleich neuer Besucher mit zurückkehrenden Besuchern. Leider ist es schwierig, zu messen, wie sich [!DNL at.js] oder [!DNL mbox.js] auf die Seitenladezeit auswirken und genaue Zahlen dazu zu nennen. Das liegt an den Implementationen der einzelnen Kunden.

Wenn die Besucher-API jedoch auf der Seite vorhanden ist, ermöglicht das [!DNL Target] ein besseres Verständnis davon, wie sich [!DNL at.js] und [!DNL mbox.js] auf die Ladezeit der Seite auswirken.

>[!NOTE]
>
>Die Besucher-API und [!DNL at.js] oder [!DNL mbox.js] wirken sich nur dann auf die Seitenladezeit aus, wenn Sie die globale Mbox verwenden (das liegt an der Technik, mit der der Haupttext ausgeblendet wird). Regionale Mboxes sind von der Besucher-API-Integration nicht betroffen.

In den folgenden Abschnitten wird die Aktionssequenz für neue und zurückkehrende Besucher beschrieben:

### Neue Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. at.js/mbox.js ist geladen und analysiert und wird ausgeführt.
1. Wenn die automatische Erstellung der globalen Mbox aktiviert ist, wird die Target JavaScript-Bibliothek Folgendes tun:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die [!DNL Target]-Bibliothek versucht, [!DNL Experience Cloud Visitor ID]-Daten abzurufen.
   * Weil es sich um einen neuen Besucher handelt, versendet die Besucher-API eine domänenübergreifende Anfrage an demdex.net.
   * Nachdem [!DNL Experience Cloud Visitor ID]-Daten abgerufen wurden, wird eine Anfrage an [!DNL Target] ausgelöst.

### Zurückkehrende Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. at.js/mbox.js ist geladen und analysiert und wird ausgeführt.
1. Wenn die automatische Erstellung der globalen Mbox aktiviert ist, gilt für die [!DNL Target] JavaScript-Bibliothek:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die [!DNL Target]-Bibliothek versucht, [!DNL Experience Cloud Visitor ID]-Daten abzurufen.
   * Die Besucher-API ruft Cookie-Daten ab.
   * Nachdem [!DNL Experience Cloud Visitor ID]-Daten abgerufen wurden, wird eine Anfrage an [!DNL Target] ausgelöst.

>[!NOTE]
>
>Wenn die Besucher-API vorhanden ist, muss bei neuen Besuchern [!DNL Target] mehrfach über die Verbindung gehen, um sicherzustellen, dass [!DNL Target]-Anfragen die [!DNL Experience Cloud Visitor ID]-Daten enthalten. Bei zurückkehrenden Besuchern geht [!DNL Target] nur über die Verbindung zu [!DNL Target], um den personalisierten Inhalt abzurufen.

## Warum sind die Antwortzeiten nach einem Upgrade von einer vorherigen Version von at.js auf Version 1.0.0 scheinbar langsamer? {#section_DFBA5854FFD142B49AD87BFAA09896B0}

Bei [!DNL at.js] der Version 1.0.0 und höher werden alle Anforderungen parallel ausgelöst. In den vorherigen Versionen werden die Anforderungen sequenziell ausgeführt, d. h. die Anforderungen werden in eine Warteschlange verschoben, und [!DNL Target] wartet auf den Abschluss der ersten Anforderung, bevor der Vorgang mit der nächsten Anforderung fortgesetzt wird.

Die Art der Ausführung von Anforderungen in früheren Versionen von [!DNL at.js] unterliegt dem sogenannten „Head of Line Blocking“. In [!DNL at.js] 1.0.0 und höher ist zu der parallelen Anforderungsausführung gewechselt.[!DNL Target]

Wenn Sie sich beispielsweise das Wasserfallmodell der Netzwerkregisterkarte für [!DNL at.js] 0.9.1 ansehen, werden Sie feststellen, dass die nächste [!DNL Target]-Anforderung erst gestartet wird, nachdem die vorherige fertiggestellt wurde. Bei [!DNL at.js] 1.0.0 und höher ist dies nicht der Fall. Dort beginnen alle Anforderungen grundsätzlich zu derselben Zeit.

Auf die Antwortzeit bezogen kann dies mathematisch wie folgt betrachtet werden:

<ul class="simplelist"> 
 <li> at.js 0.9.1: Reaktionszeit aller [!DNL Target] requests = Summe der Antwortzeiten von Anforderungen </li> 
 <li> at.js 1.0.0 und höher: Reaktionszeit aller [!DNL Target] requests = maximum of requests response time </li> 
</ul>

Die [!DNL at.js]-Bibliothek Version 1.0.0 führt die Anforderungen schneller aus. Zudem laufen [!DNL at.js]-Anforderungen asynchron, sodass das Rendern der Seiten nicht blockiert. [!DNL Target] Selbst wenn der Abschluss von Anforderungen mehrere Sekunden dauert, wird die gerenderte Seite angezeigt. Lediglich einige Teile der Seite bleiben leer, bis [!DNL Target] eine Antwort vom [!DNL Target]-Edge erhält.

## Kann ich die [!DNL Target]-Bibliothek asynchron laden? {#section_AB9A0CA30C5440C693413F1455841470}

In at.js 1.0.0 kann die [!DNL Target]-Bibliothek asynchron geladen werden.

So laden Sie at.js asynchron:

* Der empfohlene Ansatz erfolgt über Tags in [!DNL Adobe Experience Platform].
* Sie können at.js auch asynchron laden, indem Sie dem Skript-Tag zum Laden von at.js das asynchrone Attribut hinzufügen. Verwenden Sie etwas wie:

   ```
   <script src="<URL to at.js>" async></script>
   ```

* Sie können at.js auch mithilfe dieses Codes asynchron laden:

   ```
   var script = document.createElement('script'); 
   script.async = true; 
   script.src = "<URL to at.js>"; 
   document.head.appendChild(script);
   ```

Das asynchrone Laden von at.js eignet sich hervorragend, um zu verhindern, dass das Rendern des Browsers blockiert wird. Bei dieser Technik kann es jedoch zu Flackereffekten auf der Webseite kommen.

Sie können ein Flackern vermeiden, indem Sie ein pre-hiding-Snippet verwenden, das die Seite (oder bestimmte Teile) ausblendet und diese dann nach at.js einblendet und die globale Anfrage geladen hat. Der Ausschnitt muss vor dem Laden von at.js hinzugefügt werden.

Wenn Sie at.js über eine asynchrone [!DNL Adobe Experience Platform]-Implementierung bereitstellen, stellen Sie sicher, dass Sie das pre-hiding-Snippet direkt auf Ihren Seiten einfügen, bevor Sie [!DNL Target] mit [!DNL Adobe Experience Platform]-Einbettungs-Code implementieren.

Wenn Sie at.js über eine synchrone DTM-Implementierung bereitstellen, kann das vor-ausgeblendete Snippet über eine Seitenladeregel hinzugefügt werden, die oben auf der Seite ausgelöst wird.

Weitere Informationen finden Sie unter [Verwaltung von Flackern mit „at.js“](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

## Ist at.js mit der [!DNL Adobe Experience Manager]-Integration (Experience Manager) kompatibel? {#section_6177AE10542344239753764C6165FDDC}

[!DNL Adobe Experience Manager] 6.2 mit FP-11577 (oder neuer) unterstützt jetzt [!DNL at.js]-Implementierungen mit der [!UICONTROL Adobe Target Cloud Services]-Integration.

## Wie kann ich mit at.js ein Flackern beim Laden von Seiten verhindern ? {#section_4D78AAAE73C24E578C974743A3C65919}

Mit Target wird das Flackern beim Laden von Seiten auf verschiedenen Wegen vermieden: Weitere Informationen finden Sie unter  [Verwaltung von Flackern mit „at.js“](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

## Wie groß ist at.js? {#section_6A25C9A14C66441785A7635FEF5C4475}

Die at.js-Datei hat beim Download eine Größe von etwa 109 KB. Da die meisten Server Dateien jedoch automatisch komprimieren, um die Dateigröße zu verringern, ist at.js bei Komprimierung (mit GZIP oder einer ähnlichen Anwendung) auf dem Server etwa 34 KB groß und wird in dieser Größe auch geladen, wenn Benutzer Ihre Webseite besuchen. Die Komprimierungseinstellungen des Servers, auf dem at.js installiert ist, bestimmen die tatsächliche Größe der Datei.

## Warum ist at.js größer als mbox.js? {#section_AA1C43897E46448FA3E26EEC10ED7E51}

at.js-Implementierungen verwenden nur eine Bibliothek ([!DNL at.js]), während bei mbox.js-Implementierungen zwei Bibliotheken ([!DNL mbox.js] und [!DNL target.js]) zum Einsatz kommen. Es wäre also gerechter, at.js mit mbox.js *und* `target.js` zu vergleichen. Beim Vergleich der komprimierten Größen der beiden Versionen ist ersichtlich, dass die at.js-Version 1.2 34 KB groß ist und die mbox.js-Version 63 eine Größe von 26,2 KB hat. ``

at.js ist deshalb größer, weil im Vergleich zu mbox.js deutlich mehr DOM-Parsing durchgeführt wird. Dies ist erforderlich, da at.js „Rohdaten“ in der JSON-Antwort erhält und diese zunächst verarbeiten muss. mbox.js verwendet `document.write()`, das Parsing wird vom Browser übernommen.

Trotz der größeren Datei zeigen unsere Tests, dass Seiten mit at.js schneller geladen werden als Seiten mit mbox.js. Zudem bietet at.js eine höhere Sicherheit, da keine zusätzlichen dynamischen Dateien geladen werden und `document.write` nicht benötigt wird.

## Enthält at.js jQuery? Kann ich diese Komponente von „at.js“ löschen, wenn ich jQuery bereits auf meiner Website verwende? {#section_E4604E46E7B34460B8DD6A78D9B476F9}

at.js nutzt derzeit Teile von jQuery, deshalb wird Ihnen oben in at.js der MIT-Lizenzhinweis angezeigt. jQuery wird nicht ausgelöst und die Bibliothek übt keinen Einfluss auf die bereits auf Ihrer Seite eingebettete jQuery-Bibliothek aus, bei der es sich möglicherweise um eine andere Version handelt. Der jQuery-Code in at.js lässt sich nicht löschen.

## Unterstützt „at.js“ Safari und domänenübergreifende Einstellungen, die als „nur x“ eingestellt sind? {#section_114EC271A6E045E1B2183B66F1B71285}

Nein, ist die domänenübergreifende Einstellung auf „nur x“ festgelegt und sind Drittanbieter-Cookies in Safari deaktiviert, setzen sowohl [!DNL mbox.js] als auch at.js ein deaktiviertes Cookie und es werden für diese Kundendomäne keine mbox-Abfragen ausgeführt.

Sollen Safari-Besucher unterstützt werden, wäre eine bessere X-Domäne „deaktiviert“ (setzt nur ein Erstanbieter-Cookie) oder „aktiviert“ (setzt in Safari nur ein Erstanbieter-Cookie, während in anderen Browsern Erst- und Drittanbieter-Cookies gesetzt werden).

## Kann ich [!DNL Target] Visual Experience Composer in meinen Einzelseiten-Programmen verwenden? {#section_459C1BEABD4B4A1AADA6CF4EC7A70DFB}

Ja. Sie können VEC für Ihre SPA benutzen, wenn Sie at.js 2.x verwenden. Weitere Informationen finden Sie unter [Visual Experience Composer (VEC) für Einzelseiten-Programme](/help/main/c-experiences/spa-visual-experience-composer.md).

## Kann ich den [!DNL Adobe Experience Cloud]-Debugger für at.js-Implementierungen verwenden? {#section_FF3CF4C5FD2F4DB1BF1A6B39DA161637}

Ja. Sie können außerdem mboxTrace für das Debugging oder die Entwicklerwerkzeuge Ihres Browsers verwenden und zum Isolieren von Mbox-Aufrufen nach „mbox“ filtern, um die Netzwerkanforderungen zu analysieren.

## Kann ich mit at.js Sonderzeichen in meinen Mbox-Namen verwenden ? {#section_8E31D2E8A27642098934D7DACFB2A600}

Ja, genau wie bei mbox.js.

## Warum werden meine Mboxes nicht auf meinen Webseiten ausgelöst? {#section_4BA5DA424B734324AAB51E4588FA50F5}

[!DNL Target]-Kunden verwenden mitunter Cloud-basierte Instanzen mit [!DNL Target] zum Testen oder für einfache Machbarkeitsprüfungen. Diese Domänen sind neben vielen anderen Teil der [öffentlichen Suffix-Liste](https://publicsuffix.org/list/public_suffix_list.dat).

Moderne Browser speichern keine Cookies, wenn Sie diese Domänen verwenden - es sei denn, Sie passen die Einstellung `cookieDomain` mit targetGlobalSettings() an. Weitere Informationen finden Sie unter [Verwenden Cloud-basierter Instanzen mit Target](https://developer.adobe.com/target/implement/client-side/target-debugging-atjs/targeting-using-cloud-based-instances/).

## Können IP-Adressen bei der Verwendung von at.js als Cookie-Domäne dienen? {#section_8BEEC91A3410459D9E442840A3C88AF7}

Ja, wenn Sie [at.js, Version 1.2 oder neuer](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) verwenden. [!DNL Adobe] empfiehlt jedoch dringend, immer die neueste Version zu verwenden.

>[!NOTE]
>
>Die folgenden Beispiele sind nicht notwendig, wenn Sie at.js der Version 1.2 oder neuer verwenden.

Abhängig davon, wie Sie [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) verwenden, müssen Sie möglicherweise weitere Änderungen am Code vornehmen, nachdem Sie at.js heruntergeladen haben. Benötigen Sie beispielsweise etwas voneinander abweichende Einstellungen für Ihre Implementierungen von [!DNL Target] auf verschiedenen Websites und konnten Sie diese Einstellungen nicht dynamisch mit JavaScript festlegen, nehmen Sie diese Anpassungen manuell vor, nachdem Sie die Datei heruntergeladen haben und bevor Sie sie auf der entsprechenden Website hochladen.

In den folgenden Beispielen können Sie die at.js-Funktion `targetGlobalSettings()` zum Einfügen eines Code-Ausschnitts verwenden, um IP-Adressen zu unterstützen:

Dieses Beispiel betrifft eine einzelne IP-Adresse:

```
if (window.location.hostname === '123.456.78.9') { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

Dieses Beispiel betrifft einen IP-Adressbereich:

```
if (/^123\.456\.78\..*/g.test(window.location.hostname)) { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

## Warum werden mir Warnhinweise wie zum Beispiel „Aktionen mit fehlenden Selektoren“ angezeigt?  {#section_C36BED5B16634361A1BA46FCB731489D}

Diese Nachrichten stehen in keiner Verbindung zur [!DNL at.js]-Funktionalität. Die [!DNL at.js]-Bibliothek versucht, alles zu melden, das nicht im DOM zu finden ist.

Nachfolgend finden Sie mögliche Grundursachen für diesen Warnhinweis:

* Die Seite wird dynamisch erstellt und at.js kann das Element nicht finden.
* Die Seite wird langsam erstellt (aufgrund eines langsamen Netzwerks) und at.js kann den Selektor im DOM nicht finden.
* Die Seitenstruktur, auf der Aktivität ausgeführt wird, wurde geändert. [!UICONTROL  Wenn Sie die Aktivität erneut im ]Visual Experience Composer (VEC) öffnen, sollte Ihnen ein Warnhinweis angezeigt werden. Sie sollten die Aktivität aktualisieren, damit alle erforderlichen Elemente gefunden werden können.
* Die zugrundeliegende Seite ist Teil eines [!UICONTROL Einzelseiten-Programms] oder die Seite enthält Elemente, die weiter unten auf der Seite auftauchen und der [!DNL at.js] „Selektor-Polling-Mechanismus“ kann diese Elemente nicht finden. Es ist unter Umständen hilfreich, den `selectorsPollingTimeout` zu erhöhen. Weitere Informationen finden Sie unter [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).
* Eine beliebige Klick-Tracking-Metrik versucht, sich zu jeder Seite hinzuzufügen, unabhängig von der URL, in der die Metrik eingerichtet wurde. Diese Situation ist zwar harmlos, hat aber viele dieser Warnhinweise zur Folge.

   Um die bestmöglichen Ergebnisse zu erzielen, sollten Sie die aktuellste Version von [!DNL at.js] herunterladen und verwenden. Weitere Informationen finden Sie unter [„at.js“-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) und [Herunterladen von „at.js“](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/).

## Was ist die Domain tt.omtrdc.net, zu der die Aufrufe des [!DNL Target]-Servers gehen? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] ist der Domainname für das EDGE-Netzwerk von Adobe, mit dem alle Server-Aufrufe für Target empfangen werden.

## Warum verwendet at.js nicht immer die Cookie-Flags „HttpOnly“und „Secure“? {#section_74527E3B41B54B0A83F217C3E664ED1F}

„HttpOnly“ kann nur über Server-seitigen Code festgelegt werden. [!DNL Target]-Cookies, wie z. B. Mbox, werden über JavaScript-Code erstellt und gespeichert, also kann [!DNL Target] Cookieflag „HttpOnly“ nicht verwenden. [!DNL Target] verwendet set HttpOnly für Drittanbieter-Cookies, die Server-seitig gesetzt werden, wenn domänenübergreifend aktiviert.

„Secure“ kann nur über JavaScript festgelegt werden, wenn die Seite mit HTTPS geladen wurde. Wenn die Seite nur mit HTTP geladen wird, kann JavaScript dieses Flag nicht festlegen. Darüber hinaus ist das Cookie bei der Verwendung des Flags „Secure“ nur auf HTTPS-Seiten verfügbar. Für Seiten, die über HTTPS geladen werden, legt [!DNL Target] die Attribute Secure und SameSite=None fest.

Um sicherzustellen, dass [!DNL Target] Benutzer ordnungsgemäß verfolgen kann und die Cookies Client-seitig generiert werden, verwendet [!DNL Target] keine dieser Flags außer in den oben genannten Situationen.

## Wie oft sendet at.js Netzwerkanfragen?  {#section_57C5235DF7694AF093A845D73EABADFD}

Die [!DNL Target] gesamte Entscheidungsfindung von findet Server-seitig statt. Das bedeutet, dass at.js jedes Mal, wenn die Seite neu geladen oder eine öffentliche at.js-API aufgerufen wird, eine Netzwerkanfrage gesendet wird.

## Können wir im besten Fall davon ausgehen, dass Benutzer durch das Ausblenden, Ersetzen und Wiedereinblenden von Inhalten keine Beeinträchtigung der Seitenladezeit bemerken werden? {#section_CB3C566AD61F417FAC0EC5AC706723EB}

at.js vermeidet das Vorab-Ausblenden des HTML-Bodys oder anderer DOM-Elemente über einen längeren Zeitraum, dies ist jedoch von den Netzwerkbedingungen und der Aktivitätseinrichtung abhängig. at.js bietet [Einstellungen](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/), mit denen Sie den CSS-Style zum Ausblenden des Bodys anpassen können, um nicht den gesamten HTML-Body, sondern nur bestimmte Teile der Seite auszublenden. Hierbei wird erwartet, dass diese Teile DOM-Elemente enthalten, die „personalisiert“ werden müssen.

## Wie lautet die Reihenfolge der Ereignisse in einem durchschnittlichen Szenario, in dem sich ein Benutzer für eine Aktivität qualifiziert?  {#section_56E6F448E901403FB77DF02F44C44452}

Bei der at.js-Anfrage handelt es sich um eine asynchrone `XMLHttpRequest`, weshalb wir folgende Schritte ausführen:

1. Die Seite wird geladen.
1. at.js blendet den HTML-Body vorab aus. Es gibt eine Einstellung, mit der sich anstelle des gesamten HTML-Bodys nur ein bestimmter Container ausblenden lässt.
1. Die at.js-Anfrage wird gesendet.
1. Nachdem die [!DNL Target]-Antwort eingegangen ist, extrahiert [!DNL Target] die CSS-Selektoren.
1. Mit den CSS-Selektoren erstellt [!DNL Target] STYLE-Tags, um die anzupassenden DOM-Elemente vorab auszublenden.
1. Der STYLE zum Vorab-Ausblenden des HTML-Bodys wird entfernt.
1. [!DNL Target] beginnt mit dem Abrufen der DOM-Elemente.
1. Wenn ein DOM-Element gefunden wird, wendet [!DNL Target] DOM-Änderungen an und der STYLE zum Vorab-Ausblenden des Elements wird entfernt.
1. Wenn keine DOM-Elemente gefunden werden, werden durch ein globales Timeout alle Elemente eingeblendet, um Seitenfehler zu verhindern.

## Wie oft war der Seiteninhalt vollständig geladen und sichtbar, wenn at.js das Element, das durch die Aktivität geändert wird, zum letzten Mal einblendet? {#section_01AFF476EFD046298A2E17FE3ED85075}

Wie oft war der Seiteninhalt im oben aufgeführten Szenario vollständig geladen und sichtbar, wenn at.js das Element, das durch die Aktivität geändert wird, zum letzten Mal einblendet? Anders ausgedrückt: Die Seite ist vollständig sichtbar, ausgenommen der Aktivitätsinhalt, der kurz nach dem anderen Inhalt eingeblendet wird.

at.js blockiert nicht das Seiten-Rendering. Benutzer bemerken möglicherweise leere Bereiche auf der Seite, in denen sich die von [!DNL Target] angepassten Elemente befinden. Wenn der anzuwendende Inhalt nicht viele Remote-Assets, wie z. B. Skripte oder Bilder, enthält, wird alles schnell dargestellt.

## Wie wirkt sich eine vollständig zwischengespeicherte Seite auf das oben aufgeführte Szenario aus? Ist es in diesem Fall wahrscheinlicher, dass der Aktivitätsinhalt merklich nach dem Rest des Seiteninhalts geladen wird?  {#section_CE76335A3E0B41CB8253DEE5E060FCDA}

Wenn eine Seite in einem CDN gespeichert ist, das sich nahe am Standort des Benutzers, aber nicht in der Nähe des [!DNL Target]-Edge befindet, erlebt dieser Benutzer möglicherweise Verzögerungen. [!DNL Target]-Edges sind jedoch über die ganze Welt verteilt, sodass dies in der Regel kein Problem darstellt.

## Ist es möglich, ein Hero-Bild anzuzeigen, das nach kurzer Verzögerung ersetzt wird?  {#section_C25B07B25B854AAE8DEE1623D0FA62A3}

Stellen Sie sich folgendes Szenario vor:

Das [!DNL Target]-Timeout beträgt fünf Sekunden. Ein Benutzer lädt eine Seite, die eine Aktivität zum Anpassen des Hero-Bilds aufweist. at.js sendet die Anfrage, um zu bestimmen, ob eine Aktivität angewendet werden muss, die erste Antwort bleibt jedoch aus. Wir können also davon ausgehen, dass der Benutzer den regulären Inhalt des Hero-Bilds sieht, da keine Antwort von [!DNL Target] zu etwaigen anzuwendenden Aktivitäten eingegangen ist. Nach vier Sekunden gibt [!DNL Target] eine Antwort mit den Aktivitätsinhalten zurück.

Ist es zu diesem Zeitpunkt möglich, dass die alternative Version angezeigt wird? Nach vier Sekunden könnte das Hero-Bild also ausgetauscht werden. Würde der Benutzer diesen Austausch bemerken?

Das Hero-DOM-Element ist zu Beginn ausgeblendet. Nachdem eine Antwort von [!DNL Target] eingeht, wendet at.js die DOM-Änderungen an, wie z. B. die IMG-Änderung und die Anzeige des angepassten Hero-Bilds.

## Welcher HTML-Doctype ist für at.js erforderlich?

at.js erfordert den Doctype HTML 5.

Diese Syntax lautet:

`<!DOCTYPE html>`

Der Doctype HTML 5 stellt sicher, dass die Seite im Standardmodus geladen wird. Beim Laden im Quirks-Modus sind einige JS-APIs, von denen at.js abhängig ist, deaktiviert. [!DNL Target] deaktiviert at.js im Quirks-Modus.
