---
keywords: Recommendations
description: Erfahren Sie mehr über die Implementierungsanforderungen für Analytics für [!DNL Target] (A4T) und was Sie beachten sollten, bevor Sie diese Integration implementieren.
title: Was sollte ich vor der Implementierung von A4T wissen?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 30%

---

# Vor der Implementierung von Analytics for Target (A4T) mit at.js

Beim Aktivieren von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T).

Bevor Sie sich für die Verwendung dieser Integration entscheiden, überprüfen Sie folgende Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Berichtsprozesse.

>[!NOTE]
>
>Dieser Artikel gilt nur für at.js-Implementierungen.

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie mit der Verwendung von A4T beginnen können, müssen Sie die Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie die [Bereitstellungsformular für Marketing Cloud-Integrationen](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} , um die Bereitstellung anzufordern.

Für diese A4T-Integration müssen Sie in Abhängigkeit davon, ob Sie Weiterleitungsangebote in A4T verwenden möchten oder nicht, die folgenden Bibliotheksversionen (oder neuere) implementieren.

>[!NOTE]
>
>Die folgenden Anforderungen enthalten die *Minimum* Versionen von at.js, die zur Implementierung von A4T erforderlich sind. Die [!DNL Target] Team verwaltet nur zwei Versionen von [!DNL at.js]- die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 1.8.0
* [!DNL Adobe Target]: at.js, Version 0.9.1
* Adobe Analytics: appMeasurement.js, Version 1.7.0

Informationen zur Implementierung von A4T mit dem [!DNL Platform Web SDK], siehe [Adobe Experience Platform Web SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 2.3.0

   >[!NOTE]
   >
   >at.js 1.8.0 und höher und at.js 2.x und höher funktionieren nicht mehr mit Visitor API-Versionen älter als 2.5.0 im Hinblick auf die Übergabe von Adobe Audience Manager (AAM)-Parametern.

* [!DNL Adobe Target]: at.js, Version 1.6.2

* Adobe Analytics: appMeasurement.js, Version 2.1

Download- und Bereitstellungsanweisungen finden Sie unter [Implementierung von Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Informationen zur Implementierung von A4T mit dem [!DNL Platform Web SDK], siehe [Adobe Experience Platform Web SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* Diese Integration wird für neue Aktivitäten aktiviert, wenn Sie die Verwendung von [!DNL Analytics] als Berichtsquelle. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* Der Prozess der Einrichtung [!DNL Analytics] als Berichtsquelle für [!DNL Target] umfasst mehrere Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nachdem Sie diese Schritte ausgeführt haben, können Sie [!DNL Analytics] als Berichtsquelle, wenn sie für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Die [!DNL Visitor ID service] erstellt eine freigegebene [!DNL Visitor ID] über [!DNL Adobe Experience Cloud]. Obwohl die Variable [!DNL Target] mboxPC-ID oder [!DNL Audience Manager] UUID ersetzt die Methode [!DNL Analytics] identifiziert neue Besucher. Bei ordnungsgemäßer Einrichtung wird [!DNL Analytics] Besucher sollten auch über ihre alten [!DNL Analytics] Kennung. Gleichermaßen, weil die [!DNL Target] mboxPCid bleibt intakt, nein [!DNL Target] Besucherprofildaten gehen bei der Aktualisierung auf [!DNL Visitor ID service].
* Die [!DNL Visitor ID service] muss vor dem [!DNL Analytics] und [!DNL Target] Seiten-Code. Stellen Sie sicher, dass `VisitorAPI.js` oberhalb der Tags für alle anderen [!DNL Experience Cloud] Lösungen.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nach Aktivierung dieser Integration wird eine zusätzliche Latenz von 5 bis 10 Minuten in [!DNL Analytics]. Diese Steigerung der Latenz ermöglicht Daten aus [!DNL Analytics] und [!DNL Target] werden, damit Sie Aktivitäten nach Seite und Site-Abschnitt aufschlüsseln können.

Diese Zunahme spiegelt sich in allen [!DNL Analytics] Dienste und Tools, einschließlich der Livestream- und Echtzeitberichterstellung, und gilt in den folgenden Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, finalisierten Daten und Daten-Feeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Die Erhöhung der Latenz beginnt nach der Implementierung der [!DNL Experience Cloud] Besucher-ID-Service, auch wenn Sie diese Integration nicht vollständig implementiert haben.

## Zusätzliche ID  {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] -Aufrufe, die von einer A4T-Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, müssen über eine entsprechende [!DNL Analytics] Treffer, der die zusätzliche ID für A4T nutzt, um ordnungsgemäß zu funktionieren.

Treffer, die Daten aus [!DNL Analytics] und [!DNL Target] enthalten eine zusätzliche Daten-ID. Diese ID finden Sie in der [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als `sdid` Parameter. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.

Wann [Fehlerbehebung](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)müssen Sie sicherstellen, dass die zusätzliche ID in [!DNL Analytics] Treffer.

## Clientseitige Analytics-Protokollierung {#client-side}

Wenn at.js, wird die [!DNL Experience Cloud Visitor ID Service]und appMeasurement.js auf der Seite stehen, [!DNL Analytics]und [!DNL Target] ordnet Ereignisse für Berichterstellungs- und Analysezwecke im Backend korrekt zu, sofern die richtige zusätzliche ID von der Seite einbezogen wird. Sie müssen keine zusätzlichen Vorgänge verwalten und durchführen, damit A4T ordnungsgemäß funktioniert.

Es gibt Fälle, in denen Sie mehr Kontrolle darüber haben möchten, wann und wie Analysedaten im Zusammenhang mit [!DNL Target] nach [!DNL Analytics] für Berichtszwecke. Möglicherweise verfügen Sie über ein internes Analysetool, das Sie für interne Zwecke verwenden. Sie möchten die Analysedaten jedoch auch an senden [!DNL Analytics] über Ihr internes Analyseprodukt, damit andere Mitglieder Ihres Unternehmens weiterhin [!DNL Analytics] als visuelle Berichtsquelle. Siehe [Schritt 7: Verweisen auf at.js auf allen Seiten der Site](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementierung von Analytics for Target* für weitere Informationen.

## Freigegebene Zielgruppen

Beim Füllen der [Bereitstellungsformular für Marketing Cloud-Integrationen](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}sind sich der folgenden wichtigen Informationen bezüglich der [!UICONTROL Freigegebene Zielgruppen] Option aufgeführt unter[!UICONTROL Für welche Funktionen fordern Sie Bereitstellung an]?&quot;

![Anforderungsformular](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Bei Anforderung [!UICONTROL Freigegebene Zielgruppen], aktivieren Sie [!UICONTROL Target] und [!UICONTROL Adobe Audience Manager] (AAM) zum Austausch von Informationen, in diesem Fall Zielgruppen.

>[!IMPORTANT]
>
>Diese Integration zwischen [!UICONTROL Target] und AAM sind mit zusätzlichen Kosten verbunden. Sie werden für jede [!UICONTROL Target] -Aufruf in AAM.
