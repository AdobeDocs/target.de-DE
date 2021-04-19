---
keywords: Implementierung;JavaScript-Bibliothek;js;ATJS;on-device-Entscheidungsfindung;on-device-Entscheidungsfindung;at.js;on-device;on-device
description: Erfahren Sie, wie Sie mit der Bibliothek "at.js"Entscheidungen auf dem Gerät durchführen
title: Wie funktioniert die On-device-Entscheidungsfindung mit der JavaScript-Bibliothek "at.js"?
feature: 'at.js '
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '3506'
ht-degree: 7%

---

# Geräteinterne Entscheidungsfindung für &quot;at.js&quot;

>[!NOTE]
>
>Die Entscheidung für das On-Device-System steht mit dem kommenden [at.js 2.5.0 Release](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) zur Verfügung. Datum wird bald bekannt gegeben.

Ab Version 2.5.0 gilt für at.js-Angebot die Geräteentscheidung. Mit der On-Device-Entscheidungsfindung können Sie Ihre [A/B-Aktivitäten](/help/c-activities/t-test-ab/test-ab.md) und [Erlebnis-Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT) im Browser zwischenspeichern, um eine speicherinterne Entscheidungsfindung ohne blockierende Netzwerkanforderung für das [!DNL Adobe Target] Edge-Netzwerk durchzuführen.

[!DNL Target] Darüber hinaus wird die Flexibilität bei der Bereitstellung der relevantesten und aktuellsten Erfahrung durch Ihre experimentelle und maschinelle Lernfunktionen (ML-gesteuerte) Personalisierungs-Aktivitäten über einen Live-Server-Aufruf Angebot. Mit anderen Worten, wenn die Leistung am wichtigsten ist, können Sie die Entscheidungsfindung auf dem Gerät verwenden. Wenn jedoch das relevanteste, aktuellste und ML-gesteuerte Erlebnis benötigt wird, kann stattdessen ein Server-Aufruf durchgeführt werden.

## Welche Vorteile bietet die Entscheidungsfindung auf dem Gerät?

Die Vorteile der Entscheidung über das Gerät sind unter anderem:

* **Schnelle Entscheidungen und Erlebnisse liefern.** Die Sicherung und Entscheidungsfindung erfolgt im Arbeitsspeicher und im Browser, um eine Blockierung von Netzwerkanforderungen zu vermeiden.
* **Verbessern Sie die Anwendungsleistung.** Führen Sie Experimente durch und liefern Sie Ihren Kunden und Benutzern Personalisierung, ohne dass die Benutzererfahrung beeinträchtigt wird.
* **Verbessern Sie die Google Site-Qualitätsbewertung.** Verbessern Sie die Google Site-Qualitätsbewertung Ihres Onlinegeschäftes, da Entscheidungen im Arbeitsspeicher stattfinden, um sie für die Verbraucher leichter zu entdecken.
* **Erfahren Sie mehr über Echtzeitanalysen.** Erhalten Sie Einblicke in die Performance Ihrer Aktivität in Echtzeit über den Berichte  [Analytics for Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Mit A4T können Sie Ihre Strategie in kritischen Momenten umdrehen.

## Unterstützte Funktionen 

Das Adobe Target JS SDK bietet Kunden die Flexibilität, zwischen Leistung und Frische von Daten für Entscheidungen zu wählen. Mit anderen Worten: Wenn die Bereitstellung der relevantesten und interessantesten personalisierten Inhalte über maschinelles Lernen für Sie von größter Bedeutung ist, sollte ein Live-Server-Aufruf durchgeführt werden. Wenn die Leistung jedoch kritischer ist, sollte eine Entscheidung über ein Gerät und einen Speicher getroffen werden. Informationen zur Funktionsfähigkeit der Geräteentscheidung finden Sie in der Liste der unterstützten Funktionen:

* Aktivitätstypen 
* Audience-Targeting
* Zuordnungsmethode

Weitere Informationen finden Sie unter [Unterstützte Funktionen für Entscheidungen auf dem Gerät](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md).

## Wie funktioniert die Entscheidungsfindung auf dem Gerät?

Wenn Sie at.js mit aktivierter on-device-Entscheidungsfunktion bereitstellen und initialisieren, wird ein [rule artifact](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md), das Ihre geräteinterne Entscheidungsfindung für A/B- und XT-Aktivitäten, -Audiencen und -Assets enthält, vom nächsten Akamai-CDN auf Ihren Besucher heruntergeladen und lokal im Browser Ihres Besuchers zwischengespeichert. Wenn von at.js eine Anforderung zum Abrufen eines Erlebnisses gesendet wird, erfolgt die Entscheidung, welches Erlebnis im Arbeitsspeicher zurückgegeben werden soll, basierend auf den im zwischengespeicherten Regelartefakt kodierten Metadaten.

## Entscheidungsmethode

Bei der Entscheidung über das Gerät führt [!DNL Target] eine neue Einstellung mit dem Namen [!UICONTROL Entscheidungsmethode] ein. Die Einstellung [!UICONTROL Entscheidungsmethode] gibt an, wie at.js Ihre Erlebnisse bereitstellt. [!UICONTROL Die ] Entscheidungsmethode hat drei Werte:

* [!UICONTROL Nur serverseitig]
* [!UICONTROL Nur auf dem Gerät]
* [!UICONTROL Hybrid]

### Nur serverseitig

[!UICONTROL Nur serverseitig ] ist die standardmäßige Entscheidungsmethode, die standardmäßig eingestellt wird, wenn at.js 2.5.0+ in Ihren Webeigenschaften implementiert und bereitgestellt wird.

Die Verwendung von [!UICONTROL Nur serverseitig] als Standardkonfiguration bedeutet, dass alle Entscheidungen im [!DNL Target]-Edge-Netzwerk getroffen werden, was einen blockierenden Server-Aufruf umfasst. Dieser Ansatz kann inkrementelle Latenzzeiten einführen, bietet aber auch erhebliche Vorteile, z. B. die Möglichkeit, die maschinellen Lernfunktionen der Zielgruppe anzuwenden, zu denen die Aktivitäten [Recommendations](/help/c-recommendations/recommendations.md), [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) und [Auto-Zielgruppe](/help/c-activities/auto-target/auto-target-to-optimize.md) gehören.

Darüber hinaus kann die Verbesserung Ihrer personalisierten Erlebnisse durch Verwendung des Benutzerprofils der Zielgruppe, das sitzungs- und Kanal-übergreifend beibehalten wird, leistungsstarke Ergebnisse für Ihr Unternehmen liefern.

Und schließlich können Sie mit [!UICONTROL Nur serverseitig] die Adobe Experience Cloud-Audiencen und Feinabstimmungen verwenden, die über Audience Manager- und Adobe Analytics-Segmente zielgerichtet bearbeitet werden können.

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem Adobe Target Edge-Netzwerk. Dieses Flussdiagramm erfasst neue Besucher und wiederkehrende Besucher.

![Nur serverseitiges Flussdiagramm](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

Die folgende Liste entspricht den Nummern im Diagramm:

| Schritt | Beschreibung |
| --- | --- |
| 1 | Das [!DNL Experience Cloud Visitor ID] wird vom [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) abgerufen. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>   Die at.js-Bibliothek kann auch asynchron geladen werden, wobei ein optionales, auf der Seite implementiertes Snippet zum Vorausblenden von Elementen implementiert ist. |
| 3 | Die Bibliothek at.js blendet den Körper aus, um Flackern zu vermeiden. |
| 4 | Es wird eine Seitenladeanforderung durchgeführt, die alle konfigurierten Parameter enthält, z. B. (ECID, Kunden-ID, benutzerdefinierte Profil, Benutzerparameter usw.) |
| 5 | Profilskripte werden ausgeführt und anschließend in den Profilspeicher eingespeist.<br>Der Profil Store fordert qualifizierte Audiencen aus der Audience-Bibliothek an (z. B. freigegebene Audiencen  [!DNL Adobe Analytics],  [!DNL Adobe Audience Manager]usw.).<br>Kundenattribute werden in einem Batch-Prozess an den Profilspeicher übermittelt. |
| 6 | Der Profil Store dient zum Filtern von Aktivitäten für die Qualifizierung und das Bucketing von Audiencen. |
| 7 | Der resultierende Inhalt wird ausgewählt, nachdem das Erlebnis anhand der Live-Aktivitäten [!DNL Target] ermittelt wurde. |
| 8 | Die Bibliothek at.js blendet die entsprechenden Elemente auf der Seite aus, die mit dem Erlebnis verknüpft sind, das gerendert werden muss. |
| 9 | In der &quot;at.js&quot;-Bibliothek wird der Hauptteil angezeigt, damit der Rest der Seite für die Ansicht des Besuchers geladen werden kann. |
| 10 | Die at.js-Bibliothek manipuliert das DOM, um das Erlebnis über das Edge-Netzwerk der Zielgruppe wiederzugeben. |
| 11 | Das Erlebnis wird für den Besucher gerendert. |
| 12 | Die gesamte Webseite wird geladen. |
| 13 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. |
| 14 | Zieldaten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und in die [!DNL Analytics]-Berichte-Datenspeicherung verarbeitet. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

### Nur auf dem Gerät

[!UICONTROL &quot;Nur auf dem Gerät&quot;ist ] die Entscheidungsmethode, die in at.js 2.5.0 und höher festgelegt werden muss, wenn die Entscheidung auf dem Gerät nur auf allen Webseiten verwendet werden soll.

Die Geräteinterne Entscheidungsfindung kann Ihre Erlebnisse und Personalisierungs-Aktivitäten schnell bereitstellen, da die Entscheidungen anhand eines zwischengespeicherten Regelartikels getroffen werden, das alle Ihre Aktivitäten enthält, die für eine Geräteentscheidung infrage kommen.

Weitere Informationen darüber, welche Aktivitäten für die Entscheidungsfindung auf dem Gerät infrage kommen, finden Sie unter [Unterstützte Funktionen bei der Geräteentscheidung](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md).

Diese Entscheidungsmethode sollte nur verwendet werden, wenn die Leistung auf allen Seiten, für die Entscheidungen von [!DNL Target] erforderlich sind, äußerst kritisch ist. Beachten Sie außerdem, dass bei Auswahl dieser Entscheidungsmethode Ihre [!DNL Target]-Aktivitäten, die nicht für eine geräteinterne Entscheidungsfindung infrage kommen, nicht bereitgestellt oder ausgeführt werden. Die Bibliothek &quot;at.js&quot;2.5.0+ ist so konfiguriert, dass nur nach dem zwischengespeicherten Artefakt für Regeln gesucht wird, um Entscheidungen zu treffen.

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser &quot;at.js 2.5.0+&quot;und dem Akamai-CDN. Das Akamai-CDN speichert das Regelartefakt für den ersten Besuch des Besuchers zwischen. Beim ersten Seitenbesuch für einen neuen Besucher muss das JSON-Regelartefakt aus dem Akamai-CDN heruntergeladen werden, um lokal im Browser des Besuchers zwischengespeichert zu werden. Nachdem das Artefakt der JSON-Regeln heruntergeladen wurde, wird die Entscheidung sofort ohne blockierenden Netzwerkaufruf getroffen. Das folgende Flussdiagramm erfasst neue Besucher.

![Nur-Gerät-Flussdiagramm](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

Die folgende Liste entspricht den Nummern im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteinterne Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden fortlaufend auf Updates überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergegeben wird.

| Schritt | Beschreibung |
| --- | --- |
| 1 | Das [!DNL Experience Cloud Visitor ID] wird vom [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) abgerufen. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron geladen werden, wobei ein optionales, auf der Seite implementiertes Snippet zum Vorausblenden von Elementen implementiert ist. |
| 3 | Die Bibliothek at.js blendet den Körper aus, um Flackern zu vermeiden. |
| 4 | Die at.js-Bibliothek stellt eine Anforderung zum Abrufen des JSON-Regelartefakts vom nächsten Akamai-CDN zum Besucher. |
| 5 | Das Akamai-CDN reagiert mit dem JSON-Regelartefakt. |
| 6 | Das JSON-Regelartefakt wird lokal im Browser des Besuchers zwischengespeichert. |
| 7 | Die Bibliothek at.js interpretiert das JSON-Regelartefakt und führt die Entscheidung zum Abrufen des Erlebnisses aus und blendet die getesteten Elemente aus. |
| 8 | In der &quot;at.js&quot;-Bibliothek wird der Hauptteil angezeigt, damit der Rest der Seite für die Ansicht des Besuchers geladen werden kann. |
| 9 | Die at.js-Bibliothek manipuliert das DOM, um das Erlebnis aus dem zwischengespeicherten JSON-Regelartefakt wiederzugeben. |
| 10 | Das Erlebnis wird für den Besucher gerendert. |
| 11 | Die gesamte Webseite wird geladen. |
| 12 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zieldaten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und in die [!DNL Analytics]-Berichte-Datenspeicherung verarbeitet. [!DNL Analytics][!DNL Analytics]Analytics-Daten können dann sowohl in als auch in eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs for Target (A4T).[!DNL Target] |

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem zwischengespeicherten JSON-Regelartefakt für den nachfolgenden Seitenaufruf oder den wiederkehrenden Besuch des Besuchers. Da das Artefakt der JSON-Regeln bereits im Cache gespeichert und im Browser verfügbar ist, wird die Entscheidung sofort ohne einen blockierenden Netzwerkaufruf getroffen. Dieses Flussdiagramm erfasst nachfolgende Seitennavigation oder rückkehrende Besucher.

![Nur-Gerät-Flussdiagramm für die anschließende Seitennavigation und wiederholte Besuche](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

Die folgende Liste entspricht den Nummern im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteinterne Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden fortlaufend auf Updates überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergegeben wird.

| Schritt | Beschreibung |
| --- | --- |
| 3 | Das [!DNL Experience Cloud Visitor ID] wird vom [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) abgerufen. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron geladen werden, wobei ein optionales, auf der Seite implementiertes Snippet zum Vorausblenden von Elementen implementiert ist. |
| 1 | Die Bibliothek at.js blendet den Körper aus, um Flackern zu vermeiden. |
| 4 | Die Bibliothek at.js interpretiert das JSON-Regelartefakt und führt die Entscheidung im Speicher aus, das Erlebnis abzurufen. |
| 5 | Die getesteten Elemente werden ausgeblendet. |
| 6 | In der &quot;at.js&quot;-Bibliothek wird der Hauptteil angezeigt, damit der Rest der Seite für die Ansicht des Besuchers geladen werden kann. |
| 7 | Die at.js-Bibliothek manipuliert das DOM, um das Erlebnis aus dem zwischengespeicherten JSON-Regelartefakt wiederzugeben. |
| 8 | Das Erlebnis wird für den Besucher gerendert. |
| 9 | Die gesamte Webseite wird geladen. |
| 10 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zieldaten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und in die [!DNL Analytics]-Berichte-Datenspeicherung verarbeitet. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

### Hybrid

[!UICONTROL Bei ] Hybridis handelt es sich um die Entscheidungsmethode, die in at.js 2.5.0+ festgelegt werden muss, wenn sowohl Entscheidungen auf dem Gerät als auch Aktivitäten, die einen Netzwerkaufruf an das Adobe Target Edge-Netzwerk erfordern, ausgeführt werden müssen.

Wenn Sie sowohl Aktivitäten für die Entscheidungsfindung auf dem Gerät als auch serverseitige Aktivitäten verwalten, kann es etwas kompliziert und mühsam sein, wenn Sie darüber nachdenken, wie [!DNL Target] auf Ihren Seiten bereitgestellt und bereitgestellt werden soll. Bei Verwendung von Hybrid als Entscheidungsmethode weiß [!DNL Target], wann ein Serveraufruf an das Adobe Target Edge-Netzwerk für Aktivitäten erfolgen muss, die eine serverseitige Ausführung erfordern, und wann nur Entscheidungen auf dem Gerät ausgeführt werden sollen.

Das JSON-Regelartefakt enthält Metadaten, um at.js darüber zu informieren, ob eine mbox eine serverseitige Aktivität oder eine on-device-Aktivität zur Entscheidungsfindung besitzt. Mit dieser Entscheidungsmethode wird sichergestellt, dass Aktivitäten, die Sie schnell bereitstellen möchten, über die Entscheidungsfindung auf dem Gerät ausgeführt werden. Bei Aktivitäten, die eine leistungsfähigere, von ML ausgehende Personalisierung erfordern, erfolgt diese Aktivität über das Adobe Target Edge-Netzwerk.

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+, dem Akamai-CDN und dem Adobe Target Edge-Netzwerk für einen neuen Besucher, der Ihre Seite zum ersten Mal besucht. Der Nachteil dieses Diagramms ist, dass das JSON-Regelartefakt asynchron heruntergeladen wird, während die Entscheidungen über das Adobe Target Edge-Netzwerk getroffen werden.

Dieser Ansatz gewährleistet, dass die Größe des Artefakts, das viele Aktivitäten umfassen kann, die Latenz der Entscheidung nicht negativ beeinflusst. Das synchrone Herunterladen der JSON-Regeln und anschließende Entscheidungsfindung können sich auch negativ auf die Latenz auswirken und inkonsistent sein. Daher ist die Hybrid-Entscheidungsmethode eine Best Practice-Empfehlung, immer einen serverseitigen Aufruf für die Entscheidung für einen neuen Besucher durchzuführen, und da das Artefakt der JSON-Regeln parallel zwischengespeichert wird. Bei nachfolgenden Seitenbesuchen und wiederkehrenden Besuchen werden die Entscheidungen aus dem Cache und im Arbeitsspeicher durch das Artefakt der JSON-Regeln getroffen.

![Hybrid-Flussdiagramm für einen erstmaligen Besucher](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

Die folgende Liste entspricht den Nummern im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteinterne Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden fortlaufend auf Updates überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergegeben wird.

| Schritt | Beschreibung |
| --- | --- |
| 3 | Das [!DNL Experience Cloud Visitor ID] wird vom [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) abgerufen. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron geladen werden, wobei ein optionales, auf der Seite implementiertes Snippet zum Vorausblenden von Elementen implementiert ist. |
| 3 | Die Bibliothek at.js blendet den Körper aus, um Flackern zu vermeiden. |
| 4 | Eine Seitenladeanforderung wird an das Adobe Target Edge Network gesendet, einschließlich aller konfigurierten Parameter wie (ECID, Kunden-ID, benutzerdefinierte Parameter, User Profil usw.). |
| 5 | Parallel dazu stellt at.js eine Anforderung zum Abrufen des JSON-Regelartefakts vom nächsten Akamai-CDN zum Besucher. |
| 6 | (Adobe Target Edge Network) Profil-Skripten werden ausgeführt und dann in den Profil Store eingespeist. Der Profil Store fordert qualifizierte Audiencen aus der Audience-Bibliothek an (z. B. freigegebene Audiencen von [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] usw.). |
| 7 | Das Akamai-CDN reagiert mit dem JSON-Regelartefakt. |
| 8 | Der Profil Store dient zum Filtern von Aktivitäten für die Qualifizierung und das Bucketing von Audiencen. |
| 9 | Der resultierende Inhalt wird ausgewählt, nachdem das Erlebnis anhand der Live-Aktivitäten [!DNL Target] ermittelt wurde. |
| 10 | Die Bibliothek at.js blendet die entsprechenden Elemente auf der Seite aus, die mit dem Erlebnis verknüpft sind, das gerendert werden muss. |
| 11 | In der &quot;at.js&quot;-Bibliothek wird der Hauptteil angezeigt, damit der Rest der Seite für die Ansicht des Besuchers geladen werden kann. |
| 12 | Die at.js-Bibliothek manipuliert das DOM, um das Erlebnis über das Edge-Netzwerk der Zielgruppe wiederzugeben. |
| 13 | Das Erlebnis wird für den Besucher gerendert. |
| 14 | Die gesamte Webseite wird geladen. |
| 15 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zieldaten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und in die [!DNL Analytics]-Berichte-Datenspeicherung verarbeitet. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

Das folgende Diagramm zeigt die Interaktion zwischen Ihrem Besucher, dem Browser, at.js 2.5.0+ und dem zwischengespeicherten JSON-Regelartefakt für eine anschließende Seitennavigation oder einen wiederkehrenden Besuch. In diesem Diagramm sollten Sie sich nur auf den Anwendungsfall konzentrieren, bei dem eine Geräteentscheidung für die anschließende Seitennavigation oder den anschließenden Besuch getroffen wird. Beachten Sie, dass je nachdem, welche Aktivitäten für bestimmte Seiten live sind, ein serverseitiger Aufruf zum Ausführen serverseitiger Entscheidungen durchgeführt werden kann.

![Hybrid-Flussdiagramm für nachfolgende Seitennavigation und wiederholte Besuche](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

Die folgende Liste entspricht den Nummern im Diagramm:

>[!NOTE]
>
>[!DNL Adobe Target] Admin-Server qualifizieren alle Aktivitäten, die für eine geräteinterne Entscheidungsfindung infrage kommen, generieren das JSON-Regelartefakt und übertragen es an das Akamai-CDN. Ihre Aktivitäten werden fortlaufend auf Updates überwacht, um ein neues JSON-Regelartefakt auszugeben, das an das Akamai-CDN weitergegeben wird.

| Schritt | Beschreibung |
| --- | --- |
| 1 | Das [!DNL Experience Cloud Visitor ID] wird vom [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) abgerufen. |
| 2 | Die Bibliothek at.js wird synchron geladen und im Dokumentenkörper verborgen.<br>Die at.js-Bibliothek kann auch asynchron geladen werden, wobei ein optionales, auf der Seite implementiertes Snippet zum Vorausblenden von Elementen implementiert ist. |
| 3 | Die Bibliothek at.js blendet den Körper aus, um Flackern zu vermeiden. |
| 4 | Es wird eine Anforderung zum Abrufen eines Erlebnisses gesendet. |
| 5 | Die Bibliothek at.js bestätigt, dass das JSON-Regelartefakt bereits zwischengespeichert wurde, und führt die Entscheidung im Speicher aus, das Erlebnis abzurufen. |
| 6 | Die getesteten Elemente werden ausgeblendet. |
| 7 | In der &quot;at.js&quot;-Bibliothek wird der Hauptteil angezeigt, damit der Rest der Seite für die Ansicht des Besuchers geladen werden kann. |
| 8 | Die at.js-Bibliothek manipuliert das DOM, um das Erlebnis aus dem zwischengespeicherten JSON-Regelartefakt wiederzugeben. |
| 9 | Das Erlebnis wird für den Besucher gerendert. |
| 10 | Die gesamte Webseite wird geladen. |
| 11 | [!DNL Analytics]-Daten werden an Datenerfassungsserver übermittelt. Zieldaten werden über die SDID mit [!DNL Analytics]-Daten abgeglichen und in die [!DNL Analytics]-Berichte-Datenspeicherung verarbeitet. [!DNL Analytics]-Daten können dann sowohl in [!DNL Analytics] als auch in [!DNL Target] eingesehen werden. Möglich ist dies mithilfe von Berichten des Typs [!UICONTROL Analytics for Target] (A4T). |

## Wie aktiviere ich die Entscheidungsfindung auf dem Gerät?

Für alle [!DNL Target]-Kunden, die at.js 2.5.0+ verwenden, ist eine geräteinterne Entscheidungsfindung verfügbar.

So aktivieren Sie die Entscheidung auf dem Gerät:

>[!NOTE]
>
>Sie müssen über die [!UICONTROL Admin] oder [!UICONTROL Genehmigende ] [Benutzerrolle](/help/administrating-target/c-user-management/user-management.md) verfügen, um den Umschalter für die Geräteentscheidung zu aktivieren oder zu deaktivieren.

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Kontodetails]**.
1. Schieben Sie unter **[!UICONTROL Kontodetails]** den Umschalter **[!UICONTROL Geräteinterne Entscheidungsfindung]** zur &quot;on&quot;-Position.

   ![Umschalter für die Entscheidungsfindung auf dem Gerät](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   Die Option &quot;[!UICONTROL Alle vorhandenen qualifizierten Aktivitäten auf dem Gerät in Artefakt] einschließen&quot;wird angezeigt, wenn Sie die Geräteentscheidung aktivieren.
1. (Bedingt) Schieben Sie den Umschalter an die &quot;An&quot;-Position, wenn alle Live-Zielgruppen, die für eine Geräteentscheidung infrage kommen, automatisch in das Artefakt aufgenommen werden sollen.

   Wenn Sie diesen Umschalter deaktivieren, müssen Sie alle Entscheidungsfunktionen auf dem Gerät neu erstellen und aktivieren, damit sie in das Artefakt der generierten Aktivitäten aufgenommen werden. Mit anderen Worten, Aktivitäten, die sich im Livemodus befinden, bevor der Umschalter [!UICONTROL Gerätekonfiguration] aktiviert wird, sind nicht im Artefakt der Regeln enthalten.

Nachdem Sie den Umschalter [!UICONTROL Geräteinterne Entscheidungsfindung] aktiviert haben, beginnt [!DNL Target], [Regelartefakte](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md) für Ihren Client zu generieren und zu propagieren.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass Sie den Umschalter aktivieren, bevor Sie das Adobe Target SDK initialisieren, um die Entscheidung auf dem Gerät zu verwenden. Die Artefakte der Regel müssen zuerst generiert und an die Akamai-CDNs weitergegeben werden, damit die Entscheidung über das Gerät funktioniert. Die Propagierung kann fünf bis zehn Minuten dauern, bis das erste Regelartefakt generiert und an das Akamai-CDN übertragen wird.

## Wie konfiguriere ich at.js 2.5.0+ für die Verwendung von Entscheidungen auf dem Gerät?

1. Klicken Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!UICONTROL Kontodetails]**.
1. Klicken Sie unter **[!UICONTROL Implementierungsmethoden]** > **[!UICONTROL Hauptimplementierungsmethode]** auf **[!UICONTROL Bearbeiten]** neben Ihrer at.js-Version (muss at.js 2.5.0 oder höher sein).

   ![Einstellungen der Hauptimplementierungsmethode bearbeiten](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >Wenden Sie sich vor dem Ändern dieser Standardeinstellungen an den Kundendienst, damit Sie keine Auswirkungen auf Ihre aktuelle Implementierung haben.

1. Wählen Sie die gewünschte Entscheidungsmethode aus:

   * [!UICONTROL Nur serverseitig]
   * [!UICONTROL Nur auf dem Gerät]
   * [!UICONTROL Hybrid]

   ![&quot;at.js&quot;-Einstellungsbedienfeld bearbeiten](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### Globale Einstellungen

Sie können eine standardmäßige [!UICONTROL Entscheidungsmethode] für alle [!DNL Target]-Entscheidungen konfigurieren. Die verschiedenen Entscheidungsmethoden sind [!UICONTROL Nur serverseitig], [!UICONTROL Nur auf dem Gerät] und [!UICONTROL Hybrid]. Die in der Benutzeroberfläche der Zielgruppe ausgewählte Entscheidungsmethode wird unter `window.targetGlobalSettings` unter dem Feld `decisioningMethod` konfiguriert. Weitere Informationen zu `decisioningMethod` in [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

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

Wenn Sie `decisioningMethod` in `window.targetGlobalSettings` festlegen, aber `decisioningMethod` für jede Adobe Target-Entscheidung entsprechend Ihrem Verwendungsfall überschreiben möchten, können Sie dieses Verfahren durchführen, indem Sie `decisioningMethod` im Aufruf von at.js2.5.0+ [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) angeben.

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
>Um &quot;auf dem Gerät&quot;oder &quot;Hybrid&quot;als Entscheidungsmethode im getOffers()-Aufruf zu verwenden, stellen Sie sicher, dass die globale Einstellung `decisioningMethod` als &quot;auf dem Gerät&quot;oder &quot;Hybrid&quot;hat. Die Bibliothek at.js 2.5.0+ muss wissen, ob das Artefakt der JSON-Regeln unmittelbar nach dem Laden auf der Seite heruntergeladen und zwischengespeichert werden soll. Wenn die Entscheidungsmethode für die globale Einstellung auf &quot;serverseitig&quot;festgelegt ist und die Entscheidungsmethode &quot;auf dem Gerät&quot;oder &quot;hybrid&quot;an den getOffers()-Aufruf übergeben wird, wird für at.js 2.5.0+ das Artefakt der JSON-Regel nicht zwischengespeichert, um Ihre Entscheidungen auf dem Gerät auszuführen.

### Artefaktcache TTL

[!DNL Target] stellt Ihre Aktivitäten dar, die für die Entscheidung auf dem Gerät als Artefakt qualifiziert sind, das aus Metadaten, Regeln und Bedingungen besteht. Dieses Artefakt wird im Akamai CDN zwischengespeichert. Während des ersten Besuchs Ihres Benutzers lädt der Browser des Benutzers das Artefakt herunter und speichert es zwischen, das Ihre Aktivitäten zur Gerätebestimmung darstellt.

Bei nachfolgenden Besuchen auf Ihrer Site prüft der Browser automatisch, ob eine neuere Version des Artefakts heruntergeladen werden muss. Diese Prüfung erhöht die Latenz. Die TTL des Artefakt-Cache definiert die Anzahl der Minuten, die der Browser seit dem letzten erfolgreichen Download nicht auf ein aktualisiertes Artefakt überprüfen soll. Je länger der Zeitraum, desto besser die Leistung. Je kürzer der Zeitraum, desto besser die Daten frisch, aber um den Preis einer zusätzlichen Latenz.

## Woher weiß ich, dass eine Aktivität für die Entscheidungsfindung auf dem Gerät infrage kommt?

Nachdem Sie eine Aktivität erstellt haben, für die eine Entscheidung auf dem Gerät zulässig ist, wird auf der Seite [!UICONTROL Übersicht] eine Beschriftung mit dem Wortlaut [!UICONTROL Für eine gerätegebundene Entscheidungsfindung ] angezeigt.

![Beschriftung für die Entscheidungsfindung auf dem Gerät auf der Übersichtsseite der Aktivität.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

Diese Bezeichnung bedeutet nicht, dass die Aktivität immer über die Geräteentscheidung bereitgestellt wird. Diese Aktivität wird nur dann auf dem Gerät ausgeführt, wenn at.js 2.5.0+ für die Verwendung von Entscheidungen auf dem Gerät konfiguriert ist. Wenn at.js 2.5.0+ nicht für die Verwendung auf dem Gerät konfiguriert ist, wird diese Aktivität weiterhin über einen Server-Aufruf von at.js bereitgestellt.

Sie können nach allen Aktivitäten filtern, die für die Entscheidungsfindung auf dem Gerät auf der Seite [!UICONTROL Aktivitäten] infrage kommen, über den Filter [!UICONTROL Gerätespezifische Entscheidungsfindung].

![Auf der Seite &quot;Aktivitäten&quot;können Sie den Filter für die Geräteentscheidung auswählen.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>Nach dem Erstellen und Aktivieren einer Aktivität, die für eine Entscheidung auf dem Gerät infrage kommt, kann es fünf bis zehn Minuten dauern, bis sie in das Regelartifact aufgenommen wird, das generiert und an den Akamai CDN-Point der Präsenzen weitergegeben wird.

## Zusammenfassung der Schritte, mit denen sichergestellt werden soll, dass meine Aktivitäten für die Entscheidungsfindung auf dem Gerät über &quot;at.js 2.5.0+&quot;bereitgestellt werden?

1. Rufen Sie die Adobe Target-Benutzeroberfläche auf und navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Implementierung]** > **[!DNL Account Details]**, um den Umschalter **[!UICONTROL Gerätekonfiguration]** zu aktivieren.
1. Aktivieren Sie den Umschalter **&quot;[!UICONTROL Schließen Sie alle vorhandenen qualifizierten Aktivitäten für die Geräteentscheidung in den Umschalter ein.]**

   Die erste JSON-Regelerstellung kann bis zu 10 Minuten dauern.

1. Erstellen und aktivieren Sie einen [Aktivität-Typ, der von der geräteinternen Entscheidungsfindung unterstützt wird](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md), und überprüfen Sie, ob die Entscheidung für das Gerät zulässig ist.
1. Stellen Sie die Entscheidungsmethode **[!UICONTROL entweder auf**[!UICONTROL &quot;Hybrid&quot;]**oder auf**[!UICONTROL &quot;Nur auf dem Gerät&quot;]**über die Benutzeroberfläche der at.js-Einstellungen ein.]**
1. Laden Sie at.js 2.5.0+ herunter und stellen Sie es auf Ihren Seiten bereit.
