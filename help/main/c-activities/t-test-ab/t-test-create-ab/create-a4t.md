---
keywords: Targeting;Analytics;Tracking-Server;Analytics for Target;A4T
description: Erfahren Sie, wie Sie eine Aktivität konfigurieren [!DNL Adobe Target]  die  [!DNL Adobe Analytics]  Berichtsquelle (A4T) verwendet wird.
title: Wie kann ich - [!DNL Analytics]  in  [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 16%

---

# [!DNL Adobe Analytics] verwenden

Sie können eine Aktivität in [!DNL Adobe Target] so konfigurieren, dass [!DNL Adobe Analytics] als Berichtsquelle (A4T) verwendet wird.

Detaillierte Informationen zum Einrichten von [!DNL Analytics] als Datenquelle für [!DNL Target] finden Sie unter [Adobe Analytics als Reporting-Source für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Bevor Sie eine Aktivität einrichten, die [!DNL Analytics] als Berichtsquelle verwendet, legen Sie das Ziel der Aktivität fest, z. B. die Steigerung des Umsatzes pro Besucher (RPV) oder die Steigerung der Klicks auf den Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Obwohl Sie in [!DNL Analytics] jederzeit zusätzliche Metriken auswählen können, müssen Sie dennoch eine bestimmte Metrik angeben, auf die sich dieser Test voraussichtlich auswirken wird.

>[!NOTE]
>
>Die Option [!DNL Adobe Analytics] ist verfügbar, wenn Sie Ihr [!DNL Adobe Experience Cloud]-Konto sowohl mit [!DNL Analytics] als auch mit [!DNL Target] verknüpft haben, auch wenn die Integration zwischen [!DNL Target] und [!DNL Analytics] für Ihr Konto nicht eingerichtet wurde.

Bei der Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target] wählen Sie eine [!DNL Analytics] Report Suite aus, um [!DNL Target] Aktivitätsdaten zu erhalten. Um eine Berichtsquelle anzugeben, wählen Sie zunächst eines der [!DNL Analytics] Unternehmen aus, mit denen Ihr Konto verknüpft ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Adobe Target] bereitgestellt wurden. Wenn die erwartete Report Suite nicht angezeigt wird, versuchen Sie zunächst, sich abzumelden und sich wieder bei der [!DNL Adobe Experience Cloud] anzumelden, um es dann erneut zu versuchen. Wenn die Report Suite noch immer in der Liste fehlt, wenden Sie sich an die Kundenunterstützung.

[!UICONTROL Analytics for Target] (A4T) erfordert einen Trackingserver, um Ergebnisse korrekt zu melden. Im Feld [!UICONTROL Tracking Server] wird ein standardmäßiger Tracking-Server angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie den richtigen Tracking-Server in dieses Feld einbeziehen. Weitere Informationen finden [ unter „Verwenden eines Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)Trackingservers“.

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung der Aktivität keinen Trackingserver angeben, wenn Sie at.js-Version 0.9.1 (oder höher) verwenden. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Goals & Settings] leer lassen.

Beim Einrichten von Aktivitäten nach der Einrichtung von [!DNL Analytics] als Berichtsquelle gibt es keine Option zum Einrichten von Zielgruppen für das Reporting. [!DNL Analytics] Segmente sind im Bericht [!DNL Target] [!UICONTROL Activities] verfügbar.

Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können jede [!DNL Analytics] Metrik auswählen, die im [!DNL Analytics] Metrikselektor verfügbar ist.

Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch den Test verbessern möchten.

Nachdem ein Besucher Ihr Ziel erreicht hat, ist dieser Besucher nicht mehr in der Aktivität enthalten. Wenn der Besucher nach Abschluss einer Aktivität erneut Ihre Aktivität aufruft, wird dieser Besucher als neuer Besucher gezählt.
