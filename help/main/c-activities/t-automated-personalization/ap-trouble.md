---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: Erfahren Sie mehr über die potenziellen Herausforderungen bei der Verwendung von [!UICONTROL Automated Personalization] (AP)-Aktivitäten in Adobe Target und lernen Sie Lösungsvorschläge kennen.
title: Wie kann ich Fehler bei [!UICONTROL Automated Personalization] Aktivitäten beheben?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
source-git-commit: 2cb2c2b68f6487d1af41ecc7e73750afa1ad85f9
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 32%

---

# Fehlerbehebung [!UICONTROL Automated Personalization]

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, mit denen Sie bei der Verwendung von [!UICONTROL Automated Personalization] (AP) konfrontiert sein könnten, sowie einige Lösungsvorschläge.

## Meine [!UICONTROL Automated Personalization]-Aktivität braucht zu lange, um Modelle zu erstellen. {#section_20028B204DBB4D77A324BA193434AEE2}

+++Siehe Details

Es gibt mehrere Änderungen beim Einrichten von Aktivitäten, die die erwartete Zeit zum Erstellen von Modellen reduzieren können, einschließlich der Anzahl der Erlebnisse in Ihrer [!UICONTROL Automated Personalization], des Traffics auf Ihrer Site und Ihrer ausgewählten Erfolgsmetrik.

**Lösung:** Überprüfen Sie die Einrichtung Ihrer Aktivität und stellen Sie fest, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Sie verlieren keine Aktivitätsdaten, wenn Sie die Erfolgsmetrik von RPV auf Konversion ändern.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Angebote oder Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an den Standorten Ihrer Aktivitäten auftreten, desto schneller können Modelle erstellt werden.

+++

## Meine [!UICONTROL Automated Personalization] Aktivität hat keinen Anstieg erzeugt. {#section_8900BC8968474438B8092F7A94C0C6CF}

+++Siehe Details

Es sind mehrere Faktoren erforderlich, damit eine [!UICONTROL Automated Personalization] Aktivität eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Stellen Sie sicher, dass Sie die Stichprobengrößen im Voraus berechnen. Die vorzeitige Berechnung der Stichprobengrößen trägt dazu bei, sicherzustellen, dass ausreichend Strom vorhanden ist, um einen angemessenen Anstieg zu erkennen. Anschließend können Sie den A/B-Test für eine bestimmte Dauer ausführen, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn ein A/B-Testergebnis eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse ergibt, ist die Wahrscheinlichkeit hoch, dass eine personalisierte Aktivität erfolgreich ist. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. Normalerweise liegt das Problem darin, dass die Angebote oder Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

## Meine [!UICONTROL Automated Personalization] Aktivitäts-URL zeigt Angebotsinhalte auf falschen Seiten an. {#section_82A224406DBF4107B05204BEFBBE458C}

+++Siehe Details

In [!UICONTROL Automated Personalization] werden die URL- und Vorlagentestregeln zur [!DNL Target] Begrenzung für Anforderungseinträge hinzugefügt (z. B. target-global-mbox), wobei sie nur einmal ausgewertet werden. Sobald sich ein Benutzer für eine Aktivität qualifiziert hat, werden die Targeting-Regeln auf Zielgruppen-Anfrageebene nicht neu ausgewertet. Die Zielgruppe wird jedoch zu Standort-Targeting-Regeln hinzugefügt.

**Lösung:** Fügen Sie die erforderlichen Vorlagenregeln als Eingabe-Audience der Aktivität hinzu. Eine Zielgruppenprüfung findet bei jeder Anforderung/jedem Aufruf statt.

+++

## Jede von einer Konversionsmetrik abhängige Metrik konvertiert nie. {#section_076D1F44298C4E4A849AC52F5A33214D}

+++Siehe Details

Dieses Ergebnis ist zu erwarten.

In einer [!UICONTROL Automated Personalization] Aktivität wird der Besucher nach der Konvertierung einer Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Post-Ziel handelt) aus dem Erlebnis entlassen und die Aktivität neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 hängt von C1 ab. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da der Besucher beim Konvertieren von C1 freigeschaltet wird.

+++

## Meine Erlebnis-URLs funktionieren nicht erwartungsgemäß.  {#section_7B08DA1F30AA483E9406336DAF361BA4}

+++Siehe Details

* Wenn die Vorschau auf der neuen Registerkarte nicht angezeigt wird (aufgrund des Browser-Cache), aktualisieren Sie sie zwei- oder dreimal. Sie können den Link auch kopieren und in einem neuen Browser oder einer neuen Sitzung öffnen.
* Generieren Sie die Erlebnis-URL-Links erneut, wenn Sie Inhalte geändert haben, und geben Sie die neuen Links für Ihre Teamkollegen frei.

+++
