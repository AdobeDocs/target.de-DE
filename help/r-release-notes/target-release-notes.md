---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
title: Versionshinweise zu Adobe Target
feature: null
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 405715f1ee1afd1d298dc7f1ef0cd3599620cbca
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 11%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 31. August 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>* **Adobe nochmal als Führer im Gartner Magic Quadrant für Personalisierungsmaschinen**: Adobe wurde im dritten Gartner Magic Quadrant for Personalization Engines 2020-Bericht erneut zum Leader ernannt. Der Gartner Magic Quadrant for Personalization Engines bewertete Anbieter anhand von 15 Kriterien, die in zwei Kategorien unterteilt sind: Vollständigkeit der Sicht und Ausführungsfähigkeit. [Lesen Sie mehr darüber im Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **&quot;mbox.js&quot;-Einstellung**: Am 18. Januar 2021 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 18. Januar 2021 schlagen alle von &quot;mbox.js&quot;ausgeführten Aufrufe korrekt fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie Adobe Targets mbox.js zu at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von der Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite mit den Ankündigungen zur Zielgruppe finden Sie Informationen zu den kommenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


## Target Standard/Premium 20.8.1 (2. September 2020)

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der dazu führte, dass beim Laden der neuen [!UICONTROL Administrationsseiten] nach dem Wechsel der Organisation Fehler angezeigt wurden. (TGT-37730)
* Korrektur eines Anzeigefehlers, der dazu führte, dass auf der Seite [!UICONTROL Administration > Implementierung] der falsche Clientcode angezeigt wurde. (TGT-37849)
* Es wurde ein Problem behoben, das Benutzer manchmal daran hinderte, die Bearbeitungsfunktionen im [!UICONTROL Visual Experience Composer] (VEC) zu verwenden, nachdem VEC erfolgreich geladen wurde. (TGT-37162)
* Es wurde ein Fehler behoben, der verhinderte, dass Seiten in VEC und Enhanced Experience Composer (EEC) geladen wurden, obwohl die VEC Helper-Erweiterung installiert war. Dies war auf Änderungen in Google Chrome 80+ zurückzuführen. Laden Sie die [aktualisierte VEC Helper-Erweiterung](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)herunter. (TGT-37893)
* Es wurde ein Problem behoben, das manchmal verhinderte, dass Benutzer at.js von der Seite [!UICONTROL Administration > Implementierung] herunterladen konnten, nachdem sie das Unternehmen gewechselt hatten. (TGT-37668)
* Die Download-Schaltfläche von at.js ist jetzt beim Laden deaktiviert, um zu verhindern, dass mehrere Anforderungen gesendet werden, wenn Benutzer mehrmals auf die Download-Schaltfläche klicken. [!DNL Target] (TGT-37633)
* Es wurde ein Fehler in den Aktivitäten [!UICONTROL Erlebnis-Targeting] (XT) behoben, der dazu führte, dass Erlebnisse über einen längeren Zeitraum &quot;Ergebnisse abrufen&quot;angezeigt wurden. (TGT-37684)
* Verbesserte Navigation und Funktionalität für Benutzer, die nur über Tastatur verfügen. (TGT-34479 und TGT-34473)
* Es wurden Beschriftungen in der Benutzeroberfläche hinzugefügt, um Benutzern mithilfe von Hilfstechnologien zu helfen. (TGT-34480)
* Die Fehlermeldung beim Löschen eines mobilen Viewports, der derzeit in einer Aktivität verwendet wird, wurde verbessert. Die Fehlermeldung lautet jetzt: &quot;Dieser Viewport ist derzeit einer oder mehreren Aktivitäten zugeordnet. Sie müssen den Viewport aus diesen Aktivitäten entfernen, bevor Sie ihn löschen können.&quot; (TGT-37030)
* Unterstützung im VEC hinzugefügt, um die Klick-Verfolgung auf einem CSS-Selektor zuzulassen, der mehr als einem Element auf der Seite entspricht. (TGT-37323)
* Es wurde ein Fehler behoben, der verhinderte, dass bestimmte Benutzer die Liste [!UICONTROL Aktivität] anzeigen konnten. Die folgende Fehlermeldung wurde angezeigt: &quot;URL-Vorschläge können nicht abgerufen werden.&quot; Der Fehler trat bei Benutzern auf, die Wagenrückgaben in ihrem Vornamen (Vorname/r/n) im Backend-System der Adobe verwenden. (TGT-37330)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer die Seite &quot; [!UICONTROL Aktivität] &quot;anzeigen konnten, wenn der Arbeitsflächenname (in [!UICONTROL Adobe Admin Console für Enterprise]angegeben) einen Apostroph enthielt. (TGT-37709)
* Es wurde ein Problem in den Aktivitäten zur [!UICONTROL automatischen Zuordnung] bei der Auswahl von Optimierungs- und Konversionsmetriken behoben, bei dem eine Fehlermeldung fälschlicherweise die Benutzer zur Auswahl einer Report Suite informierte, obwohl bereits eine Report Suite angegeben wurde. (TGT-37689)
* Es wurde ein Fehler behoben, der manchmal dazu führte, dass Metriken auf der Seite &quot; [!UICONTROL Ziele und Einstellungen] &quot;leer waren, nachdem sie zur Seite &quot; [!UICONTROL Targeting] &quot;und dann zurück navigiert wurden. (TGT-37691)
* Es wurde ein Problem behoben, das einen falschen Wert für die zuletzt geänderte Version für [!DNL Recommendations] Kriterien verursachte. (TGT-37666)
* Es wurde ein Fehler behoben, der dazu führte, dass Mbox-IDs in der Dropdown-Liste &quot;Mboxes&quot;anstelle von Mbox-Namen angezeigt wurden. (TGT-37739)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
