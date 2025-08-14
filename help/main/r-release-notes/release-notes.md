---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 1a5c47277bfd5eb1c90887728540bbc3b0433d77
workflow-type: tm+mt
source-wordcount: '3800'
ht-degree: 9%

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

## [!DNL Target Standard/Premium] 25.8.2 (14. August 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

**[!UICONTROL Activities]**

+++Details anzeigen
* **Problem beim Laden von Aktivitäten in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben**: Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem bestimmte Aktivitäten beim Versuch, sie zu bearbeiten, nicht geladen werden konnten. Dieses Problem führte dazu, dass Kundinnen und Kunden Benutzende in einem Bildschirm für das unbegrenzte Laden ließen. Dieses Problem wirkte sich auf mehrere Aktivitäten aus und wurde als inkonsistent über Kunden hinweg gemeldet. Mit dieser Fehlerbehebung werden die betroffenen Aktivitäten jetzt ordnungsgemäß geladen, was eine nahtlose Bearbeitung ermöglicht und Unterbrechungen der Aktivitäts-Workflows reduziert. (TGT-53209)
* **Fehler beim Speichern einer Aktivität im Erstellungsprozess aufgrund einer `optionLocalId` Validierung**: Es wurde ein Problem im Erstellungsprozess einer Aktivität behoben, das Kunden daran hinderte, Änderungen aufgrund eines Backend-Validierungsfehlers zu speichern: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Dieses Problem trat beim Ändern bestimmter Elemente innerhalb einer Aktivität auf, was zu einem fehlgeschlagenen Speichervorgang führte. Die Korrektur stellt sicher, dass `optionLocalId` Verweise jetzt korrekt validiert werden, sodass Kunden Aktivitäten speichern können, ohne diesen Fehler zu bemerken. (TGT-53293)
* **Absturz beim Erstellen von Aktivitäten behoben, der durch ungültige Optionsverweise beim Wechseln von Seiten verursacht wurde**: Es wurde ein Problem beim Erstellen von Aktivitäten behoben, das dazu führte, dass die Benutzeroberfläche nach dem dreimaligen Wechsel von Seiten während der Bearbeitung abstürzte. Der Absturz wurde durch ungültige Optionsverweise ausgelöst, was zu Konsolenfehlern führte, wie z. B. „Option mit localId &#39;7&#39; nicht gefunden.“ Mit diesem Update können Kunden jetzt zwischen Seiten wechseln und Änderungen vornehmen, ohne Systemfehler oder -unterbrechungen festzustellen. (TGT-53295)
* **Fehler beim Speichern in einem Prozess zur Erstellung von Aktivitäten, der durch ungültige Benutzereingaben beim Bearbeiten von Erlebnissen verursacht wurde**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden Änderungen an einer Aktivität aufgrund eines Fehlers bei der ungültigen Benutzereingabe nicht speichern konnten. Der Fehler trat beim Ändern von Erlebnissen in der aktualisierten Benutzeroberfläche auf und verhinderte, dass Aktualisierungen übergeben wurden. Die Aktivität kann jetzt erfolgreich gespeichert werden, sodass Kunden sie ohne Unterbrechung bearbeiten und veröffentlichen können. (TGT-53267)
* **Ladeproblem beim Erstellen von Aktivitäten, das die Bearbeitung in der aktualisierten Benutzeroberfläche blockiert hat**: Es wurde ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kunden aufgrund eines Bildschirms zum kontinuierlichen Laden keine Aktivitäten in der aktualisierten Benutzeroberfläche bearbeiten konnten. Kunden können jetzt Aktivitäten öffnen und ändern, ohne dass Ladefehler auftreten. (TGT-53415)
* **Problem mit Erlebnisanforderungen im Prozess zur Erstellung von Aktivitäten für AP-Aktivitäten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem [!UICONTROL Automated Personalization] (AP)-Aktivitäten in der aktualisierten Benutzeroberfläche zwei Standorte statt zwei Erlebnisse benötigten. Dieses Verhalten blockierte Anwendungsfälle, in denen Kunden einen einzelnen Standort mit mehreren Angeboten konfiguriert haben, was zuvor unterstützt wurde. Die Anforderung wurde entsprechend der ursprünglichen Funktionalität korrigiert, sodass Kundinnen und Kunden unabhängig von der Anzahl der Standorte mit AP-Aktivitäten mit zwei Erlebnissen fortfahren können. (TGT-53429)
* **Feldverhalten für getrackte Elemente im Klick-Tracking-Modus korrigiert, um nicht gespeicherte Eingaben zu verhindern und die Klarheit zu verbessern**: Es wurde ein Problem im Prozess zur Erstellung einer Aktivität behoben, bei dem das [!UICONTROL Tracked Element] Feld im [!DNL Click Track]-Modus bearbeitbar war, aber den eingegebenen Namen nicht beibehielt, was zu Verwirrung bei den Kunden führte. Das Feld ist jetzt deaktiviert, um nicht gespeicherte Eingaben zu verhindern, und die Benennung ausgewählter Elemente wurde klarer formuliert, um die Zielkonfiguration und die Tracking-Genauigkeit zu verbessern.** (TGT-53458)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das die Benennung von verfolgten Komponenten im [!UICONTROL Click Track]-Modus blockierte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Kunden verfolgte Komponenten im [!UICONTROL Click Track]-Modus nicht benennen konnten. Nach der Eingabe eines Namens erschien das Feld bearbeitbar, behielt jedoch die Eingabe nicht bei. Standardmäßig werden im Bearbeitungsmodus allgemeine Bezeichnungen wie „MEIN PRIMÄRES ZIEL 0“ verwendet. Das Feld Nachverfolgte Elemente ist jetzt deaktiviert. Das Benennungsverhalten wurde klarer formuliert, um die Zieleinrichtung und -nachverfolgbarkeit zu verbessern. (TGT-51396)

+++

**Experience Fragments (XFs)**

+++Details anzeigen
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, das eine unbeabsichtigte Bearbeitung von aus AEM exportierten Fragmenten durch HTML ermöglichte**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, durch das Kunden die aus [!DNL Experience Fragments] (AEM) exportierten HTML of [!DNL Adobe Experience Manager] (XFs) in [!DNL Target] bearbeiten konnten. Dieses Verhalten war unbeabsichtigt, da XFs nach der Veröffentlichung aus AEM für die Bearbeitung gesperrt bleiben sollten. Die Korrektur stellt sicher, dass die Option &quot;HTML bearbeiten“ für von AEM exportierte Fragmente nicht mehr verfügbar ist, wodurch die Inhaltsintegrität und die erwartete Governance erhalten bleiben. (TGT-53286)
* **Intermittierendes Vorschauproblem für XF-Inhalte im Prozess zur Erstellung von Aktivitäten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem XF-Inhalte intermittierend im Vorschaumodus in der aktualisierten Benutzeroberfläche nicht gerendert werden konnten. Obwohl der Inhalt korrekt bereitgestellt wurde, wurde die Vorschau nicht konsistent angezeigt, was es für Kunden schwierig machte, die Angebotseinrichtung zu validieren. XF-Vorschauen werden jetzt zuverlässig geladen, was die Konfidenz und Effizienz bei der Konfiguration von Aktivitäten verbessert. (TGT-53318)

+++

**QA-Modus**

