---
keywords: Recommendations;Angebot;Vorschau;Start;Status;Kriterien;Algorithmus
description: Erfahren Sie, wie Sie eine Vorschau Ihrer Adobe [!DNL Target] Recommendations-Aktivität anzeigen, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten.
title: Wie starte ich eine Recommendations-Aktivität in der Vorschau?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 6e15b9b10e6a40c8efec06c45442b0f9894e648e
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 16%

---

# Vorschau und Starten Ihrer Recommendations-Aktivität

Nachdem Sie Ihre [!UICONTROL Recommendations]-, [!UICONTROL A/B Test]- oder [!UICONTROL Experience Targeting] (XT)-Aktivität mit [Recommendations-Angeboten](/help/main/c-recommendations/recommendations-as-an-offer.md) erstellt haben, sollten Sie Ihre Empfehlungen in der Vorschau anzeigen, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] bietet mehrere Möglichkeiten, Ihre Empfehlungen in der Vorschau anzuzeigen.

## Überprüfen des Recommendations-Algorithmusstatus

Nach dem Erstellen einer Aktivität führt [!DNL Recommendations] einen Algorithmus aus, um Empfehlungen zu generieren. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Im [!UICONTROL Activity] Übersichtsdiagramm, in dem der Kriterienstatus aufgeführt ist, können Sie überprüfen, ob der Algorithmus vollständig ausgeführt wurde. Die folgende Abbildung zeigt den Status im Aktivitätsdiagramm auf der [!UICONTROL Overview] einer [!DNL Recommendations] Aktivität:

![Übersichtsseite der Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status auf der Seite [!UICONTROL Overview] einer [!UICONTROL A/B Test]- oder XT-Aktivität:

![A/B-Test-Übersichtsseite](/help/main/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden, wie unten dargestellt:

* [!UICONTROL Results Ready]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Results Not Ready]: Zeigt an, dass der Algorithmus nicht beendet wurde.
* [!UICONTROL Feed Failure]: Zeigt an, dass die Feed-Datei für benutzerdefinierte Kriterien nicht abgerufen werden konnte.

![Dialogfeld „Ergebnisse“](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität mit einem Kriterium berechnet [!DNL Target] Empfehlungen basierend auf der ausgewählten Sammlung, den Kriterien, dem Design und den Promotions. Die Durchführung dieser Berechnung dauert einige Zeit, und der Zeitrahmen unterscheidet sich je nach ausgewählter Empfehlungslogik, Datenbereich, Anzahl der Elemente in Ihrem Katalog, Menge der von Ihren Kunden generierten Verhaltensdaten und ausgewählter Verhaltensdatenquelle.

Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit, wie im Folgenden dargestellt wird:

### Mboxes

Wenn Mboxes als Verhaltensdatenquelle ausgewählt wird, werden die Kriterien nach der Erstellung sofort ausgeführt. Je nach Menge der verwendeten Verhaltensdaten und der Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern. Änderungen an der Kriterienkonfiguration bewirken normalerweise eine Neuausführung des Algorithmus. Abhängig von der vorgenommenen Änderung sind die zuvor berechneten Empfehlungen möglicherweise erst nach Abschluss der erneuten Ausführung verfügbar oder bei größeren Änderungen nur Backup- oder Standardinhalte, bis die erneute Ausführung abgeschlossen ist. Wenn ein Algorithmus nicht geändert wird, wird er von [!DNL Target] je nach ausgewähltem Datumsbereich automatisch alle 12 bis 48 Stunden erneut ausgeführt.

### Adobe Analytics

Wenn das Kriterium [!DNL Adobe Analytics] als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Verfügbarkeit der Kriterien nach deren Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden.

* **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics]-Systemlast ab.
* **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn beim Erstellen eines neuen Kriteriums oder Bearbeiten eines vorhandenen Kriteriums die ausgewählte Report Suite bereits mit [!DNL Target Recommendations] verwendet wurde und der Datenbereich gleich oder kleiner dem ausgewählten Datenbereich ist, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
* **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Wenn ein Benutzer beispielsweise für die [!UICONTROL Viewed Affinity] Empfehlung ein Produkt anzeigt, wird ein Tracking-Aufruf für die Produktansicht nahezu in Echtzeit an [!DNL Analytics] übergeben. Die [!DNL Analytics] werden am nächsten Tag auf einen frühen [!DNL Target] verschoben, und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] erfordert keine Ausführung des Offline-Algorithmus und die Ergebnisse sind sofort verfügbar. [!UICONTROL Top Viewed]- und [!UICONTROL Top Sellers]-Algorithmen, die auf Mbox-Daten basieren, liefern im Allgemeinen aufgrund der einfacheren erforderlichen Berechnung sehr schnell Ergebnisse. Dies können gute Optionen sein, wenn Sie eine Entwurfsänderung in der Vorschau anzeigen oder bestätigen möchten, dass Verhaltensdaten korrekt erfasst werden.

