---
keywords: Kriterien;Algorithmus;Branche;Vertikal;Seitentyp;Empfehlungsschlüssel;Empfehlungslogik;Logik;Datenbereich;Verhaltensdatenquelle;Verhaltensdatenquelle;Ersatzempfehlungen;Einschlussregeln;Attributgewichtung;aktuelle Kategorie;benutzerdefiniertes Attribut;Zulzuletzt gekaufter Artikel;Zulzuletzt angezeigter Artikel;Am häufigsten angezeigte Artikel;Favoritenste Kategorie;Popularität;Zuletzt angezeigte Artikel;Zulzuletzt gekauft;Letzte;Letzte;Letzte;Zulzuletzt angesehen;Zulzuletzt angesehen;Favor;Zulzuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angezeigt;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angezeigt;Zuletzt angesehen;Zuletzt angesehen;Zuletzt angezeigt;Zuletzt angesehen;Zuletzt angezeigt;Zuletzt
description: Erfahren Sie, wie Sie Kriterien erstellen, die den Inhalt Ihrer Adobe Recommendations-Aktivitäten steuern, um die für Ihre Aktivität am besten geeigneten Empfehlungen anzuzeigen.
title: Wie erstelle ich Kriterien in Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Kriterien erstellen{#create-criteria}

Kriterien in [!UICONTROL Adobe Target] [!UICONTROL Recommendations] steuern den Inhalt Ihrer [!UICONTROL Recommendations]-Aktivitäten. Erstellen Sie Kriterien zur Anzeige der Empfehlungen, die am besten zu Ihrer Aktivität passen. Diese Kriterien verwenden die Aktionen des Besuchers, um festzulegen, welche Inhalte oder Produkte angezeigt werden sollen.

Die folgenden Abschnitte erläutern, wie Sie ein neues Kriterium erstellen.

## Auf den Bildschirm &quot;Neue Kriterien erstellen&quot;zugreifen

Sie haben viele Möglichkeiten, um auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!DNL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!DNL Recommendations]-Aktivität mit dem [!UICONTROL Visual Experience Composer] (VEC) erstellen, werden Sie sofort zum Bildschirm [!UICONTROL Kriterien auswählen, nachdem Sie ein Element auf Ihrer Seite ausgewählt haben und auf [!UICONTROL Ersetzen mit Recommendations], [!UICONTROL Recommendations vor] oder [!UICONTROL einfügen Fügen Sie Recommendations nach] ein. ] Sie können dann ein verfügbares Kriterium auswählen oder auf **[!UICONTROL Kriterien erstellen]** klicken. Wenn Sie ein neues Kriterium erstellen, haben Sie die Möglichkeit, Ihre Kriterien für die Verwendung mit anderen [!DNL Recommendations]-Aktivitäten zu speichern. Weitere Informationen finden Sie unter [Erstellen einer Recommendations-Aktivität](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Klicken Sie beim Bearbeiten einer [!DNL Recommendations]Aktivität in ein Feld für die [!UICONTROL Empfehlungsposition] auf Ihrer Seite und wählen Sie **[!UICONTROL Kriterien ändern]**. Klicken Sie im Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Kriterien erstellen]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!DNL Recommendations]-Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf den Bildschirm [!UICONTROL Neue Kriterien erstellen] zugreifen: den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriterien erstellen]**.

   ![Neue Kriterien erstellen](/help/c-recommendations/c-algorithms/assets/CreateNewCriteria_full-new.png)

1. Konfigurieren Sie die Informationen in den folgenden Abschnitten.

## Basisinformationen   {#info}

1. Geben Sie einen **[!UICONTROL Kriteriennamen]** ein.

   Dies ist der „interne“ Name, der für die Beschreibung der Kriterien verwendet wird. Sie möchten zum Beispiel Ihre Kriterien „Produkte mit der höchsten Marge“ nennen, Sie möchten jedoch nicht, dass dieser Titel öffentlich angezeigt wird. Sehen Sie sich den nächsten Schritt an, um den öffentlichen Titel festzulegen.

   ![Abschnitt &quot;Grundlegende Informationen&quot;](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Geben Sie einen öffentlichen **[!UICONTROL Anzeigetitel]** ein, der auf der Seite für alle Empfehlungen angezeigt wird, die diesen Kriterien entsprechen.

   So wäre es möglicherweise sinnvoll, „Personen, die das ansahen, sahen auch dies an“ oder „Ähnliche Produkte“ einzublenden, wenn Sie diese Kriterien zum Einblenden von Empfehlungen verwenden.

1. Geben Sie eine kurze **[!UICONTROL Beschreibung]** des Kriteriums ein.

   Die Beschreibung sollte Ihnen dabei helfen, die Kriterien zu identifizieren, und kann Informationen über den Zweck der Kriterien enthalten.

1. Wählen Sie eine Branche, die auf den Zielen Ihrer Recommendations-Aktivität basiert.

   | Vertikaler Markt | Ziel |
   |--- |--- |
   | Einzelhandel/E-Commerce | Zum Kauf führende Konversion |
   | Lead-Generierung/B2B/Finanzdienstleistungen | Konversion ohne Kauf |
   | Medien/Verlagswesen | Interaktion |

   Andere Optionen für Kriterien ändern sich auf Grundlage des vertikalen Markts, den Sie auswählen.

1. Wählen Sie einen **[!UICONTROL Seitentyp]** aus.

   Verschiedene Seitentypen stehen zur Verfügung.

   Vertikaler Markt und Seitentyp werden zusammen genutzt, um Ihre gespeicherten Kriterien zu kategorisieren, wodurch die Wiederverwendung der Kriterien für andere [!DNL Recommendations]-Aktivitäten erleichtert wird.

1. Wählen Sie einen **[!UICONTROL Empfehlungsschlüssel]** aus.

   Weitere Informationen zum Stützen von Kriterien auf einen Schlüssel finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. Wählen Sie die **[!UICONTROL Empfehlungslogik]** aus.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md).

   >[!NOTE]
   >
   >Wenn Sie **[!UICONTROL Elemente]**/ **[!UICONTROL Medien mit ähnlichen Attributen]** auswählen, können Sie [Inhaltsähnlichkeitsregeln](#similarity) festlegen.

## Datenquelle {#data-source}

1. Legen Sie den **[!UICONTROL Datumsbereich]** fest, um den Zeitraum der verfügbaren historischen Benutzerverhaltensdaten festzulegen, die bei der Bestimmung der anzuzeigenden Empfehlungen verwendet werden.

   ![Datenbereich-Schieberegler](/help/c-recommendations/c-algorithms/assets/data-range.png)

   Wählen Sie ein kürzeres Datenfenster, wenn Ihre Site durch hohes Traffic-Aufkommen und häufig wechselndes Verhalten gekennzeichnet ist. Ein kürzeres Fenster ermöglicht es [!DNL Recommendations], besser auf Änderungen am Markt und in Ihrem Unternehmen zu reagieren. Ein kürzeres Fenster bedeutet zum Beispiel, dass [!DNL Recommendations] Änderungen im Besucherverhalten erkennt, wenn Ihre Besucher Saisoneinkäufe absolvieren - wie etwa zum Schulanfang oder zu Weihnachten –, und Artikel empfiehlt, die zur jeweiligen Einkaufssaison passen.

   Wenn Sie nur über wenige Daten verfügen oder das Besucherverhalten sich nur selten ändert, können Sie ein längeres Fenster auswählen. Bei vielen Websites führt ein kürzeres Fenster jedoch zu besseren Empfehlungen.

   Die verfügbaren Datenbereiche sind:

   * Zwei Tage
   * Eine Woche
   * Zwei Woche
   * Ein Monat
   * Zwei Monate

1. (Bedingt) Wählen Sie die gewünschte **[!UICONTROL Verhaltensdatenquelle]** aus: [!UICONTROL mboxes] oder [!UICONTROL Analytics].

   >[!NOTE]
   >
   >Der Abschnitt [!UICONTROL Behavioral Data Source] wird nur angezeigt, wenn Ihre Implementierung [Analytics for Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwendet.

   ![Abschnitt &quot;Verhaltensdatenquelle&quot;](/help/c-recommendations/c-algorithms/assets/behavioural-data-source.png)

   Wenn Sie sich für [!UICONTROL Analytics] entschieden haben, wählen Sie die gewünschte Report Suite.

   Wenn die Kriterien [!DNL Adobe Analytics] als verhaltensbasierte Datenquelle verwenden, hängt die Zeit für die Verfügbarkeit von Kriterien davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster für andere Kriterien verwendet wurden, wie nachfolgend beschrieben:

   * **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics] Systemlast ab.
   * **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn Sie ein neues Kriterium erstellen oder ein vorhandenes Kriterium bearbeiten und die ausgewählte Report Suite bereits mit [!DNL Target Recommendations] verwendet wurde und der Datumsbereich gleich oder kleiner als der ausgewählte Datumsbereich ist, sind die Daten unmittelbar verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
   * **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn sich ein Benutzer ein Produkt ansieht, wird für die Empfehlung [!UICONTROL Viewed Affinity] in nahezu Echtzeit ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] gesendet. Die [!DNL Analytics]-Daten werden am Morgen des nächsten Tages an [!DNL Target] gesendet und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

   Weitere Informationen finden Sie unter [Verwenden Sie Adobe Analytics mit Zielgruppe Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

## Inhalt {#content}

Inhaltsregeln bestimmen, was passiert, wenn die Anzahl der empfohlenen Artikel Ihren [Empfehlungsentwurf](/help/c-recommendations/c-design-overview/design-overview.md) nicht ausfüllt. Möglicherweise geben [!DNL Recommendations]-Kriterien weniger Empfehlungen zurück, als im Entwurf angegeben sind. Wenn Ihr Entwurf z. B. Slots für vier Elemente enthält, Ihre Kriterien jedoch nur zwei Artikel empfehlen, können Sie die verbleibenden Slots leer lassen oder Reserveempfehlungen verwenden, um die zusätzlichen Slots zu füllen.

![Inhaltsabschnitt](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Partielles Design-Rendering]** an die Position &quot;on&quot;.

   Es werden so viele Plätze wie möglich ausgefüllt, die Designvorlage kann jedoch Leerzeichen für die verbleibenden Plätze enthalten. Wenn diese Option deaktiviert ist und nicht genügend Inhalte vorhanden sind, um alle verfügbaren Plätze auszufüllen, werden keine Empfehlungen bereitgestellt und stattdessen Standardinhalte angezeigt.

   Aktivieren Sie diese Option, wenn Empfehlungen mit leeren Slots versorgt werden sollen. Verwenden Sie Reserveempfehlungen, wenn Sie möchten, dass Empfehlungszeiträume mit Inhalten gefüllt werden, die auf Ihren Kriterien basieren und mit leeren Slots gefüllt werden, die mit ähnlichen oder beliebten Inhalten Ihrer Site gefüllt sind, wie im nächsten Schritt beschrieben.

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Backup Recommendations]** anzeigen zur &quot;on&quot;-Position.

   Füllen Sie alle verbleibenden leeren Slots im Design mit einer zufälligen Auswahl der am häufigsten angezeigten Produkte aus Ihrer gesamten Site.

   Die Verwendung von Reserveempfehlungen stellt sicher, dass Ihr Empfehlungsentwurf alle verfügbaren Plätze ausfüllt. Angenommen, Sie haben ein Design im Format 4 x 1, wie unten dargestellt:

   ![4 x 1 Design](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Nehmen wir einmal an, Ihre Kriterien führen dazu, dass nur zwei Artikel empfohlen werden. Wenn Sie die Option [!UICONTROL Teilweises Design-Rendering] aktivieren, werden die ersten beiden Slots ausgefüllt, aber die verbleibenden beiden Slots bleiben leer. Wenn Sie jedoch die Option [!UICONTROL Backup-Recommendations anzeigen] aktivieren, werden die ersten beiden Slots basierend auf Ihren angegebenen Kriterien ausgefüllt und die restlichen zwei Slots werden basierend auf Ihren Reserveempfehlungen ausgefüllt.

   Die folgende Matrix zeigt das Ergebnis, das Sie bei Verwendung der Optionen [!UICONTROL Partielles Design Rendering] und [!UICONTROL Backup Recommendations] beobachten werden:

   | Teilweises Entwurfs-Rendering | Ersatzempfehlungen | Ergebnis |
   |--- |--- |--- |
   | Deaktiviert | Deaktiviert | Wenn weniger Empfehlungen zurückgegeben werden als im Entwurf vorgesehen, wird der Empfehlungsentwurf durch Standardinhalte ersetzt und es erscheinen keine Empfehlungen. |
   | Aktiviert | Deaktiviert | Der Entwurf wird gerendert, kann jedoch leere Positionen enthalten, falls weniger Empfehlungen zurückgegeben werden, als im Entwurf vorgesehen. |
   | Aktiviert | Aktiviert | Ersatzempfehlungen erscheinen an solchen leeren Positionen und vervollständigen den Entwurf.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf nur teilweise gerendert.<br>In dem Fall, dass die Kriterien keine Empfehlungen zurückgeben und die Einschlussregeln die Ersatzempfehlungen auf null reduzieren, wird der Entwurf durch Standardinhalte ersetzt. |
   | Deaktiviert | Aktiviert | Ersatzempfehlungen erscheinen an solchen leeren Positionen und vervollständigen den Entwurf.<br>Sollte die Anwendung von Einschlussregeln auf die Ersatzempfehlungen die Anzahl an geeigneten Ersatzempfehlungen so stark einschränken, dass der Entwurf nicht vervollständigt werden kann, wird der Entwurf durch Standardinhalte ersetzt und es werden keine Empfehlungen angezeigt. |

   Weitere Informationen finden Sie unter [Verwenden Sie eine Reserveempfehlung](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Bedingt) Wenn Sie im vorherigen Schritt **[!UICONTROL Backup-Recommendations anzeigen]** ausgewählt haben, können Sie **[!UICONTROL Einschlussregeln auf Sicherungsempfehlungen anwenden]** aktivieren.

   Einschlussregeln bestimmen, welche Artikel in Ihren Empfehlungen enthalten sind. Die verfügbaren Optionen hängen von Ihrem vertikalen Markt ab.

   Weitere Informationen finden Sie unter [Einschlussregeln](#inclusion) unten angeben.

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Vorher gekaufte Artikel empfehlen]** an die Position &quot;on&quot;.

   Diese Einstellung basiert auf `productPurchasedId`. Das Standardverhalten ist es, zuvor gekaufte Artikel nicht zu empfehlen. In den meisten Fällen ist es nicht sinnvoll, Artikel zu bewerben, die Kunden kürzlich gekauft haben. Es ist nützlich, wenn Sie Artikel verkaufen, die Kunden in der Regel nur einmal kaufen, zum Beispiel Kayaks. Wenn Sie Artikel verkaufen, die Personen wiederholt kaufen, z. B. Shampoo oder andere persönliche Artikel, sollten Sie diese Option aktivieren.

## Ähnlichkeit von Inhalten {#similarity}

Verwenden Sie Regeln zur [!UICONTROL Ähnlichkeit von Inhalten] für die Bereitstellung von Empfehlungen basierend auf Artikeln oder Medienattributen.

>[!NOTE]
>
>Wenn Sie **[!UICONTROL Elemente]**/ **[!UICONTROL Medien mit ähnlichen Attributen]** als [Empfehlungslogik](#info) ausgewählt haben, haben Sie die Möglichkeit, Inhaltsähnlichkeitsregeln festzulegen.

Mithilfe der Funktion für Ähnlichkeit von Inhalten werden Artikelattribut-Schlüsselwörter verglichen und Empfehlungen basierend darauf erstellt, wie viele Schlüsselwörter die verschiedenen Artikel gemeinsam haben. Empfehlungen, die auf der Ähnlichkeit von Inhalten basieren, benötigen für herausragende Ergebnisse keine historischen Daten.

Eine Erstellung von Empfehlungen anhand der Ähnlichkeit von Inhalten ist besonders bei neuen Artikeln effektiv, die bei Empfehlungen mit der Funktion *Personen, die das ansahen, sahen auch dies an* und anderen, auf historischem Verhalten von Benutzern basierenden Optionen nicht angezeigt werden. Anhand der Ähnlichkeit von Inhalten können sinnvolle Empfehlungen für neue Benutzer erstellt werden, für die noch keine historischen Daten oder Einkäufe verzeichnet wurden.

Wählen Sie **[!UICONTROL Artikel]**/**[!UICONTROL Medien mit ähnlichen Attributen]** aus, haben Sie die Option, Regeln zur Steigerung oder Minderung der Wichtigkeit bestimmter Artikelattribute bei der Erstellung von Empfehlungen festzulegen. Bei Artikeln wie beispielsweise Büchern möchten Sie möglicherweise die Bedeutung von Attributen wie *Genre*, *Autor*, *Serie* und so weiter hervorheben, um ähnliche Bücher zu empfehlen.

![](assets/ContentSimilarity.png)

Da beim Vergleich der Ähnlichkeit von Inhalten Stichwörter verwendet werden, führen einige Attribute wie *Botschaft* oder *Beschreibung* zu einer Verwässerung der Vergleiche. Sie können daher Regeln erstellen, mit denen solche Attribute ignoriert werden.

Standardmäßig sind alle Attribute auf den Wert *Grundlinie* eingestellt. Sie müssen keine Regeln erstellen, wenn Sie diese Einstellung nicht ändern möchten.

>[!NOTE]
>
>Der Algorithmus zur Ähnlichkeit von Inhalten verwendet bei der Berechnung der Ähnlichkeit zwischen Elementen möglicherweise Stichproben. Infolgedessen können die Übereinstimmungsbewertungen von Elementen je nach Ausführung des Algorithmus variieren.

## Einschlussregeln {#inclusion}

Mehrere Optionen ermöglichen es Ihnen, die in Ihren Empfehlungen angezeigten Elemente einzuschränken. Sie können Einschlussregeln beim Erstellen von Kriterien oder Promotions verwenden.

![Einschlussregeln](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Einschlussregeln sind optional. Das Festlegen dieser Regeln jedoch ermöglicht Ihnen die bessere Steuerung der Artikel, die in Ihren Empfehlungen erscheinen. Jedes konfigurierte Detail schränkt die Anzeigekriterien weiter ein.

Beispiel: Sie können nur Damenschuhe anzeigen, deren Bestand über 50 und deren Preis zwischen 25 und 45 Euro liegt. Sie können auch jedes Attribut gewichten, sodass die für Ihr Unternehmen wichtigeren Artikel am ehesten angezeigt werden.

Weiteres Beispiel: Sie können Stellenangebote ausschließlich für Besucher Ihrer Website anzeigen, die aus bestimmten Orten stammen und über die erforderlichen Abschlüsse verfügen.

Die Optionen für die Einschlussregeln variieren je nach vertikalem Markt. Einschlussregeln werden standardmäßig auf Ersatzempfehlungen angewendet.

>[!IMPORTANT]
>
>Sie sollten mit Einschlussregeln vorsichtig umgehen. Sie sind nützlich, wenn Ihr Unternehmen beispielsweise mit Regeln arbeitet, die erfordern, dass eine Marke nicht empfohlen wird, während eine andere Marke gezeigt wird. Bei dieser Funktion kommt es jedoch zu Opportunitätskosten. Ein gewisser Lift-Prozentsatz geht möglicherweise verloren, wenn Artikel nicht angezeigt werden, die normalerweise durch die Aktivitätskriterien angezeigt werden würden.

Die Einschlussregeln werden mit „AND“ verbunden. Alle Regeln müssen erfüllt sein, damit ein Artikel in den Empfehlungen berücksichtigt wird.

Führen Sie zum Erstellen einer einfachen Einschlussregel die folgenden Schritte aus, um - wie im oben stehenden Beispiel - nur Damenschuhe mit einem Bestand von mehr als 50 und einem Preis von zwischen 25 und 45 € anzuzeigen.

1. Legen Sie einen Preisbereich für die Produkte fest, die Sie empfehlen möchten.
1. Legen Sie den Mindestbestand für die Produkte fest, die Sie empfehlen möchten.
1. Konfigurieren Sie die Empfehlung, um nur Artikel anzuzeigen, wenn sie bestimmte Kriterien erfüllen.

   ![](assets/Recs_InclusionRules.png)

   Sie können angeben, dass Artikel nur berücksichtigt werden, wenn eines der Attribute in der Liste eine oder mehrere angegebene Bedingungen erfüllt oder nicht erfüllt.

   Die verfügbaren Auswerter sind von dem Wert abhängig, den Sie in der ersten Dropdownliste auswählen. Sie können mehrere Elemente auflisten. Diese Artikel werden durch ODER ausgewertet.

   Mehrere Regeln werden mit „AND“ kombiniert.

   >[!NOTE]
   >
   >Diese Option beschränkt die in der Empfehlung angezeigten Elemente. Sie hat keine Auswirkungen darauf, auf welchen Seiten die Empfehlung angezeigt wird. Um eine Einschränkung bezüglich der Anzeige der Empfehlung vorzunehmen, wählen Sie die Seiten im Experience Composer aus.

Weitere Informationen finden Sie unter [Dynamische und statische Einschlussregeln verwenden](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Attributgewichtung {#weighting}

Sie können mehrere Regeln hinzufügen, um den Algorithmus basierend auf wichtigen Informationen oder Metadaten zum Inhaltskatalog zu &quot;verschieben&quot;, sodass bestimmte Elemente mit höherer Wahrscheinlichkeit angezeigt werden.

So haben Sie zum Beispiel die Möglichkeit, rabattierten Artikeln eine höherer Gewichtung zu verleihen, damit sie öfter in den Empfehlungen erscheinen. Artikel, die nicht Teil des Sonderangebots sind, werden nicht vollständig ausgeschlossen, jedoch weniger häufig angezeigt. Auf denselben Algorithmus können mehrere gewichtete Attribute angewendet werden und die gewichteten Attribute können mit dem in der Empfehlung aufgeteilten Traffic getestet werden.

1. Wählen Sie einen Wert aus.

   Der Wert bestimmt den Typ des Elements, das mit größerer Wahrscheinlichkeit und auf der Basis mehrerer verfügbarer Kriterien angezeigt wird.

1. Wählen Sie einen Auswerter.

1. Geben Sie das Keyword ein, um die Regelattribute abzuschließen.

   Die vollständige Regel könnte beispielsweise &quot;Kategorie enthält Unterzeichenfolgen-Schuhe&quot;lauten.

   ![](assets/Recs_AttributeWeighting.png)

1. Wählen Sie die Wertigkeit aus, die der Regel zugeordnet werden soll.

   Die Gewichtung kann von 0 bis 100 in 25er-Schritten eingestellt werden.

1. Fügen Sie nach Bedarf weitere Regeln hinzu.

Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Wenn Sie eine neue [!UICONTROL Recommendations]-Aktivität erstellen oder eine bestehende bearbeiten, wird das Kontrollkästchen **[!UICONTROL Kriterien für später speichern]** automatisch aktiviert. Sollten Sie die Kriterien nicht in anderen Aktivitäten verwenden wollen, deaktivieren Sie das Kontrollkästchen, bevor Sie speichern.

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33) ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
