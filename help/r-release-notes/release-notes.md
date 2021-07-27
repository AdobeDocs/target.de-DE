---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Versionshinweise
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 21c7675085bf5dc06bf9b1b38a82b2be4d4b0f76
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 100%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek „at.js“, um mögliche Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## at.js 2.6.0 (16. Juli 2021)

* Das Attribut „secure“ wurde zu Cookies hinzugefügt für alle Fälle, in denen die at.js-Einstellungen `secureOnly` auf `true` gesetzt sind.
* Bei Verwendung von `triggerView()` sind jetzt Antwort-Token verfügbar.
* Es wurde ein Problem im Zusammenhang mit dem Ereignis `CONTENT_RENDERING_NO_OFFERS` behoben. Jetzt wird dieses Ereignis korrekt ausgelöst, wenn kein Inhalt von [!DNL Target] zurückgegeben wird.
* Details zur Klickmetrik von [!DNL Anlytics for Target] (A4T) werden bei der Verwendung von `prefetch`-Anfragen korrekt zurückgegeben.
* Die UUID-Generierung verwendet nicht mehr `Math.random()`, sondern beruht auf `window.crypto`.
* Der Ablauf des `sessionId`-Cookies wird bei jedem Netzwerkaufruf korrekt verlängert.
* Die Ansichts-Cache-Initialisierung für die [!UICONTROL Einzelseiten-Anwendung] (SPA, Single Page Application) wird jetzt korrekt verarbeitet und berücksichtigt die Einstellungen `viewsEnable`.

## [!DNL Target Standard/Premium] 21.6.1 (30. Juni 2021)

Diese Version beinhaltet die folgenden neuen Funktionen und Verbesserungen. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

| Funktion | Details |
| --- | --- |
| [!UICONTROL Analytics for Target] (A4T) | Wenn Sie auf der Seite [!UICONTROL Berichte] auf den Link ]In Analytics anzeigen[!UICONTROL  in einer Aktivität klicken, die [!DNL Analytics] als Berichtsquelle (A4T) verwendet, wird jetzt [!DNL Analysis Workspace] geöffnet. Zuvor wurden durch den Link die Berichte von [!DNL Analytics] geöffnet. (TGT-36959) |

## Python SDK 1.0.0 (16. Juni 2021)

Das neue [!DNL Adobe Target] Python-SDK mit Funktionen zur geräteinternen Entscheidungsfindung ist jetzt verfügbar. Diese neueste Erweiterung ergänzt die [!DNL Target]-Suite der Server-seitigen SDKs. Diese SDKs helfen Ihnen bei der Integration mit [!DNL Target] und beschleunigen Ihre Time-to-Value – und all das in der Sprache Ihrer Wahl. Server-seitige Integrationen werden immer beliebter, da sich der Markt in eine Cookie-freie Welt verlagert, in der First-Party-Daten wertvoll sind. Target-SDKs sind in den gängigsten Programmiersprachen auf dem Markt verfügbar (Python, Java, JavaScript, C# / .Net).

Weitere Informationen finden Sie in der [Dokumentation zum Python SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/python-sdk) im Handbuch [Adobe Target SDKs](https://adobetarget-sdks.gitbook.io/docs/).

## ![Adobe Experience Platform Web SDK-Badge](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK]Version 2.5.0 (1. Juni 2021)

Diese Version von [!DNL Platform Web SDK] unterstützt Folgendes:

| Funktion | Details |
| --- | --- |
| Umleitungs-Unterstützung mit [!UICONTROL Analytics for Target] (A4T) | Das Platform Web SDK unterstützt jetzt Umleitungen von [!DNL Target] bei der Verwendung von [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Weitere Informationen finden Sie unter [Analytics für die  [!DNL Target] -Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority-Produktaktualisierung | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
