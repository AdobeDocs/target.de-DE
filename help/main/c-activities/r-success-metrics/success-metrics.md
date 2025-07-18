---
keywords: Targeting;Erfolg;Konversionsmetrik;Seitenbewertungsmetrik;Seitenansichtsmetrik;Umsatzmetriken;Zeit vor Ort-Metrik;geschätzter Wert;erweiterte Einstellungen;Erfolgsmetriken;erweiterte Einstellungen;Abhängigkeit;Abhängig;Anzahl inkrementieren und Benutzer in Aktivität halten;Anzahl inkrementieren, Benutzer freigeben und erneuten Eintritt erlauben;Anzahl inkrementieren, Benutzer freigeben und Erneuten Eintritt sperren
description: Erfahren Sie mehr über Erfolgsmetriken, mit denen Sie den Erfolg einer Aktivität ermitteln können. Zu den Erfolgsmetriken gehören Konversionen, Umsatz, Seitenansichten, benutzerdefinierte Punktzahl und Zeit vor Ort.
title: Was sind Erfolgsmetriken?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: a34d40bef584bfa941731df718cb402c658f5d28
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 22%

---

# [!UICONTROL Success metrics]

Erfolgsmetriken in [!DNL Adobe Target] sind wichtige Indikatoren, mit denen Sie die Leistung Ihrer -Aktivitäten messen können. Diese Metriken erfassen wichtige Geschäftsergebnisse wie Konversionen, Umsatz pro Besucher und Kundeninteraktion, sodass Sie die Auswirkungen bestimmter Erlebnisse oder Angebote bewerten können.

Sie können beispielsweise verfolgen, ob eine neue Promotion den Umsatz pro Besucher steigert oder zu mehr Artikeln führt, die zum Warenkorb hinzugefügt werden. Erfolgsmetriken helfen auch dabei, Probleme in Benutzerflüssen wie Registrierungs-, Checkout- oder Kaufprozessen zu identifizieren und liefern gleichzeitig Einblicke in das gesamte Besucherverhalten.

## Überblick

[!DNL Target] sind Erfolgsmetriken mit empfohlenen Einstellungen vorkonfiguriert, um eine genaue Berichterstellung und ein effektives Tracking sicherzustellen.

Standardmäßig verwenden Konversionsereignisse die -**[!UICONTROL Increment count & keep user in activity].** Mit dieser Einstellung wird jeder Besucher nur einmal als Konversion gezählt. Es werden keine wiederholten Konversionen gezählt. Diese Besucher sehen während ihrer gesamten Sitzung weiterhin den Aktivitätsinhalt.

Bei Umsatzmetriken, die dieselbe Einstellung verwenden, protokolliert nur die erste Bestellung eines Besuchers Bestelldetails. Nachfolgende Bestellungen erhöhen zwar die Konversionsanzahl, tragen aber nicht zu umsatzbasierten Metriken wie [!UICONTROL Revenue per Visitor (RPV)], [!UICONTROL Average Order Value (AOV)] oder [!DNL Total Sales] bei. Diese zusätzlichen Bestellungen sind auch aus dem [!UICONTROL Order Details] ausgeschlossen.

>[!NOTE]
>
>Bei Aktivitäten, die [Analytics als Berichtsquelle](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) verwenden, verwendet die Zielmetrik immer die Einstellungen &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; und &quot;[!UICONTROL On Every Impression]&quot;. Diese Einstellungen *nicht*.

Die folgenden Erfolgsmetriken können im Abschnitt [!UICONTROL Reporting Settings] der [!UICONTROL Activity Settings page] unter dem [!UICONTROL Goals & Settings] Schritt konfiguriert werden:

| Erfolgsmetrik | Messungsansatz | Definition |
|--- |--- |--- |
| [!UICONTROL Conversion] | Konversionsbasiert | Eine Konversion liegt vor, wenn ein Besucher eine von Ihnen definierte Aktion auf Ihrer Site ausführt, z. B. <ul><li>Seite angezeigt</li><li>Mbox angezeigt</li><li>Klicks auf ein Element</li></ul>Eine Konversion kann einmal pro Besucher oder jedes Mal gezählt werden, wenn ein Besucher eine Konversion abschließt. |
| [!UICONTROL Revenue] | Konversionsbasiert | Durch den Besuch generierter Umsatz. Sie können nur eine Umsatzmetrik auswählen:<ul><li>Mbox angezeigt</li></ul>Weitere Informationen zu den Änderungen an der aktualisierten [!DNL Target]-Benutzeroberfläche in Bezug auf die Erfolgsmetriken Umsatz finden Sie [Aktualisiert [!DNL Target] UI-Änderungen](#changes) unten. |
| [!UICONTROL Engagement] | Interaktionsbasiert | Interaktion, die durch den Besuch generiert wurde. Sie können aus den folgenden Interaktionsmetriken auswählen:<UL><li>Seitenansichten: Jeder einzelne Besuch wird als Konversion gezählt.</li><li>[!UICONTROL Custom Scoring]: Aggregierte Punktzahl basierend auf dem Wert, der den auf der Website besuchten Seiten zugewiesen wurde, und zwar ab dem Punkt, an dem der Besucher die erste Anzeige [!DNL Target] Anfrage der Aktivität zum ersten Mal sieht.</li>[!DNL Time on Site]: Besuchszeit (in Sekunden) ab dem Punkt, an dem der Besucher die erste Anzeige der Aktivität [!DNL Target] die Anforderung zum Laden der endgültigen Seite mit einer Anforderung in der Sitzung sieht.</UL> |

Bei interaktionsbasierten Metriken (im Gegensatz zu konversionsbasierten und umsatzbasierten Metriken) müssen sich Besucher bei jedem Besuch erneut für die Aktivität qualifizieren, um die Anzahl für diese Sitzung zu erhöhen. Die zugehörige Metrik steigt nach erneuter Qualifikation und endet mit dem Ende der jeweiligen Besuchersitzung. Sitzungen enden nach einer Inaktivität von 30 Minuten. Daher werden die Ergebnisse beim Testen nicht sofort angezeigt. Alle Ergebnisse dieser Sitzung sind jedoch innerhalb weniger Minuten nach dem Ende der Sitzung verfügbar.

## Benutzerdefinierte Erfolgsmetriken

Sie können auch benutzerdefinierte Erfolgsmetriken erstellen.

Wählen Sie nach Auswahl der Erfolgsmetrik die Aktion, die von einem Besucher unternommen wurde, um das Ziel zu erreichen. Wählen Sie beispielsweise eine [!UICONTROL Conversion] Metrik aus, legen Sie sie so fest, dass sie einmal pro Besucher gezählt wird, und legen Sie dann fest, ob der Erfolg erzielt wird, wenn ein Besucher eine bestimmte Seite (oder eine Reihe von Seiten) aufruft, eine bestimmte [!DNL Target] aufruft oder auf einen bestimmten Link klickt.

Wenn diese Option aktiviert ist, liefert das Feld [!UICONTROL Estimated Value of one conversion] (für die [!UICONTROL Page Score] Metriken nicht verfügbar) einen Wert für Ihr Ziel, aber nicht für andere Metriken. Mit diesem Wert kann [!DNL Target] die geschätzte Umsatzsteigerung berechnen. Dieses Feld ist optional, ohne Eintrag kann jedoch kein Umsatzwachstum für eine nicht umsatzbezogene Metrik berechnet werden. Für alle Umsatzmetriken ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] und [!UICONTROL Orders]) nutzt die Schätzung [!UICONTROL Revenue per Visitor]. Der Datentyp ist eine Währung. Weitere Informationen finden Sie unter [Schätzen der Umsatzsteigerung](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

Die Erfolgsmetriken, die Sie für Ihre Aktivität auswählen, sind in den Berichtseinstellungen verfügbar, wenn Sie einen Bericht für die Aktivität anzeigen.

Einige Metriken, z. B. [!UICONTROL Custom Scoring] und [!UICONTROL Revenue Per Visitor], erfordern eine benutzerdefinierte Implementierung, die Informationen wie Bestellsummen und Auftrags-IDs weitergibt.

## Erweiterte Einstellungen   {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Mit den erweiterten Einstellungen können Sie verwalten, wie Sie Erfolg messen. Zu den Optionen gehören das Hinzufügen von Abhängigkeiten, die Auswahl, ob der Benutzer in der Aktivität bleiben oder entfernt werden soll, und die Auswahl, ob die Metrik einmal pro Eintritt oder bei jeder Impression gezählt werden soll.

Um auf die [!UICONTROL Advanced Settings] Optionen zuzugreifen, klicken Sie auf das **[!UICONTROL More Actions]** ( ![Symbol Mehr Aktionen](/help/main/assets/icons/MoreSmallListVert.svg) ) und dann auf **[!UICONTROL Advanced Settings]**.

![Menü „Erweiterte Einstellungen“](/help/main/c-activities/r-success-metrics/assets/advanced-settings-refresh.png)

Weitere Informationen zu den [!UICONTROL Advanced Settings] Optionen (“[!UICONTROL What will happen after a user encounters this goal]&quot; und &quot;[!UICONTROL How will the count be incremented]„) finden Sie unter [Was passiert, nachdem ein Benutzer auf diese Zielmetrik trifft](#what-happens)?

>[!NOTE]
>
>Wenn Sie [!DNL Adobe Analytics] als Ihre Berichterstellungsquelle verwenden, werden die Einstellungen vom [!DNL Analytics]-Server verwaltet. Die Option [!UICONTROL Advanced Settings] ist nicht verfügbar. Weitere Informationen finden Sie unter [Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Abhängigkeit hinzufügen

Sie können die erweiterten Einstellungen verwenden, um abhängige Erfolgsmetriken zu erstellen, wobei eine Metrik nur inkrementiert wird, wenn ein Besucher zuerst eine andere Metrik erreicht.

So kann eine Testkonversion zum Beispiel nur dann gültig sein, wenn ein Besucher das Angebot anklickt oder auf eine bestimmte Seite gelangt, bevor die Konversion erfolgt.

Die Abhängigkeitsfunktion wird *nicht* für Folgendes unterstützt:

* [!UICONTROL Recommendations]. Diese Funktionalität wird für alle anderen Aktivitätstypen unterstützt.
* Wenn Sie [Analytics als Berichtsquelle verwenden](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Metriktyp „Angezeigte Seite“.
* Metriktyp „Elementklick“ für Visual Experience Composer (VEC)-Aktivitäten.

Abhängige Erfolgsmetriken werden in den folgenden Fällen nicht konvertiert:

* Im Fall einer gegenseitigen Abhängigkeit, bei der Metrik1 von Metrik2 und Metrik2 von Metrik1 abhängt, kann keine der beiden Metriken umgewandelt werden.
* [!UICONTROL Automated Personalization]-Aktivitäten geben Benutzer frei und starten die Aktivität neu, wenn die Konversionsmetriken erreicht sind, sodass keine von der Konversionsmetrik abhängigen Metriken konvertiert werden.

### Was passiert, wenn ein Benutzer auf diese Zielmetrik trifft? {#what-happens}

Verwenden Sie die erweiterten Einstellungen, um festzulegen, was geschehen soll, wenn ein Benutzer die Sollmetrik erreicht. In der folgenden Tabelle sind die verfügbaren Optionen aufgeführt:

| Ein Benutzer findet diese Sollmetrik vor | Optionen |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Angeben, wie die Anzahl erhöht wird:<ul><li>Einmal pro Teilnehmer (Standard)</li><li>Bei jeder Anzeige, einschließlich Seitenaktualisierungen</li><li>Bei jeder Anzeige</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Wählen Sie das Erlebnis aus, das der Besucher sieht, wenn er erneut die Aktivität aufruft:<ul><li>Gleiches Erlebnis (Standard)</li><li>Ein zufällig ausgewähltes Erlebnis</li><li>Ein noch nicht gesehenes Erlebnis</li></ul> |
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

## [!DNL Target] Änderungen an der Benutzeroberfläche aktualisiert {#changes}

Mit der [[!DNL Target Standard/Premium] 25.2.1](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2) die am 17. Februar 2015 veröffentlicht wurde, wurden aktualisierte [!DNL Target]- und [!UICONTROL Visual Experience Composer] (VEC)-Benutzeroberflächen eingeführt. In diesem Abschnitt werden die wichtigsten Unterschiede zwischen der veralteten und der aktualisierten Benutzeroberfläche beschrieben, insbesondere im Hinblick auf die Konfiguration und Verwaltung von Erfolgsmetriken.

### Änderungen an der Benutzeroberfläche im Zusammenhang mit [!UICONTROL Revenue] Erfolgsmetriken

In der aktualisierten [!DNL Target] wurde die Dropdown-Liste [!UICONTROL Default View for Reporting] entfernt. Dieses Feld war redundant, da es zuvor die standardmäßige Berichtsansicht unter [!DNL Overview] > [!UICONTROL Reports] in der Legacy-Benutzeroberfläche gespeichert hat.

Mit der aktualisierten Benutzeroberfläche ist die standardmäßige Berichtsmetrik jetzt immer auf [!UICONTROL Revenue per Visitor (RPV)] festgelegt. Sie können die Ansicht im Abschnitt [!UICONTROL Reports] weiterhin anpassen, um die Metriken anzuzeigen, die für Ihre Analyse am relevantesten sind.

Diese Änderung wirkt sich nicht auf die Versandmetriken aus. Diese Änderung wirkt sich nur auf den in der Berichtsansicht angezeigten Standardfilter aus. Da RPV die am häufigsten verwendete Metrik unter Kunden ist, wurde dieser Standard ausgewählt, um Reporting-Workflows zu optimieren. Sie können innerhalb des [!UICONTROL Reports] Abschnitts jederzeit zu anderen Metriken wechseln.