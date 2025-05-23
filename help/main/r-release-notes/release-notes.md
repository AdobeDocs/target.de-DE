---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 0d7ae6e269211b1c0beea346f527d28c8765f8c3
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 21%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Einstellen der Target-Benutzeroberflächenversion (23. Mai 2025) {#toggle}

Der Rollout der neuen [!DNL Target]-Benutzeroberfläche wird bis zum 27. **2025**. Ab diesem Zeitpunkt haben alle Kunden Zugriff auf die neueste Version der Benutzeroberfläche.

Ab **22. Juni** wird der Umschalter für die Benutzeroberflächenversion entfernt. Alle Benutzer wechseln dauerhaft zur neuen Benutzeroberfläche, ohne die Möglichkeit, zur vorherigen Version zurückzukehren.

**Wichtige Informationen zum Umschalten der Benutzeroberflächenversion**

Wir bieten eine temporäre Funktion, mit der Sie mithilfe einer Umschaltfläche zwischen der aktualisierten [!DNL Target]-Benutzeroberfläche und der Legacy-Version wechseln können. Diese Option ist nur während der letzten Phase des Rollouts der Benutzeroberfläche verfügbar.

![Umschalter für Target-Benutzeroberflächenversion](/help/main/r-release-notes/assets/toggle.png)

Sobald der Rollout abgeschlossen ist, wird der Umschalter entfernt und alle Benutzenden werden am (22. **2025) dauerhaft zur aktualisierten Benutzeroberfläche**. Adobe empfiehlt, vorauszuplanen, da diese Funktion bald auslaufen wird.

**Einschränkungen des Umschalt-Verhaltens der Benutzeroberfläche**

* **Sichtbarkeit neuer Aktivitäten**: Aktivitäten, die in der aktualisierten Benutzeroberfläche erstellt wurden, werden nicht angezeigt, wenn Sie zur alten Benutzeroberfläche zurückkehren.
* **Bearbeiten vorhandener Aktivitäten**: Änderungen an vorhandenen Aktivitäten (die ursprünglich in der veralteten Benutzeroberfläche erstellt wurden), während die aktualisierte Benutzeroberfläche verwendet wird, werden auf Ihrer Website veröffentlicht. Diese Aktualisierungen werden jedoch nicht in der alten Benutzeroberfläche angezeigt, wenn Sie zurückwechseln. Nur die letzten Aktualisierungen, die von der alten Benutzeroberfläche vorgenommen wurden, werden dort angezeigt.
* **Konsistenz der Aktivitätsdetails**: Die neuesten Änderungen werden unabhängig von der verwendeten Benutzeroberfläche auf Ihrer Live-Website angezeigt. In der veralteten Benutzeroberfläche werden jedoch nur die neuesten Änderungen angezeigt, die in dieser Version vorgenommen wurden. Dies kann verwirrend sein, wenn die in der aktualisierten Benutzeroberfläche bearbeiteten Aktivitäten anders aussehen als die in der alten Benutzeroberfläche.

Weitere Informationen zur aktualisierten Benutzeroberfläche finden Sie in den folgenden Ressourcen:

* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) - Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2)
* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) - Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1)
* [[!UICONTROL Visual Experience Composer] Kalender](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
* [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

## [!DNL Target Standard/Premium] 25.5.3 (22. Mai 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem die Funktion „Nach Namen suchen“ in der [!UICONTROL Activities]-Liste bei Abfragen mit mehreren Wörtern nicht korrekt funktionierte. (TGT-52529)
* Es wurde ein Problem behoben, das das Ausschließen von Erlebnissen aus [!UICONTROL Automated Personalization] (AP)-Aktivitäten verhinderte. (TGT-52383)
* Es wurde ein Problem behoben, bei dem bei der Verwaltung von Inhalten in AP-Aktivitäten die Option &quot;[!UICONTROL Contains]&quot; in der [!UICONTROL Filter Rules] fehlte. (TGT-52384)
* Fehlerkorrektur - Die Berichterstellung in [!UICONTROL Automated Personalization] (AP)-Aktivitäten ist jetzt inkonsistent. Dies bezieht sich insbesondere auf die Art und Weise, wie Standardangebote verfolgt und mithilfe von `optionLocalId` aus dem internen System von [!DNL Target] gemeldet werden.
* Es wurde ein Problem behoben, bei dem QA-Links nicht das beabsichtigte Aktivitätserlebnis bereitstellten. (TGT-52163)
* Es wurde ein Problem behoben, bei dem Benutzende mit [!UICONTROL Approver]-Berechtigungen fälschlicherweise daran gehindert wurden, Live-Aktivitäten zu bearbeiten, und die Fehlermeldung „Zugriff verweigert“ erhielten. (TGT-52416)
* Es wurde ein Problem behoben, bei dem Zielgruppenverfeinerungen für bestimmte Aktivitäten in der aktualisierten [!DNL Target]-Benutzeroberfläche nicht angezeigt wurden. (TGT-52057)
* Es wurde ein Fehler behoben, der dazu führte, dass Zielgruppenverfeinerungen und Aktivitäts-Zielgruppen in der aktualisierten Benutzeroberfläche rückgängig gemacht wurden. (TGT-52158)
* Es wurde ein Problem behoben, bei dem das Generieren von Ad-hoc-Angeboten zu doppelten Angeboten führte. (TGT-51938)
* Es wurde ein Problem behoben, durch das Angebotsaktualisierungen blockiert und fälschlicherweise der Fehler „Ungültiger Benutzer“ angezeigt wurde. (TGT-52361)
* Es wurde ein Problem behoben, das das Speichern vorhandener Aktivitäten verhinderte und einen Fehler „Ungültige Benutzereingabe“ auslöste. (TGT-52422)
* Es wurde ein Problem behoben, das die Bearbeitung vorhandener HTML-Angebote blockierte und beim Speichern den Fehler „Ungültige Benutzereingabe“ auslöste, selbst wenn keine Code-Änderungen vorgenommen wurden. (TGT-52351)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Target] das Zeichen &quot;#&quot; in der URL einer Website nicht erkennen konnten. (TGT-52093)
* Es wurde ein Problem behoben, das dazu führte, dass [!DNL Recommendations]-Aktivitäten zum Hinzufügen oder Aktualisieren von Promotions nicht bearbeitet werden konnten, was zu Speicherfehlern und doppelten Promotions führte. (TGT-52343)
* Es wurde ein Problem behoben, das Änderungen an Kriterien oder Designs in [!DNL Recommendations]-Aktivitäten verhinderte, was zu dem Fehler „Ungültige JSON: Nicht erkannter Eigenschaftsname“ führte. (TGT-52375)
* Es wurde ein Problem behoben, bei dem Sequenzkriterien in der [!UICONTROL Visual Experience Composer] (VEC) für [!DNL Recommendations] Aktivitäten nicht korrekt angezeigt wurden. (TGT-52435)
* Es wurde ein Problem behoben, bei dem Ansichten auf SPA-Seiten bei Verwendung der -[!DNL Adobe Experience Platform Web SDK] nicht korrekt identifiziert wurden. (TGT-52106)
* Es wurde ein Problem behoben, bei dem Details zur On-Device Decisioning (ODS) nicht korrekt gespeichert wurden, obwohl sie in der Payload des Batch-Vorgangs enthalten waren. (TGT-52406)
* Ein `audienceMetadata` Feld wurde zu den Aktivitäten hinzugefügt, sodass es während der Bearbeitung gelesen und aktualisiert werden kann. (TGT-51004)
* Es wurde eine Fehlermeldung hinzugefügt, die Benutzer benachrichtigt, wenn ein Zielgruppen-Zeitrahmen ungültig ist. (TGT52522)
* Die Aktivitätsstruktur wurde aktualisiert, um doppelte Zielgruppen verschiedener Typen zu unterstützen. (TGT-51200)

## Version [!DNL Adobe Target] [!DNL AI Assistant] (16. Mai 2025)

Wir freuen uns, den Start des [!DNL AI Assistant] in [!DNL Adobe Target] bekannt geben zu können! Diese leistungsstarke Benutzeroberfläche soll Ihnen helfen, [!DNL Target] Konzepte einfach zu navigieren und zu verstehen. Verfügbar für mehrere Produkte in [!DNL Adobe Experience Cloud], einschließlich [!DNL Target], [!DNL AI Assistant] ist hier, um Ihr Erlebnis zu revolutionieren.

[!DNL AI Assistant] in [!UICONTROL Target] ist ein Tool für Gespräche, mit dem Sie Ihre Workflows mit [!DNL Experience Platform] Anwendungen und Services beschleunigen können. Nutzen Sie [!DNL AI Assistant], um Ihre Gesamtproduktivität zu steigern und Ihr Wissen über Produkte zu erweitern

[!DNL Target] bietet die erste Phase der [!DNL AI Assistant] wertvolles Produktwissen, das auf [!DNL Experience League] Dokumentation basiert. Unabhängig davon, ob Sie ein Profilskript einrichten, Fehler beheben oder ein Upgrade auf AEP Web SDK in Betracht ziehen, [!DNL AI Assistant] Sie Folgendes behandelt.

Weitere Informationen finden Sie unter [Übersicht über den Adobe Experience Platform-KI-Assistenten](/help/main/c-intro/ai-assistant.md).

## [!DNL Target Standard/Premium] 25.5.2 (8. Mai 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* [!DNL Target] Benutzer mit [!UICONTROL Product Administrator]- und [!UICONTROL System Administrator] können jetzt alle Einstellungen auf den [!UICONTROL Administration] Seiten bearbeiten, unabhängig von ihrer Rolle in [!DNL Target]. Benutzende ohne diese Berechtigungen haben schreibgeschützten Zugriff auf diese Einstellungen. Diese Aktualisierung stellt eine strengere Zugriffskontrolle über [Administrationseinstellungen](/help/main/administrating-target/administrating-target.md) sicher. (TGT-48179)
* Es wurde ein Caching-Problem behoben, das das Speichern der Aktivität [Site-Voreinstellungen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) verhinderte. (TGT-52213)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden die Auswahl nach ID und Klasse im Abschnitt [!UICONTROL Site Preferences] nach dem Laden der Site in Visual Experience Composer nicht aktivieren konnten. Die [!UICONTROL Site Preferences]-Einstellung wird auch nach der Aktivierung automatisch auf Deaktiviert zurückgesetzt. (TGT-52207)
* Es wurde ein Problem behoben, bei dem der [!UICONTROL Visual Experience Composer] (VEC) nicht die richtige Seite anzeigte, wenn [Seitenversand](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings)-URLs mit einem Schrägstrich (/) endeten. (TGT-52237)
* Ein Problem wurde behoben, das verhinderte, dass benutzerdefinierte Code-Änderungen beim Ändern von Erlebnissen entfernt wurden. (TGT-52240)
* Es wurde ein Problem behoben, bei dem HTML-Änderungen im VEC vorhandene Seitenelemente überlagerten. (TGT-52265)
* Es wurde ein Problem behoben, das die Bearbeitung von benutzerdefiniertem Code in der aktualisierten VEC verhinderte, da der vorhandene benutzerdefinierte Code nicht im Editor sichtbar war. (TGT-52272)
* Es wurde ein Fehler behoben, der die Fehlermeldung „Doppelte Namen sind nicht zulässig“ beim Speichern einer Recommendations-Aktivität verursachte. (TGT-52318)
* Es wurde ein Problem im aktualisierten VEC behoben, das Kunden daran hinderte, Textelemente zu bearbeiten oder Container-Objekte zu entfernen. (TGT-52348)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Customer Journey Analytics] auf einer Aktivitäts-[!UICONTROL Overview]-Seite nicht korrekt angezeigt wurden. (TGT-52359)
* Es wurde ein Problem behoben, das verhinderte, dass Berichtsgruppen in [!UICONTROL Automated Personalization] (AP)-Aktivitäten bestehen blieben. (TGT-52368)
* Ein Problem wurde behoben, das das Speichern von Aktivitäten verhinderte, die Offer Decisioning enthalten. (TGT-52390)
* Es wurde ein Problem behoben, bei dem das Standardangebot ausgewählt war, aber andere Angebotsinhalte, die in [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Multivariate Test] (MVT)-Aktivitäten angezeigt wurden. (TGT-52372)
* Die GET-Berechtigungslogik zur Prüfung mit ODER zwischen dem vollständigen Organisationszugriff und dem spezifischen Organisations- + Benutzerzugriff wurde korrigiert. (TGT-52374)
* Es wurde ein Problem behoben, bei dem Zielgruppennamen nicht angezeigt wurden, nachdem eine Zielgruppe für [!UICONTROL Managed Content] und [!UICONTROL Reporting Audiences] ausgewählt wurde, obwohl [!UICONTROL Show Only Selected] aktiviert war. (TGT-52393)

## [!DNL Target Standard/Premium] 25.5.1 (5. Mai 2025)

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
