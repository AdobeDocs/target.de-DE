---
keywords: FAQ; häufig gestellte Fragen; Analytics für Target; a4T; Weiterleitung; Weiterleitungsangebot; adobe-mc-sdid; adobe_mc_ref
description: Antworten auf Fragen zur Verwendung von Umleitungs-Angeboten bei der Verwendung von Analytics für [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] Aktivitäten
title: Wo finde ich häufig gestellte Fragen zu Umleitungs-Angeboten mit A4T?
feature: 'Analytics for Target (A4T) '
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: b14c9bb4bc0363c77de084c7ae7110e73c5f2f13
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 62%

---

# Umleitungsangebote – Häufig gestellte Fragen zu A4T

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Verwendung von Umleitungs-Angeboten, wenn [!DNL Adobe Analytics] als Berichte für [!DNL Adobe Target] (A4T) verwendet wird.

## Unterstützt Analytics für Adobe Target (A4T) Umleitungs-Angebot? {#section_46B8B03ED4D542C6AD875F5F61176298}

Ja, wenn Ihre Implementierung [!DNL at.js] verwendet. Ihre Implementierung muss jedoch die unten aufgeführten Mindestanforderungen erfüllen, um [Weiterleitungsangebote](/help/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in Aktivitäten zu verwenden, die Analytics als Berichtsquelle verwenden.

>[!NOTE]
>
>Es gibt ein bekanntes Problem, bei dem einer begrenzten Anzahl von Kunden mit Redirects mit A4T ein höherer Prozentsatz an aufgetrennten Treffern angezeigt wird. Siehe [Bekannte Probleme und gelöste Probleme](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Welche Mindestanforderungen gelten für die Verwendung von Umleitungs-Angeboten mit A4T? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

Ihre Implementierung muss folgende Mindestanforderungen erfüllen:

* Experience Cloud-Besucher-ID-Service: [!DNL visitorAPI.js], Version 2.3.0 oder neuer.
* Adobe Analytics: [!DNL appMeasurement.js] Version 2.1.
* Adobe Target: [!DNL at.js], Version 1.6.2 oder neuer.

   Die [!DNL mbox.js] Bibliothek unterstützt keine Umleitungsangebote in A4T. Ihre Implementierung muss [!DNL at.js] verwenden.

Die drei Bibliotheken müssen sowohl auf der Seite mit dem Weiterleitungsangebot als auch auf der Seite, auf die der Besucher umgeleitet wird, enthalten sein.

## Warum gibt es manchmal Datendiskrepanzen zwischen A4T und Analytics?

Es werden einige Datendiskrepanzen erwartet. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen Target und Analytics bei Verwendung und Nichtverwendung von A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

## Warum werden manchmal Seitenaufrufe auf der Originalseite und auf der Umleitungsseite gezählt?  {#section_B8F6CC2190B84CF08D945E797C5AF07B}

Bei Verwendung von at.js Version 1.6.3 oder höher ist das Zählen von Ansichten auf beiden Seiten kein Problem. Diese Race-Bedingung betrifft nur Kunden, die frühere Versionen verwenden. Das Target-Team behält zwei Versionen von at.js: die aktuelle Version und die davor. Führen Sie bei Bedarf ein Upgrade von at.js durch, um sicherzustellen, dass Sie eine [unterstützte Version](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) ausführen.

Wenn Sie eine frühere, nicht unterstützte Version von at.js verwenden, besteht die Möglichkeit, dass eine Race-Bedingung eintritt, die dazu führen kann, dass der Analytics-Aufruf ausgelöst wird, bevor die Umleitung auf der ersten Seite ausgeführt wird. Dies kann dazu führen, dass Ansichten auf der Originalseite und auf der Umleitungsseite gezählt werden. Diese Situation führt zu einem zusätzlichen Seitenaufruf auf der ersten Seite, selbst wenn der Besucher diese erste Seite nie wirklich „gesehen“ hat.

Die Verwendung des formularbasierten Composers zum Erstellen einer Umleitungs-Aktivität wird empfohlen, um die Seitenumleitung zu beschleunigen, da der Code auf der Seite ausgeführt wird. Es wird zudem die Erstellung eines Umleitungsangebots für jeden Besuch einschließlich des Standardbesuchs empfohlen, wobei die Umleitung zur ursprünglichen Seite zurückführen würde. Durch das Erstellen eines Umleitungs-Angebots für jedes Erlebnis wird sichergestellt, dass eine Fehlzählung bei allen Erlebnissen stattfindet. Berichte und Analyse sind für den Test weiterhin gültig.

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
| `adobe_mc_sdid` | Der Parameter `adobe_mc_sdid` gibt die Supplemental Data Id (SDID) und die Experience Cloud Org Id von der Standardseite an die neue Seite weiter. Diese IDs ermöglichen es A4T, die Anforderung der Zielgruppe auf der Standardseite mit der Analytics-Anforderung auf der neuen Seite zu &quot;verbinden&quot;. |
| `adobe_mc_ref` | Der Parameter `adobe_mc_ref` gibt die verweisende URL der Standardseite an die neue Seite weiter. Bei Verwendung mit AppMeasurement.js Version 2.1 (oder höher) verwendet Analytics diesen Parameterwert als verweisende URL auf der neuen Seite. |

Diese Parameter werden automatisch zu den Umleitungs-URLs hinzugefügt, wenn die integrierten Umleitungsangebote in VEC und in Form-Based Experience Composer verwendet werden, wenn der Besucher-ID-Service auf der Seite implementiert ist. Wenn Sie Ihren eigenen benutzerdefinierten Code in VEC und in Form-Based Experience Composer verwenden, müssen Sie sicherstellen, dass Sie diese Parameter mit Ihrem benutzerdefinierten Code weitergeben.

## Meine Webserver entfernen diese Parameter aus meinen URLs, was soll ich tun?  {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

Arbeiten Sie mit Ihrem IT-Team zusammen, um diese Parameter ( `adobe_mc_sdid` und `adobe_mc_ref`) auf die Zulassungsliste setzen.

## Was ist, wenn ich A4T nicht für meine Umleitungsaktivitäten verwende und nicht möchte, dass diese zusätzlichen Parameter zu meinen URLs hinzugefügt werden? {#section_9E608D75FF9349FE96C65FEDD7539F45}

Verwenden Sie eine benutzerdefinierte Umleitung, wenn:

* Sie verwenden A4T nicht mit Ihrer Umleitungs-Aktivität
* Sie haben den Besucher-ID-Dienst implementiert
* Sie möchten nicht, dass diese Parameter automatisch Ihren URLs hinzugefügt werden

Als Best Practice empfiehlt es sich jedoch, den Parameter `adobe_mc_ref` in der URL zu behalten, um die verweisenden Informationen korrekt an [!DNL Analytics] weiterzugeben.

## Warum sind die Parameter adobe_mc_ref und adobe_mc_sdid in meiner Implementierung doppelt URL-kodiert? {#section_5EFE5F012B944C40865731EA18E7E79E}

Wenn Sie A4T und Weiterleitungsangebote verwenden, hängt Target die Parameter `adobe_mc_ref` und `adobe_mc_sdid` an die URL an. Diese Werte sind bereits URL-kodiert. Meistens funktioniert alles wie erwartet. Möglicherweise haben einige Kunden jedoch Systeme zur Lastverteilung oder WEB-Server, die versuchen, die Abfrage-String-Parameter erneut zu kodieren.

Aufgrund dieser doppelten Kodierung kann die Besucher-API den SDID-Wert nicht abrufen, wenn sie versucht, den Wert `adobe_mc_sdid` zu entschlüsseln, und sie erstellt dann eine neue SDID. Dieser Vorgang führt dazu, dass fehlerhafte SDID-Werte an Zielgruppe und Analytics gesendet werden. Für Umleitungen in Analytics-Berichten wird eine ungleichmäßige Aufteilung angezeigt.

Adobe empfiehlt, mit Ihrem IT-Team zu sprechen, um sicherzustellen, dass `adobe_mc_ref` und `adobe_mc_sdid` auf die Zulassungsliste gesetzt werden, damit diese Werte in keiner Weise transformiert werden.

## Warum muss die verweisende URL an die neue Seite übergeben werden? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

Angenommen, ein Besucher klickt auf einen Link auf [!DNL `www.google.com`] zu Ihrer Homepage (`www.mysite.com/index.html`), auf der eine Umleitungsseite live ist, und wird dann zu einer neuen Aktivität (`www.mysite.com/index2.html`) umgeleitet.

Bisher hat die [!DNL Analytics]-Anfrage auf der neuen Seite eine verweisende URL von [!DNL `www.mysite.com/index.html`] statt von [!DNL `www.google.com`] gemeldet. Dies führte zu ungenauen Berichten in [!DNL Analytics] im Zusammenhang mit den verweisenden URLs (beispielsweise Marketingkanalberichte). Somit berücksichtigten die Berichte nicht, dass Sie über [!DNL `www.google.com`] auf die Seite kamen.

Bei [!DNL at.js] Version 0.9.6 (oder höher) und [!DNL AppMeasurement.js] 2.1 (oder höher) zeigt die [!DNL Analytics]-Anforderung auf der neuen Seite eine verweisende URL von [!DNL `www.google.com`] an.

## Kann ich benutzerdefinierte/HTML-Weiterleitungsangebote verwenden? {#section_E49F9A83A286488C8F1098A040203D7E}

Nein, Sie müssen für Aktivitäten mit [!DNL Analytics] als Berichterstellungsquelle (A4T) ein integriertes Weiterleitungsangebot verwenden. Aus der Sicht von [!DNL Target] sind HTML-Angebote undurchsichtig: [!DNL Target] kann nicht erkennen, dass ein bestimmter HTML-Abschnitt JavaScript zum Instantiieren einer Weiterleitung enthält.

## Unterstützt das [!DNL Adobe Experience Platform Web SDK] Umleitungs-Angebot für A4T? {#platform}

Die folgenden häufig gestellten Fragen bieten weitere Informationen zur Verwendung von A4T und leiten Angebot mit dem [!DNL Platform Web SDK] um.

>[!NOTE]
>
>Die Unterstützung für A4T in einer [!DNL Adobe Experience Platform Web SDK]-Implementierung, die in diesem Artikel besprochen wird, ist für die [!DNL Platform Web SDK] Version 2.5.0 (24. Mai 2021) geplant.

### Unterstützt Analytics for Target (A4T) Umleitungsangebote?

Ja, A4T über das Platform Web SDK unterstützt [Umleitungs-Angebot](/help/c-experiences/c-manage-content/offer-redirect.md).

### Werden [!UICONTROL Visual Experience Composer] (VEC) und [!UICONTROL Form-Based Experience Composer] unterstützt?

Ja, der [[!UICONTROL Visual Experience Composer]](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) und der [[!UICONTROL Form-Based Experience Composer]](/help/c-experiences/form-experience-composer.md) werden unterstützt, wenn Sie integrierte Umleitungs-Angebot verwenden.

### Kann ich mit dem [!DNL Platform Web SDK] benutzerdefinierte/HTML-Umleitungs-Angebot verwenden?

Nein, Sie müssen ein integriertes Umleitungs-Angebot für Aktivitäten verwenden, die A4T verwenden. Aus der Perspektive [!DNL Target] sind HTML-Angebot undurchsichtig. [!DNL Target] kann nicht erkennen, dass ein bestimmtes HTML-Stück JavaScript enthält, das eine Umleitung instanziiert.
