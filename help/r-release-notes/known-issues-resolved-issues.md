---
keywords: Bekannte Probleme;gelöste Probleme;Versionshinweise;Fehler;Probleme;Fehlerbehebungen
description: Hier finden Sie Informationen zu bekannten Problemen in Adobe Target, einschließlich Informationen zur Problemumgehung. Gelöste Probleme werden in den Abschnitt „Gelöst“ verschoben.
title: Wo finde ich Informationen zu bekannten Problemen und gelösten Problemen?
feature: Versionshinweise
exl-id: 6eb854f7-ed46-4673-afeb-0b44970598cd
source-git-commit: 131a938470a45144ad3ab487b6bccfa306abcaf1
workflow-type: tm+mt
source-wordcount: '4505'
ht-degree: 97%

---

# Bekannte Probleme und gelöste Probleme

Informationen zu bekannten Problemen in [!DNL Adobe Target]. Dazu gehören auch Informationen zu Problemen, die gelöst wurden.

>[!NOTE]
>
>Die Problemnummern in Klammern dienen internen Adobe-Benutzern.

## Bekannte Probleme {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

Die folgenden Abschnitte führen bekannte Probleme bei [!DNL Target] auf:

### Traffic-Verteilung von Aktivitäten mit automatisierter Zuordnung mithilfe von A4T {#aa-a4t}

In einigen Fällen kann die Traffic-Verteilung von [!UICONTROL Aktivitäten mit automatischer Zuordnung], die [!UICONTROL Analytics for Target] (A4T) verwenden, von der gemeldeten Konversionsrate der einzelnen Erlebnisse abweichen. Dies tritt häufiger bei Aktivitäten mit einem hohen Anteil an rückkehrendem Besucher-Traffic auf. Betroffene Kunden werden über betroffene Aktivitäten benachrichtigt.

Bis dieses Problem behoben ist, verwenden Sie [!UICONTROL Automatische Zuordnung] mit standardmäßigen [!DNL Target]-Berichten oder verwenden Sie standardmäßige A/B-Tests mit [!DNL Analytics]-Berichten als Alternative zu [!UICONTROL Automatische Zuordnung] mit [!DNL Analytics]-Berichten. (Die 131 populärsten)

### Analytics for Adobe Target (A4T)-Metriken für automatische Zuordnungs- und Targeting-Aktivitäten

In der Benutzeroberfläche von [!DNL Target] können Benutzer nicht unterstützte Interaktions- und Umsatzmetriken als primäre Zielmetrik für die Optimierung in [!UICONTROL automatischen Zuordnungs]- und [!UICONTROL automatischen Targeting]-Aktivitäten auswählen. Konversionsmetriken werden unterstützt, Interaktions- und Umsatzmetriken dagegen *nicht*. Wenn Sie als Zielmetriken Interaktions- oder Umsatzmetriken auswählen, wird kein Optimierungsmodell erstellt.

Eine Liste der unterstützten und nicht unterstützten Zielmetriken finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md). (TNT-38409)

### Der Enhanced Experience Composer (EEC) unterstützt keine PUT-Anfragen.

Ein Problem mit dem EEC verhindert derzeit, dass PUT-Anfragen unterstützt werden, und führt zu einem 504-Timeout-Fehler. (TGT-41493)

### [!DNL Adobe Experience Platform] Segmentnamen werden nicht im Bericht [!UICONTROL Wichtige Attribute] angezeigt.

[!DNL Adobe Experience Platform] Segmentnamen werden für die Aktivitäten [!UICONTROL Automatisierte Personalisierung] (AP) und [!UICONTROL Automatisches Targeting] (AT) nicht im Bericht [!UICONTROL Wichtige Attribute] angezeigt. (Die 3813 populärsten)

### Die Archivierung von Aktivitäten mit [!UICONTROL automatischem Targeting] kann zu Synchronisationsproblemen führen.

Der Versuch, inaktive Aktivitäten für [!UICONTROL Automatisches Targeting] zu archivieren, kann zu Synchronisationsproblemen führen. Solange dieses Problem nicht behoben ist, archivieren Sie die Aktivitäten für [!UICONTROL Automatisches Targeting] nicht. Belassen Sie sie im Status [!UICONTROL Inaktiv]. (TGT-40885)

### Seitenversand {#page-delivery}

Wenn Sie eine Vorlagenregel hinzufügen, z. B. URL enthält (/Checkout, /Warenkorb), werden Ihren Regeln im [Seitenversand](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md), zusätzliche Leerzeichen vorangestellt. Diese zusätzlichen Leerzeichen haben einen rein kosmetischen Zweck und wirken sich nicht auf die Erstellung von Zielgruppen und die Bereitstellung von Angeboten aus. (TGT-35920)

