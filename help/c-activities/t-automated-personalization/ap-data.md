---
description: Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
seo-description: Adobe Target erfasst und verwendet eine Vielzahl von Daten, um seine Personalisierungsalgorithmen in automatisierten Personalisierungs- (AP)- und automatisierten (AT)-Aktivitäten zu erstellen. Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
seo-title: Datenerfassung für die Personalisierungs-Algorithmen von Adobe Target
solution: Target
title: Datenerfassung für die Target-Personalisierungsalgorithmen
title-outputclass: Premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: Premium
translation-type: tm+mt
source-git-commit: 1662c5e83a3712626536a659e5001cd537343883

---


# ![PREMIUM](/help/assets/premium.png) Datenerfassung für die Target-Personalisierungsalgorithmen{#data-collection-for-the-target-personalization-algorithms}

Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.

Weitere Informationen über die Target-Personalisierungsalgorithmen finden Sie unter [Random-Forest-Algorithmus](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

Folgende Tabelle zeigt die Daten, die von der automatisierten Personalisierung standardmäßig erfasst werden, ohne dass der Marketing-Experte hierfür eine Aktion durchführen muss, sowie die Namenskonvention, die zur Anzeige dieser Attribute in [Berichten zu Personalization Insights](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) verwendet wird. Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen über das Hochladen zusätzlicher Daten finden Sie unter [Hochladen von Daten für die Personalisierungsalgorithmen von Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Datentyp | Beschreibung | Datentyp-Namenskonvention | Beispielattribute |
| --- | --- | --- | --- |
| URL-Parameter | Target untersucht die URL, um die URL-Parameter zu extrahieren. | `Custom - URL Parameter - [URL Parameter]` | Benutzerspezifische Daten |
| Verweisende URL-Parameter | Im Allgemeinen entspricht die verweisende URL der URL, die auf eine bestimmte Seite verweist, die den Mbox-Aufruf initiiert hat.<br>Beachten Sie, dass sich die Aktivität der Benutzer auf Ihrer Site und die technische Implementierung Ihrer Site auf diese Variable auswirken kann. | `Custom - [Referring URL Parameter] - [Parameter value]` | Benutzerspezifische Daten |
| Umgebungs- und Sitzungsdaten | Informationen darüber, wie und wann der Benutzer auf die Aktivität zugreift.<br>Siehe &quot;Umgebungs- und Sitzungsdaten&quot; . | `Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]` | Besucherprofil – Beginn des letzten Besuchs<br>Besucherprofil – Gesamtbesuche<br>Besucherprofil – Durchschnittl. Zeit pro Besuch<br>Browser – Zeitzone<br>Browser – Wochentag<br>Browser – Spracheinstellung<br>Browser – Typ<br>Betriebssystem – Version |
| Geografisch | Informationen zum Standort des Besuchers.<br>Siehe &quot;Geografische Daten&quot; unten. | `Geo - [geo attribute]` | Stadt<br>Land<br>Region/Bundesstaat<br>Postleitzahl<br>Breitengrad<br>Längengrad<br>ISP oder Mobilnetzbetreiber |
| Gerät und Mobildaten | Gerät- und mobilspezifische Informationen.<br>Siehe &quot;Geräte- und Mobildaten&quot; . | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Mobilgerät - osmobile<br>Screen Size |

Die folgenden Abschnitte enthalten detaillierte Informationen zu den verschiedenen Datentypen, einschließlich Attributnamen, Beschreibungen und Beispielwerten.

>[!NOTE]
>
>Einige der Werte in den folgenden Tabellen wurden auf die nächste Ganzzahl oder Stunde gerundet.

## Umgebungs- und Sitzungsdaten

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Browser – Wochentag | Der Tag der Woche, an dem der Besucher auf die Aktivität zugreift. | 0 bis 6.<br>(0 ist Sonntag) |
| Browser - Stunde des Tages | Die Stunde des Tages, an dem der Besucher auf die Aktivität zugreift. | 0 bis 23<br>(0 ist Mitternacht) |
| Browser - Wochenstunde | Die Stunde der Woche, an der der Besucher auf die Aktivität zugreift. | 0 bis 168<br>(Sonntag Mitternacht ist 0) |
| Browser – Spracheinstellung | Die im Browser des Besuchers festgelegte Sprache, mit der der Zugriff auf die Aktivität erfolgt. | Enghdeutsch<br> |
| Browser - Bildschirmhöhe (px) | Die Browserbildschirmhöhe des Geräts (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Browser - Tageszeit | Die Uhrzeit des Browsers, an dem der Besucher auf die Aktivität zugreift. | 0, 6, 12, 18<br>(0 ist Nacht, 6 ist morgen, 12 ist nachmittag, 18 ist Abend) |
| Browser – Zeitzone | Die Zeitzone des Besuchers beim Zugriff auf die Aktivität. | Pacific timeeastern<br>timegmt<br> |
| Browser – Typ | Der Typ des Browsers, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Chromefirefoxinternet<br><br>explorersafariother<br><br> |
| Browser - Wochentag/Wochenende | Der Arbeitsstatus, als der Besucher auf die Aktivität zugreift (Wochenende, Arbeitsstunden oder Wochentag). | Samstag und Sonntag ist der Wochenendmontag<br>bis Freitag 0900 bis 1800, bis der Freitag<br>bis Freitag 1800 ist, bis 9000 Uhr Wochentag ist. |
| Browser - Fensterhöhe (px) | Die Fensterhöhe des Browsers (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Browser - Fensterbreite (px) | Die Fensterbreite des Browsers (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Gerät - Bildschirmhöhe | Die Bildschirmhöhe des Geräts, mit dem der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Gerät - Bildschirmbreite | Die Bildschirmbreite des Geräts, mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Mobil &gt; Pixeldichte (ppi) | Die Pixeldichte des Mobilgeräts, mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Betriebssystem | Das Betriebssystem auf dem Gerät des Besuchers, das für den Zugriff auf die Aktivität verwendet wird. | Mac oswindowslinuxsearch<br><br><br>botunknown<br>OS |
| Betriebssystem - Version | Die Version des Betriebssystems, mit der der Besucher auf die Aktivität zugreift. | Windows 10<br>Mac OS 10 |
| Traffic-Quellen - URL der verweisenden Einstiegsseite | Die erste Seite, die der Besucher beim Zugriff auf Ihre Site sah. | `https://www.adobe.com/ecloud.html` |

## Geografische Daten

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Geo - Stadt | Die Stadt, von der aus der Besucher auf die Aktivität zugreift. | San Francisco |
| Geo - Land | Das Land, von dem aus der Besucher auf die Aktivität zugreift. | Deutschland |
| Geo - DMA | Der angegebene Marketingbereich (DMA), von dem aus der Besucher auf die Aktivität zugreift. | Charlottesville |
| Geo - Breitengrad | Der Breitengrad, von dem aus der Besucher auf die Aktivität zugreift. | 47.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) |
| Geo - Längengrad | Der Längengrad, von dem aus der Besucher auf die Aktivität zugreift. | -122.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) |
| Geo - Bundesland/Region | Der Status oder die Region, von dem aus der Besucher auf die Aktivität zugreift. | Utahnew<br>South Wales |
| Geo - Postleitzahl | Der Postleitzahl, von dem aus der Besucher auf die Aktivität zugreift. | 84004 |
| Mobilnetzbetreiber - Netzbetreiber | Der Mobilnetzbetreiber, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Vodafonet<br>-Mobile |
| Netzwerk - Verbindungsgeschwindigkeit | Die Netzwerkverbindungsgeschwindigkeit des Geräts, wenn der Besucher auf die Aktivität zugreift. | Broadbandcabledslmobilewirelesssatellite<br><br><br><br><br> |
| Netzwerk - Domänenname | Der Name der Netzwerkdomäne, von der aus der Besucher auf die Aktivität zugreift. | `nnt.net` |
| Netzwerk - ISP | Das Netzwerk, von dem aus der Besucher auf die Aktivität zugreift. | nnt communications corporation |

## Geräte- und Mobildaten

| Attribute name | Attributbeschreibung | Beispielwerte |
| --- | --- | --- |
| Mobil - Gerät - Marke | Die Marke des Mobilgeräts, mit der der Besucher auf die Aktivität zugreift. | Apple |
| Mobilgerät - Gerät - Modellname | Der Modellname des mobilen Geräts, mit dem der Besucher auf die Aktivität zugreift. | Iphone XS |
| Mobile - OS - OSX | Gibt an, ob der Benutzer für den Zugriff auf die Aktivität ein OSX-Gerät verwendet hat. | 0 lautet False, 1 ist true |
| Mobil - Bildschirmhöhe (px) | Die Bildschirmhöhe des Mobilgeräts (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |
| Mobil - Bildschirmbreite (px) | Die Bildschirmbreite des Mobilgeräts (in Pixel), mit der der Besucher auf die Aktivität zugreift. | 1, 2, 3 usw. |