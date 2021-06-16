---
keywords: Fehlerbehebung; Metrikdiskrepanzen; FAQ; Berichte; neuer Besucher; neue Besucher; wiederkehrende Besucher; wiederkehrende Besucher; wiederkehrende Besucher; erneuter Besuch; neuer Besuch
description: Erkunden Sie eine Liste häufig gestellter Fragen und Antworten zur Berichterstellung für Adobe [!DNL Target] .
title: Wo finde ich Antworten auf Fragen zu [!DNL Target] Berichten?
feature: Berichte
exl-id: 1a345a67-5050-4bd3-858d-99731d2c1dd3
source-git-commit: c0eae79da63e2f269f603b4d9fd2a5a1170e2687
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 33%

---

# Häufig gestellte Fragen zum Reporting

Liste der häufig gestellten Fragen zur Berichterstellung in [!DNL Adobe Target].

## Wie werden die Metriken „Neue Besucher“ und „Wiederkehrende Besucher“ gezählt? {#methodology}

Der erste Besuch eines neuen Besuchers dauert so lange an, wie der Besucher auf der Site aktiv ist.
Wenn der Benutzer 30 Minuten oder länger inaktiv ist, wird die Sitzung zurückgesetzt. Das Zurücksetzen der Sitzung bedeutet, dass dieser Besucher beim nächsten Besuch zum rückkehrenden Besucher wird oder nach 30 Minuten Inaktivität wieder aktiv wird.
Wenn sich der Besucher alle 29 Minuten an einem ganzen Tag um die Site bewegt, wird dieser Besucher an diesem ganzen Tag als neuer Besucher gezählt. Die Sitzung wurde nie zurückgesetzt, da der Besucher nie den Schwellenwert von 30 Minuten überschritten hat.

In den folgenden Informationen wird ausführlicher erläutert, wie neue Besucher und wiederkehrende Besucher gezählt werden. Es werden auch Beispiele aufgeführt, die erklären, warum die Summe dieser beiden Segmente nicht immer der Gesamtzahl der Besucher entspricht.

### Neue Besucher

Ein Besucher wird dem Segment „Neue Besucher“ hinzugefügt, wenn eine der folgenden Bedingungen zutrifft:

* Der Besucher besucht die Site zum ersten Mal.
* Der Besucher besucht die Site zum ersten Mal seit dem Löschen seiner Cookies.
* Der Besucher besucht die Site zum ersten Mal seit dem Ablauf der [Lebensdauer seines Besucherprofils](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md).

### Zurückkehrende Besucher

Ein Besucher wird dem Segment „ Wiederkehrende Besucher“ hinzugefügt, wenn der Besucher die Site bereits besucht hatte, sie jedoch für mindestens 30 Minuten verlassen hat und später mit denselben Cookies zur Site zurückgekehrt ist. Solange ein Besucher innerhalb der Lebensdauer seines Profils zurückkehrt, ist er ein wiederkehrender Besucher.

Angenommen, die Profillebensdauer beträgt 14 Tage (Standardeinstellung). Ein Besucher wird in das Segment Wiederkehrende Besucher aufgenommen, wenn die folgenden Bedingungen erfüllt sind:

* Ein Besucher besucht die Site zum ersten Mal und wird als neuer Besucher aufgezeichnet.
* Der Besucher verlässt die Site, gibt aber sechs Tage später zurück.

Da die Profillebensdauer auf 14 Tage festgelegt ist, ist dieser Besucher im Segment Wiederkehrende Besucher enthalten. Wenn der Besucher innerhalb dieses Zeitraums von sechs Tagen Cookies gelöscht hat, wird dieser Besucher in das Segment &quot;Neue Besucher&quot;aufgenommen.

### Beispiele, die Diskrepanzen zwischen Metrikzahlen erklären

**Beispiel 1**: Wenn diese beiden Segmente auf eine Aktivität angewendet werden, ergeben das Segment &quot;Neue Besucher&quot;und das Segment &quot;Wiederkehrende Besucher&quot;nicht immer die Gesamtanzahl der Besucher.

