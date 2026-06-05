---
keywords: Recommendations; Recommendations-Aktivität; Kriterien; Algorithmus; Empfehlungsschlüssel; benutzerdefinierter Schlüssel; Branche; Vertikal; Einzelhandel; E-Commerce; Lead-Generierung; B2B; Finanzdienstleistungen; Medien; Publishing
description: Erfahren Sie, wie Sie in Adobe Kriterien verwenden [!DNL Target] [!DNL Recommendations].
title: Wie verwende ich Kriterien in  [!DNL Target] ?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
TQID: https://experienceleague.adobe.com/Wo7I3piBQ7zwYF7kqRphDeWjcBCpyvIvTkwKK0t0f9U
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 657
ht-degree: 7%

---

# [!UICONTROL Kriterien]

[!UICONTROL Kriterien] in [!DNL Adobe Target] [!DNL Recommendations] sind Regeln, die basierend auf einem vorab festgelegten Satz von Besucherverhalten bestimmen, welche Produkte oder Inhalte empfohlen werden sollen. Die Kriterien können auf angesagten Trends, dem aktuellen und früheren Verhalten eines Besuchers oder auf ähnlichen Produkten und Inhalten basieren. Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehrere Kriterien verwenden.

In den folgenden Abschnitten werden die Kriterienschlüssel und die Empfehlungslogik, die Sie für jeden Schlüssel verwenden können, ausführlicher erläutert. Klicken Sie auf die Links, um weitere Informationen zu erhalten.

## Vertikaler Markt {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Beim Erstellen eines Kriteriums wählen Sie basierend auf den Zielen Ihrer Recommendations-Aktivität eine Branche aus.

| Vertikaler Markt | Ziel |
|--- |--- |
| [!UICONTROL Retail/eCommerce] | Zum Kauf führende Konversion |
| [!UICONTROL Lead-Generierung/B2B/Finanzdienstleistungen] | Konversion ohne Kauf |
| [!UICONTROL Medien/Veröffentlichen] | Interaktion |

Andere Kriterienoptionen ändern sich je nach ausgewählter Branchen-Vertikale. Sie können die Standardbranchenhöhe auf der Seite **[!UICONTROL Administration] > [!UICONTROL Recommendations]** festlegen oder für jedes Kriterium die Branchenhöhe angeben.

## Algorithmentyp {#section_885B3BB1B43048A88A8926F6B76FC482}

Der ausgewählte Algorithmustyp bestimmt die verfügbaren Algorithmen.

In der folgenden Tabelle werden die verschiedenen Algorithmustypen und die zugehörigen Algorithmen erläutert.

| Algorithmustyp | Verwendungszeitpunkt | Verfügbare Algorithmen |
| --- | --- | --- |
| [!UICONTROL Warenkorbbasiert] | Empfehlungen auf der Grundlage des Warenkorbinhalts des Benutzers aussprechen. | <ul><li>[!UICONTROL Personen, die diese angesehen haben, haben auch Folgendes angesehen]</li><li>[!UICONTROL Personen, die diese angesehen haben, kauften auch]</li><li>[!UICONTROL Personen, die diese gekauft haben, kauften auch]</li></ul>Weitere Informationen finden Sie unter [Warenkorbbasiert](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Stützen der Empfehlung auf einen Empfehlungsschlüssel*. |
| [!UICONTROL Beliebtheitsbasiert] | Empfehlungen auf der Grundlage der allgemeinen Popularität eines Elements auf Ihrer Website oder auf der Grundlage der Popularität von Elementen innerhalb der Lieblings- oder am häufigsten angezeigten Kategorie, Marke, Genre usw. | <ul><li>[!UICONTROL Am häufigsten auf der Website angezeigt]</li><li>[!UICONTROL Am häufigsten angezeigt nach Kategorie]</li><li>[!UICONTROL Am häufigsten angezeigt nach Elementattribut]</li><li>[!UICONTROL Topverkäufe auf der Website]</li><li>[!UICONTROL Topverkäufe nach Kategorie]</li><li>[!UICONTROL Topverkäufe nach Artikelattribut]</li><li>[!UICONTROL Am besten nach Analytics-Metrik]</li></ul> |
| [!UICONTROL Elementbasiert] | Empfehlungen geben, basierend auf der Suche nach ähnlichen Elementen, die der Benutzer gerade anzeigt oder kürzlich angeschaut hat. | <ul><li>[!UICONTROL Personen, die dies angesehen haben, haben dies angesehen]</li><li>[!UICONTROL Leute, die das angesehen haben, kauften das]</li><li>[!UICONTROL Personen, die das gekauft haben, kauften das]</li><li>[!UICONTROL Elemente mit ähnlichen Attributen]</li></ul> |
| [!UICONTROL Benutzerbasiert] | Empfehlungen auf der Grundlage des Benutzerverhaltens aussprechen. | <ul><li>[!UICONTROL Vor Kurzem aufgerufene Artikel]</li><li>[!UICONTROL Empfohlen für Sie]</li></ul> |
| [!UICONTROL Benutzerdefinierte Kriterien] | Empfehlungen basierend auf einer benutzerdefinierten Datei geben, die Sie hochladen. | <ul><li>Benutzerdefinierter Algorithmus</li></ul> |

Weitere Informationen zu den einzelnen Algorithmen finden Sie unter [Stützen der Recommendation auf einen Recommendation-Schlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Verwenden eines benutzerdefinierten Empfehlungsschlüssels {#custom-key}

Sie können Empfehlungen auch auf dem Wert eines benutzerdefinierten Profilattributs basieren.

>[!NOTE]
>
>Benutzerdefinierte Profilparameter können über JavaScript, API oder Integrationen an [!DNL Target] übergeben werden. Weitere Informationen zu benutzerdefinierten Profilattributen finden Sie unter [Besucherprofile](/help/main/c-target/c-visitor-profile/visitor-profile.md).

Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Benutzer der Warteschlange zuletzt hinzugefügt hat.

1. Klicken Sie **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**.

1. Füllen Sie die Informationen im Abschnitt [Grundlegende Informationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Wählen Sie im Abschnitt [Empfohlener ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo)&quot; **[!UICONTROL Elementbasiert]** aus der Liste **[!UICONTROL Algorithmustyp]** aus.

1. Wählen Sie **[!UICONTROL Personen, die dies angesehen haben, das angezeigt haben]** aus der Liste **[!UICONTROL Algorithmus]** aus.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus der Liste **[!UICONTROL Empfehlungsschlüssel]** aus (z. B. [!UICONTROL Zuletzt angezeigt zur Watchlist hinzugefügt]).

## Anzeigen von Kriterieninformationen {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Sie können Details zu den Kriterien anzeigen, indem Sie auf die gewünschten Kriterien in der Spalte &quot;[!UICONTROL &quot; ].

In den **[!UICONTROL Attributen]** und Details können Sie allgemeine Informationen zu den ausgewählten Kriterien anzeigen, einschließlich [!UICONTROL Name], [!UICONTROL Beschreibung], [!UICONTROL Branche vertikal], [!UICONTROL Seitentypen], [!UICONTROL Empfehlungsschlüssel], [!UICONTROL Empfehlungslogik], [!UICONTROL Algorithmus-ID] und Informationen zur letzten Änderung (Datum und wer hat den Algorithmus geändert).

Im Abschnitt **[!UICONTROL Nutzung]** können Sie eine Liste der Aktivitäten anzeigen, die auf die ausgewählten Kriterien verweisen.

>[!NOTE]
>
>Die [!UICONTROL Algorithmusnutzung] wird derzeit nur für [!DNL Recommendations] Aktivitäten unterstützt. Diese Funktion wird derzeit nicht für [!UICONTROL A/B-]-, [!UICONTROL Automatische Zuordnung]-, [!UICONTROL Automatisches Targeting]- und [!UICONTROL Experience Targeting] (XT)-Aktivitäten unterstützt, die [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).
