---
description: Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs) ermöglicht es Marketing-Experten, für SPAs selbst Tests zu erstellen und Inhalt zu personalisieren, ohne von der kontinuierlichen Weiterentwicklung abhängig zu sein. Mit VEC können Aktivitäten auf Basis der beliebtesten Frameworks erstellt werden, beispielsweise mit React oder Angular.
keywords: SPA VEC;React;Angular;react.js;SPA Visual Experience Composer;Optionen in SPA Experience Composer;Einzelseiten-App;Single-Page-App;SPA;Optionen für mobile Erlebnisse;Target-Ansicht
seo-description: Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs) in Adobe Target ermöglicht es Marketing-Experten, für SPAs selbst Tests zu erstellen und Inhalt zu personalisieren, ohne von der kontinuierlichen Weiterentwicklung abhängig zu sein. Mit VEC können Aktivitäten auf Basis der beliebtesten Frameworks erstellt werden, beispielsweise mit React oder Angular.
seo-title: Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)
solution: Target
title: Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)
topic: Standard
uuid: 4dcd6d9c-b2e3-4759-a2e0-3696c572faba
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs){#single-page-app-spa-visual-experience-composer}

In [!DNL Adobe Target] bietet [!UICONTROL Visual Experience Composer] (VEC) Marketing-Experten die Möglichkeit, selbst Aktivitäten zu erstellen und Erlebnisse zu personalisieren, die über die globale Mbox von Adobe Target dynamisch für herkömmliche Multi-Page-Apps bereitgestellt werden können. Dies beruht jedoch darauf, Angebote beim Laden der Seite oder über nachfolgende Serveraufrufe abzurufen, wodurch wie im Diagramm unten dargestellt Latenzzeiten entstehen. Dieser Ansatz funktioniert nicht gut mit Einzelseiten-Apps (SPAs), da dadurch die Benutzererfahrung und die Anwendungsleistung beeinträchtigt werden.

![Herkömmlicher Lebenszyklus und SPA-Lebenszyklus](/help/c-experiences/assets/trad-vs-spa.png)

Mit der neuesten Version bieten wir nun VEC für SPAs an. VEC für SPAs ermöglicht es Marketing-Experten, für SPAs selbst Tests zu erstellen und Inhalt zu personalisieren, ohne von der kontinuierlichen Weiterentwicklung abhängig zu sein. Mit VEC können Sie [A/B-Test](/help/c-activities/t-test-ab/test-ab.md)- und [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md)-Aktivitäten (XT-Aktivitäten) in beliebten Frameworks wie React und Angular erstellen.

## Adobe Target-Ansichten und Einzelseiten-Apps

Adobe Target VEC für SPAs basiert auf einem neuen Konzept für Ansichten: Eine Ansicht entspricht einer logischen Gruppe visueller Elemente, aus denen sich ein SPA-Erlebnis zusammensetzt. Eine SPA kann also als eine Reihe von Ansichten anstelle von URLs betrachtet werden, die je nach Benutzerinteraktion aufgerufen werden. Eine Ansicht umfasst in der Regel eine ganze Site oder eine Gruppe visueller Elemente innerhalb einer Site.

Um Ansichten genauer erklären zu können, navigieren wir einmal über diese fiktive E-Commerce-Site, die in React implementiert wurde, und betrachten einige Beispielansichten. Klicken Sie auf die folgenden Links, um diese Website auf einer neuen Browser-Registerkarte zu öffnen.

**Link:[Homepage](https://target.enablementadobe.com/react/demo/#/)**

![Homepage](/help/c-experiences/assets/home.png)

Wenn wir zur Homepage navigieren, können wir sofort ein Hero-Bild sehen, das einen Osterverkauf bewirbt, sowie die neuesten Produkte, die auf der Site verkauft werden. In diesem Fall kann die gesamte Homepage als Ansicht definiert werden. Dies sollten Sie im Hinterkopf behalten, da wir darauf im Abschnitt „Implementieren von Adobe Target-Ansichten“ unten näher eingehen werden.

**Link:[Produktseite](https://target.enablementadobe.com/react/demo/#/products)**

![Produktseite](/help/c-experiences/assets/product-site.png)

Da uns die Produkte interessieren, klicken wir auf den Link zu den Produkten. Ähnlich wie die Homepage kann die gesamte Produktseite als Ansicht definiert werden. Wir können diese Ansicht „Produkte“ nennen, genau wie der Pfadname in `https://target.enablementadobe.com/react/demo/#/products`.

![Produktseite 2](/help/c-experiences/assets/product-site-2.png)

Am Anfang dieses Abschnitts haben wir Ansichten als ganze Site oder sogar als eine Gruppe visueller Elemente auf der Site definiert. Wie oben gezeigt, können die vier auf der Site angezeigten Produkte auch gruppiert und als Ansicht betrachtet werden. Als Name für diese Ansicht käme „Produkte“ in Frage.

![Produktseite 3](/help/c-experiences/assets/product-site-3.png)

Klicken Sie auf die Schaltfläche „Mehr laden“, um weitere Produkte auf der Site zu erkunden. In diesem Fall ändert sich die Website-URL nicht. Hier kann auch nur die zweite Zeile der oben gezeigten Produkte als Ansicht angesehen werden. Der Name der Ansicht könnte also „PRODUKTSEITE-2“ lauten.

**Link:[Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

![Checkout-Seite](/help/c-experiences/assets/checkout.png)

Da uns einige Produkte auf der Site gefallen haben, beschließen wir, ein paar zu kaufen. Auf der Checkout-Site erhalten wir die Möglichkeit, zwischen dem normalen Versand oder der Expresszustellung zu wählen. Da eine beliebige Gruppe visueller Elemente auf einer Site als Ansicht definiert werden kann, können wir diese Ansicht „Versand-Voreinstellungen“ nennen.

Das Konzept Ansichten aber kann noch viel mehr ausgeweitet werden. Für Marketing-Experten, die den Inhalt einer Site je nach Versandpräferenz personalisieren möchten, gibt es die Möglichkeit, eine Ansicht für jede Versandpräferenz zu erstellen. Wenn wir in diesem Fall den normalen Versand auswählen, kann die Ansicht „Normaler Versand“ heißen. Wenn die Expresszustellung ausgewählt wird, kann die Ansicht „Expresszustellung“ lauten.

Ihre Marketing-Experten können auch einen A/B-Test durchführen, um zu sehen, ob die Änderung der Farbe von Blau auf Rot nach Auswahl der Expresszustellung die Konversion im Vergleich zu gleichbleibend blauer Button-Farbe für beide Versandoptionen steigert.

## Implementieren von Adobe Target-Ansichten

Nachdem wir nun erklärt haben, was Adobe Target-Ansichten sind, können wir dieses Konzept in Target nutzen, um Marketern die Möglichkeit zu geben, mithilfe des VEC A/B- und XT-Tests in SPAs durchzuführen. Dies erfordert eine einmalige Einrichtung durch den Entwickler. Nachfolgend sind die Schritte beschrieben, die sie dazu befolgen müssen.

1. Installieren Sie at.js 2.x.

   Zunächst müssen Sie at.js 2.x installieren. Diese Version von at.js wurde speziell für SPAs entwickelt. Frühere Versionen von at.js und mbox.js unterstützen Adobe Target-Ansichten und VEC für SPA nicht.

   ![Dialogfeld „Implementierungsdetails“](/help/c-experiences/assets/imp-200.png)

   Laden Sie at.js 2.x über die Adobe Target-Benutzeroberfläche unter [!UICONTROL Einrichtung &gt; Implementierung] herunter. at.js 2.x kann auch über [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) bereitgestellt werden. Die Adobe Target-Erweiterungen sind derzeit jedoch nicht aktuell und werden nicht unterstützt.

1. Implementieren Sie die neueste at.js 2.x-Funktion: [triggerView()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) auf Ihren Sites.

   Nachdem Sie die Ansichten Ihrer SPA, in denen Sie einen A/B- oder XT-Test durchführen möchten, definiert haben, implementieren Sie die `triggerView()`-Funktion von at.js 2.x und übergeben Sie die Ansichten als Parameter. Dadurch können Marketing-Experten VEC zum Entwerfen und Ausführen der A/B- und XT-Tests für diese Ansichten verwenden. Wenn die `triggerView()`-Funktion für diese Ansichten nicht definiert wurde, erkennt VEC die Ansichten nicht, sodass Marketing-Experten den VEC nicht zum Entwerfen und Ausführen von A/B- und XT-Tests verwenden können.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Typ | Erforderlich? | Validierung | Beschreibung |
   | --- | --- | --- | --- | --- |
   | viewName | Zeichenfolge | Ja | 1. Keine nachfolgenden Leerzeichen.<br>2. Darf nicht leer sein.<br>3. Der Name der Ansicht sollte für alle Seiten eindeutig sein.<br>4. **Warnung:** Der Anzeigename sollte nicht mit „`/`“ beginnen oder enden. Dies liegt daran, dass der Kunde den Anzeigenamen im Allgemeinen aus dem URL-Pfad entnimmt. Für uns sind „home“ und „`/home`“ unterschiedlich.<br>5. **Warnung:** Dieselbe Ansicht sollte nicht mehrmals hintereinander mit der Option `{page: true}` ausgelöst werden. | Geben Sie eine beliebige Zeichenfolge als Namen für Ihre Ansicht an. Der Name dieser Ansicht wird im Bedienfeld [!UICONTROL Änderungen] von VEC angezeigt, sodass Marketing-Experten Aktionen erstellen und ihre A/B- und XT-Aktivitäten ausführen können. |
   | options | Objekt | Nein |  |  |
   | Optionen &gt; Seite | Boolesch | Nein |  | **TRUE**: Der Standardwert der Seite ist „wahr“. Bei `page=true` werden Benachrichtigungen zur Erhöhung der Impressions-Anzahl an die Edge-Server gesendet.<br>**FALSE**: Bei `page=false` werden keine Benachrichtigungen zur Erhöhung der Impressions-Anzahl gesendet. Dies sollte verwendet werden, wenn Sie nur eine Komponente auf einer Seite mit einem Angebot neu rendern möchten. |

   Im Folgenden sehen wir einige beispielhafte Anwendungsfälle dazu, wie Sie in React die `triggerView()`-Funktion für unsere fiktive E-Commerce-SPA aufrufen:

   **Link:[Homepage](https://target.enablementadobe.com/react/demo/#/)**

   ![Home-React-1](/help/c-experiences/assets/react1.png)

   Wenn wir als Marketer A/B-Tests auf der gesamten Homepage durchführen möchten, bietet es sich an, die Ansicht, die aus der URL entnommen werden kann, „home“ zu nennen.

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

   **Link:[Produkte-Site](https://target.enablementadobe.com/react/demo/#/products)**

   Schauen wir uns nun ein Beispiel an, das etwas komplizierter ist. Nehmen wir als Marketing-Experten an, wir möchten die zweite Reihe der Produkte personalisieren, indem wir die Farbe der Preisbeschriftung auf Rot ändern, nachdem ein Benutzer auf die Schaltfläche „Mehr laden“ geklickt hat.

   ![React-Produkte](/help/c-experiences/assets/react4.png)

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

   **Link:[Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

   ![React-Checkout](/help/c-experiences/assets/react6.png)

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

1. Starten Sie A/B- oder XT-Aktivitäten über VEC.

   Wenn `adobe.target.triggerView()` in Ihrer SPA implementiert wurde und die Namen der Ansichten als Parameter übergeben wurden, kann VEC diese Ansichten erkennen und es Benutzern ermöglichen, Aktionen für und Änderungen an ihren A/B- und XT-Aktivitäten zu erstellen.

   >[!NOTE]
   >
   >VEC für SPAs ist eigentlich derselbe VEC, den Sie auch auf normalen Webseiten verwenden. Es sind jedoch einige zusätzliche Funktionen verfügbar, wenn Sie eine Einzelseiten-App öffnen, bei der `triggerView()` implementiert ist.

Im Bedienfeld [Änderungen](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) und bei den Aktionen für VEC gibt es zwei wesentliche Verbesserungen, mit denen VEC gut mit SPAs funktioniert.

**Bedienfeld „Änderungen“**

Im Bedienfeld [!UICONTROL Änderungen] werden die für eine bestimmte Ansicht erstellten Aktionen erfasst. Beachten Sie, dass alle Aktionen für eine Ansicht unter dieser Ansicht gruppiert werden.

**Aktionen**

Durch Klicken auf eine Aktion wird das Element auf der Sites hervorgehoben, in dem diese Aktion angewendet wird. Jede VEC-Aktion, die unter einer Ansicht erstellt wurde, hat folgende Symbole, wie unten dargestellt: Informationen, Bearbeiten, Klonen, Verschieben und Löschen.

![Änderungen](/help/c-experiences/assets/modifications.png)

Die einzelnen Aktionen sind in der folgenden Tabelle beschrieben:

| Seite | Beschreibung |
| --- | --- |
| Informationen | Zeigt die Details der Aktion an. |
| Bearbeiten | Ermöglicht die direkte Bearbeitung der Eigenschaften dieser Aktion. |
| Klonen | Clone the action to one or more Views that exist on the [!UICONTROL Modifications] panel or to one or more Views that you have browsed and navigated to in the VEC. The action doesn’t have to necessarily exist in the [!UICONTROL Modifications] panel.<br>**Hinweis**: Nachdem ein Klonvorgang durchgeführt wurde, müssen Sie über [!UICONTROL Durchsuchen] zur Ansicht im VEC navigieren, um zu sehen, ob die geklonte Aktion ein gültiger Vorgang war. Wenn die Aktion nicht auf die Ansicht angewendet werden kann, wird ein Fehler angezeigt. |
| Verschieben | Verschiebt die Aktion in ein Seitenladereignis oder eine andere Ansicht, die bereits im Änderungs-Bedienfeld vorhanden ist.<br>[!UICONTROL Seitenladereignis] - Alle Aktionen, die dem Seitenladeereignis entsprechen, werden beim ersten Laden Ihrer Webanwendung angewendet.<br>**Hinweis** : Nachdem Sie einen Verschiebevorgang durchgeführt haben, müssen Sie über Durchsuchen zur Ansicht im VEC navigieren, um zu sehen, ob der Verschiebevorgang ein gültiger Vorgang war. Wenn die Aktion nicht auf die Ansicht angewendet werden kann, wird ein Fehler angezeigt. |
| Löschen | Löscht die Aktion. |

>[!NOTE]
>
>Sie können viele Aktionen ausführen, bevor die Seite im VEC geladen wird, oder auch, wenn die Seite nicht vollständig geladen wird. Aktionen, die nicht bearbeitet werden können, bevor die Website geladen ist, sind in der Benutzeroberfläche von deaktiviert.

**Beispiel 1**

Sehen wir uns das Beispiel oben an, in dem wir eine Home-Ansicht erstellt haben. Für diese Ansicht haben wir dabei zwei Ziele im Auge:

1. Die Farbe der Schaltflächen „Zum Einkaufswagen hinzufügen“ und „Gefällt mir“ in eine hellere blaue Farbe ändern. Dies sollte sich bei „Seite laden“ befinden, da wir Komponenten der Kopfzeile ändern.
1. Die Bezeichnung von „Aktuellste Produkte 2019“ zu „Schärfste Produkte 2019“ und die Textfarbe in Violett ändern.

Um dies auszuführen, klicken Sie im VEC auf [!UICONTROL Erstellen] und wenden Sie diese Änderungen auf die Home-Ansicht an.

![Beispiel 1](/help/c-experiences/assets/example1.png)

**Beispiel 2**

Sehen wir uns das Beispiel oben an, in dem wir die Ansicht PRODUKTSEITE-2 erstellt haben. Unser Ziel ist es, die Bezeichnung „Preis“ in „Verkaufspreis“ und die Farbe in Rot zu ändern.

1. Klicken Sie auf [!UICONTROL Durchsuchen] und dann auf den Link [!UICONTROL Produkte] in der Kopfzeile.
1. Klicken Sie einmal auf [!UICONTROL Mehr laden], um zur zweiten Produktreihe zu gelangen.
1. Klicken Sie auf [!UICONTROL Erstellen].
1. Wenden Sie die Aktionen an, um die Textbeschriftung in „Verkaufspreis“ und die Farbe in Rot zu ändern.

![Beispiel 2](/help/c-experiences/assets/example2.png)

**Beispiel 3**

Schließlich können Ansichten, wie bereits erwähnt, auf granularer Ebene definiert werden. Ansichten können einen Status oder sogar eine Option in einem Optionsfeld sein. Zuvor haben wir die Ansichten CHECKOUT-EXPRESS und CHECKOUT-NORMAL erstellt. Unser Ziel ist es, die Schaltflächenfarbe für die CHECKOUT-EXPRESS-Ansicht in Rot zu ändern.

1. Klicken Sie auf [!UICONTROL Durchsuchen].
1. Fügen Sie dem Warenkorb einige Produkte hinzu.
1. Klicken Sie oben rechts auf das Warenkorbsymbol.
1. Klicken Sie auf „Zur Kasse gehen“.
1. Klicken Sie auf das Optionsfeld „Expresszustellung“.
1. Klicken Sie auf [!UICONTROL Erstellen].
1. Ändern Sie die Schaltfläche von „Bezahlen“ in „Bestellung abschließen“ und die Farbe in Rot.

![Beispiel 3](/help/c-experiences/assets/example3.png)

>[!NOTE]
>
>Die CHECKOUT-EXPRESS-Ansicht wird erst im Bedienfeld „Änderungen“ angezeigt, wenn Sie auf das Optionsfeld „Expresszustellung“ klicken. Dies liegt daran, dass die `triggerView()`-Funktion ausgelöst wird, wenn das Optionsfeld „Expresszustellung“ ausgewählt wird. Dies ist aber nur der Fall, wenn VEC weiß, dass eine Ansicht im Bedienfeld „Änderungen“ angezeigt wird.

## Ein tief gehender Blick auf at.js und SPAs

**Wie kann ich nach dem ersten Laden der Seite in meiner SPA die Ansichten für die neuesten Zielgruppendaten abrufen, die durch Aktionen erfasst wurden?**

Der typische Arbeitsablauf von at.js 2.x beginnt, wenn Ihre Site geladen wird. Alle Ihre Ansichten und Aktionen werden zwischengespeichert, sodass nachfolgende Benutzeraktionen auf Ihrer Site zum Abruf von Angeboten keine Server-Aufrufe auslösen. Wenn Sie Ansichten je nach aktuellsten Benutzeraktionen abrufen möchten, die auf Grundlage der nachfolgenden Benutzeraktionen aktualisiert wurden, können Sie `getOffers()` und `applyOffers()` mit den aktuellsten weitergeleiteten Zielgruppen- und Profildaten aufrufen.

Angenommen, Sie sind ein Telekommunikationsunternehmen und Sie haben eine SPA, die at.js 2.x verwendet. Als Unternehmen möchten Sie die folgenden Ziele erreichen:

* Einem abgemeldeten oder anonymen Benutzer das neueste Angebot ihres Unternehmens, z. B. ein Hero-Angebot „Ein Monat kostenlos“, auf `http://www.telecom.com/home` anzeigen.
* Einem angemeldeten Benutzer, dessen Vertrag ausläuft, ein Upgrade-Angebot zeigen, z. B. „Sie haben Anspruch auf ein kostenloses Telefon!“ auf `http://www.telecom.com/loggedIn/home` anzeigen.

Ihre Entwickler benennen die Ansichten und rufen `triggerView()` wie folgt auf:

* Für `http://www.telecom.com/home` lautet der Ansichtsname „Abgemeldet Home“.
   * `triggerView(“Logged Out Home”)` wird aufgerufen.
* Für `http://www.telecom.com/loggedIn/home` lautet der Ansichtsname „Angemeldet Home“.
   * `triggerView(“Logged In Home”)` wird bei einer Richtungsänderung aufgerufen.

Anschließend führen Ihre Marketing-Experten die folgenden A/B-Aktivitäten über VEC aus:

* A/B-Aktivität mit dem Angebot „Ein Monat kostenlos“ für Zielgruppen mit dem Parameter „`loggedIn= false`“, die bei `http://www.telecom.com/home` angezeigt wird, wobei der Name der Ansicht „Abgemeldet Home“ lautet.
* A/B-Aktivität mit dem Angebot „Sie haben Anspruch auf ein kostenloses Telefon!“ für Zielgruppen mit dem Parameter „`loggedIn=true`“, das bei `http://www.telecom.com/loggedIn/home` angezeigt wird, wobei der Name der Ansicht „Angemeldet Hero-Angebot“ lautet.

Betrachten wir einmal diesen Benutzerablauf:

1. Ein anonymer, abgemeldeter Benutzer landet auf Ihrer Seite.
1. Da Sie at.js 2.x verwenden, geben Sie den Parameter „`loggedIn = false`“ beim Laden der Seite an, um alle in aktiven Aktivitäten vorhandenen Ansichten abzurufen, die für Zielgruppen mit dem Parameter „`loggedIn = false`“ geeignet sind.
1. at.js 2.x ruft dann die Ansicht „Abgemeldet Home“ und die Aktion, die das Angebot „Ein Monat kostenlos“ anzeigt, ab, und speichert sie im Cache.
1. Wenn `triggerView(“Logged Out Home”)` aufgerufen wird, wird das Angebot „Ein Monat kostenlos“ aus dem Cache abgerufen und das Angebot wird ohne einen Serveraufruf angezeigt.
1. Der Benutzer klickt nun auf „Anmelden“ und gibt seine Anmeldeinformationen ein.
1. Da Ihre Website eine SPA ist, wird die Seite nicht komplett geladen, sondern leitet den Benutzer stattdessen zu `http://www.telecom.com/loggedIn/home`.

Hier aber liegt das Problem. Der Benutzer meldet sich an und wir treffen auf `triggerView(“Logged In Home”)`, weil wir diesen Code bei einer Richtungsänderung platziert haben. Diese weist at.js 2.x an, die Ansicht und Aktionen aus dem Cache abzurufen, aber die einzige Ansicht, die im Cache vorhanden ist, ist „Abgemeldet Home“.

Wie können wir also unsere Ansicht „Abgemeldet Home“ abrufen und das Angebot „Sie haben Anspruch auf ein kostenloses Telefon!“ anzeigen? Und da alle nachfolgenden Aktionen auf Ihrer Site aus der Perspektive eines angemeldeten Benutzers stammen, wie können Sie sicherstellen, dass alle nachfolgenden Aktionen zu personalisierten Angeboten für angemeldete Benutzer führen?

Sie können die in at.js 2.x unterstützten neuen Funktionen `getOffers()` und `applyOffers()` verwenden:

```
adobe.target.getOffers({
  request: {
  prefetch: {
    "views": [
      {
        "parameters": {
          "loggedIn": true
        },
      }
    ]
  },
});
```

Übermitteln Sie die Antwort von `getOffers()` und `applyOffers()` und schon werden alle Ansichten und Aktionen, die mit „loggedIn = true“ verknüpft sind, den Cache von at.js aktualisieren.

Mit anderen Worten: at.js 2.x unterstützt eine Methode zum Abrufen von Ansichten, Aktionen und Angeboten mit den aktuellsten Zielgruppendaten auf Anforderung.

**Unterstützt at.js 2.x A4T für Einzelseiten-Apps?**

Ja, at.js 2.x unterstützt A4T für SPA über die `triggerView()`-Funktion, wenn Sie Adobe Analytics und den Experience Cloud-Besucher-ID-Dienst implementiert haben. Siehe Diagramm unten mit schrittweisen Beschreibungen.

![Target-Ablauf](/help/c-experiences/assets/atjs-spa-flow.png)

| Schritt | Beschreibung |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern, die mit der Ansicht zusammenhängen. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 3 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den Target-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

>[!NOTE]
>Wenn Sie keine Benachrichtigungen an Adobe Analytics zur Impressions-Zählung bei jedem Auslösen einer Ansicht senden möchten, geben Sie `{page: false}` an die `triggerView()`-Funktion weiter, damit die Impressions-Zählung nicht erhöht wird, wenn eine Ansicht mehrmals für eine Komponente ausgelöst wird, die regelmäßig erneut gerendert wird. Beispiel:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## Unterstützte Aktivitäten

| Aktivitätstyp | Unterstützt? |
| --- | --- |
| [A/B-Test](/help/c-activities/t-test-ab/test-ab.md) | Ja |
| [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md)<br>bei A/B-Test- und Erlebnis-Targeting(XT)-Aktivitäten | Ja |
| [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja |
| [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Nein |
| [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md) | Nein |
| [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) | Nein |
| [Recommendations](/help/c-recommendations/recommendations.md) | Nein |

**Wie führen wir, wenn wir at.js 2.x installiert und`triggerView()`auf unseren Sites implementiert haben, A/B-Aktivitäten mit automatischem Targeting aus, da SPA VEC das automatische Targeting nicht unterstützt?**

Wenn Sie A/B-Aktivitäten mit automatischem Targeting verwenden möchten, können Sie alle Aktionen so verschieben, dass sie in VEC beim Laden der Seite ausgeführt werden. Bewegen Sie den Mauszeiger über die einzelnen Aktionen und klicken Sie auf die Schaltfläche [!UICONTROL Verschieben nach „Seite laden“]. Anschließend können Sie im nächsten Schritt das automatische Targeting für die Traffic-Zuordnungsmethode auswählen.

## Unterstützte Integrationen

| Integration | Unterstützt? |
| --- | --- |
| [Analytics for Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | Ja |
| [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md) | Ja |
| [Kundenattribute](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Ja |
| [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md) | Ja |

## Unterstützte Funktionen {#supported-features}

| Funktion | Unterstützt? |
| --- | --- |
| [Arbeitsbereiche und Eigenschaften](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Ja |
| [QA-Links](/help/c-activities/c-activity-qa/activity-qa.md) | Ja |
| [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) | Nein |
| [Benutzerspezifischer Code ](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | Ja |
| [VEC-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Alle |
| [Klick-Tracking](/help/c-activities/r-success-metrics/click-tracking.md) | Ja |
| [Bereitstellung mehrerer Aktivitäten](/help/c-experiences/c-visual-experience-composer/multipage-activity.md) | Ja |

## Page Delivery settings for the SPA VEC {#page-delivery-settings}

[!UICONTROL Mit den Einstellungen für die Seitenauslieferung] können Sie Regeln konfigurieren, um zu bestimmen, wann eine Target-Aktivität qualifiziert und für eine Zielgruppe ausgeführt werden soll.

To access the [!UICONTROL Page Delivery] options from within the VEC&#39;s three-part guided activity-creation workflow, from the **[!UICONTROL Experiences]** step, click **[!UICONTROL Configure]** (the gear icon) &gt; **[!UICONTROL Page Delivery]**.

![Seitenauslieferungsoptionen, Dialogfeld](/help/c-experiences/assets/page-delivery.png)

For example, as defined by the [!UICONTROL Page Delivery] settings shown above, a Target activity qualifies and executes when a visitor lands directly on `https://www.adobe.com` *or* when a visitor lands on any URL that contains `https://www.adobe.com/products`. Dies funktioniert perfekt für jede mehrseitige Anwendung, bei der jede Interaktion mit der Seite eine Seitenneuladung aufruft, für die at. js die Aktivitäten abruft, die sich für die URL qualifizieren, zu der der Benutzer navigiert.

However, because SPAs work differently, the [!UICONTROL Page Delivery] settings must be configured in a way that allows all actions to be applied to the Views as defined in the SPA VEC activity.

### Verwendungsfall

Betrachten Sie diesen Beispiel-Anwendungsfall:

![SPA VEC-Änderungsbedienfeld](/help/c-experiences/assets/page-delivery-example.png)

Folgende Änderungen wurden vorgenommen:

* Changed the background color in the Home view, which is located under the URL: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* Changed the button color in the Products view, which is located under the URL: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).

With the example above in mind, what would happen when we configure [!UICONTROL Page Delivery] settings to only include: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/) in an SPA with at.js 2.*x*?

![Seitenbereitstellung, Dialogfeld](/help/c-experiences/assets/spa-page-delivery.png)

Die folgende Abbildung zeigt den Target Flow - Seitenlastanforderung in at. js 2.*x*:

![Zielfluss - at. js 2.0 Seitenladenanforderung](/help/c-experiences/assets/page-load-request.png)

**Benutzerreise Nr. 1**

* A user navigates directly to [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* at.js 2.*x* gibt an, ob eine Aktivität für die URL ausgeführt werden muss: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* In Schritt 6 gibt Target Edge die Aktionen für die Start- und Produktansicht zurück, sodass sie im Browser zwischengespeichert werden.

**Ergebnis**: Der Benutzer sieht die grüne Hintergrundfarbe in der Startansicht. When the user then navigates to [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products), the blue background color of the button is seen because the action is cached in the browser under the Products view.

Note: The user navigating to [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) did not trigger a page load.

**Benutzerreise Nr. 2**

* A user navigates directly to [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* at.js 2.*x* gibt an, ob eine Aktivität für die URL ausgeführt werden muss: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* There are no activities qualified for [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* Da keine Aktivitäten qualifiziert sind, gibt es keine Aktionen und Ansichten für at. js 2 zwischengespeichert.*x* auszulösen.

**Ergebnis**: Selbst wenn Sie für `triggerView()` die Produktansicht definiert und eine Aktion an die Produktansicht über SPA VEC durchgeführt haben, wird die erwartete Aktion nicht angezeigt, da Sie keine Regel erstellt haben, die [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) in den Seitenbereitstellungseinstellungen enthält.

### Best Practice

Sie können sehen, dass die Verwaltung der Benutzerreise recht schwierig sein kann, da Benutzer auf einer beliebigen URL Ihrer Einzelseitenanwendung landen können und zu jeder anderen Seite navigieren. Daher empfiehlt es sich, eine Seitenauslieferungsregel anzugeben, die die Basis-URL enthält, damit sie die gesamte Einzelseitenanwendung enthält. Auf diese Weise müssen Sie nicht alle verschiedenen Routen und Pfade berücksichtigen, die ein Benutzer benötigt, um zu einer Seite zu gelangen, auf der Sie eine A/B-Test- oder Erlebnis-Targeting (XT)-Aktivität anzeigen möchten.

Um das oben stehende Problem zu beheben, können wir beispielsweise die Basis-URL in den Seitenbereitstellungseinstellungen angeben:

![Seitenbereitstellung, Dialogfeld](/help/c-experiences/assets/conclusion.png)

Dadurch wird sichergestellt, dass immer, wo ein Besucher auf die SPA landet und zur Homepage oder zur Seitenansicht navigiert, die angewendeten Aktionen angezeigt werden.

Now, whenever you add an action to a View in the SPA VEC, we will show you the following pop-up message to remind you to think about the [!UICONTROL Page Delivery] rules.

![Seitenbereitstellungseinstellungen](/help/c-experiences/assets/pop-up-message.png)

Diese Meldung wird angezeigt, wenn Sie die erste Aktion einer Ansicht für jede neue Aktivität hinzufügen, die Sie erstellen. This message helps ensure that everyone in your organization learns how to apply these [!UICONTROL Page Delivery] rules correctly.

## Schulungsvideo: Verwendung von VEC für SPAs in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249?captions=ger)

See [Using the Visual Experience Composer for Single Page Application (SPA VEC) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) for more information.
