---
keywords: AJO;Adobe Journey Optimizer;Adobe Journey Optimizer-Target-Integration;Recommendations;Target-Recommendations;Integration
description: Integration  [!DNL Adobe Target Recommendations] mit [!DNL Adobe Journey Optimizer].
title: Wie verwende ich  [!DNL Target Recommendations]  Kunden-Journey [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
exl-id: 81bbbd51-47fc-4e23-a1cb-7c18fea1c159
TQID: https://experienceleague.adobe.com/JA--Ll80bDZwn9WtGqIb-z3YxyJLOvOYPzuhZeKA17w
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 637
ht-degree: 2%

---

# Integrieren von [!DNL Adobe Target Recommendations] und [!DNL Adobe Journey Optimizer]

Dieser Artikel enthält Anwendungsbeispiele und Anleitungen für die Integration von [!DNL Adobe Target Recommendations] mit [!DNL Adobe Journey Optimizer], sodass Sie vernetzte, kontextuelle und personalisierte Kundenerlebnisse bereitstellen können.

Durch diese Integration können Sie mehr Konversionen fördern und die Wirkung von E-Mail-Nachrichten mit personalisierten Empfehlungen sehen.

## Voraussetzungen

Um die Integration von [!DNL Target Recommendations] und [!DNL Adobe Journey Optimizer] zu verwenden, benötigen Sie Folgendes:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) mit der [Adobe Experience Platform Web SDK implementiert](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep/aep-web-sdk-overview){target=_blank}.

  Diese Funktion ist nicht verfügbar mit einer [!DNL Target Standard] Lizenz oder bei der Implementierung von [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home){target=_blank}.

## Beispiele für Anwendungsfälle

Diese Anwendungsfälle sind nur einige mögliche Anwendungsfälle für die Integration von [!DNL Target Recommendations] mit [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]sendet nach Warenkorbabbruch eine personalisierte E-Mail**: Dieser Anwendungsfall basiert darauf, dass ein Kunde eine Website besucht, Artikel in den Warenkorb legt und dann die Website verlässt, ohne den Kaufvorgang abzuschließen.

  Angenommen, ein Besucher besucht beispielsweise die Website eines Bekleidungsunternehmens und legt zwei Wintermäntel und ein Sweatshirt in den Warenkorb. Der Besucher wird dann abgelenkt und verlässt die Website oder ist sich über die Käufe nicht sicher und schließt den Browser oder die App.

  Nach einem bestimmten Zeitraum, vielleicht einige Stunden oder einen Tag, führt eine benutzerdefinierte Aktion in [!DNL Journey Optimizer] einen Aufruf an [!DNL Target Recommendations] durch, um den Inhalt des Transaktionsabbruchs mithilfe eines [Warenkorb-basierten Recommendations](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)-Algorithmus zu ermitteln. [!DNL Journey Optimizer] sendet diesem Besucher dann eine personalisierte E-Mail, um ihn daran zu erinnern, dass der Kaufvorgang nicht abgeschlossen wurde, sowie Bilder und Links zu den abgebrochenen Artikeln.

* **[!DNL Adobe Journey Optimizer]sendet nach Site-Besuchen eine Massen-E-Mail, um Besucher daran zu erinnern, welche Artikel angezeigt wurden**: Dieser Anwendungsfall basiert darauf, dass Besucher eine Website besuchen, verschiedene Artikel anzeigen und dann die Website oder App verlassen, ohne Artikel in den Warenkorb zu legen.

  Nach einem bestimmten Zeitraum ruft eine benutzerdefinierte Aktion in [!DNL Journey Optimizer] [!DNL Target Recommendations] auf, um mithilfe der [!DNL Adobe Experience Cloud Identifier] (EDID) jedes Besuchers, seines [!DNL Target] Profils und eines [benutzerbasierten](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) Algorithmus zu bestimmen, welche Elemente jeder angezeigt hat. [!DNL Adobe Journey Optimizer] sendet dann jedem Mitglied der qualifizierten Zielgruppe eine personalisierte E-Mail mit Bildern und Links zu den angezeigten Elementen jedes Besuchers, um den Besucher zu veranlassen, zurückzukehren und einen Kauf zu tätigen.

  In diesem Szenario werden die [!UICONTROL Experience Cloud-Besucher-ID] (ECID) und der Inhalt des [!DNL Target] jedes Besuchers verwendet, um die Empfehlung basierend auf dem kürzlich angezeigten Algorithmus zu generieren.

  Angenommen, ein Besucher besucht beispielsweise eine Einzelhandels-Website und sieht sich mehrere Uhren an. Das [!DNL Target] dieses Besuchers wird mit einer Liste der angezeigten Überwachungen aktualisiert. Unter Verwendung der ECID und des [!DNL Target] des Besuchers sendet [!DNL Target] die Empfehlung an [!DNL Journey Optimizer]. [!DNL Journey Optimizer] sendet dann eine E-Mail mit Bildern und Links zu den Uhren, die dieser Besucher angesehen hat, unter Verwendung des Algorithmus für die zuletzt angezeigte Anzeige. Ein anderer Besucher erhält eine personalisierte E-Mail mit Bildern und Links zu den Elementen, die er angezeigt hat. Jede E-Mail-Nachricht wird für jeden Besucher personalisiert.

* **[!DNL Adobe Journey Optimizer]sendet nach dem Site-Besuch eine Massen-E-Mail an qualifizierte Besucher, um beliebte Elemente vorzuschlagen**: Dieser Anwendungsfall basiert darauf, dass ein Besucher eine Website besucht, aber keine bestimmten Elemente angezeigt. Die E-Mail wird stapelweise an alle Besucher gesendet, die sich für eine bestimmte Zielgruppe qualifizieren, z. B.:

  Angenommen, der Besucher sieht keine bestimmten Uhren. Vielleicht hat der Besucher einfach auf die Website geklickt und Kategorieseiten oder Blogeinträge angesehen. Daher verfügt das [!DNL Target]-Profil nicht über spezifische Informationen zu den kürzlich angezeigten Elementen. In diesem Fall verwendet [!DNL Target Recommendations] eine [Sicherungsempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md), damit [!DNL Journey Optimizer] eine E-Mail mit Bildern und Links zu beliebten Elementen auf der Website senden können, um den Besucher zur Rückkehr zu bewegen und möglicherweise einen Kauf zu tätigen.
