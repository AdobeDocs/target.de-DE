---
keywords: known issues;resolved issues;release notes;bugs;issues;fixes
description: Informationen zu bekannten Problemen in dieser Version von Adobe Target. Dazu gehören auch Informationen zu Problemen, die gelöst wurden.
title: Bekannte Probleme und gelöste Probleme   in Adobe Target
feature: known issues
uuid: f8e8e057-1842-4922-ab7f-4d5441048573
translation-type: tm+mt
source-git-commit: a09a90333079a25f83a7f242e52194146a2337ab
workflow-type: tm+mt
source-wordcount: '3897'
ht-degree: 77%

---


# Bekannte Probleme und gelöste Probleme  

Informationen zu bekannten Problemen in dieser Version von Target. Dazu gehören auch Informationen zu Problemen, die gelöst wurden.

>[!NOTE]
>
>Die Ausgabennummern in Klammern dienen internen Adobe-Benutzern.

## Bekannte Probleme {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

Die folgenden Abschnitte führen bekannte Probleme bei [!DNL Target] auf:

### Analytics for Zielgruppe (A4T)-Metriken für Aktivitäten mit automatisierter Zuordnung und automatischer Zielgruppe

In der [!DNL Target] Benutzeroberfläche gibt es derzeit ein bekanntes Problem, bei dem Benutzer nicht unterstützte Interaktions- und Umsatzmetriken als Hauptzielmetrik für die Optimierung in den Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL automatische Zielgruppe] auswählen können. Konversionsmetriken werden unterstützt. Interaktions- und Umsatzmetriken werden *nicht* unterstützt. Wenn Sie Interaktions- oder Umsatzzielmetriken auswählen, wird kein Optimierungsmodell erstellt (auch wenn die [!DNL Target] Benutzeroberfläche Ihnen derzeit die Auswahl nicht unterstützter Zielmetriken erlaubt).

Eine Liste der unterstützten und nicht unterstützten Zielmetriken finden Sie unter [Unterstützte Zielmetriken](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) in *Erstellen einer Aktivität, die Analytics als Berichte-Quelle* verwendet. (TNT-38409)

### Seitenversand {#page-delivery}

Wenn Sie eine Vorlagenregel hinzufügen, z. B. URL enthält (/Checkout, /Warenkorb), werden Ihren Regeln im [Seitenversand](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md), zusätzliche Leerzeichen vorangestellt. Diese Änderung hat rein optische Auswirkungen und keinen Einfluss auf die Erstellung von Audience-Definitionen und den Versand von Angeboten. (TGT-35920)

### Links zur Qualitätssicherung Vorschau

Vorschaulinks für Aktivitäts-QAs werden möglicherweise nicht geladen, wenn im Konto zu viele gespeicherte Aktivitäten vorhanden sind. Ein erneuter Versuch mit den Vorschau-Links sollte das Problem lösen. Archivieren Sie gespeicherte Aktivitäten, die nicht mehr aktiv verwendet werden, um zu verhindern, dass dieses Problem weiterhin auftritt. (TNT-37294)

### Qualitätssicherungsmodus für Recommendations-Aktivitäten

Ein bekanntes Problem verhindert die Vorschau, wenn in der Aktivität verwendete Kriterien elementbasiert oder auf Kategorien basieren. (TNT-37455)

### Umleitungsangebote {#redirect}

Die folgenden Probleme bei Umleitungsangeboten sind bekannt:

* Eine geringe Anzahl von Kunden hat gemeldet, dass unter bestimmten Bedingungen ein höherer Grad an Varianz in der Traffic-Verteilung auftritt, wenn ein Umleitungsangebot in Aktivitäten verwendet wird, die mit Analytics for Target (A4T) konfiguriert wurden. Adobe-Techniker arbeiten derzeit an diesem Problem.
* Umleitungsaktivitäten in at.js-Implementierungen können eine Schleife der Vorschau-URL auslösen (das Angebot wird immer wieder bereitgestellt). Sie können stattdessen den [QA-Modus](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) verwenden, um Vorschau und Qualitätssicherung durchzuführen. Dieses Problem hat keine Auswirkungen auf die tatsächliche Bereitstellung des Angebots. (TGT-23019)

### Laden einer Seite im VEC abbrechen {#cancel}

