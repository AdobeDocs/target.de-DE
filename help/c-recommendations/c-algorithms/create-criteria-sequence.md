---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;
description: Verwenden Sie Sequenzen von bis zu fünf Kriterien, um die Elemente, die in Ihren Adobe Target Recommendations-Aktivitäten angezeigt werden, besser zu kontrollieren.
title: Erstellen von Kriteriensequenzen
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: 381c405e55475f2474881541698d69b87eddf6fb
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 44%

---


# ![PREMIUM](/help/assets/premium.png) Kriteriensequenzen erstellen

Verwenden Sie Sequenzen von bis zu fünf Kriterien, um mehr Kontrolle über die Elemente zu erhalten, die in Ihren [!UICONTROL Recommendations]-Aktivitäten angezeigt werden.

>[!NOTE]
>
>Kriteriensequenzen können nicht mit [!UICONTROL Empfehlungs]-Aktivitäten verwendet werden, die vor der Version Oktober 2016 von [!DNL Target Premium] erstellt wurden.

Bevor Sie eine Kriteriensequenz erstellen können, müssen Sie zuerst die Kriterien erstellen, die in der Sequenz stehen sollen. Siehe [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) für weitere Informationen.

Mithilfe einer Kriteriensequenz können Sie zusätzliche gezielte Empfehlungen bereitstellen, anstatt allgemeinere Reserveempfehlungen zu verwenden, wenn ein Kriterium nicht genügend Ergebnisse zurückgibt, um Ihr Design zu füllen. In der Regel wird eine Kriteriensequenz vom spezifischeren Targeting, das möglicherweise weniger Ergebnisse zurückgibt, zum allgemeineren Targeting fortgesetzt, das in der Regel mehr Ergebnisse zurückgibt.

Die Sequenzen Ihrer Kriterien können je nach Seitentyp variieren, wie in den folgenden Beispielen gezeigt:

| Seitentyp | Mögliche Sequenzreihenfolge |
| --- | --- |
| Produktseite | <ol><li>Basierend auf dem aktuellen Artikel, von der gleichen Marke</li><li>Basierend auf dem aktuellen Artikel, von allen Marken</li><li>Basierend auf Inhaltsähnlichkeit</li><li>Basierend auf Topverkäufen</li><li>Basierend auf Artikeln, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |
| Startseite | <ol><li>Basierend auf dem letzten Einkauf des Besuchers </li><li>Basierend auf dem Lieblingsartikel des Besuchers</li><li>Basierend auf der Lieblingskategorie des Besuchers</li><li>Basierend auf Topverkäufen</li><li>Basierend auf den Elementen, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |

## Auf den Bildschirm &quot;Kriteriensequenz erstellen&quot;zugreifen

Es gibt mehrere Möglichkeiten, um auf den Bildschirm [!UICONTROL Kriteriensequenz erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm der Bibliothek **[!UICONTROL Empfehlungen]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!UICONTROL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!UICONTROL Recommendations] -Aktivität erstellen, klicken Sie im Bildschirm &quot;Kriterien auswählen&quot;auf Neu **** erstellen > Kriteriensequenz **[!UICONTROL erstellen]**. Sie haben die Möglichkeit, Ihre neue Kriteriensequenz zu speichern, um sie mit anderen [!UICONTROL Recommendations]-Aktivitäten zu verwenden.
* When you are editing a [!UICONTROL Recommendations] activity, click in a [!UICONTROL Recommendations Location] box on your page, then select **[!UICONTROL Change Criteria]**. Klicken Sie im Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!UICONTROL Recommendations]-Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf den Bildschirm &quot;Kriteriensequenz [!UICONTROL erstellen&quot;zugreifen] : den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf Kriterien **[!UICONTROL erstellen]** > Kriteriensequenz **[!UICONTROL erstellen]**.

   ![](assets/CreateCriteriaSequence.png)

## Füllen Sie den Abschnitt Informationen aus

1. Geben Sie einen **[!UICONTROL Namen]** für die Sequenz ein.

   Dies ist der „interne“ Name, der zur Beschreibung der Kriteriensequenz dient. Besuchern Ihrer Website wird dieser Name nicht angezeigt.

   ![Abschnitt &quot;Kriteriensequenz erstellen&quot;](/help/c-recommendations/c-algorithms/assets/criteria-sequence-info.png)

1. Geben Sie einen öffentlich sichtbaren **[!UICONTROL generischen Anzeigetitel]** ein, der auf der Seite angezeigt werden soll, wenn zum Ausfüllen des [!UICONTROL Empfehlungs]-Entwurfs mehrere Kriterien in der Sequenz verwendet werden.

   Ein Beispiel: Sie möchten die Zeichenfolge „Kunden, die diesen Artikel angezeigt haben, haben sich auch interessiert für …“ ersetzen. Stattdessen soll „Für Sie empfohlen“ angezeigt werden, wenn das Design Artikel enthält, die auf mehreren [!UICONTROL Recommendations]-Schlüsseln basieren.

1. Geben Sie eine kurze **[!UICONTROL Beschreibung]** der Kriteriensequenz ein.

   Die Beschreibung sollte Ihnen dabei helfen, die Kriteriensequenz zu identifizieren, und kann Informationen über ihren Zweck enthalten.

1. Wählen Sie eine Branche, die auf den Zielen Ihrer Recommendations-Aktivität basiert.

   | Vertikaler Markt | Ziel |
   |--- |--- |
   | Einzelhandel/E-Commerce | Zum Kauf führende Konversion |
   | Lead-Generierung/B2B/Finanzdienstleistungen | Konversion ohne Kauf |
   | Medien/Verlagswesen | Interaktion |

   Ihr standardmäßiger vertikaler Markt wird automatisch angezeigt.

   Andere Optionen für Kriterien ändern sich auf Grundlage des vertikalen Markts, den Sie auswählen.

1. Wählen Sie einen **[!UICONTROL Seitentyp]** aus.

   Verschiedene Seitentypen stehen zur Verfügung.

   Vertikaler Markt und Seitentypen dienen beide zusammen zur Kategorisierung Ihrer gespeicherten Kriteriensequenz, was die Wiederverwendung von Sequenzen für andere [!UICONTROL Recommendations]-Aktivitäten vereinfacht.

## Sequenz erstellen {#sequence}

Die Reihenfolge der Sequenz definiert die Reihenfolge, in der ein Entwurf gefüllt wird. Wenn Kriterium 1 nicht genügend Empfehlungen zum Ausfüllen Ihres Entwurfs enthält, werden die verbleibenden Plätze mit Kriterium 2 usw. ausgefüllt.

1. Klicken Sie im Abschnitt **[!UICONTROL Kriteriensequenz]** auf **[!UICONTROL Hinzufügen Kriterien]**.

   ![hinzufügen](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. On the [!UICONTROL Select Criteria] screen, select a criteria.

   Sie können das Suchfeld und die Filter-Dropdownliste verwenden, um die gewünschten Kriterien zu finden.

   ![Kriterienauswahl](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. Klicken Sie auf **[!UICONTROL Hinzufügen]**.

1. (Optional) Schieben Sie die **[!UICONTROL Begrenzung der Anzahl der zurückgegebenen]** Elemente auf die Position &quot;Ein&quot;und geben Sie dann die Anzahl der Elemente an (zwischen 1 und 50).

   ![Anzahl der zurückgegebenen Elemente begrenzen](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Um den Wert der Option &quot;Anzahl der zurückgegebenen [!UICONTROL Elemente] begrenzen&quot;besser zu verstehen, sollten Sie die folgenden Anwendungsfälle berücksichtigen:

   * **Verwendungsfall 1**: Sie möchten eine Mischung aus verschiedenen Arten von Artikeln in einer einzigen Recommendations-Ablage haben. Sie möchten beispielsweise eine Mischung aus Oberbekleidung (Jacken) und Oberteil (Hemden, T-Shirts) zeigen. Um dies zu erreichen, verwenden Sie eine Sammlung für die Aktivität, die alle potenziellen Produkttypen enthält, die Sie in beliebigen Slots in Ihrem Design verwenden möchten. Richten Sie dann Ihre ersten Kriterien mit einem statischen Filter ein, der die Kriterien auf nur Oberbekleidung beschränkt, und richten Sie Ihr zweites Kriterium mit einem statischen Filter ein, der die Kriterien auf nur Oberteile beschränkt. Fügen Sie schließlich beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

      Die Empfehlungsablage könnte auf Ihrer Site wie folgt aussehen:

      ![Empfehlungsbereich für spezielle Produkte](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Anwendungsfall 2**: Sie möchten sowohl alternative Elemente als auch ergänzende Elemente miteinander kombinieren. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden und einen dynamischen Filter zu verwenden, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus zu verwenden und einen dynamischen Filter zu verwenden, der nur empfohlene Artikel enthält, die nicht mit der Kategorie des aktuellen Elements übereinstimmen. Fügen Sie schließlich beide Kriterien zu einer Sequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

1. Fügen Sie Ihrer Sequenz weitere Kriterien hinzu. Sie können einer Sequenz bis zu fünf Kriterien hinzufügen.

## Ersatzinhalt angeben

Wählen Sie aus, welche Inhalte zurückgegeben werden, wenn nicht genügend Empfehlungen zum Ausfüllen der Designvorlage verfügbar sind.

Wenn Sie eine Kriteriensequenz erstellen, werden Einstellungen für Reserveempfehlungen und partielles Design-Rendering für die einzelnen Kriterien ignoriert, aus denen die Sequenz gebildet wird. Wenn Sie Reserveempfehlungen und partielles Design-Rendering verwenden möchten, müssen Sie sie für die Sequenz aktivieren. Wählen Sie die entsprechenden Einstellungen aus. Wenn Sie Reserveempfehlungen zulassen, können Sie auch auswählen, ob für die Reserven Einschlussregeln gelten sollen.

![Einstellungen zum Sichern von Inhalten](/help/c-recommendations/c-algorithms/assets/backup-content-settings.png)

1. (Optional) Schieben Sie den Umschalter für die **[!UICONTROL teilweise]** Entwurfswiedergabe an die Position &quot;Ein&quot;.

   Es werden so viele Plätze wie möglich ausgefüllt, die Designvorlage kann jedoch Leerzeichen für die verbleibenden Plätze enthalten.

1. (Optional) Schieben Sie den **[!UICONTROL Sicherungs-Recommendations]** -Umschalter an die &quot;An&quot;-Position.

   Füllen Sie alle verbleibenden leeren Slots im Design mit einer zufälligen Auswahl der am häufigsten angezeigten Produkte aus Ihrer gesamten Site.

   Weitere Informationen finden Sie unter [Verwenden einer Reserveempfehlung](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Bedingt) Wenn Sie im vorherigen Schritt &quot; **[!UICONTROL Sicherung von Recommendations]** &quot;ausgewählt haben, können Sie &quot;Einschlussregeln auf Reserveempfehlungen **[!UICONTROL anwenden&quot;auswählen]**.

   For more information see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die Kriteriensequenz wird in der Kriterienliste angezeigt.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](../../c-recommendations/c-algorithms/algorithms.md).

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33) ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
