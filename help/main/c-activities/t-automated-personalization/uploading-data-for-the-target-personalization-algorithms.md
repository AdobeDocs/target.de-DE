---
keywords: Automated Personalization;AP;Daten hochladen;Offline-Daten;Personalisierungsalgorithmus;Automatisches Targeting;Automatisches Targeting;Best Practices
description: Erfahren Sie, wie Sie Offline-Daten beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Automatisches Targeting]-Aktivitäten hochladen.
title: Wie kann ich Daten für Personalization-Algorithmen hochladen?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
TQID: 'https://experienceleague.adobe.com/B1vwWrii4DfQzXftwcmgzbhBkDAZFo5mDRn3a7dULj0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 7%
---
# Hochladen von Daten für die [!DNL Target] Personalisierungsalgorithmen {#upload-data-personalization}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Offline- und benutzerdefinierte Daten an die Algorithmen **[!UICONTROL Automated Personalization]** und **[!UICONTROL Automatisches Targeting]** senden und welche Best Practices Sie befolgen sollten.

>[!ENDSHADEBOX]

Offline-Daten wie CRM-Informationen oder Tendenzwerte zur Kundenabwanderung können beim Erstellen von Personalisierungsmodellen in [!DNL Adobe Target] **[!UICONTROL Automated Personalization]** (AP)- und **[!UICONTROL Automatisches Targeting]**-Aktivitäten von unschätzbarem Wert sein.

Es gibt mehrere Möglichkeiten, Daten in die Personalisierungsalgorithmen **[!UICONTROL Automated Personalization]** (AP) und **[!UICONTROL Automatisches Targeting]** einzugeben. Zusätzlich zu den Methoden unter [Methoden für die Datenübernahme in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=de){target=_blank} werden in den [!DNL Target] auch [!DNL Experience Cloud] freigegebene Zielgruppen (**[!UICONTROL Adobe Analytics]**, [!DNL Audience Manager]) und Reporting-Zielgruppen während der Aktivität verwendet.

Informationen zu den Daten, die automatisch von den Personalisierungsalgorithmen **[!UICONTROL Automated Personalization]** und **[!UICONTROL Automatisches Targeting]** erfasst und verwendet werden, finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Best Practices {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

Befolgen Sie diese Best Practices, wenn Sie Daten für die [!DNL Target] Personalisierungsalgorithmen hochladen:

* Je höher die Qualität der Daten ist, die den [!DNL Target] Personalisierungsalgorithmen zur Verfügung stehen, desto höher ist auch die Qualität der resultierenden Modelle in Ihren **[!UICONTROL Aktivitäten vom Typ]** und **[!UICONTROL Automatisches Targeting]**.
* Beschränken Sie die Verwendung mehrerer Profilskripte oder Attribute, die demselben Zweck dienen.
* Übergeben Sie keine eindeutige ID, wie z. B. eine Sitzungs-ID, wenn sie nicht benötigt wird.
* Überprüfen Sie, welche Daten [!DNL Target] automatisch erfasst ([Datenerfassung für Target Personalization-](/help/main/c-activities/t-automated-personalization/ap-data.md)), damit Sie keine doppelten Informationen senden. [!DNL Target] verwendet beispielsweise IP-Adressen, um die Postleitzahlen von Besuchern zu bestimmen. Es ist also nicht erforderlich, diese Information als separate Variable zu übergeben.
* Übergeben Sie nicht mehrere Werte in demselben Attribut oder derselben Variablen. Wenn mehrere Variablen verkettet sind, behandeln die [!DNL Target] Personalisierungsalgorithmen jede Zeichenfolge als eindeutigen Wert, wodurch der Wert der Informationen für die Personalisierung reduziert wird.
* Nutzen Sie eine einprägsame und aussagekräftige Namenskonvention, um Ihre [Personalization Insights-](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md) verständlicher zu machen.