* Das folgende bekannte Problem tritt derzeit auf, wenn das Laden einer Aktivität des Typs [!UICONTROL A/B-Test] oder [!UICONTROL Erlebnis-Targeting] (XT) innerhalb des VEC abgebrochen wird, die eine Umleitungs-URL enthält.

   Im Schritt eines der drei Workflows im VEC wird beim Abbrechen des Seitenladevorgangs das Bedienfeld [!UICONTROL Änderungen] im VEC angezeigt und die Umleitungs-URL wird auf das Erlebnis angewendet (z. B. Erlebnis B). Wenn Sie die Schritte zwei oder drei durchführen und dann zu Schritt 1 zurückkehren, tritt die folgende Situation auf.

   Bei „Erlebnis B“ wird standardmäßig die Vorlage für das Laden von Website-Dateien gerendert und das Bedienfeld [!UICONTROL Änderungen] kann aufgerufen werden. Dies sollte nicht der Fall sein, da eine Umleitung zu einer URL-Vorlage angewendet wird. Die Umleitung zur URL-Vorlage sollte angezeigt werden.

   So zeigen Sie den korrekten Status des Erlebnisses im VEC an:

   Wenn Sie zu einem anderen Erlebnis wechseln und dann zurück zu „Erlebnis B“ wechseln, [!DNL Target] wird die Umleitung zur URL-Vorlage angezeigt, die auf dieses Erlebnis angewendet wird, und das Bedienfeld [!UICONTROL Änderungen] kann nicht aufgerufen werden. (TGT-32138)

* Bei Websites mit einseitigen Anwendungen (SPA) können Sie beim Abbrechen der Ladevorgänge keine Aktionen im Bedienfeld [!UICONTROL Änderungen] bearbeiten.

### Recommendations

Die folgenden Probleme bei Recommendations-Aktivitäten sind bekannt:

* Entitäten verlieren ordnungsgemäß die Gültigkeit, wenn innerhalb von 60 Tagen keine Updates per Feed oder API empfangen werden. Die abgelaufenen Entitäten werden jedoch nach ihrem Ablauf nicht aus dem Katalogsuchindex entfernt. (IRI-857)
* Die Overlays „Informationen zur Verwendung“ für Kriterien und Designs entsprechen nicht ihrer Verwendung in A/B- und Erlebnis-Targeting-Aktivitäten. (TGT-34331)
* Für Recommendations-Angebote in A/B- und Erlebnis-Targeting-Aktivitäten wird keine Vorschau der Recommendations-Taskleiste angezeigt. (TGT-33426)
* Sammlungen, Ausschlüsse, Kriterien und Designs, die über die API erstellt wurden, sind in der Target-Benutzeroberfläche nicht sichtbar und können nur über die API bearbeitet werden. (TGT-35777)
* Recommendations-Aktivitäten, die über die API erstellt wurden, können zwar in der Benutzeroberfläche angezeigt, aber nur über die API bearbeitet werden.
* Der Feed-Status „Benutzerspezifische Kriterien“ in der Kriterien-Listenansicht (Karte) wird alle zehn Minuten aktualisiert und kann in seltenen Fällen mehr als zehn Minuten veraltet sein. Der in der Ansicht zur Bearbeitung benutzerdefinierter Kriterien angezeigte Status wird in Echtzeit abgerufen und ist stets auf dem neuesten Stand. (TGT-35896, TGT-36173)

### Multivarianz-Test (MVT)-Aktivitäten

In einer MVT-Aktivität ist der in der Tabelle und im Diagramm angezeigte Gewinner nicht konsistent, wenn Sie die Metriken prüfen. Dieses Phänomen tritt auf, wenn ein Benutzer von der Zusammenfassungs- zur Diagrammansicht und wieder zurück zur Zusammenfassungsansicht wechselt, eine Metrik ändert und dann zur Diagrammansicht wechselt. Wenn dieses Problem auftritt, wird in der Zusammenfassungsansicht immer der korrekte Gewinner angezeigt. Wenn der Benutzer die Diagrammansicht nie zwischen Zusammenfassungsansichten wechselt, wird in der Diagrammansicht der korrekte Gewinner angezeigt.

### at.js  {#atjs}

Bekannte Probleme mit at.js:

* Bei Verwendung von at.js-Versionen älter als 2.2.0 werden beim Klick-Tracking keine Konversionen in Analytics for Target (A4T) gemeldet, wenn der Adobe Analytics-Code nicht in Seitenelementen (wie Schaltflächen) vorhanden ist. Für dieses Problem wurde in at.js 2.2.0 eine Korrektur implementiert. Wenn dieses Problem auftritt, [führen Sie ein Upgrade auf die neueste at.js-Version durch](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).
* Wenn Sie ein Erlebnis ohne Änderungen mit at.js 2.1.1 oder einer früheren Version erstellen (z. B. ein Standarderlebnis), wird das Erlebnis möglicherweise nicht in Berichten, Analytics für Target (A4T), Adobe Analytics oder Google Analytics gezählt. Darüber hinaus funktioniert das [ttMeta-Plug-in](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md) möglicherweise nicht ordnungsgemäß.

   Verwenden Sie als Problemumgehung im Erlebnisinhalt einen Leerraum. (TNT-33366)

   >[!NOTE]
   >
   >Eine Korrektur dieses Problems wurde in at.js 2.2.0 implementiert. Sie sollten ein Upgrade auf die [neueste Version oder at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) vornehmen oder die oben genannte Problemumgehung nur für at.js-Versionen vor 2.2.0 verwenden.

