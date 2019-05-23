---
description: Adobe „Analytics for Target“ (A4T) ist eine lösungsübergreifende Integration, die Ihnen das Erstellen von Aktivitäten ermöglicht, die auf Konversionsmetriken und Zielgruppensegmenten aus Analytics basieren. Dank dieser Integration können Sie Ihre Ergebnisse anhand von Analytics-Berichten überprüfen. Wenn Sie Analytics als Berichterstellungsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf der Analytics-Datenerfassung.
keywords: a4t; Analytics; Analytics für Target; Analytics-Berichtsquelle; Adobe Analytics als Berichtsquelle für Target
seo-description: Adobe „Analytics for Target“ (A4T) ist eine lösungsübergreifende Integration, die Ihnen das Erstellen von Aktivitäten ermöglicht, die auf Konversionsmetriken und Zielgruppensegmenten aus Analytics basieren. Dank dieser Integration können Sie Ihre Ergebnisse anhand von Analytics-Berichten überprüfen. Wenn Sie Analytics als Berichterstellungsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf der Analytics-Datenerfassung.
seo-title: Adobe Analytics als Berichtsquelle für Adobe Target (A4T)
solution: Target
subtopic: Multivarianz-Test
title: Adobe Analytics als Berichtsquelle für Adobe Target (A4T)
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: f59e96cd5afcae9d27d730aecead9eb360f04026

---


# Adobe Analytics als Berichtsquelle für Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

Adobe „Analytics for Target“ (A4T) ist eine lösungsübergreifende Integration, die Ihnen das Erstellen von Aktivitäten ermöglicht, die auf Konversionsmetriken und Zielgruppensegmenten aus Analytics basieren. Mit der A4T-Integration können Sie Ihre Ergebnisse anhand von Analytics-Berichten überprüfen. Wenn Sie Analytics als Berichterstellungsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf der Analytics-Datenerfassung.

## Überblick über A4T {#section_92B66069210C40DBA937790E8CC596CF}

Die Integration von Analytics for Target zwischen Analytics und Target bietet leistungsstarke Analysen und Tools mit Zeitersparnis für Ihr Optimierungsprogramm.

Die Verwendung von Analytics-Daten in Target bietet drei grundlegende Vorteile:

* Marketingexperten können zu jedem Zeitpunkt Analytics-Erfolgsmetriken oder Berichterstellungssegmente dynamisch auf Target-Aktivitätsberichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Da alle Daten aus einer einzigen Quelle stammen, sind keine Schwankungen zu erwarten, die bei der Erfassung von Daten in zwei separaten Systemen auftreten würden.
* Alle erforderlichen Daten werden von Ihrer bestehenden Adobe Analytics-Implementierung erfasst. Es ist nicht notwendig, Mboxes ausschließlich für das Erfassen von Daten für Berichte auf Seiten zu implementieren. Dennoch wird empfohlen, für automatisierte Personalisierungsaktivitäten eine Mbox für die Auftragsbestätigung zu implementieren.

