---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: Potenzielle Herausforderungen bei der Verwendung von [!UICONTROL Automated Personalization] (AP)-Aktivitäten in Adobe Target zusammen mit empfohlenen Lösungen.
title: Fehlerbehebung [!UICONTROL Automated Personalization] Aktivitäten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Erfahren Sie, was in Target Premium enthalten ist."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
source-git-commit: 2cb2c2b68f6487d1af41ecc7e73750afa1ad85f9
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 31%

---

# Fehlerbehebung [!UICONTROL Automated Personalization]

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, denen Sie bei der Verwendung von [!UICONTROL Automated Personalization] (AP) und einige empfohlene Lösungen.

## My [!UICONTROL Automated Personalization] -Aktivität braucht zu lange, um Modelle zu erstellen. {#section_20028B204DBB4D77A324BA193434AEE2}

+++Siehe Details

Es gibt verschiedene Aktivitätseinrichtungsänderungen, die die erwartete Zeit zum Erstellen von Modellen verringern können, einschließlich der Anzahl der Erlebnisse in Ihren [!UICONTROL Automated Personalization] Aktivität, den Traffic zu Ihrer Site und Ihre ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie Ihre Aktivitätseinrichtung und sehen Sie, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu erhöhen, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Sie verlieren keine Aktivitätsdaten, wenn Sie die Erfolgsmetrik von RPV in Konversion ändern.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Angebote oder Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen beschleunigt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen in Ihren Aktivitätsstandorten vorhanden sind, desto schneller werden Modelle erstellt.

+++

## My [!UICONTROL Automated Personalization] -Aktivität keine Steigerung generiert hat. {#section_8900BC8968474438B8092F7A94C0C6CF}

+++Siehe Details

Für eine [!UICONTROL Automated Personalization] -Aktivität zur Steigerung:

* Die Angebote müssen so unterschiedlich sein, dass sie Besucher beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die für das Optimierungsziel von Bedeutung ist.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Stellen Sie sicher, dass Sie die Stichprobengrößen vorzeitig berechnen. Durch die vorzeitige Berechnung der Stichprobengrößen können Sie sicherstellen, dass ausreichend Strom vorhanden ist, um eine angemessene Steigerung zu sehen. Anschließend können Sie den A/B-Test für eine feste Dauer ausführen, ohne ihn zu stoppen oder Änderungen vorzunehmen. Wenn ein A/B-Test-Ergebnis eine statistisch signifikante Steigerung für eines oder mehrere Erlebnisse zeigt, ist es wahrscheinlich, dass eine personalisierte Aktivität erfolgreich ist. Personalisierung kann auch dann funktionieren, wenn es keine Unterschiede in den Gesamt-Antwortraten der Erlebnisse gibt. In der Regel ist das Problem auf Angebote oder Standorte zurückzuführen, die keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Bedeutung erkannt zu werden.

+++

## My [!UICONTROL Automated Personalization] Aktivitäts-URL zeigt Angebotsinhalte auf falschen Seiten an. {#section_82A224406DBF4107B05204BEFBBE458C}

+++Siehe Details

In [!UICONTROL Automated Personalization], werden die URL- und Vorlagentestregeln zum [!DNL Target] Einstiegsbeschränkung für Anfragen (z. B. target-global-mbox), bei der sie nur einmal ausgewertet werden. Wenn sich ein Benutzer für eine Aktivität qualifiziert hat, werden die Targeting-Regeln auf Target-Anfragebene nicht erneut ausgewertet. Die Zielgruppe wird jedoch zu Standort-Targeting-Regeln hinzugefügt.

**Lösung:** Fügen Sie die erforderlichen Vorlagenregeln als Eingabe-Audience der Aktivität hinzu. Eine Zielgruppenprüfung findet bei jeder Anforderung/jedem Aufruf statt.

+++

## Metriken, die von einer Konversionsmetrik abhängig sind, werden nicht konvertiert. {#section_076D1F44298C4E4A849AC52F5A33214D}

+++Siehe Details

Dieses Ergebnis ist zu erwarten.

In einer [!UICONTROL Automated Personalization] Aktivität, sobald eine Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Postziel handelt) konvertiert wurde, wird der Besucher aus dem Erlebnis freigesetzt und die Aktivität wird neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 ist von C1 abhängig. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 konvertiert und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da bei der Konvertierung von C1 der Besucher freigegeben wird.

+++

## Meine Erlebnis-URLs funktionieren nicht erwartungsgemäß.  {#section_7B08DA1F30AA483E9406336DAF361BA4}

+++Siehe Details

* Wenn Sie die Vorschau nicht auf der neuen Registerkarte sehen können (aufgrund des Browser-Cache), versuchen Sie, die Seite zwei- oder dreimal zu aktualisieren. Sie können den Link auch kopieren und in einem neuen Browser oder einer neuen Sitzung öffnen.
* Generieren Sie die Erlebnis-URL-Links erneut, wenn Sie Inhalte geändert haben, und geben Sie die neuen Links für Ihre Teamkollegen frei.

+++
