---
keywords: Fehlerbehebung;Metrik-Diskrepanzen;FAQ;Berichte;neuer Besucher;neue Besucher;wiederkehrender Besucher;wiederkehrende Besucher;wiederkehrender Besuch;neuer Besuch
description: Hier finden Sie eine Liste häufig gestellter Fragen und Antworten zum Adobe- [!DNL Target] .
title: Wo finde ich Antworten auf Fragen zum  [!DNL Target] ?
feature: Reports
exl-id: 1a345a67-5050-4bd3-858d-99731d2c1dd3
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 20%

---

# Häufig gestellte Fragen zum Reporting

Liste der häufig gestellten Fragen zur Berichterstellung in [!DNL Adobe Target].

## Wie werden die Metriken „Neue Besucher“ und „Wiederkehrende Besucher“ gezählt? {#methodology}

Der erste Besuch eines neuen Besuchers dauert so lange, wie der Besucher auf der Website aktiv ist.
Wenn der Benutzer 30 Minuten oder länger inaktiv ist, wird die Sitzung zurückgesetzt. Das Zurücksetzen der Sitzung bedeutet, dass dieser Besucher beim nächsten Besuch zu einem wiederkehrenden Besucher wird oder nach 30 Minuten Inaktivität wieder aktiv wird.
Wenn sich der Besucher einen ganzen Tag lang alle 29 Minuten auf der Website bewegt, wird dieser Besucher an diesem Tag als Neuer Besucher gezählt. Die Sitzung wurde nie zurückgesetzt, da der Besucher nie den Schwellenwert von 30 Minuten überschritten hat.

In den folgenden Informationen wird genauer erläutert, wie neue Besucher und wiederkehrende Besucher gezählt werden. Beispiele werden auch einbezogen, um zu erklären, warum die Summe dieser beiden Segmente nicht immer die Gesamtzahl der Besucher ergibt.

### Neue Besucher

Ein Besucher wird dem Segment „Neue Besucher“ hinzugefügt, wenn eine der folgenden Bedingungen zutrifft:

* Der Besucher besucht die Website zum ersten Mal.
* Der Besucher besucht die Site zum ersten Mal seit dem Löschen seiner Cookies.
* Der Besucher besucht die Website zum ersten Mal seit dem Ablauf der [Lebensdauer des Besucherprofils](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md).

### Zurückkehrende Besucher

Ein Besucher wird dem Segment „ Wiederkehrende Besucher“ hinzugefügt, wenn der Besucher die Site bereits besucht hatte, sie jedoch für mindestens 30 Minuten verlassen hat und später mit denselben Cookies zur Site zurückgekehrt ist. Solange ein Besucher innerhalb der Lebensdauer seines Profils zurückkehrt, ist er ein wiederkehrender Besucher.

Angenommen, die Lebensdauer Ihres Profils ist auf 14 Tage festgelegt (Standard). Ein Besucher wird dem Segment „Wiederkehrende Besucher“ hinzugefügt, wenn die folgenden Bedingungen erfüllt sind:

* Ein Besucher besucht die Website zum ersten Mal und wird als Neuer Besucher aufgezeichnet.
* Der Besucher verlässt die Website, kehrt jedoch sechs Tage später zurück.

Da die Profillebensdauer auf 14 Tage festgelegt ist, ist dieser Besucher im Segment „Wiederkehrende Besucher“ enthalten. Wenn der Besucher Cookies innerhalb dieses Zeitraums von sechs Tagen gelöscht hat, wird dieser Besucher in das Segment „Neue Besucher“ aufgenommen.

### Beispiele, die Diskrepanzen zwischen Metrikzahlen erklären

**Beispiel 1**: Wenn diese beiden Segmente auf eine Aktivität angewendet werden, ergeben das Segment „Neue Besucher“ und das Segment „Wiederkehrende Besucher“ nicht immer die Gesamtanzahl der Besucher.

Betrachten Sie das folgende Beispiel unter Berücksichtigung der oben genannten Bedingungen für neue Besucher und wiederkehrende Besucher:

* Ein Besucher besucht die Website zum ersten Mal und wird als Neuer Besucher gezählt.
* Der Besucher kehrt zur Website zurück, nachdem die Bedingungen für wiederkehrende Besucher erfüllt sind, und wird als wiederkehrender Besucher gezählt.

Dieser Besucher wird in der Gesamtbesucherzahl der Aktivität als einzelner Besucher gezählt, obwohl er sowohl in den Segmenten „Neue Besucher“ als auch „Wiederkehrende Besucher“ gezählt wird.

