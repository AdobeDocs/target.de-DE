---
description: Informationen zur Verwendung von Visual Experience Composer (VEC).
seo-description: Informationen zur Verwendung von Visual Experience Composer (VEC) in Adobe Target.
seo-title: Adobe Target Visual Experience Composer (VEC)
title: Visual Experience Composer (VEC)
uuid: f1e6f67e-1d7e-4806-8389-2ce165b534b4
translation-type: tm+mt
source-git-commit: f59e96cd5afcae9d27d730aecead9eb360f04026

---


# Visual Experience Composer (VEC){#visual-experience-composer-vec}

Informationen zur Verwendung von Visual Experience Composer (VEC).

Der VEC ist eine der Hauptkomponenten von [!DNL Adobe Target]. VEC ist ein Editor, mit dem Marketingexperten und Designer Inhalte mithilfe einer visuellen Benutzeroberfläche erstellen und ändern können. Viele Entwurfsentscheidungen können getroffen werden, ohne den Code direkt bearbeiten zu müssen. Die Bearbeitung von HTML und JavaScript ist über die Bearbeitungsoptionen, die im Composer verfügbar sind, ebenfalls möglich.

Auf der Registerkarte **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Voreinstellungen]** von Target können Sie die Standard-URL von Visual Experience Composer eingeben.

