---
keywords: ajo; Adobe Journey Optimizer; Adobe Journey Optimizer-Target-Integration; Empfehlungen; Target-Empfehlungen; Integration
description: Integrieren Sie [!DNL Adobe Target Recommendations] in [!DNL Adobe Journey Optimizer].
title: Wie verwende ich [!DNL Target Recommendations] in Journey mit [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
exl-id: 81bbbd51-47fc-4e23-a1cb-7c18fea1c159
source-git-commit: 36af6518c90ec4e055747d633b7721e5491a8d64
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 1%

---

# Integrieren von [!DNL Adobe Target Recommendations] und [!DNL Adobe Journey Optimizer]

In diesem Artikel werden Anwendungsfälle und Informationen erläutert, die Sie bei der Einrichtung der Integration zwischen [!DNL Adobe Target Recommendations] und [!DNL Adobe Journey Optimizer] unterstützen, damit Sie Ihren Kunden verknüpfte, kontextbezogene und personalisierte Erlebnisse bereitstellen können.

Diese Integration hilft Ihnen, mehr Konversionen zu fördern und die Auswirkungen von E-Mail-Nachrichten mit personalisierten Empfehlungen zu sehen.

## Voraussetzungen 

Um die Integration von [!DNL Target Recommendations] und [!DNL Adobe Journey Optimizer] zu verwenden, benötigen Sie Folgendes:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) wurde mit dem [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank} implementiert.

  Diese Funktion ist nicht mit einer [!DNL Target Standard] -Lizenz oder bei der Implementierung von [!DNL Target] mit at.js oder anderen [!DNL Target] -SDKs verfügbar.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Anwendungsbeispiele

Dies sind nur einige mögliche Anwendungsfälle für die Integration von [!DNL Target Recommendations] mit [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]sendet eine personalisierte E-Mail nach dem stehen gelassenen Warenkorb**: Dieser Anwendungsfall basiert auf einem Besucher einer Website, dem Einfügen von Artikeln in den Warenkorb und dem anschließenden Verlassen der Site ohne Abschluss des Kaufprozesses.

  Angenommen, ein Besucher besucht die Website eines Bekleidungsunternehmens und legt zwei Wintermäntel und ein Pullover in den Warenkorb. Der Besucher wird dann abgelenkt und verlässt die Website oder ist sich der Käufe nicht sicher und schließt den Browser oder die App.

  Nach einem bestimmten Zeitraum, vielleicht ein paar Stunden oder einen Tag, führt eine benutzerdefinierte Aktion in [!DNL Adobe Journey Optimizer] einen Aufruf an [!DNL Target Recommendations] durch, um den Inhalt des abgebrochenen Warenkorbs mithilfe eines [Warenkorb-basierten Recommendations](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) -Algorithmus zu ermitteln. [!DNL Adobe Journey Optimizer] sendet diesem Besucher dann eine personalisierte E-Mail, um ihn daran zu erinnern, dass der Kaufprozess nicht abgeschlossen wurde, sowie Bilder und Links zu den abgebrochenen Artikeln.

* **[!DNL Adobe Journey Optimizer]sendet eine Massen-E-Mail nach Site-Besuchen, um Besucher daran zu erinnern, welche Artikel angezeigt wurden**: Dieser Anwendungsfall basiert auf Besuchern, die eine Website besuchen, verschiedene Artikel anzeigen und dann die Site oder App verlassen, ohne Artikel in den Warenkorb zu legen.

  Nach einem bestimmten Zeitraum führt eine benutzerdefinierte Aktion in [!DNL Adobe Journey Optimizer] einen Aufruf an [!DNL Target Recommendations] durch, um zu bestimmen, welche Elemente jeder Besucher angesehen hat. Dazu werden das [!DNL Adobe Experience Cloud Identifier] (EDID), das [!DNL Target] -Profil des Besuchers und ein [benutzerbasierter](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) Algorithmus verwendet. [!DNL Adobe Journey Optimizer] sendet dann jedem Mitglied der qualifizierten Zielgruppe eine personalisierte E-Mail mit Bildern und Links zu den angezeigten Elementen jedes Besuchers, damit der Besucher zurückkehrt und einen Kauf tätigt.

  In diesem Szenario werden die [!UICONTROL Experience Cloud Visitor ID] (ECID) und der Inhalt des [!DNL Target] -Profils jedes Besuchers verwendet, um die Empfehlung basierend auf dem kürzlich angezeigten Algorithmus zu generieren.

  Angenommen, ein Besucher besucht eine Einzelhandelswebsite und sieht sich mehrere Uhren an. Das [!DNL Target] -Profil dieses Besuchers wird mit einer Liste der angezeigten Uhren aktualisiert. Unter Verwendung der ECID und des Besucherprofils [!DNL Target] sendet [!DNL Target] die Empfehlung an [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] sendet dann mithilfe des kürzlich angezeigten Algorithmus eine E-Mail mit Bildern und Links zu den Uhren, die dieser Besucher angesehen hat. Ein anderer Besucher erhält eine personalisierte E-Mail mit Bildern und Links zu den von diesem Besucher angezeigten Elementen. Jede E-Mail-Nachricht wird für jeden Besucher personalisiert.

* **[!DNL Adobe Journey Optimizer]sendet eine Massen-E-Mail an qualifizierte Besucher nach dem Site-Besuch, um beliebte Artikel vorzuschlagen**: Dieser Anwendungsfall basiert auf einem Besucher, der eine Website besucht, aber keine bestimmten Artikel anzeigt. Die E-Mail wird stapelweise an alle Personen gesendet, die sich für eine bestimmte Zielgruppe qualifizieren, z. B.:

  Angenommen, der Besucher sieht keine bestimmten Uhren. Vielleicht hat der Besucher einfach auf die Site geklickt und Kategorieseiten oder Blogeinträge angezeigt. Daher verfügt das Profil [!DNL Target] nicht über bestimmte Informationen zu kürzlich angezeigten Elementen. In diesem Fall verwendet [!DNL Target Recommendations] eine [Reserveempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md), damit [!DNL Adobe Journey Optimizer] eine E-Mail mit Bildern und Links zu beliebten Artikeln auf der Website senden kann, damit der Besucher zurückkehrt und möglicherweise einen Kauf tätigt.
