---
keywords: responsive;mobile viewports;viewport;devices;mobile;responsive web design;rwd
description: Mit mobilen Viewports können Sie Vorschauen dazu erstellen, wie Ihre Adobe Target-Aktivitäten auf Bildschirmen unterschiedlicher Größe angezeigt werden.
title: Mobile Viewports für responsive Erlebnisse
feature: null
uuid: 86a74584-4a4d-428b-9d29-f7ebdf0cef2a
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 70%

---


# Mobile Viewports for responsive experiences{#mobile-viewports-for-responsive-experiences}

Mobile viewports help you preview how your [!DNL Target] activities appear on screens of various sizes.

Die Funktion zur mobilen Viewport-Vorschau wurde für responsive Sites entwickelt, die auf verschiedenen Geräten, Fenstern oder Bildschirmgrößen gut dargestellt werden. Responsive Sites passen sich automatisch an jede Bildschirmgröße an, einschließlich Desktop-PCs, Laptops, Tablets oder Mobiltelefone.

>[!NOTE]
>
> * Verwenden Sie mobile Viewports, wenn Ihre Site responsiv ist und dieselben Elemente auf Ihrer Desktop-Seite in einer anderen Konfiguration auf Ihrer mobilen Seite verwendet werden. If you have a separate mobile site with a separate structure, such as `m.mysite.com`, use a [multipage activity](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) instead.
   >
   >
* Mobile Viewports sind nicht verfügbar, wenn sie von einem Umleitungsangebot überlagert werden.


Ein Viewport wird durch die Größe des Rechtecks definiert, das von einer Webseite auf Ihrem Bildschirm ausgefüllt wird. Es ist die Größe des Browser-Fensters abzüglich der Bildlaufleisten und Symbolleisten. Browser verwenden „CSS-Pixel“. Für viele Geräte, zum Beispiel solche mit Retina-Bildschirm, ist der Viewport kleiner als die beworbene Geräteauflösung.