**Beispiel 2**: Abweichungen zwischen den Zahlen für neue und wiederkehrende Besucher hängen auch davon ab, wie Sie die [ der Aktivität konfigurieren](/help/main/c-activities/r-success-metrics/success-metrics.md).

Beispiel:

Mehrere neue Besucher besuchen Ihre Site und sind für eine Aktivität qualifiziert. Diese neuen Besucher werden in das Segment Neue Besucher gezählt. Alle diese Besucher haben auch einen Besuch in dieser Aktivität aufgezeichnet.

Einige Besucher erreichen die Konversionsmetrik, die als „Anzahl erhöhen und Benutzer in Aktivität halten“ konfiguriert wurde. Angenommen, einige dieser Benutzenden treffen die Konversionsmetrik mehrmals, dann erhöht sich die Konversionsmetrik nicht. Bei dieser Einrichtung können einige Benutzende jedoch auf die Konversionsmetrik klicken und dann zurück zur Startseite navigieren, wobei sie sich erneut für die Aktivität qualifizieren, um einen neuen Besuch aufzuzeichnen.

## Warum enthalten meine [!UICONTROL Experience Targeting] (XT)-Berichte Metriken für Kontrollerlebnisse?

XT-Aktivitäten sollten immer ein Kontrollerlebnis haben. Wenn Sie eine XT -Aktivität auf ähnliche Weise wie eine [!UICONTROL A/B Test] verwenden, was ein recht häufiges Szenario ist, sind die Daten zum Kontrollerlebnis nützlich. Wenn die Kontrollerlebnisdaten in Ihren Berichten nicht nützlich sind, können Sie sie ignorieren.

## Warum ist die Anzahl der Besuche in [!DNL Target] niedriger als in anderen [!DNL Adobe Experience Cloud] Lösungen? {#section_7E626FDB417E41B8B58BBF30FB207409}

Metrikzahlen, z. B. Besuche, die von [!DNL Target] gemeldet werden, sind aus verschiedenen Gründen immer niedriger als die gemeldeten Zahlen in anderen [!DNL Experience Cloud] Lösungen:

* [!DNL Target] zählt nur die Besuche von Besuchern, die für die Aktivität qualifiziert sind. In anderen Lösungen werden Besuche für Besucher angezeigt, die die Seite aufrufen, unabhängig davon, durch welche Aktivität sie auf die Seite gelangt sind.
* Möglicherweise führen unterschiedliche Aktivitäten zum gleichen Ort (diese Aktivitäten schließen sich gegenseitig aus). Somit werden Besuchern auf einer Webseite verschiedene Inhalte angezeigt, was sich auf die in [!DNL Target] registrierten Metrikwerte auswirkt.

## Warum stehen für meinen Aktivitätsbericht keine Daten zur Verfügung? {#section_E4722F6445884130951DF79981C8289B}

Wenn der Inhalt einer Aktivität erfolgreich an Besuchende gesendet wurde, ihr Bericht jedoch keine Daten enthält, wird möglicherweise die folgende Fehlermeldung angezeigt: „Für die ausgewählten Berichtseinstellungen sind keine Daten verfügbar.“

Es gibt einige mögliche Gründe, warum in Aktivitätsberichten Daten fehlen:

* Sie haben nicht die richtige Umgebung in den Einstellungen des Berichts ausgewählt
* Dem Kontrollerlebnis ist kein Traffic zugeordnet

### Sie haben nicht die richtige Umgebung in den Einstellungen des Berichts ausgewählt:

Wurde der Inhalt einer Aktivität den Benutzern erfolgreich bereitgestellt, enthält der zugehörige Bericht jedoch keine Daten, stellen Sie sicher, dass in den Berichtseinstellungen die korrekte Umgebung ([Hostgruppe](/help/main/administrating-target/hosts.md)) ausgewählt wurde.

So ändern Sie die Umgebung für einen Aktivitätsbericht:

1. Klicken Sie auf **[!UICONTROL Activities]**, dann in der Liste auf die gewünschte Aktivität, und klicken Sie anschließend auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf das Zahnradsymbol, um die Berichtseinstellungen zu bearbeiten.

   ![Dialogfeld für A/B-Einstellungen](/help/main/c-reports/c-report-settings/assets/ab_settings_dialog.png)

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Environment]** die Option **[!UICONTROL Production]** aus.

   Möglicherweise stehen Berichtsdaten bei Auswahl einer Entwicklungsumgebung nicht zur Verfügung.

