---
description: Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, die sich möglicherweise aus der Verwendung der automatisierten Personalisierung ergeben, sowie die jeweils vorgeschlagenen Lösungen.
title: Fehlerbehebung bei der automatisierten Personalisierung
feature: ap
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 94%

---


# ![PREMIUM](/help/assets/premium.png) Fehlerbehebung bei der automatisierten Personalisierung{#troubleshoot-automated-personalization}

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, die sich möglicherweise aus der Verwendung der automatisierten Personalisierung ergeben, sowie die jeweils vorgeschlagenen Lösungen.

## Die Aktivität meiner automatisierten Personalisierung braucht zu lange, um Modelle zu erstellen. {#section_20028B204DBB4D77A324BA193434AEE2}

Es gibt verschiedene Aktivitätseinrichtungsänderungen, welche die zum Erstellen von Modellen erwartete Dauer verringern können. Dazu zählen die Anzahl der Erlebnisse in Ihrem Test „Automatisierte Personalisierung“, der Traffic auf Ihrer Site sowie Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung dahingehend, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, in der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Wenn Sie die Erfolgsmetrik von „RPV“ in „Konversion“ ändern, gehen keine Aktivitätsdaten verloren.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Angebote oder Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn die Anzahl der Erlebnisse in einer Aktivität verringert wird, wird das Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitätspositionen vorhanden sind, desto schneller werden die Modelle erstellt.

## Die Aktivität meiner automatisierten Personalisierung generiert keine Steigerung.   {#section_8900BC8968474438B8092F7A94C0C6CF}

Es sind verschiedene Faktoren erforderlich, damit eine Aktivität vom Typ „Automatisierte Personalisierung“ eine Steigerung generiert:

* Die Angebote müssen sich stark genug voneinander unterscheiden, um Besucher zu beeinflussen.
* Die Angebote müssen sich dort befinden, wo sie einen Unterschied für das Optimierungsziel ausmachen.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass eine ausreichende Leistung vorliegt, um eine angemessene Steigerung zu sehen. Führen Sie zudem den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn in den Ergebnissen eines A/B-Tests eine signifikante Steigerung von mindestens einem Erlebnis gezeigt wird, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Natürlich kann die Personalisierung selbst dann funktionieren, wenn keine Unterschiede in den Gesamtantwortraten der Erlebnisse vorliegen. Das Problem geht in der Regel auf Angebote/Positionen zurück, die sich nicht stark genug auf das mit statistischer Bedeutung zu ermittelnde Optimierungsziel auswirken.

## Die Aktivitäts-URL meiner automatisierten Personalisierung zeigt Angebotsinhalte auf falschen Seiten an.   {#section_82A224406DBF4107B05204BEFBBE458C}

In AP werden die URL- und Vorlagentestregeln der Anforderungseingabebeschränkung [!DNL Target] hinzugefügt (z. B. Zielgruppe-global-mbox), wo sie nur einmal ausgewertet werden. Sobald sich ein Benutzer für eine Aktivität qualifiziert hat, werden die Targeting-Regeln auf Zielgruppe-Anforderungsebene nicht erneut bewertet. Die Zielgruppe wird jedoch zu Standort-Targeting-Regeln hinzugefügt.

**Lösung:** Fügen Sie die erforderlichen Vorlagenregeln als Eingabezielgruppe der Kampagne hinzu. Eine Zielgruppenprüfung findet bei jeder Anforderung/jedem Aufruf statt.

Dieses Problem wird in einer kommenden Aktualisierung behoben.

## Die von einer Konversionsmetrik abhängigen Metriken werden nicht konvertiert.   {#section_076D1F44298C4E4A849AC52F5A33214D}

Dieses Ergebnis ist zu erwarten.

Bei einer automatisierten Personalisierungsaktivität wird der Benutzer von dem Erlebnis abgekoppelt und die Aktivität neu gestartet, sobald eine Konversionsmetrik (egal ob Optimierungsziel oder Postziel) konvertiert wurde.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist abhängig von C1. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 konvertiert und erst danach A1, wird A1 auch dann nicht konvertiert, da der Besucher abgekoppelt wird, sobald C1 konvertiert ist.

## Meine Erlebnis-URLs funktionieren nicht erwartungsgemäß.   {#section_7B08DA1F30AA483E9406336DAF361BA4}

* Wenn Sie die Vorschau nicht auf der neuen Registerkarte anzeigen können (aufgrund des Browser-Caches), aktualisieren Sie die Seite zwei- oder dreimal oder kopieren Sie den Link und öffnen Sie ihn in einem neuen Browser oder in einer neuen Sitzung.
* Generieren Sie die Erlebnis-URL-Links erneut, wenn Sie Inhalte geändert haben, und geben Sie die neuen Links für Ihre Teamkollegen frei.

