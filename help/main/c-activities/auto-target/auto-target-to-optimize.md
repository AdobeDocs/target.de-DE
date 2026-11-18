---
keywords: Automatisches Targeting;Targeting;Traffic-Zuordnung;häufig gestellte Fragen;FAQ;Fehlerbehebung;Fehlerbehebung
description: Erfahren Sie, wie [!UICONTROL &#x200B; Aktivität vom Typ „Automatisches Targeting] jedem Besucher auf der Grundlage von Kundenprofilen und dem Verhalten ähnlicher Besucher das passendste Erlebnis bereitstellt.
title: Was ist eine [!UICONTROL automatisches Targeting]-Aktivität?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 59ca30dc-45a0-4129-b832-84e1132d3b69
TQID: 'https://experienceleague.adobe.com/uKmfIlOcT-tZgOjuvERXuif-Y5-2Jw3prtPbuBjv1is'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: de439134b0ee5aa795ae255bba852b9b6f10da12
workflow-type: tm+mt
source-wordcount: '2072'
ht-degree: 12%
---
# Erste Schritte mit [!UICONTROL automatischem Targeting] {#auto-target-overview}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie eine Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** jedem Besucher das passendste Erlebnis bereitstellt, wie sie funktioniert, wie die Traffic-Zuordnung ausgewählt wird und wie sie im Vergleich mit **[!UICONTROL Automated Personalization]** aussieht.

>[!ENDSHADEBOX]

**[!UICONTROL Automatisches Targeting]**-Aktivitäten in [!DNL Adobe Target] verwenden fortschrittliche Machine Learning-Algorithmen zur Auswahl eines maßgeschneiderten Erlebnisses aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen zur Personalisierung von Inhalten und Steigerung von Konversionen. **[!UICONTROL Automatisches Targeting]** stellt jedem Besucher basierend auf dem individuellen Kundenprofil und dem Verhalten vorheriger Besucher mit ähnlichen Profilen das passendste Erlebnis bereit.

>[!NOTE]
>
>* **[!UICONTROL Automatisches Targeting]** ist als Teil der [!DNL Target Premium]-Lösung verfügbar. Diese Funktion ist in [!DNL Target Standard] nicht ohne eine [!DNL Target Premium]-Lizenz verfügbar. Weitere Informationen zu den erweiterten Funktionen dieser Lizenz finden Sie unter [Target Premium](/help/main/c-intro/intro.md).
>
>* **[!UICONTROL Analytics for Target]** (A4T) unterstützt **[!UICONTROL Automatisches Targeting]**-Aktivitäten. Weitere Informationen finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

Wählen Sie [Erstellen einer A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)Aktivität mit dem angeleiteten dreistufigen Workflow die Option **[!UICONTROL Automatisches Targeting für personalisierte Erlebnisse]** auf der Seite **[!UICONTROL Targeting]** (Schritt 2). Die Schritte finden Sie unter [Erstellen einer automatischen Targeting-Aktivität](/help/main/c-activities/auto-target/create-auto-target.md).

![Einstellungen der Traffic-Zuordnungsmethode](/help/main/c-activities/automated-traffic-allocation/assets/auto-target.png)

Mit dieser Option innerhalb des A/B-Aktivitätsflusses können Sie maschinelles Lernen verwenden, um Inhalte basierend auf einer Reihe von Erlebnissen, die von Marketing-Experten definiert werden, mit einem Klick zu personalisieren. **[!UICONTROL Automatisches Targeting]** ermöglicht im Vergleich zu herkömmlichen A/B-Tests oder **[!UICONTROL automatischen Zuordnung]** maximale Optimierung, indem bestimmt wird, welches Erlebnis für jeden Besucher angezeigt werden soll. Im Gegensatz zu einer A/B-Aktivität, bei der das Ziel darin besteht, einen einzelnen Gewinner zu finden **[!UICONTROL bestimmt]** Automatisches Targeting) automatisch das beste Erlebnis für einen bestimmten Besucher. Das beste Erlebnis basiert auf dem Besucherprofil und anderen kontextuellen Informationen.

Ähnlich wie **[!UICONTROL Automated Personalization]** verwendet **[!UICONTROL Automatisches Targeting]** einen [Random Forest-](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), eine führende Datenwissenschafts-Ensemble-Methode, um das beste Erlebnis zu ermitteln, das einem Besucher angezeigt werden soll. **[!UICONTROL Automatisches Targeting]** kann sich an Änderungen im Besucherverhalten anpassen und daher dauerhaft ausgeführt werden, um eine Steigerung zu ermöglichen. Diese Methode wird auch als „Always-on“-Modus bezeichnet.

