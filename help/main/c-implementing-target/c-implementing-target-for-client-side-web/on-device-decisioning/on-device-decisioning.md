---
keywords: Implementierung;JavaScript-Bibliothek;js;at.js;on-device Decisioning;on device decisioning;at.js;on-device;on device
description: Erfahren Sie, wie Sie mit der at.js-Bibliothek geräteübergreifende Entscheidungen treffen können.
title: Wie funktioniert die Entscheidungsfindung auf dem Gerät mit der JavaScript-Bibliothek at.js?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '3552'
ht-degree: 18%

---

# Entscheidungsfindung auf dem Gerät für at.js

Ab Version 2.5.0 bietet at.js Entscheidungen auf Geräten. Über die Entscheidungsfindung auf dem Gerät können Sie Ihre [A/B-Test](/help/main/c-activities/t-test-ab/test-ab.md) und [Erlebnis-Targeting](/help/main/c-activities/t-experience-target/experience-target.md) (XT) -Aktivitäten im Browser, um speicherinterne Entscheidungen ohne blockierende Netzwerkanforderung für die [!DNL Adobe Target] Edge Network.

[!DNL Target] bietet außerdem die Flexibilität, das relevanteste und aktuellste Erlebnis aus Ihren Experimentierungs- und maschinell lernfähigen (ML-gesteuerten) Personalisierungsaktivitäten über einen Live-Server-Aufruf bereitzustellen. Mit anderen Worten: Wenn die Leistung am wichtigsten ist, können Sie die Entscheidungsfindung auf dem Gerät verwenden. Wenn jedoch das relevanteste, aktuellste und ML-gesteuerte Erlebnis benötigt wird, kann stattdessen ein Server-Aufruf durchgeführt werden.

## Welche Vorteile bietet die Entscheidungsfindung auf dem Gerät?

Zu den Vorteilen der geräteübergreifenden Entscheidungsfindung gehören:

* **Schnelle Entscheidungen und Erlebnisse bieten.** Bucketing- und Entscheidungsfindung werden im Arbeitsspeicher und im Browser durchgeführt, um zu verhindern, dass Netzwerkanforderungen blockiert werden.
* **Verbessern der Anwendungsleistung.** Führen Sie Experimente durch und liefern Sie Ihren Kunden und Benutzern Personalisierung, ohne die Benutzererfahrungen der Endbenutzer zu beeinträchtigen.
* **Verbessern der Google-Site-Qualitätsbewertung.** Wenn Entscheidungen im Speicher getroffen werden, verbessern Sie die Google Site Quality-Bewertung Ihres Onlinegeschäfts, um ihn für die Verbraucher leichter zu finden.
* **Erfahren Sie mehr über Echtzeitanalysen.** Erhalten Sie Einblicke aus Ihrer Aktivitätsleistung in Echtzeit über [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) Berichterstellung (A4T). Mit A4T können Sie Ihre Strategie in kritischen Momenten umdrehen.

## Unterstützte Funktionen

Das Adobe Target JS SDK bietet Kunden die Möglichkeit, für Entscheidungen zwischen Leistung und Aktualisierung von Daten zu wählen. Sollte Ihnen also die Bereitstellung der relevantesten und ansprechendsten personalisierten Inhalte über maschinelles Lernen am wichtigsten sein, sollte ein Live-Server-Aufruf durchgeführt werden. Wenn die Leistung jedoch kritischer ist, sollte eine Entscheidung auf dem Gerät und im Speicher getroffen werden. Informationen zur Funktionsfähigkeit der gerätebezogenen Entscheidungsfindung finden Sie in der Liste der unterstützten Funktionen:

* Aktivitätstypen 
* Zielgruppen-Targeting
* Zuordnungsmethode

Weitere Informationen finden Sie unter [Unterstützte Funktionen für geräteübergreifende Entscheidungen](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/).

## Wie funktioniert die Entscheidungsfindung auf dem Gerät?

