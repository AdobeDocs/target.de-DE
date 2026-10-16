---
keywords: Visual Experience Composer;VEC;WYSIWYG
description: Lernen Sie die Grundlagen der Verwendung von Visual Experience Composer (VEC) in Adobe Target kennen. VEC ist ein WYSIWYG-Editor, mit dem Sie mühelos personalisierte Erlebnisse erstellen können.
title: Wie verwende ich Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
TQID: 'https://experienceleague.adobe.com/X4nfYuOtD3TVusnVIIEZhXwUdCZ-dMvbZeJlrkmI9Hs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 140a7287246905d47bf02a84348627017a619386
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%
---
# [!UICONTROL Visual Experience Composer] (VEC)

Der [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] ist ein WYSIWYG-Editor zum Erstellen und Testen personalisierter Erlebnisse direkt auf Websites und mobilen Web-Seiten, ohne den Code zu bearbeiten.

Erstellen Sie Erlebnisse und Angebote für [!DNL Target] Aktivitäten, indem Sie Elemente per Drag-and-Drop verschieben, Inhalte austauschen und Seiten-Layouts ändern. Der Composer bietet auch Optionen zum Bearbeiten von HTML und JavaScript.

## Browser-Anforderungen {#browser-requirements}

[!DNL Safari] wird für die [!DNL Adobe Target] unterstützt. Sie können formularbasierte Aktivitäten in [!DNL Safari] erstellen und alle -Funktionen außer VEC und [!UICONTROL Enhanced Experience Composer] (EEC) verwenden. Wenn Sie Visual Experience Composer in [!DNL Safari] öffnen, werden Sie durch eine Überlagerung aufgefordert, zum [!DNL Google Chrome] zu wechseln, um Erlebnisse zu bearbeiten.

Browser wie [!DNL Firefox] blockieren möglicherweise Seiten, die gemischte Inhalte enthalten, z. B. eine nicht sichere Seite innerhalb einer sicheren Site, sodass sie in Visual Experience Composer nicht angezeigt werden. Wenn eine Seite nicht angezeigt wird, klicken Sie auf das Symbol neben der URL in der Adressleiste des Browsers und dann auf **[!UICONTROL Schutz auf dieser Seite deaktivieren]**. Dieses Problem hat keinen Einfluss darauf, wie Seiten den Site-Besuchern angezeigt werden.

## VEC öffnen {#open-the-vec}

Um festzulegen, welche Seite standardmäßig in VEC geöffnet wird, geben Sie eine Standard-URL [!UICONTROL Visual Experience Composer] auf der [!DNL Target] Registerkarte **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** ein.

Wenn Sie keine Standard-URL festlegen, wird der VEC mit einer leeren Seite geöffnet, auf der Sie eine URL angeben können.

