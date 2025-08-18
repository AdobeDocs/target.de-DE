---
keywords: Remote-Angebot;Remote-Angebotsauswahlmatrix;zwischengespeicherte Inhalte;dynamischer Inhalt;URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in Adobe verwenden [!DNL Target]  um externe Inhalte (Inhalte in einer CMS oder einem anderen System) zu hosten. Finden Sie heraus, warum Sie Remote-Angebote verwenden sollten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 28%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote dazu, außerhalb von [!DNL Adobe Target] [!DNL Target] Inhalt zu hosten, auf den zugreift und den das Tool für Benutzerwebseiten zur Verfügung stellt. Diese Inhalte können sich aus Gründen der Benutzerfreundlichkeit oder aus Sicherheitsgründen in einem Content-Management-System (CMS) oder einem anderen System befinden.

>[!NOTE]
>
>Remote-Angebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer erstellt ](/help/main/c-experiences/form-experience-composer.md). Remote-Angebote können nicht im Visual Experience Composer (VEC) erstellt oder angewendet werden. Inhalte werden an den [!DNL Target] Anfragespeicherorten eingefügt, sodass diese wahrscheinlich nicht für eine globale [!DNL Target]-Anfrage geeignet sind.
>
>[!DNL Target Classic] enthielt ähnliche Funktionen: [!UICONTROL Offer on Your Site] und [!UICONTROL Offer Outside Test&Target].

Einige Beispiele für Remote-Angebote sind:

* Verschiedene Versionen Ihrer Querverkäufe
* Dynamische Warenkorbmeldungen
* Formulare
* Rechner
* Zinsänderungen
* E-Mails
* Kiosks
* Sprachassistenten

## Best Practices für die Verwendung von Remote-Angeboten {#section_7718512D08E14121B6F6B8C38134F4BC}

Best Practices für die Verwendung von Remote-Angeboten in Ihren Aktivitäten:

* Wenn sich Ihr Angebot in derselben Domain wie die [!DNL Target]-Anfragen befindet, können Sie mit der Option [!UICONTROL Cached] relative URLs zur Beschreibung Ihres Angebotsspeicherorts verwenden.

  Beim Verschieben Ihrer Aktivität von den Vorbereitungsservern auf die Produktionsserver hat dieses Verfahren den Vorteil, dass ohne manuelles Ändern der URL automatisch auf den Inhalt zugegriffen werden kann.

* Wenn Ihr Test Daten umfasst, die von Ihrem Server dynamisch generiert wurden, ist die Option [!UICONTROL Dynamic] möglicherweise die richtige Wahl.
* Wenn Sie nur das Erscheinungsbild Ihrer vorhandenen Remote-Angebotsinhalte testen möchten, verwenden Sie die [!UICONTROL Visual Experience Composer], um das Erscheinungsbild der Inhalte zu ändern, die vom Content-Management-System zurückgegeben werden.
* Verwenden Sie die [Remote-Angebotsauswahlmatrix](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um das Angebot auszuwählen, das für Ihren spezifischen Fall am besten geeignet ist. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Erstellen eines Remote-Angebots über die Seite „Code-Angebote“

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.

   ![Angebote > Angebote codieren](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Dialogfeld „Remote-Angebot erstellen“](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der [!UICONTROL Assets] zu finden.

1. Geben Sie den Umleitungs-URL-Typ an.

   Weitere Informationen finden [ unter „Umleitungs-URL-Typ: zwischengespeichert ](#url-type) dynamisch“.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Remote-Angebot mit dem formularbasierten Experience Composer erstellen

1. Wählen Sie beim Erstellen einer Aktivität mit [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, um den Abschnitt &quot;**[!UICONTROL Content]**&quot; anzuzeigen.

   ![Inhaltsabschnitt in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf die Dropdown-Liste **[!UICONTROL Default Content]** und dann auf **[!UICONTROL Change Remote Offer]**.

   ![Remote-Angebotsoption ändern](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Dialogfeld „Remote-Angebot erstellen“](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der [!UICONTROL Assets] zu finden.

1. Geben Sie den Umleitungs-URL-Typ an.

   Weitere Informationen finden [ unter „Umleitungs-URL-Typ: zwischengespeichert ](#url-type) dynamisch“.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch {#url-type}

Die folgenden Informationen helfen Ihnen, die Unterschiede zwischen den beiden Optionen zu verstehen:

### Zwischengespeicherte URL

Der Inhalt für ein zwischengespeichertes Remote-Angebot wird aus [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt von der Remote-URL ab und speichert dann den Inhalt in [!DNL Target]. Wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält, wird das Angebot von [!DNL Target] bereitgestellt.

Zwischengespeicherte Remote-Angebote bieten mehr Sicherheit, da jemand, der sich bei angemeldet hat, den Inhalt nicht ändern [!DNL Target]. Soll der Inhalt bearbeitet werden, müsste sich jemand im Content-Management-System oder dem System anmelden, in dem der Inhalt gespeichert ist, und ihn dort bearbeiten.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### Dynamische URL

Ein dynamisches Remote-Angebot wird vom Content-Management- oder anderen System und nicht von [!DNL Target] aus bereitgestellt.

Möglicherweise möchten Sie nicht, dass der Inhalt regelmäßig zwischengespeichert und dann von [!DNL Target] bereitgestellt wird, wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält. Stattdessen sollten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise bestimmte Informationen übergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Add Parameter]** klicken, um eine oder mehrere [!DNL Target] Anfragen oder Anfrageparameter hinzuzufügen.

## Remote-Angebote in Aktivitäten verwenden

Sie müssen Remote-Angebote mithilfe der [!UICONTROL Form-Based Experience Composer] anwenden. Sie können derzeit keine Remote-Angebote mit dem VEC anwenden.

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten. Diese Erlebnisse können in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Recommendations]-Aktivitäten genutzt werden, wenn der Visual Experience Composer nicht verfügbar oder unpraktisch in der Anwendung ist. Beispielsweise können Sie die [!UICONTROL Form-Based Experience Composer] verwenden, um Erlebnisse zu erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) finden Sie detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Speicherort an und fügen Sie gegebenenfalls Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdown-Liste im Abschnitt **[!UICONTROL Content]** und dann auf **[!UICONTROL Change Remote Offer]**.

   ![Remote-Angebotsoption ändern](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Wählen Sie das gewünschte Remote-Angebot aus dem [!UICONTROL Select Remote Offer] Dialogfeld aus und klicken Sie dann auf **[!UICONTROL Done]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebote {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird ausgeführt, nachdem Sie die Seite gerendert haben. Ein unsichtbarer iframe sammelt die Daten, kopiert sie aus dem Frame und fügt sie auf der Seite ein, wobei die übergebenen Werte geladen werden.

![remote_offer_howitworks_2 Bild](assets/remote_offer_howitworks_2.jpeg)

## Remote-Angebotsauswahlmatrix {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Die Matrix zur Remote-Angebotsauswahl hilft Ihnen bei der Entscheidung, welche Art von Remote-Angebot ausgewählt werden soll: [!UICONTROL Cached] oder [!UICONTROL Dynamic].

| Funktion | Zwischengespeichert | Dynamisch |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle 2 Stunden im Cache gespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut oder relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |

## Schulungsvideo: Formularbasierter Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video erhalten Sie eine Demo des formularbasierten Composers, mit dem Sie Remote-Angebote erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