+++Details anzeigen
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem führende Leerzeichen in URLs fehlerhafte QA-Links verursachten**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem führende Leerzeichen in der Aktivitäts-URL beim Speichern nicht ordnungsgemäß abgeschnitten wurden. Dies führte zu ungültigen QA-Links und falscher Formatierung im Backend. Nach der Aktualisierung werden die URLs jetzt sauber gespeichert, was fehlerhafte Links verhindert und die Zuverlässigkeit der QA-Workflows für Kunden verbessert. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen
* **Es wurde ein Problem in der Benutzeroberfläche für die Katalogsuche behoben, bei dem die erweiterte Suche keine Vorschläge bereitstellen konnte**: Es wurde ein Problem in der neuen [!UICONTROL Catalog Search]-Benutzeroberfläche behoben, bei dem die [!UICONTROL Advanced Search]-Funktion keine Vorschläge bereitstellen konnte. Die Benutzer mussten exakte Werte mit präziser Schreibweise eingeben, was die Suche umständlich und fehleranfällig machte. Mit dieser Fehlerbehebung bietet der [!UICONTROL Advanced Search] jetzt relevante Vorschläge, wie Benutzer tippen, die Benutzerfreundlichkeit verbessern und die Reibung beim Auffinden von Produkten reduzieren. (TGT-52008)
* **Es wurden mehrere UI- und Filterprobleme behoben, um die Reaktionsfähigkeit und die Entitätsinteraktion zu verbessern**: Es wurden mehrere Probleme behoben, darunter mangelhafte Reaktionsfähigkeit von Kriteriendetails auf Geräten mit kleinem Bildschirm, fehlende Ergebnisse bei der Auswahl von „Alle Hostgruppen“ im Umgebungsfilter und die Unfähigkeit, mit Entitäten ohne Namen zu interagieren. Diese Korrekturen verbessern die Benutzerfreundlichkeit über Bildschirmgrößen hinweg, stellen eine genaue Filterung sicher und ermöglichen eine vollständige Interaktion mit allen Produktentitäten, was das Gesamterlebnis für Benutzende verbessert. (TGT-52992)
* **Fehlende Produkt-IDs in der Detailansicht von Recommendations bei der Erstellung von Aktivitäten wurden behoben**: Es wurde ein Problem im Prozess zur Erstellung von [!DNL Recommendations]-Aktivitäten behoben, bei dem Produkt-IDs im Bildschirm mit den Produktdetails fehlten, was es Kunden erschwerte, Produkt-IDs während Workflows zu kopieren oder zu referenzieren. Die Produkt-IDs werden jetzt klar in der Detailansicht angezeigt, was die Sichtbarkeit verbessert und eine effizientere Produktverwaltung für Kunden unterstützt. (TGT-51964)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Produktnachrichten nicht in der Recommendations-Ansicht angezeigt wurden**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem in der [!UICONTROL Message] in der [!DNL Recommendations]-Ansicht keine Produktdaten angezeigt wurden, obwohl Nachrichten vorhanden waren. Kunden mussten die Spalte manuell entfernen und erneut hinzufügen, um den Inhalt vorübergehend anzuzeigen, der beim Scrollen oder Suchen oft wieder verschwand. Diese Aktualisierung stellt die konsistente Sichtbarkeit von Produktnachrichten wieder her und verbessert die Katalognavigation und die Überprüfungs-Workflows. (TGT-52777)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem bei Auswahl von „Alle Hostgruppen“ in der Recommendations-Ansicht keine Ergebnisse zurückgegeben wurden**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem bei Auswahl der Umgebung „Alle Hostgruppen“ in der [!DNL Recommendations]-Ansicht keine Ergebnisse zurückgegeben wurden. Kunden können jetzt Produktdaten wie erwartet über alle Hostgruppen hinweg anzeigen und so die Sichtbarkeit und Filtergenauigkeit während der Einrichtung der Aktivität verbessern. (TGT-53006)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem der Umschalter für die vordere Promotion nach dem Speichern nicht beibehalten wurde**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem das Deaktivieren des Umschalters für die vordere Promotion in den Aktivitätseinstellungen nach dem Speichern nicht beibehalten wurde. Kunden, die versuchten, die Frontend-Promotion zu entfernen, sahen den Umschalter nach einem erneuten Besuch der Aktivität wieder aktiviert, was eine ordnungsgemäße Anpassung verhinderte. Diese Aktualisierung ermöglicht ein zuverlässiges Speichern von Änderungen, sodass Kunden die volle Kontrolle über die Promotioneinstellungen haben. (TGT-53215)
* **Inkonsistente Sortierung nach [!UICONTROL Last Updated] Spalte korrigiert:** Fehlerkorrektur - Beim Erstellen von Aktivitäten wird der Katalog jetzt nicht mehr nach der [!UICONTROL Last updated] Spalte sortiert, was zu inkonsistenten Ergebnissen führt. Kunden waren nicht in der Lage, Produktdaten basierend auf Aktualisierungszeitstempeln zuverlässig zu organisieren, was die Überprüfung und Verwaltung von Katalogen erschwerte. Die Sortierung funktioniert jetzt erwartungsgemäß und verbessert die Genauigkeit und Benutzerfreundlichkeit in der aktualisierten Benutzeroberfläche. (TGT-53116)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen
* **Probleme beim Laden der Aktivität und beim [!UICONTROL Cancel] von Schaltflächen im Prozess zur Erstellung einer Aktivität behoben**: Es wurde ein Problem im Prozess zur Erstellung einer Aktivität behoben, bei dem bestimmte Aktivitäten nicht geladen werden konnten, sodass Kunden nicht auf Änderungen zugreifen konnten. Darüber hinaus reagierte die Schaltfläche [!UICONTROL Cancel] nicht, was Kunden daran hinderte, den Ladevorgang zu stoppen oder die Bearbeitungsansicht zu verlassen. Durch diese Fehlerbehebung wird sichergestellt, dass -Aktivitäten jetzt zuverlässig geladen werden und die [!UICONTROL Cancel]-Schaltfläche erwartungsgemäß funktioniert, was die Gesamtstabilität und das Benutzererlebnis in Visual Experience Composer verbessert. (VEC)(TGT-53218)
* **Problem beim Wechsel von Erlebnissen in der aktualisierten VEC-Benutzeroberfläche behoben, das die Bearbeitung blockiert und [!UICONTROL Cancel] Schaltfläche deaktiviert hat**: Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem Änderungen beim Wechsel zwischen Erlebnissen in einer Experience Targeting-(XT)-Aktivität nicht geladen werden konnten. Kunden konnten keine Erlebnisse bearbeiten, die über die ursprünglich eingegebene hinausgingen, und die Schaltfläche [!UICONTROL Cancel] fehlte oder reagierte nicht. Diese Fehlerbehebung stellt sicher, dass Änderungen jetzt in allen Erlebnissen korrekt geladen werden und dass die Schaltfläche &quot;[!UICONTROL Cancel]&quot; auch ohne die Helper-Erweiterung zuverlässig funktioniert, was die Bearbeitungs-Workflows verbessert und Frustrationen reduziert. (TGT-53256)
* **Problem mit weißem Bildschirm beim Wechsel zwischen mehreren Erlebnissen im Prozess zur Erstellung einer Aktivität behoben**: Es wurde ein Problem behoben, bei dem das Wechseln zwischen mehreren Erlebnissen zu einem weißen Bildschirm führte. Es wurde auch ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kunden auf einen weißen Bildschirm stießen, wenn sie versuchten, mehrere Erlebnisse innerhalb einer Aktivität zu ändern. Dieses Problem trat auf, nachdem Änderungen auf zwei Erlebnisse angewendet und dann ein drittes Erlebnis ausgewählt wurden, wodurch weitere Bearbeitungen verhindert wurden. Die Aktualisierung sorgt für einen reibungslosen Übergang zwischen Erlebnissen, sodass Kunden Änderungen ohne Unterbrechung vornehmen können. (TGT-53266)
* **Es wurde ein Problem in VEC behoben, bei dem benutzerdefinierte Code-Änderungen über Bearbeitungssitzungen hinweg nicht zuverlässig gespeichert wurden**: Es wurde ein Problem behoben, bei dem benutzerdefinierte Code-Änderungen, die in Visual Experience Composer (VEC) vorgenommen wurden, nicht zuverlässig in einem einzigen Versuch gespeichert wurden. Kunden meldeten, dass Änderungen wie Stilaktualisierungen oder HTML-Bearbeitungen zeitweise auf der Website und in den QA-URLs fehlten, selbst nachdem sie sowohl die [!UICONTROL Edit Content]- als auch die endgültige [!UICONTROL Save]-Schaltfläche verwendet hatten. Diese Regression wurde behoben, sodass alle benutzerdefinierten Code-Änderungen über Bearbeitungssitzungen hinweg wie erwartet bestehen bleiben.** (TGT-53418)
* **Fehlende `triggerViews` in der aktualisierten Benutzeroberfläche während der Aktivitätserstellung wurden behoben**: Es wurde ein Problem im Prozess zur Aktivitätserstellung behoben, bei dem `triggerViews` nicht in der aktualisierten Benutzeroberfläche angezeigt wurden, obwohl sie auf der Seite korrekt implementiert waren. Dies wirkte sich auf mehrere Kunden aus und erschwerte die Validierung ansichtsbasierter Trigger während der Aktivitätseinrichtung. `TriggerViews` werden nun erwartungsgemäß angezeigt, sodass Kundinnen und Kunden ihre Konfigurationen zuverlässig abschließen und testen können. (TGT-53239)
* **Problem beim Laden von Ansichten im Prozess zur Erstellung von Aktivitäten für bestimmte Web-Seiten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Ansichten in der aktualisierten Benutzeroberfläche für bestimmte Web-Seiten nicht geladen wurden, obwohl sie korrekt implementiert und in Versand- oder Interaktionsaufrufen sichtbar waren. Dies wirkte sich auf mehrere Kunden aus und erschwerte die Validierung des ansichtsbasierten Targeting. Ansichten werden jetzt konsistent auf allen unterstützten Seiten angezeigt, was die Zuverlässigkeit bei der Einrichtung von Aktivitäten verbessert. (TGT-53246)
* **Problem beim zeitweisen Laden von Ansichten im Prozess zur Erstellung von Aktivitäten in der aktualisierten Benutzeroberfläche behoben**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem Ansichten während der Aktivitätsbearbeitung zeitweise nicht in der aktualisierten Benutzeroberfläche angezeigt wurden. Obwohl der richtige Ansichtsname in der Netzwerk-Payload vorhanden war, wurde er in der Benutzeroberfläche nicht konsistent erkannt, was sich auf die Möglichkeit von Kundinnen und Kunden auswirkte, die ansichtsbasierte Personalisierung zu konfigurieren. Ansichten werden jetzt zuverlässig angezeigt und unterstützen eine reibungslosere Einrichtung und Validierungs-Workflows. (TGT-53223)
* **Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem verfolgte Aktionsnamen nicht in der aktualisierten Benutzeroberfläche gespeichert wurden**: Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem verfolgte Aktionsmetriken nicht in der aktualisierten Benutzeroberfläche gespeichert werden konnten. Nachdem ein getracktes Element benannt und die Aktivität gespeichert wurde, wurde der Name beim erneuten Öffnen auf eine Standardbeschriftung zurückgesetzt, was zu Verwirrung führte und die Zielkonfiguration unterbrach. Nachverfolgte Aktionen behalten jetzt ihre zugewiesenen Namen bei, sodass Kundinnen und Kunden Konversionsmetriken genau festlegen und verwalten können. (TGT-53453)

