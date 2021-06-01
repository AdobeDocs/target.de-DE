---
keywords: Recommendations; Angebot; Vorschau; Launch; Status; Kriterien; Algorithmus
description: 'Erfahren Sie, wie Sie eine Vorschau Ihrer Adobe [!DNL Target] Recommendations-Aktivität anzeigen können, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. '
title: Wie kann ich eine Recommendations-Aktivität in der Vorschau anzeigen und starten?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: f4972f04906cb3476f50abedd6cec847e015daf9
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 17%

---

# Vorschau und Starten Ihrer Recommendations-Aktivität

Nachdem Sie die Aktivität [!UICONTROL Recommendations], [!UICONTROL A/B-Test] oder [!UICONTROL Erlebnis-Targeting] (XT)-Aktivität mit [Recommendations-Angeboten](/help/c-recommendations/recommendations-as-an-offer.md) erstellt haben, sollten Sie eine Vorschau Ihrer Empfehlungen anzeigen, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] bietet mehrere Möglichkeiten, Ihre Empfehlungen in der Vorschau anzuzeigen.

## Überprüfen des Recommendations-Algorithmusstatus

Nach Erstellung einer Aktivität führt [!DNL Recommendations] einen Algorithmus aus, um Empfehlungen zu generieren. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Sie können überprüfen, ob der Algorithmus im Übersichtsdiagramm [!UICONTROL Aktivität] ausgeführt wurde, in dem der Kriterienstatus aufgeführt ist. Die folgende Abbildung zeigt den Status im Aktivitätsdiagramm auf der Seite [!DNL Recommendations] der Aktivität [!UICONTROL Übersicht] :

![Übersichtsseite der Recommendations-Aktivität](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status auf einer [!UICONTROL A/B-Test]- oder XT-Aktivitätsseite [!UICONTROL Überblick]:

![Seite &quot;A/B-Test-Übersicht&quot;](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden:

* [!UICONTROL Ergebnisse bereit]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Ergebnisse nicht bereit]: Gibt an, dass der Algorithmus noch nicht abgeschlossen ist.
* [!UICONTROL Feed-Fehler]: Gibt an, dass die benutzerdefinierte Kriterien-Feed-Datei nicht abgerufen werden konnte.

![Dialogfeld &quot;Ergebnisse&quot;](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität, die ein Kriterium enthält, berechnet [!DNL Target] Empfehlungen basierend auf der ausgewählten Sammlung, den Kriterien, dem Design und den Promotions. Diese Berechnung benötigt etwas Zeit, um sie durchzuführen. Der Zeitrahmen unterscheidet sich je nach ausgewählter Empfehlungslogik, Datumsbereich, Anzahl der Elemente in Ihrem Katalog, Menge der Verhaltensdaten, die Ihre Kunden generiert haben, und ausgewählter Verhaltens-Datenquelle.

Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit, wie im Folgenden dargestellt wird:

### Mboxes

Wenn Mboxes als Verhaltensdatenquelle ausgewählt wird, werden die Kriterien nach der Erstellung sofort ausgeführt. Je nach Menge der verwendeten Verhaltensdaten und der Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern. Änderungen an der Kriterienkonfiguration bewirken normalerweise eine Neuausführung des Algorithmus. Je nach vorgenommener Änderung stehen die zuvor berechneten Empfehlungen möglicherweise erst nach Abschluss einer erneuten Ausführung zur Verfügung oder bei größeren Änderungen sind nur Backup- oder Standardinhalte verfügbar, bis eine erneute Ausführung abgeschlossen ist. Wenn ein Algorithmus nicht geändert wird, wird er von [!DNL Target] je nach ausgewähltem Datumsbereich automatisch alle 12 bis 48 Stunden erneut ausgeführt.

### Adobe Analytics

Wenn das Kriterium [!DNL Adobe Analytics] als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Verfügbarkeit der Kriterien nach deren Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden.

* **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics]-Systemlast ab.
* **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn beim Erstellen eines neuen Kriteriums oder Bearbeiten eines vorhandenen Kriteriums die ausgewählte Report Suite bereits mit verwendet wurde und  [!DNL Target Recommendations]der Datenbereich kleiner oder gleich dem ausgewählten Datenbereich ist, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
* **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn sich ein Benutzer ein Produkt ansieht, wird für die Empfehlung [!UICONTROL Viewed Affinity] in nahezu Echtzeit ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] gesendet. Die [!DNL Analytics]-Daten werden am nächsten Tag an [!DNL Target] Anfang gesendet und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

