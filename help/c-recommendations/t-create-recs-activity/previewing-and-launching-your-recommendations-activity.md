---
keywords: Recommendations;Angebot;Vorschau;Start;Status;Kriterien;Algorithmus
description: 'Erfahren Sie, wie Sie Ihre Adobe Target Recommendations-Aktivität so Vorschau haben, dass sichergestellt ist, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. '
title: Wie kann ich eine Recommendations-Aktivität starten und Vorschau durchführen?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 17%

---


# Vorschau und Starten der Recommendations-Aktivität

Nachdem Sie die Aktivität [!UICONTROL Recommendations], [!UICONTROL A/B-Test] oder [!UICONTROL Erlebnis-Targeting] (XT) mit [Recommendations-Angeboten](/help/c-recommendations/recommendations-as-an-offer.md) erstellt haben, sollten Sie Ihre Empfehlungen Vorschau haben, um sicherzustellen, dass die Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] angebote zur Vorschau Ihrer Empfehlungen auf verschiedene Weisen.

## Überprüfen des Recommendations-Algorithmusstatus

Nach dem Erstellen einer Aktivität führt [!DNL Recommendations] einen Algorithmus aus, um Empfehlungen zu generieren. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Sie können überprüfen, ob der Algorithmus im Übersichtsdiagramm [!UICONTROL Aktivität] ausgeführt wurde, in dem der Kriterienstatus aufgelistet ist. Die folgende Abbildung zeigt den Status im Diagramm &quot;Aktivität&quot;auf einer [!DNL Recommendations] Aktivität [!UICONTROL Übersicht]:

![Recommendations Aktivität - Übersichtsseite](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status auf einer [!UICONTROL A/B-Test]- oder XT-Aktivität [!UICONTROL Übersichtsseite]:

![Seite &quot;Übersicht über A/B-Tests&quot;](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden:

* [!UICONTROL Ergebnisse bereit]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Ergebnisse nicht verfügbar]: Gibt an, dass der Algorithmus noch nicht ausgeführt wurde.
* [!UICONTROL Feed-Fehler]: Gibt an, dass die Feed-Datei mit benutzerdefinierten Kriterien nicht abgerufen werden konnte.

![Dialogfeld &quot;Ergebnisse&quot;](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität, die ein Kriterium enthält, berechnet [!DNL Target] Empfehlungen basierend auf der ausgewählten Sammlung, den Kriterien, dem Entwurf und den Promotions. Diese Berechnung dauert etwas länger, und der Zeitrahmen unterscheidet sich je nach ausgewählter Empfehlungslogik, Datenbereich, Anzahl der Elemente in Ihrem Katalog, Menge der von Ihren Kunden generierten Verhaltensdaten und ausgewählter verhaltensbezogener Datenquelle.

Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit, wie im Folgenden dargestellt wird:

### Mboxes

Wenn Mboxes als Verhaltensdatenquelle ausgewählt wird, werden die Kriterien nach der Erstellung sofort ausgeführt. Je nach Menge der verwendeten Verhaltensdaten und der Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern. Änderungen an der Kriterienkonfiguration bewirken normalerweise eine Neuausführung des Algorithmus. Je nach vorgenommener Änderung stehen die zuvor berechneten Empfehlungen möglicherweise erst nach Abschluss einer erneuten Ausführung zur Verfügung oder bei größeren Änderungen sind nur Backup- oder Standardinhalte verfügbar, bis eine erneute Ausführung abgeschlossen ist. Wenn ein Algorithmus nicht geändert wird, wird er von [!DNL Target] je nach ausgewähltem Datumsbereich automatisch alle 12 bis 48 Stunden erneut ausgeführt.

### Adobe Analytics

Wenn das Kriterium [!DNL Adobe Analytics] als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Verfügbarkeit der Kriterien nach deren Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden.

* **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics]-Systemlast ab.
* **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn beim Erstellen eines neuen Kriteriums oder Bearbeiten eines vorhandenen Kriteriums die ausgewählte Report Suite bereits verwendet wurde  [!DNL Target Recommendations], wobei der Datenbereich mindestens dem ausgewählten Datenbereich entspricht, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
* **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn sich ein Benutzer ein Produkt ansieht, wird für die Empfehlung [!UICONTROL Viewed Affinity] in nahezu Echtzeit ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] gesendet. Die [!DNL Analytics]-Daten werden am nächsten Tag an [!DNL Target] Anfang gesendet und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

>[!NOTE]
>
>[!UICONTROL Vor Kurzem aufgerufene ] Elemente erfordern keinen Offline-Algorithmus, und die Ergebnisse sind sofort verfügbar. [!UICONTROL Top-] Viewer- und  [!UICONTROL Top-] Sellersalgorithmen, die auf Mbox-Daten basieren, liefern aufgrund der vereinfachten Berechnung im Allgemeinen sehr schnell Ergebnisse. Dies können gute Optionen sein, wenn Sie eine Designänderung Vorschau oder sicherstellen möchten, dass Verhaltensdaten korrekt erfasst werden.

## Verwenden von QS-Links zur Vorschau Recommendations

Nachdem der Algorithmus Ergebnisse vorliegen haben, können Sie diese Ergebnisse mit der [QA-Link](/help/c-activities/c-activity-qa/activity-qa.md)-Funktion von [!DNL Adobe Target] Vorschau haben. Die QS-Links finden Sie im Abschnitt [!UICONTROL Aktivität QA] auf der Übersichtsseite zur Aktivität:

![Link „Aktivitäts-QA“](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig fügt [!DNL Target] Sie automatisch zur erforderlichen Audience für den QA-Link hinzu. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Targeting-Regeln hat, muss Ihr Profil diese Targeting-Regeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Mithilfe eines QS-Links können Sie die Empfehlungen auf Ihrer Seite Vorschau haben:

![Vorgestellte Produkte](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Der QS-Modus für Zielgruppen ist &quot;sticky&quot; und wird in einem Cookie gespeichert. Wenn Sie den Qualitätssicherungs-Modus nicht beenden, werden die Qualitätssicherungsergebnisse auf der gesamten Site angezeigt. Um den QA-Modus zu beenden, verwenden Sie das Lesezeichen [a1/>.](/help/c-activities/c-activity-qa/activity-qa-bookmark.md)
   >
   >
* Im QA-Modus hat das Durchsuchen der Site keine Auswirkungen auf die kürzlich angezeigten Elemente [!UICONTROL oder [!UICONTROL Zuletzt gekaufte Artikel] Ihres Profils.&quot; ] Dieses Verhalten wird planmäßig ausgeführt, um eine unbeabsichtigte Verschmutzung von Produktionsverhaltensdaten zu vermeiden. Zur Vorschau der Ergebnisse eines Kriteriums [!UICONTROL Zuletzt angezeigte Elemente] oder [!UICONTROL Benutzerbasierte Recommendations] durchsuchen Sie zunächst die Site außerhalb des Qualitätssicherungs-Modus und öffnen dann in derselben Sitzung einen Link zum Qualitätssicherungs-Modus.


## Verwenden des CSV-Downloads zur Vorschau von Empfehlungen

In einigen Fällen sollten Sie die empfohlenen Elemente prüfen. Dies ist besonders hilfreich, wenn Sie Algorithmen wie [!UICONTROL Personen verwenden, die diese Ansicht angezeigt haben, und dies] anzeigen, wobei je nach dem Artikel, den der Benutzer gerade anzeigt, unterschiedliche Elemente empfohlen werden und Sie möglicherweise Tausende oder Millionen von verschiedenen Elementen in Ihrem Katalog haben.

Die Ergebnisse können erst heruntergeladen werden, wenn für mindestens einen Algorithmus in der Aktivität der Status [!UICONTROL Ergebnisse bereit] angezeigt wird.

Um Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol in der oberen rechten Ecke der Übersichtsseite der Aktivität und dann auf **[!UICONTROL Daten herunterladen]**.

![Datenoption herunterladen](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie es, um die empfohlenen Elemente anzuzeigen:

![CSV-Datei für empfohlene Elemente](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste empfohlener Artikel, in diesem Fall die am häufigsten angezeigte. Die Empfehlungen werden durch Umgebung getrennt, in diesem Fall enthält nur die Umgebung Produktion Empfehlungen. Für diesen Algorithmus haben wir keine Einschränkungen auf Basis des Schlüsselwerts angewendet. Daher enthält die mit einem Sternchen (*) beschriftete Zeile den gesamten Empfehlungssatz. Bei anderen Algorithmustypen, die auf einem Schlüsselwert basieren, wie [!UICONTROL Personen, die diesen Wert angezeigt haben, &quot;Angezeigt&quot;], werden die Schlüsselwerte (d.h. die &quot;This&quot;-Elemente) in der Spalte ganz links aufgelistet und die empfohlenen Elemente (d.h. die &quot;that&quot;-Elemente) werden von links nach rechts in den Spalten &quot;Recommendation_X&quot;aufgelistet.

>[!NOTE]
>
>Für Aktivitäten mit einem [!UICONTROL Benutzerbasierten Recommendations]-Algorithmus sind keine Ergebnisdownloads verfügbar. Ergebnisdownloads sind für Kriterien mit der Empfehlungslogik [!UICONTROL Zuletzt angezeigte Elemente] nicht verfügbar.

## Aktivieren der Recommendations-Aktivität

Klicken Sie auf der Registerkarte [!UICONTROL Übersicht über Aktivitäten] auf den Dropdownpfeil neben dem Status und wählen Sie **[!UICONTROL Aktivieren]**.

![Option aktivieren](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status zu [!UICONTROL Aktivieren] wird:

![ wird aktiviert ...](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis ein paar Minuten wechselt der Status zu [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch mit derselben Dropdown-Liste deaktivieren oder archivieren können.

## Unterbrechungen beim Ändern der Recommendations-Einstellungen vermeiden

Wenn Sie Sammlungen, Kriterien, Promotions oder Designeinstellungen in einer Live-Aktivität ändern, können die Algorithmusergebnisse ungültig werden und der Algorithmusstatus in [!UICONTROL Ergebnisse nicht bereit] geändert werden.[!DNL Recommendations]

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
