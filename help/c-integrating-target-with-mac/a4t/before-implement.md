---
keywords: Recommendations
description: Bei Ihrem Datenerfassungsprozess treten verschiedene Änderungen auf, wenn Sie Analytics als Berichtsquelle für Target (A4T) verwenden.
title: Vor der Implementierung von Adobe Analytics als Berichte-Quelle für Adobe Target (A4T)
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 52%

---


# Vor der Implementierung{#before-you-implement}

Bei der Datenerfassung treten mehrere Änderungen auf, wenn [!DNL Analytics] als Berichte-Quelle für [!DNL Target] (A4T) aktiviert wird.

Bevor Sie sich für die Verwendung dieser Integration entscheiden, überprüfen Sie folgende Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Berichtsprozesse:

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie A4T verwenden können, müssen Sie eine Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie das Provisioning-Formular [Marketing Cloud-Integrationen](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.

Für diese A4T-Integration müssen Sie in Abhängigkeit davon, ob Sie Weiterleitungsangebote in A4T verwenden möchten oder nicht, die folgenden Bibliotheksversionen (oder neuere) implementieren:

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 1.8.0
* [!DNL Adobe Target] (je nach Implementierung): at.js, Version 0.9.1 oder mbox.js, Version 61
* Adobe Analytics: appMeasurement.js, Version 1.7.0

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 2.3.0
* [!DNL Adobe Target]: at.js, Version 1.6.2

   **Hinweis:** Die mbox.js-Bibliothek unterstützt keine Weiterleitungsangebote mit A4T. Ihre Implementierung muss at.js verwenden.

* Adobe Analytics: appMeasurement.js, Version 2.1

Download- und Bereitstellungsanweisungen finden Sie unter [Analytics for Zielgruppe Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* Diese Integration ist auf neuen Aktivitäten aktiviert, wenn Sie [!DNL Analytics] als Berichte-Quelle auswählen. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* Das Einrichten von [!DNL Analytics] als Berichte-Quelle für [!DNL Target] umfasst mehrere Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nachdem Sie diese Schritte ausgeführt haben, können Sie [!DNL Analytics] als Berichte-Quelle verwenden, sobald diese für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Das [!DNL Visitor ID service] erstellt ein freigegebenes [!DNL Visitor ID] über das [!DNL Adobe Experience Cloud]. Obwohl die UUID [!DNL Target] &quot;mboxPC-ID&quot;oder [!DNL Audience Manager] nicht ersetzt wird, ersetzt sie die Art und Weise, wie [!DNL Analytics] neue Besucher identifiziert. Bei ordnungsgemäßer Einrichtung sollten die zurückgegebenen [!DNL Analytics]-Besucher auch über ihre alte [!DNL Analytics]-ID identifiziert werden, um das Cliffen von Besuchern zu verhindern. Da die [!DNL Target]-mboxPCid intakt bleibt, gehen beim Upgrade auf [!DNL Visitor ID service] keine [!DNL Target]-Profil-Daten des Besuchers verloren.
* Das [!DNL Visitor ID service] muss vor dem [!DNL Analytics]- und [!DNL Target]-Seitencode ausgeführt werden. Stellen Sie sicher, dass `VisitorAPI.js` für alle anderen [!DNL Experience Cloud]-Lösungen über den -Tags angezeigt wird.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nach Aktivierung dieser Integration wird eine zusätzliche Latenz von 5-10 Minuten in [!DNL Analytics] angezeigt. Durch diese Erhöhung der Latenz können Daten von [!DNL Analytics] und [!DNL Target] im selben Treffer gespeichert werden, sodass Sie Aktivitäten nach Seite und Site-Abschnitt unterteilen können.

Diese Steigerung spiegelt sich in allen [!DNL Analytics]-Diensten und -Tools einschließlich Live-Stream- und Echtzeit-Berichte wider und gilt für die folgenden Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, endgültige Daten und Datenfeeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Beachten Sie, dass die Latenz die Beginn nach der Implementierung des Besucher-ID-Diensts [!DNL Experience Cloud] erhöht, auch wenn Sie diese Integration nicht vollständig implementiert haben.

## Zusätzliche ID   {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target]-Aufrufe, die von einer A4T-Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, müssen einen entsprechenden [!DNL Analytics]-Treffer haben, der dieselbe zusätzliche ID aufweist, damit A4T ordnungsgemäß funktioniert.

Treffer, die Daten von [!DNL Analytics] und [!DNL Target] enthalten, enthalten eine zusätzliche Daten-ID. Diese ID wird im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als `sdid`-Parameter angezeigt. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.
* Eine Version von [!DNL mbox.js], die diese Integration unterstützt, wurde implementiert.

Stellen Sie bei [Fehlerbehebung](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) sicher, dass die zusätzliche ID bei [!DNL Analytics]-Treffern vorhanden ist.

## Clientseitige Analytics-Protokollierung {#client-side}

Wenn sich at.js, die [!DNL Experience Cloud Visitor ID Service] und appMeasurement.js auf der Seite befinden, verknüpfen [!DNL Analytics]und [!DNL Target] standardmäßig Ereignisse für Reporting- und Analysezwecke im Backend, sofern die korrekte zusätzliche ID von der Seite wie oben erläutert einbezogen wird. Sie müssen keine weiteren Vorgänge für A4T verwalten und durchführen, damit sie ordnungsgemäß funktionieren.

In manchen Fällen könnten Sie aber mehr Kontrolle darüber haben wollen, wann und wie Analysedaten in Verbindung mit [!DNL Target] zu Berichtszwecken an [!DNL Analytics] gesendet werden sollen. Möglicherweise verfügen Sie über ein unternehmensinternes Analysetool, das Sie für interne Zwecke nutzen, und möchten auch die Analysedaten an [!DNL Analytics] über Ihr internes Analyseprodukt senden, damit andere Mitarbeiter weiterhin [!DNL Analytics] als visuelle Berichtsquelle nutzen können. Weitere Informationen finden Sie unter [Schritt 7: Verweisen auf at.js oder mbox.js auf allen Seiten der Website](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementieren von Analytics for Target*.

## Freigegebene Zielgruppen

Beachten Sie beim Ausfüllen des Bereitstellungsformulars für [Marketing Cloud-Integrationen die folgenden wichtigen Informationen bezüglich der Option [!UICONTROL Freigegebene Audiencen], die unter &quot;[!UICONTROL Für welche Funktionen fordern Sie Bereitstellung]?&quot;aufgeführt ist.](https://www.adobe.com/go/audiences)

![Anforderungsformular](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wenn Sie [!UICONTROL Freigegebene Audiencen] anfordern, aktivieren Sie [!UICONTROL Zielgruppe] und [!UICONTROL Adobe Audience Manager] (AAM), um Informationen freizugeben, in diesem Fall Audiencen.

>[!IMPORTANT]
>
>Diese Integration zwischen [!UICONTROL Zielgruppe] und AAM ist mit zusätzlichen Kosten verbunden. Sie werden für jeden [!UICONTROL Zielgruppe]-Aufruf in AAM in Rechnung gestellt.
