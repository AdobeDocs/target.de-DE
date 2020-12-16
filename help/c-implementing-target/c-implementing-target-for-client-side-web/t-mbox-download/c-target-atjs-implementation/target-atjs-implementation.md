---
keywords: Target Standard;at.js;implementation
description: „at.js“ ist die neue Implementierungsbibliothek für Adobe Target und ist sowohl auf typische Webimplementierungen als auch auf Einzelseiten-Apps ausgelegt.
title: Migration von „mbox.js“ zu „at.js“
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 96%

---


# Migration von „mbox.js“ zu „at.js“{#migrate-from-mbox-js-to-at-js}

at.js ist die neue Implementierungsbibliothek für [!DNL Adobe Target] und ist sowohl auf typische Webimplementierungen als auch auf Einzelseitenanwendungen ausgelegt.

Neben anderen Vorteilen sorgt [!DNL at.js] für kürzere Ladezeiten von Seiten bei Webimplementierungen und bietet bessere Implementierungsoptionen für Einzelseiten-Apps.

[!DNL at.js] ersetzt [!DNL mbox.js] bei [!DNL Target]-Implementierungen. [!DNL at.js] enthält darüber hinaus die Komponenten, die sich in [!DNL target.js] befanden, weshalb kein Aufruf mehr an [!DNL target.js] erfolgt.

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 mit FP-11577 (oder neuer) unterstützt at.js-Implementierungen mit der Adobe Target Cloud-Integration. Weitere Informationen finden Sie unter [Feature Packs](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) und [Integrieren mit Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in der Dokumentation zu *Adobe Experience Manager 6.2*.

## Vorteile von at.js {#benefits}

In der folgenden Tabelle werden die Unterschiede der beiden Bibliotheken erläutert:

| Bibliotheksreferenz | Beschreibung |
|--- |--- |
| at.js | at.js ersetzt mbox.js für [!DNL Target]-Implementierungen.<br>Neben anderen Vorteilen sorgt at.js für kürzere Ladezeiten von Seiten bei Webimplementierungen, bessere Sicherheit, Vermeidung von document.write-Warnungen in Google Chrome und bessere Implementierungsoptionen für Einzelseiten-Apps.<br>Weitere Informationen finden Sie unter [„at.js“-Implementierung](#implement). |
| mbox.js | Vor [!DNL Target] 16.3.1 (März 2016) benötigte [!DNL Target] einen Aufruf an mbox.js, um die globale Mbox zu erstellen, die erforderlich war, damit [!DNL Target] Aktivitäten bereitstellen sowie Klicks und die meisten Erfolgsmetriken verfolgen konnte. Diese Datei enthält alle für Ihre Aktivitäten erforderlichen Bibliotheken. Daher müssen Sie keine unterschiedlichen Dateiversionen für einzelne Aktivitäten verwalten.<br>Wenn bereits umgebrochene Mboxes von einer früheren [!DNL Target]-Implementierung auf Ihren Seiten vorhanden sind, können diese Mboxes auch auf der neuen Benutzeroberfläche verwendet werden. Die aktualisierte mbox.js-Datei ist nach wie vor erforderlich, diese Mboxes können jedoch für Aktivitäten ausgewählt und mit dem Visual Experience Composer bearbeitet werden.<br>[!DNL Target] Standard und Premium aktualisieren und ergänzen mbox.js mit einer Referenz zu einer Datei namens target.js. Die target.js-Datei wird von Adobe gehostet. Die Datei Target.js ermöglicht das Bearbeiten von Inhalten auf einer beliebigen Seite im Visual Experience Composer, auch dann, wenn die Seite keine vordefinierten Mboxes enthält. Auf jeder Seite Ihrer Website muss auf diese Datei verwiesen werden.<br>Weitere Informationen finden Sie unter [„mbox.js“-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md).<br>**Wichtig:** Die „mbox.js“-Bibliothek wird weiterhin unterstützt, aber es gibt keine weiteren Funktionsupdates. Alle Kunden sollten auf at.js migrieren. Weitere Informationen finden Sie unter [Migration zu at.js von mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md) |

## Implementieren von at.js {#implement}

Verwenden Sie [!DNL at.js], indem Sie die [!DNL mbox.js]-Referenz auf Seiten ersetzen, auf denen Sie die Bibliothek einsetzen möchten. [!DNL mbox.js] und [!DNL at.js] können nicht zusammen auf derselben Seite verwendet werden. Einzeln können Sie sie jedoch auf jeder Seite Ihrer Website nutzen.

Die [!DNL at.js]-Bibliothek funktioniert in bestehenden Implementierungen mit den Funktionen `mboxCreate()`, `mboxDefine()` und `mboxUpdate()` und unterstützt neue Funktionen, die auf auf Einzelseiten-Apps basierende Implementierungen ausgerichtet sind.

Sie können [!DNL at.js] überall einsetzen, wo Sie aktuell [!DNL mbox.js] verwenden.

[!DNL at.js] bietet im Vergleich zur [!DNL mbox.js]-Bibliothek viele Verbesserungen, wie zum Beispiel die folgenden:

* Vollständig asynchrone Kommunikation über Cross-Domain-AJAX

   >[!IMPORTANT]
   >
   >[!DNL at.js] kommuniziert mit den Servern von [!DNL Target] zwar asynchron, die [!DNL at.js]-Datei selbst muss jedoch synchron im `<head>`-Abschnitt Ihrer Seite geladen werden. Idealerweise sollte die Datei eine der ersten Skripts sein, die geladen werden. Nach dem Laden führt [!DNL at.js] asynchron Mbox-Aufrufe über `XMLHttpRequest` durch und blockiert das Rendern von Seiten nicht.

* Keine blockierenden Aufrufe mehr
* Ohne Verwendung von `document.write()`
* Keine sofortige Ausführung von JavaScript-Code in [!DNL Target]-Antworten
* Bessere Zeitüberschreitung und Fehlerverarbeitung

   * Anpassbare [Zeitüberschreitung](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) pro Aufruf
   * Kein erneutes Laden bei Zeitüberschreitungen

* Speziell für Einzelseiten-Apps/MVC-Rahmen entwickelte Funktionen

## Schulungsvideo: Vorteile von at.js und Best Practices bei der Implementierung  ![Übersichtskennzeichnung](/help/assets/overview.png)

Dieses Video ist eine Aufzeichnung von „[Office Hours](/help/cmp-resources-and-contact-information.md)“, einer Initiative der Adobe-Kundenunterstützung.

* So funktioniert die at.js-Bibliothek
* Vorteile von at.js gegenüber mbox.js
* Verwaltung von Flackern mit „at.js“
* Fehlerbehandlung in at.js
* Debugging-Methoden
* Bekannte Probleme und Roadmap

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
