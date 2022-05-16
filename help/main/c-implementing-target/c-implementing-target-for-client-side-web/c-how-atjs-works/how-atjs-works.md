---
keywords: Systemdiagramm;Flimmern;at.js;Implementierung;JavaScript-Bibliothek;js;at.js
description: Erfahren Sie, wie die  [!DNL Target] -JavaScript-Bibliothek (at.js), einschließlich Systemdiagrammen, funktioniert. Dies hilft Ihnen auch, den Workflow zum Laden von Seiten besser zu verstehen.
title: Wie funktioniert die JavaScript-Bibliothek at.js?
feature: at.js
role: Developer
exl-id: 2193c02a-2a85-4ae1-bfbd-40fa7b87f0a0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: ht
source-wordcount: '1106'
ht-degree: 100%

---

# Funktionsweise von „at.js“

Zur Client-seitigen Implementierung von [!DNL Adobe Target] müssen Sie die JavaScript-Bibliothek „at.js“ verwenden.

Bei Client-seitigen Implementierungen von [!DNL Adobe Target] stellt [!DNL Target] die mit einer Aktivität verknüpften Erlebnisse direkt dem Client-Browser bereit. Der Browser entscheidet, welches Erlebnis angezeigt werden soll, und zeigt es an. Bei einer Client-seitigen Implementierung können Sie einen WYSIWYG-Editor, Visual [Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder eine nicht visuelle Schnittstelle, den [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md), verwenden, um Ihre Tests und Personalisierungserlebnisse zu erstellen.

## Was ist at.js?

Die at.js-Bibliothek ist die neue Implementierungsbibliothek für Target. Die at.js-Bibliothek sorgt für kürzere Seitenladezeiten bei Web-Implementierungen und bietet bessere Implementierungsoptionen für Single-Page-Anwendungen. „at.js“ ist die empfohlene Implementierungsbibliothek und wird häufig mit neuen Funktionen aktualisiert. Wir empfehlen allen Kunden, die   [neueste Version von „at.js“](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) zu implementieren oder zu ihr zu migrieren.

Weitere Informationen finden Sie unter [JavaScript-Bibliotheken in Target](/help/main/c-intro/how-target-works.md#libraries).

In der unten dargestellten [!DNL Target]-Implementierung sind folgende [!DNL Adobe Experience Cloud]-Lösungen enthalten: Analytics, Target und Audience Manager. Darüber hinaus werden die folgenden Experience Cloud Core Services implementiert: [!DNL Adobe Experience Platform], [!DNL Audiences] und [!DNL Visitor ID Service].

## Was ist der Unterschied zwischen at.js 1.*x*- und at.js 2.x-Workflow-Diagrammen?

Weitere Informationen zu den Unterschieden, die in 2.x im Vergleich zu 1.x eingeführt wurden, finden Sie unter [Aktualisieren von at.js 1.x auf at.js 2](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md).*x*.

Grob betrachtet gibt es einige Unterschiede zwischen den beiden Versionen:

* at.js 2.x hat kein globales Mbox-Anfragekonzept, sondern stellt Anfragen beim Laden der Seite. Eine Anfrage beim Laden der Seite kann als Anfrage zum Abrufen von Inhalten verstanden werden, die beim ersten Laden Ihrer Website angewendet werden soll.
* In at.js 2.x wird ein Ansichtenkonzept verwaltet, das für Einzelseiten-Apps (SPAs) verwendet wird. at.js 1.*x* kennt dieses Konzept nicht.

## Diagramme in at.js 2.x

Die folgenden Diagramme helfen Ihnen dabei, den Arbeitsablauf von at.js 2.x mit Ansichten zu verstehen und wie dieser die Integration der SPAs verbessert. Eine bessere Einführung in die in at.js 2.x verwendeten Konzepte finden Sie unter [Implementieren von Einzelseiten-Apps](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Ablauf mit at.js 2.x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Schritt | Details |
| --- | --- |
| 1 | Ein Aufruf gibt die [!DNL Experience Cloud ID] zurück, falls sich der Benutzer authentifiziert hat. Bei einem weiteren Aufruf wird die Kunden-ID synchronisiert. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>at.js kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert wird. |
| 3 | Es wird eine Seitenlade-Anfrage durchgeführt, in der alle konfigurierten Parameter (MCID, SDID und Kunden-ID) enthalten sind. |
| 4 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist. Der Speicher ruft geeignete Zielgruppen aus der Zielgruppenbibliothek ab (beispielsweise über Adobe Analytics, Zielgruppen-Management etc. bereitgestellte Zielgruppen).<br>Kundenattribute werden in einem Batch-Prozess an den Profilspeicher übermittelt. |
| 5 | Basierend auf den URL-Anfrageparametern und den Profildaten entscheidet [!DNL Target], welche Aktivitäten und Erlebnisse für die aktuelle Seite und zukünftige Ansichten an den Besucher zurückgegeben werden sollen. |
| 6 | Zielgerichteter Inhalt wird zurück an die Seite übermittelt. Dieser enthält optional Profilwerte für eine weitere Personalisierung.<br>Die zielgerichteten Inhalte auf der aktuellen Seite werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern.<br>Zielgerichtete Inhalte für Ansichten, die als Ergebnis von Benutzeraktionen in einer SPA angezeigt werden, werden im Browser zwischengespeichert, sodass die SPA sofort ohne zusätzlichen Server-Aufruf angezeigt werden kann, wenn die Ansichten durch `triggerView()` ausgelöst werden. |
| 7 | Analytics-Daten werden an Datenerfassungsserver übermittelt. |
| 8 | Zielgerichtete Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt.<br>Analytics-Daten können dann sowohl in Analytics als auch in Target eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs Analytics for Target (A4T). |

Egal, wo `triggerView()` in Ihrer SPA implementiert ist, werden die Ansichten und Aktionen aus dem Cache abgerufen und dem Benutzer ohne Serveraufruf gezeigt. `triggerView()` sendet außerdem eine Benachrichtigungsanfrage an das [!DNL Target]-Backend, um Impressions-Zählungen zu erhöhen und aufzuzeichnen. Weitere Informationen zu at.js für SPAs mit Ansichten finden Sie unter [Implementieren von Einzelseiten-Apps](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target-Ablauf at.js 2 x triggerView](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Schritt | Details |
| --- | --- |
| 1 | `triggerView()` wird in der Einzelseiten-App aufgerufen, um eine Ansicht wiederzugeben und Aktionen anzuwenden, die visuelle Elemente ändern. |
| 2 | Gezielte Inhalte für die Ansicht werden aus dem Cache gelesen. |
| 3 | Die zielgerichteten Inhalte werden so schnell wie möglich bereitgestellt, ohne dass Standardinhalte aufflackern. |
| 4 | Die Benachrichtigungsanfrage wird an den [!DNL Target]-Profilspeicher gesendet, damit der Besucher in der Aktivität erfasst und die Metrik erhöht wird. |
| 5 | Analysedaten werden an den Datenerfassungsserver gesendet. |
| 6 | Target-Daten werden über die SDID mit Analytics-Daten abgeglichen und im Analytics-Berichtspeicher abgelegt. Analysedaten können dann über A4T-Berichte sowohl in Analytics als auch in Target angezeigt werden. |

### Video: Architekturdiagramm von at.js 2.x

at.js 2.x verbessert die Unterstützung von Adobe Target für SPAs und kann mit anderen Experience Cloud-Lösungen integriert werden. In diesem Video wird erklärt, wie alles zusammenkommt.

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Weitere Informationen finden Sie unter [Funktionsweise von at.js 2.x](https://experienceleague.adobe.com/docs/target-learn/tutorials/implementation/understanding-how-atjs-20-works.html?lang=de).

## at.js 1.x-Diagramm

![Target-Ablauf at.js 1 x](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/target-flow.png)

| Schritt | Beschreibung | Aufruf | Beschreibung |
|--- |--- |--- |--- |
| 1 | Ein Aufruf gibt die [!DNL Experience Cloud ID] (MCID) zurück, falls sich der Benutzer authentifiziert hat. Bei einem weiteren Aufruf wird die Kunden-ID synchronisiert. | 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen. |
| 3 | Es wird ein globaler Mbox-Aufruf durchgeführt, in dem alle konfigurierten Parameter, MCID, SDID und Kunden-IDs enthalten sind (optional). | 4 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist. Der Speicher ruft geeignete Zielgruppen aus der [!UICONTROL Zielgruppenbibliothek] ab (z. B. über [!DNL Adobe Analytics], [!DNL Audience Manager] usw. bereitgestellte Zielgruppen).<br>Kundenattribute werden in einem Batch-Prozess an [!DNL Profile Store] übermittelt. |
| 5 | Basierend auf URL, Mbox-Parametern und Profildaten wird von [!DNL Target] entschieden, welche Aktivitäten und Erlebnisse dem Besucher angezeigt werden sollen. | 6 | Zielgerichteter Inhalt wird zurück an die Seite übermittelt. Dieser enthält optional Profilwerte für eine weitere Personalisierung.<br>Das Erlebnis wird so schnell wie möglich ohne ein Flackern der Standardinhalte bereitgestellt. |
| 7 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. | 8 | [!DNL Target]-Daten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und im [!DNL Analytics]-Berichtspeicher abgelegt.<br>[!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!DNL Analytics for Target] (A4T). |

### Video – Office Hours: Tipps und Übersicht zu at.js (26. Juni 2019)

Dieses Video ist eine Aufzeichnung von Office Hours, einer Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* Vorteile der Verwendung von at.js
* at.js-Einstellungen
* Einstellungen bei Flackern
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
