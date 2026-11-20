---
keywords: Recommendations; Intro; Einführung; Webinar; Demo
description: Erfahren Sie mehr über Recommendations-Aktivitäten in Adobe [!DNL Target], die automatisch Inhalte anzeigen, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten.
title: Was sind Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: bc4d9a46-ea21-4687-b8a0-7f2e1dc33ebf
TQID: 'https://experienceleague.adobe.com/6jmXI9CsdCnyyQrQXKzq5WF8OQPQSCbE2Zb8AnpUvks'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: 4f38c80880eedd9b966cdb2f178f408bb529b60c
workflow-type: tm+mt
source-wordcount: '1633'
ht-degree: 9%
---
# Einführung in Recommendations {#introduction-to-recommendations}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie [!DNL Recommendations] Aktivitäten in [!DNL Adobe Target] für Besucher relevante Produkte oder Inhalte anzeigen und wie Sie eine [!DNL Recommendations] Implementierung und Aktivität planen und erstellen.

>[!ENDSHADEBOX]

Diese Seite basiert auf dem Webinar *Einführung in Recommendations*. Eine [!DNL Recommendations] zeigt automatisch Produkte oder Inhalte an, die für Kunden interessant sein könnten, indem Echtzeitvorschläge basierend auf vorherigen Besuchen optimiert werden. Auf der Seite wird auch beschrieben, wie Sie eine [!DNL Recommendations] Aktivität in der [!DNL Target]-Benutzeroberfläche erstellen.

## Einführung

Kunden erwarten zunehmend Empfehlungen und verwenden diese als Ausgangspunkt, um andere verfügbare Optionen zu erkunden. Fast jeder hat ein Produkt gekauft, das er zum ersten Mal in einer Empfehlung gesehen hat, ob in einem Geschäft oder auf einem digitalen Grundstück.

![Empfehlung für Zubehör, das üblicherweise mit einem neuen Telefon gekauft wird, einschließlich Ladestationen, Gehäuse und Kopfhörer.](/help/main/c-recommendations/assets/intro-1.png)

Die Art und Weise, wie Menschen Medien und Inhalte konsumieren, wird zunehmend durch personalisierte Empfehlungen bestimmt, und Digital-First-Marken wie Netflix, Spotify und YouTube starten das Kundenerlebnis mit Empfehlungen. Da mehr Alternativen denn je verfügbar sind, ist es entscheidend, die relevantesten Inhalte für einen Kunden am Punkt der Interaktion zu identifizieren.

Marketingexperten verwenden [!DNL Adobe Target], um personalisierte Erlebnisse für eine Vielzahl von Branchen, Kundentypen und Kanäle verfügbar zu machen. In der folgenden Tabelle finden Sie einige Beispiele dafür, wie Kunden [!DNL Target] zur Bereitstellung personalisierter Empfehlungen verwenden.

| Anwendungsfall | Beispiel |
|---|---|
| Veröffentlichung läuft | Web-Herausgeber verwenden [!DNL Target Recommendations], um Website-Besuchern Artikel zu empfehlen und die Interaktion zu steigern. |
| Videoschulungen | [!DNL Adobe Creative Cloud] verwendet [!DNL Target], um Photoshop-Benutzenden in der Photoshop-Anwendung Video-Tutorials zu empfehlen. |
| Gaming | Gaming-Unternehmen verwenden [!DNL Target], um Benutzern Spiele und Inhalte auf ihren Konsolen zu empfehlen. |
| B2B-Verkäufe | Business-to-Business-Unternehmen verwenden [!DNL Target], um B2B-Pospects Videos, White Papers und Blog-Posts zu empfehlen, Downloads bereitzustellen und Bestandskunden Hilfe anzubieten. |
| Reisen | Ein deutscher Reiseunternehmer verwendet [!DNL Target], um Reisenden Hotels und Ähnliches zu empfehlen. Weitere Informationen finden Sie in der [Adobe Summit-Sitzung](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608){target=_blank}. |
| Einteilung | Ein führender B2B-retailer verwendet [!DNL Target], um wiederkehrenden Besuchern im Browser und in seiner mobilen App die besten Kategorien und Produkte zu empfehlen. |

