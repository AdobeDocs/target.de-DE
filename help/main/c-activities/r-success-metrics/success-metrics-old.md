---
keywords: Targeting;Erfolg;Konversionsmetrik;Seitenbewertungsmetrik;Seitenansichtsmetrik;Umsatzmetriken;Zeit vor Ort-Metrik;geschätzter Wert;erweiterte Einstellungen;Erfolgsmetriken;erweiterte Einstellungen;Abhängigkeit;Abhängig;Anzahl inkrementieren und Benutzer in Aktivität halten;Anzahl inkrementieren, Benutzer freigeben und erneuten Eintritt erlauben;Anzahl inkrementieren, Benutzer freigeben und Erneuten Eintritt sperren
description: Erfahren Sie mehr über Erfolgsmetriken in Adobe [!DNL Target]  mit denen Sie den Erfolg einer Aktivität ermitteln können. Zu den Erfolgsmetriken gehören Konversionen, Umsatz, Seitenansichten, benutzerdefinierte Punktzahl und Zeit vor Ort.
title: Was sind Erfolgsmetriken?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 42%

---

# Erfolgsmetriken

In [!DNL Adobe Target] werden Erfolgsmetriken als Parameter verwendet, um den Erfolg einer Aktivität zu messen. Erfolgsmetriken umfassen wichtige geschäftliche Messwerte, mit denen Sie den Erfolg eines bestimmten Erlebnisses oder Angebots in einer [!DNL Target] Aktivität ermitteln können.

So können Sie beispielsweise feststellen, ob ein neues Angebot oder das Hinzufügen eines Artikel zu einem Warenkorb Ihren Umsatz pro Besucher steigert. Erfolgsmetriken können hilfreich sein, um Probleme mit der Registrierung, der Sortierung oder dem Kauftrichter oder einfach mit der Besucher- und Kundeninteraktion zu ermitteln.

## Überblick

[!DNL Target] sind Erfolgsmetriken mit den optimalen Optionen für Reporting- und Tracking-Zwecke vorkonfiguriert.

Standardmäßig sind Konversionsereignisse auf &quot;[!UICONTROL Increment count & keep user in activity]&quot; festgelegt. Konversionen werden nur einmal gezählt, es werden keine wiederholten Konversionen gezählt und der Besucher sieht immer den Aktivitätsinhalt.

Umsatzmetriken, die auf &quot;[!UICONTROL Increment count & keep user in activity]&quot; eingestellt sind, protokollieren Auftragsdetails nur für die erste Bestellung, die von demselben Besucher getätigt wurde. Alle nachfolgenden Bestellungen erhöhen die Konversionsanzahl, erhöhen jedoch nicht den Umsatz in RPV/AOV/Sales und werden nicht in den [!UICONTROL Order Details] Bericht aufgenommen.

>[!NOTE]
>
>Bei Aktivitäten, [&#x200B; „Analytics“ als Berichtsquelle &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, verwendet die Zielmetrik immer die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; und &quot;[!UICONTROL On Every Impression]&quot;. Dies *nicht*.

Es sind folgende Erfolgsmetriken verfügbar:

| Erfolgsmetrik | Messungsansatz | Definition |
|--- |--- |--- |
| Konversion | Konversionsbasiert | Eine Konversion liegt vor, wenn ein Besucher eine von Ihnen definierte Aktion auf Ihrer Site ausführt, z. B. <ul><li>Auf eine Schaltfläche geklickt</li><li>Seite angezeigt</li><li>Abgeschlossene Umfrage</li><li>hat einen Kauf getätigt</li></ul>Eine Konversion kann einmal pro Besucher oder jedes Mal gezählt werden, wenn ein Besucher eine Konversion abschließt. |
| Umsatz | Konversionsbasiert | Durch den Besuch generierter Umsatz. Sie können aus folgenden Umsatzmetriken wählen:<ul><li>Umsatz pro Besucher (RPV)</li><li>Durchschnittlicher Bestellwert (AOV)</li><li>Gesamtverkäufe</li><li>Bestellungen</li></ul> |
| Seitenansichten | Interaktionsbasiert | Jeder eindeutige Besuch wird als Konversion gezählt. |
| Benutzerspezifisches Ergebnis | Interaktionsbasiert | Aggregierter Wert, der auf dem Wert basiert, der den auf der Website besuchten Seiten zugewiesen wurde, und zwar ab dem Punkt, an dem der Besucher die erste Anzeige [!DNL Target] Anfrage der Aktivität zum ersten Mal sieht. |
| Besuchszeit pro Site | Interaktionsbasiert | Besuchszeit (in Sekunden) ab dem Zeitpunkt, an dem der Besucher die erste Anzeige der Aktivität [!DNL Target] die Anforderung zum Laden der endgültigen Seite mit einer Anforderung in der Sitzung sieht. |

Bei interaktionsbasierten Metriken müssen sich Besucher (im Gegensatz zu konversions- oder umsatzbasierten Metriken) erneut für die Aktivität qualifizieren, um den Zähler für diese Sitzung zu erhöhen. Die zugehörige Metrik steigt nach erneuter Qualifikation und endet mit dem Ende der jeweiligen Besuchersitzung. Sitzungen enden nach einer Inaktivität von 30 Minuten. Daher werden die Ergebnisse beim Testen nicht sofort angezeigt. Alle Ergebnisse dieser Sitzung sind jedoch innerhalb weniger Minuten nach dem Ende der Sitzung verfügbar.

## Benutzerdefinierte Erfolgsmetriken

Sie können auch benutzerdefinierte Erfolgsmetriken erstellen.

Wählen Sie nach Auswahl der Erfolgsmetrik die Aktion, die von einem Besucher unternommen wurde, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Conversion] Metrik aus, legen Sie sie so fest, dass sie einmal pro Besucher gezählt wird, und legen Sie dann fest, ob der Erfolg erzielt wird, wenn ein Besucher eine bestimmte Seite (oder eine Reihe von Seiten) aufruft, eine bestimmte [!DNL Target] aufruft oder auf einen bestimmten Link klickt.

Wenn diese Option aktiviert ist, liefert das Feld [!UICONTROL Estimated Value of one conversion] (für die [!UICONTROL Page Score] Metriken nicht verfügbar) einen Wert für Ihr Ziel, aber nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] und [!UICONTROL Orders]) nutzt die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

Die für Ihre Aktivität gewählten Erfolgsmetriken sind in den Berichtseinstellungen verfügbar, wenn Sie einen Bericht für die Aktivität anzeigen.

Einige Metriken, z. B. [!UICONTROL Custom Scoring] und [!UICONTROL Revenue Per Visitor], erfordern eine benutzerdefinierte Implementierung, die Informationen wie Bestellsummen und Auftrags-IDs weitergibt.

## Erweiterte Einstellungen   {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Mit den erweiterten Einstellungen können Sie verwalten, wie Sie Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder entfernt werden soll, und die Auswahl, ob die Metrik einmal pro Eintritt oder bei jeder Impression gezählt werden soll.

Um auf die [!UICONTROL Advanced Settings] Optionen zuzugreifen, klicken Sie auf **[!UICONTROL vertical ellipses]** > **[!UICONTROL Advanced Settings]**.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option [!UICONTROL Advanced Settings] ist nicht verfügbar. Weitere Informationen finden Sie unter [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Abhängigkeit hinzufügen

Sie können die erweiterten Einstellungen verwenden, um abhängige Erfolgsmetriken zu erstellen, wobei eine Metrik nur inkrementiert wird, wenn ein Besucher zuerst eine andere Metrik erreicht.

![Abhängigkeit hinzufügen](/help/main/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

So kann eine Testkonversion zum Beispiel nur dann gültig sein, wenn ein Besucher das Angebot anklickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Die Abhängigkeitsfunktion wird *nicht* für Folgendes unterstützt:

* [!UICONTROL Recommendations]. Diese Funktionalität wird für alle anderen Aktivitätstypen unterstützt.
* Wenn Sie [Analytics als Berichtsquelle verwenden](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Metriktyp „Angezeigte Seite“.
* Metriktyp „Elementklick“ für Visual Experience Composer (VEC)-Aktivitäten.

Abhängige Erfolgsmetriken werden in folgenden Fällen nicht umgewandelt:

* Im Fall einer gegenseitigen Abhängigkeit, bei der Metrik1 von Metrik2 und Metrik2 von Metrik1 abhängt, kann keine der beiden Metriken umgewandelt werden.
* Bei Aktivitäten mit automatisierter Personalisierung werden Benutzer freigegeben und die Aktivität neu gestartet, wenn die Konversionsmetriken erreicht werden. Metriken, die von der Konversionsmetrik abhängen, werden somit nicht umgewandelt.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?

Verwenden Sie die erweiterten Einstellungen, um festzulegen, was geschehen soll, wenn ein Benutzer die Sollmetrik erreicht. In der folgenden Tabelle sind die verfügbaren Optionen aufgeführt:

| Ein Benutzer findet diese Sollmetrik vor | Optionen |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Angeben, wie die Anzahl erhöht wird:<ul><li>Einmal pro Teilnehmer (Standard)</li><li>Bei jeder Anzeige, einschließlich Seitenaktualisierungen</li><li>Bei jeder Anzeige</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Auswahl des Erlebnisses, das der Besucher bei erneuter Teilnahme an der Aktivität sieht:<ul><li>Gleiches Erlebnis (Standard)</li><li>Ein zufällig ausgewähltes Erlebnis</li><li>Ein noch nicht gesehenes Erlebnis</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | Festlegen, was der Benutzer anstelle des Aktivitätsinhalts sieht:<ul><li>Gleiches Erlebnis, ohne Tracking (Standard)</li><li>Den Standardinhalt oder den Inhalt einer anderen Aktivität</li></ul> |

>[!NOTE]
>
>Wenn Sie eine Metrik für eine der [!UICONTROL Increment Count] Optionen (oben erwähnt) konfigurieren, wird die Metrikanzahl nur auf Besucherebene einmal pro Teilnehmer korrekt erhöht. Die Metrikanzahl erhöht sich einmal pro Besuch für jede neue Sitzung auf Besuchsebene.

### Wie wird die Anzahl erhöht:

Wählen Sie das gewünschte Verhalten aus:

* Einmal pro Teilnehmer 
* Bei jeder Impression (ohne Seitenaktualisierungen)
* Bei jeder Anzeige

## Bekannte Probleme

* Erfolgsmetriken, für die die Einstellung der erweiterten Option „Wie wird die Zählung erhöht“ auf „Jede Impression“ oder „Jede Impression (ohne Aktualisierungen)“ gesetzt ist, können nicht als Erfolgsmetrik mit einer abhängigen Metrik verwendet werden.

Wenn eine Erfolgsmetrik so eingestellt ist, dass sie bei jeder Impression erhöht wird, zählt [!DNL Target] den Besucher jedes Mal neu, wenn er diese Erfolgsmetrik besucht. [!DNL Target] setzt dann die Erfolgsmetrik „Mitgliedschaft“ auf 0 zurück, damit sie wieder auf die nächste Impression zählen kann. Wenn also eine andere Metrik verlangt, dass diese Metrik zuerst gesehen werden muss, erkennt [!DNL Target] nie, dass der Benutzer die erste Metrik gesehen hat.

## Schulungsvideo: Aktivitätsmetriken

Dieses Video zeigt, wie Sie die verschiedenen Aktivitätsmetriken verwenden.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
