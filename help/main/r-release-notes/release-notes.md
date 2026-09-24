---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 4d083419d76b0287c3c254a0fc382abc7444cc75
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 32%
---
# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 26.9.6 (24. September 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Endlose Umleitungsschleife beim Zugriff auf eine SSO-authentifizierte Seite über den Visual Experience Composer**. Wenn eine in Visual Experience Composer geladene Seiten-URL einen SSO-/Anmelde-Umleitungsfluss durchlief, trat Visual Experience Composer in eine endlose Umleitungsschleife ein und erreichte nie die beabsichtigte Seite. (TGT-56233)

+++

## [!DNL Target Standard/Premium] 26.9.5 (21. September 2026)

### Funktion

<table>
<thead>
<tr>
<th><strong>Vorab-Ausblenden von Inhalten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durch das Vorab-Ausblenden von Inhalten wird das Flackern der Seite reduziert, da nur die Abschnitte ausgeblendet werden, die durch die Adobe Target-Personalisierung geändert werden sollen. So wird das Erlebnis beim Laden von Inhalten reibungsloser. Dadurch wird vermieden, dass die gesamte Seite ausgeblendet wird, und der Implementierungsaufwand beim Starten neuer Aktivitäten wird minimiert.</p>
<p>Diese Funktion wurde bereits in eingeschränkter Verfügbarkeit veröffentlicht und steht nun allen Umgebungen zur Verfügung (allgemeine Verfügbarkeit).</p>
<p>Weitere Informationen finden Sie in der <a href="../administrating-target/content-pre-hiding.md">ausführlichen Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

### Verbesserungen

**[!UICONTROL Analytics for Target]**

+++Details anzeigen

* **Link zum A4T-Bericht wird nicht in [!DNL Target] Benutzeroberfläche generiert**. Bei [!DNL A4T] Aktivitäten wurde der Berichtlink nicht im Abschnitt **[!UICONTROL Berichte]** generiert, obwohl die zugrunde liegenden Berichtsdaten sowohl in der [!DNL Target]-Benutzeroberfläche als auch in der [!DNL Adobe Analytics]-Benutzeroberfläche sichtbar waren. (TGT-56247)

+++

## [!DNL Target Standard/Premium] 26.9.4 (17. September 2026)

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **[!UICONTROL Einfügen vor]-Steuerelement, auf das [!DNL Experience Fragments] im obersten Seitenelement nicht zugreifen**. Wenn Sie im Visual Experience Composer das oberste Element auf einer Seite auswählen, wird die Seite nach oben gescrollt, wodurch das Steuerelement **[!UICONTROL Einfügen vor]** über dem sichtbaren Ansichtsfenster gerendert wird, in dem es nicht ausgewählt werden konnte. (TGT-55829)

+++

## [!DNL Target Standard/Premium] 26.9.3 (16. September 2026)

**[!UICONTROL Berichterstellung]**

+++Details anzeigen

* **Fehlende Werte [!UICONTROL Anstieg] und [!UICONTROL Konfidenz] in einigen [!DNL A4T Auto-Target] Berichten**. Bei [!DNL A4T Auto-Target] Aktivitäten mit dem Optimierungsziel **[!UICONTROL Maximieren der Besuchsumrechnungsrate]** wurde die standardmäßige Berichtsmetrik **[!UICONTROL Meine Primäre Metrik]** nicht korrekt aufgelöst, sodass **[!UICONTROL Anstieg]** und **[!UICONTROL Konfidenz]** leer blieb. (TGT-56137)

+++

**[!UICONTROL Analytics for Target]**

+++Details anzeigen

* **[!UICONTROL Reporting-Source]-Feld ist jetzt schreibgeschützt für Live-Aktivitäten ohne [!DNL Analytics] Zugriff**. Wenn der Eigentümer einer Live-Aktivität keinen Zugriff auf [!DNL Adobe Analytics] hatte, konnten das Feld **[!UICONTROL Reporting-Source]** und das zugehörige Feld weiterhin bearbeitet werden. (TGT-56089)

+++

## [!DNL Target Standard/Premium] 26.9.2 (8. September 2026)


**[!UICONTROL Recommendations]**

+++Details anzeigen

* **[!DNL New]Benutzeroberfläche codiert Feed-URLs falsch**. Beim Erstellen eines Recommendations-Feeds über eine URL in der neuen [!DNL Target] wurde die Feed-URL falsch codiert, was dazu führte, dass die Feed-Erstellung mit einem unbekannten Fehler fehlschlug. (TGT-56084)

+++

**[!UICONTROL Berichterstellung]**

+++Details anzeigen

* **Der Bericht „Automatisierte Segmente“ zeigt Attributwerte nicht konsistent**. Der Bericht Automatisierte Segmente zeigt Attributwerte und -bereiche für [!DNL Automated Personalization]- und [!DNL Auto-Target]-Aktivitäten inkonsistent an. Einige automatisierte Segmente zeigen nur den Attributnamen anstelle des zugehörigen Werts oder Bereichs an. (TGT-55855)

+++

## [!DNL Target Standard/Premium] 26.9.1 (1. September 2026)

**[!UICONTROL Zielgruppe]**

+++Details anzeigen

* **Das Kopieren einer Aktivität mit einer Zielgruppe „Nur Aktivität“ schlägt fehl beim Speichern**. Wenn eine A/B-Aktivität eine Zielgruppenregel „Nur Aktivität“ (lokal) und eine benutzerdefinierte Code-Änderung verwendet, schlägt das Kopieren und Speichern der Kopie mit dem Fehler „Ungültige Zielgruppen-IDs“ fehl. (TGT-55785)

+++

**[!DNL Adobe Target]MCP-Server — Recommendations-Tools (Public Beta)**

+++Details anzeigen

Der [!DNL Adobe Target] MCP-Server stellt jetzt Recommendations-Tools bereit, mit denen Sie Kriterien, Sammlungen, Designs, Promotions und Ausschlüsse auflisten, überprüfen, erstellen und aktualisieren und den Produktkatalog direkt über Ihren KI-Assistenten durchsuchen können.

Für diese Funktion ist ein Recommendations-aktivierter Mandant mit **Target Premium** erforderlich. Sie ist nicht für Nicht-Premium-Konten verfügbar.

Weitere Informationen finden Sie unter [MCP Server Tools-Referenz](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md).

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