## Elemente großartiger Empfehlungen

Tolle Empfehlungen sind relevant und personalisiert. Drei Elemente fördern Relevanz und Personalisierung:

* **Marketer-Steuerelemente** um die Relevanz der empfohlenen Elemente zu fördern. Marketing-Experten wissen, welche Attribute ihrer Produkte oder Inhalte ein Recommendations-Modell berücksichtigen sollte. Auf einer Video-Website könnten Benutzer beispielsweise an Filmen desselben Regisseurs interessiert sein, aber wahrscheinlich nicht an Filmen aus demselben Studio. [!DNL Target] bietet Steuerelemente, um Algorithmen mit diesem Domain-Wissen zu verbessern.
* **Ausgefeilte Modelle** um Millionen von Katalogelementen und Interaktionsereignissen einen Sinn zu geben. [!DNL Target] verfügt über maschinelle Lernfunktionen, die über ein Jahrzehnt Erfahrung aufgebaut wurden und Milliarden von Empfehlungen pro Jahr verarbeiten.
* **Benutzerkontext**, um sicherzustellen, dass die Empfehlungen zeitnah und relevant sind. Beispielsweise dürfen Empfehlungen nicht das Video enthalten, das jemand gerade angesehen hat, oder das Shirt, das jemand gerade zum Warenkorb hinzugefügt hat. Das [!DNL Target] Benutzerprofil kann in Recommendations verwendet werden, um eine Personalisierung sicherzustellen.

## Implementieren von [!DNL Target] Recommendations

Beginnen Sie mit einer Strategie, die die folgenden Punkte definiert:

* **Zu empfehlende Elemente**: Produkte, Videos oder Inhalte.
* **Orte für Empfehlungen**: Die Kanäle (Web, Mobile, Im-Store, ein Kiosk usw.), die Teile der Kunden-Journey und die Seiten Ihrer Site, die Empfehlungen enthalten.
* **Erfolgsmessung**: Ermitteln, ob Empfehlungen erfolgreich sind, z. B. durch Vergleich eines Erlebnisses ohne Empfehlungen mit einem Erlebnis mit Empfehlungen oder durch Vergleich von zwei verschiedenen Arten von Empfehlungen. Einige Metriken, z. B. die Auswirkung auf den Kundenlebenszeitwert, sind schwer direkt zu messen, sodass eine konkretere Metrik oft einfacher zu verwenden ist, z. B. der Umsatz pro Besuch, der durchschnittliche Bestellwert oder die Anzahl der Klicks. In einigen Fällen besteht das Ziel darin, eine Metrik zu minimieren, z. B. die Anzahl der Support-Aufrufe.

Nach Festlegung der Strategie umfasst die Umsetzung der [!DNL Target Recommendations] drei große Schritte:

![Abbildung der drei Schritte einer Recommendations-Implementierung: Unterrichten von Target über Ihre Inhalte oder Produkte, Erfassen des Benutzerverhaltens und Abrufen von Recommendations mit dem richtigen Kontext.](assets/intro-6.png)

### [!DNL Target] über Ihre Inhalte oder Produkte unterrichten

Wenn Sie mit [!DNL Recommendations] beginnen, geben Sie Informationen zu jedem Element weiter, das Sie empfehlen möchten.

![Abbildung, die zeigt, wie Sie Target über Ihre Inhalte oder Produkte informieren: Feeds im CSV- oder Google-Feed-Format, die Datenschicht mit Target, die API und die Analytics-Integration.](assets/intro-7.png)

Die einfachste und am häufigsten verwendete Methode besteht darin, eine CSV-Datei täglich oder wöchentlich über ein Produktinformations-Management-System oder ein Content-Management-System zu senden. Andere Optionen bestehen darin, Informationen auf der Datenschicht von Ihrer Seite mithilfe der [!DNL Adobe Target] JavaScript-Bibliothek zu übermitteln, die APIs zu verwenden, um Informationen direkt aus Ihrem Quellsystem zu übermitteln, oder die [!DNL Adobe Analytics]-Integration zu verwenden, wenn Sie bereits Katalogdaten an [!DNL Analytics] übergeben. Sie können mehrere Optionen zusammen verwenden, z. B. die meisten Daten täglich über eine CSV-Datei und Inventaraktualisierungen häufiger über eine API übergeben. Die IT-Abteilung ist in der Regel an der Einrichtung dieses Schritts beteiligt.

Unabhängig von der gewählten Methode sollten Sie Metadaten zu jedem Element in drei Kategorien einschließen:

* **Daten, die Sie dem Benutzer anzeigen möchten, der die Empfehlung erhält.** Zum Beispiel den Namen des Films und eine URL mit einer Miniaturansicht.
* **Daten, die für die Anwendung von Marketing- und Merchandising-Steuerelementen nützlich sind.** Beispielsweise die Bewertung des Films, sodass Sie keine Filme mit explizit sexuellen Inhalten empfehlen.
* **Daten, die für die Bestimmung der Ähnlichkeit von Elementen mit anderen Elementen nützlich sind.** Beispielsweise das Genre des Films oder die Darsteller im Film.

### Erfassen des Benutzerverhaltens

![Abbildung, die zeigt, wie das Benutzerverhalten erfasst wird: Ansichten und Klicks führen zu Käufen, Konversionen, Downloads, Abonnements und Wiedergaben, die mit Target, Analytics oder der API verfolgt werden.](assets/intro-9.png)

Fügen Sie Tags hinzu oder verwenden Sie Ihre vorhandene [!DNL Analytics]-Implementierung, damit [!DNL Target] weiß, welche Elemente Ihre Benutzer anzeigen und kaufen. Wenn der Kauf für Ihren Kontext nicht relevant ist, verfolgen Sie einen anderen Konversionstyp, z. B. das Herunterladen einer PDF, das Ausfüllen einer Umfrage, das Abonnieren eines Newsletters oder das Ansehen eines Videos.

Wenn Sie [!DNL Target] bereits zum Ausführen von A/B-Test -Aktivitäten auf Ihrer Site verwenden, haben Sie diesen Schritt möglicherweise bereits abgeschlossen. Wenn Sie bereits [!DNL Adobe Analytics] verwenden, um Berichte über Site-Besuche und das Konversionsverhalten zu erstellen, können Sie [!DNL Analytics] als Verhaltensdatenquelle verwenden. Andernfalls besteht die einfachste Option darin, dies mit einem Tag-Manager wie Tags in [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html?lang=de){target=_blank} einzurichten. Offline- oder In-App-Interaktionen können auch über die Echtzeit-API an [!DNL Target] gesendet werden.

### Erhalten von Empfehlungen mit dem richtigen Kontext

![Abbildung, die zeigt, wie Empfehlungen mit dem richtigen Kontext abgerufen werden: Das aktuell angezeigte Produkt, die aktuelle Produktkategorie, die von Benutzenden bevorzugte Kategorie, die von Benutzenden bevorzugte Marke und die Benutzerloyalitätsstufe werden an Target übergeben.](assets/intro-10.png)

Neben dem Gesamtverhalten des Benutzers benötigt [!DNL Target] den spezifischen Kontext, in dem Empfehlungen angezeigt werden, wozu Informationen über die Seite und Informationen aus dem Benutzerprofil gehören. [!DNL Target] verwendet diese Informationen, um Elemente zu filtern und die Personalisierung von Empfehlungen zu verbessern.

## Erstellen der ersten Recommendations-Aktivität

Eine [!DNL Recommendations] Aktivität kombiniert eine Zielgruppe, Kriterien und ein Design. [!DNL Target] umfasst 14 integrierte Zielgruppen, 42 integrierte Kriterien und 10 integrierte Design-Vorlagen. Sie können jedes dieser Elemente anpassen oder eigene hinzufügen.

