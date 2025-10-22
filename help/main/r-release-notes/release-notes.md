---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7d73870275c266055825c2fce90489ef82825fca
workflow-type: tm+mt
source-wordcount: '1700'
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

## [!DNL Target Standard/Premium] 25.10.1 (22. Oktober 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**Aktivitäten**

+++ Details anzeigen
* **Es wurde ein Problem mit der Benutzerfreundlichkeit in der aktualisierten Benutzeroberfläche**. [!UICONTROL Observers] können jetzt Aktivitäten mit der Option &quot;[!UICONTROL View Activity]&quot; in der Vorschau anzeigen, genau wie in der Benutzeroberfläche der Vorgängerversion. (TGT-51741)
* **[!UICONTROL Observer]Benutzer können jetzt Aktivitätsinhalte in der aktualisierten Benutzeroberfläche anzeigen.** Die Sichtbarkeit für Benutzer mit Beobachterrolle in der aktualisierten Benutzeroberfläche für Aktivitäten wurde wiederhergestellt. Zuvor konnten Beobachter keine Änderungen, Angebote und Inhaltsänderungen anzeigen - Funktionen, die in der alten Benutzeroberfläche verfügbar waren. (TGT-53785)
* **[!UICONTROL Approver]Benutzer können jetzt Aktivitätsziele bearbeiten, ohne dass ein Fehler mit Editor-Berechtigung auftritt.** Ein Berechtigungsproblem in der Benutzeroberfläche für die Erstellung von Aktivitäten wurde behoben, das Benutzende auf Genehmigerebene daran hinderte, Änderungen an erweiterten Zieleinstellungen zu speichern. Betroffene Benutzende erhielten einen `403 Forbidden.Resource` Fehler, der Editor-Berechtigungen erforderlich machte, obwohl sie über ausreichende Zugriffsrechte verfügten. (TGT-53819)

+++

**Zielgruppen**

+++Details anzeigen
* **Auswahl mehrerer Zielgruppen im Reporting „Nur diese Aktivität“ wiederhergestellt.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer mehrere Zielgruppen unter dem Abschnitt [!UICONTROL This activity only] in [!UICONTROL Goals & Settings] auswählen konnten. (TGT-53283)
* **Zielgruppenbasierte Berichtsdiagramme zeigen jetzt die Konversionsdaten korrekt an.** Es wurde ein Problem auf der Registerkarte &quot;[!UICONTROL Reports]&quot; behoben, das dazu führte, dass Diagramme bei der Auswahl von nicht standardmäßigen Zielgruppen fehlschlugen. Obwohl Daten- und Konfidenzmetriken verfügbar waren, zeigte das visuelle Diagramm nur eine durchgezogene Linie, was die Analyse schwierig machte. (TGT-53769)
* **Die [!UICONTROL Targeting]-Benutzeroberfläche zeigt jetzt eindeutig ausgeschlossene Zielgruppenregeln an.** Es wurde ein Problem im [!UICONTROL Targeting] Abschnitt der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, bei dem die auf [!UICONTROL Exclude] festgelegten Zielgruppenregeln nicht deutlich angezeigt wurden. Dies führte zu Verwirrung bei der Überprüfung der Zielgruppenbestimmungslogik, insbesondere für Zielgruppen, die bestimmte URLs ausschließen. (TGT-53809)
* **Zielgruppendefinitionswerte können jetzt auf der Registerkarte &quot;[!UICONTROL Targeting]&quot; ausgewählt und kopiert werden.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer Zielgruppenregelwerte auf der Registerkarte [!UICONTROL Targeting] auswählen und kopieren konnten. Diese Funktion war in der veralteten Benutzeroberfläche verfügbar, fehlt jedoch in der aktualisierten Benutzeroberfläche. (TGT-53856)

+++

**Lokalisierung**

