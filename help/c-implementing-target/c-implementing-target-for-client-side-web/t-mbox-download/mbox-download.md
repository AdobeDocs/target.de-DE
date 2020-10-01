---
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
description: Möchten Sie Target Standard oder Target Premium verwenden, fügen Sie eine Codezeile hinzu, mit der „mbox.js“ aufgerufen wird.
title: „mbox.js“-Implementierung
feature: null
subtopic: Getting Started
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: 1397891d4451d9e66a25e018e6bd7078e70cfd3f
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 55%

---


# „mbox.js“-Implementierung{#mbox-js-implementation}

Möchten Sie Target Standard oder Target Premium verwenden, fügen Sie eine Codezeile hinzu, mit der „mbox.js“ aufgerufen wird.

Sie können eine der beiden Referenzbibliotheken verwenden: [!DNL mbox.js] oder [!DNL at.js]. [Die Vorteile von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) werden die Unterschiede zwischen den beiden Bibliotheken erklärt.

>[!NOTE]
>
>**Entfernen** von mbox.js: Am 18. Januar 2021 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 18. Januar 2021 schlagen alle von &quot;mbox.js&quot;ausgeführten Aufrufe korrekt fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
>
>Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
>
>Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.

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