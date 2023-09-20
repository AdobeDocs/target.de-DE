---
keywords: deduplizieren;Duplikate zulassen;duplizierte Angebote ausschließen;automatisierte Personalisierung;duplizierte Angebote deaktivieren;ausschließen;Standardinhalt;Ausschlussgruppe
description: Verwalten von Ausschlüssen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] AP-Aktivitäten. Erstellen Sie Ausschlussgruppen und schließen Sie doppelte Angebote, spezifische Erlebnisse und Standardinhalte aus.
title: Verwalten von Ausschlüssen in [!UICONTROL Automated Personalization] Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: b5f06878a6ca8b4c571bfe05a52bfb3f471a697e
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 58%

---

# Verwalten von Ausschlüssen

Verwalten von Ausschlüssen durch Erstellen von Ausschlussgruppen, Ausschließen doppelter Angebote, Ausschließen bestimmter Erlebnisse und Ausschließen von Standardinhalten in [!UICONTROL Automated Personalization] AP-Aktivitäten in [!DNL Adobe Target].

## Erstellen von Ausschlussgruppen {#task_AAAA6C7239A84F7696C8492F04B575A2}

Erstellen von Ausschlussgruppen in [!UICONTROL Automated Personalization] (AP)-Aktivitäten, um sicherzustellen, dass Erlebnisse mit den vorgesehenen Angeboten automatisch ausgeschlossen werden.

Ausschlussgruppen eignen sich hervorragend, um sicherzustellen, dass nicht kompatible Angebote nicht an verschiedenen Stellen in demselben Erlebnis dargestellt werden. Angenommen, Sie haben zwei Angebote: eines für einen Rabatt von 20 % für alle Waren und das andere für einen Rabatt von 15 %. Sie möchten nie, dass diese beiden Angebote Besuchern im selben Erlebnis präsentiert werden. Wenn Sie diese beiden Angebote zu einer Ausschlussgruppe hinzufügen, können Sie sicherstellen, dass dies nie der Fall ist.