+++Details anzeigen
* **Fehlerhafte Übersetzung von „quote“ im zh_CN-Seiteneditor.** hat einen kontextuellen Übersetzungsfehler im Gebietsschema zh_CN korrigiert, bei dem der Begriff „Angebot“ fälschlicherweise als &quot;&quot; übersetzt wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich die beabsichtigte Bedeutung auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53841)
* **Falsche Übersetzung von „Zitat entfernt“ im zh_CN Seiteneditor Kontext korrigiert.** hat einen Übersetzungsfehler im Gebietsschema zh_CN korrigiert, bei dem „entferntes Angebot“ fälschlicherweise als &quot;&quot; gerendert wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich der Begriff auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53843)
* **Falsche Übersetzung von „Zitat umgeordnet“ im zh_CN Seiteneditor Kontext korrigiert.** hat einen kontextuellen Übersetzungsfehler im Gebietsschema zh_CN korrigiert, bei dem „Angebot neu angeordnet“ fälschlicherweise als &quot;&quot; übersetzt wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich der Begriff auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53844)
* **Falsche Übersetzung von „Zitat geändert“ im zh_CN Seiteneditor Kontext korrigiert.** hat einen Übersetzungsfehler im Gebietsschema zh_CN korrigiert, bei dem „Angebot geändert“ fälschlicherweise als &quot;&quot; gerendert wurde, was auf ein kommerzielles Preisangebot hindeutet. Im Abschnitt Typografie > Überschriftenstil > Blockquote bezieht sich der Begriff auf ein Formatierungselement - Zitatblock - und nicht auf die Preisgestaltung. (TGT-53845)

+++

**Recommendations**

+++Details anzeigen
* **Änderungen an der CSS-Auswahl für Recommendations werden jetzt korrekt gespeichert.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer den CSS-Selektor für Recommendations-Platzierungen aktualisieren konnten. Änderungen wurden nach dem Speichern rückgängig gemacht, Aktualisierungen der Zielgruppen-Container wurden blockiert. (TGT-53835)
* **Die Auswahl des Seitenladeereignisses bleibt jetzt in den Empfehlungsänderungen erhalten.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, das verhinderte, dass Benutzer Änderungen speichern konnten, wenn der Ereignistyp einer Empfehlung von [!UICONTROL View] in [!UICONTROL Page Load] gewechselt wurde. Obwohl die Auswahl erfolgreich erschien, kehrte sie nach der Abfahrt zurück und blockierte die Veröffentlichung der Aktivität. (TGT-53957)

+++

**Berichte**

+++Details anzeigen
* **&quot;[!UICONTROL Export order details to CSV]&quot; lädt jetzt vollständige Daten herunter.** Es wurde ein Problem in der aktualisierten [!UICONTROL Overview]-Benutzeroberfläche behoben, das dazu führte, dass bei der Option &quot;[!UICONTROL Export Order details to CSV]&quot; leere Dateien heruntergeladen wurden, selbst wenn gültige Berichtsdaten vorhanden waren. (TGT-53787)

+++

**Sicherheit**

