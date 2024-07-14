---
keywords: Kriteriensequenz; mehrere Kriterien; Algorithmen; Kriterien; Empfehlungskriterien; Sequenz; Anzahl der zurückgegebenen Elemente begrenzen; Steuerung auf Slot-Ebene; Slot
description: Erfahren Sie, wie Sie Sequenzen von bis zu fünf Kriterien festlegen, um eine bessere Kontrolle über die Elemente zu erhalten, die in Ihren Recommendations-Aktivitäten angezeigt werden.
title: Wie erstelle ich Kriteriensequenzen in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: c8b0e0414603761b1c67b13d74ffa96d745c99e3
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 19%

---

# Erstellen von Kriteriensequenzen

Verwenden Sie Sequenzen von bis zu fünf Kriterien, um eine bessere Kontrolle über die Elemente zu erhalten, die in Ihren [!DNL Adobe Target] [!UICONTROL Recommendations] -Aktivitäten angezeigt werden. Sie können auch die Anzahl der zurückgegebenen Elemente einschränken (manchmal auch als &quot;Steuerung auf Zeitnischen&quot;bezeichnet).

>[!NOTE]
>
>Kriteriensequenzen können nicht mit [!UICONTROL Recommendations] -Aktivitäten verwendet werden, die vor der Oktober 2016-Version von [!DNL Target Premium] erstellt wurden.

Bevor Sie eine Kriteriensequenz erstellen können, müssen Sie zuerst die Kriterien erstellen, die in der Sequenz stehen sollen. Weitere Informationen finden Sie unter [Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) .

Mithilfe einer Kriteriensequenz können Sie zusätzliche gezielte Empfehlungen bereitstellen, anstatt allgemeinere Reserveempfehlungen zu verwenden, wenn ein Kriterium nicht genügend Ergebnisse zurückgibt, um Ihr Design zu füllen. In der Regel geht eine Kriteriensequenz von einem spezifischeren Targeting, das möglicherweise weniger Ergebnisse zurückgibt, zu einem allgemeineren Targeting über, das normalerweise mehr Ergebnisse zurückgibt.

Ihre Kriteriensequenzen können je nach Seitentyp variieren, wie in den folgenden Beispielen dargestellt:

| Seitentyp | Mögliche Reihenfolge der Sequenz |
| --- | --- |
| Produktseite | <ol><li>Basierend auf dem aktuellen Artikel von derselben Marke</li><li>Basierend auf dem aktuellen Artikel, von allen Marken</li><li>Basierend auf Inhaltsähnlichkeit</li><li>Basierend auf Topverkäufen</li><li>Basierend auf Artikeln, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |
| Startseite | <ol><li>Basierend auf dem letzten Einkauf des Besuchers </li><li>Basierend auf dem Lieblingsartikel des Besuchers</li><li>Basierend auf der Lieblingskategorie des Besuchers</li><li>Basierend auf Topverkäufen</li><li>Basierend auf den Elementen, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |

## Erstellen einer Kriteriensequenz

Kriteriensequenzen werden im Bildschirm [!UICONTROL Create Criteria Sequence] erstellt.

Es gibt mehrere Möglichkeiten, den Bildschirm [!UICONTROL Create Criteria Sequence] zu erreichen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie auf dem Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!UICONTROL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!UICONTROL Recommendations] -Aktivität erstellen, klicken Sie im Bildschirm [!UICONTROL Select Criteria] auf **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. Sie können Ihre neue Kriteriensequenz speichern, um sie mit anderen [!UICONTROL Recommendations] -Aktivitäten zu verwenden.
* Wenn Sie eine [!UICONTROL Recommendations] -Aktivität bearbeiten, klicken Sie in ein [!UICONTROL Recommendations Location] -Feld auf Ihrer Seite und wählen Sie dann **[!UICONTROL Change Criteria]** aus. Klicken Sie auf dem Bildschirm [!UICONTROL Select Criteria] auf **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. Sie können Ihre neuen Kriterien speichern, um sie mit anderen [!UICONTROL Recommendations] -Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mit der ersten Methode auf den Bildschirm [!UICONTROL Create Criteria Sequence] zugreifen: auf den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Klicken Sie im Abschnitt **[!UICONTROL Criteria Sequence]** auf das Pluszeichen ( + ), um eine oder mehrere Kriteriensequenzen hinzuzufügen.

   Die Sequenzreihenfolge definiert die Reihenfolge, in der ein Entwurf gefüllt wird. Wenn Kriterien 1 nicht genügend Empfehlungen zum Ausfüllen Ihres Designs enthält, werden die verbleibenden Plätze mit Kriterien 2 usw. gefüllt.

1. Wählen Sie auf dem Bildschirm [!UICONTROL Select Criteria] ein Kriterium aus und klicken Sie dann auf **[!UICONTROL Save]**.

   Sie können das Feld [!UICONTROL Search] und die Filteroption verwenden, um die gewünschten Kriterien zu finden.

1. (Optional) Schalten Sie den Umschalter **[!UICONTROL Limit the number of items returned]** in die Position &quot;Ein&quot;und geben Sie dann die Anzahl der Elemente an (zwischen 1 und 50).

   Um den Wert der Option [!UICONTROL Limit the number of items returned] besser zu verstehen (manchmal auch als &quot;Steuerung auf Ebene des Slots&quot;bezeichnet), sollten Sie die folgenden Anwendungsfälle berücksichtigen:

   * **Nutzungsszenario 1**: Sie möchten eine Mischung verschiedener Arten von Artikeln in einer einzelnen Empfehlungsablage haben. Sie möchten beispielsweise eine Mischung aus Oberbekleidung (Jacken) und Oberteil (Hemden, T-Shirts) zeigen. Verwenden Sie dazu eine Sammlung für die Aktivität, die alle potenziellen Produktarten enthält, die Sie in beliebigen Slots in Ihrem Design wünschen. Richten Sie dann Ihre ersten Kriterien mit einem statischen Filter ein, der die Kriterien so begrenzt, dass nur Oberbekleidung einbezogen wird, und richten Sie Ihr zweites Kriterium mit einem statischen Filter ein, der die Kriterien so begrenzt, dass nur Oberteile einbezogen werden. Fügen Sie abschließend beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

     Die Empfehlungsablage könnte auf Ihrer Site wie folgt aussehen:

     ![Empfehlungsablage für präsentierte Produkte](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Nutzungsszenario 2**: Sie möchten eine Mischung aus alternativen und ergänzenden Elementen. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der nur empfohlene Artikel enthält, die nicht mit der Kategorie des aktuellen Elements übereinstimmen. Fügen Sie abschließend beide Kriterien zu einer Sequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

1. Fügen Sie Ihrer Sequenz weitere Kriterien hinzu. Sie können einer Sequenz bis zu fünf Kriterien hinzufügen.

1. Aktivieren Sie [Optionen zum Sichern von Inhalten](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klicken Sie auf **[!UICONTROL Create]**.

   Die Kriteriensequenz wird in der Liste [!UICONTROL Criteria] angezeigt.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).