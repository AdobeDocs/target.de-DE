---
keywords: Remote-Angebot; zwischengespeicherter Inhalt; dynamischer Inhalt; URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in [!DNL Target] , um externe Inhalte (Inhalte in einem CMS oder einem anderen System) zu hosten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
source-git-commit: 26cb9d6a2359714f41acaf91c6e26a7e0ac93238
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 20%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote dazu, außerhalb von [!DNL Adobe Target] [!DNL Target] Inhalt zu hosten, auf den zugreift und den das Tool für Benutzerwebseiten zur Verfügung stellt. Diese Inhalte können sich in einem Content Management (CMS) oder einem anderen System befinden, entweder aus Gründen der Benutzerfreundlichkeit oder aus Sicherheitsgründen.

>[!NOTE]
>
>Dieser Artikel enthält Informationen zu Aktualisierungen des [!DNL Target] -Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Die [!DNL Adobe Target] -Team ermöglicht oft neuen Funktionen für ausgewählte Kunden zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen in Zukunft für alle Kunden aktiviert [!DNL Target Standard/Premium] veröffentlicht und in den Versionshinweisen angekündigt.

Remote-Angebote können auf der [!UICONTROL Offers] > [!UICONTROL Code Offers] oder in der [Forms-basierter Experience Composer](/help/main/c-experiences/form-experience-composer.md). Remote-Angebote können nicht im [!UICONTROL Visual Experience Composer] (VEC). Der Inhalt wird in die [!DNL Target] -Anfragespeicherorte anfordern, sodass diese Orte höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage.

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

* Wenn sich Ihr Angebot in derselben Domäne wie das [!DNL Target] -Anfragen mithilfe der [!UICONTROL Cached] -Option können Sie relative URLs zur Beschreibung Ihres Angebotorts verwenden.

  Das bedeutet, dass beim Verschieben Ihrer Aktivität von Ihren Staging-Servern in die Produktion der Inhalt automatisch zugänglich ist, ohne die URL manuell ändern zu müssen.