![Standard-VEC-URL-Einstellungen](/help/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Diese URL legt fest, wo Sie beginnen, wenn Sie VEC öffnen. Wenn Sie keine Standardeinstellung festlegen, wird Ihnen beim Öffnen des Editors eine leere Seite angezeigt. Sie können die URL dann festlegen.

>[!NOTE]
>
>Bestimmte Browser wie Firefox blockieren möglicherweise die Anzeige einer Seite im VEC, wenn die Seite gemischten Inhalt enthält (z. B. eine nicht sichere Seite auf einer sicheren Site). Wenn Ihre Seite nicht angezeigt wird, klicken Sie auf das Symbol neben der URL in der Browser-Adressleiste und klicken **[!UICONTROL Sie auf Schutz auf dieser Seite deaktivieren]**. Dieses Problem betrifft nicht die Anzeige Ihrer Seiten für Site-Besucher.

Inhalte innerhalb eines iframe auf der Seite können nicht im VEC geändert werden. Um Inhalte in einem iframe zu bearbeiten, stellen Sie sicher, dass das iframe-Dokument auf Target-aktiviert ist, und laden Sie dann diese iframe-URL in VEC.

Sie können die Dropdownmenüs oben auf der Seite verwenden, um zu sehen, wie die Seite für verschiedene Zielgruppen oder mit verschiedenen Erlebnissen erscheinen würde. Sie können einen Namen für jedes Erlebnis in der zweiten Dropdownliste angeben. Wenn Sie beispielsweise den Standort des Startseiten-Links in Ihrer Navigationsleiste testen möchten, können Sie einem Erlebnis, in dem der Startseiten-Link zuerst angezeigt wird, zum Beispiel die Bezeichnung „Startseiten-Link“ geben, um die Erlebnisse in der Liste leichter zu identifizieren.

>[!NOTE]
>
>Änderungen an den Strukturen einer Seite, die sich auf die Orte auswirken, welche in einer auf der Seite erstellten Aktivität verwendet werden, können Probleme bei der Bearbeitung des Erlebnisses verursachen. Wenn ein Ort außerhalb des VEC geändert wurde, kann Target den Ort, an dem der Inhalt geändert wurde, nicht finden.

Wenn Sie Ihren Mauszeiger auf der Seite bewegen, folgt dem Cursor ein kontextbezogenes Feld, das Elemente auf der Seite hervorhebt.

![VEC hervorgehoben](/help/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Klicken Sie auf das **[!UICONTROL Overlays]** -Symbol, um die Darstellung der Hervorhebung zu ändern. Sie können beispielsweise nur Bilder, Links, regionale mboxes, Änderungen oder javascript hervorheben. Sie können die Farbe der Hervorhebung ändern. Sie können auch eine Hervorhebungsfarbe und die Art der Füllung, die zur Hervorhebung verschiedener Elementtypen verwendet wird, festlegen.

![Überlagerungseinstellungen ändern](/help/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Klicken Sie auf ein hervorgehobenes Element, um ein Menü mit Optionen für diesen Elementtyp aufzurufen. Klicken Sie zum Beispiel auf ein Bild und wählen **[!UICONTROL Sie Bearbeiten &gt; Text/HTML]** , um den Text zu ändern, oder klicken Sie auf eine Schaltfläche und ändern Sie die Hintergrundfarbe. Sie können die Schaltflächen oben links auf der Seite verwenden, um die Overlays ein- und auszuschalten.

Sie können auch auf **[!UICONTROL Durchsuchen]** klicken und dann von der primären Seite, wie zum Beispiel einer Versandseite oder einem Einkaufswagen, zu einer verfügbaren Seite navigieren und Änderungen an dieser Seite testen. Sie können auch auf Seitenelemente zugreifen, die verfügbar werden, wenn Sie den Mauszeiger darüber bewegen, wie zum Beispiel Flyout-Menüs und Minicarts. Wenn Sie mit dem Durchsuchen der Seite fertig sind, klicken Sie auf **[!UICONTROL Erstellen], um das Erlebnis zu bearbeiten.** Vielleicht möchten Sie zum Beispiel den Entwurf für ein Einkaufswagendropdown oder ein Bilderkarussell verändern.

>[!NOTE]
>
>Wenn ein Hover-Zustand von JavaScript abhängig ist, vergewissern Sie sich, dass **[!UICONTROL JavaScript deaktivieren]** nicht ausgewählt wurde. JavaScript muss aktiviert sein, um JavaScript-Elemente zu bearbeiten.

Weitere Informationen zu den im VEC verfügbaren Optionen finden Sie [unter Visual Experience Composer-Optionen](../../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

Sie können einige Änderungen auf einer Seite ausführen, während die Seite geladen wird (oder nachdem die Seite nicht geladen wurde), oder Sie können das Laden der Seite im VEC abbrechen. Weitere Informationen finden Sie unter:

* [Bearbeiten einer Seite während der Ladezeit der Seite oder nach dem Laden der Seite](#loading)
* [Laden einer Seite im VEC abbrechen](#cancel-loading)

## Bearbeiten einer Seite während der Ladezeit der Seite oder nach dem Laden der Seite {#loading}

Sie können viele Aktionen ausführen, bevor die Seite im VEC geladen wird, oder selbst dann, wenn die Seite nicht vollständig geladen werden kann (wenn beispielsweise benutzerdefinierter Code nicht mehr funktioniert).

Einige Gründe, aus denen Sie möglicherweise auf eine Seite zugreifen oder sie bearbeiten möchten, während sie innerhalb des VEC oder nach der Ladung geladen wird:

* Sie möchten eine einfache Änderung an einer Seite vornehmen, z. B. um benutzerdefinierten Code hinzuzufügen oder den Namen eines Erlebnisses zu ändern.
* Sie möchten vorhandene benutzerdefinierten Code von einer Seite kopieren, die nicht mehr verfügbar ist.
* Sie wissen, dass eine Seite nicht im VEC geladen wird, aber Sie möchten trotzdem einfache Änderungen vornehmen.

Während die Seite geladen wird (oder nachdem sie nicht geladen wurde), sind das [!UICONTROL Bedienfeld &quot;Erlebnisse] &quot; , [!UICONTROL das Bedienfeld&quot; Änderungen&quot;] und die Einstellungen oben im Erlebnis (Überlagerungen, Änderungen, Konfigurationen usw.) barrierefrei zugänglich.

Die folgende Abbildung zeigt, dass Sie benutzerdefinierter Code einfügen oder andere Aktionen ausführen können, während die Seite noch geladen wird:

![Seitenladevorgang](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Laden einer Seite im VEC abbrechen {#cancel-loading}

Sie können das Laden einer Seite innerhalb des VEC abbrechen, um die Bearbeitung der Aktivität zu entsperren, ohne warten zu müssen, bis die Seite geladen wird. Diese Funktion spart Zeit und hilft Ihnen, einfache Bearbeitungen vorzunehmen oder benutzerdefinierten Code effizienter einzufügen, ohne auf die Seite innerhalb des VEC zu warten.

Einige Gründe, weshalb Sie die Seitenladevorgänge im VEC abbrechen möchten, umfassen:

* Sie möchten kleinere Änderungen an vorhandenen Änderungen vornehmen
* Sie möchten eine oder mehrere vorhandene Änderungen löschen
* Sie möchten benutzerdefinierten Code einfügen oder bearbeiten
* Sie haben versehentlich die falsche URL für die Seite eingegeben.
* Sie möchten javascript aktivieren oder deaktivieren, bevor Sie die Seite im VEC laden
* Sie möchten den Seitenbereitstellungskriterien weitere Vorlagentestregeln hinzufügen.
* Sie möchten den Global Enhanced Experience Composer (EEC) überschreiben, wenn eine Seite über das EEC oder nur iframe geladen wird, möglicherweise kann sich die Seite auf die Seite auswirken.

Nachdem Sie das Laden der Seite im VEC abgebrochen haben, können Sie in der Aktivität zwischen Erlebnissen wechseln, ohne darauf warten zu müssen, dass die Seite geladen wird. Um die Seite erneut in VEC anzuzeigen, müssen Sie auf **[!UICONTOL die Schaltfläche &quot;Neu laden]** &quot; klicken.

>[!IMPORTANT]
>
>Beachten Sie, dass, wenn benutzerdefinierter Code oder Änderungen vorgenommen werden, durch die Entscheidung zum Abbrechen des Ladens innerhalb des VEC sichergestellt wird, dass Ihre Kodierung oder Änderungen ordnungsgemäß durchgeführt werden. Stellen Sie sicher, dass Sie eine ordnungsgemäße Qualitätssicherung durchführen, um sicherzustellen, dass Ihr benutzerdefinierter Code und alle anderen Änderungen wie erwartet bereitgestellt werden.

Um das Laden einer Seite im VEC abzubrechen, klicken Sie auf **[!UICONTROL die]** Schaltfläche &quot;Ladevorgang abbrechen&quot; , während die Seite geladen wird. Die Seite wird für diese Aktivität während der aktuellen Bearbeitungssitzung in VEC nicht geladen.

![Schaltfläche &quot;Ladevorgang abbrechen «](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Um weiterhin Erlebnisse in der aktuellen Aktivität zu verwalten oder neue Änderungen hinzuzufügen, müssen Sie auf die Schaltfläche **[!UICONTROL &quot;Neu laden]** &quot; klicken.

![Schaltfläche &quot;Neu laden «](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>Es gibt ein aktuelles bekanntes Problem mit dieser Funktion, das in der nächsten Version behoben wird. Weitere Informationen finden Sie unter &quot;Ladevorgang einer Seite im VEC abbrechen&quot; in den [bekannten Problemen und](/help/r-release-notes/known-issues-resolved-issues.md#cancel) Seite mit gelösten Problemen.

## Schulungsvideos

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Visual Experience Composer (7:17)

In diesem Video erhalten Sie Informationen zum Verwenden der Optionen in Visual Experience Composer.

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (1 von 2) (7:17)

* Inhalt einer Seite ändern
* Layout einer Seite ändern

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2 von 2) (7:29)

* Erlebnis umbenennen und duplizieren
* Umleitungserlebnis erstellen
* Aktivität auf eine einzelne URL oder eine Gruppe von URLs ausrichten
* Mehrseitige Aktivität erstellen
* Erlebnisse für responsive Websites ansehen und erstellen
* Überlagerungen zum Hervorheben von Elementtypen nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Office Hours: Visual Experience Composer

Dieses Video ist eine Aufzeichnung von „[Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)“, einer Initiative der Adobe-Kundenunterstützung.

* So funktioniert der VEC
* So vermeiden Sie häufige Probleme mit dem VEC
* Workarounds für den VEC

>[!VIDEO](https://video.tv.adobe.com/v/20784/)