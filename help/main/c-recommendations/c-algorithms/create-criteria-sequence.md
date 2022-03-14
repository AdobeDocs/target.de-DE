---
keywords: Kriteriensequenz; mehrere Kriterien; Algorithmen; Kriterien; Empfehlungskriterien; Sequenz; Anzahl der zurückgegebenen Elemente begrenzen; Steuerung auf Slot-Ebene; Slot
description: Erfahren Sie, wie Sie Sequenzen von bis zu fünf Kriterien festlegen, um eine bessere Kontrolle über die Elemente zu erhalten, die in Ihrer Adobe angezeigt werden. [!DNL Target] Recommendations-Aktivitäten.
title: Wie erstelle ich Kriteriensequenzen in Recommendations?
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 34%

---

# ![PREMIUM](/help/main/assets/premium.png) Kriteriensequenzen erstellen

Verwenden Sie Sequenzen von bis zu fünf Kriterien, um mehr Kontrolle über die Elemente zu erhalten, die in Ihren [!UICONTROL Recommendations]-Aktivitäten angezeigt werden. Sie können auch die Anzahl der zurückgegebenen Elemente einschränken (manchmal auch als &quot;Steuerung auf Ebene der Zeitnischen&quot;bezeichnet).

>[!NOTE]
>
>Kriteriensequenzen können nicht mit [!UICONTROL Empfehlungs]-Aktivitäten verwendet werden, die vor der Version Oktober 2016 von [!DNL Target Premium] erstellt wurden.

Bevor Sie eine Kriteriensequenz erstellen können, müssen Sie zuerst die Kriterien erstellen, die in der Sequenz stehen sollen. Siehe [Erstellen von Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) für weitere Informationen.

Mithilfe einer Kriteriensequenz können Sie zusätzliche gezielte Empfehlungen bereitstellen, anstatt allgemeinere Reserveempfehlungen zu verwenden, wenn ein Kriterium nicht genügend Ergebnisse zurückgibt, um Ihr Design zu füllen. In der Regel wird eine Kriteriensequenz von einem spezifischeren Targeting, das möglicherweise weniger Ergebnisse zurückgibt, zu einem allgemeineren Targeting, das normalerweise mehr Ergebnisse zurückgibt.

Ihre Kriteriensequenzen können je nach Seitentyp variieren, wie in den folgenden Beispielen dargestellt:

| Seitentyp | Mögliche Sequenzreihenfolge |
| --- | --- |
| Produktseite | <ol><li>Basierend auf dem aktuellen Artikel, von der gleichen Marke</li><li>Basierend auf dem aktuellen Artikel, von allen Marken</li><li>Basierend auf Inhaltsähnlichkeit</li><li>Basierend auf Topverkäufen</li><li>Basierend auf Artikeln, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |
| Startseite | <ol><li>Basierend auf dem letzten Einkauf des Besuchers </li><li>Basierend auf dem Lieblingsartikel des Besuchers</li><li>Basierend auf der Lieblingskategorie des Besuchers</li><li>Basierend auf Topverkäufen</li><li>Basierend auf den Elementen, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |

## Erstellen einer Kriteriensequenz

Sie erstellen Kriteriensequenzen aus dem [!UICONTROL Kriteriensequenz erstellen] angezeigt.

Es gibt mehrere Möglichkeiten, um auf den Bildschirm [!UICONTROL Kriteriensequenz erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm der Bibliothek **[!UICONTROL Empfehlungen]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!UICONTROL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!UICONTROL Recommendations] -Aktivität, klicken Sie im Bildschirm &quot;Kriterien auswählen&quot;auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie haben die Möglichkeit, Ihre neue Kriteriensequenz zu speichern, um sie mit anderen [!UICONTROL Recommendations]-Aktivitäten zu verwenden.
* Wenn Sie eine [!UICONTROL Recommendations] Aktivität, klicken Sie in eine [!UICONTROL Recommendations-Standort] auf Ihrer Seite ein und wählen Sie **[!UICONTROL Kriterien ändern]**. Klicken Sie im Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!UICONTROL Recommendations]-Aktivitäten zu verwenden.

