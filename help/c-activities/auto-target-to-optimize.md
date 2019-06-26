---
description: Beim automatischen Targeting werden mehrere marketerdefinierte Erlebnisse mit hoher Leistung über das erweiterte maschinelle Lernen ausgewählt. Zudem erhalten alle Besucher basierend auf ihrem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen ein optimal auf sie zugeschnittenes Erlebnis, um die Inhalte zu personalisieren und Konversionen zu fördern.
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung
seo-description: Beim automatischen Targeting werden mehrere marketerdefinierte Erlebnisse mit hoher Leistung über das erweiterte maschinelle Lernen ausgewählt. Zudem erhalten alle Besucher basierend auf ihrem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen ein optimal auf sie zugeschnittenes Erlebnis, um die Inhalte zu personalisieren und Konversionen zu fördern.
seo-title: Automatisches Targeting
solution: Target
title: Automatisches Targeting
title-outputclass: premium
topic: Standard
uuid: fce769d2-9e7f-4064-add7-76e1fc394b4f
badge: premium
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# ![PREMIUM](/help/assets/premium.png) Automatisches Targeting{#auto-target}

[!UICONTROL Automatisches Targeting] verwendet fortschrittliches maschinelles Lernen, um aus mehreren leistungsstarken Erlebnissen mit Marketingexperten auswählen zu können, um Inhalte zu personalisieren und Konversionen zu fördern. Automatisches Targeting stellt das benutzerspezifische Erlebnis für jeden Besucher basierend auf seinem individuellen Kundenprofil und dem Verhalten voriger Besucher mit ähnlichen Profilen bereit.

>[!NOTE]
>
>[!UICONTROL Automatisches Targeting] ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. For more information about the advanced features this license provides, see [Target Premium](/help/c-intro/intro.md).

Beim [Erstellen einer A/B-Aktivität mit einem geleiteten Arbeitsablauf in drei Schritten](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) können Sie Traffic mithilfe der Option [!UICONTROL Automatisches Targeting für personalisierte Erlebnisse] zuordnen:

![Automatisches Targeting für die Option personalisierte Erlebnisse](/help/c-activities/assets/auto-target-ui-new.png)

## Überblick {#section_972257739A2648AFA7E7556B693079C9}

Mit der Option [!UICONTROL Automatisches Targeting] im A/B-Aktivitätsfluss können Sie maschinelles Lernen nutzen, damit basierend auf einer Reihe von Erlebnissen, die von Marketingexperten definiert wurden, personalisiert wird. [!UICONTROL Automatisches Targeting] soll im Vergleich zum herkömmlichen A/B-Test oder „Automatisch zuweisen“ eine maximale Optimierung bereitstellen, indem bestimmt wird, welches Erlebnis welchem Besucher angezeigt wird. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden, bestimmt [!UICONTROL Automatisches Targeting] automatisch das beste Erlebnis für einen bestimmten Besucher (basierend auf seinem Profil und anderen Kontextinformationen), um ein maximal personalisiertes Erlebnis bereitzustellen.

Ähnlich wie bei der automatisierten Personalisierung verwendet [!UICONTROL Automatisches Targeting] einen Random Forest-Algorithmus, eine führende Methode in der Datenwissenschaft, um das beste Erlebnis für einen Besucher zu ermitteln. Da sich [!UICONTROL Automatisches Targeting] an Änderungen im Besucherverhalten anpassen kann, kann es dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Dies wird manchmal auch als „Always-on“-Modus bezeichnet.

Im Gegensatz zu einer A/B-Aktivität, bei der die Erlebniszuordnung an einen bestimmten Besucher gebunden ist, optimiert [!UICONTROL Automatisches Targeting] das angegebene Geschäftsziel im Verlauf der einzelnen Besuche. Wie in [!UICONTROL Automatisierte Personalisierung] reserviert[!UICONTROL  Automatisches Targeting] standardmäßig einen Teil des Traffics der Aktivität als Kontrollgruppe zum Messen der Steigerung. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

Beim Verwenden von [!UICONTROL Automatisches Targeting] müssen einige Hinweise beachtet werden:

* Es ist nicht möglich, eine bestimmte Aktivität von [!UICONTROL Automatisches Targeting] in „Automatisierte Personalisierung“ umzuschalten und umgekehrt.
* Es ist nicht möglich, von der manuellen Traffic-Zuordnung (herkömmlicher A/B-Test) zu [!UICONTROL Automatisches Targeting] und umgekehrt zu wechseln, sobald eine Aktivität aktiv ist.
* Wenn Hosts und Umgebungen (Hostgruppen) verwendet werden, werden die Modelle nur für die Produktionsumgebung erstellt. Alle Umgebungen tragen Daten für das Erstellen von Modellen für Produktionskampagnen bei.
* Es müssen mindestens zwei Erlebnisse verwendet werden.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

Bei Erörterungen zu [!UICONTROL Automatisches Targeting] sind die folgenden Begriffe hilfreich:

| Begriff | Definition |
|---|---|
| Multi-Armed Bandit | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| Random Forest | Random Forest ist ein führender Ansatz beim maschinellen Lernen. Im Datenwissenschaftlerjargon ist dies eine Ensemble-Classification- oder Regressionsmethode, die auf der Grundlage von Besuchern und Besuchsattributen eine große Anzahl von Entscheidungsbäumen erstellt. Random Forest wird von Target eingesetzt, um zu bestimmen, welches Erlebnis die höchste Wahrscheinlichkeit einer Konversion (oder den höchsten Umsatz pro Besuch) für jeden einzelnen Besucher hat. Weitere Informationen zu Random Forest in Target finden Sie unter [Random Forest-Algorithmus](../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA). |
| Thompson Sampling | Ziel des Thompson Samplings ist es, festzustellen, welches (nicht personalisierte) Erlebnis insgesamt das beste ist, während gleichzeitig die „Kosten“ für die Auffindung dieses Erlebnisses minimiert werden. Das Thompson Sampling wählt immer einen Gewinner aus, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. Weitere Informationen finden Sie unter [Thompson Sampling](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Funktionsweise von [!UICONTROL Automatisches Targeting] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Unter den folgenden Links erhalten Sie weitere Informationen über Daten und Algorithmen, die den Funktionen [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ zugrunde liegen:

| Begriff | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist der wichtigste Personalisierungsalgorithmus von Target; er wird in [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendet. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere Prognoseleistung zu erzielen, als dies bei der isolierten Verwendung dieser Lernalgorithmen möglich wäre. Der Random Forest-Algorithmus des automatisierten Personalisierungssystems ist eine Classification- oder Regressionsmethode, deren Funktionsweise die Konstruktion einer Vielzahl von Entscheidungsbäumen während der Anlernzeit zugrunde liegt. |
| [Hochladen von Daten für die Personalisierungsalgorithmen von Target](/help/c-activities/t-automated-personalization/algo-random-forest.md) | Es gibt mehrere Möglichkeiten, um Daten für die Modelle [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ einzugeben. |
| [Datenerfassung für die Target-Personalisierungsalgorithmen](/help/c-activities/t-automated-personalization/ap-data.md) | Die Personalisierungsalgorithmen von Target erfassen automatisch eine Vielzahl von Daten. |

## Bestimmen der Traffic-Zuordnung {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach dem Ziel Ihrer Aktivität können Sie eine unterschiedliche Traffic-Zuordnung zwischen den Kontroll- und personalisierten Erlebnissen auswählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdownliste [!UICONTROL Zuordnung anpassen] können Sie aus den folgenden Optionen auswählen:

* Personalisierungsalgorithmus auswerten
* Personalisierungs-Datenverkehr maximieren
* Zuordnung anpassen

![Dropdown-Liste &quot;Zuordnung «](/help/c-activities/assets/split-new.png)

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **Personalisierung evaluieren (50/50)**: Wenn Ihr Ziel darin besteht, den Algorithmus zu testen, verwenden Sie 50/50 Prozent der Besucher zwischen dem Kontrollelement und dem zielgerichteten Algorithmus. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Für die Verwendung mit &quot;Random Experiences&quot; als Steuerelement vorgeschlagen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ gesehen erhalten weniger Besucher ein personalisiertes Erlebnis</li></ul> |
| **Traffic-Optimierung maximieren (10. Januar)**: Wenn Ihr Ziel die Erstellung einer &quot;Immer ein&quot; -Aktivität ist, stellen Sie 10% der Besucher in das Steuerelement ein, um sicherzustellen, dass genügend Daten für die Algorithmen im Laufe der Zeit erhalten bleiben. Beachten Sie, dass das Personalisieren einer größeren Traffic-Menge zur Folge hat, dass die Bestimmung der exakten Steigerung weniger präzise ist. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Steuerung verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher mit einem personalisierten Erlebnis</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **Zuordnung anpassen** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

Um den Steuerungsprozentsatz anzupassen, klicken Sie auf die Symbole in der Spalte &quot;Zuordnung&quot; . Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

![Traffic-Zuordnung für automatisches Targeting ändern](/help/c-activities/assets/auto-target-control.png)

You can [select a specific experience to use as control](/help/c-activities/t-automated-personalization/experience-as-control.md) or you can use the Random experience option.

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

**Die Verwendung von[!DNL Analytics]als Datenquelle oder Berichterstellungs-Endpunkt wird vom Algorithmus nicht unterstützt.**

**Target sammelt automatisch Informationen über Besucher, um Personalisierungsmodelle zu erstellen.**

* Weitere Informationen zu den bei [!UICONTROL Automatisches Targeting] und „Automatisierte Personalisierung“ verwendeten Parametern finden Sie unter [Datenerfassung bei „Automatisierte Personalisierung“](../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058).

**Target verwendet automatisch alle von Experience Cloud gemeinsam genutzten Zielgruppen, um diese Personalisierungsmodelle zu erstellen.**

* Um Zielgruppen zu dem Modell hinzuzufügen, sind Ihrerseits keine besonderen Aktivitäten erforderlich. Informationen zum Verwenden von Experience Cloud-Zielgruppen mit Target finden Sie unter [Experience Cloud Audiences](../c-integrating-target-with-mac/mmp.md#concept_F4863DE4C92D4805AB690B4B3D487969)

**Marketer können für die Erstellung von Personalisierungsmodellen Offline-Daten, Propensity Scores oder andere benutzerdefinierte Daten hochladen.**

* Weitere Informationen zum [Hochladen von Daten für „Automatisches Targeting“ und „Automatisierte Personalisierung“](../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

## Worin unterscheidet sich [!UICONTROL Automatisches Targeting] von „Automatisierte Personalisierung“? {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

**Für die Erstellung eines personalisierten Modells ist beim[!UICONTROL automatischen Targeting]häufig weniger Traffic erforderlich als bei der automatisierten Personalisierung.**

Auch wenn die zum Erstellen der Modelle [!UICONTROL Automatisches Targeting] und [!UICONTROL Automatisierte Personalisierung] erforderliche Traffic-Menge *pro Erlebnis* identisch ist, liegen in der Regel in einer Aktivität vom Typ „Automatisierte Personalisierung“ mehr Aktivitäten vor als in einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]. Wenn Sie beispielsweise über eine Aktivität vom Typ [!UICONTROL Automatisierte Personalisierung] verfügen, in der Sie zwei Angebote pro Position mit zwei Positionen erstellen, verfügen Sie insgesamt über vier (2 = 4) in der Aktivität enthaltene Erlebnisse (ohne Ausschlüsse). Mit [!UICONTROL Automatisches Targeting] können Sie festlegen, dass Erlebnis 1 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht und dass Erlebnis 2 Angebot 1 an Position 1 und Angebot 2 an Position 2 einbezieht. Da Ihnen [!UICONTROL Automatisches Targeting] ermöglicht auszuwählen, dass Sie über mehrere Änderungen in einem Erlebnis verfügen möchten, können Sie die Anzahl der Gesamterlebnisse in Ihrer Aktivität reduzieren.

Für [!UICONTROL Automatisches Targeting] können einfache Faustregeln zum Nachvollziehen der Traffic-Anforderungen verwendet werden:

* **Wenn „Konversion“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 7.000 Besuche und 350 Konversionen verfügen.
* **Wenn „Umsatz pro Besuch“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 1.000 Konversionen pro Erlebnis verfügen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

**Für das[!UICONTROL automatische Targeting]ist ein kompletter Satz von Setup-Funktionen vorhanden.**

* Da [!UICONTROL Automatisches Targeting] im Arbeitsablauf einer A/B-Aktivität eingebettet wird, profitiert [!UICONTROL Automatisches Targeting] vom ausgereiften und bewährten Visual Experience Composer (VEC). [QS-Links](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) können ebenfalls mit [!UICONTROL Automatisches Targeting] genutzt werden.

**Für[!UICONTROL automatisches Targeting]gibt es ein umfangreiches Framework für Online-Tests.**

* Der „mehrarmige Bandit“ ist Bestandteil eines größeren Online-Test-Frameworks, das es unseren Datenwissenschaftlern und Forschern erlaubt, die Resultate ihrer kontinuierlichen Verbesserungen unter Praxisbedingungen zu untersuchen.
* Künftig ermöglicht uns diese Testumgebung, unseren datenaffinen Kunden unsere maschinelle Lernplattform bereitzustellen, damit diese ihre eigenen Modelle einbringen und so die in Target vorhandenen Modelle noch ergänzen können.

## Berichterstellung und [!UICONTROL Automatisches Targeting] {#section_42EE7F5E65E84F89A872FE9921917F76}

Weitere Informationen finden Sie unter [Zusammenfassender Bericht zu „Automatisches Targeting“](../c-reports/auto-target-summary-report.md#concept_E2171F7B57C1417DAAD7E7909A3FB073) im Abschnitt [Berichte](../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6).

## Häufig gestellte Fragen zum automatischen Targeting {#section_5C120A2B11D14D9BAF767BBAB50FED23}

**Wie lauten die Best Practices zum Einrichten einer Aktivität vom Typ[!UICONTROL Automatisches Targeting]?**

* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik vom Typ „Umsatz pro Besuch“ (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität gegenüber einer Konversion funktioniert.
* Legen Sie die Zuordnung zwischen der Kontrolle und den personalisierten Erlebnissen fest, bevor Sie die Aktivität auf Basis Ihrer Ziele beginnen.
* Ermitteln Sie, ob Sie über ausreichend Traffic für die Seite verfügen, auf der Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] in einer angemessenen Dauer für zu erstellende Personalisierungsmodelle ausgeführt wird.
   * Wenn Sie den Personalisierungsalgorithmus testen, sollten Sie weder Erlebnisse ändern noch Profilattribute hinzufügen/entfernen, während die Aktivität aktiv ist.

* Schließen Sie ggf. eine A/B-Aktivität zwischen den Angeboten und Positionen ab, die Sie für Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] verwenden möchten, um sicherzustellen, dass sich die Position(en) und Angebote auf das Optimierungsziel auswirken. Wenn eine A/B-Aktivität keinen signifikanten Unterschied aufzeigen kann, kommt es wahrscheinlich auch nicht zu einer Steigerung durch [!UICONTROL Automatisches Targeting].

   * Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen Erlebnissen aufzeigt, da sich die von Ihnen in Erwägung gezogenen Angebote möglicherweise nicht ausreichend voneinander unterscheiden, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder das Optimierungsziel liegt zu weit vom Konversionstrichter entfernt, um von Ihren ausgewählten Angeboten betroffen zu sein.

* Versuchen Sie, während des Aktivitätsverlaufs wesentliche Änderungen an den Erlebnissen vorzunehmen.

**Werden die Häkchen, die angeben, ob ein Modell für das jeweilige Erlebnis erstellt ist, aktualisiert, wenn sich der Berichtsdatumsbereich ändert?**

Nein, Häkchen für die Modellgenerierung zeigen nur die bisher erstellten Modelle an. Es gibt keine Möglichkeit zurückzukehren und zu sehen, ob ein Modell abgeschlossen wurde.

**Wenn ein Besucher die Aktivität vom Typ[!UICONTROL Automatisches Targeting]NICHT sieht und konvertiert, zählt dann die Konversion dann in meiner Aktivität?**

Nein, es werden nur die Besucher im Bericht gezählt, die sich für die Aktivität vom Typ [!UICONTROL Automatisches Targeting] qualifizieren und sie anzeigen.

**Meine Aktivität vom Typ[!UICONTROL Automatisches Targeting]generiert offenbar keine Steigerung. Was ist los?**

Es sind vier Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automatisierte Personalisierung] eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen.

Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

**Wann sollte ich meine Aktivität vom Typ[!UICONTROL Automatisches Targeting]anhalten?**

[!UICONTROL „Automatisches Targeting“] kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzuhalten.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

**Wie lange sollte ich warten, bis Modelle erstellt werden?**

Wie lange es dauert, bis in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] Modelle erstellt werden, hängt in der Regel vom Traffic Ihrer ausgewählten Aktivitätsposition(en) und Ihrer Aktivitätserfolgsmetrik ab.

Für [!UICONTROL Automatisches Targeting] können einfache Faustregeln zum Nachvollziehen der Traffic-Anforderungen verwendet werden:

* **Wenn „Konversion“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 7.000 Besuche und 350 Konversionen verfügen.
* **Wenn „Umsatz pro Besuch“ Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag pro Erlebnis. Zusätzlich muss die Aktivität über mindestens 1.000 Konversionen pro Erlebnis verfügen. Für „Umsatz pro Besuch (RPV)“ sind aufgrund der höheren Datenvarianz, die im Vergleich zur Konversionsrate für gewöhnlich im Besuchsumsatz vorhanden ist, in der Regel mehr Daten zum Erstellen von Modellen erforderlich.

**Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?**

Nein, es müssen mindestens zwei Modelle in Ihrer Aktivität erstellt werden, damit die Personalisierung gestartet wird.

**Ab wann kann ich die Ergebnisse meiner Aktivität vom Typ[!UICONTROL Automatisches Targeting]anzeigen?**

Sie können die Ergebnisse Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen, sobald Sie über mindestens zwei Erlebnisse mit für das Erlebnis erstellten Modellen (grünes Häkchen) verfügen, die Modelle erstellt haben.

**Kann ich ein spezifisches Erlebnis angeben, das als Steuerelement verwendet werden soll?**

You can select an experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern.

For more information, see [Use a specific experience as control](/help/c-activities/t-automated-personalization/experience-as-control.md).

## Fehlerbehebung für [!UICONTROL Automatisches Targeting] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, die sich möglicherweise aus der Verwendung von [!UICONTROL Automatisches Targeting] ergeben, sowie die jeweils vorgeschlagenen Lösungen.

**Meine Aktivität vom Typ[!UICONTROL Automatisches Targeting]braucht zu lange, um Modelle zu erstellen.**

Es gibt verschiedene Aktivitätseinrichtungsänderungen, welche die zum Erstellen von Modellen erwartete Dauer verringern können. Dazu zählen die Anzahl der Erlebnisse in Ihrer Aktivität vom Typ [!UICONTROL Automatisches Targeting], der Traffic auf Ihrer Site sowie Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung dahingehend, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, in der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn die Anzahl der Erlebnisse in einer Aktivität verringert wird, wird das Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitätspositionen vorhanden sind, desto schneller werden die Modelle erstellt.

**Meine Aktivität vom Typ[!UICONTROL Automatisches Targeting]generiert keine Steigerung.**

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

## Schulungsvideo: Erklärungen zu Aktivitäten vom Typ „Automatisches Targeting“

In diesem Video wird die Einrichtung einer A/B-Aktivität für [!UICONTROL Automatisches Targeting] beschrieben.

Nach Abschluss dieser Schulung sollten Sie zu Folgendem in der Lage sein:

* Definieren von Tests zu [!UICONTROL Automatisches Targeting]
* Vergleichen und Kontrahieren von [!UICONTROL Automatisches Targeting] mit „Automatisierte Personalisierung“
* Erstellen von Aktivitäten für [!UICONTROL Automatisches Targeting]

>[!VIDEO](https://video.tv.adobe.com/v/18558?captions=ger)