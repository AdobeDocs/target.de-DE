---
keywords: Recommendations; Recommendations-Algorithmen; Recommendations-Aktivitäten; Recommendations Classic
description: Informationen zu den Unterschieden zwischen den herkömmlichen Recommendations Classic-Aktivitäten und den Recommendations-Aktivitäten in  [!DNL Target]  Premium.
title: Was ist der Unterschied zwischen Recommendations Classic und Recommendations in  [!DNL Target]  Premium?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
TQID: https://experienceleague.adobe.com/EoTkyY0kOwRKT52WIwOuTCoUziIJOnNtTo6llsTNpsM
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 83%

---

# Recommendations Classic und Recommendations-Aktivitäten in [!DNL Target] Premium

Informationen, die bei der Entscheidung zwischen Recommendations Classic und Recommendations-Aktivitäten in Target Premium helfen.

>[!NOTE]
>
>Recommendations-Aktivitäten sind als Teil der [!DNL Target Premium]-Lösung verfügbar. Sie sind in [!DNL Target Standard] nicht ohne [!DNL Target Premium]-Lizenz verfügbar.

Im klassischen [!DNL Recommendations]-Produkt wurden Empfehlungen durch Erstellen einer Datenerfassungs-Mbox auf einer Seite und anschließendes Hinzufügen einer Anzeige-Mbox an einem bestimmten Ort auf der Seite angezeigt. Die [!DNL Recommendations]-Aktivität in [!DNL Target Premium] ermöglicht es Ihnen, Besucherinformationen zu sammeln und Ihre Empfehlungen überall auf der Seite zu erstellen, ohne dass hierfür die Erstellung einer Mbox an jedem Ort, an dem Sie Produkte oder Inhalte empfehlen wollen, erforderlich ist. Ein einfacher JavaScript-Verweis im Header der Seite aktiviert Empfehlungen überall auf der Seite. Verwenden Sie diesen JavaScript-Verweis, um Schlüssel an die globale [!DNL Target]-Mbox zu übergeben, wie zum Beispiel die Schlüssel `entity.id` und `entity.categoryId`.

[!DNL Recommendations Classic] erscheint als eigene Karte in der [!DNL Experience Cloud]-Benutzeroberfläche. Eine [!DNL Recommendations]-Aktivität steht im [!DNL Target Premium]-Workflow zur Verfügung.

[!DNL Recommendations Classic]-Benutzer können weiterhin ihre [!DNL Recommendations]-Mboxes in [!DNL Target Recommendations] verwenden. Sie können auch die klassische und die [!DNL Target]-Vorgehensweisen kombinieren, indem sie ihre Mboxes beibehalten und den JavaScript-Code im Header verwenden, um die [!DNL Recommendations]-Funktionalität für die anderen Elemente auf der Seite zu aktivieren. Um jedoch die volle [!DNL Target]-Funktionalität zu erhalten, sollten [!DNL Recommendations Classic]-Benutzer ihre alte Mbox löschen und sich allein auf [!DNL Target Recommendations] verlassen.

Die [!DNL Recommendations]-Aktivität in [!DNL Target] wird in [!DNL Recommendations Classic] in den folgenden Hauptbereichen verbessert:

## Empfehlungen als Angebot

Sie können Empfehlungen in [!UICONTROL A/B-] (einschließlich [!UICONTROL Automatische Zuordnung] und [!UICONTROL Automatisches Targeting]) und [!UICONTROL Erlebnis-Targeting] (XT) einbeziehen.

Diese Funktion eröffnet völlig neue Funktionen wie z. B.:

* Testen und Targeting von Empfehlungen und Inhalt ohne Recommendations innerhalb derselben Aktivität.
* Experimentieren Sie einfach mit Empfehlungen auf der Seite, einschließlich der Reihenfolge mehrerer Empfehlungen.
* Übertragen Sie Traffic mithilfe der automatischen Zuordnung automatisch an das [!UICONTROL &#x200B; Recommendations-Erlebnis mit &#x200B;] besten Leistung.
* Dynamische Zuweisung von Besuchern zu benutzerspezifischen Recommendations-Erlebnissen basierend auf ihrem Profil mithilfe [!UICONTROL automatischen Targetings].

Erstellen Sie zunächst eine Aktivität des Typs [!UICONTROL A/B]Test oder [!UICONTROL Erlebnis-]) mit dem [!UICONTROL Visual Experience Composer] und verwenden Sie die Aktion [!UICONTROL Einfügen vor], [!UICONTROL Einfügen nach] oder [!UICONTROL Ersetzen mit], um einem Erlebnis Empfehlungen hinzuzufügen.

