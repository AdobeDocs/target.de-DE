---
keywords: Mobile Web Experience Editor
description: Dieses Thema enthält Vorschläge zur Lösung einiger Probleme, die beim Entwerfen eines MVT-Tests in Adobe Target auftreten können.
title: Fehlerbehebung bei Multivarianz-Tests
feature: mvt
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 77%

---


# Fehlerbehebung bei Multivarianz-Tests{#troubleshoot-multivariate-tests}

Dieses Thema enthält Vorschläge zur Lösung einiger Probleme, die beim Entwerfen eines MVT-Tests in Adobe Target auftreten können.

* Wenn Sie Analytics-basierte Metriken verwenden und beim Bearbeiten einer Aktivität die Berichtssuite nicht geladen wird (Netz wird angezeigt), wechseln Sie zu Target-Metriken und anschließend wieder zurück zu Analytics-basierten Metriken. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem Bericht vornehmen, der bereits ausgeführt wird, kann das dazu führen, dass Sie den Test und dessen Daten zurücksetzen.

   Target ermöglicht Ihnen das Bearbeiten einer Live-Aktivität. Achten Sie darauf, dass das Bearbeiten einer ausgeführten Aktivität zu einem Zurücksetzen des Tests führen kann, sodass Berichte einige der Änderungen möglicherweise nicht erkennen.

   Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

   Die spezifischen Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen, sind:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.