+++

## [!DNL Target Standard/Premium] 25.8.1 (7. August 2025)

Dieses Release umfasst die folgenden Erweiterungen und Fehlerbehebungen:

**Aktivitäten**

+++Details anzeigen
* Es wurden mehrere Probleme mit der aktualisierten Benutzeroberfläche behoben, darunter Fehler beim Löschen von Seitentypen aufgrund von Abständen in Eingabewerten, unzuverlässigen Aktivitätskopien zwischen Arbeitsbereichen und fehlerhaften Seitenbereitstellungsregeln in QS-Umgebungen. (TGT-52703)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Benutzende mit der Rolle [!UICONTROL Editor] auf Live-Aktivitäten zugreifen und versuchen konnten, sie zu bearbeiten. Dies sollte eingeschränkt werden. In der Aktivitätsliste und den Übersichtsbildschirmen werden Bearbeitungsoptionen für Live-Aktivitäten fälschlicherweise angezeigt, was zu potenziellen unbeabsichtigten Änderungen führt. (TGT-53055)
* Es wurde ein Problem in der [!UICONTROL Advanced Search]-Benutzeroberfläche behoben, bei dem Benutzer bei Auswahl der Operatoren „Wert ist vorhanden“ oder „Wert ist nicht vorhanden“ aufgefordert wurden, einen Operanden einzugeben, der für diese Bedingungen nicht erforderlich sein sollte. (TGT-51961)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Versuche, Aktivitäten aus dem Staging in den Produktionsarbeitsbereich zu kopieren, durchgängig fehlgeschlagen sind, selbst in Sandbox-Umgebungen. Kunden stießen auf verschiedene Fehlermeldungen, darunter „Anonyme Zielgruppe bereits von der Aktivität verwendet“ und „Ungültige Zielgruppen-ID“, obwohl sie gültige Konfigurationen verwendeten und über geeignete Arbeitsbereich-Berechtigungen verfügten. (TGT-52394)

