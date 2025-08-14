---
keywords: Deduplizierung;Duplikate zulassen;doppelte Angebote ausschließen;Automated Personalization;doppelte Angebote nicht zulassen;ausschließen;Standardinhalt;
description: Verwalten von Ausschlüssen in [!UICONTROL Automated Personalization] (AP)-Aktivitäten.
title: Wie verwalte ich Ausschlüsse in [!UICONTROL Automated Personalization] Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: c5016d212edafa908b8755044e73d28167e20e8a
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 37%

---

# Verwalten von Ausschlüssen

Verwalten Sie Ausschlüsse, indem Sie doppelte Angebote ausschließen, bestimmte Erlebnisse ausschließen und Standardinhalte in [!UICONTROL Automated Personalization] (AP)-Aktivitäten in [!DNL Adobe Target] ausschließen.

## Doppelte Angebote ausschließen {#concept_4EF78013F80E48EFA024AE0274C9F037}

Verhindern Sie, dass Angebote aus der Angebotsbibliothek dupliziert werden, wenn sie an verschiedenen Stellen in [!UICONTROL Automated Personalization] Aktivitäten verwendet werden.

Möglicherweise verfügen Sie über eine Aktivität mit sechs Orten auf einer Seite mit 12 Angeboten. Hier besteht die Gefahr, dass das gleiche Angebot in einer Aktivität mehrmals angezeigt wird. Dadurch wird verhindert, dass doppelte Angebote gleichzeitig an unterschiedlichen Positionen in derselben Aktivität angezeigt werden.

Klicken Sie auf das **[!UICONTROL Configure]** > **[!UICONTROL Duplicate Offers]** und dann auf **[!UICONTROL Allow Duplicates]** oder **[!UICONTROL Disallow Duplicates]**.

