---
keywords: Targeting; Analytics; Tracking-Server; Analytics für Target; a4t
description: Erfahren Sie, wie Sie eine Aktivität in [!DNL Adobe Target] für die Verwendung von [!DNL Adobe Analytics] als Berichtsquelle (A4T) konfigurieren.
title: Wie kann ich [!DNL Analytics] Daten in [!DNL Target] verwenden?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 16%

---

# Verwenden von [!DNL Adobe Analytics] -Daten

Sie können eine Aktivität in [!DNL Adobe Target] so konfigurieren, dass [!DNL Adobe Analytics] als Berichtsquelle (A4T) verwendet wird.

Detaillierte Informationen zum Einrichten von [!DNL Analytics] als Datenquelle für [!DNL Target] finden Sie unter [Adobe Analytics als Reporting-Source für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Bevor Sie eine Aktivität einrichten, die [!DNL Analytics] als Berichtsquelle verwendet, müssen Sie das Ziel für die Aktivität festlegen, z. B. die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Sie können zwar jederzeit zusätzliche Metriken in [!DNL Analytics] auswählen, Sie müssen jedoch weiterhin eine bestimmte Metrik angeben, auf die sich dieser Test voraussichtlich auswirken wird.

>[!NOTE]
>
>Die Option [!DNL Adobe Analytics] ist verfügbar, wenn Sie Ihr [!DNL Adobe Experience Cloud]-Konto sowohl mit [!DNL Analytics] als auch mit [!DNL Target] verknüpft haben, auch wenn die Integration zwischen [!DNL Target] und [!DNL Analytics] für Ihr Konto nicht eingerichtet wurde.

Wenn Sie [!DNL Analytics] als Berichtsquelle für [!DNL Target] auswählen, wählen Sie eine [!DNL Analytics] Report Suite aus, die [!DNL Target] Aktivitätsdaten erhält. Um eine Berichtsquelle anzugeben, wählen Sie zunächst eines der [!DNL Analytics] Unternehmen aus, an die Ihr Konto gebunden ist, und wählen dann die entsprechende Report Suite für die Aktivität aus. Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Adobe Target] bereitgestellt wurden. Wenn die erwartete Report Suite nicht angezeigt wird, versuchen Sie zunächst, sich abzumelden und sich wieder bei [!DNL Adobe Experience Cloud] anzumelden, um es erneut zu versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die Kundenunterstützung.

Für [!UICONTROL Analytics for Target] (A4T) ist ein Tracking-Server erforderlich, um Ergebnisse korrekt zu melden. Im Feld [!UICONTROL Tracking Server] wird ein standardmäßiger Trackingserver angezeigt. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie in dieses Feld den richtigen Tracking-Server einschließen. Weitere Informationen finden Sie unter [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) .

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität keinen Trackingserver angeben, wenn Sie at.js , Version 0.9.1 (oder neuer) verwenden. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Goals & Settings] leer lassen.

Beim Einrichten einer Aktivität nach der Einrichtung von [!DNL Analytics] als Berichtsquelle gibt es keine Möglichkeit, Zielgruppen für die Berichterstellung einzurichten. [!DNL Analytics] -Segmente sind im Bericht [!DNL Target] [!UICONTROL Activities] verfügbar.

Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können eine beliebige [!DNL Analytics] -Metrik auswählen, die in der Metrikauswahl [!DNL Analytics] verfügbar ist.

Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch den Test verbessern möchten.

Nachdem ein Besucher Ihr Ziel erreicht hat, wird dieser Besucher nicht mehr in die Aktivität aufgenommen. Wenn der Besucher nach Abschluss einer Aktivität erneut Ihre Aktivität aufruft, wird dieser Besucher als neuer Besucher gezählt.
