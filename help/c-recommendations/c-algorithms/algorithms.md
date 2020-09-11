---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Kriterien in Adobe Target Recommendations sind Regeln, die festlegen, welche Produkte basierend auf einem vordefinierten Besucher-Verhalten empfohlen werden.
title: Kriterien in Adobe Target Recommendations
feature: criteria
uuid: 738db164-174b-45b8-bb8a-778f6494f1d7
translation-type: tm+mt
source-git-commit: 55f0791bb68fc98e319fa70a647e5168ac72ae1e
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 69%

---


# ![PREMIUM](/help/assets/premium.png) Kriterien

Kriterien sind Regeln, die auf Basis vorab ermittelter Verhaltensweisen von Besuchern festlegen, welche Produkte empfohlen werden.

Kriterien bestimmen, welche Aktion zu welcher Empfehlung führt. Sie können mehrere Empfehlungstypen untereinander testen, indem Sie mehrere Kriterien verwenden.

## Vertikaler Markt {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Wählen Sie einen vertikalen Markt auf Grundlage der Ziele Ihrer Empfehlungsaktivität aus. Je nach ausgewählter Branchenstufe,

| Vertikaler Markt | Ziel |
|--- |--- |
| Einzelhandel/E-Commerce | Zum Kauf führende Konversion |
| Lead-Generierung/B2B/Finanzdienstleistungen | Konversion ohne Kauf |
| Medien/Verlagswesen | Interaktion |

## Recommendation key {#section_885B3BB1B43048A88A8926F6B76FC482}

Der ausgewählte Empfehlungsschlüssel bestimmt den Kriterientyp. Es gibt viele Kriterientypen. Sie werden beim Einrichten einer [!DNL Recommendations]-Aktivität als Kriterienkarten dargestellt.

