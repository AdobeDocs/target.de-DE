---
keywords: target documentation change log;documentation updates;new topics;edits;updates
description: Auf dieser Seite werden wichtige Änderungen an der Dokumentation zur Adobe-Zielgruppe, geordnet nach Versionen, Liste.
title: Änderungen an der Adobe Target-Produktdokumentation.
topic: Standard
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
translation-type: tm+mt
source-git-commit: da102687f5d73813e3670b166eb0e668b96c93b6
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 36%

---


# Dokumentationsänderungen{#documentation-changes}

This page lists important changes made to the [!DNL Adobe Target] product documentation.

## Adobe Target Standard/Premium 20.4.1 (6. Mai 2020) 

| Datum | Thema | Änderungen |
| --- | --- | --- |
| Mai 21 | [Randknoten der Whitelist-Zielgruppe](/help/c-implementing-target/c-considerations-before-you-implement-target/white-list-edges.md) | Der Liste `mboxedge30.tt.omtrdc.net` hinzugefügt. |
| Mai 20 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Es wurden Informationen zur kommenden Zielgruppe Standard/Premium 20.6.1 (10. Juni 2020) hinzugefügt. |
|  | [Hosts](/help/administrating-target/hosts.md) | Es wurde ein Hinweis zum Abschnitt &quot;Best Practices für die Sicherheit&quot;hinzugefügt. |
| Mai 14 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Es wurden Informationen zu den Änderungen an der Profil Batch Status API Version 2 hinzugefügt. |
| Mai 13 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Der Abschnitt &quot;Bekannte Einschränkungen&quot;wurde hinzugefügt. |
| Mai 11 | [Hosts](/help/administrating-target/hosts.md) | Es wurden Informationen zur Verwendung der Ubox-Funktion mit Umleitungen und Whitelists hinzugefügt. |
|  | [Arbeiten mit Weiterleitungen](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) | Es wurden Informationen zur Verwendung von Hosts hinzugefügt, um Open-Redirect-Schwachstellen zu vermeiden. |
|  | [Integration von Recommendations in E-Mail](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | Es wurden Informationen zur Verwendung von Hosts hinzugefügt, um Open-Redirect-Schwachstellen zu vermeiden. |
|  | [E-Mail: Target-Implementierung](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md) | Es wurden Informationen zur Verwendung von Hosts hinzugefügt, um Open-Redirect-Schwachstellen zu vermeiden. |
| Mai 7 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Mit der bevorstehenden Vernichtung von &quot;mbox.js&quot;am 30. August 2020 hat David Son, Adobe Zielgruppe Product Manager, kürzlich einen Entwicklerchat gehostet, um die Vorteile der Migration von &quot;mbox.js&quot;auf &quot;at.js&quot;zu erörtern. Über einen Link können Sie sich das Webinar für die nächsten 30 Tage ansehen. |
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
|  | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Das Datum der Zielgruppe Standard/Premium Version (20.4.1) wurde in den 6. Mai geändert. |
| April 23 | [CNAME und Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Das Thema wurde aktualisiert. |
| April 22 | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Neuer Abschnitt hinzugefügt: *Änderungen an der Profil Batch-Status-API, Version 2 (4. Mai 2020).* |
| April 20 | [Target-Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Neuer Abschnitt hinzugefügt: *Adobe Zielgruppe Skill Builder: Entwickler-Chat, migrieren Sie &quot;mbox.js&quot;der Adobe-Zielgruppe in &quot;at.js&quot;.* |
| April 14 | [Edge-Hosts der Whitelist-Zielgruppe](/help/c-implementing-target/c-considerations-before-you-implement-target/white-list-edges.md) | Neues Thema |
| April 10 | [Implementieren von Einzelseiten-Apps](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp) | Neuer Abschnitt hinzugefügt: &quot;Best Practices für die Implementierung&quot;. |
| April 7 | [Steigerung und Konfidenz – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence) | Der Text für &quot;Warum kann ich Steigerung und Konfidenz bei berechneten Metriken nicht sehen?&quot; wurde aktualisiert. |
| April 2 | [Nützliche Variablen, Profile, Parameter und Methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Es wurden Informationen zur Verwendung `user.header('x-forwarded-for')` mit neueren AWS-Kanten zum Abrufen der IP-Adressen von Benutzern hinzugefügt. |
|  | [Aktualisieren von at.js 1.*x* auf at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Folgender Hinweis wurde hinzugefügt:<ul><li>Nach der Installation der ECID-Bibliothek v 4.3.0 + und at.js 2.*x* können Sie Aktivitäten erstellen, die mehrere Domänen umfassen und Benutzer tracken können. Beachten Sie, dass diese Funktion erst nach Ablauf der Sitzung funktioniert.</li></ul> |
| 30. März | [Bekannte und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Es wurden bekannte Probleme hinzugefügt, die at.js-Versionen vor at.js 2.2.0 betreffen. Dieses Problem führte dazu, dass Klick-Tracking keine Konvertierungen in Analytics für die Zielgruppe (A4T) meldete, wenn Adobe Analytics-Code nicht in Seitenelementen vorhanden war. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Die folgenden Informationen wurden den Details zu at.js Version 2.2.0 hinzugefügt:<ul><li>Es wurde ein Fehler behoben, der dazu führte, dass Klick-Tracking keine Konversionen in Analytics für Zielgruppe (A4T) meldete, wenn Adobe Analytics-Code nicht in Seitenelementen vorhanden war.</li></ul> |
| 25. März | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Es wurden Informationen zu den folgenden neuen Versionen von at.js hinzugefügt:<ul><li>at.js Version 2.3.0</li><li>at.js Version 1.8.1</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Die folgenden neuen Zeilen wurden im Abschnitt &quot;Einstellungen&quot;hinzugefügt:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>Der folgende neue Abschnitt wurde hinzugefügt:<ul><li>Content Security-Richtlinie</li></ul> |
| 24. März | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact) | Es wurden Informationen zu den Auswirkungen für Folgendes hinzugefügt:<ul><li>Profil-Skripten basierend auf 3rdPartyID</li><li>QS-/Vorschauen-URLs auf iOS-Geräten</li></ul> |
| 20. März | [Versionshinweise (aktuell)](/help/r-release-notes/release-notes.md) | Die Zielgruppe Standard/Premium 20.2.1 wird am 23. März 2020 veröffentlicht. |
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
