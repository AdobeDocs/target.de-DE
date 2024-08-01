---
keywords: Empfehlungen erstellen; Recommendations-Aktivität; neue Empfehlungen; Recommendations-Übersicht
description: Erfahren Sie, wie Sie mit dem Adobe [!DNL Target] Visual Experience Composer (VEC) eine Recommendations-Aktivität direkt auf einer für  [!DNL Target] aktivierten Seite erstellen.
title: Wie erstelle ich eine Recommendations-Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: 3c687b2d28f576a60951c8bb10434250104500b4
workflow-type: tm+mt
source-wordcount: '1249'
ht-degree: 55%

---

# Erstellen einer Recommendations-Aktivität

Mit dem Target Visual Experience Composer (VEC) können Sie eine Recommendations-Aktivität direkt auf einer für Target aktivierten Seite erstellen und Teile der Seite in Target verändern.

1. Klicken Sie auf **[!UICONTROL Activities]** > **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

1. Wählen Sie bei Bedarf **[!UICONTROL Visual (Default)]** aus.

   ![Dialogfeld „Erstellen einer Recommendations-Aktivität“](/help/main/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie [!UICONTROL Form] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und zum formularbasierten Experience Composer bietet Target den VEC für Einzelseitenanwendungen und den VEC für Mobile Apps. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die Option [!UICONTROL [Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in der obigen Abbildung ist eine Funktion von [Target Premium](/help/main/c-intro/intro.md) . Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.

1. (Abhängig von Ihrer Lizenz) Wenn Sie [Target Premium-Kunde ](/help/main/c-intro/intro.md#premium)sind, wählen Sie einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie eine Aktivitäts-URL an und klicken Sie auf **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher stimmen sowohl [!DNL `http://www.adobe.com`] als auch [!DNL `https://wwww.adobe.com`] überein.

   Die Aktivitäts-URL ist die Seite, auf der die Empfehlungen eingeblendet werden.

   Wenn Sie auf [!UICONTROL Next] klicken, wird der VEC geöffnet und Ihre Seite angezeigt. Sie können ein aktuelles Element durch Empfehlungen ersetzen oder Empfehlungen einfügen.

1. Klicken Sie auf ein Element auf Ihrer Seite. Wenn an der Position des Elements Empfehlungen verfügbar sind, klicken Sie auf **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]** oder **[!UICONTROL Insert Recommendations After]**.

   Besucher Ihrer Site sehen den empfohlenen Inhalt nur, wenn sie sich für die Empfehlung qualifizieren. Besucher, die sich nicht für die Empfehlung qualifizieren, sehen Standardinhalte.

   ![Recommendations-Optionen](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: Wenn Sie ein Element durch Empfehlungen ersetzen, wird der aktuelle Inhalt gelöscht und durch Ihre Empfehlungen ersetzt. Wenn Besucher Ihre Site besuchen und sich für die Empfehlung qualifizieren, sehen sie die empfohlenen Artikel im angegebenen Bereich anstelle des vorhandenen Inhalts.
   * **[!UICONTROL Insert Recommendations Before]**: Beim Einfügen von Empfehlungen vor dem ausgewählten Element wird der empfohlene Inhalt vor diesem Element platziert. Je nach Seitenaufbau wird die Empfehlung oben oder links neben dem ausgewählten Element angezeigt.
   * **[!UICONTROL Insert Recommendations After]**: Beim Einfügen von Empfehlungen nach dem ausgewählten Element wird der empfohlene Inhalt nach diesem Element platziert. Je nach Seitenaufbau wird die Empfehlung unten oder rechts neben dem ausgewählten Element angezeigt.

   Mit der Option **[!UICONTROL Expand Selection]** können Sie den ausgewählten Ort (übergeordneten Container) erweitern, um die gewünschten Seitenelemente einfacher zu identifizieren und einzuschließen.

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

   Kriterien werden in Form von Karten dargestellt, die Informationen zu dem jeweiligen Kriterium anzeigen. Standardmäßig zeigt der Bildschirm &quot;[!UICONTROL Select Criteria]&quot;Kriterien an, die mit Ihrer vertikalen Branche und dem Seitentyp kompatibel sind, den Sie im vorherigen Schritt ausgewählt haben. Sie können diese Optionen ändern, wenn Sie andere Kriterien angezeigt haben möchten.

   >[!NOTE]
   >
   >Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für die Empfehlungen zum aktuellen Element bzw. zur aktuellen Kategorie übergeben, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Compatible]** . Die Option [!UICONTROL Compatible] wird je nach Ihren Recommendations-Einstellungen ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**) möglicherweise nicht angezeigt. Weitere Informationen finden Sie unter [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

   ![Dialogfeld „Kriterien auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

   * Um nach einem vorhandenen Kriterium zu suchen (z. B. wenn viele Kriterienkarten angezeigt werden), geben Sie einen entsprechenden Suchtext in das Suchfeld ein, bis das gewünschte Kriterium angezeigt wird. Wählen Sie dieses dann aus und klicken Sie auf **[!UICONTROL Next]**.

     Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

   * Um ein neues Kriterium zu erstellen, klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** und geben Sie dann die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Erstellen von Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * Sie können auch Kriterien in Sequenzen gruppieren. Um eine neue Kriteriensequenz zu erstellen, klicken Sie auf **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Weitere Informationen finden Sie unter [Kriteriensequenz erstellen](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md) .

1. Klicken Sie auf **[!UICONTROL Next]**.
1. [Entwurf auswählen](/help/main/c-recommendations/c-design-overview/design-overview.md).

   Ein Entwurf ist eine Vorlage, die das Aussehen der Orte auf Ihrer Seite festlegt. [!DNL Target] enthält mehrere vorkonfigurierte Entwürfe. Sie können auch Ihre eigenen, benutzerdefinierten Entwürfe erstellen. Weitere Informationen finden Sie unter [Erstellen eines Entwurfs](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) und [Anpassen eines Entwurfs](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Dialogfeld „Entwurf auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Jeder Entwurf beinhaltet eine grafische Darstellung des jeweiligen Entwurfs und Symbole, die zeigen, wie viele Ihrer aktiven und inaktiven Aktivitäten derzeit diesen Entwurf verwenden.

   * Um einen oder mehrere vorhandene Entwürfe auszuwählen, klicken Sie auf die Entwürfe und dann auf **[!UICONTROL Next]**.

     Wenn Sie mehrere Kriterien ausgewählt haben, können Sie lediglich einen Entwurf auswählen.

   * Um einen benutzerdefinierten Entwurf zu erstellen, klicken Sie auf **[!UICONTROL Create Design]** und geben Sie dann den Namen und den Code für den neuen Entwurf ein. Klicken Sie auf &quot;**[!UICONTROL Next]**&quot;, wählen Sie ein Bild aus oder laden Sie es hoch und klicken Sie auf &quot;**[!UICONTROL Done]**&quot;> &quot;**[!UICONTROL Done]**&quot;. Weitere Informationen zum Erstellen eines neuen Entwurfs finden Sie unter [Erstellen eines Entwurfs](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicken Sie auf **[!UICONTROL Next]**.

   Sie haben auch die Möglichkeit, Ihren Empfehlungen Promotions hinzuzufügen. Weitere Informationen zum Hinzufügen von Vorwärts- und Rückwärts-Promotions finden Sie unter [Hinzufügen von Promotions](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicken Sie auf **[!UICONTROL Save]**.

   Im Bildschirm „VEC“ wird das Empfehlungsdesign Ihrer Seite angezeigt.

1. (Optional) Klicken Sie auf **[!UICONTROL Preview]** , um zu sehen, wie die Aktivität für Besucher aussehen wird.

   Der [!UICONTROL Preview] -Modus ermöglicht Ihnen die Interaktion mit Ihren Empfehlungen, so wie es ein Besucher tun würde.

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
   * Sammlung ändern (neben der Bezeichnung [!UICONTROL Criteria] )
   * Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Entwurfscode anzeigen
   * Entwurf ändern oder entfernen

1. Klicken Sie zum Abschluss auf **[!UICONTROL Next]** .
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
   * Freigeben der Aktivität für Ihren Experience Cloud-Feed
   * Aktivität überprüfen
   * Ihre Erlebnis-URLs ansehen
   * Daten herunterladen
   * den Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Details zu Kriterien ein- oder ausblenden
   * Code für Ihre Entwürfe ansehen

1. (Optional) Öffnen Sie die Seite &quot;[!UICONTROL Reports]&quot;, um den Bericht anzuzeigen, der die Leistung Ihrer [!DNL Recommendations] -Aktivität anzeigt.

1. (Optional) Öffnen Sie die Seite &quot;[!UICONTROL Collisions]&quot;, um alle möglicherweise auftretenden [Aktivitätskollisionen](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) anzuzeigen.

   Kollisionen von Aktivitäten treten auf, wenn mehrere Aktivitäten Inhalte auf derselben Seite bereitstellen sollen. Dies kann zur Darstellung unerwarteter Inhalte führen.

## Schulungsvideo: Erstellen einer Recommendations-Aktivität (7:15) ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