Betrachten Sie das folgende Beispiel, indem Sie die oben genannten Bedingungen für neue Besucher und wiederkehrende Besucher berücksichtigen:

* Ein Besucher besucht die Site zum ersten Mal und wird als neuer Besucher gezählt.
* Der Besucher kehrt zur Site zurück, nachdem die Bedingungen für wiederkehrende Besucher erfüllt wurden und er als wiederkehrender Besucher gezählt wird.

Dieser Besucher wird in der gesamten Besucherzahl der Aktivität als einzelner Besucher gezählt, auch wenn er sowohl in den Segmenten &quot;Neue Besucher&quot;als auch &quot;Wiederkehrende Besucher&quot;gezählt wird.

**Beispiel 2**: Diskrepanzen zwischen den Zahlen für neue Besucher und wiederkehrende Besucher hängen auch davon ab, wie Sie die  [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md) der Aktivität konfigurieren.

Beispiel:

Mehrere neue Besucher besuchen Ihre Site und sind für eine Aktivität qualifiziert. Diese neuen Besucher werden für das Segment &quot;Neue Besucher&quot;gezählt. Alle diese Besucher verzeichneten auch einen Besuch in dieser Aktivität.

Einige Besucher treffen die Konversionsmetrik, die als &quot;Anzahl erhöhen und Benutzer in Aktivität belassen&quot;konfiguriert wurde. Angenommen, einige dieser Benutzer treffen die Konversionsmetrik mehrmals, erhöht sich die Konversionsmetrik nicht. Bei dieser Konfiguration können jedoch einige Benutzer die Konversionsmetrik erreichen und dann zurück zur Startseite navigieren, wodurch sie sich erneut in die Aktivität qualifizieren, um einen neuen Besuch aufzuzeichnen.

## Warum enthalten meine [!UICONTROL Erlebnis-Targeting] (XT)-Berichte Metriken für Kontrollerlebnisse?

XT-Aktivitäten sollten immer ein Kontrollerlebnis haben. Wenn Sie eine XT-Aktivität auf ähnliche Weise wie eine [!UICONTROL A/B-Test]-Aktivität verwenden, was ein ziemlich häufiges Szenario ist, sind die Kontrollerlebnisdaten nützlich. Wenn die Kontrollerlebnisdaten in Ihren Berichten nicht nützlich sind, können Sie sie ignorieren.

## Warum ist die Anzahl der Besuche in [!DNL Target] niedriger als in anderen [!DNL Adobe Experience Cloud]-Lösungen? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metrikwerte, beispielsweise Besuche, die von [!DNL Target] gemeldet werden, liegen aus verschiedenen Gründen immer unter den gemeldeten Zahlen in anderen [!DNL Experience Cloud]-Lösungen:

* [!DNL Target] zählt nur die Besuche von Besuchern, die für die Aktivität qualifiziert sind. In anderen Lösungen werden Besuche für Besucher angezeigt, die die Seite aufrufen, unabhängig davon, durch welche Aktivität sie auf die Seite gelangt sind.
* Möglicherweise führen unterschiedliche Aktivitäten zum gleichen Ort (diese Aktivitäten schließen sich gegenseitig aus). Somit werden Besuchern auf einer Webseite verschiedene Inhalte angezeigt, was sich auf die in [!DNL Target] registrierten Metrikwerte auswirkt.

## Warum stehen für meinen Aktivitätsbericht keine Daten zur Verfügung? {#section_E4722F6445884130951DF79981C8289B}

Wurde der Inhalt einer Aktivität den Benutzern erfolgreich bereitgestellt, enthält der zugehörige Bericht jedoch keine Daten, stellen Sie sicher, dass in den Berichtseinstellungen die korrekte Umgebung ([Hostgruppe](/help/administrating-target/hosts.md)) ausgewählt wurde.

Sollten Sie eine Entwicklungsumgebung ausgewählt haben, wird möglicherweise folgende Fehlermeldung ausgegeben: „Es sind keine Daten für die ausgewählten Berichtseinstellungen vorhanden.“