Sie können auch einschränken, welche Zielgruppen bestimmte Angebote in den AP-Aktivitäten sehen können. Weitere Informationen finden Sie unter [Targeting von Automated Personalization-Angeboten](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

**So erstellen Sie eine Ausschlussgruppe:**

1. Klicken Sie [beim Erstellen oder Bearbeiten einer AP-Aktivität in der Header-Leiste ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)auf **[!UICONTROL Inhalt verwalten]**.

   ![Option „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

1. Im [!UICONTROL Inhalt verwalten] Dialogfeld, klicken Sie auf **[!UICONTROL Ausschlussgruppen]**.

   ![Inhalt verwalten > Dialogfeld „Ausschlussgruppen“](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Wenn Sie zuvor Ausschlussgruppen erstellt haben, werden sie in der Liste angezeigt. Wenn Sie noch keine Ausschlussgruppe erstellt haben, werden Sie aufgefordert, eine zu erstellen.

1. Klicken Sie auf **[!UICONTROL Ausschlussgruppe erstellen]**.

   ![Dialogfeld „Ausschlussgruppe erstellen“](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Erforderlich) Geben Sie einen beschreibenden Namen für die Ausschlussgruppe an.

   Ein beschreibender Name hilft Ihnen oder anderen Benutzern, schnell eine Gruppe zu finden und ihren Zweck zu verstehen.

1. Suchen Sie die gewünschten Angebote, die Sie der Ausschlussgruppe hinzufügen möchten, und wählen Sie sie aus.

   Sie können mehrere Angebote vom selben Standort in einer Ausschlussgruppe auswählen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Die Angebote in der Ausschlussgruppe werden in Zukunft automatisch aus denselben Erlebnissen ausgeschlossen.

## Ausschluss doppelter Angebote {#concept_4EF78013F80E48EFA024AE0274C9F037}

Verhindern Sie die Duplizierung von Angeboten aus der Bibliothek, wenn diese bei [!UICONTROL automatischer Personalisierung] an verschiedenen Orten eingesetzt werden.

Möglicherweise verfügen Sie über eine Aktivität mit sechs Orten auf einer Seite mit 12 Angeboten. Hier besteht die Gefahr, dass das gleiche Angebot in einer Aktivität mehrmals angezeigt wird. Dadurch wird verhindert, dass doppelte Angebote gleichzeitig an unterschiedlichen Positionen in derselben Aktivität angezeigt werden.

Klicken Sie auf **[!UICONTROL Konfigurieren]** Zahnradoption > **[!UICONTROL Angebote duplizieren]** Klicken Sie auf **[!UICONTROL Duplikate zulassen]** oder **[!UICONTROL Duplikate nicht zulassen]**.

![Optionen für doppelte Angebote](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Ausschluss bestimmter Erlebnisse {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Schließen Sie bestimmte Erlebnisse aus, wenn Sie bestimmte Angebotskombinationen aus Ihrer [!UICONTROL Automated Personalization] -Aktivität.

Es kann bestimmte Kombinationen geben, die nicht zusammenarbeiten, oder Sie können die Anzahl der getesteten Erlebnisse einschränken, um die Traffic-Anforderungen für Ihre Aktivität zu reduzieren.

1. Klicken Sie [beim Erstellen oder Bearbeiten einer AP-Aktivität in der Header-Leiste ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)auf **Inhalt verwalten**.

   ![Option „Inhalt verwalten“](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Die Liste [!UICONTROL Erlebnisse] zeigt jedes Erlebnis an, das anhand der Permutationen sämtlicher Inhalts- und Positionsoptionen generiert wurde.

1. Sie können Erlebnisse nach Bedarf ausschließen.

   Sie können spezifische Erlebnisse ausschließen, indem Sie den Mauszeiger über das gewünschte Erlebnis bewegen und dann auf das Ausschlusssymbol klicken.

   ![Ausschluss eines Erlebnisses mit dem Mauszeiger](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Alternativ können Sie Erlebnisse in einem Batch-Vorgang ausschließen, indem Sie das Kontrollkästchen für die entsprechenden Erlebnisse aktivieren und dann auf die **[!UICONTROL Ausschließen]** in der oberen rechten Ecke des Dialogfelds. Die [!UICONTROL Ausschließen] wird angezeigt, wenn mindestens ein Erlebnis aktiviert ist.

   ![Erlebnisse im Batch-Modus ausschließen](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden. Klicken Sie dazu auf die Dropdownliste [!UICONTROL Status].

   Die Erlebnisse werden jetzt aus der Aktivität ausgeschlossen und ihre [!UICONTROL Status] anzeigen als [!UICONTROL Ausgeschlossen].

   ![Ausgeschlossene Erlebnisse](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Ausschluss von Standardinhalten {#task_DCB4528989DF4C05A3A4729E5891D18F}

Manchmal möchten Sie Ihren Standardinhalt möglicherweise nicht in Ihre [!UICONTROL Automated Personalization] -Aktivität. Wie Sie auf diese Einstellung zugreifen, unterscheidet sich vom Erstellen von Ausschlussgruppen. Sie können diese Methode verwenden, um nur über ein Angebot (unterscheidet sich von Ihrem Standardinhalt) an einer Position als Teil Ihrer AP-Aktivität zu verfügen.

Das Ausschließen von Standardinhalt ist eine sehr gute Möglichkeit, um das Erscheinungsbild der restlichen Seite zu ändern, um die von Ihnen mit der AP-Aktivität getesteten Angebote anzupassen. Wenn Sie beispielsweise die Farbpalette der von Ihnen getesteten Angebote abgleichen möchten, können Sie die Hintergrundfarbe Ihrer Seite ändern und die standardmäßige Hintergrundfarbe ausschließen.

**So schließen Sie Standardinhalt mit Visual Experience Composer (VEC) aus:**

1. while [Erstellen oder Bearbeiten einer AP-Aktivität](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), wählen Sie den zu ersetzenden Inhalt aus und klicken Sie auf , um auf **[!UICONTROL Text/HTML ändern]**, **[!UICONTROL Bild ändern]** oder **[!UICONTROL Hintergrundfarbe ändern]**.
1. Erstellen Sie im Dialogfeld Ihren neuen Inhalt und deaktivieren Sie **Einbeziehen** rechts neben dem Standardinhalt (oder deaktivieren Sie das Standardbild/-video auf dem Bildschirm „Inhalt auswählen“).

   Je nach Inhalt oder Angebotstyp kann die Variable [!UICONTROL Einschließen] an einer etwas anderen Stelle.

   Für Text-/HTML-Inhalt:

   ![Kontrollkästchen „Einbeziehen“ im Dialogfeld „Text/HTML bearbeiten“](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Für Bild-/Videoinhalt:

   ![Kontrollkästchen „Einbeziehen“ im Dialogfeld „Inhalt auswählen“](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Für die Hintergrundfarbe:

   ![Kontrollkästchen „Einbeziehen“ im Dialogfeld „Hintergrundfarbe bearbeiten“](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Sie können die Erlebnisse über die von Ihnen angegebenen Angebote unter [!UICONTROL Inhalt verwalten] anzeigen. Beachten Sie, dass in keine Erlebnisse erstellt werden [!UICONTROL Inhalt verwalten] unter Verwendung des von Ihnen ausgeschlossenen Standardangebots.

   ![exclude_content_vec_4 image](assets/exclude_content_vec_4.png)

**[!UICONTROL So schließen Sie mit dem formularbasierten Experience Composer Standardinhalt aus]:**

1. Klicken Sie beim Erstellen oder Bearbeiten einer AP-Aktivität unter **[!UICONTROL Inhalt]** auf **[!UICONTROL Text/HTML ändern]** oder **[!UICONTROL Bildangebot ändern]**.
1. Erstellen Sie im Dialogfeld Ihren neuen Inhalt und deaktivieren Sie **[!UICONTROL Einbeziehen]** rechts neben dem Standardinhalt (oder deaktivieren Sie das Standardbild/-video auf dem Bildschirm „Inhalt auswählen“).

   Je nach Inhalt oder Angebotstyp kann die Variable [!UICONTROL Einschließen] an einer etwas anderen Stelle.

   Für Text-/HTML-Inhalt:

   ![exclude_content_form_1 image](assets/exclude_content_form_1.png)

   Für Bild-/Videoinhalt:

   ![exclude_content_form_2 image](assets/exclude_content_form_2.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Sie können die Erlebnisse über die von Ihnen angegebenen Angebote unter [!UICONTROL Inhalt verwalten] anzeigen. Beachten Sie, dass in keine Erlebnisse erstellt werden [!UICONTROL Inhalt verwalten] unter Verwendung des von Ihnen ausgeschlossenen Standardangebots.

   ![exclude_content_form_3 image](assets/exclude_content_form_3.png)
