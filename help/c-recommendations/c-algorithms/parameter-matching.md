---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Dynamische Filterung in Adobe Target Recommendations durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anforderung (API oder mbox).
title: Filtern nach Parameterübereinstimmung in Regeln für die dynamische Integration in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: c814215476ef6e40f4f175fe3f9dbb2c26b966eb
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 10%

---


# ![PREMIUM](/help/assets/premium.png) -Parameterübereinstimmung

Dynamisches Filtern durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anforderung (API oder mbox).

Empfehlen Sie beispielsweise nur Inhalte, die mit dem Seitenparameter &quot;Branche&quot;oder anderen Parametern übereinstimmen, wie z. B. Geräteabmessungen oder Geolocation, wie in den folgenden Beispielen.

* Mbox-Parameter für Bildschirmbreite und -höhe können zur Zielgruppe von mobilen Besuchern und zur Empfehlung von Mobilgeräten und Zubehör verwendet werden.
* Erstellen Sie eine Recommendations-Regel, die nur die meistverkauften Mobiltelefone zurückgibt, die der Bildschirmhöhe des Mobilgeräts entsprechen oder diese überschreiten, das der Besucher mit der Ansicht verwendet.
* Regionale Geo-Positionsparameter können verwendet werden, um Empfehlungen für Tools während des Winters zurückzugeben. Schneeflocken und andere Schneefälle können für Besucher in Bereichen empfohlen werden, in denen es schneit, aber nicht für Besucher in Gebieten, in denen es nicht schneit.

>[!NOTE]
>
>Wenn die Aktivität vor dem 31. Oktober 2016 erstellt wurde, schlägt ihr Versand fehl, wenn der Filter &quot;Parameterübereinstimmung&quot;verwendet wird. So umgehen Sie das Problem:
>
>* Erstellen Sie eine neue Aktivität und fügen Sie Ihre Kriterien darin hinzu.
>* Verwenden Sie Kriterien, die den Filter „Parameterübereinstimmung“ nicht enthalten.
>* Entfernen Sie den Filter „Parameterübereinstimmung“ aus Ihren Kriterien.


## Beispiele für Parameterübereinstimmung

[!UICONTROL Mit der Parameterübereinstimmung] können Sie Inhalte empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Geräteabmessungen oder Geolocation, wie im folgenden Beispiel:

[!DNL Recommendations] kann mit den Parameterwerten übereinstimmen, die im [!DNL Target] Aufruf gesendet werden. In diesem Fall [!DNL Target] [!DNL Target] erkennt ein Besucher, dass er ein Mobilgerät verwendet, basierend auf den im Aufruf gesendeten Parametern für Bildschirmhöhe und -breite, und empfiehlt nur Elemente, die Mobilgeräte sind.

Betrachten Sie den folgenden Beispielaufruf zur Zielgruppe:

![Zielgruppe-Aufruf](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Auf der Seite, die ein Besucher anzeigt, werden Mobilgeräteprodukte angezeigt.

![Produkte für Mobilgeräte](/help/c-recommendations/c-algorithms/assets/phones.png)
