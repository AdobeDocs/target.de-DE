---
keywords: Targeting;Analytics;Tracking-Server;Analytics for Target;A4T
description: Erfahren Sie, wie Sie eine Aktivität konfigurieren, [!DNL Adobe Target] [!DNL Adobe Analytics] als Berichtsquelle (A4T) zu verwenden.
title: Wie kann ich [!DNL Analytics] in [!DNL Target] verwenden?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
TQID: 'https://experienceleague.adobe.com/x38YsYI4a6-92oOr6Fs3RfKrJHbSaLNj0cki5CInPPg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 891742a5-242d-5099-966a-ca76c17cd2d2
    internal-label: Analytics for Target (A4T)
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%
---
# [!DNL Adobe Analytics] verwenden {#create-a4t}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine Aktivität konfigurieren, um [!DNL Adobe Analytics] als Berichtsquelle (A4T) zu verwenden, was Sie vor dem Start vorbereiten müssen und wie Sie das Ziel der Aktivität auswählen.

>[!ENDSHADEBOX]

Analytics for Target (A4T) misst die Ergebnisse einer [!DNL Adobe Target] mit den Daten und Metriken von [!DNL Adobe Analytics]. Um A4T zu verwenden, konfigurieren Sie die Aktivität so, dass [!DNL Analytics] ihre Berichtsquelle ist. Detaillierte Informationen zum Einrichten von [!DNL Analytics] als Datenquelle für [!DNL Target] finden Sie unter [Adobe Analytics als Reporting-Source für Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## Bevor Sie beginnen {#before-you-begin}

>[!NOTE]
>
>Die Option **[!UICONTROL Adobe Analytics]** ist verfügbar, wenn Ihr [!DNL Adobe Experience Cloud]-Konto sowohl mit [!DNL Analytics] als auch mit [!DNL Target] verknüpft ist, auch wenn die Integration zwischen [!DNL Target] und [!DNL Analytics] für Ihr Konto nicht eingerichtet wurde.

Bevor Sie eine Aktivität erstellen, legen Sie ihr Ziel fest, z. B. die Steigerung des Umsatzes pro Besucher (Revenue per Visitor, RPV) oder die Steigerung der Klicks auf Ihren Warenkorb. Wählen Sie dann die endgültige Erfolgsmetrik , die dieses Ziel misst. In [!DNL Analytics] können jederzeit zusätzliche Metriken ausgewählt werden. Sie müssen jedoch weiterhin die eine Metrik angeben, auf die sich dieser Test voraussichtlich auswirken wird.

## Analytics als Berichtsquelle auswählen {#select-reporting-source}

>[!NOTE]
>
>Wenn Sie at.js Version 0.9.1 oder höher verwenden, müssen Sie beim Erstellen einer Aktivität, die [!DNL Adobe Analytics] als Berichtsquelle verwendet, keinen Trackingserver angeben. Die at.js-Bibliothek sendet die Werte des Tracking-Servers automatisch an [!DNL Target]. Das **[!UICONTROL Tracking-Server]** auf der Seite **[!UICONTROL Ziele und Einstellungen]** kann leer bleiben.

Die Berichtsquelle wird auf der Seite **[!UICONTROL Ziele und Einstellungen]** der Aktivität ausgewählt. Auf dieser Seite wählen Sie ein [!DNL Analytics] Unternehmen und die Report Suite aus, die die [!DNL Target] Aktivitätsdaten erhält, und überprüfen den Tracking-Server.

➡️ Die Schritte, die Report Suite-Anforderungen und die Details zum Tracking-Server finden Sie unter [Reporting Source](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source).

Wenn [!DNL Analytics] die Berichtsquelle ist, bietet die Aktivität keine Option zum Einrichten von Zielgruppen für das Reporting. [!DNL Analytics] Segmente sind stattdessen im Bericht [!DNL Target]Aktivitäten **&#x200B;**&#x200B;verfügbar.

## Legen Sie das Ziel der Aktivität fest {#set-goal}

Jede Aktivität erfordert eine Erfolgsmetrik als Ziel. Das Ziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Es können alle Metriken verwendet werden, die im [!DNL Analytics] Metrikselektor verfügbar sind. Es empfiehlt sich, einen Test nie ohne das Ziel einer bestimmten Verbesserung durchzuführen.

Das Festlegen eines Ziels hindert Sie nicht daran, andere Metriken zur Auswertung der Testergebnisse zu verwenden. Das Ziel identifiziert jedoch die eine Sache, die Sie mit dem Test verbessern möchten.

Nachdem ein Besucher Ihr Ziel erreicht hat, ist dieser Besucher nicht mehr in der Aktivität enthalten. Wenn der Besucher die Aktivität nach deren Abschluss erneut aufruft, wird dieser Besucher als neuer Besucher gezählt.
