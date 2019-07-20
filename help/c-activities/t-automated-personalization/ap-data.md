---
description: Adobe Target erfasst und verwendet eine Vielzahl von Daten, um seine Personalisierungsalgorithmen in automatisierten Personalisierungs- (AP)- und automatisierten (AT)-Aktivitäten zu erstellen. Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
keywords: Umgebungsdaten; session data; geo data; geografische Daten; Gerätedaten; mobile data; attribute; Profilattribute
seo-description: Adobe Target erfasst und verwendet eine Vielzahl von Daten, um seine Personalisierungsalgorithmen in automatisierten Personalisierungs- (AP)- und automatisierten (AT)-Aktivitäten zu erstellen. Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
seo-title: Datenerfassung für die Personalisierungs-Algorithmen von Adobe Target
solution: Target
title: Datenerfassung für die Target-Personalisierungsalgorithmen
title-outputclass: Premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: Premium
translation-type: tm+mt
source-git-commit: 156587a0375fe2dbf8c461e310b2eae04b491b57

---


# ![PREMIUM](/help/assets/premium.png) Datenerfassung für die Target-Personalisierungsalgorithmen{#data-collection-for-the-target-personalization-algorithms}

Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.

Weitere Informationen über die Target-Personalisierungsalgorithmen finden Sie unter [Random-Forest-Algorithmus](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

The following table shows the data collected by Automated Personalization and Auto-Target by default, without the marketer having to do anything, as well as the naming convention used to indicate these attributes in [Personalization Insights Reports](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen über das Hochladen zusätzlicher Daten finden Sie unter [Hochladen von Daten für die Personalisierungsalgorithmen von Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Datentyp | Beschreibung | Datentyp-Namenskonvention | Beispielattribute |
| --- | --- | --- | --- |
| [Geräte- und Mobildaten](#device-mobile) | Gerät- und mobilspezifische Informationen.<br>Siehe "Geräte- und Mobildaten" . | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Mobile Device OS<br>Mobile Screen Size |
| [Umgebungsdaten](#env) | Informationen über das Betriebssystem des Besuchers und darauf, wie und wann der Besucher auf die Aktivität zugreift. | `Browser - / Operating System] - [Attribute Name]` | Browser – Typ |
| Erlebnis Cloud-Segment | Zielgruppen, die in Audience Manager oder Analytics erstellt und über die Experience Cloud freigegeben wurden | `Custom - Experience Cloud Audience - [Audience Name]` | Benutzerspezifische Daten |
| [Geografische Daten](#geo) | Informationen zum Standort des Besuchers.<br>Siehe "Geografische Daten" unten. | `Geo - [geo attribute]` | Stadt<br>Land<br>Region/Bundesstaat<br>Postleitzahl<br>Breitengrad<br>Längengrad<br>ISP oder Mobilnetzbetreiber |
| Profilattribute | Profilskripte oder Attribute direkt über die Aktualisierungs-API in das Target-Profil hochgeladen | `Custom - Visitor Profile - [attribute name]` | Benutzerspezifische Daten |
| Verweisende URL-Parameter | Im Allgemeinen entspricht die verweisende URL der URL, die auf eine bestimmte Seite verweist, die den Mbox-Aufruf initiiert hat.<br>Beachten Sie, dass sich die Aktivität der Benutzer auf Ihrer Site und die technische Implementierung Ihrer Site auf diese Variable auswirken kann. | `Custom - [Referring URL Parameter] - [Parameter value]` | Benutzerspezifische Daten |
| Berichterstellungssegmente | Alle in der Aktivitätseinrichtung eingerichteten Segmente. | `Reporting Segment -[Segment Name]` | Benutzerspezifische Daten |
| [Sitzungsdaten](#session) | Informationen über das Verhalten des Besuchers in der Sitzung beim Zugriff auf die Aktivität. | `Visitor Profile - [Attribute Name]` | Besucherprofil – Beginn des neuesten Besuchs |
| URL-Parameter | Target untersucht die URL, um die URL-Parameter zu extrahieren. | `Custom - URL Parameter - [URL Parameter]` | Benutzerspezifische Daten |

Die folgenden Abschnitte enthalten detaillierte Informationen zu den verschiedenen Datentypen, einschließlich Attributnamen, Beschreibungen und Beispielwerten.

## Device and Mobile data {#device-mobile}

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Mobil - Gerät - Marke | Die Marke des Mobilgeräts, mit der der Besucher auf die Aktivität zugreift. | Apple |
| Mobil - Gerät - ereader | Gibt an, ob es sich bei dem Gerät um ein ereader handelt. | 0 lautet False, 1 ist true |
| Mobil - Gerät - Spielekonsole | Gibt an, ob das Gerät eine Spielekonsole ist. | 0 lautet False, 1 ist true |
| Mobil - Gerät - Medienplayer | Gibt an, ob das Gerät ein Medienplayer ist. | 0 lautet False, 1 ist true |
| Mobil - Gerät - Mobiltelefon | Gibt an, ob das Gerät ein Mobiltelefon ist. | 0 lautet False, 1 ist true |
| Mobilgerät - Gerät - Modellname | Der Modellname des mobilen Geräts, mit dem der Besucher auf die Aktivität zugreift. | Iphone XS |
| Gerät - Set-Top-Box | Gibt an, ob das Gerät ein Set-Top-Feld ist. | 0 lautet False, 1 ist true |
| Mobil - Gerät - Tablet | Gibt an, ob das Gerät ein Tablet ist. | 0 lautet False, 1 ist true |
| Mobil - Pixeldichte (ppi) | Die Pixeldichte des Mobilgeräts, mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Mobil - OS - OSX (Android, Windows usw.) | Gibt an, ob der Benutzer ein OSX (oder Android, Windows usw.) verwendet hat. Gerät, um auf die Aktivität zuzugreifen. | 0 lautet False, 1 ist true |
| Mobil - Bildschirmhöhe (px) | Die Bildschirmhöhe des Mobilgeräts (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Mobil - Bildschirmbreite (px) | Die Bildschirmbreite des Mobilgeräts (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |

## Environmental data {#env}

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Browser – Wochentag | Der Tag der Woche, an dem der Besucher auf die Aktivität zugreift. | 0 bis 6.<br>(0 ist Sonntag) |
| Browser - Stunde des Tages | Die Stunde des Tages, an dem der Besucher auf die Aktivität zugreift. | 0 to 23<br>(0 is midnight) |
| Browser - Wochenstunde | Die Stunde der Woche, an der der Besucher auf die Aktivität zugreift. | 0 to 168<br>(Sunday midnight is 0) |
| Browser – Spracheinstellung | Die im Browser des Besuchers festgelegte Sprache, mit der der Zugriff auf die Aktivität erfolgt. | English<br>German |
| Browser - Bildschirmhöhe (px) | Die Browserbildschirmhöhe des Geräts (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Browser - Tageszeit | Die Uhrzeit des Browsers, an dem der Besucher auf die Aktivität zugreift. | 0, 6, 12, 18<br>(0 is night, 6 is morning,<br>12 is afternoon, 18 is evening) |
| Browser – Zeitzone | Die Zeitzone des Besuchers beim Zugriff auf die Aktivität. | Pacific Time<br>Eastern Time<br>GMT |
| Browser – Typ | Der Typ des Browsers, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other |
| Browser - Wochentag/Wochenende | Der Arbeitsstatus, als der Besucher auf die Aktivität zugreift (Wochenende, Arbeitsstunden oder Wochentag). | Saturday and Sunday is weekend<br>Monday-Friday 0900 to 1800 is work time<br>Monday-Friday after 1800 until 0900 is weekday free time |
| Browser - Fensterhöhe (px) | Die Fensterhöhe des Browsers (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Browser - Fensterbreite (px) | Die Fensterbreite des Browsers (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Gerät - Bildschirmhöhe | Die Bildschirmhöhe des Geräts, mit dem der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Gerät - Bildschirmbreite | Die Bildschirmbreite des Geräts, mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Betriebssystem | Das Betriebssystem auf dem Gerät des Besuchers, das für den Zugriff auf die Aktivität verwendet wird. | Mac OS<br>Windows<br>Linux<br>Search Bot<br>Unknown OS |
| Betriebssystem - Version | Die Version des Betriebssystems, mit der der Besucher auf die Aktivität zugreift. | Windows 10<br>Mac OS 10 |
| Traffic-Quellen - URL der verweisenden Einstiegsseite | Die erste Seite, die der Besucher beim Zugriff auf Ihre Site sah. | `https://www.adobe.com/ecloud.html` |

## Geographical data {#geo}

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Geo - Stadt | Die Stadt, von der aus der Besucher auf die Aktivität zugreift. | San Francisco |
| Geo - Land | Das Land, von dem aus der Besucher auf die Aktivität zugreift. | Deutschland |
| Geo - DMA | Der angegebene Marketingbereich (DMA), von dem aus der Besucher auf die Aktivität zugreift. | Charlottesville |
| Geo - Breitengrad | Der Breitengrad, von dem aus der Besucher auf die Aktivität zugreift. | 47.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy) |
| Geo - Längengrad | Der Längengrad, von dem aus der Besucher auf die Aktivität zugreift. | -122.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy) |
| Geo - Bundesland/Region | Der Status oder die Region, von dem aus der Besucher auf die Aktivität zugreift. | Utah<br>New South Wales |
| Geo - Postleitzahl | Der Postleitzahl, von dem aus der Besucher auf die Aktivität zugreift. | 84004 |
| Mobilnetzbetreiber - Netzbetreiber | Der Mobilnetzbetreiber, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Vodafone<br>T-Mobile |
| Netzwerk - Verbindungsgeschwindigkeit | Die Netzwerkverbindungsgeschwindigkeit des Geräts, wenn der Besucher auf die Aktivität zugreift. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite |
| Netzwerk - Domänenname | Der Name der Netzwerkdomäne, von der aus der Besucher auf die Aktivität zugreift. | `nnt.net` |
| Netzwerk - ISP | Das Netzwerk, von dem aus der Besucher auf die Aktivität zugreift. | nnt communications corporation |

## Session data {#session}

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Besucherprofil - Wert der Aktivitätslebensdauer | Gibt die Summe aller Bestellwerte für alle Besuche/Sitzungen einer bestimmten Aktivität an. | Double |
| Besucherprofil - Aktivitätslebensdauer auf der Site | Gibt die Gesamtbesuchszeit des Besuchers an, wobei die aktuelle Sitzung ausgeschlossen wird, und wird aktualisiert, wenn die Sitzung abläuft. | Double, Millisekunden |
| Besucherprofil - Durchschnittliche Seitenansichten pro Besuch während der Aktivität | Gibt die durchschnittliche Anzahl der Seitenansichten pro Sitzung an, wobei die aktuelle Sitzung ausgeschlossen wird. | Double |
| Besucherprofil – Durchschnittliche Zeit pro Besuch | Gibt die durchschnittliche Zeit pro Besuch/Sitzung an. Dies schließt die aktuelle Sitzung kein. | Double, Millisekunden |
| Besucherprofil - Erster Besuch | Gibt den Zeitpunkt des ersten Besuchs an, den der Benutzer mit Target interagiert hat. | Double, Millisekunden |
| Besucherprofil - Stunden seit dem letzten Besuch | Gibt die Stunden seit dem letzten Besuch dieser bestimmten Aktivität an. | Double (nur ganzzahlpositive positive Zahl) 1, 2, 3 usw. |
| Besucherprofil - Impressionen für Standort/Inhalt | Gibt die Anzahl der Impressionen an einer bestimmten Kombination aus Position/Inhalt in einer bestimmten Aktivität an. | Double (nur ganzzahlpositive positive Zahl) 1, 2, 3 usw. |
| Besucherprofil - Letzte Target-Interaktion | Gibt den Zeitpunkt der letzten Interaktion mit Target an. Interaktionen erfolgen bei jeder mbox-Anfrage, da die aktuelle Implementierung von Target das Profil bei jeder Anforderung aktualisiert. | Double, Millisekunden |
| Besucherprofil - Vor Aktivität gesehene Seiten | Gibt die Anzahl der Gesamtseitenansichten (Impressionen) einschließlich aktueller Besuche/Sitzung an, bis der Besucher die Aktivität aufruft. | Double (nur ganzzahlpositive positive Zahl) 1, 2, 3 usw. |
| Besucherprofil - Seitenansichten im aktuellen Besuch | Gibt die Anzahl der Seitenansichten im aktuellen Besuch/Besuch an, bis der Besucher die Aktivität aufruft. Genauer ausgedrückt, die Anzahl der Impressionen. Diese Impressionen sind keine echten Seitenansichten, sondern wie oft die Anforderung Target erreicht hat. Target kann nicht zwischen Timeouts und anderen Gründen unterscheiden, weshalb der Benutzer den Inhalt weder empfangen noch anzeigen konnte. | Double (nur Ganzzahlpositive positive Zahl) |
| Besucherprofil - Beginn des aktuellen Besuchs | Gibt den Zeitpunkt an, zu dem der aktuelle Besuch/die aktuelle Sitzung mit Target gestartet wurde. Der Besuch mit Target kann ohne Eingabe einer Aktivität eingeleitet werden. Alles, was erforderlich ist, ist ein Aufruf einer beliebigen mbox. Ein Besucher kann bis zur Teilnahme an der Aktivität vorgehen und der Schnappschuss wird durchgeführt. | Double, Millisekunden |
| Besucherprofil – Beginn des neuesten Besuchs | Gibt den Zeitpunkt an, zu dem der letzte Besuch/die letzte Sitzung mit Target gestartet wurde. Dieses Attribut wird aktualisiert, wenn die Sitzung abläuft.<br>Wenn dies die erste Sitzung für den Besucher ist, führt dies zu `LAST_SESSION_START = 0.` | Double, Millisekunden |
| Besucherprofil - Zeit seit dem letzten Besuch beim ersten Eingeben der Aktivität | Gibt die Dauer zwischen der vorherigen Sitzung und dem Zeitpunkt an, zu dem der Benutzer die Aktivität aufruft und der Schnappschuss ausgeführt wird. | Double, Millisekunden |
| Besucherprofil - Zeit im Besuch vor der Aktivität | Gibt den Unterschied zwischen der letzten Interaktion mit Target und dem Start des aktuellen Besuchs an. Dieses Attribut kann als Besuchs-/Sitzungsdauer betrachtet werden, bis der Benutzer die Aktivität aufruft und der Schnappschuss ausgeführt wird.<br>Negative Werte treten auf, wenn die Sitzung beginnt und die letzte Aktualisierungszeit durch denselben mbox-Aufruf ausgelöst wird. Negative Werte sollten als 0 (Null) betrachtet werden. | Double, Millisekunden |
| Besucherprofil – Gesamtbesuche | Gibt die Gesamtzahl der Besuche/Sitzungen an. Schließt den aktuellen Besuch/die aktuelle Sitzung kein. | Double (nur ganzzahlpositive positive Zahl) 1, 2, 3 usw. |
| Besucherprofil - Gesamtbesuche in Aktivität | Gibt die Anzahl der Besuche einer bestimmten Aktivität an. Wenn kein vorheriger Besuch vorhanden ist, wird 0 (null) zurückgegeben. | Double (nur ganzzahlpositive positive Zahl) 1, 2, 3 usw. |
| Besucherprofil - Gesamtbesuche in Aktivität mit Umrechnung | Gibt die Anzahl der Besuche/Sitzungen für eine bestimmte Aktivität an, wenn mindestens eine Konversion während des Besuchs stattgefunden hat. | Double |
| Besucherprofil - Besuche in Aktivität ohne Umrechnung | Anzahl der Besuche/Sitzungen ohne Konversionen zu einer bestimmten Aktivität. Dieser Wert wird nach der Konvertierung auf Null zurückgesetzt oder -1, wenn die Konvertierung nie erfolgte. | Double (nur ganzzahlpositive positive Zahl) 1, 2, 3 usw. |
