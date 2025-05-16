---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 63df83fd7479c7be7e4cd4c08501ab17511a41fb
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 32%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

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