* Wenn Ihr Test Daten umfasst, die dynamisch von Ihrem Server generiert wurden, wird die [!UICONTROL Dynamic] -Option die richtige Wahl sein.
* Wenn Sie nur das Erscheinungsbild Ihres vorhandenen Remote-Angebotsinhalts testen möchten, verwenden Sie die [!UICONTROL Visual Experience Composer] , um das Erscheinungsbild des Inhalts zu ändern, der vom Content Management System zurückgegeben wird.
* Verwenden Sie die [Auswahlmatrix für Remote-Angebote](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um Ihnen bei der Auswahl des Angebots zu helfen, das für Ihren spezifischen Fall am besten geeignet ist. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Erstellen Sie ein Remote-Angebot aus dem [!UICONTROL Code Offers] page

1. Klicks **[!UICONTROL Offers]** und wählen Sie dann die **[!UICONTROL Code Offers]** Registerkarte.

   ![Angebote > Code-Angebote](/help/main/c-experiences/c-manage-content/assets/offers-code-offers-new.png)

1. Klicks **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

   ![Dialogfeld &quot;Remote-Angebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui_new.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell im [!UICONTROL Assets] -Bibliothek.

1. (Bedingt) Wenn Sie eine [Target Premium-Konto](/help/main/c-intro/intro.md#premium), wählen Sie die gewünschte [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geben Sie den Typ der Umleitungs-URL an.

   Siehe [Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch](#url-type) unten finden Sie weitere Informationen.

1. Geben Sie die absolute Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Erstellen Sie ein Remote-Angebot mit dem [!UICONTROL Form-Based Experience Composer]

1. Beim Erstellen einer Aktivität mit dem [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md), wählen Sie den Speicherort aus, an dem die **[!UICONTROL Content]** Abschnitt.

   ![Inhaltsabschnitt im formularbasierten Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klicken Sie auf **[!UICONTROL Default Content]** Dropdown-Liste und klicken Sie auf **[!UICONTROL Change Remote Offer]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klicks **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Dialogfeld &quot;Remote-Angebot erstellen&quot;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell im [!UICONTROL Assets] -Bibliothek.

1. Geben Sie den Typ der Umleitungs-URL an.

   Siehe [Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch](#url-type) unten finden Sie weitere Informationen.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Umleitungs-URL-Typ: Zwischengespeichert oder dynamisch {#url-type}

Die folgenden Informationen helfen Ihnen dabei, die Unterschiede zwischen den beiden Optionen zu verstehen:

### Zwischengespeicherte URL

Der Inhalt eines zwischengespeicherten Remote-Angebots wird von [!DNL Target].

alle zwei Stunden, [!DNL Target] ruft den Inhalt an der Remote-URL ab und speichert ihn dann in [!DNL Target]. Wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält, [!DNL Target] liefert das Angebot.

Zwischengespeicherte Remote-Angebote bieten höhere Sicherheit, da sich jemand bei [!DNL Target] kann den Inhalt nicht ändern. Um den Inhalt zu ändern, muss jemand protokollieren oder ein anderes System verwenden und den Inhalt dort ändern.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### Dynamische URL

Ein dynamisches Remote-Angebot wird vom Content Management oder einem anderen System bereitgestellt und nicht von [!DNL Target].

Möglicherweise möchten Sie nicht, dass Inhalte regelmäßig zwischengespeichert und dann von [!DNL Target] wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält. Stattdessen möchten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise spezifische Informationen weitergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Add Parameter]** , um eine oder mehrere [!DNL Target] Anforderungen oder Anforderungsparameter.

## Verwenden von Remote-Angeboten in Aktivitäten

Sie müssen Remote-Angebote mithilfe des [!UICONTROL Form-Based Experience Composer]. Remote-Angebote können derzeit nicht mit der [!UICONTROL Visual Experience Composer] (VEC).

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Erlebnis- und Angebotserstellungsoberfläche, die beim Erstellen von Erlebnissen zur Verwendung in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) und [!UICONTROL Recommendations] Aktivitäten, wenn die [!UICONTROL Visual Experience Composer] nicht verfügbar oder praktikabel. Sie können beispielsweise die [!UICONTROL Form-Based Experience Composer] , um Erlebnisse zu erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Siehe [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) für detaillierte Schritt-für-Schritt-Anweisungen.

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste im **[!UICONTROL Content]** und klicken Sie auf **[!UICONTROL Change Remote Offer]**.

   ![Option &quot;Remote-Angebot ändern&quot;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Wählen Sie das gewünschte Remote-Angebot aus dem [!UICONTROL Select Remote Offer] Dialogfeld und klicken Sie auf **[!UICONTROL Done]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebote {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird ausgeführt, nachdem Sie die Seite gerendert haben. Ein unsichtbarer iFrame erfasst die Daten, kopiert sie aus dem Frame und fügt sie in die Seite ein, wodurch die übergebenen Werte geladen werden.

![remote_offer_howitworks_2 image](assets/remote_offer_howitworks_2.jpeg)

1. Der Browser des Besuchers fordert eine Seite von Ihrem Server an.

2. Browser rendert die Seite, einschließlich mboxes.

3. `mboxCreate` -Aufruf enthält Parameter, die zum Rendern dynamischer Inhalte erforderlich sind.

4. [!DNL Target] gibt URL mit dem Speicherort des dynamischen Inhalts und seiner Parameter zurück. Legt einen iFrame im mbox-Bereich fest.

5. Browser fordert URL an und rendert in der Seite.

## Auswahlmatrix für Remote-Angebote {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Die Auswahlmatrix für Remote-Angebote hilft Ihnen bei der Entscheidung, welcher Typ von Remote-Angebot ausgewählt werden soll: [!UICONTROL Cached] oder [!UICONTROL Dynamic].

| Funktion | Zwischengespeichert | Dynamisch |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle zwei Stunden zwischengespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut oder Relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |

## Schulungsvideo: Form-Based Composer ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird eine Demo der [!UICONTROL Form-Based Experience Composer], mit denen Sie Remote-Angebote erstellen können.

* Erstellen Sie eine Aktivität mit der [!UICONTROL Form-Based Experience Composer]
* Verwendungszeitpunkt [!UICONTROL Form-Based Experience Composer] im Vergleich zur [!UICONTROL Visual Experience Composer]
* Verfeinerungen zur Ausrichtung auf einen Standort nutzen

>[!VIDEO](https://video.tv.adobe.com/v/17390)