### Vorschaulinks für QA

Vorschaulinks für die Aktivitäts-QA gespeicherter Aktivitäten werden möglicherweise nicht geladen, wenn im Konto zu viele gespeicherte Aktivitäten vorhanden sind. Versuchen Sie die Vorschaulinks erneut zu laden. Das Problem lässt sich in der Regel durch regelmäßige Archivierung nicht mehr aktiv verwendeter gespeicherter Aktivitäten verhindern. (TNT-37294)

### QA-Modus für Recommendations-Aktivitäten

Ein bekanntes Problem verhindert die Vorschau, wenn die in einer Aktivität verwendeten Kriterien auf Elementen oder Kategorien basieren. (TNT-37455)

### Umleitungsangebote {#redirect}

Die folgenden Probleme bei Umleitungsangeboten sind bekannt:

* Von einigen wenigen Kunden wurde zurückgemeldet, dass in der Traffic-Verteilung ein höherer Grad an Varianzen auftritt, wenn Umleitungsangebote in Aktivitäten verwendet werden, die mit Analytics for Target (A4T) konfiguriert wurden.
* Umleitungsaktivitäten in at.js-Implementierungen können eine Schleife der Vorschau-URL auslösen (das Angebot wird immer wieder bereitgestellt). Sie können stattdessen den [QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) verwenden, um Vorschau und Qualitätssicherung durchzuführen. Dieses Problem hat keine Auswirkungen auf die tatsächliche Bereitstellung des Angebots. (TGT-23019)

### Problem beim Abbrechen des Seitenladevorgangs in Visual Experience Composer (VEC) {#cancel}

* Das folgende bekannte Problem tritt derzeit auf, wenn das Laden einer Aktivität des Typs [!UICONTROL A/B-Test] oder [!UICONTROL Erlebnis-Targeting] (XT) innerhalb des VEC abgebrochen wird, die eine Umleitungs-URL enthält.

   Im ersten Schritt des durch VEC angeleiteten Workflows wird beim Abbrechen des Seitenladevorgangs das Bedienfeld [!UICONTROL Änderungen] im VEC angezeigt und die Umleitung zur URL-Vorlage wird auf das Erlebnis angewendet (z. B. Erlebnis B). Wenn Sie die Schritte zwei oder drei durchführen und dann zu Schritt 1 zurückkehren, tritt die folgende Situation auf.

   Bei „Erlebnis B“ wird standardmäßig die Vorlage für das Laden von Website-Dateien gerendert und das Bedienfeld [!UICONTROL Änderungen] kann aufgerufen werden. Dies sollte nicht der Fall sein, da eine Umleitung zu einer URL-Vorlage angewendet wird. Die Umleitung zur URL-Vorlage sollte angezeigt werden.

   So zeigen Sie den korrekten Status des Erlebnisses im VEC an:

   Wenn Sie zu einem anderen Erlebnis und dann zurück zu „Erlebnis B“ wechseln, zeigt [!DNL Target] die auf dieses Erlebnis angewendete Umleitung zur URL-Vorlage an, und das Bedienfeld [!UICONTROL Änderungen] ist nicht abrufbar. (TGT-32138)

* Bei Websites mit einseitigen Anwendungen (SPA) können Sie beim Abbrechen der Ladevorgänge keine Aktionen im Bedienfeld [!UICONTROL Änderungen] bearbeiten.

### Recommendations

Die folgenden Probleme bei [!UICONTROL Recommendations]-Aktivitäten sind bekannt:

* Wenn eine [!UICONTROL Recommendations]-Aktivität mit einer aktiven Promotion kopiert wird, wirkt sich jede Änderung an der kopierten bzw. der ursprünglichen Aktivität derzeit auch auf das Original bzw. die Kopie aus. (TGT-39155)

   Temporäre Umgehung:

   * Deaktivieren Sie die Promotion von Aktivitäten.
   * Kopieren Sie die Aktivität.
   * Aktivieren Sie die Promotions in jeder Aktivität wieder.

