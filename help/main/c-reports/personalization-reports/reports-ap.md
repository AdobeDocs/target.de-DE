---
keywords: Zielgruppenbestimmung;AP-Berichte;Automated Personalization-Berichte;Bericht auf Aktivitätsebene;Bericht auf Angebotsebene;Bericht mit Angebotsdetails;FAQ
description: Erfahren Sie, wie der Automated Personalization-Zusammenfassungsbericht in Adobe Target interpretiert wird. Von diesem Bericht aus können Sie zu den Berichten Automatisierte Segmente und Wichtige Attribute wechseln.
title: Wie verwende ich die Automated Personalization-Zusammenfassungsberichte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
TQID: https://experienceleague.adobe.com/Gj9Jo0NHnSxGE4BpvFbd0SudYjbkP4yrV3GFHWHNPjw
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 702
ht-degree: 21%

---

# Automated Personalization-Zusammenfassungsberichte

Benutzende von [!UICONTROL Automated Personalization-Aktivitäten] in [!DNL Adobe Target] können spezialisierte Zusammenfassungsberichte erhalten.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Es ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/main/c-intro/intro.md#premium).

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte [!UICONTROL automatisierte Personalisierung] aus der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Berichte]**.

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol Filtern ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um die Liste zu filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Typ], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metriktyp] und [!UICONTROL Activity Source] auswählen.

1. (Optional) Klicken Sie auf das Symbol **[!UICONTROL Herunterladen]** ( ![Herunterladen-Symbol](/help/main/assets/icons/Download.svg) ), um die Zusammenfassungsansicht herunterzuladen (z. B. Vergleich von Kontroll- und Targeting-Traffic), aufgeschlüsselt nach allen verfügbaren Erfolgsmetriken.

[!UICONTROL Automatisierte Personalisierung] liefert die folgenden Berichte:

* Aktivitätsebene
* Angebotsebene
* Automatisierte Segmente
* Wichtige Attribute

## Aktivitätsstufenbericht {#section_6F72FC5C790B4492B3DCECBFFA971337}

Der Bericht [!UICONTROL Aktivitätsebene] vergleicht die Gesamtleistung beim Einsatz eines „[!UICONTROL Automatisierte Personalisierung]“-Algorithmus mit zufällig bereitgestellten Inhalten (Kontrolle).

Die Standardregeln für die Auswertung von A/B-Testergebnissen gelten weiterhin, einschließlich Steigerung, Konfidenz, Trends, Dauer und so weiter. Weitere Informationen zur Interpretation der Ergebnisse finden Sie unter [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Angebotsstufenbericht {#section_CAA6409879E349C6906E2BE8156D87A1}

Der Bericht [!UICONTROL Angebotsebene] für das „Random Forest“-Erlebnis vergleicht die Leistung der einzelnen durch Algorithmen bereitgestellten Angebote mit demselben, zufällig bereitgestellten Angebot (Kontrolle). Aus diesem Grund sollten Angebote in dieser Ansicht nicht miteinander verglichen werden.

Klicken Sie auf den Erlebnisalgorithmus (zufällige Gesamtstruktur oder Kontrolle), um den Bericht [!UICONTROL Angebotsebene] anzuzeigen.

>[!NOTE]
>
>Ein Uhrensymbol zeigt an, dass das Algorithmusmodell noch im Aufbau begriffen ist. Ein Häkchensymbol zeigt an, dass der Basisalgorithmus eingerichtet wurde.

Angebote können in [Berichtsgruppen“ angezeigt ](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md). Diese Berichtsgruppen können reduziert und erweitert werden. Klicken Sie **[!UICONTROL der Tabelle auf]** Kontrolle **[!UICONTROL oder Targeting]**, um aggregierte Informationen nach Berichtsgruppen und nicht nach Angeboten anzuzeigen.

## Automatisierte Segmente

Klicken Sie auf [!UICONTROL  Symbol &quot;] Segmente“. Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

Weitere Informationen finden Sie unter [Bericht zu automatisierten Segmenten](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf [!UICONTROL  Symbol „Wichtige ]&quot;. Dieser Bericht zeigt, wie in verschiedenen Aktivitäten verschiedene Attribute für die Personalisierungsentscheidung des Modells mehr (oder weniger) wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

Weitere Informationen finden Sie unter [Bericht zu wichtigen Attributen](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Häufig gestellte Fragen

### Warum unterscheiden sich die Daten zwischen den Berichten Aktivitätsebene und Angebotsebene?

**[!UICONTROL Aktivitätsebene] Bericht**: Besuche, die auf dem Bericht [!UICONTROL Aktivitätsebene] aufgezeichnet wurden, erfassen die Anzahl der Besuche des Kontrollerlebnisses/der Kontrollerlebnisse im Vergleich zu „zielgerichtetem“ Traffic. Der zielgerichtete Traffic umfasst eine Mischung aus Exploration-Traffic und personalisiertem Traffic.

**Bericht auf Angebotsebene**: Die im Bericht [!UICONTROL Angebotsebene] erfassten Impressionen erfassen die Anzahl der Impressionen für jedes Angebot. Daher entspricht in einer Aktivität mit mehr als einem Standort die Gesamtzahl der Besuche, die im Bericht [!UICONTROL Angebotsebene] für alle Berichtsgruppen erfasst werden, dem Vielfachen der Anzahl der Besuche, die für Kontroll- oder Zieldatenverkehr im Bericht [!UICONTROL Aktivitätsebene] erfasst wurden, multipliziert mit der Gesamtzahl der Standorte in der Aktivität. Impressionen von Standardinhalten, die an Orten auftreten, an denen Standardinhalte als verfügbare Option verfügbar waren, werden in der Angebotsgruppe „Standardinhalt“ aufgezeichnet. Impressionen von Angeboten, deren Zuweisung zu einer Berichtsgruppe aufgehoben wurde, werden in der Angebotsgruppe „Ungruppiert“ erfasst.

>[!NOTE]
>
>Die Anzahl der im Bericht [!UICONTROL Angebotsebene] aufgezeichneten Impressionen ist möglicherweise kein exaktes ganzzahliges Vielfaches der Anzahl der im Bericht [!UICONTROL Aktivitätsebene] aufgezeichneten Besuche. Dies liegt an geringfügigen Abweichungen, die bei der Erfassung des Berichtsdatenverkehrs über das Internet auftreten (die typische Diskrepanzrate liegt unter 5 %). Daher ist die Anzahl der Impressionen kein exaktes Vielfaches, wenn die Anzahl der in der Aktivität verfügbaren Standorte nach der Aktivierung der Aktivität geändert wurde.
