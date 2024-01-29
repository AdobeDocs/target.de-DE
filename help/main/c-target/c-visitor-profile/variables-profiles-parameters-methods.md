---
keywords: Variablen; Profile; Parameter; eingebaute Profile; Methoden; URL-Variablen; Geo-Profile; Drittanbieterprofile; Mbox-Variablen; Kampagnenvariablen; Kundenattribute
description: Zeigen Sie eine Liste verschiedener Profile, Variablen und Parameter an, die in Profilskripten in Adobe Target nützlich sind.
title: Welche Profile, Variablen und Parameter werden in verwendet? [!DNL Target]?
feature: Audiences
exl-id: 96ef9a56-fe76-428e-a164-c01829fdf45d
source-git-commit: d3c9a5bfa1e0496387103d82dd811f28581ba8bf
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 70%

---

# Nützliche Variablen, Profile, Parameter und Methoden

Diese Seite listet Profile, Variablen und Parameter auf, die in Profilskripten nützlich sind.

## Integrierte Profile {#section_2B694370003C4F8E8E29E0B2F6E52045}

| Profil | Hinweise |
|--- |--- |
| user.activeActivities<br>user.activeCampaigns | Gibt die Kampagnen-ID für alle Kampagnen/Aktivitäten zurück, in denen sich der Benutzer befindet. Dies passiert auch dann, wenn er in der aktuellen Sitzung nicht mit der Kampagne/Aktivität interagiert hat. |
| user.pcId |  |
| user.sessionId |  |
| user.categoryAffinity |  |
| user.categoryAffinities | Gibt ein Array der Präferenzen zurück, die für den Benutzer vorhanden sind |
| user.isFirstSession |  |
| user.isNewSession |  |
| user.daysSinceLastVisit |  |
| user.browser | Der Benutzeragent |
| user.header | Alle `user.header`-Profile werden von den Kopfzeilendaten einer Mbox-Anfrage integriert |
| user.header(&#39;x-forwarded-for&#39;) | Die öffentliche IP-Adresse der Netzwerkverbindung des Besuchers.<br>Sie können dies beispielsweise auf verschiedene Arten erhalten [whatismyip.com](https://www.whatismyip.com/). Die IP-Adresse ist nicht die NAT-Adresse (interne Adresse), die mit 10., 192.168. oder 172 beginnt.<br>Hinweis: user.header(&#39;x-cluster-client-ip&#39;) wurde eingestellt. |
| user.header(&#39;host&#39;) | Website-Hostname |
| user.header(&#39;cookie&#39;) | Cookie-Daten des Besuchers |
| user.header(&#39;user-agent&#39;) | Benutzeragent des Benutzer-Browsers |
| user.header(&#39;accept-language&#39;) | Besuchersprache |
| user.header(&#39;accept-encoding&#39;) | Besucher-Zeichenkodierung |
| user.header(&#39;accept&#39;) | Besuchersprache und Zeichenkodierung |
| user.header(&#39;connection&#39;) | Serververbindung. Beispiel: keep-live |
| user.header(&#39;referrer&#39;) | Website-URL der aktuellen Seite des Besuchers. Funktioniert nicht im Internet Explorer. |
| user.getLocal(&#39;param_name&#39;); | Rufen Sie den Wert ab, den Sie mithilfe von `user.setLocal`. |
| user.setLocal(&#39;param_name&#39;,&#39;value&#39;) | Erstellen Sie persistente Profilwerte in einem Profilskript. Diese Werte bleiben wie ein Profilskript erhalten, Sie haben jedoch nur Zugriff darauf innerhalb des Skripts, das festgelegt wurde. |
| user.get(&#39;param_name&#39;) |  |
| user.parameter | Aus Profilskripten erstellte beständige Profilattribute. Verweist auch auf &quot;Systemprofile&quot;wie Geolocation, Besuchsanzahl usw. |
| profile.get(&#39;param_name&#39;) | Die richtige Methode zum Abrufen eines Profilparameters, der in einem Profilskript verwendet werden soll, ist die Methode profile.get(&#39;param_name&#39;) . |
| profile.param(&#39;param_name&#39;); |  |
| profile.parameter(&#39;parameter_name&#39;); | mbox-Parameter, die aufgrund ihres Profil.  -Präfix als beständig festgelegt wurden. |
| „profile.browserTime“ | Die lokale Browserzeit des Besuchers. Erstellen Sie für die Systemzeit ein neues Datenobjekt im Profilskript. |
| profile.averageDaysBetweenVisits |  |
| profile.sessionCount |  |
| profile.mobile.isTablet | Besuchergerät ist ein Tablet.<P>Dieses Profil ersetzt die veraltete Version [Browser ist die iPad-Zielgruppenkategorie](/help/main/c-target/c-audiences/c-target-rules/browser.md). |
| profile.mobile.isMobilePhone | Besuchergerät ist ein Mobiltelefon.<P>Dieses Profil ersetzt die veraltete Version [Browser ist die iPhone-Zielgruppenkategorie](/help/main/c-target/c-audiences/c-target-rules/browser.md). |
| parameter= | Allgemeiner Begriff für zusätzliche Werte, die mit einer Mbox weitergegeben werden, zum Beispiel Namen-/Werte-Paare. Nicht beständig, sofern nicht mit `profile.parameter` oder `user.parameter` so festgelegt. |

## URL-Variablen {#section_8F25958273164EBAA6DC659302993FD3}

| `landing` | `referrer` | `page` |
|---|---|---|
| `landing.url` | `referrer.url` | `page.url` |
| `landing.domain` | `referrer.domain` | `page.domain` |
| `landing.protocol` | `referrer.protocol` | `page.protocol` |
| `landing.param` | `referrer.param` | `page.param` |
| `landing.query` | `referrer.query` | `page.query` |

## Geo- und Mobilnetzbetreiber-Profile {#section_08441DA42E7346918FBB345818854997}

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`
* `profile.geolocation.latitude`
* `profile.geolocation.longitude`

## mbox-Variablen {#section_C42F0D33BD8044BE812FA0B7905CC0ED}

| Variable | Hinweise |
|--- |--- |
| `mbox.name` |  |
| mbox.param(&#39;param_name&#39;) |  |
| Automatisch mit jeder Anfrage weitergegebene Parameter:<ul><li>mbox.param(&#39;browserHeight&#39;)</li><li>mbox.param(&#39;browserTimeOffset&#39;)</li><li>mbox.param(&#39;browserWidth&#39;)</li><li>mbox.param(&#39;colorDepth&#39;)</li><li>mbox.param(&#39;mboxXDomain&#39;)</li><li>mbox.param(&#39;mboxTime&#39;)</li><li>mbox.param(&#39;screenHeight&#39;)</li><li>mbox.param(&#39;screenWidth&#39;)</li></ul> |
| Parameter, die mit Bestellaufgabe-Mboxes weitergegeben werden:<ul><li>mbox.param(&#39;orderId&#39;)</li><li>mbox.param(&#39;orderTotal&#39;)</li><li>mbox.param(&#39;productPurchasedId&#39;)</li></ul> |
| mbox3rdPartyId | Ein Parameter „mbox“ zum Synchronisieren einer Kunden-ID mit der mboxPC-ID in Target. Eine Kunden-ID ist eine ID, die Ihr Unternehmen zum Verfolgen von Besuchern verwendet, zum Beispiel eine CRM-ID, eine Mitglieds-ID oder etwas Ähnliches. Diese ID kann dann zum Hinzufügen von Informationen über die Profil-APIs und [Kundenattribute](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/customer-attributes.html){target=_blank}. |
| mboxPageValue | Bei jeder Mbox-Anfrage wird der Seite ein Wert zugewiesen. |
| mboxDebug | Wird nur für Debug-Informationen verwendet. Zur Seiten-URL hinzugefügt, nach der at.js sucht. |
| mboxOverride.browserIp | Legt einen anderen Geo-Standort als den tatsächlichen Standort fest, damit Sie sehen können, wie etwas an einem anderen Standort aussehen würde.<br>**Hinweis:** mboxOverride-Parameter sollte nur beim Testen der Aktivität verwendet werden, aber nicht bei der Produktion. Die Verwendung von MboxOverride-Parametern kann bei der Verwendung von [Analytics für Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) zu Berichtsdiskrepanzen führen. Sie sollten während des Testens den [Aktivitäts-QA-Modus](/help/main/c-activities/c-activity-qa/activity-qa.md) verwenden, um sicherzustellen, dass Ihre Aktivität wie erwartet funktioniert, bevor Sie die Aktivität in Ihre Live-Umgebung versetzen. |

## Kundenattribute {#section_62B4821EB6564FF4A14159A837AD4EDB}

Kundenattribute können in Profilskripts referenziert werden, formatiert als `crs.get('<Datasource Name>.<Attribute name>')`.

Diese Attribute stehen auch als Tokens in Profilskripts und direkt in Angeboten zur Verfügung, ohne dass zunächst ein Profilskript erforderlich ist. Das Token sollte folgende Form aufweisen: `${crs.datasourceName.attributeName}`. Beachten Sie, dass die Leerzeichen in `datasourceName` sollte bei jedem API-Aufruf entfernt werden.