* Wenn [!DNL Target] ein JSON-Angebot mit getOffer() zurückgibt, wird der JSON-Typ zurückgegeben. Ein JSON Recommendations-Design hingegen wird mit einem HTML-Typ zurückgegeben.
* Entitäten verlieren ordnungsgemäß die Gültigkeit, wenn innerhalb von 60 Tagen keine Updates per Feed oder API empfangen werden. Die abgelaufenen Entitäten werden jedoch nach ihrem Ablauf nicht aus dem Katalogsuchindex entfernt. (IRI-857)
* Die Overlays „Informationen zur Verwendung“ für Kriterien und Designs entsprechen nicht ihrer Verwendung in A/B- und Erlebnis-Targeting-Aktivitäten. (TGT-34331)
* Für Recommendations-Angebote in A/B- und Erlebnis-Targeting-Aktivitäten wird keine Vorschau der Recommendations-Taskleiste angezeigt. (TGT-33426)
* Sammlungen, Ausschlüsse, Kriterien und Designs, die über die API erstellt wurden, sind in der Benutzeroberfläche von Target nicht sichtbar und können nur über die API bearbeitet werden. Erstellen Sie umgekehrt eines dieser Elemente in der Benutzeroberfläche von Target und bearbeiten Sie diese später über die API, werden die Änderungen nicht in der Benutzeroberfläche von Target angezeigt. Über die API bearbeitete Elemente sollten weiterhin über die API bearbeitet werden, um sicherzustellen, dass keine Änderungen verloren gehen. (TGT-35777)
* Recommendations-Aktivitäten, die über die API erstellt wurden, können zwar in der Benutzeroberfläche angezeigt, aber nur über die API bearbeitet werden.
* Der Feed-Status „Benutzerspezifische Kriterien“ in der Kriterien-Listenansicht (Karte) wird alle zehn Minuten aktualisiert und kann in seltenen Fällen mehr als zehn Minuten veraltet sein. Der in der Bearbeitungsansicht für benutzerdefinierte Kriterien angezeigte Status wird in Echtzeit abgerufen und ist stets auf dem neuesten Stand. (TGT-35896, TGT-36173)
* In Kriterien- und Designkarten ist die Anzahl der Aktivitäten, in denen sie verwendet werden, nicht korrekt angegeben. Wenn ein Kriterium oder ein Design in einer A/B-Aktivität verwendet wird, gibt die Karte möglicherweise fälschlich an, dass das Kriterium oder Design nicht verwendet wird. (TGT-36621, TGT-37217)

### Multivarianz-Test (MVT)-Aktivitäten

In einer MVT-Aktivität ist der in der Tabelle und im Diagramm angezeigte Gewinner bei der Überprüfung der Metriken möglicherweise nicht identisch. Diese Situation tritt ein, wenn ein Benutzer von der Zusammenfassungs- zur Diagrammansicht und wieder zurück zur Zusammenfassungsansicht wechselt, eine Metrik ändert und dann zur Diagrammansicht wechselt. Wenn dieses Problem auftritt, wird in der Zusammenfassungsansicht immer der korrekte Gewinner angezeigt. Wenn der Benutzer die Diagrammansicht nie zwischen Zusammenfassungsansichten wechselt, wird in der Diagrammansicht der korrekte Gewinner angezeigt.

### at.js {#atjs}

Bekannte Probleme mit at.js:

* Bei Verwendung einer at.js-Version vor 2.2.0 werden beim Klick-Tracking keine Konversionen in Analytics for Target (A4T) gemeldet, wenn der Adobe Analytics-Code nicht in Seitenelementen (z. B. Schaltflächen) vorhanden ist. Für dieses Problem wurde in at.js 2.2.0 eine Korrektur implementiert. Wenn dieses Problem auftritt, [führen Sie ein Upgrade auf die neueste at.js-Version durch](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).
* Wenn Sie ein Erlebnis ohne Änderungen mit at.js 2.1.1 oder einer früheren Version erstellen (z. B. ein Standarderlebnis), wird das Erlebnis möglicherweise nicht in Berichten, Analytics for Target (A4T), Adobe Analytics oder Google Analytics gezählt. Darüber hinaus funktioniert das ttMeta-Plug-in möglicherweise nicht ordnungsgemäß.

   Verwenden Sie als Problemumgehung im Erlebnisinhalt einen Leerraum. (TNT-33366)

   >[!NOTE]
   >
   >Eine Korrektur dieses Problems wurde in at.js 2.2.0 implementiert. Führen Sie das Upgrade auf die [neueste Version von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) durch oder verwenden Sie die oben genannte Problemumgehung, jedoch nur für at.js-Versionen vor 2.2.0.

* Beim Laden einer Seite in Visual Experience Composer (VEC) muss Target ermitteln, ob die globale Mbox-Einstellung aktiviert oder deaktiviert ist und ob an der Stelle, an der der Benutzer die Recommendation in VEC anwenden möchte, ein entityID- oder categoryID-Eintrag vorhanden ist. Basierend auf diesen Informationen wird die Kriterienliste gefiltert. Die Standardliste enthält zwar gefilterte Algorithmen, doch mit dem [Kompatibilitäts-Kontrollkästchen](/help/c-recommendations/t-create-recs-activity/algo-select-recs.md) können Sie die vollständige Algorithmenliste anzeigen.

   Bei der Verwendung von at.js ist das Kontrollkästchen „Kompatibilität“ ausgeblendet, sodass Sie keine inkompatiblen Algorithmen anzeigen können.

   Dieses Problem gilt nur für Recommendations-Aktivitäten, für die VEC verwendet wird.

   **Problemumgehung**: Deaktivieren Sie die Option [!UICONTROL Inkompatible Kriterien filtern] in [!UICONTROL Recommendations > Einstellungen]. Nach dem Deaktivieren dieser Einstellung werden alle Kriterien (kompatible und inkompatible) in der Kriterienauswahl angezeigt. (TGT-25949)

