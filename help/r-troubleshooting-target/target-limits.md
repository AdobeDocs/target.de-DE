---
keywords: character limit;mbox parameters;batch delivery api;profile parameters;limits;built in profiles;maximum;limit;constraint;character;best practice;orderid;orderTotal;mbox3rdPartyID;category;categoryID
description: Informationen zu Zeichen- und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.) für Aktivitäten und andere Elemente in Adobe Target.
title: Beschränkungen
feature: reference general
topic: Standard
uuid: 603fb800-a26c-43ec-b2d9-ef7a8ed8721e
translation-type: tm+mt
source-git-commit: d3c8c328e122eaf7bf1829fc46f55ef23ad187e6
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 77%

---


# Beschränkungen{#limits}

Informationen zu Zeichen- und anderen Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.) für Aktivitäten und andere Elemente in Adobe Target.

>[!NOTE]
>
>Die unten aufgeführten Limits sollten als „harte“ Begrenzungen erachtet werden, sofern sie nicht als „empfohlen“ gekennzeichnet sind.
>
>Wenn die als „empfohlen“ gekennzeichneten Limits erreicht oder überschritten werden, kann sich die Leistung verlangsamen. Langsame Ladezeiten der Oberfläche können ebenfalls durch eine sehr komplexe Aktivität bedingt sein, die viele Zielgruppen, Ziele und Erlebnisse enthält.
>
>Hochkomplexe Aktivitäten sollten mit Adobe Consulting geprüft und in einer eingeschränkten Umgebung getestet werden, bevor sie zur Produktion freigegeben werden.

## Aktivitäten

**Empfohlenes Limit**: 10.000 aktive Live-Aktivitäten.

**Empfohlene Beschränkung**: 10.000 aktive gespeicherte (und nicht beendete) Aktivitäten.

## Aktivitätsname

**Limit**: 250 Zeichen.

## Zielgruppennamen

**Limit**: 255 Zeichen.

## Zielgruppen

**Limit**: 50 Zielgruppen pro Mbox, Metrik oder Erlebnis.

## Audiencen, pro Konto wiederverwendbar

**Empfohlenes Limit**: 20,000 Zielgruppen.

## categoryId-Parameter

**Limit**: 128 Zeichen.

## Kundenattributnamen

**Maximal**: 250 Zeichen über Feed oder API.

## Kundenattribut-Alias-ID

**Limit**: 50 Zeichen.

## Kundenattribute, hochladen

* **Maximale Dateigröße für jeden Upload mit der HTTP-Methode**: 100 MB.
* **maximale Dateigröße für jeden Upload mit der FTP-Methode**: 4 GB
* **Anzahl der Attribute, die abonniert** werden dürfen: 5 für [!DNL Target Standard] und 200 für [!DNL Target Premium].

## Benutzerdefinierte Entitätsattribute

**Limit**: Die maximale Länge hängt von der Sprache ab.

* 15.000 Zeichen (Einzelwert, Ein- und Zwei-Byte-Sprachen)
* 500 Werte, 100 Zeichen pro Wert (mehrere Werte)

Die maximale Länge von benutzerdefinierten Attributen für Einzelwert-Entitäten beträgt 15.000 Zeichen (für 1- und 2-Byte-UTF-8-kodierte Sprachen wie Englisch und andere Sprachen mit lateinischen Skriptbuchstaben) oder 10.000 Zeichen (für 3-Byte-UTF-8-kodierte Sprachen wie Chinesisch, Japanisch und Koreanisch).

Benutzerdefinierte Attribute mit mehreren Werten dürfen maximal 500 Werte enthalten. Jeder einzelne Wert ist auf 100 Zeichen begrenzt. Die Gesamtanzahl der Zeichen für alle Werte muss den Beschränkungen für die maximale Länge von benutzerdefinierten Attributen für Einzelwertentitäten entsprechen (siehe oben).

## EntityID-Parameter

**Limit**: 1.000 Zeichen.

## excludedIds {#excludedid}

**Limit**: 5 KB für POST-Anforderungen. 2.083 Zeichen minus der Länge der URL für GET-Anforderungen.

Bei GET-Anforderungen beträgt der Grenzwert für das Back-End zwar 5 KB, aufgrund der Tatsache, dass Microsoft Internet Explorer die URL auf 2.083 Zeichen begrenzt, beträgt der tatsächliche Grenzwert 2.083 Zeichen minus der aktuellen Länge der URL.

## Erlebnisnamen

**Limit**: 50 Zeichen.

## Erlebnisse pro Aktivität

**Limit**: 2.000 Erlebnisse pro Erlebnis-Targeting (XT), A/B-Test, Multivarianz-Test (MVT) und automatischem Targeting.

30.000 Erlebnisse pro automatisierter Personalisierung (AP).

## In-Mbox-Profilattributwert

**Limit**: 256 Zeichen.

Längere Werte werden abgeschnitten.

## In-Mbox-Profilnamen

**Limit**: 128 Zeichen.

## mbox-Namen

**Limit**: 250 Zeichen.

## Mbox-Parameter

**Limit**: Die folgenden Beschränkungen gelten für Mbox-Parameter:

Für Standard-Mbox-Aufrufe:
* Mbox-Parameter: 500 Parameter pro Mbox.
* Profil-Parameter: 500 Parameter Profil-Parameter pro mbox.
* Andere Parameter (URL, verweisende URL usw.): 50 Parameter pro Mbox für jeden Parametertyp.

Diese Beschränkungen gelten, sofern die Anfrage nicht durch Webbrowser-Beschränkungen gekürzt wird.

