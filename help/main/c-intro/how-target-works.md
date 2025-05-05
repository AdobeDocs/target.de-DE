---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;Suchmaschinenoptimierung;seo;Edge-Cluster;zentrale Cluster;at.js;mbox.js;
description: Erfahren Sie [!DNL Adobe Target]  wie funktioniert, einschließlich Informationen zu JavaScript-Bibliotheken (AEP Web SDK at.js), Nutzungsstrategien für Server-Aufrufe, Nutzung, Adobe-Rechenzentren, SEO-Tests und Bots.
title: Wie funktioniert  [!DNL Target] ?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: c5cca9b4b95289626ade1654bb508ee9f0bf35f3
workflow-type: tm+mt
source-wordcount: '2215'
ht-degree: 24%

---

# Funktionsweise von [!DNL Adobe Target]

Erfahren Sie, wie [!DNL Adobe Target] funktioniert, einschließlich Details zu den JavaScript-Bibliotheken ([!DNL Adobe Experience Platform Web SDK] und at.js). Dieser Artikel behandelt auch die verschiedenen Aktivitätstypen, die Sie erstellen können, [!DNL Target] Nutzungszählungsstrategien, die [!DNL Target] Edge Network-, SEO- und Bot-Erkennung.

Zu den wichtigsten Punkten gehören:

* **JavaScript-Bibliotheken**: Erfahren Sie mehr über die [!DNL Target] JavaScript-Bibliotheken: [!DNL Adobe Experience Platform Web SDK] und at.js.
* **Nutzungsstrategien für Server-Aufrufe**: Verstehen Sie, wie [!DNL Target] verschiedene Server-Aufrufe zählt, einschließlich Endpunkte, einzelner Mbox-, Batch-Mbox-, Ausführungs-, Vorabruf- und Benachrichtigungsaufrufe.
* **Edge Network**: Erfahren Sie, wie [!DNL Target] mit dem [!DNL Adobe Experience Platform Edge Network] interagiert.
* **Geschütztes Benutzererlebnis** Erfahren Sie, wie [!DNL Adobe] die Verfügbarkeit und Leistung der Targeting-Infrastruktur sicherstellt.
* **SEO-Richtlinien** Befolgen Sie die Best Practices für die Ausrichtung [!DNL Target] Aktivitäten an den SEO-Richtlinien.
* **Bot-Traffic**: Erfahren Sie, wie Target Bot-Traffic verarbeitet, um verzerrende Tests und Personalisierungsalgorithmen zu vermeiden.

## [!DNL Adobe Target] JavaScript-Bibliotheken {#libraries}

Target lässt sich mithilfe von [!DNL Experience Platform Web SDK] oder at.js in Websites integrieren:

