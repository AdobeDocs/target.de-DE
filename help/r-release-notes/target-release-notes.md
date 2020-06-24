---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Targets enthalten.
title: Hinweise zur Vorabversion des Adobe Targets
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: a6bcaac474927ddd0a14d4cb274c0460e6002a9b
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 15%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 24. Juni 2020**

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

Die gesamte [!DNL Target] Benutzeroberfläche wird schrittweise mit einem neuen technischen Stapel umgeschrieben, um eine höhere Performance zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu verkürzen und die Benutzerfreundlichkeit im gesamten Produkt zu verbessern. Der erste Abschnitt, der aktualisiert wurde, ist der Abschnitt [!UICONTROL Einstellungen] , der in [!UICONTROL Administration]umbenannt wurde.

Im Rahmen dieser Aktualisierung können Sie auf einfache Weise viele Aktionen mithilfe der Seiten im Abschnitt &quot; [!UICONTROL Verwaltung] &quot;durchführen, z. B.:

* Laden Sie die neueste Datei &quot;at.js&quot;von der Registerkarte &quot; [!UICONTROL Implementierung] &quot;herunter (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**).
* Passen Sie Ihre at.js-Einstellungen an und können Sie Ihre Änderungen ganz einfach überprüfen (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**).
* Ändern Sie erweiterte Einstellungen für Berichte wie Standardwährung und -zeit, IPs zum Ausschließen vom Berichte usw. (**[!UICONTROL Administration]** > **[!UICONTROL Berichte]**)
* IP-Adressen von Besuchern aus Datenschutzgründen verschleiern (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**)
* Ansicht der bestehenden Liste der Benutzer nach Arbeitsbereich und deren Rollen, bevor sie in Adobe Admin Console verwaltet werden (**[!UICONTROL Administration]** > **[!UICONTROL Benutzer]**).
* Suchen und filtern Sie alle Tabellen im Abschnitt &quot; [!UICONTROL Administration] &quot;.

Zu den bedeutsamen Änderungen gehören:

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
