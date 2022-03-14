---
keywords: Multivarianz-Tests; Fehlerbehebung; Fehlerbehebung; MVT
description: Erfahren Sie mehr über potenzielle Herausforderungen, die sich bei der Verwendung von Multivarianz-Test-Aktivitäten (MVT) in Adobe Target stellen können, sowie über Lösungsvorschläge.
title: Wie kann ich Probleme mit Multivarianz-Tests beheben?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 42%

---

# Fehlerbehebung bei Multivarianz-Tests

Dieses Thema enthält Vorschläge zur Lösung einiger Probleme, die beim Entwerfen eines [!UICONTROL Multivarianz] (MVT) Test in [!DNL Adobe Target].

* Wenn Sie beim Bearbeiten einer Aktivität [!DNL Analytics]-basierte Metriken nicht laden und die Report Suite nicht geladen wird (das Netz wird angezeigt), wechseln Sie zu [!DNL Target] Metriken und wechseln Sie dann erneut zu [!DNL Analytics]-basierte Metrik. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem bereits ausgeführten Test vornehmen, können Sie den Test und seine Daten zurücksetzen.

   [!DNL Target] ermöglicht die Bearbeitung einer Live-Aktivität. Achten Sie darauf, dass das Bearbeiten einer ausgeführten Aktivität zu einem Zurücksetzen des Tests führen kann, sodass Berichte einige der Änderungen möglicherweise nicht erkennen.

   Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

   Die spezifischen Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen, sind:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.
