---
description: Häufig gestellte Fragen zu Adobe Target für mobile Apps
keywords: mobile app;frequently asked questions;faq;target mobile app
seo-description: Häufig gestellte Fragen zu Adobe Target für mobile Apps
seo-title: Häufig gestellte Fragen zu Adobe Target für mobile Apps
title: Häufig gestellte Fragen zu Adobe Target für mobile Apps
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 43a00c7ade1f2e10a023ffdcb2e75cf2483e6907

---


# Häufig gestellte Fragen zu Target für mobile Apps

Liste der häufig gestellten Fragen [!DNL Target] zu mobilen Apps

## Soll ich das SDK [!DNL Adobe Experience Platform Launch] bereitstellen oder kann ich das SDK ohne Verwendung bereitstellen? [!DNL Launch]

Das SDK ist im [Adobe Marketing Cloud-Git](https://github.com/Adobe-Marketing-Cloud/acp-sdks/)verfügbar. Wenn Sie [Launch](https://docs.adobe.com/content/help/en/launch/using/overview.html)nicht verwenden, müssen Sie Ihre eigene Einstellungsdatei verwalten und in Ihrer App verwalten.

## Kann der Visual Experience Composer (VEC) für mobile Apps mit React-Native-Unterstützung für das Adobe Experience Platform SDK v5 verwendet werden?

Der [VEC für native mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) unterstützt derzeit keine native React-App. Sie müssen den [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md)verwenden.

## Ermöglicht die Mobile SDK-Integration die Einführung neuer Funktionen für Mobilgeräte? Kann ich das Feature-Flag ohne neue Codebereitstellungen aktivieren und deaktivieren?

Ja, Sie können unser mobiles SDK verwenden, um Funktionen schrittweise einzuführen.

## Sollte ich für komplexere Logik direkt in der App entwickeln, anstatt Mobile VEC zu verwenden? Wenn ja, welche Entwicklungssprache sollte ich verwenden?

Derzeit unterstützt der VEC gängige Einsatzfälle wie das Ändern von Bild, Text, Farbe usw. Für komplexere Anwendungsfälle wie das Personalisieren des App-Layouts müssen Sie die [!DNL Target] Anforderung/Position (Mbox) in den Code einfügen und den [formularbasierten Experience Composer](/help/c-experiences/form-experience-composer.md) verwenden, um Erlebnisse zu entwerfen und Traffic zuzuordnen. Unser mobiles SDK unterstützt Java, Objective C und Swift. Die Auswahl der Sprache hängt von den Vorlieben und Ressourcen Ihres Teams ab.

## Which SDKs are available today?

Die Adobe Experience Platform Mobile-SDKs unterstützen derzeit iOS, Android und React. Weitere Informationen finden Sie im Handbuch[zu ](https://aep-sdks.gitbook.io/docs/)Adobe Experience Cloud Platform Mobile SDKs.

## Wie häufig erfolgt die Überprüfung der Breiten- und Längengrad durch die standortbasierte Funktion?

See the Adobe Places documentation for more information.[](https://placesdocs.com/places-services-by-adobe-documentation/)

## Welche nativen Klassen werden von mobilen "Ansichten"unterstützt? Unterstützen sie eine abgeleitete NSObject-Klasse (oder ein Android-Objekt) oder nur NSViewController und Aktivitäten?

Weitere Informationen zur [manuellen Darstellung von Ansichten](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views)finden Sie in der Android-Dokumentation.

## Benötige ich at.js, damit die Mobile-SDKs der Adobe Experience Platform funktionieren?

Nein, Sie benötigen at.js nicht, um die mobilen SDKs zu verwenden. at.js ist die [!DNL Target] JavaScript-Bibliothek für Websites. Die Adobe Experience Platform Mobile-SDKs sind für mobile Apps vorgesehen.

## Is Target Mobile a functionality of Adobe Target Premium Product SKU only?

For Adobe Target Standard customers, you can use our Mobile SDKs for A/B Test and Experience Targeting (XT) activities only. If you want to use Recommendations or AI-powered features in the mobile app, you need an Adobe Target Premium license.[](/help/c-intro/intro.md#premium)

## Can I leverage audiences from Adobe Audience Manager (AAM) in the VEC for Mobile Apps?

Yes, Adobe Experience Platform Mobile SDKs are built for Audience Manager, Analytics, Campaign, and Target. [](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html)[](https://docs.adobe.com/content/help/en/analytics/landing/home.html)[](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html) Your audiences in Audience Manager are shared with .[!DNL Target]

## Is there a mobile app integration between Adobe Experience Manager (AEM) and Target mobile activities?

It is on our roadmap but there is no timeline yet. Currently, you can share JSON Experience Fragments from AEM to Target and there might be potential to then use them in a mobile app activity.[](/help/c-experiences/c-manage-content/aem-experience-fragments.md)

## Can I add more images using the VEC or only change existing images?

You can currently change existing images only.
