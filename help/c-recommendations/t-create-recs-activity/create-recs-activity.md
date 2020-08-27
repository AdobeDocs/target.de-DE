---
keywords: create recommendations;recommendations activity;new recommendations;recommendations overview
description: Mit dem Target Visual Experience Composer (VEC) können Sie eine Recommendations-Aktivität direkt auf einer für Target aktivierten Seite erstellen und Teile der Seite in Target verändern.
title: Erstellen einer Recommendations-Aktivität
feature: recs creation
uuid: c3f22cce-204a-4509-92c4-8fec43fbaebe
translation-type: tm+mt
source-git-commit: d5a48db0c954871269714ef32d0545ed4898660f
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 93%

---


# ![PREMIUM](/help/assets/premium.png) Eine Recommendations-Aktivität erstellen{#create-a-recommendations-activity}

Mit dem Target Visual Experience Composer (VEC) können Sie eine Recommendations-Aktivität direkt auf einer für Target aktivierten Seite erstellen und Teile der Seite in Target verändern.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Empfehlungen]**.

   ![Erstellen einer Recommendations-Aktivität](/help/c-recommendations/t-create-recs-activity/assets/Menu_CreateActivity.png)

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Standard)]** aus.

   ![Dialogfeld „Erstellen einer Recommendations-Aktivität“](/help/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie [!UICONTROL Formular] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und zum formularbasierten Experience Composer bietet Target den VEC für Einzelseitenanwendungen und den VEC für Mobile Apps. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >The [!UICONTROL [Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.

1. (Abhängig von Ihrer Lizenz) Wenn Sie [Target Premium-Kunde ](/help/c-intro/intro.md#premium)sind, wählen Sie einen [Arbeitsbereich](/help/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie eine Aktivitäts-URL an und klicken Sie auf **[!UICONTROL Weiter]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] überein.

   Die Aktivitäts-URL ist die Seite, auf der die Empfehlungen eingeblendet werden.

   Wenn Sie auf [!UICONTROL Weiter] klicken, wird Ihre Seite im VEC geöffnet. Sie können ein aktuelles Element durch Empfehlungen ersetzen oder Empfehlungen einfügen.

1. Click an element on your page, then if recommendations are available where that element is located, click **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]**, or **[!UICONTROL Insert Recommendations After]**.

   ![Recommendations-Optionen](/help/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   Wenn Sie ein Element durch Empfehlungen ersetzen, wird der aktuelle Inhalt gelöscht und durch Ihre Empfehlungen ersetzt.

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

   ![Optionen zur Auswahl des Seitentyps](/help/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. [Wählen Sie mindestens ein Kriterium aus](/help/c-recommendations/c-algorithms/algorithms.md).

   Kriterien werden in Form von Karten dargestellt, die Informationen zu dem jeweiligen Kriterium anzeigen. In der Standardeinstellung werden im Bildschirm [!UICONTROL Kriterien auswählen] Kriterien angezeigt, die mit Ihrem vertikalen Markt und dem von Ihnen ausgewählten Seitentyp kompatibel sind. Sie können diese Optionen ändern, wenn Sie andere Kriterien angezeigt haben möchten.

   >[!NOTE]
   >
   >Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für die Empfehlungen zum aktuellen Element bzw. zur aktuellen Kategorie übergeben, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, heben Sie die Auswahl für die Option **[!UICONTROL Kompatibel]** auf. Die Option [!UICONTROL Kompatibel] wird je nach Recommendations-Einstellungen (**[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]** > **[!UICONTROL Inkompatible Kriterien filtern]**) möglicherweise nicht angezeigt. Weitere Informationen finden Sie unter [Einstellungen](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84).

   ![Dialogfeld „Kriterien auswählen“](/help/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

   * Um nach einem vorhandenen Kriterium zu suchen (zum Beispiel wenn viele Kriterienkarten angezeigt werden), geben Sie einen entsprechenden Suchtext in das Suchfeld ein, bis das gewünschte Kriterium angezeigt wird. Wählen Sie dieses dann aus und klicken Sie auf **[!UICONTROL Weiter]**.

      Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

   * To create a new criteria, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**, then fill in the information for the new criteria. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Erstellen von Kriterien](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE).
   * Sie können auch Kriterien in Sequenzen gruppieren. To create a new criteria sequence, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Weitere Informationen finden Sie unter [Erstellen von Kriteriensequenzen](../../c-recommendations/c-algorithms/create-criteria-sequence.md#task_8A9CB465F28D44899F69F38AD27352FE).

1. Klicken Sie auf **[!UICONTROL Weiter]**.
1. [Entwurf auswählen](/help/c-recommendations/c-design-overview/design-overview.md).

   Ein Entwurf ist eine Vorlage, die das Aussehen der Orte auf Ihrer Seite festlegt. [!DNL Target] enthält mehrere vorkonfigurierte Entwürfe. Sie können auch Ihre eigenen, benutzerdefinierten Entwürfe erstellen. Weitere Informationen finden Sie unter  [Erstellen eines Entwurfs](../../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) und [Anpassen eines Entwurfs](../../c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Dialogfeld „Entwurf auswählen“](/help/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Jeder Entwurf beinhaltet eine grafische Darstellung des jeweiligen Entwurfs und Symbole, die zeigen, wie viele Ihrer aktiven und inaktiven Aktivitäten derzeit diesen Entwurf verwenden.

   * Wenn Sie einen oder mehrere der vorhandenen Entwurf auswählen möchten, klicken Sie auf die Entwürfe und anschließend auf **[!UICONTROL Weiter]**.

      Wenn Sie mehrere Kriterien ausgewählt haben, können Sie lediglich einen Entwurf auswählen.

   * Um einen benutzerdefinierten Entwurf zu erstellen, klicken Sie auf **[!UICONTROL Entwurf erstellen]** und geben dann den Namen und den Code für den neuen Entwurf ein. Klicken Sie auf **[!UICONTROL Weiter]**, wählen Sie anschließend ein Bild aus oder laden Sie ein Bild hoch und klicken Sie dann auf **[!UICONTROL Fertig]** > **[!UICONTROL Fertig]**. Weitere Informationen zum Erstellen eines neuen Entwurfs finden Sie unter [Erstellen eines Entwurfs](../../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicken Sie auf **[!UICONTROL Weiter]**.

   Sie haben auch die Möglichkeit, Ihren Empfehlungen Promotions hinzuzufügen. Weitere Informationen über das Hinzufügen von Vorwärts- und Rückwärts-Promotions finden Sie unter  [Hinzufügen von Promotions](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).
1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Im Bildschirm „VEC“ wird das Empfehlungsdesign Ihrer Seite angezeigt.

1. (Optional) Klicken Sie auf **[!UICONTROL Vorschau]**, um zu sehen, wie die Aktivität für Besucher angezeigt wird.

   Im [!UICONTROL Vorschau]-Modus können Sie mit Ihren Empfehlungen interagieren, so wie es ein Besucher tun würde.

   Haben Sie die Vorschau der Empfehlungen abgeschlossen, klicken Sie auf **[!UICONTROL Erstellen]**.

1. Überprüfen Sie Ihre Empfehlung im VEC und klicken Sie auf **[!UICONTROL Weiter]**.

1. Überprüfen Sie Ihre [!DNL Recommendations]-Aktivität im Flussdiagramm und nehmen Sie erforderliche Änderungen vor.

   ![Flussdiagramm für Recommendations](/help/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   Das Flussdiagramm führt Sie durch die Schritte zur Auswahl der Zielgruppe für die Aktivität, zum Einrichten der Erlebnisse und zum Festlegen der Erfolgsmetriken.

   Im Flussdiagramm haben Sie folgende Möglichkeiten:

   * Ändern der Zielgruppe, der Empfehlungen angezeigt werden

      >[!NOTE]
      >
      >Zusätzlich zur Auswahl einer vorhandenen Zielgruppe können Sie eine [Zielgruppe für nur eine Aktivität erstellen](../../c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) oder [mehrere Zielgruppen kombinieren](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), um Ad-hoc-Zielgruppen zu erstellen statt eine neue Zielgruppe zu erstellen.

      Standardmäßig werden Empfehlungen für alle Benutzer angezeigt. Sie können Empfehlungen jedoch auf eine spezifische Zielgruppe ausrichten.

      Bei einer [!DNL Recommendations]-Aktivität wird der Kontrollgruppe die Seite ohne Empfehlungen angezeigt.

   * Kriterien ansehen
   * Sammlung ändern (neben der Bezeichnung [!UICONTROL Kriterien])
   * Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Entwurfscode anzeigen
   * Entwurf ändern oder entfernen

1. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie fertig sind.
1. Geben Sie Ihre Aktivitätseinstellungen an.

   Geben Sie zum Beispiel einen Namen (erforderlich) und ein Ziel (optional) für die Aktivität ein. Weitere Informationen zu den Einstellungen finden Sie unter [Recommendations Activities-Einstellungen](../../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >Wenn Sie einen [!DNL Recommendation]-Aktivitätsnamen angeben, der bereits für eine andere Aktivität in [!DNL Recommendations Classic] vorhanden ist, wird die neue Aktivität noch einmal mit einem neuen Namen synchronisiert. Der neue Name ist der ursprüngliche Name, der mit einem Zeitstempel versehen wird, um ihn eindeutig zu machen. Dieser neue Name wird sowohl in [!DNL Target Standard/Premium] als auch in [!DNL Recommendations Classic] angezeigt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]**.

   Für Ihre Aktivität wird eine Übersicht angezeigt.

   Auf der Seite [!UICONTROL Übersicht] können Sie:

   * die Aktivität aktivieren
   * die Aktivität bearbeiten
   * die Aktivität an Ihre Experience Cloud-Pinnwand anheften
   * Ihre Erlebnis-URLs ansehen
   * Daten herunterladen
   * den Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Details zu Kriterien ein- oder ausblenden
   * Code für Ihre Entwürfe ansehen

1. (Optional) Öffnen Sie die Seite [!UICONTROL Berichte], um den Bericht anzusehen, der die Leistung Ihrer [!DNL Recommendations]-Aktivität anzeigt.
1. (Optional) Öffnen Sie die Seite [!UICONTROL Kollisionen], um eventuell auftretende [Aktivitäten-Kollisionen](/help/c-experiences/c-visual-experience-composer/activity-collisions.md) anzuzeigen.

   Kollisionen von Aktivitäten treten auf, wenn mehrere Aktivitäten Inhalte auf derselben Seite bereitstellen sollen. Dies kann zur Darstellung unerwarteter Inhalte führen.

## Schulungsvideo: Erstellen einer Recommendations-Aktivität (7:15) ![Tutorialzeichen](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)