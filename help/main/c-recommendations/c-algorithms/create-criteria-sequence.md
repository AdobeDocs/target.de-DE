---
keywords: Kriteriensequenz;mehrere Kriterien;Algorithmen;Kriterien;Recommendations-Kriterien;Sequenz;Anzahl der zurückgegebenen Elemente begrenzen;Steuerung auf Slot-Ebene;Slot
description: Erfahren Sie, wie Sie Sequenzen von bis zu fünf Kriterien festlegen, um eine bessere Kontrolle über die Elemente auszuüben, die in Ihren Recommendations-Aktivitäten angezeigt werden.
title: Wie erstelle ich Kriteriensequenzen in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
TQID: https://experienceleague.adobe.com/dxO5cKxesTxgzZyfcvydQUlSq4TAgFN0ztT5VIe1WKU
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 833
ht-degree: 21%

---

# Erstellen von Kriteriensequenzen

Verwenden Sie Sequenzen von bis zu fünf Kriterien, um eine bessere Kontrolle über die Elemente auszuüben, die in Ihren [!DNL Adobe Target]Recommendations[!UICONTROL Aktivitäten ]. Sie können auch die Anzahl der zurückgegebenen Elemente begrenzen (manchmal auch als „Steuerung der Steckplatzebene“ bezeichnet).

>[!NOTE]
>
>Kriteriensequenzen können nicht mit Aktivitäten [!UICONTROL Recommendations) verwendet werden, ] vor der [!DNL Target Premium] vom Oktober 2016 erstellt wurden.

Bevor Sie eine Kriteriensequenz erstellen können, müssen Sie zuerst die Kriterien erstellen, die in der Sequenz stehen sollen. Weitere Informationen [ Sie unter ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) erstellen .

Mithilfe einer Kriteriensequenz können Sie zusätzliche gezielte Empfehlungen bereitstellen, anstatt allgemeinere Reserveempfehlungen zu verwenden, wenn ein Kriterium nicht genügend Ergebnisse zurückgibt, um Ihr Design zu füllen. In der Regel geht eine Kriteriensequenz von einer spezifischeren Zielgruppenbestimmung, die möglicherweise weniger Ergebnisse zurückgibt, zu einer allgemeineren Zielgruppenbestimmung über, die in der Regel mehr Ergebnisse zurückgibt.

Ihre Kriteriensequenzen können je nach Seitentyp variieren, wie in den folgenden Beispielen gezeigt:

| Seitentyp | Mögliche Reihenfolge |
| --- | --- |
| Produktseite | <ol><li>Basierend auf aktuellem Artikel, von derselben Marke</li><li>Basierend auf dem aktuellen Artikel, von allen Marken</li><li>Basierend auf Inhaltsähnlichkeit</li><li>Basierend auf Topverkäufen</li><li>Basierend auf Artikeln, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |
| Startseite | <ol><li>Basierend auf dem letzten Einkauf des Besuchers </li><li>Basierend auf dem Lieblingsartikel des Besuchers</li><li>Basierend auf der Lieblingskategorie des Besuchers</li><li>Basierend auf Topverkäufen</li><li>Basierend auf den Elementen, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |

## Erstellen einer Kriteriensequenz

Kriteriensequenzen werden auf dem Bildschirm [!UICONTROL Kriteriensequenz erstellen] erstellt.

Es gibt mehrere Möglichkeiten, um auf den Bildschirm [!UICONTROL Kriteriensequenz erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm der Bibliothek **[!UICONTROL Empfehlungen]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!UICONTROL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!UICONTROL Recommendations]-Aktivität erstellen, klicken Sie auf dem Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie haben die Möglichkeit, Ihre neue Kriteriensequenz zur Verwendung mit anderen [!UICONTROL -Aktivitäten ] speichern.
* Wenn Sie eine Aktivität vom Typ [!UICONTROL Recommendations] bearbeiten, klicken Sie auf ] Seite in ein Feld [!UICONTROL Recommendations-Speicherort und wählen Sie dann **[!UICONTROL Kriterien ändern]** aus. Klicken Sie im Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie haben die Möglichkeit, Ihre neuen Kriterien für die Verwendung mit anderen [!UICONTROL Recommendations]-Aktivitäten zu speichern.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf [!UICONTROL  Bildschirm ]Kriteriensequenz erstellen **[!UICONTROL zugreifen: dem Bildschirm Recommendations]** > **[!UICONTROL Kriterien]** Bibliothek .

1. Klicken Sie **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**.

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Klicken Sie **[!UICONTROL Abschnitt]** auf das Pluszeichen ( + ), um eine oder mehrere Kriteriensequenzen hinzuzufügen.

   Die Sequenzreihenfolge definiert die Reihenfolge, in der ein Design ausgefüllt wird. Wenn Kriterium 1 nicht genügend Empfehlungen zum Ausfüllen Ihres Designs enthält, werden die verbleibenden Slots mit Kriterium 2 usw. ausgefüllt.

1. Wählen Sie [!UICONTROL  Bildschirm &quot;] auswählen“ ein Kriterium aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

   Sie können das Feld [!UICONTROL Suche] und die Filteroption verwenden, um die gewünschten Kriterien zu finden.

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Begrenzung der Anzahl der zurückgegebenen Elemente]** auf die „Ein“-Position und geben Sie dann die Anzahl der Elemente (zwischen 1 und 50) an.

   Beachten Sie die folgenden Anwendungsfälle, um den Wert der Option [!UICONTROL Begrenzung der Anzahl der zurückgegebenen Elemente] (manchmal auch als „Steuerung auf Steckplatzebene“ bezeichnet) zu verstehen:

   * **Anwendungsfall 1**: Sie möchten eine Mischung aus verschiedenen Arten von Elementen in einer einzigen Recommendations-Taskleiste haben. Beispiel: Sie möchten eine Mischung aus Oberbekleidung (Jacken) und Oberteilen (Hemden, T-Shirts) anzeigen. Verwenden Sie dazu eine Sammlung für die Aktivität , die alle potenziellen Produkttypen in allen Slots in Ihrem Design enthält. Richten Sie dann Ihre ersten Kriterien mit einem statischen Filter ein, der die Kriterien auf Oberbekleidung einschränkt, und richten Sie Ihre zweiten Kriterien mit einem statischen Filter ein, der die Kriterien auf Oberbekleidung einschränkt. Fügen Sie schließlich beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf zwei Slots.

     Die Recommendations -Taskleiste könnte auf Ihrer Site wie folgt aussehen:

     ![Empfohlene Produkt-Taskleiste](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Anwendungsfall 2**: Sie möchten eine Mischung aus alternativen und komplementären Elementen. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der nur empfohlene Artikel enthält, die nicht mit der Kategorie des aktuellen Artikels übereinstimmen. Fügen Sie schließlich beide Kriterien zu einer Sequenz hinzu und beschränken Sie das erste Kriterium auf zwei Slots.

1. Fügen Sie Ihrer Sequenz weitere Kriterien hinzu. Sie können einer Sequenz bis zu fünf Kriterien hinzufügen.

1. Aktivieren Sie [Optionen für Sicherungsinhalte](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klicken Sie **[!UICONTROL Erstellen]**.

   Die Kriteriensequenz wird in der Liste [!UICONTROL Kriterien] angezeigt.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).
