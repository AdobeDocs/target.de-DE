---
keywords: remote offer;remote offer selection matrix;cached content;dynamic content
description: Kann ich Remote-Angebot verwenden, um externe Inhalte zu hosten?
title: Remote-Angebote erstellen
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: d966727239d982116e3cd1c2925cb1627e2954ea
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 58%

---


# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote dazu, außerhalb von [!DNL Adobe Target] [!DNL Target] Inhalt zu hosten, auf den zugreift und den das Tool für Benutzerwebseiten zur Verfügung stellt. Diese Inhalte können sich in einem Content-Management (CMS) oder einem anderen System befinden, entweder aus Gründen der Benutzerfreundlichkeit oder aus Sicherheitsgründen.

>[!NOTE]
>
>Remote-Angebot können auf der Seite &quot;Angebote&quot;> &quot;Code-Angebot&quot;oder im [Forms-Based Experience Composer](/help/c-experiences/form-experience-composer.md) erstellt werden. Remote-Angebot können nicht im Visual Experience Composer (VEC) erstellt werden. Inhalte werden in die Anforderungsspeicherorte [!DNL Target] eingefügt, sodass diese wahrscheinlich nicht für eine globale [!DNL Target]-Anforderung geeignet sind.
>
>[!DNL Target Classic] verfügte über ähnliche Funktionen: [!UICONTROL Angebot auf Ihrer Seite] und [!UICONTROL Angebot außerhalb von Test&amp;Target].

Einige Beispiele für Remote-Angebote sind:

* Verschiedene Versionen Ihrer Querverkäufe
* Dynamische Warenkorbmeldungen
* Formulare
* Rechner
* Zinsänderungen

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

### Typ der zwischengespeicherten URL

Der Inhalt eines zwischengespeicherten Remote-Angebots wird von [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt der Remote-URL ab und speichert ihn in [!DNL Target]. Laden Besucher die Seite mit einem Erlebnis, in dem ein Remote-Angebot enthalten ist, wird das Angebot von [!DNL Target] bereitgestellt.

Zwischengespeicherte Remote-Angebot bieten eine höhere Sicherheit, da jemand, der bei [!DNL Target] angemeldet ist, den Inhalt nicht ändern kann. Soll der Inhalt bearbeitet werden, müsste sich jemand im Inhaltsverwaltungssystem oder dem System anmelden, in dem der Inhalt gespeichert ist, und ihn dort bearbeiten.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### Dynamischer URL-Typ

Ein dynamisches Remote-Angebot wird vom Inhaltsverwaltungssystem oder einem anderen System bereitgestellt, nicht von [!DNL Target].

Möglicherweise möchten Sie nicht, dass Inhalte regelmäßig in den Zwischenspeicher geladen und anschließend von [!DNL Target] bereitgestellt werden, wenn Besucher die Seite mit einem Erlebnis laden, in dem ein Remote-Angebot enthalten ist. Stattdessen möchten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise spezifische Informationen übermitteln, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder unterschiedlich) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Hinzufügen Parameter]** klicken, um eine oder mehrere [!DNL Target]-Anforderungen oder -Anforderungsparameter hinzuzufügen.

## Best Practices für die Verwendung von Remote-Angeboten {#section_7718512D08E14121B6F6B8C38134F4BC}

Best Practices für die Verwendung von Remote-Angeboten in Ihren Aktivitäten:

* Wenn sich Ihr Angebot in derselben Domäne wie die [!DNL Target]-Anforderungen befindet, können Sie mit der Option [!UICONTROL Zwischengespeichert] relative URLs zur Beschreibung Ihres Angebots verwenden.

   Beim Verschieben Ihrer Aktivität von den Vorbereitungsservern auf die Produktionsserver hat dieses Verfahren den Vorteil, dass ohne manuelles Ändern der URL automatisch auf den Inhalt zugegriffen werden kann.

* Sollten in Ihrem Test dynamisch vom Server generierte Daten enthalten sein, ist die Option [!UICONTROL Dynamisch] möglicherweise die richtige Wahl.
* Sollten Sie lediglich planen, die Darstellung des Inhalts Ihres bestehenden Remote-Angebots zu prüfen, verwenden Sie den [!UICONTROL Visual Experience Composer], um Aussehen und Eindruck des Inhalts anzupassen, der vom Inhaltsverwaltungssystem ausgegeben wird.
* Verwenden Sie die Auswahlmatrix für Remote-Angebot (unten), um das Angebot auszuwählen, das für den jeweiligen Fall am besten geeignet ist. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

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