---
keywords: Empfehlung; Backup; Sicherung
description: Erfahren Sie, wie Sie Reserveempfehlungen in Adobe verwenden. [!DNL Target] Recommendations. Empfehlungen, die nicht genügend empfohlene Artikel enthalten, zeigen die Ergebnisse des Backup-Algorithmus an.
title: Wie verwende ich eine Reserveempfehlung in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 82%

---

# Verwenden einer Reserveempfehlung

Wenn Sie die Funktion für Reserveempfehlungen in Adobe Target verwenden, zeigt eine Empfehlung, die nicht genügend empfohlene Artikel enthält, keinen Standardinhalt an. Stattdessen zeigen Empfehlungen die Ergebnisse des Reservealgorithmus an.

Wenn Sie keine Reserveempfehlung verwenden, zeigt das System dem Benutzer Standardinhalt an, wenn eine Empfehlung nicht genügend Artikel zum Ausfüllen der Anzeige aufweist.

>[!NOTE]
>
>Weitere Informationen finden Sie in der [Abschnitt &quot;Inhalt&quot;der Kriterien &quot;Erstellen&quot;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) -Thema, einschließlich einer Matrix, die die Ergebnisse erläutert, die Sie bei der Verwendung der [!UICONTROL Teilweises Design-Rendering] und [!UICONTROL Backup Recommendations anzeigen] Optionen zusammen oder getrennt.

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

Wenn „Teilweises Design-Rendering aktivieren“ (siehe  [Ähnlichkeit von Inhalten](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) deaktiviert ist und die Vorlage nicht angezeigt wird, wird entweder die Reserveempfehlung oder der Standardinhalt angezeigt.
