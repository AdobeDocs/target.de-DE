---
keywords: responsiv;mobile Viewports;Viewport;Geräte;mobil;responsives Webdesign;rwd
description: Mit mobilen Viewports können Sie sehen, wie Ihre Adobe-[!DNL Target] auf Screens in verschiedenen Größen aussehen. Hier finden Sie eine Liste häufig verwendeter Viewport-Größen und -Auflösungen.
title: Wie verwende ich Mobile Viewports für responsive Erlebnisse?
feature: Visual Experience Composer (VEC)
exl-id: 1062e7a1-10b4-4746-bce9-67017978578d
TQID: 'https://experienceleague.adobe.com/uBJtaoaCh28mRGwc-SlK-XhU6sOIK3RaT58-ZXxSsHw'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 19%
---
# Mobile Viewports für responsive Erlebnisse {#mobile-viewports}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mobile Viewports konfigurieren und verwenden können, um Erlebnisse für Bildschirme verschiedener Größen in der Vorschau anzuzeigen und zu erstellen.

>[!ENDSHADEBOX]

Mobile Viewports zeigen [!DNL Adobe Target] Aktivitäten auf den Bildschirmgrößen verschiedener Geräte an. Sie wurden für responsive Sites entwickelt, die sich automatisch an Desktops, Laptops, Tablets und Mobiltelefone anpassen. Zudem können mit ihnen überprüft werden, ob auf jedem dieser Sites ein Erlebnis gut dargestellt wird.

