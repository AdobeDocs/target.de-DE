---
keywords: Empfehlungen erstellen; Recommendations-Aktivität; neue Empfehlungen; Recommendations-Übersicht
description: Erfahren Sie, wie Sie mit dem  [!DNL Target] [!UICONTROL Visual Experience Composer]VEC) eine  [!DNL Recommendations] -Aktivität erstellen.
title: Wie erstelle ich eine  [!DNL Recommendations] -Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 52%

---

# [!DNL Recommendations] erstellen

Verwenden Sie den [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC), um eine [!DNL Recommendations] Aktivität direkt auf einer [!DNL Target]-aktivierten Seite zu erstellen und Teile der Seite innerhalb von [!DNL Target] zu ändern.

1. Klicken Sie auf **[!UICONTROL Activities]** > **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

1. Wählen Sie bei Bedarf **[!UICONTROL Visual]** aus.

   Wenn Sie die [!UICONTROL Form-Based Experience Composer] bevorzugen, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und [!UICONTROL Form-Based Experience Composer] bietet [!DNL Target] den [!UICONTROL Single Page Application] VEC an. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Bedingt) Wählen Sie einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geben Sie eine Aktivitäts-URL an und klicken Sie dann auf **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] überein.

   Die Aktivitäts-URL ist die Seite, auf der die Empfehlungen angezeigt werden.

   Wenn Sie auf [!UICONTROL Create] klicken, öffnet sich VEC und zeigt Ihre Seite an. Sie können ein aktuelles Element durch Empfehlungen ersetzen oder Empfehlungen einfügen.

