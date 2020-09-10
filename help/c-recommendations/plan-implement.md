---
keywords: Recommendations;settings;preferences;industry vertical;filter incompatible criteria;default host group;thumb base url;recommendations api token
description: Was Sie vor der Erstellung einer Recommendations-Aktivität wissen müssen.
title: Planen und Implementieren von Recommendations
feature: recommendations general
uuid: 37be7fb3-3686-4dec-9cca-478d28191985
translation-type: tm+mt
source-git-commit: 00749d54d0416c57364ff648bd0911e636c84bc7
workflow-type: tm+mt
source-wordcount: '1592'
ht-degree: 97%

---


# ![PREMIUM](/help/assets/premium.png) -Plan und Umsetzung von Recommendations {#plan-and-implement-recommendations}

Was Sie vor der Erstellung einer Recommendations-Aktivität wissen müssen.

## Planen und Implementieren von Recommendations {#concept_02AA644A4C7D4D5CB1D9CADA208CF8D1}

Was Sie vor der Erstellung einer [!DNL Recommendations]-Aktivität wissen müssen

[!DNL Recommendations] erfordert, dass Sie die folgende Informationshierarchie einrichten:

| Schritt | Informationen | Details |
|--- |--- |--- |
| ![Schritt 1](/help/c-recommendations/assets/step1_red.png) | JavaScript-Bibliothek | Jede der Seiten muss einen Verweis auf at.js, Version 0.9.1 (oder neuer) oder mbox.js, Version 55 (oder neuer) enthalten. Dieser Implementierungsschritt ist auf allen Seiten erforderlich, auf denen eine Target-Aktivität verwendet wird; er kann Schlüssel wie eine Produkt- oder Kategorie-ID umfassen.<BR>Weitere Informationen zu at.js finden Sie unter [at.js-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md).<br>Weitere Informationen zu mbox.js finden Sie unter [Mbox.js-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md). |
| ![Schritt 2](/help/c-recommendations/assets/step2_red.png) | Schlüssel | Der Schlüssel legt den Produkttyp bzw. den Inhaltstyp fest, der in Ihren Empfehlungen angezeigt wird. Zum Beispiel kann der Schlüssel eine Produktkategorie sein. Siehe [Aufbauen der Empfehlung auf einen Empfehlungsschlüssel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). |
| ![Schritt 3](/help/c-recommendations/assets/step3_red.png) | Attribute | Attribute liefern spezifischere Informationen über die Produkte, die Sie anzeigen möchten. Beispielsweise könnte es sein, dass Sie Produkte in einem bestimmten Preisbereich oder Artikel, deren Bestand einen Schwellenwert erreicht, anzeigen möchten. Attribute können in einer Mbox oder durch einen  [Feed](/help/c-recommendations/c-products/feeds.md) bereitgestellt werden.<br>Siehe [[Einschlussregeln](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion)angeben. |
| ![Schritt 4](/help/c-recommendations/assets/step4_red.png) | Ausnahmen | Ausnahmen legen fest, welche spezifischen Artikel nicht in Ihren Empfehlungen angezeigt werden.<br>Siehe [Ausnahmen](/help/c-recommendations/c-products/exclusions.md). |
| ![Schritt 5](/help/c-recommendations/assets/step5_red.png) | Kaufdetails | Kaufdetails enthalten Informationen über die gekauften Artikel und die Reihenfolge und die Bestellung nach Abschluss des Kaufs. |

## Basisimplementierung {#concept_D1154A3FB0FB4467A29AD2BDD21C82D5}

Die Basisimplementierung erfordert, dass Sie Parameter an Ihre Seite weitergeben, die festlegen, welche Produkte oder Seiten in Ihren Empfehlungen angezeigt werden.

Bevor Sie mit der Einrichtung einer [!DNL Recommendations]-Aktivität beginnen, müssen Sie verstehen, wie Ihre Produktdaten an [!DNL Recommendations] übermittelt werden, und entscheiden, welche Methode für Ihren Bedarf am besten geeignet ist.

Es gibt zwei Methoden für die Bereitstellung von Informationen über Produkte und Services an [!DNL Recommendations]:

| Methode | Beschreibung |
|--- |--- |
| Direkte Übermittlung von Parametern an die Seite | Diese Methode eignet sich gut für Elemente, die sich häufig ändern. Da hierfür jedoch die Vornahme von Änderungen direkt an der Seite notwendig ist, erfordert diese Methode in vielen Organisationen die Einbeziehung der IT-Abteilung und der Personen, die Seiten implementieren. |
| Übermittlung von Parametern über einen Google- oder CSV-Feed | Diese Methode eignet sich gut für Sammlungen, die sich selten ändern. Normalerweise ist es nicht notwendig, Ihre Implementierung oder Ihren Seiten-Code zu verändern, um Produktinformationen über ein Feed bereitzustellen. Die Produktliste bleibt jedoch statisch, sodass schnelle Änderungen mit größeren Schwierigkeiten verbunden sind. Weitere Informationen finden Sie unter [Feeds](/help/c-recommendations/c-products/feeds.md). |

Diese Methoden können separat oder gemeinsam wie in den folgenden Beispielen verwendet werden.

## Beispiel 1: Kombinieren von Seite und Feeds  {#section_DF6BAE4BF11548BD9C44D0A426BCF5A7}

Eine übliche Implementierungsoption für [!DNL Recommendations] verwendet sowohl Seitenparameter als auch Feeds.

Diese Methode wird möglicherweise von Einzelhändlern bevorzugt, die über ein relativ stabiles Produktsortiment verfügen, jedoch auf bestimmte Saisonartikel oder reduzierte Artikel hinweisen möchten. Die meisten Kunden stellen ihre Informationen hauptsächlich über den Feed zur Verfügung und passen ihre Seite nur gelegentlich an.

Verwenden Sie einen Feed, um Informationen bereitzustellen, die sich häufig nicht ändern. Verwenden Sie folgende Parameter, unabhängig davon, ob es sich um eine CSV-Datei oder um einen Google-Feed handelt:

* Erforderliche Parameter

   * `entity.id`

* Nützliche Parameter

   * `entity.name`
   * `entity.categoryId`
   * `entity.brand`
   * `entity.pageUrl`
   * `entity.thumbnailUrl`
   * `entity.message`
   * Alle benutzerdefinierten Attribute

Sobald der Feed eingerichtet und an die Seite weitergegeben [!DNL Recommendations]wird, übermitteln Sie Parameter auf der Seite für Attribute, die häufig geändert werden, d. h. häufiger als täglich.

* Erforderliche Parameter

   * `entity.id`
   * `entity.categoryId`

* Nützliche Parameter

   * `entity.inventory`
   * `entity.value`

Priorität erhält jeweils den zuletzt ausgeführten Datensatz. Sollten Sie den Feed zuerst übermitteln und die Seitenparameter anschließend aktualisieren, werden an den Seitenparametern vorgenommene Änderungen angezeigt und die Elementdaten, die vom Feed übermittelt werden, angepasst.

## Beispiel 2: Übermittlung aller Parameter auf der Seite mit Produktdetails (oder Inhaltsdetails){#section_D5A4F69457604CA7AACFD7BFF79B58A9}

Wenn Sie alle Parameter auf der Seite übermitteln, können Sie durch eine Aktualisierung der Seite schnell Updates vornehmen. In einigen Organisationen erfordert dies die Einbeziehung der IT-Abteilung bzw. Ihres Webdesign-Teams.

Dieses Beispiel kann von besonderem Nutzen für Medienunternehmen sein, deren Inhalte sich ständig ändern.

* Erforderliche Parameter

   * `entity.id`
   * `entity.categoryId`
   * Alle sonstigen Attribute

## Beispielcode  {#section_6E8A73376F30468BB549F337C4C220B1}

Sie können beispielsweise den folgenden Code in der Kopfzeile Ihrer Produkt- oder Inhaltsseiten verwenden:

```
function targetPageParams() {
 return {
    "entity": {
       "id": "32323",
       "categoryId": "My Category",
       "value": 105.56,
       "inventory": 329
    }
 }
}
```

Weitere Beispiele des Codes, den Sie auf verschiedenen Seitentypen verwenden können, finden Sie im Abschnitt  [Implementierung nach Seitentyp](../c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC).

## Implementierung nach Seitentyp {#reference_DE38BB07BD3C4511B176CDAB45E126FC}

Seitentypen beeinflussen Ihre Implementierung von [!DNL Recommendations].

Möglicherweise möchten Sie verschiedene Empfehlungstypen für Produktseiten und Kategorieseiten oder die Startseite bereitstellen. Bei jeder Seite können Sie vor dem Mbox-Aufruf spezifische Funktionen ausführen, um die passende Empfehlung anzuzeigen.

Informationen zu den Attributen in den Beispielen finden Sie unter [Entitätsattribute](../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F).

Es ist eine gültige JSON-Formatierung erforderlich.

Die in den Beispielen unten angezeigte Funktion `targetPageParams` ist besonders dann hilfreich, wenn Sie eine Tag-Management-Lösung verwenden, um Ihre Seiten zu implementieren. [!DNL Adobe Launch] oder [!DNL Adobe Dynamic Tag Manager] (DTM) platziert die at.js/mbox.js und die `targetPageParams`-Funktion auf Ihrer Seite und ermöglicht es Ihnen, die Werte zu konfigurieren. Sie müssen diese Funktion entweder vor Ihrem at.js-/mbox.js-Aufruf platzieren oder in den Abschnitt „Extra JavaScript“ Ihrer at.js/mbox.js stellen.

## Alle Seiten {#section_A22061788BAB42BB82BA087DEC3AA4AD}

Sämtliche Seiten, die Empfehlungen enthalten, erfordern auf der Seite einen Verweis auf [!DNL at.js] oder [!DNL mbox.js]. Fügen Sie allen Seiten mit Empfehlungen eines der folgenden Elemente hinzu:

```
<script src="../at.js /></script>
```

```
<script src="../mbox.js /></script>
```

Diese Implementierung erfordert Folgendes:

* [!DNL at.js] Version 0.9.2 (oder höher) oder [!DNL mbox.js] Version 55 (oder höher)

* [!DNL mbox.js] muss den Verweis auf [!DNL target.js] beinhalten ([!DNL at.js] erfordert keinen Verweis auf [!DNL target.js])

Weitere Informationen zur Implementierung [!DNL at.js]finden Sie unter [Bereitstellen von at.js](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md#topic_ECF2D3D1F3384E2386593A582A978556).

Weitere Informationen zur Implementierung von [!DNL mbox.js] finden Sie unter [Mbox.js-Implementierung](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420).

Weitere Informationen zu den Unterschieden zwischen den beiden Target-JavaScript-Bibliotheken finden Sie unter.[Vorteile von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits).

## Kategorieseite {#section_F51A1AAEAC0E4B788582BBE1FEC3ABDC}

Wahrscheinlich möchten Sie Ihre Empfehlungen auf der Kategorieseite auf Produkte und Inhalt innerhalb dieser Kategorie beschränken. Um eine Kategorieseite einzurichten, richten Sie die Schlüssel ein, die von der Seite verwendet werden. Weitere Informationen zu Schlüsseln erhalten Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "My Category" 
      } 
   } 
}
```

## Produktseite {#section_205B3953C9664125A17CA8574FA6B2A3}

Möglicherweise möchten Sie auf einer Produktseite spezifische Artikel oder Artikel mit einem bestimmten Preis bzw. einem bestimmten Bestandsniveau empfehlen. Bei einer Produktseite müssen Sie möglicherweise häufig wechselnde Attribute (wie Wert und Bestand) einstellen, zusätzlich zu den für eine Kategorieseite erforderlichen Schlüsseln.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "My Category", 
         "value": 105.56, 
         "inventory": 329 
      } 
   } 
}
```

## Einkaufswagenseite  {#section_D37E48700F074556B925D0CA0291405E}

Wahrscheinlich möchten Sie auf einer Einkaufswagenseite einige Artikel aus Ihren Empfehlungen ausnehmen, wie zum Beispiel solche Artikel, die bereits im Einkaufswagen sind.

```
<script type="text/javascript">
function targetPageParams() {
   return {
      "excludedIds": [352, 223, 23432, 432, 553]
      }
}
</script>
```

## Danksagungsseite  {#section_C6126A4517A1478693AB7EC2A1D4ACCA}

Möglicherweise möchten Sie auf der Danksagungsseite den Gesamtbetrag und die ID sowie die gekauften Produkte anzeigen, ohne weitere Artikel zu empfehlen. Sie können eine zweite Mbox implementieren, um die Bestellinformationen zu erfassen.

* Lesen Sie bei der Verwendung von at.js  [Konversions-Tracking](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).
* Wenn Sie mbox.js verwenden, lesen Sie [Erstellen einer Mbox für Auftragsbestätigungen - mbox.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md#task_0036D5F6C062442788BB55E872816D82).

## Einstellungen {#concept_C1E1E2351413468692D6C21145EF0B84}

Verwalten Sie Ihre Implementierung von [!DNL Recommendations] mithilfe der Einstellungen.

To access the [!UICONTROL Recommendations Settings] options, open [!DNL Target] in the [!DNL Adobe Experience Cloud], then click **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

![](assets/recs_settings.png)

Die folgenden Optionen sind verfügbar:

| Einstellung | Beschreibung |
|--- |--- |
| Benutzerdefinierte globale Mbox | (Optional) Geben Sie die benutzerdefinierte globale Mbox an, die für [!DNL Target]-Aktivitäten verwendet wird. Standardmäßig wird die globale mbox, die von [!DNL Target] verwendet wird, auch für [!DNL Recommendations] verwendet.<br>Hinweis: Diese Option wird auf der Seite &quot; [!DNL Target] Administration  &quot;festgelegt. Öffnen Sie [!DNL Target]und klicken Sie dann auf [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]. |
| Vertikaler Markt | Der vertikale Markt hilft Ihnen bei der Kategorisierung Ihrer Empfehlungskriterien. Dies hilft Mitgliedern Ihres Teams bei der Suche nach Kriterien, die für eine bestimmte Seite sinnvoll sind, wie zum Beispiel Kriterien, die sich am besten für eine Einkaufswagenseite oder eine Medienseite eignen. |
| Inkompatible Kriterien filtern | Aktivieren Sie diese Option, um nur diejenigen Kriterien anzuzeigen, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für das aktuelle Element/die aktuellen Kategorieempfehlungen übermitteln, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, deaktivieren Sie diese Option.<br>Es wird empfohlen, dass Sie diese Option deaktivieren, wenn Sie eine Tag-Management-Lösung verwenden.<br>Weitere Informationen zu dieser Option finden Sie unter [FAQ zu Empfehlungen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md). |
| Standard-Hostgruppe | Wählen Sie Ihre Standard-Hostgruppe aus.<br>Die Hostgruppe kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungen zu trennen. Sie können beispielsweise Hostgruppen für Entwicklungs- und Produktionsumgebungen, unterschiedliche Marken oder unterschiedliche Länder verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben. Bereitgestellte Empfehlungen hängen von der in der Anforderung angegebenen Hostgruppe ab.<br>Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.<br>**Hinweis:** Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.<br>Der [!UICONTROL Umgebungs]-Filter ist an den folgenden Stellen in der [!DNL Target]-Benutzeroberfläche verfügbar:<ul><li>Katalogsuche (Recommendations > Katalogsuche)</li><li>Dialogfeld „Sammlung erstellen“ ([!UICONTROL Recommendations > Sammlungen > Neu erstellen])</li><li>Dialogfeld „Sammlung aktualisieren“ ([!UICONTROL Recommendations > Sammlungen > Bearbeiten])</li><li>Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations > Ausschlüsse > Neu erstellen])</li><li>Ausschlussdialogfeld aktualisieren ([!UICONTROL Empfehlungen > Ausnahmen > Bearbeiten])</li></ul>Weitere Informationen finden Sie unter [Hosts](/help/administrating-target/hosts.md). |
| Miniaturansicht Basis-URL | Durch Festlegen einer Basis-URL für Ihren Produktkatalog können Sie relative URLs verwenden, wenn Sie beim Ausfüllen Ihrer URL Miniaturen Ihrer Produkte angeben.<br>Beispiel: <br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br> legt eine URL relativ zur Basis-URL der Miniaturansicht fest. |
| Recommendations-API-Token | Verwenden Sie diesen Token in Recommendations-API-Aufrufen, zum Beispiel der Download-API. |
