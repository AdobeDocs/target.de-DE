---
keywords: Multivariater Test; MVT; MVT-Plan; Multivariater Testplan
description: Erfahren Sie, wie Sie einen [!UICONTROL Multivarianz-Test] in [!DNL Adobe Target] planen, damit Sie einen erfolgreichen Test erstellen können.
title: Wie plane ich einen [!UICONTROL Multivarianz-]?
feature: Multivariate Tests
exl-id: 130718d5-7bd9-4b1a-b81a-7a146f0ffd0d
TQID: 'https://experienceleague.adobe.com/Fg9jOrPlkLxpbJdG-AKoWHD3YvIGEJPu7Os-RdfXvQA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 62%
---
# Planen eines [!UICONTROL Multivarianz-Tests]

[!UICONTROL Multivariate Tests] (MVT) -Aktivitäten in [!DNL Adobe Target] erfordern eine gewisse Planung, bevor Sie einen erfolgreichen Test erstellen können.

MVT erfordert ausreichend Traffic, um nützliche Ergebnisse zu generieren. Vor der Einrichtung Ihres Tests sollten Sie sich über Ihr übliches Traffic-Aufkommen im Klaren sein, einschließlich der Anzahl der Impressionen und Konversionen. Diese Informationen helfen dabei, die Wahrscheinlichkeit zu verringern, einen Test mit Anforderungen zu entwerfen, die den Traffic Ihrer Site überschreiten.

Elemente müssen voneinander unabhängig sein. Testen Sie z. B. Ihr Layout und Ihren Inhalt nicht im selben Test.

Untersuchen Sie den HTML-Code auf den Seiten, die Sie testen möchten. Stellen Sie sicher, dass die HTML-Elemente auf Ihrer Site keine doppelten DOM-IDs aufweisen. Doppelte IDs können dazu führen, dass derselbe Inhalt an mehr als einen Ort geliefert wird.

Planen Sie den Test der Elemente auf Ihrer Seite, die mit großer Wahrscheinlichkeit signifikante Ergebnisse produzieren. Zum Beispiel führt ein Banner oder ein Hero Image wahrscheinlich zu mehr Konversionen als eine Änderung der Fußzeile. Wenn Sie weniger einflussreiche Elemente mit in Ihren Test aufnehmen, erhöhen sich dadurch lediglich das Traffic-Aufkommen und die erforderliche Zeit zum Test der markanteren Elemente auf der Seite.

Schließlich sollten Sie vor der Erstellung Ihres Tests Inhalt erstellen, den Sie testen möchten. Machen Sie sich mit den unterschiedlichen Inhalten für jedes Angebot vertraut und erstellen Sie Bilder, Text und HTML-Angebote, die Sie wahrscheinlich im Test verwenden werden.

## Schulungsvideo: Erstellen von Multivarianz-Tests (9:25) ![Tutorial-Badge](/help/main/assets/tutorial.png)

In diesem Video wird gezeigt, wie Sie mit dem [!DNL Target] dreistufigen Workflow einen Multivarianz-Test planen und erstellen.

* Definieren und gestalten eines Multivariater Tests
* Erstellen eines Multivarianz-Tests

>[!VIDEO](https://video.tv.adobe.com/v/17395)
