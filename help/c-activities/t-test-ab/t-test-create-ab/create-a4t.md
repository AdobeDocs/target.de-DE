---
description: Sie können eine Aktivität in Target Standard erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
keywords: Targeting;Analytics;Trackingserver
seo-description: Sie können eine Aktivität in Target Standard erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
seo-title: Verwenden von Analytics-Daten
solution: Target
title: Verwenden von Analytics-Daten
uuid: 4ac0c181-030b-4cf5-b138-acf02c7af4f6
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Verwenden von Analytics-Daten{#using-analytics-data}

Sie können eine Aktivität in Target Standard erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.

Detaillierte Informationen zur Einrichtung von Analytics als Datenquelle für Target finden Sie im Abschnitt [Adobe Analytics als Berichtsquelle für Adobe Target](https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html).

Bevor Sie eine Aktivität einrichten, die Analytics als Berichtsquelle verwendet, müssen Sie das Ziel für die Aktivität festlegen, beispielsweise die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Kampagne aus. Auch wenn Sie jederzeit zusätzliche Metriken in Analytics auswählen können, müssen Sie trotzdem eine bestimmte Metrik angeben, auf die dieser Test erwartungsgemäß Auswirkungen hat.

>[!NOTE]
>
>Die Option „Adobe Analytics“ ist verfügbar, wenn Sie Ihr Adobe Experience Cloud-Konto sowohl mit Analytics als auch mit Target verknüpft haben, auch wenn die Integration zwischen Target und Analytics für Ihr Konto nicht eingerichtet wurde.

Wenn Sie Analytics als Berichtsquelle für Target auswählen, wählen Sie eine Analytics-Report Suite, um Target-Aktivitätsdaten zu empfangen. Wählen Sie dazu zunächst ein Analytics-Unternehmen aus, an das Ihr Konto gebunden ist, und wählen Sie anschließend die der Aktivität entsprechende Report Suite aus. Es stehen nur Report Suites, die für die Verbindung mit Adobe Target bereitgestellt werden, zur Auswahl zur Verfügung. Wenn nicht die erwarteten Report Suites angezeigt werden, versuchen Sie, sich bei Adobe Experience Cloud ab- und dann wieder anzumelden, und wiederholen Sie den Vorgang. Wenn die Report Suite weiterhin nicht in der Liste zu finden ist, wenden Sie sich an den Kundendienst.

Analytics for Target erfordert einen Trackingserver, damit die Ergebnisse richtig in Berichten zusammengefasst werden. Im Feld für den Trackingserver erscheint ein Standard-Trackingserver. Sollten Sie mehr als einen Trackingserver verwenden, müssen Sie prüfen, dass in diesem Feld der richtige Server aufgeführt ist. Weitere Informationen zu diesem Thema finden Sie unter [Verwendung eines Analytics-Trackingservers](../../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

>[!NOTE]
>
>Sollten Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität und bei der Verwendung von mbox.js Version 61 (oder neuer) oder at.js Version 0.9.1 (oder neuer) keinen Trackingserver angeben. Die Bibliothek von mbox.js oder at.js sendet automatisch Trackingserverwerte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL „Tracking Server“] auf der Seite [!UICONTROL „Ziele und Einstellungen“] freilassen.

Wenn Sie eine Aktivität einrichten, nachdem Sie Analytics als Berichtsquelle festgelegt haben, gibt es keine Möglichkeit, Zielgruppen für die Berichterstellung festzulegen. Analytics-Segmente sind in den Target Activities-Berichten verfügbar.

Sie müssen eine Erfolgsmetrik als Ziel für jeden Test festlegen. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Kampagne signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können sämtliche in der Metrikauswahl von Analytics verfügbaren Analytics-Metriken auswählen.

Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch den Test verbessern möchten.

Nachdem ein Besucher Ihr Ziel erreicht hat, ist er nicht länger Teil der Kampagne. Tritt der Besucher nach Abschluss einer Aktivität erneut in die Kampagne ein, wird er als neuer Besucher betrachtet.
