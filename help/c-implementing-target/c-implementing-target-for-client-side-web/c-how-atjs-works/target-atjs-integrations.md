---
description: In diesem Artikel werden gängige Integrationen mit Target und der jeweilige Status der Unterstützung mit „at.js“ beschrieben.
keywords: at.js-Integration;unterstützte Integrationen;nicht unterstützte Integrationen;Drittanbieter-Integrationen
seo-description: In diesem Artikel werden gängige Integrationen mit Target und der jeweilige Status der Unterstützung mit „at.js“ beschrieben.
seo-title: „at.js“-Integrationen
solution: Target
title: „at.js“-Integrationen
topic: Standard
uuid: 19036a1d-941c-4d31-8c7b-f50c86996b1c
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# „at.js“-Integrationen{#at-js-integrations}

In diesem Artikel werden gängige Integrationen mit [!DNL Target] und der jeweilige Status der Unterstützung mit at.js beschrieben.

Wenn Sie eine Integration benötigen, die nicht unterstützt oder hier nicht erwähnt wird, wenden Sie sich an Ihren Kundenbetreuer oder Berater.

## Unterstützte Integrationen {#section_3B44A970D3FB42D1973701452C868B55}

| Integration | Details |
|--- |--- |
| Analytics for Target (A4T) | Siehe [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](../../../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). |
| Profile und Zielgruppen (P&amp;A) | Siehe [Zielgruppen](https://marketing.adobe.com/resources/help/de_DE/mcloud/audience_library.html) in der Hilfe zu Adobe Experience Cloud und Core Services. |
| Experience Cloud ID-Dienst | Siehe [Adobe Experience Cloud ID-Dienst-Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcvid/). |
| Adobe Launch | Launch ist die Tag-Management-Plattform der nächsten Generation von Adobe und die bevorzugte Methode zur Implementierung von Adobe Target. Launch bietet Kunden eine einfache Möglichkeit, alle Analyse-, Marketing- und Werbe-Tags bereitzustellen und zu verwalten, die zur Unterstützung entsprechender Kundenerfahrungen erforderlich sind.  Weitere Informationen finden Sie unter [Implementieren von Target mit Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25). |
| Dynamic Tag Management (DTM) | Weitere Informationen finden Sie im [Handbuch zur Implementierung von Target mit Dynamic Tag Management](https://marketing.adobe.com/resources/help/de_DE/target/ov2/implementing-target-using-dynamic-tag-management.html).   Wichtig: [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) ist die bevorzugte und aktuellste Methode zur Implementierung von Target und der „at.js“-Bibliothek. Verwenden Sie für alle neuen Target-Implementierungen Launch. Die folgende Anleitung ist für bestehende Kunden bestimmt, die eine DTM-Implementierung nutzen.   Beachten Sie bei der Verwendung einer DTM-Integration Folgendes: <ul><li>Bibliotheksverwaltung: Verwenden Sie die Hosting-Option „Benutzerdefiniert“, um „at.js“ zu verwenden. Die Option „Automatisch“ wird derzeit nicht unterstützt. </li></ul> |
| Adobe Experience Manager (AEM) Cloud Service | Der AEM-Cloud-Service ermöglicht die Erstellung von A/B-Tests und Erlebnis-Targeting-Aktivitäten im AEM-Workflow. Unterstützt „at.js“ mit Adobe Experience Manager 6.2 mit FP-11577 (oder höher). Weitere Informationen finden Sie unter [Integration mit Adobe Target](https://helpx.adobe.com/de/experience-manager/6-2/sites/administering/using/target.html). Wählen Sie zuerst Ihre AEM-Version. |
| AEM-Erlebnisfragmente | Mithilfe von in AEM in Target-Aktivitäten erstellten Erlebnisfragmenten können Sie die Benutzerfreundlichkeit und Performance von AEM mit den leistungsstarken Target-Funktionen für automatisierte Intelligenz (AI) und maschinelles Lernen (ML) kombinieren, um Erlebnisse bedarfsgerecht zu testen und zu personalisieren.  AEM kombiniert all Ihre Inhalte und Assets an einer zentralen Stelle, um Ihre Personalisierungsstrategie zu begünstigen. Mit AEM können Sie an einer Stelle problemlos Inhalte für Desktops, Tablets und mobile Geräte erstellen, ohne Code zu schreiben. Es müssen keine Seiten für jedes Gerät erstellt werden - AEM passt die einzelnen Erlebnisse automatisch mit Ihren Inhalten an.  Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](../../../c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8). |

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
| Drittanbieter für Daten (z. B. Demandbase, BlueKai, Wetter-APIs) | Viele externe Datenanbieter, die zur Ergänzung der Target-Benutzerprofile eingesetzt werden, können mit der „at.js“-Funktion für [Datenanbieter](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) integriert werden.. |