---
keywords: Visual Experience Composer;vec;wysiwyg
description: Informationen zur Verwendung von Visual Experience Composer (VEC) in Adobe Target.
title: 'Visual Experience Composer (VEC) '
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 94%

---


# Visual Experience Composer (VEC) 

Informationen zur Verwendung des [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].

VEC ist eine WYSIWYG-Benutzeroberfläche, mit der Sie ganz einfach personalisierte Erlebnisse und Angebot im Site-Kontext erstellen und testen können. Sie können Erlebnisse und Angebote für Targeting-Aktivitäten erstellen, indem Sie das Layout und den Inhalt einer Webseite (oder eines Angebots) oder einer mobilen Webseite per Drag &amp; Drop austauschen und verändern.

Der VEC ist eine der Hauptkomponenten von [!DNL Adobe Target]. Der VEC ermöglicht Marketingexperten und Designern, Inhalte über eine visuelle Benutzeroberfläche zu erstellen und zu ändern. Viele Entwurfsentscheidungen können getroffen werden, ohne den Code direkt bearbeiten zu müssen. Die Bearbeitung von HTML und JavaScript ist über die Bearbeitungsoptionen, die im Composer verfügbar sind, ebenfalls möglich.

Auf der Registerkarte &quot;Zielgruppe **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**&quot;können Sie die Standard-URL von Visual Experience Composer eingeben.

