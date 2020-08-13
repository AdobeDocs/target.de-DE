---
keywords: recommendation;backup;back up
description: Wenn Sie die Funktion „Reserveempfehlung“ verwenden, zeigen Empfehlungen, die nicht über genügend empfohlene Elemente verfügen, keinen Standardinhalt an. Stattdessen zeigen Empfehlungen die Ergebnisse des Reservealgorithmus an.
title: Verwenden einer Reserveempfehlung
feature: criteria
uuid: 2910a844-9dd6-4e69-8652-b2215fed1545
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Verwenden einer Reserveempfehlung{#use-a-backup-recommendation}

Wenn Sie die Funktion „Reserveempfehlung“ verwenden, zeigen Empfehlungen, die nicht über genügend empfohlene Elemente verfügen, keinen Standardinhalt an. Stattdessen zeigen Empfehlungen die Ergebnisse des Reservealgorithmus an.

Wenn Sie keine Reserveempfehlung verwenden, zeigt das System dem Benutzer Standardinhalt an, wenn eine Empfehlung nicht genügend Artikel zum Ausfüllen der Anzeige aufweist.

Wenn die Daten des Algorithmus aufgebraucht sind, füllt die Funktion „Reserveempfehlung“ verbleibende Slots immer mit den am häufigsten angezeigten Artikeln der Site aus. Beispiel: Ihre Vorlage wurde so konfiguriert, dass fünf empfohlene Artikel angezeigt werden, und Sie verwenden den Algorithmus *Kaufpräferenzen*. Da Sie jedoch nur über genügend Daten für zwei Slots verfügen, füllt die Funktion „Reserveempfehlung“ die verbleibenden drei Slots immer mit den am häufigsten angezeigten Artikeln aus.

Reserveempfehlungen werden zufällig aus den 500 am häufigsten angezeigten Produkten der gesamten Site ausgewählt. Der Datenzeitraum für Reserveempfehlungen beträgt eine Woche.

Die 500 am häufigsten angezeigten Ergebnisse werden sequenziell angeordnet und anschließend in Behälter mit 20 Ergebnissen aufgeteilt. Die Behälter werden in der entsprechenden Reihenfolge verarbeitet. Die Ergebnisse in den einzelnen Behältern werden jedoch randomisiert und an die Seite zurückgegeben. Wenn die Benutzer die Seite aktualisieren, werden ihnen neue, randomisierte Ergebnisse angezeigt. Wenn der Ergebnissatz der Vereinigung der Sammlung und der Filterungsregeln kleiner als 20 ist, erfolgt eine randomisierte Auswahl aus der Sammlung.

Entsprechend diesem Behälterprozess werden Sicherungsempfehlungen in der folgenden Reihenfolge angezeigt:

1. Anzeige der 20 am häufigsten angezeigten Elemente, randomisiert, dann
1. Anzeige der nächsten 20 am häufigsten angezeigten Elemente, randomisiert, dann
1. Anzeige der nächsten 20 am häufigsten angezeigten Elemente, randomisiert
1. und so weiter

Ohne das Bucketing von Sicherungsempfehlungen ist es möglich, das 499. am häufigsten angezeigte Element, gefolgt vom 200. am häufigsten angezeigten Element, gefolgt vom 380. am häufigsten angezeigten Element usw. anzuzeigen. Das Bucketing stellt sicher, dass die am häufigsten angezeigten Elemente als Erstes angezeigt werden.

>[!NOTE]
>
>Wenn Sie Ihre Artikel in Katalogen gruppieren, verwenden die für jeden Algorithmus innerhalb der Empfehlung erzeugten Reserveempfehlungen ebenfalls den Katalog, sodass nur Artikel im Katalog in die Reserveempfehlung aufgenommen werden.

Jedes Element, das durch globale Ausschlussregeln ausgeschlossen wurde, kann nicht als Reserveempfehlung dienen.

Reserveempfehlungen sind standardmäßig aktiviert und füllen die Extraslots in einer Vorlage mit einer zufallsbasierten Auswahl der beliebtesten Artikel der Site aus.

Duplikate werden aus Empfehlungen-Batches entfernt.

Die Nutzung von Reserveempfehlungen ist normalerweise Gegenstand der Diskussion im Implementierungsteam während des ersten Setups. Wenn Sie die Einstellungen für die Reserveempfehlung ändern möchten, wenden Sie sich bitte an Ihren Kundenbetreuer.

Wenn „Teilweises Design-Rendering aktivieren“ (siehe  [Ähnlichkeit von Inhalten](../../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96)) deaktiviert ist und die Vorlage nicht angezeigt wird, wird entweder die Reserveempfehlung oder der Standardinhalt angezeigt.