Wenn Sie at.js mit aktivierter On-Device-Entscheidungsfindung bereitstellen und initialisieren, wird ein [Regelartefakt](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/){target=_blank}, das Ihre on-Device-Entscheidungsfindung für A/B- und XT-Aktivitäten, Zielgruppen und Assets enthält, wird vom nächsten Akamai-CDN zu Ihrem Besucher heruntergeladen und lokal im Browser Ihres Besuchers zwischengespeichert. Wenn von at.js eine Anfrage zum Abrufen eines Erlebnisses gestellt wird, wird die Entscheidung darüber, welches Erlebnis zurückgegeben werden soll, im Arbeitsspeicher getroffen, basierend auf den im zwischengespeicherten Regelartefakt kodierten Metadaten.

## Entscheidungsmethode

Mit gerätebezogenen Entscheidungen [!DNL Target] führt eine neue Einstellung mit dem Namen [!UICONTROL Entscheidungsmethode]. Die [!UICONTROL Entscheidungsmethode] bestimmt, wie at.js Ihre Erlebnisse bereitstellt. [!UICONTROL Entscheidungsmethode] hat drei Werte:

* [!UICONTROL Nur Server-seitig]
* [!UICONTROL Nur auf dem Gerät]
* [!UICONTROL Hybrid]

### Nur Server-seitig

[!UICONTROL Nur Server-seitig] ist die standardmäßige Entscheidungsmethode, die vorkonfiguriert ist, wenn at.js 2.5.0+ implementiert und in Ihren Web-Eigenschaften bereitgestellt wird.

Die Verwendung von [!UICONTROL Nur Server-seitig] als Standardkonfiguration bedeutet, dass alle Entscheidungen im [!DNL Target]-Edge-Netzwerk getroffen werden, was einen blockierenden Server-Aufruf beinhaltet. Dieser Ansatz kann zu einer inkrementellen Latenz führen, bietet aber auch erhebliche Vorteile, z. B. die Möglichkeit, die maschinellen Lernfunktionen von Target anzuwenden, zu denen die Aktivitäten [Recommendations](/help/main/c-recommendations/recommendations.md), [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) und [Automatisches Targeting](/help/main/c-activities/auto-target/auto-target-to-optimize.md) gehören.

Darüber hinaus kann die Erweiterung Ihrer personalisierten Erlebnisse mithilfe des Target-Benutzerprofils, das sitzungs- und kanalübergreifend beibehalten wird, leistungsstarke Ergebnisse für Ihr Unternehmen liefern.

Schließlich erlaubt Ihnen [!UICONTROL Nur Server-seitig], die Adobe Experience Cloud zu verwenden und Zielgruppen anzupassen, die über Audience Manager- und Adobe Analytics-Segmente angesprochen werden können.

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem Adobe Target Edge-Netzwerk. Dieses Flussdiagramm erfasst neue Besucher und wiederkehrende Besucher.

