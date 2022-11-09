---
keywords: zeichenbeschränkung;mbox-parameter;batch-bereitstellungs-api;profilparameter;beschränkungen;integrierte profile;maximum;beschränkung;bedingung;zeichen;best practice;orderid;orderTotal;mbox3rdPartyID;kategorie;categoryID;fehlerbehebung
description: Anzeigen einer Liste von Zeichenbeschränkungen und anderen Beschränkungen, die Aktivitäten und andere Elemente in [!DNL Adobe Target].
title: Zeichen-, Größen- und andere Beschränkungen in [!DNL Adobe Target]?
feature: Troubleshooting
mini-toc-levels: 3
exl-id: b318ab16-1382-4f3a-8764-064adf384d6b
source-git-commit: 8890d29a71506095a166321e324a000b5ad862a6
workflow-type: tm+mt
source-wordcount: '1348'
ht-degree: 97%

---

# Beschränkungen

Zeichen- und andere Beschränkungen (Angebotsgröße, Zielgruppen, Profile, Werte, Parameter usw.) die Aktivitäten und andere Elemente in [!DNL Adobe Target] betreffen.

>[!NOTE]
>
>Die unten aufgeführten Limits sollten als „harte“ Begrenzungen erachtet werden, sofern sie nicht als „empfohlen“ gekennzeichnet sind.
>
>Wenn die als „empfohlen“ gekennzeichneten Limits erreicht oder überschritten werden, kann sich die Leistung verlangsamen. Langsame Ladezeiten der Oberfläche können ebenfalls durch eine sehr komplexe Aktivität bedingt sein, die viele Zielgruppen, Ziele und Erlebnisse enthält.
>
>Hochkomplexe Aktivitäten sollten mit [!DNL Adobe] Consulting geprüft und in einer eingeschränkten Umgebung getestet werden, bevor sie zur Produktion freigegeben werden.

## Aktivitäten

### Aktivitätsname

* **Limit**: 250 Zeichen.

### Anzahl der Aktivitäten pro Konto

* **Empfohlenes Limit**: 10.000 aktive Live-Aktivitäten.

* **Empfohlenes Limit**: 10.000 aktive gespeicherte (und noch nicht beendete) Aktivitäten.

## Target-API-Aufrufe

* **Beschränkung**: 50 Aufrufe pro Minute für die APIs zur Aktualisierung von Admin-, Berichts- und Massenprofilen. Diese Beschränkung gilt nicht für die APIs zu Versand und einfacher Profilaktualisierung.

   Wenn Sie mehr als 50 API-Aufrufe pro Minute ausführen, gibt [!DNL Target] die Fehlermeldung „503 HTTP-Status“ zurück.

## Zielgruppen

### Zielgruppennamen

* **Limit**: 255 Zeichen.

### Zielgruppen pro Konto, wiederverwendbar

* **Empfohlenes Limit**: 20.000 Zielgruppen.

### Anzahl der Zielgruppen pro Mbox, Metrik oder Erlebnis

* **Limit**: 50 Zielgruppen

## categoryId-Parameter

* **Limit**: 256 Zeichen.

## Inhaltsbereitstellung {#content-delivery}

* **Limit**: 100 gleichzeitige [!DNL Target]-Anfragen zur Inhaltsbereitstellung pro Benutzersitzung.

   Wenn ein Kunde 100 gleichzeitige [!DNL Target]-Anfragen zur Inhaltsbereitstellung für eine bestimmte Benutzersitzung überschreitet, werden alle nachfolgenden Anfragen für diese Benutzersitzung blockiert. Zwei oder mehr Anfragen gelten als gleichzeitig, wenn sie alle an den [!DNL Target]-Server gesendet werden, bevor die Antwort für eine dieser Anfragen empfangen wird. [!DNL Target] verarbeitet gleichzeitige Anfragen für dieselbe Sitzung sequenziell.

* **Fehlerverhalten**:

   * Bereitstellungs-API und Batch-Mbox v2:
      * Fehler-Code: HTTP 420 – zu viele Anfragen
      * Fehlermeldung: „Zu viele Anfragen mit derselben Sitzungs-ID“
   * Legacy-mBox-API:
      * Standardinhalt mit Kommentar „Zu viele Anfragen mit derselben Sitzungs-ID“
   * at.js:
      * Standardinhalt wird angezeigt



## Kundenattribute

### Kundenattributnamen

* **Limit**: 250 Zeichen über Feed oder API.

### Kundenattribut-Alias-ID

* **Limit**: 50 Zeichen.

### Kundenattribute, Upload

* **Maximale Dateigröße pro Upload über HTTP**: 100 MB.
* **Maximale Dateigröße pro Upload über FTP**: 4 GB.
* **Anzahl der zum Abonnieren zulässigen Attribute**: 5 für [!DNL Target Standard] und 200 für [!DNL Target Premium].

## Entitäten

### Anzahl der Entitäten

* Die maximale Anzahl von Entitäten, die in einem Entwurf referenziert werden können, egal ob hart codiert oder in Schleife, beträgt 99.
* Als empfohlenes Limit für die beste Performance gilt: Im Katalog sollten weniger als eine Million Elemente pro Umgebung und weniger als zehn Millionen Elemente in allen Umgebung gespeichert sein.
* Das obere Limit beträgt zehn Millionen Elemente pro Umgebung und 100 Millionen Elemente für alle Umgebungen. Wenn Sie zwischen einer Million und zehn Millionen Elemente pro Umgebung haben, wird die Leistung der Benutzeroberfläche [!UICONTROL Katalogsuche] beeinträchtigt. [!DNL Target Recommendations] produziert und sendet jedoch weiterhin Empfehlungen.

### Benutzerdefinierte Entitätsattribute

* **Benutzerdefinierte Entitätsattribute**: 100.

* **Zeichenbeschränkung**: Die maximale Zeichenlänge hängt von der Sprache ab.

   * 15.000 Zeichen (Einzelwert, Ein- und Zwei-Byte-Sprachen)
   * 500 Werte, 100 Zeichen pro Wert (mehrere Werte)

   Die maximale Länge von benutzerdefinierten Attributen für Einzelwert-Entitäten beträgt 15.000 Zeichen (für 1- und 2-Byte-UTF-8-codierte Sprachen wie Englisch und andere Sprachen mit lateinischen Skriptbuchstaben) oder 10.000 Zeichen (für 3-Byte-UTF-8-codierte Sprachen wie Chinesisch, Japanisch und Koreanisch).

   Benutzerdefinierte Attribute mit mehreren Werten dürfen maximal 500 Werte enthalten. Jeder einzelne Wert ist auf 100 Zeichen begrenzt. Die Gesamtanzahl der Zeichen für alle Werte muss den Beschränkungen für die maximale Länge von benutzerdefinierten Attributen für Einzelwertentitäten entsprechen (siehe oben).

### entity.id

* **Beschränkung für Implementierungen, die die Erfassung von Kaufinformationen erfordern**: 50 Zeichen.

   Diese Beschränkung wird erzwungen, da der mBox-Parameter `productPurchasedId` die entity.ids erfasst, wodurch die Zeichenanzahl auf 50 begrenzt wird.

* **Beschränkung für Implementierungen, für die nur ansichtsbasierte Algorithmen erforderlich sind**: 1.000 Zeichen.

   Zu den ansichtsbasierten Algorithmen gehören „Ansicht/Ansicht“, „Am häufigsten angesehen“, „Zuletzt angezeigt“ usw.

## excludedIds {#excludedid}

