---
description: In Target Standard sind die Erfolgsmetriken zu Berichts- und Verfolgungszwecken vorkonfiguriert.
keywords: Targeting;Erfolg;Konversionsmetrik;Metrik für Seitenwertung;Metrik für Seitenansichten;Umsatzmetriken;Metrik „Besuchszeit pro Site“;geschätzter Wert;erweiterte Einstellungen
seo-description: In Target Standard sind die Erfolgsmetriken zu Berichts- und Verfolgungszwecken vorkonfiguriert.
seo-title: Erfolgsmetriken
solution: Target
title: Erfolgsmetriken
uuid: 24e9ae0f-099b-430b-b2bb-03b405f88929
translation-type: tm+mt
source-git-commit: 2a400b05f3e5637465fe65a10285544793d67b47

---


# Erfolgsmetriken{#success-metrics}

In Target Standard sind die Erfolgsmetriken zu Berichts- und Verfolgungszwecken vorkonfiguriert.

Erfolgsmetriken sind Parameter, die zum Messen des Erfolgs einer Aktivität verwendet werden. Erfolgsmetriken beinhalten wichtige Geschäftsmaßnahmen, mit denen Sie den Erfolg eines bestimmten Erlebnisses oder Angebots in einer Target-Aktivität ermitteln können. Sie können beispielsweise bestimmen, ob ein neues Angebot Ihren Umsatz pro Besucher steigern oder einen Artikel zu einem Warenkorb hinzufügt. Erfolgsmetriken können hilfreich sein, um Probleme mit Registrierung, Sortierung oder Kauftrichter zu ermitteln, aber auch einfach mit Besucherbindung oder Kundenbindung.

Im Zuge des Ziels von [!DNL Target Standard], die Testerstellung zu vereinfachen, übernimmt die Anwendung einige der Konfigurationen, die in [!DNL Target Classic] noch manuell durchgeführt werden mussten. Erfolgsmetriken werden beispielsweise mit den optimalen Optionen vorkonfiguriert.

Standardmäßig sind Konversionsereignisse in [!DNL Target Standard] auf „einmal zählen und Teilnehmer in der Aktivität halten“ festgelegt. Konversionen werden nur einmal gezählt. Wiederholte Konversionen werden nicht gezählt, und dem Besucher wird immer der Testinhalt angezeigt.

Umsatzmetriken, die auf „Anzahl inkrementieren und Benutzer in der Aktivität beibehalten“ festgelegt sind, protokollieren Bestelldetails nur für die erste Bestellung, die von demselben Besucher aufgegeben wurde. Alle nachfolgenden Bestellungen erhöhen die Anzahl Konversionen, steigern den Umsatz von RPV/AOV/Vertrieb jedoch nicht und werden nicht in den Bestelldetailbericht aufgenommen.

Es sind folgende Erfolgsmetriken verfügbar:

| Erfolgsmetrik | Messungsansatz | Definition |
|--- |--- |--- |
| Konversion | Konversionsbasiert | Eine Konversion liegt vor, wenn ein Besucher eine Aktion auf Ihrer Website ausführt, die Sie definiert haben (Klicken auf eine Schaltfläche, Anzeigen einer Seite, Teilnehmen an einer Umfrage oder Tätigen eines Kaufs). Eine Konversion kann entweder einmal pro Besucher oder jedes Mal, wenn ein Besucher eine Konversion durchführt, gezählt werden. |
| Umsatz | Konversionsbasiert | Durch den Besuch generierter Umsatz. Sie können aus folgenden Umsatzmetriken wählen:<ul><li>Umsatz pro Besucher (RPV)</li><li>Durchschnittlicher Bestellwert (AOV)</li><li>Gesamtverkäufe</li></ul> |
| Seitenansichten | Interaktionsbasiert | Jeder eindeutige Besuch wird als Konversion gezählt. |
| Besuchszeit pro Site | Interaktionsbasiert | Die während des Besuchs verbrachte Zeit (in Sekunden) ab der Anzeige der ersten Anzeige-Mbox der Aktivität bis zum Laden der letzten Seite mit einer Mbox während der Sitzung. |
| Benutzerspezifisches Ergebnis | Interaktionsbasiert | Kumuliertes Ergebnis auf Grundlage des den auf der Site besuchten Seiten zugewiesenen Wertes ab dem Zeitpunkt, zu dem der Besucher die Anzeige-Mbox der Aktivität zum ersten Mal anzeigt. |

Bei interaktionsbasierten Metriken müssen sich Besucher (im Gegensatz zu konversions- oder umsatzbasierten Metriken) erneut für die Aktivität qualifizieren, um den Zähler für diese Sitzung zu erhöhen. Die zugehörige Metrik steigt nach erneuter Qualifikation und endet mit dem Ende der jeweiligen Besuchersitzung. Sitzungen enden nach einer Inaktivität von 30 Minuten. Deshalb sind die Ergebnisse nicht direkt während des Tests verfügbar, sondern erst einige Minuten nach Ende der Sitzung.

Sie können auch benutzerdefinierte Erfolgsmetriken erstellen.

Wählen Sie nach Auswahl der Erfolgsmetrik die Aktion, die von einem Besucher unternommen wurde, um das Ziel zu erreichen. Wählen Sie beispielsweise eine Konversionsmetrik und legen Sie sie so fest, dass sie einmal pro Besucher gezählt wird. Legen Sie dann fest, ob Erfolg erzielt wird, wenn ein Besucher eine bestimmte Seite (oder eine Reihe von Seiten) anzeigt, eine bestimmte Mbox anzeigt oder auf einen bestimmten Link klickt.

Bei Aktivierung bietet der geschätzte Wert eines Konversionsfeldes (nicht verfügbar für Seitenwertungsmetriken) einen Wert für Ihr Ziel, jedoch nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Die Schätzung verwendet für alle Umsatzmetriken (Umsatz pro Besucher, durchschnittlicher Bestellwert, Gesamtverkäufe und Bestellungen) die Metrik „Umsatz pro Besucher“. Der Datentyp ist eine Währung. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](../../administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE).

Die für Ihre Aktivität gewählten Erfolgsmetriken sind in den Berichtseinstellungen verfügbar, wenn Sie einen Bericht für die Aktivität anzeigen.

Einige Metriken wie „Benutzerdefiniertes Ergebnis“ und „Umsatz pro Besucher“ erfordern eine benutzerdefinierte Implementierung, durch die Informationen wie Gesamtbestellungen und Bestell-IDs eingefügt werden.

## Erweiterte Einstellungen {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Mit den erweiterten Einstellungen können Sie verwalten, wie Sie Erfolg messen. Die Optionen umfassen das Zählen der Metrik pro Anzeige oder einmal pro Besucher sowie die Wahl, ob Benutzer in der Aktivität bleiben können oder entfernt werden.

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option für erweiterte Einstellungen steht nicht zur Verfügung.

![Dropdown-Liste Erweiterte Einstellungen](/help/c-activities/r-success-metrics/assets/Menu_AdvancedSettings.png)

Darüber hinaus können Sie abhängige Erfolgsmetriken über die erweiterten Einstellungen erstellen, die immer nur dann als erreicht verbucht werden, wenn ein Besucher zuvor eine andere Metrik erfüllt hat.

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
| Anzahl erhöhen und Benutzer in der Aktivität belassen | Angeben, wie die Anzahl erhöht wird:<ul><li>Einmal pro Teilnehmer (Standard)</li><li>Bei jeder Anzeige, einschließlich Seitenaktualisierungen</li><li>Bei jeder Anzeige</li></ul> |
| Anzahl erhöhen, Benutzer entlassen und erneute Teilnahme zulassen | Auswahl des Erlebnisses, das der Besucher bei erneuter Teilnahme an der Aktivität sieht:<ul><li>Das gleiche Erlebnis (Standard)</li><li>Ein zufällig ausgewähltes Erlebnis</li><li>Ein noch nicht gesehenes Erlebnis</li></ul> |
| Anzahl erhöhen, Benutzer entlassen und den Benutzer für die erneute Teilnahme sperren | Festlegen, was der Benutzer anstelle des Aktivitätsinhalts sieht:<ul><li>Das gleiche Erlebnis, ohne Tracking (Standard)</li><li>Den Standardinhalt oder den Inhalt einer anderen Aktivität</li></ul> |

## Schulungsvideo: Aktivitätsmetriken

Dieses Video zeigt, wie Sie die verschiedenen Aktivitätsmetriken verwenden.

* Erläuterung von „Zielmetriken“
* Verstehen und Erstellen von Metriken für Konversionen, Umsatz und Interaktion
* Erstellen einer Metrik mit Klick-Tracking

>[!VIDEO](https://video.tv.adobe.com/v/17380?captions=ger)