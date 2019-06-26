---
description: Möchten Sie Target Standard oder Target Premium verwenden, fügen Sie eine Codezeile hinzu, mit der „mbox.js“ aufgerufen wird.
keywords: Implementierung;Mbox;mbox.js herunterladen;API herunterladen;mbox.js-API
seo-description: Möchten Sie Target Standard oder Target Premium verwenden, fügen Sie eine Codezeile hinzu, mit der „mbox.js“ aufgerufen wird.
seo-title: „mbox.js“-Implementierung
solution: Target
subtopic: Erste Schritte
title: „mbox.js“-Implementierung
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# „mbox.js“-Implementierung{#mbox-js-implementation}

Möchten Sie Target Standard oder Target Premium verwenden, fügen Sie eine Codezeile hinzu, mit der „mbox.js“ aufgerufen wird.

Sie können eine der beiden Referenzbibliotheken verwenden: [!DNL mbox.js] oder [!DNL at.js]. [Die Vorteile von at. js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) erklären die Unterschiede zwischen den beiden Bibliotheken.

>[!NOTE]
>
>Die „mbox.js“-Bibliothek wird weiterhin unterstützt, aber es gibt keine weiteren Funktionsupdates. Alle Kunden sollten auf at.js migrieren. Weitere Informationen finden Sie unter [Migration von „mbox.js“ zu „at.js“](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

Die einzelne Referenz zu [!DNL mbox.js] auf jeder Seite stellt die Bibliotheken bereit, die für alle Ihre Aktivitäten erforderlich sind. [!DNL mbox.js] sendet auf jeder Seite einen Aufruf an [!DNL Target], auf der die Datei [!DNL mbox.js] referenziert ist. Dies ermöglicht es [!DNL Target], Folgendes zu tun:

* Target-Aktivitäten bereitstellen,
* Klicks verfolgen,
* die meisten Erfolgsmetriken verfolgen.

>[!TIP]
>
>Zur Vereinfachung der Implementierung können Sie [!DNL mbox.js] in Ihrer globalen Kopfzeile referenzieren.

Daher müssen Sie keine unterschiedlichen Dateiversionen für einzelne Aktivitäten verwalten.

1. Referenzieren Sie [!DNL mbox.js] im Abschnitt `<head>` auf jeder Seite Ihrer Website.

   `<script src="/ *`directory`*/ *`scripts`*/mbox.js"></script>`

   Dabei ist ` *`directory`*/ *`scripts`*` das Verzeichnis, in dem Sie die [!DNL mbox.js]-Datei nach dem Herunterladen gespeichert haben. 
Wenn Sie bereits Mboxes aus einer bestehenden Implementierung auf Ihrer Seite haben, können diese Mboxes weiterhin auf der neuen Oberfläche verwendet werden. Die aktualisierte [!DNL mbox.js]-Datei ist nach wie vor erforderlich, diese Mboxes können jedoch für Aktivitäten ausgewählt und mit dem [!UICONTROL Visual Experience Composer] bearbeitet werden.