![Standard-VEC-URL-Einstellungen](/help/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Diese URL legt fest, wo Sie beim Öffnen des VEC starten. Wenn Sie keine Standardeinstellung festlegen, wird Ihnen beim Öffnen des Editors eine leere Seite angezeigt. Sie können die URL dann festlegen.

>[!NOTE]
>
>In bestimmten Browsern, wie Firefox, kann die Anzeige der Seite im VEC blockiert sein, wenn die Seite gemischten Inhalt enthält (z. B. eine nicht sichere Seite auf einer sicheren Site). Wird die Seite nicht angezeigt, klicken Sie auf das Symbol neben der URL in der Browser-Adressleiste und wählen Sie **[!UICONTROL Schutz auf dieser Seite deaktivieren]**. Dieses Problem betrifft nicht die Anzeige Ihrer Seiten für Site-Besucher.

Inhalt in einem iframe auf der Seite kann nicht im VEC bearbeitet werden. Zum Bearbeiten von Inhalten in einem iFrame müssen Sie sicherstellen, dass das iFrame-Dokument für Target aktiviert wurde. Erst dann können Sie diese iFrame-URL im VEC laden.

Sie können die Dropdownmenüs oben auf der Seite verwenden, um zu sehen, wie die Seite für verschiedene Zielgruppen oder mit verschiedenen Erlebnissen erscheinen würde. Sie können einen Namen für jedes Erlebnis in der zweiten Dropdownliste angeben. Wenn Sie beispielsweise den Standort des Startseiten-Links in Ihrer Navigationsleiste testen möchten, können Sie einem Erlebnis, in dem der Startseiten-Link zuerst angezeigt wird, zum Beispiel die Bezeichnung „Startseiten-Link“ geben, um die Erlebnisse in der Liste leichter zu identifizieren.

>[!NOTE]
>
>Änderungen an den Strukturen einer Seite, die sich auf die Orte auswirken, welche in einer auf der Seite erstellten Aktivität verwendet werden, können Probleme bei der Bearbeitung des Erlebnisses verursachen. Wenn ein Ort außerhalb des VEC verändert wurde, ist Target möglicherweise nicht in der Lage, den Ort zu finden, dessen Inhalt verändert wurde.

Wenn Sie Ihren Mauszeiger auf der Seite bewegen, folgt dem Cursor ein kontextbezogenes Feld, das Elemente auf der Seite hervorhebt.

![VEC hervorgehoben](/help/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Klicken Sie auf das **[!UICONTROL Overlays]**-Symbol, um die Anzeigeart der Hervorhebung zu ändern. Sie können beispielsweise nur Bilder, Links, regionale Mboxes, Änderungen oder JavaScript hervorheben. Sie können die Farbe der Hervorhebung ändern. Sie können auch eine Hervorhebungsfarbe und die Art der Füllung, die zur Hervorhebung verschiedener Elementtypen verwendet wird, festlegen.

![Überlagerungseinstellungen ändern](/help/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Klicken Sie auf ein hervorgehobenes Element, um ein Menü mit für dieses Element verfügbaren Optionen anzuzeigen. Sie können beispielsweise auf ein Bild klicken und **[!UICONTROL Bearbeiten > Text/HTML]** auswählen, um den Text zu ändern, oder auf eine Schaltfläche klicken und die Hintergrundfarbe zu ändern. Sie können die Schaltflächen oben links auf der Seite verwenden, um die Overlays ein- und auszuschalten.

Sie können auch auf **[!UICONTROL Durchsuchen]** klicken und dann von der primären Seite, wie zum Beispiel einer Versandseite oder einem Einkaufswagen, zu einer verfügbaren Seite navigieren und Änderungen an dieser Seite testen. Sie können auch auf Seitenelemente zugreifen, die verfügbar werden, wenn Sie den Mauszeiger darüber bewegen, wie zum Beispiel Flyout-Menüs und Minicarts. Wenn Sie mit dem Durchsuchen der Seite fertig sind, klicken Sie auf **[!UICONTROL Erstellen]**, um das Erlebnis zu bearbeiten. Vielleicht möchten Sie zum Beispiel den Entwurf für ein Einkaufswagendropdown oder ein Bilderkarussell verändern.

>[!NOTE]
>
>Wenn ein Hover-Zustand von JavaScript abhängig ist, vergewissern Sie sich, dass **[!UICONTROL JavaScript deaktivieren]** nicht ausgewählt wurde. JavaScript muss aktiviert sein, um JavaScript-Elemente zu bearbeiten.

Weitere Informationen zu den verfügbaren Optionen in VEC finden Sie unter [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

Sie können einige Änderungen auf einer Seite ausführen, während die Seite geladen wird (oder nachdem die Seite nicht geladen wurde), oder Sie können das Laden der Seite im VEC abbrechen. Weitere Informationen finden Sie unter:

* [Bearbeiten einer Seite während der Ladezeit der Seite oder nachdem die Seite nicht geladen werden konnte](#loading)
* [Laden einer Seite im VEC abbrechen](#cancel-loading)

## Bearbeiten einer Seite während der Ladezeit der Seite oder nachdem die Seite nicht geladen werden konnte {#loading}

Sie können viele Aktionen ausführen, bevor die Seite im VEC geladen wird, oder selbst dann, wenn die Seite nicht vollständig geladen werden kann (wenn beispielsweise benutzerdefinierter Code nicht mehr funktioniert).

Einige Gründe, aus denen Sie möglicherweise auf eine Seite zugreifen oder sie bearbeiten möchten, während sie innerhalb des VEC geladen wird bzw. nach dem gescheiterten Laden:

* Sie möchten eine einfache Änderung an einer Seite vornehmen, z. B. um benutzerdefinierten Code hinzuzufügen oder den Namen eines Erlebnisses zu ändern.
* Sie möchten vorhandene benutzerdefinierte Codes von einer Seite kopieren, die nicht mehr verfügbar ist.
* Sie wissen, dass eine Seite nicht im VEC geladen wird, aber Sie möchten trotzdem einfache Änderungen vornehmen.

Während die Seite geladen wird (oder nachdem sie nicht geladen wurde), sind das Bedienfeld [!UICONTROL Erlebnisse], das Bedienfeld [!UICONTROL Änderungen] und die Einstellungen oben im Erlebnis (Überlagerungen, Änderungen, Konfigurationen usw.) alle barrierefrei zugänglich.

Die folgende Abbildung zeigt, dass Sie benutzerdefinierten Code einfügen oder andere Aktionen ausführen können, während die Seite noch geladen wird:

![Seitenladevorgang](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Laden einer Seite im VEC abbrechen {#cancel-loading}

Sie können das Laden einer Seite innerhalb des VEC abbrechen, um die Bearbeitung der Aktivität zu entsperren, ohne warten zu müssen, bis die Seite geladen wird. Diese Funktion spart Zeit und hilft Ihnen, einfache Bearbeitungen vorzunehmen oder benutzerdefinierten Code effizienter einzufügen, ohne auf das Laden der Seite innerhalb des VEC zu warten.

Einige Gründe, weshalb Sie die Seitenladevorgänge im VEC abbrechen möchten:

* Sie möchten kleinere Änderungen an vorhandenen Änderungen vornehmen
* Sie möchten eine oder mehrere vorhandene Änderungen löschen
* Sie möchten benutzerdefinierten Code einfügen oder bearbeiten
* Sie haben versehentlich die falsche URL für die Seite eingegeben.
* Sie möchten JavaScript aktivieren oder deaktivieren, bevor Sie die Seite im VEC laden
* Sie möchten weitere Regeln für Vorlagetestkriterien zu den Seitenbereitstellungskriterien hinzufügen.
* Sie möchten den Global Enhanced Experience Composer (EEC) überschreiben, wenn eine Seite über das EEC oder nur über iframe geladen wird, was möglicherweise von Seite zu Seite unterschiedlich sein kann.

Nachdem Sie das Laden der Seite im VEC abgebrochen haben, können Sie in der Aktivität zwischen Erlebnissen wechseln, ohne darauf warten zu müssen, dass die Seite geladen wird. Um die Seite erneut im VEC anzuzeigen, müssen Sie auf die Schaltfläche **[!UICONTROL Neu laden]** klicken.

>[!IMPORTANT]
>
>Beachten Sie, dass, wenn benutzerdefinierter Code oder Änderungen vorgenommen werden, durch die Entscheidung zum Abbrechen des Ladens innerhalb des VEC sichergestellt wird, dass Ihre Kodierung oder Änderungen ordnungsgemäß durchgeführt werden. Stellen Sie sicher, dass Sie eine ordnungsgemäße Qualitätssicherung durchführen, um sicherzustellen, dass Ihr benutzerdefinierter Code und alle anderen Änderungen wie erwartet bereitgestellt werden.

Um das Laden einer Seite im VEC abzubrechen, klicken Sie auf die Schaltfläche **[!UICONTROL Ladevorgang abbrechen]**, während die Seite geladen wird. Die Seite wird für diese Aktivität während der aktuellen Bearbeitungssitzung im VEC nicht geladen.

![Schaltfläche „Ladevorgang abbrechen“](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Um weiterhin Erlebnisse in der aktuellen Aktivität zu verwalten oder neue Änderungen hinzuzufügen, müssen Sie auf die Schaltfläche **[!UICONTROL Neu laden]** klicken.

![Schaltfläche „Neu laden“](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>Es gibt ein bekanntes Problem mit dieser Funktion, das in der nächsten Version behoben wird. Weitere Informationen finden Sie unter „Laden einer Seite im VEC abbrechen“ auf der Seite [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#cancel).

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Visual Experience Composer (1 von 2) (7:17) ![Tutorial badge](/help/assets/tutorial.png)

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2 von 2) (7:29) ![Tutorial badge](/help/assets/tutorial.png)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Bürozeiten: Visual Experience Composer ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video ist eine Aufzeichnung von „[Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)“, einer Initiative der Adobe-Kundenunterstützung.

* So funktioniert der VEC
* So vermeiden Sie häufige Probleme mit dem VEC
* Workarounds für den VEC

>[!VIDEO](https://video.tv.adobe.com/v/20784/)