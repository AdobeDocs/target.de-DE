---
keywords: at.js; Browser-Benutzeragent; Benutzeragent; Client-Hinweise; user-agent
description: Erfahren Sie mehr [!DNL Adobe Target] verwendet den Benutzeragenten und Client Hints, um Besucher für die Segmentierung und Personalisierung zu qualifizieren.
title: Benutzeragent und Client-Hinweise
feature: at.js
role: Developer
source-git-commit: 2527608fc781913024d5d6ffee49aff9eb6c2f42
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 3%

---

# Benutzeragent und Client-Hinweise

[!DNL Adobe Target] verwendet den Benutzeragenten, um Besucher für die Segmentierung und Personalisierung zu qualifizieren.

Jedes Mal, wenn ein Webbrowser eine Anforderung an einen Server sendet, enthält der Header der Anfrage Informationen über den Browser und die Umgebung, in der der Browser ausgeführt wird. Seit den frühen Tagen des Internets wurden diese Daten in einer einzigen Zeichenfolge zusammengefasst, die &quot;user-agent&quot;genannt wird.

Im Folgenden finden Sie ein Beispiel für einen Benutzeragenten eines Mac OS X-basierten Computers, der einen Safari-Browser verwendet:

```
Mozilla/5.0 (Linux; Android 12; SM-S908E) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.41 Mobile Safari/537.36 
```

Von diesem Benutzeragenten kann der Server, der die Anfrage erhält, die folgenden Informationen zum Browser und Betriebssystem erkennen:

| Informationen | Details |
| --- | --- |
| Softwarename | Chrome |
| Softwareversion | 101 |
| Vollversion der Software | 101.0.4951.41 |
| Name der Layout-Engine | AppleWebKit |
| Layout-Engine-Version | 537.36 |
| Betriebssystem | Android |
| Betriebssystemversion | Android 12 (Snow Cone) |
| Gerät | SM-S908E (Samsung Galaxy S22 Ultra) |

Im Laufe der Jahre ist die Menge der Browser- und Geräteinformationen, die in der Zeichenfolge &quot;user-agent&quot;enthalten sind, gestiegen.

## Anwendungsfälle für Benutzeragenten

Mit Benutzeragenten erhalten Marketing- und Entwicklungsteams seit langem wichtige Einblicke in die Funktionsweise von Browsern und Betriebssystemen. und -Geräte zeigen Site-Inhalte an und zeigen an, wie Benutzer mit Websites interagieren. Benutzeragenten werden auch verwendet, um Spam zu verhindern und Bots zu filtern, die Sites für eine Vielzahl zusätzlicher Zwecke durchsuchen.

In den letzten Jahren haben einige Site-Eigentümer und Marketing-Anbieter den Benutzer-Agent zusammen mit anderen Informationen in Anfrage-Headern verwendet, um digitale Fingerabdrücke zu erstellen, die als Mittel zur Identifizierung von Benutzern ohne deren Wissen verwendet werden können. Trotz des wichtigen Zwecks, den der Benutzer-Agent für Site-Eigentümer erfüllt, haben Browser-Entwickler beschlossen, Änderungen an der Funktionsweise von Benutzeragenten vorzunehmen, um potenzielle Datenschutzprobleme für Site-Besucher zu begrenzen.

User-Agent Client Hints ist die Lösung, die Browser-Entwickler entwickelt haben. Client Hints ermöglicht es Sites weiterhin, die erforderlichen Browser-, Betriebssystem- und Geräteinformationen zu erfassen und gleichzeitig einen besseren Schutz vor verdeckten Tracking-Methoden wie dem Fingerabdruck zu bieten.

## Client-Hinweise

Benutzeragenten-Client-Hinweise bieten Website-Inhabern die Möglichkeit, auf einen Großteil der Informationen zuzugreifen, die im Benutzeragenten verfügbar sind, jedoch auf eine mehr datenschutzfreundliche Weise. Wenn moderne Browser einen Benutzer-Agenten an einen Webserver senden, wird der gesamte Benutzer-Agent bei jeder Anfrage gesendet, unabhängig davon, ob dies erforderlich ist. Client Hints hingegen erzwingt ein Modell, bei dem der Server den Browser nach den zusätzlichen Informationen über den Client fragen muss. Nach Erhalt dieser Anfrage kann der Browser seine eigenen Richtlinien oder Benutzerkonfigurationen anwenden, um zu bestimmen, welche Daten zurückgegeben werden. Anstatt den gesamten Benutzer-Agenten standardmäßig für alle Anfragen verfügbar zu machen, wird der Zugriff jetzt explizit und überprüfbar verwaltet.

