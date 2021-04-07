---
keywords: implementieren;Implementierung;Einrichten;Einrichten;Datenanbieter
description: Daten mithilfe von Datenanbietern in die Zielgruppe laden
title: Wie erhalte ich Daten mithilfe von Datenanbietern in die Zielgruppe?
feature: Implementierung
role: Developer
translation-type: tm+mt
source-git-commit: e8c25685341319fea4381386cad1ce0c5b80face
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 66%

---

# Datenanbieter

Datenanbieter sind eine Funktion, mit der Sie Daten von Dritten einfach an [!DNL Adobe Target] weitergeben können.

Hinweis: Datenanbieter benötigen at.js 1.3 oder höher.

## Format

Die Einstellung `window.targetGlobalSettings.dataProviders` entspricht einer Reihe von Datenanbietern.

Weitere Informationen zur Struktur für die einzelnen Datenanbieter finden Sie unter [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Verwendungsbeispiele

Erfassen Sie Daten von Drittanbietern, wie z. B. einem Wetterdienst, einem DMP oder sogar Ihrem eigenen Webservice. Anschließend können Sie diese Daten zur Erstellung von Zielgruppen und zielgerichtetem Inhalt und zur Aufwertung des Benutzerprofils verwenden.

## Vorteile der Methode

Mit dieser Einstellung können Kunden Daten von Drittdatenanbietern sammeln, beispielsweise Demandbase, BlueKai und benutzerspezifische Services, und die Daten an Target als Mbox-Parameter in der globalen Mbox-Anfrage weitergeben.

Sie unterstützt die Sammlung von Daten von mehreren Anbietern über asynchrone und synchrone Anfragen.

Mit diesem Ansatz ist es ein Leichtes, Flicker- oder Standardinhalte zu verwalten und gleichzeitig unabhängige Timeouts für die einzelnen Anbieter festzulegen, um die Auswirkungen auf die Seitenleistung zu begrenzen

## Einschränkungen

Wenn die zu `window.targetGlobalSettings.dataProviders` hinzugefügten Datenanbieter asynchron sind, werden sie parallel ausgeführt. Die Besucher-API-Anforderung wird parallel zu den Funktionen ausgeführt, die zu `window.targetGlobalSettings.dataProviders` hinzugefügt wurden, um eine minimale Wartezeit zu ermöglichen.

at.js versucht nicht, die Daten im Cache zu speichern. Wenn der Datenanbieter die Daten nur einmal abruft, sollte er sicherstellen, dass die Daten zwischengespeichert werden, und die Cachedaten für den zweiten Aufruf verarbeiten, wenn die Anbieterfunktion aufgerufen wird.

## Codebeispiele

Unter [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) finden Sie verschiedene Beispiele.

## Links zu relevanten Informationen

Dokumentation: [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

## Schulungsvideos:

* [Verwenden von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Implementieren von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-technical-video-implement.html)