---
keywords: Recommendations
description: Erfahren Sie mehr über die Implementierungsanforderungen für Analytics  [!DNL Target] A4T) und darüber, was Sie vor der Implementierung dieser Integration beachten sollten.
title: Was sollte ich vor der Implementierung von A4T wissen?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 656f728ba890f1f5afc0404e22f6acb1a2565fe6
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 24%

---

# Vor der Implementierung von Analytics for Target (A4T) mit at.js

Beim Aktivieren von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) treten im Datenerfassungsprozess mehrere Änderungen auf.

Bevor Sie sich für diese Integration entscheiden, lesen Sie die folgenden Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Reporting-Prozesse.

>[!NOTE]
>
>Dieser Artikel gilt nur für at.js-Implementierungen. Informationen zur Implementierung von [!UICONTROL Analytics for Target] (A4T) mit dem [!DNL Adobe Experience Platform Web SDK] finden Sie unter [Protokollierung von Adobe Analytics for Target (A4T) in der Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/a4t/overview-a4t.html?lang=de){target=_blank}.

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie mit der Verwendung von A4T beginnen können, müssen Sie anfordern, dass Ihr Konto für die Integration bereitgestellt wird. Verwenden Sie das Bereitstellungsformular für [Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}Integrationen, um die Bereitstellung anzufordern.

Diese A4T-Integration erfordert die Implementierung der folgenden Bibliotheksversionen (oder neuer), je nachdem, ob Umleitungsangebote mit A4T verwendet werden sollen oder nicht.

