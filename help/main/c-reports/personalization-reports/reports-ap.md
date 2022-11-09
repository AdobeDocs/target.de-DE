---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; Aktivitätsstufenbericht; Angebotsebene-Bericht; Angebotsdetailbericht; FAQ
description: Erfahren Sie, wie Sie den Automated Personalization-Zusammenfassungsbericht in Adobe Target interpretieren. Sie können aus diesem Bericht zu den Berichten "Automatisierte Segmente"und "Wichtige Attribute"wechseln.
title: Wie verwende ich die Automated Personalization-Zusammenfassungsberichte?
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: 3a11b368838adb4a6b4f99249db260da8f3f423b
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 34%

---

# ![PREMIUM](/help/main/assets/premium.png) Berichte zur automatisierten Personalisierung

Für Benutzer von [!UICONTROL Automated Personalization] Aktivitäten in [!DNL Adobe Target].

>[!NOTE]
>
>Die Funktion [!UICONTROL Automatisierte Personalisierung] steht als Bestandteil der [!DNL Target Premium]-Lösung zur Verfügung. Sie ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/main/c-intro/intro.md#premium).

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte [!UICONTROL automatisierte Personalisierung] aus der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Berichte.]**

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie [!UICONTROL Automatisierte Personalisierung] in der Dropdownliste [!UICONTROL Typ] auswählen.

1. (Optional) Klicken Sie auf das Symbol zum **[!UICONTROL Herunterladen]**, um die Zusammenfassungsansicht herunterzuladen (etwa zum Vergleichen von Kontroll- und Targeting-Traffic), aufgeschlüsselt nach allen verfügbaren Erfolgsmetriken.

[!UICONTROL Automatisierte Personalisierung] liefert die folgenden Berichte:

* Aktivitätsebene
* Angebotsebene
* Automatisierte Segmente
* Wichtige Attribute

## Aktivitätsstufenbericht {#section_6F72FC5C790B4492B3DCECBFFA971337}

Der Bericht [!UICONTROL Aktivitätsebene] vergleicht die Gesamtleistung beim Einsatz eines „[!UICONTROL Automatisierte Personalisierung]“-Algorithmus mit zufällig bereitgestellten Inhalten (Kontrolle).

![Aktivitätsstufenbericht ](/help/main/c-reports/assets/box_plot_ap.png)

Die Standardregeln für die Auswertung von A/B-Testergebnissen gelten weiterhin, einschließlich Steigerung, Konfidenz, Trends, Dauer und so weiter. Weitere Informationen zur Ergebnisauswertung finden Sie in  [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Angebotsstufenbericht {#section_CAA6409879E349C6906E2BE8156D87A1}

Der Bericht [!UICONTROL Angebotsebene] für das „Random Forest“-Erlebnis vergleicht die Leistung der einzelnen durch Algorithmen bereitgestellten Angebote mit demselben, zufällig bereitgestellten Angebot (Kontrolle). Aus diesem Grund sollten Angebote in dieser Ansicht nicht miteinander verglichen werden.

Klicken Sie auf den Erlebnisalgorithmus (Random Forest oder Kontrolle), um die [!UICONTROL Angebotsebene] Bericht.

![Angebotsstufenbericht in Adobe Target](/help/main/c-reports/assets/ap_OfferLevelRpt.png)

>[!NOTE]
>
>Ein Uhrsymbol zeigt an, dass das Algorithmusmodell noch erstellt wird. Ein Häkchen-Symbol zeigt an, dass der Basisalgorithmus eingerichtet wurde.

Angebote können in [Berichtsgruppen](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md)und diese Berichtsgruppen reduziert und erweitert werden können. Klicken **[!UICONTROL Kontrolle]** oder **[!UICONTROL Targeting]** in der Tabelle, um aggregierte Informationen nach Berichtsgruppen und nicht nach Angeboten anzuzeigen.

## Automatisierte Segmente

Klicken Sie auf [!UICONTROL Automatisierte Segmente] Symbol. Dieser Bericht zeigt, wie unterschiedliche Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Symbol für automatisierte Segmente](/help/main/c-reports/assets/icon-automated-sements-ap.png)

Weitere Informationen finden Sie unter [Bericht &quot;Automatisierte Segmente&quot;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf [!UICONTROL Wichtige Attribute] Symbol. Dieser Bericht zeigt, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Personalisierungsentscheidung des Modells sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol &quot;Wichtige Attribute&quot;](/help/main/c-reports/assets/icon-important-attributes-ap.png)

Weitere Informationen finden Sie unter [Bericht &quot;Wichtige Attribute&quot;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Häufig gestellte Fragen  

### Warum gibt es Unterschiede bei den Daten zwischen den Berichten Aktivitäts- und Angebotsebene?

**[!UICONTROL Aktivitätsebene] Bericht**: Auf der [!UICONTROL Aktivitätsebene] erfassen die Anzahl der Besuche bei den Kontrollerlebnissen im Vergleich zu &quot;zielgerichteter&quot;Traffic. Zielgerichteter Traffic umfasst eine Mischung aus Erkundungs-Traffic und personalisiertem Traffic.

**Angebotsstufenbericht**: Auf der [!UICONTROL Angebotsebene] erfassen die Anzahl der Impressionen für jedes Angebot. Daher wird in einer Aktivität mit mehr als einem Standort die Gesamtzahl der Besuche erfasst, die in der Variablen [!UICONTROL Angebotsebene] ist für alle Berichtsgruppen gleich der Anzahl der Besuche, die für Kontroll- oder Targeting-Traffic im [!UICONTROL Aktivitätsebene] -Bericht die Gesamtanzahl der Standorte in der Aktivität. Impressionen von Standardinhalten, die an Orten auftreten, an denen Standardinhalt verfügbar war, werden in der Angebotgruppe &quot;Standardinhalt&quot;aufgezeichnet. Impressionen von Angeboten, die keiner Berichtsgruppe zugewiesen wurden, werden in der Angebotsgruppe &quot;Nicht gruppiert&quot;aufgezeichnet.

>[!NOTE]
>
>Die Anzahl der Impressionen, die auf der [!UICONTROL Angebotsebene] -Bericht kann keine exakte Ganzzahl sein, sondern nur die Anzahl der Besuche, die im [!UICONTROL Aktivitätsebene] Bericht. Dies ist auf geringfügige Diskrepanzen bei der Erfassung des Daten-Traffics über das Internet zurückzuführen (typische Diskrepanz liegt unter 5 %). Daher ist die Anzahl der Impressionen kein exaktes Vielfaches, wenn sich die Anzahl der in der Aktivität verfügbaren Orte nach der Aktivierung der Aktivität geändert hat.
