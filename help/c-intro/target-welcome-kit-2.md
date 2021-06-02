---
keywords: Welcome Kit; Target Welcome Kit; Intro; Einführung; Erste Schritte
description: Hier erhalten Sie einen Überblick über Adobe Target. Sie erfahren, welche Aktivitäten, Kanäle und Integrationen es gibt, wie die Lösung implementiert wird und vieles mehr.
title: Wo finde ich eine übersichtliche Einführung in Target?
feature: Überblick
exl-id: 19238d4c-b7e1-418d-96e5-c46a3769f7bf
translation-type: ht
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: ht
source-wordcount: '2520'
ht-degree: 100%

---

# Kapitel 2: Adobe [!DNL Target] auf einen Blick

Bevor Sie mit [!DNL Adobe Target] beginnen, sollten Sie sich in dieser Übersicht mit der Lösung vertraut machen. In diesem Kapitel erfahren Sie mehr über die wichtigsten Funktionen der Lösung, die Marken-Touchpoints, auf denen Sie diese Lösung verwenden können, Implementierungsoptionen, wichtige Funktionen und Workflows der Benutzeroberfläche, Governance-Features und deren Rolle in der [!DNL Adobe Experience Cloud]. Sofern nicht mit einem [!DNL Adobe Target Premium]-Badge versehen, sind die in diesem Kapitel beschriebenen Funktionen sowohl in [!DNL Adobe Target Premium] als auch in [!DNL Adobe Target Standard] verfügbar. Weitere Informationen finden Sie unter [Einführung in Target](/help/c-intro/intro.md).

## Funktionen und Aktivitäten

Tests und Personalisierung sind die beiden übergeordneten Funktionen von [!DNL Target], die Sie beim Erstellen Ihrer „Aktivitäten“ in [!DNL Target] verwenden können. Möglicherweise wird der Begriff „Test“ synonym mit „Optimierung“ und „Personalisierung“ verwendet, und diese beiden Begriffe sind wiederum ein Synonym für „Targeting“.

In einer Testaktivität vergleichen Sie eine Varianz eines digitalen Erlebnisses mit einer oder mehreren anderen Varianzen, um festzustellen, welche dieser Varianzen die meisten Besucher zur gewünschten Aktion veranlasst. [!DNL Target] bietet die folgenden Testfunktionen: A/B-Tests, Multivariate Testing (MVT) und automatische Zuordnung.

Mit einer Personalisierungsaktivität bieten Sie ein digitales Erlebnis, das auf eine bestimmte Besuchergruppe oder auf einzelne Besucher zugeschnitten ist. [!DNL Target] bietet die folgenden Personalisierungsfunktionen: Erlebnis-Targeting, automatisches Targeting, Automated Personalization und Recommendations.

Weitere Informationen zu diesen Funktionen, deren Anwendungsbereichen und deren Verwendung finden Sie unter [Target-Aktivitätstypen](/help/c-activities/target-activities-guide.md).

| Aktivitätstyp | Details |
| --- | --- |
| A/B-Tests | Vergleichen Sie zwei oder mehr Varianzen Ihrer Erlebnisse oder Angebote auf Ihrer Website oder anderen digitalen Kunden-Touchpoints, um zu ermitteln, welche Varianz während eines vorab festgelegten Testzeitraums Ihre wichtigsten geschäftlichen Messwerte am meisten verbessert. A/B-Tests eignen sich für groß angelegte Änderungen, zum Beispiel für neue Webseitenlayouts, neue Ansätze der Site-Navigation oder in großem Maßstab geänderte Elemente eines digitalen Erlebnisses wie Kopievarianten, Bilder und Steuerelemente für Aktionsaufrufe. [Mehr Info](/help/c-activities/t-test-ab/test-ab.md). |
| Automatische Zuordnung | Identifizieren Sie mit dieser Funktion das beste Erlebnis aus zwei oder mehr Erlebnissen und ordnen Sie dem Gewinner automatisch mehr Traffic zu, um die Konversionen während der Fortführung des Tests und des maschinellen Lernens zu steigern. Diese Funktion greift auf die künstliche Intelligenz von [!DNL Adobe Sensei] zurück. [Mehr Info](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| Automatisches Targeting<br>(Premium) | Nutzen Sie in [!DNL Target] die KI-Funktionen von Adobe Sensei, um für jeden Besucher aus mehreren Erlebnissen das beste zu ermitteln und bereitzustellen – auf der Grundlage seines persönlichen Kundenprofils und des Verhaltens früherer Besucher mit ähnlichen Profilen. Automatisches Targeting ermöglicht Personalisierung in jedem Maßstab. [Mehr Info](/help/c-activities/auto-target/auto-target-to-optimize.md). |
| Automated Personalization<br>(Premium) | Nutzen Sie die fortschrittlichen Machine Learning-Algorithmen und die Automatisierung von [!DNL Adobe Sensei], um verschiedene Kombinationen aus Bildern, Kopien und anderen Elementen in einem Angebot zu prüfen und für jeden Besucher die beste Kombination hinsichtlich der Erreichung Ihrer Geschäftsziele bereitzustellen (z. B. mehr Konversionen oder höhere Umsätze pro Besucher). [Mehr Info](/help/c-activities/t-automated-personalization/automated-personalization.md). |
| Erlebnis-Targeting (XT) | Stellen Sie einer bestimmten Zielgruppe Inhalte auf Basis benutzerdefinierter Regeln und Kriterien bereit. In dem Wissen, dass Ihre Zielgruppen für Sie wertvoll sind, ist **[!UICONTROL Erlebnis-Targeting]** extrem hilfreich für die Ausrichtung bestimmter Erlebnisse oder Inhalte an bestimmten Zielgruppen. Sie entwickeln dabei ein Gespür dafür, welche Erlebnisse bei welchen Zielgruppen Anklang finden. [Mehr Info](/help/c-activities/t-experience-target/experience-target.md). |
| Multivariate Testing (MVT) | Vergleichen Sie alle möglichen Kombinationen der verschiedenen Elemente auf Ihrer Seite oder in Ihrem digitalen Erlebnis – z. B. drei verschiedene Hintergrundbilder, zwei Varianzen einer Kopie und zwei verschiedene Schaltflächenfarben. MVT ermittelt, welche Kombination bei einer bestimmten Zielgruppe am besten funktioniert und welche Elemente sich am meisten auf das Ergebnis auswirken. [Mehr Info](/help/c-activities/c-multivariate-testing/multivariate-testing.md). |
| Recommendations<br>(Premium) | Nutzen Sie die KI-Funktionen von Adobe Sensei für automatische Produkt- oder Inhaltsempfehlungen auf Basis früherer Aktivitäten des Besuchers oder anderer Kunden. [Mehr Info](/help/c-recommendations/recommendations.md). |

## Kanäle

Mit [!DNL Target] können Sie digitale Erlebnisse praktisch überall testen und personalisieren – auf herkömmlichen digitalen Touchpoints wie Ihrer Website, Ihrer mobilen Site und Ihrer mobilen App, aber auch auf Touchpoints wie Kiosks, E-Mails, IoT-Geräten, Spielekonsolen und sogar Sprachassistenten wie Alexa und Cortana. Viele Unternehmen verwenden [!DNL Target] bereits auf ihrer Website. Jüngste Studien deuten jedoch darauf hin, dass weitaus mehr Menschen über Mobilgeräte auf Marken zugreifen. Auf die Optimierung Ihrer mobilen Kanäle dürfen Sie daher keinesfalls verzichten. Idealerweise vereinheitlichen Sie die Besuchererlebnisse auf all Ihren Touchpoints, um ein nahtloses, konsistentes Erlebnis zu bieten.

| Kanal | Details |
| --- | --- |
| Website | [!DNL Target] kann für die Ausführung von A/B-Tests, Multivariate Testing (MVT) sowie Erlebnis-Targeting-, automatische Zuordnungs-, automatische Targeting-, Automated Personalization- und Recommendations-Aktivitäten auf Seiten Ihrer mehr- oder einseitigen Anwendungen und mobilen Websites verwendet werden, um Besucher- und Kundeninteraktion zu verbessern und Konversionen und Umsätze zu steigern. |
| Mobiles Web | [!DNL Target] kann auf Ihren mobilen Webseiten für die gleichen Aktivitäten verwendet werden wie auf Websites, um auch dort die Besucher- und Kundeninteraktion zu verbessern und Konversionen und Umsätze zu steigern. |
| Mobile App | [!DNL Target] kann zum Testen und Personalisieren der Erlebnisse in mobilen Apps auf Grundlage des Benutzerverhaltens und des mobilen Kontexts verwendet werden. Mit [!DNL Target] können Sie mithilfe iterativer Tests, Erlebnis-Targeting und KI-basierter Personalisierung überzeugende Interaktionen bereitstellen, die die Konversionsrate steigern. Für mobile Apps müssen Sie [!DNL Target] über das Adobe Mobile Services SDK verwenden. |
| IoT/An jedem Ort | [!DNL Target] bietet eine serverseitige Implementierung. Damit können Sie dieselben Test- und Personalisierungsfunktionen, die Sie für Aktivitäten auf Ihrer herkömmlichen Website, auf Ihrer mobilen Site und in mobilen Apps verwenden, auch in E-Mails und auf Touchpoints nutzen, wenn kein Browser zur Verfügung steht oder kein JavaScript-Code verwendet wird. Sie können daher auch Kiosks, Set-Top-Boxen, Spielekonsolen, Sprachassistenten und andere nicht traditionelle Touchpoints testen und personalisieren. |

## Implementierungen

Vermutlich möchten Sie [!DNL Target] zum Testen und Personalisieren vieler verschiedener digitaler Touchpoints verwenden, darunter herkömmliche Websites, Websites und Apps für Mobilgeräte, aber auch Touchpoints, für die kein Browser zur Verfügung steht oder kein JavaScript-Code verwendet wird. In einigen Fällen fordern interne oder externe Richtlinien zusätzliche Kontroll- und Sicherheitsstufen. Eventuell verwenden Sie auch Prozesse, die aus Leistungsgründen auf einem Backend-Server ausgeführt werden müssen. Diese Vielzahl an Einsatzmöglichkeiten unterstützt [!DNL Target] durch verschiedene Implementierungsmöglichkeiten: clientseitig, serverseitig oder als Hybridlösung.

| Implementierungstyp | Details |
| --- | --- |
| Clientseitig | Bei dieser Implementierung von [!DNL Target] stellt [!DNL Target] die mit einer Aktivität verbundenen Erlebnisse direkt auf dem Client-Browser bereit. Der Browser entscheidet, welches Erlebnis angezeigt werden soll, und zeigt es an. Bei der clientseitigen Implementierung können Sie einen WYSIWYG-Editor, Visual **[!UICONTROL Experience Composer]** (VEC) oder eine nicht visuelle Schnittstelle, den **[!UICONTROL formularbasierten Experience Composer]**, zur Erstellung Ihrer Tests und Personalisierungserlebnisse verwenden. [Mehr Info](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). |
| Serverseitig | Bei der serverseitigen Implementierung von [!DNL Target] fordert ein Client-Gerät über Ihren Server ein Erlebnis an. Diese Anforderung sendet der Server an [!DNL Target], und [!DNL Target] sendet die Antwort an den Server zurück. Ihr Server entscheidet dann, welches Erlebnis zum Rendern an das Client-Gerät gesendet werden soll. Das Erlebnis muss nicht in einem Browser angezeigt werden. Es kann auch in einer E-Mail oder an einem Kiosk, über einen Sprachassistenten oder über ein anderes nicht visuelles Erlebnis oder nicht browserbasiertes Gerät angezeigt werden. Da sich Ihr Server zwischen dem Client und [!DNL Target] befindet, ist diese Art der Implementierung auch dann optimal, wenn Sie mehr Kontrolle und Sicherheit benötigen oder komplexe Backend-Prozesse haben, die auf Ihrem Server ausgeführt werden sollen. [Mehr Info](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Hybridimplementierung | Bei dieser Art der Implementierung wählen Sie je nach Anwendungsfall den geeignetsten Implementierungsansatz. Beispielsweise können Sie für einen A/B-Test eines Angebots in einem Hero-Banner auf der Homepage eine clientseitige Implementierung verwenden, parallel dazu aber auch eine serverseitige Implementierung, um die internen Suchergebnisse zu bestimmen, die in einem Client-Browser angezeigt werden, die Erlebnisse, die ein Smart Car-Dashboard rendert, oder Sprachantworten, die von einem Sprachassistenten zurückgegeben werden. |

## Aktivitätselemente

In [!DNL Target] können Sie Personalisierungs- und Optimierungsaktivitäten erstellen, aber auch Aktivitäten, die Ihren Personalisierungsansatz optimieren. Jede Aktivität enthält wesentliche Elemente: die Erlebnisse oder Angebote, die Sie testen oder personalisieren, die Zielgruppen oder Einzelpersonen, denen Sie ein Erlebnis bereitstellen, die Metriken, mit denen Sie die Auswirkungen der Aktivität messen, und die Berichte, die diese Auswirkungen visuell darstellen.

| Elementtyp | Details |
| --- | --- |
| Erlebnisse | Ein Angebot, ein Bild, ein Text, eine Schaltfläche, ein Video, eine Kombination dieser Elemente auf einer Seite, eine gesamte Webseite oder mehrere Seiten, die einen Kauftrichter oder eine andere logische Seitenfolge bilden können. Ein Erlebnis kann auch die Antwort eines Sprachassistenten, ein Skript für den Kundendienst oder sogar ein personalisierter Geschmack in einem Getränkeautomaten sein. Sie können Erlebnisse in [!DNL Target] Aktivitäten testen oder personalisieren. [Mehr Info](/help/c-experiences/experiences.md). |
| Angebote | Ein Inhaltsblock, der Bilder, Text, HTML, Links, Videos, eine Aktionsaufrufschaltfläche, die Antwort eines Sprachassistenten oder einen anderen Inhaltstyp enthalten kann. Ein Angebot kann für einen Rabatt, einen kostenlosen Versand oder ähnliches verwendet werden. Ein Angebot kann auf einer Webseite angezeigt werden, aber auch auf jedem anderen Kunden-Touchpoint gerendert werden, zum Beispiel in einem Sprachassistenten oder auf einer Spielkonsole. Beim Test eines Angebots messen Sie seinen Erfolg im Vergleich zu anderen Angeboten bzw. zu einem Inhalt ohne dieses Angebot. [Mehr Info](/help/c-experiences/c-manage-content/manage-content.md). |
| Zielgruppen | Eine Gruppe von Personen mit denselben Merkmalen, wie beispielsweise „neue Besucher“, „wiederkehrende Besucher“ oder „wiederkehrende Besucher aus einem bestimmten Bundesland“. Mit der Zielgruppenfunktion können Sie Ihre Inhalte und Erlebnisse speziell an bestimmte Zielgruppen anpassen. Durch geeignete Botschaften zum richtigen Zeitpunkt für die richtigen Personen können Sie so Ihr digitales Marketing optimieren. Wird ein Besucher als Teil einer Zielgruppe identifiziert, bestimmt [!DNL Target] basierend auf den Kriterien, die bei der Erstellung der Aktivität festgelegt wurden, welches Erlebnis ihm angezeigt wird. [Mehr Info](/help/c-target/target.md). |
| Erfolgsmetriken | Die wichtigsten geschäftlichen Messwerte, mit denen Sie den Erfolg eines bestimmten Erlebnisses oder Angebots in einer [!DNL Target]-Aktivität ermitteln. So können Sie beispielsweise feststellen, ob ein neues Angebot oder das Hinzufügen eines Artikels zu einem Warenkorb Ihren Umsatz pro Besucher steigert. Erfolgsmetriken können hilfreich sein, um Probleme mit der Registrierung, der Sortierung oder dem Kauftrichter oder einfach mit der Besucher- und Kundeninteraktion zu ermitteln. [Mehr Info](/help/c-activities/r-success-metrics/success-metrics.md). |
| Berichte | Informationen über den Fortschritt und die Ergebnisse Ihrer Aktivitäten, die Ihnen bei der datengestützten Entscheidungsfindung helfen. Berichtsdaten können Ihnen bei der Entscheidung helfen, wann ein Test beendet werden soll, zeigen Ihnen, welches Erlebnis oder Angebot der Gewinner ist, und bieten Einblicke oder Erkenntnisse, um die nächsten Aktionen zu bestimmen. [Mehr Info](/help/c-reports/reports.md). |

## Tools zum Erstellen von Aktivitäten

[!DNL Target] stellt drei wichtige Tools zur Einrichtung Ihrer Test- und Personalisierungsaktivitäten bereit: [!UICONTROL Visual Experience Composer] (VEC), den [!UICONTROL formularbasierten Experience Composer] und den [!UICONTROL Visual Experience Composer für Einzelseiten-Apps (SPA)]. Alle führen Sie in drei Schritten durch den Einrichtungsprozess der Aktivität: Definieren der Erlebnisse, Auswählen oder Definieren der Zielgruppen und Auswählen der primären und der sekundären Erfolgsmetrik, mit denen Sie die Ergebnisse Ihrer Aktivität messen.

| Tool | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Eine WYSIWYG-Benutzeroberfläche, mit der Sie personalisierte Erlebnisse und Angebote im Kontext der Website ganz einfach erstellen und testen können. Sie können Erlebnisse und Angebote für [!DNL Target]-Aktivitäten erstellen, indem Sie das Layout und den Inhalt einer Webseite (oder eines Angebots) bzw. einer mobilen Webseite per Drag &amp; Drop austauschen und verändern. [Mehr Info](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md). |
| [!UICONTROL Formularbasierter Experience Composer] | Eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten. Diese Erlebnisse können in A/B-Tests sowie in Erlebnis-Targeting-, Automated Personalization- und Recommendations-Aktivitäten genutzt werden, wenn der Visual Experience Composer nicht verfügbar oder unpraktisch in der Anwendung ist. So können Sie den formularbasierten Composer beispielsweise verwenden, um Erlebnisse und Angebote für E-Mails, Kiosks und Sprachassistenten zu erstellen. [Mehr Info](/help/c-experiences/form-experience-composer.md). |
| [!UICONTROL Visual Experience Composer für Einzelseiten-Apps (SPA)] | VEC für SPAs ermöglicht es Marketing-Experten, für SPAs selbst Tests zu erstellen und Inhalt zu personalisieren, ohne von der kontinuierlichen Weiterentwicklung abhängig zu sein. Mit VEC können Sie A/B-Test- und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) in beliebten Frameworks wie React und Angular erstellen. [Mehr Info](/help/c-experiences/spa-visual-experience-composer.md). |

## Governance und Kontrolle

Für die Zuweisung der richtigen Benutzerrollen, Zugriffsebenen und Berechtigungen für [!DNL Target] verwenden Sie die Verwaltungskonsole. [!UICONTROL Target Premium]-Benutzer erhalten durch [!UICONTROL Enterprise-Berechtigungen] granularere Governance- und Kontrollmöglichkeiten.

| Tool | Details |
| --- | --- |
| [!UICONTROL Adobe Admin Console for Enterprise] | Fügen Sie Adobe Target Benutzer hinzu und weisen Sie ihnen über die Adobe Admin Console Berechtigungen zu. [Mehr Info](/help/administrating-target/c-user-management/c-user-management/user-management.md). |
| [!UICONTROL Enterprise-Berechtigunge]n<br>(Premium) | Eine Möglichkeit zur Vergabe von unternehmensweiten Benutzerzugriffen auf [!DNL Target]. Sie können [!DNL Target] Benutzer hinzufügen, Berechtigungen auf Grundlage deren Rollen zuweisen und Workspaces für Teams basierend auf unterschiedlichen Abteilungen, globalen Standorten, Kanälen und anderen logischen Gruppierungen erstellen. Sie können Benutzern die Rollen „Beobachter“, „Bearbeiter“, „Publisher“ oder „Genehmiger“ zuweisen. [Mehr Info](/help/administrating-target/c-user-management/property-channel/property-channel.md). |

## Integrationen

[!DNL Target] kann mit vielen Systemen von Erst-, Zweit- und Drittanbietern integriert werden. Durch diese Integrationen erhalten Sie auch Zugriff auf die in diesen Systemen vorliegenden Besucher- und Kundendaten und können sie in Ihren Zielgruppen für Tests und Personalisierungen verwenden. Als Teil von [!DNL Adobe Experience Cloud]integriert sich [!DNL Target] eng in [!DNL Experience Cloud]-Lösungen und deren Core Services.

| Integration | Details |
| --- | --- |
| Adobe Experience Cloud | [!DNL Target] verfügt über Integrationen mit anderen [!DNL Adobe Experience Cloud]-Lösungen, durch die Erlebnisse in jedem Maßstab personalisiert werden können. Nutzen Sie die Leistungsstärke von [!DNL Target] zusammen mit [Adobe Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md), [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md), [Adobe Campaign](/help/c-integrating-target-with-mac/campaign-and-target.md), [Adobe Audience Manager](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) (AAM) und [Adobe Experience Manager](/help/c-experiences/c-manage-content/aem-experience-fragments.md) (AEM). |
| Target-APIs (Premium) | [!UICONTROL Target] bietet mehr als 40 APIs, die Sie zur Integration von Adobe Target in Erst-, Zweit- und Drittanbietersysteme verwenden können. [Mehr Info](/help/api/api-overview.md). |

## Bitte beachten Sie

Berücksichtigen Sie die folgenden Erfahrungswerte, bevor Sie zum nächsten Kapitel „Entwicklung Ihrer Test- und Personalisierungsideen“ übergehen.

### Best Practices für die Optimierung

* **Gute Strategie**: Wie lauten unser Ziel und unsere Hypothese? Sind sie aufeinander abgestimmt? Wir möchten zum Beispiel die Zahl der eingereichten Kreditanträge erhöhen. Dabei gehen wir davon aus, dass wir den Antragstellern die erste Hürde durch weniger Felder im Antragsformular nehmen.
* **Disziplinierte Methodik**: Beginnen wir mit unseren Tests an den richtigen Stellen? Sie benötigen beispielsweise Stellen mit ausreichend Traffic, der sich tatsächlich auf die ausschlaggebenden Geschäftsmetriken auswirkt.
* **Korrektes Setup**: Erreichen wir mit dem Setup unserer Aktivität unser Ziel? Versuchen wir beispielsweise die Zahl der eingereichten Kreditanträge zu erhöhen, sollten wir uns auf Menschen konzentrieren, die Interesse an einem Kredit haben, und wir sollten die Klicks auf die Schaltfläche „Senden“ messen.
* **Gründliche Analyse**: Wurde die Testaktivität vollständig abgeschlossen? Was sagen die Ergebnisse? Führen Sie Ihre Aktivität bis zu einer statistischen Genauigkeit von 95 % bis 99 % aus. Dokumentieren Sie, weshalb Sie das erfolgreichste Erlebnis überzeugt, und nutzen Sie Ihre Erkenntnisse auch für andere Optimierungen.
* **Iterative Tests**: Setzen wir auf den Erfahrungen aus früheren Aktivitäten auf? Wenn Sie eine erfolgreiche Taktik finden, versuchen Sie diese zu verbessern und Änderungen vorzunehmen, um Ihre Erfolgsmetriken weiter zu optimieren.

### Meinungen können die Ergebnisse negativ beeinflussen

* Meinungen, die Ergebnisse negativ beeinflussen können: Highest Paid Person’s Opinion (HIPPO), d. h. die Meinungen, Ansichten und Vorurteile der bestbezahlten Person Beispielsweise möchte der Geschäftsführer das Suchfeld verkleinern, um auf den Seiten mehr Platz zu schaffen. Das sollten wir testen, um sicherzustellen, dass die Nutzung der Suchfunktion dadurch nicht nachlässt.
* Handeln wir nach unserer oder der Meinung anderer? „Mir gefällt dieser Test nicht.“ „Dem Kunden wird dieses Ergebnis garantiert nicht gefallen.“ Obwohl Intuition oft hilfreich ist, haben A/B-Tests immer wieder bewiesen, dass Bauchgefühl auch irren kann.
* Oder haben Sie sich frei von Meinungen gemacht und denken allein an Optimierung? Ich bin gespannt, welches Erlebnis gewinnt. Haben wir genügend Optionen zum Testen?

### Auch Annahmen können die Ergebnisse negativ beeinflussen

* Annahmen, die Effizienz und Wirksamkeit beeinträchtigen: Herdenmentalität – so macht das die Konkurrenz. Beispiel: Alle unsere Wettbewerber verwenden Hero-Banner mit sich drehenden Bildern. Dann sollten wir das auch so machen.
* Die Annahme, dass wir wissen, warum etwas funktioniert oder auch nicht funktioniert. Die Annahme, dass wir gar nicht testen müssen. Beispiel: Wir präsentieren unsere Hotelzimmer schon immer vom höchsten bis zum niedrigsten Preis.
* Handeln wir nach Annahmen? Wir müssen das nicht testen. Schließlich haben wir die Analysen bereits überprüft. (Ja, aber Analysen sind nicht die ganze Wahrheit. Durch Tests könnten Sie mehr herausfinden.)
* Oder haben Sie sich frei von Meinungen gemacht und denken allein an Optimierung? Wir testen alles.
