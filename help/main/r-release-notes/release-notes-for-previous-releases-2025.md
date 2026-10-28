---
keywords: Versionshinweise;Vorabversionshinweise;zukünftige Verbesserungen;zukünftige Fehlerbehebungen;zukünftige Funktionen;bevorstehende Version
description: Dieser Abschnitt enthält eine Liste der Funktionen, Verbesserungen und Fehlerbehebungen früherer Versionen von Adobe Target.
title: Welche Funktionen sind in früheren Versionen von 2025 enthalten?
feature: Release Notes
TQID: 'https://experienceleague.adobe.com/cjheajZKokzwCNspfQckh6PHh5ecetdj7vZrrq9IqXw'
source-git-commit: 7f111df77c4b368dbe000a699ee19f5ff1ea266f
workflow-type: tm+mt
source-wordcount: '25402'
ht-degree: 5%
---
# Versionshinweise für vorherige Versionen

Versionshinweise für frühere Versionen von [!DNL Adobe Target] einschließlich Versionshinweisen für [!DNL Target Standard/Premium], die [!DNL Target]-Plattform und die [!DNL Target] JavaScript-Bibliothek (at.js).

Die Versionshinweise sind in absteigender Reihenfolge nach Monat und Jahr der Veröffentlichung aufgeführt.

>[!NOTE]
>
>Informationen zu den Target-Versionen (Plattform und Target Standard/Premium) finden Sie unter [Target-Versionshinweise (aktuell)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A).

## Versionshinweise für 2025

### [!DNL Target Standard/Premium] 25.11.2 (14. November 2025)

**Decisioning-Angebote**

+++Details anzeigen

* **Angebotsentscheidungen mit ausgeblendeten oder ungültigen Selektoren können in der aktualisierten Benutzeroberfläche nicht bearbeitet werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Angebotsentscheidungen, die an ausgeblendete oder ungültige Selektoren gebunden waren, nicht bearbeitet werden konnten, es sei denn, das Element war im Visual Experience Composer (VEC) sichtbar. Die Bearbeitung wird jetzt direkt über das Bedienfeld unterstützt, wodurch die in der alten Benutzeroberfläche verfügbaren Funktionen wiederhergestellt werden und sichergestellt wird, dass Angebotsentscheidungen unabhängig von der Sichtbarkeit der Auswahl geändert werden können. (TGT-53899)

+++

**Recommendations**

+++Details anzeigen

* **Das Bearbeiten von Kriterien in einer Aktivität führte zum Absturz der Seite.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die Bearbeitung von Aktivitätskriterien dazu führte, dass die Seite mit Konsolenfehlern im Zusammenhang mit `useCrudActionsCtx` abstürzte. Der Kriterieneditor wird jetzt korrekt geladen und funktioniert, sodass Aktivitäten ohne Unterbrechung bearbeitet werden können. (TGT-53971)
* **[!UICONTROL Nachricht]-Spalte konnte in der aktualisierten Benutzeroberfläche gelegentlich keine Produktdaten anzeigen.** Es wurde ein Problem in der aktualisierten [!UICONTROL Recommendations]-Benutzeroberfläche behoben, bei dem in der Spalte [!UICONTROL Nachricht] in der [!UICONTROL Katalogsuche] gelegentlich keine Produktdaten angezeigt wurden, obwohl im Feed Werte vorhanden waren. Die Spalte zeigt nun konsistent die richtigen Nachrichtenwerte für alle Produkte an und gewährleistet so eine zuverlässige Sichtbarkeit, ohne dass die Spalte manuell neu konfiguriert werden muss. (TGT-52777)
* **[!UICONTROL Schaltfläche „Recommendations-] herunterladen“ ist nach dem Speichern der Aktivität in der aktualisierten Benutzeroberfläche nicht sichtbar.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Recommendations-Daten herunterladen] für bestimmte gespeicherte Aktivitäten auch nach dem erneuten Speichern nicht angezeigt wurde. Die Schaltfläche wird jetzt über alle Aktivitäten hinweg konsistent angezeigt, sodass Benutzerinnen und Benutzer Empfehlungsdaten zuverlässig exportieren können, ohne Problemumgehungen zu benötigen. (TGT-53802)
* **Beim Öffnen bestimmter Produkte aus einer Sammlung wird „Angeforderte Ressource wurde nicht gefunden“ zurückgegeben, und dem Modal fehlt eine Option zum Schließen.** Es wurde ein Problem in der aktualisierten Recommendations-Benutzeroberfläche behoben, bei dem das Öffnen bestimmter Produkte aus einer Sammlung den Fehler „Angefragte Ressource wurde nicht gefunden“ auslöste und ein leeres modales Fenster ohne eine Option zum Schließen anzeigte. Das Modal lädt Produktdetails jetzt korrekt, und es steht immer eine Option zum Schließen zur Verfügung, um es elegant zu beenden. (TGT-53986)

+++

## [!DNL Target Standard/Premium] 25.11.1 (10. November 2025)


**Analytics for Target (A4T)**

+++Details anzeigen

* **[!UICONTROL Ziele und Einstellungen] Fehlermeldung bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle in der aktualisierten Benutzeroberfläche.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche [!UICONTROL Übersicht] behoben, bei dem im Abschnitt Ziele der Fehler „Irgendetwas ist schiefgelaufen“ angezeigt wurde. Wir können Ihre Anfrage nicht bearbeiten. Wenden Sie sich an [!DNL Adobe Client Care], wenn das Problem weiterhin besteht, wenn [!DNL Adobe Analytics] (A4T) als Berichtsquelle ausgewählt wurde. Die Ziele werden jetzt mit [!UICONTROL Adobe Analytics]-Metriken korrekt angezeigt, was eine konsistente Sichtbarkeit über alle Berichtsquellen hinweg gewährleistet. (TGT-54021)

+++

**Zielgruppen**

+++Details anzeigen

* **In der aktualisierten Benutzeroberfläche können nicht mehrere Reporting-Zielgruppen ausgewählt werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Benutzende beim Bearbeiten einer Aktivität nicht mehrere neu erstellte Reporting-Zielgruppen gleichzeitig auswählen konnten. Es können jetzt mehrere Zielgruppen gleichzeitig zugewiesen werden, was die Flexibilität und Effizienz bei der Einrichtung von Berichten verbessert. (TGT-53253)

+++

**Decisioning-Angebote**

+++Details anzeigen

* **Entscheidungsangebote können in der aktualisierten Benutzeroberfläche nicht bearbeitet oder ersetzt werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Decisioning-Angebote nicht über das Bedienfeld [!UICONTROL Änderungen] bearbeitet oder ersetzt werden konnten und Angebotsnamen leer erschienen. Entscheidungsangebote sind jetzt vollständig barrierefrei und bearbeitbar, sodass die Parität mit der veralteten Benutzeroberfläche wiederhergestellt wird und sichergestellt ist, dass Kunden Angebote direkt in -Aktivitäten verwalten können. (TGT-53884)

+++

**Lokalisierung**

+++Details anzeigen

* **Korrektur mehrerer Lokalisierungsfehler in der koreanischen und japanischen Benutzeroberfläche.** (TGT-54003, TGT-54004, TGT-54006, TGT-54007 UND TGT-54018)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen

* **Bei der Promotion nach Attribut mit Entitätsattribut-Übereinstimmung konnte der Empfehlungsschlüssel nach dem Speichern der Aktivität nicht geladen werden.** Es wurde ein Problem behoben, bei dem Promotions des Typs [!UICONTROL Promotion nach Attribut] mit dem Regeltyp [!UICONTROL Entitätsattributübereinstimmung] beim Bearbeiten nach dem Speichern einer Aktivität den Empfehlungsschlüssel nicht geladen haben. Das Problem wurde dadurch verursacht, dass der `customKeyId` nicht über GraphQL angefordert wurde. Empfehlungsschlüssel werden jetzt während der Bearbeitung der Promotion korrekt geladen. (TGT-53117)
* **Empfehlung bleibt beim Wechsel von ExpB zu ExpA visuell erhalten.** Es wurde ein Problem behoben, bei dem durch Einfügen einer Empfehlung in Erlebnis B und anschließendem Wechsel zu Erlebnis A das Feld für Empfehlungsangebote sichtbar blieb. Dies war lediglich eine visuelle Inkonsistenz. Änderungen werden beim Wechseln zwischen Erlebnissen jetzt korrekt dargestellt, wodurch ein genaues Benutzeroberflächenverhalten sichergestellt wird. (TGT-53911)
* **Empfehlungsschlüssel wird für [!UICONTROL Promotion nach Attribut] nicht geladen, wobei [!UICONTROL Entitätsattribut] übereinstimmt.** Es wurde ein Problem behoben, bei dem Promotions des Typs [!UICONTROL Promotion nach Attribut] mit dem Regeltyp [!UICONTROL Entitätsattributübereinstimmung] den Empfehlungsschlüssel beim Bearbeiten nach dem Speichern einer Aktivität nicht geladen haben. Der Empfehlungsschlüssel wird jetzt korrekt über GraphQL abgerufen, sodass die Promotions wie erwartet angezeigt und funktionieren. (TGT-53917)
* **Bearbeiten von Empfehlungen für ausgeblendete HTML-Elemente funktioniert nicht in der aktualisierten Benutzeroberfläche.** Es wurde ein Problem in der Benutzeroberfläche [!UICONTROL Neu erstellen] und VEC behoben, bei dem Empfehlungsaktivitäten, die auf ausgeblendete HTML-Elemente angewendet wurden, nicht bearbeitet werden konnten. Diese Funktion funktioniert jetzt erwartungsgemäß und stellt die Parität mit der veralteten Benutzeroberfläche wieder her. Außerdem wird sichergestellt, dass Empfehlungen unabhängig von der Sichtbarkeit der Elemente geändert werden können. (TGT-53953)
* **Empfehlungsaktivitäten für ausgeblendete HTML-Elemente in der aktualisierten Benutzeroberfläche können nicht bearbeitet werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Empfehlungsaktivitäten, die auf ausgeblendete HTML-Elemente angewendet wurden, nicht bearbeitet werden konnten. Diese Funktion funktioniert jetzt erwartungsgemäß und stellt die Parität mit der veralteten Benutzeroberfläche wieder her. Außerdem wird sichergestellt, dass Empfehlungen unabhängig von der Sichtbarkeit der Elemente geändert werden können. (TGT-53951)
* **Im Empfehlungskatalog fehlen in der aktualisierten Benutzeroberfläche gelegentlich Attributwerte.** Es wurde ein Problem in der aktualisierten [!UICONTROL Recommendations]-Benutzeroberfläche behoben, bei dem in Katalogsuchlisten gelegentlich bestimmte Attributwerte (z. B. Nachricht) nicht angezeigt wurden, selbst wenn sie im Produkt-Feed vorhanden waren. Attributwerte werden jetzt konsistent in Suchergebnissen geladen, ohne dass eine Spaltenumkonfiguration erforderlich ist. Dies verbessert die Zuverlässigkeit und Effizienz der Katalogverwaltung. (TGT-52769)
* **[!UICONTROL Download Recommendations]-Schaltfläche fehlt für [!DNL Recommendations] Aktivitäten in der aktualisierten Benutzeroberfläche.** Es wurde ein Problem in der aktualisierten [!DNL Recommendations]-Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Empfehlungen herunterladen] für A/B-Aktivitäten, die Recommendations verwenden, nicht sichtbar war. Die Schaltfläche wird jetzt korrekt angezeigt, sodass Benutzende Empfehlungsdaten wie erwartet exportieren können, was der Funktionalität in der alten Benutzeroberfläche entspricht. (TGT-53768)
* **[!UICONTROL Schaltfläche „Empfehlungsdaten herunterladen] fehlt in der aktualisierten Benutzeroberfläche „Übersicht“.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche [!UICONTROL Übersicht] behoben, bei dem die Schaltfläche [!UICONTROL Empfehlungsdaten herunterladen] für Aktivitäten mit Empfehlungen nicht sichtbar war. Die Schaltfläche wird jetzt korrekt angezeigt, sodass Benutzende Recommendations-Daten direkt exportieren können, ohne zur alten Benutzeroberfläche zurückkehren zu müssen. (TGT-53772)
* **Das Bearbeiten von Aktivitätskriterien führte in der aktualisierten Benutzeroberfläche manchmal zu einem leeren Bildschirm.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem das Klicken [!UICONTROL Kriterien in Erlebnissen bearbeiten] gelegentlich zu einem leeren Bildschirm für bestimmte Aktivitäten führte. Der Kriterieneditor wird jetzt zuverlässig über alle Aktivitäten hinweg geladen, sodass Benutzer ihn ohne Unterbrechung bearbeiten können. (TGT-53961)
* **Sequenzkriterien können in der aktualisierten Benutzeroberfläche nicht bearbeitet werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem der Versuch, [!UICONTROL Sequenzkriterien] zu bearbeiten, dazu führte, dass das Kriterienpopup beim Laden hängen blieb und dann einen leeren Bildschirm anzeigte. Der Kriterieneditor wird jetzt korrekt geladen, sodass Benutzer Sequenzkriterien ohne Unterbrechung bearbeiten und aktualisieren können. (TGT-53985)

+++

**[!UICONTROL Berichte]**

+++Details anzeigen

* **[!UICONTROL MVT-] (Multivariate Test) und Diagrammberichterstattungsprobleme verhinderten die Berichterstellung.** Es wurde ein Problem behoben, bei dem MVT-Aktivitäten in der [!UICONTROL -Benutzeroberfläche &#x200B;]Standortbeitrag) und Diagrammberichte generieren konnten und der Fehler „Irgendetwas ist schiefgelaufen“ angezeigt wurde. Wir können Ihre Anfrage nicht bearbeiten.“ Berichte werden nun korrekt in der Benutzeroberfläche geladen, wodurch eine vollständige Sichtbarkeit gewährleistet ist. (TGT-53654)
* **MVT-Berichte werden aufgrund eines Fehlers im Beitragsbericht [!UICONTROL Element] nicht geladen.** Es wurde ein Problem behoben, bei dem MVT-Aktivitätsberichte nicht in der Target-Benutzeroberfläche geladen werden konnten und der Fehler „Bericht zum Elementbeitrag konnte nicht abgerufen werden“ angezeigt wurde. Berichte werden jetzt korrekt angezeigt, sodass die Elementbeiträge vollständig sichtbar sind. (TGT-53691)
* **Exportieren von Auftragsdetails in CSV-Anfrage für [!UICONTROL Experience Targeting] (XT)-Aktivitäten.** Fehlerkorrektur - Die Option [!UICONTROL Auftragsdetails in CSV exportieren] wird jetzt für XT-Aktivitäten korrekt angezeigt und als leere Datei zurückgegeben. Die Option wird jetzt nur noch für AP-Aktivitäten angezeigt, um eine genaue Exportfunktion sicherzustellen und Verwirrung zu vermeiden. (TGT-53798)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **[!UICONTROL Änderung löschen] Aufgrund eines Schaltflächenproblems konnten keine Aktivitätsänderungen entfernt werden.** Es wurde ein Problem behoben, bei dem die Schaltfläche [!UICONTROL Änderung löschen] in der [!DNL Target]-Benutzeroberfläche nicht funktionierte, sodass Benutzer keine Änderungen innerhalb von Aktivitäten entfernen konnten. Die Schaltfläche funktioniert jetzt erwartungsgemäß und ermöglicht das zuverlässige Löschen von Änderungen ohne Verzögerung. (TGT-53728)
* **Bevorzugte Selektoren werden in der aktualisierten Benutzeroberfläche nicht erkannt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem bevorzugte Selektoren wie `data-target-component-id` nicht in der CSS-Selektorliste im VEC angezeigt wurden. Benutzerinnen und Benutzer können jetzt zuverlässig bevorzugte Attribute anstelle von dynamisch generierten Klassennamen auswählen, was ein stabiles Targeting über SPA-Seitenaktualisierungen hinweg gewährleistet. (TGT-53908)
* **Die Ausrichtung des Aktivitätsstandorts zwischen den Seiten [!UICONTROL Bearbeiten] und [!UICONTROL Übersicht] stimmt nicht überein.** Es wurde ein Problem behoben, bei dem die Nummerierung des Aktivitätsspeicherorts auf der Seite [!UICONTROL Übersicht] nicht mit Aktualisierungen auf der Seite [!UICONTROL Erlebnis bearbeiten“ &#x200B;]. Die Positionen bleiben jetzt in beiden Ansichten konsistent, sodass eine genaue Ausrichtung gewährleistet ist und fehlende oder falsch nummerierte Positionen vermieden werden. (TGT-53960 und TGT-53954)
* **Wechseln zurück in den Modus [!UICONTROL Design] in aktualisiertem VEC nicht möglich.** Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem Benutzende nach dem Navigieren zu einer neuen Seite im Modus [!UICONTROL Durchsuchen] nicht in den Modus [!UICONTROL Design] wechseln konnten. Der [!UICONTROL Design]-Umschalter funktioniert jetzt ordnungsgemäß, sodass Änderungen nahtlos auf allen Seiten angewendet werden können. (TGT-53988 und TGT-53993)
* **Abfrageparameter wird in der Aktivitätsübersicht nicht angezeigt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Abfrageparameter auf der Seite [!UICONTROL Übersicht] für Aktivitäten nicht angezeigt wurden, was zu Diskrepanzen zwischen der [!UICONTROL Übersicht] und den Seitenbereitstellungs-URLs führte. Abfrageparameter werden jetzt korrekt angezeigt, sodass Aktivitätspositionen in allen Ansichten vollständig dargestellt und konsistent sind. (TGT-53701)

+++

### [!DNL Target Standard/Premium] 25.10.1 (22. Oktober 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**Aktivitäten**

+++ Details anzeigen
* **Es wurde ein Problem mit der Benutzerfreundlichkeit in der aktualisierten Benutzeroberfläche**. [!UICONTROL Beobachter] können Aktivitäten jetzt mit der Option [!UICONTROL Aktivität anzeigen] in der Vorschau anzeigen, genau wie in der alten Benutzeroberfläche. (TGT-51741)
* **[!UICONTROL Beobachter]-Benutzer können jetzt Aktivitätsinhalte in der aktualisierten Benutzeroberfläche anzeigen.** Sichtbarkeit für Benutzer mit Beobachterrolle in der aktualisierten Aktivitäts-Benutzeroberfläche wiederhergestellt. Zuvor konnten Beobachter keine Änderungen, Angebote und Inhaltsänderungen anzeigen - Funktionen, die in der alten Benutzeroberfläche verfügbar waren. (TGT-53785)
* **[!UICONTROL Genehmigende Person] Benutzende können jetzt Aktivitätsziele bearbeiten, ohne dass ein Fehler mit Editor-Berechtigung auftritt.** Es wurde ein Berechtigungsproblem in der Benutzeroberfläche „Aktivitätserstellung“ behoben, das Benutzende auf Genehmigerebene daran hinderte, Änderungen an erweiterten Zieleinstellungen zu speichern. Betroffene Benutzende erhielten einen `403 Forbidden.Resource` Fehler, der Editor-Berechtigungen erforderlich machte, obwohl sie über ausreichende Zugriffsrechte verfügten. (TGT-53819)

+++

**Zielgruppen**

+++Details anzeigen

* **Auswahl mehrerer Zielgruppen im Reporting „Nur diese Aktivität“ wiederhergestellt.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer mehrere Zielgruppen unter dem Abschnitt [!UICONTROL Nur diese Aktivität] in [!UICONTROL Ziele und Einstellungen] auswählen konnten. (TGT-53283)
* **Zielgruppenbasierte Berichtsdiagramme zeigen jetzt die Konversionsdaten korrekt an.** Es wurde ein Problem auf der Registerkarte [!UICONTROL Berichte] behoben, das dazu führte, dass Diagramme bei der Auswahl von nicht standardmäßigen Zielgruppen fehlschlugen. Obwohl Daten- und Konfidenzmetriken verfügbar waren, zeigte das visuelle Diagramm nur eine durchgezogene Linie, was die Analyse schwierig machte. (TGT-53769)
* **Die Benutzeroberfläche [!UICONTROL Targeting] zeigt jetzt eindeutig ausgeschlossene Zielgruppenregeln an.** Es wurde ein Problem im Abschnitt [!UICONTROL Targeting] der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, bei dem die auf [!UICONTROL Ausschließen] gesetzten Zielgruppenregeln nicht deutlich angezeigt wurden. Dies führte zu Verwirrung bei der Überprüfung der Zielgruppenbestimmungslogik, insbesondere für Zielgruppen, die bestimmte URLs ausschließen. (TGT-53809)
* **Zielgruppendefinitionswerte können jetzt auf der Registerkarte [!UICONTROL Targeting] ausgewählt und kopiert werden.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer Zielgruppenregelwerte auf der Registerkarte [!UICONTROL Targeting] auswählen und kopieren konnten. Diese Funktion war in der veralteten Benutzeroberfläche verfügbar, fehlt jedoch in der aktualisierten Benutzeroberfläche. (TGT-53856)

+++

**Lokalisierung**

+++Details anzeigen

* **Fehlerhafte Übersetzung von „quote“ im zh_CN-Seiteneditor.** Korrektur eines kontextuellen Übersetzungsfehlers im Gebietsschema zh_CN, bei dem der Begriff „Angebot“ fälschlicherweise als &quot;&quot; übersetzt wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich die beabsichtigte Bedeutung auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53841)
* **Falsche Übersetzung von „Zitat entfernt“ im zh_CN Seiteneditor Kontext korrigiert.** Korrektur eines Übersetzungsfehlers im Gebietsschema zh_CN, bei dem „entferntes Angebot“ fälschlicherweise als &quot;&quot; gerendert wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich der Begriff auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53843)
* **Fehlerkorrektur - Übersetzung von „Zitat neu angeordnet“ im zh_CN-Seiteneditor-Kontext.** Korrektur eines kontextuellen Übersetzungsfehlers im zh_CN-Gebietsschema, bei dem „Angebot neu angeordnet“ fälschlicherweise als &quot;&quot; übersetzt wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich der Begriff auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53844)
* **Falsche Übersetzung von „Zitat geändert“ im zh_CN Seiteneditor Kontext korrigiert.** Korrektur eines Übersetzungsfehlers im Gebietsschema zh_CN, bei dem „Angebot geändert“ fälschlicherweise als &quot;&quot; gerendert wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich der Begriff auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53845)

+++

**Recommendations**

+++Details anzeigen

* **Änderungen an der CSS-Auswahl für Recommendations werden jetzt korrekt gespeichert.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer den CSS-Selektor für Recommendations-Platzierungen aktualisieren konnten. Änderungen wurden nach dem Speichern rückgängig gemacht, Aktualisierungen der Zielgruppen-Container wurden blockiert. (TGT-53835)
* **Die Auswahl des Seitenladeereignisses bleibt jetzt in den Empfehlungsänderungen erhalten.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer Änderungen speichern konnten, wenn der Ereignistyp einer Empfehlung von [!UICONTROL Ansicht] in [!UICONTROL Seitenladen] gewechselt wurde. Obwohl die Auswahl erfolgreich erschien, kehrte sie nach der Abfahrt zurück und blockierte die Veröffentlichung der Aktivität. (TGT-53957)

+++

**Berichte**

+++Details anzeigen

* **&quot;[!UICONTROL Auftragsdetails in CSV exportieren] lädt jetzt vollständige Daten herunter.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche [!UICONTROL Übersicht] behoben, das dazu führte, dass die Option [!UICONTROL Auftragsdetails in CSV exportieren] leere Dateien herunterlädt, selbst wenn gültige Berichtsdaten vorhanden waren. (TGT-53787)

+++

**Sicherheit**

+++Details anzeigen

* **IMS-Vorfilter wurde hinzugefügt, um GQL-Endpunkte vor organisationsübergreifender Datengefährdung zu schützen.** Es wurde eine Sicherheitslücke auf der Registerkarte Admin behoben, die sich auf die Endpunkte LicenseGroups und targetProperties GraphQL auswirkte. Das Problem entstand durch die Verwendung der JIL-API mit einem Admin-Client-Token, das für den Zugriff auf unternehmensübergreifende Produktdaten ausgenutzt werden könnte. (TGT-53837)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen

* **Die Autorenstabilität wurde in der Benutzeroberfläche „Aktivität erstellen“ wiederhergestellt.** Es wurde ein zeitweiliges Problem in der VEC-Benutzeroberfläche behoben, das dazu führte, dass das Authoring fehlschlug und Links unerwartet anklickbar wurden, sodass die Benutzer von der Seite weggeleitet wurden. (TGT-53153)
* **Bearbeitung für gespeicherte Aktivitäten in der Benutzeroberfläche „Aktivitätserstellung“ wurde wiederhergestellt.** Es wurde ein Problem behoben, durch das Benutzer nach dem Speichern von Änderungen keine Aktivitäten bearbeiten konnten. Betroffene Aktivitäten blieben in &quot;[!UICONTROL Anwenden erster Änderungen] stecken, blockierten weitere Updates und blendeten die Schaltfläche [!UICONTROL Abbrechen] aus. (TGT-53631)
* **Der VEC wartet nicht mehr mit &quot;[!UICONTROL Anwenden erster Änderungen] auf** Es wurde ein Leistungsproblem in VEC behoben, das zu langen Verzögerungen beim Laden von Erlebnissen mit einer hohen Anzahl von Änderungen führte. Betroffene Benutzende sahen die Benutzeroberfläche mehrere Minuten lang [!UICONTROL &#x200B; „Anwenden erster &#x200B;]&quot; hängen, insbesondere in Szenarien mit Experience B. (TGT-53727)
* **Der VEC lädt jetzt Änderungen ohne Stammelemente.**
Es wurde ein Problem in VEC behoben, das dazu führte, dass Erlebnisse beim Laden von Änderungen blockiert wurden, denen ein klares Stammelement fehlte. Diese Änderungen haben zuvor dazu geführt, dass die Benutzeroberfläche unbegrenzt an „Anwenden [!UICONTROL &#x200B; ersten Änderungen“ &#x200B;]. (TGT-53799)
* **Änderungen in Aktivitäten werden jetzt erwartungsgemäß gespeichert.** Es wurde ein berechtigungsbezogenes Problem in der neuen Benutzeroberfläche „Erstellen“ behoben, das verhinderte, dass Benutzer Änderungen speichern konnten, wenn sie Ziele und erweiterte Einstellungen in Aktivitäten bearbeiteten. Betroffene Benutzende sahen ein rotes Fehlerband und die Meldung „Forbidden.Resource“, obwohl sie angemessenen Zugriff hatten. (TGT-53816)
* **Die VEC-Benutzeroberfläche behält jetzt die Erlebnisänderungen über Ansichten hinweg bei.** Es wurden mehrere Probleme in der aktualisierten VEC behoben, die sich auf die Erlebnisentwicklung auswirkten. Die Änderungen wurden nicht korrekt beibehalten, insbesondere wenn HTML-Angebote verwendet oder zwischen Ansichten gewechselt wurde. (TGT-53825)
* **Alle Ansichten werden jetzt korrekt angezeigt, wenn eine Änderung mehrere Erlebnisse umfasst.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, bei dem nur eine Ansicht angezeigt wurde, wenn eine Änderung auf mehrere Ansichten angewendet wurde. In der Tooltip von „Mauszeiger bewegen“ konnten nicht alle zugehörigen Ansichten aufgelistet werden, obwohl die Änderung korrekt angewendet wurde. (TGT-53827)
* **Der VEC wartet nicht mehr zeitweise mit &quot;[!UICONTROL Anwenden erster Änderungen] auf** Es wurde ein zeitweiliges Problem in VEC behoben, bei dem Erlebnisse nicht geladen werden konnten und bei &quot;[!UICONTROL Anwenden erster Änderungen“ &#x200B;]. Dieses Verhalten war inkonsistent und löste manchmal Umleitungsschleifen aus oder erforderte eine manuelle Cache-Leerung. (TGT-53916)
* **VEC-Ladeproblem konnte nicht reproduziert werden.** Wir haben ein gemeldetes Problem untersucht, bei dem der VEC beim Bearbeiten vorhandener Aktivitäten [!UICONTROL &#x200B; „Anwenden &#x200B;] Änderungen“ feststeckte. Es wurde vermutet, dass das Verhalten mit HTML-Inhalten zusammenhängt, denen ein übergeordnetes Element fehlt. Wir setzen die Überwachung auf Wiederholungen fort und empfehlen die Verwendung strukturierter Container für HTML-Angebote, um die Stabilität sicherzustellen. (TGT-53972)
* **[!UICONTROL Design]-Modus in VEC verhält sich nicht mehr wie [!UICONTROL Durchsuchen]-Modus mit Unterbrechungen.** Es wurde ein Problem in der Benutzeroberfläche behoben, bei dem [!UICONTROL Design]-Modus sich zeitweise wie [!UICONTROL Durchsuchen] verhielt, klickbare `<a>`-Links ermöglichte und die Elementauswahl verhinderte. Dies führte dazu, dass das Hover-Feld ausgeblendet wurde und die Änderungs-Workflows blockiert wurden. (TGT-53136)
* **Klicks auf die Schaltfläche im [!UICONTROL Composer]-Modus führen nicht mehr zu einer Trigger-Seitenumleitung.** Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem das Klicken auf eine Schaltfläche [!UICONTROL Composer]-Modus zu einer unerwarteten Umleitung zur Ziel-URL der Schaltfläche führte. Dies hinderte Benutzende daran, call-to-action (CTA)-Elemente zu bearbeiten, und störte den Authoring-Workflow. (TGT-53137)
* **Aktualisierungen des Angebotscodes in Aktivitäten von Automated Personalization werden jetzt ohne Fehler gespeichert.** Es wurde ein Problem in der Benutzeroberfläche „Neu erstellen“ behoben, das den Fehler &quot;[!UICONTROL Ungültige Benutzereingabe] beim Aktualisieren des Angebotscodes in [!UICONTROL Automated Personalization]-Aktivitäten verursachte. Der Fehler hinderte Benutzer daran, Änderungen zu speichern, selbst wenn die Eingabe gültig war. (TGT-53586)
* **[!UICONTROL Design]-Modus in VEC blockiert jetzt die Link-Navigation für bearbeitbare Komponenten.** Es wurde ein Problem im aktualisierten VEC behoben, bei dem durch anklickbare Elemente (z. B. Schaltflächen und Links) eine Seitenumleitung ausgelöst wurde, selbst wenn sich der [!UICONTROL Design]-Modus befand. Dieses Verhalten hat den [!UICONTROL Durchsuchen]-Modus imitiert und Benutzende daran gehindert, Schlüsselkomponenten zu ändern. (TGT-53696)
* **Metrik [!UICONTROL Auf ein Element geklickt] funktioniert jetzt ohne Umleitung oder Fehler.** Es wurde ein Problem in der Benutzeroberfläche „Neu erstellen“ behoben, das bei Auswahl der Konversionsmetrik &quot;[!UICONTROL &#x200B; auf ein Element geklickt“ zu unerwarteten Weiterleitungen &#x200B;] leeren Bildschirmen führte. Durch Klicken auf eine Schaltfläche während des Setups wurde die Navigation ausgelöst, anstatt das Element zu registrieren, was zu einem Fehler [!UICONTROL Element nicht gefunden] führte. (TGT-53817)
* **Vorhandene Aktivitäten bleiben während der Bearbeitung nicht mehr in der unendlichen Ladeschleife stecken.** Es wurde ein Problem in der Benutzeroberfläche „Neu erstellen“ behoben, bei dem durch die Bearbeitung einer vorhandenen Aktivität in Visual Experience Composer die Seite in einer unendlichen Ladeschleife stecken blieb. Dieses Problem hatte keine Auswirkungen auf neu erstellte Aktivitäten und wurde durch bereits vorhandene Änderungen auf der Seite ausgelöst. (TGT-53913)
* **Vorhandene Aktivitätsseiten mit Änderungen werden jetzt im VEC korrekt geladen.** Es wurde ein Problem im aktualisierten VEC behoben, durch das Seiten in der Ladephase beim Bearbeiten einer vorhandenen Aktivität mit gespeicherten Änderungen hängen blieben. Neue Aktivitäten ohne Problem geladen, aber zuvor konfigurierte Aktivitäten konnten nicht gerendert werden. (TGT-53967)

+++

### [!DNL Target Standard/Premium] 25.9.3 (30. September 2025)

Diese Version enthält die folgenden Verbesserungen und Fehlerbehebungen.

+++[!UICONTROL Zielgruppen]

* **Regeln zum Zielgruppenausschluss wurden fälschlicherweise als Aufnahme in der [!DNL Target]-Benutzeroberfläche angezeigt.** Audiences, die mit Ausschlussregeln konfiguriert wurden, wurden beim Bearbeiten der Zielgruppenbestimmung in einer Aktivität als einbezogen angezeigt. Obwohl die Ausschlusslogik während der Ausführung korrekt angewendet wurde, konnte die Regel in der Benutzeroberfläche nicht genau wiedergegeben werden, da die Kennzeichnung „Ausschließen“ weggelassen wurde. Die [!DNL Target]-Benutzeroberfläche zeigt jetzt die Ausschlussregeln sowohl in der Zielgruppen-Konfiguration als auch in den Zielgruppen-Workflows korrekt an, wodurch Klarheit und Konsistenz für die Kampagneneinrichtung gewährleistet sind. (TGT-53808)
* **Im Abschnitt [!UICONTROL Targeting] wurde nicht angegeben, dass eine Zielgruppenregel auf „Ausschließen“ festgelegt wurde.** Audiences, die mit einer Ausschlusslogik konfiguriert wurden, wurden fälschlicherweise als Aufnahme im Abschnitt [!UICONTROL Targeting] der Benutzeroberfläche zur Erstellung von Aktivitäten angezeigt. Obwohl das Backend die Ausschlussregel korrekt angewendet hat, konnte sie von der Benutzeroberfläche nicht visuell dargestellt werden, wodurch die Kennzeichnung „Ausschließen“ weggelassen wurde, was während der Kampagneneinrichtung zu Verwirrung führte. Im Abschnitt [!UICONTROL Targeting] werden jetzt die Ausschlussregeln angezeigt, was die Konsistenz zwischen der Zielgruppenkonfiguration und der Zielgruppenvisualisierung gewährleistet. (TGT-53809)

+++

+++Lokalisierung

* **Es wurde eine Terminologieinkonsistenz bei der Übersetzung von „Vollständige Detailansicht“ ins vereinfachte Chinesisch behoben.**
Zuvor wurde der Begriff „Details“ im vereinfachten Chinesisch (zh_CN) fälschlicherweise als &quot;&quot; übersetzt, was gegen etablierte Terminologieleitlinien verstößt. Dies wurde in &quot;&quot; geändert, um die Konsistenz mit der Terminologiedatenbank sicherzustellen. (TGT-53741)

+++

+++[!UICONTROL Recommendations]

* **Empfehlungsfelder waren im VEC schwer zu finden und auszuwählen.** Nachdem Sie ein Recommendations-Angebot in (VEC) hinzugefügt haben, wurde beim Klicken auf die Änderung im linken Bedienfeld das entsprechende Recommendations-Feld auf der Seite nicht markiert bzw. ein Bildlauf dorthin durchgeführt. Dies machte es schwierig, das Angebot zu finden und zu bearbeiten, insbesondere wenn es unter Selektoren ausgeblendet oder minimal formatiert war. Wenn Sie auf eine Empfehlungsänderung klicken, wird das zugehörige Element jetzt korrekt hervorgehoben und ein Bildlauf durchgeführt, was die Benutzerfreundlichkeit verbessert und die Bearbeitungseffizienz im aktualisierten Prozess zur Erstellung von Aktivitäten verbessert. (TGT-52571)
* **Empfehlungsselektoren wurden nach dem Speichern einer Aktivität falsch neu geschrieben.** Beim Hinzufügen einer Empfehlung zu einem Element in Visual Experience Composer war der Selektor zunächst korrekt, wurde aber nach dem Speichern und erneuten Öffnen der Aktivität in einen generischen Selektor geändert. Der Versuch, die ursprüngliche Auswahl manuell wiederherzustellen, führte zu Validierungsfehlern. Empfehlungsselektoren bleiben jetzt nach dem Speichern korrekt erhalten, was eine zuverlässige Zielgruppenbestimmung und Bearbeitbarkeit im aktualisierten Prozess der Aktivitätserstellung gewährleistet. (TGT-53709)
* **Kriterieninhalt konnte beim Ändern einer vorhandenen Aktivität nicht bearbeitet werden.** Beim Bearbeiten einer Aktivität [!UICONTROL &#x200B; der Inhaltsabschnitt &#x200B;]Kriterien“ deaktiviert, wobei die Schaltflächen ausgegraut waren und nicht reagierten. Dieses Problem wurde behoben, indem sichergestellt wurde[!UICONTROL &#x200B; dass &#x200B;]Kriterienkonfigurationen“ bei Aktivitätsaktualisierungen vollständig bearbeitbar sind. Kunden können jetzt Inhalte [!UICONTROL Kriterien] ändern, ohne die Auswahl wechseln oder Problemumgehungen verwenden zu müssen, was die Flexibilität und Benutzerfreundlichkeit im aktualisierten Prozess der Aktivitätserstellung verbessert. (TGT-53812)
* **Kriterien konnten innerhalb einer Aktivität nicht bearbeitet werden.** Die Optionen [!UICONTROL Kriterien bearbeiten] und [!UICONTROL Kriterien entfernen] wurden beim Zugriff auf Kriterien in einer Aktivität deaktiviert. Dieselben Kriterien können jedoch erfolgreich über die Registerkarte [!UICONTROL Recommendations] bearbeitet werden. Die Kriterien können jetzt sowohl über den Workflow für die Bearbeitung der Aktivität als auch über die Registerkarte [!UICONTROL Recommendations] vollständig bearbeitet werden, was ein konsistentes und effizientes Bearbeitungserlebnis gewährleistet. (TGT-53814)

+++

+++[!UICONTROL Berichte]

* **Das Generieren von Ad-hoc-Angeboten in A[!UICONTROL Automated Personalization]-Aktivitäten führte zu Inkonsistenzen bei der Berichterstellung.** Die Verwendung der Funktion zum Generieren von Ad-hoc-Angeboten in [!UICONTROL Automated Personalization] (AP)-Aktivitäten führte zu ungenauen Berichten. Insbesondere wurden Angebots-IDs standortübergreifend wiederverwendet, was dazu führte, dass Berichtsdaten falsch zugeordnet oder überschrieben wurden. Ad-hoc-Angebote werden jetzt mit separaten Kennungen pro Standort generiert, um eine genaue Verfolgung und Berichterstellung für alle konfigurierten Erlebnisse sicherzustellen. (TGT-53757)
* **Aktivitätsberichte konnten aufgrund eines JavaScript-Fehlers nicht geladen werden.** Beim Zugriff auf die Registerkarte „Berichte“ für bestimmte Aktivitäten [!UICONTROL &#x200B; Kunden &#x200B;] die Meldung „Irgendetwas ist schiefgelaufen“. Der Fehler wurde durch einen JavaScript-Ausnahmefehler verursacht: Eigenschaften von nicht definierten Inhalten können nicht gelesen werden (Lesen von „indexOf„), ausgelöst während des `getAnalyticsReportSummary` GraphQL-Aufrufs. Berichte werden jetzt korrekt geladen und die Fehlerbehandlung wurde verbessert, um ähnliche Fehler im aktualisierten Workflow für die Erstellung von Aktivitäten zu verhindern. (TGT-53797)
* **Berichte stürzten nach der Interaktion mit der Bildlaufleiste ab.** Durch Klicken auf die Bildlaufleiste auf der [!UICONTROL Berichte] stürzt die Seite ab, begleitet von einem JavaScript-Fehler:
  `SyntaxError: Failed to execute 'querySelector' on 'Element': '[data-key="a-currentcopy"hiretalent""]' is not a valid selector.` Berichte werden jetzt korrekt geladen und gescrollt, ohne dass Fehler oder Abstürze ausgelöst werden. (TGT-53828)
* **In eReports wurde die primäre Metrik nicht angezeigt.** Die primäre Metrik, die als Konversionsmetrik mithilfe einer Mbox konfiguriert wurde, fehlte in den Aktivitätsberichten. Die Suche nach Metriknamen oder Mbox-Namen führte zu keinen Ergebnissen und verhinderte die Sichtbarkeit wichtiger Leistungsdaten. Primäre Metriken werden jetzt korrekt auf der Registerkarte [!UICONTROL Berichte] angezeigt, was eine genaue Verfolgung und Analyse der Kampagnenleistung gewährleistet. (TGT-53773)
* **Die Registerkarte [!UICONTROL Berichte] in der aktualisierten Benutzeroberfläche stürzte bei der Interaktion mit der horizontalen Bildlaufleiste ab.** Die [!UICONTROL Berichte]-Ansicht stürzte zeitweise mit dem Fehler „Irgendetwas ist schiefgelaufen“ ab, wenn die horizontale Bildlaufleiste verwendet wurde, um auf Metriken außerhalb der Ansicht zuzugreifen. Die Bildlaufleiste funktioniert jetzt zuverlässig, sodass Kundinnen und Kunden alle Metriken anzeigen und analysieren können, ohne dass sie Problemumgehungen wie das Verkleinern oder Verwenden von Umschalt-Bildlauf benötigen. (TGT-53824)

+++

+++[!UICONTROL Visual Experience Composer] (VEC)

* **Durch Klicken auf Breadcrumbs in VEC wurde das Bearbeitungsmenü nicht konsistent angezeigt.**
Bei der Auswahl von HTML-Elementen über die Breadcrumbs in (VEC) wird das Bearbeitungsmenü gelegentlich nicht angezeigt oder verschwindet schnell, was die Elementauswahl unzuverlässig macht. Das Bearbeitungsmenü wird jetzt beim Navigieren über Breadcrumbs durchgängig angezeigt, was den Workflow zur Elementauswahl im aktualisierten Prozess zur Erstellung von Aktivitäten verbessert. (TGT-52873)
* **Das Kontextmenü wird in VEC zeitweise nicht angezeigt.** Das Kontextmenü in der aktualisierten VEC-Benutzeroberfläche wurde beim Klicken auf Elemente nicht konsequent angezeigt, sodass der Zugriff auf Bearbeitungsoptionen erschwert wurde. Das Kontextmenü wird jetzt zuverlässig bei der Elementauswahl angezeigt, was den Bearbeitungs-Workflow und die allgemeine Benutzerfreundlichkeit im aktualisierten Prozess der Aktivitätserstellung verbessert. (TGT-53015)
* **Das Kontextmenü wurde für bestimmte Elemente im VEC nicht angezeigt.** Das Kontextmenü wurde nicht angezeigt, wenn bestimmte Elemente in dem aktualisierten VEC ausgewählt wurden, sodass Änderungen nur schwer angewendet werden konnten. Das Kontextmenü wird nun für alle unterstützten Elemente angezeigt, was die Zuverlässigkeit und Benutzerfreundlichkeit der Bearbeitung im aktualisierten Workflow für die Erstellung von Aktivitäten verbessert. (TGT-53248)
* **Kontextmenü bei Verwendung von Breadcrumbs in VEC verschwand beim ersten Klick.** Wenn Sie ein übergeordnetes Element über die Breadcrumbs in VEC auswählen, wird das Kontextmenü kurz angezeigt und dann ausgeblendet, sodass die Bearbeitungsoptionen nur schwer zugänglich sind. Das Kontextmenü bleibt jetzt beim Navigieren durch Breadcrumbs für Elemente sichtbar und funktioniert. Dies verbessert die Zuverlässigkeit des Workflows zur Elementauswahl im aktualisierten Prozess zur Erstellung von Aktivitäten. (TGT-53424)
* **Das Kontextmenü wurde für Elemente der obersten Ebene in Visual Experience Composer nicht angezeigt.** Bei der Auswahl von Elementen der obersten Ebene - z. B. `<div>` oder `<main>`-Tags - über die Breadcrumbs im VEC trat kein Trigger im Kontextmenü auf, was weitere Bearbeitungsaktionen verhinderte. Das Kontextmenü wird jetzt durchgängig für alle unterstützten Elemente angezeigt, einschließlich Container der obersten Ebene, was die Flexibilität und Benutzerfreundlichkeit des Arbeitsablaufs für die Erstellung von Aktivitäten verbessert. (TGT-53770)
* **Elemente auf einer bestimmten Seite konnten im VEC nicht bearbeitet werden.** Bestimmte Elemente auf der Seite konnten in dem aktualisierten VEC nicht ausgewählt oder bearbeitet werden. Dieses Problem wurde auf diese Seite isoliert und wirkte sich nicht auf andere Seiten innerhalb desselben Kontos aus. Alle Elemente auf der Seite können nun wie erwartet ausgewählt und bearbeitet werden, wodurch der Workflow zur Erstellung der Aktivität wieder voll funktionsfähig ist. (TGT-53353)
* **Der Arbeitsablauf beim Anzeigen von untergeordneten Elementen während der Elementauswahl im VEC wurde verbessert.** Um die Benutzerfreundlichkeit und Genauigkeit während der Aktivitätserstellung zu verbessern, zeigt der VEC jetzt untergeordnete Elemente an, wenn Sie den Mauszeiger über ein übergeordnetes HTML-Element bewegen oder es auswählen. Diese Verbesserung ermöglicht es Kunden, die Struktur der Seite besser zu verstehen und genauere Änderungen vorzunehmen, wodurch der Bearbeitungs-Workflow in der aktualisierten Benutzeroberfläche optimiert wird. (TGT-53416)
* **Elemente in vorhandenen Aktivitäten konnten nicht über die Änderungsleiste bearbeitet werden.** Beim Bearbeiten zuvor erstellter Aktivitäten konnte die Änderungsleiste für bestimmte Elemente auf der Seite nicht aktiviert werden, wodurch Aktualisierungen verhindert wurden. Dieses Problem trat hauptsächlich bei modifizierten Aktivitäten auf und war bei neu erstellten Aktivitäten schwer zu reproduzieren. Die Änderungsleiste wird jetzt konsistent angezeigt und ermöglicht die Bearbeitung aller unterstützten Elemente, was die Zuverlässigkeit und Benutzerfreundlichkeit im aktualisierten Workflow für die Erstellung von Aktivitäten verbessert. (TGT-53013)

+++

+++[!UICONTROL Arbeitsbereiche]

* **Beim Klonen einer Aktivität in einen anderen Arbeitsbereich wurde der Fehler „Ungültige Benutzereingabe“ ausgelöst.** Der Versuch, eine Aktivität von einem Arbeitsbereich in einen anderen zu klonen, führte zu einem Fehler: „InvalidProperty.json - Nicht erkannter Eigenschaftsname &#39;content&#39;.“ Dieses Problem wurde durch eine fehlerhafte Verarbeitung von Aktivitätsmetadaten während des Klonvorgangs verursacht. Aktivitäten können jetzt erfolgreich über Arbeitsbereiche hinweg geklont werden, ohne Validierungsfehler auszulösen, wodurch reibungslosere Workflow für die Bereitstellung von Aktivitäten gewährleistet sind. (TGT-53731 und TGT-53736)

+++

### [!DNL Target Standard/Premium] 25.9.2 (22. September 2025)

Dieses Release enthält die folgenden Fehlerbehebungen und Erweiterungen:

**[!UICONTROL Zielgruppen]**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem Aktivitäten aufgrund ungültiger Zielgruppen-IDs nicht kopiert werden konnten.** Kunden, die versuchten, Aktivitäten im aktualisierten Prozess der Aktivitätserstellung zu kopieren, stießen auf einen Fehler, der durch ungültige Zielgruppen-IDs verursacht wurde (z. B. -1752722444307). Dieses Backend-Validierungsproblem verhinderte die Duplizierung von Aktivitäten innerhalb desselben Arbeitsbereichs. Dieses Problem wurde behoben, und Aktivitäten können jetzt erfolgreich kopiert werden, ohne dass zielgruppenbezogene Fehler auftreten. (TGT-53717)
* **Es wurde ein Problem behoben, bei dem in den [!UICONTROL Automated Personalization-Aktivitäten im Modal „Inhalt verwalten] Fehler bei der Benutzereingabe für [!UICONTROL &#x200B; Zielgruppen &#x200B;] Aktivität auftraten.** Kunden stoßen bei der Konfiguration von Zielgruppen, die nur Aktivitäten vorbehalten sind, im Modal [!UICONTROL Inhalt verwalten] für AP-Aktivitäten auf Fehler bei ungültigen Benutzereingaben. Dieses Problem trat auf, obwohl die Zielgruppen zuvor erfolgreich verwendet wurden. Kombinierte Zielgruppenkonfigurationen werden jetzt korrekt gespeichert, ohne dass Validierungsfehler ausgelöst werden. (TGT-53749)

+++

**Dokumentation**

+++Details anzeigen

* **Target-spezifische Web SDK-Dokumentationsseiten wurden in das Adobe Target-Repository verschoben.** Im Rahmen der Neustrukturierung der Web SDK-Dokumentation wurden [!DNL Target] Inhalte von den allgemeinen Web SDK-Dokumenten in das [!DNL Adobe Target]Entwicklerhandbuch[&#x200B; migriert](https://experienceleague.adobe.com/de/docs/target-dev/developer/a4t/overview-a4t?lang=en){target=_blank}. Diese Änderung verbessert die Auffindbarkeit von Inhalten und stellt sicher, dass die lösungsspezifische Anleitung vom entsprechenden Produkt-Team gepflegt wird. (TGT-53374)

+++

**[!UICONTROL Angebotsentscheidungen]**

+++Details anzeigen

* **Die Option Angebotsentscheidung ist jetzt bei der Erstellung der ersten Aktivität durchgängig sichtbar.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die Option [!UICONTROL Angebotsentscheidung] beim erstmaligen Erstellungsfluss für A/B-Aktivitäten nicht angezeigt wurde, insbesondere beim Zugriff im Inkognito-Modus für Mandanten mit aktivierten Angebotsentscheidungen. Die Option wurde erst nach dem Navigieren zum Schritt [!UICONTROL Targeting] und zurück zu &quot;[!UICONTROL &quot; &#x200B;]. Durch diese Fehlerbehebung wird sichergestellt, dass die Option [!UICONTROL Angebotsentscheidung] bei der Ersteinrichtung sofort verfügbar ist, was die Benutzerfreundlichkeit verbessert und Verwirrung verringert. (TGT-51888)

+++

**[!UICONTROL Angebote]**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem Umleitungsangebote beim `includeContent=true` keine `redirectOptions` in die Payload enthielten.** Kunden, die Umleitungsangebote mit abrufen`includeContent=true ` fehlt in der Antwort-Payload das Feld `redirectOptions` . Diese Inkonsistenz wirkte sich auf Workflows aus, z. B. auf das Kopieren von Angeboten und die Erstellung von Aktivitäten. Umleitungsangebote enthalten jetzt bei Inhaltsanfragen korrekt `redirectOptions`. (TGT-53737)

+++

**[!DNL Recommendations]**

+++Details anzeigen

* **Klick-Tracking für [!UICONTROL Recommendations]-Aktivitäten wiederhergestellt, die in der aktualisierten Benutzeroberfläche erstellt wurden.** Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem in &#x200B;] aktualisierten Benutzeroberfläche erstellte Aktivitäten das Klick-Tracking nicht registrieren konnten, was zu null gemeldeten Konversionen führte. In der veralteten Benutzeroberfläche erstellte Aktivitäten verfolgten Klicks korrekt und meldeten Konversionen erwartungsgemäß. Diese Fehlerbehebung stellt sicher, dass die in der aktualisierten Benutzeroberfläche erstellten Recommendations-Aktivitäten jetzt die richtigen Tracking-Attribute enthalten und Konversionsberichte sowie die Ausrichtung an A4T-Metriken wiederhergestellt werden. (TGT-53287)
* **Klick-Tracking für Recommendations-Aktivitäten wiederhergestellt.** Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem in &#x200B;] aktualisierten Benutzeroberfläche erstellte Aktivitäten das Klick-Tracking nicht registrieren konnten, was zu null gemeldeten Konversionen führte. Die veraltete Benutzeroberfläche wendete eine Tracking-ID (`at-track-click`) korrekt auf [!UICONTROL Recommendations]-Inhalte an, während die aktualisierte Benutzeroberfläche fälschlicherweise einen Platzhalter (`__recsClickTrackIdPlaceholder__`) einfügte, was das Backend-Tracking verhinderte. Diese Fehlerbehebung stellt sicher, dass [!DNL Recommendations] Inhalt jetzt die richtige Tracking-ID enthält, sodass das Konversionsreporting wiederhergestellt und die Ausrichtung an A4T-Metriken wiederhergestellt werden kann. (TGT-53496)
* **Absturz des Sammlungs-Editors in aktualisierter Benutzeroberfläche behoben.** Fehlerkorrektur - In der aktualisierten Benutzeroberfläche von [!UICONTROL Visual Experience Composer] (VEC) stürzt die Seite beim Öffnen einer Sammlung im Editor-Bedienfeld jetzt mit dem Fehler TypeError ab: Eigenschaften von nicht definierten Inhalten können nicht gelesen werden (Lesen von „customLocale„). Dieser Fehler ist über mehrere Aktivitätstypen hinweg aufgetreten, einschließlich [!UICONTROL Recommendations] und A/B-Tests. (TGT-53703)
* **Option zum Entfernen der ausgewählten Sammlung, die im VEC wiederhergestellt wurde.** Es wurde ein Problem in VEC behoben, bei dem Benutzende nur eine ausgewählte Sammlung in einer [!UICONTROL Recommendations]-Aktivität ersetzen, sie jedoch nicht vollständig entfernen konnten. Diese Einschränkung blockierte Anwendungsfälle, die eine saubere Entfernung der Sammlung ohne Ersatz erfordern. Mit dieser Fehlerbehebung wird eine klare Option zum Entfernen der ausgewählten Sammlung eingeführt, was eine größere Flexibilität bei der Einrichtung von Aktivitäten und die Anpassung an das Verhalten der veralteten Benutzeroberfläche ermöglicht. (TGT-53652)
* **Benutzerdefinierte Kriteriensammlungen werden jetzt in der Benutzeroberfläche [!UICONTROL Recommendations] korrekt angezeigt.** Es wurde ein Problem in der Recommendations-Oberfläche behoben, bei dem mit benutzerdefinierten Kriterien erstellte Sammlungen keine Produktergebnisse anzeigen konnten. Während standardmäßige attributbasierte Sammlungen erwartungsgemäß funktionierten, gaben diejenigen, die benutzerdefinierte Filter verwendeten, trotz gültiger Katalogübereinstimmungen „Keine Ergebnisse gefunden“ zurück. Durch diese Fehlerbehebung wird sichergestellt, dass Sammlungen, die benutzerdefinierte Attribute verwenden, jetzt korrekt in der Registerkarte [!UICONTROL Produkt] aufgefüllt werden, sodass die volle Funktionalität für personalisierte Recommendations-Workflows wiederhergestellt wird. (TGT-53653)
* **Es wurde ein Problem behoben, bei dem Sammlungen beim ersten Öffnen der Seite [!UICONTROL Produkte] keine Produkte anzeigten.** Kunden, die auf Sammlungen im Abschnitt [!UICONTROL Recommendations] zugegriffen haben, haben beim ersten Öffnen der Seite [!UICONTROL Produkte] leere Produktergebnisse erhalten. Dieses Problem wurde durch einen Backend-Fehler in der GraphQL-Abfrage verursacht, der beim Laden von Produktdaten für Sammlungen mit benutzerdefinierten Kriterien fehlgeschlagen ist. Das Problem wurde behoben, und Produkte werden nun korrekt angezeigt, ohne dass die Umgebung gewechselt werden muss. (TGT-53694)
* **Es wurde ein Problem behoben, bei dem Sammlungen in formularbasierten [!UICONTROL Recommendations]-Aktivitäten nicht entfernt werden konnten.** Kunden, die [!UICONTROL Recommendations]-Aktivitäten mit dem [!UICONTROL formularbasierten Experience Composer] erstellen, konnten die Auswahl einer zuvor ausgewählten Sammlung nicht aufheben. Vor dem Speichern der Benutzeroberfläche muss eine Sammlung ausgewählt sein, damit Benutzer nicht zu „Alle Sammlungen“ zurückkehren können. Dieses Verhalten wurde aktualisiert, damit es der VEC-Funktionalität entspricht, sodass Kundinnen und Kunden ohne ausgewählte Sammlung speichern und standardmäßig wie erwartet „Alle Sammlungen“ verwenden können. (TGT-53708)
* **Es wurde ein Problem behoben, bei dem Promotions aufgrund fehlender Sammlungs- oder Filterregelwerte nicht nach Attribut festgelegt werden konnten.** Kunden, die Promotions nach Attribut im Prozess zur Erstellung einer Aktivität konfigurieren, haben einen Fehler festgestellt, der besagt, dass einer Promotion entweder eine Sammlungs-ID oder Filterregelwerte fehlten. Dieses Validierungsproblem blockierte den Fortschritt, selbst wenn die Einrichtung abgeschlossen zu sein schien. Promotions können jetzt erfolgreich gespeichert werden, wenn sie nach Attribut konfiguriert wurden. (TGT-53750)
* **Es wurde ein Problem behoben, bei dem Aktivitäten aufgrund doppelter Erlebnisnamen nicht gespeichert werden konnten.** Beim Speichern von Aktivitäten, die bestimmte Kriterienkombinationen und Designs enthielten, ist bei den Kunden ein Fehler wegen ungültiger Benutzereingabe aufgetreten. Der Fehler wurde durch doppelte Erlebnisnamen ausgelöst, selbst wenn das Setup gültig zu sein schien. Aktivitäten mit unterschiedlichen Konfigurationen können jetzt ohne Namenskonflikte gespeichert werden. (TGT-53805)
* **Es wurde ein Problem behoben, bei dem die Validierung für nach Attribut konfigurierte Promotions ungültig blieb.** Kunden stießen bei der Einrichtung von Promotions nach Attribut im Prozess der Aktivitätserstellung auf dauerhafte Validierungsfehler, selbst wenn alle erforderlichen Felder korrekt ausgefüllt waren. Dieses Problem wurde durch eine falsche Validierungslogik im Workflow [!UICONTROL Recommendations] verursacht. Attributbasierte Promotions werden jetzt wie erwartet validiert und gespeichert. (TGT-53811)
* **Es wurde ein Problem behoben, bei dem beim Anwenden einer Promotion auf eine Live [!UICONTROL Recommendations]-Aktivität ein Fehler aufgetreten ist.** Kunden erhielten den Fehler „Bei einer Promotion fehlen entweder eine Sammlungs-ID oder Filterregelwerte“, wenn sie versuchten, eine Frontend-Promotion auf eine Live-Aktivität vom Typ [!UICONTROL Recommendations] anzuwenden, selbst nachdem sie gültige Konfigurationsdetails angegeben hatten. Promotions können jetzt erfolgreich auf Live-Aktivitäten angewendet werden, ohne Validierungsfehler auszulösen, was ein reibungsloseres Erlebnis in der aktualisierten Benutzeroberfläche zur Erstellung von Aktivitäten gewährleistet. (TGT-53738)
* **Es wurde ein Problem behoben, bei dem Produkte in Sammlungen in der [!UICONTROL Recommendations]-Benutzeroberfläche nicht sichtbar waren.** Kunden eines einzelnen Mandanten berichteten, dass Produktlisten nicht geladen werden konnten, wenn bestimmte Sammlungen im Abschnitt [!UICONTROL Recommendations] der neuen Benutzeroberfläche angezeigt wurden. Das Problem wurde vorübergehend durch Wechseln der Umgebungen behoben, diese Problemumgehung führte jedoch zu einem schlechten Benutzererlebnis. Produktentitäten werden jetzt konsistent geladen, ohne dass die Umgebung umgeschaltet werden muss. (TGT-53783)
* **Es wurde ein Problem behoben, bei dem Kriterien und Designs nicht in einer Zeile der Benutzeroberfläche für die Erstellung von Aktivitäten angezeigt wurden.** Zuvor wurden Kriterien und Designs im Prozess zur Erstellung von Aktivitäten in einem komprimierten Format angezeigt, sodass es für Kunden schwierig ist, einzelne Elemente anzuzeigen und zu verwalten. Jedes Kriterium und Design wird jetzt in einer eigenen Zeile angezeigt, was die Lesbarkeit und Benutzerfreundlichkeit in der aktualisierten Benutzeroberfläche verbessert. (TGT-53818)

+++

**Berichte**

+++Details anzeigen

* **[!UICONTROL Gesamtumsatz]-Metrik ist jetzt in CSV-Exporten aus Aktivitätsberichten enthalten.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche [!UICONTROL Übersicht] behoben, bei dem der Gesamtumsatz in der Ansicht des Aktivitätsberichts korrekt angezeigt wurde, aber im CSV-Export fehlte und als 0 $ angezeigt wurde. Aufgrund dieser Diskrepanz konnten sich Benutzer für Offline-Analysen und -Berichte nicht auf exportierte Daten verlassen. (TGT-53325)
* **[!UICONTROL Gesamtumsatz]-Metrik ist jetzt in CSV-Exporten aus Aktivitätsberichten enthalten.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei [!UICONTROL &#x200B; die Metrik „Gesamtumsatz] in der Ansicht des Aktivitätsberichts korrekt angezeigt wurde, aber im CSV-Export fehlte. Aufgrund dieser Diskrepanz konnten Benutzer nicht auf vollständige Leistungsdaten in heruntergeladenen Berichten zugreifen. Diese Fehlerbehebung stellt sicher, dass [!UICONTROL Gesamtumsätze] jetzt korrekt in CSV-Exporten enthalten sind, wodurch die Konsistenz zwischen In-App-Reporting und Offline-Analyse wiederhergestellt wird. (TGT-53330)
* **Verbessertes Fehler-Messaging für [!UICONTROL Diagrammansicht] wenn Metriken nicht aktiviert sind.** Es wurde ein Problem in VEC behoben, bei dem in [!UICONTROL Diagrammansicht] eine allgemeine Fehlermeldung angezeigt wurde, wenn eine angeforderte Metrik in der zugehörigen [!DNL Analytics] Report Suite nicht aktiviert war. Dieses Problem wurde durch einen `not_enabled_metric` in der Backend-GraphQL-Antwort ausgelöst. Diese Fehlerbehebung ersetzt den vagen Fehler durch eine informativere Meldung, die Benutzern hilft, Konfigurationsprobleme in [!DNL Analytics] zu identifizieren, wodurch Verwirrung und unnötige Support-Eskalationen reduziert werden. (TGT-53577)
* **Es wurde ein Problem behoben, bei dem die Berichtsdauer das unterstützte Limit von 90 Tagen überschritt.** Kunden, die den Filter &quot;[!UICONTROL Letzte X Tage] im Abschnitt [!UICONTROL Berichte] verwenden, konnten eine Dauer von mehr als 90 Tagen auswählen, was zu Leistungsproblemen und unvollständigen Daten führen konnte. Der Filter wurde aktualisiert, um einen maximalen Zeitraum von 90 Tagen zu erzwingen und ein konsistentes und zuverlässiges Reporting zu gewährleisten. (TGT-53795)
* **Es wurde ein Problem behoben, bei dem Leistungs-CSV-Berichte unter Verwendung der Standardumgebung anstelle der ausgewählten Umgebung generiert wurden.** Zuvor, als Kundinnen und Kunden die Umgebung in den Berichtseinstellungen geändert und einen Leistungsbericht generiert haben, enthielt die resultierende CSV-Datei Daten aus der Standardumgebung und nicht aus der ausgewählten.  Die Benutzeroberfläche übergibt nun den `environmentId`-Parameter korrekt, sodass der Bericht die ausgewählte Umgebung widerspiegelt. Darüber hinaus wurde die Fehlerbehandlung verbessert. Wenn während der CSV-Generierung GraphQL-Fehler auftreten, zeigt die Benutzeroberfläche jetzt eine klare Fehlermeldung an, anstatt eine leere CSV-Datei zu erstellen. (TGT-53064)
* **Es wurde ein Problem behoben, bei dem die Berichterstellung von Analytics for Target (A4T) keine Daten in der [!UICONTROL Diagrammansicht“ &#x200B;].** Kunden und Kundinnen, die [!DNL Target] mit A4T-Integration verwenden, haben beim Wechsel zur Diagrammansicht auf der Registerkarte Reporting von A/B-Testaktivitäten den Fehler „Irgendetwas ist schiefgelaufen“ festgestellt. Obwohl die [!UICONTROL Tabellenansicht] korrekt geladen wurde, konnte [!UICONTROL Diagrammansicht] keine Metriktrends über den ausgewählten Zeitraum rendern. [!UICONTROL Diagrammansicht] zeigt jetzt für alle unterstützten Metriken die erwarteten Leistungsdaten an und verbessert so die Sichtbarkeit und Berichtsgenauigkeit in der aktualisierten Benutzeroberfläche. (TGT-53573)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen

* **Elementmetadaten sind jetzt beim Bewegen des Mauszeigers im Breadcrumb-Menü sichtbar.** Das Breadcrumb-Menü in VEC wurde verbessert, sodass zusätzliche Elementdetails wie ID, Klasse und Name angezeigt werden, wenn der Mauszeiger über ein Element bewegt wird. Diese Verbesserung hilft Benutzenden, Elemente während der Einrichtung von Aktivitäten leichter zu identifizieren und zu unterscheiden. (TGT-53409)
* **Der Breadcrumb-Mauszeiger hebt jetzt das entsprechende Element im VEC hervor.** Der [!UICONTROL Visual Experience Composer] wurde verbessert, um das entsprechende Element im Editor hervorzuheben, wenn der Mauszeiger über Elemente im Breadcrumb-Menü bewegt wird. Der Elementtyp wird ebenfalls angezeigt, z. B. Container, fett gedruckter Text oder Schaltfläche. Dieses Verhalten gilt für gleichrangige -Elemente und schließt nicht unterstützte Typen wie SVG basierend auf der Validierungsliste aus. (TGT-53411)
* **Warnhinweis zu nicht gespeicherten Änderungen wurde in VEC-Änderungs-Workflows wiederhergestellt.** Es wurde ein Problem in VEC behoben, bei dem Benutzende nicht mehr über nicht gespeicherte Änderungen in benutzerdefinierten Code-Änderungen benachrichtigt wurden. Im Gegensatz zur veralteten Benutzeroberfläche fehlten für das neue Erlebnis Eingabeaufforderungen beim Navigieren weg oder Schließen des Personalisierungseditors, was zu einem versehentlichen Verlust des Fortschritts führte. Mit dieser Fehlerbehebung werden Warnhinweise für alle Änderungstypen, einschließlich benutzerdefiniertem Code, wiederhergestellt und sichergestellt, dass Benutzende vor dem Beenden gewarnt werden, ohne zu speichern. (TGT-53435).
* **Änderungen am benutzerdefinierten Code bleiben jetzt während der Seitenaktualisierung im VEC erhalten.** Fehlerkorrektur - In VEC gehen Änderungen an benutzerdefiniertem Code bei Website-Aktualisierungen verloren. Dieses Problem trat auf Seiten mit mehreren Neuladungen auf, sodass der Editor nicht gespeicherte Änderungen zurücksetzen und rückgängig machen konnte. Durch die Korrektur wird sichergestellt, dass benutzerdefinierte Code-Bearbeitungen auch dann intakt bleiben, wenn die Seite während der Bearbeitung neu geladen wird, um einen versehentlichen Verlust des Fortschritts zu verhindern. (TTGT-53501)
* **Anmeldeproblem für Site-Zugriff innerhalb des VEC behoben.** Es wurde ein Problem behoben, bei dem sich Benutzer beim Zugriff über VEC nicht bei ihrer Website anmelden konnten. Der Anmeldefluss leitete Benutzer wiederholt zur Anmeldeseite zurück, wodurch die Einrichtung und Vorschau von Aktivitäten verhindert wurde. Diese Fehlerbehebung stellt sicher, dass der VEC nicht mehr in das Anmeldeverhalten eingreift und so den erwarteten Zugriff für authentifizierte Benutzer wiederherstellt. (TGT-53524)
* **Problem mit Cookie-Duplikaten in der VEC Helper-Erweiterung behoben.** Es wurde ein Problem behoben, bei dem die [!UICONTROL Adobe Experience Cloud Visual Editing Helper]-Erweiterung das `at_qa_mode`-Cookie während der Qualitätssicherung über Vorschau-Links duplizierte. Beim manuellen Wechsel zwischen Vorschauindizes wurden mehrere Cookies mit domänenübergreifenden Konflikten erstellt, sodass Tester keine Varianten zuverlässig wechseln konnten. Dieses Verhalten wurde sogar außerhalb der Target-Benutzeroberfläche beobachtet und betraf sowohl interne als auch Client-Konten. Diese Fehlerbehebung stellt eine konsistente Cookie-Behandlung sicher, indem doppelte Einträge verhindert und der Domain-Umfang ausgerichtet wird. So kann die Variante nahtlos gewechselt werden, ohne dass eine manuelle Cookie-Bereinigung erforderlich ist. (TGT-53579)
* **Es wurde ein Problem behoben, bei dem das Klicken auf Elemente auf einer bestimmten Homepage zu Speicherlecks führte.** Kunden, die Aktivitäten auf dieser Homepage erstellen, haben bei der Interaktion mit Seitenelementen Speicherlecks festgestellt. Das Problem war mit überhöhten Konsolenwarnungen und zunehmender Speichernutzung in Unterframes verbunden, insbesondere im Zusammenhang mit falsch formatierten Srcset-Attributen. Die Speichernutzung bleibt jetzt während der Interaktion stabil. (TGT-53761)
* **Es wurde ein Problem behoben, bei dem der VEC abstürzte und beim Laden bestimmter Aktivitäten einen leeren Bildschirm anzeigte.** Kunden eines bestimmten Mandanten meldeten, dass der Editor bestimmte Aktivitäten nicht laden konnte. Der VEC blieb bei „Anwenden erster Änderungen“ hängen, bevor er abstürzte und einen leeren Bildschirm anzeigte. Der VEC lädt jetzt betroffene Aktivitäten ohne Fehler im aktualisierten Prozess zur Erstellung von Aktivitäten. (TGT-52932)
* **Es wurde ein Problem behoben, bei dem [!UICONTROL &#x200B; Leiste „Inhalt verwalten] in [!UICONTROL Automated Personalization]-Aktivitäten inkonsistente Ortsbeschriftungen anzeigten.** Kunden meldeten, dass in [!UICONTROL &#x200B; Leiste &#x200B;]Inhalt verwalten“ auf den Registerkarten [!UICONTROL Erlebnisse] und [!UICONTROL Angebote] nicht übereinstimmende Standortnummern angezeigt wurden. (z. B. Standort 2 und Standort 4 in Erlebnissen und Standort 1 und Standort 2 in Angebot), selbst wenn nur zwei Standorte konfiguriert waren. Standortbeschriftungen sind jetzt konsistent und genau auf Änderungen abgebildet, was die Klarheit und Benutzerfreundlichkeit beim Erstellen von Aktivitäten verbessert. (TGT-52934)
* **Es wurde ein Problem behoben, bei dem Änderungen in VEC nach dem Speichern verloren gingen.** Kundinnen und Kunden berichteten, dass nach dem Speichern einer Änderung in VEC die Seite aktualisiert und die Änderung an die vorherige Version zurückgesetzt wird. Dieses Problem führte dazu, dass die letzten Aktualisierungen verloren gingen, es sei denn, die gesamte Aktivität wurde sofort gespeichert. Änderungen bleiben nun nach dem Speichern korrekt erhalten und der Editor macht Änderungen nicht mehr unerwartet rückgängig, was ein zuverlässiges Erlebnis im Arbeitsablauf für die Erstellung von Aktivitäten gewährleistet. (TGT-53500)
* **Verbesserte Elementauswahl in Visual Experience Composer durch Anzeige des Elementtyps beim Bewegen des Mauszeigers und bei der Auswahl.** Um die Benutzerfreundlichkeit während der Aktivitätserstellung zu verbessern, dekoriert der VEC jetzt HTML-Elemente mit ihrem Typ, wenn der Mauszeiger über sie bewegt oder sie ausgewählt werden. Diese Verbesserung hilft Kunden, die richtigen Elemente leichter zu identifizieren und auszuwählen. Ausgewählte Elemente werden farblich hervorgehoben, Elemente, auf die gezeigt wird, sind blau hervorgehoben. Der Elementtyp wird ebenfalls angezeigt, sodass der Kontext während der Bearbeitung klarer wird. (TGT-53502)

+++

### Datenstrom-Updates (19. September 2025)

Die Kombination aus Datenstrom-ID und Sandbox muss für [!DNL Adobe Target] Zielverbindungen eindeutig sein.

Die Validierungslogik für [!DNL Target] Zielverbindungen wurde aktualisiert, um zu erzwingen, dass die Kombination aus Datenstrom-ID und Sandbox-Name innerhalb einer IMS-Organisation eindeutig sein muss. Dies bedeutet:

* Dieselbe Datenstrom-ID und dasselbe Sandbox-Namenspaar können nicht über mehrere [!DNL Target] Zielverbindungen hinweg wiederverwendet werden.
* Dieselbe Datenstrom-ID kann nur für verschiedene Verbindungen verwendet werden, wenn sie in verschiedenen Sandboxes konfiguriert sind.
* Diese Regel gilt für alle ausgewählten Datenstrom, auch wenn „Keine“ ausgewählt ist.

Diese Aktualisierung stellt eine konsistente Konfiguration sicher und verhindert Konflikte in Multi-Sandbox-Umgebungen. Weitere Informationen finden Sie unter [Adobe Target-Verbindung](https://experienceleague.adobe.com/de/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} im *Experience Platform-Ziele* Handbuch.

### [!DNL Target Standard/Premium] 25.9.1 (5. September 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Experience Fragments]**

+++Details anzeigen

* **Verbesserte Benutzerzuordnung für [!UICONTROL AEM Experience Fragment] Angebote.** Es wurde ein Problem in VEC behoben, bei dem im Feld &quot;[!UICONTROL Zuletzt aktualisiert]&quot; für [!UICONTROL AEM Experience Fragment]&#x200B;(XF)-Angebote fälschlicherweise eine Code-ID anstelle des Benutzernamens angezeigt wurde. Diese Diskrepanz trat bei der Angebotsauswahl in der aktualisierten Benutzeroberfläche auf und führte zu Inkonsistenzen mit den alten Benutzeroberflächen- und HTML-Angeboten, die den Namen des letzten Editors korrekt anzeigten. Diese Fehlerbehebung stellt eine konsistente Benutzerzuordnung über alle Angebotstypen hinweg sicher und verbessert die Transparenz und Ausrichtung an dem erwarteten Verhalten. (TGT-52880 und TGT-52898)

+++

**Offer Decisioning**

+++Details anzeigen

* **Fehler bei der Angebotsentscheidung für ODE-Angebote behoben.** Es wurde ein Problem behoben, bei dem durch [!DNL Target] eingefügte ODE-Angebote (Offer Decisioning Engine) aufgrund fehlender Formatmetadaten einen 400-Fehler zurückgaben. Die Fehlermeldung deutete darauf hin, dass der MIME-Typ null war, was die erfolgreiche Verarbeitung von Angebotsentscheidungen verhinderte. Diese Fehlerbehebung stellt eine ordnungsgemäße Verarbeitung von Angebotsmetadaten sicher, stellt die Funktionalität für die Bereitstellung personalisierter Inhalte wieder her und ermöglicht die unterbrechungsfreie Ausführung von Marketing-Kampagnen. (TGT-53635)
* **Problem mit dem ODS-Angebot-Rendering behoben.** Es wurde ein Problem behoben, bei dem [!DNL Offer Decision Service] (ODS)-Angebote, die über [!DNL Adobe Journey Optimizer] (AJO) erstellt wurden, nicht gerendert wurden, wenn Aktivitäten mit dem VEC in der aktualisierten Benutzeroberfläche erstellt wurden. Dieselbe Konfiguration funktionierte in der alten Benutzeroberfläche korrekt, was zu Verwirrung und zur blockierten Kampagnenausführung führte. Diese Fehlerbehebung stellt die konsistente Bereitstellung von Angeboten für beide Benutzeroberflächenversionen sicher und stellt das erwartete Verhalten für die AJO-gesteuerte Personalisierung wieder her.

+++

**Berichte**

+++Details anzeigen

* **Die Option „Herunterladen“ wurde im Abschnitt „Berichte“ der aktualisierten Benutzeroberfläche „Berichte - Übersicht“ wiederhergestellt.** Es wurde ein Problem in der neuen Übersichts-Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Herunterladen] im Abschnitt Berichte fehlte, was Benutzer daran hinderte, Attributwertwerte zu exportieren. Diese Aktualisierung stellt die vollständige Exportfunktion wieder her und ermöglicht einen optimierten Zugriff auf herunterladbare Daten für Analysen und Berichte. (TGT-53222)
* **[!UICONTROL Vollständiger CSV-Bericht herunterladen] Schaltfläche in der Ansicht [!UICONTROL Wichtige Attribute] wiederhergestellt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche zur Aktivitätserstellung behoben, bei dem [!UICONTROL &#x200B; Schaltfläche „Vollständigen CSV-Bericht herunterladen] im Abschnitt [!UICONTROL Wichtige Attribute] in der Berichtsansicht fehlte. Mit dieser Fehlerbehebung wird der Zugriff auf herunterladbare Einblicke wiederhergestellt, um sicherzustellen, dass die Funktionen der aktualisierten und der alten Benutzeroberfläche konsistent sind. (TGT-53238)
* **Gelöste UI-Probleme mit Auswirkung auf [!UICONTROL Automatisches Targeting]-Reporting in der aktualisierten Übersichts-Benutzeroberfläche.** Fehlerkorrektur - In der aktualisierten Übersichtsoberfläche treten jetzt keine Probleme mehr auf, die sich auf das Reporting [!UICONTROL Automatisches Targeting] auswirken. Zu diesen Fehlerbehebungen gehören:

  * Fehlende Steigerung- und Konfidenzmetriken in Zusammenfassungsberichten
  * Falsche Farbanzeige für das Kontrollkästchen „Modelle erstellt“
  * Nicht funktionaler Diagrammbericht trotz Datenvarianz in [!DNL Analytics]
  * Fehlender Downloadlink für die Berichte [!UICONTROL Automatisierte Segmente] und [!UICONTROL Wichtige Attribute]
  * Beschädigte [!UICONTROL automatisierte Segmente] Berichtanzeige

  Diese Korrekturen stellen das erwartete Berichtsverhalten wieder her und verbessern die Sichtbarkeit der Leistung [!UICONTROL automatischen Targetings] in der aktualisierten Benutzeroberfläche. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++Details anzeigen

* **Die Formularvalidierung wurde in der aktualisierten Benutzeroberfläche um die Bedingungen für das Vorhandensein von Parametern korrigiert.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Kunden bei Auswahl von &quot;[!UICONTROL Benutzerdefinierter Mbox-Parameterwert ist &#x200B;]&quot; oder &quot;[!UICONTROL Parameter ist &#x200B;]&quot; fälschlicherweise einen Wert eingeben mussten. Dieses Verhalten steht im Konflikt mit der beabsichtigten Logik, die einfach prüft, ob ein Parameter unabhängig von seinem Wert vorhanden ist. Durch die Korrektur wird die Formularvalidierung an das erwartete Verhalten angepasst, was eine reibungslosere Einrichtung der Aktivitäten ermöglicht und die vollständige Übernahme der aktualisierten Benutzeroberfläche unterstützt. (TGT-53638)
* **Formularlogik korrigiert für Regeln zum Vorhandensein von Parametern im Seitenversand.“** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Benutzende bei der Auswahl von Seitenbereitstellungsregeln wie &quot;[!UICONTROL Parameter ist vorhanden]&quot;, &quot;[!UICONTROL Parameter ist nicht vorhanden],“[!UICONTROL Parameterwert ist &#x200B;]&quot; oder &quot;[!UICONTROL Parameterwert ist nicht vorhanden]&quot; fälschlicherweise einen zusätzlichen Parameterwert eingeben mussten. Dieses Verhalten war nicht konsistent mit der veralteten Benutzeroberfläche und widersprach der beabsichtigten Logik, das Vorhandensein von Parametern zu erkennen, ohne einen Wert anzugeben. Dieser Fix stellt das erwartete Regelkonfigurationsverhalten wieder her, optimiert die Aktivitätseinrichtung und verbessert die Benutzerfreundlichkeit. (TGT-53640)
* **Die Validierungslogik für den mehrseitigen Regel-Builder in der aktualisierten Benutzeroberfläche wurde verbessert.** Es wurden mehrere Validierungsprobleme im mehrseitigen Regel-Builder innerhalb der aktualisierten Benutzeroberfläche behoben. Zu diesen Fehlerbehebungen gehören:

  * Regelerstellung wird verhindert, wenn der mbox-Parameter leer ist
  * Anzeigen geeigneter Fehlermeldungen für ungültige Regelstatus
  * Korrigieren der Validierungslogik für unäre und parameterbasierte Operatoren, die keine Operandenwerte erfordern
  * Aktivieren von Hash-Fragmentregeln mit unären Operatoren durch Wiederherstellen der Speicherfunktion

  Diese Aktualisierungen stellen eine genaue Regelkonfiguration sicher und verbessern die Benutzerfreundlichkeit in komplexen Seitenbereitstellungsszenarien. (TGT-53722)
* **Problem mit dem Umbenennen des Speicherorts in A/B- und MVT-Aktivitäten behoben.** Es wurde ein Fehler in der aktualisierten Benutzeroberfläche behoben, durch den die Umbenennung eines Speicherorts in einer [!UICONTROL A/B]- oder [!UICONTROL Multivarianz-Test]&#x200B;(MVT)-Aktivität nach dem Navigieren zwischen der Speicherortliste, dem Targeting und zurück nicht beibehalten wurde. Durch diese Aktualisierung wird sichergestellt, dass Ortsnamenänderungen gespeichert und im gesamten Aktivitäts-Workflow konsistent übernommen werden. (TGT-52367)
* **Die Persistenz des Standortnamens für MVT- und AP-Aktivitäten in der aktualisierten Benutzeroberfläche wurde korrigiert.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem in Aktivitäten vom Typ [!UICONTROL Multivariater Test] (MVT) und [!UICONTROL Automated Personalization] (AP) bearbeitete Standortnamen nicht korrekt gespeichert wurden. Nach dem Umbenennen eines Speicherorts wurde durch das Navigieren zwischen Registerkarten [!UICONTROL Targeting] und [!UICONTROL Erlebnisse] der vorherige Status der Namen wiederhergestellt. Diese Fehlerbehebung stellt eine konsistente Ortsbenennung auf allen Registerkarten sicher und verbessert die Zuverlässigkeit bei der Einrichtung der Aktivität. (TGT-52927)
* **Standortbeschriftung im Bedienfeld Erlebnisse verwalten für MVT-Aktivitäten korrigiert.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem das Bedienfeld [!UICONTROL Erlebnisse verwalten] in Aktivitäten [!UICONTROL Multivariater Test] (MVT) eine inkonsistente Standortnummerierung anzeigte. Durch diese Korrektur wird sichergestellt, dass Standortbeschriftungen sequenziell sind und korrekt mit benutzerdefinierten Änderungen ausgerichtet werden, was die Klarheit und Benutzerfreundlichkeit während der Einrichtung des Erlebnisses verbessert. (TGT-52929)

+++

### [!DNL Target Standard/Premium] 25.8.4 (1. September 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Aktivitäten]**

+++Details anzeigen

* **Kunden konnten keine Aktivitäts- oder Dokumentnamen aus der [!UICONTROL Aktivitätsübersicht]** kopieren: Zuvor konnten Kunden den Namen einer Aktivität oder das zugehörige Angebot/Dokument nicht direkt aus der [!UICONTROL Aktivitätsübersicht] im aktualisierten Prozess zur Aktivitätserstellung kopieren. Diese Einschränkung beeinträchtigte die Benutzerfreundlichkeit, insbesondere bei kleineren Bildschirmen. Kunden können jetzt ohne Problemumgehungen einfach sowohl Aktivitäts- als auch Dokumentnamen kopieren. (TGT-51850)
* **Proaktive Aufnahme kuratierter [!DNL Target]-Kundendaten während der Aktivitätserstellung**: Der Prozess der Aktivitätserstellung wurde verbessert, indem die proaktive Erfassung von Berichten, Inhalten und Screenshots von [!DNL Target] Kunden ermöglicht wurde. Diese Verbesserung behebt Datenlücken, die in vorhandenen Anwendungsfällen identifiziert wurden, und sorgt für genauere Einblicke während der Aktivität und der Einrichtung von Experimenten. (TGT-52415)
* **AP-Aktivitäten konnten keine modellbereiten Daten im Abschnitt [!UICONTROL Berichte] abrufen**: Kundinnen und Kunden, die Automated Personalization (AP)-Aktivitäten im Abschnitt [!UICONTROL Berichte] angezeigt haben, konnten keine modellbereiten Indikatoren auf der Berichtgruppen- und Angebotsebene sehen. Dieses Problem trat auf, weil modellbereite Daten nicht korrekt aus dem Backend abgerufen wurden. Die Funktion wurde wiederhergestellt, und modellbereite Daten werden jetzt erwartungsgemäß angezeigt. (TGT-53600 und TGT-53601)
* **Für die Zukunft geplante Aktivitäten haben in der Übersicht über [!UICONTROL Aktivität] fälschlicherweise den Status &quot;[!UICONTROL Live]&quot;**: Kundinnen und Kunden haben beobachtet, dass Aktivitäten, die in der Zukunft beginnen sollen, in der Übersicht über [!UICONTROL Aktivität] fälschlicherweise als &quot;[!UICONTROL Live]&quot; gekennzeichnet wurden. Diese Statusabweichung wurde behoben, und geplante Aktivitäten werden jetzt korrekt als &quot;[!UICONTROL &quot; angezeigt] ohne dass die Seite aktualisiert werden muss. (TGT-52835)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen

* **Produktliste war im Dialogfeld [!UICONTROL Sammlung anzeigen] nicht sichtbar:** Zuvor konnten Kundinnen und Kunden die Produktliste nicht sehen, wenn sie eine Sammlung auf der Registerkarte [!UICONTROL Recommendations] ansahen. Das Dialogfeld [!UICONTROL Sammlung anzeigen] zeigt nun die zugehörigen Produkte korrekt an, was die Transparenz und Benutzerfreundlichkeit in der aktualisierten [!UICONTROL Recommendations]-Benutzeroberfläche verbessert. (TGT-50531)
* **Es wurde ein Problem behoben, das zu einer Filterung unter Berücksichtigung der Groß-/Kleinschreibung bei [!UICONTROL Produktkatalogsuche] erweiterten Suche** führte: Die erweiterte Suchfilterung auf der Seite [!UICONTROL Produktkatalogsuche] ignoriert jetzt korrekt die Groß-/Kleinschreibung und stimmt mit dem Verhalten sowohl des Backend- als auch des GraphQL-Services überein. Diese Aktualisierung stellt konsistente und genaue Vorschlagsergebnisse für Kunden sicher, unabhängig von der Groß-/Kleinschreibung. (TGT-53585)
* **Die erweiterte Suche in der aktualisierten Benutzeroberfläche [!UICONTROL Produktkatalogsuche] hat keine Vorschläge bereitgestellt**: Kundinnen und Kunden, die die erweiterte Suchfunktion in der aktualisierten Benutzeroberfläche [!UICONTROL Produktkatalogsuche] verwenden, mussten genaue Werte mit korrekter Schreibweise eingeben, da keine Vorschläge angezeigt wurden. Dieses Problem machte es schwierig, Produkte effizient zu finden. Vorschläge werden jetzt bei der Eingabe der erweiterten Suche wie erwartet angezeigt. (TGT-52008)
* **Einige genehmigende Personen konnten keine Produkte in der [!UICONTROL Produktkatalogsuche]** anzeigen: Kundinnen und Kunden mit [!UICONTROL genehmigenden Person]-Berechtigungen konnten keine Produkte in der [!UICONTROL Produktkatalogsuche] sehen, obwohl andere Benutzende mit identischen Rollen Zugriff hatten. Dieses Problem wurde durch eine Berechtigungsinkonsistenz verursacht, die sich auf die Katalogsichtbarkeit auswirkte. Alle genehmigenden Personen können jetzt Produkte wie erwartet im Abschnitt [!UICONTROL Recommendations] anzeigen. (TGT-53617)

+++ 

**[!UICONTROL Berichte]**

+++Details anzeigen

* **Berichte konnten für die Desktop-Zielgruppe aufgrund eines Fehlers bezüglich eines ungültigen Zielgruppennamen nicht geladen werden**: Beim Versuch, im Prozess zum Erstellen einer Aktivität Berichte für die eine Zielgruppe anzuzeigen, ist ein GraphQL-Fehler aufgetreten. Das System hat die Meldung „Ungültiger Zielgruppenname: XXXXX“ zurückgegeben, wodurch der Zugriff auf Berichtsdaten verhindert wurde. Berichte werden nun für die Desktop-Zielgruppe korrekt geladen. (TGT-53371)
* **Der Wechsel zwischen Zielgruppen auf der Seite „Berichte“ verursachte Fehler in der Target**-Benutzeroberfläche: Bei der Auswahl bestimmter Zielgruppen im Abschnitt [!UICONTROL Berichte] traten Fehler auf. Dieses Problem wurde durch eine ungültige Behandlung von Zielgruppen in Backend-GraphQL-Aufrufen verursacht, was zu unerwarteten Fehlern und fehlenden Daten führte. Das Problem wurde behoben, und Desktop-Zielgruppen werden jetzt ohne Fehler geladen - auch wenn keine Daten verfügbar sind. (TGT-53370)
* **[!UICONTROL Diagrammansicht] im Abschnitt [!UICONTROL Berichte] wurden keine Werte aus[!DNL Analytics]** angezeigt: Kunden, die auf [!UICONTROL Diagrammansicht] im Abschnitt Berichte“ zugreifen, haben fehlende Daten festgestellt, wobei alle Werte mit null angezeigt wurden. Dieses Problem wurde durch einen falschen Datenabruf von [!UICONTROL Analytics] verursacht. [!UICONTROL Diagrammansicht] zeigt jetzt erwartete Werte an. (TGT-52792)
+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Das Klicken auf „Cookies akzeptieren“ mit dem [!UICONTROL Enhanced Experience Composer] (EEC) ist aufgrund einer fehlenden Funktion fehlgeschlagen**: Kunden meldeten, dass der Versuch, Cookies über den EEC zu akzeptieren, zu einem Konsolenfehler führte: `handleclickAcceptAllButton is not defined`. Die Cookie-Akzeptanzfunktion funktioniert jetzt erwartungsgemäß und sorgt in der aktualisierten Benutzeroberfläche für ein reibungsloseres Erlebnis bei der Erstellung von Aktivitäten. (TGT-52794)
* **In der neuen EEC-Benutzeroberfläche konnten bestimmte Seiten nicht geladen werden, die zuvor in der alten Benutzeroberfläche unterstützt wurden**: Kundinnen und Kunden meldeten, dass der neue EEC einige Seiten nicht laden konnte, auf die in der alten Benutzeroberfläche trotz auf der Site vorhandenem iframe-Busting-Code zugegriffen werden konnte. Der aktualisierte Prozess zur Erstellung von Aktivitäten unterstützt jetzt das Laden dieser Seiten und stellt die Kompatibilität für Workflows zur Aktivitätserstellung wieder her. (TGT-53061)
* **Der VEC zeigte beim Bearbeiten von Erlebnissen einen leeren weißen Bildschirm an**: Kunden eines bestimmten Mandanten berichteten, dass der VEC-Bildschirm leer war, wenn sie versuchten, Erlebnisse in dem aktualisierten VEC zu bearbeiten. Dieses Problem betraf sowohl neu erstellte als auch ältere Aktivitäten und verhinderte so die Workflow-Kontinuität. Der VEC wird jetzt korrekt geladen, sodass Kunden Erlebnisse ohne Unterbrechung bearbeiten können. (TGT-53547)
* **Der VEC stürzte ab und zeigte beim Laden bestimmter Aktivitäten einen leeren Bildschirm an**: Kunden eines bestimmten Mandanten berichteten, dass der VEC bestimmte Aktivitäten nicht laden konnte. Der Erlebnis-Editor blieb bei „Anwenden erster Änderungen“ hängen, bevor er abstürzte und einen leeren Bildschirm anzeigte. Konsolenfehler zeigen an, dass nicht definierte Eigenschaften nicht gelesen werden konnten. Der Editor lädt jetzt betroffene Aktivitäten ohne Fehler in den aktualisierten VEC. (TGT-53548)
* **Das Löschen aller Datumswerte mithilfe der Rücktaste hat zu einem Absturz der Seite geführt**: Kundinnen und Kunden, die Aktivitäten im Abschnitt [!UICONTROL Ziele und Einstellungen] planen, haben einen Absturz erlebt, wenn sie die Rücktaste verwendet haben, um alle Werte aus den Feldern &quot;[!UICONTROL Angegebenes Datum und Uhrzeit] zu löschen. Dieses Problem wurde durch einen Null-Referenzfehler in der Datumsbehandlungslogik verursacht. Die Seite verarbeitet leere Datumseingaben jetzt ohne Abstürze problemlos. (TGT-53624)
* **Aufgrund einer ungültigen Payload sind keine Produkte in [!UICONTROL Produktkatalogsuche] angezeigt**: Kunden, die auf den [!UICONTROL Recommendations]-Abschnitt in [!UICONTROL Produktkatalogsuche], haben leere Ergebnisse festgestellt, die durch eine ungültige GraphQL-Payload verursacht wurden. Aufgrund dieses Backend-Fehlers konnten Produktdaten nicht korrekt geladen werden. Produkte werden nun in der aktualisierten Benutzeroberfläche erwartungsgemäß angezeigt. (TGT-53630)
* **[!DNL Scene7]Bilder wurden im aktualisierten VEC** mit niedrigerer Auflösung gespeichert: Kunden, die Erlebnisse im aktualisierten VEC bearbeiteten, bemerkten, dass [!UICONTROL Scene7]-Bild-URLs ohne Auflösungsparameter gespeichert wurden, was dazu führte, dass Bilder in schlechterer Qualität bereitgestellt wurden (400×400 anstelle der vorgesehenen 800×800). Bild-URLs behalten jetzt die richtigen Parameter bei, um eine ordnungsgemäße Auflösung sicherzustellen. (TGT-52631)
* **Live-Aktivitäten konnten weiterhin in VEC bearbeitet werden**: Kunden konnten auf Bearbeitungsoptionen für Live-Aktivitäten in dem aktualisierten VEC zugreifen, was zu unbeabsichtigten Änderungen führen konnte. Dieses Problem wurde behoben, indem die Bearbeitungsfunktion für Live-Aktivitäten deaktiviert wurde. Schaltflächen zum Bearbeiten sind jetzt für Bearbeiter in der Aktivitätenliste und in der Übersicht ausgeblendet, während Genehmigende und andere Rollen nicht betroffen sind. (TGT-53055)
* **Der Abschnitt [!UICONTROL Fehlgeschlagen] und [!UICONTROL Entwurf] im aktualisierten VEC wurde eingestellt** Die Optionen [!UICONTROL Fehlgeschlagen] und [!UICONTROL Entwurf] wurden aus dem aktualisierten VEC entfernt. Die neue Benutzeroberfläche unterstützt keine Entwurfsstatus mehr, und fehlgeschlagene Kampagnen werden nicht im Backend gespeichert. Diese Optionen sind nicht mehr relevant. Die zugehörigen Filter und Backend-Felder (z. B. `uiSyncFailed`, `errorMessage`) wurden ebenfalls entfernt, um die Aktivitätsverwaltung zu optimieren. (TGT-53150)
* **Anmeldung beim VEC für eine Aktivität nicht möglich**: Kunden, die versuchen, sich über den VEC bei ihrer Website anzumelden, wurden wiederholt zur Anmeldeseite weitergeleitet, wodurch der Zugriff auf die Aktivitätsbearbeitung verhindert wurde. Dieses Problem war intern nicht reproduzierbar und stand möglicherweise im Zusammenhang mit der Site-seitigen Sitzungsverarbeitung. Der Anmeldefluss wurde stabilisiert und Kunden können jetzt ohne Weiterleitungsfehler auf den VEC zugreifen. (TGT-53524)
* **Durch zweimaliges Drücken der Zurück-Taste im [!UICONTROL Durchsuchen]-Modus stürzte der VEC ab**: Kunden, die im VEC durch den [!UICONTROL Durchsuchen]-Modus navigierten, stürzten ab, wenn die Zurück-Taste des Browsers zweimal gedrückt wurde. Dieses Problem führte dazu, dass der Editor eingefroren ist und eine Seitenaktualisierung erforderlich wurde. Der Editor verarbeitet die Rücknavigation nun zuverlässig, ohne dass es zu Abstürzen kommt. (GT-53568)
* **Aktivitäten konnten aufgrund nicht definierter Standortzuordnungen nicht bearbeitet werden**: Beim Versuch, Aktivitäten zu bearbeiten, ist ein Fehler aufgetreten, der durch nicht definierte Standort-IDs in der `LocationMapping.behaviorTargetedActivity`-Logik verursacht wurde. Dieses Problem führte zu einem 400-Fehler und blockierten Aktivitätsaktualisierungen. Aktivitäten können jetzt ohne standortbezogene Validierungsfehler bearbeitet werden. (TGT-53607)
* **Speicheraktivitäten haben einen Fehler „Ungültige Benutzereingabe“ ausgelöst**: Kunden haben einen Fehler „Ungültige Benutzereingabe“ festgestellt, wenn sie versucht haben, Aktivitäten zu speichern, nachdem sie kleinere Änderungen im aktualisierten VEC vorgenommen hatten. Der Fehler wurde durch nicht übereinstimmende Standortzuordnungen in der Backend-Validierungslogik verursacht. Aktivitäten können jetzt erfolgreich gespeichert werden, ohne dass ortsbezogene Fehler ausgelöst werden. (TGT-53603)

+++

### [!DNL Target Standard/Premium] 25.8.3 (21. August 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Aktivitäten]**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem beim Speichern von Aktivitäten aufgrund fehlerhafter Eigenschaftsdaten ein Fehler wegen ungültiger Benutzereingabe** wurde: Beim Versuch, vorhandene Aktivitäten zu speichern, trat ein kritischer Fehler auf. Die Fehlermeldung wies auf eine ungültige Benutzereingabe hin und verwies insbesondere auf einen nicht erkannten Inhalt mit dem Eigenschaftsnamen in der JSON-Payload. Insbesondere wurden neue Aktivitäten, die dieselbe Eigenschaft verwenden, erfolgreich gespeichert, was darauf hindeutet, dass das Problem auf die alten Aktivitätsdaten beschränkt wurde. Der Prozess zur Erstellung von Aktivitäten verarbeitet jetzt korrekt veraltete Eigenschaftskonfigurationen, verhindert ungültige Eingabefehler und stellt ein konsistentes Speicherverhalten für neue und vorhandene Aktivitäten sicher. (TGT-53507)
* **Es wurde ein Problem behoben, das Kunden daran hinderte, eine Aktivität aufgrund eines InvalidProperty.Json-Fehlers zu speichern**: Beim Versuch, eine Aktivität in der aktualisierten Benutzeroberfläche zu speichern, trat ein Fehler auf, auch ohne dass Änderungen vorgenommen wurden. Die Fehlermeldung weist auf eine ungültige JSON-Struktur hin: „Ungültige JSON. Unbekannter Eigenschaftsname „content“. Speicherort: Zeile - 1, Spalte - 432.“ Dieses Problem wurde durch eine nicht erkannte Eigenschaft in der Anfrage-Payload verursacht und wurde nun behoben. Kunden können Aktivitäten erfolgreich speichern, ohne diesen Fehler zu bemerken. (TGT-53513)
* **Es wurde ein Problem behoben, bei dem geplante Aktivitäten fälschlicherweise einen [!UICONTROL Live]-Status bis zur Seitenaktualisierung angezeigt**: Kunden beobachteten, dass beim Planen der Live-Schaltung einer Aktivität zu einem zukünftigen Datum und zu einer zukünftigen Uhrzeit der Status sofort [!UICONTROL Live] anstelle von [!UICONTROL Geplant] angezeigt wurde. Dies führte zu Verwirrung, obwohl die Bestätigungsmeldung korrekt angibt, dass die Aktivität geplant war. Beim Aktualisieren der Seite wurde die Statusanzeige korrigiert. Dieses Problem wurde jetzt behoben, und geplante Aktivitäten zeigen den Status Geplant korrekt an, ohne dass eine Aktualisierung erforderlich ist. (TGT-52937)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem Kundinnen und Kunden während des Prozesses zur Erstellung einer Aktivität keine Report Suite-Namen eingeben konnten**: Kundinnen und Kunden, die [!DNL Adobe Analytics] als Berichtsquelle während des Prozesses zur Erstellung einer Aktivität verwenden, konnten keine Eingaben in die Dropdown-Liste [!UICONTROL Report Suite] vornehmen, um nach bestimmten Report Suites zu suchen. Dies wirkte sich auf Workflows für Unternehmen mit einer großen Anzahl von Report Suites aus, bei denen das manuelle Scrollen die Einrichtung erheblich verzögerte. Die Dropdown-Liste war nicht alphabetisch geordnet und reagierte nicht konsistent auf eingegebene -Eingaben, was es schwierig machte, Report Suites wie „Office + Store - Web - Produktion“ zu finden. Dieses Problem wurde behoben, und Kundinnen und Kunden können jetzt effizient suchen, indem sie Report Suite-Namen eingeben. (TGT-53345)

+++

**[!UICONTROL Zielgruppen]**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem abgelaufene „Zeitrahmen“-Zielgruppen das Speichern von Aktivitäten blockierten, selbst nachdem sie entfernt worden waren**: Kunden konnten Aktivitäten in der aktualisierten Benutzeroberfläche aufgrund eines Fehlers im Zusammenhang mit abgelaufenen „Zeitrahmen“-Zielgruppen nicht speichern. Selbst nach dem Entfernen der betroffenen Zielgruppe blieb die Fehlermeldung bestehen: „Aktivität enthält Zielgruppe mit ungültigem Zeitrahmen.“ Dieses Problem trat auf, weil das System die Zielgruppe „Nur Aktivität“ weiterhin validierte, auch wenn sie nicht mehr verwendet wurde. Das Verhalten wurde durch Zeitzonendiskrepanzen weiter kompliziert. Die Validierungslogik wurde korrigiert, und Kundinnen und Kunden können jetzt Aktivitäten speichern, ohne diesen Fehler zu bemerken. (TGT-53517)

+++

**[!UICONTROL Experience Fragment]e**

+++Details anzeigen

* **Es wurde ein Problem behoben, das Kunden daran hinderte, Experience Fragments mithilfe von [!UICONTROL Einfügen vor] oder [!UICONTROL Einfügen nach] in der Benutzeroberfläche einzufügen.** Kunden traten beim Versuch, [!UICONTROL Experience Fragments] mithilfe der Optionen „Einfügen vor“ oder „Einfügen nach“ in der aktualisierten Benutzeroberfläche in eine Aktivität einzufügen, auf einen Fehler auf. Die angezeigte Fehlermeldung war: „Angebotsinhalte müssen genau ein HTML-Element enthalten.“ Dieses Problem war spezifisch für die aktualisierte Benutzeroberfläche und trat in der vorherigen Version nicht auf. Dieses Problem wurde jetzt behoben, und Kundinnen und Kunden können [!UICONTROL Experience Fragments“ erfolgreich einfügen] ohne diesen Fehler zu bemerken. (TGT-53442)

+++

**[!UICONTROL Angebotsentscheidungen]**

+++Details anzeigen

* **Es wurde ein Problem behoben, das Kunden daran hinderte, Entscheidungsangebote zu bearbeiten und bestimmte Seitenelemente in der aktualisierten Benutzeroberfläche auszuwählen**: Während des aktualisierten Prozesses zum Erstellen von Aktivitäten konnten Kunden keine vorhandenen Entscheidungsangebote bearbeiten oder bestimmte Seitenelemente in Visual Experience Composer (VEC) auswählen. Entscheidungsangebote wurden fälschlicherweise als HTML-Angebote angezeigt und während der Bearbeitung vorgenommene Änderungen wurden nicht gespeichert. Darüber hinaus konnten bestimmte regionale URLs, z. B. die Japan-Site, nicht ordnungsgemäß in VEC geladen werden, was die Erstellung und Aktualisierung von Aktivitäten blockierte. Entscheidungsangebote werden jetzt korrekt angezeigt, Seitenelemente können erwartungsgemäß ausgewählt werden und regionale URLs werden ordnungsgemäß in VEC geladen, wodurch die volle Bearbeitungsfunktion wiederhergestellt wird. (TGT-53425)
* **Es wurde ein Problem behoben, bei [!UICONTROL Angebotsentscheidung] Selektoren nach dem Speichern nicht unerwartet geändert und geändert werden konnten**: Im aktualisierten Prozess zur Erstellung von Aktivitäten konnten Kundinnen und Kunden den Selektor [!UICONTROL Angebotsentscheidung] nicht wie beabsichtigt ändern. Der Versuch, den Selektor zu ändern, schlug fehl und der Selektor wurde nach dem Speichern auf einen falschen Wert zurückgesetzt. Dieses Verhalten führte dazu, dass das Entscheidungsangebot aus Visual Experience Composer (VEC) verschwand und weitere Bearbeitungen blockiert wurden. Selektoränderungen werden jetzt korrekt beibehalten und Entscheidungsangebote bleiben nach dem Speichern im VEC sichtbar und bearbeitbar. (TGT-53433)
* **Es wurde ein Problem behoben, bei [!UICONTROL Angebotsentscheidungen] nach dem Speichern aus der Aktivität verschwanden**: [!UICONTROL Angebotsentscheidungen], die während des Erstellungsprozesses der Aktivität hinzugefügt wurden, wurden nach dem Speichern und erneuten Öffnen der Aktivität nicht beibehalten. Dieses Problem trat beim Bearbeiten dynamischer Inhalte und beim Einfügen von [!UICONTROL Angebotsentscheidungen] mit bestimmten Selektoren und Eigenschaften auf. [!UICONTROL Angebotsentscheidungen] bleiben nach dem Speichern korrekt erhalten, und die Selektoren bleiben intakt, was ein konsistentes Targeting- und Bearbeitungsverhalten gewährleistet. (TGT-53434)

+++

**[!DNL Recommendations]**

+++Details anzeigen

* **Es wurde ein Problem in [!DNL Recommendations] Benutzeroberfläche behoben, bei dem der CSV-Download für benutzerdefinierte Kriterien den Fehler 404 zurückgab**: Es wurde ein Problem behoben, bei dem Kunden die CSV-Datei für benutzerdefinierte Kriterien beim Erstellen der Aktivität nicht herunterladen konnten. Der Download-Link funktioniert jetzt ordnungsgemäß, sodass Kunden benutzerdefinierte Kriterien wie erwartet exportieren können. (TGT-51966)
* **Inkonsistentes Laden von Bildern in [!UICONTROL Katalogsuche]**: Es wurde ein Problem behoben, bei dem Miniaturansichten und Bilder in [!UICONTROL Katalogsuche] beim Erstellen der Aktivität nicht konsistent geladen wurden. Bilder werden nur angezeigt, wenn die Spalte „Miniatur-URL“ sichtbar war und einige Produktbilder nach Navigations- oder Suchaktionen teilweise oder überhaupt nicht geladen wurden. Das Ladeverhalten des Bildes wurde stabilisiert, und Miniaturansichten werden nun unabhängig von der Sichtbarkeit der Spalte oder von Navigationsaktionen zuverlässig angezeigt. (TGT-52778)
* **Es wurde ein Problem behoben, durch das die Bearbeitung einer Empfehlung in einem duplizierten Erlebnis das ursprüngliche Erlebnis beeinträchtigte**: Kundinnen und Kunden berichteten, dass die Änderung einer Empfehlung in einem duplizierten Erlebnis das ursprüngliche Erlebnis unbeabsichtigt veränderte. Insbesondere nach dem Duplizieren von Erlebnis B im Prozess zur Erstellung der Aktivität und dem Bearbeiten des Designs oder der Kriterien wurden dieselben Änderungen im ursprünglichen Erlebnis B widergespiegelt, obwohl es sich um separate Entitäten handelte. Duplizierte Erlebnisse behalten jetzt separate Konfigurationen bei, sodass Änderungen an einem Erlebnis keine Auswirkungen auf das Original haben. (TGT-53369)
* **Es wurde ein Problem behoben, bei dem Änderungen an einem duplizierten Erlebnis das ursprüngliche Erlebnis in einer Aktivität unbeabsichtigt beeinträchtigten**: Kundinnen und Kunden berichteten, dass beim Duplizieren eines Erlebnisses innerhalb einer Aktivität und beim Zuweisen einer neuen Zielgruppe alle Änderungen am Design oder an den Kriterien des duplizierten Erlebnisses auch im ursprünglichen Erlebnis widergespiegelt wurden. Dieses Problem trat auf, obwohl keine direkten Änderungen an der Originalversion vorgenommen wurden, was die Möglichkeit beeinträchtigte, unabhängige Varianten innerhalb derselben Aktivität zu erstellen. Der Prozess zur Erstellung von Aktivitäten isoliert jetzt doppelte Erlebnisse korrekt, sodass Änderungen an einem Erlebnis keine Auswirkungen auf das Original haben. (TGT-53361)
* **Es wurde ein Problem behoben, bei dem [!UICONTROL Empfehlungskatalog] zeitweise keine vollständigen Produktattributdaten anzeigen konnte**: In der aktualisierten [!DNL Recommendations]-Benutzeroberfläche trat ein Problem auf, bei dem bestimmte Produktattribute, wie z. B. Nachricht, nicht konsistent in den [!UICONTROL Katalogsuche] angezeigt wurden, obwohl die Daten im Feed vorhanden waren. Aufgrund dieses Problems mussten Kundinnen und Kunden die Sichtbarkeit der Spalten manuell neu konfigurieren, um die fehlenden Werte abzurufen. [!UICONTROL Katalogsuche] zeigt jetzt zuverlässig alle konfigurierten Attribute an, sodass keine manuellen Spaltenzurücksetzungen mehr erforderlich sind. (TGT-52769)
* **Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem eine &#x200B;]Front-Promotion“ in einer Live-Aktivität nicht deaktiviert werden konnte**: Versuche, eine [!UICONTROL Front-Promotion] in einer Live-Aktivität zu deaktivieren, wurden nicht gespeichert. Nach Auswahl [!UICONTROL Change Promotion] und Deaktivierung blieb die Promotion beim erneuten Bearbeiten der Aktivität aktiv, was Aktualisierungen an Empfehlungskonfigurationen verhinderte. Die Einstellungen für die Promotion werden jetzt korrekt gespeichert, sodass Kundinnen und Kunden Promotion-Aktionen in Live-Aktivitäten wie erwartet deaktivieren oder ändern können. (TGT-53231)
* **Es wurde ein Problem behoben, bei dem die Aktivierung einer [!DNL Recommendations] [!UICONTROL Promotion] ohne Daten eine unklare Fehlermeldung auslöste**: Die Aktivierung einer [!UICONTROL Front]- oder [!UICONTROL Back-Promotion] in einer [!DNL Recommendations]-Aktivität ohne Angabe erforderlicher Werte führte zu einer allgemeinen „Ungültiger Eingabefehler“-Nachricht. Das zugrunde liegende Problem war ein fehlendes Konfigurationsfeld, aber die Fehlermeldung gab die Ursache nicht klar an, was die Fehlerbehebung erschwerte. Der Prozess zur Erstellung von Aktivitäten bietet jetzt eine klare und verwertbare Fehlermeldung, wenn erforderliche Felder wie `collectionId` oder Regeln fehlen, sodass Kunden Konfigurationsprobleme schnell identifizieren und beheben können. (TGT-52616)
* **Es wurde ein Problem behoben, das die Anzeige der [!UICONTROL Produkt]-Liste im [!UICONTROL Bearbeiten]-Modal auf der Registerkarte [!UICONTROL Recommendations]** verhinderte: Kunden konnten die gefilterte Produktliste beim Bearbeiten einer [!UICONTROL Sammlung] oder [!UICONTROL Ausschluss] auf der Registerkarte [!UICONTROL Recommendations] nicht anzeigen. Es wurde erwartet, dass die Liste in Echtzeit auf der Grundlage der angewendeten Regeln aktualisiert wird, aber sie erschien nicht wie beabsichtigt. Dieses Problem wurde behoben, und die Produktliste wird jetzt korrekt angezeigt und dynamisch aktualisiert, wenn Regeln geändert werden. (TGT-53481)
* **Es wurde ein Problem mit dem Layout des Dialogfelds „Details anzeigen“ in der aktualisierten Benutzeroberfläche behoben**: Das Layout des Modals „Details anzeigen“ in der aktualisierten Benutzeroberfläche wurde geändert, um die Klarheit und Benutzerfreundlichkeit zu verbessern. Das Dialogfeld enthält jetzt zwei Registerkarten:
  * [!UICONTROL Details]: Zeigt alle relevanten Informationen für das ausgewählte Element an.
  * Registerkarte [!UICONTROL Inventar]: Zeigt alle Produkte an, die nach den aktuellen Sammlungs- und Ausschlussregeln gefiltert wurden.

  Diese Verbesserung hilft Kunden, im Rahmen des Prozesses zur Erstellung von Aktivitäten einfacher durch artikelspezifische Daten und den Inventarkontext zu navigieren und diese zu verstehen. (TGT-53503)

  * **Es wurde ein Problem behoben, bei dem entfernte Promotions in Recommendations-Aktivitäten nach dem Speichern wieder auftraten**: Kundinnen und Kunden berichteten, dass beim  oder [!UICONTROL Zurück] von [!DNL Recommendations] Aktivitäten und beim Speichern der Aktivität die Promotions beim erneuten Öffnen weiterhin angezeigt wurden. Dieses Problem trat sowohl in der Staging- als auch in der Produktionsumgebung auf und hatte Auswirkungen auf den aktualisierten Prozess der Aktivitätserstellung. Das Problem wurde behoben. Promotions, die aus einer Aktivität entfernt wurden, bleiben jetzt nach dem Speichern korrekt erhalten. (TGT-53490)

+++

**Berichte**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem der Bericht [!UICONTROL Automatisierte Segmente] null Zielgruppenwerte anzeigte**: Kundinnen und Kunden meldeten, dass [!UICONTROL Automatisierte Segmente] in Aktivitätsberichten null für Zielgruppendaten zeigten, was eine genaue Analyse der Segmentleistung verhinderte. Dieses Problem trat beim Zugriff auf den Abschnitt [!UICONTROL Berichte] und bei der Auswahl [!UICONTROL Automatisierte Segmente] auf, obwohl gültige Zielgruppendaten erwartet wurden. [!UICONTROL Automatisierte Segmente] zeigt jetzt die Zielgruppenwerte korrekt an, um zuverlässige Berichte und Segmentierungseinblicke sicherzustellen. (TGT-52793)

+++

**Single Page Applications (SPAs)**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem beim Wechseln zwischen [!UICONTROL Durchsuchen]- und [!UICONTROL Design]-Modus der SPA-Status in der aktualisierten Benutzeroberfläche zurückgesetzt wurde**: Kundinnen und Kunden berichteten, dass der Wechsel zwischen [!UICONTROL Durchsuchen]- und [!UICONTROL Design]-Modus in der aktualisierten Benutzeroberfläche dazu führte, dass der Web-Editor neu geladen wurde, wodurch der Status von SPAs zurückgesetzt wurde. Durch dieses Problem wurden Workflows unterbrochen und Kunden mussten die Informationen erneut eingeben. Das Problem wurde behoben. Der SPA-Status wird jetzt beim Wechseln zwischen Modi beibehalten, was ein reibungsloseres und konsistenteres Erlebnis bei der Erstellung von Aktivitäten gewährleistet. (TGT-53074)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das die Progression zum Schritt [!UICONTROL Targeting] in AP-Aktivitäten blockierte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden nicht in der Lage waren, mit dem Schritt [!UICONTROL Targeting] in [!UICONTROL Automated Personalization] (AP)-Aktivitäten fortzufahren, es sei denn, zwei Standorte wurden hinzugefügt. Dieses Verhalten unterschied sich vom vorherigen Erlebnis, bei dem ein einzelner Standort mit mehreren Angeboten ausreichend war. Die Anforderung wurde korrigiert, sodass Kundinnen und Kunden weiterhin Einzelspeicherort-Setups als Teil ihrer API-Workflows verwenden können. (TGT-53426)
* **Es wurde ein Problem behoben, bei dem der neue Prozess zum Erstellen von Aktivitäten den Parameter „fmt=png-alpha“ für transparente Bilder nicht**: In der aktualisierten Benutzeroberfläche enthielten Bilder, die während des Prozesses zum Erstellen von Aktivitäten eingefügt wurden, nicht mehr standardmäßig den Parameter &quot;`fmt=png-alpha`&quot;, was zu einem Verlust der Transparenz führte. Dieses Verhalten unterschied sich von dem der vorherigen Benutzeroberfläche, die den -Parameter automatisch an Bild-URLs angehängt hat, wobei transparente Hintergründe beibehalten wurden. Der Prozess zur Erstellung von Aktivitäten wendet nun den `fmt=png-alpha`-Parameter korrekt auf Bild-URLs an, wenn Transparenz erforderlich ist, um ein konsistentes Rendering transparenter Assets sicherzustellen. (TGT-52615)
* **Es wurde ein Problem behoben, das Kunden daran hinderte, in der aktualisierten Benutzeroberfläche nach Report Suites zu suchen**: In der aktualisierten Benutzeroberfläche konnten Kunden in der Dropdown-Liste [!UICONTROL Report Suites] im Abschnitt [!UICONTROL Ziele und Einstellungen] keine Eingaben vornehmen und suchen, wodurch es schwierig wurde, bestimmte Report Suites zu finden, insbesondere für Mandanten mit einer großen Anzahl von Einträgen. Im Gegensatz zur vorherigen Benutzeroberfläche war die Liste nicht sortiert und es fehlte eine eingabebasierte Filterung. Dieses Problem wurde behoben. Kunden können jetzt tippen, um Report Suites zu suchen und zu filtern, und so die in der alten Benutzeroberfläche verfügbaren Funktionen wiederherstellen. (TGT-53514)

+++

**[!UICONTROL Arbeitsbereiche]**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem eine Kundin oder ein Kunde, die bzw. der auf einen einzigen Arbeitsbereich beschränkt war, Aktivitäten aus anderen Arbeitsbereichen anzeigen konnte**: Kundinnen und Kunden mit Zugriff auf einen Arbeitsbereich konnten unerwartet Aktivitäten in allen Arbeitsbereichen anzeigen, wenn sie [!UICONTROL Alle Arbeitsbereiche] im Prozess zur Erstellung einer Aktivität auswählten. Diese Sichtbarkeit birgt das Risiko von unbeabsichtigten Änderungen an Live-Aktivitäten in anderen Arbeitsbereichen, die sich möglicherweise auf die Website-Leistung auswirken. Die Zugriffssteuerungen für Workspace wurden verbessert, um sicherzustellen, dass Kunden nur Aktivitäten in ihrem zugewiesenen Arbeitsbereich anzeigen und mit ihnen interagieren können. (TGT-53101)
* **Es wurde ein Problem behoben, bei dem ein Kunde Aktivitäten aus der [!UICONTROL Standard-Workspace] ohne Zugriff anzeigen konnte:** Ein Kunde mit Zugriff, der auf den Staging-Arbeitsbereich beschränkt war, konnte Aktivitäten aus der [!UICONTROL Standard-Workspace] über den Prozess zur Erstellung von Aktivitäten anzeigen. Dieses Verhalten trat trotz korrekter Backend-Konfiguration und Zugriffsrechten auf. Die Zugriffssteuerungen für Workspace wurden verbessert, um sicherzustellen, dass Kunden Aktivitäten nur in ihrem zugewiesenen Arbeitsbereich anzeigen können. (TGT-53297)

+++

### [!DNL Target Standard/Premium] 25.8.2 (14. August 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

**[!UICONTROL Aktivitäten]**

+++Details anzeigen

* **Problem beim Laden von Aktivitäten in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben**: Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem bestimmte Aktivitäten beim Versuch, sie zu bearbeiten, nicht geladen werden konnten. Dieses Problem führte dazu, dass Kundinnen und Kunden Benutzende in einem Bildschirm für das unbegrenzte Laden ließen. Dieses Problem wirkte sich auf mehrere Aktivitäten aus und wurde als inkonsistent über Kunden hinweg gemeldet. Mit dieser Fehlerbehebung werden die betroffenen Aktivitäten jetzt ordnungsgemäß geladen, was eine nahtlose Bearbeitung ermöglicht und Unterbrechungen der Aktivitäts-Workflows reduziert. (TGT-53209)
* **Fehler beim Speichern einer Aktivität im Erstellungsprozess aufgrund einer `optionLocalId` Validierung**: Es wurde ein Problem im Erstellungsprozess einer Aktivität behoben, das Kunden daran hinderte, Änderungen aufgrund eines Backend-Validierungsfehlers zu speichern: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Dieses Problem trat beim Ändern bestimmter Elemente innerhalb einer Aktivität auf, was zu einem fehlgeschlagenen Speichervorgang führte. Die Korrektur stellt sicher, dass `optionLocalId` Verweise jetzt korrekt validiert werden, sodass Kunden Aktivitäten speichern können, ohne diesen Fehler zu bemerken. (TGT-53293)
* **Absturz beim Erstellen von Aktivitäten behoben, der durch ungültige Optionsverweise beim Wechseln von Seiten verursacht wurde**: Es wurde ein Problem beim Erstellen von Aktivitäten behoben, das dazu führte, dass die Benutzeroberfläche nach dem dreimaligen Wechsel von Seiten während der Bearbeitung abstürzte. Der Absturz wurde durch ungültige Optionsverweise ausgelöst, was zu Konsolenfehlern führte, wie z. B. „Option mit localId &#39;7&#39; nicht gefunden.“ Mit diesem Update können Kunden jetzt zwischen Seiten wechseln und Änderungen vornehmen, ohne Systemfehler oder -unterbrechungen festzustellen. (TGT-53295)
* **Fehler beim Speichern in einem Prozess zur Erstellung von Aktivitäten, der durch ungültige Benutzereingaben beim Bearbeiten von Erlebnissen verursacht wurde**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden Änderungen an einer Aktivität aufgrund eines Fehlers bei der ungültigen Benutzereingabe nicht speichern konnten. Der Fehler trat beim Ändern von Erlebnissen in der aktualisierten Benutzeroberfläche auf und verhinderte, dass Aktualisierungen übergeben wurden. Die Aktivität kann jetzt erfolgreich gespeichert werden, sodass Kunden sie ohne Unterbrechung bearbeiten und veröffentlichen können. (TGT-53267)
* **Ladeproblem beim Erstellen von Aktivitäten, das die Bearbeitung in der aktualisierten Benutzeroberfläche blockiert hat**: Es wurde ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kunden aufgrund eines Bildschirms zum kontinuierlichen Laden keine Aktivitäten in der aktualisierten Benutzeroberfläche bearbeiten konnten. Kunden können jetzt Aktivitäten öffnen und ändern, ohne dass Ladefehler auftreten. (TGT-53415)
* **Problem mit der Erlebnisanforderung im Prozess zur Erstellung von Aktivitäten für AP-Aktivitäten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem für [!UICONTROL Automated Personalization] (AP)-Aktivitäten zwei Standorte anstelle von zwei Erlebnissen in der aktualisierten Benutzeroberfläche erforderlich waren. Dieses Verhalten blockierte Anwendungsfälle, in denen Kunden einen einzelnen Standort mit mehreren Angeboten konfiguriert haben, was zuvor unterstützt wurde. Die Anforderung wurde entsprechend der ursprünglichen Funktionalität korrigiert, sodass Kundinnen und Kunden unabhängig von der Anzahl der Standorte mit AP-Aktivitäten mit zwei Erlebnissen fortfahren können. (TGT-53429)
* **Feldverhalten für getrackte Elemente im Klick-Tracking-Modus korrigiert, um nicht gespeicherte Eingaben zu verhindern und die Klarheit zu verbessern**: Es wurde ein Problem im Prozess zur Erstellung einer Aktivität behoben, bei dem das Feld [!UICONTROL Getracktes Element] im [!DNL Click Track]-Modus bearbeitbar war, aber den eingegebenen Namen nicht beibehielt, was zu Verwirrung bei den Kunden führte. Das Feld ist jetzt deaktiviert, um nicht gespeicherte Eingaben zu verhindern, und die Benennung ausgewählter Elemente wurde klarer formuliert, um die Zielkonfiguration und Tracking-Genauigkeit zu verbessern.** (TGT-53458)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das die Benennung von verfolgten Komponenten im Modus &quot;[!UICONTROL Klick-]&quot; blockierte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden verfolgte Komponenten im Modus [!UICONTROL Klick-] nicht benennen konnten. Nach der Eingabe eines Namens erschien das Feld bearbeitbar, behielt jedoch die Eingabe nicht bei. Standardmäßig werden im Bearbeitungsmodus allgemeine Bezeichnungen wie „MEIN PRIMÄRES ZIEL 0“ verwendet. Das Feld Nachverfolgte Elemente ist jetzt deaktiviert. Das Benennungsverhalten wurde klarer formuliert, um die Zieleinrichtung und -nachverfolgbarkeit zu verbessern. (TGT-51396)

+++

**Experience Fragments (XFs)**

+++Details anzeigen

* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das eine unbeabsichtigte Bearbeitung von aus AEM exportierten Fragmenten durch HTML ermöglichte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, durch das Kunden die aus [!DNL Adobe Experience Manager] (AEM) exportierten HTML of [!DNL Experience Fragments] (XFs) in [!DNL Target] bearbeiten konnten. Dieses Verhalten war unbeabsichtigt, da XFs nach der Veröffentlichung aus AEM für die Bearbeitung gesperrt bleiben sollten. Die Korrektur stellt sicher, dass die Option &quot;HTML bearbeiten“ für von AEM exportierte Fragmente nicht mehr verfügbar ist, wodurch die Inhaltsintegrität und die erwartete Governance erhalten bleiben. (TGT-53286)
* **Intermittierendes Vorschauproblem für XF-Inhalte im Prozess zur Erstellung von Aktivitäten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem XF-Inhalte intermittierend im Vorschaumodus in der aktualisierten Benutzeroberfläche nicht gerendert werden konnten. Obwohl der Inhalt korrekt bereitgestellt wurde, wurde die Vorschau nicht konsistent angezeigt, was es für Kunden schwierig machte, die Angebotseinrichtung zu validieren. XF-Vorschauen werden jetzt zuverlässig geladen, was die Konfidenz und Effizienz bei der Konfiguration von Aktivitäten verbessert. (TGT-53318)

+++

**QA-Modus**

+++Details anzeigen

* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem führende Leerzeichen in URLs fehlerhafte QA-Links verursachten**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem führende Leerzeichen in der Aktivitäts-URL beim Speichern nicht ordnungsgemäß abgeschnitten wurden. Dies führte zu ungültigen QA-Links und falscher Formatierung im Backend. Nach der Aktualisierung werden die URLs jetzt sauber gespeichert, was fehlerhafte Links verhindert und die Zuverlässigkeit der QA-Workflows für Kunden verbessert. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen

* **Es wurde ein Problem in der Benutzeroberfläche der Katalogsuche behoben, bei dem die erweiterte Suche keine Vorschläge bereitstellen konnte**: Es wurde ein Problem in der neuen Benutzeroberfläche [!UICONTROL Katalogsuche] behoben, bei dem die Funktion [!UICONTROL Erweiterte Suche] keine Vorschläge bereitstellen konnte. Die Benutzer mussten exakte Werte mit präziser Schreibweise eingeben, was die Suche umständlich und fehleranfällig machte. Mit dieser Fehlerbehebung bietet die [!UICONTROL Erweiterte Suche] jetzt relevante Vorschläge, wenn Benutzende tippen, die Benutzerfreundlichkeit verbessern und die Reibung bei der Suche nach Produkten reduzieren. (TGT-52008)
* **Es wurden mehrere UI- und Filterprobleme behoben, um die Reaktionsfähigkeit und die Entitätsinteraktion zu verbessern**: Es wurden mehrere Probleme behoben, darunter mangelhafte Reaktionsfähigkeit von Kriteriendetails auf Geräten mit kleinem Bildschirm, fehlende Ergebnisse bei der Auswahl von „Alle Hostgruppen“ im Umgebungsfilter und die Unfähigkeit, mit Entitäten ohne Namen zu interagieren. Diese Korrekturen verbessern die Benutzerfreundlichkeit über Bildschirmgrößen hinweg, stellen eine genaue Filterung sicher und ermöglichen eine vollständige Interaktion mit allen Produktentitäten, was das Gesamterlebnis für Benutzende verbessert. (TGT-52992)
* **Fehlende Produkt-IDs in der Detailansicht von Recommendations bei der Erstellung von Aktivitäten wurden behoben**: Es wurde ein Problem im Prozess zur Erstellung von [!DNL Recommendations]-Aktivitäten behoben, bei dem Produkt-IDs im Bildschirm mit den Produktdetails fehlten, was es Kunden erschwerte, Produkt-IDs während Workflows zu kopieren oder zu referenzieren. Die Produkt-IDs werden jetzt klar in der Detailansicht angezeigt, was die Sichtbarkeit verbessert und eine effizientere Produktverwaltung für Kunden unterstützt. (TGT-51964)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Produktnachrichten nicht in der Recommendations-Ansicht angezeigt wurden**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem in der Spalte [!UICONTROL Nachricht] in der [!DNL Recommendations]-Ansicht keine Produktdaten angezeigt wurden, obwohl Nachrichten vorhanden waren. Kunden mussten die Spalte manuell entfernen und erneut hinzufügen, um den Inhalt vorübergehend anzuzeigen, der beim Scrollen oder Suchen oft wieder verschwand. Diese Aktualisierung stellt die konsistente Sichtbarkeit von Produktnachrichten wieder her und verbessert die Katalognavigation und die Überprüfungs-Workflows. (TGT-52777)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem bei Auswahl von „Alle Hostgruppen“ in der Recommendations-Ansicht keine Ergebnisse zurückgegeben wurden**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem bei Auswahl der Umgebung „Alle Hostgruppen“ in der [!DNL Recommendations]-Ansicht keine Ergebnisse zurückgegeben wurden. Kunden können jetzt Produktdaten wie erwartet über alle Hostgruppen hinweg anzeigen und so die Sichtbarkeit und Filtergenauigkeit während der Einrichtung der Aktivität verbessern. (TGT-53006)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem der Umschalter für die vordere Promotion nach dem Speichern nicht beibehalten wurde**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem das Deaktivieren des Umschalters für die vordere Promotion in den Aktivitätseinstellungen nach dem Speichern nicht beibehalten wurde. Kunden, die versuchten, die Frontend-Promotion zu entfernen, sahen den Umschalter nach einem erneuten Besuch der Aktivität wieder aktiviert, was eine ordnungsgemäße Anpassung verhinderte. Diese Aktualisierung ermöglicht ein zuverlässiges Speichern von Änderungen, sodass Kunden die volle Kontrolle über die Promotioneinstellungen haben. (TGT-53215)
* **Inkonsistente Sortierung nach Spalte [!UICONTROL Letzte Aktualisierung] wurde behoben** Es wurde ein Problem beim Prozess der Aktivitätserstellung behoben, bei dem das Sortieren des Katalogs nach der Spalte [!UICONTROL Letzte &#x200B;]) zu inkonsistenten Ergebnissen führte. Kunden waren nicht in der Lage, Produktdaten basierend auf Aktualisierungszeitstempeln zuverlässig zu organisieren, was die Überprüfung und Verwaltung von Katalogen erschwerte. Die Sortierung funktioniert jetzt erwartungsgemäß und verbessert die Genauigkeit und Benutzerfreundlichkeit in der aktualisierten Benutzeroberfläche. (TGT-53116)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen

* **Probleme mit dem Laden der Aktivität und [!UICONTROL Abbrechen] Schaltflächen im Prozess zur Erstellung einer Aktivität behoben**: Es wurde ein Problem im Prozess zur Erstellung einer Aktivität behoben, bei dem bestimmte Aktivitäten nicht geladen werden konnten, sodass Kunden nicht auf Änderungen zugreifen konnten. Darüber hinaus reagierte die Schaltfläche [!UICONTROL Abbrechen] nicht, was Kunden daran hinderte, den Ladevorgang zu stoppen oder die Bearbeitungsansicht zu verlassen. Diese Fehlerbehebung stellt sicher, dass -Aktivitäten jetzt zuverlässig geladen werden und die Schaltfläche [!UICONTROL Abbrechen] wie erwartet funktioniert, was die Gesamtstabilität und das Benutzererlebnis in Visual Experience Composer verbessert. (VEC)(TGT-53218)
* **Problem beim Wechsel von Erlebnissen in der aktualisierten VEC-Benutzeroberfläche behoben, das die Bearbeitung blockierte und [!UICONTROL Schaltfläche Abbrechen] deaktivierte**: Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem Änderungen beim Wechsel zwischen Erlebnissen in einer Experience Targeting-(XT)-Aktivität nicht geladen werden konnten. Kunden konnten keine Erlebnisse bearbeiten, die über das ursprünglich eingegebene hinausgingen, und die Schaltfläche [!UICONTROL Abbrechen] fehlte oder reagierte nicht. Diese Fehlerbehebung stellt sicher, dass Änderungen jetzt in allen Erlebnissen korrekt geladen werden und dass die Schaltfläche [!UICONTROL Abbrechen] auch ohne die Helper-Erweiterung zuverlässig funktioniert. Dies verbessert die Bearbeitungs-Workflows und verringert die Frustration. (TGT-53256)
* **Problem mit weißem Bildschirm beim Wechsel zwischen mehreren Erlebnissen im Prozess zur Erstellung einer Aktivität behoben**: Es wurde ein Problem behoben, bei dem das Wechseln zwischen mehreren Erlebnissen zu einem weißen Bildschirm führte. Es wurde auch ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kunden auf einen weißen Bildschirm stießen, wenn sie versuchten, mehrere Erlebnisse innerhalb einer Aktivität zu ändern. Dieses Problem trat auf, nachdem Änderungen auf zwei Erlebnisse angewendet und dann ein drittes Erlebnis ausgewählt wurden, wodurch weitere Bearbeitungen verhindert wurden. Die Aktualisierung sorgt für einen reibungslosen Übergang zwischen Erlebnissen, sodass Kunden Änderungen ohne Unterbrechung vornehmen können. (TGT-53266)
* **Es wurde ein Problem in VEC behoben, bei dem benutzerdefinierte Code-Änderungen über Bearbeitungssitzungen hinweg nicht zuverlässig gespeichert wurden**: Es wurde ein Problem behoben, bei dem benutzerdefinierte Code-Änderungen, die in Visual Experience Composer (VEC) vorgenommen wurden, nicht zuverlässig in einem einzigen Versuch gespeichert wurden. Kunden meldeten, dass Änderungen wie Stilaktualisierungen oder HTML-Bearbeitungen zeitweise auf der Website und in den QA-URLs fehlten, selbst nachdem sie sowohl die Schaltflächen [!UICONTROL Inhalt bearbeiten] als auch [!UICONTROL Speichern] verwendet hatten. Diese Regression wurde behoben, sodass alle benutzerdefinierten Code-Änderungen über Bearbeitungssitzungen hinweg wie erwartet bestehen bleiben.** (TGT-53418)
* **Fehlende `triggerViews` in der aktualisierten Benutzeroberfläche während der Aktivitätserstellung wurden behoben**: Es wurde ein Problem im Prozess zur Aktivitätserstellung behoben, bei dem `triggerViews` nicht in der aktualisierten Benutzeroberfläche angezeigt wurden, obwohl sie auf der Seite korrekt implementiert waren. Dies wirkte sich auf mehrere Kunden aus und erschwerte die Validierung ansichtsbasierter Trigger während der Aktivitätseinrichtung. `TriggerViews` werden nun erwartungsgemäß angezeigt, sodass Kundinnen und Kunden ihre Konfigurationen zuverlässig abschließen und testen können. (TGT-53239)
* **Problem beim Laden von Ansichten im Prozess zur Erstellung von Aktivitäten für bestimmte Web-Seiten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Ansichten in der aktualisierten Benutzeroberfläche für bestimmte Web-Seiten nicht geladen wurden, obwohl sie korrekt implementiert und in Versand- oder Interaktionsaufrufen sichtbar waren. Dies wirkte sich auf mehrere Kunden aus und erschwerte die Validierung des ansichtsbasierten Targeting. Ansichten werden jetzt konsistent auf allen unterstützten Seiten angezeigt, was die Zuverlässigkeit bei der Einrichtung von Aktivitäten verbessert. (TGT-53246)
* **Problem beim zeitweisen Laden von Ansichten im Prozess zur Erstellung von Aktivitäten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Ansichten während der Aktivitätsbearbeitung zeitweise nicht in der aktualisierten Benutzeroberfläche angezeigt wurden. Obwohl der richtige Ansichtsname in der Netzwerk-Payload vorhanden war, wurde er in der Benutzeroberfläche nicht konsistent erkannt, was sich auf die Möglichkeit von Kundinnen und Kunden auswirkte, die ansichtsbasierte Personalisierung zu konfigurieren. Ansichten werden jetzt zuverlässig angezeigt und unterstützen eine reibungslosere Einrichtung und Validierungs-Workflows. (TGT-53223)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem verfolgte Aktionsnamen nicht in der aktualisierten Benutzeroberfläche gespeichert wurden**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem verfolgte Aktionsmetriken nicht in der aktualisierten Benutzeroberfläche gespeichert werden konnten. Nachdem ein getracktes Element benannt und die Aktivität gespeichert wurde, wurde der Name beim erneuten Öffnen auf eine Standardbeschriftung zurückgesetzt, was zu Verwirrung führte und die Zielkonfiguration unterbrach. Nachverfolgte Aktionen behalten jetzt ihre zugewiesenen Namen bei, sodass Kundinnen und Kunden Konversionsmetriken genau festlegen und verwalten können. (TGT-53453)

+++

### [!DNL Target Standard/Premium] 25.8.1 (7. August 2025)

Dieses Release umfasst die folgenden Erweiterungen und Fehlerbehebungen:

**Aktivitäten**

+++Details anzeigen

* Es wurden mehrere Probleme mit der aktualisierten Benutzeroberfläche behoben, darunter Fehler beim Löschen von Seitentypen aufgrund von Abständen in Eingabewerten, unzuverlässigen Aktivitätskopien zwischen Arbeitsbereichen und fehlerhaften Seitenbereitstellungsregeln in QS-Umgebungen. (TGT-52703)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Benutzende mit der [!UICONTROL Editor]-Rolle auf Live-Aktivitäten zugreifen und versuchen konnten, sie zu bearbeiten. Dies sollte eingeschränkt werden. In der Aktivitätsliste und den Übersichtsbildschirmen werden Bearbeitungsoptionen für Live-Aktivitäten fälschlicherweise angezeigt, was zu potenziellen unbeabsichtigten Änderungen führt. (TGT-53055)
* Fehlerkorrektur - In der Benutzeroberfläche [!UICONTROL Erweiterte Suche] werden Benutzer bei Auswahl der Operatoren „Wert ist vorhanden“ oder „Wert ist nicht vorhanden“ aufgefordert, einen Operanden einzugeben, der für diese Bedingungen nicht erforderlich sein sollte. (TGT-51961)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Versuche, Aktivitäten aus dem Staging in den Produktionsarbeitsbereich zu kopieren, durchgängig fehlgeschlagen sind, selbst in Sandbox-Umgebungen. Kunden stießen auf verschiedene Fehlermeldungen, darunter „Anonyme Zielgruppe bereits von der Aktivität verwendet“ und „Ungültige Zielgruppen-ID“, obwohl sie gültige Konfigurationen verwendeten und über geeignete Arbeitsbereich-Berechtigungen verfügten. (TGT-52394)

+++

**Experience Fragments (XFs)**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem Experience Fragment (XF)-Inhalte in der Vorschau [!UICONTROL Visual Experience Composer] (VEC) nicht gerendert werden können, obwohl sie in der Inhaltsbereitstellung ordnungsgemäß funktionieren. (TGT-53318)

+++

**Lokalisierung**

+++Details anzeigen

* Es wurde ein Lokalisierungsproblem behoben, bei dem die Schaltfläche „Promotion hinzufügen“ im Abschnitt „Promotions“ in mehreren Sprachumgebungen im QA-Mandanten nicht lokalisiert erschien. (TGT-53263)

+++

**Angebote**

+++Details anzeigen

* Es wurde ein Problem behoben, durch das beim Bearbeiten eines vorhandenen HTML-Angebots über Visual Experience Composer (VEC) alle Änderungen aus der Inhaltsbereitstellung entfernt wurden. Die Änderungen werden auf der Registerkarte Änderung ausgegraut angezeigt und werden in der QS-Vorschau nicht angezeigt, obwohl sie in der alten Benutzeroberfläche korrekt angewendet wurden. (TGT-52863)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Änderungen an HTML-Angeboten, die im [!UICONTROL Visual Experience Composer] (VEC) vorgenommen wurden, nach der Navigation von der Registerkarte [!UICONTROL Targeting] zurück zu [!UICONTROL Erlebnisse] blieben. (TGT-52874)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem das Einfügen eines HTML-Angebots vor und eines anderen nach demselben Selektor zu einer falschen Speicherortgenerierung führte. Als Kunden von der Registerkarte [!UICONTROL Targeting] zur Registerkarte [!UICONTROL Erlebnis] zurückkehrten, wurde nur ein Selektor beibehalten, was zu Änderungen und einer fehlerhaften Bereitstellung von Inhalten führte. Dieses Verhalten unterschied sich von dem der alten Benutzeroberfläche, die beide Änderungen mit unterschiedlichen Standortkennungen korrekt beibehielt. (TGT-52891)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem durch Klicken auf ein hinzugefügtes Angebot in der Leiste [!UICONTROL Änderungen] das Bedienfeld [!UICONTROL Konfiguration] zeitweise angezeigt und ausgeblendet wurde, was die Interaktion mit den Angebotseinstellungen erschwerte. (TGT-53288)
* Es wurde ein Problem behoben, bei dem HTML-Angebote, die zu zielgruppenspezifischen Varianten innerhalb einer Aktivität hinzugefügt wurden, nicht konsistent gespeichert wurden oder im Änderungsabschnitt angezeigt wurden. Nachdem während der Bearbeitung zwischen Audiences gewechselt wurde, waren zuvor angewendete Angebote manchmal verschwunden oder konnten nicht gerendert werden, wodurch die Validierung unterbrochen und die Bereitschaft für Aktivitäten verzögert wurde. (TGT-53440)
* Es wurde ein Problem behoben, bei dem das Kopieren einer Aktivität, die Angebote enthielt, dazu führte, dass in der neuen Aktivität doppelte Angebote erstellt wurden. Dieses Verhalten verursachte unnötige Unübersichtlichkeit und Verwirrung, insbesondere beim Verschieben von Aktivitäten zwischen Arbeitsbereichen. Die Korrektur stellt sicher, dass [!DNL Target] Angebote jetzt korrekt und ohne Duplizierung in den Zielarbeitsbereich kopiert werden, was die Aktivitätsverwaltung optimiert und die Workflow-Effizienz verbessert. (TGT-53454)

+++

**Single Page Applications (SPAs)**

+++Details anzeigen

* Es wurde ein Problem im aktualisierten VEC behoben, das Kunden daran hinderte, Änderungen an [!UICONTROL &#x200B; (Single Page Application] (SPA)-Ansichten anzuwenden. Während Aktivitäten, die in der alten Benutzeroberfläche erstellt wurden, ansichtsspezifisches Targeting unterstützten, konnte die neue Benutzeroberfläche Änderungen an diesen Ansichten nicht erkennen oder zulassen, wobei die Steuerelemente zum Umschalten der Ansicht deaktiviert wurden. (TGT-52556)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem Änderungen an Erlebnissen, die in [!UICONTROL Visual Experience Composer] vorgenommen wurden, entweder nicht sichtbar waren oder in der Benutzeroberfläche inkonsistent erschienen. (TGT-TGT-53381)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem im Abschnitt [!UICONTROL Inhalt verwalten] kein Alternativtext für Erlebnis-Miniaturansichten angezeigt wurde. Dieses Problem machte es für Benutzende schwierig, Dokumente zu identifizieren, insbesondere wenn Dateinamen lang oder abgeschnitten waren. (TGT-52291)
* Es wurde ein Fehler behoben, bei dem Kundinnen und Kunden beim Konfigurieren von [!UICONTROL Seitenversand]-Regeln in VEC-Aktivitäten auf falsche Validierungsfehler stießen. Insbesondere wurde bei Operatoren wie „ist gleich eines von“ und „ist nicht gleich eines von“ die Auslösung „Ungültige Eingabe für den Operatortyp“ bei der Eingabe von Textwerten ausgelöst, obwohl Text unterstützt werden sollte. (TGT-52629)
* Es wurden mehrere Probleme behoben, die zu inkonsistentem Verhalten im Bedienfeld [!UICONTROL Änderungen] der aktualisierten Benutzeroberfläche führten, wenn Angebote über die Schaltfläche „Angebot auswählen“ ausgewählt wurden. Statt das vorhandene Angebot zu ersetzen, hat die Benutzeroberfläche ein Duplikat hinzugefügt und versucht, mit beiden Angeboten zu interagieren, was zu Konsolenfehlern führte, z. B. `selectorNotFound`. Darüber hinaus wird bei einigen Angeboten nicht die Schaltfläche „Angebot auswählen“ angezeigt, sondern nur bearbeitbare Eigenschaften. (TGT-53321)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem HTML-Code-Änderungen, die während der Aktivitätseinrichtung vorgenommen wurden, nicht auf Variantenseiten beibehalten wurden, obwohl sie für Kontrollgruppen korrekt gespeichert wurden. Trotz mehrfacher Versuche und der Neuerstellung von Tests ohne Seitengruppierungen konnten die Variantenseiten durchgängig keine Änderungen beibehalten, was sich auf die Inhaltsbereitstellung und die QS-Validierung auswirkte. (TGT-53436)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem der Operator „ist gleich eines von“ in Seitenbereitstellungsregeln Eingabewerte nicht akzeptieren konnte. Bei der Konfiguration von Kundenparametern für alle Mboxes führte die Auswahl dieses Operators zu einem Fehler „Ungültige Eingabe“, was die Erstellung von Regeln verhinderte. (TGT-52623)

+++

**Arbeitsbereiche**

+++Details anzeigen

* Der Arbeitsablauf beim Kopieren von Aktivitäten zwischen Arbeitsbereichen wurde verbessert. Das Kopieren von Aktivitäten zwischen Arbeitsbereichen führte aufgrund fehlender Zielgruppen und nicht zugewiesener Eigenschaften zu Synchronisierungsfehlern. Dieses Update führt einen intelligenteren, intuitiveren Workflow ein, der sicherstellt, dass kopierte Aktivitäten ordnungsgemäß konfiguriert und für die Veröffentlichung bereit sind. (TGT-47094)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden aufgrund eines Fehlers in der `copyActivityBatchOperations`-Mutation keine Aktivitäten zwischen Arbeitsbereichen kopieren konnten. Der Versuch, Aktivitäten zu duplizieren, führte zu einem Server-Fehler (500) und einer Null-Antwort-Payload. (TGT-52405)
* Es wurde ein Problem behoben, bei dem Aktivitäten nicht synchronisiert werden konnten, wenn Angebote, auf die in der Konfiguration verwiesen wurde, im ausgewählten Arbeitsbereich nicht zugänglich waren. Dies führte zu Veröffentlichungsfehlern und ließ Aktivitäten in einem fehlgeschlagenen Status zurück. (TGT-52535)
* Fehlerkorrektur - Beim Kopieren von Aktivitäten zwischen Arbeitsbereichen in der aktualisierten [!DNL Target]-Benutzeroberfläche treten jetzt keine Fehler mehr auf. Kunden stießen auf Fehler im Zusammenhang mit dem Zielgruppenzugriff, insbesondere bei Live-Aktivitäten, und auf eine falsche Berechtigungsprüfung, selbst wenn die Benutzenden sowohl in Quell- als auch in Ziel[!UICONTROL Arbeitsbereichen „Genehmigende Person]-Rollen hatten. (TGT-53002)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem das Kopieren von Aktivitäten innerhalb desselben Arbeitsbereichs unnötig die zugehörigen Angebote und Zielgruppen duplizierte. (TGT-53457)
* Es wurde ein Problem behoben, um Fälle zu beheben, in denen Ad-hoc- (anonyme) Zielgruppen nicht korrekt zwischen nicht standardmäßigen Arbeitsbereichen oder von nicht standardmäßigen in standardmäßige Arbeitsbereiche kopiert wurden. Während frühere Aktualisierungen eine ordnungsgemäße Duplizierung für Szenarien mit Standardeinstellungen sowie Szenarien mit identischem Arbeitsbereich sicherstellten, konzentrierte sich diese Verbesserung auf die Beibehaltung kombinierter Zielgruppenkonfigurationen, die mehrere Arbeitsbereiche umfassen. Die Korrektur stellt ein konsistentes Zielgruppenverhalten und eine genaue Zielgruppenbestimmung über alle Arbeitsbereich-Transitionen hinweg sicher. (TGT-53268)

+++

### [!DNL Target Standard/Premium] 25.7.4 (1. August 2025)

Diese Version behebt aktuelle Probleme, die in erster Linie durch komplexe Kundenanpassungen verursacht werden, und umfasst die folgenden Fehlerbehebungen und Verbesserungen:

**Aktivitäten**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem ein Kunde den Fehler „Ungültige Benutzereingabe“ beim Versuch feststellte, eine Live-Aktivität zu speichern, selbst wenn keine Änderungen vorgenommen wurden. Die GraphQL-Antwort zeigt ein doppeltes LocalId-Problem an. (TGT-53329 UND TGT-53373 UND TGT-53195)
* Es wurde ein Problem behoben, das die Erstellung eines Umleitungserlebnisses in der aktualisierten VEC verhinderte. Die Umleitungs-URL wurde ignoriert und stattdessen die Originalseite angezeigt. (TGT-53306)

+++

**Lokalisierung**

+++Details anzeigen

* Fehlerkorrektur - Bei der Lokalisierung im Modal [!UICONTROL Kriterien erstellen] wurde bei der Auswahl der Option „Zwischen folgenden Werten“ in der Dropdown-Liste [!UICONTROL Preisregel auswählen] die Zeichenfolge „An“ im Abschnitt [!UICONTROL Einschlussregeln] nicht lokalisiert. (TGT-49754)
* Es wurde ein Lokalisierungsproblem behoben, bei dem die Zeichenfolge &quot;[!UICONTROL Alle Hostgruppen]&quot; in der Dropdown-Liste [!UICONTROL Umgebung] des Assistenten zur Erstellung von Feeds nicht korrekt lokalisiert wurde. (TGT-46737)

+++

**QA**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem die QS-Umgebung keine Daten über mehrere Registerkarten hinweg laden konnte, wodurch die Oberfläche unbrauchbar wurde. (TGT-53377)
* Fehlerkorrektur - In der QS-Umgebung kann jetzt eine Aktivität erstellt werden. Der Prozess wurde zur Seite [!UICONTROL Aktivitäten] umgeleitet, anstatt erfolgreich abgeschlossen zu werden. (TGT-53328)

+++

**Recommendations**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem der Mauszeiger über den Operanden „Deep-Learning“ beim Erstellen einer Sammlung in [!DNL Recommendations] zum Absturz der Seite führte. (TGT-53305)
* Es wurde ein Problem behoben, bei dem Filtervorschläge in [!UICONTROL Katalogsuche] in der aktualisierten Benutzeroberfläche ungenau waren. (TGT-52007)
* Es wurde ein Problem in der [!DNL Recommendations]-Benutzeroberfläche behoben, bei dem der Operandenfilter bei Verwendung der Operatoren „Wert ist vorhanden“ oder „Wert ist nicht vorhanden“ angezeigt wird, obwohl er ausgeblendet werden sollte. (TGT-53012)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen

* Fehlerkorrektur - Wenn ein(e) Benutzende(r[!UICONTROL &#x200B; beim Bearbeiten einer Automated Personalization]AP)-Aktivität auf [!UICONTROL Fertig] klickt, wird die Seite leer und reagiert nicht mehr. (TGT-53047 und TGT-52993)
* Es wurde ein Problem behoben, bei dem [!UICONTROL &#x200B; Auswahl der Konversionsmetrik „Angezeigte &#x200B;]&quot; unter [!UICONTROL Ziele und Einstellungen] zum Absturz der Seite führte. (TGT-53346, TGT-53343 und TGT-53348)
* Es wurde ein Problem behoben, bei dem die Funktion [!UICONTROL Umleiten an URL] nicht wie erwartet funktioniert - selbst bei gültigen URLs erfolgt keine Umleitung. (TGT-53307)

+++

**Arbeitsbereiche**

+++Details anzeigen

* Fehlerkorrektur - Das Kopieren von Aktivitäten zwischen Arbeitsbereichen führt jetzt nicht mehr zu doppelten „Zielgruppen-Copy“-Einträgen und ID-Konflikten. Zielgruppen werden jetzt mit eindeutigen IDs, Workspace-Kontext und rekursiver Handhabung für kombinierte Zielgruppen kopiert (bis zu 5 Ebenen). (TGT-53081)
* Fehlerkorrektur - Wenn der Arbeitsbereich auf &quot;[!UICONTROL Alle Arbeitsbereiche“ eingestellt ist] führt das Kopieren einer Aktivität, die bereits im Standardarbeitsbereich vorhanden ist, zu einem falschen Fehler:

  „Mindestens eine Eigenschaft sollte für nicht standardmäßige Arbeitsbereiche enthalten sein.“

  Da sich die Kopie im Standardarbeitsbereich befindet, sollte keine -Eigenschaft erforderlich sein. Der Versuch, eine Eigenschaft hinzuzufügen und zu speichern, führt zu einem zweiten Fehler:

  „Ungültige Benutzereingabe“

+++

### [!DNL Target Standard/Premium] 25.7.3 (Freitag, 24. Juli 2025)

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, enthält diese Version die folgenden Fehlerbehebungen und Aktualisierungen:

**Aktivitäten**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem die `buildViews`-Methode in der Builder-Klasse fälschlicherweise auf die Gesamtanzahl der Ansichten `viewMaxLocalId` wurde, anstatt auf die höchste zugewiesene `viewLocalId`. (TGT-53207)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem gelöschte Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten als `Deleted option with ID: X` anstelle ihrer ursprünglichen Namen angezeigt wurden (z. B. `Offer Name [Deleted]` wie in der veralteten Benutzeroberfläche gezeigt). Diese Korrektur stellt eine aussagekräftige Kennzeichnung für gelöschte Angebote wieder her, verbessert die Klarheit und macht das Reporting genauer und benutzerfreundlicher. (TGT-52921)
* Es wurde ein Problem behoben, bei dem einige Aktivitäten, die vom [!DNL Target]-Frontend zu [!DNL Target] Central migriert wurden, aufgrund eines zuvor behobenen Synchronisierungsfehlers inkonsistente Metrikkonfigurationen hatten. Insbesondere bei Aktivitäten, die ursprünglich eine Konversionsmetrik verwendet haben und später auf eine Analytics-basierte Metrik aktualisiert wurden, wurden veraltete Werte in den `primaryMetricType`- und `successCriteria` beibehalten. (TGT-52643)
* Es wurde ein Problem behoben, bei dem der gesamte Inhalt einer QS-Vorschauseite bearbeitbar wurde, da das `contentEditable`-Attribut unbeabsichtigt in HTML-Änderungen aufgenommen wurde. Dadurch konnten Benutzer auf einen beliebigen Text auf der Seite klicken und ihn bearbeiten, was zu Layout-Problemen und Verwirrung während der Qualitätssicherung führen konnte. (TGT-53247)
* Es wurde ein Problem behoben, bei dem das Verschieben einer Änderung von [!DNL Page Load] in [!UICONTROL Ansicht] dazu führte, dass die Änderung dupliziert wurde, während sie [!UICONTROL Seitenladen“ &#x200B;] und auch in der [!UICONTROL Ansicht] angezeigt wurde. Außerdem würde das Entfernen der Änderung aus der [!UICONTROL Ansicht] fälschlicherweise auch aus [!UICONTROL Seitenladen] entfernen. (TGT-53270)

+++

**APIs**

+++Details anzeigen

* Es wurde ein Problem in der Backend-Persistenzschicht behoben, bei dem gelöschte Optionen korrekt gespeichert wurden, aber über vorhandene API-Endpunkte nicht zugänglich waren. Daher konnten Frontend-Anwendungen keine aussagekräftigen Namen für gelöschte Optionen abrufen, was sich auf historische Berichtsansichten auswirkte. Durch diese Fehlerbehebung wird sichergestellt, dass erhaltene gelöschte Optionsdaten jetzt ordnungsgemäß in der Benutzeroberfläche angezeigt werden können. (TGT-52973)
* Es wurde ein neuer Migrationsendpunkt implementiert, um die Übertragung gelöschter Aktivitätsoptionen von JCR-basierten Aktivitäten zu [!DNL Target] Central zu unterstützen. Diese Funktion ermöglicht eine systemübergreifende konsistente Verfolgung und Berichterstellung. Diese Funktion stellt sicher, dass gelöschte Optionen im [!DNL Target] Frontend und Backend beibehalten und synchronisiert werden, was die historische Berichterstellung und Datenintegrität verbessert. (TGT-53217)
* Es wurde ein neuer API-Endpunkt eingeführt, mit dem Benutzer zuvor gelöschte Aktivitätsoptionen aus einer sekundären Datenbank wiederherstellen können. Diese Funktion nutzt die vorhandene Infrastruktur, die von den Klassen `RemovedCampaignElements` und `RemovedOptionInfo` bereitgestellt wird, um eine nahtlose Wiedereingliederung gelöschter Optionen in aktive Aktivitäten sicherzustellen. (TGT-52903)
* Es wurde ein Problem behoben, bei dem [!DNL Recommendations] Aktivitäten, die Metriknamen mit mehr als 25 Zeichen enthielten, aufgrund von API-Einschränkungen nicht geöffnet oder bearbeitet werden konnten. Diese Fehlerbehebung stellt die Kompatibilität mit Metriknamen sicher, die die Zeichenbeschränkung überschreiten, und stellt den vollständigen Zugriff auf die betroffenen Aktivitäten wieder her. (TGT-52839)

+++

**Formularbasierter Experience Composer**

+++Details anzeigen

* Fehlerkorrektur - Der Editor stürzt in [!UICONTROL Form-Based Experience Composer] nach dem Klicken auf das Symbol **[!UICONTROL Inhalt verwalten]** (Symbol ![Inhalt verwalten](/help/main/assets/icons/Experience.svg) ) beim Erstellen oder Bearbeiten einer [!UICONTROL Automated Personalization] (AP) ab. (TGT-53047)

+++

**Recommendations**

+++Details anzeigen

* Es wurde ein Problem behoben[!UICONTROL &#x200B; das verhinderte, &#x200B;] zusätzliche Ergebnisse beim Scrollen zum unteren Rand der Liste geladen wurden, wodurch das Verhalten der veralteten Benutzeroberfläche wiederhergestellt wurde. (TGT-53088)
* Es wurde ein Problem behoben, durch das das Löschen von Elementen [!UICONTROL &#x200B; Dialogfeld &#x200B;]Kriteriendetails“ blockiert wurde. (TGT-53245)
* Es wurde ein Problem behoben, das das Öffnen oder Interagieren mit Produkten ohne Namen verhinderte. Dieses Problem trat auf, wenn Umgebungen ausgewählt wurden, die unbenannte Ergebnisse zurückgaben, wodurch der Zugriff auf Produktdetails verhindert wurde. (TGT-53007)
* Ein Problem wurde behoben, das dazu führte[!UICONTROL &#x200B; dass die Seite „Katalogsuche] abstürzte und bei der Auswahl bestimmter Produkte einen leeren Bildschirm anzeigte. (TGT-53087)
* Es wurde ein Problem behoben, bei dem Benutzer die [!DNL Recommendation]-Aktivität site_cart_z1 in der [!DNL Target]-Benutzeroberfläche nicht bearbeiten konnten. Beim Versuch, die Aktivität zu öffnen, wurde ein Fehler auf der Seite [!UICONTROL Übersicht] ausgelöst, wodurch der Zugriff auf den Editor blockiert wurde. (TGT-53221)

+++

**Berichterstellung**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem das Sandbox-Feld in der Aktivitätsdatenbank beim Wechsel der Berichtsquelle von [!DNL Customer Journey Analytics] oder [!DNL Analytics] zu [!DNL Target] nicht gelöscht wurde. Zuvor hat die Benutzeroberfläche Sandbox: null korrekt gesendet, aber das Backend hat diesen Wert ignoriert, sodass veraltete Sandbox-Daten beibehalten wurden. Das Backend löscht jetzt das Sandbox-Feld ordnungsgemäß, wenn null empfangen wird. (TGT-52798)
* Die Persistenzschicht für gelöschte Optionen im Target-Backend wurde erneut implementiert, um präzise Verlaufsberichte in [!UICONTROL Automated Personalization] (AP)-Aktivitäten zu unterstützen. Zuvor ging beim Löschen einer Option ihr Name verloren, sodass es schwierig war, vergangene Leistungsdaten zu interpretieren.

  **Wichtige Verbesserungen**:

  * Gelöschte Optionen werden jetzt mithilfe der vorhandenen `RemovedCampaignElements` und `RemovedOptionInfo` Infrastruktur nachverfolgt.
  * Wenn eine Option aus einer AP-Aktivität entfernt wird, bleiben ihre Metadaten (z. B. ID und Name) erhalten.
  * Die Reporting-Benutzeroberfläche kann jetzt den ursprünglichen Optionsnamen (z. B. `Option Name [Deleted]`) neben historischen Metriken anzeigen, was die Klarheit und Benutzerfreundlichkeit verbessert.

  Diese Aktualisierung gewährleistet konsistente und aussagekräftige Berichte, auch nachdem Optionen aus einer Aktivität entfernt wurden. (TGT-52986)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen

* Fehlerkorrektur - Das Anwenden einer Änderung an einer Ansicht in VEC führt jetzt nicht mehr zu einer Duplizierung und löst den Fehler „Ungültige Benutzereingabe“ aus. (TGT-52886)
* Fehlerkorrektur: Bei der Funktion [!UICONTROL Rückgängig] für die Optionen [!UICONTROL Einfügen vor] und [!UICONTROL Einfügen nach] beim Konfigurieren von Bildangeboten in Visual Experience Composer tritt jetzt kein Fehler mehr auf.

  Zuvor führte das Rückgängigmachen einer Aktion [!UICONTROL Einfügen vor] oder [!UICONTROL Einfügen nach] für Bildangebote zu inkonsistentem Verhalten oder dem Versagen, die Änderung ordnungsgemäß rückgängig zu machen, insbesondere bei Aktivitäten, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. Dieses Problem wurde behoben, um sicherzustellen, dass die Rückgängigmachungen für diese Änderungen jetzt zuverlässig funktionieren. (TGT-52809)

* Es wurde ein Problem behoben, bei dem das `contentEditable`-Attribut versehentlich auf „true“ gesetzt wurde und im gespeicherten HTML-Inhalt beibehalten wurde. Dieses Update sorgt für eine sauberere, erwartete HTML-Ausgabe ohne unbeabsichtigtes Bearbeitungsverhalten. (TGT-52319)
* Um einen dauerhaften Verlust gelöschter Optionen zu verhindern und ein konsistentes Verhalten aller Services sicherzustellen, wurde für Optionen in der Benutzeroberfläche und zugehörige Microservices eine Funktion zum weichen Löschen implementiert.

  **Wichtige**:

  * Optionen werden nicht mehr dauerhaft gelöscht. Stattdessen werden sie im Parameter-XML-Objekt mit einem neuen Flag für „Gelöscht: true“ gekennzeichnet.
  * Dieses Flag wird nur von der aktualisierten [!DNL Target]-Benutzeroberfläche verwendet, um gelöschte Optionen vom Rendering auszuschließen und zu verhindern, dass sie an Edge-Services gesendet werden.
  * Gelöschte Optionen bleiben während der Bearbeitung Teil der Aktivitäts-Payload und stellen die Rückverfolgbarkeit sicher, während die Bereitstellung nicht vorhandener Optionen an Kunden vermieden wird.

  Diese Aktualisierung verbessert die Datenintegrität und entspricht den Best Practices für die Verwaltung von Löschungen in verteilten Systemen. (TGT-52726)

+++

**Arbeitsbereiche**

+++Details anzeigen

* Fehlerkorrektur - Beim Kopieren einer Aktivität aus einem nicht standardmäßigen in einen standardmäßigen Arbeitsbereich oder zwischen nicht standardmäßigen Arbeitsbereichen tritt jetzt kein Fehler mehr auf. Angebote werden jetzt mit verbessertem Tracking und Benennung dupliziert, um Konflikte zu vermeiden.

  **Wichtige Verbesserungen**:
  * Angebote werden im Zielarbeitsbereich mit aktualisierten IDs und Metadaten neu erstellt.
  * Kopierte Angebote werden im folgenden Format umbenannt: „Angebotsname kopieren“ plus einer zufälligen Zahl oder einem Zeitstempel, um die Eindeutigkeit sicherzustellen.
  * Das System aktualisiert den Angebots- und Aktivitätsstatus entsprechend den neuen IDs.
  * Diese Funktion verhindert Fehler, die durch mehrere identische „Angebotskopie“-Namen während wiederholter Kopieraktionen verursacht werden.
  * Angebote werden möglicherweise nicht sofort in der Angebotsliste des Zielarbeitsbereichs angezeigt, werden aber ordnungsgemäß verarbeitet und angezeigt.

  Diese Aktualisierung verbessert die Zuverlässigkeit und Rückverfolgbarkeit bei der Verwaltung von Angeboten über mehrere Arbeitsbereiche hinweg. (TGT-53080)

+++

### [!DNL Target Standard/Premium] 25.7.2 (Samstag, 18. Juli 2025)

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, enthält diese Version die folgenden Fehlerbehebungen und Aktualisierungen:

**Aktivitäten**

+++Details anzeigen

* Es wurde eine zusätzliche Bestätigungswarnung hinzugefügt, die beim Abbrechen von Aktivitätsbearbeitungen mit nicht gespeicherten Änderungen erscheint: „Möchten Sie diese Aktivität wirklich speichern? Wenn Sie nicht speichern, gehen alle Ihre Änderungen verloren.“ Diese Meldung hilft, einen versehentlichen Datenverlust zu verhindern. (TGT-52865)
* Alte Funktionalität auf dem Schieberegler [!UICONTROL Priorität] in [!UICONTROL Ziele und Einstellungen] wiederhergestellt, sodass Kundinnen und Kunden einen numerischen Wert direkt eingeben können, wie in der alten Benutzeroberfläche unterstützt. (TGT-53185 und TGT-53219)

+++

**Zielgruppen**

+++Details anzeigen

* Ein Problem wurde behoben, das dazu führte, dass Aktivitäten mit benutzerdefinierten Zielgruppen nicht gespeichert oder bearbeitet werden konnten. Kunden erhalten die Fehlermeldung „Wir können Ihre Anfrage nicht abschließen. Bitte kontaktieren Sie [!DNL Adobe Client Care], wenn das Problem weiterhin besteht.“ beim Versuch, Änderungen an bestimmten Aktivitäten zu speichern oder sogar ohne Änderungen zu speichern. (TGT-53189)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem Kunden Berichte für bestimmte Aktivitäten auf der Seite [!UICONTROL Ziele und Einstellungen] angezeigt haben. Der Link [!UICONTROL In Analytics anzeigen] verweist nun fälschlicherweise auf die QS-Umgebung und nicht auf die Produktionsumgebung. (TGT-53163)

+++

**[!UICONTROL Erlebnisse] und [!UICONTROL Angebote]**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem das Aufrufen von `triggerView` über benutzerdefinierten Code eine Endlosschleife verursachte. (TGT-52885)
* Es wurde ein Problem behoben, das zu Diskrepanzen zwischen den für -Aktivitäten definierten `LocalIds` und den in Erlebnisdefinitionen verwendeten `LocalIds` führte. (TGT-52669)
* Es wurde ein Problem behoben, bei dem Metriknamen auf der Seite [!UICONTROL Übersicht] der Aktivität fehlten und nur „Angebot“ anstelle des richtigen Metriknamens angezeigt wurde. (TGT-53054)

+++

**Formularbasierter Experience Composer**

+++Details anzeigen

* Fehlerkorrektur - Im [!UICONTROL Formular-basierten Experience Composer] wird jetzt die Fehlermeldung „Eigenschaften von nicht definierten Inhalten können nicht gelesen werden (Map wird gelesen)“ angezeigt, das Speichern von Aktivitäten verhindert wurde. (TGT-53145)

+++

**Recommendations**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem durch Klicken auf [!UICONTROL Katalogsuche] der Fehler „Produktdetails konnten nicht abgerufen werden“ angezeigt und ein Modal ohne eine Option zum Schließen geöffnet wurde. (TGT-53082)
* Es wurde ein Problem behoben[&#x200B; bei dem &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md)Recommendations als Angebote“ in [!UICONTROL A/B-Test]-Aktivitäten beim Ändern von Sammlungen oder Promotions nicht korrekt aktualisiert wurden. (TGT-52884)
* Es wurde ein Problem in der Produktionsumgebung behoben, bei dem durch Klicken auf eine Entität in der aktualisierten Benutzeroberfläche der Fehler angezeigt wurde: „Produktdetails konnten nicht abgerufen werden. Bitte [!DNL Adobe Client Care] kontaktieren, wenn das Problem weiterhin besteht.“ (TGT-53071)

+++

**Berichte**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem das Speichern von Auftragsdetails in einer CSV-Datei zu einer leeren Datei führte. (TGT-52225)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* Es wurde ein Problem auf der Seite [!UICONTROL Ziele und Einstellungen] behoben, bei dem in mehreren Erlebnissen verwendete Selektoren nicht konsistent als ausgewählt markiert wurden. (TGT-53062)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten verhinderte und die Fehlermeldung „Eigenschaften von nicht definierten Inhalten können nicht gelesen werden (Lesen von „Zuordnung„)“ auslöste. (TGT-53161)

+++

**Arbeitsbereiche**

+++Details anzeigen

* Verbesserte Handhabung von Ad-hoc-Angeboten beim Wechsel von Arbeitsbereichen.
  * Beim Wechsel vom Standardarbeitsbereich zu einem nicht standardmäßigen Arbeitsbereich (oder zwischen nicht standardmäßigen Arbeitsbereichen) werden Ad-hoc-Angebote jetzt korrekt kopiert. Bei der Initialisierung wird der Workspace-Kontext aktualisiert und dem Angebot wird eine neue ID zugewiesen, um Eindeutigkeit sicherzustellen.
  * Es treten keine Änderungen auf, wenn Sie im selben Arbeitsbereich bleiben. (TGT-53079)
* Es wurde ein Problem behoben, das Kunden daran hinderte[&#x200B; Aktivitäten zwischen verschiedenen Arbeitsbereichen zu &#x200B;](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6). (TGT-52753 und TGT-47094)
* Fehlerkorrektur - Beim Ändern von Eigenschaften zwischen Arbeitsbereichen tritt jetzt kein Fehler mehr auf.
  * Wenn Sie zwischen dem Standardarbeitsbereich und einem nicht standardmäßigen Arbeitsbereich wechseln und die aktuelle Eigenschaft im Zielarbeitsbereich vorhanden ist, wird die Eigenschaft beibehalten.
  * Wenn in der [!UICONTROL Eigenschaften]-Liste ein Warnhinweis angezeigt wird (der wahrscheinlich darauf hinweist, dass einige Eigenschaften möglicherweise nicht kompatibel sind) und der Kunde auf [!UICONTROL Hinzufügen] oder [!UICONTROL Entfernen] klickt und dann auf [!UICONTROL Speichern], werden alle Eigenschaften entfernt, die sich nicht im Zielarbeitsbereich befinden. Wenn der Kunde auf [!UICONTROL Abbrechen] klickt, bleiben alle Eigenschaften erhalten, auch wenn sie nicht im Zielarbeitsbereich vorhanden sind. (TGT-47094)
  * Wenn Sie im selben Arbeitsbereich bleiben oder von einem nicht standardmäßigen Arbeitsbereich zum Standardarbeitsbereich oder einem anderen Arbeitsbereich wechseln, bleibt alles unverändert. (TGT-53078)
* Die Validierungslogik der Entität wurde aktualisiert, um den ursprünglichen Arbeitsbereichskontext der Aktivität zu berücksichtigen. Entitäten wie [!UICONTROL Experience Fragments] (XFs) werden jetzt basierend auf dem Arbeitsbereich validiert, in dem die Aktivität ursprünglich erstellt wurde. Wenn beispielsweise eine XF im Standardarbeitsbereich vorhanden ist und die Aktivität von Arbeitsbereich X in Arbeitsbereich Y kopiert wird, ist die Validierung weiterhin erfolgreich, solange die XF im ursprünglichen (standardmäßigen) Arbeitsbereich gültig ist. (TGT-53196)
* Verbesserte Unterstützung für das Kopieren von Ad-hoc-Zielgruppen während der Aktivitätsduplizierung.
  * Ad-hoc-Zielgruppen, einschließlich Metriken, Berichterstellung, Seiten- und Nur-Aktivität-Typen, werden jetzt in den folgenden Szenarien automatisch kopiert:
    * Beim Kopieren einer Aktivität aus dem Standardarbeitsbereich in einen nicht standardmäßigen Arbeitsbereich.
    * Beim Kopieren einer Aktivität innerhalb desselben Arbeitsbereichs. (TGT-53197)

+++

### [!DNL Target Standard/Premium] 25.7.1 (Samstag, 11. Juli 2025)

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, enthält diese Version die folgenden Fehlerbehebungen und Aktualisierungen:

**Aktivitäten**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem die [!UICONTROL Aktivitäts-QA]-URL einen unnötigen Abfrageparameter enthielt: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* Es wurde ein Problem behoben, bei dem Vorschau-URLs fälschlicherweise zusätzliche Zielgruppen enthielten, die über die vom Benutzer explizit eingegebene hinausgingen. Dieses Verhalten wurde korrigiert, um sicherzustellen, dass beim Generieren eines QA- oder Vorschau-Links nur die angegebene Zielgruppe angewendet wird. (TGT-52912)
* Ein Problem wurde behoben, das dazu führte, dass Benutzer [!UICONTROL &#x200B; Aktivitäten für Automatisches Targeting &#x200B;]AT) nicht erstellen konnten, wenn [!UICONTROL Automatische Zuordnung] (AA) bei der Einrichtung der Traffic-Zuordnung zuerst ausgewählt wurde. Dieses Problem führte zu einem Backend-Validierungsfehler und verhindert, dass die Aktivität gespeichert wird. (TGT-53096)

+++

**Zielgruppen**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem Benutzende mit der [!UICONTROL Genehmiger]-Rolle Zielgruppenverfeinerungen nur für Aktivitäten hinzufügen oder speichern konnten. Der Versuch, dies zu tun, führte zu einem 403-Fehler (Forbidden) und gab an, dass die Berechtigung &quot;[editor]&quot; erforderlich war, obwohl der Benutzer über ausreichende Berechtigungen zum Genehmigen und Verwalten von Aktivitäten verfügte. (TGT-52984)
* Es wurde ein Problem behoben, bei dem eine aktivitätsspezifische Zielgruppe mithilfe der Option [!UICONTROL Zielgruppenverfeinerung entfernen] nicht mehr in der Zielgruppenliste zur erneuten Auswahl innerhalb derselben Aktivität angezeigt wird. Dieses Verhalten verhinderte, dass Benutzer dieselbe Zielgruppe erneut hinzufügen konnten, es sei denn, sie wurde von Grund auf neu erstellt. (TGT-52979)
* Es wurde ein Problem behoben, bei dem Zielgruppenverfeinerungen nur für Aktivitäten sofort aus der Benutzeroberfläche verschwanden, nachdem sie von einem Speicherort entfernt wurden, noch bevor die Aktivität gespeichert wurde. Dieses Verhalten stand im Widerspruch zu den erwarteten Funktionen und der QuickInfo-Anleitung, in der es heißt: „Alle nicht verwendeten Zielgruppen aus dieser Bibliothek werden gelöscht, sobald die Aktivität gespeichert wurde.“ (TGT-52982)
* Fehlerkorrektur - Jetzt wird nicht mehr versucht, einer Aktivität eine andere Zielgruppe als [!UICONTROL Alle Besucher] zuzuweisen. Beim Speichern wird die folgende Fehlermeldung angezeigt: „Wir können Ihre Anfrage nicht abschließen. Bitte den [!UICONTROL Adobe-Kundendienst kontaktieren] wenn das Problem weiterhin besteht.“ (TGT-53008)
* Fehlerkorrektur - Das Speichern einer Aktivität nach dem Erstellen und Zuweisen einer neuen Zielgruppe im Aktivitätseditor wird jetzt problemlos möglich sein. Die folgende Fehlermeldung wurde angezeigt: „Wir können Ihre Anfrage nicht abschließen. Bitte den [!UICONTROL Adobe-Kundendienst kontaktieren] wenn das Problem weiterhin besteht.“ (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem das Kopieren einer vorhandenen Aktivität und das Ändern der Berichtsquelle in [!DNL Adobe Analytics] (A4T) zu einem Fehler „Ungültige Benutzereingabe“ führte. Der Fehler wurde ausgelöst, wenn bestimmte Metrikaktionen, die mit [!DNL Analytics] Reporting nicht kompatibel sind, wie `restart_same_experience`, `restart_random_experience` und `restart_new_experience`, von der ursprünglichen Aktivität beibehalten wurden. (TGT-52900)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine Aktivität zu erstellen oder zu speichern, wenn sie [!DNL Adobe Analytics] (A4T) als Berichtsquelle im Schritt [!UICONTROL Ziele und Einstellungen] auswählten. Das Problem trat speziell bei der Auswahl [!UICONTROL &#x200B; Metrik „Benutzerspezifisches Ereignis] auf (z. B. „Benutzerspezifisches Ereignis 16„), was zu folgendem Fehler führte: „Ungültige Benutzereingabe“. (TGT-52910)
* Es wurde ein Problem behoben, bei dem Benutzende durch Klicken auf [!UICONTROL &#x200B; Link „In Analytics anzeigen] auf die Homepage anstelle des vorgesehenen [!DNL Analytics]-Dashboards umgeleitet wurden. (TGT-53092 und TGT-53093)
  <!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* Es wurde ein Problem behoben, das auftrat, wenn eine [!DNL Recommendations] Aktivität in der aktualisierten [!UICONTROL Übersicht]-Benutzeroberfläche angezeigt wurde und der Abschnitt [!UICONTROL Ziele und Einstellungen] nicht geladen, wenn [!DNL Adobe Analytics] (A4T) als Berichtsquelle ausgewählt wurde. Die folgende Fehlermeldung wurde angezeigt: „Irgendetwas ist schiefgelaufen. Wir können Ihre Anfrage nicht bearbeiten. Wenden Sie sich an den Kundendienst von Adobe, wenn das Problem weiterhin besteht.“ (TGT-52999)

+++

**[!UICONTROL Erlebnisse] und [!UICONTROL Angebote]**

+++Details anzeigen
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem die Funktion &#x200B;]Inhalt verwalten“ den Status eines Speicherorts nicht ordnungsgemäß validierte, nachdem alle Inhaltsoptionen entfernt wurden. Dieses Problem kann zu inkonsistentem Verhalten oder Fehlern beim Speichern oder Fortsetzen der Aktivitätskonfiguration führen. (TGT-52801)
* Es wurde ein Problem behoben, bei dem Benutzende auf den Fehler „Ungültige Eingabe“ stießen, wenn eine neue Seite hinzugefügt und bestimmte Elemente in verschiedenen Erlebnissen gelöscht wurden. Der Fehler wird durch doppelte `LocalIds` ausgelöst, die während der Elementbearbeitung generiert werden, insbesondere beim Wechseln zwischen Erlebnissen und beim Ändern freigegebener Seitenstrukturen. (TGT-52720)
* Es wurde ein Problem behoben, bei dem die Verwendung [!UICONTROL &#x200B; Funktion &#x200B;]Ad-hoc-Angebot generieren“ dazu führte, dass undefinierte Positionen im Bedienfeld [!UICONTROL Inhalt verwalten] angezeigt wurden. (TGT-53076 und TGT-53070)
* Das Verhalten für den Kunden klargestellt, bei dem Änderungen, die mithilfe eines HTML-Angebots vorgenommen wurden, möglicherweise fehlen, wenn der Kunde vom Schritt [!UICONTROL Targeting] zurück zu [!UICONTROL Erlebnisse] navigiert. Für diesen Kunden generierte die betroffene Website dynamisch mehrere DOM-Selektoren, die sich mit jedem Laden der Seite änderten. Daher kann der ursprünglich für die Änderung verwendete Selektor beim erneuten Öffnen des Editors nicht gefunden werden, was dazu führt, dass die Änderung fehlt oder ungültig ist. Dieses Szenario funktioniert wie vorgesehen. Um sicherzustellen, dass Änderungen visuell im Editor bestehen bleiben, wird empfohlen, dass Clients stabile, konsistente Selektoren verwenden, die sich nicht über Seitenneuladungen hinweg ändern. (TGT-52874)
* Es wurde ein Problem behoben, bei dem der Versuch, ein Angebot zu löschen oder zu deaktivieren, das Teil eines ausgeschlossenen Erlebnisses war, den Fehler „Ungültige Benutzereingabe“ auslöste. Dieses Problem trat auf, obwohl das Angebot in den eingeschlossenen Erlebnissen nicht aktiv verwendet wurde. (TGT-52917)

+++

**Formularbasierter Experience Composer**

+++Details anzeigen

* Es wurde ein Problem in formularbasierten Aktivitäten behoben, bei dem das Duplizieren eines Erlebnisses und das Bearbeiten des benutzerdefinierten Codes in einem der duplizierten Erlebnisse diese Änderungen unbeabsichtigt auf alle duplizierten Erlebnisse anwenden würden. Jedes Erlebnis behält nun nach der Duplizierung seinen eigenen benutzerdefinierten Code unabhängig bei. (TGT-51600)

+++

**Lokalisierung**

+++Details anzeigen

* Aktualisierte Lokalisierungszeichenfolgen in der neuen Benutzeroberfläche für Französisch (fr_FR), Deutsch (de_DE), Italienisch (it_IT), Koreanisch (ko_KO) und vereinfachtes Chinesisch (zh_CN).

+++

**[!DNL Recommendations]**

+++Details anzeigen

* Ein neuer [!DNL Recommendations]-Feed wurde hinzugefügt [Status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partieller Import fehlgeschlagen]. (KB-2215)
* Fehlerkorrektur - Der Workflow zum Erstellen von Aktivitäten beim Hinzufügen von [!DNL Recommendations] mit [!UICONTROL Promotions] funktioniert jetzt fehlerfrei. Wenn Benutzende &quot;[!UICONTROL Nach Attribut weiterleiten] ausgewählt und eine Filterregel hinzugefügt haben (z. B. [!UICONTROL Parameterübereinstimmung]), wurden der ausgewählte Regeltyp und die ausgewählten Operandenwerte nach dem Speichern und erneuten Bearbeiten der Aktivität nicht beibehalten. Beim erneuten Öffnen würde sich der Filterregeltyp unerwartet ändern und Operandenwerte fehlen. (TGT-53059)
* Es wurde ein Problem in der [!DNL Recommendations]-Benutzeroberfläche behoben, bei dem jede mit einer einzelnen Regel erstellte Promotion falsch interpretiert und als Promotion-Typ „Liste von Elementen“ angezeigt wurde, unabhängig von der Logik der Regel. (TGT-53063)
* Fehlerkorrektur - Bei der Verwendung der aktualisierten [!UICONTROL Übersicht]Benutzeroberfläche fehlt die Schaltfläche [!UICONTROL Recommendations-Daten herunterladen] für [!UICONTROL Experience Targeting] (XT)-Aktivitäten, die [!DNL Recommendations] enthalten. (TGT-52730 und TGT-52756)
* Zuvor wurde in der Recommendations-Benutzeroberfläche nur die Anzahl der Entitäten angezeigt, die erfolgreich aus einem Feed importiert wurden. Das Backend-Nachrichtenformat umfasst jedoch sowohl die Anzahl der importierten Entitäten als auch die Gesamtzahl der Entitäten im Format `# of entities imported / # of total entities`. Aufgrund dieser Diskrepanz wurde den Benutzenden in der Benutzeroberfläche nur der erste Wert (Anzahl der importierten Daten) angezeigt, was zu Verwirrung führte. Die Benutzeroberfläche zeigt jetzt beide Zahlen an. (TGT-53073)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden eine Filterregel beim Konfigurieren einer [!UICONTROL Nach Attribut &#x200B;]&quot;-Promotion in einer formularbasierten A/B-Aktivität mit Empfehlungen nicht speichern konnten. Nach dem Speichern und erneuten Öffnen der Aktivität fehlte die Filterregel und die Aktivität konnte nicht erfolgreich gespeichert werden. (TGT-53057)

  +++

**Berichte**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem durch Auswahl von [!UICONTROL Auftragsdetails in CSV exportieren] auf der [!UICONTROL Berichte]-Seite eine leere Datei heruntergeladen wurde. Dieses Problem trat auch dann auf, wenn gültige Bestelldaten in der Aktivität vorhanden waren. (TGT-52225)
* Fehlerkorrektur - Jetzt tritt kein Fehler mehr auf, wenn versucht wird, eine Aktivität nach dem Erstellen und Zuweisen einer neuen Reporting-Zielgruppe zu speichern. Die zurückgegebene Fehlermeldung war: „Zugriff verweigert. Um diesen Vorgang auszuführen, sind alle folgenden Berechtigungen erforderlich: [editor]. Dieses Problem trat auf, obwohl der Benutzer Zugriff auf der Ebene der genehmigenden Person hatte. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* Es wurde ein Problem behoben, bei dem die Anwendung einer Änderung auf eine Ansicht dazu führte, dass die Ansicht dupliziert wurde und die Aktivität den Fehler „Ungültige Benutzereingabe“ zurückgab. Durch diese Fehlerbehebung wird sichergestellt, dass Ansichtsänderungen korrekt angewendet werden, ohne dass Duplizierungs- oder Validierungsfehler ausgelöst werden. (TGT-52886)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code fälschlicherweise für das falsche Erlebnis angezeigt wurden. Insbesondere wurden Änderungen, die für ein Erlebnis vorgesehen waren, in einem anderen Erlebnis gezeigt, was zu Verwirrung und einer potenziellen Fehlkonfiguration von Live-Aktivitäten führte. (TGT-52776)
* Ein Problem wurde behoben, das das Bearbeiten oder Speichern benutzerdefinierter Code-Änderungen in der neuen VEC-Benutzeroberfläche verhinderte. Speziell:

  * Nach dem Bearbeiten und Speichern eines benutzerdefinierten Code-Blocks wurden die Änderungen weder in der Benutzeroberfläche noch in der QS-Vorschau angezeigt.
  * In einigen Fällen konnten Änderungen erst gelöscht werden, nachdem die Aktivität geschlossen und erneut geöffnet wurde.
  * Als Problemumgehung mussten Benutzende den Code kopieren, die Änderung löschen und ihn manuell mit den aktualisierten Inhalten neu erstellen. (TGT-53072)

* Es wurde ein Problem behoben, bei dem das Bearbeiten und Speichern von benutzerdefiniertem Code dazu führte[!UICONTROL &#x200B; dass das Bedienfeld &#x200B;]Änderungen“ nicht mehr reagierte. (TGT-53075)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code in Variantenerlebnissen ungewollt im [!UICONTROL Control]-Erlebnis widergespiegelt wurden. Dies führte zu unbeabsichtigten Änderungen im Versandverhalten. Das [!UICONTROL Control]-Erlebnis bleibt jetzt von benutzerdefinierten Code-Bearbeitungen an anderen Erlebnissen isoliert. (TGT-52413)
* Es wurde ein Problem behoben, bei dem Änderungen an einem Erlebnis (z. B. Erlebnis B) versehentlich in ein anderes Erlebnis (Erlebnis A) dupliziert wurden, wenn der Benutzer auf das zweite Erlebnis klickte, bevor der Editor vollständig geladen war. Dieses Verhalten kann auch dazu führen, dass Änderungen verloren gehen, wenn das ursprünglich ausgewählte Erlebnis keine Änderungen aufwies. (TGT-52597)
* Es wurde ein Problem behoben, bei dem Änderungen[!UICONTROL &#x200B; die im Schritt &#x200B;]Änderungen“ der Aktivitätserstellung vorgenommen wurden, nicht konsistent gespeichert wurden. In einigen Fällen wird nach Abschluss aller Schritte und Klicken auf [!UICONTROL Speichern] das benutzerdefinierte Skript, das im Abschnitt [!UICONTROL Änderungen] hinzugefügt wurde, nicht auf der Live-Site widergespiegelt, obwohl keine sichtbaren Fehler während des Speichervorgangs aufgetreten sind. (TGT-52661)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code nicht korrekt gespeichert und unbeabsichtigt in mehreren Erlebnissen innerhalb derselben Aktivität gespiegelt wurden. Darüber hinaus traten beim Öffnen oder Aktualisieren bestimmter Aktivitäten Zugriffsprobleme auf, was zu leeren Bildschirmen führte. Diese Probleme wurden nun behoben, um eine stabile Aktivitätsbearbeitung und eine genaue Isolierung der Erlebnisse sicherzustellen. (TGT-52594)
* Es wurde ein Problem behoben, bei dem Benutzende im [!UICONTROL Durchsuchen-Modus) nicht zu einer anderen URL navigieren &#x200B;]. Tester und Bearbeiter konnten dadurch alternative Seiten innerhalb derselben Aktivitätssitzung nicht validieren oder in der Vorschau anzeigen. (TGT-53052)
* Es wurde ein Problem behoben, bei [!UICONTROL &#x200B; mehrere Instanzen von Visual Experience &#x200B;] (VEC) gleichzeitig während der Erstellung einer Aktivität geöffnet wurden. Dieses Problem trat auf, wenn Benutzende den [!UICONTROL Enhanced Experience Composer] (EEC) deaktiviert und den abschließenden Schrägstrich aus der Website-URL im Schritt [!UICONTROL Seitenbereitstellung] entfernt haben. (TGT-52782)
* Es wurde ein Problem behoben, bei dem die Metrik [!UICONTROL Umsatz] im Schritt [!UICONTROL Ziele und Einstellungen] fälschlicherweise standardmäßig auf [!UICONTROL Umsatz pro Besuch] (RPVISIT) eingestellt wurde, selbst wenn der Benutzer eine andere Metrik ausgewählt hatte.  Das Problem trat beim Reduzieren und erneuten Erweitern des Bedienfelds für die Metrikkonfiguration auf, wodurch der zuvor ausgewählte Wert zurückgesetzt wurde. (TGT-52811 und TGT-52878)
* Fehlerkorrektur - Im Workflow zum Erstellen von Aktivitäten treten jetzt keine Probleme mehr im Zusammenhang mit der Angebotsbenennung und der Inhaltsübersetzung in den Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Multivariate Testing] (MVT) auf:

  Wichtige angesprochene Probleme:

  * Das Erstellen mehrerer HTML-Angebote mit demselben Namen (z. B. „Erlebnis„) hat den Fehler „Doppelte Angebotsnamen sind nicht zulässig“ ausgelöst, aber die Benutzeroberfläche hat nicht klar angegeben, welche Angebote den Konflikt verursacht haben.
  * Beim Umbenennen von Angeboten über das rechte Bedienfeld wurde der Name in der Benutzeroberfläche aktualisiert, die Änderung wurde jedoch nicht auf der Registerkarte [!UICONTROL Inhalt verwalten] oder der Registerkarte [!UICONTROL Angebote] widergespiegelt, was zu persistenten Validierungsfehlern führte.
  * Obwohl der Fehler beim Duplizieren des Namens in MVT-Aktivitäten nach dem Umbenennen nicht fortbestand, konnte die Benutzeroberfläche aktualisierte Angebotsnamen weiterhin nicht konsistent auf allen Registerkarten widerspiegeln. (TGT-52933)

  +++

### [!DNL Target Standard/Premium] 25.6.4 (Samstag, 27. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Die Option [!UICONTROL Neu anordnen] wurde zur aktualisierten Benutzeroberfläche [!UICONTROL Visual Experience Composer] (VEC) hinzugefügt, um sie an die in Legacy-VEC verfügbaren Funktionen anzupassen. (TGT-46957 und TGT-52876)
* Es wurde ein Problem behoben, bei dem Änderungen an Variantenerlebnissen (z. B. Erlebnis B) in einer [!UICONTROL A/B-Test]-Aktivität nicht beibehalten wurden. Nach dem Wechsel zwischen Erlebnissen würden die Änderungen an der Variante verschwinden. Dieses Problem hatte keine Auswirkungen auf das Kontrollerlebnis. (TGT-52664)
* Es wurde ein Problem behoben, bei dem bestimmte Kunden keine Aktivitäten erstellen oder speichern konnten, während andere dieselben Aktionen ohne Problem ausführen konnten. Das Problem war in allen Konten inkonsistent. (TGT-52842)
* Es wurde ein Problem behoben, bei dem Benutzende in der aktualisierten VEC keine Änderungen an das [!UICONTROL Seitenladeereignis) verschieben konnten] eine Funktion, die in der veralteten Benutzeroberfläche vorhanden war. (TGT-52617)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben[!UICONTROL &#x200B; bei dem &#x200B;]Seitenladeereignisse“ beim Erstellen von Änderungen in [!DNL Target] nicht sichtbar waren; Aktualisierungen wurden nur auf Ansichten angewendet. (TGT-52604)
* Ein Problem wurde behoben, das dazu führte, dass einige Aktivitätsänderungen in der aktualisierten VEC nicht korrekt angezeigt wurden. (TGT-52818)
* Fehlerkorrektur - Beim Abrufen von Berichtsdaten für [!UICONTROL Automated Personalization] (AP)-Aktivitäten tritt jetzt keine Nullzeiger-Ausnahme mehr auf. (TGT-52362)
* Es wurde ein Problem behoben, das verhinderte, dass Details auf Angebotsebene in der CSV-Datei für [!UICONTROL Automated Personalization] (AP)-Aktivitäten angezeigt wurden. (TGT-52675)
* Fehlerkorrektur - Beim Anwenden von Änderungen im aktualisierten VEC werden Änderungen zunächst korrekt angezeigt, einschließlich des erwarteten [!UICONTROL Experience Fragment]. Wenn jedoch Erlebnisse gewechselt oder zusätzliche Bearbeitungen vorgenommen werden, können einige Änderungen aufgrund von Problemen mit dem Selektor nicht angewendet werden. (TGT-52679)
* Es wurde ein Problem behoben, bei dem bei Erstellung einer neuen Aktivität durch Klonen einer vorhandenen die Seiten-URLs aus der ursprünglichen Aktivität von den QA-Links in der geklonten Aktivität fälschlicherweise beibehalten wurden. (TGT-52775)
* Es wurde ein Problem behoben, durch das [!UICONTROL On-Device Decisioning] in der aktualisierten VEC nicht verfügbar war. (TGT-52371)
* Ein Problem wurde behoben, das die Bearbeitung einer [!DNL Recommendations] verhinderte. Beim Versuch, über die Target-Benutzeroberfläche auf den VEC zuzugreifen, trat auf der Seite [!UICONTROL Überblick] ein Fehler auf, der alle Änderungen verhinderte. (TGT-52823)
* Es wurde ein Problem behoben, das das Speichern einer [!DNL Recommendations]-Aktivität verhinderte, wenn Erlebnisnamen 50 Zeichen überstiegen. (TGT-52619)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden eine Recommendations -Aktivität nicht speichern konnten, nachdem sie die Kriterien in der neuen Benutzeroberfläche geändert hatten. Das Problem scheint berechtigungsbezogen zu sein und betrifft nicht alle Benutzer mit ähnlichen Rollen. (TGT-52816)
* Es wurde ein Problem behoben, bei dem Benutzende mit [!UICONTROL Editor]-Rolle eine [!DNL Recommendations] Aktivität nicht bearbeiten konnten. Der Versuch, das Design zu ändern und die Aktivität zu speichern, führte zu einem 403-Fehler (Forbidden) und gab an, dass die Berechtigung &quot;[editor]&quot; erforderlich war, obwohl die Benutzerin bzw. der Benutzer diese Rolle bereits im entsprechenden Arbeitsbereich hatte. (TGT-52836)

### [!DNL Target Standard/Premium] 25.6.3 (Samstag, 20. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Fehlerkorrektur - Beim Kopieren einer Aktivität von einem Arbeitsbereich in einen anderen Arbeitsbereich treten jetzt keine Fehler mehr auf, z. B. „Darf nicht null sein“ oder „Irgendetwas ist schiefgelaufen“. (TGT-52474)
* Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem für &#x200B;] Aktivitäten keine Berichte [!UICONTROL Automatisierte Segmente] und wichtige Attribute“ generiert wurden. (TGT-52904)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem die standardmäßige Inhaltsverarbeitung in [!UICONTROL Automated Personalization]-Aktivitäten (AP) nicht mit der veralteten Benutzeroberfläche übereinstimmte. Das System fügt jetzt automatisch eine `optionGroup` mit dem Namen „Standardinhalt“ mit `optionGroupLocalId = 0` hinzu, wenn keine Gruppe explizit hinzugefügt wird. Diese Gruppe umfasst die Standardoption (z. B. `optionLocalId: 0`). Wenn der Standardinhalt entfernt wird, wird auch die entsprechende Optionsgruppe entfernt. (TGT-52651)
* Es wurde ein Problem in [!UICONTROL Multivarianz-Test]-Aktivitäten) behoben, bei dem die Wiederverwendung eines `experienceLocalId` aus zuvor entfernten Erlebnissen fälschlicherweise nicht zulässig war. (TGT-52672)
* Ein Problem wurde behoben, das das Kopieren oder Bearbeiten von Aktivitäten verhinderte, die ein Experience Fragment enthielten. Dadurch wurde der Fehler ausgelöst: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* Es wurde ein Problem behoben, bei dem URLs an Aktivitätspositionen Abfrageparameter aufgrund von ungültigen Zeichen, wie Schrägstrichen (/), nicht anzeigen konnten. (TNT52845)
* Die Validierungsfehlermeldung für [!DNL A/B Test] Aktivitätsaktualisierungen über die Backend-API wurde verbessert. Wenn doppelte Ortsnamen vorhanden sind, wird in der Meldung jetzt deutlich angegeben: „Doppelte Namen sind nicht zulässig“ für `locations.selectors`. (TGT-52589)
* Fehlerkorrektur - Beim Aktualisieren einer Live-Aktivität [!UICONTROL Recommendations] tritt jetzt kein Fehler mehr auf, da in der Payload der Anfrage eine Eigenschaft nicht erkannt wurde. Das System verarbeitet jetzt ordnungsgemäß die „Ungültige JSON. Fehler „Nicht erkannter Eigenschaftsname“. (TGT-52723)
* Fehlerkorrektur - Das Erstellen eines [!DNL Recommendations]-Designs ist jetzt möglich. Durch Klicken auf [!UICONTROL Erstellen] wurde die Meldung „Im Skript sollte mindestens eine Entitätsvariable verwendet werden.“ ausgelöst. (TGT-52395 und TGT-52899)
* Es wurde ein Problem behoben, bei dem das erneute Speichern eines [!DNL Recommendations] Designs ohne Änderungen blockiert wurde. (TGT-52879)
* Fehlerkorrektur - Beim Speichern einer „Recommendations“-Aktivität tritt jetzt kein Backend[!UICONTROL Validierungsfehler mehr &#x200B;]. (TGT-52716)
* Es wurde ein Problem im [!UICONTROL Form-Based Experience Composer] behoben, bei dem der Mauszeiger über eine Mbox mit Sonderzeichen in der Dropdown-Liste [!UICONTROL Speicherort] dazu führte, dass der Editor leer blieb und die Meldung „Fehler beim Ausführen von „querySelector“ für „Element“ auslöste.“ angezeigt. (TGT-52717)
* Verbesserte Genauigkeit des Zufuhrstatus mit einem neuen „PARTIALLY_IMPORTED“-Indikator. Zuvor wurden Feeds als „Erfolg“ markiert, selbst wenn nicht alle Zeilen in einer Datei importiert wurden, was irreführend war. (TGT-52892)
* Fehlerkorrektur - Nach der Migration zu AP V2 `/admin/rest/ui/v1/campaigns` bei bestimmten API-Aufrufen an Client-seitige Fehler zurückgegeben (HTTP 4xx). (TGT-52721)

### [!DNL Target Standard/Premium] 25.6.2 (Freitag, 12. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein [neuer FAQ-Artikel](/help/main/c-intro/updated-ui-faq.md) hinzugefügt, in dem allgemeine Fragen zur aktualisierten [!DNL Target]-Benutzeroberfläche und zu [!UICONTROL Visual Experience Composer] (VEC) behandelt werden.
* Es wurde ein Problem behoben, bei dem die Regel &quot;[!UICONTROL URL - enthält nicht]&quot; im [!UICONTROL Seitenversand] nicht funktionierte, sodass Inhalte auch dann angezeigt werden konnten, wenn sie hätten blockiert werden sollen. (TGT-52754)
* Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem &#x200B;]Seitenversand“ fälschlicherweise die Fehlermeldung „Doppelte Seiten-URLs sind nicht zulässig. (TGT-52765)
* Es wurde ein Problem behoben, bei dem Zielgruppen für [!UICONTROL Seitenbereitstellungs]-URLs, die Experience Fragments enthielten, mit einer fehlerhaften Anfügung von # erstellt wurden. (TGT-52786)
* Es wurde ein Problem behoben, bei dem das Kopieren einer Aktivität und das Bearbeiten der Einstellungen auf [!UICONTROL &#x200B; Seite „Ziele &#x200B;] Einstellungen“ dazu führte, dass die [!DNL Target]-Benutzeroberfläche nicht mehr reagierte. (TGT-52797)
* Fehlerkorrektur - In der aktualisierten [!UICONTROL Visual Experience Composer] (VEC) wird jetzt eine zusätzliche Seite in einer A/B-Test[!UICONTROL Aktivität &#x200B;] dieselbe URL umgeleitet. (TGT-51838)
* Es wurde ein Problem behoben, bei dem Änderungen an Metriken auf der [!UICONTROL Ziele und Einstellungen] beim Bearbeiten einer Aktivität nicht gespeichert wurden. (TGT-52799)
* Es wurde ein Problem behoben, bei dem das Hinzufügen eines neuen Erlebnisses während des Ladevorgangs des Web-Editors dazu führte, dass das neue Erlebnis Inhalte aus dem vorherigen Erlebnis duplizierte. (TGT-51397)
* Es wurde die Möglichkeit wiederhergestellt, benutzerdefinierten Code außerhalb des `<head>`-Tags zu verwenden, eine Funktion, die zuvor in der Legacy-Benutzeroberfläche von Target verfügbar war. (TGT-52304 und TGT-52300)
* Unnötige Validierung bei der Auswahl des Standardarbeitsbereichs während der Aktivitätserstellung wurde entfernt. Die obligatorische Eigenschaftenvalidierung gilt nicht mehr für den Standardarbeitsbereich, bleibt aber für nicht standardmäßige Arbeitsbereiche bestehen. (TGT-52449)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, bei dem `triggerView()` Aufrufe nicht erkannt wurden. (TGT-52575)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, das verhinderte, dass Benutzer Änderungen zu [!UICONTROL Single Page Application]-Ansichten (SPA) hinzufügen konnten. (TGT-52556)
* Ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche wurde behoben, das dazu führte, dass Kundinnen und Kunden keine Angebotsdetails anzeigen konnten. (TGT-52607)
* Es wurde ein Problem behoben, bei dem Aktualisierungen an Angeboten in [!UICONTROL Angebotsbibliothek] nicht in der aktualisierten Version [!UICONTROL Visual Experience Composer] (VEC) widergespiegelt wurden. (TGT-52637)
* Fehlerkorrektur - Der Abschnitt Angebote wird jetzt beim Erstellen einer Aktivität korrekt angezeigt. (TGT-52773)
* Es wurde eine Validierung hinzugefügt, um sicherzustellen, dass alle `optionLocalIds`, auf die in `optionGroups` verwiesen wird, im Optionen-Array vorhanden sind. Ungültige Verweise werden bei der Erstellung der Aktivität automatisch entfernt. (TGT-52687)
* Es wurde ein Problem behoben, bei dem Berichtsgruppen und Ausschlüsse nach dem Hinzufügen eines neuen Angebots nicht beibehalten wurden. (TGT-52728)
* Es wurde ein Problem behoben, bei dem für Aktivitäten ohne [!UICONTROL &#x200B; Schaltfläche &#x200B;]Aktivitäts-QA) eine leere Optionsauswahl angezeigt wurde. (TGT-52733)
* Es wurde ein Problem behoben, bei dem QA-Links Inhalte nicht richtig rendern konnten. (TGT-52718)
* Es wurde ein Problem behoben, bei dem das Ersetzen eines Elements durch ein Experience Fragment die Änderungen in der QS-Umgebung nicht korrekt widerspiegelte. (TGT-52762)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, das zu einem Fehler „Ungültige Eingabe“ führte, wenn Benutzende versuchten, Experience Fragments hinzuzufügen. (TGT-52701)
* Es wurde ein Problem behoben, bei dem das Modal „Zielgruppe bearbeiten“ beim Bearbeiten des Zielgruppen-Targeting im aktualisierten Visual [!UICONTROL &#x200B; Composer (]) leer erschien. (TGT-52749)
* Es wurde eine Nachricht hinzugefügt, die Benutzer darüber informiert, wenn im ausgewählten Arbeitsbereich nicht auf eine Entität zugegriffen werden kann. (TGT-52767)
* Es wurde ein Problem behoben, bei dem die Benutzeroberfläche die manuelle Zuweisung einer Umgebungs-ID zu einem Kriterium nicht zuließ. Stattdessen wird standardmäßig die ID für die Hostgruppe [!UICONTROL Produktkatalogsuche] verwendet. Mit dieser Fehlerbehebung wird sichergestellt, dass Kriterienänderungen jetzt in allen Umgebungen angewendet werden, nicht nur in der Standardumgebung. (TGT-52817)
* Es wurde ein Problem behoben, bei dem die Option [!UICONTROL Recommendations-Daten herunterladen] für [!UICONTROL Experience Targeting)-] mit Recommendations fehlte. (TGT-52730 und TGT-52756)

### [!DNL Target Standard/Premium] 25.6.1 (Samstag, 6. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem QA-Links nicht das richtige Erlebnis für die zugehörige Aktivität lieferten. (TGT-52163 und TGT-52790)
* Fehlerkorrektur - Bei QA-Links fehlt jetzt die zugehörige Zielgruppen-ID. (TGT-52722)
* Es wurde ein Problem behoben, um sicherzustellen, dass Erlebnisse nur bereitgestellt werden, wenn die konfigurierten URL-Bedingungen für die Seitenbereitstellung korrekt erfüllt sind. (TGT-52696)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine [!DNL Recommendations] Design-Vorlage zu erstellen. Der Versuch, eine Vorlage zu erstellen, hat den Fehler ausgelöst: „Im Skript sollte mindestens eine Entitätsvariable verwendet werden.“ (TGT-52395)
* Es wurde ein Problem behoben, das das Speichern von [!DNL Recommendations]-Designs mithilfe von Velocity-Arrays verhinderte. Die Fehlermeldung „Es muss mindestens eine Entitätsvariable im Skript verwendet werden“ wurde fälschlicherweise ausgelöst. (TGT-52734)
* Es wurde ein Problem behoben, bei dem Änderungen in [!UICONTROL Visual Experience Composer] (VEC) nicht zugänglich waren, wenn die Seite für interne Web-Seiten nicht geladen werden konnte. (TGT-52488 UND TGT-52470)
* Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem das Bedienfeld &#x200B;]Änderungen“ in VEC auf kleineren Bildschirmgrößen nicht sichtbar war. (TGT-52470)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem der Wechsel vom [!UICONTROL Durchsuchen]-Modus zurück zum [!UICONTROL Design]-Modus einen Konsolenfehler verursachte und weitere Interaktionen verhinderte. (TGT-52532)
* Es wurde ein Problem in Visual Experience Composer behoben, bei dem durch Klicken auf bestimmte Elemente unbeabsichtigt deren Größe erweitert wurde. (TGT-52497)
* Es wurde ein Problem behoben, bei dem bestimmte Seitenelemente nicht geladen oder in Visual Experience Composer nicht erkannt werden konnten, wodurch Interaktionen wie das Auswählen von Schaltflächen oder Bannern verhindert und die genaue Ereignisverfolgung in -Aktivitäten unterbrochen wurde. (TGT-52663)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Angebote in [!UICONTROL Automated Personalization]-Aktivitäten (AP) zu löschen oder zu entfernen. (TGT-52690)
* Es wurde ein Problem behoben, das zu einem inkonsistenten Verhalten bei der Aktivitätsqualifizierung in mehrseitigen Aktivitäten führte. (TGT-52694)
* Es wurde ein Fehler behoben, der dazu führte, dass auf der Seite [!UICONTROL Übersicht] der Aktivität eine ungültige URL für den [!UICONTROL Speicherort der Aktivität] angezeigt wurde. (TGT-52695)
* Ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche wurde behoben, das dazu führte, dass für Aktivitätsspeicherorte doppelte Einträge angezeigt wurden. (TGT-52693)
* Es wurde ein Problem behoben, das einen `getAudiencesV3` auslöste und Kunden daran hinderte, Aktivitäten zu bearbeiten oder zu kopieren. (TGT-52709)
* Es wurde ein Problem behoben, das beim Hinzufügen von [!UICONTROL Experience Fragments] oder HTML-Angeboten zu einer Aktivität zu einem Fehler „Ungültige Payload“ führte. (TGT-52779 und TGT-52773)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben[!UICONTROL &#x200B; bei dem E-Experience Fragments &#x200B;] einem ungültigen Eingabefehler nicht korrekt angezeigt wurden. (TGT-52701)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Aktivitäten im [!UICONTROL formularbasierten Experience Composer] aufgrund eines ungültigen Benutzerfehlers zu bearbeiten. (TGT-52470)
* Es wurde ein Lokalisierungsproblem in der koreanischen Sprache behoben, bei dem bei früheren Übersetzungen Zeichen außerhalb der mehrsprachigen Basisebene verwendet wurden. Die aktualisierte Übersetzung verwendet geeignete Zeichen, die die beabsichtigte Bedeutung genau vermitteln. (TGT-52508 und TGT-52509)
* Fehlerkorrektur - Bei der Lokalisierung in Koreanisch tritt bei der Auswahl des Start- und Enddatums für eine Aktivität kein Übersetzungsproblem mehr auf, wenn die Übersetzung für „Datum“ inkonsistent ist. (TGT-52510)

### [!DNL Target Standard/Premium] 25.5.4 (29. Mai 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, das das Hinzufügen oder Bearbeiten von URLs im QA-Modus verhinderte. (TGT-51941)
* Unter [!UICONTROL Berichte] > [!UICONTROL Berichteinstellungen] ( ![Berichteinstellungen-Symbol](/help/main/assets/icons/Setting.svg) ) wurde eine Einstellung für den QA-Modus hinzugefügt, um sie an die Funktionalität der veralteten [!DNL Target]-Benutzeroberfläche anzupassen. (TGT-52228 und TGT-52329)
* Es wurde ein Problem behoben, bei dem die formularbasierte Aktivität falsche QA-Links generierte. Die Aktivitäts-URL/-position enthielt am Ende eine unbeabsichtigte „1“, die jetzt entfernt wurde, um eine genaue Verknüpfung sicherzustellen. (TGT-52355 und TGT-52358)
* Es wurde ein Problem behoben, bei dem die formularbasierte Aktivität falsche QA-Links generierte. Die Aktivitäts-URL enthielt eine unbeabsichtigte `http://pid-ppc` am Anfang der URL, die jetzt entfernt wurde, um eine genaue Verknüpfung sicherzustellen. (TGT-52557)
* Es wurde ein Problem behoben, bei dem [!DNL Target] ungültige QA-Links für formularbasierte Aktivitäten generierte. (TGT-52528 und TGT-52603)
* Es wurde ein Problem behoben, bei dem das Speichern einer geänderten Aktivität zwar verarbeitet, aber nie abgeschlossen wurde und in [!DNL Target] keine Fehlermeldung angezeigt wurde. (TGT-52461)
* Es wurde ein Problem behoben, bei dem der aktualisierte [!UICONTROL Visual Experience Composer] (VEC) den `at_property` nicht automatisch erkennen konnte. (TGT-52347)
* Es wurde ein Problem behoben, das dazu führte, dass zwei Änderungen aufgezeichnet wurden, wenn nach dem Wechsel zwischen [!UICONTROL Durchsuchen]- und [!UICONTROL Design]-Modus in VEC bei der Interaktion mit einem Formularelement nur eine Änderung erwartet wurde. (TGT-52455)
* Es wurde ein Problem behoben, das die Auswahl der Einstellung [!UICONTROL Auf ein Element geklickt] in der aktualisierten VEC verhinderte, da ein Fehler angezeigt wurde, der besagte, dass der Selektor ungültig, bereits verwendet oder nicht sichtbar war. (TGT-52467)
* Es wurde ein Problem behoben, bei dem das Hinzufügen eines [!UICONTROL Recommendations-Angebots]-Felds in dem aktualisierten VEC dazu führte, dass doppelte (Ghost-)Felder angezeigt wurden. Beim Wechsel zwischen Erlebnis A und B wurden wiederholt weitere Geisterboxen hinzugefügt. (TGT-52505 und TGT-52519)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Änderungen an einem HTML-Angebot, die über das Menü [!UICONTROL Angebot] vorgenommen wurden, nicht in der zugehörigen Aktivität widergespiegelt wurden und umgekehrt. Dieses Verhalten entspricht nun der veralteten Benutzeroberfläche, in der Aktualisierungen korrekt zwischen dem Menü [!UICONTROL Angebot] und der Aktivität synchronisiert werden. (TGT-52540 und TGT-52541)
* Es wurde ein Problem behoben, bei dem aktuelle Aktualisierungen [!UICONTROL Experience Fragments] in der [!UICONTROL Angebotsbibliothek] nicht widergespiegelt wurden, wenn versucht wurde, sie in einer Aktivität zu verwenden. (TGT-52659)
* Fehlerkorrektur - Die Lokalisierung einer Bestätigungsnachricht in Chinesisch (vereinfacht) funktioniert jetzt fehlerfrei. In der vorherigen Version fehlten Anführungszeichen um den Ortsnamen und die verwendete informelle Sprache, im Gegensatz zum Stil-Handbuch des Kunden. Die aktualisierte Übersetzung verwendet jetzt die richtige Interpunktion und einen formalen Ton. (TGT-52364)

### [!DNL Target Standard/Premium] 25.5.3 (22. Mai 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem die Funktion „Nach Namen suchen[!UICONTROL &#x200B; in der &#x200B;] „Aktivitäten“ bei Abfragen mit mehreren Wörtern nicht korrekt funktionierte. (TGT-52529)
* Es wurde ein Problem behoben, das das Ausschließen von Erlebnissen aus [!UICONTROL Automated Personalization] (AP)-Aktivitäten verhinderte. (TGT-52383)
* Es wurde ein Problem behoben, bei dem die Option [!UICONTROL Enthält] bei der Verwaltung von Inhalten in [!UICONTROL Filterregeln] fehlte. (TGT-52384)
* Fehlerkorrektur - In [!UICONTROL Automated Personalization] (AP)-Aktivitäten gibt es keine Berichte mehr, die speziell darauf ausgerichtet sind, wie Standardangebote verfolgt und anhand von `optionLocalId` aus dem internen System von [!DNL Target] gemeldet werden.
* Es wurde ein Problem behoben, bei dem QA-Links nicht das beabsichtigte Aktivitätserlebnis bereitstellten. (TGT-52163)
* Es wurde ein Problem behoben, bei dem Benutzende mit [!UICONTROL Genehmiger]-Berechtigungen fälschlicherweise daran gehindert wurden, Live-Aktivitäten zu bearbeiten, und die Fehlermeldung „Zugriff verweigert“ erhielten. (TGT-52416)
* Es wurde ein Problem behoben, bei dem Zielgruppenverfeinerungen für bestimmte Aktivitäten in der aktualisierten [!DNL Target]-Benutzeroberfläche nicht angezeigt wurden. (TGT-52057)
* Es wurde ein Fehler behoben, der dazu führte, dass Zielgruppenverfeinerungen und Aktivitäts-Zielgruppen in der aktualisierten Benutzeroberfläche rückgängig gemacht wurden. (TGT-52158)
* Es wurde ein Problem behoben, bei dem das Generieren von Ad-hoc-Angeboten zu doppelten Angeboten führte. (TGT-51938)
* Es wurde ein Problem behoben, durch das Angebotsaktualisierungen blockiert und fälschlicherweise der Fehler „Ungültiger Benutzer“ angezeigt wurde. (TGT-52361)
* Es wurde ein Problem behoben, das das Speichern vorhandener Aktivitäten verhinderte und einen Fehler „Ungültige Benutzereingabe“ auslöste. (TGT-52422)
* Es wurde ein Problem behoben, das die Bearbeitung vorhandener HTML-Angebote blockierte und beim Speichern den Fehler „Ungültige Benutzereingabe“ auslöste, selbst wenn keine Code-Änderungen vorgenommen wurden. (TGT-52351)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Target] das Zeichen &quot;#&quot; in der URL einer Website nicht erkennen konnten. (TGT-52093)
* Es wurde ein Problem behoben, das dazu führte, dass [!DNL Recommendations]-Aktivitäten zum Hinzufügen oder Aktualisieren von Promotions nicht bearbeitet werden konnten, was zu Speicherfehlern und doppelten Promotions führte. (TGT-52343)
* Es wurde ein Problem behoben, das Änderungen an Kriterien oder Designs in [!DNL Recommendations]-Aktivitäten verhinderte, was zu dem Fehler „Ungültige JSON: Nicht erkannter Eigenschaftsname“ führte. (TGT-52375)
* Es wurde ein Problem behoben, bei dem Sequenzkriterien in [!UICONTROL Visual Experience Composer) &#x200B;] VEC für [!DNL Recommendations] Aktivitäten nicht korrekt angezeigt wurden. (TGT-52435)
* Es wurde ein Problem behoben, bei dem Ansichten auf SPA-Seiten bei Verwendung der -[!DNL Adobe Experience Platform Web SDK] nicht korrekt identifiziert wurden. (TGT-52106)
* Es wurde ein Problem behoben, bei dem Details zur On-Device Decisioning (ODS) nicht korrekt gespeichert wurden, obwohl sie in der Payload des Batch-Vorgangs enthalten waren. (TGT-52406)
* Ein `audienceMetadata` Feld wurde zu den Aktivitäten hinzugefügt, sodass es während der Bearbeitung gelesen und aktualisiert werden kann. (TGT-51004)
* Es wurde eine Fehlermeldung hinzugefügt, die Benutzer benachrichtigt, wenn ein Zielgruppen-Zeitrahmen ungültig ist. (TGT52522)
* Die Aktivitätsstruktur wurde aktualisiert, um doppelte Zielgruppen verschiedener Typen zu unterstützen. (TGT-51200)

<!--
### [!DNL Adobe Target] [!DNL AI Assistant] release (May 16, 2025)

We are thrilled to announce the launch of the [!DNL AI Assistant] in [!DNL Adobe Target]! This powerful user interface feature is designed to help you navigate and understand [!DNL Target] concepts with ease. Available across multiple products in [!DNL Adobe Experience Cloud], including [!DNL Target], [!DNL AI Assistant] is here to revolutionize your experience.

[!DNL AI Assistant] in [!UICONTROL Target] is a conversational tool that you can use to accelerate your workflows with [!DNL Experience Platform] applications and services. Use [!DNL AI Assistant] to boost your overall productivity and amplify your understanding of product knowledge

In [!DNL Target], the first phase of [!DNL AI Assistant] provides invaluable product knowledge grounded in [!DNL Experience League] documentation. Whether you are setting up a profile script, troubleshooting errors, or considering an upgrade to the AEP Web SDK, [!DNL AI Assistant] has you covered.

For more information, see [Coworker skills for Adobe Target](/help/main/c-intro/coworker-skills.md).
-->

### [!DNL Target Standard/Premium] 25.5.2 (8. Mai 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* [!DNL Target] Benutzer mit Berechtigungen [!UICONTROL Produktadministrator] und [!UICONTROL Systemadministrator] können jetzt alle Einstellungen auf den Seiten [!UICONTROL Administration] bearbeiten, unabhängig von ihrer Rolle in [!DNL Target]. Benutzende ohne diese Berechtigungen haben schreibgeschützten Zugriff auf diese Einstellungen. Diese Aktualisierung stellt eine strengere Zugriffskontrolle über [Administrationseinstellungen](/help/main/administrating-target/administrating-target.md) sicher. (TGT-48179)
* Es wurde ein Caching-Problem behoben, das das Speichern der Aktivität [Site-Voreinstellungen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) verhinderte. (TGT-52213)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden die Auswahl nach ID und Klasse im Abschnitt [!UICONTROL Site-Voreinstellungen] nach dem Laden der Site in Visual Experience Composer nicht aktivieren konnten. Die [!UICONTROL Site-Voreinstellungen] wird auch nach der Aktivierung automatisch auf Deaktiviert zurückgesetzt. (TGT-52207)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Visual Experience Composer] (VEC) nicht die richtige Seite anzeigte, wenn [Seitenbereitstellungs](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings)-URLs mit einem Schrägstrich (/) endeten. (TGT-52237)
* Ein Problem wurde behoben, das verhinderte, dass benutzerdefinierte Code-Änderungen beim Ändern von Erlebnissen entfernt wurden. (TGT-52240)
* Es wurde ein Problem behoben, bei dem HTML-Änderungen im VEC vorhandene Seitenelemente überlagerten. (TGT-52265)
* Es wurde ein Problem behoben, das die Bearbeitung von benutzerdefiniertem Code in der aktualisierten VEC verhinderte, da der vorhandene benutzerdefinierte Code nicht im Editor sichtbar war. (TGT-52272)
* Es wurde ein Fehler behoben, der die Fehlermeldung „Doppelte Namen sind nicht zulässig“ beim Speichern einer Recommendations-Aktivität verursachte. (TGT-52318)
* Es wurde ein Problem im aktualisierten VEC behoben, das Kunden daran hinderte, Textelemente zu bearbeiten oder Container-Objekte zu entfernen. (TGT-52348)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Customer Journey Analytics] auf einer Aktivitätsseite [!UICONTROL Übersicht] nicht korrekt angezeigt wurden. (TGT-52359)
* Es wurde ein Problem behoben, das verhinderte, dass Berichtsgruppen in [!UICONTROL Automated Personalization]-Aktivitäten (AP) bestehen blieben. (TGT-52368)
* Ein Problem wurde behoben, das das Speichern von Aktivitäten verhinderte, die Offer Decisioning enthalten. (TGT-52390)
* Es wurde ein Problem behoben, bei dem das Standardangebot ausgewählt war, aber andere Angebotsinhalte in den Aktivitäten [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Multivarianz-Test] (MVT) angezeigt wurden. (TGT-52372)
* Die GET-Berechtigungslogik zur Prüfung mit ODER zwischen dem vollständigen Organisationszugriff und dem spezifischen Organisations- + Benutzerzugriff wurde korrigiert. (TGT-52374)
* Es wurde ein Problem behoben, bei dem Zielgruppennamen nicht angezeigt wurden, nachdem eine Zielgruppe für [!UICONTROL Verwaltete Inhalte] und [!UICONTROL Berichterstellungs-Zielgruppen] ausgewählt wurde, obwohl [!UICONTROL Nur ausgewählte anzeigen] aktiviert war. (TGT-52393)

### [!DNL Target Standard/Premium] 25.5.1 (5. Mai 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, das verhinderte, dass Zielgruppenoptimierungen für bestimmte Aktivitäten in der aktualisierten Benutzeroberfläche angezeigt wurden. (TGT-52057)
* Es wurde ein Problem behoben, das die Verwendung kombinierter Zielgruppen in -Aktivitäten verhinderte. (TGT-52346)
* Es wurde ein Problem behoben, das die Erstellung einer neuen Aktivität in einem nicht standardmäßigen Arbeitsbereich mithilfe einer Zielgruppe „Nur Aktivität“ im selben Arbeitsbereich verhinderte. (TGE-52349)
* Es wurde ein Problem behoben, das dazu führte, dass Zielgruppen, die nur für Aktivitäten bestimmt waren, nach dem Erstellen und Auswählen einer neuen Zielgruppe nicht mehr in der aktualisierten Benutzeroberfläche angezeigt wurden. (TGT=52091)
* Fehlerkorrektur - In -Aktivitäten können jetzt doppelte Zielgruppen verwendet werden. (TGT-51200 und TGT-52057)
* Es wurde ein Fehler behoben, der dazu führte, dass Zielgruppenverfeinerungen und Aktivitäts-Zielgruppen in der aktualisierten Benutzeroberfläche rückgängig gemacht wurden. (TGT-52158)
* Es wurde ein Problem behoben, das die Erstellung einer neuen Aktivität aufgrund des Benutzereingabefehlers verhinderte: „Nicht-standardmäßiger Arbeitsbereich ist für diesen Benutzer nicht zulässig.“ (TGT-52267)
* Es wurde ein Problem behoben, das die Anzeige von Angeboten in der aktualisierten Benutzeroberfläche sowohl für standardmäßige als auch für nicht standardmäßige Arbeitsbereiche verhinderte. [!DNL Target] zeigt jetzt Angebote aus beiden Arbeitsbereichen an. (TGT-52339)
* Es wurde ein Problem behoben, bei dem [!DNL Target] Kunden beim Bearbeiten einer Aktivität und Ändern eines geänderten Website-Elements nicht gewarnt haben. (TGT-52100)
* Es wurde ein Problem behoben, bei dem beim Bearbeiten eines Angebots mit Ad-hoc-Angeboten ein neues Angebot erstellt wurde, anstatt das vorhandene zu aktualisieren. (TGT-52135)
* Fehlerkorrektur - Beim Verschieben von Angeboten in Ordner tritt jetzt kein Fehler mehr wegen ungültiger Payload auf. (TGT-52325)
* Es wurde ein Problem behoben, das beim Verschieben von Angeboten in Ordner zu einem Fehler bei der Benutzereingabe führte. (TGT-52296)
* Für jede Aktivität wurde ein `audienceMetadata` Feld hinzugefügt, und es wurde sichergestellt, dass es beim Bearbeiten der Aktivität gelesen und aktualisiert wird. (TGT-51004)

### [!DNL Target Standard/Premium] 25.4.5 (25. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, das zu Diskrepanzen in den Zielgruppenauflistungen zwischen der Seite [!UICONTROL Aktivität]-Einstellungen und der Übersichtsseite [!UICONTROL Reporting] führte. (TGT-52203)
* Es wurde ein Problem behoben, das das Hinzufügen einer neuen Seite zu einer Aktivität aufgrund eines Fehlers bei der ungültigen Benutzereingabe verhinderte. (TGT-52263)
* Es wurde ein Problem behoben, das dazu führte, dass `OptionLocalIDs` fälschlicherweise inkrementiert wurden, wenn die Option unverändert blieb. (TGT-52187)
* Es wurde ein Problem behoben, das dazu führte, dass `location` und `OptionLocalIDs` fälschlicherweise inkrementiert wurden, wenn die Option unverändert blieb. (TGT-52188)
* Es wurde ein Fehler behoben, der dazu führte, dass der Speicherort auf der Seite [!UICONTROL Übersicht] der Aktivität falsch war. (TGT-52182)
* Es wurde ein Problem behoben, bei dem für einen ungültigen Speicherort keine Warnung zu einem ungültigen Selektor angezeigt wurde. (TGT-52110)
* Es wurde ein Problem behoben, sodass heruntergeladene Berichtsdateien die in der Reporting-Benutzeroberfläche vorhandenen Daten korrekt anzeigen. (TGT-52068)
* Fehlerkorrektur: Batch-Vorgänge schlagen nach dem Hinzufügen von Seitenbereitstellungsregeln nicht fehl. (TGT-52097)
* Es wurde ein Fehler behoben, der dazu führte, dass [!DNL Target] alle Abfrageparameter aus der URL der Website kürzte. (TGT-52100)
* Es wurde ein Konsolenfehler behoben, der Kunden daran hinderte, Aktivitäten in der alten und aktualisierten [!DNL Target]-Benutzeroberfläche zu erstellen. (TGT-52181)
* Es wurde ein Problem behoben, durch das Kunden keine neuen Seiten hinzufügen konnten, was zu einem Fehler bei der ungültigen Benutzereingabe führte. (TGT-52258)
* Es wurde ein Problem behoben, das dazu führte, dass Änderungen ausgeblendet wurden, nachdem zusätzliche Seiten hinzugefügt und dann zurück zur Registerkarte [!UICONTROL Erlebnisse] navigiert wurde. (TGT-52264)
* Es wurde ein Problem behoben, durch das Kundinnen und Kunden daran gehindert wurden, die Zielgruppe in einer [!UICONTROL Experience Targeting] (XT)-Aktivität zu ändern. (TGT-52191)
* Fehlerkorrektur - Die Bearbeitung einer XT-Aktivität ist jetzt möglich, da die Benutzeroberflächenregel nicht unterstützt wird. (TGT-52273)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, bei dem Breadcrumbs nicht immer unten im Editor angezeigt wurden, was bei der präzisen Auswahl von Elementen zu Problemen führte. (TGT-52169)
* Es wurde ein Problem behoben, bei dem in [!UICONTROL &#x200B; Dropdown-Liste &#x200B;]Zielgruppe“ aufgrund von Paginierung nicht alle Zielgruppen angezeigt wurden. (TGT-52204)
* Es wurde ein Problem behoben, das zu einer ungültigen Benutzereingabenachricht beim Hinzufügen neuer Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten führte. (TGT-52210)
* Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem Analytics for Target] (A4T) fälschlicherweise als Berichtsquelle ausgewählt wurde, obwohl die Kundin bzw. der Kunde keinen Zugriff auf A4T hatte. (TGT-52226)
* Es wurde ein Problem behoben, das das Speichern einer Aktivität mit der URL[!UICONTROL Metrik „Seite anzeigen] verhinderte. (TGT-52260)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Arbeitsbereiche beim Erstellen von Angeboten innerhalb einer Aktivität auszuwählen. (TGT-52289)
* Es wurde ein Problem behoben, durch das Kunden keine Aktivitäten in allen Arbeitsbereichen erstellen konnten. (TGT-52218)
* Es wurde ein Problem behoben, bei dem Änderungen von einem Erlebnis falsch angezeigt wurden, wenn zu einem anderen Erlebnis gewechselt wurde. (TGT-52184)
* Es wurde ein Problem behoben, bei dem das Standardangebot beim Öffnen der Aktivität nicht korrekt in der [!DNL Target]-Benutzeroberfläche angezeigt wurde. (TGT-52198)

### Aktualisierung der Target-Berechtigungen (22. April 2025)

Diese zukünftige Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Produkt]- und [!UICONTROL Lösungen]-Administratoren die Einstellungen in den [!UICONTROL Administration]-Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die Abschnitte [!UICONTROL Administration].

Weitere Informationen finden Sie unter [Verwaltung von Target](/help/main/administrating-target/start-target.md).

### [!DNL Target Standard/Premium] 25.4.4 (17. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde eine Fehlermeldung hinzugefügt, die Benutzende anleitet, wie doppelte Optionen in einer Aktivität aufgelöst werden können. (TGT-51927)
* Es wurde ein Problem behoben, bei dem `ClickTrack` Selektoren beim Löschen von Seiten oder Erlebnissen mit Umleitungsangeboten nicht entfernt wurden. (TGT-51952)
* Es wurde ein Problem behoben, das dadurch verursacht wurde, dass leere `ClickTrack` zugelassen wurden. [!DNL Target] erfordert jetzt, dass das Auswahlfeld nicht leer sein darf. (TGT-52107)
* Es wurde ein Problem behoben, durch das Metriken fälschlicherweise mit doppelten Namen zugelassen wurden. Metriken erfordern jetzt eindeutige Namen. (TGT-52201)
* Es wurde ein Problem behoben, bei dem Zielgruppendefinitionen beim Bearbeiten des Targeting auf Angebotsebene in [!UICONTROL Automated Personalization] (AP)-Aktivitäten nicht sichtbar waren. (TGT-52148)
* Es wurde ein Problem behoben, das Kunden mit [!UICONTROL Editor]-Rechten daran hinderte, Aktivitäten zu speichern. (TGT-52227)
* `OptionLocalIDs` nicht mehr falsch inkrementiert, wenn die Option unverändert bleibt. (TGT-52139)
* Fehlerkorrektur - Beim Erstellen einer Aktivität wird jetzt nicht mehr die Meldung „Ungültiger `optionLocalIds`&quot; angezeigt. (TGT-52154)
* Die Diskrepanzen zwischen den für eine Aktivität definierten `OptionLocalIDs` und den für die Definition von Erlebnissen definierten Diskrepanzen wurden behoben. (TGT-52215)
* Fehlerkorrektur - Beim Erstellen einer A/B-Aktivität tritt jetzt kein Validierungsfehler mehr auf. (TGT-51923)

### [!DNL Target Standard/Premium] 25.4.3 (11. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der Kundinnen und Kunden daran hinderte, das Popup-Fenster mit Zielgruppeninformationen für bestimmte [!UICONTROL Experience Targeting] (XT)-Aktivitäten zu öffnen. (TGT-52049)
* [!UICONTROL &#x200B; Es wurde ein Problem behoben, bei dem die Zielgruppeneinstellung nach &#x200B;] im Visual Experience Composer (VEC[!UICONTROL &#x200B; auf „Alle Besucher] zurückgesetzt wurde. (TGT-52132)
* Es wurde ein Problem behoben, bei dem Zielgruppenoptimierungen für bestimmte Aktivitäten nicht angezeigt wurden (TGT-52057)
* Es wurde ein Problem behoben, das Kunden daran hinderte, ein [!UICONTROL Experience Fragment] in den Standardarbeitsbereich einzufügen. (TGT-52073)
* Es wurde ein Problem behoben, bei dem ein Angebot als „Inhalt nicht gefunden“ angezeigt wurde und nicht auf der Seite [!UICONTROL Angebote] für eine [!UICONTROL Automated Personalization] (AP)-Aktivität angezeigt wurde. (TGT-52150)
* Es wurde die Möglichkeit hinzugefügt, innerhalb einer Aktivität doppelte Zielgruppen zuzulassen. (TGT-51200)
* Fehlerkorrektur - Nach der Bearbeitung wird auf der Seite [!UICONTROL Ziele und Einstellungen] für eine XT-Aktivität kein falscher Mbox-Name mehr angezeigt. (TGT-52026)
* Es wurde ein Problem behoben, bei dem `defaultContent` in Optionen angezeigt wurden, obwohl sie nicht in `experiences/optionLocations` waren. (TGT-52036)
* Es wurde ein Problem behoben, um sicherzustellen, dass leere Zeichenfolgen nicht in Nullwerte konvertiert werden. (TGT-52037)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden [!UICONTROL Optimierungsziel] in [!UICONTROL Berichterstellungseinstellungen] auf der Seite [!UICONTROL Ziele und Einstellungen] nach Bearbeitungen neu konfigurieren mussten. (TGT-52071)
* Es wurde ein Problem behoben, bei dem bei einer Aktivität ohne Seitenbereitstellungsregeln mehrere Regeln auf der Seite [!UICONTROL Überblick] angezeigt wurden. (TGT-52084)
* Es wurde eine Fehlermeldung für Benutzer hinzugefügt, die versuchen, ein Angebot mit Zeichen außerhalb der mehrsprachigen Basisebene wie Emojis zu speichern. (TGT-52105)
* Fehlerkorrektur - Beim Öffnen einer Aktivität wird jetzt nicht mehr die Fehlermeldung „Diese Aktivität verwendet eine oder mehrere Zielgruppen, die an der Quelle gelöscht wurden.“ (TGT-52120)
* Es wurde ein Problem behoben, bei dem ClickTrack-Metriken während der Bearbeitung nicht im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) angezeigt wurden. (TGT-52152)
* Es wurde ein Problem behoben, bei dem eine URL mit einem Abfrageparameter als Speicherort der Aktivität den Abfrageparameter auf der Seite „Übersicht[!UICONTROL &#x200B; der &#x200B;] Aktivität nicht anzeigte. (TGT-51635)
* Es wurde ein Problem behoben, das die Anzeige der gesamten Erlebnis-URL im [!UICONTROL Durchsuchen-Modus] im [!UICONTROL Visual Experience Composer] (VEC) verhinderte. (TGT-52101)
* Es wurde ein Problem behoben, bei dem die Bearbeitung einer Aktivität dazu führte, dass die Seitenbereitstellung am Ende der URL ein &quot;/&quot; hinzufügte, wodurch sie ungültig wurde. (TGT-52114)
* Es wurde ein Problem behoben[!UICONTROL &#x200B; bei dem der Link &#x200B;]Aktivitäts-QA“ im [!UICONTROL formularbasierten Experience Composer] fälschlicherweise zur [!DNL Adobe Experience Cloud] Homepage umgeleitet wurde. (TGT-52055)
* Es wurde ein Problem behoben, bei dem zusätzliche Seiten, die zur [!UICONTROL A/B-Test]-Aktivität hinzugefügt wurden, nach dem Speichern und erneuten Öffnen nicht beibehalten wurden. (TGT-51994)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Stile im Abschnitt Inline-Stil zu löschen. (TGT-52070)
* Der Zugriff auf [Karten für Zielgruppendefinitionen](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) im Dialogfeld [!UICONTROL Aktivitäts-]&quot; wurde wiederhergestellt, ähnlich wie in der veralteten Benutzeroberfläche. (TGT-52056)
* Die aktualisierte Benutzeroberfläche hat Seiten oder Zielgruppen nicht ohne Änderungen gespeichert. Wenn Kundinnen und Kunden einer Aktivität neue Seiten oder Zielgruppen hinzugefügt, diese jedoch nicht geändert haben, haben [!DNL Target] die unveränderten Zielgruppen beim Speichern verworfen. An relevanten Stellen wurden Benachrichtigungen hinzugefügt, um Benutzer über dieses Verhalten zu informieren. (TGT-52104)

### [!DNL Target Standard/Premium] 25.4.1 (2. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der dazu führte, dass Erlebnis-Zielgruppen aus -Aktivitäten verschwanden. (TGT-52003)
* Fehlerkorrektur - Beim Versand treten jetzt keine unerwarteten Elemente mehr auf. (TGT-52011)
* Es wurde ein Problem behoben, das Kunden daran hinderte, die Zielgruppe im Zielgruppendiagramm auf der Seite [!UICONTROL /] und während der Bearbeitung der Aktivität anzuzeigen. (TGT-52050)
* Es wurde ein Problem behoben, das dazu führte, dass Kundinnen und Kunden Erlebnisse in [!UICONTROL Experience Targeting)-Aktivitäten (XT] nicht nach ihrer Priorität neu anordnen konnten. (TGT-52054)
* Es wurde ein Problem behoben, das beim Rückgängigmachen von Textstil-Änderungen zu falschem Rendering führte. (TGT-51876)
* Es wurde ein Problem behoben, durch das [!DNL Target] beim Ändern eines Umleitungsangebots auch alle [!UICONTROL ClickTrack]-Selektoren entfernt, die mit diesem Angebot verknüpft sind. (TGT-51936)
* Es wurde ein Problem behoben, das dazu führte, dass [!DNL Target] beim Abbrechen von [!UICONTROL ClickTrack] den Selektor fälschlicherweise speicherte. (TGT-51937)
* Es wurde ein Problem behoben, das nach dem Öffnen und Schließen der Mbox-Auswahl auf der Seite [!UICONTROL Ziele und Einstellungen] ohne Änderungen zu einem Fehler wegen ungültigem Namen führte. (TGT-51983)
* Es wurde ein Problem behoben, das die Bearbeitung von Ad-hoc-Angeboten blockierte, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. (TGT-51984)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten blockierte, die Ad-hoc-Angebote mit benutzerdefiniertem Code enthielten. (TGT-51995)
* Es wurde ein Problem behoben, das dazu führte, dass Ausschlussregeln beim Bearbeiten kombinierter Zielgruppendefinitionen als Einschlussregeln angezeigt wurden. (TGT-51999)
* Ein Problem wurde behoben, das dazu führte, dass benutzerdefinierter Code während der Erlebnisbearbeitung nicht korrekt angezeigt wurde. (TGT-52005)
* Es wurde ein Problem behoben, durch das die Option [!UICONTROL Einfügen vor] nicht verfügbar war, um Inhalte vor der Navigationsleiste einzufügen. (TGT-52031)
* Fehlerkorrektur - Das Standarderlebnis in Berichten wird jetzt korrekt hervorgehoben. (TGT-51716)
* Es wurde ein Problem behoben, das beim Erstellen einer Aktivität eine `default message [Invalid optionLocalIds: xx]]` auslöste. (TGT-52038)

### at.js-Version 2.11.8 (31. März 2025)

* Behobene CodeQL-identifizierte Sicherheitslücke in der Validierung von Zeichenfolgen-Suffixen, um Edge-Fälle während Größenänderungs- und Verschiebungsvorgängen zu verhindern. (TNT-51516)

### [!DNL Target Standard/Premium] 25.3.8 (28. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, das dazu führte[!UICONTROL &#x200B; dass die Seite &#x200B;]Aktivitäten“ langsam geladen wurde. (TGT-51151)

### [!DNL Target Standard/Premium] 25.3.7 (26. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, durch das das Speichern mehrseitiger Aktivitäten blockiert wurde, wenn eine Seite nach Änderungen gelöscht wurde. (TGT-51988)
* Es wurde ein Fehler behoben, der beim Bearbeiten einer Aktivität auftrat: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* Es wurde ein Problem behoben, durch das beim Hinzufügen neuer Änderungen zu einer Aktivität vorhandene Änderungen entfernt wurden. (TGT-51981)
* Es wurde ein Problem behoben, bei dem das Ersetzen einer Zielgruppe durch &quot;[!UICONTROL Alle Besucher]&quot; während der Erstellung oder Bearbeitung der Aktivität den Fehler „Doppelte Zielgruppen sind nicht zulässig“ verursachte. (TGT-51978)
* Es wurde ein Problem behoben, das beim Speichern einer A/B-Test[!UICONTROL -Aktivität den Fehler „Ungültige &#x200B;]&quot; verursachte. (TGT-51976)
* Es wurde ein Problem behoben, das verhinderte, dass berechnete Metriken korrekt auf der Seite [!UICONTROL Ziele und Einstellungen] angezeigt wurden. (TGT-51975)
* Es wurde ein Problem behoben, das verhinderte, dass in der [!DNL Analytics]-Konfiguration für die `pageviews` Metrik `companyName` und `reportSuite` vorhanden waren. (TGT-51965)
* Es wurde ein Problem behoben, durch das beim Wechsel zwischen Erlebnissen in einer Aktivität Änderungen entfernt wurden. (TGT-51945)
* Es wurde ein Problem behoben, bei dem beim Entfernen einer Seitenzielgruppe auch [!UICONTROL ClickTrack]-Selektoren entfernt wurden. (TGT-51935)
* Es wurde ein Problem behoben, durch das eine Aktivität nach dem Öffnen der Seite [!UICONTROL Überblick] nicht bearbeitbar war. (TGT-51931)
* Es wurde ein Problem behoben, das während der Erstellung einer Aktivität zu einem `[Unused optionLocalIds: 0]]`-Fehler führte. (TGT-51920)
* Es wurde ein Problem behoben, bei dem einige Änderungen nach dem Entfernen von Änderungen am Textstil nicht korrekt übersetzt wurden. (TGT-51876)
* Es wurde ein Problem behoben, das verhinderte, dass Zielgruppen in dem [!UICONTROL formularbasierten Experience Composer“ korrekt aktualisiert &#x200B;]. (TGT-51845)
* Es wurde ein Problem behoben, bei dem die URL [!UICONTROL Visual Experience Composer] während der Aktivitätsnavigation nicht korrekt aktualisiert wurde. (TGT-51832)
* Es wurde ein Problem behoben, durch das Angebote nicht in der [!UICONTROL Angebote]-Benutzeroberfläche angezeigt wurden, obwohl sie beim Erstellen einer Aktivität und Hinzufügen von Angeboten korrekt angezeigt wurden. (TGT-51805)
* Es wurde ein Problem behoben, bei dem einigen Aktivitäten ein Fallback-Bildschirm fehlte, um Standardinhalte anzuzeigen, wenn personalisierte oder zielgerichtete Inhalte nicht bereitgestellt werden konnten. (TGT-51638)
* Es wurde ein Problem behoben, durch das Live-Angebote und bestimmte Ordner nicht korrekt in der [!UICONTROL Angebote]-Benutzeroberfläche angezeigt wurden. (TGT-51628)
* Es wurde ein Problem behoben, durch das einige URL-Zeichenfolgen und goURLs nicht korrekt lokalisiert werden konnten. (TGT-35741)
* Es wurde ein Problem behoben, das verhinderte[!UICONTROL &#x200B; dass Rollen (], [!UICONTROL Editor] und [!UICONTROL Beobachter]) in der [!DNL Target]-Benutzeroberfläche korrekt lokalisiert wurden. (TGT-29925)

### [!DNL Target Standard/Premium] 25.3.6 (14. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Der Fehler „Ungültige Benutzereingabe“ in Aktivitäten von [!UICONTROL Visual Experience Composer] (VEC) wurde behoben, wobei [!UICONTROL Klick-Tracking] aktiviert, wenn derselbe [!UICONTROL Klick-Tracking]-Selektor mehrmals verwendet wird. (TGT-51921)
* Der Fehler „Ungültige Benutzereingabe“ in VEC-Aktivitäten mit freigegebenen Speicherorten (z. B. HEAD-Selektor) und identischen Angeboten wurde behoben. (TGT-51879)
* Es wurde ein Problem behoben, das dazu führte, dass Erlebnisänderungen für alle Zielgruppen freigegeben wurden. (TGT-51815)
* Validierungsfehler beim Erstellen von Aktivitäten aufgrund von Segment-ID-Konflikten wurden behoben. Die Fehler traten auf, als [!DNL Target] vorhandene Aktivitäten mit anonymen Segmenten erkannte. (TGT-51784)
* Es wurde ein Problem behoben, das [!DNL Target] daran hinderte, Aktivitäten mit Ausschlussregeln in einer Zielgruppe zu speichern. (TGT-51581)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Ordner ohne Zugriff auf den Standardarbeitsbereich zu erstellen, zu löschen oder zu verschieben. (TGT-51499)
* Es wurde ein Problem behoben, das dazu führte, dass GET-Anfragen beim Abrufen [!DNL Analytics] Metrikliste fehlschlugen. (TGT-51106)

### [!DNL Target Standard/Premium] 25.3.5 (11. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, durch das Benutzer keine Angebote im Bedienfeld [!UICONTROL Änderungen] ändern konnten. (TGT-51800)
* Es wurde ein Problem behoben, bei dem Aktionen im linken Bereich für Erlebnisse und Zielgruppen falsch angezeigt wurden, einschließlich im [!UICONTROL ClickTrack]-Modus. (TGT-51895)
* Es wurde ein Problem behoben, bei [!UICONTROL ClickTrack]-Selektoren nicht auf die richtige Zielgruppenseite angewendet wurden. (TGT-51871)

### [!DNL Target Standard/Premium] 25.3.4 (7. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem reine Aktivitäts-Zielgruppen im Bedienfeld [!UICONTROL Zielgruppen] nicht sichtbar waren, sodass sie nicht bearbeitet oder wiederverwendet werden konnten. (TGT-51860)
* Es wurde ein Problem behoben, durch das [!DNL Target Standard] Kunden keine Aktivitäten mit der Berichterstellung [!UICONTROL Analytics for Target] (A4T) erstellen konnten. (TGT-51854)
* Es wurde ein Problem behoben, durch das lokale ID-Zähler während Batch-Erstellungs- und -Bearbeitungsvorgängen von der Payload ausgeschlossen wurden. (TGT-51867)

### [!DNL Target Standard/Premium] 25.3.2 (6. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Fehlerkorrektur - Beim Kopieren einer Aktivität mit einer Zielgruppe auf Basis einer reinen Aktivität wird jetzt keine neue Aktivität mehr erstellt, sondern stattdessen die Zielgruppe der ursprünglichen Aktivität verwendet. (TGT-51855)
* Ein Problem wurde behoben, das die Bearbeitung von [!UICONTROL Experience Targeting]-Aktivitäten mit Zielgruppen, die nur für Aktivitäten bestimmt sind, verhinderte. (TGT-51846)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Visual Experience Composer] (VEC) beim ersten Bearbeiten keine Änderungen korrekt auf ein Erlebnis angewendet hat. (TGT-51843)
* Es wurde ein Problem behoben, das beim Klicken auf bestimmte Elemente in VEC einen „ID“-Fehler auslöste. (TGT-51814)
* Die Fehlerbehandlung in VEC während der Aktivitätserstellung wurde aktualisiert. (TGT-51759)
* Es wurde ein Problem behoben, bei dem eine fehlende Ansicht [!UICONTROL &#x200B; Bedienfeld &#x200B;]Änderungen“ einen Fehler „Ungültige Benutzereingabe“ beim Speichern der Aktivität verursachte. (TGT-51827)
* Es wurde ein Problem behoben, das die Erstellung von Recommendations-Kriterien verhinderte. (TGT-51834)
* Es wurde eine Bestätigungsnachricht vor der Weiterleitung an eine andere URL hinzugefügt. (TGT-51703)
* Es wurden Probleme mit GraphQL-Integrationstests in Angeboten und Ordnern behoben. (TGT-51839)

### [!DNL Target Standard/Premium] 25.3.1 (3. März 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Eine kombinierte Zielgruppe kann Untergruppen enthalten, von denen jede mehrere Zielgruppen enthält. In dieser Version wurde ein Problem behoben, das die Anzeige von Untergruppen-Zielgruppen im Dialogfeld [!UICONTROL Regeln] verhinderte. (TGT-51813)
* Es wurde ein Problem behoben, bei dem einige Erlebnis-Zielgruppen beim Öffnen älterer Aktivitäten durch [!UICONTROL Alle &#x200B;]&quot; ersetzt wurden. (TGT-51812)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten mit Audiences, die nur für Aktivitäten bestimmt sind, verhinderte. (TGT-51807)
* Es wurde ein Problem behoben, durch das die Bearbeitung von Änderungen am Seitenkopf in der aktualisierten [!DNL Target]-Benutzeroberfläche verhindert wurde. (TGT-51797)
* Es wurde ein Null-Fehler behoben, der beim Duplizieren eines Erlebnisses, beim Löschen eines anderen Erlebnisses und beim anschließenden Versuch, die Aktivität zu speichern, auftrat. (TGT-51796)
* Es wurde ein Problem behoben, das verhinderte, dass Regeln zum Ausschluss von Zielgruppen im Informationsbereich der Zielgruppe während des Schritts [!UICONTROL Targeting] beim Erstellen von Aktivitäten angezeigt wurden. (TGT-51579)
* Aktualisierte Fehlermeldungen, die auf Koreanisch lokalisiert sind. (TGT-51701 und TGT-51699)

### [!DNL Target Standard/Premium] 25.2.3 (26. Februar 2025)

Diese Version umfasst die folgenden Aktualisierungen:

* Es wurde ein Problem behoben, durch das Aktivitätsaktualisierungen nach [!DNL Target] Version 25.2.1 für einige Aktivitäten verhindert wurden. (TGT-51781)
* Es wurde ein Problem behoben, bei dem alle Änderungen an der im Status befindlichen Zielgruppe beim Abbrechen des Prozesses der Aktivitätserstellung entfernt wurden (Auswahl von [!UICONTROL Abbrechen] anstelle von [!UICONTROL Zielgruppe hinzufügen]). (TGT-51769 und TGT-51770)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Visual Experience Composer] (VEC) für einige Aktivitäten nicht geladen werden konnte, insbesondere wenn benutzerdefinierter Code verwendet wurde.  Dieses Problem führte dazu, dass der VEC einen leeren Bildschirm anzeigte oder die [!DNL Target] Benutzeroberfläche auf ihre ältere Version zurücksetzte. (TGT-51758)
* Es wurde ein Problem behoben, bei dem Änderungen nach der Bearbeitung der Seitenbereitstellung für Zielgruppen verworfen wurden. (TGT-51756)
* Es wurde ein Problem behoben, bei dem alle nicht-metrischen Zielgruppen (Seite und Erlebnis-Zielgruppen) aus Aktivitäten entfernt wurden, nachdem ein Metriktyp auf der Seite [!UICONTROL Ziele und Einstellungen] geändert wurde. (TGT-51753)
* Es wurde ein Problem behoben, bei dem durch Klicken [!UICONTROL Abbrechen] während der Bearbeitung einer Aktivität in der Target-Benutzeroberfläche [!UICONTROL Aktivitätenliste] anstelle der Seite [!UICONTROL Aktivitätsdetails] navigiert wurde. (TGT-51731)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Berichte über die Option [!UICONTROL Berichte in CSV exportieren] herunterzuladen. (TGT-51708)
* Es wurde ein Problem im formularbasierten Experience Composer behoben, bei dem [!DNL Target Standard] Kunden fälschlicherweise als mit [!UICONTROL Eigenschaften] einer [!DNL Target Premium] Funktion angezeigt wurden. (TGT-51678)
* Es wurde ein Problem behoben, durch das [!DNL Adobe Experience Platform] beim Erstellen neuer Angebote nicht angezeigt werden konnten. (TGT-51665)
* Alle aktiven Filter für [!DNL Recommendations] Inventar wurden in die Schnellsuche verschoben, wobei die Benutzeroberfläche [!UICONTROL &#x200B; der &#x200B;] Katalogsuche anstelle der Leiste [!UICONTROL Filter] ausgerichtet wurde. (TGT-50723)

### at.js-Version 2.11.7 (26. Februar 2025)

Diese Version enthält die folgende Aktualisierung:

* Fehlerkorrektur - Die Telemetrie-Protokollierung funktioniert jetzt, wenn `localStorage` nicht verfügbar ist. Die Telemetrie verursachte bei einigen Kunden, die in ihren Browsern deaktiviert `localStorage`, ein Problem.

Weitere Informationen zu dieser und vorherigen at.js-Versionen finden Sie unter [at.js-Versionsdetails](https://experienceleague.adobe.com/de/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

### Target Standard/Premium 25.2.1 (Dienstag, 17. Februar 2025) {#ui-update-2}

Diese Version umfasst die folgenden Aktualisierungen:

* [!UICONTROL Aktivitäten] Aktualisierung der Benutzeroberfläche
* Aktualisierung der [!DNL Recommendations]-Benutzeroberfläche

#### [!UICONTROL Aktivitäten] Aktualisierung der Benutzeroberfläche

Im Zuge der weiteren Modernisierung der [!DNL Adobe Target]-Benutzeroberfläche freuen wir uns, die allgemeine Verfügbarkeit der aktualisierten Benutzeroberfläche [!UICONTROL Aktivitäten] bekannt geben zu können.

>[!NOTE]
>
>Ab dem 17. Februar haben Kunden schrittweise Zugriff auf die neue Benutzeroberfläche [!UICONTROL Aktivitäten]. Um einen nahtlosen Rollout für alle Kunden sicherzustellen, wird diese Version in kontrollierten Phasen bereitgestellt. In der ersten Phase wird die ursprüngliche Gruppe [!DNL Target] Kunden auf die neue Benutzeroberfläche [!UICONTROL Aktivitäten] aktualisiert. In nachfolgenden Phasen werden die verbleibenden Kunden aktualisiert.

>[!IMPORTANT]
>
>Wichtige Informationen zum Plan zum Ende der Lebensdauer des [!DNL Target]-Benutzeroberflächen-Umschalters finden Sie unter [[!DNL Target] Einstellung des Benutzeroberflächen-Umschalters](/help/main/r-release-notes/release-notes.md#toggle).

Basierend auf dem neuesten [!DNL Adobe Spectrum] Design-System standardisiert das Update zuvor inkonsistente Design-Muster und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:

* [Neu gestaltete Berichterstellung](/help/main/administrating-target/reporting.md) um bessere Einblicke in die Ergebnisse der Aktivität zu erhalten.
* [[!UICONTROL &#x200B; Seite „Änderungsprotokoll]](/help/main/c-activities/change-log.md) wurde aktualisiert und es werden jetzt die Informationen aus dem [[!DNL Audit Query API]](https://experienceleague.adobe.com/de/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} für Echtzeit-Einblicke abgerufen.
* [Anpassbare Listenansichten](/help/main/c-activities/activities.md) für eine bessere Flexibilität bei den verschiedenen Team-Anforderungen.
* [Verbesserte Schnellinfo- und Detailbildschirme](/help/main/c-activities/activities.md) für einen einfacheren Zugriff auf Informationen.
* [Optionen für sitzungspersistente Suche und Filter](/help/main/c-activities/activities.md).
* Komplett [neu [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) mit Unterstützung für die neuesten Sicherheitsaktualisierungen von Browser-Anbietern und einer modernen Benutzeroberfläche.

  Informationen dazu, wie sich der aktualisierte VEC von der vorherigen Version unterscheidet, finden Sie unter:

  * [Änderungen am Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
  * [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Aktualisierte [!DNL Chrome] Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) Unterstützung von Manifest V3 für erhöhte Sicherheit und verbesserte Unterstützung für Erstanbieter-Cookies.

![Aktivitäten aktualisieren](/help/main/r-release-notes/assets/activities-refresh.png)

#### Aktualisierung der [!DNL Recommendations]-Benutzeroberfläche

Im Zuge der weiteren Modernisierung der [!DNL Adobe Target]-Benutzeroberfläche freuen wir uns, die allgemeine Verfügbarkeit der aktualisierten [!DNL Recommendations]-Benutzeroberfläche bekannt geben zu können.

>[!NOTE]
>
>Ab dem 17. Februar haben Kunden schrittweise Zugriff auf die neue Benutzeroberfläche [!UICONTROL Recommendations]. Um einen nahtlosen Rollout für alle Kunden sicherzustellen, wird diese Version in kontrollierten Phasen bereitgestellt. In der ersten Phase wird die ursprüngliche Gruppe [!DNL Target] Kunden auf die neue Benutzeroberfläche [!UICONTROL Aktivitäten] aktualisiert. In nachfolgenden Phasen werden die verbleibenden Kunden aktualisiert.

Basierend auf dem neuesten [!DNL Adobe Spectrum] Design-System standardisiert das Update zuvor inkonsistente Design-Muster und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:

* Die [Produktkatalogsuche](/help/main/c-recommendations/c-products/catalog-search.md) bietet jetzt eine aktualisierte Datenbank, die eine Echtzeit-Synchronisierung von Produkten ermöglicht.
* [!UICONTROL Recommendations]-Objekte ([!UICONTROL Kriterien], [!UICONTROL Designs], [!UICONTROL Sammlungen] und [!UICONTROL Ausschlüsse]), [&#x200B; über die API erstellt wurden, sind jetzt in der Benutzeroberfläche verfügbar](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Recommendations](/help/main/administrating-target/recommendations-settings.md)Einstellungen wurden im Abschnitt [!UICONTROL Administration] konsolidiert.
* Anpassbare Listenansichten für eine bessere Flexibilität bei den verschiedenen Team-Anforderungen.
* Die Code-Editoren für HTML und JSON wurden aktualisiert ([&#x200B; und Zeilennummerierung](/help/main/c-experiences/c-manage-content/create-json-offer.md).
* Verbesserte Bildschirme für Schnellinformationen und Details für einen einfacheren Zugriff auf Informationen.
* Optionen für sitzungspersistente Suche und Filter.

![Aktualisierung der Recommendations-Benutzeroberfläche](/help/main/r-release-notes/assets/recs-ui-refresh.png)

### Target Standard/Premium 25.1.1 (Freitag, 9. Januar 2025) {#ui-update-1}

Diese Version umfasst die folgenden Aktualisierungen:

#### Aktualisierung der [!UICONTROL Angebotsbibliothek] -Benutzeroberfläche

Um das Benutzererlebnis für [!DNL Adobe Target] Benutzer zu verbessern, aktualisiert diese Version die Benutzeroberfläche [!UICONTROL Angebotsbibliothek].

>[!NOTE]
>
>Um einen nahtlosen Rollout für alle Kunden sicherzustellen, wird diese Version in kontrollierten Phasen bereitgestellt. Im ersten Schritt wurde die ursprüngliche Gruppe der Target-Kunden auf die neue Angebots-Benutzeroberfläche aktualisiert. In nachfolgenden Phasen werden die verbleibenden Kunden aktualisiert.

>[!IMPORTANT]
>
>Wichtige Informationen zum Plan zum Ende der Lebensdauer des [!DNL Target]-Benutzeroberflächen-Umschalters finden Sie unter [[!DNL Target] Einstellung des Benutzeroberflächen-Umschalters](/help/main/r-release-notes/release-notes.md#toggle).

Mit dem neuesten [!DNL Adobe Spectrum]-Design-System standardisiert dieses Update inkonsistente Design-Muster und führt neue Verbesserungen ein, darunter die folgenden:

* **Massenangebotsverwaltung**: Gleichzeitiges Auswählen und Löschen oder Verschieben mehrerer Angebote.

* **[!UICONTROL Code-Editor]-Upgrades**: Aktualisierte HTML- und JSON-Editoren mit Syntaxhervorhebung und Zeilennummerierung.

* **Verbesserte Angebotskarten**: Verbesserte Karten für schnelle Informationen und Details für einen einfacheren Zugriff auf Informationen.

* **Persistente Suche und Filter**: Fügt Optionen für sitzungspersistente Suche und Filter hinzu.

Weitere Informationen finden Sie [Angebote](/help/main/c-experiences/c-manage-content/manage-content.md) und den Unterartikeln in diesem Abschnitt. Alle Artikel zu Angeboten in diesem Abschnitt wurden aktualisiert, um diese Änderungen an der Benutzeroberfläche widerzuspiegeln.

Im Folgenden finden Sie ein kurzes Video zu den Änderungen in dieser Version:

![Video zur Aktualisierung der Angebotsbenutzeroberfläche](/help/main/r-release-notes/assets/offers-video-v2.gif)
