---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e612ec5814c931349699b6b4d2c9fa71b493413c
workflow-type: tm+mt
source-wordcount: '2594'
ht-degree: 13%

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
* **Bearbeiten vorhandener Aktivitäten**: Änderungen an vorhandenen Aktivitäten (die ursprünglich in der veralteten Benutzeroberfläche erstellt wurden), während die aktualisierte Benutzeroberfläche verwendet wird, werden auf Ihrer Website veröffentlicht. Diese Aktualisierungen werden jedoch nicht in der alten Benutzeroberfläche angezeigt, wenn Sie zurückwechseln. Nur die letzten Aktualisierungen, die von der alten Benutzeroberfläche vorgenommen wurden, werden dort angezeigt.
* **Konsistenz der Aktivitätsdetails**: Die neuesten Änderungen werden unabhängig von der verwendeten Benutzeroberfläche auf Ihrer Live-Website angezeigt. In der veralteten Benutzeroberfläche werden jedoch nur die neuesten Änderungen angezeigt, die in dieser Version vorgenommen wurden. Dies kann verwirrend sein, wenn die in der aktualisierten Benutzeroberfläche bearbeiteten Aktivitäten anders aussehen als die in der alten Benutzeroberfläche.

#### Weitere Ressourcen zu Informationen über die aktualisierte Benutzeroberfläche

