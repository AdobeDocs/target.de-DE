---
keywords: Übersicht und Referenz;Aktivitäten;Einführung
description: Lernen Sie die Grundlagen von Adobe Target kennen. In diesem Artikel werden Zielgruppen, Typen von Aktivitäten und andere Funktionen vorgestellt.
title: Wie verwende ich Zielgruppe?
feature: Overview
exl-id: c9555d79-d505-41ff-ba4b-ab94793f9efa
translation-type: tm+mt
source-git-commit: 094756ac64e2740e81834fde4b07d4b643ac39b9
workflow-type: tm+mt
source-wordcount: '1528'
ht-degree: 83%

---

# Wichtige Target-Konzepte

Informationen zu wichtigen Konzepten, die Ihnen helfen, die Funktionen von [!DNL Adobe Target] zu verstehen.

## Aktivitäten und Tests {#section_BEA0A0C51A8847579B566060206DE7E8}

Eine Aktivität legt die Erlebnisse fest, auf die ein Site-Besucher stoßen kann.

Sie können z. B. eine Aktivität entwerfen, die zwei verschiedene Landingpages testet: eine, die Informationen zu Sommerschuhen für Damen hervorhebt, und eine, die allgemein Sommerbekleidung bewirbt. Durch die Aktivität werden die Bedingungen festgelegt, die steuern, wann diese beiden Landingpages angezeigt werden, sowie die Metriken, die bestimmen, welche Seite erfolgreicher ist. Die Aktivität ist so konfiguriert, dass sie bei Erfüllung bestimmter Bedingungen zum Beginn und zum Ende gebracht wird. Diese Bedingungen können das Starten und Beenden der Aktivität zwischen bestimmten Daten oder bis zum Beginn der Genehmigung der Aktivität und das Ende der Deaktivierung umfassen.

Planen Sie beim Entwerfen einer Aktivität sorgfältig. Bestimmen Sie, wann die Aktivität Beginn und wie lange sie dauert. Führen Sie dann Ihre Angebote auf, und weisen Sie jedem dieser Angebote eine Zielgruppe zu.

Target enthält mehrere Aktivitätstypen. In der folgenden Tabelle finden Sie einen Überblick über die einzelnen Aktivitätstypen mit Links, über die Sie mehr erfahren können. Um Ihnen bei der Auswahl der besten Aktivität zu helfen, hat das Zielgruppe-Team auch den [Adobe Target Aktivitäten Guide](/help/c-activities/target-activities-guide.md) erstellt.

