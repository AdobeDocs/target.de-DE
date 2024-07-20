---
keywords: Analytics für Target; a4t; Analytics als Berichtsquelle; Analytics
description: Erfahren Sie, wie Sie Analytics für [!DNL Target]  (A4T) verwenden. A4T bietet Zugriff auf Analytics-Berichte für [!DNL Target] Aktivitäten, die Analytics-Metriken und Zielgruppensegmente verwenden.
title: Wie verwende ich Reporting in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 39%

---

# A4T-Reporting

Durch Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) erhalten Sie Zugriff auf [!DNL Analytics] Berichte für Ihre [!DNL Target] -Aktivitäten.

Sie können Berichte für Ihre Aktivitäten sowohl in [!DNL Analytics] als auch in [!DNL Target] anzeigen.

Best Practices für die Berichterstellung mit [!DNL Analytics] für [!DNL Target], [besuchen Sie diese Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Überblick {#section_035A62D65608423285D8A5A54731E2C5}

Sowohl die Berichte [!DNL Analytics] als auch [!DNL Target] messen die Teilnehmer (die Personen, die an den Tests teilnehmen) und nicht die Besucher der Site.

Jedes Mal, wenn ein Besucher Aktivitätsinhalte auf der Seite sieht, führt [!DNL Target] einen direkten Server-zu-Server-Aufruf an [!DNL Analytics] durch, einschließlich der Aktivität und des Erlebnisses, die der Besucher gesehen hat. [!DNL Target] ruft auch [!DNL Analytics] auf, wenn die Konversion vorgenommen wird. [!DNL Analytics] fügt die Konversion als spezifisches neues [!DNL Analytics] -Ereignis mit dem Namen &quot;Aktivitätskonversion&quot;hinzu, das zusammen mit anderen von [!DNL Analytics] erfassten Daten verfolgt wird.

Wenn der Vorgang [!UICONTROL Select] verwendet wird und Sie nach *Teilnehmern* sortieren, werden in den Berichten nur Erlebnisse angezeigt, die während des ausgewählten Zeitraums Teilnehmer erhalten haben.

>[!NOTE]
>
>Berichte mit [!DNL Target] haben eine Wartezeit von vier Minuten. Bei Aktivitäten, die mit A4T unterstützt werden, kann es sowohl in den [!DNL Target]- als auch in den [!DNL Analytics] -Berichten bis zu 24 Stunden dauern, bis die Aktivität zum ersten Mal gespeichert wurde, bevor die Berichtsdaten durch Erlebnisse aufgeschlüsselt werden können. Die in den ersten 24 Stunden gesammelten Daten sind noch präzise und werden dem richtigen Erlebnis zugewiesen.

## Berichte in Analytics  {#analytics}

In [!DNL Analytics] werden mehrere Dimensionen und Metriken bereitgestellt, nachdem die A4T-Integration aktiviert wurde.

### Dimensionen

* [!UICONTROL Analytics for Target] - Die übergeordnete ID, die über die Integration übergeben wird. Das Format dieser Dimension ist `Activity ID:Experience ID:3rd ID`. Die folgenden Dimensionen sind Classifications dieser Dimension.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - kann ignoriert werden

### Metriken

* [!UICONTROL Activity Impressions] - Entspricht der [!UICONTROL Entrants]-Zahl im [!DNL Target] -Bericht.
* [!UICONTROL Activity Conversions] - Entspricht der [!UICONTROL Custom Conversions]-Zahl im [!DNL Target] -Bericht.

Verwenden Sie in [!DNL Analysis Workspace] das Bedienfeld [!UICONTROL Analytics for Target] , um Ihre [!DNL Target] Aktivitäten und Erlebnisse mit Steigerung und Konfidenz zu analysieren. Weitere Informationen finden Sie unter [Bedienfeld &quot;Analytics for Target (A4T)&quot;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de) im *Leitfaden für Analytics-Tools*.

>[!IMPORTANT]
>
>Wenn Ihr [!UICONTROL Target Activities] -Bericht in [!DNL Analytics] &quot;nicht angegeben&quot;auflistet, anstatt Ihre Aktivitäten aufzulisten, ist eine Aktualisierung für Ihr bereitgestelltes Konto erforderlich. Wenden Sie sich an den Kundendienst, um dieses Problem zu beheben.

Ausführliche Informationen und Beispiele finden Sie im Tutorial [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) , das von Adobe Experience League bereitgestellt wird.

## Berichte in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wenn [!DNL Analytics] als Berichtsquelle verwendet wird, zeigen die Berichte in [!DNL Target] die von [!DNL Analytics] erfassten Daten an. Der Bericht unterscheidet sich etwas von anderen [!DNL Target] Berichten:

* Die Liste [!UICONTROL Audiences] enthält die Zielgruppen, die für Ihre [!DNL Analytics] Report Suite verfügbar sind.
* Die Liste [!UICONTROL Metric] zeigt jede Metrik an, die über [!DNL Analytics] verfügbar ist.

  Jede Metrik ist verfügbar, einschließlich benutzerdefinierter oder berechneter Metriken, die in [!DNL Analytics] integriert sind.

  Erhöhte Zahlen werden im Bericht als positiv angezeigt, selbst wenn eine Erhöhung nicht erwünscht ist. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

Sie können die Metrik oder Zielgruppe in [!DNL Target] auf den Bericht anwenden, nachdem die Aktivität gestartet wurde oder selbst nach Abschluss des Tests. Es ist nicht erforderlich, dass Sie im Vorhinein genau wissen, was Sie messen möchten.

Klicken Sie auf , um den vollständigen [!DNL Analytics] -Bericht direkt auf der Seite des Aktivitätsberichts anzuzeigen.

## Aktivitätserstellung {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Bei der Erstellung einer Aktivität müssen Sie auf der Seite [!UICONTROL Settings] ein Ziel für die Aktivität angeben. Dieses Ziel wird zur Standardmetrik für den Bericht und wird immer als erste Option in der Metrikauswahl aufgeführt. Sie können keine Segmente für die Berichterstellung auswählen, wie Sie es für eine reguläre Target-Aktivität tun würden. Ein Test mit [!DNL Analytics] verwendet [!DNL Adobe Analytics] -Segmente anstelle von [!DNL Target] -Zielgruppen.

## Durchführen von Offlineberechnungen für Analytics für Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Sie können Offlineberechnungen für Konfidenzintervalle für A4T mithilfe der Excel-Datei [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Für A4T verwenden wir eine t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank}-Berechnung von [Welch&#39; für kontinuierliche Variablen (anstelle von binären Metriken). In Analytics werden Besucher immer verfolgt und jede durchgeführte Aktion wird gezählt. Wenn ein Besucher mehrfach einkauft oder eine Erfolgsmetrik mehrfach besucht, werden diese zusätzlichen Treffer also gezählt. Daher ist die Metrik eine kontinuierliche Variable. Um die t-Test-Berechnung des Welch durchzuführen, ist die &quot;Quadratsumme&quot;erforderlich, um die Varianz zu berechnen, die im Nenner der t-Statistik verwendet wird. [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) erläutert die Details der verwendeten mathematischen Formeln. Die Summe der Quadrate kann von [!DNL Analytics] abgerufen werden. Zum Abrufen der Summe aus Quadratdaten müssen Sie für einen Testzeitraum einen Export auf Besucherebene für die zu optimierende Metrik durchführen.

Wenn Sie beispielsweise auf Seitenansichten pro Besucher optimieren, exportieren Sie eine Stichprobe der Gesamtanzahl der Seitenansichten pro Besucher für einen bestimmten Zeitraum, vielleicht einige Tage (nur einige tausend Datenpunkte sind erforderlich). Anschließend quadrieren Sie die einzelnen Werte und bilden die Summe der Gesamtwerte (die Reihenfolge der Vorgänge muss hier unbedingt beachtet werden). Dieser „Quadratsummen“-Wert wird anschließend im Complete Confidence Calculator verwendet. Verwenden Sie für diese Werte den Bereich „Umsatz“ dieses Arbeitsblatts.

**So verwenden Sie die [!DNL Analytics]-Datenexportfunktion:**

1. Melden Sie sich bei [!DNL Adobe Analytics] an.
1. Klicken Sie auf **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Füllen Sie auf der Registerkarte **[!UICONTROL Data Warehouse Request]** die Felder aus.

   Weitere Informationen zu den einzelnen Feldern finden Sie unter „Data Warehouse-Beschreibungen“ in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Feld | Anleitung |
   |--- |--- |
   | Anforderungsname | Geben Sie einen Namen für Ihre Anforderung ein. |
   | Berichtsdatum | Geben Sie einen Zeitraum und eine Granularität an.<br>Es hat sich bewährt, für die erste Anforderung maximal eine Stunde oder einen Tag mit Daten auszuwählen.  Die Verarbeitung von Data Warehouse-Dateien dauert umso länger, je länger der angeforderte Zeitraum ist. Daher ist es immer am besten, zunächst Daten für einen kleineren Zeitraum anzufordern, um sicherzustellen, dass die Datei das erwartete Ergebnis zurückgibt. Rufen Sie anschließend Request Manager auf, duplizieren Sie die Anforderung und fragen Sie beim zweiten Durchlauf mehr Daten an. Wenn Sie die Granularität auf einen anderen Wert als &quot;Keine&quot;umschalten, wird die Dateigröße drastisch erhöht.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Verfügbare Segmente | Wenden Sie bei Bedarf ein Segment an. |
   | Aufschlüsselung | Wählen Sie die gewünschten Dimensionen aus: Standard ist vorkonfiguriert (OOTB), während &quot;Benutzerdefiniert&quot;eVars und Props enthält. Es wird empfohlen, &quot;Besucher-ID&quot;zu verwenden, wenn Informationen zur Besucher-ID-Ebene erforderlich sind, anstatt &quot;Experience Cloud-Besucher-ID&quot;.<ul><li>Die Besucher-ID ist die finale ID, die von Analytics verwendet wird. Sie lautet entweder AID (wenn es sich um einen bestehenden Kunden handelt) oder MID (wenn der Kunde neu ist oder nach dem Start des MC-Besucher-ID-Diensts Cookies gelöscht hat).</li><li>Die Experience Cloud-Besucher-ID wird nur für Kunden festgelegt, die neu sind oder nach dem Start des MC-Besucher-ID-Service Cookies gelöscht haben.</li></ul> |
   | Metriken | Wählen Sie die gewünschten Metriken aus. Die Standardeinstellung lautet OOTB, während die benutzerdefinierte Einstellung benutzerdefinierte Ereignisse einschließt. |
   | Berichtvorschau | Überprüfen Sie vor dem Planen des Berichts Ihre Einstellungen.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Auslieferung planen | Geben Sie eine E-Mail-Adresse ein, an die die Datei gesendet werden soll, benennen Sie die Datei und wählen Sie dann [!UICONTROL Send Immediately] aus.<br>Hinweis: Die Datei kann über FTP unter [!UICONTROL Advanced Delivery Options]<br>![Bereitstellung planen](/help/main/c-reports/assets/datawarehouse3.png) bereitgestellt werden. |

1. Klicken Sie auf **[!UICONTROL Request this Report]**.

   Die Dateibereitstellung kann je nach Umfang der angeforderten Daten bis zu 72 Stunden in Anspruch nehmen. Sie können den Fortschritt Ihrer Anfrage jederzeit überprüfen, indem Sie auf [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] klicken.

   Wenn Sie Daten, die Sie in der Vergangenheit angefordert haben, erneut anfordern möchten, können Sie eine alte Anforderung aus dem [!UICONTROL Request Manager] nach Bedarf duplizieren.

Weitere Informationen über [!DNL Data Warehouse] finden Sie in der [!DNL Analytics]-Hilfsdokumentation unter den folgenden Links:

* [Erstellen einer Data Warehouse-Anfrage](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Best Practices für Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)