![Nur serverseitiges Flussdiagramm](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

Die folgende Liste entspricht den Zahlen im Diagramm:

| Schritt | Beschreibung |
| --- | --- |
| 1 | Die [!DNL Experience Cloud Visitor ID] wird aus dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>   Die at.js-Bibliothek kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert ist. |
| 3 | Die at.js-Bibliothek blendet den Text aus, um Flackern zu verhindern. |
| 4 | Es wird eine Seitenladeanforderung durchgeführt, die alle konfigurierten Parameter enthält, z. B. (ECID, Kunden-ID, benutzerdefinierte Parameter, Benutzerprofil usw.). |
| 5 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist.<br>Der Profilspeicher ruft geeignete Zielgruppen aus der Zielgruppenbibliothek ab (z. B. über freigegebene Zielgruppen [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]usw.).<br>Kundenattribute werden in einem Batch-Prozess an den Profilspeicher übermittelt. |
| 6 | Der Profilspeicher wird für die Zielgruppenqualifizierung und -zusammenfassung verwendet, um Aktivitäten zu filtern. |
| 7 | Der resultierende Inhalt wird ausgewählt, nachdem das Erlebnis aus der Live-Umgebung ermittelt wurde. [!DNL Target] Aktivitäten. |
| 8 | Die at.js-Bibliothek blendet die entsprechenden Elemente auf der Seite aus, die mit dem Erlebnis verknüpft sind, das gerendert werden muss. |
| 9 | Die at.js-Bibliothek zeigt den Hauptteil an, sodass der Rest der Seite geladen werden kann, damit der Besucher ihn anzeigen kann. |
| 10 | Die at.js-Bibliothek bearbeitet das DOM, um das Erlebnis aus dem Target Edge Network zu rendern. |
| 11 | Das Erlebnis wird für den Besucher gerendert. |
| 12 | Die gesamte Webseite wird geladen. |
| 13 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. |
| 14 | Zielgruppendaten werden mit [!DNL Analytics] Daten über die SDID und werden in der [!DNL Analytics] Berichtspeicher. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

### Nur auf dem Gerät

[!UICONTROL Nur auf dem Gerät] ist die Entscheidungsmethode, die in at.js 2.5.0 oder höher festgelegt werden muss, wenn die Entscheidungsfindung auf dem Gerät nur auf Ihren Web-Seiten verwendet werden soll.

Die Entscheidungsfindung auf dem Gerät kann Ihre Erlebnisse und Personalisierungsaktivitäten schnell bereitstellen, da die Entscheidungen aus einem zwischengespeicherten Regelartefakt getroffen werden, das all Ihre Aktivitäten enthält, die für die Entscheidungsfindung auf dem Gerät qualifiziert sind.

Weitere Informationen dazu, welche Aktivitäten für die Entscheidungsfindung auf dem Gerät qualifiziert sind, finden Sie unter [Unterstützte Funktionen bei Entscheidungen auf Geräten](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/).

Diese Entscheidungsmethode sollte nur verwendet werden, wenn die Leistung auf allen Seiten, für die Entscheidungen von [!DNL Target] erforderlich sind, äußerst kritisch ist. Beachten Sie außerdem, dass bei Auswahl dieser Entscheidungsmethode Ihre [!DNL Target]-Aktivitäten, die nicht für die Entscheidungsfindung auf dem Gerät qualifiziert sind, nicht bereitgestellt bzw. ausgeführt werden. Die Bibliothek at.js 2.5.0+ ist so konfiguriert, dass nur nach dem zwischengespeicherten Regelartefakt gesucht wird, um Entscheidungen zu treffen.

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem Akamai-CDN. Das Akamai-CDN speichert das Regelartefakt für den ersten Besuch des Besuchers zwischen. Beim ersten Seitenbesuch eines neuen Besuchers muss das JSON-Regelartefakt vom Akamai-CDN heruntergeladen werden, damit es lokal im Browser des Besuchers zwischengespeichert werden kann. Nachdem das JSON-Regelartefakt heruntergeladen wurde, wird die Entscheidung sofort ohne blockierenden Netzwerkaufruf getroffen. Das folgende Flussdiagramm erfasst neue Besucher.

![Flussdiagramm nur auf dem Gerät](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

Die folgende Liste entspricht den Zahlen im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteübergreifende Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden kontinuierlich auf Aktualisierungen überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergeleitet wird.

| Schritt | Beschreibung |
| --- | --- |
| 1 | Die [!DNL Experience Cloud Visitor ID] wird aus dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert ist. |
| 3 | Die at.js-Bibliothek blendet den Text aus, um Flackern zu verhindern. |
| 4 | Die at.js-Bibliothek stellt eine Anfrage, das JSON-Regelartefakt vom nächsten Akamai-CDN an den Besucher abzurufen. |
| 5 | Das Akamai-CDN reagiert mit dem JSON-Regelartefakt. |
| 6 | Das JSON-Regelartefakt wird lokal im Browser des Besuchers zwischengespeichert. |
| 7 | Die at.js-Bibliothek interpretiert das JSON-Regelartefakt, führt die Entscheidung zum Abrufen des Erlebnisses aus und blendet die getesteten Elemente aus. |
| 8 | Die at.js-Bibliothek zeigt den Hauptteil an, sodass der Rest der Seite geladen werden kann, damit der Besucher ihn anzeigen kann. |
| 9 | Die at.js-Bibliothek bearbeitet das DOM, um das Erlebnis aus dem zwischengespeicherten JSON-Regelartefakt zu rendern. |
| 10 | Das Erlebnis wird für den Besucher gerendert. |
| 11 | Die gesamte Webseite wird geladen. |
| 12 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zielgruppendaten werden mit [!DNL Analytics] Daten über die SDID und werden in der [!DNL Analytics] Berichtspeicher. [!DNL Analytics][!DNL Analytics]Analytics-Daten können dann sowohl in als auch in eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs for Target (A4T).[!DNL Target] |

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem zwischengespeicherten JSON-Regelartefakt für den nachfolgenden Seitenaufruf oder den wiederkehrenden Besuch des Besuchers. Da das JSON-Regelartefakt bereits zwischengespeichert und im Browser verfügbar ist, wird die Entscheidung sofort ohne blockierenden Netzwerkaufruf getroffen. Dieses Flussdiagramm erfasst nachfolgende Seitennavigation oder wiederkehrende Besucher.

![Flussdiagramm nur auf dem Gerät für nachfolgende Seitennavigation und wiederholte Besuche](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

Die folgende Liste entspricht den Zahlen im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteübergreifende Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden kontinuierlich auf Aktualisierungen überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergeleitet wird.

| Schritt | Beschreibung |
| --- | --- |
| 1 | Die [!DNL Experience Cloud Visitor ID] wird aus dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert ist. |
| 3 | Die at.js-Bibliothek blendet den Text aus, um Flackern zu verhindern. |
| 4 | Die at.js-Bibliothek interpretiert das JSON-Regelartefakt und führt die Entscheidung im Speicher aus, das Erlebnis abzurufen. |
| 5 | Die getesteten Elemente sind ausgeblendet. |
| 6 | Die at.js-Bibliothek zeigt den Hauptteil an, sodass der Rest der Seite geladen werden kann, damit der Besucher ihn anzeigen kann. |
| 7 | Die at.js-Bibliothek bearbeitet das DOM, um das Erlebnis aus dem zwischengespeicherten JSON-Regelartefakt zu rendern. |
| 8 | Das Erlebnis wird für den Besucher gerendert. |
| 9 | Die gesamte Webseite wird geladen. |
| 10 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zielgruppendaten werden mit [!DNL Analytics] Daten über die SDID und werden in der [!DNL Analytics] Berichtspeicher. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

### Hybrid

[!UICONTROL Hybrid] ist die Entscheidungsmethode, die in at.js 2.5.0+ festgelegt werden muss, wenn sowohl Entscheidungen auf dem Gerät als auch Aktivitäten, die einen Netzwerkaufruf an das Adobe Target Edge-Netzwerk erfordern, ausgeführt werden müssen.

Wenn Sie sowohl Entscheidungsaktivitäten auf dem Gerät als auch Server-seitige Aktivitäten verwalten, kann es bei der Bereitstellung von [!DNL Target] auf Ihren Seiten etwas kompliziert und mühsam werden. Bei „Hybrid“ als Entscheidungsmethode weiß [!DNL Target], wann ein Server-Aufruf an das Adobe Target Edge-Netzwerk für Aktivitäten durchgeführt werden muss, für die eine Server-seitige Ausführung erforderlich ist, und wann nur Entscheidungen auf dem Gerät ausgeführt werden sollen.

Das JSON-Regelartefakt enthält Metadaten, die at.js darüber informieren, ob eine Mbox eine Server-seitige Aktivität ausführt oder eine Entscheidungsaktivität auf dem Gerät aufweist. Diese Entscheidungsmethode stellt sicher, dass Aktivitäten, die Sie schnell bereitstellen möchten, über Entscheidungsfindung auf dem Gerät durchgeführt werden und für Aktivitäten, die eine leistungsfähigere ML-gesteuerte Personalisierung erfordern, diese Aktivitäten über das Adobe Target Edge-Netzwerk erfolgen.

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+, dem Akamai CDN und dem Adobe Target Edge Network für einen neuen Besucher, der Ihre Seite zum ersten Mal besucht. Der Nachteil dieses Diagramms besteht darin, dass das JSON-Regelartefakt asynchron heruntergeladen wird, während die Entscheidungen über das Adobe Target Edge-Netzwerk getroffen werden.

Dieser Ansatz stellt sicher, dass die Größe des Artefakts, das viele Aktivitäten umfassen kann, die Latenz der Entscheidung nicht negativ beeinflusst. Das synchrone Herunterladen des JSON-Regelartefakts und die anschließende Entscheidungsfindung können sich ebenfalls nachteilig auf die Latenz auswirken und inkonsistent sein. Daher ist die hybride Entscheidungsmethode eine Best Practice-Empfehlung, immer einen serverseitigen Aufruf für die Entscheidung für einen neuen Besucher durchzuführen, da das JSON-Regelartefakt parallel zwischengespeichert wird. Bei nachfolgenden Seitenbesuchen und erneuten Besuchen werden die Entscheidungen aus dem Cache und im Speicher über das JSON-Regelartefakt getroffen.

![Hybrides Flussdiagramm für einen erstmaligen Besucher](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

Die folgende Liste entspricht den Zahlen im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteübergreifende Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden kontinuierlich auf Aktualisierungen überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergeleitet wird.

| Schritt | Beschreibung |
| --- | --- |
| 1 | Die [!DNL Experience Cloud Visitor ID] wird aus dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert ist. |
| 3 | Die at.js-Bibliothek blendet den Text aus, um Flackern zu verhindern. |
| 4 | Eine Seitenladeanforderung wird an das Adobe Target Edge Network gesendet, einschließlich aller konfigurierten Parameter wie (ECID, Kunden-ID, benutzerdefinierte Parameter, Benutzerprofil usw.). |
| 5 | Parallel dazu sendet at.js eine Anfrage zum Abrufen des JSON-Regel-Artefakts vom nächsten Akamai-CDN an den Besucher. |
| 6 | (Adobe Target Edge Network) Profilskripte werden ausgeführt und dann in den Profilspeicher eingespeist. Der Profilspeicher ruft geeignete Zielgruppen aus der Zielgruppenbibliothek ab (z. B. über freigegebene Zielgruppen [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]usw.). |
| 7 | Das Akamai-CDN reagiert mit dem JSON-Regelartefakt. |
| 8 | Der Profilspeicher wird für die Zielgruppenqualifizierung und -zusammenfassung verwendet, um Aktivitäten zu filtern. |
| 9 | Der resultierende Inhalt wird ausgewählt, nachdem das Erlebnis aus der Live-Umgebung ermittelt wurde. [!DNL Target] Aktivitäten. |
| 10 | Die at.js-Bibliothek blendet die entsprechenden Elemente auf der Seite aus, die mit dem Erlebnis verknüpft sind, das gerendert werden muss. |
| 11 | Die at.js-Bibliothek zeigt den Hauptteil an, sodass der Rest der Seite geladen werden kann, damit der Besucher ihn anzeigen kann. |
| 12 | Die at.js-Bibliothek bearbeitet das DOM, um das Erlebnis aus dem Target Edge Network zu rendern. |
| 13 | Das Erlebnis wird für den Besucher gerendert. |
| 14 | Die gesamte Webseite wird geladen. |
| 15 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zielgruppendaten werden mit [!DNL Analytics] Daten über die SDID und werden in der [!DNL Analytics] Berichtspeicher. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem zwischengespeicherten JSON-Regelartefakt für eine nachfolgende Seitennavigation oder einen wiederkehrenden Besuch. In diesem Diagramm konzentrieren Sie sich nur auf den Anwendungsfall, dass eine geräteübergreifende Entscheidung für die nachfolgende Seitennavigation oder den nachfolgenden wiederkehrenden Besuch getroffen wird. Beachten Sie, dass je nachdem, welche Aktivitäten für bestimmte Seiten live sind, ein Server-seitiger Aufruf durchgeführt werden kann, um serverseitige Entscheidungen auszuführen.

![Hybrides Flussdiagramm für nachfolgende Seitennavigation und wiederholte Besuche](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

Die folgende Liste entspricht den Zahlen im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteübergreifende Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden kontinuierlich auf Aktualisierungen überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergeleitet wird.

| Schritt | Beschreibung |
| --- | --- |
| 1 | Die [!DNL Experience Cloud Visitor ID] wird aus dem [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron mit einem optionalen Pre-hiding-Snippet geladen werden, das auf der Seite implementiert ist. |
| 3 | Die at.js-Bibliothek blendet den Text aus, um Flackern zu verhindern. |
| 4 | Es wird eine Anfrage zum Abrufen eines Erlebnisses gesendet. |
| 5 | Die at.js-Bibliothek bestätigt, dass das JSON-Regelartefakt bereits zwischengespeichert wurde, und führt die Entscheidung im Speicher aus, das Erlebnis abzurufen. |
| 6 | Die getesteten Elemente sind ausgeblendet. |
| 7 | Die at.js-Bibliothek zeigt den Hauptteil an, sodass der Rest der Seite geladen werden kann, damit der Besucher ihn anzeigen kann. |
| 8 | Die at.js-Bibliothek bearbeitet das DOM, um das Erlebnis aus dem zwischengespeicherten JSON-Regelartefakt zu rendern. |
| 9 | Das Erlebnis wird für den Besucher gerendert. |
| 10 | Die gesamte Webseite wird geladen. |
| 11 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zielgruppendaten werden mit [!DNL Analytics] Daten über die SDID und werden in der [!DNL Analytics] Berichtspeicher. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

## Wie aktiviere ich die Entscheidungsfindung auf dem Gerät?

Die Entscheidungsfindung auf dem Gerät ist für alle [!DNL Target] Kunden, die at.js 2.5.0 oder höher verwenden.

So aktivieren Sie die Entscheidungsfindung auf dem Gerät:

>[!NOTE]
>
>Sie müssen über die [!UICONTROL Admin] oder [!UICONTROL Genehmiger] [Benutzerrolle](/help/main/administrating-target/c-user-management/user-management.md) , um den Umschalter On-Device Decisioning zu aktivieren bzw. zu deaktivieren.

1. Klicken **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Kontodetails]**.
1. under **[!UICONTROL Kontodetails]**, schieben Sie die **[!UICONTROL On-Device Decisioning]** Umschalten auf die Position &quot;Ein&quot;.

   ![Umschalten der Entscheidungsfindung auf dem Gerät](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   Die &quot;[!UICONTROL Alle vorhandenen Entscheidungsaktivitäten auf dem Gerät in das Artefakt einschließen]&quot; angezeigt, wenn Sie die Entscheidungsfindung auf dem Gerät aktivieren.
1. (Bedingt) Schalten Sie den Umschalter in die &quot;Ein&quot;-Position, wenn Sie möchten, dass alle Ihre Live-Target-Aktivitäten, die für die Entscheidungsfindung auf dem Gerät geeignet sind, automatisch in das Artefakt einbezogen werden.

   Wenn Sie diesen Umschalter deaktivieren, müssen Sie alle Entscheidungsaktivitäten auf dem Gerät neu erstellen und aktivieren, damit sie in das generierte Regelartefakt aufgenommen werden. Mit anderen Worten: Jede Aktivität im Live-Status, bevor die [!UICONTROL On-Device Decisioning] -Umschalter sind nicht im Regelartefakt enthalten.

Nach der Aktivierung der [!UICONTROL On-Device Decisioning] Umschalten, [!DNL Target] beginnt mit der Erzeugung und Vermehrung [ruleArtefakte](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/){target=_blank} für Ihren Client verwenden.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass Sie den Umschalter aktivieren, bevor Sie das Adobe Target-SDK initialisieren, um die Entscheidungsfindung auf dem Gerät zu verwenden. Die Regelartefakte müssen zuerst generiert und an die Akamai-CDNs übertragen werden, damit die geräteübergreifende Entscheidungsfindung funktioniert. Es kann fünf bis zehn Minuten dauern, bis das erste Regelartefakt generiert und an das Akamai-CDN übertragen wird.

## Wie konfiguriere ich at.js 2.5.0+ für die Verwendung von geräteübergreifenden Entscheidungen?

1. Klicken **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Kontodetails]**.
1. under **[!UICONTROL Implementierungsmethoden]** > **[!UICONTROL Hauptimplementierungsmethode]** klicken **[!UICONTROL Bearbeiten]** neben Ihrer at.js-Version (muss at.js 2.5.0 oder höher sein).

   ![Einstellungen der Hauptimplementierungsmethode bearbeiten](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >Wenden Sie sich vor Änderung dieser Standardeinstellungen an den Kundendienst, damit Sie sich nicht auf Ihre aktuelle Implementierung auswirken.

1. Wählen Sie die gewünschte Entscheidungsmethode aus:

   * [!UICONTROL Nur Server-seitig]
   * [!UICONTROL Nur auf dem Gerät]
   * [!UICONTROL Hybrid]

   ![&quot;at.js&quot;-Einstellungsbedienfeld bearbeiten](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### Globale Einstellungen

Sie können die Standardeinstellung [!UICONTROL Entscheidungsmethode] für alle [!DNL Target] Entscheidungen. Die verschiedenen Entscheidungsmethoden sind [!UICONTROL Nur serverseitig], [!UICONTROL Nur auf Gerät]und [!UICONTROL Hybrid]. Die in der Target-Benutzeroberfläche ausgewählte Entscheidungsmethode wird in `window.targetGlobalSettings` unter `decisioningMethod` -Feld. Weitere Informationen zum `decisioningMethod` in [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

```javascript
<head> 
    <script type="text/javascript">

        window.targetGlobalSettings = { 
            clientCode: "yourClientCodeHere", 
            imsOrgId: "imsOrgId@AdobeOrg", 
            decisioningMethod: "on-device"

        }; 
    </script>

    <script type="text/javascript" src="at.js"></script> 
</head>
```

### Benutzerdefinierte Einstellung

Wenn Sie `decisioningMethod` in `window.targetGlobalSettings`, aber die `decisioningMethod` Für jede Adobe Target-Entscheidung entsprechend Ihrem Anwendungsfall können Sie dieses Verfahren durchführen, indem Sie `decisioningMethod` in at.js2.5.0+ [getOffers()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/){target=_blank}-Aufruf.

```javascript
adobe.target.getOffers({ 

  decisioningMethod:"on-device", 
  request: { 
    execute: { 
      mboxes: [ 
        { 
          index: 0, 
          name: "homepage" 
        } 
      ] 
    } 
 } 
});
```

>[!NOTE]
>
>Um &quot;on-device&quot;oder &quot;hybrid&quot;als Entscheidungsmethode im getOffers()-Aufruf zu verwenden, stellen Sie sicher, dass die globale Einstellung `decisioningMethod` als &quot;auf dem Gerät&quot;oder &quot;Hybrid&quot;. Die Bibliothek at.js 2.5.0+ muss wissen, ob das JSON-Regelartefakt unmittelbar nach dem Laden auf der Seite heruntergeladen und zwischengespeichert werden soll. Wenn die Entscheidungsmethode für die globale Einstellung auf &quot;Server-seitig&quot;festgelegt ist und die Entscheidungsmethode &quot;auf dem Gerät&quot;oder &quot;Hybrid&quot;an den getOffers()-Aufruf übergeben wird, wird für at.js 2.5.0+ das JSON-Regelartefakt nicht zwischengespeichert, um Ihre Entscheidungen auf dem Gerät auszuführen.

### Artifact Cache TTL

[!DNL Target] stellt Ihre Aktivitäten dar, die sich für die Entscheidungsfindung auf dem Gerät als ein Artefakt qualifizieren, das aus Metadaten, Regeln und Bedingungen besteht. Dieses Artefakt wird im Akamai-CDN zwischengespeichert. Während des ersten Besuchs Ihres Benutzers lädt der Browser des Benutzers das Artefakt herunter und speichert es zwischen, das Ihre Entscheidungsaktivitäten auf dem Gerät darstellt.

Bei nachfolgenden Besuchen Ihrer Site prüft der Browser automatisch, ob eine neuere Version des Artefakts heruntergeladen werden muss. Durch diese Prüfung wird Latenz hinzugefügt. Die Artefakt-Cache-TTL definiert die Anzahl der Minuten, die der Browser seit dem letzten erfolgreichen Download nicht auf ein aktualisiertes Artefakt überprüfen soll. Je länger der Zeitrahmen, desto besser die Leistung. Je kürzer der Zeitrahmen ist, desto besser ist die Aktualisierung der Daten, jedoch auf Kosten zusätzlicher Latenz.

## Woher weiß ich, dass eine Aktivität für die Entscheidungsfindung auf dem Gerät geeignet ist?

Nachdem Sie eine Aktivität erstellt haben, die für eine Entscheidung auf dem Gerät infrage kommt, wird eine Beschriftung angezeigt, die [!UICONTROL Eignung für On-Device Decisioning], ist in der Aktivität [!UICONTROL Übersicht] Seite.

![Bezeichnung der für eine Entscheidung in Frage kommenden On-Device auf der Übersichtsseite der Aktivität.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

Diese Bezeichnung bedeutet nicht, dass die Aktivität immer über On-Device-Entscheidungen bereitgestellt wird. Nur wenn at.js 2.5.0 oder höher für die Verwendung von gerätebezogenen Entscheidungen konfiguriert ist, wird diese Aktivität auf dem Gerät ausgeführt. Wenn at.js 2.5.0 oder höher nicht für die Verwendung auf dem Gerät konfiguriert ist, wird diese Aktivität weiterhin über einen Server-Aufruf von at.js bereitgestellt.

Sie können nach allen Aktivitäten filtern, die für eine Entscheidung auf dem Gerät infrage kommen. [!UICONTROL Tätigkeiten] über die Seite [!UICONTROL Eignung für On-Device Decisioning] Filter.

![Auf der Seite &quot;Aktivitäten&quot;angezeigte Filter für die Entscheidungsfindung auf dem Gerät.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>Nachdem Sie eine Aktivität erstellt und aktiviert haben, für die eine Entscheidung auf dem Gerät möglich ist, kann es fünf bis zehn Minuten dauern, bis sie im Regelartefakt enthalten ist, das generiert und an den Akamai CDN-Punkt der Präferenzen weitergeleitet wird.

## Zusammenfassung der Schritte, die sicherstellen, dass meine on-device-Entscheidungsaktivitäten über at.js 2.5.0+ bereitgestellt werden?

1. Rufen Sie die Adobe Target-Benutzeroberfläche auf und navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!DNL Account Details]** um die **[!UICONTROL On-Device Decisioning]** umschalten.
1. Aktivieren Sie die **&quot;[!UICONTROL Alle vorhandenen Entscheidungsaktivitäten auf dem Gerät in das Artefakt einschließen]&quot;** umschalten.

   Die erste Generierung von JSON-Regeln-Artefakten kann bis zu 10 Minuten dauern.

1. Erstellen und Aktivieren einer [Aktivitätstyp, der von geräteinterner Entscheidungsfindung unterstützt wird](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/)und stellen Sie sicher, dass die Entscheidung auf dem Gerät getroffen werden kann.
1. Legen Sie die **[!UICONTROL Entscheidungsmethode]** entweder **[!UICONTROL &quot;Hybrid&quot;]** oder **[!UICONTROL &quot;Nur auf Gerät&quot;]** über die Benutzeroberfläche für at.js-Einstellungen.
1. Laden Sie at.js 2.5.0+ herunter und stellen Sie es auf Ihren Seiten bereit.
