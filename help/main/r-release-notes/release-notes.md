---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 186bfa96c0849d9cd838b3d493c10cccfd4ff068
workflow-type: tm+mt
source-wordcount: '4104'
ht-degree: 8%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

+++Details anzeigen
Das [!DNL Target]-Team bietet eine temporäre Funktion, mit der Sie mithilfe einer Umschalter-Schaltfläche zwischen der aktualisierten [!DNL Target]-Benutzeroberfläche und der Legacy-Version wechseln können. Diese Option ist nur während der letzten Phase des Rollouts der Benutzeroberfläche verfügbar.

![Umschalter für Target-Benutzeroberflächenversion](/help/main/r-release-notes/assets/toggle.png)

Sobald der Rollout abgeschlossen ist, wird der Umschalter entfernt und alle Benutzer wechseln dauerhaft zur aktualisierten Benutzeroberfläche. [!DNL Adobe] empfiehlt, vorauszuplanen, da diese Funktion bald auslaufen wird.

#### Zeitleiste der Einstellung

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, hat das [!DNL Target]-Team den Zeitplan für die Einstellung angepasst:

* **17. Juni 2025**: Alle IMS-Organisationen wurden für die aktualisierte [!DNL Target]-Benutzeroberfläche aktiviert, entweder für bestimmte Benutzer oder unternehmensweit, um mit dem Testen des neuen Erlebnisses zu beginnen.