>[!NOTE]
>
>In den folgenden Anforderungen sind die (*)* Versionen von at.js aufgeführt, die für die Implementierung von A4T erforderlich sind. Das [!DNL Target]-Team verwaltet nur zwei Versionen von [!DNL at.js] - die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen in den einzelnen Versionen finden Sie unter [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 1.8.0
* [!DNL Adobe Target]: at.js-Version 0.9.1
* Adobe Analytics: appMeasurement.js, Version 1.7.0

Informationen zur Implementierung von A4T mit dem [!DNL Platform Web SDK] finden Sie unter [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 2.3.0

  >[!NOTE]
  >
  >at.js 1.8.0 und höher und at.js 2.x und höher funktionieren nicht mehr mit Visitor API-Versionen älter als 2.5.0 im Hinblick auf die Übergabe von Adobe Audience Manager (AAM)-Parametern.

* [!DNL Adobe Target]: at.js-Version 1.6.2

* Adobe Analytics: appMeasurement.js, Version 2.1

Anweisungen zum Herunterladen und Bereitstellen finden Sie unter [Analytics for Target-Implementierung](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Informationen zur Implementierung von A4T mit dem [!DNL Platform Web SDK] finden Sie unter [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* Diese Integration wird für neue Aktivitäten aktiviert, wenn Sie [!DNL Analytics] als Berichtsquelle verwenden. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* Der Prozess zum Einrichten von [!DNL Analytics] als Berichtsquelle für [!DNL Target] umfasst mehrere Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nachdem Sie diese Schritte abgeschlossen haben, können Sie [!DNL Analytics] als Berichtsquelle verwenden, wenn es für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Der [!DNL Visitor ID service] erstellt eine gemeinsame [!DNL Visitor ID] für die [!DNL Adobe Experience Cloud]. Die [!DNL Target] mboxPC-ID oder [!DNL Audience Manager] UUID wird zwar nicht ersetzt, aber die Art und Weise, wie [!DNL Analytics] neue Besucher identifiziert. Bei ordnungsgemäßer Einrichtung sollten wiederkehrende [!DNL Analytics] auch über ihre alte [!DNL Analytics]-ID identifiziert werden. Da die [!DNL Target] mboxPCid intakt bleibt, gehen beim Upgrade auf die [!DNL Target] auch keine [!DNL Visitor ID service] Besucherprofildaten verloren.
* Der [!DNL Visitor ID service] muss vor dem [!DNL Analytics] und [!DNL Target] Seiten-Code ausgeführt werden. Stellen Sie sicher, dass für alle anderen `VisitorAPI.js`-Lösungen [!DNL Experience Cloud] über den Tags angezeigt wird.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nach Aktivierung dieser Integration tritt in [!DNL Analytics] eine zusätzliche Latenz von 5-10 Minuten auf. Durch diese Latenzerhöhung können Daten aus [!DNL Analytics] und [!DNL Target] im selben Treffer gespeichert werden, sodass Sie Aktivitäten nach Seite und Site-Bereich aufschlüsseln können.

Dieser Anstieg spiegelt sich in allen [!DNL Analytics] Services und Tools wider, einschließlich Live-Stream- und Echtzeit-Reporting, und gilt in den folgenden Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Bei aktuellen Daten zu Konversionsmetriken, finalisierten Daten und Daten-Feeds werden alle Treffer um zusätzliche 5-7 Minuten verzögert.

Die Latenzsteigerung beginnt nach der Implementierung des [!DNL Experience Cloud] Besucher-ID-Service, auch wenn diese Integration noch nicht vollständig implementiert wurde.

## Zusätzliche ID  {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] Aufrufe, die von einer A4T-Aktivität zum Bereitstellen von Inhalten oder Aufzeichnen der Zielmetrik verwendet werden, müssen einen entsprechenden [!DNL Analytics]-Treffer aufweisen, der die zusätzliche ID teilt, damit A4T ordnungsgemäß funktioniert.

Treffer, die Daten aus [!DNL Analytics] und [!DNL Target] enthalten, enthalten eine zusätzliche Daten-ID. Diese ID wird im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de) als `sdid` angezeigt. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.

Stellen [&#x200B; bei &#x200B;](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)Fehlerbehebung) sicher, dass die zusätzliche ID bei [!DNL Analytics] Treffern vorhanden ist.

## Client-seitige Analytics-Protokollierung {#client-side}

Wenn sich at.js, die [!DNL Experience Cloud Visitor ID Service] und appMeasurement.js auf der Seite befinden, [!DNL Analytics] und ordnet [!DNL Target] Ereignisse für Reporting- und Analysezwecke im Backend korrekt zu, solange die richtige zusätzliche ID von der Seite enthalten ist. Sie müssen keine zusätzlichen Vorgänge verwalten und durchführen, damit A4T ordnungsgemäß funktioniert.

Es gibt Fälle, in denen Sie mehr Kontrolle darüber wünschen, wann und wie Sie Analysedaten zu [!DNL Target] zu Berichtszwecken an [!DNL Analytics] senden. Möglicherweise verfügen Sie über ein internes Analysetool, das Sie für interne Zwecke verwenden. Sie möchten jedoch auch die Analysedaten über Ihr internes Analyseprodukt an [!DNL Analytics] senden, damit andere Mitglieder Ihrer Organisation [!DNL Analytics] weiterhin als visuelle Berichtsquelle verwenden können. Weitere Informationen finden Sie [Schritt 7: Referenzieren von at.js auf allen &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7)-Seiten *unter Analytics for Target-*).

## Freigegebene Zielgruppen

Beachten Sie beim Ausfüllen des Bereitstellungsformulars für [Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}Integrationen die folgenden wichtigen Informationen zur [!UICONTROL Shared Audiences], die unter &quot;[!UICONTROL For which capabilities are you requesting provisioning]?“ aufgeführt sind

![Anfrageformular](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wenn Sie [!UICONTROL Shared Audiences] anfordern, aktivieren Sie [!UICONTROL Target] und [!UICONTROL Adobe Audience Manager] (AAM), um Informationen, in diesem Fall Zielgruppen, auszutauschen.

>[!IMPORTANT]
>
>Diese Integration zwischen [!UICONTROL Target] und AAM verursacht zusätzliche Kosten. In AAM werden Sie für jeden [!UICONTROL Target]-Aufruf in Rechnung gestellt.
