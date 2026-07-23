---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c74d8b09fba181fcded2f982d99a03f1e7f3a07a
workflow-type: tm+mt
source-wordcount: 927
ht-degree: 29%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 26.7.4 (23. Juli 2026)

**Berichterstellung**

+++Details anzeigen

* **Das Diagramm Konversionsrate ist für eine bestimmte mobile Zielgruppe nicht verfügbar.** Es wurde ein Problem behoben[!UICONTROL  bei dem das Diagramm „Konversionsrate] für bestimmte mobile Zielgruppen nicht gerendert wurde. (TGT-55611)

* **Konversionsziel „Eine Mbox angezeigt“ funktioniert nicht, wenn es aus dem Dropdown-Menü ausgewählt wird.** Es wurde ein Problem behoben, bei dem bei Auswahl einer Mbox aus der Dropdown-Liste [!UICONTROL Ziele und Einstellungen] für ein Konversionsziel vom Typ „Angezeigte Mbox“ der Mbox-Name falsch gespeichert und dadurch die Aufzeichnung von Konversionen verhindert wurde. (TGT-55588)

+++

**Zielgruppen**

+++Details anzeigen

* **Layout-Problem auf der Seite „Zielgruppenbibliothek“.** Es wurde ein Layout-Problem behoben, das auftrat, wenn Filter auf der Seite [!UICONTROL Zielgruppenbibliothek] aktiviert wurden, während die Seitennavigation reduziert war. (TGT-55502)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Mobile-Version wird nicht korrekt geladen.** Es wurde ein Problem behoben, bei dem [!UICONTROL Visual Experience Composer] keine Möglichkeit zum Aktualisieren bot und so verhinderte, dass die mobile Ansicht korrekt geladen wurde. (TGT-54408)

* **Bearbeiten oder Löschen von Änderungsaktionen funktioniert nicht.** Es wurde ein Problem behoben, bei dem das Bearbeiten oder Löschen einer Änderung aus der [!UICONTROL Erlebnis bearbeiten]-Ansicht nicht funktionierte. (TGT-55250)

* **Durchsuchen-Modus reagiert nach dem Laden der Aktivität nicht.** Es wurde ein Problem behoben[!UICONTROL  bei dem der ]Durchsuchen“ für Erlebnisse mit einer Änderung nicht mehr reagierte, was eine weitere Navigation und Bearbeitung verhinderte. (TGT-55306)

* **Elemente im Salesforce LWC (Shadow DOM) können nicht ausgewählt werden.** Es wurde ein Problem behoben, bei dem [!UICONTROL Visual Experience Composer] mithilfe von Shadow DOM keine Elemente auswählen konnte, die in Salesforce Lightning-Web-Komponenten verschachtelt waren, was zu einem Fehler „Selektor nicht gefunden“ führte. (TGT-54956)

* **Doppelte Angebote erschienen im [!UICONTROL Visual Experience Composer].** Es wurde ein Problem behoben, bei dem Änderungen und Angebote zeitweise in der Benutzeroberfläche für die Erstellung von Aktivitäten dupliziert erschienen. (TGT-55685)

+++

**Administration**

+++Details anzeigen

* **Der Assistent zur Inhaltserstellung wurde in „Inhalt [!UICONTROL &quot; ].** Die Funktion zur Inhaltserstellung von „KI-Assistent“ wurde umbenannt, um [!UICONTROL Inhalte generieren] über [!DNL Target] Benutzeroberflächenoberflächen hinweg zu ermöglichen. (TGT-55689)

+++

**Recommendations**

+++Details anzeigen

* **Beliebtheitsbasierte Recommendations unter Verwendung von Profilattributen.** [!DNL Target] unterstützt jetzt die Gruppierung von Popularitätsempfehlungen, am häufigsten angezeigt und Topverkäufe, dynamisch nach Besucherprofilattributen wie Land, bevorzugte Sprache oder Mitgliedschaftsstufe. (TAPER-7614)

* **Unstimmigkeit der Empfehlungssammlung zwischen [!UICONTROL Sammlungen] und der Aktivitätskonfiguration.** Es wurde ein Problem behoben, bei dem eine [!UICONTROL Recommendations]-Sammlung zusätzliche, nicht qualifizierte Entitäten zurückgab, wenn sie in der Aktivitätskonfiguration im Vergleich zur Ansicht [!UICONTROL Recommendations] > [!UICONTROL Sammlungen] angezeigt wurde. (TGT-55554)

+++

## [!DNL Target Standard/Premium] 26.7.2 (16. Juli 2026)

**Aktivitäten**

+++Details anzeigen

* **Falsche Zielinformationen auf der Seite [!UICONTROL Aktivitätsübersicht].** Es wurde ein Problem behoben[!UICONTROL  bei dem auf der Seite ]Aktivitätsübersicht“ für [!DNL Automated Personalization] Aktivitäten zusätzliche Ziele anstelle des Optimierungsziels angezeigt wurden. (TGT-55553)

* **Nicht reagierender Bildschirm beim Navigieren auf Seiten im [!UICONTROL Durchsuchen]-Modus.** Es wurde ein Problem behoben, bei dem der Bildschirm beim Navigieren zwischen Seiten im [!UICONTROL -Modus nicht ] reagierte. (TGT-55565)

+++

**Startseite**

+++Details anzeigen

* **Änderung der Benutzeroberfläche für [!UICONTROL Beste Leistung] und [!UICONTROL Speichert].** Die Benutzeroberfläche für die leistungsstärksten Komponenten wurde aktualisiert und das Erlebnis wird gespeichert. (TGT-54975)

+++

**Zielgruppen**

+++Details anzeigen

* **Nicht lokalisierte Zeichenfolgen im Dialogfeld [!UICONTROL Profilskript erstellen].** Es wurde ein Problem behoben, bei dem Zeichenfolgen [!UICONTROL  Dialogfeld „Profilskript erstellen] nicht lokalisiert wurden. (TGT-51527)

+++

## [!DNL Target Standard/Premium] 26.7.1 (9. Juli 2026)

**Aktivitäten**

+++Details anzeigen

* **Inkonsistente Quellanzeige auf [!UICONTROL Aktivitäten], [!UICONTROL Zielgruppen] und [!UICONTROL Angeboten] Seiten.** Es wurde ein Problem behoben, bei dem die Quelle auf den Seiten [!UICONTROL Aktivitäten], [!UICONTROL Zielgruppen] und [!UICONTROL Angebote] inkonsistent angezeigt wurde. (TGT-55247)

* **Die Aktivitätsquelle ändert sich bei der Bearbeitung über die Benutzeroberfläche.** Es wurde ein Problem behoben, bei dem durch das Bearbeiten einer Aktivität über die Benutzeroberfläche die ursprüngliche Aktivitätsquelle geändert wurde. (TGT-55248)

+++

**Zielgruppen**

+++Details anzeigen

* **Falscher Standardarbeitsbereich beim Bearbeiten einer Zielgruppe.** Es wurde ein Problem behoben, bei dem der Standardarbeitsbereich nach der Bearbeitung einer Zielgruppe falsch war. (TGT-55510)

+++

**Berichterstellung**

+++Details anzeigen

* **CSV-Download-Fehler für Mai-Berichte.** Es wurde ein Problem behoben, bei dem das Herunterladen eines CSV-Berichts für Mai fehlgeschlagen ist. (TGT-55524)

+++

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit der [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

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
