---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e5bc137ed1f32b07569a4f1a31746da19fb164d3
workflow-type: tm+mt
source-wordcount: '1736'
ht-degree: 17%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.11.2 (14. November 2025)

**Decisioning-Angebote**

+++Details anzeigen
* **Angebotsentscheidungen mit ausgeblendeten oder ungültigen Selektoren können in der aktualisierten Benutzeroberfläche nicht bearbeitet werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Angebotsentscheidungen, die an ausgeblendete oder ungültige Selektoren gebunden waren, nicht bearbeitet werden konnten, es sei denn, das Element war in Visual Experience Composer (VEC) sichtbar. Die Bearbeitung wird jetzt direkt über das Bedienfeld unterstützt, wodurch die in der alten Benutzeroberfläche verfügbaren Funktionen wiederhergestellt werden und sichergestellt wird, dass Angebotsentscheidungen unabhängig von der Sichtbarkeit der Auswahl geändert werden können. (TGT-53899)

+++

**Recommendations**

+++Details anzeigen
* **Das Bearbeiten von Kriterien in einer Aktivität führte zum Absturz der Seite.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die Bearbeitung von Aktivitätskriterien dazu führte, dass die Seite mit Konsolenfehlern im Zusammenhang mit `useCrudActionsCtx` abstürzte. Der Kriterieneditor wird jetzt korrekt geladen und funktioniert, sodass Aktivitäten ohne Unterbrechung bearbeitet werden können. (TGT-53971)
* In **[!UICONTROL Message]Spalte konnten in der aktualisierten Benutzeroberfläche gelegentlich keine Produktdaten angezeigt werden.** Es wurde ein Problem in der aktualisierten [!UICONTROL Recommendations]-Benutzeroberfläche behoben, bei dem in der [!UICONTROL Message] Spalte in [!UICONTROL Catalog Search] gelegentlich keine Produktdaten angezeigt wurden, obwohl Werte im Feed vorhanden waren. Die Spalte zeigt nun konsistent die richtigen Nachrichtenwerte für alle Produkte an und gewährleistet so eine zuverlässige Sichtbarkeit, ohne dass die Spalte manuell neu konfiguriert werden muss. (TGT-52777)
* **[!UICONTROL Download Recommendations Data]Schaltfläche wird nach dem Speichern der Aktivität in der aktualisierten Benutzeroberfläche nicht angezeigt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Download Recommendations Data] für bestimmte gespeicherte Aktivitäten auch nach dem erneuten Speichern nicht angezeigt wurde. Die Schaltfläche wird jetzt über alle Aktivitäten hinweg konsistent angezeigt, sodass Benutzerinnen und Benutzer Empfehlungsdaten zuverlässig exportieren können, ohne Problemumgehungen zu benötigen. (TGT-53802)
* **Beim Öffnen bestimmter Produkte aus einer Sammlung wird „Angeforderte Ressource wurde nicht gefunden“ zurückgegeben, und dem Modal fehlt eine Option zum Schließen.** Es wurde ein Problem in der aktualisierten Recommendations-Benutzeroberfläche behoben, bei dem das Öffnen bestimmter Produkte aus einer Sammlung den Fehler „Angefragte Ressource wurde nicht gefunden“ auslöste und ein leeres modales Fenster ohne eine Option zum Schließen anzeigte. Das Modal lädt Produktdetails jetzt korrekt, und es steht immer eine Option zum Schließen zur Verfügung, um es elegant zu beenden. (TGT-53986)

+++

## [!DNL Target Standard/Premium] 25.11.1 (10. November 2025)


**Analytics for Target (A4T)**

+++Details anzeigen
* **[!UICONTROL Goals & Settings]Fehlermeldung bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle in der aktualisierten Benutzeroberfläche.** Es wurde ein Problem in der aktualisierten [!UICONTROL Overview]-Benutzeroberfläche behoben, bei dem im Abschnitt Ziele der Fehler „Irgendetwas ist schiefgelaufen“ angezeigt wurde. Wir können Ihre Anfrage nicht bearbeiten. Wenden Sie sich an [!DNL Adobe Client Care], wenn das Problem weiterhin besteht, wenn [!DNL Adobe Analytics] (A4T) als Berichtsquelle ausgewählt wurde. Ziele werden nun korrekt mit [!UICONTROL Adobe Analytics] Metriken angezeigt, was eine konsistente Sichtbarkeit über alle Berichtsquellen hinweg gewährleistet. (TGT-54021)

