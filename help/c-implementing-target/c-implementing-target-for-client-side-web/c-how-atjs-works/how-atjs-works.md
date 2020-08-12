---
keywords: system diagram;flicker;at.js;implementation;javascript library;js;atjs
description: Adobe Target-Systemdiagramm zur Darstellung des Anruf- und Informationsflusses bei Aufrufen oder Datensammlungen einer automatisch erstellten globalen Mbox bei der Verwendung von „at.js“.
title: So funktioniert die Adobe Target JavaScript-Bibliothek "at.js"
feature: null
topic: Standard
uuid: 8ed04881-3dd9-496f-9c9c-feb9c740ed80
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 88%

---


# Funktionsweise von „at.js“{#how-at-js-works}

To implement [!DNL Adobe Target] client-side, you must use the at.js JavaScript library.

Bei Client-seitigen Implementierungen von [!DNL Adobe Target] stellt [!DNL Target] die mit einer Aktivität verknüpften Erlebnisse direkt dem Client-Browser bereit. Der Browser entscheidet, welches Erlebnis angezeigt werden soll, und zeigt es an. Bei einer Client-seitigen Implementierung können Sie einen WYSIWYG-Editor, Visual [Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder eine nicht visuelle Schnittstelle, den [formularbasierten Experience Composer](/help/c-experiences/form-experience-composer.md), verwenden, um Ihre Tests und Personalisierungserlebnisse zu erstellen.

## Was ist at.js?

Die [at.js-Bibliothek](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) ist die neue Implementierungsbibliothek für Target. Die „at.js“-Bibliothek sorgt für kürzere Seitenladezeiten bei Webimplementierungen und bietet bessere Implementierungsoptionen für Single-Page-Anwendungen. „at.js“ ist die empfohlene Implementierungsbibliothek und wird häufig mit neuen Funktionen aktualisiert. Wir empfehlen allen Kunden, die  [neueste Version von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) zu implementieren oder zu ihr zu migrieren.

Weitere Informationen finden Sie unter [JavaScript-Bibliotheken in Target](/help/c-intro/how-target-works.md#libraries).

In the [!DNL Target] implementation illustrated below, the following [!DNL Adobe Experience Cloud] solutions are implemented: Analytics, Target, and Audience Manager. Zudem wurden zentrale Experience Cloud-Services implementiert: Adobe Launch, Zielgruppen und Besucher-ID-Service.

## Was ist der Unterschied zwischen &quot;at.js 1&quot;?*x*- und at.js 2.x-Workflow-Diagrammen?

Weitere Informationen zu den Unterschieden, die in 2.x im Vergleich zu 1.x eingeführt wurden, finden Sie unter [Aktualisieren von at.js 1.x auf at.js 2](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md).*x*.

Grob betrachtet gibt es einige Unterschiede zwischen den beiden Versionen:

* at.js 2.x hat kein globales Mbox-Anfragekonzept, sondern stellt Anfragen beim Laden der Seite. Eine Anfrage beim Laden der Seite kann als Anfrage zum Abrufen von Inhalten verstanden werden, die beim ersten Laden Ihrer Website angewendet werden soll.
* at.js 2.x manages  a concepts called Views, which are use for Single Page Applications (SPAs). at.js 1.*x* kennt dieses Konzept nicht.

## Diagramme in at.js 2.x

Die folgenden Diagramme helfen Ihnen dabei, den Arbeitsablauf von at.js 2.x mit Ansichten zu verstehen und wie dieser die Integration der SPAs verbessert. Eine bessere Einführung in die in at.js 2.x verwendeten Konzepte finden Sie unter [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Ablauf mit at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Schritt | Details |
| --- | --- |
| 1 | Ein Aufruf gibt die [!DNL Experience Cloud ID] zurück, falls sich der Benutzer authentifiziert hat. Bei einem weiteren Aufruf wird die Kunden-ID synchronisiert. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>at.js kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert wird. |
| 3 | Es wird eine Seitenlade-Anfrage durchgeführt, in der alle konfigurierten Parameter (MCID, SDID und Kunden-ID) enthalten sind. |
| 4 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist. Der Speicher ruft geeignete Zielgruppen aus der Zielgruppenbibliothek ab (beispielsweise über Adobe Analytics, Zielgruppen-Management etc. bereitgestellte Zielgruppen).<br>Kundenattribute werden in einem Batch-Prozess an den Profilspeicher übermittelt. |
| 5 | Basierend auf den URL-Anfrageparametern und den Profildaten entscheidet [!DNL Target], welche Aktivitäten und Erlebnisse für die aktuelle Seite und zukünftige Ansichten an den Besucher zurückgegeben werden sollen. |
| 6 | Zielgerichteter Inhalt wird zurück an die Seite übermittelt. Dieser enthält optional Profilwerte für eine weitere Personalisierung.<br>Die zielgerichteten Inhalte auf der aktuellen Seite werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern.<br>Gezielte Inhalte für Ansichten, die aufgrund von Benutzeraktionen in einer SPA angezeigt werden, werden im Browser zwischengespeichert, sodass sie sofort ohne zusätzlichen Serveraufruf angewendet werden können, wenn die Ansichten durch ausgelöst werden `triggerView()`. |
| 7 | Analytics-Daten werden an Datenerfassungsserver übermittelt. |
| 8 | Zielgerichtete Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt.<br>Analytics-Daten können dann sowohl in Analytics als auch in Target eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs Analytics for Target (A4T). |

Egal, wo `triggerView()` in Ihrer SPA implementiert ist, werden die Ansichten und Aktionen aus dem Cache abgerufen und dem Benutzer ohne Serveraufruf gezeigt. `triggerView()` sendet außerdem eine Benachrichtigungsanfrage an das [!DNL Target]-Backend, um Impressions-Zählungen zu erhöhen und aufzuzeichnen. Weitere Informationen zu at.js für SPAs mit Ansichten finden Sie unter [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Ablauf at.js 2 x triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Schritt | Details |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 3 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den [!DNL Target]-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

### Video - Architekturdiagramm von at.js 2.x

at.js 2.x verbessert die Unterstützung von Adobe Target für SPAs und kann mit anderen Experience Cloud-Lösungen integriert werden. In diesem Video wird erklärt, wie alles zusammenkommt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Weitere Informationen finden Sie unter [Die Funktionsweise](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) von at.js 2.x.

## at.js 1.x-Diagramm

![Target-Ablauf at.js 1 x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/target-flow.png)

| Schritt | Beschreibung | Aufruf | Beschreibung |
|--- |--- |--- |--- |
| 1 | Ein Aufruf gibt die [!DNL Experience Cloud ID] (MCID) zurück, falls sich der Benutzer authentifiziert hat. Bei einem weiteren Aufruf wird die Kunden-ID synchronisiert. | 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen. |
| 3 | Es wird ein globaler Mbox-Aufruf durchgeführt, in dem alle konfigurierten Parameter, MCID, SDID und Kunden-IDs enthalten sind (optional). | 4 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist. Der Speicher ruft geeignete Zielgruppen aus der [!UICONTROL Zielgruppenbibliothek] ab (z. B. über [!DNL Adobe Analytics], [!DNL Audience Manager] usw. bereitgestellte Zielgruppen).<br>Kundenattribute werden in einem Batch-Prozess an [!DNL Profile Store] übermittelt. |
| 5 | Basierend auf URL, Mbox-Parametern und Profildaten wird von [!DNL Target] entschieden, welche Aktivitäten und Erlebnisse dem Besucher angezeigt werden sollen. | 6 | Zielgerichteter Inhalt wird zurück an die Seite übermittelt. Dieser enthält optional Profilwerte für eine weitere Personalisierung.<br>Das Erlebnis wird so schnell wie möglich ohne ein Flackern der Standardinhalte bereitgestellt. |
| 7 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. | 8 | [!DNL Target]-Daten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und im [!DNL Analytics]-Berichtspeicher abgelegt.<br>[!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!DNL Analytics for Target] (A4T). |

### Video - Bürozeiten: &quot;at.js&quot;-Tipps und -Übersichten (26. Juni 2019)

Dieses Video ist eine Aufzeichnung von Office Hours, eine Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* Vorteile der Verwendung von &quot;at.js&quot;
* &quot;at.js&quot;-Einstellungen
* Handhabung von Flackern
* Debuggen von „at.js“
* Bekannte Probleme
* FAQs

>[!VIDEO](https://video.tv.adobe.com/v/27959)

## Darstellung von Angeboten mit HTML-Inhalten durch at.js {#render}

Bei der Darstellung von Angeboten mit HTML-Inhalten wendet at.js den folgenden Algorithmus an:

1. Bilder werden vorab geladen (wenn `<img>`-Tags in HTML-Inhalten vorhanden sind).

1. HTML-Inhalte sind mit dem DOM-Knoten verbunden.

1. Inline-Skripte werden ausgeführt (Code, der in `<script>`-Tags eingeschlossen ist).

1. Remote-Skripte werden asynchron geladen und ausgeführt (`<script>`-Tags mit `src`-Attributen).

Wichtige Hinweise:

* at.js garantiert nicht die Reihenfolge der Ausführung von Remote-Skripten, da diese asynchron geladen werden.
* Inline-Skripte sollten nicht von Remote-Skripten abhängig sein, da diese später geladen und ausgeführt werden.