So ändern Sie die Umgebung für einen Aktivitätsbericht:

1. Klicken Sie auf **[!UICONTROL Aktivitäten]**, wählen Sie die gewünschte Aktivität aus der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Berichte.]**
1. Klicken Sie auf das Zahnradsymbol, um die Berichtseinstellungen zu bearbeiten.

   ![Dialogfeld für A/B-Einstellungen](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >Das Zahnradsymbol steht nicht für Berichte zur [!UICONTROL automatisierten Personalisierung] zur Verfügung.

1. Wählen Sie in der **[!UICONTROL Umgebung]** die Option **[!UICONTROL Produktion]** aus.

   Möglicherweise stehen Berichtsdaten bei Auswahl einer Entwicklungsumgebung nicht zur Verfügung.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Weitere Informationen zu Umgebungen finden Sie unter [Hosts](/help/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

## Warum unterscheidet sich der Traffic zwischen meinen Erlebnissen in meiner A/B- oder MVT-Aktivität? {#uneven}

Ich setze beispielsweise die Traffic-Aufspaltung auf 50/50 oder 25/25/25/25, sehe aber eine sehr unterschiedliche Verteilung zwischen Erlebnissen in der Berichterstellung. Es gibt mehrere erklärbare Gründe für ungleiche Besucherzahlen in [!DNL Target] Berichten:

* Wenn eine [!DNL Target] -Aktivität zum ersten Mal gestartet wird, kann die Traffic-Verteilung aufgrund der Edge-Knotenarchitektur, die [!DNL Target] verwendet, um die Bereitstellung von Erlebnissen zu optimieren, uneinheitlich sein. Es empfiehlt sich, einer Aktivität Zeit zu geben, mehr Daten zu sammeln, und die Verteilung normalisiert sich. Weitere Informationen zur Architektur von [!DNL Adobe Target] und Edge-Knoten finden Sie unter [Funktionsweise von Adobe Target](/help/c-intro/how-target-works.md).
* Wenn Sie sich in [!DNL Target] oder [!DNL Analytics] befinden und die Metrik **[!UICONTROL Besuche]** verwenden, denken Sie daran, dass [!DNL Target] ein besucherbasiertes System ist und die Traffic-Verteilung für einen A/B- oder MVT-Test auf Besucherebene zugewiesen wird. Wenn Sie also Aktivitätsergebnisse mit der Metrik **[!UICONTROL Besuche]** untersuchen, kann die Traffic-Verteilung ungleichmäßig erscheinen, da bestimmte Besucher möglicherweise mehrere Besuche haben. Besucher ist die standardmäßige Normalisierungsmetrik bei der Bewertung der Aktivitätsleistung.
* Die Best Practice für A/B- und Multivarianz-Tests besteht darin, Traffic-Aufteilungen gleichmäßig zu halten. Die Änderung der Traffic-Verteilung zwischen Erlebnissen (z. B. zwischen 90/10 und 50/50) während eines Tests kann zu uneinheitlichen Besuchern über Erlebnisse hinweg führen. Das niedrigere Traffic-Erlebnis wird möglicherweise nie &quot;aufholen&quot;.
* Wenn Sie die oben genannten Best Practices befolgen und sich die Traffic-Aufspaltung im Laufe der Zeit nicht normalisiert, sollten Sie Folgendes überprüfen:

   * Verwenden Sie die neueste at.js-Bibliothek? Weitere Informationen zur aktuellen Version und den zugehörigen Versionshinweisen finden Sie unter [at.js-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * Ist dies ein Umleitungstest? Eine fehlerhafte Timing von Tags, die auf der Seite ausgelöst werden, kann zu ungleichen Traffic-Aufspaltungen führen, insbesondere bei der Verwendung von [!DNL Analytics] als Datenquelle für eine [!DNL Target] -Aktivität. Weitere Informationen zum Beheben einer ungleichmäßigen Traffic-Verteilung bei einer Umleitungsaktivität mit Analytics for Target (A4T) finden Sie unter [Umleitungsangebote - A4T-FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
