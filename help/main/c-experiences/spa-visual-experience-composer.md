---
keywords: SPA VEC;React;Angular;react.js;SPA Visual Experience Composer;Optionen in SPA Experience Composer;Einzelseiten-App;Single-Page-App;SPA;Optionen für mobile Erlebnisse;Target-Ansicht
description: Erfahren Sie, wie Sie mit dem SPA VEC in Adobe [!DNL Target]  Tests erstellen und Inhalte auf SPA im Selbststudium personalisieren können, ohne von der kontinuierlichen Entwicklung abhängig zu sein.
title: Wie verwende ich die Single Page App Visual Experience Composer (SPA VEC)?
feature: Visual Experience Composer (VEC)
exl-id: fd3dcfaa-e5c6-45a1-8229-9c206562e5b0
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '3569'
ht-degree: 64%

---

# Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)

In [!DNL Adobe Target] bietet der [!UICONTROL Visual Experience Composer] (VEC) Marketing-Experten eine Do-it-yourself-Funktion zum Erstellen von Aktivitäten und Personalisieren von Erlebnissen, die dynamisch über die globale Mbox von Adobe Target in herkömmlichen mehrseitigen Anwendungen bereitgestellt werden können. Dies beruht jedoch darauf, Angebote beim Laden der Seite oder über nachfolgende Serveraufrufe abzurufen, wodurch wie im Diagramm unten dargestellt Latenzzeiten entstehen. Dieser Ansatz funktioniert nicht gut mit Einzelseiten-Apps (SPAs), da dadurch die Benutzererfahrung und die Anwendungsleistung beeinträchtigt werden.

![Herkömmlicher Lebenszyklus und SPA-Lebenszyklus](/help/main/c-experiences/assets/trad-vs-spa.png)

Mit der neuesten Version bieten wir nun VEC für SPAs an. VEC für SPAs ermöglicht es Marketing-Experten, für SPAs selbst Tests zu erstellen und Inhalt zu personalisieren, ohne von der kontinuierlichen Weiterentwicklung abhängig zu sein. Mit VEC können Sie [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md)- und [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md)-Aktivitäten (XT-Aktivitäten) in beliebten Frameworks wie React und Angular erstellen.

## Adobe [!DNL Target] Ansichten und Single Page Applications

Adobe Target VEC für SPAs basiert auf einem neuen Konzept für Ansichten: Eine Ansicht entspricht einer logischen Gruppe visueller Elemente, aus denen sich ein SPA-Erlebnis zusammensetzt. Eine SPA kann also als eine Reihe von Ansichten anstelle von URLs betrachtet werden, die je nach Benutzerinteraktion aufgerufen werden. Eine Ansicht umfasst in der Regel eine ganze Site oder eine Gruppe visueller Elemente innerhalb einer Site.

Um weiter zu erklären, was Ansichten sind, gehen wir zu dieser hypothetischen Online-E-Commerce-Site, die in React implementiert ist, und sehen uns einige Beispielansichten an. Klicken Sie auf die folgenden Links, um diese Website auf einer neuen Browser-Registerkarte zu öffnen.

**Link: [Startseite](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/)**

![Homepage](/help/main/c-experiences/assets/home.png)

Wenn wir zur Homepage navigieren, können wir sofort ein Hero-Bild sehen, das einen Osterverkauf bewirbt, sowie die neuesten Produkte, die auf der Site verkauft werden. In diesem Fall kann die gesamte Homepage als Ansicht definiert werden. Dies sollten Sie im Hinterkopf behalten, da wir darauf im Abschnitt „Implementieren von Adobe Target-Ansichten“ unten näher eingehen werden.

**Link: [Produktseite](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products)**

![Produktseite](/help/main/c-experiences/assets/product-site.png)

Da uns die Produkte interessieren, klicken wir auf den Link zu den Produkten. Ähnlich wie die Homepage kann die gesamte Produktseite als Ansicht definiert werden. Wir können diese Ansicht „Produkte“ nennen, genau wie der Pfadname in `https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products`.

![Produktseite 2](/help/main/c-experiences/assets/product-site-2.png)

