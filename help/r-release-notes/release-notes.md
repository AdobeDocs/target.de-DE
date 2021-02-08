---
keywords: Versionshinweise;Neue Funktionen;Releases;Updates;Update;Release;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerbehebungen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Release Notes
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 39%

---


# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

(Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

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

## at.js 2.4.0 (14. Januar 2021)

Diese Version von at.js ist ein Maintenance Release und umfasst die folgenden Fehlerbehebungen:

* Unterstützt Versand-API-KundenIDs mit Unified Profil/Platform ID.
* Fehlerhafte Tag-Injektion im Stil wurde behoben.

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu  [Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
