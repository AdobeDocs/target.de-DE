---
keywords: Kriteriensequenz;mehrere Kriterien;Algorithmen;Kriterien;Recommendations-Kriterien;Sequenz;Anzahl der zurückgegebenen Elemente begrenzen;Steuerung auf Slot-Ebene;Slot
description: Erfahren Sie, wie Sie Sequenzen von bis zu fünf Kriterien festlegen, um eine bessere Kontrolle über die Elemente auszuüben, die in Ihren Recommendations-Aktivitäten angezeigt werden.
title: Wie erstelle ich Kriteriensequenzen in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
TQID: 'https://experienceleague.adobe.com/dxO5cKxesTxgzZyfcvydQUlSq4TAgFN0ztT5VIe1WKU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 9%
---
# Erstellen von Kriteriensequenzen {#create-criteria-sequence}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Kriteriensequenzen erstellen, um die Elemente zu steuern, die in [!DNL Adobe Target Recommendations] Aktivitäten angezeigt werden.

>[!ENDSHADEBOX]

Sequenzen von bis zu fünf Kriterien ermöglichen eine bessere Kontrolle über die Elemente, die in [!DNL Adobe Target] **[!UICONTROL Recommendations]**-Aktivitäten erscheinen. Die Anzahl der zurückgegebenen Elemente kann ebenfalls begrenzt sein (manchmal auch als „Steuerung der Slotebene“ bezeichnet).

Wenn ein Kriterium nicht genügend Ergebnisse zurückgibt, um den Entwurf auszufüllen, liefert eine Kriteriensequenz zusätzliche zielgerichtete Empfehlungen anstelle allgemeinerer Backup-Empfehlungen. In der Regel geht eine Kriteriensequenz von einer spezifischeren Zielgruppenbestimmung, die möglicherweise weniger Ergebnisse zurückgibt, zu einer allgemeineren Zielgruppenbestimmung über, die in der Regel mehr Ergebnisse zurückgibt.

>[!NOTE]
>
>Kriteriensequenzen können nicht mit Aktivitäten **[!UICONTROL Recommendations) verwendet werden,]** vor der [!DNL Target Premium] vom Oktober 2016 erstellt wurden.

Um eine Kriteriensequenz zu erstellen, erstellen Sie zunächst die Kriterien, die in die Sequenz aufgenommen werden sollen. Weitere Informationen [ Sie unter ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) erstellen .

Die Reihenfolge einer Kriteriensequenz kann je nach Seitentyp variieren, wie in den folgenden Beispielen gezeigt:

| Seitentyp | Mögliche Reihenfolge |
| --- | --- |
| Produktseite | <ol><li>Basierend auf aktuellem Artikel, von derselben Marke</li><li>Basierend auf dem aktuellen Artikel, von allen Marken</li><li>Basierend auf Inhaltsähnlichkeit</li><li>Basierend auf Topverkäufen</li><li>Basierend auf Artikeln, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |
| Startseite | <ol><li>Basierend auf dem letzten Einkauf des Besuchers </li><li>Basierend auf dem Lieblingsartikel des Besuchers</li><li>Basierend auf der Lieblingskategorie des Besuchers</li><li>Basierend auf Topverkäufen</li><li>Basierend auf den Elementen, die auf der gesamten Website am häufigsten angezeigt wurden</li></ol> |

## Erstellen einer Kriteriensequenz

Kriteriensequenzen werden auf dem Bildschirm **[!UICONTROL Kriteriensequenz erstellen]** erstellt. Es gibt mehrere Möglichkeiten, um diesen Bildschirm zu erreichen. Einige Bildschirmoptionen variieren je nachdem, wie der Bildschirm erreicht wird.