Nachstehend finden Sie die Viewports und Auflösungen für einige bekannte Geräte. Remember to use the viewport size in [!DNL Target]. Auf verschiedenen Websites sind die Viewport-Größen für gängige Geräte aufgeführt. Weitere Informationen finden Sie unter [https://viewportsizer.com/devices/](https://viewportsizer.com/devices/) oder auf der Website des Geräteherstellers.

| Gerät | Viewport-Größe | Geräteauflösung |
|---|---|---|
| iPhone SE | 375 (B) x 667 (H) | 750 (B) x 1334 (H) |
| iPhone 11 Pro Max | 414 (B) x 896 (H) | 1242 (B) x 2688 (H) |
| iPhone 11 Xs Max. | 414 (B) x 896 (H) | 1242 (B) x 2688 (H) |
| iPhone 11 | 414 (B) x 896 (H) | 828 (B) x 1792 (H) |
| iPhone 11 Xr | 414 (B) x 896 (H) | 828 (B) x 1792 (H) |
| iPhone 11 Pro | 375 (B) x 812 (H) | 1125 (B) x 2436 (H) |
| iPhone 11 X | 375 (B) x 812 (H) | 1125 (B) x 2436 (H) |
| iPhone 11 Xs | 375 (B) x 812 (H) | 1125 (B) x 2436 (H) |
| iPhone X | 375 (B) x 812 (H) | 1125 (B) x 2436 (H) |
| iPhone 8 Plus | 414 (B) x 736 (H) | 1080 (B) x 1920 (H) |
| iPhone 8 | 375 (B) x 667 (H) | 750 (B) x 1334 (H) |
| iPhone 7 Plus | 414 (B) x 736 (H) | 1080 (B) x 1920 (H) |
| iPhone 7 | 375 (B) x 667 (H) | 750 (B) x 1334 (H) |
| iPhone 6s Plus | 414 (B) x 736 (H) | 1080 (B) x 1920 (H) |
| iPhone 6s | 375 (B) x 667 (H) | 750 (B) x 1334 (H) |
| iPhone 6 Plus | 414 (B) x 736 (H) | 1080 (B) x 1920 (H) |
| iPhone 6 | 375 (B) x 667 (H) | 750 (B) x 1334 (H) |
| iPad  Pro | 1024 (B) x 1366 (H) | 2048 (B) x 2732 (H) |
| iPad der 3. und 4. Generation | 768 (B) x 1024 (H) | 1536 (B) x 2048 (H) |
| iPad Air 1 und 2 | 768 (B) x 1024 (H) | 1536 (B) x 2048 (H) |
| iPad Mini | 768 (B) x 1024 (H) | 768 (B) x 1024 (H) |
| iPad Mini 2 und 3 | 768 (B) x 1024 (H) | 1536 (B) x 2048 (H) |
| Nexus 6P | 411 (B) x 731 (H) | 1440 (B) x 2560 (H) |
| Nexus 5X | 411 (B) x 731 (H) | 1080 (B) x 1920 (H) |
| Google Pixel | 411 (B) x 731 (H) | 1080 (B) x 1920 (H) |
| Google Pixel XL | 411 (B) x 731 (H) | 1440 (B) x 2560 (H) |
| Google Pixel 2 | 411 (B) x 731 (H) | 1080 (B) x 1920 (H) |
| Google Pixel 2 XL | 411 (B) x 823 (H) | 1440 (B) x 2880 (H) |
| Samsung Galaxy Note 5 | 480 (B) x 853 (H) | 1440 (B) x 2560 (H) |
| LG G5 | 480 (B) x 853 (H) | 1440 (B) x 2560 (H) |
| One Plus 3 | 480 (B) x 853 (H) | 1080 (B) x 1920 (H) |
| Samsung Galaxy S9 | 360 (B) x 740 (H) | 1440 (B) x 2960 (H) |
| Samsung Galaxy S9+ | 360 (B) x 740 (H) | 1440 (B) x 2960 (H) |
| Samsung Galaxy S8 | 360 (B) x 740 (H) | 1440 (B) x 2960 (H) |
| Samsung Galaxy S8+ | 360 (B) x 740 (H) | 1440 (B) x 2960 (H) |
| Samsung Galaxy S7 | 360 (B) x 640 (H) | 1440 (B) x 2560 (H) |
| Samsung Galaxy S7 Edge | 360 (B) x 640 (H) | 1440 (B) x 2560 (H) |
| Nexus 7 (2013) | 600 (B) x 960 (H) | 1200 (B) x 1920 (H) |
| Nexus 9 | 768 (B) x 1024 (H) | 1536 (B) x 2048 (H) |
| Samsung Galaxy Tab 10 | 800 (B) x 1280 (H) | 800 (B) x 1280 (H) |
| Chromebook Pixel | 1280 (B) x 850 (H) | 2560 (B) x 1700 (H) |

Wenn Sie eine Aktivität für Benutzer auf einem bestimmten Gerät bereitstellen möchten, wählen Sie im Aktivitätsdiagramm die entsprechende Zielgruppe für das Gerät aus. Verwenden Sie den Mobile Web Composer, um die Seite für das Gerät in der Aktivität zu bearbeiten. Wenn Sie eine Aktivität in all Ihren digitalen Erlebnissen ausführen und sicherstellen möchten, dass es auf allen Geräten ansprechend aussieht, wenden Sie nicht das Targeting an, sondern verwenden Sie mobile Viewports, um auf jeder Bildschirmgröße eine Vorschau für die Aktivität anzuzeigen.

Wenn Sie über eine responsive Site verfügen, wird Ihre Site in der Regel so erstellt, dass beim Zugriff durch ein Gerät mit einer bestimmten Bildschirmgröße eine andere Ansicht geöffnet wird. Diese Bildschirmgrößen, die solche neuen Ansichten auslösen, werden auch als CSS-Haltepunkte bezeichnet. CSS-Haltepunkte sind Punkte, an denen Website-Inhalte je nach Gerätebreite antworten, um das optimale Layout für Besucher anzuzeigen. CSS-Haltepunkte werden auch als [Media-Abfragen](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)bezeichnet.

Save your CSS breakpoints in [!DNL Target] so you can preview your experiences for each view you define. Each of these experiences is displayed in a mobile viewport in the [!DNL Target] interface. Öffnen Sie die Ansicht für jeden Bildschirm, indem Sie entlang der Oberkante der Anzeige auf diesen Viewport klicken.

Wenn Ihre Site nicht responsiv ist, können Sie zum Anzeigen einer Site weiterhin den Mobile Web Composer verwenden, wenn Ihre Aktivität auf ein bestimmtes Gerät ausgerichtet ist.

>[!IMPORTANT]
>
>Although you can edit an experience from within mobile viewports, these changes apply to all viewports and devices, not just the viewport that you&#39;re working in. Gleichermaßen wird bei der Bearbeitung eines Erlebnisses in der normalen Desktop-Ansicht die Seite für alle Bildschirmgrößen und nicht nur für die Desktop-Ansicht geändert. Derzeit bieten wir keine Unterstützung für Viewport-spezifische Seitenänderungen.

## Mobile viewport configuration {#task_B4B161499DC0470584ED922A4D20FCAB}

Konfigurieren Sie alle mobilen Viewports, die Sie beim Erstellen Ihrer Erlebnisse verfügbar machen möchten.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. Um einen neuen mobilen Viewport hinzuzufügen, klicken Sie im Abschnitt **[!UICONTROL Mobile Viewports-Konfiguration]** auf **[!UICONTROL Hinzufügen]**.

   ![hinzufügen Viewport](/help/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   To change the configuration of an existing mobile viewport, select that viewport, then click the [!UICONTROL Edit] (pencil) icon.

1. Geben Sie einen Namen für den mobilen Viewport ein.

   Geben Sie Ihrem mobilen Viewport einen beschreibenden Namen, der leicht wiederzuerkennen ist. Der Name kann aus bis zu 36 Zeichen bestehen.

1. Geben Sie die Bildschirmgröße des Mobilgeräts mit Breite und Höhe ein.

   Die Breite kann zwischen 150 und 968 Pixeln betragen. Die Breite kann zwischen 150 und 1280 Pixeln betragen.

1. (Optional) Wählen Sie das Betriebssystem des Geräts aus.

   Optionen:

   * Android
   * iOS
   * Windows
   * Symbian
   * BlackBerry

   Wenn Sie [Enhanced Experience Composer](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) verwenden und ein Betriebssystem auswählen, emuliert dieses Gerät, wenn Sie die Seite aufrufen. [!DNL Target] If, for example, there is a different look and feel for Android than iOS on your responsive site, [!DNL Target] mimics that behavior.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Create a responsive experience {#task_D6332438B5EE48CCA8AF199270F1CAEF}

Add mobile viewports to your [!DNL Target] activities to create responsive experiences for mobile screens.

1. Erstellen Sie die [gewünschte Aktivität](/help/c-activities/activities.md).
1. Klicken Sie im Visual Experience Composer auf das Symbol **[!UICONTROL Einstellungen]** und wählen Sie anschließend **[!UICONTROL Mobile Viewports hinzufügen]** aus.

   ![Option &quot;Hinzufügen Mobile Viewports&quot;](/help/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. Klicken Sie auf das Symbol **[!UICONTROL Geräte]** und aktivieren Sie dann jedes Gerät, das über einen mobilen Viewport verfügen soll.

   ![Aktivieren von mobilen Viewports](/help/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   Die mobilen Viewports sind nach Breite aufsteigend (vom kleinsten zum größten) aufgelistet.

1. Bearbeiten Sie die mobilen Viewports nach Bedarf.

   Alle Änderungen, die Sie an den Erlebnissen vornehmen (zum Beispiel, wenn Sie den Text in einer Überschrift ändern), werden für die Erlebnisse auf allen Geräten angewendet.

   Bewegen Sie den Mauszeiger über den Namen eines Viewports, um die Größe des Viewports anzuzeigen.

   ![iPhone 11 Pro Max. responsive Erlebnisse](/help/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. If desired, toggle between portrait and landscape modes by clicking the desired orientation icon.

   ![Ausrichtungsoptionen](/help/c-experiences/c-visual-experience-composer/assets/orientation.png)

## Use Case: Target two iPhone versions {#task_CC3144BF5BA54034996E1D3DB0BC1A35}

This use case shows how to configure experiences for two iPhone versions: iPhone 6 and iPhone 6 Plus.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. In the **[!UICONTROL Mobile Viewport Configuration]** section, create mobile viewports for iPhone 6 and iPhone 6 plus.

   Verwenden Sie für die Viewports folgende Einstellungen:

   | Name | Breite | Höhe | Betriebssystem |
   |---|---|---|---|
   | iPhone 6 | 375 | 667 | iOS |
   | iPhone 6 Plus | 414 | 736 | iOS |

   ![](assets/iphoneviewportconfig.png)

1. Create an activity with the experience you would like to target.
1. Wählen Sie das Erlebnis aus, das Sie für Benutzer bereitstellen möchten, die über ein iPhone 6 oder iPhone 6 Plus auf Ihre Site zugreifen.
1. Klicken Sie für die Auswahl Ihres Ziels auf **[!UICONTROL Zielgruppe erstellen]** und konfigurieren Sie wie unten dargestellt eine Zielgruppe:

   ![](assets/iphoneaudiences.png)

   Da das iPhone gedreht werden kann und so in das Querformat wechselt, müssen sowohl Breite als auch Höhe gleichzeitig größer als 320 sein. Dies führt zu einer Bedingung, die nur die Geräte 6 und 6 Plus erfüllen, wenn als Gerätemodell das iPhone angegeben wird.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Richten Sie die Aktivität wie gewohnt weiter ein.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Visual Experience Composer (2 von 2) (7:29) ![Übersichtskennzeichnung](/help/assets/overview.png)

Im folgenden Demonstrationsvideo erfahren Sie etwas dazu, wie Sie in Visual Experience Composer mit mobilen Viewports arbeiten:

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Kontovoreinstellungen in der Adobe Target- ![Übersichtskennzeichnung](/help/assets/overview.png)

This video includes information about setting up mobile viewports, beginning at 4:40 in the video.

>[!VIDEO](https://video.tv.adobe.com/v/17379)