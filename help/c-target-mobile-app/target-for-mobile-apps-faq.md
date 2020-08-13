---
keywords: mobile app;frequently asked questions;faq;target mobile app
description: Häufig gestellte Fragen zu Adobe Target für mobile Apps.
title: Häufig gestellte Fragen zu Adobe Target für mobile Apps
feature: mobile implementation
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Häufig gestellte Fragen zur Zielgruppe von Apps

Liste häufig gestellter Fragen zu [!DNL Target] mobilen Apps.

## Soll ich das SDK [!DNL Adobe Experience Platform Launch] bereitstellen oder kann ich das SDK ohne Verwendung bereitstellen? [!DNL Launch]

Das SDK ist auf der [Adobe Marketing Cloud-Git](https://github.com/Adobe-Marketing-Cloud/acp-sdks/)verfügbar. Wenn Sie [Launch](https://docs.adobe.com/content/help/en/launch/using/overview.html)nicht verwenden, müssen Sie Ihre eigene Einstellungsdatei verwalten und in Ihrer App verwalten.

## Welche SDKs stehen heute zur Verfügung?

Die Adobe Experience Platform Mobile SDKs unterstützen derzeit iOS, Android und React. For more information, see the [Adobe Experience Cloud Platform Mobile SDKs guide](https://aep-sdks.gitbook.io/docs/).

## What is the frequency of the location-based feature, in terms of verification about the latitude and longitude?

Weitere Informationen finden Sie in der Dokumentation [zu](https://placesdocs.com/places-services-by-adobe-documentation/) Adoben-Orten.

## Benötige ich at.js, damit die Adobe Experience Platform Mobile SDKs funktionieren?

Nein, Sie benötigen at.js nicht, um die mobilen SDKs zu verwenden. at.js ist die [!DNL Target] JavaScript-Bibliothek für Websites. Die Adobe Experience Platform Mobile SDKs sind für mobile Apps vorgesehen.

## Is Target Mobile a functionality of Adobe Target Premium Product SKU only?

Nein. Für [!DNL Adobe Target Standard] Kunden können Sie unsere Mobile SDKs nur mit dem [!DNL Target Standard] Mobile App Add-on für A/B-Test- und Erlebnis-Targeting (XT)-Aktivitäten verwenden. If you want to use Recommendations or AI-powered features in the mobile app, you need an [Adobe Target Premium](/help/c-intro/intro.md#premium) license.

## Is there a mobile app integration between Adobe Experience Manager (AEM) and Target mobile activities?

It is on our roadmap but there is no timeline yet. Currently, you can share JSON [Experience Fragments](/help/c-experiences/c-manage-content/aem-experience-fragments.md) from AEM to Target and there might be potential to then use them in a mobile app activity.
