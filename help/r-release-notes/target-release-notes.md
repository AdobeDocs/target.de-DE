---
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [! DNL Adobe Target] veröffentlicht.
keywords: Versionshinweise
seo-description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [! DNL Adobe Target] veröffentlicht.
seo-title: Versionshinweise zu Adobe Target (Vorabversion)
solution: Target
title: Target-Versionshinweise (Vorabversion)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 48d265feb329355f5aabe34a6a950d78df981966

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für die neuesten oder kommenden [!DNL Adobe Target]-Versionen.

**Zuletzt aktualisiert am 19. Juli 2019**

>[!NOTE]
>
>Diese Versionshinweise enthalten Vorabversionsinformationen. Veröffentlichungsdaten, Funktionen und andere Informationen können ohne vorherige Benachrichtigung geändert werden. Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Timing der Versionen identisch sein oder abweichen.
>
>Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Standard/Premium 19.7.1 (24. Juli 2019) {#tgt-19-7-1}

Dieses Release umfasst die folgenden neuen Funktionen und Erweiterungen:

| Funktion / Verbesserung | Beschreibung |
| --- | --- |
| Visual Experience Composer für mobile Apps | In der mobilen App-VEC wird ein neues Bedienfeld "Änderungen" angezeigt, in dem die Elemente angezeigt werden, die Sie für die Klick-Tracking eingerichtet haben. (TGT-31741) |
| ![Premium badgerecommenüationen](/help/assets/premium.png)<br>in A/B-Test- und Erlebnis-Targeting (XT)-Aktivitäten | Der Recommendations-Angebotsstatus (Algorithmus) wird auf der Seite Überblick für A/B-Test- und XT-Aktivitäten angezeigt, die Recommendations-Angebote enthalten. Zu den Status gehören: Ergebnisse bereit, Ergebnisse nicht bereit und Feed-Fehler. (TGT-33649) |
| Unterstützung domänenübergreifender Tracking-Unterstützung für at. js 2.0 + über die Experience Cloud ID (ECID)-Bibliothek | Zuvor wurde die domänenübergreifende Verfolgung in at. js 2 nicht unterstützt.*x*. Mit dieser Version können Kunden, die at. js 2.0 oder höher verwenden, jetzt domänenübergreifende Verfolgung über die ECID-Bibliothek nutzen. Die ECID-Bibliothek muss zusammen mit at. js 2.0 oder höher auf der Seite installiert sein, damit die domänenübergreifende Verfolgung funktioniert. [Die Experience Cloud ID-Bibliothek 4.3.0 +](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) muss verwendet werden. |
| Target-Unterstützung für ITP 2.1 und ITP 2.2 von Apple über die Experience Cloud ID (ECID)-Bibliothek 4.3 | Target-Kunden können die Apple ITP 2.1 und ITP 2.2 heute durch Nutzung des CNAME-Zertifizierungsprogramms von Adobe abschwächen. With this release, Target introduces a seamless integration with the ECID library 4.3, which leverages a server-side cookie to mitigate ITP 2.1 and ITP 2.2. It is highly recommended that Target customers deploy [ECID library 4.3+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) in conjunction with Target’s JavaScript library to mitigate any future ITP releases. Die ECID-Bibliothek wird weiterhin Verbesserungen an der Entwicklung vornehmen, die eine robuste Lösung für die sich ständig ändernden Cookie-Richtlinien bereitstellen, die von Browsern eingeführt wurden. |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
