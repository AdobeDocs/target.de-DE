---
keywords: änderungsprotokoll zur target-dokumentation;aktualisierungen in der dokumentation;neue themen;bearbeitungen;aktualisierungen;aktualisierung
description: Halten Sie sich über wichtige Ergänzungen und Änderungen in der Dokumentation von  [!DNL Adobe Target]  auf dem Laufenden.
title: Wo kann ich Aktualisierungen an der Dokumentation von  [!DNL Target] sehen?
feature: Release Notes
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
source-git-commit: e93747d07b980aa29a8985c3872fd704d520e0cd
workflow-type: tm+mt
source-wordcount: '1824'
ht-degree: 98%

---

# Dokumentationsänderungen

Auf dieser Seite sind wichtige Änderungen an der Produktdokumentation von [!DNL Adobe Target] zusammengefasst.

## [!DNL Adobe Target] Standard/Premium 22.10.1 (gestaffelte Veröffentlichung vom 10. bis 13. Oktober 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 21. Dezember | [Anpassen eines Designs mithilfe von Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md) | klargestellt, dass Entitätsattribute an [!DNL Recommendations] im `productPage` Mbox oder CSV-Upload können in einem Design angezeigt werden, mit Ausnahme von Attributen mit mehreren Werten. |
| 20. Dezember | [[!UICONTROL Berichtsgruppen für Angebote in Automated Personalization]](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md) | Es wurden zusätzliche Informationen zu Berichtsgruppen unter &quot;Einschränkungen&quot;hinzugefügt. |
| 14. Dezember | [Berichtseinstellungen](/help/main/c-reports/c-report-settings/report-settings.md#environment) | Es wurde ein Hinweis unter dem Abschnitt „Umgebung“ zur Verwendung von [!DNL Adobe Experience Platform] (AEP) zum Senden von Metrikdaten an [!DNL Target] hinzugefügt. |
| 29. November | [Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md) | Klarstellung des Texts durch Hinzufügen des folgenden Absatzes:<ul><li>Die Geoinformationen eines Besuchers werden anhand der Ursprungs-IP-Adresse einer [!DNL Target]-Standortanfrage (mBox-Anfrage) bestimmt. Die IP-zu-Geo-Auflösung erfolgt beim ersten Aufruf einer neuen Sitzung. Das bedeutet: Wenn sich die IP-Adresse eines Besuchers während einer Besuchssitzung ändert, basieren die Geoinformationen weiterhin auf der IP-Adresse des ersten Aufrufs.</li></ul> |
| 28. November | [Übersicht über die Models-API](https://developer.adobe.com/target/before-administer/models-api){target=_blank} im *Adobe Target-Entwicklerhandbuch*. | Neue Models-API.<br>Funktionen können für [!DNL Target]-Algorithmen des maschinellen Lernens gesperrt werden, sodass sie in keinerlei Modellen oder Aktivitäten für [!UICONTROL Automatisches Targeting] oder [!UICONTROL Automated Personalization] verwendet werden können. |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen über die Models-API-Version (23. November 2022) hinzugefügt. |
| 23. November | [Vor der Implementierung von Analytics for Target (A4T) mit at.js](/help/main/c-integrating-target-with-mac/a4t/before-implement.md) | Der Link zum [Bereitstellungsformular für Experience Cloud-Integrationen](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} wurde aktualisiert. |
| 16. November | [Adobe Target-Ankündigungen und -Veranstaltungen](/help/main/r-release-notes/target-announcements.md) | Informationen zur Registrierung für die folgende Veranstaltung wurden hinzugefügt:<ul><li>[!DNL Adobe Target] Community-Kaffeepause mit Fragen und Antworten (29. November)</li></ul> |
| 8. November | [Wie lange sollten A/B-Tests laufen?](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) | Es wurde ein wichtiger Hinweis hinzugefügt: Um genaue Ergebnisse zu erhalten, müssen Sie die Seite neu laden, bevor Sie Parameter im [!DNL Adobe Target] [!UICONTROL Rechner für den Stichprobenumfang] ändern. Es wurde auch ein Hinweis im tatsächlichen [Rechner](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=de){target=_blank} hinzugefügt. |
|  | [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682) | Die Beschreibung für den Parameter `adobe_mc_sdid` in der Tabelle wurde aktualisiert. |
|  | [Fehlerbehebung für Aktivitäten](/help/main/c-activities/c-troubleshooting-activities/troubleshooting-activities.md) | Es wurde der neue Abschnitt hinzugefügt: „Nach der Aktivitätskonversion befindet sich der Besucher in keinem Erlebnis.“ |
|  | [Benutzerdefinierte Parameter](/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md) | Es wurde ein Hinweis hinzugefügt: Die mbox, die Sie aus der Dropdown-Liste [!UICONTROL Filtern nach] auswählen, wird bei der Erstellung einer Aktivität nicht gespeichert. Mit dieser Option können Sie die Parameter je nach der ausgewählten mbox filtern. |
| 2. November | Bekannte Probleme und gelöste Probleme | Die Seite wurde entfernt, und relevante Probleme wurden auf die entsprechenden Seiten verschoben, sodass Informationen im Kontext angezeigt werden. |
| 25. Oktober | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Version 22.10.3 von [!DNL Target Standard/Premium] hinzugefügt. |
| 19. Oktober | [Kategorieaffinität](/help/main/c-target/c-visitor-profile/category-affinity.md#section_8B86C7FF50294208866ABF16F07D5EB9) | Es wurde ein Hinweis hinzugefügt, der die Bewertung erklärt, wenn mehrere Kategorien innerhalb eines einzelnen mbox-Aufrufs übergeben werden. |
| 18. Oktober | [Erstellen einer [!UICONTROL Automated Personalization]-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) | Der Text wurde aktualisiert, um darauf hinzuweisen, dass Sie zwar bis zu 30.000 Erlebnisse in einem AP-Test erstellen können, der Algorithmus aber am besten funktioniert, wenn weniger als 10.000 unterschiedliche Erlebnisse verwendet werden. Diese Beschränkung gilt selbst dann, wenn bei der Aktivität die Option [!UICONTROL Duplikate nicht anzeigen] aktiviert ist. |
|  | [Häufig gestellte Fragen zur Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization-faq.md) | Der Text wurde aktualisiert, um darauf hinzuweisen, dass Sie zwar bis zu 30.000 Erlebnisse in einem AP-Test erstellen können, der Algorithmus aber am besten funktioniert, wenn weniger als 10.000 unterschiedliche Erlebnisse verwendet werden. Diese Beschränkung gilt selbst dann, wenn bei der Aktivität die Option [!UICONTROL Duplikate nicht anzeigen] aktiviert ist. |
| 14. Oktober | [[!DNL Adobe Target] Ankündigungen und Veranstaltungen](/help/main/r-release-notes/target-announcements.md) | Registrierungsinformationen über die [!DNL Adobe Target]-Kaffeepause mit Fragen und Antworten der Community (26. Oktober 2022) wurden hinzugefügt. |
| 10. Oktober | [[!UICONTROL Visual Editing Helper]-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) | Neuer Artikel. |
|  | [Beheben von Problemen im Zusammenhang mit Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md) | Abschnitt „[Meine Seite wird im VEC nicht angezeigt (nur VEC)](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md#does-not-load)“ wurde aktualisiert. |
| 4. Oktober | [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) | Neues Thema<br>Die Informationen in diesem Artikel ersetzen die PDF-Datei mit den *Adobe Target-Berechnungen für A/B-Tests*, die zuvor auf dieser Website zum Download verfügbar war. |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Version 22.10.1 von [!DNL Target Standard/Premium] hinzugefügt. |

## [!DNL Adobe Target] Standard/Premium 22.9.1 (gestaffelte Veröffentlichung vom 13. bis 15. September 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 3. Oktober | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Die Daten für die Version [!DNL Target Standard/Premium] 22.10.1 wurden aktualisiert. |
| 22. September | [[!DNL Adobe Target] Ankündigungen und Veranstaltungen](/help/main/r-release-notes/target-announcements.md) | Es wurden Informationen zu folgendem Ereignis ergänzt:<ul><li>[!DNL Adobe Target] Community Coffee Break mit Fragen und Antworten (28. September 2022)</li></ul> |
| 15. September | [[!DNL Adobe Target] Ankündigungen und Veranstaltungen](/help/main/r-release-notes/target-announcements.md) | Informationen zum folgenden Webinar wurden hinzugefügt:<ul><li>Anpassung der KI-gestützten Personalisierung: Neue Funktionen in [!DNL Adobe Target] (11. Oktober 2022)</li></ul> |
| 13. September | [Die  [!DNL Target] Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md)  | Es wurden Informationen über Benachrichtigungen hinzugefügt, wenn ein [!DNL Recommendations]-Feed fehlschlägt. |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Version 22.9.1 von [!DNL Target Standard/Premium] hinzugefügt. |

## Adobe Target Standard/Premium 22.8.1 (gestaffelte Veröffentlichung: 17.–18. August 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 22. August | [[!DNL Adobe Target] Ankündigungen und Ereignisse](/help/main/r-release-notes/target-announcements.md) | Es wurden Informationen zu der folgenden Ankündigung hinzugefügt:<ul><li>[!DNL Target] im Gartner Magic Quadrant für Personalisierungs-Engines (2022) als führend ausgezeichnet</li></ul>Es wurden Informationen zu folgenden anstehenden Ereignissen hinzugefügt:<ul><li>[!DNL Adobe Target] Kaffeepause mit Fragen und Antworten der Community (31. August 2022)</li><li>Chef&#39;s Collection: Recipes for Personalization (30. August 2022)</li><li>[!DNL Adobe Target] Skill Builders – Mobile Experience Optimization (6. September 2022)</li><li>[!DNL Adobe Target] Skill Builders – AI-Driven Personalization and Recommendations (15. September 2022)</li></ul>Es wurde ein Aufzeichnungs-Link für die folgende Webinar-Sitzung hinzugefügt:<ul><li>Adobe: Personalization Industry Insider – Einzelhandel (11. August 2022)</li></ul> |
| 22. August | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Version 22.8.1 von [!DNL Target Standard/Premium] hinzugefügt. |

## Adobe Target Standard/Premium 22.6.1 (gestaffelte Veröffentlichung: 7.–9. Juni 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 30. Juni | [Adobe Target-Entwicklerhandbuch](https://developer.adobe.com/target/){target=_blank} | Einführung des *Adobe Target-Entwicklerhandbuch* zur Konsolidierung aller [!DNL Target]-Entwicklerinhalte in einem praktischen Portal. Das Portal enthält Informationen zur Implementierung von [!DNL Target] und [!DNL Recommendations], [!DNL Target]-SDKs und [!DNL Target]-APIs. |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Version 22.6.2 von [!DNL Target Standard/Premium] hinzugefügt. |
|  | [Target-Ankündigungen und -Events](/help/main/r-release-notes/target-announcements.md) | Es wurden Links zu Aufzeichnungen früherer Webinar-Sitzungen hinzugefügt. |
| 14. Juni | [Planen und Implementieren von Recommendations](https://developer.adobe.com/target/implement/recommendations/){target=_blank} | Code-Beispiele wurden in den folgenden Abschnitten aktualisiert:<ul><li>Hinzufügungen zum Warenkorb/Warenkorbansichten/Checkout-Seiten</li><li>Ausschließen von Artikeln, die sich bereits im Warenkorb des Besuchers befinden</li></ul> |
| 7. Juni | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Version 22.6.1 von [!DNL Target Standard/Premium] hinzugefügt. |

## Adobe Target Standard/Premium 22.5.1 (gestaffelte Veröffentlichung; 11.–13. Mai 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 7. Juni | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Vorabversionsinformationen für die Version 22.6.1 von [!DNL Target Standard/Premium] hinzugefügt. |
| 31. Mai | [Target-Ankündigungen und -Events](/help/main/r-release-notes/target-announcements.md#webinar-series) | Es wurden Informationen über die kommende kurze Session der [!DNL Adobe Target]-Community (29. Juni 2022) hinzugefügt |
| 25. Mai | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen über die [!DNL Target]-Plattform-Version (25. Mai 2022) und die at.js-Version 2.9.0 (27. Mai 2022) hinzugefügt. |
|  | [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Es wurden Informationen über die at.js-Version 2.9.0 hinzugefügt. |
|  | [User-agent und Client Hints](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} | Neues Thema |
|  | [Target-Ankündigungen und -Ereignisse](/help/main/r-release-notes/target-announcements.md#webinar-series) | Es wurde ein Link mit der Aufzeichnung des folgenden Webinars hinzugefügt: Dick&#39;s Sporting Goods: Personalisierung und die sich ändernde Landschaft im Einzelhandel (19. Mai 2022) |
| 23. Mai | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Vorab-Versionshinweise für at.js-Version 2.9.0 hinzugefügt (25. Mai 2022). |
| 11. Mai | [Target-Ankündigungen und -Events](/help/main/r-release-notes/target-announcements.md#webinar-series) | Es wurden Informationen und Registrierungs-Links für die folgenden Webinare hinzugefügt:<ul><li>Dick&#39;s Sporting Goods: Personalisierung und die sich ändernde Landschaft im Einzelhandel</li><li>Adobe: Personalization Industry Insider – Finanzdienstleister und Versicherungen</li><li>City National Bank: So erreichen Sie die Top 1 % der digitalen Optimierung </li><li>Adobe: Personalisierung mit Präzision – [!DNL Adobe Analytics] und [!DNL Target] </li><li>City National Bank: Zero to Hero – Launch und Skalierung eines Personalisierungsprogramms</li><li>Adobe: Entdecken Sie wirkungsvolle Optimierungsmöglichkeiten</li><li>Adobe: Personalization Industry Insider – Einzelhandel </li></ul>Eine Aufzeichnung für das folgende Webinar wurde hinzugefügt:<ul><li>Echtzeit-Personalisierung mit [!DNL Adobe Target]</li></ul> |
|  | [Richtlinien zur Content Security Policy (CSP)](https://developer.adobe.com/target/before-implement/privacy/content-security-policy/){target=_blank} | Der Abschnitt „Häufig gestellte Fragen“ wurde hinzugefügt. |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen zu den Releases von [!DNL Target Standard/Premium] 22.5.1 und der Target-Plattform (11.–13. Mai 2022) hinzugefügt. |

## Adobe Target Standard/Premium 22.4.1 (28. April)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 10. Mai | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Vorabversion 22.5.1 von [!DNL Target Standard/Premium] hinzugefügt. |
| 28. April | [Enterprise-Benutzerberechtigungen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#move-audience) | Die folgende häufig gestellte Frage wurde hinzugefügt:<ul><li>Kann ich eine Zielgruppe von einem Arbeitsbereich in einen anderen verschieben?</li></ul> |
|  | [[!UICONTROL Automatische Zuordnung] – Überblick](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#section_0E72C1D72DE74F589F965D4B1763E5C3) | Folgende FAQs wurden hinzugefügt:<ul><li>Kann mit der Aktivität [!UICONTROL Automatische Zuordnung] das Lookback-Fenster während eines Tests angepasst werden, um Veränderungen im Zeitverlauf zu berücksichtigen?</li><li>Wird bei [!UICONTROL Automatische Zuordnung] einem wiederkehrenden Besucher das erfolgreichste Erlebnis angezeigt, wenn sich das erfolgreichste Erlebnis von dem unterscheidet, das der Besucher bei der Qualifizierung für die Aktivität gesehen hat?</li></ul> |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen zu den Releases von [!DNL Target Standard/Premium] 22.4.1 und der Target-Plattform (27. April 2022) hinzugefügt. |

## Adobe Target Standard/Premium 22.3.1 (5. April)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 26. April | [Target-Ankündigungen und -Events](/help/main/r-release-notes/target-announcements.md) | Es wurden Informationen zu folgenden Events hinzugefügt:<ul><li>Webinar: Echtzeit-Personalisierung mit Adobe Target (28. April 2022)</li><li>[!DNL Adobe Target] Community-Kaffeepause mit Fragen und Antworten (25. Mai 2022)</li></ul> |
|  | [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#discrepancies) | Die folgende häufig gestellte Frage wurde hinzugefügt:<ul><li>Wie kann ich Diskrepanzen bei der Traffic-Verteilung bei der Verwendung von Umleitungsangeboten in A4T-Aktivitäten minimieren?</li></ul> |
|  | [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | Folgender Abschnitt wurde hinzugefügt:<ul><li>Entfernen von ClientLibs und externem HTML-Code aus nach Target exportierten Experience Fragments</li></ul> |
| 21. April | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Informationen zur Vorabversion der [!DNL Target]-Plattform wurden hinzugefügt, deren Veröffentlichung für den 17. April 2022 geplant ist. |
| 20. April | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Vorabversion von [!DNL Target Standard/Premium] 22.4.1 hinzugefügt. |
| 14. April | [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md) | Es wurden Informationen zum Neuanordnen-Abschnitt hinzugefügt, in denen erklärt wird, wie inkonsistentes VEC-Verhalten bei den Aktionen [!UICONTROL Verschieben] und [!UICONTROL Neu anordnen] aufgrund des verzögerten Ladens von DOM-Elementen gehandhabt werden sollen. |
| 13. April | [Target-Ankündigungen und -Ereignisse](/help/main/r-release-notes/target-announcements.md) | Es wurden Informationen zu folgendem Ereignis ergänzt:<ul><li>[!DNL Adobe Target] Kaffeepause mit Fragen und Antworten der Community (27. April 2022)</li></ul> |
|  | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur [!DNL Target]-Plattform-Version hinzugefügt. |
| 4. April | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen zur Version 22.3.1 von [!DNL Target Standard/Premium] aktualisiert. |

## Adobe Target Standard/Premium 22.2.1 (1. Februar 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 30. März | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur [!DNL Target]-Plattform-Version hinzugefügt. |
| 28. März | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Vorabversion der [!DNL Target]-Plattform hinzugefügt. |
| 22. März | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Versionsinformationen zur Fehlerbehebung in [!DNL Target Standard/Premium] hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Vorabversion 22.3.1 von [!DNL Target Standard/Premium] hinzugefügt. |
| 17. März | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Vorabversions-Informationen zur Fehlerbehebung in [!DNL Target Standard/Premium] hinzugefügt. |
|  | [Echtzeit-Profilsynchronisation für mbox3rdPartyId](/help/main/c-target/c-visitor-profile/3rd-party-id.md) | Der folgende Satz zur Profilsynchronisierung wurde aktualisiert: „Aktualisierungen werden alle 5 bis 10 Minuten mit dem Profilspeicher synchronisiert.“ |
| 8. März | [Target-Ankündigungen und -Ereignisse](/help/main/r-release-notes/target-announcements.md) | Es wurden Informationen zu folgendem Ereignis ergänzt:<ul><li>[!DNL Adobe Target] Kaffeepause mit Fragen und Antworten der Community (30. März 2022)</li></ul> |
| 7. März | [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/audiences.md#aep) | Ein neuer Abschnitt wurde unter „Verwenden von Zielgruppen aus [!DNL Adobe Experience Platform]“ hinzugefügt<ul><li>Anwendungsfälle für die Personalisierung</li></ul> |
| 25. Februar | [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) | Die folgenden Abschnitte wurden aktualisiert:<ul><li>[Automatische Zuordnung und automatisches Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#both)</li><li>[Automatische Zuordnung](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa)</li></ul> |
|  | [Interpretieren der automatischen Zuordnungsberichte](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | Neue FAQs wurden hinzugefügt:<ul><li>Sind die Abzeichen „Kein Gewinner“, „Gewinner“ und „Stern“ verfügbar für Aktivitäten des Typs [!UICONTROL Automatische Zuordnung], die [!UICONTROL Analytics als Berichtsquelle] (A4T) verwenden?</li></ul> |
|  | [Erstellen einer Zielgruppe „Nur Aktivität“](/help/main/c-target/creating-activity-only-audience.md) | Es wurden Informationen zum Abschnitt „Überlegungen“ hinzugefügt, die Ausschlussregeln erläutern. |
| 10. Februar | [Visual Experience Composer Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Es wurden Informationen zum Laden von Websites mit Service Workers im Visual Experience Composer (VEC) hinzugefügt. |
| 7. Februar | [Target-Ankündigungen und -Ereignisse](/help/main/r-release-notes/target-announcements.md) | Es wurden Informationen zu folgendem Ereignis ergänzt:<ul><li>[!DNL Adobe Target] Kaffeepause mit Fragen und Antworten der Community (23. Februar 2022)</li></ul> |
| 3. Februar | [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/audiences.md#RTCDP) | Neuen Abschnitt und Video hinzugefügt: „Video: Personalisierung für den nächsten Treffer mit Real-time CDP und [!DNL Adobe Target]“. |
| 2. Februar | [Fehlerbehebung bei der Inhaltsbereitstellung](/help/main/c-activities/c-troubleshooting-activities/content-trouble.md#escape) | Folgender Abschnitt wurde hinzugefügt: „Das Umgehen von Anführungszeichen in [!DNL Target]-Profilattributwerten funktioniert nicht wie erwartet“. |
| 1. Februar | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen über die Version 22.2.1 von [!DNL Target Standard/Premium] hinzugefügt. |

## [!DNL Adobe Target Standard/Premium] 22.1.1 (12. Januar 2022)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 31. Januar | [Target-Versionshinweise (Vorabversion)](/help/main/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Vorabversion 22.2.1 von [!DNL Target Standard/Premium] hinzugefügt. |
| 28. Januar | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen über die at.js-Version 2.8.1 hinzugefügt. |
|  | [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Es wurden Informationen über die at.js-Version 2.8.1 hinzugefügt. |
| 27. Januar | [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | Das Thema wurde aktualisiert und es wurden Informationen über [!DNL AEM as a Cloud Service] und [!DNL Adobe I/0] hinzugefügt. |
| 26. Januar | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen über die Version 22.1.2 von [!DNL Target Standard/Premium] hinzugefügt. |
|  | [Erstellen von Zielgruppen](/help/main/c-target/c-audiences/audiences.md) | Es wurden Informationen über Zielgruppen von [!DNL Adobe Experience Platform] hinzugefügt. |
|  | [Kombinieren mehrerer Zielgruppen](/help/main/c-target/combining-multiple-audiences.md) | Es wurden Informationen über Zielgruppen von [!DNL Adobe Experience Platform] hinzugefügt. |
| 21. Januar | [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Informationen über die at.js-Version 1.8.3 wurden hinzugefügt. |
| 19. Januar | [Aktualisieren von at.js 1.*x* auf at.js 2.x *x*](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Folgender Abschnitt wurde hinzugefügt: „at.js 2.*x* unterstützt nicht das Erstellen von Zielgruppen unter Verwendung von vst.*-Parametern“ |
| 12. Januar | [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md) | Es wurden Informationen über die Version 22.1.1 von [!DNL Target Standard/Premium] hinzugefügt. |
|  | [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank} | Link zum Tutorial mit Implementierungsanweisungen für [!DNL Adobe Experience Cloud] mit Web SDK hinzugefügt. |