* Klicken Sie im Bildschirm der Bibliothek **[!UICONTROL Empfehlungen]** > **[!UICONTROL Kriterien]** auf **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Hier erstellte Kriterien werden automatisch für alle **[!UICONTROL Recommendations]**-Aktivitäten verfügbar gemacht.
* Klicken Sie beim Erstellen **[!UICONTROL Aktivität]** Recommendations“ auf dem Bildschirm **[!UICONTROL Kriterien auswählen]** auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Die neue Kriteriensequenz kann zur Verwendung mit anderen **[!UICONTROL Recommendations“-]** gespeichert werden.
* Klicken Sie beim Bearbeiten einer **[!UICONTROL Recommendations]**-Aktivität in ein Feld **[!UICONTROL Recommendations-Speicherort]** auf der Seite und wählen Sie **[!UICONTROL Kriterien ändern]** aus. Klicken Sie im Bildschirm **[!UICONTROL Kriterien auswählen]** auf **[!UICONTROL Neu erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**. Die neuen Kriterien können zur Verwendung mit anderen **[!UICONTROL Recommendations“-]** gespeichert werden.

Bei den folgenden Schritten wird davon ausgegangen **[!UICONTROL dass der Bildschirm]** Kriteriensequenz erstellen“ über das Menü **[!UICONTROL Kriterien]** aufgerufen wird.

1. Klicken Sie **[!UICONTROL Recommendations]** > **[!UICONTROL Kriterien]**.

1. Klicken Sie **[!UICONTROL Kriterien erstellen]** > **[!UICONTROL Kriteriensequenz erstellen]**.

   ![Kriterienseite mit der im Menü Kriterien erstellen ausgewählten Option Kriteriensequenz erstellen](../assets/criteria_create_6.png)

1. Füllen Sie die Informationen im Abschnitt [Basisinformationen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) aus.

1. Klicken Sie **[!UICONTROL Abschnitt]** auf das Pluszeichen ( + ), um eine oder mehrere Kriteriensequenzen hinzuzufügen.

   Die Sequenzreihenfolge definiert die Reihenfolge, in der ein Design ausgefüllt wird. Wenn Kriterium 1 nicht genügend Empfehlungen zum Ausfüllen des Designs enthält, werden die verbleibenden Slots mit Kriterium 2 usw. ausgefüllt.

   ![Abschnitt Kriteriensequenz des Dialogfelds „Kriteriensequenz erstellen“ mit fünf ausgewählten Kriterienfeldern und dem Pluszeichen von Kriterium 1](../assets/criteria_create_7.png)

1. Wählen Sie **[!UICONTROL Bildschirm &quot;]** auswählen“ ein Kriterium aus und klicken Sie dann auf **[!UICONTROL Speichern]**.

   Das **[!UICONTROL Suchen]** und die Filteroption können verwendet werden, um die gewünschten Kriterien zu finden.

1. (Optional) Aktivieren Sie **[!UICONTROL Begrenzung der Anzahl der zurückgegebenen Elemente]** und geben Sie dann die Anzahl der Elemente (zwischen 1 und 50) an.

   ![Abschnitt „Kriteriensequenz“ mit der Option Für Sie als Kriterium 1 empfohlenen und „Anzahl der zurückgegebenen Elemente begrenzen“ aktiviert](../assets/criteria_create_8.png)

   Die folgenden Anwendungsfälle veranschaulichen den Wert der Option **[!UICONTROL Begrenzung der Anzahl der zurückgegebenen Elemente]** (manchmal auch als „Steuerung der Steckplatzebene“ bezeichnet).

   +++ Anwendungsfälle für die Begrenzung der Anzahl der zurückgegebenen Elemente

   * **Anwendungsfall 1**: Eine Mischung aus verschiedenen Arten von Artikeln in einer einzigen Empfehlungsschale, z. B. eine Mischung aus Oberbekleidung (Jacken) und Oberteilen (Hemden, T-Shirts). Verwenden Sie dazu eine Sammlung für die Aktivität , die alle Produkttypen enthält, die in jedem Steckplatz des Designs angezeigt werden können. Anschließend richten Sie die ersten Kriterien mit einem statischen Filter ein, der nur Oberbekleidung umfasst, und die zweiten Kriterien mit einem statischen Filter, der nur Oberteile umfasst. Fügen Sie schließlich beide Kriterien zu einer Kriteriensequenz hinzu und beschränken Sie die ersten Kriterien auf zwei Slots.

     Die Recommendations -Taskleiste könnte auf einer Site wie folgt aussehen:

     ![Empfohlene Produkt-Taskleiste](assets/featured-products.png)

   * **Anwendungsfall 2**: Eine Mischung aus alternativen Elementen und komplementären Elementen. Richten Sie ein Kriterium ein, um einen angezeigten/angezeigten Algorithmus zu verwenden, und einen dynamischen Filter, der die empfohlenen Elemente auf die Kategorie des aktuellen Elements beschränkt. Richten Sie das zweite Kriterium ein, um einen angezeigten/gekauften Algorithmus und einen dynamischen Filter zu verwenden, der nur empfohlene Artikel enthält, die nicht der Kategorie des aktuellen Artikels entsprechen. Fügen Sie schließlich beide Kriterien zu einer Sequenz hinzu und beschränken Sie das erste Kriterium auf zwei Slots.

   +++

1. Fügen Sie der Sequenz weitere Kriterien hinzu. Einer Sequenz können bis zu fünf Kriterien hinzugefügt werden.

1. Aktivieren Sie [Optionen für Sicherungsinhalte](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Klicken Sie **[!UICONTROL Erstellen]**.

Die Kriteriensequenz wird in der Liste **[!UICONTROL Kriterien]** angezeigt.

Weitere Informationen zu den Optionen für die Empfehlungslogik finden Sie unter [Erste Schritte mit Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).
