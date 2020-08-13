---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
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
* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;mit Würde fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder: Developer chat, migrate Adobe Target&#39;s mbox.js to at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite mit den Ankündigungen zur Zielgruppe finden Sie Informationen zu den kommenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## at.js 2.3.2 (24. Juli 2020)

Diese Version von at.js ist ein Maintenance Release und beinhaltet die folgende Fehlerbehebung:

* Fixed a bug when a script or code adds default property to the window or document.

## Target Standard/Premium 20.7.1 (27. Juli 2020) 

Dieses Release umfasst die folgenden Änderungen:

### [!UICONTROL Administration] section UI refresh

We are gradually rewriting the entire [!DNL Target] UI using a new tech stack to be able to offer improved performance, reduce the maintenance time required when releasing new features, and to improve the user experience across the product. The first section refreshed is the [!UICONTROL Setup] section, which has been renamed [!UICONTROL Administration].

As part of this refresh, you will be able to easily perform many actions using the pages in the [!UICONTROL Administration] section, such as:

* Download the latest at.js file from the [!UICONTROL Implementation] tab (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Customize your at.js settings and be able to easily review your changes (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Modify enhanced reporting settings, such as the default currency and time zone, IPs to exclude from reporting, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Berichte]**)
* Obfuscate visitor IP addresses for privacy reasons (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* View the existing list of users per workspace and their roles, before managing them in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Search and filter all tables in the [!UICONTROL Administration] section.

For more information, see [Administer Target Overview](/help/administrating-target/administrating-target.md).

### Verbesserungen, Korrekturen von Problemen und Änderungen

This release contains the following enhancements, fixes, and changes:

* Fixed an issue that prevented site preferences from being retained after refresh. (TGT-37239)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Einfügen nach] > [!UICONTROL Bild] nicht ordnungsgemäß mit SVG-Bildern (Scalable Vector Graphics) funktionierte. (TGT-37242)
* Es wurde ein Problem für Benutzer mit der Rolle [!UICONTROL Herausgeber] behoben, das das Löschen von Aktivitäten verhinderte. (TGT-37358)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer eine Aktivität bearbeiten konnten, wenn &quot; [!UICONTROL Alle meine Arbeitsbereiche] &quot;ausgewählt wurde. (TGT-37276)

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - serverseitige APIs der Zielgruppe](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu Adobe Targets serverseitigen APIs. |
| [Versionshinweise - Zielgruppe Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK &quot;Node.js&quot;. |
| [Versionshinweise - Zielgruppe Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Versionshinweise zum Java-SDK von Adobe Target. |
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
