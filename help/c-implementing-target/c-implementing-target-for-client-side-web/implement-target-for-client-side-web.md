---
keywords: implementieren;Implementierung;at.js;adobe experience platform web sdk;aep web sdk
description: Erfahren Sie, wie Sie Adobe Target für clientseitige Webanwendungen mit dem Adobe Experience Platform Web SDK (AEP Web SDK) oder der JavaScript-Zielgruppe at.js implementieren.
title: Wie implementiere ich die Zielgruppe für clientseitige Web-Anwendungen?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Übersicht: Target für Client-seitiges Web implementieren

Bei Client-seitigen Implementierungen von [!DNL Adobe Target] stellt [!DNL Target] die mit einer Aktivität verknüpften Erlebnisse direkt dem Client-Browser bereit. Der Browser entscheidet, welches Erlebnis angezeigt werden soll, und zeigt es an. Bei einer Client-seitigen Implementierung können Sie einen WYSIWYG-Editor, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) oder eine nicht visuelle Schnittstelle, den [formularbasierten Experience Composer](/help/c-experiences/form-experience-composer.md), verwenden, um Aktivitäten und Personalisierungserlebnisse zu erstellen.

Um [!DNL Adobe Target] clientseitig zu implementieren, müssen Sie eine der folgenden JavaScript-Bibliotheken verwenden:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [JavaScript-Bibliothek &quot;at.js&quot;der Zielgruppe](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden.
>
>* **Adobe Experience Platform Web SDK**: Mit dem  [!UICONTROL Adobe Experience Platform Web ] SDK können Sie über das Adobe Experience Edge Network mit den verschiedenen Diensten im  [!DNL Experience Cloud] (einschließlich  [!DNL Target]) interagieren. Wenn Sie eine Migration zu [!DNL Adobe Experience Platform Web SDK] vornehmen, finden Sie weitere Informationen unter [Was ist Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) im *Web SDK Guide*.
   >
   >
* **at.js**: Die JavaScript-Bibliothek at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen. Wenn Sie zu at.js migrieren möchten, finden Sie weitere Informationen unter [Funktionsweise von at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Obwohl &quot;mbox.js&quot;derzeit unterstützt wird (bis 31. März 2021), haben wir seit Juli 2017 keine Funktionsupdates für diese Bibliothek bereitgestellt. Indem wir alle Kunden in das [!UICONTROL Adobe Experience Platform Web SDK] oder at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
