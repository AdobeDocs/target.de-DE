---
keywords: Mobile App;Häufig gestellte Fragen;FAQ;Mobilanwendung als Ziel auswählen
description: Häufig gestellte Fragen zu Adobe Target für mobile Apps
title: Häufig gestellte Fragen zu Adobe Target für mobile Apps
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

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

## Welche SDKs sind heute verfügbar?

Die Adobe Experience Platform Mobile-SDKs unterstützen derzeit iOS, Android und React. Weitere Informationen finden Sie im Handbuch[zu ](https://aep-sdks.gitbook.io/docs/)Adobe Experience Cloud Platform Mobile SDKs.

## Wie häufig erfolgt die Überprüfung der Breiten- und Längengrad durch die standortbasierte Funktion?

Weitere Informationen finden Sie in der Dokumentation[ zu ](https://placesdocs.com/places-services-by-adobe-documentation/)Adobe Places.

## Welche nativen Klassen werden von mobilen "Ansichten"unterstützt? Unterstützen sie eine abgeleitete NSObject-Klasse (oder ein Android-Objekt) oder nur NSViewController und Aktivitäten?

Weitere Informationen zur [manuellen Darstellung von Ansichten](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views)finden Sie in der Android-Dokumentation.

## Benötige ich at.js, damit die Mobile-SDKs der Adobe Experience Platform funktionieren?

Nein, Sie benötigen at.js nicht, um die mobilen SDKs zu verwenden. at.js ist die [!DNL Target] JavaScript-Bibliothek für Websites. Die Adobe Experience Platform Mobile-SDKs sind für mobile Apps vorgesehen.

## Ist Target Mobile nur eine Funktion der Adobe Target Premium-Produkt-SKU?

Für Kunden von Adobe Target Standard können Sie unsere Mobile SDKs nur für A/B-Test- und Erlebnis-Targeting (XT)-Aktivitäten verwenden. Wenn Sie Recommendations oder AI-basierte Funktionen in der mobilen App verwenden möchten, benötigen Sie eine [Adobe Target Premium](/help/c-intro/intro.md#premium) -Lizenz.

## Kann ich Zielgruppen aus Adobe Audience Manager (AAM) im VEC für mobile Apps nutzen?

Ja. Adobe Experience Platform Mobile-SDKs sind für [Audience Manager](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html), [Analytics](https://docs.adobe.com/content/help/en/analytics/landing/home.html), [Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html)und Target erstellt. Ihre Zielgruppen in Audience Manager werden freigegeben [!DNL Target].

## Gibt es eine mobile App-Integration zwischen Adobe Experience Manager (AEM) und Target Mobile-Aktivitäten?

Es ist auf unserem Fahrplan, aber es gibt noch keinen Zeitplan. Derzeit können Sie JSON- [Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md) aus AEM in Target freigeben, und es besteht möglicherweise die Möglichkeit, diese dann in einer mobilen App-Aktivität zu verwenden.

## Kann ich mit dem VEC weitere Bilder hinzufügen oder nur vorhandene Bilder ändern?

Derzeit können nur vorhandene Bilder geändert werden.
