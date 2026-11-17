---
keywords: Automatisches Targeting; Targeting; Traffic-Zuordnung; häufig gestellte Fragen; FAQ; Fehlerbehebung; Problembehebung; Traffic
description: Erfahren Sie mehr über Fehlerbehebungsthemen und häufig gestellte Fragen zu [!UICONTROL automatischen Targeting]-Aktivitäten.
title: Wie kann ich Fehler bei Aktivitäten [!UICONTROL  automatisches Targeting ]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
TQID: 'https://experienceleague.adobe.com/LXOa1Ma0y8VbncCPN1Az33p-GDsd-bW-BDqJjSGbVQU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 878df20c7fb08c893239135c20f358b5606d0c6f
workflow-type: tm+mt
source-wordcount: '1841'
ht-degree: 10%
---
# [!UICONTROL Automatisches Targeting] häufig gestellte Fragen und Fehlerbehebung {#auto-target-faqs}

>[!BEGINSHADEBOX]

**Auf dieser Seite** finden Sie Antworten auf häufig gestellte Fragen zu **[!UICONTROL automatischen Targeting]**-Aktivitäten und empfohlene Lösungen für häufige Probleme.

>[!ENDSHADEBOX]

Auf dieser Seite werden häufig gestellte Fragen (FAQs) beantwortet und die Schritte zur Fehlerbehebung bei **[!UICONTROL automatischen Targeting]**-Aktivitäten in [!DNL Adobe Target] beschrieben.

## Häufig gestellte Fragen {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Konsultieren Sie bei der Arbeit mit Aktivitäten vom Typ **[!UICONTROL Automatisches Targeting]** die folgenden Fragen und Antworten.

+++ Wie lauten die Best Practices zum Einrichten einer Aktivität vom Typ [!UICONTROL Automatisches Targeting]?

* Entscheiden Sie, ob der Geschäftswert einer Erfolgsmetrik **[!UICONTROL Umsatz pro Besuch]** (RPV) die zusätzlichen Traffic-Anforderungen wert ist. RPV benötigt in der Regel mindestens 1.000 Konversionen pro Erlebnis, damit eine Aktivität funktioniert, im Vergleich zu einer Konversion.
* Entscheiden Sie basierend auf Ihren Zielen über die Zuordnung zwischen Kontroll- und personalisierten Erlebnissen, bevor Sie mit der Aktivität beginnen.
* Stellen Sie fest, ob ausreichend Traffic zu der Seite vorhanden ist, auf der Ihre **[!UICONTROL Automatisches Targeting]**-Aktivität ausgeführt wird, damit die Personalisierungsmodelle in angemessener Zeit erstellt werden können.
* Wenn Sie den Personalisierungsalgorithmus testen, ändern Sie keine Erlebnisse und fügen Sie keine Profilattribute hinzu bzw. entfernen Sie sie nicht, während die Aktivität live ist.
* Erwägen Sie den Abschluss einer A/B-Aktivität zwischen den Angeboten und Standorten, die Sie in Ihrer **[!UICONTROL automatischen Targeting]**-Aktivität verwenden möchten, um sicherzustellen, dass die Standorte und Angebote Auswirkungen auf das Optimierungsziel haben. Wenn in einer A/B-Aktivität kein signifikanter Unterschied nachgewiesen wird **[!UICONTROL generiert]** Automatisches Targeting“ wahrscheinlich auch keine Steigerung.

  Wenn ein A/B-Test keine statistisch signifikanten Unterschiede zwischen den Erlebnissen aufzeigt, unterscheiden sich die von Ihnen in Betracht gezogenen Angebote wahrscheinlich nicht ausreichend voneinander, wirken sich die von Ihnen ausgewählten Standorte nicht auf die Erfolgsmetrik aus oder ist das Optimierungsziel in der Konversions-funnel zu weit, um von Ihren ausgewählten Angeboten beeinflusst zu werden.

* Nehmen Sie während der Aktivität keine wesentlichen Änderungen an den Erlebnissen vor.

+++

+++ Wird die Verwendung von automatischem Targeting bis zur Erstellung der Modelle mit einer Aufteilung von 90 (Kontrolle) zu 10 (Targeting) empfohlen?

Die optimale Aufteilung der Traffic-Zuordnung hängt davon ab, was Sie erreichen möchten.

