---
keywords: Recommendations; Angebot; Vorschau; Launch; Status; Kriterien; Algorithmus
description: Erfahren Sie, wie Sie eine Vorschau Ihrer Adobe [!DNL Target] Recommendations-Aktivität anzeigen können, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten.
title: Wie kann ich eine Recommendations-Aktivität in der Vorschau anzeigen und starten?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 6e15b9b10e6a40c8efec06c45442b0f9894e648e
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 16%

---

# Vorschau und Starten Ihrer Recommendations-Aktivität

Nachdem Sie die Aktivität [!UICONTROL Recommendations], [!UICONTROL A/B Test] oder [!UICONTROL Experience Targeting] (XT) mit [Recommendations-Angeboten](/help/main/c-recommendations/recommendations-as-an-offer.md) erstellt haben, sollten Sie eine Vorschau Ihrer Empfehlungen anzeigen, um sicherzustellen, dass Ergebnisse verfügbar sind, bevor Sie die Aktivität starten. [!DNL Target Recommendations] bietet mehrere Möglichkeiten, eine Vorschau Ihrer Empfehlungen anzuzeigen.

## Überprüfen des Recommendations-Algorithmusstatus

Nach Erstellung einer Aktivität führt [!DNL Recommendations] einen Algorithmus aus, um Empfehlungen zu generieren. Die Ausführung dieses Algorithmus kann einige Stunden dauern.

Sie können im Übersichtsdiagramm [!UICONTROL Activity] überprüfen, ob die Ausführung des Algorithmus abgeschlossen ist. Hier wird der Kriterienstatus aufgelistet. Die folgende Abbildung zeigt den Status im Aktivitätsdiagramm auf der Seite [!UICONTROL Overview] einer [!DNL Recommendations] -Aktivität:

![Recommendations-Aktivitätsübersichtsseite](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Die folgende Abbildung zeigt den Status auf der Seite [!UICONTROL A/B Test] oder [!UICONTROL Overview] einer XT-Aktivität:

![Seite &quot;Überblick über A/B-Tests&quot;](/help/main/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

Zu den Statusergebnissen gehören die folgenden:

* [!UICONTROL Results Ready]: Gibt an, dass der Algorithmus Ergebnisse zurückgegeben hat
* [!UICONTROL Results Not Ready]: Gibt an, dass der Algorithmus noch nicht abgeschlossen ist.
* [!UICONTROL Feed Failure]: Gibt an, dass die benutzerdefinierte Kriterien-Feed-Datei nicht abgerufen werden konnte.

![Dialogfeld &quot;Ergebnisse&quot;](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Wie lange dauert die Ausführung des Algorithmus?

Nach dem Speichern einer Aktivität, die ein Kriterium enthält, berechnet [!DNL Target] Empfehlungen basierend auf der ausgewählten Sammlung, den Kriterien, dem Entwurf und den Promotions. Diese Berechnung benötigt etwas Zeit, um sie durchzuführen. Der Zeitrahmen unterscheidet sich je nach ausgewählter Empfehlungslogik, Datumsbereich, Anzahl der Elemente in Ihrem Katalog, Menge der Verhaltensdaten, die Ihre Kunden generiert haben, und ausgewählter Verhaltens-Datenquelle.

Die Verhaltensdatenquelle hat den größten Einfluss auf die Verarbeitungszeit, wie im Folgenden dargestellt wird:

### Mboxes

Wenn Mboxes als Verhaltensdatenquelle ausgewählt wird, werden die Kriterien nach der Erstellung sofort ausgeführt. Je nach Menge der verwendeten Verhaltensdaten und der Größe des Katalogs kann die Ausführung des Algorithmus bis zu 12 Stunden dauern. Änderungen an der Kriterienkonfiguration bewirken normalerweise eine Neuausführung des Algorithmus. Je nach vorgenommener Änderung stehen die zuvor berechneten Empfehlungen möglicherweise erst nach Abschluss einer erneuten Ausführung zur Verfügung oder bei größeren Änderungen sind nur Backup- oder Standardinhalte verfügbar, bis eine erneute Ausführung abgeschlossen ist. Wenn ein Algorithmus nicht geändert wird, wird er von [!DNL Target] je nach ausgewähltem Datumsbereich automatisch alle 12 bis 48 Stunden erneut ausgeführt.

### Adobe Analytics

Wenn das Kriterium [!DNL Adobe Analytics] als Verhaltens-Datenquelle verwendet, hängt der Zeitpunkt der Verfügbarkeit der Kriterien nach deren Erstellung davon ab, ob die ausgewählte Report Suite und das Lookback-Fenster bereits für andere Kriterien verwendet wurden.

* **Einmalige Einrichtung der Report Suite**: Wenn eine Report Suite zum ersten Mal mit einem Datumsbereich-Lookback-Fenster verwendet wird, kann es zwei bis sieben Tage dauern, bis [!DNL Target Recommendations] die Verhaltensdaten für die ausgewählte Report Suite von [!DNL Analytics] vollständig heruntergeladen hat. Dieser Zeitraum hängt von der [!DNL Analytics]-Systemlast ab.
* **Neue oder bearbeitete Kriterien mit einer bereits verfügbaren Report Suite**: Wenn Sie ein neues Kriterium erstellen oder ein vorhandenes Kriterium bearbeiten und die ausgewählte Report Suite bereits mit [!DNL Target Recommendations] verwendet wurde und der Datenbereich mindestens dem ausgewählten Datenbereich entspricht, sind die Daten sofort verfügbar und es ist keine einmalige Einrichtung erforderlich. In diesem Fall oder wenn die Einstellungen eines Algorithmus bearbeitet werden, ohne dass die ausgewählte Report Suite oder der ausgewählte Datumsbereich geändert wird, wird der Algorithmus innerhalb von 12 Stunden ausgeführt bzw. erneut ausgeführt.
* **Laufende Ausführung von Algorithmen**: Daten werden täglich von [!DNL Analytics] zu [!DNL Target Recommendations] übertragen. Beispiel: Wenn ein Benutzer ein Produkt anzeigt, wird für die [!UICONTROL Viewed Affinity] -Empfehlung ein Produktansichts-Tracking-Aufruf an [!DNL Analytics] fast in Echtzeit übergeben. Die [!DNL Analytics] -Daten werden am nächsten Tag zu Beginn an [!DNL Target] gesendet und [!DNL Target] führt den Algorithmus in weniger als 12 Stunden aus.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] erfordert keine Ausführung des Offline-Algorithmus und die Ergebnisse sind sofort verfügbar. [!UICONTROL Top Viewed] - und [!UICONTROL Top Sellers] -Algorithmen, die auf Mbox-Daten basieren, erzeugen aufgrund der einfacheren Berechnung im Allgemeinen sehr schnell Ergebnisse. Dies können gute Optionen sein, wenn Sie eine Entwurfsänderung in der Vorschau anzeigen oder überprüfen möchten, ob Verhaltensdaten korrekt erfasst werden.

## Verwenden von QA-Links zur Vorschau von Recommendations

Nachdem der Algorithmus Ergebnisse bereitgestellt hat, können Sie diese Ergebnisse mit der Funktion [QA-Link](/help/main/c-activities/c-activity-qa/activity-qa.md) von [!DNL Adobe Target] in der Vorschau anzeigen. QA-Links sind im Abschnitt [!UICONTROL Activity QA] der Aktivitätsübersichtsseite verfügbar:

![Link „Aktivitäts-QA“](/help/main/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standardmäßig fügt [!DNL Target] Sie automatisch zur gewünschten Zielgruppe für den QA-Link hinzu. Wenn diese Einstellung deaktiviert ist und Ihre Aktivität Targeting-Regeln hat, muss Ihr Benutzerprofil diese Targeting-Regeln erfüllen, damit das Erlebnis mit Empfehlungen angezeigt wird.

Über einen QA-Link können Sie eine Vorschau der Empfehlungen auf Ihrer Seite anzeigen:

![Vorgestellte Produkte](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Der QA-Modus von Target ist &quot;sticky&quot;und wird in einem Cookie gespeichert. Wenn Sie den QA-Modus nicht beenden, werden die QA-Ergebnisse auf der gesamten Site angezeigt. Um den QA-Modus zu beenden, verwenden Sie das [Lesezeichen](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* Im QA-Modus wirkt sich das Durchsuchen der Site nicht auf die [!UICONTROL Recently Viewed Items] oder [!UICONTROL Recently Purchased Items] Ihres Profils aus. Dieses Verhalten tritt beabsichtigt auf, um eine unbeabsichtigte Verschmutzung von Produktionsverhaltensdaten zu vermeiden. Um Ergebnisse aus einem [!UICONTROL Recently Viewed Items] - oder [!UICONTROL User-Based Recommendations] -Kriterium in der Vorschau anzuzeigen, durchsuchen Sie zunächst die Site außerhalb des QA-Modus und öffnen dann dieselbe Sitzung, um einen QA-Modus-Link zu öffnen.

## Verwenden des CSV-Downloads zur Vorschau von Empfehlungen

In einigen Fällen können Sie die empfohlenen spezifischen Elemente prüfen. Dies ist besonders hilfreich bei der Verwendung von Algorithmen wie [!UICONTROL People Who Viewed This, Viewed That], wo je nach dem Artikel, den der Benutzer gerade anzeigt, unterschiedliche Elemente empfohlen werden und Sie Tausende oder Millionen von verschiedenen Artikeln in Ihrem Katalog haben können.

Die Ergebnisse können erst heruntergeladen werden, wenn für mindestens einen Algorithmus in der Aktivität der Status &quot;[!UICONTROL Results Ready]&quot; angezeigt wird.

Um Ergebnisse für die Vorschau herunterzuladen, klicken Sie auf das Menüsymbol in der oberen rechten Ecke der Aktivitätsübersichtsseite und dann auf **[!UICONTROL Download data]**.

![Datenoption herunterladen](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

Eine CSV-Datei wird heruntergeladen. Öffnen Sie es, um die empfohlenen Elemente anzuzeigen:

![CSV-Datei mit empfohlenen Elementen](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Von links nach rechts ist eine Liste empfohlener Artikel, in diesem Fall am häufigsten angezeigt. Die Empfehlungen sind durch die Umgebung getrennt. In diesem Fall enthält nur die Produktionsumgebung Empfehlungen.

Wenn ein Sternchen (*) der erste Wert einer Zeile ist, zeigt es [Sicherungselemente](/help/main/c-recommendations/c-algorithms/backup-recs.md) an. Sicherungselemente werden angezeigt, wenn nicht alle Plätze in einem Entwurf durch die empfohlenen Elemente des Algorithmus (Kriterien) ausgefüllt werden können.

Für andere Algorithmustypen, die auf einem Schlüsselwert basieren, wie z. B. [!UICONTROL People Who Viewed This, Viewed That], werden die Schlüsselwerte (d. h. die &quot;Diese&quot;Elemente) in der Spalte ganz links aufgelistet und die empfohlenen Elemente (d. h. die &quot;Diese&quot;Elemente) werden von links nach rechts in den Spalten &quot;Empfehlung_X&quot;aufgelistet.

>[!NOTE]
>
>Für Aktivitäten, die einen [!UICONTROL User-Based Recommendations] -Algorithmus enthalten, sind keine Ergebnisse-Downloads verfügbar. Für Kriterien, die die Empfehlungslogik [!UICONTROL Recently-Viewed Items] verwenden, sind keine Ergebnisse-Downloads verfügbar.

## Aktivieren der Recommendations-Aktivität

Klicken Sie auf der Registerkarte [!UICONTROL Activity Overview] auf den Dropdown-Pfeil neben dem Status und wählen Sie dann **[!UICONTROL Activate]** aus.

![Option aktivieren](/help/main/c-recommendations/t-create-recs-activity/assets/activate.png)

Beachten Sie, dass der Status zu [!UICONTROL Activating] wird:

![Aktivieren](/help/main/c-recommendations/t-create-recs-activity/assets/activating.png)

Nach einigen Sekunden bis zu einigen Minuten wechselt der Status auf [!UICONTROL Live]:

![Live](/help/main/c-recommendations/t-create-recs-activity/assets/live.png)

Beachten Sie, dass Sie die Aktivität auch über dieselbe Dropdownliste deaktivieren oder archivieren können.

## Vermeiden von Unterbrechungen beim Ändern der Recommendations-Einstellungen

Eine Änderung von [!DNL Recommendations] -Sammlungen, -Kriterien, -Promotions oder -Designeinstellungen in einer Live-Aktivität kann dazu führen, dass die Algorithmusergebnisse ungültig werden und der Status eines Algorithmus sich auf [!UICONTROL Results Not Ready] ändert.

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
