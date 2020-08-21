---
keywords: welcome kit;target welcome kit;intro;introduction;getting started
description: Adobe Target Begrüßungs-Kit - Kapitel 4
title: Adobe Target Begrüßungs-Kit - Kapitel 4
feature: intro
translation-type: tm+mt
source-git-commit: abe2e2acdf5cdd24ac2f9039cdb1119f5d3afb90
workflow-type: tm+mt
source-wordcount: '2874'
ht-degree: 0%

---


# Kapitel 4: Tipps zur Verwendung der Zielgruppe

Aufgrund unserer Arbeit mit vielen [!DNL Target] Benutzern haben wir festgestellt, wie Sie von Ihrer [!DNL Target] Lösung mehr Wert erhalten können. Wir haben diese in den vielen Tipps zusammengefasst, die wir in diesem Kapitel enthalten haben. Auch wenn Sie nicht bereit sind, alle diese Ideen sofort zu nutzen, halten Sie an dieser Liste fest. Je mehr Erfahrung Sie mit der Lösung haben und je älter Ihr Programm ist, desto mehr erfahren Sie, wie Sie mit diesen Tipps mehr erreichen können [!DNL Target].

## Tipp 1: Optimieren Sie die Personalisierung, indem Sie das Besucher-Profil um zusätzliche Daten erweitern.

Sie können Erlebnisse mit [!DNL Target] Daten sofort personalisieren. Aber Sie können Ihre Daten noch besser personalisieren, indem Sie Ihre eigenen Daten in den Mix einfügen. Sie können Ihr Profil mit historischen Daten aus [!DNL Adobe Analytics] und Echtzeit-Daten aus Ihrem System erweitern [!DNL Adobe Audience Manager]. Sie können auch Kundenattribute verwenden, eine Funktion im People-Core-Service in [!DNL Adobe Experience Cloud], um CRM-Daten, Drittanbieter-Partnerdaten und von Drittanbietern erworbene Daten ganz einfach in [!DNL Target]Ihre Website zu integrieren.

Beispielsweise können Sie Kaufdaten aus Ihrem Verkaufsort mit einem Besucher-Profil verknüpfen. Erstellen Sie dazu einfach eine CSV-Datei mit bis zu 200 Offline-Variablen und laden Sie sie entweder direkt [!DNL Adobe Experience Cloud] über einen Datei-Upload hoch oder verwenden Sie FTP, um Ihre Datei zu hosten und regelmäßig zu aktualisieren. Sobald sich Ihre Kundenattribute befinden, können Sie sie [!DNL Adobe Experience Cloud]Lösungen zuordnen, z. B. [!DNL Experience Cloud] und [!DNL Adobe Analytics] [!DNL Target] wo sie für Analyse, Tests und Personalisierung verfügbar sein werden.

Eine schrittweise Anleitung finden Sie unter [Benutzerdefinierte Attribute](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) .

**Gut zu wissen**: Da [!DNL Target] es sich um eine offene und agnostische Plattform handelt, die mit verschiedenen Technologien gut funktioniert, können Sie CRM- oder erworbene Daten auf viele verschiedene Arten hinzufügen. Das bedeutet, dass Sie eine Methode wählen können, die für Ihr Unternehmen am besten geeignet ist.

Weitere Informationen finden Sie unter [Methoden für die Zielgruppe](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md) von Daten.

## Tipp 2: Durch die Verknüpfung von Zielgruppe-Audiencen mit anderen Adobe Experience Cloud-Audiencen können Sie Ihre persönlichen Daten noch besser personalisieren.

Das Zusammenführen von Audiencen, die in unterschiedlichen [!DNL Adobe Experience Cloud] Lösungen leben, kann Ihnen ein umfassenderes Verständnis Ihrer Kunden sowie die Möglichkeit geben, sich stärker zu personalisieren. Wenn Sie beispielsweise Daten zur Audience in Echtzeit [!DNL Target] bereitstellen, [!DNL Adobe Analytics] werden Verlaufsdaten zur Audience bereitgestellt. Die Kombination dieser beiden Faktoren kann Ihnen dabei helfen, festzustellen, wann das Verhalten eines Kunden konsistent ist und wann möglicherweise die Möglichkeit besteht, auf ein neues Verhalten zu reagieren. Klicken Sie beim Erstellen einer Aktivität einfach auf das Dropdown-Menü neben &quot;Alle Besucher&quot;. Markieren Sie anschließend die Kästchen mit bis zu zwanzig Audiencen, klicken Sie auf &quot;Mehrere Audiencen kombinieren&quot;und klicken Sie auf &quot;Speichern&quot;.

