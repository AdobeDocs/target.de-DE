---
description: Legen Sie Ihre Kontovoreinstellungen fest, um Target Standard oder Target Premium so zu konfigurieren, dass es korrekt mit Ihrem Konto funktioniert.
keywords: Kontovoreinstellungen;Voreinstellungen;Site-Details;benutzerdefinierter Mbox-Name;für das Reporting verwendete Experience Cloud-Lösung;geschätzte Umsatzsteigerung anzeigen;CSS-Selektoren;Elementklassen verwenden;Standard-URL für Visual Experience Composer;Enhanced Experience Composer aktivieren;Erlebnismomentaufnahmen generieren;mobile Viewport-Konfiguration;Branche;inkompatible Kriterien filtern
seo-description: Legen Sie Ihre Kontovoreinstellungen fest, um Adobe Target Standard oder Target Premium so zu konfigurieren, dass sie ordnungsgemäß mit Ihrem Konto funktionieren.
seo-title: Voreinstellungen
solution: Target
subtopic: Erste Schritte
title: Voreinstellungen
topic: Standard
uuid: ed3904c8-533b-4b9c-a3a1-079c61b1bf2a
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Voreinstellungen{#preferences}

Legen Sie Ihre Kontovoreinstellungen fest, um [!DNL Target Standard] oder [!DNL Target Premium] so zu konfigurieren, dass es korrekt mit Ihrem Konto funktioniert.

Klicken Sie zum Festlegen Ihrer Kontovoreinstellungen auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Voreinstellungen]**, konfigurieren Sie Ihre Voreinstellungen und klicken Sie dann auf **[!UICONTROL Senden]**.

In der folgenden Illustration ist dargestellt, welche Einstellungen auf der Seite [!UICONTROL Kontovoreinstellungen] verfügbar sind.

![Voreinstellungen-Seite](/help/administrating-target/r-target-account-preferences/assets/target-account-preferences.png)

