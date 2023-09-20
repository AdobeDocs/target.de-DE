---
keywords: Automated Personalization; App; Hochladen von Daten; Offline-Daten; Personalisierungsalgorithmus; automatisches Targeting; automatisches Targeting; Best Practices
description: Erfahren Sie, wie Sie beim Erstellen von Personalisierungsmodellen in Offline-Daten hochladen können [!DNL Adobe Target] [!UICONTROL Automated Personalization] AP und [!UICONTROL Automatisches Targeting] Aktivitäten.
title: Wie kann ich Daten für Personalisierungsalgorithmen hochladen?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 25%

---

# Hochladen von Daten für die [!DNL Target] Personalisierungsalgorithmen

Offline-Daten, wie z. B. CRM-Informationen oder Tendenzwerte zur Kundenabwanderung, können beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] AP und [!UICONTROL Automatisches Targeting] Aktivitäten.

Es gibt verschiedene Möglichkeiten für die Dateneingabe in die Algorithmen zur [!UICONTROL automatisierten Personalisierung] (AP) und zum [!UICONTROL automatischen Targeting. ] Zusätzlich zu den Methoden in [Verfahren für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, [!DNL Experience Cloud] freigegebene Zielgruppen ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) und aktivitätsinterne Berichterstellungszielgruppen auch in [!DNL Target] Algorithmen.

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen der [!UICONTROL automatisierten Personalisierung] und des [!UICONTROL automatischen Targetings] gesammelt und verwendet werden, finden Sie unter [Datenerfassung für die automatisierte Personalisierung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best Practices   {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Die folgende Liste enthält Best Practices für das Hochladen von Daten für [!DNL Target] Personalisierungsalgorithmen:

* Die hochwertigeren Daten, die verfügbar sind für [!DNL Target] Personalisierungsalgorithmen: Je besser die Qualität der resultierenden Modelle in Ihren [!UICONTROL Automated Personalization] und [!UICONTROL Automatisches Targeting] Aktivitäten.
* Beschränken Sie die Verwendung mehrerer Profilskripte oder -attribute, die denselben Zweck erfüllen.
* Übergeben Sie keine eindeutige ID, z. B. eine Sitzungs-ID, falls nicht erforderlich.
* Überprüfen der Daten [!DNL Target] automatisch erfasst ( [Datenerfassung für die Personalisierungsalgorithmen von Target](/help/main/c-activities/t-automated-personalization/ap-data.md)), damit Sie keine doppelten Informationen senden. Beispiel: [!DNL Target] verwendet IP-Adressen, um die Postleitzahlen der Besucher zu ermitteln. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Werte im selben Attribut oder in derselben Variablen. Wenn mehrere Variablen verkettet sind, [!DNL Target] Personalisierungsalgorithmen behandeln jede Zeichenfolge als einen eindeutigen Wert, wodurch der Wert der Personalisierungsinformationen verringert wird.
* Verwenden Sie eindeutige Namen, die leicht zu merken sind, damit Ihre  [Personalization Insights-Berichte](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) leichter verständlich sind.
