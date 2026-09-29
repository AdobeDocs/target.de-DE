---
keywords: Einschlussregeln;Einschlusskriterien;Recommendations;Promotion;Promotions;dynamische Filterung;dynamische Parameterübereinstimmung
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Recommendations dynamisch filtern können, indem Sie Elemente (Entitäten) mit einem Wert in der Anfrage (API oder Mbox) vergleichen.
title: Wie filtere ich nach Parameterübereinstimmung in Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
TQID: 'https://experienceleague.adobe.com/GTli-O1p4Gm2Fg9J-L0ukQ8dSw2t-da8OatFLP8Ks9g'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '351'
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
