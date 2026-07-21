---
keywords: Flimmern,pre-hide,Prehiding,Personalisierung,Implementierung,Anti-Flimmern,VEC,Visual Experience Composer
description: Erfahren Sie, wie durch das Vorab-Ausblenden von Inhalten das Flackern reduziert wird, indem nur die Regionen ausgeblendet werden, die sich durch die aktive Adobe Target-Personalisierung ändern, indem eine Einstellung auf Kontoebene, eine einfache Seitenbibliothek und Steuerelemente für die einzelnen Aktivitäten verwendet werden.
title: Vorab-Ausblenden von Inhalten für personalisierte Erlebnisse
feature: Administration & Configuration
role: Admin
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
source-git-commit: 77741253fdfb007d0eda0c57fe293df2f9c638a2
workflow-type: tm+mt
source-wordcount: '624'
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

1. [!DNL Target] erstellt einen Regelsatz aus Live- [!UICONTROL Visual Experience Composer] und [!UICONTROL Enhanced Experience Composer]-Aktivitäten. Der Regelsatz listet Selektoren und Regionen auf, die sich im Versand ändern können.

   Beachten Sie[!UICONTROL &#x200B; dass Aktivitäten von „Form-Based Composer] nicht unterstützt werden.

1. Die -Bibliothek ruft diesen Regelsatz aus dem Adobe-CDN ab und blendet übereinstimmende Elemente nur dann vorab aus, wenn der personalisierte Inhalt noch geladen wird.

1. Unter **[!UICONTROL Ziele und Einstellungen]** können Sie das **[!UICONTROL Vorab-Ausblenden von Inhalten]** für einzelne Aktivitäten deaktivieren, jedoch nur, wenn es auf Kontoebene aktiviert ist. [Weitere Informationen](#content-pre-hiding-activity)

## Aktivieren der Vorab-Ausblendung von Inhalten für Ihre Instanz {#content-pre-hiding-enable-account}

>[!IMPORTANT]
>
>Um das Vorab-Ausblenden von Inhalten für die Instanz zu aktivieren, müssen Sie ein **Administrator** sein.

Das Vorab-Ausblenden von Inhalten für Ihre Instanz ist deaktiviert, bis Sie sie aktivieren. Verwenden Sie **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**, um die Funktion zu aktivieren, Standardwerte festzulegen und auf den Download für Ihr Implementierungs-Team zuzugreifen.

1. Klicken Sie [!DNL Target] auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.

1. Aktivieren Sie im **[!UICONTROL Vorab-Ausblenden von Inhalten]** die Option zum Vorab-Ausblenden von Inhalten.

   ![](assets/content-pre-hiding-1.png)

1. Aktualisieren Sie bei Bedarf die **[!UICONTROL Zeitüberschreitung vor dem Ausblenden]** in Sekunden.

1. Klicken Sie auf **[!UICONTROL Speichern]**. Dadurch werden Flimmerverwaltungseinstellungen auf Ihre Instanz angewendet.

1. Klicken Sie nach der Aktivierung **[!UICONTROL Herunterladen]** und fügen Sie dann die Datei zur `<head>` hinzu, damit sie vor dem [!DNL at.js] oder der [!DNL Web SDK] geladen wird. Umfassende Implementierungsanweisungen finden Sie unter [SDK zum Vorab-Ausblenden von Inhalten](https://experienceleague.adobe.com/de/docs/target-dev/developer/client-side/prehide-sdk).

   ![](assets/content-pre-hiding-2.png)

Ihre Instanz verwendet jetzt die Einstellungen für das Vorab-Ausblenden und das Timeout gespeicherter Inhalte als Standard für Aktivitäten, die sich anmelden.

## Aktivieren der Vorab-Ausblendung von Inhalten für Ihre Aktivität {#content-pre-hiding-activity}

Wählen Sie bei für Ihre Instanz aktiviertem Vorab-Ausblenden aus, ob jede Aktivität sie in „Ziele **[!UICONTROL Einstellungen“]**. Aktivitäten, für die Sie die Vorab-Ausblendung aktivieren, werden live in das Zielverhalten einbezogen.

[!DNL Target] erstellt dann einen schlanken Regelsatz aus Live-Aktivitäten, die in [!UICONTROL Visual Experience Composer] (VEC) und dem [!UICONTROL Form-Based Composer] verfasst wurden und die Selektoren und Bereiche beschreiben, die die Bereitstellung ändern kann.

Beim Erstellen oder Bearbeiten einer Aktivität:

1. Rufen Sie die Aktivität auf, für die Sie die Option zum Vorab-Ausblenden aktivieren möchten.

1. Rufen Sie die **[!UICONTROL Aktivität bearbeiten]** auf und wählen Sie **[!UICONTROL Ziele und Einstellungen bearbeiten]** aus.

   ![](assets/content-pre-hiding-3.png)

1. Schalten Sie im Menü **[!UICONTROL Vorab ausblenden]** die Option **[!UICONTROL Vorab ausblenden von Inhalten aktivieren]** um, um diese Aktivität für oder von der Vorab-Ausblendung zu deaktivieren.

   ![](assets/content-pre-hiding-4.png)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern und schließen]**.

Nach dem Speichern und der Live-Schaltung von Aktivitäten oder der Deaktivierung von werden die Regelsätze aktualisiert, sodass das Vorab-Ausblenden mit dem tatsächlichen Versand abgestimmt bleibt, ohne dass der Seiten-Code bei jedem Launch bearbeitet werden muss.

Auf der Besucherseite ruft die Bibliothek diesen Regelsatz bei jedem Laden der Seite aus dem Adobe-CDN ab und blendet übereinstimmende Elemente nur bei Bedarf vorab aus, bis personalisierte Inhalte bereit sind.
