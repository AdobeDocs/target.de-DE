---
keywords: mbox.js-Änderungen;mbox.js-Versionen
description: Erfahren Sie mehr über die ältere Implementierung von "mbox.js"in Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Was ist in jeder Version von mbox.js enthalten?
feature: 'at.js '
role: Entwickler
exl-id: 4e95de13-2848-497a-9d06-41e9cbd98b42
translation-type: tm+mt
source-git-commit: 0a685427a047bfc0a2f5e81525b32df70af6d69f
workflow-type: tm+mt
source-wordcount: '2422'
ht-degree: 94%

---

# „mbox.js“-Versionsdetails{#mbox-js-version-details}

Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Ab dem 31. März 2021 wird die Bibliothek &quot;mbox.js&quot; [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

>[!NOTE]
>
>Wir empfehlen allen Benutzern von mbox.js die Aktualisierung auf Version 57 oder neuer. Einige Benutzer berichteten von Zeitüberschreitungen, wenn `target.js` nicht geladen werden konnte. In Version 57 wurde dieses Problem behoben. Verwenden Sie jedoch den [!DNL Experience Cloud Visitor ID]-Dienst, benötigen Sie mindestens Version 58.

Die Art, mit der Target auf Aufrufe Ihrer Seite antwortet, hängt von der Version der verwendeten Target-Bibliothek ab und davon, ob die Implementierung der Besucher-ID vorhanden ist und ob die Besucher-ID existiert. Weitere Informationen finden Sie unter  [Antworten auf Target-Aufrufe nach Bibliotheksversion](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/call-responses-library-version.md#concept_A95A4758A1E7405D947E9B4BCB5D62F0).

>[!NOTE]
>
>Die mbox.js-Bibliothek wird nicht mehr weiterentwickelt. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. Weitere Informationen finden Sie unter [Migration von „mbox.js“ zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

## „mbox.js“, Version 63{#section_ED8EFCF653A845ED8927F759578C4A33}

**Target-Version:** 17.7.1

[!DNL mbox.js], Version 63 ist verfügbar. Weitere Informationen finden Sie unter [mbox.js herunterladen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/target-download-config-mbox.md).

Folgende Verbesserungen und Fehlerbehebungen sind in Version 63 von [!DNL mbox.js] enthalten:

* Behebung eines Problems bezüglich der SDID-Generierung bei der Verwendung von `mboxDefine()` und `mboxUpdate()`. Dies betrifft nur Clients mit der Besucher-API auf der Seite.

## „mbox.js“, Version 62 {#section_723A9119FE204183847D3B0929A99B41}

* Behobene Probleme mit Flackern in umgeleiteten Aktivitäten, wenn diese in Google Chrome aufgerufen wurden.
* Funktion `secureOnly` hinzugefügt, die anzeigt, ob mbox.js nur HTTPS verwenden soll oder ob es möglich ist, dass basierend auf dem Seitenprotokoll zwischen HTTP und HTTPS umgeschaltet wird. Es handelt sich hierbei um eine erweiterte Einstellung, deren Standardwert „falsch“ lautet.

## „mbox.js“, Version 61 {#section_F3B59C5578B64883AE013B9342151193}

**Target-Version:** 16.7.2

**Releasedatum:** 28. Juli 2016

„mbox.js“, Version 61 enthält die folgenden Erweiterungen:

* Der ID-Generierungsalgorithmus „mboxSession“ in der JavaScript-Datums-API generiert nun eine zufällige Zeichenfolge, anstatt einen Zeitstempel und eine zufällige Zeichenfolgen zu verwenden.
* Die folgenden Details treffen nur zu, wenn Sie auf Ihrer Seite die Besucher-API verwenden:

   * [!DNL mbox.js], Version 61 überschreibt die Eigenschaft `loadTimeout` der Besucher-API nicht. Kunden können zur Steuerung der Besucher-API-Integration `visitorApiTimeout` und `visitorApiPageDisplayTimeout` verwenden.
   * Es wurde die Einstellung `optoutEnabled` hinzugefügt, die künftige Abwahlfunktionen in Adobe Experience Cloud unterstützen soll. Der Standardwert ist „false“. Ist die Eigenschaft aktiviert, werden alle Abfragen asynchron gegen den [!DNL /ajax]-Endpunkt ausgeführt, wie es in Version 60 der Fall war.
   * Die Ausblendung des Textkörpers ist standardmäßig deaktiviert. Target blendet den Textkörpers nur aus, wenn die automatische Erstellung der globalen Mbox und das Ausblenden des Textkörpers aktiviert sind.
   * Sind keine Besucher-ID-Cookies von Experience Cloud vorhanden, werden beim erstmaligen Laden der Seite Abfragen asynchron gegen [!DNL /ajax] ausgeführt. Beim zweiten Laden der Seite setzt Target den normalen Fluss ein, da die Besucher-ID-Werte bereits vorhanden sind.
   * Sollten Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität und bei der Verwendung von mbox.js Version 61 (oder neuer) oder at.js Version 0.9.1 (oder neuer) keinen Trackingserver angeben. Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

## „mbox.js“, Version 60   {#section_3BDAB885FA13444A8D35940A4BFF5825}

**Target-Version:** 16.4.1

**Veröffentlichungsdatum:** 21. April 2016

Standardmäßig werden Seiteninhalte nicht ausgeblendet. Bei Version 60 werden Seiteninhalte nur ausgeblendet, wenn die Option „Globale Mbox automatisch erstellen“ aktiviert ist. Für das Ausblenden von Seiten wird die CSS-Eigenschaft `opacity:0` verwendet statt `display:none`. Somit wird die ordnungsgemäße Bereitstellung schneller Seiten sowie die Abstimmung mit [!DNL at.js] gewährleistet.

Der Textkörper kann mithilfe zweier Einstellungen ausgeblendet werden:

* `bodyHidingEnabled` Die Standardeinstellung ist „false“, was bedeutet, dass der HTML-TEXTKÖRPER nicht ausgeblendet wird.

* bodyHiddenStyle

   Der Standardwert lautet `body{opacity:0}`. Dieser Wert kann abgeändert werden, beispielsweise in `body{display:none}`.

Diese Einstellungen können beispielsweise durch Folgendes ignoriert werden:

```
<script> 
window.targetGlobalSettings = { 
 bodyHidingEnabled: true, 
 bodyHiddenStyle: "body{opacity:0}", 
 visitorApiPageDisplayTimeout: 2000 
}; 
</script>
```

In der Ausblendetechnik werden Stil-Tags verwendet, mit deren Hilfe Stile hinzugefügt und entfernt werden. Somit wird sichergestellt, dass die Stile der Seite nach Ausführung des Ausblendecodes der Seite unverändert bleiben.

**Anwender von DTM:** Beachten Sie, dass diese Option die Verwendung automatischer Importoptionen verhindert, da die oben beschriebene Konfiguration in der Oberfläche von Target nicht gespeichert werden kann. Arbeiten Sie mit den oben stehenden Anweisungen und kopieren Sie den Inhalt in das Codefenster der benutzerdefinierten Hostingoption.

Außerdem werden in Version 60 alle Mboxes über einen AJAX-Endpunkt aufgerufen, wenn die Datei [!DNL visitorAPI.js] für den Experience Cloud-Besucher-ID-Service vorhanden ist. Dies ist erforderlich, da Besucher-API-Methoden asynchron sind. Ein Vorteil dieses Ansatzes liegt in der drastisch verkürzten Start-Render-Zeit, da Mbox-Anforderungen das Rendering nicht blockieren. Das bedeutet jedoch auch, dass alle [!DNL Target]-Angebotsinhalte asynchron ausgeführt werden, sodass jeglicher Angebotscode entsprechend programmiert werden muss. Angebote, die `document.write` enthalten, und anderer Code, der darauf ausgelegt ist, beim ersten Laden der Seite ausgeführt zu werden, werden nicht erwartungsgemäß ausgeführt.

* Ansynchrone Aufrufe in V60

   Bei der Verwendung von V60 mit dem Besucher-ID-Service werden alle Mbox-Aufrufe asynchron durchgeführt. Diese Arbeitsweise bei der Verwendung von Mboxes ist neu, gehen Sie bei der Aktualisierung auf diese Version also vorsichtig vor. Lesen Sie sich die [Hinweise zu asynchronen Aufrufen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#section_B586360A3DD34E2995AE25A18E3FB953) in der Dokumentation von [!DNL at.js] durch ([!DNL at.js] arbeitet ebenfalls mit asynchronen Aufrufen), um einige der Risiken kennenzulernen.
* Mögliches Flackern neuer Besucherszenarien

   Bei der Verwendung der Versionen 58, 59 und 60 im Besucher-ID-Service werden Mbox-Aufrufe erst durchgeführt, wenn die Besucher-ID gesetzt wurde (oder bis eine Zeitüberschreitung aufgetreten ist). Dies geschieht beim erstmaligen Laden einer Seite durch einen neuen Besucher.

## „mbox.js“, Version 59   {#section_FF0E70C4C17E402D8374DE428C5D996E}

**Target-Version:** 16.2.1

**Veröffentlichungsdatum:** 17. Februar 2016

„mbox.js“, Version 59 enthält die folgenden Erweiterungen:

* Die Mbox-Deaktivierung wurde auf 30 Minuten verringert.
* Ein Fehler, der beim Aus-/Einblenden von Seiten auftrat, wurde behoben.

   Statt `display:none`, wie in Version 58, wird zum Ausblenden der Seite `opacity:0` verwendet. Diese Änderung verhindert Fehler, die bei der vorherigen Methode zum Ausblenden von Seiten bei Websites im Responsive-Design auftraten.

## „mbox.js“, Version 58   {#section_5070B0D1C87F4937BB97727923DD36C7}

**Target-Version:** 15.7.1

**Veröffentlichungsdatum:** 30. Juli 2015

Diese Version von mbox.js ist erforderlich, wenn Sie Analytics als Berichtsquelle für Target verwenden, und wird für Profile und Zielgruppen dringend empfohlen.

Version 58 von mbox.js stellt sicher, dass der Experience Cloud-Besucher-ID-Service eine Besucher-ID zurückgibt, bevor Target-Aufrufe gesendet werden. Dadurch wird sichergestellt, dass die Zielgruppendaten, die über die Profil- und Zielgruppen-Kerndienste freigegeben werden, für den ersten Target-Aufruf in der Benutzersitzung zur Verfügung stehen. Um das Flackern von Standardinhalten vor der Rückgabe der Testinhalte zu vermeiden, blendet Target den `<BODY>` aus, bis der Besucher-ID-Service zurückgibt. `display:none` kommt zum Einsatz, um die Seite auszublenden.

Diese Aktualisierung behebt auch einen Fehler, der beim Verwenden von Analytics als Berichtsquelle für Target auftrat und dazu führte, dass eine zu hohe Anzahl an Besuchern in Analytics-Berichten für Besuche erfasst wurden, die nur eine Seite umfassten.

mbox.js legt Werte für die Zeitüberschreitung fest, falls der Besucher-ID-Service nichts zurückgibt. Die Standardzeitüberschreitung für den Besucher-ID-Service beträgt 500 ms (0,5 Sekunden). Ein weiterer Wert für die Zeitüberschreitung legt die Obergrenze dafür fest, wie lange das `<BODY>`-Tag ausgeblendet wird. Der Standardwert beträgt 500 ms (0,5 Sekunden). Diese Zeitüberschreitungen können durch Einfügen des folgenden Codes vor der mbox.js-Referenz auf jeder Seite geändert werden:

```
<script> 
window.targetGlobalSettings = { 
 visitorApiTimeout: 500, 
 visitorApiPageDisplayTimeout: 500 
}; 
</script> 
```

„mbox.js“, Version 58 oder neuer führt Nicht-JavaScript-Inhalte der globalen Mbox unmittelbar nach dem HTML-Tag `BODY` aus. JavaScript-Inhalte innerhalb des Tags `<script>` der globalen Mbox werden nach Auslösen von `DOMContentLoaded` ausgeführt. Diese Reihenfolge der Inhaltsbereitstellung gewährleistet, dass JavaScript-Inhalte der globalen Mbox ordnungsgemäß bereit- und dargestellt werden.

## „mbox.js“, Version 57 {#section_6BA1CDBF75B14A94B59E8624ACF583D4}

**Target-Version:** 15.4.1

**Veröffentlichungsdatum:** 21. April 2015

Folgende Änderungen wurden in dieser Version vorgenommen:

* Die automatisch erstellte Antwort der globalen Mbox für Target Standard verwendet document.write() nicht mehr oder erstellt ein `<div>` Element.

   Dadurch wird die Anforderung entfernt, dass die Datei mbox.js das letzte Element in `<head>` der Seite sein muss. Eine starke QS wird für die Aufrüstung auf diese neue Version empfohlen.

   Diese Änderung kann Änderungen am Verhalten bei der Bereitstellung einiger Angebotstypen verursachen. Die folgenden spezifischen Bedingungen müssen in Betracht gezogen werden:

   * HTML-Inhalte, die als Teil eines „Plug-in-Angebots“ zurückgegeben wurden, werden nicht korrekt gerendert, doch JavaScript in den Angeboten wird erwartungsgemäß ausgeführt.
   * Für JavaScript-Angebote, die an die globale Mbox zurückgegeben werden, kann der JavaScript-Code in das Tag `<script>` eingebettet oder durch ein `src`-Attribut referenziert werden.

      Fügen Sie dazu das `async`-Attribut dem Skriptaufruf wie folgt hinzu:

      `<script src='external-url' async='true'></script>`

      Beachten Sie, dass das `async`-Attribut im Internet Explorer nur eingeschränkt unterstützt wird (Details finden Sie hier:[https://developer.mozilla.org/de/docs/Web/HTML/Element/script#Browser_compatibility](https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility)); daher sollten Sie Besucher, die ältere IE-Versionen nutzen, von den Tests ausschließen, die diese Drittanbieterskripts enthalten.

* Es wurden Probleme behoben, die in Version 56 gemeldet wurden, und zwar aufgrund der Änderungen im Extra JavaScript-Abschnitt von mbox.js. Der gesamte Code im Extra JavaScript-Abschnitt ist im globalen Gültigkeitsbereich erneut verfügbar.

Die folgende Funktionalität wird in mbox.js, Version 57 nicht unterstützt:

* Eine automatisch in Target Standard erstellte globale Mbox funktioniert nicht mit gehosteten Angebotstypen von Target Classic. Gehostete Angebotstypen sind „Angebot auf Ihrer Site“ und „Angebot außerhalb von Test&amp;Target“.

   Dies bedeutet, dass Sie in Target Classic die automatisch in Target Standard erstellte Mbox nicht auswählen sollten, wenn eines dieser Angebote erforderlich ist.
* Es werden nur JavaScript-Plug-ins unterstützt.

   Wenn das Angebot eines Plug-ins JavaScript-Code und HTML kombiniert, dann wird der JavaScript-Code ausgeführt, doch der HTML-Inhalt wird nicht angezeigt.

mbox.js, Version 57 umfasst auch wichtige Fehlerbehebungen:

* Es wurde ein Problem behoben, durch das das SiteCatalyst-Plug-in in mbox.js v56 nicht funktionierte.
* Es wurde ein Problem behoben, das aufgrund von Änderungen des Gültigkeitsbereichs zu Extra JavaScript-Fehlern führte.
* Machen Sie die Änderungen am Konstruktor von mboxFactory rückgängig.

## „mbox.js“, Version 56 {#section_C4F4A53584B741FF9FD907D81CB7E164}

**Target-Version:** 15.1.2

**Veröffentlichungsdatum:** 17. Februar 2015

>[!NOTE]
>
>Einige Benutzer berichteten von Zeitüberschreitungen, wenn `target.js` nicht geladen werden konnte. In Version 57 wurde dieses Problem behoben. Verwenden Sie jedoch den [!DNL Experience Cloud Visitor ID]-Dienst, benötigen Sie mindestens Version 58.

Folgende Änderungen wurden in dieser Version vorgenommen:

* Änderungen bei Recommendations Premium zur Unterstützung der Übermittlung von Parametern an globale mbox
* Es wird ein 5-Sekunden-Timeout zum target.js-Ladeaufruf hinzugefügt. In dem seltenen Fall, dass die Datei nicht geladen wird, wird die Seite gerendert und es werden keine Target Standard-Aktivitäten angezeigt.
* „Extra JavaScript“ wurde zur Ausführung vor der globalen Mbox verschoben.

   Alle Einstellungen in v56+ werden mit einem Namensraum versehen. Wenn Funktionen durch „extra JavaScript“ deklariert werden, müssen diese mit dem Präfix `window` versehen werden.

   Beispiel:

   `function foo {`

   `}`

   wird zu:

   `window.foo = function() {`

   `}`

   Variablen, die global erreichbar sein sollen, müssen ebenfalls mit dem Präfix `window` versehen werden.

* Ein Cookie namens „em-disabled“ wurde hinzugefügt, das mbox.js dem Benutzer gibt, wenn target.js bei der Zustellung nicht geladen wird. Dieses Cookie verhindert, dass Angebote, die mit dem Visual Experience Composer erstellt wurden, auf der Site gerendert werden. Benutzer mit diesem Cookie sehen weder den Testinhalt noch werden sie in diesen Aktivitätsberichten gezählt. Alle anderen Angebotsinhalte (zum Beispiel von Kampagnen in Target Classic) werden weiterhin geladen. Das Cookie hat eine Lebensdauer von 30 Minuten ab dem Zeitpunkt des Ladefehlers.

## Mbox, Version 55

**Target-Version:** 15.1

**Veröffentlichungsdatum:** 19. Januar 2015

Version 53 wird durch IE-Korrekturen ergänzt.

## Mbox, Version 54

**Target-Version:** 14.9.2

**Releasedatum:** 30. September 2014

Ändert die globale Mbox-Implementierung von „document.write“ auf „AJAX“. Dadurch wird die Anforderung entfernt, dass die mbox.js-Datei das letzte Element im Abschnitt der Seite `<head>` sein muss. Diese Version steht nur via API zur Verfügung. Klienten können die Version herunterladen und diese mbox.js-Datei verwenden. Bei einigen Sites treten im Zusammenhang mit dieser Implementierung flackernde Inhalte auf. Daher sollten Sie die Integration in Ihre Site überprüfen.

## Mbox, Version 53

**Target-Version:** 14.9.1

**Releasedatum:** 14. September 2014

Das Problem, dass einige Target-Seitenparameter in Internet Explorer nicht korrekt ausgelöst werden, wurde behoben.

## Mbox, Version 52

**Target-Version:** 14.8

**Releasedatum:** 14. August 2014

Die Funktion mboxParameter funktioniert jetzt in Target Standard und Premium.

Es wurde ein Fehler behoben, der verhindert hat, dass die Analytics-Verfolgung in IE 9 und 11 funktioniert. Diese Änderung betrifft ausschließlich Nutzer von Analytics.

Die [Übermittlung von Parametern](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) ist jetzt in Array-Form, als JSON-Objekt oder als kommagetrennte Liste (zuvor unterstützt) an die target-global-mbox möglich, mithilfe der Funktion targetPageParams().

M2PcId und alles mit Bezug zu VisitorId wurde umbenannt.

Die Löschung der defaultDiv einer registrierten Mbox wurde gestattet.

## Mbox, Version 51

**Target-Version:** 14.6

**Releasedatum:** 25. Juni 2014

Es wurde ein Fehler behoben, der ein falsches Cookie auf Sites mit zwei Zeichen in ihrer obersten Domäne gesetzt hat.

Es wurde ein geringfügiger Fehler in mbox.js behoben, der zur Rückgabe von Hashtag-Werten geführt hat.

## Mbox, Version 50

Die Synchronisierung zwischen Target Standard und Target Classic wurde verbessert.

## Mbox, Version 49

Die Internet Explorer 10-Unterstützung für geschachtelte Mboxes wurde verbessert.

## Mbox, Version 48

Unterstützung für Adobe Analytics als Berichtsquelle für Target.

## Mbox, Version 47

„mbox.js“ unterstützt nun die Verwendung eines benutzerdefinierten globalen Mbox-Namens für Target Standard.

## Mbox, Version 46

Vollständige Unterstützung für den Experience Cloud-Besucher-ID-Service für die Implementierung von Target Standard mit einer einzelnen Codezeile. Dies ermöglicht die serverseitige Integration von Adobe Analytics und das gemeinsame Profil von Experience Cloud.

Es wurde ein Problem bei der Bereitstellung von Inhalt in IE10 im Dokumentenmodus behoben.

## Mbox, Version 45

Vollständiger Support für den Experience Cloud-Besucher-ID-Service. Dies ermöglicht die serverseitige Integration von Adobe Analytics und das gemeinsame Profil von Experience Cloud.

## Mbox, Version 44

Neuer Parameter in URL durch mboxVizTarget hinzugefügt:

mboxDOMLoaded

## Mbox, Version 43

Support für Target Standard hinzugefügt.

## Mbox, Version 42

Ersten Support für den Experience Cloud-Besucher-ID-Service hinzugefügt.

## Mbox, Version 41

* Auch mit der Einstellung „nur x“ den Erstanbieter-Cookie deaktivieren, um die Ladezeit zu verbessern und ständige Seitenaktualisierungen zu verhindern

   Ein Timeout-Cookie wird gesetzt, wenn der Aufruf an Target nicht rechtzeitig zurückgegeben wird. Dies ist eine schnellere Methode als lediglich das Drittanbieter-Cookie zu verwenden. Wenn lediglich das Drittanbieter-Cookie verwendet wird, wird die Seite kontinuierlich aktualisiert, während auf eine positive Antwort von den Target-Servern gewartet wird.

* Problem mit der Traffic-Begrenzung behoben, die nur noch auftritt, wenn mbox.js aktiviert ist

   Dieses Problem ist bei Traffic-Beschränkungen für die mbox.js von Kunden aufgetreten, die dazu geführt haben, dass die Timeout-Einstellung nicht funktioniert. Dies hat dazu geführt, dass die Seite aktualisiert wurde, während auf eine positive Antwort von den Target-Servern gewartet wurde.

* Problem mit SiteCatalyst-Plug-in behoben, damit es immer den Ajax Fetcher benutzt

   Vor dieser Änderung kam es für Benutzer des Test&amp;Target-to-SiteCatalyst-Plug-ins zu Situationen, bei denen abhängig vom Ladezeitpunkt des Plug-ins ein document.write ausgelöst werden konnte, das die Seite löschte.

## Mbox, Version 38

Support für seitenbasierten SiteCatalyst für die Test&amp;Target-Integration (muss aktiviert sein)

## Mbox, Version 37

Verschlüsselte URL-Schlüssel

## Mbox, Version 36

Änderung von Mbox zur Verwendung von tt.omtrdc.net

## Mbox, Version 35

* mbox debug ist jetzt immer remote
* mboxTime-Parameter hinzugefügt. Dieser Parameter ist die Zeit, wie sie der Benutzer sieht, in ms seit dem Zeitraum, GMT. Dieser wird nur einmal berechnet.

## Mbox, Version 34

* Versucht immer, das aktuelle Standard-div abzurufen, anstatt auf eine zwischengespeicherte Version zu verweisen.

   Dies behebt ein Problem mit einem zwischengespeicherten div für Standardinhalte, das aufgrund eines mboxUpdate nicht in dem DOM ist, das den Inhalt für das Standard-div bereitgestellt hat.

* mbox.getDefaultDiv hat einen neuen optionalen booleschen Parameter. Wenn dieser wahr ist, wird das aktuelle Standard-div zurückgegeben. Wenn er false ist, wird das letzte zwischengespeicherte Standard-div zurückgegeben.
* mbox.loaded zur Unterstützung von Ajax-Load aktualisiert
* Der mboxURL-Parameter wird jetzt mit encodeURIComponent anstatt mit escape verschlüsselt
* Testet, ob encodeURIComponent durch den Browser unterstützt wird, und zeigt Standardinhalt an, falls dies nicht der Fall ist. Außerdem wurden folgende mbox.js-Konfigurationsoptionen entfernt:
   * encode\_mbox\_parameters
   * mbox\_signal\_support
