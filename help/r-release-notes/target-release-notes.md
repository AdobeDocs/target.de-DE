---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen Versionen der DNL-Adobe-Zielgruppe enthalten.
title: Versionshinweise zu Adobe Zielgruppe
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 7857b9765a9338405b6705046333f11f8255b365
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 20%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 27. Mai 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Zielgruppe nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Siehe *Adobe Zielgruppe Skill Builder: Entwickler-Chat, migrieren Sie unten die Datei &quot;mbox.js&quot;der Adobe-Zielgruppe zu &quot;at.js&quot;* .
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.


## Adobe Zielgruppe Skill Builder: Entwickler-Chat, migrieren Sie &quot;mbox.js&quot;der Adobe-Zielgruppe in &quot;at.js&quot; {#skill-builder}

Mit der bevorstehenden Vernichtung von &quot;mbox.js&quot;am 30. August 2020 hat David Son, Adobe Zielgruppe Product Manager, kürzlich einen Entwicklerchat gehostet, um die Vorteile der Migration von &quot;mbox.js&quot;auf &quot;at.js&quot;zu erörtern. In den nächsten 30 Tagen können Sie die Aufzeichnung des Webinars [Ansicht](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true)leisten.

## Target Standard/Premium 20.6.1 (10. Juni 2020) 

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Analytics for Target (A4T) Unterstützung für Aktivitäten mit automatisierter Zuordnung | Ab der Juni-Version unterstützen Tests mit automatisierter Zuordnung [Analytics für die Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md). Mit dieser Integration können Sie die Multi-Armed Bandit-Funktion der automatischen Zuordnung verwenden, um Traffic zu erfolgreichsten Erlebnissen zu steigern, während Sie eine Adobe Analytics-Zielmetrik und/oder Adobe Analytics-Berichte- und -Analysen-Funktionen verwenden. Wenn Sie bereits A4T [für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben, sind Sie alle bereit! |
| Herausgeberrolle | Diese neue Rolle ähnelt der aktuellen Beobachterrolle (Aktivitäten können zwar Ansicht, aber nicht erstellt oder bearbeitet werden). Die Rolle &quot;Herausgeber&quot;verfügt jedoch über die zusätzliche Berechtigung für aktive Aktivitäten. |
| Administrationsseite<br>zuvor &quot;Setup&quot;. | Die Seite &quot;Einstellungen&quot;wurde in &quot;Administration&quot;umbenannt und die Benutzeroberfläche für alle Menüelemente wurde aktualisiert, um den Arbeitsablauf und die Benutzerfreundlichkeit zu verbessern.<br>Zu den verfügbaren Menüpunkten gehören:<ul><li>Visual Experience Composer</li><li>Berichterstellung</li><li>Scene7-Einstellungen</li><li>Implementierung</li><li>Properties</li><li>Hosts</li><li>Umgebung</li><li>Antwort-Token</li><li>Benutzer</li></ul> |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
