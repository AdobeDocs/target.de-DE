---
description: Liste der häufig gestellten Fragen zur Berichterstellung in Target
keywords: Fehlerbehebung; Metrikdiskrepanzen; häufig gestellte Fragen; Berichte
seo-description: Liste der häufig gestellten Fragen zur Berichterstellung in Adobe Target.
seo-title: Häufig gestellte Fragen zur Berichterstellung für Adobe Target
solution: Target
title: Häufig gestellte Fragen zum Reporting
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: a6f2eceaddf67653b36a1687ba071f7226169516

---


# Häufig gestellte Fragen zum Reporting{#reporting-faq}

Liste der häufig gestellten Fragen zur Berichterstellung in [!DNL Target].

## Why do my [!UICONTROL Experience Targeting] (XT) reports contain metrics for control experiences?

XT-Aktivitäten sollten immer ein Kontrollerlebnis haben. If you are using an XT activity in a similar manner to an [!UICONTROL A/B Test] activity, which is a fairly common scenario, the control experience data is useful. Sie können die Kontrollerlebnisdaten ignorieren, wenn sie in Ihren Berichten nicht nützlich sind.

## Why are the number of visits lower in [!DNL Target] than in other [!DNL Adobe Experience Cloud] solutions? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metrikwerte, beispielsweise Besuche, die von [!DNL Target] angezeigt werden, liegen aus verschiedenen Gründen immer unter den Werten in [!DNL Experience Cloud]-Lösungen:

* [!DNL Target] zählt nur die Besuche von Besuchern, die für die Aktivität qualifiziert sind. In anderen Lösungen werden Besuche für Besucher angezeigt, die die Seite anzeigen, unabhängig davon, durch welche Aktivität sie auf die Seite gelangt sind.
* Es kann Situationen geben, in denen verschiedene Aktivitäten miteinander konkurrieren (sich gegenseitig ausschließen). Somit werden Besuchern auf einer Webseite verschiedene Inhalte angezeigt, was sich auf die in [!DNL Target] registrierten Metrikwerte auswirkt.

## Warum stehen für meinen Aktivitätsbericht keine Daten zur Verfügung? {#section_E4722F6445884130951DF79981C8289B}

If an activity's content was successfully delivered to users but its report contains no data, ensure that you have the correct environment ([host group](/help/administrating-target/hosts.md)) selected in the report's settings.

Sollten Sie eine Entwicklungsumgebung ausgewählt haben, wird möglicherweise folgende Fehlermeldung ausgegeben: „Es sind keine Daten für die ausgewählten Berichtseinstellungen vorhanden.“

So ändern Sie die Umgebung für einen Aktivitätsbericht:

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte Aktivität aus der Liste aus und klicken Sie auf die Registerkarte **Berichte[!UICONTROL .]**
1. Klicken Sie auf das Zahnradsymbol, um die Berichtseinstellungen zu bearbeiten.

   ![A/B-Einstellungen, Dialogfeld](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >The gear icon is not available for [!UICONTROL Automated Personalization] (AP) reports.

1. Wählen Sie in der **[!UICONTROL Umgebung]** die Option **[!UICONTROL Produktion]** aus.

   Möglicherweise stehen Berichtsdaten bei Auswahl einer Entwicklungsumgebung nicht zur Verfügung.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Weitere Informationen zu Umgebungen finden Sie unter [Hosts](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).
