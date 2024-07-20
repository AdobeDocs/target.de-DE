---
keywords: Remote-Angebot; Auswahlmatrix für Remote-Angebote; zwischengespeicherter Inhalt; dynamischer Inhalt; URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in Adobe [!DNL Target] verwenden können, um externe Inhalte (Inhalte in einem CMS oder einem anderen System) zu hosten. Erfahren Sie, warum Sie möglicherweise Remote-Angebote verwenden möchten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 28%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote dazu, außerhalb von [!DNL Adobe Target] [!DNL Target] Inhalt zu hosten, auf den zugreift und den das Tool für Benutzerwebseiten zur Verfügung stellt. Diese Inhalte können sich in einem Content Management (CMS) oder einem anderen System befinden, entweder aus Gründen der Benutzerfreundlichkeit oder aus Sicherheitsgründen.

>[!NOTE]
>
>Remote-Angebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) erstellt werden. Sie können keine Remote-Angebote im Visual Experience Composer (VEC) erstellen oder anwenden. Inhalte werden in die [!DNL Target] -Anfragespeicherorte eingefügt, sodass sie höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage geeignet sind.
>
>[!DNL Target Classic] verfügte über ähnliche Funktionen: [!UICONTROL Offer on Your Site] und [!UICONTROL Offer Outside Test&Target].

Einige Beispiele für Remote-Angebote sind:

* Verschiedene Versionen Ihrer Querverkäufe
* Dynamische Warenkorbmeldungen
* Formulare
* Rechner
* Zinsänderungen
* E-Mails
* Kiosk
* Sprachassistenten

## Best Practices für die Verwendung von Remote-Angeboten {#section_7718512D08E14121B6F6B8C38134F4BC}

Best Practices für die Verwendung von Remote-Angeboten in Ihren Aktivitäten:

* Wenn sich Ihr Angebot in derselben Domäne wie die [!DNL Target] -Anforderungen befindet, können Sie mit der Option [!UICONTROL Cached] relative URLs für die Beschreibung Ihres Angebotsortes verwenden.

  Beim Verschieben Ihrer Aktivität von den Vorbereitungsservern auf die Produktionsserver hat dieses Verfahren den Vorteil, dass ohne manuelles Ändern der URL automatisch auf den Inhalt zugegriffen werden kann.

* Wenn Ihr Test dynamisch von Ihrem Server generierte Daten umfasst, kann die Option [!UICONTROL Dynamic] die richtige Wahl sein.
* Wenn Sie nur das Erscheinungsbild Ihres vorhandenen Remote-Angebotsinhalts testen möchten, verwenden Sie den [!UICONTROL Visual Experience Composer] , um das Erscheinungsbild des Inhalts zu ändern, der vom Content Management System zurückgegeben wird.
* Verwenden Sie die [Auswahlmatrix für Remote-Angebote](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um das für Ihren spezifischen Fall am besten geeignete Angebot auszuwählen. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Remote-Angebot über die Seite Code-Angebote erstellen

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.

   ![Angebote > Code-Angebote](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Dialogfeld &quot;Remote-Angebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der [!UICONTROL Assets] -Bibliothek.

1. Geben Sie den Typ Umleitungs-URL an.

   Weitere Informationen finden Sie unter [Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch](#url-type) weiter unten.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Remote-Angebot mit dem formularbasierten Experience Composer erstellen

1. Wählen Sie beim Erstellen einer Aktivität mit dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Content]** angezeigt werden soll.

   ![Inhaltsabschnitt im formularbasierten Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf die Dropdownliste **[!UICONTROL Default Content]** und dann auf **[!UICONTROL Change Remote Offer]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Dialogfeld &quot;Remote-Angebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der [!UICONTROL Assets] -Bibliothek.

1. Geben Sie den Typ Umleitungs-URL an.

   Weitere Informationen finden Sie unter [Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch](#url-type) weiter unten.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch {#url-type}

Die folgenden Informationen helfen Ihnen dabei, die Unterschiede zwischen den beiden Optionen zu verstehen:

### Zwischengespeicherte URL

Der Inhalt eines zwischengespeicherten Remote-Angebots wird von [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt an der Remote-URL ab und speichert ihn dann in [!DNL Target]. Wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält, wird das Angebot von [!DNL Target] bereitgestellt.

Zwischengespeicherte Remote-Angebote bieten verbesserte Sicherheit, da jemand, der sich bei [!DNL Target] angemeldet hat, den Inhalt nicht ändern kann. Soll der Inhalt bearbeitet werden, müsste sich jemand im Inhaltsverwaltungssystem oder dem System anmelden, in dem der Inhalt gespeichert ist, und ihn dort bearbeiten.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### Dynamische URL

Ein dynamisches Remote-Angebot wird vom Content Management oder einem anderen System bereitgestellt und nicht von [!DNL Target].

Möglicherweise möchten Sie nicht, dass Inhalte regelmäßig zwischengespeichert und dann von [!DNL Target] bereitgestellt werden, wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält. Stattdessen möchten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise spezifische Informationen weitergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Add Parameter]** klicken, um eine oder mehrere [!DNL Target] Anforderungen oder Anforderungsparameter hinzuzufügen.

## Verwenden von Remote-Angeboten in Aktivitäten

Sie müssen Remote-Angebote mit dem [!UICONTROL Form-Based Experience Composer] anwenden. Sie können derzeit keine Remote-Angebote mit dem VEC anwenden.

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting]- (XT), [!UICONTROL Automated Personalization]- (AP) und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn der Visual Experience Composer nicht verfügbar oder praktisch zur Verwendung nicht verfügbar ist. Beispielsweise können Sie mit dem [!UICONTROL Form-Based Experience Composer] Erlebnisse erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Detaillierte schrittweise Anweisungen finden Sie unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) .

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste im Abschnitt **[!UICONTROL Content]** und dann auf **[!UICONTROL Change Remote Offer]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Wählen Sie das gewünschte Remote-Angebot im Dialogfeld [!UICONTROL Select Remote Offer] aus und klicken Sie dann auf **[!UICONTROL Done]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebote {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird ausgeführt, nachdem Sie die Seite gerendert haben. Ein unsichtbarer iframe erfasst die Daten, kopiert sie aus dem Frame und fügt sie in die Seite ein, wobei die übergebenen Werte geladen werden.

![remote_offer_howitworks_2 image](assets/remote_offer_howitworks_2.jpeg)

## Auswahlmatrix für Remote-Angebote {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Die Auswahlmatrix für Remote-Angebote hilft Ihnen bei der Entscheidung, welchen Typ von Remote-Angebot Sie wählen sollten: [!UICONTROL Cached] oder [!UICONTROL Dynamic].

| Funktion | Zwischengespeichert | Dynamisch |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle 2 Stunden im Cache gespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut oder Relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird der formularbasierte Composer vorgestellt, mit dem Sie Remote-Angebote erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
