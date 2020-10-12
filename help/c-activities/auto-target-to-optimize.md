---
keywords: auto-target;targeting;traffic allocation;frequently aske questions;faq;troubleshooting;trouble shooting
description: Die automatische Zielgruppe in Adobe Target verwendet fortschrittliches maschinelles Lernen, um aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen auszuwählen, um Inhalte zu personalisieren und Konversionen zu fördern. Automatisches Targeting stellt das benutzerspezifische Erlebnis für jeden Besucher basierend auf seinem individuellen Kundenprofil und dem Verhalten voriger Besucher mit ähnlichen Profilen bereit.
title: Automatisches Targeting
feature: auto-target
topic: Standard
uuid: fce769d2-9e7f-4064-add7-76e1fc394b4f
translation-type: tm+mt
source-git-commit: 5675672777c778676b878dee2f713b16bc62bc1e
workflow-type: tm+mt
source-wordcount: '3744'
ht-degree: 83%

---


# ![PREMIUM](/help/assets/premium.png) Automatisches Targeting

[!UICONTROL Automatisches Targeting] verwendet fortschrittliches maschinelles Lernen, um aus mehreren leistungsstarken Erlebnissen mit Marketingexperten auswählen zu können, um Inhalte zu personalisieren und Konversionen zu fördern. Automatisches Targeting stellt das benutzerspezifische Erlebnis für jeden Besucher basierend auf seinem individuellen Kundenprofil und dem Verhalten voriger Besucher mit ähnlichen Profilen bereit.

>[!NOTE]
>
>[!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/c-intro/intro.md).

## Echtzeit-Erfolgsgeschichte mit automatisierter Zielgruppe {#success}

Ein großer Bekleidungshändler hat kürzlich eine [!UICONTROL Auto-Zielgruppe] -Aktivität mit zehn produktbasierten Erlebnissen (plus zufälliger Kontrolle) verwendet, um den richtigen Inhalt für jeden Besucher bereitzustellen. &quot;[!UICONTROL Hinzufügen zum Warenkorb]&quot;wurde als primäre Optimierungsmetrik gewählt. Die angestrebten Erlebnisse stiegen im Durchschnitt um 29,09 %. Nach der Erstellung der [!UICONTROL Automatisch Zielgruppe] Modelle wurde die Aktivität auf 90 % personalisierte Erlebnisse eingestellt.

In nur zehn Tagen wurden mehr als 1.700.000 Dollar an Steigerungen erzielt.

Lesen Sie weiter, um zu erfahren, wie Sie mit der [!UICONTROL automatischen Zielgruppe] die Steigerung und den Umsatz in Ihrem Unternehmen steigern.

## Überblick {#section_972257739A2648AFA7E7556B693079C9}

Beim [Erstellen einer A/B-Aktivität mit einem geleiteten Arbeitsablauf in drei Schritten](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) können Sie Traffic mithilfe der Option [!UICONTROL Automatisches Targeting für personalisierte Erlebnisse] zuordnen:

![Automatisches Targeting für personalisierte Erlebnisse](/help/c-activities/assets/auto-target-ui-new.png)

Mit der Option [!UICONTROL Automatisches Targeting] im A/B-Aktivitätsfluss können Sie maschinelles Lernen nutzen, damit basierend auf einer Reihe von Erlebnissen, die von Marketingexperten definiert wurden, personalisiert wird. [!UICONTROL Automatisches Targeting] soll im Vergleich zum herkömmlichen A/B-Test oder „Automatisch zuweisen“ eine maximale Optimierung bereitstellen, indem bestimmt wird, welches Erlebnis welchem Besucher angezeigt wird. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden, bestimmt [!UICONTROL Automatisches Targeting] automatisch das beste Erlebnis für einen bestimmten Besucher (basierend auf seinem Profil und anderen Kontextinformationen), um ein maximal personalisiertes Erlebnis bereitzustellen.

