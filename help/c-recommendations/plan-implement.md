---
keywords: Recommendations; Einstellungen; Voreinstellungen; vertikaler Markt; Filtern inkompatibler Kriterien; Standard-Hostgruppe; Thumb-Base-URL; Recommendations-API-Token
description: 'Erfahren Sie, wie Sie Recommendations-Aktivitäten in Adobe Target implementieren. '
title: Wie implementiere ich Recommendations-Aktivitäten?
feature: Recommendations
exl-id: b6edb504-a8b6-4379-99c1-6907e71601f9
source-git-commit: 6d601c0099e9e8451571af7b75641620a94578fc
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 31%

---

# ![PREMIUM](/help/assets/premium.png) Planung und Umsetzung [!DNL Recommendations]

Vor der Einrichtung Ihrer ersten [!DNL Recommendations] Aktivität in [!DNL Adobe Target]führen Sie die folgenden Schritte aus:

1. [Implementierung [!DNL Target]](#implement-target) auf der Web- und mobilen App-Oberfläche, die Sie zur Erfassung des Benutzerverhaltens und zur Bereitstellung von Empfehlungen verwenden möchten.
1. [Richten Sie Ihre [!DNL Recommendations] Katalog](#rec-catalog) von Produkten oder Inhalten, die Sie Ihren Benutzern empfehlen möchten.
1. [Übergeben von Verhaltensinformationen und -kontext](#pass-behavioral) nach [!DNL Target Recommendations] , damit sie personalisierte Empfehlungen bereitstellen kann.
1. [Konfigurieren globaler Ausnahmen](#exclusions).
1. [Konfigurieren [!DNL Recommendations] settings](#concept_C1E1E2351413468692D6C21145EF0B84).

## Implementierung [!DNL Target] {#implement-target}

[!DNL Target Recommendations] erfordert, dass Sie die [!DNL Adobe Experience Platform Web SDK] oder at.js 0.9.2 (oder höher). Siehe [Implementierung [!DNL Target]](/help/c-implementing-target/implementing-target.md) für weitere Informationen.

## Recommendations-Katalog einrichten {#rec-catalog}

Bereitstellung hochwertiger Empfehlungen, [!DNL Target] muss über die Produkte oder Inhalte informiert sein, die Sie empfehlen möchten. Ihr Katalog sollte normalerweise drei Arten von Informationen zu den Artikeln enthalten, die Sie empfehlen möchten. Nehmen wir an, Sie empfehlen Filme. Fügen Sie Folgendes hinzu:

1. Daten, die dem Benutzer angezeigt werden sollen, der die Empfehlung erhält. Beispielsweise können Sie den Namen des Films und eine URL für ein Miniaturbild des Filmposters anzeigen.
1. Daten, die zur Anwendung von Marketing- und Merchandising-Steuerelementen nützlich sind. Beispielsweise können Sie die Filmanzeige so anzeigen, dass Sie keine Filme vom Typ NC-17 empfehlen.
1. Daten, die für die Bestimmung der Ähnlichkeit von Elementen mit anderen Elementen nützlich sind. Sie können beispielsweise das Genre des Films und den Regisseur des Films anzeigen.

[!DNL Target] bietet mehrere Integrationsoptionen zum Ausfüllen Ihres Katalogs. Diese Optionen können zusammen verwendet werden, um verschiedene Elemente im Katalog zu aktualisieren oder um verschiedene Elementattribute auf unterschiedlichen Frequenzen zu aktualisieren.

| Methode | Was es ist | Einsatz | Zusätzliche Informationen |
| --- | --- | --- | --- |
| Katalog-Feed | einen Feed planen (CSV, Google Product XML oder [!DNL Analytics Product Classifications]), die täglich hochgeladen und aufgenommen werden. | Zum Senden von Informationen über mehrere Elemente gleichzeitig. Zum Senden von Informationen, die sich selten ändern. | Siehe [Feeds](/help/c-recommendations/c-products/feeds.md). |
| Entitäts-API | Rufen Sie eine API auf, um Aktualisierungen für ein einzelnes Element in Minutenschnelle zu senden. | Zum Versand von Updates, wenn sie jeweils etwa einen Artikel betreffen. Zum Senden von Informationen, die sich häufig ändern (z. B. Preis, Bestand/Lagerbestand). | Siehe [Entwicklerdokumentation für Entitäts-API](https://developers.adobetarget.com/api/recommendations/#tag/Entities). |
| Übergeben von Aktualisierungen auf der Seite | Senden Sie Aktualisierungen für ein einzelnes Element per JavaScript auf der Seite oder mithilfe der Bereitstellungs-API. | Zum Versand von Updates, wenn sie jeweils etwa einen Artikel betreffen. Zum Senden von Informationen, die sich häufig ändern (z. B. Preis, Bestand/Lagerbestand). | Siehe [Artikelansichten/Produktseiten](#items-product-pages) unten. |

Die meisten Kunden sollten mindestens einen Feed implementieren. Anschließend können Sie Ihren Feed mit Aktualisierungen für häufig geänderte Attribute oder Elemente ergänzen, indem Sie entweder die Entitäten-API oder die Seitenmethode verwenden.

## Übergeben von Verhaltensinformationen und -kontext {#pass-behavioral}

Die Verhaltensinformationen und -kontexte, an die Sie übergeben sollten [!DNL Target] hängt von der Aktion ab, die Ihr Besucher durchführt und die häufig mit dem Seitentyp verknüpft ist, mit dem Ihr Besucher interagiert.

### Artikelansichten/Produktseiten {#items-product-pages}

Auf Seiten, auf denen ein Besucher ein einzelnes Element anzeigt, z. B. eine Produktdetailseite, sollten Sie die Identität des vom Besucher angesehenen Elements weitergeben. Sie sollten auch die detaillierteste Kategorie des Elements übergeben, das der Besucher anzeigt, um Filterempfehlungen für die aktuelle Kategorie zu ermöglichen.

Sie können auch bestimmte schnell wechselnde Attribute auf der Produktseite selbst übergeben. Sie können beispielsweise den Preis (`value`) und Lagerbestand.

```
<script type="text/javascript">
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "running-shoes", 
         "value": 119.99, 
         "inventory": 329 
      } 
   } 
}
</script>
```

### Kategorieansichten/Kategorieseiten

Wahrscheinlich möchten Sie Ihre Empfehlungen auf einer Kategorieseite auf Produkte oder Inhalte innerhalb dieser Kategorie beschränken. Stellen Sie dazu sicher, dass Sie die Identität der aktuell angezeigten Kategorie übergeben.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "running-shoes" 
      } 
   } 
}
```

### Zusatz zum Warenkorb/Ansichten/Checkout-Seiten {#cart}

Auf einer Warenkorbseite können Sie Artikel basierend auf dem Inhalt des aktuellen Warenkorbs des Besuchers empfehlen. Übergeben Sie dazu die IDs aller Elemente im aktuellen Warenkorb des Besuchers mithilfe des speziellen Parameters `cartIds`.

```
function targetPageParams() {
   return {
      "cartIds": ["352", "223", "23432", "432", "553"]
      }
}
```

Die auf dem Warenkorb basierende Empfehlungslogik ähnelt der[!UICONTROL Empfohlen für Sie]&quot;benutzerbasierter Algorithmus und zum &quot;[!UICONTROL Personen, die diese ansahen, kauften diese]&quot; und &quot;[!UICONTROL Personen, die diese kauften, kauften diese]&quot;artikelbasierte Algorithmen.

[!DNL Target] verwendet kollaborative Filtermethoden, um Ähnlichkeiten für jedes Element im Warenkorb des Besuchers zu ermitteln, und kombiniert dann diese Ähnlichkeiten im Verhalten für jedes Element, um eine zusammengeführte Liste zu erhalten.

[!DNL Target] Außerdem können Marketing-Experten das Besucherverhalten innerhalb einer einzelnen Sitzung oder sitzungsübergreifend betrachten:

* **Innerhalb einer einzelnen Sitzung**: Auf Grundlage dessen, was andere Besucher innerhalb einer einzelnen Sitzung unternommen haben.

   Wenn Sie sich das Verhalten innerhalb einer einzelnen Sitzung ansehen, kann es sinnvoll sein, wenn es den Eindruck gibt, dass Produkte sich stark auf der Grundlage einer Nutzung, eines Ereignisses oder eines Ereignisses &quot;verbinden&quot;. Beispielsweise kauft ein Besucher einen Drucker und benötigt möglicherweise auch Tinte und Papier. Oder ein Besucher kauft Erdnussbutter und benötigt möglicherweise auch Brot und Gelee.

* **Über mehrere Sitzungen hinweg**: Auf Grundlage dessen, was andere Besucher über mehrere Sitzungen hinweg unternommen haben.

   Wenn Sie sich das Verhalten über mehrere Sitzungen hinweg ansehen, kann es sinnvoll sein, wenn es den Eindruck gibt, dass Produkte stark aufeinander abgestimmt sind, basierend auf der Präferenz oder dem Geschmack des Besuchers. Zum Beispiel mag ein Besucher Star Wars und vielleicht auch Indiana Jones, auch wenn der Besucher nicht unbedingt beide Filme in derselben Sitzung sehen möchte. Oder ein Besucher mag das Brettspiel &quot;Codenames&quot; und könnte auch das Brettspiel &quot;Avalon&quot;, auch wenn der Besucher nicht beide Spiele gleichzeitig spielen kann. 

[!DNL Target] gibt Empfehlungen für jeden Besucher basierend auf den Artikeln im aktuellen Warenkorb heraus, unabhängig davon, ob Sie sich das Besucherverhalten innerhalb einer einzelnen Sitzung oder sitzungsübergreifend ansehen.

### Ausschließen von bereits im Warenkorb befindlichen Artikeln

Auf Seiten Ihrer gesamten Site können Sie einige Artikel aus Empfehlungen ausschließen. So können Sie beispielsweise keine Artikel empfehlen, die sich bereits im aktuellen Warenkorb des Besuchers befinden. Übergeben Sie dazu die IDs aller Elemente, die Sie ausschließen möchten, mithilfe des speziellen Parameters `excludedIds`.

```
function targetPageParams() {
   return {
      "excludedIds": ["352", "223", "23432", "432", "553"]
      }
}
```

### Seiten zur Kauf-/Bestellbestätigung

Wenn ein Kaufereignis eintritt, geben Sie die Identität des/der gekauften Artikel weiter. Siehe [Konversions-Tracking](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053) in *Implementierung [!DNL Target] ohne Tag-Manager*.

## Konfigurieren globaler Ausnahmen {#exclusions}

Schließen Sie alle Elemente auf globaler Ebene aus, die Sie einem Besucher nie empfehlen möchten. Siehe [Ausnahmen](/help/c-recommendations/c-products/exclusions.md).

## Konfigurieren [!DNL Recommendations] settings {#concept_C1E1E2351413468692D6C21145EF0B84}

Verwalten Sie Ihre Implementierung von [!DNL Recommendations] mithilfe der Einstellungen.

So greifen Sie auf die [!UICONTROL Recommendations-Einstellungen] Optionen, öffnen [!DNL Target] im [!DNL Adobe Experience Cloud]Klicken Sie auf **[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]**.

![](assets/recs_settings.png)

Die folgenden Optionen sind verfügbar:

| Einstellung | Beschreibung |
|--- |--- |
| Benutzerdefinierte globale Mbox | (Optional) Geben Sie die benutzerdefinierte globale Mbox an, die für [!DNL Target]-Aktivitäten verwendet wird. Standardmäßig wird die globale mbox, die von [!DNL Target] verwendet wird, auch für [!DNL Recommendations] verwendet.<br>Hinweis: Diese Option wird auf der [!DNL Target] [!UICONTROL Administration] Seite. Öffnen [!DNL Target]Klicken Sie auf [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]. |
| Vertikaler Markt | Der vertikale Markt hilft Ihnen bei der Kategorisierung Ihrer Empfehlungskriterien. Diese Informationen helfen Mitgliedern Ihres Teams dabei, Kriterien zu finden, die für eine bestimmte Seite sinnvoll sind, z. B. Kriterien, die sich am besten für die Warenkorbseite oder für eine Medienseite eignen. |
| Inkompatible Kriterien filtern | Aktivieren Sie diese Option, um nur diejenigen Kriterien anzuzeigen, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss `entity.id` oder `entity.categoryId` für die aktuellen Element-/aktuellen Kategorieempfehlungen kompatibel sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, deaktivieren Sie diese Option.<br>Es wird empfohlen, dass Sie diese Option deaktivieren, wenn Sie eine Tag-Management-Lösung verwenden.<br>Weitere Informationen zu dieser Option finden Sie unter [FAQ zu Empfehlungen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md). |
| Standard-Hostgruppe | Wählen Sie Ihre Standard-Hostgruppe aus.<br>Die Hostgruppe kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungen zu trennen. Sie können beispielsweise Hostgruppen für Entwicklungs- und Produktionsumgebungen, unterschiedliche Marken oder unterschiedliche Länder verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben. Bereitgestellte Empfehlungen hängen von der in der Anforderung angegebenen Hostgruppe ab.<br>Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.<br>**Hinweis:** Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.<br>Der [!UICONTROL Umgebungs]-Filter ist an den folgenden Stellen in der [!DNL Target]-Benutzeroberfläche verfügbar:<ul><li>Katalogsuche (Recommendations > Katalogsuche)</li><li>Dialogfeld „Sammlung erstellen“ ([!UICONTROL Recommendations > Sammlungen > Neu erstellen])</li><li>Dialogfeld „Sammlung aktualisieren“ ([!UICONTROL Recommendations > Sammlungen > Bearbeiten])</li><li>Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations > Ausschlüsse > Neu erstellen])</li><li>Ausschlussdialogfeld aktualisieren ([!UICONTROL Empfehlungen > Ausnahmen > Bearbeiten])</li></ul>Weitere Informationen finden Sie unter [Hosts](/help/administrating-target/hosts.md). |
| Miniaturansicht Basis-URL | Durch Festlegen einer Basis-URL für Ihren Produktkatalog können Sie relative URLs verwenden, wenn Sie beim Ausfüllen Ihrer URL Miniaturen Ihrer Produkte angeben.<br>Beispiel: <br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br> legt eine URL relativ zur Basis-URL der Miniaturansicht fest. |
| Recommendations-API-Token | Verwenden Sie diesen Token in Recommendations-API-Aufrufen, zum Beispiel der Download-API. |