Benutzeragenten-Client-Hinweise sind in Chrome seit Version 89 verfügbar. Aktuelle Versionen von Chromium-basierten Browsern wie Microsoft Edge, Opera, Brave, Chrome Android, Opera Android und Samsung Internet unterstützen ebenfalls die Client Hints-API.

Client-Hinweise in den Kopfzeilen der ersten vom Browser an einen Webserver gerichteten Anfrage enthalten die Browsermarke, die Hauptversion des Browsers und einen Hinweis darauf, ob es sich bei dem Client um ein Mobilgerät handelt. Jedes Datenelement hat einen eigenen Header-Wert, anstatt in eine einzelne Benutzer-Agent-Zeichenfolge gruppiert zu werden, wie im folgenden Beispiel gezeigt:

```
Sec-CH-UA: "Chromium";v="101", "Google Chrome";v="101", " Not;A Brand";v="99" 
Sec-CH-UA-Mobile: ?0 
Sec-CH-UA-Platform: "macOS"
```

Im folgenden Beispiel wird der Benutzer-Agent für denselben Browser verwendet:

```
Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.54 Safari/537.36 
```

Obwohl die Informationen ähnlich sind, enthält die erste Anforderung an den Server Client-Hints, die nur eine Untergruppe der verfügbaren Elemente in der Zeichenfolge &quot;user-agent&quot;enthalten. Bei der Anfrage fehlen die Betriebssystemarchitektur, die vollständige Betriebssystemversion, der Name der Layout-Engine, die Version der Layout-Engine und die vollständige Browser-Version. Bei nachfolgenden Anfragen ermöglicht die Client Hints-API Webservern jedoch, zusätzliche, hohe Entropy-Details zum Gerät anzufordern. Wenn diese hohen Entropy-Werte abhängig von der Browserrichtlinie oder den Benutzereinstellungen angefordert werden, kann die Browserantwort diese Informationen enthalten.

Das folgende Beispiel ist ein JSON-Objekt, das von der Client Hints-API zurückgegeben wird, wenn hohe Entropiewerte angefordert werden:

```
{ 

    "architecture":"x86", 
    "bitness":"64", 
    "brands":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100" 
        } 
    ], 
    "fullVersionList":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99.0.0.0" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100.0.4896.127" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100.0.4896.127" 
        } 
    ], 
    "mobile":false, 
    "model":"", 
    "platformVersion":"12.2.1" 
} 
```

Die hohen Entropy-Werte umfassen mehrere zusätzliche Informationen, die in den standardmäßigen Client Hints-Informationen nicht verfügbar sind. Die folgende Tabelle enthält Details dazu, welche Daten in der Standardanfrage verfügbar sind, im Vergleich zu den Informationen zu hohen Entropie-Benutzeragenten-Client-Hints.

| HTTP-Header | JavaScript | User-agent | Client-Hinweis | Hoher Entropie-Client-Hinweis |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | Marken | Ja | Ja | Nein |
| Sec-CH-UA-Platform | Plattform | Ja | Ja | Nein |
| Sec-CH-UA-Mobile | mobile | Ja | Ja | Nein |
| Sec-CH-UA-Platform-Version | platformVersion | Ja | Nein | Ja |
| Sec-CH-UA-Arch | Architektur | Ja | Nein | Ja |
| Sec-CH-UA-Modell | model | Ja | Nein | Ja |
| SEC-CH-UA-Bitness | Bitrate | Ja | Nein | Ja |
| sec-CH-UA-full-version-list | fullVersionList | Ja | Nein | Ja |

## Migration zu Client Hints

Derzeit senden Chromium-basierte Browser den Benutzeragenten zusammen mit Client Hints in den Headern von Anforderungen an Webserver. Ab April 2022 und bis Februar 2023 wird jedoch die Menge der in der Benutzeragenten-Zeichenfolge enthaltenen Daten reduziert. In anderen Browsern wie Safari und Firefox wird die Zeichenfolge &quot;user-agent&quot;weiterhin verwendet. aber auch sie werden den Umfang der darin enthaltenen Informationen verringern.

## [!DNL Target] Anwendungsfälle, die Clint-Hinweise erfordern

Die folgenden Anwendungsfälle in Target erfordern Client-Hinweise:

