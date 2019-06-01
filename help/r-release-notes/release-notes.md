---
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Erweiterungen, Fehlerbehebungen und bekannten Problemen in jeder Target Standard- und Target Premium-Version.
keywords: Versionshinweise; Vorabversion
seo-description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
seo-title: Target-Versionshinweise (aktuell)
solution: Target
title: Target-Versionshinweise (aktuell)
topic: 'Recommendations '
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 2462ad2d49449217827fa474aa5f3f0a3e8c777d

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version.

## Mitteilungen

Folgende wichtige Ankündigungen sollten Sie kennen:

* Am 20. Februar 2019 wurde die Adobe Target-Infrastruktur in den Regionen EMEA, Japan und APAC aktualisiert, um keine Daten mehr von Endbenutzern mit älteren Geräten oder Webbrowsern zu erfassen, die TLS 1.1 oder höher nicht unterstützen. Dieses Upgrade ist für den Nordamerikanischen Bereich für den **1. April 2019 geplant**. Die Migration zu TLS 1.2 bietet eine verbesserte Sicherheit. Es ist wichtig, dass Sie die Details durchgehen und die Änderungen an Ihrem IT-Team planen, um einen glatten Übergang zu erhalten. Weitere Informationen finden Sie [unter TLS (Transport Layer Security)-](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)Verschlüsselung.
* [!DNL Target] und [!DNL Adobe Marketing Cloud] werden ab März 2019 die Unterstützung für Microsoft Internet Explorer 11 beenden. Diese Änderung betrifft nur [!DNL Target]-Authoring. Diese Änderung wirkt sich nicht auf die Bereitstellung von Erlebnissen aus. Wechseln Sie zu Microsoft Edge oder einem anderen Browser. Weitere Informationen finden Sie unter [Unterstützte Browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## at. js Version 2.1.0 (3. Juni 2019)

Wir freuen uns über die folgenden spannenden Funktionen in at. js 2.1.0:

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Support für Adobe-Teilnahme | Adobe Opt-In bietet die Möglichkeit, Adobe-Lösungsintegrationen mit Genehmigungsverwaltungsplattformen zu vereinfachen.<br>Weitere Informationen zu Adobe Opt-In finden Sie unter [Privatsphäre und Datenschutz-Grundverordnung (DSGVO)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| Branchenübliche CSP-kompatibel | at. js verwendet keine eval () mehr, um javascript auszuführen. |
| Clientseitige Analyseprotokollierung | Gibt Kunden volle Kontrolle darüber, wie sie Analytics-Daten an Adobe Analytics senden können, ob auf Client- oder serverseitig.<br>Weitere Informationen finden Sie unter [clientseitige Analytics-Anmeldung](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) *Vor der Implementierung*. |
| Benachrichtigungen senden | Ermöglicht es Entwicklern, Benachrichtigungen zu senden, wenn ein Erlebnis durch ihren Code statt durch Verwendung oder `applyOffer()``applyOffers()`Verwendung wiedergegeben wird.<br>Weitere Informationen finden Sie unter [adobe. target. sendnotifications (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md). |
| Geringere Dateigröße | Die Größe von at. js wird um ~ 24% verringert. Die kleinere Dateigröße verbessert die Seitenladeleistung und verringert die Zeit, at. js auf der Seite herunterzuladen. |
| Aktualisierungen der Dokumentation von at. js | Eine vollständige Liste aller Artikel, die aufgrund der Veröffentlichung von at. js 2.1.0 aktualisiert wurden, finden Sie in [den Dateiänderungen vom 3. Juni 2019](/help/r-release-notes/doc-change.md). |

## Visual Experience Composer für Mobile Apps (14. Mai 2019) {#mobile-app-vec-may14-1}

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer (VEC) für mobile Apps | Mit Mobile App VEC können Sie Aktivitäten erstellen und Inhalte auf nativen Mobil-Apps ohne ständige Entwicklungsabhängigkeiten und App-Versionszyklen personalisieren.<br>Weitere Informationen finden Sie unter:<ul><li>[Visual Experience Composer für mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Einrichten des Klick-Trackings im Mobile VEC](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul> |

## [!DNL Target] Standard/Premium 19.5.1 (21. Mai 2019) {#tgt-19-5-1}

(Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

### Funktionsaktualisierungen

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Einzelseitenanwendung Visual Experience Composer (SPA VEC) | Der SPA VEC enthält die folgenden Verbesserungen, mit denen Sie Ihre Arbeit schneller und effizienter erledigen können:<ul><li>Durch Klicken auf eine Aktion in der SPA wird das Element auf der Site markiert, auf das diese Aktion angewendet wird. Jede VEC-Aktion, die unter einer Ansicht erstellt wurde, hat vier entsprechende Symbole: Informationen, Bearbeiten, Verschieben und Löschen. Mit der neuen Funktion &quot;Verschieben&quot; in dieser Version können Sie die Aktion in ein Seitenladereignis oder eine andere Ansicht verschieben, die bereits im Änderungs-Bedienfeld vorhanden ist. (TGT-33746)</li><li>Sie können viele Aktionen ausführen, bevor die Seite im VEC geladen wird, oder selbst dann, wenn die Seite nicht vollständig geladen werden kann (wenn beispielsweise benutzerdefinierter Code nicht mehr funktioniert). Aktionen, die nicht bearbeitet werden können, bevor die Website geladen ist, sind in der Benutzeroberfläche von Target deaktiviert. (TGT-33851 und TGT-34149)</li></ul>Weitere Informationen finden Sie unter [Visual Experience Composer für Einzelseiten-Apps (SPAs)](/help/c-experiences/spa-visual-experience-composer.md). |

### Verbesserungen, Fehlerbehebungen und Änderungen

* Die Symbole der Symbolleiste werden entsprechend angezeigt, nachdem Sie das Laden einer Seite innerhalb des VEC abgebrochen haben. Wenn bestimmte Aktionen erst nach dem vollständigen Laden der Seite ausgeführt werden können, werden die zugehörigen Symbolleistensymbole deaktiviert. (TGT-33811)

## Visual Experience Composer für Mobile Apps (14. Mai 2019) {#mobile-vec-may14-2}

| Funktion/Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer (VEC) für mobile Apps | Mit Mobile App VEC können Sie Aktivitäten erstellen und Inhalte auf nativen Mobil-Apps ohne ständige Entwicklungsabhängigkeiten und App-Versionszyklen personalisieren.<br>Weitere Informationen finden Sie unter:<ul><li>[Visual Experience Composer für mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS – Einrichten der App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Einrichten des Klick-Trackings im Mobile VEC](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li><li>[Video: Visual Experience Composer für Mobile Apps](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#video)</li></ul> |

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
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |