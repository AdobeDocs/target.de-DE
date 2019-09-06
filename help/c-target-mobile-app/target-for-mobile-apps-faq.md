---
description: Häufig gestellte Fragen zu Adobe Target für mobile Apps.
keywords: mobile App; häufig gestellte Fragen; faq; Targeting mobiler Apps
seo-description: Häufig gestellte Fragen zu Adobe Target für mobile Apps.
seo-title: Häufig gestellte Fragen zu Adobe Target für mobile Apps
title: Häufig gestellte Fragen zu Adobe Target für mobile Apps
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 43a00c7ade1f2e10a023ffdcb2e75cf2483e6907

---


# Häufig gestellte Fragen zu Target für mobile Apps

Liste der häufig gestellten Fragen zu [!DNL Target] mobilen Apps.

## Sollte ich das [!DNL Adobe Experience Platform Launch] SDK bereitstellen oder kann ich das SDK ohne Verwendung des [!DNL Launch]SDK bereitstellen?

Das SDK ist im [Adobe Marketing Cloud-Git verfügbar](https://github.com/Adobe-Marketing-Cloud/acp-sdks/). Wenn [Sie nicht starten](https://docs.adobe.com/content/help/en/launch/using/overview.html), müssen Sie Ihre eigene Einstellungsdatei verwalten und sie in Ihrer App verwalten.

## Kann Visual Experience Composer (VEC) für mobile Apps mit React-Native Unterstützung für das Adobe Experience Platform SDK v 5 verwendet werden?

Die [VEC für native mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) unterstützt derzeit nicht die React Native App. Sie müssen den [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md)verwenden.

## Lässt die mobile SDK-Integration neue Funktionen für Mobilgeräte zu? Kann ich das Funktionsflag ohne neue Implementierungen aktivieren oder deaktivieren?

Ja, Sie können unser mobiles SDK verwenden, um Funktionen schrittweise zu entwickeln.

## Sollte ich für eine komplexere Logik direkt in der App entwickeln, anstatt Mobile VEC zu verwenden? Welche Entwicklungssprache sollte ich verwenden?

Derzeit unterstützt VEC gängige Anwendungsfälle wie das Ändern von Bildern, Text, Farbe usw. Für fortgeschrittenere Anwendungsfälle wie das Personalisieren des App-Layouts müssen Sie die [!DNL Target] Anforderung/Position (mbox) in den Code einfügen und den [formularbasierten Experience Composer](/help/c-experiences/form-experience-composer.md) verwenden, um Erlebnisse zu entwerfen und Traffic zuzuordnen. Unser mobiles SDK unterstützt Java, Target C und Swift. Es hängt von der Voreinstellung und den Ressourcen Ihres Teams ab, die Sprache auszuwählen.

## Welche sdks sind heute verfügbar?

Die Adobe Experience Platform Mobile sdks unterstützen derzeit ios, Android und React. Weitere Informationen finden Sie im [Handbuch Adobe Experience Cloud Platform Mobile sdks](https://aep-sdks.gitbook.io/docs/).

## Was ist die Häufigkeit der standortbasierten Funktion, in Bezug auf die Prüfung des Breiten- und Längengrad?

Weitere Informationen finden Sie in der [Dokumentation](https://placesdocs.com/places-services-by-adobe-documentation/) zu Adobe Places.

## Welche nativen Klassen unterstützen Mobilgeräte- "Ansichten" ? Unterstützen sie eine beliebige nsobject-Klasse (oder ein beliebiges Android-Objekt) oder nur nsviewcontroller und Aktivitäten?

Weitere Informationen finden Sie in der Android-Dokumentation zum [manuellen Deklarieren von Ansichten](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views).

## Benötige ich at. js für die mobilen sdks von Adobe Experience Platform?

Nein, Sie benötigen at. js nicht für die Verwendung der mobilen sdks. " at. js" ist die [!DNL Target] javascript-Bibliothek für Websites. Die Adobe Experience Platform Mobile sdks sind für mobile Apps gedacht.

## Funktioniert Target Mobile nur mit Adobe Target Premium Product SKU?

Für Adobe Target Standard-Kunden können Sie unsere Mobile sdks nur für A/B-Test- und Erlebnis-Targeting (XT)-Aktivitäten verwenden. Wenn Sie Recommendations oder AI-basierte Funktionen in der mobilen App verwenden möchten, benötigen Sie eine [Adobe Target Premium](/help/c-intro/intro.md#premium) -Lizenz.

## Kann ich Zielgruppen aus Adobe Audience Manager (AAM) in VEC für Mobile Apps nutzen?

Ja, Adobe Experience Platform Mobile sdks sind für [Audience Manager](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html), [Analytics](https://docs.adobe.com/content/help/en/analytics/landing/home.html), [Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html)und Target aufgebaut. Ihre Zielgruppen in Audience Manager werden freigegeben.[!DNL Target]

## Gibt es eine mobile App-Integration zwischen Adobe Experience Manager (AEM) und Target Mobile-Aktivitäten?

Es ist unser Plan, aber noch keine Zeitleiste. Derzeit können Sie JSON [-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md) von AEM auf Target freigeben und es kann dann möglich sein, sie in einer mobilen App-Aktivität zu verwenden.

## Kann ich mit dem VEC weitere Bilder hinzufügen oder nur vorhandene Bilder ändern?

Derzeit können Sie vorhandene Bilder nur ändern.
