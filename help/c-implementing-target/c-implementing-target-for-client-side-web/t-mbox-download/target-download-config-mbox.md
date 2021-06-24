---
keywords: Implementierung;Mbox;mbox.js;mbox.js herunterladen;mbox.js konfigurieren
description: Erfahren Sie mehr über die alte mbox.js-Implementierung von Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Wie lade ich die Bibliothek [!DNL Target] mbox.js herunter?
feature: at.js
role: Developer
exl-id: 92096b1b-a8a5-435b-8e62-24b5d15d392f
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 74%

---

# mbox.js herunterladen

Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Wir empfehlen allen Kunden, vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek zu migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

Zur Verwendung des neuen [!DNL Adobe Target] [!UICONTROL  Visual Experience Editor] müssen Sie eine zusätzliche Zeile JavaScript als Teil Ihrer [!DNL mbox.js]-Datei einschließen.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** in [!DNL Target Standard].
1. Klicken Sie auf **[!UICONTROL mbox.js herunterladen]** und folgen Sie den Anweisungen zum Speichern der Datei.
1. (Bedingt) Sollten Sie [!DNL mbox.js], Version 60 oder neuer verwenden, können Sie die Bibliothek so konfigurieren, dass automatisch Seiteninhalte ausgeblendet werden, bis die Mboxes geladen werden, damit das Flackern auf nicht responsiven Seiten verringert wird.

1. Erstellen Sie die [!DNL mbox.js]-Referenz auf der Website.

   Ab [!DNL mbox.js], Version 57, kann der [!DNL mbox.js]-Verweis an einer beliebigen Stelle im `<head>`-Abschnitt auf der Seite platziert werden.

   >[!IMPORTANT]
   >
   >Wenn Sie eine [!DNL mbox.js]-Version verwenden, die älter als Version 57 ist, dann muss der Verweis das letzte Element im `<head>`-Abschnitt Ihrer Seiten sein. Ist die Referenz nicht das letzte Element, kann dies zu schwerwiegenden Anzeige- und Performance-Problemen führen.

1. Laden Sie die gespeicherte [!DNL mbox.js]-Datei an den Ort in Ihrer Hosting-Umgebung hoch, den Sie im Code angegeben haben.
