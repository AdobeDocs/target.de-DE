---
keywords: Target Standard; Recommendations; Target Premium; Automated Personalization; automatisches Targeting; Berechtigungen; Was ist Adobe Target?
description: Lernen Sie die Grundlagen von Adobe [!DNL Target] Standard und Adobe [!DNL Target] Premium kennen. [!DNL Target] Premium umfasst erweiterte Funktionen, die nicht im Standardprodukt verfügbar sind.
landing-page-description: Personalisieren Sie die Erlebnisse Ihrer Kunden, um den Umsatz Ihrer Websites und Mobile Sites sowie Mobile Apps, Social Media und anderer digitaler Kanäle zu maximieren.
short-description: Personalisieren Sie die Erlebnisse Ihrer Kunden, um den Umsatz Ihrer Websites und Mobile Sites sowie Mobile Apps, Social Media und anderer digitaler Kanäle zu maximieren.
title: Was ist Target?
feature: Overview
exl-id: 0e729c71-618b-4ab8-93a3-d37e73ec2740
TQID: https://experienceleague.adobe.com/Mr8fwY1FNfJShSezC50YX1QeBagmuovUySsQUO8jPqo
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: 2cecb1f8ae52fd6c47e543710bb14e00503c06ef
workflow-type: tm+mt
source-wordcount: '1644'
ht-degree: 33%
---
# Einführung in [!DNL Target]


>[!CONTEXTUALHELP]
>id="target_sample_size_ab_daily_traffic"
>title="Täglicher Datenverkehr"
>abstract="Wie viele Benutzer pro Tag in Ihr Experiment eintreten. Wenn Sie Ihren täglichen Traffic nicht kennen, wählen Sie oben \„Traffic-Volumen\&quot; und der Rechner wird es mit Ihren anderen Eingaben lösen."

>[!CONTEXTUALHELP]
>id="target_sample_size_setup"
>title="Einrichten des Tests"
>abstract="Diese Felder definieren Ihren A/B-Test, was Sie erwarten und wie zuversichtlich Sie im Ergebnis sein müssen. Das Feld, das an das oben ausgewählte gebunden ist, wird automatisch gelöst. Füllen Sie den Rest mit den erwarteten Werten aus."

>[!CONTEXTUALHELP]
>id="target_sample_size_number_experiences"
>title="Anzahl der Erlebnisse"
>abstract="Anzahl der Varianten im Experiment, einschließlich der Kontrolle. Ein A/B-Test hat zwei Arme. Fünf Varianten plus ein Steuerelement ergibt 6. Mehr Waffen erfordern proportional mehr Verkehr, um die statistische Leistung aufrechtzuerhalten."

>[!CONTEXTUALHELP]
>id="target_sample_size_duration"
>title="Dauer des A/B-Tests"
>abstract="Wie viele Tage Ihr Experiment ausgeführt wird. Längere Dauer geben Ihrem Experiment mehr Zeit, Daten zu erfassen, sodass Sie kleinere Effekte zuverlässig erkennen können. Kürzere Zeiträume erfordern größere Effekte oder mehr Traffic pro Tag, um ein zuverlässiges Ergebnis zu erzielen."

>[!CONTEXTUALHELP]
>id="target_sample_size_minimum_detectable_effect"
>title="minimale feststellbare Wirkung"
>abstract="Die kleinste erkennenswerte Verbesserung, die minimale Änderung in Ihrer Metrik, auf die Sie reagieren würden. Dies ist die Größe des Anstiegs in Prozentpunkten, nicht die prozentuale Änderung im Verhältnis zur Grundlinie. Wenn Ihre Grundlinie beispielsweise 5 % beträgt und ein Anstieg um 1 Prozentpunkt von Bedeutung ist, geben Sie 1 ein."

>[!CONTEXTUALHELP]
>id="target_sample_size_expected_improvement"
>title="Erwartete Verbesserung"
>abstract="Die vom Experiment erwartete Verbesserung."

>[!CONTEXTUALHELP]
>id="target_sample_size_variance"
>title="Variance"
>abstract="Wie verteilt die Werte Ihrer Metrik sind, nicht ihr Durchschnitt. Eine Metrik wie eine Klickrate (meistens 0 und 1 s) hat eine niedrige Varianz, eine Metrik wie der Umsatz pro Benutzer (einige wenige hohe Ausgaben, viele niedrige) kann eine viel höhere Varianz haben. Wenn Sie sich nicht sicher sind, behalten Sie den Standardwert 1 bei."

>[!CONTEXTUALHELP]
>id="target_sample_size_confidence_level"
>title="Konfidenzniveau"
>abstract="Wie zuversichtlich man sein muss, dass ein Ergebnis nicht bloß eine Zufallszahl ist, bevor man es als real bezeichnet, der Schwellenwert für statistische Signifikanz. Ein Konfidenzniveau von 95 % bedeutet, dass höchstens eine 5 %ige Wahrscheinlichkeit besteht, dass ein falsch positives Ergebnis vorliegt. Höhere Werte verringern die Anzahl falsch positiver Ergebnisse, erfordern jedoch mehr Daten."

>[!CONTEXTUALHELP]
>id="target_sample_size_statistical_power"
>title="Teststärke"
>abstract="Die Wahrscheinlichkeit, einen Effekt zu erkennen, wenn es wirklich existiert, die Empfindlichkeit des Experiments. 80 % Leistung bedeutet, dass eine Wahrscheinlichkeit von 80 % besteht, einen echten Effekt zu erkennen. Höhere Leistung reduziert Fehlalarme, erfordert jedoch mehr Traffic oder eine längere Laufzeit."

>[!CONTEXTUALHELP]
>id="target_sample_size_traffic_mode"
>title="Verkehrsmodus"
>abstract="Wie Benutzer in Ihr Experiment eintreten. Fortlaufend: Benutzende treten während der Experimentdauer täglich ein. Der Traffic verlagert sich automatisch auf leistungsfähigere Varianten, wenn Ergebnisse eintreten."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="Metriktyp"
>abstract="Welche Art von Metrik messen Sie? Prozentsatz: Verwenden Sie dies für binäre Ergebnisse wie Klicks oder Konversionen, bei denen jeder Benutzer etwas tut oder nicht tut. Zahl: Verwenden Sie diese Option für Metriken wie Umsatz oder Seitenansichten, bei denen der Wert von Benutzer zu Benutzer stark variieren kann."

>[!CONTEXTUALHELP]
>id="target_sample_size_auto_daily_traffic"
>title="Täglicher Datenverkehr"
>abstract="Wie viele Benutzer pro Tag in Ihr Experiment eintreten. Wird für kontinuierliche Experimente verwendet, die über mehrere Tage laufen, wobei sich der Traffic automatisch in Richtung leistungsfähigerer Varianten verschiebt, wenn Ergebnisse eintreten."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_metric_rate"
>title="Baseline-Metrikrate"
>abstract="Aktuelle Leistung vor Beginn des Experiments, Durchschnitt des Kontrollarms. Immer erforderlich. Geben Sie als Prozentsatz für Prozentmetriken ein: Wenn 5 % der Besucher heute auf „Kaufen“ klicken, geben Sie 5 ein. Geben Sie für Zählmetriken den unformatierten Dezimalwert ein."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="Primäre Metrik"
>abstract="Die primäre Metrik wird automatisch aus den Reporting-Einstellungen abgerufen. Um Änderungen vorzunehmen, ändern Sie die Zielmetrik unter Ziele und Einstellungen ."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="Hypothese"
>abstract="Die Hypothese ist eine von Ihnen definierte Aussage, die das erwartete Ergebnis des Experiments erklärt. Geben Sie eine Beschreibung dessen an, was wo geändert wird, und geben Sie an, welche Metrik sich wie ändern soll."

>[!CONTEXTUALHELP]
>id="target_ai_insights_insights"
>title="Einblicke"
>abstract="Experimenterkenntnisse sind die Erkenntnisse, die KI gewinnt, wenn die Experimentdaten statistische Signifikanz erreicht haben."

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="Opportunities"
>abstract="Experimentmöglichkeiten sind von der KI vorgeschlagene Behandlungsideen, die auf Mustern der KI basieren, die in Ihren Experiment-Screenshots und -Ergebnissen gefunden wurden."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="Abwandlungsdetails"
>abstract="Behandlungsdetails zeigen Bilder davon, wie eine Behandlung aussieht, wenn ein Benutzer für sie qualifiziert ist. Sie können diese Bilder für alle Experimente überprüfen. Bei einigen Experimenten werden Sie möglicherweise aufgefordert, das Bild zu bestätigen oder es bei Bedarf zu ersetzen."

[!DNL Adobe Target], Teil der [!DNL Adobe Experience Cloud], bietet umfassende Tools zur Personalisierung von Kundenerlebnissen über Web, mobile Sites, Apps, soziale Medien und andere digitale Kanäle.

[!DNL Target] trägt zur Umsatzmaximierung bei und kann als [!DNL Target Standard] oder [!DNL Target Premium] lizenziert werden.

## [!UICONTROL Target Standard] {#section_ACD5EFF17AAB4E979CBEFA0145CCD905}

