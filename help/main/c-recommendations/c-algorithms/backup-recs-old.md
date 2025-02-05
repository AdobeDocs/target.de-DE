---
keywords: Empfehlung; Backup; Sicherung
description: Erfahren Sie, wie Sie Sicherungsempfehlungen in Adobe [!DNL Target] Recommendations verwenden. Empfehlungen, für die nicht genügend empfohlene Elemente vorhanden sind, zeigen die Ergebnisse des Backup-Algorithmus an.
title: Wie verwende ich eine Sicherungsempfehlung in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 77%

---

# Verwenden einer Reserveempfehlung

Wenn Sie die Funktion „Recommendations sichern“ in [!DNL Adobe Target] verwenden, werden für jede Empfehlung, die nicht über genügend empfohlene Elemente verfügt, keine Standardinhalte angezeigt. Stattdessen zeigen Empfehlungen die Ergebnisse des Reservealgorithmus an.

Wenn Sie keine Reserveempfehlung verwenden, zeigt das System dem Benutzer Standardinhalt an, wenn eine Empfehlung nicht genügend Artikel zum Ausfüllen der Anzeige aufweist.

>[!NOTE]
>
>Weitere Informationen finden Sie im Abschnitt [Inhalt“ des Themas Erstellen von ](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content), einschließlich einer Matrix, in der die Ergebnisse erläutert werden, die Sie bei der gemeinsamen oder separaten Verwendung der Optionen [!UICONTROL Partial Design Rendering] und [!UICONTROL Show Backup Recommendations] beobachten werden.

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

Wenn die Option Teilweises Design-Rendering aktivieren ([Inhaltseinstellungen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) nicht aktiviert ist und die Vorlage nicht angezeigt wird, wird stattdessen entweder die Backup-Empfehlung oder der Standardinhalt angezeigt.
