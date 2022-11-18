---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8c348f40be8df5018d63c6b6fe75e1f8e804eafc
workflow-type: ht
source-wordcount: '420'
ht-degree: 100%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am: 19. Oktober 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target] Standard/Premium 22.10.3 (gestaffelte Veröffentlichung vom 25. bis 27. Oktober 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **25. Oktober**: Region Europa, Naher Osten und Afrika (EMEA)
* **26. Oktober**: Region Asien-Pazifik (APAC)
* **27. Oktober**: Region Nord- und Südamerika

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
| --- | --- |
| A4T-Metriken für [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]<br> (verfügbar für die Auswahl von Kunden zum Testen) wurden optimiert. (Wird in einer zukünftigen Version für alle Kunden verfügbar sein.) | Beachten Sie die folgenden Änderungen:<ul><li>Nicht-binäre und Maximierungsmetriken im Reporting von [!UICONTROL Analytics for Target] (A4T) für die Aktivitäten [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting] werden jetzt unterstützt</li><li>Das Verhalten für bestehende Aktivitäten wird bis Februar 2023 beibehalten. Nach diesem Datum werden die Aktivitäten eingestellt, um die Migration vorhandener Aktivitäten auf das neue Verhalten zu erzwingen.</li><li>Ab dem 20. Februar 2023 wird die Unterstützung für die Metriken `averagetimespentonsite`, `bouncerate` und `entries` in [!DNL Target]-Aktivitäten nicht mehr unterstützt.</li></ul> |

* Es wurden Tooltips in der [!DNL Target]-Benutzeroberfläche hinzugefügt, die Kunden dabei helfen, effizienter im Zielgruppen-Builder zu navigieren und zu erfahren, wie Funktionen verwendet werden, die ihnen möglicherweise nicht bekannt sind. (TGT-44139)
* Es wurde eine Funktion hinzugefügt, mit der verhindert werden kann, dass Kunden eine Aktivität bearbeiten, die von [!DNL Target] deaktiviert wurde, weil sie nicht unterstützte Metriken verwendet. Eine Meldung in der Benutzeroberfläche weist Kunden an, die Aktivität zu duplizieren und dann die Konversionsmetrik zu aktualisieren.

   Mit dieser Version werden `averagetimespentonsite`-, `bouncerate`- und `entries`-Metriken in [!DNL Target]-Aktivitäten für neue Aktivitäten nicht mehr unterstützt. Vorhandene Aktivitäten können diese Metriken bis Mai 2023 weiterhin verwenden.

* Es wurde eine QuickInfo in der [!DNL Target]-Benutzeroberfläche hinzugefügt, die Kunden bei der Auswahl eines Optimierungskriteriums hilft, während sie eine Aktivität für [!UICONTROL Automatisches Targeting], die A4T verwendet, erstellen oder bearbeiten.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |


## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
