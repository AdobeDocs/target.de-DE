---
description: Sollten Sie eine ältere Version von „at.js“ oder „mbox.js“ verwenden, müssen Sie einen Trackingserver für Aktivitäten angeben, bei denen Analytics for Target (A4T) zum Einsatz kommt.
keywords: Analytics-Trackingserver; A4T; Adobe Experience Cloud-Debugger; Berichtsquelle
seo-description: Sollten Sie eine ältere Version von „at.js“ oder „mbox.js“ verwenden, müssen Sie einen Trackingserver für Aktivitäten angeben, bei denen Analytics for Target (A4T) zum Einsatz kommt.
seo-title: Verwenden eines Analytics-Trackingservers
title: Verwenden eines Analytics-Trackingservers
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 74a6f402bc0c9dae6f89cbdb632d7dbc53743593

---


# Verwenden eines Analytics-Trackingservers{#use-an-analytics-tracking-server}

Sollten Sie eine ältere Version von „at.js“ oder „mbox.js“ verwenden, müssen Sie einen Trackingserver für Aktivitäten angeben, bei denen Analytics for Target (A4T) zum Einsatz kommt.

>[!NOTE]
>
>Sollten Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität und bei der Verwendung von mbox.js Version 61 (oder neuer) oder at.js Version 0.9.1 (oder neuer) keinen Trackingserver angeben. Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

Damit gewährleistet werden kann, dass Daten aus Target in Analytics an die richtige Stelle übermittelt werden, ist für A4T ein Trackingserver erforderlich, mit dem Abfragen an Modstats in Target gesendet werden können. Für Implementierungen mit mehreren Trackingservern kann mit dem Adobe Experience Cloud-Debugger festgestellt werden, welcher der richtige Trackingserver für Ihre Aktivität ist.

Der Debugger sollte auf einer Seite angezeigt werden, auf der die Aktivität wiedergegeben werden soll, damit gewährleistet ist, dass der richtige Trackingserver ausgewählt wird. Alternativ kann für jedes Konto ein Standard-Trackingserver angegeben werden. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Standardeinstellung bearbeiten oder festlegen möchten.

1. Öffnen Sie auf der Seite, auf der Sie die Aktivität erstellen, den Adobe Experience Cloud-Debugger.

   Sollte der Debugger nicht installiert sein, folgen Sie den [Installationsanweisungen für den Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger_install.html).

   ![](assets/Screen_DebuggerTrackServ.png)

   Der Trackingserver findet sich im SiteCatalyst-Bildbereich des Debuggers. Das Feld trägt den Namen *Erstanbieter-Cookies* oder *Drittanbieter-Cookies*, abhängig von der Implementierung, und der Wert des Analytics-Trackingservers hat eines der folgenden Formate:

   * (für CNAME-Implementierungen)
   * (für Implementierungen ohne RDC)
   * (für RDC-Implementierung)
   *Company* steht für den Unternehmensnamen in Analytics, *metrics* ist ein Beispiel für einen CNAME-Wert und *d1* ist ein Beispiel für ein Analytics-Rechenzentrum.
1. Kopieren Sie den Inhalt des Felds vollständig.
1. Fügen Sie die Daten im Abschnitt zu [!UICONTROL Berichtseinstellungen] im Bildschirm „[!UICONTROL Ziele und Einstellungen]**“ in das Feld[!UICONTROL Trackingserver]** ein.

   >[!NOTE]
   >
   >Adobe Analytics muss als Berichtsquelle für die Aktivitäten eingestellt sein, anderenfalls ist das Trackingserverfeld nicht verfügbar.

