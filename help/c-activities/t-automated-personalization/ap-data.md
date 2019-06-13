---
description: Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
seo-description: Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.
seo-title: Datenerfassung für die Target-Personalisierungsalgorithmen
solution: Target
title: Datenerfassung für die Target-Personalisierungsalgorithmen
title-outputclass: Premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: Premium
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Datenerfassung für die Target-Personalisierungsalgorithmen{#data-collection-for-the-target-personalization-algorithms}

Target sammelt und verwendet automatisch eine Vielzahl an Daten zum Erstellen seiner Personalisierungsalgorithmen in den Aktivitäten „Automatisierte Personalisierung“ (AP) und „Automatisches Targeting“ (AT). Wenn ein Besucher die AP- oder AT-Aktivität aktiviert, wird eine Momentaufnahme an Informationen an einen Satz von Trainingsdatensätzen (die Besucherdaten, anhand deren die Personalisierungsalgorithmen lernen) weitergegeben.

Weitere Informationen über die Target-Personalisierungsalgorithmen finden Sie unter [Random-Forest-Algorithmus](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

Folgende Tabelle zeigt die Daten, die von der automatisierten Personalisierung standardmäßig erfasst werden, ohne dass der Marketing-Experte hierfür eine Aktion durchführen muss, sowie die Namenskonvention, die zur Anzeige dieser Attribute in [Berichten zu Personalization Insights](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) verwendet wird. Sie können den Eingabedatensatz jederzeit erweitern. Weitere Informationen über das Hochladen zusätzlicher Daten finden Sie unter [Hochladen von Daten für die Personalisierungsalgorithmen von Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Datentyp | Beschreibung | Datentyp-Namenskonvention | Beispielattribute |
|--- |--- |--- |--- |
| URL-Parameter | Target untersucht die URL, um die URL-Parameter zu extrahieren. | `Custom - URL Parameter - [URL Parameter]` | Benutzerspezifische Daten |
| Verweisende URL-Parameter | Im Allgemeinen entspricht die verweisende URL der URL, die auf eine bestimmte Seite verweist, die den Mbox-Aufruf initiiert hat.<br>Beachten Sie, dass sich die Aktivität der Benutzer auf Ihrer Site und die technische Implementierung Ihrer Site auf diese Variable auswirken kann. | `Custom - [Referring URL Parameter] - [Parameter value]` | Benutzerspezifische Daten |
| Umgebungs- und Sitzungsdaten | Informationen darüber, wie und wann der Benutzer auf die Aktivität zugreift. | `Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]` | Besucherprofil – Beginn des letzten Besuchs<br>Besucherprofil – Gesamtbesuche<br>Besucherprofil – Durchschnittl. Zeit pro Besuch<br>Browser – Zeitzone<br>Browser – Wochentag<br>Browser – Spracheinstellung<br>Browser – Typ<br>Betriebssystem – Version |
| Geografie | Informationen zum Standort des Besuchers. | `Geo - [geo attribute]` | Stadt<br>Land<br>Region/Bundesstaat<br>Postleitzahl<br>Breitengrad<br>Längengrad<br>ISP oder Mobilnetzbetreiber |
| Gerät und Mobildaten | Gerät- und mobilspezifische Informationen. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Mobilgerät-Betriebssystem<br>Mobilgerät - Bildschirmgröße |

