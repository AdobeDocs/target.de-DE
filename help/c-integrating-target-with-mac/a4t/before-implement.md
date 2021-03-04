---
keywords: Recommendations
description: Erfahren Sie mehr über die Implementierungsanforderungen für Analytics for Zielgruppe (A4T) und was Sie beachten sollten, bevor Sie diese Integration implementieren.
title: Was sollte ich vor der Implementierung von A4T wissen?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4abf975095c5e29eea42d67119a426a3922d8d79
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 34%

---


# Vor der Implementierung{#before-you-implement}

Bei der Datenerfassung treten mehrere Änderungen auf, wenn [!DNL Adobe Analytics] als Berichte-Quelle für [!DNL Adobe Target] (A4T) aktiviert wird.

Bevor Sie sich für die Verwendung dieser Integration entscheiden, überprüfen Sie folgende Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Berichtsprozesse:

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie mit der Verwendung von A4T beginnen können, müssen Sie die Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie das Provisioning-Formular [Marketing Cloud-Integrationen](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.

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
* Das Einrichten von [!DNL Analytics] als Berichte-Quelle für [!DNL Target] umfasst mehrere Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nachdem Sie diese Schritte ausgeführt haben, können Sie [!DNL Analytics] als Berichte-Quelle verwenden, wenn sie für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Das [!DNL Visitor ID service] erstellt ein freigegebenes [!DNL Visitor ID] über das [!DNL Adobe Experience Cloud]. Obwohl die UUID [!DNL Target] &quot;mboxPC-ID&quot;oder [!DNL Audience Manager] nicht ersetzt wird, ersetzt sie die Art und Weise, wie [!DNL Analytics] neue Besucher identifiziert. Bei ordnungsgemäßer Einrichtung sollten zurückgegebene [!DNL Analytics]-Besucher auch mit ihrer alten [!DNL Analytics]-ID identifiziert werden. Da die [!DNL Target]-mboxPCid intakt bleibt, gehen beim Upgrade auf [!DNL Visitor ID service] keine [!DNL Target]-Profil-Daten des Besuchers verloren.
* Das [!DNL Visitor ID service] muss vor dem [!DNL Analytics]- und [!DNL Target]-Seitencode ausgeführt werden. Stellen Sie sicher, dass `VisitorAPI.js` für alle anderen [!DNL Experience Cloud]-Lösungen über den -Tags angezeigt wird.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nach Aktivierung dieser Integration wird eine zusätzliche Latenz von 5-10 Minuten in [!DNL Analytics] angezeigt. Durch diese Erhöhung der Latenz können Daten von [!DNL Analytics] und [!DNL Target] im selben Treffer gespeichert werden, sodass Sie Aktivitäten nach Seite und Site-Abschnitt unterteilen können.

Diese Steigerung spiegelt sich in allen [!DNL Analytics]-Diensten und -Tools einschließlich Live-Stream- und Echtzeit-Berichte wider und gilt für die folgenden Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Bei aktuellen Daten zu Konversionsmetriken, finalisierten Daten und Datenfeeds werden alle Treffer um weitere 5-7 Minuten verzögert.

Die Latenz erhöht die Beginn, nachdem Sie den [!DNL Experience Cloud]-Besucher-ID-Dienst implementiert haben, auch wenn Sie diese Integration noch nicht vollständig implementiert haben.

## Zusätzliche ID   {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target]-Aufrufe, die von einer A4T-Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, müssen einen entsprechenden [!DNL Analytics]-Treffer haben, der die zusätzliche ID teilt, damit A4T ordnungsgemäß funktioniert.

Treffer, die Daten von [!DNL Analytics] und [!DNL Target] enthalten, enthalten eine zusätzliche Daten-ID. Diese ID wird im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als `sdid`-Parameter angezeigt. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.
* Eine Version von [!DNL mbox.js], die diese Integration unterstützt, wurde implementiert.

Stellen Sie bei [Fehlerbehebung](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) sicher, dass die zusätzliche ID bei [!DNL Analytics]-Treffern vorhanden ist.

## Clientseitige Analytics-Protokollierung {#client-side}

Wenn sich at.js, [!DNL Experience Cloud Visitor ID Service] und appMeasurement.js auf der Seite befinden, [!DNL Analytics] und [!DNL Target] Ereignis für Berichte- und Analysezwecke korrekt im Backend zusammenfügen, solange die richtige zusätzliche ID auf der Seite enthalten ist. Sie müssen keine zusätzlichen Vorgänge verwalten und durchführen, damit A4T ordnungsgemäß funktioniert.

Es gibt Fälle, in denen Sie möglicherweise mehr Kontrolle darüber haben möchten, wann und wie Analysedaten zu [!DNL Target] zu Berichten an [!DNL Analytics] gesendet werden. Möglicherweise verfügen Sie über ein internes Analysetool, das Sie für interne Zwecke verwenden. Sie möchten die Analysedaten jedoch auch über Ihr internes Analyseprodukt an [!DNL Analytics] senden, damit andere Mitarbeiter Ihres Unternehmens [!DNL Analytics] weiterhin als visuelle Berichte verwenden können. Weitere Informationen finden Sie unter [Schritt 7: Verweisen auf at.js oder mbox.js auf allen Seiten der Website](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementieren von Analytics for Target*.

## Freigegebene Zielgruppen

Beachten Sie beim Ausfüllen des Bereitstellungsformulars für [Marketing Cloud-Integrationen die folgenden wichtigen Informationen bezüglich der Option [!UICONTROL Freigegebene Audiencen], die unter &quot;[!UICONTROL Für welche Funktionen fordern Sie Bereitstellung]?&quot;aufgeführt ist.](https://www.adobe.com/go/audiences)

![Anforderungsformular](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wenn Sie [!UICONTROL Freigegebene Audiencen] anfordern, aktivieren Sie [!UICONTROL Zielgruppe] und [!UICONTROL Adobe Audience Manager] (AAM), um Informationen freizugeben, in diesem Fall Audiencen.

>[!IMPORTANT]
>
>Diese Integration zwischen [!UICONTROL Zielgruppe] und AAM ist mit zusätzlichen Kosten verbunden. Für jeden [!UICONTROL Zielgruppe]-Aufruf in AAM werden Gebühren erhoben.
