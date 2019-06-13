---
description: Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „mbox.js“-Einstellungsseite unterstützen.
keywords: erweiterte mbox.js-Einstellungen;Client;Serverdomäne;xdomain;Komprimierungsstufe;Unterstützung von Client-Sitzungs-ID;secureOnly;Unterstützung von Client PC-ID;Pass Page;verweisende URL;Traffic-Stufe;Traffic-Dauer;Funktionsrumpf mboxParameters();Funktionsrumpf mboxSupported();Funktionsrumpf mboxCookieDomain();Extra-JavaScript;SiteCatalyst-Plug-in;mbox.js als selbstextrahierendes JavaScript erhalten;flackern;Körper ausblenden;Körper ausblenden
seo-description: Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „mbox.js“-Einstellungsseite unterstützen.
seo-title: mbox.js konfigurieren
solution: Target
title: mbox.js konfigurieren
uuid: e79c7af7-f8bd-4e2b-8e67-b04eddf0c65d
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mbox.js konfigurieren{#configure-mbox-js}

Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „mbox.js“-Einstellungsseite unterstützen.

Die Standardeinstellungen der [!DNL mbox.js]-Funktionsbibliothek entsprechen den Anforderungen der meisten [!DNL Target]-Kunden.

Wenden Sie sich bei Bedarf an Ihren Kundenbetreuer, wenn Sie die [!DNL mbox.js]-Einstellungen ändern möchten.

Die folgenden Einstellungen sind verfügbar:

## Kunde

Der Kundencode für Ihr Konto

Wenn Sie [!UICONTROL Einrichten &gt; Implementierung &gt; „mbox.js“-Einstellungen bearbeiten] aufrufen, finden Sie den Clientcode für Ihr Konto ganz oben.

## Zeitüberschreitung

Zeitüberschreitung der Target-Anfrage.

Unter [!UICONTROL Einrichtung &gt; Implementierung &gt; mbox.js-Einstellungen bearbeiten] ist die Zeitüberschreitung nach der Komprimierungsstufe die Zeitüberschreitung Ihrer Target-Anfrage. Standardmäßig ist dieser Wert auf 15 Sekunden festgelegt. Wir empfehlen jedoch, den Wert auf 2–5 Sekunden festzulegen.

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