## Verwenden von QA-Links für die Vorschau von Recommendations

Nachdem der Algorithmus die Ergebnisse fertig hat, können Sie diese Ergebnisse mit der Funktion [QA-Link](/help/main/c-activities/c-activity-qa/activity-qa.md) von [!DNL Adobe Target] in der Vorschau anzeigen. QA-Links sind im Abschnitt [!UICONTROL Activity QA] der Seite Aktivitätsübersicht verfügbar:

![Link „Aktivitäts-QA“](/help/main/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig fügt [!DNL Target] Sie automatisch zur erforderlichen Zielgruppe für den QA-Link hinzu. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Zielgruppenbestimmungsregeln hat, muss Ihr Benutzerprofil diese Zielgruppenbestimmungsregeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Mit einem QA-Link können Sie eine Vorschau der Recommendations auf Ihrer Seite anzeigen:

![Vorgestellte Produkte](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Der QA-Modus von Target ist „sticky“ und wird in einem Cookie gespeichert. Wenn Sie den QA-Modus nicht beenden, werden die QA-Ergebnisse auf der gesamten Site angezeigt. Um den QA-Modus zu beenden, verwenden Sie die [Lesezeichenliste](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* Im QA-Modus hat das Durchsuchen der Site keine Auswirkungen auf die [!UICONTROL Recently Viewed Items] oder [!UICONTROL Recently Purchased Items] Ihres Profils. Dieses Verhalten ist beabsichtigt, um eine unbeabsichtigte Verschmutzung der Produktionsverhaltensdaten zu vermeiden. Um Ergebnisse aus einem [!UICONTROL Recently Viewed Items] oder [!UICONTROL User-Based Recommendations] Kriterien in der Vorschau anzuzeigen, durchsuchen Sie die Website zunächst außerhalb des QA-Modus und öffnen Sie dann über dieselbe Sitzung einen Link für den QA-Modus.

## Verwenden des CSV-Downloads zur Vorschau der Recommendations

In einigen Fällen empfiehlt es sich, die empfohlenen spezifischen Elemente zu überprüfen. Dies ist besonders hilfreich bei der Verwendung von Algorithmen wie [!UICONTROL People Who Viewed This, Viewed That], bei denen je nach dem Element, das der Benutzer gerade anzeigt, ein anderer Satz von Elementen empfohlen wird und bei denen möglicherweise Tausende oder Millionen von verschiedenen Elementen in Ihrem Katalog vorhanden sind.

Die Ergebnisse können erst heruntergeladen werden, wenn für mindestens einen Algorithmus in der Aktivität ein [!UICONTROL Results Ready] angezeigt wird.

Um die Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol oben rechts auf der Seite Aktivitätsübersicht und dann auf **[!UICONTROL Download data]**.

![Option „Daten herunterladen“](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie sie, um die empfohlenen Elemente anzuzeigen:

![Empfohlene Elemente CSV-Datei](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste der empfohlenen Elemente, in diesem Fall die am häufigsten angezeigten. Die Empfehlungen sind durch die Umgebung getrennt. In diesem Fall enthält nur die Produktionsumgebung Empfehlungen.

Wenn ein Sternchen (*) der erste Wert einer Zeile ist, bedeutet dies [Sicherungselemente](/help/main/c-recommendations/c-algorithms/backup-recs.md). Backup-Elemente werden angezeigt, wenn nicht alle Slots in einem Design mit den empfohlenen Elementen des Algorithmus (Kriterien) gefüllt werden können.

Bei anderen Algorithmustypen, die auf einem Schlüsselwert basieren, z. B. [!UICONTROL People Who Viewed This, Viewed That], werden die Schlüsselwerte (d. h. die Elemente „This„) in der Spalte ganz links und die empfohlenen Elemente (d. h. die Elemente „That„) von links nach rechts in den Spalten Recommendation_X aufgeführt.

>[!NOTE]
>
>Ergebnis-Downloads sind nicht für Aktivitäten verfügbar, die einen [!UICONTROL User-Based Recommendations] enthalten. Ergebnis-Downloads sind für Kriterien, die die [!UICONTROL Recently-Viewed Items] Empfehlungslogik verwenden, nicht verfügbar.

## Aktivieren der Recommendations-Aktivität

Klicken Sie auf der Registerkarte [!UICONTROL Activity Overview] auf den Dropdown-Pfeil neben dem Status und wählen Sie dann **[!UICONTROL Activate]** aus.

![Option aktivieren](/help/main/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status [!UICONTROL Activating] wird:

![Wird aktiviert](/help/main/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis einigen Minuten wird der Status auf [!UICONTROL Live] geändert:

![Live](/help/main/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch über dieselbe Dropdown-Liste deaktivieren oder archivieren können.

## Unterbrechungen beim Ändern von Recommendations-Einstellungen vermeiden

Das Ändern [!DNL Recommendations] Sammlungen, Kriterien, Promotions oder Design-Einstellungen in einer Live-Aktivität kann dazu führen, dass die Algorithmusergebnisse ungültig werden und der Status eines Algorithmus in [!UICONTROL Results Not Ready] geändert wird.

Um zu vermeiden, dass eine Live-Aktivität unterbrochen wird, empfehlen wir, beim Ändern einer Live-Aktivität den folgenden Ansatz zu verwenden:

1. Duplizieren Sie die ursprüngliche Aktivität (Aktivität 1) und die Kriterien, die Sie ändern möchten, um eine neue Aktivität (Aktivität 2) zu erstellen.
1. Nehmen Sie Änderungen an der duplizierten Aktivität (Aktivität 2) und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Zeigen Sie eine Vorschau der neuen, geänderten Aktivität (Aktivität 2) an und bestätigen Sie, dass die Ergebnisse wie gewünscht sind.
1. Aktivieren Sie die neue Aktivität (Aktivität 2).
1. Deaktivieren Sie die ursprüngliche Aktivität (Aktivität 1).

Wenn Sie historische Berichtsergebnisse in derselben Aktivität beibehalten müssen, ist ein alternativer Ansatz möglich, der zu einer temporären Unterbrechung der Verfügbarkeit von Recommendations führen kann:

1. Duplizieren Sie die ursprüngliche Aktivität (Aktivität 1) und die Kriterien, die Sie ändern möchten, um eine neue Aktivität (Aktivität 2) zu erstellen.
1. Nehmen Sie Änderungen an der duplizierten Aktivität (Aktivität 2) und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Zeigen Sie eine Vorschau der neuen, geänderten Aktivität (Aktivität 2) an und bestätigen Sie, dass die Ergebnisse wie gewünscht sind.
1. Pausieren Sie die neue geänderte Aktivität (Aktivität 2) und tauschen Sie die Einstellungen/Kriterien in die ursprüngliche Aktivität (Aktivität 1) ein.
1. Zeigen Sie eine Vorschau der ursprünglichen Aktivität (Aktivität 1) an und bestätigen Sie, dass die Ergebnisse wie gewünscht ausfallen.
1. Reaktivieren Sie die ursprüngliche Aktivität (Aktivität 1).
