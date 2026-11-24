---
keywords: Empfehlung; Backup; Sicherung
description: Erfahren Sie, wie Sie Backup-Empfehlungen in Adobe [!DNL Target Recommendations] verwenden.
title: Verwenden einer Reserveempfehlung
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
TQID: 'https://experienceleague.adobe.com/TziWJoAuEdCqa7uMTpX0O0InnlnjtbPXP-0wzQ-FCM0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 18%
---
# Verwenden einer Reserveempfehlung {#backup-recommendations}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Backup-Empfehlungen die verbleibenden Steckplätze eines Designs in [!DNL Adobe Target Recommendations] füllen.

>[!ENDSHADEBOX]

Wenn eine Empfehlung nicht genügend empfohlene Elemente zum Ausfüllen des Designs enthält, zeigt die Backup-Empfehlungsfunktion in [!DNL Adobe Target] die Ergebnisse des Backup-Algorithmus anstelle des Standardinhalts an. Ohne eine Sicherungsempfehlung zeigt das System dem Benutzer Standardinhalte an.

>[!NOTE]
>
>Weitere Informationen, einschließlich einer Matrix, in der die Ergebnisse der Verwendung der Optionen **[!UICONTROL Teilweises Design-Rendering]** und **[!UICONTROL Sicherungsinhalt anzeigen]** zusammen oder separat erläutert werden, finden Sie im Abschnitt [Sicherungsinhalt von Kriterien erstellen](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

Die Funktion für Sicherungsempfehlungen verwendet immer die am häufigsten angezeigten Elemente auf der Website, um alle verbleibenden Slots zu füllen, nachdem die Daten des Algorithmus verwendet wurden. Beispielsweise ist ein Design so konfiguriert, dass fünf empfohlene Elemente angezeigt werden, der Algorithmus verfügt jedoch über genügend Daten, um nur zwei der fünf Slots zu füllen. Die Backup-Empfehlungsfunktion füllt dann die anderen drei Slots mit den am häufigsten angezeigten Elementen.

Reserveempfehlungen werden zufällig aus den 500 am häufigsten angezeigten Produkten der gesamten Site ausgewählt. Der Datenzeitraum für Reserveempfehlungen beträgt eine Woche.

Die 500 am häufigsten angezeigten Ergebnisse werden sequenziell angeordnet und anschließend in Buckets mit 20 Ergebnissen aufgeteilt. Die Behälter werden der Reihe nach bereitgestellt, aber die Ergebnisse innerhalb jedes Behälters werden randomisiert und an die Seite zurückgegeben, sodass Benutzenden, die die Seite aktualisieren, neue, randomisierte Ergebnisse angezeigt werden. Wenn der Ergebnissatz aus der Vereinigung der Sammlung und der Filterregeln kleiner als 20 ist, werden Elemente zufällig aus der Sammlung ausgewählt.

Entsprechend diesem Bucket-Prozess werden Sicherungsempfehlungen in der folgenden Reihenfolge angezeigt:

1. Die 20 meistgesehenen Artikel, randomisiert.
1. Die nächsten 20 meistgesehenen Artikel, randomisiert.
1. Die nächsten 20 meistgesehenen Artikel, randomisiert, und so weiter.

Ohne Gruppierung könnte der 499. am häufigsten angezeigte Artikel angezeigt werden, gefolgt vom 200. am häufigsten angezeigten Artikel, gefolgt vom 380. am häufigsten angezeigten Artikel usw. Durch das Bucketing wird sichergestellt, dass die am häufigsten angezeigten Elemente zuerst empfohlen werden.

Wenn Elemente in Sammlungen gruppiert werden, verwenden die für die einzelnen Kriterien generierten Sicherungsempfehlungen auch die Sammlung, sodass nur Elemente in der Sammlung in die Sicherungsempfehlung aufgenommen werden. Jedes Element, das durch globale Ausschlussregeln ausgeschlossen wurde, kann nicht als Reserveempfehlung dienen. Duplikate werden aus Empfehlungen-Batches entfernt.

Sicherungsempfehlungen sind standardmäßig aktiviert und füllen die zusätzlichen Slots in einem Design mit einer zufälligen Auswahl der beliebtesten Elemente auf der Site.

Die Verwendung von Recommendations für Backups ist in der Regel Teil der Erörterung mit dem Implementierungs-Team während der Ersteinrichtung. Wenden Sie sich an den Account Manager, um die Einstellung für die Sicherungsempfehlung nach der Implementierung zu ändern.

Wenn **[!UICONTROL Partielles Design-Rendering]** (siehe [Backup-Inhalt](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) nicht aktiviert ist und das Design nicht ausgefüllt werden kann, werden stattdessen Backup-Empfehlungen (wenn aktiviert) oder Standardinhalte angezeigt.