Weitere Informationen finden Sie unter [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md).

## Kriterien {#section_117709846DAA404580EBE879FFCBD9BA}

[!DNL Target Recommendations] umfasst eine Kriterienbibliothek, die vorab verpackte Sätze von Regeln und Konfigurationen enthält. In [!DNL Recommendations Classic] wurde jede Empfehlung manuell erstellt, wozu ein Formular ausgefüllt und eine Auswahl aus einer umfassenden Regelliste getroffen werden musste. Von nun an können Sie zur Erstellung einer [!DNL Recommendations]-Aktivität einfach einen vorkonfigurierten Kriteriensatz wählen. Sie können weiterhin benutzerdefinierte Empfehlungen erstellen, die Kriterienbibliothek enthält jedoch viele der gebräuchlichsten Konfigurationen - vorgefertigt, um den Prozess zu vereinfachen, und in einer allgemein verständlichen Sprache. Diese vorab verpackten Kriterien können wie vorhanden verwendet oder kopiert und bearbeitet werden, um Ihren spezifischen Bedürfnissen zu entsprechen.

![overview_criteria Bild](assets/overview_criteria.png)

Kriterien werden nach vertikalen Märkten, Seitentypen und Implementierung vorkonfiguriert. Zum Beispiel können Sie nach Kriterien suchen, die auf die Einzelhandelsbranche zutreffen, auf einer Produktseite verwendet werden und Produkte aus einer bestimmten Kategorie anzeigen (wie durch den Parameter `entity.categoryID` definiert).

Weitere Informationen zur Verwendung und Erstellung von Kriterien finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Workflow {#section_76B4A26297BF422382DE2C79A2713D3C}

Der [!DNL Recommendations]-Workflow wurde vereinfacht. Anstatt komplizierte Formulare auszufüllen, folgen Sie einem visuellen Arbeitsablauf, um:

1. die Kriterien auszuwählen,
1. Wählen Sie ein vorkonfiguriertes [Design](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) aus.
1. die resultierenden Empfehlungen in der Vorschau zu betrachten.

## Visuelle Vorschau {#section_639B9E38C9EC4093BF9023EE0F2A15AC}

Sie können Ihre Empfehlungen in einer Vorschau anzeigen, nachdem Sie diese eingerichtet haben, und alle notwendigen Änderungen vornehmen, ohne dass Sie diese auf der Seite erstellen und die Seite dann zum Testen verlassen müssen. Die Vorschau steht in [!DNL Target] zur Verfügung.

## Targeting {#section_93295EA0DBA14210B8518AF4802A459F}

In [!DNL Recommendations Classic] gab es sechs Targeting-Optionen. Recommendations-Aktivitäten verwenden die gesamte Bandbreite der Targeting-Optionen von Target. Definieren Sie eine Zielgruppe entweder mit [!DNL Target] oder anderen [!DNL Adobe Experience Cloud]-Zielgruppen (z. B. [!DNL Audience Manager] und [!DNL Analytics]), wählen Sie dann den Prozentsatz der Aktivitätsteilnehmer aus, die jeden Entwurf sehen, und den Prozentwerten, die das Steuerelement sehen.

![Overview_Targeting-Bild](assets/overview_targeting.png)

## Berichterstellung {#section_25C2FCCE4BC1488496C517C0470B5CD6}

In [!DNL Target] bietet [!DNL Recommendations] eine verbesserte Berichterstellung, die auf die Möglichkeiten aufbaut, die [!DNL Target] und [!DNL Experience Cloud] bieten. Anstatt lediglich den Lift anzuzeigen, der durch [!DNL Recommendations] im Vergleich zu den Ergebnissen ohne erreicht wird, können Sie die vollständigen Informationen über Ihre [!DNL Recommendations]Recommendations-Aktivität anzeigen.

![overview_report image](assets/overview_report.png)
