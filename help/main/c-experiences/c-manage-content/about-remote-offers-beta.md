---
keywords: Remote-Angebot; zwischengespeicherter Inhalt; dynamischer Inhalt; URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in [!DNL Target] nutzen können, um externe Inhalte von einer CMS oder anderen Systemen zu hosten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#beta newtab=true" tooltip="Was sind Beta-Funktionen in  [!DNL Adobe Target]?"
hide: true
hidefromtoc: true
exl-id: e83ad57e-716d-4595-b5cf-3a882fcb9e37
source-git-commit: 4b57712b838906611702db521b51af84077501e6
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 18%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote, um Inhalte außerhalb von [!DNL Adobe Target] zu hosten, sodass [!DNL Target] auf diese Inhalte verweisen und sie an Benutzer-Websites bereitstellen kann. Diese Inhalte können sich aus Gründen der Benutzerfreundlichkeit oder Sicherheit in einem Content Management System (CMS) oder einem anderen System befinden.

>[!NOTE]
>
>Dieser Artikel enthält Informationen zu Aktualisierungen der [!DNL Target] -Benutzeroberfläche, die derzeit Teil eines Beta-Programms ist. Das [!DNL Adobe Target]-Team ermöglicht für ausgewählte Kunden oft neue Funktionen zu Test- und Feedback-Zwecken. Nach Abschluss des Testzeitraums werden diese Funktionen für alle Kunden in zukünftigen [!DNL Target]-Versionen aktiviert und in den [Versionshinweisen](/help/main/r-release-notes/release-notes.md) angekündigt.

Remote-Angebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) erstellt werden. Sie können keine Remote-Angebote im VEC (0) erstellen oder anwenden. [!UICONTROL Visual Experience Composer] Inhalte werden in die [!DNL Target] -Anfragespeicherorte eingefügt, sodass diese Orte höchstwahrscheinlich nicht für eine globale [!DNL Target] -Anfrage geeignet sind.

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

  Das bedeutet, dass beim Verschieben Ihrer Aktivität von Ihren Staging-Servern in die Produktion der Inhalt automatisch zugänglich ist, ohne die URL manuell ändern zu müssen.

* Wenn Ihr Test dynamisch von Ihrem Server generierte Daten umfasst, kann die Option [!UICONTROL Dynamic] die richtige Wahl sein.
* Wenn Sie nur das Erscheinungsbild Ihres vorhandenen Remote-Angebotsinhalts testen möchten, verwenden Sie den [!UICONTROL Visual Experience Composer] , um das Erscheinungsbild des Inhalts zu ändern, der vom Content Management System zurückgegeben wird.
* Verwenden Sie die [Auswahlmatrix für Remote-Angebote](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um das für Ihren spezifischen Fall am besten geeignete Angebot auszuwählen. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Remote-Angebot über die Seite [!UICONTROL Code Offers] erstellen

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.

1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Geben Sie im Dialogfeld [!UICONTROL Create Remote Offer] einen beschreibenden Namen für das Angebot ein.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der [!UICONTROL Offers] -Bibliothek.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto](/help/main/c-intro/intro.md#premium) verfügen, wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie den Typ der Umleitungs-URL an.

   Weitere Informationen finden Sie unter [Umleitungs-URL-Typ: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic]](#url-type) unten.

1. Geben Sie die absolute Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Remote-Angebot mit dem [!UICONTROL Form-Based Experience Composer] erstellen

1. Wählen Sie beim Erstellen einer Aktivität mit dem [formularbasierten Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Content]** angezeigt werden soll.
1. Klicken Sie auf die Dropdownliste **[!UICONTROL Content]**, klicken Sie auf das Symbol **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Change Remote Offer]**.

1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen beim schnellen Auffinden des Angebots in der [!UICONTROL Assets] -Bibliothek.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto](/help/main/c-intro/intro.md#premium) verfügen, wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie den Typ der Umleitungs-URL an.

   Weitere Informationen finden Sie unter [Umleitungs-URL-Typ: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic]](#url-type) unten.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Umleitungs-URL-Typ: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic] {#url-type}

Die folgenden Informationen helfen Ihnen dabei, die Unterschiede zwischen den beiden Optionen zu verstehen:

### [!UICONTROL Onsite Cached] URL

Der Inhalt eines zwischengespeicherten Remote-Angebots wird von [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt an der Remote-URL ab und speichert ihn dann in [!DNL Target]. Wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält, stellt [!DNL Target] das Angebot bereit.

Zwischengespeicherte Remote-Angebote bieten verbesserte Sicherheit, da jemand, der sich bei [!DNL Target] angemeldet hat, den Inhalt nicht ändern kann. Um den Inhalt zu ändern, muss sich ein Benutzer beim Content Management oder einem anderen System anmelden und den Inhalt dort ändern.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### [!UICONTROL Onsite Dynamic] URL

Ein dynamisches Remote-Angebot wird vom Content Management oder einem anderen System bereitgestellt und nicht von [!DNL Target].

Möglicherweise möchten Sie nicht, dass Inhalte regelmäßig zwischengespeichert und dann von [!DNL Target] bereitgestellt werden, wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält. Stattdessen möchten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise spezifische Informationen weitergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Add Parameter]** klicken, um eine oder mehrere [!DNL Target] Anforderungen oder Anforderungsparameter hinzuzufügen.

## Verwenden von Remote-Angeboten in Aktivitäten

Wenden Sie Remote-Angebote mit dem [!UICONTROL Form-Based Experience Composer] an. Sie können derzeit keine Remote-Angebote mit dem VEC (0) anwenden.[!UICONTROL Visual Experience Composer]

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten, die beim Erstellen von Erlebnissen für die Verwendung in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting]- (XT), [!UICONTROL Automated Personalization]- (AP) und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn die [!UICONTROL Visual Experience Composer] nicht verfügbar oder praktisch zur Verwendung ist. Beispielsweise können Sie mit dem [!UICONTROL Form-Based Experience Composer] Erlebnisse erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Detaillierte schrittweise Anweisungen finden Sie unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) .

1. Geben Sie den gewünschten Ort an und fügen Sie bei Bedarf Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdownliste **[!UICONTROL Content]**, klicken Sie auf das Symbol **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Change Remote Offer]**.

1. Wählen Sie das gewünschte Remote-Angebot im Dialogfeld [!UICONTROL Change Remote Offer] aus und klicken Sie dann auf **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebote {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird ausgeführt, nachdem Sie die Seite gerendert haben. Ein unsichtbarer iFrame erfasst die Daten, kopiert sie aus dem Frame und fügt sie in die Seite ein, wodurch die übergebenen Werte geladen werden.

![remote_offer_howitworks_2 image](assets/remote_offer_howitworks_2.jpeg)

1. Der Browser des Besuchers fordert eine Seite von Ihrem Server an.

2. Browser rendert die Seite, einschließlich mboxes.

3. Der Aufruf von `mboxCreate` enthält Parameter, die zum Rendern dynamischer Inhalte erforderlich sind.

4. [!DNL Target] gibt eine URL mit dem Speicherort des dynamischen Inhalts und seiner Parameter zurück. Legt einen iFrame im mbox-Bereich fest.

5. Der Browser fordert die URL an und rendert sie auf der Seite.

## Auswahlmatrix für Remote-Angebote {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Die Auswahlmatrix für Remote-Angebote hilft Ihnen bei der Entscheidung, welchen Typ von Remote-Angebot Sie wählen sollten: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic].

| Funktion | Onsite zwischengespeichert | Onsite Dynamic |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle zwei Stunden zwischengespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut oder Relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |
