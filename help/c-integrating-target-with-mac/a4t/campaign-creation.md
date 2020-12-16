---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: Sie können eine Aktivität in Target Standard/Premium erstellen, um Adobe Analytics als Berichtsquelle (A4T) zu verwenden.
title: Erstellen einer Aktivität, die A4T als Berichte-Quelle verwendet
feature: a4t general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 18%

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

## Unterstützung von Analytics für Zielgruppe (A4T) für Aktivitäten mit automatisierter Zuordnung und automatischer Zielgruppe {#a4t-aa}

Die Adobe Target-zu-Adobe Analytics-Integration, auch [Analytics for Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md) genannt, wurde aktualisiert. Aktivitäten für die automatische Zuordnung und automatische Zielgruppe unterstützen jetzt Analytics für die Zielgruppe.

Diese Integration ermöglicht Ihnen Folgendes:

* Verwenden Sie die Multi-Armed Bandit-Funktion von [Automatisierte Zuordnung](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), um Traffic zu erfolgreichsten Erlebnissen zu fördern.
* Verwenden Sie den Algorithmus zum Lernen von Ensemble-Maschinen von [Auto-Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md), um ein optimales Erlebnis für jeden Besucher basierend auf Profil, Verhalten und Kontext auszuwählen, während Sie eine [!DNL Adobe Analytics]-Zielmetrik und die [!DNL Adobe Analytics]’ Rich-Berichte- und Analyse-Funktionen verwenden.

Vergewissern Sie sich, dass Sie [A4T für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben. Wenn Sie `analyticsLogging = client_side` verwenden, müssen Sie auch den Wert `sessionId` an [!DNL Analytics] übergeben. Weitere Informationen finden Sie unter [Analytics for Zielgruppe (A4T) Berichte](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) im Handbuch *Adobe Target SDKs*.

Erster Schritt:

1. Wählen Sie beim Erstellen einer A/B-Test-Aktivität auf der Seite **[!UICONTROL Targeting]** eine der folgenden Optionen als **[!UICONTROL Traffic-Zuordnungsmethode]**:

   * Automatische Zuordnung zu bestem Erlebnis
   * Automatische Zielgruppe für personalisierte Erlebnisse

1. Wählen Sie **[!UICONTROL Adobe Analytics]** für Ihre **[!UICONTROL Berichte-Quelle]** auf der Seite **[!UICONTROL Ziele und Einstellungen]** und wählen Sie die Report Suite aus, die Ihrem gewünschten Optimierungsziel entspricht.

1. Wählen Sie eine Metrik für das Primär-Ziel.

   * Wählen Sie **[!UICONTROL Konversion]**, um [!DNL Adobe Target] zum Festlegen des Optimierungsziels zu verwenden.
   * Wählen Sie **[!UICONTROL Verwenden Sie eine Analytics-Metrik]** und wählen Sie dann eine Metrik aus [!DNL Analytics] zur Verwendung als Optimierungsziel. Sie können eine vordefinierte [!DNL Analytics]-Konversionsmetrik oder ein benutzerdefiniertes [!DNL Analytics]-Ereignis verwenden.

1. Speichern und aktivieren Sie Ihre Aktivität.

   [!UICONTROL Die automatische ] Zuordnung verwendet Ihre ausgewählte Metrik, um die Aktivität zu optimieren, wodurch Besucher zu dem Erlebnis geleitet werden, das Ihre Zielmetrik maximiert.

   Oder

   [!UICONTROL Auto-] Targeting verwendet Ihre ausgewählte Metrik zur Optimierung der Aktivität, wodurch Besucher zu einem personalisierten besten Erlebnis werden.

1. Verwenden Sie die Registerkarte **[!UICONTROL Berichte]**, um den Berichte Ihrer Aktivität nach Ihrer Auswahl von [!DNL Adobe Analytics]-Metriken Ansicht. Klicken Sie auf **[!UICONTROL Ansicht in Analytics]**, um tief zu tauchen und Ihre Berichte-Daten weiter zu segmentieren.

### Unterstützte Zielmetriken

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] TargetingWählen Sie einen der folgenden Metriktypen als primäre Zielmetrik für die Optimierung:

* [!DNL Adobe Target] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] Konversionsmetriken vorstellen
* [!DNL Adobe Analytics] benutzerspezifische Ereignisse

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targeting erfordert die Auswahl einer Metrik, die auf einem binomialen Ereignis basiert, d. h. einem Ereignis, das entweder passiert oder nicht, z. B. ein Klick, eine Konversion, eine Bestellung usw. (Diese Ereignisse werden manchmal auch als Bernoulli-, Binär- oder diskrete Ereignis bezeichnet.)

