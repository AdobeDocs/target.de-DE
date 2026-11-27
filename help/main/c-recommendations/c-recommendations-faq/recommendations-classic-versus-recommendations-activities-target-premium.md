---
keywords: Recommendations; Recommendations-Algorithmen; Recommendations-Aktivitäten; Recommendations Classic
description: Informationen zu den Unterschieden zwischen den herkömmlichen Recommendations Classic- und Recommendations-Aktivitäten in [!DNL Target] Premium.
title: Was ist der Unterschied zwischen Recommendations Classic und Recommendations in [!DNL Target] Premium?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
TQID: 'https://experienceleague.adobe.com/EoTkyY0kOwRKT52WIwOuTCoUziIJOnNtTo6llsTNpsM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 19%
---
# Recommendations Classic und Recommendations-Aktivitäten in [!DNL Target] Premium {#classic-versus-activities}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie sich [!DNL Recommendations Classic] von [!DNL Recommendations] Aktivitäten in [!DNL Target Premium] unterscheidet, um zwischen ihnen zu wählen.

>[!ENDSHADEBOX]

>[!NOTE]
>
>[!DNL Recommendations] Activities sind als Teil der [!DNL Target Premium]-Lösung verfügbar. Sie sind in [!DNL Target Standard] nicht ohne [!DNL Target Premium]-Lizenz verfügbar.

Im klassischen [!DNL Recommendations]-Produkt wurden Empfehlungen durch Erstellen einer Datenerfassungs-Mbox auf einer Seite und anschließendes Hinzufügen einer Anzeige-Mbox an einem bestimmten Ort auf der Seite angezeigt. Die [!DNL Recommendations] in [!DNL Target Premium] erfasst Besucherinformationen und erstellt die Recommendations an jeder beliebigen Stelle auf der Seite, ohne Mbox für jeden Ort, an dem Produkte oder Inhalte empfohlen werden. Eine JavaScript-Referenz in der Kopfzeile der Seite ermöglicht Empfehlungen an jeder beliebigen Stelle auf der Seite. Diese Referenz übergibt Schlüssel wie die `entity.id`- und `entity.categoryId` an die globale [!DNL Target]-Mbox.

[!DNL Recommendations Classic] erscheint als eigene Karte in der [!DNL Experience Cloud]-Benutzeroberfläche. Eine [!DNL Recommendations]-Aktivität steht im [!DNL Target Premium]-Workflow zur Verfügung.

[!DNL Recommendations Classic]-Benutzer können weiterhin ihre [!DNL Recommendations]-Mboxes in [!DNL Target Recommendations] verwenden. Die klassischen und [!DNL Target] Ansätze können auch kombiniert werden, indem die Mboxes beibehalten und der JavaScript-Code in der Kopfzeile verwendet wird, um [!DNL Recommendations] Funktionalität für die anderen Seitenelemente zu aktivieren. Um jedoch die volle [!DNL Target] zu erhalten, möchten [!DNL Recommendations Classic] Benutzer möglicherweise die alte Mbox löschen und verlassen sich ausschließlich auf [!DNL Target Recommendations].

Die [!DNL Recommendations] Aktivität in [!DNL Target] verbessert die [!DNL Recommendations Classic] in den folgenden Hauptbereichen.

## Empfehlungen als Angebot {#recs-as-offer}

Recommendations können in [!UICONTROL A/B-Test]-Aktivitäten (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) und [!UICONTROL Erlebnis-Targeting] (XT) enthalten sein. Dies ermöglicht unter anderem das Testen und Targeting von Recommendations und Nicht-Recommendations-Inhalten innerhalb derselben Aktivität. Weitere Informationen finden Sie unter [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

## Kriterien {#criteria-comparison}

[!DNL Target Recommendations] umfasst eine Kriterienbibliothek mit vorkonfigurierten Regeln und Konfigurationen. [!DNL Recommendations Classic] wurde jede Empfehlung manuell erstellt, indem ein Formular ausgefüllt und aus einer großen Liste von Regeln ausgewählt wurde. Wenn eine [!DNL Recommendations] erstellt wird, wird ein vorkonfigurierter Kriteriensatz ausgewählt. Benutzerdefinierte Empfehlungen können weiterhin erstellt werden, aber die Kriterienbibliothek enthält viele der gängigsten Konfigurationen, die vorkonfiguriert wurden, um den Prozess zu vereinfachen, und in denen die Sprache verwendet wird, die von Personen verstanden wird. Die vorkonfigurierten Kriterien können unverändert verwendet oder kopiert und bearbeitet werden, um spezifischen Anforderungen gerecht zu werden.

![Folie mit einer Kriterienkarte, „Up-Sell“, mit der Sprache, die die Leute verstehen, den Regeln und der Logik und der Konfiguration](assets/overview_criteria.png)

Kriterien werden nach vertikalen Märkten, Seitentypen und Implementierung vorkonfiguriert. Beispielsweise können die Kriterien, die für die vertikale Einzelhandelsseite gelten, zur Verwendung auf einer Produktseite gefunden werden, auf der Produkte aus einer bestimmten Kategorie angezeigt werden (wie durch den `entity.categoryID`-Parameter definiert).

Weitere Informationen zur Verwendung und Erstellung von Kriterien finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Workflow {#workflow-comparison}

Der [!DNL Recommendations]-Workflow wird vereinfacht. Anstelle von komplizierten Formularen führt ein visueller Workflow durch die folgenden Schritte:

1. die Kriterien auszuwählen,
1. Wählen Sie ein vorkonfiguriertes [Design](/help/main/c-recommendations/c-design-overview/create-design.md#create-design) aus.
1. die resultierenden Empfehlungen in der Vorschau zu betrachten.

## Visuelle Vorschau {#visual-preview}

Empfehlungen können nach dem Einrichten in der Vorschau angezeigt werden. Alle erforderlichen Änderungen können vorgenommen werden, ohne die Empfehlungen auf der Seite zu erstellen und anschließend zu testen. Die Vorschau steht in [!DNL Target] zur Verfügung.

## Targeting {#targeting-comparison}

[!DNL Recommendations Classic] hatte sechs Targeting-Optionen. [!DNL Recommendations] -Aktivitäten nutzen die gesamte Palette der [!DNL Target] Targeting-Optionen. Eine Zielgruppe wird mithilfe von [!DNL Target] oder anderen [!DNL Adobe Experience Cloud] Zielgruppen (wie [!DNL Audience Manager] und [!DNL Analytics]) definiert. Der Prozentsatz der Aktivitätseinsteiger, die die einzelnen Designs sehen, und der Prozentsatz, der das Steuerelement sieht, werden dann ausgewählt.

![Flussdiagramm mit der Zielgruppe „Alle Besucher“, den Up-Sell-Kriterien, drei Designs mit jeweils 30 % Traffic und der Kontrollgruppe „Keine Empfehlung“](assets/overview_targeting.png)

## Berichterstellung {#reporting-comparison}

[!DNL Target] bietet [!DNL Recommendations] eine verbesserte Berichterstellung, die die Funktionen von [!DNL Target] und [!DNL Experience Cloud] nutzt. Anstatt nur die Steigerung anzuzeigen, die [!DNL Recommendations] im Vergleich zu den Ergebnissen ohne Steigerung bietet, enthalten die Berichte vollständige Informationen über die [!DNL Recommendations].

