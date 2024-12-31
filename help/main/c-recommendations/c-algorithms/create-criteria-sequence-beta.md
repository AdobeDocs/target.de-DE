---
keywords: Kriteriensequenz;mehrere Kriterien;Algorithmen;Kriterien;Recommendations-Kriterien;Sequenz;Anzahl der zurückgegebenen Elemente begrenzen;Steuerung auf Slot-Ebene;Slot
description: Erfahren Sie, wie Sie Sequenzen von bis zu fünf Kriterien festlegen, um eine bessere Kontrolle über die Elemente auszuüben, die in Ihren Recommendations-Aktivitäten angezeigt werden.
title: Wie erstelle ich Kriteriensequenzen in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 9c521c61-7141-4fbc-81b7-a5b62dea10b6
source-git-commit: 22b0ba18efb736b291f9b7951acd9f706beedbe1
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 19%

---

# Erstellen von Kriteriensequenzen

Verwenden Sie Sequenzen von bis zu fünf Kriterien, um eine bessere Kontrolle über die Elemente auszuüben, die in Ihren [!DNL Adobe Target]-[!UICONTROL Recommendations]-Aktivitäten angezeigt werden. Sie können auch die Anzahl der zurückgegebenen Elemente begrenzen (manchmal auch als „Steuerung der Steckplatzebene“ bezeichnet).

>[!NOTE]
>
>Kriteriensequenzen können nicht mit [!UICONTROL Recommendations] Aktivitäten verwendet werden, die vor der Version vom Oktober 2016 von [!DNL Target Premium] erstellt wurden.

Bevor Sie eine Kriteriensequenz erstellen können, müssen Sie zuerst die Kriterien erstellen, die in der Sequenz stehen sollen. Weitere Informationen [ Sie unter ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) erstellen .

Mithilfe einer Kriteriensequenz können Sie zusätzliche gezielte Empfehlungen bereitstellen, anstatt allgemeinere Reserveempfehlungen zu verwenden, wenn ein Kriterium nicht genügend Ergebnisse zurückgibt, um Ihr Design zu füllen. In der Regel geht eine Kriteriensequenz von einer spezifischeren Zielgruppenbestimmung, die möglicherweise weniger Ergebnisse zurückgibt, zu einer allgemeineren Zielgruppenbestimmung über, die in der Regel mehr Ergebnisse zurückgibt.

Ihre Kriteriensequenzen können je nach Seitentyp variieren, wie in den folgenden Beispielen gezeigt:

| Seitentyp | Mögliche Reihenfolge |
| --- | --- |
| Produktseite | <ol><li>Basierend auf aktuellem Artikel, von derselben Marke</li><li>Basierend auf dem aktuellen Artikel, von allen Marken</li><li>Basierend auf Inhaltsähnlichkeit</li><li>Basierend auf Topverkäufen</li><li>Basierend auf Artikeln, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |
| Startseite | <ol><li>Basierend auf dem letzten Einkauf des Besuchers </li><li>Basierend auf dem Lieblingsartikel des Besuchers</li><li>Basierend auf der Lieblingskategorie des Besuchers</li><li>Basierend auf Topverkäufen</li><li>Basierend auf den Elementen, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |

## Erstellen einer Kriteriensequenz

Kriteriensequenzen werden auf dem [!UICONTROL Create Criteria Sequence] erstellt.

Es gibt mehrere Möglichkeiten, den [!UICONTROL Create Criteria Sequence] zu erreichen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliothek auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!UICONTROL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!UICONTROL Recommendations] Aktivität erstellen, klicken Sie auf dem [!UICONTROL Select Criteria] Bildschirm auf **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. Sie haben die Möglichkeit, Ihre neue Kriteriensequenz zur Verwendung mit anderen [!UICONTROL Recommendations] Aktivitäten zu speichern.
* Wenn Sie eine [!UICONTROL Recommendations] bearbeiten, klicken Sie in ein [!UICONTROL Recommendations Location] auf Ihrer Seite und wählen Sie dann **[!UICONTROL Change Criteria]** aus. Klicken Sie auf dem [!UICONTROL Select Criteria] Bildschirm auf **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. Sie haben die Möglichkeit, Ihre neuen Kriterien für die Verwendung mit anderen [!UICONTROL Recommendations] Aktivitäten zu speichern.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie auf den [!UICONTROL Create Criteria Sequence] über die erste Methode zugreifen: den Bildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliothek .

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Klicken Sie im Abschnitt **[!UICONTROL Criteria Sequence]** auf das Pluszeichen ( + ), um eine oder mehrere Kriteriensequenzen hinzuzufügen.

   Die Sequenzreihenfolge definiert die Reihenfolge, in der ein Design ausgefüllt wird. Wenn Kriterium 1 nicht genügend Empfehlungen zum Ausfüllen Ihres Designs enthält, werden die verbleibenden Slots mit Kriterium 2 usw. ausgefüllt.

1. Wählen Sie auf dem Bildschirm [!UICONTROL Select Criteria] ein Kriterium aus und klicken Sie dann auf **[!UICONTROL Save]**.

   Sie können das [!UICONTROL Search] und die Filteroption verwenden, um die gewünschten Kriterien zu finden.

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Limit the number of items returned]** auf die Position „Ein“ und geben Sie dann die Anzahl der Elemente (zwischen 1 und 50) an.

   Beachten Sie die folgenden Anwendungsfälle, um den Wert der [!UICONTROL Limit the number of items returned]-Option (manchmal auch als „Steuerung auf Steckplatzebene“ bezeichnet) zu verstehen:

   * **Anwendungsfall 1**: Sie möchten eine Mischung aus verschiedenen Arten von Elementen in einer einzigen Recommendations-Taskleiste haben. Beispiel: Sie möchten eine Mischung aus Oberbekleidung (Jacken) und Oberteilen (Hemden, T-Shirts) anzeigen. Verwenden Sie dazu eine Sammlung für die Aktivität , die alle potenziellen Produkttypen in allen Slots in Ihrem Design enthält. Richten Sie dann Ihre ersten Kriterien mit einem statischen Filter ein, der die Kriterien auf Oberbekleidung einschränkt, und richten Sie Ihre zweiten Kriterien mit einem statischen Filter ein, der die Kriterien auf Oberbekleidung einschränkt. Fügen Sie schließlich beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf zwei Slots.

     Die Recommendations -Taskleiste könnte auf Ihrer Site wie folgt aussehen:

     ![Empfohlene Produkt-Taskleiste](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Anwendungsfall 2**: Sie möchten eine Mischung aus alternativen und komplementären Elementen. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der nur empfohlene Artikel enthält, die nicht mit der Kategorie des aktuellen Artikels übereinstimmen. Fügen Sie schließlich beide Kriterien zu einer Sequenz hinzu und beschränken Sie das erste Kriterium auf zwei Slots.

1. Fügen Sie Ihrer Sequenz weitere Kriterien hinzu. Sie können einer Sequenz bis zu fünf Kriterien hinzufügen.

1. Aktivieren Sie [Optionen für Sicherungsinhalte](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klicken Sie auf **[!UICONTROL Create]**.

   Die Kriteriensequenz wird in der [!UICONTROL Criteria] angezeigt.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).