Am Anfang dieses Abschnitts haben wir Ansichten als ganze Site oder sogar als eine Gruppe visueller Elemente auf der Site definiert. Wie oben gezeigt, können die vier auf der Site angezeigten Produkte auch gruppiert und als Ansicht betrachtet werden. Als Name für diese Ansicht käme „Produkte“ in Frage.

![Produktseite 3](/help/main/c-experiences/assets/product-site-3.png)

Klicken Sie auf die Schaltfläche „Mehr laden“, um weitere Produkte auf der Site zu erkunden. In diesem Fall ändert sich die Website-URL nicht. Hier kann auch nur die zweite Zeile der oben gezeigten Produkte als Ansicht angesehen werden. Der Name der Ansicht könnte also „PRODUKTSEITE-2“ lauten.

**link: [Checkout](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/checkout)**

![Checkout-Seite](/help/main/c-experiences/assets/checkout.png)

Da uns einige Produkte auf der Site gefallen haben, beschließen wir, ein paar zu kaufen. Auf der Checkout-Site erhalten wir die Möglichkeit, zwischen dem normalen Versand oder der Expresszustellung zu wählen. Da eine beliebige Gruppe visueller Elemente auf einer Site als Ansicht definiert werden kann, können wir diese Ansicht „Versand-Voreinstellungen“ nennen.

Das Konzept Ansichten aber kann noch viel mehr ausgeweitet werden. Für Marketing-Experten, die den Inhalt einer Site je nach Versandpräferenz personalisieren möchten, gibt es die Möglichkeit, eine Ansicht für jede Versandpräferenz zu erstellen. Wenn wir in diesem Fall den normalen Versand auswählen, kann die Ansicht „Normaler Versand“ heißen. Wenn die Expresszustellung ausgewählt wird, kann die Ansicht „Expresszustellung“ lauten.

Ihre Marketing-Experten können auch einen A/B-Test durchführen, um zu sehen, ob die Änderung der Farbe von Blau auf Rot nach Auswahl der Expresszustellung die Konversion im Vergleich zu gleichbleibend blauer Button-Farbe für beide Versandoptionen steigert.

## Implementieren von Adobe-[!DNL Target]

Nachdem wir nun erklärt haben, was Adobe Target-Ansichten sind, können wir dieses Konzept in Target nutzen, um Marketern die Möglichkeit zu geben, mithilfe des VEC A/B- und XT-Tests in SPAs durchzuführen. Dies erfordert eine einmalige Einrichtung durch den Entwickler. Führen wir die Schritte zur Einrichtung durch.

1. Installieren Sie at.js 2.x.

   Zunächst müssen Sie at.js 2.x installieren. Diese Version von at.js wurde speziell für SPAs entwickelt. Frühere Versionen von at.js und unterstützen keine Adobe Target-Ansichten und den VEC für SPA.

   ![Dialogfeld „Implementierungsdetails“](/help/main/c-experiences/assets/imp-200.png)

   Laden Sie at.js 2.x über die Adobe Target-Benutzeroberfläche unter [!UICONTROL Administration > Implementation] herunter. at.js 2.x kann auch über Tags in [Adobe Experience Platform bereitgestellt ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html?lang=de){target=_blank}. Die Adobe Target-Erweiterungen sind jedoch derzeit nicht aktuell und werden nicht unterstützt.

