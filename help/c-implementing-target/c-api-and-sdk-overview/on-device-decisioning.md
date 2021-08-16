---
keywords: Server-seitig;Server-seitig;SDK;SDK;auf Gerät;Entscheidungsfindung;auf Gerät;Gerät;Nulllatenz;Latenz;nahe Null;node.js
description: Erfahren Sie, wie Sie mit der Entscheidungsfindung auf dem Gerät Ihre [!DNL Target] A/B- und MVT-Aktivitäten auf Ihrem Server zwischenspeichern können, um speicherinterne Entscheidungen bei nahezu Nulllatenz durchzuführen.
title: Was ist On-Device Decisioning?
feature: Serverseitig implementieren
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: fe70f357e2298f1656d713aae5fae800e6775d64
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 10%

---

# Geräteinterne Entscheidungsfindung

Die On-Device-Entscheidungsfindung bietet die Möglichkeit, Ihre [!DNL Adobe Target] [!UICONTROL A/B-Test]- und [!UICONTROL Erlebnis-Targeting](XT)-Aktivitäten auf Ihrem Server zwischenzuspeichern und speicherinterne Entscheidungen mit nahezu null Latenz durchzuführen, ohne Netzwerkanforderungen an das [!DNL Adobe Target] Edge-Netzwerk zu blockieren.

