---
description: Liste der häufig gestellten Fragen zur Berichterstellung in Target
keywords: Fehlerbehebung; Metrikdiskrepanzen; häufig gestellte Fragen; Berichte
seo-description: Liste der häufig gestellten Fragen zur Berichterstellung in Target
seo-title: Häufig gestellte Fragen zum Reporting
solution: Target
title: Häufig gestellte Fragen zum Reporting
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Häufig gestellte Fragen zum Reporting{#reporting-faq}

Liste der häufig gestellten Fragen zur Berichterstellung in Target

## Warum ist die Anzahl der Besuche in Target niedriger als in anderen Experience Cloud-Lösungen? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metrikwerte, beispielsweise Besuche, die von [!DNL Target] angezeigt werden, liegen aus verschiedenen Gründen immer unter den Werten in [!DNL Experience Cloud]-Lösungen:

* [!DNL Target] zählt nur die Besuche von Besuchern, die für die Aktivität qualifiziert sind. In anderen Lösungen werden Besuche für Besucher angezeigt, die die Seite anzeigen, unabhängig davon, durch welche Aktivität sie auf die Seite gelangt sind.
* Möglicherweise verweisen mehrere Aktivitäten auf den gleichen Ort (diese Aktivitäten schließen sich gegenseitig aus). Somit werden Besuchern auf einer Webseite verschiedene Inhalte angezeigt, was sich auf die in [!DNL Target] registrierten Metrikwerte auswirkt.

## Warum stehen für meinen Aktivitätsbericht keine Daten zur Verfügung? {#section_E4722F6445884130951DF79981C8289B}

Wurde der Inhalt einer Aktivität den Benutzern erfolgreich bereitgestellt, enthält der zugehörige Bericht jedoch keine Daten, stellen Sie sicher, dass in den Berichtseinstellungen die korrekte Umgebung (Hostgruppe) ausgewählt wurde.

Sollten Sie eine Entwicklungsumgebung ausgewählt haben, wird möglicherweise folgende Fehlermeldung ausgegeben: „Es sind keine Daten für die ausgewählten Berichtseinstellungen vorhanden.“

So ändern Sie die Umgebung für einen Aktivitätsbericht:

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte Aktivität aus der Liste aus und klicken Sie auf die Registerkarte **Berichte[!UICONTROL .]**
1. Klicken Sie auf das Zahnradsymbol, um die Berichtseinstellungen zu bearbeiten.

   ![](assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >Das Zahnradsymbol steht nicht für Berichte zur automatisierten Personalisierung zur Verfügung.

1. Wählen Sie in der **[!UICONTROL Umgebung]** die Option **[!UICONTROL Produktion]** aus.

   Möglicherweise stehen Berichtsdaten bei Auswahl einer Entwicklungsumgebung nicht zur Verfügung.

1. Klicken Sie auf **[!UICONTROL Einstellungen speichern]**.

Weitere Informationen zu Umgebungen finden Sie unter [Hosts](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).
