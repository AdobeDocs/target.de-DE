---
keywords: Recommendations
description: Erfahren Sie mehr über die Implementierungsanforderungen für Analytics for [!DNL Target]  (A4T) und was Sie beachten müssen, bevor Sie diese Integration implementieren.
title: Was sollte ich vor der Implementierung von A4T wissen?
feature: 'Analytics for Target (A4T) '
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 4c696f55f56a116cff61c2c307f750e72cc0107c
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 31%

---

# Vor der Implementierung von Analytics for Target (A4T) mit at.js

Bei der Aktivierung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) im Datenerfassungsprozess treten verschiedene Änderungen auf.

Bevor Sie sich für die Verwendung dieser Integration entscheiden, überprüfen Sie folgende Abschnitte und berücksichtigen Sie die Auswirkungen auf Ihre Berichtsprozesse.

>[!NOTE]
>
>Dieser Artikel gilt nur für at.js-Implementierungen.

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie mit der Verwendung von A4T beginnen können, müssen Sie die Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie das [Marketing Cloud Integrations Provisioning-Formular](https://www.adobe.com/go/audiences), um die Bereitstellung anzufordern.

Für diese A4T-Integration müssen Sie in Abhängigkeit davon, ob Sie Weiterleitungsangebote in A4T verwenden möchten oder nicht, die folgenden Bibliotheksversionen (oder neuere) implementieren:

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 1.8.0
* [!DNL Adobe Target] (je nach Implementierung): at.js, Version 0.9.1 oder mbox.js, Version 61
* Adobe Analytics: appMeasurement.js, Version 1.7.0

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 2.3.0

   **Hinweis:**  at.js 1.8.0 oder höher funktioniert nicht mehr mit Visitor API-Versionen älter als 2.5.0 für die Übergabe von  [!DNL Adobe Audience Manager] (AAM) Parametern.

* [!DNL Adobe Target]: at.js, Version 1.6.2

   **Hinweis**: Die mbox.js-Bibliothek unterstützt keine Umleitungsangebote mit A4T. Ihre Implementierung muss at.js verwenden.

* Adobe Analytics: appMeasurement.js, Version 2.1

Download- und Bereitstellungsanweisungen finden Sie unter [Analytics for Target-Implementierung](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* Diese Integration ist für neue Aktivitäten aktiviert, wenn Sie [!DNL Analytics] als Berichtsquelle auswählen. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* Der Prozess der Einrichtung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] umfasst mehrere Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nachdem Sie diese Schritte ausgeführt haben, können Sie [!DNL Analytics] als Berichtsquelle verwenden, wenn diese für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Der [!DNL Visitor ID service] erstellt eine freigegebene [!DNL Visitor ID] für [!DNL Adobe Experience Cloud]. Obwohl die [!DNL Target]-mboxPC-ID oder die [!DNL Audience Manager]-UUID nicht ersetzt wird, ersetzt sie die Methode, mit der [!DNL Analytics] neue Besucher identifiziert. Bei ordnungsgemäßer Einrichtung sollten wiederkehrende [!DNL Analytics] -Besucher auch über ihre alte [!DNL Analytics] -ID identifiziert werden. Da die [!DNL Target]-mboxPCid intakt bleibt, gehen beim Upgrade auf [!DNL Visitor ID service] keine [!DNL Target]-Besucherprofildaten verloren.
* Der [!DNL Visitor ID service] muss vor Ihrem [!DNL Analytics]- und [!DNL Target]-Seiten-Code ausgeführt werden. Stellen Sie sicher, dass `VisitorAPI.js` über den Tags für alle anderen [!DNL Experience Cloud]-Lösungen angezeigt wird.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nachdem diese Integration aktiviert wurde, tritt eine zusätzliche Latenz von 5 bis 10 Minuten in [!DNL Analytics] auf. Diese Steigerung der Latenz ermöglicht die Speicherung von Daten aus [!DNL Analytics] und [!DNL Target] im selben Treffer, sodass Sie Aktivitäten nach Seite und Website-Abschnitt aufschlüsseln können.

Diese Steigerung spiegelt sich in allen [!DNL Analytics]-Diensten und -Tools wider, einschließlich der Live-Stream- und Echtzeitberichterstellung, und gilt in den folgenden Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, finalisierten Daten und Daten-Feeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Die Erhöhung der Latenz beginnt, nachdem Sie den Besucher-ID-Dienst [!DNL Experience Cloud] implementiert haben, auch wenn Sie diese Integration nicht vollständig implementiert haben.

## Zusätzliche ID  {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target]-Aufrufe, die von einer A4T-Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, müssen einen entsprechenden [!DNL Analytics]-Treffer aufweisen, der die zusätzliche ID teilt, damit A4T ordnungsgemäß funktioniert.

Treffer, die Daten von [!DNL Analytics] und [!DNL Target] enthalten, enthalten eine zusätzliche Daten-ID. Sie können diese ID im [Adobe Experience Cloud-Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als den Parameter `sdid` sehen. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.
* Eine Version von [!DNL mbox.js], die diese Integration unterstützt, wurde implementiert.

Stellen Sie bei [Fehlerbehebung](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) sicher, dass die zusätzliche ID bei [!DNL Analytics]-Treffern vorhanden ist.

## Clientseitige Analytics-Protokollierung {#client-side}

Wenn sich at.js, [!DNL Experience Cloud Visitor ID Service] und appMeasurement.js auf der Seite befinden, werden die Ereignisse [!DNL Analytics] und [!DNL Target] im Backend korrekt für Berichterstellungs- und Analysezwecke zugeordnet, sofern die richtige zusätzliche ID auf der Seite enthalten ist. Sie müssen keine zusätzlichen Vorgänge verwalten und durchführen, damit A4T ordnungsgemäß funktioniert.

Es gibt Fälle, in denen Sie möglicherweise mehr Kontrolle darüber haben möchten, wann und wie Analysedaten zu [!DNL Target] zu [!DNL Analytics] zu Berichtszwecken an  gesendet werden. Möglicherweise verfügen Sie über ein internes Analysetool, das Sie für interne Zwecke verwenden. Sie möchten die Analysedaten jedoch auch über Ihr internes Analyseprodukt an [!DNL Analytics] senden, damit andere Mitglieder Ihres Unternehmens [!DNL Analytics] weiterhin als visuelle Berichtsquelle verwenden können. Weitere Informationen finden Sie unter [Schritt 7: Verweisen auf at.js oder mbox.js auf allen Seiten der Website](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementieren von Analytics for Target*.

## Freigegebene Zielgruppen

Beachten Sie beim Ausfüllen des [Marketing Cloud Integrations Provisioning-Formulars](https://www.adobe.com/go/audiences) die folgenden wichtigen Informationen zur Option [!UICONTROL Freigegebene Zielgruppen], die unter &quot;[!UICONTROL Für welche Funktionen fordern Sie die Bereitstellung]?&quot;aufgeführt sind.

![Anforderungsformular](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wenn Sie [!UICONTROL Freigegebene Zielgruppen] anfordern, aktivieren Sie [!UICONTROL Target] und [!UICONTROL Adobe Audience Manager] (AAM), um Informationen, in diesem Fall Zielgruppen, freizugeben.

>[!IMPORTANT]
>
>Diese Integration zwischen [!UICONTROL Target] und AAM führt zu zusätzlichen Kosten. Sie werden für jeden [!UICONTROL Target]-Aufruf in AAM in Rechnung gestellt.
