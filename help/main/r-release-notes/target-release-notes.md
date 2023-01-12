---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 02105c00a856e755ef2fd0bb41620fd35ed609d2
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 37%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 4. Januar 2023**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 22.13.3 (25.-26. Januar 2023)

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

* Unterstützung für JSON-Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten, die den Form-Based Experience Composer verwenden. (TGT-41460)
* implementiert [QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) für AP-Aktivitäten.
* Erlebnisnamen in [!DNL Recommendations] -Aktivitäten werden nun mit Anzeigenamen angezeigt, damit Kunden Daten besser miteinander korrelieren können in [!DNL Adobe Analytics] mit dem in [!DNL Target] Benutzeroberfläche. (TGT-41853)
* Es wurde ein Problem behoben, das den Fehler &quot;500&quot;in [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten, die Empfehlungen enthalten. Dieses Problem wurde beim [!DNL Target] Kriterienobjekte konnten nicht ordnungsgemäß aus dem [!DNL Target] Benutzeroberfläche und [!DNL Recommendations] -Backend, das nicht mehr verwendet wird. (TGT-44383)
* Der Speicherort wurde aus dem angezeigten Angebotsnamen im [!UICONTROL Angebotsebene] Bericht für [!UICONTROL Automated Personalization] Aktivitäten. Durch diese Änderung wird der Bericht leichter lesbar. (TGT-44294)
* Die[!UICONTROL Experience Fragment]&quot; in der [!UICONTROL Visual Experience Composer] Workflow (VEC). Die Option lautet jetzt &quot;[!UICONTROL HTML XF].&quot; (TGT-44132)
* Es wurde die Möglichkeit hinzugefügt, die Metadaten von Experience Fragment-Angeboten in der QuickInfo zu Angeboten anzuzeigen. (TGT-43838)
* Die Kalenderoptionen 45 Tage und 90 Tage wurden aus der AP entfernt und [!UICONTROL Automatisches Targeting] [!UICONTROL Personalization Insights] und [!UICONTROL Wichtige Attribute] in [!DNL Target] Benutzeroberfläche. Aufgrund von Nutzungsmustern und zur Verbesserung der Leistung werden diese Datumsbereiche nicht mehr unterstützt. Die Benutzeroberfläche wurde aktualisiert, um die derzeit zulässigen Bereiche widerzuspiegeln: 15, 30 und 60 Tage. (TGT-39357)
* Die Möglichkeit, die [!UICONTROL Wie Optimierungsziel] -Einstellung auf [!UICONTROL Ziele und Einstellungen] Seite, nachdem die Aktivität live ist. (TGT-43923)
* Es wurde ein Problem behoben, das Probleme mit dem standardmäßigen Arbeitsplatz im [!DNL Target] Backend beim Upgrade von [!DNL Target Standard] nach [!DNL Target Premium]. (TGT-44081 und TGT-44306)
* Der Link auf der [!UICONTROL Implementierung] page ([!UICONTROL Administration] > [!UICONTROL Implementierung]) für &quot;Implementierungsmethoden mit On-Device Decisioning&quot;auf die Seite verweisen, auf der erläutert wird, wie Sie die Entscheidungsfindung auf dem Gerät für alle unterstützten SDKs verwenden können: Node.js, Java, .NET und Python. Weitere Informationen finden Sie unter [Erste Schritte mit Target-SDKs](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Fehlerkorrektur - Beim Verwenden von [!DNL Scene7] und [!DNL Target].
* Die Barrierefreiheit der [!DNL Target] Benutzeroberfläche für Personen mit Behinderungen durch Verwendung der Ergebnisse einer internen Nutzungsprüfung. Zu diesen Verbesserungen der Barrierefreiheit gehören der Zugriff auf Funktionen, auf die zuvor nicht über die Tastatur zugegriffen werden konnte, Verbesserungen bei Alternativtext, die Möglichkeit, Teile der Benutzeroberfläche zu vergrößern, um sie besser zu verwenden, ein verbesserter Tastaturfokus und mehr.   (TGT-42759)
* Verschiedene Lokalisierungskorrekturen im gesamten [!DNL Target] Benutzeroberfläche.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |


## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
