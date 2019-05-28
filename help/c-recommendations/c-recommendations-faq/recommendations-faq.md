---
description: Liste der häufig gestellten Fragen (FAQs) zu Recommendations-Aktivitäten.
keywords: Fehlerbehebung; häufig gestellte Fragen; FAQ; FAQs; Empfehlungen; Sonderzeichen; Attributgewichtung; Ähnlichkeit von Inhalten
seo-description: Liste der häufig gestellten Fragen (FAQs) zu Recommendations-Aktivitäten.
seo-title: Recommendations-FAQs
solution: Target
title: Recommendations-FAQs
title-outputclass: premium
topic: Premium
uuid: 27752811-0ffe-4d60-83d1-39e18b1953d5
badge: premium
translation-type: tm+mt
source-git-commit: 9261f626f43ccd17c9b8c86a361642ae9833e3e2

---


# ![PREMIUM](/help/assets/premium.png) FAQ zu Empfehlungen{#recommendations-faq}

Liste der häufig gestellten Fragen (FAQs) zu Recommendations-Aktivitäten.

## Was ist der erwartete Zeitrahmen für Recommendations-Vorgänge?

Die folgenden Änderungen sollten innerhalb von etwa 60 Minuten widergespiegelt werden:

* Elementattribute, die in der Designvorlage zurückgegeben werden.
* Elementattribute, die in globalen Ausschlussregeln verwendet werden, die verhindern, dass das Element in zurückgegebene Empfehlungen aufgenommen wird.
* Elementattribute, die in Einschlussregeln in den Kriterien verwendet werden, die Auswirkungen darauf haben, ob das Element in zurückgegebenen Empfehlungen einbezogen oder ausgeschlossen wird.

Die folgenden Änderungen werden erst wirksam, wenn der nächste Algorithmus ausgeführt wird (12-24 Stunden):

* Elementattribute, die in den für die Aktivität verwendeten Sammlungsregeln verwendet werden.
* Elementattribute, die in einer Promotion basierend auf einem Attribut oder einer Sammlung verwendet werden, die mit der Aktivität verknüpft ist.
* Element-Kategorie, in der das Element für eine &quot;Aktuelle Kategorie&quot; oder&quot; Favoritenkategorie&quot; im Algorithmus &quot;Topverkäufe&quot; oder&quot; Am meisten angezeigt&quot; angezeigt wird.
* Rangordnung empfohlener Artikel, wenn das Attribut sich geändert hat und als benutzerdefinierter Schlüssel für einen Algorithmus verwendet wird.
* Rangordnung empfohlener Artikel basierend auf dem geänderten Attribut (n), wenn die Empfehlungslogik &quot;Elemente mit ähnlichen Attributen&quot; lautet, wenn die Gewichtungsfaktoren&quot; Inhaltähnlichkeit&quot; verwendet werden oder wenn die Faktoren &quot;Attributgewichtung&quot; verwendet werden.

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

Die verfügbaren Kriterien basieren auf der aktuellen Kategorie. Beim Erstellen von Recommendations-Angeboten zeigt der Algorithmus-Wähler Kriterien auf Grundlage der Kategorie-ID an.

Wenn der Speicherort, auf den Sie diese Kriterien anwenden, die Kategorie-ID nicht enthält, sind im Algorithmus-Wähler bestimmte Kriterien nicht verfügbar.

Bei der Verwendung eines Speicherorts, unter dem die Kategorie-ID in der Mbox vorhanden ist, enthält der Kriterien-Wähler alle anwendbaren Kriterien.

Das Ziel verfügt über eine Einstellung zum [Filtern inkompatibler Kriterien](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84), um die intelligente Filterung der Algorithmusauswahl zu steuern.

>[!NOTE]
>
>Diese Einstellung gilt nur für Aktivitäten, die im Visual Experience Composer (VEC) erstellt wurden. Sie gilt nicht für Aktivitäten, die im Formular-basierten Experience Composer erstellt wurden (Target verfügt über keinen Speicherortkontext).

