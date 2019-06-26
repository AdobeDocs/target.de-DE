---
description: Dieses Thema enthält Empfehlungen für die Lösung einiger Probleme, die möglicherweise beim Entwurf eines Multivarianz-Tests entstehen.
keywords: Mobile Web Experience-Editor
seo-description: Dieses Thema enthält Empfehlungen für die Lösung einiger Probleme, die möglicherweise beim Entwurf eines Multivarianz-Tests entstehen.
seo-title: Fehlerbehebung bei Multivarianz-Tests
solution: Target
subtopic: Mobile Viewports
title: Fehlerbehebung bei Multivarianz-Tests
topic: Standard
uuid: 4de03e03-cbbd-4e8f-a1b9-19ba8b2e6951
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Fehlerbehebung bei Multivarianz-Tests{#troubleshoot-multivariate-tests}

Dieses Thema enthält Empfehlungen für die Lösung einiger Probleme, die möglicherweise beim Entwurf eines Multivarianz-Tests entstehen.

* Wenn Sie Analytics-basierte Metriken verwenden und beim Bearbeiten einer Aktivität die Berichtssuite nicht geladen wird (Netz wird angezeigt), wechseln Sie zu Target-Metriken und anschließend wieder zurück zu Analytics-basierten Metriken. Die Berichtssuite sollte jetzt geladen werden.
* Wenn Sie Änderungen an einem Bericht vornehmen, der bereits ausgeführt wird, kann das dazu führen, dass Sie den Test und dessen Daten zurücksetzen.

   Target ermöglicht Ihnen das Bearbeiten einer Live-Aktivität. Achten Sie darauf, dass das Bearbeiten einer ausgeführten Aktivität zu einem Zurücksetzen des Tests führen kann, sodass Berichte einige der Änderungen möglicherweise nicht erkennen.

   Es ist sicher, kleinere Änderungen wie die Bearbeitung vorhandenen Texts bzw. vorhandener HTML-Angebote vorzunehmen.

   Die spezifischen Aktionen, die zu einem Zurücksetzen von Erlebnisnamen und Berichten führen, sind:

   * Hinzufügen eines neuen Orts.
   * Löschen eines Orts.
   * Hinzufügen neuer Angebote oder Löschen von Angeboten aus einem vorhandenen Ort.

