---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Erweiterungen, Fehlerbehebungen und bekannten Problemen in jeder Target Standard- und Target Premium-Version.
keywords: Versionshinweise; Vorabversion
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
seo-title: Target-Versionshinweise (aktuell)
solution: Target
title: Target-Versionshinweise (aktuell)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version.

## Mitteilungen

Folgende wichtige Ankündigungen sollten Sie kennen:

* Am 20. Februar 2019 wurde die Adobe Target-Infrastruktur in den Regionen EMEA, Japan und APAC aktualisiert, um keine Daten mehr von Endbenutzern mit älteren Geräten oder Webbrowsern zu erfassen, die TLS 1.1 oder höher nicht unterstützen. Dieses Upgrade ist für den nordamerikanischen Bereich für den **1. April 2019 geplant**. Die Migration zu TLS 1.2 bietet eine verbesserte Sicherheit. Für einen reibungslosen Übergang sollten Sie die Details zu diesem Thema genau durchlesen und die Änderungen mit Ihrem IT-Team entsprechend planen. Weitere Informationen finden Sie unter [TLS (Transport Layer Security)-Verschlüsselungsänderungen](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] und [!DNL Adobe Marketing Cloud] werden ab März 2019 die Unterstützung für Microsoft Internet Explorer 11 beenden. Diese Änderung betrifft nur [!DNL Target]-Authoring. Diese Änderung wirkt sich nicht auf die Bereitstellung von Erlebnissen aus. Wechseln Sie zu Microsoft Edge oder einem anderen Browser. Weitere Informationen finden Sie unter [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## Target Standard/Premium 19.6.1 (26. Juni 2019)

Dieses Release umfasst die folgenden neuen Funktionen und Erweiterungen:

| Funktion / Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer (VEC) | **Neue VEC-Menüoptionen**: Wenn Sie im VEC auf ein Seitenelement klicken, werden in einem Menü die für diesen Elementtyp verfügbaren Optionen angezeigt.<ul><li>You can now use the [!UICONTROL Styles &gt; Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>See *Styles* in [Visual Experience Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**Verbesserungen** an Clicktracking: Wir haben den Prozess zur Konfiguration der Klick-Tracking im VEC und im Einzelseitenanwendung (SPA) verbessert.<ul><li>Während Sie Elemente auswählen, die bei der Klick-Verfolgung verwendet werden sollen, werden die Namen aller verfügbaren Elemente im Bedienfeld &quot;Modifizierungen&quot; auf der rechten Seite angezeigt, sodass die gewünschten Elemente schnell und einfach ausgewählt werden können.</li><li>The [!UICONTROL Goals &amp; Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. Sie können den Mauszeiger über diese Nummer bewegen, um die Namen aller ausgewählten Elemente anzuzeigen. (TGT-33878)</li></ul>See [Click tracking](/help/c-activities/r-success-metrics/click-tracking.md). |
| Visual Experience Composer für Einzelseiten-Apps (SPA VEC) | **Geführter Arbeitsablauf**: Ein neuer geführter Arbeitsablauf hilft Ihnen, zu verstehen, wie die Einstellungen für die Seitenauslieferung konfiguriert werden sollen, um eine Aktivität für Ihre einzelne Seite-App erfolgreich auszuführen und auszuführen. (TGT-33718)<br> See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Änderungen klonen**: Sie können jetzt eine Änderung mithilfe der SPA VEC definieren und diese Änderung dann klonen, um sie in anderen Ansichten Ihrer Einzelseitenanwendung zu verwenden. (TGT-33882)<br>See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md). |
| Mobile Visual Experience Composer | **Mehrere App-Versionen**: Sie können jetzt Aktivitäten für mehrere Versionen Ihrer mobilen App erstellen. Dadurch sparen Sie Zeit und Mühe, wenn die Versionen ähnlich sind, und Sie müssen die Benutzeroberfläche der App nicht wesentlich ändern. (TGT-34231)<br>See &quot;Manage multiple app versions&quot; in [Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#using-the-mobile-vec). |
| ![Premium-Badge](/help/assets/premium.png) Automatisierte Personalisierung (AP) und Automatisches Targeting | **Spezifisches Erlebnis als Steuerung**: Sie können ein Erlebnis auswählen, das beim Erstellen einer AP- oder automatisch-Targeting-Aktivität als Kontrolle verwendet werden soll. Mit dieser Funktion können Sie den gesamten Traffic-Traffic an ein bestimmtes Erlebnis weiterleiten, basierend auf dem Prozentsatz der Traffic-Zuordnung, der in der Aktivität konfiguriert wurde. Anschließend können Sie die Leistungsberichte des personalisierten Traffic auswerten, um den Traffic zu diesem Erlebnis zu steuern. Die aktuelle Kontrolloption (zufällig bereitgestellte Erlebnisse) ist weiterhin verfügbar. (TGT-32801 &amp; TGT-26572)<br>See [Use a specific experience as control](/help/c-activities/t-automated-personalization/experience-as-control.md).<br>**Personalisierungsinsight-Berichte**: Die Benennung des Marketingprogramms für Attribute, wenn ein Besucher ein bestimmtes Inhaltselement an einem bestimmten Ort sieht, bietet aussagekräftigere Informationen. (TGT-33326 &amp; TGT-34957)<br>See [Data collection for the Target personalization algorithms](/help/c-activities/t-automated-personalization/ap-data.md). |
| Google Chrome-Cookie-Richtlinien | Google hat kürzlich angekündigt, dass die Entwickler seit Chrome 76, die für ein Release vom 30. Juli 2019 verpackt sind, explizit angeben müssen, welche Cookies auf Websites funktionieren und welche Cookies Benutzer verfolgen können.<br>Da die Branche ein sicheres Web für Verbraucher schaffen kann, ist Target absolut verpflichtet, personalisierte Erlebnisse während des Meetings bereitzustellen und die Datenschutzerwartungen der Besucher zu überschreiten.<br>Weitere Informationen finden Sie unter [Google Chrome-Cookie-Cookie-Richtlinien](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md). |

## at. js Version 2.1.0 (3. Juni 2019)

Wir freuen uns über die folgenden spannenden Funktionen in at. js 2.1.0:

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Support für Adobe-Teilnahme | Adobe Opt-In bietet die Möglichkeit, Adobe-Lösungsintegrationen mit Genehmigungsverwaltungsplattformen zu vereinfachen.<br>Weitere Informationen zu Adobe Opt-In finden Sie unter [Privatsphäre und Datenschutz-Grundverordnung (DSGVO)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| Branchenübliche CSP-kompatibel | at. js verwendet keine eval () mehr, um javascript auszuführen. |
| Clientseitige Analyseprotokollierung | Gibt Kunden volle Kontrolle darüber, wie sie Analytics-Daten an Adobe Analytics senden können, ob auf Client- oder serverseitig.<br>Weitere Informationen finden Sie unter [clientseitige Analytics-Anmeldung](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) *Vor der Implementierung*. |
| Benachrichtigungen senden | Allows developers to send notifications when an experience is rendered by their code instead of using `applyOffer()` or `applyOffers()`.<br>Weitere Informationen finden Sie unter [adobe. target. sendnotifications (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md). |
| Geringere Dateigröße | Die Größe von at. js wird um ~ 24% verringert. Die kleinere Dateigröße verbessert die Seitenladeleistung und verringert die Zeit, at. js auf der Seite herunterzuladen. |
| Aktualisierungen der Dokumentation von at. js | For a full list of all articles updated due to the at.js 2.1.0 release, see the June 3, 2019 entries in [Documentation changes](/help/r-release-notes/doc-change.md). |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://marketing.adobe.com/resources/help/en_US/whatsnew/). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |