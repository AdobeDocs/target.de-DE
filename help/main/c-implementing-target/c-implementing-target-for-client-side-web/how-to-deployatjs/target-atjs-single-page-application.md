---
keywords: Implementierung von Einzelseitenanwendungen;Implementieren von Einzelseitenanwendungen;SPA;at.js 2.x;at.js;Einzelseitenanwendung;Einzelseitenanwendung;SPA;SPA
description: Erfahren Sie, wie Sie Adobe verwenden [!DNL Target] at.js 2.x zur Implementierung [!DNL Target] für Einzelseiten-Apps (SPA).
title: Kann ich implementieren [!DNL Target] für Einzelseiten-Apps (SPA)?
feature: Implement Server-side
role: Developer
exl-id: 624f8e62-b443-4093-8e05-9320a365ea07
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '2764'
ht-degree: 70%

---

# Implementieren von Einzelseiten-Apps

Herkömmliche Websites arbeiteten auf Basis von Page-to-Page-Navigationsmodellen (auch als Multi-Page-Anwendungen bekannt), bei denen Website-Designs eng an URLs gekoppelt waren und Übergänge von einer Webseite zu einer anderen einen Seitenladevorgang benötigten. Moderne Webanwendungen wie z. B. Einzelseiten-Apps (SPAs) nutzen stattdessen ein Modell, das die Rendering-Funktion der Browseroberfläche beschleunigt, wodurch oft keine Neuladungen der Seite erforderlich sind. Diese Erlebnisse werden oft durch Kundeninteraktionen wie Bildläufe, Klicks und Cursorbewegungen ausgelöst. Mit der Entwicklung neuer Ideen im modernen Web hat sich auch die Relevanz herkömmlicher allgemeiner Ereignisse (z. B. das Laden der Seite) zur Implementierung von Personalisierung und Experimenten verringert.

![Herkömmlicher Seitenlebenszyklus und SPA-Lebenszyklus](/help/main/c-experiences/assets/trad-vs-spa.png)

at.js 2.x bietet umfassende Funktionen, mit denen Ihr Unternehmen mithilfe von Client-seitigen Technologien der neuesten Generation Personalisierungen ausführen kann. Diese Version konzentriert sich auf die Verbesserung von at.js, um harmonische Interaktionen mit SPAs zu ermöglichen.

Hier einige Vorteile der Verwendung von at.js 2.x, die in früheren Versionen nicht verfügbar sind:

* Möglichkeit zur Zwischenspeicherung aller Angebote beim Seitenladen, um mehrere Server-Aufrufe auf einen einzelnen Server-Aufruf zu reduzieren
* Drastische Verbesserung der Erlebnisse Ihrer Endbenutzer auf Ihrer Site, da Angebote sofort über den Cache angezeigt werden, ohne dass durch herkömmliche Server-Aufrufe Latenz entsteht
* Einfache Einrichtung mit einmaliger, einzeiliger Codeeingabe und Entwicklerunterstützung, sodass Ihre Marketing-Experten A/B- und Erlebnis-Targeting(XT)-Aktivitäten über VEC in Ihrer SPA erstellen und ausführen können

## Adobe [!DNL Target] Ansichten und Einzelseiten-Apps

Adobe Target VEC für SPAs basiert auf einem neuen Konzept für Ansichten: Eine Ansicht entspricht einer logischen Gruppe visueller Elemente, aus denen sich ein SPA-Erlebnis zusammensetzt. Eine SPA kann also als eine Reihe von Ansichten anstelle von URLs betrachtet werden, die je nach Benutzerinteraktion aufgerufen werden. Eine Ansicht umfasst in der Regel eine ganze Site oder eine Gruppe visueller Elemente innerhalb einer Site.

Um Ansichten genauer erklären zu können, navigieren wir einmal über diese fiktive E-Commerce-Site, die in React implementiert wurde, und betrachten einige Beispielansichten. Klicken Sie auf die folgenden Links, um diese Website auf einer neuen Browser-Registerkarte zu öffnen.

