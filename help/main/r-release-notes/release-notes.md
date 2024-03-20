---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6e15b9b10e6a40c8efec06c45442b0f9894e648e
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 59%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Aktualisierungen für `Browser:iPad` und `Browser:iPhone` in [!UICONTROL Browser] Zielgruppenattribute (30. April 2024)

| Updates | Details |
|--- |--- |
| [!UICONTROL Browser:iPad] und [!UICONTROL Browser:iPhone] aktualisiert in [Browserattribute](/help/main/c-target/c-audiences/c-target-rules/browser.md) wird beim Erstellen von Zielgruppen verwendet. | [!DNL Adobe Target] ermöglicht [Zielgruppe für eines oder mehrere Kategorieattribute](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), einschließlich Besuchern, die [Browser- oder Browseroptionen](/help/main/c-target/c-audiences/c-target-rules/browser.md) wenn sie Ihre Seite besuchen.<P>Beginnen Sie mit der [!DNL Target] Standard/Premium 24.3.1 (4.-6. März 2024), integrierte Zielgruppen, die mithilfe der Target-Benutzeroberfläche erstellt wurden, z. B. `Browser:iPad` und `Browser:iPhone` wird aktualisiert, um ein korrektes Targeting für [!DNL iPad] und [!DNL iPhone] using `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` und `profile.mobile.isTablet`.<P>Diese Aktualisierung erfordert keine Maßnahmen seitens der Kunden.<p><B>Wichtig</b>: Damit Kunden eine korrekte Zielgruppenbestimmung für [!DNL iPad] und [!DNL iPhone] In Profilskripten (und JavaScript-Segmenten) müssen vom Kunden manuelle Änderungen vorgenommen werden durch **30. April 2024**. Beispiele für alternative Einstellungen, die manuell geändert werden müssen, finden Sie unter [Aktualisierungen für [!DNL iPad] und [!DNL iPhone] in [!UICONTROL Browser] Zielgruppenattribute](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

## [!UICONTROL Visual Editing Helper] Erweiterung (14. März 2024)

Diese Version enthält die folgenden Verbesserungen und Fehlerbehebungen für die [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) Erweiterung für [!DNL Google Chrome]:

* Der iFrame-Lademechanismus beim Erstellen von Authoring auf den Websites von Kunden wurde verbessert.
* Es wurde ein Fehler behoben, der dazu führte, dass die -Erweiterung Cookies bei der Bearbeitung im [!UICONTROL Visual Experience Composer] (VEC).

## [!DNL Target] Standard/Premium 24.3.1 (4.-6. März 2024)

Die Veröffentlichung dieser Version ist für die folgenden Tage geplant:

* **4. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **5. März**: Region Asien-Pazifik (APAC)
* **6. März**: Region Nord- und Südamerika

Diese Version umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Die Logik zur Berechnung der Anzahl eindeutiger Selektoren in einer Aktivität wurde korrigiert. (TGT-47878)
* Es wurde ein Problem behoben, das [!UICONTROL Multivariate] (MVT) Aktivitäten, die mit [!UICONTROL Analytics for Target] (A4T) nicht ordnungsgemäß angezeigt werden. (TGT-47490)
* Die Warnmeldung, die in Berichten angezeigt wird, wenn ein Erlebnis ohne Traffic als Kontrollerlebnis verwendet wird, wurde verbessert. (TGT-47537)
* Es wurden zahlreiche Backend- und Lokalisierungskorrekturen hinzugefügt.

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