* Mboxes werden in Microsoft Explorer 11-Browsern nicht ausgelöst, nachdem ein Upgrade auf die at.js-Version 1.0 ausgeführt wurde. Die Ursache dafür ist die Interaktion zwischen at.js und Visitor API 2.2.0. Dieses Problem betrifft die at.js-Version 0.9.6 und höher. (TNT-27600)
* at.js funktioniert möglicherweise nicht bei Cordova-/Hybrid-Apps, da Erstanbieter-Cookies von diesen Anwendungen nicht unterstützt werden. (TNT-26166)

   **Problemumgehung**: Konfigurieren Sie at.js mit aktivierter Option „x-only“ und übermitteln Sie `mboxThirdPartyId` in Aufrufen, um Benutzer zu verwalten.

### Erfolgsmetriken

Erfolgsmetriken, für die die Einstellung der erweiterten Option „Wie wird die Zählung erhöht“ auf „Jede Impression“ oder „Jede Impression (ohne Aktualisierungen)“ gesetzt ist, können nicht als Erfolgsmetrik mit einer abhängigen Metrik verwendet werden.

Wenn eine Erfolgsmetrik so eingestellt ist, dass sie bei jeder Impression erhöht wird, zählt Target den Besucher jedes Mal neu, wenn er diese Erfolgsmetrik besucht. Target setzt dann die Erfolgsmetrik „Mitgliedschaft“ auf 0 zurück, sodass ab der nächsten Impression wieder neu gezählt wird. Wenn also eine andere Metrik verlangt, dass diese Metrik zuerst gesehen werden muss, kann Target nicht erkennen, dass der Benutzer diese erste Metrik bereits gesehen hat.

### Analytics for [!DNL Target] (A4T)