>[!NOTE]
>
>[!UICONTROL Für kürzlich angezeigte ] Elemente ist kein Offline-Algorithmus erforderlich und die Ergebnisse sind sofort verfügbar. [!UICONTROL Die ] Top-Viewer- und  [!UICONTROL Top-] Sellersalgorithmen, die auf Mbox-Daten basieren, liefern im Allgemeinen sehr schnell Ergebnisse aufgrund der einfacheren Berechnung, die erforderlich ist. Dies können gute Optionen sein, wenn Sie eine Entwurfsänderung in der Vorschau anzeigen oder überprüfen möchten, ob Verhaltensdaten korrekt erfasst werden.

## Verwenden von QA-Links zur Vorschau von Recommendations

Nachdem der Algorithmus Ergebnisse bereitgestellt hat, können Sie diese Ergebnisse mit der [QA-Link](/help/c-activities/c-activity-qa/activity-qa.md)-Funktion von [!DNL Adobe Target] in der Vorschau anzeigen. QA-Links sind im Abschnitt [!UICONTROL Aktivitäts-QA] der Aktivitäts-Übersichtsseite verfügbar:

![Link „Aktivitäts-QA“](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig fügt [!DNL Target] Sie automatisch zur erforderlichen Audience für den QA-Link hinzu. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Targeting-Regeln hat, muss Ihr Benutzerprofil diese Targeting-Regeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Über einen QA-Link können Sie eine Vorschau der Empfehlungen auf Ihrer Seite anzeigen:

![Vorgestellte Produkte](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Der QA-Modus von Target ist &quot;sticky&quot;und wird in einem Cookie gespeichert. Wenn Sie den QA-Modus nicht beenden, werden die QA-Ergebnisse auf der gesamten Site angezeigt. Um den QA-Modus zu beenden, verwenden Sie das [Bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).
   >
   >
* Im QA-Modus wirkt sich das Durchsuchen der Site nicht auf die [!UICONTROL Zuletzt angezeigten Elemente] oder [!UICONTROL Zuletzt gekaufte Artikel] aus. Dieses Verhalten tritt beabsichtigt auf, um eine unbeabsichtigte Verschmutzung von Produktionsverhaltensdaten zu vermeiden. Um die Ergebnisse eines [!UICONTROL Kürzlich angezeigten Elements] oder [!UICONTROL Benutzerbasierten Recommendations]-Kriteriums in der Vorschau anzuzeigen, navigieren Sie zuerst außerhalb des QA-Modus zu der Site und öffnen dann dieselbe Sitzung, um einen QA-Modus-Link zu öffnen.


## Verwenden des CSV-Downloads zur Vorschau von Empfehlungen

In einigen Fällen können Sie die empfohlenen spezifischen Elemente prüfen. Dies ist besonders hilfreich bei der Verwendung von Algorithmen wie [!UICONTROL Personen, die das ansahen, sahen auch dies] an, wobei je nach dem vom Benutzer angezeigten Element unterschiedliche Artikel empfohlen werden und Sie möglicherweise Tausende oder Millionen von verschiedenen Artikeln in Ihrem Katalog haben.

Ergebnisse können erst heruntergeladen werden, wenn für mindestens einen Algorithmus in der Aktivität der Status [!UICONTROL Ergebnisse bereit] angezeigt wird.

Um Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol in der oberen rechten Ecke der Aktivitätsübersichtsseite und dann auf **[!UICONTROL Daten herunterladen]**.

![Option &quot;Daten herunterladen&quot;](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie es, um die empfohlenen Elemente anzuzeigen:

![CSV-Datei mit empfohlenen Elementen](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste empfohlener Artikel, in diesem Fall am häufigsten angezeigt. Die Empfehlungen sind durch die Umgebung getrennt. In diesem Fall enthält nur die Produktionsumgebung Empfehlungen. Für diesen Algorithmus haben wir keine Einschränkungen auf der Grundlage des Schlüsselwerts angewendet. Daher enthält die mit einem Sternchen (*) beschriftete Zeile den vollständigen Satz von Empfehlungen. Bei anderen Algorithmustypen, die auf einem Schlüsselwert basieren, wie [!UICONTROL Personen, die diesen Wert angezeigt haben, sahen auch dies an], werden die Schlüsselwerte (d. h. die &quot;This&quot;-Elemente) in der Spalte ganz links aufgelistet und die empfohlenen Elemente (d. h. die &quot;That&quot;-Elemente) werden von links nach rechts in den Spalten &quot;Recommendation_X&quot;aufgelistet.

>[!NOTE]
>
>Für Aktivitäten mit einem [!UICONTROL Benutzerbasierten Recommendations]-Algorithmus sind keine Ergebnisdownloads verfügbar. Für Kriterien, die die Empfehlungslogik [!UICONTROL Kürzlich angezeigte Elemente] verwenden, sind keine Ergebnisse-Downloads verfügbar.

## Aktivieren der Recommendations-Aktivität

Klicken Sie auf der Registerkarte [!UICONTROL Aktivitätsübersicht] auf den Dropdown-Pfeil neben dem Status und wählen Sie dann **[!UICONTROL Aktivieren]** aus.

![Option aktivieren](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status [!UICONTROL Aktivieren] lautet:

![ wird aktiviert ...](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis zu einigen Minuten wechselt der Status zu [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch über dieselbe Dropdownliste deaktivieren oder archivieren können.

## Vermeiden von Unterbrechungen beim Ändern der Recommendations-Einstellungen

Eine Änderung von [!DNL Recommendations] -Sammlungen, -Kriterien, -Promotions oder -Designeinstellungen in einer Live-Aktivität kann dazu führen, dass die Algorithmusergebnisse ungültig werden und der Status eines Algorithmus sich zu [!UICONTROL Ergebnisse nicht bereit] ändert.

Um zu vermeiden, dass eine Live-Aktivität gestört wird, empfehlen wir beim Ändern einer Live-Aktivität den folgenden Ansatz:

1. Duplizieren Sie die Aktivität und die Kriterien, die Sie ändern möchten.
1. Nehmen Sie Änderungen an der duplizierten Aktivität und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Sehen Sie sich die neue, geänderte Aktivität in der Vorschau an und überprüfen Sie, ob die Ergebnisse Ihren Anforderungen entsprechen.
1. Aktivieren Sie die neue Aktivität.
1. Deaktivieren Sie die alte Aktivität.

Wenn Sie die historischen Berichtsergebnisse in derselben Aktivität beibehalten müssen, ist ein alternativer Ansatz möglich, der zu einer vorübergehenden Unterbrechung der Empfehlungsverfügbarkeit führen kann:

1. Duplizieren Sie die Aktivität und die Kriterien, die Sie ändern möchten.
1. Nehmen Sie Änderungen an der duplizierten Aktivität und den Kriterien vor und warten Sie, bis der Algorithmus Ergebnisse generiert.
1. Sehen Sie sich die neue, geänderte Aktivität in der Vorschau an und überprüfen Sie, ob die Ergebnisse Ihren Anforderungen entsprechen.
1. Halten Sie die vorhandene Aktivität an und tauschen Sie die Einstellungen/Kriterien auf die neuen Kriterien aus.
1. Überprüfen Sie die Vorschau der vorhandenen Aktivität und bestätigen Sie, dass die Ergebnisse Ihren Anforderungen entsprechen.
1. Aktivieren Sie die Aktivität erneut.
