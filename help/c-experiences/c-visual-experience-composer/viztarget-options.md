---
keywords: Optionen für den Visual Experience Composer;Optionen für den Erlebnissetzer;Erlebnisoptionen;Bearbeiten-HTML;Bearbeiten-Text/HTML;Bearbeiten-Hintergrundfarbe;Hintergrundfarbe;Einfügeelement;Verknüpfung;Verknüpfung;Visual Experience Composer-Verknüpfung;Bearbeiten-CSS-Klasse;CSS-Klasse;CSS-Klasse;Austausch-Angebot;Angebot-Swap;Bild-Swap;Element entfernen;Element ausblenden;Element ausblenden;Element ausblenden;Element ausblenden;Verschieben;Element zu diesem Link navigieren;Link navigieren;navigieren;navigieren;navigieren;navigieren;navigieren;navigieren;Verknüpfen;Verknüpfen;Rückgängig;Wiederholen;Rückgängig/Wiederholen;Benutzerdefinierte Ereignis;Webkomponenten
description: Entdecken Sie die Optionen in Adobe Targets Visual Experience Composer (VEC). Klicken Sie einfach auf ein Element, um zu sehen, welche Optionen für dieses Element verfügbar sind.
title: Wie verwende ich die VEC-Optionen (Visual Experience Composer)?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: 823694603c0248316e471f0b15070c0a34356620
workflow-type: tm+mt
source-wordcount: '2626'
ht-degree: 71%

---

# Visual Experience Composer-Optionen

Wenn Sie auf ein Seitenelement im [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC), zeigt ein Menü die Optionen an, die für diesen Elementtyp verfügbar sind. Darüber hinaus wird am unteren Rand der Seite ein DOM-Pfad angezeigt, mit dem Sie einfach durch die Seitenstruktur navigieren können.

## VEC-Optionen

Die verschiedenen Visual Experience Composer (VEC)-Aktionen sind in Menüs gruppiert, um Ihren Auftrag schneller und effizienter zu gestalten:

![VEC-Optionen-Menü](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Die verfügbaren Optionen hängen von dem Aktivitätstyp ab, den Sie bearbeiten.

### [!UICONTROL Bearbeiten ]

Die folgenden Optionen sind verfügbar:

#### [!UICONTROL Text/HTML] {#edit-text-html}

Ändern Sie den HTML-Code für das Element, etwa den Text für einen Textbereich, eine Schaltfläche oder einen Link.

Neben HTML-Code können Sie auch benutzerdefiniertes JavaScript bearbeiten und einfügen.

Beim Bearbeiten von Text und HTML für [!UICONTROL A/B]- und [!UICONTROL Erlebnisziel-Aktivitäten] stehen mehrere Rich-Text-Formatierungsoptionen zur Verfügung. Sie können eine Schriftart und einen Schriftstil auswählen, die Textausrichtung ändern und andere Standardformatierungsoptionen für Texte anwenden. Beim Ändern von HTML können Sie zwischen der Codeansicht und der Rich-Text-Bearbeitungsansicht der HTML umschalten.

Die folgenden HTML 5-Tags können verschachtelt sein:

| Tag | Zulässige verschachtelte Tags |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

#### [!UICONTROL Hintergrundfarbe]

Verwenden Sie den Farbwähler, um eine Hintergrundfarbe auszuwählen oder zu konfigurieren. Sie können ein Farbmuster auswählen und es mithilfe von RGB-Werten oder Farb-Hex-Codes anpassen. Das rote X im Farbwähler macht den Hintergrund transparent.

**Hinweis:** Diese Option ist nicht für Elemente verfügbar, wenn ein Hintergrundbild festgelegt ist.

#### [!UICONTROL Stile ] {#styles}

Verwenden Sie das Bedienfeld [!UICONTROL Stile], um den Wert vorhandener Stile für das ausgewählte Element anzuzeigen oder zu bearbeiten. Sie können auch zusätzliche Formatierungen hinzufügen.

So greifen Sie auf [!UICONTROL Stile] auf ein Seitenelement innerhalb des VEC klicken und dann auf **[!UICONTROL Bearbeiten]** > **[!UICONTROL Stile]**.

Das Bedienfeld [!UICONTROL Stile] wird rechts im VEC angezeigt. Das Bedienfeld enthält eine Liste der Stile, mit denen Sie das ausgewählte Element bearbeiten oder die Sie zum ausgewählten Element hinzufügen können. Mit einem Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie mit Cascading Style Sheets (CSS) gut vertraut sind oder Code von Ihrem Entwickler erhalten.

![Stile-Bedienfeld](/help/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Wenn Sie verschiedene Stile anwenden, können Sie Ihre Änderungen jederzeit rückgängig machen, indem Sie auf [!UICONTROL Zurücksetzen] Symbol, das in der oberen rechten Ecke der [!UICONTROL Stile] -Feld, nachdem Sie einen Bereich geändert haben. Klicken Sie auf [!UICONTROL Zurücksetzen] setzt alle Änderungen im Bedienfeld des aktuellen Bereichs zurück.

Erweitern Sie jeden Abschnitt, um Stile zu bearbeiten oder hinzuzufügen, wie unten beschrieben. Um Ihre Änderungen zu speichern, klicken Sie oben im Bedienfeld auf das Symbol „Zurück“, um zur Hauptanzeige des Bedienfelds zurückzukehren, und klicken Sie dann auf **[!UICONTROL Speichern]**.

Blaue Punkte im Hauptbereich und neben jeder Option in den verschiedenen Bereichsfenstern zeigen an, dass Sie die entsprechenden Stile geändert haben. Dieser visuelle Indikator erleichtert Ihnen die Überprüfung Ihrer Änderungen, bevor Sie auf [!UICONTROL Speichern].

>[!NOTE]
>
>Schnellaktionen für Layoutänderungen, Hintergrundfarbe, Größenanpassungen und Verschieben sind ebenfalls als separate Aktionen im VEC-Menü verfügbar. Diese Optionen können als separate Aktionen verwendet werden oder Sie können das Menü Stile verwenden, wie hier erklärt.

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

   Obwohl der Rich-Text-Editor (Text bearbeiten/HTML) zur Feinabstimmung verfügbar ist, stehen über diese Option Schnellaktionen zum Ändern des gesamten Elements zur Verfügung. Wenn Sie die Typografie-Bearbeitungen nur auf einen Teil des Textes anwenden möchten (nicht auf den ganzen Text), verwenden Sie den [Rich-Text-Editor](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   Sie können die folgenden Typografie-Stile bearbeiten:

   * [!UICONTROL Schriftgröße]
   * [!UICONTROL Schriftstärke]
   * [!UICONTROL Textformat]
   * [!UICONTROL Farbe] (geben Sie den Farbcode an oder verwenden Sie den Farbwähler)
   * [!UICONTROL Wortabstand]
   * [!UICONTROL Zeilenhöhe]
   * [!UICONTROL Textausrichtung]

* **[!UICONTROL Rand]**

   Ändern Sie den Rand für das ausgewählte Element. Sie können die linken, rechten, unteren und oberen Ränder ändern.

   Klicken Sie auf das Dropdownsymbol für jeden Rand, um unter den folgenden Optionen zu wählen:

   * [!UICONTROL Auto]
   * [!UICONTROL Wert] (Ziehen Sie den Schieberegler, um den Rand festzulegen oder die Anzahl der Pixel für jeden Rand festzulegen)

   Für den Rand werden positive und negative Werte unterstützt.

   Zielgruppe unterstützt auch andere Größen wie z.B. rem, pc, em. Weitere Informationen zu diesen Einheiten finden Sie unter [CSS-Tipps und Tricks für Web-Stylesheets](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Umrandung]**

   Ändern Sie die Umrandung für das ausgewählte Element. Sie können die linke, rechte, untere und obere Umrandung ändern.

   Ziehen Sie den Schieberegler, um die Umrandung festzulegen, oder legen Sie die Anzahl der Pixel für die Dicke der Umrandung fest.

   Umrandungsdicken von 0 aufwärts werden unterstützt.

   Zielgruppe unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html), wie z. B. rem, pc, em.

* **[!UICONTROL Rahmen]**

   Klicken Sie auf die Rahmensymbole oben im Bedienfeld, um den Rahmen des ausgewählten Elements zu ändern.

   Sie können die folgenden Stile für jeden Rahmen bearbeiten (oben, rechts, unten und links):

   * [!UICONTROL Rahmenstil] (keine, ausgeblendet, gepunktet, gestrichelt, ausgefüllt oder Dublette)
   * [!UICONTROL Rahmenfarbe] (geben Sie den Farbcode an oder verwenden Sie den Farbwähler)
   * [!UICONTROL Rahmenbreite] (Ziehen Sie den Schieberegler, um eine Randbreite auszuwählen oder die Breite in Pixel anzugeben)

   Rahmendicken von 0 aufwärts werden unterstützt.

   Zielgruppe unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html), wie z. B. rem, pc, em.

* **[!UICONTROL Position]**

   Verschieben Sie das ausgewählte Element von seiner aktuellen Position aus. Sie können die Elemente oben, unten, links, rechts und [Z-Index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) Position.

   Klicken Sie auf die Dropdownliste [!UICONTROL Statisch], um aus den folgenden Positionsoptionen auszuwählen:

   * [!UICONTROL Statisch]
   * [!UICONTROL Relativ]
   * [!UICONTROL Absolut      ]
   * [!UICONTROL Stickiness]
   * [!UICONTROL Fest]

   Klicken Sie auf das Dropdownsymbol für jede Position, um unter den folgenden Optionen auszuwählen:

   * [!UICONTROL Automatisch]
   * [!UICONTROL Wert] (Ziehen Sie den Schieberegler, um das Element zu positionieren, oder geben Sie die Anzahl der Pixel an, um das Element zu verschieben)

   Für die Position werden positive und negative Werte unterstützt.

   Zielgruppe unterstützt auch [andere Größeneinheiten](https://www.w3.org/Style/Examples/007/units.en.html), wie z. B. rem, pc, em.

* **[!UICONTROL Größe]**

   Ändern Sie die Breite und Höhe des ausgewählten Elements.

   Klicken Sie auf das Dropdownsymbol neben [!UICONTROL Breite] und [!UICONTROL Höhe], um unter den folgenden Optionen auszuwählen:

   * [!UICONTROL Automatisch]
   * [!UICONTROL Wert] (Ziehen Sie den Schieberegler, um das Element zu vergrößern, oder geben Sie die Anzahl der Pixel für jede Dimension an)

* **[!UICONTROL Filter]**

   Ziehen Sie den Schieberegler für jede Filteroption oder geben Sie den gewünschten Prozentsatz an:

   * [!UICONTROL Sepia]
   * [!UICONTROL Kontrast]
   * [!UICONTROL Helligkeit]
   * [!UICONTROL Graustufen]
   * [!UICONTROL Weichzeichnen]
   * [!UICONTROL Deckkraft]
   * [!UICONTROL Invertieren]
*
[!UICONTROL  Farbton rotieren]
   * [!UICONTROL Sättigung]

* **[!UICONTROL CSS-Editor]**

   Mit dem Echtzeit-CSS-Editor können Sie Änderungen anzeigen und Stile hinzufügen, wenn Sie mit Cascading Style Sheets (CSS) gut vertraut sind oder Code von Ihrem Entwickler erhalten.

   Im CSS-Editor werden alle Änderungen angezeigt, die Sie im Bedienfeld „Stile“ vornehmen. Wie in unten stehender Abbildung gezeigt wurden Schriftgröße, oberer Rand und Bildgröße geändert:

   ![CSS-Editor mit Änderungen](/help/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Beachten Sie die blauen Punkte neben den Optionen [!UICONTROL Typografie], [!UICONTROL Rand] und [!UICONTROL Größe] in der obigen Abbildung. Diese Punkte zeigen an, dass Sie diese Abschnitte geändert haben. Wenn Sie diese Abschnittsbedienfelder öffnen, werden neben den spezifischen Optionen, die Sie geändert haben, blaue Punkte angezeigt.

   Sie können Ihren eigenen Code eingeben, wenn der gewünschte Stil standardmäßig nicht in den [!UICONTROL Stilen] verfügbar ist.

   Im CSS-Editor werden nur Details zur aktuellen Sitzung angezeigt. Wenn Sie Änderungen speichern und den Editor dann erneut öffnen, werden Details zu Ihrer vorherigen Änderung nicht im Editor angezeigt, auch wenn Sie dasselbe Element erneut auswählen.

   >[!IMPORTANT]
   >
   >Sie können ein Hintergrundbild mithilfe des CSS-Editors anwenden, es kann jedoch zu Flackern führen. Testen Sie Ihre Änderungen vor der Implementierung.

#### [!UICONTROL CSS-Klasse]

Geben Sie die vordefinierte CSS-Klasse, die für das Element verwendet wurde, an. Wenn mehr als ein Element ausgewählt ist, trennen Sie mehrere CSS-Klassen durch ein Leerzeichen.

Verfügbar für Aktivitäten mit [!UICONTROL A/B], [!UICONTROL Automated Personalization] und [!UICONTROL Multivarianz-Tests].

#### [!UICONTROL Link]

Ändern Sie die URL im Link.

Verwenden Sie „Link bearbeiten“, um die Auswahl zu aktualisieren, damit auf dasselbe Bildelement gezeigt wird. Die Verlinkung zu einem anderen Bildelement wird jedoch nicht unterstützt. Um eine Verlinkung zu einem anderen Bildelement herzustellen, löschen Sie die ursprüngliche Aktion aus dem Code-Editor und verwenden Sie den [!UICONTROL Visual Experience Composer], um die Aktion auf das andere Bildelement anzuwenden.

### [!UICONTROL Einfügen vor]

Die folgenden Optionen sind verfügbar:

#### [!UICONTROL Bild], [!UICONTROL HTML]und [!UICONTROL Text]

Fügen Sie zusätzlich zur Bearbeitung von bestehendem Inhalt nun auch jede Art von Elementen zu Ihrer Seite hinzu. Fügen Sie Text, Code, Listen und mehr hinzu, um komplett unterschiedliche Erlebnisse zum Testen zu erstellen.

Wählen Sie ein Element auf der Seite aus, klicken Sie auf [!UICONTROL Einfügen vor] und wählen Sie aus, ob Sie ein Bild, HTML-Code oder Text einfügen möchten. Das eingefügte Element wird vor dem ausgewählten Element angezeigt.

Das Verhalten des eingefügten Elements hängt von der Struktur der Seite, Ihrem CSS und anderen Seitenkonfigurationsoptionen ab. Für eine korrekte Anzeige der Seite ist gültiges HTML erforderlich. Sie sollten Ihre Seite nach dem Einfügen eines Elements immer testen, um sicherzustellen, dass sie wie erwartet angezeigt wird.

[!UICONTROL Recommendations] unterstützt das [!UICONTROL Einfügen vor] Inhalten von DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:** Für das Einfügen eines Bildes muss [!DNL Adobe Scene7 Publishing System] aktiviert sein, damit Sie Zugriff auf die Bildbibliothek haben.

#### Empfehlung

Schließen Sie Empfehlungen in A/B-Test- (einschließlich automatischer Zuweisung und automatischem Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md).

#### [!UICONTROL Erlebnisfragment]

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### [!UICONTROL Einfügen nach]

Die folgenden Optionen sind verfügbar:

#### [!UICONTROL Bild], [!UICONTROL HTML]und [!UICONTROL Text]

Fügen Sie zusätzlich zur Bearbeitung von bestehendem Inhalt nun auch jede Art von Elementen zu Ihrer Seite hinzu. Fügen Sie Text, Code, Listen und mehr hinzu, um komplett unterschiedliche Erlebnisse zum Testen zu erstellen.

Wählen Sie ein Element auf der Seite aus, klicken Sie auf [!UICONTROL Einfügen nach] und wählen Sie aus, ob Sie ein Bild, HTML-Code oder Text einfügen möchten. Das eingefügte Element wird nach dem ausgewählten Element angezeigt.

Das Verhalten des eingefügten Elements hängt von der Struktur der Seite, Ihrem CSS und anderen Seitenkonfigurationsoptionen ab. Für eine korrekte Anzeige der Seite ist gültiges HTML erforderlich. Sie sollten Ihre Seite nach dem Einfügen eines Elements immer testen, um sicherzustellen, dass sie wie erwartet angezeigt wird.

[!UICONTROL Recommendations] unterstützt das [!UICONTROL Einfügen nach] nach DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:** Für das Einfügen eines Bildes muss [!DNL Adobe Scene7 Publishing System] aktiviert sein, damit Sie Zugriff auf die Bildbibliothek haben.

#### Empfehlung

Schließen Sie Empfehlungen in A/B-Test- (einschließlich automatischer Zuweisung und automatischem Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md).

#### [!UICONTROL Erlebnisfragment]

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### [!UICONTROL Ersetzen durch]

Die folgenden Optionen sind verfügbar:

#### [!UICONTROL Bild]

Wählen Sie ein anderes Bild aus der Inhaltsbibliothek. Die für den Tausch verfügbaren Bilder beinhalten auch Bilder, die in den Asset-Ordner von Experience Cloud oder in die Inhaltsbibliothek in Target hochgeladen wurden.

Bei der eigentlichen Erstellung der Aktivität ist die angezeigte URL nicht die für die Bereitstellung genutzte URL. Nach der Synchronisierung wird diese URL auf eine Produktions-URL für Scene7 aktualisiert.

Die ursprüngliche URL könnte beispielsweise wie folgt aussehen:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Nach Synchronisierung der Aktivität sieht die URL möglicherweise wie folgt aus:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations unterstützt „Ersetzen durch“ in DIV-, SECTION- und ARTICLE-Tags.

**Hinweis:** Für den Tausch von Bildern ist ein Adobe Scene7 Publishing System-Konto erforderlich.

#### [!UICONTROL HTML-Angebot]

Wählen Sie in der [!UICONTROL Inhaltsbibliothek] ein anderes Angebot aus.

**Hinweis:** HTML-Angebote werden auf [!DNL Target]-Servern gespeichert.

Ein HTML-Angebot kann bis zu 256 KB groß sein.

#### Empfehlung

Schließen Sie Empfehlungen in A/B-Test- (einschließlich automatischer Zuweisung und automatischem Targeting) und Erlebnis-Targeting-Aktivitäten (XT-Aktivitäten) ein. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md).

#### [!UICONTROL Erlebnisfragment]

Fügen Sie Erlebnisfragmente, die in [!DNL Adobe Experience Manager] (AEM) erstellt wurden, in [!DNL Target]-Aktivitäten ein, um eine Optimierung oder Personalisierung zu ermöglichen. Weitere Informationen finden Sie unter [AEM-Erlebnisfragmente](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### [!UICONTROL Layout]

Die folgenden Optionen sind verfügbar:

#### [!UICONTROL Neu anordnen]

Ziehen Sie das Element an einen anderen Ort innerhalb des gleichen übergeordneten Elements oder DIV. Andere Elemente wechseln den Standort, um für das neu angeordnete Element Platz zu schaffen.

**Hinweis:** Klick-Tracking kann für neu angeordnete Elemente nicht durchgeführt werden.

#### [!UICONTROL Größe ändern]

Ändern Sie die Größe eines Elements auf Ihrer Seite. Bei Auswahl von [!UICONTROL Größe ändern], wird in der rechten unteren Ecke des Elements ein Griff angezeigt, mit dem Sie die Ecke ziehen können, um die Größe zu ändern. Halten Sie die Umschalttaste gedrückt, um das Größenverhältnis beizubehalten.

**Hinweis:** Die Größe von Inline-Elementen kann nicht geändert werden.

#### [!UICONTROL Verschieben ] {#move}

Verschieben Sie Elemente auf Ihrer Seite. Im Gegensatz zu [!UICONTROL Elemente neu anordnen] werden bei der Option [!UICONTROL Verschieben] keine anderen Elemente verschoben, um Platz für das verschobene Element zu machen. Verwenden Sie die Pfeiltasten, um geringfügige Korrekturen vorzunehmen. (Geplante Erweiterung: Unterstützung, um sicherzustellen, dass verschobene Elemente nicht hinter anderen Elementen ausgeblendet werden.)

In bestimmten Situationen, z. B. wenn eine CSS-Beschränkung die Bindung eines Elements innerhalb des übergeordneten Elements erfordert, können Sie das Element nicht außerhalb des übergeordneten Elements verschieben. Elemente können nicht aus einem Container verschoben werden, der folgende CSS-Eigenschaft hat:`overflow: hidden`

#### [!UICONTROL Ausblenden]

Blenden Sie das Element aus. Der weiße Bereich bleibt bestehen, der Inhalt wird jedoch entfernt.

#### [!UICONTROL Entfernen]

Entfernen Sie das Element. Der weiße Bereich hinter dem Bild wird entfernt, und der Bereich, in dem sich das Element befand, wird ausgeblendet.

**Hinweis:** Elemente innerhalb einer „klassischen“ Mbox (eine mit einer Target Classic-Kampagne erstellte Mbox) können nicht mit dieser Option entfernt werden.

### [!UICONTROL Abschnitt erweitern]

Wählen Sie das übergeordnete Element zusätzlich zum ursprünglich ausgewählten Element aus. Wenn Sie ein übergeordnetes Element auswählen, werden alle untergeordneten Elemente dieses Elements automatisch ausgewählt. Sie können diese Auswahl mehrere Male erweitern.

### [!UICONTROL Gehen Sie zu dem Link]

Öffnen Sie das Ziel dieses Links.

### [!UICONTROL Rückgängig]/[!UICONTROL Wiederholen]

Rückgängigmachen von Änderungen, die Sie während einer Bearbeitungssitzung an Ihren Aktivitäten vornehmen Sie können außerdem Änderungen wiederherstellen, die zuvor rückgängig gemacht wurden.

## Zu beachten {#considerations}

* Weitere Informationen zu Angeboten mit HTML-Inhalten finden Sie unter „Darstellung von Angeboten mit HTML-Inhalten durch at.js“ in [Funktionsweise von „at.js“](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render).

## Unterstützung benutzerdefinierter Elemente (26. Oktober 2021) {#custom}

VEC unterstützt [Webkomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components) um personalisierte Erlebnisse und Angebot zu benutzerdefinierten Elementen und Elementen in benutzerdefinierten Elementen zu erstellen und zu testen. Diese Funktionalität ist im VEC für alle verfügbar. [!DNL Target] Aktivitäten.

>[!NOTE]
>
>VEC-Unterstützung für benutzerdefinierte Elemente wird unterstützt in [at.js-Version](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) 2.7.0 (oder neuer). Stellen Sie sicher, dass auf Ihrer Website die erforderliche Version bereitgestellt wurde. Wenn Sie die [Helferweiterung für Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)muss die erforderliche Version von at.js bereitgestellt werden. Die oben beschriebenen VEC-Optionen sind nicht sichtbar und stehen für die Verwendung mit nicht unterstützten Versionen von at.js zur Verfügung.
>
>Die VEC-Unterstützung für benutzerdefinierte Elemente wird derzeit nicht von der unterstützt. [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

Die meisten VEC-Aktionen werden auf benutzerdefinierten Ereignissen und in benutzerdefinierten Ereignissen unterstützt, mit folgenden Ausnahmen:

Folgende Aktionen sind für benutzerdefinierte Elemente nicht verfügbar:

* [!UICONTROL Bearbeiten ]
   * [!UICONTROL Text/HTML]
   * [!UICONTROL Link]
   * [!UICONTROL Quelle bearbeiten]

* [!UICONTROL Inhalt ersetzen]

Die folgende Aktion ist in benutzerdefinierten Elementen nicht verfügbar:

* [!UICONTROL Layout]
   * [!UICONTROL Neu anordnen]

## In Elementen mithilfe des DOM-Pfades navigieren {#dom-path}

Wenn Sie auf ein Element auf der Seite klicken, wird das VEC-Optionsmenü angezeigt. Zusätzlich wird, wenn Sie auf ein Element klicken, der entsprechende DOM-Pfad unten auf der Seite angezeigt.

![DOM-Pfad](/help/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Sie können den DOM-Pfad verwenden, um Informationen über das ausgewählte Element (Typ, ID und Klasse) schnell anzuzeigen und den DOM-Pfad nach oben oder unten verschieben, um das gewünschte Element auszuwählen.

Wenn Sie den Mauszeiger über den DOM-Pfad bewegen, markiert ein blaues Feld das entsprechende Element im VEC. Wenn Sie auf das Element klicken, markiert ein orangefarbenes Feld das Element und das VEC-Optionsmenü wird wie oben beschrieben angezeigt.

Mithilfe des DOM-Pfades können Sie mühelos zu jedem übergeordneten, parallelen oder untergeordneten Element innerhalb des VEC navigieren.

Die DOM-Pfad-Funktion ist auch verfügbar, wenn Sie das [Klick-Tracking](/help/c-activities/r-success-metrics/click-tracking.md) einrichten.