* [[!DNL Target] Häufig gestellte Fragen zur Aktualisierung der Benutzeroberfläche](/help/main/c-intro/updated-ui-faq.md): In dieser häufig gestellten Frage werden häufige Fragen zur neuen [!DNL Target]-Benutzeroberfläche und -[!UICONTROL Visual Experience Composer] (VEC) behandelt, einschließlich Navigationsänderungen, Funktionsspeicherorte und der Einstellung des Umschalters für die temporäre Benutzeroberfläche. Unabhängig davon, ob Sie Marketing-Experte, Entwickler oder Administrator sind, hilft Ihnen diese häufig gestellte Frage dabei, den Übergang reibungslos zu gestalten und die aktualisierte Benutzeroberfläche optimal zu nutzen.
* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für [!UICONTROL Activities], [!UICONTROL Recommendations] und den [!UICONTROL Visual Experience Composer] (VEC).
* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für die [!UICONTROL Offers Library].
* [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md): Bietet einen kurzen Überblick, der Ihnen hilft, sich mit [!DNL Target] vertraut zu machen, und enthält Links für detailliertere Informationen und schrittweise Anweisungen.
* [[!UICONTROL Visual Experience Composer] Änderungen](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der alten und der aktualisierten Version des VEC erläutert.
* [[!UICONTROL Visual Experience Composer] Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): In diesem Artikel werden die aktualisierte VEC-Benutzeroberfläche und ihre Optionen erläutert.

+++

## [!DNL Target Standard/Premium] 25.7.1 (Samstag, 11. Juli 2025)

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, enthält diese Version die folgenden Fehlerbehebungen und Aktualisierungen:

**Aktivitäten**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem die [!UICONTROL Activity QA]-URL einen unnötigen Abfrageparameter enthielt: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* Es wurde ein Problem behoben, bei dem Vorschau-URLs fälschlicherweise zusätzliche Zielgruppen enthielten, die über die vom Benutzer explizit eingegebene hinausgingen. Dieses Verhalten wurde korrigiert, um sicherzustellen, dass beim Generieren eines QA- oder Vorschau-Links nur die angegebene Zielgruppe angewendet wird. (TGT-52912)
* Ein Problem wurde behoben, das dazu führte, dass Benutzer keine [!UICONTROL Auto-Target] (AT)-Aktivitäten erstellen konnten, wenn bei der Einrichtung der Traffic-Zuordnung zuerst [!UICONTROL Auto-Allocate] (AA) ausgewählt wurde. Dieses Problem führte zu einem Backend-Validierungsfehler und verhindert, dass die Aktivität gespeichert wird. (TGT-53096)

+++

**Zielgruppen**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem Benutzende mit der Rolle [!UICONTROL Approver] keine Zielgruppenverfeinerungen nur für Aktivitäten hinzufügen oder speichern konnten. Der Versuch, dies zu tun, führte zu einem 403-Fehler (Forbidden) und gab an, dass die Berechtigung &quot;[editor]&quot; erforderlich war, obwohl der Benutzer über ausreichende Berechtigungen zum Genehmigen und Verwalten von Aktivitäten verfügte. (TGT-52984)
* Fehlerkorrektur - Wenn eine aktivitätsspezifische Zielgruppe mithilfe der Option [!UICONTROL Remove Audience Refinement] entfernt wird, wird die Zielgruppe nicht mehr in der Liste der Zielgruppen für die erneute Auswahl innerhalb derselben Aktivität angezeigt. Dieses Verhalten verhinderte, dass Benutzer dieselbe Zielgruppe erneut hinzufügen konnten, es sei denn, sie wurde von Grund auf neu erstellt. (TGT-52979)
* Es wurde ein Problem behoben, bei dem Zielgruppenverfeinerungen nur für Aktivitäten sofort aus der Benutzeroberfläche verschwanden, nachdem sie von einem Speicherort entfernt wurden, noch bevor die Aktivität gespeichert wurde. Dieses Verhalten stand im Widerspruch zu den erwarteten Funktionen und der QuickInfo-Anleitung, in der es heißt: „Alle nicht verwendeten Zielgruppen aus dieser Bibliothek werden gelöscht, sobald die Aktivität gespeichert wurde.“ (TGT-52982)
* Fehlerkorrektur - Jetzt wird nicht mehr versucht, einer Aktivität eine andere Zielgruppe als [!UICONTROL All Visitors] zuzuweisen. Beim Speichern wird die folgende Fehlermeldung angezeigt: „Wir können Ihre Anfrage nicht abschließen. Bitte [!UICONTROL Adobe Client Care] kontaktieren, wenn das Problem weiterhin besteht.“ (TGT-53008)
* Fehlerkorrektur - Das Speichern einer Aktivität nach dem Erstellen und Zuweisen einer neuen Zielgruppe im Aktivitätseditor wird jetzt problemlos möglich sein. Die folgende Fehlermeldung wurde angezeigt: „Wir können Ihre Anfrage nicht abschließen. Bitte kontaktieren Sie [!UICONTROL Adobe Client Care], wenn das Problem weiterhin besteht.“ (TGT-52977)

+++

**[!UICONTROL Analytics for Target](A4T)**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem das Kopieren einer vorhandenen Aktivität und das Ändern der Berichtsquelle in [!DNL Adobe Analytics] (A4T) zu einem Fehler „Ungültige Benutzereingabe“ führte. Der Fehler wurde ausgelöst, wenn bestimmte Metrikaktionen, die mit [!DNL Analytics] Reporting nicht kompatibel sind, wie `restart_same_experience`, `restart_random_experience` und `restart_new_experience`, von der ursprünglichen Aktivität beibehalten wurden. (TGT-52900)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine Aktivität zu erstellen oder zu speichern, wenn sie im [!DNL Adobe Analytics] Schritt [!UICONTROL Goals & Settings] (A4T) als Berichtsquelle auswählten. Das Problem trat speziell bei der Auswahl einer [!UICONTROL Custom Event]-Metrik auf (z. B. „Benutzerspezifisches Ereignis 16„), was zu folgendem Fehler führte: „Ungültige Benutzereingabe“. (TGT-52910)
* Es wurde ein Problem behoben, bei dem Benutzer durch Klicken auf den Link &quot;[!UICONTROL View in Analytics]&quot; auf die Homepage anstelle des vorgesehenen [!DNL Analytics]-Dashboards umgeleitet wurden. (TGT-53092 und TGT-53093)
  <!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* Ein Problem wurde behoben, dass dazu führte, dass beim Anzeigen einer [!DNL Recommendations] -Aktivität in der aktualisierten [!UICONTROL Overview]-Benutzeroberfläche der [!UICONTROL Goals & Settings]-Abschnitt nicht geladen wurde, wenn [!DNL Adobe Analytics] (A4T) als Berichtsquelle ausgewählt wurde. Die folgende Fehlermeldung wurde angezeigt: „Irgendetwas ist schiefgelaufen. Wir können Ihre Anfrage nicht bearbeiten. Wenden Sie sich an den Kundendienst von Adobe, wenn das Problem weiterhin besteht.“ (TGT-52999)

+++

**[!UICONTROL Experiences]und[!UICONTROL Offers]**

+++Details anzeigen
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* Es wurde ein Problem behoben, bei dem die [!UICONTROL Manage Content]-Funktion den Status eines Speicherorts nicht ordnungsgemäß validierte, nachdem alle Inhaltsoptionen entfernt wurden. Dies kann zu inkonsistentem Verhalten oder Fehlern beim Speichern oder Fortsetzen der Aktivitätskonfiguration führen. (TGT-52801)
* Es wurde ein Problem behoben, bei dem Benutzende auf den Fehler „Ungültige Eingabe“ stießen, wenn eine neue Seite hinzugefügt und bestimmte Elemente in verschiedenen Erlebnissen gelöscht wurden. Der Fehler wurde durch doppelte `LocalIds` ausgelöst, die während der Elementbearbeitung generiert wurden, insbesondere beim Wechseln zwischen Erlebnissen und beim Ändern freigegebener Seitenstrukturen. (TGT-52720)
* Es wurde ein Problem behoben, bei dem die Verwendung der [!UICONTROL Generate Adhoc Offer]-Funktion dazu führte, dass undefinierte Positionen im [!UICONTROL Manage Content] angezeigt wurden. (TGT-53076 und TGT-53070)
* Das Verhalten für den Kunden klargestellt, bei dem Änderungen, die mithilfe eines HTML-Angebots vorgenommen wurden, fehlen könnten, wenn vom [!UICONTROL Targeting] Schritt zurück zum [!UICONTROL Experiences] navigiert wird. Für diesen Kunden generierte die betroffene Website dynamisch mehrere DOM-Selektoren, die sich mit jedem Laden der Seite änderten. Daher kann der ursprünglich für die Änderung verwendete Selektor beim erneuten Öffnen des Editors nicht gefunden werden, was dazu führt, dass die Änderung fehlt oder ungültig ist. Dies funktioniert wie vorgesehen. Um sicherzustellen, dass Änderungen visuell im Editor bestehen bleiben, wird empfohlen, dass Clients stabile, konsistente Selektoren verwenden, die sich nicht über Seitenneuladungen hinweg ändern. (TGT-52874)
* Es wurde ein Problem behoben, bei dem der Versuch, ein Angebot zu löschen oder zu deaktivieren, das Teil eines ausgeschlossenen Erlebnisses war, den Fehler „Ungültige Benutzereingabe“ auslöste. Dieses Problem trat auf, obwohl das Angebot in den eingeschlossenen Erlebnissen nicht aktiv verwendet wurde. (TGT-52917)

+++

**Formularbasierter Experience Composer**

+++Siehe Details
* Es wurde ein Problem in formularbasierten Aktivitäten behoben, bei dem das Duplizieren eines Erlebnisses und das Bearbeiten des benutzerdefinierten Codes in einem der duplizierten Erlebnisse diese Änderungen unbeabsichtigt auf alle duplizierten Erlebnisse anwenden würden. Jedes Erlebnis behält nun nach der Duplizierung seinen eigenen benutzerdefinierten Code unabhängig bei. (TGT-51600)

+++

**Lokalisierung**

+++Siehe Details
* Aktualisierte Lokalisierungszeichenfolgen in der neuen Benutzeroberfläche für Französisch (fr_FR), Deutsch (de_DE), Italienisch (it_IT), Koreanisch (ko_KO) und vereinfachtes Chinesisch (zh_CN).

+++

**[!DNL Recommendations]**

+++Siehe Details
* Ein neuer [!DNL Recommendations]-Feed [Status](/help/main/c-recommendations/c-products/feeds.md#status) wurde hinzugefügt: [!UICONTROL Partial Import Failed]. (KB-2215)
* Fehlerkorrektur - Der Workflow zum Erstellen von Aktivitäten beim Hinzufügen von [!DNL Recommendations] mit [!UICONTROL promotions] funktioniert jetzt fehlerfrei. Wenn Benutzende &quot;[!UICONTROL Promote by Attribute]&quot; ausgewählt und eine Filterregel hinzugefügt haben (z. B. [!UICONTROL Parameter Matching]), wurden der ausgewählte Regeltyp und die ausgewählten Operandenwerte nach dem Speichern und erneuten Bearbeiten der Aktivität nicht beibehalten. Beim erneuten Öffnen würde sich der Filterregeltyp unerwartet ändern und Operandenwerte fehlen. (TGT-53059)
* Es wurde ein Problem in der [!DNL Recommendations]-Benutzeroberfläche behoben, bei dem jede mit einer einzelnen Regel erstellte Promotion falsch interpretiert und als Promotion-Typ „Liste von Elementen“ angezeigt wurde, unabhängig von der Logik der Regel. (TGT-53063)
* Fehlerkorrektur - Bei der Verwendung der aktualisierten [!UICONTROL Overview]Benutzeroberfläche fehlt die Schaltfläche &quot;[!UICONTROL Download Recommendations Data]&quot; für [!UICONTROL Experience Targeting] (XT)-Aktivitäten, die [!DNL Recommendations] enthalten. (TGT-52730 und TGT-52756)
* Zuvor wurde in der Recommendations-Benutzeroberfläche nur die Anzahl der Entitäten angezeigt, die erfolgreich aus einem Feed importiert wurden. Das Backend-Nachrichtenformat umfasst jedoch sowohl die Anzahl der importierten Entitäten als auch die Gesamtzahl der Entitäten im Format `# of entities imported / # of total entities`. Aufgrund dieser Diskrepanz wurde den Benutzenden in der Benutzeroberfläche nur der erste Wert (Anzahl der importierten Daten) angezeigt, was zu Verwirrung führte. Die Benutzeroberfläche zeigt jetzt beide Zahlen an. (TGT-53073)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden beim Konfigurieren einer &quot;[!UICONTROL Promote by attribute]&quot;-Promotion in einer formularbasierten A/B-Aktivität mit Empfehlungen keine Filterregel speichern konnten. Nach dem Speichern und erneuten Öffnen der Aktivität fehlte die Filterregel und die Aktivität konnte nicht erfolgreich gespeichert werden. (TGT-53057)

+++

**Berichte**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem die Auswahl von &quot;[!UICONTROL Export order details to CSV]&quot; auf der Seite &quot;[!UICONTROL Reports]&quot; dazu führte, dass eine leere Datei heruntergeladen wurde. Dieses Problem trat auch dann auf, wenn gültige Bestelldaten in der Aktivität vorhanden waren. (TGT-52225)
* Fehlerkorrektur - Jetzt tritt kein Fehler mehr auf, wenn versucht wird, eine Aktivität nach dem Erstellen und Zuweisen einer neuen Reporting-Zielgruppe zu speichern. Die zurückgegebene Fehlermeldung war: „Zugriff verweigert. Um diesen Vorgang auszuführen, sind alle folgenden Berechtigungen erforderlich: [editor]. Dieses Problem trat auf, obwohl der Benutzer Zugriff auf der Ebene der genehmigenden Person hatte. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem die Anwendung einer Änderung auf eine Ansicht dazu führte, dass die Ansicht dupliziert wurde und die Aktivität den Fehler „Ungültige Benutzereingabe“ zurückgab. Durch diese Fehlerbehebung wird sichergestellt, dass Ansichtsänderungen korrekt angewendet werden, ohne dass Duplizierungs- oder Validierungsfehler ausgelöst werden. (TGT-52886)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code fälschlicherweise für das falsche Erlebnis angezeigt wurden. Insbesondere wurden Änderungen, die für ein Erlebnis vorgesehen waren, in einem anderen Erlebnis gezeigt, was zu Verwirrung und einer potenziellen Fehlkonfiguration von Live-Aktivitäten führte. (TGT-52776)
* Ein Problem wurde behoben, das das Bearbeiten oder Speichern benutzerdefinierter Code-Änderungen in der neuen VEC-Benutzeroberfläche verhinderte. Speziell:

   * Nach dem Bearbeiten und Speichern eines benutzerdefinierten Code-Blocks wurden die Änderungen weder in der Benutzeroberfläche noch in der QS-Vorschau angezeigt.
   * In einigen Fällen konnten Änderungen erst gelöscht werden, nachdem die Aktivität geschlossen und erneut geöffnet wurde.
   * Als Problemumgehung mussten Benutzende den Code kopieren, die Änderung löschen und ihn manuell mit den aktualisierten Inhalten neu erstellen. (TGT-53072)

* Es wurde ein Problem behoben, bei dem das Bearbeiten und Speichern von benutzerdefiniertem Code dazu führte, dass das [!UICONTROL Modifications] Bedienfeld nicht mehr reagierte. (TGT-53075)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code in Variantenerlebnissen unbeabsichtigt im [!UICONTROL Control] widergespiegelt wurden. Dies führte zu unbeabsichtigten Änderungen im Versandverhalten. Das [!UICONTROL Control] bleibt jetzt von benutzerdefinierten Code-Bearbeitungen an anderen Erlebnissen isoliert. (TGT-52413)
* Es wurde ein Problem behoben, bei dem Änderungen an einem Erlebnis (z. B. Erlebnis B) versehentlich in ein anderes Erlebnis (Erlebnis A) dupliziert wurden, wenn der Benutzer auf das zweite Erlebnis klickte, bevor der Editor vollständig geladen war. Dieses Verhalten kann auch dazu führen, dass Änderungen verloren gehen, wenn das ursprünglich ausgewählte Erlebnis keine Änderungen aufwies. (TGT-52597)
* Es wurde ein Problem behoben, bei dem Änderungen, die im [!UICONTROL Modifications] Schritt der Aktivitätserstellung vorgenommen wurden, nicht konsistent gespeichert wurden. In einigen Fällen wird das im Abschnitt [!UICONTROL Save] hinzugefügte benutzerdefinierte Skript nach Abschluss aller Schritte und Klicken auf [!UICONTROL Modifications] nicht auf der Live-Site widergespiegelt, obwohl während des Speichervorgangs keine sichtbaren Fehler aufgetreten sind. (TGT-52661)
* Es wurde ein Problem behoben, bei dem Änderungen an benutzerdefiniertem Code nicht korrekt gespeichert und unbeabsichtigt in mehreren Erlebnissen innerhalb derselben Aktivität gespiegelt wurden. Darüber hinaus traten beim Öffnen oder Aktualisieren bestimmter Aktivitäten Zugriffsprobleme auf, was zu leeren Bildschirmen führte. Diese Probleme wurden nun behoben, um eine stabile Aktivitätsbearbeitung und eine genaue Isolierung der Erlebnisse sicherzustellen. (TGT-52594)
* Es wurde ein Problem behoben, bei dem Benutzende in [!UICONTROL Browse Mode] nicht zu einer anderen URL navigieren konnten. Tester und Bearbeiter konnten dadurch alternative Seiten innerhalb derselben Aktivitätssitzung nicht validieren oder in der Vorschau anzeigen. (TGT-53052)
* Es wurde ein Problem behoben, bei dem mehrere [!UICONTROL Visual Experience Composer] (VEC)-Instanzen gleichzeitig während der Aktivitätserstellung geöffnet wurden. Dieses Problem trat auf, wenn Benutzende den [!UICONTROL Enhanced Experience Composer] (EEC) deaktiviert und den nachgestellten Schrägstrich im [!UICONTROL Page Delivery] Schritt aus der Website-URL entfernt haben. (TGT-52782)
* Es wurde ein Problem behoben, bei dem die Dropdown-Liste [!UICONTROL Revenue] im [!UICONTROL Goals & Settings] fälschlicherweise auf [!UICONTROL Revenue per Visit] (RPVISIT) eingestellt war, selbst wenn der Benutzer eine andere Metrik ausgewählt hatte.  Beim Reduzieren und erneuten Erweitern des Bedienfelds für die Metrikkonfiguration ist ein Problem aufgetreten, sodass der zuvor ausgewählte Wert zurückgesetzt wurde. (TGT-52811 und TGT-52878)
* Fehlerkorrektur - Im Workflow zum Erstellen von Aktivitäten treten jetzt keine Probleme mehr im Zusammenhang mit der Angebotsbenennung und der Inhaltsübersetzung in [!UICONTROL Automated Personalization] Aktivitäten (AP) und [!UICONTROL Multivariate Testing] (MVT) auf:

  Wichtige angesprochene Probleme:

   * Das Erstellen mehrerer HTML-Angebote mit demselben Namen (z. B. „Erlebnis„) hat den Fehler „Doppelte Angebotsnamen sind nicht zulässig“ ausgelöst, aber die Benutzeroberfläche hat nicht klar angegeben, welche Angebote den Konflikt verursacht haben.
   * Beim Umbenennen von Angeboten über das rechte Bedienfeld wurde der Name in der Benutzeroberfläche aktualisiert, die Änderung wurde jedoch nicht auf der Registerkarte [!UICONTROL Manage Content] oder der Registerkarte [!UICONTROL Offers] angezeigt, was zu anhaltenden Validierungsfehlern führte.
   * Obwohl der Fehler beim Duplizieren des Namens in MVT-Aktivitäten nach dem Umbenennen nicht fortbestand, konnte die Benutzeroberfläche aktualisierte Angebotsnamen weiterhin nicht konsistent auf allen Registerkarten widerspiegeln. (TGT-52933)

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
