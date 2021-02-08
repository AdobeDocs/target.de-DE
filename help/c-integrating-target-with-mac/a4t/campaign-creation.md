---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie eine Aktivität in Adobe Target konfigurieren, die Adobe Analytics als Berichte-Quelle (A4T) verwendet.
title: Wie erstelle ich eine Aktivität, die A4T verwendet?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Erstellen einer Aktivität, die Analytics als Berichte-Quelle verwendet

Sie können eine Aktivität in [!DNL Target] konfigurieren, um [!DNL Adobe Analytics] als Berichte-Quelle (A4T) zu verwenden.

Bevor Sie eine Aktivität einrichten, die [!DNL Analytics] als Berichte-Quelle verwendet, müssen Sie das Ziel für die Aktivität festlegen, z. B. die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf den Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Obwohl Sie jederzeit weitere Metriken in [!DNL Analytics] auswählen können, müssen Sie dennoch eine bestimmte Metrik angeben, die Sie von diesem Test erwarten.

## Erstellen Sie die Aktivität

Das Erstellen einer [!DNL Target]-Aktivität, die [!DNL Analytics] als Berichte-Quelle verwendet, ähnelt dem Einrichten einer regulären [!DNL Target]-Aktivität mit einigen wichtigen Unterschieden. Beispielsweise können Sie beim Erstellen der Aktivität kein Segment für Berichte auswählen, da alle in [!DNL Analytics] verfügbaren Segmente beim Anzeigen eines Berichts angewendet werden können.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >Der Name einer Aktivität darf das Zeichen &quot;%&quot;nicht enthalten, wenn [!DNL Analytics] als Berichte verwendet wird.

1. Wählen Sie den Aktivitätstyp aus und beginnen Sie mit der Einrichtung der Aktivität.

   Wenn Sie eine [!UICONTROL Aktivität für die automatische Zuordnung] oder [!UICONTROL Auto-Zielgruppe] erstellen möchten, finden Sie weitere Informationen unter [A4T-Unterstützung für Aktivitäten für die automatische Zuordnung und automatische Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Wählen Sie in den **[!UICONTROL Einstellungen]** für die Aktivität **[!UICONTROL Adobe Analytics]** aus und geben Sie Ihr Unternehmen an.
1. Wählen Sie eine Report Suite aus.

   Sie können eine beliebige Report Suite auswählen, die unter [!DNL Analytics] verfügbar ist. Die Report Suite definiert, wo die erfassten Daten verfügbar sind. Virtuelle Report Suites werden nicht in der Liste der Report Suites aufgeführt.

   Beim Auswählen der Report Suite kann es vorkommen, dass Ihnen zwei Fehler gemeldet werden:

   * Sie erhalten die Fehlermeldung, dass keine Report Suites verfügbar sind, obwohl Ihr Konto korrekt eingerichtet ist.

      Möglicherweise müssen Sie Ihre [!DNL Analytics]-Firma überprüfen. Wenn Ihr [!DNL Adobe Experience Cloud]-Konto mit mehr als einer [!DNL Analytics]-Firma verknüpft ist, melden Sie sich bei [!DNL Target] ab und melden Sie sich unter der richtigen Firma bei [!DNL Analytics] an. Kehren Sie dann zu [!DNL Target] zurück, und die Report Suites werden geladen.

   * Ihnen wird nicht die Report Suite angezeigt, die Sie erwartet haben.

      Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Target] bereitgestellt werden. Wenn die erwarteten Report Suites nicht angezeigt werden, melden Sie sich zunächst ab und melden Sie sich wieder bei [!DNL Adobe Experience Cloud] an, um es erneut zu versuchen.
   Wenn die Report Suite(s) weiterhin nicht in der Liste zu finden ist/sind, [wenden Sie sich an den Kundendienst](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Legen Sie den Trackingserver fest.

   Siehe [Verwenden eines Analytics-Tracking-Servers](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definieren Sie das Erlebnis.
1. Legen Sie das Aktivitätsziel fest.

   Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können eine beliebige [!DNL Analytics]-Metrik auswählen, die in der [!DNL Analytics]-Metrikauswahl verfügbar ist.

   >[!NOTE]
   >
   >Sie können eine benutzerspezifische, auf Zielgruppen basierende Metrik an [!DNL Analytics] senden, anstatt sich nur auf [!DNL Analytics]-Daten zu verlassen. Sie können beispielsweise den Klick auf eine Seite überwachen, die normalerweise nicht von [!DNL Analytics] verfolgt wird. Diese benutzerspezifische Metrik wird automatisch vom Server [!DNL Target] an [!DNL Analytics] gesendet und wird in der Metrikauswahl unter [!DNL Analytics] als Metrik &quot;[!DNL Target] Konversion&quot;angezeigt. Die [!DNL Target]-Konversionsmetrik ist leer, wenn Sie [!DNL Analytics]-Metriken verwenden.

   Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch die Aktivität verbessern möchten.

   Der Besucher bleibt nach Erreichen des Ziels in der Aktivität. Der Besucher sieht weiterhin den Aktivitätsinhalt, wird jedoch nicht als neuer Aktivitätseintrag gezählt.

   >[!NOTE]
   >
   >Beim Einrichten einer Aktivität nach der Einrichtung von [!DNL Analytics] als Ihre Berichte-Quelle gibt es keine Möglichkeit, Audiencen für Berichte einzurichten. [!DNL Analytics] Segmente sind im Bericht  [!DNL Target] Aktivitäten verfügbar.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Aktivitäten für A4T und die automatische Zuordnung und automatische Zielgruppe

Weitere Informationen finden Sie unter [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischer Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).