* **[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}**: Diese Client-seitige JavaScript-Bibliothek ermöglicht es [!DNL Adobe Experience Cloud] Kunden, über die [!DNL Experience Platform Edge Network] mit verschiedenen Services zu interagieren. [!DNL Adobe] empfiehlt neuen [!DNL Target], die [!DNL Experience Platform Web SDK] zu implementieren.
* **[at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=de){target=_blank}**: Diese Implementierungsbibliothek für [!DNL Target] verbessert die Seitenladezeiten für Web-Implementierungen und bietet bessere Optionen für Single-Page-Anwendungen. [!DNL Adobe] wird häufig mit neuen Funktionen aktualisiert und empfiehlt allen [at.js-Benutzern, auf die neueste Version zu aktualisieren](https://experienceleague-review.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

>[!NOTE]
>
>Die Bibliothek „mbox.js“ ist eine veraltete Implementierung für [!DNL Target] und wird nach dem 31. März 2021 nicht mehr unterstützt. Aktualisieren Sie auf die [!UICONTROL Experience Platform Web SDK] (empfohlen) oder die neueste Version von at.js.

Referenzieren Sie die [!UICONTROL Experience Platform Web SDK] oder at.js auf jeder Seite Ihrer Site. Fügen Sie beispielsweise eine dieser Bibliotheken zu Ihrer globalen Kopfzeile hinzu. Verwenden Sie alternativ [Tags in Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/tags/home){target=_blank}, um [!DNL Target] zu implementieren.

Die folgenden Ressourcen enthalten detaillierte Informationen zur Implementierung von [!DNL Experience Platform Web SDK] oder „at.js“:

* [[!DNL Adobe Experience Platform Web SDK] Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=de){target=_blank}
* [Implementieren von  [!DNL Target]  mithilfe von  [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch){target=_blank}

Bei jeder Besucheranforderung einer für [!DNL Target] optimierten Seite wird eine Echtzeitanforderung an das Targeting-System gesendet, um den bereitzustellenden Inhalt zu bestimmen. Diese Anfrage wird jedes Mal beim Laden einer Seite gestellt und erfüllt. Sie wird durch Aktivitäten und Erlebnisse gesteuert, die vom Marketing-Experten gesteuert werden. Inhalte sind auf individuelle Besucher der Website ausgerichtet, wodurch die Antwort- und Akquiseraten sowie der Umsatz maximiert werden. Personalisierte Inhalte helfen sicherzustellen, dass Besucher reagieren, interagieren oder Käufe tätigen.

[!DNL Target] ist jedes Seitenelement Teil eines einheitlichen Erlebnisses, das mehrere Elemente enthalten kann.

Der angezeigte Inhalt hängt von der Art der Aktivität ab, die Sie erstellen:

### [!UICONTROL A/B Test]

In einem einfachen A/B-Test werden Inhalte nach dem Zufallsprinzip aus den zugewiesenen Erlebnissen ausgewählt. Sie können die Traffic-Zuordnungsprozentsätze für jedes Erlebnis festlegen. Anfangs kann der Traffic aufgrund der zufälligen Aufteilung ungleichmäßig verteilt sein, wird aber mit zunehmendem Traffic ausgeglichen. Bei zwei Erlebnissen wird beispielsweise das Starterlebnis nach dem Zufallsprinzip ausgewählt. Geringer Traffic kann den Prozentsatz der Besucher in Richtung eines Erlebnisses verschieben, aber diese Situation gleicht sich mit mehr Traffic aus.

Geben Sie für jedes Erlebnis Prozentziele an. Zur Auswahl des anzuzeigenden Erlebnisses wird eine Zufallszahl generiert. Die resultierenden Prozentsätze stimmen möglicherweise nicht genau mit den Zielen überein, aber höherer Traffic führt zu einer engeren Aufteilung an den Zielzielen.

1. Ein Kunde fordert eine Seite von Ihrem Server an, die in seinem Browser angezeigt wird.
1. Im Browser des Kunden wird ein Erstanbieter-Cookie gesetzt, um sein Verhalten zu speichern.
1. Die Seite ruft das Targeting-System auf.
1. Inhalte werden anhand der Aktivitätsregeln angezeigt.

Weitere Informationen finden Sie unter [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate] identifiziert das erfolgreichste Erlebnis aus zwei oder mehr Optionen. Dem Gewinner wird dann automatisch mehr Traffic zugewiesen, was im Laufe des Tests und des Lernens die Konversionen erhöht.

Weitere Informationen finden Sie unter [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) .

### [!UICONTROL Auto-Target] (AT)

[!UICONTROL Auto-Target] nutzt fortschrittliche Machine Learning-Algorithmen zur Auswahl eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen. [!UICONTROL Auto-Target] bietet jedem Besucher das passendste Erlebnis, basierend auf den individuellen Kundenprofilen und dem Verhalten früherer Besucher mit ähnlichen Profilen. Verwenden Sie [!UICONTROL Auto-Target], um Inhalte zu personalisieren und Konversionen zu fördern.

Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

### [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besucher/innen durch fortschrittliche Algorithmen für maschinelles Lernen verschiedene Varianten zu. AP personalisiert Inhalte anhand individueller Kundenprofile, um die Steigerung zu fördern.

Weitere Informationen finden Sie unter [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

### [!UICONTROL Experience Targeting] (XT)

[!UICONTROL Experience Targeting] (XT) stellt Inhalte für bestimmte Zielgruppen auf der Grundlage von Regeln und Kriterien bereit, die von den Werbungtreibenden definiert werden. Einschließlich Geotargeting ist XT nützlich, um Regeln zu definieren, die auf bestimmte Erlebnisse oder Inhalte für bestimmte Zielgruppen ausgerichtet sind. Für eine Aktivität können mehrere Regeln festgelegt werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen. Wenn Besucher Ihre Website aufrufen, werden sie von XT ausgewertet, um festzustellen, ob sie die Kriterien erfüllen. Wenn sie sich qualifizieren, treten sie in die Aktivität ein und sehen das für sie entwickelte Erlebnis. Sie können Erlebnisse für mehrere Zielgruppen innerhalb einer einzelnen Aktivität erstellen.

Weitere Informationen finden Sie unter [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4).

### [!UICONTROL Multivariate Test] (MVT)

[!UICONTROL Multivariate Testing] (MVT) vergleicht Kombinationen von Angeboten in Seitenelementen, um festzustellen, welche Kombination für eine bestimmte Zielgruppe am besten funktioniert. MVT ermittelt also, welches Element den größten Einfluss auf den Erfolg der Aktivität hat.

Weitere Informationen finden Sie unter [Multivariante Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

### [!UICONTROL Recommendations]

[!UICONTROL Recommendations] -Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Aktivitäten oder anderen Algorithmen für Kunden interessant sein könnten. Recommendations helfen, Kunden zu relevanten Elementen zu führen, die sie andernfalls möglicherweise nicht entdecken würden.

Weitere Informationen finden Sie unter [Recommendations](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0).

<!--
## How [!DNL Target] counts server-call usage {#usage}

[!DNL Target] counts only server calls that provide value to customers. The following table shows how [!DNL Target] counts endpoints, single mbox, batch mbox calls, execute, prefetch, and notification calls.

The following information helps you understand the counting strategy used for [!DNL Target] server calls, as shown in the table below:

* **Count Once**: Counts once per API call.
* **Count the Number of mboxes**: Counts the number of mboxes under the array in the payload of a single API call.
* **Ignore**: Is not counted at all.
* **Count the Number of Views (Once)**: Counts the number of views under the array in the payload. In a typical implementation, a view notification has only one view under the notifications array, making this equivalent to counting once in most implementations.

|Endpoint|Fetch type|Options|Counting strategy|
|--- |--- |--- |-- |
|`rest//v1/mbox`|Single|[!UICONTROL execute]|Count once|
|`rest/v2/batchmbox`|Batch|[!UICONTROL execute]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch]|Ignore|
||Batch|[!UICONTROL notifications]|Count the number of mboxes|
|`/ubox/[raw\|image\|page]`|Single|[!UICONTROL execute]|Count once|
|`rest/v1/delivery`<p>`/rest/v1/target-upstream`|Single|[!UICONTROL execute] > [!UICONTROL pageLoad]|Count once|
||Single|[!UICONTROL prefetch] > [!UICONTROL pageLoad]|Ignore|
||Single|[!UICONTROL prefetch] > [!UICONTROL views]|Ignore|
||Batch|[!UICONTROL execute] > [!UICONTROL mboxes]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch] > [!UICONTROL mboxes]|Ignore|
||Batch|[!UICONTROL notifications] > [!UICONTROL views]|Count the number of views (once)|
||Batch|[!UICONTROL notifications] > [!UICONTROL pageLoad]|Count once|
||Batch|[!UICONTROL notifications] > type ([!UICONTROL conversions])|Count once|
||Batch|[!UICONTROL notifications] > [!UICONTROL mboxes]|Count the number of mboxes|

-->

## Das Edge-Netzwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Eine &quot;Edge&quot; ist eine geografisch verteilte Serving-Architektur, die Besuchenden die angeforderten Inhalte unabhängig von ihrem Standort optimal beantwortet.

Zur Verbesserung der Reaktionszeiten werden auf [!DNL Target]-Edges nur Aktivitätslogik, zwischengespeicherte Profile und Angebotsinformationen gehostet.

Aktivitäts- und Inhaltsdatenbanken, [!DNL Analytics], APIs und die Benutzeroberflächen der Werbungtreibenden werden in [!DNL Adobe] zentralen Clustern gespeichert. Aktualisierungen werden an die [!DNL Target]-Edges gesendet, die automatisch mit den zentralen Clustern synchronisiert werden, um zwischengespeicherte Aktivitätsdaten kontinuierlich zu aktualisieren. Außerdem werden alle 1:1-Modelle an jedem Edge gespeichert, sodass komplexe Anforderungen lokal verarbeitet werden können.

Jeder Edge-Cluster enthält alle erforderlichen Informationen, um auf Inhaltsanfragen von Besuchern zu reagieren und Analysedaten zu verfolgen. Die Besucheranforderungen werden an den nächstgelegenen Edge-Cluster weitergeleitet.

Weitere Informationen erhalten Sie im Whitepaper [Sicherheitsübersicht über Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

[!DNL Target] wird weltweit auf Adobe-eigenen und von Adobe geleasten Rechenzentren gehostet.

An zentralen Cluster-Standorten befinden sich sowohl Datenerfassungs- als auch Datenverarbeitungszentren. An den Standorten von Edge-Clustern befinden sich nur Datenerfassungszentren. Jede Report Suite ist einem speziellen Datenverarbeitungscenter zugewiesen.

Die Site-Aktivitätsdaten der Kunden werden vom nächstgelegenen der sieben Edge-Cluster erfasst. Diese Daten werden dann zur Verarbeitung an ein vordefiniertes zentrales Cluster-Ziel (Oregon, Dublin oder Singapur) weitergeleitet. Die Daten des Besucherprofils werden im Edge Cluster gespeichert, der der Besucherin oder dem Besucher der Website am nächsten ist. Die Standorte der Edge-Cluster umfassen die Standorte der zentralen Cluster sowie Virginia, Mumbai, Sydney und Tokio.

Anstatt alle Targeting-Anfragen von einem einzigen Ort aus zu verarbeiten, werden die Anfragen von dem Edge-Cluster verarbeitet, der dem Besucher am nächsten ist. Dieser Ansatz verringert die Auswirkungen von Netzwerk- und Internet-Reisezeiten.

![Karte mit den verschiedenen Typen von Target-Servern](/help/main/c-intro/assets/target-servers.png)

Zentrale [!DNL Target]-Cluster, gehostet auf Amazon Web Services (AWS):

* Oregon, USA
* Dublin, Irland
* Republik Singapur

[!DNL Target]-Edge-Cluster, gehostet auf AWS:

* Mumbai, Indien
* Tokio, Japan
* Virginia, USA
* Oregon, USA
* Sydney, Australien
* Dublin, Irland
* Republik Singapur

Der [!DNL Target Recommendations]-Service wird in einem Rechenzentrum von [!DNL Adobe] in Oregon gehostet.

>[!IMPORTANT]
>
>[!DNL Target] fehlt derzeit ein Edge-Cluster in China, was die Besucherleistung für [!DNL Target] Kunden in der Region einschränkt. Die Firewall und das Fehlen von Edge-Clustern können Site-Erlebnisse beeinträchtigen und zu langsamen Rendering- und Seitenladezeiten führen. Darüber hinaus kann es bei Marketing-Experten zu Latenzen kommen, wenn sie die [!DNL Target] Authoring-Benutzeroberfläche verwenden.

Gegebenenfalls können Sie [!DNL Target]-Edge-Cluster aber auf Zulassungslisten setzen. Weitere Informationen finden Sie unter [Target-Edge-Knoten auf Zulassungslisten setzen](https://experienceleague.adobe.com/de/docs/target-dev/developer/implementation/privacy/allowlist-edges){target=_blank}.

## Geschütztes Benutzererlebnis {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe] stellt sicher, dass die Verfügbarkeit und Performance der Targeting-Infrastruktur so zuverlässig wie möglich ist. Kommunikationsstörungen zwischen dem Browser eines Besuchers und [!DNL Adobe] Servern können jedoch die Inhaltsbereitstellung unterbrechen.

Zum Schutz vor Dienstunterbrechungen und Verbindungsproblemen werden an allen Standorten vom Kunden definierte Standardinhalte gespeichert. Dieser Standardinhalt wird angezeigt, wenn der Browser eines Besuchers keine Verbindung zu [!DNL Target] herstellen kann.

An der Seite werden keine Änderungen vorgenommen, wenn der Browser des Besuchers innerhalb eines definierten Timeout-Zeitraums keine Verbindung herstellen kann (Standard: 15 Sekunden). Wenn diese Timeout-Frist erreicht ist, wird der Standardinhalt angezeigt.

[!DNL Adobe] schützt das Benutzererlebnis durch die Optimierung und Sicherung der Performance.

* [!DNL Adobe] stellt Leistungsbenchmarks auf der Grundlage von Branchenstandards sicher, die von der [!UICONTROL Adobe Service Level Agreement] garantiert werden.
* Das Edge-Netzwerk stellt eine rechtzeitige Datenbereitstellung sicher.
* [!UICONTROL Adobe] setzt einen mehrstufigen Ansatz zur Sicherung seiner Anwendungen ein, der Kunden ein Höchstmaß an Verfügbarkeit und Zuverlässigkeit bietet.
* [!DNL Target] Consulting bietet Unterstützung bei der Implementierung und laufenden Produktsupport.

## Benutzerfreundliches Testen der Suchmaschinenoptimierung (SEO) {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] ist an den Suchoptimierungsrichtlinien für Tests ausgerichtet. [!DNL Google] fördert Benutzertests und erklärt, dass A/B und [!UICONTROL Multivariate Testing] das organische Suchmaschinenranking nicht beeinträchtigen, wenn bestimmte Richtlinien eingehalten werden.

[!DNL Adobe Target] ist an den Suchoptimierungsrichtlinien für Prüfungen ausgerichtet.

Weitere Informationen finden Sie unter folgenden Google-Ressourcen:

* [Website-Tests und Google-Suche](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Experimente und Maskierung](https://support.google.com/analytics/answer/12979939?hl)


Die Richtlinien wurden in einem Beitrag auf dem [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) veröffentlicht. Obwohl dieser Beitrag aus dem Jahr 2012 stammt, ist er [!DNL Google] aktuellste Stellungnahme zu diesem Thema und die Leitlinien sind nach wie vor gültig.

* **Kein Cloaking**: Beim Cloaking (Maskierung) wird dem Benutzer eine Variante des Inhalts angezeigt, Suchmaschinenbots jedoch eine völlig andere Variante. Hierzu werden Bots identifiziert und mit unterschiedlichen Inhalten versorgt.

  [!DNL Target] ist so konfiguriert, dass Suchmaschinenbots wie normale Benutzer behandelt werden. Daher können Bots in Aktivitäten eingeschlossen werden, wenn sie zufällig ausgewählt werden und die Testvarianzen „sehen“.

* **Verwenden von rel=„canonical“**: Gelegentlich sind für einen A/B-Test unterschiedliche URLs für Varianten erforderlich. In diesen Fällen sollten alle Varianzen das Tag rel=„canonical“ enthalten, das auf die ursprüngliche (Kontroll-)URL verweist. Wenn [!DNL Adobe] beispielsweise die Startseite mit verschiedenen URLs für jede Variante testet, sollte das folgende kanonische Tag für die Startseite im `<head>`-Tag jeder Variante platziert werden:

  `<link rel="canonical" href="https://www.adobe.com" />`

* **Verwendung von 302-Umleitungen (temporär**: Wenn für Varianz-Seiten eines Tests separate URLs verwendet werden, empfiehlt [!DNL Google] die Verwendung einer 302-Umleitung, um Traffic an die Testvarianzen umzuleiten. Die 302-Umleitung informiert Suchmaschinen darüber, dass die Umleitung temporär und nur während des Tests aktiv ist.

  Eine 302-Umleitung ist eine Server-seitige Umleitung, während [!DNL Target] und die meisten Optimierungsanbieter Client-seitige Funktionen verwenden. Daher ist [!DNL Target] nicht vollständig konform mit den Weiterleitungsempfehlungen von [!DNL Google]. Dies wirkt sich jedoch nur auf einen Bruchteil der Tests aus. Beim Standardansatz der Testdurchführung mit [!DNL Target] werden Inhalte innerhalb einer einzigen URL geändert, sodass keine Umleitungen mehr erforderlich sind. Wenn für Testvarianzen mehrere URLs erforderlich sind, verwendet [!DNL Target] den JavaScript-`window.location`, der nicht angibt, ob es sich um eine 301- oder 302-Umleitung handelt.

  [!DNL Adobe] sucht aktiv nach Lösungen, die den Suchmaschinenrichtlinien vollständig entsprechen. Für Kunden, die separate URLs für Tests benötigen, ist [!DNL Adobe] der Ansicht, dass die korrekte Implementierung kanonischer Tags die damit verbundenen Risiken mindert.

* **Führen Sie Experimente nur so lange wie nötig durch**: [!DNL Adobe] definiert „so lange wie nötig“ als die Zeit, die zum Erreichen der statistischen Signifikanz erforderlich ist. [!DNL Target] bietet Best Practices und den [!DNL Adobe Target]Rechner [Stichprobengröße](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6), um zu bestimmen, wann Ihr Test diesen Punkt erreicht hat. [!DNL Adobe] empfiehlt, die hart codierte Implementierung erfolgreicher Tests in Ihren Test-Workflow einzubinden und die entsprechenden Ressourcen zuzuweisen.

  Die „Veröffentlichung“ erfolgreicher Tests mit [!DNL Target] wird nicht als dauerhafte Lösung empfohlen. Wenn der erfolgreichste Test für 100 % der Benutzer ständig veröffentlicht wird, kann dieser Ansatz vorübergehend verwendet werden, während der erfolgreichste Test hartcodiert wird.

  Beachten Sie, was sich durch Ihren Test geändert hat. Geringfügige Aktualisierungen wie Schaltflächenfarben wirken sich nicht auf die organischen Rangfolgen aus. Textänderungen sollten jedoch hartcodiert sein.

  Betrachten Sie auch die Barrierefreiheit der Seite, die Sie testen. Wenn die Seite für Suchmaschinen nicht zugänglich ist und nie für eine organische Suche vorgesehen war, gelten diese Überlegungen nicht. Ein Beispiel wäre eine dedizierte Landingpage für eine E-Mail-Kampagne.

Laut Google wirken sich Tests beim Befolgen der Richtlinien nicht oder nur geringfügig auf das Trefferranking Ihrer Site aus.

Zusätzlich zu diesen Richtlinien stellt Google eine weitere Richtlinie in der Dokumentation für das Werkzeug für Inhaltstests bereit:

* „Die Seitenvarianzen sollten dem Inhalt Ihrer Originalseiten ähnlich sein. Die Varianzen sollten die allgemeine Wahrnehmung der ursprünglichen Inhalte durch die Benutzer nicht ändern.“

Als Beispiel gibt Google an: „Wenn eine Originalseite voller Keywords ist, die nicht den für die Benutzer verfügbaren Inhalten entsprechen, kann diese Seite aus unserem Index entfernt werden.“

[!UICONTROL Adobe] ist der Ansicht, dass eine unbeabsichtigte Änderung der Bedeutung des ursprünglichen Inhalts in Testvarianzen kaum möglich ist. [!UICONTROL Adobe] empfiehlt jedoch, sich der Keyword-Themen auf einer Seite bewusst zu sein und diese Themen zu pflegen. Änderungen am Seiteninhalt, besonders das Löschen oder Hinzufügen relevanter Keywords, kann dazu führen, dass sich das organische Ranking der Seite ändert. [!DNL Adobe] empfiehlt, den SEO-Partner in den Testvorgang einzubeziehen.

## Bots {#bots}

[!DNL Target] verwendet die [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/)-Metrik „isRobot“ zur Erkennung bekannter Bots anhand der im Anforderungsheader übergebenen Benutzeragenten-Zeichenfolge.

>[!NOTE]
>
> Bei [!DNL Server-Side] Anforderungen hat der im [Kontextknoten der Anforderung](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) übergebene Wert eine höhere Priorität als die für die Bot-Erkennung verwendete Benutzeragenten-Zeichenfolge.

Als Bot-generiert identifizierter Traffic wird weiterhin als Inhalt bereitgestellt. Um sicherzustellen, dass [!DNL Target] den SEO-Richtlinien entspricht, werden Bots wie reguläre Benutzer behandelt. Bot-Traffic kann jedoch A/B-Tests oder Personalisierungsalgorithmen verfälschen, wenn er wie normale Benutzer behandelt wird. Daher wird der bekannte Bot-Traffic in Ihrer [!DNL Target] anders behandelt. Das Entfernen des Bot-Traffics bietet eine genauere Messung der Benutzeraktivität.

Für bekannten Bot-Traffic tut [!DNL Target] nicht:

* Ein Besucherprofil erstellen oder abrufen
* Profilattribute protokollieren oder Profilskripte ausführen
* Nach [!DNL Adobe Audience Manager] (AAM)-Segmenten suchen (falls zutreffend).
* Bot-Traffic für die Modellierung oder Bereitstellung personalisierter Inhalte für [!UICONTROL Recommendations], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] oder [!UICONTROL Auto-Allocate] Aktivitäten verwenden
* Einen Aktivitätsbesuch für Berichte erfassen
* Daten für die Weitergabe an die [!DNL Adobe Experience Cloud]-Plattform aufzeichnen

Bei bekanntem Bot-Traffic tut [!DNL Target] bei Verwendung von [!UICONTROL Analytics for Target] (A4T) Folgendes nicht:

* Ereignisse an [!DNL Analytics] senden

Für bekannten Bot-Traffic gibt [!DNL Target] bei Verwendung der `client_side`-Protokollierung Folgendes nicht zurück:

* `tnta payload`
