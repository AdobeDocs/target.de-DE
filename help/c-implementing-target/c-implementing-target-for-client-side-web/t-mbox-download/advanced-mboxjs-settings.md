---
keywords: erweiterte mbox.js-Einstellungen;Client;Serverdomäne;xdomain;Komprimierungsstufe;Unterstützung von Client-Sitzungs-ID;secureOnly;Unterstützung von Client PC-ID;Pass Page;verweisende URL;Traffic-Stufe;Traffic-Dauer;Funktionsrumpf mboxParameters();Funktionsrumpf mboxSupported();Funktionsrumpf mboxCookieDomain();Extra-JavaScript;SiteCatalyst-Plug-in;mbox.js als selbstextrahierendes JavaScript erhalten;flackern;Körper ausblenden;Körper ausblenden
description: Erfahren Sie mehr über die ältere Implementierung von "mbox.js"in Adobe Target. Migrieren Sie zum Adobe Experience Platform Web SDK (AEP Web SDK) oder zur neuesten Version von at.js.
title: Wie konfiguriere ich die Zielgruppe mbox.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 70%

---


# mbox.js konfigurieren

Informationen, die Sie bei der Festlegung verschiedener Einstellungen auf der „mbox.js“-Einstellungsseite unterstützen.

>[!IMPORTANT]
>
>**mbox.js Ende der Lebensdauer**: Am 31. März 2021  [!DNL Adobe Target] wird die Bibliothek &quot;mbox.js&quot;nicht mehr unterstützt. Nach dem 31. März 2021 schlagen alle Aufrufe von &quot;mbox.js&quot;korrekt fehl und wirken sich auf Ihre Seiten aus, deren [!DNL Target]-Aktivitäten ausgeführt werden, indem Standardinhalte bereitgestellt werden.
>
>Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder at.js-JavaScript-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: zielgruppe für clientseitige Web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md) implementieren.

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