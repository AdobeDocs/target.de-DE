---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen Versionen der DNL-Adobe-Zielgruppe enthalten.
title: Versionshinweise zu Adobe Zielgruppe
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 1d34000b446c0fd37c6894bf5066f3cd16fc92a7

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 25. März 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Zielgruppe nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.


## Zielgruppe at.js (25. März 2020)

Die folgenden neuen Versionen der JavaScript-Bibliotheken der Zielgruppe &quot;at.js&quot;sind verfügbar:

* at.js Version 2.3.0
* at.js Version 1.8.1

For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## Target Standard/Premium 20.2.1 (23. März 2020) 

>[!IMPORTANT]
>
>Siehe Informationen über die Einstellung von &quot;mbox.js&quot;.

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass Kunden beim Durchführen einer Katalogsuche eine Sammlung auswählen konnten. (TGT-36230)
* Es wurde ein Problem behoben, durch das Kriterien, die über API erstellt wurden, aber nicht von einer in der Benutzeroberfläche der Zielgruppe erstellten Aktivität referenziert wurden, fälschlicherweise aus der Benutzeroberfläche gelöscht werden konnten. (TGT-35917)
* Implementierung von Sicherheitsverbesserungen in Content Security Policy (CSP). (TGT-36190)
* Es wurde ein Fehler behoben, der dazu führte, dass &quot;NaN%&quot;angezeigt wurde, wenn die prozentuale Attributgewichtung nach links verschoben wurde. (TGT-36211)
* Es wurden Probleme mit der lokale Anpassung behoben, sodass der Benutzeroberflächentext in verschiedenen Sprachen korrekt angezeigt wird.
* Wir haben die Liste der verfügbaren Metriken aus Adobe Analytics für die Zielgruppe (A4T)-Aktivitäten standardisiert, indem Adobe Analytics-Metriken, die in der aktuellen Version der Adobe Analytics-APIs nicht unterstützt werden, nicht mehr unterstützt werden. Auf diese Weise können wir unsere A4T-Unterstützung in zukünftigen Adobe-Zielgruppen erweitern.

   Folgende Änderungen wurden vorgenommen:

   * &quot;Durchschnittliche Besuchszeit pro Seite&quot;wurde durch &quot;Durchschnittliche Besuchszeit pro Site&quot;ersetzt. Alle Aktivitäten, die diese Metrik als Metrik für primäre Ziele verwenden, haben &quot;Durchschnittliche Besuchszeit pro Site&quot;(Hinweis: in Minuten statt in Sekunden), die beim nächsten Bearbeiten der Aktivität als primäre Zielmetrik ausgewählt wurde.
   * &quot;Besucher&quot;wurde durch &quot;Individuelle Besucher&quot;ersetzt. Bei allen Aktivitäten, die diese Metrik als primäre Zielmetrik verwenden, wird beim nächsten Bearbeiten der Aktivität &quot;Individuelle Besucher&quot;als primäre Zielmetrik ausgewählt.

* Die folgenden Metriken wurden nicht mehr unterstützt und können nicht mehr als primäre Zielmetrik beim Erstellen einer neuen A4T-Aktivität ausgewählt werden.

   | Veraltete Metriken | Vorgeschlagene Ersatzmetriken |
   |--- |--- |
   | Tägliche Besucher, stündliche Besucher, monatliche Besucher, vierteljährliche Besucher, wöchentliche Besucher, jährliche Besucher | Unique Visitors |
   | Durchschnittliche Besuchstiefe | entfällt. Nicht als primäre Zielmetrik vorgeschlagen |
   | Bots | entfällt. Nicht als primäre Zielmetrik vorgeschlagen |
   | Absturzrate für Mobilgeräte, durchschnittliche Länge der vorherigen Sitzung, Durchschn. Avg. Rang für den Mobile App Store, Absturzrate für Mobilanwendungen, Durchschn. Bewertung für den App Store | entfällt. Nicht als primäre Zielmetrik vorgeschlagen |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
