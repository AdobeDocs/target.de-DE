---
keywords: responsiv;mobile Viewports;Viewport;Geräte;Mobil;reaktionsfähiges Webdesign;rwd
description: Mit mobilen Viewports können Sie sehen, wie Ihre Adobe Target-Aktivitäten auf Bildschirmen unterschiedlicher Größe aussehen. Finden Sie eine Liste der beliebten Viewport-Größen und -Auflösungen des Geräts.
title: Wie verwende ich mobile Viewports für responsive Erlebnisse?
feature: 'Visual Experience Composer (VEC) '
translation-type: tm+mt
source-git-commit: 69677b9d384d9817a39386fc1388a4aa42121713
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 36%

---


# Mobile Viewports für responsive Erlebnisse

Mit mobilen Viewports können Sie Ihre [!DNL Adobe Target]-Aktivitäten auf Bildschirmen unterschiedlicher Größe Vorschau werden.

Die Funktion zur mobilen Viewport-Vorschau wurde für responsive Sites entwickelt, die auf verschiedenen Geräten, Fenstern und Bildschirmgrößen gut dargestellt werden. Responsive Sites passen sich automatisch an jede Bildschirmgröße an, einschließlich Desktop-PCs, Laptops, Tablets oder Mobiltelefone.

>[!NOTE]
>
> * Verwenden Sie mobile Viewports, wenn Ihre Site responsiv ist und dieselben Elemente auf Ihrer Desktop-Seite in einer anderen Konfiguration auf Ihrer mobilen Seite verwendet werden. Wenn Sie eine separate Mobilgeräte-Site mit einer separaten Struktur haben, z. B. `m.mysite.com`, verwenden Sie stattdessen eine [mehrseitige Aktivität](/help/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48).
   >
   >
* Mobile Viewports sind nicht verfügbar, wenn sie von einem Umleitungsangebot überlagert werden.


Ein Viewport wird durch die Größe des Rechtecks definiert, das von einer Webseite auf Ihrem Bildschirm ausgefüllt wird. Der Viewport ist die Größe des Browser-Fensters abzüglich der Bildlaufleisten und Symbolleisten. Browser verwenden „CSS-Pixel“. Für viele Geräte, zum Beispiel solche mit Retina-Bildschirm, ist der Viewport kleiner als die beworbene Geräteauflösung.

Nachstehend finden Sie die Viewports und Auflösungen für gängige Geräte. Denken Sie daran, die Viewport-Größe in [!DNL Target] zu verwenden.