[!UICONTROL A4] Tfor  [!UICONTROL Auto-] Zuordnung und  [!UICONTROL Auto-] Targeting unterstützen keine Optimierung für kontinuierliche Metriken wie Umsatz, Anzahl der bestellten Produkte, Sitzungsdauer, Anzahl der Ansichten während der Sitzung usw. (Diese nicht unterstützten Metriktypen werden manchmal auch als nicht-binomielle oder nicht-Bernoulli-Metriken bezeichnet.)

Die folgenden Metriktypen werden nicht als primäre Zielmetriken unterstützt:

* [!DNL Adobe Target] Interaktions- und Umsatzmetriken
* [!DNL Adobe Analytics] Interaktions- und Umsatzmetriken

   Es ist möglicherweise möglich, eine [!DNL Analytics]-Interaktions- oder Umsatzmetrik als primäre Zielmetrik auszuwählen, da [!DNL Target] nicht alle Interaktions- und Umsatzmetriken von [!DNL Analytics] identifizieren und ausschließen kann. Gehen Sie vorsichtig vor, um nur binomielle Konversionsmetriken oder benutzerdefinierte Ereignis von [!DNL Analytics] auszuwählen.

* [!DNL Adobe Analytics] berechnete Metriken

### Einschränkungen und Hinweise

Einige Einschränkungen und Hinweise gelten für die automatische Zuordnung und die automatische Zielgruppe. Andere Einschränkungen und Hinweise gelten für die eine oder andere Aktivität.

#### Automatische Zuordnung und Zielgruppe

* Die Quelltexte des Berichte können nicht von [!DNL Analytics] in [!DNL Target] oder umgekehrt geändert werden, nachdem eine Aktivität aktiviert wurde.
* Obwohl errechnete Metriken nicht als primäre Zielmetriken unterstützt werden, ist es oft möglich, das angestrebte Ergebnis zu erzielen, indem Sie stattdessen ein benutzerdefiniertes Ereignis als primäre Zielmetrik auswählen. Wenn Sie z. B. eine Metrik wie &quot;Formularabschlüsse pro Besucher&quot;optimieren möchten, wählen Sie ein benutzerdefiniertes Ereignis, das &quot;Formularabschlüsse&quot;als primäre Zielmetrik entspricht. [!DNL Target] normalisiert Konversionsmetriken automatisch pro Besuch, um eine ungleiche Traffic-Verteilung zu berücksichtigen. Daher ist es nicht erforderlich, eine berechnete Metrik für die Normalisierung zu verwenden.
* [!DNL Target] verwendet das Zuordnungsmodell &quot;Same Touch&quot;in der Implementierung von  [!UICONTROL Auto-] AllocationA4T.

#### Automatische Zuordnung

* [!UICONTROL Auto-] Allocatemodels trainieren wie gewohnt alle zwei Stunden.

#### Automatisches Targeting

* [!UICONTROL Auto-] Targeting-Modelle werden weiterhin alle 24 Stunden trainiert, wie üblich. Konversionsdaten von [!DNL Analytics] werden jedoch um weitere sechs bis 24 Ereignis verzögert. Diese Verzögerung bedeutet, dass die Verteilung des Traffics durch [!DNL Target] die neuesten Ereignis verfolgt, die in [!DNL Analytics] aufgezeichnet wurden. Dies wird die größte Wirkung in den ersten 48 Stunden nach dem ersten Aktivieren einer Aktivität haben. Die Performance der Aktivität spiegelt das Umrechnungsverhalten nach Ablauf von fünf Tagen stärker wider. [!DNL Analytics] Sie sollten die Verwendung von [!UICONTROL Automatisierte Zuordnung] anstelle von [!UICONTROL Automatische Zielgruppe] für Aktivitäten mit kurzer Dauer in Erwägung ziehen, bei denen der meisten Traffic innerhalb der ersten fünf Lebensjahre der Aktivität auftritt.
* Wenn [!DNL Analytics] als Datenquelle für eine [!UICONTROL Auto-Zielgruppe]-Aktivität verwendet wird, gelten Sitzungen als beendet, nachdem sechs Stunden abgelaufen sind. Konversionen, die nach sechs Stunden auftreten, werden nicht gezählt.

Weitere Informationen finden Sie unter [Zuordnungsmodelle und Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html) im *Analytics-Tools-Handbuch*.
