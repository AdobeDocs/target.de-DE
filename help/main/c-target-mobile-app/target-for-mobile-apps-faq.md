---
keywords: mobile App; häufig gestellte Fragen; FAQ; Targeting mobiler Apps
description: Anzeigen von häufig gestellten Fragen und deren Antworten auf die Adobe [!DNL Target] für mobile Apps.
title: Häufig gestellte Fragen zu [!DNL Target] für mobile Apps?
feature: Implement Mobile
role: Developer
exl-id: 1ddd8345-e753-4608-9293-939e092cb16d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---

# Target für mobile Apps – FAQs

Liste der häufig gestellten Fragen zu [!DNL Target] für mobile Apps.

## Sollte ich Tags in [!DNL Adobe Experience Platform] zum Bereitstellen des SDK oder kann ich das SDK ohne Verwendung von bereitstellen [!DNL Launch]?

Das SDK ist im [Adobe Marketing Cloud Git](https://github.com/Adobe-Marketing-Cloud/acp-sdks/). Wenn Sie [Tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de)müssen Sie Ihre eigene Einstellungsdatei verwalten und in Ihrer App verwalten.

## Welche SDKs sind heute verfügbar?

Die Adobe Experience Platform Mobile SDKs unterstützen derzeit iOS, Android und React. Weitere Informationen finden Sie unter [Handbuch zu Adobe Experience Cloud Platform Mobile SDKs](https://aep-sdks.gitbook.io/docs/).

## Wie oft ist die standortbasierte Funktion hinsichtlich der Verifizierung des Längen- und Breitengrads?

Siehe [Dokumentation zu Adobe Places](https://placesdocs.com/places-services-by-adobe-documentation/) für weitere Informationen.

## Benötige ich at.js, damit die Adobe Experience Platform Mobile SDKs funktionieren?

Nein, Sie benötigen at.js nicht, um die mobilen SDKs zu verwenden. &quot;at.js&quot;ist die [!DNL Target] JavaScript-Bibliothek für Websites. Die Adobe Experience Platform Mobile SDKs sind für mobile Apps vorgesehen.

## Is [!DNL Target] Eine Funktion der Adobe für Mobilgeräte [!DNL Target] Nur Premium-Produkt-SKU?

Nein. Für [!DNL Adobe Target Standard] Kunden verwenden, können Sie unsere Mobile SDKs nur für A/B-Test- und Erlebnis-Targeting-Aktivitäten (XT) mit der Variablen [!DNL Target Standard] Mobile App-Add-on. Wenn Sie Recommendations- oder AI-gestützte Funktionen in der App verwenden möchten, benötigen Sie eine [Adobe Target Premium](/help/main/c-intro/intro.md#premium) Lizenz.

## Gibt es eine Mobile-App-Integration zwischen Adobe Experience Manager (AEM) und [!DNL Target] mobile Aktivitäten?

Es liegt auf unserem Fahrplan, aber es gibt noch keinen Zeitplan. Derzeit können Sie JSON freigeben [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) von AEM zu Target und es kann sein, dass sie dann in einer App-Aktivität verwendet werden.