>[!IMPORTANT]
>
>Bevor Sie A4T verwenden können, müssen Sie eine Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie [dieses Formular](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.
>
>Die Integration, die Adobe Analytics als Datenquelle für Adobe Target (A4T) aktiviert, stellt die nächste Generation des Test&amp;Target-zu-SiteCatalyst-Plugins dar. Dieses Plugin ist veraltet, es wird aber nach wie vor für Kunden unterstützt, die es bereits verwenden.

Wenn Sie Analytics als Berichtsquelle für eine Aktivität verwenden, basiert die gesamte Berichterstellung und Segmentierung für diese Aktivität auf Analytics.

Sämtliche Analytics-Metriken (einschließlich berechneter Metriken) sind in Target Standard/Premium und dem Target Activities-Bericht in Analytics verfügbar. Gleichermaßen können die in Analytics verfügbaren Segmente auf beide Lösungen angewendet werden. Sie können die Metrik oder die Zielgruppe auf den Bericht in Target Standard/Premium anwenden, nachdem der Test gestartet oder sogar nachdem der Test abgeschlossen wurde.

Jede Metrik ist enthalten, inklusive benutzerdefinierter oder berechneter Metriken, die in Analytics integriert sind.

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn Sie über einen Einsatz von A4T nachdenken, sollten Sie die folgenden Punkte beachten:

* Zur Verwendung von Adobe Analytics als Berichtsquelle für Adobe Target müssen Sie und Ihr Unternehmen Zugriff auf Adobe Analytics und Adobe Target haben. [Wenden Sie sich an Ihren Kundenvertreter,](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) wenn Sie eine der beiden Lösungen benötigen.
* Die Berichtsquelle wird für jede Aktivität festgelegt. Target erfasst weiterhin Daten für die Verwendung in der Berichterstellung, und Target-Daten sind nach wie vor verfügbar, wenn Sie es vorziehen, dass eine Aktivität auf von Target erfassten Daten basiert.
* Sie können nur eine der beiden Berichtsquellen verwenden. Sie können für eine einzelne Aktivität nicht Daten aus beiden Quellen erfassen.
* Wenn Sie A4T verwenden, sind alle Erfolgsmetriken, die für Ihre Aktivitäten zur Verfügung stehen, Analytics-Metriken. Ihre Zielmetrik kann jedoch auf einem Mbox-Abruf basieren. So können Sie zum Beispiel die in Target vorhandenen Clicktracking-Funktionen bei A4T nutzen, anstatt Clicktrackingcode für Analytics zu implementieren.
* Wenn Sie in der Target-Benutzeroberfläche Berichte zu einer A4T-Aktivität anzeigen, werden Ihnen Analytics-Daten angezeigt. Wenn Sie beispielsweise die Besucher-Metrik in Target verwenden, verwenden Sie die Besucher-Metrik von Analytics und nicht die von Target. Diese wird jetzt als „Entrants“ bezeichnet. Dieser Unterschied ist insbesondere für grundlegende Traffic-Metriken (Visitors, Visits, Page Views) und Konversionsmetriken von Bedeutung.
* Bereits vorhandene Target-Aktivitäten verwenden weiterhin die Target-Datenerfassung und sind von der Aktivierung von A4T nicht betroffen.
* Bei der Verwendung von Analytics als Berichtsquelle ist nur eine einzige Mbox-basierte Metrik erlaubt.
* Bei einem Server-zu-Server-Aufruf von Target zu Analytics werden Aktivitäts- und Erlebnisinformationen an Analytics gesendet. Durch diese Integration werden keine zusätzlichen Server-Aufrufe für Target oder Analytics getätigt.

## Unterstützte Aktivitätstypen {#section_F487896214BF4803AF78C552EF1669AA}

Die folgende Tabelle zeigt, welche Aktivitätstypen von Analytics als Berichtsquelle unterstützt werden (A4T):

| Aktivitätstypen | Kompatibel mit A4T? | Anmerkungen (falls zutreffend) |
|--- |--- |--- |
| A/B-Aktivität mit manueller Traffic-Aufteilung | Ja |
| A/B-Aktivität mit automatisierter Zuordnung | Nein |
| A/B-Aktivität mit automatischem Targeting | Nein |
| Erlebnis-Targeting (XT) | Ja |
| Multivarianz-Tests (MVT) | Ja | Erfordert, dass die Mbox-basierte Zielmetrik den Bericht „Elementbeitrag“ abruft.  Der Bericht „Elementbeitrag“ unterstützt derzeit keine Analytics-Metriken. |
| AP-Aktivität (Automatisierte Personalisierung) | Nein |
| Recommendations  Aktivitäten | Ja |
| Mobile Anwendung | Ja | Wird unterstützt mit dem Mobile Services SDK, Version 4.13.1 (oder neuer).  Weitere Informationen finden Sie in der [Dokumentation zu Mobile Services](https://marketing.adobe.com/resources/help/en_US/mobile/). |
| E-Mail | Nein |
| API für serverseitige Bereitstellung | Ja | Weitere Informationen finden Sie unter [Serverseitig: Target implementieren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| NodeJS-SDK | Ja | Weitere Informationen finden Sie unter [Serverseitig: Target implementieren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| AEM 6.1 (oder früher) Cloud Service Integration | Nein |
| AEM 6.2 (oder neuer) Cloud Service Integration | Ja | Weitere Informationen finden Sie unter [Integrieren mit Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in der Dokumentation zu Adobe Experience Manager 6.2. |
| Jede Aktivität mit einem Umleitungsangebot | Ja | Die Mindestanforderungen für die Verwendung von Weiterleitungsangeboten mit A4T sind strenger. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Ja |

Da noch nicht alle Aktivitätstypen A4T unterstützen, empfiehlt es sich, wichtige Konversions-Mboxes (wie die Mbox „orderConfirmPage“) beizubehalten oder zu implementieren.

## Beispiele für A4T-Berichte   {#section_F0A43A1CB2F04E8282B909E4D7034361}

Um A4T-Berichte in [!DNL Target]**anzuzeigen, klicken Sie auf[!UICONTROL Aktivitäten]**, dann in der Liste auf die gewünschte Aktivität, die [!DNL Analytics] als Berichtsquelle verwendet, und anschließend auf die Registerkarte **[!UICONTROL Berichte].**

>[!NOTE]
>
>Sie können oben auf der Seite [!UICONTROL Aktivitäten] die Dropdown-Liste [!UICONTROL Berichtsquelle] nutzen, um nur Aktivitäten anzuzeigen, die [!DNL Analytics] als Berichtsquelle verwenden.

Sie können zwischen Tabellenansicht und [!UICONTROL Diagrammansicht] des Berichts umschalten, indem Sie rechts oben im Bericht auf das entsprechende Symbol klicken.

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Berichtsmetrik], in der die verfügbaren [!DNL Analytics]-Zielmetriken aufgeführt sind:

![](assets/a4t_report_graph1.png)

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Zielgruppe], in der die verfügbaren [!DNL Analytics]-Zielgruppen aufgeführt sind:

![](assets/a4t_report_graph2.png)

Die folgende Abbildung zeigt die [!UICONTROL Tabellenansicht] eines A4T-Berichts:

![](assets/a4t_report_table.png)

Um den Bericht in [!DNL Analytics] statt in [!DNL Target] anzuzeigen, klicken Sie oben im Bericht auf **[!UICONTROL In Analytics anzeigen]**.

## Analytics und Target: Tutorial „Best Practices für Analysen“{#section_3438E6E77A464424B717A4FD333B84B2}

Öffnen Sie das Tutorial [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) von Adobe Experience League.

## Schulungsvideos:

Die folgenden Videos enthalten weitere Informationen zu den in diesem Artikel behandelten Konzepten.

### Analytics for Target (A4T) (4:32)

In diesem Video wird erläutert, wie sich Adobe Analytics als eine Adobe Target-Berichtsquelle einsetzen lässt, die die Analysen Ihres Optimierungsprogramms unterstützt.

* Erläuterung: Was ist A4T und wozu dient es?
* Erläuterung der Funktionsweise von A4T
* Verstehen der Voraussetzungen für die Verwendung von A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics/Target-Integration (A4T) (40:33)

Dieses Video ist eine Aufzeichnung von [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), eine Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* So richten Sie die Integration ein und überprüfen, ob sie funktioniert
* So funktioniert die Integration
* Erfahren Sie, welche Berichte Sie in Analytics am besten verwenden
* Antworten auf häufige Fragen zu A4T

>[!VIDEO](https://video.tv.adobe.com/v/22223/)