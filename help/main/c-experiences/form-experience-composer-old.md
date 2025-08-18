---
keywords: Form-Based Experience Composer;Form-Based Composer;Verfeinerungen
description: Erfahren Sie, wie Sie den Adobe [!DNL Target] Form-basierten Experience Composer für die Erstellung nicht visueller Erlebnisse verwenden. Verwenden Sie diesen Composer, wenn VEC nicht verfügbar oder unpraktisch in der Anwendung ist.
title: Wie verwende ich den formularbasierten Experience Composer?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
source-git-commit: 2f86c9ee89b4e1698180f6b3dc9df393733eb780
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 37%

---

# Form-Based Experience Composer

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Oberfläche zur Erlebnis- und Angebotserstellung, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B Test]-, [!UICONTROL Experience Targeting]-, [!UICONTROL Automated Personalization]- und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn der [!UICONTROL Visual Experience Composer] (VEC) nicht verfügbar oder unpraktisch für die Verwendung ist. Beispielsweise können Sie den Form-Based Experience Composer verwenden, um Erlebnisse und Angebote für den Versand in E-Mails, Kiosks und Sprachassistenten zu erstellen.

Wenn Sie eine [!UICONTROL Recommendations] Aktivität erstellen, gibt es keine Erlebnisse. Wählen Sie Ihre Kriterien und Ihren Entwurf aus. Wenn Sie mehrere Kriterien oder Designs auswählen, generiert [!UICONTROL Target] automatisch die Erlebnisse.

1. Klicken Sie auf **[!UICONTROL Create Activity]** und wählen Sie dann den Aktivitätstyp aus, den Sie erstellen möchten.

   Die [!UICONTROL Form-Based Experience Composer] ist für [!UICONTROL A/B Test], [!UICONTROL Experience Targeting], [!UICONTROL Automated Personalization] und [!UICONTROL Recommendations] verfügbar.

1. Wählen Sie **[!UICONTROL Form]** im Dialogfeld [!UICONTROL Create Activity] aus.

1. (Bedingt) Wählen Sie einen Arbeitsbereich und eine Eigenschaft aus.

1. Klicken Sie auf **[!UICONTROL Next]**.

   Die [!UICONTROL Form-Based Experience Composer] wird geöffnet.

   ![location_refinements image](assets/location_refinements.png)

   Dieser Bildschirm unterscheidet sich, wenn Sie eine [!UICONTROL Recommendations] Aktivität erstellen. [!UICONTROL Recommendations] Aktivitäten umfassen keine Erlebnisse.

1. Benennen Sie die Aktivität, indem Sie auf &quot;[!UICONTROL Untitled Activity]&quot; klicken.
1. Wählen Sie einen Standort aus.

   Wenn Sie in das [!UICONTROL Select Location] klicken, wird eine Liste der verfügbaren Speicherorte angezeigt. Wählen Sie einen dieser Standorte aus.

   Sie können auch einen Standort eingeben, der hier nicht aufgelistet ist. Dies kann sich als nützlich erweisen, wenn die Mbox noch nicht erstellt oder auf einer Seite angezeigt wurde. Geben Sie den Namen des Orts ein. Seien Sie vorsichtig, wenn Sie einen Standort eingeben, der noch nicht vorhanden ist. Wenn die Schreibweise oder Groß-/Kleinschreibung nicht mit der Schreibweise oder Groß-/Kleinschreibung bei Mbox-Aufruf übereinstimmt, dann wird die Aktivität nicht bereitgestellt. Manuell eingegebene Speicherorte werden in der Liste der verfügbaren Speicherorte gespeichert. Wenn Sie das nächste Mal versuchen, einen manuell eingegebenen Speicherort auszuwählen, wird er in der Dropdown-Liste [!UICONTROL Select Location] für diese Aktivität verfügbar sein.

   >[!NOTE]
   >
   >Wenn Sie während der Erstellung einer Aktivität einen manuell eingegebenen Speicherort erstellen, wird nicht automatisch ein neuer Speicherort erstellt. Der Ortsname wird nur im Kontext der Aktivität gespeichert. Der Speicherort wird erstellt, wenn ein Aufruf zur Inhaltsbereitstellung erfolgt. Nach der Erstellung des Speicherorts ist er zur Verwendung in anderen Aktivitäten, zur Erstellung von Zielgruppen usw. verfügbar. aus der Dropdown-Liste der verfügbaren Speicherorte.

1. Klicken Sie auf **[!UICONTROL Add Audience Refinements]**, wählen Sie eine oder mehrere [Zielgruppe](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) für diese Aktivität aus und klicken Sie dann auf **[!UICONTROL Done]**.

   ![location_refinements_2 Bild](assets/location_refinements_2.png)

   In der [!UICONTROL Form-based Experience Composer] wurden Verfeinerungen durch die vollständige Funktionalität für Zielgruppen ersetzt. Verfeinerungen für vorhandene Aktivitäten wurden auf [Zielgruppen nur für Aktivitäten“ ](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

1. Wählen Sie den Inhaltstyp aus, der an diesem Standort angezeigt werden soll.

   ![form_content image](assets/form_content.png)

1. Geben Sie für den ausgewählten Content-Typ den Inhalt an.

   **HTML-Angebot ändern:** Wählen Sie ein HTML-Angebot.

   **Bildangebot ändern:** Wählen Sie ein in der Inhaltsbibliothek in Target gespeichertes Bild aus.

   Sie können außerdem einen Link zum Bild hinzufügen (Clickthrough, Ziel, Landing usw.)

   1. Klicken Sie auf [!UICONTROL Change Image Offer].
   1. Wählen Sie das gewünschte Bild aus und klicken Sie dann auf [!UICONTROL Edit Links].
   1. Geben Sie die gewünschte URL oder Seite auf Ihrer Site an und klicken Sie dann auf [!UICONTROL Update].

   **JSON-Angebot ändern:** Wählen Sie ein JSON-Angebot.

   **Experience Fragment ändern** Wählen Sie ein Experience Fragment aus. Weitere Informationen finden Sie unter [Experience Fragment](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

   **Umleitungsangebot ändern:** Wählen Sie ein Umleitungsangebot. Weitere Informationen finden Sie unter [Umleitungsangebote erstellen](/help/main/c-experiences/c-manage-content/offer-redirect.md).

   **Remote-Angebot ändern** Wählen Sie ein Remote-Angebot aus. Weitere Informationen finden Sie unter [Remote-Angebote erstellen](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

   **HTML-Angebot erstellen:**

   1. Klicken Sie auf [!UICONTROL Offers] und wählen Sie dann die Registerkarte [!UICONTROL Code Offers] aus.
   1. Klicken Sie auf [!UICONTROL Create] > [!UICONTROL HTML Offer].
   1. Geben Sie einen Angebotsnamen ein.
   1. Geben Sie im Feld „Code“ den HTML-Code ein oder kopieren Sie ihn dorthin.
   1. Klicken Sie auf [!UICONTROL Save].

   **JSON-Angebot erstellen:**

   1. Klicken Sie auf [!UICONTROL Offers] und wählen Sie dann die Registerkarte [!UICONTROL Code Offers] aus.
   1. Klicken Sie auf [!UICONTROL Create] > [!UICONTROL JSON Offer].
   1. Geben Sie einen Angebotsnamen ein.
   1. Schreiben Sie Ihren JSON-Code in das Feld „Code“ oder kopieren Sie ihn dorthin.
   1. Klicken Sie auf [!UICONTROL Save].

   **Empfehlung hinzufügen:**

   Für eine Recommendations -Aktivität bietet Ihnen die Dropdown-Liste Inhalt die [!UICONTROL Add Recommendation] Option. Klicken Sie auf **[!UICONTROL Add Recommendation]** und wählen Sie dann den Seitentyp aus. Folgen Sie den üblichen auf der Oberfläche angegebenen Schritten, um [eine Recommendations-Aktivität zu erstellen](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   Bei der Auswahl der Recommendations-Kriterien im formularbasierten Experience Composer gibt es jetzt einen direkten Link zur ausgewählten Kriterienkarte, damit Sie die Kriterien schnell und einfach bearbeiten können.

   ![change_criteria Bild](assets/change_criteria.png)

   Auf der Seite „Targeting“ des Drei-Schritte-Workflows zu Target:

   ![change_criteria_2 Bild](assets/change_criteria_2.png)

   **Angebotsentscheidung hinzufügen:**

   Fügen Sie einer [!DNL Adobe Journey Optimizer]-Aktivität ein in [!DNL Adobe Target] (AJO) erstelltes Angebot hinzu, um Ihren Besuchern auf Ihrer Website oder mobilen Site mithilfe von Offer Decisioning das beste dynamische Angebot und Erlebnis zu bieten. Diese Option ist nur für manuelle [!UICONTROL A/B Test] und [!UICONTROL Experience Targeting] (XT)-Aktivitäten verfügbar.

   Weitere Informationen finden Sie unter [Verwenden von Angebotsentscheidungen](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

1. (Optional, für [!UICONTROL A/B Test]-, [!UICONTROL Automated Personalization]- und [!UICONTROL Experience Targeting]-Aktivitäten) Um diesen Vorgang für weitere Standorte zu wiederholen, klicken Sie auf **[!UICONTROL Add Location]** und konfigurieren Sie den Standort und den Inhalt.
1. Klicken Sie auf **[!UICONTROL Next]** und führen Sie dann die für Ihren Aktivitätstyp üblichen Schritte zur Aktivitätserstellung aus.

* [Erstellen eines A/B-Tests](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [Erstellen einer Erlebnis-Targeting-Aktivität](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Recommendations-Aktivität erstellen](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Schulungsvideo: Formularbasierter Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

Im folgenden Video wird der Form-Based Experience Composer vorgeführt.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
