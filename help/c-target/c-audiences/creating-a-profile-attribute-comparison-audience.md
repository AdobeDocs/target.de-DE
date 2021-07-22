---
keywords: Zielgruppe; Tendenz; Profilattribut; Vergleichen; Vergleich; Zielgruppe erstellen; Erstellen einer Zielgruppe
description: Erfahren Sie, wie Sie eine Zielgruppe definieren, um zwei Profilattribute zu vergleichen.
title: Kann ich zwei Profilattribute für die Verwendung in Zielgruppen vergleichen?
feature: Zielgruppen
exl-id: 033e90f1-5a05-4fce-a520-68826860a908
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 61%

---

# Erstellen einer Zielgruppe zum Profilattributvergleich

Definieren Sie eine Zielgruppe in [!DNL Adobe Target] , um zwei Profilattribute für Ihre [Zielgruppenbibliothek](/help/c-target/c-audiences/audiences.md) oder eine [Nur Aktivität](/help/c-target/creating-activity-only-audience.md) zu vergleichen. Definieren Sie über Operatoren wie „größer als“, „kleiner als“ oder „gleich“ eine Zielgruppe, um die Werte zweier verschiedener Profilattribute dynamisch miteinander zu vergleichen.

>[!NOTE]
>
>Diese Funktion ist nur für die Kategorie [[!UICONTROL Besucherprofil]](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E) verfügbar.

## Überblick {#section_303CBC78194D49A2A004945D425441E1}

Zielgruppen werden durch Regeln definiert, die bestimmen, wer in eine [!DNL Target]-Aktivität eingeschlossen und wer davon ausgeschlossen wird. Eine Zielgruppendefinition kann mehrere Regeln enthalten, wobei die einzelnen Regeln wiederum mehrere Parameter aufweisen können. Wenn eine der eingeschlossenen Regeln die Kategorie [!UICONTROL Besucherprofil] verwendet, können Sie eine Regel auf der Grundlage des spezifischen Werts eines Besucherprofilattributs definieren oder den Wert dieses Attributs mit einem anderen Besucherprofilattribut vergleichen.

Nehmen wir beispielsweise an, Sie arbeiten für ein Möbelunternehmen und laden zwei Tendenzwerte für Kunden in [!DNL Target] hoch:

* Wahrscheinlichkeit, in den nächsten 90 Tagen Esszimmermöbel zu kaufen
* Wahrscheinlichkeit, in den nächsten 90 Tagen Wohnzimmermöbel zu kaufen

Sie könnten eine Zielgruppe erstellen, die dadurch definiert ist, dass die Neigung zum Kauf von Esszimmermöbeln größer als die Neigung zum Kauf von Wohnzimmermöbeln ist. [!DNL Target] würde daraufhin die Propensity Scores für Ess- bzw. Wohnzimmermöbel des vorliegenden Besuchers dynamisch miteinander vergleichen, um zu bestimmen, ob der Besucher in die entsprechende Zielgruppe fällt.

Weitere Informationen finden Sie unter [Verfahren für die Datenübernahme in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17).

## Erstellen einer Zielgruppe zum Profilattributvergleich {#section_7A62FD47D5C74C3EBC3417ACDBB85013}

1. Klicken Sie auf **[!UICONTROL Zielgruppen]** > **[!UICONTROL Zielgruppe erstellen]**.
1. Benennen Sie die Zielgruppe und fügen Sie eine optionale Beschreibung hinzu.
1. Ziehen Sie **[!UICONTROL Besucherprofil]** in den Bereich Audience Builder .
1. Wählen Sie in der Dropdownliste **[!UICONTROL Besucherprofil]** ein Attribut aus:

   ![Propensity Score 1](assets/propensity_score_1.png)

1. Wählen Sie einen Auswerter aus:

   ![Propensity Score 2](assets/propensity_score_2.png)

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Vergleichstyp]** die Option **[!UICONTROL Attribut]** aus.

   Mit dem Vergleichstyp &quot;statischer Wert&quot;können Sie das Besucherprofilattribut mit bestimmten Werten vergleichen.

   ![Propensity Score 3](assets/propensity_score_3.png)

   >[!NOTE]
   >
   >Wenn Sie eine der standardmäßigen Besucherprofilkategorien verwenden (z. B. &quot;Neuer Besucher&quot;oder &quot;Wiederkehrender Besucher&quot;), können Sie nur die Option für statische Werte auswählen. Die dynamischen Vergleichsoptionen sind nur für Standardkategorien verfügbar. Andere Beispiele, in denen die dynamischen Vergleichsoptionen nicht verfügbar sind, umfassen „Erste Seite der Sitzung“, „Nicht in anderen Tests“, „Nicht die erste Seite der Sitzung“ und „Kategorieaffinität“.

1. Wählen Sie das zusätzliche Attribut aus, das Sie mit dem ursprünglichen Attribut vergleichen wollen.

   ![](assets/propensity_score_4.png)

1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Schulungsvideo ![Badge &quot;Überblick&quot;](/help/assets/overview.png) {#section_3BB8DBF3418F4520B3E274B6F40AF8F3}

Das folgende Video enthält weitere Informationen sowie ein Szenario, in dem Sie diese Funktion einsetzen könnten:

>[!VIDEO](https://video.tv.adobe.com/v/23218/)
