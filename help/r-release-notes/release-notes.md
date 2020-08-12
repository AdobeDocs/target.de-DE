---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
feature: null
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 30%

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!IMPORTANT]
>
>* **Adobe nochmal als Führer im Gartner Magic Quadrant für Personalisierungsmaschinen**: Adobe wurde im dritten Gartner Magic Quadrant for Personalization Engines 2020-Bericht erneut zum Leader ernannt. Der Gartner Magic Quadrant for Personalization Engines bewertete Anbieter anhand von 15 Kriterien, die in zwei Kategorien unterteilt sind: Vollständigkeit der Sicht und Ausführungsfähigkeit. [Lesen Sie mehr darüber im Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;mit Würde fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite mit den Ankündigungen zur Zielgruppe finden Sie Informationen zu den kommenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## at.js 2.3.2 (24. Juli 2020)

Diese Version von at.js ist ein Maintenance Release und beinhaltet die folgende Fehlerbehebung:

* Es wurde ein Fehler behoben, der auftrat, wenn ein Skript oder Code dem Fenster oder Dokument die Standardeigenschaft hinzufügt.

## Target Standard/Premium 20.7.1 (27. Juli 2020) 

Dieses Release umfasst die folgenden Änderungen:

### [!UICONTROL Aktualisierung der Benutzeroberfläche des Administrationsbereichs]

Die gesamte [!DNL Target] Benutzeroberfläche wird schrittweise mit einem neuen technischen Stapel umgeschrieben, um eine höhere Performance zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu verkürzen und die Benutzerfreundlichkeit im gesamten Produkt zu verbessern. Der erste Abschnitt, der aktualisiert wurde, ist der Abschnitt [!UICONTROL Einstellungen] , der in [!UICONTROL Administration]umbenannt wurde.

Im Rahmen dieser Aktualisierung können Sie auf einfache Weise viele Aktionen mithilfe der Seiten im Abschnitt &quot; [!UICONTROL Verwaltung] &quot;durchführen, z. B.:

* Laden Sie die neueste Datei &quot;at.js&quot;von der Registerkarte &quot; [!UICONTROL Implementierung] &quot;herunter (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**).
* Passen Sie Ihre at.js-Einstellungen an und können Sie Ihre Änderungen ganz einfach überprüfen (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**).
* Modify enhanced reporting settings, such as the default currency and time zone, IPs to exclude from reporting, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Berichte]**)
* IP-Adressen von Besuchern aus Datenschutzgründen verschleiern (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**)
* Ansicht der bestehenden Liste der Benutzer nach Arbeitsbereich und deren Rollen, bevor sie in Adobe Admin Console verwaltet werden (**[!UICONTROL Administration]** > **[!UICONTROL Benutzer]**).
* Suchen und filtern Sie alle Tabellen im Abschnitt &quot; [!UICONTROL Administration] &quot;.

Weitere Informationen finden Sie unter Übersicht über [Zielgruppen verwalten](/help/administrating-target/administrating-target.md).

### Verbesserungen, Korrekturen von Problemen und Änderungen

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass Site-Voreinstellungen nach der Aktualisierung beibehalten wurden. (TGT-37239)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Einfügen nach] > [!UICONTROL Bild] nicht ordnungsgemäß mit SVG-Bildern (Scalable Vector Graphics) funktionierte. (TGT-37242)
* Es wurde ein Problem für Benutzer mit der Rolle [!UICONTROL Herausgeber] behoben, das das Löschen von Aktivitäten verhinderte. (TGT-37358)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer eine Aktivität bearbeiten konnten, wenn &quot; [!UICONTROL Alle meine Arbeitsbereiche] &quot;ausgewählt wurde. (TGT-37276)

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Release notes - Target server-side APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Release notes related to Adobe Target&#39;s server-side APIs. |
| [Release notes - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK &quot;Node.js&quot;. |
| [Release Notes - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Release notes related to Adobe Target&#39;s Java SDK. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der Adobe Target at.js JavaScript-Bibliothek. |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek &quot;mbox.js&quot;nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter Versionshinweise zu [Experience Cloud](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
