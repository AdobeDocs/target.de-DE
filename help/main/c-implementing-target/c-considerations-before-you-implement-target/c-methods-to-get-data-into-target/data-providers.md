---
keywords: implementieren;implementieren;einrichten;Einrichtung;Datenanbieter
description: Daten abrufen [!DNL Target] Verwendung von Datenanbietern.
title: Wie erhalte ich Daten? [!DNL Target] Verwenden von Datenanbietern?
feature: Implementation
role: Developer
exl-id: 05fe9190-4d36-43e2-9fc7-c354a6821bfb
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 67%

---

# Datenanbieter

Datenanbieter sind eine Funktion, mit der Sie Daten von Drittanbietern einfach an weitergeben können. [!DNL Adobe Target].

Hinweis: Datenanbieter benötigen at.js 1.3 oder höher.

## Format

Die Einstellung `window.targetGlobalSettings.dataProviders` entspricht einer Reihe von Datenanbietern.

Weitere Informationen zur Struktur für die einzelnen Datenanbieter finden Sie unter [Datenanbieter](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Anwendungsbeispiele

Erfassen Sie Daten von Drittanbietern, wie z. B. einem Wetterdienst, einem DMP oder sogar Ihrem eigenen Webservice. Anschließend können Sie diese Daten zur Erstellung von Zielgruppen und zielgerichtetem Inhalt und zur Aufwertung des Benutzerprofils verwenden.

## Vorteile der Methode

Mit dieser Einstellung können Kunden Daten von Drittdatenanbietern sammeln, beispielsweise Demandbase, BlueKai und benutzerspezifische Services, und die Daten an Target als Mbox-Parameter in der globalen Mbox-Anfrage weitergeben.

Sie unterstützt die Sammlung von Daten von mehreren Anbietern über asynchrone und synchrone Anfragen.

Mit diesem Ansatz ist es ein Leichtes, Flicker- oder Standardinhalte zu verwalten und gleichzeitig unabhängige Timeouts für die einzelnen Anbieter festzulegen, um die Auswirkungen auf die Seitenleistung zu begrenzen

## Einschränkungen

Wenn Datenanbieter zu `window.targetGlobalSettings.dataProviders` asynchron sind, werden sie parallel ausgeführt. Die Besucher-API-Anfrage wird parallel mit den Funktionen ausgeführt, die zu `window.targetGlobalSettings.dataProviders` um eine minimale Wartezeit zu ermöglichen.

at.js versucht nicht, die Daten zwischenzuspeichern. Wenn der Datenanbieter die Daten nur einmal abruft, sollte er sicherstellen, dass die Daten zwischengespeichert werden, und die Cachedaten für den zweiten Aufruf verarbeiten, wenn die Anbieterfunktion aufgerufen wird.

## Codebeispiele

Unter [Datenanbieter](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) finden Sie verschiedene Beispiele.

## Links zu relevanten Informationen

Dokumentation: [Datenanbieter](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

## Schulungsvideos:

* [Verwenden von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Implementieren von Datenanbietern in Adobe Target](https://helpx.adobe.com/de/target/kt/using/dataProviders-atjs-technical-video-implement.html)
