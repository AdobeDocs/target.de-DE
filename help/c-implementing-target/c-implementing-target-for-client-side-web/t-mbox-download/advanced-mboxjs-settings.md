---
keywords: advanced mbox.js settings;client;server domain;xdomain;compression level;client session id support;secureOnly;client pc id support;pass page;referring url;traffic level;traffic duration;mboxParameters() function body;mboxSupported() function body;mboxCookieDomain() function body;Extra JavaScript;SiteCatalyst plug-in;Get mbox.js as self-extracting JavaScript;flicker;body hiding;hide body
description: Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „mbox.js“-Einstellungsseite unterstützen.
title: mbox.js konfigurieren
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 91%

---


# mbox.js konfigurieren{#configure-mbox-js}

Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „mbox.js“-Einstellungsseite unterstützen.

Die Standardeinstellungen der [!DNL mbox.js]-Funktionsbibliothek entsprechen den Anforderungen der meisten [!DNL Target]-Kunden.

Wenden Sie sich bei Bedarf an Ihren Kundenbetreuer, wenn Sie die [!DNL mbox.js]-Einstellungen ändern möchten.

Die folgenden Einstellungen sind verfügbar:

## Kunde

Der Kundencode für Ihr Konto

Bei Ansicht [!UICONTROL Administration > Implementierung] ist der Client oben der Client-Code für Ihr Konto.

## Zeitüberschreitung

Zeitüberschreitung der Target-Anfrage.

Wenn Sie [!UICONTROL Administration > Implementierung] anzeigen, ist die Einstellung für das Timeout (Sekunden) der Timeout-Wert für Ihre Zielgruppe. Standardmäßig ist dieser Wert auf 15 Sekunden festgelegt. Wir empfehlen jedoch, den Wert auf 2–5 Sekunden festzulegen.

## XDomain

Legt fest, ob der Browser die Cookies in Ihrer eigenen Domäne (Erstanbieter-Cookies), in der Target-Domäne oder in beiden Domänen einrichtet.

Wenn Sie diese Einstellung ändern, wirkt sich dies sowohl auf „mbox.js“ als auch „at.js“ aus.

## Komprimierungsstufe

Legt fest, wie stark die mbox.js-Bibliotheksdatei komprimiert ist. Durch Erhöhen der Kompressionsstufe wird die Seitenladezeit verkürzt.

## mboxParameters()-Funktionsrumpf

Gibt zusätzliche Parameter zurück, die an jeden Mbox-Aufruf weitergegeben werden.

Beispiel:

return &quot;test=123&quot;;

## mboxSupported()-Funktionsrumpf

Gibt „false“ zurück, um bestimmte Benutzer auszuschließen.

Beispiel:

return !navigator.userAgent.indexOf(&#39;Safari&#39;) != -1;

Folgende Browser können akzeptiert oder ausgeschlossen werden:

* IE 5.0 oder neuer (Windows)
* Netscape 5.0 oder neuer (Mac, Windows, Linux)
* Safari 1.2.4 oder neuer (Mac)
* Mozilla Firefox 1.0 oder neuer (Mac, Windows, Linux)

## mboxCookieDomain()-Funktionsrumpf

Gibt eine Zeichenfolge zurück, die die Domäne für das Einrichten der Erstanbieter-Cookies beschreibt.

Beispiel:

return &quot;YOUR-DOMAIN&quot;;

## Extra JavaScript

Umfasst extra JavaScript, das auf den einzelnen Seiten ausgeführt werden soll.

## SiteCatalyst-Plug-in

Aktiviert das Analytics Target-Plug-in.

Wenn das Analytics-Plug-in aktiviert ist, erzeugt es einen Plug-in-Code in mbox.js. Dieser Code sendet Analytics-Tag-Informationen als mbox-Anfrage auf jeder mit Analytics getaggten Seite an die Target-Server.

Beachten Sie, dass auf der Seite weiterhin auf das Analytics-Plug-in verwiesen werden muss.

## secureOnly

Zeigt an, ob „mbox.js“ nur HTTPS verwenden sollte oder es möglich ist, dass basierend auf dem Seitenprotokoll zwischen HTTP und HTTPS umgeschaltet wird. Es handelt sich hierbei um eine erweiterte Einstellung, deren Standardwert „falsch“ lautet.