---
keywords: Targeting; Erfolg; Konversionsmetrik; Metrik für Seitenbewertung; Metrik für Seitenansichten; Umsatzmetriken; Metrik für die Besuchszeit pro Site; geschätzter Wert; erweiterte Einstellungen; Erfolgsmetriken; erweiterte Einstellungen; Abhängigkeit; abhängig; Anzahl erhöhen und Benutzer in Aktivität belassen; Anzahl erhöhen, Benutzer freigeben und Wiedereintritt erlauben; Anzahl erhöhen, Benutzer freigeben und an Wiedereintritt hindern
description: Informationen zu Erfolgsmetriken in Adobe [!DNL Target] die Ihnen bei der Bestimmung des Erfolgs einer Aktivität helfen. Zu den Erfolgsmetriken gehören Konversion, Umsatz, Seitenansichten, benutzerspezifische Bewertung und Besuchszeit pro Site.
title: Was sind Erfolgsmetriken?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: b0bf54d47ac44afc3597f308ea38fd479c54026d
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 43%

---

# Erfolgsmetriken

In [!DNL Adobe Target] Erfolgsmetriken sind Parameter, mit denen der Erfolg einer Aktivität gemessen wird. Erfolgsmetriken umfassen wichtige Geschäftskennzahlen, mit denen Sie den Erfolg eines bestimmten Erlebnisses oder Angebots in einer [!DNL Target] Aktivität.

So können Sie beispielsweise feststellen, ob ein neues Angebot oder das Hinzufügen eines Artikel zu einem Warenkorb Ihren Umsatz pro Besucher steigert. Erfolgsmetriken können hilfreich sein, um Probleme mit der Registrierung, der Sortierung oder dem Kauftrichter oder einfach mit der Besucher- und Kundeninteraktion zu ermitteln.

## Überblick

In [!DNL Target], werden die Erfolgsmetriken mit den optimalen Optionen für Berichterstellungs- und Verfolgungszwecke vorkonfiguriert.

Standardmäßig sind Konversionsereignisse auf &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen].&quot; Konversionen werden nur einmal gezählt, keine wiederholten Konversionen gezählt und der Besucher sieht immer den Aktivitätsinhalt.

Umsatzmetriken, die auf &quot;[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]&quot; protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher getätigt wurde. Alle nachfolgenden Bestellungen erhöhen die Konversionsanzahl, führen jedoch nicht zu Umsatz zu RPV/AOV/Sales und werden nicht in die [!UICONTROL Bestelldetails] Bericht.

>[!NOTE]
>
>Für Aktivitäten, die [Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwendet die Zielmetrik immer die[!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen]&quot; und &quot;[!UICONTROL Bei jeder Impression]&quot;. Dies ist *not* konfigurierbar.

Es sind folgende Erfolgsmetriken verfügbar:

| Erfolgsmetrik | Messungsansatz | Definition |
|--- |--- |--- |
| Konversion | Konversionsbasiert | Die Konversion erfolgt, wenn ein Besucher eine von Ihnen definierte Aktion auf Ihrer Site ausführt, z. B. <ul><li>Klicken auf eine Schaltfläche</li><li>Seite angezeigt</li><li>Umfrage abgeschlossen</li><li>Kauf getätigt</li></ul>Eine Konversion kann einmal pro Besucher oder jedes Mal gezählt werden, wenn ein Besucher eine Konversion durchführt. |
| Umsatz | Konversionsbasiert | Durch den Besuch generierter Umsatz. Sie können aus folgenden Umsatzmetriken wählen:<ul><li>Umsatz pro Besucher (RPV)</li><li>Durchschnittlicher Bestellwert (AOV)</li><li>Gesamtverkäufe</li><li>Bestellungen</li></ul> |
| Seitenansichten | Interaktionsbasiert | Jeder eindeutige Besuch wird als Konversion gezählt. |
| Benutzerspezifisches Ergebnis | Interaktionsbasiert | Aggregierter Wert basierend auf dem Wert, der den auf der Site besuchten Seiten zugewiesen wird, ab dem Zeitpunkt, zu dem der Besucher die erste Anzeige der Aktivität anzeigt [!DNL Target] -Anfrage. |
| Besuchszeit pro Site | Interaktionsbasiert | Zeit, die während des Besuchs verbracht wurde (in Sekunden), ab dem Zeitpunkt, zu dem der Besucher die erste Anzeige der Aktivität sieht [!DNL Target] Anfrage zum Laden der letzten Seite mit einer Anfrage in der Sitzung. |

Bei interaktionsbasierten Metriken müssen sich Besucher (im Gegensatz zu konversions- oder umsatzbasierten Metriken) erneut für die Aktivität qualifizieren, um den Zähler für diese Sitzung zu erhöhen. Die zugehörige Metrik steigt nach erneuter Qualifikation und endet mit dem Ende der jeweiligen Besuchersitzung. Sitzungen enden nach einer Inaktivität von 30 Minuten. Daher werden die Ergebnisse nicht sofort während des Tests angezeigt. jedoch sind alle Ergebnisse dieser Sitzung innerhalb weniger Minuten nach dem Ende der Sitzung verfügbar.

## Benutzerdefinierte Erfolgsmetriken

Sie können auch benutzerdefinierte Erfolgsmetriken erstellen.

Wählen Sie nach Auswahl der Erfolgsmetrik die Aktion, die von einem Besucher unternommen wurde, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Konversion] Metrik, legen Sie fest, dass sie einmal pro Besucher gezählt wird, und legen Sie dann fest, ob ein Erfolg erzielt wird, wenn ein Besucher eine bestimmte Seite (oder mehrere Seiten) anzeigt oder eine bestimmte [!DNL Target] anfordern oder auf einen bestimmten Link klicken.

Wenn diese Option aktiviert ist, wird die [!UICONTROL Geschätzter Wert einer Konversion] -Feld (nicht verfügbar für [!UICONTROL Seitenergebnis] Metriken) einen Wert für Ihr Ziel bereitstellt, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Umsatz pro Besucher], [!UICONTROL Durchschnittlicher Bestellwert], [!UICONTROL Gesamtverkäufe]und [!UICONTROL Bestellungen]), verwendet die Schätzung [!UICONTROL Umsatz pro Besucher]. Der Datentyp ist eine Währung. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

Die für Ihre Aktivität gewählten Erfolgsmetriken sind in den Berichtseinstellungen verfügbar, wenn Sie einen Bericht für die Aktivität anzeigen.

Einige Metriken, z. B. [!UICONTROL Benutzerdefinierte Bewertung] und [!UICONTROL Umsatz pro Besucher], erfordern eine benutzerdefinierte Implementierung, die Informationen wie Bestellsummen und Bestell-IDs weitergibt.

## Erweiterte Einstellungen   {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Mit den erweiterten Einstellungen können Sie verwalten, wie Sie Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder sie entfernen soll und ob die Metrik einmal pro Teilnehmer oder bei jeder Impression gezählt werden soll.

So greifen Sie auf die [!UICONTROL Erweiterte Einstellungen] Optionen, klicken Sie auf die **[!UICONTROL vertikale Ellipsen]** > **[!UICONTROL Erweiterte Einstellungen]**.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die [!UICONTROL Erweiterte Einstellungen] nicht verfügbar. Weitere Informationen finden Sie unter [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Abhängigkeit hinzufügen

Sie können die erweiterten Einstellungen verwenden, um abhängige Erfolgsmetriken zu erstellen und nur dann eine Metrik zu inkrementieren, wenn ein Besucher zuerst eine andere Metrik erreicht.

![Abhängigkeit hinzufügen](/help/main/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

So kann eine Testkonversion zum Beispiel nur dann gültig sein, wenn ein Besucher das Angebot anklickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Die Abhängigkeitsfunktion ist *not* unterstützt für Folgendes:

* [!UICONTROL Recommendations]-Aktivitäten. Diese Funktionalität wird für alle anderen Aktivitätstypen unterstützt.
* Wenn Sie [Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Metriktyp &quot;Angezeigte Seite&quot;.
* Der Metriktyp &quot;Angeklickt ein Element&quot;für VEC-Aktivitäten (Visual Experience Composer).

Abhängige Erfolgsmetriken werden in folgenden Fällen nicht umgewandelt:

* Im Fall einer gegenseitigen Abhängigkeit, bei der Metrik1 von Metrik2 und Metrik2 von Metrik1 abhängt, kann keine der beiden Metriken umgewandelt werden.
* Bei Aktivitäten mit automatisierter Personalisierung werden Benutzer freigegeben und die Aktivität neu gestartet, wenn die Konversionsmetriken erreicht werden. Metriken, die von der Konversionsmetrik abhängen, werden somit nicht umgewandelt.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?

Verwenden Sie die erweiterten Einstellungen, um festzulegen, was geschehen soll, wenn ein Benutzer die Sollmetrik erreicht. In der folgenden Tabelle finden Sie die verfügbaren Optionen:

| Ein Benutzer findet diese Sollmetrik vor | Optionen |
|--- |--- |
| [!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen] | Angeben, wie die Anzahl erhöht wird:<ul><li>Einmal pro Teilnehmer  (Standard)</li><li>Bei jeder Anzeige, einschließlich Seitenaktualisierungen</li><li>Bei jeder Anzeige</li></ul> |
| [!UICONTROL Anzahl erhöhen, Benutzer freigeben und Wiedereintritt erlauben] | Auswahl des Erlebnisses, das der Besucher bei erneuter Teilnahme an der Aktivität sieht:<ul><li>Das gleiche Erlebnis  (Standard)</li><li>Ein zufällig ausgewähltes Erlebnis</li><li>Ein noch nicht gesehenes Erlebnis</li></ul> |
| [!UICONTROL Anzahl erhöhen, Benutzer freigeben und an Wiedereintritt hindern] | Festlegen, was der Benutzer anstelle des Aktivitätsinhalts sieht:<ul><li>Das gleiche Erlebnis, ohne Tracking  (Standard)</li><li>Den Standardinhalt oder den Inhalt einer anderen Aktivität</li></ul> |

>[!NOTE]
>
>Wenn Sie eine Metrik für eine der [!UICONTROL Anzahl erhöhen] -Optionen (siehe oben), wird die Metrikanzahl nur einmal pro Teilnehmer auf Besucherebene korrekt erhöht. Die Metrikanzahl wird für jede neue Sitzung auf Besuchsebene einmal pro Besuch erhöht.

### Wie wird die Anzahl erhöht:

Wählen Sie das gewünschte Verhalten aus:

* Einmal pro Teilnehmer 
* Bei jeder Impression (außer Seitenaktualisierungen)
* Bei jeder Anzeige

## Bekannte Probleme

* Erfolgsmetriken, für die die Einstellung der erweiterten Option „Wie wird die Zählung erhöht“ auf „Jede Impression“ oder „Jede Impression (ohne Aktualisierungen)“ gesetzt ist, können nicht als Erfolgsmetrik mit einer abhängigen Metrik verwendet werden.

Wenn eine Erfolgsmetrik bei jeder Impression auf inkrementiert wird, [!DNL Target] zählt den Besucher jedes Mal erneut, wenn der Besucher diese Erfolgsmetrik besucht. [!DNL Target] setzt dann die Erfolgsmetrik „Mitgliedschaft“ auf 0 zurück, sodass ab der nächsten Impression wieder neu gezählt wird. Wenn also für eine andere Metrik erforderlich ist, dass diese Metrik zuerst angezeigt wurde, [!DNL Target] erkennt nie, dass der Benutzer die erste Metrik gesehen hat.

## Schulungsvideo: Aktivitätsmetriken

Dieses Video zeigt, wie Sie die verschiedenen Aktivitätsmetriken verwenden.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktionen
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)