**Link: [Startseite](https://target.enablementadobe.com/react/demo/#/)**

![Homepage](/help/main/c-experiences/assets/home.png)

Wenn wir zur Homepage navigieren, können wir sofort ein Hero-Bild sehen, das einen Osterverkauf bewirbt, sowie die neuesten Produkte, die auf der Site verkauft werden. In diesem Fall kann die gesamte Homepage als Ansicht definiert werden. Dies sollten Sie im Hinterkopf behalten, da wir darauf im Abschnitt „Implementieren von Adobe Target-Ansichten“ unten näher eingehen werden.

**Link: [Produktseite](https://target.enablementadobe.com/react/demo/#/products)**

![Produktseite](/help/main/c-experiences/assets/product-site.png)

Da uns die Produkte dieses Unternehmens interessieren, klicken wir auf den Link zu den Produkten. Ähnlich wie die Homepage kann die gesamte Produktseite als Ansicht definiert werden. Wir können diese Ansicht „Produkte“ nennen, genau wie der Pfadname in `https://target.enablementadobe.com/react/demo/#/products)`.

![Produktseite 2](/help/main/c-experiences/assets/product-site-2.png)

Am Anfang dieses Abschnitts haben wir Ansichten als ganze Site oder sogar als eine Gruppe visueller Elemente auf der Site definiert. Wie oben gezeigt, können die vier auf der Site angezeigten Produkte auch gruppiert und als Ansicht betrachtet werden. Als Name für diese Ansicht käme „Produkte“ in Frage.

![Produktseite 3](/help/main/c-experiences/assets/product-site-3.png)

Klicken Sie auf die Schaltfläche „Mehr laden“, um weitere Produkte auf der Site zu erkunden. In diesem Fall ändert sich die Website-URL nicht. Hier kann auch nur die zweite Zeile der oben gezeigten Produkte als Ansicht angesehen werden. Der Name der Ansicht könnte also „PRODUKTSEITE-2“ lauten.

**Link: [Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

![Checkout-Seite](/help/main/c-experiences/assets/checkout.png)

Da uns einige Produkte auf der Site gefallen haben, beschließen wir, ein paar zu kaufen. Auf der Checkout-Site erhalten wir die Möglichkeit, zwischen dem normalen Versand oder der Expresszustellung zu wählen. Da eine beliebige Gruppe visueller Elemente auf einer Site als Ansicht definiert werden kann, können wir diese Ansicht „Versand-Voreinstellungen“ nennen.

Das Konzept Ansichten aber kann noch viel mehr ausgeweitet werden. Für Marketing-Experten, die den Inhalt einer Site je nach Versandpräferenz personalisieren möchten, gibt es die Möglichkeit, eine Ansicht für jede Versandpräferenz zu erstellen. Wenn wir in diesem Fall den normalen Versand auswählen, kann die Ansicht „Normaler Versand“ heißen. Wenn die Expresszustellung ausgewählt wird, kann die Ansicht „Expresszustellung“ lauten.

Ihre Marketing-Experten können auch einen A/B-Test durchführen, um zu sehen, ob die Änderung der Farbe von Blau auf Rot nach Auswahl der Expresszustellung die Konversion im Vergleich zu gleichbleibend blauer Button-Farbe für beide Versandoptionen steigert.

## Implementieren von Adobe [!DNL Target] Ansichten

Nachdem wir nun erklärt haben, was Adobe Target-Ansichten sind, können wir dieses Konzept in Target nutzen, um Marketern die Möglichkeit zu geben, mithilfe des VEC A/B- und XT-Tests in SPAs durchzuführen. Dies erfordert eine einmalige Einrichtung durch den Entwickler. Nachfolgend sind die Schritte beschrieben, die sie dazu befolgen müssen.

1. Installieren Sie at.js 2.x.

   Zunächst müssen Sie at.js 2.x installieren. Diese Version von at.js wurde speziell für SPAs entwickelt. Frühere Versionen von at.js und mbox.js (jetzt nicht mehr unterstützt) unterstützen keine Adobe Target-Ansichten und VEC für SPA.

   Laden Sie at.js 2.x über die Adobe Target-Benutzeroberfläche unter herunter. [!UICONTROL Administration > Implementierung]. at.js 2.x kann auch über Tags in bereitgestellt werden. [!DNL Adobe Experience Platform].

1. Implementieren Sie die neueste at.js 2.x-Funktion `triggerView()` auf Ihren Sites.

   Nachdem Sie die Ansichten Ihrer SPA, in denen Sie einen A/B- oder XT-Test durchführen möchten, definiert haben, implementieren Sie die `triggerView()`-Funktion von at.js 2.x und übergeben Sie die Ansichten als Parameter. Dadurch können Marketing-Experten VEC zum Entwerfen und Ausführen der A/B- und XT-Tests für diese Ansichten verwenden. Wenn die `triggerView()`-Funktion für diese Ansichten nicht definiert wurde, erkennt VEC die Ansichten nicht, sodass Marketing-Experten den VEC nicht zum Entwerfen und Ausführen von A/B- und XT-Tests verwenden können.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Typ | Erforderlich? | Validierung | Beschreibung |
   | --- | --- | --- | --- | --- |
   | viewName | Zeichenfolge | Ja | 1. Keine nachfolgenden Leerzeichen.<br>2. Darf nicht leer sein.<br>3. Der Name der Ansicht sollte für alle Seiten eindeutig sein.<br>4. **Warnung:** Der Anzeigename sollte nicht mit „`/`“ beginnen oder enden. Dies liegt daran, dass der Kunde den Anzeigenamen im Allgemeinen aus dem URL-Pfad entnimmt. Für uns sind „home“ und „`/home`“ unterschiedlich.<br>5. **Warnung:** Dieselbe Ansicht sollte nicht mehrmals hintereinander mit der Option `{page: true}` ausgelöst werden. | Geben Sie eine beliebige Zeichenfolge als Namen für Ihre Ansicht an. Der Name dieser Ansicht wird im Bedienfeld [!UICONTROL Änderungen] von VEC angezeigt, sodass Marketing-Experten Aktionen erstellen und ihre A/B- und XT-Aktivitäten ausführen können. |
   | options | Objekt | Nein |  |  |
   | Optionen > Seite | Boolesch | Nein |  | **TRUE**: Der Standardwert der Seite ist „wahr“. Bei `page=true` werden Benachrichtigungen zur Erhöhung der Impressions-Anzahl an die Edge-Server gesendet.<br>**FALSE**: Bei `page=false` werden keine Benachrichtigungen zur Erhöhung der Impressions-Anzahl gesendet. Dies sollte verwendet werden, wenn Sie nur eine Komponente auf einer Seite mit einem Angebot neu rendern möchten. |

   Im Folgenden sehen wir einige beispielhafte Anwendungsfälle dazu, wie Sie in React die `triggerView()`-Funktion für unsere fiktive E-Commerce-SPA aufrufen:

   **Link: [Startseite](https://target.enablementadobe.com/react/demo/#/)**

   ![Home-React-1](/help/main/c-experiences/assets/react1.png)

   Wenn wir als Marketer A/B-Tests auf der gesamten Homepage durchführen möchten, bietet es sich an, die Ansicht „Home“ zu nennen:

```
 function targetView() {
   var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash

   viewName = viewName || 'home'; // view name cannot be empty

   // Sanitize viewName to get rid of any trailing symbols derived from URL
   if (viewName.startsWith('#') || viewName.startsWith('/')) {
     viewName = viewName.substr(1);
   }

   // Validate if the Target Libraries are available on your website
   if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
     adobe.target.triggerView(viewName);
   }
 }

 // react router v4
 const history = syncHistoryWithStore(createBrowserHistory(), store);
 history.listen(targetView);

 // react router v3
 <Router history={hashHistory} onUpdate={targetView} >
```

**Link: [Produktseite](https://target.enablementadobe.com/react/demo/#/products)**

Schauen wir uns nun ein Beispiel an, das etwas komplizierter ist. Nehmen wir als Marketing-Experten an, wir möchten die zweite Reihe der Produkte personalisieren, indem wir die Farbe der Preisbeschriftung auf Rot ändern, nachdem ein Benutzer auf die Schaltfläche „Mehr laden“ geklickt hat.

![React-Produkte](/help/main/c-experiences/assets/react4.png)

```
 function targetView(viewName) {
   // Validate if the Target Libraries are available on your website
   if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
     adobe.target.triggerView(viewName);
   }
 }

 class Products extends Component {
   render() {
     return (
       <button type="button" onClick={this.handleLoadMoreClicked}>Load more</button>
     );
   }

   handleLoadMoreClicked() {
     var page = this.state.page + 1; // assuming page number is derived from component’s state
     this.setState({page: page});
     targetView('PRODUCTS-PAGE-' + page);
   }
 }
```

**Link: [Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

![React-Checkout](/help/main/c-experiences/assets/react6.png)

Für Marketing-Experten, die den Inhalt einer Site je nach Versandpräferenz personalisieren möchten, gibt es die Möglichkeit, eine Ansicht für jede Versandpräferenz zu erstellen. Wenn wir in diesem Fall den normalen Versand auswählen, kann die Ansicht „Normaler Versand“ heißen. Wenn die Expresszustellung ausgewählt wird, kann die Ansicht „Expresszustellung“ lauten.

Ihre Marketing-Experten können auch einen A/B-Test durchführen, um zu sehen, ob die Änderung der Farbe von Blau auf Rot nach Auswahl der Expresszustellung die Konversion im Vergleich zu gleichbleibend blauer Button-Farbe für beide Versandoptionen steigert.

```
 function targetView(viewName) {
   // Validate if the Target Libraries are available on your website
   if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
     adobe.target.triggerView(viewName);
   }
 }

 class Checkout extends Component {
   render() {
     return (
       <div onChange={this.onDeliveryPreferenceChanged}>
         <label>
           <input type="radio" id="normal" name="deliveryPreference" value={"Normal Delivery"} defaultChecked={true}/>
           <span> Normal Delivery (7-10 business days)</span>
         </label>

         <label>
           <input type="radio" id="express" name="deliveryPreference" value={"Express Delivery"}/>
           <span> Express Delivery* (2-3 business days)</span>
         </label>
       </div>
     );
   }
   onDeliveryPreferenceChanged(evt) {
     var selectedPreferenceValue = evt.target.value;
     targetView(selectedPreferenceValue);
   }
 }
```

## Systemdiagramme in at.js 2.x

Die folgenden Diagramme helfen Ihnen dabei, den Arbeitsablauf von at.js 2.x mit Ansichten zu verstehen und wie dieser die Integration der SPAs verbessert. Eine bessere Einführung in die in at.js 2.x verwendeten Konzepte finden Sie unter [Implementieren von Einzelseiten-Apps](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Ablauf mit at.js 2.x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Schritt | Details |
| --- | --- |
| 1 | Ein Aufruf gibt die [!DNL Experience Cloud ID] zurück, falls sich der Benutzer authentifiziert hat. Bei einem weiteren Aufruf wird die Kunden-ID synchronisiert. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>at.js kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert wird. |
| 3 | Es wird eine Seitenlade-Anfrage durchgeführt, in der alle konfigurierten Parameter (MCID, SDID und Kunden-ID) enthalten sind. |
| 4 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist. Der Speicher ruft geeignete Zielgruppen aus der Zielgruppenbibliothek ab (beispielsweise über Adobe Analytics, Zielgruppen-Management etc. bereitgestellte Zielgruppen).<br>Kundenattribute werden in einem Batch-Prozess an den Profilspeicher übermittelt. |
| 5 | Basierend auf den URL-Anfrageparametern und den Profildaten entscheidet [!DNL Target], welche Aktivitäten und Erlebnisse für die aktuelle Seite und zukünftige Ansichten an den Besucher zurückgegeben werden sollen. |
| 6 | Zielgerichteter Inhalt wird zurück an die Seite übermittelt. Dieser enthält optional Profilwerte für eine weitere Personalisierung.<br>Die zielgerichteten Inhalte auf der aktuellen Seite werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern.<br>Zielgerichtete Inhalte für Ansichten, die als Ergebnis von Benutzeraktionen in einer SPA, die im Browser zwischengespeichert wird, angezeigt werden. Die SPA kann sofort ohne zusätzlichen Serveraufruf angewendet werden, wenn die Ansichten durch `triggerView()` ausgelöst werden. |
| 7 | Analytics-Daten werden an Datenerfassungsserver übermittelt. |
| 8 | Zielgerichtete Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt.<br>Analytics-Daten können dann sowohl in Analytics als auch in Target eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs Analytics for Target (A4T). |

Egal, wo `triggerView()` in Ihrer SPA implementiert ist, werden die Ansichten und Aktionen aus dem Cache abgerufen und dem Benutzer ohne Serveraufruf gezeigt. `triggerView()` sendet außerdem eine Benachrichtigungsanfrage an das [!DNL Target]-Backend, um Impressions-Zählungen zu erhöhen und aufzuzeichnen.

![Target-Ablauf at.js 2.x triggerView](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Schritt | Details |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 3 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den [!DNL Target]-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

## Visual Experience Composer für Einzelseiten-Apps (SPAs)

Nachdem Sie die Installation von at.js 2.x abgeschlossen und `triggerView()` zu Ihrer Site hinzugefügt haben, führen Sie mit dem VEC A/B- und XT-Aktivitäten aus. Weitere Informationen finden Sie unter [Visual Experience Composer für Einzelseiten-Apps (SPAs)](/help/main/c-experiences/spa-visual-experience-composer.md).

>[!NOTE]
>
>VEC für SPAs ist eigentlich derselbe VEC, den Sie auch auf normalen Webseiten verwenden. Es sind jedoch einige zusätzliche Funktionen verfügbar, wenn Sie eine Einzelseiten-App öffnen, bei der `triggerView()` implementiert ist.

## Verwenden Sie TriggerView, um sicherzustellen, dass A4T richtig mit at.js 2.x und SPAs funktioniert.  {#triggerview}

Um sicherzustellen, dass [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) ordnungsgemäß mit at.js 2.x arbeitet, müssen Sie dieselbe SDID in der Target-Anforderung und in der Analytics-Anforderung senden.

Best Practices in Bezug auf SPAs:

* Verwenden Sie benutzerspezifische Ereignisse für Benachrichtigungen, wenn in der Anwendung interessante Ereignisse auftreten.
* Auslösen eines benutzerspezifischen Ereignisses vor dem Start der Ansicht
* Auslösen eines benutzerspezifischen Ereignisses, wenn die Anzeige abgeschlossen wird

Zu at.js 2.x wurde eine neue API[-TriggerView ()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)-Funktion hinzugefügt. Sie sollten at.js `triggerView()` darüber informieren, dass eine Ansicht beginnt.

Um zu sehen, wie benutzerspezifische Ereignisse kombiniert werden, sehen wir uns in at.js 2.x und Analytics ein Beispiel an. In diesem Beispiel wird davon ausgegangen, dass die HTML-Seite die Besucher-API gefolgt von at.js 2.x und AppMeasurement enthält.

Nehmen wir an, dass die folgenden benutzerspezifischen Ereignisse vorhanden sind:

* `at-view-start` - Wenn die Ansicht beginnt
* `at-view-end` - Wenn die Ansicht abgeschlossen wird

Um sicherzustellen, dass A4T mit at.js 2.x arbeitet, vergewissern Sie sich von Folgendem:

Der Starthandler für die Ansicht sollte wie folgt aussehen:

```
document.addEventListener("at-view-start", function(e) {
  var visitor = Visitor.getInstance("<your Adobe Org ID>");
  
  visitor.resetState();
  adobe.target.triggerView("<view name>");
});
```

Der Endhandler für die Ansicht sollte etwa wie folgt aussehen:

```
document.addEventListener("at-view-end", function(e) {
  // s - is the AppMeasurement tracker object
  s.t();
});
```

>[!NOTE]
>
>Sie müssen die Ereignisse `at-view-start` und `at-view-end` auslösen. Diese Ereignisse sind nicht Teil von benutzerspezifischen at.js-Ereignissen.

Obwohl diese Beispiele JavaScript-Code verwenden, kann all dies vereinfacht werden, wenn Sie einen Tag-Manager verwenden, z. B. Tags in [Adobe Experience Platform](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

Wenn die vorhergehenden Schritte eingehalten werden, sollten Sie eine robuste A4T-Lösung für SPAs haben.

## Best Practices bei der Implementierung {#bp}

Mit at.js 2.x-APIs können Sie Ihre [!DNL Target] -Implementierung in vielerlei Hinsicht, es ist jedoch wichtig, während dieses Prozesses die richtige Reihenfolge der Vorgänge zu befolgen.

Die folgenden Informationen beschreiben die Reihenfolge der Vorgänge, die Sie beim erstmaligen Laden einer Einzelseiten-App in einem Browser ausführen müssen, sowie für alle nachfolgenden Ansichtsänderungen.

### Reihenfolge der Vorgänge beim ersten Laden der Seite

| Schritt | Aktion | Details |
| --- | --- | --- |
| 1 | Laden von VisitorAPI-JS | Diese Bibliothek ist für die Zuweisung einer ECID an den Besucher verantwortlich. Diese ID wird später von anderen verwendet [!DNL Adobe] -Lösungen auf der Web-Seite. |
| 2 | at.js 2.x laden | at.js 2.x lädt alle erforderlichen APIs, die Sie zur Implementierung verwenden [!DNL Target] Anfragen und Ansichten. |
| 3 | Ausführen [!DNL Target] Anfrage | Wenn Sie über eine Datenschicht verfügen, empfehlen wir, kritische Daten zu laden, die an gesendet werden müssen [!DNL Target] vor dem Ausführen einer [!DNL Target] -Anfrage. Auf diese Weise können Sie `targetPageParams` zum Senden aller Daten, die Sie für die Zielgruppenbestimmung verwenden möchten. Sie müssen sicherstellen, dass Sie in diesem API-Aufruf &quot;Ausführen > pageLoad&quot;sowie &quot;Vorabruf > Ansichten&quot;anfordern. wenn Sie `pageLoadEnabled` und `viewsEnabled`, dann erfolgt sowohl &quot;Ausführen&quot;> &quot;pageLoad&quot;als auch &quot;Vorab abrufen&quot;> Ansichten automatisch in Schritt 2. andernfalls müssen Sie die `getOffers()` API, um diese Anfrage zu stellen. |
| 4 | Aufruf `triggerView()` | Da die [!DNL Target] -Anfrage, die Sie in Schritt 3 initiiert haben, kann Erlebnisse sowohl für die Seitenladeausführung als auch für Ansichten zurückgeben, stellen Sie sicher, dass `triggerView()` wird nach der [!DNL Target] -Anfrage wird zurückgegeben und die Anwendung der Angebote auf den Cache wird abgeschlossen. Sie müssen diesen Schritt nur einmal pro Ansicht ausführen. |
| 5 | Rufen Sie die [!DNL Analytics] Seitenansichts-Beacon | Dieses Beacon sendet die mit den Schritten 3 und 4 verknüpfte SDID an [!DNL Analytics] für die Datenzuordnung. |
| 6 | Aufrufen zusätzlicher `triggerView({"page": false})` | Dies ist ein optionaler Schritt für SPA Frameworks, die bestimmte Komponenten auf der Seite potenziell erneut rendern können, ohne dass eine Änderung der Ansicht stattfindet. In solchen Fällen ist es wichtig, dass Sie diese API aufrufen, um sicherzustellen, dass [!DNL Target] Erlebnisse werden erneut angewendet, nachdem das SPA Framework die Komponenten erneut gerendert hat. Sie können diesen Schritt so oft ausführen, wie Sie sicherstellen möchten, dass [!DNL Target] Erlebnisse in Ihren SPA-Ansichten beibehalten. |

### Reihenfolge der Vorgänge für SPA Änderung der Ansicht (kein vollständiges Neuladen der Seite)

| Schritt | Aktion | Details |
| --- | --- | --- |
| 1 | Aufruf `visitor.resetState()` | Diese API stellt sicher, dass die SDID für die neue Ansicht beim Laden neu generiert wird. |
| 2 | Aktualisieren Sie den Cache, indem Sie `getOffers()` API | Dies ist ein optionaler Schritt, der durchgeführt werden kann, wenn diese Ansichtsänderung das Potenzial hat, den aktuellen Besucher für mehr zu qualifizieren. [!DNL Target] Aktivitäten oder die Deaktivierung dieser Aktivitäten. An dieser Stelle können Sie auch zusätzliche Daten an senden [!DNL Target] zur Aktivierung weiterer Targeting-Funktionen. |
| 3 | Aufruf `triggerView()` | Wenn Sie Schritt 2 ausgeführt haben, müssen Sie auf die [!DNL Target] -Anfrage an und wenden Sie die Angebote auf den Cache an, bevor Sie diesen Schritt ausführen. Sie müssen diesen Schritt nur einmal pro Ansicht ausführen. |
| 4 | Aufruf `triggerView()` | Wenn Sie Schritt 2 nicht ausgeführt haben, können Sie diesen Schritt ausführen, sobald Sie Schritt 1 abgeschlossen haben. Wenn Sie Schritt 2 und Schritt 3 ausgeführt haben, sollten Sie diesen Schritt überspringen. Sie müssen diesen Schritt nur einmal pro Ansicht ausführen. |
| 5 | Rufen Sie die [!DNL Analytics] Seitenansichts-Beacon | Dieses Beacon sendet die mit den Schritten 2, 3 und 4 verknüpfte SDID an [!DNL Analytics] für die Datenzuordnung. |
| 6 | Aufrufen zusätzlicher `triggerView({"page": false})` | Dies ist ein optionaler Schritt für SPA Frameworks, die bestimmte Komponenten auf der Seite potenziell erneut rendern können, ohne dass eine Änderung der Ansicht stattfindet. In solchen Fällen ist es wichtig, dass Sie diese API aufrufen, um sicherzustellen, dass [!DNL Target] Erlebnisse werden erneut angewendet, nachdem das SPA Framework die Komponenten erneut gerendert hat. Sie können diesen Schritt so oft ausführen, wie Sie sicherstellen möchten, dass [!DNL Target] Erlebnisse in Ihren SPA-Ansichten beibehalten. |

## Schulungsvideos

Weitere Informationen dazu finden Sie in den folgenden Videos:

### Funktionsweise von at.js 2.x ![Übersichtszeichen](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Siehe [Funktionsweise von at.js 2.x](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) für weitere Informationen.

### Implementieren von at.js 2.x in eine SPA ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/26248)

Siehe [Implementieren von Adobe Target at.js 2.x in eine Einzelseiten-App (SPA)](https://helpx.adobe.com/target/kt/using/atjs2-single-page-application-technical-video-implement.html) für weitere Informationen.

### Verwenden von VEC für SPA in Adobe Target ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Siehe [Verwenden von Visual Experience Composer für Einzelseiten-Apps (SPA VEC) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) für weitere Informationen.