>[!NOTE]
>
> * Verwenden Sie mobile Viewports, wenn die Site responsiv ist und die mobile Seite die Elemente der Desktop-Seite in einem anderen Layout wiederverwendet. Wenn die mobile Site separat ist und eine eigene Struktur aufweist, z. B. `m.mysite.com`, verwenden Sie stattdessen eine [mehrseitige Aktivität](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#multipage-activity).
>
>* Mobile Viewports sind nicht verfügbar, wenn sich eine Umleitungsangebotsüberlagerung mit ihnen überschneidet.

## Viewports und CSS Breakpoints

Ein Viewport ist der Bereich des Bildschirms, den eine Web-Seite ausfüllt: die Größe des Browser-Fensters abzüglich der Bildlaufleisten und Symbolleisten. Browser messen sie in CSS-Pixeln, sodass auf vielen Geräten, wie z. B. Geräten mit Netzhautbildschirmen, der Viewport kleiner ist als die beworbene Geräteauflösung. Verwenden Sie immer die Viewport-Größe in [!DNL Target]. In der folgenden Tabelle sind beide Werte für gängige Geräte aufgeführt.

+++ Viewports und Auflösungen beliebter Geräte

>[!NOTE]
>
>Auf verschiedenen Websites sind die Viewport-Größen für gängige Geräte aufgeführt. Ein Beispiel finden Sie unter `https://viewportsizer.com/devices/`. Die genauesten und aktuellsten Informationen finden Sie auf der Website des Geräteherstellers.
>
>Darstellungsfeldgrößen mit der Kennzeichnung „Test“. sind Schätzungen.

| Gerät | Viewport-Größe (Breite x Höhe) | Geräteauflösung (Breite x Höhe) |
|---|---|---|
| iPhone 18 Pro Max | 440 x 956 | 1320 x 2868 |
| iPhone 18 Pro | 402 x 874 | 1206 x 2622 |
| iPhone 17 Pro Max | 440 x 956 | 1320 x 2868 |
| iPhone 17 Pro | 402 x 874 | 1206 x 2622 |
| iPhone Air | 420 x 912 | 1260 x 2736 |
| iPhone 17 | 402 x 874 | 1206 x 2622 |
| iPhone 16e | 390 x 844 | 1170 x 2532 |
| iPad (A16) | 820 x 1180 | 1640 x 2360 |
| iPad Mini (A17 Pro) | 744 x 1133 | 1488 x 2266 |
| iPad Air 11″ (M3 / M4) | 820 x 1180 | 1640 x 2360 |
| iPad Pro 11″ (M5) | 834 x 1210 | 1668 x 2420 |
| Google Pixel 11 | 412 x 924 (ca.) | 1080 x 2424 |
| Google Pixel 11 Pro | 410 x 914 (Est.) | 1280 x 2856 |
| Google Pixel 11 Pro XL | 448 x 997 (ca.) | 1344 x 2992 |
| Google Pixel 10 | 412 x 924 | 1080 x 2424 |
| Google Pixel 10 Pro | 410 x 914 (Est.) | 1280 x 2856 |
| Google Pixel 10 Pro XL | 448 x 997 (ca.) | 1344 x 2992 |
| Samsung Galaxy S26 | 360 x 780 | 1080 x 2340 |
| Samsung Galaxy S26 Ultra | 412 x 891 | 1440 x 3120 |
| iPhone Duo (ungefaltet) | 890 x 626 (Est.) | 2670 x 1878 |
| iPhone Duo (gefaltet) | 466 x 678 (ca.) | 1398 x 2034 |
| Samsung Galaxy Z Fold 7 (gefaltet) | 412 x 960 (ca.) | 1080 x 2520 |
| Samsung Galaxy Z Flip 8 | 360 x 840 (ca.) | 1080 x 2520 |
| Google Pixel 11 Pro Fold (entfaltet) | 791 x 820 (ca.) | 2076 x 2152 |

+++

Eine responsive Site wechselt bei bestimmten Bildschirmgrößen zu einem anderen Layout. Diese Größen werden als CSS Breakpoints oder [Medienabfragen) &#x200B;](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries). Wenn Sie die CSS Breakpoints der Website in [!DNL Target] speichern, können Sie jede Ansicht in der Vorschau anzeigen. Wenn Sie oben auf dem Display auf einen Viewport klicken, wird die Ansicht für diese Bildschirmgröße geöffnet.

Um eine Aktivität für ein bestimmtes Gerät bereitzustellen, wählen Sie im Aktivitätsdiagramm die Zielgruppe für dieses Gerät aus und bearbeiten Sie dann die Seite für dieses Gerät im Mobile Web Composer. Mit demselben Tool können Sie eine Site anzeigen, die nicht reagiert, wenn die Aktivität auf ein bestimmtes Gerät abzielt. Um eine Aktivität auf allen Geräten auszuführen, wenden Sie kein Targeting an und zeigen Sie die Aktivität mit mobilen Viewports auf jeder Bildschirmgröße in der Vorschau an.

>[!IMPORTANT]
>
>Erlebnisse können über mobile Viewports bearbeitet werden. Die Änderungen gelten jedoch für alle Viewports und Geräte, nicht nur für den verwendeten Viewport. Auf die gleiche Weise wird beim Bearbeiten eines Erlebnisses in der Desktop-Ansicht die Seite für alle Bildschirmgrößen geändert. [!DNL Target] unterstützt derzeit keine Viewport-spezifischen Seitenänderungen.

## Konfigurieren von mobilen Viewports {#task_B4B161499DC0470584ED922A4D20FCAB}

Definieren Sie die mobilen Viewports, die beim Erstellen von Erlebnissen verfügbar sind.

1. Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. Klicken Sie **[!UICONTROL Abschnitt „Konfiguration mobiler]**&quot; auf **[!UICONTROL Hinzufügen]**.

   ![Viewport hinzufügen](/help/main/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   Oder

   Um die Konfiguration eines vorhandenen mobilen Viewports zu ändern, wählen Sie diesen Viewport aus und klicken Sie dann auf das **[!UICONTROL Bearbeiten]**-Symbol.

1. Geben Sie einen beschreibenden Namen für den mobilen Viewport ein. Der Name kann aus bis zu 36 Zeichen bestehen.
1. Geben Sie die Bildschirmgröße des Mobilgeräts ein. Die Breite kann 150 bis 968 Pixel und die Höhe 150 bis 1280 Pixel betragen.
1. (Optional) Wählen Sie das Betriebssystem des Geräts aus.

   Optionen:

   * Android
   * iOS
   * Windows
   * Symbian
   * BlackBerry

   Wenn [Enhanced Experience Composer](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#enable-eec) aktiviert ist und ein Betriebssystem ausgewählt ist, emuliert [!DNL Target] dieses Gerät, wenn die Seite aufgerufen wird. Wenn die responsive Site beispielsweise für Android ein anderes Erscheinungsbild aufweist als für iOS, ahmt [!DNL Target] dieses Verhalten nach.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Beim Versuch, einen verwendeten mobilen Viewport zu löschen, wird die folgende Meldung angezeigt: „Dieser Viewport ist derzeit mit einer oder mehreren Aktivitäten verknüpft. Entfernen Sie den Viewport aus diesen Aktivitäten, um ihn zu löschen“.

## Erstellen eines responsiven Erlebnisses {#task_D6332438B5EE48CCA8AF199270F1CAEF}

Fügen Sie mobile Viewports zu [!DNL Target] Aktivitäten hinzu, um responsive Erlebnisse für Mobilgeräte zu erstellen.

1. Erstellen Sie die [gewünschte Aktivität](/help/main/c-activities/activities.md).
1. Klicken Sie im **[!UICONTROL Visual Experience]**) auf das Symbol **[!UICONTROL Einstellungen]** und wählen Sie dann **[!UICONTROL Mobile Viewports hinzufügen]**.

   ![Option „Mobile Viewports“](/help/main/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. Klicken Sie auf **[!UICONTROL Geräte]** und aktivieren Sie dann jedes Gerät, das über einen mobilen Viewport verfügen soll.

   ![Mobile Viewports aktivieren](/help/main/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   Die mobilen Viewports sind nach Breite aufsteigend (vom kleinsten zum größten) aufgelistet.

1. Bearbeiten Sie das Erlebnis in den mobilen Viewports nach Bedarf. Jede Änderung gilt für das Erlebnis auf allen Geräten, z. B. eine Änderung am Text einer Überschrift. Bewegen Sie den Mauszeiger über den Namen eines Viewports, um die Größe des Viewports anzuzeigen.

   ![Responsives Erlebnis auf dem iPhone 11 Pro Max](/help/main/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. (Optional) Schalten Sie durch Klicken auf das Ausrichtungssymbol zwischen Hoch- und Querformat um.

   ![Ausrichtungsoptionen](/help/main/c-experiences/c-visual-experience-composer/assets/orientation.png)

## Schulungsvideos

Die folgenden Videos enthalten weitere Informationen zu mobilen Viewports.

### Visual Experience Composer (2 von 2) (7:29) ![Übersichts-Badge](/help/main/assets/overview.png)

Das folgende Demovideo enthält Informationen zur Verwendung von Visual Experience Composer für mobile Viewports:

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/30166?captions=ger)

### Kontovoreinstellungen in Adobe Target ![Übersichts-Badge](/help/main/assets/overview.png)

Dieses Video enthält Informationen zum Einrichten von mobilen Viewports, beginnend um 4:40 Uhr im Video.

>[!VIDEO](https://video.tv.adobe.com/v/3507632?captions=ger)