>[!NOTE]
>
>Einige dieser Voreinstellungen sind nur verfügbar, wenn [Sie über Target Premium](/help/c-intro/intro.md#premium)verfügen.

## Site-Details {#section_04A3340FC29B46978DB77058259F4EE0}

Geben Sie an, wie Ihre Site konfiguriert wurde.

### Benutzerdefinierte globale mbox

Wählen Sie den optionalen Namen der von Ihnen zur Bereitstellung von [!DNL Target]-Aktivitäten verwendeten benutzerdefinierten Mbox. Diese globale Mbox muss leer sein, was bedeutet, dass sie keinen Standardinhalt enthält. Speichern Sie diese Einstellung erst, nachdem die aktualisierte Datei [!DNL at.js] auf [!DNL mbox.js] Ihrer Site installiert wurde.

>[!CAUTION]
>
>Ein fehlerhafte Konfiguration dieser Einstellung kann zu Ausfällen vorhandener Aktivitäten führen.

## Ergebnisse und Berichterstellung {#section_47C887AABD704A96BCD1C00BEABF4BCE}

Festlegen von Optionen, mit denen bestimmt wird, welche Daten für Ergebnisse und Berichte verwendet werden

| Option | Beschreibung |
|--- |--- |
| Für die Berichterstellung verwendete Experience Cloud-Lösung | Wählen Sie die Berichterstellungsquelle für Ihre Aktivitäten aus; zur Wahl stehen [!DNL Target] und Adobe Analytics. Sie können die Berichtsquelle auch für jede Aktivität neu auswählen. Beachten Sie bei der Auswahl der Berichtsquelle folgende Informationen:<ul><li>Die Erstellung, Aktivierung und Deaktivierung von Aktivitäten der Typen [!UICONTROL Automatische Zuordnung], [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization] sind unabhängig von der ausgewählten Berichtsquelle zulässig. Diese Aktivitätstypen werden nicht unterstützt, wenn Sie [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) auswählen. Selbst wenn Sie Analytics als Berichtsquelle angeben, wird für diese Aktivitätstypen [!DNL Target] als Quelle verwendet.</li><li>Wenn die Berichtsquelle hier auf Analytics festgelegt ist, dürfen Sie Aktivitäten, die [!DNL Target] als Berichtsquelle verwenden (Target wurde pro Aktivität als Berichtsquelle angegeben), nicht aktivieren. Sie müssen die Berichtsquelle in Ihrer Aktivität zu „Analytics“ oder die Reporting-Engine unter „Setup“ &gt; „Voreinstellungen“ zu „Pro Aktivität auswählen“ ändern.</li><li>Wenn die Berichtsquelle hier auf [!DNL Target] festgelegt ist, dürfen Sie Aktivitäten, die Analytics als Berichtsquelle verwenden, nicht aktivieren. Sie müssen die Berichtsquelle in Ihrer Aktivität zu [!DNL Target]„ “ oder die Berichtsquelle unter „Setup“ &gt; „Voreinstellungen“ zu „Pro Aktivität auswählen“ ändern.</li><li>Wenn die Berichtsquelle auf Pro Aktivität auswählen festgelegt ist, können Sie Aktivitäten erstellen, aktivieren und deaktivieren, die von der ausgewählten Berichtsquelle unterstützt werden. Eine Tabelle unterstützter Aktivitätstypen finden Sie unter [Adobe Analytics als Berichtsquelle für Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).</li><li>Wenn Sie von manuellen A/B-Aktivitäten zu Aktivitäten mit [!UICONTROL automatischer Zuordnung] oder AT-Aktivitäten ([!UICONTROL Automatisches Targeting]) wechseln, gehen alle Metriken und Reporting-Zielgruppen verloren, wenn die Berichtsquelle der manuellen A/B-Aktivität nicht von der [!UICONTROL Aktivität zu automatischer Zuordnung] bzw. der [!UICONTROL AT-Aktivität] unterstützt wird.</li></ul> |
| Geschätzte Umsatzsteigerung anzeigen | Sie können außerdem bestimmen, die Umsatzsteigerung anzuzeigen, wenn Sie für Ihr Ziel einen Geldwert festlegen. [!DNL Target] kann die Umsatzsteigerung schätzen, die Sie erzielen könnten, wenn sich alle Benutzer das erfolgreichste Erlebnis ansehen würden. Die Funktion zur Schätzung der Steigerung ist standardmäßig deaktiviert. <br>Experience Cloud-Administratoren können diese Funktion aktivieren bzw. deaktivieren. Wenn die Schätzung der Steigerung deaktiviert ist, werden die entsprechenden Felder nicht auf der Benutzeroberfläche angezeigt. Durch die Deaktivierung der Funktion gehen keine Daten verloren, auch nicht die Daten, die für Ihre Schätzungen verwendet werden. Die Schätzungen basieren auf den erfassten Daten, unabhängig davon, ob die Funktion aktiviert ist oder nicht.<br>Ausführliche Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| Aktivieren der feinjustierten Prioritäten | Lassen Sie numerische Einträge für die Priorität von 0-999 zu.<br>Abhängig von Ihren Einstellungen variieren die Optionen und die Oberfläche für Prioritäten. Sie können die veralteten Einstellungen „Hoch“, „Mittel“ und „Niedrig“ verwenden oder eine genauere Einstufung mit Werten von 0 bis 999 aktivieren. <br>Die Priorität wird verwendet, wenn mehrere Aktivitäten dem gleichen Ort mit der gleichen Zielgruppe zugewiesen sind. Wenn dem Ort zwei oder mehr Aktivitäten zugewiesen sind, wird die Aktivität mit der höchsten Priorität angezeigt. |

## CSS-Selektoren {#section_8155EDBF449E4198863235F94D1EA872}

Geben Sie an, wie [!DNL Target] CSS-Selektoren generiert.

Diese Optionen helfen [!DNL Target] dabei, die Struktur Ihrer Site zu verstehen, um bessere CSS-Selektoren für die Bereitstellung von Inhalten zu erzeugen. Standardmäßig erstellt [!DNL Target] die Selektoren auf Basis der Element-IDs auf der Seite. Wenn auf Ihrer Site nur wenige IDs verwendet werden oder IDs auf derselben Seite dupliziert werden, ist die Verwendung von Klassen wahrscheinlich die bessere Option.

Sie können eine oder beide der folgenden Optionen verwenden:

| Option | Beschreibung |
|--- |--- |
| Element-IDs verwenden | Deaktivieren Sie diese Option, wenn die gleiche ID für mehrere Elemente verwendet wird oder sich die Element-ID beim Laden der Seite möglicherweise ändert. |
| Elementklassen verwenden | Standardmäßig verwendet [!DNL Target] nur Element-IDs. Wenn Ihre Seite jedoch so entwickelt wurde, dass zur Identifizierung von Elementen Klassen verwendet werden (wie beispielsweise bei einer mit [!DNL Adobe Experience Manager] erstellten Seite), dann sollten Sie die Option [!UICONTROL Elementklassen verwenden] auswählen.<br>**Hinweis:** Obwohl alles unternommen wurde, um Genauigkeit sicherzustellen, sollten Sie bedenken, dass die Verwendung von Klassen zu Fehlern führen kann. Wenn Sie keine der beiden Optionen auswählen, hat dies auch Auswirkungen auf die Genauigkeit. Die Reihenfolge für Genauigkeit lautet IDs &gt; Klassen &gt; keine der beiden Optionen. Sie sollten Ihre Seite immer testen, um sicherzustellen, dass die Selektoren korrekt sind.<br>Sie können diese Einstellung pro Aktivität außer Kraft setzen (klicken Sie dazu auf das Zahnradsymbol [!UICONTROL Einstellungen] und wählen Sie anschließend [!UICONTROL CSS-Selektoren] aus). Dies ist besonders dann nützlich, wenn Sie mehrere Sites haben, die unterschiedlich konfiguriert sind.<br>**Hinweis:** Die Außerkraftsetzung der Einstellung pro Aktivität ist nicht in den Aktivitäten [!UICONTROL Automated Personalization] und [!UICONROL Multivarianz-Tests] verfügbar. Weitere Informationen zu Selektoren finden Sie im Abschnitt [Element-Selektoren, die im Visual Experience Composer verwendet werden](/help/c-experiences/c-visual-experience-composer/vec-selectors.md). |

## Visual Experience Composer {#section_CD9BDD372CF54E678F88E8BA95757A5A}

| Option | Beschreibung |
|--- |--- |
| Standard-URL des Visual Experience Composer | Die Standard-URL, die von [!UICONTROL Visual Experience Composer] verwendet wird. Dies ist die Standardseite, wie Ihre Startseite, die verwendet wird, wenn Sie ein Erlebnis für jede neue Aktivität einrichten. Sollten Sie keine Standard-URL festlegen, müssen Sie für jede Aktivität bei deren Erstellung eine eigene URL eingeben. |
| Erweiterten Experience Composer aktivieren | Ermöglicht die Bearbeitung auf Sites, die iFrames zerstören, sowie auf Seiten mit gemischten Inhalten. Einige Sites sind möglicherweise nicht mit der erweiterten Version kompatibel. Heben Sie die Auswahl für diese Option auf, um zum ursprünglichen Experience Composer zurückzukehren. Die Aktivitätenbereitstellung auf Sites wird durch diese Auswahl nicht beeinträchtigt.<br>Weitere Informationen finden Sie unter [Fehlerbehebung beim Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).<br>**Hinweis:** Sie können den Enhanced Experience Composer auch auf Aktivitätsebene aktivieren. |
| Gemischte Inhalte laden | Aktivieren Sie gemischte Inhalte, wenn Sie eine Website mit Enhanced Experience Composer öffnen. Durch Aktivierung dieser Option werden statische Ressourcen über Target-Proxy-Server nicht mehr geladen. |
| Erlebnismomentaufnahmen generieren | Bei der Aktivierung von Erlebnismomentaufnahmen werden Miniaturen Ihrer Erlebnisse in der Übersicht des Aktivitätsarbeitsablaufs generiert. Die Deaktivierung von Momentaufnahmen kann bei einigen Benutzern zu einer Beschleunigung der Performance führen. |

## Mobile Viewport-Konfiguration {#section_42176D062BCE4A28ADBB784CC4BEF84D}

Sie können Geräte hinzufügen, die für die Vorschau der Erlebnisse verwendet werden sollen. Jedem Gerät ist dabei eine Zielgruppe zugeordnet.

| Option | Beschreibung |
|--- |--- |
| ![Premium-Zeichen](/help/assets/premium.png) Neu hinzufügen | Klicken Sie auf [!UICONTROL Neu hinzufügen], geben Sie einen beschreibenden Namen für den mobilen Viewport ein, legen Sie Höhe und Breite fest, wählen Sie das gewünschte Betriebssystem aus und klicken Sie auf [!UICONTROL Speichern]. Informationen zum Hinzufügen eines mobilen Viewports finden Sie unter [Mobile Viewport – Konfiguration](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md). |

## Schulungsvideo: Kontovoreinstellungen (7:33)

In diesem Video finden Sie Informationen zu Kontovoreinstellungen.

* Beschreibung der in [!DNL Target Standard] verfügbaren Kontoeinstellungen

>[!VIDEO](https://video.tv.adobe.com/v/17379)