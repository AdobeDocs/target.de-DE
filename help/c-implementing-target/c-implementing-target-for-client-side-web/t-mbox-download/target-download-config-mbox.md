---
keywords: Implementation;Mbox;mbox.js;download mbox.js;configure mbox.js
description: Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.
title: mbox.js herunterladen
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 94%

---


# mbox.js herunterladen{#download-mbox-js}

Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.

Zur Verwendung des neuen [!DNL Adobe Target] [!UICONTROL  Visual Experience Editor] müssen Sie eine zusätzliche Zeile JavaScript als Teil Ihrer [!DNL mbox.js]-Datei einschließen.

1. Klicken Sie unter [!DNL Target Standard] auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**.
1. Klicken Sie auf **[!UICONTROL mbox.js herunterladen]** und folgen Sie den Anweisungen zum Speichern der Datei.
1. (Bedingt) Sollten Sie [!DNL mbox.js], Version 60 oder neuer verwenden, können Sie die Bibliothek so konfigurieren, dass automatisch Seiteninhalte ausgeblendet werden, bis die Mboxes geladen werden, damit das Flackern auf nicht responsiven Seiten verringert wird.

   Weitere Informationen finden Sie unter „Unterdrücken des Flackerns für Seitenladevorgänge“ in den [erweiterten „mbox.js“-Einstellungen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C).

1. Erstellen Sie die [!DNL mbox.js]-Referenz auf der Website.

   Ab [!DNL mbox.js], Version 57, kann der [!DNL mbox.js]-Verweis an einer beliebigen Stelle im `<head>`-Abschnitt auf der Seite platziert werden.

   >[!IMPORTANT]
   >
   >Wenn Sie eine [!DNL mbox.js]-Version verwenden, die älter als Version 57 ist, dann muss der Verweis das letzte Element im `<head>`-Abschnitt Ihrer Seiten sein. Ist die Referenz nicht das letzte Element, kann dies zu schwerwiegenden Anzeige- und Performance-Problemen führen. Weitere Informationen finden Sie unter [Was mbox.js tut](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-technical.md).

1. Laden Sie die gespeicherte [!DNL mbox.js]-Datei an den Ort in Ihrer Hosting-Umgebung hoch, den Sie im Code angegeben haben.
