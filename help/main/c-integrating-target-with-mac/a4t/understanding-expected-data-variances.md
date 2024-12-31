---
keywords: Datenabweichungen; Analytics; Unterschiede; Varianz; a4t; Analytics für Target; Analytics als Berichtsquelle; Diskrepanzen; Diskrepanz
description: Erfahren Sie mehr über die erwarteten Datenabweichungen zwischen Adobe [!DNL Target]  und Analytics, wenn Sie Analytics nicht für  [!DNL Target] A4T) verwenden. Dadurch werden Datenabweichungen vollständig beseitigt.
title: Wie hoch ist die erwartete Datenabweichung zwischen Analytics und A4T?
feature: Analytics for Target (A4T)
exl-id: 9e63f309-8ec1-4ed5-a1f9-6c3098a7b8f6
source-git-commit: 4abd24f63dd65e65a1d8b07647630eeb640e7a1d
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 45%

---

# Erwartete Datenabweichungen zwischen Adobe [!DNL Target] und Adobe Analytics bei Verwendung und Nichtverwendung von A4T

Informationen zu erwarteten Datenabweichungen zwischen [!DNL Target] und Adobe [!DNL Analytics] bei der *Verwendung* und *Nicht*-Verwendung von Analytics als Berichtsquelle (A4T). A4T reduziert Datenabweichungen erheblich.

## Erwartete Datenabweichung bei Verwendung von A4T {#expected-using-a4t}

Mit A4T werden sowohl bei Analytics- als auch Target-Berichterstellung zu Aktivitäten ausschließlich Analytics-Daten verwendet, sodass es kaum Abweichungen zwischen den Lösungen in den Target-Aktivitätsberichten gibt. Unter bestimmten Umständen vergleichen Kundinnen und Kunden jedoch Target-Daten mit Analytics-Daten außerhalb des Bereichs der A4T-Integration und haben daher die unten beschriebenen Varianzprobleme.

Im Folgenden finden Sie einige Szenarien, in denen zu erwartende Datenvarianzen auftreten können:

* A4T lässt die Möglichkeit zu, dass ein Target-Treffer (oben auf der Seite) auftritt, aber kein Analytics-Treffer (unten auf der Seite) auftritt. Angenommen, ein Besucher lädt die Seite, schließt jedoch den Browser, bevor der Analytics-Aufruf ausgelöst wird. In diesen Fällen schließt A4T den Target-Treffer aus den Daten aus. Wenn Target-Treffer (wieder oben auf der Seite) als Analytics-Treffer gezählt werden, wenn kein tatsächlicher Analytics-Aufruf erfolgt, entsteht eine Inkonsistenz mit dem Datensatz in Analytics (Besucherinflation usw.).

  Wenn in Target ein Umleitungstest eingerichtet wird, um Traffic 50/50 (oder 25/25/25/25 usw.) zu teilen, wird das Benutzerverhalten möglicherweise nicht gleichmäßig verteilt. Wenn eine ungleiche Aufteilung angezeigt wird, bedeutet dies einfach, dass eine Benutzergruppe einen Analytics-Aufruf auf der Landingpage nicht ausführen konnte, während die anderen Gruppen dies taten. Durch dieses Fehlschlagen des Analytics-Aufrufs für eine Gruppe wurde der Treffer von Target für diesen Benutzer ausgeschlossen, sodass die Unstimmigkeiten entstanden.

  Adobe hofft, dieses Problem in Zukunft lösen zu können, da Adobe-Teams auf A4T auf der Adobe Experience Platform hinarbeiten. Adobe-Teams bestimmen, wie diese verschiedenen Ereignisse, die zu unterschiedlichen Zeiten auf der Seite auftreten, gehandhabt werden.

## Erwartete Datenabweichungen bei der *Nichtverwendung* von A4T {#expected-not-using-a4t}

Abweichungen von 15–20 % sind normal, selbst mit ähnlichen Datensätzen. Systeme, die unterschiedlich zählen, können deutlich höhere Datenabweichungen von bis zu 35–50 % aufweisen. Manchmal können die Abweichungen sogar noch größer sein.

Auch wenn sich die Daten selbst deutlich unterscheiden, stimmen die Trends in der Regel überein. Solange die Unterschiede und Trends konsistent bleiben, bleiben die Daten gültig und nützlich. Sind Unterschiede und Trends inkonsistent, könnte das auf falsche Einstellungen hindeuten. Kontaktieren Sie in diesem Fall Ihren Kundenbetreuer, der Ihnen gerne weiterhelfen wird.

[!DNL Analytics] verwendet ein auf Besuchen und Transaktionen basierendes System, wohingegen besucherbasierte Metriken verwendet. [!DNL Target] Wenn ein Besucher eine Seite öffnet, wird dies in [!DNL Analytics] als Besuch gezählt, aber [!DNL Target] zählt den Besuch erst, wenn die in der Aktivität festgelegten Bedingungen erfüllt sind.

Berichte in [!DNL Target] zeigen die Leistung basierend auf der Konversions-Mbox an, die beim Definieren der Aktivität ausgewählt wurde. Diese Konversions-Mbox-Daten werden jedoch nicht an [!DNL Analytics] gesendet, das entsprechend der Definition in Ihrer [!DNL Analytics]-Tagging-Implementierung über eigene Konversionsvariablen verfügt. Wenn Sie identische Daten erwarten (z. B. wenn die Bestellung eines Einzelhändlers bestätigt, dass die Seite sowohl eine Konversions-Mbox als auch ein [!DNL Analytics] Kaufereignis enthält), können die Daten aufgrund der Platzierung dieser Tags unterschiedlich sein. Im Großen und Ganzen sind die Tendenzen in den Berichten über die beiden Produkte ähnlich.

Erwartete Datenabweichungen können sowohl technischer als auch geschäftlicher Natur sein.

### Beispiele technischer Abweichungen  {#section_C3B50ED2E2F9416FAC91437CF1A87369}

Datenabweichungen können durch folgende technische Unterschiede entstehen:

* [!DNL Target] Besucher müssen Cookies und JavaScript zulassen
* Erst- und Drittanbieter-Cookies werden anders verarbeitet. Das führt dazu, dass Daten aus diesen Cookie-Typen nicht übereinstimmen
* Die relative Positionierung von Tags auf Seiten und der „Verlust“, der durch Besucher, die die Seite vor dem vollständigen Laden verlassen, hervorgerufen wird.
* Zeitzonen-Probleme
* Unterschiede, auf welchen Geräten Zählungen möglich sind

### Beispiele geschäftlicher Abweichungen  {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

Datenabweichungen können durch die folgenden geschäftlichen Unterschiede entstehen:

* Unterschiede zwischen Besucher- und Besuchsmetriken
* Beim Targeting für Aktivitäten werden manche Besucher ausgeschlossen.
* Eine einzelne Mbox auf mehreren Seiten, die Besucher auf jeder dieser Seiten zählt
* Aktivitätsprioritäten können einige Besucher einschließen und andere auf einer Seite ausschließen
* Besucherinnen und Besucher, die einmal konvertiert haben, können erneut gezählt werden, wenn sie die Aktivität erneut aufrufen
* [!DNL Analytics] zählt alle Konversionen für alle Besuche und Besucher, [!DNL Target] zählt jedoch nur Konversionen für Besuche und Besucher, die in der Aktivität inbegriffen sind