+++

**Experience Fragments (XFs)**

+++Details anzeigen
* Es wurde ein Problem behoben, bei dem Experience Fragment (XF)-Inhalte in der [!UICONTROL Visual Experience Composer] (VEC)-Vorschau nicht gerendert werden können, obwohl sie in der Inhaltsbereitstellung ordnungsgemäß funktionieren. (TGT-53318)

+++

**Lokalisierung**

+++Details anzeigen
* Es wurde ein Lokalisierungsproblem behoben, bei dem die Schaltfläche „Promotion hinzufügen“ im Abschnitt „Promotions“ in mehreren Sprachumgebungen im QA-Mandanten nicht lokalisiert erschien. (TGT-53263)

+++

**Angebote**

+++Details anzeigen
* Es wurde ein Problem behoben, durch das beim Bearbeiten eines vorhandenen HTML-Angebots über Visual Experience Composer (VEC) alle Änderungen aus der Inhaltsbereitstellung entfernt wurden. Die Änderungen werden auf der Registerkarte Änderung ausgegraut angezeigt und werden in der QS-Vorschau nicht angezeigt, obwohl sie in der alten Benutzeroberfläche korrekt angewendet wurden. (TGT-52863)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Änderungen an HTML-Angeboten, die im [!UICONTROL Visual Experience Composer] (VEC) vorgenommen wurden, nach der Navigation von der Registerkarte [!UICONTROL Targeting] zurück zu [!UICONTROL Experiences] nicht beibehalten wurden. (TGT-52874)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem das Einfügen eines HTML-Angebots vor und eines anderen nach demselben Selektor zu einer falschen Speicherortgenerierung führte. Als Kunden von der Registerkarte [!UICONTROL Targeting] zur Registerkarte [!UICONTROL Experience] zurückkehrten, wurde nur ein Selektor beibehalten, was zu Änderungen und einer fehlerhaften Bereitstellung des Inhalts führte. Dieses Verhalten unterschied sich von dem der alten Benutzeroberfläche, die beide Änderungen mit unterschiedlichen Standortkennungen korrekt beibehielt. (TGT-52891)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem durch Klicken auf ein hinzugefügtes Angebot in der [!UICONTROL Modifications] Leiste das Bedienfeld [!UICONTROL Configuration] der rechten Seite gelegentlich angezeigt und ausgeblendet wurde, sodass es schwierig war, mit den Angebotseinstellungen zu interagieren. (TGT-53288)
* Es wurde ein Problem behoben, bei dem HTML-Angebote, die zu zielgruppenspezifischen Varianten innerhalb einer Aktivität hinzugefügt wurden, nicht konsistent gespeichert wurden oder im Änderungsabschnitt angezeigt wurden. Nachdem während der Bearbeitung zwischen Audiences gewechselt wurde, waren zuvor angewendete Angebote manchmal verschwunden oder konnten nicht gerendert werden, wodurch die Validierung unterbrochen und die Bereitschaft für Aktivitäten verzögert wurde. (TGT-53440)
* Es wurde ein Problem behoben, bei dem das Kopieren einer Aktivität, die Angebote enthielt, dazu führte, dass in der neuen Aktivität doppelte Angebote erstellt wurden. Dieses Verhalten verursachte unnötige Unübersichtlichkeit und Verwirrung, insbesondere beim Verschieben von Aktivitäten zwischen Arbeitsbereichen. Die Korrektur stellt sicher, dass [!DNL Target] Angebote jetzt korrekt und ohne Duplizierung in den Zielarbeitsbereich kopiert werden, was die Aktivitätsverwaltung optimiert und die Workflow-Effizienz verbessert. (TGT-53454)

