---
description: Bei Ihrem Datenerfassungsprozess treten verschiedene Änderungen auf, wenn Sie Analytics als Berichtsquelle für Target (A4T) verwenden.
keywords: Recommendations
seo-description: Bei Ihrem Datenerfassungsprozess treten verschiedene Änderungen auf, wenn Sie Analytics als Berichtsquelle für Target (A4T) verwenden.
seo-title: Vor der Implementierung Adobe Analytics als Berichtsquelle für Adobe Target (A4T)
solution: Target
title: Vor der Implementierung
topic: Premium
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Vor der Implementierung{#before-you-implement}

Bei Ihrem Datenerfassungsprozess treten verschiedene Änderungen auf, wenn Sie Analytics als Berichtsquelle für Target (A4T) verwenden.

Bevor Sie sich für die Verwendung dieser Integration entscheiden, überprüfen Sie folgende Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Berichtsprozesse:

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie A4T verwenden können, müssen Sie eine Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie [dieses Formular](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.

Für diese A4T-Integration müssen Sie in Abhängigkeit davon, ob Sie Weiterleitungsangebote in A4T verwenden möchten oder nicht, die folgenden Bibliotheksversionen (oder neuere) implementieren:

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* Experience Cloud-Besucher-ID-Service: visitorAPI.js, Version 1.8.0
* Adobe Target (je nach Implementierung): at.js, Version 0.9.1 oder mbox.js, Version 61
* Adobe Analytics: appMeasurement.js, Version 1.7.0

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* Experience Cloud-Besucher-ID-Service: visitorAPI.js, Version 2.3.0
* Adobe Target: at.js Version 1.6.2

   **Hinweis:** Die mbox.js-Bibliothek unterstützt keine Weiterleitungsangebote mit A4T. Ihre Implementierung muss at.js verwenden.

* Adobe Analytics: appMeasurement.js, Version 2.1

Download- und Implementierungsanweisungen sind im Abschnitt [Adobe für die Target-Implementierung](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_a4timplementation.html) aufgelistet.

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* Diese Integration ist bei neuen Aktivitäten aktiviert, wenn Sie Analytics als Berichtsquelle auswählen. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* Der Prozess zur Einrichtung von Analytics als Berichtsquelle für Target umfasst verschiedene Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nach dem Ausführen dieser Schritte können Sie Analytics als Ihre Berichtsquelle verwenden, sobald es für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Der Besucher-ID-Service erstellt eine freigegebene Besucher-ID in Experience Cloud. Sie ersetzt zwar nicht die Target-mboxPC-ID oder die UUID in Audience Manager, jedoch ersetzt sie die Art und Weise, wie neue Besucher in Analytics ermittelt werden. Bei ordnungsgemäßer Konfiguration sollten wiederkehrende Analytics-Besucher ebenfalls über ihre alte Analytics-ID identifiziert werden, um Besucherklippen zu verhindern. Gleichermaßen gehen beim Upgrade auf den Besucher-ID-Service keine Profildaten von Target-Besuchern verloren, da die Target-mboxPC-ID intakt bleibt.
* Der Besucher-ID-Service muss vor dem Analytics- und Target-Seiten-Code ausgeführt werden. Stellen Sie sicher, dass `VisitorAPI.js` über den Tags für alle anderen Experience Cloud-Produkte angezeigt wird.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nach der Aktivierung dieser Integration werden Sie eine zusätzliche Latenz von 5 bis 10 Minuten in Adobe Analytics wahrnehmen. Diese Steigerung der Latenz ermöglicht die Speicherung von Daten aus Analytics und Target für den gleichen Treffer, sodass Sie Tests nach Seite und Site-Abschnitt aufschlüsseln können.

Diese Steigerung spiegelt sich in sämtlichen Services und Tools von Adobe Analytics wider, einschließlich Live-Stream und Echtzeit-Berichterstattung, und gilt für folgende Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, endgültige Daten und Datenfeeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Achten Sie darauf, dass die Erhöhung der Latenz nach der Implementierung des Experience Cloud-Besucher-ID-Services beginnt, auch wenn Sie diese Integration nicht vollständig implementiert haben.

## Zusätzliche ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

Zu allen Target-Aufrufen, die von einer A4T-Aktivität zur Übermittlung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, muss es einen zugehörigen Analytics-Treffer geben, der die gleiche Zusatz-ID hat, damit A4T ordnungsgemäß funktioniert.

Treffer, die Daten aus Analytics und Target enthalten, enthalten eine zusätzliche Daten-ID. Sie können diese ID im [Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=debugger) als `sdid`-Parameter ansehen. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.
* Eine Version von [!DNL mbox.js], die diese Integration unterstützt, wurde implementiert.

Stellen Sie bei der Fehlerbehebung sicher, dass die zusätzliche ID bei Analytics-Treffern vorhanden ist.

## Client-side Analytics logging {#client-side}

By default, when at.js, the [!DNL Experience Cloud Visitor ID Service], and appMeasurement.js are on the page, [!DNL Adobe Analytics] and [!DNL Target] correctly stitch events for reporting and analytics purposes in the backend as long as the correct supplemental ID is included from the page, as mentioned above. Sie müssen keine weiteren Vorgänge für A 4 T verwalten und durchführen, damit sie ordnungsgemäß funktionieren.

However, there are cases when you might want to have more control on when and how to send analytics data related to [!DNL Target] to [!DNL Analytics] for reporting purposes. You might have an in-house analytics tool that you leverage for internal purposes but also want to send the analytics data to [!DNL Analytics] via your in-house analytics product so that other members of your organization can continue to utilize [!DNL Analytics] as a visual reporting source. See [Step 7: Reference at.js or mbox.js on all site pages](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics for Target Implementation* for more information.
