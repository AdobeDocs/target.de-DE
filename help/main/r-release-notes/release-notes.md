---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 839ca14d658115ebdb2d4b3239f3ea5efff1fa60
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 93%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## at.js-Version 2.10.1 (2. Februar 2023)

* Es wurde ein Fehler behoben, durch den Aktivitäten mit Zielgruppenregeln, die Parameter mit Punkten in ihren Namen enthielten, nicht das erwartete Erlebnis für die Entscheidungsfindung auf dem Gerät zurückgaben.
* Es wurde ein Fehler behoben, der in at.js 2.6.0 eingeführt wurde und in dem at.js einen Bereitstellungsaufruf auslöste, selbst wenn `mboxDisable` aktiviert wurde.

Informationen zu allen at.js-Versionen finden Sie unter [&quot;at.js&quot;-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## [!DNL Target] Standard/Premium 22.13.3 (25.-26. Januar 2023)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **25. Januar**: Region Europa, Naher Osten und Afrika (EMEA)
* **25. Januar**: Region Asien-Pazifik (APAC)
* **26. Januar**: Region Nord- und Südamerika

Diese Version umfasst die folgenden neuen Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Details |
| --- | --- |
| Unterstützung von [JSON-Angeboten](/help/main/c-experiences/c-manage-content/create-json-offer.md) in Automated Personalization (AP) | Jetzt werden JSON-Angebote in Aktivitäten von [!UICONTROL Automated Personalization] (AP) unterstützt, für die der formularbasierte Experience Composer verwendet wird. (TGT-41460) |
| [AEM Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | Es wurde die Möglichkeit hinzugefügt, zwischen Fragmenttypen in [!DNL Adobe Experience Manager] (AEM XF) zu unterscheiden, die nach [!DNL Target] exportiert werden. Anstelle der Option „Experience Fragment“ ermöglicht es Ihnen [!DNL Target] nun, nach „HTML XF“ und „JSON XF“ zu filtern und zu suchen. (TGT-44132) |

* Es wurde ein Problem behoben, das zu einem „Fehler 500“ in [!UICONTROL A/B-Test-] und [!UICONTROL Experience Targeting] (XT)-Aktivitäten, die Empfehlungen enthalten, führte. Dieses Problem trat auf, wenn [!DNL Target] nicht mehr verwendete Kriterienobjekte nicht ordnungsgemäß aus der [!DNL Target]-Benutzeroberfläche und dem [!DNL Recommendations]-Backend löschen konnte. (TGT-44383)
* Der Speicherort wurde aus dem angezeigten Angebotsnamen im Bericht auf [!UICONTROL Angebotsebene] für [!UICONTROL Automated Personalization]-Aktivitäten entfernt. Durch diese Änderung wird der Bericht leichter lesbar. (TGT-44294)
* Die Kalenderoptionen für 45 Tage und 90 Tage wurden aus den AP- und [!UICONTROL Auto-Target] [!UICONTROL Personalisierungs-Insights] sowie aus den Berichten zu [!UICONTROL wichtigen Attributen] in der [!DNL Target]-Benutzeroberfläche entfernt. Aufgrund von Nutzungsmustern und im Hinblick auf eine Verbesserung der Leistung werden diese Datumsbereiche nicht mehr unterstützt. Die Benutzeroberfläche wurde mit den derzeit zulässigen Bereichen aktualisiert: 15, 30 und 60 Tage. (TGT-39357)
* Die Möglichkeit, die Einstellung [!UICONTROL Wie Optimierungsziel] auf der Seite [!UICONTROL Ziele und Einstellungen] zu ändern, nachdem die Aktivität live ist, wurde entfernt. (TGT-43923)
* Es wurde ein Problem behoben, das beim Upgrade von [!DNL Target Standard] nach [!DNL Target Premium] zu Problemen mit dem standardmäßigen Arbeitsbereich im [!DNL Target]-Backend führte. (TGT-44081 und TGT-44306)
* Es wurde eine Änderung vorgenommen, sodass [!DNL Analytics] Report Suites mit dem Punktsymbol „.“ im Namen in der Benutzeroberfläche von [!DNL Target] nun zum Erstellen von [!DNL Analytics]-Klassifizierungs-Feeds verwendet werden können.
* Der Link auf der Seite [!UICONTROL Implementierung] ([!UICONTROL Verwaltung] > [!UICONTROL Implementierung]) für „Implementierungsmethoden mit On-Device Decisioning“ wurde geändert, um auf die Seite verweisen, auf der erläutert wird, wie Sie die geräteinterne Entscheidungsfindung für alle unterstützten SDKs verwenden können: Node.js, Java, .NET und Python. Weitere Informationen finden Sie unter [Erste Schritte mit Target-SDKs](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Ein Fehler, der bei Verwendung von [!DNL Scene7] und [!DNL Target] zu Problemen mit Datei-Uploads führte, wurde behoben.
* Die Barrierefreiheit der [!DNL Target]-Benutzeroberfläche für Personen mit Behinderungen wurde auf Grundlage der Ergebnisse eines internen Usability-Audits verbessert. Es wird nun Zugriff auf Funktionen geboten, auf die zuvor nicht über die Tastatur zugegriffen werden konnte, die Alternativtexte wurden verbessert, Teile der Benutzeroberfläche können nun vergrößert werden, um sie besser verwenden zu können, der Tastaturfokus wurde verbessert und mehr. (TGT-42759)
* Es wurden in der gesamten [!DNL Target]-Benutzeroberfläche Lokalisierungskorrekturen vorgenommen.

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [at.js-Versionsdetails](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md). |
