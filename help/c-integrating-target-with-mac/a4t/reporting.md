---
keywords: Analytics für Target; a4t; Analytics als Berichtsquelle
description: Erfahren Sie, wie Sie Analytics für die Zielgruppe (A4T) verwenden. A4T bietet Zugriff auf Analytics-Berichte für Aktivitäten der Zielgruppe, die Analytics-Metriken und Audiencen-Segmente verwenden.
title: Wie verwende ich Berichte in A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# A4T-Reporting{#a-t-reporting}

Durch Verwendung von [!DNL Analytics] als Ihre Berichte-Quelle für [!DNL Target] (A4T) haben Sie Zugriff auf [!DNL Analytics]-Berichte für Ihre [!DNL Target]-Aktivitäten.

Sie können Berichte für Ihre Aktivitäten sowohl in [!DNL Analytics] als auch in [!DNL Target] Ansicht erstellen.

Die Best Practices für Berichte mit [!DNL Analytics] für [!DNL Target], [finden Sie auf dieser Adobe Spark-Seite](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Überblick {#section_035A62D65608423285D8A5A54731E2C5}

Die Berichte [!DNL Analytics] und [!DNL Target] messen die Teilnehmer (die Personen, die an den Tests teilnehmen) und nicht die Besucher zur Site.

Jedes Mal, wenn ein Besucher Seiteninhalte anzeigt, führt [!DNL Target] einen direkten Server-zu-Server-Aufruf an [!DNL Analytics] durch, einschließlich der Aktivität und des Erlebnisses, die der Besucher sah. [!DNL Target] wird auch  [!DNL Analytics] immer dann aufgerufen, wenn die Konvertierung erfolgt. [!DNL Analytics] fügt die Konversion als spezifisches neues  [!DNL Analytics] Ereignis mit dem Namen &quot;Aktivität Conversion&quot;hinzu, das zusammen mit anderen erfassten Daten verfolgt wird  [!DNL Analytics].

Wenn der Vorgang [!UICONTROL Select] verwendet wird und Sie nach *Teilnehmer* sortieren, werden in den Berichten nur Erlebnisse angezeigt, die während des ausgewählten Zeitraums Teilnehmer erhalten haben.

>[!NOTE]
>
>Berichte, die mit [!DNL Target] betrieben werden, haben eine Latenz von vier Minuten. Bei Aktivitäten, die mit A4T betrieben werden, kann es sowohl in den Berichten [!DNL Target] als auch [!DNL Analytics] bis zu 24 Stunden nach der ersten Speicherung der Aktivität dauern, bis die Berichtsdaten nach Erlebnissen aufgeschlüsselt werden können. Die in den ersten 24 Stunden gesammelten Daten sind noch präzise und werden dem richtigen Erlebnis zugewiesen.

## Berichte in Analytics   {#analytics}

In [!DNL Analytics] stehen mehrere Dimensionen und Metriken zur Verfügung, nachdem die A4T-Integration aktiviert wurde.

### Dimensionen

* [!UICONTROL Analytics für Zielgruppe] : Die übergeordnete ID, die durch die Integration weitergegeben wird. Das Format dieser Dimension ist `Activity ID:Experience ID:3rd ID`. Die folgenden Dimensionen sind Klassifizierungen dieser Dimension.
* [!UICONTROL Target Activities]
* [!UICONTROL Target-Erlebnisse]
* [!UICONTROL Zielgruppe Aktivität] >  [!UICONTROL Erlebnis]
* [!UICONTROL 3. ID]  - kann ignoriert werden

### Metriken

* [!UICONTROL Aktivitäten-Impressionen] : Entspricht der   Anzahl der Teilnehmer im  [!DNL Target] Bericht.
* [!UICONTROL Aktivitäten-Konversionen] : Entspricht der  [!UICONTROL benutzerspezifischen ] Konversionsnummer im  [!DNL Target] Bericht.

Verwenden Sie in [!DNL Analysis Workspace] das Bedienfeld [!UICONTROL Analytics für Zielgruppe], um Ihre [!DNL Target]-Aktivitäten und -Erlebnisse mit Steigerung und Konfidenz zu analysieren. Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T) Panel](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) im *Analytics Tools Guide*.

>[!IMPORTANT]
>
>Wenn Ihr [!UICONTROL Zielgruppe-Aktivitäten]-Bericht in [!DNL Analytics]-Listen &quot;nicht angegeben&quot;anstatt der Auflistung Ihrer Aktivitäten erscheint, ist eine Aktualisierung für Ihr bereitgestelltes Konto erforderlich. Wenden Sie sich an den Kundendienst, um dieses Problem zu beheben.

Ausführliche Informationen und Beispiele finden Sie unter [Analytics &amp; Zielgruppe: Best Practices für die Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), bereitgestellt von Adobe Experience League.

## Berichte in Target   {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wenn [!DNL Analytics] als Berichte verwendet wird, zeigen Berichte in [!DNL Target] die von [!DNL Analytics] erfassten Daten an. Der Bericht unterscheidet sich etwas von anderen [!DNL Target]-Berichten:

* Die Liste [!UICONTROL Audiencen] zeigt die für Ihre [!DNL Analytics] Report Suite verfügbaren Audiencen.
* Die Liste [!UICONTROL Metrik] zeigt alle Metriken an, die über [!DNL Analytics] verfügbar sind.

   Jede Metrik ist verfügbar, einschließlich benutzerspezifischer oder berechneter Metriken, die in [!DNL Analytics] integriert sind.

   Beachten Sie, dass jede Zahl, die erhöht wird, im Bericht als positiv dargestellt wird, auch wenn eine Erhöhung eigentlich unerwünscht ist. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

Sie können die Metrik oder Audience auf den Bericht in [!DNL Target] anwenden, nachdem die Aktivität gestartet wurde oder sogar nachdem der Test abgeschlossen wurde. Es ist nicht erforderlich, dass Sie im Vorhinein genau wissen, was Sie messen möchten.

Klicken Sie auf , um den vollständigen [!DNL Analytics]-Bericht direkt auf der Aktivität-Berichtsseite Ansicht.

## Aktivitätserstellung {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Während der Erstellung einer Aktivität müssen Sie auf der Seite [!UICONTROL Einstellungen] ein spezifisches Ziel für diese Aktivität angeben. Dieses Ziel wird zur Standardmetrik für den Bericht und wird immer als erste Option in der Metrikauswahl aufgeführt. Sie können keine Segmente für die Berichterstellung auswählen, wie Sie es für eine reguläre Target-Aktivität tun würden. Bei einem Test mit [!DNL Analytics] werden anstelle von [!DNL Target]-Audiencen [!DNL Adobe Analytics]-Segmente verwendet.

## Offline-Berechnungen für Analytics for Zielgruppe (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Weitere Informationen dazu finden Sie unter [Durchführen von Offline-Berechnungen für Analytics for Target (A4T)](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
