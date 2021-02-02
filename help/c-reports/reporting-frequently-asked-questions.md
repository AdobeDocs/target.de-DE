---
keywords: Fehlerbehebung;Metrikdiskrepanzen;FAQ;Berichte;Neuer Besucher;Neue Besucher;Rückkehrender Besucher;Rückkehrende Besucher;Rückkehrender Besuch;Neuer Besuch
description: Liste der häufig gestellten Fragen zur Berichterstellung in Adobe Target
title: Häufig gestellte Fragen zum Reporting
feature: Reports
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 30%

---


# Häufig gestellte Fragen zum Reporting{#reporting-faq}

Liste der häufig gestellten Fragen zur Berichterstellung in [!DNL Target].

## Wie werden die Metriken &quot;Neue Besucher&quot;und &quot;Wiederkehrende Besucher&quot;gezählt?

Die folgenden Informationen erklären, wie neue Besucher und wiederkehrende Besucher gezählt werden, und zeigen Beispiele dafür, warum die Summe dieser beiden Segmente nicht immer der Gesamtanzahl der Besucher entspricht.

### Neue Besucher

Ein Besucher wird in das Segment Neue Besucher einbezogen, wenn eine der folgenden Bedingungen erfüllt ist:

* Der Besucher besucht die Site zum ersten Mal.
* Der Besucher besucht die Site zum ersten Mal seit dem Löschen von Cookies.
* Der Besucher besucht die Site zum ersten Mal seit Ablauf der Lebensdauer des [Besucher-Profils](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md).

### Zurückkehrende Besucher

Der Besucher wird im Segment &quot;Rückkehrende Besucher&quot;enthalten, wenn der Benutzer die Site zuvor besucht hat, mindestens 30 Minuten lang verlassen hat und mit denselben Cookies erneut zur Site zurückkehrt. Solange ein Besucher innerhalb der Lebensdauer seines Profils zurückkehrt, ist er ein wiederkehrender Besucher.

Angenommen, die Lebensdauer Ihres Profils ist auf 14 Tage eingestellt (Standard). Ein Besucher wird in das Segment &quot;Rückkehrende Besucher&quot;aufgenommen, wenn die folgenden Bedingungen erfüllt sind:

* Ein Besucher besucht die Site zum ersten Mal und wird als neuer Besucher aufgezeichnet.
* Der Besucher verlässt die Site, gibt aber sechs Tage später zurück.

Da die Lebensdauer des Profils auf 14 Tage festgelegt ist, ist dieser Besucher im Segment &quot;Rückkehrende Besucher&quot;enthalten. Beachten Sie, dass, wenn der Besucher innerhalb dieses Zeitraums von sechs Tagen Cookies gelöscht hat, dieser Besucher in das Segment &quot;Neue Besucher&quot;aufgenommen wird.

### Beispiele zur Erklärung von Diskrepanzen zwischen Metrikwerten

**Beispiel 1**: Wenn diese beiden Segmente auf eine Aktivität angewendet werden, ergeben die Segmente &quot;Neue Besucher&quot;und &quot;Wiederkehrende Besucher&quot;nicht immer die Gesamtanzahl der Besucher.

Betrachten Sie das folgende Beispiel unter den oben genannten Bedingungen für neue Besucher und wiederkehrende Besucher:

* Ein Besucher besucht die Site zum ersten Mal und wird als neuer Besucher gezählt.
* Der Besucher kehrt zur Site zurück, nachdem die Bedingungen für wiederkehrende Besucher erfüllt wurden und als wiederkehrender Besucher gezählt wird.

Dieser Besucher wird als ein Besucher in der Gesamtanzahl der Besucher der Aktivität gezählt, auch wenn er sowohl in den Segmenten &quot;Neue Besucher&quot;als auch in den Segmenten &quot;Wiederkehrende Besucher&quot;gezählt wird.

**Beispiel 2**: Diskrepanzen zwischen den Zählungen für neue Besucher und wiederkehrende Besucher hängen auch davon ab, wie Sie die  [Erfolgsmetriken](/help/c-activities/r-success-metrics/success-metrics.md) der Aktivität konfigurieren.

Beispiel:

Eine Reihe neuer Besucher besuchen Ihre Site und sind für eine Aktivität qualifiziert. Diese neuen Besucher werden für das Segment &quot;Neue Besucher&quot;gezählt. Alle diese Besucher verzeichneten auch einen Besuch in dieser Aktivität.

