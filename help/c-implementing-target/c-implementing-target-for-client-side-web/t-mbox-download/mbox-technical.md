---
keywords: implementation;mbox.js;dom manipulation library;target.js;visual experience composer;iframe;angular sites;single page applications;single page app;SPA
description: Diese Informationen helfen Ihren technischen Mitarbeitern dabei, die „mbox.js“-Implementierung und die möglichen Auswirkungen auf Ihre Site zu verstehen.
title: Funktionsweise von „mbox.js“
feature: null
translation-type: tm+mt
source-git-commit: ae44c57c7b8767915fbbce4271a4b1858dd07efd
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 80%

---


# Funktionsweise von „mbox.js“{#what-mbox-js-does}

Diese Informationen helfen Ihren technischen Mitarbeitern dabei, die „mbox.js“-Implementierung und die möglichen Auswirkungen auf Ihre Site zu verstehen.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

Target Standard erfordert die [!DNL mbox.js]-Version 58 oder neuer. Anweisungen zum Herunterladen und Aktualisieren von [!DNL mbox.js] finden Sie unter [Mbox-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420).

Für Target Standard ruft [!DNL mbox.js] eine andere JavaScript-Datei auf, [!DNL target.js]. [!DNL Target.js] wird von Adobe gehostet und automatisch aktualisiert. Sie müssen nichts unternehmen, um [!DNL target.js] zu aktualisieren, und es gibt keine kundenspezifischen Anpassungen.

[!DNL Target.js] erstellt eine Mbox mit der Bezeichnung `target-global-mbox` im `<head>`-Abschnitt Ihrer Seite.

[!DNL Target.js] wird von [!DNL mbox.js] von einer Zeile von JavaScript-Code aufgerufen, die zum Feld [!UICONTROL Extra JavaScript] in [!DNL mbox.js] hinzugefügt wird. Die einzige Möglichkeit, [!DNL target.js] zu deaktivieren, ist, die Codezeile nicht aufzunehmen und so auch [!DNL Target] zu deaktivieren.

[!DNL Target.js] hat in [!DNL Target] zwei Funktionen:

* DOM-Manipulation
* Aktiviert visuelle Elemente von [!UICONTROL Visual Experience Composer]

## DOM-Manipulation {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] steuert die von Standard verwendete DOM-Manipulationsbibliothek. Zur Anzeige des Inhalts auf einer Website verweist [!DNL target.js] auf [!DNL sizzle.js] (Version1.10.8-pre). [!DNL Sizzle.js] aktiviert die HTML-Elementselektoren. Mit Ausnahme von [!DNL sizzle.js] wird nur natives JavaScript verwendet. Es ist keine jquery erforderlich.

Zusätzlich wird folgendes Snippet zur Abstimmung von DOM verwendet:
 
`https://github.com/dperini/ContentLoaded`

## Target.js und der Visual Experience Composer {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Wenn Sie den [!UICONTROL Visual Experience Composer] zum Einrichten eines Erlebnisses für eine Aktivität verwenden, wird Ihre Webseite in einem iFrame geöffnet. Wenn der iFrame geladen ist, sendet Standard einen HTML5-`postMessage`-API-Aufruf. [!DNL Target.js] erkennt sämtliche `postMessage`-Aufrufe und schließt die folgenden JavaScript-Bibliotheken auf der Website ein:

* Für die Erstellung von Miniaturansichten: [!DNL https://html2canvas.hertzen.com/]
* Für eine domänenübergreifende Abfrage: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], verwendet, um Nachrichten über die iFrames hinweg zu senden. Durch diese Skripts kann Adobe Daten zwischen den Seiten senden.

## Zu berücksichtigende Punkte für Angular-Sites und Einzelseiten-Apps   {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Sollten Sie Target in eine Angular-Site oder eine Einzelseiten-App (SPA) integrieren, sollten Sie die at.js-Bibliothek anstatt der mbox.js-Bibliothek verwenden.

Weitere Informationen finden Sie unter [„at.js“-Implementierung](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).