* **30. Juni 2025**: Die [updated [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md) wurde zum Standarderlebnis für alle IMS-Organisationen, die den Umschalter für die Benutzeroberflächenversion aktiviert haben.

   * Kunden, die derzeit die veraltete Benutzeroberfläche sehen, sehen jetzt standardmäßig die aktualisierte Benutzeroberfläche bei der Anmeldung.
   * Der Umschalter für die Benutzeroberflächenversion bleibt bis Ende Juli verfügbar, sodass Benutzer bei Bedarf zurückkehren können.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] empfiehlt dringend, die aktualisierte [!DNL Target]-Benutzeroberfläche zu verwenden. Wechseln Sie nur dann zurück zur alten Benutzeroberfläche, wenn ein Blocker-Problem auftritt (aufgrund [ Einschränkungen des Umschaltverhaltens](#limitations).

* **15. Juli bis 30. Juli 2025**: Der Umschalter für die Benutzeroberflächenversion wird in Phasen dauerhaft deaktiviert. Betroffene IMS-Organisationen können nicht mehr zur alten Benutzeroberfläche zurückkehren.

   * Ausnahmen werden von Fall zu Fall überprüft.
   * Verzögerungen bei der Einstellung des Umschalters werden nur kurz (einige Tage) gewährt, während Blocker-Probleme behoben werden.

Wenden Sie sich bei Fragen oder [ Probleme, die während dieser Umstellung auftreten könnten, an die ](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md)Adobe-Kundenunterstützung.

#### Einschränkungen des Umschalt-Verhaltens der Benutzeroberfläche {#limitations}

Die folgenden Informationen beschreiben die Einschränkungen, die Sie bei der Verwendung des Umschalters Version beachten sollten:

* **Sichtbarkeit neuer Aktivitäten**: Aktivitäten, die in der aktualisierten Benutzeroberfläche erstellt wurden, werden nicht angezeigt, wenn Sie zur alten Benutzeroberfläche zurückkehren.
* **Bearbeiten vorhandener Aktivitäten**: Änderungen an vorhandenen Aktivitäten (die ursprünglich in der veralteten Benutzeroberfläche erstellt wurden), während die aktualisierte Benutzeroberfläche verwendet wird, werden auf Ihrer Website veröffentlicht. Diese Aktualisierungen sind jedoch nicht in der alten Benutzeroberfläche sichtbar, wenn Sie zurückwechseln. Dort werden nur die letzten Aktualisierungen angezeigt, die von der alten Benutzeroberfläche vorgenommen wurden.
* **Konsistenz der Aktivitätsdetails**: Die neuesten Änderungen werden unabhängig von der verwendeten Benutzeroberfläche auf Ihrer Live-Website angezeigt. Die veraltete Benutzeroberfläche zeigt jedoch nur die neuesten Änderungen an, die innerhalb dieser Version vorgenommen wurden. Dies kann verwirrend sein, wenn die in der aktualisierten Benutzeroberfläche bearbeiteten Aktivitäten anders aussehen als die in der alten Benutzeroberfläche.

#### Weitere Ressourcen zu Informationen über die aktualisierte Benutzeroberfläche

* [[!DNL Target] Häufig gestellte Fragen zur Aktualisierung der Benutzeroberfläche](/help/main/c-intro/updated-ui-faq.md): In dieser häufig gestellten Frage werden häufige Fragen zur neuen [!DNL Target]-Benutzeroberfläche und -[!UICONTROL Visual Experience Composer] (VEC) behandelt, einschließlich Navigationsänderungen, Funktionsspeicherorte und der Einstellung des Umschalters für die temporäre Benutzeroberfläche. Unabhängig davon, ob Sie Marketing-Experte, Entwickler oder Administrator sind, hilft Ihnen diese häufig gestellte Frage dabei, den Übergang reibungslos zu gestalten und die aktualisierte Benutzeroberfläche optimal zu nutzen.
* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für [!UICONTROL Activities], [!UICONTROL Recommendations] und den [!UICONTROL Visual Experience Composer] (VEC).
* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für die [!UICONTROL Offers Library].
* [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md): Bietet einen kurzen Überblick, der Ihnen hilft, sich mit [!DNL Target] vertraut zu machen, und enthält Links für detailliertere Informationen und schrittweise Anweisungen.
* [[!UICONTROL Visual Experience Composer] Änderungen](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der alten und der aktualisierten Version des VEC erläutert.
* [[!UICONTROL Visual Experience Composer] Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): In diesem Artikel werden die aktualisierte VEC-Benutzeroberfläche und ihre Optionen erläutert.

+++

## [!DNL Target Standard/Premium] 25.9.2 (22. September 2025)

Dieses Release enthält die folgenden Fehlerbehebungen und Erweiterungen:

**[!UICONTROL Audiences]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem Aktivitäten aufgrund ungültiger Zielgruppen-IDs nicht kopiert werden konnten.** Kunden, die versuchten, Aktivitäten im aktualisierten Prozess der Aktivitätserstellung zu kopieren, trat ein Fehler auf, der durch ungültige Zielgruppen-IDs verursacht wurde (z. B. -1752722444307). Dieses Backend-Validierungsproblem verhinderte die Duplizierung von Aktivitäten innerhalb desselben Arbeitsbereichs. Dieses Problem wurde behoben, und Aktivitäten können jetzt erfolgreich kopiert werden, ohne dass zielgruppenbezogene Fehler auftreten. (TGT-53717)
* **Es wurde ein Problem behoben, bei dem in den [!UICONTROL Automated Personalization] Aktivitäten des [!UICONTROL Manage Content]-Modals Fehler bei der Benutzereingabe für Zielgruppen auftraten, die nur für Aktivitäten bestimmt waren.** Kunden haben beim Konfigurieren von Zielgruppen „Nur Aktivität“ im [!UICONTROL  Manage Content]-Modal für AP-Aktivitäten Fehler bei der Benutzereingabe festgestellt. Dieses Problem trat auf, obwohl die Zielgruppen zuvor erfolgreich verwendet wurden. Kombinierte Zielgruppenkonfigurationen werden jetzt korrekt gespeichert, ohne dass Validierungsfehler ausgelöst werden. (TGT-53749)

+++

**Dokumentation**

+++Details anzeigen
* **Target-spezifische Web SDK-Dokumentationsseiten wurden in das Adobe Target-Repository verschoben.** Im Rahmen der Neustrukturierung der Web SDK-Dokumentation wurden [!DNL Target] Inhalte von den allgemeinen Web SDK-Dokumenten in das [!DNL Adobe Target]-[ migriert](https://experienceleague.adobe.com/en/docs/target-dev/developer/a4t/overview-a4t?lang=en){target=_blank}. Diese Änderung verbessert die Auffindbarkeit von Inhalten und stellt sicher, dass die lösungsspezifische Anleitung vom entsprechenden Produkt-Team gepflegt wird. (TGT-53374)

+++

**[!UICONTROL Offer Decisions]**

+++Details anzeigen
* **Die Option Angebotsentscheidung ist jetzt bei der Erstellung der ersten Aktivität durchgängig sichtbar.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die Option [!UICONTROL Offer Decision] beim erstmaligen Erstellungsfluss von A/B-Aktivitäten nicht angezeigt wurde, insbesondere beim Zugriff im Inkognito-Modus auf Mandanten mit aktivierten Angebotsentscheidungen. Die Option wird nur angezeigt, nachdem zum [!UICONTROL Targeting] Schritt navigiert wurde und zurück zu [!UICONTROL Experiences]. Durch diese Fehlerbehebung wird sichergestellt, dass die [!UICONTROL Offer Decision]-Option bei der Ersteinrichtung sofort verfügbar ist, was die Benutzerfreundlichkeit verbessert und die Verwirrung verringert. (TGT-51888)

+++

**[!UICONTROL Offers]**

+++Details anzeigen
* **Es wurde ein Problem behoben, bei dem Umleitungsangebote beim `redirectOptions` keine `includeContent=true` in die Payload enthielten.** Kunden, die Umleitungsangebote mit abrufen`includeContent=true ` fehlte in der Antwort-Payload das Feld `redirectOptions` . Diese Inkonsistenz wirkte sich auf Workflows aus, z. B. auf das Kopieren von Angeboten und die Erstellung von Aktivitäten. Umleitungsangebote enthalten jetzt bei Inhaltsanfragen korrekt `redirectOptions`. (TGT-53737)

+++

**[!DNL Recommendations]**

+++Details anzeigen
* **Klick-Tracking für [!UICONTROL Recommendations] Aktivitäten wiederhergestellt, die in der aktualisierten Benutzeroberfläche erstellt wurden.** Es wurde ein Problem behoben, bei dem [!UICONTROL Recommendations] in der aktualisierten Benutzeroberfläche erstellten Aktivitäten das Klick-Tracking nicht registrieren konnten, was zu null gemeldeten Konversionen führte. In der veralteten Benutzeroberfläche erstellte Aktivitäten verfolgten Klicks korrekt und meldeten Konversionen erwartungsgemäß. Diese Fehlerbehebung stellt sicher, dass die in der aktualisierten Benutzeroberfläche erstellten Recommendations-Aktivitäten jetzt die richtigen Tracking-Attribute enthalten und Konversionsberichte sowie die Ausrichtung an A4T-Metriken wiederhergestellt werden. (TGT-53287)
* **Klick-Tracking für Recommendations-Aktivitäten wiederhergestellt.** Es wurde ein Problem behoben, bei dem [!UICONTROL Recommendations] in der aktualisierten Benutzeroberfläche erstellten Aktivitäten das Klick-Tracking nicht registrieren konnten, was zu null gemeldeten Konversionen führte. Die veraltete Benutzeroberfläche hat eine Tracking-ID (`at-track-click`) korrekt auf [!UICONTROL Recommendations] Inhalte angewendet, während die aktualisierte Benutzeroberfläche fälschlicherweise einen Platzhalter (`__recsClickTrackIdPlaceholder__`) eingefügt hat, was das Backend-Tracking verhindert hat. Diese Fehlerbehebung stellt sicher, dass [!DNL Recommendations] Inhalt jetzt die richtige Tracking-ID enthält, sodass das Konversionsreporting wiederhergestellt und die Ausrichtung an A4T-Metriken wiederhergestellt werden kann. (TGT-53496)
* **Absturz des Sammlungseditors in der aktualisierten Benutzeroberfläche behoben.** Es wurde ein Problem in der aktualisierten [!UICONTROL Visual Experience Composer] (VEC)-Benutzeroberfläche behoben, bei dem das Öffnen einer Sammlung im Editor-Bereich zum Absturz der Seite mit einem TypeError führte: Eigenschaften von nicht definierten Inhalten konnten nicht gelesen werden (Lesen von „customLocale„). Dieser Fehler trat über mehrere Aktivitätstypen hinweg auf, einschließlich [!UICONTROL Recommendations]- und A/B-Tests. (TGT-53703)
* **Option zum Entfernen der ausgewählten Sammlung, die in VEC wiederhergestellt wurde.** Es wurde ein Problem in VEC behoben, bei dem Benutzende nur eine ausgewählte Sammlung in einer [!UICONTROL Recommendations] Aktivität ersetzen, sie jedoch nicht vollständig entfernen konnten. Diese Einschränkung blockierte Anwendungsfälle, die eine saubere Entfernung der Sammlung ohne Ersatz erfordern. Mit dieser Fehlerbehebung wird eine klare Option zum Entfernen der ausgewählten Sammlung eingeführt, was eine größere Flexibilität bei der Einrichtung von Aktivitäten und die Anpassung an das Verhalten der veralteten Benutzeroberfläche ermöglicht. (TGT-53652)
* **Benutzerdefinierte Kriteriensammlungen werden nun in der [!UICONTROL Recommendations] Benutzeroberfläche korrekt angezeigt.** Es wurde ein Problem in der Recommendations-Oberfläche behoben, bei dem mit benutzerdefinierten Kriterien erstellte Sammlungen keine Produktergebnisse anzeigen konnten. Während standardmäßige attributbasierte Sammlungen erwartungsgemäß funktionierten, gaben diejenigen, die benutzerdefinierte Filter verwendeten, trotz gültiger Katalogübereinstimmungen „Keine Ergebnisse gefunden“ zurück. Durch diese Fehlerbehebung wird sichergestellt, dass Sammlungen, die benutzerdefinierte Attribute verwenden, jetzt korrekt in der Registerkarte [!UICONTROL Product] ausgefüllt werden, sodass die volle Funktionalität für personalisierte Recommendations-Workflows wiederhergestellt wird. (TGT-53653)
* **Es wurde ein Problem behoben, bei dem Sammlungen beim ersten Öffnen der [!UICONTROL Products]-Seite keine Produkte anzeigten.** Kunden, die auf Sammlungen im Abschnitt [!UICONTROL Recommendations] zugreifen, haben beim ersten Öffnen der [!UICONTROL Products] leere Produktergebnisse erhalten. Dieses Problem wurde durch einen Backend-Fehler in der GraphQL-Abfrage verursacht, der beim Laden von Produktdaten für Sammlungen mit benutzerdefinierten Kriterien fehlgeschlagen ist. Das Problem wurde behoben, und Produkte werden nun korrekt angezeigt, ohne dass die Umgebung gewechselt werden muss. (TGT-53694)
* **Es wurde ein Problem behoben, bei dem Sammlungen in formularbasierten [!UICONTROL Recommendations]-Aktivitäten nicht entfernt werden konnten.** Kunden, die [!UICONTROL Recommendations] Aktivitäten mit dem [!UICONTROL Form-Based Experience Composer] erstellen, konnten die Auswahl einer zuvor ausgewählten Sammlung nicht aufheben. Vor dem Speichern der Benutzeroberfläche muss eine Sammlung ausgewählt sein, damit Benutzer nicht zu „Alle Sammlungen“ zurückkehren können. Dieses Verhalten wurde aktualisiert, damit es der VEC-Funktionalität entspricht, sodass Kundinnen und Kunden ohne ausgewählte Sammlung speichern und standardmäßig wie erwartet „Alle Sammlungen“ verwenden können. (TGT-53708)
* **Es wurde ein Problem behoben, bei dem Promotions aufgrund fehlender Sammlungs- oder Filterregelwerte nicht nach Attribut festgelegt werden konnten.** Kunden, die im Prozess zur Erstellung einer Aktivität Promotions nach Attribut konfigurieren, ist ein Fehler aufgetreten, der angibt, dass in einer Promotion entweder eine Sammlungs-ID oder Filterregelwerte fehlten. Dieses Validierungsproblem blockierte den Fortschritt, selbst wenn die Einrichtung abgeschlossen zu sein schien. Promotions können jetzt erfolgreich gespeichert werden, wenn sie nach Attribut konfiguriert wurden. (TGT-53750)
* **Es wurde ein Problem behoben, bei dem Aktivitäten aufgrund doppelter Erlebnisnamen nicht gespeichert werden konnten.** Kunden haben beim Speichern von Aktivitäten, die bestimmte Kombinationen von Kriterien und Designs enthielten, den Fehler „Ungültige Benutzereingabe“ festgestellt. Der Fehler wurde durch doppelte Erlebnisnamen ausgelöst, selbst wenn das Setup gültig zu sein schien. Aktivitäten mit unterschiedlichen Konfigurationen können jetzt ohne Namenskonflikte gespeichert werden. (TGT-53805)
* **Es wurde ein Problem behoben, bei dem die Validierung für nach Attribut konfigurierte Promotions ungültig blieb.** Kunden stießen bei der Einrichtung von Promotions nach Attribut im Prozess der Aktivitätserstellung auf dauerhafte Validierungsfehler, selbst wenn alle erforderlichen Felder korrekt ausgefüllt wurden. Dieses Problem wurde durch eine falsche Validierungslogik im [!UICONTROL Recommendations]-Workflow verursacht. Attributbasierte Promotions werden jetzt wie erwartet validiert und gespeichert. (TGT-53811)
* **Es wurde ein Problem behoben, bei dem durch die Anwendung einer Promotion auf eine Live [!UICONTROL Recommendations]-Aktivität ein Fehler ausgelöst wurde.** Kunden haben den Fehler „Bei einer Promotion fehlen entweder eine Sammlungs-ID oder Filterregelwerte“ festgestellt, wenn sie versuchten, eine Frontend-Promotion auf eine Live [!UICONTROL Recommendations]-Aktivität anzuwenden, selbst nachdem sie gültige Konfigurationsdetails angegeben hatten. Promotions können jetzt erfolgreich auf Live-Aktivitäten angewendet werden, ohne Validierungsfehler auszulösen, was ein reibungsloseres Erlebnis in der aktualisierten Benutzeroberfläche zur Erstellung von Aktivitäten gewährleistet. (TGT-53738)
* **Es wurde ein Problem behoben, bei dem Produkte in Sammlungen in der [!UICONTROL Recommendations]-Benutzeroberfläche nicht sichtbar waren.** Kunden eines einzelnen Mandanten meldeten, dass Produktlisten nicht geladen werden konnten, wenn bestimmte Sammlungen im Abschnitt [!UICONTROL Recommendations] der neuen Benutzeroberfläche angezeigt wurden. Das Problem wurde vorübergehend durch Wechseln der Umgebungen behoben, diese Problemumgehung führte jedoch zu einem schlechten Benutzererlebnis. Produktentitäten werden jetzt konsistent geladen, ohne dass die Umgebung umgeschaltet werden muss. (TGT-53783)
* **Es wurde ein Problem behoben, bei dem Kriterien und Designs nicht in einer Zeile der Benutzeroberfläche für die Erstellung von Aktivitäten angezeigt wurden.** Zuvor wurden Kriterien und Designs im Prozess zur Erstellung von Aktivitäten in einem komprimierten Format angezeigt, sodass es für Kunden schwierig ist, einzelne Elemente anzuzeigen und zu verwalten. Jedes Kriterium und Design wird jetzt in einer eigenen Zeile angezeigt, was die Lesbarkeit und Benutzerfreundlichkeit in der aktualisierten Benutzeroberfläche verbessert. (TGT-53818)

+++

**Berichte**

+++Details anzeigen
* **[!UICONTROL Total Revenue]Metrik ist jetzt in CSV-Exporten aus Aktivitätsberichten enthalten.** Es wurde ein Problem in der aktualisierten [!UICONTROL Overview]-Benutzeroberfläche behoben, bei dem der Gesamtumsatz in der Ansicht des Aktivitätsberichts korrekt angezeigt wurde, aber im CSV-Export fehlte und als 0 $ angezeigt wurde. Aufgrund dieser Diskrepanz konnten sich Benutzer für Offline-Analysen und -Berichte nicht auf exportierte Daten verlassen. (TGT-53325)
* **[!UICONTROL Total Sales]Metrik ist jetzt in CSV-Exporten aus Aktivitätsberichten enthalten.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem die [!UICONTROL Total Sales] Metrik in der Ansicht des Aktivitätsberichts korrekt angezeigt wurde, aber im CSV-Export fehlte. Aufgrund dieser Diskrepanz konnten Benutzer nicht auf vollständige Leistungsdaten in heruntergeladenen Berichten zugreifen. Diese Fehlerbehebung stellt sicher, dass [!UICONTROL Total Sales] jetzt korrekt in CSV-Exporten enthalten sind, wodurch die Konsistenz zwischen In-App-Reporting und Offline-Analyse wiederhergestellt wird. (TGT-53330)
* **Verbesserte Fehlermeldung für [!UICONTROL Graph View], wenn Metriken nicht aktiviert sind.** Es wurde ein Problem in VEC behoben, bei dem der [!UICONTROL Graph View] eine generische Fehlermeldung anzeigte, wenn eine angeforderte Metrik in der zugehörigen [!DNL Analytics] Report Suite nicht aktiviert war. Dieses Problem wurde durch einen `not_enabled_metric` in der Backend-GraphQL-Antwort ausgelöst. Diese Fehlerbehebung ersetzt den vagen Fehler durch eine informativere Meldung, die Benutzern hilft, Konfigurationsprobleme in [!DNL Analytics] zu identifizieren, wodurch Verwirrung und unnötige Support-Eskalationen reduziert werden. (TGT-53577)
* **Es wurde ein Problem behoben, bei dem die Berichtsdauer das unterstützte Limit von 90 Tagen überschritt.** Kunden, die den Filter &quot;[!UICONTROL Last X Days]&quot; im [!UICONTROL Reports] verwenden, konnten eine Dauer von mehr als 90 Tagen auswählen, was zu Leistungsproblemen und unvollständigen Daten führen konnte. Der Filter wurde aktualisiert, um einen maximalen Zeitraum von 90 Tagen zu erzwingen und ein konsistentes und zuverlässiges Reporting zu gewährleisten. (TGT-53795)
* **Es wurde ein Problem behoben, bei dem Leistungs-CSV-Berichte unter Verwendung der Standardumgebung anstelle der ausgewählten Umgebung generiert wurden.** Als Kundinnen und Kunden die Umgebung in den Berichtseinstellungen geändert und einen Leistungsbericht generiert haben, enthielt die resultierende CSV-Datei bisher Daten aus der Standardumgebung und nicht aus der ausgewählten.  Die Benutzeroberfläche übergibt nun den `environmentId`-Parameter korrekt, sodass der Bericht die ausgewählte Umgebung widerspiegelt. Darüber hinaus wurde die Fehlerbehandlung verbessert. Wenn während der CSV-Generierung GraphQL-Fehler auftreten, zeigt die Benutzeroberfläche jetzt eine klare Fehlermeldung an, anstatt eine leere CSV-Datei zu erstellen. (TGT-53064)
* **Es wurde ein Problem behoben, bei dem in der Berichterstellung von Analytics for Target (A4T) keine Daten in [!UICONTROL Graph View] angezeigt wurden.** Kunden, die [!DNL Target] mit A4T-Integration verwenden, haben beim Wechsel zur Diagrammansicht auf der Registerkarte Reporting von A/B-Testaktivitäten den Fehler „Irgendetwas ist schiefgelaufen“ festgestellt. Obwohl der [!UICONTROL Table View] korrekt geladen wurde, konnten [!UICONTROL Graph View] keine Metrik-Trends über den ausgewählten Zeitraum rendern. [!UICONTROL Graph View] zeigt jetzt für alle unterstützten Metriken die erwarteten Leistungsdaten an und verbessert so die Sichtbarkeit und Berichtsgenauigkeit in der aktualisierten Benutzeroberfläche. (TGT-53573)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen
* **Elementmetadaten sind jetzt beim Bewegen des Mauszeigers im Breadcrumb-Menü sichtbar.** Das Breadcrumb-Menü in VEC wurde verbessert, sodass beim Bewegen des Mauszeigers über ein Element zusätzliche Elementdetails wie ID, Klasse und Name angezeigt werden. Diese Verbesserung hilft Benutzenden, Elemente während der Einrichtung von Aktivitäten leichter zu identifizieren und zu unterscheiden. (TGT-53409)
* **Breadcrumb-Mauszeiger hebt jetzt das entsprechende Element in VEC hervor.** Die [!UICONTROL Visual Experience Composer] wurde verbessert, sodass das entsprechende Element im Editor hervorgehoben wird, wenn der Mauszeiger über Elemente im Breadcrumb-Menü bewegt wird. Der Elementtyp wird ebenfalls angezeigt, z. B. Container, fett gedruckter Text oder Schaltfläche. Dieses Verhalten gilt für gleichrangige -Elemente und schließt nicht unterstützte Typen wie SVG basierend auf der Validierungsliste aus. (TGT-53411)
* **Warnhinweis zu nicht gespeicherten Änderungen wurde in VEC-Änderungs-Workflows wiederhergestellt.** Es wurde ein Problem in VEC behoben, bei dem Benutzende nicht mehr über nicht gespeicherte Änderungen in benutzerdefinierten Code-Änderungen benachrichtigt wurden. Im Gegensatz zur veralteten Benutzeroberfläche fehlten für das neue Erlebnis Eingabeaufforderungen beim Navigieren weg oder Schließen des Personalisierungseditors, was zu einem versehentlichen Verlust des Fortschritts führte. Mit dieser Fehlerbehebung werden Warnhinweise für alle Änderungstypen, einschließlich benutzerdefiniertem Code, wiederhergestellt und sichergestellt, dass Benutzende vor dem Beenden gewarnt werden, ohne zu speichern. (TGT-53435).
* **Änderungen am benutzerdefinierten Code bleiben jetzt während der Seitenaktualisierung im VEC erhalten.** Es wurde ein Problem in VEC behoben, bei dem Änderungen an benutzerdefiniertem Code während der Aktualisierung der Website verloren gingen. Dieses Problem trat auf Seiten mit mehreren Neuladungen auf, sodass der Editor nicht gespeicherte Änderungen zurücksetzen und rückgängig machen konnte. Durch die Korrektur wird sichergestellt, dass benutzerdefinierte Code-Bearbeitungen auch dann intakt bleiben, wenn die Seite während der Bearbeitung neu geladen wird, um einen versehentlichen Verlust des Fortschritts zu verhindern. (TTGT-53501)
* **Anmeldeproblem für den Site-Zugriff innerhalb des VEC behoben.** Es wurde ein Problem behoben, bei dem sich Benutzende beim Zugriff über VEC nicht bei ihrer Website anmelden konnten. Der Anmeldefluss leitete Benutzer wiederholt zur Anmeldeseite zurück, wodurch die Einrichtung und Vorschau von Aktivitäten verhindert wurde. Diese Fehlerbehebung stellt sicher, dass der VEC nicht mehr in das Anmeldeverhalten eingreift und so den erwarteten Zugriff für authentifizierte Benutzer wiederherstellt. (TGT-53524)
* **Problem mit Cookie-Duplikaten in der VEC Helper-Erweiterung behoben.** Es wurde ein Problem behoben, bei dem die [!UICONTROL Adobe Experience Cloud Visual Editing Helper]-Erweiterung das `at_qa_mode`-Cookie während der QS über Vorschau-Links duplizierte. Beim manuellen Wechsel zwischen Vorschauindizes wurden mehrere Cookies mit domänenübergreifenden Konflikten erstellt, sodass Tester keine Varianten zuverlässig wechseln konnten. Dieses Verhalten wurde sogar außerhalb der Target-Benutzeroberfläche beobachtet und betraf sowohl interne als auch Client-Konten. Diese Fehlerbehebung stellt eine konsistente Cookie-Behandlung sicher, indem doppelte Einträge verhindert und der Domain-Umfang ausgerichtet wird. So kann die Variante nahtlos gewechselt werden, ohne dass eine manuelle Cookie-Bereinigung erforderlich ist. (TGT-53579)
* **Es wurde ein Problem behoben, bei dem das Klicken auf Elemente auf einer bestimmten Homepage zu Speicherlecks führte.** Kunden, die Aktivitäten auf dieser Homepage erstellen, haben bei der Interaktion mit Seitenelementen Speicherlecks festgestellt. Das Problem war mit überhöhten Konsolenwarnungen und zunehmender Speichernutzung in Unterframes verbunden, insbesondere im Zusammenhang mit falsch formatierten Srcset-Attributen. Die Speichernutzung bleibt jetzt während der Interaktion stabil. (TGT-53761)
* **Es wurde ein Problem behoben, bei dem der VEC abstürzte und beim Laden bestimmter Aktivitäten einen leeren Bildschirm anzeigte.** Kunden eines bestimmten Mandanten meldeten, dass der Editor bestimmte Aktivitäten nicht laden konnte. Der VEC blieb bei „Anwenden erster Änderungen“ hängen, bevor er abstürzte und einen leeren Bildschirm anzeigte. Der VEC lädt jetzt betroffene Aktivitäten ohne Fehler im aktualisierten Prozess zur Erstellung von Aktivitäten. (TGT-52932)
* **Es wurde ein Problem behoben, bei dem in der [!UICONTROL Manage Content] Leiste in [!UICONTROL Automated Personalization] Aktivitäten inkonsistente Positionsbeschriftungen angezeigt wurden.** Kunden meldeten, dass in der [!UICONTROL Manage Content]-Leiste auf den Registerkarten [!UICONTROL Experiences] und [!UICONTROL Offers] nicht übereinstimmende Standortnummern angezeigt wurden. (z. B. Standort 2 und Standort 4 in Erlebnissen und Standort 1 und Standort 2 in Angebot), selbst wenn nur zwei Standorte konfiguriert waren. Standortbeschriftungen sind jetzt konsistent und genau auf Änderungen abgebildet, was die Klarheit und Benutzerfreundlichkeit beim Erstellen von Aktivitäten verbessert. (TGT-52934)
* **Es wurde ein Problem behoben, bei dem Änderungen in VEC nach dem Speichern verloren gingen.** Kunden meldeten, dass nach dem Speichern einer Änderung in VEC die Seite aktualisiert und die Änderung auf die vorherige Version zurückgesetzt wurde. Dieses Problem führte dazu, dass die letzten Aktualisierungen verloren gingen, es sei denn, die gesamte Aktivität wurde sofort gespeichert. Änderungen bleiben nun nach dem Speichern korrekt erhalten und der Editor macht Änderungen nicht mehr unerwartet rückgängig, was ein zuverlässiges Erlebnis im Arbeitsablauf für die Erstellung von Aktivitäten gewährleistet. (TGT-53500)
* **Verbesserte Elementauswahl in Visual Experience Composer durch Anzeige des Elementtyps beim Bewegen und Auswählen des Mauszeigers.** Um die Benutzerfreundlichkeit während der Aktivitätserstellung zu verbessern, dekoriert der VEC jetzt HTML-Elemente mit ihrem Typ, wenn der Mauszeiger über sie bewegt oder sie ausgewählt werden. Diese Verbesserung hilft Kunden, die richtigen Elemente leichter zu identifizieren und auszuwählen. Ausgewählte Elemente werden farblich hervorgehoben, Elemente, auf die gezeigt wird, sind blau hervorgehoben. Der Elementtyp wird ebenfalls angezeigt, sodass der Kontext während der Bearbeitung klarer wird. (TGT-53502)

+++

## Datenstrom-Updates (19. September 2025)

Die Kombination aus Datenstrom-ID und Sandbox muss für [!DNL Adobe Target] Zielverbindungen eindeutig sein.

Die Validierungslogik für [!DNL Target] Zielverbindungen wurde aktualisiert, um zu erzwingen, dass die Kombination aus Datenstrom-ID und Sandbox-Name innerhalb einer IMS-Organisation eindeutig sein muss. Dies bedeutet:

* Dieselbe Datenstrom-ID und dasselbe Sandbox-Namenspaar können nicht über mehrere [!DNL Target] Zielverbindungen hinweg wiederverwendet werden.
* Dieselbe Datenstrom-ID kann nur für verschiedene Verbindungen verwendet werden, wenn sie in verschiedenen Sandboxes konfiguriert sind.
* Diese Regel gilt für alle ausgewählten Datenstrom, auch wenn „Keine“ ausgewählt ist.

Diese Aktualisierung stellt eine konsistente Konfiguration sicher und verhindert Konflikte in Multi-Sandbox-Umgebungen. Weitere Informationen finden Sie unter [Adobe Target-Verbindung](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} im *Experience Platform-Ziele* Handbuch.

## [!DNL Target Standard/Premium] 25.9.1 (5. September 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Experience Fragments]**

+++Details anzeigen
* **Verbesserte Benutzerzuordnung für [!UICONTROL AEM Experience Fragment] Angebote.** hat ein Problem in VEC behoben, bei dem im Feld &quot;[!UICONTROL Last updated]&quot; für [!UICONTROL AEM Experience Fragment] (XF) fälschlicherweise eine Code-ID anstelle des Benutzernamens angezeigt wurde. Diese Diskrepanz trat bei der Angebotsauswahl in der aktualisierten Benutzeroberfläche auf und führte zu Inkonsistenzen mit den alten Benutzeroberflächen- und HTML-Angeboten, die den Namen des letzten Editors korrekt anzeigten. Diese Fehlerbehebung stellt eine konsistente Benutzerzuordnung über alle Angebotstypen hinweg sicher und verbessert die Transparenz und Ausrichtung an dem erwarteten Verhalten. (TGT-52880 und TGT-52898)

+++

**Offer Decisioning**

+++Details anzeigen
* **Fehler bei der Angebotsentscheidung für ODE-Angebote behoben.** Es wurde ein Problem behoben, bei dem durch [!DNL Target] eingefügte ODE-Angebote (Offer Decisioning Engine) aufgrund fehlender Formatmetadaten einen 400-Fehler zurückgaben. Die Fehlermeldung deutete darauf hin, dass der MIME-Typ null war, was die erfolgreiche Verarbeitung von Angebotsentscheidungen verhinderte. Diese Fehlerbehebung stellt eine ordnungsgemäße Verarbeitung von Angebotsmetadaten sicher, stellt die Funktionalität für die Bereitstellung personalisierter Inhalte wieder her und ermöglicht die unterbrechungsfreie Ausführung von Marketing-Kampagnen. (TGT-53635)
* **Problem mit dem ODS-Angebotsrendering behoben.** Es wurde ein Problem behoben, bei dem über [!DNL Offer Decision Service] (AJO) erstellte [!DNL Adobe Journey Optimizer] (ODS)-Angebote nicht gerendert wurden, wenn Aktivitäten in der aktualisierten Benutzeroberfläche mit VEC erstellt wurden. Dieselbe Konfiguration funktionierte in der alten Benutzeroberfläche korrekt, was zu Verwirrung und zur blockierten Kampagnenausführung führte. Diese Fehlerbehebung stellt die konsistente Bereitstellung von Angeboten für beide Benutzeroberflächenversionen sicher und stellt das erwartete Verhalten für die AJO-gesteuerte Personalisierung wieder her.

+++

**Berichte**

+++Details anzeigen
* **Download-Option im Berichtabschnitt der aktualisierten Benutzeroberfläche für Berichte wiederhergestellt.** Es wurde ein Problem in der neuen Übersichts-Benutzeroberfläche behoben, bei dem die Schaltfläche [!UICONTROL Download] im Abschnitt Berichte fehlte, was Benutzer daran hinderte, Attributwertbewertungen zu exportieren. Diese Aktualisierung stellt die vollständige Exportfunktion wieder her und ermöglicht einen optimierten Zugriff auf herunterladbare Daten für Analysen und Berichte. (TGT-53222)
* **[!UICONTROL Download full CSV report]Schaltfläche wurde in der [!UICONTROL Important attributes] wiederhergestellt.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche zur Erstellung von Aktivitäten behoben, bei dem die Schaltfläche [!UICONTROL Download full CSV report] im Abschnitt [!UICONTROL Important Attributes] in der Berichtsansicht fehlte. Mit dieser Fehlerbehebung wird der Zugriff auf herunterladbare Einblicke wiederhergestellt, um sicherzustellen, dass die Funktionen der aktualisierten und der alten Benutzeroberfläche konsistent sind. (TGT-53238)
* **Gelöste UI-Probleme, die [!UICONTROL Auto Target] Reporting in der aktualisierten Übersichts-Benutzeroberfläche betreffen.** Es wurden mehrere UI-Probleme in der aktualisierten Übersichtsoberfläche behoben, die sich auf [!UICONTROL Auto Target] Aktivitätsberichte auswirkten. Zu diesen Fehlerbehebungen gehören:

   * Fehlende Steigerung- und Konfidenzmetriken in Zusammenfassungsberichten
   * Falsche Farbanzeige für das Kontrollkästchen „Modelle erstellt“
   * Nicht funktionaler Diagrammbericht trotz Datenvarianz in [!DNL Analytics]
   * Fehlender Downloadlink für [!UICONTROL Automated Segments] und [!UICONTROL Important Attributes] Berichte
   * Fehlerhafte [!UICONTROL Automated Segments] Berichtanzeige

  Diese Korrekturen stellen das erwartete Berichtsverhalten wieder her und verbessern die Sichtbarkeit der [!UICONTROL Auto Target] in der gesamten aktualisierten Benutzeroberfläche. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++Details anzeigen
* **Die Formularvalidierung wurde hinsichtlich der Parameterpräsenz-Bedingungen in der aktualisierten Benutzeroberfläche korrigiert.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Kunden bei Auswahl von &quot;[!UICONTROL Custom mbox parameter value is present]&quot; oder &quot;[!UICONTROL Parameter is present]&quot; fälschlicherweise einen Wert eingeben mussten. Dieses Verhalten steht im Konflikt mit der beabsichtigten Logik, die einfach prüft, ob ein Parameter unabhängig von seinem Wert vorhanden ist. Durch die Korrektur wird die Formularvalidierung an das erwartete Verhalten angepasst, was eine reibungslosere Einrichtung der Aktivitäten ermöglicht und die vollständige Übernahme der aktualisierten Benutzeroberfläche unterstützt. (TGT-53638)
* **Formularlogik wurde für Regeln zum Vorhandensein von Parametern im Seitenversand korrigiert.“** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Benutzende bei der Auswahl von Seitenbereitstellungsregeln wie &quot;[!UICONTROL Parameter is present]&quot;, &quot;[!UICONTROL Parameter is not present]&quot;, &quot;[!UICONTROL Parameter value is present]&quot; oder &quot;[!UICONTROL Parameter value is not present]&quot; fälschlicherweise einen zusätzlichen Parameterwert eingeben mussten. Dieses Verhalten war nicht konsistent mit der veralteten Benutzeroberfläche und widersprach der beabsichtigten Logik, das Vorhandensein von Parametern zu erkennen, ohne einen Wert anzugeben. Dieser Fix stellt das erwartete Regelkonfigurationsverhalten wieder her, optimiert die Aktivitätseinrichtung und verbessert die Benutzerfreundlichkeit. (TGT-53640)
* **Die Validierungslogik für den mehrseitigen Regel-Builder in der aktualisierten Benutzeroberfläche wurde verbessert.** Es wurden mehrere Validierungsprobleme im mehrseitigen Regel-Builder innerhalb der aktualisierten Benutzeroberfläche behoben. Zu diesen Fehlerbehebungen gehören:

   * Regelerstellung wird verhindert, wenn der mbox-Parameter leer ist
   * Anzeigen geeigneter Fehlermeldungen für ungültige Regelstatus
   * Korrigieren der Validierungslogik für unäre und parameterbasierte Operatoren, die keine Operandenwerte erfordern
   * Aktivieren von Hash-Fragmentregeln mit unären Operatoren durch Wiederherstellen der Speicherfunktion

  Diese Aktualisierungen stellen eine genaue Regelkonfiguration sicher und verbessern die Benutzerfreundlichkeit in komplexen Seitenbereitstellungsszenarien. (TGT-53722)
* **Problem mit dem Umbenennen des Speicherorts in A/B- und MVT-Aktivitäten behoben.** Es wurde ein Fehler in der aktualisierten Benutzeroberfläche behoben, durch den das Umbenennen eines Speicherorts in einer [!UICONTROL A/B Test]- oder [!UICONTROL Multivariate Test] (MVT)-Aktivität nach dem Navigieren zwischen der Standortliste, dem Targeting und zurück nicht beibehalten wurde. Durch diese Aktualisierung wird sichergestellt, dass Ortsnamenänderungen gespeichert und im gesamten Aktivitäts-Workflow konsistent übernommen werden. (TGT-52367)
* **Die Persistenz des Standortnamens für MVT- und AP-Aktivitäten in der aktualisierten Benutzeroberfläche wurde korrigiert.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem in [!UICONTROL Multivariate Test] (MVT)- und [!UICONTROL Automated Personalization] (AP)-Aktivitäten bearbeitete Ortsnamen nicht korrekt gespeichert wurden. Nach dem Umbenennen eines Speicherorts wurde durch das Navigieren zwischen Registerkarten wie [!UICONTROL Targeting] und [!UICONTROL Experiences] der vorherige Status der Namen wiederhergestellt. Diese Fehlerbehebung stellt eine konsistente Ortsbenennung auf allen Registerkarten sicher und verbessert die Zuverlässigkeit bei der Einrichtung der Aktivität. (TGT-52927)
* **Standortbeschriftung im Bedienfeld Erlebnisse verwalten für MVT-Aktivitäten korrigiert.** Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem das Bedienfeld [!UICONTROL Manage Experiences] in [!UICONTROL Multivariate Test] (MVT)-Aktivitäten eine inkonsistente Standortnummerierung anzeigte. Durch diese Korrektur wird sichergestellt, dass Standortbeschriftungen sequenziell sind und korrekt mit benutzerdefinierten Änderungen ausgerichtet werden, was die Klarheit und Benutzerfreundlichkeit während der Einrichtung des Erlebnisses verbessert. (TGT-52929)

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
