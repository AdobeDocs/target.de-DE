---
keywords: Multivarianz-Tests; Fehlerbehebung; Fehlerbehebung; MVT
description: Potenzielle Herausforderungen bei der Verwendung von [!UICONTROL Multivarianz-Test] (MVT) Aktivitäten in [!DNL Adobe Target]zusammen mit empfohlenen Lösungen.
title: Wie kann ich eine Fehlerbehebung bei einem [!UICONTROL Multivarianz-Test]?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 21%

---

# Fehlerbehebung [!UICONTROL Multivarianz-Test] activities

Dieser Artikel enthält Vorschläge zur Lösung einiger Probleme, die beim Entwerfen einer [!UICONTROL Multivarianz-Test] (MVT) in [!DNL Adobe Target].

* Wenn Sie beim Bearbeiten einer Aktivität [!DNL Analytics]-basierte Metriken nicht laden und die Report Suite nicht geladen wird (das Netz wird angezeigt), ändern Sie die Metriken in [!DNL Target] Metriken und wechseln Sie dann erneut zu [!DNL Analytics]-basierte Metrik. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem bereits ausgeführten Test vornehmen, können Sie den Test und seine Daten zurücksetzen.

  [!DNL Target] ermöglicht die Bearbeitung einer Live-Aktivität. Wenn Sie eine laufende Aktivität bearbeiten, kann der Test zurückgesetzt werden, sodass Berichte einige der Änderungen möglicherweise nicht erkennen.

  Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

  Zu den spezifischen Aktionen, die Erlebnisnamen und Berichte zurücksetzen, gehören:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.
