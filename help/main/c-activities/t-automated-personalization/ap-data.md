---
keywords: Umgebungsdaten; Sitzungsdaten; Geodaten; geografische Daten; Gerätedaten; mobile Daten; Attribute; Profilattribute; Personalisierungsalgorithmen; Algorithmen für maschinelles Lernen; Algorithmen für maschinelles Lernen
description: Erfahren Sie, welche Daten Adobe haben [!DNL Target] erfasst und verwendet , um seine Algorithmen für maschinelles Lernen zu erstellen.
title: Welche Daten werden erfasst, um Algorithmen für maschinelles Lernen zu erstellen?
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '2023'
ht-degree: 52%

---

# ![PREMIUM](/help/main/assets/premium.png) Von [!DNL Target] Algorithmen für maschinelles Lernen

[!DNL Adobe Target] automatisch eine Vielzahl von Daten erfasst und verwendet, um seine Personalisierungsalgorithmen in [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Automatisches Targeting] (AT) Tätigkeiten. Wenn ein Besucher eine AP- oder AT-Aktivität aufruft, wird eine Momentaufnahme der Informationen an eine Reihe von &quot;Trainings-Datensätzen&quot;übergeben (die Besucherdaten, über die die Personalisierungsalgorithmen lernen).

Weitere Informationen zum [!DNL Target] Personalisierungsalgorithmen, siehe [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Standard [!DNL Adobe Target] Attributkategorien

Die folgende Tabelle zeigt die von [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] Aktivitäten standardmäßig ohne Konfiguration von [!DNL Target] oder andere [!DNL Adobe] -Lösungen sowie der Benennungskonvention, die verwendet wird, um diese Attribute in [Berichte zu Personalization Insights](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen über das Hochladen zusätzlicher Daten finden Sie unter  [Hochladen von Daten für die [!DNL Target] Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Datenkategorie | Systempräfix | Beschreibung | Anzeigename in [!UICONTROL Insights] Berichte |
| --- | --- | --- | --- |
| Umgebungsparameter | ENV | Informationen zur Umgebung eines Benutzers, einschließlich Betriebssystem, Browser und Tageszeit/Wochentag. | Browser - [Attributname]<br>Betriebssystem - [Wert] |
| Geografie | GEO | Informationen zur geografischen Lage eines Benutzers, die über die IP-Suche abgerufen werden. | Geo - [geo-Attribut] |
| Mobilgerät | MOB | Informationen zum Mobilgerät eines Benutzers. | Gerät - [Geräteattribut]<br>Mobile - [mobile attribute] |
| Zielberichtssegmente | SEG | In konfigurierte Berichtssegmente [!DNL Target] Berichterstellung. | Berichtssegment -[Segmentname] |
| Sitzungsverhalten | SES | Informationen zum Benutzerverhalten, z. B. die Anzahl der angezeigten Seiten. | Besucherprofil - [Attributname] |

## Benutzerdefinierte Adobe Target-Attributkategorien

Die folgende Tabelle zeigt die vom Kunden bereitgestellten Daten, die von [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] Aktivitäten. Diese Daten werden nur erfasst, wenn Sie sie bereitstellen. Spezifische Attributnamen und Beispielwerte sind spezifisch für Ihre Systemkonfiguration.

| Datenkategorie | Systempräfix | Beschreibung | Anzeigename in [!UICONTROL Insights] Berichte |
| --- | --- | --- | --- |
| Seitenparameter | BOX | Benutzerdefinierte Seitenparameter (&quot;mbox-Parameter&quot;), die beim Aufruf an [!DNL Target]. | Benutzerspezifisch - Mbox-Parameter - [Parametername] |
| [!DNL Target] Profil | PRO | Benutzerdefinierte Profilattribute, die direkt in die [!DNL Target] Profil über API oder Seitenparameter und [!DNL Target] Profilskripte. | Benutzerspezifisch - Besucherprofil - [Attributname] |
| Kundenattribute | CRS | Kundenattribute, die in die [!DNL Target] Profil über [Adobe Experience Cloud-Kundenattributdienst](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html){target=_blank}. | Benutzerspezifisch - Besucherprofil - [Attributname] |
| URL-Parameter | URL | URL und alle URL-Parameter für die aktuell angezeigte Seite. | Benutzerspezifisch - URL-Parameter - [URL-Parameter] |
| Verweisende URL | REF | Verweisende URL und alle URL-Parameter für die verweisende URL. | Benutzerspezifisch - [Verweisender URL-Parameter] - [Parameterwert] |
| Freigegebene Zielgruppen in Adobe Experience Cloud | AAM | Alle Zielgruppen, die für [!DNL Target] von anderen [!DNL Adobe Experience Cloud] Lösungen (z. B. [!DNL Adobe Audience Manager] und [!DNL Adobe Analytics]über die [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html){target=_blank}). | Benutzerspezifisch - Experience Cloud-Zielgruppe - [Zielgruppenname] |
| Adobe Experience Platform-Zielgruppen in der Echtzeit-Kundendatenplattform | UPS | In der Echtzeit-Kundendatenplattform von AEP gemeinsam genutzte Zielgruppen [!DNL Target] über Ziele. |  |
| Adobe Experience Platform-Attribute zur Echtzeit-Kundendatenplattform | AEP | Für die Echtzeit-Kundendatenplattform von AEP freigegebene Attribute der Kundendatenplattform [!DNL Target] über Ziele. Diese Funktion ist derzeit als Betaversion verfügbar. |  |

## Blocking-Funktionen aus [!DNL Target] Algorithmen für maschinelles Lernen

Funktionen können für [!DNL Target]-Algorithmen des maschinellen Lernens gesperrt werden, sodass sie in keinerlei Modellen oder Aktivitäten für [!UICONTROL Automatisches Targeting] oder [!UICONTROL Automated Personalization] verwendet werden können.

Weitere Informationen finden Sie unter [Übersicht über die Modelle-API (Auf die Blockierungsliste setz)](https://developer.adobe.com/target/before-administer/models-api/){target=_blank} im *Adobe Target-Entwicklerhandbuch*.

## Gerät und Mobildaten {#device-mobile}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Mobile - Device - Brand | Die Marke des Mobilgeräts, mit der der Besucher auf die Aktivität zugegriffen hat. | Apple | MOB_targeting.mobile.vendor |
| Mobile - Device - eReader | Gibt an, ob es sich bei dem Gerät um einen E-Book-Reader handelt. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.ereader |
| Mobile - Device - Game Console | Gibt an, ob das Gerät eine Spielkonsole ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.gamesConsole |
| Mobile - Device - Media Player | Gibt an, ob das Gerät ein Media Player ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.mediaPlayer |
| Mobile - Device - Mobile Phone | Gibt an, ob das Gerät ein Mobiltelefon ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.mobilePhone |
| Mobile - Device - Model Name | Der Modellname des Mobilgeräts, mit dem der Besucher auf die Aktivität zugegriffen hat. | iPhone XS | MOB_targeting.mobile.model |
| Device - Set-Top Box | Gibt an, ob das Gerät eine Set-Top-Box ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.setTopBox |
| Mobile - Device - Tablet | Gibt an, ob das Gerät ein Tablet ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.table |
| Mobile - Pixel Density (ppi) | Die Pixeldichte des Mobilgeräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayPpi |
| Mobilgerät – Betriebssystem - OSX (Android, Windows usw.) | Gibt an, ob der Benutzer ein OSX (oder Android, Windows usw.) verwendet hat. Gerät, um auf die Aktivität zuzugreifen. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.os[BS]<br>Beispiel: MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux |
| Mobile - Screen Height (px) | Die Bildschirmhöhe des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayHeight |
| Mobile - Screen Width (px) | Die Bildschirmbreite des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayWidth |

## Umgebungsdaten {#env}

|Attributname|Attributbeschreibung|Beispielwerte|Systemname| | — | — | — | — | |Browser - Day of Week|Der Wochentag, an dem der Besucher auf die Aktivität zugegriffen hat.|0 bis 6.<br>(0 ist Sonntag)|ENV_DayOfWeek| |Browser - Hour of Day|Die Stunde des Tages, zu der der Besucher auf die Aktivität zugegriffen hat.|0 bis 23<br>(0 ist Mitternacht)|ENV_UserHour| |Browser - Hour of Week|Die Stunde der Woche, in der der Besucher auf die Aktivität zugegriffen hat.|0 bis 168<br>(Sonntag Mitternacht ist 0)|ENV_WeekHour| |Browser - Language Setting|Die Sprache, die im Browser des Besuchers angegeben ist, der für den Zugriff auf die Aktivität verwendet wird.|Englisch<br>German|ENV_Language| |Browser - Time of Day|Die Tageszeit des Browsers, zu der der Besucher auf die Aktivität zugegriffen hat.|0, 6, 12, 18<br>(0 ist Nacht, 6 ist Morgen)<br>12 ist Nachmittag, 18 ist Abend)|ENV_LocalTimePeriod| |Browser - Timezone|Die Zeitzone des Besuchers beim Zugriff auf die Aktivität.|Pacific Time<br>Eastern Time<br>GMT|ENV_BrowserTimezoneOffsetMinutes| |Browser - Typ|Der Typ des Browsers, den der Besucher beim Zugriff auf die Aktivität verwendet hat.|Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other|ENV_Browser| |Browser - Weekday/Weekend|Der Arbeitsstatus, zu dem der Besucher auf die Aktivität zugegriffen hat (Wochenende, Arbeitsstunden oder Wochentagsfreizeit).|Samstag und Sonntag sind Wochenende<br>Montag bis Freitag 0900 bis 1800 ist Arbeitszeit<br>Montag bis Freitag nach 1800 bis 0900 ist Wochentags-Freizeit|ENV_UserHourType| |Browser - Window Height (px)|Die Fensterhöhe des Browsers (in Pixel), mit der der Besucher auf die Aktivität zugegriffen hat.|1, 2, 3 usw.|ENV_BrowserHeight| |Browser - Window Width (px)|Die Fensterbreite des Browsers (in Pixel), mit der der Besucher auf die Aktivität zugegriffen hat.|1, 2, 3 usw.|ENV_BrowserWidth| |Gerät - Bildschirmhöhe (px)|Die Bildschirmhöhe des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat.|1, 2, 3 usw.|ENV_ScreenHeight| |Gerät - Bildschirmbreite (px)|Die Bildschirmbreite des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat.|1, 2, 3 usw.|ENV_ScreenWidth| |Betriebssystem|Das Betriebssystem auf dem Gerät des Besuchers, das für den Zugriff auf die Aktivität verwendet wird.|Mac OS<br>Windows<br>Linux<br>Search Bot<br>Unknown OS|ENV_OperatingSystem| |Betriebssystem - Version|Die Version des Betriebssystems, mit der der Besucher auf die Aktivität zugegriffen hat.|Windows 10<br>Mac OS 10|ENV_OperatingSystemVersion| |Traffic-Quellen - Verweis auf die Landingpage-URL|Die erste Seite, die der Besucher beim Zugriff auf Ihre Site sah.|`https://www.adobe.com/ecloud.html`|ENV_Referrer|

## Geografische Daten {#geo}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Geo - City | Die Stadt, von der aus der Besucher auf die Aktivität zugegriffen hat. | San Francisco | geo_city |
| Geo - Country | Das Land, von dem aus der Besucher auf die Aktivität zugegriffen hat. | Deutschland | geo_country |
| Geo - DMA | Der angegebene Marketingbereich (DMA), von dem aus der Besucher auf die Aktivität zugegriffen hat. | Charlottesville | Geo_DMA |
| Geo - Latitude | Der Breitengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 47.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) | GEO_Latitude |
| Geo - Longitude | Der Längengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | -122.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) | GEO_Longitude |
| Geo - State/Region | Der Bundesstaat oder die Region, von der aus der Besucher auf die Aktivität zugegriffen hat. | Utah<br>New South Wales | GEO_State<br>GEO_Region |
| Geo - Zip Code | Die Postleitzahl, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 84004 | GEO_ZipCode |
| Mobile - Carrier | Der Mobilnetzbetreiber, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | Vodafone<br>T-Mobile | GEO_mobileCarrier |
| Network - Connection Speed | Die Netzwerkverbindungsgeschwindigkeit des Geräts, als der Besucher auf die Aktivität zugegriffen hat. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite | GEO_ConnectionSpeed |
| Network - Domain Name | Der Name der Netzwerkdomäne, von der aus der Besucher auf die Aktivität zugegriffen hat. | `nnt.net` | GEO_DomainName |
| Network - ISP | Das Netzwerk, von dem aus der Besucher auf die Aktivität zugegriffen hat. | nnt communications corporation | GEO_IspName |

## Sitzungsdaten {#session}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Visitor Profile - Activity Lifetime Order Value | Gibt die Summe aller Bestellwerte für alle Besuche/Sitzungen einer bestimmten Aktivität an. | Doppelt | SES_CUMULATIVE_ORDER_VALUE |
| Visitor Profile - Activity Lifetime Time on Site | Gibt die Gesamtbesuchszeit des Besuchers an, wobei die aktuelle Sitzung ausgeschlossen ist. Sie wird aktualisiert, wenn die Sitzung abgelaufen ist. | Doppelt, Millisekunden | SES_TOTAL_TIME |
| Visitor Profile -Average Page Views per Visit during Activity | Gibt die durchschnittliche Anzahl der Seitenansichten pro Sitzung an, wobei die aktuelle Sitzung ausgeschlossen ist. | Doppelt | SES_REQUESTS_PER_SESSION |
| Visitor Profile - Average Time per Visit | Gibt die durchschnittliche Zeit pro Besuch/Sitzung an. Die aktuelle Sitzung ist ausgeschlossen. | Doppelt, Millisekunden | SES_TIME_PER_SESSION |
| Visitor Profile - First Visit | Gibt den Zeitpunkt des ersten Besuchs an, mit dem der Benutzer interagiert hat [!DNL Target]. | Doppelt, Millisekunden | SES_PROFILE_CREATION_TIME |
| Visitor Profile - Hours since Last Visit | Gibt die Stunden seit dem letzten Besuch einer bestimmten Aktivität an. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_HOURS_SINCE_LAST_VISIT |
| Visitor Profile - Impressions of Location/Content | Gibt die Anzahl der Impressionen bei einer bestimmten Kombination aus Ort/Inhalt bei einer bestimmten Aktivität an. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| Besucherprofil - Zuletzt [!DNL Target] Interaction | Gibt den Zeitpunkt der letzten Interaktion mit [!DNL Target]. Interaktionen treten bei jedem [!DNL Target] Anfrage , da die aktuelle Implementierung von [!DNL Target] aktualisiert das Profil bei jeder Anfrage. | Doppelt, Millisekunden | SES_PROFILE_UPDATE_TIME |
| Visitor Profile - Pages Seen Before Activity | Gibt die Anzahl aller Seitenansichten (Impressionen) einschließlich des aktuellen Besuchs/der aktuellen Sitzung an, bevor der Besucher die Aktivität aufruft. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_TOTAL_PAGE_VIEWS |
| Visitor Profile - Page Views in Current Visit | Gibt die Anzahl der Seitenansichten beim aktuellen Besuch/bei der aktuellen Sitzung an, bevor der Besucher die Aktivität aufruft. Genauer gesagt, die Anzahl der Impressionen. Diese Impressionen sind keine echten Seitenansichten, sondern geben an, wie oft die Anfrage Target erreicht hat. Target kann nicht zwischen Timeouts und anderen Gründen unterscheiden, weshalb der Benutzer den Inhalt nicht empfangen oder anzeigen kann. | Doppelt (nur positive Ganzzahl) | SES_SESSION_POSITION |
| Visitor Profile - Start of Current Visit | Gibt den Zeitpunkt an, zu dem der aktuelle Besuch/die aktuelle Sitzung mit Target begonnen hat. Der Besuch mit Target kann ohne Eingabe einer Aktivität eingeleitet werden. Alles, was erforderlich ist, ist ein Aufruf an alle [!DNL Target] -Anfrage. Es kann einige Zeit dauern, bis ein Besucher die Aktivität auslöst und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden | SES_SESSION_START |
| Visitor Profile - Start of Most Recent Visit | Gibt den Zeitpunkt des letzten Besuchs/der letzten Sitzung an mit [!DNL Target] gestartet. Dieses Attribut wird aktualisiert, wenn die Sitzung abgelaufen ist.<br>Wenn dies die erste Sitzung für den Besucher ist, steht `LAST_SESSION_START = 0.` | Doppelt, Millisekunden | SES_LAST_SESSION_START |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Gibt die Dauer zwischen der vorherigen Sitzung und dem Zeitpunkt an, zu dem der Benutzer die Aktivität aufruft und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden | SES_RECENCY |
| Visitor Profile - Time in Visit Before Enter Activity | Gibt den Unterschied zwischen der letzten Interaktion mit [!DNL Target] und zu dem Zeitpunkt, zu dem der aktuelle Besuch begann. Dieses Attribut kann als Besuchs-/Sitzungsdauer betrachtet werden, bis der Benutzer die Aktivität aufruft und die Momentaufnahme erfolgt.<br>Negative Werte treten auf, wenn die Sitzung beginnt und die letzte Aktualisierungszeit durch denselben [!DNL Target] aufrufen. Negative Werte sollten als 0 (Null) betrachtet werden. | Doppelt, Millisekunden | SES_SESSION_TIME |
| Besucherprofil – Gesamtbesuche | Gibt die Gesamtzahl der Besuche/Sitzungen an. Der aktuelle Besuch/die aktuelle Sitzung ist ausgeschlossen. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_TOTAL_SESSIONS |
| Visitor Profile - Total Visits to Activity | Gibt die Anzahl der Besuche bis zu einer bestimmten Aktivität an. Wenn kein vorheriger Besuch vorhanden ist, wird 0 (null) zurückgegeben. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_PREVIOUS_VISIT_COUNT |
| Visitor Profile - Total Visits to Activity with Conversion | Gibt die Anzahl der Besuche/Sitzungen bis zu einer bestimmten Aktivität an, wenn mindestens eine Konversion während des Besuchs stattgefunden hat. | Double | SES_CUMULATIVE_SUCCESSES |
| Visitor Profile - Visits to Activity with No Conversion | Anzahl der Besuche/Sitzungen ohne Konversionen bis zu einer bestimmten Aktivität. Dieser Wert wird nach einer Konversion auf null zurückgesetzt oder -1, wenn nie eine Konversion erfolgte. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_SUCCESS_RECENCY |
