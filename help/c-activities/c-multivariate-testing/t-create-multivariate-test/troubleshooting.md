---
keywords: Multivarianz-Tests;Fehlerbehebung;Fehlerbehebung;MVT
description: Entdecken Sie potenzielle Herausforderungen, mit denen Sie möglicherweise konfrontiert sind, wenn Sie Multivarianz-Test-(MVT-)Aktivitäten in Adobe Target verwenden, und schlagen Sie Lösungsvorschläge vor.
title: Wie behebe ich Fehler bei Multivarianz-Tests?
feature: Multivariate Tests
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 42%

---


# Fehlerbehebung bei Multivarianz-Tests

Dieses Thema enthält Vorschläge zur Behebung einiger Probleme, die beim Entwerfen eines [!UICONTROL Multivarianz] (MVT)-Tests in [!DNL Adobe Target] auftreten können.

* Wenn Sie beim Bearbeiten einer Aktivität [!DNL Analytics]-basierte Metriken verwendet haben und die Report Suite nicht geladen wird (Kreisel wird angezeigt), wechseln Sie zu [!DNL Target]-Metriken und wechseln Sie dann erneut zu [!DNL Analytics]-basierter Metrik. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem bereits ausgeführten Test vornehmen, können Sie den Test und seine Daten zurücksetzen.

   [!DNL Target] können Sie eine Live-Aktivität bearbeiten. Achten Sie darauf, dass das Bearbeiten einer ausgeführten Aktivität zu einem Zurücksetzen des Tests führen kann, sodass Berichte einige der Änderungen möglicherweise nicht erkennen.

   Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

   Die spezifischen Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen, sind:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.

