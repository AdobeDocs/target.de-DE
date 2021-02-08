---
keywords: Targeting;AP-Berichte;Automatisierte Personalisierungsberichte;Bericht auf Aktivität;Bericht auf Angebot-Ebene;Bericht auf Angebot-Ebene;FAQ
description: Erfahren Sie, wie Sie den Automated Personalization-Zusammenfassungsbericht in Adobe Target interpretieren. Sie können in diesem Bericht zu den Berichten zu automatisierten Segmenten und wichtigen Attributen wechseln.
title: Wie verwende ich die Automated Personalization-Zusammenfassungsberichte?
feature: Reports
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 40%

---


# ![PREMIUM](/help/assets/premium.png) Berichte zur automatisierten Personalisierung

Spezialisierte Zusammenfassungsberichte stehen Benutzern der Aktivitäten [!UICONTROL Automated Personalization] in [!DNL Adobe Target] zur Verfügung.

>[!NOTE]
>
>Die Funktion [!UICONTROL Automatisierte Personalisierung] steht als Bestandteil der [!DNL Target Premium]-Lösung zur Verfügung. Sie ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/c-intro/intro.md#premium).

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte [!UICONTROL automatisierte Personalisierung] aus der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Berichte.]**

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie [!UICONTROL Automatisierte Personalisierung] in der Dropdownliste [!UICONTROL Typ] auswählen.

1. (Optional) Klicken Sie auf das Symbol zum **[!UICONTROL Herunterladen]**, um die Zusammenfassungsansicht herunterzuladen (etwa zum Vergleichen von Kontroll- und Targeting-Traffic), aufgeschlüsselt nach allen verfügbaren Erfolgsmetriken.

[!UICONTROL Automatisierte Personalisierung] liefert die folgenden Berichte:

* Aktivität
* Angebot-Ebene
* Automatisierte Segmente
* Wichtige Attribute

## Aktivitätsstufenbericht {#section_6F72FC5C790B4492B3DCECBFFA971337}

Der Bericht [!UICONTROL Aktivitätsebene] vergleicht die Gesamtleistung beim Einsatz eines „[!UICONTROL Automatisierte Personalisierung]“-Algorithmus mit zufällig bereitgestellten Inhalten (Kontrolle).

![Aktivitätsstufenbericht ](/help/c-reports/assets/box_plot_ap.png)

Die Standardregeln für die Auswertung von A/B-Testergebnissen gelten weiterhin, einschließlich Steigerung, Konfidenz, Trends, Dauer und so weiter. Weitere Informationen zur Ergebnisauswertung finden Sie in  [Über die Konversionsrate](/help/c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844)

## Angebotsstufenbericht {#section_CAA6409879E349C6906E2BE8156D87A1}

Der Bericht [!UICONTROL Angebotsebene] für das „Random Forest“-Erlebnis vergleicht die Leistung der einzelnen durch Algorithmen bereitgestellten Angebote mit demselben, zufällig bereitgestellten Angebot (Kontrolle). Aus diesem Grund sollten Angebote in dieser Ansicht nicht miteinander verglichen werden.

Klicken Sie auf den Erlebnisalgorithmus (Random Forest oder Kontrolle), um den Bericht [!UICONTROL Angebot Level] Ansicht.

![](assets/ap_OfferLevelRpt.png)

Angebote können innerhalb von Berichtsgruppen angezeigt werden. Diese Berichtsgruppen können minimiert und maximiert werden. Wählen Sie in der Dropdownliste [!UICONTROL Berichterstellungsgruppe] aus, um sich Details nach Berichtsgruppen und nicht nach Angeboten anzeigen zu lassen.

>[!NOTE]
>
>Das Uhrsymbol zeigt an, dass das Algorithmusmodell noch erstellt wird. Das Häkchen-Symbol zeigt an, dass der Basisalgorithmus eingerichtet wurde.

## Automatisierte Segmente

Klicken Sie auf das Symbol [!UICONTROL Automatisierte Segmente]. Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebot/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Symbol für automatisierte Segmente](/help/c-reports/assets/icon-automated-sements-ap.png)

Weitere Informationen finden Sie unter [Bericht &quot;Automatisierte Segmente](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md)&quot;.

## Wichtige Attribute

Klicken Sie auf das Symbol [!UICONTROL Wichtige Attribute]. Dieser Bericht zeigt, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Art und Weise sind, wie das Modell sich für die Personalisierung entscheidet. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol &quot;Wichtige Attribute&quot;](/help/c-reports/assets/icon-important-attributes-ap.png)

Weitere Informationen finden Sie unter [Bericht &quot;Wichtige Attribute](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md)&quot;.

## Häufig gestellte Fragen  

### Warum unterscheiden sich die Daten zwischen den Berichten auf Ebene der Aktivität und auf Ebene der Angebote?

**[!UICONTROL Bericht ] zur** Aktivität: Besuche, die im Bericht  [!UICONTROL Aktivität ] Levelbericht aufgezeichnet werden, erfassen die Anzahl der Besuche bei Kontrollerlebnissen im Vergleich zu Kontrollerlebnissen. &quot;zielgerichteter&quot;Traffic. Zielgerichteter Traffic umfasst eine Kombination aus Erkundungstransfer und personalisiertem Traffic.

**Bericht** auf Angebot-Ebene: Impressionen, die im  [!UICONTROL Angebot ] Levelreport erfasst werden, erfassen die Anzahl der Impressionen für jedes Angebot. Daher entspricht die Gesamtzahl der Besuche, die in einer Aktivität mit mehr als einem Ort im Bericht [!UICONTROL Angebot-Ebene] aller Berichte-Gruppen aufgezeichnet wurden, dem Mehrfachen der Anzahl der Besuche, die für Kontroll- oder Targeting-Traffic im Bericht [!UICONTROL Aktivität-Ebene] aufgezeichnet wurden, dem Mehrfachen der Gesamtzahl der Orte in der Aktivität. Impressionen von Standardinhalten, die an Orten auftreten, an denen Standardinhalt verfügbar war, werden in der Angebot-Gruppe &quot;Standardinhalt&quot;aufgezeichnet. Impressionen von Angeboten, die keiner Berichte-Gruppe zugewiesen wurden, werden in der Gruppe &quot;Nicht gruppierte&quot;Angebot aufgezeichnet.

>[!NOTE]
>
>Die Anzahl der Impressionen, die im Bericht [!UICONTROL Angebot Level] aufgezeichnet werden, ist möglicherweise keine exakte Ganzzahl, bei der es sich um ein Vielfaches der im Bericht [!UICONTROL Aktivität Level] aufgezeichneten Besuche handelt. Dies ist auf geringfügige Diskrepanzen bei der Erfassung des Datenverkehrs über das Internet zurückzuführen (die typische Diskrepanz liegt unter 5 %). Die Anzahl der Impressionen ist daher kein exaktes Vielfaches, wenn sich die Anzahl der in der Aktivität verfügbaren Stellen nach der Aktivierung der Aktivität verändert hat.
