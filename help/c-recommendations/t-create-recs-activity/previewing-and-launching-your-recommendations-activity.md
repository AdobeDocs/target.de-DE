---
keywords: Recommendations;Angebot;Vorschau;Start
description: 'Nachdem Sie Ihre Recommendations-, A/B-Test- oder Erlebnis-Targeting-Aktivität (XT) mit Adobe Target Recommendations-Angeboten erstellt haben, sollten Sie eine Vorschau davon anzeigen, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. Target Recommendations bietet mehrere Möglichkeiten zur Vorschau Ihrer Empfehlungen. '
title: 'Nachdem Sie Ihre Recommendations-, A/B-Test- oder Erlebnis-Targeting-Aktivität (XT) mit Adobe Target Recommendations-Angeboten erstellt haben, sollten Sie eine Vorschau davon anzeigen, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. Target Recommendations bietet mehrere Möglichkeiten zur Vorschau Ihrer Empfehlungen. '
subtopic: Recommendations
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Vorschau Ihrer Recommendations-Aktivität anzeigen und starten

Nachdem Sie Ihre [!UICONTROL Recommendations]-, [!UICONTROL A/B-Test]- oder [!UICONTROL Erlebnis-Targeting] -Aktivität mit [Recommendations-Angeboten](/help/c-recommendations/recommendations-as-an-offer.md)erstellt haben, sollten Sie eine Vorschau Ihrer Empfehlungen anzeigen, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] bietet mehrere Möglichkeiten zur Vorschau Ihrer Empfehlungen.

## Status des Recommendations-Algorithmus überprüfen

Nach dem Erstellen einer Aktivität wird ein Algorithmus zum Generieren von Empfehlungen [!DNL Recommendations] ausgeführt. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Sie können prüfen, ob der Algorithmus im Übersichtsdiagramm [!UICONTROL Aktivität] , in dem der Kriterienstatus aufgeführt ist, ausgeführt wurde. Die folgende Abbildung zeigt den Status im Aktivitätsdiagramm auf der Seite " [!DNL Recommendations]Übersicht[!UICONTROL  "einer ] Aktivität:

![Recommendations-Aktivitätsübersichtsseite](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status auf der Seite [!UICONTROL A/B-Test] oder XT-Aktivität [!UICONTROL Übersicht] :

![Seite "Übersicht über A/B-Tests"](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden:

* [!UICONTROL Ergebnisse bereit]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Ergebnisse nicht verfügbar]: Gibt an, dass der Algorithmus noch nicht ausgeführt wurde.
* [!UICONTROL Feed-Fehler]: Gibt an, dass die Feed-Datei mit benutzerdefinierten Kriterien nicht abgerufen werden konnte.

![Dialogfeld "Ergebnisse"](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität, die ein Kriterium enthält, werden Empfehlungen basierend auf der ausgewählten Sammlung, den ausgewählten Kriterien, dem Entwurf und den ausgewählten Promotions [!DNL Target] berechnet. Diese Berechnung nimmt etwas Zeit in Anspruch. Der Zeitrahmen hängt von der ausgewählten Empfehlungslogik, dem Datumsbereich, der Anzahl der Elemente in Ihrem Katalog, der Anzahl der Verhaltensdaten Ihrer Kunden und der ausgewählten Verhaltensdatenquelle ab.

Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit, wie im Folgenden dargestellt wird:

### Mboxes

Wenn Mboxes als Verhaltensdatenquelle ausgewählt wird, werden die Kriterien nach der Erstellung sofort ausgeführt. Je nach Menge der verwendeten Verhaltensdaten und der Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern. Änderungen an der Kriterienkonfiguration bewirken normalerweise eine Neuausführung des Algorithmus. Je nach vorgenommener Änderung stehen die zuvor berechneten Empfehlungen möglicherweise erst nach Abschluss einer erneuten Ausführung zur Verfügung oder bei größeren Änderungen sind nur Backup- oder Standardinhalte verfügbar, bis eine erneute Ausführung abgeschlossen ist. Wenn ein Algorithmus nicht geändert wird, wird er von [!DNL Target] je nach ausgewähltem Datumsbereich automatisch alle 12 bis 48 Stunden erneut ausgeführt.

### Adobe Analytics

Wenn das Kriterium [!DNL Adobe Analytics] als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Verfügbarkeit der Kriterien nach deren Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden.

* **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics]-Systemlast ab.
* **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn beim Erstellen eines neuen Kriteriums oder Bearbeiten eines vorhandenen Kriteriums die ausgewählte Report Suite bereits verwendet wurde [!DNL Target Recommendations], wobei der Datenbereich mindestens dem ausgewählten Datenbereich entspricht, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
* **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn sich ein Benutzer ein Produkt ansieht, wird für die Empfehlung [!UICONTROL Viewed Affinity] in nahezu Echtzeit ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] gesendet. The [!DNL Analytics] data is pushed to [!DNL Target] early the next day and [!DNL Target] runs the algorithm in fewer than 12 hours.

