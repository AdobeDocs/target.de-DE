---
keywords: Implementierung;Mbox;mbox.js;mbox.js herunterladen;mbox.js konfigurieren
description: Erfahren Sie mehr über die ältere Implementierung von "mbox.js"in Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Wie lade ich die Bibliothek  [!DNL Target] mbox.js herunter?
feature: 'at.js '
role: Developer
exl-id: 92096b1b-a8a5-435b-8e62-24b5d15d392f
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 58%

---

# mbox.js herunterladen

Target Standard und Premium verwenden eine modifizierte Version der Adobe Target-Datei „mbox.js“.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Ab dem 31. März 2021 wird die Bibliothek &quot;mbox.js&quot; [!DNL Adobe Target] nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

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
