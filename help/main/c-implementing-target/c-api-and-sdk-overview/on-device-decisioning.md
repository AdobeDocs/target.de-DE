---
keywords: Server-seitig;Server-seitig;SDK;SDK;auf Gerät;Entscheidungsfindung;auf Gerät;Gerät;Nulllatenz;Latenz;nahe Null;node.js
description: Erfahren Sie, wie Sie mit der Entscheidungsfindung auf dem Gerät Ihre [!DNL Target] A/B- und MVT-Aktivitäten auf Ihrem Server, um speicherinterne Entscheidungen bei nahezu Nulllatenz durchzuführen.
title: Was ist On-Device Decisioning?
feature: Implement Server-side
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 10%

---

# Geräteinterne Entscheidungsfindung

Die Entscheidungsfindung auf dem Gerät bietet die Möglichkeit, Ihre [!DNL Adobe Target] [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) -Aktivitäten auf Ihrem Server verwenden und speicherinterne Entscheidungen bei nahezu null Latenz durchführen, ohne Netzwerkanforderungen an die [!DNL Adobe Target] Edge Network.

Weitere Informationen finden Sie unter [Einführung in die geräteübergreifende Entscheidungsfindung](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) im *[Dokumentation zu Adobe Target SDKs](https://adobetarget-sdks.gitbook.io/docs/)*.

## Webinar: Personalisieren und Testen mit Nulllatenz bei geräteinterner Entscheidungsfindung mit [!DNL Adobe Target]

Marketer, Produkteigentümer und Entwickler sind mehr denn je gefordert, die Erlebnisse ihrer Kunden auf Websites, in Apps und überall dort, wo sie mit ihren Kunden in Kontakt treten, zu optimieren. Mehrere Tools mit Datensilos und komplizierten Implementierungen sind unzureichend.

In diesem aufgezeichneten Webinar [!DNL Adobe Target] Produktexperten besprechen, wie sich durch die Verschiebung kritischer Entscheidungen zur Erlebnisoptimierung auf dem Gerät zur lokalen Ausführung mit nahezu Nulllatenz die Türen für aufregende neue Anwendungsfälle öffnen und gleichzeitig die Site-Leistung für Ihre Kunden verbessern lassen.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## Best Practices.

Adobe empfiehlt die folgenden Best Practices bei der Verwendung von Entscheidungen auf dem Gerät:

### Best Practices bei der Entscheidungsmethode &quot;on device&quot; {#best-practices-on-device}

Bei Verwendung von &quot;on-device&quot;als Entscheidungsmethode wird das Artefakt heruntergeladen, wenn der Besucher die Webseite zum ersten Mal lädt. Eine Aktivitätsqualifikation, die beim ersten Laden der Seite (kein Cache) durchgeführt werden muss, erfolgt erst, nachdem das Artefakt vollständig heruntergeladen wurde. Es gibt bestimmte Best Practices, die Sie anwenden können, um sicherzustellen, dass Aktivitätsqualifikationen für einen neuen anonymen Besucher schnell erfolgen.

* Deaktivieren Sie &quot;On-Device&quot;-fähige Aktivitäten, die nicht im Artefakt enthalten sein sollen.
* Wenn Sie [!DNL Target Premium]können Sie [Eigenschaften/Arbeitsbereiche](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) , um verschiedene Artefaktdateien für verschiedene Arbeitsbereiche zu erstellen.
* Wenn Ihre Artefaktdateien aus berechtigten Gründen sehr groß werden, können Sie die &quot;hybride&quot;Entscheidungsmethode verwenden. Mit dieser Methode können Sie das Artefakt parallel und alle [!DNL Target] API-Aufrufe gehen über das Kabel, bis das Artefakt heruntergeladen wurde. Lesen Sie das Beste [Abschnitt &quot;Vorgehensweisen&quot;im &quot;Hybrid-Entscheidungsmodus&quot;](#best-practices-hybrid) weiter unten, um mehr über diesen Ansatz zu erfahren.
* Wenn Sie über eine Einzelseiten-App verfügen (SPA), [!DNL Adobe] empfiehlt, at.js zu laden und zu initialisieren, bevor Sie beim ersten Laden der Seite die JavaScript-Hauptdatei Ihrer Anwendung laden. Dieser Ansatz startet das Herunterladen des Artefakts viel früher und ermöglicht so ein schnelleres Erlebnis-Rendering.

### Best Practices bei der Entscheidungsmethode &quot;hybrid&quot; {#best-practices-hybrid}

Bei Verwendung von &quot;hybrid&quot;als Entscheidungsmethode wird das Artefakt parallel heruntergeladen. Bis zum Herunterladen des Artefakts können alle [!DNL Target] API-Aufrufe gehen über das Netzwerk, selbst wenn die &quot;Standorte&quot;gerätefähig sind. Dieses Verhalten ist standardmäßig für alle `getOffers()` und bietet in den meisten Situationen die beste Leistung. Wenn Sie das Standardverhalten von `getOffers()` durch Festlegen der `decisioningMethod` nach `on-device`folgen Sie diesen Best Practices, um Fehler zu vermeiden und die beste Leistung sicherzustellen.

* Wenn Sie `getOffers()` mit `decisioningMethod` as `on-device` Wenn die Seite zum ersten Mal geladen wird, müssen Sie dies im at.js-Ereignishandler &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot;tun, um Fehler zu vermeiden. Wenn Ihr Artefakt sehr groß ist, werden alle &quot;Orte&quot;, die diesen Ansatz verwenden, erst gerendert, nachdem das Artefakt vollständig heruntergeladen wurde. Dies kann das Rendern von Erlebnissen verzögern. [!DNL Adobe] empfiehlt, diesen Ansatz selten zu verwenden. Befolgen Sie die Best Practices, um die Artefaktgröße unter der [Abschnitt mit Best Practices für &quot;On Device&quot;](#best-practices-on-device) bei Verwendung dieses Ansatzes weiter oben beschrieben.

## Tutorial: Entscheidung auf dem Gerät

[!DNL Adobe Target] Die Entscheidungsfindung auf dem Gerät ermöglicht die Bereitstellung von nahezu null Latenzinhalten.

Dieses 7-minütige Video:

* Beschreibt die Entscheidungsfindung auf dem Gerät, einschließlich der Art und Weise, wie sie mit anderen Methoden von [!DNL Target] Implementierung
* Zeigt, wie Sie die Entscheidungsfindung auf dem Gerät in [!DNL Target]
* Untersucht eine formularbasierte Composer-Beispielaktivität, die mit JSON-Inhalten konfiguriert wurde
* Zeigt den Beispiel-Node.JS-SDK-Code mit der Schlüsselkonfiguration an, die für die Entscheidungsfindung auf dem Gerät erforderlich ist
* Zeigt Ergebnisse in einem Browser an

>[!VIDEO](https://video.tv.adobe.com/v/329032)

Weitere Videos und Tutorials finden Sie im Abschnitt [Adobe Target Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html?lang=de) Handbuch.

## Adobe Tech Blog - Part 1: Ausführen [!DNL Adobe Target] NodeJS-SDK für Experimentierung und Personalisierung auf Edge-Plattformen (Akamai Edge Workers)

[Klicken Sie hier , um auf den Blogpost zuzugreifen.](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9).

## Adobe Tech Blog – Part 2: Führen Sie das [!DNL Adobe Target] NodeJS SDK zum Experimentieren und Personalisieren auf Edge-Plattformen aus (AWS Lambda@Edge)

[Klicken Sie hier , um auf den Blogpost zuzugreifen.](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563).