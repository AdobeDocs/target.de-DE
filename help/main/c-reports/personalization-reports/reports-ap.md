---
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; Aktivitätsstufenbericht; Angebotsebene-Bericht; Angebotsdetailbericht; FAQ
description: Erfahren Sie, wie Sie den Automated Personalization-Zusammenfassungsbericht in Adobe Target interpretieren. Sie können von diesem Bericht aus zu den Berichten "Automatisierte Segmente"und "Wichtige Attribute"wechseln.
title: Wie verwende ich die Automated Personalization-Zusammenfassungsberichte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 12%

---

# Automated Personalization-Zusammenfassungsberichte

Für Benutzer von [!UICONTROL Automated Personalization] -Aktivitäten in [!DNL Adobe Target] stehen spezialisierte Zusammenfassungsberichte zur Verfügung.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] ist als Teil der [!DNL Target Premium] -Lösung verfügbar. Sie ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) enthalten.

1. Klicken Sie auf **[!UICONTROL Activities]**, klicken Sie in der Liste auf die gewünschte [!UICONTROL Automated Personalization] -Aktivität und klicken Sie dann auf die Registerkarte **[!UICONTROL Reports]** .

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie [!UICONTROL Automated Personalization] aus der Dropdownliste [!UICONTROL Type] auswählen.

1. (Optional) Klicken Sie auf das Symbol &quot;**[!UICONTROL Download]**&quot;, um die Zusammenfassungsansicht herunterzuladen (z. B. Vergleich von Kontroll- und Targeting-Traffic), die nach allen verfügbaren Erfolgsmetriken aufgeschlüsselt ist.

[!UICONTROL Automated Personalization] liefert die folgenden Berichte:

* Aktivitätsebene
* Angebotsebene
* Automatisierte Segmente
* Wichtige Attribute

## Aktivitätsstufenbericht {#section_6F72FC5C790B4492B3DCECBFFA971337}

Der Bericht [!UICONTROL Activity Level] vergleicht die Gesamtleistung der Verwendung eines [!UICONTROL Automated Personalization] -Algorithmus mit zufällig bereitgestellten Inhalten (Kontrolle).

![Aktivitätsstufenbericht](/help/main/c-reports/assets/box_plot_ap.png)

Die Standardregeln für die Auswertung von A/B-Testergebnissen gelten weiterhin, einschließlich Steigerung, Konfidenz, Trends, Dauer und so weiter. Weitere Informationen zur Interpretation der Ergebnisse finden Sie unter [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Angebotsstufenbericht {#section_CAA6409879E349C6906E2BE8156D87A1}

Der Bericht &quot;[!UICONTROL Offer Level]&quot;für das Random Forest-Erlebnis vergleicht die Leistung der einzelnen auf Algorithmen angewendeten Angebote mit demselben zufällig bereitgestellten Angebot (Kontrolle). Aus diesem Grund sollten Angebote in dieser Sicht nicht miteinander verglichen werden.

Klicken Sie auf den Erlebnisalgorithmus (Random Forest oder Kontrolle), um den Bericht [!UICONTROL Offer Level] anzuzeigen.

![Angebotsstufenbericht in Adobe Target](/help/main/c-reports/assets/ap_OfferLevelRpt.png)

>[!NOTE]
>
>Ein Uhrsymbol zeigt an, dass das Algorithmusmodell noch erstellt wird. Ein Häkchen-Symbol zeigt an, dass der Basisalgorithmus eingerichtet wurde.

Angebote können innerhalb von [Berichtsgruppen](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md) angezeigt werden. Diese Berichtsgruppen können reduziert und erweitert werden. Klicken Sie in der Tabelle auf **[!UICONTROL Control]** oder **[!UICONTROL Targeted]** , um aggregierte Informationen nach Berichtsgruppen und nicht nach Angeboten anzuzeigen.

## Automatisierte Segmente

Klicken Sie auf das Symbol &quot;[!UICONTROL Automated Segments]&quot;. Dieser Bericht zeigt, wie unterschiedliche Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP-/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

![Symbol für automatisierte Segmente](/help/main/c-reports/assets/icon-automated-sements-ap.png)

Weitere Informationen finden Sie unter [Bericht &quot;Automatisierte Segmente&quot;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf das Symbol &quot;[!UICONTROL Important Attributes]&quot;. Dieser Bericht zeigt, wie verschiedene Attribute in verschiedenen Aktivitäten wichtiger (oder weniger) für die Personalisierungsentscheidung des Modells sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

![Symbol &quot;Wichtige Attribute&quot;](/help/main/c-reports/assets/icon-important-attributes-ap.png)

Weitere Informationen finden Sie unter [Bericht &quot;Wichtige Attribute&quot;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Häufig gestellte Fragen  

### Warum gibt es Unterschiede bei den Daten zwischen den Berichten Aktivitäts- und Angebotsebene?

**[!UICONTROL Activity Level]report**: Im [!UICONTROL Activity Level] -Bericht aufgezeichnete Besuche erfassen die Anzahl der Besuche des/der Kontrollerlebnisse im Vergleich zu &quot;zielgerichtetem&quot;Traffic. Zielgerichteter Traffic umfasst eine Mischung aus Erkundungs-Traffic und personalisiertem Traffic.

**Angebotsstufenbericht**: Im [!UICONTROL Offer Level] -Bericht aufgezeichnete Impressionen erfassen die Anzahl der Impressionen für jedes Angebot. Daher entspricht die Gesamtzahl der Besuche, die in einer Aktivität mit mehr als einem Standort im [!UICONTROL Offer Level] -Bericht für alle Berichtsgruppen aufgezeichnet wurden, dem Mehrfachen der Anzahl der Besuche, die im [!UICONTROL Activity Level] -Bericht für Kontroll- oder Targeting-Traffic aufgezeichnet wurden, und dem Mehrfachen der Gesamtzahl der Orte in der Aktivität. Impressionen von Standardinhalten, die an Orten auftreten, an denen Standardinhalt verfügbar war, werden in der Angebotgruppe &quot;Standardinhalt&quot;aufgezeichnet. Impressionen von Angeboten, die keiner Berichtsgruppe zugewiesen wurden, werden in der Angebotsgruppe &quot;Nicht gruppiert&quot;aufgezeichnet.

>[!NOTE]
>
>Die Anzahl der im [!UICONTROL Offer Level] -Bericht aufgezeichneten Impressionen ist möglicherweise keine exakte Ganzzahl, die das Vielfache der im [!UICONTROL Activity Level] -Bericht aufgezeichneten Besuche angibt. Dies ist auf geringfügige Diskrepanzen bei der Erfassung des Daten-Traffics über das Internet zurückzuführen (typische Diskrepanz liegt unter 5 %). Daher ist die Anzahl der Impressionen kein exaktes Vielfaches, wenn sich die Anzahl der in der Aktivität verfügbaren Orte nach der Aktivierung der Aktivität geändert hat.
