---
keywords: Kriteriensequenz;Mehrere Kriterien;Algorithmen;Kriterien;Empfehlungskriterien;Sequenz;Anzahl der zurückgegebenen Elemente;Steuerung auf der Ebene des Slots;Steckplatz
description: Erfahren Sie, wie Sie Sequenzen von bis zu fünf Kriterien festlegen, um die Elemente, die in Ihrer Adobe [!DNL Target] Recommendations-Aktivitäten angezeigt werden, besser zu kontrollieren.
title: Wie erstelle ich Kriteriensequenzen in Recommendations?
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 34%

---

# ![PREMIUM](/help/assets/premium.png) Kriteriensequenzen erstellen

Verwenden Sie Sequenzen von bis zu fünf Kriterien, um mehr Kontrolle über die Elemente zu erhalten, die in Ihren [!UICONTROL Recommendations]-Aktivitäten angezeigt werden. Sie können auch die Anzahl der zurückgegebenen Elemente einschränken (manchmal auch als &quot;Steuerung auf Slot-Ebene&quot;bezeichnet).

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

## Kriteriensequenz erstellen

Kriteriensequenzen werden im Bildschirm [!UICONTROL Kriteriensequenz erstellen] erstellt.

Es gibt mehrere Möglichkeiten, um auf den Bildschirm [!UICONTROL Kriteriensequenz erstellen] zu gelangen. Einige Bildschirmoptionen variieren je nachdem, wie Sie auf den Bildschirm gelangen.

* Klicken Sie im Bildschirm der Bibliothek **[!UICONTROL Empfehlungen]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Kriterien, die Sie hier erstellen, stehen automatisch für alle [!UICONTROL Recommendations]-Aktivitäten zur Verfügung.
* Wenn Sie eine [!UICONTROL Recommendations]-Aktivität erstellen, klicken Sie im Bildschirm &quot;Kriterien auswählen&quot;auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie haben die Möglichkeit, Ihre neue Kriteriensequenz zu speichern, um sie mit anderen [!UICONTROL Recommendations]-Aktivitäten zu verwenden.
* Wenn Sie eine [!UICONTROL Recommendations]-Aktivität bearbeiten, klicken Sie auf ein Feld [!UICONTROL Recommendations-Position] und wählen Sie **[!UICONTROL Change Criteria]**. Klicken Sie im Bildschirm [!UICONTROL Kriterien auswählen] auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Sie können Ihre neuen Kriterien speichern, um Sie mit anderen [!UICONTROL Recommendations]-Aktivitäten zu verwenden.

Bei den folgenden Schritten wird davon ausgegangen, dass Sie mithilfe der ersten Methode auf den Bildschirm [!UICONTROL Kriteriensequenz erstellen] zugreifen: den Bibliotheksbildschirm **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**.

   ![](assets/CreateCriteriaSequence.png)

1. Füllen Sie die Informationen im Abschnitt [Grundlegende Informationen](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Klicken Sie im Abschnitt **[!UICONTROL Kriteriensequenz]** auf **[!UICONTROL Hinzufügen Kriterien]**.

   Die Sequenzreihenfolge definiert die Reihenfolge, in der ein Entwurf gefüllt wird. Wenn Kriterium 1 nicht genügend Empfehlungen zum Ausfüllen Ihres Entwurfs enthält, werden die verbleibenden Plätze mit Kriterium 2 usw. ausgefüllt.

   ![hinzufügen](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Wählen Sie im Bildschirm [!UICONTROL Kriterien auswählen] ein Kriterium aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   Sie können das Suchfeld und die Filter-Dropdownliste verwenden, um die gewünschten Kriterien zu finden.

   ![Kriterienauswahl](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Optional) Schieben Sie den Umschalter **[!UICONTROL Die Anzahl der zurückgegebenen Elemente auf die Position &quot;on&quot;und geben Sie dann die Anzahl der Elemente an (zwischen 1 und 50).]**

   ![Anzahl der zurückgegebenen Elemente begrenzen](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Um den Wert der Option [!UICONTROL Anzahl der zurückgegebenen Elemente begrenzen (manchmal auch als &quot;Steuerung auf Slot-Ebene&quot;bezeichnet) zu verstehen, sollten Sie die folgenden Anwendungsfälle berücksichtigen:]

   * **Verwendungsfall 1**: Sie möchten eine Mischung aus verschiedenen Arten von Artikeln in einer einzigen Recommendations-Ablage haben. Sie möchten beispielsweise eine Mischung aus Oberbekleidung (Jacken) und Oberteil (Hemden, T-Shirts) zeigen. Um dies zu erreichen, verwenden Sie eine Sammlung für die Aktivität, die alle potenziellen Produkttypen enthält, die Sie in beliebigen Slots in Ihrem Design verwenden möchten. Richten Sie dann Ihre ersten Kriterien mit einem statischen Filter ein, der die Kriterien auf nur Oberbekleidung beschränkt, und richten Sie Ihr zweites Kriterium mit einem statischen Filter ein, der die Kriterien auf nur Oberteile beschränkt. Fügen Sie schließlich beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

      Die Empfehlungsablage könnte auf Ihrer Site wie folgt aussehen:

      ![Empfehlungsbereich für spezielle Produkte](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Anwendungsfall 2**: Sie möchten sowohl alternative Elemente als auch ergänzende Elemente miteinander kombinieren. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden und einen dynamischen Filter zu verwenden, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus zu verwenden und einen dynamischen Filter zu verwenden, der nur empfohlene Artikel enthält, die nicht mit der Kategorie des aktuellen Elements übereinstimmen. Fügen Sie schließlich beide Kriterien zu einer Sequenz hinzu und beschränken Sie die ersten Kriterien auf 2 Slots.

1. Fügen Sie Ihrer Sequenz weitere Kriterien hinzu. Sie können einer Sequenz bis zu fünf Kriterien hinzufügen.

1. Aktivieren Sie die Optionen [Backup-Inhalt](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Die Kriteriensequenz wird in der Kriterienliste angezeigt.

   Weitere Informationen zu den Empfehlungslogikoptionen finden Sie unter [Kriterien](/help/c-recommendations/c-algorithms/algorithms.md).

## Schulungsvideo: Kriterien in Recommendations erstellen (12:33)  ![Tutorialzeichen](/help/assets/tutorial.png)

Dieses Video enthält die folgenden Informationen:

* Erstellen von Kriterien
* Erstellen von Kriteriensequenzen
* Hochladen benutzerdefinierter Kriterien

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