Eine schrittweise Anleitung finden Sie unter [Kombinieren mehrerer Audiencen](/help/c-target/combining-multiple-audiences.md) .

**Gut zu wissen**: [!DNL Adobe Audience Manager] audiencen sind [!DNL Target] automatisch verfügbar. Aber die Freigabe von [!DNL Adobe Analytics] Audiencen erfordert ein wenig manuelles Setup. Markieren Sie einfach das Kästchen &quot;Make this an Experience Cloud Audience&quot; während der Audience-Erstellung in [!DNL Analytics]. Klicken Sie anschließend [!DNL Target]auf &quot;Experience Cloud-Audiencen importieren&quot;.

## Tipp 3: Exportieren Sie Daten aus der Zielgruppe zur Verwendung mit Drittanbieterwerkzeugen.

Mithilfe von Antworttoken können Administratoren Daten ganz einfach aus [!DNL Target] und in Tools von Drittanbietern abrufen. Dies kann hilfreich sein, wenn Sie Daten zu Daten hinzufügen möchten, die in einem Umfrage-Tool erfasst wurden. Wenn beispielsweise eine Umfrage eine Stichprobe einer Population mit einem Erlebnis mit einem Wert von &quot;9&quot;und einem Erlebnis mit einem Wert von &quot;4&quot;anzeigt, können Sie Ihre Daten verwenden, um zu sehen, wer Erlebnis A gesehen hat und wer Erlebnis B gesehen hat. Sie können auch Antwort-Token verwenden, um [!DNL Target] Daten in Ihr internes Data Warehouse zu exportieren. Klicken Sie einfach auf &quot;Administration&quot;, und schalten Sie dann den Schalter neben dem gewünschten Antworttoken auf die Position ein. Als Nächstes erstellen Sie eine Aktivität. Die Daten können dann an den Drittanbieter übertragen werden. Sie können mithilfe von Debuggingwerkzeugen überprüfen, ob die Daten exportiert [!DNL Target] werden.

Eine schrittweise Anleitung finden Sie unter [Antworttoken](/help/administrating-target/response-tokens.md) .

**Hilfreicher Hinweis**: Bevor ein Administrator ein mit einem Drittanbieter verknüpftes Antwort-Token aktivieren kann, muss ein Entwickler eine Partnerschaft mit dieser Drittanbieter-Firma einrichten.

Eine schrittweise Anleitung finden Sie unter [Antworttoken](/help/administrating-target/response-tokens.md) .

**Führen Sie zuerst** Folgendes aus: Vergewissern Sie sich, dass Sie at.js Version 1.1 oder höher verwenden. Wenn Sie eine frühere Version verwenden, werden die Antwort-Token angezeigt, at.js kann sie jedoch nicht verwenden.

## Tipp 4: Erstellen Sie Audiencen aus diesen Schlüsselvariablen, um den Wert Ihrer Aktivität zu erhöhen.

Berücksichtigen Sie beim Erstellen von Audiencen zum Targeting oder Testen von Promotions und Angeboten zunächst folgende Variablen:

* Verhalten. Besuchsmuster und Kaufmuster auf der Site
* Verweisende Stelle. Verweisende Websites und Kampagnen
* Temporal. Tageszeiten, Wochentage und saisonale Faktoren
* Offline. Besuchs- und Kaufmuster in physischen Geschäften
* Umgebung. Land der Herkunft, Betriebssystem, Browsertyp

## Tipp 5: Gewähren Sie Benutzern den Zugriff, den sie für ihre Arbeit benötigen.

