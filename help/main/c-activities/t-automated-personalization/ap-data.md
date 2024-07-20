---
keywords: Umgebungsdaten; Sitzungsdaten; Geodaten; geografische Daten; Gerätedaten; mobile Daten; Attribute; Profilattribute; Personalisierungsalgorithmen; Algorithmen für maschinelles Lernen; Algorithmen für maschinelles Lernen
description: Erfahren Sie, welche Daten [!DNL Adobe Target] erfasst und verwendet, um die Algorithmen für maschinelles Lernen zu erstellen.
title: Welche Daten werden erfasst, um Algorithmen für maschinelles Lernen zu erstellen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 51%

---

# Von [!DNL Target]-Algorithmen für maschinelles Lernen verwendete Daten

[!DNL Adobe Target] sammelt und verwendet automatisch verschiedene Daten, um seine Personalisierungsalgorithmen in den Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] (AT) zu erstellen. Wenn ein Besucher eine [!UICONTROL Automated Personalization] - oder [!UICONTROL Auto-Target] -Aktivität aufruft, wird eine Momentaufnahme mit Informationen an eine Reihe von &quot;Trainings-Datensätzen&quot;übergeben (die Besucherdaten, über die die Personalisierungsalgorithmen lernen).

Weitere Informationen zu den [!DNL Target] Personalisierungsalgorithmen finden Sie unter [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Standard-Attributkategorien [!DNL Target]

Die folgende Tabelle zeigt die Daten, die von den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] standardmäßig ohne Konfiguration von [!DNL Target] oder anderen [!DNL Adobe] -Lösungen erfasst werden. Die Tabelle enthält auch die Namenskonvention, die zur Anzeige dieser Attribute in [Personalization Insights Reports](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) verwendet wird. Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen zum Hochladen zusätzlicher Daten finden Sie unter [Hochladen von Daten für die [!DNL Target] Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Datenkategorie | Systempräfix | Beschreibung | Anzeigename in [!UICONTROL Insights] Berichten |
| --- | --- | --- | --- |
| Umgebungsparameter | ENV | Informationen zur Umgebung eines Benutzers, einschließlich Betriebssystem, Browser und Tageszeit/Wochentag. | Browser - [Attributname]<br>Betriebssystem - [Wert] |
| Geografie | GEO | Informationen zur geografischen Lage eines Benutzers, abgerufen über IP-Suche. | Geo - [geo attribute] |
| Mobilgerät | MOB | Informationen zum Mobilgerät eines Benutzers. | Device - [device attribute]<br>Mobile - [mobile attribute] |
| [!DNL Target] Berichtssegmente | SEG | Berichtssegmente, die in der [!DNL Target] -Berichterstellung konfiguriert wurden. | Berichtssegment -[Segmentname] |
| Sitzungsverhalten | SES | Informationen zum Benutzerverhalten, z. B. die Anzahl der angezeigten Seiten. | Besucherprofil - [Attributname] |

## Benutzerdefinierte [!DNL Target] Attributkategorien

Die folgende Tabelle zeigt die vom Kunden bereitgestellten Daten, die von den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] erfasst werden. Diese Daten werden nur erfasst, wenn Sie sie bereitstellen. Spezifische Attributnamen und Beispielwerte beziehen sich speziell auf Ihre Systemkonfiguration.