1. Implementieren Sie die neueste Funktion von at.js 2.x: [triggerView()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-triggerview-atjs-2.html){target=_blank} auf Ihren Sites.

   Nachdem Sie die Ansichten Ihrer SPA definiert haben, in denen Sie einen A/B- oder XT-Test durchführen möchten, implementieren Sie die `triggerView()` von at.js 2.x mit den als Parameter übergebenen Ansichten. Dadurch können Marketing-Experten VEC zum Entwerfen und Ausführen der A/B- und XT-Tests für diese Ansichten verwenden. Wenn die `triggerView()`-Funktion für diese Ansichten nicht definiert wurde, erkennt VEC die Ansichten nicht, sodass Marketing-Experten den VEC nicht zum Entwerfen und Ausführen von A/B- und XT-Tests verwenden können.

   **`adobe.target.triggerView(viewName, options)`**

   | Parameter | Typ | Erforderlich? | Validierung | Beschreibung |
   | --- | --- | --- | --- | --- |
   | viewName | Zeichenfolge | Ja | 1. Keine nachfolgenden Leerzeichen.<br>2. Darf nicht leer sein.<br>3. Der Name der Ansicht sollte für alle Seiten eindeutig sein.<br>4. **Warnung:** Der Anzeigename sollte nicht mit „`/`“ beginnen oder enden. Dies liegt daran, dass der Kunde den Anzeigenamen im Allgemeinen aus dem URL-Pfad entnimmt. Für uns sind „home“ und „`/home`“ unterschiedlich.<br>5. **Warnung:** Dieselbe Ansicht sollte nicht mehrmals hintereinander mit der Option `{page: true}` ausgelöst werden. | Geben Sie eine beliebige Zeichenfolge als Namen für Ihre Ansicht an. Dieser Ansichtsname wird im [!UICONTROL Modifications] des VEC angezeigt, damit Marketer Aktionen erstellen und ihre A/B- und XT-Aktivitäten ausführen können. |
   | options | Objekt | Nein |  |  |
   | Optionen > Seite | Boolesch | Nein |  | **TRUE**: Der Standardwert der Seite ist „wahr“. Bei `page=true` werden Benachrichtigungen zur Erhöhung der Impressions-Anzahl an die Edge-Server gesendet.<br>**FALSE**: Bei der `page=false` werden keine Benachrichtigungen gesendet, um die Anzahl der Impressionen zu erhöhen. Dies sollte verwendet werden, wenn Sie nur eine Komponente auf einer Seite mit einem Angebot neu rendern möchten. |

   Sehen wir uns nun einige Beispielanwendungsfälle an, in denen beschrieben wird, wie die `triggerView()` in React für unsere hypothetische E-Commerce-SPA aufgerufen wird:

   **Link: [Startseite](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/)**

   ![Home-React-1](/help/main/c-experiences/assets/react1.png)

   Wenn wir als Marketer A/B-Tests auf der gesamten Homepage durchführen möchten, bietet es sich an, die Ansicht, die aus der URL entnommen werden kann, „home“ zu nennen.

   ```javascript
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

   **Link: [Produktseite](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products)**

   Sehen wir uns ein Beispiel an, das etwas komplizierter ist. Nehmen wir an, als Marketing-Experten möchten wir die zweite Zeile der Produkte personalisieren, indem wir die Farbe des Preisschilds in Rot ändern, nachdem ein Benutzer auf die Schaltfläche Mehr laden geklickt hat.

   ![React-Produkte](/help/main/c-experiences/assets/react4.png)

   ```javascript
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
       var page = this.state.page + 1; // assuming page number is derived from component's state
       this.setState({page: page});
       targetView('PRODUCTS-PAGE-' + page);
     }
   }
   ```

   **link: [Checkout](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/checkout)**

   ![React-Checkout](/help/main/c-experiences/assets/react6.png)

   Für Marketing-Experten, die den Inhalt einer Site je nach Versandpräferenz personalisieren möchten, gibt es die Möglichkeit, eine Ansicht für jede Versandpräferenz zu erstellen. Wenn wir in diesem Fall den normalen Versand auswählen, kann die Ansicht „Normaler Versand“ heißen. Wenn die Expresszustellung ausgewählt wird, kann die Ansicht „Expresszustellung“ lauten.

   Ihre Marketing-Experten können auch einen A/B-Test durchführen, um zu sehen, ob die Änderung der Farbe von Blau auf Rot nach Auswahl der Expresszustellung die Konversion im Vergleich zu gleichbleibend blauer Button-Farbe für beide Versandoptionen steigert.

   ```javascript
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

Im Bedienfeld [Änderungen](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) und bei den Aktionen für VEC gibt es zwei wesentliche Verbesserungen, mit denen VEC gut mit SPAs funktioniert.

**Bedienfeld „Änderungen“**

Das Bedienfeld [!UICONTROL Modifications] erfasst wie unten dargestellt die für eine bestimmte Ansicht erstellten Aktionen. Beachten Sie, dass alle Aktionen für eine Ansicht unter dieser Ansicht gruppiert werden.

**Aktionen**