![VEC hervorgehoben](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Erlebnisse bearbeiten {#edit-experiences}

### Erlebnisse anzeigen und benennen {#view-and-name-experiences}

Verwenden Sie die Registerkarten in der Leiste [!UICONTROL Erlebnisse], um anzuzeigen, wie Ihre Seite in verschiedenen Zielgruppen oder mit unterschiedlichen Erlebnissen angezeigt wird. Geben Sie jedem Erlebnis einen beschreibenden Namen, damit es in der Liste leichter zu identifizieren ist.

Wenn Sie z. B. die Position des Startseiten-Links in Ihrer Navigationsleiste testen, nennen Sie das Erlebnis, in dem er zuerst angezeigt wird, „Startseiten-Link zuerst“.

![Umbenennen eines Erlebnisses in der Leiste Erlebnisse](/help/main/c-experiences/c-visual-experience-composer/assets/rename_exp.png)

### Auswählen und Ändern von Elementen {#select-and-modify-elements}

Bewegen Sie den Cursor über die Seite, um einzelne Elemente mit einem kontextsensitiven Feld hervorzuheben.

Klicken Sie auf ein hervorgehobenes Element, um die Bearbeitungsoptionen für diesen Elementtyp anzuzeigen. Wählen Sie beispielsweise ein Bild aus und klicken Sie auf **[!UICONTROL Bildquelle ändern]**, um es zu ersetzen, oder wählen Sie eine Schaltfläche aus, um seine Textfarbe zu ändern.

![Bearbeitungsoptionen für ein ausgewähltes Element](/help/main/c-experiences/c-visual-experience-composer/assets/properties-exp.png)

Sie können keine Inhalte in einem IFrame bearbeiten, der in die Seite eingebettet ist. Um diesen Inhalt zu bearbeiten, stellen Sie sicher, dass das iframe-Dokument [!DNL Target] aktiviert ist, und laden Sie dann die iframe-URL direkt in den VEC.

Änderungen an der Seitenstruktur außerhalb von VEC können Standorte betreffen, die von einer Aktivität verwendet werden. Wenn sich diese Speicherorte ändern, können [!DNL Target] möglicherweise die von Ihnen geänderten Elemente nicht finden, was zu Problemen bei der Bearbeitung von Erlebnissen führen kann.

### Durchsuchen und Design {#browse-and-design}

Klicken Sie **[!UICONTROL Durchsuchen]**, um zu einer Seite zu navigieren, auf die über die aktuelle Seite zugegriffen werden kann, z. B. zu einer Versandseite oder einem Warenkorb, und dort die Änderungen zu testen.

![Durchsuchen-Modus im VEC](/help/main/c-experiences/c-visual-experience-composer/assets/browse_exp.png)

Im Durchsuchen-Modus können Sie auch auf Elemente zugreifen, die beim Bewegen des Mauszeigers angezeigt werden, wie Flyout-Menüs und Mini-Warenkörbe. Wenn Sie die Seite oder das Element erreichen, die Sie bearbeiten möchten, klicken Sie auf **[!UICONTROL Design]**, um das Erlebnis zu bearbeiten.

Wenn der Hover-Status von JavaScript abhängt, stellen Sie sicher, dass **[!UICONTROL JavaScript deaktivieren]** nicht ausgewählt ist. JavaScript muss aktiviert sein, damit davon abhängige Elemente bearbeitet werden können.

Weitere Informationen zu den verfügbaren Bearbeitungsoptionen finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

## Seitenladevorgang verwalten {#manage-page-loading}

Einige Bearbeitungsoptionen bleiben verfügbar, während eine Seite geladen wird oder nachdem sie nicht geladen werden kann. Sie können das Laden der Seite auch abbrechen, um auf diese Optionen zuzugreifen, ohne zu warten.

### Bearbeiten Sie eine Seite, während die Seite geladen wird oder nachdem sie nicht geladen werden kann {#loading}

Sie können einige Änderungen vornehmen, bevor eine Seite in VEC vollständig geladen ist oder nachdem sie nicht geladen werden kann, z. B. weil benutzerdefinierter Code nicht mehr funktioniert.

Verwenden Sie die verfügbaren Bearbeitungsoptionen, um:

* Nehmen Sie einfache Änderungen vor, z. B. Hinzufügen von benutzerdefiniertem Code oder Umbenennen eines Erlebnisses
* Kopieren Sie vorhandenen benutzerdefinierten Code von einer Seite, auf die nicht mehr zugegriffen werden kann
* Einfache Änderungen an einer Seite vornehmen, die nicht in VEC geladen werden kann

Die Optionen [!UICONTROL Erlebnisse] Leiste, [!UICONTROL Komponenten] Leiste und [!UICONTROL Konfigurieren] bleiben verfügbar, während die Seite geladen wird oder nachdem sie nicht geladen werden kann.

### Abbrechen des Seitenladevorgangs in VEC {#cancel-loading}

Abbrechen des Seitenladevorgangs in Visual Experience Composer, um die Aktivität zu bearbeiten, ohne darauf zu warten, dass das Laden der Seite abgeschlossen ist.

Das Abbrechen des Seitenladevorgangs ist bei folgenden Aufgaben nützlich:

* Geringfügige Änderungen an vorhandenen Änderungen vornehmen
* Löschen einer oder mehrerer vorhandener Änderungen
* Benutzerdefinierten Code einfügen oder bearbeiten
* Korrigieren einer falsch eingegebenen Seiten-URL
* Aktivieren oder deaktivieren Sie JavaScript, bevor Sie die Seite in VEC laden
* Hinzufügen von Vorlagentestregeln zu den Kriterien [!UICONTROL Seitenbereitstellung]
* Überschreiben Sie den globalen Umschalter [!UICONTROL Enhanced Experience Composer] (EEC) beim Laden einer Seite durch den EEC oder im iframe-only-Modus

Nach dem Abbrechen des Seitenladevorgangs können Sie in der Aktivität zwischen Erlebnissen wechseln, ohne darauf zu warten, dass die Seite geladen wird. Klicken Sie **[!UICONTROL Neu laden]**, um die Seite erneut im VEC anzuzeigen.

>[!IMPORTANT]
>
>Wenn Sie benutzerdefinierten Code bearbeiten oder andere Änderungen vornehmen, nachdem Sie das Laden der Seite abgebrochen haben, führen Sie Qualitätssicherungstests durch, um zu überprüfen, ob Ihre Änderungen wie erwartet bereitgestellt werden.

Um das Laden der Seite zu stoppen, klicken Sie **[!UICONTROL Laden abbrechen]** während die Seite geladen wird. Die Seite bleibt für diese Aktivität während der aktuellen Bearbeitungssitzung entladen, es sei denn, sie wird neu geladen.

Klicken Sie **[!UICONTROL Neu laden]**, um die Erlebnisverwaltung in der aktuellen Aktivität fortzusetzen oder neue Änderungen hinzuzufügen.
