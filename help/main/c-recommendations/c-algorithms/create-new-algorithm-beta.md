---
keywords: Kriterien; Algorithmus; vertikaler Markt; Seitentyp; Empfehlungsschlüssel; Empfehlungslogik; Logik; Datenbereich; Lookback-Fenster; Verhaltens-Datenquelle; partielles Design; Ersatzempfehlungen; Einschlussregeln; Attributgewichtung; aktuelle Kategorie; benutzerdefiniertes Attribut; zuletzt gekauftes Element; zuletzt angezeigtes Element; am häufigsten angezeigte Artikel; Favoritenkategorie; Beliebtheit; zuletzt angezeigtes Element; zuletzt gekauft; zuletzt angesehen
description: Erfahren Sie, wie Sie Kriterien erstellen, die den Inhalt Ihrer [!DNL Recommendations] Aktivitäten steuern, um die Empfehlungen anzuzeigen, die für Ihre Aktivität am besten geeignet sind.
title: Wie erstelle ich [!UICONTROL Criteria] in  [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: c8b0e0414603761b1c67b13d74ffa96d745c99e3
workflow-type: tm+mt
source-wordcount: '2554'
ht-degree: 47%

---

# Erstellen von Kriterien

Kriterien in [!UICONTROL Adobe Target] [!UICONTROL Recommendations] steuern den Inhalt Ihrer [!UICONTROL Recommendations] -Aktivitäten. Erstellen Sie Kriterien, um die Empfehlungen anzuzeigen, die für Ihre Aktivität am besten geeignet sind. Diese Kriterien verwenden die Aktionen des Besuchers, um zu bestimmen, welche Inhalte oder Produkte angezeigt werden sollen.

In den folgenden Abschnitten wird beschrieben, wie Sie neue Kriterien erstellen.

## Zugriff auf den Bildschirm &quot;Neue Kriterien erstellen&quot;

Es gibt mehrere Möglichkeiten, den Bildschirm [!UICONTROL Create New Criteria] zu erreichen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie auf dem Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations] -Aktivität mit dem VEC (1}) erstellen, gelangen Sie sofort zum Bildschirm [!UICONTROL Select Criteria] , nachdem Sie ein Element auf Ihrer Seite ausgewählt und auf [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before] oder [!UICONTROL Insert Recommendations After] geklickt haben. [!UICONTROL Visual Experience Composer] Sie können dann ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Create Criteria]** klicken. Wenn Sie ein neues Kriterium erstellen, können Sie Ihre Kriterien speichern, um sie mit anderen [!DNL Recommendations] -Aktivitäten zu verwenden. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Wenn Sie eine [!DNL Recommendations] -Aktivität bearbeiten, klicken Sie in ein [!UICONTROL Recommendations Location] -Feld auf Ihrer Seite und wählen Sie **[!UICONTROL Change Criteria]** aus. Klicken Sie auf dem Bildschirm [!UICONTROL Select Criteria] auf **[!UICONTROL Create Criteria]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!DNL Recommendations]-Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mit der ersten Methode auf den Bildschirm [!UICONTROL Create New Criteria] zugreifen: auf den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Konfigurieren Sie die Informationen in den folgenden Abschnitten.

## [!UICONTROL Basic Information] {#info}

1. Geben Sie einen **[!UICONTROL Criteria Name]** ein.

   Dies ist der „interne“ Name, der für die Beschreibung der Kriterien verwendet wird. Sie möchten zum Beispiel Ihre Kriterien „Produkte mit der höchsten Marge“ nennen, Sie möchten jedoch nicht, dass dieser Titel öffentlich angezeigt wird. Sehen Sie sich den nächsten Schritt an, um den öffentlichen Titel festzulegen.

