---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen, Fehlerbehebungen und bekannten Problemen für jede Adobe Target Standard- und Target Premium-Version.
title: 'Adobe Target-Versionshinweise (aktuell) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: d45a38376ebe98d212fba3097159a7b89b792c53

---


# Target-Versionshinweise (aktuell){#target-release-notes-current}

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen für jede Target Standard- und Target Premium-Version. Zusätzlich werden gegebenenfalls Versionshinweise für Zielgruppen-APIs, SDKs, die JavaScript-Bibliothek (at.js) und andere Plattformänderungen einbezogen.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Zielgruppe nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Siehe *Adobe Zielgruppe Skill Builder: Entwickler-Chat, migrieren Sie &quot;mbox.js&quot;der Adobe-Zielgruppe zu &quot;at.js* &quot;unten, um Informationen zur Registrierung für einen demnächst erscheinenden Entwickler-Chat zu diesem Thema zu erhalten.
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.


Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Adobe Zielgruppe Skill Builder: Entwickler-Chat, migrieren Sie &quot;mbox.js&quot;der Adobe-Zielgruppe in &quot;at.js&quot; {#skill-builder}

Lernen Sie David Son, Adobe Zielgruppe Product Manager kennen, der die Vorteile der Migration von &quot;mbox.js&quot;auf &quot;at.js&quot;erläutert. Erfahren Sie mehr über die neuesten at.js-Updates, die verbesserten Funktionen und die Abstimmung mit größeren Trends im Technologiebereich. Außerdem erhalten Sie praktische Tipps, wie Sie bei der Migration von &quot;mbox.js&quot;zu &quot;at.js&quot;einen optimalen Nutzen aus der Zielgruppe ziehen können. Adobe Zielgruppe Developers wird dies nicht verpassen!

Dienstag, 5. Mai, 8:00 - 9:00 Uhr (PDT)

[Melden Sie sich jetzt hier an!](https://atskillbuilder-devchat.experienceleague.adobeevents.com/)

## Target Standard/Premium 20.4.1 (27. April 2020)

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Problem behoben, durch das Geräte- und Browsertypen für eine Audience fälschlicherweise qualifiziert wurden. (TGT-36266)
* Es wurde ein Fehler behoben, der verhinderte, dass Berichtsdaten angezeigt wurden, wenn sie auf Bildschirmen mit einer Breite von weniger als 963 Pixeln angezeigt wurden. (TGT-36549)
* Es wurde ein Fehler behoben, der dazu führte, dass Berichte zur automatischen Personalisierung nicht korrekt dargestellt wurden. (TGT-36619)
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
| [Versionshinweise - serverseitige APIs der Zielgruppe](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Versionshinweise zu den serverseitigen APIs von Adobe Zielgruppe. |
| [Versionshinweise - Zielgruppe Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Versionshinweise zum Node.js-SDK der Adobe-Zielgruppe. |
| [Versionshinweise - Zielgruppe Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Versionshinweise zum Java-SDK der Adobe Zielgruppe. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der JavaScript-Bibliothek &quot;at.js&quot;der Adobe-Zielgruppe. |
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
