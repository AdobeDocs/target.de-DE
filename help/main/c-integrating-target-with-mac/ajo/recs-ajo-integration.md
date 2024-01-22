---
keywords: ajo; Adobe Journey Optimizer; Adobe Journey Optimizer-Target-Integration; Empfehlungen; Target-Empfehlungen; Integration
description: Integrieren [!DNL Adobe Target Recommendations] mit [!DNL Adobe Journey Optimizer].
title: Verwendung [!DNL Target Recommendations] bei Journey, die [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
source-git-commit: 1faedc44c4f8f95000b666af8eecaf1eca5bf48d
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 3%

---

# Integrieren [!DNL Adobe Target Recommendations] und [!DNL Adobe Journey Optimizer]

In diesem Artikel werden Anwendungsfälle und Informationen erläutert, die Sie bei der Einrichtung der Integration zwischen [!DNL Adobe Target Recommendation] und [!DNL Adobe Journey Optimizer] um Ihnen zu helfen, Ihren Kunden verknüpfte, kontextbezogene und personalisierte Erlebnisse bereitzustellen.

## Voraussetzungen 

So verwenden Sie die [!DNL Target Recommendations] und [!DNL Adobe Journey Optimizer] -Integration benötigen Sie Folgendes:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implementiert mithilfe der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

  Die Funktion ist nicht verfügbar bei einer [!DNL Target Standard] Lizenz oder bei der Implementierung [!DNL Target] mit at.js oder anderen [!DNL Target] SDKs

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Anwendungsbeispiele

Im Folgenden finden Sie nur zwei mögliche Anwendungsfälle für die Integration von [!DNL Target Recommendations] mit [!DNL Adobe Journey Optimizer]:

* **[!DNL Customer Journey Optimizer]sendet eine personalisierte E-Mail nach einem Warenkorbabbruch**: Dieser Anwendungsfall basiert auf einem Kunden, der eine Website besucht, Artikel in den Warenkorb legt und dann die Site verlässt, ohne den Kaufprozess abzuschließen.

  Angenommen, ein Besucher besucht die Website eines Bekleidungsunternehmens und legt zwei Wintermäntel und ein Pullover in den Warenkorb. Der Besucher wird dann abgelenkt und verlässt die Website oder ist sich der Käufe nicht sicher und schließt den Browser oder die App.

  Nach einem bestimmten Zeitraum, vielleicht ein paar Stunden oder einen Tag, eine benutzerdefinierte Aktion in [!DNL Adobe Journey Optimizer] führt einen Aufruf an [!DNL Target Recommendations] um den Inhalt des Warenkorbs zu ermitteln. [!DNL Adobe Journey Optimizer] sendet diesem Besucher eine personalisierte E-Mail, um ihn daran zu erinnern, dass der Kaufvorgang nicht abgeschlossen wurde, sowie Bilder und Links zu den abgebrochenen Artikeln.

* **[!DNL Customer Journey Optimizer]sendet eine E-Mail nach dem Site-Besuch mit dem Benutzerprofil**: Dieser Anwendungsfall basiert auf einem Kunden, der eine Website besucht, verschiedene Artikel anzeigt und dann die Site verlässt, ohne Artikel in den Warenkorb zu legen.

  Nach einem bestimmten Zeitraum wird eine benutzerdefinierte Aktion in [!DNL Adobe Journey Optimizer] führt einen Aufruf an [!DNL Target Recommendations] , um zu bestimmen, welche Elemente dieser Besucher mit dem Besucher angezeigt hat. [!DNL Adobe Experience Cloud Identifier] (BEARBEITUNG). [!DNL Adobe Journey Optimizer] sendet diesem Besucher eine personalisierte E-Mail, um ihn daran zu erinnern, dass der Kaufvorgang nicht abgeschlossen wurde, sowie Bilder und Links zu den abgebrochenen Artikeln.

