---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6ecc59588b51da505b8f567a7e87ccef0f375477
workflow-type: tm+mt
source-wordcount: '1959'
ht-degree: 15%

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

## [!DNL Target Standard/Premium] 25.8.1 (7. August 2025)

Dieses Release umfasst die folgenden Erweiterungen und Fehlerbehebungen:

**Aktivitäten**

+++Siehe Details
* Es wurden mehrere Probleme mit der aktualisierten Benutzeroberfläche behoben, darunter Fehler beim Löschen von Seitentypen aufgrund von Abständen in Eingabewerten, unzuverlässigen Aktivitätskopien zwischen Arbeitsbereichen und fehlerhaften Seitenbereitstellungsregeln in QS-Umgebungen. (TGT-52703)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Benutzende mit der Rolle [!UICONTROL Editor] auf Live-Aktivitäten zugreifen und versuchen konnten, sie zu bearbeiten. Dies sollte eingeschränkt werden. In der Aktivitätsliste und den Übersichtsbildschirmen werden Bearbeitungsoptionen für Live-Aktivitäten fälschlicherweise angezeigt, was zu potenziellen unbeabsichtigten Änderungen führt. (TGT-53055)
* Es wurde ein Problem in der [!UICONTROL Advanced Search]-Benutzeroberfläche behoben, bei dem Benutzer bei Auswahl der Operatoren „Wert ist vorhanden“ oder „Wert ist nicht vorhanden“ aufgefordert wurden, einen Operanden einzugeben, der für diese Bedingungen nicht erforderlich sein sollte. (TGT-51961)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem Versuche, Aktivitäten aus dem Staging in den Produktionsarbeitsbereich zu kopieren, durchgängig fehlgeschlagen sind, selbst in Sandbox-Umgebungen. Kunden stießen auf verschiedene Fehlermeldungen, darunter „Anonyme Zielgruppe bereits von der Aktivität verwendet“ und „Ungültige Zielgruppen-ID“, obwohl sie gültige Konfigurationen verwendeten und über geeignete Arbeitsbereich-Berechtigungen verfügten. (TGT-52394)

+++

**Experience Fragments (XFs)**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem Experience Fragment (XF)-Inhalte in der [!UICONTROL Visual Experience Composer] (VEC)-Vorschau nicht gerendert werden können, obwohl sie in der Inhaltsbereitstellung ordnungsgemäß funktionieren. (TGT-53318)

+++

**Lokalisierung**

+++Siehe Details
* Es wurde ein Lokalisierungsproblem behoben, bei dem die Schaltfläche „Promotion hinzufügen“ im Abschnitt „Promotions“ in mehreren Sprachumgebungen im QA-Mandanten nicht lokalisiert erschien. (TGT-53263)

+++

**Angebote**

+++Siehe Details
* Es wurde ein Problem behoben, durch das beim Bearbeiten eines vorhandenen HTML-Angebots über Visual Experience Composer (VEC) alle Änderungen aus der Inhaltsbereitstellung entfernt wurden. Die Änderungen werden auf der Registerkarte Änderung ausgegraut angezeigt und werden in der QS-Vorschau nicht angezeigt, obwohl sie in der alten Benutzeroberfläche korrekt angewendet wurden. (TGT-52863)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem Änderungen an HTML-Angeboten, die im [!UICONTROL Visual Experience Composer] (VEC) vorgenommen wurden, nach der Navigation von der Registerkarte [!UICONTROL Targeting] zurück zu [!UICONTROL Experiences] nicht beibehalten wurden. (TGT-52874)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem das Einfügen eines HTML-Angebots vor und eines anderen nach demselben Selektor zu einer falschen Speicherortgenerierung führte. Als Kunden von der Registerkarte [!UICONTROL Targeting] zur Registerkarte [!UICONTROL Experience] zurückkehrten, wurde nur ein Selektor beibehalten, was zu Änderungen und einer fehlerhaften Bereitstellung des Inhalts führte. Dieses Verhalten unterschied sich von dem der alten Benutzeroberfläche, die beide Änderungen mit unterschiedlichen Standortkennungen korrekt beibehielt. (TGT-52891)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem durch Klicken auf ein hinzugefügtes Angebot in der [!UICONTROL Modifications] Leiste das Bedienfeld [!UICONTROL Configuration] der rechten Seite gelegentlich angezeigt und ausgeblendet wurde, sodass es schwierig war, mit den Angebotseinstellungen zu interagieren. (TGT-53288)
* Es wurde ein Problem behoben, bei dem HTML-Angebote, die zu zielgruppenspezifischen Varianten innerhalb einer Aktivität hinzugefügt wurden, nicht konsistent gespeichert wurden oder im Änderungsabschnitt angezeigt wurden. Nachdem während der Bearbeitung zwischen Audiences gewechselt wurde, waren zuvor angewendete Angebote manchmal verschwunden oder konnten nicht gerendert werden, wodurch die Validierung unterbrochen und die Bereitschaft für Aktivitäten verzögert wurde. (TGT-53440)
* Es wurde ein Problem behoben, bei dem das Kopieren einer Aktivität, die Angebote enthielt, dazu führte, dass in der neuen Aktivität doppelte Angebote erstellt wurden. Dieses Verhalten verursachte unnötige Unübersichtlichkeit und Verwirrung, insbesondere beim Verschieben von Aktivitäten zwischen Arbeitsbereichen. Die Korrektur stellt sicher, dass [!DNL Target] Angebote jetzt korrekt und ohne Duplizierung in den Zielarbeitsbereich kopiert werden, was die Aktivitätsverwaltung optimiert und die Workflow-Effizienz verbessert. (TGT-53454)