Erleichtern Sie sich die Arbeit mit den Daten Ihres Unternehmens und bewahren Sie die Sicherheit. [!DNL Target Premium] ermöglicht Administratoren die Steuerung des Zugriffs auf verschiedene interne und externe Teams.

Weitere Informationen finden Sie unter [Enterprise-Benutzerberechtigungen](/help/administrating-target/c-user-management/property-channel/property-channel.md) .

**Hilfreicher Hinweis**: Wenn beim Hinzufügen von Benutzern der Name eines Teammitglieds noch nicht hinzugefügt wurde (z. B. bei einem Mitarbeiter einer Agentur eines Drittanbieters), löst die Eingabe der E-Mail-Adresse und des Passworts eine E-Mail-Einladung aus, sich dem Arbeitsbereich des Teams anzuschließen.

Verwenden von Target Standard? Sie können Ihren Benutzern weiterhin drei Zugriffsebenen [mit schreibgeschützten Rollen, Editor- und genehmigenden Rollen](/help/administrating-target/c-user-management/c-user-management/user-management.md) zuweisen!

## Tipp 6: Entdecken Sie, wie ein Angebot während einer Customer Journey funktioniert, indem Sie es auf jeder einzelnen Seite der Reise testen.

Erfahren Sie, wie ein Angebot, z. B. kostenloser Versand, während einer Kundenreise funktioniert, die über mehrere Seiten auf Ihrer Website stattfindet.

Eine schrittweise Anleitung finden Sie unter [Mehrseitige Aktivität](/help/c-experiences/c-visual-experience-composer/multipage-activity.md) .

**Hilfreicher Hinweis**: Wenn Sie die URL ändern, nachdem Sie einen Seitenbereich angegeben haben, wird das Erlebnis zurückgesetzt. Das bedeutet, dass die angegebenen Varianten nicht mehr angezeigt werden. Wenn Sie die URL ändern müssen, denken Sie daran, das Erlebnis neu zu definieren.

## Tipp 7: Testen Sie ein Angebot mit verschiedenen Audiencen, um festzustellen, ob Audiencen unterschiedliche Präferenzen haben.

Mit Experience Versions können Sie einen Test mit Varianten für beliebig viele Audiencen ausführen. Sie können beispielsweise eine Banneranzeige erstellen, die kostenlosen Versand anbietet - mit Bildern und Währungsvarianten für Kunden in den USA, Großbritannien und den USA -, ohne dass Sie Tests für drei verschiedene Audiencen durchführen müssen.

