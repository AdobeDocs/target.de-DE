---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;Suchmaschinenoptimierung;seo;edge-Cluster, central clusters;at.js;mbox.js;
description: Erfahren Sie, wie Adobe Target funktioniert, einschließlich Informationen zu den JavaScript-Bibliotheken der Zielgruppe (at.js und AEP Web SDK), den Adobe-Rechenzentren und den SEO-Tests.
title: Wie wirkt Zielgruppe?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
translation-type: tm+mt
source-git-commit: 73053526e68e08136ab66b9d4c1aa17958cfc76e
workflow-type: tm+mt
source-wordcount: '2574'
ht-degree: 32%

---

# Funktionsweise von Adobe Target

Erfahren Sie, wie [!DNL Adobe Target] funktioniert, einschließlich Informationen zu den [!DNL Adobe Experience Platform Web SDK]- und JavaScript-Bibliotheken (at.js und mbox.js). In diesem Artikel werden auch die verschiedenen Aktivitäten vorgestellt, die Sie mit [!DNL Target] erstellen können. Sie können auch mehr über das [!DNL Target] Edge-Netzwerk, Suchmaschinenoptimierung (SEO) und wie [!DNL Target] Bots erkennt.

## Zielgruppe Platform Web SDKs und JavaScript Libraries {#libraries}

[!DNL Target] Integration mit Websites mithilfe der Bibliotheken  [!DNL AEP Web SDK] oder JavaScript:

* **Adobe Experience Platform Web SDK:** Das  [AEP Web ](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) SDK ist eine neue clientseitige JavaScript-Bibliothek. Mit dem AEP Web SDK können Kunden von [!DNL Adobe Experience Cloud] über das [!DNL AEP] Edge-Netzwerk mit den verschiedenen Diensten im [!DNL Experience Cloud] (einschließlich [!DNL Target]) interagieren. Adobe empfiehlt, dass alle neuen [!DNL Target]-Kunden [!DNL AEP Web SDK] implementieren.
* **at.js:** Die  [at.js-](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) Bibliothek ist eine Implementierungsbibliothek für  [!DNL Target]. Die „at.js“-Bibliothek sorgt für kürzere Seitenladezeiten bei Webimplementierungen und bietet bessere Implementierungsoptionen für Single-Page-Anwendungen. at.js wird häufig mit neuen Funktionen aktualisiert. Adobe empfiehlt, dass alle Kunden, die at.js verwenden, ihre Implementierungen auf die [aktuelle Version von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) aktualisieren.
* **mbox.js:**[](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) Die „mbox.js“-Bibliothek ist die alte Implementierungsbibliothek für [!DNL Target]. Die Bibliothek &quot;mbox.js&quot;wird bis zum 31. März 2021 unterstützt. Es werden jedoch keine Funktionsaktualisierungen durchgeführt.

>[!IMPORTANT]
>
>Alle Kunden sollten zur [!DNL AEP Web SDK] oder zur neuesten Version von at.js migrieren. Weitere Informationen finden Sie unter [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) oder [Migration von &quot;mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA) zu &quot;at.js&quot;.

Verweisen Sie auf jeder Seite Ihrer Site auf [!DNL AEP Web SDK] oder at.js. Sie können beispielsweise eine dieser Bibliotheken zu Ihrem globalen Header hinzufügen. Alternativ können Sie [Adobe Platform launch](https://experienceleague.adobe.com/docs/launch/using/overview.html) verwenden, um [!DNL Target] zu implementieren.

Die folgenden Ressourcen enthalten detaillierte Informationen zur Implementierung des AEP Web SDK oder at.js:

* [Adobe Experience Platform Web SDK Extension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=en#configure-the-aep-web-sdk-extension)
* [Zielgruppe mithilfe von Adobe Experience Platform Launch implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

Jedes Mal, wenn ein Besucher eine Seite anfordert, die für [!DNL Target] optimiert wurde, wird eine Anforderung an das Targeting-System gesendet. Die Anforderung hilft bei der Bestimmung der Inhalte, die für diesen Besucher bereitgestellt werden sollen. Dieser Prozess erfolgt in Echtzeit. Jedes Mal, wenn eine Seite geladen wird, wird eine Anforderung für den Inhalt vom System gesendet und erfüllt. Der Inhalt wird durch die vom Marketingspezialisten kontrollierten Aktivitäten und Erlebnisse geregelt und auf den einzelnen Besucher der Site zugeschnitten. Es werden Inhalte bereitgestellt, auf die die einzelnen Site-Besucher mit hoher Wahrscheinlichkeit reagieren, mit ihnen interagieren oder letztendlich kaufen. Personalisierter Inhalt hilft, Antwortquoten, Akquise-Raten und Umsatz zu maximieren.

In [!DNL Target] ist jedes Element auf der Seite Teil eines einzigen Erlebnisses für die gesamte Seite. Jedes Erlebnis kann mehrere Elemente auf der Seite enthalten.

Der Inhalt, der Besuchern angezeigt wird, hängt vom erstellten Aktivitätstyp ab:

### A/B-Test

Der Inhalt, der in einem einfachen A/B-Test angezeigt wird, wird zufällig aus den Erlebnissen ausgewählt, die Sie der Aktivität zuweisen. Sie können die Prozentsätze für die Traffic-Zuordnung für jedes Erlebnis zuweisen. Infolge dieser zufälligen Aufteilung des Traffics kann es einen erheblichen anfänglichen Traffic dauern, bis die Prozentsätze ausgeglichen sind. Wenn Sie beispielsweise zwei Erlebnisse erstellen, wird das Anfangserlebnis per Zufall ausgewählt. Bei wenig Traffic besteht die Möglichkeit, dass der Prozentsatz von Besuchern auf ein Erlebnis ausgerichtet wird. Mit zunehmendem Traffic gleichen sich die Prozentsätze aus.

Sie können für jedes Erlebnis prozentuale Ziele festlegen. In diesem Fall wird eine zufällige Nummer generiert und diese Nummer wird verwendet, um das anzuzeigende Erlebnis auszuwählen. Die sich ergebenden Prozentzahlen entsprechen möglicherweise nicht genau den festgelegten Zielen, allerdings bedeutet mehr Traffic, dass die Erlebnisse enger auf die beabsichtigen Ziele aufgeteilt werden sollten.

1. Ein Kunde ruft eine Seite von Ihrem Server auf und zeigt sie im Browser an.
1. Im Browser des Kunden wird ein Erstanbieter-Cookie gesetzt, um das Kundenverhalten zu speichern.
1. Die Seite ruft das Targeting-System auf.
1. Basierend auf den Regeln Ihrer Aktivität werden Inhalte angezeigt.

Weitere Informationen finden Sie unter [Erstellen eines A/B-Tests](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

### Automatische Zuordnung

Die automatisierte Zuordnung identifiziert einen Gewinner unter zwei oder mehr Erlebnissen. Bei der automatischen Zuordnung wird automatisch mehr Traffic an das erfolgreichste Erlebnis weitergeleitet, wodurch Konversionen erhöht werden, während der Test weiter ausgeführt und gelernt wird.

Weitere Informationen finden Sie unter [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

### Automatisches Targeting (AT)

Die automatische Zielgruppe nutzt fortschrittliches maschinelles Lernen, um aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen auszuwählen. Die automatische Zielgruppe bietet jedem Besucher das passendste Erlebnis. Experience Versand basiert auf individuellen Profilen und dem Verhalten früherer Besucher mit ähnlichen Profilen. Verwenden Sie die automatische Zielgruppe, um Inhalte zu personalisieren und Konvertierungen zu fördern.

Weitere Informationen finden Sie unter [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md).

### Automatisierte Personalisierung (AP)

Automated Personalization (AP) kombiniert Angebot oder Meldungen und verwendet fortschrittliches maschinelles Lernen, um verschiedenen Angebot-Variationen zu jedem Besucher zuzuordnen. Experience Versand basiert auf individuellen Profilen von Kunden, um Inhalte zu personalisieren und die Steigerung zu fördern.

Weitere Informationen finden Sie unter [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

### Erlebnis-Targeting (XT)

Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.

Erlebnis-Targeting, einschließlich Geotargeting, ermöglicht die Definition von Regeln für Erlebnisse oder Inhalte, die auf eine bestimmte Zielgruppe ausgerichtet sind. Für eine Aktivität können mehrere Regeln definiert werden, um verschiedene Inhaltsvarianten für verschiedene Zielgruppen bereitzustellen. Wenn Besucher Ihre Website aufrufen, werden sie vom Erlebnis-Targeting (XT) geprüft, um festzustellen, ob sie die von Ihnen festgelegten Kriterien erfüllen. Ist dies der Fall, treten sie in die Aktivität ein und das für die qualifizierenden Zielgruppen entworfene Erlebnis wird angezeigt. Sie können Erlebnisse für mehrere Zielgruppen innerhalb einer einzelnen Aktivität erstellen.

Weitere Informationen finden Sie unter [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4).

### Multivarianz-Tests (MVT)

Multivariate Testing (MVT) vergleicht Kombinationen von Angeboten in Elementen auf einer Seite, um festzustellen, welche Kombination für eine bestimmte Audience die beste Leistung erzielt. MVT hilft dabei herauszufinden, welches Element den Erfolg der Aktivität am meisten beeinflusst.

Weitere Informationen finden Sie unter [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

### Recommendations

Recommendations-Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten. Mit diesen Empfehlungen stellen Sie Kunden relevante Artikel vor, von denen diese andernfalls möglicherweise nichts gewusst hätten.

Weitere Informationen finden Sie unter [Empfehlungen](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0).

## Das Edge-Netzwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Ein &quot;Edge&quot;ist eine geografisch verteilte Serving-Architektur, die Besuchern, die Inhalte anfordern, optimale Reaktionszeiten gewährleistet, unabhängig davon, wo sie sich auf der ganzen Welt befinden.

Zur Verbesserung der Reaktionszeiten werden unter [!DNL Target] Kanten nur die Logik der Aktivität, zwischengespeicherte Profil und Informationen zum Angebot gehostet.

Aktivitäten- und Inhaltsdatenbanken, [!DNL Analytics]-Daten, APIs und Benutzeroberflächen von Marketingspezialisten befinden sich in den Central Clusters der Adobe. Aktualisierungen werden dann an die Kanten [!DNL Target] gesendet. Die Central-Cluster und Edge-Cluster werden automatisch synchronisiert, um die zwischengespeicherten Daten zur Aktivität kontinuierlich zu aktualisieren. Alle 1:1-Modelle werden ebenfalls an jeder Kante gespeichert, sodass diese komplexeren Anforderungen auch an der Kante verarbeitet werden können.

Jeder Edge-Cluster verfügt über alle erforderlichen Informationen, um auf die Inhaltsanforderung des Besuchers zu reagieren und Analysedaten zu dieser Anforderung zu verfolgen. Besucher-Anfragen werden an den nächsten Edge-Cluster weitergeleitet.

Weitere Informationen erhalten Sie im Whitepaper [Sicherheitsübersicht über Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

Die [!DNL Target]-Lösung wird weltweit in Rechenzentren von Adoben und Adoben gehostet.

Zentrale Clusterpositionen enthalten sowohl ein Datenerfassungscenter als auch ein Datenverarbeitungscenter. Edge-Cluster-Standorte enthalten nur ein Datenerfassungscenter. Jede Report Suite wird einem speziellen Datenverarbeitungscenter zugewiesen.

Die Daten zur Aktivität der Kunden-Site werden von den sieben Edge-Clustern erfasst, die am nächsten liegen. Diese Daten werden an den vordefinierten zentralen Cluster-Zielort eines Kunden (einer von drei Speicherorten: Oregon, Dublin, Singapur) zur Verarbeitung bestimmt. Besucher-Profil-Daten werden auf dem Edge-Cluster gespeichert, der dem Site-Besucher am nächsten liegt. Zu den Edge-Clustern gehören die Standorte Central Cluster sowie Virginia, Amsterdam, Sydney, Tokio und Hong Kong.

Anstatt auf alle Targeting-Anfragen von einem einzigen Ort zu antworten, werden Anforderungen vom Edge-Cluster verarbeitet, der dem Besucher am nächsten kommt. Dieser Prozess hilft, die Auswirkungen der Netzwerk-/Internet-Reisezeit zu mildern.

![Zuordnung der verschiedenen Typen von Zielgruppen-Servern](/help/c-intro/assets/target-servers.png)

[!DNL Target] Central-Cluster, die auf Amazon Web Services (AWS) gehostet werden, umfassen:

* Oregon, USA
* Dublin, Irland
* Republik Singapur

[!DNL Target] Edge-Cluster, die auf AWS gehostet werden, umfassen:

* Mumbai, Indien
* Tokio, Japan
* Virginia, USA
* Oregon, USA
* Sydney, Australien
* Dublin, Irland
* Republik Singapur

Der [!DNL Target Recommendations]-Dienst wird in einem [!DNL Adobe]-Rechenzentrum in Oregon gehostet.

>[!IMPORTANT]
>
>[!DNL Adobe Target] Derzeit gibt es keinen Edge Cluster in China, und die Performance des Besuchers ist für  [!DNL Target] Kunden in China weiterhin begrenzt. Aufgrund der Firewall und des Fehlens von Edge Clusters innerhalb des Landes können die Erlebnisse von Sites mit [!DNL Target] bereitgestellt werden. Erlebnisse können langsam gerendert werden, und Seitenladevorgänge können betroffen sein. Außerdem können Marketingexperten bei der Verwendung der Authoring-Benutzeroberfläche [!DNL Target] Latenzzeiten erleben.

Sie können bei Bedarf [!DNL Target] Edge-Cluster in Zulassungslisten einfügen. Weitere Informationen finden Sie unter [Edge-Knoten der Zulassungsliste-Zielgruppe](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md).

## Geschütztes Benutzererlebnis {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe stellt sicher, dass die Verfügbarkeit und Performance der Targeting-Infrastruktur so zuverlässig wie möglich ist. Eine Kommunikationsunterbrechung zwischen dem Browser eines Besuchers und den Servern der Adobe kann jedoch zu einer Unterbrechung des Content-Versands führen.

Zum Schutz vor Serviceunterbrechungen und Verbindungsproblemen sind alle Orte so eingerichtet, dass sie (vom Kunden definiert) Standardinhalte enthalten. Dieser Standardinhalt wird angezeigt, wenn der Browser des Benutzers keine Verbindung zu [!DNL Target] herstellen kann.

An der Seite werden keine Änderungen vorgenommen, wenn der Browser des Benutzers innerhalb eines festgelegten Timeout-Zeitraums (standardmäßig 15 Sekunden) keine Verbindung herstellen kann. Wenn diese Timeout-Frist erreicht ist, wird der Standardinhalt angezeigt.

Adobe schützt das Benutzererlebnis durch die Optimierung und Sicherung der Performance.

* Adobe stellt Leistungsbenchmarks auf Grundlage von Branchenstandards sicher, die durch die Dienstgütevereinbarung (Service Level Agreement, SLA) von Adobe gewährleistet werden.
* Das Edge-Netzwerk stellt eine rechtzeitige Datenbereitstellung sicher.
* Adobe setzt einen mehrstufigen Ansatz zur Sicherung seiner Anwendungen ein, um Kunden auf diese Weise ein Höchstmaß an Verfügbarkeit und Zuverlässigkeit zu gewähren.
* [!DNL Target] Consulting bietet Unterstützung bei der Implementierung und laufenden Produktsupport.

## Benutzerfreundliches Testen der Suchmaschinenoptimierung (SEO){#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] ist an den Suchoptimierungsrichtlinien für Prüfungen ausgerichtet.

Google fördert Benutzertests. Google erklärt in seiner Dokumentation, dass A/B und Multivariate Testing organische Suchmaschinenrankings nicht beeinträchtigen, wenn Sie bestimmte Richtlinien befolgen.

Weitere Informationen finden Sie unter folgenden Google-Ressourcen:

* [Website-Tests und Google-Suche](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Experimente und Maskierung](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

Die Richtlinien wurden in einem Beitrag auf dem [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) veröffentlicht. Obwohl dieser Beitrag aus dem Jahr 2012 stammt, ist er die aktuellste Stellungnahme von Google zu diesem Thema und die Richtlinien sind nach wie vor gültig.

* **Kein Verschließen**: Beim Cloaking wird Ihren Benutzern eine Reihe von Inhalten und Suchmaschinen-Bots andere Inhalte angezeigt. Das Schließen erfolgt durch die spezifische Identifizierung von Bots und die gezielte Fütterung unterschiedlicher Inhalte.

   [!DNL Target] wurde als Plattform so entworfen, dass Bots von Suchmaschinen genau wie normale Benutzer behandelt werden. Daher können Bots in Aktivitäten eingeschlossen werden, wenn die Bots zufällig ausgewählt sind und die Testvarianten &quot;angezeigt&quot;werden.

* **Verwenden Sie rel=&quot;canonical&quot;**: Manchmal muss ein A/B-Test mit unterschiedlichen URLs für die Variationen eingerichtet werden. In diesen Fällen sollten alle Variationen das Tag `rel="canonical"` enthalten, das auf die ursprüngliche (Kontroll-)URL verweist. Angenommen, die Adobe testet ihre Startseite unter Verwendung unterschiedlicher URLs für jede Variante. Das folgende kanonische Tag für die Startseite würde im `<head>`-Tag für jede der Variationen eingefügt:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Verwenden Sie 302 (temporäre) Umleitungen**: In Fällen, in denen für die Variantenseiten in einem Test separate URLs verwendet werden, empfiehlt Google die Verwendung einer 302-Umleitung, um den Traffic in die Testvarianten zu leiten. Die 302-Umleitung teilt den Suchmaschinen mit, dass die Umleitung vorübergehend ist und nur aktiv ist, solange der Test ausgeführt wird.

   Eine 302-Umleitung ist eine serverseitige Umleitung, und [!DNL Target] und die meisten Optimierungsanbieter nutzen clientseitige Funktionen. Daher ist die Weiterleitung ein Bereich, in dem [!DNL Target] nicht vollständig mit den Empfehlungen von Google übereinstimmt. Diese Praxis betrifft jedoch nur einen kleinen Teil der Tests. Der Standardansatz zum Ausführen von Tests mit [!DNL Target] ruft zum Ändern von Inhalten innerhalb einer einzelnen URL auf, sodass keine Umleitungen erforderlich sind. Es gibt Fälle, in denen Kunden mehrere URLs verwenden müssen, um ihre Testvarianten darzustellen. In diesen Fällen verwendet [!DNL Target] den JavaScript-Befehl `window.location`. Mit diesem Befehl werden Benutzer zu Testvarianten weitergeleitet, was nicht explizit bedeutet, dass die Umleitung 301 oder 302 beträgt.

   Die Adobe sucht nach praktikablen Lösungen, die vollständig mit den Richtlinien der Suchmaschinen übereinstimmen. Für Kunden, die separate URLs zum Testen verwenden müssen, ist die Adobe zuversichtlich, dass eine ordnungsgemäße Implementierung der kanonischen Tags das mit diesem Ansatz verbundene Risiko verringert.

* **Experimente nur so lange wie nötig** ausführen: Die Adobe hält &quot;so lange wie nötig&quot;für notwendig, bis sie statistische Bedeutung erlangt. [!DNL Target][Es stehen in Best Practices](https://docs.adobe.com/content/target-microsite/testcalculator.html) zur Verfügung, mit deren Hilfe festgestellt werden kann, wann Ihr Test diesen Punkt erreicht hat. Adobe empfiehlt, dass Sie die hartcodierte Implementierung erfolgreicher Tests in Ihren Testarbeitsablauf integrieren und die entsprechenden Ressourcen zuweisen.

   Die Verwendung der [!DNL Target]-Plattform zum &quot;Veröffentlichen&quot;erfolgreicher Tests wird nicht als dauerhafte Lösung empfohlen. Wenn der Gewinner-Test für 100 % der Benutzer zu 100 % veröffentlicht wird, kann dieser Ansatz verwendet werden, während der Prozess der Hartkodierung des Gewinner-Tests abgeschlossen ist.

   Beachten Sie dabei auch, was durch Ihren Test geändert wurde. Die einfache Aktualisierung der Farbe von Schaltflächen oder anderen kleineren, nicht textbasierten Elementen auf der Seite hat keinen Einfluss auf Ihre organische Rangordnung. Änderungen an Texten sollten jedoch auf jeden Fall hartcodiert werden.

   Berücksichtigen Sie außerdem, wie einfach auf die zu testende Seite zugegriffen werden kann. Wenn die Seite nicht für Suchmaschinen zugänglich ist und überhaupt nicht für die organische Suche entwickelt wurde, dann gelten keine der obigen Erwägungen. Ein Beispiel ist eine dedizierte Landingpage für eine E-Mail-Kampagne.

Laut Google wirken sich Tests beim Befolgen der Richtlinien nicht oder nur geringfügig auf das Trefferranking Ihrer Site aus.

Zusätzlich zu diesen Richtlinien stellt Google eine weitere Richtlinie in der Dokumentation für das Werkzeug für Inhaltstests bereit:

* „Die Seitenvariationen sollten dem Inhalt Ihrer Originalseiten ähnlich sein. Die Variationen sollten die allgemeine Wahrnehmung der ursprünglichen Inhalte durch die Benutzer nicht ändern.“

Als Beispiel gibt Google an: „Wenn eine Originalseite voller Schlüsselwörter ist, die nicht den für die Benutzer verfügbaren Inhalten entsprechen, kann diese Seite aus unserem Index entfernt werden.“

Adobe ist der Ansicht, dass es schwierig wäre, die Bedeutung des Originalinhalts in Testvarianten unbeabsichtigt zu ändern. Adobe empfiehlt jedoch, sich der Themen der Suchbegriffe auf einer Seite bewusst zu sein und diese Themen zu pflegen. Änderungen am Seiteninhalt, besonders das Löschen oder Hinzufügen relevanter Schlüsselwörter, kann dazu führen, dass sich das organische Ranking der Seite ändert. Adobe empfiehlt, dass Sie sich im Rahmen Ihres Testprotokolls mit Ihrem SEO-Partner in Verbindung setzen.

## Bots {#bots}

Adobe [!DNL Target] verwendet die Metrik [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) &quot;isRobot&quot;, um bekannte Bots basierend auf der Benutzeragenten-Zeichenfolge zu erkennen, die im Anforderungs-Header übergeben wird.

>[!NOTE]
>
> Bei Anforderungen von [!DNL Server-Side] erhält der Wert, der im Knoten [Anforderung &quot;Kontext&quot;](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) übergeben wird, Vorrang vor der Benutzeragenten-Zeichenfolge für die Bot-Erkennung.

Traffic, der als von einem Bot generiert identifiziert wird, wird weiterhin mit Inhalten bereitgestellt. Bots werden wie normale Benutzer behandelt, um sicherzustellen, dass [!DNL Target] den SEO-Richtlinien entspricht. Die Verwendung von Bot-Traffic kann A/B-Tests oder Personalisierungsalgorithmen verfälschen, wenn Bots wie normale Benutzer behandelt werden. Wenn daher ein bekannter Bot in Ihrer [!DNL Target]-Aktivität erkannt wird, wird der Traffic geringfügig anders behandelt. Durch das Entfernen des Bot-Traffics erhalten Sie eine korrektere Messung der Benutzeraktivität.

Insbesondere für den bekannten Bot-Traffic [!DNL Target] nicht:

* Ein Besucherprofil erstellen oder abrufen
* Profilattribute erfassen oder Profilskripte ausführen
* Nach Adobe Audience Manager (AAM)-Segmenten suchen (falls zutreffend).
* Verwenden Sie Bot-Traffic bei der Modellierung und Bereitstellung personalisierter Inhalte für Recommendations-, Auto-Zielgruppe-, Automated Personalization- oder Auto-Allokation-Aktivitäten
* Einen Aktivitätsbesuch für Berichte erfassen
* An die [!DNL Adobe Experience Cloud]-Plattform zu sendende Protokolldaten
