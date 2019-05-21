---
description: Informationen zu Zeichen- und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.) für Aktivitäten und andere Elemente in Adobe Target.
keywords: Zeichenbeschränkung; Mbox-Parameter; Batch-Bereitstellungs-API; Profilparameter; Beschränkungen; integrierte Profile; Maximum; Beschränkung; Bedingung; Zeichen; Best Practice; BestellID; gesamte Bestellung; MboxdrittanbieterID; Kategorie; KategorieID
seo-description: Informationen zu Zeichen- und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.) für Aktivitäten und andere Elemente in Adobe Target.
seo-title: Beschränkungen
solution: Target
title: Beschränkungen
topic: Standard
uuid: 603fb800-a26c-43ec-b2d9-ef7a8ed8721e
translation-type: tm+mt
source-git-commit: dda07f19bddb870b20dabc484a1b97d55bcc5775

---


# Beschränkungen{#limits}

Informationen zu Zeichen- und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.) für Aktivitäten und andere Elemente in Adobe Target.

Bei den unten aufgeführten Beschränkungen handelt es sich um empfohlene Beschränkungen. Wenn diese Beschränkungen erreicht oder überschritten werden, kann sich die Performance verlangsamen. Langsame Ladezeiten der Oberfläche können ebenfalls durch eine sehr komplexe Aktivität bedingt sein, die viele Zielgruppen, Ziele und Erlebnisse enthält.

Hochkomplexe Aktivitäten sollten mit Adobe Consulting geprüft und in einer eingeschränkten Umgebung getestet werden, bevor sie zur Produktion freigegeben werden.

## Aktivitätsnamen

**Limit**: 250 Zeichen.

## Zielgruppennamen

**Limit**: 256 Zeichen.

Werte mit mehr als 256 Zeichen werden gekürzt.

## categoryId-Parameter

**Limit**: 250 Zeichen.

## Kundenattributnamen

**Limit**: 128 Zeichen.

## Kundenattributalias-ID

**50** Zeichen begrenzen.

## Benutzerdefinierte Entitätsattribute

**Limit**: Die maximale Länge hängt von der Sprache ab.

* 15.000 Zeichen (Einzelwert, ein- und Zweibyte-Sprachen)
* 500 Werte, 100 Zeichen pro Wert (mehrere Werte)

Die maximale Länge von benutzerdefinierten Attributen für Einzelwertentitäten beträgt 15.000 Zeichen (für ein- und zweibyte-UTF -8-kodierte Sprachen wie Englisch und andere lateinische Skriptbuchstaben) oder 10.000 Zeichen (für 3-Byte-UTF -8-kodierte Sprachen wie Chinesisch, Japanisch und Koreanisch).

Benutzerdefinierte Attribute mit mehreren Werten dürfen maximal 500 Werte enthalten. Jeder einzelne Wert ist auf 100 Zeichen begrenzt. Die Gesamtanzahl der Zeichen für alle Werte muss den Beschränkungen für die maximale Länge von benutzerdefinierten Attributen für Einzelwertentitäten entsprechen (siehe oben).

## Entityid-Parameter

**Limit**: 1.000 Zeichen.

## Excludedids {#excludedid}

**Limit**: 5 KB für POST-Anforderungen. 2.083 Zeichen minus der Länge der URL für GET-Anforderungen.

Bei GET-Anforderungen beträgt der Grenzwert für das Back-End zwar 5 KB, aufgrund der Tatsache, dass Microsoft Internet Explorer die URL auf 2.083 Zeichen begrenzt, beträgt der tatsächliche Grenzwert 2.083 Zeichen minus der aktuellen Länge der URL.

## Erlebnisnamen

**Limit**: 20 Zeichen.

## In-mbox-Profilattributwert

**Limit**: 256 Zeichen.

Längere Werte werden abgeschnitten.

## In-mbox-Profile in einer mbox-Anfrage

**Limit**: 50 Profile.

Alle Profile über 50 werden ignoriert.

## In-mbox-Profilnamen

**Limit**: 128 Zeichen.

## mbox-Namen

**Limit**: 250 Zeichen.

## Mbox-Parameter

**Limit**: Die folgenden Beschränkungen gelten für Mbox-Parameter:

