---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Targets enthalten.
title: Hinweise zur Vorabversion des Adobe Targets
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 058828bbf3f13704d9e941563b7dab5259be6809
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 19%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 23. Juni 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Target-Aktivitäten ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie die Datei &quot;mbox.js&quot;in Adobe Target zu &quot;at.js&quot;](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.
   >
   >
* **Target-Mitteilungen**: Auf der Seite &quot;Ankündigungen zum Target&quot;finden Sie Informationen zu kommenden Ereignissen, einschließlich Target Skill Builder-Sitzungen, Entwicklerchats, Webinars und Target Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Target-Mitteilungen](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.6.1 (Juli 2020, genaues Datum TBD)

Diese Version umfasst die folgenden Verbesserungen:

### Analytics für Target (A4T)-Unterstützung für [!UICONTROL Auto-Target] -Aktivitäten

[!UICONTROL Auto-Target] -Aktivitäten unterstützen jetzt [Analytics für Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

Diese Integration nutzt fortschrittliches maschinelles Lernen, um aus mehreren leistungsstarken, von Marketingexperten definierten Erlebnissen auszuwählen, um Inhalte zu personalisieren und Konversionen zu fördern. Automatisches Targeting stellt das benutzerspezifische Erlebnis für jeden Besucher basierend auf seinem individuellen Kundenprofil und dem Verhalten voriger Besucher mit ähnlichen Profilen bereit.

Wenn Sie bereits A4T [für die Verwendung mit A/B-Test-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben, sind Sie alle bereit!

### [!UICONTROL Aktualisierung der Benutzeroberfläche des Administrationsbereichs]

Wir haben den [!UICONTROL Administrationsbereich] (früher [!UICONTROL Admin]) und seine Seiten aktualisiert, um Ihre Workflows einfacher und effizienter zu gestalten.

Zu den Highlights gehören:

* **[!UICONTROL Visual Experience Composer]-Seite **: Auf dieser neuen Seite (**[!UICONTROL Administration ]**>**[!UICONTROL Visual Experience Composer ]**) können Sie:

   * Konfigurieren Sie allgemeine Einstellungen für VEC (geben Sie die Standard-URL an, aktivieren Sie den [!UICONTROL Enhanced Experience Composer], laden Sie gemischte Inhalte und erstellen Sie Erlebnismomentaufnahmen im Flussdiagramm der Aktivität)
   * Mobile Viewports konfigurieren
   * CSS-Selektoren konfigurieren

* **[!UICONTROL Berichte]-Seite **: Auf dieser neuen Seite (**[!UICONTROL Administration ]**>**[!UICONTROL Berichte ]**) können Sie allgemeine Einstellungen konfigurieren, die in[!DNL Target]Berichte verwendet werden, die für Ihr gesamtes[!DNL Target]Konto gelten.

   Zu den verfügbaren Einstellungen gehören:

   * Die [!DNL Adobe Experience Cloud] für den Berichte zu verwendende Lösung
   * Die für den Berichte zu verwendende Zeitzone
   * Die für den Berichte zu verwendende Währung
   * IP-Adressen, die vom Berichte ausgeschlossen werden
   * Zeigt eine geschätzte Umsatzsteigerung im Berichte an
   * Eignung für genau festgelegte Prioritäten

* Die vorherige [!UICONTROL Hostingseite] wurde in zwei neue Seiten unterteilt:

   * [!UICONTROL Hosts]
   * [!UICONTROL Umgebung]

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
