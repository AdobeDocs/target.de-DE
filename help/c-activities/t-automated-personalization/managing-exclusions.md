---
description: Verwalten Sie Ausnahmen, indem Sie Ausschlussgruppen erstellen, ohne duplizierte Angebote auszuschließen, bestimmte Erlebnisse auszuschließen und Standardinhalte in automatisierten Personalisierungs-Aktivitäten (AP) auszuschließen.
keywords: deduplizieren;Duplikate zulassen;duplizierte Angebote ausschließen;automatisierte Personalisierung;duplizierte Angebote nicht zulassen
seo-description: Verwalten Sie Ausschlüsse, indem Sie Ausschlussgruppen erstellen, ohne duplizierte Angebote ausschließen, bestimmte Erlebnisse ausschließen und Standardinhalte in Aktivitäten mit automatisierter Personalisierung (AP) von Adobe Target ausschließen.
seo-title: Verwalten von Ausschlüssen
solution: Target,Analytics
title: Verwalten von Ausschlüssen
uuid: c67901d2-19cd-47d3-b8c4-abdcb046f404
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![Ausnahmen für Premium-Badge](/help/assets/premium.png) verwalten{#manage-exclusions}

Verwalten Sie Ausnahmen, indem Sie Ausschlussgruppen erstellen, ohne duplizierte Angebote auszuschließen, bestimmte Erlebnisse auszuschließen und Standardinhalte in automatisierten Personalisierungs-Aktivitäten (AP) auszuschließen.

## Create exclusion groups {#task_AAAA6C7239A84F7696C8492F04B575A2}

Erstellen Sie Ausschlussgruppen in AP-Aktivitäten (automatisierte Personalisierung), um sicherzustellen, dass Erlebnisse mit den vorgesehenen Angeboten automatisch ausgeschlossen werden.

Ausschlussgruppen eignen sich hervorragend, um sicherzustellen, dass nicht kompatible Angebote nicht an verschiedenen Stellen in demselben Erlebnis dargestellt werden. Nehmen wir beispielsweise an, es liegen zwei Angebote vor: eines beinhaltet 20 % Rabatt auf alle Waren und das andere 15 % Rabatt. Diese beiden Angebote sollten den Besuchern grundsätzlich nie innerhalb desselben Erlebnisses präsentiert werden. Indem Sie diese beiden Angebote einer Ausschlussgruppe hinzufügen, können Sie sicherstellen, dass dies nie der Fall sein wird.

Sie können auch einschränken, welche Zielgruppen bestimmte Angebote in AP-Aktivitäten anzeigen können. For more information, see [Target Automated Personalization offers](/help/c-activities/t-automated-personalization/ap-target-offers.md).

**So erstellen Sie eine Ausschlussgruppe:**

1. While [creating or editing an AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md), click **[!UICONTROL Manage Content]** in the header bar.

   ![Inhaltsverwaltung verwalten](/help/c-activities/t-automated-personalization/assets/manage-content.png)

1. Klicken Sie im Dialogfeld [!UICONTROL Inhalt verwalten]**auf[!UICONTROL Ausschlussgruppe]**.

   ![Inhalt verwalten &gt; Ausschlussgruppen, Dialogfeld](/help/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Wenn Sie zuvor Ausschlussgruppen erstellt haben, werden sie in der Liste angezeigt. Wenn Sie noch keine Ausschlussgruppe erstellt haben, werden Sie aufgefordert, eine zu erstellen.

1. Klicken Sie auf **[!UICONTROL Ausschlussgruppe erstellen]**.

   ![Ausschlussgruppe erstellen, Dialogfeld](/help/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Erforderlich) Geben Sie einen beschreibenden Namen für die Ausschlussgruppe an.

   Ein beschreibender Name hilft Ihnen oder anderen Benutzern, schnell eine Gruppe zu finden und ihren Zweck zu verstehen.

1. Suchen Sie die gewünschten Angebote, die Sie der Ausschlussgruppe hinzufügen möchten, und wählen Sie sie aus.

   Sie können mehrere Angebote vom selben Standort in einer Ausschlussgruppe auswählen.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Die Angebote in der Ausschlussgruppe werden von nun an automatisch aus denselben Erlebnissen ausgeschlossen.

## Exclude duplicate offers {#concept_4EF78013F80E48EFA024AE0274C9F037}

Verhindern Sie die Duplizierung von Angeboten aus der Bibliothek, wenn diese bei [!UICONTROL automatischer Personalisierung] an verschiedenen Orten eingesetzt werden.

Möglicherweise verfügen Sie über eine Aktivität mit sechs Orten auf einer Seite mit 12 Angeboten. Hier besteht die Gefahr, dass das gleiche Angebot in einer Aktivität mehrmals angezeigt wird. Dadurch wird verhindert, dass doppelte Angebote gleichzeitig an unterschiedlichen Positionen in derselben Aktivität angezeigt werden.

Klicken Sie auf **[!UICONTROL Konfigurieren]** &gt; **[!UICONTROL Doppelt vorhandenes Angebot]** und wählen Sie **[!UICONTROL Duplikate zulassen]** oder **[!UICONTROL Duplikate nicht zulassen]** aus.

![Optionen für doppelte Angebote](/help/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Exclude specific experiences {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Schließen Sie spezifische Erlebnisse aus, wenn Sie bestimmte Angebotskombinationen aus Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ ausschließen möchten.

Es gibt möglicherweise bestimmte Kombinationen, die nicht gut gemeinsam funktionieren, oder Sie möchten möglicherweise die Anzahl der getesteten Erlebnisse eingrenzen, um die Traffic-Anforderungen für Ihre Aktivität zu verringern.

1. While [creating or editing an AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md), click **Manage Content** in the header bar.

   ![Inhaltsverwaltung verwalten](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Die Liste [!UICONTROL Erlebnisse] zeigt jedes Erlebnis an, das anhand der Permutationen sämtlicher Inhalts- und Positionsoptionen generiert wurde.

1. Sie können Erlebnisse nach Bedarf ausschließen.

   Sie können spezifische Erlebnisse ausschließen, indem mit dem Mauszeiger über das gewünschte Erlebnis fahren und dann auf das Ausschlusssymbol klicken.

   ![Erlebnis durch den Mauszeiger ausschließen](/help/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Or you can batch exclude/include experiences by selecting the checkbox for the relevant experiences and then clicking the **[UICONTROL Exclude]** icon in the top right corner of the dialog box. The [!UICONTROL Exclude] icon appears when one or more experiences are checked.

   ![Erlebnisse ausschließen](/help/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   Sie können diese Listenansicht so filtern, dass nur ausgeschlossene oder nur eingeschlossene Aktivitäten angezeigt werden. Klicken Sie dazu auf die Dropdownliste [!UICONTROL Status].

   Die Erlebnisse werden nun aus der Aktivität ausgeschlossen und ihr [!UICONTROL Status] lautet [!UICONTROL Ausgeschlossen].

   ![Ausgeschlossene Erlebnisse](/help/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Exclude default content {#task_DCB4528989DF4C05A3A4729E5891D18F}

In manchen Fällen möchten Sie Ihren Standardinhalt möglicherweise nicht als ein Teil Ihrer Aktivität vom Typ „Automatisierte Personalisierung“ einbeziehen. Wie Sie auf diese Einstellung zugreifen, unterscheidet sich vom Erstellen von Ausschlussgruppen. Mit dieser Methode können Sie im Rahmen Ihrer AP-Aktivität nur ein Angebot (anders als Ihren Standardinhalt) an einem Ort verwenden.

Das Ausschließen von Standardinhalten bietet eine großartige Möglichkeit, das Erscheinungsbild des Rest der Seite an die Angebote anzupassen, die Sie mit Ihrer AP-Aktivität testen. Wenn Sie beispielsweise die Farbpalette der von Ihnen getesteten Angebote abgleichen möchten, können Sie die Hintergrundfarbe Ihrer Seite ändern und die standardmäßige Hintergrundfarbe ausschließen.

**So schließen Sie Standardinhalt mit Visual Experience Composer (VEC) aus:**

1. While [creating or editing an AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md), select the content you want to replace and click to access **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]**, or **[!UICONTROL Change Background Color]**.
1. Erstellen Sie im Dialogfeld Ihren neuen Inhalt und deaktivieren Sie **Einbeziehen** rechts neben dem Standardinhalt (oder deaktivieren Sie das Standardbild/-video auf dem Bildschirm „Inhalt auswählen“).

   Je nach Inhalts-/Angebotstyp befindet sich das Kontrollkästchen [!UICONTROL Einbeziehen] an einer etwas anderen Position.

   Für Text-/HTML-Inhalt:

   ![Kontrollkästchen &quot;Text/HTML bearbeiten&quot; aktivieren](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Für Bild-/Videoinhalt:

   ![Kontrollkästchen aktivieren, Dialogfeld &quot;Inhalt auswählen «](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Für die Hintergrundfarbe:

   ![Kontrollkästchen im Dialogfeld Hintergrundfarbe bearbeiten aktivieren](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Sie können die Erlebnisse über die von Ihnen angegebenen Angebote unter [!UICONTROL Inhalt verwalten] anzeigen. Sie werden feststellen, dass in [!UICONTROL Inhalt verwalten] keine Erlebnisse mit dem von Ihnen ausgeschlossenen Standardangebot erstellt sind.

   ![](assets/exclude_content_vec_4.png)

**So schließen Sie mit dem formularbasierten Experience Composer Standardinhalt aus:**

1. Klicken Sie beim Erstellen oder Bearbeiten einer AP-Aktivität unter **[!UICONTROL Inhalt]** auf **[!UICONTROL Text/HTML ändern]** oder **[!UICONTROL Bildangebot ändern]**.
1. Erstellen Sie im Dialogfeld Ihren neuen Inhalt und deaktivieren Sie **[!UICONTROL Einbeziehen]rechts neben dem Standardinhalt (oder deaktivieren Sie das Standardbild/-video auf dem Bildschirm „Inhalt auswählen“).**

   Je nach Inhalts-/Angebotstyp befindet sich das Kontrollkästchen „Einbeziehen“ an einer etwas anderen Position.

   Für Text-/HTML-Inhalt:

   ![](assets/exclude_content_form_1.png)

   Für Bild-/Videoinhalt:

   ![](assets/exclude_content_form_2.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Sie können die Erlebnisse über die von Ihnen angegebenen Angebote unter [!UICONTROL Inhalt verwalten] anzeigen. Sie werden feststellen, dass in [!UICONTROL Inhalt verwalten] keine Erlebnisse mit dem von Ihnen ausgeschlossenen Standardangebot erstellt sind.

   ![](assets/exclude_content_form_3.png)