Wenn Sie auf die Einstellung [!UICONTROL Inkompatible Kriterien filtern] zugreifen möchten, klicken Sie auf [!UICONTROL Recommendations] &gt; [!UICONTROL Einstellungen]:

![](assets/recs_settings_filter.png)

Wenn die Einstellung [!UICONTROL Inkompatible Kriterien filtern] NICHT aktiviert ist, filtert Target Algorithmen im Algorithmus-Wähler nicht, und es werden alle Algorithmen angezeigt.

Wenn die Einstellung [!UICONTROL Inkompatible Kriterien filtern] aktiviert ist, liest Target in VEC-Aktivitäten die entityId- und Kategorie-ID-Einträge aus dem gewählten Speicherort und zeigt dann Algorithmen basierend auf `currentItem|currentCategory` an (wenn für den jeweiligen Speicherort entsprechende Werte vorhanden sind). Daraufhin werden im Algorithmus-Wähler standardmäßig nur kompatible Algorithmen für den gewählten Speicherort angezeigt.

Bei aktivierter Einstellung [!UICONTROL Inkompatible Kriterien filtern] können Sie nichtkompatible Algorithmen trotzdem anzeigen, indem Sie beim Auswählen von Kriterien das Kontrollkästchen [!UICONTROL Kompatibel] deaktivieren.

![](assets/compatible_checkbox.png)

Die folgende Liste enthält Sonderfälle, in denen das Kontrollkästchen [!UICONTROL Kompatibel] in Target nicht angezeigt wird:

* Der Speicherort enthält sowohl entityId- als auch Kategorie-ID-Einträge. In diesem Fall erfolgt keine Filterung.
* Sie verwenden [!DNL mbox.js] der Version 55 oder früher.
* Auf der Seite werden keine Mbox-aufrufe ausgelöst (!config.isAutoCreateGlobalMbox &amp;&amp; !config.isRegionalmbox)
* Es sind keine Target-Parameter definiert.

## Was sollte ich tun, wenn eine Sammlung in Recommendations den Wert null (0) annimmt?   {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

Beachten Sie die folgenden Informationen, wenn eine Sammlung, die zuvor nicht null war, den Wert null annimmt:

* Sie können die Sammlung erneut speichern und prüfen, ob der Wert aktualisiert wird. Beachten Sie, dass durch das erneute Speichern die Sammlung alle Algorithmen erneut ausführt, die diese Sammlung verwenden.
* Befinden Sie sich in der richtigen Umgebung? Zu [!DNL /target/products.html#recsSettings] gehen, um gegenzuprüfen (wie unten dargestellt).

   ![](assets/product_catalog.png)

* Ist Ihr Index aktuell? Überprüfen Sie bei [!DNL /target/products.html#productSearch], wie viele Stunden der Index alt ist (z. B. „Vor 3 Stunden indiziert“). Sie können den Index bei Bedarf aktualisieren.
* Haben Sie Änderungen am Feed oder an der Datenebene vorgenommen, die dazu geführt haben, dass Ihre Entitäten nicht mehr mit den Sammlungsregeln übereinstimmen? Stellen Sie sicher, dass die Groß-/Kleinschreibung übereinstimmt (Beachtung der Groß-/Kleinschreibung).
* Wurde der Feed erfolgreich ausgeführt? Hat jemand Änderungen am FTP-Verzeichnis, Kennwort usw. vorgenommen?
* Target setzt Aktualisierungen an der Bereitstellung (auf der Seite/App des Kunden) schnellstmöglich um. Dennoch müssen für den Vermarkter auf der Benutzeroberfläche einige Darstellungen bereitgestellt werden. Bereitstellungsaktualisierungen werden nicht zwingend verzögert, um auf die Synchronisierung der Benutzeroberflächenaktualisierungen zu warten. Mithilfe von [mboxTrace](https://marketing.adobe.com/resources/help/en_US/target/target/c_content_trouble.html#) können Sie die Inhalte des Systems zu dem Zeitpunkt anzeigen, zu dem eine Anforderung eingeht.

## Worin besteht der Unterschied zwischen der allgemeinen und der Inhaltsähnlichkeits-spezifischen Attributgewichtung? {#section_FCD96598CBB44B16A4C6C084649928FF}

Die Attributgewichtung liegt in zwei Formen vor: „Standardattributgewichtung“ und „Inhaltsähnlichkeits-Attributgewichtung“.

Die „Standardattributgewichtung“ gilt für die meisten, wenn nicht gar für alle Kriterientypen (nicht nur „Inhaltsähnlichkeit“). Dieser Gewichtungstyp gewichtet bestimmte Attributwerte stärker. Im folgenden Beispiel werden Nike-Produkte in den Ausgabeempfehlungen angestoßen.

![](assets/attribute_weighting_example.png)

Die „Inhaltsähnlichkeits-Attributgewichtung“ gilt nur für Kriterien der Inhaltsähnlichkeit.

Dieser Gewichtungstyp ist dynamischer und basiert auf dem aktuellen „Empfehlungsschlüssel“ (dem derzeit angezeigten Element). Wenn im folgenden Beispiel (Marke x 16) ein Besucher Sneaker von Nike anzeigt, werden diesem Besucher mit höherer Wahrscheinlichkeit andere Nike-Produkte empfohlen (nicht nur Sneaker) als Sneaker von anderen Herstellern. Wenn ein Besucher Sneaker der Marke Adidas anzeigen würde, würden ihm wahrscheinlich Adidas-Produkte empfohlen.

![](assets/content_similarity_example.png)

## Warum ist Target manchmal nicht in der Lage, Empfehlungen anzuzeigen?   {#section_DB3F40673AED42228E407C05437D99E9}

Target kann manchmal keine Empfehlungen anzeigen, wenn zu wenig Empfehlungen verfügbar sind.

Die Anzahl der pro Kriterium generierten Werte ist die 5-fache Anzahl der im Design angegebenen Entitäten. Die Laufzeitfilterung (beispielsweise Inventar, Mbox-Attributabgleich) wird angewendet, nachdem die 5x-Werte generiert wurden. Daher ist es möglich, dass zur Bereitstellungszeit weniger als 5x-Werte vorhanden sind. Erhöhen Sie zum Abschwächen dieser Situation die Anzahl der Entitäten im Design, indem Sie zusätzliche Entitäten ausblenden.

Das folgende JavaScript kann zu Beginn des Designs verwendet werden, um die Anzahl der angeforderten Entitäten zu erhöhen. In diesem Beispiel würde die angeforderte Anzahl von Entitäten 50 (5 x 10) betragen.

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

## Welche Größenbeschränkung besteht für einen API-Aufruf beim Einfügen/Aktualisieren von Produkten? Kann ich 50.000 Produkte mit einem Aufruf aktualisieren, indem ich die API statt eines Feeds verwende?   {#section_434FE1F187B7436AA39B7C14C7895168}

Target begrenzt Posts auf Anwendungsebene auf 50 MB. Dies erfolgt jedoch nur, wenn der Content-Type-Header `application/x-www-form-urlencoded` übergeben wird.

Sie können sicherlich versuchen, 50.000 Produkte in einem einzigen Aufruf zu senden. Wenn das nicht funktioniert, teilen Sie die Produkte in Batches auf. Normalerweise wird empfohlen, dass Kunden Aufrufe in Batches mit jeweils 5.000 oder 10.000 Produkten aufteilen, um die Wahrscheinlichkeit einer Zeitüberschreitung aufgrund von hoher Systemauslastung zu reduzieren.

## Muss ich einen Mbox-Namen angeben, wenn ich Recommendations-Kriterien, -Promotions oder Vorlagentestregeln erstelle?   {#section_FFA42ABCC5954B48A46526E32A3A88A2}

Beim Erstellen von Recommendations-Kriterien, -Promotions oder Vorlagentestregeln, die auf einem basieren, erhalten Sie von `mboxParameter`mboxParameter keine Aufforderung mehr, `mboxName` einzugeben. Der Mbox-Name ist nun optional. Mit dieser Änderung können Sie Parameter aus mehreren Mboxes verwenden oder auf einen Parameter verweisen, der noch nicht am Rand aufgezeichnet wurde.

So wählen Sie den gewünschten Parameter aus:

* Wählen Sie beim Erstellen neuer Kriterien, Promotions oder Vorlagentestregeln einen Parameter aus der Liste aus oder geben Sie die ersten Buchstaben des Parameternamens bzw. den gesamten Namen des gewünschten Parameters ein.
* Wenn Sie den Mbox-, aber nicht den Parameternamen kennen, filtern Sie mithilfe des Kontrollkästchens nach der bekannten Mbox, die den gewünschten Parameter übergibt.

Bei keiner der Methoden gibt es eine Verbindung zwischen Mbox und Parameter. Die Kriterien, Promotions oder Vorlagentestregeln funktionieren basierend auf dem Parameter über alle Mboxes hinweg, die diesen Parameter übergeben.

Wenn Sie bestehende Kriterien, Promotions oder Vorlagentestregeln bearbeiten, werden die Filterkriterien mit dem Mbox-Namen angezeigt, der bei der Erstellung angegeben wurde.

## Warum kann ich meine alte Recommendations-Aktivität nicht speichern, nachdem ich eine neue Zielgruppe definiert habe?   {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

Stellen Sie sicher, dass die Zielgruppe einen eindeutigen Namen aufweist. Wenn Sie der Zielgruppe den Namen einer bereits vorhandenen Zielgruppe zugewiesen haben, können Sie die alte Recommendations-Aktivität, also Recommendations-Aktivitäten, die vor Oktober 2016 erstellt wurden, nicht speichern.

## Wie groß dürfen CSV-Dateien für den Feedupload maximal sein?   {#section_20F1AF4839A447B9889B246D6E873538}

Es gibt keine feste Grenze hinsichtlich der Zeilen oder Dateigröße für den Feedupload von CSV-Dateien. Als Best Practice empfehlen wir jedoch, die CSV-Datei auf 1 GB zu beschränken, um Fehler während des Uploadprozesses zu vermeiden. Wenn die Größe der Datei 1 GB übersteigt, teilen Sie sie am besten in mehrere Feeddateien auf. Die maximale Anzahl benutzerdefinierter Attributspalten ist 100 und benutzerdefinierte Attribute sind auf 4.096 Zeichen beschränkt. Zusätzliche Beschränkungen zur Länge der erforderlichen Spalten finden Sie auf der   [Seite mit Target-Beschränkungen](../../r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1).

## Kann ich eine Entität dynamisch ausschließen?

In der Abfragezeichenfolge können Sie Entitäts-IDs für Entitäten übermitteln, die Sie aus Ihren Empfehlungen ausschließen möchten. So kann es beispielsweise hilfreich sein, Artikel auszuschließen, die sich bereits im Warenkorb befinden.

Verwenden Sie den Mbox-Parameter `excludedIds`, um die Ausschlussfunktion zu aktivieren. Dieser Parameter verweist auf eine Liste mit kommagetrennten Entitäts-IDs. Beispiel, `mboxCreate(..., "excludedIds=1,2,3,4,5")`. Der Wert wird übermittelt, wenn Empfehlungen angefordert werden.

>[!NOTE]
>
>Wenn zu viele Entitäten ausgeschlossen werden, verhalten sich Empfehlungen so, als wären nicht genug Entitäten vorhanden, um die Empfehlungsvorlage auszufüllen.

Hängen Sie `entityIds`das `&excludes=${mbox.excludedIds}` Token an die Inhalts-URL des Angebots an. Wenn die Inhalts-URL extrahiert wird, werden die erforderlichen Parameter mit aktuellen Mbox-Anforderungsparametern ersetzt.

Standardmäßig ist diese Funktion für neu erstellte Empfehlungen aktiviert. Bestehende Empfehlungen müssen gespeichert werden, um dynamisch ausgeschlossene Entitäten zu unterstützen.