* **Limit**: 5 KB für POST-Anforderungen. 2.083 Zeichen minus der Länge der URL für GET-Anforderungen.

   Bei GET-Anforderungen beträgt der Grenzwert für das Backend zwar 5 KB, aufgrund der Tatsache, dass Microsoft Internet Explorer die URL auf 2.083 Zeichen begrenzt, beträgt der tatsächliche Grenzwert 2.083 Zeichen minus der aktuellen Länge der URL.

## Erlebnisse

### Erlebnisnamen

* **Limit**: 50 Zeichen.

### Erlebnisse pro Aktivität

* **Limit**: 2.000 Erlebnisse pro [!UICONTROL Erlebnis-Targeting] (XT), [!UICONTROL A/B-Test], [!UICONTROL Multivarianz-Test] (MVT) und [!UICONTROL Automatisches Targeting] Aktivität.

   30.000 Erlebnisse pro Automated Personalization (AP).

### Änderungen pro Erlebnis

* **Limit**: 50 pro Erlebnis für jede Aktivität

## Mboxes

### In-Mbox-Profilattributwert

* **Limit**: 256 Zeichen.

   Längere Werte werden abgeschnitten.

### In-Mbox-Profilnamen

* **Limit**: 128 Zeichen.

### Mbox-Namen

* **Limit**: 250 Zeichen.

### Mbox-Parameter {#mbox-parameters}

* **Limit**: Die folgenden Beschränkungen gelten für Mbox-Parameter:

   Für Standard-Mbox-Aufrufe:

   * Mbox-Parameter: 500 Parameter pro Mbox.
   * Profilparameter: 500 Profilparameter pro Mbox.
   * Andere Parameter (URL, verweisende URL usw.): 50 Parameter pro Mbox für jeden Parametertyp.

   Diese Beschränkungen gelten, sofern die Anfrage nicht durch Webbrowser-Beschränkungen gekürzt wird.

   Bei Verwendung der Batch-Bereitstellungs-API beträgt die Beschränkung 50 Mboxes pro Batch-Anforderung.

   Wenn Sie die Batch-Bereitstellungs-API im Mobile Services SDK verwenden, sind die Beschränkung von 50 Mbox-Parametern, 50 Profilparametern und 50 für andere Parametertypen Einschränkungen der API selbst. Es ist nicht möglich, mit der Batch-Bereitstellungs-API Anfragen zu senden, die mehr als diese Anzahl von Parametern enthalten. Bei einer Überschreitung dieser Beschränkungen gibt die API die folgende Fehlermeldung zurück:

   „Die Anzahl der mboxParameters darf 50 nicht überschreiten.“

   Für Endpunkte festgelegte Beschränkungen:

   **Batch mbox v2**:

   * Mbox-Parameter: 100
   * Maximale Länge des Mbox-Parameternamens: 128
   * Der Mbox-Parameterwert darf nicht null sein.
   * Mbox-Parameterwert: 5000
   * Profilparameter: 50
   * Maximale Länge des Profilparameternamens: 128
   * Der Profilparameterwert darf nicht null sein.
   * Maximale Länge des Profilparameterwerts: 256

   **Bereitstellungs-API – Endpunkt**:

   * Mbox-Parameter: 100
   * Maximale Länge des Mbox-Parameternamens: 128
   * Der Mbox-Parameterwert darf nicht null sein.
   * Mbox-Parameterwert: 5000
   * Profilparameter: 50
   * Maximale Länge des Profilparameternamens: 128
   * Der Profilparameterwert darf nicht null sein.
   * Maximale Länge des Profilparameterwerts: 256



### URL-Adressen zur Mbox-Anfrage

* **Limit**: 2.083 Zeichen.

   Diese Beschränkung beruht auf URL-Längenbeschränkungen für Microsoft Internet Explorer.

### mbox3rdPartyId-Parameter

* **Limit**: 256 Zeichen.

## Angebote

### Angebotsnamen

* **Limit**: 250 Zeichen.

### Anzahl der Angebote

* **Empfohlenes Limit**: Insgesamt 50.000 Angebote.

