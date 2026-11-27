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
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%
---
# Erste Schritte mit dem [!UICONTROL Visual Experience Composer] {#vec-overview}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie den [!UICONTROL Visual Experience Composer] (VEC) öffnen, Erlebnisse bearbeiten und das Laden von Seiten verwalten.

>[!ENDSHADEBOX]

Der [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] ist ein WYSIWYG-Editor zum Erstellen und Testen personalisierter Erlebnisse direkt auf Websites und mobilen Webseiten, ohne Code zu bearbeiten.

Erlebnisse und Angebote für [!DNL Target] Aktivitäten werden durch Ziehen und Ablegen von Elementen, Austauschen von Inhalten und Ändern des Seiten-Layouts erstellt. Der Composer bietet auch Optionen zum Bearbeiten von HTML und JavaScript.

## Browser-Anforderungen {#browser-requirements}

[!DNL Safari] wird für die [!DNL Adobe Target] unterstützt. Formularbasierte Aktivitäten können in [!DNL Safari] mit allen Funktionen erstellt werden, mit Ausnahme von VEC und [!UICONTROL Enhanced Experience Composer] (EEC). Wenn VEC in [!DNL Safari] geöffnet wird, fordert eine Überlagerung den Benutzer auf, zur [!DNL Google Chrome] zu wechseln, um Erlebnisse zu bearbeiten.

Browser wie [!DNL Firefox] blockieren möglicherweise Seiten, die gemischte Inhalte enthalten, z. B. eine nicht sichere Seite innerhalb einer sicheren Site, sodass sie in Visual Experience Composer nicht angezeigt werden. Wenn eine Seite nicht angezeigt wird, klicken Sie auf das Symbol neben der URL in der Adressleiste des Browsers und dann auf **[!UICONTROL Schutz auf dieser Seite deaktivieren]**. Dieses Problem hat keinen Einfluss darauf, wie Seiten den Site-Besuchern angezeigt werden.

## VEC öffnen {#open-the-vec}

Um festzulegen, welche Seite standardmäßig in VEC geöffnet wird, geben Sie eine Standard-URL [!UICONTROL Visual Experience Composer] auf der [!DNL Target] Registerkarte **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** ein. Wenn keine Standard-URL festgelegt ist, wird der VEC mit einer leeren Seite geöffnet, auf der eine URL angegeben werden kann.