* Beim Laden einer Seite in Visual Experience Composer (VEC) muss Target ermitteln, ob die globale Mbox-Einstellung aktiviert oder deaktiviert ist und ob an der Stelle, an der der Benutzer die Empfehlung im VEC anwenden möchte, ein entityID- oder categoryID-Eintrag vorhanden ist. Basierend auf diesen Informationen wird die Kriterienliste gefiltert. Die Standardliste enthält zwar gefilterte Algorithmen, doch mit dem [Kompatibilitäts-Kontrollkästchen](/help/c-recommendations/t-create-recs-activity/algo-select-recs.md) können Sie die vollständige Algorithmenliste anzeigen.

   Bei der Verwendung von at.js ist das Kontrollkästchen „Kompatibilität“ ausgeblendet, sodass Sie keine inkompatiblen Algorithmen anzeigen können.

   Dieses Problem gilt nur für Recommendations-Aktivitäten, für die VEC verwendet wird.

   **Problemumgehung**: Deaktivieren Sie die Option [!UICONTROL Inkompatible Kriterien filtern] in [!UICONTROL Recommendations > Einstellungen]. Nach dem Deaktivieren dieser Einstellung werden alle Kriterien (kompatible und inkompatible) in der Kriterienauswahl angezeigt. (TGT-25949)

* Mboxes werden in Microsoft Explorer 11-Browsern nicht ausgelöst, nachdem ein Upgrade auf die at.js-Version 1.0 ausgeführt wurde. Die Ursache dafür ist die Interaktion zwischen at.js und Visitor API 2.2.0. Dieses Problem betrifft die at.js-Version 0.9.6 und höher. (TNT-27600)
* at.js funktioniert möglicherweise nicht bei Cordova-/Hybrid-Apps, da Erstanbieter-Cookies von diesen Anwendungen nicht unterstützt werden. (TNT-26166)

   **Problemumgehung**: Konfigurieren Sie at.js mit aktivierter Option „x-only“ und übermitteln Sie `mboxThirdPartyId` in Aufrufen, um Benutzer zu verwalten.

### Erfolgsmetriken

Erfolgsmetriken mit der Einstellung der erweiterten Option „Wie wird die Zählung erhöht“ auf „Jede Impression“ oder „Jede Impression (ohne Aktualisierungen)“ können nicht als Erfolgsmetrik verwendet werden, von der eine andere Metrik abhängig ist.

Wenn eine Erfolgsmetrik bei jeder Impression erhöht werden soll, zählt Target den Besucher jedes Mal neu, sobald der Besucher diese Erfolgsmetrik besucht. Target setzt dann die Erfolgsmetrik „Mitgliedschaft“ auf 0 zurück, sodass ab der nächsten Impression wieder neu gezählt wird. Wenn also eine andere Metrik verlangt, dass diese Metrik zuerst gesehen worden sein soll, kann Target niemals erkennen, dass der Benutzer die erste Metrik gesehen hat.

### Analytics for Target (A4T)

Wenden Sie bei Verwendung von Impressionen und Konversionen der Zielgruppe in Analysis Workspace das Attribution IQ-Modell &quot;Gleich Touch&quot;auf die Metriken an, um eine genaue Zählung sicherzustellen. Um ein [nicht standardmäßiges Zuordnungsmodell](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html)anzuwenden, klicken Sie mit der rechten Maustaste auf die Metrik, um die Spalteneinstellungen zu **ändern. Aktivieren Sie &quot;Nicht standardmäßiges Zuordnungsmodell verwenden&quot;> &quot;Gleiches Touch-Modell**&quot;auswählen. Ohne Anwendung dieses Modells werden die Metriken überbewertet.

Alle aktuellen Analytics-Pakete können dieses Modell mit Attribution IQ hinzufügen. Wenn Sie keinen Zugriff auf Attribution IQ haben, verlassen Sie sich bitte auf A4T-Daten in Reports &amp; Analysen.

### Target-APIs

Kunden können keine CRUD-Vorgänge für Aktivitäten mit Automatisierte Zuordnung über die v3-Version der A/B-Aktivitäten-API auf Adobe I/O durchführen.

### GEO-Targeting

Am 10. Mai 2020 haben wir unsere GEO-Provider-Dateien aktualisiert, die einige Inkonsistenzen eingeführt haben. Beispielsweise wurden einige Werte mit Kommas hinzugefügt. obwohl die Werte in bestehenden Audiencen kein Komma hatten. Nicht alle unsere Versand-Server waren von dieser Änderung betroffen. Daher haben Audiencen, die solche Werte verwenden, möglicherweise nicht alle richtigen Besucher zwischen dem 10. Mai und dem 22. Juli 2020 qualifiziert.