>[!NOTE]
>
>Auf verschiedenen Websites sind die Viewport-Größen für gängige Geräte aufgeführt. Siehe z. B. [https://viewportsizer.com/devices/](https://viewportsizer.com/devices/). Die genauesten und aktuellsten Informationen finden Sie auf der Website des Geräteherstellers.

| Gerät | Viewport-Größe (Breite x Höhe) | Geräteauflösung (Breite x Höhe) |
|---|---|---|
| iPhone 12 | 390 x 844 | 1170 x 2532 |
| iPhone 12 Mini | 360 x 780 | 1080 x 2340 |
| iPhone 11 Pro | 390 x 844 | 1170 x 2532 |
| iPhone 12 Pro Max | 428 x 926 | 1248 x 2778 |
| iPhone SE | 214 x 379 | 640 x 1136 |
| iPhone 11 Pro Max | 414 x 896 | 1242 x 2688 |
| iPhone 11 Xs Max. | 414 x 896 | 1242 x 2688 |
| iPhone 11 | 414 x 896 | 828 x 1792 |
| iPhone 11 Xr | 414 x 896 | 828 x 1792 |
| iPhone 12 Pro | 375 x 812 | 1125 x 2436 |
| iPhone 11 X | 375 x 812 | 1125 x 2436 |
| iPhone 11 Xs | 375 x 812 | 1125 x 2436 |
| iPhone X | 375 x 812 | 1125 x 2436 |
| iPhone 8 Plus | 414 x 736 | 1080 x 1920 |
| iPhone 8 | 375 x 667 | 750 x 1334 |
| iPhone 7 Plus | 414 x 736 | 1080 x 1920 |
| iPhone 7 | 375 x 667 | 750 x 1334 |
| iPhone 6s Plus | 414 x 736 | 1080 x 1920 |
| iPhone 6s | 375 x 667 | 750 x 1334 |
| iPhone 6 Plus | 414 x 736 | 1080 x 1920 |
| iPhone 6 | 375 x 667 | 750 x 1334 |
| iPad  Pro | 1024 x 1366 | 2048 x 2732 |
| iPad der 3. und 4. Generation | 768 x 1024 | 1536 x 2048 |
| iPad Air 1 und 2 | 768 x 1024 | 1536 x 2048 |
| iPad Mini | 768 x 1024 | 768 x 1024 |
| iPad Mini 2 und 3 | 768 x 1024 | 1536 x 2048 |
| Nexus 6P | 411 x 731 | 1440 x 2560 |
| Nexus 5X | 411 x 731 | 1080 x 1920 |
| Google Pixel | 411 x 731 | 1080 x 1920 |
| Google Pixel XL | 411 x 731 | 1440 x 2560 |
| Google Pixel 2 | 411 x 731 | 1080 x 1920 |
| Google Pixel 2 XL | 411 x 823 | 1440 x 2880 |
| Samsung Galaxy Note 5 | 480 x 853 | 1440 x 2560 |
| LG G5 | 360 W x 640 | 1440 x 2560 |
| LG G4 | 360 W x 640 | 1440 x 2560 |
| LG G3 | 360 W x 640 | 1440 x 2560 |
| One Plus 3 | 480 x 853 | 1080 x 1920 |
| Samsung Galaxy S9 | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S9+ | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S8 | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S8+ | 360 x 740 | 1440 x 2960 |
| Samsung Galaxy S7 | 360 x 640 | 1440 x 2560 |
| Samsung Galaxy S7 Edge | 360 x 640 | 1440 x 2560 |
| Nexus 7 (2013) | 600 x 960 | 1200 x 1920 |
| Nexus 9 | 768 x 1024 | 1536 x 2048 |
| Samsung Galaxy Tab 10 | 800 x 1280 | 800 x 1280 |
| Chromebook Pixel | 1280 x 850 | 2560 x 1700 |

Um eine Aktivität für Besucher auf einem bestimmten Gerät bereitzustellen, wählen Sie die entsprechende Audience für dieses Gerät im Diagramm für die Aktivität. Verwenden Sie den Mobile Web Composer, um die Seite für das Gerät in der Aktivität zu bearbeiten. Wenn Sie eine Aktivität auf Ihrem gesamten digitalen Erlebnis ausführen möchten, um sicherzustellen, dass sie auf allen Geräten gut aussieht, wenden Sie kein Targeting an. Verwenden Sie stattdessen mobile Viewports, um die Aktivität in jeder Bildschirmgröße Vorschau.

Bei responsive Sites wird Ihre Site in der Regel auf eine andere Ansicht geöffnet, wenn der Zugriff über ein Gerät mit einer bestimmten Bildschirmgröße erfolgt. Diese Bildschirmgrößen, die solche neuen Ansichten auslösen, werden auch als CSS-Haltepunkte bezeichnet. CSS-Haltepunkte sind Punkte, an denen Website-Inhalte je nach Gerätebreite antworten, um das optimale Layout für Besucher anzuzeigen. CSS-Haltepunkte werden auch als [Media-Abfragen](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries) bezeichnet.

Speichern Sie Ihre CSS-Haltepunkte in [!DNL Target], damit Sie Ihre Erlebnisse für jede von Ihnen definierte Ansicht Vorschau haben. Jedes dieser Erlebnisse wird in einem mobilen Viewport in der [!DNL Target]-Schnittstelle angezeigt. Öffnen Sie die Ansicht für jeden Bildschirm, indem Sie entlang der Oberkante der Anzeige auf diesen Viewport klicken.

Wenn Ihre Site nicht responsiv ist, verwenden Sie den Mobile Web Composer, um eine Site Ansicht, wenn Ihre Aktivität auf ein bestimmtes Gerät ausgerichtet ist.

>[!IMPORTANT]
>
>Sie können ein Erlebnis in mobilen Viewports bearbeiten. Diese Änderungen gelten jedoch für alle Viewports und Geräte, nicht nur für den Viewport, in dem Sie arbeiten. Gleichermaßen wird bei der Bearbeitung eines Erlebnisses in der normalen Desktop-Ansicht die Seite für alle Bildschirmgrößen und nicht nur für die Desktop-Ansicht geändert. Derzeit unterstützt [!DNL Target] keine Viewport-spezifischen Seitenänderungen.

## Mobile Viewport-Konfiguration {#task_B4B161499DC0470584ED922A4D20FCAB}

Konfigurieren Sie die mobilen Viewports, die Sie beim Erstellen Ihrer Erlebnisse verfügbar machen möchten.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. Klicken Sie im Abschnitt **[!UICONTROL Mobile Viewports configuration]** auf **[!UICONTROL Hinzufügen]**.

   ![hinzufügen Viewport](/help/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   Oder

   Um die Konfiguration eines vorhandenen mobilen Viewports zu ändern, wählen Sie diesen Viewport aus und klicken Sie dann auf das Symbol [!UICONTROL Bearbeiten] (Stiftsymbol).

1. Geben Sie einen Namen für den mobilen Viewport ein.

   Geben Sie Ihrem mobilen Viewport einen beschreibenden Namen, der leicht wiederzuerkennen ist. Der Name kann aus bis zu 36 Zeichen bestehen.

1. Geben Sie die Bildschirmgröße des Mobilgeräts an (Breite und Höhe).

   Die Breite kann 150 bis 968 Pixel betragen. Die Höhe kann 150 bis 1280 Pixel betragen.

1. (Optional) Wählen Sie das Betriebssystem des Geräts aus.

   Optionen:

   * Android
   * iOS
   * Windows
   * Symbian
   * BlackBerry

   Wenn Sie [Enhanced Experience Composer](/help/c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) verwenden und ein Betriebssystem auswählen, emuliert dieses Gerät, wenn Sie die Seite aufrufen. [!DNL Target] Beispiel: Wenn Android ein anderes Erscheinungsbild hat als iOS auf Ihrer responsiven Site, [!DNL Target] imitiert dieses Verhalten.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Wenn Sie versuchen, einen verwendeten mobilen Viewport zu löschen, wird die folgende Meldung angezeigt: &quot;Dieser Viewport ist derzeit einer oder mehreren Aktivitäten zugeordnet. Sie müssen den Viewport aus diesen Aktivitäten entfernen, bevor Sie ihn löschen können.&quot;

## Reaktionsfähiges Erlebnis {#task_D6332438B5EE48CCA8AF199270F1CAEF} erstellen

hinzufügen mobilen Viewports auf Ihre [!DNL Target]-Aktivitäten, um responsive Erlebnisse für Mobilgeräte zu erstellen.

1. Erstellen Sie die [gewünschte Aktivität](/help/c-activities/activities.md).
1. Klicken Sie im Bereich [!UICONTROL Visual Experience Composer] (VEC) auf das Zahnradsymbol **[!UICONTROL Einstellungen]** und wählen Sie **[!UICONTROL Hinzufügen Mobile Viewports]**.

   ![Option &quot;Hinzufügen Mobile Viewports&quot;](/help/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. Klicken Sie auf das Symbol **[!UICONTROL Geräte]** und aktivieren Sie dann jedes Gerät, das über einen mobilen Viewport verfügen soll.

   ![Aktivieren von mobilen Viewports](/help/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   Die mobilen Viewports sind nach Breite aufsteigend (vom kleinsten zum größten) aufgelistet.

1. Bearbeiten Sie die mobilen Viewports nach Bedarf.

   Änderungen, die Sie am Erlebnis vornehmen, werden auf allen Geräten auf das Erlebnis angewendet. Sie können beispielsweise den Text in einer Überschrift ändern.

   Bewegen Sie den Mauszeiger über den Namen eines Viewports, um die Größe des Viewports anzuzeigen.

   ![iPhone 11 Pro Max. responsive Erlebnisse](/help/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. Schalten Sie bei Bedarf zwischen Hoch- und Querformat um, indem Sie auf das gewünschte Ausrichtungssymbol klicken.

   ![Ausrichtungsoptionen](/help/c-experiences/c-visual-experience-composer/assets/orientation.png)

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Visual Experience Composer (2 von 2) (7:29)  ![Übersichtskennzeichnung](/help/assets/overview.png)

Im folgenden Demonstrationsvideo erfahren Sie etwas dazu, wie Sie in Visual Experience Composer mit mobilen Viewports arbeiten:

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Kontovoreinstellungen in Adobe Target ![Kennzeichen &quot;Überblick](/help/assets/overview.png)

Dieses Video enthält Informationen zum Einrichten von mobilen Viewports, beginnend um 4:40 Uhr im Video.

>[!VIDEO](https://video.tv.adobe.com/v/17379)