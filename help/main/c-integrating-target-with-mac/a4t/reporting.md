---
keywords: Analytics für Target; a4t; Analytics als Berichtsquelle; Analytics
description: Erfahren Sie, wie Sie Analytics für [!DNL Target] (A4T). A4T bietet Zugriff auf Analytics-Berichte für [!DNL Target] Aktivitäten, die Analytics-Metriken und Zielgruppensegmente verwenden.
title: Wie verwende ich Reporting in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 493ecd762b5228d33377ac8263b90a0f9c73127e
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 47%

---

# A4T-Reporting

Verwenden [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) bietet Ihnen Zugriff auf [!DNL Analytics] Berichte für Ihre [!DNL Target] Aktivitäten.

Sie können Berichte für Ihre Aktivitäten in beiden [!DNL Analytics] und [!DNL Target].

Best Practices für die Berichterstellung mit [!DNL Analytics] für [!DNL Target], [Besuch dieser Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Überblick {#section_035A62D65608423285D8A5A54731E2C5}

Beide [!DNL Analytics] und [!DNL Target] -Berichte messen die Teilnehmer (die Personen, die an den Tests teilnehmen) und nicht die Besucher der Site.

Jedes Mal, wenn ein Besucher Aktivitätsinhalte auf der Seite sieht, [!DNL Target] führt einen direkten Server-zu-Server-Aufruf an [!DNL Analytics], einschließlich der Aktivität und des Erlebnisses, die der Besucher gesehen hat. [!DNL Target] auch Aufrufe [!DNL Analytics] wann immer die Konvertierung erfolgt. [!DNL Analytics] fügt die Konversion als spezifische neue [!DNL Analytics] Ereignis mit dem Namen &quot;Aktivitätskonversion&quot;, das zusammen mit anderen von [!DNL Analytics].

Wenn die [!UICONTROL Auswählen] verwendet wird und Sie nach *Teilnehmer* festgelegt ist, werden in den Berichten nur Erlebnisse angezeigt, die während des ausgewählten Zeitraums Teilnehmer erhalten haben.

>[!NOTE]
>
>Berichte gestützt auf [!DNL Target] eine Latenz von vier Minuten haben. Bei Aktivitäten, die mit A4T unterstützt werden, in beiden [!DNL Target] und [!DNL Analytics] -Berichten kann es bis zu 24 Stunden nach der anfänglichen Speicherung der Aktivität dauern, bis die Berichtsdaten durch Erlebnisse aufgeschlüsselt werden können. Die in den ersten 24 Stunden gesammelten Daten sind noch präzise und werden dem richtigen Erlebnis zugewiesen.

## Berichte in Analytics  {#analytics}

In [!DNL Analytics]gibt es mehrere Dimensionen und Metriken, die verfügbar gemacht werden, nachdem die A4T-Integration aktiviert wurde.

### Dimensionen

* [!UICONTROL Analytics for Target] - Die übergeordnete ID, die über die Integration übergeben wird. Das Format dieser Dimension ist `Activity ID:Experience ID:3rd ID`. Die folgenden Dimensionen sind Classifications dieser Dimension.
* [!UICONTROL Target Activities]
* [!UICONTROL Target-Erlebnisse]
* [!UICONTROL Target-Aktivität] > [!UICONTROL Erlebnis]
* [!UICONTROL 3. ID] - kann ignoriert werden

### Metriken

* [!UICONTROL Aktivitätsimpressionen] - Entspricht der [!UICONTROL Teilnehmer] Zahl in der [!DNL Target] Bericht.
* [!UICONTROL Aktivitätskonversionen] - Entspricht der [!UICONTROL Benutzerdefinierte Konversionen] Zahl in der [!DNL Target] Bericht.

In [!DNL Analysis Workspace], verwenden Sie die [!UICONTROL Analytics for Target] Bedienfeld zur Analyse Ihrer [!DNL Target] Aktivitäten und Erlebnisse mit Steigerung und Konfidenz. Weitere Informationen finden Sie unter [Bedienfeld &quot;Analytics for Target&quot;(A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=de) im *Leitfaden für Analytics-Tools*.

>[!IMPORTANT]
>
>Wenn [!UICONTROL Target Activities] in [!DNL Analytics] &quot;nicht angegeben&quot;statt Ihrer Aktivitäten auflistet, ist eine Aktualisierung für Ihr bereitgestelltes Konto erforderlich. Wenden Sie sich an den Kundendienst, um dieses Problem zu beheben.

Für detaillierte Informationen und Beispiele öffnen Sie das [Analytics und Target: Best Practices für Analysen](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) Tutorial, bereitgestellt von Adobe Experience League.

## Berichte in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wann [!DNL Analytics] als Berichtsquelle verwendet wird, werden Berichte in [!DNL Target] die erfassten Daten anzeigen [!DNL Analytics]. Der Bericht unterscheidet sich etwas von anderen [!DNL Target] Berichte:

* Die [!UICONTROL Zielgruppen] Die Liste zeigt die für Ihre [!DNL Analytics] Report Suite.
* Die [!UICONTROL Metrik] Liste zeigt jede Metrik an, die über [!DNL Analytics].

   Jede Metrik ist verfügbar, einschließlich benutzerdefinierter oder berechneter Metriken, die in [!DNL Analytics].

   Erhöhte Zahlen werden im Bericht als positiv angezeigt, selbst wenn eine Erhöhung nicht erwünscht ist. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

Sie können die Metrik oder Zielgruppe auf den Bericht in [!DNL Target] nach dem Start der Aktivität oder auch nach Abschluss des Tests. Es ist nicht erforderlich, dass Sie im Vorhinein genau wissen, was Sie messen möchten.

Klicken Sie auf , um den vollständigen [!DNL Analytics] direkt von der Seite des Aktivitätsberichts aus.

## Aktivitätserstellung {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Während der Erstellung einer Aktivität müssen Sie auf der Seite [!UICONTROL Einstellungen] ein spezifisches Ziel für diese Aktivität angeben. Dieses Ziel wird zur Standardmetrik für den Bericht und wird immer als erste Option in der Metrikauswahl aufgeführt. Sie können keine Segmente für die Berichterstellung auswählen, wie Sie es für eine reguläre Target-Aktivität tun würden. Ein Test mit [!DNL Analytics] uses [!DNL Adobe Analytics] Segmente anstelle von [!DNL Target] Zielgruppen.

## Durchführen von Offlineberechnungen für Analytics für Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Für A4T verwenden wir eine [Welch&#39;s t-Test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} Berechnung für kontinuierliche Variablen (anstelle binärer Metriken). In Analytics werden Besucher immer verfolgt und jede durchgeführte Aktion wird gezählt. Wenn ein Besucher mehrfach einkauft oder eine Erfolgsmetrik mehrfach besucht, werden diese zusätzlichen Treffer also gezählt. Daher ist die Metrik eine kontinuierliche Variable. Um die t-Test-Berechnung des Welch durchzuführen, ist die &quot;Quadratsumme&quot;erforderlich, um die Varianz zu berechnen, die im Nenner der t-Statistik verwendet wird. [Statistische Berechnungen in A/Bn-Tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) erläutert die Einzelheiten der verwendeten mathematischen Formeln. Die Quadratsumme kann abgerufen werden von [!DNL Analytics]. Zum Abrufen der Summe aus Quadratdaten müssen Sie für einen Testzeitraum einen Export auf Besucherebene für die zu optimierende Metrik durchführen.

Wenn Sie beispielsweise auf Seitenansichten pro Besucher optimieren, exportieren Sie eine Stichprobe der Gesamtanzahl der Seitenansichten pro Besucher für einen bestimmten Zeitraum, vielleicht einige Tage (nur einige tausend Datenpunkte sind erforderlich). Anschließend quadrieren Sie die einzelnen Werte und bilden die Summe der Gesamtwerte (die Reihenfolge der Vorgänge muss hier unbedingt beachtet werden). Dieser „Quadratsummen“-Wert wird anschließend im Complete Confidence Calculator verwendet. Verwenden Sie für diese Werte den Bereich „Umsatz“ dieses Arbeitsblatts.

**So verwenden Sie die [!DNL Analytics]-Datenexportfunktion:**

1. Melden Sie sich bei [!DNL Adobe Analytics] an.
1. Klicken Sie auf **[!UICONTROL Werkzeuge]** > **[!UICONTROL Data Warehouse]**.
1. Füllen Sie auf der Registerkarte **[!UICONTROL Data Warehouse-Anforderung]** die Felder aus.

   Weitere Informationen zu den einzelnen Feldern finden Sie unter „Data Warehouse-Beschreibungen“ in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Feld | Anleitung |
   |--- |--- |
   | Anforderungsname | Geben Sie einen Namen für Ihre Anforderung ein. |
   | Berichtsdatum | Geben Sie einen Zeitraum und eine Granularität an.<br>Es hat sich bewährt, für die erste Anforderung maximal eine Stunde oder einen Tag mit Daten auszuwählen.  Die Verarbeitung von Data Warehouse-Dateien dauert umso länger, je länger der angeforderte Zeitraum ist. Daher ist es immer am besten, zunächst Daten für einen kleineren Zeitraum anzufordern, um sicherzustellen, dass die Datei das erwartete Ergebnis zurückgibt. Rufen Sie anschließend Request Manager auf, duplizieren Sie die Anforderung und fragen Sie beim zweiten Durchlauf mehr Daten an. Wenn Sie die Granularität auf einen anderen Wert als &quot;Keine&quot;umschalten, wird die Dateigröße drastisch erhöht.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Verfügbare Segmente | Wenden Sie bei Bedarf ein Segment an. |
   | Aufschlüsselung | Wählen Sie die gewünschten Dimensionen aus:   Die Standardeinstellung ist Out-Of-The-Box (OOTB), während die benutzerdefinierte Einstellung eVars und Eigenschaften umfasst. Es wird empfohlen, &quot;Besucher-ID&quot;zu verwenden, wenn Informationen zur Besucher-ID-Ebene erforderlich sind, anstatt &quot;Experience Cloud-Besucher-ID&quot;.<ul><li>Die Besucher-ID ist die finale ID, die von Analytics verwendet wird. Sie lautet entweder AID (wenn es sich um einen bestehenden Kunden handelt) oder MID (wenn der Kunde neu ist oder nach dem Start des MC-Besucher-ID-Diensts Cookies gelöscht hat).</li><li>Die Experience Cloud-Besucher-ID wird nur für Kunden festgelegt, die neu sind oder nach dem Start des MC-Besucher-ID-Service Cookies gelöscht haben.</li></ul> |
   | Metriken | Wählen Sie die gewünschten Metriken aus. Die Standardeinstellung lautet OOTB, während die benutzerdefinierte Einstellung benutzerdefinierte Ereignisse einschließt. |
   | Berichtvorschau | Überprüfen Sie vor dem Planen des Berichts Ihre Einstellungen.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Auslieferung planen | Geben Sie eine E-Mail-Adresse ein, an den die Datei gesendet wird. Benennen Sie die Datei und wählen Sie dann [!UICONTROL Sofort senden] aus.<br>Hinweis: Die Datei kann über FTP unter [!UICONTROL Erweiterte Auslieferungsoptionen]<br>![Lieferung planen](/help/main/c-reports/assets/datawarehouse3.png) ausgegeben werden. |

1. Klicken Sie auf **[!UICONTROL Diesen Bericht anfordern]**.

   Die Dateibereitstellung kann je nach Umfang der angeforderten Daten bis zu 72 Stunden in Anspruch nehmen. Sie können den Fortschritt Ihrer Anforderung jederzeit überprüfen, indem Sie auf [!UICONTROL Werkzeuge] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] klicken.

   Wenn Sie Daten, die Sie in der Vergangenheit angefordert haben, erneut anfordern möchten, können Sie eine alte Anforderung aus dem [!UICONTROL Anforderungs-Manager] nach Bedarf.

Weitere Informationen über [!DNL Data Warehouse] finden Sie in der [!DNL Analytics]-Hilfsdokumentation unter den folgenden Links:

* [Erstellen einer Data Warehouse-Anforderung](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Best Practices für Data Warehousen](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)