1. Klicken Sie auf **[!UICONTROL Save]**.

Weitere Informationen zu Umgebungen finden Sie unter [Hosts](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

### Dem Kontrollerlebnis ist kein Traffic zugeordnet

Wenn der Inhalt einer Aktivität erfolgreich für Benutzer bereitgestellt wurde, ihr Bericht jedoch keine Daten enthält, stellen Sie sicher, dass Sie ein Erlebnis mit Traffic als Kontrollerlebnis verwenden.

1. Klicken Sie auf **[!UICONTROL Activities]**, dann in der Liste auf die gewünschte Aktivität, und klicken Sie anschließend auf die Registerkarte **[!UICONTROL Reports]** .
1. Klicken Sie auf das Zahnradsymbol, um die Berichtseinstellungen zu bearbeiten.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Control]** ein Erlebnis aus, das Traffic erhält.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Weitere Informationen zum Aktualisieren einer [!UICONTROL Automated Personalization] (AP)-Aktivität und zum Ändern des Kontrollerlebnisses in ein Erlebnis, das Traffic erhält, finden Sie unter [Auswahl des Kontrollelements für die Automated Personalization- oder automatische Targeting-Aktivität](/help/main/c-activities/t-automated-personalization/experience-as-control.md).


## Warum wird der Traffic zwischen meinen Erlebnissen in meiner A/B- oder MVT-Aktivität unterschiedlich aufgeteilt? {#uneven}

Zum Beispiel habe ich die Traffic-Aufteilung auf 50/50 oder 25/25/25/25 festgelegt, aber ich sehe eine sehr unterschiedliche Verteilung zwischen den Erlebnissen in der Berichterstellung. Es gibt mehrere erklärbare Gründe für eine uneinheitliche Besucherzahl in [!DNL Target]:

* Beim ersten Start einer [!DNL Target]-Aktivität kann die Traffic-Verteilung aufgrund der Edge-Knotenarchitektur, die [!DNL Target] zur Optimierung der Erlebnisbereitstellung verwendet, ungleichmäßig sein. Es empfiehlt sich, einer Aktivität etwas Zeit einzuräumen, um mehr Daten zu erfassen, und die Verteilung normalisiert sich. Weitere Informationen zur [!DNL Adobe Target] und zu Edge-Knoten finden Sie unter [Funktionsweise von Adobe Target](/help/main/c-intro/how-target-works.md).
* Wenn Sie sich in [!DNL Target] oder [!DNL Analytics] befinden und die **[!UICONTROL Visits]** verwenden, denken Sie daran, dass [!DNL Target] ein besucherbasiertes System ist und die Traffic-Verteilung für einen A/B- oder MVT-Test auf Besucherebene zugewiesen wird. Wenn Sie also die Aktivitätsergebnisse mit der Metrik **[!UICONTROL Visits]** untersuchen, kann die Traffic-Verteilung ungleichmäßig erscheinen, da bestimmte Besucher möglicherweise mehrere Besuche haben. Besucher ist die Standard-Normalisierungsmetrik bei der Bewertung der Aktivitätsleistung.
* Die Best Practice für A/B- und MVT-Tests besteht darin, den Traffic gleichmäßig zu verteilen. Eine Änderung der Traffic-Verteilung zwischen Erlebnissen (z. B. von 90/10 auf 50/50) während eines Tests kann zu ungleichen Besucherzahlen zwischen den Erlebnissen führen. Das Erlebnis mit geringerem Traffic wird möglicherweise nie „aufholen“.
* Wenn Sie die oben genannten Best Practices befolgen und die Traffic-Aufteilung sich im Laufe der Zeit nicht normalisiert, sollten Sie Folgendes überprüfen:

   * Verwenden Sie die neueste at.js-Bibliothek? Weitere Informationen über die aktuelle Version und die zugehörigen Versionshinweise finden Sie unter [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.

   * Ist es ein Umleitungstest? Falsches Timing beim Auslösen von Tags auf der Seite kann zu ungleichen Traffic-Unterteilungen führen, insbesondere bei Verwendung von [!DNL Analytics] als Datenquelle für eine [!DNL Target]. Weitere Informationen zur Behebung einer ungleichmäßigen Traffic-Verteilung bei einer Umleitungsaktivität mit Analytics for Target (A4T) finden Sie unter [Umleitungsangebote - A4T-FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
