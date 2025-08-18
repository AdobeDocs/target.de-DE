---
keywords: Umgebungsdaten; Sitzungsdaten; Geodaten; geografische Daten; Gerätedaten; mobile Daten; Attribute; Profilattribute; Personalisierungsalgorithmen; Algorithmen für maschinelles Lernen; Algorithmen für maschinelles Lernen
description: Erfahren Sie [!DNL Adobe Target]  welche Daten erfasst und verwendet werden, um ihre Algorithmen für maschinelles Lernen zu erstellen.
title: Welche Daten werden erfasst, um Algorithmen für maschinelles Lernen zu erstellen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: fe6a7addd3854c430798fc339741c9ae6a4efc7d
workflow-type: tm+mt
source-wordcount: '1958'
ht-degree: 51%

---

# Von [!DNL Target] Algorithmen für maschinelles Lernen verwendete Daten

[!DNL Adobe Target] erfasst und verwendet automatisch verschiedene Daten, um seine Personalisierungsalgorithmen in [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Auto-Target] (AT)-Aktivitäten zu erstellen. Wenn ein Besucher eine [!UICONTROL Automated Personalization]- oder [!UICONTROL Auto-Target]-Aktivität aufruft, wird eine Momentaufnahme der Informationen an einen Satz von „Trainingsdatensätzen“ (die Besucherdaten, aus denen die Personalisierungsalgorithmen lernen) übergeben.

