---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 92f5953a96b92175784600d1b04a23ec4d7152ec
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 24%

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>* **Adobe nochmal als Führer im Gartner Magic Quadrant für Personalisierungsmaschinen**: Adobe wurde im dritten Gartner Magic Quadrant for Personalization Engines 2020-Bericht erneut zum Leader ernannt. Der Gartner Magic Quadrant for Personalization Engines bewertete Anbieter anhand von 15 Kriterien, die in zwei Kategorien unterteilt sind: Vollständigkeit der Sicht und Ausführungsfähigkeit. [Lesen Sie mehr darüber im Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **&quot;mbox.js&quot;-Einstellung**: Am 18. Januar 2021 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 18. Januar 2021 schlagen alle von &quot;mbox.js&quot;ausgeführten Aufrufe korrekt fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite &quot;Ankündigungen&quot;der Zielgruppe finden Sie Informationen zu den bevorstehenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 20.8.3 (15. September 2020)

| Funktion | Details |
| --- | --- |
| ![Premium-Badge](/help/assets/premium.png) Analytics for Zielgruppe (A4T)-Unterstützung für Aktivitäten mit automatischer Zielgruppe | [!UICONTROL Aktivitäten der automatischen Zielgruppe] unterstützen jetzt [Analytics für die Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Diese Integration ermöglicht es Ihnen, mithilfe des [!UICONTROL Automatisch Zielgruppe] Lernalgorithmus ein optimales Erlebnis für jeden Besucher anhand seines Profils, seines Verhaltens und seines Kontexts zu wählen.<br>Wenn Sie bereits A4T [für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben, sind Sie alle bereit!<br>Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T)-Unterstützung für Aktivitäten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) zur automatischen Zuordnung und automatischen Zielgruppe bei der Erstellung von *Aktivitäten*. |

## Target Standard/Premium 20.8.2 (10. September 2020)

| Funktion | Details |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) Control-Empfehlungen-Slots innerhalb von Kriteriensequenzen | Kriteriensequenzen ermöglichen es Ihnen jetzt, die Anzahl der Slots zu steuern, die von den einzelnen Empfehlungskriterien aufgenommen wurden. So können Sie verschiedene Elementtypen oder verschiedene Algorithmuslogiken kombinieren und zuordnen.<br>Weitere Informationen finden Sie unter Kriteriensequenzen [erstellen](/help/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) . |

## Target Standard/Premium 20.8.1 (2. September 2020)

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der dazu führte, dass beim Laden der neuen [!UICONTROL Administrationsseiten] nach dem Wechsel der Organisation Fehler angezeigt wurden. (TGT-37730)
* Korrektur eines Anzeigefehlers, der dazu führte, dass auf der Seite [!UICONTROL Administration > Implementierung] der falsche Clientcode angezeigt wurde. (TGT-37849)
* Es wurde ein Problem behoben, das Benutzer manchmal daran hinderte, die Bearbeitungsfunktionen im [!UICONTROL Visual Experience Composer] (VEC) zu verwenden, nachdem VEC erfolgreich geladen wurde. (TGT-37162)
* Es wurde ein Fehler behoben, der verhinderte, dass Seiten in VEC und Enhanced Experience Composer (EEC) geladen wurden, obwohl die VEC Helper-Erweiterung installiert war. Dies war auf Änderungen in Google Chrome 80+ zurückzuführen. Laden Sie die [aktualisierte VEC Helper-Erweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)herunter. (TGT-37893)
* Es wurde ein Problem behoben, das manchmal verhinderte, dass Benutzer at.js von der Seite [!UICONTROL Administration > Implementierung] herunterladen konnten, nachdem sie das Unternehmen gewechselt hatten. (TGT-37668)
* Die Download-Schaltfläche von at.js ist jetzt beim Laden deaktiviert, um zu verhindern, dass mehrere Anforderungen gesendet werden, wenn Benutzer mehrmals auf die Download-Schaltfläche klicken. [!DNL Target] (TGT-37633)
* Es wurde ein Fehler in den Aktivitäten [!UICONTROL Erlebnis-Targeting] (XT) behoben, der dazu führte, dass Erlebnisse über einen längeren Zeitraum &quot;Ergebnisse abrufen&quot;angezeigt wurden. (TGT-37684)
* Verbesserte Navigation und Funktionalität für Benutzer, die nur über Tastatur verfügen. (TGT-34479 und TGT-34473)
* Es wurden Beschriftungen in der Benutzeroberfläche hinzugefügt, um Benutzern mithilfe von Hilfstechnologien zu helfen. (TGT-34480)
* Die Fehlermeldung beim Löschen eines mobilen Viewports, der derzeit in einer Aktivität verwendet wird, wurde verbessert. Die Fehlermeldung lautet jetzt: &quot;Dieser Viewport ist derzeit einer oder mehreren Aktivitäten zugeordnet. Sie müssen den Viewport aus diesen Aktivitäten entfernen, bevor Sie ihn löschen können.&quot; (TGT-37030)
* Unterstützung im VEC hinzugefügt, um die Klick-Verfolgung auf einem CSS-Selektor zuzulassen, der mehr als einem Element auf der Seite entspricht. (TGT-37323)
* Es wurde ein Fehler behoben, der verhinderte, dass bestimmte Benutzer die Liste [!UICONTROL Aktivität] anzeigen konnten. Die folgende Fehlermeldung wurde angezeigt: &quot;URL-Vorschläge können nicht abgerufen werden.&quot; Der Fehler trat bei Benutzern auf, die Wagenrückgaben in ihrem Vornamen (Vorname/r/n) im Backend-System der Adobe verwenden. (TGT-37330)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer die Seite &quot; [!UICONTROL Aktivität] &quot;anzeigen konnten, wenn der Arbeitsflächenname (in [!UICONTROL Adobe Admin Console für Enterprise]angegeben) einen Apostroph enthielt. (TGT-37709)
* Es wurde ein Problem in den Aktivitäten zur [!UICONTROL automatischen Zuordnung] bei der Auswahl von Optimierungs- und Konversionsmetriken behoben, bei dem eine Fehlermeldung fälschlicherweise die Benutzer zur Auswahl einer Report Suite informierte, obwohl bereits eine Report Suite angegeben wurde. (TGT-37689)
* Es wurde ein Fehler behoben, der manchmal dazu führte, dass Metriken auf der Seite &quot; [!UICONTROL Ziele und Einstellungen] &quot;leer waren, nachdem sie zur Seite &quot; [!UICONTROL Targeting] &quot;und dann zurück navigiert wurden. (TGT-37691)
* Es wurde ein Fehler behoben, der zu einem falschen Wert mit der letzten Änderung für [!DNL Recommendations] Kriterien führte. (TGT-37666)
* Es wurde ein Fehler behoben, der dazu führte, dass Mbox-IDs in der Dropdown-Liste &quot;Mboxes&quot;anstelle von Mbox-Namen angezeigt wurden. (TGT-37739)

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - serverseitige APIs der Zielgruppe](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu Adobe Targets serverseitigen APIs. |
| [Versionshinweise - Zielgruppe Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK &quot;Node.js&quot;. |
| [Versionshinweise - Zielgruppe Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Versionshinweise zum Java-SDK von Adobe Target. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der Adobe Target at.js JavaScript-Bibliothek. |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek &quot;mbox.js&quot;nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu [Experience Cloud](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
