---
keywords: Remote-Angebot; Auswahlmatrix für Remote-Angebote; zwischengespeicherter Inhalt; dynamischer Inhalt; URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in Adobe verwenden. [!DNL Target] , um externe Inhalte (Inhalte in einem CMS oder einem anderen System) zu hosten. Erfahren Sie, warum Sie möglicherweise Remote-Angebote verwenden möchten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 48%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote dazu, außerhalb von [!DNL Adobe Target] [!DNL Target] Inhalt zu hosten, auf den zugreift und den das Tool für Benutzerwebseiten zur Verfügung stellt. Diese Inhalte können sich in einem Content Management (CMS) oder einem anderen System befinden, entweder aus Gründen der Benutzerfreundlichkeit oder aus Sicherheitsgründen.

>[!NOTE]
>
>Remote-Angebote können auf der [!UICONTROL Angebote] > [!UICONTROL Code-Angebote] oder in der [Forms-basierter Experience Composer](/help/main/c-experiences/form-experience-composer.md). Sie können keine Remote-Angebote im Visual Experience Composer (VEC) erstellen oder anwenden. Der Inhalt wird in die [!DNL Target] Anfragespeicherorte, sodass diese höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage.
>
>[!DNL Target Classic] verfügte über ähnliche Funktionen: [!UICONTROL Angebot auf Ihrer Seite] und [!UICONTROL Angebot außerhalb von Test&amp;Target].

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

* Wenn sich Ihr Angebot in derselben Domäne wie das [!DNL Target] -Anfragen mithilfe der [!UICONTROL Zwischengespeichert] -Option können Sie relative URLs zur Beschreibung Ihres Angebotorts verwenden.

   Beim Verschieben Ihrer Aktivität von den Vorbereitungsservern auf die Produktionsserver hat dieses Verfahren den Vorteil, dass ohne manuelles Ändern der URL automatisch auf den Inhalt zugegriffen werden kann.

* Sollten in Ihrem Test dynamisch vom Server generierte Daten enthalten sein, ist die Option [!UICONTROL Dynamisch] möglicherweise die richtige Wahl.
* Sollten Sie lediglich planen, die Darstellung des Inhalts Ihres bestehenden Remote-Angebots zu prüfen, verwenden Sie den [!UICONTROL Visual Experience Composer], um Aussehen und Eindruck des Inhalts anzupassen, der vom Inhaltsverwaltungssystem ausgegeben wird.
* Verwenden Sie die [Auswahlmatrix für Remote-Angebote](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um Ihnen bei der Auswahl des Angebots zu helfen, das für Ihren spezifischen Fall am besten geeignet ist. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Remote-Angebot über die Seite Code-Angebote erstellen

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.

   ![Angebote > Code-Angebote](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Remote-Angebot]**.

   ![Dialogfeld &quot;Remote-Angebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. Geben Sie den Typ Umleitungs-URL an.

   Siehe [Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch](#url-type) unten finden Sie weitere Informationen.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Remote-Angebot mit dem formularbasierten Experience Composer erstellen

1. Beim Erstellen einer Aktivität mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), wählen Sie den Speicherort aus, an dem die **[!UICONTROL Inhalt]** Abschnitt.

   ![Inhaltsbereich in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf **[!UICONTROL Standardinhalt]** Dropdown-Liste und klicken Sie auf **[!UICONTROL Remote-Angebot ändern]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Remote-Angebot]**.

   ![Dialogfeld &quot;Remote-Angebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. Geben Sie den Typ Umleitungs-URL an.

   Siehe [Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch](#url-type) unten finden Sie weitere Informationen.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch {#url-type}

Die folgenden Informationen helfen Ihnen dabei, die Unterschiede zwischen den beiden Optionen zu verstehen:

### Zwischengespeicherte URL

Der Inhalt eines zwischengespeicherten Remote-Angebots wird von [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt der Remote-URL ab und speichert ihn in [!DNL Target]. Laden Besucher die Seite mit einem Erlebnis, in dem ein Remote-Angebot enthalten ist, wird das Angebot von [!DNL Target] bereitgestellt.

Zwischengespeicherte Remote-Angebote bieten höhere Sicherheit, da sich jemand bei [!DNL Target] kann den Inhalt nicht ändern. Soll der Inhalt bearbeitet werden, müsste sich jemand im Inhaltsverwaltungssystem oder dem System anmelden, in dem der Inhalt gespeichert ist, und ihn dort bearbeiten.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### Dynamische URL

Ein dynamisches Remote-Angebot wird vom Inhaltsverwaltungssystem oder einem anderen System bereitgestellt, nicht von [!DNL Target].

Möglicherweise möchten Sie nicht, dass Inhalte regelmäßig in den Zwischenspeicher geladen und anschließend von [!DNL Target] bereitgestellt werden, wenn Besucher die Seite mit einem Erlebnis laden, in dem ein Remote-Angebot enthalten ist. Stattdessen möchten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise spezifische Informationen weitergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Parameter hinzufügen]** , um eine oder mehrere [!DNL Target] Anforderungen oder Anforderungsparameter.

## Verwenden von Remote-Angeboten in Aktivitäten

Sie müssen Remote-Angebote mithilfe des [!UICONTROL Form-Based Experience Composer]. Sie können derzeit keine Remote-Angebote mit dem VEC anwenden.

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebotserstellungsoberfläche, die beim Erstellen von Erlebnissen zur Verwendung in [!UICONTROL A/B-Tests], [!UICONTROL Erlebnis-Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Recommendations] Aktivitäten, wenn der Visual Experience Composer nicht verfügbar oder nicht praktisch zur Verwendung ist. Sie können beispielsweise die [!UICONTROL Form-Based Experience Composer] , um Erlebnisse zu erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Siehe [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) für detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste im **[!UICONTROL Inhalt]** und klicken Sie auf **[!UICONTROL Remote-Angebot ändern]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Wählen Sie das gewünschte Remote-Angebot aus dem [!UICONTROL Remote-Angebot auswählen] Dialogfeld und klicken Sie auf **[!UICONTROL Fertig]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebote {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird ausgeführt, nachdem Sie die Seite gerendert haben. Ein unsichtbarer iframe erfasst die Daten, kopiert sie aus dem Frame und fügt sie in die Seite ein, wobei die übergebenen Werte geladen werden.

![remote_offer_howitworks_2 image](assets/remote_offer_howitworks_2.jpeg)

## Auswahlmatrix für Remote-Angebote {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Mit der Auswahlmatrix für Remote-Angebote können Sie entscheiden, welcher Typ von Remote-Angebot festgelegt werden soll: [!UICONTROL Zwischengespeichert] oder [!UICONTROL Dynamisch].

| Funktion | Zwischengespeichert | Dynamisch |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle 2 Stunden im Cache gespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut      oder Relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird der formularbasierte Composer vorgestellt, mit dem Sie Remote-Angebote erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
