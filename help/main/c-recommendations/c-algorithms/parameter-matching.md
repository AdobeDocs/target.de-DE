---
keywords: Einschlussregeln;Einschlusskriterien;Recommendations;Promotion;Promotions;dynamische Filterung;dynamische Parameterübereinstimmung
description: Erfahren Sie, wie Sie in Adobe/ [!DNL Target]  dynamisch filtern können, indem Sie Elemente (Entitäten) mit einem Wert in der Anfrage (API oder Mbox) vergleichen.
title: Wie filtere ich nach Parameterübereinstimmung in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
TQID: https://experienceleague.adobe.com/GTli-O1p4Gm2Fg9J-L0ukQ8dSw2t-da8OatFLP8Ks9g
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 10%

---

# [!UICONTROL Parameterübereinstimmung]

Dynamisches Filtern durch Vergleichen von Elementen (Entitäten) mit einem Wert in der Anfrage (API oder Mbox).

Empfehlen Sie beispielsweise nur Inhalte, die dem Seitenparameter „Branche“ oder anderen Parametern wie Geräteabmessungen oder Geografie entsprechen, wie in den folgenden Beispielen dargestellt.

* Mbox-Parameter für Bildschirmbreite und -höhe können verwendet werden, um mobile Besucher anzusprechen und nur Mobilgeräte und Zubehör zu empfehlen.
* Erstellen Sie eine Recommendations-Regel, die nur die meistverkauften Mobiltelefone zurückgibt, die mit der Bildschirmhöhe des Mobilgeräts, das der Besucher verwendet, übereinstimmen oder diese überschreiten.
* Regionale Standortparameter können verwendet werden, um im Winter Empfehlungen für Werkzeuge zurückzugeben. Schneefräsen und andere Schneeminderungswerkzeuge können für Besucher in Gebieten empfohlen werden, in denen es schneit, aber nicht für Besucher in Gebieten, in denen es nicht schneit.

>[!NOTE]
>
>Wenn die Aktivität vor dem 31. Oktober 2016 erstellt wurde, schlägt der Versand fehl, wenn der Filter „Parameterübereinstimmung“ verwendet wird. So umgehen Sie das Problem:
>
>* Erstellen Sie eine neue Aktivität und fügen Sie Ihre Kriterien darin hinzu.
>* Verwenden Sie Kriterien, die den Filter „Parameterübereinstimmung“ nicht enthalten.
>* Entfernen Sie den Filter „Parameterübereinstimmung“ aus Ihren Kriterien.

## Beispiele für Parameterübereinstimmung

Mit [!UICONTROL Parameterübereinstimmung] können Sie Inhalte empfehlen, die den Seitenparametern oder den Parametern des Besuchers entsprechen, z. B. Geräteabmessungen oder Geografie, wie im folgenden Beispiel gezeigt:

[!DNL Recommendations] können mit Parameterwerten übereinstimmen, die im [!DNL Target] Aufruf gesendet werden. In diesem Fall erkennt [!DNL Target] anhand der Parameter Bildschirmhöhe und Breite, die im [!DNL Target] Aufruf gesendet werden, dass ein Besucher ein Mobilgerät verwendet, und empfiehlt nur Elemente, die Mobilgeräte sind.

Betrachten Sie das folgende Beispiel für einen Target-Aufruf:

![Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Auf der Seite, die ein Besucher anzeigt, werden ihm Produkte für Mobilgeräte angezeigt.

![Produkte für Mobilgeräte](/help/main/c-recommendations/c-algorithms/assets/phones.png)
