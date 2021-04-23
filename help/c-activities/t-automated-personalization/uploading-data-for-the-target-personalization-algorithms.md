---
keywords: Automated Personalization;App;Hochladen von Daten;Offlinedaten;Personalisierungsalgorithmus;automatische Zielgruppe;automatische Zielgruppe;Best Practices
description: Erfahren Sie, wie Sie Offline-Daten wie CRM-Informationen hochladen, wenn Sie Personalisierungsmodelle in Adobe [!DNL Target] Automated Personalization (AP)-Aktivitäten erstellen.
title: Wie kann ich Daten für Personalisierungsalgorithmen hochladen?
feature: Automatisierte Personalisierung
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 75%

---

# Hochladen von Daten für die Personalisierungsalgorithmen [!DNL Target]

Offline-Daten, wie z. B. CRM-Informationen oder Kundenstamm-Tendenzwerte, können beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization]- (AP)-Aktivitäten unglaublich wertvoll sein.

Es gibt verschiedene Möglichkeiten für die Dateneingabe in die Algorithmen zur [!UICONTROL automatisierten Personalisierung] (AP) und zum [!UICONTROL automatischen Targeting. ] Zusätzlich zu den Methoden in  [Verfahren für die Datenübernahme in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) werden gemeinsam genutzte Experience Cloud-Zielgruppen (Adobe Analytics, Audience Management) und aktivitätsinterne Berichtszielgruppen auch in unseren Algorithmen verwendet.

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen der automatisierten Personalisierung und des automatischen Targetings gesammelt und verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/c-activities/t-automated-personalization/ap-data.md).

## Best Practices {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In der folgenden Liste finden Sie Best Practices zum Hochladen von Daten für die Target-Personalisierungsalgorithmen:

* Je höher die Qualität der verfügbaren Daten in den Target-Personalisierungsalgorithmen, desto höher die Qualität der entsprechenden Modelle in Ihren AP- und AT-Aktivitäten.
* Beschränken Sie die Verwendung mehrerer Profilskripte oder -attribute, die denselben Zweck erfüllen.
* Übergeben Sie keine eindeutige ID, wie z. B. eine Sitzungs-ID, sofern nicht erforderlich.
* Überprüfen Sie, welche Daten Target automatisch erfasst (  [Datenerfassung für die Target-Personalisierungsalgorithmen](/help/c-activities/t-automated-personalization/ap-data.md)), damit Sie Informationen nicht doppelt senden. Target verwendet beispielsweise IP-Adressen, um die Postleitzahl der Besucher zu ermitteln. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Variablen in einem Attribut/einer Variablen. Wenn mehrere Variablen verbunden sind, behandeln die Target-Personalisierungsalgorithmen jede Zeichenfolge als eigenen Wert und reduzieren so die Informationen für die Personalisierung.
* Verwenden Sie eindeutige Namen, die leicht zu merken sind, damit Ihre  [Personalization Insights-Berichte](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) leichter verständlich sind.
