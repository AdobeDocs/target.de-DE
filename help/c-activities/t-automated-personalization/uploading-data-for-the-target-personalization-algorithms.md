---
description: Offline-Daten wie CRM-Informationen oder Propensity Scores zur Kundenabwanderung können beim Aufbau von Personalisierungsmodellen von unschätzbarem Wert sein.
title: Hochladen von Daten für die Target-Personalisierungsalgorithmen
feature: ap
uuid: eb0938b9-7f35-4bb5-ac4b-260b2144db5b
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 100%

---


# Hochladen von Daten für die Target-Personalisierungsalgorithmen{#upload-data-for-target-s-personalization-algorithms}

Offline-Daten wie CRM-Informationen oder Propensity Scores zur Kundenabwanderung können beim Aufbau von Personalisierungsmodellen von unschätzbarem Wert sein.

Es gibt verschiedene Möglichkeiten für die Dateneingabe in die Algorithmen zur automatisierten Personalisierung (AP) und zum automatischen Targeting. Zusätzlich zu den Methoden in  [Verfahren für die Datenübernahme in Target](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) werden gemeinsam genutzte Experience Cloud-Zielgruppen (Adobe Analytics, Audience Management) und aktivitätsinterne Berichtszielgruppen auch in unseren Algorithmen verwendet.

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen der automatisierten Personalisierung und des automatischen Targetings gesammelt und verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058).

## Best Practices {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In der folgenden Liste finden Sie Best Practices zum Hochladen von Daten für die Target-Personalisierungsalgorithmen:

* Je höher die Qualität der verfügbaren Daten in den Target-Personalisierungsalgorithmen, desto höher die Qualität der entsprechenden Modelle in Ihren AP- und AT-Aktivitäten.
* Beschränken Sie die Verwendung mehrerer Profilskripte oder -attribute, die denselben Zweck erfüllen.
* Übergeben Sie keine eindeutige ID, wie z. B. eine Sitzungs-ID, sofern nicht erforderlich.
* Überprüfen Sie, welche Daten Target automatisch erfasst (  [Datenerfassung für die Target-Personalisierungsalgorithmen](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)), damit Sie Informationen nicht doppelt senden. Target verwendet beispielsweise IP-Adressen, um die Postleitzahl der Besucher zu ermitteln. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Variablen in einem Attribut/einer Variablen. Wenn mehrere Variablen verbunden sind, behandeln die Target-Personalisierungsalgorithmen jede Zeichenfolge als eigenen Wert und reduzieren so die Informationen für die Personalisierung.
* Verwenden Sie eindeutige Namen, die leicht zu merken sind, damit Ihre  [Personalization Insights-Berichte](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) leichter verständlich sind.

