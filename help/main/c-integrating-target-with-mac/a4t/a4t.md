---
keywords: a4t; Analytics; Analytics für Target; Analytics-Berichtsquelle; Adobe Analytics als Berichtsquelle für Target; at.js; Adobe Experience Platform Web SDK; Platform Web SDK; Plattform-SDK
description: Verwendung [!DNL Analytics] für [!DNL Target] (A4T), um Aktivitäten zu erstellen, die auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmente und Verwendung [!DNL Analytics] Berichte zur Untersuchung der Ergebnisse.
title: Was ist [!DNL Analytics] für [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 30%

---

# [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Sie Aktivitäten erstellen können, die auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmente. Mit der A4T-Integration können Sie [!DNL Analytics] Berichte, um Ihre Ergebnisse zu überprüfen. Wenn Sie [!DNL Analytics] als Berichtsquelle für eine Aktivität dient, basieren alle Berichte und Segmentierungen für diese Aktivität auf [!DNL Analytics] Datenerfassung.

## Überblick {#section_92B66069210C40DBA937790E8CC596CF}

Die [!DNL Analytics for Target] Integration zwischen [!DNL Analytics] und [!DNL Target] bietet leistungsstarke Analyse- und Zeitersparniswerkzeuge für Ihr Optimierungsprogramm.

Die drei Hauptvorteile der Verwendung von [!DNL Analytics] Daten in [!DNL Target] sind:

* Marketingexperten können dynamisch [!DNL Analytics] Erfolgsmetriken oder Berichtssegmente an [!DNL Target] Aktivitätsberichte. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Da alle Daten aus einer einzigen Quelle stammen, sind keine Schwankungen zu erwarten, die bei der Erfassung von Daten in zwei separaten Systemen auftreten würden.
* Ihre vorhandene [!DNL Analytics] -Implementierung erfasst alle erforderlichen Daten. Es ist nicht notwendig, Mboxes ausschließlich für das Erfassen von Daten für Berichte auf Seiten zu implementieren.

Wenn Sie [!DNL Analytics] als Berichtsquelle für eine Aktivität dient, basieren alle Berichte und Segmentierungen für diese Aktivität auf [!DNL Analytics].

Alle [!DNL Analytics] Metriken, einschließlich berechneter Metriken, sind verfügbar in [!DNL Target] und [!UICONTROL Target Activities] in [!DNL Analytics], mit einer Ausnahme. Die berechneten Metriken für [!UICONTROL Steigerung und Konfidenz] werden nicht unterstützt. Gleichermaßen sind alle Segmente verfügbar in [!DNL Analytics] kann auf beide Lösungen angewendet werden. Sie können die Metrik oder Zielgruppe auf den Bericht in [!DNL Target] nach dem Start der Aktivität oder auch nach Abschluss der Aktivität.

Jede Metrik ist enthalten, einschließlich benutzerdefinierter oder berechneter Metriken, die in [!DNL Analytics].

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn Sie über einen Einsatz von A4T nachdenken, sollten Sie die folgenden Punkte beachten:

* Verwendung [!DNL Analytics] als Berichtsquelle für [!DNL Target], müssen Sie und Ihr Unternehmen Zugriff auf [!DNL Analytics] und [!DNL Target]. [Wenden Sie sich an Ihren Kundenvertreter,](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) wenn Sie eine der beiden Lösungen benötigen.
* Die Berichtsquelle wird für jede Aktivität festgelegt. [!DNL Target] erfasst weiterhin Daten für die Verwendung in Berichten und [!DNL Target] Daten sind weiterhin verfügbar, wenn Sie es vorziehen, eine Aktivität auf Daten zu stützen, die von [!DNL Target].
* Verwenden Sie eine Berichtsquelle oder die andere. Sie können für eine einzelne Aktivität nicht Daten aus beiden Quellen erfassen.
* Bei Verwendung von A4T sind alle für Ihre Aktivitäten verfügbaren Erfolgsmetriken [!DNL Analytics] Metriken. Bei der Verwendung von at.js kann Ihre Zielmetrik jedoch auf einem Mbox-Aufruf basieren. Sie können beispielsweise die vordefinierten Klick-Tracking-Funktionen von Target mit A4T verwenden, anstatt [!DNL Analytics] Klick-Trackingcode.
* Beim Anzeigen der Berichterstellung für eine A4T-Aktivität im [!DNL Target] Benutzeroberfläche, die Sie anzeigen [!DNL Analytics] Daten. Wenn Sie beispielsweise die [!UICONTROL Besucher] Metrik in [!DNL Target], verwenden Sie die [!DNL Analytics] [!UICONTROL Besucher] Metrik, nicht die [!DNL Target] [!UICONTROL Besucher] Metrik, die jetzt [!UICONTROL Teilnehmer]. Dieser Unterschied ist besonders für grundlegende Traffic-Metriken wichtig ([!UICONTROL Besucher], [!UICONTROL Besuche], [!UICONTROL Seitenansichten]) und Konversionsmetriken.
* Vorhandene [!DNL Target] weiterhin [!DNL Target] Datenerfassung und sind von der Aktivierung von A4T nicht betroffen.
* Bei der Verwendung von A4T ist nur eine mbox-basierte Metrik zulässig.
* Ein Server-zu-Server-Aufruf von [!DNL Target] nach [!DNL Analytics] sendet Aktivitäts- und Erlebnisinformationen an [!DNL Analytics]. Diese Integration führt nicht zu zusätzlichen Server-Aufrufen für [!DNL Target] oder [!DNL Analytics].

   In einigen Situationen wird die Classification aus [!DNL Target] nach [!DNL Analytics] Fehlschlagen und Aktivitäten zeigen keine Daten in [!DNL Analytics]. Siehe [Fehlerbehebung bei der Analytics- und Target-Integration (A4T)](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Sie können auch [Kundenunterstützung kontaktieren](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) für weitere Hilfe.

## A4T implementieren

Informationen zur Implementierung von A4T mit at.js und der [!DNL Adobe Experience Platform Web SDK], siehe [Analytics für [!DNL Target] Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Unterstützte Aktivitätstypen {#section_F487896214BF4803AF78C552EF1669AA}

Die folgenden Abschnitte enthalten Informationen zu den unterstützten Aktivitätstypen bei der Verwendung der [!DNL Adobe Experience Platform Web SDK] oder at.js:

| Aktivitätstypen | Kompatibel mit A4T? | Anmerkungen (falls zutreffend) |
|--- |--- |--- |
| [A/B-Aktivität mit manueller Traffic-Aufteilung](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |  |
| [A/B-Aktivität mit automatisierter Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja | Siehe [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| [A/B-Aktivität mit automatischem Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Ja | Siehe [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| [Erlebnis-Targeting (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |  |
| [Multivarianz-Tests (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja | Erfordert das mbox-basierte Ziel-Metrikziel, um die [!UICONTROL Element Contribution] Bericht. Die [!UICONTROL Element Contribution] Bericht wird derzeit nicht unterstützt [!DNL Analytics] Metriken. |
| [AP-Aktivität (Automatisierte Personalisierung)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nein |  |
| [Recommendations-Aktivität](/help/main/c-recommendations/recommendations.md) | Ja |  |
| [Jede Aktivität mit einem Umleitungsangebot](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Ja |

Da alle Aktivitätstypen A4T noch nicht unterstützen, wird empfohlen, wichtige Konversions-Mboxes beizubehalten oder zu implementieren, wie z. B. die `orderConfirmPage` mbox.

## Beispiele für A4T-Berichte {#section_F0A43A1CB2F04E8282B909E4D7034361}

So zeigen Sie A4T-Berichte in [!DNL Target]klicken **[!UICONTROL Tätigkeiten]** klicken Sie auf die gewünschte Aktivität in der Liste, die [!DNL Analytics] als Berichtsquelle verwenden, klicken Sie auf die **[!UICONTROL Berichte]** Registerkarte.

>[!NOTE]
>
>Sie können die [!UICONTROL Berichtsquelle] Dropdown-Liste oben im [!UICONTROL Tätigkeiten] Seite, um nur Aktivitäten anzuzeigen, die A4T verwenden.

Sie können zwischen [!UICONTROL Tabellenansicht] und [!UICONTROL Diagrammansicht] durch Klicken auf das entsprechende Symbol oben rechts im Bericht.

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Berichtsmetrik], in der die verfügbaren [!DNL Analytics]-Zielmetriken aufgeführt sind:

![](assets/a4t_report_graph1.png)

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Zielgruppe], in der die verfügbaren [!DNL Analytics]-Zielgruppen aufgeführt sind:

![](assets/a4t_report_graph2.png)

Die folgende Abbildung zeigt die [!UICONTROL Tabellenansicht] eines A4T-Berichts:

![](assets/a4t_report_table.png)

Um den Bericht in [!DNL Analytics] statt in [!DNL Target] anzuzeigen, klicken Sie oben im Bericht auf **[!UICONTROL In Analytics anzeigen]**.

## Analytics und Target: Tutorial „Best Practices für Analysen“ {#section_3438E6E77A464424B717A4FD333B84B2}

Öffnen Sie die [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) Tutorial, bereitgestellt von [!DNL Adobe Experience League].

## Schulungsvideos:

Die folgenden Videos enthalten weitere Informationen zu den in diesem Thema behandelten Konzepten.

### Analytics for Adobe Target (A4T) (4:32) ![Übersichtszeichen](/help/main/assets/overview.png)

In diesem Video wird die Verwendung von [!DNL Analytics] als Berichtsquelle in [!DNL Target] um die Analyse Ihres Optimierungsprogramms voranzutreiben.

* Erläuterung: Was ist A4T und wozu dient es?
* Erläuterung der Funktionsweise von A4T
* Verstehen der Voraussetzungen für die Verwendung von A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics/Adobe Target-Integration (A4T) (40:33) ![Tutorial-Badge](/help/main/assets/tutorial.png)

Dieses Video ist eine Aufzeichnung von [Office Hours](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), eine Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* So richten Sie die Integration ein und überprüfen, ob sie funktioniert
* So funktioniert die Integration
* Erfahren Sie, welche Berichte Sie in Analytics am besten verwenden
* Antworten auf häufige Fragen zu A4T

[Analytics/Target-Integration (A4T) Geschäftszeiten](https://helpx.adobe.com/de/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Analytics für [!DNL Target] Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md): Enthält Implementierungsinformationen für at.js und das Platform Web SDK.
>* [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
>* [Was ist das Adobe Experience Platform Web SDK?](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html): Enthält Übersichtsinformationen zum Platform Web SDK.
>* [Target-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html): Enthält spezifische Informationen zu [!DNL Target] und [!DNL Platform Web SDK].