![Administrationsseite mit hervorgehobener Registerkarte „Visual Experience Composer“, auf der die Einstellungen „Standard-URL“, „Enhanced Experience Composer“ und „Gemischte Inhalte laden“ angezeigt werden](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Erlebnisse bearbeiten {#edit-experiences}

### Erlebnisse anzeigen und benennen {#view-and-name-experiences}

Die Registerkarten in der Leiste **[!UICONTROL Erlebnisse]** zeigen, wie die Seite für unterschiedliche Zielgruppen oder mit unterschiedlichen Erlebnissen angezeigt wird. Ein beschreibender Name für jedes Erlebnis erleichtert die Identifizierung in der Liste. Wenn Sie beispielsweise die Position des Startseiten-Links in einer Navigationsleiste testen, kann das Erlebnis, in dem er zuerst angezeigt wird, als „Startseiten-Link zuerst“ bezeichnet werden.

![Das Dialogfeld „Erlebnis umbenennen“ mit dem Namen „Startseite“ wurde zuerst über das Symbol „Umbenennen“ von Erlebnis B geöffnet](/help/main/c-experiences/c-visual-experience-composer/assets/rename_exp.png)

### Auswählen und Ändern von Elementen {#select-and-modify-elements}

Wenn Sie den Cursor über die Seite bewegen, werden einzelne Elemente in einem kontextabhängigen Feld hervorgehoben. Durch Klicken auf ein hervorgehobenes Element werden die Bearbeitungsoptionen für diesen Elementtyp angezeigt. Wenn Sie beispielsweise ein Bild auswählen und auf **[!UICONTROL Bildangebot ändern]** klicken, wird es ersetzt, und durch Auswahl einer Schaltfläche kann dessen Textfarbe geändert werden.

![Bearbeitungsoptionen, die über einem ausgewählten Bild angezeigt werden](/help/main/c-experiences/c-visual-experience-composer/assets/properties-exp.png)

Inhalte innerhalb eines in die Seite eingebetteten iframes können nicht bearbeitet werden. Um diesen Inhalt zu bearbeiten, stellen Sie sicher, dass das iframe-Dokument [!DNL Target] aktiviert ist, und laden Sie dann die iframe-URL direkt in den VEC.

Änderungen an der Seitenstruktur außerhalb des VEC können sich auf die von einer Aktivität verwendeten Speicherorte auswirken. Wenn sich diese Speicherorte ändern, können [!DNL Target] möglicherweise die geänderten Elemente nicht finden, was bei der Bearbeitung von Erlebnissen zu Problemen führen kann.

### Durchsuchen und Design {#browse-and-design}

Klicken Sie **[!UICONTROL Durchsuchen]**, um zu einer Seite zu navigieren, auf die über die aktuelle Seite zugegriffen werden kann, z. B. zu einer Versandseite oder einem Warenkorb, und dort die Änderungen zu testen.

![Durchsuchen-Modus im VEC mit dem URL-Feld und den Rückwärts- und Vorwärtspfeilen](/help/main/c-experiences/c-visual-experience-composer/assets/browse_exp.png)

Im Durchsuchen-Modus können Sie auch auf Elemente zugreifen, die beim Bewegen des Mauszeigers angezeigt werden, z. B. Flyout-Menüs und Mini-Warenkörbe. Wenn die zu bearbeitende Seite oder das zu bearbeitende Element erreicht ist, klicken Sie auf **[!UICONTROL Design]**, um die Oberfläche zu bearbeiten.

Wenn der Hover-Status von JavaScript abhängt, stellen Sie sicher, dass **[!UICONTROL JavaScript deaktivieren]** nicht ausgewählt ist. JavaScript muss aktiviert sein, damit davon abhängige Elemente bearbeitet werden können.

Weitere Informationen zu den verfügbaren Bearbeitungsoptionen finden Sie unter [Visual Experience Composer-Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

## Seitenladevorgang verwalten {#manage-page-loading}

Einige Bearbeitungsoptionen bleiben verfügbar, während eine Seite geladen wird oder nachdem sie nicht geladen werden kann. Das Laden der Seite kann auch abgebrochen werden, um ohne zu warten auf diese Optionen zuzugreifen.

### Bearbeiten Sie eine Seite, während die Seite geladen wird oder nachdem sie nicht geladen werden kann {#loading}

Einige Änderungen können vorgenommen werden, bevor eine Seite in VEC vollständig geladen ist, oder nachdem sie nicht geladen werden kann, z. B. weil benutzerdefinierter Code nicht mehr funktioniert.

Die verfügbaren Bearbeitungsoptionen ermöglichen Folgendes:

* Nehmen Sie einfache Änderungen vor, z. B. Hinzufügen von benutzerdefiniertem Code oder Umbenennen eines Erlebnisses
* Kopieren Sie vorhandenen benutzerdefinierten Code von einer Seite, auf die nicht mehr zugegriffen werden kann
* Einfache Änderungen an einer Seite vornehmen, die nicht in VEC geladen werden kann

Die Optionen **[!UICONTROL Erlebnisse]** Leiste, **[!UICONTROL Komponenten]** Leiste und **[!UICONTROL Konfigurieren]** bleiben verfügbar, während die Seite geladen wird oder nachdem sie nicht geladen werden kann.

### Abbrechen des Seitenladevorgangs in VEC {#cancel-loading}

Wenn Sie das Laden der Seite in VEC abbrechen, können Sie die Aktivität bearbeiten, ohne darauf zu warten, dass die Seite fertig geladen wird. Dies ist nützlich für:

* Geringfügige Änderungen an vorhandenen Änderungen vornehmen
* Löschen einer oder mehrerer vorhandener Änderungen
* Benutzerdefinierten Code einfügen oder bearbeiten
* Korrigieren einer falsch eingegebenen Seiten-URL
* Aktivieren oder deaktivieren Sie JavaScript, bevor Sie die Seite in VEC laden
* Hinzufügen von Vorlagentestregeln zu den Kriterien **[!UICONTROL Seitenbereitstellung]**
* Überschreiben Sie den globalen Umschalter [!UICONTROL Enhanced Experience Composer] (EEC) beim Laden einer Seite durch den EEC oder im iframe-only-Modus

Nachdem das Laden der Seite abgebrochen wurde, können Sie in der Aktivität zwischen Erlebnissen wechseln, ohne darauf zu warten, dass die Seite geladen wird. Klicken Sie **[!UICONTROL Neu laden]**, um die Seite erneut im VEC anzuzeigen.

>[!IMPORTANT]
>
>Wenn benutzerdefinierter Code bearbeitet wird oder andere Änderungen vorgenommen werden, nachdem das Laden der Seite abgebrochen wurde, führen Sie Qualitätssicherungstests durch, um zu überprüfen, ob die Änderungen wie erwartet bereitgestellt werden.

Um das Laden der Seite zu stoppen, klicken Sie **[!UICONTROL Laden abbrechen]** während die Seite geladen wird. Die Seite bleibt für diese Aktivität während der aktuellen Bearbeitungssitzung entladen, es sei denn, sie wird neu geladen.

Klicken Sie **[!UICONTROL Neu laden]**, um die Erlebnisverwaltung in der aktuellen Aktivität fortzusetzen oder neue Änderungen hinzuzufügen.
