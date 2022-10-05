---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: c5445903e7bbab210d0e72200c54ab07975c21c5
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 49%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 22.10.1 (gestaffelte Version vom 5. bis 7. Oktober 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **Oktober 5**: Region Asien-Pazifik (APAC)
* **6. Oktober**: Amerikanische Region
* **7. Oktober**: Region Europa, Naher Osten und Afrika (EMEA)

Diese Version enthält die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) Experience Fragments | Zu den Aktualisierungen der AEM-Funktion für Experience Fragments gehören:<ul><li>Es wurde die Möglichkeit hinzugefügt, AEM Experience Fragments nach Typ (HTML oder JSON) im [!UICONTROL Angebote] Liste. (TGT-43121)</li><li>Es wurde ein Problem behoben, durch das Kunden JSON einfügen konnten [!UICONTROL Experience Fragment] Angebote bei Verwendung von VEC, die nicht unterstützt wird. JSON-Angebote können nur eingefügt werden, wenn die [!UICONTROL Formularbasiertes Erlebnis] Composer. (TGT-43846)</li></ul>Weitere Informationen finden Sie unter AEM [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Neu [!UICONTROL Visual Experience Composer] Erweiterung für Google Chrome | Eine neue [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC)-Erweiterung für Chrome ist im Chrome Web Store verfügbar.<br>Ab Januar 2023 wird die aktuelle [!DNL Target] Die VEC Helper-Erweiterung funktioniert in Google Chrome nicht mehr, da Google keine Erweiterungen mit Manifest V2 zulässt. Laden Sie die neue Erweiterung herunter, um Ihre Websites weiterhin visuell zu erstellen in [!DNL Target] ab dem neuen Jahr.<br>Die folgenden Links zeigen die beiden Erweiterungen im Chrome Web Store:<ul><li>[Neue Erweiterung](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Alte Erweiterung](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Weitere Informationen finden Sie unter [Visual Editing Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]<br>(Das genaue Veröffentlichungsdatum muss noch festgelegt werden.) | Beachten Sie die folgenden Änderungen:<ul><li>Unterstützung für binäre Metriken und Maximierungsmetriken in [!UICONTROL Analytics for Target] A4T-Reporting für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] activities</li><li>Das Verhalten für bestehende Aktivitäten wurde bis zum 20. Februar 2023 beibehalten. Nach diesem Datum werden die Aktivitäten eingestellt, um die Migration vorhandener Aktivitäten zu neuem Verhalten zu erzwingen</li><li>Ab dem 20. Februar 2023 unterstützt `averagetimespentonsite`, `bouncerate`und `entries` Metriken in [!DNL Target] -Aktivitäten werden nicht mehr unterstützt.</li></ul> |

* Es wurde ein Fehler behoben, der verhinderte, dass Informationen zu Zielgruppenregeln ordnungsgemäß im [!UICONTROL Zielgruppenverfeinerungen] Informationsfenster. (TGT-43917)
* Die Leistung der [!DNL Target] Benutzeroberfläche beim Laden von Zielgruppen, die sich an die [empfohlene Begrenzung der Targeting-Regeln](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* Es wurde ein Fehler behoben, der dazu führte, dass einige Komponenten im [!UICONTROL Änderungen] Bedienfeld auf [!UICONTROL Erlebnisse] Seite beim Erstellen oder Bearbeiten von Aktivitäten im VEC nach dem Wechsel von [!UICONTROL Erstellen] nach [!UICONTROL Durchsuchen] -Modus. (TGT-43300)
* Fehlerkorrektur - Einige Kunden können jetzt archivieren [!UICONTROL A/B-Test] Aktivitäten, die [!UICONTROL Automatisches Targeting]. (TGT-40978)
* Es wurde die Möglichkeit hinzugefügt, automatisch ein einzelnes Angebot an mehreren Stellen innerhalb einer Berichtsgruppe zu verwenden. (TGT-40689)

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
