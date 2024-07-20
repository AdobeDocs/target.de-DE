---
keywords: a4t;Analytics;Analytics for Target;Analytics-Berichtsquelle;Adobe Analytics als Berichtsquelle für Target;at.js;Adobe Experience Platform Web SDK;Platform Web SDK;Plattform-SDK
description: Verwenden Sie  [!DNL Analytics]  für  [!DNL Target]  (A4T), um Aktivitäten basierend auf Konversionsmetriken und Zielgruppensegmenten von  [!DNL Analytics]  zu erstellen, und untersuchen Sie die Ergebnisse mithilfe  [!DNL Analytics] -Berichten.
title: Was ist  [!DNL Analytics]  für  [!DNL Target]  (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: f7bb9b5d6e96095a31f50f1976b87d9ee7b7eb51
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 81%

---

# [!DNL Adobe Analytics] fungiert als Berichtsquelle für [!DNL Adobe Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, die Ihnen das Erstellen von Aktivitäten ermöglicht, die auf Konversionsmetriken und Zielgruppensegmenten aus [!DNL Analytics] basieren. Mit der A4T-Integration können Sie Ihre Ergebnisse anhand von [!DNL Analytics]-Berichten überprüfen. Wenn Sie [!DNL Analytics] als Berichterstellungsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf der [!DNL Analytics]-Datenerfassung.

## Überblick {#section_92B66069210C40DBA937790E8CC596CF}

Die [!DNL Analytics for Target]-Integration zwischen [!DNL Analytics] und [!DNL Target] bietet leistungsstarke Analysen und Tools, die Ihnen helfen, Zeit zu sparen und Ihr Marketing-Programm zu optimieren.

Die Verwendung von [!DNL Analytics]-Daten in [!DNL Target] bietet drei grundlegende Vorteile:

* Marketing-Experten können zu jedem Zeitpunkt [!DNL Analytics]-Erfolgsmetriken oder Berichterstellungssegmente dynamisch auf [!DNL Target]-Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Da alle Daten aus einer einzigen Quelle stammen, sind keine Schwankungen zu erwarten, die bei der Erfassung von Daten in zwei separaten Systemen auftreten würden.
* Alle erforderlichen Daten werden durch Ihre bestehende [!DNL Analytics]-Implementierung erfasst. Es ist nicht notwendig, Mboxes auf Seiten zu implementieren, nur um Daten für Berichte zu erfassen.

Wenn Sie [!DNL Analytics] als Berichtsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf [!DNL Analytics].

Alle [!DNL Analytics] -Metriken, einschließlich berechneter Metriken, sind in [!DNL Target] und im [!UICONTROL Target Activities] -Bericht in [!DNL Analytics] verfügbar, mit einer Ausnahme. Die berechneten Metriken für [!UICONTROL Lift & Confidence] werden nicht unterstützt. Gleichermaßen können die in [!DNL Analytics] verfügbaren Segmente auf beide Lösungen angewendet werden. Sie können eine Metrik oder Zielgruppe auf einen [!DNL Target]-Bericht anwenden, nachdem eine Aktivität gestartet wurde oder sogar nachdem sie abgeschlossen ist.

Alle Metriken sind enthalten, einschließlich benutzerdefinierter oder berechneter Metriken, die in [!DNL Analytics] integriert sind.

Nach dem Classification-Zeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn Sie über einen Einsatz von A4T nachdenken, sollten Sie die folgenden Punkte beachten:

* Zur Verwendung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] müssen Sie und Ihr Unternehmen Zugriff auf [!DNL Analytics] und [!DNL Target] haben. [Wenden Sie sich an Ihren Kundenvertreter,](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) wenn Sie eine der beiden Lösungen benötigen.
* Die Berichtsquelle wird für jede Aktivität festgelegt. [!DNL Target] erfasst weiterhin Daten für die Verwendung in Berichten, und [!DNL Target]-Daten sind nach wie vor verfügbar, falls Sie möchten, dass Aktivitäten auf von [!DNL Target] erfassten Daten basieren.
* Sie können eine der beiden Berichtsquellen verwenden. Sie können für eine einzelne Aktivität nicht Daten aus beiden Quellen erfassen.
* Wenn Sie A4T verwenden, sind alle Erfolgsmetriken, die für Ihre Aktivitäten zur Verfügung stehen, [!DNL Analytics]-Metriken. Ihre Zielmetrik kann jedoch auf einem Mbox-Abruf basieren, wenn Sie at.js verwenden. So können Sie zum Beispiel die nativen Clicktracking-Funktionen von Target bei A4T nutzen, anstatt Clicktracking-Code für [!DNL Analytics] zu implementieren.
* Wenn Sie in der [!DNL Target]-Benutzeroberfläche Berichte zu einer A4T-Aktivität anzeigen, werden Ihnen [!DNL Analytics]-Daten angezeigt. Wenn Sie beispielsweise die Metrik [!UICONTROL Visitor] in [!DNL Target] verwenden, verwenden Sie die Metrik [!DNL Analytics] [!UICONTROL Visitor] und nicht die Metrik [!DNL Target] [!UICONTROL Visitors], die jetzt als [!UICONTROL Entrants] bezeichnet wird. Dieser Unterschied ist besonders für grundlegende Traffic-Metriken ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) und Konversionsmetriken wichtig.
* Bereits vorhandene [!DNL Target]-Aktivitäten verwenden weiterhin die von [!DNL Target] erfassten Daten und sind von der Aktivierung von A4T nicht betroffen.
* Bei der Verwendung von A4T ist nur eine einzige Mbox-basierte Metrik zulässig.
* Bei einem Server-zu-Server-Aufruf von [!DNL Target] an [!DNL Analytics] werden Aktivitäts- und Erlebnisinformationen an [!DNL Analytics] gesendet. Durch diese Integration werden keine zusätzlichen Server-Aufrufe für [!DNL Target] oder [!DNL Analytics] getätigt.

  Manchmal schlagen die in [!DNL Target] durchgeführten Classifications in [!DNL Analytics] fehl und in [!DNL Analytics] werden für Aktivitäten keine Daten angezeigt. Weitere Informationen dazu finden Sie im Abschnitt [Fehlerbehebung bei der Analytics- und Target-Integration (A4T)](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Sie können auch die [Kundenunterstützung kontaktieren](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB), wenn Sie weitere Hilfe benötigen.

## Implementieren von A4T

Informationen zur Implementierung von A4T mit at.js und [!DNL Adobe Experience Platform Web SDK] finden Sie im Abschnitt [Analytics für  [!DNL Target] -Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Unterstützte Aktivitätstypen {#section_F487896214BF4803AF78C552EF1669AA}

Die folgenden Abschnitte enthalten Informationen zu den unterstützten Aktivitätstypen bei der Verwendung von [!DNL Adobe Experience Platform Web SDK] oder at.js:

| Aktivitätstypen | Kompatibel mit A4T? | Anmerkungen (falls zutreffend) |
|--- |--- |--- |
| [A/B-Aktivität mit manueller Traffic-Aufteilung](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |  |
| [A/B-Aktivität mit automatisierter Zuordnung](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja | Siehe [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| [A/B-Aktivität mit automatischem Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Ja | A4T-Unterstützung für Aktivitäten des Typs „Automatisches Targeting“ ist jetzt sowohl für [!DNL Platform Web SDK] als auch für at.js verfügbar. |
| [Erlebnis-Targeting (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |  |
| [Multivarianz-Tests (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja | Erfordert das mbox-basierte Ziel-Metrik-Ziel, den [!UICONTROL Element Contribution] -Bericht zu erhalten. Der [!UICONTROL Element Contribution] -Bericht unterstützt derzeit keine [!DNL Analytics] -Metriken. |
| [AP-Aktivität (Automated Personalization)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nein |  |
| [Recommendations-Aktivität](/help/main/c-recommendations/recommendations.md) | Ja |  |
| [Jede Aktivität mit einem Umleitungsangebot](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Ja |

Da noch nicht alle Aktivitätstypen A4T unterstützen, empfiehlt es sich, wichtige Konversions-Mboxes (wie die Mbox „`orderConfirmPage`“) beizubehalten oder zu implementieren.

## Beispiele für A4T-Berichte {#section_F0A43A1CB2F04E8282B909E4D7034361}

Um A4T-Berichte in [!DNL Target] anzuzeigen, klicken Sie auf **[!UICONTROL Activities]**, klicken Sie in der Liste, die [!DNL Analytics] als Berichtsquelle verwendet, auf die gewünschte Aktivität und klicken Sie dann auf die Registerkarte **[!UICONTROL Reports]** .

>[!NOTE]
>
>Sie können die Dropdownliste &quot;[!UICONTROL Reporting Source]&quot;oben auf der Seite &quot;[!UICONTROL Activities]&quot;verwenden, um nur Aktivitäten anzuzeigen, die A4T verwenden.

Sie können zwischen [!UICONTROL Table View] und [!UICONTROL Graph View] des Berichts umschalten, indem Sie auf das entsprechende Symbol oben rechts im Bericht klicken.

Die folgende Abbildung zeigt den [!UICONTROL Graph View] eines A4T-Berichts mit der Dropdownliste [!UICONTROL Report Metric], in der die verfügbaren [!DNL Analytics] -Zielmetriken angezeigt werden:

![a4t_report_graph1 Bild](assets/a4t_report_graph1.png)

Die folgende Abbildung zeigt den [!UICONTROL Graph View] eines A4T-Berichts mit der Dropdownliste [!UICONTROL Audience], in der die verfügbaren [!DNL Analytics] Zielgruppen aufgeführt sind:

![a4t_report_graph2 Bild](assets/a4t_report_graph2.png)

Die folgende Abbildung zeigt den [!UICONTROL Table View] eines A4T-Berichts:

![a4t_report_table Bild](assets/a4t_report_table.png)

Um den Bericht in [!DNL Analytics] anstatt in [!DNL Target] anzuzeigen, klicken Sie oben im Bericht auf **[!UICONTROL View in Analytics]** .

## Analytics und Target: Tutorial „Best Practices für Analysen“ {#section_3438E6E77A464424B717A4FD333B84B2}

Öffnen Sie das Tutorial [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) von [!DNL Adobe Experience League].

## Schulungsvideos:

In den folgenden Videos erhalten Sie weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Analytics für Adobe Target (A4T) (4:32) ![Übersichts-Badge](/help/main/assets/overview.png)

In diesem Video wird erläutert, wie sich [!DNL Analytics] als eine [!DNL Target]-Berichtsquelle einsetzen lässt, die die Analysen Ihres Marketing-Programms unterstützt.

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

[Analytics/Target-Integration (A4T) Office Hours](https://helpx.adobe.com/de/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Analytics für  [!DNL Target] -Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md): Enthält Implementierungsinformationen für at.js und das Platform Web SDK.
>* [Umleitungsangebote – Häufig gestellte Fragen zu A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
>* [Was ist das Adobe Experience Platform Web SDK?](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de): Enthält allgemeine Informationen zum Platform Web SDK.
>* [Target-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html?lang=de): Enthält spezifische Informationen zu [!DNL Target] und [!DNL Platform Web SDK].
