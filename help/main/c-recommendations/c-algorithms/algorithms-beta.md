---
keywords: Empfehlungen; Empfehlungsaktivität; Kriterien; Algorithmus; Empfehlungsschlüssel; benutzerdefinierter Schlüssel; vertikaler Markt; Einzelhandel; E-Commerce; Lead-Generierung; b2b; Finanzdienste; Medien; Veröffentlichung
description: Erfahren Sie, wie Sie Kriterien in Adobe [!DNL Target] [!DNL Recommendations] verwenden.
title: Wie verwende ich Kriterien in [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 9c6ff35269a81aa0c2ea331985c6f5ddd5c8ccb3
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 7%

---

# [!UICONTROL Criteria]

[!UICONTROL Criteria] in [!DNL Adobe Target] [!DNL Recommendations] sind Regeln, die festlegen, welche Produkte oder Inhalte basierend auf einem vorab festgelegten Satz von Besucherverhalten empfohlen werden. Kriterien können auf beliebten Trends, dem aktuellen und früheren Verhalten eines Besuchers oder ähnlichen Produkten und Inhalten basieren. Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehrere Kriterien verwenden.

Die folgenden Abschnitte erläutern mehr über die Kriterienschlüssel und die Empfehlungslogik, die Sie für jeden Schlüssel verwenden können. Klicken Sie auf die Links, um weitere Informationen anzuzeigen.

## Vertikaler Markt {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Beim Erstellen eines Kriteriums wählen Sie basierend auf den Zielen Ihrer Recommendations-Aktivität einen vertikalen Markt aus.

| Vertikaler Markt | Ziel |
|--- |--- |
| [!UICONTROL Retail/Ecommerce] | Zum Kauf führende Konversion |
| [!UICONTROL Lead Generation/B2B/Financial Services] | Konversion ohne Kauf |
| [!UICONTROL Media/Publishing] | Interaktion |

Andere Optionen für Kriterien ändern sich je nach vertikalem Markt, den Sie auswählen. Sie können Ihre standardmäßige vertikale Branche auf der Seite **[!UICONTROL Administration]>[!UICONTROL Recommendations]** festlegen oder für jedes Kriterium den vertikalen Markt angeben.

## Algorithmentyp {#section_885B3BB1B43048A88A8926F6B76FC482}

Der ausgewählte Algorithmustyp bestimmt die verfügbaren Algorithmen.

![Kriterienseite](assets/criteria-page-new.png)

In der folgenden Tabelle werden die verschiedenen Algorithmustypen und die zugehörigen Algorithmen erläutert.

| Algorithmustyp | Verwendungsbereiche | Verfügbare Algorithmen |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Machen Sie Empfehlungen basierend auf den Inhalten des Warenkorbs des Benutzers. | <ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul>Weitere Informationen finden Sie unter [Warenkorb-basiert](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Stützen der Empfehlung auf einen Empfehlungsschlüssel*. |
| [!UICONTROL Popularity-Based] | Machen Sie Empfehlungen basierend auf der allgemeinen Beliebtheit eines Artikels auf Ihrer Site oder auf der Beliebtheit von Artikeln in der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. eines Benutzers. | <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | Empfehlungen aussprechen, die darauf basieren, ähnliche Artikel wie ein Artikel zu finden, den der Benutzer gerade ansieht oder kürzlich angesehen hat. | <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | Empfehlungen basierend auf dem Benutzerverhalten erstellen. | <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
| [!UICONTROL Custom Criteria] | Machen Sie Empfehlungen basierend auf einer benutzerdefinierten Datei, die Sie hochladen. | <ul><li>Benutzerspezifischer Algorithmus</li></ul> |

Weitere Informationen zu den einzelnen Algorithmen finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Verwenden eines benutzerdefinierten Empfehlungsschlüssels {#custom-key}

Sie können Empfehlungen auch auf dem Wert eines benutzerdefinierten Profilattributs basieren.

>[!NOTE]
>
>Benutzerdefinierte Profilparameter können über JavaScript, API oder Integrationen an [!DNL Target] übergeben werden. Weitere Informationen zu benutzerdefinierten Profilattributen finden Sie unter [Besucherprofile](/help/main/c-target/c-visitor-profile/visitor-profile.md).

Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Benutzer zuletzt zur Warteschlange hinzugefügt hat.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Füllen Sie die Informationen im Abschnitt [Grundlegende Informationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Wählen Sie im Abschnitt [Empfohlener Algorithmus](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) **[!UICONTROL Item Based]** aus der Liste **[!UICONTROL Algorithm Type]** aus.

1. Wählen Sie **[!UICONTROL People Who Viewed This, Viewed That]** aus der Liste **[!UICONTROL Algorithm]** aus.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Liste **[!UICONTROL Recommendation Key]** aus (z. B. [!UICONTROL Last Show Added to Watchlist]).

## Anzeigen von Kriterieninformationen {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Sie können Kriteriendetails anzeigen, indem Sie auf die gewünschten Kriterien in der Spalte [!UICONTROL Name] klicken.

![Bewegen des Mauszeigers über die Kriterienkarte](/help/main/c-recommendations/c-algorithms/assets/criteria-hover.png)

Auf der Registerkarte **[!UICONTROL Algorithm Info]** können Sie allgemeine Informationen zu den ausgewählten Kriterien anzeigen, einschließlich der [!UICONTROL Name], [!UICONTROL Description], [!UICONTROL Industry Vertical], [!UICONTROL Page Types], [!UICONTROL Recommendation Key], [!UICONTROL Recommendation Logic], [!UICONTROL Algorithm ID] und der zuletzt geänderten Informationen (Datum und Benutzer, die den Algorithmus geändert haben).

Im Abschnitt **[!UICONTROL Algorithm Usage]** können Sie eine Liste der Aktivitäten anzeigen, die auf die ausgewählten Kriterien verweisen.

>[!NOTE]
>
>Die Funktion [!UICONTROL Algorithm Usage] wird derzeit nur für [!DNL Recommendations] -Aktivitäten unterstützt. Diese Funktion wird derzeit nicht für die Aktivitäten [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] und [!UICONTROL Experience Targeting] (XT) unterstützt, die [Empfehlungen als Angebot enthalten](/help/main/c-recommendations/recommendations-as-an-offer.md).