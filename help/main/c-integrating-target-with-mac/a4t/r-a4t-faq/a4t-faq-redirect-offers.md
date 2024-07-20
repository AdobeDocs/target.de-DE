---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Weiterleitung; Weiterleitungsangebot; adobe-mc-sdid; adobe_mc_ref
description: Hier finden Sie Antworten auf Fragen zur Verwendung von Umleitungsangeboten bei der Verwendung von Analytics für [!DNL Target]  (A4T). Mit A4T können Sie Analytics-Berichte für [!DNL Target] Aktivitäten verwenden.
title: Wo finde ich häufig gestellte Fragen zu Umleitungsangeboten mit A4T?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 44%

---

# Umleitungsangebote – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Verwendung von Umleitungsangeboten bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T) gestellte Fragen.

## Unterstützt Analytics for Adobe Target (A4T) Umleitungsangebote? {#section_46B8B03ED4D542C6AD875F5F61176298}

+++Antwort
Ja, wenn Ihre Implementierung [!DNL at.js] verwendet. Ihre Implementierung muss jedoch die unten aufgeführten Mindestanforderungen erfüllen, um [Weiterleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in Aktivitäten zu verwenden, die Analytics als Berichtsquelle verwenden.

+++

## Was sind die Mindestanforderungen für die Verwendung von Umleitungsangeboten mit A4T? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

+++Antwort
Ihre Implementierung muss die folgenden Mindestanforderungen erfüllen:

* Experience Cloud-Besucher-ID-Service: [!DNL visitorAPI.js], Version 2.3.0 oder neuer.
* Adobe Analytics: [!DNL appMeasurement.js] Version 2.1.
* Adobe Target: [!DNL at.js], Version 1.6.2 oder neuer.

Die drei Bibliotheken müssen sowohl auf der Seite mit dem Weiterleitungsangebot als auch auf der Seite, auf die der Besucher umgeleitet wird, enthalten sein.

+++

## Warum gibt es manchmal Datendiskrepanzen zwischen A4T und Analytics?

+++Antwort
Es werden einige Datendiskrepanzen erwartet. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

+++

## Wie kann ich Diskrepanzen bei der Traffic-Verteilung bei der Verwendung von Umleitungsangeboten in A4T-Aktivitäten minimieren? {#discrepancies}

+++Antwort
Eine begrenzte Anzahl von Kunden hat höhere Abweichungen in der Traffic-Verteilung bei der Verwendung von Umleitungsangeboten in Aktivitäten gemeldet, die mit [!UICONTROL Analytics for Target] (A4T) konfiguriert wurden.

Beachten Sie Folgendes:

* Eine falsche Reihenfolge von [!DNL Target] - und [!DNL Analytics] -Aufrufen kann für höhere Varianzgrade verantwortlich sein.

  Der Aufruf [!DNL Target] muss dem Aufruf [!DNL Analytics] auf der Quellseite (wo eine Umleitung erfolgt) und auf der Zielseite (wo die Umleitung endet) vorangehen.

* Stellen Sie sicher, dass Sie Umleitungsangebote in A4T-Umleitungsaktivitäten verwenden.
* Wenn sich auf der Quellseite mehrere [!DNL Target] Ortsanforderungen befinden (wo die Umleitung erfolgt), empfiehlt [!DNL Adobe], die Umleitungsaktivität für die erste [!DNL Target] Ortsanforderung auszuführen.

  Wenn Sie die Umleitungsaktivität für die erste [!DNL Target] -Ortsanforderung ausführen, werden die Chancen von Aktivitätsqualifikationen verringert, die bei anderen [!DNL Target] -Ortsanforderungen auftreten und im Bericht gezählt werden. Besucher, die umgeleitet werden, müssen nicht in den Berichten anderer Aktivitäten gezählt werden, da sie die Erlebnisse nicht sehen.

+++

## Warum werden manchmal Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt?  {#section_B8F6CC2190B84CF08D945E797C5AF07B}

+++Antwort
Bei der Verwendung von at.js Version 1.6.3 oder höher ist die Zählung von Seitenansichten auf beiden Seiten kein Problem. Diese Race-Bedingung betrifft nur Kunden, die frühere Versionen verwenden. Das Target-Team behält zwei Versionen von at.js: die aktuelle Version und die davor. Aktualisieren Sie at.js nach Bedarf, um sicherzustellen, dass Sie eine [unterstützte Version](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} ausführen.

Wenn Sie eine frühere, nicht unterstützte Version von at.js verwenden, besteht die Möglichkeit, dass eine Race-Bedingung eintritt, die dazu führen kann, dass der Analytics-Aufruf ausgelöst wird, bevor die Umleitung auf der ersten Seite ausgeführt wird. Diese Situation kann dazu führen, dass Seitenansichten auf der Originalseite und auf der Umleitungsseite gezählt werden. Diese Situation führt zu einem zusätzlichen Seitenaufruf auf der ersten Seite, selbst wenn der Besucher diese erste Seite nie wirklich „gesehen“ hat.

Es wird empfohlen, den formularbasierten Composer zum Erstellen einer Umleitungsaktivität zu verwenden, um die Umleitung der Seite zu beschleunigen, da der Code auf der Seite ausgeführt wird. Es wird zudem die Erstellung eines Umleitungsangebots für jeden Besuch einschließlich des Standardbesuchs empfohlen, wobei die Umleitung zur ursprünglichen Seite zurückführen würde. Durch die Erstellung eines Umleitungsangebots für jedes Erlebnis wird sichergestellt, dass bei einer fehlerhaften Zählung alle Erlebnisse berücksichtigt werden. Die Berichterstellung und Analyse sind für den Test weiterhin gültig.

Ein Grund für die Verwendung von Umleitungsangeboten für alle Erlebnisse in der Aktivität, einschließlich des Standarderlebnisses (Kontrollerlebnis), besteht darin, dieselben Bedingungen für alle Erlebnisse zu verwenden. Wenn das Standarderlebnis beispielsweise kein Umleitungsangebot enthält, aber die anderen Erlebnisse Umleitungsangebote haben, stellt die Geschwindigkeit des Erlebnisses ohne Umleitungsangebot einen Vorteil dar. Umleitungsangebote werden nur für temporäre Szenarien empfohlen, z. B. Tests. Umleitungsangebote werden nicht für permanente Szenarien wie die Personalisierung empfohlen. Nachdem Sie den &quot;Gewinner&quot;ermittelt haben, sollten Sie die Umleitung entfernen, um die Seitenladeleistung zu verbessern.

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
| `adobe_mc_sdid` | Der Parameter `adobe_mc_sdid` gibt die Supplemental Data Id (SDID) und die Experience Cloud Org Id (SDID) von der Standardseite an die neue Seite weiter. Diese IDs ermöglichen es A4T, die Target-Anfrage auf der Standardseite mit der Analytics-Anfrage auf der neuen Seite zu &quot;verknüpfen&quot;.<br>Das erwartete Format, das in der URL übermittelt wird (bei Hybridanwendungen oder von einer App zur Website oder von einer Website zur anderen), ist `ex. adobe_mc_sdid=SDID=123|MCORGID=123456789@AdobeOrg|TS=1498569322` |
| `adobe_mc_ref` | Der Parameter `adobe_mc_ref` gibt die verweisende URL der Standardseite an die neue Seite weiter. Bei Verwendung mit AppMeasurement.js Version 2.1 (oder neuer) verwendet Analytics diesen Parameterwert als verweisende URL auf der neuen Seite. |

Diese Parameter werden automatisch zu den Umleitungs-URLs hinzugefügt, wenn die integrierten Umleitungsangebote in VEC und in Form-Based Experience Composer verwendet werden, wenn der Besucher-ID-Service auf der Seite implementiert ist. Wenn Sie Ihren eigenen benutzerdefinierten Code in VEC und in Form-Based Experience Composer verwenden, müssen Sie sicherstellen, dass Sie diese Parameter mit Ihrem benutzerdefinierten Code weitergeben.

+++

## Meine Webserver entfernen diese Parameter aus meinen URLs, was soll ich tun?  {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

+++Antwort
Arbeiten Sie mit Ihrem IT-Team zusammen, damit diese Parameter ( `adobe_mc_sdid` und `adobe_mc_ref`) auf die Zulassungsliste gesetzt werden.

+++

## Was ist, wenn ich A4T nicht für meine Umleitungsaktivitäten verwende und nicht möchte, dass diese zusätzlichen Parameter zu meinen URLs hinzugefügt werden? {#section_9E608D75FF9349FE96C65FEDD7539F45}

+++Antwort
Verwenden Sie eine benutzerdefinierte codierte Umleitung, wenn:

* Sie verwenden A4T nicht für Ihre Umleitungsaktivität
* Sie haben den Besucher-ID-Dienst implementiert.
* Sie möchten nicht, dass diese Parameter automatisch zu Ihren URLs hinzugefügt werden

Als Best Practice empfiehlt es sich jedoch, den Parameter `adobe_mc_ref` in der URL zu behalten, um die verweisenden Informationen korrekt an [!DNL Analytics] weiterzugeben.

+++

## Warum sind die Parameter adobe_mc_ref und adobe_mc_sdid in meiner Implementierung doppelt URL-kodiert? {#section_5EFE5F012B944C40865731EA18E7E79E}

+++Antwort
Wenn Sie A4T und Umleitungsangebote verwenden, hängt Target die Parameter `adobe_mc_ref` und `adobe_mc_sdid` an die URL an. Diese Werte sind bereits URL-kodiert. Meistens funktioniert alles wie erwartet. Möglicherweise haben einige Kunden jedoch Systeme zur Lastverteilung oder WEB-Server, die versuchen, die Abfrage-String-Parameter erneut zu kodieren.

Aufgrund dieser doppelten Kodierung kann die Besucher-API den SDID-Wert nicht abrufen, wenn sie versucht, den Wert `adobe_mc_sdid` zu entschlüsseln, und sie erstellt dann eine neue SDID. Dieser Prozess führt dazu, dass falsche SDID-Werte an Target und Analytics gesendet werden, und Sie sehen eine ungleiche Aufteilung für Umleitungen in Analytics-Berichten.

Adobe empfiehlt, dass Sie mit Ihrem IT-Team sprechen, um sicherzustellen, dass `adobe_mc_ref` und `adobe_mc_sdid` auf die Zulassungsliste gesetzt werden, damit diese Werte nicht umgewandelt werden.

+++

## Warum muss die verweisende URL an die neue Seite übergeben werden? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

+++Antwort
Angenommen, ein Besucher klickt auf einen Link auf [!DNL `www.google.com`] zu Ihrer Homepage (`www.mysite.com/index.html`), auf der eine Umleitungsaktivität aktiv ist, und wird dann zu einer neuen Seite (`www.mysite.com/index2.html`) umgeleitet.

Zuvor hatte die [!DNL Analytics] -Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.mysite.com/index.html`] anstelle von [!DNL `www.google.com`] gemeldet. Dies führte zu ungenauen Berichten in [!DNL Analytics] im Zusammenhang mit den verweisenden URLs (beispielsweise Marketingkanalberichte). Die Berichte hatten verloren, dass Sie von [!DNL `www.google.com`] auf die Site kamen.

Bei [!DNL at.js] Version 0.9.6 (oder neuer) und [!DNL AppMeasurement.js] 2.1 (oder neuer) gibt die [!DNL Analytics] -Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.google.com`] an.