Durch Klicken auf eine Aktion wird das Element auf der Sites hervorgehoben, in dem diese Aktion angewendet wird. Jede VEC-Aktion, die unter einer Ansicht erstellt wurde, verfügt über die folgenden, unten aufgeführten Symbole: Informationen, Bearbeiten, Klonen, Verschieben und Löschen.

![Änderungen](/help/main/c-experiences/assets/modifications.png)

Die einzelnen Aktionen sind in der folgenden Tabelle beschrieben:

| Seite | Beschreibung |
| --- | --- |
| Informationen | Zeigt die Details der Aktion an. |
| Bearbeiten | Ermöglicht die direkte Bearbeitung der Eigenschaften dieser Aktion. |
| Klonen | Klonen Sie die Aktion in eine oder mehrere Ansichten, die im Bedienfeld [!UICONTROL Modifications] vorhanden sind, oder in eine oder mehrere Ansichten, die Sie im VEC durchsucht und aufgerufen haben. Die Aktion muss nicht unbedingt im [!UICONTROL Modifications] vorhanden sein.<br>**Hinweis**: Nachdem ein Klonvorgang durchgeführt wurde, müssen Sie zur Ansicht in VEC über [!UICONTROL Browse] navigieren, um zu sehen, ob die geklonte Aktion ein gültiger Vorgang war. Wenn die Aktion nicht auf die Ansicht angewendet werden kann, wird ein Fehler angezeigt. |
| Verschieben | Hiermit wird die Aktion in ein Seitenladereignis oder eine andere Ansicht verschoben, die im Änderungs-Bedienfeld bereits vorhanden ist.<br>[!UICONTROL Page Load Event] - Alle Aktionen, die dem Seitenladeereignis entsprechen, werden beim ersten Laden der Seite Ihrer Web-Anwendung angewendet.<br>**Hinweis** Nachdem ein Verschiebevorgang ausgeführt wurde, müssen Sie über Durchsuchen zur Ansicht im VEC navigieren, um festzustellen, ob es sich um einen gültigen Vorgang handelte. Wenn die Aktion nicht auf die Ansicht angewendet werden kann, wird ein Fehler angezeigt. |
| Löschen | Löscht die Aktion. |

>[!NOTE]
>
>Sie können viele Aktionen ausführen, bevor die Seite im VEC geladen wird, oder selbst dann, wenn die Seite gar nicht geladen werden kann. Aktionen, die nicht vor dem Laden der Website bearbeitet werden können, sind in der Benutzeroberfläche deaktiviert.

**Beispiel 1**

Sehen wir uns das obige Beispiel an, in dem wir eine Startansicht erstellt haben. Für diese Ansicht haben wir dabei zwei Ziele im Auge:

1. Die Farbe der Schaltflächen „Zum Einkaufswagen hinzufügen“ und „Gefällt mir“ in eine hellere blaue Farbe ändern. Dies sollte bei einem „Seitenladevorgang“ erfolgen, da wir Komponenten der Kopfzeile ändern.
1. Die Bezeichnung von „Aktuellste Produkte 2019“ zu „Schärfste Produkte 2019“ und die Textfarbe in Violett ändern.

Um diese Ziele auszuführen, klicken Sie in VEC auf [!UICONTROL Compose] und wenden Sie diese Änderungen in der Startansicht an.

![Beispiel 1](/help/main/c-experiences/assets/example1.png)

**Beispiel 2**

Sehen wir uns das obige Beispiel an, in dem wir eine Ansicht „PRODUCTS-PAGE-2“ erstellt haben. Unser Ziel ist es, die Bezeichnung „Preis“ in „Verkaufspreis“ und die Farbe in Rot zu ändern.

1. Klicken Sie auf [!UICONTROL Browse] und dann auf den [!UICONTROL Products] Link in der Kopfzeile.
1. Klicken Sie einmal auf [!UICONTROL Load More] , um zur zweiten Produktzeile zu gelangen.
1. Klicken Sie auf [!UICONTROL Compose].
1. Wenden Sie die Aktionen an, um die Textbeschriftung in „Verkaufspreis“ und die Farbe in Rot zu ändern.

![Beispiel 2](/help/main/c-experiences/assets/example2.png)

**Beispiel 3**

