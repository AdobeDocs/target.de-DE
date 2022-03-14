---
keywords: Form-Based Experience Composer;Form-Based Composer;Verfeinerungen
description: Erfahren Sie, wie Sie die Adobe verwenden [!DNL Target] Form-Based Experience Composer für die Erstellung nicht visueller Erlebnisse. Verwenden Sie diesen Composer, wenn der VEC nicht verfügbar oder nicht praktisch zu verwenden ist.
title: Wie verwende ich den formularbasierten Experience Composer?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 46%

---

# Form-Based Experience Composer

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebotserstellungsoberfläche, die beim Erstellen von Erlebnissen zur Verwendung in [!UICONTROL A/B-Test], [!UICONTROL Erlebnis-Targeting], [!UICONTROL Automated Personalization]und [!UICONTROL Recommendations] Aktivitäten, wenn die [!UICONTROL Visual Experience Composer] (VEC) nicht verfügbar oder praktisch nicht. Sie können beispielsweise den formularbasierten Experience Composer verwenden, um Erlebnisse und Angebote für die Bereitstellung in E-Mails, Kiosks und Sprachassistenten zu erstellen.

Wenn Sie eine [!UICONTROL Recommendations] -Aktivität, gibt es keine Erlebnisse. Wählen Sie Ihre Kriterien und Ihren Entwurf aus. Wenn Sie mehrere Kriterien oder Entwürfe auswählen, [!UICONTROL Target] generiert automatisch die Erlebnisse.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]** und wählen Sie dann den Typ der Aktivität aus, die Sie erstellen möchten.

   Die [!UICONTROL Form-Based Experience Composer] ist verfügbar für [!UICONTROL A/B-Test], [!UICONTROL Erlebnis-Targeting], [!UICONTROL Automated Personalization]und [!UICONTROL Recommendations] Aktivitäten.

1. Auswählen **[!UICONTROL Formular]** von [!UICONTROL Aktivität erstellen] Dialogfeld.

1. (Bedingt) Wählen Sie einen Arbeitsbereich und eine Eigenschaft aus.

1. Klicken Sie auf **[!UICONTROL Weiter]**.

   Die [!UICONTROL Form-Based Experience Composer] geöffnet.

   ![](assets/location_refinements.png)

   Dieser Bildschirm unterscheidet sich bei der Erstellung eines [!UICONTROL Recommendations] Aktivität. [!UICONTROL Recommendations-Aktivitäten schließen keine Erlebnisse ein.]

1. Benennen Sie die Aktivität, indem Sie auf &quot;[!UICONTROL Unbenannte Aktivität].&quot;
1. Wählen Sie einen Standort aus.

   Wenn Sie auf die [!UICONTROL Standort auswählen] angezeigt, wird eine Liste der verfügbaren Orte angezeigt. Wählen Sie einen dieser Standorte aus.

   Sie können auch einen Standort eingeben, der hier nicht aufgelistet ist. Dies kann sich als nützlich erweisen, wenn die Mbox noch nicht erstellt oder auf einer Seite angezeigt wurde. Geben Sie den Namen des Orts ein. Seien Sie vorsichtig, wenn Sie einen Standort eingeben, der noch nicht vorhanden ist. Wenn die Schreibweise oder Groß-/Kleinschreibung nicht mit der Schreibweise oder Groß-/Kleinschreibung bei Mbox-Aufruf übereinstimmt, dann wird die Aktivität nicht bereitgestellt. Manuell eingegebene Orte werden in der Liste der verfügbaren Orte gespeichert. Wenn Sie das nächste Mal versuchen, einen manuell eingegebenen Speicherort auszuwählen, ist er im [!UICONTROL Standort auswählen] Dropdown-Liste für diese Aktivität.

   >[!NOTE]
   >
   >Wenn Sie während der Erstellung einer Aktivität einen manuell eingegebenen Ort erstellen, wird kein neuer Ort automatisch erstellt. Der Ortsname wird nur im Kontext der Aktivität gespeichert. Der Speicherort wird erstellt, wenn ein Inhaltsbereitstellungsaufruf erfolgt. Nach der Erstellung des Standorts ist er für die Verwendung in anderen Aktivitäten, die Erstellung von Zielgruppen usw. verfügbar. aus der Dropdown-Liste der verfügbaren Orte.

1. Klicken **[!UICONTROL Zielgruppenverfeinerungen hinzufügen]**, wählen Sie eine oder mehrere [audience](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) Klicken Sie für diese Aktivität auf **[!UICONTROL Fertig]**.

   ![](assets/location_refinements_2.png)

   Im [!UICONTROL Form-Based Experience Composer]wurden Verfeinerungen durch die volle Zielgruppenfunktionalität ersetzt. Verfeinerungen für vorhandene Aktivitäten wurden in  [Zielgruppen „Nur Aktivität“](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) migriert.

