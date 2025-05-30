---
keywords: Targeting
description: Erfahren Sie [!DNL Target]  wie Adobe Konversionsrate, Steigerung, Konfidenz und Konfidenzintervall für jedes Erlebnis anzeigt und berechnet.
title: Wie kann ich Konversionsrate, Steigerung und Konfidenzniveau anzeigen?
feature: Reports
exl-id: b4cfe926-eb36-4ce1-b56c-7378150b0b09
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '2113'
ht-degree: 49%

---

# Konversionsrate

Konversionsrate, Steigerung, Konfidenz und Konfidenzintervall werden für jedes Erlebnis gemeldet.

Die folgende Abbildung zeigt die Diagrammkopfzeile für eine Beispielaktivität mit hervorgehobenen [!UICONTROL Conversion Rate]-, [!UICONTROL Lift]- und [!UICONTROL Confidence].

![Bild mit Konversionsrate](assets/conversion-rate.jpg)

>[!NOTE]
>
>Duplizierte Bestellungen werden in allen Daten ignoriert, wenn ein `orderID` übergeben wird. Im Audit-Bericht werden die ignorierten duplizierten Bestellungen aufgelistet.

## Konversionsrate {#section_07A36846C4E84D0881906809B9CE5A74}

Zeigt die mittlere Konversionsrate, die Konfidenz, das Intervall und die Anzahl der Konversionen an.

Betrachten Sie zum Beispiel die folgende Berichtsspalte „Konversionsrate“:

![Bild mit Konversionsrate und Details](assets/conversion-rate-detail.jpg)

Die erste Zeile ist das Kontrollerlebnis. Es zeigt eine Konversion von 15 Prozent mit drei Konversionen. Die zweite Zeile, Erlebnis B, zeigt eine Konversionsrate von 15 Prozent mit einem Konfidenzintervall von plus oder minus 15,65 Prozent und drei Konversionen an.

>[!NOTE]
>
>Derzeit wird das Konfidenzintervall nur für binäre Metriken berechnet.

## Steigerung {#section_0F409572C720433D9378092ABC999982}

Vergleicht für jedes Erlebnis die Konversionsrate mit dem Kontrollerlebnis.

Steigerung = (Erlebnis-CR - Kontroll-CR) / Kontroll-CR

Wenn die Kontrollinstanz 0 ist, gibt es keine prozentuale Steigerung.


## Verkaufsdaten {#section_30A674731BA6440E9BB93C421BE990EE}

AOV-, RPV- und Verkaufsdaten werden für jedes Erlebnis angezeigt, wenn Sie eine Mbox für Platzierungsaufträge (`orderConfirmPage`) eingefügt und als Konversions-Mbox ausgewählt haben.

## Konfidenzniveau und Konfidenzintervall {#concept_0D0002A1EBDF420E9C50E2A46F36629B}

Für jedes Erlebnis werden die Konfidenz und das Konfidenzintervall angezeigt.

Sie können Offlineberechnungen für for Target (A4T) durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics]Analytics erforderlich. Weitere Informationen dazu finden Sie weiter unten unter „Durchführen von Offline-Berechnungen für Analytics for Target (A4T)“.

### Konfidenz {#section_26FE5E44BDD5478792A65FCFD83DCCDC}

Die Konfidenz eines angezeigten Erlebnisses oder Angebots ist eine Wahrscheinlichkeit (ausgedrückt als Prozentsatz), mit der ein Ergebnis erzielt wird, das weniger extrem ist als das tatsächlich beobachtete Ergebnis, wenn die Nullhypothese wahr ist (im Wesentlichen, wenn es keinen Unterschied bei den Konversionsraten zwischen diesem Erlebnis oder Angebot und dem Kontrollerlebnis/Angebot gibt). Im Hinblick auf p-Werte ist diese angezeigte Konfidenz 1 - p-Wert. Einfach ausgedrückt: Eine höhere Konfidenz deutet darauf hin, dass die Daten weniger konsistent mit der Annahme sind, dass das Angebot/Erlebnis der Kontrolle und des Nicht-Kontrollbereichs die gleichen Konversionsraten aufweisen.

Das Vertrauen wird auf 100 % aufgerundet, wenn es größer oder gleich 99,995 % ist.

![conf_report image](assets/conf_report.png) ![conf_report_detail image](assets/conf_report_detail.png)