| Kriterientyp | Schlüssel |
|--- |--- |
| Aktuelle Seitenaktivität | Empfehlen Sie Artikel auf Basis des Verhaltens der Benutzer auf der aktuellen Seite. Zum Beispiel möchten Besucher, die einen bestimmten Artikel ansehen, möglicherweise andere Artikel derselben Kategorie ansehen.<ul><li>[Aktueller Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Aktuelle Kategorie](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| Benutzerspezifisch | Empfohlene Artikel auf Grundlage benutzerspezifischer Attribute<ul><li>[Benutzerspezifisches Attribut ](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>Wenn Sie Empfehlungen auf Grundlage von benutzerspezifischen Attributen erstellen, müssen Sie das benutzerspezifische Attribut auswählen und anschließend den Empfehlungstyp festlegen. |
| Vergangenes Verhalten | Empfehlen Sie Artikel auf Basis früherer Reaktionen von Besuchern auf Artikel. Zum Beispiel ist die Wahrscheinlichkeit höher, dass Personen, die sich für eine bestimmte Marke entschieden haben, weitere Artikel dieser Marke kaufen.<ul><li>[Zuletzt gekaufter Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Zuletzt angezeigter Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Am häufigsten angezeigter Artikel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[Favoritenkategorie](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| Beliebtheit | Empfehlen Sie die beliebtesten Artikel, wie zum Beispiel die beliebtesten Videos in einer verwandten Kategorie oder Produkte, die auf Ihrer Site am häufigsten angezeigt wurden.<ul><li>[Beliebtheit](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| Vor Kurzem aufgerufene Artikel | Die Artikel empfehlen, die der Besucher vor Kurzem aufgerufen hat, wie zum Beispiel Artikel, die er oder sie sich bei seinem letzten Besuch auf Ihrer Website angesehen hat, oder Artikel, die momentan am meisten im Trend liegen.<br>Der Algorithmus „Kürzlich angezeigte Elemente“ liefert Ergebnisse, die spezifisch für die Aktivität eines Besuchers in einer [Umgebung](/help/administrating-target/hosts.md) sind. Wenn zwei Sites zu unterschiedlichen Umgebungen gehören und ein Besucher zwischen den beiden Sites wechselt, gibt der Algorithmus nur die jeweiligen Elemente der entsprechenden Site zurück.<br>Dieser Kriterientyp wird nicht durch Sammlungen beschränkt.<ul><li>[Vor Kurzem aufgerufene Artikel ](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed)</li></ul>**Hinweis:** Sie können die Kriterien für kürzlich angesehene Elemente nicht für Backup-Recommendations verwenden.<br>„Kürzlich angezeigte Elemente/Medien“ kann so gefiltert werden, dass nur Elemente mit einem bestimmten Attribut angezeigt werden.<ul><li>Kürzlich angesehene Kriterien können analog zu anderen Kriterien in Empfehlungen konfiguriert werden.</li><li>Sie können [Sammlungen](/help/c-recommendations/c-products/collections.md), [Ausschlüsse](/help/c-recommendations/c-products/exclusions.md) und [Einschlüsse](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (einschließlich der speziellen Regeln für „Preis“ und „Bestand“) können auf die gleiche Weise wie alle anderen Kriterien genutzt werden.</li></ul>Mögliche Nutzungsszenarien:<ul><li>In einer multinationalen Firma mit mehreren Unternehmen zeigt möglicherweise ein Besucher Elemente über mehrere digitale Eigenschaften hinweg an. In diesem Fall können Sie die kürzlich angezeigten Elemente so begrenzen, dass nur die entsprechende Eigenschaft angezeigt wird, wo sie angezeigt wurden. Dadurch wird verhindert, dass kürzlich angezeigte Elemente für die Site einer anderen digitalen Eigenschaft angezeigt werden.</li></ul> |

## Verwenden eines benutzerdefinierten Empfehlungsschlüssels {#custom-key}

Sie können Empfehlungen auch auf dem Wert eines benutzerspezifischen Profil-Attributs basieren.

>[!NOTE]
>
>Benutzerdefinierte Profil-Parameter können über JavaScript, API oder Integrationen an die Zielgruppe übergeben werden. Weitere Informationen zu benutzerdefinierten Profil-Attributen finden Sie unter [Besucher-Profil](/help/c-target/c-visitor-profile/visitor-profile.md).

Angenommen, Sie möchten empfohlene Filme basierend auf dem Film anzeigen, den ein Benutzer der Warteschlange zuletzt hinzugefügt hat.

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Last Show Added to Watchlist]).

1. Select your [!UICONTROL Recommendation Logic] (for example, [!UICONTROL People Who Viewed This, Viewed That]).

   ![Neues Kriterium erstellen, Dialogfeld](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

If your custom profile attribute does not directly match to a single entity ID, it is necessary to explain to [!DNL Recommendations] how you want the match to an entity to occur.

Nehmen wir beispielsweise an, Sie möchten die Artikel mit den besten Verkäufen von der Lieblingsmarke eines Benutzers anzeigen.

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Favorite Brand]).

1. Select the [!UICONTROL Recommendation Logic] you want to use with this key (for example, [!UICONTROL Top Sellers]).

   Die Option [!UICONTROL Gruppieren nach individuellem Wert] wird angezeigt.

1. Wählen Sie das Entitätsattribut aus, das dem ausgewählten Schlüssel entspricht. In this case [!UICONTROL Favorite Brand] matches to `entity.brand`.

   [!DNL Recommendations] erstellt nun für jede Marke eine &quot;Topverkäufe&quot;-Liste und zeigt dem Benutzer die entsprechende &quot;Topverkäufe&quot;-Liste basierend auf dem im Profil [!UICONTROL Favoritenmarke] gespeicherten Wert an.

   ![Attribut &quot;Topverkäufe&quot;](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteria/algorithms {#criteria-algorithms}

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

## Viewing criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Sie können Kriteriendetails auf einer Popupkarte anzeigen, indem Sie mit dem Mauszeiger über eine Karte fahren und auf das Informationssymbol einer Kriterienkarte klicken, ohne das Kriterium zu öffnen.

![Bewegen des Mauszeigers über die Kriterienkarte](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Klicken Sie auf die Registerkarte **[!UICONTROL Algorithmusinformationen]**, um allgemeine Informationen zu den ausgewählten Kriterien anzuzeigen, einschließlich Name, Beschreibungen, vertikalen Markt, Seitentyp(en), Empfehlungsschlüssel, Empfehlungslogik und Algorithmus-ID.

![Registerkarte „Algorithmusinformationen“](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Klicken Sie auf die Registerkarte **[!UICONTROL Algorithmusnutzung]**, um eine Liste der Aktivitäten anzuzeigen, die das ausgewählte Kriterium verwenden. Die Karte wird aktiv, inaktiv und als Entwurf von Aktivitäten Liste. Klicken Sie auf die Dropdown-Listen Live-Aktivitäten/Inaktive Aktivitäten/Aktivitäten-Entwürfe, um die gesamte Liste von Aktivitäten, die auf dieses Kriterium verweisen, Ansicht. Sie können auf einen Aktivitätslink klicken, um die Aktivität zur Bearbeitung zu öffnen.

![Registerkarte &quot;Algorithmusverwendung&quot;](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>Die Funktion [!UICONTROL Algorithmusverwendung] wird derzeit nur für Recommendations-Aktivitäten unterstützt. Diese Funktion wird derzeit nicht für Aktivitäten von A/B-Tests, automatisierter Zuordnung, automatischer Zielgruppe und Erlebnis-Targeting (XT) unterstützt, die [Empfehlungen als Angebot](/help/c-recommendations/recommendations-as-an-offer.md)enthalten.
