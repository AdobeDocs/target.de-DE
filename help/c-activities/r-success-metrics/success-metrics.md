---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics
description: In Adobe Target sind Erfolgsmetriken sowohl für Berichte- als auch für Verfolgungszwecke vorkonfiguriert.
title: Erfolgsmetriken im Adobe Target
uuid: 24e9ae0f-099b-430b-b2bb-03b405f88929
translation-type: tm+mt
source-git-commit: c7664f9674234565a3657f453541095811fa5aa6
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 83%

---


# Erfolgsmetriken{#success-metrics}

In Adobe Target sind Erfolgsmetriken sowohl für Berichte- als auch für Verfolgungszwecke vorkonfiguriert.

Erfolgsmetriken sind Parameter, die zur Messung des Erfolgs einer Aktivität verwendet werden. Erfolgsmetriken umfassen die wichtigsten betrieblichen Messwerte, mit denen Sie den Erfolg eines bestimmten Erlebnisses oder Angebots in einer Target-Aktivität ermitteln können. So können Sie beispielsweise feststellen, ob ein neues Angebot oder das Hinzufügen eines Artikel zu einem Warenkorb Ihren Umsatz pro Besucher steigert. Erfolgsmetriken können hilfreich sein, um Probleme mit der Registrierung, der Sortierung oder dem Kauftrichter oder einfach mit der Besucher- und Kundeninteraktion zu ermitteln.

Im Zuge des Ziels von [!DNL Target Standard], die Testerstellung zu vereinfachen, übernimmt die Anwendung einige der Konfigurationen, die in [!DNL Target Classic] noch manuell durchgeführt werden mussten. Erfolgsmetriken werden beispielsweise mit den optimalen Optionen vorkonfiguriert.

By default, conversion events are set to &quot;Count once and keep the entrant in the activity&quot; in [!DNL Target Standard]. Konversionen werden nur einmal gezählt. Wiederholte Konversionen werden nicht gezählt, und dem Besucher wird immer der Testinhalt angezeigt.

Umsatzmetriken, die auf „Anzahl inkrementieren und Benutzer in der Aktivität beibehalten“ festgelegt sind, protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher aufgegeben wurde. Alle nachfolgenden Bestellungen erhöhen die Anzahl Konversionen, steigern den Umsatz von RPV/AOV/Vertrieb jedoch nicht und werden nicht in den Bestelldetailbericht aufgenommen.

>[!NOTE]
>
>Das Standardverhalten für Aktivitäten, die [Analytics als Berichte-Quelle](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, lautet &quot;Anzahl erhöhen und Benutzer in der Aktivität belassen&quot;mit &quot;Einmal pro Teilnehmer&quot;.

Es sind folgende Erfolgsmetriken verfügbar:

| Erfolgsmetrik | Messungsansatz | Definition |
|--- |--- |--- |
| Konversion | Konversionsbasiert | Eine Konversion liegt vor, wenn ein Besucher eine Aktion auf Ihrer Website ausführt, die Sie definiert haben (Klicken auf eine Schaltfläche, Anzeigen einer Seite, Teilnehmen an einer Umfrage oder Tätigen eines Kaufs). Eine Konversion kann entweder einmal pro Besucher oder jedes Mal, wenn ein Besucher eine Konversion durchführt, gezählt werden. |
| Umsatz | Konversionsbasiert | Durch den Besuch generierter Umsatz. Sie können aus folgenden Umsatzmetriken wählen:<ul><li>Umsatz pro Besucher (RPV)</li><li>Durchschnittlicher Bestellwert (AOV)</li><li>Gesamtverkäufe</li></ul> |
| Seitenansichten | Interaktionsbasiert | Jeder eindeutige Besuch wird als Konversion gezählt. |
| Besuchszeit pro Site | Interaktionsbasiert | Besuchszeit (in Sekunden) ab dem Zeitpunkt, zu dem der Besucher die erste Anfrage zur Anzeige des Targets der Aktivität bis zum Laden der letzten Seite mit einer Anforderung in der Sitzung anzeigt. |
| Benutzerspezifisches Ergebnis | Interaktionsbasiert | Aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the activity&#39;s first display [!DNL Target] request. |

Bei interaktionsbasierten Metriken müssen sich Besucher (im Gegensatz zu konversions- oder umsatzbasierten Metriken) erneut für die Aktivität qualifizieren, um den Zähler für diese Sitzung zu erhöhen. Die zugehörige Metrik steigt nach erneuter Qualifikation und endet mit dem Ende der jeweiligen Besuchersitzung. Sitzungen enden nach einer Inaktivität von 30 Minuten. Deshalb sind die Ergebnisse nicht direkt während des Tests verfügbar, sondern erst einige Minuten nach Ende der Sitzung.

Sie können auch benutzerdefinierte Erfolgsmetriken erstellen.

Wählen Sie nach Auswahl der Erfolgsmetrik die Aktion, die von einem Besucher unternommen wurde, um das Ziel zu erreichen. For example, choose a Conversion metric, set it to be counted once per visitor, then set whether success is achieved when a visitor views a certain page (or set of pages), views a specific [!DNL Target] request, or clicks a specific link.

Bei Aktivierung bietet der geschätzte Wert eines Konversionsfeldes (nicht verfügbar für Seitenwertungsmetriken) einen Wert für Ihr Ziel, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Die Schätzung verwendet für alle Umsatzmetriken (Umsatz pro Besucher, durchschnittlicher Bestellwert, Gesamtverkäufe und Bestellungen) die Metrik „Umsatz pro Besucher“. Der Datentyp ist eine Währung. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

Die für Ihre Aktivität gewählten Erfolgsmetriken sind in den Berichtseinstellungen verfügbar, wenn Sie einen Bericht für die Aktivität anzeigen.

Einige Metriken wie „Benutzerdefiniertes Ergebnis“ und „Umsatz pro Besucher“ erfordern eine benutzerdefinierte Implementierung, durch die Informationen wie Gesamtbestellungen und Bestell-IDs eingefügt werden.

## Erweiterte Einstellungen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Mit den erweiterten Einstellungen können Sie verwalten, wie Sie Erfolg messen. Die Optionen umfassen das Zählen der Metrik pro Anzeige oder einmal pro Besucher sowie die Wahl, ob Benutzer in der Aktivität bleiben können oder entfernt werden.

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option für erweiterte Einstellungen steht nicht zur Verfügung.

![Dropdown-Liste „Erweiterte Einstellungen“](/help/c-activities/r-success-metrics/assets/Menu_AdvancedSettings.png)

Darüber hinaus können Sie mithilfe der erweiterten Einstellungen abhängige Erfolgsmetriken erstellen, die immer nur dann als erreicht verbucht werden, wenn ein Besucher zuvor eine andere Metrik erfüllt hat.

![Abhängigkeit hinzufügen](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

So kann eine Testkonversion zum Beispiel nur dann gültig sein, wenn ein Besucher das Angebot anklickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Abhängige Erfolgsmetriken werden nur für Aktivitäten mit A/B-Test, automatisierter Personalisierung, Erlebnis-Targeting und Multivariate Tests unterstützt. Derzeit liegt keine Unterstützung für Empfehlungen vor.

>[!NOTE]
>
>Abhängige Erfolgsmetriken werden in folgenden Fällen nicht umgewandelt:

* Im Fall einer gegenseitigen Abhängigkeit, bei der Metrik1 von Metrik2 und Metrik2 von Metrik1 abhängt, kann keine der beiden Metriken umgewandelt werden.
* Bei Aktivitäten mit automatisierter Personalisierung werden Benutzer freigegeben und die Aktivität neu gestartet, wenn die Konversionsmetriken erreicht werden. Metriken, die von der Konversionsmetrik abhängen, werden somit nicht umgewandelt.

Verwenden Sie die erweiterten Einstellungen, um festzulegen, was geschehen soll, wenn ein Benutzer die Sollmetrik erreicht. In der folgenden Tabelle finden Sie die verfügbaren Optionen.

| Ein Benutzer findet diese Sollmetrik vor | Optionen |
|--- |--- |
| Anzahl erhöhen und Benutzer in der Aktivität belassen | Angeben, wie die Anzahl erhöht wird:<ul><li>Einmal pro Teilnehmer  (Standard)</li><li>Bei jeder Anzeige, einschließlich Seitenaktualisierungen</li><li>Bei jeder Anzeige</li></ul> |
| Anzahl erhöhen, Benutzer entlassen und erneute Teilnahme zulassen | Auswahl des Erlebnisses, das der Besucher bei erneuter Teilnahme an der Aktivität sieht:<ul><li>Das gleiche Erlebnis  (Standard)</li><li>Ein zufällig ausgewähltes Erlebnis</li><li>Ein noch nicht gesehenes Erlebnis</li></ul> |
| Anzahl erhöhen, Benutzer entlassen und den Benutzer für die erneute Teilnahme sperren | Festlegen, was der Benutzer anstelle des Aktivitätsinhalts sieht:<ul><li>Das gleiche Erlebnis, ohne Tracking  (Standard)</li><li>Den Standardinhalt oder den Inhalt einer anderen Aktivität</li></ul> |

## Schulungsvideo: Aktivitätsmetriken

Dieses Video zeigt, wie Sie die verschiedenen Aktivitätsmetriken verwenden.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380)