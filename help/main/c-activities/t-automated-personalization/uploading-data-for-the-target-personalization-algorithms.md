---
keywords: Automated Personalization; App; Hochladen von Daten; Offline-Daten; Personalisierungsalgorithmus; automatisches Targeting; automatisches Targeting; Best Practices
description: Erfahren Sie, wie Sie beim Erstellen von Personalisierungsmodellen in den Aktivitäten [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] Offline-Daten hochladen.
title: Wie kann ich Daten für Personalization-Algorithmen hochladen?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 10%

---

# Hochladen von Daten für die [!DNL Target]-Personalisierungsalgorithmen

Offline-Daten wie CRM-Informationen oder Tendenzwerte zur Kundenabwanderung können beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Auto-Target]-Aktivitäten von unschätzbarem Wert sein.

Es gibt mehrere Möglichkeiten, Daten in die Personalisierungsalgorithmen [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Auto-Target] einzugeben. Zusätzlich zu den Methoden unter [Methoden für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank}, [!DNL Experience Cloud] freigegebene Zielgruppen ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) und In-Aktivität-Berichterstellungszielgruppen werden auch in [!DNL Target]-Algorithmen verwendet.

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen [!UICONTROL Automated Personalization] und [!UICONTROL Auto-Target] erfasst und verwendet werden, finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best Practices   {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Die folgende Liste enthält Best Practices für das Hochladen von Daten für [!DNL Target] Personalisierungsalgorithmen:

* Je höher die Qualität der für [!DNL Target] -Personalisierungsalgorithmen verfügbaren Daten ist, desto höher ist die Qualität der resultierenden Modelle in Ihren [!UICONTROL Automated Personalization] - und [!UICONTROL Auto-Target] -Aktivitäten.
* Beschränken Sie die Verwendung mehrerer Profilskripte oder -attribute, die denselben Zweck erfüllen.
* Übergeben Sie keine eindeutige ID, z. B. eine Sitzungs-ID, falls nicht erforderlich.
* Überprüfen Sie, welche Daten [!DNL Target] automatisch erfasst ( [Datenerfassung für die Personalization-Algorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md)), damit Sie keine doppelten Informationen senden. Beispiel: [!DNL Target] verwendet IP-Adressen, um die Postleitzahlen der Besucher zu ermitteln. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Werte im selben Attribut oder in derselben Variablen. Wenn mehrere Variablen verkettet sind, behandeln die [!DNL Target] -Personalisierungsalgorithmen jede Zeichenfolge als einen eindeutigen Wert, wodurch der Wert der Informationen für die Personalisierung verringert wird.
* Verwenden Sie eine unvergessliche und aussagekräftige Namenskonvention, um Ihre [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) verständlicher zu machen.
