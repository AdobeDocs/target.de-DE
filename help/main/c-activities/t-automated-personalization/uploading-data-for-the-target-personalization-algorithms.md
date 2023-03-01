---
keywords: Automated Personalization; App; Hochladen von Daten; Offline-Daten; Personalisierungsalgorithmus; automatisches Targeting; automatisches Targeting; Best Practices
description: Erfahren Sie, wie Sie beim Erstellen von Personalisierungsmodellen in Adobe Offline-Daten wie CRM-Informationen hochladen können. [!DNL Target] Automated Personalization (AP)-Aktivitäten.
title: Wie kann ich Daten für Personalisierungsalgorithmen hochladen?
feature: Automated Personalization
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 67%

---

# Hochladen von Daten für die [!DNL Target] Personalisierungsalgorithmen

Offline-Daten, wie z. B. CRM-Informationen oder Tendenzwerte zur Kundenabwanderung, können beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] AP-Aktivitäten.

Es gibt verschiedene Möglichkeiten für die Dateneingabe in die Algorithmen zur [!UICONTROL automatisierten Personalisierung] (AP) und zum [!UICONTROL automatischen Targeting. ] Zusätzlich zu den Methoden in [Verfahren für die Datenübernahme in Target](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/){target=_blank}, Experience Cloud shared audiences (Adobe Analytics, Audience Management){target=_blank} und aktivitätsinterne Reporting-Zielgruppen werden auch in unseren Algorithmen verwendet.

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen der automatisierten Personalisierung und des automatischen Targetings gesammelt und verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best Practices   {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In der folgenden Liste finden Sie Best Practices zum Hochladen von Daten für die Target-Personalisierungsalgorithmen:

* Je höher die Qualität der verfügbaren Daten in den Target-Personalisierungsalgorithmen, desto höher die Qualität der entsprechenden Modelle in Ihren AP- und AT-Aktivitäten.
* Beschränken Sie die Verwendung mehrerer Profilskripte oder -attribute, die denselben Zweck erfüllen.
* Übergeben Sie keine eindeutige ID, wie z. B. eine Sitzungs-ID, sofern nicht erforderlich.
* Überprüfen Sie, welche Daten Target automatisch erfasst (  [Datenerfassung für die Target-Personalisierungsalgorithmen](/help/main/c-activities/t-automated-personalization/ap-data.md)), damit Sie Informationen nicht doppelt senden. Target verwendet beispielsweise IP-Adressen, um die Postleitzahl der Besucher zu ermitteln. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Variablen in einem Attribut/einer Variablen. Wenn mehrere Variablen verbunden sind, behandeln die Target-Personalisierungsalgorithmen jede Zeichenfolge als eigenen Wert und reduzieren so die Informationen für die Personalisierung.
* Verwenden Sie eindeutige Namen, die leicht zu merken sind, damit Ihre  [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) leichter verständlich sind.
