---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: 'https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
  - id: c5abb976-5170-45d6-bcac-66d15d10a4d4
    internal-label: Release notes
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ece061af0f50ec45e07b9710d355a9c91731578e
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 42%
---
# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 26.10.2 (15. Oktober 2026)

**[!UICONTROL Aktivitäten]**

+++Details anzeigen

* **Falsche Zieleinstellungen in der Aktivitätsübersicht angezeigt**. Es wurde ein Problem behoben, bei dem die Zieleinstellungen, die auf der Seite **[!UICONTROL Übersicht]** einer Aktivität angezeigt wurden, falsch waren. Beispielsweise wurde `https://` zur Seiten-URL hinzugefügt und die Bedingung **[!UICONTROL URL enthält]** wurde nicht angezeigt, obwohl die tatsächliche Zielkonfiguration korrekt war. (TGT-56326)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen

* **Backup-Empfehlungen, die angezeigt werden, nachdem eine Promotion in einer Live-Aktivität aktualisiert wurde**. Es wurde ein Problem behoben, bei dem das Bearbeiten einer Promotion in einer Live [!DNL Recommendations]-Aktivität dazu führte, dass [!DNL Target] neue Promotion- und Empfehlungseinheiten erstellte, obwohl sich in ihrer Definition nichts änderte. (TGT-56369)

+++

**[!UICONTROL Berichte]**

+++Details anzeigen

* **Berichtvorgaben nach zwei Wochen gelöscht**. Es wurde ein Problem behoben, bei dem die Berichtsvoreinstellungen, die Benutzende für eine Aktivität gespeichert hatten, nach etwa zwei Wochen automatisch gelöscht wurden. (TGT-56374)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Safari-Unterstützung zu[!DNL Adobe Target]** hinzugefügt. [!DNL Target] wird jetzt im [!DNL Safari]-Browser unterstützt. Beachten Sie, dass Visual Experience Composer und [!DNL Enhanced Experience Composer] in [!DNL Safari] nicht unterstützt werden. Daher wird jetzt im [!DNL VEC] eine Überlagerung angezeigt, die Benutzer darüber informiert, dass sie zur Verwendung des Editors zu [!DNL Chrome] wechseln müssen. (TGT-55853)
  [Weitere Informationen](../c-experiences/c-visual-experience-composer/visual-experience-composer.md#browser-requirements)
+++


## [!DNL Target Standard/Premium] 26.10.1 (13. Oktober 2026)

**[!UICONTROL Analytics for Target]**

+++Details anzeigen

* **A4T-Reporting schlägt mit dem Fehler „Irgendetwas ist schiefgelaufen“**. Es wurde ein Problem behoben, bei dem bei [!DNL A4T] Aktivitäten mit einer neu hinzugefügten Report Suite im [!DNL Target] Bericht der Fehler „Etwas ist schiefgelaufen“ anstelle der Ergebnisse angezeigt wurde. Wenn Sie **[!UICONTROL In Analytics anzeigen]** klicken, wird auch die Meldung „Inkompatible Report Suite“ mit fehlenden [!DNL Analytics for Target] angezeigt. (TGT-56389)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen

* **Raw-HTML wird anstelle des Angebotsnamens für [!DNL Experience Fragments] angezeigt, die über eine Mbox bereitgestellt werden**. Es wurde ein Problem behoben **[!UICONTROL bei dem im Bedienfeld]**&#x200B;Änderungen“ rohe HTML/Code anstelle des Angebotsnamens angezeigt wurde, wenn ein [!DNL Experience Fragment] über eine Mbox bereitgestellt wurde. (TGT-56241)

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
| [Adobe Priority-Produktaktualisierung](https://www.adobe.com/de/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
