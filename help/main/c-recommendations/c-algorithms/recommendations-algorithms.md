---
keywords: Empfehlungsalgorithmen; Modellschulung; Modellbereitstellung; Inhaltsbereitstellung; artikelbasiert; benutzerbasiert; Beliebtheitsbasiert; Warenkorb-basiert; benutzerdefinierte Kriterien
description: Erfahren Sie mehr über die in [!DNL Target Recommendations] verwendeten Algorithmen, einschließlich Modellschulung und Modellbereitstellung.
title: Wo erhalte ich Informationen über die Wissenschaft hinter den Recommendations-Algorithmen von Target?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
mini-toc-levels: 2
exl-id: c156952b-8eda-491d-a68e-d3d09846f640
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2739'
ht-degree: 0%

---

# Die Wissenschaft hinter den Empfehlungsalgorithmen von Target

Eine ausführliche Beschreibung der in [!DNL Adobe Target Recommendations] verwendeten Algorithmen, einschließlich der Logik und mathematischen Details der Modellschulung und des Prozesses der Modellbereitstellung.

Modellschulung ist der Prozess, wie Empfehlungen von den [!DNL Adobe Target]-Lernalgorithmen generiert werden. Das Modell-Serving stellt dar, wie [!DNL Target] Empfehlungen für Ihre Site-Besucher bereitstellt (auch als Inhaltsbereitstellung bezeichnet).

[!DNL Target] enthält die folgenden umfassenden Typen von Algorithmen in [!DNL Recommendations]:

* **Artikelbasierte Algorithmen**: Fügen Sie Algorithmen ein, die der Logik folgen: &quot;Personen, die diesen Artikel angesehen/gekauft haben, haben auch diese Artikel angesehen/gekauft.&quot; Diese Algorithmen werden unter dem Dachbegriff kollaboratives Filtern von item-item sowie [!UICONTROL Items with Similar Attributes] Algorithmen gruppiert.

* **Benutzerbasierte Algorithmen**: Schließen Sie die Algorithmen [!UICONTROL Recently Viewed] und [!UICONTROL Recommended for You] ein.

* **Beliebtheitsbasierte Algorithmen**: Binden Sie Algorithmen ein, die die am häufigsten angezeigten oder am häufigsten gekauften Artikel auf der Website oder die am häufigsten angezeigten Artikel oder die am häufigsten angezeigten Artikel nach Kategorie oder Artikelattribut zurückgeben.

* **Warenkorb-basierte Algorithmen**: Schließen Sie Empfehlungen, die auf mehreren Artikeln basieren, mit der Logik ein, &quot;Personen, die diese Artikel angesehen/gekauft haben, haben auch diese Artikel angesehen/gekauft&quot;.

* **Benutzerdefinierte Kriterien**: Schließen Sie Empfehlungen basierend auf benutzerdefinierten Dateien ein, die in [!DNL Target] hochgeladen wurden.