* mbox-Parameter: 500 Parameter pro mbox.
* Profilparameter: 500 Parameter.
* Profilparameter pro Mbox:
* Andere Parameter (URL, verweisende URL usw.): 50 Parameter pro Mbox für jeden Parametertyp.

Für Parameter, die in der Target-Datenbank protokolliert werden, gelten die oben genannten Grenzwerte für Standard-mbox-Anfragen. Diese Beschränkungen gelten, sofern die Anfrage nicht durch Webbrowser-Beschränkungen gekürzt wird.

Wenn Sie die [Batch-Bereitstellungs-API](https://developers.adobetarget.com/api/#server-side-batch-delivery) im Mobile Services SDK verwenden, sind die Beschränkung von 50 Mbox-Parametern, 50 Profilparametern und 50 für andere Parametertypen Einschränkungen der API selbst. Es ist nicht möglich, mit der Batch-Bereitstellungs-API Anfragen zu senden, die mehr als diese Anzahl von Parametern enthalten. Wenn eine Anforderung mehr als diese Beschränkungen enthält, gibt die API die folgende Fehlermeldung zurück:„Die Anzahl der Mbox-Parameter darf 100 nicht überschreiten.“

## Urls für mbox-Anfragen

**Limit**: 2.083 Zeichen.

Diese Beschränkung beruht auf Längenbeschränkungen für Microsoft Internet Explorer.

## mbox3rdPartyId-Parameter

**Limit**: 60 Zeichen.

## Angebotsnamen

**Limit**: 250 Zeichen.

## Angebotsgröße

**Limit**: Die folgenden Größenbeschränkungen gelten für Angebote:

* 256 KB für HTML-Angebote.
* 64 KB für visuelle Angebote aus der Benutzeroberfläche.
* 512 KB aus der API.

Wenn Sie eine globale Mbox verwenden, gilt die Beschränkung für den gesamten Satz an Inhalten, die für die Seite zurückgegeben werden. Die Beschränkung der Angebotsseite optimiert die Seitenladezeit. Wenn der Grenzwert überschritten wird, wird folgende Meldung angezeigt:

„Der Inhalt für das Erlebnis ist für die Bereitstellung zu groß. Ändern Sie das Erlebnis, damit weniger Seiten-Code betroffen ist.“

## orderId-Parameter

**Limit**: 120 Zeichen.

Empfohlene Beschränkung. 

## orderTotal-Parameter

**Limit**: 120 Zeichen.

Empfohlene Beschränkung. 

## productPurchasedId-Parameter

**Limit**: 47 Zeichen pro kommagetrennten Wert.

Alles mehr wird durch das System abgeschnitten.

## Wiederverwendbare Zielgruppen/Konto

**Limit**: 75 Zielgruppen.

Empfohlene Beschränkung. Wenn Sie zu viele haben, wird es auf der Oberfläche zu JavaScript-Timeouts kommen.

## Skript-Profileingabefeld in der Target-Benutzeroberfläche

**Limit**: 2.000 Zeichen.

Empfohlene Beschränkung. Abhängig von der Größe der verschlüsselten Zeichenfolge, die viel länger als die Rohzeichenfolge sein kann. Wenn die Zeichenfolge zu groß ist, tritt ein Fehler auf, bevor die Zeichenfolge an Adobe Target weitergeleitet wird.

## Skript-Profilnamen

**Limit**: 50 Zeichen.

## Skript-Profilwerte

**Limit**: 2.048 Zeichen.

Aus Leistungsgründen empfehlen wir einen Rückgabewert, der nicht länger als 256 Zeichen ist.

Wenn für einen String-Rückgabewert die Größe des Rückgabewerts 2.048 Zeichen überschreitet, wird das Skript vom System deaktiviert.

Wenn für einen Array-Rückgabewert die Größe der verketteten Werte des Arrays 2.048 Zeichen überschreitet, wird das Skript vom System deaktiviert.

## Targeting-Bedingungen

**Limit**: 1.000 Werte.

Empfohlene Beschränkung. Dies bezieht sich auf die Anzahl der durch eine Zeile getrennten Werte im Targeting-Textbereich, z. B. die Eingabe von 1.000 Postleitzahlen in eine Postleitzahl-Zielgruppe.