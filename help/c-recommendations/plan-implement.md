---
keywords: Recommendations; Einstellungen; Voreinstellungen; vertikaler Markt; Filtern inkompatibler Kriterien; Standard-Hostgruppe; Thumb-Base-URL; Recommendations-API-Token
description: 'Erfahren Sie, wie Sie Recommendations-Aktivitäten in Adobe Target implementieren. '
title: Wie implementiere ich die Recommendations-Aktivitäten?
feature: Recommendations
exl-id: b6edb504-a8b6-4379-99c1-6907e71601f9
source-git-commit: 68670f0b7753ee34c186a380004620ae4ba0cfd1
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 37%

---

# ![PREMIUM](/help/assets/premium.png) Recommendations planen und umsetzen

Vor dem Einrichten der ersten [!DNL Recommendations] Aktivität in [!DNL Adobe Target]führen Sie die folgenden Schritte aus:

| Schritt | Details |
|--- |--- |
| ![Schritt 1](/help/c-recommendations/assets/step1_red.png) | [Implementierung [!DNL Adobe Target]](#implement-target) auf den Oberflächen von Websites und mobilen Apps, die Sie zur Erfassung des Benutzerverhaltens und zur Bereitstellung von Empfehlungen verwenden möchten. |
| ![Schritt 2](/help/c-recommendations/assets/step2_red.png) | [Richten Sie Ihre [!DNL Recommendations] Katalog](#rec-catalog) von Produkten oder Inhalten, die Sie Ihren Benutzern empfehlen möchten. |
| ![Schritt 3](/help/c-recommendations/assets/step3_red.png) | [Verhaltensinformationen und Kontext weitergeben](#pass-behavioral) nach [!DNL Adobe Target Recommendations] , damit sie personalisierte Empfehlungen abgeben kann. |
| ![Schritt 4](/help/c-recommendations/assets/step4_red.png) | [Globale Ausschlüsse konfigurieren](#exclusions). |
| ![Schritt 5](/help/c-recommendations/assets/step5_red.png) | [Konfigurieren [!DNL Recommendations] Einstellungen](#concept_C1E1E2351413468692D6C21145EF0B84). |

## Adobe Target implementieren {#implement-target}

[!DNL Target Recommendations] erfordert die Implementierung von [!DNL Adobe Experience Platform Web SDK] oder at.js 0.9.2 (oder neuer). Siehe [Zielgruppe implementieren](/help/c-implementing-target/implementing-target.md) für weitere Informationen.

## Recommendations-Katalog einrichten {#rec-catalog}

um Empfehlungen hoher Qualität abzugeben, [!DNL Target] müssen über die Produkte oder Inhalte informiert sein, die Sie empfehlen möchten. Ihr Katalog sollte in der Regel drei Arten von Informationen über die Elemente enthalten, die Sie empfehlen möchten. Nehmen wir an, Sie empfehlen Filme. Folgendes einschließen:

1. Daten, die dem Benutzer angezeigt werden sollen, der die Empfehlung erhält. Sie können z. B. den Namen des Films und eine URL für ein Miniaturbild des Filmplakats anzeigen.
1. Daten, die zur Anwendung von Marketing- und Merchandising-Steuerelementen nützlich sind. Sie können zum Beispiel die Bewertung des Films anzeigen, sodass Sie keine NC-17-Filme empfehlen.
1. Daten, die zur Bestimmung der Ähnlichkeit von Elementen mit anderen Elementen nützlich sind. Sie können beispielsweise das Genre des Films und den Regisseur des Films anzeigen.

[!DNL Target] Angebot mehrerer Integrationsoptionen zum Ausfüllen des Katalogs. Diese Optionen können zusammen verwendet werden, um verschiedene Elemente im Katalog zu aktualisieren oder um verschiedene Elementattribute auf verschiedenen Frequenzen zu aktualisieren.

| Methode | Was es ist | Einsatz | Zusätzliche Informationen |
| --- | --- | --- | --- |
| Katalog-Feed | einen Feed planen (CSV, Google Product XML) oder [!DNL Analytics Product Classifications]), die täglich hochgeladen und aufgenommen werden. | Zum Senden von Informationen über mehrere Elemente gleichzeitig. Zum Senden von Informationen, die sich selten ändern. | Siehe [Feeds](/help/c-recommendations/c-products/feeds.md). |
| Entitäts-API | Rufen Sie eine API auf, um Aktualisierungen für ein einzelnes Element an die Minute zu senden. | Für das Versenden von Updates, da sie sich um jeweils ein Element handeln. Für den Versand von Informationen, die sich häufig ändern (z.B. Preis, Bestand/Lagerbestand). | Siehe [Entitäts-API-Entwicklerdokumentation](https://developers.adobetarget.com/api/recommendations/#tag/Entities). |
| Aktualisierungen auf der Seite weitergeben | Mit JavaScript auf der Seite oder über die Versand-API an aktuelle Updates für ein einzelnes Element senden. | Für das Versenden von Updates, da sie sich um jeweils ein Element handeln. Für den Versand von Informationen, die sich häufig ändern (z.B. Preis, Bestand/Lagerbestand). | Siehe Ansichten zu Elementen/Produktseiten unten. |

Die meisten Kunden sollten mindestens einen Feed implementieren. Sie können Ihren Feed dann mit Aktualisierungen für häufig geänderte Attribute oder Elemente ergänzen, indem Sie entweder die Entitäts-API oder die auf der Seite angezeigte Methode verwenden.

## Verhaltensinformationen und Kontext weitergeben {#pass-behavioral}

Die Verhaltensinformationen und der Kontext, an die Sie weitergeben sollten [!DNL Target] hängt von der Aktion ab, die Ihr Besucher einnimmt und die häufig mit dem Seitentyp verknüpft ist, mit dem Ihr Besucher interagiert.

### Element-Ansichten/Produktseiten

Auf Seiten, auf denen ein Besucher ein einzelnes Element anzeigt, wie z. B. eine Produktdetailseite, sollten Sie die Identität des Elements übergeben, das der Besucher anzeigt. Sie sollten auch die detaillierteste Kategorie des Elements, das der Besucher anzeigt, übergeben, damit die Filterempfehlungen der aktuellen Kategorie zugeordnet werden können.

Sie können auch bestimmte schnell wechselnde Attribute auf der Produktseite selbst übergeben. Sie können zum Beispiel den Preis (`value`) und Bestand/Lagerbestand.

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

### Ansichten/Kategorien der Kategorie

Auf einer Kategorie-Seite möchten Sie Ihre Empfehlungen wahrscheinlich auf Produkte oder Inhalte in dieser Kategorie beschränken. Stellen Sie dazu sicher, dass Sie die Identität der aktuell angezeigten Kategorie weitergeben.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "running-shoes" 
      } 
   } 
}
```

### Hinzufügen zum Warenkorb/Ansichten zum Warenkorb/Checkout-Seiten

Auf einer Warenkorbseite können Sie Elemente basierend auf dem Inhalt des aktuellen Warenkorbs des Besuchers empfehlen. Übergeben Sie dazu die IDs aller Artikel im aktuellen Warenkorb des Besuchers unter Verwendung des speziellen Parameters `cartIds`.

```
function targetPageParams() {
   return {
      "cartIds": ["352", "223", "23432", "432", "553"]
      }
}
```

### Elemente ausschließen, die sich bereits im Warenkorb des Besuchers befinden

Auf Seiten in Ihrer Site können Sie einige Elemente aus den Empfehlungen ausschließen. Sie sollten beispielsweise keine Elemente empfehlen, die sich bereits im aktuellen Warenkorb des Besuchers befinden. Übergeben Sie dazu die IDs aller auszuschließenden Elemente mithilfe des speziellen Parameters. `excludedIds`.

```
function targetPageParams() {
   return {
      "excludedIds": ["352", "223", "23432", "432", "553"]
      }
}
```

### Kauf-/Bestellbestätigungsseiten

Wenn ein Ereignis des Kaufs auftritt, geben Sie die Identität des/der erworbenen Artikels/Artikel weiter. Siehe [Konversionen verfolgen](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053) in *Implementierung [!DNL Target] ohne Tag-Manager*.

## Globale Ausschlüsse konfigurieren {#exclusions}

Alle Elemente auf globaler Ebene ausschließen, die einem Besucher nie empfohlen werden sollen. Siehe [Ausnahmen](/help/c-recommendations/c-products/exclusions.md).

## Konfigurieren [!DNL Recommendations] Einstellungen {#concept_C1E1E2351413468692D6C21145EF0B84}

Verwalten Sie Ihre Implementierung von [!DNL Recommendations] mithilfe der Einstellungen.

So greifen Sie auf [!UICONTROL Recommendations-Einstellungen] Optionen öffnen [!DNL Target] in [!DNL Adobe Experience Cloud], und klicken Sie dann auf **[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]**.

![](assets/recs_settings.png)

Die folgenden Optionen sind verfügbar:

| Einstellung | Beschreibung |
|--- |--- |
| Benutzerdefinierte globale Mbox | (Optional) Geben Sie die benutzerdefinierte globale Mbox an, die für [!DNL Target]-Aktivitäten verwendet wird. Standardmäßig wird die globale mbox, die von [!DNL Target] verwendet wird, auch für [!DNL Recommendations] verwendet.<br>Hinweis: Diese Option wird auf der [!DNL Target] [!UICONTROL Anwendung] Seite. Öffnen [!DNL Target], und klicken Sie dann auf [!UICONTROL Anwendung] > [!UICONTROL Visual Experience Composer]. |
| Vertikaler Markt | Der vertikale Markt hilft Ihnen bei der Kategorisierung Ihrer Empfehlungskriterien. Diese Informationen helfen Mitgliedern Ihres Teams bei der Suche nach Kriterien, die für eine bestimmte Seite sinnvoll sind, z. B. Kriterien, die für die Warenkorbseite oder für eine Medienseite am besten geeignet sind. |
| Inkompatible Kriterien filtern | Aktivieren Sie diese Option, um nur diejenigen Kriterien anzuzeigen, bei denen die ausgewählte Seite die erforderlichen Daten übermittelt. Nicht alle Kriterien werden auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss übergeben werden `entity.id` oder `entity.categoryId` damit die Empfehlungen für das aktuelle Element/die aktuelle Kategorie kompatibel sind. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, deaktivieren Sie diese Option.<br>Es wird empfohlen, dass Sie diese Option deaktivieren, wenn Sie eine Tag-Management-Lösung verwenden.<br>Weitere Informationen zu dieser Option finden Sie unter [FAQ zu Empfehlungen](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md). |
| Standard-Hostgruppe | Wählen Sie Ihre Standard-Hostgruppe aus.<br>Die Hostgruppe kann verwendet werden, um die verfügbaren Elemente in Ihrem Katalog für verschiedene Verwendungen zu trennen. Sie können beispielsweise Hostgruppen für Entwicklungs- und Produktionsumgebungen, unterschiedliche Marken oder unterschiedliche Länder verwenden. Standardmäßig basieren die Vorschauergebnisse in „Katalogsuche“, „Sammlungen“ und „Ausnahmen“ auf der Standardhostgruppe. (Mit dem Umgebungsfilter können Sie auch eine andere Hostgruppe auswählen, um die Ergebnisse in der Vorschau anzuzeigen.) Neu hinzugefügte Elemente sind standardmäßig in allen Hostgruppen verfügbar, es sei denn, beim Erstellen oder Aktualisieren des Elements wurde eine Umgebungs-ID angegeben. Bereitgestellte Empfehlungen hängen von der in der Anforderung angegebenen Hostgruppe ab.<br>Wenn Ihre Produkte nicht angezeigt werden, stellen Sie sicher, dass Sie die richtige Hostgruppe verwenden. Wenn Sie beispielsweise Ihre Empfehlung so festlegen, dass eine Staging-Umgebung verwendet wird, und Ihre Hostgruppe auf „Staging“ eingestellt ist, müssen Sie eventuell Ihre Erfassung in der Staging-Umgebung neu erstellen, damit die Angebote angezeigt werden. Um zu sehen, welche Produkte in jeder Umgebung verfügbar sind, verwenden Sie für jede Umgebung die Katalogsuche. Sie können auch eine Vorschau der Inhalte von Recommendations-Sammlungen und -Ausschlüssen für eine ausgewählte Umgebung (Hostgruppe) anzeigen.<br>**Hinweis:** Nachdem Sie die ausgewählte Umgebung geändert haben, müssen Sie auf „Suchen“ klicken, um die zurückgegebenen Ergebnisse zu aktualisieren.<br>Der [!UICONTROL Umgebungs]-Filter ist an den folgenden Stellen in der [!DNL Target]-Benutzeroberfläche verfügbar:<ul><li>Katalogsuche (Recommendations > Katalogsuche)</li><li>Dialogfeld „Sammlung erstellen“ ([!UICONTROL Recommendations > Sammlungen > Neu erstellen])</li><li>Dialogfeld „Sammlung aktualisieren“ ([!UICONTROL Recommendations > Sammlungen > Bearbeiten])</li><li>Dialogfeld „Ausschluss erstellen“ ([!UICONTROL Recommendations > Ausschlüsse > Neu erstellen])</li><li>Ausschlussdialogfeld aktualisieren ([!UICONTROL Empfehlungen > Ausnahmen > Bearbeiten])</li></ul>Weitere Informationen finden Sie unter [Hosts](/help/administrating-target/hosts.md). |
| Miniaturansicht Basis-URL | Durch Festlegen einer Basis-URL für Ihren Produktkatalog können Sie relative URLs verwenden, wenn Sie beim Ausfüllen Ihrer URL Miniaturen Ihrer Produkte angeben.<br>Beispiel: <br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br> legt eine URL relativ zur Basis-URL der Miniaturansicht fest. |
| Recommendations-API-Token | Verwenden Sie diesen Token in Recommendations-API-Aufrufen, zum Beispiel der Download-API. |
