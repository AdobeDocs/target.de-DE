---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie eine Aktivität in Adobe konfigurieren [!DNL Target] , der Adobe Analytics als Berichtsquelle verwendet (A4T).
title: Wie erstelle ich eine Aktivität, die A4T verwendet?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 36%

---

# Erstellen einer Aktivität mit Analytics als Berichtsquelle

Sie können eine Aktivität in [!DNL Adobe Target] zur Verwendung [!DNL Adobe Analytics] als Berichtsquelle (A4T).

Bevor Sie eine Aktivität einrichten, die [!DNL Analytics] als Berichtsquelle festlegen, legen Sie das Ziel für die Aktivität fest, z. B. die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Sie können zwar jederzeit weitere Metriken auswählen in [!DNL Analytics]müssen Sie weiterhin eine bestimmte Metrik angeben, auf die sich dieser Test voraussichtlich auswirken wird.

## Erstellen Sie die Aktivität

Erstellen einer [!DNL Target] -Aktivität, die [!DNL Analytics] da die Berichtsquelle der Einrichtung einer regulären [!DNL Target] -Aktivität mit einigen wichtigen Unterschieden. Beispielsweise können Sie beim Erstellen der Aktivität kein Segment für die Berichterstellung auswählen, da alle in verfügbaren Segmente [!DNL Analytics] kann bei der Anzeige eines Berichts angewendet werden.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >Der Aktivitätsname darf das Zeichen &quot;%&quot;nicht enthalten, wenn [!DNL Analytics] wird als Berichtsquelle verwendet.

1. Wählen Sie den Aktivitätstyp aus und beginnen Sie mit der Einrichtung der Aktivität.

   Wenn Sie eine [!UICONTROL Automatische Zuordnung] oder [!UICONTROL Automatisches Targeting] -Aktivität, siehe [A4T-Unterstützung für Aktivitäten mit automatischer Zuordnung und automatischem Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) für weitere Informationen.

1. Wählen Sie in den **[!UICONTROL Einstellungen]** für die Aktivität **[!UICONTROL Adobe Analytics]** aus und geben Sie Ihr Unternehmen an.
1. Wählen Sie eine Report Suite aus.

   Sie können eine beliebige Report Suite auswählen, die in [!DNL Analytics]. Die Report Suite definiert, wo die erfassten Daten verfügbar sind. Virtuelle Report Suites werden nicht in der Liste der Report Suites aufgeführt.

   Beim Auswählen der Report Suite kann es vorkommen, dass Ihnen zwei Fehler gemeldet werden:

   * Sie erhalten die Fehlermeldung, dass keine Report Suites verfügbar sind, obwohl Ihr Konto korrekt eingerichtet ist.

      Überprüfen Sie Ihre [!DNL Analytics] Unternehmen. Wenn [!DNL Adobe Experience Cloud] -Konto an mehrere [!DNL Analytics] Unternehmen, abmelden von [!DNL Target]und melden Sie sich bei an [!DNL Analytics] unter der richtigen Firma. Kehren Sie dann zu [!DNL Target]und die Report Suites geladen werden.

   * Ihnen wird nicht die Report Suite angezeigt, die Sie erwartet haben.

      Nur Report Suites, für die eine Verbindung hergestellt wurde [!DNL Target] zur Auswahl verfügbar sind. Wenn die erwarteten Report Suites nicht angezeigt werden, melden Sie sich zunächst ab und melden Sie sich wieder bei der [!DNL Adobe Experience Cloud] erneut versuchen.
   Wenn noch eine oder mehrere Report Suites in der Liste fehlen, geben Sie bitte an, [Kundenunterstützung kontaktieren](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Legen Sie den Trackingserver fest.

   Siehe [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definieren Sie das Erlebnis.
1. Legen Sie das Aktivitätsziel fest.

   Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können beliebige [!DNL Analytics] Metrik verfügbar in der [!DNL Analytics] Metrikauswahl.

   >[!NOTE]
   >
   >Sie können eine benutzerspezifische Target-basierte Metrik an senden [!DNL Analytics] anstatt sich nur auf [!DNL Analytics] Daten. Sie können beispielsweise das Klicken auf eine Seite überwachen, was normalerweise nicht von [!DNL Analytics]. Diese benutzerdefinierte Metrik wird an [!DNL Analytics] automatisch aus dem [!DNL Target] und wird als[!DNL Target] Konversionsmetrik in der Metrikauswahl in [!DNL Analytics]. Die [!DNL Target] Die Konversionsmetrik ist leer, wenn Sie [!DNL Analytics] Metriken.

   Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch die Aktivität verbessern möchten.

   Der Besucher bleibt nach Erreichen des Ziels in der Aktivität. Der Besucher sieht weiterhin den Aktivitätsinhalt, wird jedoch nicht als neuer Aktivitätseintrag gezählt.

   >[!NOTE]
   >
   >Beim Einrichten einer Aktivität nach der Einrichtung [!DNL Analytics] als Berichtsquelle angeben, gibt es keine Möglichkeit, Zielgruppen für die Berichterstellung einzurichten. [!DNL Analytics] -Segmente sind im Abschnitt [!DNL Target] Aktivitätsbericht.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## A4T- und Automatisierte Zuordnung- und Automatisches Targeting-Aktivitäten

Weitere Informationen finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
