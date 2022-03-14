---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; dynamisch; Parameterübereinstimmung
description: Erfahren Sie, wie Sie in Adobe dynamisch filtern. [!DNL Target] Recommendations durch Vergleich von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).
title: Wie kann ich in Recommendations-Aktivitäten nach Parameterübereinstimmung filtern?
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 10%

---

# ![PREMIUM](/help/main/assets/premium.png) Parameterübereinstimmung

Dynamisches Filtern per Vergleich von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).

Beispielsweise nur empfohlene Inhalte, die mit dem Branchen-Seitenparameter übereinstimmen, oder andere Parameter wie Gerätedimensionen oder Geolokation, wie in den folgenden Beispielen dargestellt.

* Mbox-Parameter für Bildschirmbreite und -höhe können verwendet werden, um mobile Besucher anzusprechen und nur mobile Geräte und Zubehör zu empfehlen.
* Erstellen Sie eine Recommendations-Regel, die nur die am häufigsten verkauften Mobiltelefone zurückgibt, die mit der Bildschirmhöhe des Mobilgeräts übereinstimmen oder diese überschreiten, das der Besucher mit der Ansicht der Seite verwendet.
* Regionale Geostandortparameter können verwendet werden, um Empfehlungen für Tools während des Winters zurückzugeben. Schneeballdämmer und andere Schneemessungswerkzeuge können für Besucher in Bereichen empfohlen werden, in denen es schneit, aber nicht für Besucher in Gebieten empfohlen wird, in denen es nicht schneit.

>[!NOTE]
>
>Wenn die Aktivität vor dem 31. Oktober 2016 erstellt wurde, schlägt die Bereitstellung fehl, wenn der Filter &quot;Parameterübereinstimmung&quot;verwendet wird. So umgehen Sie das Problem:
>
>* Erstellen Sie eine neue Aktivität und fügen Sie Ihre Kriterien darin hinzu.
>* Verwenden Sie Kriterien, die den Filter „Parameterübereinstimmung“ nicht enthalten.
>* Entfernen Sie den Filter „Parameterübereinstimmung“ aus Ihren Kriterien.


## Beispiele für Parameterübereinstimmung

[!UICONTROL Parameterübereinstimmung] können Sie Inhalte empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Gerätedimensionen oder Geolokation, wie im folgenden Beispiel gezeigt:

[!DNL Recommendations] kann mit den Parameterwerten übereinstimmen, die in der [!DNL Target] aufrufen. In diesem Fall [!DNL Target] erkennt, dass ein Besucher ein Mobilgerät verwendet, basierend auf den Parametern für Bildschirmhöhe und -breite, die in der Variablen [!DNL Target] und empfiehlt nur Elemente, die Mobilgeräte sind.

Betrachten Sie den folgenden Beispiel-Target-Aufruf:

![Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Auf der Seite, die ein Besucher anzeigt, werden ihm Produkte für Mobilgeräte angezeigt.

![Mobilgeräteprodukte](/help/main/c-recommendations/c-algorithms/assets/phones.png)
