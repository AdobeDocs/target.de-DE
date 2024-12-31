---
keywords: Recommendations; Intro; Einführung; Webinar; Demo
description: Erfahren Sie mehr über Recommendations-Aktivitäten in Adobe  [!DNL Target] . Diese zeigen automatisch Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten.
title: Was sind Recommendations-Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: bc4d9a46-ea21-4687-b8a0-7f2e1dc33ebf
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2086'
ht-degree: 90%

---

# Einführung in Recommendations

Der Text in diesem Artikel stammt vom Webinar *Einführung in Recommendations*, das Sie sich unten zur Gänze ansehen können.

Das Webinar *„Einführung in Recommendations“* beinhaltet eine ausführliche Untersuchung, wie der Wert von [!DNL Adobe Target Recommendations] wirksam eingesetzt werden kann. Erfahren Sie, wie diese [!DNL Target]-Aktivität automatisch Produkte oder Inhalte anzeigt, die für Ihre Kunden von Interesse sein könnten, indem sie Echtzeitvorschläge auf der Grundlage früherer Besuche optimiert. Außerdem können Sie in die [!DNL Target]-Benutzeroberfläche eintauchen, um eine schrittweise Übersicht über das Erstellen einer [!DNL Recommendations]-Aktivität zu erhalten.

## Einführung

Wir alle kennen die Empfehlungen, die uns beim Online-Einkauf angezeigt werden. Immer mehr Kunden erwarten diese Empfehlungen und verwenden sie als Ausgangspunkt, um andere verfügbare Angebote zu durchsuchen. Wenn Sie an Ihr eigenes Kaufverhalten denken, müssen Sie wohl zugeben, dass diese Empfehlungen wirklich gut funktionieren. Fast jeder von uns hat schon einmal ein Produkt gekauft, das er bzw. sie zuerst in einer Empfehlung gesehen haben – egal ob im Internet oder in einem Laden.

Die folgende Abbildung zeigt eine Empfehlung, die Zubehör präsentiert, das häufig mit einem neuen Smartphone gekauft wird, darunter auch Ladestationen und Kopfhörer.

![Empfehlung von Zubehör, das andere mit einem neuen Handy gekauft haben.](/help/main/c-recommendations/assets/intro-1.png)

Aber wir denken nicht immer darüber nach, wie Digital-First-Marken die Messlatte der Kundenerwartungen höher legen. Unser Konsum von Medien und Inhalten wird immer mehr von personalisierten Empfehlungen gesteuert. Überlegen Sie, was Sie als Erstes sehen, wenn Sie Netflix, Spotify oder YouTube öffnen. Diese Unternehmen beginnen das Kundenerlebnis mit Empfehlungen. In einer Welt, in der mehr Alternativen denn je verfügbar sind, ist es entscheidend, dass Sie die relevantesten Inhalte für Ihre Kundinnen und Kunden am Punkt der Interaktion identifizieren können.

![Empfehlung, die digitale Marken präsentiert](/help/main/c-recommendations/assets/intro-2.png)

Marketingexperten verwenden [!DNL Adobe Target], um personalisierte Erlebnisse für eine Vielzahl von Branchen, Kundentypen und Kanäle verfügbar zu machen.

[!DNL Adobe Target] stellt personalisierte Inhalte überall bereit.

![Abbildung zeigt, wie Target Empfehlungen an verschiedenen Orten bereitstellt](/help/main/c-recommendations/assets/intro-3.png)

