---
keywords: document.write;target;implement;implement target;dtm;dynamic tag management;at.js;mbox.js;target.js;mbox
description: Implementieren Sie Target, indem Sie die Verweise auf die Target-Bibliotheken („at.js“ oder „mbox.js“) in Ihre Webseiten integrieren.
title: Erläuterung der JavaScript-Bibliotheken in Target
feature: implementation general
topic: Target
uuid: c8a254c9-afc9-4a55-be01-788c11bef7cc
translation-type: tm+mt
source-git-commit: 05bf843e5016d33ba436f6f24f5a0d05045d5129
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 100%

---


# Erläuterung der [!DNL Target]-JavaScript-Bibliotheken{#understand-the-target-javascript-libraries}

Implementieren Sie [!DNL Target], indem Sie die Verweise auf die [!DNL Target]-Bibliotheken (at.js oder mbox.js) in Ihre Webseiten integrieren.

>[!NOTE]
>
>Die mbox.js-Bibliothek wird nicht mehr weiterentwickelt. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. Weitere Informationen finden Sie unter [Migration von „mbox.js“ zu „at.js“](../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

## Unterschiede zwischen den beiden Bibliotheken {#section_40117C78C2F84FECAC4F1BA40CC4F171}

In der folgenden Tabelle werden die Unterschiede der beiden Bibliotheken erläutert:

| Bibliotheksreferenz | Beschreibung |
|--- |--- |
| at.js | at.js ersetzt mbox.js für [!DNL Target]-Implementierungen.<br>Neben anderen Vorteilen sorgt at.js für kürzere Ladezeiten von Seiten bei Webimplementierungen, bessere Sicherheit, Vermeidung von document.write-Warnungen in Google Chrome und bessere Implementierungsoptionen für Einzelseiten-Apps.<br>Weitere Informationen finden Sie unter [„at.js“-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md). |
| mbox.js | Vor [!DNL Target] 16.3.1 (März 2016) benötigte [!DNL Target] einen Aufruf an mbox.js, um die globale Mbox zu erstellen, die erforderlich war, damit [!DNL Target] Aktivitäten bereitstellen sowie Klicks und die meisten Erfolgsmetriken verfolgen konnte. Diese Datei enthält alle für Ihre Aktivitäten erforderlichen Bibliotheken. Daher müssen Sie keine unterschiedlichen Dateiversionen für einzelne Aktivitäten verwalten.<br>Wenn bereits umgebrochene Mboxes von einer früheren [!DNL Target]-Implementierung auf Ihren Seiten vorhanden sind, können diese Mboxes auch auf der neuen Benutzeroberfläche verwendet werden. Die aktualisierte mbox.js-Datei ist nach wie vor erforderlich, diese Mboxes können jedoch für Aktivitäten ausgewählt und mit dem Visual Experience Composer bearbeitet werden.<br>[!DNL Target] Standard und Premium aktualisieren und ergänzen mbox.js mit einer Referenz zu einer Datei namens target.js. Die target.js-Datei wird von Adobe gehostet. Die Datei Target.js ermöglicht das Bearbeiten von Inhalten auf einer beliebigen Seite im Visual Experience Composer, auch dann, wenn die Seite keine vordefinierten Mboxes enthält. Auf jeder Seite Ihrer Website muss auf diese Datei verwiesen werden.<br>Weitere Informationen finden Sie unter [„mbox.js“-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md).<br>**Wichtig:** Die „mbox.js“-Bibliothek wird weiterhin unterstützt, aber es gibt keine weiteren Funktionsupdates. Alle Kunden sollten auf at.js migrieren. Weitere Informationen finden Sie unter [Migration zu at.js von mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md)<br> |

## Auswirkung von at.js und mbox.js auf die Seitenladezeit {#section_16630CD0FF0A498EB596A51381366A5A}

Viele Kunden und Berater möchten wissen, wie sich [!DNL at.js] und [!DNL mbox.js] auf die Seitenladezeit auswirken, insbesondere beim Vergleich neuer Besucher mit zurückkehrenden Besuchern. Leider ist es schwierig, zu messen, wie sich [!DNL at.js] oder [!DNL mbox.js] auf die Seitenladezeit auswirken und genaue Zahlen dazu zu nennen. Das liegt an den Implementationen der einzelnen Kunden.

Wenn die Besucher-API jedoch auf der Seite vorhanden ist, ermöglicht uns das ein besseres Verständnis darüber, wie sich [!DNL at.js] und [!DNL mbox.js] auf die Seitenladezeit auswirken.

>[!NOTE]
>
>Die Besucher-API und [!DNL at.js] oder [!DNL mbox.js] wirken sich nur dann auf die Seitenladezeit aus, wenn Sie die globale Mbox verwenden (das liegt an der Technik, mit der der Haupttext ausgeblendet wird). Regionale Mboxes sind von der Besucher-API-Integration nicht betroffen.

In den folgenden Abschnitten wird die Aktionssequenz für neue und zurückkehrende Besucher beschrieben:

### Neue Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. at.js/mbox.js ist geladen und analysiert und wird ausgeführt.
1. Wenn die automatische Erstellung der globalen Mbox aktiviert ist, wird die Target JavaScript-Bibliothek Folgendes tun:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die Target-Bibliothek versucht, Experience Cloud-Besucher-ID-Daten abzurufen.
   * Weil es sich um einen neuen Besucher handelt, versendet die Besucher-API eine domänenübergreifende Anfrage an demdex.net.
   * Nachdem die Experience Cloud-Besucher-ID-Daten abgerufen wurden, wird eine Anfrage an Target gesendet.

### Zurückkehrende Besucher

1. Die Besucher-API ist geladen und analysiert und wird ausgeführt.
1. at.js/mbox.js ist geladen und analysiert und wird ausgeführt.
1. Wenn die automatische Erstellung der globalen Mbox aktiviert ist, wird die Target JavaScript-Bibliothek Folgendes tun:

   * Sie wird das Besucher-Objekt instanziieren.
   * Die Target-Bibliothek versucht, Experience Cloud-Besucher-ID-Daten abzurufen.
   * Die Besucher-API ruft Cookie-Daten ab.
   * Nachdem die Experience Cloud-Besucher-ID-Daten abgerufen wurden, wird eine Anfrage an Target gesendet.

>[!NOTE]
>
>Wenn die Besucher-API vorhanden ist, muss Target bei neuen Besuchern mehrfach über die Verbindung gehen, um sicherzustellen, dass Target-Anfragen die Daten der Experience Cloud-Besucher-ID enthalten. Bei zurückkehrenden Besuchern geht Target nur über die Verbindung, um den personalisierten Inhalt in Target abzurufen.
