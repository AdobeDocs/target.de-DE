---
keywords: Analytics für Target; a4t; Analytics als Berichtsquelle; Analytics
description: Erfahren Sie, wie Sie Analytics für [!DNL Target] (A4T). A4T bietet Zugriff auf Analytics-Berichte für [!DNL Target] Aktivitäten, die Analytics-Metriken und Zielgruppensegmente verwenden.
title: Wie verwende ich Reporting in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 29%

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

## Durchführen von Offlineberechnungen für Analytics for Adobe Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Weitere Informationen dazu finden Sie unter [Durchführen von Offline-Berechnungen für Analytics for Target (A4T)](/help/main/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
