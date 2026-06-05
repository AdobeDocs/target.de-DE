---
keywords: Übersicht und Referenz;Aktivitäten;Einführung
description: Lernen Sie die Grundlagen von Adobe Target kennen. In diesem Artikel werden Target, dessen Typen von Aktivitäten und andere Funktionen vorgestellt.
title: Wie verwende ich Target?
feature: Overview
exl-id: c9555d79-d505-41ff-ba4b-ab94793f9efa
TQID: https://experienceleague.adobe.com/l4bZ9esCTiZNakTrNp89n5mAeFci5dp0HCLZYV-GleA
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
subfeature_v2:
  - id: b077c1f1-7e5f-4dbf-a193-70e9fe784bb2
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
  - id: c2923fce-066f-4e68-bc28-ac56b57ccb5c
  - id: ca2e0bf6-f9f8-4b6b-a630-a3c4b1455817
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
  - id: e73b329c-f712-4a22-abe7-bfbf3be6d0f9
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
  - id: f2d0aafb-18af-41a0-a32e-2788eafacc2b
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1538
ht-degree: 84%

---

# Wichtige Target-Konzepte

Informationen zu wichtigen Konzepten, die Sie beim Verstehen der Features und Funktionen von [!DNL Adobe Target] unterstützen.

## Aktivitäten und Tests {#section_BEA0A0C51A8847579B566060206DE7E8}

Eine Aktivität legt die Erlebnisse fest, auf die ein Site-Besucher stoßen kann.

Sie können z. B. eine Aktivität entwerfen, die zwei verschiedene Landingpages testet: eine, die Informationen zu Sommerschuhen für Damen hervorhebt, und eine, die allgemein Sommerbekleidung bewirbt. Durch die Aktivität werden die Bedingungen festgelegt, die steuern, wann diese beiden Landingpages angezeigt werden, sowie die Metriken, die bestimmen, welche Seite erfolgreicher ist. Die Aktivität ist so konfiguriert, dass sie beginnt und endet, wenn bestimmte Bedingungen erfüllt sind. Beispielsweise kann es sich bei den Bedingungen für den Beginn und das Ende einer Aktivität um ein bestimmtes Datum handeln, oder aber der Beginn erfolgt, wenn eine Aktivität genehmigt wird, und das Ende erfolgt, wenn sie deaktiviert wird.

Gehen Sie bei der Planung einer Aktivität sorgfältig vor. Bestimmen Sie, wann die Aktivität beginnen soll und wie lange sie dauern soll. Führen Sie dann Ihre Angebote auf, und weisen Sie jedem dieser Angebote eine Zielgruppe zu.

Target enthält mehrere Aktivitätstypen. In der folgenden Tabelle finden Sie einen Überblick über die einzelnen Aktivitätstypen mit Links, über die Sie mehr erfahren können. Damit Sie den Aktivitätstyp für Ihre Zwecke besser auswählen können, hat das Target-Team das [Adobe Target-Aktivitätshandbuch](/help/main/c-activities/target-activities-guide.md) erstellt.

