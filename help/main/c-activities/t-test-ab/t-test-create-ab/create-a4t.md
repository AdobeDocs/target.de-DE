---
keywords: Targeting; Analytics; Tracking-Server; Analytics für Target; a4t
description: Erfahren Sie, wie Sie eine Aktivität in Adobe konfigurieren [!DNL Target] , um Adobe Analytics als Berichtsquelle zu verwenden. Diese Integration heißt Analytics für [!DNL Target] (A4T).
title: Wie kann ich Analytics-Daten in Target verwenden?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 80%

---

# Verwenden von Analytics-Daten

Sie können eine Aktivität in [!DNL Adobe Target] zur Verwendung [!DNL Adobe Analytics] als Berichtsquelle (A4T).

Detaillierte Informationen zum Einrichten von Analytics als Datenquelle für Target finden Sie unter [Adobe Analytics als Berichtsquelle für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Bevor Sie eine Aktivität einrichten, die Analytics als Berichtsquelle verwendet, müssen Sie das Ziel für die Aktivität festlegen, beispielsweise die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Kampagne aus. Auch wenn Sie jederzeit zusätzliche Metriken in Analytics auswählen können, müssen Sie trotzdem eine bestimmte Metrik angeben, auf die dieser Test erwartungsgemäß Auswirkungen hat.

>[!NOTE]
>
>Die Option „Adobe Analytics“ ist verfügbar, wenn Sie Ihr Adobe Experience Cloud-Konto sowohl mit Analytics als auch mit Target verknüpft haben, auch wenn die Integration zwischen Target und Analytics für Ihr Konto nicht eingerichtet wurde.

Wenn Sie Analytics als Berichtsquelle für Target auswählen, wählen Sie eine Analytics-Report Suite, um Target-Aktivitätsdaten zu empfangen. Wählen Sie dazu zunächst ein Analytics-Unternehmen aus, an das Ihr Konto gebunden ist, und wählen Sie anschließend die der Aktivität entsprechende Report Suite aus. Es stehen nur Report Suites, die für die Verbindung mit Adobe Target bereitgestellt werden, zur Auswahl zur Verfügung. Wenn nicht die erwarteten Report Suites angezeigt werden, versuchen Sie, sich bei Adobe Experience Cloud ab- und dann wieder anzumelden, und wiederholen Sie den Vorgang. Wenn die Report Suite weiterhin nicht in der Liste zu finden ist, wenden Sie sich an den Kundendienst.

Analytics for Target erfordert einen Trackingserver, damit die Ergebnisse richtig in Berichten zusammengefasst werden. Im Feld für den Trackingserver erscheint ein Standard-Trackingserver. Sollten Sie mehr als einen Trackingserver verwenden, müssen Sie prüfen, dass in diesem Feld der richtige Server aufgeführt ist. Weitere Informationen zu diesem Thema finden Sie unter [Verwendung eines Analytics-Trackingservers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

>[!NOTE]
>
>Wenn Sie Adobe Analytics als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Aktivitätserstellung keinen Trackingserver angeben, wenn Sie at.js , Version 0.9.1 (oder neuer) verwenden. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Ziele und Einstellungen] leer lassen.

Wenn Sie eine Aktivität einrichten, nachdem Sie Analytics als Berichtsquelle festgelegt haben, gibt es keine Möglichkeit, Zielgruppen für die Berichterstellung festzulegen. Analytics-Segmente sind in den Target Activities-Berichten verfügbar.

Sie müssen eine Erfolgsmetrik als Ziel für jeden Test festlegen. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Kampagne signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können sämtliche in der Metrikauswahl von Analytics verfügbaren Analytics-Metriken auswählen.

Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch den Test verbessern möchten.

Nachdem ein Besucher Ihr Ziel erreicht hat, ist er nicht länger Teil der Kampagne. Tritt der Besucher nach Abschluss einer Aktivität erneut in die Kampagne ein, wird er als neuer Besucher betrachtet.