+++

**Zielgruppen**

+++Details anzeigen
* **In der aktualisierten Benutzeroberfläche können nicht mehrere Reporting-Zielgruppen ausgewählt werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Benutzende beim Bearbeiten einer Aktivität nicht mehrere neu erstellte Reporting-Zielgruppen gleichzeitig auswählen konnten. Es können jetzt mehrere Zielgruppen gleichzeitig zugewiesen werden, was die Flexibilität und Effizienz bei der Einrichtung von Berichten verbessert. (TGT-53253)

+++

**Decisioning-Angebote**

+++Details anzeigen
* **Entscheidungsangebote in der aktualisierten Benutzeroberfläche können nicht bearbeitet oder ersetzt werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Decisioning-Angebote nicht über das [!UICONTROL Modifications] bearbeitet oder ersetzt werden konnten und Angebotsnamen leer erschienen. Entscheidungsangebote sind jetzt vollständig barrierefrei und bearbeitbar, sodass die Parität mit der veralteten Benutzeroberfläche wiederhergestellt wird und sichergestellt ist, dass Kunden Angebote direkt in -Aktivitäten verwalten können. (TGT-53884)

+++

**Lokalisierung**

+++Details anzeigen
* **Korrektur mehrerer Lokalisierungsfehler in der koreanischen und japanischen Benutzeroberfläche.** (TGT-54003, TGT-54004, TGT-54006, TGT-54007 UND TGT-54018)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen
* **Bei einer Promotion nach Attribut mit Übereinstimmung bei einem Entitätsattribut konnte der Empfehlungsschlüssel nach dem Speichern der Aktivität nicht geladen werden.** Es wurde ein Problem behoben, bei dem bei Promotions des Typs [!UICONTROL Promotion by Attribute] mit dem Regeltyp [!UICONTROL Entity Attribute Matching] der Empfehlungsschlüssel nach dem Speichern einer Aktivität nicht geladen wurde. Das Problem wurde dadurch verursacht, dass der `customKeyId` nicht über GraphQL angefordert wurde. Empfehlungsschlüssel werden jetzt während der Bearbeitung der Promotion korrekt geladen. (TGT-53117)
* **Empfehlung bleibt beim Wechsel von ExpB zu ExpA visuell erhalten.** Es wurde ein Problem behoben, bei dem durch Einfügen einer Empfehlung in Erlebnis B und anschließendem Wechsel zu Erlebnis A das Feld für das Empfehlungsangebot sichtbar blieb. Dies war lediglich eine visuelle Inkonsistenz. Änderungen werden beim Wechseln zwischen Erlebnissen jetzt korrekt dargestellt, wodurch ein genaues Benutzeroberflächenverhalten sichergestellt wird. (TGT-53911)
* **Empfehlungsschlüssel wird für [!UICONTROL Promotion by Attribute] mit [!UICONTROL Entity Attribute] nicht geladen.** Es wurde ein Problem behoben, bei dem Promotions des Typs [!UICONTROL Promotion by Attribute] mit dem Regeltyp [!UICONTROL Entity Attribute Matching] den Empfehlungsschlüssel beim Bearbeiten nach dem Speichern einer Aktivität nicht geladen haben. Der Empfehlungsschlüssel wird jetzt korrekt über GraphQL abgerufen, sodass die Promotions wie erwartet angezeigt und funktionieren. (TGT-53917)
* **Bearbeiten von Empfehlungen für ausgeblendete HTML-Elemente funktioniert nicht in der aktualisierten Benutzeroberfläche.** Es wurde ein Problem in der [!UICONTROL New Create]- und VEC-Benutzeroberfläche behoben, bei dem Empfehlungsaktivitäten, die auf ausgeblendete HTML-Elemente angewendet wurden, nicht bearbeitet werden konnten. Diese Funktion funktioniert jetzt erwartungsgemäß und stellt die Parität mit der veralteten Benutzeroberfläche wieder her. Außerdem wird sichergestellt, dass Empfehlungen unabhängig von der Sichtbarkeit der Elemente geändert werden können. (TGT-53953)
* **Empfehlungsaktivitäten für ausgeblendete HTML-Elemente in der aktualisierten Benutzeroberfläche können nicht bearbeitet werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Empfehlungsaktivitäten, die auf ausgeblendete HTML-Elemente angewendet wurden, nicht bearbeitet werden konnten. Diese Funktion funktioniert jetzt erwartungsgemäß und stellt die Parität mit der veralteten Benutzeroberfläche wieder her. Außerdem wird sichergestellt, dass Empfehlungen unabhängig von der Sichtbarkeit der Elemente geändert werden können. (TGT-53951)
* **Im Empfehlungskatalog fehlen in der aktualisierten Benutzeroberfläche gelegentlich Attributwerte.** Es wurde ein Problem in der aktualisierten [!UICONTROL Recommendations]-Benutzeroberfläche behoben, bei dem in Katalogsuchlisten bestimmte Attributwerte (z. B. Nachricht) zeitweise nicht angezeigt wurden, selbst wenn sie im Produkt-Feed vorhanden waren. Attributwerte werden jetzt konsistent in Suchergebnissen geladen, ohne dass eine Spaltenumkonfiguration erforderlich ist. Dies verbessert die Zuverlässigkeit und Effizienz der Katalogverwaltung. (TGT-52769)
* **[!UICONTROL Download Recommendations]Schaltfläche für [!DNL Recommendations] Aktivitäten in der aktualisierten Benutzeroberfläche fehlt.** Es wurde ein Problem in der aktualisierten [!DNL Recommendations]-Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Download Recommendations] für A/B-Aktivitäten mit Recommendations nicht sichtbar war. Die Schaltfläche wird jetzt korrekt angezeigt, sodass Benutzende Empfehlungsdaten wie erwartet exportieren können, was der Funktionalität in der alten Benutzeroberfläche entspricht. (TGT-53768)
* **[!UICONTROL Download Recommendation Data]Schaltfläche fehlt in der aktualisierten Benutzeroberfläche „Übersicht“.** Es wurde ein Problem in der aktualisierten [!UICONTROL Overview]-Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Download Recommendation Data] für Aktivitäten mit Empfehlungen nicht sichtbar war. Die Schaltfläche wird jetzt korrekt angezeigt, sodass Benutzende Recommendations-Daten direkt exportieren können, ohne zur alten Benutzeroberfläche zurückkehren zu müssen. (TGT-53772)
* **Das Bearbeiten von Aktivitätskriterien führte in der aktualisierten Benutzeroberfläche manchmal zu einem leeren Bildschirm.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem durch Klicken [!UICONTROL Edit Criteria in Experiences] gelegentlich ein leerer Bildschirm für bestimmte Aktivitäten angezeigt wurde. Der Kriterieneditor wird jetzt zuverlässig über alle Aktivitäten hinweg geladen, sodass Benutzer ihn ohne Unterbrechung bearbeiten können. (TGT-53961)
* **Sequenzkriterien können in der aktualisierten Benutzeroberfläche nicht bearbeitet werden.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem der Versuch, [!UICONTROL Sequence Criteria] zu bearbeiten, dazu führte, dass das Kriterienpopup beim Laden hängen blieb und dann einen leeren Bildschirm anzeigte. Der Kriterieneditor wird jetzt korrekt geladen, sodass Benutzer Sequenzkriterien ohne Unterbrechung bearbeiten und aktualisieren können. (TGT-53985)

