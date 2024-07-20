---
keywords: Multivarianz-Tests; Fehlerbehebung; Fehlerbehebung; MVT
description: Erfahren Sie mehr über potenzielle Herausforderungen bei der Verwendung von [!UICONTROL Multivariate Test] (MVT)-Aktivitäten in  [!DNL Adobe Target] sowie über empfohlene Lösungen.
title: Wie kann ich eine Fehlerbehebung für einen [!UICONTROL Multivariate Test] durchführen?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 22%

---

# Fehlerbehebung bei [!UICONTROL Multivariate Test] -Aktivitäten

Dieser Artikel enthält Vorschläge zum Beheben einiger Probleme, die beim Entwerfen eines [!UICONTROL Multivariate Test] (MVT) in [!DNL Adobe Target] auftreten können.

* Wenn Sie bei der Bearbeitung einer Aktivität [!DNL Analytics]-basierte Metriken verwendet haben und die Report Suite nicht geladen wird (das Netz wird angezeigt), wechseln Sie die Metriken zu [!DNL Target] -Metriken und dann erneut zu [!DNL Analytics] -basierter Metrik. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem bereits ausgeführten Test vornehmen, können Sie den Test und seine Daten zurücksetzen.

  Mit [!DNL Target] können Sie eine Live-Aktivität bearbeiten. Wenn Sie eine laufende Aktivität bearbeiten, kann der Test zurückgesetzt werden, sodass Berichte einige der Änderungen möglicherweise nicht erkennen.

  Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

  Zu den spezifischen Aktionen, die Erlebnisnamen und Berichte zurücksetzen, gehören:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.
