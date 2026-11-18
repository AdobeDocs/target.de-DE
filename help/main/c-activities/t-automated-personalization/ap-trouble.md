---
keywords: Automated Personalization;AP;Fehlerbehebung;Fehlerbehebung;Modell;Steigerung
description: Entdecken Sie die potenziellen Herausforderungen, vor denen Sie bei der Verwendung von [!UICONTROL Automated Personalization] (AP)-Aktivitäten in Adobe Target stehen könnten, zusammen mit Lösungsvorschlägen.
title: Wie kann ich Fehler bei [!UICONTROL Automated Personalization]-Aktivitäten beheben?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Hier finden Sie Informationen zum Lieferumfang von Target Premium."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
TQID: 'https://experienceleague.adobe.com/1Qevyq-TiutN1dEZnfC1DDmUgXoHIxtBl-3RMPq-m-0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 7%
---
# Fehlerbehebung bei [!UICONTROL Automated Personalization] {#ap-troubleshooting}

>[!BEGINSHADEBOX]

**Auf dieser Seite** finden Sie Lösungen für häufige Probleme mit **[!UICONTROL Automated Personalization]**-Aktivitäten.

>[!ENDSHADEBOX]

Aktivitäten laufen nicht immer erwartungsgemäß ab. Anhand der folgenden Liste können Sie die Ursache häufiger Probleme bei [!UICONTROL Automated Personalization] (AP)-Aktivitäten identifizieren und die vorgeschlagene Lösung anwenden.

## Modelle und Aufzug {#models-and-lift}

+++ Meine [!UICONTROL Automated Personalization]-Aktivität braucht zu lange, um Modelle zu erstellen

Mehrere Optionen zum Einrichten von Aktivitäten wirken sich auf die Zeit aus, die Modelle erstellen müssen, einschließlich der Anzahl der Erlebnisse in Ihrer **[!UICONTROL Automated Personalization]**-Aktivität, des Traffics auf Ihrer Site und der ausgewählten Erfolgsmetrik.

**Lösung:** Überprüfen Sie die Einrichtung Ihrer Aktivität und überprüfen Sie, ob Sie Änderungen vornehmen können, die die Geschwindigkeit verbessern, mit der Modelle erstellt werden.

* Wenn Ihre Erfolgsmetrik auf „RPV“ festgelegt ist, können Sie dann zur Konversion wechseln? Bei Konversionsaktivitäten ist in der Regel weniger Traffic zum Erstellen von Modellen erforderlich. Sie verlieren keine Aktivitätsdaten, wenn Sie die Erfolgsmetrik von RPV auf Konversion ändern.
* Liegt Ihre Erfolgsmetrik weit unten im Verkaufstrichter Ihrer Aktivitätserlebnisse? Eine niedrigere Konversionsrate erhöht die Traffic-Anforderungen für zu erstellende Modelle, da eine Mindestanzahl an Konversionen erforderlich ist.
* Gibt es Angebote oder Erlebnisse, die Sie von Ihrer Aktivität ausschließen können? Das Verringern der Anzahl von Erlebnissen in einer Aktivität beschleunigt die Zeit zum Erstellen von Modellen.
* Gibt es eine Seite mit höherem Traffic, auf der diese Aktivität erfolgreicher wäre? Je mehr Traffic und Konversionen an den Standorten Ihrer Aktivitäten auftreten, desto schneller können Modelle erstellt werden.

+++

+++ Meine Aktivität vom Typ [!UICONTROL Automated Personalization] hat keine Steigerung generiert

Für eine **[!UICONTROL Automated Personalization]**-Aktivität sind mehrere Faktoren erforderlich, um eine Steigerung zu generieren:

* Die Angebote müssen unterschiedlich genug sein, um die Besucher zu beeinflussen.
* Die Angebote müssen sich an einer Stelle befinden, die einen Unterschied zum Optimierungsziel darstellt.
* Es müssen genügend Traffic- und Teststärke im Test vorhanden sein, um die Steigerung zu ermitteln.
* Der Personalisierungsalgorithmus muss gut funktionieren.