### Angebote mit der Beschriftung &quot;Verarbeitung&quot;

Bei Image-Angeboten auf der Seite &quot;Angebote&quot;wird die Beschriftung &quot;Verarbeitung&quot;manchmal mehrere Stunden nach dem Hochladen der Bilder beibehalten. In den meisten Fällen handelt es sich hierbei nur um ein Problem mit der Bezeichnung: die Image-Angebot können weiterhin in Aktivitäten verwendet und bereitgestellt werden. In einigen Fällen ist jedoch unter Umständen kein Image-Angebot für die Aktion &quot;Inhalt ersetzen&quot;> &quot;Bild&quot;verfügbar. In diesem Fall sollten Sie das Image-Angebot erneut hochladen und nach einigen Stunden überprüfen, ob das Image-Angebot zum Austausch verfügbar ist. (TGT-37458)

## Gelöste Probleme {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Wenn bekannte Probleme behoben sind, werden sie in die folgenden Abschnitte verschoben und es werden ggf. zusätzliche Notizen hinzugefügt.

### Berichte für die automatische Zielgruppe {#at-metrics}

Es wurde ein Problem behoben, durch das der Berichte der [!DNL Adobe Target Premium] automatischen Zielgruppe [!UICONTROL von] Benutzern ab 15. September 2014:30 Uhr beeinträchtigt wurde. (PDT) bis 6. Oktober, 9.25 Uhr (PDT). Bei der Anzeige von Berichten für die betroffenen Konversionsmetriken (die entweder mit der Option &quot;[!UICONTROL Angezeigte Seite]&quot;oder &quot;[!UICONTROL Auf mbox]geklickt&quot;konfiguriert wurden) werden die Konversionsraten falsch gemeldet. Es ist derzeit kein Problem mit dem Versand bekannt.

So synchronisieren und korrigieren Sie Ihren Berichte:

1. Kopieren Sie die betroffenen Aktivitäten für die [!UICONTROL automatische Zielgruppe] und speichern Sie sie.
1. Aktivieren Sie die neu gespeicherten Aktivitäten (sofern die betroffenen Aktivitäten live geschaltet wurden).
1. Löschen Sie die ursprünglichen (betroffenen) Aktivitäten.

(TGT-38522, CSO 20201006007)

### Berichterstellung {#conversions-audiences}

Konversionen erhöhen sich derzeit je nach verwendeter Audience unterschiedlich.

Wenn beispielsweise für denselben Besucher die Konversionszählung auf inkrementieren &quot;Einmal pro Teilnehmer:&quot;eingestellt ist:

* Audience: &quot;Alle qualifizierten Besucher&quot;für Konversionen auf Besuchsebene werden nur einmal inkrementiert. Dies ist das erwartete Verhalten.
* Audience: &quot;Neue Besucher&quot;für Konvertierungen auf Besuchsebene werden jedes Mal falsch inkrementiert, anstatt nur einmal zu inkrementieren. Dies ist nicht das erwartete Verhalten.

Wenn die Konversionszählung auf inkrementieren &quot;Bei jedem Impression:&quot;eingestellt ist

* Audience: &quot;Alle qualifizierten Besucher&quot;für Konvertierungen auf Besucher-Ebene werden nicht jedes Mal korrekt inkrementiert, sondern nur einmal. Dies ist nicht das erwartete Verhalten.
* Audience: &quot;Neue Besucher&quot;für Konversionen auf Besucher-Ebene werden jedes Mal erhöht. Dies ist das erwartete Verhalten.

Beachten Sie, dass sich dieses Problem nur auf den [!DNL Target] Berichte bezieht. Dies ist kein Problem bei der Verwendung von [!UICONTROL Analytics for Zielgruppe] (A4T)-Berichte.

Dieses Problem wurde behoben.

### Seiten, die nicht im Visual Experience Composer (VEC) oder Enhanced Experience Composer (EEC) geladen werden, wenn Google Chrome Version 80+ verwendet wird

