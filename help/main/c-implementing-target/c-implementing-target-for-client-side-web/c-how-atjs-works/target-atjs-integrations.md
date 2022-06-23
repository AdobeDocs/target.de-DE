---
keywords: at.js-Integration;unterstützte Integrationen;nicht unterstützte Integrationen;Drittanbieter-Integrationen
description: Siehe Von Adobe unterstützte (und nicht unterstützte) Integrationen [!DNL Target] at.js, einschließlich Analytics für [!DNL Target] (A4T), dem Experience Cloud-ID-Dienst und mehr.
title: Welche Integrationen unterstützt at.js?
feature: at.js
role: Developer
exl-id: 148c744d-2a2b-40f8-964b-c51283ae7d1c
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 82%

---

# „at.js“-Integrationen

In diesem Artikel werden gängige Integrationen mit [!DNL Target] und der jeweilige Status der Unterstützung mit at.js beschrieben.

Wenn Sie eine Integration benötigen, die nicht unterstützt oder hier nicht erwähnt wird, wenden Sie sich an Ihren Kundenbetreuer oder Berater.

## Unterstützte Integrationen {#section_3B44A970D3FB42D1973701452C868B55}

| Integration | Details |
|--- |--- |
| Analytics for Target (A4T) | Siehe [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). |
| Profile und Zielgruppen (P&amp;A) | Siehe [Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de) im *Hauptdienste-Benutzerhandbuch*. |
| Experience Cloud ID-Dienst | Siehe [Dokumentation des Adobe Experience Cloud ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| Tags in [!DNL Adobe Experience Platform] | Tags in [!DNL Adobe Experience Platform] sind die nächste Generation von Tag-Management-Funktionen von [!DNL Adobe]. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerlebnisse erforderlich sind. Siehe [Implementierung [!DNL Target] using [!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/). |
| Adobe Experience Manager (AEM) Cloud Service | Der AEM-Cloud-Service ermöglicht die Erstellung von A/B-Tests und Erlebnis-Targeting-Aktivitäten im AEM-Workflow. Unterstützt „at.js“ mit Adobe Experience Manager 6.2 mit FP-11577 (oder höher). Weitere Informationen erhalten Sie, indem Sie unter [Integration in Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) Ihre AEM-Version auswählen. |
| AEM-Experience Fragments | Mithilfe von in AEM in Target-Aktivitäten erstellten Erlebnisfragmenten können Sie die Benutzerfreundlichkeit und Performance von AEM mit den leistungsstarken Target-Funktionen für automatisierte Intelligenz (AI) und maschinelles Lernen (ML) kombinieren, um Erlebnisse bedarfsgerecht zu testen und zu personalisieren.  AEM kombiniert all Ihre Inhalte und Assets an einer zentralen Stelle, um Ihre Personalisierungsstrategie zu begünstigen. Mit AEM können Sie an einer Stelle problemlos Inhalte für Desktops, Tablets und mobile Geräte erstellen, ohne Code zu schreiben. Es müssen keine Seiten für jedes Gerät erstellt werden - AEM passt die einzelnen Erlebnisse automatisch mit Ihren Inhalten an.  Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8). |

## Nicht unterstützte Integrationen {#section_8EFCAED418DC42E0B07F95924819EAC2}

| Integration | Details |
|--- |--- |
| [!DNL Legacy Target to SiteCatalyst Integration] | Hierbei handelte es sich um die Integration, bei der Kampagnen- und Rezept-IDs über den Seitenaufruf an [!DNL SiteCatalyst] gesendet wurden, damit Berichte auf der Benutzeroberfläche von [!DNL SiteCatalyst] erstellt werden konnten. Diese Funktionalität wird durch A4T ersetzt. |
| [!DNL Legacy Target to SiteCatalyst Integration] | Hierbei handelte es sich um die Integration, die Mbox-Aufrufe namens `"SiteCatalyst: Event"` und `"SiteCatalyst: Purchase"` tätigte, damit Sie Erfolgsmetriken und Benutzerprofile auf Grundlage von eVars und Eigenschaften erstellen konnten. Diese Funktionalität wird durch A4T und P&amp;A ersetzt. |
| [!DNL Legacy Audience Manager (AAM) to Target Integration] | Hierbei handelte es sich um die Integration, die Frontend-API-Aufrufe tätigte, um AAM-Segmente abzurufen, und diese anschließend als Mbox-Parameter bei jedem Mbox-Aufruf an die Seite sendete. |

## Drittanbieterintegrationen {#section_EE599839CCAD49DD97640E5EDAD9082E}

| Integration | Details |
|--- |--- |
| Andere Tag-Manager | „at.js“ sollte auch mit anderen Tag-Management-plattformen funktionieren, die nicht von Adobe stammen, grundsätzlich sollten Sie beim Einsatz benutzerdefinierter Integrationsfunktionen, die von anderen Anbietern entwickelt wurden, jedoch vorsichtig sein. Deren Integrationen sind möglicherweise von internen mbox.js-Funktionen abhängig, die es in at.js nicht mehr gibt. |
| Drittanbieter für Daten (z. B. Demandbase, BlueKai, Wetter-APIs) | Viele Drittanbieter für Daten, die zur Ergänzung der Target-Benutzerprofile verwendet werden, können mithilfe von at.js integriert werden. [Datenanbieter](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)Funktion {target=_blank}. |