+++

**[!UICONTROL Reports]**

+++Details anzeigen
* **[!UICONTROL Multivariate Test](MVT)-Speicherorte und Diagrammberichterstattungsprobleme verhinderten die Berichterstellung.** Es wurde ein Problem behoben, bei dem MVT-Aktivitäten keine [!UICONTROL Location Contribution]- und Diagrammberichte in der Target-Benutzeroberfläche generieren konnten und der Fehler „Irgendetwas ist schiefgelaufen“ angezeigt wurde. Wir können Ihre Anfrage nicht bearbeiten.“ Berichte werden nun korrekt in der Benutzeroberfläche geladen, wodurch eine vollständige Sichtbarkeit gewährleistet ist. (TGT-53654)
* **MVT-Berichte werden aufgrund eines Fehlers [!UICONTROL Element] Beitragsbericht nicht geladen.** Es wurde ein Problem behoben, bei dem MVT-Aktivitätsberichte nicht in der Target-Benutzeroberfläche geladen werden konnten und der Fehler „Bericht zum Elementbeitrag konnte nicht abgerufen werden“ angezeigt wurde. Berichte werden jetzt korrekt angezeigt, sodass die Elementbeiträge vollständig sichtbar sind. (TGT-53691)
* **Exportieren von Auftragsdetails in CSV-Anfrage für [!UICONTROL Experience Targeting] (XT)-Aktivitäten.** Es wurde ein Problem behoben, bei dem die Option [!UICONTROL Export Order Details to CSV] fälschlicherweise für XT-Aktivitäten angezeigt und eine leere Datei zurückgegeben wurde. Die Option wird jetzt nur noch für AP-Aktivitäten angezeigt, um eine genaue Exportfunktion sicherzustellen und Verwirrung zu vermeiden. (TGT-53798)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Details anzeigen
* **[!UICONTROL Delete Modification]Problem mit der Schaltfläche hat das Entfernen von Aktivitätsänderungen verhindert.** Es wurde ein Problem behoben, bei dem die Schaltfläche [!UICONTROL Delete Modification] in der [!DNL Target]-Benutzeroberfläche nicht funktionierte, sodass Benutzer Änderungen innerhalb von Aktivitäten nicht entfernen konnten. Die Schaltfläche funktioniert jetzt erwartungsgemäß und ermöglicht das zuverlässige Löschen von Änderungen ohne Verzögerung. (TGT-53728)
* **Bevorzugte Selektoren werden in der aktualisierten Benutzeroberfläche nicht erkannt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem bevorzugte Selektoren wie `data-target-component-id` nicht in der CSS-Selektorliste im VEC angezeigt wurden. Benutzerinnen und Benutzer können jetzt zuverlässig bevorzugte Attribute anstelle von dynamisch generierten Klassennamen auswählen, was ein stabiles Targeting über SPA-Seitenaktualisierungen hinweg gewährleistet. (TGT-53908)
* **Die Ausrichtung des Aktivitätsstandorts stimmt nicht mit den [!UICONTROL Edit]- und [!UICONTROL Overview] überein.** Es wurde ein Problem behoben, bei dem die Nummerierung des Aktivitätsspeicherorts auf der Seite [!UICONTROL Overview] nicht mit Aktualisierungen auf der Seite [!UICONTROL  Edit Experience]abgestimmt war. Die Positionen bleiben jetzt in beiden Ansichten konsistent, sodass eine genaue Ausrichtung gewährleistet ist und fehlende oder falsch nummerierte Positionen vermieden werden. (TGT-53960 und TGT-53954)
* **In aktualisiertem VEC kann nicht zurück in den [!UICONTROL Design] Modus gewechselt werden.** Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem Benutzende nicht in den [!UICONTROL Design]-Modus zurückkehren konnten, nachdem sie im [!UICONTROL Browse]-Modus zu einer neuen Seite navigiert waren. Der [!UICONTROL Design]-Umschalter funktioniert jetzt ordnungsgemäß, sodass Änderungen nahtlos auf allen Seiten angewendet werden können. (TGT-53988 und TGT-53993)
* **Abfrageparameter wird in der Aktivitätsübersicht nicht angezeigt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Abfrageparameter für Aktivitäten nicht auf der Seite [!UICONTROL Overview] angezeigt wurden, was zu Diskrepanzen zwischen den URLs für die [!UICONTROL Overview] und die Seitenbereitstellung führte. Abfrageparameter werden jetzt korrekt angezeigt, sodass Aktivitätspositionen in allen Ansichten vollständig dargestellt und konsistent sind. (TGT-53701)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md) | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind. |
| [Versionshinweise für vorherige Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Sehen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium an. |
| [Versionshinweise zu Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de){target=_blank} | Sehen Sie sich die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an. |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| [Adobe Priority-Produktaktualisierung](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
