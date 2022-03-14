---
keywords: Empfehlungen; Empfehlungsaktivität; Kriterien; Algorithmus; Empfehlungsschlüssel; benutzerdefinierter Schlüssel; vertikaler Markt; Einzelhandel; E-Commerce; Lead-Generierung; b2b; Finanzdienste; Medien; Veröffentlichung
description: Erfahren Sie, wie Sie Kriterien in Adobe verwenden [!DNL Target] [!DNL Recommendations].
title: Wie verwende ich Kriterien in [!DNL Target] Recommendations?
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 24%

---

# ![PREMIUM](/help/main/assets/premium.png) Kriterien

Kriterien in [!DNL Adobe Target] [!DNL Recommendations] sind Regeln, die festlegen, welche Produkte oder Inhalte basierend auf einem vorab festgelegten Satz von Besucherverhalten empfohlen werden. Die Kriterien können auf angesagten Trends, dem aktuellen und früheren Verhalten eines Besuchers oder auf ähnlichen Produkten und Inhalten basieren. Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehrere Kriterien verwenden.

In den folgenden Abschnitten werden mehr über Kriterienschlüssel und die Empfehlungslogik erläutert, die Sie für jeden Schlüssel verwenden können. Klicken Sie auf die Links, um weitere Informationen anzuzeigen.

## Vertikaler Markt {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Beim Erstellen eines Kriteriums wählen Sie basierend auf den Zielen Ihrer Recommendations-Aktivität einen vertikalen Markt aus.

| Vertikaler Markt | Ziel |
|--- |--- |
| Einzelhandel/E-Commerce | Zum Kauf führende Konversion |
| Lead-Generierung/B2B/Finanzdienstleistungen | Konversion ohne Kauf |
| Medien/Verlagswesen | Interaktion |

Andere Optionen für Kriterien ändern sich je nach vertikalem Markt, den Sie auswählen. Sie können Ihren standardmäßigen vertikalen Markt auf die Variable **[!UICONTROL Recommendations > Einstellungen]** oder Sie können für jedes Kriterium den vertikalen Markt angeben.

## Algorithmentyp {#section_885B3BB1B43048A88A8926F6B76FC482}

Der ausgewählte Algorithmustyp bestimmt die verfügbaren Algorithmen. Es gibt mehrere Algorithmustypen, die beim Einrichten einer [!DNL Recommendations] Aktivität.

![Kriterienseite](assets/criteria-page.png)

In der folgenden Tabelle werden die verschiedenen Algorithmustypen und die zugehörigen Algorithmen erläutert.

