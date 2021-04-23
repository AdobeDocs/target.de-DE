---
keywords: implementieren;Implementierung;Einrichten;Setup;Kundenattribute
description: 'Daten können mit Kundenattributen abgerufen werden. [!DNL Target] '
title: 'Wie erhalte ich Daten mithilfe von Kundenattributen? [!DNL Target] '
feature: Implementierung
role: Developer
exl-id: b6c4a286-7994-492d-bde9-346af7aa314f
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 51%

---

# Kundenattribute

Mit Kundenattributen können Sie Besucher-Profil-Daten via FTP in das [!DNL Adobe Experience Cloud] hochladen. Verwenden Sie nach dem Hochladen die Daten in [!DNL Adobe Analytics] und [!DNL Adobe Target].

Target Standard-Kunden können fünf Attribute anwenden, Zielgruppe Premium-Kunden können 200 Attribute anwenden.

## Format

Eine CSV-Datei mit Experience Cloud IDs (ECIDs) und Attributname-Wert-Paaren wird per FTP oder manuell in die Experience Cloud-UI hochgeladen.

## Verwendungsbeispiele

Ihr CRM-System oder ein anderes internes System speichert wertvolle Informationen, die Sie mit der Experience Cloud von Adobe teilen möchten, einschließlich Target und Analytics.

## Vorteile der Methode

Das Hochladen von Kundendaten erzeugt in Target einen Profileintrag für diesen Besucher, auch wenn Target den Besucher noch nicht gesehen hat.

Dieselben Daten stehen automatisch in Target und Analytics zur Verfügung.

FTP kann eine einfachere Implementierungsmethode als API sein.

## Einschränkungen

Target Standard-Kunden können fünf Attribute anwenden, Zielgruppe Premium-Kunden können 200 Attribute anwenden

Kann nur Werte über Kundenattribute aktualisieren, nicht auf der Seite.

Erfordert die Implementierung von Experience Cloud ID (ECID).

## Codebeispiele

Details finden Sie unter [Erstellen Sie eine Kundenattributquelle und laden Sie die Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) hoch.

### Links zu relevanten Informationen

[Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
