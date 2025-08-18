---
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
description: Erfahren Sie, wie Sie eine Aktivität in Adobe [!DNL Target]  konfigurieren, die Adobe Analytics als Berichtsquelle (A4T) verwendet.
title: Wie erstelle ich eine Aktivität, die A4T verwendet?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 28%

---

# Erstellen einer Aktivität mit Analytics als Berichtsquelle

Sie können eine Aktivität in [!DNL Adobe Target] so konfigurieren, dass [!DNL Adobe Analytics] als Berichtsquelle (A4T) verwendet wird.

Bevor Sie eine Aktivität einrichten, die [!DNL Analytics] als Berichtsquelle verwendet, legen Sie das Ziel der Aktivität fest, z. B. die Steigerung des Umsatzes pro Besucher (Revenue per Visitor, RPV) oder die Steigerung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Sie können in [!DNL Analytics] zwar jederzeit weitere Metriken auswählen, müssen aber dennoch eine bestimmte Metrik angeben, auf die sich dieser Test voraussichtlich auswirken wird.

## Erstellen der Aktivität

Das Erstellen einer [!DNL Target] Aktivität, die [!DNL Analytics] als Berichtsquelle verwendet, ähnelt dem Einrichten einer regulären [!DNL Target] Aktivität, mit einigen wichtigen Unterschieden. Sie können beispielsweise beim Erstellen der Aktivität kein Segment für das Reporting auswählen, da alle in [!DNL Analytics] verfügbaren Segmente beim Anzeigen eines Berichts angewendet werden können.

1. Klicken Sie auf **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Ein Aktivitätsname darf nicht das Zeichen &quot;%&quot; enthalten, wenn [!DNL Analytics] als Berichtsquelle verwendet wird.
   >
   >Verwenden Sie nicht denselben Aktivitätsnamen für zwei Aktivitäten aus separaten [Arbeitsbereichen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) die A4T-Berichte verwenden.

1. Wählen Sie den Aktivitätstyp aus und beginnen Sie mit der Einrichtung der Aktivität.

   Wenn Sie eine [!UICONTROL Auto-Allocate]- oder [!UICONTROL Auto-Target]-Aktivität erstellen möchten, finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) weitere Informationen.

1. Wenn Sie zum **[!UICONTROL Settings]** Teil des Arbeitsablaufs für die Aktivitätserstellung gelangen, wählen Sie **[!UICONTROL Adobe Analytics]** und geben Sie Ihr Unternehmen an.
1. Wählen Sie eine Report Suite aus.

   Sie können jede Report Suite auswählen, die Ihnen in [!DNL Analytics] zur Verfügung steht. Die Report Suite definiert, wo die erfassten Daten verfügbar sind. Virtual Report Suites sind nicht in der Report Suite-Liste enthalten.

   Beim Auswählen der Report Suite kann es vorkommen, dass Ihnen zwei Fehler gemeldet werden:

   * Sie erhalten die Fehlermeldung, dass keine Report Suites verfügbar sind, obwohl Ihr Konto korrekt eingerichtet ist.

     Überprüfen Sie Ihre [!DNL Analytics]. Wenn Ihr [!DNL Adobe Experience Cloud]-Konto mit mehr als einem [!DNL Analytics] Unternehmen verknüpft ist, melden Sie sich von [!DNL Target] ab und melden Sie sich unter dem richtigen Unternehmen bei [!DNL Analytics] an. Kehren Sie dann zu [!DNL Target] zurück, und die Report Suites werden geladen.

   * Ihnen wird nicht die Report Suite angezeigt, die Sie erwartet haben.

     Es stehen nur Report Suites zur Auswahl, die für die Verbindung mit [!DNL Target] bereitgestellt wurden. Wenn die erwarteten Report Suites nicht angezeigt werden, versuchen Sie zunächst, sich abzumelden und sich wieder bei der [!DNL Adobe Experience Cloud] anzumelden, um es dann erneut zu versuchen.

   Wenn eine oder mehrere Report Suites noch in der Liste fehlen, wenden Sie sich [an die Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Legen Sie den Trackingserver fest.

   Siehe [Verwenden eines Analytics-Tracking-Servers](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definieren Sie das Erlebnis.
1. Legen Sie das Aktivitätsziel fest.

   Sie müssen eine Erfolgsmetrik auswählen, die als Ziel für jede Aktivität verwendet werden soll. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können jede [!DNL Analytics] Metrik auswählen, die im [!DNL Analytics] Metrikselektor verfügbar ist.

   >[!NOTE]
   >
   >Sie können eine benutzerdefinierte Target-basierte Metrik an [!DNL Analytics] senden, anstatt sich nur auf [!DNL Analytics] Daten zu verlassen. Sie können beispielsweise das Klicken auf eine Seite überwachen, was von [!DNL Analytics] normalerweise nicht verfolgt wird. Diese benutzerdefinierte Metrik wird vom [!DNL Analytics]-Server automatisch an [!DNL Target] gesendet und in der Metrikauswahl in [!DNL Target] als Metrik &quot;[!DNL Analytics] Conversion“ angezeigt. Die [!DNL Target] Konversionsmetrik ist leer, wenn Sie [!DNL Analytics] verwenden möchten.

   Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch die Aktivität verbessern möchten.

   Der Besucher bleibt nach Erreichen des Ziels in der Aktivität. Der Besucher sieht weiterhin den Aktivitätsinhalt, wird jedoch nicht als neuer Aktivitätseintrag gezählt.

   >[!NOTE]
   >
   >Beim Einrichten einer Aktivität nach der Einrichtung von [!DNL Analytics] als Berichtsquelle gibt es keine Option zum Einrichten von Zielgruppen für das Reporting. [!DNL Analytics] Segmente sind im Bericht [!DNL Target] verfügbar.

1. Klicken Sie auf **[!UICONTROL Save]**.

## A4T- und automatische Zuordnungs- und automatische Targeting-Aktivitäten

Weitere Informationen finden Sie unter [A4T-Unterstützung für automatische Zuordnungs- und automatische Targeting-Aktivitäten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