### Zielgruppenattribute

Wenn Sie [!DNL Target] Zielgruppen verwenden und eines der folgenden Zielgruppenattribute verwenden, [!DNL Target] erfordert, dass Client Hints die richtige Segmentierung durchführt:

* Browser
* Betriebssystem
* Mobil

### Profilskripte

Wenn Sie Profilskripte verwenden und auf die `user.browser` -Attribut (bezieht sich auf &quot;user-agent&quot;), müssen Sie möglicherweise das Profilskript aktualisieren, um auch einen oder mehrere Client-Hinweise zu überprüfen. Sie können über die Funktion auf alle Client-Hinweise zugreifen `user.clientHint('sec-ch-ua-xxxxx')`. Der Kopfzeilenname des Client Hint muss in Kleinbuchstaben angegeben werden.

Das folgende Beispiel zeigt, wie ein Windows-Betriebssystem in einem Profilskript richtig erkannt wird:

```
"return (((user.browser != null) && (user.browser.indexOf(\"Windows\") > -1)) || " + 
      "((user.clientHint('sec-ch-ua-platform') != null) && 
(user.clientHint('sec-ch-ua-platform') === 'Windows')));" 
```

In den folgenden Abschnitten werden die Kopfzeilen von Client Hints und die zugehörigen Anwendungssemantiken für Profilskripte angezeigt.

#### Sec-CH-UA

Entropie: Geringe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA){target=_blank} Zielgruppenattribut: Verwendung von Browserprofil-Skripten: `user.clientHint('sec-ch-ua')`

#### Sec-CH-UA-Arch

Entropie: Hohe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch){target=_blank} Zielgruppenattribut: Nutzung von Profilskripten: `user.clientHint('sec-ch-ua-arch')`

#### SEC-CH-UA-Bitness

Entropie: Hohe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness){target=_blank} Zielgruppenattribut: Nutzung von Profilskripten: `user.clientHint('sec-ch-ua-bitness')`

#### sec-CH-UA-full-version-list

Entropie: Hohe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List){target=_blank} Zielgruppenattribut: Verwendung von Browserprofil-Skripten: `user.clientHint('sec-ch-ua-full-version-list')`

#### Sec-CH-UA-Mobile

Entropie: Geringe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile){target=_blank} Zielgruppenattribut: Verwendung von Profilskripten für Mobilgeräte: `user.clientHint('sec-ch-ua-mobile')`

#### Sec-CH-UA-Modell

Entropie: Hohe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model){target=_blank} Zielgruppenattribut: Verwendung von Profilskripten für Mobilgeräte: `user.clientHint('sec-ch-ua-model')`

#### Sec-CH-UA-Platform

Entropie: Geringe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform){target=_blank} Zielgruppenattribut: Verwendung von Betriebssystemprofilskripten: `user.clientHint('sec-ch-ua-platform')`

#### Sec-CH-UA-Platform-Version

Entropie: Hohe Dokumentation: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version){target=_blank} Zielgruppenattribut: Nutzung von Profilskripten: `user.clientHint('sec-ch-ua-platform-version')`

## Weitergeben von Client-Hinweisen an [!DNL Adobe Target]

Die folgenden Abschnitte enthalten je nach Ihrer [!DNL Target] Implementierung.

### at.js-Version 2.9.0 (oder höher)

Ab at.js 2.9.0 werden Benutzeragenten-Client-Hinweise automatisch vom Browser erfasst und an gesendet [!DNL Target] when `getOffer/getOffers()` aufgerufen wird. Standardmäßig erfasst at.js nur &quot;Geringe Entropie&quot;-Client-Hinweise. Wenn Sie die Zielgruppensegmentierung durchführen oder Profilskripte verwenden, die auf Daten basieren, die in den vorhergehenden Abschnitten als &quot;Hohe Entropie&quot;kategorisiert wurden, müssen Sie at.js so konfigurieren, dass es über den Browser Client-Hints mit &quot;Hoher Entropie&quot;erfasst `targetGlobalSettings`.

`window.targetGlobalSettings = { allowHighEntropyClientHints: true };`

### Serverseitige SDKs

Weitere Informationen zum Übergeben von Client-Hinweisen über Server-seitige SDKs finden Sie unter [Client-Hinweise](https://adobetarget-sdks.gitbook.io/docs/core-principles/audience-targeting#client-hints){target=_blank} im *Adobe Target SDKs* Dokumentation.












