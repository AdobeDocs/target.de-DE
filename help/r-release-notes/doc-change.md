---
keywords: target documentation change log;documentation updates;new topics;edits
description: Auf dieser Seite werden wichtige Änderungen an der Adobe Target-Dokumentation aufgelistet, die nach Versionen sortiert wurden.
title: Änderungen an der Adobe Target-Produktdokumentation.
topic: Standard
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
translation-type: tm+mt
source-git-commit: 16f2dbeba46ee3d0e180223a8f3be20ca627119b

---


# Dokumentationsänderungen{#documentation-changes}

Auf dieser Seite sind wichtige Änderungen an der [!DNL Adobe Target]-Dokumentation aufgeführt.

## Adobe Target/Standard/Premium 19.10.1 (22. Oktober 2019)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 27. Januar 2020 | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Folgende Informationen wurden hinzugefügt: &quot;Wenn Sie die Batch Delivery API verwenden, beträgt der Grenzwert 50 Mboxes pro Batch-Anforderung.&quot; |
|  | [Ressourcen und Kontaktinformationen](/help/cmp-resources-and-contact-information.md#section_354AC2658BA84A2A96E64C5B2C43B73B) | Link zum Öffnen eines Support-Tickets aktualisiert. |
| 23. Januar 2020 | [Berichte zur automatischen Zuordnung interpretieren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Es wurde ein Hinweis zur Verwendung des Stichprobengrößenrechners von Adobe Target hinzugefügt, um den Gewinner zu ermitteln. |
|  | [Entitätsattribute](/help/c-recommendations/c-products/entity-attributes.md) | Es wurde ein Hinweis hinzugefügt, der erklärt, dass bei Verwendung von at.js 2.*x*, `mboxCreate` wird nicht mehr unterstützt. So geben Sie Produkt- oder Inhaltsinformationen mithilfe von at.js 2 an Recommendations weiter.*x*, verwenden `targetPageParams`. |
| 22. Januar 2020 | [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Folgende häufig gestellte Fragen wurden aktualisiert: &quot;Kann ich den Stichprobengrößenrechner verwenden, wenn ich die automatisierte Zuordnung verwende, um abzuschätzen, wie lange die Aktivität dauern wird, um den Gewinner zu ermitteln?&quot; |
| 15. Januar 2020 | [Zulassen von gemischtem Inhalt in Ihrem Browser](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md) | Es wurde ein Schulungsvideo und eine Anleitung hinzugefügt, die erklären, wie Sie Ihre Site-Einstellungen aktualisieren, um gemischten Inhalt in der neuesten Version von Chrome zuzulassen. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md) | Es wurde ein Hinweis zum Hochladen und Entfernen von Entitäts- und Entitätsattributen hinzugefügt. |
|  | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Folgende häufig gestellte Fragen wurden hinzugefügt:Was bedeutet die Antwort NO_CONTENT manchmal, die im Content Trace von Recommendations zurückgegeben wird? |
|  | [Erstellen einer Mbox für Auftragsbestätigungen – mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md) | Es wurde ein Hinweis hinzugefügt, der erklärt, wie eine Auftragsbestätigung mit at.js 2 durchgeführt wird.*x*. |
| 9. Januar 2020 | [Änderungen der TLS-Verschlüsselung (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Text aktualisiert.<br>Ab dem 1. März 2020 unterstützt Adobe Target keine TLS 1.1-Verschlüsselung mehr für Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), Aktivitätsbereitstellung, APIs usw. Bitte aktualisieren Sie vor dem 1. März 2020 auf TLS 1.2, um Probleme zu vermeiden. |
| 6. Januar 2020 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurde ein bekanntes Problem mit dem Feed-Status Benutzerspezifische Kriterien hinzugefügt. |
| 19. Dezember 2019 | [Versionshinweise - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Es wurden Informationen über Version 1.1.0 hinzugefügt. |
| 12. Dezember 2019 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Abschnitt FAQ aktualisiert. |
|  | [Berichte zur automatischen Zuordnung interpretieren](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Thema umbenannt und der folgende Abschnitt hinzugefügt: &quot;Verstehen Sie die Berichte zu Steigerung und Vertrauen in Aktivitäten mit automatisierter Zuordnung.&quot; |
| 11. Dezember 2019 | [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Neue FAQs hinzugefügt: &quot;Wie bewertet Target URLs beim Targeting?&quot; |
| 10. Dezember 2019 | [Zielbegrenzungen](/help/r-troubleshooting-target/target-limits.md) | Der Abschnitt &quot;mbox-Parameter&quot;wurde aktualisiert. |
|  | [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md) | Es wurde ein Hinweis zur Unterstützung der Funktion Kriterienverwendung hinzugefügt. |
| 5. Dezember 2019 | [Seiten der Site](/help/c-target/c-audiences/c-target-rules/site-pages.md) | Das Thema wurde aktualisiert. |
| 2. Dezember 2019 | [Standortdienst verwenden](/help/c-target-mobile-app/use-location-service.md) | Neues Thema |
| 26. November 2019 | [Verwaltung von Flackern mit „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) | Text in &quot;Verwalten des Flackerns beim asynchronen Laden von at.js&quot;aktualisiert. |
|  | [Target Insider-Newsletter](/help/r-release-notes/target-insider-newsletter.md) | Es wurde ein Link zum Newsletter vom November 2019 hinzugefügt. |
|  | [Benutzer](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Text und Bilder unter &quot;Rollen und Berechtigungen festlegen&quot;wurden aktualisiert. |
| 15. November 2019 | [Zehn häufige A/B-Testfallen und wie sie vermieden werden können](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md) | &quot;Pitfall 7: Änderung der Traffic-Zuordnung während des Testzeitraums.&quot; |
| 11. November 2019 | [Versionshinweise - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Es wurden Informationen über Version 1.0.1 hinzugefügt. |
|  | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das ganze Thema wurde aktualisiert. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md#section_DD308A53AF0F48FA8C81423580561FE7) | Es wurden Informationen hinzugefügt, die erklären, dass Geoinformationen [!DNL Target] nicht gespeichert werden, wie z. B. Postleitzahlen. |
| 8. November 2019 | [Target Insider-Newsletter](/help/r-release-notes/target-insider-newsletter.md) | Es wurden Links zu weiteren Problemen in der Vergangenheit hinzugefügt. |
|  | [Vorschriften zur Privatsphäre und zum Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | CCPA-Abschnitt mit neuer Notiz aktualisiert.<br>Es wurden neue FAQ hinzugefügt, die Kunden darüber informieren, dass Target Kunden nicht die Möglichkeit bietet, Daten direkt von Target an Dritte weiterzugeben oder zu verkaufen. Daher gibt es keine Möglichkeit, den Verkauf für Target abzuwählen. |
| 7. November 2019 | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md#examples) | Codebeispiel für den Parameter adobeQA hinzugefügt. |
| 5. November 2019 | [Site-Seiten](/help/c-target/c-audiences/c-target-rules/site-pages.md#ts) | Der Text im Abschnitt &quot;Fehlerbehebung&quot;wurde aktualisiert. |
| 4. November 2019 | [Häufig gestellte Fragen zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Text unter den folgenden häufig gestellten Fragen aktualisiert: &quot;Warum sehe ich Warnmeldungen wie &quot;Aktionen mit fehlenden Selektoren&quot;?&quot; |
| 31. Oktober 2019 | [Arbeiten mit Attributen mit mehreren Werten](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Neues Thema |
|  | [Versionshinweise - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Neues Thema |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#audience-parameters) | Neuer Abschnitt hinzugefügt: &quot;Welches at.js 1.*x* -Parameter zum Erstellen von Zielgruppen werden in at.js 2 nicht unterstützt.*x*?&quot; |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurde ein neues bekanntes Problem mit zusätzlichen Leerzeichen hinzugefügt, die zu Vorlagenregeln hinzugefügt werden. |
|  | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur Version Target Premium 19.10.2 und zur Target Java SDK-Version hinzugefügt. |
| 30. Oktober 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur kommenden Target Premium-Version 19.10.2 (31. Oktober 2019) hinzugefügt. |
| 29. Oktober 2019 | [Ähnlichkeit von Inhalten](/help/c-recommendations/c-algorithms/create-new-algorithm.md#concept_5402DAFA279C4E46A9A449526889A0CB) | Es wurde ein Hinweis hinzugefügt. |
|  | [Vorschau Ihrer Recommendations-Aktivität anzeigen und starten](/help/c-recommendations/t-create-recs-activity/previewing-and-launching-your-recommendations-activity.md) | Neues Thema |
| 25. Oktober 2019 | [Benutzerdefinierte Parameter](/help/c-target/c-audiences/c-target-rules/custom-parameters.md#considerations) | Es wurde ein neuer Artikel unter &quot;Überlegungen&quot;hinzugefügt, der erklärt, dass Targeting nicht anhand interner Mbox-Parameter bewertet wird. |
|  | [Verwenden dynamischer und statischer Einschlussregeln](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) | Das Thema wurde vollständig aktualisiert und veraltete Beispiele wurden entfernt. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Es wurde ein Hinweis-Link zur Target-Bereitstellungs-API-Dokumentation hinzugefügt, der Ihnen hilft, die verfügbaren Typen für Anforderungen/Antworten (Array, Zeichenfolge usw.) zu verstehen. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Es wurde ein Hinweis-Link zur Target-Bereitstellungs-API-Dokumentation hinzugefügt, der Ihnen hilft, die verfügbaren Typen für Anforderungen/Antworten (Array, Zeichenfolge usw.) zu verstehen. |
|  | [Site-Seiten](/help/c-target/c-audiences/c-target-rules/site-pages.md#ts) | Der Abschnitt &quot;Fehlerbehebung&quot;wurde hinzugefügt. |
| 24. Oktober 2019 | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#section_DB3F40673AED42228E407C05437D99E9) | Text in den folgenden häufig gestellten Fragen aktualisiert: &quot;Warum kann Target manchmal keine Empfehlungen anzeigen?&quot; |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Es wurde ein Hinweis zu einem bekannten Problem hinzugefügt, das ältere Versionen von at.js betrifft (früher als Version 2.2.0). |
|  | [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md) | Es wurde ein Hinweis zum Standardverhalten von Erfolgsmetriken für Aktivitäten mit A4T hinzugefügt. |
| 22. Oktober 2019 | [Kriterien/Algorithmen ](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms) | Zeile für benutzerbasierte Empfehlungen hinzugefügt. |
|  | [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md#custom-key) | Neuer Abschnitt hinzugefügt: &quot;Verwenden eines benutzerdefinierten Empfehlungsschlüssels.&quot; |
|  | [Häufig gestellte Fragen zu Target und Zielgruppen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Neue FAQs hinzugefügt: &quot;Wird beim Erstellen komplexer URL-Zeichenfolgen die gesamte URL ausgewertet [!DNL Target] ?&quot; |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.10.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target/Standard/Premium 19.9.1 (30. September 2019)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 17. Oktober 2019 | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Thema aktualisiert, um zu erläutern, wie Activity QA mit Drittanbieter-Cookies funktioniert. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Die Versionshinweise wurden aktualisiert und enthalten nun Informationen zu Änderungen an der einheitlichen Shell. |
| 10. Oktober 2019 | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state) | Neuer Abschnitt hinzugefügt: &quot;serverState&quot;. |
|  | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den Versionen at.js 2.2 und at.js 1.8 hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den Versionen at.js 2.2 und at.js 1.8 hinzugefügt. |
|  | [Fehlerbehebung bei Aktivitäten](/help/c-activities/c-troubleshooting-activities/troubleshooting-activities.md) | Neuer Abschnitt hinzugefügt: &quot;Ich habe eine Aktivität mit der Target-Benutzeroberfläche erstellt und kann sie nicht über die API aktualisieren.&quot; |
| 9. Oktober 2019 | [Server-seitig: Target-Implementierung](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Das Thema wurde aktualisiert. |
|  | [Versionshinweise - Target-serverseitige APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Neues Thema |
|  | [Versionshinweise - SDK für Target Node.js](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Neues Thema |
|  | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den Versionen V1/Delivery API und Node.js SDK hinzugefügt. |
| 8. Oktober 2019 | [Target Insider-Newsletter](/help/r-release-notes/target-insider-newsletter.md) | Neues Thema mit Links zum ersten Stapel von Newslettern, mit weiteren Informationen. |
| 3. Oktober 2019 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurde Folgendes hinzugefügt: <ul><li>Bekanntes Problem und Problemumgehung beim Erstellen eines Erlebnisses ohne Änderungen mit at.js 2.*x* -Bibliothek.</li><li>Sammlungen, Ausschlüsse, Kriterien und Designs, die über API erstellt wurden, sind in der Benutzeroberfläche von Target nicht sichtbar und können nur über API bearbeitet werden.</li><li>Recommendations-Aktivitäten, die über API erstellt wurden, können in der Benutzeroberfläche angezeigt werden, können aber nur über API bearbeitet werden.</li></ul> |
|  | [Fehlerbehebung bei der Inhaltsbereitstellung](/help/c-activities/c-troubleshooting-activities/content-trouble.md#mboxdebug) | Hinweis zum Abschnitt &quot;mboxDebug&quot;hinzugefügt. |
| 2. Oktober 2029 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zu kommenden Versionen hinzugefügt. |
| 1. Oktober 2019 | [Nützliche Variablen, Profile, Parameter und Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Der Text im Abschnitt &quot;Kundenattribute&quot;wurde aktualisiert. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Codebeispiel im Abschnitt &quot;Aufruf von getOffers() für alle Ansichten&quot;aktualisiert. |
| 30. September 2019 | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.9.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.7.1 (23. Juli 2019) {#tgt-19-7-1}

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 27. September 2019 | [Wie lange sollten A/B-Tests laufen?](/help/c-activities/t-test-ab/sample-size-determination.md) | Der Text zum Stichprobengrößenrechner von Target wurde aktualisiert. |
|  | [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Der Text zum Stichprobengrößenrechner von Target wurde aktualisiert. |
| 24. September 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Das Datum der Target/Standard-Version 19.2.1 wurde auf den 30. September 2019 geändert. |
|  | [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md) | Ein Schulungsvideo wurde hinzugefügt. |
| 10. September 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur Version Target Standard/Premium 19.9.1 hinzugefügt. |
| 9. September 2019 | [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md#considerations) | Abschnitt &quot;Überlegungen&quot;hinzugefügt. |
|  | [SameSite-Cookie-Richtlinien von Google Chrome](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) | Der Text für das gesamte Thema wurde aktualisiert. |
|  | [Content Security Policy (CSP)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/content-security-policy.md) | Neues Thema |
| 6. September 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur Version Target Standard/Premium 19.9.1 (10. September 2019) hinzugefügt. |
|  | [Häufig gestellte Fragen zu Target für mobile Apps](/help/c-target-mobile-app/target-for-mobile-apps-faq.md) | Neues Thema |
| 4. September 2019 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das Thema wurde aktualisiert. |
| 23. August 2019 | [Mobile Target-Vorschau](/help/c-target-mobile-app/target-mobile-preview.md) | Aktualisiertes Code-Snippet in `AndroidManifest.xml`. |
| 22. August 2019 | [Visual Experience Composer für mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) | Informationen zur Verwendung unzulässiger Zeichen in App-IDs wurden entfernt. Es gibt keine Einschränkungen mehr. |
|  | [Benutzerdefinierte Parameter](/help/c-target/c-audiences/c-target-rules/custom-parameters.md#considerations) | Neuer Abschnitt wurde hinzugefügt: „Zu beachten“ |
|  | [Hochladen benutzerdefinierter Kriterien](/help/c-recommendations/c-algorithms/recommendations-csv.md) | Folgender Satz wurde aktualisiert: Benutzerspezifische Kriterienupdates sind standardmäßig kumulativ. Neue Schlüssel-Wert-Paare, die in der CSV-Uploaddatei angegeben werden, überschreiben bestehende Schlüssel-Wert-Paare. Vorhandene Schlüssel-Wert-Paare, für die keine Schlüssel im CSV-Upload spezifiziert ist, können trotzdem bereitgestellt werden und laufen 31 Tagen nach dem letzten Hochladen als Teil der CSV-Datei ab. |
| 20. August 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Die Veröffentlichung der Target/Premium 19.8.1-Version (20. August 2019) wurde verschoben. Inhalte aus dieser Version werden in Version 19.9.1 (24. September 2019) bereitgestellt. |
|  | [Häufig gestellte Fragen: Entwürfe](/help/c-recommendations/c-design-overview/template-faq.md) | Folgende FAQ wurden hinzugefügt: „Der Preis meines empfohlenen Artikels zeigt nicht beide Ziffern rechts vom Dezimalzeichen an. Wie kann ich sie anzeigen?“ |
| 16. August 2019 | [Echtzeit-Profilsynchronisierung für mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md) | Neuer Abschnitt wurde hinzugefügt: „Zu beachten“ |
|  | [Erstellen einer Recommendations-Aktivität](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md) | Eine Schulungsvideos wurden hinzugefügt. |
|  | [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [Hochladen benutzerdefinierter Kriterien](/help/c-recommendations/c-algorithms/recommendations-csv.md) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [Erstellen von Kriteriensequenzen](/help/c-recommendations/c-algorithms/create-criteria-sequence.md) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [Erstellen eines Designs](/help/c-recommendations/c-design-overview/create-design.md) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [Sammlungen](/help/c-recommendations/c-products/collections.md) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [Ausnahmen](/help/c-recommendations/c-products/exclusions.md) | Ein Schulungsvideo wurde hinzugefügt. |
| 14. August 2019 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Text wurde aktualisiert und ein Schulungsvideo-Link wurde hinzugefügt. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Informationen zum `consumerID`-Schlüssel wurden erläutert. |
|  | [Visual Experience Composer – Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#move) | Die Informationen im Abschnitt „Layout > Verschieben“ wurden aktualisiert. |
| 12. August 2019 | [Android – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#sdk-library) | Informationen zu Abhängigkeiten und Artefakten wurden aktualisiert.<br>Das Codebeispiel für die `AndroidManifest.XML`-Datei wurde aktualisiert. |
|  | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Die Liste der Verbesserungen und Fehlerbehebungen im Abschnitt „Target Mobile VEC SDK iOS 2.1.0 &amp; Android 1.1.1“ wurde aktualisiert. |
|  | [Bearbeiten einer Aktivität oder Speichern als Entwurf](/help/c-activities/edit-activity.md#classic) | Neuer Abschnitt wurde hinzugefügt: „Verwendung älterer Aktivitäten, die in Recommendations Classic erstellt wurden“. |
| 9. August 2019 | [Funktionsweise von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render) | Neuer Abschnitt hinzugefügt: „Darstellung von Angeboten mit HTML-Inhalten durch at.js“. |
|  | [Visual Experience Composer – Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#considerations) | Neuer Abschnitt wurde hinzugefügt: „Zu beachten“ |
| 7. August 2019 | [Vorabruf des Angebotsinhalts](/help/c-target-mobile-app/prefetch-offer-content.md) | Ein Hinweis wurde hinzugefügt, dass die Vorabruffunktion in den SDKs nicht für die Aktivitätstypen „Automatisches Targeting“, „Automatisierte Zuordnung“ und „Automatisierte Personalisierung“ unterstützt wird. |
|  | [Fehlerbehebung bei der Analytics- und Target-Integration (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md#unspecified) | Ein Hinweis wurde aktualisiert, sodass jetzt angegeben wird, wie lange der Klassifizierungsprozess dauert. |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#unspecified) | Ein Hinweis wurde aktualisiert, sodass jetzt angegeben wird, wie lange der Klassifizierungsprozess dauert. |
|  | [Vorschriften zur Privatsphäre und zum Datenschutz](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Das Thema wurde aktualisiert und enthält jetzt auch Informationen zum California Consumer Privacy Act (CCPA). |
| 6. August 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Versionshinweise für Target Mobile VEC SDK iOS 2.1.0 und Android 1.1.0 wurden hinzugefügt. |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#metrics) | Informationen zur Verwendung der Metriken [!UICONTROL Aktivitätsimpressionen] und [!UICONTROL Aktivitätskonversionen] in [!DNL Analysis Workspace] wurden aktualisiert. |
| 1. August 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Eine wichtige Mitteilung zur API-Unterstützung für Enterprise-Berechtigungen wurde hinzugefügt. |
|  | [Zugriff von Adobe I/O Integrationen auf Arbeitsbereiche gewähren und Rollen zuweisen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md) | Neues Thema |
| 31. Juli 2019 | [Einführung in Recommendations](/help/c-recommendations/introduction-to-recommendations.md) | Neues Thema |
|  | [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md#recently-viewed) | Ein Hinweis zu kürzlich angezeigten Artikeln wurde hinzugefügt. |
|  | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#preview) | Informationen zu einem bekannten Problem mit Vorschaulinks für Aktivitäts-QAs wurden hinzugefügt. |
| 29. Juli 2019 | [Häufig gestellte Fragen zum Reporting](/help/c-reports/reporting-frequently-asked-questions.md) | Neue FAQ wurde hinzugefügt: „Warum enthalten meine [!UICONTROL Erlebnis-Targeting] (XT)-Berichte Metriken für Kontrollerlebnisse?“ |
| 24. Juli 2019 | [Aktualisieren von at.js 1.*x* auf at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Neuer Abschnitt wurde hinzugefügt: [Unterstützung von domänenübergreifendem Tracking in at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain) |
|  | [Apple Intelligent Tracking Prevention (ITP) 2.*x*](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)  | Neues Thema |
|  | [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md#status) | Neuer Abschnitt wurde hinzugefügt: „Status des Recommendations-Angebots anzeigen“. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md) | Die Zeile „Elemente werden importiert“ wurde aktualisiert und die Zeile „Feed erfolgreich importiert um *Zeit*“ unter [Feed-Status](/help/c-recommendations/c-products/feeds.md#status) wurde hinzugefügt. |
|  | [Katalogsuche](/help/c-recommendations/c-products/catalog-search.md) | Der Text zur Aktualisierung des Katalogs wurde aktualisiert. |
|  | [Einrichten des Klick-Trackings in der Mobile App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md) | Informationen zum Bedienfeld „Änderungen“ wurden hinzugefügt, in dem die von Ihnen für Klick-Tracking eingerichteten Elemente angezeigt werden. |
|  | [Funktionsweise von Adobe Target](/help/c-intro/how-target-works.md#bots) | Neuer Abschnitt wurde hinzugefügt: „Bots“ |
|  | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md#best) | Best Practices wurden hinzugefügt, um eine langsame Regex-Ausführung zu vermeiden. |
|  | [Visual Experience Composer für Mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#ts) | Der Fehlerbehebungsabschnitt wurde mit einem Hinweis aktualisiert, dass die Zeicheneinschränkungen nicht mehr für App-Namen gelten. Die Einschränkungen gelten nur für IDs. |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md#steps) | Zu den Schritten wurden unterstützte FTP-Servereinstellungen hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informationen zur at.js-Version 2.1.1 wurden hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.7.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.6.1 (26. Juni 2019) {#tgt-19-6-1}

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 10. Juli 2019 | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Für die folgenden Elemente wurden Beschränkungsinformationen hinzugefügt:<ul><li>Anzahl der Erlebnisse pro Aktivität</li><li>Anzahl der Erfolgsmetriken pro Aktivität</li><li>Anzahl der Berichtszielgruppen/Segmente pro Aktivität</li><li>Anzahl der Zielgruppen pro Mbox, Metrik und Erlebnis</li><li>Anzahl eindeutiger Werte pro Targeting-Regel</li><li>Anzahl eindeutiger Zielgruppen pro Targeting-Regel</li><li>Anzahl eindeutiger Targeting-Regeln pro Aktivität</li><li>Anzahl der aktiven Profilskripte</li><li>Anzahl der Profilskripte</li><li>Anzahl der Gesamtschleifen pro Profilskript</li><li>Anzahl der aktiven Aktivitäten</li><li>Anzahl der aktiven (und nicht beendeten) Aktivitäten</li><li>Anzahl der Properties</li><li>Anzahl der Angebote</li></ul> |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur kommenden Target-Version 19.7.1 hinzugefügt (23. Juli 2019).<br>Diese Informationen können sich ändern. |
| 8. Juli 2019 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Es wurden Informationen hinzugefügt, in denen erklärt wird, warum CNAME verwendet werden sollte. |
| 28. Juni 2019 | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#redirect)<br>[Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md)<br>[Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Es wurden Informationen zu einem bekannten Problem hinzugefügt, bei dem einer begrenzten Anzahl von Kunden mit Redirects mit A4T ein höherer Prozentsatz an aufgetrennten Treffern angezeigt wird. |
| 26. Juni 2019 | [Visual Experience-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) | Es wurden Informationen über die [!UICONTROL Hintergrund]-Option unter *Stile* hinzugefügt. |
|  | [Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)](/help/c-experiences/spa-visual-experience-composer.md) | Es wurden Informationen über die Aktion [!UICONTROL Klonen] hinzugefügt. |
|  | [Klick-Tracking](/help/c-activities/r-success-metrics/click-tracking.md) | Es wurden Informationen zum Bedienfeld [!UICONTROL Ausgewählte Elemente] hinzugefügt. |
|  | [Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings) | Neuer Abschnitt: Einstellungen für die Seitenbereitstellung für den SPA-VEC |
|  | [Auswahl des Kontrollelements für die automatisierte Personalisierung oder die automatische Targeting-Aktivität](/help/c-activities/t-automated-personalization/experience-as-control.md) | Neues Thema |
|  | [SameSite-Cookie-Richtlinien von Google Chrome](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) | Neues Thema |
|  | [Datenerfassung für die Target-Personalisierungsalgorithmen](/help/c-activities/t-automated-personalization/ap-data.md) | Neue Tabellen wurden hinzugefügt, um einzelne Attribute zu erklären und Beispiele anzugeben. |
|  | [Häufig gestellte Fragen zur automatisierten Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | Neuer FAQ-Abschnitt wurde hinzugefügt: Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?<br>Dieser FAQ-Abschnitt wurde überarbeitet: Mithilfe welcher Best Practices kann ich eine Aktivität vom Typ „Automatisierte Personalisierung“ einrichten? |
|  | [Automatisches Targeting](/help/c-activities/auto-target-to-optimize.md) | Es wurden Informationen und häufig gestellte Fragen hinzugefügt, in denen erläutert wird, wie ein spezifisches Erlebnis als Kontrolle spezifiziert wird.<br>Der Abschnitt „Bestimmen der Traffic-Zuordnung“ wurde aktualisiert. |
|  | [Erstellen einer Automated Personalization-Aktivität](/help/c-activities/t-automated-personalization/create-ap-activity.md) | Es wurde ein Schritt mit Informationen hinzugefügt, in dem ein bestimmtes Erlebnis als Standarderlebnis ausgewählt werden kann. |
|  | [Visual Experience Composer für Mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) | Es wurden Informationen zur Verwaltung mehrerer App-Versionen hinzugefügt. |
|  | [Bekannte gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurden Informationen zu Berichten hinzugefügt, die in manchen Situationen bei Aktivitäten mit automatischem Targeting nicht gerendert werden können. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.6.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.5.1 (21. Mai 2019) {#tgt-19-5-1}

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 19. Juni 2019 | [Hinzufügen von Promotions](/help/c-recommendations/t-create-recs-activity/adding-promotions.md) | Es wurden Informationen hinzugefügt, in denen erläutert wird, dass Werbeaktionen in Bezug auf Produkte dedupliziert werden, die von den Kriterien für Ihre Aktivität empfohlen werden. |
| 13. Juni 2019 | [Bericht „Wichtige Attribute“](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) | Ein neuer FAQ-Abschnitt wurde hinzugefügt: Warum erhalten in einem bestimmten automatisierten Segment manche Angebote/Erlebnisse mit einer geringeren Konversionsrate mehr Traffic als andere Angebote/Erlebnisse? |
|  | [Funktionsweise von Adobe Target](/help/c-intro/how-target-works.md) | Ein wichtiger Hinweis zur Verwendung von Target in China wurde hinzugefügt. |
|  | [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Microsoft Internet Explorer 11 (IE 11) wurde aus dem Abschnitt zur Benutzeroberfläche von Target Standard/Premium entfernt. Target unterstützt nicht mehr IE 11 und ist nicht mehr damit kompatibel. Diese Änderung betrifft nur die Target-Benutzeroberfläche. Die Inhaltsbereitstellung ist nicht betroffen. Ähnliche Mitteilungen waren schon zu Adobe Analytics, Adobe Experience Platform und Adobe Audience Manager veröffentlicht worden. Wir empfehlen Benutzern, zu einem unterstützten Browser zu wechseln. |
| 11. Juni 2019 | [Aktivitätserstellung](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | Es wurde ein Hinweis entfernt, der erklärte, dass es nicht nötig ist, einen Tracking-Server anzugeben, wenn Sie A4T verwenden. |
|  | [Aktivitäten](/help/c-activities/activities.md) | Es wurde erklärt, dass gelöschte Aktivitäten nicht wiederhergestellt werden können. Als Best Practice können Sie eine Aktivität archivieren und bei Bedarf wieder aus dem Archiv holen. |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Die Einschränkung wurde entfernt, in der erklärt wurde, dass der Experience Cloud-Debugger in at.js 2.x nicht vollständig unterstützt wird. |
| 7. Juni 2019 | [Anpassen eines Designs mithilfe von Velocity](/help/c-recommendations/c-design-overview/customizing-a-template.md#default) | Ein neuer Abschnitt wurde hinzugefügt: Szenario: Erstellen Sie ein standardmäßiges Recommendations-Design von 4 x 2 mit Null-Prüfungen. |
|  | [Schulungsvideos für Adobe Target Standard und Premium](/help/c-intro/target-standard-premium-training-videos.md#tutorials) | Der Link zur neuen Tutorials-Site von Adobe Target wurde aktualisiert. |
|  | [iOS – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md) | Text und Codefragmente wurden aktualisiert. |
| 6. Juni 2019 | [adobe.target.triggerView (viewName, options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) | Die Beschreibung des `options > page`-Parameters wurde aktualisiert. |
|  | [Erste Schritte für Administratoren](/help/administrating-target/start-target.md) | Der gesamte Artikel wurde aktualisiert. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden vorläufige Versionshinweise für die Target-Version 19.6.1 hinzugefügt. |
| 5. Juni 2019 | [Visual Experience Composer für Mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) | Es wurde ein neuer [Abschnitt zur Fehlerbehebung](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#ts) hinzugefügt. |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Es wurden Informationen zur Implementierung von at.js mithilfe von Adobe Launch (die bevorzugte Methode zur Implementierung) aktualisiert. |
|  | [Wichtige Target-Konzepte](/help/c-intro/target-key-concepts.md) | Kleinere Textänderungen. |
| 3. Juni 2019 | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zur kommenden Version von at.js 2.1.0 hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zur kommenden Version von at.js 2.1.0 hinzugefügt. |
|  | [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md) | Ein neuer Abschnitt wurde hinzugefügt: Clientseitige Analytics-Protokollierung |
|  | [Implementieren von Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) | Schritt 7 wurde überarbeitet. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Der Tabelle wurden für die folgenden Feldnamen Zeilen hinzugefügt:<ul><li>Request > experienceCloud</li><li>Request > experienceCloud > analytics</li><li>Request > experienceCloud > analytics > logging</li></ul> |
|  | [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | Zur Tabelle für `adobe.target.sendNotifications(options)` wurde eine Zeile hinzugefügt. |
|  | [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md) | Neues Thema |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#integrations) | Es wurden Informationen über die Unterstützung von Adobe Opt-in in at.js 2.1.0 hinzugefügt. |
|  | [Privatsphäre und Datenschutz-Grundverordnung](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Die Informationen über die Unterstützung von Opt-in at.js 2.1.0 wurden aktualisiert. |
| 31. Mai 2019 | [Mobile](/help/c-target/c-audiences/c-target-rules/mobile.md) | Es wurde ein Hinweis zum Targeting von Geräten mit iOS 12.2 hinzugefügt. |
|  | [Planen und Implementieren von Recommendations](/help/c-recommendations/plan-implement.md) | Das Codebeispiel wurde aktualisiert. |
| 30. Mai 2019 | [Zugriff auf Target über Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md#doc-lang) | Die Dokumentation ist jetzt in vereinfachtem Chinesisch verfügbar. |
|  | [Herunterladen von Daten in Form einer CSV-Datei](/help/c-reports/downloading-data-in-csv-file.md) | Neue Einschränkungen wurden im Abschnitt „Bestelldetails als CSV exportieren“ hinzugefügt: In der Reporting-Benutzeroberfläche von Target angewendete Zielgruppen werden nicht in den Download-Bericht übertragen. |
|  | [Berichtseinstellungen](/help/c-reports/c-report-settings/report-settings.md) | Screenshots wurden aktualisiert. |
| 29. Mai 2019 | [Kategorieaffinität](/help/c-target/c-visitor-profile/category-affinity.md) | Der Text wurde aktualisiert, um den Unterschied zwischen `user.categoryId` und `entity.categoryId` zu verdeutlichen. |
|  | [Migration von „mbox.js“ zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md) | Ein Abschnitt zu diesem Thema wurde neu positioniert: Die Vorteile von at.js. |
|  | [Häufig gestellte Fragen zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Ein Abschnitt zu diesem Thema wurde neu positioniert: Wie wirken sich at.js und mbox.js auf Seitenladezeiten aus? |
|  | [Übergeben dynamischer Daten an Angebote](/help/c-experiences/c-manage-content/passing-profile-attributes-to-the-html-offer.md) | Die Syntax in der Zeile „Vergangenes Verhalten“ wurde korrigiert. |
| 28. Mai 2019 | [Zugriff auf Target über Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md#doc-lang) | Ein neuer Abschnitt wurde hinzugefügt: „Ändern der Sprache für die Target-Produktdokumentation“. |
|  | [Ermitteln eines Gewinners](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Die Informationen zu P-Werten wurden aktualisiert. |
|  | [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) | Ein Fehlerbehebungsabschnitt wurde hinzugefügt, der erklärt, wie Target mehrere Ebenen von iFrames handhabt. |
|  | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Ein neuer FAQ-Abschnitt wurde hinzugefügt: Wie lange dauert das Aufrufen von Recommendations? |
|  | [Implementieren von Target mit Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) | Die Informationen unter dem Abschnitt „Vorteile der Implementierung von at.js mit der Target-Launch-Erweiterung“ wurden aktualisiert. |
|  | [Fehlerbehebung bei der Inhaltsbereitstellung](/help/c-activities/c-troubleshooting-activities/content-trouble.md) | Ein neuer Fehlerbehebungsabschnitt wurde hinzugefügt, in dem erklärt wird, dass at.js keine Mboxes auslöst, wenn ein ungültiger Dokumenttyp verwendet wird. |
| 24. Mai 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen über die at.js-Version 2.1.0 hinzugefügt. |
| 23. Mai 2019 | [Verwalten von Ausschlüssen](/help/c-activities/t-automated-personalization/managing-exclusions.md) | Informationen und ein Link wurden hinzugefügt, in denen beschrieben wird, wie mithilfe von Targeting-Regeln eingeschränkt werden kann, welche Zielgruppen bestimmte Angebote in AP-Aktivitäten sehen können. |
|  | [Server-seitig: Target-Implementierung](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Erlebnisse und Angebote](/help/c-experiences/experiences.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Zielgruppen](/help/c-target/target.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Berichte](/help/c-reports/reports.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Visual Experience Composer (VEC)](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Der Text in der Einführung wurde aktualisiert. |
|  | [Glossar](/help/c-intro/glossary.md) | Mehrere Einträge wurden hinzugefügt und aktualisiert. |
| 22. Mai 2019 | [Visual Experience Composer für Mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#video) | Ein Schulungsvideo wurde hinzugefügt. |
|  | [iOS – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md#tutorial) | Links zu neuen Tutorials wurden hinzugefügt:<ul><li>Implementieren von Experience Cloud in mobile Objective-C-Anwendungen unter iOS</li><li>Implementieren von Experience Cloud in mobile Swift-Anwendungen unter iOS</li></ul> |
|  | [Android – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#tutorial) | Ein Link zum neuen Tutorial wurde hinzugefügt:<ul><li>Implementieren der Experience Cloud in Android-Apps</li></ul> |
|  | [Einführung in Target](/help/c-intro/intro.md#kit) | Ein Link wurde zum Adobe Target Welcome Kit hinzugefügt. |
| 21. Mai 2019 | [Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)](/help/c-experiences/spa-visual-experience-composer.md) | <ul><li>Die Informationen zur Option „Verschieben“ wurden aktualisiert.</li><li>Ein Hinweis wurde hinzugefügt, dass Sie zahlreiche Aktionen ausführen können, bevor die Seite im VEC geladen wird, oder selbst dann, wenn die Seite gar nicht geladen werden kann. </li></ul> |
|  | [Benutzer](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Text und Bilder wurden aktualisiert und ein Schulungsvideo wurde hinzugefügt. |
|  | [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Text und Bilder wurden aktualisiert. |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Die Zeichenbeschränkung für die Kundenattribut-Alias-ID wurde hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.5.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.4.2 (30. April 2019) {#target-19-4-2}

**Hinweis**: Die Target Standard/Premium 19.4.1-Version war eine grundlegende Version, um die Adobe Experience Cloud-Benutzeroberfläche zu aktualisieren und so Marken- und Produktänderungen widerzuspiegeln.

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 15. Mai 2019 | [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#triggerview) | Es wurde ein Hinweis hinzugefügt, dass Sie die `at-view-start`-Ereignisse und `at-view-end`-Ereignisse auslösen müssen. |
| 14. Mai 2019 | [Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md),<br>[Android - Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md),<br>[ios - Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md), <br>[Einrichten des Klick-Trackings im Mobile VEC](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md) | Neue Themen |
|  | [Übergeben dynamischer Daten in Angebote](/help/c-experiences/c-manage-content/passing-profile-attributes-to-the-html-offer.md) | Text aktualisiert. |
| 13. Mai 2019 | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Es wurde ein Element zur Überlegungen zur Verwendung von QA-Modus in einer mehrseitigen Aktivität hinzugefügt. |
|  | [Gleiches Erlebnis auf ähnlichen Seiten](/help/c-experiences/c-visual-experience-composer/temtest.md) | Die Schritte wurden aktualisiert, um sie an die Benutzeroberfläche anzupassen. |
|  | [Häufig gestellte Fragen zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Neue FAQ hinzugefügt: „Welchen HTML-Doctype benötigt at.js?“ |
| 10. Mai 2019 | [Voreinstellungen](/help/administrating-target/r-target-account-preferences/target-account-preferences.md) | Text und Abbildung aktualisiert. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Text aktualisiert. |
| 9. Mai 2019 | [A4T-Reporting](/help/c-integrating-target-with-mac/a4t/reporting.md#reports-in-analysis-workspace) | Neuer Abschnitt hinzugefügt: „Berichte im Analysis Workspace“ |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Neue FAQ hinzugefügt: „Kann ich meine Target-Aktivitätsdaten im Adobe Analysis Workspace anzeigen?“ |
|  | [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md#faqs) | Neue FAQ hinzugefügt: „Werden Click-Track-Konversionen aufgezeichnet, wenn eine Umleitungsseite und die Aktivitäts-URL zu unterschiedlichen Eigenschaften gehören?“ |
| 8. Mai 2019 | [Schulungsvideos für Adobe Target Standard und Premium](/help/c-intro/target-standard-premium-training-videos.md) | Inhalt und Links wurden aktualisiert. |
|  | [Entitätsattribute](/help/c-recommendations/c-products/entity-attributes.md) | Der Text in der Notiz unter der `entity.id`-Variablen wurde aktualisiert. |
| 1. Mai 2019 | [Entitätsattribute](/help/c-recommendations/c-products/entity-attributes.md) | Die Groß-/Kleinschreibung wurde in den folgenden Variablennamen korrigiert:<br>Geändert von `pageURL` zu `pageUrl`.<br>Geändert von `thumbnailURL` zu `thumbnailUrl`. |
| 30. April 2019 | [Visual Experience Composer–Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | <ul><li>Neuer Abschnitt hinzugefügt: „Stile“</li><li>Es wurde eine Tabelle mit HTML5-Tags hinzugefügt, die verschachtelt werden können.</li></ul> |
|  | [Klick-Tracking](/help/c-activities/r-success-metrics/click-tracking.md) | Es wurden Informationen über die DOM-Pfad-Funktion zum Abschnitt „Erwägungen“ hinzugefügt. |
|  | [Feed-Status und Indikatoren](/help/c-recommendations/c-products/feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537) | Die Tabelle „Feed-Status“ wurde aktualisiert. |
|  | [Arbeiten mit Inhalten in der Bibliothek](/help/c-experiences/c-manage-content/assets-working.md) | Es wurden Informationen zum Löschen von Ordnern und Bildern aus der Asset-Bibliothek hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.4.2 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.3.1 (29. März 2019) {#section-19-3-1}

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 29. April 2019 | [Berechtigungen für Unternehmensbenutzer](/help/administrating-target/c-user-management/property-channel/property-channel.md#section_31D3450ADEAE4A29963A34F8E8C19FE0) | Folgende FAQ wurden hinzugefügt: „Warum erhalte ich eine Fehlermeldung, dass keine Eigenschaft mit dieser Aktivität verbunden ist, auch wenn eine Eigenschaft zugewiesen ist?“ |
| 24. April 2019 | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#types) | Es wurde ein Hinweis zu „Aktivitätstypen“ hinzugefügt. |
|  | [Testen einer E-Mail-Bild-AdBox](/help/c-implementing-target/c-non-javascript-based-implementation/testing-email-image-adbox.md) | Das Codebeispiel wurde neu formatiert. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Kleinere Tippfehler korrigiert. |
| 23. April 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Aktualisierte Versionshinweise und Änderungsdatum bis zum 30. April (am 29. April). |
| 22. April 2019 | [Zugriff auf Target über Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md) | Neuer Abschnitt hinzugefügt: „Ändern der Standardsprache für die Target-Benutzeroberfläche“. |
| 19. April 2019 | [Bericht „Automatisierte Segmente“](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md#section_740910A52FA646B4AC9452F98C2F5719) | Neue FAQ hinzugefügt: „Gibt es eine Logik zur Reihenfolge, in der Attribute in einer Segmentkarte angezeigt werden?“ |
|  | [Feeds](/help/c-recommendations/c-products/feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537) | Aktualisierung eines wichtigen Hinweises, der beschreibt, wann hochgeladene Entitäten ablaufen. |
| 16. April 2019 | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Neue FAQ hinzugefügt: „Kann ich den Prozentsatz der Traffic-Zuordnung in einer Aktivität ändern, die nach der Aktivierung der Aktivität A4T verwendet?“ |
| 15. April 2019 | [Erste Bereitstellung – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-initial-provisioning.md) | Neue FAQ hinzugefügt: „Wie kann ich eine mehrseitige A4T-Aktivität einrichten?“ |
|  | [Anforderungen hinsichtlich Benutzerberechtigungen](/help/c-integrating-target-with-mac/a4t/account-reqs.md) | Das Thema wurde aktualisiert. |
|  | [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Bekannte Probleme für Ausschlussgruppen wurden in die Tabelle der gelösten Probleme verschoben. |
| 11. April 2019 | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Codebeispiele wurden aktualisiert. |
|  | [Visual Experience Composer Helper-Erweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Screenshots wurden hinzugefügt. |
|  | [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Folgende FAQ wurde hinzugefügt: „Sollte ich ein leistungsschwaches Erlebnis aus einer automatisierten Zuordnung entfernen, um einen Gewinner zu bestimmen?“ |
| 10. April 2019 | [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md) | Kleinere Textaktualisierungen im Abschnitt „Implementierungsanforderungen“ (Anforderungen wurden neu sortiert). |
|  | [adobe.target.triggerView (viewName, options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) | Der Text für den Parameter „options > page“ wurde aktualisiert. |
| 8. April 2019 | [Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md) | [Erwartete Datenabweichungen bei der Nichtverwendung von A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md#expected-using-a4t) wurde aktualisiert. |
|  | [Minimieren überhöhter Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md) | Informationen zu A4T und Umleitungen unter [Was trägt zu partiellen Daten bei?](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#section_C9C906BEAA7D44DAB9D3C03932A2FEB8) wurden aktualisiert. |
|  | [Vor der Implementierung](/help/c-integrating-target-with-mac/a4t/before-implement.md#section_A0D2EF18033D4C3997B08A6EBB34C17A) | Die Mininum-Anforderungen für die Verwendung von A4T mit Umleitungen (at.js Version 1.6.2) wurden aktualisiert. |
|  | [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58) | <ul><li>Die Mininum-Anforderungen für die Verwendung von A4T mit Umleitungen (at.js Version 1.6.2) wurden aktualisiert.</li><li>Es wurden Informationen hinzugefügt, die beschreiben, wie Datenmetriken gezählt werden, wenn ein Target-Treffer auftritt, jedoch keine Analytics-Treffer auftreten. </li> |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md#excludedid) | Es wurden Informationen zu den Beschränkungen für den `excludedIDs`-mbox-Parameter hinzugefügt. |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#response-tokens) | Neuer Abschnitt hinzugefügt: Antwort-Token. |
| 5. April 2019 | [Adobe Target Basics Webinar: Einführung in Recommendations](/help/c-recommendations/recommendations.md#intro-to-recs) | Link zur Webinar-Aufzeichnung „Einführung in Recommendations“ hinzugefügt. |
|  | [Lesezeichenliste für Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa-bookmark.md) | Der JavaScript-Code für das Aktivitäts-QA-Lesezeichen wurde aktualisiert. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Die vorläufigen Versionshinweise für die Target-Versionen 19.4.1 und Target 19.4.2 wurden aktualisiert, beide für April 2019. |
| 4. April 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden vorläufige Versionshinweise für die Target 19.4.1- und Target 19.4.2-Versionen hinzugefügt, die beide für April 2019 geplant sind. |
| 30. März 2019 | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md#excludedid) | Es wurden Informationen zu den Beschränkungen für den `excludedID`-mbox-Parameter hinzugefügt. |
| 29. März 2019 | [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurde das folgende bekannte Problem hinzugefügt: „Für Einzelseitenanwendungen (SPA) ist es nicht möglich, das Laden von Aktionen im Bereich [!UICONTROL Änderungen] zu bearbeiten.“<br>Das folgende bekannte Problem wurde in den Abschnitt Gelöste Probleme verschoben: „v 1 Version der Angebots-APIs auf Adobe I/O behandelt alle Angebote, die über Target erstellt wurden, im Standardarbeitsbereich.“ |
| 28. März 2019 | [Visual Experience Composer (VEC)](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) | Die folgenden neuen Abschnitte wurden hinzugefügt:<ul><li>[Laden einer Seite im VEC abbrechen.](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading)</li><li>[Bearbeiten einer Seite, während die Seite geladen wird oder wenn die Seite nicht geladen werden konnte](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li></ul> |
|  | [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Neuer Abschnitt: [In Elementen über den DOM-Pfad navigieren](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path). |
|  | [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#cancel) | Es wurde ein aktuelles bekanntes Problem hinzugefügt, das auftritt, wenn Sie das Laden einer Seite innerhalb des VEC abbrechen. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.3.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.2.1 (19. Februar 2019) {#section-19-2-1}

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 20. März 2019 | [Häufig gestellte Fragen zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Die folgende FAQ wurde aktualisiert: [Kann ich die Target-Bibliothek asynchron laden?](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#section_AB9A0CA30C5440C693413F1455841470) |
|  | [Echtzeit-Profilsynchronisation für mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md) | Unten auf der Seite wurde ein Hinweis hinzugefügt. |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md)<br>[benutzerdefinierter Entitätsattribute](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) | Es wurden Informationen zu den Beschränkungen für „benutzerdefinierter Entitätsattribute“ hinzugefügt. |
|  | [Häufig gestellte Fragen zu Zielen und Zielgruppen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md#strings-that-represent-numbers) | Text aktualisiert. |
|  | [Neue Kriterien erstellen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#custom) | Es wurde ein neuer Abschnitt hinzugefügt, der erklärt, wie profilbasierte Gruppierungen für Popularitätsalgorithmen erstellt werden: „Verwenden eines benutzerdefinierten Empfehlungsschlüssels“. |
| 19. März 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den at.js-Versionen 2.0.1 und 1.7.1 hinzugefügt. |
|  | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | Folgende FAQ wurde hinzugefügt: „Unterstützt A4T virtuelle Report Suites?“ |
| 18. März 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) und [at.js-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den at.js-Versionen 2.0.1 und 1.7.1 hinzugefügt. |
|  | [Methoden zum Importieren von Daten in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#section_92AB4820A5624C669D9A1F1B6220D4FA) und [Kundenattribute](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Hinzugefügt: Folgende Zeichen können nicht in `mbox3rdPartyID` gesendet werden: Plus-Zeichen (+) und Schrägstrich (/). |
| 15. März 2019 | [Vor der Implementierung](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md) | Wichtiger Hinweis: Änderungen an at.js oder mbox.js werden von der Adobe-Kundenbetreuung nicht unterstützt. |
| 14. März 2019 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Das Datum der Target Standard/Premium 19.3.1-Veröffentlichung wurde auf 29. März 2019 geändert. |
| 13. März 2019 | [Erstellen einer Automated Personalization-Aktivität](/help/c-activities/t-automated-personalization/create-ap-activity.md) | Der Text in der Zeile Konversionsmetrik wurde aktualisiert. |
|  | [Profilattribute](/help/c-target/c-visitor-profile/profile-parameters.md) | Neuer Abschnitt hinzugefügt: „JavaScript-Referenz für Skript-Profilparameter“. |
|  | [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | Neu strukturierte Seite und neue Seiten für jede at.js-Funktion erstellt, um leichter auf Informationen zugreifen zu können. |
|  | [Funktionsweise von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Es wurde ein einleitender Absatz zur Erläuterung einer Client-seitigen Implementierung hinzugefügt. |
|  | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Folgende FAQ wurde hinzugefügt: „Kann ich eine Entität dynamisch ausschließen?“ |
| 12. März 2019 | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) und [Debug at.js mithilfe des Adobe Experience Cloud-Debuggers](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) | Der Debugger ist jetzt eine unterstützte Integration mit at.js 2.x. |
| 11. März 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md)<br>[Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md)<br>[Änderungen der TLS (Transport Layer Security)-Verschlüsselung](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Der Text wurde dahingehend aktualisiert, dass TLS am **1. April 2019** geändert wird. |
|  | [adobe.target.getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Folgender Abschnitt wurde hinzugefügt: „Daten aus mehfachen Mboxes über getOffers() und applyOffers() abrufen und rendern“. |
| 6. März 2019 | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Zeile „at_property“ zur Tabelle „at.js 1.x Parameter auf at.js 2.x Nutzlastzuordnung“ hinzugefügt. |
|  | [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) | Neuer Abschnitt hinzugefügt: „Verwenden von TriggerView, um sicherzustellen, dass A4T ordnungsgemäß mit at.js 2.x und SPAs funktioniert.“ |
| 4. März 2019 | [Dokumentation zu Recommendations Classic](/help/c-recommendations/recommendations-classic-documentaton.md) | Neues Thema |
|  | [Recommendations Classic und Recommendations-Aktivitäten in Target Premium](/help/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md) | Es wurden Informationen zu Recommendations als Angebot hinzugefügt. |
| 28. Februar 2019 | [Aktivitäten](/help/c-activities/activities.md) | Text und Bilder aktualisiert. |
|  | [Einführung in Target](/help/c-intro/intro.md) | „Empfehlungen als Angebot“ unter „Target Premium“ hinzugefügt. |
|  | [Wichtige Target-Konzepte](/help/c-intro/target-key-concepts.md) | Die Tabelle „Aktivitätstypen“ wurde aktualisiert. |
| 26. Februar 2019 | [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Es wurde ein bekanntes Problem zur Unterstützung von Unternehmens-Berechtigungen in Target-APIs hinzugefügt. |
| 25. Februar 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md)<br>[Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md)<br>[Änderungen der TLS (Transport Layer Security)-Verschlüsselung](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Die folgenden Informationen wurden aktualisiert:<br>Am 20. Februar 2019 wurde die Adobe Target-Infrastruktur in den Regionen EMEA, Japan und APAC aktualisiert, um keine Daten mehr von Endbenutzern mit älteren Geräten oder Webbrowsern zu erfassen, die TLS 1.1 oder höher nicht unterstützen. Diese Aktualisierung ist für Nordamerika am **4. März 2019** geplant. Die Migration zu TLS 1.2 bietet eine verbesserte Sicherheit. Für einen reibungslosen Übergang sollten Sie die Details zu diesem Thema genau durchlesen und die Änderungen entsprechend planen. |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#payload-mapping) | Neuer Abschnitt: „at.js 1.x Parameter auf at.js 2.x Nutzlastzuordnung“. |
|  | [Beheben von Problemen mit Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) | Die Spalte „Hostnamen“ wurde zu den IP-Adressen der Whitelist hinzugefügt. |
| 22. Februar 2019 | [Konfigurieren von Unternehmensberechtigungen](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Der Abschnitt „Arbeitsbereichs-ID erhalten“ wurde hinzugefügt. |
| 20. Februar 2019 | [Kategorieaffinität](/help/c-target/c-visitor-profile/category-affinity.md) | Der Abschnitt „Kategorieaffinitätsalgorithmus“ wurde aktualisiert. |
| 19. Februar 2019 | [Visual Experience Composer (VEC) für Einzelseiten-Apps (SPAs)](/help/c-experiences/spa-visual-experience-composer.md) | Neues Thema und Schulungsvideos. |
|  | [Implementieren von Single-Page-Anwendungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) | Neues Thema und Schulungsvideos. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den at.js-Versionen 1.7.0 und 2.0.0 hinzugefügt. |
|  | [Aktualisieren von at.js 1.x auf at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Neues Thema und Schulungsvideo. |
|  | [„at.js“-Funktionen](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | Aktualisierung des Themas, um Änderungen durch die Einführung von at.js 2.x widerzuspiegeln.<br> Für at.js 2.x sind drei neue Funktionen verfügbar.<ul><li>adobe.target.getOffers(options)</li><li>adobe.target.applyOffers(options)</li><li>adobe.target.triggerView (viewName, options)</li></ul> |
|  | [Funktionsweise von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | Das Thema wurde aktualisiert, um Änderungen mit der Einführung von at.js 2.x widerzuspiegeln. Außerdem Schulungsvideo hinzugefügt. |
|  | [Verwaltung von Flackern mit „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) | Das Thema wurde aktualisiert, um Änderungen mit der Einführung von at.js 2.x widerzuspiegeln. |
|  | [Häufig gestellte Fragen zu „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Das Thema wurde aktualisiert, um Änderungen mit der Einführung von at.js 2.x widerzuspiegeln. |
|  | [„at.js“-Debugging mit dem Adobe Experience Cloud-Debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) | Es wurde ein Hinweis hinzugefügt, der erklärt, dass die Adobe Experience Cloud-Debugger-Netzwerkanforderung und die Mbox-Trace-Funktionen für at.js 2.x noch nicht unterstützt werden. |
|  | [at.js-Cookies](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | Neues Thema |
|  | [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md) | Neues Thema |
|  | [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | <ul><li>Es wurden Informationen zur Verwendung der Aktion [!UICONTROL „Einfügen vor“, „Einfügen nach“ oder „Ersetzen mit“] hinzugefügt, um einem Erlebnis Recommendations in einer A/B-Test- oder Erlebnis-Targeting-Aktivität hinzuzufügen.</li><li>Es wurden Informationen zur Verwendung der Aktion [!UICONTROL „Enfügen vor“ oder „Einfügen nach“] hinzugefügt, um AEM-Erlebnisfragmente zu einem Erlebnis hinzuzufügen.</li></ul> |
|  | [Visual Experience Composer Helper-Erweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Neues Thema |
|  | [Privatsphäre und Datenschutz-Grundverordnung](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (DSGVO) | Kleinere Bearbeitungen und Informationen über die Opt-in-Funktionalität und at.js 1.7.0 und at.js 2. |
|  | [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md) | Bekannte Probleme zu Target-APIs wurden hinzugefügt. |
|  | [Entitätsattribute](/help/c-recommendations/c-products/entity-attributes.md) | Es wurde ein Hinweis hinzugefügt, dass die Werte für Entitätsattribute nach 61 Tagen ablaufen. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.2.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 19.1.1 (22. Januar 2019) {#section-19-1-1}

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 2. Februar 2019 | [Target-Versionshinweise](/help/r-release-notes/target-release-notes.md) (Vorabversion) | Die Hinweise zur Vorabversion für die Version [!DNL Target] 19.2.1 (19. Februar 2019) wurden aktualisiert. |
| 30. Januar 2019 | [Ziele und Zielgruppen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Neue FAQ hinzugefügt: Zeichenfolgen, die Zahlen darstellen (Fließkommazahlen werden ebenfalls unterstützt) werden als Zahlen verglichen. |
| 29. Januar 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Verfügbarkeitsdatum Enterprise-Berechtigungen in Target-APIs aktualisiert am 21. Februar 2019. |
|  | [Systemstatusaktualisierungen und proaktive Benachrichtigungen](/help/r-release-notes/system-status-updates.md) | Proaktiver Benachrichtigungsabschnitt hinzugefügt. |
| 22. Januar 2019 | [Sammlungen](/help/c-recommendations/c-products/collections.md)<br>[Ausschlüsse](/help/c-recommendations/c-products/exclusions.md)<br>[Katalogsuche](/help/c-recommendations/c-products/catalog-search.md)<br>[](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)<br>[EinstellungenRecommendations: Filtern von Sammlungen und Ausschlüssen nach Umgebung (Hostgruppe)](/help/administrating-target/hosts.md) | Es wurden Informationen zum Filtern von Sammlungen und Ausschlüssen nach Umgebung (Hostgruppe) hinzugefügt. |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Die Informationen in der Zeile „Profilskript-Wert“ wurden aktualisiert. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 19.1.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 18.11.1 (12. November 2018) {#section_4AD10E8B7EB04F96807FFDB763F31703}

| Datum | Thema | Änderungen |
|--- |--- |--- |
| 16. Januar 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md)<br>[Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md)<br>[at.js-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen über die at.js-Version 1.6.4 hinzugefügt. |
| 10. Januar 2019 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md)<br>[Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md)<br>[Änderungen der TLS-Verschlüsselung (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Es wurde das Datum hinzugefügt, ab dem die Unterstützung der TLS 1.0-Verschlüsselung durch Target vollständig abläuft: 20. Februar 2019 |
| 9. Januar 2019 | [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Es wurden Informationen zu Recommendations zu „Einfügen vor“-, „Einfügen nach“- und „Ersetzen mit“-Zeilen hinzugefügt. |
|  | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md)<br>[Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md)<br>[Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Es wurden Informationen über Target und die Adobe Experience Cloud-Unterstützung für Microsoft Internet Explorer 11 ab März 2019 hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen für die Versionen Target 19.1.1 und at.js 1.6.4 veröffentlicht. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen für at.js Version 1.6.4 hinzugefügt. |
|  | [Minimieren von überhöhten Besuchs- und Besucherzahlen in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md) | Es wurde ein Hinweis entfernt, dass Kunden seit dem 14. November 2016 keine A4T-Aktivitäten mit Umleitungsangeboten mehr erstellen können. |
|  | [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Es wurde ein Hinweis unter „Warum sind Seitenansichten auf der ursprünglichen Seite und auf der Umleitungsseite manchmal gezählt?“ hinzugefügt. |
| 20. Dezember 2018 | [Target serverseitig implementieren](../c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Es wurde ein Hinweis zu CORS hinzugefügt. |
| 14. Dezember 2018 | [Implementieren von Target mit Adobe Launch](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) | Link zu einem neuen Schulungsvideo hinzugefügt: Implementieren von Target mit dem Adobe Launch Tutorial. |
|  | [Berichte zu Personalization Insights](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | Es wurde ein Link zu einem Schulungsvideo hinzugefügt. |
| 13. Dezember 2018 | [Form-Based Experience Composer](../c-experiences/form-experience-composer.md) | Text und Abbildung aktualisiert. |
|  | [Bekannte Probleme und gelöste Probleme](known-issues-resolved-issues.md) | Bekanntes Problem wurde hinzugefügt, dass der Recommendations-Feed-Index „Warten auf Index“ anzeigen kann, wenn die Elemente im Feed mit denen im vorherigen Schritt übereinstimmen. |
|  | [Zielgruppenauswahl](../c-activities/t-test-ab/t-test-create-ab/ab-audience.md) | Bilder aktualisiert. |
|  | [Hinzufügen von Erlebnissen](../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md) | Bild aktualisiert. |
|  | [Erstellen eines A/B-Tests](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) | Bilder aktualisiert. |
|  | [Testzusammenfassung](../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md) | Bild aktualisiert. |
|  | [Erlebnisvorschau für Multivarianz-Tests](../c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md) | Bild aktualisiert. |
|  | [Erstellen von Kombinationen](../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md) | Text und Bilder aktualisiert. |
|  | [Erstellen eines Multivarianz-Tests](../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) | Text und Bilder aktualisiert. |
| 11. Dezember 2018 | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Es wurde hinzugefügt, dass der Standardwert für overrideMboxEdgeServer „true“ ist, beginnend mit at.js Version 1.6.2. |
| 7. Dezember 2018 | [ Bekannte Probleme und gelöste Probleme ](known-issues-resolved-issues.md) | Die folgende Tabelle wurde aus der Tabelle „Bekannte Probleme“ in die Tabelle „Gelöste Probleme“ verschoben: <ul><li>at.js: Mboxes, die aufgrund der Interaktion zwischen at.js und Visitor API 2.2.0.0 nicht in Microsoft Explorer 11 ausgelöst werden, nachdem sie auf at.js Version 1.0 aktualisiert wurden.</li><li>Geo-Targeting: Die Suche nach einer Zeichenfolge, die Sonderzeichen enthält (z. B. ein Leerzeichen oder ein Komma), funktioniert derzeit beim Erstellen von Geotargeting-Zielgruppen nicht.</li></ul> |
| 5. Dezember 2018 | [ Berichte zu Personalization Insights ](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | Es wurde ein Hinweis hinzugefügt, dass die Personalization Insights-Berichte nur in der Standardumgebung verfügbar sind. |
|  | [ Adobe Analytics als Berichtsquelle für Adobe Target (AT) ](../c-integrating-target-with-mac/a4t/a4t.md) | Die Tabelle wurde aktualisiert, um anzugeben, dass A4T serverseitige Bereitstellungen unterstützt. |
| 29. November 2018 | [ Schätzen des für einen erfolgreichen Test erforderlichen Traffics](../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) | Kleinere Textaktualisierungen und aktualisierte Bilder. |
| 27. November 2018 | [Aktivitäten](../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) | Text und Bilder aktualisiert. |
|  | [ Profilskriptattribute ](../c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2) | Es wurde ein Hinweis hinzugefügt, dass Target pro Konto über maximal 1.000 Profilskripte verfügt. |
| 15. November 2018 | [ Target-Versionshinweise (aktuell) ](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A)<br>[ Target-Versionshinweise (Vorabversion) ](../r-release-notes/target-release-notes.md#reference_4A966062C61048D1A81412E2DDB16E34)<br>[ at.js-Versionsdetails ](../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) | Es wurden Informationen über die at.js-Version 1.6.3 hinzugefügt. |
|  | [ Berichte zu Personalization Insights ](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) | Es wurden neue Themen für die neuen Personalization Insights-Berichte hinzugefügt: Automatisierte Segmente und Wichtige Attribute. |
| 14. November 2018 | Version 18.11.1 [Versionshinweise (aktuell) ](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 18.10.1 (24. Oktober 2018) {#section_F3DB9A89D944428DBEE04634EB712601}

| Datum | Thema | Änderungen |
|--- |--- |--- |
| 8. November 2018 | [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) | Das NodeJS-SDK wurde zur Kompatibilitätstabelle hinzugefügt. |
| 7. November 2018 | [Wie lange sollten A/B-Tests laufen?](../c-activities/t-test-ab/sample-size-determination.md#concept_2801F552DB874C20B8A17C1B774C0383) | Das Thema wurde bearbeitet und es wurden zusätzliche Informationen hinzugefügt. |
|  | [Target-Versionshinweise (Vorabversion)](../r-release-notes/target-release-notes.md#reference_4A966062C61048D1A81412E2DDB16E34) | Es wurden Informationen zu Funktionen in Target-Version 18.11.1 hinzugefügt. |
| 5. November 2018 | [Integration von Recommendations in E-Mail](../c-recommendations/c-recommendations-faq/integrating-recs-email.md#reference_256B16C894864F24AF970E43DC174420) | Der Link in Option 3 wurde aktualisiert. |
|  | [Kundenattribute](../c-target/c-visitor-profile/working-with-customer-attributes.md#concept_16C5C434D32D4EB1AD44A71821F3DEE8) | Folgender Hinweis wurde hinzugefügt:<br>**Wichtig **: Der Name der Datenquelle und der Attributname dürfen keinen Punkt enthalten. |
| 31. Oktober 2018 | [Systemstatusupdates](../r-release-notes/system-status-updates.md#concept_5CBDF506BEFA40E483CC7DE0DA915EAD) | Das Thema wurde aktualisiert. |
|  | [Webinar-Reihe zu Target-Grundlagen](../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4) | Es wurde ein Link zur Aufzeichnung „Best Practices für Zielgruppensegmentierung“ hinzugefügt. |
| 29. Oktober 2018 | [Änderungen der TLS-Verschlüsselung (Transport Layer Security)](../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) | Es wurde ein neuer Abschnitt hinzugefügt: „Erwartetes Verhalten bei Browsern, die nur TLS 1.0 unterstützen“. |
| 26. Oktober 2018 | [Bekannte Probleme und gelöste Probleme](../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541) | <ul><li>Es wurde ein bekanntes Problem hinzugefügt, das bei der Suche nach Zeichenfolgen mit Sonderzeichen während der Erstellung von Geotargeting-Zielgruppen auftritt.</li><li>Das Umleitungsproblem von „at.js“-Version 1.6.0 wurde in die Tabelle „Behobene Probleme“ verschoben.</li><li>Das Problem, bei dem Aktivitäten im Standardarbeitsbereich, die per API gelöscht wurden, weiterhin in der Target-Benutzeroberfläche angezeigt werden, wurde in die Tabelle „Behobene Probleme“ verschoben.</li></ul> |
| 24. Oktober 2018 | [Voreinstellungen](../administrating-target/r-target-account-preferences/target-account-preferences.md#reference_0CF97B1C2214412ABBC8222EA8A36D7E) | Es wurden Informationen hinzugefügt, die bei der Auswahl der Berichtsquelle für Aktivitäten in „Setup“ > „Voreinstellungen“ bzw. bei der Auswahl pro Aktivität zu beachten sind. |
|  | [Erstellen einer Automated Personalization-Aktivität](../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) | Es wurden Informationen zum Filtern nicht zugewiesener Angebote hinzugefügt. |
|  | [Erlebnis erstellen](../c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) | Es wurden Informationen zum Duplizieren von Erlebnissen in XT-Erlebnissen hinzugefügt. |
|  | [Hinzufügen von Erlebnissen](../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) | Es wurden Informationen zum Duplizieren von Erlebnissen in A/B-Tests hinzugefügt. |
|  | [ Über Zielgruppen](../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271) | Es wurden Informationen zur Verarbeitung von in Target-Aktivitäten referenzierten Zielgruppen, die in Adobe Audience Manager (AAM) gelöscht wurden, hinzugefügt. |
|  | [„at.js“-Integrationen](../c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) | Das Thema wurde aktualisiert. |
|  | [Implementieren von Target ohne einen Tag-Manager](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#topic_397FFA3D6918456BBE02A9FBE9537894) | Es wurden alle Abschnitt aktualisiert.  Es wurde ein neuer Abschnitt hinzugefügt: „at.js“-Implementierung. |
|  | Version 18.10.1 [Versionshinweise](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe Target Standard/Premium 18.9.1 (26. September 2018)  {#section_F7E74227BB9D467E9ABC0797EDC2FE0D}

<table id="table_0348AA29207D48A4BDFFA187F4F845B7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum </th> 
   <th colname="col2" class="entry"> Thema </th> 
   <th colname="col3" class="entry"> Änderungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 24. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein bekanntes Problem hinzugefügt, bei dem per API im Standardarbeitsbereich gelöschte Aktivitäten weiterhin in der Target-Benutzeroberfläche angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md#topic_AFFDC672A8A34D028B100EF6BE5D8129" format="dita" scope="local"> Durchschnittliche Steigerung, Steigerungsgrenzen und Konfidenzintervall </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein Hinweis hinzugefügt, der angibt, dass zwischen manuellen Berechnungen mit den aufgeführten Formeln und den im Bericht angezeigten Zahlen kleine Abweichungen auftreten können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 22. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md#concept_4D8107E193B64168A3C0B85B51612991" format="dita" scope="local"> Target-Cookie </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein wichtiger Hinweis oben im Thema hinzugefügt, um Kunden darauf aufmerksam zu machen, keine vertraulichen Informationen an mboxSession und mboxPC zu senden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 21. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js-Versionsdetails </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen über at.js-Version 1.6.2 hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#topic_6BCC0D0984184379A2A2EA6FFC948899" format="dita" scope="local"> Privatsphäre und Datenschutz-Grundverordnung (DSGVO) </a> </p> </td> 
   <td colname="col3"> <p>Der Abschnitt „Adobe Target- und Adobe Launch-Opt-in“ wurde hinzugefügt. </p> <p>Folgende Abschnitte mit häufig gestellten Fragen wurden aktualisiert: </p> <p> 
     <ul id="ul_BBF57B0E30A541E1BD1BCADD21A3D0F7"> 
      <li id="li_020DE613F4F340D8B68186465883A60C"> <p>Wie werden Einwilligungen in Adobe Target verwaltet? </p> </li> 
      <li id="li_515B157F27B04342BB5664FD8E258FE2"> <p>Welche IDs werden unterstützt, um Kunden zu helfen, Datenzugriffs- und Löschungsanfragen gemäß DSGVO in Target nachzukommen? </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25" format="dita" scope="local"> Implementieren von Target mit Adobe Launch </a> </p> </td> 
   <td colname="col3"> <p>Der Link zur Adobe Target-Erweiterung wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 18. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> Von Recommendations-Feed verarbeitenden Servern verwendete IP-Adressen </a> </p> </td> 
   <td colname="col3"> <p>Der von Target Recommendations-Aktivitäten verwendete IP-Adressbereich wurde aktualisiert. </p> <p>Der von Target Recommendations-APIs verwendete IP-Adressbereich wurde hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 12. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40" format="dita" scope="local"> Aktivitäts-QA </a> </p> </td> 
   <td colname="col3"> <p>Folgende Abschnitte unter <span class="wintitle">„Zu berücksichtigen“</span> wurden aktualisiert: </p> <p>Aktivitäts-QA zeigt keinen Inhalt für archivierte Aktivitäten oder Aktivitäten an, deren Enddatum vorüber ist. Wenn Sie eine beendete Aktivität deaktivieren, müssen Sie die Aktivität erneut speichern, damit Aktivitäts-QA funktioniert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 10. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../target-home.md#topic_74F655D8648E4586BCCFD789E60D13CE" format="dita" scope="local"> Adobe Target-Produktdokumentation </a> </p> </td> 
   <td colname="col3"> <p>Die Adobe Target-Produktdokumentation folgender Sprachen wurde aktualisiert: Deutsch, Französisch, Italienisch, Japanisch, Portugiesisch (Brasilien) und Spanisch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 9. Oktober 2019 </td> 
   <td colname="col2"> <p> <a href="../c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profilattribute </a> </p> </td> 
   <td colname="col3"> <p>Es wurden häufig gestellte Fragen zu Profilskripten hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> Von Recommendations-Feed verarbeitenden Servern verwendete IP-Adressen </a> </p> </td> 
   <td colname="col3"> <p>Der Text wurde bearbeitet, um anzugeben, dass <span class="wintitle">Recommendations</span>-Aktivitäten IP-Adressen im Data Center in Oregon verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 8. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> Von Recommendations-Feed verarbeitenden Servern verwendete IP-Adressen </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein neuer IP-Adressbereich für die CIDR-Notation hinzugefügt: 192.243.242.0.0/24. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#concept_72A95F6466A04B409FCD5989A6B6A554" format="dita" scope="local"> Berichte anzeigen - Häufig gestellte Fragen zu A4T </a> </p> </td> 
   <td colname="col3"> <p>Der gesamte Abschnitt „Sollte ich beim Anzeigen von Berichten Besucher, Aktivitätsimpressionen oder Besuche verwenden?“ wurde aktualisiert. Die Metrikbeschreibungen wurden umformuliert und es wurde eine Liste zu berücksichtigender Punkte hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local"> Erstellen von Kriterien </a> </p> </td> 
   <td colname="col3"> <p>Der Abschnitt „Erwartete Verarbeitungszeit für Kriterien“ wurde hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local">Aktivitäten</a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zur Deaktivierung der Funktion „Tipp des Tages“ hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="https://spark.adobe.com/page/Lo3Spm4oBOvwF/" format="https" scope="external"> Analytics und Target: Best Practices für Analysen </a> </p> </td> 
   <td colname="col3"> <p>Sehen Sie sich das neue A4T-Tutorial (Analytics for Target) an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584" format="dita" scope="local"> Funktionsweise von Adobe Target </a> </p> </td> 
   <td colname="col3"> <p>Das ganze Thema wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Erstellen eines A/B-Tests </a> </p> <p> <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Erstellen einer Aktivität vom Typ „Automatisierte Personalisierung“</a> </p> <p> <a href="../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Erstellen einer Erlebnis-Targeting-Aktivität </a> </p> <p> <a href="../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710" format="dita" scope="local"> Erstellen eines Multivarianz-Tests </a> </p> <p> <a href="../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB" format="dita" scope="local"> Einstellungen für Recommendations-Aktivitäten </a> </p> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Hinzufügen von Erlebnissen </a> </p> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB" format="dita" scope="local"> Festlegen von Metriken </a> </p>
   </td> 
   <td colname="col3"> <p>Die Tabelle der in Aktivitäts-, Erlebnis- oder Metriknamen unzulässigen Zeichen wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2. Oktober 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/collections.md#concept_671BEFFB997D4F1282665BF3CAC00AC5" format="dita" scope="local"> Sammlungen </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein Hinweis nach Schritt 1 hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/exclusions.md#task_E79DA82BA402415FB41232976EDEF1CA" format="dita" scope="local"> Ausnahmen </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein Hinweis nach Schritt 1 hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 27. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17" format="dita" scope="local"> Verfahren für die Datenübernahme in Target </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zu in Abfragezeichenfolgen zulässigen Zeichen hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> <p>Das bekannte Problem hinsichtlich des Reportings auf Angebotsebene in AP-Aktivitäten wurde in die Tabelle „Behobene Probleme“ verschoben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 26. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer-Optionen </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zur Option <span class="wintitle">„Einfügen vor“</span> hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local">Erstellen einer Aktivität vom Typ „Automatisierte Personalisierung“</a> </td> 
   <td colname="col3"> <p>Es wurden Informationen zur Liste „Berichtsgruppe“ hinzugefügt, in der Sie Angebote nach Berichtsgruppe filtern können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Verwalten von Ausschlüssen </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zur Verwendung mehrerer Angebote vom selben Standort in einer Ausschlussgruppe hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Webinar-Reihe zu Target-Grundlagen </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein Link zur Sitzung „Best Practices bei Reporting und Wertesozialisation“ hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a> </p> </td> 
   <td colname="col3"> <p>Folgender Hinweis wurde hinzugefügt: </p> <p> <p>Wichtig: Hochgeladene Feeds laufen nach 61 Tagen ab. Das bedeutet, dass Empfehlungen nicht mehr zurückgegeben werden, wenn eine Feeddatei nicht in den letzten 60 Tagen verarbeitet wurde. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein bekanntes Problem hinsichtlich des Reportings auf Angebotsebene in AP-Aktivitäten hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/integrating-recs-email.md#reference_256B16C894864F24AF970E43DC174420" format="dita" scope="local"> Integration von Recommendations in E-Mail </a> </p> </td> 
   <td colname="col3"> <p>Der Hinweis unter „Option 1: Verwenden der Bereitstellungs-API“ wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0" format="dita" scope="local"> Recommendations </a> </p> </td> 
   <td colname="col3"> <p>Die Themen im gesamten Abschnitt wurden neu sortiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Version 18.9.1 <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Versionshinweise </a> </p> </td> 
   <td colname="col3"> <p>Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Target Standard/Premium 18.8.1 (21. August 2018)  {#section_6A146EE91FFB49D1BA398B36817CD0A2}

<table id="table_F09AC99B587A4D6390B1F8AE54F5DC47"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Datum </th> 
   <th colname="col2" class="entry"> Thema </th> 
   <th colname="col3" class="entry"> Änderungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 21. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F" format="dita" scope="local"> Debugging von at.js mithilfe des Adobe Experience Cloud-Debuggers </a> </p> </td> 
   <td colname="col3"> <p>Das gesamte Thema wurde überarbeitet und es wurden Schulungsvideos hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 20. September 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Versionshinweise Target </a> </p> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> at.js-Versionsdetails </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zur „at.js“-Version 1.6.1 hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 19. September 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> Das folgende Problem mit dem Code-Editor wurde aus der Tabelle „Bekannte Probleme“ in die Tabelle „Gelöste Probleme“ verschoben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 18. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> Erlebnisvorlagen </a> </p> </td> 
   <td colname="col3"> <p>Neues Thema </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Webinar-Reihe zu Target-Grundlagen </a> </p> </td> 
   <td colname="col3"> <p>Die Daten anstehender Webinare wurden aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 11. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-activities/c-activity-qa/use-qa-mode-with-server-side-delivery.md#concept_54698C5CE8934F68B20961CD83FD6202" format="dita" scope="local"> Verwenden von Aktivitäts-QA mit Server-seitiger Bereitstellung </a> </p> </td> 
   <td colname="col3"> <p>Neues Thema </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Benutzerdefinierte Parameter </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zur erneuten Speicherung vor Version 18.5.1 erstellter benutzerdefinierter Zielgruppen hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> <p>Es wurde ein bekanntes Problem hinzugefügt: Target-Aktivitätsimpressionen und -konversionen werden derzeit im Analysis Workspace nicht richtig gezählt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#concept_41F88DE95D2943178BEC382736B5C038" format="dita" scope="local"> Häufig gestellte Fragen zur DSGVO </a> </p> </td> 
   <td colname="col3"> <p>Das Codebeispiel wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Recommendations-FAQs </a> </p> </td> 
   <td colname="col3"> <p>Die erforderliche Velocity-Version wurde zu 1.7.0 geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 10. September 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Versionshinweise Target </a> </p> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> TLS-Verschlüsselungsänderungen (Transport Layer Security) </a> </p> </td> 
   <td colname="col3"> <p>Das Datum, an dem Adobe die Unterstützung von TLS 1.0 einstellt, wurde vom 12. September 2018 zu Februar 2019 geändert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local"> Berichte </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen sowie ein Link zur Unterstützung bei der Planung von A/B-Tests hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Recommendations-FAQs </a> </p> </td> 
   <td colname="col3"> <p>Folgende häufig gestellte Frage wurde hinzugefügt: Wie groß dürfen CSV-Dateien für den Feedupload maximal sein? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Besucherprofil </a> </p> </td> 
   <td colname="col3"> <p>Folgender Abschnitt wurde hinzugefügt: </p> <p>Für jeden Mbox-Aufruf mit neuem <span class="codeph">mboxPC</span>-Wert wird ein Besucherprofil im lokalen Edge-Speicher erstellt. Nach 30 Minuten Inaktivität wird das Profil in der Target-Datenbank gespeichert und ist für andere Edges zugänglich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90" format="dita" scope="local"> Aktivitäts-URL </a> </p> </td> 
   <td colname="col3"> <p>Text und Abbildung wurden aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 7. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Recommendations-FAQs </a> </p> </td> 
   <td colname="col3"> <p>Folgende häufig gestellte Frage wurde hinzugefügt: Warum kann ich meine alte Recommendations-Aktivität nicht speichern, nachdem ich eine neue Zielgruppe definiert habe? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4. September 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#section_42725F3C837247D58AE1831EA330E44D" format="dita" scope="local"> Datenanbieter </a> </p> </td> 
   <td colname="col3"> <p>Das Codebeispiel wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#concept_41F88DE95D2943178BEC382736B5C038" format="dita" scope="local"> Häufig gestellte Fragen zur DSGVO </a> </p> </td> 
   <td colname="col3"> <p>Kleinere Änderungen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 30. August 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> Das folgende bekannte Problem wurde hinzugefügt: <p> 
     <ul id="ul_7AF527E5989D468BBC9472EA1C7F376D"> 
      <li id="li_7F53C6F01E1E471FB546AF98F1FF7F1E"> <p>Bei der Verwendung von <span class="codeph">at.js</span>-Version 1.6.0 treten A4T-Umleitungen (Analytics for Target) auf, jedoch ohne Aktivitätsqualifikation. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 28. August 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F" format="dita" scope="local"> Entitätsattribute </a> </p> </td> 
   <td colname="col3"> <p>Die Element-ID-Zeile wurde aktualisiert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Inhaltseinstellungen </a> </p> </td> 
   <td colname="col3"> <p>Die Informationen zur Option <span class="wintitle">„Zuvor gekaufte Artikel empfehlen“</span> wurden überarbeitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 21. August 2018 </td> 
   <td colname="col2"> <p> <a href="../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Personalization Insights-Berichte </a> </p> </td> 
   <td colname="col3"> <p>Neues Thema </p> <p> <p>Hinweis: Diese Funktion ist in Kürze verfügbar. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Änderungen </a> </p> </td> 
   <td colname="col3"> <p>Es wurden Informationen zum Andocken des Bedienfelds „Änderungen“ hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer-Optionen </a> </p> </td> 
   <td colname="col3"> <p>Die Tabelle wurde umstrukturiert, um die neuen Gruppierungen widerzuspiegeln. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Webinar-Reihe zu Target-Grundlagen </a> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_D5E4E05DFE7A4E45BF199395D7AC3CE1"> 
      <li id="li_7A4A621EC5C34E4AADD46AA294620D9C"> <p>Es wurden Informationen zu anstehenden Webinaren hinzugefügt. </p> </li> 
      <li id="li_A77B214010EF45BEBD0E2CBB256AD67D"> <p>Es wurde ein Link zur Aufzeichnung des zweiten Webinars „Schritte zum Hinzufügen von Automatisierung und komplexeren Aktivitäten“ hinzugefügt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local">Aktivitäten</a> </p> </td> 
   <td colname="col3"> <p>Der Abschnitt „Tipps und Tricks“ wurde hinzugefügt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekannte Probleme und gelöste Probleme </a> </p> </td> 
   <td colname="col3"> <p>Das Problem, bei dem Umleitungsaktivitäten in <span class="codeph">at.js</span>-Implementierungen eine Schleife der Vorschau-URL auslösen können, wurde umformuliert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> TLS-Verschlüsselungsänderungen (Transport Layer Security) </a> </p> </td> 
   <td colname="col3"> <p>Das vorherige Datum der Einstellung der TLS-1.0-Unterstützung (12. September 2018) wurde entfernt. </p> <p>Das Datum, zu dem die Unterstützung von TLS 1.0 eingestellt wird, wird später bekannt gegeben. Es ist jedoch wichtig, sich schon jetzt mit den Details vertraut zu machen und die Änderungen zu planen, um einen reibungslosen Wechsel zu gewährleisten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Version 18.8.1 <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Versionshinweise </a> </p> </td> 
   <td colname="col3"> <p>Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. </p> </td> 
  </tr> 
 </tbody> 
</table>

