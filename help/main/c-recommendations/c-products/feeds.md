---
keywords: Empfehlungs-Feed; Feed; SAINT; ftp; csv;klassifizierungen;analytics classifications
description: Erfahren Sie, wie Feeds Entitäten mithilfe von CSV-Dateien, dem Feed-Format für die Google-Produktsuche und [!DNL Analytics] Produktklassifizierungen in [!DNL Adobe Target] [!DNL Recommendations] importieren.
title: Wie verwende ich [!UICONTROL Feeds] in  [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: 7b336a9e-23f4-4b09-9c8f-b9cb68162b1b
source-git-commit: a0cf6d497fc5b9a04888d0c6597c98bbbb639cbe
workflow-type: tm+mt
source-wordcount: '2463'
ht-degree: 45%

---

# Feeds

Verwenden Sie Feeds, um Entitäten in [!DNL Adobe Target] [!DNL Recommendations] zu importieren. Entitäten können mit CSV-Dateien, dem Google Product Search-Feed-Format und [!DNL Adobe Analytics] Produktklassifizierungen gesendet werden.

## Feeds - Übersicht {#concept_D1E9C7347C5D4583AA69B02E79607890}

Mit Feeds können Sie [Entitäten](/help/main/c-recommendations/c-products/products.md) übergeben oder Ihre Mbox-Daten mit Informationen ergänzen, die entweder nicht auf der Seite verfügbar sind oder nicht sicher von der Seite gesendet werden können, z. B. Marge, COGS usw.

Mit Feeds können Sie detaillierte Elementinformationen an [!DNL Recommendations] übergeben, z. B. Produkt-ID, Kategorie, Name, Nachricht und andere Attribute.

Sie können auswählen, welche Spalten aus Ihrer [!DNL Target] -Produktklassifizierungsdatei oder Google-Produktsuchdatei Sie an den [!DNL Recommendations] -Server senden möchten.

Diese Datenelemente zu den einzelnen Elementen können dann zu folgenden Zwecken verwendet werden:

* Werte in Entwürfen anzeigen
* Definieren von Kriterieneinschlussregeln
* Sortieren von Elementen in verschiedene Sammlungen
* Ausschlüsse auf Empfehlungen anwenden

Elementbeschreibungen können mithilfe von Feeds oder Mboxes an [!DNL Target] übergeben werden. Wenn Daten von einem Entitäts-Feed und einer Mbox erfasst werden, haben die aktuellen Daten Priorität. In der Regel stammen die aktuellen Daten von einer mbox, da sie häufiger angezeigt wird. Für den seltenen Fall, dass die Entitäts-Feed-Daten und die Mbox-Daten gleich aktuell sind, werden die Mbox-Daten verwendet.

Die Liste [!UICONTROL Feeds] ( **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]**) enthält Informationen zu allen Feeds, die Sie erstellt haben.

![Feeds-Seite](/help/main/c-recommendations/c-products/assets/feeds-page.png)

Die Seite [!UICONTROL Feeds] enthält die folgenden Spalten:

* **Name**: Der Name des beim Erstellen angegebenen Feeds. Um den Namen eines Feeds zu bearbeiten, müssen Sie den Feed bearbeiten. Wenn Sie den Feed mit dem neuen Namen speichern, wird der Feed aktualisiert.
* **Typ**: Zu den Typen zählen [CSV](/help/main/c-recommendations/c-products/feeds.md#section_65CC1148C7DD448FB213FDF499D35FCA), [Google-Produkt-Feed](/help/main/c-recommendations/c-products/feeds.md#section_8EFA98B5BC064140B3F74534AA93AFFF) und [Analytics Classifications](/help/main/c-recommendations/c-products/feeds.md#section_79E430D2C75443BEBC9AA0916A337E0A).
* **Status**: Der aktuelle [Status des Feeds](/help/main/c-recommendations/c-products/feeds.md#concept_E475986720D1400999868B3DFD14A7A0).
* **Zeitplan**: Zeigt den Aktualisierungszeitplan für den Feed an: [!UICONTROL Daily], [!UICONTROL Weekly], [!DNL Every 2 Weeks] oder [!UICONTROL Never].
* **Artikel**: Zeigt die Anzahl der Artikel im Feed an.
* **Zuletzt aktualisiert**: Zeigt das Datum und die Uhrzeit der letzten Aktualisierung des Feeds sowie den Namen der Person an, die den Feed aktualisiert hat. Wenn der [!UICONTROL Last Updated] -Feed &quot;nicht definiert&quot;lautet, kommt der Feed von [!DNL Recommendations Classic] und kann nicht innerhalb von [!DNL Target Premium Recommendations] geändert werden.

Klicken Sie auf das Informationssymbol, um eine Karte mit dem Datum des letzten Uploads und der URL des Feeds anzuzeigen.

Klicken Sie auf das Auslassungssymbol, um auf die folgenden Aktionen zuzugreifen: [!UICONTROL Deactivate], [!DNL Edit], [!UICONTROL Copy] und [!UICONTROL Delete].

>[!IMPORTANT]
>
>Hochgeladene Entitäten und Entitätsattribute laufen nach 61 Tagen ab. Das bedeutet:
>
>* Ihr Feed sollte mindestens einmal monatlich ausgeführt werden, um sicherzustellen, dass Ihre Kataloginhalte nicht ablaufen.
>* Wenn Sie ein Element aus Ihrer Feed-Datei entfernen, wird dieses Element nicht aus Ihrem Katalog entfernt. Um das Element aus dem Katalog zu entfernen, löschen Sie es manuell über die [!DNL Target] -Benutzeroberfläche oder -API. Oder ändern Sie die Elementattribute (z. B. das Inventar), um sicherzustellen, dass das Element von der Berücksichtigung ausgeschlossen wird.

## Source-Typen

Entitäten können mit CSV-Dateien, dem Google Product Search-Feed-Format und [!DNL Adobe Analytics] Produktklassifizierungen gesendet werden.

### CSV {#section_65CC1148C7DD448FB213FDF499D35FCA}

Sie können eine CSV-Datei im proprietären CSV-Upload-Format [!DNL Adobe] erstellen. Die Datei enthält Anzeigeinformationen über die reservierten und benutzerspezifischen Attribute für Ihre Produkte. Ersetzen Sie zum Hochladen von für Ihre Implementierung spezifischen Attributen `CustomN` in der Kopfzeile durch den Namen des gewünschten Attributs. Im folgenden Beispiel wurde `entity.Custom1` ersetzt durch: `entity.availability`. Sie können die Datei anschließend per Massenvorgang auf den [!DNL Recommendations]-Server hochladen.

Die Verwendung des CSV-Formats bietet die folgenden Vorteile im Vergleich zum Google-Feed-Format:

* Das .csv-Format erfordert keine Feldzuordnungen.
* Das .csv-Format unterstützt Attribute mit mehreren Werten (siehe Beispiel unten).
* Das .csv-Format unterstützt bis zu 100 benutzerdefinierte Attribute. Wenn Sie mehr als 100 benutzerspezifische Attribute benötigen, können Sie eine zweite Feed-Datei erstellen, in dem ein anderer Satz an benutzerspezifischen Attributen angegeben wird.

Verwenden Sie die Massen-Upload-Methode, um Anzeigeinformationen zu senden, wenn Ihre Seite keine Mboxes enthält oder wenn Sie Ihre Anzeigeinformationen mit Artikeln ergänzen möchten, die nicht auf Ihrer Site verfügbar sind. So können Sie z. B. Lagerbestandsinformationen versenden, die auf der Site nicht zur Verfügung stehen.

Alle Daten, die mit der CSV-Datei, dem Google-Produkt-Feed oder dem [!DNL Analytics] Produkt-Classification-Feed hochgeladen wurden, überschreiben den vorhandenen Entitätsattributwert in der Datenbank. Wenn Sie Preisinformationen über Mbox-Anfragen und anschließend andere Preiswerte in einer Datei senden, überschreiben die Werte in der Datei die mittels Mbox-Anfrage festgelegten Werte. Eine Ausnahme bildet das Entitätsattribut `categoryId`, für das Kategoriewerte bis zu einer Längenbeschränkung von 250 Zeichen angehängt statt überschrieben werden.

>[!IMPORTANT]
>
>Verwenden Sie in Ihrer CSV-Datei keine Werte in doppelten Anführungszeichen (&quot;), sofern dies nicht beabsichtigt ist. Wenn Sie Werte in doppelten Anführungszeichen setzen, müssen Sie sie mit Escape-Zeichen versehen, indem Sie sie in einen anderen Satz doppelter Anführungszeichen einschließen. Doppelte Anführungszeichen ohne Escape-Zeichen verhindern das ordnungsgemäße Laden des Recommendations-Feeds.

Die folgende Syntax ist falsch:

```
"Apples "Bananas" Grapes"",
```

Die folgenden Syntax ist richtig:

```
"Apples ""Bananas"" Grapes""",
```

>[!NOTE]
>
>Sie können einen vorhandenen Wert nicht mit einem leeren Wert überschreiben. Übergeben Sie einen anderen Wert an seiner Stelle, um ihn zu überschreiben. Im Falle eines Verkaufspreises besteht eine gängige Lösung darin, entweder einen tatsächlichen &quot;NULL&quot;-Wert oder eine andere Meldung zu übermitteln. Sie können dann eine Vorlagenregel verfassen, um Artikel mit diesem Wert auszuschließen.

Das Produkt ist auf der Admin-Oberfläche ungefähr zwei Stunden nach dem erfolgreichen Upload seiner Entität verfügbar.

Im Folgenden finden Sie einen Beispielcode für eine CSV-Datei:

```
## RECSRecommendations Upload File 
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines. 
## RECS 
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left. 
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'. 
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations. 
## RECSentity.id,entity.name,entity.categoryId,entity.message,entity.thumbnailUrl,entity.value,entity.pageUrl,entity.inventory,entity.margin,entity.last_updated_by,entity.multi_english,entity.availability,entity.tax_country,entity.tax_region,entity.tax_rate,entity.product_type,entity.item_group_id,entity.color,entity.size,entity.brand,entity.gtin 
na3456,RipCurl Watch with Titanium Dial,Watches & Sport,Cutting edge titanium with round case,https://example.com/s7/na3456_Viewer,425,https://example.com/shop/en-us/na3456_RipCurl,24,0.25,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Titanium,44mm,RipCurl,"075380 01050 5" 
na3457,RipCurl Watch with Black Dial,Watches & Sport,Cutting edge matte black with round case,https://example.com/s7/na3457_Viewer,275,https://example.com/shop/en-us/na3457_RipCurl,24,0.27,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Black,44mm,RipCurl,"075340 01060 7"
```

### Google {#section_8EFA98B5BC064140B3F74534AA93AFFF}

Der Feed-Typ Google-Produktsuche verwendet das Google-Format. Dies unterscheidet sich vom proprietären CSV-Upload-Format [!DNL Adobe].

Wenn Sie über einen vorhandenen Google-Produkt-Feed verfügen, können Sie diesen als Ihre Importdatei verwenden.

>[!NOTE]
>
>Es müssen nicht Google-Daten verwendet werden. [!DNL Recommendations] verwendet dasselbe Format wie Google. Sie können mit dieser Methode alle Ihre Daten hochladen und dabei die verfügbaren Planungsfunktionen nutzen. Dennoch müssen Sie die von Google festgelegten und vordefinierten Attributnamen verwenden, wenn Sie die Datei einrichten.

Die meisten Einzelhändler laden Produkte in Google hoch. Wenn ein Besucher also die Google-Produktsuche verwendet, werden seine Produkte angezeigt. [!DNL Recommendations] berücksichtigt für Entitäts-Feeds exakt die Spezifikationen von Google. Entitäts-Feeds können an [!DNL Recommendations] über .xml, .txt oder .tsv gesendet werden und die von Google](https://support.google.com/merchants/answer/188494?hl=en&amp;topic=2473824&amp;ctx=topic#US) definierten [Attribute verwenden. Die Ergebnisse können auf den [Google-Shopping-Seiten](https://www.google.com/prdhp) durchsucht werden.

>[!NOTE]
>
>Die POST-Methode muss auf dem Server zugelassen sein, der den Google-Feed-Inhalt hostet.

Da [!DNL Recommendations] -Benutzer bereits .xml- oder .txt-Feeds konfigurieren, um sie per URL oder FTP an Google zu senden, akzeptieren Entitäts-Feeds diese Produktdaten und erstellen mit ihnen den Empfehlungskatalog. Geben Sie an, wo sich dieser Feed befindet, und der Recommendations-server ruft die Daten ab.

Wenn Sie die Google-Produktsuche für den Entitäts-Feed-Upload verwenden, müssen Sie weiterhin eine Produktseiten-Mbox auf der Seite haben, wenn Sie dort Empfehlungen anzeigen oder Produktansichten für die Algorithmusbereitstellung basierend auf Ansichten verfolgen möchten.

Google Feeds unterstützen nicht mehrere Werte für ein benutzerdefiniertes Attribut.

Der Feed wird zu dem Zeitpunkt ausgeführt, zu dem Sie ihn speichern und aktivieren. Er wird zu dem Zeitpunkt ausgeführt, zu dem Sie den Feed speichern, und dann täglich eine Stunde später.

Nachfolgend finden Sie einen Beispielcode für eine Feed-XML-Datei für die Google-Produktsuche:

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<feed xmlns="https://www.w3.org/2005/Atom" xmlns:ns2="https://base.google.com/ns/1.0" xmlns:ns3="https://base.google.com/cns/1.0"> 
    <title>Product Feed</title> 
    <link href="https://example.com"/> 
    <updated>2017-12-13T08:45:04.918-08:00</updated> 
    <author> 
        <name>Product Feed Author</name> 
    </author> 
    <id>https://example.com</id> 
    <entry> 
        <title>RipCurl Watch with Titanium Dial</title> 
        <description>Cutting edge Titanium with Round case</description> 
        <ns2:id>na3452</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3452_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 01050 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3452_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3452_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>425</ns2:price> 
        <ns2:product_review_average>5.0</ns2:product_review_average> 
        <ns2:product_review_count>30</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>375</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
    <entry> 
        <title>RipCurl Watch with Black Dial</title> 
        <description>Cutting edge matte black with Round case</description> 
        <ns2:id>na3453</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3453_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 013450 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3453_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3453_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>275</ns2:price> 
        <ns2:product_review_average>4.8</ns2:product_review_average> 
        <ns2:product_review_count>23</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>249</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
</feed> 
```

Nachfolgend finden Sie einen Beispielcode für eine Feed-TSV-Datei für die Google-Produktsuche:

```
id    title    description    link    price    condition    availability    image_link    tax    shipping_weight    shipping    google_product_category    product_type    item_group_id    color    size    gender    age_group    pattern    brand    gtin    mpn 
na3454    RipCurl Watch with Titanium Dial    Cutting edge titanium with round case    https://example.com/shop/en-us/na3454_RipCurl    425    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075380 01050 5    DZ1437 
na3455    RipCurl Watch with Black Dial    Cutting edge matte black with round case    https://example.com/shop/en-us/na3455_RipCurl    275    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075340 01060 7    DZ1446
```

### [!DNL Analytics] Produktklassifizierungen {#section_79E430D2C75443BEBC9AA0916A337E0A}

Die [!DNL Analytics] Produkt-Classification ist die einzige für Empfehlungen verfügbare Classification. Weitere Informationen zu dieser Klassifizierungsdatei finden Sie unter [Über Klassifizierungen](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) im Leitfaden *Analytics-Komponenten* . Es ist möglich, dass nicht alle für Empfehlungen benötigten Informationen in Ihrer aktuellen Implementierung verfügbar sind. Befolgen Sie dieses Benutzerhandbuch, wenn Sie es zu Ihrer Classification-Datei hinzufügen möchten.

>[!IMPORTANT]
>
>Beachten Sie vor dem Import von Entitätsdaten in [!DNL Recommendations] mithilfe von [!DNL Analytics] -Produktklassifizierungen, dass dies nicht die bevorzugte Methode ist.
>
> Beachten Sie die folgenden Einschränkungen:
>
>* Aktualisierungen an den Entitätsattributen umfassen eine zusätzliche Verzögerung von bis zu 24 Stunden.
>* [!DNL Target] unterstützt nur [!UICONTROL Product Classifications]. Die Produkt-SKU [!DNL Analytics] muss derselben Ebene wie die [!DNL Recommendations] `entity.id` zugeordnet sein. Benutzerdefinierte [!DNL Analytics] Klassifizierungen können mit [!UICONTROL Adobe Consulting Services] erstellt werden. Wenden Sie sich bei Fragen an Ihren Kundenbetreuer.

## Feed erstellen {#steps}

Erstellen Sie einen Feed, um Informationen über Ihre Produkte oder Services in [!DNL Recommendations] einzufügen.

1. Klicken Sie in der Target-Oberfläche auf **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]**.

   ![Erstellen eines Feed-Dialogfelds](assets/CreateFeed.png)

1. Geben Sie einen beschreibenden Namen für Ihren Feed an.
1. Wählen Sie einen **[!UICONTROL Source Type]** aus.

   * [!UICONTROL CSV]
   * [!UICONTROL Google Product Feed]
   * [!UICONTROL Analytics Classifications]

   Informationen zu den Feed-Typen [!UICONTROL CSV] und [!UICONTROL Google Product Feed] finden Sie unter [Feeds Overview](/help/main/c-recommendations/c-products/feeds.md#concept_D1E9C7347C5D4583AA69B02E79607890). Sie können auch [ein CSV-Modell-Handbuch herunterladen](/help/main/c-recommendations/c-products/assets/EntityFileUploadTemplate.csv), um den Feed korrekt zu formatieren.

1. (Bedingt) Wenn Sie **[!UICONTROL CSV]** oder **[!UICONTROL Google Product Feed]** ausgewählt haben, geben Sie den Speicherort an, an dem auf den Feed zugegriffen werden kann.

   * **FTP**: Wenn Sie „FTP“ ausgewählt haben, geben Sie die FTP-Serverdaten, die Anmeldedaten, den Dateinamen und das FTP-Verzeichnis an. Sie können FTP mit SSL (FTPS) für sicherere Uploads verwenden.

     Unterstützte FTP-Servereinstellungen:

      * FTP und FTPS müssen für die Verwendung von passivem FTP eingestellt sein.
      * Für FTPS konfigurieren Sie den Server so, dass er explizite FTPS-Verbindungen akzeptiert.
      * SFTP wird nicht unterstützt.
      * Sie können manuell einen Port angeben, an dem die Verbindung initiiert werden soll (z. B. `ftp://ftp.yoursite.com:2121`). Wenn Sie keinen Port angeben, wird der standardmäßige FTP- oder FTPS-Port verwendet.

   * **URL**: Wenn Sie [!UICONTROL URL] auswählen, geben Sie die URL an.

1. (Bedingt) Wenn Sie **[!UICONTROL Analytics Classifications]** ausgewählt haben, wählen Sie die Report Suite aus der Dropdownliste aus.

1. Klicken Sie auf den Pfeil **[!UICONTROL Next]** , um die Optionen [!UICONTROL Schedule] anzuzeigen.

   ![Schrittergebnis](assets/CreateFeedSchedule.png)

1. Wählen Sie eine Aktualisierungsoption aus:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 Weeks]
   * [!UICONTROL Never]: Planen Sie keine Aktualisierung. Wählen Sie diese Option aus, wenn Sie nicht möchten, dass dieser Feed ausgeführt wird.

1. Geben Sie die Zeit an, zu der Ihr Feed ausgeführt werden soll.

   Diese Option basiert auf der Zeitzone, die in Ihrem Browser verwendet wird. Wenn Sie einen Zeitpunkt in einer anderen Zeitzone verwenden möchten, müssen Sie diesen Zeitpunkt anhand Ihrer Zeitzone berechnen.

1. Klicken Sie auf den Pfeil **[!UICONTROL Next]** , um die Optionen [!UICONTROL Mapping] anzuzeigen, und geben Sie an, wie Sie Ihre Daten [!DNL Target] -Definitionen zuordnen möchten.

   ![Schrittergebnis](assets/CreatFeedMapping.png)

1. (Optional) Wenn der Feed einer Umgebung (Hostgruppe) zugeordnet werden soll, wählen Sie die Hostgruppe aus.

   Standardmäßig gehört der Feed zu allen Hostgruppen. So wird sichergestellt, dass Artikel in diesem Feed in jeder Umgebung verfügbar sind. Weitere Informationen finden Sie unter [Hosts](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

1. Klicken Sie auf **[!UICONTROL Save]**.

Nachdem Sie einen Feed erstellt oder bearbeitet haben, wird er sofort ausgeführt. Der Feed wird dann entsprechend den von Ihnen festgelegten Parametern aktualisiert. Es dauert ein wenig, bis die Informationen verfügbar sind. Zunächst muss der Feed synchronisiert, dann bearbeitet und anschließend indexiert werden, bevor er veröffentlicht und verfügbar gemacht werden kann. Der aktuelle Status wird unter [Feed-Status](/help/main/c-recommendations/c-products/feeds.md#status) in der Liste „Feeds“ angezeigt. Sie können [!DNL Target] schließen, bevor der Prozess abgeschlossen ist, und der Prozess wird weiter ausgeführt.

Während der Indexierung erscheinen Produkte und Feed-Header vor der Indexierung von individuellen Werten. Auf diese Weise können Sie Produkte durchsuchen und anzeigen, sodass Sie Sammlungen, Ausschlüsse, Designs und Aktivitäten erstellen können, bevor die Indizierung abgeschlossen ist.

Wenn als Status „Erfolg“ gemeldet wird, bedeutet dies, dass die Datei gefunden und korrekt analysiert wurde. Bis zum Abschluss der Indexierung, die abhängig von der Größe Ihrer Datei einige Zeit in Anspruch nehmen kann, steht die Information nicht zur Verwendung in [!DNL Recommendations] zur Verfügung. Wenn der Prozess fehlschlägt, bedeutet dies, dass die Datei nicht gefunden wurde. Sie haben beispielsweise eine falsche URL verwendet oder Ihre FTP-Informationen waren falsch oder es ist ein Parsing-Fehler aufgetreten.

## Feedstatus-Optionen und -Indikatoren {#concept_E475986720D1400999868B3DFD14A7A0}

Informationen über die möglichen Feedstatus-Optionen und deren Indikatoren.

### Feedstatus-Optionen {#status}

Folgende Statusoptionen stehen für Feeds zur Verfügung:

| Status | Beschreibung |
|--- |--- |
| [!UICONTROL Syncing] | Die Einrichtungsinformationen des Feeds werden in [!DNL Target] gespeichert. |
| [!UICONTROL Sync Failed] | Die Einrichtungsinformationen des Feeds konnten nicht in [!DNL Target] gespeichert werden. Erneut versuchen. |
| [!UICONTROL No Feed Run] | Sie haben einen Feed erstellt, aber nicht geplant (die Häufigkeit ist auf &quot;Nie&quot;eingestellt). |
| Geplant am *Tag und Uhrzeit* | Der Feed wurde nicht ausgeführt, jedoch für eine bestimmte Uhrzeit an einem bestimmten Tag geplant. |
| [!UICONTROL Waiting for Download] | [!DNL Target] bereitet den Download der Feed-Datei vor. |
| [!UICONTROL Downloading Feed File] | [!DNL Target] lädt die Feed-Datei herunter. |
| [!UICONTROL Importing Items] | [!DNL Target] importiert Elemente aus der Feed-Datei. |
| Feed erfolgreich importiert um *Zeit* | [!DNL Target] hat die Feed-Datei in sein Inhaltsbereitstellungssystem importiert. Änderungen an Artikelattributen wurden im Inhaltsbereitstellungssystem vorgenommen und werden in Kürze in den bereitgestellten Empfehlungen übernommen. Wenn die erwarteten Änderungen nicht angezeigt werden, versuchen Sie es erneut und aktualisieren Sie die Seite mit den Empfehlungen.<br>Hinweise:<ul><li>Wenn Änderungen an den Attributen eines Artikels dazu führen, dass ein Artikel aus Empfehlungen ausgeschlossen wird, wird der Ausschluss sofort übernommen. Wenn ein Element neu hinzugefügt wird oder Änderungen an Attributen dazu führen, dass ein Element *nicht mehr* aus Empfehlungen ausgeschlossen wird, wird es erst beim nächsten Algorithmus-Update angezeigt, das innerhalb von 24 Stunden erfolgt.</li><li>Wenn dieser Status angezeigt wird, werden die Aktualisierungen möglicherweise noch nicht in der Benutzeroberfläche von [!UICONTROL Catalog Search] angezeigt. Unter [!UICONTROL Catalog Search] wird ein separater Status angezeigt, der angibt, wann der durchsuchbare Katalog zuletzt aktualisiert wurde.</li></ul> |
| [!UICONTROL Failed to Index] | Die Index-Operation ist fehlgeschlagen. Erneut versuchen. |
| [!UICONTROL Server Not Found] | FTP- oder URL-Speicherorte sind ungültig oder nicht erreichbar. |

Um einen Feed zu aktualisieren (z. B. um Änderungen an Ihrer Feed-Konfiguration oder Feed-Datei vorzunehmen), öffnen Sie den Feed, nehmen Sie die gewünschten Änderungen vor und klicken Sie auf **[!UICONTROL Save]**.

>[!IMPORTANT]
>
>Hochgeladene Entitäten laufen nach 61 Tagen ab. Das bedeutet, dass Ihre Feed-Datei mindestens alle 60 Tage hochgeladen werden sollte, um eine Unterbrechung Ihrer Empfehlungsaktivitäten zu vermeiden. Wenn ein Element nicht mindestens alle 60 Tage in einer Feed-Datei (oder einer anderen Methode zur Aktualisierung der Entität) enthalten ist, zeigt [!DNL Target] an, dass das Element nicht mehr relevant ist, und entfernt es aus dem Katalog.

### Feedstatus-Indikatoren {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

Die folgenden Feedstatus-Indikatoren werden in der Spalte [!UICONTROL Status] angezeigt:

| Statusindikator | Beschreibung |
|--- |--- |
| Grüner Statusindikator | Wenn die Indexierung eines Feeds erfolgreich abgeschlossen wurde, zeigt ein grüner Statuspunkt an, dass der Feed einen erfolgreichen Status hat. |
| Gelber Statusindikator | Wenn ein Feed oder Feed-Index um 25 % der Feed-Frequenz verzögert wird, wird ein gelber Punkt für den Status angezeigt. Beispielsweise wird für einen Feed, der täglich ausgeführt wird, ein gelber Punkt angezeigt, wenn der Index sechs Stunden nach der geplanten Zeit nicht abgeschlossen wurde. Hinweis: Sobald der Feed-Status &quot;Warten auf Indexwarteschlange&quot;lautet, sind die neu aktualisierten Werte in der Bereitstellung und Kriterienverarbeitung verfügbar. |
| Weißer Statusindikator | Wenn ein Feed nicht geplant ist, gibt ein weißer Punkt für den Status an, dass der Feed noch nicht ausgeführt wurde. |
| Roter Statusindikator | Wenn der Feed keine Daten auf den Server hochladen kann, wird eine rote Statusanzeige angezeigt. |

Sehen Sie sich folgende Beispiele an:

**Beispiel 1:**

* Tag 1: Der tägliche Feed wird um 9:00 Uhr PST verarbeitet.
* Tag zwei: Es ist 15:30 Uhr und der Feed wurde seit gestern um 9:00 Uhr nicht ausgeführt

Der Status ist gelb, da der Index vor rund 6,5 Stunden erstellt werden sollte. 6,5 Stunden + 24 ergibt 127 % des Feed-Zeitfensters.

**Beispiel 2:**

* 1. Januar: Monatlicher Feed wird um 9:00 Uhr PST verarbeitet.
* 3. Februar: Es ist 10:00 Uhr und der Feed wurde einen Monat, einen Tag und eine Stunde lang nicht ausgeführt.

Der Status ist gelb, da der Index vor rund einem Tag und einer Stunde hätte ausgeführt werden müssen. Auch wenn dies nur (31 + (1 / 25)) / 30 = 1,03 % der Häufigkeitseinstellung ergibt, wurde der Höchstwert von einem Tag für die Verzögerung überschritten.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Grundlagen zu Feeds in Recommendations (3:01) ![Badge &quot;Überblick&quot;](/help/main/assets/overview.png)

Dieses Video enthält die folgenden Informationen:

* Den Zweck von Feeds verstehen
* Den Wert von Feeds verstehen

>[!VIDEO](https://video.tv.adobe.com/v/27695)

### Feed erstellen (6:44) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Einen Feed einrichten
* Welchen Feed-Typ Sie verwenden sollten

>[!VIDEO](https://video.tv.adobe.com/v/27696)
