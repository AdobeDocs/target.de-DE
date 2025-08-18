---
keywords: Recommendations; Recommendations-Kriterien; Recommendations-Algorithmen; Recommendations-Aktivität; Kriterien; Targeting mit Recommendations; Recs
description: Erfahren Sie mehr über Recommendations-Aktivitäten in Adobe  [!DNL Target] . Diese zeigen automatisch Inhalte an, die basierend auf früheren Benutzeraktivitäten oder anderen Algorithmen für Ihre Kunden interessant sein könnten.
title: Was ist  [!DNL Target]  Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 0d986e17-bc99-4c08-a963-7f9a6619609a
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 97%

---

# Recommendations

[!DNL Adobe Target Recommendations]-Aktivitäten zeigen automatisch Produkte oder Inhalte an, die basierend auf früheren Benutzeraktivitäten, Einstellungen oder anderen Algorithmen für Ihre Besucher interessant sein könnten. [!DNL Target Recommendations] helfen, Besucher zu relevanten Inhalten zu führen, von denen sie andernfalls möglicherweise nichts erfahren hätten. [!DNL Recommendations] ermöglichen Ihnen die Bereitstellung relevanter Inhalte für Ihre Besucher – zum richtigen Zeitpunkt und an der richtigen Stelle.

>[!NOTE]
>
>[!DNL Recommendations] Aktivitäten sind als Bestandteil der [Target Premium-Lösung](/help/main/c-intro/intro.md#premium) verfügbar. Sie sind in [!DNL Target Standard] nicht ohne [!DNL Target Premium]-Lizenz verfügbar.
>
>Falls Sie aktuell [!DNL Recommendations Classic] haben, finden Sie weitere Informationen zu den beiden Lösungen unter [Recommendations Classic versus Recommendations Activities in Target Premium](/help/main/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5).

[!DNL Recommendations] unterstützt Sie dabei, Echtzeitvorschläge über verschiedene Kanäle, Apps, Seiten, E-Mails und andere Bereitstellungsoptionen hinweg zu optimieren und zu personalisieren, um Interaktionen und Konversionen zu steigern, während gleichzeitig der Verwaltungsaufwand sinkt.

[!DNL Recommendations] hilft Ihnen bei Folgendem:

* Komplexe Kriterien (Regeln) zur Automatisierung von Empfehlungen erstellen
* Empfehlungen automatisch anzeigen, indem Sie einige wenige JavaScript-Snippets einsetzen
* Empfehlungskriterien und -entwürfe, die Empfehlungen anzeigen, testen und optimieren
* Berichte zu den Ergebnissen Ihrer Empfehlungsaktivitäten erstellen

Die folgende Illustration stellt Recommendations auf einer Webseite dar:

![velocity_example image](assets/velocity_example.png)

Eine Recommendation bestimmt, wie ein Produkt einem Besucher je nach dessen Aktivitäten auf der Site vorgeschlagen wird. Beispiel:

| Wunschaktion | Empfehlung |
|--- |--- |
| Regen Sie Personen, die einen Rucksack kaufen, dazu an, Wanderschuhe und Wanderstöcke zu kaufen. | Erstellen Sie mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Kriteriums eine Empfehlung, die Artikel anzeigt, welche oft zusammen gekauft werden. |
| Steigern Sie die Zeit, die ein Besucher auf Ihrer Medienwebsite verbringt, indem Sie Videoinhalte empfehlen, die den gerade angesehenen Videos ähneln. | Erstellen Sie mithilfe des „Personen, die dies angesehen haben, sahen auch“-Kriteriums eine Empfehlung, die andere Videos vorschlägt. |
| Empfehlen Sie Kunden, die sich Informationen über Sparpläne bei Ihrer Bank angesehen haben, Informationen zu IRA-Konten. | Zeigen Sie mithilfe des „Personen, die diesen Artikel angesehen haben, kauften auch“-Kriteriums andere Produkte, die von Personen gekauft wurden, nachdem sie ein Produkt angesehen haben, ohne dabei das erste Produkt in den Empfehlungen anzuzeigen. |

Weitere Informationen zu diesen und anderen [!DNL Recommendations]-Kriterien finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Begriffe

Bevor Sie mit der Arbeit mit [!DNL Recommendations] beginnen, sollten Sie sich mit einigen der in diesem Abschnitt verwendeten Begriffe vertraut machen. Machen Sie sich keine Gedanken, wenn Sie diese Begriffe noch nicht vollständig verstehen. Sie werden Ihnen, während Sie Ihre [!DNL Recommendations]-Aktivitäten einrichten, immer vertrauter werden.

| Begriff | Definition |
| --- | --- |
| Aktivität | Mit den Aktivitäten in [!DNL Target] können Sie Inhalte an bestimmte Zielgruppen anpassen und Ihre Seitendesigns testen. [!DNL Recommendations] ist nur einer der vielen Aktivitätstypen in [!DNL Target]. Weitere Informationen finden Sie unter [Target-Aktivitätstypen](/help/main/c-activities/target-activities-guide.md). |
| Entitäten | Entitäten beziehen sich auf die Artikel, die Sie empfehlen möchten. Entitäten können sich auf Verschiedenes beziehen, etwa auf Produkte, Inhalte (Artikel, Slideshows, Bilder, Filme und Fernsehsendungen), Stellenausschreibungen, Restaurants und so weiter. Weitere Informationen finden Sie unter [Entitäten](/help/main/c-recommendations/c-products/products.md). |
| Feeds | Mit Feeds werden Entitäten in [!DNL Recommendations] importiert. Entitäten können mithilfe von CSV-Dateien, dem Google-Produktsuche-Feedformat und Adobe Analytics-Classifications gesendet werden. Weitere Informationen finden Sie unter [Feeds](/help/main/c-recommendations/c-products/feeds.md). |
| Katalog | Kataloge beziehen sich auf den gesamten Produktsatz (Entitäten). Ihr Katalog kann viele Sammlungen enthalten – eine Möglichkeit, Ihre Produkte in logischen Buckets zu organisieren. |
| Sammlung | Sammlungen beziehen sich auf eine Reihe ähnlicher oder verwandter Elemente, z. B. eine einzelne Produktkategorie. Sie können jedoch beliebige Artikel in einer Kategorie gruppieren, wenn dies für Ihr Geschäft sinnvoll ist, wie zum Beispiel Produkte in einer bestimmten Preisspanne bzw. mit einer bestimmten Farbe, oder Artikel, die wahrscheinlich in einer bestimmten geografischen Region interessant sind. Weitere Informationen finden Sie unter [Sammlungen](/help/main/c-recommendations/c-products/collections.md). |
| Kriterien | Kriterien sind Regeln, die auf Basis vorab ermittelter Verhaltensweisen von Besuchern festlegen, welche Produkte empfohlen werden.<br>Einige Beispiele für Kriterien sind: <ul><li>Personen, die das kauften, kauften dies</li><li>Personen, die das ansahen, sahen auch dies an</li><li>Artikel mit ähnlichen Attributen</li><li>Zuletzt gekaufter Artikel</li><li>Favoritenkategorie</li></ul>  Weitere Informationen finden Sie unter [Kriterien](/help/main/c-recommendations/c-algorithms/algorithms.md). |
| Designs | Designs definieren das Erscheinungsbild der Recommendations in einer [!DNL Recommendations]-Aktivität, beispielsweise in einer Zeile, Spalte, Tabelle oder einem Raster. Die Abbildung oben in diesem Artikel zeigt ein 4 x 1-Design. Weitere Informationen finden Sie unter [Erstellen eines Designs](/help/main/c-recommendations/c-design-overview/create-design.md). |
| Positionen | Positionen beziehen sich auf einen bestimmten Inhaltsbereich auf einer Webseite, in einer mobilen App oder einer E-Mail, in dem Sie eine Aktivität zu Personalisierungs- und Optimierungszwecken ausführen. |
| Zielgruppen | Eine Zielgruppe ist eine Gruppe ähnlicher Aktivitätsteilnehmer, denen die Ergebnisse einer ausgewählten Aktivität dargestellt wird. Eine Zielgruppe ist eine Gruppe von Personen mit denselben Merkmalen, wie z. B. ein neuer Besucher, ein wiederkehrender Besucher oder wiederkehrende Besucher aus einer bestimmten Region. Mit der Zielgruppenfunktion können Sie Ihre Inhalte und Erlebnisse speziell an bestimmte Zielgruppen anpassen. Durch geeignete Botschaften zum richtigen Zeitpunkt für die richtigen Personen können Sie so Ihr digitales Marketing optimieren. Weitere Informationen finden Sie unter [Zielgruppen](/help/main/c-target/target.md). |
| Recommendations als Angebot | Eine Funktion, die die Einbeziehung von Recommendations in Aktivitäten für A/B-Tests (einschließlich automatischer Zuordnung und automatischen Targetings) und Erlebnis-Targeting (XT) zulässt. Weitere Informationen finden Sie unter [Recommendations als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## Schulungsvideo: Aktivitätstypen ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert. [!DNL Recommendations] wird ab 7 :20 besprochen.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Adobe Target Basics-Webinar: Einführung in Recommendations ![Tutorial-Badge](/help/main/assets/tutorial.png) {#intro-to-recs}

Das Webinar *„Einführung in Recommendations“* beinhaltet eine ausführliche Untersuchung, wie der Wert von [!DNL Adobe Target Recommendations] wirksam eingesetzt werden kann. Erfahren Sie, wie diese [!DNL Target]-Aktivität automatisch Produkte oder Inhalte anzeigt, die für Ihre Kunden von Interesse sein könnten, indem sie Echtzeitvorschläge auf der Grundlage früherer Besuche optimiert. Außerdem können Sie in die [!DNL Target]-Benutzeroberfläche eintauchen, um eine schrittweise Übersicht über das Erstellen einer [!DNL Recommendations]-Aktivität zu erhalten.

[Einführung in Recommendations](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)
