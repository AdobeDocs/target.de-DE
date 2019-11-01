---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder kommenden Adobe Target-Versionen enthalten.
keywords: Versionshinweise;Versionen;Aktualisierungen;Zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen
seo-description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
seo-title: Versionshinweise zu Adobe Target
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 5f05f218e5fdea26827b86cb7fbea05ac6349014

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert am: 31. Oktober 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target-Plattform (31. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Java SDK | Mit dem [!DNL Target] Java-SDK können Sie [!DNL Target] serverseitig bereitstellen. Mit diesem Java-SDK können Sie problemlos [!DNL Target] mit anderen [!DNL Adobe Experience Cloud] Lösungen wie dem [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]und [!DNL Adobe Audience Manager]dem<br>Das Java-SDK führt Best Practices ein und entfernt bei der Integration mit [!DNL Target] unserer Bereitstellungs-API Komplexitäten, sodass sich Ihre Entwicklungsteams auf die Geschäftslogik konzentrieren können. Die folgenden bemerkenswerten Funktionen werden in der neuesten Version eingeführt:<ul><li>Unterstützung für Vorab-Abruf und Benachrichtigungen, die eine Leistungsoptimierung durch Zwischenspeicherung ermöglichen.</li><li>Unterstützung für die Leistungsoptimierung, wenn Sie eine Hybrid-Integration von sowohl auf Ihren Webseiten als auch auf [!DNL Target] der Serverseite haben. Wir führen eine Einstellung ein, `serverState` die von Erlebnissen gefüllt wird, die serverseitig abgerufen werden, sodass at.js 2.2 keinen zusätzlichen Serveraufruf mehr ausführt, um die Erlebnisse abzurufen. Dieser Ansatz optimiert die Seitenladeleistung.</li><li>Unterstützung für das Abrufen von VEC-erstellten Aktivitäten über das Java-SDK, das durch die neue API zur Auslieferung ermöglicht wird.</li><li>Open Source, damit Ihre Entwickler zum Java-SDK[von ](https://github.com/adobe/target-java-sdk)Target beitragen können.</li></ul>Weitere Informationen finden Sie unter [Versionshinweise - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md).<br>Weitere Informationen zum Target Java SDK finden Sie im Adobe Tech Blog - [Serverseitige Optimierung mit dem neuen Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2). |

## Target Standard/Premium 19.10.2 (31. Oktober 2019)

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| ![Premium-Zeichen](/help/assets/premium.png) Arbeiten mit Attributen mit mehreren Werten | Manchmal möchten Sie mit einem Feld mit mehreren Werten arbeiten. Sehen Sie sich folgende Beispiele an:<ul><li>Sie bieten den Benutzern Filme an. Ein Film hat mehrere Schauspieler.</li><li>Sie verkaufen Tickets für Konzerte. Ein Benutzer hat mehrere Lieblingsbands.</li><li>Du verkaufst Kleidung. Ein Hemd ist in verschiedenen Größen erhältlich.</li></ul>Um Empfehlungen in diesen Szenarien zu bearbeiten, können Sie Daten mit mehreren Werten an Target Recommendations weiterleiten und spezielle Operatoren mit mehreren Werten verwenden. |

## Target Standard/Premium 20.1.1

Die Target Standard/Premium-Version 20.1.1 wird im Januar 2020 veröffentlicht. Das genaue Datum, die Funktionen und Verbesserungen werden hier bekannt gegeben.

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
