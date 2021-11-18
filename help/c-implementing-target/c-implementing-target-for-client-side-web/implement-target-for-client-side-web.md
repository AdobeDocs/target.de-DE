---
keywords: implementieren;Implementierung;at.js;Adobe Experience Platform Web SDK;aep Web SDK
description: Erfahren Sie, wie Sie Adobe implementieren [!DNL Target] for client-side web using the Adobe Experience Platform Web SDK  (AEP Web SDK) or the [!DNL Target] at.js-JavaScript-Bibliothek.
title: Implementieren [!DNL Target] für Client-seitiges Web
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 47%

---

# Übersicht: implementieren [!DNL Target] für Client-seitige Websites

Bei Client-seitigen Implementierungen von [!DNL Adobe Target] stellt [!DNL Target] die mit einer Aktivität verknüpften Erlebnisse direkt dem Client-Browser bereit. Der Browser entscheidet, welches Erlebnis angezeigt werden soll, und zeigt es an. Bei einer Client-seitigen Implementierung können Sie einen WYSIWYG-Editor, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder eine nicht visuelle Schnittstelle, den [formularbasierten Experience Composer](/help/c-experiences/form-experience-composer.md), verwenden, um Aktivitäten und Personalisierungserlebnisse zu erstellen.

Zu implementieren [!DNL Adobe Target] clientseitig müssen Sie eine der folgenden JavaScript-Bibliotheken verwenden:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [JavaScript-Bibliothek &quot;at.js&quot;in Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**Beendigung von**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen. Adobe empfiehlt allen Kunden vor diesem Datum die Migration zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek at.js, um mögliche Probleme mit ihren Sites zu vermeiden.
>
>* **Adobe Experience Platform Web SDK**: Die [!UICONTROL Adobe Experience Platform Web SDK] ermöglicht die Interaktion mit den verschiedenen Diensten im [!DNL Experience Cloud] (einschließlich [!DNL Target]) über das Adobe Experience Edge Network. Wenn Sie sich für eine Migration zum [!DNL Adobe Experience Platform Web SDK], siehe [Was ist das Adobe Experience Platform Web SDK?](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) im *Web SDK-Anleitung*.
>
>* **at.js**: Die JavaScript-Bibliothek at.js verbessert die Seitenladezeiten bei Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen. Informationen zum Migrieren zu at.js finden Sie unter [Funktionsweise von &quot;at.js&quot;](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) und [Adobe Target Skill Builder: Entwickler-Chat, Migration von Adobe Target mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).


