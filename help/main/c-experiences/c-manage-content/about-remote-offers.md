---
keywords: Remote-Angebot;zwischengespeicherte Inhalte;dynamischer Inhalt;URL-Typ
description: Erfahren Sie, wie Sie Remote-Angebote in [!DNL Target]  nutzen können, um externe Inhalte von einem CMS oder anderen Systemen zu hosten.
title: Wie erstelle ich Remote-Angebote?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
TQID: https://experienceleague.adobe.com/maKcis5ROOKMcc3-axxGv1qJIQzC6o-Qc-Cjl8clQ1I
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1145
ht-degree: 23%

---

# Remote-Angebote erstellen

Verwenden Sie Remote-Angebote, um Inhalte außerhalb von [!DNL Adobe Target] zu hosten, sodass [!DNL Target] diese Inhalte referenzieren und an Benutzer-Websites bereitstellen können. Diese Inhalte können sich aus Gründen der Benutzerfreundlichkeit oder der Sicherheit in einem Content-Management-System (CMS) oder einem anderen System befinden.

Remote-Angebote können auf der Seite [!UICONTROL Angebote] > [!UICONTROL Code-Angebote] oder im [Forms-basierten Experience Composer erstellt ](/help/main/c-experiences/form-experience-composer.md). Remote-Angebote können nicht im [!UICONTROL Visual Experience Composer) (]) erstellt oder angewendet werden. Inhalte werden an den [!DNL Target] Anfragespeicherorten eingefügt, sodass diese Speicherorte wahrscheinlich nicht für eine globale [!DNL Target]-Anfrage geeignet sind.

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

* Wenn sich Ihr Angebot in derselben Domain wie die [!DNL Target]-Anfragen befindet, können Sie mit der Option [!UICONTROL Zwischengespeichert] relative URLs zur Beschreibung Ihres Angebotsspeicherorts verwenden.

  Das bedeutet, dass beim Verschieben Ihrer Aktivität von Ihren Staging-Servern in die Produktion automatisch auf die Inhalte zugegriffen werden kann, ohne dass die URL manuell geändert werden muss.

