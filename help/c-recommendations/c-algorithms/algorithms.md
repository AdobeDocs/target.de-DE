---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Kriterien in Adobe Target sind Regeln, die festlegen, welche Produkte oder Inhalte auf der Grundlage eines vordefinierten Verhaltens von Besuchern empfohlen werden.
title: Kriterien in Adobe Target Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 53%

---


# ![PREMIUM](/help/assets/premium.png) Kriterien

Kriterien in [!DNL Adobe Target] sind Regeln, die festlegen, welche Besucher oder Inhalte basierend auf einem vordefinierten Satz von Verhaltensweisen empfohlen werden. Die Kriterien können auf angesagten Trends, dem aktuellen und früheren Verhalten eines Besuchers oder auf ähnlichen Produkten und Inhalten basieren. Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehrere Kriterien verwenden.

Die folgenden Abschnitte erläutern mehr über Kriterienkombinationen und die Empfehlungslogik, die Sie für jeden Schlüssel verwenden können. Klicken Sie auf die Links, um weitere Informationen anzuzeigen.

## Vertikaler Markt {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Beim Erstellen eines Kriteriums wählen Sie eine Branche auf der Grundlage der Ziele Ihrer Recommendations-Aktivität aus.

| Vertikaler Markt | Ziel |
|--- |--- |
| Einzelhandel/E-Commerce | Zum Kauf führende Konversion |
| Lead-Generierung/B2B/Finanzdienstleistungen | Konversion ohne Kauf |
| Medien/Verlagswesen | Interaktion |

Andere Kriterienoptionen ändern sich je nach ausgewählter Branchenzahl. Sie können die Standardbranchenvertikale Einstellung auf der Seite **[!UICONTROL Recommendations > Settings]** oder die Branche für jedes Kriterium festlegen.

## Empfehlungsschlüssel {#section_885B3BB1B43048A88A8926F6B76FC482}

Der ausgewählte Empfehlungsschlüssel bestimmt den Kriterientyp. Es gibt viele Kriterientypen. Sie werden beim Einrichten einer [!DNL Recommendations]-Aktivität als Kriterienkarten dargestellt.

![Kriterienseite](/help/c-recommendations/c-algorithms/assets/criteria-page.png)

In der folgenden Tabelle werden die verschiedenen Kriterientypen und die zugehörigen Schlüssel erläutert. Klicken Sie auf die Links, um detaillierte Informationen zu den einzelnen Schlüsseln anzuzeigen.

| Kriterientyp | Schlüssel |
|--- |--- |
| Aktuelle Seitenaktivität | Empfehlen Sie Artikel auf Basis des Verhaltens der Benutzer auf der aktuellen Seite. Zum Beispiel möchten Besucher, die einen bestimmten Artikel ansehen, möglicherweise andere Artikel derselben Kategorie ansehen.<ul><li>[Aktueller Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Aktuelle Kategorie](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| Benutzerspezifisch | Empfohlene Artikel auf Grundlage benutzerspezifischer Attribute<ul><li>[Benutzerspezifisches Attribut ](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>Wenn Sie Empfehlungen auf Grundlage von benutzerspezifischen Attributen erstellen, müssen Sie das benutzerspezifische Attribut auswählen und anschließend den Empfehlungstyp festlegen. |
| Vergangenes Verhalten | Empfehlen Sie Artikel auf Basis früherer Reaktionen von Besuchern auf Artikel. Zum Beispiel ist die Wahrscheinlichkeit höher, dass Personen, die sich für eine bestimmte Marke entschieden haben, weitere Artikel dieser Marke kaufen.<ul><li>[Zuletzt gekaufter Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Zuletzt angezeigter Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Am häufigsten angezeigter Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[Favoritenkategorie](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| Beliebtheit | Empfehlen Sie die beliebtesten Artikel, wie zum Beispiel die beliebtesten Videos in einer verwandten Kategorie oder Produkte, die auf Ihrer Site am häufigsten angezeigt wurden.<ul><li>[Beliebtheit](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| [Vor Kurzem aufgerufene Artikel ](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed) | Empfehlen Sie Artikel, die ein Besucher zuletzt aufgerufen hat, z. B. Artikel, die ein Besucher beim letzten Besuch Ihrer Site angesehen hat, oder Artikel, die momentan am meisten im Trend liegen. |

## Verwenden eines benutzerdefinierten Empfehlungsschlüssels {#custom-key}

Sie können Empfehlungen auch auf dem Wert eines benutzerspezifischen Profil-Attributs basieren.

>[!NOTE]
>
>Benutzerdefinierte Profil-Parameter können über JavaScript, API oder Integrationen an die Zielgruppe übergeben werden. Weitere Informationen zu benutzerdefinierten Profil-Attributen finden Sie unter [Besucher-Profil](/help/c-target/c-visitor-profile/visitor-profile.md).

Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Benutzer der Warteschlange zuletzt hinzugefügt hat.

1. Wählen Sie Ihr benutzerdefiniertes Profil-Attribut aus der Dropdown-Liste [!UICONTROL Empfehlungsschlüssel] aus (z. B. [!UICONTROL Letzte Anzeige hinzugefügt zur Watchlist]).

1. Wählen Sie die [!UICONTROL Empfehlungslogik] aus (z. B. [!UICONTROL Personen, die dies angezeigt haben, sahen dies] an).

   ![Neues Kriterium erstellen, Dialogfeld](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

Wenn Ihr benutzerdefiniertes Profil-Attribut nicht direkt mit einer Entitäts-ID übereinstimmt, müssen Sie [!DNL Recommendations] erklären, wie die Übereinstimmung mit einer Entität erfolgen soll.

Nehmen wir beispielsweise an, Sie möchten die Artikel mit den besten Verkäufen von der Lieblingsmarke eines Benutzers anzeigen.

1. Wählen Sie Ihr benutzerdefiniertes Profil-Attribut aus der Dropdown-Liste [!UICONTROL Empfehlungsschlüssel] (z. B. [!UICONTROL Favoritenmarke]).

1. Wählen Sie die [!UICONTROL Empfehlungslogik] aus, die Sie mit diesem Schlüssel verwenden möchten (z. B. [!UICONTROL Topverkäufe]).

   Die Option [!UICONTROL Gruppieren nach individuellem Wert] wird angezeigt.

1. Wählen Sie das Entitätsattribut aus, das dem ausgewählten Schlüssel entspricht. In diesem Fall stimmt [!UICONTROL Favoritenmarke] mit `entity.brand` überein.

   [!DNL Recommendations] erstellt nun eine &quot;Topverkäufe&quot;-Liste für jede Marke und zeigt dem Benutzer die passende &quot;Topverkäufe&quot;-Liste basierend auf dem im Attribut  [!UICONTROL Favorite ] Brandprofile gespeicherten Wert.

   ![Attribut &quot;Topverkäufe&quot;](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Kriterien/Algorithmen {#criteria-algorithms}

[!DNL Target Recommendations] verwendet komplexe Algorithmen, um zu ermitteln, wann die Aktionen eines Benutzers den für Ihre Aktivität festgelegten Kriterien entsprechen. Der Empfehlungsschlüssel bestimmt die verfügbaren Optionen der Empfehlungslogik.

| Kriterien | Beschreibung |
|--- |--- |
| [Artikel/Medien mit ähnlichen Attributen](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#similar-attributes) | Empfiehlt auf Grundlage von aktueller Seitenaktivität oder früherem Besucherverhalten Artikel oder Medien, die eine Ähnlichkeit zu anderen Artikeln oder Medien aufweisen. |
| [Personen, die das ansahen, sahen auch dies an](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-viewed) | Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. |
| [Personen, die das ansahen, kauften dies](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-bought) | Empfiehlt die Artikel, die am häufigsten von Kunden in derselben Sitzung angesehen werden, in der der angegebene Artikel angesehen wird. |
| [Personen, die das kauften, kauften dies](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#bought-bought) | Empfiehlt Artikel, die am häufigsten von Kunden zur selben Zeit gekauft werden, wie der angegebene Artikel. |
| [Site-Affinität](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#site-affinity) | Empfiehlt Artikel auf Grundlage der Wahrscheinlichkeit eines Zusammenhangs zwischen Artikeln. |
| [Topverkäufe](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#top-sellers) | Die Artikel, die in den meisten abgeschlossenen Bestellungen enthalten sind Wenn derselbe Artikel in einer Bestellung mehrmals bestellt wurde, zählt dies als eine Bestellung. |
| [Am häufigsten angezeigt](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed) | Die am häufigsten angezeigten Artikel oder Medien |
| [Benutzerbasiertes Recommendations](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based) | Empfiehlt Artikel basierend auf dem Browsen, Anzeigen und Kaufverlauf jedes Besuchers. Diese Elemente werden allgemein als &quot;Empfohlen für Sie&quot;bezeichnet. |

>[!NOTE]
>
>Wenn Sie eine Empfehlung ausführen und deren Kriterien ändern, verlieren Sie Ihre Berichtsdaten.

Sie können auch zusätzliche bekannte Informationen über einen Besucher verwenden, um Ihre Empfehlungen zu verbessern.

Alle eintägigen Kriterien werden zweimal täglich ausgeführt. Alle einwöchigen und längeren Kriterien werden einmal täglich ausgeführt. Site-Affinitätskriterien werden einmal täglich ausgeführt. Reservekriterien werden zweimal täglich ausgeführt.

## Anzeigen von Kriterieninformationen {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Sie können Kriteriendetails auf einer Popupkarte anzeigen, indem Sie mit dem Mauszeiger über eine Karte fahren und auf das Informationssymbol einer Kriterienkarte klicken, ohne das Kriterium zu öffnen.

![Bewegen des Mauszeigers über die Kriterienkarte](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Klicken Sie auf die Registerkarte **[!UICONTROL Algorithmusinformationen]**, um allgemeine Informationen zu den ausgewählten Kriterien anzuzeigen, einschließlich Name, Beschreibungen, vertikalen Markt, Seitentyp(en), Empfehlungsschlüssel, Empfehlungslogik und Algorithmus-ID.

![Registerkarte „Algorithmusinformationen“](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Klicken Sie auf die Registerkarte **[!UICONTROL Algorithmusnutzung]**, um eine Liste der Aktivitäten anzuzeigen, die das ausgewählte Kriterium verwenden. Die Karte wird aktiv, inaktiv und als Entwurf von Aktivitäten Liste. Klicken Sie auf die Dropdown-Listen Live-Aktivitäten/Inaktive Aktivitäten/Aktivitäten-Entwürfe, um die gesamte Liste von Aktivitäten, die auf dieses Kriterium verweisen, Ansicht. Sie können auf einen Aktivitätslink klicken, um die Aktivität zur Bearbeitung zu öffnen.

![Registerkarte &quot;Algorithmusverwendung&quot;](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>Die Funktion [!UICONTROL Algorithmusverwendung] wird derzeit nur für Recommendations-Aktivitäten unterstützt. Diese Funktion wird derzeit nicht für Aktivitäten von A/B-Tests, automatisierter Zuordnung, automatischer Zielgruppe und Erlebnis-Targeting (XT) unterstützt, die [Recommendations als Angebot](/help/c-recommendations/recommendations-as-an-offer.md) enthalten.
