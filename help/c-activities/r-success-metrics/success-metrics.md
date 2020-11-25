---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics;advanced settings;dependency;dependant;Increment Count & Keep User in Activity;Increment Count, Release user, & Allow Reentry;increment Count, Release User, & Bar from Reentry
description: In Adobe Target sind Erfolgsmetriken Parameter, mit denen der Erfolg einer Aktivität gemessen wird. Erfolgsmetriken umfassen die wichtigsten betrieblichen Messwerte, mit denen Sie den Erfolg eines bestimmten Erlebnisses oder Angebots in einer Target-Aktivität ermitteln können.
title: Erfolgsmetriken in Adobe Target
feature: success metrics
translation-type: tm+mt
source-git-commit: a12eea60aa3e66cdb54ab284fa3f942be4d56178
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 48%

---


# Erfolgsmetriken

In [!DNL Adobe Target] success metrics are parameters used to measure the success of an activity. Success metrics include key business measures that enable you to determine the success of a given experience or offer in a [!DNL Target] activity.

So können Sie beispielsweise feststellen, ob ein neues Angebot oder das Hinzufügen eines Artikel zu einem Warenkorb Ihren Umsatz pro Besucher steigert. Erfolgsmetriken können hilfreich sein, um Probleme mit der Registrierung, der Sortierung oder dem Kauftrichter oder einfach mit der Besucher- und Kundeninteraktion zu ermitteln.

## Überblick

Erfolgsmetriken [!DNL Target]werden vorkonfiguriert und bieten optimale Optionen für Berichte- und Verfolgungszwecke.

Standardmäßig sind die Ereignis für die Konvertierung auf &quot;Anzahl[!UICONTROL erhöhen und Benutzer in Aktivität]belassen&quot;eingestellt. Konversionen werden nur einmal gezählt, keine wiederholten Konvertierungen gezählt und der Besucher sieht immer den Inhalt der Aktivität.

Revenue metrics that are set to &quot;[!UICONTROL Increment count &amp; keep user in activity]&quot; log order details only for the first order made by the same visitor. All subsequent orders increase conversion count, but will not add revenue to RPV/AOV/Sales, and will not be included in the [!UICONTROL Order Details] report.