![Optionen für doppelte Angebote](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Ausschließen spezifischer Erlebnisse {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Schließen Sie bestimmte Erlebnisse aus, wenn Sie bestimmte Angebotskombinationen aus Ihrer [!UICONTROL Automated Personalization] ausschließen möchten.

Möglicherweise gibt es bestimmte Kombinationen, die nicht zusammenarbeiten, oder Sie beschränken die Anzahl der getesteten Erlebnisse, um die Traffic-Anforderungen für Ihre Aktivität zu senken.

1. Klicken Sie [beim Erstellen oder Bearbeiten einer AP-Aktivität in der Header-Leiste ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)auf **Inhalt verwalten**.

   ![Option „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Die [!UICONTROL Experiences] Liste zeigt jedes Erlebnis, das aus den Permutationen aller Inhalts- und Standortoptionen generiert wurde.

1. Sie können Erlebnisse nach Bedarf ausschließen.

   Sie können spezifische Erlebnisse ausschließen, indem Sie den Mauszeiger über das gewünschte Erlebnis bewegen und dann auf das Ausschlusssymbol klicken.

   ![Ausschluss eines Erlebnisses mit dem Mauszeiger](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Alternativ können Sie Erlebnisse im Batch-Modus ausschließen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann auf das **[!UICONTROL Exclude]** oben rechts im Dialogfeld klicken. Das [!UICONTROL Exclude] wird angezeigt, wenn mindestens ein Erlebnis aktiviert ist.

   ![Erlebnisse im Batch-Modus ausschließen](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden, indem Sie auf die Dropdown-Liste [!UICONTROL Status] klicken.

   Die Erlebnisse sind jetzt von der Aktivität ausgeschlossen und ihre [!UICONTROL Status] werden als [!UICONTROL Excluded] angezeigt.

   ![Ausgeschlossene Erlebnisse](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Standardinhalt ausschließen {#task_DCB4528989DF4C05A3A4729E5891D18F}

Manchmal ist es sinnvoll, Standardinhalte nicht in die [!UICONTROL Automated Personalization] einzubeziehen. Wie Sie auf diese Einstellung zugreifen, unterscheidet sich vom Erstellen von Ausschlussgruppen. Sie können diese Methode verwenden, um nur über ein Angebot (unterscheidet sich von Ihrem Standardinhalt) an einer Position als Teil Ihrer AP-Aktivität zu verfügen.

Das Ausschließen von Standardinhalt ist eine sehr gute Möglichkeit, um das Erscheinungsbild der restlichen Seite zu ändern, um die von Ihnen mit der AP-Aktivität getesteten Angebote anzupassen. Wenn Sie beispielsweise die Farbpalette der von Ihnen getesteten Angebote abgleichen möchten, können Sie die Hintergrundfarbe Ihrer Seite ändern und die standardmäßige Hintergrundfarbe ausschließen.

**So schließen Sie Standardinhalte mithilfe des [!UICONTROL Visual Experience Composer] (VEC) aus:**

1. Wählen [ beim Erstellen oder Bearbeiten einer AP](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)Aktivität den zu ersetzenden Inhalt aus und klicken Sie, um auf **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]** oder **[!UICONTROL Change Background Color]** zuzugreifen.
1. Erstellen Sie im Dialogfeld einen neuen Inhalt und deaktivieren Sie **Einschließen** rechts neben dem Standardinhalt (oder deaktivieren Sie die Option Standardbild/Standardvideo auf dem [!UICONTROL Select Content]).

   Je nach Inhalts- oder Angebotstyp befindet sich das Kontrollkästchen [!UICONTROL Include] an einer etwas anderen Stelle.

   Für Text-/HTML-Inhalt:

   ![Kontrollkästchen „Einbeziehen“ im Dialogfeld „Text/HTML bearbeiten“](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Für Bild-/Videoinhalt:

   ![Kontrollkästchen „Einbeziehen“ im Dialogfeld „Inhalt auswählen“](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Für die Hintergrundfarbe:

   ![Kontrollkästchen „Einbeziehen“ im Dialogfeld „Hintergrundfarbe bearbeiten“](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klicken Sie auf **[!UICONTROL Save]**.

   Sie können die Erlebnisse sehen, die aus den Angeboten erstellt wurden, die Sie unter [!UICONTROL Manage Content] angegeben haben. Sie werden feststellen, dass in [!UICONTROL Manage Content] keine Erlebnisse mit dem von Ihnen ausgeschlossenen Standardangebot erstellt werden.

   ![exclude_content_vec_4 Bild](assets/exclude_content_vec_4.png)

**So schließen Sie Standardinhalte mithilfe der [!UICONTROL Form-Based Experience Composer] aus:**

1. Klicken Sie beim Erstellen oder Bearbeiten einer AP-Aktivität unter **[!UICONTROL Change Text/HTML]** auf **[!UICONTROL Change Image Offer]** oder **[!UICONTROL Content]** .
1. Erstellen Sie im Dialogfeld einen neuen Inhalt und deaktivieren Sie **[!UICONTROL Include]** rechts neben dem Standardinhalt (oder deaktivieren Sie die Option Standardbild/Standardvideo auf dem [!UICONTROL Select Content]).

   Je nach Inhalts- oder Angebotstyp befindet sich das Kontrollkästchen [!UICONTROL Include] an einer etwas anderen Stelle.

   Für Text-/HTML-Inhalt:

   ![exclude_content_form_1 Bild](assets/exclude_content_form_1.png)

   Für Bild-/Videoinhalt:

   ![exclude_content_form_2 Bild](assets/exclude_content_form_2.png)

1. Klicken Sie auf **[!UICONTROL Save]**.

   Sie können die Erlebnisse sehen, die aus den Angeboten erstellt wurden, die Sie unter [!UICONTROL Manage Content] angegeben haben. Sie werden feststellen, dass in [!UICONTROL Manage Content] keine Erlebnisse mit dem von Ihnen ausgeschlossenen Standardangebot erstellt werden.

   ![exclude_content_form_3 Bild](assets/exclude_content_form_3.png)