Schließlich können Ansichten, wie bereits erwähnt, auf granularer Ebene definiert werden. Ansichten können einen Status oder sogar eine Option in einem Optionsfeld sein. Zuvor haben wir die Ansichten CHECKOUT-EXPRESS und CHECKOUT-NORMAL erstellt. Unser Ziel ist es, die Schaltflächenfarbe für die CHECKOUT-EXPRESS-Ansicht in Rot zu ändern.

1. Klicken Sie auf [!UICONTROL Browse].
1. Fügen Sie dem Warenkorb einige Produkte hinzu.
1. Klicken Sie oben rechts auf das Warenkorbsymbol.
1. Klicken Sie auf „Zur Kasse gehen“.
1. Klicken Sie auf das Optionsfeld „Expresszustellung“.
1. Klicken Sie auf [!UICONTROL Compose].
1. Ändern Sie die Schaltfläche von „Bezahlen“ in „Bestellung abschließen“ und die Farbe in Rot.

![Beispiel 3](/help/main/c-experiences/assets/example3.png)

>[!NOTE]
>
>Die CHECKOUT-EXPRESS-Ansicht wird erst im Bedienfeld „Änderungen“ angezeigt, wenn Sie auf das Optionsfeld „Expresszustellung“ klicken. Dies liegt daran, dass die `triggerView()`-Funktion ausgelöst wird, wenn das Optionsfeld „Expresszustellung“ ausgewählt wird. Dies ist aber nur der Fall, wenn VEC weiß, dass eine Ansicht im Bedienfeld „Änderungen“ angezeigt wird.

## Ein tief gehender Blick auf at.js und SPAs

**Wie kann ich nach dem ersten Laden der Seite in meiner SPA die Ansichten für die neuesten Zielgruppendaten abrufen, die durch Aktionen erfasst wurden?**

Der typische Workflow von at.js 2.x besteht darin, dass beim Laden Ihrer Site alle Ihre Ansichten und Aktionen zwischengespeichert werden, sodass nachfolgende Benutzeraktionen auf Ihrer Site keine Trigger-Server-Aufrufe zum Abrufen von Angeboten ausführen. Wenn Sie Ansichten je nach aktuellsten Benutzeraktionen abrufen möchten, die auf Grundlage der nachfolgenden Benutzeraktionen aktualisiert wurden, können Sie `getOffers()` und `applyOffers()` mit den aktuellsten weitergeleiteten Zielgruppen- und Profildaten aufrufen.

Angenommen, Sie sind ein Telekommunikationsunternehmen und Sie haben eine SPA, die at.js 2.x verwendet. Als Unternehmen möchten Sie die folgenden Ziele erreichen:

* Für einen abgemeldeten oder anonymen Benutzer sollten Sie die neueste Unternehmensaktion anzeigen, z. B. ein Hero-Angebot „Erster Monat kostenlos“ auf `http://www.telecom.com/home`.
* Für einen angemeldeten Benutzer sollte ein Upgrade-Angebot für Benutzer angezeigt werden, deren Verträge demnächst anstehen, z. B. „Sie haben Anspruch auf ein kostenloses Telefon!“ auf `http://www.telecom.com/loggedIn/home` anzeigen.

Ihre Entwickler benennen die Ansichten und rufen `triggerView()` wie folgt auf:

* Für `http://www.telecom.com/home` lautet der Ansichtsname „Abgemeldet Home“.
   * `triggerView("Logged Out Home")` wird aufgerufen.
* Für `http://www.telecom.com/loggedIn/home` lautet der Ansichtsname „Angemeldet Home“.
   * `triggerView("Logged In Home")` wird bei einer Richtungsänderung aufgerufen.

Anschließend führen Ihre Marketing-Experten die folgenden A/B-Aktivitäten über VEC aus:

* A/B-Aktivität mit dem Angebot „Erster Monat frei“ für Zielgruppen mit dem Parameter &quot;`loggedIn= false`&quot;, die in `http://www.telecom.com/home` angezeigt werden sollen, wo der Ansichtsname „Abgemeldet Startseite“ lautet.
* A/B-Aktivität mit der Option „Sie haben Anspruch auf ein kostenloses Telefon!“ Angebot für Zielgruppen mit dem Parameter &quot;`loggedIn=true`&quot;, das in `http://www.telecom.com/loggedIn/home` angezeigt werden soll, wobei der Name der Ansicht „Hero-Angebot angemeldet“ lautet.