>[!NOTE]
>
>[!UICONTROL Kürzlich angezeigte Elemente] erfordern keinen Offline-Algorithmus, und die Ergebnisse sind sofort verfügbar. [!UICONTROL Algorithmen für die am häufigsten angezeigten] und [!UICONTROL Topverkäufe] , die auf Mbox-Daten basieren, liefern im Allgemeinen sehr schnell Ergebnisse, da eine einfachere Berechnung erforderlich ist. Dies können gute Optionen sein, wenn Sie eine Designänderung in der Vorschau anzeigen oder bestätigen möchten, dass Verhaltensdaten korrekt erfasst werden.

## Verwenden von QS-Links zur Vorschau von Recommendations

Nachdem der Algorithmus Ergebnisse vorliegen haben, können Sie eine Vorschau dieser Ergebnisse mit der [QS-Link](/help/c-activities/c-activity-qa/activity-qa.md) -Funktion von [!DNL Adobe Target]. Qualitätssicherungs-Links finden Sie im Abschnitt [!UICONTROL Aktivitätsprüfung] auf der Seite Aktivitätsübersicht:

![Link „Aktivitäts-QA“](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig werden Sie [!DNL Target] automatisch zur gewünschten Zielgruppe für den QA-Link hinzugefügt. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Targeting-Regeln hat, muss Ihr Benutzerprofil diese Targeting-Regeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Mithilfe eines QS-Links können Sie eine Vorschau der Empfehlungen auf Ihrer Seite anzeigen:

![Vorgestellte Produkte](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>Der QS-Modus von Target ist "sticky"und wird in einem Cookie gespeichert. Wenn Sie den QS-Modus nicht beenden, werden die Qualitätssicherungsergebnisse auf der gesamten Site angezeigt. Um den Qualitätssicherungs-Modus zu beenden, verwenden Sie das [Bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).

>[!NOTE]
>
>Im Qualitätssicherungs-Modus hat das Durchsuchen der Site keine Auswirkungen auf die [!UICONTROL zuletzt angezeigten Artikel] oder die [!UICONTROL zuletzt gekauften Artikel]Ihres Profils. Dieses Verhalten wird standardmäßig ausgeführt, um eine unbeabsichtigte Verschmutzung der Produktionsverhaltensdaten zu vermeiden. Um die Ergebnisse von [!UICONTROL kürzlich angezeigten Artikeln] oder [!UICONTROL benutzerbasierten Recommendations] -Kriterien in der Vorschau anzuzeigen, navigieren Sie zunächst außerhalb des Qualitätssicherungs-Modus zu der Site und öffnen Sie dann in derselben Sitzung einen Link zum Qualitätssicherungsmodus.

## Verwenden des CSV-Downloads zur Vorschau von Empfehlungen

In einigen Fällen sollten Sie die empfohlenen Elemente prüfen. Dies ist besonders hilfreich, wenn Sie Algorithmen wie " [!UICONTROL Personen, die das ansahen"oder "Angezeigt haben"verwenden, wobei]je nach dem Artikel, den der Benutzer gerade anzeigt, unterschiedliche Artikel empfohlen werden und Sie möglicherweise Tausende oder Millionen von verschiedenen Artikeln in Ihrem Katalog haben.

Ergebnisse können erst heruntergeladen werden, wenn für mindestens einen Algorithmus in der Aktivität der Status [!UICONTROL Ergebnisbereit] angezeigt wird.

Um Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol in der oberen rechten Ecke der Seite "Aktivitätsübersicht"und dann auf Daten **[!UICONTROL herunterladen]**.

![Datenoption herunterladen](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie es, um die empfohlenen Elemente anzuzeigen:

![CSV-Datei für empfohlene Elemente](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste empfohlener Artikel, in diesem Fall die am häufigsten angezeigte. Die Empfehlungen werden durch die Umgebung getrennt, in diesem Fall enthält nur die Produktionsumgebung Empfehlungen. Für diesen Algorithmus haben wir keine Einschränkungen auf Basis des Schlüsselwerts angewendet. Daher enthält die mit einem Sternchen (*) beschriftete Zeile den gesamten Empfehlungssatz. Bei anderen Algorithmustypen, die auf einem Schlüsselwert basieren, wie z. B. [!UICONTROL Personen, die diesen Artikel angezeigt haben, "Angezeigt darauf]", werden die Schlüsselwerte (d. h. die "This"-Elemente) in der Spalte ganz links aufgelistet und die empfohlenen Elemente (d. h. die "that"-Elemente) werden von links nach rechts in den Spalten Recommendation_X aufgeführt.

>[!NOTE]
>
>Ergebnisdownloads sind nicht für Aktivitäten verfügbar, die einen [!UICONTROL benutzerbasierten Recommendations] -Algorithmus enthalten. Ergebnisdownloads stehen für Kriterien nicht zur Verfügung, die die Empfehlungslogik [!UICONTROL Zuletzt angezeigte Elemente] verwenden.

## Aktivieren Ihrer Recommendations-Aktivität

Klicken Sie auf der Registerkarte [!UICONTROL Aktivitätsübersicht] auf den Dropdownpfeil neben dem Status und wählen Sie dann **[!UICONTROL Aktivieren]**.

![Option aktivieren](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status zu [!UICONTROL Aktivieren]wird:

![ wird aktiviert ...](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis einigen Minuten wechselt der Status zu [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch über dieselbe Dropdownliste deaktivieren oder archivieren können.

## Unterbrechungen beim Ändern der Recommendations-Einstellungen vermeiden

Das Ändern von [!DNL Recommendations] Sammlungen, Kriterien, Promotions oder Designeinstellungen in einer Live-Aktivität kann dazu führen, dass die Algorithmusergebnisse ungültig werden und der Status eines Algorithmus sich in [!UICONTROL Ergebnisse nicht bereit]ändert.

Um zu vermeiden, dass eine Live-Aktivität gestört wird, sollten Sie beim Ändern einer Live-Aktivität den folgenden Ansatz wählen:

1. Duplizieren Sie die Aktivität und die Kriterien, die Sie ändern möchten.
1. Nehmen Sie Änderungen an der duplizierten Aktivität und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Sehen Sie sich die neue, geänderte Aktivität in der Vorschau an und stellen Sie sicher, dass die Ergebnisse den Anforderungen entsprechen.
1. Aktivieren Sie die neue Aktivität.
1. Deaktivieren Sie die alte Aktivität.

Wenn Sie historische Berichtsergebnisse in derselben Aktivität beibehalten müssen, ist ein alternativer Ansatz möglich, der die Verfügbarkeit von Empfehlungen vorübergehend beeinträchtigen könnte:

1. Duplizieren Sie die Aktivität und die Kriterien, die Sie ändern möchten.
1. Nehmen Sie Änderungen an der duplizierten Aktivität und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Sehen Sie sich die neue, geänderte Aktivität in der Vorschau an und stellen Sie sicher, dass die Ergebnisse den Anforderungen entsprechen.
1. Halten Sie die vorhandene Aktivität an und tauschen Sie die Einstellungen/Kriterien gegen die neuen Kriterien aus.
1. Zeigen Sie die vorhandene Aktivität in der Vorschau an und bestätigen Sie, dass die Ergebnisse den Anforderungen entsprechen.
1. Aktivieren Sie die Aktivität erneut.
