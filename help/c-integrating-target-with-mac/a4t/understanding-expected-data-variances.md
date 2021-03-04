---
keywords: Datenabweichungen; Analytics; Unterschiede; Varianz; a4t; Analytics für Target; Analytics als Berichtsquelle; Diskrepanzen; Diskrepanz
description: Erfahren Sie mehr über die erwarteten Datenabweichungen zwischen Adobe Target und Analytics, wenn Sie Analytics nicht für die Zielgruppe (A4T) verwenden, wodurch Datenschwankungen vollständig beseitigt werden.
title: Was ist die erwartete Datenabweichung zwischen Analytics und A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4abf975095c5e29eea42d67119a426a3922d8d79
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 49%

---


# Erwartete Datenabweichungen zwischen Adobe Target und Adobe Analytics bei Verwendung und Nichtverwendung von A4T

Informationen zu erwarteten Datenabweichungen zwischen [!DNL Target] und Adobe [!DNL Analytics] bei der *Verwendung* und *Nicht*-Verwendung von Analytics als Berichtsquelle (A4T). A4T reduziert Datenabweichungen erheblich.

## Erwartete Datenabweichungen bei der Verwendung von A4T {#expected-using-a4t}

Mit A4T werden sowohl bei Analytics- als auch Target-Berichterstellung zu Aktivitäten ausschließlich Analytics-Daten verwendet, sodass es kaum Abweichungen zwischen den Lösungen in den Target-Aktivitätsberichten gibt. Unter bestimmten Umständen vergleichen die Kunden jedoch die Daten der Zielgruppe mit den Analytics-Daten außerhalb des Bereichs der A4T-Integration und erleben so die im Folgenden beschriebenen Varianzprobleme.

Im Folgenden sind einige Szenarien aufgeführt, in denen Sie die erwartete Datenabweichung erleben können:

* A4T lässt die Möglichkeit zu, dass ein Target-Treffer (oben auf der Seite) auftritt, aber kein Analytics-Treffer (unten auf der Seite) auftritt. Angenommen, ein Besucher lädt die Seite, schließt jedoch den Browser, bevor der Analytics-Aufruf ausgelöst wird. In diesen Fällen schließt A4T den Treffer der Zielgruppe aus den Daten aus. Wenn Sie zulassen, dass Treffer von Zielgruppen (erneut am Seitenanfang) ohne einen tatsächlichen Analytics-Aufruf als Analytics-Treffer gezählt werden, entstehen Inkonsistenzen mit den Daten in Analytics (Besucher-Inflation usw.).

   Wenn ein Umleitungstest in der Zielgruppe eingerichtet wird, um den Traffic 50/50 (oder 25/25/25 usw.) zu teilen, wird das Benutzerverhalten möglicherweise nicht gleichmäßig aufgeteilt. Wenn Sie eine ungleichmäßige Aufteilung sehen, bedeutet dies einfach, dass eine Benutzergruppe einen Analytics-Aufruf auf der Landingpage nicht mehr ausgeführt hat als die anderen Gruppen. Durch dieses Fehlschlagen des Analytics-Aufrufs für eine Gruppe wurde der Treffer von Target für diesen Benutzer ausgeschlossen, sodass die Unstimmigkeiten entstanden.

   Adobe hofft, dieses Problem zukünftig in Angriff zu nehmen, da Adobe-Teams an A4T auf der Adobe Experience Platform arbeiten. Adoben-Teams bestimmen, wie diese verschiedenen Ereignis zu unterschiedlichen Zeitpunkten auf der Seite behandelt werden.

   >[!NOTE]
   >
   >Es gibt ein bekanntes Problem, bei dem einer begrenzten Anzahl von Kunden mit Redirects mit A4T ein höherer Prozentsatz an aufgetrennten Treffern angezeigt wird. Siehe [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Erwartete Datenabweichungen bei der *Nichtverwendung* von A4T   {#expected-not-using-a4t}

Abweichungen von 15–20 % sind normal, selbst mit ähnlichen Datensätzen. Systeme, die unterschiedlich zählen, können deutlich höhere Datenabweichungen von bis zu 35–50 % aufweisen. Manchmal können die Abweichungen sogar noch höher sein.

Auch wenn sich die Daten selbst deutlich unterscheiden, stimmen die Trends in der Regel überein. Solange die Unterschiede und Trends konsistent bleiben, bleiben die Daten gültig und nützlich. Sind Unterschiede und Trends inkonsistent, könnte das auf falsche Einstellungen hindeuten. Kontaktieren Sie in diesem Fall Ihren Kundenbetreuer, der Ihnen gerne weiterhelfen wird.

[!DNL Analytics] verwendet ein auf Besuchen und Transaktionen basierendes System, wohingegen besucherbasierte Metriken verwendet. [!DNL Target] Wenn ein Besucher eine Seite öffnet, zählt sie als Besuch in [!DNL Analytics], aber [!DNL Target] zählt den Besuch erst, wenn die in der Aktivität festgelegten Bedingungen erfüllt sind.

Berichte in [!DNL Target] zeigen die Leistung basierend auf der Konversions-mbox an, die beim Definieren der Aktivität ausgewählt wurde. Diese Konversions-Mbox-Daten werden jedoch nicht an [!DNL Analytics] gesendet, das über eigene Konversionsvariablen verfügt, wie von Ihrer [!DNL Analytics]-Tagging-Implementierung definiert. Wenn Sie identische Daten erwarten (z. B. wenn die Bestellung eines Einzelhändlers bestätigt, dass die Seite sowohl eine Konversions-mbox als auch ein [!DNL Analytics]-Ereignis enthält), können sich die Daten aufgrund der Platzierung dieser Tags unterscheiden. Im Allgemeinen sind die Trends in den Berichten der beiden Produkte ähnlich.

Erwartete Datenabweichungen können sowohl technischer als auch geschäftlicher Natur sein.

### Beispiele technischer Abweichungen   {#section_C3B50ED2E2F9416FAC91437CF1A87369}

Datenabweichungen können durch folgende technische Unterschiede entstehen:

* [!DNL Target] Besucher müssen Cookies und JavaScript zulassen
* Erst- und Drittanbieter-Cookies werden anders verarbeitet. Das führt dazu, dass Daten aus diesen Cookie-Typen nicht übereinstimmen
* Die relative Positionierung von Tags auf Seiten und der „Verlust“, der durch Besucher, die die Seite vor dem vollständigen Laden verlassen, hervorgerufen wird.
* Zeitzonen-Probleme
* Unterschiede, auf welchen Geräten Zählungen möglich sind

### Beispiele geschäftlicher Abweichungen   {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

Datenabweichungen können durch die folgenden geschäftlichen Unterschiede entstehen:

* Unterschiede zwischen Besucher- und Besuchsmetriken
* Beim Targeting für Aktivitäten werden manche Besucher ausgeschlossen.
* Eine einzelne mbox auf mehreren Seiten, die Besucher auf jeder dieser Seiten zählt
* Zu den Prioritäten der Aktivität können einige Besucher und andere auf einer Seite gehören
* Besucher, die einmal konvertiert wurden, können erneut gezählt werden, wenn sie die Aktivität erneut aufrufen
* [!DNL Analytics] zählt alle Konversionen für alle Besuche und Besucher, [!DNL Target] zählt jedoch nur Konversionen für Besuche und Besucher, die in der Aktivität inbegriffen sind