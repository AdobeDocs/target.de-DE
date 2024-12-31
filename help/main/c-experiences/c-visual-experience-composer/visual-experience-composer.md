---
keywords: Visual Experience Composer;VEC;WYSIWYG
description: Lernen Sie die Grundlagen der Verwendung von Visual Experience Composer (VEC) in Adobe Target kennen. VEC ist ein WYSIWYG-Editor, mit dem Sie mühelos personalisierte Erlebnisse erstellen können.
title: Wie verwende ich Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
source-git-commit: 4abd24f63dd65e65a1d8b07647630eeb640e7a1d
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 73%

---

# Visual Experience Composer (VEC)

Informationen zur Verwendung des [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].

VEC ist eine Benutzeroberfläche von WYSIWYG, mit der Sie personalisierte Erlebnisse und Angebote im Kontext der Website einfach erstellen und testen können. Sie können Erlebnisse und Angebote für Targeting-Aktivitäten erstellen, indem Sie das Layout und den Inhalt einer Webseite (oder eines Angebots) oder einer mobilen Webseite per Drag &amp; Drop austauschen und verändern.

Der VEC ist eine der Hauptkomponenten von [!DNL Adobe Target]. Der VEC ermöglicht Marketingexperten und Designern, Inhalte über eine visuelle Benutzeroberfläche zu erstellen und zu ändern. Viele Entwurfsentscheidungen können getroffen werden, ohne den Code direkt bearbeiten zu müssen. Die Bearbeitung von HTML und JavaScript ist über die Bearbeitungsoptionen, die im Composer verfügbar sind, ebenfalls möglich.

Auf der Registerkarte Target **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** können Sie die standardmäßige Visual Experience Composer-URL eingeben.