[!DNL Target Standard] ist das Frontend zu [!DNL Adobe Target] und ermöglicht die visuelle Erstellung und Verwaltung von A/B-Tests und regelbasierten Targeting-Aktivitäten. [!DNL Target] unterstützt das Einfügen von benutzerdefiniertem Code innerhalb und außerhalb des Workflows [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). [!DNL Target Standard] bietet eine vereinfachte Implementierungsstrategie für Ihre digitalen Eigenschaften, bei der eine einzige Codezeile auf jeder Seite die gesamte Kommunikation zwischen Ihrer Site und [!DNL Target] verwaltet.

In [!DNL Target Standard] sind die Best Practices der Branche integriert, sodass sie sich sowohl für neue als auch erfahrene Benutzer eignen. Mit dem [!DNL Adobe Experience Cloud] können Sie mühelos Daten und Ergebnisse freigeben und mit Team-Mitgliedern zusammenarbeiten.

## [!DNL Target Premium] {#premium}

[!BADGE Premium]{type=Positive}

[!DNL Target Premium] ist ein erweitertes -Angebot, das gegen eine Lizenz zusätzliche Premium-Funktionen zu [!DNL Target Standard] hinzufügt. Alle [!DNL Target Premium] Artikel in [!DNL Target] Handbüchern enthalten das [!UICONTROL Premium]-Badge oben auf jeder Seite oder inline in der Nähe des betroffenen Textes. Das [!UICONTROL Premium]-Badge kann angeklickt werden und enthält Links zu diesem Abschnitt.

**[!DNL Target Premium]umfasst die folgenden Funktionen:**

### [!UICONTROL Automatisierte Personalisierung]