1. Wählen Sie den Inhaltstyp aus, der an diesem Standort angezeigt werden soll.

   ![](assets/form_content.png)

1. Geben Sie für den ausgewählten Content-Typ den Inhalt an.

   **HTML-Angebot ändern:** Wählen Sie ein HTML-Angebot.

   **Bildangebot ändern:** Wählen Sie ein in der Inhaltsbibliothek in Target gespeichertes Bild aus.

   Sie können außerdem einen Link zum Bild hinzufügen (Clickthrough, Ziel, Landing usw.)

   1. Klicken Sie auf [!UICONTROL Bildangebot ändern].
   1. Klicken Sie auf das gewünschte Bild und anschließend auf [!UICONTROL Links bearbeiten].
   1. Geben Sie die gewünschte URL oder Seite Ihrer Site an und klicken Sie auf [!UICONTROL Aktualisieren].

   **JSON-Angebot ändern:** Wählen Sie ein JSON-Angebot.

   **Erlebnisfragment ändern:** Wählen Sie ein Erlebnisfragment. Weitere Informationen finden Sie unter [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

   **Umleitungsangebot ändern:** Wählen Sie ein Umleitungsangebote. Weitere Informationen finden Sie unter [Erstellen von Umleitungsangeboten](/help/main/c-experiences/c-manage-content/offer-redirect.md).

   **Remote-Angebot ändern:** Wählen Sie ein Remote-Angebot. Weitere Informationen finden Sie unter [Remote-Angebote erstellen](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

   **HTML-Angebot erstellen:**

   1. Klicken Sie auf [!UICONTROL Angebote] und wählen Sie anschließend die Registerkarte [!UICONTROL Code-Angebote] aus.
   1. Klicken Sie auf [!UICONTROL Erstellen] > [!UICONTROL HTML-Angebot].
   1. Geben Sie einen Angebotsnamen ein.
   1. Geben Sie im Feld „Code“ den HTML-Code ein oder kopieren Sie ihn dorthin.
   1. Klicken Sie auf [!UICONTROL Speichern].

   **JSON-Angebot erstellen:**

   1. Klicken Sie auf [!UICONTROL Angebote] und wählen Sie anschließend die Registerkarte [!UICONTROL Code-Angebote] aus.
   1. Klicken Sie auf [!UICONTROL Erstellen] > [!UICONTROL JSON-Angebot].
   1. Geben Sie einen Angebotsnamen ein.
   1. Schreiben Sie Ihren JSON-Code in das Feld „Code“ oder kopieren Sie ihn dorthin.
   1. Klicken Sie auf [!UICONTROL Speichern].

   **Empfehlung hinzufügen:**

   Bei einer Recommendations-Aktivität bietet die Dropdown-Liste Inhalt die Option [!UICONTROL Empfehlung hinzufügen] -Option. Klicken Sie auf **[!UICONTROL Empfehlung hinzufügen]** und wählen Sie dann den Seitentyp aus. Folgen Sie den üblichen auf der Oberfläche angegebenen Schritten, um [eine Recommendations-Aktivität zu erstellen](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   Bei der Auswahl der Recommendations-Kriterien im formularbasierten Experience Composer gibt es jetzt einen direkten Link zur ausgewählten Kriterienkarte, damit Sie die Kriterien schnell und einfach bearbeiten können.

   ![](assets/change_criteria.png)

   Auf der Seite „Targeting“ des Drei-Schritte-Workflows zu Target:

   ![](assets/change_criteria_2.png)

   **Angebotsentscheidung hinzufügen:**

   Hinzufügen eines in erstellten Angebots [!DNL Adobe Journey Optimizer] (AJO) zu einem [!DNL Adobe Target] Aktivität , um Ihren Besuchern auf Ihrer Website oder auf Ihrer mobilen Site mithilfe von offer decisioning das beste dynamische Angebot und Erlebnis zu unterbreiten. Diese Option ist für manuelle [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) -Aktivitäten.

   Weitere Informationen finden Sie unter [Angebotsentscheidungen verwenden](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

1. (Optional, für [!UICONTROL A/B-Test], [!UICONTROL Automated Personalization]und [!UICONTROL Erlebnis-Targeting] Aktivitäten) Um diesen Vorgang für weitere Standorte zu wiederholen, klicken Sie auf **[!UICONTROL Ort hinzufügen]** und konfigurieren Sie den Ort und den Inhalt.
1. Klicken **[!UICONTROL Nächste]** und führen Sie dann die Schritte zur Aktivitätserstellung wie gewohnt für Ihren Aktivitätstyp aus.

* [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Erstellen einer Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

Im folgenden Video wird der Form-Based Experience Composer vorgeführt.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
