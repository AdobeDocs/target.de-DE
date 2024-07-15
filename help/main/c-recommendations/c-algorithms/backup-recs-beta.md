---
keywords: Empfehlung; Backup; Sicherung
description: Erfahren Sie, wie Sie Sicherungsempfehlungen in Adobe [!DNL Target Recommendations] verwenden.
title: Wie verwende ich eine Reserveempfehlung in [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 6d2a313b0e54aa5f6717eee850c79e4092309e7d
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 70%

---

# Verwenden einer Reserveempfehlung

Wenn Sie die Funktion für Reserveempfehlungen in [!DNL Adobe Target] verwenden, zeigen Empfehlungen, die nicht genügend empfohlene Artikel enthalten, keinen Standardinhalt an. Stattdessen zeigen Empfehlungen die Ergebnisse des Reservealgorithmus an.

Wenn Sie keine Reserveempfehlung verwenden, zeigt das System dem Benutzer Standardinhalt an, wenn eine Empfehlung nicht genügend Artikel zum Ausfüllen der Anzeige aufweist.

>[!NOTE]
>
>Weitere Informationen finden Sie im Abschnitt [Inhalt des Themas Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) , einschließlich einer Matrix, die die Ergebnisse erläutert, die bei der Verwendung der Optionen [!UICONTROL Partial Design Rendering] und [!UICONTROL Show Backup Recommendations] zusammen oder getrennt zu beobachten sind.

Die Funktion für Reserveempfehlungen verwendet immer die am häufigsten angezeigten Elemente auf der Site, um alle verbleibenden Plätze auszufüllen, nachdem die Daten des Algorithmus verwendet wurden. Beispiel: Ihre Vorlage wurde so konfiguriert, dass fünf empfohlene Artikel angezeigt werden, und Sie verwenden den Algorithmus *Kaufpräferenzen*. Da Sie jedoch nur über genügend Daten für zwei Slots verfügen, füllt die Funktion „Reserveempfehlung“ die verbleibenden drei Slots immer mit den am häufigsten angezeigten Artikeln aus.

Reserveempfehlungen werden zufällig aus den 500 am häufigsten angezeigten Produkten der gesamten Site ausgewählt. Der Datenzeitraum für Reserveempfehlungen beträgt eine Woche.

Die 500 am häufigsten angezeigten Ergebnisse werden sequenziell angeordnet und anschließend in Behälter mit 20 Ergebnissen aufgeteilt. Die Behälter werden in der entsprechenden Reihenfolge verarbeitet. Die Ergebnisse in den einzelnen Behältern werden jedoch randomisiert und an die Seite zurückgegeben. Wenn die Benutzer die Seite aktualisieren, werden ihnen neue, randomisierte Ergebnisse angezeigt. Wenn der Ergebnissatz aus der Vereinigung der Sammlung und der Filterregeln kleiner als 20 ist, wird er zufällig aus der Sammlung ausgewählt.

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

Wenn &quot;Teilweises Design-Rendering aktivieren&quot;(siehe [Inhaltseinstellungen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) nicht aktiviert ist und die Vorlage nicht angezeigt wird, wird stattdessen entweder die Reserveempfehlung oder der Standardinhalt angezeigt.