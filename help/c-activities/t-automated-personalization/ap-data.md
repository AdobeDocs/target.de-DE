---
keywords: environmental data;session data;geo data;geographical data;device data;mobile data;attributes;profile attributes
description: Adobe Target sammelt und verwendet automatisch eine Vielzahl von Daten zum Erstellen der Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird diese Momentaufnahme an Informationen an ein Set von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
title: Datenerfassung für die Adobe Target-Personalisierungsalgorithmen
feature: null
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1755'
ht-degree: 96%

---


# ![PREMIUM](/help/assets/premium.png) Datenerfassung für die Target-Personalisierungsalgorithmen{#data-collection-for-the-target-personalization-algorithms}

Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird diese Momentaufnahme an Informationen an ein Set von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.

Weitere Informationen über die Target-Personalisierungsalgorithmen finden Sie unter  [Random-Forest-Algorithmus](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

Folgende Tabelle zeigt die Daten, die von der automatisierten Personalisierung und dem automatischen Targeting standardmäßig erfasst werden, ohne dass der Marketingexperte hierfür eine Aktion durchführen muss, sowie die Namenskonvention, die zur Anzeige dieser Attribute in [Berichten zu Personalization Insights](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) verwendet wird. Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen über das Hochladen zusätzlicher Daten finden Sie unter  [Hochladen von Daten für die Personalisierungsalgorithmen von Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Datentyp | Beschreibung | Datentyp-Namenskonvention | Beispielattribute |
| --- | --- | --- | --- |
| [Gerät und Mobildaten](#device-mobile) | Gerät- und mobilspezifische Informationen.<br>Siehe unten „Gerät und Mobildaten“. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Betriebssystem des Mobilgeräts<br>Bildschirmgröße des Mobilgeräts |
| [Umgebungsdaten](#env) | Informationen über das Betriebssystem des Besuchers und darüber, wie und wann der Besucher auf die Aktivität zugreift. | `Browser - / Operating System] - [Attribute Name]` | Browser - Type |
| Experience Cloud-Segment | Zielgruppen, die in Audience Manager oder Analytics erstellt und über Experience Cloud freigegeben wurden | `Custom - Experience Cloud Audience - [Audience Name]` | Benutzerspezifische Daten |
| [Geografische Daten](#geo) | Informationen zum Standort des Besuchers.<br>Siehe „Geografische Daten“ unten. | `Geo - [geo attribute]` | Stadt<br>Land<br>Region/Bundesstaat<br>Postleitzahl<br>Breitengrad<br>Längengrad<br>ISP oder Mobilnetzbetreiber |
| Profilattribute | Profilskripte oder Attribute, die direkt über die Aktualisierungs-API in das Target-Profil hochgeladen werden | `Custom - Visitor Profile - [attribute name]` | Benutzerspezifische Daten |
| Verweisende URL-Parameter | In general, the referring URL is the URL that referred to a particular page that initiated the Target call.<br>Beachten Sie, dass sich die Aktivität der Benutzer auf Ihrer Site und die technische Implementierung Ihrer Site auf diese Variable auswirken kann. | `Custom - [Referring URL Parameter] - [Parameter value]` | Benutzerspezifische Daten |
| Berichtssegmente | Alle bei der Aktivitätseinrichtung ausgewählte Segmente. | `Reporting Segment -[Segment Name]` | Benutzerspezifische Daten |
| [Sitzungsdaten](#session) | Informationen über das Verhalten des Besuchers in der Sitzung beim Zugriff auf die Aktivität | `Visitor Profile - [Attribute Name]` | Visitor Profile - Start of Most Recent Visit |
| URL-Parameter | Target untersucht die URL, um die URL-Parameter zu extrahieren. | `Custom - URL Parameter - [URL Parameter]` | Benutzerspezifische Daten |

Die folgenden Abschnitte enthalten detaillierte Informationen zu den verschiedenen Datentypen, einschließlich Attributnamen, Beschreibungen und Beispielwerte.

## Gerät und Mobildaten {#device-mobile}

| Attributname | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Mobile - Device - Brand | Die Marke des Mobilgeräts, mit der der Besucher auf die Aktivität zugegriffen hat. | Apple |
| Mobile - Device - eReader | Gibt an, ob es sich bei dem Gerät um einen E-Book-Reader handelt. | 0 ist „false“, 1 ist „true“ |
| Mobile - Device - Game Console | Gibt an, ob das Gerät eine Spielkonsole ist. | 0 ist „false“, 1 ist „true“ |
| Mobile - Device - Media Player | Gibt an, ob das Gerät ein Media Player ist. | 0 ist „false“, 1 ist „true“ |
| Mobile - Device - Mobile Phone | Gibt an, ob das Gerät ein Mobiltelefon ist. | 0 ist „false“, 1 ist „true“ |
| Mobile - Device - Model Name | Der Modellname des Mobilgeräts, mit dem der Besucher auf die Aktivität zugegriffen hat. | iPhone XS |
| Device - Set-Top Box | Gibt an, ob das Gerät eine Set-Top-Box ist. | 0 ist „false“, 1 ist „true“ |
| Mobile - Device - Tablet | Gibt an, ob das Gerät ein Tablet ist. | 0 ist „false“, 1 ist „true“ |
| Mobile - Pixel Density (ppi) | Die Pixeldichte des Mobilgeräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Mobilgerät – Betriebssystem - OSX (Android, Windows usw.) | Gibt an, ob der Benutzer ein OSX (oder Android, Windows usw.) verwendet hat. Gerät, um auf die Aktivität zuzugreifen. | 0 ist „false“, 1 ist „true“ |
| Mobile - Screen Height (px) | Die Bildschirmhöhe des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Mobile - Screen Width (px) | Die Bildschirmbreite des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |

## Umgebungsdaten {#env}

| Attributname | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Browser - Day of Week | Der Tag der Woche, an dem der Besucher auf die Aktivität zugegriffen hat. | 0 bis 6<br>(0 ist Sonntag) |
| Browser - Hour of Day | Die Stunde des Tages, in der der Besucher auf die Aktivität zugegriffen hat. | 0 bis 23<br>(0 ist Mitternacht) |
| Browser - Hour of Week | Die Stunde der Woche, in der der Besucher auf die Aktivität zugegriffen hat. | 0 bis 168<br>(Sonntag Mitternacht ist 0) |
| Browser - Language Setting | Die im Browser des Besuchers festgelegte Sprache, mit der der Zugriff auf die Aktivität erfolgt. | English<br>German |
| Browser - Screen Height (px) | Die Browserbildschirmhöhe des Geräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Browser - Time of Day | Die Uhrzeit des Browsers, zu der der Besucher auf die Aktivität zugegriffen hat. | 0, 6, 12, 18<br>(0 ist Nacht, 6 ist Morgen,<br>12 ist Nachmittag, 18 ist Abend) |
| Browser - Timezone | Die Zeitzone, in der der Besucher auf die Aktivität zugegriffen hat. | Pacific Time<br>Eastern Time<br>GMT |
| Browser - Type | Der Typ des Browsers, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other |
| Browser - Weekday/Weekend | Der Werktagsstatus, unter dem der Besucher auf die Aktivität zugegriffen hat (Wochenende, Arbeitsstunden oder Wochentags-Freizeit). | Samstag und Sonntag ist Wochenende<br>Montag bis Freitag 0900 bis 1800 Uhr<br>Montag bis Freitag 1800 bis 0900 Uhr ist Wochentags-Freizeit. |
| Browser - Window Height (px) | Die Fensterhöhe des Browsers (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Browser - Window Width (px) | Die Fensterbreite des Browsers (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Device - Screen Height | Die Bildschirmhöhe des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Device - Screen Width | Die Bildschirmbreite des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. |
| Betriebssystem | Das Betriebssystem auf dem Gerät des Besuchers, das für den Zugriff auf die Aktivität verwendet wurde. | Mac OS<br>Windows<br>Linux<br>Search Bot<br>OS Unknown |
| Operating System - Version | Die Version des Betriebssystems, mit der der Besucher auf die Aktivität zugegriffen hat. | Windows 10<br>Mac OS 10 |
| Traffic Sources - Referring Landing Page URL | Die erste Seite, die der Besucher beim Zugriff auf Ihre Site gesehen hat. | `https://www.adobe.com/ecloud.html` |

## Geografische Daten {#geo}

| Attributname | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Geo - City | Die Stadt, von der aus der Besucher auf die Aktivität zugegriffen hat. | San Francisco |
| Geo - Country | Das Land, von dem aus der Besucher auf die Aktivität zugegriffen hat. | Deutschland |
| Geo - DMA | Der angegebene Marketingbereich (DMA), von dem aus der Besucher auf die Aktivität zugegriffen hat. | Charlottesville |
| Geo - Latitude | Der Breitengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 47.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) |
| Geo - Longitude | Der Längengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | -122.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) |
| Geo - State/Region | Der Bundesstaat oder die Region, von der aus der Besucher auf die Aktivität zugegriffen hat. | Utah<br>New South Wales |
| Geo - Zip Code | Die Postleitzahl, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 84004 |
| Mobile - Carrier | Der Mobilnetzbetreiber, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Vodafone<br>T-Mobile |
| Network - Connection Speed | Die Netzwerkverbindungsgeschwindigkeit des Geräts, als der Besucher auf die Aktivität zugegriffen hat. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite |
| Network - Domain Name | Der Name der Netzwerkdomäne, von der aus der Besucher auf die Aktivität zugegriffen hat. | `nnt.net` |
| Network - ISP | Das Netzwerk, von dem aus der Besucher auf die Aktivität zugegriffen hat. | nnt communications corporation |

## Sitzungsdaten {#session}

| Attributname | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Visitor Profile - Activity Lifetime Order Value | Gibt die Summe aller Bestellwerte für alle Besuche/Sitzungen einer bestimmten Aktivität an. | Doppelt |
| Visitor Profile - Activity Lifetime Time on Site | Gibt die Gesamtbesuchszeit des Besuchers an, wobei die aktuelle Sitzung ausgeschlossen ist. Sie wird aktualisiert, wenn die Sitzung abgelaufen ist. | Doppelt, Millisekunden |
| Visitor Profile -Average Page Views per Visit during Activity | Gibt die durchschnittliche Anzahl der Seitenansichten pro Sitzung an, wobei die aktuelle Sitzung ausgeschlossen ist. | Doppelt |
| Visitor Profile - Average Time per Visit | Gibt die durchschnittliche Zeit pro Besuch/Sitzung an. Die aktuelle Sitzung ist ausgeschlossen. | Doppelt, Millisekunden |
| Visitor Profile - First Visit | Gibt den Zeitpunkt des ersten Besuchs an, bei dem der Benutzer mit Target interagiert hat. | Doppelt, Millisekunden |
| Visitor Profile - Hours since Last Visit | Gibt die Stunden seit dem letzten Besuch einer bestimmten Aktivität an. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. |
| Visitor Profile - Impressions of Location/Content | Gibt die Anzahl der Impressionen bei einer bestimmten Kombination aus Ort/Inhalt bei einer bestimmten Aktivität an. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. |
| Visitor Profile - Last Target Interaction | Gibt den Zeitpunkt der letzten Interaktion mit Target an. Interaction happens on every [!DNL Target] request because the current implementation of [!DNL Target] updates the profile on each request. | Doppelt, Millisekunden |
| Visitor Profile - Pages Seen Before Activity | Gibt die Anzahl aller Seitenansichten (Impressionen) einschließlich des aktuellen Besuchs/der aktuellen Sitzung an, bevor der Besucher die Aktivität aufruft. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. |
| Visitor Profile - Page Views in Current Visit | Gibt die Anzahl der Seitenansichten beim aktuellen Besuch/bei der aktuellen Sitzung an, bevor der Besucher die Aktivität aufruft. Genauer gesagt, die Anzahl der Impressionen. Diese Impressionen sind keine echten Seitenansichten, sondern geben an, wie oft die Anfrage Target erreicht hat. Target kann nicht zwischen Timeouts und anderen Gründen unterscheiden, weshalb der Benutzer den Inhalt nicht empfangen oder anzeigen kann. | Doppelt (nur positive Ganzzahl) |
| Visitor Profile - Start of Current Visit | Gibt den Zeitpunkt an, zu dem der aktuelle Besuch/die aktuelle Sitzung mit Target begonnen hat. Der Besuch mit Target kann ohne Eingabe einer Aktivität eingeleitet werden. All that is required is a call to any [!DNL Target] request. Es kann einige Zeit dauern, bis ein Besucher die Aktivität auslöst und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden |
| Visitor Profile - Start of Most Recent Visit | Gibt den Zeitpunkt an, zu dem der letzte Besuch/die letzte Sitzung mit Target gestartet wurde. Dieses Attribut wird aktualisiert, wenn die Sitzung abgelaufen ist.<br>Wenn dies die erste Sitzung für den Besucher ist, steht `LAST_SESSION_START = 0.` | Doppelt, Millisekunden |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Gibt die Dauer zwischen der vorherigen Sitzung und dem Zeitpunkt an, zu dem der Benutzer die Aktivität aufruft und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden |
| Visitor Profile - Time in Visit Before Enter Activity | Gibt den Unterschied zwischen der letzten Interaktion mit Target und dem Beginn des aktuellen Besuchs an. Dieses Attribut kann als Besuchs-/Sitzungsdauer betrachtet werden, bis der Benutzer die Aktivität aufruft und die Momentaufnahme erfolgt.<br>Negative Werte treten auf, wenn der Beginn der Sitzung und die letzte Aktualisierungszeit durch denselben [!DNL Target] Aufruf ausgelöst werden. Negative Werte sollten als 0 (Null) betrachtet werden. | Doppelt, Millisekunden |
| Besucherprofil – Gesamtbesuche | Gibt die Gesamtzahl der Besuche/Sitzungen an. Der aktuelle Besuch/die aktuelle Sitzung ist ausgeschlossen. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. |
| Visitor Profile - Total Visits to Activity | Gibt die Anzahl der Besuche bis zu einer bestimmten Aktivität an. Wenn kein vorheriger Besuch vorhanden ist, wird 0 (null) zurückgegeben. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. |
| Visitor Profile - Total Visits to Activity with Conversion | Gibt die Anzahl der Besuche/Sitzungen bis zu einer bestimmten Aktivität an, wenn mindestens eine Konversion während des Besuchs stattgefunden hat. | Double |
| Visitor Profile - Visits to Activity with No Conversion | Anzahl der Besuche/Sitzungen ohne Konversionen bis zu einer bestimmten Aktivität. Dieser Wert wird nach einer Konversion auf null zurückgesetzt oder -1, wenn nie eine Konversion erfolgte. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. |
