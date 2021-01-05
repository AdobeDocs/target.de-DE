---
keywords: Multivariate Tests;troubleshoot;troubleshooting;mvt
description: Dieses Thema enthält Vorschläge zur Lösung einiger Probleme, die beim Entwerfen eines MVT-Tests in Adobe Target auftreten können.
title: Fehlerbehebung bei Multivarianz-Tests
feature: Multivariate Tests
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 45%

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

