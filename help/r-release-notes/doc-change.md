---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update
description: This page lists important changes made to the Adobe Target documentation, ordered by releases.
title: Änderungen an der Adobe Target-Produktdokumentation.
feature: release notes
topic: Standard
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
translation-type: tm+mt
source-git-commit: 15a80d35a8a6bce0a55f40c4ae13aa801738880d
workflow-type: tm+mt
source-wordcount: '1894'
ht-degree: 29%

---


# Dokumentationsänderungen{#documentation-changes}

This page lists important changes made to the [!DNL Adobe Target] product documentation.

## Adobe Target Standard/Premium 20.7.1 (27. Juli 2020)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 14. August | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Bekanntes Problem bei der Qualitätssicherung in Recommendations-Aktivitäten wurde hinzugefügt. |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Added text indicating that if you are using `serverState` and using `<script>` tags in the content returned, ensure that your HTML content uses `<\/script>` instead of `</script>`. |
| 12. August | [Understand the Target UI](/help/c-intro/understand-the-target-ui.md) | Neues Thema |
|  | [Adobe Target API overview](/help/api/api-overview.md) | Neues Thema |
| 10. August | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Added text indicating that the size of the cookie header will increase when using CNAME. |
|  | [Zielgruppe mit Adobe Audience Manager integrieren](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) | Neues Thema |
|  | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurde ein Link zur Ansicht des folgenden archivierten Webinars hinzugefügt: &quot;Wie HSBC Adobe Target und AI nutzt, um die Personalisierung schnell zu optimieren und zu liefern.&quot; |
| 6. August | [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md#how-long) | Text für folgende häufig gestellte Fragen aktualisiert: &quot;Wie lange sollte ich warten, bis Modelle gebaut werden?&quot; |
|  | [Classifications – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-classifications.md) | Der Text für &quot;targetType&quot;wurde aktualisiert. |
| August 5 | [Löschen des Target-Cookies](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md) | Das ganze Thema wurde aktualisiert. |
| August 4 | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Registrierungsinformationen zum Webinar &quot;Personalisierungsstrategien mit künstlicher Intelligenz und Adobe Target&quot;hinzugefügt, das für den 13. August geplant ist. |
|  | [Zulassen von gemischtem Inhalt in Ihrem Browser](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md) | Das Thema wurde aktualisiert. |
| August 3 | [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md) | Es wurde ein Hinweis hinzugefügt, der verdeutlicht, was die Optionen [!UICONTROL Anzahl] erhöhen im Hinblick auf Besucher oder Besuche bedeuten. |
| Juli 31 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurde ein neues bekanntes Problem hinzugefügt: &quot;Angebote mit der Beschriftung &quot;Verarbeitung&quot;.&quot; |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Added code sample to use `getoffers()` to perform a pageLoad. |
|  | [Target announcements and events](/help/r-release-notes/target-announcements.md) | Added registration information about the upcoming Adobe Target Community Coffee Break on August 5. |
| Juli 28 | [Personalization Insights reports](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md),<br>[Automated Segments report](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md),<br>and [Important Attributes report](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) | Updated text in the note at the top of the topics. |
|  | [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Folgende FAQs wurden hinzugefügt:<ul><li>Kann ich die Option &quot;Berichtsdaten zurücksetzen&quot;beim Ausführen einer Aktivität für die automatische Zuordnung verwenden?</li><li>How does Auto-Allocate build models with regard to environments?</li></ul> |
|  | [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md) | Folgende Frage wurde hinzugefügt:    <ul><li>Can I use the Reset Report Data option while running an Auto-Target activity?</li></ul>Updated text in the &quot;Considerations&quot; section. |
|  | [Automated Personalization FAQs](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | Folgende FAQs wurden hinzugefügt:<ul><li>Can I use the Reset Report Data option while running an Automated Personalization activity?</li><li>Wie erstellt Automated Personalization Modelle in Bezug auf Umgebung?</li></ul> |
|  | [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Added information about Internet Explorer and unknown elements. |
|  | [Kundenattribute](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Updated following paragraph:<br>[!DNL Adobe] does not guarantee that 100% of customer attribute (visitor profile) data from CRM databases will be onboarded to the [!DNL Experience Cloud] and, thus, be available for use for targeting in [!DNL Target]. In unserem aktuellen Design besteht die Möglichkeit, dass ein kleiner Anteil der Daten (bis zu 0,1 % der großen Produktionschargen) möglicherweise nicht an Bord mitgeführt wird. |
| Juli 27 | [Verwaltung von Target](/help/administrating-target/administrating-target.md) | Der Text in allen verknüpften Themen auf dieser Seite wurde aktualisiert, um die neuen Änderungen an der Benutzeroberfläche für die [!UICONTROL Administrationsseiten] widerzuspiegeln. |
|  | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Folgende Änderungen wurden vorgenommen: <ul><li>Registrierungsinformationen für das folgende Webinar hinzugefügt: &quot;Wie HSBC Adobe Target und AI nutzt, um die Personalisierung schnell zu optimieren und zu liefern.&quot;</li><li>Es wurden Informationen darüber hinzugefügt, dass Adobe erneut als &quot;Leader&quot;im Gartner Magic Quadrant für Personalisierungsmaschinen bezeichnet wird.</li></ul> |
|  | [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md) | Klarere Informationen unter Schritt 4: Wählen Sie einen Ort aus. |
| Juli 24 | <br>[„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informationen zur at.js-Version 2.3.2 wurden hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.7.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.5.1 (17. Juni 2020) 

| Datum | Thema | Änderungen |
| --- | --- | --- |
| Juli 17 | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target-Kaffeepause vom 22. Juli hinzugefügt. |
| Juli 15 | [Die automatisierte Zuordnung kann Ihnen schnellere Testergebnisse und mehr Umsatz als ein manueller Test liefern](/help/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md) | Neues Thema |
| Juli 14 | [Häufig gestellte Fragen zur automatischen Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md),<br>[automatischen Zielgruppe](/help/c-activities/auto-target-to-optimize.md)<br><br>[und automatisierten Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | Häufig gestellte Fragen wurden hinzugefügt, in denen empfohlen wird, die Zielmetrik nicht mitten in einer Aktivität zu ändern. |
| Juli 7 | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target-Kaffeepause vom 8. Juli hinzugefügt. |
| 25. Juni | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Version 20.6.1 von Target Standard/Premium (Juli 2020) hinzugefügt. |
|  | [Übersicht über die Zielgruppe](/help/r-release-notes/target-documentation.md) | Neues Thema, in dem die verschiedenen [!DNL Target] Dokumentationsquellen ausführlich beschrieben werden. |
| 23. Juni | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target-Kaffeepause vom 24. Juni hinzugefügt. |
|  | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Es wurde ein Hinweis hinzugefügt, dass das Erstellen von Skripten mit abhängigen Profilen, die das Ergebnis eines Profil-Skripts in einem anderen Profil-Skript verwenden, nicht empfohlen wird. |
|  | [Funktionsweise von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Das folgende Video wurde hinzugefügt: Bürozeiten: &quot;at.js&quot;-Tipps und -Übersicht |
| 17. Juni | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das Thema wurde aktualisiert. |
|  | [Antwort-Token](/help/administrating-target/response-tokens.md) | Es wurden Informationen zu Antwort-Token für die Traffic-Zuordnungsmethode für [!UICONTROL Auto-Zielgruppe] - und [!UICONTROL Automated Personalization] -Aktivitäten hinzugefügt. |
|  | [Aktivitätserstellung](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | Es wurden Informationen zur Unterstützung von Analytics for Zielgruppe (A4T) für Aktivitäten mit automatisierter Zuordnung hinzugefügt. |
|  | [Benutzer](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Es wurden Informationen zur neuen [!UICONTROL Herausgeberrolle] unter Rollen und Berechtigungen *festlegen* hinzugefügt. |
|  | [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Informationen zur neuen [!UICONTROL Herausgeberrolle] unter *Schritt 6 hinzugefügt: Legen Sie Rollen und Berechtigungen* fest. |
|  | [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Link zu den *Bürozeiten hinzugefügt: Zielgruppe Premium-Arbeitsflächen-Sitzung*. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.5.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.4.1 (6. Mai 2020) 

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 15. Juni | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den Versionen at.js 1.8.2 und at.js 2.3.1 hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den Versionen at.js 1.8.2 und at.js 2.3.1 hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Die Hinweise für die Version [!DNL Target Standard/Premium] 20.5.1 (17. Juni 2020) wurden aktualisiert und enthalten nun Informationen zur Unterstützung von A4T in [!DNL Analysis Workspace]. |
| 12. Juni | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Informationen zur Einstellung `deviceIdLifetime` wurden hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zu den Versionen at.js 1.8.2 und at.js 2.3.1 hinzugefügt. |
| Juni 8 | [Target for mobile apps FAQ](/help/c-target-mobile-app/target-for-mobile-apps-faq.md) | Text für folgende häufig gestellte Fragen aktualisiert: &quot;Ist Zielgruppe Mobile nur eine Funktion der Adobe Target Premium-Produkt-SKU?&quot; |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Das ganze Thema wurde aktualisiert. |
| June 5 | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target-Kaffeepause vom 10. Juni hinzugefügt. |
|  | [Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md) | Text für folgende häufig gestellte Fragen aktualisiert: &quot;Warum kann ich Steigerung und Konfidenz bei berechneten Metriken nicht sehen?&quot; |
| 4. Juni | [A4T-Reporting](/help/c-integrating-target-with-mac/a4t/reporting.md) | Updated the &quot;Reports in Analytics&quot; section. |
| Juni 1 | [Mitteilungen zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurde eine neue Seite zur Ankündigung anstehender Ereignis der Zielgruppe hinzugefügt. |
|  | [Mobile Viewports für responsive Erlebnisse](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) | Updated viewport dimensions and resolutions for Apple iPhone 11, Apple iPhone SE, and Google Pixel 2 XL models. |
| Mai 28 | [Häufig gestellte Fragen zum Reporting](/help/c-reports/reporting-frequently-asked-questions.md) | Folgende neue Frage wurde hinzugefügt: <ul><li>How are the New Visitors and Returning Visitors metrics counted?</li></ul> |
| Mai 27 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Added information about Analytics for Target (A4T) support for Auto-Allocate activities. |
| Mai 26 | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Folgende Informationen wurden hinzugefügt: &quot;Der Parameter bleibt im Profil, nachdem das Skript deaktiviert wurde. Benutzer, deren Profil bereits einen Parameter enthalten, der in der Audience einer Aktivität verwendet wird, sind in dieser Aktivität berechtigt.&quot; |
| Mai 21 | [Zulassungsliste Zielgruppe Edge-Knoten](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Der Liste `mboxedge30.tt.omtrdc.net` hinzugefügt. |
| Mai 20 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur kommenden Target Standard/Premium-Version 20.6.1 (10. Juni 2020) hinzugefügt. |
|  | [Hosts](/help/administrating-target/hosts.md) | Es wurde ein Hinweis zum Abschnitt &quot;Best Practices für die Sicherheit&quot;hinzugefügt. |
| Mai 14 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den Änderungen an der Profil Batch Status API Version 2 hinzugefügt. |
| Mai 13 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Der Abschnitt &quot;Bekannte Einschränkungen&quot;wurde hinzugefügt. |
| Mai 11 | [Hosts](/help/administrating-target/hosts.md) | Es wurden Informationen zur Verwendung der Ubox-Funktion mit Umleitungen und Zulassungslisten hinzugefügt. |
|  | [Arbeiten mit Weiterleitungen](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) | Es wurden Informationen zur Verwendung von Hosts hinzugefügt, um Open-Redirect-Schwachstellen zu vermeiden. |
|  | [Integration von Recommendations in E-Mail](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | Added information about using hosts to avoid Open Redirect Vulnerabilities. |
|  | [E-Mail: Target-Implementierung](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md) | Added information about using hosts to avoid Open Redirect Vulnerabilities. |
| Mai 7 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | With the upcoming deprecation of mbox.js on August 30, 2020, David Son, Adobe Target Product Manager recently hosted a developer chat to discuss the benefits of migrating mbox.js to at.js. There is a link where you can watch the webinar for the next 30 days. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Updated the &quot;Considerations&quot; section. |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Die Zeile &quot;overrideMboxEdgeServer&quot;unter &quot;Einstellungen&quot;wurde aktualisiert. |
| Mai 6 | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md) | Added information about ITP 2.3. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.4.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.2.1 (19. Februar 2020)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| Mai 4 | [Häufig gestellte Fragen zum Reporting](/help/c-reports/reporting-frequently-asked-questions.md#uneven) | Added new FAQ: &quot;Why is the traffic split between my experiences uneven in my A/B or MVT activity?&quot; |
| April 29 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Added known issue for reporting with extreme orders. |
| April 28 | [Nützliche Variablen, Profile, Parameter und Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Removed information about using `user.header('x-forwarded-for')` with newer AWS edges to retrieve users&#39; IP addresses. Dieser Befehl funktioniert jetzt mit neueren AWS-Kanten. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Das Datum der Target Standard/Premium-Version (20.4.1) wurde in den 6. Mai geändert. |
| April 23 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das Thema wurde aktualisiert. |
| April 22 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Added new section: *Profile Batch Status API v2 changes (May 4, 2020).* |
| April 20 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Added new section: *Adobe Target Skill Builder: Developer chat, migrate Adobe Target&#39;s mbox.js to at.js.* |
| April 14 | [Zulassungsliste Zielgruppe Edge Hosts](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Neues Thema |
| April 10 | [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp) | Neuer Abschnitt hinzugefügt: &quot;Best Practices für die Implementierung&quot;. |
| April 7 | [Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence) | Der Text für &quot;Warum kann ich Steigerung und Konfidenz bei berechneten Metriken nicht sehen?&quot; wurde aktualisiert. |
| April 2 | [Nützliche Variablen, Profile, Parameter und Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Es wurden Informationen zur Verwendung `user.header('x-forwarded-for')` mit neueren AWS-Kanten zum Abrufen der IP-Adressen von Benutzern hinzugefügt. |
|  | [Aktualisieren von at.js 1.*x* auf at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Folgender Hinweis wurde hinzugefügt:<ul><li>Nach der Installation der ECID-Bibliothek v 4.3.0 + und at.js 2.*x* können Sie Aktivitäten erstellen, die mehrere Domänen umfassen und Benutzer tracken können. Beachten Sie, dass diese Funktion erst nach Ablauf der Sitzung funktioniert.</li></ul> |
| March 30 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Es wurden bekannte Probleme hinzugefügt, die at.js-Versionen vor at.js 2.2.0 betreffen. Dieses Problem führte dazu, dass Klick-Tracking keine Konvertierungen in Analytics für die Zielgruppe (A4T) meldete, wenn Adobe Analytics-Code nicht in Seitenelementen vorhanden war. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Die folgenden Informationen wurden den Details zu at.js Version 2.2.0 hinzugefügt:<ul><li>Es wurde ein Problem behoben, bei dem Klick-Tracking keine Konversionen in Analytics für Zielgruppe (A4T) meldete, wenn Adobe Analytics-Code nicht in Seitenelementen vorhanden war.</li></ul> |
| March 25 | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den folgenden neuen Versionen von at.js hinzugefügt:<ul><li>at.js Version 2.3.0</li><li>at.js version 1.8.1</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Die folgenden neuen Zeilen wurden im Abschnitt &quot;Einstellungen&quot;hinzugefügt:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>Der folgende neue Abschnitt wurde hinzugefügt:<ul><li>Content Security Policy</li></ul> |
| March 24 | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact) | Es wurden Informationen zu den Auswirkungen für Folgendes hinzugefügt:<ul><li>Profil-Skripten basierend auf 3rdPartyID</li><li>QS-/Vorschauen-URLs auf iOS-Geräten</li></ul> |
| 20. März | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurde angegeben, dass die Target Standard/Premium-Version 20.2.1 der 23. März 2020 sein wird. |
| 13. März | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Die Anzahl der &quot;Audiencen, die pro Konto wiederverwendet werden können&quot;wurde aktualisiert. |
| 12. März | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md#summit) | Es wurden Informationen zur Registrierung für den freien Zugang zur Online-Konferenz des digitalen Gipfels hinzugefügt. |
| März 9 | [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) | Es wurden weitere Informationen im Abschnitt &quot;Ersetzen des letzten Oktetts von IP-Adressen&quot;hinzugefügt. |
|  | [Arbeiten mit Attributen mit mehreren Werten](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Codebeispiel in *Übergeben eines Parameters mit mehreren Werten in JavaScript* aktualisiert. |
|  | [Benutzerdefinierte Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md) | Codebeispiel in *Verwenden von APIs* unter *Implementieren von Attributen* mit mehreren Werten hinzugefügt. |
| 4. März | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Das gesamte Thema wurde aktualisiert und der Abschnitt &quot;Best Practices&quot;wurde umfassend überarbeitet. |
| 21. Februar | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur neuen Adobe Experience Cloud-Navigation hinzugefügt. |
| 20. Februar | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Updated the description for the `enabled` setting. Es wurden Informationen zu den folgenden Einstellungen hinzugefügt: `pageLoadEnabled` und `viewsEnabled`. |
| 19. Februar | [Versionshinweise](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur bevorstehenden Vernichtung der Bibliothek &quot;mbox.js&quot;hinzugefügt. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Es wurde ein Hinweis hinzugefügt, der in at.js 1 unterstützt `mboxOverride.browserIp` wird.*x*, zur Verfügung. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurde klargestellt, welche Versionen von &quot;at.js&quot;vom Zielgruppe-Team unterstützt werden. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.2.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.1.1 (4. Februar 2020)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| Februar 4 | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.1.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |
