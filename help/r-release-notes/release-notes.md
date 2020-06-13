---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 25f7ce65f4f9b863ce6ebfe0a7ff8df08e561741
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 32%

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie die Datei &quot;mbox.js&quot;von Adobe Target in &quot;at.js&quot;](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite mit den Ankündigungen zur Zielgruppe finden Sie Informationen zu den kommenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Änderungen an Profil Batch Status API, Version 2 (14. Mai 2020)

Ab der Version vom 20. Mai gibt der Profil Batch-Status nur noch Fehlerdaten auf Zeilenebene zurück (Erfolgsdaten werden nicht zurückgegeben). Fehlgeschlagene Profil-IDs werden von der API in Zukunft zurückgegeben.

Die vorherigen und neuen API-Antworten lauten wie folgt:

`ProfileBatchStatus Api
http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Zurzeit sehen wir die Antwort wie folgt:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**Nach dem 4. Mai lautet die Antwort:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

## Target Standard/Premium 20.4.1 (6. Mai 2020) 

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Problem behoben, durch das Geräte- und Browsertypen für eine Audience fälschlicherweise qualifiziert wurden. (TGT-36266)
* Es wurde ein Fehler behoben, der verhinderte, dass Berichtsdaten angezeigt wurden, wenn sie auf Bildschirmen mit einer Breite von weniger als 963 Pixeln angezeigt wurden. (TGT-36549)
* Es wurde ein Fehler behoben, der dazu führte, dass Berichte zur automatischen Personalisierung nicht korrekt dargestellt wurden. (TGT-36619)
* Es wurde ein Fehler behoben, der dazu führte, dass inkompatible Metriken in Aktivitäten für die automatische Zuordnung und automatische Zielgruppe ausgewählt wurden, die Analytics für die Zielgruppe (A4T) verwenden. (TGT-36646)
* Es wurde ein Fehler behoben, der dazu führte, dass bestimmte Optionen im Visual Experience Composer (VEC) nicht korrekt angezeigt wurden. (TGT-36571)
* Es wurde ein Fehler in der Benutzeroberfläche der Zielgruppe behoben, der dazu führte, dass andere Recommendations-Angebot-Vorschauen den bearbeiteten Inhalt anzeigten, nachdem ein Benutzer den Inhalt in einem Erlebnis ersetzt hatte. (TGT-36053 und TGT-36894)
* Es wurde ein Fehler behoben, der verhinderte, dass einige Benutzer Elemente aus einem Recommendations-Katalog löschen konnten. (TGT-36455)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer Recommendations-Kriterien auf einer mehrseitigen Aktivität speichern konnten. (TGT-36249)
* Es wurde ein Fehler behoben, der dazu führte, dass die Optionsfelder der verhaltensbasierten Datenquelle beim Bearbeiten der Kriterien eine zweite aufeinander folgende Zeit lang ausgeblendet wurden. (TGT-36796)
* Es wurde ein Anzeigeproblem behoben, das dazu führte, dass ein Recommendations-Algorithmus &quot;Ergebnisse abrufen&quot;für einen längeren Zeitraum anzeigte. (TGT-36550 und TGT-36551)
* Viele in verschiedenen Sprachen lokalisierte Benutzeroberflächenzeichenfolgen wurden aktualisiert.

## Zusätzliche Versionshinweise und Versionshinweise

| Ressource | Details |
|--- |--- |
| [Versionshinweise - serverseitige APIs der Zielgruppe](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu den serverseitigen APIs von Adobe Target. |
| [Versionshinweise - Zielgruppe Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Adobe Target-SDK Node.js. |
| [Versionshinweise - Zielgruppe Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Versionshinweise zum Java-SDK von Adobe Target. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der JavaScript-Bibliothek von Adobe Target &quot;at.js&quot;. |
| [„mbox.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Auf dieser Seite sind die Änderungen bei jeder Version von mbox.js aufgeführt.<br>Beachten Sie, dass die Bibliothek &quot;mbox.js&quot;nicht mehr entwickelt wird. Alle Kunden sollten eine Migration von mbox.js zu at.js durchführen. |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise {#section_1BC5F5208DA548E9B4344A0836E4B943}

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Zeigen Sie detaillierte Informationen zu Aktualisierungen in diesem Benutzerhandbuch an, die möglicherweise nicht in den Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie unter [Experience Cloud-Versionshinweise](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Informationen vor der Versionsveröffentlichung {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Liste der priorisierten Adobe-Produktaktualisierungen | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
