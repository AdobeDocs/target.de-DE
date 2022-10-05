---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7f5b4265adbb0e98b7250f99b0268ba5b70dec7c
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 81%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 22.10.1 (gestaffelte Veröffentlichung vom 10. bis 13. Oktober 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **10. Oktober**: Region Asien-Pazifik (APAC)
* **11. Oktober**: Region Nord- und Südamerika
* **13. Oktober**: Region Europa, Naher Osten und Afrika (EMEA)

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) Experience Fragments | Zu den Aktualisierungen der AEM-Funktion für Experience Fragments gehören:<ul><li>Es wurde die Möglichkeit hinzugefügt, AEM Experience Fragments nach Typ (HTML oder JSON) im [!UICONTROL Angebote] Liste. (TGT-43121)</li><li>Es wurde ein Problem behoben, durch das Kunden in der Lage waren, bei Verwendung des VEC JSON [!UICONTROL Experience Fragment]-Angebote einzufügen, was nicht unterstützt wird. JSON-Angebote können nur eingefügt werden, wenn der [!UICONTROL formularbasierte Erlebnis]-Composer verwendet wird. (TGT-43846)</li></ul>Weitere Informationen finden Sie unter AEM [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Neue [!UICONTROL Visual Experience Composer]-Erweiterung für Google Chrome | Eine neue [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC)-Erweiterung für Chrome ist im Chrome Web Store verfügbar.<br>Ab Januar 2023 wird die aktuelle [!DNL Target] VEC Helper-Erweiterung in Google Chrome nicht mehr funktionieren, da Google keine Erweiterungen mehr zulässt, die Manifest V2 verwenden. Laden Sie die neue Erweiterung herunter, um Ihre Websites ab dem neuen Jahr weiterhin in [!DNL Target] visuell gestalten zu können.<br>Die folgenden Links zeigen die beiden Erweiterungen im Chrome Web Store:<ul><li>[Neue Erweiterung](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Alte Erweiterung](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Weitere Informationen finden Sie unter [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Dokumentationsaktualisierungen | Die wichtigsten Aktualisierungen der Dokumentation umfassen Folgendes:<ul><li>Neu und aktualisiert [Dokumentation zur Adobe Target Admin- und Reporting-API](https://developer.adobe.com/target/administer/admin-api/){target=_blank} umfasst eine umfassende Erfassung von Admin- und Reporting-API-Endpunkten, einschließlich Eigenschaften, Angeboten, Hosts, Umgebungen, Clients, Zielgruppen, Aktivitäten und mehr.<br>Siehe dies und zusätzlichen Entwicklerinhalt im Abschnitt [[!DNL Adobe Target] [!UICONTROL Entwicklerhandbuch]](https://developer.adobe.com/target/){target=_blank}.</li><li>[Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>In diesem Artikel werden die detaillierten statistischen Berechnungen dokumentiert, die bei manuellen A/Bn-Tests in [!DNL Adobe Target].<br>Die Informationen in diesem Artikel ersetzen die *Adobe Target-Berechnungen für A/B-Tests* PDF-Datei, die zuvor auf dieser Website zum Download verfügbar war.</li></ul> |

* Es wurde ein Problem behoben, das verhinderte, dass Informationen zu Zielgruppenregeln im Informationsfenster [!UICONTROL Zielgruppenverfeinerungen] korrekt angezeigt wurden. (TGT-43917)
* Die Leistung der [!DNL Target]-Benutzeroberfläche beim Laden von Zielgruppen, die sich dem [empfohlenen Limit der Zielgruppenbestimmungsregeln](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules) nähern, wurde verbessert. (TGT-43675)
* Es wurde ein Problem behoben, das dazu führte, dass einige Komponenten im Bedienfeld [!UICONTROL Änderungen] auf der Seite [!UICONTROL Erfahrungen] nicht richtig angezeigt wurden, wenn Aktivitäten im VEC erstellt oder bearbeitet wurden, nachdem vom Modus [!UICONTROL Zusammenstellen] zum Modus [!UICONTROL Durchsuchen] gewechselt wurde. (TGT-43300)
* Es wurde ein Problem behoben, das einige Kunden daran hinderte, [!UICONTROL A/B-Test]-Aktivitäten zu archivieren, die [!UICONTROL Automatisches Targeting] verwenden. (TGT-40978)
* Es wurde die Möglichkeit hinzugefügt, ein einzelnes Angebot automatisch an mehreren Orten innerhalb einer einzigen Berichtsgruppe zu verwenden. (TGT-40689)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md). |
