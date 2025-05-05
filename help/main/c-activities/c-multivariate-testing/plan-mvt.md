---
keywords: Multivariater Test; MVT; MVT-Plan; Multivariater Testplan
description: Erfahren Sie, wie Sie ein [!UICONTROL Multivariate Test] in planen [!DNL Adobe Target]  damit Sie einen erfolgreichen Test erstellen können.
title: Wie plane ich ein [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 130718d5-7bd9-4b1a-b81a-7a146f0ffd0d
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 64%

---

# [!UICONTROL Multivariate Test] planen

[!UICONTROL Multivariate Tests] (MVT) -Aktivitäten in [!DNL Adobe Target] erfordern eine gewisse Planung, bevor Sie einen erfolgreichen Test erstellen können.

MVT erfordert ausreichend Traffic, um nützliche Ergebnisse zu generieren. Vor der Einrichtung Ihres Tests sollten Sie sich über Ihr übliches Traffic-Aufkommen im Klaren sein, einschließlich der Anzahl der Impressionen und Konversionen. Diese Informationen helfen dabei, die Wahrscheinlichkeit zu verringern, einen Test mit Anforderungen zu entwerfen, die den Traffic Ihrer Site überschreiten.

Elemente müssen voneinander unabhängig sein. Testen Sie z. B. Ihr Layout und Ihren Inhalt nicht im selben Test.

Untersuchen Sie den HTML-Code für die Seiten, die Sie testen möchten. Stellen Sie sicher, dass die HTML-Elemente auf Ihrer Site keine doppelten DOM-IDs aufweisen. Doppelte IDs können dazu führen, dass derselbe Inhalt an mehr als einen Ort geliefert wird.

Planen Sie den Test der Elemente auf Ihrer Seite, die mit großer Wahrscheinlichkeit signifikante Ergebnisse produzieren. Zum Beispiel führt ein Banner oder ein Heldenbild wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Elemente mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Elemente auf der Seite.

Schließlich sollten Sie vor der Erstellung Ihres Tests Inhalt erstellen, den Sie testen möchten. Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Test verwenden werden.

## Schulungsvideo: Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Sie mit dem [!DNL Target] dreistufigen Workflow einen Multivarianz-Test planen und erstellen.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/30168?captions=ger)