+++

**Single Page Applications (SPAs)**

+++Details anzeigen
* Es wurde ein Problem im aktualisierten VEC behoben, das Kunden daran hinderte, Änderungen an [!UICONTROL Single Page Application] (SPA)-Ansichten anzuwenden. Während Aktivitäten, die in der alten Benutzeroberfläche erstellt wurden, ansichtsspezifisches Targeting unterstützten, konnte die neue Benutzeroberfläche Änderungen an diesen Ansichten nicht erkennen oder zulassen, wobei die Steuerelemente zum Umschalten der Ansicht deaktiviert wurden. (TGT-52556)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen
* Es wurde ein Problem behoben, bei dem Änderungen an Erlebnissen, die in der [!UICONTROL Visual Experience Composer] vorgenommen wurden, entweder nicht sichtbar waren oder in der Benutzeroberfläche inkonsistent erschienen. (TGT-TGT-53381)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem im [!UICONTROL Manage Content] Abschnitt kein Alternativtext für Erlebnisminiaturansichten angezeigt wurde. Dieses Problem machte es für Benutzende schwierig, Dokumente zu identifizieren, insbesondere wenn Dateinamen lang oder abgeschnitten waren. (TGT-52291)
* Es wurde ein Fehler behoben, bei dem Kunden beim Konfigurieren von [!UICONTROL page delivery] in VEC-Aktivitäten auf falsche Validierungsfehler stießen. Insbesondere wurde bei Operatoren wie „ist gleich eines von“ und „ist nicht gleich eines von“ die Auslösung „Ungültige Eingabe für den Operatortyp“ bei der Eingabe von Textwerten ausgelöst, obwohl Text unterstützt werden sollte. (TGT-52629)
* Es wurden mehrere Probleme behoben, die zu einem inkonsistenten Verhalten im [!UICONTROL Modifications] Bereich der aktualisierten Benutzeroberfläche führten, wenn Angebote mit der Schaltfläche „Angebot auswählen“ ausgewählt wurden. Statt das vorhandene Angebot zu ersetzen, hat die Benutzeroberfläche ein Duplikat hinzugefügt und versucht, mit beiden Angeboten zu interagieren, was zu Konsolenfehlern führte, z. B. `selectorNotFound`. Darüber hinaus wird bei einigen Angeboten nicht die Schaltfläche „Angebot auswählen“ angezeigt, sondern nur bearbeitbare Eigenschaften. (TGT-53321)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem HTML-Code-Änderungen, die während der Aktivitätseinrichtung vorgenommen wurden, nicht auf Variantenseiten beibehalten wurden, obwohl sie für Kontrollgruppen korrekt gespeichert wurden. Trotz mehrfacher Versuche und der Neuerstellung von Tests ohne Seitengruppierungen konnten die Variantenseiten durchgängig keine Änderungen beibehalten, was sich auf die Inhaltsbereitstellung und die QS-Validierung auswirkte. (TGT-53436)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem der Operator „ist gleich eines von“ in Seitenbereitstellungsregeln Eingabewerte nicht akzeptieren konnte. Bei der Konfiguration von Kundenparametern für alle Mboxes führte die Auswahl dieses Operators zu einem Fehler „Ungültige Eingabe“, was die Erstellung von Regeln verhinderte. (TGT-52623)