**Lösung:** Es empfiehlt sich zunächst mithilfe eines einfachen, nicht personalisierten A/B-Tests sicherzustellen, dass der Inhalt und die Positionen, aus denen die Aktivitätserlebnisse bestehen, tatsächlich einen Unterschied zu den Gesamtansprechraten darstellen. Berechnen Sie die Stichprobengrößen im Voraus, um sicherzustellen, dass ausreichend Energie vorhanden ist, um einen angemessenen Anstieg zu erkennen, und führen Sie dann den A/B-Test für eine feste Dauer durch, ohne ihn anzuhalten oder Änderungen vorzunehmen. Wenn die A/B-Testergebnisse eine statistisch signifikante Steigerung eines oder mehrerer Erlebnisse zeigen, ist eine personalisierte Aktivität wahrscheinlich erfolgreich. Personalization kann auch dann funktionieren, wenn sich die Gesamtansprechraten der Erlebnisse nicht unterscheiden. Normalerweise liegt das Problem darin, dass die Angebote oder Standorte keine ausreichende Auswirkung auf das Optimierungsziel haben, um mit statistischer Signifikanz erkannt zu werden.

+++

## Aktivitätseinrichtung und Reporting {#setup-and-reporting}

+++ Meine [!UICONTROL Automated Personalization]-Aktivitäts-URL zeigt Angebotsinhalte auf falschen Seiten an

**Ursache:** In **[!UICONTROL Automated Personalization]** werden die URL- und Vorlagentestregeln zur Einschränkung für den Eintrag von [!DNL Target]-Anfragen hinzugefügt (z. B. target-global-mbox), wo sie nur einmal ausgewertet werden. Nachdem sich ein Besucher für eine Aktivität qualifiziert hat, werden die Zielgruppenbestimmungsregeln auf [!DNL Target] Anforderungsebene nicht neu ausgewertet, während die Zielgruppe für die Zielgruppenbestimmung zu den Zielgruppenbestimmungsregeln für Standorte hinzugefügt wird.

**Lösung:** Fügen Sie die erforderlichen Vorlagenregeln als Eingabe-Audience der Aktivität hinzu. Die Zielgruppe wird bei jeder Anfrage (Aufruf) ausgewertet.

+++

+++ Jede von einer Konversionsmetrik abhängige Metrik konvertiert nie

Dieses Verhalten ist zu erwarten.

In einer **[!UICONTROL Automated Personalization]**-Aktivität wird der Besucher nach der Konvertierung einer Konversionsmetrik (unabhängig davon, ob es sich um ein Optimierungsziel oder ein POST-Ziel handelt) aus dem Erlebnis entlassen und die Aktivität neu gestartet.

Eine Aktivität hat beispielsweise eine Konversionsmetrik (C1) und eine zusätzliche Metrik (A1), die von C1 abhängt. Wenn ein Besucher zum ersten Mal in die Aktivität eintritt und weder C1 noch A1 konvertiert hat, wird A1 aufgrund der Abhängigkeit von der Erfolgsmetrik nicht konvertiert. Wenn der Besucher C1 und dann A1 konvertiert, wird A1 immer noch nicht konvertiert, da der Besucher beim Konvertieren von C1 freigegeben wird.

+++

+++ Meine Erlebnis-URLs funktionieren nicht erwartungsgemäß

**Lösung:** Verwenden Sie die folgenden Aktionen:

* Wenn die Vorschau auf der neuen Registerkarte nicht angezeigt wird (aufgrund des Browser-Cache), aktualisieren Sie zwei oder drei Mal. Sie können den Link auch kopieren und in einem neuen Browser oder einer neuen Sitzung öffnen.
* Wenn Sie Inhalte geändert haben, generieren Sie die Erlebnis-URL-Links neu und teilen Sie die neuen Links mit Ihren Teamkollegen.

+++
