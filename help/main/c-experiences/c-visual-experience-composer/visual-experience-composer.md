---
keywords: Visual Experience Composer;VEC;WYSIWYG
description: Lernen Sie die Grundlagen der Verwendung von Visual Experience Composer (VEC) in Adobe Target kennen. VEC ist ein WYSIWYG-Editor, mit dem Sie mühelos personalisierte Erlebnisse erstellen können.
title: Wie verwende ich Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
source-git-commit: 35699792dac84c93775aab9dde46d62c988e2838
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 57%

---

# Visual Experience Composer (VEC)

Informationen zur Verwendung des [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].

>[!NOTE]
>
>Die Version [!DNL Target Standard/Premium] 25.2.1 (12. Februar 2025) enthielt eine aktualisierte Version des VEC. Informationen darüber, wie sich der aktualisierte VEC von der vorherigen Version unterscheidet, finden Sie unter [Änderungen am Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md).

VEC ist eine Benutzeroberfläche von WYSIWYG, mit der Sie personalisierte Erlebnisse und Angebote im Kontext der Website einfach erstellen und testen können. Sie können Erlebnisse und Angebote für [!DNL Target] Aktivitäten erstellen, indem Sie das Layout und den Inhalt einer Web-Seite (oder eines Angebots) oder einer mobilen Web-Seite per Drag-and-Drop austauschen und ändern.

Der VEC ist eine der Hauptkomponenten von [!DNL Adobe Target]. Der VEC ermöglicht Marketingexperten und Designern, Inhalte über eine visuelle Benutzeroberfläche zu erstellen und zu ändern. Viele Entwurfsentscheidungen können getroffen werden, ohne den Code direkt bearbeiten zu müssen. Die Bearbeitung von HTML und JavaScript ist über die Bearbeitungsoptionen, die im Composer verfügbar sind, ebenfalls möglich.

Auf der Registerkarte Target **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** können Sie die Standard-[!UICONTROL Visual Experience Composer]-URL eingeben.

![VEC hervorgehoben](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

Diese URL legt fest, wo Sie beim Öffnen des VEC starten. Wenn Sie keine Standardeinstellung festlegen, wird Ihnen beim Öffnen des Editors eine leere Seite angezeigt. Sie können die URL dann festlegen.

>[!NOTE]
>
>Bestimmte Browser, z. B. [!DNL Firefox], blockieren möglicherweise die Anzeige einer Seite im VEC, wenn die Seite gemischte Inhalte enthält (z. B. eine nicht sichere Seite in einer sicheren Site). Wenn Ihre Seite nicht angezeigt wird, klicken Sie auf das Symbol neben der URL in der Browser-Adressleiste und klicken Sie auf **[!UICONTROL Disable protection on this page]**. Dieses Problem betrifft nicht die Anzeige Ihrer Seiten für Site-Besucher.

Inhalt in einem iframe auf der Seite kann nicht im VEC bearbeitet werden. Um Inhalte in einem iframe zu bearbeiten, stellen Sie sicher, dass das iframe-Dokument [!DNL Target] aktiviert ist, und laden Sie dann diese iframe-URL in den VEC.

Über die Registerkarten im [!UICONTROL Experiences] können Sie Ihre Seite so anzeigen, wie sie für unterschiedliche Zielgruppen oder mit unterschiedlichen Erlebnissen dargestellt würde. Sie können für jedes Erlebnis einen Namen angeben. Wenn Sie beispielsweise den Standort des Startseiten-Links in Ihrer Navigationsleiste testen möchten, können Sie einem Erlebnis, in dem der Startseiten-Link zuerst angezeigt wird, zum Beispiel die Bezeichnung „Startseiten-Link“ geben, um die Erlebnisse in der Liste leichter zu identifizieren.

>[!NOTE]
>
>Änderungen an den Strukturen einer Seite, die sich auf die Orte auswirken, welche in einer auf der Seite erstellten Aktivität verwendet werden, können Probleme bei der Bearbeitung des Erlebnisses verursachen. Wenn ein Speicherort außerhalb von VEC geändert wurde, können [!DNL Target] den Speicherort, an dem der Inhalt geändert wurde, möglicherweise nicht finden.

Wenn Sie Ihren Mauszeiger auf der Seite bewegen, folgt dem Cursor ein kontextbezogenes Feld, das Elemente auf der Seite hervorhebt.

<!--Click the **[!UICONTROL Overlays]** icon to change the way the highlight displays. For example, you can choose to highlight only images, links, regional mboxes, modifications, or JavaScript. You can change the color of the highlight. You can also specify a highlight color and type of fill used to highlight different element types.

![Change Overlay settings](/help/main/c-experiences/c-visual-experience-composer/assets/change-overlay.png)-->

Klicken Sie auf ein hervorgehobenes Element für ein Menü mit Optionen, die für diesen Elementtyp verfügbar sind. Sie können beispielsweise auf ein Bild klicken und **[!UICONTROL Change Image]** auswählen, um das Bild in ein anderes Bild zu ändern. Oder klicken Sie auf eine Schaltfläche und ändern Sie die Textfarbe.

Sie können auch auf **[!UICONTROL Browse]** klicken, dann zu einer Seite gehen, die auf der primären Seite verfügbar ist, z. B. eine Versandseite oder einen Warenkorb, und die Änderungen auf dieser Seite testen. Sie können auch auf Seitenelemente zugreifen, die verfügbar werden, wenn Sie den Mauszeiger darüber bewegen, wie zum Beispiel Flyout-Menüs und Minicarts. Wenn Sie mit dem Navigieren zur Seite fertig sind, klicken Sie auf **[!UICONTROL Design]** , um das Erlebnis zu bearbeiten. Vielleicht möchten Sie zum Beispiel den Entwurf für ein Einkaufswagendropdown oder ein Bilderkarussell verändern.

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

Um mit der Verwaltung von Erlebnissen in der aktuellen Aktivität fortzufahren oder neue Änderungen hinzuzufügen, müssen Sie auf die Schaltfläche **[!UICONTROL Reload]** klicken.
