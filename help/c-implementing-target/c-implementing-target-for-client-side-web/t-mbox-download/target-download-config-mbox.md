---
description: Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.
keywords: Implementierung;Mbox;mbox.js;mbox.js herunterladen;mbox.js konfigurieren
seo-description: Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.
seo-title: mbox.js herunterladen
solution: Target
subtopic: Erste Schritte
title: mbox.js herunterladen
topic: Standard
uuid: b2a46321-cac7-4924-92dd-a80b50e27cee
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mbox.js herunterladen{#download-mbox-js}

Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.

Zur Verwendung des neuen [!DNL Adobe Target] [!UICONTROL  Visual Experience Editor] müssen Sie eine zusätzliche Zeile JavaScript als Teil Ihrer [!DNL mbox.js]-Datei einschließen.

1. Klicken Sie auf **[!UICONTROL Einrichtung]** &gt; **[!UICONTROL Implementierung]** in [!DNL Target Standard].
1. Klicken Sie auf **[!UICONTROL mbox.js herunterladen]** und folgen Sie den Anweisungen zum Speichern der Datei.
1. (Bedingt) Sollten Sie [!DNL mbox.js], Version 60 oder neuer verwenden, können Sie die Bibliothek so konfigurieren, dass automatisch Seiteninhalte ausgeblendet werden, bis die Mboxes geladen werden, damit das Flackern auf nicht responsiven Seiten verringert wird.

   Weitere Informationen finden Sie unter „Unterdrücken des Flackerns für Seitenladevorgänge“ in den [erweiterten „mbox.js“-Einstellungen](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C).

1. Erstellen Sie die [!DNL mbox.js]-Referenz auf der Website.

   Ab [!DNL mbox.js], Version 57, kann der [!DNL mbox.js]-Verweis an einer beliebigen Stelle im `<head>`-Abschnitt auf der Seite platziert werden.

   >[!IMPORTANT]
   >
   >Wenn Sie eine [!DNL mbox.js]-Version verwenden, die älter als Version 57 ist, dann muss der Verweis das letzte Element im `<head>`-Abschnitt Ihrer Seiten sein. Ist die Referenz nicht das letzte Element, kann dies zu schwerwiegenden Anzeige- und Performance-Problemen führen. Weitere Informationen finden Sie im Abschnitt [Technische Details zur Implementierung](https://marketing.adobe.com/resources/help/en_US/target/ov/c_mbox_technical.html).

1. Laden Sie die gespeicherte [!DNL mbox.js]-Datei an den Ort in Ihrer Hosting-Umgebung hoch, den Sie im Code angegeben haben.
