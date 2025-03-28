---
keywords: Welcome Kit;Target Welcome Kit;Intro; Einführung;Erste Schritte
description: Lesen Sie Tipps unserer Experten zur Verwendung von Adobe  [!DNL Target]  im Rahmen Ihrer Test- und Personalisierungsstrategie.
title: Wo finde ich Tipps und Tricks zur Verwendung von Target?
feature: Overview
exl-id: 86437ad1-83ea-4670-b503-6c3c1fff0c16
source-git-commit: 52f11998149cddeb4245a0f07280562d79332a04
workflow-type: tm+mt
source-wordcount: '2883'
ht-degree: 72%

---

# Kapitel 4: Tipps zur Verwendung von Target

In Zusammenarbeit mit vielen [!DNL Target] Benutzern haben wir Wege gefunden, durch die Sie den Wert Ihrer [!DNL Target]-Lösung steigern können. Wir haben diese in den vielen Tipps zusammengefasst, die wir in diesem Kapitel aufgenommen haben. Vermutlich werden Sie jetzt noch nicht alle diese Ideen umsetzen können. Werfen Sie jedoch immer wieder einen Blick darauf. Je mehr Erfahrung Sie mit der Lösung haben und je mehr Ihr Programm heranreift, desto mehr werden Sie sehen, wie diese Tipps Ihnen helfen können, mehr mit [!DNL Target] zu erreichen.

## Tipp 1: Optimieren Sie die Personalisierung durch zusätzliche Daten im Besucherprofil.

Sie können Erlebnisse bereits sehr gut mit den vorkonfigurierten [!DNL Target]-Daten personalisieren. Wenn Sie diesem Angebot aber noch eigene Daten hinzufügen, erhalten Sie wesentlich bessere Personalisierungsergebnisse. Sie können Ihr Profil mit historischen Daten aus [!DNL Adobe Analytics] und Echtzeitdaten aus [!DNL Adobe Audience Manager] erweitern. Sie können auch Kundenattribute verwenden, eine Funktion des People Core Service von [!DNL Adobe Experience Cloud], und CRM-Daten, Partnerdaten von Zweitanbietern und zugekaufte Daten von Drittanbietern problemlos in [!DNL Target] integrieren.

Beispielsweise können Sie Kaufdaten aus Ihrem Point-of-Sale-System mit einem Besucherprofil verknüpfen. Erstellen Sie dazu einfach eine CSV-Datei mit bis zu 200 Offline-Variablen und laden Sie diese Datei über einen Datei-Upload entweder direkt in die [!DNL Adobe Experience Cloud] hoch oder verwenden Sie FTP, um die Datei zu hosten und regelmäßig zu aktualisieren. Sobald sich Ihre Kundenattribute in der [!DNL Adobe Experience Cloud] befinden, können Sie sie [!DNL Experience Cloud]-Lösungen wie [!DNL Adobe Analytics] und [!DNL Target] zuordnen. Dort stehen sie dann für Analysen, Tests und für die Personalisierung zur Verfügung.

Eine schrittweise Anleitung finden Sie unter [Benutzerspezifische Attribute](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=de).

**Gut zu wissen**: Da es sich bei [!DNL Target] um eine offene und agnostische Plattform handelt, deren Unterstützung für verschiedene Technologien herausragend ist, können Sie CRM- oder erworbene Daten auf viele verschiedene Weisen hinzufügen. Sie können also die Methode wählen, die für Ihre Organisation am besten geeignet ist.

Weitere Informationen finden [ unter „Verfahren für die Datenübernahme in ](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}&quot;.

## Tipp 2: Optimieren Sie die Personalisierung durch Kombination Ihrer [!DNL Target]-Zielgruppen mit anderen Zielgruppen aus Adobe Experience Cloud.