| Aktivitätstyp | Beschreibung |
|--- |--- |
| [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) | A/B-Tests vergleichen zwei oder mehr Versionen des Inhalts Ihrer Website, um festzustellen, welche Version Ihre Konversionen während eines vorab festgelegten Testzeitraums am besten verbessert.<br>**Hinweis:** Sie können jetzt [Empfehlungen in A/B-Test-Aktivitäten einfügen](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |
| [Automatische Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Durch die automatische Zuordnung kann aus zwei oder mehr Erlebnissen das erfolgversprechendste ermittelt und dem Gewinner automatisch mehr Traffic zugewiesen werden, um die Konversionen während der Fortführung des Tests und des Lernens zu steigern.<br>**Hinweis:** Sie können jetzt [Empfehlungen in Aktivitäten mit automatisierter Zuordnung“ &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |
| [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/main/assets/premium.png) | Automatisches Targeting nutzt fortschrittliche Machine-Learning-Algorithmen zur Identifizierung eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketing-Experten definierten Erlebnissen. Automatische Targeting -Aktivitäten bieten jedem Besucher basierend auf seinem individuellen Kundenprofil und dem Verhalten früherer Besucher mit ähnlichen Profilen das passendste Erlebnis, um Inhalte zu personalisieren und Konversionen zu fördern.<br>**Hinweis:** Sie können jetzt [Empfehlungen in automatische Targeting -Aktivitäten einfügen](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |
| [Verwenden von Analytics-Daten](/help/main/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A4T) | Sie können eine Aktivität so konfigurieren, dass [!DNL Adobe Analytics] als Berichtsquelle verwendet wird. Für diesen Aktivitätstyp ist es erforderlich, dass Sie Ihr [!DNL Adobe Experience Cloud]-Konto sowohl mit [!DNL Analytics] als auch mit [!DNL Target] verbinden. |
| [Multivarianz-Test](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Beim Multivariate Testing (MVT) werden Kombinationen aus Angeboten in Elementen auf einer Seite verglichen, um zu bestimmen, welche Kombination die beste Leistung für eine bestimmte Zielgruppe erzielt. Zudem gibt er an, welches Element den größten Einfluss auf den Erfolg der Aktivität hat. |
| [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) | Beim Experience Targeting (XT) werden Inhalte für eine bestimmte Zielgruppe basierend auf einem Satz aus Regeln und Kriterien, die von den Werbungtreibenden definiert werden, bereitgestellt.<br>**Hinweis:** Sie können jetzt [Empfehlungen in Experience Targeting-Aktivitäten einfügen](/help/main/c-recommendations/recommendations-as-an-offer.md). Diese Funktion erfordert, dass Sie über eine [Target Premium-Lizenz](/help/main/c-intro/intro.md#premium) verfügen. |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/main/assets/premium.png) | Automated Personalization (AP) kombiniert Angebote oder Nachrichten und ordnet den einzelnen Besuchern basierend auf deren individuellem Kundenprofil durch erweitertes Machine Learning verschiedene Varianzen zu, um die Inhalte zu personalisieren und Konversionen zu fördern. |
| [Recommendations](/help/main/c-recommendations/recommendations.md)<br>![Target Premium](/help/main/assets/premium.png) | Eine Empfehlung bestimmt, wie ein Produkt dem Website-Benutzer je nach dessen Aktivitäten auf der Site vorgeschlagen werden soll.<br>So können Sie zum Beispiel Personen, die einen Rucksack kaufen, dazu anregen, den Kauf von Wanderschuhen und -stöcken zu erwägen. Mithilfe des „Kunden, die diesen Artikel gekauft haben, haben auch folgende Artikel gekauft“-Algorithmus können Sie eine Empfehlung erstellen, die Artikel anzeigt, welche oft zusammen gekauft werden. Oder Sie möchten Besucher ermutigen, mehr Zeit auf Ihrer Medienwebsite zu verbringen, indem Sie ihnen ähnliche Videos empfehlen, die sie gerade angesehen haben, und zwar mithilfe des Algorithmus „Personen, die diesen Algorithmus angezeigt haben“.<br>**Hinweis:** Sie können jetzt Empfehlungen in A/B-Tests (einschließlich automatisierter Zuordnung und automatischen Targetings) und Erlebnis-Targeting (XT) einbeziehen. Siehe [Empfehlungen als Angebot](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## Positionen {#section_F18FBF1ED23340ED9F39C51971A4E874}

Primär ist ein Ort eine Seite auf Ihrer Website. Dabei kann es sich auch um eine Stelle in einer mobilen App, einer E-Mail oder eine beliebige andere Stelle handeln, an der Sie eine Optimierung durchführen.

Orte sind grundlegend für Aktivitäten und Erlebnisse. Sie entscheiden, ob ein Ort eine der folgenden Aufgaben, beide Aufgaben oder keine ausführt:

* Anzeige und Austausch des Inhalts für Besucher
* Protokollierung des Besucherverhaltens

Bei [!DNL Target Standard] kann ein Ort ein beliebiges Element auf einer Seite sein, sofern die Seite eine einzelne Codezeile enthält, die [!DNL Target] im Abschnitt `<head>` jeder Seite aktiviert, die Sie verfolgen möchten. Diese Codezeile ruft die JavaScript-Bibliotheken auf, die für das Sammeln der Informationen und die Bereitstellung zielgerichteter Erlebnisse für Ihre Besucher erforderlich sind.

Standorte werden mit Zielgruppen kombiniert, um eine beinahe unendliche Anzahl von Optionen für die zielgerichtete Bereitstellung von Informationen für Ihre Kunden zur Verfügung zu stellen. So können Sie zum Beispiel einen Rabattcoupon für Neukunden einblenden, wenn ein Besucher die Site nie zuvor besucht hat. Gleichermaßen kann die Seite verändert werden, um Angebote anzuzeigen, die für wiederkehrende Kunden optimiert sind.

Sie können auch Standorte verwenden, um die Navigation eines Besuchers durch Ihre Website zu verfolgen. Zusätzlich können Sie Standorte dazu verwenden, um nachzuverfolgen, ob ein Besucher eine bestimmte Erfolgsmetrik aufweist, z. B. ob er einen Artikel zum Warenkorb hinzufügt oder einen Kauf abschließt.

## Erlebnisse und Seiten-Designs {#section_B806FB752EC1470784755C1EB3D4AC70}

Ein Erlebnis, manchmal auch als Rezept bezeichnet, definiert den Inhalt, der auf Ihrer Seite angezeigt wird, sowie andere Seitenelemente wie Links.

Ein Erlebnis bestimmt, welches Angebot an einem bestimmten Standort angezeigt wird, wenn die Targeting-Bedingungen zutreffen. Das Erlebnis legt beispielsweise fest, dass oben auf der Seite ein Angebot für den Versand innerhalb von zwei Tagen angezeigt wird, wenn ein Besucher zum wiederholten Mal Ihre Site besucht. Das Erlebnis legt außerdem fest, dass an der gleichen Stelle ein 10-prozentiger Rabatt angezeigt wird, wenn ein Besucher die Seite zum ersten Mal betrachtet.

Ein Erlebnis setzt sich aus Angeboten, Bild-Assets und anderen HTML-Elementen (wie Links) zusammen, die auf der Seite angezeigt werden, um den Besucher zu einem von Ihnen gewünschten Ergebnis zu führen. In [!DNL Target] werden Orte, Angebote und Erlebnisse kombiniert, um zu bestimmen, welcher Inhalt auf Ihrer Site während eines bestimmten Tests angezeigt wird.

Ein Erlebnis kann auch ein anderer Seitenentwurf sein. Zum Beispiel kann ein Erlebnis über eine Reihe von Links im oberen Teil der Seite verfügen, während ein anderes Erlebnis andere Links bzw. dieselben Links in einer anderen Anordnung enthält. Möglicherweise möchten Sie testen, ob ein Bild im Vergleich zu einem anderen eine größere Steigerung ermöglicht oder ob die Wahrscheinlichkeit, dass eine Anzeige angeklickt wird, oben auf Ihrer Seite höher ist als an einem anderen Ort.

[!DNL Target] optimiert die Erlebnisse für jeden Ihrer Besucher über Ihre digitalen Touchpoints hinweg und kann verschiedene Erlebnisse testen, um zu ermitteln, welche am erfolgreichsten sind. Wenn Sie das Targeting der Erlebnisse sorgfältig planen, können Sie sicherstellen, dass den Besuchern auf Ihrer Site die für sie relevantesten Angebote an den richtigen Stellen auf Ihrer Seite angezeigt werden. Und so verbessern Sie Ihre Chancen auf einen erfolgreichen Besuch.

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

## Zielgruppen {#section_3F32DA46BDF947878DD79DBB97040D01}

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
| Freigegebene Zielgruppen | Zielgruppen können über [!DNL Adobe Experience Cloud]-Lösungen hinweg freigegeben werden. Beispiele finden Sie unter [Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=de). |

Informationen darüber, wie das Besucherprofil Informationen über Besucher auf Ihrer Seite verfolgt, finden Sie unter [Besucherprofile](/help/main/c-target/c-visitor-profile/visitor-profile.md#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1).

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Aktivitätstypen (9:03) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video werden die in [!DNL Target Standard/Premium] verfügbaren Aktivitätstypen erläutert.

* Beschreiben der Aktivitätstypen in [!DNL Adobe Target]
* Auswählen des für Ihre Ziele geeigneten Aktivitätstyps
* Beschreibung des für alle Aktivitätstypen gültigen Arbeitsablaufs mit drei Schritten

>[!VIDEO](https://video.tv.adobe.com/v/29397?captions=ger)

### Verwenden von Zielgruppen in Adobe Target (6:21) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video wird erläutert, wie sich Zielgruppen in [!DNL Target Standard/Premium] einsetzen lassen.

* Erläuterung des Begriffs „Zielgruppe“
* Erläuterung der beiden Arten, auf die Zielgruppen zur Optimierung eingesetzt werden
* Auffinden von Zielgruppen in der Zielgruppenliste
* Zuordnung einer Aktivität zu einer Zielgruppe
* Verwenden von Zielgruppen für die passive Berichterstattung zu einer Aktivität

>[!VIDEO](https://video.tv.adobe.com/v/29395?captions=ger)
