---
description: Durch die Verwendung von Analytics als Berichtsquelle für Target (A4T) erhalten Sie Zugriff auf Analytics-Berichte für Ihre Target-Aktivitäten.
keywords: Analytics für Target; a4t; Analytics als Berichtsquelle
seo-description: Durch die Verwendung von Analytics als Berichtsquelle für Target (A4T) erhalten Sie Zugriff auf Analytics-Berichte für Ihre Target-Aktivitäten.
seo-title: A4T-Reporting
solution: Target
subtopic: Multivarianz-Test
title: A4T-Reporting
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# A4T-Reporting{#a-t-reporting}

Durch die Verwendung von Analytics als Berichtsquelle für Target (A4T) erhalten Sie Zugriff auf Analytics-Berichte für Ihre Target-Aktivitäten.

Sie können sowohl in Analytics als auch in Target Standard/Premium Berichte für Ihre Aktivitäten ansehen.

Reporting-Best-Practices für Analytics for Target finden Sie auf dieser [Adobe Spark-Seite](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Überblick {#section_035A62D65608423285D8A5A54731E2C5}

Sowohl Analytics- als auch Target-Berichte messen anstelle der Site-Besucher die Zahl der Teilnehmer (die Personen, die sich am Test beteiligen).

Jedes Mal, wenn ein Besucher Aktivitätsinhalte auf der Seite sieht, startet Target einen direkten Server-zu-Server-Aufruf an Analytics, einschließlich Informationen dazu, welche Aktivitäten und Erlebnisse der Besucher gesehen hat. Target ruft Analytics auch immer dann auf, wenn die Konversion erfolgt ist. Analytics fügt die Konversion als spezifisches neues Analytics-Ereignis mit der Bezeichnung „Aktivitätskonversion“ hinzu, das zusammen mit anderen von Analytics erfassten Daten verfolgt wird.

Wenn der Vorgang „Auswählen“ verwendet wird und Sie eine Sortierung nach *Teilnehmern* vornehmen, werden in den Berichten lediglich solche Erlebnisse angezeigt, bei denen während des ausgewählten Zeitraums Teilnehmer registriert wurden.

>[!NOTE]
>
>Mit Target erstellte Berichte haben eine Wartezeit von vier Minuten. Für Aktivitäten, die mit A4T erstellt werden, kann es sowohl bei Target- als auch bei Analytics-Berichten bis zu 24 Stunden nach der erstmaligen Speicherung der Aktivität dauern, bevor die Berichtsdaten durch Erlebnisse aufgegliedert werden können. Die in den ersten 24 Stunden gesammelten Daten sind noch präzise und werden dem richtigen Erlebnis zugewiesen.

## Berichte in Analytics {#section_F6884872DC864AE7913587FAED4CD11C}

Klicken Sie in Analytics im linken Menü auf **[!UICONTROL Target]** &gt; **[!UICONTROL Target-Aktivitäten]**. In Target zeigen die Berichte der Aktivität automatisch Analytics-Daten, Metriken und Segmente an. Daten erscheinen in diesen Berichten ca. eine Stunde nach der Erfassung auf der Site. Sämtliche Metriken, Zielgruppen und Werte in den Berichten stammen aus der Report Suite, die Sie bei der Einrichtung der Aktivität ausgewählt haben.

Verwenden Sie in Analytics den Target-Aktivitätenbericht, um die Ergebnisse Ihrer Target-Aktivität anzuzeigen. (Veraltete) Test&amp;Target-Berichte enthalten Informationen über Ihre alten Seitenintegrationen im Test&amp;Target-Plugin-Stil und umfassen keine Daten aus Analytics for Target. Im Aktivitätenbericht können Sie Informationen über Ihre Target-Erlebnisse anzeigen. Klicken Sie auf **[!UICONTROL Metriken]** und wählen Sie dann den Metriktyp **Target[!UICONTROL .]** Für Ihren Bericht stehen zwei Metriken zur Verfügung:

* **Aktivitätseinträge:** Entspricht der Anzahl der Teilnehmer im Target-Bericht.
* **Aktivitätskonversionen:** Entspricht der Anzahl der benutzerdefinierten Konversionen im Target-Bericht.

>[!NOTE]
>
>Details zur Target-Steigerung und Konfidenz sind ebenfalls in Analytics verfügbar. Weitere Informationen finden Sie im Abschnitt zu [Target-Steigerung und Konfidenzberichtstyp](https://marketing.adobe.com/resources/help/en_US/reference/report_target_lift_confidence.html) in der Produktdokumentation zu Adobe Analytics.

>[!IMPORTANT]
>
>Wenn in Ihrem Target-Aktivitätenbericht in Analytics anstelle einer Auflistung Ihrer Aktivitäten die Meldung „nicht angegeben“ erscheint, ist ein Update für das für Sie bereitgestellte Konto erforderlich. Wenden Sie sich an den Kundendienst, um dieses Problem zu beheben.

## Berichte in Target {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wenn Analytics als Berichtsquelle verwendet wird, zeigen die Berichte in Target Standard die Daten an, die über Analytics erfasst werden. Der Bericht unterscheidet sich leicht von anderen Target Standard-Berichten:

* Die Liste mit den Zielgruppen enthält die Zielgruppen, die für Ihre Analytics-Report Suite verfügbar sind.
* Die Metrikenliste enthält sämtliche Metriken, die über Analytics verfügbar sind.

   Jede Metrik ist verfügbar, inklusive benutzerdefinierter oder berechneter Metriken, die in Analytics integriert sind.

   Beachten Sie, dass jede Zahl, die erhöht wird, im Bericht als positiv dargestellt wird, auch wenn eine Erhöhung eigentlich unerwünscht ist. Beispiel: Obwohl Sie eine geringere Absprungrate wünschen, wird die höhere Absprungrate als Gewinner mit der höchsten Steigerung angezeigt. Wenn Sie Entscheidungen auf Basis Ihrer Berichte treffen, müssen Sie auf diese und ähnliche Metriken achten und darauf, ob Sie diese Zahlen senken oder erhöhen möchten.

Sie können die Metrik oder die Zielgruppe auf den Bericht in Target anwenden, nachdem der Test gestartet oder sogar nachdem der Test abgeschlossen wurde. Es ist nicht erforderlich, dass Sie im Vorhinein genau wissen, was Sie messen möchten.

Klicken Sie, um den vollständigen Analytics-Bericht direkt auf der Berichtsseite der Aktivität anzuzeigen.

## Berichte in Analysis Workspace {#reports-in-analysis-workspace}

Sie können mithilfe von [!DNL Adobe Analysis Workspace] tiefere Einblicke gewinnen, um die Daten zu visualisieren oder Einblicke zu finden, die unter der Oberfläche verborgen sind.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by Adobe Experience League.

## Aktivitätserstellung {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Während der Erstellung einer Aktivität müssen Sie auf der Seite [!UICONTROL Einstellungen] ein spezifisches Ziel für diese Aktivität angeben. Dieses Ziel wird zur Standardmetrik für den Bericht und wird immer als erste Option in der Metrikauswahl aufgeführt. Sie können keine Segmente für die Berichterstellung auswählen, wie Sie es für eine reguläre Target-Aktivität tun würden. Ein Test mit Analytics verwendet Adobe Analytics-Segmente anstelle von Target Standard-Zielgruppen.

## Durchführen von Offlineberechnungen für Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Sie können Offlineberechnungen für A4T durchführen. Dazu ist jedoch ein Schritt mit Datenexporten in [!DNL Analytics] erforderlich.

Weitere Informationen dazu finden Sie unter [Durchführen von Offline-Berechnungen für Analytics for Target (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