### Angebotsgröße {#offer-size}

Die folgenden Größenbeschränkungen gelten für Angebote:

* 1024 KB für HTML-Angebote.
* 1024 KB (pro Erlebnis) für visuelle Angebote der Benutzeroberfläche.
* 1024 KB aus der API.

   Bei der Verwendung einer globalen Mbox gilt die Beschränkung für den kompletten Satz an zurückgegebenen Inhalten für die Seite. Die Beschränkung der Angebotsseite optimiert die Seitenladezeit. Wenn der Grenzwert überschritten wird, wird folgende Meldung angezeigt:

   „Der Inhalt für das Erlebnis ist für die Bereitstellung zu groß. Ändern Sie das Erlebnis, damit weniger Seiten-Code betroffen ist.“

## orderId-Parameter

* **Empfohlenes Limit**: 120 Zeichen.

## orderTotal-Parameter

* **Empfohlenes Limit**: 120 Zeichen.

## productPurchasedId-Parameter

* **Limit**: 50 Zeichen pro kommagetrenntem Wert, 250 Zeichen insgesamt. Einzelwerte mit einer Länge von mehr als 50 Zeichen werden vom System abgeschnitten. Gesamtlängen über 250 Zeichen führen zu einem Fehler 400.

## Profilskripte

* **Empfohlenes Limit für aktive Profilskripte (die aktiviert sind)**: 300

* **Empfohlenes Limit für alle Profilskripte eines Kontos**: 2.000

* **Empfehlungen zur Reduzierung der Komplexität von Profilskripten**: Die Anzahl der durch Profilskripte ausführbaren Anweisungen ist begrenzt. Weitere Informationen finden Sie unter [Best Practices](/help/main/c-target/c-visitor-profile/profile-parameters.md#best) im Abschnitt *Profilattribute*.

## Eigenschaften

* **Empfohlenes Limit**: 5.000 Eigenschaften.

## Berichtszielgruppen/-segmente

* **Limit**: 50 Berichtszielgruppen/-segmente pro Aktivität.

## Skriptprofil-Eingabefeld in der [!DNL Target]-Benutzeroberfläche

* **Empfohlenes Limit**: 2.000 Zeichen.

   Abhängig von der Größe der verschlüsselten Zeichenfolge, die viel länger als die Rohzeichenfolge sein kann. Wenn die Zeichenfolge zu groß ist, tritt ein Fehler auf, bevor die Zeichenfolge an Adobe Target weitergeleitet wird.

## Skriptprofile

### Skriptprofilnamen

* **Limit**: 50 Zeichen.

### Skriptprofilwerte

* **Limit**: 2.048 Zeichen.

   Aus Leistungsgründen empfehlen wir einen Rückgabewert, der nicht länger als 256 Zeichen ist.

   Wenn für einen String-Rückgabewert die Größe des Rückgabewerts 2.048 Zeichen überschreitet, wird das Skript vom System deaktiviert.

   Wenn für einen Array-Rückgabewert die Größe der verketteten Werte des Arrays größer als 2.048 Zeichen ist, wird das Skript vom System deaktiviert.

## Erfolgsmetriken

* **Limit**: 200 pro Aktivität.

## Targeting

### Targeting-Bedingungen

* **Empfohlenes Limit**: 1.000 Werte.

   Dies bezieht sich auf die Anzahl der durch eine Zeile getrennten Werte im Targeting-Textbereich, z. B. die Eingabe von 1.000 Postleitzahlen in eine Postleitzahl-Zielgruppe.

### Targeting-Regeln {#targeting-rules}

* **Empfohlenes Limit**: 2.500 Zeichen pro Targeting-Regelwert.
* **Empfohlenes Limit**: 50,000 einmalige Werte pro Zielgruppe in Targeting-Regeln.
* **Empfohlenes Limit**: 100.000 einmalige Werte für Targeting-Regeln pro Aktivität.
