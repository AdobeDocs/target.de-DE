---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update
description: Auf dieser Seite werden wichtige Änderungen an der Adobe Target-Dokumentation, geordnet nach Versionen, Liste.
title: Änderungen an der Adobe Target-Produktdokumentation.
topic: Standard
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
translation-type: tm+mt
source-git-commit: 4287c93058e279da6de262a19fbabb4bbacdf7ad
workflow-type: tm+mt
source-wordcount: '1856'
ht-degree: 29%

---


# Dokumentationsänderungen{#documentation-changes}

This page lists important changes made to the [!DNL Adobe Target] product documentation.

## Adobe Target Standard/Premium 20.7.1 (27. Juli 2020)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 12. August | [Die Benutzeroberfläche der Zielgruppe](/help/c-intro/understand-the-target-ui.md) | Neues Thema |
|  | [Übersicht über die Adobe Target API](/help/api/api-overview.md) | Neues Thema |
| 10. August | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Es wurde Text hinzugefügt, der angibt, dass die Größe des Cookie-Headers bei Verwendung von CNAME zunimmt. |
|  | [Zielgruppe mit Adobe Audience Manager integrieren](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) | Neues Thema |
|  | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurde ein Link zur Ansicht des folgenden archivierten Webinars hinzugefügt: &quot;Wie HSBC Adobe Target und AI nutzt, um die Personalisierung schnell zu optimieren und zu liefern.&quot; |
| 6. August | [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md#how-long) | Text für folgende häufig gestellte Fragen aktualisiert: &quot;Wie lange sollte ich warten, bis Modelle gebaut werden?&quot; |
|  | [Classifications – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-classifications.md) | Der Text für &quot;targetType&quot;wurde aktualisiert. |
| August 5 | [Löschen des Target-Cookies](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md) | Das ganze Thema wurde aktualisiert. |
| August 4 | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Registrierungsinformationen zum Webinar &quot;Personalisierungsstrategien mit künstlicher Intelligenz und Adobe Target&quot;hinzugefügt, das für den 13. August geplant ist. |
|  | [Enabling mixed content in your browser](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md) | Das Thema wurde aktualisiert. |
| August 3 | [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md) | Es wurde ein Hinweis hinzugefügt, der verdeutlicht, was die Optionen [!UICONTROL Anzahl] erhöhen im Hinblick auf Besucher oder Besuche bedeuten. |
| Juli 31 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Added new known issue: &quot;Image Offers showing “Processing” label.&quot; |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Codebeispiel für die Durchführung `getoffers()` von pageLoad hinzugefügt. |
|  | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Added registration information about the upcoming Adobe Target Community Coffee Break on August 5. |
| Juli 28 | [Personalization Insights-Berichte](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md),<br>[Automatisierte Segmente-Bericht](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md),<br>und Bericht &quot; [Wichtige Attribute&quot;](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) | Updated text in the note at the top of the topics. |
|  | [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Folgende FAQs wurden hinzugefügt:<ul><li>Kann ich die Option &quot;Berichtsdaten zurücksetzen&quot;beim Ausführen einer Aktivität für die automatische Zuordnung verwenden?</li><li>Wie werden Buildmodelle mit automatisierter Zuordnung in Bezug auf Umgebung erstellt?</li></ul> |
|  | [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md) | Folgende Frage wurde hinzugefügt:    <ul><li>Kann ich die Option &quot;Berichtsdaten zurücksetzen&quot;beim Ausführen einer Aktivität für die automatische Zielgruppe verwenden?</li></ul>Der Text im Abschnitt &quot;Überlegungen&quot;wurde aktualisiert. |
|  | [Häufig gestellte Fragen zu Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | Folgende FAQs wurden hinzugefügt:<ul><li>Kann ich beim Ausführen einer Automated Personalization-Aktivität die Option Berichtsdaten zurücksetzen verwenden?</li><li>Wie erstellt Automated Personalization Modelle in Bezug auf Umgebung?</li></ul> |
|  | [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Es wurden Informationen zu Internet Explorer und unbekannten Elementen hinzugefügt. |
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
| Juli 15 | [Auto-Allocate can give you faster test results and higher revenue than a manual test](/help/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md) | Neues Thema |
| Juli 14 | [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md),<br>[Auto-Target](/help/c-activities/auto-target-to-optimize.md),<br>and<br>[Automated Personalization FAQ](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | Added FAQs recommending that you should not change the goal metric midway through an activity. |
| Juli 7 | [Target announcements and events](/help/r-release-notes/target-announcements.md) | Added information about the July 8 Adobe Target Coffee Break. |
| 25. Juni | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Version 20.6.1 von Target Standard/Premium (Juli 2020) hinzugefügt. |
|  | [Target documentation overview](/help/r-release-notes/target-documentation.md) | Neues Thema, in dem die verschiedenen [!DNL Target] Dokumentationsquellen ausführlich beschrieben werden. |
| 23. Juni | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Added information about the June 24 Adobe Target Coffee Break. |
|  | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Added note that creating dependent profile scripts that use the result of one profile script in another profile script is not recommended. |
|  | [Funktionsweise von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Added the following video: Office hours: at.js tips and overview |
| June 17 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das Thema wurde aktualisiert. |
|  | [Antwort-Token](/help/administrating-target/response-tokens.md) | Es wurden Informationen zu Antwort-Token für die Traffic-Zuordnungsmethode für [!UICONTROL Auto-Zielgruppe] - und [!UICONTROL Automated Personalization] -Aktivitäten hinzugefügt. |
|  | [Aktivitätserstellung](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | Es wurden Informationen zur Unterstützung von Analytics for Zielgruppe (A4T) für Aktivitäten mit automatisierter Zuordnung hinzugefügt. |
|  | [Benutzer](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Es wurden Informationen zur neuen [!UICONTROL Herausgeberrolle] unter Rollen und Berechtigungen *festlegen* hinzugefügt. |
|  | [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Added information about the new [!UICONTROL Publisher] role under *Step 6: Specify roles and permissions*. |
|  | [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Added link to the *Office hours: Target Premium Workspaces session*. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.5.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.4.1 (6. Mai 2020) 

| Datum | Thema | Änderungen |
| --- | --- | --- |
| June 15 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Added information about the at.js 1.8.2 and at.js 2.3.1 releases. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den Versionen at.js 1.8.2 und at.js 2.3.1 hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Die Hinweise für die Version [!DNL Target Standard/Premium] 20.5.1 (17. Juni 2020) wurden aktualisiert und enthalten nun Informationen zur Unterstützung von A4T in [!DNL Analysis Workspace]. |
| 12. Juni | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Informationen zur Einstellung `deviceIdLifetime` wurden hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zu den Versionen at.js 1.8.2 und at.js 2.3.1 hinzugefügt. |
| Juni 8 | [Häufig gestellte Fragen zur Zielgruppe von Apps](/help/c-target-mobile-app/target-for-mobile-apps-faq.md) | Text für folgende häufig gestellte Fragen aktualisiert: &quot;Ist Zielgruppe Mobile nur eine Funktion der Adobe Target Premium-Produkt-SKU?&quot; |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Das ganze Thema wurde aktualisiert. |
| Juni 5 | [Ankündigungen und Ereignisse zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target-Kaffeepause vom 10. Juni hinzugefügt. |
|  | [Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md) | Text für folgende häufig gestellte Fragen aktualisiert: &quot;Warum kann ich Steigerung und Konfidenz bei berechneten Metriken nicht sehen?&quot; |
| 4. Juni | [A4T-Reporting](/help/c-integrating-target-with-mac/a4t/reporting.md) | Der Abschnitt &quot;Berichte in Analytics&quot;wurde aktualisiert. |
| Juni 1 | [Mitteilungen zur Zielgruppe](/help/r-release-notes/target-announcements.md) | Es wurde eine neue Seite zur Ankündigung anstehender Ereignis der Zielgruppe hinzugefügt. |
|  | [Mobile Viewports für responsive Erlebnisse](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) | Die Viewport-Dimensionen und -Auflösungen für Apple iPhone 11-, Apple iPhone SE- und Google Pixel 2 XL-Modelle wurden aktualisiert. |
| Mai 28 | [Häufig gestellte Fragen zum Reporting](/help/c-reports/reporting-frequently-asked-questions.md) | Folgende neue Frage wurde hinzugefügt: <ul><li>Wie werden die Metriken &quot;Neue Besucher&quot;und &quot;Wiederkehrende Besucher&quot;gezählt?</li></ul> |
| Mai 27 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Unterstützung von Analytics for Zielgruppe (A4T) für Aktivitäten mit automatisierter Zuordnung hinzugefügt. |
| Mai 26 | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Folgende Informationen wurden hinzugefügt: &quot;Der Parameter bleibt im Profil, nachdem das Skript deaktiviert wurde. Benutzer, deren Profil bereits einen Parameter enthalten, der in der Audience einer Aktivität verwendet wird, sind in dieser Aktivität berechtigt.&quot; |
| Mai 21 | [Zulassungsliste Zielgruppe Edge-Knoten](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Der Liste `mboxedge30.tt.omtrdc.net` hinzugefügt. |
| Mai 20 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur kommenden Target Standard/Premium-Version 20.6.1 (10. Juni 2020) hinzugefügt. |
|  | [Hosts](/help/administrating-target/hosts.md) | Es wurde ein Hinweis zum Abschnitt &quot;Best Practices für die Sicherheit&quot;hinzugefügt. |
| Mai 14 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den Änderungen an der Profil Batch Status API Version 2 hinzugefügt. |
| Mai 13 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Der Abschnitt &quot;Bekannte Einschränkungen&quot;wurde hinzugefügt. |
| Mai 11 | [Hosts](/help/administrating-target/hosts.md) | Es wurden Informationen zur Verwendung der Ubox-Funktion mit Umleitungen und Zulassungslisten hinzugefügt. |
|  | [Arbeiten mit Weiterleitungen](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) | Es wurden Informationen zur Verwendung von Hosts hinzugefügt, um Open-Redirect-Schwachstellen zu vermeiden. |
|  | [Integration von Recommendations in E-Mail](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | Es wurden Informationen zur Verwendung von Hosts hinzugefügt, um Open-Redirect-Schwachstellen zu vermeiden. |
|  | [E-Mail: Target-Implementierung](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md) | Added information about using hosts to avoid Open Redirect Vulnerabilities. |
| Mai 7 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | With the upcoming deprecation of mbox.js on August 30, 2020, David Son, Adobe Target Product Manager recently hosted a developer chat to discuss the benefits of migrating mbox.js to at.js. There is a link where you can watch the webinar for the next 30 days. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Abschnitt &quot;Überlegungen&quot;wurde aktualisiert. |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Die Zeile &quot;overrideMboxEdgeServer&quot;unter &quot;Einstellungen&quot;wurde aktualisiert. |
| Mai 6 | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md) | Es wurden Informationen zu ITP 2.3 hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.4.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.2.1 (19. Februar 2020)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| Mai 4 | [Häufig gestellte Fragen zum Reporting](/help/c-reports/reporting-frequently-asked-questions.md#uneven) | Neue FAQs hinzugefügt: &quot;Warum ist der Traffic zwischen meinen Erlebnissen unterschiedlich, auch in meiner A/B- oder MVT-Aktivität?&quot; |
| April 29 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Bekanntes Problem beim Berichte mit extremen Bestellungen wurde hinzugefügt. |
| April 28 | [Nützliche Variablen, Profile, Parameter und Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Informationen zum Abrufen der IP-Adressen von Benutzern mit `user.header('x-forwarded-for')` neueren AWS-Kanten wurden entfernt. Dieser Befehl funktioniert jetzt mit neueren AWS-Kanten. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Das Datum der Target Standard/Premium-Version (20.4.1) wurde in den 6. Mai geändert. |
| April 23 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das Thema wurde aktualisiert. |
| April 22 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Neuer Abschnitt hinzugefügt: *Änderungen an der Profil Batch-Status-API, Version 2 (4. Mai 2020).* |
| April 20 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Neuer Abschnitt hinzugefügt: *Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets &quot;mbox.js&quot;zu &quot;at.js&quot;.* |
| April 14 | [Zulassungsliste Zielgruppe Edge Hosts](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Neues Thema |
| April 10 | [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp) | Neuer Abschnitt hinzugefügt: &quot;Best Practices für die Implementierung&quot;. |
| April 7 | [Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence) | Der Text für &quot;Warum kann ich Steigerung und Konfidenz bei berechneten Metriken nicht sehen?&quot; wurde aktualisiert. |
| April 2 | [Nützliche Variablen, Profile, Parameter und Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Es wurden Informationen zur Verwendung `user.header('x-forwarded-for')` mit neueren AWS-Kanten zum Abrufen der IP-Adressen von Benutzern hinzugefügt. |
|  | [Aktualisieren von at.js 1.*x* auf at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Folgender Hinweis wurde hinzugefügt:<ul><li>Nach der Installation der ECID-Bibliothek v 4.3.0 + und at.js 2.*x* können Sie Aktivitäten erstellen, die mehrere Domänen umfassen und Benutzer tracken können. Beachten Sie, dass diese Funktion erst nach Ablauf der Sitzung funktioniert.</li></ul> |
| 30. März | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Es wurden bekannte Probleme hinzugefügt, die at.js-Versionen vor at.js 2.2.0 betreffen. Dieses Problem führte dazu, dass Klick-Tracking keine Konvertierungen in Analytics für die Zielgruppe (A4T) meldete, wenn Adobe Analytics-Code nicht in Seitenelementen vorhanden war. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Die folgenden Informationen wurden den Details zu at.js Version 2.2.0 hinzugefügt:<ul><li>Es wurde ein Problem behoben, bei dem Klick-Tracking keine Konversionen in Analytics für Zielgruppe (A4T) meldete, wenn Adobe Analytics-Code nicht in Seitenelementen vorhanden war.</li></ul> |
| 25. März | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den folgenden neuen Versionen von at.js hinzugefügt:<ul><li>at.js version 2.3.0</li><li>at.js Version 1.8.1</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Added the following new rows in the &quot;Settings&quot; section:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>Der folgende neue Abschnitt wurde hinzugefügt:<ul><li>Content Security-Richtlinie</li></ul> |
| 24. März | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact) | Added information about impacts for the following:<ul><li>Profile scripts based on 3rdPartyID</li><li>QA/Preview URLs in iOS devices</li></ul> |
| 20. März | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Indicated that the Target Standard/Premium 20.2.1 release will be March 23, 2020. |
| 13. März | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Udated the number of &quot;Audiences, reusable per account.&quot; |
| 12. März | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md#summit) | Es wurden Informationen zur Registrierung für den freien Zugang zur Online-Konferenz des digitalen Gipfels hinzugefügt. |
| März 9 | [Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) | Es wurden weitere Informationen im Abschnitt &quot;Ersetzen des letzten Oktetts von IP-Adressen&quot;hinzugefügt. |
|  | [Arbeiten mit Attributen mit mehreren Werten](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Codebeispiel in *Übergeben eines Parameters mit mehreren Werten in JavaScript* aktualisiert. |
|  | [Benutzerdefinierte Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md) | Added code sample in *Using APIs* under *Implementing multi-value attributes*. |
| 4. März | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Das gesamte Thema wurde aktualisiert und der Abschnitt &quot;Best Practices&quot;wurde umfassend überarbeitet. |
| February 21 | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Added information about the new Adobe Experience Cloud navigation. |
| February 20 | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Updated the description for the `enabled` setting. Added information for the following settings: `pageLoadEnabled` and `viewsEnabled`. |
| 19. Februar | [Versionshinweise](/help/r-release-notes/release-notes.md) | Added information about the upcoming deprecation of the mbox.js library. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Es wurde ein Hinweis hinzugefügt, der in at.js 1 unterstützt `mboxOverride.browserIp` wird.*x*, zur Verfügung. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurde klargestellt, welche Versionen von &quot;at.js&quot;vom Zielgruppe-Team unterstützt werden. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.2.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 20.1.1 (4. Februar 2020)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| February 4 | [Versionshinweise](/help/r-release-notes/release-notes.md): 20.1.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |
