---
keywords: Recommendations; Angebot; Vorschau; Launch; Status; Kriterien; Algorithmus
description: Erfahren Sie, wie Sie eine Vorschau Ihrer Adobe [!DNL Target] Recommendations-Aktivität anzeigen, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten.
title: Wie kann ich eine Recommendations-Aktivität in der Vorschau anzeigen und starten?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
TQID: 'https://experienceleague.adobe.com/21swhpZie0QN09m0LB7VwVO-9U6GWxQ0kbthPlnns18'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%
---
# Vorschau und Starten Ihrer Recommendations-Aktivität {#preview-launch-recs-activity}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie den Algorithmusstatus überprüfen, eine Vorschau der Recommendations anzeigen und eine [!DNL Recommendations] aktivieren können.

>[!ENDSHADEBOX]

Durch die Vorschau der Empfehlungen vor dem Start einer Aktivität wird bestätigt, dass Ergebnisse verfügbar sind. Dies gilt für [!UICONTROL Recommendations], [!UICONTROL A/B-] und [!UICONTROL Experience Targeting] (XT)-Aktivitäten, die [Recommendations-Angebote](/help/main/c-recommendations/recommendations-as-an-offer.md) enthalten. [!DNL Target Recommendations] bietet mehrere Möglichkeiten, eine Vorschau der Recommendations anzuzeigen.

## Überprüfen des Algorithmusstatus {#check-status}

Nachdem eine Aktivität erstellt wurde, führt [!DNL Recommendations] einen Algorithmus aus, um die Empfehlungen zu generieren. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Der Status des Algorithmus wird mit den Kriterien im Aktivitätsdiagramm auf der Seite **[!UICONTROL Überblick]** der Aktivität [!DNL Recommendations] aufgelistet.

![Seite Recommendations-Aktivität - Übersicht](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview-new.png)

Der Status kann einer der folgenden sein:

* **[!UICONTROL Ergebnisse bereit]**: Der Algorithmus hat Ergebnisse zurückgegeben.
* **[!UICONTROL Ergebnisse nicht bereit]**: Die Ausführung des Algorithmus ist noch nicht abgeschlossen.
* **[!UICONTROL Feed-]**: Die Feed-Datei mit benutzerdefinierten Kriterien konnte nicht abgerufen werden.

![Dialogfeld „Ergebnisse“](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Schätzen der Algorithmuslaufzeit {#algorithm-run-time}

Nachdem eine Aktivität, die ein Kriterium enthält, gespeichert wurde, berechnet [!DNL Target] die Recommendations anhand der ausgewählten Sammlung, des ausgewählten Kriteriums, des ausgewählten Designs und der ausgewählten Promotions. Die erforderliche Zeit hängt von der Empfehlungslogik, dem Datenbereich, der Anzahl der Elemente im Katalog, der Menge der von Kundinnen und Kunden generierten Verhaltensdaten und der Verhaltensdatenquelle ab. Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit.

### Mboxes

Wenn Mboxes die Verhaltensdatenquelle sind, werden die Kriterien sofort nach der Erstellung ausgeführt. Je nach Menge der Verhaltensdaten und Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern.

Änderungen an der Kriterienkonfiguration führen im Allgemeinen dazu, dass der Algorithmus erneut ausgeführt wird. Abhängig von der Änderung sind die zuvor berechneten Empfehlungen möglicherweise erst verfügbar, wenn die Wiederholung abgeschlossen ist. Bei größeren Änderungen sind nur Backup- oder Standardinhalte verfügbar, bis die erneute Ausführung abgeschlossen ist.

Ein Algorithmus, der nicht geändert wird, wird je nach ausgewähltem Datenbereich automatisch alle 12-48 Stunden [!DNL Target].

### [!DNL Adobe Analytics]

Wenn [!DNL Adobe Analytics] die Verhaltensdatenquelle ist, hängt die Zeit, bis die Kriterien verfügbar sind davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden. Wenn eine Report Suite zum ersten Mal mit einem bestimmten Lookback-Fenster verwendet wird, kann es [!DNL Target Recommendations] zwei bis sieben Tage dauern, bis die Verhaltensdaten von [!DNL Analytics] heruntergeladen sind.

Informationen zum Timing neuer oder bearbeiteter Kriterien und zur Durchführung laufender Algorithmusausführungen finden Sie im Dropdown-Menü **Kriterienverfügbarkeit, wenn Analytics die Datenquelle ist** in [Data Source](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source).

>[!NOTE]
>
>**[!UICONTROL Zuletzt angezeigte Elemente]** erfordert keine Ausführung des Offline-Algorithmus, und die Ergebnisse sind sofort verfügbar. Die Algorithmen **[!UICONTROL Am häufigsten angezeigt]** und **[!UICONTROL Topverkäufe]**, die auf Mbox-Daten basieren, liefern im Allgemeinen sehr schnell Ergebnisse, da die Berechnung einfacher ist. Diese Algorithmen eignen sich gut, um eine Entwurfsänderung in der Vorschau anzuzeigen oder zu bestätigen, dass Verhaltensdaten korrekt erfasst werden.

## Vorschau mit QA-Link {#preview-qa-link}

Nachdem der Algorithmus die Ergebnisse fertig hat, können die Ergebnisse mit der Funktion [QA-Link](/help/main/c-activities/c-activity-qa/activity-qa.md) von [!DNL Adobe Target] in der Vorschau angezeigt werden. QA-Links sind im Abschnitt **[!UICONTROL Speicherort der Aktivität]** der Übersichtsseite **[!UICONTROL Aktivität]** verfügbar und zeigen die Empfehlungen auf der Seite an.

![Vorgestellte Produkte](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>Standardmäßig fügt [!DNL Target] den Benutzer automatisch der erforderlichen Zielgruppe für den QA-Link hinzu. Wenn diese Einstellung deaktiviert ist und die Aktivität über Zielgruppenbestimmungsregeln verfügt, muss das Benutzerprofil diese Zielgruppenbestimmungsregeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Der QA-Modus weist die folgenden Verhaltensweisen auf:

* [!DNL Target] QA-Modus wird in einem Cookie gespeichert und bleibt seitenübergreifend bestehen. Wenn der QA-Modus nicht beendet wird, werden die QA-Ergebnisse weiterhin auf der gesamten Site angezeigt. Um den QA-Modus zu beenden, verwenden Sie die [Lesezeichenliste](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
* Im QA-Modus wirkt sich das Durchsuchen der Site nicht auf die **[!UICONTROL Zuletzt angezeigte Artikel“]** „Zuletzt **[!UICONTROL gekaufte Artikel“]** Profils aus. Dieses Verhalten ist beabsichtigt, um eine unbeabsichtigte Verschmutzung der Produktionsverhaltensdaten zu vermeiden. Um eine Vorschau der Ergebnisse aus den Kriterien **[!UICONTROL Zuletzt angezeigte Elemente]** oder **[!UICONTROL Benutzerbasierte Empfehlungen]** anzuzeigen, durchsuchen Sie zunächst die Site außerhalb des QA-Modus und öffnen Sie dann in derselben Sitzung einen Link zum QA-Modus.

## Vorschau mit dem CSV-Download {#preview-csv}

Durch das Herunterladen der Ergebnisse können die spezifischen empfohlenen Elemente geprüft werden. Dies ist besonders hilfreich für Algorithmen wie **[!UICONTROL Personen, die dies angezeigt haben, haben das angezeigt]**, bei denen die empfohlenen Elemente von dem Element abhängen, das der Besucher derzeit anzeigt, und der Katalog kann Tausende oder Millionen verschiedener Elemente enthalten.

1. Warten Sie, bis **[!UICONTROL Status „Ergebnisse bereit]** für mindestens einen Algorithmus in der Aktivität angezeigt wird. Die Ergebnisse können nicht heruntergeladen werden.

1. Klicken Sie auf **[!UICONTROL Übersichtsseite]** Aktivität“ oben rechts auf das Menüsymbol und dann auf **[!UICONTROL Daten herunterladen]**.

   ![Option „Daten herunterladen“](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

1. Öffnen Sie die heruntergeladene CSV-Datei, um die empfohlenen Elemente anzuzeigen.

   ![Empfohlene Elemente CSV-Datei](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Die Datei listet die empfohlenen Elemente von links nach rechts auf, in diesem Beispiel die am häufigsten angezeigten. Die Empfehlungen sind durch die Umgebung getrennt. In diesem Beispiel enthält nur die Produktionsumgebung Empfehlungen.

Eine Zeile, die mit einem Sternchen (*) beginnt, listet [Sicherungselemente](/help/main/c-recommendations/c-algorithms/backup-recs.md) auf. Backup-Elemente werden angezeigt, wenn die empfohlenen Elemente des Algorithmus (Kriterien) nicht alle Slots eines Designs ausfüllen können.

Bei Algorithmen, die auf einem Schlüsselwert basieren, z. B **[!UICONTROL „Personen, die dies angezeigt haben,]** dies angezeigt haben“, befinden sich die Schlüsselwerte (die „dies“ Elemente) in der Spalte ganz links. Die empfohlenen Elemente (die „that“-Elemente) werden von links nach rechts in den Spalten Recommendation_X aufgeführt.

Bei Aktivitäten mit sehr großen Ergebnismengen schlägt die Option **[!UICONTROL Daten herunterladen]** möglicherweise mit dem Fehler fehl `Error while fetching recommendation data file.` Dies geschieht, wenn die generierte CSV die Antwortgröße überschreitet, die die Benutzeroberfläche in einem einzigen Download zurückgeben kann.

>[!NOTE]
>
>Ergebnisse-Downloads sind nicht für Aktivitäten verfügbar, die einen **[!UICONTROL benutzerbasierten Recommendations]**-Algorithmus enthalten, oder für Kriterien, die die Empfehlungslogik **[!UICONTROL Kürzlich angezeigte Elemente]** verwenden.

### CSV-Download-Format für populäritäts- und schlüsselbasierte Algorithmen {#format}

Die CSV-Download-Datei spiegelt konsistent die Ergebnisse wider, die nach der Ausführung der Backend-Kriterien generiert wurden.

* **Popularitätsbasierte Algorithmen (nicht schlüsselbasiert)**: Die Datei enthält:

  * Eine Reihe von Backup-Empfehlungen mit dem Präfix (*)
  * Eine separate Zeile, in der die Recommendations basierend auf den Algorithmuseinstellungen aufgelistet sind

* **Schlüsselbasierte Algorithmen**: Die Datei enthält:

  * Eine Sicherungszeile, wie bei populäritätsbasierten Algorithmen
  * Mehrere Zeilen im Schlüssel-Wert-Format, wobei der erste Eintrag die Produkt-ID des Schlüssels ist, gefolgt von kommagetrennten Produkt-IDs, die die Empfehlungskandidaten darstellen

## die Aktivität aktivieren {#activate-activity}

Beim Aktivieren der Aktivität wird sie gestartet und ihr Status ändert sich in **[!UICONTROL Live]**.

Klicken Sie auf der Registerkarte **[!UICONTROL Aktivitätsübersicht]** auf den **[!UICONTROL Status]**-Dropdown-Pfeil und wählen Sie dann **[!UICONTROL Aktivieren]**. Wenn sich die Aktivität derzeit im Status **[!UICONTROL Inaktiv]** befindet, wird die Dropdown-Liste mit **[!UICONTROL Inaktiv]** gekennzeichnet. Nach einigen Sekunden bis einigen Minuten wechselt der Status zu **[!UICONTROL Live]**.

Dieselbe Dropdown-Liste kann auch zum Deaktivieren oder Archivieren der Aktivität verwendet werden.

## Unterbrechungen beim Ändern von Einstellungen vermeiden {#avoid-disruptions}

Das Ändern [!DNL Recommendations] Sammlungen, Kriterien, Promotions oder Design-Einstellungen in einer Live-Aktivität kann die Algorithmusergebnisse ungültig machen und den Status eines Algorithmus in &quot;**[!UICONTROL nicht bereit“]**.

Um eine Live-Aktivität nicht zu unterbrechen, wird empfohlen, eine Kopie der Aktivität zu ändern und dann das Original zu ersetzen:

1. Duplizieren Sie die ursprüngliche Aktivität (Aktivität 1) und die zu ändernden Kriterien, um eine neue Aktivität (Aktivität 2) zu erstellen.
1. Nehmen Sie die Änderungen an der duplizierten Aktivität (Aktivität 2) und ihren Kriterien vor und warten Sie dann, bis der Algorithmus Ergebnisse generiert.
1. Zeigen Sie eine Vorschau der geänderten Aktivität (Aktivität 2) an und bestätigen Sie, dass die Ergebnisse wie gewünscht ausfallen.
1. Aktivieren Sie die neue Aktivität (Aktivität 2).
1. Deaktivieren Sie die ursprüngliche Aktivität (Aktivität 1).

Wenn die historischen Berichtsergebnisse in derselben Aktivität aufbewahrt werden müssen, ist ein alternativer Ansatz möglich. Dieser Ansatz kann die Verfügbarkeit der Empfehlungen vorübergehend beeinträchtigen:

1. Duplizieren Sie die ursprüngliche Aktivität (Aktivität 1) und die zu ändernden Kriterien, um eine neue Aktivität (Aktivität 2) zu erstellen.
1. Nehmen Sie die Änderungen an der duplizierten Aktivität (Aktivität 2) und ihren Kriterien vor und warten Sie dann, bis der Algorithmus Ergebnisse generiert.
1. Zeigen Sie eine Vorschau der geänderten Aktivität (Aktivität 2) an und bestätigen Sie, dass die Ergebnisse wie gewünscht ausfallen.
1. Hält die geänderte Aktivität an (Aktivität 2) und tauscht die Einstellungen und Kriterien in die ursprüngliche Aktivität (Aktivität 1) um.
1. Zeigen Sie eine Vorschau der ursprünglichen Aktivität (Aktivität 1) an und bestätigen Sie, dass die Ergebnisse wie gewünscht ausfallen.
1. Reaktivieren Sie die ursprüngliche Aktivität (Aktivität 1).