+++Details anzeigen
* **IMS-Vorfilter wurde hinzugefügt, um GQL-Endpunkte vor organisationsübergreifender Datengefährdung zu schützen.** hat eine Sicherheitslücke auf der Registerkarte Admin behoben, die sich auf die Endpunkte licenseGroups und targetProperties GraphQL auswirkte. Das Problem entstand durch die Verwendung der JIL-API mit einem Admin-Client-Token, das für den Zugriff auf unternehmensübergreifende Produktdaten ausgenutzt werden könnte. (TGT-53837)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen
* **Die Autoreninstanz wurde in der Benutzeroberfläche für die Erstellung von Aktivitäten wiederhergestellt.** Es wurde ein zeitweiliges Problem in der VEC-Benutzeroberfläche behoben, das dazu führte, dass das Authoring fehlschlug und Links unerwartet anklickbar wurden, wodurch Benutzer von der Seite weg weitergeleitet wurden. (TGT-53153)
* **Die Bearbeitung wurde für gespeicherte Aktivitäten in der Benutzeroberfläche zum Erstellen von Aktivitäten wiederhergestellt.** Ein Problem wurde behoben, das dazu führte, dass Benutzer nach dem Speichern von Änderungen keine Aktivitäten bearbeiten konnten. Betroffene Aktivitäten blieben in &quot;[!UICONTROL Applying initial modifications]&quot; stecken, blockierten weitere Updates und blendeten die Schaltfläche &quot;[!UICONTROL Cancel]&quot; aus. (TGT-53631)
* **Der VEC wartet nicht mehr mit &quot;[!UICONTROL Applying initial modifications]&quot; auf.** Es wurde ein Leistungsproblem in VEC behoben, das zu langen Verzögerungen beim Laden von Erlebnissen mit einer hohen Anzahl von Änderungen führte. Betroffene Benutzende sahen die Benutzeroberfläche mehrere Minuten lang auf &quot;[!UICONTROL Applying initial modifications]&quot; stecken, insbesondere in Experience B-Szenarien. (TGT-53727)
* **Der VEC lädt jetzt Änderungen ohne Stammelemente.**
Es wurde ein Problem in VEC behoben, das dazu führte, dass Erlebnisse beim Laden von Änderungen blockiert wurden, denen ein klares Stammelement fehlte. Durch diese Änderungen wurde die Benutzeroberfläche zuvor unbegrenzt an „A“ [!UICONTROL pplying initial modifications]. (TGT-53799)
* **Änderungen in Aktivitäten werden jetzt erwartungsgemäß gespeichert.** Es wurde ein berechtigungsbezogenes Problem in der neuen Benutzeroberfläche „Erstellen“ behoben, das verhinderte, dass Benutzer Änderungen speichern konnten, wenn sie Ziele und erweiterte Einstellungen in Aktivitäten bearbeiteten. Betroffene Benutzende sahen ein rotes Fehlerband und die Meldung „Forbidden.Resource“, obwohl sie angemessenen Zugriff hatten. (TGT-53816)
* **Die VEC-Benutzeroberfläche behält jetzt ansichtsübergreifende Erlebnisänderungen bei.** Es wurden mehrere Probleme in der aktualisierten VEC behoben, die sich auf die Erlebnisentwicklung auswirkten. Die Änderungen wurden nicht korrekt beibehalten, insbesondere wenn HTML-Angebote verwendet oder zwischen Ansichten gewechselt wurde. (TGT-53825)
* **Alle Ansichten werden jetzt korrekt angezeigt, wenn eine Änderung mehrere Erlebnisse umfasst.** Es wurde ein Problem in der Benutzeroberfläche zum Erstellen von Aktivitäten behoben, bei dem beim Anwenden einer Änderung in mehreren Ansichten nur eine Ansicht angezeigt wurde. In der Tooltip von „Mauszeiger bewegen“ konnten nicht alle zugehörigen Ansichten aufgelistet werden, obwohl die Änderung korrekt angewendet wurde. (TGT-53827)
* **Der VEC bleibt nicht mehr zeitweise bei &quot;[!UICONTROL Applying initial modifications]&quot; stehen.** Es wurde ein zeitweiliges Problem in VEC behoben, bei dem Erlebnisse nicht geladen werden konnten und auf &quot;[!UICONTROL Applying initial modifications]&quot; blieben. Dieses Verhalten war inkonsistent und löste manchmal Umleitungsschleifen aus oder erforderte eine manuelle Cache-Leerung. (TGT-53916)
* **VEC-Ladeproblem konnte nicht reproduziert werden.** Wir haben ein gemeldetes Problem untersucht, bei dem der VEC beim Bearbeiten vorhandener Aktivitäten auf &quot;[!UICONTROL Applying initial modifications]&quot; feststeckt. Es wurde vermutet, dass das Verhalten mit HTML-Inhalten zusammenhängt, denen ein übergeordnetes Element fehlt. Wir setzen die Überwachung auf Wiederholungen fort und empfehlen die Verwendung strukturierter Container für HTML-Angebote, um die Stabilität sicherzustellen. (TGT-53972)
* **[!UICONTROL Design]Modus im VEC verhält sich nicht mehr wie [!UICONTROL Browse] Modus mit Unterbrechungen.** Es wurde ein Problem in der Benutzeroberfläche behoben, bei dem sich der [!UICONTROL Design]-Modus zeitweise wie [!UICONTROL Browse]-Modus verhielt, klickbare `<a>`-Links ermöglichte und die Elementauswahl verhinderte. Dies führte dazu, dass das Hover-Feld ausgeblendet wurde und die Änderungs-Workflows blockiert wurden. (TGT-53136)
* **Klicks auf die Schaltfläche im [!UICONTROL Composer]-Modus führen nicht mehr zu einer Trigger-Seitenumleitung.** Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem das Klicken auf eine Schaltfläche im [!UICONTROL Composer]-Modus zu einer unerwarteten Umleitung zur Ziel-URL der Schaltfläche führte. Dies hinderte Benutzende daran, call-to-action (CTA)-Elemente zu bearbeiten, und störte den Authoring-Workflow. (TGT-53137)
* **Aktualisierungen des Angebotscodes in Aktivitäten von Automated Personalization werden jetzt fehlerfrei gespeichert.** hat ein Problem in der neuen Benutzeroberfläche „Erstellen“ behoben, das beim Aktualisieren des Angebots-Codes in [!UICONTROL Invalid user input] Aktivitäten zu einem &quot;[!UICONTROL Automated Personalization]&quot;-Fehler führte. Der Fehler hinderte Benutzer daran, Änderungen zu speichern, selbst wenn die Eingabe gültig war. (TGT-53586)
* Der **[!UICONTROL Design]-Modus in VEC blockiert jetzt die Link-Navigation für bearbeitbare Komponenten.** Es wurde ein Problem im aktualisierten VEC behoben, bei dem klickbare Elemente - wie Schaltflächen und Links - die Seitenumleitung auslösten, selbst wenn sie sich im [!UICONTROL Design] befanden. Dieses Verhalten ahmte den [!UICONTROL Browse]-Modus nach und hinderte Benutzer daran, Schlüsselkomponenten zu ändern. (TGT-53696)
* **Metrik [!UICONTROL Clicked an element] funktioniert jetzt ohne Umleitung oder Fehler.** Es wurde ein Problem in der Benutzeroberfläche „Neu erstellen“ behoben, das bei Auswahl der Konversionsmetrik &quot;[!UICONTROL Clicked an element]&quot; zu unerwarteten Umleitungen und leeren Bildschirmen führte. Durch Klicken auf eine Schaltfläche während des Setups wurde die Navigation ausgelöst, anstatt das Element zu registrieren, was zu einem &quot;[!UICONTROL element not found]&quot;-Fehler führte. (TGT-53817)
* **Vorhandene Aktivitäten bleiben während der Bearbeitung nicht mehr in der unendlichen Ladeschleife stecken.** Es wurde ein Problem in der Benutzeroberfläche „Neu erstellen“ behoben, bei dem durch die Bearbeitung einer vorhandenen Aktivität in Visual Experience Composer die Seite in einer unendlichen Ladeschleife stecken blieb. Dieses Problem hatte keine Auswirkungen auf neu erstellte Aktivitäten und wurde durch bereits vorhandene Änderungen auf der Seite ausgelöst. (TGT-53913)
* **Vorhandene Aktivitätsseiten mit Änderungen werden jetzt korrekt in VEC geladen.** Es wurde ein Problem im aktualisierten VEC behoben, durch das Seiten in der Ladephase beim Bearbeiten einer vorhandenen Aktivität mit gespeicherten Änderungen hängen blieben. Neue Aktivitäten ohne Problem geladen, aber zuvor konfigurierte Aktivitäten konnten nicht gerendert werden. (TGT-53967)

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