Die folgenden Schritte setzen voraus, dass Sie auf die [!UICONTROL Kriteriensequenz erstellen] mit der ersten Methode: die **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]** Bibliotheksbildschirm.

1. Klicken **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken **[!UICONTROL Erstellen von Kriterien]** > **[!UICONTROL Kriteriensequenz erstellen]**.

   ![](assets/CreateCriteriaSequence.png)

1. Füllen Sie die Informationen im [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) Abschnitt.

1. Im **[!UICONTROL Kriteriensequenz]** Abschnitt, klicken Sie auf **[!UICONTROL Kriterien hinzufügen]**.

   Die Sequenzreihenfolge definiert die Reihenfolge, in der ein Entwurf gefüllt wird. Wenn Kriterien 1 nicht genügend Empfehlungen zum Ausfüllen Ihres Designs enthält, werden die verbleibenden Plätze mit Kriterien 2 usw. gefüllt.

   ![Kriterien hinzufügen](/help/main/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Im [!UICONTROL Kriterien auswählen] , wählen Sie ein Kriterium aus und klicken Sie auf **[!UICONTROL Hinzufügen]**.

   Sie können das Suchfeld und die Filter-Dropdowns verwenden, um die gewünschten Kriterien zu finden.

   ![Kriterienauswahl](/help/main/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Optional) Schieben Sie die **[!UICONTROL Anzahl der zurückgegebenen Elemente begrenzen]** schalten Sie auf die Position &quot;Ein&quot;um und geben Sie dann die Anzahl der Elemente an (zwischen 1 und 50).

   ![Anzahl der zurückgegebenen Elemente begrenzen](/help/main/c-recommendations/c-algorithms/assets/limit-number.png)

   So verstehen Sie den Wert der Variablen [!UICONTROL Anzahl der zurückgegebenen Elemente begrenzen] -Option (manchmal auch als &quot;Steuerung auf Ebene der Zeitnischen&quot;bezeichnet) berücksichtigen Sie die folgenden Anwendungsfälle:

   * **Anwendungsfall 1**: Sie möchten eine Mischung aus verschiedenen Arten von Artikeln in einer einzelnen Empfehlungsablage haben. Sie möchten beispielsweise eine Mischung aus Oberbekleidung (Jacken) und Oberteil (Hemden, T-Shirts) zeigen. Verwenden Sie dazu eine Sammlung für die Aktivität, die alle potenziellen Produktarten enthält, die Sie in beliebigen Slots in Ihrem Design wünschen. Richten Sie dann Ihre ersten Kriterien mit einem statischen Filter ein, der die Kriterien so begrenzt, dass nur Oberbekleidung einbezogen wird, und richten Sie Ihr zweites Kriterium mit einem statischen Filter ein, der die Kriterien so begrenzt, dass nur Oberteile einbezogen werden. Fügen Sie abschließend beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

      Die Empfehlungsablage könnte auf Ihrer Site wie folgt aussehen:

      ![Empfehlungsablage für vorgestellte Produkte](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Anwendungsfall 2**: Sie möchten eine Mischung aus alternativen und ergänzenden Artikeln. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus zu verwenden, und verwenden Sie einen dynamischen Filter, der nur empfohlene Artikel enthält, die nicht mit der Kategorie des aktuellen Elements übereinstimmen. Fügen Sie abschließend beide Kriterien zu einer Sequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

1. Fügen Sie Ihrer Sequenz weitere Kriterien hinzu. Sie können einer Sequenz bis zu fünf Kriterien hinzufügen.

1. Aktivieren [Optionen für Backup-Inhalt](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die Kriteriensequenz wird in der Kriterienliste angezeigt.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