![Abbildung der Teile, die eine gute Recommendations-Aktivität ausmachen: die Zielgruppe (die diese Recommendations sehen sollte), die Kriterien (welche Elemente empfohlen werden sollten) und das Design (wie die empfohlenen Elemente angezeigt werden).](assets/intro-11.png)

[!DNL Target] verwendet das Konzept der Kriterienkarte, das wie ein Rezept für die Personalisierung ist. Die Auswahl oder Erstellung der richtigen Kriterien ist wichtig, um die gewünschten Personalisierungsergebnisse zu erzielen. Eine Kriterienkarte funktioniert wie eine funnel, die Sie aus Ihrem gesamten Katalog bis hin zu Ihren endgültigen Empfehlungen führt.

![Abbildung der funnel-Kriterien: Kataloginhalte, statische Filter (Sammlungen und Ausschlüsse), Algorithmus (Empfehlungsschlüssel und -logik), Online-Geschäftsregeln (dynamische Filterung und Attributgewichtung) und endgültige Empfehlungen neben einer Beispielkriterienkarte.](assets/intro-14.png)

In den folgenden Abschnitten werden die Teile dieser funnel und ihre Funktionsweise in [!DNL Target] beschrieben.

### Statische Filter (Sammlungen und Ausschlüsse)

Statische Filter sind allgemein anwendbare Regeln in Bezug auf Katalogattribute, von denen Sie nicht erwarten, dass sie häufig geändert werden, sodass Sie sie in mehreren Empfehlungen verwenden können.

![Abbildung statischer Filter. Inhalt: Schließt alle Filme ein und schließt Filme mit der Einstufung NC-17 von den Empfehlungen aus. Produkte: Umfasst alle in den Vereinigten Staaten verfügbaren Produkte und schließt Produkte von einem regionalen Private Label aus.](assets/intro-16.png)

### Algorithmus (Empfehlungsschlüssel und -logik)

Der nächste Schritt besteht darin, einen Empfehlungsschlüssel und eine Logik auszuwählen, die die Grundlage für Ihre Empfehlung bilden. Der Empfehlungsschlüssel ist das gesuchte Objekt, aufgrund dessen eine Empfehlung ausgewählt wird.

![Abbildung des Algorithmusschritts. Empfehlungsschlüssel: aktuell angezeigter Artikel, aktuell angezeigte Kategorie, zuletzt gekaufter Artikel oder benutzerdefiniertes Attribut. Empfehlungslogik: Artikel mit ähnlichen Attributen, am häufigsten angezeigte Artikel in der Kategorie, Kunden, die diesen Artikel gekauft haben, haben auch diese Artikel gekauft, oder benutzerdefinierter Algorithmus.](assets/intro-17.png)

[!DNL Target] umfasst ein Portfolio von Algorithmen.

![Abbildung des Portfolios an Algorithmen: Beliebtheitsbasierte (am häufigsten angezeigt, Topverkäufe), inhaltsbasierte (Inhaltsähnlichkeit), artikelbasierte kollaborative Filterung (angezeigt/angezeigt, angezeigt/gekauft, gekauft/gekauft, wobei gekauft jede Konversion sein kann), personalisiert (kürzlich angezeigt, Site-Affinität, profilerweiterte Zusammenstellung). Filtern), und bringen Sie Ihre eigenen (benutzerdefinierte Algorithmen).](assets/intro-15.png)

### Online-Geschäftsregeln

Der letzte Schritt besteht in der Anwendung von Online-Geschäftsregeln, die Ihre Algorithmen mit Domain-Wissen und aktuellem Kontext verbessern, basierend darauf, was der Besucher auf Ihrem digitalen Eigentum tut.

![Illustration von Online-Geschäftsregeln. Inhalt: Schließen Sie zuvor angesehene Filme aus, zeigen Sie Filme desselben Regisseurs und steigern Sie die Qualität Ihrer Filme mit demselben Genre. Produkte: Ausschließen von nicht vorrätigen Produkten, Anzeigen von Artikeln mit einem Preis von 5 bis 500 $ und Verstärken von Artikeln aus derselben Marke.](/help/main/c-recommendations/assets/intro-18.png)
