---
keywords: Targeting; Analytics; Tracking-Server; Analytics für Target; a4t
description: Erfahren Sie, wie Sie eine Aktivität in [!DNL Adobe Target] zur Verwendung [!DNL Adobe Analytics] als Berichtsquelle (A4T).
title: Wie kann ich [!DNL Analytics] Daten in [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 19%

---

# Verwenden [!DNL Adobe Analytics] data

Sie können eine Aktivität in [!DNL Adobe Target] zur Verwendung [!DNL Adobe Analytics] als Berichtsquelle (A4T).

Detaillierte Informationen zur Einrichtung von [!DNL Analytics] als Datenquelle für [!DNL Target], siehe [Adobe Analytics als Berichtsquelle für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Bevor Sie eine Aktivität einrichten, die [!DNL Analytics] Legen Sie als Berichtsquelle das Ziel für die Aktivität fest, z. B. die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Sie können jedoch jederzeit weitere Metriken auswählen in [!DNL Analytics]müssen Sie weiterhin eine bestimmte Metrik angeben, auf die sich dieser Test voraussichtlich auswirken wird.

>[!NOTE]
>
>Die [!DNL Adobe Analytics] ist verfügbar, wenn Sie Ihre [!DNL Adobe Experience Cloud] -Konto mit beiden [!DNL Analytics] und [!DNL Target], auch wenn die Integration zwischen [!DNL Target] und [!DNL Analytics] wurde nicht für Ihr Konto eingerichtet.

Bei Auswahl von [!DNL Analytics] als Berichtsquelle für [!DNL Target], wählen Sie eine [!DNL Analytics] Report Suite, die empfangen wird [!DNL Target] Aktivitätsdaten. Um eine Berichtsquelle anzugeben, wählen Sie zunächst eine der [!DNL Analytics] Unternehmen, an die Ihr Konto gebunden ist, und wählen Sie dann die entsprechende Report Suite für die Aktivität aus. Nur Report Suites, für die eine Verbindung hergestellt wurde [!DNL Adobe Target] stehen zur Auswahl zur Verfügung. Wenn die erwartete Report Suite nicht angezeigt wird, melden Sie sich zunächst ab und dann wieder bei der [!DNL Adobe Experience Cloud] erneut versuchen. Wenn die Report Suite weiterhin nicht in der Liste enthalten ist, wenden Sie sich an die Kundenunterstützung.

[!UICONTROL Analytics for Target] (A4T) erfordert einen Tracking-Server, um die Ergebnisse korrekt zu melden. Ein standardmäßiger Trackingserver wird im [!UICONTROL Tracking-Server] -Feld. Wenn Sie mehr als einen Tracking-Server verwenden, stellen Sie sicher, dass Sie in dieses Feld den richtigen Tracking-Server einschließen. Siehe [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) für weitere Informationen.

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Berichtsquelle für Ihre Aktivität verwenden, müssen Sie bei der Erstellung einer Aktivität keinen Trackingserver angeben, wenn Sie at.js , Version 0.9.1 (oder neuer) verwenden. Die at.js-Bibliothek sendet automatisch Tracking-Server-Werte an [!DNL Target]. Bei der Erstellung einer Aktivität können Sie das Feld [!UICONTROL Tracking Server] auf der Seite [!UICONTROL Ziele und Einstellungen] leer lassen.

Beim Einrichten der Aktivität nach der Einrichtung [!DNL Analytics] als Berichtsquelle angeben, gibt es keine Möglichkeit, Zielgruppen für die Berichterstellung einzurichten. [!DNL Analytics] -Segmente sind im Abschnitt [!DNL Target] [!UICONTROL Tätigkeiten] Bericht.

Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können eine beliebige [!DNL Analytics] Metrik verfügbar in der [!DNL Analytics] Metrikauswahl.

Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch den Test verbessern möchten.

Nachdem ein Besucher Ihr Ziel erreicht hat, wird dieser Besucher nicht mehr in die Aktivität aufgenommen. Wenn der Besucher nach Abschluss einer Aktivität erneut Ihre Aktivität aufruft, wird dieser Besucher als neuer Besucher gezählt.
