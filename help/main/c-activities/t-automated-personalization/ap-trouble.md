---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: Entdecken Sie die potenziellen Herausforderungen, vor denen Sie bei der Verwendung von [!UICONTROL Automated Personalization] (AP)-Aktivitäten in Adobe Target stehen könnten, zusammen mit Lösungsvorschlägen.
title: Wie kann ich Fehler bei [!UICONTROL Automated Personalization]-Aktivitäten beheben?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=de#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
TQID: https://experienceleague.adobe.com/1Qevyq-TiutN1dEZnfC1DDmUgXoHIxtBl-3RMPq-m-0
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 764
ht-degree: 30%

---

# Fehlerbehebung bei [!UICONTROL Automated Personalization]

Manchmal verlaufen Aktivitäten nicht erwartungsgemäß. Im Folgenden finden Sie einige potenzielle Herausforderungen, mit denen Sie bei der Verwendung von [!UICONTROL Automated Personalization] (AP) konfrontiert sein könnten, sowie einige Lösungsvorschläge.

## Meine [!UICONTROL Automated Personalization]-Aktivität braucht zu lange, um Modelle zu erstellen. {#section_20028B204DBB4D77A324BA193434AEE2}

+++Details anzeigen

Es gibt mehrere Änderungen beim Einrichten von Aktivitäten, die die erwartete Zeit zum Erstellen von Modellen reduzieren können, einschließlich der Anzahl der Erlebnisse in Ihrer [!UICONTROL Automated Personalization]-Aktivität, des Traffics auf Ihrer Site und Ihrer ausgewählten Erfolgsmetrik.

**Lösung:** Überprüfen Sie die Einrichtung Ihrer Aktivität und stellen Sie fest, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit zu verbessern, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Sie verlieren keine Aktivitätsdaten, wenn Sie die Erfolgsmetrik von RPV auf Konversion ändern.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die zum Erstellen von Modellen erforderlichen Traffic-Anforderungen, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Angebote oder Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an den Standorten Ihrer Aktivitäten auftreten, desto schneller können Modelle erstellt werden.

+++

## Meine Aktivität vom Typ Automated Personalization&quot; hat keine Steigerung generiert. {#section_8900BC8968474438B8092F7A94C0C6CF}

+++Details anzeigen

Es sind mehrere Faktoren erforderlich, damit eine Aktivität vom Typ [!UICONTROL Automated Personalization] eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen aus denen die Aktivitätserlebnisse bestehen, wirklich einen Unterschied zu den Gesamtantwortraten darstellen. Stellen Sie sicher, dass Sie die Stichprobengrößen im Voraus berechnen. Die vorzeitige Berechnung der Stichprobengrößen trägt dazu bei, sicherzustellen, dass ausreichend Strom vorhanden ist, um einen angemessenen Anstieg zu erkennen. Anschließend können Sie den A/B-Test für eine bestimmte Dauer ausführen, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn ein A/B-Testergebnis eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse ergibt, ist die Wahrscheinlichkeit hoch, dass eine personalisierte Aktivität erfolgreich ist. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. Normalerweise liegt das Problem darin, dass die Angebote oder Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

## Meine [!UICONTROL Automated Personalization]-Aktivitäts-URL zeigt Angebotsinhalte auf falschen Seiten an. {#section_82A224406DBF4107B05204BEFBBE458C}

+++Details anzeigen

In [!UICONTROL Automated Personalization] werden die URL- und Vorlagentestregeln zur [!DNL Target] Begrenzung für Anforderungseinträge hinzugefügt (z. B. target-global-mbox), wo sie nur einmal ausgewertet werden. Sobald sich ein Benutzer für eine Aktivität qualifiziert hat, werden die Targeting-Regeln auf Zielgruppen-Anfrageebene nicht neu ausgewertet. Die Zielgruppe wird jedoch zu Standort-Targeting-Regeln hinzugefügt.

**Lösung:** Fügen Sie die erforderlichen Vorlagenregeln als Eingabe-Audience der Aktivität hinzu. Eine Zielgruppenprüfung findet bei jeder Anforderung/jedem Aufruf statt.

+++

## Jede von einer Konversionsmetrik abhängige Metrik konvertiert nie. {#section_076D1F44298C4E4A849AC52F5A33214D}

+++Details anzeigen

Dieses Ergebnis ist zu erwarten.

In einer [!UICONTROL Automated Personalization]-Aktivität wird der Besucher nach der Konvertierung einer Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Post-Ziel handelt) aus dem Erlebnis entlassen und die Aktivität neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 hängt von C1 ab. Wenn ein Besucher die Aktivität das erste Mal antrifft und die Kriterien zum Konvertieren von A1 und C1 nicht konvertiert werden, wird die Metrik A1 aufgrund der Erfolgsmetrikabhängigkeit nicht konvertiert. Wenn der Besucher C1 und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da der Besucher beim Konvertieren von C1 freigeschaltet wird.

+++

## Meine Erlebnis-URLs funktionieren nicht erwartungsgemäß. {#section_7B08DA1F30AA483E9406336DAF361BA4}

+++Details anzeigen

* Wenn die Vorschau auf der neuen Registerkarte nicht angezeigt wird (aufgrund des Browser-Cache), aktualisieren Sie sie zwei- oder dreimal. Sie können den Link auch kopieren und in einem neuen Browser oder einer neuen Sitzung öffnen.
* Generieren Sie die Erlebnis-URL-Links erneut, wenn Sie Inhalte geändert haben, und geben Sie die neuen Links für Ihre Teamkollegen frei.

+++
