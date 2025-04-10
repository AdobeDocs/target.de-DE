---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 2e3191da2ac21f51fa6e08af615659db1ccdd2d9
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 52%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 25.4.1 (2. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der dazu führte, dass Erlebnis-Zielgruppen aus -Aktivitäten verschwanden. (TGT-52003)
* Fehlerkorrektur - Beim Versand treten jetzt keine unerwarteten Elemente mehr auf. (TGT-52011)
* Es wurde ein Problem behoben, durch das Kunden die Anzeige der Zielgruppe im Targeting-Diagramm auf der [!UICONTROL r]-Seite und während der Aktivitätsbearbeitung nicht sehen konnten. (TGT-52050)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Erlebnisse in [!UICONTROL Experience Targeting] (XT)-Aktivitäten nach Priorität neu anzuordnen. (TGT-52054)
* Es wurde ein Problem behoben, das beim Rückgängigmachen von Textstil-Änderungen zu falschem Rendering führte. (TGT-51876)
* Es wurde ein Problem behoben, durch das [!DNL Target] beim Ändern eines Umleitungsangebots auch alle [!UICONTROL ClickTrack] entfernt, die mit diesem Angebot verknüpft sind. (TGT-51936)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Target] beim Abbrechen von [!UICONTROL ClickTrack] die Auswahl fälschlicherweise speicherte. (TGT-51937)
* Es wurde ein Problem behoben, das nach dem Öffnen und Schließen der Mbox-Auswahl auf der [!UICONTROL Goals & Settings] ohne Änderungen zu einem Fehler wegen ungültigem Namen führte. (TGT-51983)
* Es wurde ein Problem behoben, das die Bearbeitung von Ad-hoc-Angeboten blockierte, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. (TGT-51984)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten blockierte, die Ad-hoc-Angebote mit benutzerdefiniertem Code enthielten. (TGT-51995)
* Es wurde ein Problem behoben, das dazu führte, dass Ausschlussregeln beim Bearbeiten kombinierter Zielgruppendefinitionen als Einschlussregeln angezeigt wurden. (TGT-51999)
* Ein Problem wurde behoben, das dazu führte, dass benutzerdefinierter Code während der Erlebnisbearbeitung nicht korrekt angezeigt wurde. (TGT-52005)
* Es wurde ein Problem behoben, durch das die [!UICONTROL Insert Before]-Option zum Einfügen von Inhalten vor der Navigationsleiste nicht mehr verfügbar war. (TGT-52031)
* Fehlerkorrektur - Das Standarderlebnis in Berichten wird jetzt korrekt hervorgehoben. (TGT-51716)
* Es wurde ein Problem behoben, das beim Erstellen einer Aktivität eine `default message [Invalid optionLocalIds: xx]]` auslöste. (TGT-52038)

## at.js-Version 2.11.8 (31. März 2025)

* Behobene CodeQL-identifizierte Sicherheitslücke in der Validierung von Zeichenfolgen-Suffixen, um Edge-Fälle während Größenänderungs- und Verschiebungsvorgängen zu verhindern. (TNT-51516)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

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
| [Vorrangiges Produkt-Update von Adobe](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