Eine schrittweise Anleitung finden Sie unter [Mehrere Erlebnis-Audiencen in einem A/B-Test](/help/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md) - und [Erlebnisversionen in Adobe Target](https://helpx.adobe.com/target/how-to/experience-versions.html?playlist=/ccx/v1/collection/product/target/seg-%20ment/business-practitioners/explevel/beginner-adls/applaunch/how-to-2/collection.ccx.js?ref=helpx.adobe.com) .

## Tipp 8: Sparen Sie Zeit, indem Sie Erlebnisse in ähnlichen Aktivitäten replizieren.

Erstellen Sie eine Variante auf einer Webseite, z. B. eine neue Schaltflächenfarbe, und wenden Sie sie automatisch auf alle Seiten an, die dieselbe Vorlage verwenden. Sie können Seiten angeben oder die Variationen auf alle ähnlichen Seiten Ihrer Website anwenden.

Eine schrittweise Anleitung finden Sie unter [Einbeziehen des gleichen Erlebnisses auf ähnlichen Seiten](/help/c-experiences/c-visual-experience-composer/temtest.md) .

## Tipp 9: Reduzieren Sie die Übersichtlichkeit in Ihrer Audience-Bibliothek, indem Sie einmalige Audiencen erstellen.

Wenn Sie ein Segment als Ziel auswählen, von dem Sie wissen, dass es nicht erneut zu Zielgruppen kommt (z. B. Kunden, die von einem unerwarteten Wetterereignis betroffen sind), kann die Erstellung einer einmaligen Audience Ihnen dabei helfen, die Aufgabe zu erledigen, ohne dass Sie Ihre Audience-Bibliothek übersichtlicher gestalten müssen. Dadurch wird es einfacher, Audiencen zu finden, die Sie immer und immer wieder verwenden.

Eine schrittweise Anleitung finden Sie unter [Erstellen einer Nur-Aktivität-Audience](/help/c-target/creating-activity-only-audience.md) .

**Hoch angeforderte Funktion**: Unsere Kunden haben uns gebeten, die Möglichkeit zu schaffen, dass Audiencen mit nur einem Verwendungszweck nicht automatisch in der Audience-Bibliothek gespeichert werden. Jetzt müssen sie keine Audiencen mehr manuell löschen, um ihre Bibliotheken zu organisieren.

## Tipp 10: Einfache Tests werden schneller ausgeführt, ohne dass sie den Standard-QS-Prozess durchlaufen.

Es gibt nichts Schlimmeres als eine Aktivität zu haben, die bereit ist zu gehen und dann Wochen darauf zu warten, dass sie den Standard-QS-Prozess abschließt. Sie können die meisten Aktivitäten durch Weiterleiten einiger QS-Links an Kollegen überprüfen, um sie in verschiedenen Browsern zu testen. Wahrscheinlich möchten Sie für Bemühungen, die die Funktion der Site drastisch verändern, mehr QS-Tests durchführen, aber in Wirklichkeit sollten Sie weniger dieser Aktivitäten und weitaus mehr der grundlegenderen Aktivitäten haben. Durch das Hinzufügen besserer Rechte-Kontrollen, damit weniger Menschen Dinge voll leben können, werden auch sinnvolle Grenzen gesetzt und Sie können das erreichen, was Sie brauchen, ohne dabei Geschwindigkeit und Effizienz zu opfern. Eine andere Möglichkeit besteht darin, über eine IT-Ressource zu verfügen, die eine zeitnahe Überwachung des Qualitätssicherungsprozesses ermöglicht.

Eine schrittweise Anleitung finden Sie unter [Aktivität QA](/help/c-activities/c-activity-qa/activity-qa.md) .

## Tipp 11: Führen Sie Tests auf Seiten mit hohem Traffic durch, damit sie schneller statistische Bedeutung erreichen.

Viele Marketingexperten starten Optimierungs-Programm für die Segmentierung und das Targeting von Audiencen, ohne zu prüfen, ob die dargestellten Traffic-Stufen und -Audiencen innerhalb des Testzeitraums zu signifikanten Ergebnissen für ihre Optimierungs- und Konversionsziele führen. Um diesen allgemeinen Fehler zu vermeiden, beantworten Sie diese Fragen im Voraus:

* Wie viele individuelle Besucher pro Tag gibt es auf der Seite?
* Was ist der Konversionsrate für die Seite?
* Wie lange müssen Sie den Test voraussichtlich ausführen, bevor Sie ihn als abgeschlossen bezeichnen können?

**Hilfreicher Tipp**: Verwenden Sie den [Stichprobengrößenrechner](https://docs.adobe.com/content/target-microsite/testcalculator.html) der Zielgruppe, um die für einen erfolgreichen Test erforderliche Stichprobengröße zu ermitteln.

## Tipp 12: Entwerfen Sie einfachere Tests, um sicherzustellen, dass Sie sie erstellen und implementieren können.

Nachdem alle Aspekte des Testentwurfs berücksichtigt wurden, kann ein Plan sehr komplex werden. Je nachdem, wo Ihr Unternehmen mit Tests arbeitet und wie Ihre Gruppe die Ergebnisse entwerfen, codieren, ausführen und analysieren kann, stellen Sie fest, ob der Test zu ehrgeizig erscheint. Falls ja, seien Sie bereit, den Umfang und die Komplexität zu reduzieren. Besser zu Beginn klein, als den Test überhaupt nicht durchzuführen. Sie können keine effektive Steigerung liefern, wenn Sie den Test nie starten. Es ist wichtig, die Wünsche des Teams mit den Realitäten Ihrer Ressourcen und Fähigkeiten in Einklang zu bringen.

## Tipp 13: Komplexe Tests in kleinere Aktivitäten unterteilen, um sie zu erreichen.

Anstatt einen großen Test mit mehreren Variablen und einer komplexen Entwicklung zu entwickeln, sollten Sie eine weniger komplexe Reihe kleinerer Tests mit minimalen Variablen entwickeln. Dies ermöglicht ein tiefergehendes Verständnis der Testleistung basierend auf bestimmten Variablen. Außerdem reduziert es mögliche technische Probleme, die mit der Entwicklung größerer Projekte einhergehen.

![Darstellung komplexer Tests](/help/c-intro/assets/break-complex-tasks.png)

## Tipp 14: Maximieren Sie Ihre Testauswirkungen, indem Sie Tests näher am Ende des Konversionstrichter durchführen.

Wenn Sie so nahe an der Seite testen, auf der Besucher auf &quot;Kauf abschließen&quot;, &quot;Anwendung senden&quot;oder auf andere Weise eine Konversion abschließen, erzielen Sie in der Regel die wirkungsvollsten Ergebnisse. Besucher, die das Trichterende erreichen, sind qualifiziert, haben mehr Zeit investiert und sind bereit zu kaufen. Testen Sie daher Einblicke in ihre Präferenzen und Aktionen, um rentable Änderungen vorzunehmen. Da Seiten auf dem Kaufpfad für die Konversionsraten entscheidend sind, sollten auf diesen Seiten durchgeführte Tests mit wichtigen Interessenträgern verknüpft werden, bevor sie veröffentlicht werden.

![Umrechnungstrichterdarstellung](/help/c-intro/assets/conversion-funnel.png)

## Tipp 15: Aktualisieren Sie Ihre Tests ständig, um iterative Verbesserungen zu erzielen.

Wenn sich Ihre Hypothese nicht als wahr erwiesen hat, denken Sie an Möglichkeiten, Ihren Test zu verbessern. Denken Sie daran, dass Ihr Experiment keine Zeitverschwendung war, selbst wenn keines der getesteten Erlebnisse besser ablief. Ein erfolgreicher Test bedeutet nicht immer eine Steigerung des Umsatzes oder der Umrechnung. Wenn der Test Ihre Hypothese unterstützt, dann sind Sie auf dem Weg, eine allgemeine Theorie zu entwickeln. Aber auch wenn Sie ein klares Gewinnerergebnis haben, hören Sie nicht auf. Zu oft machen Marketingexperten den Fehler, ein Mal zu testen und dann auf diese Ergebnisse zu setzen, ohne wirklich zu verstehen, was zu dem Erfolg führte. Planen Sie stattdessen, diese Ergebnisse zu durchlaufen, um herauszufinden, warum der Front-Läufer voran war. Dadurch erhalten Sie tiefere Einblicke, die Sie in zukünftigen Kampagnen verwenden können.

## Tipp 16: Vergleichen Sie Tests und Personalisierungs-Aktivitäten für Ideen, um das Targeting zu verbessern.

Der Vergleich der Konversionsleistung verschiedener Audiencen in verschiedenen Tests an verschiedenen Orten kann dabei helfen, die Optimierungsstrategie einer Firma zu fokussieren und zu verfeinern. Verwenden Sie Testvergleiche, um herauszufinden, welche Audiencen am nützlichsten zu testen sind, welche zielgerichteten Erlebnisse erhalten sollten und welche Erlebnisse am ehesten eine Antwort hervorrufen.

So führte beispielsweise ein Finanzdienstleistungskunde eine Kampagne zur Werbeaktion für eine Kreditkarte durch, bei der es um professionelle Ereignis-Anreize ging. Durch partielle Multivarianz-Tests seiner Landingpages war der Kunde in der Lage, Botschaften über Kreditkartenvorteile optimal mit sportlichen Anreizen zur Zielgruppe unterschiedlicher Audiencen vom Kundenstamm auszugleichen. Dieser Ansatz ermöglichte es der Firma, während eines zeitnahen Fensters, das ein wichtiges Ereignis des Sports umgibt, Nutzen zu ziehen und die Umrechnung zu maximieren.

## Tipp 17: Machen Sie Tests nützlich, indem Sie sie nur dann starten, wenn Sie wissen, dass Sie mit den Daten handeln können.

Ein Test ist sinnlos, wenn Sie nicht genau wissen, wie Sie mit den Daten umgehen werden. Dazu gehören die Kenntnis Ihrer wichtigsten Erfolgsmetrik, was passieren muss, um einen Gewinner zu fördern, wie Sie die Testergebnisse weiterverfolgen werden und was Sie mit den Informationen zur Audience tun werden. Für einen schnellen und erfolgreichen Test ist es wichtig, dass alle am Test beteiligten Gruppen (Entwickler, Kreative, Testspezialisten usw.) ihre Rolle vor dem Teststart kennen.

## Tipp 18: Bevor Sie einen Test starten, sollten Sie sicherstellen, dass das Unternehmen das Schieben des Gewinners unterstützt.

Erfolgreiche Optimierungsunternehmen glauben an das Konzept des Testens und verstehen, dass ihre professionellen Meinungen darüber, welche Erfahrung den Test gewinnen wird, nicht immer wahr sind. Sie bestimmen den Gewinner auf der Grundlage einer soliden Datengrundlage und sind bestrebt und bereit, das erfolgreichste Erlebnis nach dem Eintreten der Ergebnisse live zu gestalten, auch wenn es nicht den Erwartungen entspricht oder widersinnig erscheint.

So hat beispielsweise ein Kunde von Adobe Healthcare Services kürzlich den Testwert demonstriert, indem er zeigte, wie ein Heldenbanner, das das Team als Slam-Dunk betrachtet hatte, die Konversion tatsächlich negativ beeinflusst hat. Wenn Ihr Unternehmen noch keine vollständigen Tests durchgeführt hat, sollten zunächst einfachere, kleinere Tests durchgeführt werden, damit Änderungen an Testergebnissen inkrementell vorgenommen werden können.

## Tipp 19: Teilen Sie allen mit, dass Sie einen Test gestartet haben, um Bedenken zu vermeiden, wenn sich die Site ändert.

Einer der Vorteile der Einrichtung Ihrer Aktivitäten zur Verwendung von QS-Parametern besteht darin, dass Sie diese Links für alle Mitarbeiter Ihres Teams freigeben können. Sie machen mehr Personen auf die Aktivität aufmerksam und stellen sicher, dass sie nicht davon ausgehen, dass die Site nicht richtig funktioniert, wenn sie eine Testvariante erreichen.

Nach Abschluss der Tests können Sie mithilfe der Mitteilung von Kampagnen, Testergebnissen und insbesondere den gewonnenen Erkenntnissen das Bewusstsein für die Testergebnisse und das Interesse daran schärfen. Die Weitergabe der Ergebnisse an alle Mitarbeiter der Organisation vermeidet das erneute Testen einer Hypothese, informiert jeden darüber, was funktioniert, und hilft ihnen, ihre eigenen Vorstellungen davon, was funktioniert, grundlegend herauszufordern, basierend auf dem, was Sie gefunden haben. Es empfiehlt sich, eine Vorlage zu erstellen, die Sie jedes Mal verwenden, um Ihre Ergebnisse und wichtigen Erfahrungen zu teilen.
Dann erwägen Sie, ein freigegebenes Buch oder ein Microsoft PowerPoint-Deck zu erstellen, das diese Lernprozesse kumulativ erfasst.

## Tipp 20: Tippen Sie auf mobile Funktionen, um innovativere mobile Aktivitäten zu erstellen.

Die Benutzererfahrung auf Tablets und Smartphones muss sich auf touchgesteuerte Steuerelemente konzentrieren, da die Hauptinteraktion auf Besuchern statt auf Mausklicks und Tastatursteuerelemente erfolgt. Profitieren Sie von mobilen Anzeigesteuerelementen wie Blättern, Berühren, Ziehen, Pinch- und Zoom-Gesten. Verwenden Sie einfache, große Schaltflächen, um Interaktionen und Navigation festzulegen, z. B. eine große Warenkorb- oder Videowiedergabeschaltfläche. Wenn Sie für den Handel mit Mobilgeräten konzipieren, integrieren Sie eine umfassende Produktvisualisierung, die für den Gerätetyp optimiert ist. Suchen Sie immer nach Möglichkeiten, den Fokus auf das Benutzererlebnis auf eingebettete, große Viewer oder interaktive Zoom- und Schwenk-Funktionen im Vollbildmodus, 360-Grad-Rotationsset und erweiterte Videofunktionen zu verlagern.

## Tipp 21: Hilft mobilen Besuchern, das zu finden, was sie wollen, indem sie die mobile Suche optimieren.

Benutzer mit Mobilgeräten haben eine hohe Priorität. Die meisten von ihnen verwenden die Suche, bevor sie etwas Anderes auf m-commerce Sites tun, was die Optimierung der Suche nach Mobilgeräten entscheidend macht. Zur Verbesserung der Suchmaschinenoptimierung (SEO) für Mobilgeräte verwenden Sie explizite Navigationshinweise für einfaches Browsen. Implementieren Sie außerdem die automatische Empfehlung und Autokorrektur in Sucheingabefeldern, um die Schwierigkeiten bei der Mobileingabe zu beheben. Stellen Sie überzeugende, relevante Suchergebnisse bereit, die für Bildschirmgröße und -position optimiert wurden.

## Tipp 22: Erreichen Sie mobile Audiencen mithilfe des Tageszeitansatzes-Targeting für mobile SEM-Kampagnen.

Verstehen Sie, wie und wann Sie Ihre Audience erreichen und wie Sie Ihre täglichen Werbeausgaben besser verwalten können, indem Sie Ihre mobilen Kampagnen tagtäglich in verschiedene Segmente unterteilen.

Viele Marketingexperten begehen den Fehler, nicht genügend Budget zur Verfügung zu stellen, um diesen Anteil an Stimmen in den Stunden zu erfassen, in denen der Einsatz bestimmter Geräte am stärksten ist, und hinterlassen so eine Menge Umsatz und Interessenten auf dem Tisch.

So spitzt sich die Tablettennutzung in der Regel abends an, und viele Benutzer navigieren beim Fernsehen. Im Gegensatz dazu greifen Smartphone-Benutzer in der Regel unterwegs auf Inhalte zu. Höchste Konvertierungszeiten variieren auch je nach Branche. Daher ist es wichtig zu verstehen, wann Ihre individuellen Kunden am ehesten handeln.

## Bitte beachten Sie

Berücksichtigen Sie die folgenden Ideen, bevor wir zum nächsten Kapitel übergehen: &quot;Anregung zum Testen und Personalisieren von Aktivitäten.&quot;

### Wenn Sie Ihre Tests erstellen, nicht dekorieren, seien Sie absichtlich.

* Kontrollieren Sie den Fluss mit absichtlichen Augenpfaden, die sich auf Konversionspunkte konzentrieren.
* Vergewissern Sie sich, dass Sie Ihre Immobilie zu Ihrem Vorteil nutzen.
* Nutzen Sie den Bildfokus, um sicherzustellen, dass Bilder nicht dekorativ sind, sondern für Sie funktionieren.
* Reduzieren Sie mit der vereinfachten Kopie Übersichtlichkeit, Reibung und Unschärfe.
* Stellen Sie sicher, dass Sie über effektive Aktionsaufrufe verfügen, wenn der Benutzer aktiv werden muss.
* hinzufügen Glaubwürdigkeit durch benutzergenerierte Inhalte, wo immer möglich.

### Vereinfachen Sie Ihre Website.

* Machen Sie Kunden nicht zum Lesen. Sie werden es nicht.
* Machen Sie es einfach zu scannen.
* Verwenden Sie Blöcke mit Aufzählungszeichen.
* Stellen Sie sicher, dass Ihre Kopie einem klaren, sequenziellen Gedankenprozess folgt.

### Effektiver Aktionsaufruf (CTA)

* Legen Sie sich in die Schuhe des Kunden.
* Verwenden Sie aktionsorientierte Sprache.
* Betrachten Sie die Motivation zur Umrechnung.
* Behandeln Sie das Ergebnis der Konvertierung.
* Stellen Sie sicher, dass CTAs angezeigt werden!