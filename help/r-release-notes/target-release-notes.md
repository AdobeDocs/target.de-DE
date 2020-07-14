---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Targets enthalten.
title: Hinweise zur Vorabversion des Adobe Targets
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 7f23f80a0528ea2e6de78a5491c87ca72862813d
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 16%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am 13. Juli 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;mit Würde fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden, indem Standardinhalte bereitgestellt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Funktionsweise](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) von &quot;at.js&quot;und [Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie die Datei &quot;mbox.js&quot;in Adobe Target zu &quot;at.js&quot;](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite &quot;Ankündigungen&quot;der Zielgruppe finden Sie Informationen zu den bevorstehenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


## Target Standard/Premium 20.7.1 (21. Juli 2020) 

Diese Version umfasst die folgenden Verbesserungen:

### [!UICONTROL Aktualisierung der Benutzeroberfläche des Administrationsbereichs]

Die gesamte [!DNL Target] Benutzeroberfläche wird schrittweise mit einem neuen technischen Stapel umgeschrieben, um eine höhere Performance zu erzielen, die Wartungszeit bei der Veröffentlichung neuer Funktionen zu verkürzen und die Benutzerfreundlichkeit im gesamten Produkt zu verbessern. Der erste Abschnitt, der aktualisiert wurde, ist der Abschnitt [!UICONTROL Einstellungen] , der in [!UICONTROL Administration]umbenannt wurde.

Im Rahmen dieser Aktualisierung können Sie auf einfache Weise viele Aktionen mithilfe der Seiten im Abschnitt &quot; [!UICONTROL Verwaltung] &quot;durchführen, z. B.:

* Laden Sie die neueste Datei &quot;at.js&quot;von der Registerkarte &quot; [!UICONTROL Implementierung] &quot;herunter (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**).
* Passen Sie Ihre at.js-Einstellungen an und können Sie Ihre Änderungen ganz einfach überprüfen (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**).
* Ändern Sie erweiterte Einstellungen für Berichte wie Standardwährung und -zeit, IPs zum Ausschließen vom Berichte usw. (**[!UICONTROL Administration]** > **[!UICONTROL Berichte]**)
* IP-Adressen von Besuchern aus Datenschutzgründen verschleiern (**[!UICONTROL Administration]** > **[!UICONTROL Implementierung]**)
* Ansicht der bestehenden Liste der Benutzer nach Arbeitsbereich und deren Rollen, bevor sie in Adobe Admin Console verwaltet werden (**[!UICONTROL Administration]** > **[!UICONTROL Benutzer]**).
* Suchen und filtern Sie alle Tabellen im Abschnitt &quot; [!UICONTROL Administration] &quot;.

### Verbesserungen, Korrekturen von Problemen und Änderungen

Diese Version enthält die folgenden Erweiterungen, Fehlerbehebungen und Änderungen:

* Es wurde ein Fehler behoben, der verhinderte, dass Site-Voreinstellungen nach der Aktualisierung beibehalten wurden. (TGT-37239)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Einfügen nach] > [!UICONTROL Bild] nicht ordnungsgemäß mit SVG-Bildern (Scalable Vector Graphics) funktionierte. (TGT-37242)
* Es wurde ein Problem für Benutzer mit der Rolle [!UICONTROL Herausgeber] behoben, das das Löschen von Aktivitäten verhinderte. (TGT-37358)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer eine Aktivität bearbeiten konnten, wenn &quot; [!UICONTROL Alle meine Arbeitsbereiche] &quot;ausgewählt wurde. (TGT-37276)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
