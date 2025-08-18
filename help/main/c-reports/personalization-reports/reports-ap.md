---
keywords: Zielgruppenbestimmung;AP-Berichte;Automated Personalization-Berichte;Bericht auf Aktivitätsebene;Bericht auf Angebotsebene;Bericht mit Angebotsdetails;FAQ
description: Erfahren Sie, wie der Automated Personalization-Zusammenfassungsbericht in Adobe Target interpretiert wird. Von diesem Bericht aus können Sie zu den Berichten Automatisierte Segmente und Wichtige Attribute wechseln.
title: Wie verwende ich die Automated Personalization-Zusammenfassungsberichte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 11%

---

# Automated Personalization-Zusammenfassungsberichte

Für Benutzer [!UICONTROL Automated Personalization] Aktivitäten in [!DNL Adobe Target] stehen spezielle Zusammenfassungsberichte zur Verfügung.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Es ist nicht in [!DNL Target Standard] ohne [Target Premium-Lizenz enthalten](/help/main/c-intro/intro.md#premium).

1. Klicken Sie auf **[!UICONTROL Activities]**, dann in der Liste auf die gewünschte [!UICONTROL Automated Personalization] und anschließend auf die Registerkarte **[!UICONTROL Reports]** .

   Wenn Sie viele Aktivitäten haben, klicken Sie auf das Symbol Filtern ![Filtersymbol](/help/main/assets/icons/Filter.svg) ), um die Liste zu filtern, indem Sie Optionen aus den Dropdown-Listen [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] und [!UICONTROL Activity Source] auswählen.

1. (Optional) Klicken Sie auf das **[!UICONTROL Download]** ( ![Download-Symbol](/help/main/assets/icons/Download.svg) ), um die Zusammenfassungsansicht herunterzuladen (z. B. Vergleich von Kontroll- und Zieldatenverkehr), aufgeschlüsselt nach allen verfügbaren Erfolgsmetriken.

[!UICONTROL Automated Personalization] bietet die folgenden Berichte:

* Aktivitätsebene
* Angebotsebene
* Automatisierte Segmente
* Wichtige Attribute

## Aktivitätsstufenbericht {#section_6F72FC5C790B4492B3DCECBFFA971337}

Der [!UICONTROL Activity Level] vergleicht die Gesamtleistung der Verwendung eines [!UICONTROL Automated Personalization] Algorithmus mit zufällig bereitgestellten Inhalten (Kontrolle).

Die Standardregeln für die Auswertung von A/B-Testergebnissen gelten weiterhin, einschließlich Steigerung, Konfidenz, Trends, Dauer und so weiter. Weitere Informationen zur Interpretation der Ergebnisse finden Sie unter [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## Angebotsstufenbericht {#section_CAA6409879E349C6906E2BE8156D87A1}

Der [!UICONTROL Offer Level] für das Erlebnis „Zufällige Gesamtstruktur“ vergleicht die Leistung der einzelnen auf einen Algorithmus angewendeten Angebote mit demselben zufällig bereitgestellten Angebot (Kontrolle). Aus diesem Grund sollten Angebote in dieser Ansicht nicht miteinander verglichen werden.

Klicken Sie auf den Erlebnisalgorithmus (zufällige Gesamtstruktur oder Kontrolle), um den [!UICONTROL Offer Level] anzuzeigen.

>[!NOTE]
>
>Ein Uhrensymbol zeigt an, dass das Algorithmusmodell noch im Aufbau begriffen ist. Ein Häkchensymbol zeigt an, dass der Basisalgorithmus eingerichtet wurde.

Angebote können in [Berichtsgruppen“ angezeigt ](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md). Diese Berichtsgruppen können reduziert und erweitert werden. Klicken Sie auf **[!UICONTROL Control]** oder **[!UICONTROL Targeted]** in der Tabelle, um aggregierte Informationen nach Berichtsgruppen und nicht nach Angeboten anzuzeigen.

## Automatisierte Segmente

Klicken Sie auf das Symbol [!UICONTROL Automated Segments] . Dieser Bericht zeigt, wie verschiedene Besucher unterschiedlich auf die Angebote/Erlebnisse in Ihrer AP/AT-Aktivität reagieren. Dieser Bericht zeigt, wie unterschiedliche automatisierte Segmente, die von den Target-Personalisierungsmodellen definiert werden, auf die Angebote/Erlebnisse in der Aktivität reagiert haben.

Weitere Informationen finden Sie unter [Bericht zu automatisierten Segmenten](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## Wichtige Attribute

Klicken Sie auf das Symbol [!UICONTROL Important Attributes] . Dieser Bericht zeigt, wie in verschiedenen Aktivitäten verschiedene Attribute für die Personalisierungsentscheidung des Modells mehr (oder weniger) wichtig sind. Dieser Bericht stellt die wichtigsten Attribute, die das Modell beeinflusst haben, und ihre relative Bedeutung dar.

Weitere Informationen finden Sie unter [Bericht zu wichtigen Attributen](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Häufig gestellte Fragen  

### Warum unterscheiden sich die Daten zwischen den Berichten Aktivitätsebene und Angebotsebene?

**[!UICONTROL Activity Level]Bericht**: Besuche, die im [!UICONTROL Activity Level] Bericht aufgezeichnet werden, erfassen die Anzahl der Besuche des Kontrollerlebnisses/der Kontrollerlebnisse im Vergleich zum „zielgerichteten“ Traffic. Der zielgerichtete Traffic umfasst eine Mischung aus Exploration-Traffic und personalisiertem Traffic.

**Bericht auf Angebotsebene**: Die im [!UICONTROL Offer Level] Bericht erfassten Impressionen erfassen die Anzahl der Impressionen für jedes Angebot. Daher entspricht in einer Aktivität mit mehr als einem Standort die Gesamtzahl der im [!UICONTROL Offer Level]-Bericht erfassten Besuche für alle Berichtsgruppen dem Vielfachen der Anzahl der im [!UICONTROL Activity Level]-Bericht für Kontroll- oder Zieldatenverkehr erfassten Besuche multipliziert mit der Gesamtzahl der Standorte in der Aktivität. Impressionen von Standardinhalten, die an Orten auftreten, an denen Standardinhalte als verfügbare Option verfügbar waren, werden in der Angebotsgruppe „Standardinhalt“ aufgezeichnet. Impressionen von Angeboten, deren Zuweisung zu einer Berichtsgruppe aufgehoben wurde, werden in der Angebotsgruppe „Ungruppiert“ erfasst.

>[!NOTE]
>
>Die Anzahl der im [!UICONTROL Offer Level] Bericht aufgezeichneten Impressionen ist möglicherweise kein exaktes ganzzahliges Vielfaches der Anzahl der im [!UICONTROL Activity Level] Bericht aufgezeichneten Besuche. Dies liegt an geringfügigen Abweichungen, die bei der Erfassung des Berichtsdatenverkehrs über das Internet auftreten (die typische Diskrepanzrate liegt unter 5 %). Daher ist die Anzahl der Impressionen kein exaktes Vielfaches, wenn die Anzahl der in der Aktivität verfügbaren Standorte nach der Aktivierung der Aktivität geändert wurde.
