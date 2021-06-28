---
keywords: implementieren;Implementierung;at.js;Adobe Experience Platform Web SDK;aep Web SDK
description: Erfahren Sie, wie Sie die JavaScript-Bibliothek "at.js"von Adobe [!DNL Target] for client-side web using the Adobe Experience Platform Web SDK  (AEP Web SDK) or the [!DNL Target] implementieren.
title: Implementieren von [!DNL Target] für Client-seitiges Web
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 48%

---

# Übersicht: [!DNL Target] für clientseitige Web implementieren

Bei Client-seitigen Implementierungen von [!DNL Adobe Target] stellt [!DNL Target] die mit einer Aktivität verknüpften Erlebnisse direkt dem Client-Browser bereit. Der Browser entscheidet, welches Erlebnis angezeigt werden soll, und zeigt es an. Bei einer Client-seitigen Implementierung können Sie einen WYSIWYG-Editor, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder eine nicht visuelle Schnittstelle, den [formularbasierten Experience Composer](/help/c-experiences/form-experience-composer.md), verwenden, um Aktivitäten und Personalisierungserlebnisse zu erstellen.

Um [!DNL Adobe Target] clientseitig zu implementieren, müssen Sie eine der folgenden JavaScript-Bibliotheken verwenden:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [JavaScript-Bibliothek &quot;at.js&quot;in Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen. Adobe empfiehlt allen Kunden vor diesem Datum die Migration zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek at.js, um mögliche Probleme mit ihren Sites zu vermeiden.
>
>* **Adobe Experience Platform Web SDK**: Mit dem  [!UICONTROL Adobe Experience Platform Web ] SDK können Sie über das Adobe Experience Edge Network mit den verschiedenen Diensten in der  [!DNL Experience Cloud] (einschließlich  [!DNL Target]) interagieren. Wenn Sie eine Migration zu [!DNL Adobe Experience Platform Web SDK] vornehmen, finden Sie weitere Informationen unter [Was ist das Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) im *Web SDK Guide*.
   >
   >
* **at.js**: Die JavaScript-Bibliothek at.js verbessert die Seitenladezeiten bei Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen. Wenn Sie sich für eine Migration zu at.js entscheiden, finden Sie weitere Informationen unter [Funktionsweise von &quot;at.js&quot;](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie die mbox.js von Adobe Target zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).


