---
keywords: Recommendations
description: Erfahren Sie mehr über die Implementierungsanforderungen für Analytics für [!DNL Target]  (A4T) und darüber, was Sie beachten sollten, bevor Sie diese Integration implementieren.
title: Was sollte ich vor der Implementierung von A4T wissen?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 23%

---

# Vor der Implementierung von Analytics for Target (A4T) mit at.js

Bei der Aktivierung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) im Datenerfassungsprozess treten verschiedene Änderungen auf.

Bevor Sie sich für die Verwendung dieser Integration entscheiden, lesen Sie die folgenden Abschnitte und bedenken Sie die Auswirkungen auf Ihre Berichtsprozesse.

>[!NOTE]
>
>Dieser Artikel gilt nur für at.js-Implementierungen.

## Implementierungsanforderungen {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Bevor Sie mit der Verwendung von A4T beginnen können, müssen Sie die Bereitstellung Ihres Kontos für die Integration anfordern. Verwenden Sie das [Marketing Cloud Integrations Provisioning-Formular](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}, um die Bereitstellung anzufordern.

Für diese A4T-Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, je nachdem, ob Sie Umleitungsangebote mit A4T verwenden möchten oder nicht.

>[!NOTE]
>
>In den folgenden Anforderungen sind die *minimalen* Versionen von at.js aufgeführt, die zur Implementierung von A4T erforderlich sind. Das [!DNL Target]-Team verwaltet nur zwei Versionen von [!DNL at.js] - die aktuelle Version und die zweitneueste Version. Führen Sie bei Bedarf ein Upgrade von [!DNL at.js] durch, um sicherzustellen, dass Sie eine unterstützte Version ausführen. Weitere Informationen zu den Funktionen der einzelnen Versionen finden Sie unter [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.

### Anforderungen, wenn *keine* Umleitungsangebote mit A4T verwendet werden

Bei dieser Integration müssen Sie die folgenden Bibliotheksversionen (oder neuer) implementieren, wenn Sie nicht planen, Weiterleitungsangebote mit A4T zu verwenden. Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 1.8.0
* [!DNL Adobe Target]: at.js , Version 0.9.1
* Adobe Analytics: appMeasurement.js, Version 1.7.0

Informationen zur Implementierung von A4T mit dem [!DNL Platform Web SDK] finden Sie unter [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

### Anforderungen, wenn Umleitungsangebote mit A4T verwendet werden

Für die Verwendung von Weiterleitungsangeboten mit A4T müssen Sie die folgenden Bibliotheksversionen (oder neuere) implementieren: Die angezeigte Reihenfolge ist die Reihenfolge der Vorgänge.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js, Version 2.3.0

  >[!NOTE]
  >
  >at.js 1.8.0 und höher und at.js 2.x und höher funktionieren nicht mehr mit Visitor API-Versionen älter als 2.5.0 im Hinblick auf die Übergabe von Adobe Audience Manager (AAM)-Parametern.

* [!DNL Adobe Target]: at.js, Version 1.6.2

* Adobe Analytics: appMeasurement.js, Version 2.1

Download- und Bereitstellungsanweisungen finden Sie unter [Implementierung von Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Informationen zur Implementierung von A4T mit dem [!DNL Platform Web SDK] finden Sie unter [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=de){target=_blank}.

## Was Sie vor der Implementierung wissen sollten {#section_50D49CC52E11414089C89FB67F9B88F5}

* Diese Integration wird für neue Aktivitäten aktiviert, wenn Sie [!DNL Analytics] als Berichtsquelle auswählen. Ihre bestehenden Aktivitäten sind von den in diesem Dokument beschriebenen Implementierungsänderungen nicht betroffen.
* Der Prozess der Einrichtung von [!DNL Analytics] als Berichtsquelle für [!DNL Target] umfasst mehrere Implementierungsschritte, gefolgt von einem Bereitstellungsschritt. Es empfiehlt sich, vor der Implementierung die unten stehende Prozessbeschreibung durchzulesen. Nachdem Sie diese Schritte ausgeführt haben, können Sie [!DNL Analytics] als Berichtsquelle verwenden, wenn es für Sie aktiviert ist. Der Bereitstellungsprozess kann bis zu fünf Werktage dauern.
* Die [!DNL Visitor ID service] erstellt eine gemeinsame [!DNL Visitor ID] für die [!DNL Adobe Experience Cloud]. Obwohl sie die [!DNL Target] mboxPC-ID oder die [!DNL Audience Manager] UUID nicht ersetzt, ersetzt sie die Art und Weise, wie [!DNL Analytics] neue Besucher identifiziert. Bei ordnungsgemäßer Einrichtung sollten wiederkehrende [!DNL Analytics] Besucher auch über ihre alte [!DNL Analytics] -ID identifiziert werden. Da die mboxPCid [!DNL Target] intakt bleibt, gehen beim Upgrade auf die [!DNL Visitor ID service] auch keine [!DNL Target] Besucherprofildaten verloren.
* Die [!DNL Visitor ID service] muss vor Ihrem [!DNL Analytics] - und [!DNL Target] -Seiten-Code ausgeführt werden. Stellen Sie sicher, dass `VisitorAPI.js` über den Tags für alle anderen [!DNL Experience Cloud] -Lösungen angezeigt wird.

## Latenz {#section_9489BE6FD21641A4844E591711E3F813}

Nachdem diese Integration aktiviert wurde, tritt in [!DNL Analytics] eine zusätzliche Latenz von 5 bis 10 Minuten auf. Diese Steigerung der Latenz ermöglicht die Speicherung von Daten aus [!DNL Analytics] und [!DNL Target] für denselben Treffer, sodass Sie Aktivitäten nach Seite und Website-Abschnitt aufschlüsseln können.

Diese Steigerung spiegelt sich in allen [!DNL Analytics] -Diensten und -Tools wider, einschließlich der Live-Stream- und Echtzeitberichterstellung, und gilt in den folgenden Szenarien:

* Bei Livestream, Echtzeitberichten &amp; API-Anforderungen sowie aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Für aktuelle Daten zu Konversionsmetriken, finalisierten Daten und Daten-Feeds werden alle Treffer um zusätzliche 5 bis 7 Minuten verzögert.

Die Erhöhung der Latenz beginnt nach der Implementierung des Besucher-ID-Diensts [!DNL Experience Cloud] , auch wenn Sie diese Integration nicht vollständig implementiert haben.

## Zusätzliche ID  {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] -Aufrufe, die von einer A4T-Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, müssen einen entsprechenden [!DNL Analytics] -Treffer aufweisen, der die zusätzliche ID teilt, damit A4T ordnungsgemäß funktioniert.

Treffer, die Daten aus [!DNL Analytics] und [!DNL Target] enthalten, enthalten eine zusätzliche Daten-ID. Sie können diese ID im Parameter [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als den Parameter `sdid` sehen. Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Diese ID wird jedes Mal erstellt, wenn folgende Kriterien vorhanden sind:

* Der Besucher-ID-Service wurde implementiert.

Stellen Sie bei [Fehlerbehebung](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) sicher, dass die zusätzliche ID bei [!DNL Analytics] Treffern vorhanden ist.

## Clientseitige Analytics-Protokollierung {#client-side}

Wenn sich at.js, die [!DNL Experience Cloud Visitor ID Service] und die appMeasurement.js auf der Seite befinden, werden Ereignisse für Berichterstellungs- und Analysezwecke im Backend korrekt zugeordnet, sofern die richtige zusätzliche ID von der Seite einbezogen wird. [!DNL Analytics][!DNL Target] Sie müssen keine zusätzlichen Vorgänge verwalten und durchführen, damit A4T ordnungsgemäß funktioniert.

Es gibt Fälle, in denen Sie möglicherweise mehr Kontrolle darüber haben möchten, wann und wie Analysedaten im Zusammenhang mit [!DNL Target] an [!DNL Analytics] zu Berichtszwecken gesendet werden. Möglicherweise verfügen Sie über ein internes Analysetool, das Sie für interne Zwecke verwenden. Sie möchten die Analysedaten jedoch auch über Ihr internes Analyseprodukt an [!DNL Analytics] senden, damit andere Mitglieder Ihres Unternehmens [!DNL Analytics] weiterhin als visuelle Berichtsquelle verwenden können. Weitere Informationen finden Sie unter [Schritt 7: Verweisen auf at.js auf allen Seiten der Site](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics for Target-Implementierung* .

## Freigegebene Zielgruppen

Beachten Sie beim Ausfüllen des Formulars [Marketing Cloud Integrations Provisioning Form](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} die folgenden wichtigen Informationen bezüglich der Option [!UICONTROL Shared Audiences], die unter &quot;[!UICONTROL For which capabilities are you requesting provisioning]?&quot;aufgeführt ist.

![Anforderungsformular](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wenn Sie [!UICONTROL Shared Audiences] anfordern, aktivieren Sie [!UICONTROL Target] und [!UICONTROL Adobe Audience Manager] (AAM), um Informationen, in diesem Fall Zielgruppen, freizugeben.

>[!IMPORTANT]
>
>Diese Integration zwischen [!UICONTROL Target] und AAM führt zu zusätzlichen Kosten. Sie werden für jeden [!UICONTROL Target] -Aufruf in AAM in Rechnung gestellt.