Betrachten wir einmal diesen Benutzerablauf:

1. Ein anonymer, abgemeldeter Benutzer landet auf Ihrer Seite.
1. Da Sie at.js 2.x verwenden, übergeben Sie beim Laden der Seite den Parameter &quot;`loggedIn = false`&quot;, um alle in aktiven Aktivitäten vorhandenen Ansichten abzurufen, die für den Fall qualifiziert sind, dass die Zielgruppe den Parameter &quot;`loggedIn = false`&quot; hat.
1. at.js 2.x ruft dann die Startansicht und Aktion Abgemeldet ab, um das Angebot „Erster Monat frei“ anzuzeigen, und speichert es im Cache.
1. Wenn `triggerView("Logged Out Home")` aufgerufen wird, wird das Angebot „Erster Monat frei“ aus dem Cache abgerufen und das Angebot wird ohne Server-Aufruf angezeigt.
1. Der Benutzer klickt nun auf „Anmelden“ und gibt seine Anmeldeinformationen ein.
1. Da Ihre Website eine SPA ist, wird die Seite nicht komplett geladen, sondern leitet den Benutzer stattdessen zu `http://www.telecom.com/loggedIn/home`.

Hier aber liegt das Problem. Der Benutzer meldet sich an und wir treffen auf `triggerView("Logged In Home")`, weil wir diesen Code bei einer Richtungsänderung platziert haben. Diese weist at.js 2.x an, die Ansicht und Aktionen aus dem Cache abzurufen, aber die einzige Ansicht, die im Cache vorhanden ist, ist „Abgemeldet Home“.

Wie können wir dann unsere Anmeldeansicht abrufen und die Meldung „Sie haben Anspruch auf ein kostenloses Telefon!“ anzeigen? anzeigen? Und da alle nachfolgenden Aktionen auf Ihrer Site aus der Perspektive eines angemeldeten Benutzers stammen, wie können Sie sicherstellen, dass alle nachfolgenden Aktionen zu personalisierten Angeboten für angemeldete Benutzer führen?

Sie können die in at.js 2.x unterstützten neuen Funktionen `getOffers()` und `applyOffers()` verwenden:

```javascript
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

Übergeben Sie die Antwort von `getOffers()` an `applyOffers()`. Jetzt werden alle Ansichten und Aktionen, die mit „loggedIn = true“ verknüpft sind, den at.js-Cache aktualisieren.

Mit anderen Worten: at.js 2.x unterstützt eine Methode zum Abrufen von Ansichten, Aktionen und Angeboten mit den aktuellsten Zielgruppendaten auf Anforderung.

**Unterstützt at.js 2.x A4T für Einzelseiten-Apps?**

Ja, at.js 2.x unterstützt A4T für SPA über die `triggerView()`-Funktion, wenn Sie Adobe Analytics und den Experience Cloud-Besucher-ID-Dienst implementiert haben. Siehe Diagramm unten mit schrittweisen Beschreibungen.

![Target-Ablauf](/help/main/c-experiences/assets/atjs-spa-flow.png)

| Schritt | Beschreibung |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern, die mit der Ansicht zusammenhängen. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 3 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den Target-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

>[!NOTE]
>Wenn Sie nicht jedes Mal Benachrichtigungen zur Impressionszählung an Adobe Analytics senden möchten, wenn eine Ansicht ausgelöst wird, übergeben Sie `{page: false}` an die `triggerView()` , damit die Impressionszählung nicht erhöht wird, wenn eine Ansicht mehrmals für eine Komponente ausgelöst wird, die ständig neu gerendert wird. Beispiel:
>
>`adobe.target.triggerView("PRODUCTS-PAGE-2", {page:false})`

## Unterstützte Aktivitäten

| Aktivitätstyp | Unterstützt? |
| --- | --- |
| [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [Recommendations as a Offer](/help/main/c-recommendations/recommendations-as-an-offer.md)<br>in A/B-Test- und Erlebnis-Targeting(XT)-Aktivitäten | Ja |
| [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja |
| [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Nein |
| [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nein |
| [Automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nein |
| [Recommendations](/help/main/c-recommendations/recommendations.md) | Nein |

**Wie führen wir, wenn wir at.js 2.x installiert und `triggerView()` auf unseren Sites implementiert haben, A/B-Aktivitäten mit automatischem Targeting aus, da SPA VEC das automatische Targeting nicht unterstützt?**

Wenn Sie A/B-Aktivitäten mit automatischem Targeting verwenden möchten, können Sie alle Aktionen so verschieben, dass sie in VEC beim Laden der Seite ausgeführt werden. Bewegen Sie den Mauszeiger über die einzelnen Aktionen und klicken Sie auf die Schaltfläche [!UICONTROL Move to Page Load Event] . Anschließend können Sie im nächsten Schritt das automatische Targeting für die Traffic-Zuordnungsmethode auswählen.

## Unterstützte Integrationen

| Integration | Unterstützt? |
| --- | --- |
| [Analytics for Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) | Ja |
| [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md) | Ja |
| [Kundenattribute](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/customer-attributes.html){target=_blank} | Ja |
| [AEM-Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | Ja |

## Unterstützte Funktionen {#supported-features}

| Funktion | Unterstützt? |
| --- | --- |
| [Arbeitsbereiche und Eigenschaften](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) | Ja |
| [QA-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) | Ja |
| [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) | Nein |
| [Benutzerspezifischer Code ](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | Ja |
| [VEC-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) | Alle |
| [Klick-Tracking](/help/main/c-activities/r-success-metrics/click-tracking.md) | Ja |
| [Bereitstellung mehrerer Aktivitäten](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md) | Ja |

## Seitenbereitstellungseinstellungen für den SPA VEC {#page-delivery-settings}

Mit [!UICONTROL Page Delivery] Einstellungen können Sie Regeln konfigurieren, um zu bestimmen, wann eine Target-Aktivität für eine Zielgruppe qualifiziert und ausgeführt werden soll.

Um auf die [!UICONTROL Page Delivery] Optionen im dreiteiligen Workflow für die geführte Aktivitätserstellung von VEC zuzugreifen, klicken Sie im **[!UICONTROL Experiences]** Schritt auf **[!UICONTROL Configure]** (Zahnradsymbol) > **[!UICONTROL Page Delivery]**.

![Dialogfeld „Seitenbereitstellung“](/help/main/c-experiences/assets/page-delivery.png)

Wie durch die oben gezeigten [!UICONTROL Page Delivery] definiert, qualifiziert sich beispielsweise eine Target-Aktivität und wird ausgeführt, wenn ein Besucher direkt auf `https://www.adobe.com` landet *oder* wenn ein Besucher auf einer URL landet, die `https://www.adobe.com/products` enthält. Dies eignet sich besonders für alle mehrseitigen Anwendungen, bei der bei jeder Seiteninteraktion die Seite neu geladen wird. In at.js werden dabei die Aktivitäten abgerufen, die sich für die vom Benutzer geöffnete URL qualifizieren.

Da die SPA jedoch anders funktioniert, müssen die [!UICONTROL Page Delivery] so konfiguriert werden, dass alle Aktionen auf die Ansichten angewendet werden können, wie sie in der SPA VEC-Aktivität definiert sind.

### Anwendungsfall

Im Folgenden wird ein Anwendungsfall beschrieben:

![Bedienfeld für SPA-VEC-Änderungen](/help/main/c-experiences/assets/page-delivery-example.png)

Folgende Änderungen wurden vorgenommen:

* Hintergrundfarbe in der Startansicht geändert, die sich unter der URL befindet: [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/).
* Schaltflächenfarbe in der Ansicht „Produkte“ geändert, die sich unter der URL befindet: [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products).

Was würde im Hinblick auf das obige Beispiel passieren, wenn wir [!UICONTROL Page Delivery] so konfigurieren, dass nur Folgendes enthalten ist: [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/) in einer SPA mit at.js 2.*x*?

![Dialogfeld „Seitenbereitstellung“](/help/main/c-experiences/assets/spa-page-delivery.png)