+++

## Kann ich benutzerdefinierte/HTML-Weiterleitungsangebote verwenden? {#section_E49F9A83A286488C8F1098A040203D7E}

+++Antwort
Nein, Sie müssen ein integriertes Umleitungsangebot für Aktivitäten verwenden, die [!DNL Analytics] als Berichtsquelle (A4T) verwenden. Aus der Sicht von [!DNL Target] sind HTML-Angebote undurchsichtig: [!DNL Target] kann nicht erkennen, dass ein bestimmter HTML-Abschnitt JavaScript zum Instantiieren einer Weiterleitung enthält.

+++

## ![Adobe Experience Platform Web SDK Badge](/help/main/assets/platform.png) Unterstützt [!DNL Adobe Experience Platform Web SDK] Umleitungsangebote für A4T? {#platform}

Die folgenden häufig gestellten Fragen enthalten weitere Informationen zur Verwendung von A4T und zur Umleitung von Angeboten mit dem [!DNL Platform Web SDK].

### Unterstützt Analytics for Target (A4T) Umleitungsangebote?

+++Antwort
Ja, A4T über das Platform Web SDK unterstützt [Umleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md).

+++

### Werden [!UICONTROL Visual Experience Composer] (VEC) und [!UICONTROL Form-Based Experience Composer] unterstützt?

+++Antwort
Ja, die [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und die [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) werden unterstützt, wenn Sie integrierte Umleitungsangebote verwenden.

+++

### Kann ich benutzerdefinierte/HTML-Umleitungsangebote mit dem [!DNL Platform Web SDK] verwenden?

+++Antwort
Nein, Sie müssen ein integriertes Umleitungsangebot für Aktivitäten verwenden, die A4T verwenden. Aus Sicht von [!DNL Target] sind HTML-Angebote undurchsichtig. [!DNL Target] kann nicht erkennen, dass ein bestimmtes HTML-Element JavaScript enthält, das eine Umleitung instanziiert.

+++