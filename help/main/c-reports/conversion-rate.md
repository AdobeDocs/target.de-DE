---
keywords: Targeting
description: Erfahren Sie, wie Adobe [!DNL Target] zeigt die Konversionsrate, Steigerung, Konfidenz und Konfidenzintervall für jedes Erlebnis an und berechnet sie.
title: Wie kann ich die Konversionsrate, Steigerung und Konfidenzniveau anzeigen?
feature: Reports
exl-id: b4cfe926-eb36-4ce1-b56c-7378150b0b09
source-git-commit: 493ecd762b5228d33377ac8263b90a0f9c73127e
workflow-type: tm+mt
source-wordcount: '2150'
ht-degree: 53%

---

# Konversionsrate

Konversionsrate, Steigerung, Konfidenzintervall und Konfidenzintervall werden für jedes Erlebnis gemeldet.

In der folgenden Illustration wird die Diagrammüberschrift für eine Beispielaktivität in dargestellt, wobei die Überschriften [!UICONTROL Konversionsrate], [!UICONTROL Lift] und [!UICONTROL Konfidenz] hervorgehoben wurden.

![](assets/conversion-rate.jpg)

>[!NOTE]
>
>Duplizierte Bestellungen werden in allen Daten ignoriert, wenn ein `orderID` übergeben wird. Im Audit-Bericht werden die ignorierten duplizierten Bestellungen aufgelistet.

## Konversionsrate {#section_07A36846C4E84D0881906809B9CE5A74}

Zeigt die mittlere Konversionsrate, die Konfidenz, das Intervall und die Anzahl der Konversionen an.

Betrachten Sie zum Beispiel die folgende Berichtsspalte „Konversionsrate“:

![](assets/conversion-rate-detail.jpg)

Die erste Zeile ist das Kontrollerlebnis. Es zeigt eine Konversion von 15 Prozent mit drei Konversionen. Die zweite Zeile, Erlebnis B, zeigt eine Konversionsrate von 15 Prozent mit einem Konfidenzintervall von plus oder minus 15,65 Prozent und drei Konversionen an.

>[!NOTE]
>
>Derzeit wird das Konfidenzintervall nur für binäre Metriken berechnet.

## Steigerung {#section_0F409572C720433D9378092ABC999982}

Vergleicht für jedes Erlebnis die Konversionsrate mit dem Kontrollerlebnis.

Steigerung = (Erlebnis-CR - Kontroll-CR) / Kontroll-CR

Wenn die Kontrollinstanz 0 ist, gibt es keine prozentuale Steigerung.


## Verkaufsdaten {#section_30A674731BA6440E9BB93C421BE990EE}

AOV-, RPV- und Verkaufsdaten werden für jedes Erlebnis angezeigt, wenn Sie eine Bestellung einfügen (`orderConfirmPage`) und als Konversions-Mbox ausgewählt.

## Konfidenzniveau und Konfidenzintervall {#concept_0D0002A1EBDF420E9C50E2A46F36629B}

Für jedes Erlebnis werden das Konfidenzintervall und das Konfidenzintervall angezeigt.

Sie können Offlineberechnungen für for Target (A4T) durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics]Analytics erforderlich. Weitere Informationen dazu finden Sie weiter unten unter „Durchführen von Offline-Berechnungen für Analytics for Target (A4T)“.

### Konfidenz {#section_26FE5E44BDD5478792A65FCFD83DCCDC}

Die Konfidenz eines angezeigten Erlebnisses oder Angebots ist eine Wahrscheinlichkeit (ausgedrückt als Prozentsatz), ein Ergebnis zu erzielen, das weniger extrem ist als das tatsächlich beobachtete Ergebnis, wenn die Null-Hypothese wahr ist (im Wesentlichen, wenn es keinen Unterschied in den Konversionsraten zwischen diesem Erlebnis oder Angebot und dem Kontrollerlebnis/Angebot gibt). In Bezug auf p-Werte ist diese angezeigte Konfidenz 1 - p-Wert. Einfach ausgedrückt zeigt eine höhere Konfidenz, dass die Daten weniger konsistent mit der Annahme sind, dass das Kontroll- und Nicht-Kontrollangebot/-Erlebnis über gleiche Konversionsraten verfügen.