Die folgende Abbildung zeigt den Target-Ablauf: Seitenladeanfrage in at.js 2.*x*:

![Target-Ablauf: Seitenladeanfrage in at.js 2.0](/help/main/c-experiences/assets/page-load-request.png)

**Customer Journey Nr. 1**

* Ein Benutzer navigiert direkt zu [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/).
* at.js 2.*x* führt eine Abfrage an Edge durch, um festzustellen, ob eine Aktivität für die URL ausgeführt werden muss: [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/).
* In Schritt 6 gibt Target Edge die Aktionen für die Startseiten- und Produktansicht zurück, sodass sie im Browser zwischengespeichert werden.

**Ergebnis**: Der Benutzer sieht die grüne Hintergrundfarbe in der Startansicht. Wenn der/die Benutzende dann zu [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products) navigiert, wird die blaue Hintergrundfarbe der Schaltfläche angezeigt, da die Aktion im Browser unter der Produktansicht zwischengespeichert wird.

Hinweis: Der Benutzer, der zu [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products) navigiert, hat keinen Trigger beim Laden einer Seite erzeugt.

**Customer Journey Nr. 2**

* Ein Benutzer navigiert direkt zu [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products).
* at.js 2.*x* führt eine Abfrage an Edge durch, um festzustellen, ob eine Aktivität für die URL ausgeführt werden muss: [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products).
* Es gibt keine für [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products) qualifizierten Aktivitäten.
* Da es keine Aktivitäten gibt, müssen auch keine Aktionen und Ansichten zwischengespeichert werden, damit at.js 2 *x* ausgelöst werden kann.

**Ergebnis**: Selbst wenn Sie `triggerView()` für die Produktansicht definiert und über den SPA VEC eine Aktion zur Produktansicht durchgeführt haben, wird die erwartete Aktion nicht angezeigt, da Sie keine Regel erstellt haben, die [https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products](https://experienceleague.adobe.com/developer/ashop-react-demo/at-js/#/products) in die Seitenbereitstellungseinstellungen aufgenommen hat.

### Best Practice

Die Verwaltung der Customer Journey kann schwierig sein, da Kunden auf jeder beliebigen URL der Einzelseitenanwendung landen und zu jeder anderen Seite navigieren können. Daher empfiehlt es sich, eine Seitenbereitstellungsregel zu spezifizieren, die die Basis-URL beinhaltet, damit die gesamte Einzelseitenanwendung enthalten ist. Auf diese Weise müssen Sie nicht über all die verschiedenen Journey und Pfade nachdenken, die ein(e) Benutzende(r) verwendet, um zu einer Seite zu gelangen, auf der Sie eine A/B-Test - oder Erlebnis-Targeting (XT)-Aktivität anzeigen möchten.

Um das oben stehende Problem zu beheben, können Sie beispielsweise die Basis-URL in den Seitenbereitstellungs-Einstellungen spezifizieren:

![Dialogfeld „Seitenbereitstellung“](/help/main/c-experiences/assets/conclusion.png)

Dadurch wird sichergestellt, dass ein Kunde die angewendeten Aktionen sehen kann, unabhängig davon, wo er auf der SPA landet und ob er zur Startseite oder zur Seitenansicht navigiert.

Jedes Mal, wenn Sie im SPA VEC eine Aktion zu einer Ansicht hinzufügen, wird Ihnen die folgende Popup-Meldung angezeigt, die Sie daran erinnert, über die [!UICONTROL Page Delivery] Regeln nachzudenken.

![Meldung zu den Seitenbereitstellungs-Einstellungen ](/help/main/c-experiences/assets/pop-up-message.png)

Diese Meldung wird angezeigt, wenn Sie die erste Aktion einer Ansicht für jede von Ihnen neu erstellte Aktivität hinzufügen. Diese Meldung hilft sicherzustellen, dass alle Personen in Ihrem Unternehmen lernen, wie diese [!UICONTROL Page Delivery] korrekt angewendet werden.

## Schulungsvideo: Verwendung von VEC für SPAs in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Weitere [ finden Sie unter „Verwenden des Visual Experience Composer für Einzelseitenanwendungen (SPA VEC) ](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) Adobe Target&quot;.