* Sollten in Ihrem Test dynamisch vom Server generierte Daten enthalten sein, ist die Option [!UICONTROL Dynamisch] möglicherweise die richtige Wahl.
* Sollten Sie lediglich planen, die Darstellung des Inhalts Ihres bestehenden Remote-Angebots zu prüfen, verwenden Sie den [!UICONTROL Visual Experience Composer], um Aussehen und Eindruck des Inhalts anzupassen, der vom Inhaltsverwaltungssystem ausgegeben wird.
* Verwenden Sie die [Remote-Angebotsauswahlmatrix](#reference_B23BEDD29DDD47709A7651AFD27E776B) (unten), um das Angebot auszuwählen, das für Ihren spezifischen Fall am besten geeignet ist. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Fragen haben.

## Erstellen eines Remote-Angebots über die Seite [!UICONTROL Angebote ]Code)

1. Klicken Sie auf **[!UICONTROL Angebote]** und wählen Sie anschließend die Registerkarte **[!UICONTROL Code-Angebote]** aus.

1. Klicken Sie **[!UICONTROL Angebot erstellen]** > **[!UICONTROL Remote-Angebot]**.

1. Geben [!UICONTROL  im Dialogfeld „Remote-] erstellen“ einen beschreibenden Namen für das Angebot ein.

   Ein beschreibender Name hilft Ihnen und anderen, das Angebot schnell in der Bibliothek [!UICONTROL Angebote] zu finden.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto verfügen](/help/main/c-intro/intro.md#premium) wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie den Umleitungs-URL-Typ an.

   Weitere Informationen finden [ unter „URL-Typ [!UICONTROL Onsite ] oder [!UICONTROL Onsite Dynamic]](#url-type) unten.

1. Geben Sie die absolute Remote-URL für das Remote-Angebot an.

1. Klicken Sie **[!UICONTROL Erstellen]**.

## Erstellen eines Remote-Angebots mit dem [!UICONTROL formularbasierten Experience Composer]

1. Wählen Sie beim Erstellen einer Aktivität mit [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) den Speicherort aus, an dem der Abschnitt **[!UICONTROL Inhalt]** angezeigt werden soll.
1. Klicken Sie auf **[!UICONTROL Inhalt]** Dropdown-Liste, klicken Sie auf das Symbol **[!UICONTROL Liste]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Remote-Angebot ändern]**.

1. Klicken Sie **[!UICONTROL Angebot erstellen]** > **[!UICONTROL Remote-Angebot]**.

1. Geben Sie einen beschreibenden Namen für das Angebot an.

   Ein beschreibender Name unterstützt Sie und andere dabei, das Angebot problemlos in der Bibliothek [!UICONTROL Assets] aufzufinden.

1. (Bedingt) Wenn Sie über ein [Target Premium-Konto verfügen](/help/main/c-intro/intro.md#premium) wählen Sie den gewünschten [Arbeitsbereich](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) aus.

1. Geben Sie den Umleitungs-URL-Typ an.

   Weitere Informationen finden [ unter „URL-Typ [!UICONTROL Onsite ] oder [!UICONTROL Onsite Dynamic]](#url-type) unten.

1. Geben Sie die Remote-URL für das Remote-Angebot an.

1. Klicken Sie **[!UICONTROL Erstellen]**.

## Umleitungs-URL-Typ: [!UICONTROL Onsite zwischengespeichert] oder [!UICONTROL Onsite dynamisch] {#url-type}

Die folgenden Informationen helfen Ihnen, die Unterschiede zwischen den beiden Optionen zu verstehen:

### [!UICONTROL Onsite zwischengespeichert] URL

Der Inhalt für ein zwischengespeichertes Remote-Angebot wird aus [!DNL Target] bereitgestellt.

Alle zwei Stunden ruft [!DNL Target] den Inhalt von der Remote-URL ab und speichert dann den Inhalt in [!DNL Target]. Wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält, stellt [!DNL Target] das Angebot bereit.

Zwischengespeicherte Remote-Angebote bieten mehr Sicherheit, da jemand, der sich bei angemeldet hat, den Inhalt nicht ändern [!DNL Target]. Um den Inhalt zu ändern, muss sich jemand beim Content Management oder einem anderen System anmelden und den Inhalt dort ändern.

Sie können für zwischengespeicherte Remote-Angebote eine absolute oder relative URL angeben.

### [!UICONTROL Onsite Dynamic] URL

Ein dynamisches Remote-Angebot wird vom Content-Management- oder anderen System und nicht von [!DNL Target] aus bereitgestellt.

Möglicherweise möchten Sie nicht, dass der Inhalt regelmäßig zwischengespeichert und dann von [!DNL Target] bereitgestellt wird, wenn Besucher eine Site mit einem Erlebnis laden, das ein Remote-Angebot enthält. Stattdessen sollten Sie das System aufrufen, das den Inhalt hostet, und möglicherweise bestimmte Informationen übergeben, damit das zurückgegebene Angebot für jeden Benutzer dynamisch (oder anders) sein kann. Meldet sich ein Benutzer beispielsweise auf einer Kreditkarten-Website an, auf der ein dynamisches Angebot enthalten ist, können Sie in die URL Parameter für die Kontoinformationen des Benutzers einfügen. In diesem Fall zeigt die Webseite benutzerspezifische Daten an, beispielsweise den Kontostand.

Sie können auf **[!UICONTROL Parameter hinzufügen]** klicken, um eine oder mehrere [!DNL Target] oder Anfrageparameter hinzuzufügen.

## Remote-Angebote in Aktivitäten verwenden

Anwenden von Remote-Angeboten mithilfe [!UICONTROL Form-Based Experience Composer]. Sie können derzeit keine Remote-Angebote mit dem [!UICONTROL Visual Experience Composer] (VEC) anwenden.

Der [!DNL Adobe Target] [!UICONTROL formularbasierte Experience Composer] ist eine nicht visuelle Oberfläche zur Erlebnis- und Angebotserstellung, die beim Erstellen von Erlebnissen für [!UICONTROL A/B-]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- und [!UICONTROL Recommendations]-Aktivitäten nützlich ist, wenn der [!UICONTROL Visual Experience Composer] nicht verfügbar oder unpraktisch in der Anwendung ist. Beispielsweise können Sie den [!UICONTROL formularbasierten Experience Composer) verwenden] um Erlebnisse zu erstellen, die Remote-Angebote verwenden.

1. Erstellen oder bearbeiten Sie eine Aktivität im [!UICONTROL formularbasierten Experience Composer].

   Unter [Form-Based Experience Composer](/help/main/c-experiences/form-experience-composer.md) finden Sie detaillierte schrittweise Anweisungen.

1. Geben Sie den gewünschten Speicherort an und fügen Sie gegebenenfalls Zielgruppenverfeinerungen hinzu.

1. Klicken Sie auf **[!UICONTROL Inhalt]** Dropdown-Liste, klicken Sie auf das Symbol **[!UICONTROL Liste]** ( ![Liste](/help/main/assets/icons/MoreSmallList.svg) ) und dann auf **[!UICONTROL Remote-Angebot ändern]**.

1. Wählen Sie das gewünschte Remote-Angebot im Dialogfeld [!UICONTROL Remote-Angebot ändern] aus und klicken Sie dann auf **[!UICONTROL Angebot erstellen]** > **[!UICONTROL Remote-Angebot]**.

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

Die Matrix zur Remote-Angebotsauswahl hilft Ihnen bei der Auswahl des Remote-Angebots: [!UICONTROL Onsite Cached] oder [!UICONTROL Onsite Dynamic].

| Funktion | Onsite zwischengespeichert | Dynamische Onsite-Bereitstellung |
|--- |--- |--- |
| Wird bei jeder Anforderung eines Besuchers aktualisiert | Nein | Ja |
| Inhaltsaktualisierungen | Alle zwei Stunden zwischengespeichert | Sofort nach jeder Anforderung aktualisiert |
| Ladezeit | Schneller | Langsamer aufgrund Anforderungsverarbeitung |
| JavaScript wird auf Seite angezeigt | Ja | Nein, aber kann per URL übergeben werden |
| Angebote können JavaScript enthalten. | Ja | Ja |
| Angebots-URL | Absolut oder relativ | Relativ |
| Anfordernder Computer | Adobe-Server | Der Computer des Besuchers, auf dem die Cookies des Besuchers gespeichert sind |