Das Vertrauen wird auf 100 % aufgerundet, wenn es größer oder gleich 99,995 % ist.

![](assets/conf_report.png)  ![](assets/conf_report_detail.png)

Bevor Sie jedoch eine geschäftliche Entscheidung treffen, sollten Sie warten, bis der Umfang der Proben groß genug ist und für ein oder mehrere Erlebnisse über einen längeren Zeitraum vier Vertrauensbalken angezeigt werden. So können Sie sicher sein, dass die Ergebnisse stabil sind.


### Konfidenzintervall {#section_F582738DFE1648C78B93D81EBC6CACF7}

>[!NOTE]
>
>Derzeit wird das Konfidenzintervall nur für binäre Metriken berechnet.

Die *Konfidenzintervall* ist ein Bereich von Schätzungen, innerhalb dessen der wahre Wert der Metrik auf einem bestimmten Konfidenzniveau gefunden werden kann. Target zeigt immer Konfidenzintervalle von 95 % an. Das Konfidenzintervall wird als hellgrauer +/–-Prozentsatz in der Spalte „Konversionsrate“ angezeigt. Im folgenden Beispiel beträgt das Konfidenzintervall für die Steigerung von Erlebnis B plus bzw. minus 15,65 Prozent.

![](assets/conversion_rate.png)

**Beispiel:** Der beobachtete RPV eines Erlebnisses beträgt 10 USD und 95 % **Konfidenzintervall** zwischen 5 und 15 Dollar beträgt. Unbekannt ist der tatsächliche RPV 12 Dollar. Wenn wir diesen Test dann mehrmals ausgeführt haben, enthalten 95 % der Zeit, in der das zu berechnende Konfidenzintervall die _true_ Wert des RPV von 12 USD.

**Was beeinflusst das Konfidenzintervall?** Die Formel folgt statistischen Standardmethoden zur Berechnung der Konfidenzintervalle.

* **Probengröße:** Wenn die Probengröße steigt, wird das Intervall kleiner. Das wird bevorzugt, da es bedeutet, dass Ihre Berichte näher an den wahren Wert der Erfolgsmetrik herankommen.
* **Standardabweichung geringer:** Weitere ähnliche Ergebnisse, z. B. ähnliche AOVs oder ähnliche Besucher-Konversionszahlen pro Tag, führen zu einer Reduzierung der Standardabweichung.

## Berechnung der Konfidenz und Anleitung zur Offline-Berechnung  {#section_86F7C231943043A5B8B6BFE67B706E3B}

