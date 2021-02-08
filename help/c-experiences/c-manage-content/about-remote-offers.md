---
keywords: Remote-Angebot;Auswahlmatrix für Remote-Angebote;Cache-Inhalt;Dynamischer Inhalt;URL-Typ
description: Erfahren Sie, wie Sie mit Remote-Angeboten in Adobe Target externe Inhalte (Inhalte in einem CMS oder einem anderen System) hosten können. Erfahren Sie, warum Sie möglicherweise Remote-Angebot verwenden möchten.
title: Wie erstelle ich Remote-Angebot?
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote dazu, außerhalb von [!DNL Adobe Target] [!DNL Target] Inhalt zu hosten, auf den zugreift und den das Tool für Benutzerwebseiten zur Verfügung stellt. Diese Inhalte können sich in einem Content-Management (CMS) oder einem anderen System befinden, entweder aus Gründen der Benutzerfreundlichkeit oder aus Sicherheitsgründen.

>[!NOTE]
>
>Remote-Angebot können auf der Seite [!UICONTROL Angebot] > [!UICONTROL Code-Angebot] oder im [Forms-basierten Experience Composer](/help/c-experiences/form-experience-composer.md) erstellt werden. Sie können keine Remote-Angebot im Visual Experience Composer (VEC) erstellen oder anwenden. Inhalte werden in die Anforderungsspeicherorte [!DNL Target] eingefügt, sodass diese wahrscheinlich nicht für eine globale [!DNL Target]-Anforderung geeignet sind.
>
>[!DNL Target Classic] verfügte über ähnliche Funktionen: [!UICONTROL Angebot auf Ihrer Seite] und [!UICONTROL Angebot außerhalb von Test&amp;Target].

Einige Beispiele für Remote-Angebote sind:

* Verschiedene Versionen Ihrer Querverkäufe
* Dynamische Warenkorbmeldungen
* Formulare
* Rechner
* Zinsänderungen
* E-Mails
* Kioske
* Sprachassistenten

## Best Practices für die Verwendung von Remote-Angeboten {#section_7718512D08E14121B6F6B8C38134F4BC}

Best Practices für die Verwendung von Remote-Angeboten in Ihren Aktivitäten:

* Wenn sich Ihr Angebot in derselben Domäne wie die [!DNL Target]-Anforderungen befindet, können Sie mit der Option [!UICONTROL Zwischengespeichert] relative URLs zur Beschreibung Ihres Angebots verwenden.

   Beim Verschieben Ihrer Aktivität von den Vorbereitungsservern auf die Produktionsserver hat dieses Verfahren den Vorteil, dass ohne manuelles Ändern der URL automatisch auf den Inhalt zugegriffen werden kann.

* Sollten in Ihrem Test dynamisch vom Server generierte Daten enthalten sein, ist die Option [!UICONTROL Dynamisch] möglicherweise die richtige Wahl.
* Sollten Sie lediglich planen, die Darstellung des Inhalts Ihres bestehenden Remote-Angebots zu prüfen, verwenden Sie den [!UICONTROL Visual Experience Composer], um Aussehen und Eindruck des Inhalts anzupassen, der vom Inhaltsverwaltungssystem ausgegeben wird.
* Verwenden Sie die [Auswahlmatrix für Remote-Angebot](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um das für Ihren spezifischen Fall am besten geeignete Angebot auszuwählen. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Ein Remote-Angebot auf der Seite &quot;Code-Angebot&quot;erstellen

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.

   ![Angebote > Code-Angebote](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Remote-Angebot]**.

   ![Remote-Angebot erstellen, Dialogfeld](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. Geben Sie den Typ der Umleitungs-URL an.

   Siehe [Umleitungs-URL-Typ: Zwischengespeichert oder Dynamisch](#url-type) unten für weitere Informationen.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Remote-Angebote mit dem Form-Based Experience Composer erstellen

1. Wählen Sie beim Erstellen einer Aktivität mit dem [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Inhalt]** angezeigt werden soll.

   ![Inhaltsabschnitt im Form-Based Experience Composer](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf die Dropdown-Liste **[!UICONTROL Standardinhalt]** und dann auf **[!UICONTROL Remote-Angebot ändern]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]** > **[!UICONTROL Remote-Angebot]**.

   ![Remote-Angebot erstellen, Dialogfeld](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. Geben Sie den Typ der Umleitungs-URL an.

   Siehe [Umleitungs-URL-Typ: Zwischengespeichert oder Dynamisch](#url-type) unten für weitere Informationen.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch {#url-type}

Die folgenden Informationen helfen Ihnen, die Unterschiede zwischen den beiden Optionen zu verstehen:

### Zwischengespeicherte URL

Der Inhalt eines zwischengespeicherten Remote-Angebots wird von [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt der Remote-URL ab und speichert ihn in [!DNL Target]. Laden Besucher die Seite mit einem Erlebnis, in dem ein Remote-Angebot enthalten ist, wird das Angebot von [!DNL Target] bereitgestellt.

Zwischengespeicherte Remote-Angebot bieten eine höhere Sicherheit, da jemand, der bei [!DNL Target] angemeldet ist, den Inhalt nicht ändern kann. Soll der Inhalt bearbeitet werden, müsste sich jemand im Inhaltsverwaltungssystem oder dem System anmelden, in dem der Inhalt gespeichert ist, und ihn dort bearbeiten.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### Dynamische URL

Ein dynamisches Remote-Angebot wird vom Inhaltsverwaltungssystem oder einem anderen System bereitgestellt, nicht von [!DNL Target].

Möglicherweise möchten Sie nicht, dass Inhalte regelmäßig in den Zwischenspeicher geladen und anschließend von [!DNL Target] bereitgestellt werden, wenn Besucher die Seite mit einem Erlebnis laden, in dem ein Remote-Angebot enthalten ist. Stattdessen möchten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise spezifische Informationen übermitteln, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder unterschiedlich) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Hinzufügen Parameter]** klicken, um eine oder mehrere [!DNL Target]-Anforderungen oder -Anforderungsparameter hinzuzufügen.

## Remote-Angebot in Aktivitäten verwenden

Sie müssen Remote-Angebot mit dem [!UICONTROL Form-Based Experience Composer] anwenden. Sie können derzeit keine Remote-Angebot mit VEC anwenden.

Der [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebot-Erstellungsoberfläche, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B-Tests], [!UICONTROL Erlebnis-Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Recommendations nützlich ist. a10/> Aktivitäten, bei denen der Visual Experience Composer nicht verfügbar oder nicht einsetzbar ist. ] Sie können beispielsweise den [!UICONTROL Form-Based Experience Composer] verwenden, um Erlebnisse zu erstellen, die Remote-Angebot verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Detaillierte Anleitungen finden Sie unter [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

1. Geben Sie den gewünschten Speicherort an und fügen Sie bei Bedarf Audiencen hinzu.

1. Klicken Sie im Abschnitt **[!UICONTROL Content]** auf die Dropdown-Liste und dann auf **[!UICONTROL Remote-Angebot ändern]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Wählen Sie das gewünschte Remote-Angebot im Dialogfeld [!UICONTROL Remote-Angebot] auswählen und klicken Sie dann auf **[!UICONTROL Fertig]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebot {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird nach dem Rendern der Seite ausgeführt. Ein unsichtbarer iframe sammelt die Daten, kopiert sie aus dem Frame und fügt sie auf der Seite ein und lädt die übergebenen Werte.

![](assets/remote_offer_howitworks_2.jpeg)

## Auswahlmatrix für Remote-Angebot {#reference_B23BEDD29DDD47709A7651AFD27E776B}

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

## Schulungsvideo: Form-Based Composer ![Tutorial badge](/help/assets/tutorial.png)

In diesem Video wird eine Demo des formularbasierten Composers gezeigt, mit dem Sie Remote-Angebot erstellen können.

* Aktivität mithilfe von Form-Based Experience Composer erstellen
* Wann Form-Based Experience Composer und wann Visual Experience Composer verwendet werden sollte
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)