1. Klicken Sie auf ein Element auf Ihrer Seite. Wenn dann Empfehlungen für den Speicherort dieses Elements verfügbar sind, klicken Sie auf **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]** oder **[!UICONTROL Insert Recommendations After]**.

   Besucher Ihrer Site sehen die empfohlenen Inhalte nur, wenn sie für die Empfehlung qualifiziert sind. Besucherinnen und Besucher, die sich nicht für die Empfehlung qualifizieren, sehen Standardinhalte.

   ![Recommendations-Optionen](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: Wenn Sie ein Element durch Empfehlungen ersetzen, wird der aktuelle Inhalt gelöscht und durch Ihre Empfehlungen ersetzt. Wenn Besucher Ihre Site besuchen und sich für die Empfehlung qualifizieren, werden ihnen die empfohlenen Elemente im angegebenen Bereich anstelle des vorhandenen Inhalts angezeigt.
   * **[!UICONTROL Insert Recommendations Before]**: Durch Einfügen von Empfehlungen vor dem ausgewählten Element wird der empfohlene Inhalt vor diesem Element platziert. Je nach Seitenaufbau wird die Empfehlung über dem ausgewählten Element oder links davon angezeigt.
   * **[!UICONTROL Insert Recommendations After]**: Durch Einfügen von Empfehlungen nach dem ausgewählten Element wird der empfohlene Inhalt nach diesem Element platziert. Je nach Seitenaufbau wird die Empfehlung unter oder rechts neben dem ausgewählten Element angezeigt.

   Mit der Option **[!UICONTROL Expand Selection]** können Sie die ausgewählte Position (den übergeordneten Container) erweitern, damit Sie die gewünschten Seitenelemente leichter identifizieren und einschließen können.

1. Wählen Sie einen Seitentyp aus.

   Zu den Seitentypen zählen:

   * Einkaufswagenseite
   * Kategorieseite
   * „Homepage“
   * Landingpage
   * Produktseite
   * Suchergebnisseite
   * Danksagungsseite
   * Sonstige

   ![Optionen zur Auswahl des Seitentyps](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. [Wählen Sie mindestens ein Kriterium aus](/help/main/c-recommendations/c-algorithms/algorithms.md).

   Kriterien werden in Form von Karten dargestellt, die Informationen zu dem jeweiligen Kriterium anzeigen. Standardmäßig zeigt der Bildschirm [!UICONTROL Select Criteria] Kriterien an, die mit Ihrer vertikalen Branche und dem Seitentyp kompatibel sind, den Sie im vorherigen Schritt ausgewählt haben. Sie können diese Optionen ändern, wenn Sie andere Kriterien angezeigt haben möchten.

   >[!NOTE]
   >
   >Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für die Empfehlungen zum aktuellen Element bzw. zur aktuellen Kategorie übergeben, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn für die Aktivität jedoch inkompatible Kriterien verfügbar sein sollen, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Compatible]** . Die Option [!UICONTROL Compatible] wird je nach Ihren Recommendations-Einstellungen möglicherweise nicht angezeigt ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**). Weitere Informationen finden Sie unter [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=de){target=_blank}.

   ![Dialogfeld „Kriterien auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

   * Um nach einem vorhandenen Kriterium zu suchen (z. B. wenn eine große Anzahl von Kriterienkarten angezeigt wird), geben Sie im Suchfeld ein, bis das gewünschte Kriterium angezeigt wird. Wählen Sie dann das Kriterium aus und klicken Sie auf **[!UICONTROL Next]**.

     Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

   * Um neue Kriterien zu erstellen, klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** und geben Sie die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Erstellen von Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * Sie können auch Kriterien in Sequenzen gruppieren. Um eine neue Kriteriensequenz zu erstellen, klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Weitere Informationen [ Sie unter ](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md) von Kriterien erstellen .

1. Klicken Sie auf **[!UICONTROL Next]**.
1. [Entwurf auswählen](/help/main/c-recommendations/c-design-overview/design-overview.md).

   Ein Entwurf ist eine Vorlage, die das Aussehen der Orte auf Ihrer Seite festlegt. [!DNL Target] umfasst mehrere vorkonfigurierte Designs. Sie können auch Ihre eigenen, benutzerdefinierten Entwürfe erstellen. Weitere Informationen finden Sie unter [Erstellen eines Designs](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) und [Anpassen eines Designs](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Dialogfeld „Entwurf auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Jeder Entwurf beinhaltet eine grafische Darstellung des jeweiligen Entwurfs und Symbole, die zeigen, wie viele Ihrer aktiven und inaktiven Aktivitäten derzeit diesen Entwurf verwenden.

   * Um ein oder mehrere vorhandene Designs auszuwählen, klicken Sie auf die Designs und dann auf **[!UICONTROL Next]**.

     Wenn Sie mehrere Kriterien ausgewählt haben, können Sie lediglich einen Entwurf auswählen.

   * Um einen benutzerdefinierten Entwurf zu erstellen, klicken Sie auf **[!UICONTROL Create Design]** und geben Sie dann den Namen und den Code für den neuen Entwurf ein. Klicken Sie auf **[!UICONTROL Next]**, wählen Sie dann ein Bild aus oder laden Sie es hoch und klicken Sie auf **[!UICONTROL Done]** > **[!UICONTROL Done]**. Weitere Informationen zum Erstellen eines neuen Entwurfs finden Sie unter [Erstellen eines Entwurfs](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicken Sie auf **[!UICONTROL Next]**.

   Sie haben auch die Möglichkeit, Ihren Empfehlungen Promotions hinzuzufügen. Weitere Informationen zum Hinzufügen von Promotions vorne und hinten finden Sie unter [Hinzufügen von Promotions](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicken Sie auf **[!UICONTROL Save]**.

   Im Bildschirm „VEC“ wird das Empfehlungsdesign Ihrer Seite angezeigt.

1. (Optional) Klicken Sie auf **[!UICONTROL Preview]** , um zu sehen, wie die Aktivität den Besuchern angezeigt wird.

   [!UICONTROL Preview] Modus können Sie mit Ihren Empfehlungen ähnlich wie ein Besucher interagieren.

   Wenn Sie mit der Vorschau Ihrer Empfehlungen fertig sind, klicken Sie auf **[!UICONTROL Compose]**.

1. Überprüfen Sie Ihre Empfehlung im VEC und klicken Sie dann auf **[!UICONTROL Next]**.

1. Überprüfen Sie Ihre [!DNL Recommendations]-Aktivität im Flussdiagramm und nehmen Sie erforderliche Änderungen vor.

   ![Flussdiagramm für Recommendations](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität, zum Einrichten der Erlebnisse und zum Festlegen der Erfolgsmetriken.

   Im Flussdiagramm haben Sie folgende Möglichkeiten:

   * Ändern der Zielgruppe, der Empfehlungen angezeigt werden

     >[!NOTE]
     >
     >Zusätzlich zur Auswahl einer vorhandenen Zielgruppe können Sie eine [Zielgruppe für nur eine Aktivität erstellen](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) oder [mehrere Zielgruppen kombinieren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um Ad-hoc-Zielgruppen zu erstellen statt eine neue Zielgruppe zu erstellen.

     Standardmäßig werden Empfehlungen für alle Benutzer angezeigt. Sie können Empfehlungen jedoch auf eine spezifische Zielgruppe ausrichten.

     Bei einer [!DNL Recommendations]-Aktivität wird der Kontrollgruppe die Seite ohne Empfehlungen angezeigt.

   * Kriterien ansehen
   * Sammlung ändern (neben der [!UICONTROL Criteria])
   * Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Entwurfscode anzeigen
   * Entwurf ändern oder entfernen

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Next]** .
1. Geben Sie Ihre Aktivitätseinstellungen an.

   Geben Sie zum Beispiel einen Namen (erforderlich) und ein Ziel (optional) für die Aktivität ein. Weitere Informationen zu den Einstellungen finden Sie unter [Recommendations Activities-Einstellungen](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >Wenn Sie einen [!DNL Recommendation]-Aktivitätsnamen angeben, der bereits für eine andere Aktivität in [!DNL Recommendations Classic] vorhanden ist, wird die neue Aktivität noch einmal mit einem neuen Namen synchronisiert. Der neue Name ist der ursprüngliche Name, der mit einem Zeitstempel versehen wird, um ihn eindeutig zu machen. Dieser neue Name wird sowohl in [!DNL Target Standard/Premium] als auch in [!DNL Recommendations Classic] angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save & Close]**.

   Für Ihre Aktivität wird eine Übersicht angezeigt.

   Auf der Seite [!UICONTROL Overview] haben Sie folgende Möglichkeiten:

   * die Aktivität aktivieren
   * die Aktivität bearbeiten
   * Aktivität für Ihren Experience Cloud-Feed freigeben
   * QA der Aktivität
   * Ihre Erlebnis-URLs ansehen
   * Daten herunterladen
   * den Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Details zu Kriterien ein- oder ausblenden
   * Code für Ihre Entwürfe ansehen

1. (Optional) Öffnen Sie die Seite [!UICONTROL Reports] , um den Bericht anzuzeigen, der die Leistung Ihrer [!DNL Recommendations]-Aktivität zeigt.

1. (Optional) Öffnen Sie die Seite [!UICONTROL Collisions] , um alle [Aktivitätskollisionen](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) anzuzeigen, die auftreten könnten.

   Kollisionen von Aktivitäten treten auf, wenn mehrere Aktivitäten Inhalte auf derselben Seite bereitstellen sollen. Dies kann zur Darstellung unerwarteter Inhalte führen.

## Schulungsvideo: Erstellen einer Recommendations-Aktivität (7:15) ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