Bevor Sie jedoch eine geschäftliche Entscheidung treffen, sollten Sie warten, bis der Umfang der Proben groß genug ist und für ein oder mehrere Erlebnisse über einen längeren Zeitraum vier Vertrauensbalken angezeigt werden. So können Sie sicher sein, dass die Ergebnisse stabil sind.


### Konfidenzintervall {#section_F582738DFE1648C78B93D81EBC6CACF7}

>[!NOTE]
>
>Derzeit wird das Konfidenzintervall nur für binäre Metriken berechnet.

Das *Konfidenzintervall* ist ein Bereich von Schätzungen, innerhalb dessen der wahre Wert der Metrik bei einem bestimmten Konfidenzniveau gefunden werden kann. Target zeigt immer 95-%-Konfidenzintervalle an. Das Konfidenzintervall wird als hellgrauer +/–-Prozentsatz in der Spalte „Konversionsrate“ angezeigt. Im folgenden Beispiel beträgt das Konfidenzintervall für die Steigerung von Erlebnis B plus bzw. minus 15,65 Prozent.

![Bild mit Konversionsrate](assets/conversion_rate.png)

**Beispiel** Der beobachtete RPV eines Erlebnisses beträgt 10 $ und das 95 %-**(Konfidenzintervall** beträgt 5 bis 15 $. Unbekannt für uns, sein wahrer RPV ist $12. Wenn wir diesen Test dann mehrmals ausgeführt haben, enthalten 95 % der Zeit, die wir für das Konfidenzintervall berechnen, den _true_-Wert des RPV von 12 USD.

**Was beeinflusst das Konfidenzintervall?** Die Formel folgt statistischen Standardmethoden zur Berechnung der Konfidenzintervalle.

* **Probengröße:** Wenn die Probengröße steigt, wird das Intervall kleiner. Das wird bevorzugt, da es bedeutet, dass Ihre Berichte näher an den wahren Wert der Erfolgsmetrik herankommen.
* **Standardabweichung geringer:** Weitere ähnliche Ergebnisse, z. B. ähnliche AOVs oder ähnliche Besucher-Konversionszahlen pro Tag, führen zu einer Reduzierung der Standardabweichung.

## Berechnung der Konfidenz und Anleitung zur Offline-Berechnung  {#section_86F7C231943043A5B8B6BFE67B706E3B}

Der [heruntergeladene CSV-Bericht](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) enthält nur Rohdaten und keine berechneten Metriken wie Umsatz pro Besucher, Steigerung oder Konfidenz, die für A/B-Tests verwendet werden.

Um diese berechneten Metriken zu berechnen, laden Sie die Excel-Datei [Complete Confidence Calculator des Ziels](/help/main/assets/complete_confidence_calculator.xlsx) herunter, um den Wert der Aktivität einzugeben, oder überprüfen Sie [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

>[!NOTE]
>
>Dieser Rechner dient für Target-basierte Berichte und nicht für A4T-Berichte.

## Durchführen von Offline-Berechnungen für Analytics for Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Für A4T verwenden wir eine [Welchs t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank}-Berechnung für kontinuierliche Variablen (anstelle binärer Metriken). In Analytics werden Besucher immer verfolgt und jede durchgeführte Aktion wird gezählt. Wenn ein Besucher mehrfach einkauft oder eine Erfolgsmetrik mehrfach besucht, werden diese zusätzlichen Treffer also gezählt. Daher ist die Metrik eine kontinuierliche Variable. Zur Berechnung des t-Tests von Welch wird die „Summe der Quadrate“ benötigt, um die Varianz zu berechnen, die im Nenner der t-Statistik verwendet wird. [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) erläutert die Details der verwendeten mathematischen Formeln. Die Summe der Quadrate kann aus [!DNL Analytics] abgerufen werden. Zum Abrufen der Summe aus Quadratdaten müssen Sie für einen Testzeitraum einen Export auf Besucherebene für die zu optimierende Metrik durchführen.

Wenn Sie beispielsweise die Anzeige von Seitenansichten pro Besucher optimieren, exportieren Sie ein Beispiel für die Gesamtzahl der Seitenansichten pro Besucher für einen bestimmten Zeitraum, vielleicht für einige Tage (mehr als tausend Datenpunkte sind alles, was Sie benötigen). Anschließend quadrieren Sie die einzelnen Werte und bilden die Summe der Gesamtwerte (die Reihenfolge der Vorgänge muss hier unbedingt beachtet werden). Dieser „Quadratsummen“-Wert wird anschließend im Complete Confidence Calculator verwendet. Verwenden Sie für diese Werte den Bereich „Umsatz“ dieses Arbeitsblatts.

**So verwenden Sie die [!DNL Analytics]-Datenexportfunktion:**

1. Melden Sie sich bei [!DNL Adobe Analytics] an.
1. Klicken Sie auf **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Füllen Sie auf der Registerkarte **[!UICONTROL Data Warehouse Request]** die Felder aus.

   Weitere Informationen zu den einzelnen Feldern finden Sie unter „Data Warehouse-Beschreibungen“ in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html?lang=de).

   | Feld | Anleitung |
   |--- |--- |
   | Anforderungsname | Geben Sie einen Namen für Ihre Anforderung ein. |
   | Berichtsdatum | Geben Sie einen Zeitraum und eine Granularität an.<br>Es hat sich bewährt, für die erste Anforderung maximal eine Stunde oder einen Tag mit Daten auszuwählen.  Die Verarbeitung von Data Warehouse-Dateien dauert umso länger, je länger der angeforderte Zeitraum ist. Daher ist es immer am besten, zunächst Daten für einen kleineren Zeitraum anzufordern, um sicherzustellen, dass die Datei das erwartete Ergebnis zurückgibt. Rufen Sie anschließend Request Manager auf, duplizieren Sie die Anforderung und fragen Sie beim zweiten Durchlauf mehr Daten an. Wenn Sie die Granularität auf einen anderen Wert als „Keine“ umschalten, wird die Dateigröße ebenfalls drastisch erhöht.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Verfügbare Segmente | Wenden Sie bei Bedarf ein Segment an. |
   | Aufschlüsselung | Wählen Sie die gewünschten Dimensionen aus: Standard ist vorkonfiguriert (OOTB), während „Benutzerdefiniert“ eVars und Props enthält. Es wird empfohlen, „Besucher-ID“ zu verwenden, wenn Informationen auf Besucher-ID-Ebene benötigt werden, und nicht &quot;Experience Cloud-Besucher-ID“.<ul><li>Die Besucher-ID ist die finale ID, die von Analytics verwendet wird. Sie lautet entweder AID (wenn es sich um einen bestehenden Kunden handelt) oder MID (wenn der Kunde neu ist oder nach dem Start des MC-Besucher-ID-Diensts Cookies gelöscht hat).</li><li>Die Experience Cloud-Besucher-ID wird nur für Kunden festgelegt, die neu sind oder nach dem Start des MC-Besucher-ID-Service Cookies gelöscht haben.</li></ul> |
   | Metriken | Wählen Sie die gewünschten Metriken aus. Die Standardeinstellung lautet OOTB, während die benutzerdefinierte Einstellung benutzerdefinierte Ereignisse einschließt. |
   | Berichtvorschau | Überprüfen Sie vor dem Planen des Berichts Ihre Einstellungen.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Auslieferung planen | Geben Sie eine E-Mail-Adresse ein, an die die Datei gesendet werden soll, benennen Sie die Datei und wählen Sie dann [!UICONTROL Send Immediately] aus.<br>Hinweis: Die Datei kann über FTP unter &quot;[!UICONTROL Advanced Delivery Options]<br>![ Versand planen“ ](/help/main/c-reports/assets/datawarehouse3.png) werden. |

1. Klicken Sie auf **[!UICONTROL Request this Report]**.

   Die Dateibereitstellung kann je nach Umfang der angeforderten Daten bis zu 72 Stunden in Anspruch nehmen. Sie können den Fortschritt Ihrer Anfrage jederzeit überprüfen, indem Sie auf [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] klicken.

   Wenn Sie Daten erneut anfordern möchten, die Sie in der Vergangenheit angefordert haben, können Sie bei Bedarf eine alte Anfrage aus der [!UICONTROL Request Manager] duplizieren.

Weitere Informationen über [!DNL Data Warehouse] finden Sie in der [!DNL Analytics]-Hilfsdokumentation unter den folgenden Links:

* [Erstellen einer Data Warehouse-Anfrage](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html?lang=de)
* [Best Practices für Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html?lang=de)

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

## Warum empfiehlt [!DNL Target] die Verwendung von Welchs T-Tests? {#t-test}

A/B-Tests sind Experimente, bei denen der Mittelwert einer Geschäftsmetrik in einer Kontrollvariante (auch als Erlebnis bezeichnet) mit dem Mittelwert derselben Metrik in einem oder mehreren alternativen Erlebnissen verglichen wird.

[!DNL Target] empfiehlt die Verwendung von [Welchs t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test), da diese weniger Annahmen erfordern als Alternativen wie z-Tests und der geeignete statistische Test sind, um paarweise (quantitative) Geschäftsmetriken zwischen Kontrollerlebnissen und alternativen Erlebnissen zu vergleichen.

### Im Detail

Beim Ausführen von Online-A/B-Tests wird jeder Benutzer/Besucher nach dem Zufallsprinzip einer einzelnen Variante zugewiesen. Anschließend messen wir die gewünschten Geschäftsmetriken (z. B. Konversionen, Bestellungen, Umsatz usw.) für Besucher in jeder Variante. Der von uns verwendete statistische Test testet dann die Hypothese, dass die durchschnittliche Geschäftsmetrik (z. B. Konversionsrate, Bestellungen pro Benutzer, Umsatz pro Benutzer usw.) für die Kontrolle und eine bestimmte alternative Variante gleich ist.

Obwohl die Geschäftsmetrik selbst nach einer beliebigen Verteilung verteilt sein könnte, sollte die Verteilung des Mittelwerts dieser Metrik (innerhalb jeder Variante) über den [Zentralen Grenzwertsatz) zu einer normalen Verteilung ](https://en.wikipedia.org/wiki/Central_limit_theorem). Beachten Sie, dass es zwar keine Garantie dafür gibt, wie schnell sich diese Stichprobenverteilung des Mittelwerts auf den Normalwert annähert, diese Bedingung jedoch angesichts der Besucherzahl bei Online-Tests normalerweise erfüllt wird.

Angesichts dieser Normalität des Mittelwerts kann gezeigt werden, dass die zu verwendende Teststatistik einer T-Verteilung folgt, da es sich um das Verhältnis eines normal verteilten Werts (der Differenz der Mittelwerte der Geschäftsmetrik) zu einem Skalierungsterm auf der Grundlage einer Schätzung aus den Daten (der Standardfehler der Differenz der Mittelwerte) handelt. Der **t-Test** ist dann der geeignete Hypothesentest, wenn die Teststatistik einer t-Verteilung folgt.

### Warum keine anderen Tests verwendet werden

Ein **z-Test** ist technisch ungeeignet, da im typischen A/B-Testszenario der Nenner der Teststatistik nicht aus einer bekannten Varianz abgeleitet wird, sondern aus den Daten geschätzt werden muss. Bei ausreichend großen Stichprobengrößen sind der z-Test und der t-Test jedoch identisch.

**Chi-Quadrat** Tests werden nicht verwendet, da diese geeignet sind, um zu bestimmen, ob eine qualitative Beziehung zwischen zwei Varianten besteht (d. h. eine Nullhypothese, dass es keinen Unterschied zwischen Varianten gibt). T-Tests eignen sich besser für das Szenario _(quantitativen_ Vergleichs von Metriken.

Der **Mann-Whitney-U** Test ist ein nichtparametrischer Test, der geeignet ist, wenn die Stichprobenverteilung der mittleren Geschäftsmetrik (für jede Variante) nicht normal verteilt ist. Wie jedoch bereits erwähnt, gilt in Anbetracht der Größenordnung des Traffics, der in Online-Tests involviert ist, normalerweise der Satz der zentralen Grenze, sodass der t-Test sicher angewendet werden kann.

Komplexere Methoden wie **ANOVA** (die T-Tests auf mehr als zwei Varianten generalisieren) können angewendet werden, wenn ein Test mehr als zwei Erfahrungen hat („A/Bn-Tests„). ANOVA beantwortet jedoch die Frage „ob alle Varianten den gleichen Mittelwert haben“, während wir im typischen A/Bn-Test mehr daran interessiert sind _welche spezifische Variante_ am besten ist. In [!DNL Target] wenden wir daher regelmäßige t-Tests an, um jede Variante mit einer Kontrolle zu vergleichen, mit einer Bonferroni-Korrektur, um Mehrfachvergleiche zu berücksichtigen.