---
keywords: Änderungsprotokoll zur Target-Dokumentation; Aktualisierungen in der Dokumentation; neue Themen; Bearbeitungen; Aktualisierungen; Aktualisierung
description: Halten Sie sich mit wichtigen Ergänzungen und Änderungen an der Produktdokumentation der Adobe [!DNL Target] auf dem Laufenden.
title: Wo finde ich Informationen zu Änderungen an der Target-Dokumentation?
feature: Versionshinweise
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
translation-type: tm+mt
source-git-commit: 5d3d284f75ee00b7fd92b0083c6009334a5db2e5
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 61%

---

# Dokumentationsänderungen

Auf dieser Seite sind wichtige Änderungen an der Produktdokumentation von [!DNL Adobe Target] zusammengefasst.

## Adobe [!DNL Target] Standard/Premium 21.4.1 (19. April 2021)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 10. Mai | Recommendations-FAQs | Folgende häufig gestellte Fragen wurden hinzugefügt: &quot;Kann ich einen Algorithmus verwenden, der in [!DNL Adobe Recommendations Classic] in [!DNL Recommendations Premium] erstellt wurde?&quot; |
| 6. Mai | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Folgende FAQs wurden hinzugefügt:<ul><li>Wie lange dauert es, bis die Konfiguration meiner [!UICONTROL Recommendations]-Aktivität, Angebot-, Promo- oder Kriterieneinstellungen auf meiner Site geändert wird?</li><li>Wie lange dauert es, bis das Verhalten eines Benutzers (z. B. beim Klicken auf Produkt A und beim Kauf von Produkt B) in den Empfehlungen für *angezeigt wird, die der Benutzer* erhält?</li><li>Wie lange dauert es, bis das Verhalten eines Benutzers (z. B. Klicken auf Produkt A und Kauf von Produkt B) in den Empfehlungen für *andere* Benutzer angezeigt wird?</li></ul> |
|  | [Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) | Es wurde ein Link zum folgenden Blog-Beitrag im Adobe Tech Blog hinzugefügt:<ul><li>Teil 1: Adobe Target NodeJS SDK für Experimentieren und Personalisierung auf Edge-Plattformen (Akamai Edge Workers) ausführen</li></ul> |
| 5. Mai | [Target-Ankündigungen und -Ereignisse](/help/r-release-notes/target-announcements.md) | Es wurden Informationen zur Adobe Target Community Q&amp;A Coffee Break hinzugefügt, die am Mittwoch, den 12. Mai 2021 um 8 Uhr stattfinden wird. (PDT, GMT-7). |
| 27. April | [Cookie-Einstellungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | Thema aktualisiert, um anzugeben, dass die Cookie-Dauer (`deviceIdLifetime`-Einstellung) in at.js Version 2.3.1 oder höher überschrieben werden kann. |
|  | [Adobe Target-Handbuch](/help/target-home.md) | Es wurden Informationen zum Gipfeltreffen zur Adobe hinzugefügt. |
| 26. April | [Fehlerbehebung bei der Entscheidung für &quot;at.js&quot;auf dem Gerät](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/troubleshooting-on-device-decisioning.md) | Neues Thema |
| 19. April | [Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) | Die folgenden neuen Artikel wurden hinzugefügt:<ul><li>[Geräteinterne Entscheidungsfindung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)</li><li>[Unterstützte Funktionen für die Entscheidungsfindung auf dem Gerät](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)</li><li>[Artefakt der Entscheidungsregel auf dem Gerät](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md)</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#on-device-decisioning) | Es wurden Informationen hinzugefügt über `decisioningMethod`. |
|  | [adobe.target.getOffers() - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Es wurde Folgendes hinzugefügt:<ul><li>Informationen zum Schlüssel `decisioningMethod`.</li><li>Ein Beispiel für &quot;getCallOffers()&quot;, um eine geräteinterne Entscheidungsfindung vorzunehmen.</li></ul> |
|  | [Benutzerdefinierte at.js-Ereignisse](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | Folgende Informationen wurden hinzugefügt:<ul><li>Artefakt bei der Entscheidungsfindung auf dem Gerät erfolgreich</li><li>Artefakt bei der Entscheidungsfindung auf dem Gerät fehlgeschlagen</li></ul> |
|  | [Aktivitäten](/help/c-activities/activities.md) | Es wurden Informationen zur Entscheidungsfindung auf dem Gerät hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informationen zur at.js-Version 2.5.0 wurden hinzugefügt. |
|  | [Implementieren von Target ohne einen Tag-Manager](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md) | Es wurden Informationen zur Entscheidungsfindung auf dem Gerät hinzugefügt. |
|  | [Aktivitäts-QA](/help/c-activities/c-activity-qa/activity-qa.md) | Mit [at.js 2.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) wurde Unterstützung für Vorschauen-Links für [!UICONTROL Automated Personalization]-Aktivitäten hinzugefügt. |
|  | [Verwenden dynamischer und statischer Einschlussregeln](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators) | Es wurden Informationen zu den folgenden neuen Operatoren hinzugefügt:<ul><li>in Liste</li><li> ist nicht in der Liste enthalten</li><li>Liste enthält ein Element in</li><li>Liste enthält kein Element in</li><li>Liste enthält alle Elemente in</li><li>Liste enthält nicht alle Elemente in</li></ul> |
|  | [Adobe Target-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html)<br> (*Experience Cloud Services und* Administrationshandbuch) | Es wurden zusätzliche Informationen zur &quot;Sitzungs-ID&quot;hinzugefügt. |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.4.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe [!DNL Target] Standard/Premium 21.2.1 (9. März 2021)

| Datum | Thema | Änderungen |
| --- | --- | --- |
| 9. April | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Informationen zur Vorabversion von at.js Version 2.5.0 hinzugefügt (19. April 2021) |
| 9. April | [Target-Versionshinweise (Vorabversion)](/help/r-release-notes/target-release-notes.md) | Informationen zur Vorabversion für die Version 21.4.1 von Target Standard/Premium hinzugefügt (19. April 2021) |
|  | [Integration von Recommendations in E-Mail](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | Es wurde ein Hinweis mit Kapazitätsrichtlinien für die Optionen 1 und 2 hinzugefügt. |
| 29. März | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#persist-across-devices) | Neue FAQs hinzugefügt:<ul><li>Bestehen Empfehlungen, die auf kürzlich angezeigten Artikeln basieren, für einen Besucher auf mehreren Geräten?</li></ul> |
| 23. März | [Versionshinweise](/help/r-release-notes/release-notes.md) | Versionshinweise für at.js-Version 2.4.1 hinzugefügt. |
|  | [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Versionshinweise für at.js-Version 2.4.1 hinzugefügt. |
|  | [Recommendations-FAQs](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Die folgende häufig gestellte Frage wurde aktualisiert:<ul><li>Wie lange dauert es, bis Aktualisierungen an Elementen in meinem Katalog auf meiner Site erscheinen?</li></ul> |
| 22. März | [Von Recommendations-Feed verarbeitenden Servern verwendete IP-Adressen](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md) | Die Liste der IP-Adressen wurde aktualisiert. |
|  | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md) | Der Abschnitt &quot;Anzahl der Entitäten&quot;unter &quot;Entitäten&quot;wurde aktualisiert. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Informationen zur at.js-Version 2 wurden hinzugefügt.** xunder &quot;Wie kann ich meine Aktivitäten testen, als ob ich ein Benutzer bin, der von einem anderen Ort kommt?&quot; |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.2.1 | Folgender Abschnitt wurde hinzugefügt: <ul><li>Änderungen der IP-Adresse für Recommendations-Feed-Verarbeitungsserver (16. März 2021)</li></ul> |
| 19. März | [Anzeigen von Berichten – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#deactivated) | Folgende häufig gestellte Fragen wurden hinzugefügt:<ul><li>Warum sehe ich nach der Deaktivierung meiner Aktivität weiterhin mehr Impressionen?</li></ul> |
| 12. März | [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md#tutorial) | Das folgende neue Tutorial wurde hinzugefügt:<ul><li>Einrichten von A4T-Berichten in Analysis Workspace für automatische Targeting-Aktivitäten</li></ul> |
| 9. März | [Beschränkungen](/help/r-troubleshooting-target/target-limits.md#offer-size) | <ul><li>Die zulässigen Größenbeschränkungen für Angebote wurden aktualisiert.</li><li>Die Zeichenbeschränkung für den Parameter „categoryId“ wurde korrigiert.</li></ul> |
|  | [Zulassungsliste für Target-Edge-Knoten](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | Die IP-Adressen des [!DNL Target]-Edge wurden aktualisiert. |
|  | [Entitätsattribute](/help/c-recommendations/c-products/entity-attributes.md) | Der Text wurde erweitert und gibt nun an, dass entity.value ein Dezimalformat aufweisen muss (z. B. 15.99 anstelle von 15,99). |
|  | [Versionshinweise](/help/r-release-notes/release-notes.md): 21.2.1 | Diese Version enthält Verbesserungen und Fehlerbehebungen. In den Versionshinweisen können Sie die Informationen dazu lesen und den Links zur Dokumentation folgen. Diese Version umfasst auch einige Aktualisierungen zur Dokumentation in der Hilfe. |

## Adobe [!DNL Target] Standard/Premium 21.1.1 (19. Januar 2021)

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
