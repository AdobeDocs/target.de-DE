---
description: 'Adobe Target wird mithilfe einer von zwei JavaScript-Bibliotheken in Websites integriert: „at.js“ oder „mbox.js“.'
keywords: Übersicht und Referenz; SEO; Suchmaschinenoptimierung
seo-description: 'Adobe Target wird mithilfe einer von zwei JavaScript-Bibliotheken in Websites integriert: „at.js“ oder „mbox.js“.'
seo-title: Funktionsweise von Adobe Target
solution: Target
subtopic: Erste Schritte
title: Funktionsweise von Adobe Target
topic: Standard
uuid: 01c0072d-f77d-4f14-935b-8633f220db7b
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Funktionsweise von Adobe Target{#how-adobe-target-works}

Informationen darüber, wie Adobe Target funktioniert, einschließlich Informationen zu den JavaScript-Bibliotheken (at.js und mbox.js) und den verschiedenen in Target enthaltenen Aktivitätstypen.

## JavaScript-Bibliotheken in Target {#libraries}

Adobe Target wird mithilfe einer von zwei JavaScript-Bibliotheken in Websites integriert: „at.js“ oder „mbox.js“.

* **at.js:** Die [at.js-Bibliothek](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) ist die neue Implementierungsbibliothek für Target. Die „at.js“-Bibliothek sorgt für kürzere Seitenladezeiten bei Webimplementierungen und bietet bessere Implementierungsoptionen für Single-Page-Anwendungen. „at.js“ ist die empfohlene Implementierungsbibliothek und wird häufig mit neuen Funktionen aktualisiert. Wir empfehlen allen Kunden, die [neueste Version von „at.js“](../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) zu implementieren oder zu ihr zu migrieren.
* **mbox.js:** Die „mbox.js“-Bibliothek ist die alte Implementierungsbibliothek für Target. Die „mbox.js“-Bibliothek wird weiterhin unterstützt, aber es gibt keine weiteren Funktionsupdates.

>[!IMPORTANT]
>
>Alle Kunden sollten auf at.js migrieren. Weitere Informationen finden Sie unter [Migration zu at.js von mbox.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)

Sie müssen auf jeder Seite Ihrer Website auf eine der Target-JavaScript-Dateien verweisen. Sie können sie beispielsweise Ihrer globalen Kopfzeile hinzufügen.

Jedes Mal, wenn ein Besucher eine Seite aufruft, die für Target optimiert wurde, wird eine Anfrage an das Targeting-System gesendet, um festzulegen, welcher Inhalt für einen Besucher bereitgestellt werden soll. Dieser Prozess erfolgt in Echtzeit - jedes Mal, wenn eine Seite geladen wird, erfolgt eine Anfrage für den Inhalt, die durch das System verarbeitet wird. Der Inhalt wird durch die vom Marketingspezialisten kontrollierten Aktivitäten und Erlebnisse geregelt und auf den einzelnen Besucher der Site zugeschnitten. Es werden Inhalte bereitgestellt, auf die die einzelnen Besucher der Site mit großer Wahrscheinlichkeit reagieren, damit interagieren und letztendlich eine Kaufentscheidung treffen, um die Antwortraten, Erwerbsraten und den Umsatz zu maximieren.

In Target ist jedes Element auf der Seite Bestandteil eines einheitlichen Erlebnisses für die gesamte Seite. Jedes Erlebnis umfasst verschiedene Elemente auf der Seite. Eine Seite wird mit einer einzelnen Codezeile im `<head>` jeder Seite, die Sie verfolgen möchten, optimiert.

Der Inhalt, der Besuchern angezeigt wird, hängt vom erstellten Aktivitätstyp ab:

### A/B-Test

Weitere Informationen finden Sie unter [Erstellen eines A/B-Tests](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72).

Der Inhalt, der in einem einfachen A/B-Test angezeigt wird, wird zufällig aus den Assets ausgewählt, die Sie der Aktivität zuweisen, entsprechend den Prozentwerten, die Sie für die einzelnen Erlebnisse wählen. Als Folge dieser zufälligen Trennung des Traffic kann es anfänglich zu einem hohen Traffic-Aufkommen kommen, bevor sich die Prozentwerte ausgleichen. Wenn Sie beispielsweise zwei Erlebnisse erstellen, wird das Anfangserlebnis per Zufall ausgewählt. Bei wenig Traffic besteht die Möglichkeit, dass der Prozentsatz von Besuchern auf ein Erlebnis ausgerichtet wird. Mit zunehmendem Traffic sollten sich die Prozentsätze langsam angleichen.

Sie können für jedes Erlebnis prozentuale Ziele festlegen. In diesem Fall wird eine zufällige Nummer generiert und diese Nummer wird verwendet, um das anzuzeigende Erlebnis auszuwählen. Die sich ergebenden Prozentzahlen entsprechen möglicherweise nicht genau den festgelegten Zielen, allerdings bedeutet mehr Traffic, dass die Erlebnisse enger auf die beabsichtigen Ziele aufgeteilt werden sollten.

1. Ein Kunde ruft eine Seite von Ihrem Server auf und zeigt sie im Browser an.
2. Im Browser des Benutzers wird ein Erstanbieter-Cookie gesetzt, um das Kundenverhalten zu speichern.
3. Die Seite ruft das Targeting-System auf.
4. Basierend auf den Regeln Ihrer Kampagne werden Inhalte angezeigt.

### Automatische Zuordnung

Weitere Informationen finden Sie unter [Automatische Zuordnung](../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

Die Funktion „Automatisch zuweisen“ identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinnererlebnis automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.

### Automatisches Targeting (AT)

Weitere Informationen finden Sie unter [Automatisches Targeting](../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).

Beim automatischen Targeting werden mehrere marketerdefinierte Erlebnisse mit hoher Leistung über das erweiterte maschinelle Lernen ausgewählt. Zudem erhalten alle Besucher basierend auf ihrem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen ein optimal auf sie zugeschnittenes Erlebnis, um die Inhalte zu personalisieren und Konversionen zu fördern.

### Automatisierte Personalisierung (AP)

Weitere Informationen finden Sie unter [Automatisierte Personalisierung](../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

Die automatisierte Personalisierung (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf deren individuellen Kundenprofilen mithilfe des erweiterten maschinellen Lernens verschiedene Angebotsvarianten zu, um die Inhalte zu personalisieren und Konversionen zu fördern.

### Erlebnis-Targeting (XT)

[Erlebnis-Targeting](../c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4)

Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.

Erlebnis-Targeting, einschließlich Geotargeting, ermöglicht die Definition von Regeln für Erlebnisse oder Inhalte, die auf eine bestimmte Zielgruppe ausgerichtet sind. Es können mehrere Regeln für eine Aktivität bereitgestellt werden, um verschiedene Inhaltvarianten für verschiedene Zielgruppen bereitzustellen. Wenn Besucher Ihre Website aufrufen, werden sie vom Erlebnis-Targeting (XT) geprüft, um festzustellen, ob sie die von Ihnen festgelegten Kriterien erfüllen. Ist dies der Fall, treten sie in die Aktivität ein und das für die qualifizierenden Zielgruppen entworfene Erlebnis wird angezeigt. Sie können Erlebnisse für mehrere Zielgruppen innerhalb einer einzelnen Aktivität erstellen.

### Multivarianz-Tests (MVT)

Weitere Informationen finden Sie unter [Multivarianz-Test](../c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

Beim Multivariate Tests (MVT) werden Kombinationen aus Angeboten in Elementen auf einer Seite verglichen, um zu bestimmen, welche Kombination die beste Leistung für eine bestimmte Zielgruppe erzielt. Zudem gibt er an, welches Element den größten Einfluss auf den Erfolg der Aktivität hat.

### Recommendations

Weitere Informationen finden Sie unter [Empfehlungen](../c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0).

Recommendations-Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten. Empfehlungen tragen dazu bei, Kunden zu relevanten Elementen zu lenken, von denen sie andernfalls möglicherweise nichts wissen.

## Das Edge-Netzwerk {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

„Edge“ ist eine räumlich verteilte Serving-Architektur, die Endnutzern, die Inhalte anfordern, optimale Reaktionszeiten gewährleistet, unabhängig davon, wo sie sich auf der Welt befinden.

Um die Reaktionszeiten zu verbessern, speichern Edge-Umgebungen nur Informationen über die Aktivitäten-Logik, das zwischengespeicherte Profil und das Angebot. Die Aktivitäts- und Inhaltsdatenbanken, [!DNL Analytics]-Daten, APIs und Benutzeroberflächen der Marketingspezialisten werden in den zentralen Datenumgebungen von Adobe gespeichert. Aktualisierungen werden an die Edge-Knoten gesendet. Die zentralen Umgebungen und Edge-Knoten werden automatisch synchronisiert, um die zwischengespeicherten Aktivitätsdaten kontinuierlich zu aktualisieren. Außerdem werden an allen Edges 1:1-Modelle gespeichert, weshalb auch komplexere Anforderungen an den Edges verbleiben können.

Jeder Edge-Knoten verfügt über alle notwendigen Informationen, um auf die Inhaltsanforderung des Benutzers zu antworten und Analysedaten zu der Anforderung nachzuverfolgen. Benutzeranforderungen werden an den nächstgelegenen Edge-Knoten weitergeleitet.

![](assets/edge_network.png)

Core- und Edge-Standorte umfassen sowohl ein Datenerfassungscenter als auch ein Datenverarbeitungscenter. Edge-Standorte umfassen nur ein Datenerfassungscenter. Jede Report Suite wird einem speziellen Datenverarbeitungscenter zugewiesen.

Adobe verfügt derzeit über Rechenzentren auf mehreren Kontinenten, darunter mehrere regionale Standorte in Nordamerika, Europa und Asien.

Anstatt auf alle Targeting-Anfragen von einem einzelnen Standort zu antworten, können durch Anfragen von der Edge-Umgebung, die am nächsten zur anfragenden Stelle liegt, die Folgen der Netzwerk-/Internet-Antwortzeit vermieden werden.

Das Netzwerk dient zudem als Fail-Over-Mechanismus. Wenn ein Edge-Knoten nicht funktioniert, wird die Anfrage an den nächstliegenden Knoten weitergeleitet, um sicherzustellen, dass dem Benutzer kein Standardinhalt angezeigt wird (eine typische Backup-Antwort, wenn eine Anfrage nicht abgeschlossen werden kann).

>[!IMPORTANT]
>
>[!DNL Adobe Target] verfügt derzeit über kein Edge-Netzwerk in China und die Endbenutzerleistung wird für [!DNL Target] Kunden in China weiterhin eingeschränkt. Because of the Great Firewall and the lack of Edge nodes within the country, the experiences of sites with [!DNL Target] deployed will be slow to render and page loads will be affected. Also, the [!DNL Target] user interface might also experience latency.

## Protected User Experience {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe stellt sicher, dass die Verfügbarkeit und Performance der Targeting-Infrastruktur so zuverlässig wie möglich ist. Allerdings kann es durch einen Kommunikationsausfall zwischen dem Browser eines Endbenutzers und den Servern von Adobe zu einer Unterbrechung bei der Bereitstellung der Inhalte kommen.

Zum Schutz vor Dienstunterbrechungen und Verbindungsproblemen sind alle Orte so eingerichtet, dass sie (vom Kunden festgelegte) Standardinhalte beinhalten, die angezeigt werden, wenn der Browser des Benutzers keine Verbindung zu [!DNL Target] aufbauen kann.

An der Seite werden keine Änderungen vorgenommen, wenn der Browser des Benutzers innerhalb eines festgelegten Timeout-Zeitraums (standardmäßig 15 Sekunden) keine Verbindung herstellen kann. Wird diese Timeout-Schwelle erreicht, wird im Cookie eine Einstellung geändert, sodass dem Benutzer für alle anderen Orte sofort Standardinhalte angezeigt werden. Dieser Zustand dauert eine halbe Stunde an, danach versucht der Browser des Benutzers erneut, die Adobe-Server für Inhaltsanfragen zu kontaktieren.

Adobe schützt das Benutzererlebnis durch die Optimierung und Sicherung der Performance.

* Adobe stellt Leistungsbenchmarks auf Grundlage von Branchenstandards sicher, die durch die Dienstgütevereinbarung (Service Level Agreement, SLA) von Adobe gewährleistet werden.
* Das Edge-Netzwerk stellt eine rechtzeitige Datenbereitstellung sicher.
* Adobe setzt einen mehrstufigen Ansatz zur Sicherung seiner Anwendungen ein, um Kunden auf diese Weise ein Höchstmaß an Verfügbarkeit und Zuverlässigkeit zu gewähren.
* [!DNL Target] Consulting bietet Unterstützung bei der Implementierung und laufenden Produktsupport.

## Für Suchmaschinenoptimierung (SEO) geeignete Prüfung {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] ist an den Suchoptimierungsrichtlinien für Prüfungen ausgerichtet.

Google fördert Prüfung durch Benutzer und gibt in seiner Dokumentation an, dass A/B- und Multivariater Tests organische Suchergebnisrankings nicht negativ beeinflussen, solange die vorgegebenen Richtlinien befolgt werden.

Weitere Informationen finden Sie unter folgenden Google-Ressourcen:

* [Website-Tests und Google-Suche](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Experimente und Maskierung](https://support.google.com/analytics/answer/2576845?hl=en&ref_topic=1745207)

Die Richtlinien wurden in einem Beitrag auf dem [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) veröffentlicht. Obwohl dieser Beitrag aus dem Jahr 2012 stammt, ist er die aktuellste Stellungnahme von Google zu diesem Thema und die Richtlinien sind nach wie vor gültig.

* **Keine Maskierung** - Maskierung bedeutet, Benutzern einen bestimmten Inhalt anzuzeigen, Bots von Suchmaschinen jedoch andere Inhalte anzuzeigen, indem diese Inhalte eigens identifiziert und durch andere Inhalte ersetzt werden.

   Target wurde als Plattform so entworfen, dass Bots von Suchmaschinen genau wie normale Benutzer behandelt werden. Das bedeutet, dass Bots möglicherweise in Tests eingeschlossen werden, wenn sie zufällig ausgewählt werden, und die Testvariationen „zu sehen bekommen“.

* **Verwendung von rel=&quot;canonical&quot;** - Manchmal müssen für einen A/B-Test für Inhaltsvariationen unterschiedliche URLs erstellt werden. In diesen Fällen sollten alle Variationen das Tag `rel="canonical"` enthalten, das auf die ursprüngliche (Kontroll-)URL verweist. Prüft Adobe beispielsweise die eigene Startseite mit verschiedenen URLs für jede Variation, wäre im Tag `<head>` folgendes Canonical-Tag für jede der Variationen enthalten:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Verwendung von 302-Umleitungen (temporär)** - Werden unterschiedliche URLs im Rahmen eines Tests für Variationen verwendet, empfiehlt Google den Einsatz einer 302-Umleitung, die Traffic auf die verschiedenen Variationen umleitet. Auf diesem Weg wird Suchmaschinen mitgeteilt, dass die Umleitung nur vorübergehend und nur aktiv ist, solange die Prüfung durchgeführt wird.

   Eine 302-Umleitung ist eine Server-seitige Umleitung. Target stützt sich – wie die meisten anderen Optimierungsanbieter auch – auf Client-seitige Funktionen. Somit befolgt Target in diesem Fall die Empfehlungen von Google nicht zu hundert Prozent. Dies wirkt sich aber lediglich auf eine geringe Anzahl von Tests aus. Der Standardansatz für die Durchführung von Tests mit Target fordert sich ändernde Inhalte innerhalb einer einzigen URL, sodass keine Umleitungen erforderlich sind. Es handelt sich hierbei um Fälle, in denen Kunden mit verschiedenen URLs arbeiten müssen, um Variationen zu testen. Hier wird in Target der JavaScript-Befehl `window.location` verwendet, um Benutzer auf Testvariationen umzuleiten. Es wird dabei nicht angegeben, ob es sich um eine Umleitung des Typs 301 oder 302 handelt.

   Wir sind zwar weiterhin auf der Suche nach möglichen Lösungen für eine vollständige Umsetzung der Suchmaschinenrichtlinien für Kunden, die für ihre Tests verschiedene URLs verwenden müssen, sind jedoch überzeugt, dass die ordnungsgemäße Verwendung der oben beschriebenen Canonical-Tags für die Senkung des Risikos, das mit diesem Verfahren verbunden ist, vollkommen ausreicht.

* **Experimente nur so lange wie nötig durchführen** - „So lange wie nötig“ bedeutet für uns „so lange es dauert, bis ein Ergebnis mit statistischer Bedeutung erzielt wurde“. Es stehen in Target [Best Practices](https://docs.adobe.com/content/target-microsite/testcalculator.html) zur Verfügung, mit deren Hilfe festgestellt werden kann, wann Ihr Test diesen Punkt erreicht hat. Wir empfehlen, diese hartcodierte Implementierung erfolgreicher Tests in Ihren Test-Arbeitsablauf einzugliedern und die entsprechenden Ressourcen bereitzustellen.

   Es wird nicht empfohlen, die Plattform Target dauerhaft zur „Veröffentlichung“ der erfolgreich getesteten Variationen zu verwenden. Werden diese Variationen jedoch für 100 % der Benutzer zu 100 % der Zeit bereitgestellt, kann eine Variation mit Target veröffentlicht werden, solange die Hartcodierung noch nicht abgeschlossen ist.

   Beachten Sie dabei auch, was durch Ihren Test geändert wurde. Eine Änderung der Farbe von Schaltflächen oder anderer Elemente, die keinen Text enthalten, wirkt sich nicht auf das Suchmaschinenranking Ihrer Seite aus. Änderungen an Texten sollten jedoch auf jeden Fall hartcodiert werden.

   Berücksichtigen Sie außerdem, wie einfach auf die zu testende Seite zugegriffen werden kann. Sollte die Seite nicht für Suchmaschinen verfügbar sein und war sie niemals dafür gedacht, in organische Rankings von Suchmaschinen aufgenommen zu werden (beispielsweise im Falls einer besonderen Landingpage für E-Mail-Kampagnen), spielen die oben genannten Punkte keinerlei Rolle.

Laut Google wirken sich Tests beim Befolgen der Richtlinien nicht oder nur geringfügig auf das Trefferranking Ihrer Site aus.

Zusätzlich zu diesen Richtlinien stellt Google eine weitere Richtlinie in der Dokumentation für das Werkzeug für Inhaltstests bereit:

* „Die Seitenvariationen sollten dem Inhalt Ihrer Originalseiten ähnlich sein. Die Variationen sollten die allgemeine Wahrnehmung der ursprünglichen Inhalte durch die Benutzer nicht ändern.“

Als Beispiel gibt Google an: „Wenn eine Originalseite voller Schlüsselwörter ist, die nicht den für die Benutzer verfügbaren Inhalten entsprechen, kann diese Seite aus unserem Index entfernt werden.“

Unserer Ansicht nach ist es jedoch eher schwierig, die Bedeutung originaler Inhalte im Rahmen eines Tests unabsichtlich in solcher Weise zu verändern. Trotzdem empfehlen wir, die Schlüsselwortaussagen einer Seite zu prüfen und sie bei neuen Variationen beizubehalten. Änderungen am Seiteninhalt, besonders das Löschen oder Hinzufügen relevanter Schlüsselwörter, kann dazu führen, dass sich das organische Ranking der Seite ändert. Wir empfehlen Ihnen, Ihren SEO-Partner in den Testvorgang einzubeziehen.