Weitere Informationen finden Sie unter [Einführung in On-Device Decisioning](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) in der *[Dokumentation zu Adobe Target SDKs](https://adobetarget-sdks.gitbook.io/docs/)*.

## Webinar: Personalisieren und Testen mit Nulllatenz bei geräteinterner Entscheidungsfindung mit [!DNL Adobe Target]

Marketer, Produkteigentümer und Entwickler sind mehr denn je gefordert, die Erlebnisse ihrer Kunden auf Websites, in Apps und überall dort, wo sie mit ihren Kunden in Kontakt treten, zu optimieren. Mehrere Tools mit Datensilos und komplizierten Implementierungen sind unzureichend.

In diesem aufgezeichneten Webinar besprechen [!DNL Adobe Target] Produktexperten, wie sich bewegende Entscheidungen zur Optimierung kritischer Erlebnisse auf dem Gerät zur lokalen Ausführung mit nahezu Nulllatenz aufregenden neuen Anwendungsfällen Tür und Tor öffnen und gleichzeitig die Site-Leistung für Ihre Kunden verbessern können.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## Best Practices.

Adobe empfiehlt die folgenden Best Practices bei der Verwendung von Entscheidungen auf dem Gerät:

### Best Practices bei der Entscheidungsmethode &quot;on device&quot; {#best-practices-on-device}

Bei Verwendung von &quot;on-device&quot;als Entscheidungsmethode wird das Artefakt heruntergeladen, wenn der Besucher die Webseite zum ersten Mal lädt. Eine Aktivitätsqualifikation, die beim ersten Laden der Seite (kein Cache) durchgeführt werden muss, erfolgt erst, nachdem das Artefakt vollständig heruntergeladen wurde. Es gibt bestimmte Best Practices, die Sie anwenden können, um sicherzustellen, dass Aktivitätsqualifikationen für einen neuen anonymen Besucher schnell erfolgen.

* Deaktivieren Sie &quot;On-Device&quot;-fähige Aktivitäten, die nicht im Artefakt enthalten sein sollen.
* Wenn Sie [!DNL Target Premium] haben, können Sie [properties/workspaces](/help/administrating-target/c-user-management/property-channel/property-channel.md) verwenden, um verschiedene Artefaktdateien für verschiedene Arbeitsbereiche zu erstellen.
* Wenn Ihre Artefaktdateien aus berechtigten Gründen sehr groß werden, können Sie die &quot;hybride&quot;Entscheidungsmethode verwenden. Mit dieser Methode können Sie das Artefakt parallel herunterladen und alle [!DNL Target] API-Aufrufe werden über das Kabel gesendet, bis das Artefakt heruntergeladen wurde. Weitere Informationen zu diesem Ansatz finden Sie im Abschnitt zu Best [Practices im &quot;Hybrid&quot;-Entscheidungsmodus](#best-practices-hybrid) unten.
* Wenn Sie über eine Single Page Application (SPA) verfügen, empfiehlt [!DNL Adobe], at.js zu laden und zu initialisieren, bevor Sie beim ersten Laden der Seite die JavaScript-Hauptdatei Ihrer Anwendung laden. Dieser Ansatz startet das Herunterladen des Artefakts viel früher und ermöglicht so ein schnelleres Erlebnis-Rendering.

### Best Practices bei der Entscheidungsmethode &quot;hybrid&quot; {#best-practices-hybrid}

Bei Verwendung von &quot;hybrid&quot;als Entscheidungsmethode wird das Artefakt parallel heruntergeladen. Bis zum Herunterladen des Artefakts werden alle [!DNL Target]-API-Aufrufe über das Kabel gesendet, selbst wenn die &quot;Standorte&quot;gerätefähig sind. Dieses Verhalten ist die Standardeinstellung für alle `getOffers()`-Aufrufe und bietet in den meisten Situationen die beste Leistung. Wenn Sie das Standardverhalten von `getOffers()` ändern, indem Sie `decisioningMethod` auf `on-device` setzen, befolgen Sie diese Best Practices, um Fehler zu vermeiden und die beste Leistung sicherzustellen.

* Wenn Sie `getOffers()` mit `decisioningMethod` als `on-device` aufrufen, wenn die Seite zum ersten Mal geladen wird, müssen Sie dies im Ereignis-Handler &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot;at.js tun, um Fehler zu vermeiden. Wenn Ihr Artefakt sehr groß ist, werden alle &quot;Orte&quot;, die diesen Ansatz verwenden, erst gerendert, nachdem das Artefakt vollständig heruntergeladen wurde. Dies kann das Rendern von Erlebnissen verzögern. [!DNL Adobe] empfiehlt, diesen Ansatz selten zu verwenden. Befolgen Sie die Best Practices zur Reduzierung der Artefaktgröße im Abschnitt [ Best Practices für On Device&quot;](#best-practices-on-device) oben bei Verwendung dieses Ansatzes.

## Tutorial: Entscheidung auf dem Gerät

[!DNL Adobe Target] Die Entscheidungsfindung auf dem Gerät ermöglicht die Bereitstellung von nahezu null Latenzinhalten.

Dieses 7-minütige Video:

* Beschreibt die Entscheidungsfindung auf dem Gerät, einschließlich des Vergleichs mit anderen Methoden der [!DNL Target]-Implementierung
* Zeigt, wie Sie Entscheidungen auf dem Gerät in [!DNL Target] aktivieren
* Untersucht eine formularbasierte Composer-Beispielaktivität, die mit JSON-Inhalten konfiguriert wurde
* Zeigt den Beispiel-Node.JS-SDK-Code mit der Schlüsselkonfiguration an, die für die Entscheidungsfindung auf dem Gerät erforderlich ist
* Zeigt Ergebnisse in einem Browser an

>[!VIDEO](https://video.tv.adobe.com/v/329032)

Weitere Videos und Tutorials finden Sie im Handbuch [Adobe Target-Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html?lang=de) .

## Adobe Tech Blog - Part 1: Führen Sie [!DNL Adobe Target] NodeJS SDK für Experimentierungen und Personalisierung auf Edge-Plattformen aus (Akamai Edge Workers).

[Klicken Sie hier , um auf den Blogpost](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9) zuzugreifen.

## Adobe Tech Blog – Part 2: Führen Sie das [!DNL Adobe Target] NodeJS SDK zum Experimentieren und Personalisieren auf Edge-Plattformen aus (AWS Lambda@Edge).

[Klicken Sie hier , um auf den Blogpost](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563) zuzugreifen.