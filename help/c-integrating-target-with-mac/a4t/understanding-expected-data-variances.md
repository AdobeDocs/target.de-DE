---
description: Informationen zu erwarteten Datenabweichungen zwischen Target und Adobe Analytics, wenn Analytics nicht als Berichtsquelle (A4T) verwendet wird, wodurch alle Datenabweichungen beseitigt werden.
keywords: Datenabweichungen; Analytics; Unterschiede; Varianz; a4t; Analytics für Target; Analytics als Berichtsquelle; Diskrepanzen; Diskrepanz
seo-description: Informationen zu erwarteten Datenabweichungen zwischen Target und Adobe Analytics, wenn Analytics nicht als Berichtsquelle (A4T) verwendet wird, wodurch alle Datenabweichungen beseitigt werden.
seo-title: Erwartete Datenabweichungen bei Nichtverwendung von A4T
solution: Target
title: Erwartete Datenabweichungen bei Nichtverwendung von A4T
topic: Advanced
uuid: 61bef460-8613-4251-b1b2-b6226ec86d9b
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T{#expected-data-variances-when-not-using-a-t}

Informationen zu erwarteten Datenabweichungen zwischen [!DNL Target] und Adobe [!DNL Analytics] , wenn *sie Analytics verwenden* und *nicht* als Berichtsquelle (A 4 T) verwenden. A4T reduziert Datenabweichungen erheblich.

## Erwartete Datenvarianz bei Verwendung von A 4 T {#expected-using-a4t}

Mit A4T werden sowohl bei Analytics- als auch Target-Berichterstellung zu Aktivitäten ausschließlich Analytics-Daten verwendet, sodass es kaum Abweichungen zwischen den Lösungen in den Target-Aktivitätsberichten gibt. In einigen Fällen vergleichen Kunden Target- und Analytics-Daten jedoch möglicherweise außerhalb des A4T-Integrationsbereichs und bemerken die nachstehend beschriebenen Abweichungsprobleme.

Im Folgenden finden Sie einige Szenarien, in denen möglicherweise Datenvarianz erwartet wird:

* A 4 T ermöglicht die Möglichkeit, dass ein Target-Treffer (obere Seite der Seite) auftritt, aber kein Analytics-Treffer (unterer Seitenaufruf) stattfindet. Ein Beispiel hierfür wäre, wenn der Benutzer die Seite lädt, den Browser jedoch schließt, bevor der Analytics-Aufruf ausgelöst wird. In diesen Fällen schließt A 4 T den Treffer von Target aus unseren Daten aus. Der Grund dafür ist, dass durch das Zulassen von Treffern von Target-Treffern (erneut obere Seite) als Analytics-Treffer in der Abwesenheit eines tatsächlichen Analytics-Aufrufs Inkonsistenzen mit dem in Analytics (Besucherinflation usw.) festgelegten Datensatz entstehen würden.

   Wenn in Target ein Umleitungstest eingerichtet ist, um den Traffic 50/50 (oder 25/25/25/25 usw.) zu teilen, wird das Benutzerverhalten möglicherweise nicht gleichmäßig aufgeteilt. Wenn Sie eine ungleichmäßige Aufteilung sehen, bedeutet dies einfach, dass eine Benutzergruppe einen Analytics-Aufruf auf der Einstiegsseite nicht ausführt, mehr als die anderen. Durch dieses Fehlschlagen des Analytics-Aufrufs für eine Gruppe wurde der Treffer von Target für diesen Benutzer ausgeschlossen, sodass unstimmigkeiten entstehen.

   Dies ist etwas, das wir zukünftig besprechen sollten, wenn wir für A 4 T auf der Adobe Experience Platform arbeiten. Unsere Teams arbeiten daran, diese verschiedenen Ereignisse zu unterschiedlichen Zeiten auf der Seite zu verarbeiten.

* Angenommen, Sie erstellen eine automatisch zuordnungsfähige Aktivität für alle Besucher einer bestimmten Seite. Da Aktivitäten des Typs „Automatische Zuordnung“ A4T nicht unterstützen, werden alle Aktivitätsdaten von [!DNL Target] erfasst. Möglicherweise erwarten Sie, dass die Besucher der Aktivität in der [!DNL Target] Berichterstellung den Besuchern auf der Seite in der [!DNL Analytics] Berichterstellung für den gleichen Datumsbereich entsprechen. Dies ist ein Szenario, in dem die unten beschriebene Abweichung erwartet wird.

   Eine vollständige Liste der Aktivitätstypen, die A4T unterstützen, finden Sie unter [Unterstützte Aktivitätstypen](../../c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA).

## Erwartete Datenabweichungen bei der *Nichtverwendung* von A4T {#expected-not-using-a4t}

Abweichungen von 15–20 % sind normal, selbst mit ähnlichen Datensätzen. Systeme, die unterschiedlich zählen, können deutlich höhere Datenabweichungen von bis zu 35–50 % aufweisen. In manchen Fällen können Abweichungen sogar noch höher ausfallen.

Auch wenn sich die Daten selbst deutlich unterscheiden, stimmen die Trends in der Regel überein. Solange die Unterschiede und Trends konsistent bleiben, bleiben die Daten gültig und nützlich. Sind Unterschiede und Trends inkonsistent, könnte das auf falsche Einstellungen hindeuten. Kontaktieren Sie in diesem Fall Ihren Kundenbetreuer, der Ihnen gerne weiterhelfen wird.

[!DNL Analytics] verwendet ein auf Besuchen und Transaktionen basierendes System, wohingegen besucherbasierte Metriken verwendet. [!DNL Target] Das bedeutet, dass das Öffnen einer Seite durch einen Besucher in [!DNL Analytics] als Besuch gezählt wird, [!DNL Target] den Besuch jedoch erst zählt, wenn die in der Aktivität festgelegten Bedingungen erfüllt sind.

Berichte in [!DNL Target] zeigen die Leistung basierend auf der Konversions-Mbox an, die beim Definieren der Aktivität ausgewählt wurde. Doch diese Konversions-Mbox-Daten werden nicht an [!DNL Analytics] gesendet, das eigene Konversionsvariablen hat, so wie durch Ihre [!DNL Analytics]-Tagging-Implementierung definiert. In Fällen, in denen Sie identische Daten erwarten würden (z. B. wenn die Seite zur Bestellbestätigung eines Einzelhändlers sowohl eine Konversions-Mbox als auch ein [!DNL Analytics]-Kaufereignis beinhaltet), kann es zu Datenunterschieden aufgrund der Platzierung dieser Tags kommen. Im Allgemeinen sollten die Trends in den Berichten beider Produkte ähnlich sein.

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
* Eine einzige Mbox kann auf mehreren Seiten positioniert sein und Besucher auf jeder dieser Seiten zählen.
* Aktivitätsprioritäten können einige Besucher auf einer Seite ein- und andere ausschließen.
* Besucher, die einmal konvertiert wurden, können erneut gezählt werden, wenn sie die Aktivität erneut aufrufen.
* [!DNL Analytics] zählt alle Konversionen für alle Besuche und Besucher, [!DNL Target] zählt jedoch nur Konversionen für Besuche und Besucher, die in der Aktivität inbegriffen sind