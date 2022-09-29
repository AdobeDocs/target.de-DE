---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: f567203808ef31191754773079450bc7a323dde7
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 28%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 29. September 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 22.10.1 (gestaffelte Version vom 4. bis 6. Oktober 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **4. Oktober**: Region Europa, Naher Osten und Afrika (EMEA)
* **Oktober 5**: Region Asien-Pazifik (APAC)
* **6. Oktober**: Amerikanische Region

Diese Version enthält die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) Experience Fragments | Zu den Aktualisierungen der AEM-Funktion für Experience Fragments gehören:<ul><li>Es wurde die Möglichkeit hinzugefügt, AEM Experience Fragments nach Typ (HTML oder JSON) im [!UICONTROL Angebote] Liste. (TGT-43121)</li><li>Es wurde ein Problem behoben, durch das Kunden JSON einfügen konnten [!UICONTROL Experience Fragment] Angebote bei Verwendung von VEC, die nicht unterstützt wird. JSON-Angebote können nur eingefügt werden, wenn die [!UICONTROL Formularbasiertes Erlebnis] Composer. (TGT-43846)</li></ul>Weitere Informationen finden Sie unter AEM [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Neu [!UICONTROL Visual Experience Composer] Erweiterung für Google Chrome | Eine neue [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC)-Erweiterung für Chrome ist im Chrome Web Store verfügbar.<br>Ab Januar 2023 wird die aktuelle [!DNL Target] Die VEC Helper-Erweiterung funktioniert in Google Chrome nicht mehr, da Google keine Erweiterungen mit Manifest V2 zulässt. Laden Sie die neue Erweiterung herunter, um Ihre Websites weiterhin visuell zu erstellen in [!DNL Target] ab dem neuen Jahr.<br>Die folgenden Links zeigen die beiden Erweiterungen im Chrome Web Store:<ul><li>[Neue Erweiterung](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Alte Erweiterung](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul> |
| Optimierte A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]<br>(Das genaue Veröffentlichungsdatum muss noch festgelegt werden.) | Beachten Sie die folgenden Änderungen:<ul><li>Unterstützung für binäre Metriken und Maximierungsmetriken in [!UICONTROL Analytics for Target] A4T-Reporting für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] activities</li><li>Die Warnmeldung bezüglich der binären Metriken für wurde entfernt. [!UICONTROL Automatisches Targeting] activities</li><li>Das Verhalten für bestehende Aktivitäten wurde bis zum 20. Februar 2023 beibehalten. Nach diesem Datum werden die Aktivitäten eingestellt, um die Migration vorhandener Aktivitäten zu neuem Verhalten zu erzwingen</li><li>Ab dem 20. Februar 2023 unterstützt `averagetimespentonsite`, `bouncerate`und `entries` Metriken in [!DNL Target] -Aktivitäten werden nicht mehr unterstützt.</li></ul> |

* Es wurde ein Fehler behoben, der verhinderte, dass Informationen zu Zielgruppenregeln ordnungsgemäß im [!UICONTROL Zielgruppenverfeinerungen] Informationsfenster. (TGT-43917)
* Die Leistung der [!DNL Target] Benutzeroberfläche beim Laden von Zielgruppen, die sich an die [empfohlene Begrenzung der Targeting-Regeln](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* Es wurde ein Fehler behoben, der dazu führte, dass einige Komponenten im [!UICONTROL Änderungen] Bedienfeld auf [!UICONTROL Erlebnisse] Seite beim Erstellen oder Bearbeiten von Aktivitäten im VEC nach dem Wechsel von [!UICONTROL Erstellen] nach [!UICONTROL Durchsuchen] -Modus. (TGT-43300)
* Fehlerkorrektur - Einige Kunden können jetzt archivieren [!UICONTROL A/B-Test] Aktivitäten, die [!UICONTROL Automatisches Targeting]. (TGT-40978)
* Es wurde die Möglichkeit hinzugefügt, automatisch ein einzelnes Angebot an mehreren Stellen innerhalb einer Berichtsgruppe zu verwenden. (TGT-40689)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