Ähnlich wie bei der automatisierten Personalisierung verwendet [!UICONTROL Automatisches Targeting] einen Random Forest-Algorithmus, eine führende Methode in der Datenwissenschaft, um das beste Erlebnis für einen Besucher zu ermitteln. Da sich [!UICONTROL Automatisches Targeting] an Änderungen im Besucherverhalten anpassen kann, kann es dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Dies wird manchmal auch als „Always-on“-Modus bezeichnet.

Im Gegensatz zu einer A/B-Aktivität, bei der die Erlebniszuordnung an einen bestimmten Besucher gebunden ist, optimiert [!UICONTROL Automatisches Targeting] das angegebene Geschäftsziel im Verlauf der einzelnen Besuche. Wie in [!UICONTROL Automatisierte Personalisierung] reserviert[!UICONTROL  Automatisches Targeting] standardmäßig einen Teil des Traffics der Aktivität als Kontrollgruppe zum Messen der Steigerung. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

## Zu beachten

There are a few important considerations to keep in mind when using [!UICONTROL Auto-Target]:

* Es ist nicht möglich, eine bestimmte Aktivität von [!UICONTROL Automatisches Targeting] in „Automatisierte Personalisierung“ umzuschalten und umgekehrt.
* Es ist nicht möglich, von der manuellen Traffic-Zuordnung (herkömmlicher A/B-Test) zu [!UICONTROL Automatisches Targeting] und umgekehrt zu wechseln, sobald eine Aktivität aktiv ist.
* Ein Modell wird erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic im Vergleich zum Senden des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu identifizieren. Bei diesem Modell werden Treffer und Konversionen nur in der Standard-Umgebung berücksichtigt.

   Traffic aus einem zweiten Satz von Modellen wird für jede Modellgruppe (AP) oder Erlebnis (AT) erstellt. Bei jedem dieser Modelle werden Treffer und Konversionen in allen Umgebung berücksichtigt.

   Anfragen werden daher unabhängig von der Umgebung mit demselben Modell bedient, aber die Datenverkehrsvielfalt sollte von der Standardeinstellung ausgehen, um sicherzustellen, dass das identifizierte Gesamterlebnis mit dem realen Umgebung übereinstimmt.

* Es müssen mindestens zwei Erlebnisse verwendet werden.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

