---
keywords: Fehlerbehebung; häufig gestellte Fragen; FAQ; FAQs; Recommendations; Sonderzeichen; Attributgewichtung; Ähnlichkeit von Inhalten
description: Ansicht einer Liste häufig gestellter Fragen und Antworten zur Adobe [!DNL Target] Recommendations-Aktivitäten.
title: Wo finde ich Fragen und Antworten zu [!DNL Target] Recommendations?
feature: Recommendations
exl-id: aaa52923-1c2d-44ae-bd89-671329222077
translation-type: tm+mt
source-git-commit: 921245d9b8e2f5d99c0abf1606df9d4fd553a7b5
workflow-type: tm+mt
source-wordcount: '2995'
ht-degree: 57%

---

# ![PREMIUM](/help/assets/premium.png) FAQ zu Recommendations

Liste der häufig gestellten Fragen (FAQs) zu [!DNL Adobe Target] [!DNL Recommendations]-Aktivitäten.

## Warum zeigt [!UICONTROL Katalogsuche] nicht die richtigen Ergebnisse, wenn ich nach einem benutzerdefinierten Attribut mit einem numerischen Wert suche?

Wenn Sie eine Katalogsuche für ein benutzerdefiniertes Attribut mit einem numerischen Wert durchführen, wird das benutzerdefinierte Attribut als String-Typ und nicht als numerischer Wert betrachtet.