[[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) (AP) verwendet fortschrittliche Machine-Learning-Algorithmen, um personalisierte Erlebnisse bereitzustellen und die Konversionsraten für digitale Interaktionen zu verbessern.

AP zeichnet Besucheraktivitäten auf und erstellt Profile, um Inhalte auf ähnliche Besucher auszurichten. AP verfolgt die Reaktionen auf Inhalte für Einzelpersonen und die Population und verwendet dabei eine ausgefeilte Modellierung, um jeden Besucher basierend auf allem, was über ihn bekannt ist, automatisch anzusprechen.

AP ist vollständig automatisiert, lernt kontinuierlich mit minimaler menschlicher Analyse. Sie erstellt Modelle, um zu bestimmen, an welchen Produkten ein Besucher interessiert sein könnte, und um Informationen in Besucherprofilen zu sammeln und zu speichern. Mehrere Algorithmen stellen das beste Modell für Ihr System sicher.

### [!UICONTROL Automatisches Targeting]

[Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) nutzt fortschrittliche Machine-Learning-Algorithmen zur Identifizierung von Vermarkter-definierten Erlebnissen mit hoher Leistung. Anschließend wird jedem Besucher das passendste Erlebnis auf der Grundlage individueller Kundenprofile und des Verhaltens früherer Besucher mit ähnlichen Profilen geboten. [!UICONTROL Automatisches Targeting] hilft Ihnen bei der Personalisierung Ihrer Inhalte und steigert dadurch Ihre Konversionen.

### Recommendations

[Recommendations](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0)-Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten für Ihre Kunden interessant sein könnten. [!UICONTROL Recommendations] helfen, Kunden zu relevanten Elementen zu führen, von denen sie andernfalls möglicherweise nichts gewusst hätten.

Eine Empfehlung bestimmt, wie ein Produkt einem Kunden je nach dessen Aktivitäten auf der Site vorgeschlagen werden soll. Beispiel:

* Regen Sie Personen, die einen Rucksack kaufen, dazu an, Wanderschuhe und Wanderstöcke zu kaufen.

  Erstellen Sie mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Kriteriums eine Empfehlung, die Artikel anzeigt, welche oft zusammen gekauft werden.

* Steigern Sie die Zeit, die ein Besucher auf Ihrer Medienwebsite verbringt, indem Sie Videoinhalte empfehlen, die den gerade angesehenen Videos ähneln.

  Erstellen Sie mithilfe des „Personen, die dies angesehen haben, sahen auch“-Kriteriums eine Empfehlung, die andere Videos vorschlägt.

* Empfehlen Sie Kunden, die sich Informationen über Sparpläne bei Ihrer Bank angesehen haben, Informationen zu IRA-Konten.

  Zeigen Sie mithilfe des „Personen, die diesen Artikel angesehen haben, kauften auch“-Kriteriums andere Produkte, die von Personen gekauft wurden, nachdem sie ein Produkt angesehen haben, ohne dabei das erste Produkt in den Empfehlungen anzuzeigen.

### Empfehlungen als Angebot

[Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md) ermöglicht Ihnen die Einbeziehung von Recommendations in [!UICONTROL A/B-Test], [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting] und [!UICONTROL Experience Targeting] (XT).

Diese Funktion eröffnet völlig neue Funktionen wie z. B.:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie einfach mit Empfehlungen auf der Seite, einschließlich der Reihenfolge mehrerer Empfehlungen.
* Übertragen Sie Traffic mithilfe der automatischen Zuordnung automatisch an das [!UICONTROL &#x200B; Recommendations-Erlebnis mit &#x200B;] besten Leistung.
* Dynamische Zuweisung von Besuchern zu benutzerspezifischen Recommendations-Erlebnissen basierend auf deren individuellen Profilen mithilfe [!UICONTROL automatischen Targetings].

### Enterprise-Benutzerberechtigungen

Mit [Enterprise-Benutzerberechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838) können Sie verschiedene Profile erstellen (in der [!DNL Adobe Admin Console for Enterprise] als „Produktprofile“ bezeichnet). [!UICONTROL Enterprise-Benutzerberechtigungen] ermöglichen es Ihnen, einem einzelnen Benutzer unterschiedliche Berechtigungen zuzuweisen, die dessen Zugriffsrechte für jedes Projekt festlegen. Diese voneinander unabhängigen Projekte funktionieren ähnlich wie Report Suites in [!DNL Adobe Analytics]. Jedes Projekt verfügt über bestimmte Benutzer mit bestimmten Rollen, die einer bestimmten Reihe Berechtigungen entsprechen. Damit können Kunden die Anzeige-, Bearbeitungs-, Genehmigungs- und Veröffentlichungsrechte ihrer Benutzer einschränken. Sie können Benutzer auch nach Region, Umgebung (dev/stage/prod), Kanal oder anderen benutzerspezifischen Kriterien einschränken.

## Beta-Funktionen {#beta}

[!BADGE Beta]{type=Informative}

Das [!DNL Adobe Target]-Team bietet ausgewählten Kunden häufig neue Funktionen zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen für alle Kunden in zukünftigen [!DNL Target Standard/Premium]-Versionen aktiviert und in den Versionshinweisen angekündigt.

Artikel in [!DNL Target] Handbüchern, die Beta-Funktionen beschreiben, enthalten das Beta-Badge oben auf jeder Seite oder inline in der Nähe des betroffenen Textes. Das Beta-Badge kann angeklickt werden und enthält einen Link zu diesem Abschnitt.

## Recommendations Classic {#section_9554068100054D2DBDB298CBE5A0E413}

>[!IMPORTANT]
>
>[!DNL Recommendations Classic] ist ein älteres Produkt, das nicht mehr für neue Kunden lizenziert wird. Zur Optimierung Ihrer [!DNL Recommendations]-Ergebnisse empfehlen wir Ihnen ein Upgrade auf die oben beschriebenen, in [!DNL Adobe Target Premium] enthaltenen [!DNL Recommendations]-Aktivitäten.

[!DNL Recommendations Classic] zeigt automatisch Produkte oder Inhalte an, die ausgehend von der bisherigen Benutzeraktivität auf Ihrer Site für die betreffenden Kunden von Interesse sein könnten. Empfehlungen lenken Kunden zu Artikeln, von denen sie womöglich noch nichts wissen. Dies führt zu mehr Umsatz auf Ihrer Site.

Weitere Informationen finden Sie in der [Dokumentation zu Recommendations Classic](/help/main/assets/adobe-recommendations-classic.pdf).

## Experience League: Das Adobe [!DNL Target] Welcome Kit {#kit}

Dieses Welcome Kit erleichtert Ihnen die Erstellung Ihres Optimierungs- und Personalisierungsprogramms in [!DNL Adobe Target]. In diesem Welcome Kit sind die wichtigsten Informationen, Tools und Ressourcen zusammengestellt. Damit haben Sie Ihre erste [!DNL Target]-Aktivität im Handumdrehen vorbereitet und gestartet. Das Kit enthält Ideen für kurzfristige schnelle Erfolge, aber auch für langfristige Optimierungsstrategien.

[Das Adobe Target Welcome Kit](/help/main/c-intro/target-welcome-kit.md)

## Schulungsvideo: Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

Im folgenden Video wird erklärt, welche Aktivitätstypen in [!DNL Target Standard/Premium] verfügbar sind und wie der angeleitete dreistufige Workflow von [!DNL Target] dazu beiträgt, dass Sie Ihre Ziele für Ihre Site erreichen.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)


