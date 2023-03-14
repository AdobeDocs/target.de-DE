---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 2c4f5666b65bfc36885aad3907639a309e8c69f2
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 64%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target] Standard/Premium 22.15.1 (8. und 9. März 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **8. März**: Amerikanische Region
* **9. März**: Region Europa, Naher Osten und Afrika (EMEA)
* **9. März**: Region Asien-Pazifik (APAC)

>[!NOTE]
>
>Aufgrund von Problemen, die seitdem behoben wurden, verwenden die &quot;Optimierten A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]&quot;-Funktion, die am 8. und 9. März veröffentlicht wurde, wurde vorübergehend entfernt. Nach weiteren internen Tests wird die Funktion in den nächsten Wochen erneut veröffentlicht.

Diese Version enthält die folgenden Fehlerbehebungen:

* Aktualisierungen für die Erstellung benutzerdefinierter Webkomponenten mit der [!UICONTROL Visual Experience Composer] (VEC):

   * Die Auswahl von Shadow-DOM-Elementen im VEC wurde korrigiert, indem der Authoring-Prozess verbessert wurde, sodass keine Abhängigkeit von der [!DNL Target] Implementierungstyp beim Authoring des Shadow-Stamms. Jetzt sollte die Auswahl von Shadow DOM-Elementen im VEC für jede Website funktionieren.
   * Es wurde ein Problem behoben, das das Laden von HTML-Elementen mithilfe von #Shadow DOM im VEC verhinderte. (TGT-35801)
   * Korrektur von VEC-Problemen mit SPA Websites, die ShadowDOM verwenden. (TGT-43169)
   * Es wurde ein Problem mit dem Optimierungsziel behoben: &quot;auf ein Element geklickt&quot;hat, das den CSS-Selektor in ShadowDOM nicht ordnungsgemäß identifiziert hat.

>[!NOTE]
>
>Stellen Sie sicher, dass Sie eine [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (legierung.js) mit einer Version größer als 2.8.

**Bekanntes Problem**: Klick-Tracking für ein Shadow-Stammelement bei Verwendung von [!DNL Adobe Experience Platform Web SDK] funktioniert nicht ordnungsgemäß. (TNT-47012)

## at.js-Version 2.10.2 (7. März 2023)

* Es wurde ein Fehler behoben, der dazu führte, dass die `trackEvent` -Funktion immer einen Fehler zurückgeben.

Informationen zu allen at.js-Versionen finden Sie unter [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

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
