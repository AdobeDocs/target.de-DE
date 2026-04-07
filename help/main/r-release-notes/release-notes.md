---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
hold: true
source-git-commit: cad8c365028b28bd9349d2d283370e2c8a750180
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 35%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).


## [!DNL Target Standard/Premium] 26.4.1 (Freitag, 2. April 2026)

**Aktivitäten**

+++Details anzeigen

* **Zielgruppenattribute sind in der Ansicht „Aktivitäten“ sichtbar.** Es wurde ein Problem behoben, bei dem Details zu Zielgruppenregeln, die von einem **[!UICONTROL Activity]** angezeigt wurden, bestimmte Attribute nicht anzeigten, die beim Öffnen derselben Zielgruppe über den Abschnitt **[!UICONTROL Audiences]** angezeigt wurden. (TGT-54742)

* **Benutzerdefinierter Code wird beibehalten, wenn er auf zusätzliche Ansichten angewendet wird.** Es wurde ein Problem behoben, bei dem benutzerdefinierter Code, der auf eine **[!UICONTROL View]** angewendet wurde, entfernt werden konnte, wenn benutzerdefinierter Code für eine andere **[!UICONTROL View]** im selben **[!UICONTROL Activity]** hinzugefügt oder gespeichert wurde. (TGT-53933)

* **Exportieren von CSV zu Aktivitäten und Zielgruppen-Listenseiten.** Es wurde eine **[!UICONTROL Export CSV]** Aktion hinzugefügt, mit der Sie Aktivitätslisten über die Benutzeroberfläche exportieren können, auch wenn Filter angewendet werden, ohne sich ausschließlich auf APIs für Routineexporte zu verlassen. (TGT-51466)

* **Erlebnisänderungen werden gekennzeichnet, wenn keine Selektoren gefunden werden.** Erlebnisänderungen führen jetzt eine Selektor-Existenzprüfung durch. Wenn ein Selektor auf der Seite nicht gefunden wird, wird die Änderung als ungültig markiert. (TGT-54815)

* **[!UICONTROL Automated personalization].** Es wurden Probleme mit der Benutzeroberfläche und dem Laden von Aktivitäten behoben, die verhinderten, dass Benutzer Automated Personalization-Aktivitäten zuverlässig erstellen, bearbeiten oder verwalten konnten, wodurch die Kampagneneinrichtung blockiert und Anwendungsfälle für die Personalisierung verzögert wurden. (TGT-54421)

+++

**Zielgruppen**

+++Details anzeigen

* **Zielgruppenname und Beschreibung, die beim Erstellen von Zielgruppen aus einer Aktivität sichtbar sind.** Es wurde ein Problem behoben, bei dem die **[!UICONTROL Name]** und **[!UICONTROL Description]** Felder der Zielgruppe beim Erstellen oder Bearbeiten einer Zielgruppe aus dem Aktivitätsfluss nicht deutlich hervortraten als beim Erstellen der Zielgruppe direkt unter **[!UICONTROL Audiences]**. (TGT-54837)

+++

**Insights**

+++Details anzeigen

* **[!UICONTROL Live Activities]zählen auf Einblicke.** Es wurde ein Problem behoben, bei dem die **[!UICONTROL Live Activities]**-Metrik im Insights-Dashboard eine höhere Gesamtanzahl als die Anzahl der Aktivitäten meldete, die als in **[!UICONTROL All Activities]** aktiv erschienen. (TGT-54788)

+++

**Recommendations**

+++Details anzeigen

* **Lange ID-Listen in [!UICONTROL Global Exclusions].** Es wurde ein Problem behoben, bei dem das Einfügen oder Eingeben einer langen Liste von IDs in **[!UICONTROL Global Exclusions]** in der aktualisierten Benutzeroberfläche im Vergleich zur alten gekürzt werden konnte, was zu einer unvollständigen Ausschlussliste führte. (TGT-54422)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Details anzeigen

* **Enhanced Experience Composer (EEC)-Statusanzeige in der [!UICONTROL Visual Experience Composer].** Der EEC-Indikator gibt an, ob Enhanced Experience Composer aktiviert ist. Die Darstellung wurde überarbeitet, sodass sie nicht mehr einem interaktiven Umschalter ähnelt, da sie nur als nicht interaktive Statusanzeige dient. (TGT-54828)

* **Reduzierbare linke Leiste im [!UICONTROL Visual Experience Composer].** Die linke Leiste kann jetzt reduziert werden, während eine Aktivität zur Bearbeitung geöffnet ist. Dadurch wird der Zugriff auf **[!UICONTROL Components]** und **[!UICONTROL Properties]** für Aktivitäten verbessert, die mehrere Zielgruppen und Seiten enthalten, auch auf kleineren Displays. (TGT-54269)

+++

## [!DNL Target Standard/Premium] 26.3.7 (26. März 2026)

**Zielgruppen**

+++Details anzeigen

* **Genauigkeit der Beschriftung der Zielgruppenquelle in der Benutzeroberfläche „Zielgruppen“.** Es wurde ein Problem behoben, bei dem Zielgruppen aus dem Adobe Target v2-Ziel in Adobe Experience Platform mit **Adobe Experience Cloud** als Quelle anstelle von **Adobe Experience Platform angezeigt**. Diese Aktualisierung verbessert die Konsistenz der Quellkennzeichnung beim Filtern und Überprüfen von Zielgruppen. (TGT-54802)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md) | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind. |
| [Versionshinweise für vorherige Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Sehen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium an. |
| [Versionshinweise zu Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de){target=_blank} | Sehen Sie sich die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an. |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| [Adobe Priority-Produktaktualisierung](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
