---
description: Sie können eine Aktivität in Target Standard/Premium erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
keywords: a4t; A4T; Analytics als Berichtsquelle für Target
seo-description: Sie können eine Aktivität in Target Standard/Premium erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
seo-title: Aktivitätserstellung
solution: Target
title: Aktivitätserstellung
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: e69d746b9705670042b3c6718b3357c9d1aaf650

---


# Aktivitätserstellung{#activity-creation}

Sie können eine Aktivität in Target Standard/Premium erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.

Bevor Sie eine Aktivität einrichten, die Analytics als Berichtsquelle verwendet, müssen Sie das Ziel für die Aktivität festlegen, beispielsweise die Verbesserung des Umsatzes pro Besucher (RPV) oder die Erhöhung der Klicks auf Ihren Warenkorb. Wählen Sie eine finale Erfolgsmetrik für die Aktivität aus. Auch wenn Sie jederzeit zusätzliche Metriken in Analytics auswählen können, müssen Sie trotzdem eine bestimmte Metrik angeben, auf die dieser Test erwartungsgemäß Auswirkungen hat.

Das Erstellen einer Target Standard-Aktivität, die Analytics als Berichtsquelle verwendet, ähnelt dem Einrichten einer regulären Target Standard-Aktivität - mit einigen wesentlichen Unterschieden. Sie können beispielsweise während des Erstellens der Aktivität kein Segment für die Berichterstellung auswählen, da alle in Analytics verfügbaren Segmente beim Anzeigen eines Berichts angewendet werden können.

1. Klicken Sie auf **[!UICONTROL Aktivität erstellen]**.

   >[!NOTE]
   >
   >Wenn Analytics als Berichtsquelle verwendet wird, darf der Aktivitätsname das Zeichen „%“ nicht enthalten.

1. Wählen Sie den Aktivitätstyp aus und beginnen Sie mit der Einrichtung der Aktivität.
1. Wählen Sie in den **[!UICONTROL Einstellungen]** für die Aktivität **[!UICONTROL Adobe Analytics]** aus und geben Sie Ihr Unternehmen an.
1. Wählen Sie eine Report Suite aus.

   Sie können eine beliebige Report Suite auswählen, die in Adobe Analytics verfügbar ist. Die Report Suite definiert, wo die erfassten Daten verfügbar sind. Virtuelle Report Suites werden nicht in der Liste der Report Suites aufgeführt.

   Beim Auswählen der Report Suite kann es vorkommen, dass Ihnen zwei Fehler gemeldet werden:

   * Sie erhalten die Fehlermeldung, dass keine Report Suites verfügbar sind, obwohl Ihr Konto korrekt eingerichtet ist.
   Vielleicht sollten Sie Ihr Analytics-Unternehmen überprüfen. Wenn Ihr Experience Cloud-Konto mit mehr als einem Analytics-Unternehmen verknüpft ist, müssen Sie sich bei Target abmelden und mit dem richtigen Unternehmen bei Analytics anmelden. Kehren Sie dann zu Target zurück, und die Report Suites werden geladen.

   * Ihnen wird nicht die Report Suite angezeigt, die Sie erwartet haben.
   Es stehen nur Report Suites, die für die Verbindung mit Adobe Target bereitgestellt werden, zur Auswahl zur Verfügung. Wenn nicht die erwarteten Report Suites angezeigt werden, versuchen Sie, sich bei Adobe Experience Cloud ab- und dann wieder anzumelden, und wiederholen Sie den Vorgang.

   Wenn die Report Suite(s) weiterhin nicht in der Liste zu finden ist/sind, [wenden Sie sich an den Kundendienst](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
1. Legen Sie den Trackingserver fest.

   Siehe [Verwenden eines Analytics-Tracking-Servers](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definieren Sie das Erlebnis.
1. Legen Sie das Aktivitätsziel fest.

   Sie müssen eine Erfolgsmetrik als zu verwendendes Ziel für jeden Test festlegen. Ihr Aktivitätsziel ist die Konversionsaktivität, die eine erfolgreiche Aktivität signalisiert. Die Best Practice ist, niemals einen Test ohne ein Ziel durchzuführen, das auf eine bestimmte Art und Weise verbessert werden soll. Sie können sämtliche in der Metrikauswahl von Analytics verfügbaren Analytics-Metriken auswählen.

   >[!NOTE]
   >
   >Sie können eine benutzerdefinierte Target-basierte Metrik an Analytics senden, statt sich nur auf Analytics-Daten zu stützen. Sie können beispielsweise das Klicken auf eine Seite überwachen, was in der Regel nicht von Analytics verfolgt wird. Die benutzerdefinierte Metrik wird automatisch vom Target-Server an Analytics gesendet und wird als „Target-Konversions“-Metrik in der Metrikauswahl in Analytics angezeigt. Wenn Sie sich für die Verwendung von Analytics-Metriken entscheiden, ist die Metrik Target-Konversion leer.

   Das Einrichten eines Ziels hindert Sie nicht daran, eine andere Metrik beim Bewerten der Testergebnisse zu verwenden. Das Ziel ist jedoch eine Erinnerung an den einen Aspekt, den Sie durch die Aktivität verbessern möchten.

   Der Besucher bleibt nach Erreichen des Ziels in der Aktivität. Der Besucher sieht weiterhin den Aktivitätsinhalt, wird jedoch nicht als neuer Aktivitätseintrag gezählt.

   >[!NOTE]
   >
   >Wenn Sie eine Aktivität einrichten, nachdem Sie Analytics als Berichtsquelle festgelegt haben, gibt es keine Möglichkeit, Zielgruppen für die Berichterstellung festzulegen. Analytics-Segmente sind in den Target Activities-Berichten verfügbar.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