| Datenkategorie | Systempräfix | Beschreibung | Anzeigename in [!UICONTROL Insights] Berichten |
| --- | --- | --- | --- |
| Seitenparameter | BOX | Benutzerdefinierte Seitenparameter (&quot;mbox-Parameter&quot;), die beim Aufruf an [!DNL Target] übergeben werden. | Benutzerspezifisch - Mbox-Parameter - [Parametername] |
| [!DNL Target] profile | PRO | Benutzerdefinierte Profilattribute werden direkt über API- oder Seitenparameter sowie [!DNL Target] Profilskripte in das Profil [!DNL Target] hochgeladen. | Benutzerspezifisch - Besucherprofil - [Attributname] |
| Kundenattribute | CRS | Kundenattribute, die über das Profil [[!DNL Adobe Experience Cloud Customer Attributes Service]](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html){target=_blank} in das Profil [!DNL Target] hochgeladen wurden. | Benutzerspezifisch - Besucherprofil - [Attributname] |
| URL-Parameter | URL | URL und alle URL-Parameter für die aktuell angezeigte Seite. | Benutzerspezifisch - URL-Parameter - [URL-Parameter] |
| Verweisende URL | REF | Verweisende URL und alle URL-Parameter für die verweisende URL. | Benutzerspezifisch - [Verweisender URL-Parameter] - [Parameterwert] |
| [!DNL Adobe Experience Cloud] freigegebene Zielgruppen | AAM | Alle Zielgruppen, die für [!DNL Target] aus anderen [!DNL Adobe Experience Cloud] -Lösungen freigegeben wurden (z. B. [!DNL Adobe Audience Manager] und [!DNL Adobe Analytics] über die [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html){target=_blank}). | Benutzerspezifisch - Experience Cloud-Zielgruppe - [Zielgruppenname] |
| [!DNL Adobe Experience Platform Real-time CDP] Zielgruppen | UPS | Echtzeit-CDP-Zielgruppen der Plattform, die für [!DNL Target] über [!UICONTROL Destinations] freigegeben wurden. |  |
| [!DNL Adobe Experience Platform Real-time CDP] Attribute | AEP | Echtzeit-CDP-Attribute der Plattform, die mit [!DNL Target] über [!UICONTROL Destinations] freigegeben werden. |  |

## Sperren von Funktionen aus [!DNL Target] Algorithmen für maschinelles Lernen

Funktionen können von den Algorithmen für das maschinelle Lernen mit dem Wert [!DNL Target] blockiert werden, was verhindert, dass sie in einem beliebigen Modell oder einer Aktivität mit dem Wert [!UICONTROL Automated Personalization] oder [!UICONTROL Auto-Target] verwendet werden.

Weitere Informationen finden Sie unter [Übersicht über die Modell-API (Auf die Blockierungsliste setz)](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} im *[!DNL Adobe Target]Entwicklerhandbuch*.

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
| Mobile - OS - OS X ([!DNL Android], [!DNL Windows] usw.) | Gibt an, ob der Benutzer ein OSX-Gerät (oder [!DNL Android], [!DNL Windows] usw.) verwendet hat, um auf die Aktivität zuzugreifen. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.os[OS]<br>Beispiel: MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux |
| Mobile - Screen Height (px) | Die Bildschirmhöhe des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayHeight |
| Mobile - Screen Width (px) | Die Bildschirmbreite des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayWidth |

## Umgebungsdaten {#env}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | -- |
| Browser - Day of Week | Der Tag der Woche, an dem der Besucher auf die Aktivität zugegriffen hat. | 0-6.<br>(0 ist Sonntag) | ENV_DayOfWeek |
| Browser - Hour of Day | Die Stunde des Tages, in der der Besucher auf die Aktivität zugegriffen hat. | 0 - 23<br>(0 ist Mitternacht) | ENV_UserHour |
| Browser - Hour of Week | Die Stunde der Woche, in der der Besucher auf die Aktivität zugegriffen hat. | 0 - 168<br>(Sonntag Mitternacht ist 0) | ENV_WeekHour |
| Browser - Language Setting | Die im Browser des Besuchers festgelegte Sprache, mit der der Zugriff auf die Aktivität erfolgt. | English<br>German | ENV_Language |
| Browser - Time of Day | Die Uhrzeit des Browsers, zu der der Besucher auf die Aktivität zugegriffen hat. | 0, 6, 12, 18<br>(0 ist Nacht, 6 ist Morgen,<br>12 ist Nachmittag, 18 ist Abend) | ENV_LocalTimePeriod |
| Browser - Timezone | Die Zeitzone, in der der Besucher auf die Aktivität zugegriffen hat. | Pacific Time<br>Eastern Time<br>GMT | ENV_BrowserTimezoneOffsetMinutes |
| Browser - Type | Der Typ des Browsers, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | [!DNL Chrome]<br>[!DNL Firefox]<br>[!DNL Internet Explorer]<br>[!DNL Safari]<br>Sonstige | ENV_Browser |
| Browser - Weekday/Weekend | Der Werktagsstatus, unter dem der Besucher auf die Aktivität zugegriffen hat (Wochenende, Arbeitsstunden oder Wochentags-Freizeit). | Samstag und Sonntag sind Wochenende<br>Montag bis Freitag 0900 - 1800 ist Arbeitszeit<br>Montag bis Freitag nach 1800 bis 0900 ist Wochentags-Freizeit | ENV_UserHourType |
| Browser - Window Height (px) | Die Fensterhöhe des Browsers (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw., | ENV_BrowserHeight |
| Browser - Window Width (px) | Die Fensterbreite des Browsers (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw., | ENV_BrowserWidth |
| Gerät - Bildschirmhöhe (px) | Die Bildschirmhöhe des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw., | ENV_ScreenHeight |
| Gerät - Bildschirmbreite (px) | Die Bildschirmbreite des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw., | ENV_ScreenWidth |
| Betriebssystem | Das Betriebssystem auf dem Gerät des Besuchers, das für den Zugriff auf die Aktivität verwendet wurde. | [!DNL Mac OS]<br>[!DNL Windows]<br>[!DNL Linux]<br>Search Bot<br>Unknown OS | ENV_OperatingSystem |
| Operating System - Version | Die Version des Betriebssystems, mit der der Besucher auf die Aktivität zugegriffen hat. | [!DNL Windows] 10<br>[!DNL Mac OS] 10 | ENV_OperatingSystemVersion |
| Traffic Sources - Referring Landing Page URL | Die erste Seite, die der Besucher beim Zugriff auf Ihre Site gesehen hat. | `https://www.adobe.com/ecloud.html` | ENV_Referrer |

## Geografische Daten {#geo}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Geo - City | Die Stadt, von der aus der Besucher auf die Aktivität zugegriffen hat. | San Francisco | geo_city |
| Geo - Country | Das Land, von dem aus der Besucher auf die Aktivität zugegriffen hat. | Deutschland | geo_country |
| Geo - DMA | Der angegebene Marketingbereich (DMA), von dem aus der Besucher auf die Aktivität zugegriffen hat. | Charlottesville | Geo_DMA |
| Geo - Latitude | Der Breitengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 47.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) | GEO_Latitude |
| Geo - Longitude | Der Längengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | -122.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) | GEO_Length |
| Geo - State/Region | Der Bundesstaat oder die Region, von der aus der Besucher auf die Aktivität zugegriffen hat. | Utah<br>New South Wales | GEO_State<br>GEO_Region |
| Geo - Zip Code | Die Postleitzahl, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 84004 | GEO_ZipCode |
| Mobile - Carrier | Der Mobilnetzbetreiber, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | [!DNL Vodafone]<br>[!DNL T-Mobile] | GEO_mobileCarrier |
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
| Visitor Profile - First Visit | Gibt den Zeitpunkt des ersten Besuchs an, bei dem der Benutzer mit [!DNL Target] interagiert hat. | Doppelt, Millisekunden | SES_PROFILE_CREATION_TIME |
| Visitor Profile - Hours since Last Visit | Gibt die Stunden seit dem letzten Besuch einer bestimmten Aktivität an. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_HOURS_SINCE_LAST_VISIT |
| Visitor Profile - Impressions of Location/Content | Gibt die Anzahl der Impressionen bei einer bestimmten Kombination aus Ort/Inhalt bei einer bestimmten Aktivität an. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| Besucherprofil - Letzte [!DNL Target] Interaktion | Gibt den Zeitpunkt der letzten Interaktion mit [!DNL Target] an. Interaktion erfolgt bei jeder [!DNL Target] -Anfrage, da die aktuelle Implementierung von [!DNL Target] das Profil bei jeder Anfrage aktualisiert. | Doppelt, Millisekunden | SES_PROFILE_UPDATE_TIME |
| Visitor Profile - Pages Seen Before Activity | Gibt die Anzahl der Seitenansichten (Impressionen) insgesamt an, einschließlich des aktuellen Besuchs/der aktuellen Sitzung, bis der Besucher die Aktivität aufruft. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_TOTAL_PAGE_VIEWS |
| Visitor Profile - Page Views in Current Visit | Gibt die Anzahl der Seitenansichten im aktuellen Besuch/in der aktuellen Sitzung an, bis der Besucher die Aktivität aufruft. Genauer gesagt, die Anzahl der Impressionen. Diese Impressionen sind keine echten Seitenansichten, sondern geben an, wie oft die Anfrage [!DNL Target] erreicht hat. [!DNL Target] kann nicht zwischen Timeouts oder anderen Gründen unterscheiden, aus denen der Benutzer den Inhalt nicht erhalten oder anzeigen konnte. | Doppelt (nur positive Ganzzahl) | SES_SESSION_POSITION |
| Visitor Profile - Start of Current Visit | Gibt den Zeitpunkt an, zu dem der aktuelle Besuch/die aktuelle Sitzung mit [!DNL Target] gestartet wurde. Der Besuch mit [!DNL Target] kann ohne Eingabe einer Aktivität eingeleitet werden. Erforderlich ist lediglich ein Aufruf einer [!DNL Target] -Anfrage. Es kann einige Zeit dauern, bis ein Besucher die Aktivität aufruft und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden | SES_SESSION_START |
| Visitor Profile - Start of Most Recent Visit | Gibt den Zeitpunkt an, zu dem der letzte Besuch/die letzte Sitzung mit [!DNL Target] gestartet wurde. Dieses Attribut wird aktualisiert, wenn die Sitzung abgelaufen ist.<br>Wenn dies die erste Sitzung für den Besucher ist, ergibt dies `LAST_SESSION_START = 0.` | Doppelt, Millisekunden | SES_LAST_SESSION_START |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Gibt die Dauer zwischen der vorherigen Sitzung und dem Zeitpunkt an, zu dem der Benutzer die Aktivität aufruft und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden | SES_RECENCY |
| Visitor Profile - Time in Visit Before Enter Activity | Gibt den Unterschied zwischen der letzten Interaktion mit [!DNL Target] und dem Beginn des aktuellen Besuchs an. Dieses Attribut kann als Besuchs-/Sitzungsdauer betrachtet werden, bis der Benutzer die Aktivität aufruft und die Momentaufnahme erfolgt.<br>Negative Werte treten auf, wenn die Sitzung beginnt und die letzte Aktualisierungszeit durch denselben [!DNL Target] -Aufruf ausgelöst wird. Negative Werte sollten als 0 (Null) betrachtet werden. | Doppelt, Millisekunden | SES_SESSION_TIME |
| Besucherprofil – Gesamtbesuche | Gibt die Gesamtzahl der Besuche/Sitzungen an. Der aktuelle Besuch/die aktuelle Sitzung ist ausgeschlossen. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_TOTAL_SESSIONS |
| Visitor Profile - Total Visits to Activity | Gibt die Anzahl der Besuche bis zu einer bestimmten Aktivität an. Wenn kein vorheriger Besuch vorhanden ist, wird 0 (null) zurückgegeben. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_PREVIOUS_VISIT_COUNT |
| Visitor Profile - Total Visits to Activity with Conversion | Gibt die Anzahl der Besuche/Sitzungen bis zu einer bestimmten Aktivität an, wenn mindestens eine Konversion während des Besuchs stattgefunden hat. | Double | SES_CUMULATIVE_SUCCESSES |
| Visitor Profile - Visits to Activity with No Conversion | Anzahl der Besuche/Sitzungen ohne Konversionen bis zu einer bestimmten Aktivität. Dieser Wert wird nach einer Konversion auf null zurückgesetzt oder -1, wenn nie eine Konversion erfolgte. | Doppelt (nur positive Ganzzahl) 1, 2, 3 usw. | SES_SUCCESS_RECENCY |