Der [heruntergeladene CSV-Bericht](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden.

Um diese berechneten Metriken zu berechnen, laden Sie die [Vollständige Vertrauensberechnung](/help/main/assets/complete_confidence_calculator.xlsx) Excel-Datei zur Eingabe des Aktivitätswerts oder zur Überprüfung [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

>[!NOTE]
>
>Dieser Rechner dient für Target-basierte Berichte und nicht für A4T-Berichte.

## Durchführen von Offlineberechnungen für Analytics für Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Für A4T verwenden wir eine [Welch&#39;s t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} Berechnung für kontinuierliche Variablen (anstelle binärer Metriken). In Analytics werden Besucher immer verfolgt und jede durchgeführte Aktion wird gezählt. Wenn ein Besucher mehrfach einkauft oder eine Erfolgsmetrik mehrfach besucht, werden diese zusätzlichen Treffer also gezählt. Daher ist die Metrik eine kontinuierliche Variable. Um die t-Test-Berechnung des Welch durchzuführen, ist die &quot;Quadratsumme&quot;erforderlich, um die Varianz zu berechnen, die im Nenner der t-Statistik verwendet wird. [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) erläutert die Einzelheiten der verwendeten mathematischen Formeln. Die Quadratsumme kann abgerufen werden von [!DNL Analytics]. Zum Abrufen der Summe aus Quadratdaten müssen Sie für einen Testzeitraum einen Export auf Besucherebene für die zu optimierende Metrik durchführen.

Wenn Sie beispielsweise auf Seitenansichten pro Besucher optimieren, exportieren Sie eine Stichprobe der Gesamtanzahl der Seitenansichten pro Besucher für einen bestimmten Zeitraum, vielleicht einige Tage (nur einige tausend Datenpunkte sind erforderlich). Anschließend quadrieren Sie die einzelnen Werte und bilden die Summe der Gesamtwerte (die Reihenfolge der Vorgänge muss hier unbedingt beachtet werden). Dieser „Quadratsummen“-Wert wird anschließend im Complete Confidence Calculator verwendet. Verwenden Sie für diese Werte den Bereich „Umsatz“ dieses Arbeitsblatts.

**So verwenden Sie die [!DNL Analytics]-Datenexportfunktion:**

1. Melden Sie sich bei [!DNL Adobe Analytics] an.
1. Klicken Sie auf **[!UICONTROL Werkzeuge]** > **[!UICONTROL Data Warehouse]**.
1. Füllen Sie auf der Registerkarte **[!UICONTROL Data Warehouse-Anforderung]** die Felder aus.

   Weitere Informationen zu den einzelnen Feldern finden Sie unter „Data Warehouse-Beschreibungen“ in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Feld | Anleitung |
   |--- |--- |
   | Anforderungsname | Geben Sie einen Namen für Ihre Anforderung ein. |
   | Berichtsdatum | Geben Sie einen Zeitraum und eine Granularität an.<br>Es hat sich bewährt, für die erste Anforderung maximal eine Stunde oder einen Tag mit Daten auszuwählen.  Die Verarbeitung von Data Warehouse-Dateien dauert umso länger, je länger der angeforderte Zeitraum ist. Daher ist es immer am besten, zunächst Daten für einen kleineren Zeitraum anzufordern, um sicherzustellen, dass die Datei das erwartete Ergebnis zurückgibt. Rufen Sie anschließend Request Manager auf, duplizieren Sie die Anforderung und fragen Sie beim zweiten Durchlauf mehr Daten an. Wenn Sie die Granularität auf einen anderen Wert als &quot;Keine&quot;umschalten, wird die Dateigröße drastisch erhöht.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Verfügbare Segmente | Wenden Sie bei Bedarf ein Segment an. |
   | Aufschlüsselung | Wählen Sie die gewünschten Dimensionen aus:   Die Standardeinstellung ist Out-Of-The-Box (OOTB), während die benutzerdefinierte Einstellung eVars und Eigenschaften umfasst. Es wird empfohlen, &quot;Besucher-ID&quot;zu verwenden, wenn Informationen zur Besucher-ID-Ebene erforderlich sind, anstatt &quot;Experience Cloud-Besucher-ID&quot;.<ul><li>Die Besucher-ID ist die finale ID, die von Analytics verwendet wird. Sie lautet entweder AID (wenn es sich um einen bestehenden Kunden handelt) oder MID (wenn der Kunde neu ist oder nach dem Start des MC-Besucher-ID-Diensts Cookies gelöscht hat).</li><li>Die Experience Cloud-Besucher-ID wird nur für Kunden festgelegt, die neu sind oder nach dem Start des MC-Besucher-ID-Service Cookies gelöscht haben.</li></ul> |
   | Metriken | Wählen Sie die gewünschten Metriken aus. Die Standardeinstellung lautet OOTB, während die benutzerdefinierte Einstellung benutzerdefinierte Ereignisse einschließt. |
   | Berichtvorschau | Überprüfen Sie vor dem Planen des Berichts Ihre Einstellungen.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Auslieferung planen | Geben Sie eine E-Mail-Adresse ein, an den die Datei gesendet wird. Benennen Sie die Datei und wählen Sie dann [!UICONTROL Sofort senden] aus.<br>Hinweis: Die Datei kann über FTP unter [!UICONTROL Erweiterte Auslieferungsoptionen]<br>![Lieferung planen](/help/main/c-reports/assets/datawarehouse3.png) ausgegeben werden. |

1. Klicken Sie auf **[!UICONTROL Diesen Bericht anfordern]**.

   Die Dateibereitstellung kann je nach Umfang der angeforderten Daten bis zu 72 Stunden in Anspruch nehmen. Sie können den Fortschritt Ihrer Anforderung jederzeit überprüfen, indem Sie auf [!UICONTROL Werkzeuge] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] klicken.

   Wenn Sie Daten, die Sie in der Vergangenheit angefordert haben, erneut anfordern möchten, können Sie eine alte Anforderung aus dem [!UICONTROL Anforderungs-Manager] nach Bedarf.

Weitere Informationen über [!DNL Data Warehouse] finden Sie in der [!DNL Analytics]-Hilfsdokumentation unter den folgenden Links:

* [Erstellen einer Data Warehouse-Anforderung](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Best Practices für Data Warehousen](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)

## Zählmethodik {#concept_EC19BC897D66411BABAF2FA27BCE89AA}

Sie können sich Berichte nach verschiedenen Zählmethodiken anzeigen lassen, um besser zu verstehen, wie Ihre Aktivitäten im Laufe der Zeit oder während einer einzelnen Sitzung bei den Benutzern ankommen.

Die Zählmethodik wird von folgenden Aktivitätstypen unterstützt:

* A/B-Test

   Eine Ausnahme stellen automatische Target-A/B-Aktivitäten dar, die lediglich die Standardzählmethodik „Besuch“ unterstützen.

* Erlebnis-Targeting (XT)
* Multivarianz-Tests (MVT)

   Target unterstützt für den Beitragsbericht der MVT-Elemente keine Aktivitätsimpressionen als Umsatzmetriktypen.

* Recommendations

Derzeit wird von Aktivitäten mit automatisierter Personalisierung (AP) nur die Standardzählmethodik (Besuche) unterstützt.

Berichte können nach folgenden Zählmethodiken angezeigt werden:

* **Teilnehmer:** Ein eindeutig identifizierbarer Teilnehmer an der Aktivität (während der gesamten Aktivitätsdauer).

   Eine Person wird als neuer Teilnehmer gezählt, wenn der Besuch über einen anderen Computer oder Browser erfolgt, wenn das entsprechende Cookie gelöscht wurde oder wenn der Besucher konvertiert und mit demselben Cookie zur Aktivität zurückkehrt. Ein Teilnehmer wird mithilfe der PCID im Mbox-Cookie des Besuchers identifiziert. Ändert sich die PCID, wird die Person als neuer Besucher betrachtet.

* **Besuch:** Ein eindeutig identifizierbarer Teilnehmer eines Erlebnisses während einer einzelnen 30-minütigen Browsersitzung

   Wenn eine Konversion erreicht wird oder ein Besucher nach einer Abwesenheit von mindestens 30 Minuten die Site erneut aufruft, zählt auch ein wiederkehrender Besucher als neuer Besuch. Ein Besucher wird mithilfe der `sessionID` im Mbox-Cookie des Besuchers gekennzeichnet. Ändert sich die `sessionID`, wird der Besuch als neuer Besuch angesehen.

* **Impression/Seitenansicht:** Hier wird jedes Laden einer beliebigen Seite der Aktivität durch einen Besucher gezählt.

   Ein einzelner Besuch kann diverse Impressionen, z. B. Ihrer Startseite, beinhalten.

>[!NOTE]
>
>In der Regel werden Zählungen durch Cookies und Sitzungsaktivitäten bestimmt. Wenn Sie jedoch den End-Konversionspunkt einer Aktivität erreichen und die Aktivität dann erneut aufrufen, werden Sie als neuer Teilnehmer und neuer Aktivitätsbesuch gezählt. Dies trifft auch dann zu, wenn sich die Werte Ihrer PCID und der `sessionID` nicht geändert haben.

## Warum [!DNL Target] empfiehlt die Verwendung von Welch-T-Tests? {#t-test}

A/B-Tests sind Experimente, um den Mittelwert einiger Geschäftsmetriken in einer Kontrollvariante (auch als Erlebnis bezeichnet) mit dem Mittelwert derselben Metrik in einem oder mehreren alternativen Erlebnissen zu vergleichen.

[!DNL Target] empfiehlt, [Welch&#39;s t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test), da diese weniger Annahmen erfordern als Alternativen wie z-Tests und der geeignete statistische Test für paarweise Vergleiche von (quantitativen) Geschäftsmetriken zwischen Kontrollerlebnissen und alternativen Erlebnissen sind.

### Im Detail

Bei der Durchführung von Online-A/B-Tests wird jeder Benutzer/Besucher zufällig einer einzelnen Variante zugewiesen. Anschließend nehmen wir Messungen der Geschäftsmetriken vor, die von Interesse sind (z. B. Konversionen, Bestellungen, Umsatz usw.) für Besucher in den einzelnen Varianten. Der verwendete statistische Test testet dann die Hypothese, dass die mittlere Geschäftsmetrik (z. B. Konversionsrate, Bestellungen pro Benutzer, Umsatz pro Benutzer usw.) entspricht der Kontrollgruppe und einer bestimmten alternativen Variante.

Obwohl die Geschäftsmetrik selbst möglicherweise entsprechend einer beliebigen Verteilung verteilt wird, sollte die Verteilung des Mittelwerts dieser Metrik (innerhalb jeder Variante) über die [Central Limit Theorem](https://en.wikipedia.org/wiki/Central_limit_theorem). Beachten Sie, dass zwar keine Garantie dafür besteht, wie schnell sich diese Stichprobenverteilung des Mittelwerts auf den Normalwert annähert, diese Bedingung jedoch in der Regel aufgrund des Umfangs der Besucher bei Online-Tests erreicht wird.

Bei dieser Normalität des Mittelwerts kann nachgewiesen werden, dass die zu verwendende Teststatistik einer t-Verteilung folgt, da dies das Verhältnis eines normal verteilten Werts (die Differenz der Mittel der Geschäftsmetrik) zu einem Skalierungsbegriff ist, der auf einer Schätzung aus den Daten basiert (der Standardfehler der Mitteldifferenz). Die **t-Test** ist dann der geeignete Hypothesentest, da die Teststatistik einer t-Verteilung folgt.

### Warum keine anderen Tests verwendet werden

A **z-Test** ist technisch unangemessen, da im typischen A/B-Testszenario der Nenner der Teststatistik nicht aus einer bekannten Varianz abgeleitet wurde und stattdessen anhand der Daten geschätzt werden muss. Bei ausreichend großen Stichprobengrößen sind die z-Test- und t-Test jedoch identisch.

**Chi-squared-Tests** werden nicht verwendet, da diese zur Bestimmung der qualitativen Beziehung zwischen zwei Varianten geeignet sind (d. h. einer Nullhypothese, dass es keinen Unterschied zwischen Varianten gibt). T-Tests eignen sich besser für das Szenario von _quantitativ_ Metriken vergleichen.

Die **Mann-Whitney-U-Test** ist ein nichtparametrischer Test, der geeignet ist, wenn die Stichprobenverteilung der durchschnittlichen Geschäftsmetrik (für jede Variante) normalerweise nicht verteilt wird. Wie bereits erwähnt, gilt in Anbetracht des Umfangs des mit Online-Tests verbundenen Traffics in der Regel das zentrale Limit-Theorem, sodass der t-Test sicher angewendet werden kann.

Komplexere Methoden wie **ANOVA** (die T-Tests auf mehr als zwei Varianten verallgemeinern) können angewendet werden, wenn ein Test mehr als zwei Erlebnisse aufweist (&quot;A/Bn-Tests&quot;). ANOVA beantwortet jedoch die Frage &quot;ob alle Varianten denselben Mittelwert haben&quot;, während wir uns im typischen A/Bn-Test mehr für _welche spezifische Variante_ ist am besten. In [!DNL Target]Daher wenden wir regelmäßige T-Tests an, bei denen jede Variante mit einer Kontrolle verglichen wird, wobei eine Bonferroni-Korrektur vorgenommen wird, um mehrere Vergleiche zu berücksichtigen.