Wenn Sie die Batch Versand API verwenden, beträgt die Beschränkung 50 Mboxes pro Batch-Anforderung.

Wenn Sie die [Batch-Bereitstellungs-API](https://developers.adobetarget.com/api/#server-side-batch-delivery) im Mobile Services SDK verwenden, sind die Beschränkung von 50 Mbox-Parametern, 50 Profilparametern und 50 für andere Parametertypen Einschränkungen der API selbst. Es ist nicht möglich, mit der Batch-Bereitstellungs-API Anfragen zu senden, die mehr als diese Anzahl von Parametern enthalten. Wenn eine Anforderung mehr als diese Beschränkungen enthält, gibt die API die folgende Fehlermeldung zurück:

&quot;Die Anzahl der mboxParameters darf 50 nicht überschreiten.&quot;

Für Endpunkte festgelegte Grenzwerte:

Batch-mbox v2:
* mbox-Parameter 100
* Mbox-Parametername max. Länge 128
* mbox-Parameterwert darf nicht null sein
* mbox-Parameterwert 5000
* profil-Parameter 50
* profil-Parametername max. Länge 128
* profil-Parameterwert darf nicht null sein
* profil-Parameterwert max. Länge 256

Versand-API-Endpunkt
* mbox-Parameter 50
* Mbox-Parametername max. Länge 128
* mbox-Parameterwert darf nicht null sein
* mbox-Parameterwert 5000
* profil-Parameter 50
* profil-Parametername max. Länge 128
* profil-Parameterwert darf nicht null sein
* profil-Parameterwert max. Länge 256

## URL-Adressen zur Mbox-Anfrage

**Limit**: 2.083 Zeichen.

Diese Beschränkung beruht auf URL-Längenbeschränkungen für Microsoft Internet Explorer.

## mbox3rdPartyId-Parameter

**Limit**: 60 Zeichen.

## Angebotsnamen

**Limit**: 250 Zeichen.

## Angebotsgröße

**Limit**: Die folgenden Größenbeschränkungen gelten für Angebote:

* 256 KB für HTML-Angebote.
* 64 KB für visuelle Angebote aus der Benutzeroberfläche.
* 512 KB aus der API.

Bei der Verwendung einer globalen Mbox gilt die Beschränkung für den kompletten Satz an zurückgegebenen Inhalten für die Seite. Die Beschränkung der Angebotsseite optimiert die Seitenladezeit. Wenn der Grenzwert überschritten wird, wird folgende Meldung angezeigt:

„Der Inhalt für das Erlebnis ist für die Bereitstellung zu groß. Ändern Sie das Erlebnis, damit weniger Seiten-Code betroffen ist.“

## Angebote

**Empfohlenes Limit**: Insgesamt 50.000 Angebote.

## orderId-Parameter

**Empfohlenes Limit**: 120 Zeichen.

## orderTotal-Parameter

**Empfohlenes Limit**: 120 Zeichen.

## productPurchasedId-Parameter

**Limit**: 47 Zeichen pro kommagetrenntem Wert.

Eine längere Zeichenfolge wird vom System begrenzt.

## Profilskripte

**Empfohlene Beschränkung aktiver Profil-Skripte**: 300

**Empfohlene Obergrenze für Profil-Skripten pro Konto**: 2.000

**Recommendations zur Beschränkung der Komplexität** von Profil-Skripten: Profil-Skripten können eine begrenzte Anzahl von Anweisungen ausführen. Weitere Informationen finden Sie unter [Bewährte Verfahren](/help/c-target/c-visitor-profile/profile-parameters.md#best) in *Profil-Attributen*.

## Properties

**Empfohlenes Limit**: 5.000 Properties.

## Berichtszielgruppen/-segmente

**Limit**: 50 Berichtszielgruppen/-segmente pro Aktivität.

## Skriptprofil-Eingabefeld in der Target-Benutzeroberfläche

**Empfohlenes Limit**: 2.000 Zeichen.

Abhängig von der Größe der verschlüsselten Zeichenfolge, die viel länger als die Rohzeichenfolge sein kann. Wenn die Zeichenfolge zu groß ist, tritt ein Fehler auf, bevor die Zeichenfolge an Adobe Target weitergeleitet wird.

## Skript-Profilnamen

**Limit**: 50 Zeichen.

## Skript-Profilwerte

**Limit**: 2.048 Zeichen.

Aus Leistungsgründen empfehlen wir einen Rückgabewert, der nicht länger als 256 Zeichen ist.

Wenn für einen String-Rückgabewert die Größe des Rückgabewerts 2.048 Zeichen überschreitet, wird das Skript vom System deaktiviert.

Wenn für einen Array-Rückgabewert die Größe der verketteten Werte des Arrays größer als 2.048 Zeichen ist, wird das Skript vom System deaktiviert.

## Erfolgsmetriken

**Limit**: 200 pro Aktivität.

## Targeting-Bedingungen

**Empfohlenes Limit**: 1.000 Werte.

Dies bezieht sich auf die Anzahl der durch eine Zeile getrennten Werte im Targeting-Textbereich, z. B. die Eingabe von 1.000 Postleitzahlen in eine Postleitzahl-Zielgruppe.

## Targeting-Regeln

**Empfohlene Beschränkung**: 2.500 Zeichen pro Targeting-Regelwert.

**Empfohlenes Limit**: 30.000 einmalige Werte pro Zielgruppe in Targeting-Regeln.

**Empfohlenes Limit**: 100.000 einmalige Werte für Targeting-Regeln pro Aktivität.

