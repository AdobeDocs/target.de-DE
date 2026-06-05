---
keywords: Visual Experience Composer-Optionen;Experience Composer-Optionen;Erlebnisoptionen;Text bearbeiten;HTML bearbeiten;Text/HTML bearbeiten;Hintergrundfarbe bearbeiten;Hintergrundfarbe;Element einfügen;Link bearbeiten;Visual Experience Composer-Link;CSS-Klasse bearbeiten;CSS-Klasse;CSS-Klasse;Angebot wechseln;Angebot vertauschen;Bild vertauschen;Bild vertauschen;Element entfernen;Element entfernen;Element ausblenden;Element neu anordnen;Element verschieben;Elementgröße ändern;Element vergrößern;Auswahl erweitern;zu diesem Link navigieren;Link navigieren;navigieren;Link navigieren;Link navigieren;Link;Rückgängig;Wiederholen;Wiederholen;benutzerspezifische Ereignisse;Ereignisse;Web-Komponenten;Angebot Entscheidung;Offer Decisioning
description: Erfahren Sie mehr über die im  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) verfügbaren Optionen.
title: Wie verwende ich die Optionen [!UICONTROL Visual Experience Composer] (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '2992'
ht-degree: 55%

---

# Visual Experience Composer-Optionen

Wenn Sie auf ein Seitenelement im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) klicken, werden in einem Menü die Optionen angezeigt, die für diesen Elementtyp verfügbar sind. Darüber hinaus wird am unteren Rand der Seite ein DOM-Pfad angezeigt, mit dem Sie einfach durch die Seitenstruktur navigieren können.

Die verschiedenen Aktionen [!UICONTROL Visual Experience Composer] (VEC) sind in entsprechenden Menüoptionen gruppiert, um Ihren Auftrag schneller und effizienter zu gestalten:

![VEC-Optionen-Menü](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Die verfügbaren Optionen hängen vom Aktivitätstyp ab, den Sie erstellen oder bearbeiten.

## [!UICONTROL Bearbeiten]

Die folgenden Optionen sind verfügbar:

### [!UICONTROL text/HTML] {#edit-text-html}

Ändern Sie den HTML-Code für das Element, etwa den Text für einen Textbereich, eine Schaltfläche oder einen Link.

Neben HTML-Code können Sie auch benutzerdefiniertes JavaScript bearbeiten und einfügen.

Beim Bearbeiten von Text und HTML stehen für A/B-Aktivitäten und [!UICONTROL Erlebnis]Targeting[!UICONTROL &#x200B; verschiedene &#x200B;] zur Rich-Text-Formatierung zur Verfügung. Sie können eine Schriftart und einen Schriftstil auswählen, die Textausrichtung ändern und andere Standardformatierungsoptionen für Texte anwenden. Beim Ändern von HTML können Sie zwischen der Codeansicht und der Rich-Text-Bearbeitungsansicht der HTML umschalten.

Die folgenden HTML 5-Tags können verschachtelt sein:

| Tag | Zulässige verschachtelte Tags |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

### [!UICONTROL Hintergrundfarbe]

Verwenden Sie den Farbwähler, um eine Hintergrundfarbe auszuwählen oder zu konfigurieren. Sie können ein Farbmuster auswählen und es mithilfe von RGB-Werten oder Farb-Hex-Codes anpassen. Das rote X im Farbwähler macht den Hintergrund transparent.

**Hinweis:** Diese Option ist nicht für Elemente verfügbar, wenn ein Hintergrundbild festgelegt ist.

### [!UICONTROL Stile] {#styles}

Verwenden Sie das [!UICONTROL Stile]-Bedienfeld, um den Wert vorhandener Stile für das ausgewählte Element anzuzeigen oder zu bearbeiten. Sie können auch zusätzliche Formatierungen hinzufügen.

Um auf das Bedienfeld [!UICONTROL Stile] zuzugreifen, klicken Sie im VEC auf ein Seitenelement und dann auf **[!UICONTROL Bearbeiten]** > **[!UICONTROL Stile]**.

Das [!UICONTROL Stile]-Bedienfeld wird auf der rechten Seite des VEC angezeigt. Das Bedienfeld enthält eine Liste der Stile, mit denen Sie das ausgewählte Element bearbeiten oder die Sie zum ausgewählten Element hinzufügen können. Mit einem Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie mit Cascading Style Sheets (CSS) gut vertraut sind oder Code von Ihrem Entwickler erhalten.

![Stile-Bedienfeld](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Wenn Sie verschiedene Stile anwenden, können Sie Ihre Änderungen jederzeit rückgängig machen, indem Sie auf das [!UICONTROL Wiederherstellen]-Symbol klicken, das oben rechts im Bedienfeld [!UICONTROL Stile] angezeigt wird, nachdem Sie einen beliebigen Abschnitt geändert haben. Durch Klicken auf [!UICONTROL Wiederherstellen]-Symbol werden alle Änderungen im Bedienfeld des aktuellen Abschnitts rückgängig gemacht.

Erweitern Sie jeden Abschnitt, um Stile zu bearbeiten oder hinzuzufügen, wie unten beschrieben. Um Ihre Änderungen zu speichern, klicken Sie auf das [!UICONTROL Zurück]-Symbol oben im Bedienfeld, um zur Hauptanzeige des Bedienfelds zurückzukehren, und klicken Sie dann auf **[!UICONTROL Speichern]**.

Blaue Punkte im Hauptbedienfeld und neben den einzelnen Optionen in den verschiedenen Bedienfeldern geben an, dass Sie die entsprechenden Stile geändert haben. Dieser visuelle Indikator erleichtert Ihnen die Überprüfung Ihrer Änderungen, bevor Sie auf &quot;[!UICONTROL &quot; &#x200B;].

>[!NOTE]
>
>Schnellaktionen für Layoutänderungen, Hintergrundfarbe, Größenanpassungen und Verschieben sind ebenfalls als separate Aktionen im VEC-Menü verfügbar. Diese Optionen können als separate Aktionen verwendet werden oder Sie können das Menü Stile verwenden, wie hier beschrieben.

* **[!UICONTROL Hintergrund]**

  Sie können die Hintergrundfarbe und das Bild ändern.

   * Farbe (geben Sie den Farbcode an oder verwenden Sie den Farbwähler)
   * Bild (wählen Sie ein Bild aus der Bildauswahl aus)
   * Bildquelle (geben Sie eine externe URL an)
   * Anhang
      * Klicken Sie auf die obere Dropdownliste, um einen Bildlauf, ein festes Layout oder „lokal“ auszuwählen.
      * Klicken Sie auf die untere Dropdownliste, um „Wiederholen“, „Wiederholung x“, „Wiederholung y, „Keine Wiederholung“, „Leerzeichen“ oder „Bildlauf“ auszuwählen.
   * Schneiden
      * Klicken Sie auf die obere Dropdownliste, um „Rahmen“, „Umrandung“, „Inhaltsfenster“ oder „Text“ auszuwählen.
      * Klicken Sie auf die untere Dropdownliste, um die automatische Audiowiedergabe oder Audiowiedergabe auszuwählen.

* **[!UICONTROL Typografie]**

  Ändern Sie die Typografie eines Elements. Die Bearbeitung der Typografie ist schnell und einfach.

  Obwohl der Rich-Text-Editor (Text bearbeiten/HTML) für die Feinabstimmung verfügbar ist, sind über diese Option Schnellaktionen zum Ändern des gesamten Elements verfügbar. Wenn Sie die Typografie-Bearbeitungen nur auf einen Teil des Textes anwenden möchten (nicht auf den ganzen Text), verwenden Sie den [Rich-Text-Editor](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

  Sie können die folgenden Typografie-Stile bearbeiten:

   * [!UICONTROL Schriftgröße]
   * [!UICONTROL Schriftstärke]
   * [!UICONTROL Schriftstil]
   * [!UICONTROL Farbe] (geben Sie den Farbcode an oder verwenden Sie die Farbauswahl)
   * [!UICONTROL Wortabstand]
   * [!UICONTROL Zeilenhöhe]
   * [!UICONTROL Textausrichtung]

* **[!UICONTROL Spanne]**

  Ändern Sie den Rand für das ausgewählte Element. Sie können die linken, rechten, unteren und oberen Ränder ändern.

  Klicken Sie auf das Dropdownsymbol für jeden Rand, um unter den folgenden Optionen zu wählen:

   * [!UICONTROL Auto]
   * [!UICONTROL Wert] (Ziehen Sie den Regler, um den Rand festzulegen, oder geben Sie die Anzahl der Pixel für jeden Rand an)

  Für den Rand werden positive und negative Werte unterstützt.

  Target unterstützt auch andere Größeneinheiten wie rem, pc, em. Weitere Informationen zu diesen Einheiten finden Sie unter [Web-Stylesheets - CSS-Tipps und -Tricks](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Abstand]**

  Ändern Sie die Umrandung für das ausgewählte Element. Sie können die linke, rechte, untere und obere Umrandung ändern.

  Ziehen Sie den Schieberegler, um die Umrandung festzulegen, oder legen Sie die Anzahl der Pixel für die Dicke der Umrandung fest.

  Umrandungsdicken von 0 aufwärts werden unterstützt.

  Target unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html) wie rem, pc, em.

* **[!UICONTROL Rahmen]**

  Klicken Sie auf die Rahmensymbole oben im Bedienfeld, um den Rahmen des ausgewählten Elements zu ändern.

  Sie können die folgenden Stile für jeden Rahmen bearbeiten (oben, rechts, unten und links):

   * [!UICONTROL Rahmenstil] (keine, ausgeblendet, gepunktet, gestrichelt, geschlossen oder doppelt)
   * [!UICONTROL Rahmenfarbe] (geben Sie den Farbcode an oder verwenden Sie die Farbauswahl)
   * [!UICONTROL Rahmenbreite] (Ziehen Sie den Regler, um eine Rahmenbreite auszuwählen, oder geben Sie die Breite in Pixel an)

  Rahmendicken von 0 aufwärts werden unterstützt.

  Target unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html) wie rem, pc, em.

* **[!UICONTROL Position]**

  Verschieben Sie das ausgewählte Element von seiner aktuellen Position aus. Sie können die Oben-, Unten-, Links-, Rechts- und [Z-Index) &#x200B;](https://www.w3schools.com/cssref/pr_pos_z-index.asp).

  Klicken Sie auf [!UICONTROL Statisch] Dropdown-Liste, um aus den folgenden Positionsoptionen auszuwählen:

   * [!UICONTROL static]
   * [!UICONTROL relativ]
   * [!UICONTROL absolut]
   * [!UICONTROL Sticky]
   * [!UICONTROL Behoben]

  Klicken Sie auf das Dropdownsymbol für jede Position, um unter den folgenden Optionen auszuwählen:

   * [!UICONTROL Auto]
   * [!UICONTROL Wert] (Ziehen Sie den Regler, um das Element zu positionieren, oder geben Sie die Anzahl der Pixel an, um die das Element verschoben werden soll)

  Für die Position werden positive und negative Werte unterstützt.

  Target unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html) wie rem, pc, em.

* **[!UICONTROL Größe]**

  Ändern Sie die Breite und Höhe des ausgewählten Elements.

  Klicken Sie auf das Dropdown-Symbol neben [!UICONTROL Breite] und [!UICONTROL Höhe], um eine der folgenden Optionen auszuwählen:

   * [!UICONTROL Auto]
   * [!UICONTROL Wert] (Ziehen Sie den Regler, um die Größe des Elements festzulegen, oder geben Sie die Anzahl der Pixel für jede Dimension an)

* **[!UICONTROL Filter]**

  Ziehen Sie den Schieberegler für jede Filteroption oder geben Sie den gewünschten Prozentsatz an:

   * [!UICONTROL Sepia]
   * [!UICONTROL Kontrast]
   * [!UICONTROL Helligkeit]
   * [!UICONTROL GrayScale]
   * [!UICONTROL ausgeblendet]
   * [!UICONTROL Deckkraft]
   * [!UICONTROL Umkehren]
*[!UICONTROL &#x200B; Farbton-Drehen]
   * [!UICONTROL Sättigen]

* **[!UICONTROL CSS-Editor]**

  Mit dem Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie mit Cascading Style Sheets (CSS) gut vertraut sind oder Code von Ihrem Entwickler erhalten.

  Im CSS-Editor werden alle Änderungen angezeigt, die Sie im Bedienfeld „Stile“ vornehmen. Wie in unten stehender Abbildung gezeigt wurden Schriftgröße, oberer Rand und Bildgröße geändert:

  ![CSS-Editor mit Änderungen](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  Beachten Sie die blauen Punkte neben den Optionen [!UICONTROL Typografie], [!UICONTROL Rahmen] und [!UICONTROL Größe] in der vorherigen Abbildung. Diese Punkte zeigen an, dass Sie diese Abschnitte geändert haben. Wenn Sie diese Abschnittsbedienfelder öffnen, werden neben den spezifischen Optionen, die Sie geändert haben, blaue Punkte angezeigt.

  Sie können Ihren eigenen Code eingeben, wenn Ihr gewünschter Stil in der Datei &quot;[!UICONTROL &quot; nicht standardmäßig verfügbar &#x200B;].

  Der CSS-Editor zeigt nur Details für die aktuelle Sitzung an. Wenn Sie Änderungen speichern und den Editor dann erneut öffnen, werden Details zu Ihrer vorherigen Änderung nicht im Editor angezeigt, auch wenn Sie dasselbe Element erneut auswählen.

  >[!IMPORTANT]
  >
  >Sie können ein Hintergrundbild mithilfe des CSS-Editors anwenden, es kann jedoch zu Flackern führen. Testen Sie Ihre Änderungen vor der Bereitstellung.

### [!UICONTROL CSS-Klasse]

Geben Sie die vordefinierte CSS-Klasse, die für das Element verwendet wurde, an. Wenn mehr als ein Element ausgewählt ist, trennen Sie mehrere CSS-Klassen durch ein Leerzeichen.

Verfügbar für [!UICONTROL A/B]-, [!UICONTROL Automated Personalization]- und [!UICONTROL Multivarianz-].

### [!UICONTROL link]

Ändern Sie die URL im Link.

Verwenden Sie „Link bearbeiten“, um die Auswahl zu aktualisieren, damit auf dasselbe Bildelement gezeigt wird. Die Verlinkung zu einem anderen Bildelement wird jedoch nicht unterstützt. Um eine Verlinkung zu einem anderen Bildelement herzustellen, löschen Sie die ursprüngliche Aktion aus dem Code-Editor und verwenden Sie den [!UICONTROL Visual Experience Composer], um die Aktion auf das andere Bildelement anzuwenden.

## [!UICONTROL Einfügen vor]

Die folgenden Optionen sind verfügbar:

### [!UICONTROL Angebotsentscheidung]

Fügen Sie ein [Angebot erstellt in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=de){target=_blank} hinzu, um Ihren Kunden mithilfe von Offer Decisioning das beste Angebot und Erlebnis zu bieten.

**Hinweis:** Diese Option ist nur beim Bearbeiten oder Erstellen [[!UICONTROL &#x200B; manuellen A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types)Tests oder [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) verfügbar. Diese Option steht für andere Aktivitätstypen nicht zur Verfügung.

Weitere Informationen finden Sie unter [Verwenden von Angebotsentscheidungen](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML] und [!UICONTROL Text]

Fügen Sie zusätzlich zur Bearbeitung von bestehendem Inhalt nun auch jede Art von Elementen zu Ihrer Seite hinzu. Fügen Sie Text, Code, Listen und mehr hinzu, um komplett unterschiedliche Erlebnisse zum Testen zu erstellen.

Wählen Sie ein Element auf der Seite aus, klicken Sie auf [!UICONTROL Einfügen vor] und wählen Sie aus, ob Sie ein Bild, HTML-Code oder Text einfügen möchten. Das eingefügte Element wird vor dem ausgewählten Element angezeigt.

Das Verhalten des eingefügten Elements hängt von der Struktur der Seite, Ihrem CSS und anderen Seitenkonfigurationsoptionen ab. Für eine korrekte Anzeige der Seite ist gültiges HTML erforderlich. Sie sollten Ihre Seite nach dem Einfügen eines Elements immer testen, um sicherzustellen, dass sie wie erwartet angezeigt wird.

[!UICONTROL Recommendations] unterstützt [!UICONTROL Einfügen vor] den Inhalt von DIV-, ABSCHNITT- und ARTIKEL-Tags.

**Hinweis:** Für das Einfügen eines Bildes muss [!DNL Adobe Scene7 Publishing System] aktiviert sein, damit Sie Zugriff auf die Bildbibliothek haben.

### Empfehlung

Schließen Sie Empfehlungen in A/B-Test- (einschließlich automatischer Zuweisung und automatischem Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Einfügen nach]

Die folgenden Optionen sind verfügbar:

### [!UICONTROL Angebotsentscheidung]

Fügen Sie ein [Angebot erstellt in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=de){target=_blank} hinzu, um Ihren Kunden mithilfe von Offer Decisioning das beste Angebot und Erlebnis zu bieten.

**Hinweis:** Diese Option ist nur beim Bearbeiten oder Erstellen [[!UICONTROL &#x200B; manuellen A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types)Tests oder [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) verfügbar. Diese Option steht für andere Aktivitätstypen nicht zur Verfügung.

Weitere Informationen finden Sie unter [Verwenden von Angebotsentscheidungen](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML] und [!UICONTROL Text]

Fügen Sie zusätzlich zur Bearbeitung von bestehendem Inhalt nun auch jede Art von Elementen zu Ihrer Seite hinzu. Fügen Sie Text, Code, Listen und mehr hinzu, um komplett unterschiedliche Erlebnisse zum Testen zu erstellen.

Wählen Sie ein Element auf der Seite aus, klicken Sie auf [!UICONTROL Einfügen nach] und wählen Sie aus, ob Sie ein Bild, HTML-Code oder Text einfügen möchten. Das eingefügte Element wird nach dem ausgewählten Element angezeigt.

Das Verhalten des eingefügten Elements hängt von der Struktur der Seite, Ihrem CSS und anderen Seitenkonfigurationsoptionen ab. Für eine korrekte Anzeige der Seite ist gültiges HTML erforderlich. Sie sollten Ihre Seite nach dem Einfügen eines Elements immer testen, um sicherzustellen, dass sie wie erwartet angezeigt wird.

[!UICONTROL Recommendations] unterstützt [!UICONTROL Einfügen nach] den Inhalt von DIV-, ABSCHNITT- und ARTIKEL-Tags.

**Hinweis:** Für das Einfügen eines Bildes muss [!DNL Adobe Scene7 Publishing System] aktiviert sein, damit Sie Zugriff auf die Bildbibliothek haben.

### Empfehlung

Schließen Sie Empfehlungen in A/B-Test- (einschließlich automatischer Zuweisung und automatischem Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Inhalt ersetzen]

Die folgenden Optionen sind verfügbar:

### [!UICONTROL Angebotsentscheidung]

Fügen Sie ein [Angebot erstellt in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=de){target=_blank} hinzu, um Ihren Kunden mithilfe von Offer Decisioning das beste Angebot und Erlebnis zu bieten.

**Hinweis:** Diese Option ist nur beim Bearbeiten oder Erstellen [[!UICONTROL &#x200B; manuellen A/B]](/help/main/c-activities/t-test-ab/test-ab.md#types)Tests oder [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) verfügbar. Diese Option steht für andere Aktivitätstypen nicht zur Verfügung.

Weitere Informationen finden Sie unter [Verwenden von Angebotsentscheidungen](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Bild]

Wählen Sie ein anderes Bild aus der Inhaltsbibliothek. Die für den Tausch verfügbaren Bilder beinhalten auch Bilder, die in den Asset-Ordner von Experience Cloud oder in die Inhaltsbibliothek in Target hochgeladen wurden.

Bei der eigentlichen Erstellung der Aktivität ist die angezeigte URL nicht die für die Bereitstellung genutzte URL. Nach der Synchronisierung wird diese URL auf eine Produktions-URL für Scene7 aktualisiert.

Die ursprüngliche URL könnte beispielsweise wie folgt aussehen:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Nach Synchronisierung der Aktivität sieht die URL möglicherweise wie folgt aus:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations unterstützt „Ersetzen durch“ in DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:** Für den Tausch von Bildern ist ein Adobe Scene7 Publishing System-Konto erforderlich.

### [!UICONTROL HTML-Angebot]

Wählen Sie ein anderes Angebot aus der [!UICONTROL Inhaltsbibliothek].

**Hinweis:** HTML-Angebote werden auf [!DNL Target]-Servern gespeichert.

Ein HTML-Angebot kann bis zu 256 KB groß sein.

### Empfehlung

Schließen Sie Empfehlungen in A/B-Test- (einschließlich automatischer Zuweisung und automatischem Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Layout]

Die folgenden Optionen sind verfügbar:

### [!UICONTROL Neu anordnen]

Ziehen Sie das Element an einen anderen Ort innerhalb des gleichen übergeordneten Elements oder DIV. Andere Elemente wechseln den Standort, um für das neu angeordnete Element Platz zu schaffen.

**Hinweis**: Das Klick-Tracking funktioniert nicht bei neu angeordneten Elementen.

Derzeit gehen bestimmte VEC-Aktionen, wie [!UICONTROL Neu anordnen] und [!UICONTROL Verschieben], davon aus, dass die gleichrangigen Elemente der übergeordneten Quell- und Ziel-Elemente vollständig geladen sind. Wenn verzögertes Laden unter den übergeordneten DOM-Elementen (Quelle oder Ziel) auftritt, können diese VEC-Aktionen zu inkonsistentem Verhalten führen. Wir arbeiten an einem zuverlässigeren Ansatz, damit VEC-Aktionen in verzögert geladenen DOM-Elementen funktionieren. Als temporäre Problemumgehung können Sie in [!UICONTROL &#x200B; Szenarien „benutzerdefinierten Code] verwenden, um Ihre Erlebnisse zu rendern.

### [!UICONTROL Größe ändern]

Ändern Sie die Größe eines Elements auf Ihrer Seite. Wenn Sie [!UICONTROL Größe ändern] auswählen, wird in der rechten unteren Ecke des Elements ein Ziehgriff angezeigt, mit dem Sie die Größe dieser Ecke ändern können. Halten Sie die Umschalttaste gedrückt, um das Größenverhältnis beizubehalten.

**Hinweis:** Die Größe von Inline-Elementen kann nicht geändert werden.

### [!UICONTROL Verschieben] {#move}

Verschieben Sie Elemente auf Ihrer Seite. Im Gegensatz zu [!UICONTROL Elemente neu anordnen] werden bei der Option [!UICONTROL Verschieben] keine anderen Elemente verschoben, um Platz für das verschobene Element zu machen. Verwenden Sie die Pfeiltasten, um geringfügige Korrekturen vorzunehmen. (Geplante Verbesserung: Unterstützung, um sicherzustellen, dass verschobene Elemente nicht hinter anderen Elementen versteckt werden.)

In bestimmten Situationen, z. B. wenn eine CSS-Einschränkung erfordert, dass ein Element innerhalb seines übergeordneten Elements bleibt, können Sie das Element nicht aus seinem übergeordneten Element verschieben. Elemente können nicht aus einem Container verschoben werden, der folgende CSS-Eigenschaft hat:`overflow: hidden`

Weitere Informationen [!UICONTROL &#x200B; inkonsistentem Verhalten bei den Aktionen [!UICONTROL Verschieben] und [!UICONTROL Neu anordnen] aufgrund des verzögerten Ladens von DOM-Elementen finden Sie oben unter &#x200B;]Neu anordnen .

### [!UICONTROL Ausblenden]

Blenden Sie das Element aus. Der weiße Bereich bleibt bestehen, der Inhalt wird jedoch entfernt.

### [!UICONTROL Entfernen]

Entfernen Sie das Element. Der weiße Bereich hinter dem Bild wird entfernt, und der Bereich, in dem sich das Element befand, wird ausgeblendet.

**Hinweis:** Elemente innerhalb einer „klassischen“ Mbox (eine mit einer Target Classic-Kampagne erstellte Mbox) können nicht mit dieser Option entfernt werden.

## [!UICONTROL Abschnitt erweitern]

Wählen Sie das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element aus. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.

## [!UICONTROL Navigieren Sie zu Link]

Öffnen Sie das Ziel dieses Links.

## [!UICONTROL Rückgängig]/[!UICONTROL Wiederholen]

Rückgängigmachen von Änderungen, die Sie während einer Bearbeitungssitzung an Ihren Aktivitäten vornehmen Sie können außerdem Änderungen wiederherstellen, die zuvor rückgängig gemacht wurden.

## Zu beachten {#considerations}

* Weitere Informationen zu Angeboten mit HTML-Inhalten finden Sie unter „Darstellung von Angeboten mit HTML-Inhalten durch at.js“ in [Funktionsweise von „at.js“](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=de){target=_blank}.

## Unterstützung benutzerdefinierter Elemente {#custom}

VEC unterstützt [Web-Komponenten](https://developer.mozilla.org/de/docs/Web/Web_Components) damit Sie personalisierte Erlebnisse und Angebote für benutzerdefinierte Elemente und Elemente innerhalb benutzerdefinierter Elemente erstellen und testen können. Diese Funktion ist in Visual Experience Composer für alle [!DNL Target] Aktivitätstypen verfügbar.

>[!NOTE]
>
>VEC-Unterstützung für benutzerdefinierte Elemente wird in [at.js-Version](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} 2.7.0 (oder höher) {target=_blank}. Stellen Sie sicher, dass auf Ihrer Website die erforderliche Version bereitgestellt ist. Wenn Sie die [Visual Experience Composer Helper-Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) verwenden, muss auch die erforderliche Version von at.js bereitgestellt sein. Die oben beschriebenen VEC-Optionen sind nicht sichtbar und können nicht mit nicht unterstützten Versionen von at.js verwendet werden.
>
>VEC-Unterstützung für benutzerdefinierte Elemente wird derzeit nicht mit dem [Adobe Experience Platform Web SDK unterstützt](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

Die meisten VEC-Aktionen werden für benutzerdefinierte Ereignisse und innerhalb von benutzerdefinierten Ereignissen unterstützt, mit den folgenden Ausnahmen:

Die folgenden Aktionen sind für benutzerdefinierte Elemente nicht verfügbar:

* [!UICONTROL Bearbeiten]
   * [!UICONTROL text/HTML]
   * [!UICONTROL link]
   * [!UICONTROL Source bearbeiten]

* [!UICONTROL Inhalt ersetzen]

Die folgende Aktion ist nicht in benutzerdefinierten Elementen verfügbar:

* [!UICONTROL Layout]
   * [!UICONTROL Neu anordnen]

## Navigieren in Elementen mithilfe des DOM-Pfads {#dom-path}

Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Zusätzlich wird, wenn Sie auf ein Element klicken, der entsprechende DOM-Pfad unten auf der Seite angezeigt.

![DOM-Pfad](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten verschieben, um das gewünschte Element auszuwählen.

Wenn Sie den Mauszeiger über den DOM-Pfad bewegen, markiert ein blaues Feld das entsprechende Element im VEC. Wenn Sie auf das Element klicken, markiert ein orangefarbenes Feld das Element und das VEC-Optionsmenü wird wie oben beschrieben angezeigt.

Mithilfe des DOM-Pfades können Sie mühelos zu jedem übergeordneten, parallelen oder untergeordneten Element innerhalb des VEC navigieren.

Die DOM-Pfad-Funktion ist auch verfügbar, wenn Sie das [Klick-Tracking](/help/main/c-activities/r-success-metrics/click-tracking.md) einrichten.