>[!NOTE]
>
>Bei Aktivitäten, die [Analytics als Berichte-Quelle](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, verwendet die Zielmetrik immer die Einstellungen &quot;Anzahl[!UICONTROL erhöhen und Benutzer in Aktivität]halten&quot;und &quot;[!UICONTROL Bei jeder Impression]&quot;. Dies ist *nicht* konfigurierbar.

Es sind folgende Erfolgsmetriken verfügbar:

| Erfolgsmetrik | Messungsansatz | Definition |
|--- |--- |--- |
| Konversion | Konversionsbasiert | Die Umrechnung erfolgt, wenn ein Besucher eine von Ihnen definierte Aktion auf Ihrer Site ausführt, z. B. <ul><li>Klicken auf eine Schaltfläche</li><li>Seite angezeigt</li><li>Umfrage abgeschlossen</li><li>Einkauf vorgenommen</li></ul>Eine Konversion kann einmal pro Besucher oder jedes Mal, wenn ein Besucher eine Konversion abschließt, gezählt werden. |
| Umsatz | Konversionsbasiert | Durch den Besuch generierter Umsatz. Sie können aus folgenden Umsatzmetriken wählen:<ul><li>Umsatz pro Besucher (RPV)</li><li>Durchschnittlicher Bestellwert (AOV)</li><li>Gesamtverkäufe</li><li>Bestellungen</li></ul> |
| Seitenansichten | Interaktionsbasiert | Jeder eindeutige Besuch wird als Konversion gezählt. |
| Benutzerspezifisches Ergebnis | Interaktionsbasiert | Aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the activity&#39;s first display [!DNL Target] request. |
| Besuchszeit pro Site | Interaktionsbasiert | Time spent in the visit (in seconds) from the point the visitor sees the activity&#39;s first display [!DNL Target] request to the load of the final page with a request in the session. |

Bei interaktionsbasierten Metriken müssen sich Besucher (im Gegensatz zu konversions- oder umsatzbasierten Metriken) erneut für die Aktivität qualifizieren, um den Zähler für diese Sitzung zu erhöhen. Die zugehörige Metrik steigt nach erneuter Qualifikation und endet mit dem Ende der jeweiligen Besuchersitzung. Sitzungen enden nach einer Inaktivität von 30 Minuten. Daher werden die Ergebnisse beim Testen nicht sofort angezeigt. jedoch sind alle Ergebnisse dieser Sitzung innerhalb weniger Minuten nach dem Ende der Sitzung verfügbar.

## Benutzerspezifische Erfolgsmetriken

Sie können auch benutzerdefinierte Erfolgsmetriken erstellen.

Wählen Sie nach Auswahl der Erfolgsmetrik die Aktion, die von einem Besucher unternommen wurde, um das Ziel zu erreichen. For example, choose a [!UICONTROL Conversion] metric, set it to be counted once per visitor, then set whether success is achieved when a visitor views a certain page (or set of pages), views a specific [!DNL Target] request, or clicks a specific link.

If enabled, the [!UICONTROL Estimated Value of one conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal, but not for other metrics. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. For all revenue metrics ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], and [!UICONTROL Orders]), the estimate uses [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

Die für Ihre Aktivität gewählten Erfolgsmetriken sind in den Berichtseinstellungen verfügbar, wenn Sie einen Bericht für die Aktivität anzeigen.

Some metrics, such as [!UICONTROL Custom Scoring] and [!UICONTROL Revenue Per Visitor], require a customized implementation that passes in information such as order totals and order IDs.

## Erweiterte Einstellungen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Mit den erweiterten Einstellungen können Sie verwalten, wie Sie Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder entfernt werden soll und ob die Metrik einmal pro Teilnehmer oder bei jeder Impression gezählt werden soll.

Um die [!UICONTROL erweiterten Einstellungen] aufzurufen, klicken Sie auf die **[!UICONTROL vertikalen Auslassungspunkte]** > **[!UICONTROL Erweiterte Einstellungen]**.

![Menü „Erweiterte Einstellungen“](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. The [!UICONTROL Advanced Settings] option will not be available. For more information, see [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md).

### hinzufügen Abhängigkeit

Sie können die erweiterten Einstellungen verwenden, um abhängige Erfolgsmetriken zu erstellen, wobei eine Metrik nur inkrementiert wird, wenn ein Besucher zuerst eine andere Metrik erreicht.

![Abhängigkeit hinzufügen](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

So kann eine Testkonversion zum Beispiel nur dann gültig sein, wenn ein Besucher das Angebot anklickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Dependency functionality is *not* supported for the following:

* [!UICONTROL Recommendations-Aktivitäten. ] Diese Funktionalität wird für alle anderen Aktivitätstypen unterstützt.
* If you use [Analytics as your reporting source](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Metriktyp „Angezeigte Seite“.
* Metriktyp „Elementklick“ für Visual Experience Composer (VEC)-Aktivitäten.

Abhängige Erfolgsmetriken werden in folgenden Fällen nicht umgewandelt:

* Im Fall einer gegenseitigen Abhängigkeit, bei der Metrik1 von Metrik2 und Metrik2 von Metrik1 abhängt, kann keine der beiden Metriken umgewandelt werden.
* Bei Aktivitäten mit automatisierter Personalisierung werden Benutzer freigegeben und die Aktivität neu gestartet, wenn die Konversionsmetriken erreicht werden. Metriken, die von der Konversionsmetrik abhängen, werden somit nicht umgewandelt.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft?

Verwenden Sie die erweiterten Einstellungen, um festzulegen, was geschehen soll, wenn ein Benutzer die Sollmetrik erreicht. In der folgenden Tabelle finden Sie die verfügbaren Optionen:

| Ein Benutzer findet diese Sollmetrik vor | Optionen |
|--- |--- |
| [!UICONTROL Anzahl erhöhen und Benutzer in Aktivität belassen] | Angeben, wie die Anzahl erhöht wird:<ul><li>Einmal pro Teilnehmer  (Standard)</li><li>Bei jeder Anzeige, einschließlich Seitenaktualisierungen</li><li>Bei jeder Anzeige</li></ul> |
| [!UICONTROL Anzahl erhöhen, Benutzer freigeben und Wiedereintritt zulassen] | Auswahl des Erlebnisses, das der Besucher bei erneuter Teilnahme an der Aktivität sieht:<ul><li>Das gleiche Erlebnis  (Standard)</li><li>Ein zufällig ausgewähltes Erlebnis</li><li>Ein noch nicht gesehenes Erlebnis</li></ul> |
| [!UICONTROL Anzahl erhöhen, Benutzer freigeben und an Wiedereintritt hindern] | Festlegen, was der Benutzer anstelle des Aktivitätsinhalts sieht:<ul><li>Das gleiche Erlebnis, ohne Tracking  (Standard)</li><li>Den Standardinhalt oder den Inhalt einer anderen Aktivität</li></ul> |

>[!NOTE]
>
>Wenn Sie eine Metrik auf eine der Optionen für die [!UICONTROL Anzahl] erhöhen (siehe oben) konfigurieren, wird die Metrikanzahl nur einmal pro Teilnehmer auf der Ebene des Besuchers korrekt inkrementiert. Die Metrikanzahl wird für jede neue Sitzung auf Besuchsebene einmal pro Besuch erhöht.

### Wie wird die Anzahl erhöht:

Wählen Sie das gewünschte Verhalten aus:

* Einmal pro Teilnehmer 
* Bei jeder Impression (Seitenaktualisierungen ausschließen)
* Bei jeder Anzeige

## Schulungsvideo: Aktivitätsmetriken

Dieses Video zeigt, wie Sie die verschiedenen Aktivitätsmetriken verwenden.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)