| Aktivitätstyp | Beschreibung |
|--- |--- |
| [A/B-Test](/help/c-activities/t-test-ab/test-ab.md) | Beim A/B-Test werden zwei oder mehr Versionen Ihrer Website-Inhalte verglichen, um festzustellen, mit welcher Version Ihre Konversionen in einem vorab festgelegten Zeitraum verbessert werden.<br>**Hinweis:** Sie können [nun Empfehlungen in A/B-Test-Aktivitäten einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/c-intro/intro.md#premium) verfügen. |
| [Automatische Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Die Funktion „Automatisch zuweisen“ identifiziert einen Gewinner unter zwei oder mehr Erlebnissen und ordnet dem Gewinner automatisch mehr Traffic zu, um Konversionen zu erhöhen, während der Test weiter ausgeführt und das Lernen fortgesetzt wird.<br>**Hinweis:** Sie können jetzt [Empfehlungen in Aktivitäten mit automatisiertem Targeting einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/c-intro/intro.md#premium) verfügen. |
| [Automatisches Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/assets/premium.png) | Die automatische Zielgruppe verwendet fortschrittliches maschinelles Lernen, um mehrere leistungsstarke, von Marketingexperten definierte Erlebnisse zu identifizieren. Die Aktivitäten der automatischen Zielgruppe bieten den Besuchern das maßgeschneiderte Erlebnis auf der Grundlage ihres individuellen Profils und des Verhaltens früherer Besucher mit ähnlichen Profilen, um Inhalte zu personalisieren und Konversionen zu fördern.<br>**Hinweis:** Sie können nun [Empfehlungen in Aktivitäten mit automatischem Targeting einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/c-intro/intro.md#premium) verfügen. |
| [Verwenden von Analytics-Daten](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A4T) | Sie können eine Aktivität so konfigurieren, dass [!DNL Adobe Analytics] als Berichtsquelle verwendet wird. Für diesen Aktivitätstyp ist es erforderlich, dass Sie Ihr [!DNL Adobe Experience Cloud]-Konto sowohl mit [!DNL Analytics] als auch mit [!DNL Target] verbinden. |
| [Multivarianz-Test](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Beim Multivariate Tests (MVT) werden Kombinationen aus Angeboten in Elementen auf einer Seite verglichen, um zu bestimmen, welche Kombination die beste Leistung für eine bestimmte Zielgruppe erzielt. Zudem gibt er an, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. |
| [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md) | Beim Erlebnis-Targeting (XT) werden Inhalte für eine spezielle Zielgruppe basierend auf einem Satz aus vermarkterdefinierten Regeln und Kriterien bereitgestellt.<br>**Hinweis:** Sie können [nun Empfehlungen in Erlebnis-Targeting-Aktivitäten einfügen](/help/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/c-intro/intro.md#premium) verfügen. |
| [Automatisierte Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/assets/premium.png) | Die automatisierte Personalisierung (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf deren individuellem Kundenprofil mithilfe des erweiterten maschinellen Lernens verschiedene Variationen zu, um die Inhalte zu personalisieren und Konversionen zu fördern. |
| [Recommendations](/help/c-recommendations/recommendations.md)<br>![Target Premium](/help/assets/premium.png) | Eine Empfehlung bestimmt, wie ein Produkt dem Website-Benutzer je nach dessen Aktivitäten auf der Site vorgeschlagen werden soll.<br>So können Sie zum Beispiel Personen, die einen Rucksack kaufen, dazu anregen, den Kauf von Wanderschuhen und -stöcken zu erwägen. Mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Algorithmus können Sie eine Empfehlung erstellen, die Artikel anzeigt, welche oft zusammen gekauft werden. Oder Sie können Besucher dazu anregen, mehr Zeit auf Ihrer Medienwebsite zu verbringen, indem Sie mithilfe des „Personen, die dieses Video angesehen haben, sahen auch“-Algorithmus Videos empfehlen, die dem angezeigten Video ähneln.<br>**Hinweis:** Sie können jetzt Empfehlungen in A/B-Tests (einschließlich automatisierter Zuordnung und automatischesm Targeting) und Erlebnis-Targeting (XT) einbeziehen. Siehe [Empfehlungen als Angebot](/help/c-recommendations/recommendations-as-an-offer.md). |

## Orte {#section_F18FBF1ED23340ED9F39C51971A4E874}

Primär ist ein Ort eine Seite auf Ihrer Website. Dabei kann es sich auch um eine Stelle in einer mobilen App, einer E-Mail oder eine beliebige andere Stelle handeln, an der Sie eine Optimierung durchführen.

Orte sind grundlegend für Aktivitäten und Erlebnisse. Sie entscheiden, ob ein Ort eine der folgenden Aufgaben, beide Aufgaben oder keine ausführt:

* Anzeige und Austausch des Inhalts für Besucher
* Protokollierung des Besucherverhaltens

Bei [!DNL Target Standard] kann ein Ort ein beliebiges Element auf einer Seite sein, sofern die Seite eine einzelne Codezeile enthält, die [!DNL Target] im Abschnitt `<head>` jeder Seite aktiviert, die Sie verfolgen möchten. Diese Codezeile ruft die JavaScript-Bibliotheken auf, die für das Sammeln der Informationen und die Bereitstellung zielgerichteter Erlebnisse für Ihre Besucher erforderlich sind.

Standorte werden mit Zielgruppen kombiniert, um eine beinahe unendliche Anzahl von Optionen für die zielgerichtete Bereitstellung von Informationen für Ihre Kunden zur Verfügung zu stellen. So können Sie zum Beispiel einen Rabattcoupon für Neukunden einblenden, wenn ein Besucher die Site nie zuvor besucht hat. Gleichermaßen kann die Seite verändert werden, um Angebote anzuzeigen, die für wiederkehrende Kunden optimiert sind.

Sie können Orte auch verwenden, um den Fortschritt eines Besuchers durch Ihre Website zu verfolgen. Sie können Orte auch dazu verwenden, nachzuverfolgen, ob der Besucher eine bestimmte Erfolgsmetrik abschließt, z. B. einen Artikel zum Warenkorb hinzuzufügen oder einen Kauf abzuschließen.

## Erlebnisse und Seiten-Designs {#section_B806FB752EC1470784755C1EB3D4AC70}

Ein Erlebnis, manchmal auch als Rezept bezeichnet, definiert den Inhalt, der auf Ihrer Seite angezeigt wird, sowie andere Seitenelemente wie Links.

Ein Erlebnis bestimmt, welches Angebot an einem bestimmten Standort angezeigt wird, wenn die Targeting-Bedingungen zutreffen. Das Erlebnis legt beispielsweise fest, dass oben auf der Seite ein Angebot für den Versand innerhalb von zwei Tagen angezeigt wird, wenn ein Besucher zum wiederholten Mal Ihre Site besucht. Das Erlebnis legt außerdem fest, dass an der gleichen Stelle ein 10-prozentiger Rabatt angezeigt wird, wenn ein Besucher die Seite zum ersten Mal betrachtet.

Ein Erlebnis setzt sich aus Angeboten, Bild-Assets und anderen HTML-Elementen (wie Links) zusammen, die auf der Seite angezeigt werden, um den Besucher zu einem von Ihnen gewünschten Ergebnis zu führen. In [!DNL Target] werden Orte, Angebote und Erlebnisse kombiniert, um zu bestimmen, welcher Inhalt auf Ihrer Site während eines bestimmten Tests angezeigt wird.

Ein Erlebnis kann auch ein anderer Seitenentwurf sein. Zum Beispiel kann ein Erlebnis über eine Reihe von Links im oberen Teil der Seite verfügen, während ein anderes Erlebnis andere Links bzw. dieselben Links in einer anderen Anordnung enthält. Möglicherweise möchten Sie testen, ob ein Bild im Vergleich zu einem anderen eine größere Steigerung ermöglicht oder ob die Wahrscheinlichkeit, dass eine Anzeige angeklickt wird, oben auf Ihrer Seite höher ist als an einem anderen Ort.

[!DNL Target] optimiert Erlebnisse für jeden Ihrer Besucher für sämtliche digitalen Touchpoints und ermöglicht Ihnen, verschiedene Erlebnisse zu testen, um zu ermitteln, welche am erfolgreichsten sein werden. Wenn Sie das Targeting der Erlebnisse sorgfältig planen, können Sie sicherstellen, dass den Besuchern auf Ihrer Site die für sie relevantesten Angebote an den richtigen Stellen auf Ihrer Seite angezeigt werden. Und so verbessern Sie Ihre Chancen auf einen erfolgreichen Besuch.

## Angebote {#section_973D4CC4CEB44711BBB9A21BF74B89E9}

Ein Angebot ist der Inhalt, der während Kampagnen oder Aktivitäten auf Ihren Webseiten angezeigt wird.

Wenn Sie Ihre Webseiten testen, messen Sie den Erfolg jedes Erlebnisses mit verschiedenen Angeboten in Ihren Orten.

Ein Angebot kann verschiedene Inhaltsarten enthalten, wie zum Beispiel:

* Bild
* Text
* HTML
* Link
* Schaltfläche

Beispielsweise kann eine Webseite eines von zwei Angeboten anzeigen, abhängig davon, ob der Besucher Ihre Site zuvor besucht hat.

Ein *Erlebnis* bestimmt, welcher Inhalt angezeigt wird, wenn bestimmte Bedingungen zutreffen.

## Zielgruppen{#section_3F32DA46BDF947878DD79DBB97040D01}

Optimieren Sie Ihren zielgerichteten Inhalt für Aktivitätsteilnehmer, die spezifische Kriterien erfüllen.

Zielgruppen definieren das Ziel für Ihre Aktivität und können überall dort verwendet werden, wo Targeting verfügbar ist.

[!DNL Target]-Zielgruppen sind ein festgelegter Satz von Besucherkriterien. Angebote können auf spezifische Zielgruppen (oder Segmente) ausgerichtet werden. Nur Besucher, die dieser Zielgruppe angehören, sehen das auf sie zugeschnittene Erlebnis.

So können Sie beispielsweise eine Aktivität auf eine Zielgruppe ausrichten, die sich aus Besuchern zusammensetzt, welche einen bestimmten Browser bzw. ein bestimmtes Betriebssystem verwenden.

Sie können auch eine Aktivität auf Besucher aus einer bestimmten geografischen Region oder auf Personen, die über eine bestimmte Suchmaschine auf Ihre Seite zugreifen, ausrichten.

Zielgruppen können zur Wiederverwendung in verschiedenen Aktivitäten gespeichert oder für eine spezifische Aktivität erstellt werden.

| Zielgruppentyp | Beschreibung |
|--- |--- |
| Wiederverwendbare Zielgruppen | Wiederverwendbare Zielgruppen können für beliebige Aktivitäten ausgewählt werden. Wird eine dieser Zielgruppen verändert, so wird sie für alle Aktivitäten verändert, die diese Zielgruppe verwenden. |
| Benutzerdefinierte Segmente | Benutzerdefinierte Segmente (auch kampagnenspezifische Segmente) sind spezifisch für eine Kampagne in Target Classic. Sie werden als Teil der Kampagne erstellt und können nicht in anderen Kampagnen wiederverwendet werden. |
| Freigegebene Zielgruppen | Zielgruppen können über [!DNL Adobe Experience Cloud]-Lösungen hinweg freigegeben werden. Beispiele finden Sie unter [Audiencen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html). |

Informationen darüber, wie das Besucherprofil Informationen über Besucher auf Ihrer Seite verfolgt, finden Sie unter [Besucherprofile](/help/c-target/c-visitor-profile/visitor-profile.md#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1).

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitäten (9:03) ![Übersichtskennzeichen](/help/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreibung der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Verwenden von Audiencen in Adobe Target (6:21) ![Kennzeichen ](/help/assets/overview.png)

In diesem Video wird erläutert, wie sich Zielgruppen in [!DNL Target Standard/Premium] einsetzen lassen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/17398)
