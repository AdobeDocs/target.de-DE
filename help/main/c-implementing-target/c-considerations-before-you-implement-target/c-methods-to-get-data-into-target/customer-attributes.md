---
keywords: implementieren;implementieren;einrichten;Einrichtung;Kundenattribute
description: Daten abrufen [!DNL Target] Verwendung von Kundenattributen.
title: Wie erhalte ich Daten? [!DNL Target] Verwenden von Kundenattributen?
feature: Implementation
role: Developer
exl-id: b6c4a286-7994-492d-bde9-346af7aa314f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 51%

---

# Kundenattribute

Mit Kundenattributen können Sie Besucherprofildaten via FTP in die [!DNL Adobe Experience Cloud]. Verwenden Sie nach dem Hochladen die Daten in [!DNL Adobe Analytics] und [!DNL Adobe Target].

Target Standard-Kunden können fünf Attribute anwenden, Target Premium-Kunden 200 Attribute.

## Format

Eine CSV-Datei mit Experience Cloud IDs (ECIDs) und Attributname-Wert-Paaren wird per FTP oder manuell in die Experience Cloud-UI hochgeladen.

## Anwendungsbeispiele

Ihr CRM-System oder ein anderes internes System speichert wertvolle Informationen, die Sie mit der Experience Cloud von Adobe teilen möchten, einschließlich Target und Analytics.

## Vorteile der Methode

Das Hochladen von Kundendaten erzeugt in Target einen Profileintrag für diesen Besucher, auch wenn Target den Besucher noch nicht gesehen hat.

Dieselben Daten stehen automatisch in Target und Analytics zur Verfügung.

FTP kann eine einfachere Implementierungsmethode als API sein.

## Einschränkungen

Target Standard-Kunden können fünf Attribute anwenden, Target Premium-Kunden 200 Attribute.

Kann nur Werte über Kundenattribute aktualisieren, nicht auf der Seite.

Erfordert die Implementierung von Experience Cloud ID (ECID).

## Codebeispiele

Details finden Sie unter [Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).

### Links zu relevanten Informationen

[Erstellen einer Kundenattributquelle und Hochladen der Datendatei](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
