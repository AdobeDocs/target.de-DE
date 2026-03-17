---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
hold: true
source-git-commit: 44d9cd4de7ff2064e6005a4d7ece7f37194fbf2f
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 41%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.3.2 (10. März 2026)

**Aktivitäten**

+++Details anzeigen

* **Direkte Angebotsänderungen in werden nicht gespeichert.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem Änderungen an direkten Angeboten innerhalb eines Aktivitätserlebnisses nicht gespeichert wurden. Zuvor, als Benutzer ein Direktangebot öffneten, Änderungen vornahmen und speicherten, schienen die Änderungen zunächst widergespiegelt, gingen aber beim erneuten Öffnen des Angebots verloren. Die Korrektur stellt sicher, dass Änderungen an direkten Angeboten ordnungsgemäß gespeichert werden und beim erneuten Öffnen des Angebots beibehalten werden. (TGT-54653)

+++

**Implementierung**

+++Details anzeigen

* **Im Bildschirm Implementierung den Umschalter für die Flackerverwaltung hinzufügen.** Dem Bildschirm [!UICONTROL Implementation] wurde ein neuer Umschalter hinzugefügt, um die Aktivierung der Einstellung für die Flimmerverwaltung zu steuern. Mit diesem Umschalter können Administratoren die Flimmerverwaltung direkt im Bildschirm Implementierung konfigurieren. (TGT-52247)

+++

**Übersicht**

+++Details anzeigen

* **Vollständiger Name der Zielgruppe und des Erlebnisses auf der Übersichtsseite anzeigen.** Diese Verbesserung aktualisiert die [!UICONTROL Overview]-Seite, um den vollständigen Namen der Zielgruppen und Erlebnisse anzuzeigen. Zuvor waren lange Namen abgeschnitten und nicht vollständig sichtbar, sodass Benutzende dreifach klicken mussten, um den gesamten Text auszuwählen und den vollständigen Namen anzuzeigen. Die Aktualisierung stellt sicher, dass vollständige Zielgruppen- und Erlebnisnamen sichtbar sind, sodass Benutzende Aktivitätskonfigurationen leichter identifizieren und überprüfen können. (TGT-53323)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **VEC-Änderungen werden nicht auf Sites widergespiegelt, die Shadow DOM (Salesforce Lightning Web Components) verwenden.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem in Adobe Target vorgenommene Änderungen (z. B. Farbänderungen in CTA) nicht gespeichert oder auf der Live-Site für Salesforce-basierte Sites, die Lightning Web Components (LWC) verwenden, wiedergegeben wurden. Der CMS akzeptierte keine Aktualisierungen von Target-Aktivitäten, und dieses Problem trat in A/B-Tests und anderen Aktivitätstypen durchgängig auf. (TGT-54059)

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