* **Publishing**: Web-Herausgeber verwenden [!DNL Target Recommendations], um Site-Besuchern Artikel zu empfehlen und die Interaktion zu steigern.
* **Video-Tutorials**: [!DNL Adobe Creative Cloud] verwendet [!DNL Target], um Photoshop-Benutzern in der Photoshop-Anwendung Video-Tutorials zu empfehlen.
* **Gaming**: Gaming-Unternehmen verwenden [!DNL Target], um Benutzern auf ihren Konsolen Spiele und Inhalte zu empfehlen.
* **B2B-Verkäufe**: [B2B-Unternehmen verwenden Target, um B2B-Pospects Videos, White Papers und Blog-Posts zu empfehlen, Downloads bereitzustellen und Bestandskunden Hilfe anzubieten](https://theblog.adobe.com/testing-shifts-high-gear-intel).

* **Reisen**: [Ein deutscher Reiseunternehmer verwendet Target, um Reisenden Hotels und Ähnliches zu empfehlen](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608).

* **Einzelhandel**: [Ein führender B2B-Händler verwendet Target, um wiederkehrenden Besuchern im Browser und in seiner mobilen App die besten Kategorien und Produkte zu empfehlen](https://theblog.adobe.com/optimization-personalization-b2b-powerhouse-grainger/).

Dies sind nur einige der Arten, wie Kunden Target verwenden, um personalisierte Empfehlungen bereitzustellen.

Wie sehen gute Empfehlungen aus?

![Abbildung zeigt die drei Elementen, die in einer guten Empfehlung nicht fehlen dürfen](/help/main/c-recommendations/assets/intro-4.png)

Gute Empfehlungen sollten relevant und personalisiert sein. Zur Steigerung der Relevanz und Personalisierung benötigen Sie drei Dinge:

* **Steuerelemente für Marketingexperten**, um die Relevanz der empfohlenen Artikel zu steigern. Als Marketingexperte haben Sie wertvolles Hintergrundwissen und verstehen, welche Attribute Ihrer Produkte oder Inhalte für ein Empfehlungsmodell relevant sind. Wenn Sie eine Videoseite betreiben, wissen Sie, dass Benutzer vielleicht daran interessiert sind, Filme vom selben Regisseur zu sehen, aber wahrscheinlich kümmert es Sie nicht, Filme zu sehen, die vom selben Studio produziert wurden. [!DNL Target] stellt Ihnen Steuerelemente zur Verfügung, mit denen Sie Ihre Algorithmen auf der Basis dieser Branchenkenntnis verbessern können.
* **Hochentwickelte Modelle**, um die Millionen von Artikeln in Ihrem Katalog und den Interaktionsereignissen sinnvoll zu ordnen. [!DNL Target] besitzt eine fortschrittliche maschinelle Lernfunktionen, die sich auf jahrelange Erfahrung stützt. Zusätzlich handhaben wir Jahr für Jahr Milliarden von Empfehlungen.
* **Benutzerkontext**, um sicherzustellen, dass Empfehlungen zeitgerecht und für Ihre Benutzer relevant sind. Sie möchten das Video, das jemand gerade angesehen hat, oder das Hemd, das jemand gerade zum Warenkorb hinzugefügt hat, nicht empfehlen. Das umfangreiche Benutzerprofil von Target kann in Recommendations verwendet werden, um Personalisierung sicherzustellen.

## Implementieren von [!DNL Target] Recommendations

Beginnen Sie mit einer Strategie.

![Abbildung einer Recommendations-Strategie](/help/main/c-recommendations/assets/intro-5.png)

* **Welche Artikel möchten Sie empfehlen?** Überlegen Sie sich zunächst, welche Artikel Sie empfehlen möchten. Dies könnten Produkte, Videos oder Inhalte sein.
* **Wo möchten Sie die Empfehlungen präsentieren?** Überlegen Sie dann, wo Sie Empfehlungen präsentieren möchten. Wählen Sie die Kanäle (Web, Mobile, im Geschäft, im Kiosk usw.) aus, auf denen Empfehlungen präsentiert werden sollen. Welche Teile der Customer Journey sollen Empfehlungen enthalten? Welche Seiten auf Ihrer Website sollen Empfehlungen enthalten?
* **Wie werden Sie feststellen, ob Empfehlungen erfolgreich sind?** Angenommen, Sie haben ein Erlebnis ohne Empfehlungen und ein Erlebnis mit Empfehlungen oder Sie verfügen über zwei verschiedene Typen von Empfehlungen. Wie können Sie ermitteln, welches Erlebnis für Ihre Kunden besser war? Einige Metriken sind möglicherweise schwieriger zu messen als andere. Beispielsweise sind die Auswirkungen von Empfehlungen auf den Kundenlebenszeitwert oft nur schwer unmittelbar festzustellen. Es ist daher oft einfacher, anstelle einer abstrakten eine konkretere Metrik zu verwenden, z. B. Umsatz pro Besuch, durchschnittlicher Bestellwert oder Anzahl der Klicks. In einigen Fällen möchten Sie möglicherweise auch eine Metrik minimieren, z. B. die Anzahl der Supportanrufe.

Nachdem Sie Ihre Strategie festgelegt haben, können Sie mit der Implementierung von [!DNL Target Recommendations] beginnen.

Die Implementierung von Recommendations umfasst im Großen und Ganzen drei Schritte:

![Abbildung der Schritte zur Implementierung von Recommendations](/help/main/c-recommendations/assets/intro-6.png)

1. Trainieren von [!DNL Target] in Bezug auf Ihren Kontext oder Ihre Produkte.
1. Erfassen des Benutzerverhaltens.
1. Bereitstellen von Empfehlungen mit dem richtigen Kontext.

### Trainieren von [!DNL Target] in Bezug auf Ihren Kontext oder Ihre Produkte

Wenn Sie mit [!DNL Recommendations] beginnen, übermitteln Sie Informationen zu jedem Artikel, den Sie empfehlen möchten. [!DNL Target] bietet verschiedene Integrationsoptionen zur Erstellung Ihres Katalogs.

![Abbildung, die zeigt, wie Target in Bezug auf Kontext oder Produkte trainiert wird](/help/main/c-recommendations/assets/intro-7.png)

Die einfachste und am häufigsten verwendete Methode besteht darin, täglich oder wöchentlich eine CSV-Datei von Ihrem Produktinformationsmanagement- oder Content-Management-System zu übermitteln. Sie können jedoch auch Informationen über die Datenschicht von Ihrer Seite mithilfe der [!DNL Adobe Target]-JavaScript-Bibliothek senden, unsere APIs nutzen, um Informationen direkt aus Ihrem Ausgangssystem weiterzugeben, oder unsere [!DNL Adobe Analytics]-Integration nutzen, wenn Sie bereits Katalogdaten an [!DNL Analytics] weiterleiten.

Sie können aber auch mehrere Optionen gemeinsam verwenden, z. B. den Großteil der Daten täglich per CSV-Datei und Inventaraktualisierungen häufiger per API übermitteln.

Normalerweise hilft Ihre IT-Abteilung bei der Durchführung dieses Schritts.

Unabhängig von der gewählten Methode sollten Sie zu jedem Artikel drei Kategorien von Metadaten mitsenden:

![Abbildung von Metadaten-Informationen für Ihren Katalog](/help/main/c-recommendations/assets/intro-8.png)

* Daten, die dem Benutzer angezeigt werden sollen, der die Empfehlung erhält. Zum Beispiel den Namen des Films und eine URL mit einer Miniaturansicht.
* Daten, die zur Anwendung von Marketing- und Merchandising-Steuerelementen nützlich sind. Beispielsweise die Bewertung des Films, sodass Sie keine Filme mit explizit sexuellen Inhalten empfehlen.
* Daten, die zur Bestimmung der Ähnlichkeit von Artikeln nützlich sind. Beispielsweise das Genre des Films oder die Darsteller im Film.

### Erfassen des Benutzerverhaltens

Als Nächstes sollten Sie Tags hinzufügen oder vorhandene [!DNL Analytics]-Implementierungen nutzen, um die Konversionsereignisse (wie Öffnungen und Käufe) zu tracken, die [!DNL Target]-Algorithmen verbessern.

![Abbildung, die zeigt wie das Benutzerverhalten erfasst wird](/help/main/c-recommendations/assets/intro-9.png)

Sie müssen sicherstellen, dass [!DNL Target] weiß, welche Artikel Ihre Benutzer öffnen und kaufen. Wenn der Kauf für Ihren Kontext nicht relevant ist, sollten Sie einen anderen Konversionstyp verfolgen, z. B. das Herunterladen einer PDF, das Ausfüllen einer Umfrage, das Abonnieren eines Newsletters, das Ansehen eines Videos usw.

Wenn Sie [!DNL Target] bereits zum Durchführen von A/B-Tests auf Ihrer Site verwenden, haben Sie diesen Schritt möglicherweise bereits durchgeführt. Oder wenn Sie [!DNL Adobe Analytics] bereits dazu verwenden, Berichte zu Site-Besuchen und Konversionsverhalten zu erstellen, können Sie [!DNL Analytics] als Quelle für Ihre Verhaltensdaten verwenden. Andernfalls gestaltet sich die Einrichtung am einfachsten mithilfe eines Tag-Managers wie [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html?lang=de){target=_blank}. Es ist auch möglich, Offline- oder In-App-Interaktionen über die Echtzeit-API an [!DNL Target] zu senden.

### Erhalten von Empfehlungen mit dem richtigen Kontext

Übermitteln Sie Informationen über Benutzer und Kontext im Moment der Interaktion an [!DNL Target], um relevante und personalisierte Empfehlungen zurückzugeben.

![Abbildung, die zeigt, wie Empfehlungen mit dem richtigen Kontext abgerufen werden.](/help/main/c-recommendations/assets/intro-10.png)

Neben dem Benutzerverhalten in aggregierter Form müssen Sie [!DNL Target] den spezifischen Kontext übermitteln, in dem Empfehlungen angezeigt werden. Dazu gehören Informationen über die Seite und das Benutzerprofil. [!DNL Target] verwendet diese Informationen, um personalisierte Empfehlungen zu erstellen. Auf einer Einzelhandels-Website möchten Sie beispielsweise wissen, welches Produkt und welche Produktkategorie sich der Besucher momentan ansieht. Zusätzlich möchten Sie auch Informationen zu diesem Benutzer (Lieblingsmarke, bevorzugte Produktkategorie, Loyalitätsstufe usw.) wissen. Diese Informationen sind wichtig, damit [!DNL Target] Artikel filtern und die Personalisierung von Empfehlungen verbessern kann.

## Erstellen der ersten Recommendations-Aktivität

Was ist eine [!DNL Recommendations]-Aktivität?

![Abbildung mit den Teilen, aus denen eine gute Recommendations-Aktivität besteht](/help/main/c-recommendations/assets/intro-11.png)

Eine [!DNL Recommendations]-Aktivität besteht aus folgenden Komponenten:

* **Zielgruppe**: Wer soll diese Empfehlungen sehen?
* **Kriterien**: Welche Artikel sollen empfohlen werden?
* **Design**: Wie sollen die empfohlenen Artikel präsentiert werden?

![Abbildung einer Recommendations-Aktivität: Zielgruppen, Kriterien und Designs](/help/main/c-recommendations/assets/intro-12.png)

Standardmäßig enthält [!DNL Target] 14 integrierte Zielgruppen, 42 integrierte Kriterien und 10 integrierte Designvorlagen. Sie können jedes dieser Elemente anpassen oder eigene hinzufügen. Es gibt auch frühere [ zum Erstellen von Zielgruppen ](https://landing.adobe.com/acs/2018/na/adobe-target/registration.html) [!DNL Target]. In diesem Abschnitt wird beschrieben, wie die Kriterien definiert werden, aufgrund derer Artikel empfohlen werden.

Target verwendet das Konzept einer Kriterienkarte. Eine Kriterienkarte ist wie ein Rezept für die Personalisierung.

![Abbildung einer Kriterienkarte](/help/main/c-recommendations/assets/intro-13.png)

Die Auswahl oder Erstellung der richtigen Kriterien ist wichtig, um die gewünschten Personalisierungsergebnisse zu erzielen. Ein Kriterium ist wie ein Trichter, der Sie ausgehend vom gesamten Katalog zu Ihren endgültigen Empfehlungen führt.

![Abbildung des Trichters](/help/main/c-recommendations/assets/intro-14.png)

In den folgenden Abschnitten werden die einzelnen Teile dieses Trichters und deren Funktionsweise in [!DNL Target] beschrieben:

### Statische Filter (Sammlungen und Ausschlüsse)

Statische Filter sind allgemein anwendbare Regeln für Katalogattribute, die sich nicht häufig ändern.

![Abbildung von Sammlungen und Ausschlüssen](/help/main/c-recommendations/assets/intro-16.png)

In Bezug auf den Inhalt möchten Sie beispielsweise vielleicht alle Filme in Empfehlungen einbeziehen, aber Filme, die explizite sexuelle Inhalte haben, ausschließen. In Bezug auf den Einzelhandel verfügen Sie möglicherweise über mehrere Marken in verschiedenen Regionen der Welt. Sie möchten aber nur Produkte empfehlen, die in den USA verfügbar sind. Möglicherweise möchten Sie auch bestimmte Produkte einer regionalen Marke ausschließen.

Dies sind alles Katalogattribute, die allgemein anwendbar sind und die Sie möglicherweise in mehreren Empfehlungen verwenden möchten, und von denen nicht zu erwarten ist, dass sie sich häufig ändern.

### Algorithmus (Empfehlungsschlüssel und -logik)

Als nächsten Schritt müssen Sie einen Empfehlungsschlüssel und eine Empfehlungslogik auswählen. Hier legen Sie die Grundlage Ihrer Empfehlung fest.

![Abbildung eines Algorithmus](/help/main/c-recommendations/assets/intro-17.png)

Zunächst müssen Sie den Empfehlungsschlüssel auswählen. Der Empfehlungsschlüssel ist das gesuchte Objekt, aufgrund dessen eine Empfehlung ausgewählt wird. Er ist stellt die Basis einer Empfehlung dar.

Eine Empfehlung kann auf Folgendem basieren:

* Dem vom Besucher betrachteten Artikel
* Der vom Besucher betrachteten Kategorie
* Dem Artikel, den der Besucher zuletzt gekauft oder in den Warenkorb gelegt hat
* Einem benutzerspezifischen Attribut, das einem Besucher oder einem Artikel zugeordnet ist

Auf der Grundlage dieser Schlüssel wählen Sie dann die gewünschte Empfehlungslogik aus:

* Artikel mit ähnlichen Attributen
* Die am häufigsten angezeigten Artikel einer bestimmten Kategorie
* Kunden, die diesen Artikel gekauft haben, haben auch diese Artikel gekauft
* Ein benutzerdefiniertes Attribut

Standardmäßig enthält [!DNL Target] eine Reihe von Algorithmen.

![Abbildung der Algorithmen](/help/main/c-recommendations/assets/intro-15.png)

* Zu den **beliebtesten Algorithmen** zählen „Am häufigsten angesehen“ und „Am häufigsten gekauft“.
* Zu den **inhaltsbasierten Algorithmen** gehören „Ähnliche Inhalte“.
* **Algorithmen für artikelbasiertes kollaboratives Filtern** umfassen die Kategorien „Ansicht/Ansicht“, „Ansicht/Gekauft“ und „Gekauft/Gekauft“. Beachten Sie, dass „Gekauft“ jede beliebige Konversion sein kann.
* Zu den **personalisierten Algorithmen** zählen „Kürzlich angesehen“, „Site-Affinität“ und „Profiloptimiertes kollaboratives Filtern“.
* Sie können auch Ihre **eigenen benutzerdefinierte Algorithmen** verwenden.

### Online-Geschäftsregeln

Der letzte Schritt ist die Anwendung von Online-Geschäftsregeln. Damit versorgen Sie Ihre Algorithmen mit dem Domänenwissen und dem aktuellen Kontext, der darauf basiert, was der Besucher auf Ihrer digitalen Property gerade macht.

![Abbildung von Online-Geschäftsregeln](/help/main/c-recommendations/assets/intro-18.png)

Im Inhaltskontext möchten Sie beispielsweise vielleicht Filme ausschließen, die der Besucher bereits gesehen hat, oder Filme vom selben Regisseur oder im selben Genre empfehlen. Im Einzelhandelskontext möchten Sie möglicherweise nicht vorrätige Produkte ausschließen, Artikel im Preissegment von 5 bis 500 $ anzeigen oder Artikel derselben Marke empfehlen.

## Demo

Nachdem Sie die oben im Empfehlungstrichter beschriebenen Aufgaben ausgeführt haben, erhalten Sie Ihre endgültige Empfehlung. Sie können sich eine Produktdemonstration in [!DNL Target] ansehen. Das Demo beginnt um 21:00 Uhr im *Adobe Target Basics-Webinar*, das Sie über den unten stehenden Link erreichen.

## Adobe [!DNL Target] Basics-Webinar: Einführung in Recommendations {#intro-to-recs}

[Einführung in Recommendations](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)
