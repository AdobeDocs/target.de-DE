---
keywords: Recommendations;offer;preview;launch;status;criteria;algorithm
description: 'Nachdem Sie Ihre Recommendations-, A/B-Test- oder Erlebnis-Targeting-Aktivität (XT) mit Adobe Target Recommendations-Angeboten erstellt haben, sollten Sie diese Vorschau durchführen, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. Zielgruppe Recommendations Angebote bietet mehrere Möglichkeiten, Ihre Empfehlungen Vorschau. '
title: 'Nachdem Sie Ihre Recommendations-, A/B-Test- oder Erlebnis-Targeting-Aktivität (XT) mit Adobe Target Recommendations-Angeboten erstellt haben, sollten Sie diese Vorschau durchführen, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. Zielgruppe Recommendations Angebote bietet mehrere Möglichkeiten, Ihre Empfehlungen Vorschau. '
feature: recs creation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 16%

---


# Vorschau und Starten der Recommendations-Aktivität

Nachdem Sie Ihre [!UICONTROL Recommendations]-, [!UICONTROL A/B-Test]- oder [!UICONTROL Erlebnis-Targeting] -Aktivität mit [Recommendations-Angeboten](/help/c-recommendations/recommendations-as-an-offer.md)erstellt haben, sollten Sie Ihre Empfehlungen Vorschau haben, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] angebote zur Vorschau Ihrer Empfehlungen auf verschiedene Weisen.

## Überprüfen des Recommendations-Algorithmusstatus

Nach dem Erstellen einer Aktivität wird ein Algorithmus zum Generieren von Empfehlungen ausgeführt [!DNL Recommendations] . Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Sie können überprüfen, ob der Algorithmus fertig ausgeführt wurde, und zwar im Übersichtsdiagramm zur [!UICONTROL Aktivität] , in dem der Kriterienstatus aufgeführt ist. Die folgende Abbildung zeigt den Status im Diagramm &quot;Aktivität&quot;auf der Seite &quot; [!DNL Recommendations] Übersicht [!UICONTROL &quot;einer] Aktivität:

![Recommendations Aktivität - Übersichtsseite](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status auf einer [!UICONTROL A/B-Test] - oder XT-Aktivität- [!UICONTROL Übersichtsseite] :

![Seite &quot;Übersicht über A/B-Tests&quot;](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden:

* [!UICONTROL Ergebnisse bereit]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Ergebnisse nicht verfügbar]: Gibt an, dass der Algorithmus noch nicht ausgeführt wurde.
* [!UICONTROL Feed-Fehler]: Gibt an, dass die Feed-Datei mit benutzerdefinierten Kriterien nicht abgerufen werden konnte.

![Dialogfeld &quot;Ergebnisse&quot;](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität, die ein Kriterium enthält, werden Empfehlungen basierend auf der ausgewählten Sammlung, den Kriterien, dem Entwurf und den Promotions [!DNL Target] berechnet. Diese Berechnung dauert etwas länger, und der Zeitrahmen unterscheidet sich je nach ausgewählter Empfehlungslogik, Datenbereich, Anzahl der Elemente in Ihrem Katalog, Menge der von Ihren Kunden generierten Verhaltensdaten und ausgewählter verhaltensbezogener Datenquelle.

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
>[!UICONTROL Vor Kurzem aufgerufene Elemente] erfordern keinen Offline-Algorithmus, und die Ergebnisse sind sofort verfügbar. [!UICONTROL Algorithmen für die am häufigsten angezeigten] und [!UICONTROL Topverkäufe] , die auf Mbox-Daten basieren, liefern im Allgemeinen sehr schnell Ergebnisse, da eine einfachere Berechnung erforderlich ist. Dies können gute Optionen sein, wenn Sie eine Designänderung Vorschau oder sicherstellen möchten, dass Verhaltensdaten korrekt erfasst werden.

## Verwenden von QS-Links zur Vorschau Recommendations

Nachdem der Algorithmus Ergebnisse vorliegen haben, können Sie diese Ergebnisse mithilfe der [QS-Link](/help/c-activities/c-activity-qa/activity-qa.md) -Funktion von [!DNL Adobe Target]. Qualitätssicherungs-Links finden Sie im Abschnitt zur Qualitätssicherung [!UICONTROL von] Aktivitäten auf der Übersichtsseite zur Aktivität:

![Link „Aktivitäts-QA“](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig werden Sie [!DNL Target] automatisch zur erforderlichen Audience für den QA-Link hinzugefügt. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Targeting-Regeln hat, muss Ihr Profil diese Targeting-Regeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Mithilfe eines QS-Links können Sie die Empfehlungen auf Ihrer Seite Vorschau haben:

![Vorgestellte Produkte](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Der QS-Modus für Zielgruppen ist &quot;sticky&quot; und wird in einem Cookie gespeichert. Wenn Sie den Qualitätssicherungs-Modus nicht beenden, werden die Qualitätssicherungsergebnisse auf der gesamten Site angezeigt. Um den Qualitätssicherungs-Modus zu beenden, verwenden Sie das [Bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).
   >
   >
* Im Qualitätssicherungs-Modus hat das Durchsuchen der Site keine Auswirkungen auf die [!UICONTROL zuletzt angezeigten Artikel] oder die [!UICONTROL zuletzt gekauften Artikel]Ihres Profils.&quot; Dieses Verhalten wird planmäßig ausgeführt, um eine unbeabsichtigte Verschmutzung von Produktionsverhaltensdaten zu vermeiden. Zur Vorschau der Ergebnisse von [!UICONTROL kürzlich angezeigten Artikeln] oder [!UICONTROL benutzerbasierten Recommendations] -Kriterien navigieren Sie zuerst außerhalb des Qualitätssicherungs-Modus und öffnen dann in derselben Sitzung einen QS-Modus-Link.


## Verwenden des CSV-Downloads zur Vorschau von Empfehlungen

In einigen Fällen sollten Sie die empfohlenen Elemente prüfen. Dies ist besonders hilfreich, wenn Sie Algorithmen wie &quot; [!UICONTROL Personen, die das ansahen&quot;oder &quot;Angezeigt haben&quot;verwenden, wobei]je nach dem Artikel, den der Benutzer gerade anzeigt, unterschiedliche Artikel empfohlen werden und Sie möglicherweise Tausende oder Millionen von verschiedenen Artikeln in Ihrem Katalog haben.

Die Ergebnisse können erst heruntergeladen werden, wenn für mindestens einen Algorithmus in der Aktivität der Status &quot; [!UICONTROL Ergebnisbereit] &quot;angezeigt wird.

Um die Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol in der oberen rechten Ecke der Übersichtsseite der Aktivität und dann auf Daten **[!UICONTROL herunterladen]**.

![Datenoption herunterladen](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie es, um die empfohlenen Elemente anzuzeigen:

![CSV-Datei für empfohlene Elemente](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste empfohlener Artikel, in diesem Fall die am häufigsten angezeigte. Die Empfehlungen werden durch Umgebung getrennt, in diesem Fall enthält nur die Umgebung Produktion Empfehlungen. Für diesen Algorithmus haben wir keine Einschränkungen auf Basis des Schlüsselwerts angewendet. Daher enthält die mit einem Sternchen (*) beschriftete Zeile den gesamten Empfehlungssatz. Bei anderen Algorithmustypen, die auf einem Schlüsselwert basieren, wie z. B. [!UICONTROL Personen, die diesen Artikel angezeigt haben, &quot;Angezeigt darauf]&quot;, werden die Schlüsselwerte (d. h. die &quot;This&quot;-Elemente) in der Spalte ganz links aufgelistet und die empfohlenen Elemente (d. h. die &quot;that&quot;-Elemente) werden von links nach rechts in den Spalten &quot;Recommendation_X&quot;aufgelistet.

>[!NOTE]
>
>Für Aktivitäten mit einem [!UICONTROL benutzerbasierten Recommendations] -Algorithmus stehen keine Ergebnisdownloads zur Verfügung. Ergebnisdownloads stehen für Kriterien nicht zur Verfügung, die die Empfehlungslogik [!UICONTROL Zuletzt angezeigte Elemente] verwenden.

## Aktivieren der Recommendations-Aktivität

Klicken Sie auf der Registerkarte [!UICONTROL Statusübersicht] auf den Dropdownpfeil neben dem Status und wählen Sie **[!UICONTROL Aktivieren]**.

![Option aktivieren](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status zu [!UICONTROL Aktivieren]wird:

![ wird aktiviert ...](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis einigen Minuten wechselt der Status zu [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch mit derselben Dropdown-Liste deaktivieren oder archivieren können.

## Unterbrechungen beim Ändern der Recommendations-Einstellungen vermeiden

Das Ändern von [!DNL Recommendations] Sammlungen, Kriterien, Promotions oder Designeinstellungen in einer Live-Aktivität kann dazu führen, dass die Algorithmusergebnisse ungültig werden und der Status eines Algorithmus in [!UICONTROL Ergebnisse nicht bereit]geändert wird.

Um zu vermeiden, dass eine Live-Aktivität gestört wird, sollten Sie beim Ändern einer Live-Aktivität folgende Vorgehensweise anwenden:

1. Duplikat der Aktivität und der Kriterien, die Sie ändern möchten.
1. Nehmen Sie Änderungen an der duplizierten Aktivität und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Vorschau der neuen, geänderten Aktivität und Vergewissern Sie sich, dass die Ergebnisse Ihren Wünschen entsprechen.
1. Aktivieren Sie die neue Aktivität.
1. Deaktivieren Sie die alte Aktivität.

Wenn Sie historische Berichte in der gleichen Aktivität beibehalten müssen, ist ein alternativer Ansatz möglich, der die Verfügbarkeit von Empfehlungen vorübergehend beeinträchtigen könnte:

1. Duplikat der Aktivität und der Kriterien, die Sie ändern möchten.
1. Nehmen Sie Änderungen an der duplizierten Aktivität und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Vorschau der neuen, geänderten Aktivität und Vergewissern Sie sich, dass die Ergebnisse Ihren Wünschen entsprechen.
1. Halten Sie die vorhandene Aktivität an und tauschen Sie die Einstellungen/Kriterien gegen die neuen Kriterien aus.
1. Vorschau der vorhandenen Aktivität und Vergewissern Sie sich, dass die Ergebnisse den Anforderungen entsprechen.
1. Aktivieren Sie die Aktivität erneut.
