---
keywords: Multivariate Tests; Fehlerbehebung; Fehlerbehebung; MVT
description: Entdecken Sie die potenziellen Herausforderungen, vor denen Sie bei der Verwendung von [!UICONTROL Multivariate Test] (MVT)-Aktivitäten in  [!DNL Adobe Target] stehen könnten, zusammen mit Lösungsvorschlägen.
title: Wie kann ich eine [!UICONTROL Multivariate Test] beheben?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
TQID: https://experienceleague.adobe.com/O9lmC1PmICPCOxcMDYVcSdpRoM-bqwKR-79deFIG2mg
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 166
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
