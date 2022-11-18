---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;Suchmaschinenoptimierung;seo;Edge-Cluster;zentrale Cluster;at.js;mbox.js;
description: Erfahren Sie, wie  [!DNL Adobe Target]  funktioniert, einschließlich Informationen zu JavaScript-Bibliotheken (AEP Web SDK „at.js“), Adobe-Rechenzentren, SEO-Tests und Bots.
title: Wie funktioniert  [!DNL Target] ?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: 4564e0b95bbd19f20c75e5e83d452d12a5403083
workflow-type: ht
source-wordcount: '2583'
ht-degree: 100%

---

# Funktionsweise von [!DNL Adobe Target]

Erfahren Sie, wie [!DNL Adobe Target] funktioniert, einschließlich Informationen zu den JavaScript-Bibliotheken ([!DNL Adobe Experience Platform Web SDK] und „at.js“). In diesem Artikel werden auch die Arten von Aktivitäten vorgestellt, die Sie mit [!DNL Target] erstellen können. Auch erhalten Sie hier Informationen zum [!DNL Target]-Edge-Netzwerk, zur Suchmaschinenoptimierung (SEO) und zur Erkennung von Bots durch [!DNL Target].

## [!DNL Adobe Target] JavaScript-Bibliotheken {#libraries}

[!DNL Target] lässt sich mithilfe von [!DNL Experience Platform Web SDK] oder „at.js“ in Websites integrieren:

* **[!DNL Adobe Experience Platform Web SDK]:** Das [Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank} ist eine neue Client-seitige JavaScript-Bibliothek. Das [!DNL Experience Platform Web SDK] ermöglicht Kunden von [!DNL Adobe Experience Cloud] die Interaktion mit den verschiedenen Services in [!DNL Experience Cloud] (einschließlich [!DNL Target]) über das [!DNL Experience Platform] Edge Network. [!DNL Adobe] empfiehlt allen neuen [!DNL Target]-Kunden, das [!DNL Experience Platform Web SDK] zu implementieren.
* **at.js:** Die at.js-Bibliothek ist eine Implementierungsbibliothek für [!DNL Target]. Die at.js-Bibliothek sorgt für kürzere Seitenladezeiten bei Web-Implementierungen und bietet bessere Implementierungsoptionen für Single-Page-Anwendungen. At.js wird häufig durch neue Funktionen erweitert. [!DNL Adobe] empfiehlt allen Kunden, die at.js verwenden, ihre Implementierungen auf die [neueste Version von at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} zu aktualisieren.

>[!NOTE]
>
>Die Bibliothek „mbox.js“ ist eine veraltete Implementierungsbibliothek für [!DNL Target]. Die mbox.js-Bibliothek wird nach dem 31. März 2021 nicht mehr unterstützt. Aktualisieren Sie auf das Experience Platform Web SDK (empfohlen) oder auf die neueste Version von „at.js“.

Das [!DNL Experience Platform Web SDK] oder at.js muss auf jeder Seite Ihrer Site referenziert werden. Beispielsweise können Sie eine dieser Bibliotheken Ihrer globalen Kopfzeile hinzufügen. Alternativ können Sie [Tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de) verwenden, um [!DNL Target] zu implementieren.

Die folgenden Ressourcen enthalten detaillierte Informationen zur Implementierung von [!DNL Experience Platform Web SDK] oder „at.js“:

* [[!DNL Adobe Experience Platform Web SDK] Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=de)
* [Implementieren von  [!DNL Target]  mithilfe von  [!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/)

Bei jeder Besucheranforderung einer Seite, die für [!DNL Target] optimiert wurde, wird eine Anforderung an das Targeting-System gesendet. Die Anforderung hilft bei der Bestimmung der Inhalte, die für diesen Besucher bereitgestellt werden sollen. Dieser Prozess erfolgt in Echtzeit. Jedes Mal, wenn eine Seite geladen wird, wird eine Inhaltsanforderung gesendet, die vom System verarbeitet wird. Der Inhalt wird durch die vom Marketingspezialisten kontrollierten Aktivitäten und Erlebnisse geregelt und auf den einzelnen Besucher der Site zugeschnitten. Es werden Inhalte bereitgestellt, auf die der Site-Besucher mit hoher Wahrscheinlichkeit reagieren und mit ihnen interagieren wird und auf deren Grundlage er sich letztlich auch für einen Kauf entscheiden wird. Personalisierte Inhalte tragen dazu bei, die Antwort- und Kaufraten zu steigern und die Umsätze zu maximieren.

In [!DNL Target] ist jedes Seitenelement Bestandteil eines einheitlichen Erlebnisses, das durch die gesamte Seite bereitgestellt wird. Jedes Erlebnis kann mehrere Seitenelemente umfassen.

Der Inhalt, der Besuchern angezeigt wird, hängt vom erstellten Aktivitätstyp ab:

### [!UICONTROL A/B-Test]

Die in einem grundlegenden A/B-Test angezeigten Inhalte werden zufällig aus den der Aktivität zugewiesenen Erlebnissen ausgewählt. Die Prozentsätze der Traffic-Zuordnungen für jedes Erlebnis können Sie selbst zuteilen. Als Folge dieser zufälligen Traffic-Aufteilung kann bis zum Erreichen der Prozentwerte ein sehr großes Traffic-Aufkommen erforderlich sein. Wenn Sie beispielsweise zwei Erlebnisse erstellen, wird das Anfangserlebnis per Zufall ausgewählt. Bei wenig Traffic besteht die Möglichkeit, dass der Prozentsatz von Besuchern auf ein Erlebnis ausgerichtet wird. Mit zunehmendem Traffic gleichen sich die Prozentsätze aus.

Sie können für jedes Erlebnis prozentuale Ziele festlegen. In diesem Fall wird eine zufällige Nummer generiert und diese Nummer wird verwendet, um das anzuzeigende Erlebnis auszuwählen. Die sich ergebenden Prozentzahlen entsprechen möglicherweise nicht genau den festgelegten Zielen, allerdings bedeutet mehr Traffic, dass die Erlebnisse enger auf die beabsichtigen Ziele aufgeteilt werden sollten.

1. Ein Kunde ruft eine Seite von Ihrem Server auf und zeigt sie im Browser an.
1. Zum Speichern des Kundenverhaltens wird im Browser des Benutzers ein Erstanbieter-Cookie gesetzt.
1. Die Seite ruft das Targeting-System auf.
1. Basierend auf den Regeln Ihrer Aktivität werden Inhalte angezeigt.

Weitere Informationen finden Sie unter [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

### [!UICONTROL Automatische Zuordnung]

Durch die [!UICONTROL automatische Zuordnung] kann aus zwei oder mehr Erlebnissen das erfolgversprechendste ermittelt werden. [!UICONTROL Die automatische Zuordnung] ordnet automatisch dem erfolgreichsten Erlebnis mehr Traffic zu, wodurch sich die Konversionen während der Fortführung des Tests und des Lernens erhöhen.

Weitere Informationen finden Sie unter [[!UICONTROL Automatische Zuordnung]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

### [!UICONTROL Automatisches Targeting] (AT)

[!UICONTROL Automatisches Targeting (AT)] nutzt fortschrittliche Machine Learning-Algorithmen zur Auswahl eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen. Dabei stellt [!UICONTROL automatisches Targeting] jedem Besucher das passendste Erlebnis bereit. Die Bereitstellung des Erlebnisses basiert auf den Profilen der jeweiligen Kunden sowie dem Verhalten früherer Besucher mit ähnlichen Profilen. Verwenden Sie [!UICONTROL automatisches Targeting] zur Personalisierung Ihrer Inhalte und letztlich zur Steigerung Ihrer Konversionen.

Weitere Informationen finden Sie unter [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

### [!UICONTROL Automatisierte Personalisierung] (AP)

[!UICONTROL Automated Personalization] (AP) kombiniert Angebote und Nachrichten und ordnet den einzelnen Besucher/innen durch fortschrittliche Algorithmen für maschinelles Lernen verschiedene Varianten zu. Die Bereitstellung der personalisierten Inhalte basiert auf den Profilen der jeweiligen Kunden und führt dadurch zur Steigerung der Konversionsraten.

Weitere Informationen finden Sie unter [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

### [!UICONTROL Erlebnis-Targeting] (XT)

Beim [!UICONTROL Experience Targeting] (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus Regeln und Kriterien, die von den Werbungtreibenden definiert werden, bereitgestellt.

[!UICONTROL Erlebnis-Targeting], einschließlich Geotargeting, ermöglicht die Definition von Regeln für Erlebnisse oder Inhalte, die auf eine bestimmte Zielgruppe ausgerichtet sind. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen. Wenn Personen Ihre Website aufrufen, werden sie vom [!UICONTROL Experience Targeting] (XT) ausgewertet, um festzustellen, ob sie die von Ihnen festgelegten Kriterien erfüllen. Ist dies der Fall, treten sie in die Aktivität ein und das für die qualifizierenden Zielgruppen entworfene Erlebnis wird angezeigt. Sie können Erlebnisse für mehrere Zielgruppen innerhalb einer einzelnen Aktivität erstellen.

Weitere Informationen finden Sie unter [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4).

### [!UICONTROL Multivariate Tests] (MVT)

[!UICONTROL Multivariate Tests] (MVT) vergleichen verschiedene Kombinationen aus den Angeboten für die Elemente einer Seite, um zu bestimmen, welche Kombination für eine spezielle Zielgruppe die besten Ergebnisse erzielt. MVT ermittelt also, welches Element den größten Einfluss auf den Erfolg der Aktivität hat.

Weitere Informationen finden Sie unter [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

### [!UICONTROL Recommendations]

[!UICONTROL Recommendations]-Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten. Recommendations tragen dazu bei, Kundinnen und Kunden zu relevanten Elementen zu lenken, von denen sie andernfalls möglicherweise nichts wüssten.

Weitere Informationen finden Sie unter [Recommendations](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0).

## Das Edge-Netzwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Ein „Edge“ ist eine geografisch verteilte Server-Architektur, die Besuchenden die angeforderten Inhalte bei optimalen Reaktionszeiten bereitstellt, unabhängig davon, wo auf der Welt sie sich befinden.

Zur Verbesserung der Reaktionszeiten werden auf [!DNL Target]-Edges nur Aktivitätslogik, zwischengespeicherte Profile und Angebotsinformationen gehostet.

Die Aktivitäts- und Inhaltsdatenbanken, [!DNL Analytics]-Daten, APIs und die Benutzeroberflächen der Werbungtreibenden werden in den zentralen Clustern von Adobe gespeichert. Aktualisierungen werden an die [!DNL Target]-Edges gesendet. Die zentralen und die Edge-Cluster werden automatisch synchronisiert, damit die zwischengespeicherten Aktivitätsdaten immer aktuell sind. Außerdem werden an allen Edges sämtliche 1:1-Modelle gespeichert, weshalb auch diese komplexeren Anforderungen am Edge verarbeitet werden können.

Jeder Edge-Cluster verfügt über alle Informationen zur Beantwortung der Inhaltsanforderungen der Besucher und zur Nachverfolgung der Analysedaten zu einer Anforderung. Die Besucheranforderungen werden an den nächstgelegenen Edge-Cluster weitergeleitet.

Weitere Informationen erhalten Sie im Whitepaper [Sicherheitsübersicht über Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

Die [!DNL Target]-Lösung wird weltweit auf Adobe-eigenen und von Adobe geleasten Rechenzentren gehostet.

An den Standorten zentraler Cluster befinden sich sowohl ein Datenerfassungscenter als auch ein Datenverarbeitungscenter. An Edge-Cluster-Standorten befindet sich dagegen nur ein Datenerfassungscenter. Jede Report Suite ist einem speziellen Datenverarbeitungscenter zugewiesen.

Die Site-Aktivitätsdaten der Kunden werden vom nächstgelegenen der sieben Edge-Cluster erfasst. Diese Daten werden zur Verarbeitung an das vorbestimmte zentrale Cluster-Ziel je nach Kunde weitergeleitet (einer der drei Standorte: Oregon, Dublin, Singapur). Die Profildaten der Besucher werden in dem Edge-Cluster gespeichert, der dem Site-Besucher am nächsten liegt. Die Standorte der Edge-Cluster umfassen die Standorte der zentralen Cluster sowie Virginia, Mumbai, Sydney und Tokio.

Die Targeting-Anforderungen werden nicht immer vom gleichen Standort beantwortet, sondern von dem Edge-Cluster, der dem Besucher am nächsten liegt. Dadurch minimieren sich die Verzögerungen durch lange Übertragungswege innerhalb des Netzwerks bzw. Internets.

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
>[!DNL Adobe Target] stellt derzeit keinen Edge-Cluster in China bereit. Für [!DNL Target]-Kunden in China ist die Leistung daher weiterhin eingeschränkt. Aufgrund der Firewall und des Mangels an Edge-Clustern innerhalb des Landes können die Erlebnisse auf Sites, auf denen [!DNL Target] implementiert ist, beeinträchtigt sein. Die Erlebnisse werden eventuell nur langsam gerendert und Seitenladevorgänge können beeinträchtigt sein. Auch Marketer bemerken bei Verwendung der Authoring-Benutzeroberfläche von [!DNL Target] eventuell Latenzen.

Gegebenenfalls können Sie [!DNL Target]-Edge-Cluster aber auf Zulassungslisten setzen. Weitere Informationen finden Sie unter [Target-Edge-Knoten auf die Zulassungsliste setzen](https://developer.adobe.com/target/before-implement/privacy/allowlist-edges/){target=_blank}.

## Geschütztes Benutzererlebnis {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe] stellt sicher, dass die Verfügbarkeit und Performance der Targeting-Infrastruktur so zuverlässig wie möglich ist. Allerdings kann es durch einen Ausfall der Kommunikation zwischen dem Browser eines Besuchers und den Servern von [!DNL Adobe] zu einer Unterbrechung der Inhaltsbereitstellung kommen.

Zum Schutz vor Dienstunterbrechungen und Verbindungsproblemen werden an allen Standorten vom Kunden definierte Standardinhalte gespeichert. Dieser Standardinhalt wird angezeigt, wenn der Browser eines Benutzers keine Verbindung zu [!DNL Target] herstellen kann.

An der Seite werden keine Änderungen vorgenommen, wenn der Browser des Benutzers innerhalb eines festgelegten Timeout-Zeitraums (standardmäßig 15 Sekunden) keine Verbindung herstellen kann. Wenn diese Timeout-Frist erreicht ist, wird der Standardinhalt angezeigt.

[!DNL Adobe] schützt das Benutzererlebnis durch die Optimierung und Sicherung der Performance.

* [!DNL Adobe] stellt Leistungsbenchmarks auf Grundlage von Branchenstandards sicher, die durch die Dienstgütevereinbarung (Service Level Agreement, SLA) von Adobe gewährleistet werden.
* Das Edge-Netzwerk stellt eine rechtzeitige Datenbereitstellung sicher.
* [!UICONTROL Adobe] setzt einen mehrstufigen Ansatz zur Sicherung seiner Anwendungen ein, um Kunden auf diese Weise ein Höchstmaß an Verfügbarkeit und Zuverlässigkeit zu gewähren.
* [!DNL Target] Consulting bietet Unterstützung bei der Implementierung und laufenden Produktsupport.

## Benutzerfreundliches Testen der Suchmaschinenoptimierung (SEO) {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] ist an den Suchoptimierungsrichtlinien für Prüfungen ausgerichtet.

Google unterstützt Benutzertests. In seiner Dokumentation erklärt Google, dass A/B-Tests und [!UICONTROL Multivariate Tests] das organische Suchmaschinen-Ranking nicht beeinträchtigen, wenn bestimmte Richtlinien eingehalten werden.

Weitere Informationen finden Sie unter folgenden Google-Ressourcen:

* [Website-Tests und Google-Suche](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Experimente und Maskierung](https://support.google.com/analytics/answer/2576845?hl=de&amp;ref_topic=1745207)

Die Richtlinien wurden in einem Beitrag auf dem [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) veröffentlicht. Obwohl dieser Beitrag aus dem Jahr 2012 stammt, ist er die aktuellste Stellungnahme von Google zu diesem Thema und die Richtlinien sind nach wie vor gültig.

* **Kein Cloaking**: Beim Cloaking (Maskierung) wird dem Benutzer eine Variante des Inhalts angezeigt, Suchmaschinenbots jedoch eine völlig andere Variante. Cloaking beabsichtigt die explizite Identifizierung von Bots und das gezielte Einspeisen unterschiedlicher Inhalte.

   [!DNL Target] wurde als Plattform so entwickelt, dass Suchmaschinenbots wie normale Benutzer behandelt werden. Daher können Bots in Aktivitäten eingeschlossen werden, wenn die Bots zufällig ausgewählt werden und die Testvarianzen „sehen“ können.

* **Verwendung von rel=&quot;canonical&quot;**: Gelegentlich müssen für einen A/B-Test unterschiedliche URLs für die Varianzen erstellt werden. In diesen Fällen sollten alle Varianzen das Tag `rel="canonical"` enthalten, das auf die ursprüngliche (Kontroll)-URL verweist. Angenommen, [!DNL Adobe] testet für seine Startseite unterschiedliche URLs für jede Variante. Dazu müsste das folgende kanonische Tag für die Startseite im `<head>`-Tag jeder der Varianzen eingefügt werden:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Verwendung von 302-Umleitungen (temporär)**: Wenn für einen Varianz-Test unterschiedliche URLs verwendet werden, empfiehlt Google die Verwendung einer 302-Umleitung, die Traffic an die verschiedenen Varianzen umleitet. Die 302-Umleitung teilt Suchmaschinen mit, dass die Umleitung vorübergehend und nur bis zum Abschluss des Tests aktiv ist.

   Eine 302-Umleitung ist eine serverseitige Umleitung. [!DNL Target] stützt sich aber – wie die meisten Optimierungsanbieter – auf clientseitige Funktionen. [!DNL Target] ist in diesem Fall nicht vollständig konform mit den Empfehlungen von Google. Diese Vorgehensweise wirkt sich jedoch nur auf die wenigsten Tests aus. Beim Standardansatz der Testdurchführung mit [!DNL Target] werden sich ändernde Inhalte innerhalb einer einzigen URL verwendet, sodass keine Umleitungen erforderlich sind. In manchen Fällen jedoch muss der Kunde mit mehreren URLs arbeiten, um die Varianzen testen zu können. In diesen Fällen verwendet [!DNL Target] den JavaScript-Befehl `window.location`. Dieser Befehl leitet Benutzer zu Testvarianzen um, wobei aber nicht explizit eine Aussage darüber getroffen wird, ob die Umleitung 301 oder 302 verwendet wird.

   [!DNL Adobe] sucht weiterhin nach praktikablen Lösungen, die vollständig konform mit den Suchmaschinenrichtlinien sind. [!DNL Adobe] ist zuversichtlich, dass sich das mit diesem Ansatz verbundene Risiko für alle Kunden, die mehrere URLs zum Testen verwenden müssen, durch eine ordnungsgemäße Implementierung der kanonischen Tags verringert.

* **Durchführen der Experimente nur so lange wie nötig**: Für [!DNL Adobe] bedeutet „so lange wie nötig“ genau so lange, bis ein statistisch signifikantes Ergebnis erzielt ist. [!DNL Target] bietet Best Practices und den [!DNL Adobe Target] [Rechner für den Stichprobenumfang](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6), um zu bestimmen, wann Ihr Test diesen Punkt erreicht hat. [!DNL Adobe] empfiehlt, die hart codierte Implementierung erfolgreicher Tests in Ihren Test-Workflow einzugliedern und die hierfür erforderlichen Ressourcen bereitzustellen.

   Die „Veröffentlichung“ erfolgreicher Tests über die [!DNL Target]-Plattform wird nicht als dauerhafte Lösung empfohlen. Wenn der erfolgreichste Test für 100 % der Benutzer zu 100 % veröffentlicht wird, kann dieser Ansatz verwendet werden, während der Prozess der Hartcodierung des erfolgreichsten Tests noch durchgeführt wird.

   Beachten Sie dabei auch, was durch Ihren Test geändert wurde. Eine Änderung der Schaltflächenfarbe oder anderer Elemente, die keinen Text enthalten, wirkt sich nicht auf das organische Suchmaschinenranking Ihrer Seite aus. Änderungen an Texten sollten jedoch auf jeden Fall hart codiert werden.

   Berücksichtigen Sie außerdem, wie einfach auf die zu testende Seite zugegriffen werden kann. Wenn die Seite nicht für Suchmaschinen zugänglich ist und ein Ranking in organischen Suche zuvorderst gar nicht beabsichtigt ist, brauchen Sie sich über keine der obigen Umgehungen Gedanken zu machen. Ein Beispiel wäre eine dedizierte Landingpage für eine E-Mail-Kampagne.

Laut Google wirken sich Tests beim Befolgen der Richtlinien nicht oder nur geringfügig auf das Trefferranking Ihrer Site aus.

Zusätzlich zu diesen Richtlinien stellt Google eine weitere Richtlinie in der Dokumentation für das Werkzeug für Inhaltstests bereit:

* „Die Seitenvarianzen sollten dem Inhalt Ihrer Originalseiten ähnlich sein. Die Varianzen sollten die allgemeine Wahrnehmung der ursprünglichen Inhalte durch die Benutzer nicht ändern.“

Als Beispiel gibt Google an: „Wenn eine Originalseite voller Keywords ist, die nicht den für die Benutzer verfügbaren Inhalten entsprechen, kann diese Seite aus unserem Index entfernt werden.“

[!UICONTROL Adobe] ist der Ansicht, dass eine unbeabsichtigte Änderung der Bedeutung des ursprünglichen Inhalts in Testvarianzen kaum möglich ist. [!UICONTROL Adobe] empfiehlt jedoch, sich der Keyword-Themen auf einer Seite bewusst zu sein und diese Themen zu pflegen. Änderungen am Seiteninhalt, besonders das Löschen oder Hinzufügen relevanter Keywords, kann dazu führen, dass sich das organische Ranking der Seite ändert. [!DNL Adobe] empfiehlt, den SEO-Partner in den Testvorgang einzubeziehen.

## Bots {#bots}

Adobe [!DNL Target] verwendet die [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/)-Metrik „isRobot“ zur Erkennung bekannter Bots anhand der im Anforderungsheader übergebenen Benutzeragenten-Zeichenfolge.

>[!NOTE]
>
> Bei [!DNL Server-Side] Anforderungen hat der im [Kontextknoten der Anforderung](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) übergebene Wert eine höhere Priorität als die für die Bot-Erkennung verwendete Benutzeragenten-Zeichenfolge.

Selbst Traffic, der als „von einem Bot generiert“ identifiziert wird, gilt als bereitgestellter Inhalt. Um sicherzustellen, dass [!DNL Target] den SEO-Richtlinien entspricht, werden Bots daher wie reguläre Benutzer behandelt. Wenn Bots aber wie reguläre Benutzer behandelt werden, können A/B-Tests oder Personalisierungsalgorithmen durch Bot-Traffic verfälscht werden. Wenn daher ein bekannter Bot in Ihrer [!DNL Target]-Aktivität erkannt wird, wird der Traffic geringfügig anders als regulärer Traffic behandelt. Durch das Entfernen des Bot-Traffics erhalten Sie eine korrektere Messung der Benutzeraktivität.

Insbesondere unterlässt [!DNL Target] bei Traffic, der durch bekannte Bots generiert wird, folgende Verarbeitungsschritte:

* Ein Besucherprofil erstellen oder abrufen
* Profilattribute erfassen oder Profilskripte ausführen
* Nach [!DNL Adobe Audience Manager] (AAM)-Segmenten suchen (falls zutreffend).
* Verwenden von Bot-Traffic bei der Modellierung und Bereitstellung personalisierter Inhalte für [!UICONTROL Recommendations], [!UICONTROL automatisches Targeting], [!UICONTROL Automated Personalization] oder [!UICONTROL automatische Zuordnung]
* Einen Aktivitätsbesuch für Berichte erfassen
* Daten für die Weitergabe an die [!DNL Adobe Experience Cloud]-Plattform aufzeichnen

Für bekannten Bot-Traffic tut [!DNL Target] bei Verwendung von [!UICONTROL Analytics for Target] (A4T) das Folgende nicht:

* Ereignisse an [!DNL Analytics] senden

Für bekannten Bot-Traffic gibt [!DNL Target] bei Verwendung der Client-seitigen Protokollierung das Folgende nicht zurück:

* tnta-Payload
