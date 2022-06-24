---
keywords: implementieren;Implementierung;einrichten;Einrichtung;Seitenparameter;Tomcat;URL-encoded;In-page-Profilattribut;Mbox-Parameter;In-page-Profilattribute;Skript-Profilattribut;Bulk-Profilupdate-API;API für einzelne Dateiaktualisierungen;Kundenattribute;Datenanbieter;Daten-Anbieter;Datenanbieter
description: Daten abrufen [!DNL Target] (Seitenparameter, Profilattribute, Skript-Profilattribute, Datenanbieter, Single- und Bulk-Profil-Update-APIs, Kundenattribute).
title: Wie integriere ich Daten in Target?
feature: Implementation
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 50%

---

# Methodenübersicht

Informationen über die verschiedenen Methoden, mit denen Daten in [!DNL Adobe Target].

Zu den verfügbaren Methoden gehören:

| Methode | Details |
| --- | --- |
| [Seitenparameter](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/page-parameters/){target=_blank}<br>(Auch &quot;Mbox-Parameter&quot;genannt) | Seitenparameter sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben und nicht zur späteren Verwendung im Profil des Besuchers gespeichert werden.<br>Seitenparameter sind nützlich, um Seitendaten an Target zu senden, die nicht mit dem Profil des Besuchers gespeichert werden müssen, um sie für zukünftige Targeting-Anwendungen nutzen zu können. Diese Werte werden stattdessen verwendet, um die Seite oder die Aktion zu beschreiben, die der Benutzer auf der jeweiligen Seite ausgeführt hat. |
| [Profilattribute auf der Seite](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/in-page-profile-attributes/){target=_blank}<br>(Auch &quot;In-mbox-Profilattribute&quot;genannt) | Inpage-Profilattribute sind Name-Wert-Paare, die direkt über den Seiten-Code übergeben werden und im Profil des Besuchers für die zukünftige Verwendung gespeichert werden.<br>Die Profilattribute auf der Seite erlauben es, benutzerspezifische Daten im Profil von Target zu speichern, um sie später für ein Targeting gezielt zu segmentieren. |
| [Skript-Profilattribute](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/script-profile-attributes/){target=_blank} | Skript-Profilattribute sind Name-Wert-Paare, die in der Target-Anwendung definiert sind. Der Wert wird durch die Ausführung eines JavaScript-Snippets auf dem Target-Server über den Server-Aufruf ermittelt.<br>Benutzer schreiben kleine Code-Snippets, die pro Mbox-Aufruf ausgeführt werden, bevor ein Besucher für eine Zielgruppenmitgliedschaft und -aktivität ausgewertet wird. |
| [Datenanbieter](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/data-providers/){target=_blank} | Mit Datenanbietern können Sie Daten von Drittanbietern einfach an Target weitergeben. |
| [Bulk-Profil-Update-API](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/bulk-profile-update-api/){target=_blank} | Senden Sie über die API eine CSV-Datei an Target mit Aktualisierungen des Besucherprofils für viele Besucher. Jedes Besucherprofil kann mit mehreren In-Page-Profilattributen in einem Aufruf aktualisiert werden. |
| [Single-Profil-API](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/single-profile-update-api/){target=_blank} | Fast identisch mit der Bulk Profile Update API, aber ein Besucherprofil wird gleichzeitig aktualisiert, und zwar in Übereinstimmung mit dem API-Aufruf und nicht mit einer CSV-Datei. |
| [Kundenattribute](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/customer-attributes/){target=_blank} | Mithilfe von Kundenattributen können Sie Besucherprofildaten per FTP in die Experience Cloud hochladen. Verwenden Sie nach dem Hochladen die Daten in Adobe Analytics und Adobe Target. |












