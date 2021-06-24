---
keywords: Implementierung;Mbox;mbox.js herunterladen;API herunterladen;mbox.js-API
description: Erfahren Sie mehr über die alte mbox.js-Implementierung von Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Wie implementiere ich [!DNL Target] mit mbox.js?
feature: at.js
role: Developer
exl-id: 105095d7-8e29-413b-a7f4-e46e2e30e91f
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 65%

---

# „mbox.js“-Implementierung

Um [!DNL Adobe Target Standard] oder [!DNL Target Premium] zu verwenden, fügen Sie eine Codezeile hinzu, um mbox.js aufzurufen.

Sie können eine von zwei Bibliotheksverweisen verwenden: [!DNL Adobe Experience Platform Web SDK] oder [!DNL at.js].

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Wir empfehlen allen Kunden, vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek zu migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

Die einzelne Referenz zu [!DNL mbox.js] auf jeder Seite stellt die Bibliotheken bereit, die für alle Ihre Aktivitäten erforderlich sind. [!DNL mbox.js] sendet auf jeder Seite einen Aufruf an [!DNL Target], auf der die Datei [!DNL mbox.js] referenziert ist. Dies ermöglicht es [!DNL Target], Folgendes zu tun:

* Target-Aktivitäten bereitstellen,
* Klicks verfolgen,
* die meisten Erfolgsmetriken verfolgen.

>[!TIP]
>
>Zur Vereinfachung der Implementierung können Sie [!DNL mbox.js] in Ihrer globalen Kopfzeile referenzieren.

Daher müssen Sie keine unterschiedlichen Dateiversionen für einzelne Aktivitäten verwalten.

1. Referenzieren Sie [!DNL mbox.js] im Abschnitt `<head>` auf jeder Seite Ihrer Website.

   `<script src="/ *`directory`*/ *`scripts`*/mbox.js"></script>`

   Dabei ist ` *`directory`*/ *`scripts`*` das Verzeichnis, in dem Sie die [!DNL mbox.js]-Datei nach dem Herunterladen gespeichert haben.
Wenn Sie bereits Mboxes aus einer bestehenden Implementierung auf Ihrer Seite haben, können diese Mboxes weiterhin auf der neuen Oberfläche verwendet werden. Die aktualisierte [!DNL mbox.js]-Datei ist nach wie vor erforderlich, diese Mboxes können jedoch für Aktivitäten ausgewählt und mit dem [!UICONTROL Visual Experience Composer] bearbeitet werden.
