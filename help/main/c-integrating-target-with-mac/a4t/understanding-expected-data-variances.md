---
keywords: Datenabweichungen; Analytics; Unterschiede; Varianz; a4t; Analytics für Target; Analytics als Berichtsquelle; Diskrepanzen; Diskrepanz
description: Erfahren Sie mehr über die erwarteten Datenabweichungen zwischen Adobe [!DNL Target] und Analytics bei Nichtverwendung von Analytics für [!DNL Target]  (A4T), wodurch Datenabweichungen vollständig beseitigt werden.
title: Was ist die erwartete Datenabweichung zwischen Analytics und A4T?
feature: Analytics for Target (A4T)
exl-id: 9e63f309-8ec1-4ed5-a1f9-6c3098a7b8f6
source-git-commit: 4abd24f63dd65e65a1d8b07647630eeb640e7a1d
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 45%

---

# Erwartete Datenabweichungen zwischen Adobe [!DNL Target] und Adobe Analytics bei Verwendung und Nichtverwendung von A4T

Informationen zu erwarteten Datenabweichungen zwischen [!DNL Target] und Adobe [!DNL Analytics] bei der *Verwendung* und *Nicht*-Verwendung von Analytics als Berichtsquelle (A4T). A4T reduziert Datenabweichungen erheblich.

## Erwartete Datenabweichungen bei der Verwendung von A4T {#expected-using-a4t}

Mit A4T werden sowohl bei Analytics- als auch Target-Berichterstellung zu Aktivitäten ausschließlich Analytics-Daten verwendet, sodass es kaum Abweichungen zwischen den Lösungen in den Target-Aktivitätsberichten gibt. Unter bestimmten Umständen vergleichen Kunden Target-Daten jedoch mit Analytics-Daten, die außerhalb des A4T-Integrationsbereichs liegen, und erleben daher die unten beschriebenen Varianzprobleme.

Im Folgenden finden Sie einige Szenarien, in denen Sie die erwarteten Datenabweichungen feststellen können:

* A4T lässt die Möglichkeit zu, dass ein Target-Treffer (oben auf der Seite) auftritt, aber kein Analytics-Treffer (unten auf der Seite) auftritt. Angenommen, ein Besucher lädt die Seite, schließt jedoch den Browser, bevor der Analytics-Aufruf ausgelöst wird. In diesen Fällen schließt A4T den Target-Treffer aus den Daten aus. Wenn Target-Treffer (erneut oben auf der Seite) als Analytics-Treffer gezählt werden können, wenn kein tatsächlicher Analytics-Aufruf erfolgt, entstehen Inkonsistenzen mit dem Datensatz in Analytics (Besucherinflation usw.).

  Wenn in Target ein Umleitungstest eingerichtet ist, um den Traffic 50/50 (oder 25/25/25 usw.) aufzuteilen, wird das Benutzerverhalten möglicherweise nicht gleichmäßig aufgeteilt. Wenn Sie eine ungleichmäßige Aufspaltung sehen, bedeutet dies einfach, dass eine Benutzergruppe einen Analytics-Aufruf auf der Landingpage nicht häufiger als die anderen Gruppen ausgeführt hat. Durch dieses Fehlschlagen des Analytics-Aufrufs für eine Gruppe wurde der Treffer von Target für diesen Benutzer ausgeschlossen, sodass die Unstimmigkeiten entstanden.

  Adobe hofft, dieses Problem zukünftig zu lösen, wenn Adobe-Teams an A4T auf der Adobe Experience Platform arbeiten. Adobe-Teams bestimmen, wie mit diesen verschiedenen Ereignissen umzugehen ist, die zu unterschiedlichen Zeitpunkten auf der Seite auftreten.

## Erwartete Datenabweichungen bei der *Nichtverwendung* von A4T {#expected-not-using-a4t}

Abweichungen von 15–20 % sind normal, selbst mit ähnlichen Datensätzen. Systeme, die unterschiedlich zählen, können deutlich höhere Datenabweichungen von bis zu 35–50 % aufweisen. Manchmal können die Abweichungen sogar noch höher sein.

Auch wenn sich die Daten selbst deutlich unterscheiden, stimmen die Trends in der Regel überein. Solange die Unterschiede und Trends konsistent bleiben, bleiben die Daten gültig und nützlich. Sind Unterschiede und Trends inkonsistent, könnte das auf falsche Einstellungen hindeuten. Kontaktieren Sie in diesem Fall Ihren Kundenbetreuer, der Ihnen gerne weiterhelfen wird.

[!DNL Analytics] verwendet ein auf Besuchen und Transaktionen basierendes System, wohingegen besucherbasierte Metriken verwendet. [!DNL Target] Wenn ein Besucher eine Seite öffnet, zählt dies als Besuch in [!DNL Analytics], aber [!DNL Target] zählt den Besuch erst, wenn die in der Aktivität festgelegten Bedingungen erfüllt sind.

Berichte in [!DNL Target] zeigen die Leistung basierend auf der Konversions-Mbox an, die beim Definieren der Aktivität ausgewählt wurde. Diese Konversions-Mbox-Daten werden jedoch nicht an [!DNL Analytics] gesendet, das eigene Konversionsvariablen hat, die durch Ihre [!DNL Analytics] -Tagging-Implementierung definiert sind. Wenn Sie identische Daten erwarten (z. B. wenn die Bestellung eines Einzelhändlers bestätigt, dass die Seite sowohl eine Konversions-Mbox als auch ein [!DNL Analytics] -Kaufereignis enthält), können die Daten aufgrund der Platzierung dieser Tags unterschiedlich sein. Im Allgemeinen sind die Trends in den Berichten der beiden Produkte ähnlich.

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
* Eine einzelne mbox auf mehreren Seiten, die Besucher auf jeder dieser Seiten zählt
* Aktivitätsprioritäten können einige Besucher auf einer Seite ein- und andere ausschließen.
* Besucher, die einmal umgerechnet wurden, können erneut gezählt werden, wenn sie die Aktivität erneut aufrufen
* [!DNL Analytics] zählt alle Konversionen für alle Besuche und Besucher, [!DNL Target] zählt jedoch nur Konversionen für Besuche und Besucher, die in der Aktivität inbegriffen sind
