---
keywords: Multivariate Tests; Fehlerbehebung; Fehlerbehebung; MVT
description: Entdecken Sie die potenziellen Herausforderungen, vor denen Sie bei der Verwendung von [!UICONTROL Multivariate Test] (MVT)-Aktivitäten in  [!DNL Adobe Target] stehen könnten, zusammen mit Lösungsvorschlägen.
title: Wie kann ich eine [!UICONTROL Multivariate Test] beheben?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 22%

---

# Fehlerbehebung bei [!UICONTROL Multivariate Test] Aktivitäten

Dieser Artikel enthält Vorschläge zur Lösung einiger Probleme, die beim Entwerfen eines [!UICONTROL Multivariate Test] (MVT) in [!DNL Adobe Target] auftreten können.

* Wenn Sie bei der Bearbeitung einer Aktivität [!DNL Analytics] Metriken verwendet haben und die Report Suite nicht geladen wird (das Zahlenauswahlfeld wird angezeigt), wechseln Sie die Metriken zu [!DNL Target] Metriken und wechseln Sie dann erneut zu einer [!DNL Analytics] Metrik. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem bereits laufenden Test vornehmen, können Sie den Test und seine Daten zurücksetzen.

  [!DNL Target] können Sie eine Live-Aktivität bearbeiten. Beim Bearbeiten einer laufenden Aktivität kann der Test zurückgesetzt werden, sodass in Berichten möglicherweise einige der Änderungen nicht erkannt werden.

  Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

  Zu den spezifischen Aktionen zum Zurücksetzen von Erlebnisnamen und Berichten gehören:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.
