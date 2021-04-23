---
keywords: implementieren;Implementierung;einrichten;Einrichtung;Seitenparameter;Tomcat;URL-encoded;In-page-Profilattribut;Mbox-Parameter;In-page-Profilattribute;Skript-Profilattribut;Bulk-Profilupdate-API;API für einzelne Dateiaktualisierungen;Kundenattribute;Datenanbieter;Daten-Anbieter;Datenanbieter
description: Daten abrufen in [!DNL Target] (Seitenparameter, Profil-Attribute, Skript-Profil-Attribute, Datenanbieter, Single- und Bulk-Profil-Aktualisierungs-APIs, Kundenattribute).
title: Wie erhalte ich Daten in die Zielgruppe?
feature: Implementierung
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 62%

---

# Methodenübersicht

Informationen zu den verschiedenen Methoden, mit denen Sie Daten in [!DNL Adobe Target] abrufen können.

Zu den verfügbaren Methoden gehören:

| Methode | Details |
| --- | --- |
| [Seitenparameter](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br> (auch als &quot;mbox-Parameter&quot;bezeichnet) | Seitenparameter sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden.<br>Seitenparameter sind nützlich, um Seitendaten an eine Zielgruppe zu senden, die nicht zum zukünftigen Targeting mit dem Profil des Besuchers gespeichert werden muss. Diese Werte werden stattdessen verwendet, um die Seite oder die Aktion zu beschreiben, die der Benutzer auf der jeweiligen Seite ausgeführt hat. |
| [Seiteninterne Profil-Attribute](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br> (auch &quot;In-mbox-Profil-Attribute&quot;genannt) | Inpage-Profilattribute sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben werden und im Profil des Besuchers für die zukünftige Verwendung gespeichert werden.<br>Die Profilattribute auf der Seite erlauben es, benutzerspezifische Daten im Profil von Target zu speichern, um sie später für ein Targeting gezielt zu segmentieren. |
| [Skript-Profilattribute](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | Skript-Profilattribute sind Name-Wert-Paare, die in der Target-Anwendung definiert sind. Der Wert wird durch die Ausführung eines JavaScript-Snippets auf dem Target-Server über den Server-Aufruf ermittelt.<br>Benutzer schreiben kleine Code-Snippets, die pro Mbox-Aufruf ausgeführt werden, bevor ein Besucher für eine Zielgruppenmitgliedschaft und -aktivität ausgewertet wird. |
| [Datenanbieter](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | Mithilfe von Datenanbietern können Sie Daten von Dritten problemlos an die Zielgruppe weitergeben. |
| [Bulk-Profil-Update-API](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/bulk-profile-update-api.md) | Senden Sie über die API eine CSV-Datei an Target mit Aktualisierungen des Besucherprofils für viele Besucher. Jedes Besucherprofil kann mit mehreren In-Page-Profilattributen in einem Aufruf aktualisiert werden. |
| [Single-Profil-API](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/single-profile-update-api.md) | Fast identisch mit der Massen-Profil-Update-API, aber ein Besucher-Profil wird gleichzeitig aktualisiert, in einer Linie im API-Aufruf und nicht mit einer CSV-Datei. |
| [Kundenattribute](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/customer-attributes.md) | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verwenden Sie nach dem Hochladen die Daten in Adobe Analytics und Adobe Target. |