| Algorithmustyp | Verwendungsbereiche | Verfügbare Algorithmen |
| --- | --- | --- |
| [!UICONTROL Warenkorbbasiert] | Machen Sie Empfehlungen basierend auf den Inhalten des Warenkorbs des Benutzers. | <ul><li>Personen, die diese ansahen, sahen auch</li><li>Personen, die diese ansahen, kauften diese</li><li>Personen, die diese kauften, kauften diese</li></ul>Weitere Informationen finden Sie unter [Warenkorbbasiert](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Stützen der Empfehlung auf einen Empfehlungsschlüssel*. |
| [!UICONTROL Popularitätsbasiert] | Machen Sie Empfehlungen basierend auf der allgemeinen Beliebtheit eines Artikels auf Ihrer Site oder auf der Beliebtheit von Artikeln in der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. eines Benutzers. | <ul><li>Am häufigsten angezeigt auf der gesamten Site</li><li>Am häufigsten angezeigt nach Kategorie</li><li>Am häufigsten nach Elementattribut angezeigt</li><li>Topverkäufe auf der gesamten Site</li><li>Topverkäufe nach Kategorie</li><li>Topverkäufe nach Elementattribut</li><li>Top nach Analytics-Metrik</li></ul> |
| [!UICONTROL Artikelbasiert] | Empfehlungen aussprechen, die darauf basieren, ähnliche Artikel wie ein Artikel zu finden, den der Benutzer gerade ansieht oder kürzlich angesehen hat. | <ul><li>Personen, die das ansahen, sahen auch dies an</li><li>Personen, die das ansahen, kauften dies</li><li>Personen, die das kauften, kauften dies</li><li>Elemente mit ähnlichen Attributen</li></ul> |
| [!UICONTROL Benutzerbasiert] | Empfehlungen basierend auf dem Benutzerverhalten erstellen. | <ul><li>Vor Kurzem aufgerufene Artikel </li><li>Empfohlen für Sie</li></ul> |
| [!UICONTROL Benutzerdefinierte Kriterien] | Machen Sie Empfehlungen basierend auf einer von Ihnen hochgeladenen benutzerdefinierten Datei. | <ul><li>Benutzerspezifischer Algorithmus</li></ul> |

Weitere Informationen zu den einzelnen Algorithmen finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Verwenden eines benutzerdefinierten Empfehlungsschlüssels {#custom-key}

Sie können Empfehlungen auch auf dem Wert eines benutzerdefinierten Profilattributs basieren.

>[!NOTE]
>
>Benutzerdefinierte Profilparameter können an [!DNL Target] über JavaScript, API oder Integrationen. Weitere Informationen zu benutzerdefinierten Profilattributen finden Sie unter [Besucherprofile](/help/main/c-target/c-visitor-profile/visitor-profile.md).

Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Benutzer zuletzt zur Warteschlange hinzugefügt hat.

1. Klicken **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken **[!UICONTROL Erstellen von Kriterien]** > **[!UICONTROL Erstellen von Kriterien]**.

1. Füllen Sie die Informationen im [Abschnitt &quot;Grundlegende Informationen&quot;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Im [Empfohlener Algorithmus](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) Bereich, wählen Sie **[!UICONTROL Artikelbasiert]** von **[!UICONTROL Algorithmustyp]** Liste.

1. Auswählen **[!UICONTROL Personen, die das ansahen, sahen auch dies an]** von **[!UICONTROL Algorithmus]** Liste.

1. Wählen Sie Ihr benutzerdefiniertes Profilattribut aus dem **[!UICONTROL Empfehlungsschlüssel]** list (z. B. [!UICONTROL Zuletzt zur Watchlist hinzugefügt]).

   ![Neues Kriterium erstellen, Dialogfeld](assets/custom-key1.png)

## Anzeigen von Kriterieninformationen {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Sie können Kriteriendetails auf einer Popupkarte anzeigen, indem Sie mit dem Mauszeiger über eine Karte fahren und auf das Informationssymbol einer Kriterienkarte klicken, ohne das Kriterium zu öffnen.

![Bewegen des Mauszeigers über die Kriterienkarte](/help/main/c-recommendations/c-algorithms/assets/criteria_hover.png)

Klicken Sie auf die Registerkarte **[!UICONTROL Algorithmusinformationen]**, um allgemeine Informationen zu den ausgewählten Kriterien anzuzeigen, einschließlich Name, Beschreibungen, vertikalen Markt, Seitentyp(en), Empfehlungsschlüssel, Empfehlungslogik und Algorithmus-ID.

![Registerkarte „Algorithmusinformationen“](/help/main/c-recommendations/c-algorithms/assets/criteria_info.png)

Klicken Sie auf die Registerkarte **[!UICONTROL Algorithmusnutzung]**, um eine Liste der Aktivitäten anzuzeigen, die das ausgewählte Kriterium verwenden. Auf der Karte werden aktive, inaktive und Entwurfsaktivitäten aufgelistet. Klicken Sie auf die Dropdownlisten Live-Aktivitäten/Inaktive Aktivitäten/Entwurfsaktivitäten , um die gesamte Liste der Aktivitäten anzuzeigen, die auf dieses Kriterium verweisen. Sie können auf einen Aktivitätslink klicken, um die Aktivität zur Bearbeitung zu öffnen.

![Registerkarte &quot;Algorithmusnutzung&quot;](/help/main/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>Die [!UICONTROL Algorithmusverwendung] -Funktion wird derzeit nur für Recommendations-Aktivitäten unterstützt. Diese Funktion wird derzeit nicht für A/B-Test-, Automatisch zuweisende, automatische Targeting- und Erlebnis-Targeting-Aktivitäten (XT) unterstützt, die Folgendes enthalten: [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).