+++

**Single Page Applications (SPAs)**

+++Siehe Details
* Es wurde ein Problem im aktualisierten VEC behoben, das Kunden daran hinderte, Änderungen an [!UICONTROL Single Page Application] (SPA)-Ansichten anzuwenden. Während Aktivitäten, die in der alten Benutzeroberfläche erstellt wurden, ansichtsspezifisches Targeting unterstützten, konnte die neue Benutzeroberfläche Änderungen an diesen Ansichten nicht erkennen oder zulassen, wobei die Steuerelemente zum Umschalten der Ansicht deaktiviert wurden. (TGT-52556)

+++

**Visual Experience Composer (VEC)**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem Änderungen an Erlebnissen, die in der [!UICONTROL Visual Experience Composer] vorgenommen wurden, entweder nicht sichtbar waren oder in der Benutzeroberfläche inkonsistent erschienen. (TGT-TGT-53381)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem im [!UICONTROL Manage Content] Abschnitt kein Alternativtext für Erlebnisminiaturansichten angezeigt wurde. Dieses Problem machte es für Benutzende schwierig, Dokumente zu identifizieren, insbesondere wenn Dateinamen lang oder abgeschnitten waren. (TGT-52291)
* Es wurde ein Fehler behoben, bei dem Kunden beim Konfigurieren von [!UICONTROL page delivery] in VEC-Aktivitäten auf falsche Validierungsfehler stießen. Insbesondere wurde bei Operatoren wie „ist gleich eines von“ und „ist nicht gleich eines von“ die Auslösung „Ungültige Eingabe für den Operatortyp“ bei der Eingabe von Textwerten ausgelöst, obwohl Text unterstützt werden sollte. (TGT-52629)
* Es wurden mehrere Probleme behoben, die zu einem inkonsistenten Verhalten im [!UICONTROL Modifications] Bereich der aktualisierten Benutzeroberfläche führten, wenn Angebote mit der Schaltfläche „Angebot auswählen“ ausgewählt wurden. Statt das vorhandene Angebot zu ersetzen, hat die Benutzeroberfläche ein Duplikat hinzugefügt und versucht, mit beiden Angeboten zu interagieren, was zu Konsolenfehlern führte, z. B. `selectorNotFound`. Darüber hinaus wird bei einigen Angeboten nicht die Schaltfläche „Angebot auswählen“ angezeigt, sondern nur bearbeitbare Eigenschaften. (TGT-53321)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem HTML-Code-Änderungen, die während der Aktivitätseinrichtung vorgenommen wurden, nicht auf Variantenseiten beibehalten wurden, obwohl sie für Kontrollgruppen korrekt gespeichert wurden. Trotz mehrfacher Versuche und der Neuerstellung von Tests ohne Seitengruppierungen konnten die Variantenseiten durchgängig keine Änderungen beibehalten, was sich auf die Inhaltsbereitstellung und die QS-Validierung auswirkte. (TGT-53436)
* Es wurde ein Problem im aktualisierten VEC behoben, bei dem der Operator „ist gleich eines von“ in Seitenbereitstellungsregeln Eingabewerte nicht akzeptieren konnte. Bei der Konfiguration von Kundenparametern für alle Mboxes führte die Auswahl dieses Operators zu einem Fehler „Ungültige Eingabe“, was die Erstellung von Regeln verhinderte. (TGT-52623)

+++

**Arbeitsbereiche**

+++Siehe Details
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