1. Geben Sie für alle Empfehlungen, die dieses Kriterium verwenden, einen öffentlichen &quot;**[!UICONTROL Display Title]**&quot;ein, der auf der Seite angezeigt werden soll.

   So wäre es möglicherweise sinnvoll, „Personen, die das ansahen, sahen auch dies an“ oder „Ähnliche Produkte“ einzublenden, wenn Sie diese Kriterien zum Einblenden von Empfehlungen verwenden.

1. Geben Sie eine kurze **[!UICONTROL Description]** des Kriteriums ein.

   Die Beschreibung soll Ihnen dabei helfen, die Kriterien zu identifizieren, und kann Informationen über den Zweck der Kriterien enthalten.

1. Wählen Sie eine Branche aus, die auf den Zielen Ihrer Recommendations-Aktivität basiert.

   | Vertikaler Markt | Ziel |
   |--- |--- |
   | [!UICONTROL Retail/Ecommerce] | Zum Kauf führende Konversion |
   | [!UICONTROL Lead Generation/B2B/Financial Services] | Konversion ohne Kauf |
   | [!UICONTROL Media/Publishing] | Interaktion |

   Andere Optionen für Kriterien ändern sich je nach vertikalem Markt, den Sie auswählen.

1. Wählen Sie einen **[!UICONTROL Page Type]** aus.

   Verschiedene Seitentypen stehen zur Verfügung.

   Vertikaler Markt und Seitentypen zusammen helfen Ihnen dabei, Ihre gespeicherten Kriterien zu kategorisieren, was die Wiederverwendung der Kriterien für andere [!DNL Recommendations] -Aktivitäten erleichtert.

## [!UICONTROL Recommendations Algorithm] {#rec-algo}

