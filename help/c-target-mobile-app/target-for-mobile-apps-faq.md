---
keywords: mobile App; häufig gestellte Fragen; FAQ; Targeting mobiler Apps
description: Sehen Sie sich häufig gestellte Fragen und ihre Antworten zur Adobe [!DNL Target] für mobile Apps an.
title: Welche häufig gestellten Fragen zu [!DNL Target] Mobile Apps gibt es?
feature: Mobile implementieren
role: Developer
exl-id: 1ddd8345-e753-4608-9293-939e092cb16d
source-git-commit: eddde1bae345e2e28ca866662ba9664722dedecd
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# Target für mobile Apps – FAQs

Liste der häufig gestellten Fragen zu [!DNL Target] für mobile Apps.

## Sollte ich Tags in [!DNL Adobe Experience Platform] verwenden, um das SDK bereitzustellen, oder kann ich das SDK ohne Verwendung von [!DNL Launch] bereitstellen?

Das SDK ist im Adobe Marketing Cloud-Git](https://github.com/Adobe-Marketing-Cloud/acp-sdks/) verfügbar. [ Wenn Sie [Tags nicht in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) verwenden, müssen Sie Ihre eigene Einstellungsdatei verwalten und in Ihrer App verwalten.

## Welche SDKs sind heute verfügbar?

Die Adobe Experience Platform Mobile SDKs unterstützen derzeit iOS, Android und React. Weitere Informationen finden Sie im Handbuch [Adobe Experience Cloud Platform Mobile SDKs](https://aep-sdks.gitbook.io/docs/).

## Wie oft ist die standortbasierte Funktion hinsichtlich der Verifizierung des Längen- und Breitengrads?

Weitere Informationen finden Sie in der [Adobe Places-Dokumentation](https://placesdocs.com/places-services-by-adobe-documentation/) .

## Benötige ich at.js, damit die Adobe Experience Platform Mobile SDKs funktionieren?

Nein, Sie benötigen at.js nicht, um die mobilen SDKs zu verwenden. at.js ist die JavaScript-Bibliothek [!DNL Target] für Websites. Die Adobe Experience Platform Mobile SDKs sind für mobile Apps vorgesehen.

## Ist [!DNL Target] Mobile eine Funktion der Adobe [!DNL Target] Premium Product SKU?

Nein. Für [!DNL Adobe Target Standard]-Kunden können Sie unsere Mobile SDKs nur mit dem Add-on für mobile Apps für A/B-Tests und Erlebnis-Targeting (XT) verwenden. [!DNL Target Standard] Wenn Sie Recommendations- oder AI-gestützte Funktionen in der Mobile App verwenden möchten, benötigen Sie eine [Adobe Target Premium](/help/c-intro/intro.md#premium) -Lizenz.

## Gibt es eine Mobile-App-Integration zwischen Adobe Experience Manager (AEM) und [!DNL Target] Mobile-Aktivitäten?

Es liegt auf unserem Fahrplan, aber es gibt noch keinen Zeitplan. Derzeit können Sie JSON [Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md) von AEM in Target freigeben und es kann sein, dass Sie sie dann in einer Mobile-App-Aktivität verwenden.