Wenn es Ihr Ziel ist, so viel Traffic wie möglich zu personalisieren, können Sie während der Lebensdauer der Aktivität bei der zielgerichteten Zuordnung von 90 % und der Kontrolle von 10 % bleiben. Wenn Sie ein Experiment durchführen möchten, in dem die Leistung der Personalisierungsalgorithmen mit der Kontrolle verglichen wird, empfiehlt sich während der Lebensdauer der Aktivität eine Aufteilung von 50/50.

Best Practice ist es, die Aufteilung der Traffic-Zuordnung während der Lebensdauer der Aktivität beizubehalten, damit Besucher nicht zwischen Targeting- und Kontrollerlebnissen wechseln.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There is no way to go back and see when a model was completed.
-->

+++

+++ Wenn ein Besucher die Aktivität vom Typ [!UICONTROL Automatisches Targeting] nicht sieht und konvertiert, zählt dann die Konversion in meiner Aktivität?

Nein. Es werden nur Besucher im Bericht gezählt, die sich für die Aktivität **[!UICONTROL Automatisches Targeting]** qualifizieren und sie anzeigen.

+++

+++ Warum generiert meine [!UICONTROL Automatisches Targeting]-Aktivität keine Steigerung?

Die vier Faktoren, die zum Generieren der Steigerung erforderlich sind, und die empfohlene Lösung finden Sie im Fehlerbehebungsartikel [Meine Aktivität vom Typ Automatisches Targeting generiert keine Steigerung](#section_23995AB813F24525AF294D20A20875C8).

+++

+++ Wann sollte ich meine Aktivität vom Typ [!UICONTROL Automatisches Targeting] anhalten?

**[!UICONTROL Automatisches Targeting]** kann als eine „Always on“-Personalisierung verwendet werden, die kontinuierlich optimiert wird. Insbesondere für zeitlose Inhalte besteht keine Notwendigkeit, Ihre Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** anzuhalten.

Wenn Sie wesentliche Änderungen an den Inhalten in Ihrer Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** vornehmen möchten, empfiehlt es sich, eine neue Aktivität zu beginnen, damit andere Benutzer, die Berichte überprüfen, vergangene Ergebnisse nicht mit anderen Inhalten verwechseln oder in Beziehung setzen.

+++

+++ Wie lange sollte ich warten, bis Modelle erstellt werden?

Die Zeit, die die Modelle in Ihrer Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** benötigen, hängt in der Regel vom Traffic auf den jeweiligen Sites der Aktivität und von den Konversionsraten der in der Erfolgsmetrik der Aktivität festgelegten Metrik ab.

**[!UICONTROL Automatisches Targeting]** versucht erst dann, ein personalisiertes Modell für ein bestimmtes Erlebnis zu erstellen, wenn mindestens 50 Konversionen für dieses Erlebnis vorhanden sind. Außerdem wird das Modell nicht zur personalisierten Bereitstellung von Traffic verwendet, wenn die Qualität des erstellten Modells unzureichend ist (die Qualität wird durch Offline-Auswertung vorgehaltener „Test“-Daten mithilfe [einer Metrik namens AUC](https://de.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve) bestimmt).

Beachten Sie die folgenden Punkte bei der Modellerstellung in **[!UICONTROL Automatisches Targeting]**:

* Nach der Live-Schaltung einer Aktivität berücksichtigt **[!UICONTROL Automatisches Targeting]** beim Versuch, Modelle zu erstellen, die zufällig bereitgestellten Daten aus den letzten 45 Tagen. Beispielsweise Kontroll-Traffic sowie einige zusätzliche, zufällig bereitgestellte Daten, die vom Algorithmus vorgehalten werden.
* Wenn **[!UICONTROL Umsatz pro Besuch]** Ihre Erfolgsmetrik ist, benötigen diese Aktivitäten in der Regel mehr Daten zum Erstellen von Modellen, da die Varianz beim Besucherumsatz normalerweise höher als bei der Konversionsrate ist.
* Modelle werden für jedes Erlebnis erstellt. Wenn Sie also ein Erlebnis durch ein anderes ersetzen, muss für das neue Erlebnis ausreichend Traffic (mindestens 50 Konversionen) erfasst werden, bevor die personalisierten Modelle neu erstellt werden können.

Wenn die Erstellung Ihrer Modelle zu lange dauert, finden Sie weitere Informationen unter [Meine Aktivität vom Typ Automatisches Targeting benötigt zu lange, um Modelle zu erstellen](#section_23995AB813F24525AF294D20A20875C8).

+++

+++ Ein Modell wird in meiner Aktivität erstellt. Sind die Besuche bei diesem Erlebnis personalisiert?

Nein. In Ihrer Aktivität müssen mindestens zwei Modelle erstellt werden, damit die Personalisierung gestartet werden kann.

+++

+++ Ab wann kann ich die Ergebnisse meiner Aktivität vom Typ [!UICONTROL Automatisches Targeting] anzeigen?

Sie können die Ergebnisse Ihrer Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** anzeigen, nachdem mindestens zwei Erlebnisse Modelle erstellt haben (grünes Häkchen).

+++

+++ Kann ich ein bestimmtes Erlebnis als Kontrollerlebnis angeben?

Sie können bei der Erstellung einer [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP)- oder [AT)-Aktivität ein Kontrollerlebnis ](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

Mit dieser Funktion können Sie den gesamten Kontroll-Traffic basierend auf dem in der Aktivität konfigurierten Traffic-Zuordnungsprozentwert zu einem bestimmten Erlebnis leiten. Anschließend können Sie die Leistungsberichte des personalisierten Traffics mit dem Kontroll-Traffic zu diesem einen Erlebnis vergleichen.

Weitere Informationen finden Sie unter [Verwenden eines bestimmten Erlebnisses als Kontrolle](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

+++ Kann ich die Zielmetrik inmitten einer automatischen Targeting[!UICONTROL Aktivität ]?

Adobe rät davon ab, die Zielmetrik inmitten einer Aktivität zu ändern. Auch wenn es möglich ist, die Zielmetrik während einer Aktivität in der Benutzeroberfläche von [!DNL Target] zu ändern, sollten Sie dies nicht tun, sondern stattdessen eine neue Aktivität starten. Adobe garantiert nicht, was passiert, wenn Sie die Zielmetrik in einer Aktivität nach deren Ausführung ändern.

Diese Empfehlung gilt für **[!UICONTROL Automatische Zuordnung]**, **[!UICONTROL Automatisches Targeting]** und **[!UICONTROL Automated Personalization]**-Aktivitäten, die [!DNL Target] oder [!DNL Analytics] (A4T) als Berichtsquelle verwenden.

+++

+++ Kann ich die Option [!UICONTROL Berichtsdaten zurücksetzen] während ich eine Aktivität vom Typ [!UICONTROL Automatisches Targeting] ausführe?

Die Verwendung der **[!UICONTROL Berichtsdaten zurücksetzen]** Option für **[!UICONTROL Automatisches Targeting]**-Aktivitäten wird nicht empfohlen. Diese Option entfernt zwar die sichtbaren Berichtsdaten, nicht aber alle Trainingsdatensätze aus dem Modell **[!UICONTROL Automatisches Targeting]**. Statt die Option **[!UICONTROL Berichtsdaten zurücksetzen]** zu verwenden, eine neue Aktivität erstellen und die ursprüngliche Aktivität deaktivieren.

Diese Anleitung gilt auch für **[!UICONTROL Automatische Zuordnung]** und **[!UICONTROL Automated Personalization]**-Aktivitäten.

+++

+++ Was passiert, wenn ich ein einzelnes Erlebnis aus einer Aktivität vom Typ [!UICONTROL Automatisches Targeting] entferne?

[!DNL Target] erstellt für jedes Erlebnis ein eigenes Modell. Wenn Sie also ein Erlebnis entfernen, erstellt [!DNL Target] ein Modell weniger. Dies wirkt sich nicht auf die Modelle der anderen Erlebnisse aus.

Angenommen, Sie haben eine Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** mit acht Erlebnissen, und die Performance eines dieser Erlebnisse sagt Ihnen gar nicht zu. Sie können dieses Erlebnis entfernen. Dies wirkt sich nicht auf die Modelle der sieben verbleibenden Erlebnisse aus.

+++

## Fehlerbehebung [!UICONTROL Automatisches Targeting] {#section_23995AB813F24525AF294D20A20875C8}

Manchmal laufen die Aktivitäten nicht wie erwartet. In den folgenden Elementen werden mögliche Herausforderungen beschrieben, mit denen Sie bei der Verwendung von **[!UICONTROL Automatisches Targeting]** mit Lösungsvorschlägen konfrontiert sein könnten.

+++ Meine [!UICONTROL Automatisches Targeting]-Aktivität dauert zu lange, um Modelle zu erstellen.

Durch mehrere Änderungen bei der Einrichtung der Aktivität kann die für die Modellerstellung erwartete Zeit verkürzt werden, darunter die Anzahl der Erlebnisse in Ihrer **[!UICONTROL automatischen Targeting]**-Aktivität, der Traffic zu Ihrer Site und die ausgewählte Erfolgsmetrik.

**Lösung:** Überprüfen Sie die Einrichtung Ihrer Aktivität und stellen Sie fest, ob Sie Änderungen vornehmen möchten, um die Geschwindigkeit der Modellerstellung zu verbessern.

* Wenn Ihre Erfolgsmetrik auf **[!UICONTROL RPV]** eingestellt ist, können Sie zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Sie verlieren keine Aktivitätsdaten, wenn Sie die Erfolgsmetrik von RPV auf Konversion ändern.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Aktivitätskonversionsrate erhöht die Traffic-Anforderungen für zu erstellende Modelle, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es einige Erlebnisse, die Sie aus Ihrer Aktivität ausschließen können? Wenn Sie die Anzahl der Erlebnisse in einer Aktivität verringern, wird die Zeit zum Erstellen von Modellen verkürzt.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an Ihren Aktivitäts-Standorten vorhanden sind, desto schneller erstellen die Modelle.

Weitere Informationen zur Zeit, die Modelle benötigen, finden Sie unter [Wie lange sollte ich warten, bis Modelle erstellt werden?](#section_5C120A2B11D14D9BAF767BBAB50FED23).

+++

+++ Meine [!UICONTROL Automatisches Targeting]-Aktivität generiert keine Steigerung.

Vier Faktoren sind erforderlich, damit eine Aktivität vom Typ **[!UICONTROL Automatisches Targeting]** eine Steigerung generiert:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Stellen Sie zunächst sicher, dass Ihre Aktivität den Traffic personalisiert. Wenn nicht für alle Erlebnisse Modelle erstellt wurden, ]**Ihre Aktivität vom Typ „Automatisches Targeting**[!UICONTROL  nach wie vor einen erheblichen Teil der Besuche aus, um zu versuchen, alle Modelle so schnell wie möglich zu erstellen. Wenn keine Modelle erstellt werden **[!UICONTROL personalisiert „Automatisches Targeting]** den Traffic nicht.

Vergewissern Sie sich anschließend mithilfe eines einfachen, nicht personalisierten A/B-Tests, dass die Angebote und die Positionen der Aktivitäten wirklich einen Unterschied zu den Gesamtansprechraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass ausreichend Energie vorhanden ist, um einen angemessenen Anstieg zu erkennen, und führen Sie den A/B-Test für eine feste Dauer aus, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die A/B-Testergebnisse eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, ist es wahrscheinlich, dass eine personalisierte Aktivität funktioniert. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. In der Regel liegt das Problem daran, dass die Angebote und Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

+++ Jede von einer Konversionsmetrik abhängige Metrik konvertiert nie.

Dieses Ergebnis ist zu erwarten.

In einer **[!UICONTROL automatischen Targeting]**-Aktivität wird der Benutzer nach der Konvertierung einer Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein Post-Ziel handelt) aus dem Erlebnis entlassen und die Aktivität neu gestartet.

Nehmen wir zum Beispiel an, dass eine Aktivität mit einer Konversionsmetrik (C1) und einer zusätzlichen Metrik (A1) besteht. A1 hängt von C1 ab. Wenn ein Besucher zum ersten Mal in die Aktivität eintritt und die Kriterien zur Konvertierung von A1 und C1 nicht erfüllt sind, wird die Metrik A1 aufgrund der Abhängigkeit von der Erfolgsmetrik nicht konvertiert. Wenn der Besucher C1 und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da der Besucher beim Konvertieren von C1 freigeschaltet wird.

+++
