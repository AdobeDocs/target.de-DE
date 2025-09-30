---
keywords: Remote-Angebot;zwischengespeicherte Inhalte;dynamischer Inhalt;URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in [!DNL Target]  nutzen können, um externe Inhalte von einem CMS oder anderen Systemen zu hosten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: 856396264c4a7b7e3370cd268e7f010092e2eae2
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 18%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote, um Inhalte außerhalb von [!DNL Adobe Target] zu hosten, sodass [!DNL Target] diese Inhalte referenzieren und an Benutzer-Websites bereitstellen können. Diese Inhalte können sich aus Gründen der Benutzerfreundlichkeit oder der Sicherheit in einem Content-Management-System (CMS) oder einem anderen System befinden.

Remote-Angebote können auf der Seite [!UICONTROL Offers] > [!UICONTROL Code Offers] oder im [Forms-basierten Experience Composer erstellt ](/help/main/c-experiences/form-experience-composer.md). Remote-Angebote im [!UICONTROL Visual Experience Composer] (VEC) können nicht erstellt oder angewendet werden. Inhalte werden an den [!DNL Target] Anfragespeicherorten eingefügt, sodass diese Speicherorte wahrscheinlich nicht für eine globale [!DNL Target]-Anfrage geeignet sind.

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

* Remote-Angebote werden unterstützt in:

   * A/B-Aktivitäten
   * Experience Targeting-(XT)-Aktivitäten
   * Formularbasierte Workflows

* Remote-Angebote werden in nicht unterstützt:

   * [Premium-](/help/main/c-intro/intro.md#premium) (Automated Personalization (AP), Automatisches Targeting und Recommendations)
   * Multivariate Testing (MVT), da der VEC verwendet wird, der keine Remote-Angebote unterstützt.

* Wenn sich Ihr Angebot in derselben Domain wie die [!DNL Target]-Anfragen befindet, können Sie mit der Option [!UICONTROL Cached] relative URLs zur Beschreibung Ihres Angebotsspeicherorts verwenden.

  Das bedeutet, dass beim Verschieben Ihrer Aktivität von Ihren Staging-Servern in die Produktion automatisch auf die Inhalte zugegriffen werden kann, ohne dass die URL manuell geändert werden muss.

* Wenn Ihr Test Daten umfasst, die von Ihrem Server dynamisch generiert wurden, ist die Option [!UICONTROL Dynamic] möglicherweise die richtige Wahl.
* Wenn Sie nur das Erscheinungsbild Ihrer vorhandenen Remote-Angebotsinhalte testen möchten, verwenden Sie die [!UICONTROL Visual Experience Composer], um das Erscheinungsbild der Inhalte zu ändern, die vom Content-Management-System zurückgegeben werden.
* Verwenden Sie die [Remote-Angebotsauswahlmatrix](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um das Angebot auszuwählen, das für Ihren spezifischen Fall am besten geeignet ist. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Remote-Angebot über die [!UICONTROL Code Offers] erstellen

1. Klicken Sie auf **[!UICONTROL Offers]** und wählen Sie dann die Registerkarte **[!UICONTROL Code Offers]** aus.

1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Geben Sie im Dialogfeld &quot;[!UICONTROL Create Remote Offer]&quot; einen beschreibenden Namen für das Angebot ein.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der [!UICONTROL Offers] zu finden.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto verfügen](/help/main/c-intro/intro.md#premium) wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie den Umleitungs-URL-Typ an.

   Siehe [Umleitungs-URL-Typ: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic]](#url-type) unten für weitere Informationen.

1. Geben Sie die absolute Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Erstellen eines Remote-Angebots mithilfe der [!UICONTROL Form-Based Experience Composer]

1. Wählen Sie beim Erstellen einer Aktivität mit [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, um den Abschnitt &quot;**[!UICONTROL Content]**&quot; anzuzeigen.
1. Klicken Sie auf die Dropdown-Liste &quot;**[!UICONTROL Content]**&quot;, dann auf das **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und schließlich auf **[!UICONTROL Change Remote Offer]**.

1. Klicken Sie auf **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der [!UICONTROL Assets] zu finden.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto verfügen](/help/main/c-intro/intro.md#premium) wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie den Umleitungs-URL-Typ an.

   Siehe [Umleitungs-URL-Typ: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic]](#url-type) unten für weitere Informationen.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Umleitungs-URL-Typ: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic] {#url-type}

Die folgenden Informationen helfen Ihnen, die Unterschiede zwischen den beiden Optionen zu verstehen:

### [!UICONTROL Onsite Cached] URL

Der Inhalt für ein zwischengespeichertes Remote-Angebot wird aus [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt von der Remote-URL ab und speichert dann den Inhalt in [!DNL Target]. Wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält, stellt [!DNL Target] das Angebot bereit.

Zwischengespeicherte Remote-Angebote bieten mehr Sicherheit, da jemand, der sich bei angemeldet hat, den Inhalt nicht ändern [!DNL Target]. Um den Inhalt zu ändern, muss sich jemand beim Content Management oder einem anderen System anmelden und den Inhalt dort ändern.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### [!UICONTROL Onsite Dynamic] URL

Ein dynamisches Remote-Angebot wird vom Content-Management- oder anderen System und nicht von [!DNL Target] aus bereitgestellt.

Möglicherweise möchten Sie nicht, dass der Inhalt regelmäßig zwischengespeichert und dann von [!DNL Target] bereitgestellt wird, wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält. Stattdessen sollten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise bestimmte Informationen übergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Add Parameter]** klicken, um eine oder mehrere [!DNL Target] Anfragen oder Anfrageparameter hinzuzufügen.

## Remote-Angebote in Aktivitäten verwenden

Remote-Angebote über die [!UICONTROL Form-Based Experience Composer] anwenden. Mit dem [!UICONTROL Visual Experience Composer] (VEC) können Sie derzeit keine Remote-Angebote anwenden.

Die [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] ist eine nicht visuelle Benutzeroberfläche zur Erstellung von Erlebnissen und Angeboten. Diese Erlebnisse können in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Recommendations]-Aktivitäten verwendet werden, wenn die [!UICONTROL Visual Experience Composer] nicht verfügbar oder unpraktisch in der Anwendung ist. Beispielsweise können Sie die [!UICONTROL Form-Based Experience Composer] verwenden, um Erlebnisse zu erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL Form-Based Experience Composer].

   Unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) finden Sie detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Speicherort an und fügen Sie gegebenenfalls Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf die Dropdown-Liste &quot;**[!UICONTROL Content]**&quot;, dann auf das **[!UICONTROL List]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und schließlich auf **[!UICONTROL Change Remote Offer]**.

1. Wählen Sie das gewünschte Remote-Angebot aus dem [!UICONTROL Change Remote Offer] Dialogfeld aus und klicken Sie dann auf **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Schließen Sie die Konfiguration der Aktivität ab.

## Funktionsweise dynamischer Remote-Angebote {#concept_CC2A969420B34364A9FA78C1CE251818}

Auf dynamischen Seiten können Werte an dynamische Remote-Angebote übergeben werden.

Das Angebot wird ausgeführt, nachdem Sie die Seite gerendert haben. Ein unsichtbarer iFrame sammelt die Daten, kopiert sie aus dem Frame und fügt sie auf der Seite ein, wobei die übergebenen Werte geladen werden.

![remote_offer_howitworks_2 Bild](assets/remote_offer_howitworks_2.jpeg)

1. Der Browser des Besuchers fordert eine Seite von Ihrem Server an.

2. Browser rendert die Seite, einschließlich Mboxes.

3. `mboxCreate` Aufruf enthält Parameter, die zum Rendern dynamischer Inhalte erforderlich sind.

4. [!DNL Target] gibt eine URL mit dem Speicherort des dynamischen Inhalts und seiner Parameter zurück. Legt einen iFrame im mbox-Bereich fest.

5. Der Browser fordert die URL an und rendert sie in der -Seite.

## Remote-Angebotsauswahlmatrix {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Die Matrix zur Remote-Angebotsauswahl hilft Ihnen bei der Entscheidung, welche Art von Remote-Angebot ausgewählt werden soll: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic].

| Funktion | Onsite zwischengespeichert | Dynamische Onsite-Bereitstellung |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle zwei Stunden zwischengespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut oder relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |
