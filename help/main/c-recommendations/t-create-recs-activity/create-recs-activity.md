---
keywords: Empfehlungen erstellen; Recommendations-Aktivität; neue Empfehlungen; Recommendations-Übersicht
description: Erfahren Sie, wie Sie die Adobe verwenden [!DNL Target] Visual Experience Composer (VEC) zum Erstellen einer Recommendations-Aktivität direkt auf einer [!DNL Target]-aktivierte Seite.
title: Wie erstelle ich eine Recommendations-Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1321'
ht-degree: 61%

---

# Erstellen einer Recommendations-Aktivität

Mit dem Target Visual Experience Composer (VEC) können Sie eine Recommendations-Aktivität direkt auf einer für Target aktivierten Seite erstellen und Teile der Seite in Target verändern.

1. Klicks **[!UICONTROL Aktivität erstellen]** > **[!UICONTROL Recommendations]**.

   ![Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_CreateActivity.png)

1. Auswählen **[!UICONTROL Visuell (Standard)]**, falls erforderlich.

   ![Dialogfeld „Erstellen einer Recommendations-Aktivität“](/help/main/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   Wenn Sie den formularbasierten Experience Composer bevorzugen, wählen Sie [!UICONTROL Formular] aus. Weitere Informationen finden Sie unter [Formularbasierter Experience Composer](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Zusätzlich zum VEC und zum formularbasierten Experience Composer bietet Target den VEC für Einzelseitenanwendungen und den VEC für Mobile Apps. Weitere Informationen zu den verschiedenen Composern finden Sie unter [Erlebnisse und Angebote](/help/main/c-experiences/experiences.md).
   >
   >Informationen zur Problembehebung für den VEC finden Sie unter [Fehlerbehebung für den Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >Die [!UICONTROL [Arbeitsplatz auswählen]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) -Option in der obigen Abbildung ist eine [Target Premium](/help/main/c-intro/intro.md) Funktion. Wenn diese Option nicht angezeigt wird, verfügt Ihr Unternehmen über eine Target Standard-Lizenz.

1. (Abhängig von Ihrer Lizenz) Wenn Sie [Target Premium-Kunde ](/help/main/c-intro/intro.md#premium)sind, wählen Sie einen [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) aus.

1. Geben Sie eine Aktivitäts-URL an und klicken Sie auf **[!UICONTROL Nächste]**.

   >[!NOTE]
   >
   >[!DNL Target] unterscheidet nicht zwischen URL-Protokollen ([!DNL https] und [!DNL http]). Daher [!DNL `http://www.adobe.com`] und [!DNL `https://wwww.adobe.com`] beide stimmen überein.

   Die Aktivitäts-URL ist die Seite, auf der die Empfehlungen eingeblendet werden.

   Wenn Sie auf [!UICONTROL Weiter] klicken, wird Ihre Seite im VEC geöffnet. Sie können ein aktuelles Element durch Empfehlungen ersetzen oder Empfehlungen einfügen.

1. Klicken Sie auf ein Element auf Ihrer Seite. Wenn an der Position des Elements Empfehlungen verfügbar sind, klicken Sie auf **[!UICONTROL Ersetzen durch Recommendations]**, **[!UICONTROL Recommendations vor einfügen]** oder **[!UICONTROL Einfügen von Recommendations nach]**.

   Besucher Ihrer Site sehen den empfohlenen Inhalt nur, wenn sie sich für die Empfehlung qualifizieren. Besucher, die sich nicht für die Empfehlung qualifizieren, sehen Standardinhalte.

   ![Recommendations-Optionen](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Ersetzen durch Recommendations]**: Wenn Sie ein Element durch Empfehlungen ersetzen, wird der aktuelle Inhalt gelöscht und durch Ihre Empfehlungen ersetzt. Wenn Besucher Ihre Site besuchen und sich für die Empfehlung qualifizieren, sehen sie die empfohlenen Artikel im angegebenen Bereich anstelle des vorhandenen Inhalts.
   * **[!UICONTROL Recommendations vor einfügen]**: Beim Einfügen von Empfehlungen vor dem ausgewählten Element wird der empfohlene Inhalt vor diesem Element platziert. Je nach Seitenaufbau wird die Empfehlung oben oder links neben dem ausgewählten Element angezeigt.
   * **[!UICONTROL Einfügen von Recommendations nach]**: Beim Einfügen von Empfehlungen nach dem ausgewählten Element wird der empfohlene Inhalt nach diesem Element platziert. Je nach Seitenaufbau wird die Empfehlung unten oder rechts neben dem ausgewählten Element angezeigt.

   Die **[!UICONTROL Auswahl erweitern]** Mit dieser Option können Sie den ausgewählten Ort (übergeordneten Container) erweitern, um die gewünschten Seitenelemente einfacher zu identifizieren und einzuschließen.

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

   Kriterien werden in Form von Karten dargestellt, die Informationen zu dem jeweiligen Kriterium anzeigen. Standardmäßig wird die Variable [!UICONTROL Kriterien auswählen] -Bildschirm zeigt Kriterien an, die mit Ihrer vertikalen Branche und dem Seitentyp kompatibel sind, den Sie im vorherigen Schritt ausgewählt haben. Sie können diese Optionen ändern, wenn Sie andere Kriterien angezeigt haben möchten.

   >[!NOTE]
   >
   >Nicht jedes Kriterium wird auf jeder Seite korrekt ausgeführt. Die Seite oder Mbox muss die `entity.id` oder die `entity.categoryId` für die Empfehlungen zum aktuellen Element bzw. zur aktuellen Kategorie übergeben, um kompatibel zu sein. Allgemein ist es am besten, lediglich kompatible Kriterien anzuzeigen. Wenn Sie jedoch möchten, dass inkompatible Kriterien für die Aktivität verfügbar sind, heben Sie die Auswahl für die Option **[!UICONTROL Kompatibel]** auf. Die [!UICONTROL Kompatibel] -Option wird je nach Ihren Recommendations-Einstellungen möglicherweise nicht angezeigt ( **[!UICONTROL Recommendations]** > **[!UICONTROL Einstellungen]** > **[!UICONTROL Inkompatible Kriterien filtern]**). Weitere Informationen finden Sie unter [Einstellungen](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

   ![Dialogfeld „Kriterien auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Wenn Sie mehrere Kriterien auswählen, wird der Traffic gleichmäßig zwischen den ausgewählten Kriterien ausgewählt. Wenn Sie zum Beispiel zwei Kriterien auswählen und Ihre Aktivität zur Anzeige von Standardinhalt für 20 % der Aktivitätsteilnehmer konzipiert ist, sehen 40 % der Aktivitätsteilnehmer die Empfehlungen, die durch jedes der Kriterien kontrolliert werden. Es gibt keine Option zur Änderung der Prozentsätze für die einzelnen Kriterien.

   * Um nach einem vorhandenen Kriterium zu suchen (z. B. wenn viele Kriterienkarten angezeigt werden), geben Sie einen entsprechenden Suchtext in das Suchfeld ein, bis das gewünschte Kriterium angezeigt wird. Wählen Sie dieses dann aus und klicken Sie auf **[!UICONTROL Nächste]**.

     Einige Kriterien werden durch [!DNL Recommendations] bereitgestellt. Sie und Ihr Team können auch eigene Kriterien erstellen.

   * Um ein neues Kriterium zu erstellen, klicken Sie auf **[!UICONTROL Erstellen von Kriterien]** > **[!UICONTROL Erstellen von Kriterien]** und geben Sie dann die Informationen für die neuen Kriterien ein. Weitere Informationen zum Erstellen neuer Kriterien finden Sie unter [Erstellen von Kriterien](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * Sie können auch Kriterien in Sequenzen gruppieren. Um eine neue Kriteriensequenz zu erstellen, klicken Sie auf **[!UICONTROL Erstellen von Kriterien]** > **[!UICONTROL Kriteriensequenz erstellen]**. Siehe [Kriteriensequenz erstellen](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md) für weitere Informationen.

1. Klicks **[!UICONTROL Nächste]**.
1. [Entwurf auswählen](/help/main/c-recommendations/c-design-overview/design-overview.md).

   Ein Entwurf ist eine Vorlage, die das Aussehen der Orte auf Ihrer Seite festlegt. [!DNL Target] umfasst mehrere vorkonfigurierte Entwürfe. Sie können auch Ihre eigenen, benutzerdefinierten Entwürfe erstellen. Weitere Informationen finden Sie unter [Erstellen eines Entwurfs](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) und [Anpassen eines Entwurfs](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Dialogfeld „Entwurf auswählen“](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Jeder Entwurf beinhaltet eine grafische Darstellung des jeweiligen Entwurfs und Symbole, die zeigen, wie viele Ihrer aktiven und inaktiven Aktivitäten derzeit diesen Entwurf verwenden.

   * Um einen oder mehrere vorhandene Entwürfe auszuwählen, klicken Sie auf die Entwürfe und dann auf **[!UICONTROL Nächste]**.

     Wenn Sie mehrere Kriterien ausgewählt haben, können Sie lediglich einen Entwurf auswählen.

   * Um einen benutzerdefinierten Entwurf zu erstellen, klicken Sie auf **[!UICONTROL Design erstellen]** und geben Sie dann den Namen und den Code für das neue Design ein. Klicken Sie auf **[!UICONTROL Weiter]**, wählen Sie anschließend ein Bild aus oder laden Sie ein Bild hoch und klicken Sie dann auf **[!UICONTROL Fertig]** > **[!UICONTROL Fertig]**. Weitere Informationen zum Erstellen eines neuen Entwurfs finden Sie unter [Erstellen eines Entwurfs](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicks **[!UICONTROL Nächste]**.

   Sie haben auch die Möglichkeit, Ihren Empfehlungen Promotions hinzuzufügen. Weitere Informationen zum Hinzufügen von Vorwärts- und Rückwärts-Promotions finden Sie unter [Hinzufügen von Promotions](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   Im Bildschirm „VEC“ wird das Empfehlungsdesign Ihrer Seite angezeigt.

1. (Optional) Klicken Sie auf **[!UICONTROL Vorschau]** , um zu sehen, wie die Aktivität für Besucher aussehen wird.

   Im [!UICONTROL Vorschau]-Modus können Sie mit Ihren Empfehlungen interagieren, so wie es ein Besucher tun würde.

   Haben Sie die Vorschau der Empfehlungen abgeschlossen, klicken Sie auf **[!UICONTROL Erstellen]**.

1. Überprüfen Sie Ihre Empfehlung im VEC und klicken Sie dann auf **[!UICONTROL Nächste]**.

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
   * Sammlung ändern (neben der Bezeichnung [!UICONTROL Kriterien])
   * Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Entwurfscode anzeigen
   * Entwurf ändern oder entfernen

1. Klicken Sie auf **[!UICONTROL Weiter]**, wenn Sie fertig sind.
1. Geben Sie Ihre Aktivitätseinstellungen an.

   Geben Sie zum Beispiel einen Namen (erforderlich) und ein Ziel (optional) für die Aktivität ein. Weitere Informationen zu den Einstellungen finden Sie unter [Recommendations Activities-Einstellungen](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >Wenn Sie einen [!DNL Recommendation]-Aktivitätsnamen angeben, der bereits für eine andere Aktivität in [!DNL Recommendations Classic] vorhanden ist, wird die neue Aktivität noch einmal mit einem neuen Namen synchronisiert. Der neue Name ist der ursprüngliche Name, der mit einem Zeitstempel versehen wird, um ihn eindeutig zu machen. Dieser neue Name wird sowohl in [!DNL Target Standard/Premium] als auch in [!DNL Recommendations Classic] angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern und schließen]**.

   Für Ihre Aktivität wird eine Übersicht angezeigt.

   Auf der Seite [!UICONTROL Übersicht] können Sie:

   * die Aktivität aktivieren
   * die Aktivität bearbeiten
   * Freigeben der Aktivität für Ihren Experience Cloud-Feed
   * Aktivität überprüfen
   * Ihre Erlebnis-URLs ansehen
   * Daten herunterladen
   * den Prozentsatz der Teilnehmer ändern, denen das Kontrollerlebnis angezeigt wird
   * Details zu Kriterien ein- oder ausblenden
   * Code für Ihre Entwürfe ansehen

1. (Optional) Öffnen Sie die Seite [!UICONTROL Berichte], um den Bericht anzusehen, der die Leistung Ihrer [!DNL Recommendations]-Aktivität anzeigt.

1. (Optional) Öffnen Sie die [!UICONTROL Kollisionen] Seite zum Anzeigen einer beliebigen [Aktivitätskollisionen](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) möglicherweise eintreten.

   Kollisionen von Aktivitäten treten auf, wenn mehrere Aktivitäten Inhalte auf derselben Seite bereitstellen sollen. Dies kann zur Darstellung unerwarteter Inhalte führen.

## Schulungsvideo: Erstellen einer Recommendations-Aktivität (7:15) ![Tutorial-Badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