Weitere Informationen zu den [!DNL Target] Personalisierungsalgorithmen finden Sie unter [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Standard-[!DNL Target]

In der folgenden Tabelle sind die Daten aufgeführt, die standardmäßig von [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target]-Aktivitäten erfasst werden, ohne dass eine Konfiguration von [!DNL Target] oder anderen [!DNL Adobe] erforderlich ist. Die Tabelle enthält auch die Namenskonvention, mit der diese Attribute in [Personalization Insights-Berichten](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) angegeben werden. Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen zum Hochladen zusätzlicher Daten finden Sie unter [Hochladen von Daten für die  [!DNL Target] Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Datenkategorie | Systempräfix | Beschreibung | Anzeigename in [!UICONTROL Insights] Berichten |
| --- | --- | --- | --- |
| Umgebungsparameter | UMSCHLIESSEN | Informationen über die Umgebung eines Benutzers, einschließlich Betriebssystem, Browser und Tageszeit/Wochentag. | Browser - [Attributname]<br>Betriebssystem - [Wert] |
| Geografie | GEO | Informationen über die Geografie eines Benutzers, die über die IP-Suche abgerufen werden. | Geo - [geo-Attribut] |
| Mobilgerät | PÖBEL | Informationen zum Mobilgerät eines Benutzers. | Gerät - [Geräteattribut]<br>Mobil - [mobiles Attribut] |
| Berichterstellungssegmente [!DNL Target] | SEG | In [!DNL Target] Reporting konfigurierte Berichterstellungssegmente. | Berichterstellungssegment - [Segmentname] |
| Sitzungsverhalten | SE | Informationen zum Benutzerverhalten, z. B. die Anzahl der aufgerufenen Seiten. | Besucherprofil - [Attributname] |

## Benutzerdefinierte [!DNL Target]

Die folgende Tabelle zeigt die vom Kunden bereitgestellten Daten, die von [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target]-Aktivitäten erfasst wurden. Diese Daten werden nur erfasst, wenn Sie sie bereitstellen. Bestimmte Attributnamen und Beispielwerte sind für Ihre Systemkonfiguration spezifisch.

| Datenkategorie | Systempräfix | Beschreibung | Anzeigename in [!UICONTROL Insights] Berichten |
| --- | --- | --- | --- |
| Seitenparameter | KASTEN | Benutzerdefinierte Seitenparameter („mbox-Parameter„), die beim Aufruf von [!DNL Target] übergeben werden. | Benutzerdefiniert - Mbox-Parameter - [Parametername] |
| Profil [!DNL Target] | PRO | Benutzerdefinierte Profilattribute werden direkt über die API oder Seitenparameter und [!DNL Target] Profilskripte in das [!DNL Target]-Profil hochgeladen. | Benutzerdefiniert - Besucherprofil - [Attributname] |
| Kundenattribute | CRS | Kundenattribute, die über die [!DNL Target][[!DNL Adobe Experience Cloud Customer Attributes Service] in das ](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html?lang=de){target=_blank} hochgeladen wurden. | Benutzerdefiniert - Besucherprofil - [Attributname] |
| URL-Parameter | URL | URL und alle URL-Parameter der aktuell angezeigten Seite. | Benutzerdefiniert - URL-Parameter [URL-Parameter] |
| Verweisende URL | REF | Verweisende URL und alle URL-Parameter für die verweisende URL. | Benutzerdefiniert - [Verweisender URL-Parameter] - [Parameterwert] |
| Freigegebene Zielgruppen [!DNL Adobe Experience Cloud] | AAM | Alle Zielgruppen, die für [!DNL Target] aus anderen [!DNL Adobe Experience Cloud]-Lösungen freigegeben wurden (z. B. [!DNL Adobe Audience Manager] und [!DNL Adobe Analytics] über die [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=de){target=_blank}). | Benutzerdefiniert - Experience Cloud-Zielgruppe - [Zielgruppenname] |
| Zielgruppen [!DNL Adobe Experience Platform Real-time CDP] | USV | Platform Real-Time CDP-Zielgruppen, die über [!DNL Target] für [!UICONTROL Destinations] freigegeben wurden. |  |


## Sperren von Funktionen [!DNL Target] Algorithmen für maschinelles Lernen

Funktionen können für [!DNL Target] Algorithmen des maschinellen Lernens gesperrt werden, sodass sie in keinem [!UICONTROL Automated Personalization] oder [!UICONTROL Auto-Target] Modell oder keiner Aktivität verwendet werden können.

Auf die Blockierungsliste setzen Weitere Informationen finden Sie unter [Übersicht über die Models-API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html?lang=de){target=_blank} im *[!DNL Adobe Target]-Entwicklerhandbuch*.

## Geräte- und Mobilgerätedaten {#device-mobile}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Mobile - Device - Brand | Die Marke des Mobilgeräts, mit der der Besucher auf die Aktivität zugegriffen hat. | Apple | MOB_targeting.mobile.vender |
| Mobile - Device - eReader | Gibt an, ob es sich bei dem Gerät um einen E-Book-Reader handelt. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.reader |
| Mobile - Device - Game Console | Gibt an, ob das Gerät eine Spielkonsole ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.gamesConsole |
| Mobile - Device - Media Player | Gibt an, ob das Gerät ein Media Player ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.mediaPlayer |
| Mobile - Device - Mobile Phone | Gibt an, ob das Gerät ein Mobiltelefon ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.mobilePhone |
| Mobile - Device - Model Name | Der Modellname des Mobilgeräts, mit dem der Besucher auf die Aktivität zugegriffen hat. | iPhone XS | MOB_targeting.mobile.model |
| Device - Set-Top Box | Gibt an, ob das Gerät eine Set-Top-Box ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.setTopBox |
| Mobile - Device - Tablet | Gibt an, ob das Gerät ein Tablet ist. | 0 ist „false“, 1 ist „true“ | MOB_targeting.mobile.Tablet |
| Mobile - Pixel Density (ppi) | Die Pixeldichte des Mobilgeräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayPPI |
| Mobil - Betriebssystem - OS X ([!DNL Android], [!DNL Windows] usw.) | Gibt an, ob der Benutzer ein OSX-Gerät (oder [!DNL Android], [!DNL Windows] usw.) verwendet hat, um auf die Aktivität zuzugreifen. | 0 ist „false“, 1 ist „true“ | MOB_Targeting.mobile.os[OS]<br>Beispiel: MOB_Targeting.mobile.osX, MOB_Targeting.mobile.osWindows, MOB_Targeting.mobile.osAndroid, MOB_Targeting.mobile.osLinux |
| Mobile - Screen Height (px) | Die Bildschirmhöhe des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayHeight |
| Mobile - Screen Width (px) | Die Bildschirmbreite des Mobilgeräts (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | MOB_targeting.mobile.displayWidth |

## Umweltdaten {#env}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | -- |
| Browser - Day of Week | Der Tag der Woche, an dem der Besucher auf die Aktivität zugegriffen hat. | 0 - 6.<br>(0 ist Sonntag) | ENV_DayOfWeek |
| Browser - Hour of Day | Die Stunde des Tages, in der der Besucher auf die Aktivität zugegriffen hat. | 0 - 23<br>(0 ist Mitternacht) | ENV_UserHour |
| Browser - Hour of Week | Die Stunde der Woche, in der der Besucher auf die Aktivität zugegriffen hat. | 0 - 168<br>(Sonntagmitternacht ist 0) | ENV_WeekHour |
| Browser - Language Setting | Die im Browser des Besuchers festgelegte Sprache, mit der der Zugriff auf die Aktivität erfolgt. | English<br>German | ENV_Language |
| Browser - Time of Day | Die Uhrzeit des Browsers, zu der der Besucher auf die Aktivität zugegriffen hat. | 0, 6, 12, 18<br>(0 ist Nacht, 6 ist Morgen,<br>12 ist Nachmittag, 18 ist Abend) | ENV_LocalTimePeriod |
| Browser - Timezone | Die Zeitzone, in der der Besucher auf die Aktivität zugegriffen hat. | Pacific Time<br>Eastern Time<br>GMT | ENV_BrowserTimezoneOffsetMinutes |
| Browser - Type | Der Typ des Browsers, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | [!DNL Chrome]<br>[!DNL Firefox]<br>[!DNL Internet Explorer]<br>[!DNL Safari]<br>Sonstige | ENV_BROWSER |
| Browser - Weekday/Weekend | Der Werktagsstatus, unter dem der Besucher auf die Aktivität zugegriffen hat (Wochenende, Arbeitsstunden oder Wochentags-Freizeit). | Samstag und Sonntag sind Wochenende<br>Montag-Freitag 0900 - 1800 ist Arbeitszeit<br>Montag-Freitag nach 1800 bis 0900 ist Wochentag Freizeit | ENV_UserHourType |
| Browser - Window Height (px) | Die Fensterhöhe des Browsers (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | ENV_BrowserHeight |
| Browser - Window Width (px) | Die Fensterbreite des Browsers (in Pixeln), mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | ENV_BrowserWidth |
| Gerät - Bildschirmhöhe (px) | Die Bildschirmhöhe des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | ENV_ScreenHeight |
| Gerät - Bildschirmbreite (px) | Die Bildschirmbreite des Geräts, mit der der Besucher auf die Aktivität zugegriffen hat. | 1, 2, 3 usw. | ENV_ScreenWidth |
| Betriebssystem | Das Betriebssystem auf dem Gerät des Besuchers, das für den Zugriff auf die Aktivität verwendet wurde. | [!DNL Mac OS]<br>[!DNL Windows]<br>[!DNL Linux]<br>Bot suchen<br>unbekanntes Betriebssystem | ENV_OperatingSystem |
| Operating System - Version | Die Version des Betriebssystems, mit der der Besucher auf die Aktivität zugegriffen hat. | [!DNL Windows] 10<br>[!DNL Mac OS] 10 | ENV_OperatingSystemVersion |
| Traffic Sources - Referring Landing Page URL | Die erste Seite, die der Besucher beim Zugriff auf Ihre Site gesehen hat. | `https://www.adobe.com/ecloud.html` | ENV_REFERRER |

## Geografische Daten {#geo}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Geo - City | Die Stadt, von der aus der Besucher auf die Aktivität zugegriffen hat. | San Francisco | Geo_City |
| Geo - Country | Das Land, von dem aus der Besucher auf die Aktivität zugegriffen hat. | Deutschland | Geo_Land |
| Geo - DMA | Der angegebene Marketingbereich (DMA), von dem aus der Besucher auf die Aktivität zugegriffen hat. | Charlottesville | Geo_DMA |
| Geo - Latitude | Der Breitengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 47.269<br>Auf 3 Dezimalstellen gerundet (ca. 100 Meter Genauigkeit) | GEO_LATITUDE |
| Geo - Longitude | Der Längengrad, von dem aus der Besucher auf die Aktivität zugegriffen hat. | -122.269<br>gerundet auf 3 Dezimalstellen (ca. 100 Meter Genauigkeit) | GEO_Longitude |
| Geo - State/Region | Der Bundesstaat oder die Region, von der aus der Besucher auf die Aktivität zugegriffen hat. | Utah<br>New South Wales | GEO_state<br>GEO_region |
| Geo - Zip Code | Die Postleitzahl, von dem aus der Besucher auf die Aktivität zugegriffen hat. | 84004 | GEO_ZipCode |
| Mobile - Carrier | Der Mobilnetzbetreiber, den der Besucher beim Zugriff auf die Aktivität verwendet hat. | [!DNL Vodafone]<br>[!DNL T-Mobile] | GEO_mobileCarrier |
| Network - Connection Speed | Die Netzwerkverbindungsgeschwindigkeit des Geräts, als der Besucher auf die Aktivität zugegriffen hat. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite | GEO_ConnectionSpeed |
| Network - Domain Name | Der Name der Netzwerkdomäne, von der aus der Besucher auf die Aktivität zugegriffen hat. | `nnt.net` | GEO_DomainName |
| Network - ISP | Das Netzwerk, von dem aus der Besucher auf die Aktivität zugegriffen hat. | nnt communications corporation | GEO_ISPname |

## Sitzungsdaten {#session}

| Attributname | Attributbeschreibung | Beispielwerte | Systemname |
| --- | --- | --- | --- |
| Visitor Profile - Activity Lifetime Order Value | Gibt die Summe aller Bestellwerte für alle Besuche/Sitzungen einer bestimmten Aktivität an. | Doppelt | SES_CUMULATIVE_ORDER_VALUE |
| Visitor Profile - Activity Lifetime Time on Site | Gibt die Gesamtbesuchszeit des Besuchers an, wobei die aktuelle Sitzung ausgeschlossen ist. Sie wird aktualisiert, wenn die Sitzung abgelaufen ist. | Doppelt, Millisekunden | SES_TOTAL_TIME |
| Visitor Profile -Average Page Views per Visit during Activity | Gibt die durchschnittliche Anzahl der Seitenansichten pro Sitzung an, wobei die aktuelle Sitzung ausgeschlossen ist. | Doppelt | SES_REQUESTS_PER_SESSION |
| Visitor Profile - Average Time per Visit | Gibt die durchschnittliche Zeit pro Besuch/Sitzung an. Die aktuelle Sitzung ist ausgeschlossen. | Doppelt, Millisekunden | SES_TIME_PER_SESSION |
| Visitor Profile - First Visit | Gibt die Zeit des ersten Besuchs an, bei dem Benutzende mit [!DNL Target] interagiert haben. | Doppelt, Millisekunden | SES_PROFILE_CREATION_TIME |
| Visitor Profile - Hours since Last Visit | Gibt die Stunden seit dem letzten Besuch einer bestimmten Aktivität an. | Double (nur ganzzahlige positive Zahl) 1, 2, 3 usw. | SES_HOURS_SINCE_LAST_VISIT |
| Visitor Profile - Impressions of Location/Content | Gibt die Anzahl der Impressionen bei einer bestimmten Kombination aus Ort/Inhalt bei einer bestimmten Aktivität an. | Double (nur ganzzahlige positive Zahl) 1, 2, 3 usw. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| Besucherprofil - letzte [!DNL Target] Interaktion | Gibt den Zeitpunkt der letzten Interaktion mit [!DNL Target] an. Interaktion erfolgt bei jeder [!DNL Target]-Anfrage, da die aktuelle Implementierung von [!DNL Target] das Profil bei jeder Anfrage aktualisiert. | Doppelt, Millisekunden | SES_PROFILE_UPDATE_TIME |
| Visitor Profile - Pages Seen Before Activity | Gibt die Anzahl der gesamten Seitenansichten (Impressionen) an, einschließlich des aktuellen Besuchs/der aktuellen Sitzung, bis der Besucher in die Aktivität eintritt. | Double (nur ganzzahlige positive Zahl) 1, 2, 3 usw. | SES_TOTAL_PAGE_VIEWS |
| Visitor Profile - Page Views in Current Visit | Gibt die Anzahl der Seitenansichten während des aktuellen Besuchs/der aktuellen Sitzung an, bis der Besucher in die Aktivität eintritt. Genauer gesagt, die Anzahl der Impressionen. Bei diesen Impressions handelt es sich nicht um echte Seitenansichten, sondern um die Häufigkeit, mit der die Anfrage [!DNL Target] erreicht wurde. [!DNL Target] kann keine Zeitüberschreitungen oder andere Gründe unterscheiden, aus denen der Benutzer den Inhalt nicht erhalten oder angezeigt hat. | Doppelt (nur positive Ganzzahl) | SES_SESSION_POSITION |
| Visitor Profile - Start of Current Visit | Gibt den Zeitpunkt an, zu dem der aktuelle Besuch/die aktuelle Sitzung mit [!DNL Target] gestartet wird. Der Besuch mit [!DNL Target] kann ohne Eingabe einer Aktivität gestartet werden. Es ist lediglich ein Aufruf einer [!DNL Target]-Anfrage erforderlich. Es kann eine Weile dauern, bis der Besucher die Aktivität aufruft und der Schnappschuss erstellt wird. | Doppelt, Millisekunden | SES_SESSION_START |
| Visitor Profile - Start of Most Recent Visit | Gibt den Zeitpunkt an, zu dem der letzte Besuch/die letzte Sitzung mit [!DNL Target] gestartet wurde. Dieses Attribut wird aktualisiert, wenn die Sitzung abgelaufen ist.<br>Wenn dies die erste Sitzung für den Besucher ist, führt dies zu `LAST_SESSION_START = 0.` | Doppelt, Millisekunden | SES_LAST_SESSION_START |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Gibt die Dauer zwischen der vorherigen Sitzung und dem Zeitpunkt an, zu dem der Benutzer die Aktivität aufruft und die Momentaufnahme aufgenommen wird. | Doppelt, Millisekunden | SES_RECENCY |
| Visitor Profile - Time in Visit Before Enter Activity | Gibt die Differenz zwischen der letzten Interaktion mit [!DNL Target] und dem Beginn des aktuellen Besuchs an. Dieses Attribut kann als Besuchs-/Sitzungsdauer betrachtet werden, bis der Benutzer die Aktivität aufruft und die Momentaufnahme erfolgt.<br>Negative Werte treten auf, wenn der Sitzungsstart und die letzte Aktualisierungszeit durch denselben [!DNL Target] ausgelöst werden. Negative Werte sollten als 0 (Null) betrachtet werden. | Doppelt, Millisekunden | SES_SESSION_TIME |
| Besucherprofil – Gesamtbesuche | Gibt die Gesamtzahl der Besuche/Sitzungen an. Der aktuelle Besuch/die aktuelle Sitzung ist ausgeschlossen. | Double (nur ganzzahlige positive Zahl) 1, 2, 3 usw. | SES_TOTAL_SESSIONS |
| Visitor Profile - Total Visits to Activity | Gibt die Anzahl der Besuche bis zu einer bestimmten Aktivität an. Wenn kein vorheriger Besuch vorhanden ist, wird 0 (null) zurückgegeben. | Double (nur ganzzahlige positive Zahl) 1, 2, 3 usw. | SES_PREVIOUS_VISIT_COUNT |
| Visitor Profile - Total Visits to Activity with Conversion | Gibt die Anzahl der Besuche/Sitzungen bis zu einer bestimmten Aktivität an, wenn mindestens eine Konversion während des Besuchs stattgefunden hat. | Double | SES_CUMULATIVE_SUCCESSES |
| Visitor Profile - Visits to Activity with No Conversion | Anzahl der Besuche/Sitzungen ohne Konversionen bis zu einer bestimmten Aktivität. Dieser Wert wird nach einer Konversion auf null zurückgesetzt oder -1, wenn nie eine Konversion erfolgte. | Double (nur ganzzahlige positive Zahl) 1, 2, 3 usw. | SES_SUCCESS_RECENCY |
