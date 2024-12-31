---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Weiterleitung; Weiterleitungsangebot; adobe-mc-sdid; adobe_mc_ref
description: Hier finden Sie Antworten auf Fragen zur Verwendung von Umleitungsangeboten bei der Verwendung von Analytics für  [!DNL Target] A4T). Mit A4T können Sie Analytics-Berichte für - [!DNL Target]  verwenden.
title: Wo finde ich FAQs zu Umleitungsangeboten mit A4T?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 44%

---

# Umleitungsangebote – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf Fragen, die häufig zur Verwendung von Umleitungsangeboten gestellt werden, wenn [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) verwendet wird.

## Unterstützt Analytics for Adobe Target (A4T) Umleitungsangebote? {#section_46B8B03ED4D542C6AD875F5F61176298}

+++Antwort
Ja, wenn Ihre Implementierung [!DNL at.js] verwendet. Ihre Implementierung muss jedoch die unten aufgeführten Mindestanforderungen erfüllen, um [Weiterleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in Aktivitäten zu verwenden, die Analytics als Berichtsquelle verwenden.

+++

## Welche Mindestanforderungen gelten für die Verwendung von Umleitungsangeboten mit A4T? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

+++Antwort
Ihre Implementierung muss die folgenden Mindestanforderungen erfüllen:

* Experience Cloud-Besucher-ID-Service: [!DNL visitorAPI.js], Version 2.3.0 oder neuer.
* Adobe Analytics: [!DNL appMeasurement.js] Version 2.1.
* Adobe Target: [!DNL at.js], Version 1.6.2 oder neuer.

Die drei Bibliotheken müssen sowohl auf der Seite mit dem Weiterleitungsangebot als auch auf der Seite, auf die der Besucher umgeleitet wird, enthalten sein.

+++

## Warum gibt es manchmal Datendiskrepanzen zwischen A4T und Analytics?

+++Antwort
Es sind einige Datendiskrepanzen zu erwarten. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

+++

## Wie kann ich Diskrepanzen bei der Traffic-Verteilung bei der Verwendung von Umleitungsangeboten in A4T-Aktivitäten minimieren? {#discrepancies}

+++Antwort
Eine begrenzte Anzahl von Kunden hat einen höheren Grad an Varianzen in der Traffic-Verteilung gemeldet, wenn Umleitungsangebote in Aktivitäten verwendet werden, die mit [!UICONTROL Analytics for Target] (A4T) konfiguriert wurden.

Beachten Sie Folgendes:

* Eine falsche Reihenfolge der [!DNL Target]- und [!DNL Analytics]-Aufrufe kann zu höheren Varianzgraden führen.

  Der [!DNL Target]-Aufruf muss dem [!DNL Analytics]-Aufruf auf der Quellseite (wo die Umleitung stattfindet) und auf der Zielseite (wo die Umleitung endet) vorangehen.

* Stellen Sie sicher, dass Sie Umleitungsangebote in A4T-Umleitungsaktivitäten verwenden.
* Wenn sich mehrere [!DNL Target]-Ortsanfragen auf der Quellseite befinden (auf der die Umleitung erfolgt), empfiehlt [!DNL Adobe], die Umleitungsaktivität bei der ersten [!DNL Target]-Ortsanfrage auszuführen.

  Das Ausführen der Umleitungsaktivität für die erste [!DNL Target]-Standortanfrage verringert die Wahrscheinlichkeit, dass Aktivitätsqualifikationen für andere [!DNL Target]-Standortanfragen auftreten und im Bericht gezählt werden. Besucherinnen und Besucher, die umgeleitet werden, müssen in den Berichten über andere Aktivitäten nicht gezählt werden, da sie die Erlebnisse nicht sehen.

+++

## Warum werden manchmal Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt?  {#section_B8F6CC2190B84CF08D945E797C5AF07B}

+++Antwort
Bei Verwendung von at.js Version 1.6.3 oder höher ist das Zählen der Seitenansichten auf beiden Seiten kein Problem. Diese Race-Bedingung betrifft nur Kunden, die frühere Versionen verwenden. Das Target-Team behält zwei Versionen von at.js: die aktuelle Version und die davor. Aktualisieren Sie at.js nach Bedarf, um sicherzustellen, dass Sie eine [unterstützte Version“ ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank}.

Wenn Sie eine frühere, nicht unterstützte Version von at.js verwenden, besteht die Möglichkeit, dass eine Race-Bedingung eintritt, die dazu führen kann, dass der Analytics-Aufruf ausgelöst wird, bevor die Umleitung auf der ersten Seite ausgeführt wird. Dies kann dazu führen, dass Seitenansichten auf der Originalseite und auf der Umleitungsseite alle gezählt werden. Diese Situation führt zu einem zusätzlichen Seitenaufruf auf der ersten Seite, selbst wenn der Besucher diese erste Seite nie wirklich „gesehen“ hat.

Die Verwendung des formularbasierten Composers zum Erstellen einer Umleitungsaktivität wird empfohlen, um die Geschwindigkeit der Seitenumleitung zu erhöhen, da der Code dort auf der Seite ausgeführt wird. Es wird zudem die Erstellung eines Umleitungsangebots für jeden Besuch einschließlich des Standardbesuchs empfohlen, wobei die Umleitung zur ursprünglichen Seite zurückführen würde. Durch die Erstellung eines Umleitungsangebots für jedes Erlebnis wird sichergestellt, dass Erlebnisse aller Art falsch gezählt werden. Reporting und Analyse sind weiterhin für den Test gültig.

Ein Grund für die Verwendung von Umleitungsangeboten für alle Erlebnisse in der Aktivität, einschließlich des Standarderlebnisses (Kontrollerlebnis), besteht darin, dieselben Bedingungen für alle Erlebnisse zu verwenden. Wenn das Standarderlebnis beispielsweise kein Umleitungsangebot enthält, aber die anderen Erlebnisse Umleitungsangebote haben, stellt die Geschwindigkeit des Erlebnisses ohne Umleitungsangebot einen Vorteil dar. Umleitungsangebote werden nur für temporäre Szenarien empfohlen, z. B. Tests. Umleitungsangebote werden nicht für permanente Szenarien wie die Personalisierung empfohlen. Nachdem Sie den „Gewinner“ ermittelt haben, sollten Sie die Umleitung entfernen, um die Seitenladeleistung zu verbessern.

+++

## Werden Visual Experience Composer (VEC) und Form-Based Experience Composer unterstützt? {#section_FDA26FE7909B48539DA770559E687677}

+++Antwort
Ja, beide Composer werden unterstützt, solange Sie die integrierten Umleitungsangebote verwenden.

Wenn Sie für die Umleitung Ihren eigenen benutzerdefinierten Code verwenden, müssen Sie sicherstellen, dass Sie die beiden neuen Parameter eingeben, die Umleitungs-URLs zugeordnet sind (`adobe_mc_sdid` und `adobe_mc_ref`, Erklärung weiter unten).

+++

## Welche neuen Abfrage String-Parameter wurden zu den Umleitungs-URLs hinzugefügt? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

+++Antwort
Die folgenden Abfragezeichenfolgenparameter sind mit Umleitungsangeboten verknüpft:

| Parameter | Beschreibung |
|--- |--- |
| `adobe_mc_sdid` | Der `adobe_mc_sdid` Parameter übergibt die SDID (Supplemental Data Id) und die Experience Cloud-Organisations-ID von der Standardseite an die neue Seite. Diese IDs ermöglichen es A4T, die Target-Anfrage auf der Standardseite mit der Analytics-Anfrage auf der neuen Seite zusammenzufügen.<br>Das erwartete Format für die Übergabe von sdid in der URL (für Hybrid-Apps oder von einer App an die Website oder von einer Website an eine andere) ist `ex. adobe_mc_sdid=SDID=123|MCORGID=123456789@AdobeOrg|TS=1498569322` |
| `adobe_mc_ref` | Der Parameter `adobe_mc_ref` gibt die verweisende URL der Standardseite an die neue Seite weiter. Bei Verwendung mit AppMeasurement.js Version 2.1 (oder höher) verwendet Analytics diesen Parameterwert als verweisende URL auf der neuen Seite. |

Diese Parameter werden automatisch zu den Umleitungs-URLs hinzugefügt, wenn die integrierten Umleitungsangebote in VEC und in Form-Based Experience Composer verwendet werden, wenn der Besucher-ID-Service auf der Seite implementiert ist. Wenn Sie Ihren eigenen benutzerdefinierten Code in VEC und in Form-Based Experience Composer verwenden, müssen Sie sicherstellen, dass Sie diese Parameter mit Ihrem benutzerdefinierten Code weitergeben.

+++

## Meine Webserver entfernen diese Parameter aus meinen URLs, was soll ich tun?  {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

+++Antwort
Arbeiten Sie mit Ihrem IT-Team zusammen, um diese Parameter ( `adobe_mc_sdid` und `adobe_mc_ref`) auf die Zulassungsliste setzen.

+++

## Was ist, wenn ich A4T nicht für meine Umleitungsaktivitäten verwende und nicht möchte, dass diese zusätzlichen Parameter zu meinen URLs hinzugefügt werden? {#section_9E608D75FF9349FE96C65FEDD7539F45}

+++Antwort
Verwenden Sie eine benutzerdefinierte Weiterleitung, wenn:

* Sie verwenden A4T nicht mit Ihrer Umleitungsaktivität
* Sie haben den Besucher-ID-Dienst implementiert
* Diese Parameter sollen nicht automatisch zu Ihren URLs hinzugefügt werden

Als Best Practice empfiehlt es sich jedoch, den Parameter `adobe_mc_ref` in der URL zu behalten, um die verweisenden Informationen korrekt an [!DNL Analytics] weiterzugeben.

+++

## Warum sind die Parameter adobe_mc_ref und adobe_mc_sdid in meiner Implementierung doppelt kodiert? {#section_5EFE5F012B944C40865731EA18E7E79E}

+++Antwort
Wenn Sie A4T und Umleitungsangebote verwenden, hängt Target die `adobe_mc_ref`- und `adobe_mc_sdid` an die URL an. Diese Werte sind bereits URL-kodiert. Meistens funktioniert alles wie erwartet. Möglicherweise haben einige Kunden jedoch Systeme zur Lastverteilung oder WEB-Server, die versuchen, die Abfrage-String-Parameter erneut zu kodieren.

Aufgrund dieser doppelten Kodierung kann die Besucher-API den SDID-Wert nicht abrufen, wenn sie versucht, den Wert `adobe_mc_sdid` zu entschlüsseln, und sie erstellt dann eine neue SDID. Dies führt dazu, dass falsche SDID-Werte an Target und Analytics gesendet werden und Sie in Analytics-Berichten eine ungleichmäßige Aufspaltung für Umleitungen sehen.

Adobe empfiehlt, mit Ihrem IT-Team zu sprechen, um sicherzustellen, dass `adobe_mc_ref` und `adobe_mc_sdid` auf die Zulassungsliste gesetzt werden, damit diese Werte nicht umgewandelt werden.

+++

## Warum muss die verweisende URL an die neue Seite übergeben werden? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

+++Antwort
Angenommen, ein Besucher klickt auf einen Link [!DNL `www.google.com`] Ihrer Homepage (`www.mysite.com/index.html`), auf der eine Umleitungsaktivität live ist, und wird dann auf eine neue Seite (`www.mysite.com/index2.html`) umgeleitet.

Zuvor meldete die [!DNL Analytics]-Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.mysite.com/index.html`] anstelle von [!DNL `www.google.com`]. Dies führte zu ungenauen Berichten in [!DNL Analytics] im Zusammenhang mit den verweisenden URLs (beispielsweise Marketingkanalberichte). Die Berichte hatten die Tatsache verloren, dass Sie von [!DNL `www.google.com`] auf die Website gekommen waren.

Bei [!DNL at.js] Version 0.9.6 (oder höher) und [!DNL AppMeasurement.js] 2.1 (oder höher) meldet die [!DNL Analytics] auf der neuen Seite eine verweisende URL von [!DNL `www.google.com`].

+++

## Kann ich benutzerdefinierte/HTML-Weiterleitungsangebote verwenden? {#section_E49F9A83A286488C8F1098A040203D7E}

+++Antwort
Nein, Sie müssen ein integriertes Umleitungsangebot für Aktivitäten verwenden, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden. Aus der Sicht von [!DNL Target] sind HTML-Angebote undurchsichtig: [!DNL Target] kann nicht erkennen, dass ein bestimmter HTML-Abschnitt JavaScript zum Instantiieren einer Weiterleitung enthält.

+++

## ![Adobe Experience Platform Web SDK-Badge](/help/main/assets/platform.png) Unterstützt die [!DNL Adobe Experience Platform Web SDK] Umleitungsangebote für A4T? {#platform}

In den folgenden häufig gestellten Fragen finden Sie weitere Informationen zur Verwendung von A4T und zu Umleitungsangeboten für den [!DNL Platform Web SDK].

### Unterstützt Analytics for Target (A4T) Umleitungsangebote?

+++Antwort
Ja, A4T über die Platform Web SDK unterstützt [Umleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md).

+++

### Werden [!UICONTROL Visual Experience Composer] (VEC) und [!UICONTROL Form-Based Experience Composer] unterstützt?

+++Antwort
Ja, der [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und der [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) werden unterstützt, wenn Sie integrierte Umleitungsangebote verwenden.

+++

### Kann ich benutzerdefinierte/HTML-Umleitungsangebote mit dem [!DNL Platform Web SDK] verwenden?

+++Antwort
Nein, Sie müssen ein integriertes Umleitungsangebot für Aktivitäten verwenden, die A4T verwenden. Aus [!DNL Target] Sicht sind HTML-Angebote undurchsichtig. [!DNL Target] kann nicht wissen, dass ein bestimmtes HTML-Stück JavaScript enthält, das eine Weiterleitung instanziiert.

+++