1. Wählen Sie einen **[!UICONTROL Algorithm Type]** und einen **[!UICONTROL Algorithm]** aus:

   ![Abschnitt &quot;Empfohlener Algorithmus&quot;](assets/recommended-algorithm.png)

   | Algorithmustyp | Verwendung/Verfügbarkeit von Algorithmen |
   | --- | --- |
   | [!UICONTROL Cart-Based] | Machen Sie Empfehlungen basierend auf den Inhalten des Warenkorbs des Benutzers. <ul><li>[!UICONTROL People Who Viewed These, Also Viewed] </li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul> |
   | [!UICONTROL Popularity-Based] | Machen Sie Empfehlungen basierend auf der allgemeinen Beliebtheit eines Artikels auf Ihrer Site oder auf der Beliebtheit von Artikeln in der bevorzugten oder am häufigsten angezeigten Kategorie, Marke, Genre usw. eines Benutzers. <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
   | [!UICONTROL Item-Based] | Empfehlungen aussprechen, die darauf basieren, ähnliche Artikel wie ein Artikel zu finden, den der Benutzer gerade ansieht oder kürzlich angesehen hat. <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
   | [!UICONTROL User-Based] | Empfehlungen basierend auf dem Benutzerverhalten erstellen. | <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
   | [!UICONTROL Custom Criteria] | Machen Sie Empfehlungen basierend auf einer von Ihnen hochgeladenen benutzerdefinierten Datei. | <ul><li>Benutzerspezifischer Algorithmus</li></ul> |

   >[!NOTE]
   >
   >Wenn Sie **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]** auswählen, haben Sie die Möglichkeit, [Regeln zur Ähnlichkeit von Inhalten](#similarity) festzulegen.

1. Wählen Sie nach Bedarf ein **Elementattribut** und ein **Profilattribut zum Abgleich**, einen **Empfehlungsschlüssel**, einen **Filterschlüssel** und/oder eine **Analytics-Metrik** aus, um den Algorithmus zu konfigurieren.

Die restlichen Konfigurationsoptionen für Algorithmen variieren je nach ausgewähltem Algorithmus. Um die Konfiguration des Algorithmus abzuschließen, wählen Sie eine [!UICONTROL Recommendation Key], [!UICONTROL Filtering Key], [!UICONTROL Co-Occurrence Basis], [!UICONTROL Analytics Metric] und/oder [!UICONTROL Item Attribute] und [!UICONTROL Profile Attribute to Match] aus.

Weitere Informationen zur Auswahl eines [!UICONTROL Recommendation Key] finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## [!UICONTROL Data Source] {#data-source}

1. Wählen Sie den gewünschten **[!UICONTROL Behavioral Data Source]**: [!UICONTROL Adobe Target] oder [!UICONTROL Analytics] aus.

   >[!NOTE]
   >
   >Der Abschnitt [!UICONTROL Behavioral Data Source] wird nur angezeigt, wenn Ihre Implementierung [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwendet.

   ![Source-Abschnitt zu Verhaltensdaten](assets/data-source.png)

   Wenn Sie &quot;[!UICONTROL Analytics]&quot; auswählen, wählen Sie die gewünschte Report Suite aus.

   Wenn das Kriterium &quot;[!DNL Adobe Analytics]&quot;als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Kriterienverfügbarkeit nach Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster für andere Kriterien verwendet wurden, wie unten beschrieben:

   * **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitrahmen hängt von der Systemlast von [!DNL Analytics] ab.
   * **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn Sie ein neues Kriterium erstellen oder ein vorhandenes Kriterium bearbeiten und die ausgewählte Report Suite bereits mit [!DNL Target Recommendations] verwendet wurde und der Datumsbereich gleich oder kleiner als der ausgewählte Datumsbereich ist, sind die Daten unmittelbar verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
   * **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn ein Benutzer ein Produkt anzeigt, wird für die [!UICONTROL Viewed Affinity] -Empfehlung ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] fast in Echtzeit übergeben. Die [!DNL Analytics]-Daten werden am Morgen des nächsten Tages an [!DNL Target] gesendet und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

   Weitere Informationen finden Sie unter [Verwenden von Adobe Analytics mit Target Recommendations](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

1. Legen Sie den **[!UICONTROL Lookback Window]** fest, um den Zeitraum der verfügbaren historischen Benutzerverhaltensdaten zu bestimmen, die bei der Bestimmung der anzuzeigenden Empfehlungen verwendet werden sollen. Diese Option ist für alle Algorithmen mit Ausnahme von [!UICONTROL Items with Similar Attributes] und [!UICONTROL Custom Algorithms] verfügbar.

   ![Regler für Lookback-Fenster](assets/data-range.png)

   Wählen Sie ein kürzeres Datenfenster, wenn Ihre Site durch hohes Traffic-Aufkommen und häufig wechselndes Verhalten gekennzeichnet ist. Ein kürzeres Fenster ermöglicht es [!DNL Recommendations], besser auf Änderungen am Markt und in Ihrem Unternehmen zu reagieren. Ein kürzeres Fenster bedeutet zum Beispiel, dass [!DNL Recommendations] Änderungen im Besucherverhalten erkennt, wenn Ihre Besucher Saisoneinkäufe absolvieren - wie etwa zum Schulanfang oder zu Weihnachten –, und Artikel empfiehlt, die zur jeweiligen Einkaufssaison passen.

   Wenn Sie nur über wenige Daten verfügen oder das Besucherverhalten sich nur selten ändert, können Sie ein längeres Fenster auswählen. Bei vielen Sites führt ein kürzeres Fenster jedoch zu Empfehlungen mit höherer Qualität.

   Die verfügbaren Datenbereiche sind:

   | Option &quot;Lookback-Fenster&quot; | Aktualisierte Häufigkeit (wird beim Bewegen des Mauszeigers angezeigt) | Unterstützte Algorithmen |
   | --- | --- | --- |
   | Sechs Stunden | Algorithmus wird alle 3-6 Stunden ausgeführt | [!UICONTROL Popularity-Based] Algorithmen, wenn der ausgewählte [!UICONTROL Behavioral Data Source] [!DNL Adobe Target] ist |
   | Ein Tag | Der Algorithmus wird alle 12-24 Stunden ausgeführt | [!UICONTROL Popularity-Based] Algorithmen |
   | Zwei Tage | Der Algorithmus wird alle 12-24 Stunden ausgeführt | <ul><li>[!UICONTROL Popularity-Based] Algorithmen</li><li>[!UICONTROL Item-Based] Algorithmen</li><li>[!UICONTROL User-Based] Algorithmen</li><li>[!UICONTROL Cart-Based] Algorithmen</li></ul> |
   | Eine Woche | Der Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>[!UICONTROL Popularity-Based] Algorithmen</li><li>[!UICONTROL Item-Based] Algorithmen</li><li>[!UICONTROL User-Based] Algorithmen</li><li>[!UICONTROL Cart-Based] Algorithmen</li></ul> |
   | Zwei Woche | Der Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>[!UICONTROL Popularity-Based] Algorithmen</li><li>[!UICONTROL Item-Based] Algorithmen</li><li>Alle [!UICONTROL User-Based]-Algorithmen</li><li>[!UICONTROL Cart-Based] Algorithmen</li></ul> |
   | Einen Monat (30 Tage) | Der Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>[!UICONTROL Popularity-Based] Algorithmen</li><li>[!UICONTROL Item-Based] Algorithmen</li><li>[!UICONTROL User-Based] Algorithmen</li><li>[!UICONTROL Cart-Based] Algorithmen</li></ul> |
   | Zwei Monate (61 Tage) | Der Algorithmus wird alle 24-48 Stunden ausgeführt | <ul><li>[!UICONTROL Popularity-Based] Algorithmen</li><li>[!UICONTROL Item-Based] Algorithmen</li><li>[!UICONTROL User-Based] Algorithmen</li><li>[!UICONTROL Cart-Based] Algorithmen</li></ul> |

## [!UICONTROL Backup Content] {#content}

[!UICONTROL Backup Content] -Regeln bestimmen, was passiert, wenn die Anzahl der empfohlenen Artikel Ihren [Empfehlungsentwurf](/help/main/c-recommendations/c-design-overview/design-overview.md) nicht erfüllt. Es ist möglich, dass [!DNL Recommendations] -Kriterien weniger Empfehlungen zurückgeben, als vom Entwurf gefordert werden. Wenn Ihr Entwurf beispielsweise über Slots für vier Artikel verfügt, Ihre Kriterien jedoch nur dazu führen, dass zwei Artikel empfohlen werden, können Sie die verbleibenden Slots leer lassen. Sie können Ersatzempfehlungen zum Ausfüllen der zusätzlichen Slots verwenden oder festlegen, dass keine Empfehlungen angezeigt werden.

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Partial Design Rendering]** an die Position &quot;Ein&quot;.

   Es werden so viele Plätze wie möglich ausgefüllt, aber die Designvorlage kann leere Plätze für die verbleibenden Plätze enthalten. Wenn diese Option deaktiviert ist und nicht genügend Inhalt vorhanden ist, um alle verfügbaren Plätze auszufüllen, werden keine Empfehlungen bereitgestellt und stattdessen werden Standardinhalte angezeigt.

   Aktivieren Sie diese Option, wenn Empfehlungen mit leeren Slots bereitgestellt werden sollen. Verwenden Sie Reserveempfehlungen, wenn Sie möchten, dass Empfehlungs-Slots mit Inhalten gefüllt werden, die auf Ihren Kriterien basieren und leere Slots enthalten, die mit ähnlichen oder beliebten Inhalten von Ihrer Site gefüllt sind, wie im nächsten Schritt erläutert.

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Show Backup Content]** an die Position &quot;Ein&quot;.

   Füllen Sie alle verbleibenden leeren Slots im Design mit einer zufälligen Auswahl der am häufigsten angezeigten Produkte aus Ihrer gesamten Site aus.

   Die Verwendung von Reserveempfehlungen stellt sicher, dass Ihr Empfehlungsentwurf alle verfügbaren Slots ausfüllt. Angenommen, Sie haben ein Design von 4 x 1, wie unten dargestellt:

   ![4 x 1 Design](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

   Angenommen, Ihre Kriterien führen dazu, dass nur zwei Artikel empfohlen werden. Wenn Sie die Option &quot;[!UICONTROL Partial Design Rendering]&quot; aktivieren, werden die ersten beiden Slots ausgefüllt, die verbleibenden beiden Slots bleiben jedoch leer. Wenn Sie jedoch die Option [!UICONTROL Show Backup Recommendations] aktivieren, werden die ersten beiden Slots anhand Ihrer angegebenen Kriterien ausgefüllt und die verbleibenden beiden Slots werden basierend auf Ihren Reserveempfehlungen ausgefüllt.

   Die folgende Matrix zeigt das Ergebnis, das Sie bei Verwendung der Optionen [!UICONTROL Partial Design Rendering] und [!UICONTROL Backup Content] feststellen werden:

   | Teilweises Entwurfs-Rendering | Backup Content | Ergebnis |
   |--- |--- |--- |
   | Deaktiviert | Deaktiviert | Wenn weniger Empfehlungen zurückgegeben werden als im Entwurf vorgesehen, wird der Empfehlungsentwurf durch Standardinhalte ersetzt und es erscheinen keine Empfehlungen. |
   | Aktiviert | Deaktiviert | Der Entwurf wird gerendert, kann jedoch leere Positionen enthalten, falls weniger Empfehlungen zurückgegeben werden, als im Entwurf vorgesehen. |
   | Aktiviert | Aktiviert | Ersatzempfehlungen erscheinen an solchen leeren Positionen und vervollständigen den Entwurf.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf nur teilweise gerendert.<br>In dem Fall, dass die Kriterien keine Empfehlungen zurückgeben und die Einschlussregeln die Ersatzempfehlungen auf null reduzieren, wird der Entwurf durch Standardinhalte ersetzt. |
   | Deaktiviert | Aktiviert | Ersatzempfehlungen erscheinen an solchen leeren Positionen und vervollständigen den Entwurf.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf durch Standardinhalte ersetzt und es werden keine Empfehlungen angezeigt. |

   Weitere Informationen finden Sie unter [Verwenden einer Reserveempfehlung](/help/main/c-recommendations/c-algorithms/backup-recs.md).

1. (Bedingt) Wenn Sie im vorherigen Schritt **[!UICONTROL Show Backup Content]** ausgewählt haben, können Sie **[!UICONTROL Apply inclusion rules to backup recommendations]** aktivieren.

   Einschlussregeln bestimmen, welche Artikel in Ihren Empfehlungen enthalten sind. Die verfügbaren Optionen hängen von Ihrem vertikalen Markt ab.

   Weitere Informationen finden Sie unten unter [Einschlussregeln angeben](#inclusion) .

## Ähnlichkeit von Inhalten {#similarity}

Verwenden Sie [!UICONTROL Content Similarity] -Regeln, um Empfehlungen basierend auf Artikeln oder Medienattributen zu erstellen.

>[!NOTE]
>
>Wenn Sie **[!UICONTROL Item-Based]**/ **[!UICONTROL Media with Similar Attributes]** als Ihren [!UICONTROL Algorithm Type] und [!UICONTROL Algorithm] ausgewählt haben, können Sie Regeln zur Ähnlichkeit von Inhalten festlegen.

Mithilfe der Funktion für Ähnlichkeit von Inhalten werden Artikelattribut-Schlüsselwörter verglichen und Empfehlungen basierend darauf erstellt, wie viele Schlüsselwörter die verschiedenen Artikel gemeinsam haben. Empfehlungen, die auf der Ähnlichkeit von Inhalten basieren, benötigen für herausragende Ergebnisse keine historischen Daten.

Die Verwendung der Ähnlichkeit von Inhalten zum Generieren von Empfehlungen ist besonders effektiv für neue Artikel, die in Empfehlungen mit *Personen, die dies angesehen haben, auch angezeigt* und anderer Logik, die auf dem früheren Verhalten basiert, nicht angezeigt werden. Anhand der Ähnlichkeit von Inhalten können sinnvolle Empfehlungen für neue Benutzer erstellt werden, für die noch keine historischen Daten oder Einkäufe verzeichnet wurden.

Wenn Sie **[!UICONTROL Item-Based]**/ **[!UICONTROL Media with Similar Attributes]** auswählen, können Sie Regeln erstellen, um die Wichtigkeit bestimmter Elementattribute bei der Bestimmung von Empfehlungen zu erhöhen oder zu verringern. Bei Artikeln wie beispielsweise Büchern möchten Sie möglicherweise die Bedeutung von Attributen wie *Genre*, *Autor*, *Serie* und so weiter hervorheben, um ähnliche Bücher zu empfehlen.

Da beim Vergleich der Ähnlichkeit von Inhalten Stichwörter verwendet werden, führen einige Attribute wie *Botschaft* oder *Beschreibung* zu einer Verwässerung der Vergleiche. Sie können daher Regeln erstellen, mit denen solche Attribute ignoriert werden.

Standardmäßig sind alle Attribute auf den Wert *Grundlinie* eingestellt. Sie müssen keine Regeln erstellen, wenn Sie diese Einstellung nicht ändern möchten.

>[!NOTE]
>
>Der Algorithmus zur Ähnlichkeit von Inhalten verwendet möglicherweise Stichproben bei der Berechnung der Ähnlichkeit zwischen Elementen. Infolgedessen können die Ähnlichkeitsbewertungen zwischen den Elementen bei den einzelnen Algorithmusausführungen variieren.

## Einschlussregeln {#inclusion}

Mehrere Optionen ermöglichen es Ihnen, die in Ihren Empfehlungen angezeigten Elemente einzuschränken. Sie können Einschlussregeln beim Erstellen von Kriterien oder Promotions verwenden.

Einschlussregeln sind optional. Das Festlegen dieser Regeln jedoch ermöglicht Ihnen die bessere Steuerung der Artikel, die in Ihren Empfehlungen erscheinen. Jedes konfigurierte Detail schränkt die Anzeigekriterien weiter ein.

Beispiel: Sie können nur Damenschuhe anzeigen, deren Bestand über 50 und deren Preis zwischen 25 und 45 Euro liegt. Sie können auch jedes Attribut gewichten, sodass die für Ihr Unternehmen wichtigeren Artikel am ehesten angezeigt werden.

Weiteres Beispiel: Sie können Stellenangebote ausschließlich für Besucher Ihrer Website anzeigen, die aus bestimmten Orten stammen und über die erforderlichen Abschlüsse verfügen.

Die Optionen für die Einschlussregeln variieren je nach vertikalem Markt. Einschlussregeln werden standardmäßig auf Ersatzempfehlungen angewendet.

>[!IMPORTANT]
>
>Sie sollten mit Einschlussregeln vorsichtig umgehen. Sie sind nützlich, wenn Ihr Unternehmen beispielsweise mit Regeln arbeitet, die erfordern, dass eine Marke nicht empfohlen wird, während eine andere Marke gezeigt wird. Bei dieser Funktion kommt es jedoch zu Opportunitätskosten. Ein gewisser Lift-Prozentsatz geht möglicherweise verloren, wenn Artikel nicht angezeigt werden, die normalerweise durch die Aktivitätskriterien angezeigt werden würden.

Die Einschlussregeln werden mit „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Führen Sie zum Erstellen einer einfachen Einschlussregel die folgenden Schritte aus, um - wie im oben stehenden Beispiel - nur Damenschuhe mit einem Bestand von mehr als 50 und einem Preis von zwischen 25 und 45 € anzuzeigen.

1. (Bedingt) Schieben Sie den Umschalter **[!UICONTROL Allow recently purchased items to be recommended?]** an die Position &quot;Ein&quot;.

   Diese Einstellung basiert auf `productPurchasedId`. Das Standardverhalten ist es, zuvor gekaufte Artikel nicht zu empfehlen. In den meisten Fällen ist es nicht sinnvoll, Artikel zu bewerben, die Kunden kürzlich gekauft haben. Es ist nützlich, wenn Sie Artikel verkaufen, die Kunden in der Regel nur einmal kaufen, zum Beispiel Kayaks. Wenn Sie Artikel verkaufen, die Personen wiederholt kaufen, wie Shampoo oder andere persönliche Artikel, sollten Sie diese Option aktivieren.

1. Legen Sie einen Preisbereich für die Produkte fest, die Sie empfehlen möchten.
1. Legen Sie den Mindestbestand für die Produkte fest, die Sie empfehlen möchten.
1. Konfigurieren Sie die Empfehlung, um nur Artikel anzuzeigen, wenn sie bestimmte Kriterien erfüllen.

   Sie können angeben, dass Artikel nur berücksichtigt werden, wenn eines der Attribute in der Liste eine oder mehrere angegebene Bedingungen erfüllt oder nicht erfüllt.

   Die verfügbaren Auswerter sind von dem Wert abhängig, den Sie in der ersten Dropdownliste auswählen. Sie können mehrere Elemente auflisten. Diese Artikel werden durch ODER ausgewertet.

   Mehrere Regeln werden mit „AND“ kombiniert.

   >[!NOTE]
   >
   >Diese Option beschränkt die in der Empfehlung angezeigten Elemente. Sie hat keine Auswirkungen darauf, auf welchen Seiten die Empfehlung angezeigt wird. Um eine Einschränkung bezüglich der Anzeige der Empfehlung vorzunehmen, wählen Sie die Seiten im Experience Composer aus.

Weitere Informationen finden Sie unter [Verwenden dynamischer und statischer Einschlussregeln](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Attributgewichtung {#weighting}

Sie können mehrere Regeln hinzufügen, um den Algorithmus anhand wichtiger Informationen oder Metadaten zum Inhaltskatalog zu &quot;umkehren&quot;, sodass bestimmte Elemente mit höherer Wahrscheinlichkeit angezeigt werden.

Sie können beispielsweise eine höhere Gewichtung auf Artikel anwenden, damit sie häufiger in der Empfehlung vorkommen. Artikel, die nicht Teil des Sonderangebots sind, werden nicht vollständig ausgeschlossen, jedoch weniger häufig angezeigt. Auf denselben Algorithmus können mehrere gewichtete Attribute angewendet werden und die gewichteten Attribute können mit dem in der Empfehlung aufgeteilten Traffic getestet werden.

1. Wählen Sie einen Wert aus.

   Der Wert bestimmt den Typ des Elements, das mit größerer Wahrscheinlichkeit und auf der Basis mehrerer verfügbarer Kriterien angezeigt wird.

1. Wählen Sie einen Auswerter.

1. Geben Sie das Keyword ein, um die Regelattribute abzuschließen.

   Die vollständige Regel könnte beispielsweise &quot;Kategorie enthält Unterzeichenfolgen-Schuhe&quot;lauten.

1. Wählen Sie die Wertigkeit aus, die der Regel zugeordnet werden soll.

   Die Gewichtung kann von 0 bis 100 in 25er-Schritten eingestellt werden.

1. Fügen Sie nach Bedarf weitere Regeln hinzu.

Klicken Sie abschließend auf **[!UICONTROL Create]**.

Wenn Sie eine neue [!UICONTROL Recommendations] -Aktivität erstellen oder eine bestehende bearbeiten, ist das Kontrollkästchen **[!UICONTROL Save criteria for later]** standardmäßig aktiviert. Sollten Sie die Kriterien nicht in anderen Aktivitäten verwenden wollen, deaktivieren Sie das Kontrollkästchen, bevor Sie speichern.