Wenn Sie in Analysis Workspace Target-Aktivitätsimpressionen und -konversionen verwenden, sollten Sie auf die Metriken das Attribution IQ-Modell „Selber Kontakt“ anwenden, um eine genaue Zählung sicherzustellen. Zum Anwenden eines [nicht standardmäßigen Attributionsmodells](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/visualizations/freeform-table/column-row-settings/column-settings.html?lang=de#cja-workspace) klicken Sie mit der rechten Maustaste auf die Metrik, um **die Spalteneinstellungen zu ändern. Aktivieren Sie dann „Nicht standardmäßiges Attributionsmodell verwenden“ und wählen Sie das Modell „Selber Kontakt“ aus**. Ohne Anwendung dieses Modells werden die Metriken überbewertet.

Alle aktuellen Analytics-Pakete können dieses Modell mit Attribution IQ hinzufügen. Falls Sie keinen Zugriff auf Attribution IQ haben, greifen Sie auf die A4T-Daten in Reports &amp; Analytics zurück.

### Target-APIs

Kunden können keine CRUD-Vorgänge für Aktivitäten mit Automatisierte Zuordnung über die v3-Version der A/B-Aktivitäten-API auf Adobe I/O durchführen.

### Geotargeting

Am 10. Mai 2020 wurden von Adobe die GEO-Provider-Dateien aktualisiert, wodurch einige Inkonsistenzen entstanden sind. Beispielsweise wurden einige Werte mit Kommas hinzugefügt, obwohl die Werte in bestehenden Zielgruppen keine Kommas enthielten. Nicht alle Adobe-Bereitstellungsserver waren von dieser Änderung betroffen. Für Zielgruppen, die solche Werte verwenden, sind daher möglicherweise noch nicht alle richtigen Besucher zwischen dem 10. Mai und dem 22. Juli 2020 qualifiziert.

### Berichte – Die Daten des herunterladbaren CSV-Berichts sind mit den in der [!DNL Target]-Benutzeroberfläche angezeigten Berichtsdaten nicht identisch. {#csv}

Berichte, die als CSV-Dateien zum Herunterladen generiert wurden, sind nicht konsistent, wenn die Aktivität mehr als eine Metrik verwendet. Der herunterladbare Bericht wird nur auf der Grundlage der Berichtseinstellungen generiert und geht bei allen anderen verwendeten Metriken von demselben Wert aus.

Der korrekte Bericht ist immer der in der Benutzeroberfläche von [!DNL Target] angezeigte Bericht.

## Gelöste Probleme {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Bekannte Probleme, die behoben wurden, werden in die folgenden Abschnitte verschoben. Gegebenenfalls finden Sie dort zusätzliche Hinweise.

### Bildangebote mit der Bezeichnung „Verarbeitung“

Bildangebote auf der Seite „Angebote“ tragen gelegentlich noch mehrere Stunden nach dem Upload der Bilder die Bezeichnung „Verarbeitung“. In den meisten Fällen handelt es sich jedoch nur um ein Problem mit der Bezeichnung. Die Bildangebote können dennoch in Aktivitäten verwendet und bereitgestellt werden. (MCUI-10264, TGT-37458)

Dieses Problem wurde in der Standard- und Premium-Version von Target 20.10.1 behoben.

### Reporting von Analytics for Adobe Target (A4T)

Die folgenden Probleme in Verbindung mit A4T wurden behoben:

* Ein Problem, das sich auf A4T-Aktivitäten mit einer [!DNL Analytics]-Zielmetrik auswirkte und dazu führte, dass A4T-Berichte eine unerwartete Traffic-Aufteilung oder extrem überhöhte Konversionen anzeigten.

   Dieses Problem wirkte sich unter folgenden Bedingungen auf A4T-Berichte aus:

   * Die Aktivität wurde zwischen dem 15. September und dem 5. November 2020, 4.00 Uhr (PST), erstellt oder gespeichert.
   * Für die Aktivität war eine [!DNL Analytics]-Metrik als Zielmetrik ausgewählt.

   [!DNL Target] teilte den Traffic während dieser Zeit korrekt auf. Jedoch kam es beispielsweise vor, dass eine 50/50-Aufteilung in der Aktivitätskonfiguration im A4T-Bericht als 90/10-Aufteilung ausgegeben wurde.

   Für Besucher, die eine betroffene Aktivität nach dem 5. November, 4.00 Uhr (PST), zum ersten Mal anzeigten, wurde und wird die Traffic-Aufteilung korrekt angezeigt. Auch bei neuen Aktivitäten, die nach diesem Datum erstellt oder gespeichert wurden, wird der Traffic korrekt angegeben.

* Ein Problem, das sich auf A4T-Aktivitäten mit einer [!DNL Target]-Zielmetrik auswirkte und dazu führte, dass A4T-Berichte zu niedrige oder gar keine Konversionen zurückgaben.

   >[!NOTE]
   >
   >Dieses Problem betraf nur A4T-Berichte. Die Bereitstellung der Aktivitäten war davon nicht betroffen.

   Dieses Problem wirkte sich unter folgenden Bedingungen auf A4T-Berichte aus:

   * Die A4T-Aktivität war zwischen dem 22. September und dem 11. November 2020, 14.30 Uhr (PST), aktiv.
   * Für die Aktivität war eine [!DNL Target]-Metrik als Zielmetrik ausgewählt.
   * Wenn ein Besucher das Zielereignis der Aktivität auswählte (z. B. [!UICONTROL auf ein Element klickte]), wurde gleichzeitig eine Nicht-A4T-Aktivität mit niedrigerer Priorität ausgeführt, die mit dem Konversionsereignis übereinstimmte. Dies geschah, wenn die Nicht-A4T-Aktivität mit derselben Metrik wie die A4T-Aktivität oder mit der Metrik „any mbox“ konfiguriert war.

   Dieses Problem wirkte sich auf die Zurückmeldung von A4T-Aktivitäten aus, die zwischen dem 22. September und dem 11. November 2020, 14.30 Uhr (PST), aktiv waren. Außerhalb dieses Zeitfensters wurden die Konversionen der betroffenen A4T-Aktivitäten korrekt zurückgemeldet. Berichte für Nicht-A4T-Aktivitäten waren davon nicht betroffen.

Bei Fragen wenden Sie sich an Ihren Kundenbetreuer (CSM) oder an die [Adobe-Kundenunterstützung](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). (CSO 20201110016)

### Berichte für automatisches Targeting {#at-metrics}

Ein Problem, das sich bei [!DNL Adobe Target Premium]-Benutzern zwischen dem 15. September, 14.30 Uhr (UTC−7), und dem 6. Oktober, 9.25 Uhr (UTC−7), auf Berichte zum [!UICONTROL automatischen Targeting] auswirkte, wurde behoben. In den Berichten werden die Konversionsraten der betroffenen Konversionsmetriken (konfiguriert mit [!UICONTROL Angezeigte Seite] oder [!UICONTROL Auf mbox geklickt]) nicht korrekt angezeigt. Ein Problem mit der Bereitstellung ist derzeit nicht bekannt.

So synchronisieren und korrigieren Sie die Berichte:

1. Kopieren Sie die betroffenen Aktivitäten für [!UICONTROL automatisches Targeting] und speichern Sie die Kopien.
1. Aktivieren Sie die neu gespeicherten Aktivitäten (sofern die betroffenen Aktivitäten aktiv waren).
1. Löschen Sie die ursprünglichen, d. h. die betroffenen Aktivitäten.

(TGT-38522, CSO 20201006007)

### Berichterstellung {#conversions-audiences}

Je nach Zielgruppe erhöhen sich Konversionen derzeit unterschiedlich.

Ist beispielsweise für den gleichen Besucher die Erhöhung der Konversionszählung auf „Einmal pro Teilnehmer“ eingestellt,

* erhöhen sich die Konversionen auf Besuchsebene bei der Zielgruppe „Alle qualifizierten Besucher“ nur einmal. Dies ist das erwartete Verhalten.
* Bei der Zielgruppe „Neue Besucher“ erhöhen sich die Konversionen auf Besuchsebene dagegen fälschlicherweise jedes Mal, anstatt nur einmal. Dies ist ein nicht erwartetes Verhalten.

Ist die Erhöhung der Konversionszählung auf „Bei jeder Impression“ eingestellt,

* erhöhen sich die Konversionen auf Besuchsebene bei der Zielgruppe „Alle qualifizierten Besucher“ fälschlicherweise nur einmal, anstatt jedes Mal. Dies ist ein nicht erwartetes Verhalten.
* Bei der Zielgruppe „Neue Besucher“ erhöhen sich die Konversionen auf Besuchsebene dagegen jedes Mal. Dies ist das erwartete Verhalten.

Dieses Problem betrifft nur die Berichterstellung in [!DNL Target]. Die Berichterstellung von [!UICONTROL Analytics for Target] (A4T) ist davon nicht betroffen.

Dieses Problem wurde behoben.

### Bei Verwendung von Google Chrome ab Version 80 werden Seiten in Visual Experience Composer (VEC) oder Enhanced Experience Composer (EEC) nicht geladen.

Dieses bekannte Problem hat seine Ursache in der Entscheidung von Google, das Standardverhalten von Cookies ohne SameSite-Attribut ab Chrome Version 80 zu ändern. Vor dieser Änderung lautete der Standardwert in Chrome für alle Cookies ohne SameSite-Attribut „SameSite=None“. Ab Version 80 lautet der Standardwert „SameSite=Lax“. Dadurch ändert sich die Übertragungsmethode für Cookies bei GET- und POST-Anforderungen. Weitere Informationen finden Sie unter [SameSite-Updates](https://www.chromium.org/updates/same-site).

Weitere Informationen sowie eine Lösung zur Fehlerbehebung finden Sie unter [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite) unter der Frage „Wie wirken sich die kürzlich von Google Chrome angekündigten Cookie-Durchsetzungsrichtlinien für SameSite auf VEC und EEC aus?“.

### Ein Diagrammbericht für eine automatische Targeting-Aktivität kann nicht gerendert werden, wenn ein benutzerdefiniertes Erlebnis als Kontrolle verwendet wird.

Ein Diagrammbericht für eine automatische Targeting-Aktivität kann für „Differenz“-Modi (durchschnittliche Steigerung und tägliche Steigerung) nicht gerendert werden, wenn in keinem Ereignis Daten vorhanden sind (0 Besuche). Diese Situation kann während der frühen Phase einer Aktivität auftreten, wenn das Kontrollerlebnis als benutzerdefiniert festgelegt ist. Für die anderen Modi (gleitendes Mittel für Kontrolle und Zielgruppe, tägliche Kontrolle und Zielgruppe sowie Besuche) funktioniert dies problemlos. Sobald einige Daten vorhanden sind (Besuche sind nicht gleich null), wird der Bericht erwartungsgemäß gerendert.

Dieses Problem wurde in Target-Version 19.7.1 behoben.

### Implementierung: Globale Mbox automatisch erstellen

Bei einem neu bereitgestellten Mandanten ist das Feld [!UICONTROL Globale Mbox automatisch erstellen] auf der Registerkarte „Implementierung“ ([!UICONTROL Administration > Implementierung]) standardmäßig auf „false“ gesetzt.

Beim ersten Herunterladen von mbox.js nach der Bereitstellung ist das Feld [!UICONTROL Globale Mbox automatisch erstellen] in der heruntergeladenen Datei mbox.js und im [!DNL Target]-Backend auf „false“ festgelegt. Es wird jedoch weiterhin als „false“ auf der Seite [!UICONTROL Implementierung] der Benutzeroberfläche angezeigt, bis die Seite aktualisiert wird (nach dem Aktualisieren der Seite lautet der Status „true“).

at.js lädt `global_mbox_autocreate = false` mit einem neu bereitgestellten Mandanten herunter. Wenn zuerst mbox.js heruntergeladen wird, wird globale\_mbox\_autocreate auf „true“ gesetzt und at.js wird ebenfalls mit `global_mbox_autocreate = true` heruntergeladen. (TGT-15929)

### Unterstützung für Enterprise-Berechtigungen in [!DNL Target]-APIs {#api}

Von der Target-Benutzeroberfläche in der Angebotsbibliothek erstellte Code-Angebote werden möglicherweise im Standardarbeitsbereich angezeigt, wenn die Liste der Angebote mit GET-APIs abgerufen wird. Dieses Problem wird in der ersten Märzwoche 2019 behoben. Nach dieser Fehlerbehebung werden Code-Angebote im entsprechenden Arbeitsbereich angezeigt, wenn sie aus APIs gezogen werden. Dieses Problem betrifft *keine* von APIs erstellten Angebote. Beispielsweise werden Code-Angebote, die aus APIs erstellt wurden, im Arbeitsbereich angezeigt, in der sie erstellt wurden, unabhängig davon, ob sie über GET-APIs oder über die Target-Benutzeroberfläche abgerufen wurden.

### Berichte und extreme Bestellungen

Vom 25. November 2019 bis zum 26. April 2020 trat bei einem Target-Server ein Problem auf, das dazu führte, dass in den umsatzbasierten Berichtsmetriken AOV und RPV extreme Bestellwerte gezählt wurden. Vom 19. Dezember 2019 bis zum 23. April 2020 trat dasselbe Problem auch bei einem anderen Server auf. Von diesem Problem waren nicht alle Target-Server und nicht alle Target-Kunden betroffen.

Sie waren unter den folgenden Bedingungen *nicht* betroffen:

* Ihre Target-Implementierung verwendet verschiedene Server.
* Extreme Bestellungen waren in Ihren Berichten nicht ausgeschlossen.
* Zum Messen Ihrer Aktivitäten verwendeten Sie eine Konversionsmetrik.
* Sie nutzen für Ihre Target-Aktivitäten Analytics for Target (A4T).
* Sie befinden sich in der Region Asien-Pazifik (APAC).

Wenn Sie überprüfen möchten, ob Ihre Target-Berichte von diesem Problem betroffen waren, wenden Sie sich an die [Adobe-Kundenunterstützung](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB).

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

Die v1-Version der Angebots-APIs auf Adobe I/O behandelt alle Angebote, die über Target erstellt wurden, im Standardarbeitsbereich. (TTTEAM-41957)

Dieses Problem wurde behoben.

### at.js {#at-js-2}

Mboxes werden in Microsoft Explorer 11-Browsern nicht ausgelöst, nachdem ein Upgrade auf die at.js-Version 1.0 ausgeführt wurde. Die Ursache dafür ist die Interaktion zwischen at.js und Visitor API 2.2.0. Dieses Problem betrifft die at.js-Version 0.9.6 und höher. (TNT-27600)

Mit der Veröffentlichung von API 2.3.0 oder höher behoben.

### Geo Targeting

Die Suche nach Zeichenfolgen, die Sonderzeichen enthalten (wie z. B. Leerzeichen oder Komma), wird bei der Erstellung von Geotargeting-Zielgruppen derzeit nicht unterstützt. Das Problem tritt beispielsweise auf, wenn Sie Zielgruppen basierend auf Städten, Bundesländern, Ländern usw. erstellen. Wenn Sie z. B. „New York“ eingeben, werden keine gültigen Suchergebnisse zurückgegeben.

Im November 2018 behoben.

### at.js {#at-js-3}

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

### Recommendations

In den Sicherungsempfehlungen wird fälschlicherweise „Aktiviert“ auf den Karten vom Typ „Kürzlich angezeigte Elemente“ auf der Target-Benutzeroberfläche angezeigt. (TGT-29308)

Dieses Problem wurde in Version 18.4.1 behoben. Nun wird „Deaktiviert“ angezeigt.

### Automatisches Targeting-(AT)-Aktivitäten und Reporting-Zielgruppen

Wenn der Name einer in einer Automatisches Targeting (AT)-Aktivität verwendeten Reporting-Zielgruppe geändert wird, schlagen weitere Updates von Target für diese Aktivität möglicherweise mit einer Fehlermeldung fehl.

Dieses Problem wurde in Target-Version 18.5.1 (22. Mai 2018) behoben.

### at.js {#at-js-4}

Der Algorithmus zum Extrahieren der Domäne der obersten Ebene, die beim Speichern von Cookies verwendet werden sollte, hat sich in at.js-Version 0.9.6 geändert. Aufgrund dieser Änderung können keine Cookies für Adressen gespeichert werden, die IP verwenden. Meist werden IP-Adressen zu Testzwecken verwendet, aber als Umgehungslösungen können Sie DNS-Einträge verwenden, die Host-Datei in einem lokalen Feld anpassen oder die at.js-Funktion targetGlobalSettings() verwenden, um ein Codefragment zur Unterstützung von IP-Adressen einzufügen.

Dieses Problem wurde in at.js-Version 1.2 behoben.

### Enterprise-Benutzerberechtigungen für [!DNL Target] Premium

Im Rahmen der Migration von Enterprise-Berechtigungen wurde die gesamte Target Premium-Benutzerverwaltung von der Adobe Target-Benutzeroberfläche in die Adobe Admin Console verschoben.

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
* Es wird eine JavaScript-Ausnahme ausgegeben, wenn Sie den Form-Based Experience Composer in Schritt 1 des Prozesses verwenden und ein Erlebnis in einer Experience Targeting-(XT)-Aktivität löschen. (TGT-24366)

Das erste Problem wurde in Target-Version 17.3.1 behoben (März 2017).

Das zweite Problem wurde in Target-Version 17.6.1 behoben (Juni 2017).

### at.js {#at-js-5}

Seit der Einführung von Target 17.4.1 (27. April 2017) führt die Verwendung der Aktion „Bild einfügen“ im Visual Experience Composer (VEC) dazu, dass der Angebotsinhalt beim Verwenden der at.js-Bibliothek nicht bereitgestellt wird.

In der at.js-Version 0.9.7, die am 22. Mai 2017 veröffentlicht wurde, ist dieses Problem behoben worden.

### Berichterstattung: A/B- und Experience Targeting (XT)-Aktivitäten

Zwischen dem 27. April (21:00 PST) und 5. Mai (6:00 PST) enthielten A/B- und XT-Aktivitäten, die mit einer beliebigen Metrik und der Konversionsaktion „Angezeigte Seite“ (die nicht auf anderen Metriken basieren) erstellt oder bearbeitet wurden, möglicherweise falsch aufgezeichnete Konversionen. Dieses Problem wurde nun behoben. Jedoch ist die Berichterstellung für die Konversionsaktion „Angezeigte Seite“ zu diesen Aktivitäten während des betroffenen Zeitraums möglicherweise nicht exakt und leider nicht korrigierbar. Es wird empfohlen, sich bei Entscheidungen auf der Grundlage von Konversionsaktionen vom Typ „Angezeigte Seite“ ausschließlich auf Daten zu verlassen, die vor oder nach dem betroffenen Zeitraum aufgezeichnet wurden.

Berichterstellungsdaten für andere Metriken können weiterhin verwendet werden, weil sie nicht betroffen waren.

Im Target-Hotfix 17.4.3 behoben.

### Angebote: A/B- und Experience Targeting (XT)-Aktivitäten

Die Bereitstellung und Vorschau war bei Angeboten in A/B- und XT-Aktivitäten eingeschränkt, die mindestens zwei Erlebnisse enthielten und mit dem Form-Based Experience Composer zwischen Freitag, dem 28. April (21:00 PT) und Montag, dem 1. Mai (21:15 PT), erstellt oder bearbeitet wurden. Es wurden nur Angebote mit Standardinhalt angezeigt.

Im Target-Hotfix 17.4.3 behoben.

### at.js {#at-js-6}

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

### at.js {#at-js-7}

Wenn Benutzer versuchen, at.js von der Seite mit Implementierungsdetails herunterzuladen, nachdem sie die at.js-Einstellungen geändert haben, wird mbox.js statt at.js heruntergeladen. (TGT-23069)

In Target-Version 17.3.1 (30. März 2017) behoben.

### Globale Ausschlussregeln

Es dauert 10 bis 20 Minuten, bis globale Ausschlussregeln an Recommendations Premium propagiert sind. (RECS-5270)

In Recommendations 17.2.2.0 (6. März 2017) behoben.

### Reporting von Analytics for Adobe Target (A4T)

Berichte werden nicht aktualisiert, wenn die Berichtsmetrik geändert wird. Dieses Problem betrifft nur die Benutzeroberfläche. Dies hat keine Auswirkung auf die Erfassung oder Bereitstellung von Berichtsdaten. (TGT-22970)

In Target 17.2.2.0 (24. Februar 2017) behoben.

### CSV-Berichte

In heruntergeladenen Berichten wird die Einstellung Extreme Bestellungen ausschließen ignoriert. (TGT-21871)

In Target-Version 17.2.1.0 behoben.
