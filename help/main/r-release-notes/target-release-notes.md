---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 5ad7427df49f6091f69fadac96fd55e7b48a4cda
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 100%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 19. Januar 2023**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 22.13.3 (25. Januar 2023)

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

* Jetzt werden JSON-Angebote in Aktivitäten von [!UICONTROL Automated Personalization] (AP) unterstützt, für die der formularbasierte Experience Composer verwendet wird. (TGT-41460)
* [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) wurde für AP-Aktivitäten implementiert. (TGT-44341)
* Erlebnisnamen in [!DNL Recommendations] -Aktivitäten werden nun mit Anzeigenamen angezeigt, damit Kunden Daten in [!DNL Adobe Analytics] besser mit denen in der [!DNL Target]-Benutzeroberfläche korrelieren können. (TGT-41853)
* Es wurde ein Problem behoben, das zu einem „Fehler 500“ in [!UICONTROL A/B-Test-] und [!UICONTROL Experience Targeting] (XT)-Aktivitäten, die Empfehlungen enthalten, führte. Dieses Problem trat auf, wenn [!DNL Target] nicht mehr verwendete Kriterienobjekte nicht ordnungsgemäß aus der [!DNL Target]-Benutzeroberfläche und dem [!DNL Recommendations]-Backend löschen konnte. (TGT-44383)
* Der Speicherort wurde aus dem angezeigten Angebotsnamen im Bericht auf [!UICONTROL Angebotsebene] für [!UICONTROL Automated Personalization]-Aktivitäten entfernt. Durch diese Änderung wird der Bericht leichter lesbar. (TGT-44294)
* Die Option [!UICONTROL Experience Fragment] im Workflow von [!UICONTROL Visual Experience Composer] (VEC) wurde umbenannt. Die Option heißt jetzt „[!UICONTROL HTML XF]“. (TGT-44132)
* Es wurde die Möglichkeit hinzugefügt, die Metadaten von Experience Fragment-Angeboten im Angebotsinfo-Tooltip anzuzeigen. (TGT-43838)
* Die Kalenderoptionen für 45 Tage und 90 Tage wurden aus den AP- und [!UICONTROL Auto-Target] [!UICONTROL Personalisierungs-Insights] sowie aus den Berichten zu [!UICONTROL wichtigen Attributen] in der [!DNL Target]-Benutzeroberfläche entfernt. Aufgrund von Nutzungsmustern und im Hinblick auf eine Verbesserung der Leistung werden diese Datumsbereiche nicht mehr unterstützt. Die Benutzeroberfläche wurde mit den derzeit zulässigen Bereichen aktualisiert: 15, 30 und 60 Tage. (TGT-39357)
* Die Möglichkeit, die Einstellung [!UICONTROL Wie Optimierungsziel] auf der Seite [!UICONTROL Ziele und Einstellungen] zu ändern, nachdem die Aktivität live ist, wurde entfernt. (TGT-43923)
* Es wurde ein Problem behoben, das beim Upgrade von [!DNL Target Standard] nach [!DNL Target Premium] zu Problemen mit dem standardmäßigen Arbeitsbereich im [!DNL Target]-Backend führte. (TGT-44081 und TGT-44306)
* Der Link auf der Seite [!UICONTROL Implementierung] ([!UICONTROL Verwaltung] > [!UICONTROL Implementierung]) für „Implementierungsmethoden mit On-Device Decisioning“ wurde geändert, um auf die Seite verweisen, auf der erläutert wird, wie Sie die geräteinterne Entscheidungsfindung für alle unterstützten SDKs verwenden können: Node.js, Java, .NET und Python. Weitere Informationen finden Sie unter [Erste Schritte mit Target-SDKs](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Ein Fehler, der bei Verwendung von [!DNL Scene7] und [!DNL Target] zu Problemen mit Datei-Uploads führte, wurde behoben.
* Die Barrierefreiheit der [!DNL Target]-Benutzeroberfläche für Personen mit Behinderungen wurde auf Grundlage der Ergebnisse eines internen Usability-Audits verbessert. Es wird nun Zugriff auf Funktionen geboten, auf die zuvor nicht über die Tastatur zugegriffen werden konnte, die Alternativtexte wurden verbessert, Teile der Benutzeroberfläche können nun vergrößert werden, um sie besser verwenden zu können, der Tastaturfokus wurde verbessert und mehr. (TGT-42759)
* Es wurden in der gesamten [!DNL Target]-Benutzeroberfläche Lokalisierungskorrekturen vorgenommen.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |


## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
