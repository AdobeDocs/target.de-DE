---
keywords: Implementierung;mbox.js;DOM-Manipulations-Bibliothek;target.js;Visual Experience Composer;iFrame;Angular-Sites;Einzelseiten-Apps;Einzelseitenanwendung;SPA
description: Erfahren Sie mehr über die alte mbox.js-Implementierung von Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Was bewirkt die Bibliothek [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 62f0cbd2-17f0-43f4-98d3-ea39f314525e
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 78%

---

# Funktionsweise von „mbox.js“

Diese Informationen helfen Ihren technischen Mitarbeitern dabei, die „mbox.js“-Implementierung und die möglichen Auswirkungen auf Ihre Site zu verstehen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Wir empfehlen allen Kunden, vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek zu migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## DOM-Manipulation {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] steuert die von Standard verwendete DOM-Manipulationsbibliothek. Zur Anzeige des Inhalts auf einer Website verweist [!DNL target.js] auf [!DNL sizzle.js] (Version1.10.8-pre). [!DNL Sizzle.js] aktiviert die HTML-Elementselektoren. Mit Ausnahme von [!DNL sizzle.js] wird nur natives JavaScript verwendet. Es ist keine jquery erforderlich.

Zusätzlich wird folgendes Snippet zur Abstimmung von DOM verwendet:
 
`https://github.com/dperini/ContentLoaded`

## Target.js und der Visual Experience Composer {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Wenn Sie den [!UICONTROL Visual Experience Composer] zum Einrichten eines Erlebnisses für eine Aktivität verwenden, wird Ihre Webseite in einem iFrame geöffnet. Wenn der iFrame geladen ist, sendet Standard einen HTML5-`postMessage`-API-Aufruf. [!DNL Target.js] erkennt sämtliche `postMessage`-Aufrufe und schließt die folgenden JavaScript-Bibliotheken auf der Website ein:

* Für die Erstellung von Miniaturansichten: [!DNL https://html2canvas.hertzen.com/]
* Für eine domänenübergreifende Abfrage: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], verwendet, um Nachrichten über die iFrames hinweg zu senden. Durch diese Skripts kann Adobe Daten zwischen den Seiten senden.

## Zu berücksichtigende Punkte für Angular-Sites und Einzelseiten-Apps  {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Sollten Sie Target in eine Angular-Site oder eine Einzelseiten-App (SPA) integrieren, sollten Sie die at.js-Bibliothek anstatt der mbox.js-Bibliothek verwenden.
