---
keywords: implementation;mbox;download mbox.js;download api;mbox.js api
description: Um Adobe Target Standard oder Zielgruppe Premium zu verwenden, fügen Sie eine Codezeile hinzu, um mbox.js aufzurufen.
title: „mbox.js“-Implementierung
feature: null
translation-type: tm+mt
source-git-commit: 863c5137383d35b2eaa33082c2136b81793281ca
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 30%

---


# „mbox.js“-Implementierung

Um [!DNL Adobe Target Standard] oder [!DNL Target Premium] zu verwenden, fügen Sie eine Codezeile hinzu, um mbox.js aufzurufen.

Sie können zwei Bibliotheksverweise verwenden: [!DNL Adobe Experience Platform Web SDK] oder [!DNL at.js]. [Die Vorteile von at.](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) jserläutern die Unterschiede zwischen den Bibliotheken &quot;mbox.js&quot;und &quot;at.js&quot;.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden.
>
>* **Adobe Experience Platform Web SDK**: Mit dem  [!UICONTROL Adobe Experience Platform Web ] SDK können Sie über das Adobe Experience Edge Network mit den verschiedenen Diensten im  [!DNL Experience Cloud] (einschließlich  [!DNL Target]) interagieren. Wenn Sie eine Migration zu [!DNL Adobe Experience Platform Web SDK] vornehmen, finden Sie weitere Informationen unter [Was ist Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html), im *Web SDK Guide*. Weitere Informationen finden Sie unter [Übersicht über die Zielgruppe](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html).[!DNL Target]
   >
   >
* **at.js**: Die JavaScript-Bibliothek at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen. Wenn Sie zu at.js migrieren möchten, finden Sie weitere Informationen unter [Funktionsweise von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Obwohl &quot;mbox.js&quot;derzeit unterstützt wird (bis 31. März 2021), haben wir seit Juli 2017 keine Funktionsupdates für diese Bibliothek bereitgestellt. Indem wir alle Kunden in das [!UICONTROL Adobe Experience Platform Web SDK] oder at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.

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