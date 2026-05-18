---
keywords: Flimmern,pre-hide,Prehiding,Personalisierung,Implementierung,Anti-Flimmern,VEC,Visual Experience Composer
description: Erfahren Sie, wie durch das Vorab-Ausblenden von Inhalten das Flackern reduziert wird, indem nur die Regionen ausgeblendet werden, die sich durch die aktive Adobe Target-Personalisierung ändern, indem eine Einstellung auf Kontoebene, eine einfache Seitenbibliothek und Steuerelemente für die einzelnen Aktivitäten verwendet werden.
title: Vorab-Ausblenden von Inhalten für personalisierte Erlebnisse
feature: Administration & Configuration
role: Admin
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
source-git-commit: dfda53d7efb93ab4cbd980d27b47c0b67ee3e561
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 3%

---

# Vorab-Ausblenden von Inhalten für personalisierte Erlebnisse

>[!AVAILABILITY]
>
>Das Vorab-Ausblenden von Inhalten für personalisierte Inhalte ist als **Beta**-Funktion verfügbar.

Wenn ein Besucher eine Seite lädt, kann der Standardinhalt kurz angezeigt und dann durch personalisierte Inhalte aus [!DNL Adobe Target] ersetzt werden. Dieser sichtbare Schalter wird oft **Flackern** genannt und ist ein häufiges Erlebnisproblem bei Personalisierungsprogrammen.

Mit der Vorab-Ausblendung von Inhalten können Sie ein Flackern verhindern, indem Sie nur die Teile der Seite ausblenden, die durch Ihre Aktivitäten beim Laden der Seite personalisiert werden, sodass Ihre Kunden weniger Flackern und weniger leere Bildschirmzeit sehen.

So funktioniert das Vorab-Ausblenden von Inhalten: vom Standardkonto über die Implementierung auf der Seite bis hin zur Auswahl pro Aktivität.

1. Aktivieren Sie das Vorab-Ausblenden von Inhalten für Ihr Konto, um den globalen Standard festzulegen. Er ist standardmäßig deaktiviert. [Weitere Informationen](#content-pre-hiding-enable-account)

1. Fügen Sie die Bibliothek zum Vorab-Ausblenden von Inhalten der `<head>` aller Seiten hinzu, auf denen Sie Personalisierungsaktivitäten ausführen.

1. [!DNL Target] erstellt einen Regelsatz aus Live [!UICONTROL Visual Experience Composer]- und [!UICONTROL Enhanced Experience Composer]. Der Regelsatz listet Selektoren und Regionen auf, die sich im Versand ändern können.

   Beachten Sie, dass [!UICONTROL Form-Based Composer] Aktivitäten nicht unterstützt werden.

1. Die -Bibliothek ruft diesen Regelsatz aus dem Adobe-CDN ab und blendet übereinstimmende Elemente nur dann vorab aus, wenn der personalisierte Inhalt noch geladen wird.

1. In **[!UICONTROL Goals & Settings]** können Sie die **[!UICONTROL Content pre-hiding]** für einzelne Aktivitäten deaktivieren, jedoch nur, wenn sie auf Kontoebene aktiviert ist. [Weitere Informationen](#content-pre-hiding-activity)

## Aktivieren der Vorab-Ausblendung von Inhalten für Ihre Instanz {#content-pre-hiding-enable-account}

>[!IMPORTANT]
>
>Um das Vorab-Ausblenden von Inhalten für die Instanz zu aktivieren, müssen Sie ein **Administrator** sein.

Das Vorab-Ausblenden von Inhalten für Ihre Instanz ist deaktiviert, bis Sie sie aktivieren. Verwenden Sie **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** , um die Funktion zu aktivieren, Standardeinstellungen festzulegen und auf den Download für Ihr Implementierungs-Team zuzugreifen.

1. Klicken Sie [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. Aktivieren Sie im Menü **[!UICONTROL Content pre-hiding]** die Option zum Vorab-Ausblenden von Inhalten .

   ![](assets/content-pre-hiding-1.png)

1. Aktualisieren Sie die **[!UICONTROL Pre-hiding timeout]** bei Bedarf in Sekunden.

1. Klicken Sie auf **[!UICONTROL Save]**. Dadurch werden Flimmerverwaltungseinstellungen auf Ihre Instanz angewendet.

1. Klicken Sie nach der Aktivierung auf **[!UICONTROL Download]** und fügen Sie dann die Datei zur `<head>` hinzu, damit sie vor dem [!DNL at.js] oder der [!DNL Web SDK] geladen wird.

   ![](assets/content-pre-hiding-2.png)

Ihre Instanz verwendet jetzt die Einstellungen für das Vorab-Ausblenden und das Timeout gespeicherter Inhalte als Standard für Aktivitäten, die sich anmelden.

## Aktivieren der Vorab-Ausblendung von Inhalten für Ihre Aktivität {#content-pre-hiding-activity}

Wählen Sie bei für Ihre Instanz aktiviertem Vorab-Ausblenden aus, ob jede Aktivität sie in **[!UICONTROL Goals & Settings]** verwenden soll. Aktivitäten, für die Sie die Vorab-Ausblendung aktivieren, werden live in das Zielverhalten einbezogen.

[!DNL Target] erstellt dann einen schlanken Regelsatz aus den im [!UICONTROL Visual Experience Composer] (VEC) und im [!UICONTROL Form-Based Composer] erstellten Live-Aktivitäten und beschreibt die Selektoren und Bereiche, in denen sich der Versand ändern kann.

Beim Erstellen oder Bearbeiten einer Aktivität:

1. Rufen Sie die Aktivität auf, für die Sie die Option zum Vorab-Ausblenden aktivieren möchten.

1. Rufen Sie die Dropdown-Liste **[!UICONTROL Edit activity]** auf und wählen Sie **[!UICONTROL Edit Goals & Settings]** aus.

   ![](assets/content-pre-hiding-3.png)

1. Schalten Sie im Menü **[!UICONTROL Content pre-hiding]** die Option **[!UICONTROL Enable content pre-hiding]** ein, um diese Aktivität vom Vorab-Ausblenden auszuschließen.

   ![](assets/content-pre-hiding-4.png)

1. Klicken Sie abschließend auf **[!UICONTROL Save & Close]**.

Nach dem Speichern und der Live-Schaltung von Aktivitäten oder der Deaktivierung von werden die Regelsätze aktualisiert, sodass das Vorab-Ausblenden mit dem tatsächlichen Versand abgestimmt bleibt, ohne dass der Seiten-Code bei jedem Launch bearbeitet werden muss.

Auf der Besucherseite ruft die Bibliothek diesen Regelsatz bei jedem Laden der Seite aus dem Adobe-CDN ab und blendet übereinstimmende Elemente nur bei Bedarf vorab aus, bis personalisierte Inhalte bereit sind.
