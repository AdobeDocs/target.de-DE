---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
title: Versionshinweise zu Adobe Target
feature: Release Notes
translation-type: tm+mt
source-git-commit: ae44c57c7b8767915fbbce4271a4b1858dd07efd
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 27%

---


# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 14. Januar 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

## Target Standard/Premium 21.1.1 (19. Januar 2021) 

Dieses Maintenance Release umfasst die folgenden Erweiterungen, Fehlerbehebungen und Änderungen.

Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

* Es wurde eine Warnung hinzugefügt, wenn eine [!DNL Adobe Analytics]-Metrik ausgewählt wird, wenn [!UICONTROL Analytics als Berichte-Quelle] (A4T) in einer [!UICONTROL Auto-Zielgruppe]-Aktivität verwendet wird. [!UICONTROL Auto-] Targeting-Modelle sind für die Verwendung binärer (konversionsbasierter) Metriken optimiert. Die Auswahl einer kontinuierlichen Metrik, z. B. Umsatz, kann zu suboptimalen Ergebnissen führen, und die [!UICONTROL Personalisierungseinblicke]-Berichte sind möglicherweise nicht genau. (TGT-38926)
* Dem Bericht [!UICONTROL Zusammenfassung der automatischen Zielgruppe] für [!UICONTROL Aktivitäten mit A4T wurde ein Statussymbol hinzugefügt. ] Das grüne Häkchensymbol neben den einzelnen Erlebnissen im Bericht gibt an, dass für dieses Erlebnis ein Modell für das personalisierte maschinelle Lernen generiert wurde. Das Uhrensymbol gibt an, dass nicht genügend Traffic verarbeitet wurde, um das Modell zu erstellen. (TGT-38925)
* Die Berichte [!UICONTROL Automatisierte Segmente] und [!UICONTROL Wichtige Attribute] für [!UICONTROL Automatisierte Zielgruppe]-Aktivitäten, die A4T- und [!DNL Analytics]-Konversionsmetriken verwenden, werden generiert und sehen genauso aus wie bei der Verwendung von [!DNL Target] als Berichte-Quelle. (TGT-38931)
* Der Liste [!UICONTROL Recommendations] [!UICONTROL Umgebung] wurde eine Filteroption für die  hinzugefügt. (TGT-38353)
* Es wurde ein Fehler behoben, der dazu führte, dass die falsche Produktanzahl in Sammlungen von [!UICONTROL Recommendations] angezeigt wurde. (TGT-39162)
* Es wurde ein Filter [!UICONTROL Zuletzt aktualisiert] zum Filter [!UICONTROL Recommendations] [!UICONTROL Katalogsuche] hinzugefügt. (TGT-38340)
* Es wurde ein Fehler in [!UICONTROL Recommendations] behoben, der dazu führte, dass die Seite [!UICONTROL Sequenz erstellen] hängen blieb, nachdem die Branche vertikal geändert wurde. (TGT-38160)
* Es wurde ein Fehler behoben, der verhinderte, dass die Aktivität gespeichert wurde, wenn die Gerätekooperation aktiviert war und der Berichte von [!DNL Target] als Quelle zu [!DNL Analytics] (A4T) geändert wurde. (TGT-38163)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer eine Audience aus einem Angebot in einer [!UICONTROL Automated Personalization]-Aktivität (AP) entfernen konnten. (TGT-39058)
* Es wurde ein Fehler behoben, der dazu führte, dass der falsche Zeitraum (Beginns- und Enddaten) für einige Kunden in den Karten [!UICONTROL Audience Info] angezeigt wurde. (TGT-39150)
* Es wurde ein Fehler behoben, der dazu führte, dass einige Kunden die Liste der Aktivitäten im [!UICONTROL Standardarbeitsbereich] nicht sehen konnten. (TGT-38526)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