Im Gegensatz zu A/B-Aktivitäten, bei denen die Erlebniszuweisung für einen bestimmten Besucher starr ist, **[!UICONTROL das automatische Targeting]** das angegebene Geschäftsziel für jeden Besuch. Wie in **[!UICONTROL Automated Personalization]** reserviert **[!UICONTROL Automatisches Targeting]** einen Teil des Aktivitäts-Traffics standardmäßig als Kontrollgruppe, um die Steigerung zu messen. Für Besucher in der Kontrollgruppe wird ein zufälliges Erlebnis in der Aktivität bereitgestellt.

## Zu beachten {#considerations}

Beachten Sie bei der Verwendung von **[!UICONTROL Automatisches Targeting]** die folgenden Punkte:

* Achten Sie auf die Aktivitäts-Form. Die Leistung hängt mehr von der Anzahl der Standorte × Angebote als von der Anzahl der unbearbeiteten Erlebnisse ab. Große kartesische Kombinationen können das Laden und Bearbeiten im **[!UICONTROL Visual Experience Composer]** verlangsamen, sogar unter den dokumentierten Erfahrungsgrenzen.

  Als Best Practice empfiehlt es sich, **[!UICONTROL Automatisches Targeting]** und **[!UICONTROL Automated Personalization]**-Aktivitäten an 4-6 Standorten mit 4-6 Angeboten pro Standort durchzuführen. Größere Konfigurationen werden nicht empfohlen. Diese Aktivitäten werden direkt im Schritt **[!UICONTROL Erlebnisse]** erstellt, sodass die [!DNL Target]-Benutzeroberfläche möglicherweise Inline-Warnungen anzeigt oder das Speichern blockiert, wenn die Konfiguration unterstützte Schwellenwerte überschreitet.

* Sie können eine bestimmte Aktivität nicht vom **[!UICONTROL automatischen Targeting]** zum **[!UICONTROL Automated Personalization]** oder umgekehrt wechseln.
* Sie können nicht von **[!UICONTROL Manuelle]** Traffic-Zuordnung (traditioneller **[!UICONTROL A/B-]**) zu **[!UICONTROL Automatisches Targeting]** oder umgekehrt wechseln, nachdem eine Aktivität als Entwurf gespeichert wurde.
* Es wird ein Modell erstellt, um die Leistung der personalisierten Strategie im Vergleich zum zufällig bereitgestellten Traffic und dem Versand des gesamten Traffics an das insgesamt erfolgreichste Erlebnis zu ermitteln. Dieses Modell berücksichtigt nur Treffer und Konversionen in der Standardumgebung.

  Für jede Modellierungsgruppe (AP) oder jedes Erlebnis (AT) wird ein zweiter Modellsatz erstellt. Für jedes dieser Modelle werden Treffer und Konversionen in allen Umgebungen berücksichtigt.

  Anfragen werden unabhängig von der Umgebung mit demselben Modell bereitgestellt. Die Pluralität des Traffics sollte jedoch aus der Standardumgebung stammen, um sicherzustellen, dass das identifizierte erfolgreichste Erlebnis mit dem Verhalten in der realen Welt übereinstimmt.

* Verwenden Sie mindestens zwei Erlebnisse.

## Terminologie {#section_A309B7E0B258467789A5CACDC1D923F3}

Die folgenden Begriffe sind bei der Diskussion von **[!UICONTROL automatischem Targeting]** hilfreich:

| Begriff | Definition |
|---|---|
| [Mehrarmiger Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} | Die Methode „Multi-Armed Bandit“ stellt ein Gleichgewicht zwischen forschendem Lernen (Exploration) und der Verwertung der Lernergebnisse (Exploitation) her. |
| [Random Forest](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Random Forest ist ein führender Ansatz beim maschinellen Lernen. In datenwissenschaftlicher Hinsicht handelt es sich um eine Ensemble-Klassifizierungs- oder Regressionsmethode, bei der viele Entscheidungsbäume auf der Grundlage von Besucher- und Besuchsattributen erstellt werden. In [!DNL Target] wird mithilfe der Zufallsstruktur bestimmt, welches Erlebnis für jeden einzelnen Besucher die höchste Konversionswahrscheinlichkeit (oder den höchsten Umsatz pro Besuch) aufweist. |
| [Thompson-](https://en.wikipedia.org/wiki/Thompson_sampling){target=_blank} | Das Ziel des Thompson-Stichprobenverfahrens besteht darin, festzustellen, welches Erlebnis insgesamt am besten ist (nicht personalisiert), und gleichzeitig die „Kosten“ für das Auffinden dieses Erlebnisses zu minimieren. Beim Thompson-Stichprobenverfahren wird immer ein Gewinner ausgewählt, auch wenn es keinen statistischen Unterschied zwischen zwei Erlebnissen gibt. |

## Funktionsweise [!UICONTROL &#x200B; automatischen &#x200B;] {#section_77240E2DEB7D4CD89F52BE0A85E20136}

Auf den folgenden Seiten werden die Daten und Algorithmen beschrieben, die **[!UICONTROL automatischen Targeting]** **[!UICONTROL Automated Personalization zugrunde liegen]**:

| Thema | Details |
|--- |--- |
| [Random Forest-Algorithmus](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) | Der wichtigste Personalisierungsalgorithmus von [!DNL Target], der sowohl in **[!UICONTROL Automatisches Targeting]** als auch in **[!UICONTROL Automated Personalization]** verwendet wird, ist „Random Forest“. Ensemble-Methoden wie Random Forest verwenden mehrere Lernalgorithmen, um eine bessere prädiktive Leistung zu erzielen, als sie mit einem der einzelnen Lernalgorithmen erzielt werden könnte. Der Algorithmus der zufälligen Gesamtstruktur in **[!UICONTROL Automated Personalization]**- und **[!UICONTROL Automatisches Targeting]**-Aktivitäten ist eine Klassifizierungs- oder Regressionsmethode, die durch die Erstellung einer Vielzahl von Entscheidungsbäumen zur Trainingszeit ausgeführt wird. |
| [Daten für [!DNL Target] Personalization-Algorithmen werden hochgeladen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md) | Es gibt mehrere Möglichkeiten, Daten für die Modelle **[!UICONTROL Automatisches Targeting]** und **[!UICONTROL Automated Personalization]** einzugeben. |
| [Datenerfassung für  [!DNL Target] Personalization-Algorithmen](/help/main/c-activities/t-automated-personalization/ap-data.md) | Die Personalisierungsalgorithmen von [!DNL Target] erfassen automatisch verschiedene Daten. |

## Bestimmen der Traffic-Zuordnung {#section_AB3656F71D2D4C67A55A24B38092958F}

Je nach Ziel Ihrer Aktivität können Sie eine andere Traffic-Zuordnung zwischen Kontrolle und personalisierten Erlebnissen wählen. Es empfiehlt sich, dieses Ziel festzulegen, bevor Sie Ihre Aktivität aktivieren.

In der Dropdownliste **[!UICONTROL Zuordnung anpassen]** können Sie aus den folgenden Optionen auswählen:

* **[!UICONTROL Personalization-Algorithmus auswerten (50/50)]**
* **[!UICONTROL Maximieren des Personalization-Traffics (90/10)]**
* **[!UICONTROL Zuordnung anpassen]**

![Dropdown-Liste für das Zuordnungsziel](/help/main/c-activities/assets/split-new-ui.png)

In der folgenden Tabelle werden die drei Optionen erläutert:

| Aktivitätsziel | Vorgeschlagene Traffic-Zuordnung | Kompromisse |
|--- |--- |--- |
| **[!UICONTROL Personalisierungsalgorithmus auswerten (50/50)]**: Wenn Sie den Algorithmus testen möchten, sollten Sie eine 50/50-Prozentaufteilung der Besucher zwischen dem Kontroll- und dem Zielalgorithmus verwenden. Durch diese Aufteilung erhalten Sie die genaueste Schätzung der Steigerung. Wird zur Verwendung mit „zufälligen Erlebnissen“ als Kontrolle vorgeschlagen. | Aufteilung: 50 % Kontrolle / 50 % personalisiertes Erlebnis | <ul><li>Maximiert die Genauigkeit der Steigerung zwischen Kontrolle und personalisiert</li><li>Relativ weniger Besucher haben ein personalisiertes Erlebnis</li></ul> |
| **[!UICONTROL Maximieren des Personalization-Traffics (90/10)]**: Wenn Sie eine „Always on“-Aktivität erstellen möchten, geben Sie 10 % der Besucher die Kontrolle darüber, ob genügend Daten vorhanden sind, damit die Algorithmen im Laufe der Zeit weiterlernen können. Der Nachteil hier ist, dass Sie im Gegenzug für die Personalisierung eines größeren Teils Ihres Traffics weniger Präzision in der genauen Steigerung haben. Unabhängig von Ihrem Ziel ist dies die empfohlene Traffic-Aufteilung, wenn ein bestimmtes Erlebnis als Kontrolle verwendet wird. | Empfohlene Aufteilung: 10–30 % Kontrolle / 70–90 % personalisiertes Erlebnis | <ul><li>Maximiert die Anzahl der Besucher, die über ein personalisiertes Erlebnis verfügen</li><li>Maximiert die Steigerung</li><li>Weniger Genauigkeit in Bezug darauf, wofür die Steigerung für die Aktivität dient</li></ul> |
| **[!UICONTROL Zuordnung anpassen]** | Teilen Sie den Prozentsatz nach Bedarf manuell auf. | <ul><li>Es kann sein, dass Sie nicht die gewünschten Ergebnisse erzielen. Wenn Sie unsicher sind, sollten Sie jeweils die Vorschläge der vorangegangenen Optionen befolgen.</li></ul> |

Um den Prozentsatz **[!UICONTROL Kontrolle]** anzupassen, klicken Sie **[!UICONTROL Erlebnisse]** im Bereich **[!UICONTROL Traffic-]**&quot; und passen Sie dann die Prozentsätze wie gewünscht an. Sie dürfen die Kontrollgruppe nicht auf weniger als 10 % reduzieren.

Sie können [ein bestimmtes Erlebnis als Kontrolle auswählen](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oder die Option **[!UICONTROL Zufälliges Erlebnis]** verwenden.

## Vergleichen Sie [!UICONTROL Automatisches Targeting] und [!UICONTROL Automated Personalization] {#compare-at-ap}

**[!UICONTROL Automatisches Targeting]** und **[!UICONTROL Automated Personalization]** verwenden denselben Algorithmus und dieselben Daten, unterscheiden sich aber in der Erstellung der Erlebnisse und der Menge des von den Modellen benötigten Traffics.

### Was die beiden Aktivitätstypen gemeinsam haben {#section_2A601F482F9A44E38D4B694668711319}

* **Optimierung für jeden Besuch.** Der Algorithmus sagt die Neigung eines Besuchers zur Konversion (oder den geschätzten Umsatz aus der Konversion) voraus, um das beste Erlebnis zu erzielen. Ein Besucher hat am Ende einer vorhandenen Sitzung Anspruch auf ein neues Erlebnis. Die Ausnahme bildet ein Besucher in der Kontrollgruppe, der das Erlebnis beim ersten Besuch beibehält. Innerhalb einer Sitzung ändert sich die Prognose nicht, um die visuelle Konsistenz zu wahren.
* **Anpassung an Änderungen im Besucherverhalten.** Der mehrarmige Bandit „gibt“ immer einen kleinen Teil des Traffics aus, um während des gesamten Lebens der Aktivität weiter zu lernen und eine Übernutzung der zuvor erlernten Trends zu verhindern. Die zugrunde liegenden Modelle werden alle 24 Stunden mit den neuesten Daten zum Besucherverhalten neu erstellt. Wenn der Algorithmus keine Gewinnererlebnisse für Einzelpersonen ermitteln kann, wechselt er automatisch zur Anzeige des insgesamt besten Erlebnisses, das mithilfe des [Thompson-Stichprobenverfahrens](https://en.wikipedia.org/wiki/Thompson_sampling) gefunden wurde, während er weiterhin nach personalisierten Gewinnern sucht.
* **Eine einzelne Zielmetrik.** Der Algorithmus wird kontinuierlich für eine Metrik optimiert, die konversionsbasiert oder umsatzbasiert sein kann (genauer gesagt, &quot;**[!UICONTROL pro Besuch]**).
* **Automatische Datenerfassung.** [!DNL Target] erfasst automatisch Informationen über Besucher, um die Personalisierungsmodelle zu erstellen. Weitere Informationen zu den verwendeten Parametern finden Sie unter [Automated Personalization-Datenerfassung](/help/main/c-activities/t-automated-personalization/ap-data.md).
* **Freigegebene Zielgruppen.** [!DNL Target] verwendet automatisch alle [!DNL Adobe Experience Cloud] freigegebenen Zielgruppen, um die Personalisierungsmodelle zu erstellen. Sie müssen keine spezifischen Aktionen ausführen, um dem Modell Zielgruppen hinzuzufügen. Weitere Informationen zum Verwenden von [!DNL Experience Cloud Audiences] mit [!DNL Target] finden Sie unter [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md).
* **Benutzerdefinierte Daten.** Marketing-Experten können Offline-Daten, Tendenzwerte oder andere benutzerdefinierte Daten hochladen, um Personalisierungsmodelle zu erstellen. Erfahren Sie mehr über [Hochladen von Daten für automatisches Targeting und Automated Personalization](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

### Unterschiede zwischen den beiden Aktivitätstypen {#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB}

Erwägen Sie **[!UICONTROL automatisches Targeting]** anstelle von **[!UICONTROL Automated Personalization]** wenn Sie das gesamte Erlebnis definieren, den gesamten Satz von **[!UICONTROL Visual Experience Composer]** (VEC)-Funktionen verwenden oder strukturelle Änderungen an Ihrer Seite vornehmen möchten.

| | [!UICONTROL Automatisches Targeting] | [!UICONTROL Automatisierte Personalisierung] |
|---|---|---|
| **Erlebnisdefinition** | Sie definieren das gesamte Erlebnis, das mehrere Änderungen enthalten kann. | Einzelne Angebote werden automatisch zu einem Erlebnis kombiniert. |
| **[!UICONTROL Visual Experience Composer]-Funktionen** | **[!UICONTROL Automatisches Targeting]** ist in den A/B-Aktivitäts-Workflow eingebettet und profitiert daher von ausgereifteren und vollwertigeren VEC. Sie können auch [QA-Links](/help/main/c-activities/c-activity-qa/activity-qa.md) verwenden. | Der Editor für benutzerspezifischen Code, mehrere Erlebniszielgruppen und andere Funktionen werden nicht unterstützt. |
| **Strukturänderungen an der Seite** | Besser geeignet. Sie können beispielsweise Elemente auf Ihrer Startseite neu anordnen. | Weniger geeignet. |
| **Anzahl der Erlebnisse** | In der Regel weniger, da ein Erlebnis mehrere Änderungen enthalten kann. | Normalerweise mehr, da die Erlebnisse alle Kombinationen von Angeboten und Standorten sind. |
| **Traffic zum Erstellen der Modelle erforderlich** | Häufig weniger insgesamt. | Häufig mehr insgesamt. |

Der Traffic *pro Erlebnis* der zum Erstellen der Modelle erforderlich ist, ist für beide Aktivitätstypen gleich. **[!UICONTROL Automatisches Targeting]** erfordert häufig weniger Gesamt-Traffic, da es in der Regel über weniger Erlebnisse verfügt.

Beispiel: In einer **[!UICONTROL Automated Personalization]**-Aktivität mit zwei Angeboten pro Standort und zwei Standorten gibt es vier (2 × 2 = 4) Gesamterlebnisse in der Aktivität (ohne Ausschlüsse). In **[!UICONTROL Automatisches Targeting]** können Sie Erlebnis 1 so einrichten, dass Angebot 1 an Speicherort 1 und Angebot 2 an Speicherort 2 einbezogen wird, und Erlebnis 2 so, dass Angebot 2 an Speicherort 1 und Angebot 1 an Speicherort 2 einbezogen werden. **[!UICONTROL Automatisches Targeting]** ermöglicht mehrere Änderungen in einem Erlebnis, sodass Sie die Gesamtzahl der Erlebnisse in Ihrer Aktivität reduzieren können.

### Traffic-Anforderungen für [!UICONTROL Automatisches Targeting] {#traffic-requirements}

Die folgenden Faustregeln helfen, die Traffic-Anforderungen zu verstehen:

* **Wenn [!UICONTROL Konversion] Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag und Erlebnis. Darüber hinaus muss die Aktivität mindestens 7.000 Besuche und 350 Konversionen aufweisen.
* **Wenn [!UICONTROL Umsatz pro Besuch] Ihre Erfolgsmetrik ist:** 1.000 Besuche und mindestens 50 Konversionen pro Tag und Erlebnis. Darüber hinaus muss die Aktivität mindestens 1.000 Konversionen pro Erlebnis aufweisen. **[!UICONTROL Umsatz pro Besuch]** erfordert in der Regel mehr Daten zum Erstellen von Modellen, da die Varianz bei den Besuchereinnahmen normalerweise höher als bei der Konversionsrate ist.

**[!UICONTROL Automatisches Targeting]** bietet außerdem ein umfassendes Framework für Online-Tests. Der mehrarmige Bandit ist Teil eines größeren Online-Test-Frameworks, das es [!DNL Adobe] Datenwissenschaftlern und Forschern ermöglicht, die Vorteile ihrer kontinuierlichen Verbesserung der realen Bedingungen zu verstehen. In Zukunft wird diese Testumgebung es [!DNL Adobe] ermöglichen, ihre Plattform für maschinelles Lernen für datenversierte Kunden zu öffnen, sodass sie ihre eigenen Modelle einbringen können, um die [!DNL Target] Modelle zu ergänzen.

Weitere Informationen zu Berichten finden Sie [Reporting und Automatisches Targeting](/help/main/c-activities/auto-target/reporting-and-auto-target.md).
