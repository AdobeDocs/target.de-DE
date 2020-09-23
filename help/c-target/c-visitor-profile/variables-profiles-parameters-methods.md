---
keywords: variables;profiles;parameters;built in profiles;methods;url variables;geo profiles;third party profiles;mbox variables;campaign variables;customer attributes
description: Diese Seite listet Profile, Variablen und Parameter auf, die in Profilskripten nützlich sind.
title: Nützliche Variablen, Profile, Parameter und Methoden
feature: visitor profiles
topic: Standard
uuid: 9286467c-cbb5-42be-99c0-6687ffab0969
translation-type: tm+mt
source-git-commit: 2f437e4cf33e4facba60d53ba545beb95c16f191
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 92%

---


# Nützliche Variablen, Profile, Parameter und Methoden{#profile-and-variable-glossary}

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
| user.header(&#39;x-forwarded-for&#39;) | Die öffentliche IP-Adresse der Netzwerkverbindung des Besuchers.<br>Sie können dies auf verschiedenen Wegen erreichen, z. B. [whatismyip. com](https://www.whatismyip.com/). Die IP-Adresse ist nicht die NAT-Adresse (interne Adresse), die mit 10., 192.168. oder 172 beginnt.<br>Hinweis: user.header(&#39;x-cluster-client-ip&#39;) wurde nicht mehr unterstützt. |
| user.header(&#39;host&#39;) | Website-Hostname |
| user.header(&#39;cookie&#39;) | Cookie-Daten des Besuchers |
| user.header(&#39;user-agent&#39;) | Benutzeragent des Benutzer-Browsers |
| user.header(&#39;accept-language&#39;) | Besuchersprache |
| user.header(&#39;accept-encoding&#39;) | Besucher-Zeichenkodierung |
| user.header(&#39;accept&#39;) | Besuchersprache und Zeichenkodierung |
| user.header(&#39;connection&#39;) | Serververbindung. Beispiel: keep-live |
| user.header(&#39;referrer&#39;) | Website-URL der aktuellen Seite des Besuchers. Funktioniert nicht im Internet Explorer. |
| user.getLocal(&#39;param_name&#39;,&#39;value&#39;); |  |
| user.setLocal(&#39;param_name&#39;,&#39;value&#39;); |  |
| user.get(&#39;param_name&#39;) |  |
| user.parameter | Aus Profilskripten erstellte beständige Profilattribute. Verweist auch auf „Systemprofile“ wie geografischer Standort, Besucherzahlen usw. |
| profile.get(&#39;param_name&#39;) | Die richtige Methode zum Abrufen eines Profil-Parameters, der in einem Profil-Skript verwendet werden soll, ist die Profil.get(&#39;param_name&#39;)-Methode. |
| profile.param(&#39;param_name&#39;); |  |
| profile.parameter(&#39;parameter_name&#39;); | mbox-Parameter, die aufgrund ihres Profil.  -Präfix als beständig festgelegt wurden. |
| „profile.browserTime“ | Die lokale Browserzeit des Besuchers. Erstellen Sie für die Systemzeit ein neues Datenobjekt im Profilskript. |
| profile.averageDaysBetweenVisits |  |
| profile.sessionCount |  |
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
| mbox3rdPartyId | Ein Parameter „mbox“ zum Synchronisieren einer Kunden-ID mit der mboxPC-ID in Target. Eine Kunden-ID ist eine ID, die Ihr Unternehmen zum Verfolgen von Besuchern verwendet, zum Beispiel eine CRM-ID, eine Mitglieds-ID oder etwas Ähnliches. Diese ID kann anschließend verwendet werden für das Hinzufügen von Informationen über die Profil-APIs und  [Kundenattribute](/help/c-target/c-visitor-profile/working-with-customer-attributes.md). |
| mboxPageValue | Bei jeder Mbox-Anfrage wird der Seite ein Wert zugewiesen. |
| mboxDebug | Wird nur für Debug-Informationen verwendet. Wird der Seiten-URL hinzugefügt, auf der mbox.js danach sucht. |
| mboxOverride.browserIp | Legt einen anderen Geo-Standort als den tatsächlichen Standort fest, damit Sie sehen können, wie etwas an einem anderen Standort aussehen würde.<br>**Hinweis:** mboxOverride-Parameter sollte nur beim Testen der Aktivität verwendet werden, aber nicht bei der Produktion. Die Verwendung von MboxOverride-Parametern kann bei der Verwendung von [Analytics für Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) zu Berichtsdiskrepanzen führen. Sie sollten während des Testens den [Aktivitäts-QA-Modus](/help/c-activities/c-activity-qa/activity-qa.md) verwenden, um sicherzustellen, dass Ihre Aktivität wie erwartet funktioniert, bevor Sie die Aktivität in Ihre Live-Umgebung versetzen. |

## Kundenattribute {#section_62B4821EB6564FF4A14159A837AD4EDB}

Kundenattribute können in Profilskripts referenziert werden, formatiert als `crs.get('<Datasource Name>.<Attribute name>')`.

Diese Attribute stehen auch als Tokens in Profilskripts und direkt in Angeboten zur Verfügung, ohne dass zunächst ein Profilskript erforderlich ist. Das Token sollte folgende Form aufweisen: `${crs.datasourceName.attributeName}`. Beachten Sie, dass Leerzeichen im `datasourceName` API-Aufruf entfernt werden sollten.
