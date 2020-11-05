---
keywords: faq;frequently asked questions;analytics for target;a4T;redirect;redirect offer;adobe-mc-sdid;adobe_mc_ref
description: Dieses Thema enthält Antworten auf häufig zum Einsatz von Umleitungsangeboten bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.
title: Umleitungsangebote – Häufig gestellte Fragen zu A4T
feature: a4t troubleshooting
topic: Standard
uuid: a45cef89-3003-4177-bf84-3d5a486b950d
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 94%

---


# Umleitungsangebote – Häufig gestellte Fragen zu A4T{#redirect-offers-a-t-faq}

Dieses Thema enthält Antworten auf häufig zum Einsatz von Umleitungsangeboten bei der Verwendung von Analytics als Berichtsquelle für Target (A4T) gestellte Fragen.

## Unterstützt Analytics for Target (A4T) Umleitungsangebote? {#section_46B8B03ED4D542C6AD875F5F61176298}

Ja – vorausgesetzt, Ihre Implementierung verwendet [!DNL at.js]. Ihre Implementierung muss jedoch die unten aufgeführten Mindestanforderungen erfüllen, um [Weiterleitungsangebote](/help/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in Aktivitäten zu verwenden, die Analytics als Berichtsquelle verwenden.

>[!NOTE]
>
>Es gibt ein bekanntes Problem, bei dem einer begrenzten Anzahl von Kunden mit Redirects mit A4T ein höherer Prozentsatz an aufgetrennten Treffern angezeigt wird. Siehe [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Was sind die erforderlichen Mindestanforderungen, um Umleitungsangebote in A4T nutzen zu können? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

Ihre Implementierung muss folgende Mindestanforderungen erfüllen:

* Experience Cloud-Besucher-ID-Service: [!DNL visitorAPI.js], Version 2.3.0 oder neuer.
* Adobe Analytics: [!DNL appMeasurement.js] Version 2.1.
* Adobe Target: [!DNL at.js], Version 1.6.2 oder neuer.

   Die [!DNL mbox.js] Bibliothek unterstützt keine Umleitungsangebote in A4T. Ihre Implementierung muss [!DNL at.js] verwenden.

Die drei Bibliotheken müssen sowohl auf der Seite mit dem Weiterleitungsangebot als auch auf der Seite, auf die der Besucher umgeleitet wird, enthalten sein.

## Warum gibt es manchmal Datendiskrepanzen zwischen A4T und Analytics?

Es werden einige Datendiskrepanzen erwartet. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

## Warum werden manchmal Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt?  {#section_B8F6CC2190B84CF08D945E797C5AF07B}

Wenn die at.js-Version 1.6.3 oder höher verwendet wird, ist dies kein Problem. Diese Race-Bedingung betrifft nur Kunden, die frühere Versionen verwenden. Das Target-Team behält zwei Versionen von at.js: die aktuelle Version und die davor. Führen Sie bei Bedarf ein Upgrade von at.js durch, um sicherzustellen, dass Sie eine [unterstützte Version](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) ausführen.

Wenn Sie eine frühere, nicht unterstützte Version von at.js verwenden, besteht die Möglichkeit, dass eine Race-Bedingung eintritt, die dazu führen kann, dass der Analytics-Aufruf ausgelöst wird, bevor die Umleitung auf der ersten Seite ausgeführt wird. Dies kann dazu führen, dass die Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt werden. Diese Situation führt zu einem zusätzlichen Seitenaufruf auf der ersten Seite, selbst wenn der Besucher diese erste Seite nie wirklich „gesehen“ hat.

Es wird empfohlen, den formularbasierten Composer zum Erstellen einer Redirect-Aktivität zu verwenden, um die Geschwindigkeit der Seitenumleitung zu erhöhen. Das beeinflusst, wo der Code auf der Seite ausgeführt wird. Es wird zudem die Erstellung eines Umleitungsangebots für jeden Besuch einschließlich des Standardbesuchs empfohlen, wobei die Umleitung zur ursprünglichen Seite zurückführen würde. Dadurch wird gewährleistet, dass im Falle von Fehlzählungen alle Besuche berücksichtigt werden, sodass Berichte und Analysen für den Test weiterhin gültig sind.

Ein Grund für die Verwendung von Umleitungsangeboten für alle Erlebnisse in der Aktivität, einschließlich des Standarderlebnisses (Kontrollerlebnis), besteht darin, dieselben Bedingungen für alle Erlebnisse zu verwenden. Wenn das Standarderlebnis beispielsweise kein Umleitungsangebot enthält, aber die anderen Erlebnisse Umleitungsangebote haben, stellt die Geschwindigkeit des Erlebnisses ohne Umleitungsangebot einen Vorteil dar. Umleitungsangebote werden nur für temporäre Szenarien empfohlen, z. B. Tests. Umleitungsangebote werden nicht für permanente Szenarien wie die Personalisierung empfohlen. Nachdem Sie den „Gewinner“ ermittelt haben, sollten Sie die Umleitung entfernen, um die Seitenladeleistung zu verbessern.

Weitere Informationen zu diesem Problem finden Sie in dem Informationen zu „Weiterleitungsangeboten“ unter [Bekannte Probleme](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Kann ich Umleitungsangebote in A4T nutzen, wenn ich die JavaScript-Bibliothek mbox.js verwende? {#section_D2A8B182B7254D61A8BB2BCBA0C0F64A}

Die [!DNL mbox.js] Bibliothek unterstützt keine Umleitungsangebote in A4T. Ihre Implementierung muss [!DNL at.js] verwenden.

## Werden Visual Experience Composer (VEC) und Form-Based Experience Composer unterstützt? {#section_FDA26FE7909B48539DA770559E687677}

Ja, beide Composer werden unterstützt, solange Sie die integrierten Umleitungsangebote verwenden.

Wenn Sie für die Umleitung Ihren eigenen benutzerdefinierten Code verwenden, müssen Sie sicherstellen, dass Sie die beiden neuen Parameter eingeben, die Umleitungs-URLs zugeordnet sind (`adobe_mc_sdid` und `adobe_mc_ref`, Erklärung weiter unten).

## Welche neuen Abfrage String-Parameter wurden zu den Umleitungs-URLs hinzugefügt? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

Die folgenden Abfrage String-Parameter sind Umleitungsangeboten zugeordnet:

| Parameter | Beschreibung |
|--- |--- |
| `adobe_mc_sdid` | Der Parameter `adobe_mc_sdid` gibt die Supplemental Data Id (SDID) und Experience Cloud-Organisations-ID von der Standardseite an die neue Seite weiter, damit A4T die Target-Anfrage auf der Standardseite mit der Analytics-Anfrage auf der neuen Seite „zusammenheften“ kann. |
| `adobe_mc_ref` | Der Parameter `adobe_mc_ref` gibt die verweisende URL der Standardseite an die neue Seite weiter. Bei der Verwendung mit AppMeasurement.js Version 2.1 (oder neuer) verwendet Analytics diesen Parameterwert als verweisende URL auf der neuen Seite. |

Diese Parameter werden automatisch zu den Umleitungs-URLs hinzugefügt, wenn die integrierten Umleitungsangebote in VEC und in Form-Based Experience Composer verwendet werden, wenn der Besucher-ID-Service auf der Seite implementiert ist. Wenn Sie Ihren eigenen benutzerdefinierten Code in VEC und in Form-Based Experience Composer verwenden, müssen Sie sicherstellen, dass Sie diese Parameter mit Ihrem benutzerdefinierten Code weitergeben.

## Meine Webserver entfernen diese Parameter aus meinen URLs, was soll ich tun?  {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

You will need to work with your IT team to have these parameters ( `adobe_mc_sdid` and `adobe_mc_ref`) allowlisted.

## Was ist, wenn ich A4T nicht für meine Umleitungsaktivitäten verwende und nicht möchte, dass diese zusätzlichen Parameter zu meinen URLs hinzugefügt werden? {#section_9E608D75FF9349FE96C65FEDD7539F45}

Wenn Sie A4T nicht mit Ihrer Umleitungsaktivität verwenden, der Besucher-ID-Service bei Ihnen implementiert ist und Sie nicht möchten, dass diese Parameter automatisch zu Ihren URLs hinzugefügt werden, müssen Sie eine benutzerdefiniert codierte Umleitung verwenden.

Als Best Practice empfiehlt es sich jedoch, den Parameter `adobe_mc_ref` in der URL zu behalten, um die verweisenden Informationen korrekt an [!DNL Analytics] weiterzugeben.

## Warum sind die Parameter adobe_mc_ref und adobe_mc_sdid in meiner Implementierung doppelt URL-kodiert? {#section_5EFE5F012B944C40865731EA18E7E79E}

Wenn Sie A4T und Weiterleitungsangebote verwenden, hängt Target die Parameter `adobe_mc_ref` und `adobe_mc_sdid` an die URL an. Diese Werte sind bereits URL-kodiert. Meistens funktioniert alles wie erwartet. Möglicherweise haben einige Kunden jedoch Systeme zur Lastverteilung oder WEB-Server, die versuchen, die Abfrage-String-Parameter erneut zu kodieren.

Aufgrund dieser doppelten Kodierung kann die Besucher-API den SDID-Wert nicht abrufen, wenn sie versucht, den Wert `adobe_mc_sdid` zu entschlüsseln, und sie erstellt dann eine neue SDID. Dies führt dazu, dass falsche SDID-Werte an Target und Analytics gesendet werden und Ihnen in Analytics-Berichten eine ungleiche Verteilung für Umleitungen angezeigt wird.

We recommend that you talk to their IT team to ensure that `adobe_mc_ref` and `adobe_mc_sdid` are allowlisted so that these values are not transformed in any way.

## Warum muss die verweisende URL an die neue Seite weitergegeben werden? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

Suppose a visitor clicks a link on [!DNL `www.google.com`] to your homepage (`www.mysite.com/index.html`) on which a redirect activity is live and is then redirected to a new page (`www.mysite.com/index2.html`).

Bisher hat die [!DNL Analytics]-Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.mysite.com/index.html`] statt von [!DNL `www.google.com`] gemeldet. Dies führte zu ungenauen Berichten in [!DNL Analytics] im Zusammenhang mit den verweisenden URLs (beispielsweise Marketingkanalberichte). Somit berücksichtigten die Berichte nicht, dass Sie über [!DNL `www.google.com`] auf die Seite kamen.

Bei [!DNL at.js], Version 0.9.6 (oder neuer) und [!DNL AppMeasurement.js], 2.1 (oder neuer) berichtet die [!DNL Analytics]-Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.google.com`].

## Kann ich benutzerdefinierte/HTML-Weiterleitungsangebote verwenden? {#section_E49F9A83A286488C8F1098A040203D7E}

Nein, Sie müssen für Aktivitäten mit [!DNL Analytics] als Berichterstellungsquelle (A4T) ein integriertes Weiterleitungsangebot verwenden. Aus der Sicht von [!DNL Target] sind HTML-Angebote undurchsichtig: [!DNL Target] kann nicht erkennen, dass ein bestimmter HTML-Abschnitt JavaScript zum Instantiieren einer Weiterleitung enthält.