Derzeit gibt es keine Funktion, mit der Kunden den Attributtyp ändern können. Wenn Sie eine Änderung vornehmen müssen, eröffnen Sie ein [Supportticket](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Geben Sie darin die Attribute an, deren Typ von „String“ in „numerisch“ geändert werden muss.

## Wie lange dauert es, bis Aktualisierungen an Elementen in meinem Katalog auf meiner Site erscheinen?

Der Zeitraum und die Ergebnisse hängen davon ab, wie die Elemente aktualisiert werden.

| Quelle | Details |
| --- | --- |
| Elementattribute aktualisiert über mbox oder API | <ul><li>Recommendations wird innerhalb von 15 Minuten aktualisiert.</li><li>Vorhandene Empfehlungen und Elementattribute werden angezeigt, bis Updates verfügbar sind.</li><li>Die Katalogsuche wird nach dem Katalogindex (3-8 Stunden) aktualisiert.</li></ul> |
| Elementattribute aktualisiert über Feed | <ul><li>Recommendations wird nach der Feed-Erfassung aktualisiert (2-8 Stunden).</li><li>Vorhandene Empfehlungen und Elementattribute werden angezeigt, bis Updates verfügbar sind.</li><li>Die Katalogsuche wird nach der Feed-Erfassung (2-8 Stunden) und nach dem anschließenden Katalogindex (3-8 Stunden) aktualisiert. Die Katalogsuche wird innerhalb von insgesamt 5-16 Stunden aktualisiert.</li></ul> |
| Aus dem Katalog gelöschtes Element über die [!DNL Target]-Benutzeroberfläche oder -API | <ul><li>Recommendations wird innerhalb von 15 Minuten aktualisiert.</li><li>Vorhandene Empfehlungen und Elementattribute werden angezeigt, bis Updates verfügbar sind.</li><li>Die Katalogsuche wird nach dem Katalogindex (3-8 Stunden) aktualisiert.</li></ul> |
| Element, das über die mbox oder API zum Katalog hinzugefügt wird | <ul><li>Recommendations wird nach der Ausführung des Algorithmus aktualisiert. Algorithmusausführungen werden alle 12 Stunden für 1-2-Tage-Algorithmen und alle 24 Stunden für 7+ Tage-Algorithmen geplant.</li><li>Bestehende Empfehlungen werden angezeigt, bis Updates verfügbar sind, wenn das hinzugefügte Element kein angeforderter Schlüssel ist.</li><li>Reserveempfehlungen werden angezeigt, bis Aktualisierungen verfügbar sind, wenn das hinzugefügte Element ein angeforderter Schlüssel ist.</li><li>Die Katalogsuche wird nach dem Katalogindex (3-8 Stunden) aktualisiert.</li></ul> |
| Element, das über Feed zum Katalog hinzugefügt wird | <ul><li>Recommendations wird nach der Erfassung des Feeds aktualisiert (2-8 Stunden). Nachfolgende Algorithmusausläufe werden alle 12 Stunden für 1-2-Tage-Algorithmen und alle 24 Stunden für 7-Tage-Algorithmen geplant. Recommendations wird innerhalb von 2-32 Stunden aktualisiert.</li><li>Bestehende Empfehlungen werden angezeigt, bis Updates verfügbar sind, wenn das hinzugefügte Element kein angeforderter Schlüssel ist.</li><li>Reserveempfehlungen werden angezeigt, bis Aktualisierungen verfügbar sind, wenn das hinzugefügte Element ein angeforderter Schlüssel ist.</li><li>Die Katalogsuche wird nach der Feed-Erfassung (2-8 Stunden) und nach dem Katalogindex (3-8 Stunden) aktualisiert. Die Katalogsuche wird innerhalb von insgesamt 5-16 Stunden aktualisiert.</li></ul> |

Nach dem Import einer Feed-Datei oder nach dem Empfang von Entitäts-Updates über API oder Mbox werden die folgenden Änderungen in unter 60 Minuten übernommen:

* Wenn ein Element zuvor ausgeschlossen wurde, aber nun einbezogen werden sollte, wird das Element bei der nächsten Algorithmusausführung (12-24 Stunden) einbezogen.

   Dies geschieht, weil [!DNL Target] Ausschlüsse online und offline anwendet. Wenn ein Artikel neu ausgeschlossen wird, gilt der Online-Ausschluss schnell. Wenn ein Element neu eingeschlossen wird, verschwindet der Online-Ausschluss schnell, der Offline-Ausschluss wird jedoch erst ausgeblendet, wenn der nächste Algorithmus ausgeführt wird.

* Wenn ein Element zuvor enthalten war, aber jetzt ausgeschlossen werden sollte, wird das Element gemäß der Meldung &quot;Elementattribute aktualisiert...&quot;ausgeschlossen. Die oben besprochene Zeitleiste hängt von der Feed-Quelle ab (15 Minuten über mbox/API oder 12-24 Stunden über Feed).

Die folgenden Änderungen werden erst wirksam, wenn der nächste Algorithmus ausgeführt wird (innerhalb von 12 bis 24 Stunden):

* Elementattribute, die in den für die Aktivität verwendeten Sammlungsregeln verwendet werden.
* Elementattribute, die in einer Promotion basierend auf einem Attribut oder einer Sammlung verwendet werden, die mit der Aktivität verknüpft ist.
* Elementkategorie, in der das Element für eine „aktuelle Kategorie“ oder „Favoritenkategorie“ im Algorithmus „Topverkäufe“ oder „Am äftesten angesehen“ angezeigt wird.
* Rangordnung empfohlener Artikel, wenn das sich geänderte Attribut ein benutzerdefiniertes Attribut ist, das als benutzerdefinierter Schlüssel für einen Algorithmus verwendet wird.
* Rangordnung empfohlener Artikel basierend auf einem oder mehreren geänderten Attributen, wenn die Empfehlungslogik „Artikel mit ähnlichen Attributen“ lautet oder wenn die Gewichtungsfaktoren „Ähnlicher Inhalt“ oder die Faktoren „Attributgewichtung“ verwendet werden.

>[!NOTE]
>
>Eine Feed-Datei wird als importiert erachtet, wenn sich ihr Status von „Elemente werden importiert“ in „Aktualisierungen des Suchindex werden vorbereitet“ ändert. Es kann mehr als 60 Minuten dauern, bis Aktualisierungen in der Benutzeroberfläche der Katalogsuche angezeigt werden. Die Katalogsuche ist aktuell, wenn sich der Feedstatus in „Aktualisierungen abgeschlossen“ ändert. Auch wenn die Katalogsuche noch nicht auf dem neuesten Stand ist, spiegelt Ihre Site Aktualisierungen der oben aufgeführten Zeiträume wider. Auf der Seite „Katalogsuche“ wird die aktuelle Indexaktualisierungszeit der Katalogsuche angezeigt.

## Wie lange dauert es, bis die Konfiguration meiner [!UICONTROL Recommendations]-Aktivität, Angebot-, Promo- oder Kriterieneinstellungen auf meiner Site geändert wird?

* Eine Änderung der Promotion-Einstellungen kann bis zu fünf Stunden dauern, bis sie vor Ort angezeigt wird.
* Eine Änderung an anderen Kriterieneinstellungen wird möglicherweise erst angezeigt, wenn der nächste Algorithmus ausgeführt wird:

   * Einige Kriterieneinstellungen (z. B. &quot;Hinzufügen einer dynamischen Einschlussregel&quot;) werden sofort angezeigt.
   * Andere Kriterieneinstellungen (z. B. &quot;Entfernen einer dynamischen Einschlussregel&quot;, Änderung des Lookback-Fensters usw.) können erst nach Ausführung des nächsten Algorithmus einbezogen werden.
   * Algorithmusabläufe werden durch diese Änderungen ausgelöst, es kann jedoch bis zu 24 Stunden dauern. Algorithmen werden auch planmäßig alle 12-24 Stunden ausgeführt.

## Wie lange dauert es, bis das Verhalten eines Benutzers (z. B. beim Klicken auf Produkt A und beim Kauf von Produkt B) in den Empfehlungen für *angezeigt wird, die der Benutzer* erhält?

* Derzeit angezeigte/gekaufte Produkte/Inhalte beeinflussen die Empfehlungen, die der Benutzer in derselben Seitenansicht/[!DNL Target]-Inhaltsanforderung erhält.
* Historisches Benutzerverhalten, wie &quot;Zuletzt angezeigtes Produkt&quot;, &quot;Am meisten angezeigtes Produkt&quot;und der Gesamtüberblick zum Anzeigen/Kauf werden mit dieser Anforderung aktualisiert und beeinflussen die Empfehlungen, die der Benutzer bei der nächsten Seitenansicht/[!DNL Target]-Inhaltsanforderung erhält. Beispielsweise werden die Algorithmen &quot;Zuletzt angezeigte Artikel&quot;und &quot;Empfohlen für Sie&quot;mit jeder Ansicht/jedem Kauf aktualisiert und in der nachfolgenden Inhaltsanforderung angezeigt.

## Wie lange dauert es, bis das Verhalten eines Benutzers (z. B. Klicken auf Produkt A und Kauf von Produkt B) in den Empfehlungen für *andere* Benutzer angezeigt wird?

Das Benutzerverhalten in Aggregat wird in die Offline-Algorithmusverarbeitung einbezogen, wobei jeder Algorithmus alle 12-24 Stunden ausgeführt wird.

## Was sollte ich tun, wenn mein Array durch Sonderzeichen umbrochen wird? {#section_D27214116EE443638A60887C7D1C534E}

Verwenden Sie Escape-Werte in JavaScript. Das Array kann durch Anführungszeichen (&quot;) umbrochen werden. Der folgende Codeausschnitt ist ein Beispiel für Escape-Werte:

```
#set($String='') 
#set($escaper=$String.class.forName('org.apache.commons.lang.StringEscapeUtils')) 
<script type="text/javascript"> 
console.log("$escaper.escapeJavaScript($entity1.name)") 
console.log("$escaper.escapeJavaScript($entity2.name)") 
console.log('$escaper.escapeJavaScript($entity3.name)') 
names.push("$escaper.escapeJavaScript($entity4.name)") 
</script>
```

## Warum stehen beim Erstellen einer Recommendations-Aktivität nicht alle Kriterien, einschließlich benutzerdefinierter Kriterien, zur Verfügung?   {#section_B2265AC8B8A94E0298D495A05C5D817F}

Die verfügbaren Kriterien basieren auf der aktuellen Kategorie. Beim Erstellen von Recommendations-Angeboten zeigt die Algorithmusauswahl Kriterien auf Grundlage der Kategorie-ID an.

Wenn der Speicherort, auf den Sie diese Kriterien anwenden, die Kategorie-ID nicht enthält, sind im Algorithmus-Wähler bestimmte Kriterien nicht verfügbar.

Bei der Verwendung eines Speicherorts, unter dem die Kategorie-ID in der Mbox vorhanden ist, enthält die Kriterienauswahl alle anwendbaren Kriterien.

[!DNL Target] hat einen  [Filter Inkompatible ](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) Kriterien, um die intelligente Filterung der Algorithmusauswahl zu steuern.

>[!NOTE]
>
>Diese Einstellung gilt nur für Aktivitäten, die im Visual Experience Composer (VEC) erstellt wurden. Diese Einstellung gilt nicht für Aktivitäten, die im Form-Based Experience Composer erstellt wurden ([!DNL Target] hat keinen Ortskontext).

Wenn Sie auf die Einstellung [!UICONTROL Inkompatible Kriterien filtern] zugreifen möchten, klicken Sie auf [!UICONTROL Recommendations] > [!UICONTROL Einstellungen]:

![](assets/recs_settings_filter.png)

Wenn die Einstellung [!UICONTROL Inkompatible Kriterien filtern] NICHT aktiviert ist, filtert Algorithmen im Algorithmus-Wähler nicht, und es werden alle Algorithmen angezeigt.[!DNL Target]

Ist die Einstellung [!UICONTROL Inkompatible Kriterien filtern] aktiviert, liest [!DNL Target] in VEC-Aktivitäten entityId und Kategorien-ID vom ausgewählten Speicherort und zeigt dann Algorithmen basierend auf `currentItem|currentCategory` an (sofern die entsprechenden Werte an diesem Speicherort vorhanden sind). Daraufhin werden im Algorithmus-Wähler standardmäßig nur kompatible Algorithmen für den gewählten Speicherort angezeigt.

Bei aktivierter Einstellung [!UICONTROL Inkompatible Kriterien filtern] können Sie nichtkompatible Algorithmen trotzdem anzeigen, indem Sie beim Auswählen von Kriterien das Kontrollkästchen [!UICONTROL Kompatibel] deaktivieren.

![](assets/compatible_checkbox.png)

Die folgende Liste enthält Sonderfälle, in denen [!DNL Target] das Kontrollkästchen [!UICONTROL Kompatibel] nicht anzeigt:

* Der Speicherort enthält sowohl entityId- als auch Kategorie-ID-Einträge. In diesem Fall erfolgt keine Filterung.
* Sie verwenden [!DNL mbox.js] der Version 55 oder früher.
* Auf der Seite werden keine Mbox-Aufrufe ausgelöst (!config.isAutoCreateGlobalMbox &amp;&amp; !config.isRegionalMbox)
* [!DNL Target] -Parameter nicht definiert.

## Was sollte ich tun, wenn eine Sammlung in Recommendations den Wert null (0) annimmt?   {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

Beachten Sie die folgenden Informationen, wenn eine Sammlung, die zuvor nicht null war, den Wert null annimmt:

* Sie können die Sammlung erneut speichern und prüfen, ob der Wert aktualisiert wird. Durch das erneute Speichern führt die Sammlung alle Algorithmen, die diese Sammlung verwenden, erneut aus.
* Befinden Sie sich in der richtigen Umgebung? Zu [!DNL /target/products.html#recsSettings] gehen, um gegenzuprüfen (wie unten dargestellt).

   ![](assets/product_catalog.png)

* Ist Ihr Index aktuell? Überprüfen Sie unter [!DNL /target/products.html#productSearch], wie alt der Index ist (z. B. „Vor 3 Stunden indiziert“). Sie können den Index bei Bedarf aktualisieren.
* Haben Sie Änderungen am Feed oder an der Datenebene vorgenommen, die dazu geführt haben, dass Ihre Entitäten nicht mehr mit den Sammlungsregeln übereinstimmen? Stellen Sie sicher, dass die Groß-/Kleinschreibung übereinstimmt (Beachtung der Groß-/Kleinschreibung).
* Wurde der Feed erfolgreich ausgeführt? Wurden das FTP-Verzeichnis, das Kennwort usw. geändert?
* [!DNL Target] setzt Aktualisierungen an der Bereitstellung (auf der Seite/App des Kunden) schnellstmöglich um. [!DNL Target] muss jedoch auch eine gewisse Darstellung in der Benutzeroberfläche für den Marketingspezialisten bereitstellen. [!DNL Target] wartet mit Bereitstellungsaktualisierungen nicht auf die Synchronisierung der Benutzeroberflächenaktualisierungen. Mithilfe von [mboxTrace](/help/c-activities/c-troubleshooting-activities/content-trouble.md) können Sie die Inhalte des Systems zu dem Zeitpunkt anzeigen, zu dem eine Anforderung eingeht.

## Worin besteht der Unterschied zwischen der allgemeinen und der Inhaltsähnlichkeits-spezifischen Attributgewichtung? {#section_FCD96598CBB44B16A4C6C084649928FF}

Die Attributgewichtung liegt in zwei Formen vor: „Standardattributgewichtung“ und „Inhaltsähnlichkeits-Attributgewichtung“.

Die „Standardattributgewichtung“ gilt für die meisten, wenn nicht gar für alle Kriterientypen (nicht nur „Inhaltsähnlichkeit“). Dieser Gewichtungstyp gewichtet bestimmte Attributwerte stärker. Im folgenden Beispiel werden Nike-Produkte in den Ausgabeempfehlungen angestoßen.

![](assets/attribute_weighting_example.png)

Die „Inhaltsähnlichkeits-Attributgewichtung“ gilt nur für Kriterien der Inhaltsähnlichkeit.

Dieser Gewichtungstyp ist dynamischer und basiert auf dem aktuellen „Empfehlungsschlüssel“ (dem derzeit angezeigten Element). Wenn im folgenden Beispiel (Marke x 16) ein Besucher Sneaker von Nike anzeigt, werden diesem Besucher mit höherer Wahrscheinlichkeit andere Nike-Produkte empfohlen (nicht nur Sneaker) als Sneaker von anderen Herstellern. Wenn ein Besucher Sneaker der Marke Adidas anzeigen würde, würden ihm wahrscheinlich Adidas-Produkte empfohlen.

![](assets/content_similarity_example.png)

## Warum können Empfehlungen manchmal nicht angezeigt werden? {#section_DB3F40673AED42228E407C05437D99E9}[!DNL Target]

[!DNL Target] kann manchmal keine Empfehlungen anzeigen, wenn zu wenig Empfehlungen verfügbar sind.

Die Anzahl der pro Kriterium generierten Werte ist die dreifache Anzahl der im Design angegebenen Entitäten. Die Laufzeitfilterung (beispielsweise Inventar, Mbox-Attributabgleich) wird angewendet, nachdem die 3x-Werte generiert wurden. Daher ist es möglich, dass zur Bereitstellungszeit weniger als 3x-Werte vorhanden sind. Erhöhen Sie zum Mindern dieser Situation die Anzahl der Entitäten im Design, indem Sie andere Entitäten ausblenden.

Das folgende JavaScript kann zu Beginn des Designs verwendet werden, um die Anzahl der angeforderten Entitäten zu erhöhen. In diesem Beispiel würde die angeforderte Anzahl von Entitäten 30 (3 x 10) betragen.

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

## Welche Größenbeschränkung besteht für einen API-Aufruf beim Einfügen/Aktualisieren von Produkten? Kann ich 50.000 Produkte mit einem Aufruf aktualisieren, indem ich die API statt eines Feeds verwende?   {#section_434FE1F187B7436AA39B7C14C7895168}

[!DNL Target] begrenzt Posts auf Anwendungsebene auf 50 MB – allerdings nur, wenn der Content-Type-Header `application/x-www-form-urlencoded` übergeben wird.

Sie können sicherlich versuchen, 50.000 Produkte in einem einzigen Aufruf zu senden. Wenn das nicht funktioniert, empfiehlt sich eventuell eine Aufteilung der Produkte in Batches. Adobe empfiehlt Kunden die Aufteilung ihrer Aufrufe in Batches von jeweils 5.000 oder 10.000 Produkten. Dadurch lassen sich Zeitüberschreitungen aufgrund einer zu hohen Systemauslastung umgehen.

## Muss ich den Mbox-Namen angeben, wenn ich Testregeln für Recommendations-Kriterien, -Promotions oder -Vorlagen erstelle? {#section_FFA42ABCC5954B48A46526E32A3A88A2}

Beim Erstellen von Recommendations-Kriterien, -Promotions oder Vorlagentestregeln, die auf einem basieren, erhalten Sie von `mboxParameter`mboxParameter keine Aufforderung mehr, `mboxName` einzugeben. Der Mbox-Name ist nun optional. Mit dieser Änderung können Sie Parameter aus mehreren Mboxes verwenden oder auf einen Parameter verweisen, der noch nicht am Rand aufgezeichnet wurde.

So wählen Sie den gewünschten Parameter aus:

* Wählen Sie beim Erstellen einer Testregel für Kriterien, Promotions oder Vorlagen einen Parameternamen aus der Liste aus. Geben Sie die ersten Zeichen oder auch den vollständigen Namen des gewünschten Parameters ein.
* Wenn Sie den Mbox-, aber nicht den Parameternamen kennen, filtern Sie mithilfe des Kontrollkästchens nach der bekannten Mbox, die den gewünschten Parameter übergibt.

Bei keiner der Methoden gibt es eine Verbindung zwischen Mbox und Parameter. Eine Testregel für Kriterien, Promotions oder Vorlagen verarbeitet die Parameter aller Mboxes, die diesen Parameter übergeben.

Wenn Sie bestehende Kriterien, Promotions oder Vorlagentestregeln bearbeiten, werden die Filterkriterien mit dem Mbox-Namen angezeigt, der bei der Erstellung angegeben wurde.

## Warum kann ich meine alte Recommendations-Aktivität nicht speichern, nachdem ich eine neue Zielgruppe definiert habe?   {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

Stellen Sie sicher, dass die Zielgruppe einen eindeutigen Namen aufweist. Wenn Sie der Zielgruppe den Namen einer bereits vorhandenen Zielgruppe zugewiesen haben, können Sie die alte Recommendations-Aktivität, also Recommendations-Aktivitäten, die vor Oktober 2016 erstellt wurden, nicht speichern.

## Wie groß dürfen CSV-Dateien für den Feedupload maximal sein?   {#section_20F1AF4839A447B9889B246D6E873538}

Es gibt keine feste Grenze hinsichtlich der Zeilen oder Dateigröße für den Feedupload von CSV-Dateien. Als Best Practice empfiehlt Adobe jedoch, die CSV-Datei auf 1 GB zu beschränken, um Fehler während des Uploadprozesses zu vermeiden. Wenn die Größe der Datei 1 GB übersteigt, teilen Sie sie am besten in mehrere Feeddateien auf. Die maximale Anzahl benutzerdefinierter Attributspalten ist 100 und benutzerdefinierte Attribute sind auf 4.096 Zeichen beschränkt. Weitere Längenbeschränkungen für erforderliche Spalten finden Sie auf der Seite [[!DNL Target] Beschränkungen in ](/help/r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1).

## Kann ich eine Entität dynamisch ausschließen? {#exclude}

In der Abfragezeichenfolge können Sie Entität-IDs für Entitäten übermitteln, die Sie von Ihren Recommendations ausschließen möchten. Beispielsweise können Sie Artikel ausschließen, die sich bereits im Warenkorb befinden.

Verwenden Sie den Mbox-Parameter `excludedIds`, um die Ausschlussfunktion zu aktivieren. Dieser Parameter verweist auf eine Liste kommagetrennter Entitäts-IDs. Zum Beispiel `mboxCreate(..., "excludedIds=1,2,3,4,5")`. Der Wert wird übermittelt, wenn Empfehlungen angefordert werden.

Der Ausschluss wird nur für den aktuellen [!DNL Target]-Aufruf ausgeführt. Elemente werden bei nachfolgenden Aufrufen von [!DNL Target] nur dann ausgeschlossen, wenn der Wert `excludedIds` erneut übergeben wird. Wenn Sie die Artikel im Warenkorb auf jeder Seite aus Ihren Empfehlungen ausschließen möchten, müssen Sie den `excludedIds`-Wert auf jeder Seite übergeben.

>[!NOTE]
>
>Wenn zu viele Entitäten ausgeschlossen werden, verhalten sich die Recommendations so, als wären nicht ausreichend Entitäten zum Ausfüllen der Recommendations-Vorlage vorhanden.

Hängen Sie zum Ausschluss von `entityIds` das Token `&excludes=${mbox.excludedIds}` an die Inhalts-URL des Angebots an. Wenn die Inhalts-URL extrahiert wird, werden die erforderlichen Parameter mit aktuellen Mbox-Anforderungsparametern ersetzt.

Diese Funktion ist für neu erstellte Empfehlungen standardmäßig aktiviert. Bestehende Empfehlungen müssen gespeichert werden, um eine Unterstützung für dynamisch ausgeschlossene Entitäten zu gewährleisten.

## Was bedeutet die Antwort NO_CONTENT, die gelegentlich im Recommendations-Inhalts-Trace zurückgegeben wird?

NO_CONTENT wird zurückgegeben, wenn für die angeforderte Algorithmus- und Schlüsselkombination keine Recommendations verfügbar sind. Im Allgemeinen tritt diese Situation auf, wenn Backups für den Algorithmus deaktiviert sind und zudem mindestens eine der folgenden Bedingungen zutrifft:

* Die Ergebnisse sind noch nicht bereit.

   Diese Situation tritt normalerweise ein, wenn eine neu erstellte Aktivität zum ersten Mal gespeichert wird oder nachdem die Konfiguration der Sammlung, der Kriterien oder der in der Aktivität verwendeten Promotions geändert wurde.

* Die Ergebnisse sind für die angeforderte Algorithmus-/Schlüsselkombination bereit, jedoch noch nicht auf dem nächstgelegenen Edge-Server zwischengespeichert.

   Die Anforderung löst einen Caching-Vorgang aus. Dieses Problem sollte sich daher nach einigen Seitenneuladungen und/oder nach einigen Minuten von alleine lösen.

* Die Ergebnisse sind bereit, aber für den bereitgestellten Schlüsselwert nicht verfügbar.

   Diese Situation tritt in der Regel auf, wenn Empfehlungen für ein Element angefordert werden, das erst nach der Ausführung des letzten Algorithmus zum Katalog hinzugefügt wurde. Das Problem sollte sich nach der nächsten Ausführung des Algorithmus von alleine lösen.

* Das teilweise Vorlagen-Rendering ist deaktiviert, weswegen nicht genügend Ergebnisse zum Ausfüllen der Vorlage verfügbar sind.

   Diese Situation tritt in der Regel auf, wenn eine dynamische Einschlussregel eingerichtet ist, die aggressiv viele Elemente aus den möglichen Ergebnissen herausfiltert. Zur Vermeidung dieser Situation aktivieren Sie Backups, wenden die Einschlussregel aber nicht auf die Backups an. Oder Sie verwenden das Kriterium in Verbindung mit einem weniger aggressiv gefilterten Kriterium.

## Bestehen Empfehlungen, die auf kürzlich angezeigten Artikeln basieren, für einen Besucher auf mehreren Geräten? {#persist-across-devices}

Wenn ein Besucher eine Sitzung initiiert, wird die Sitzungs-ID an einen einzigen Edge-Computer gebunden und ein temporärer Profil-Cache wird auf diesem Edge-Computer gespeichert. Nachfolgende Anforderungen aus derselben Sitzung lesen diesen Profil-Cache, einschließlich der zuletzt angezeigten Elemente.

Wenn die Sitzung beendet wird (im Allgemeinen, wenn sie nach 30 Minuten ohne Aktivität abläuft), wird der Sitzungsstatus einschließlich der zuletzt angezeigten Elemente auf eine beständige Profil-Datenspeicherung am selben geografischen Rand beibehalten.

Nachfolgende Sitzungen von verschiedenen Geräten können dann auf diese zuletzt angezeigten Artikel zugreifen, solange die neue Sitzung mit dem Profil des Kunden über die gleiche Marketing Cloud-ID (MCID), Experience Cloud-ID (ECID) oder CustomerID/mbox3rdPartyId verknüpft ist.

Wenn ein Besucher gleichzeitig zwei aktive Sitzungen hat, werden die zuletzt angezeigten Artikel auf einem Gerät nicht aktualisiert, es sei denn, die Geräte müssen die Sitzungs-ID freigeben. Es gibt eine mögliche Problemumgehung, aber [!DNL Target] unterstützt nicht direkt die Freigabe einer Sitzungs-ID für mehrere Geräte. Der Kunde muss diese ID-Freigabe selbst verwalten.

Dieses Verhalten tritt weiterhin auf, wenn ein Besucher auf einem Gerät aktiv ist und dann einige Minuten später auf dem anderen Gerät aktiv wird. Die Sitzung des ersten Geräts läuft nicht 30 Minuten ab. Es kann bis zu fünf Minuten Verspätung eintreten, bevor der Status des Profils in den Status &quot;Dauerhaft&quot;geschrieben und verarbeitet wird. Die Sitzungsdauer beträgt etwa 35 Minuten, und das Profil wird beim Testen dieses Verhaltens gespeichert.

Wenn der Besucher nicht gleichzeitig über zwei aktive Sitzungen verfügt, werden die zuletzt auf dem anderen Gerät angezeigten Artikel, die zuletzt auf einem Gerät angezeigt wurden, aktualisiert, solange die Sitzung beendet ist. Die Sitzung läuft beim Testen dieses Verhaltens nach 35 Minuten ab.

## Kann ich einen Algorithmus verwenden, der in [!DNL Adobe Recommendations Classic] in [!DNL Recommendations Premium] erstellt wurde?

Ein in [!DNL Recommendations Classic] erstellter Algorithmus wird in [!DNL Recommendations Premium] nicht unterstützt. Sie können möglicherweise den alten Algorithmus in [!DNL Target Premium] verwenden; Allerdings kann der Algorithmus beim Deaktivieren oder Löschen der Aktivität in der [!DNL Target Premium]-Benutzeroberfläche Synchronisierungsprobleme verursachen. Weitere Informationen zu den Unterschieden zwischen den beiden Lösungen finden Sie unter [[!DNL Recommendations Classic] versus [!DNL Recommendations] Aktivitäten in [!DNL Target Premium]](/help/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md).


