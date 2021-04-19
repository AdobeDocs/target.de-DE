---
keywords: Versionshinweise;Neue Funktionen;Releases;Updates;Update;Release;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerbehebungen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von Adobe Target, einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: ' Versionshinweise '
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 35%

---

# Versionshinweise zu Target (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Ab dem 31. März 2021 wird die Bibliothek &quot;mbox.js&quot; [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Migrieren Sie vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

(Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## Target Standard/Premium 21.4.1 (19. April 2021)

Diese Version enthält die folgenden neuen Funktionen und Erweiterungen. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| Unterstützung von Entscheidungen auf dem Gerät für at.js<br>(Datum der Ankündigung) | Die geräteinterne Entscheidungsfindung ermöglicht es Marketingexperten und Entwicklern, Experimente und Personalisierungen im Browser eines Benutzers mit einer Latenz von nahezu null zu ermöglichen.<br>Weitere Informationen finden Sie unter  [Gerätebezogene Entscheidungsfindung für &quot;at.js&quot;.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![](/help/assets/premium.png) PremiumList-basierte Operatoren für Entitäts-Filterregeln | [!DNL Target Recommendations] unterstützt neue Liste-basierte Operatoren für Entitätsfilterregeln. (TGT-39234)<br>Neu hinzugefügte Operatoren umfassen:<br><ul><li>in Liste</li><li>ist nicht in der Liste enthalten</li><li>Liste enthält ein Element in</li><li>Liste enthält kein Element in</li><li>Liste enthält alle Elemente in</li><li>Liste enthält nicht alle Elemente in</li></ul>Weitere Informationen finden Sie unter &quot;Verfügbare Operatoren&quot;in [Dynamische und statische Inklusionsregeln verwenden](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Diese Version enthält die folgenden Fehlerbehebungen.

* Es wurde ein Fehler behoben, der dazu führte, dass eine Aktivität nach dem Ändern der Audience in [!UICONTROL Alle Besucher] nicht synchronisiert werden konnte. (TGT-40259)
* Es wurde ein Fehler behoben, der verhinderte, dass Angebot dupliziert wurden, wenn sie an verschiedenen Stellen in den [!UICONTROL Automated Personalization]-Aktivitäten verwendet wurden, obwohl die Option [!UICONTROL Duplikat nicht zulassen] aktiviert war. (TGT-39567)
* Es wurde ein Fehler behoben, der verhinderte, dass die Seite [!UICONTROL Administration] > [!UICONTROL Scene7 configuration] ordnungsgemäß geladen wurde. (TGT-39918)
* Es wurde ein Fehler behoben, der dazu führte, dass Eigenschaften dem falschen Arbeitsbereich zugeordnet wurden. (TGT-39869)
* Es wurde ein Problem behoben, das zu unbegrenztem Laden führte, wenn die Anforderung nach dem Ändern der Umgebung beim Erstellen eines Empfehlungsausschlusses fehlschlug. (TGT-39948)

## at.js Version 2.5.0 (Datum der Bekanntgabe)

Diese Version von at.js umfasst die folgenden Erweiterungen und Änderungen:

* [Unterstützung von ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) Entscheidungen auf dem Gerät für &quot;at.js&quot;.
* [Vorschau ](/help/c-activities/c-activity-qa/activity-qa.md) unterstützt Automated Personalization-Aktivitäten.

Mit dieser Version wird auch die Unterstützung für Microsoft Internet Explorer 10 und höher entfernt.

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Detaillierte Informationen zur Ansicht zu Aktualisierungen in diesem Handbuch, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu  [Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Produktaktualisierung mit Priorität für Adoben | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