![Standard-VEC-URL-Einstellungen](/help/main/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Diese URL legt fest, wo Sie beim Öffnen des VEC starten. Wenn Sie keine Standardeinstellung festlegen, wird Ihnen beim Öffnen des Editors eine leere Seite angezeigt. Sie können die URL dann festlegen.

>[!NOTE]
>
>In bestimmten Browsern, wie Firefox, kann die Anzeige der Seite im VEC blockiert sein, wenn die Seite gemischten Inhalt enthält (z. B. eine nicht sichere Seite auf einer sicheren Site). Wenn Ihre Seite nicht angezeigt wird, klicken Sie auf das Symbol neben der URL in der Browser-Adressleiste und klicken Sie auf **[!UICONTROL Disable protection on this page]**. Dieses Problem betrifft nicht die Anzeige Ihrer Seiten für Site-Besucher.

Inhalt in einem iframe auf der Seite kann nicht im VEC bearbeitet werden. Zum Bearbeiten von Inhalten in einem iFrame müssen Sie sicherstellen, dass das iFrame-Dokument für Target aktiviert wurde. Erst dann können Sie diese iFrame-URL im VEC laden.

Sie können die Dropdownmenüs oben auf der Seite verwenden, um zu sehen, wie die Seite für verschiedene Zielgruppen oder mit verschiedenen Erlebnissen erscheinen würde. Sie können einen Namen für jedes Erlebnis in der zweiten Dropdownliste angeben. Wenn Sie beispielsweise den Standort des Startseiten-Links in Ihrer Navigationsleiste testen möchten, können Sie einem Erlebnis, in dem der Startseiten-Link zuerst angezeigt wird, zum Beispiel die Bezeichnung „Startseiten-Link“ geben, um die Erlebnisse in der Liste leichter zu identifizieren.

>[!NOTE]
>
>Änderungen an den Strukturen einer Seite, die sich auf die Orte auswirken, welche in einer auf der Seite erstellten Aktivität verwendet werden, können Probleme bei der Bearbeitung des Erlebnisses verursachen. Wenn ein Ort außerhalb des VEC verändert wurde, ist Target möglicherweise nicht in der Lage, den Ort zu finden, dessen Inhalt verändert wurde.

Wenn Sie Ihren Mauszeiger auf der Seite bewegen, folgt dem Cursor ein kontextbezogenes Feld, das Elemente auf der Seite hervorhebt.

![VEC hervorgehoben](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Klicken Sie auf das **[!UICONTROL Overlays]**, um die Darstellung der Hervorhebung zu ändern. Sie können beispielsweise nur Bilder, Links, regionale Mboxes, Änderungen oder JavaScript hervorheben. Sie können die Farbe der Hervorhebung ändern. Sie können auch eine Hervorhebungsfarbe und die Art der Füllung, die zur Hervorhebung verschiedener Elementtypen verwendet wird, festlegen.

![Überlagerungseinstellungen ändern](/help/main/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Klicken Sie auf ein hervorgehobenes Element für ein Menü mit Optionen, die für diesen Elementtyp verfügbar sind. Sie können beispielsweise auf ein Bild klicken und **[!UICONTROL Edit > Text/HTML]** auswählen, um den Text zu ändern, oder auf eine Schaltfläche klicken und die Hintergrundfarbe ändern. Sie können die Schaltflächen oben links auf der Seite verwenden, um die Overlays ein- und auszuschalten.

Sie können auch auf **[!UICONTROL Browse]** klicken, dann zu einer Seite gehen, die auf der primären Seite verfügbar ist, z. B. eine Versandseite oder einen Warenkorb, und die Änderungen auf dieser Seite testen. Sie können auch auf Seitenelemente zugreifen, die verfügbar werden, wenn Sie den Mauszeiger darüber bewegen, wie zum Beispiel Flyout-Menüs und Minicarts. Wenn Sie mit dem Navigieren zur Seite fertig sind, klicken Sie auf **[!UICONTROL Compose]** , um das Erlebnis zu bearbeiten. Vielleicht möchten Sie zum Beispiel den Entwurf für ein Einkaufswagendropdown oder ein Bilderkarussell verändern.

>[!NOTE]
>
>Wenn der Hover-Status von JavaScript abhängt, stellen Sie sicher, dass **[!UICONTROL Disable JavaScript]** nicht ausgewählt ist. JavaScript muss aktiviert sein, um JavaScript-Elemente zu bearbeiten.

Weitere Informationen zu den verfügbaren Optionen in VEC finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

Sie können einige Änderungen auf einer Seite ausführen, während die Seite geladen wird (oder nachdem die Seite nicht geladen wurde), oder Sie können das Laden der Seite im VEC abbrechen. Weitere Informationen finden Sie unter:

* [Bearbeiten Sie eine Seite, während die Seite geladen wird oder nachdem sie nicht geladen werden kann](#loading)
* [Abbrechen des Seitenladevorgangs in VEC](#cancel-loading)

## Bearbeiten Sie eine Seite, während die Seite geladen wird oder nachdem sie nicht geladen werden kann {#loading}

Sie können viele Aktionen ausführen, bevor die Seite im VEC geladen wird, oder selbst dann, wenn die Seite nicht vollständig geladen werden kann (wenn beispielsweise benutzerdefinierter Code nicht mehr funktioniert).

Einige Gründe, aus denen Sie möglicherweise auf eine Seite zugreifen oder sie bearbeiten möchten, während sie innerhalb des VEC geladen wird bzw. nach dem gescheiterten Laden:

* Sie möchten eine einfache Änderung an einer Seite vornehmen, z. B. um benutzerdefinierten Code hinzuzufügen oder den Namen eines Erlebnisses zu ändern.
* Sie möchten vorhandene benutzerdefinierte Codes von einer Seite kopieren, die nicht mehr verfügbar ist.
* Sie wissen, dass eine Seite nicht im VEC geladen wird, aber Sie möchten trotzdem einfache Änderungen vornehmen.

Während die Seite geladen wird (oder nachdem sie nicht geladen werden kann), sind das Bedienfeld &quot;[!UICONTROL Experiences]&quot;, das Bedienfeld &quot;[!UICONTROL Modifications]&quot; und die Einstellungen oben im Erlebnis (Überlagerungen, Änderungen, Konfigurieren usw.) alle verfügbar.

Die folgende Abbildung zeigt, dass Sie benutzerdefinierten Code einfügen oder andere Aktionen ausführen können, während die Seite noch geladen wird:

![Seitenladevorgang](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Abbrechen des Seitenladevorgangs in VEC {#cancel-loading}

Sie können das Laden einer Seite innerhalb des VEC abbrechen, um die Bearbeitung der Aktivität zu entsperren, ohne warten zu müssen, bis die Seite geladen wird. Diese Funktion spart Zeit und hilft Ihnen, einfache Bearbeitungen vorzunehmen oder benutzerdefinierten Code effizienter einzufügen, ohne auf das Laden der Seite innerhalb des VEC zu warten.

Einige Gründe, weshalb Sie die Seitenladevorgänge im VEC abbrechen möchten:

* Sie möchten kleinere Änderungen an vorhandenen Änderungen vornehmen
* Sie möchten eine oder mehrere vorhandene Änderungen löschen
* Sie möchten benutzerdefinierten Code einfügen oder bearbeiten
* Sie haben versehentlich die falsche URL für die Seite eingegeben.
* Sie möchten JavaScript aktivieren oder deaktivieren, bevor Sie die Seite im VEC laden
* Sie möchten weitere Regeln für Vorlagetestkriterien zu den Seitenbereitstellungskriterien hinzufügen.
* Sie möchten den Global Enhanced Experience Composer (EEC) überschreiben, wenn eine Seite über das EEC oder nur über iframe geladen wird, was möglicherweise von Seite zu Seite unterschiedlich sein kann.

Nachdem Sie das Laden der Seite im VEC abgebrochen haben, können Sie in der Aktivität zwischen Erlebnissen wechseln, ohne darauf warten zu müssen, dass die Seite geladen wird. Um die Seite innerhalb des VEC erneut anzuzeigen, müssen Sie auf die Schaltfläche **[!UICONTROL Reload]** klicken.

>[!IMPORTANT]
>
>Beachten Sie, dass, wenn benutzerdefinierter Code oder Änderungen vorgenommen werden, durch die Entscheidung zum Abbrechen des Ladens innerhalb des VEC sichergestellt wird, dass Ihre Kodierung oder Änderungen ordnungsgemäß durchgeführt werden. Stellen Sie sicher, dass Sie eine ordnungsgemäße Qualitätssicherung durchführen, um sicherzustellen, dass Ihr benutzerdefinierter Code und alle anderen Änderungen wie erwartet bereitgestellt werden.

Um das Laden einer Seite innerhalb des VEC abzubrechen, klicken Sie während des Ladevorgangs der Seite auf die Schaltfläche **[!UICONTROL Cancel Loading]** . Die Seite wird für diese Aktivität während der aktuellen Bearbeitungssitzung im VEC nicht geladen.

![Schaltfläche „Ladevorgang abbrechen“](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Um mit der Verwaltung von Erlebnissen in der aktuellen Aktivität fortzufahren oder neue Änderungen hinzuzufügen, müssen Sie auf die Schaltfläche **[!UICONTROL Reload]** klicken.

![Schaltfläche „Neu laden“](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Visual Experience Composer (1 von 2) (7:17) ![Tutorial-Badge](/help/main/assets/tutorial.png)

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2 von 2) (7:29) ![Tutorial-Badge](/help/main/assets/tutorial.png)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Office Hours: Visual Experience Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video ist eine Aufzeichnung von „[Office Hours](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)“, einer Initiative der Adobe-Kundenunterstützung.

* So funktioniert der VEC
* So vermeiden Sie häufige Probleme mit dem VEC
* Workarounds für den VEC

>[!VIDEO](https://video.tv.adobe.com/v/20784/)