>[!NOTE]
>
>Allgemeine Informationen zu den einzelnen Algorithmustypen und den einzelnen Algorithmen finden Sie unter [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

Viele der oben aufgeführten Algorithmen basieren auf einem oder mehreren Schlüsseln. Mit diesen Schlüsseln werden ähnliche Elemente zum Zeitpunkt der Inhaltsbereitstellung (wenn Empfehlungen abgegeben werden) abgerufen. Kundenspezifische Schlüssel können das aktuelle Element, das von einem Besucher angezeigt wird, das zuletzt angezeigte oder gekaufte Element, das am häufigsten angezeigte Element, die aktuelle Kategorie oder die bevorzugte Kategorie für diesen Besucher enthalten. Andere Algorithmen, wie z. B. auf dem Warenkorb basierende oder benutzerbasierte Empfehlungen, verwenden implizite Schlüssel (die vom Kunden nicht konfiguriert werden können). Weitere Informationen finden Sie unter *Empfehlungsschlüssel* in [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys). Beachten Sie jedoch, dass diese Schlüssel nur zur Modellbereitstellungszeit (Inhaltsbereitstellung) relevant sind. Diese Schlüssel wirken sich nicht auf die &quot;Offline&quot;- oder Modellschulungszeitlogik aus.

In den folgenden Abschnitten werden Algorithmen etwas anders gruppiert als die oben beschriebenen Algorithmustypen. Die folgende Gruppierung basiert auf der Ähnlichkeit der Trainings-Logik des Modells.

## Partizipative Filterung nach Elementen

Zu den Algorithmen gehören:

* [!UICONTROL People Who Viewed This, Viewed That]
* [!UICONTROL People Who Viewed This, Bought That]
* [!UICONTROL People Who Bought This, Bought That]

Empfehlungsalgorithmen für das partizipative Filtern von Elementen basieren auf der Idee, dass Sie die Verhaltensmuster vieler Benutzer (daher kollaborativ) verwenden sollten, um nützliche Empfehlungen für ein bestimmtes Element bereitzustellen (z. B. Filtern des Katalogs möglicher Artikel, die empfohlen werden sollen). Obwohl es viele verschiedene Algorithmen gibt, die unter den allgemeinen Rahmen von [kollaborativer Filterung](https://en.wikipedia.org/wiki/Collaborative_filtering) fallen, verwenden diese Algorithmen allgemein Verhaltensdatenquellen als Eingaben. In [!DNL Target Recommendations] sind diese Eingaben die individuellen Ansichten und Käufe von Artikeln durch Benutzer.

Für den Algorithmus &quot;Personen, die diesen Artikel angesehen/gekauft haben, haben auch diese Artikel angesehen/gekauft&quot;besteht das Ziel darin, eine Ähnlichkeit zwischen allen Artikelpaaren zu berechnen. Für einen bestimmten Artikel A werden die wichtigsten Empfehlungen dann nach ihrer Ähnlichkeit (A, B) geordnet.

Ein Beispiel für eine solche Ähnlichkeit ist das gemeinsame Auftreten zwischen Artikeln: eine einfache Zählung der Anzahl der Benutzer, die beide Artikel gekauft haben. Obwohl intuitiv, ist eine solche Metrik naiv, da sie dazu neigt, beliebte Artikel zu empfehlen. Wenn beispielsweise in einem Lebensmittelhändler die meisten Menschen Brot kaufen, wird Brot mit allen Artikeln häufig vorkommen, aber es ist nicht unbedingt eine gute Empfehlung. [!DNL Target] verwendet stattdessen eine ausgefeiltere Ähnlichkeitsmetrik, die als Protokoll-Wahrscheinlichkeitsverhältnis (LLR) bezeichnet wird. Diese Menge ist groß, wenn die Wahrscheinlichkeit, dass zwei Elemente, A und B, gleichzeitig auftreten, sich von der Wahrscheinlichkeit unterscheidet, dass sie nicht gleichzeitig auftreten. Betrachten Sie aus Gründen der Konkretheit einen Fall des [!UICONTROL People Who Viewed This, Bought That]-Algorithmus. Die Ähnlichkeit des LLR ist groß, wenn die Wahrscheinlichkeit, dass B gekauft wurde, *nicht* ist, unabhängig davon, ob jemand A angesehen hat.

Wenn z. B.

![Formel für den angezeigten/gekauften Algorithmus](assets/formula.png)

dann sollte Element B nicht zusammen mit Element A empfohlen werden. Vollständige Details zu dieser Berechnung der Ähnlichkeitsrate des Protokollwahrscheinlichkeitsverhältnisses finden Sie in dieser PDF](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf) unter [.

Der logische Ablauf der eigentlichen Algorithmusimplementierung wird im folgenden Schemadiagramm dargestellt:

![Schemadiagramm eines angezeigten/gekauften Algorithmus](assets/diagram1.png)

Diese Schritte werden im Einzelnen wie folgt beschrieben:

* **Eingabedaten**: Verhaltensdaten in Form von Ansichten und Käufen von Besuchern, die erfasst werden, wenn Sie [Target](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} oder [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank} implementieren.

* **Modellschulung**:

   * **Datenbereinigung und -bearbeitung**: Für Algorithmen mit einem N-Tage-Lookback werden die Verhaltensdaten zunächst so gefiltert, dass nur die n Tage an Daten einbezogen werden. Sammlungsregeln und globale Ausschlüsse werden dann angewendet, um alle Elemente zu entfernen, die nicht empfohlen werden sollten. Schließlich lassen sich bei Besuchern, die mit mehr als 1.000 Artikeln interagiert haben, nur Nutzungsdaten von 1.000 Artikeln abrufen.
   * **Berechnung der Artikelähnlichkeit**: Dies ist der wichtigste Rechenschritt: Berechnung der Protokollwahrscheinlichkeitsverhältnisähnlichkeit zwischen allen Kandidaten-Element-Paaren und Rangpaaren von Elementen anhand dieses Ähnlichkeitswerts.
   * **Offline-Filterung**: Schließlich werden alle weiteren anwendbaren dynamischen Filter angewendet (z. B. dynamische Kategorieausschlüsse). Nach diesem Schritt werden vorberechnete Empfehlungen global zwischengespeichert und stehen somit zur Verfügung.

* **Modellbereitstellung**: Recommendations-Inhalte werden vom [!DNL Target] globalen &quot;Edge&quot;-Netzwerk bereitgestellt ](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934). [ Wenn Mbox-Anfragen an [!DNL Target] gesendet werden und festgestellt wird, dass Empfehlungsinhalte an die Seite gesendet werden sollen, wird die Anforderung für den entsprechenden [Elementschlüssel](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#keys) für den Empfehlungsalgorithmus entweder aus der Anforderung analysiert oder aus dem Benutzerprofil nachgeschlagen und dann zum Abrufen der Empfehlungen verwendet, die in den vorherigen Schritten berechnet wurden. Zu diesem Zeitpunkt werden weitere dynamische Filter angewendet, bevor das entsprechende [Design](/help/main/c-recommendations/c-design-overview/create-design.md) gerendert wird.

## Ähnlichkeit von Inhalten

Algorithmus enthalten:

* [!UICONTROL Items with Similar Attributes]

Bei diesem Algorithmustyp werden zwei Elemente als verwandt betrachtet, wenn ihre Namen und textlichen Beschreibungen semantisch ähnlich sind. Im Gegensatz zu den meisten Empfehlungsalgorithmen, in denen Verhaltensdatenquellen verwendet werden müssen, verwenden Algorithmen zur Ähnlichkeit von Inhalten Metadaten aus Produktkatalogen, um die Ähnlichkeit zwischen Artikeln abzuleiten. [!DNL Target] kann daher Empfehlungen in so genannten &quot;Cold-Start&quot;-Szenarien fördern, in denen keine Verhaltensdaten erfasst wurden (z. B. zu Beginn einer [!DNL Target] -Aktivität).

Auch wenn die Aspekte der Modellbereitstellung und Inhaltsbereitstellung der Ähnlichkeitsalgorithmen von [!DNL Target] mit anderen elementbasierten Algorithmen identisch sind, unterscheiden sich die Trainings-Schritte für das Modell erheblich und umfassen eine Reihe von Schritten zur natürlichen Sprachverarbeitung und Vorverarbeitung, wie im folgenden Diagramm dargestellt. Kernstück der Ähnlichkeitsberechnung ist die Verwendung der Kosinähnlichkeit modifizierter tf-idf-Vektoren, die jedes Element im Katalog darstellen.

![Diagramm, das den Fluss des Prozesses der Ähnlichkeit von Inhalten anzeigt](assets/diagram2.png)

Diese Schritte werden im Einzelnen wie folgt beschrieben:

* **Eingabedaten**: Wie zuvor beschrieben, basiert dieser Algorithmus ausschließlich auf Katalogdaten (die über einen [Katalog-Feed, die Entitäten-API oder über On-Page-Updates in [!DNL Target] erfasst werden).](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}

* **Modellschulung**:

   * **Attributextraktion**: Nach der Anwendung regulärer statischer Filter, Katalogregeln und globaler Ausnahmen extrahiert dieser Algorithmus relevante Textfelder aus dem Entitätsschema. [!DNL Target] verwendet automatisch die Felder Name, Nachricht und Kategorie aus den Entitätsattributen und versucht, alle Zeichenfolgenfelder aus benutzerdefinierten [Entitätsattributen](/help/main/c-recommendations/c-products/entity-attributes.md) zu extrahieren. Dies geschieht, indem sichergestellt wird, dass die meisten Werte für dieses Feld nicht als Zahl, Datum oder boolesch analysiert werden können.
   * **Entfernen von Wortstämmen und Stoppwörtern**: Für eine genauere Übereinstimmung der Textähnlichkeit ist es ratsam, sehr häufig verwendete &quot;Stoppwörter&quot;zu entfernen, die die Bedeutung eines Elements nicht wesentlich ändern (z. B. &quot;war&quot;, &quot;ist&quot;, &quot;und&quot;usw.). Auf ähnliche Weise bezieht sich Wortstamm auf den Prozess der Reduzierung von Wörtern mit verschiedenen Suffixen auf ihr Stammwort, das eine identische Bedeutung hat (z. B. &quot;Verbinden&quot;, &quot;Verbinden&quot;und &quot;Verbindung&quot;haben alle dasselbe Stammwort: &quot;Verbinden&quot;). [!DNL Target] verwendet den Snowballstempel. [!DNL Target] führt zuerst eine automatische Spracherkennung durch und kann das Entfernen von Wörtern für bis zu 50 Sprachen und für 18 Sprachen stoppen.
   * **n-Gramm-Erstellung**: Nach den vorherigen Schritten wird jedes Wort als Token behandelt. Der Prozess, zusammenhängende Sequenzen von Token zu einem einzigen Token zu kombinieren, wird als n-Gramm-Erstellung bezeichnet. Die Algorithmen von [!DNL Target] berücksichtigen bis zu 2 Gramm.
   * **tf-idf computation**: Der nächste Schritt umfasst die Erstellung von tf-idf-Vektoren, die die relative Wichtigkeit von Token in der Elementbeschreibung widerspiegeln. Für jeden Token/Begriff t in einem Element i in einem Katalog D mit |D| -Elemente, wird der Begriff Häufigkeit TF(t, i) zuerst berechnet (die Häufigkeit, mit der der Begriff im Element i erscheint), sowie die Dokumentfrequenz DF(t, D). Im Wesentlichen die Anzahl der Elemente, in denen das Token vorhanden ist. Die tf-idf-Maßnahme ist dann

     ![Formel mit tf-idf-Kennzahl](assets/formula2.png)

     [!DNL Target] verwendet die Apache Spark-Funktionsimplementierung *tf-idf*, die unter der Haube jedes Token auf einen Bereich von 218 Token hasst. In diesem Schritt wird das kundenspezifische Attribut Boosting und Burying auch angewendet, indem die Begriffsfrequenzen in jedem Vektor basierend auf den in den [Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#similarity) angegebenen Einstellungen angepasst werden.

   * **Berechnung der Elementähnlichkeit**: Die Berechnung der endgültigen Elementähnlichkeit erfolgt mithilfe einer Näherungskosinähnlichkeit. Bei zwei Elementen, *A* und *B*, mit den Vektoren tA und tB, wird die Kosinähnlichkeit wie folgt definiert:

     ![Formel, die die Berechnung der Elementähnlichkeit anzeigt](assets/formula3.png)

     Um eine signifikante Komplexität bei der Berechnung der Ähnlichkeiten zwischen allen N x N Elementen zu vermeiden, wird der Vektor *tf-idf* so abgeschnitten, dass er nur die größten 500 Einträge enthält, und dann werden die Kosinähnlichkeiten zwischen Elementen mithilfe dieser abgeschnittenen Vektordarstellung berechnet. Dieser Ansatz erweist sich als robuster für die Berechnung der geringen Vektorähnlichkeit im Vergleich zu anderen nahe gelegenen Angrenzenmethoden (ANN), z. B. beim Hashing durch lokale Gegebenheiten.

   * **Modellbereitstellung**: Dieser Prozess entspricht den kollaborativen Filtertechniken für Elemente, die im vorherigen Abschnitt beschrieben wurden.

## Mehrschlüssel-Empfehlungen

Zu den Algorithmen gehören:

* Warenkorbbasierte Empfehlungen
* [!UICONTROL Recommended For You]

Die letzten Ergänzungen der [!DNL Target]-Suite mit Empfehlungsalgorithmen sind [!UICONTROL Recommended For You] und eine Reihe von auf Warenkorb basierenden Empfehlungsalgorithmen. Beide Algorithmustypen verwenden kollaborative Filtermethoden, um einzelne elementbasierte Empfehlungen zu bilden. Anschließend werden zur Bereitstellungszeit mehrere Elemente im Browser-Verlauf des Benutzers (für [!UICONTROL Recommended For You]) oder im aktuellen Warenkorb des Benutzers (für kartbasierte Empfehlungen) verwendet, um diese artikelbasierten Empfehlungen abzurufen, die dann zusammengeführt werden, um die endgültige Liste der Empfehlungen zu bilden. Beachten Sie, dass es viele Varianten personalisierter Empfehlungsalgorithmen gibt. Die Auswahl eines Algorithmus mit mehreren Schlüsseln bedeutet, dass Empfehlungen sofort verfügbar sind, nachdem ein Besucher über einen Browserverlauf verfügt, und dass Empfehlungen aktualisiert werden können, um auf das neueste Besucherverhalten zu reagieren.

Diese Algorithmen basieren auf den im Abschnitt elementbasierte Empfehlungen beschriebenen kollaborativen Filtermethoden, enthalten aber auch eine Hyperparameter-Optimierung, um die optimale Ähnlichkeitsmetrik zwischen Artikeln zu ermitteln. Der Algorithmus führt eine chronologische Aufspaltung der Verhaltensdaten für jeden Benutzer durch und trainiert Empfehlungsmodelle für frühere Daten, während versucht wird, die Artikel vorherzusagen, die ein Benutzer später ansieht oder kauft. Die Ähnlichkeitsmetrik, die die optimale Durchschnittsgenauigkeit [1} ergibt (https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval) wird dann ausgewählt.]

Die Logik der Trainings- und Scoring-Schritte für Modelle wird im folgenden Diagramm dargestellt:

![Diagramm, das die Logik der Schritte zum Trainieren und Scoring des Modells zeigt](assets/diagram3.png)

Diese Schritte werden im Einzelnen wie folgt beschrieben:

* **Eingabedaten**: Dies entspricht den Methoden des partizipativen Filterns (CF) von Elementen. [!UICONTROL Both Recommended For You]- und Warenkorbbasierte Algorithmen verwenden Verhaltensdaten in Form von Ansichten und Käufen von Benutzern, die erfasst werden, wenn Sie [Target](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} oder [Adobe Analytics](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md){target=_blank} implementieren.

* **Modellschulung**:

   * **Datenbereinigung und -bearbeitung**: Dies entspricht auch bei kollaborativen Filtermethoden, bei denen das Lookback-Fenster angewendet wird, um Verhaltensdaten in einen geeigneten Datumsbereich zu filtern, gefolgt von der Anwendung von Katalogregeln und globalen Ausschlüssen. Bei Besuchern, die mit mehr als 1.000 Artikeln interagiert haben, werden nur die letzten 1.000 Verwendungen berücksichtigt.
   * **Trainingstest-Aufspaltung**: Führen Sie für jeden Benutzer eine chronologische Aufspaltung der Nutzung durch, wobei die ersten 80 % seiner Nutzung Trainings-Daten zugeordnet werden, wobei die verbleibenden 20 % den Testdaten zugeordnet werden.
   * **Trainieren des Modells für die Ähnlichkeit von Elementen**: Die Berechnung der Ähnlichkeit von Kernelementen unterscheidet sich für [!UICONTROL Recommended For You] und kartenbasierte Algorithmen in der Art und Weise, wie die Vektorobjektvektor erstellt werden. Für [!UICONTROL Recommended For You] haben die Element-Vektoren die Dimension &quot;Benutzer&quot;, wobei jeder Eintrag die Summe der impliziten Bewertungen für diesen Benutzer des Artikels darstellt. Für Käufe eines Artikels wird eine Gewichtung von 2x so hoch wie für Ansichten des Artikels angegeben. Für kartbasierte Empfehlungen haben die Element-Vektoren binäre Einträge. Wenn nur das Verhalten innerhalb einer Sitzung berücksichtigt werden soll, gibt es einen neuen Eintrag für jede Sitzung. Andernfalls gibt es einen Eintrag in diesem Element-Vektor für jeden Besucher.

  Der Schulungsschritt berechnet verschiedene Arten von Vektorähnlichkeiten: die LLR-Ähnlichkeit ([hier besprochen](/help/main/c-recommendations/c-algorithms/assets/log-likelihood-ratios-recommendation-algorithms.pdf)), die Kosinähnlichkeit (zuvor definiert) und eine normalisierte L2-Ähnlichkeit, definiert als:

  ![Formel zur Anzeige der Trainings-Berechnung](assets/formula4.png)

   * **Bewertung des Modells für Elementähnlichkeit**: Die Modellauswertung erfolgt anhand der im vorherigen Schritt generierten Empfehlungen und anhand von Prognosen zum Testdatensatz. Die Online-Scoring-Phase wird nachgeahmt, indem die Elementverwendungen der einzelnen Benutzer im Testdatensatz chronologisch geordnet werden und dann 100 Empfehlungen für geordnete Untergruppen von Artikeln abgegeben werden, um zu versuchen, nachfolgende Ansichten und Käufe vorherzusagen. Eine Metrik zum Abrufen von Informationen, die &quot;Mittlere durchschnittliche Genauigkeit&quot;](https://en.wikipedia.org/wiki/Evaluation_measures_(information_retrieval)), wird verwendet, um die Qualität dieser Empfehlungen zu bewerten. [ Diese Metrik berücksichtigt die Reihenfolge der Empfehlungen und bevorzugt relevante Artikel, die höher oben in der Empfehlungsliste stehen. Dies ist eine wichtige Eigenschaft für Ranking-Systeme.
   * **Modellauswahl**: Nach der Offline-Auswertung wird das Modell mit der höchsten durchschnittlichen Genauigkeit ausgewählt und alle für das Element berechneten Empfehlungen.
   * **Offline-Filterung**: Der letzte Schritt der Modellschulung ist die Anwendung aller zutreffenden dynamischen Filter. Nach diesem Schritt werden vorberechnete Empfehlungen global zwischengespeichert und stehen somit zur Verfügung.

* **Modellbereitstellung**: Im Gegensatz zu früheren Algorithmen, bei denen Empfehlungen bereitgestellt werden, indem ein einzelner Schlüssel für den Abruf und anschließend die Anwendung von Geschäftsregeln spezifiziert wird, verwenden die [!UICONTROL Recommended for You]- und Warenkorbbasierten Algorithmen einen komplexeren Laufzeitprozess.

   * **Abrufen und Zusammenführen mit mehreren Schlüsseln**: Bei kartbasierten Empfehlungen werden bis zu zehn im Warenkorb übergebene Artikel als Schlüssel für den Abruf betrachtet und Empfehlungen aus jedem dieser Artikel werden gleichmäßig gewichtet. Für [!UICONTROL Recommended for You] werden bis zu den letzten fünf einzelnen angezeigten Artikeln und den letzten fünf individuellen gekauften Artikeln als Schlüssel zum Abrufen betrachtet, wobei Empfehlungen aus gekauften Artikeln doppelt so stark gewichtet werden wie Empfehlungen aus aufgerufenen Artikeln. Wenn beim Zusammenführen von Empfehlungen ein Element in mehreren individuellen Empfehlungslisten angezeigt wird, werden seine gewichteten Ähnlichkeitswerte hinzugefügt. Die endgültige Liste der Empfehlungen aus dieser Phase ist dann die zusammengeführte Liste neu gewichteter Empfehlungen, die in absteigender Reihenfolge aufgeführt werden.
   * **Filterung**: Als Nächstes werden Filterregeln wie das Entfernen zuvor angezeigter und/oder gekaufter Artikel sowie andere dynamische Geschäftsregeln angewendet.

Diese Prozesse werden in der folgenden Abbildung veranschaulicht, in der ein Besucher Artikel A und Artikel B gekauft hat. Einzelne Empfehlungen werden mit den unter jeder Artikelbezeichnung angezeigten Offline-Ähnlichkeitswerten abgerufen. Nach dem Abrufen werden die Empfehlungen mit den bewerteten Ähnlichkeitswerten zusammengeführt. Schließlich werden in einem Szenario, in dem der Kunde angegeben hat, dass zuvor angezeigte und gekaufte Artikel herausgefiltert werden müssen, im Filterschritt die Elemente A und B aus der Liste der Empfehlungen entfernt.

![Diagramm, das die Verarbeitung von Algorithmen mit mehreren Schlüsseln anzeigt](assets/diagram4.png)

## Popularitätsbasiert

Zu den Algorithmen gehören:

* [!UICONTROL Most Viewed Across the Site]
* [!UICONTROL Most Viewed by Category]
* [!UICONTROL Most Viewed by Item Attribute]
* [!UICONTROL Top Sellers Across the Site]
* [!UICONTROL Top Sellers by Category]
* [!UICONTROL Top Sellers by Item Attribute]

[!DNL Target] bietet beliebungsbasierte Algorithmen für die beiden am häufigsten angezeigten Elemente sowie die am häufigsten verkauften Artikel auf einer Website oder aufgeschlüsselt nach einem Artikelattribut oder einer Kategorie. Beliebtheitsbasierte Algorithmen ordnen Elemente basierend auf der Anzahl der Sitzungen, in denen der Artikel in einem bestimmten Zeitraum angezeigt oder gekauft wurde.

Alle diese Algorithmen kombinieren aggregierte Verhaltensdaten, bei denen die Gesamtzahl der Sitzungen, in denen Artikel angezeigt und gekauft wurden, sowohl bei stündlichen als auch bei täglichen Auflösungen aufgezeichnet wird. Einzelne Algorithmen finden dann die am häufigsten angezeigten oder am häufigsten gekauften Artikel für das kundenkonfigurierte Lookback-Fenster.

Die einzelnen Algorithmusnuancen lauten wie folgt:

* [!UICONTROL Most Viewed Across the Site] und [!UICONTROL Top Sellers Across the Site] ordnen Elemente nach der aggregierten Anzahl der Sitzungen, in denen diese Artikel angezeigt bzw. gekauft wurden. Die Ausgabe ist eine einzelne (schlüssellose) Liste empfohlener Elemente.
* Die meisten angezeigten/Topverkäufe nach Kategorie-/Artikelattribut sind Empfehlungen, bei denen Artikel nach der aggregierten Anzahl der Sitzungen sortiert werden, in denen diese Artikel angezeigt oder gekauft wurden, jedoch nach Artikelkategorie oder spezifischem Artikelattribut gruppiert wurden. Die Ausgaben sind Listen mit empfohlenen Artikeln, die nach Werten von Kategorien oder Werten von Elementattributen eingegeben werden.

## Kürzlich angezeigt

Der Empfehlungsalgorithmus &quot;Kürzlich angezeigt&quot;ermöglicht die Personalisierung von Empfehlungen in einer Sitzung. Dieser Algorithmus erfordert keine Offline-Modellschulung. Stattdessen verwendet [!DNL Target] das eindeutige [Besucherprofil](/help/main/c-target/c-visitor-profile/visitor-profile.md) , um eine laufende Liste von Artikeln zu verwalten, die in einer bestimmten Sitzung angezeigt wurden, und kann diese Elemente in Recommendations-Aktivitäten aufdecken. Dies ermöglicht Echtzeitaktualisierungen von Empfehlungen und die Personalisierung der nächsten Seite.

## Benutzerdefinierte Kriterien

Benutzerdefinierte Kriterien ermöglichen es Kunden, [ihre eigenen Empfehlungen in  [!DNL Target]](/help/main/c-recommendations/c-algorithms/recommendations-csv.md) hochzuladen, wodurch eine wichtige Flexibilität entsteht und die Möglichkeit geboten wird, ein eigenes Modell zu entwickeln. Benutzerdefinierte Kriterien ersetzen den Teil &quot;Offline-Schulung&quot;von [!UICONTROL Item-Based] Empfehlungen, verhalten sich jedoch während der Bereitstellungsphase von Online-Inhalten ähnlich wie artikelbasierte Empfehlungsalgorithmen, da dann ein einzelner Schlüssel zum Abrufen von Empfehlungen verwendet wird und Geschäftsregeln/Filter angewendet werden.
