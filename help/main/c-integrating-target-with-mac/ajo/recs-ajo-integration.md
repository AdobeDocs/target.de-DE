---
keywords: ajo; Adobe Journey Optimizer; Adobe Journey Optimizer-Target-Integration; Empfehlungen; Target-Empfehlungen; Integration
description: Integrieren [!DNL Adobe Target Recommendations] mit [!DNL Adobe Journey Optimizer].
title: Verwendung [!DNL Target Recommendations] bei Journey, die [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
source-git-commit: ce74c85380333476b97f47fab4d2659a3c9c86e1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# Integrieren [!DNL Adobe Target Recommendations] und [!DNL Adobe Journey Optimizer]

In diesem Artikel werden Anwendungsfälle und Informationen erläutert, die Sie bei der Einrichtung der Integration zwischen [!DNL Adobe Target Recommendations] und [!DNL Adobe Journey Optimizer] um Ihnen zu helfen, Ihren Kunden verknüpfte, kontextbezogene und personalisierte Erlebnisse bereitzustellen.

Diese Integration hilft Ihnen, mehr Konversionen zu fördern und die Auswirkungen von E-Mail-Nachrichten mit personalisierten Empfehlungen zu sehen.

## Voraussetzungen 

So verwenden Sie die [!DNL Target Recommendations] und [!DNL Adobe Journey Optimizer] -Integration benötigen Sie Folgendes:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implementiert mithilfe der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

  Diese Funktion ist nicht verfügbar bei einer [!DNL Target Standard] Lizenz oder bei der Implementierung [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Anwendungsbeispiele

Dies sind nur einige mögliche Anwendungsfälle für die Integration von [!DNL Target Recommendations] mit [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]sendet eine personalisierte E-Mail nach einem Warenkorbabbruch**: Dieser Anwendungsfall basiert auf einem Kunden, der eine Website besucht, Artikel in den Warenkorb legt und dann die Site verlässt, ohne den Kaufprozess abzuschließen.

  Angenommen, ein Besucher besucht die Website eines Bekleidungsunternehmens und legt zwei Wintermäntel und ein Pullover in den Warenkorb. Der Besucher wird dann abgelenkt und verlässt die Website oder ist sich der Käufe nicht sicher und schließt den Browser oder die App.

  Nach einem bestimmten Zeitraum, vielleicht ein paar Stunden oder einen Tag, wird in [!DNL Adobe Journey Optimizer] führt einen Aufruf an [!DNL Target Recommendations] , um den Inhalt des abgebrochenen Warenkorbs mithilfe einer [Warenkorbbasierte Empfehlungen](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) -Algorithmus. [!DNL Adobe Journey Optimizer] sendet diesem Besucher eine personalisierte E-Mail, um ihn daran zu erinnern, dass der Kaufvorgang nicht abgeschlossen wurde, sowie Bilder und Links zu den abgebrochenen Artikeln.

* **[!DNL Adobe Journey Optimizer]sendet eine Massen-E-Mail nach Site-Besuchen, um Besucher daran zu erinnern, welche Artikel angezeigt wurden**: Dieser Anwendungsfall basiert auf Besuchern, die eine Website besuchen, verschiedene Artikel anzeigen und dann die Site oder App verlassen, ohne Artikel in den Warenkorb zu legen.

  Nach einem bestimmten Zeitraum wird eine benutzerdefinierte Aktion in [!DNL Adobe Journey Optimizer] führt einen Aufruf an [!DNL Target Recommendations] , um mithilfe der Variablen [!DNL Adobe Experience Cloud Identifier] (EDID), der [!DNL Target] und ein [benutzerbasiert](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) -Algorithmus. [!DNL Adobe Journey Optimizer] sendet dann jedem Mitglied der qualifizierten Zielgruppe eine personalisierte E-Mail mit Bildern und Links zu den angezeigten Elementen jedes Besuchers, damit der Besucher zurückkehrt und einen Kauf tätigt.

  In diesem Szenario wird die [!UICONTROL Experience Cloud-Besucher-ID] (ECID) und den Inhalt der [!DNL Target] profile wird verwendet, um die Empfehlung basierend auf dem kürzlich angezeigten Algorithmus zu generieren.

  Angenommen, ein Besucher besucht eine Einzelhandelswebsite und sieht sich mehrere Uhren an. Der [!DNL Target] Profil mit einer Liste der angezeigten Uhren aktualisiert. Verwenden der ECID und des [!DNL Target] Profil, [!DNL Target] sendet die Empfehlung an [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] sendet dann mithilfe des kürzlich angezeigten Algorithmus eine E-Mail mit Bildern und Links zu den Uhren, die der Besucher angesehen hat. Ein anderer Besucher erhält eine personalisierte E-Mail mit Bildern und Links zu den von diesem Besucher angezeigten Elementen. Jede E-Mail-Nachricht wird für jeden Besucher personalisiert.

* **[!DNL Adobe Journey Optimizer]sendet nach dem Site-Besuch eine Massen-E-Mail an qualifizierte Besucher, um beliebte Artikel vorzuschlagen.**: Dieser Anwendungsfall basiert auf einem Besucher, der eine Website besucht, aber keine bestimmten Elemente anzeigt. Die E-Mail wird stapelweise an alle Personen gesendet, die sich für eine bestimmte Zielgruppe qualifizieren, z. B.:

  Angenommen, der Besucher sieht keine bestimmten Uhren. Vielleicht hat der Besucher einfach auf die Site geklickt und Kategorieseiten oder Blogeinträge angezeigt. Daher wird die Variable [!DNL Target] -Profil verfügt nicht über bestimmte Informationen zu kürzlich angezeigten Elementen. In diesem Fall [!DNL Target Recommendations] verwendet eine [Reserveempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md) so [!DNL Adobe Journey Optimizer] kann eine E-Mail mit Bildern und Links zu beliebten Artikeln auf der Website senden, um den Besucher zur Rückkehr zu bewegen und möglicherweise einen Kauf zu tätigen.