Einige Besucher trafen die Konversionsmetrik, die als &quot;Anzahl erhöhen und Benutzer in Aktivität halten&quot;konfiguriert wurde. Nehmen wir an, dass einige dieser Benutzer die Konversionsmetrik mehrmals treffen, wird die Konversionsmetrik nicht erhöht. Angesichts dieser Konfiguration könnten einige Benutzer jedoch die Konversionsmetrik treffen und dann zur Startseite zurückkehren, wodurch sie sich erneut zur Aktivität berechnen, um einen neuen Besuch aufzuzeichnen.

## Warum enthalten meine [!UICONTROL Erlebnis-Targeting] (XT)-Berichte Metriken für Kontrollerlebnisse?

XT-Aktivitäten sollten immer ein Kontrollerlebnis haben. Wenn Sie eine XT-Aktivität auf ähnliche Weise wie eine [!UICONTROL A/B-Test]-Aktivität verwenden, was ein ziemlich häufiges Szenario ist, sind die Kontrollerlebnisdaten nützlich. Wenn die Kontrollerlebnisdaten in Ihren Berichten nicht nützlich sind, können Sie sie ignorieren.

## Warum ist die Anzahl der Besuche in [!DNL Target] niedriger als in anderen [!DNL Adobe Experience Cloud]-Lösungen? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metrikwerte, beispielsweise Besuche, die von [!DNL Target] angezeigt werden, liegen aus verschiedenen Gründen immer unter den Werten in [!DNL Experience Cloud]-Lösungen:

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

## Warum ist der Traffic zwischen meinen Erlebnissen ungleich in meiner A/B- oder MVT-Aktivität? {#uneven}

So setzte ich die Traffic-Aufteilung auf 50/50 oder 25/25/25/25 ein, sehe aber eine sehr unterschiedliche Verteilung der Erlebnisse im Berichte. Es gibt einige erklärbare Gründe für die ungleichmäßige Anzahl von Besuchern im Berichte [!DNL Target]:

* Wenn eine [!DNL Target]-Aktivität zum ersten Mal gestartet wird, kann die Traffic-Verteilung aufgrund der Edge-Knotenarchitektur, die [!DNL Target] zur Optimierung des Experience Versand verwendet, ungleich sein. Die beste Vorgehensweise ist, einer Aktivität Zeit zur Erhebung zusätzlicher Daten einzuräumen, und die Verteilung normalisiert sich. Weitere Informationen zur Architektur und zu Edge-Knoten finden Sie unter [Funktionsweise von Adobe Target](/help/c-intro/how-target-works.md).[!DNL Adobe Target]
* Wenn Sie sich in [!DNL Target] oder [!DNL Analytics] befinden und die Metrik **[!UICONTROL Besuche]** verwenden, denken Sie daran, dass [!DNL Target] ein Besucher-basiertes System ist und die Traffic-Verteilung für einen A/B- oder MVT-Test auf der Ebene des Besuchers zugewiesen wird. Wenn Sie also die Ergebnisse der Aktivität mit der Metrik **[!UICONTROL Besuche]** untersuchen, kann die Traffic-Verteilung ungleich erscheinen, da bestimmte Besucher möglicherweise mehrere Besuche haben. Besucher ist die standardmäßige Normalisierungsmetrik bei der Bewertung der Aktivität.
* Die beste Methode für A/B- und MVT-Tests besteht darin, Traffic-Aufteilungen gleichmäßig zu halten. Die Änderung der Traffic-Verteilung zwischen Erlebnissen (z. B. 90/10 bis 50/50) während eines Tests kann zu uneinheitlichen Besuchern über Erlebnisse hinweg führen. Das geringere Traffic-Erlebnis wird möglicherweise nie &quot;aufholen&quot;.
* Wenn Sie die oben genannten Best Practices befolgen und sich die Traffic-Aufteilung im Laufe der Zeit nicht normalisiert, sollten Sie Folgendes überprüfen:

   * Verwenden Sie die neueste &quot;at.js&quot;-Bibliothek? Weitere Informationen zur aktuellen Version und den zugehörigen Versionshinweisen finden Sie unter [at.js Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * Ist es ein Umleitungstest? Falsches Timing von Tags, die auf der Seite ausgelöst werden, kann zu ungleichen Traffic-Aufteilungen führen, insbesondere wenn [!DNL Analytics] als Datenquelle für eine [!DNL Target]-Aktivität verwendet wird. Weitere Informationen zur Behebung einer ungleichmäßigen Traffic-Verteilung bei einer Umleitungs-Aktivität mit Analytics für die Zielgruppe (A4T) finden Sie unter [Umleitungs-Angebot - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
