---
keywords: Automated Personalization;AP;Daten hochladen;Offline-Daten;Personalisierungsalgorithmus;Automatisches Targeting;Automatisches Targeting;Best Practices
description: Erfahren Sie, wie Sie Offline-Daten beim Erstellen von Personalisierungsmodellen in  [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] Aktivitäten hochladen.
title: Wie kann ich Daten für Personalization-Algorithmen hochladen?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 10%

---

# Hochladen von Daten für die [!DNL Target] Personalisierungsalgorithmen

Offline-Daten wie CRM-Informationen oder Tendenzwerte zur Kundenabwanderung können beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Auto-Target]-Aktivitäten unglaublich wertvoll sein.

Es gibt mehrere Möglichkeiten, Daten in [!UICONTROL Automated Personalization] (AP) einzugeben und Personalisierungsalgorithmen zu [!UICONTROL Auto-Target]. Zusätzlich zu den Methoden unter [Methoden für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank} werden auch [!DNL Experience Cloud] freigegebenen Zielgruppen ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) und Reporting-Zielgruppen während der Aktivität in [!DNL Target] Algorithmen verwendet.

Informationen zu den automatisch von [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] Personalisierungsalgorithmen erfassten und verwendeten Daten finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best Practices   {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Die folgende Liste enthält Best Practices zum Hochladen von Daten für [!DNL Target] Personalisierungsalgorithmen:

* Je höher die Qualität der Daten ist, die [!DNL Target] Personalisierungsalgorithmen zur Verfügung stehen, desto höher ist auch die Qualität der resultierenden Modelle in Ihren [!UICONTROL Automated Personalization]- und [!UICONTROL Auto-Target].
* Beschränken Sie die Verwendung mehrerer Profilskripte oder -attribute, die denselben Zweck erfüllen.
* Übergeben Sie keine eindeutige ID, z. B. keine Sitzungs-ID, wenn Sie sie nicht benötigen.
* Überprüfen Sie, welche Daten [!DNL Target] automatisch erfasst [Datenerfassung für die Personalization-Algorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md), damit Sie keine doppelten Informationen senden. [!DNL Target] verwendet beispielsweise IP-Adressen, um die Postleitzahlen der Besucher zu bestimmen. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Werte in demselben Attribut oder derselben Variablen. Wenn mehrere Variablen verkettet sind, behandeln [!DNL Target] Personalisierungsalgorithmen jede Zeichenfolge als eindeutigen Wert, wodurch der Wert der zu personalisierenden Informationen verringert wird.
* Nutzen Sie eine einprägsame und aussagekräftige Namenskonvention, um Ihre [Personalization Insights-](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) verständlicher zu machen.