+++

**Arbeitsbereiche**

+++Details anzeigen
* Der Arbeitsablauf beim Kopieren von Aktivitäten zwischen Arbeitsbereichen wurde verbessert. Das Kopieren von Aktivitäten zwischen Arbeitsbereichen führte aufgrund fehlender Zielgruppen und nicht zugewiesener Eigenschaften zu Synchronisierungsfehlern. Dieses Update führt einen intelligenteren, intuitiveren Workflow ein, der sicherstellt, dass kopierte Aktivitäten ordnungsgemäß konfiguriert und für die Veröffentlichung bereit sind. (TGT-47094)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden aufgrund eines Fehlers in der `copyActivityBatchOperations`-Mutation keine Aktivitäten zwischen Arbeitsbereichen kopieren konnten. Der Versuch, Aktivitäten zu duplizieren, führte zu einem Server-Fehler (500) und einer Null-Antwort-Payload. (TGT-52405)
* Es wurde ein Problem behoben, bei dem Aktivitäten nicht synchronisiert werden konnten, wenn Angebote, auf die in der Konfiguration verwiesen wurde, im ausgewählten Arbeitsbereich nicht zugänglich waren. Dies führte zu Veröffentlichungsfehlern und ließ Aktivitäten in einem fehlgeschlagenen Status zurück. (TGT-52535)
* Fehlerkorrektur - Beim Kopieren von Aktivitäten zwischen Arbeitsbereichen in der aktualisierten [!DNL Target]-Benutzeroberfläche treten jetzt keine Fehler mehr auf. Kunden stießen auf Fehler im Zusammenhang mit dem Zielgruppenzugriff, insbesondere bei Live-Aktivitäten, und der falschen Berechtigungsprüfung, selbst wenn die Benutzenden sowohl in Quell- als auch in Ziel-Arbeitsbereichen &quot;[!UICONTROL Approver]&quot;-Rollen hatten. (TGT-53002)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem das Kopieren von Aktivitäten innerhalb desselben Arbeitsbereichs unnötig die zugehörigen Angebote und Zielgruppen duplizierte. (TGT-53457)
* Es wurde ein Problem behoben, um Fälle zu beheben, in denen Ad-hoc- (anonyme) Zielgruppen nicht korrekt zwischen nicht standardmäßigen Arbeitsbereichen oder von nicht standardmäßigen in standardmäßige Arbeitsbereiche kopiert wurden. Während frühere Aktualisierungen eine ordnungsgemäße Duplizierung für Szenarien mit Standardeinstellungen sowie Szenarien mit identischem Arbeitsbereich sicherstellten, konzentrierte sich diese Verbesserung auf die Beibehaltung kombinierter Zielgruppenkonfigurationen, die mehrere Arbeitsbereiche umfassen. Die Korrektur stellt ein konsistentes Zielgruppenverhalten und eine genaue Zielgruppenbestimmung über alle Arbeitsbereich-Transitionen hinweg sicher. (TGT-53268)

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
