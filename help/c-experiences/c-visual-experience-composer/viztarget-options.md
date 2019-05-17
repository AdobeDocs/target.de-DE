---
description: Wenn Sie im Visual Experience Composer (VEC) auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt.
keywords: Optionen in Visual Experience Composer;Optionen in Experience Composer;Erlebnisoptionen;Text bearbeiten;HTML bearbeiten;Text/HTML bearbeiten;Hintergrundfarbe bearbeiten;Hintergrundfarbe;Element einfügen;Link bearbeiten;Link;Link für Visual Experience Composer;CSS-Klasse bearbeiten;CSS-Klasse;Angebot austauschen;Austausch von Angeboten;Austausch;Bild tauschen;Bildaustausch;Element entfernen;Entfernung von Elementen;Element ausblenden;Ausblendung von Elementen;neu anordnen;Element verschieben;Verschiebung von Elementen;Größe ändern;Größe anpassen;Element;Auswahl erweitern;zu diesem Link navigieren;zu Link navigieren;Linknavigation;navigieren;Link;rückgängig machen;wiederholen;rückgängig/wiederholen
seo-description: Wenn Sie im Adobe Target Visual Experience Composer (VEC) auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt.
seo-title: Adobe Target Visual Experience Composer (VEC)-Optionen
solution: Target
title: Visual Experience Composer-Optionen
topic: Standard
uuid: efd672ae-c684-455f-8ec1-0efcfe1e9534
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Visual Experience Composer-Optionen{#visual-experience-composer-options}

Wenn Sie im Visual Experience Composer (VEC) auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt. Darüber hinaus wird am unteren Rand der Seite ein DOM-Pfad angezeigt, mit dem Sie einfach durch die Seitenstruktur navigieren können.

## VEC-Optionen

Die verschiedenen Visual Experience Composer-Aktionen (VEC) sind geeignete Menüoptionen, um Ihren Auftrag schneller und effizienter zu gestalten:

![VEC-Optionsmenü](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Die verfügbaren Optionen hängen von dem Aktivitätstyp ab, den Sie bearbeiten.

### Bearbeiten  

Die folgenden Optionen sind verfügbar:

#### Text/HTML {#edit-text-html}

Ändern Sie den HTML-Code für das Element, etwa den Text für einen Textbereich, eine Schaltfläche oder einen Link.

Neben HTML-Code können Sie auch benutzerdefiniertes JavaScript bearbeiten und einfügen.

Beim Bearbeiten von Text und HTML für [!UICONTROL A/B]- und [!UICONTROL Erlebnisziel-Aktivitäten] stehen mehrere Rich-Text-Formatierungsoptionen zur Verfügung. Sie können eine Schriftart und einen Schriftstil auswählen, die Textausrichtung ändern und andere Standardformatierungsoptionen für Texte anwenden. Beim Ändern von HTML können Sie zwischen der Codeansicht und der Rich-Text-Bearbeitungsansicht der HTML umschalten.

Die folgenden HTML 5-Tags können verschachtelt sein:

| Markieren | Zulässige verschachtelte Tags |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

#### Hintergrundfarbe

Verwenden Sie den Farbwähler, um eine Hintergrundfarbe auszuwählen oder zu konfigurieren. Sie können ein Farbmuster auswählen und es mithilfe von RGB-Werten oder Farb-Hex-Codes anpassen. Das rote X im Farbwähler macht den Hintergrund transparent.

**Hinweis:** Diese Option ist nicht für Elemente verfügbar, wenn ein Hintergrundbild festgelegt ist.

#### Stile

Verwenden Sie das [!UICONTROL Stilbedienfeld] , um den Wert vorhandener Stile für das ausgewählte Element anzuzeigen oder zu bearbeiten. Sie können auch zusätzliche Formatierungen hinzufügen.

Um auf das [!UICONTROL Stile] -Bedienfeld zuzugreifen, klicken Sie innerhalb des VEC auf ein Seitenelement und dann auf **[!UICONTROL Bearbeiten]** &gt; **[!UICONTROL Stile]**.

Das [!UICONTROL Stile] -Bedienfeld wird rechts im VEC angezeigt. Das Bedienfeld enthält eine Liste der Stile, mit denen Sie das ausgewählte Element bearbeiten oder zum ausgewählten Element hinzufügen können. Mit einem Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie Cascading Style Sheets (CSS) problemlos verwenden oder Code von Ihrem Entwickler erhalten.

![Stilbedienfeld](/help/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Wenn Sie verschiedene Stile anwenden, können Sie Ihre Änderungen jederzeit wieder rückgängig machen, indem Sie auf das [!UICONTROL Symbol &quot;Wiederherstellen&quot;] klicken, das in der rechten oberen Ecke des [!UICONTROL Stilebedienfelds] angezeigt wird, nachdem Sie an einem beliebigen Abschnitt Änderungen vorgenommen haben. Beachten Sie, dass durch Klicken auf das [!UICONTROL Symbol Wiederherstellen] alle Änderungen im Bedienfeld des aktuellen Abschnitts wiederhergestellt werden.

Erweitern Sie den Abschnitt, um Stile zu bearbeiten oder hinzuzufügen, wie unten beschrieben. Um Ihre Änderungen zu speichern, klicken Sie oben im Bedienfeld auf das Symbol &quot;Zurück&quot; , um zur Hauptanzeige des Bedienfelds zurückzukehren, und klicken **[!UICONTROL Sie dann auf&quot; Speichern]**«.

Beachten Sie, dass blaue Punkte im Hauptbereich und neben jeder Option in den verschiedenen Bereichen angezeigt werden, dass Sie Änderungen an den entsprechenden Stilen vorgenommen haben. Auf diese Weise können Sie Ihre Änderungen einfach überprüfen, bevor Sie auf [!UICONTROL Speichern]klicken.

>[!NOTE]
>
>Schnellaktionen für Layoutänderungen, Hintergrundfarbe, Größenanpassung und Verschieben sind ebenfalls als separate Aktionen im VEC-Menü verfügbar. Diese Optionen können als separate Aktionen genutzt werden oder Sie können das Menü &quot;Stile&quot; verwenden, wie hier beschrieben.

* **Typografie**

   Ändern Sie die Typografie eines Elements. Die Bearbeitung von Typografie ist schnell und einfach.

   Auch wenn der Rich-Text-Editor (Text/HTML bearbeiten) zur Feinabstimmung verfügbar ist, sind über diese Option Schnellaktionen verfügbar, um Änderungen am gesamten Element vorzunehmen. Wenn Sie die Typografie nur auf einen Teil des Textes anwenden möchten (nicht auf den Volltext), verwenden Sie den [Rich-Text-Editor](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   Sie können die folgenden Typografie-Stile bearbeiten:

   * Schriftgröße
   * Schriftstärke
   * Schriftschnitt
   * Farbe (geben Sie den Farbcode an oder verwenden Sie den Farbwähler)
   * Wortabstand
   * Zeilenhöhe
   * Textausrichtung

* **Marge**

   Ändern Sie den Rand für das ausgewählte Element. Sie können die linken, rechten, unteren und oberen Ränder ändern.

   Klicken Sie auf das Dropdownsymbol für jeden Rand, um die folgenden Optionen auszuwählen:

   * Auto
   * Wert (ziehen Sie den Regler, um den Rand festzulegen oder die Anzahl der Pixel für jeden Rand festzulegen)
   Marge unterstützt positive und negative Werte.

   Target unterstützt auch andere Größeneinheiten wie rem, pc, em usw. Weitere Informationen zu diesen Einheiten finden Sie unter [CSS Tips und Tricks für Web-Stylesheets](https://www.w3.org/Style/Examples/007/units.en.html).

* **Padding**

   Ändern Sie die Umrandung für das ausgewählte Element. Sie können die linke, rechte, untere und obere Umrandung ändern.

   Ziehen Sie den Schieberegler, um die Umrandung festzulegen oder die Anzahl der Pixel für die Füllung festzulegen.

   Die erweiterte Breite unterstützt die Breite von 0 ab.

   Target unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html)wie rem, pc, em usw.

* **Rand**

   Klicken Sie auf die Rahmensymbole oben im Bedienfeld, um den Rahmen des ausgewählten Elements zu ändern.

   Sie können die folgenden Stile für jeden Rand bearbeiten (oben, rechts, unten und links):

   * Randstil (keine, ausgeblendet, gepunktet, dashed, solid oder double)
   * Rahmenfarbe (geben Sie den Farbcode an oder verwenden Sie den Farbwähler)
   * Rahmenbreite (Ziehen Sie den Regler, um eine Rahmenbreite auszuwählen oder die Breite in Pixel festzulegen)
   Der Rahmen unterstützt die Breite von 0 ab.

   Target unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html)wie rem, pc, em usw.

* **Position**

   Verschiebt das ausgewählte Element von seiner aktuellen Position aus. Sie können die Top-, Bottom-, Left-, Right- und [Z-Indexposition](https://www.w3schools.com/cssref/pr_pos_z-index.asp) des Elements ändern.

   Klicken Sie auf [!UICONTROL die] Dropdownliste Statische, um aus den folgenden Positionsoptionen auszuwählen:

   * Statisch
   * Relativ
   * Absolut 
   * Stickiness
   * Behoben
   Klicken Sie auf das Dropdownsymbol für jede Position, um die folgenden Optionen auszuwählen:

   * Auto
   * Wert (ziehen Sie den Schieberegler, um das Element zu positionieren oder die Anzahl der Pixel anzugeben, die das Element verschieben möchten)
   Position unterstützt positive und negative Werte.

   Target unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html)wie rem, pc, em usw.

* **Größe**

   Ändern Sie die Breite und Höhe des ausgewählten Elements.

   Klicken Sie auf das Dropdownsymbol neben [!UICONTROL Breite] und [!UICONTROL Höhe] , um die folgenden Optionen auszuwählen:

   * Auto
   * Wert (ziehen Sie den Regler, um das Element zu vergrößern, oder geben Sie die Anzahl der Pixel für jede Dimension an)

* **Filter**

   Ziehen Sie den Schieberegler für jede Filteroption oder geben Sie den gewünschten Prozentsatz an:

   * Sepia
   * Kontrast
   * Helligkeit
   * Grayscale
   * Weichzeichnen
   * Deckkraft
   * Invertieren
   * Hue-rotate
   * Sättigung

* **CSS Editor**

   Im Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie mit Cascading Style Sheets (CSS) problemlos arbeiten oder Code von Ihrem Entwickler erhalten.

   Im CSS-Editor werden alle Änderungen angezeigt, die Sie im Stilbedienfeld vornehmen. Wie in unten stehender Abbildung gezeigt, wurden Schriftgröße, obere Rand und Bildgröße geändert:

   ![CSS-Editor mit Änderungen](/help/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Beachten Sie die blauen Punkte neben [!UICONTROL den Optionen &quot;Typografie&quot;], [!UICONTROL &quot; Rand&quot;]und [!UICONTROL &quot;Größe] &quot; in der obigen Abbildung. Diese Punkte zeigen an, dass Sie Änderungen an diesen Abschnitten vorgenommen haben. Wenn Sie diese Abschnittsbedienfelder öffnen, werden neben den spezifischen Optionen, die Sie geändert haben, blaue Punkte angezeigt.

   Sie können Ihren eigenen Code eingeben, wenn der gewünschte Stil standardmäßig nicht in den [!UICONTROL Stilen verfügbar]ist.

   Beachten Sie, dass im CSS-Editor nur Details für die aktuelle Sitzung angezeigt werden. Wenn Sie Änderungen speichern und den Editor dann erneut öffnen, werden Details zu Ihrer vorherigen Änderung nicht im Editor angezeigt, auch wenn Sie dasselbe Element erneut auswählen.

   >[!Important]
   >
   >Sie können ein Hintergrundbild mithilfe des CSS-Editors anwenden, es kann jedoch zu Flackern führen. Testen Sie Ihre Änderungen vor der Bereitstellung.

#### CSS-Klasse

Geben Sie die vordefinierte CSS-Klasse, die für das Element verwendet wurde, an. Wenn mehr als ein Element ausgewählt ist, trennen Sie mehrere CSS-Klassen durch ein Leerzeichen.

Verfügbar für Aktivitäten mit [!UICONTROL A/B], [!UICONTROL Automated Personalization] und [!UICONTROL Multivarianz-Tests].

#### Link

Ändern Sie die URL im Link.

Verwenden Sie „Link bearbeiten“, um die Auswahl zu aktualisieren, damit auf dasselbe Bildelement gezeigt wird. Die Verlinkung zu einem anderen Bildelement wird jedoch nicht unterstützt. Um eine Verlinkung zu einem anderen Bildelement herzustellen, löschen Sie die ursprüngliche Aktion aus dem Code-Editor und verwenden Sie den [!UICONTROL Visual Experience Composer], um die Aktion auf das andere Bildelement anzuwenden.

### Einfügen vor

Die folgenden Optionen sind verfügbar:

#### Bild, HTML und Text

Fügen Sie zusätzlich zur Bearbeitung von bestehendem Inhalt nun auch jede Art von Elementen zu Ihrer Seite hinzu. Fügen Sie Text, Code, Listen und mehr hinzu, um komplett unterschiedliche Erlebnisse zum Testen zu erstellen.

Wählen Sie ein Element auf der Seite aus, klicken Sie auf [!UICONTROL Einfügen vor] und wählen Sie aus, ob Sie ein Bild, HTML-Code oder Text einfügen möchten. Das eingefügte Element wird vor dem ausgewählten Element angezeigt.

Das Verhalten des eingefügten Elements hängt von der Struktur der Seite, Ihrem CSS und anderen Seitenkonfigurationsoptionen ab. Für eine korrekte Anzeige der Seite ist gültiges HTML erforderlich. Sie sollten Ihre Seite nach dem Einfügen eines Elements immer testen, um sicherzustellen, dass sie wie erwartet angezeigt wird.

[!UICONTROL Recommendations] unterstützt das [!UICONTROL Einfügen vor] Inhalten von DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:**[!DNL Adobe Scene7 Publishing System] Für das Einfügen eines Bildes muss aktiviert sein, damit Sie Zugriff auf die Bildbibliothek haben.

#### Empfehlung

Schließen Sie Recommendations in A/B-Test- (einschließlich automatische Zuordnung und automatisches Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md).

#### Erlebnisfragment

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Einfügen nach

Die folgenden Optionen sind verfügbar:

#### Bild, HTML und Text

Fügen Sie zusätzlich zur Bearbeitung von bestehendem Inhalt nun auch jede Art von Elementen zu Ihrer Seite hinzu. Fügen Sie Text, Code, Listen und mehr hinzu, um komplett unterschiedliche Erlebnisse zum Testen zu erstellen.

Wählen Sie ein Element auf der Seite aus, klicken Sie auf [!UICONTROL Einfügen nach] und wählen Sie aus, ob Sie ein Bild, HTML-Code oder Text einfügen möchten. Das eingefügte Element wird nach dem ausgewählten Element angezeigt.

Das Verhalten des eingefügten Elements hängt von der Struktur der Seite, Ihrem CSS und anderen Seitenkonfigurationsoptionen ab. Für eine korrekte Anzeige der Seite ist gültiges HTML erforderlich. Sie sollten Ihre Seite nach dem Einfügen eines Elements immer testen, um sicherzustellen, dass sie wie erwartet angezeigt wird.

[!UICONTROL Recommendations] unterstützt das [!UICONTROL Einfügen nach] nach DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:**[!DNL Adobe Scene7 Publishing System] Für das Einfügen eines Bildes muss aktiviert sein, damit Sie Zugriff auf die Bildbibliothek haben.

#### Empfehlung

Schließen Sie Recommendations in A/B-Test- (einschließlich automatische Zuordnung und automatisches Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md).

#### Erlebnisfragment

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Ersetzen durch

Die folgenden Optionen sind verfügbar:

#### Bild

Wählen Sie ein anderes Bild aus der Inhaltsbibliothek. Die für den Tausch verfügbaren Bilder beinhalten auch Bilder, die in den Asset-Ordner von Experience Cloud oder in die Inhaltsbibliothek in Target hochgeladen wurden.

Bei der eigentlichen Erstellung der Aktivität ist die angezeigte URL nicht die für die Bereitstellung genutzte URL. Nach der Synchronisierung wird diese URL auf eine Produktions-URL für Scene7 aktualisiert.

Die ursprüngliche URL könnte beispielsweise wie folgt aussehen:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Nach Synchronisierung der Aktivität sieht die URL möglicherweise wie folgt aus:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations unterstützt Ersetzen durch DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:** Für den Tausch von Bildern ist ein Adobe Scene7 Publishing System-Konto erforderlich.

#### HTML-Angebot

Wählen Sie in der [!UICONTROL Inhaltsbibliothek] ein anderes Angebot aus.

**Hinweis:** HTML-Angebote werden auf [!DNL Target]-Servern gespeichert.

Die zulässige Maximalgröße eines HTML-Angebots beträgt 256 KB.

#### Empfehlung

Schließen Sie Recommendations in A/B-Test- (einschließlich automatische Zuordnung und automatisches Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md).

#### Erlebnisfragment

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Layout

Die folgenden Optionen sind verfügbar:

#### Neu anordnen

Ziehen Sie das Element an einen anderen Ort innerhalb des gleichen übergeordneten Elements oder DIV. Andere Elemente wechseln den Standort, um für das neu angeordnete Element Platz zu schaffen.

**Hinweis:** Klick-Tracking kann für neu angeordnete Elemente nicht durchgeführt werden.

#### Größe ändern

Ändern Sie die Größe eines Elements auf Ihrer Seite. Wenn Sie [!UICONTROL Größe ändern] auswählen, erscheint ein Handle an einer Ecke des Elements, an dem Sie es größer oder kleiner ziehen können. Halten Sie die Umschalttaste gedrückt, um das Größenverhältnis beizubehalten.

**Hinweis:** Die Größe von Inline-Elementen kann nicht geändert werden.

#### Verschieben  

Verschieben Sie Elemente auf Ihrer Seite. Im Gegensatz zu [!UICONTROL Elemente neu anordnen] werden bei der Option [!UICONTROL Verschieben] keine anderen Elemente verschoben, um Platz für das verschobene Element zu machen. Verwenden Sie die Pfeiltasten, um geringfügige Korrekturen vorzunehmen. (Geplante Erweiterung: Es soll sichergestellt werden können, dass verschobene Elemente nicht hinter anderen Elementen verborgen werden.)

In manchen Fällen, zum Beispiel wenn eine CSS-Beschränkung es erfordert, dass ein Element innerhalb des übergeordneten Elements verbleibt, können Sie das Element nicht außerhalb des übergeordneten Elements verschieben.

#### Ausblenden

Blenden Sie das Element aus. Der weiße Bereich bleibt bestehen, der Inhalt wird jedoch entfernt.

#### Entfernen

Entfernen Sie das Element. Der weiße Bereich hinter dem Bild wird entfernt, und der Bereich, in dem sich das Element befand, wird ausgeblendet.

**Hinweis:** Elemente innerhalb einer „klassischen“ Mbox (eine mit einer Target Classic-Kampagne erstellte mbox) können nicht mit dieser Option entfernt werden.

### Abschnitt erweitern

Wählen Sie das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element aus. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.

### Zum Link navigieren

Öffnet das Ziel dieses Links.

### Rückgängig/Wiederholen

Rückgängigmachen von Änderungen, die Sie während einer Bearbeitungssitzung an Ihren Aktivitäten vornehmen Sie können außerdem Änderungen wiederherstellen, die zuvor rückgängig gemacht wurden.

## Navigationselemente mithilfe des DOM-Pfades navigieren {#dom-path}

Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Wenn Sie auf ein Element klicken, wird der entsprechende DOM-Pfad unten auf der Seite angezeigt.

![DOM-Pfad](/help/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten zu verschieben, um das gewünschte Element auszuwählen.

Wenn Sie den Mauszeiger über den DOM-Pfad bewegen, markiert ein blaues Feld das entsprechende Element im VEC. Wenn Sie auf das Element klicken, markiert ein orangefarbenes Feld das Element und das VEC-Optionsmenü wird wie oben beschrieben angezeigt.

Mithilfe des DOM-Pfades können Sie mühelos zu jedem übergeordneten, geschlagenen oder untergeordneten Element innerhalb des VEC navigieren.

Die DOM-Pfad-Funktion ist auch verfügbar, wenn [Sie die Klick-Tracking einrichten](/help/c-activities/r-success-metrics/click-tracking.md).