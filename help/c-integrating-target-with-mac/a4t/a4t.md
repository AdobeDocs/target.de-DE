---
keywords: a4t; Analytics; Analytics für Target; Analytics-Berichtsquelle; Adobe Analytics als Berichtsquelle für Target; at.js; Adobe Experience Platform Web SDK; Platform Web SDK; Plattform-SDK
description: Verwenden Sie [!DNL Analytics] for [!DNL Target] (A4T) to create activities based on [!DNL Analytics] conversion metrics and audience segments and use [!DNL Analytics] Berichte, um die Ergebnisse zu untersuchen.
title: Was ist [!DNL Analytics] for [!DNL Target] (A4T)?
feature: 'Analytics for Target (A4T) '
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: 3be6ad187b99472ccd3019e6998eba4953e2f5b5
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 30%

---

# [!DNL Adobe Analytics] als Berichtsquelle für ( [!DNL Adobe Target] A4T)

[!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Sie Aktivitäten erstellen können, die auf  [!DNL Analytics] Konversionsmetriken und Zielgruppensegmenten basieren. Mit der A4T-Integration können Sie [!DNL Analytics]-Berichte verwenden, um Ihre Ergebnisse zu untersuchen. Wenn Sie [!DNL Analytics] als Berichtsquelle für eine Aktivität verwenden, basieren alle Berichte und Segmentierungen für diese Aktivität auf der [!DNL Analytics] Datenerfassung.

>[!NOTE]
>
>Die A4T-Unterstützung in einer [!DNL Adobe Experience Platform Web SDK]-Implementierung, die in diesem Artikel besprochen wird, soll mit der [!DNL Platform Web SDK]-Version 2.5.0 (1. Juni 2021) verfügbar sein.

## Überblick {#section_92B66069210C40DBA937790E8CC596CF}

Die Integration von [!DNL Analytics for Target] zwischen [!DNL Analytics] und [!DNL Target] bietet leistungsstarke Analyse- und Zeitsparungswerkzeuge für Ihr Optimierungsprogramm.

Die Verwendung von [!DNL Analytics]-Daten in [!DNL Target] bietet drei Hauptvorteile:

* Marketingexperten können [!DNL Analytics] Erfolgsmetriken oder Berichterstellungssegmente dynamisch jederzeit auf [!DNL Target] Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Da alle Daten aus einer einzigen Quelle stammen, sind keine Schwankungen zu erwarten, die bei der Erfassung von Daten in zwei separaten Systemen auftreten würden.
* Ihre vorhandene [!DNL Analytics]-Implementierung erfasst alle erforderlichen Daten. Es ist nicht notwendig, Mboxes ausschließlich für das Erfassen von Daten für Berichte auf Seiten zu implementieren.

Wenn Sie [!DNL Analytics] als Berichtsquelle für eine Aktivität verwenden, basieren alle Berichte und Segmentierungen für diese Aktivität auf [!DNL Analytics].

Alle [!DNL Analytics] -Metriken, einschließlich berechneter Metriken, sind in [!DNL Target] und im [!UICONTROL Target Activities] -Bericht in [!DNL Analytics] verfügbar, mit einer Ausnahme. Die berechneten Metriken für [!UICONTROL Lift und Konfidenz] werden nicht unterstützt. Ebenso kann jedes in [!DNL Analytics] verfügbare Segment auf beide Lösungen angewendet werden. Sie können die Metrik oder Zielgruppe in [!DNL Target] auf den Bericht anwenden, nachdem die Aktivität gestartet wurde oder selbst nachdem die Aktivität abgeschlossen wurde.

Jede Metrik ist enthalten, einschließlich benutzerdefinierter oder berechneter Metriken, die in [!DNL Analytics] integriert sind.

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn Sie über einen Einsatz von A4T nachdenken, sollten Sie die folgenden Punkte beachten:

* Um [!DNL Analytics] als Berichtsquelle für [!DNL Target] zu verwenden, müssen Sie und Ihr Unternehmen Zugriff auf [!DNL Analytics] und [!DNL Target] haben. [Wenden Sie sich an Ihren Kundenvertreter,](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) wenn Sie eine der beiden Lösungen benötigen.
* Die Berichtsquelle wird für jede Aktivität festgelegt. [!DNL Target] erfasst weiterhin Daten zur Verwendung in Berichten und  [!DNL Target] Daten sind weiterhin verfügbar, wenn Sie es vorziehen, eine Aktivität auf Daten zu stützen, die von  [!DNL Target]erfasst wurden.
* Verwenden Sie eine Berichtsquelle oder die andere. Sie können für eine einzelne Aktivität nicht Daten aus beiden Quellen erfassen.
* Bei der Verwendung von A4T sind alle für Ihre Aktivitäten verfügbaren Erfolgsmetriken [!DNL Analytics] Metriken. Bei der Verwendung von at.js kann Ihre Zielmetrik jedoch auf einem Mbox-Aufruf basieren. Sie können beispielsweise die vordefinierten Klick-Tracking-Funktionen von Target mit A4T verwenden, anstatt [!DNL Analytics] Klick-Tracking-Code implementieren zu müssen.
* Beim Anzeigen der Berichterstellung für eine A4T-Aktivität in der [!DNL Target] -Benutzeroberfläche werden [!DNL Analytics]-Daten angezeigt. Wenn Sie beispielsweise die Metrik [!UICONTROL Besucher] in [!DNL Target] verwenden, verwenden Sie die Metrik [!DNL Analytics] [!UICONTROL Besucher], nicht die Metrik [!DNL Target] [!UICONTROL Besucher] , die jetzt [!UICONTROL Teilnehmer] heißt. Dieser Unterschied ist besonders für grundlegende Traffic-Metriken ([!UICONTROL Besucher], [!UICONTROL Besuche], [!UICONTROL Seitenansichten]) und Konversionsmetriken wichtig.
* Alle vorhandenen [!DNL Target] -Aktivitäten verwenden weiterhin die Datenerfassung [!DNL Target] und sind von der Aktivierung von A4T nicht betroffen.
* Bei der Verwendung von A4T ist nur eine mbox-basierte Metrik zulässig.
* Ein Server-zu-Server-Aufruf von [!DNL Target] an [!DNL Analytics] sendet Aktivitäts- und Erlebnisinformationen an [!DNL Analytics]. Diese Integration führt nicht zu zusätzlichen Server-Aufrufen für [!DNL Target] oder [!DNL Analytics].

   In einigen Fällen schlagen die Klassifizierungen von [!DNL Target] bis [!DNL Analytics] fehl und Aktivitäten zeigen keine Daten in [!DNL Analytics] an. Siehe [Fehlerbehebung bei der Analytics- und Target-Integration (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Sie können auch [den Kundendienst](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) kontaktieren, um weitere Unterstützung zu erhalten.

## A4T implementieren

Informationen zur Implementierung von A4T mit at.js und [!DNL Adobe Experience Platform Web SDK] finden Sie unter [Analytics for [!DNL Target] implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Unterstützte Aktivitätstypen {#section_F487896214BF4803AF78C552EF1669AA}

Die folgenden Abschnitte enthalten Informationen zu unterstützten Aktivitätstypen bei Verwendung von [!DNL Adobe Experience Platform Web SDK] oder at.js:

| Aktivitätstypen | Kompatibel mit A4T? | Anmerkungen (falls zutreffend) |
|--- |--- |--- |
| [A/B-Aktivität mit manueller Traffic-Aufteilung](/help/c-activities/t-test-ab/test-ab.md) | Ja |  |
| [A/B-Aktivität mit automatisierter Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja | Siehe [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| [A/B-Aktivität mit automatischem Targeting](/help/c-activities/auto-target/auto-target-to-optimize.md) | Ja | Siehe [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| [Erlebnis-Targeting (XT)](/help/c-activities/t-experience-target/experience-target.md) | Ja |  |
| [Multivarianz-Tests (MVT)](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja | Erfordert das mbox-basierte Ziel einer Zielmetrik, um den Bericht [!UICONTROL Element Contribution] zu erhalten. Der Bericht [!UICONTROL Element Contribution] unterstützt derzeit keine [!DNL Analytics]-Metriken. |
| [AP-Aktivität (Automatisierte Personalisierung)](/help/c-activities/t-automated-personalization/automated-personalization.md) | Nein |  |
| [Recommendations-Aktivität](/help/c-recommendations/recommendations.md) | Ja |  |

Da alle Aktivitätstypen A4T noch nicht unterstützen, wird empfohlen, wichtige Konversions-Mboxes wie die Mbox `orderConfirmPage` zu behalten oder zu implementieren.

## Beispiele für A4T-Berichte {#section_F0A43A1CB2F04E8282B909E4D7034361}

Um A4T-Berichte in [!DNL Target] anzuzeigen, klicken Sie auf **[!UICONTROL Aktivitäten]**, klicken Sie in der Liste auf die gewünschte Aktivität, die [!DNL Analytics] als Berichtsquelle verwendet, und klicken Sie dann auf die Registerkarte **[!UICONTROL Berichte]** .

>[!NOTE]
>
>Sie können die Dropdownliste [!UICONTROL Berichtsquelle] oben auf der Seite [!UICONTROL Aktivitäten] verwenden, um nur Aktivitäten anzuzeigen, die A4T verwenden.

Sie können zwischen [!UICONTROL Tabellenansicht] und [!UICONTROL Diagrammansicht] des Berichts umschalten, indem Sie auf das entsprechende Symbol oben rechts im Bericht klicken.

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Berichtsmetrik], in der die verfügbaren [!DNL Analytics]-Zielmetriken aufgeführt sind:

![](assets/a4t_report_graph1.png)

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Zielgruppe], in der die verfügbaren [!DNL Analytics]-Zielgruppen aufgeführt sind:

![](assets/a4t_report_graph2.png)

Die folgende Abbildung zeigt die [!UICONTROL Tabellenansicht] eines A4T-Berichts:

![](assets/a4t_report_table.png)

Um den Bericht in [!DNL Analytics] statt in [!DNL Target] anzuzeigen, klicken Sie oben im Bericht auf **[!UICONTROL In Analytics anzeigen]**.

## Analytics und Target: Tutorial „Best Practices für Analysen“ {#section_3438E6E77A464424B717A4FD333B84B2}

Öffnen Sie [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)-Tutorial, bereitgestellt von [!DNL Adobe Experience League].

## Schulungsvideos:

Die folgenden Videos enthalten weitere Informationen zu den in diesem Thema behandelten Konzepten.

### Analytics for Adobe Target (A4T) (4:32) ![Badge &quot;Überblick&quot;](/help/assets/overview.png)

In diesem Video wird erläutert, wie Sie [!DNL Analytics] als Berichtsquelle in [!DNL Target] verwenden können, um die Analyse Ihres Optimierungsprogramms voranzutreiben.

* Erläuterung: Was ist A4T und wozu dient es?
* Erläuterung der Funktionsweise von A4T
* Verstehen der Voraussetzungen für die Verwendung von A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics/Adobe Target Integration (A4T) (40:33) ![Tutorial Badge](/help/assets/tutorial.png)

Dieses Video ist eine Aufzeichnung von [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), eine Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* So richten Sie die Integration ein und überprüfen, ob sie funktioniert
* So funktioniert die Integration
* Erfahren Sie, welche Berichte Sie in Analytics am besten verwenden
* Antworten auf häufige Fragen zu A4T

[Analytics/Target-Integration (A4T) Geschäftszeiten](https://helpx.adobe.com/de/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Analytics  [!DNL Target] für die Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md): Enthält Implementierungsinformationen für at.js und das Platform Web SDK.
>* [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
* [Was ist das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)? Enthält Übersichtsinformationen zum Platform Web SDK.
* [Target-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html): Enthält spezifische Informationen zu  [!DNL Target] und  [!DNL Platform Web SDK].

