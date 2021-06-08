---
keywords: Änderungsprotokoll zur Target-Dokumentation; Aktualisierungen in der Dokumentation; neue Themen; Bearbeitungen; Aktualisierungen; Aktualisierung
description: 'Informationen zu wichtigen Ergänzungen und Änderungen in der Produktdokumentation von Adobe  [!DNL Target] '
title: Wo finde ich Informationen zu Änderungen an der Target-Dokumentation?
feature: Versionshinweise
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
source-git-commit: 41fd231ff37bf26b955b86bf70b880e1dae0c2eb
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 79%

---

# Dokumentationsänderungen

Auf dieser Seite sind wichtige Änderungen an der Produktdokumentation von [!DNL Adobe Target] zusammengefasst.

## Adobe [!DNL Target] Standard/Premium 21.6.1 (7. Juni 2021)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 8. Juni | [Vor der Implementierung von Analytics for Target (A4T) mit at.js](/help/c-integrating-target-with-mac/a4t/before-implement.md) | Es wurde ein Hinweis hinzugefügt, der angibt, dass at.js 1.8.0 oder höher nicht mehr mit Visitor API-Versionen älter als 2.5.0 funktioniert, um [!DNL Adobe Audience Manager] (AAM) Parameter zu übergeben. |
|  | [Umgebungen](/help/administrating-target/environments.md) | Es wurde ein Hinweis hinzugefügt, der angibt, dass Hosts aus dieser Umgebung auch inaktive Aktivitäten anzeigen, wenn Sie [!UICONTROL Aktive und inaktive Aktivitäten] angeben. |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Das folgende bekannte Problem wurde hinzugefügt:<ul><li>[!DNL Adobe Experience Platform] Segmentnamen werden nicht im Bericht &quot; [!UICONTROL Wichtige ] Attribute&quot;angezeigt.</li></ul> |
| 7. Juni | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.6.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe [!DNL Target] Standard/Premium 21.4.1 (Montag, 19. April 2021) 

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 3. Juni | [Target-Ankündigungen und -Ereignisse](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target Community Q&amp;A Coffee Break hinzugefügt, die am Mittwoch, den 9. Juni 2021 um 8 Uhr stattfinden wird. (PDT, GMT-7). |
| 1. Juni | [CNAME und [!DNL Target]](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Folgende häufig gestellte Fragen wurden hinzugefügt:<ul><li>Wie verwende ich einen Ausschluss-Link mit CNAME?</li></ul> |
|  | [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) | Der Abschnitt &quot;Ausschluss-Link&quot;wurde aktualisiert, um zu erklären, wie der Ausschluss-Link mit CNAME verwendet werden kann. |
|  | [[!DNL Adobe Analytics] as the reporting source for [!DNL Adobe Target] (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | Es wurden Informationen zum [!DNL Adobe Experience Platform Web SDK] hinzugefügt. |
|  | [Analytics  [!DNL Target] für die Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#platform) | Es wurde ein neuer Abschnitt hinzugefügt:<ul><li>Implementierungsschritte für eine [!DNL Adobe Experience Platform Web SDK] -Implementierung</li></ul> |
|  | [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) | Es wurden Informationen zur Verwendung von Umleitungsangeboten mit A4T und dem Platform Web SDK hinzugefügt. |
|  | [Antwort-Token](/help/administrating-target/response-tokens.md) | Es wurden Informationen zur Verwendung von Antwort-Token mit [!DNL Adobe Experience Platform Web SDK] hinzugefügt.<br>**Hinweis**: Diese Funktion wird in einer zukünftigen Version des Platform Web SDK veröffentlicht (Datum noch festzulegen). |
|  | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur Adobe Experience Platform Web SDK-Version 2.5.0 (1. Juni 2021) hinzugefügt. |
| 27. Mai | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Es wurde ein Abschnitt für [!DNL Target]-API-Aufrufe hinzugefügt. Die Begrenzung beträgt 50 Anrufe pro Minute. |
| 20. Mai | [Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) | Es wurde ein Link zum folgenden Blogpost im Adobe Tech Blog hinzugefügt:<ul><li>Adobe Tech Blog - Part 2: Führen Sie [!DNL Adobe Target] NodeJS-SDK für Experimentierungen und Personalisierung auf Edge-Plattformen aus (AWS Lambda@Edge).</li></ul> |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Das folgende bekannte Problem wurde hinzugefügt: &quot;Die Archivierung von [!UICONTROL Aktivitäten mit automatischem Targeting] kann zu Synchronisierungsproblemen führen.&quot; |
| 17. Mai | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur „at.js“-Version 2.5.0 hinzugefügt. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Das Thema wurde aktualisiert, um anzugeben, dass Vorschaulinks für [!UICONTROL Automated Personalization] (AP)-Aktivitäten mit at.js 2.5.0 (und höher) verfügbar sind. |
|  | [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Es wurde angegeben, dass die at.js-Version 2.5.0 die Unterstützung für Microsoft Internet Explorer 10, Internet Explorer 11 und alle älteren Versionen entfernt. Microsoft Edge wird in at.js 2.5.0 und höher weiterhin unterstützt. |
|  | [Beheben von Problemen mit  [!UICONTROL Enhanced Experience Composer]](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) | Die Liste der IP-Adressen wurde auf die Zulassungsliste aktualisiert. |
| 12. Mai | [[!DNL Target] Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Vorabversionshinweise für Folgendes hinzugefügt:<ul><li>Adobe Experience Platform Web SDK (17. Mai 2021)</li><li>Target Standard Premium 21.5.2</li></ul> |
| 10. Mai | [[!DNL Recommendations] FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Folgende FAQ wurden hinzugefügt: &quot;Kann ich einen Algorithmus verwenden, der in [!DNL Adobe Recommendations Classic] in [!DNL Recommendations Premium] erstellt wurde?&quot; |
|  | [Implementieren von [!DNL Target] using [!DNL Dynamic Tag Manager]  (DTM)](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md) | Gibt an, dass [!DNL Adobe Dynamic Tag Manager] nicht mehr unterstützt wird. Stattdessen empfiehlt [!DNL Adobe] die Implementierung mit [[!DNL Adobe Experience Platform Launch]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). |
| 6. Mai | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Folgende FAQs wurden hinzugefügt:<ul><li>Wie lange dauert es, bis eine Konfigurationsänderung meiner Aktivitäts-, Angebots-, Promotion- oder Kriterieneinstellungen für [!UICONTROL Recommendations] auch auf meiner Site wirksam ist?</li><li>Wie lange dauert es, bis das Verhalten eines Benutzers (z. B. Klick auf Produkt A und Kauf von Produkt B) in den Empfehlungen berücksichtigt wird, die *dieser* Benutzer erhält?</li><li>Wie lange dauert es, bis das Verhalten eines Benutzers (z. B. Klick auf Produkt A und Kauf von Produkt B) in den Empfehlungen berücksichtigt wird, die *andere* Benutzer erhalten?</li></ul> |
|  | [Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) | Es wurde ein Link zum folgenden Blogpost im Adobe Tech Blog hinzugefügt:<ul><li>Teil 1: Run Adobe Target NodeJS SDK for Experimentation and Personalization on Edge Platforms (Akamai Edge Workers)</li></ul> |
| 5. Mai | [Target-Ankündigungen und -Ereignisse](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target Community Q&amp;A Coffee Break hinzugefügt, die am Mittwoch, den 12. Mai 2021, um 8 Uhr (PDT, GMT-7) stattfinden wird. |
| 27. April | [Cookie-Einstellungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | Ein Thema wurde aktualisiert, um darauf hinzuweisen, dass die Cookie-Dauer (`deviceIdLifetime`-Einstellung) in at.js-Version 2.3.1 oder höher überschrieben werden kann. |
|  | [Adobe Target-Anleitung](/help/target-home.md) | Es wurden Informationen zum Adobe Summit hinzugefügt. |
| 26. April | [Fehlerbehebung bei der geräteinternen Entscheidungsfindung für at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/troubleshooting-on-device-decisioning.md) | Neues Thema |
| 19. April | [Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) | Folgende neue Artikel wurden hinzugefügt:<ul><li>[Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)</li><li>[Unterstützte Funktionen für die geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)</li><li>[Artefakt der geräteinternen Entscheidungsregel](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md)</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#on-device-decisioning) | Es wurden Informationen hinzugefügt über `decisioningMethod`. |
|  | [adobe.target.getOffers() - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Folgendes wurden hinzugefügt:<ul><li>Informationen über den `decisioningMethod`-Schlüssel.</li><li>Ein Beispiel für „getCallOffers(), um eine geräteinterne Entscheidungsfindung vorzunehmen“.</li></ul> |
|  | [Benutzerdefinierte at.js-Ereignisse](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | Folgende Informationen wurden hinzugefügt:<ul><li>Artefakt bei der geräteinternen Entscheidungsfindung erfolgreich</li><li>Artefakt bei der geräteinternen Entscheidungsfindung fehlgeschlagen</li></ul> |
|  | [Aktivitäten](/help/c-activities/activities.md) | Es wurden Informationen zur geräteinternen Entscheidungsfindung hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informationen zur at.js-Version 2.5.0 wurden hinzugefügt. |
|  | [Implementieren von Target ohne einen Tag-Manager](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md) | Es wurden Informationen zur geräteinternen Entscheidungsfindung hinzugefügt. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Seit [at.js 2.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) werden Vorschau-Links für Aktivitäten vom Typ [!UICONTROL Automated Personalization] unterstützt. |
|  | [Verwenden dynamischer und statischer Einschlussregeln](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators) | Es wurden Informationen zu den folgenden neuen Operatoren hinzugefügt:<ul><li>Ist in Liste enthalten</li><li> Ist nicht in Liste enthalten</li><li>Liste enthält ein Element in</li><li>Liste enthält kein Element in</li><li>Liste enthält alle Elemente in</li><li>Liste enthält nicht alle Elemente in</li></ul> |
|  | [Adobe Target-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html?lang=de)<br> (*Handbuch für Experience Cloud Services und Administration*) | Es wurden zusätzliche Informationen zur Sitzungs-ID hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.4.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe [!DNL Target] Standard/Premium 21.2.1 (Dienstag, 9. März 2021)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 9. April | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Vorabinformationen für at.js-Version 2.5.0 wurden hinzugefügt (19. April 2021). |
| 9. April | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Vorabinformationen zu Target Standard/Premium 21.4.1 (19. April 2021) wurden hinzugefügt. |
|  | [Integration von Recommendations in E-Mail](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | Es wurde ein Hinweis zu Kapazitätsrichtlinien für die Optionen 1 und 2 hinzugefügt. |
| 29. März | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#persist-across-devices) | Neue FAQs wurden hinzugefügt:<ul><li>Werden Empfehlungen, die auf kürzlich betrachteten Artikeln basieren, für einen einzelnen Besucher auf mehreren Geräten angezeigt?</li></ul> |
| 23. März | [Versionshinweise](/help/r-release-notes/release-notes.md) | Versionshinweise für at.js-Version 2.4.1 hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Versionshinweise für at.js-Version 2.4.1 hinzugefügt. |
|  | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Die folgende häufig gestellte Frage wurde aktualisiert:<ul><li>Wie lange dauert es, bis Aktualisierungen an Elementen in meinem Katalog auf meiner Site erscheinen?</li></ul> |
| 22. März | [Von Recommendations-Feed verarbeitenden Servern verwendete IP-Adressen](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md) | Die Liste der IP-Adressen wurde aktualisiert. |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Der Abschnitt „Anzahl der Entitäten“ unter „Entitäten“ wurde aktualisiert. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Informationen zur at.js-Version 2 wurden hinzugefügt.*x* unter „Wie kann ich meine Aktivitäten als Benutzer von einem anderen Standort testen?“ |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.2.1 | Folgender Abschnitt wurde hinzugefügt: <ul><li>Änderungen der IP-Adresse für Recommendations-Feed-Verarbeitungs-Server (16. März 2021)</li></ul> |
| 19. März | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#deactivated) | Folgende häufig gestellte Fragen wurden hinzugefügt:<ul><li>Warum sehe ich nach der Deaktivierung meiner Aktivität weiterhin zusätzliche Impressionen?</li></ul> |
| 12. März | [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md#tutorial) | Das folgende neue Tutorial wurde hinzugefügt:<ul><li>Einrichten von A4T-Berichten in Analysis Workspace für automatische Targeting-Aktivitäten</li></ul> |
| 9. März | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md#offer-size) | <ul><li>Die zulässigen Größenbeschränkungen für Angebote wurden aktualisiert.</li><li>Die Zeichenbeschränkung für den Parameter „categoryId“ wurde korrigiert.</li></ul> |
|  | [Zulassungsliste für Target-Edge-Knoten](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Die IP-Adressen des [!DNL Target]-Edge wurden aktualisiert. |
|  | [Entitätsattribute](/help/c-recommendations/c-products/entity-attributes.md) | Der Text wurde erweitert und gibt nun an, dass entity.value ein Dezimalformat aufweisen muss (z. B. 15.99 anstelle von 15,99). |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.2.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe [!DNL Target] Standard/Premium 21.1.1 (Dienstag, 19. Januar 2021)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 22. Februar | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Die folgende häufig gestellte Frage wurde aktualisiert:<ul><li>Wo können Segmente in Analysis Workspace angewendet werden?</li></ul> |
| 16. Februar | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Der Text zur Größenbeschränkung von Angeboten in den vorab veröffentlichten Versionshinweisen wurde aktualisiert. |
| 11. Februar | [Funktionsweise von Target](/help/c-intro/how-target-works.md) | Der Abschnitt „Bots“ wurde aktualisiert. |
| 10. Februar | [Target-Ankündigungen und -Ereignisse](/help/r-release-notes/target-announcements.md) | Informationen zur Adobe Target Community Q&amp;A Coffee Break am Mittwoch, 24. Februar 2021, wurden hinzugefügt. |
| 8. Februar | [Mobile Target-Vorschau](/help/c-target-mobile-app/target-mobile-preview.md) | Ein Codefragment wurde hinzugefügt, das Sie der Datei AndroidManifest.xml für Version 4 des Adobe Mobile SDK hinzufügen sollten. |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Unklarheiten beim folgenden bekannten Problem wurden beseitigt:<ul><li>Sammlungen, Ausschlüsse, Kriterien und Designs, die über die API erstellt wurden, sind in der Benutzeroberfläche von Target nicht sichtbar und können nur über die API bearbeitet werden. Erstellen Sie umgekehrt eines dieser Elemente in der Benutzeroberfläche von Target und bearbeiten Sie diese später über die API, werden die Änderungen nicht in der Benutzeroberfläche von Target angezeigt. Über die API bearbeitete Elemente sollten weiterhin über die API bearbeitet werden, um sicherzustellen, dass keine Änderungen verloren gehen.</li></ul> |
| 1. Februar | [Automated Personalization-Zusammenfassungsberichte](/help/c-reports/reports-ap.md) | Der neue Abschnitt „Häufig gestellte Fragen“ wurde hinzugefügt. |
| 27. Januar | [Erstellen von Umleitungsangeboten](/help/c-experiences/c-manage-content/offer-redirect.md) | Das Thema wurde aktualisiert. |
|  | [Remote-Angebote erstellen](/help/c-experiences/c-manage-content/about-remote-offers.md) | Das Thema wurde aktualisiert. |
| 26. Januar | [Konversionsrate](/help/c-reports/conversion-rate.md) | Es wurde klargestellt, wie Target die Quadratsumme in Student-T-Tests verwendet. |
| 22. Januar | [Konversionsrate](/help/c-reports/conversion-rate.md#t-test) | Der Abschnitt „Warum empfiehlt Target die Verwendung von Student-T-Tests?“ wurde hinzugefügt. |
| 21. Januar | [Fehlerbehebung bei der Analytics- und Target-Integration (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) | Der Abschnitt „A4T-Aktivitätsberichte enthalten eine Zeile mit einer großen Anzahl „nicht spezifizierter“ Ereignisse“ wurde hinzugefügt. |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Der folgende Abschnitt wurde aktualisiert: „Warum wird in Analytics-Berichten „nicht spezifiziert“ angezeigt? Was bedeutet das?“ |
| 20. Januar | [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) | Neues Thema |
| 19. Januar | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Informationen zu Target 21.1.1 (19. Januar 2021) wurden hinzugefügt. |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Der Text zum Parameter „`productPurchasedID`“ wurde aktualisiert. |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Ein bekanntes Problem beim Kopieren einer [!UICONTROL Recommendations]-Aktivität mit einer aktiven Promotion wurde hinzugefügt. Jede Änderung an der kopierten Aktivität wirkt sich auch auf die ursprüngliche Aktivität aus (und umgekehrt). Eine temporäre Problemumgehung wird beschrieben. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.1.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |
