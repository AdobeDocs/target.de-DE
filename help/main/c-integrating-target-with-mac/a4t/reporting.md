---
keywords: Analytics for Target;A4T;Analytics als Berichtsquelle;Analytics
description: Erfahren Sie, wie Sie Analytics für  [!DNL Target] A4T) verwenden. A4T bietet Zugriff auf Analytics-Berichte für - [!DNL Target] , die Analytics-Metriken und Zielgruppensegmente verwenden.
title: Wie verwende ich Reporting in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 39%

---

# A4T-Reporting

Durch die Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) erhalten Sie Zugriff auf [!DNL Analytics] Berichte für Ihre [!DNL Target].

Sie können Berichte für Ihre Aktivitäten sowohl in [!DNL Analytics] als auch in [!DNL Target] anzeigen.

Informationen zu Best Practices für das Reporting mit [!DNL Analytics] für [!DNL Target] finden [ in dieser Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Überblick {#section_035A62D65608423285D8A5A54731E2C5}

Sowohl [!DNL Analytics]- als auch [!DNL Target] messen die Teilnehmer (die Personen, die an den Tests teilnehmen) und nicht die Besucher der Website.

Jedes Mal, wenn ein Besucher Aktivitätsinhalte auf der Seite sieht, führt [!DNL Target] einen direkten Server-zu-Server-Aufruf an [!DNL Analytics] durch, einschließlich der Aktivität und des Erlebnisses, die der Besucher gesehen hat. [!DNL Target] ruft auch [!DNL Analytics] auf, wenn die Konvertierung durchgeführt wird. [!DNL Analytics] fügt die Konversion als spezifisches neues [!DNL Analytics]-Ereignis mit dem Namen „Aktivitätskonversion“ hinzu, das zusammen mit anderen von [!DNL Analytics] erfassten Daten verfolgt wird.

Wenn der [!UICONTROL Select]-Vorgang verwendet wird und Sie nach *Eintritten* sortieren, werden nur Erlebnisse in den Berichten angezeigt, die während des ausgewählten Zeitraums Eintritte erhalten haben.

>[!NOTE]
>
>Von [!DNL Target] unterstützte Berichte haben eine Latenz von vier Minuten. Bei Aktivitäten, die von A4T unterstützt werden, kann es sowohl im [!DNL Target]- als auch im [!DNL Analytics]-Bericht bis zu 24 Stunden nach der ursprünglichen Speicherung der Aktivität dauern, bis die Berichtsdaten nach Erlebnissen aufgeschlüsselt werden können. Die in den ersten 24 Stunden gesammelten Daten sind noch präzise und werden dem richtigen Erlebnis zugewiesen.

## Berichte in Analytics  {#analytics}

In [!DNL Analytics] gibt es mehrere Dimensionen und Metriken, die bereitgestellt werden, nachdem die A4T-Integration aktiviert wurde.

### Dimensionen

* [!UICONTROL Analytics for Target] - Die übergeordnete ID, die durch die Integration übergeben wird. Das Format dieser Dimension ist `Activity ID:Experience ID:3rd ID`. Die folgenden Dimensionen sind Klassifizierungen dieser Dimension.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - Kann ignoriert werden

### Metriken

* [!UICONTROL Activity Impressions] - Stimmt mit der [!UICONTROL Entrants] im [!DNL Target] überein.
* [!UICONTROL Activity Conversions] - Stimmt mit der [!UICONTROL Custom Conversions] im [!DNL Target] überein.

Verwenden Sie [!DNL Analysis Workspace] das Bedienfeld [!UICONTROL Analytics for Target] , um Ihre [!DNL Target] Aktivitäten und Erlebnisse mit Leichtigkeit zu analysieren. Weitere Informationen finden Sie unter [Bedienfeld „Analytics for Target“ (A4T](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de) im *Handbuch zu Analytics-Tools*.

>[!IMPORTANT]
>
>Wenn Ihr [!UICONTROL Target Activities] in [!DNL Analytics] „Nicht angegeben“ auflistet, anstatt Ihre Aktivitäten aufzulisten, ist eine Aktualisierung Ihres bereitgestellten Kontos erforderlich. Wenden Sie sich an den Kundendienst, um dieses Problem zu beheben.

Detaillierte Informationen und Beispiele finden Sie im Tutorial [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) von Adobe Experience League.

## Berichte in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wenn [!DNL Analytics] als Berichtsquelle verwendet wird, zeigen Berichte in [!DNL Target] die aus [!DNL Analytics] erfassten Daten an. Der Bericht unterscheidet sich etwas von anderen [!DNL Target]:

* In der Liste [!UICONTROL Audiences] werden die Zielgruppen angezeigt, die für Ihre [!DNL Analytics] Report Suite verfügbar sind.
* In der [!UICONTROL Metric] Liste werden alle Metriken angezeigt, die über [!DNL Analytics] verfügbar sind.

  Alle Metriken sind verfügbar, einschließlich benutzerdefinierter oder berechneter Metriken, die in [!DNL Analytics] integriert sind.

  Erhöhte Zahlen werden im Bericht als positiv angezeigt, auch wenn eine Erhöhung unerwünscht ist. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

Sie können die Metrik oder Zielgruppe auf den Bericht in [!DNL Target] anwenden, nachdem die Aktivität gestartet wurde oder sogar nachdem der Test abgeschlossen ist. Es ist nicht erforderlich, dass Sie im Vorhinein genau wissen, was Sie messen möchten.

Klicken Sie, um den vollständigen [!DNL Analytics] direkt von der Seite „Aktivitätsbericht“ aus anzuzeigen.

## Aktivitätserstellung {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Bei der Erstellung einer Aktivität müssen Sie ein Ziel für die Aktivität auf der [!UICONTROL Settings] angeben. Dieses Ziel wird zur Standardmetrik für den Bericht und wird immer als erste Option in der Metrikauswahl aufgeführt. Sie können keine Segmente für die Berichterstellung auswählen, wie Sie es für eine reguläre Target-Aktivität tun würden. Bei einem Test mit [!DNL Analytics] werden [!DNL Adobe Analytics] Segmente anstelle [!DNL Target] Zielgruppen verwendet.

## Durchführen von Offline-Berechnungen für Analytics for Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Sie können Offline-Berechnungen für Konfidenz- und Konfidenzintervalle für A4T mithilfe der Excel-Datei [!DNL Target] [Konfidenzrechner abschließen](/help/main/assets/complete_confidence_calculator.xlsx) durchführen. Dies erfordert jedoch einen Schritt mit Datenexporten in [!DNL Analytics].

Für A4T verwenden wir eine [Welchs t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank}-Berechnung für kontinuierliche Variablen (anstelle binärer Metriken). In Analytics werden Besucher immer verfolgt und jede durchgeführte Aktion wird gezählt. Wenn ein Besucher mehrfach einkauft oder eine Erfolgsmetrik mehrfach besucht, werden diese zusätzlichen Treffer also gezählt. Daher ist die Metrik eine kontinuierliche Variable. Zur Berechnung des t-Tests von Welch wird die „Summe der Quadrate“ benötigt, um die Varianz zu berechnen, die im Nenner der t-Statistik verwendet wird. [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) erläutert die Details der verwendeten mathematischen Formeln. Die Summe der Quadrate kann aus [!DNL Analytics] abgerufen werden. Zum Abrufen der Summe aus Quadratdaten müssen Sie für einen Testzeitraum einen Export auf Besucherebene für die zu optimierende Metrik durchführen.

Wenn Sie beispielsweise die Anzeige von Seitenansichten pro Besucher optimieren, exportieren Sie ein Beispiel für die Gesamtzahl der Seitenansichten pro Besucher für einen bestimmten Zeitraum, vielleicht für einige Tage (mehr als tausend Datenpunkte sind alles, was Sie benötigen). Anschließend quadrieren Sie die einzelnen Werte und bilden die Summe der Gesamtwerte (die Reihenfolge der Vorgänge muss hier unbedingt beachtet werden). Dieser „Quadratsummen“-Wert wird anschließend im Complete Confidence Calculator verwendet. Verwenden Sie für diese Werte den Bereich „Umsatz“ dieses Arbeitsblatts.

**So verwenden Sie die [!DNL Analytics]-Datenexportfunktion:**

1. Melden Sie sich bei [!DNL Adobe Analytics] an.
1. Klicken Sie auf **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Füllen Sie auf der Registerkarte **[!UICONTROL Data Warehouse Request]** die Felder aus.

   Weitere Informationen zu den einzelnen Feldern finden Sie unter „Data Warehouse-Beschreibungen“ in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Feld | Anleitung |
   |--- |--- |
   | Anforderungsname | Geben Sie einen Namen für Ihre Anforderung ein. |
   | Berichtsdatum | Geben Sie einen Zeitraum und eine Granularität an.<br>Es hat sich bewährt, für die erste Anforderung maximal eine Stunde oder einen Tag mit Daten auszuwählen.  Die Verarbeitung von Data Warehouse-Dateien dauert umso länger, je länger der angeforderte Zeitraum ist. Daher ist es immer am besten, zunächst Daten für einen kleineren Zeitraum anzufordern, um sicherzustellen, dass die Datei das erwartete Ergebnis zurückgibt. Rufen Sie anschließend Request Manager auf, duplizieren Sie die Anforderung und fragen Sie beim zweiten Durchlauf mehr Daten an. Wenn Sie die Granularität auf einen anderen Wert als „Keine“ umschalten, wird die Dateigröße ebenfalls drastisch erhöht.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Verfügbare Segmente | Wenden Sie bei Bedarf ein Segment an. |
   | Aufschlüsselung | Wählen Sie die gewünschten Dimensionen aus: Standard ist vorkonfiguriert (OOTB), während „Benutzerdefiniert“ eVars und Props enthält. Es wird empfohlen, „Besucher-ID“ zu verwenden, wenn Informationen auf Besucher-ID-Ebene benötigt werden, und nicht &quot;Experience Cloud-Besucher-ID“.<ul><li>Die Besucher-ID ist die finale ID, die von Analytics verwendet wird. Sie lautet entweder AID (wenn es sich um einen bestehenden Kunden handelt) oder MID (wenn der Kunde neu ist oder nach dem Start des MC-Besucher-ID-Diensts Cookies gelöscht hat).</li><li>Die Experience Cloud-Besucher-ID wird nur für Kunden festgelegt, die neu sind oder nach dem Start des MC-Besucher-ID-Service Cookies gelöscht haben.</li></ul> |
   | Metriken | Wählen Sie die gewünschten Metriken aus. Die Standardeinstellung lautet OOTB, während die benutzerdefinierte Einstellung benutzerdefinierte Ereignisse einschließt. |
   | Berichtvorschau | Überprüfen Sie vor dem Planen des Berichts Ihre Einstellungen.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Auslieferung planen | Geben Sie eine E-Mail-Adresse ein, an die die Datei gesendet werden soll, benennen Sie die Datei und wählen Sie dann [!UICONTROL Send Immediately] aus.<br>Hinweis: Die Datei kann über FTP unter &quot;[!UICONTROL Advanced Delivery Options]<br>![ Versand planen“ ](/help/main/c-reports/assets/datawarehouse3.png) werden. |

1. Klicken Sie auf **[!UICONTROL Request this Report]**.

   Die Dateibereitstellung kann je nach Umfang der angeforderten Daten bis zu 72 Stunden in Anspruch nehmen. Sie können den Fortschritt Ihrer Anfrage jederzeit überprüfen, indem Sie auf [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] klicken.

   Wenn Sie Daten erneut anfordern möchten, die Sie in der Vergangenheit angefordert haben, können Sie bei Bedarf eine alte Anfrage aus der [!UICONTROL Request Manager] duplizieren.

Weitere Informationen über [!DNL Data Warehouse] finden Sie in der [!DNL Analytics]-Hilfsdokumentation unter den folgenden Links:

* [Erstellen einer Data Warehouse-Anfrage](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Best Practices für Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)
