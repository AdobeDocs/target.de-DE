---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: Dynamische Filterung in Adobe Target Recommendations durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anforderung (API oder mbox).
title: Filtern nach Parameterübereinstimmung in Regeln für die dynamische Integration in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 27%

---


# ![PREMIUM](/help/assets/premium.png) -Parameterübereinstimmung

Dynamisches Filtern durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anforderung (API oder mbox).

Empfehlen Sie beispielsweise nur Inhalte, die mit dem Seitenparameter &quot;Branche&quot;oder anderen Parametern übereinstimmen, wie z. B. Geräteabmessungen oder Geolocation, wie in den folgenden Beispielen.

* Mbox-Parameter für Bildschirmbreite und -höhe können zur Zielgruppe von mobilen Besuchern und zur Empfehlung von Mobilgeräten und Zubehör verwendet werden.
* Regionale Geo-Positionsparameter können verwendet werden, um Empfehlungen für Tools während des Winters zurückzugeben. Schneeflocken und andere Schneefälle können für Besucher in Bereichen empfohlen werden, in denen es schneit, aber nicht für Besucher in Gebieten, in denen es nicht schneit.

>[!NOTE]
>
>Wenn die Aktivität vor dem 31. Oktober 2016 erstellt wurde, schlägt ihr Versand fehl, wenn der Filter &quot;Parameterübereinstimmung&quot;verwendet wird. So umgehen Sie das Problem:
>
>* Erstellen Sie eine neue Aktivität und fügen Sie Ihre Kriterien darin hinzu.
>* Verwenden Sie Kriterien, die den Filter „Parameterübereinstimmung“ nicht enthalten.
>* Entfernen Sie den Filter „Parameterübereinstimmung“ aus Ihren Kriterien.


Verfügbare Operatoren:

* gleich
* ist nicht gleich
* enthält
* „Enthält nicht“
* beginnt mit
* endet mit
* größer als oder gleich
* kleiner als oder gleich
* ist zwischen