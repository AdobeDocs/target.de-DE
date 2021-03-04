---
keywords: a4t; Analytics; Analytics für Target; Analytics-Berichtsquelle; Adobe Analytics als Berichtsquelle für Target
description: Verwenden Sie Analytics für die Zielgruppe (A4T), um Aktivitäten zu erstellen, die auf Analytics-Konversionsmetriken und -Audiencen basieren, und verwenden Sie Analytics-Berichte, um die Ergebnisse zu untersuchen.
title: Was ist Analytics for Zielgruppe (A4T)?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4abf975095c5e29eea42d67119a426a3922d8d79
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 40%

---


# Adobe Analytics als Berichtsquelle für Adobe Target (A4T)

[!DNL Adobe Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Sie Aktivitäten auf der Grundlage von  [!DNL Analytics] Konversionsmetriken und Audiencen erstellen können. Mit der A4T-Integration können Sie [!DNL Analytics]-Berichte verwenden, um Ihre Ergebnisse zu untersuchen. Wenn Sie [!DNL Analytics] als Berichte für eine Aktivität verwenden, basieren der gesamte Berichte und die Segmentierung für diese Aktivität auf der Datenerfassung.[!DNL Analytics]

## A4T – Überblick {#section_92B66069210C40DBA937790E8CC596CF}

Die [!DNL Analytics for Target]-Integration zwischen [!DNL Analytics] und [!DNL Target] bietet leistungsstarke Analyse- und Zeitersparnis-Tools für Ihr Optimierungs-Programm.

Die drei Hauptvorteile der Verwendung von [!DNL Analytics]-Daten in [!DNL Target] sind:

* Marketingexperten können jederzeit dynamisch [!DNL Analytics]-Erfolgsmetriken oder -Berichte auf [!DNL Target]-Aktivitäten-Berichte anwenden. Es ist nicht erforderlich, vor Ausführung der Aktivität alles zu spezifizieren.
* Da alle Daten aus einer einzigen Quelle stammen, sind keine Schwankungen zu erwarten, die bei der Erfassung von Daten in zwei separaten Systemen auftreten würden.
* Ihre vorhandene [!DNL Analytics]-Implementierung erfasst alle erforderlichen Daten. Es ist nicht notwendig, Mboxes ausschließlich für das Erfassen von Daten für Berichte auf Seiten zu implementieren. Adobe empfiehlt weiterhin, eine Bestellbestätigungs-mbox für [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP)-Aktivitäten zu implementieren.

>[!IMPORTANT]
>
>Bevor Sie mit der Verwendung von A4T beginnen können, müssen Sie die Bereitstellung der Integration für Ihr Konto anfordern. Verwenden Sie [dieses Formular](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.
>
>Die Integration, die [!DNL Analytics] als Datenquelle für [!DNL Target] (A4T) aktiviert, stellt die nächste Generation der Test&amp;Zielgruppe zum SiteCatalyst-Plug-In dar. Dieses Plugin ist veraltet, es wird aber nach wie vor für Kunden unterstützt, die es bereits verwenden.

Wenn Sie [!DNL Analytics] als Berichte für eine Aktivität verwenden, basieren der gesamte Berichte und die Segmentierung für diese Aktivität auf [!DNL Analytics].

Alle [!DNL Analytics]-Metriken, einschließlich der berechneten Metriken, stehen in [!DNL Target] und der [!UICONTROL Zielgruppe-Aktivitäten]-Bericht in [!DNL Analytics] zur Verfügung. Ebenso können alle in [!DNL Analytics] verfügbaren Segmente auf beide Lösungen angewendet werden. Sie können die Metrik oder Audience auf den Bericht in [!DNL Target] anwenden, nachdem die Aktivität gestartet wurde oder sogar nachdem die Aktivität abgeschlossen wurde.

Jede Metrik wird einbezogen, einschließlich benutzerspezifischer oder berechneter Metriken, die in [!DNL Analytics] integriert sind.

Nach dem Klassifizierungszeitraum werden Daten ca. eine Stunde nach Erfassung auf der Site in diesen Berichten angezeigt. Sämtliche Metriken, Segmente und Werte in den Berichten stammen aus der Berichtssuite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Wenn Sie über einen Einsatz von A4T nachdenken, sollten Sie die folgenden Punkte beachten:

* Um [!DNL Analytics] als Berichte-Quelle für [!DNL Target] zu verwenden, müssen Sie und Ihre Firma Zugriff auf [!DNL Analytics] und auf [!DNL Target] haben. [Wenden Sie sich an Ihren Kundenvertreter,](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) wenn Sie eine der beiden Lösungen benötigen.
* Die Berichtsquelle wird für jede Aktivität festgelegt. [!DNL Target] erfasst weiterhin Daten, die in Berichte verwendet werden sollen, und  [!DNL Target] Daten stehen weiterhin zur Verfügung, wenn Sie eine Aktivität lieber auf von  [!DNL Target]Ihnen erfassten Daten stützen möchten.
* Verwenden Sie die eine oder andere Berichte-Quelle. Sie können für eine einzelne Aktivität nicht Daten aus beiden Quellen erfassen.
* Bei Verwendung von A4T sind alle für Ihre Aktivitäten verfügbaren Erfolgsmetriken [!DNL Analytics]-Metriken. Ihre Zielmetrik kann jedoch auf einem Mbox-Abruf basieren. Sie können beispielsweise die vordefinierten Klick-Tracking-Funktionen der Zielgruppe mit A4T verwenden, anstatt [!DNL Analytics]-Klick-Trackingcode implementieren zu müssen.
* Beim Anzeigen des Berichte einer A4T-Aktivität in der [!DNL Target]-Benutzeroberfläche werden [!DNL Analytics]-Daten angezeigt. Wenn Sie beispielsweise die Metrik [!UICONTROL Besucher] in [!DNL Target] verwenden, verwenden Sie die Metrik [!DNL Analytics] [!UICONTROL Besucher] und nicht die Metrik [!DNL Target] [!UICONTROL Besucher], die jetzt [!UICONTROL Teilnehmer] heißt. Dieser Unterschied ist besonders wichtig für grundlegende Traffic-Metriken ([!UICONTROL Besucher], [!UICONTROL Besuche], [!UICONTROL Ansichten]) und Konversionsmetriken.
* Alle vorhandenen [!DNL Target]-Aktivitäten verwenden weiterhin die Datenerfassung [!DNL Target] und sind von der Aktivierung von A4T nicht betroffen.
* Bei Verwendung von [!DNL Analytics] als Berichte ist nur eine mbox-basierte Metrik zulässig.
* Ein Server-zu-Server-Aufruf von [!DNL Target] bis [!DNL Analytics] sendet Aktivitäten- und Erlebnisinformationen an [!DNL Analytics]. Diese Integration führt nicht zu mehr Serveraufrufen für [!DNL Target] oder [!DNL Analytics].

   In einigen Fällen schlagen die Klassifizierungen von [!DNL Target] bis [!DNL Analytics] fehl und die Aktivitäten zeigen keine Daten in [!DNL Analytics] an. Siehe [Fehlerbehebung bei der Analytics- und Zielgruppe-Integration (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Sie können auch [den Kundendienst](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) kontaktieren, um weitere Unterstützung zu erhalten.

## Unterstützte Aktivität-Typen {#section_F487896214BF4803AF78C552EF1669AA}

Die folgende Tabelle zeigt, welche Aktivitäten [!DNL Analytics] als Berichte-Quelle in [!DNL Target] (A4T) unterstützen:

| Aktivitätstypen | Kompatibel mit A4T? | Anmerkungen (falls zutreffend) |
|--- |--- |--- |
| A/B-Aktivität mit manueller Traffic-Aufteilung | Ja |  |
| A/B-Aktivität mit automatisierter Zuordnung | Ja | Siehe [A4T-Unterstützung für Aktivitäten mit automatisierter Zuordnung und automatischer Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| A/B-Aktivität mit automatischem Targeting | Ja | Siehe [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischer Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| Erlebnis-Targeting (XT) | Ja |  |
| Multivarianz-Tests (MVT) | Ja | Erfordert das mbox-basierte Ziel einer Zielmetrik, um den Bericht [!UICONTROL Element Contribution] abzurufen. Der Bericht [!UICONTROL Element Contribution] unterstützt zurzeit keine [!DNL Analytics]-Metriken. |
| AP-Aktivität (Automatisierte Personalisierung) | Nein |  |
| Recommendations-Aktivität | Ja |  |
| Mobile App | Ja | Wird unterstützt mit dem Mobile Services SDK, Version 4.13.1 (oder neuer).  Weitere Informationen finden Sie in der [Dokumentation zu Mobile Services](https://experienceleague.adobe.com/docs/mobile-services/using/home.html). |
| E-Mail | Nein |  |
| Serverseitige Versand-API | Ja | Weitere Informationen finden Sie unter [Serverseitig: Target implementieren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| NodeJS-SDK | Ja | Weitere Informationen finden Sie unter [Serverseitig: Target implementieren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| AEM 6.1 (oder früher) Cloud Service Integration | Nein |  |
| AEM 6.2 (oder neuer) Cloud Service Integration | Ja | Weitere Informationen finden Sie unter [Integration mit Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in der [!DNL Adobe Experience Manager] 6.2-Dokumentation. |
| Jede Aktivität mit einem Umleitungs-Angebot | Ja | Die Mindestanforderungen für die Verwendung von Weiterleitungsangeboten mit A4T sind strenger. Weitere Informationen finden Sie unter [Umleitungsangebote – A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Ja | Weitere Informationen finden Sie unter [Node.js SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/nodejs-sdk) im Handbuch *Adobe Target SDKs*. |
| Java SDK | Ja | Weitere Informationen finden Sie unter [Java SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/java-sdk) im Handbuch *Adobe Target* SDKs. |

Da noch nicht alle Aktivitäten A4T unterstützen, sollten Sie wichtige Konversions-mboxes, wie z. B. die `orderConfirmPage`-mbox, beibehalten oder implementieren.

## Beispiele für A4T-Berichte {#section_F0A43A1CB2F04E8282B909E4D7034361}

Um A4T-Berichte in [!DNL Target] Ansicht, klicken Sie auf **[!UICONTROL Aktivitäten]**, klicken Sie in der Liste, die [!DNL Analytics] als Berichte verwendet, auf die gewünschte Aktivität und klicken Sie dann auf die Registerkarte **[!UICONTROL Berichte]**.

>[!NOTE]
>
>Sie können oben auf der Seite [!UICONTROL Aktivitäten] die Dropdown-Liste [!UICONTROL Berichtsquelle] nutzen, um nur Aktivitäten anzuzeigen, die [!DNL Analytics] als Berichtsquelle verwenden.

Sie können zwischen der [!UICONTROL Ansicht] und [!UICONTROL Grafik-Ansicht] des Berichts umschalten, indem Sie auf das entsprechende Symbol oben rechts im Bericht klicken.

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Berichtsmetrik], in der die verfügbaren [!DNL Analytics]-Zielmetriken aufgeführt sind:

![](assets/a4t_report_graph1.png)

Die folgende Abbildung zeigt die [!UICONTROL Diagrammansicht] eines A4T-Berichts mit der geöffneten Dropdownliste [!UICONTROL Zielgruppe], in der die verfügbaren [!DNL Analytics]-Zielgruppen aufgeführt sind:

![](assets/a4t_report_graph2.png)

Die folgende Abbildung zeigt die [!UICONTROL Tabellenansicht] eines A4T-Berichts:

![](assets/a4t_report_table.png)

Um den Bericht in [!DNL Analytics] statt in [!DNL Target] anzuzeigen, klicken Sie oben im Bericht auf **[!UICONTROL In Analytics anzeigen]**.

## Analytics und Target: Tutorial „Best Practices für Analysen“{#section_3438E6E77A464424B717A4FD333B84B2}

Öffnen Sie [Analytics und Zielgruppe: Best Practices für die Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), bereitgestellt von [!DNL Adobe Experience League].

## Schulungsvideos:

Die folgenden Videos enthalten weitere Informationen zu den in diesem Thema behandelten Konzepten.

### Analytics for Zielgruppe (A4T) (4:32) ![Kennzeichen &quot;Überblick&quot;](/help/assets/overview.png)

In diesem Video wird erläutert, wie [!DNL Analytics] als Berichte-Quelle in [!DNL Target] verwendet wird, um die Analyse Ihres Optimierungs-Programms zu fördern.

* Erläuterung: Was ist A4T und wozu dient es?
* Erläuterung der Funktionsweise von A4T
* Verstehen der Voraussetzungen für die Verwendung von A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics/Zielgruppe Integration (A4T) (40:33) ![Tutorial badge](/help/assets/tutorial.png)

Dieses Video ist eine Aufzeichnung von [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), eine Initiative, die vom Team der Adobe-Kundenunterstützung geleitet wird.

* So richten Sie die Integration ein und überprüfen, ob sie funktioniert
* So funktioniert die Integration
* Erfahren Sie, welche Berichte Sie in Analytics am besten verwenden
* Antworten auf häufige Fragen zu A4T

[Ambulanzzeiten für Analytics/Zielgruppe-Integration (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)
