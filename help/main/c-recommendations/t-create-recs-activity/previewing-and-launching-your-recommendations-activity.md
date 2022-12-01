---
keywords: Recommendations; Angebot; Vorschau; Launch; Status; Kriterien; Algorithmus
description: Erfahren Sie, wie Sie eine Vorschau Ihrer Adobe anzeigen können. [!DNL Target] Recommendations-Aktivität, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor die Aktivität gestartet wird.
title: Wie kann ich eine Recommendations-Aktivität in der Vorschau anzeigen und starten?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 7732f3af0fd995309035a8a214afd438ab7a1823
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 17%

---

# Vorschau und Starten Ihrer Recommendations-Aktivität

Nachdem Sie Ihre [!UICONTROL Recommendations], [!UICONTROL A/B-Test]oder [!UICONTROL Erlebnis-Targeting] (XT) Aktivität, die [Recommendations-Angebote](/help/main/c-recommendations/recommendations-as-an-offer.md), sollten Sie Ihre Empfehlungen in einer Vorschau anzeigen, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] bietet mehrere Möglichkeiten, Ihre Empfehlungen in der Vorschau anzuzeigen.

## Überprüfen des Recommendations-Algorithmusstatus

Nachdem Sie eine Aktivität erstellt haben, [!DNL Recommendations] führt einen Algorithmus aus, um Empfehlungen zu generieren. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Sie können im [!UICONTROL Aktivität] Übersichtsdiagramm, in dem der Kriterienstatus aufgeführt wird. Die folgende Abbildung zeigt den Status im Aktivitätsdiagramm auf einer [!DNL Recommendations] -Aktivität [!UICONTROL Übersicht] Seite:

![Übersichtsseite der Recommendations-Aktivität](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status eines [!UICONTROL A/B-Test] oder der XT-Aktivität [!UICONTROL Übersicht] Seite:

![Seite &quot;A/B-Test-Übersicht&quot;](/help/main/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden:

* [!UICONTROL Ergebnisse bereit]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Ergebnisse nicht bereit]: Gibt an, dass der Algorithmus noch nicht abgeschlossen ist.
* [!UICONTROL Feed-Fehler]: Gibt an, dass die benutzerdefinierte Kriterien-Feed-Datei nicht abgerufen werden konnte.

![Dialogfeld &quot;Ergebnisse&quot;](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität, die ein Kriterium enthält, [!DNL Target] berechnet Empfehlungen basierend auf der ausgewählten Sammlung, den Kriterien, dem Design und den Promotions. Diese Berechnung benötigt etwas Zeit, um sie durchzuführen. Der Zeitrahmen unterscheidet sich je nach ausgewählter Empfehlungslogik, Datumsbereich, Anzahl der Elemente in Ihrem Katalog, Menge der Verhaltensdaten, die Ihre Kunden generiert haben, und ausgewählter Verhaltens-Datenquelle.

Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit, wie im Folgenden dargestellt wird:

### Mboxes

Wenn Mboxes als Verhaltensdatenquelle ausgewählt wird, werden die Kriterien nach der Erstellung sofort ausgeführt. Je nach Menge der verwendeten Verhaltensdaten und der Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern. Änderungen an der Kriterienkonfiguration bewirken normalerweise eine Neuausführung des Algorithmus. Je nach vorgenommener Änderung stehen die zuvor berechneten Empfehlungen möglicherweise erst nach Abschluss einer erneuten Ausführung zur Verfügung oder bei größeren Änderungen sind nur Backup- oder Standardinhalte verfügbar, bis eine erneute Ausführung abgeschlossen ist. Wenn ein Algorithmus nicht geändert wird, wird er von [!DNL Target] je nach ausgewähltem Datumsbereich automatisch alle 12 bis 48 Stunden erneut ausgeführt.

### Adobe Analytics

Wenn das Kriterium [!DNL Adobe Analytics] als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Verfügbarkeit der Kriterien nach deren Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden.

* **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics]-Systemlast ab.
* **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn beim Erstellen neuer Kriterien oder Bearbeiten vorhandener Kriterien die ausgewählte Report Suite bereits mit [!DNL Target Recommendations], wobei der Datenbereich kleiner oder gleich dem ausgewählten Datenbereich ist, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
* **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn sich ein Benutzer ein Produkt ansieht, wird für die Empfehlung [!UICONTROL Viewed Affinity] in nahezu Echtzeit ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] gesendet. Die [!DNL Analytics] Daten werden an [!DNL Target] Anfang des nächsten Tages und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

>[!NOTE]
>
>[!UICONTROL Vor Kurzem aufgerufene Artikel] erfordert, dass kein Offline-Algorithmus ausgeführt wird und die Ergebnisse sofort verfügbar sind. [!UICONTROL Am häufigsten angezeigt] und [!UICONTROL Topverkäufe] Algorithmen, die auf Mbox-Daten basieren, liefern aufgrund der einfacheren Berechnung im Allgemeinen sehr schnell Ergebnisse. Dies können gute Optionen sein, wenn Sie eine Entwurfsänderung in der Vorschau anzeigen oder überprüfen möchten, ob Verhaltensdaten korrekt erfasst werden.

## Verwenden von QA-Links zur Vorschau von Recommendations

Nachdem der Algorithmus die Ergebnisse fertig gestellt hat, können Sie diese Ergebnisse mit dem [QA-Link](/help/main/c-activities/c-activity-qa/activity-qa.md) Funktionalität der [!DNL Adobe Target]. QA-Links sind im Abschnitt [!UICONTROL Aktivitäts-QA] Abschnitt der Aktivitätsübersichtsseite:

![Link „Aktivitäts-QA“](/help/main/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig [!DNL Target] fügt Sie automatisch zur gewünschten Zielgruppe für den QA-Link hinzu. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Targeting-Regeln hat, muss Ihr Benutzerprofil diese Targeting-Regeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Über einen QA-Link können Sie eine Vorschau der Empfehlungen auf Ihrer Seite anzeigen:

![Vorgestellte Produkte](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Der QA-Modus von Target ist &quot;sticky&quot;und wird in einem Cookie gespeichert. Wenn Sie den QA-Modus nicht beenden, werden die QA-Ergebnisse auf der gesamten Site angezeigt. Um den QA-Modus zu beenden, verwenden Sie die [Bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* Im QA-Modus wirkt sich das Durchsuchen der Site nicht auf die [!UICONTROL Vor Kurzem aufgerufene Artikel] oder [!UICONTROL Kürzlich gekaufte Artikel]. Dieses Verhalten tritt beabsichtigt auf, um eine unbeabsichtigte Verschmutzung von Produktionsverhaltensdaten zu vermeiden. So zeigen Sie die Ergebnisse aus einer [!UICONTROL Vor Kurzem aufgerufene Artikel] oder [!UICONTROL Benutzerbasierte Recommendations] Kriterien verwenden, navigieren Sie zuerst auf der Site außerhalb des QA-Modus und öffnen dann über dieselbe Sitzung einen QA-Modus-Link.


## Verwenden des CSV-Downloads zur Vorschau von Empfehlungen

In einigen Fällen können Sie die empfohlenen spezifischen Elemente prüfen. Dies ist besonders hilfreich bei der Verwendung von Algorithmen wie [!UICONTROL Personen, die das ansahen, sahen auch dies an], wobei je nach dem Artikel, den der Benutzer gerade anzeigt, unterschiedliche Elemente empfohlen werden und Sie möglicherweise Tausende oder Millionen von verschiedenen Artikeln in Ihrem Katalog haben.

Die Ergebnisse können erst heruntergeladen werden, wenn eine [!UICONTROL Ergebnisse bereit] -Status für mindestens einen Algorithmus in der Aktivität angezeigt.

Um Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol in der oberen rechten Ecke der Aktivitätsübersichtsseite und dann auf **[!UICONTROL Daten herunterladen]**.

![Option &quot;Daten herunterladen&quot;](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie es, um die empfohlenen Elemente anzuzeigen:

![CSV-Datei mit empfohlenen Elementen](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste empfohlener Artikel, in diesem Fall am häufigsten angezeigt. Die Empfehlungen sind durch die Umgebung getrennt. In diesem Fall enthält nur die Produktionsumgebung Empfehlungen. Für diesen Algorithmus haben wir keine Einschränkungen auf der Grundlage des Schlüsselwerts angewendet. Daher enthält die mit einem Sternchen (*) beschriftete Zeile den vollständigen Satz von Empfehlungen. Für andere Algorithmustypen, die auf einem Schlüsselwert basieren, wie z. B. [!UICONTROL Personen, die das ansahen, sahen auch dies an], werden die Schlüsselwerte (d. h. die &quot;This&quot;-Elemente) in der Spalte ganz links aufgelistet und die empfohlenen Elemente (d. h. die &quot;That&quot;-Elemente) werden von links nach rechts in den Spalten &quot;Empfehlung_X&quot;aufgelistet.

>[!NOTE]
>
>Für Aktivitäten mit einer [!UICONTROL Benutzerbasierte Recommendations] -Algorithmus. Für Kriterien mit der Variablen [!UICONTROL Vor Kurzem aufgerufene Artikel] Empfehlungslogik.

## Aktivieren der Recommendations-Aktivität

Aus dem [!UICONTROL Aktivitätsübersicht] auf den Dropdown-Pfeil neben dem Status und wählen Sie **[!UICONTROL Aktivieren]**.

![Option aktivieren](/help/main/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status [!UICONTROL Aktivieren]:

![ wird aktiviert ...](/help/main/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis einigen Minuten wechselt der Status zu [!UICONTROL Live]:

![Live](/help/main/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch über dieselbe Dropdownliste deaktivieren oder archivieren können.

## Vermeiden von Unterbrechungen beim Ändern der Recommendations-Einstellungen

Ändern [!DNL Recommendations] Sammlungen, Kriterien, Promotions oder Designeinstellungen in einer Live-Aktivität können dazu führen, dass die Algorithmusergebnisse ungültig werden und der Status eines Algorithmus sich ändert in [!UICONTROL Ergebnisse nicht bereit].

Um zu vermeiden, dass eine Live-Aktivität gestört wird, empfehlen wir beim Ändern einer Live-Aktivität den folgenden Ansatz:

1. Duplizieren Sie die ursprüngliche Aktivität (Aktivität 1) und die Kriterien, die Sie ändern möchten, um eine neue Aktivität zu erstellen (Aktivität 2).
1. Nehmen Sie Änderungen an der duplizierten Aktivität (Aktivität 2) und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Sehen Sie sich die neue, geänderte Aktivität (Aktivität 2) in der Vorschau an und überprüfen Sie, ob die Ergebnisse Ihren Anforderungen entsprechen.
1. Aktivieren Sie die neue Aktivität (Aktivität 2).
1. Deaktivieren Sie die ursprüngliche Aktivität (Aktivität 1).

Wenn Sie die historischen Berichtsergebnisse in derselben Aktivität beibehalten müssen, ist ein alternativer Ansatz möglich, der zu einer vorübergehenden Unterbrechung der Empfehlungsverfügbarkeit führen kann:

1. Duplizieren Sie die ursprüngliche Aktivität (Aktivität 1) und die Kriterien, die Sie ändern möchten, um eine neue Aktivität zu erstellen (Aktivität 2).
1. Nehmen Sie Änderungen an der duplizierten Aktivität (Aktivität 2) und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Sehen Sie sich die neue, geänderte Aktivität (Aktivität 2) in der Vorschau an und überprüfen Sie, ob die Ergebnisse Ihren Anforderungen entsprechen.
1. Halten Sie die neue, geänderte Aktivität an (Aktivität 2) und tauschen Sie die Einstellungen/Kriterien auf die ursprüngliche Aktivität (Aktivität 1) aus.
1. Überprüfen Sie die Vorschau der ursprünglichen Aktivität (Aktivität 1) und bestätigen Sie, dass die Ergebnisse wie gewünscht sind.
1. Reaktivieren Sie die ursprüngliche Aktivität (Aktivität 1).