Bei Erörterungen zu [!UICONTROL Automatisches Targeting] sind die folgenden Begriffe hilfreich:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Random Forest ist ein führender Ansatz beim maschinellen Lernen. Im Datenwissenschaftlerjargon ist dies eine Ensemble-Classification- oder Regressionsmethode, die auf der Grundlage von Besuchern und Besuchsattributen eine große Anzahl von Entscheidungsbäumen erstellt. Random Forest wird von Target eingesetzt, um zu bestimmen, welches Erlebnis die höchste Wahrscheinlichkeit einer Konversion (oder den höchsten Umsatz pro Besuch) für jeden einzelnen Besucher hat. Weitere Informationen zu Random Forest in Target finden Sie unter  [Random Forest-Algorithmus](../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA). |
| Thompson Sampling | Ziel des Thompson Samplings ist es, festzustellen, welches (nicht personalisierte) Erlebnis insgesamt das beste ist, während gleichzeitig die „Kosten“ für die Auffindung dieses Erlebnisses minimiert werden. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Funktionsweise von [!UICONTROL Automatisches Targeting] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Unter den folgenden Links erhalten Sie weitere Informationen über Daten und Algorithmen, die den Funktionen [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ zugrunde liegen:

| Begriff | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist der wichtigste Personalisierungsalgorithmus von Target; er wird in [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendet. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere Prognoseleistung zu erzielen, als dies bei der isolierten Verwendung dieser Lernalgorithmen möglich wäre. Der Random Forest-Algorithmus des automatisierten Personalisierungssystems ist eine Classification- oder Regressionsmethode, deren Funktionsweise die Konstruktion einer Vielzahl von Entscheidungsbäumen während der Anlernzeit zugrunde liegt. |
| [Hochladen von Daten für die Personalisierungsalgorithmen von Target](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Es gibt mehrere Möglichkeiten, um Daten für die Modelle [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ einzugeben. |
| [Datenerfassung für die Target-Personalisierungsalgorithmen](/help/c-activities/t-automated-personalization/ap-data.md) | Die Personalisierungsalgorithmen von Target erfassen automatisch eine Vielzahl von Daten. |

## Bestimmen der Traffic-Zuordnung  {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach dem Ziel Ihrer Aktivität können Sie eine unterschiedliche Traffic-Zuordnung zwischen den Kontroll- und personalisierten Erlebnissen auswählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdownliste [!UICONTROL Zuordnung anpassen] können Sie aus den folgenden Optionen auswählen:

* Personalisierungsalgorithmus auswerten
* Personalisierungs-Datenverkehr maximieren
* Zuordnung anpassen

![Dropdown-Liste für das Zuordnungsziel](/help/c-activities/assets/split-new.png)

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **Personalisierungsalgorithmus auswerten (50/50)**: Wenn Sie den Algorithmus testen möchten, sollten Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus verwenden. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit „zufällige Erlebnisse“ als Kontrolle empfohlen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ gesehen erhalten weniger Besucher ein personalisiertes Erlebnis</li></ul> |
| **Personalisierungs-Datenverkehr maximieren (90/10)**: Wenn Sie eine „Always on“-Aktivität erstellen möchten, sollten Sie 10 % der Besucher in den Kontrollbereich versetzen, um sicherzustellen, dass ausreichend Daten vorhanden sind, damit die Algorithmen mit der Zeit weiterhin lernen können. Beachten Sie, dass das Personalisieren einer größeren Traffic-Menge zur Folge hat, dass die Bestimmung der exakten Steigerung weniger präzise ist. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher mit einem personalisierten Erlebnis</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **Zuordnung anpassen** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

Um den Krontrollprozentsatz anzupassen, klicken Sie auf die Symbole in der Zuordnungsspalte. Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

![Traffic-Zuordnung für automatisches Targeting ändern](/help/c-activities/assets/auto-target-control.png)

Sie können [ein bestimmtes Erlebnis auswählen, das als Kontrolle verwendet werden soll](/help/c-activities/t-automated-personalization/experience-as-control.md), oder die Option „Zufälliges Erlebnis“ verwenden.

## Wann sollte [!UICONTROL Automatisches Targeting] anstelle von „Automatisierte Personalisierung“ gewählt werden? {#section_BBC4871C87944DD7A8B925811A30C633}

Es gibt verschiedene Szenarien, in denen Sie möglicherweise [!UICONTROL Automatisches Targeting] anstatt „Automatisierte Personalisierung“ verwenden möchten:

* Wenn Sie anstelle von individuellen Angeboten, die zum Formen eines Erlebnisses automatisch kombiniert werden, das gesamte Erlebnis definieren.
* Wenn Sie den vollständigen Satz der Visual Experience Composer-Funktionen (VEC) nutzen möchten, die von [!UICONTROL Automatisierte Personalisierung] nicht unterstützt werden: benutzerdefinierter Code-Editor, mehrere Erlebniszielgruppen und mehr.
* Wenn Sie strukturelle Änderungen an Ihrer Seite in unterschiedlichen Erlebnissen vornehmen möchten. Wenn Sie beispielsweise die Reihenfolge der Elemente auf Ihrer Startseite neu anordnen möchten, empfiehlt sich eher die Verwendung von [!UICONTROL Automatisches Targeting] als die Verwendung von „Automatisierte Personalisierung“.

## Was hat [!UICONTROL Automatisches Targeting] mit „Automatisierte Personalisierung“ gemeinsam? {#section_2A601F482F9A44E38D4B694668711319}

**Der Algorithmus optimiert für ein erfolgreiches Resultat jedes Besuchs.**

* Der Algorithmus prognostiziert die Neigung eines Besuchers zur Konversion (oder den voraussichtlichen Erlös aus einer Konversion), um das beste Erlebnis bereitzustellen.
* Ein Besucher ist am Ende einer bestehenden Sitzung für ein neues Erlebnis berechtigt (sofern sich der Besucher nicht in der Kontrollgruppe befindet; in diesem Fall wird diesem Besucher bei nachfolgenden Besuchen weiterhin dasselbe Erlebnis bereitgestellt, das ihm beim ersten Besuch zugewiesen wurde).
* Innerhalb einer Sitzung ändert sich die Prognose nicht, damit die Beständigkeit der angezeigten Darstellung nicht beeinträchtigt wird.

**Der Algorithmus passt sich an Änderungen im Besucherverhalten an.**

* Multi-Armed Bandit gewährleistet, dass das Modell immer einen kleinen Anteil des Traffics darauf verwendet, während des gesamten Lebenszyklus der Aktivität weiter zu lernen, um so eine Übernutzung der zuvor erlernten Trends zu verhindern.
* Die zugrunde liegenden Modelle werden alle 24 Stunden anhand der neuesten Daten zum Besucherverhalten überholt, um sicherzustellen, dass Target bei wechselnden Besucherpräferenzen immer auf dem neuesten Stand bleibt.
* Wenn der Algorithmus keine Gewinnererlebnisse für Einzelpersonen bestimmen kann, wechselt er automatisch zur Anzeige des Erlebnisses mit der besten Gesamtleistung und sucht weiterhin nach personalisierten Gewinnern. Das Erlebnis mit der besten Leistung wird mithilfe des [Thompson-Samplings](https://en.wikipedia.org/wiki/Thompson_sampling) gefunden.

**Der Algorithmus optimiert kontinuierlich für eine einzige Zielmetrik.**

* Diese Metrik kann auf Konversionen oder Umsätzen (genauer gesagt: Umsatz pro Besuch) basieren.

**Die Verwendung von [!DNL Analytics] als Datenquelle oder Berichterstellungs-Endpunkt wird vom Algorithmus nicht unterstützt.**

**Target sammelt automatisch Informationen über Besucher, um Personalisierungsmodelle zu erstellen.**

* Weitere Informationen zu den bei [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendeten Parametern finden Sie unter [Datenerfassung bei „Automatisierte Personalisierung“](../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058).

**Target verwendet automatisch alle von Experience Cloud gemeinsam genutzten Zielgruppen, um diese Personalisierungsmodelle zu erstellen.**

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Informationen zum Verwenden von Experience Cloud-Zielgruppen mit Target finden Sie unter  [Experience Cloud Audiences](../c-integrating-target-with-mac/mmp.md#concept_F4863DE4C92D4805AB690B4B3D487969)

**Marketer können für die Erstellung von Personalisierungsmodellen Offline-Daten, Propensity Scores oder andere benutzerdefinierte Daten hochladen.**

* Weitere Informationen zum [Hochladen von Daten für „Automatisches Targeting“ und „Automatisierte Personalisierung“](../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

## Worin unterscheidet sich [!UICONTROL Automatisches Targeting] von „Automatisierte Personalisierung“? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**[!UICONTROL Für die Erstellung eines personalisierten Modells ist beim automatischen Targeting] häufig weniger Traffic erforderlich als bei der automatisierten Personalisierung.**

Auch wenn die zum Erstellen der Modelle [!UICONTROL Automatisches Targeting] und [!UICONTROL Automatisierte Personalisierung] erforderliche Traffic-Menge *pro Erlebnis* identisch ist, liegen in der Regel in einer Aktivität vom Typ „Automatisierte Personalisierung“ mehr Aktivitäten vor als in einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]. Wenn Sie beispielsweise über eine Aktivität vom Typ [!UICONTROL Automatisierte Personalisierung] verfügen, in der Sie zwei Angebote pro Position mit zwei Positionen erstellen, verfügen Sie insgesamt über vier (2 = 4) in der Aktivität enthaltene Erlebnisse (ohne Ausschlüsse). Mit [!UICONTROL Automatisches Targeting] können Sie festlegen, dass Erlebnis 1 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht und dass Erlebnis 2 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht. Da Ihnen [!UICONTROL Automatisches Targeting] ermöglicht auszuwählen, dass Sie über mehrere Änderungen in einem Erlebnis verfügen möchten, können Sie die Anzahl der Gesamterlebnisse in Ihrer Aktivität reduzieren.

Für [!UICONTROL Automatisches Targeting] können einfache Faustregeln zum Nachvollziehen der Traffic-Anforderungen verwendet werden:

* **Wenn „Konversion“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 7.000 Besuche und 350 Konversionen verfügen.
* **Wenn „Umsatz pro Besuch“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 1.000 Konversionen pro Erlebnis verfügen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

**[!UICONTROL Für das automatische Targeting] ist ein kompletter Satz von Setup-Funktionen vorhanden.**

* Da [!UICONTROL Automatisches Targeting] im Arbeitsablauf einer A/B-Aktivität eingebettet wird, profitiert [!UICONTROL Automatisches Targeting] vom ausgereiften und bewährten Visual Experience Composer (VEC). [QS-Links](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) können ebenfalls mit [!UICONTROL Automatisches Targeting] genutzt werden.

**[!UICONTROL Für automatisches Targeting] gibt es ein umfangreiches Framework für Online-Tests.**

* Der „mehrarmige Bandit“ ist Bestandteil eines größeren Online-Test-Frameworks, das es unseren Datenwissenschaftlern und Forschern erlaubt, die Resultate ihrer kontinuierlichen Verbesserungen unter Praxisbedingungen zu untersuchen.
* Künftig ermöglicht uns diese Testumgebung, unseren datenaffinen Kunden unsere maschinelle Lernplattform bereitzustellen, damit diese ihre eigenen Modelle einbringen und so die in Target vorhandenen Modelle noch ergänzen können.

## Berichterstellung und [!UICONTROL Automatisches Targeting] {#section_42EE7F5E65E84F89A872FE9921917F76}

Weitere Informationen finden Sie unter [Zusammenfassender Bericht zu „Automatisches Targeting“](../c-reports/auto-target-summary-report.md#concept_E2171F7B57C1417DAAD7E7909A3FB073) im Abschnitt [Berichte](../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6).

## Häufig gestellte Fragen zum automatischen Targeting {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Lesen Sie die folgenden häufig gestellten Fragen und Antworten, während Sie mit Aktivitäten der [!UICONTROL automatischen Zielgruppe] arbeiten:

### Wie lauten die Best Practices zum Einrichten einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]?

* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik vom Typ „Umsatz pro Besuch“ (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen der Kontrolle und den personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Ermitteln Sie, ob Sie über ausreichend Traffic für die Seite verfügen, auf der Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] in einer angemessenen Dauer für zu erstellende Personalisierungsmodelle ausgeführt wird.
   * Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie weder Erlebnisse ändern noch Profilattribute hinzufügen/entfernen, während die Aktivität aktiv ist.

* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Positionen ab, die Sie für Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] verwenden möchten, um sicherzustellen, dass sich die Position(en) und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, kommt es wahrscheinlich auch nicht zu einer Steigerung durch [!UICONTROL Automatisches Targeting].

   * Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während des Aktivitätsverlaufs wesentliche Änderungen an den Erlebnissen vorzunehmen.

### Werden die Häkchen, die angeben, ob ein Modell für das jeweilige Erlebnis erstellt ist, aktualisiert, wenn sich der Berichtsdatumsbereich ändert?

Nein, Häkchen für die Modellgenerierung zeigen nur die bisher erstellten Modelle an. Es gibt keine Möglichkeit zurückzukehren und zu sehen, ob ein Modell abgeschlossen wurde.

### Wenn ein Besucher die Aktivität vom Typ [!UICONTROL Automatisches Targeting] NICHT sieht und konvertiert, zählt dann die Konversion dann in meiner Aktivität?

Nein, es werden nur die Besucher im Bericht gezählt, die sich für die Aktivität vom Typ [!UICONTROL Automatisches Targeting] qualifizieren und sie anzeigen.

### Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] generiert offenbar keine Steigerung. Was ist los?  

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automatisierte Personalisierung] eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

### Wann sollte ich meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anhalten?

[!UICONTROL „Automatisches Targeting“] kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzuhalten.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

### Wie lange sollte ich warten, bis Modelle erstellt werden?  {#how-long}

The length of time it takes for models to build in your [!UICONTROL Auto-Target] activity typically depends on the traffic to your selected activity location(s) and conversion rates associated with you activity success metric.

[!UICONTROL Die automatische Zielgruppe] versucht nicht, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, bis mindestens 50 Konvertierungen für dieses Erlebnis vorhanden sind. Wenn das erstellte Modell von unzureichender Qualität ist (was durch die Offline-Auswertung der &quot;Test&quot;-Daten unter Verwendung [einer Metrik, AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)genannt, bestimmt wird), wird das Modell nicht dazu verwendet, Traffic auf eine personalisierte Weise zu liefern.

Einige weitere Punkte, die im Zusammenhang mit der Modellerstellung der [!UICONTROL Auto-Zielgruppe]zu beachten sind:

* Sobald eine Aktivität live ist, berücksichtigt die [!UICONTROL automatische Zielgruppe] bis zu den letzten 45 Tagen zufällig bereiteter Daten, wenn versucht wird, Modelle zu erstellen (d. h. den Traffic zu steuern, sowie einige extra zufällig bereitgestellte Daten, die von unserem Algorithmus bereitgestellt werden).
* Wenn [!UICONTROL Umsatz pro Besuch] Ihre Erfolgsmetrik ist, benötigen diese Aktivitäten in der Regel mehr Daten, um Modelle zu erstellen, da die Datenabweichung, die normalerweise im Besuchsumsatz im Vergleich zu Konversionsrat besteht, höher ist.
* Da Modelle auf der Grundlage der einzelnen Erlebnisse erstellt werden, müssen beim Ersetzen eines Erlebnisses durch ein anderes ausreichend Traffic (d. h. mindestens 50 Konversionen) für das neue Erlebnis gesammelt werden, bevor personalisierte Modelle neu erstellt werden können.

### Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?  

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

### Ab wann kann ich die Ergebnisse meiner Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen?

Sie können die Ergebnisse Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen, sobald Sie über mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, die Modelle erstellt haben.

### Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

Sie können bei der Erstellung einer [automatisierten Personalisierung](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) oder eines [automatischen Targetings](/help/c-activities/auto-target-to-optimize.md) (AT) ein Kontrollerlebnis auswählen.

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie in den Leistungsberichten den personalisierten Traffic mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/c-activities/t-automated-personalization/experience-as-control.md).

### Kann ich die Zielmetrik in der Mitte durch eine Auto-Zielgruppe-Aktivität ändern? {#change-metric}

Es wird nicht empfohlen, die Zielmetrik mitten in einer Aktivität zu ändern. Obwohl die Zielmetrik während einer Aktivität mithilfe der [!DNL Target] Benutzeroberfläche geändert werden kann, sollten Sie immer eine neue Aktivität Beginn haben. Wir garantieren nicht, was passiert, wenn Sie die Sollmetrik in einer Aktivität nach der Ausführung ändern.

Diese Empfehlung gilt für [!UICONTROL Aktivitäten mit automatisierter Zuordnung], [!UICONTROL automatischer Zielgruppe]und [!UICONTROL Automated Personalization] , die entweder [!DNL Target] oder [!DNL Analytics] (A4T) als Berichte verwenden.

### Kann ich die Option &quot;Berichtsdaten zurücksetzen&quot;beim Ausführen einer Aktivität für die automatische Zielgruppe verwenden?

Die Verwendung der Option [!UICONTROL Berichtsdaten] zurücksetzen für Aktivitäten mit [!UICONTROL automatischer Zielgruppe] wird nicht empfohlen. Obwohl die Daten des sichtbaren Berichte entfernt werden, entfernt diese Option nicht alle Schulungsdatensätze aus dem [!UICONTROL Modell der automatischen Zielgruppe] . Anstatt die Option Berichtsdaten [!UICONTROL zurücksetzen] für Aktivitäten mit [!UICONTROL automatischer Zielgruppe] zu verwenden, erstellen Sie eine neue Aktivität und deaktivieren Sie die ursprüngliche Aktivität. (Hinweis: Diese Anleitung gilt auch für [!UICONTROL Aktivitäten mit automatisierter Zuordnung] und [!UICONTROL Automated Personalization] .)

## Fehlerbehebung für [!UICONTROL Automatisches Targeting] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, die sich möglicherweise aus der Verwendung von [!UICONTROL Automatisches Targeting] ergeben, sowie die jeweils vorgeschlagenen Lösungen.

**Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] braucht zu lange, um Modelle zu erstellen.**

Es gibt verschiedene Aktivitätseinrichtungsänderungen, welche die zum Erstellen von Modellen erwartete Dauer verringern können. Dazu zählen die Anzahl der Erlebnisse in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting], der Traffic auf Ihrer Site sowie Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung dahingehend, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, in der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn die Anzahl der Erlebnisse in einer Aktivität verringert wird, wird das Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitätspositionen vorhanden sind, desto schneller werden die Modelle erstellt.

**Meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] generiert keine Steigerung.**

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ „Automatisierte Personalisierung“ eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn die Modelle nicht für alle Erlebnisse erstellt sind, verarbeitet Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] weiterhin zufallsbasiert einen signifikanten Teil an Besuchen, um zu versuchen, alle Modelle schnellstmöglich zu erstellen. Ohne erstellte Modelle wird der Traffic mit [!UICONTROL Automatisches Targeting] nicht personalisiert.

Stellen Sie als Nächstes mithilfe eines nicht personalisierten A/B-Tests sicher, dass die Angebote und Aktivitätspositionen wirklich einen Unterschied für die Gesamtantwortraten ausmachen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

**Die von einer Konversionsmetrik abhängigen Metriken werden nicht konvertiert.**

Dieses Ergebnis ist zu erwarten.

Bei einer Aktivität vom Typ [!UICONTROL Automatisches Targeting] wird der Benutzer von dem Erlebnis abgekoppelt und die Aktivität neu gestartet, sobald eine Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder nachgelegenes Ziel handelt) konvertiert wurde.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist abhängig von C1. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 konvertiert und erst danach A1, wird A1 auch dann nicht konvertiert, da der Besucher abgekoppelt wird, sobald C1 konvertiert ist.

## Schulungsvideo: Erklärungen zu Aktivitäten vom Typ „Automatisches Targeting“ ![Übersichtskennzeichnung](/help/assets/overview.png)

In diesem Video wird die Einrichtung einer A/B-Aktivität für [!UICONTROL Automatisches Targeting] beschrieben.

Nach Abschluss dieser Schulung sollten Sie zu Folgendem in der Lage sein:

* Definieren von Tests zu [!UICONTROL Automatisches Targeting]
* Vergleichen und Kontrahieren von [!UICONTROL Automatisches Targeting] mit „Automatisierte Personalisierung“
* Erstellen von Aktivitäten für [!UICONTROL Automatisches Targeting]

>[!VIDEO](https://video.tv.adobe.com/v/18558)