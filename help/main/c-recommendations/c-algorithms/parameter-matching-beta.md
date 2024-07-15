---
keywords: Einschlussregeln; Einschlusskriterien; Empfehlungen; Promotion; Promotions; dynamische Filterung; dynamisch; Parameterübereinstimmung
description: Erfahren Sie, wie Sie in Adobe [!DNL Target] Recommendations dynamisch filtern können, indem Sie Elemente (Entitäten) mit einem Wert in der Anfrage (API oder Mbox) vergleichen.
title: Wie kann ich in Recommendations-Aktivitäten nach Parameterübereinstimmung filtern?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6a55260fd49e07e2b217f6becfbc778251a5d0d
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 10%

---

# [!UICONTROL Parameter Matching]

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

Mit [!UICONTROL Parameter Matching] können Sie Inhalte empfehlen, die mit den Seitenparametern oder den Parametern des Besuchers übereinstimmen, z. B. Gerätedimensionen oder Geolokation, wie im folgenden Beispiel gezeigt:

[!DNL Recommendations] kann mit den Parameterwerten übereinstimmen, die im [!DNL Target] -Aufruf gesendet werden. In diesem Fall erkennt [!DNL Target], dass ein Besucher ein Mobilgerät verwendet, basierend auf den Parametern für Bildschirmhöhe und -breite, die im [!DNL Target] -Aufruf gesendet werden, und empfiehlt nur Elemente, die Mobilgeräte sind.

Betrachten Sie den folgenden Beispiel-Target-Aufruf:

![Target-Aufruf](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

Auf der Seite, die ein Besucher anzeigt, werden ihm Produkte für Mobilgeräte angezeigt.

![Mobilgeräte-Produkte](/help/main/c-recommendations/c-algorithms/assets/phones.png)