Durch Kombination Ihrer Zielgruppen aus unterschiedlichen [!DNL Adobe Experience Cloud]-Lösungen erhalten Sie einen tieferen Einblick in Ihre Kunden und wesentlich bessere Optimierungsmöglichkeiten. So stellt Ihnen [!DNL Target] beispielsweise Echtzeitdaten zu Ihren Zielgruppen bereit, aus [!DNL Adobe Analytics] erhalten Sie zusätzlich jedoch auch historische Daten. Die Kombination dieser beiden Faktoren kann Ihnen dabei helfen festzustellen, wann das Verhalten eines Kunden konsistent ist und wann es eine Möglichkeit gibt, auf ein neues Verhalten zu reagieren. Klicken Sie beim Erstellen einer Aktivität einfach auf das Dropdown-Menü neben „Alle Besucher“. Aktivieren Sie als Nächstes die Kontrollkästchen von bis zu zwanzig Zielgruppen, klicken Sie auf „Mehrere Zielgruppen kombinieren“ und dann auf „Speichern“.

Eine schrittweise Anleitung finden Sie unter [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md).

**Gut zu wissen**: [!DNL Adobe Audience Manager]-Zielgruppen sind in [!DNL Target] automatisch verfügbar. Die Freigabe von [!DNL Adobe Analytics]-Zielgruppen muss jedoch manuell eingerichtet werden. Aktivieren Sie bei der Erstellung der Zielgruppe in [!DNL Analytics] einfach das Kontrollkästchen „Als Experience Cloud-Zielgruppe festlegen“. Klicken Sie dann in [!DNL Target] auf &quot;Experience Cloud-Zielgruppen importieren“.

## Tipp 3: Exportieren Sie Daten aus [!DNL Target] in Programme von Drittanbietern.

Mit Antwort-Token können Administratoren Daten problemlos aus [!DNL Target] in Programme von Drittanbietern exportieren. Dies ist zum Beispiel sehr praktisch, wenn Sie Ihre Daten zu anderen Daten hinzufügen möchten, die in einem Umfragetool erfasst wurden. Wenn beispielsweise eine Stichprobe einer Bevölkerung in einer Umfrage ein Erlebnis mit „9“ Punkten und eine andere Stichprobe dasselbe Erlebnis mit „4“ Punkten bewertete, können Sie anhand Ihrer Daten ermitteln, wer Erlebnis A und wer Erlebnis B gesehen hat. Sie können auch Antwort-Token verwenden, um [!DNL Target] Daten in Ihr internes Data Warehouse zu exportieren. Klicken Sie einfach auf „Administration“ und schalten Sie den Schalter neben dem gewünschten Antwort-Token auf „Ein“. Erstellen Sie danach eine Aktivität. Die Daten können nun an den Drittanbieter übertragen werden. Mit Debuggingwerkzeugen können Sie überprüfen, ob [!DNL Target] die Daten exportiert.

Eine schrittweise Anleitung finden Sie unter [Antwort-Token](/help/main/administrating-target/response-tokens.md).

**Hinweis**: Ein Administrator kann das einem Drittanbieter zugeordnete Antwort-Token nur aktivieren, wenn ein Entwickler eine Partnerschaft mit diesem Drittanbieterunternehmen eingerichtet hat.

Eine schrittweise Anleitung finden Sie unter [Antwort-Token](/help/main/administrating-target/response-tokens.md).

**Erster Schritt**: Vergewissern Sie sich, dass Sie at.js Version 1.1 oder höher verwenden. Wenn Sie eine frühere Version verwenden, werden die Antwort-Token angezeigt, aber at.js kann sie nicht verwenden.

## Tipp 4: Mit Zielgruppen aus folgenden Schlüsselvariablen wird Ihre Aktivität wertvoller.

Beziehen Sie in die Erstellung Ihrer Zielgruppen für das Targeting oder Testen von Promotions und Angeboten die folgenden Variablen ein:

* Verhalten: Besuchs- und Kaufmuster auf der Site
* Referrer: Verweisende Websites und Kampagnen
* Temporär: Tageszeiten, Wochentage und saisonale Faktoren
* Offline: Besuchs- und Kaufmuster in Ladengeschäften
* Umgebung: Ursprungsland, Betriebssystem, Browsertyp

## Tipp 5: Erteilen Sie Benutzern den Zugriff, den sie für ihre Arbeit benötigen.

Erleichtern Sie Ihren Benutzern die Arbeit mit den Daten Ihrer Organisation, ohne auf Sicherheit zu verzichten. In [!DNL Target Premium] können Administratoren die Zugriffsebene ihrer internen und externen Teams genau steuern.

Weitere Informationen finden Sie unter [Enterprise-Benutzerberechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

**Hinweis**: Wenn beim Hinzufügen von Benutzern der Name eines Teammitglieds noch nicht zu Ihrer Organisation hinzugefügt wurde - dies ist häufig der Fall bei Mitarbeitern externer Unternehmen - und Sie dessen E-Mail-Adresse und Kennwort eingeben, erhält das Teammitglied den Trigger einer E-Mail-Einladung zur Teilnahme am Arbeitsbereich des Teams.

Verwenden Sie Target Standard? Auch dort können Sie Ihren Benutzern [drei Zugriffsebenen](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) zuweisen – mit schreibgeschütztem Zugriff, Editorzugriff oder Genehmigerzugriff.

## Tipp 6: Ermitteln Sie die Performance eines Angebots in der gesamten Kunden-Journey, indem Sie es auf jeder Seite der Journey testen.

Ermitteln Sie, wie ein Angebot, z. B. kostenloser Versand, in einer Kunden-Journey abschneidet, die mehrere Seiten Ihrer Website umfasst.

Eine schrittweise Anleitung finden Sie unter [Mehrseitige Aktivität](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md).

**Hinweis**: Wenn Sie nach der Angabe eines Seitenbereichs die URL ändern, wird das Erlebnis zurückgesetzt. Von Ihnen angegebene Varianzen werden dann nicht mehr angezeigt. Vergessen Sie nach einer URL-Änderung daher nicht, das Erlebnis neu zu definieren.

## Tipp 7: Testen Sie ein Angebot mit verschiedenen Zielgruppen, um festzustellen, ob die Zielgruppen unterschiedliche Vorlieben haben.

Mit Erlebnisversionen können Sie einen Test mit Varianzen für beliebig viele Zielgruppen ausführen. Sie können beispielsweise eine Banneranzeige für kostenlosen Versand erstellen – mit Bild- und Währungsvarianten für Kunden in den USA, Großbritannien und den Vereinigten Arabischen Emiraten –, ohne getrennte Tests für drei verschiedene Zielgruppen durchführen zu müssen.

Eine [ Anleitung finden Sie unter „Verschiedene Erlebniszielgruppen in ](/help/main/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md) A/B-Test“.

## Tipp 8: Sparen Sie Zeit durch die Replizierung von Aktivitätserlebnissen auf ähnlichen Seiten.

Erstellen Sie auf einer Webseite eine Varianz, zum Beispiel eine neue Schaltflächenfarbe, und wenden Sie diese automatisch auf alle Seiten an, die aus derselben Vorlage erstellt wurden. Sie können einzelne Seiten angeben oder die Varianzen auf alle ähnlichen Seiten Ihrer Website anwenden.

Eine schrittweise Anleitung finden Sie unter [Gleiches Erlebnis auf ähnlichen Seiten](/help/main/c-experiences/c-visual-experience-composer/temtest.md).

## Tipp 9: Halten Sie Ihre Zielgruppenbibliothek durch die Erstellung einmalig verwendeter Zielgruppen überschaubar.

Wenn Sie Ihr Targeting für ein Segment ausführen, von dem Sie wissen, dass Sie es nicht mehr untersuchen werden (z. B. Kunden, die von einem unerwarteten Wetterereignis betroffen sind), kann die Erstellung einer einmaligen Zielgruppe Ihnen dabei helfen, Ihre Arbeit zu erledigen, ohne Ihre Zielgruppenbibliothek zu überladen. Zielgruppen, die Sie häufiger benötigen, finden Sie dadurch leichter.

Eine schrittweise Anleitung finden Sie unter [Erstellen einer Zielgruppe „Nur Aktivität“](/help/main/c-target/creating-activity-only-audience.md).

**Expliziter Kundenwunsch**: Unsere Kunden baten uns immer wieder um eine Option, durch die Zielgruppen, die nur einmal verwendet werden, aus der automatischen Speicherung in der Zielgruppenbibliothek ausgenommen werden können. Diese Zielgruppen müssen nun nicht mehr manuell gelöscht werden, um die Bibliothek überschaubar zu halten.

## Tipp 10: Führen Sie einfache Tests durch Weglassen des Standard-QA-Prozesses schneller durch.

Es gibt nichts Schlimmeres als eine fertige Aktivität zu haben und dann Wochen auf den Abschluss des Standard-QA-Prozesses warten zu müssen. Für die meisten Aktivitäten ist eine Qualitätssicherung, bei der Sie Kollegen einige QA-Links senden, damit diese die Aktivität in verschiedenen Browsern testen, durchaus ausreichend. Aktivitäten, durch die sich die Site-Funktion erheblich ändert, werden Sie mit Sicherheit einem gründlichen QA-Prozess unterziehen. Diese komplexen Aktivitäten kommen in der Praxis jedoch eher selten vor. Auch eine bessere Berechtigungskontrolle, durch die weniger Menschen Dinge live anstoßen können, setzt sinnvolle Grenzen, und Sie erreichen damit schneller und effizienter, was Sie brauchen. Eine weitere Möglichkeit wäre die Beauftragung einer dedizierten IT-Ressource, die für einen zügigen QA-Prozess sorgt.

Eine schrittweise Anleitung finden Sie unter [Aktivitäts-QA](/help/main/c-activities/c-activity-qa/activity-qa.md).

## Tipp 11: Führen Sie Tests auf Seiten mit hohem Traffic durch, damit sie schneller statistische Bedeutung erreichen.

Viele Marketer starten Optimierungsprogramme für die Segmentierung und das Targeting von Zielgruppen, ohne zu prüfen, ob das vorhandene Traffic-Aufkommen und die verwendeten Zielgruppen innerhalb des Testzeitraums zu signifikanten Ergebnissen für ihre Optimierungs- und Konversionsziele führen. Zur Vermeidung dieses häufigen Fehlers sollten Sie sich im Voraus folgende Fragen beantworten:

* Wie viele Unique Visitors hat die Seite täglich?
* Wie hoch ist die Konversionsrate der Seite?
* Wie lange müssten Sie den Test voraussichtlich durchführen, um ihn mit einem signifikanten Ergebnis abschließen zu können?

**Tipp**: Verwenden Sie den [!DNL Adobe Target]Rechner für [Stichprobengröße](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6), um die für einen erfolgreichen Test erforderliche Stichprobengröße zu bestimmen.

## Tipp 12: Entwerfen Sie einfachere Tests, um sicherzustellen, dass Sie sie erstellen und implementieren können.

Wenn alle Aspekte eines Testentwurfs berücksichtigt werden, kann ein Plan sehr komplex werden. Entscheiden Sie nach der Testerfahrung Ihres Unternehmens und der Fähigkeit Ihrer Gruppe, die Ergebnisse zu entwerfen, zu codieren, auszuführen und zu analysieren, ob der Test zu ehrgeizig erscheint. Falls ja, seien Sie auch bereit, einen Schritt zurückzugehen und den Umfang und die Komplexität zu reduzieren. Es ist besser, bescheidener zu beginnen, als den Test gar nicht durchzuführen. Sie können keine effektive Steigerung bewirken, wenn Sie den Test nie starten. Es ist wichtig, die Bestrebungen des Teams mit den Realitäten Ihrer Ressourcen und Fähigkeiten in Einklang zu bringen.

## Tipp 13: Teilen Sie komplexe Tests in kleinere Aktivitäten auf, die erreicht werden können.

Einem großen Test mit vielen Variablen und einer komplexen Entwicklung ist in aller Regel eine weniger komplexe Reihe kleinerer Tests mit weniger Variablen vorzuziehen. Dadurch lässt sich die Auswirkung der einzelnen Variablen auf die Test-Performance wesentlich besser erkennen. Auch technische Probleme, die in der Regel erst bei größeren Projekten entstehen, reduzieren sich dadurch.

![Abbildung: Aufteilung komplexer Tests](/help/main/c-intro/assets/break-complex-tasks.png)

## Tipp 14: Maximieren Sie die Wirkung Ihrer Tests, indem Sie die Tests näher am Ende des Konversionstrichters durchführen.

Tests möglichst nahe an der Seite, auf der Besucher auf „Kauf abschließen“, „Antrag senden“ oder eine andere Art des Konversionsabschlusses klicken, haben in der Regel die wirkungsvollsten Ergebnisse. Besucher, die das Trichterende erreichen, sind meist qualifizierter, haben mehr Zeit investiert und sind bereit zu kaufen. Ein Test deren Präferenzen und Aktionen hilft Ihnen, wirklich rentable Änderungen vorzunehmen. Da die Seiten auf dem Kaufpfad für die Konversionsraten entscheidend sind, sollten auf diesen Seiten durchgeführte Tests vor dem Start mit wichtigen Stakeholdern abgesprochen werden.

![Abbildung: Konversionstrichter](/help/main/c-intro/assets/conversion-funnel.png)

## Tipp 15: Aktualisieren Sie Ihre Tests laufend, um iterative Verbesserungen zu erzielen.

Wenn sich Ihre Hypothese nicht als wahr erwiesen hat, denken Sie an Möglichkeiten, Ihren Test zu verbessern. Denken Sie daran, dass Ihr Experiment keine Zeitverschwendung war, auch wenn keines der getesteten Erlebnisse eine bessere Leistung erbrachte. Ein erfolgreicher Test bedeutet nicht immer eine Steigerung des Umsatzes oder der Konversionen. Wenn der Test tatsächlich Ihre Hypothese unterstützt, sind Sie auf dem besten Weg, eine allgemeine Theorie zu entwickeln. Aber selbst wenn Sie ein eindeutiges Gewinnerergebnis haben, hören Sie damit nicht auf. Zu oft machen Marketer den Fehler, ein Mal zu testen und dann auf diese Ergebnisse zu setzen, ohne wirklich zu verstehen, was zu dem Erfolg führte. Versuchen Sie stattdessen, die Ergebnisse in einem iterierenden Test zu rekonstruieren, um festzustellen, warum der Front-Läufer vorne war. Sie erhalten dadurch tiefere Einblicke, die Sie für zukünftige Kampagnen nutzen können.

## Tipp 16: Vergleichen Sie Tests und Personalisierungsaktivitäten, um festzustellen, wie Sie Ihr Targeting verbessern können.

Der Vergleich der Konversionsleistung verschiedener Zielgruppen in verschiedenen Tests an verschiedenen Orten kann dabei helfen, die Optimierungsstrategie eines Unternehmens zu fokussieren und zu verfeinern. Ermitteln Sie durch Testvergleiche, welche Zielgruppen für Tests am wertvollsten sind, welche Zielgruppen zielgerichtete Erlebnisse erhalten sollten und welche Erlebnisse am wahrscheinlichsten eine Antwort hervorrufen.

Ein Kunde aus dem Finanzsektor beispielsweise führte eine Kampagne zur Bewerbung einer Kreditkarte durch, die durch Tickets für professionelle Sportveranstaltungen Konversionsanreize setzte. Durch partielles Multivariate Testing seiner Landingpages gelang es dem Kunden, seine Werbebotschaft zu den Vorteilen der Kreditkarte optimal mit dem Anreiz einer kostenlosen Sportveranstaltung zu erweitern und dadurch bestimmte Zielgruppen seines Kundenstamms gezielt anzusprechen. Mit diesem Ansatz gelang es dem Unternehmen innerhalb eines durch die Sportveranstaltung festgelegten Zeitfensters, seine Konversionsrate zu steigern und die Umsätze zu maximieren.

## Tipp 17: Tests sollten nützlich sein – starten Sie einen Test nur, wenn Sie wissen, wie Sie mit den Daten umgehen.

Ein Test ist sinnlos, wenn Sie nicht genau wissen, wie Sie die Daten verarbeiten werden. Dies schließt die Kenntnis Ihrer wichtigsten Erfolgsmetrik ein, was passieren muss, um einen Gewinner voranzutreiben, wie Sie die Testergebnisse umsetzen und was Sie mit den Zielgruppeninformationen machen werden. Für einen schnellen und erfolgreichen Test ist es wichtig, dass sich alle am Test beteiligten Gruppen (Entwickler, Kreative, Testspezialisten usw.) vor dem Start des Tests über dessen Rolle im Klaren sind.

## Tipp 18: Stellen Sie vor dem Start eines Tests sicher, dass das Unternehmen auch bereit ist, den Testsieger voranzutreiben.

Erfolgreiche Optimierungsorganisationen glauben an das Konzept des Testens und wissen, dass ihre professionellen Ansichten darüber, welche Erfahrung den Test gewinnen wird, sich nicht immer als wahr erweisen. Sie bestimmen den Gewinner auf einer soliden Datengrundlage und sind bereit, das erfolgreichste Erlebnis nach dem Eintreffen der Ergebnisse live umzusetzen, auch wenn es nicht ihren Erwartungen entspricht oder widersinnig erscheint.

Beispielsweise demonstrierte ein Kunde von Adobe aus dem Gesundheitswesen erst kürzlich den Wert von Tests, als sich in seinem Test zeigte, dass ein Hero-Banner, das das Team als klaren Favoriten betrachtete, die Konversionsrate tatsächlich negativ beeinflusste. Wenn Ihr Unternehmen Tests noch nicht vollständig angenommen hat, ist es am besten, zunächst einfachere, kleinere Tests durchzuführen, damit Änderungen aus Testergebnissen schrittweise vorgenommen werden können.

## Tipp 19: Kommunizieren Sie in Ihrer Organisation, dass Sie einen Test gestartet haben, um Irritationen aufgrund von Site-Änderungen zu vermeiden.

Einer der Vorteile von Aktivitäten, die Sie mit QA-Parametern einrichten, besteht darin, dass Sie diese Links mit allen Mitarbeitern Ihres Teams austauschen können. Sie sensibilisieren mehr Personen für die Aktivität und stellen sicher, dass sie nicht davon ausgehen, dass die Site nicht richtig funktioniert, wenn sie auf eine Testvariante stoßen.

Wenn Sie Ihre Organisation nach Abschluss der Tests über Kampagnenstarts, Testergebnisse und insbesondere die gewonnenen Erkenntnisse informieren, fördern Sie das Bewusstsein für die Tests und das Interesse an deren Ergebnissen. Durch die Weitergabe der Ergebnisse an alle Mitarbeiter des Unternehmens wird auch vermieden, dass eine Hypothese erneut getestet wird. Jeder in der Organisation lernt daraus, was funktioniert, und kann mit diesen Erkenntnissen seine eigenen Vorstellungen dessen, was funktioniert, grundlegend hinterfragen. Es empfiehlt sich, eine Vorlage vorzubereiten, die Sie jedes Mal verwenden können, um Ihre Erkenntnisse und wichtigen Erkenntnisse zu teilen.
Ziehen Sie auch in Erwägung, die Testerfahrungen Ihres Unternehmens in einem Handbuch oder einer Microsoft PowerPoint-Mappe zusammenzustellen und diese(s) für jeden im Unternehmen freizugeben.

## Tipp 20: Erweitern Sie Ihre Tests auch auf mobile Funktionen, um innovativere mobile Erlebnisse zu schaffen.

Benutzererlebnisse auf Tablets und Smartphones finden im Wesentlichen über Touch-Elemente statt – nicht wie auf Desktops über Mausklicks und Tastatureingaben. Nutzen Sie für Erlebnisse auf Mobilgeräten die mobilen Anzeigesteuerelemente einschließlich Streichen, Tippen, Ziehen und mit zwei Fingern Auseinander- und Zusammenziehen. Verwenden Sie zur Steuerung der Interaktion und Navigation einfache, große Schaltflächen – z. B. für den Warenkorb oder die Videowiedergabe. Statten Sie Ihre Shopping-App für Mobilgeräte mit reichhaltigem Bildmaterial zu Ihren Produkten aus, das für den Gerätetyp optimiert ist. Suchen Sie nach jeder Gelegenheit, das Benutzererlebnis auf eingebettete, große Viewer oder interaktive Zoom- und Schwenkfunktionen im Vollbildmodus, 360-Grad-Rotationen und erweiterte Videofunktionen umzuleiten.

## Tipp 21: Helfen Sie mobilen Besuchern durch Optimierung der mobilen Suchfunktion, das Gewünschte zu finden.

Mobilgerätebenutzer gehen in der Regel sehr zielstrebig vor. Die meisten von ihnen informieren sich vor jedem anderen Schritt auf einer mCommerce-Site zunächst über die Suchfunktion. Die Optimierung der Suche auf Mobilgeräten ist daher entscheidend. Zur Suchmaschinenoptimierung (SEO) für Mobilgeräte sollten Sie explizite Navigationshilfen für einfaches Browsen integrieren. Implementieren Sie in Sucheingabefeldern zudem automatische Empfehlungen und Autokorrektur, um der unkomfortablen Texteingabe auf Mobilgeräten entgegenzuwirken. Stellen Sie überzeugende und relevante Suchergebnisse bereit, die an die Bildschirmgröße und -position angepasst sind.

## Tipp 22: Erreichen Sie mobile Zielgruppen in Mobile-SEM-Kampagnen mit einem tageszeitlich angepassten Targeting.

Erfahren Sie, wie und wann Sie Ihre Zielgruppe erreichen und wie Sie Ihre täglichen Werbeausgaben besser verwalten können, indem Sie Ihre Mobile-Kampagnen den ganzen Tag über in verschiedene Segmente unterteilen.

Viele Marketer machen den Fehler, für die Stunden, in denen bestimmte Geräte am meisten genutzt werden, nicht ausreichend Budget zur Verfügung zu stellen, um diesen Stimmanteil zu erfassen. So bleiben Umsätze und unzählige Leads oft einfach auf dem Tisch liegen.

Tablets werden beispielsweise bevorzugt abends genutzt, und viele Benutzer browsen dort während des Fernsehens im Internet. Smartphones werden dagegen eher tagsüber von unterwegs aus genutzt. Spitzenkonversionszeiten sind auch branchenabhängig. Daher ist es wichtig zu verstehen, wann Ihre Unique Customers am ehesten handeln.

## Bitte beachten Sie

Berücksichtigen Sie die folgenden Erfahrungswerte, bevor Sie zum nächsten Kapitel „Ideen für Test- und Personalisierungsaktivitäten“ übergehen.

### Achten Sie im Design Ihrer Tests nicht auf dekorative Details, sondern auf den Zweck.

* Richten Sie den Flow bewusst auf die Erzielung von Konversionspunkten.
* Nutzen Sie die Ihnen verfügbaren Flächen zu Ihrem Vorteil.
* Setzen Sie Bilder gezielt als funktionale Elemente und nicht als Dekoration ein.
* Gestalten Sie Ihr Angebot in einer vereinfachten Kopie übersichtlich, klar und reibungslos.
* Verwenden Sie effektive Aktionsaufrufe (CTAs), wenn der Benutzer aktiv werden muss.
* Gestalten Sie Ihre Angebote, sofern möglich, durch benutzergenerierte Inhalte glaubwürdig.

### Vereinfachen Sie Ihre Website.

* Kunden nicht „zwingen“, zu lesen. Das werden sie nicht.
* Erleichtern Sie ihm das Durchscannen.
* Verwenden Sie klar gegliederte Blöcke mit Aufzählungszeichen.
* Achten Sie in Ihrer Kopie auf einen klaren, sequenziellen Gedankenablauf.

### Verwenden Sie effektive Aktionsaufrufe (CTAs).

* Versetzen Sie sich in die Lage des Kunden.
* Verwenden Sie eine aktionsorientierte Sprache.
* Überlegen Sie sich, was den Kunden zur Konversion motivieren könnte.
* Adressieren Sie auch das Ergebnis einer Konversion.
* Stellen Sie sicher, dass CTAs deutlich sichtbar sind!
