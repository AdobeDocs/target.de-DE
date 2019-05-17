---
description: Für Benutzer der automatisierten Personalisierung stehen spezialisierte Berichte zur Verfügung.
keywords: Targeting; AP-Berichte; Automatisierte Personalisierung-Berichte; Aktivitätsstufenbericht; Angebotsebenenbericht; Angebotsdetailbericht
seo-description: Für Benutzer der automatisierten Personalisierung stehen spezialisierte Berichte zur Verfügung.
seo-title: Automated Personalization-Zusammenfassungsberichte
solution: Target
title: Automated Personalization-Zusammenfassungsberichte
title-outputclass: premium
uuid: 959b6814-9686-4741-8a79-5957e64f6209
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Berichte zur automatisierten Personalisierung{#automated-personalization-summary-reports}

Für Benutzer der automatisierten Personalisierung stehen spezialisierte Berichte zur Verfügung.

>[!NOTE]
>
>Automatisierte Personalisierung ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Sie wird bei [!DNL Target Standard] ohne [!DNL Target Premium]-Lizenz ausgeschlossen.

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte [!UICONTROL automatisierte Personalisierung] aus der Liste aus und klicken Sie auf die Registerkarte **Berichte[!UICONTROL .]**

   Wenn Sie viele Aktivitäten haben, können Sie die Liste filtern, indem Sie [!UICONTROL Automatisierte Personalisierung] in der Dropdownliste [!UICONTROL Typ] auswählen.

1. (Optional) Klicken Sie auf das Symbol zum [!UICONTROL Herunterladen], um die Zusammenfassungsansicht herunterzuladen (etwa zum Vergleichen von Kontroll- und Targeting-Traffic), aufgeschlüsselt nach allen verfügbaren Erfolgsmetriken.

>[!NOTE]
>
>Das [!UICONTROL Einstellungssymbol] steht nicht für Berichte für [!UICONTROL Automatisierte Personalisierung] zur Verfügung.

[!UICONTROL Automatisierte Personalisierung] liefert die folgenden Berichte:

## Aktivitätsstufenbericht   {#section_6F72FC5C790B4492B3DCECBFFA971337}

Der Bericht [!UICONTROL Aktivitätsebene] vergleicht die Gesamtleistung beim Einsatz eines „[!UICONTROL Automatisierte Personalisierung]“-Algorithmus mit zufällig bereitgestellten Inhalten (Kontrolle).

![](assets/box_plot_ap.jpg)

Die Standardregeln für die Auswertung von A/B-Testergebnissen gelten weiterhin, einschließlich Steigerung, Konfidenz, Trends, Dauer und so weiter. Weitere Informationen zur Ergebnisauswertung finden Sie in   [Über die Konversionsrate](../c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844)

## Angebotsstufenbericht {#section_CAA6409879E349C6906E2BE8156D87A1}

Der Bericht [!UICONTROL Angebotsebene] für das „Random Forest“-Erlebnis vergleicht die Leistung der einzelnen durch Algorithmen bereitgestellten Angebote mit demselben, zufällig bereitgestellten Angebot (Kontrolle). Aus diesem Grund sollten Angebote in dieser Ansicht nicht miteinander verglichen werden. Im Beispiel unten ist ersichtlich, dass Angebot D eine Steigerung von 12,43 % verzeichnet, wenn es gemäß der Logik des Algorithmus (Random Forest) und nicht zufällig (Kontrolle) bereitgestellt wird.

Klicken Sie auf den Erlebnisalgorithmus (Random Forest oder Kontrolle), um den Bericht „Angebotsebene“ aufzurufen.

![](assets/ap_OfferLevelRpt.png)

Angebote können innerhalb von Berichtsgruppen angezeigt werden. Diese Berichtsgruppen können minimiert und maximiert werden. Wählen Sie in der Dropdownliste [!UICONTROL Berichterstellungsgruppe] aus, um sich Details nach Berichtsgruppen und nicht nach Angeboten anzeigen zu lassen.

>[!NOTE]
>
>Das Uhrsymbol zeigt an, dass das Algorithmusmodell noch erstellt wird. Das Häkchen zeigt an, dass der Basisalgorithmus eingerichtet wurde.