Dieses bekannte Problem bezieht sich auf die Entscheidung von Google, das Standardverhalten von Cookies ohne SameSite-Attribut zu ändern, beginnend mit Chrome Version 80. Vor der Änderung in Chrome wurden alle Cookies ohne das Attribut SameSite auf &quot;SameSite=None&quot;und jetzt standardmäßig auf &quot;SameSite=Lax&quot;gesetzt. Dadurch wird die Art und Weise geändert, wie Cookies bei GET- und POST-Anforderungen gesendet werden. Siehe [Gleiche Site-Aktualisierungen](https://www.chromium.org/updates/same-site).

Weitere Informationen und eine Fehlerbehebung finden Sie unter &quot;Wie wirken sich die kürzlich angekündigten Google Chrome SameSite-Cookie-Durchsetzungsrichtlinien auf VEC und EEC aus?&quot; in [Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

### Ein Diagrammbericht für eine automatische Targeting-Aktivität kann nicht gerendert werden, wenn ein benutzerdefiniertes Erlebnis als Kontrolle verwendet wird.

Ein Diagrammbericht für eine automatische Targeting-Aktivität kann für „Differenz“-Modi (durchschnittliche Steigerung und tägliche Steigerung) nicht gerendert werden, wenn in keinem Ereignis Daten vorhanden sind (0 Besuche). Diese Situation kann während der frühen Phase einer Aktivität auftreten, wenn das Kontrollerlebnis als benutzerdefiniert festgelegt ist. Für die anderen Modi (gleitendes Mittel für Kontrolle und Zielgruppe, tägliche Kontrolle und Zielgruppe sowie Besuche) funktioniert dies problemlos. Sobald einige Daten vorhanden sind (Besuche sind nicht gleich null), wird der Bericht erwartungsgemäß gerendert.

Dieses Problem wurde in Target-Version 19.7.1 behoben.

### mbox.js

Die mbox.js-Bibliothek unterstützt keine clientseitigen Vorlagensprachen wie Handlebars und Mustache. Diese Sprachen *werden* von der Bibliothek at.js unterstützt.

**Hinweis**: Die mbox.js-Bibliothek wird nicht mehr weiterentwickelt. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. Weitere Informationen finden Sie unter [Migration zu at.js von mbox.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

### Implementierung: Globale Mbox automatisch erstellen

On the Implementation tab ([!UICONTROL Administration > Implementation]) the [!UICONTROL Global Mbox Auto Create] field will be &quot;false&quot; by default for a newly provisioned tenant.

Beim ersten Herunterladen von mbox.js nach der Bereitstellung ist das Feld [!UICONTROL Globale Mbox automatisch erstellen] in der heruntergeladenen Datei mbox.js und im [!DNL Target]-Backend auf „false“ festgelegt. Es wird jedoch weiterhin als „false“ auf der Seite [!UICONTROL Implementierung] der Benutzeroberfläche angezeigt, bis die Seite aktualisiert wird (nach dem Aktualisieren der Seite lautet der Status „true“).

at.js lädt `global_mbox_autocreate = false` mit einem neu bereitgestellten Mandanten herunter. Wenn zuerst mbox.js heruntergeladen wird, wird globale\_mbox\_autocreate auf „true“ gesetzt und at.js wird ebenfalls mit `global_mbox_autocreate = true` heruntergeladen. (TGT-15929)

### Unterstützung von Enterprise-Berechtigungen in Target-APIs {#api}

Von der Target-Benutzeroberfläche in der Angebotsbibliothek erstellte Code-Angebote werden möglicherweise in der Standardarbeitsfläche angezeigt, wenn die Liste der Angebote mit GET-APIs abgerufen wird. Dieses Problem wird in der ersten Märzwoche 2019 behoben. Nach dieser Fehlerbehebung werden Codeangebote in der entsprechenden Arbeitsfläche angezeigt, wenn sie aus APIs gezogen werden. Dieses Problem betrifft *keine* von APIs erstellten Angebote. Beispielsweise werden Codeangebote, die aus APIs erstellt wurden, in der Arbeitsfläche angezeigt, in der sie erstellt wurden, unabhängig davon, ob sie über GET-APIs oder über die Target-Benutzeroberfläche abgerufen wurde.

### Berichte und extreme Bestellungen

Vom 25. November 2019 bis zum 26. April 2020 trat bei einem Zielgruppe-Server ein Problem auf, bei dem extreme Bestellwerte in umsatzbasierten Berichtsmetriken (AOV, RPV) gezählt wurden. Vom 19. Dezember 2019 bis zum 23. April 2020 trat bei einem anderen Server dasselbe Problem auf. Dieses Problem betraf nicht alle Zielgruppen- oder Zielgruppen-Server.

Sie wurden *nicht* betroffen, wenn:

* Ihre Implementierung der Zielgruppe verwendet verschiedene Server.
* Extreme Bestellungen wurden in Ihren Berichten nicht ausgeschlossen.
* Sie haben zur Messung Ihrer Aktivitäten eine Konversionsmetrik verwendet.
* Ihre Zielgruppe-Aktivitäten verwenden Analytics für die Zielgruppe (A4T).
* Sie befinden sich in der Region Asien-Pazifik (APAC).

Wenden Sie sich an den [Kundendienst](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB), um festzustellen, ob dieses Problem Ihren Zielgruppe-Berichte beeinflusst hat.

### Recommendations

* Recommendations-Feed-Index kann „Warten auf Index“ anzeigen, wenn die Elemente im Feed mit denen im vorherigen Schritt übereinstimmen. Die Produkterfassung für die Bereitstellung wird nicht beeinträchtigt. (RECS-6663)

   Dieses Problem wurde in Target-Version 19.4.2 behoben.

* Recommendations-Feeds werden langsamer verarbeitet als erwartet. (COR-2836)

   In Target-Version 16.10.1 behoben.

* In der Benutzeroberfläche von Empfehlungs-Feeds wird nicht der korrekte Indizierungsstatus angezeigt. Die Backend-Aufträge funktionieren ordnungsgemäß, aber die Benutzeroberfläche kann den aktuellen Status nicht abrufen und anzeigen.

   Dieses Problem wurde in Version 17.10.1 behoben.

### Umleitungsangebote

Eine Wettlaufsituation auf Ihrer Seite kann dazu führen, dass Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt werden. Aktualisierungen der Implementierung von at.js sind geplant, um sicherzustellen, dass solche Wettlaufsituationen vermieden werden.

Dieses Problem wurde in at.js 1.6.3 behoben.

### Ausschlussgruppen

* Beim Anwenden der automatischen Deduplizierung nach dem Erstellen von Ausschlussgruppen ist die Anzahl im Aktivitätsdiagramm auf der Benutzeroberfläche möglicherweise falsch.
* Wenn eine vorhandene Aktivität für die Ausschlussgruppe bearbeitet wird, spiegeln sich die manuellen Einschlüsse möglicherweise nicht korrekt auf der Benutzeroberfläche wider.

Diese Probleme wurden behoben.

### Target-APIs

Die v1-Version der Angebots-APIs auf Adobe I/O behandelt alle Angebote, die über Target erstellt wurden, in der Standardarbeitsfläche. (TTTEAM-41957)

Dieses Problem wurde behoben.

### at.js

Mboxes werden in Microsoft Explorer 11-Browsern nicht ausgelöst, nachdem ein Upgrade auf die at.js-Version 1.0 ausgeführt wurde. Die Ursache dafür ist die Interaktion zwischen at.js und Visitor API 2.2.0. Dieses Problem betrifft die at.js-Version 0.9.6 und höher. (TNT-27600)

Mit der Veröffentlichung von API 2.3.0 oder höher behoben.

### Geo   Targeting

Die Suche nach Zeichenfolgen, die Sonderzeichen enthalten (wie z. B. Leerzeichen oder Komma), wird bei der Erstellung von Geotargeting-Zielgruppen derzeit nicht unterstützt. Das Problem tritt beispielsweise auf, wenn Sie Zielgruppen basierend auf Städten, Bundesländern, Ländern usw. erstellen. Wenn Sie z. B. „New York“ eingeben, werden keine gültigen Suchergebnisse zurückgegeben.

Im November 2018 behoben.

### at.js

Bei der Verwendung von at.js-Version 1.6.0 treten A4T-Umleitungen (Analytics for Target) auf, jedoch ohne Aktivitätsqualifikation.

Das Problem wurde mit „at.js“-Version 1.6.2 behoben.

### Aktivitäten, Arbeitsflächen und Löschen der Aktivitäts-API

Aktivitäten im Standardarbeitsbereich, die per API gelöscht wurden, werden weiterhin in der Target-Benutzeroberfläche angezeigt. Workaround: Löschen Sie alle Aktivitäten im Standardarbeitsbereich über die Target-Benutzeroberfläche. (TGT-31315)

Behoben am 25. Oktober 2018.

### AP-Reporting (Automated Personalization) auf Angebotsebene

Wenn Sie auf das entsprechende Erlebnis im Bericht einer AP-Aktivität klicken, um Berichte auf Angebotsebene anzuzeigen, werden derzeit nur leere Ergebnisse, eine Fehlermeldung und ein Ladesymbol angezeigt. (TNT-30695)

Behoben am 27. September 2018.

### Code-Editor

Wenn Sie den VEC in Schritt 1 der Drei-Schritte-Workflows neu laden, während Sie in Firefox oder Internet Explorer mit dem Code-Editor arbeiten, wird die Registerkarte „Änderungen“ nicht ordnungsgemäß angezeigt. Die VEC-Funktionalität ist hiervon nicht betroffen. (TGT-28730)

Dieses Problem wurde in Version 18.9.1 behoben.

### Recommendations-Aktivität, die eine Attributpromotion-Regel verwendet

Wenn Sie eine Recommendations-Aktivität bearbeiten oder kopieren, für die eine Attributpromotion-Regel verwendet wird, wird beim Klicken auf Speichern der Fehler „Enthält fehlendes Feld“ angezeigt.

Dieses Problem wurde in Version 17.8.1 behoben.

### Ersatzempfehlungen

In den Sicherungsempfehlungen wird fälschlicherweise „Aktiviert“ auf den Karten vom Typ „Kürzlich angezeigte Elemente“ auf der Target-Benutzeroberfläche angezeigt. (TGT-29308)

Dieses Problem wurde in Version 18.4.1 behoben. Nun wird „Deaktiviert“ angezeigt.

### AT-(Automatisches Targeting)-Aktivitäten und Reporting-Zielgruppen

Wenn der Name einer in einer AT-(Automatisches Targeting)-Aktivität verwendeten Reporting-Zielgruppe geändert wird, schlagen weitere Updates von Target für diese Aktivität möglicherweise mit einer Fehlermeldung fehl.

Dieses Problem wurde in Target-Version 18.5.1 (22. Mai 2018) behoben.

### at.js

Der Algorithmus zum Extrahieren der Domäne der obersten Ebene, die beim Speichern von Cookies verwendet werden sollte, hat sich in at.js-Version 0.9.6 geändert. Aufgrund dieser Änderung können keine Cookies für Adressen gespeichert werden, die IP verwenden. Meist werden IP-Adressen zu Testzwecken verwendet, aber als Umgehungslösungen können Sie DNS-Einträge verwenden, die Host-Datei in einem lokalen Feld anpassen oder die at.js-Funktion targetGlobalSettings() verwenden, um ein Codefragment zur Unterstützung von IP-Adressen einzufügen.

Dieses Problem wurde in at.js-Version 1.2 behoben.

### Berechtigungen für Unternehmensbenutzer für Target Premium

Im Rahmen der Migration von Unternehmensberechtigungen wurde die gesamte Target Premium-Benutzerverwaltung von der Adobe Target-Benutzeroberfläche in die Adobe Admin Console verschoben.

Infolge der Migration liegen zwei potenzielle Probleme vor, die Sie beachten sollten:

* Nicht-Admin-Benutzer haben eine E-Mail mit dem Hinweis erhalten, dass Sie nun Zugriff auf Adobe Target haben. Dies deutet darauf hin, dass die Migration für Ihre Organisation abgeschlossen ist. Die E-Mail selbst kann ignoriert werden.
* Nach der Migration wurden einige Berichte von zuvor deaktivierten Benutzern in der Adobe Admin Console wieder angezeigt. Dies könnte für Ihre Organisation zum Problem werden, wenn vor der Migration deaktivierte Benutzer in der Adobe Admin Console weiterhin in Ihrer Benutzerliste in Target erscheinen. Es wird empfohlen, dass Administratoren die Benutzerliste in Admin Console überprüfen, um den Zugriff zu validieren.

Dieses Problem wurde am 30. August 2017 behoben.

### Aktivitätserstellung

Ein Problem mit der Version 17.6.2 hat sich möglicherweise auf Aktivitäten ausgewirkt, die zwischen dem 22. Juni und dem 29. Juni 2017 erstellt und/oder aktualisiert wurden. Aktivitäten mit folgendem Inhalt waren betroffen:

* Für Erlebnisse, die in Experience Targeting (XT) neu angeordnet wurden, wurde die originale Reihenfolge wiederhergestellt
* Lokale Segmentregeln für die Aktivität (nicht innerhalb einer Zielgruppe gespeichert) sind verloren gegangen: kombinierte Zielgruppen, Standortpräzisierungen und beliebige Regeln zu den Erfolgsmetriken.

Andere Aktivitäten waren nicht betroffen.

**Wichtig**: Dieses Problem wird nicht automatisch behoben. Sie müssen die betroffenen Aktivitäten erneut speichern, um das Problem zu beheben.

Dieses Problem wurde am 29. Juni 2017 behoben.

### Form-Based Experience Composer

Die folgenden bekannten Probleme wurden bei der Verwendung von Form-Based Experience Composer gemeldet:

* Wenn Sie den Form-Based Experience Composer mit einer anderen Mbox als der automatisch erstellten globalen Mbox (target-global-mbox) verwenden und dann eine Interaktionsmetrik als Erfolgsmetrik auswählen, dann wird die Metrik nur auf Seiten erhöht, auf denen die Mbox in der Aktivität verwendet wird. Wenn Ihre mbox beispielsweise homepage\_mbox lautet, ist die Metrik „Seiten pro Besuch“ die Anzahl der Treffer für homepage\_mbox während des Besuchs. (TGT-22789)
* Es wird eine JavaScript-Ausnahme ausgegeben, wenn Sie den Form-Based Experience Composer in Schritt 1 des Prozesses verwenden und ein Erlebnis in einer Experience Targeting (XT)-Aktivität löschen. (TGT-24366)

Das erste Problem wurde in Target-Version 17.3.1 behoben (März 2017).

Das zweite Problem wurde in Target-Version 17.6.1 behoben (Juni 2017).

### at.js

Seit der Einführung von Target 17.4.1 (27. April 2017) führt die Verwendung der Aktion „Bild einfügen“ im Visual Experience Composer (VEC) dazu, dass der Angebotsinhalt beim Verwenden der at.js-Bibliothek nicht bereitgestellt wird.

In der at.js-Version 0.9.7, die am 22. Mai 2017 veröffentlicht wurde, ist dieses Problem behoben worden.

### Berichterstattung: A/B- und Experience Targeting (XT)-Aktivitäten

Zwischen dem 27. April (21:00 PST) und 5. Mai (6:00 PST) enthielten A/B- und XT-Aktivitäten, die mit einer beliebigen Metrik und der Konversionsaktion „Angezeigte Seite“ (die nicht auf anderen Metriken basieren) erstellt oder bearbeitet wurden, möglicherweise falsch aufgezeichnete Konversionen. Dieses Problem wurde nun behoben. Jedoch ist die Berichterstellung für die Konversionsaktion „Angezeigte Seite“ zu diesen Aktivitäten während des betroffenen Zeitraums möglicherweise nicht exakt und leider nicht korrigierbar. Es wird empfohlen, sich bei Entscheidungen auf der Grundlage von Konversionsaktionen vom Typ „Angezeigte Seite“ ausschließlich auf Daten zu verlassen, die vor oder nach dem betroffenen Zeitraum aufgezeichnet wurden.

Berichterstellungsdaten für andere Metriken können weiterhin verwendet werden, weil sie nicht betroffen waren.

Im Target-Hotfix 17.4.3 behoben.

### Angebote: A/B- und Experience Targeting (XT)-Aktivitäten

Die Bereitstellung und Vorschau war bei Angeboten in A/B- und XT-Aktivitäten eingeschränkt, die mindestens zwei Erlebnisse enthielten und mit dem Form-Based Experience Composer zwischen Freitag, dem 28. April (21:00 PT) und Montag, dem 1. Mai (21:15 PT), erstellt oder bearbeitet wurden. Es wurden nur Angebote mit Standardinhalt angezeigt.

Im Target-Hotfix 17.4.3 behoben.

### at.js

Die folgenden Aktionen haben dazu geführt, dass das Angebot bei der Verwendung des Visual Experience Composers (VEC) und der at.js-Funktion zum Verschieben und Neuanordnen nicht bereitgestellt wurde.

Dieses Problem wurde in at.js-Version 0.9.6 behoben.

### Berichte

Die Möglichkeit mehrere Metriken in einem Bericht anzuzeigen, die mit Target 17.3.1 (30. März 2017) eingeführt worden war, wurde entfernt, weil es zu unerwartetem Verhalten kam. Diese Funktion wird in einer zukünftigen Version wieder verfügbar sein.

Die Möglichkeit, mehrere Metriken in einem Bericht anzuzeigen, besteht seit Target-Version 17.4.1 (27. April 2017).

### Angebote

Aus der Bildangebotsbibliothek gelöschte Bilder (Angebote > Bildangebote) bleiben in der Benutzeroberfläche sichtbar. In einer kommenden Version werden keine gelöschten Bilder mehr angezeigt. In der Zwischenzeit werden gelöschte Bilder auf der Benutzeroberfläche mit dem Status Gelöscht angezeigt. (TGT-23793)

In Target 17.4.1 (27. April 2017) behoben.

### Umleitungsangebote

Für die Kriterien vom Typ „Kürzlich angesehen“ ziehen auf Entitäten basierende dynamische Regeln keine Empfehlung nach sich, wenn der Parameter entity.id in der Mbox-Anfrage nicht gesendet wird. (RECS-6241)

Dieses Problem wurde nach der Recommendations-Version (22. März 2018) behoben. Nach der Recommendations-Version überspringt Target die auf der Entität basierenden dynamischen Regeln, wenn entity.id in der Mbox-Anfrage nicht gesendet wird.

### at.js

Wenn Benutzer versuchen, at.js von der Seite mit Implementierungsdetails herunterzuladen, nachdem sie die at.js-Einstellungen geändert haben, wird mbox.js statt at.js heruntergeladen. (TGT-23069)

In Target-Version 17.3.1 (30. März 2017) behoben.

### Globale Ausschlussregeln

Es dauert 10 bis 20 Minuten, bis globale Ausschlussregeln an Recommendations Premium propagiert sind. (RECS-5270)

In Recommendations 17.2.2.0 (6. März 2017) behoben.

### Berichterstellung von Analytics for Target (A4T)

Berichte werden nicht aktualisiert, wenn die Berichtsmetrik geändert wird. Es handelt sich dabei um ein Problem der Benutzeroberfläche. Dies hat keine Auswirkung auf die Erfassung oder Bereitstellung von Berichtsdaten. (TGT-22970)

In Target 17.2.2.0 (24. Februar 2017) behoben.

### CSV-Berichte

In heruntergeladenen Berichten wird die Einstellung Extreme Bestellungen ausschließen ignoriert. (TGT-21871)

In Target-Version 17.2.1.0 behoben.
