---
keywords: Target Standard;at.js;Implementierung
description: Erfahren Sie, wie Sie zu at.js migrieren, der neuen Implementierungsbibliothek für Adobe [!DNL Target] die sowohl für typische Webimplementierungen als auch für Einzelseiten-Apps (SPA) entwickelt wurde.
title: Wie migriere ich von "mbox.js"zu "at.js"?
feature: at.js
role: Developer
exl-id: 1d95faeb-7caa-44d6-b637-a06db393e50e
source-git-commit: e0713ccd25da71c2655b567ff8715a22203f46fb
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 88%

---

# Migration von „mbox.js“ zu „at.js“

at.js ist die neue Implementierungsbibliothek für [!DNL Adobe Target] und ist sowohl auf typische Webimplementierungen als auch auf Einzelseitenanwendungen ausgelegt.

Neben anderen Vorteilen sorgt [!DNL at.js] für kürzere Ladezeiten von Seiten bei Webimplementierungen und bietet bessere Implementierungsoptionen für Einzelseiten-Apps.

[!DNL at.js] ersetzt [!DNL mbox.js] bei [!DNL Target]-Implementierungen. [!DNL at.js] enthält darüber hinaus die Komponenten, die sich in [!DNL target.js] befanden, weshalb kein Aufruf mehr an [!DNL target.js] erfolgt.

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 mit FP-11577 (oder neuer) unterstützt at.js-Implementierungen mit der Adobe Target Cloud-Integration. Weitere Informationen finden Sie unter [Feature Packs](https://experienceleague.adobe.com/docs/) und [Integrieren mit Adobe Target](https://experienceleague.adobe.com/docs/) in der Dokumentation zu *Adobe Experience Manager 6.2*.

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

## Schulungsvideo: Vorteile von at.js und Best Practices bei der Implementierung  ![Übersichtszeichen](/help/assets/overview.png)

Dieses Video ist eine Aufzeichnung von „[Office Hours](/help/cmp-resources-and-contact-information.md)“, einer Initiative der Adobe-Kundenunterstützung.

* So funktioniert die at.js-Bibliothek
* Vorteile von at.js gegenüber mbox.js
* Verwaltung von Flackern mit „at.js“
* Fehlerbehandlung in at.js
* Debugging-Methoden
* Bekannte Probleme und Roadmap

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
