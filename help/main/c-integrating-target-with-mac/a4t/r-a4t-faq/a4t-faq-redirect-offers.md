---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Weiterleitung; Weiterleitungsangebot; adobe-mc-sdid; adobe_mc_ref
description: Antworten auf Fragen zur Verwendung von Umleitungsangeboten bei der Verwendung von Analytics für [!DNL Target] (A4T). Mit A4T können Sie Analytics-Reporting für [!DNL Target] Aktivitäten.
title: Wo finde ich häufig gestellte Fragen zu Umleitungsangeboten mit A4T?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 61%

---

# Umleitungsangebote – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig zur Verwendung von Umleitungsangeboten bei Verwendung von [!DNL Adobe Analytics] als Berichtsquelle für [!DNL Adobe Target] (A4T).

## Unterstützt Analytics for Adobe Target (A4T) Umleitungsangebote? {#section_46B8B03ED4D542C6AD875F5F61176298}

Ja, wenn Ihre Implementierung [!DNL at.js]. Ihre Implementierung muss jedoch die unten aufgeführten Mindestanforderungen erfüllen, um [Weiterleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in Aktivitäten zu verwenden, die Analytics als Berichtsquelle verwenden.

>[!NOTE]
>
>Es gibt ein bekanntes Problem, bei dem einer begrenzten Anzahl von Kunden mit Redirects mit A4T ein höherer Prozentsatz an aufgetrennten Treffern angezeigt wird. Siehe [Bekannte Probleme und gelöste Probleme](/help/main/r-release-notes/known-issues-resolved-issues.md#redirect).

## Was sind die Mindestanforderungen für die Verwendung von Umleitungsangeboten mit A4T? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

Ihre Implementierung muss folgende Mindestanforderungen erfüllen:

* Experience Cloud-Besucher-ID-Service: [!DNL visitorAPI.js], Version 2.3.0 oder neuer.
* Adobe Analytics: [!DNL appMeasurement.js] Version 2.1.
* Adobe Target: [!DNL at.js], Version 1.6.2 oder neuer.

Die drei Bibliotheken müssen sowohl auf der Seite mit dem Weiterleitungsangebot als auch auf der Seite, auf die der Besucher umgeleitet wird, enthalten sein.

## Warum gibt es manchmal Datendiskrepanzen zwischen A4T und Analytics?

Es werden einige Datendiskrepanzen erwartet. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

## Warum werden manchmal Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt?  {#section_B8F6CC2190B84CF08D945E797C5AF07B}

Bei der Verwendung von at.js Version 1.6.3 oder höher ist die Zählung von Seitenansichten auf beiden Seiten kein Problem. Diese Race-Bedingung betrifft nur Kunden, die frühere Versionen verwenden. Das Target-Team behält zwei Versionen von at.js: die aktuelle Version und die davor. Führen Sie bei Bedarf ein Upgrade von at.js durch, um sicherzustellen, dass Sie eine [unterstützte Version](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) ausführen.

Wenn Sie eine frühere, nicht unterstützte Version von at.js verwenden, besteht die Möglichkeit, dass eine Race-Bedingung eintritt, die dazu führen kann, dass der Analytics-Aufruf ausgelöst wird, bevor die Umleitung auf der ersten Seite ausgeführt wird. Diese Situation kann dazu führen, dass Seitenansichten auf der Originalseite und auf der Umleitungsseite gezählt werden. Diese Situation führt zu einem zusätzlichen Seitenaufruf auf der ersten Seite, selbst wenn der Besucher diese erste Seite nie wirklich „gesehen“ hat.

Es wird empfohlen, den formularbasierten Composer zum Erstellen einer Umleitungsaktivität zu verwenden, um die Umleitung der Seite zu beschleunigen, da der Code auf der Seite ausgeführt wird. Es wird zudem die Erstellung eines Umleitungsangebots für jeden Besuch einschließlich des Standardbesuchs empfohlen, wobei die Umleitung zur ursprünglichen Seite zurückführen würde. Durch die Erstellung eines Umleitungsangebots für jedes Erlebnis wird sichergestellt, dass bei einer fehlerhaften Zählung alle Erlebnisse berücksichtigt werden. Die Berichterstellung und Analyse sind für den Test weiterhin gültig.

Ein Grund für die Verwendung von Umleitungsangeboten für alle Erlebnisse in der Aktivität, einschließlich des Standarderlebnisses (Kontrollerlebnis), besteht darin, dieselben Bedingungen für alle Erlebnisse zu verwenden. Wenn das Standarderlebnis beispielsweise kein Umleitungsangebot enthält, aber die anderen Erlebnisse Umleitungsangebote haben, stellt die Geschwindigkeit des Erlebnisses ohne Umleitungsangebot einen Vorteil dar. Umleitungsangebote werden nur für temporäre Szenarien empfohlen, z. B. Tests. Umleitungsangebote werden nicht für permanente Szenarien wie die Personalisierung empfohlen. Nachdem Sie den „Gewinner“ ermittelt haben, sollten Sie die Umleitung entfernen, um die Seitenladeleistung zu verbessern.

Weitere Informationen zu diesem Problem finden Sie in dem Informationen zu „Weiterleitungsangeboten“ unter [Bekannte Probleme](/help/main/r-release-notes/known-issues-resolved-issues.md#redirect).

## Werden Visual Experience Composer (VEC) und Form-Based Experience Composer unterstützt? {#section_FDA26FE7909B48539DA770559E687677}

Ja, beide Composer werden unterstützt, solange Sie die integrierten Umleitungsangebote verwenden.

Wenn Sie für die Umleitung Ihren eigenen benutzerdefinierten Code verwenden, müssen Sie sicherstellen, dass Sie die beiden neuen Parameter eingeben, die Umleitungs-URLs zugeordnet sind (`adobe_mc_sdid` und `adobe_mc_ref`, Erklärung weiter unten).

## Welche neuen Abfrage String-Parameter wurden zu den Umleitungs-URLs hinzugefügt? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

Die folgenden Abfrage String-Parameter sind Umleitungsangeboten zugeordnet:

| Parameter | Beschreibung |
|--- |--- |
| `adobe_mc_sdid` | Die `adobe_mc_sdid` übergibt die Supplemental Data Id (SDID) und die Experience Cloud Org ID von der Standardseite an die neue Seite. Diese IDs ermöglichen es A4T, die Target-Anfrage auf der Standardseite mit der Analytics-Anfrage auf der neuen Seite zu &quot;verknüpfen&quot;. |
| `adobe_mc_ref` | Der Parameter `adobe_mc_ref` gibt die verweisende URL der Standardseite an die neue Seite weiter. Bei der Verwendung mit AppMeasurement.js Version 2.1 (oder höher) verwendet Analytics diesen Parameterwert als verweisende URL auf der neuen Seite. |

Diese Parameter werden automatisch zu den Umleitungs-URLs hinzugefügt, wenn die integrierten Umleitungsangebote in VEC und in Form-Based Experience Composer verwendet werden, wenn der Besucher-ID-Service auf der Seite implementiert ist. Wenn Sie Ihren eigenen benutzerdefinierten Code in VEC und in Form-Based Experience Composer verwenden, müssen Sie sicherstellen, dass Sie diese Parameter mit Ihrem benutzerdefinierten Code weitergeben.

## Meine Webserver entfernen diese Parameter aus meinen URLs, was soll ich tun?  {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

Arbeiten Sie mit Ihrem IT-Team zusammen, um diese Parameter zu erhalten ( `adobe_mc_sdid` und `adobe_mc_ref`) auf die Zulassungsliste gesetzt.

## Was ist, wenn ich A4T nicht für meine Umleitungsaktivitäten verwende und nicht möchte, dass diese zusätzlichen Parameter zu meinen URLs hinzugefügt werden? {#section_9E608D75FF9349FE96C65FEDD7539F45}

Verwenden Sie eine benutzerdefinierte codierte Umleitung, wenn:

* Sie verwenden A4T nicht für Ihre Umleitungsaktivität
* Sie haben den Besucher-ID-Dienst implementiert.
* Sie möchten nicht, dass diese Parameter automatisch zu Ihren URLs hinzugefügt werden

Als Best Practice empfiehlt es sich jedoch, den Parameter `adobe_mc_ref` in der URL zu behalten, um die verweisenden Informationen korrekt an [!DNL Analytics] weiterzugeben.

## Warum sind die Parameter adobe_mc_ref und adobe_mc_sdid in meiner Implementierung doppelt URL-kodiert? {#section_5EFE5F012B944C40865731EA18E7E79E}

Wenn Sie A4T und Weiterleitungsangebote verwenden, hängt Target die Parameter `adobe_mc_ref` und `adobe_mc_sdid` an die URL an. Diese Werte sind bereits URL-kodiert. Meistens funktioniert alles wie erwartet. Möglicherweise haben einige Kunden jedoch Systeme zur Lastverteilung oder WEB-Server, die versuchen, die Abfrage-String-Parameter erneut zu kodieren.

Aufgrund dieser doppelten Kodierung kann die Besucher-API den SDID-Wert nicht abrufen, wenn sie versucht, den Wert `adobe_mc_sdid` zu entschlüsseln, und sie erstellt dann eine neue SDID. Dieser Prozess führt dazu, dass falsche SDID-Werte an Target und Analytics gesendet werden, und Sie sehen eine ungleiche Aufteilung für Umleitungen in Analytics-Berichten.

Adobe empfiehlt, mit Ihrem IT-Team zu sprechen, um sicherzustellen, dass `adobe_mc_ref` und `adobe_mc_sdid` auf die Zulassungsliste gesetzt werden, sodass diese Werte nicht umgewandelt werden.

## Warum muss die verweisende URL an die neue Seite übergeben werden? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

Angenommen, ein Besucher klickt auf einen Link auf [!DNL `www.google.com`] auf Ihrer Homepage (`www.mysite.com/index.html`), bei dem eine Umleitungsaktivität aktiv ist und dann zu einer neuen Seite umgeleitet wird (`www.mysite.com/index2.html`).

Bisher hat die [!DNL Analytics]-Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.mysite.com/index.html`] statt von [!DNL `www.google.com`] gemeldet. Dies führte zu ungenauen Berichten in [!DNL Analytics] im Zusammenhang mit den verweisenden URLs (beispielsweise Marketingkanalberichte). Somit berücksichtigten die Berichte nicht, dass Sie über [!DNL `www.google.com`] auf die Seite kamen.

Mit [!DNL at.js] Version 0.9.6 (oder neuer) und [!DNL AppMeasurement.js] 2.1 (oder höher), die [!DNL Analytics] -Anfrage auf der neuen Seite gibt eine verweisende URL von [!DNL `www.google.com`].

## Kann ich benutzerdefinierte/HTML-Weiterleitungsangebote verwenden? {#section_E49F9A83A286488C8F1098A040203D7E}

Nein, Sie müssen für Aktivitäten mit [!DNL Analytics] als Berichterstellungsquelle (A4T) ein integriertes Weiterleitungsangebot verwenden. Aus der Sicht von [!DNL Target] sind HTML-Angebote undurchsichtig: [!DNL Target] kann nicht erkennen, dass ein bestimmter HTML-Abschnitt JavaScript zum Instantiieren einer Weiterleitung enthält.

## ![Adobe Experience Platform Web SDK-Badge](/help/main/assets/platform.png) Stellt die [!DNL Adobe Experience Platform Web SDK] Unterstützung von Umleitungsangeboten für A4T? {#platform}

Die folgenden häufig gestellten Fragen enthalten weitere Informationen zur Verwendung von A4T und zur Umleitung von Angeboten mit der [!DNL Platform Web SDK].

### Unterstützt Analytics for Target (A4T) Umleitungsangebote?

Ja, A4T über das Platform Web SDK unterstützt [Umleitungsangebote](/help/main/c-experiences/c-manage-content/offer-redirect.md).

### Sind die [!UICONTROL Visual Experience Composer] (VEC) und [!UICONTROL Form-Based Experience Composer] unterstützt?

Ja, die [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) werden unterstützt, wenn Sie integrierte Umleitungsangebote verwenden.

### Kann ich benutzerdefinierte/HTML-Umleitungsangebote mit dem [!DNL Platform Web SDK]?

Nein, Sie müssen ein integriertes Umleitungsangebot für Aktivitäten verwenden, die A4T verwenden. Aus dem [!DNL Target] Perspektive, HTML-Angebote sind undurchsichtig. [!DNL Target] kann nicht wissen, dass ein bestimmtes HTML-Element JavaScript enthält, das eine Umleitung instanziiert.