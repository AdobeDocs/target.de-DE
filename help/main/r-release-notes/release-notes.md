---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 098415849152065b734cbebbab8dcf1d0805e202
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 14%

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

## Datenstrom-Updates (19. September 2025)

Die Kombination aus Datenstrom-ID und Sandbox muss für [!DNL Adobe Target] Zielverbindungen eindeutig sein.

Die Validierungslogik für [!DNL Target] Zielverbindungen wurde aktualisiert, um zu erzwingen, dass die Kombination aus Datenstrom-ID und Sandbox-Name innerhalb einer IMS-Organisation eindeutig sein muss. Dies bedeutet:

* Dieselbe Datenstrom-ID und dasselbe Sandbox-Namenspaar können nicht über mehrere [!DNL Target] Zielverbindungen hinweg wiederverwendet werden.
* Dieselbe Datenstrom-ID kann nur für verschiedene Verbindungen verwendet werden, wenn sie in verschiedenen Sandboxes konfiguriert sind.
* Diese Regel gilt für alle ausgewählten Datenstrom, auch wenn „Keine“ ausgewählt ist.

Diese Aktualisierung stellt eine konsistente Konfiguration sicher und verhindert Konflikte in Multi-Sandbox-Umgebungen. Weitere Informationen finden Sie unter [Adobe Target-Verbindung](https://experienceleague.adobe.com/de/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} im *Experience Platform-Ziele* Handbuch.

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
