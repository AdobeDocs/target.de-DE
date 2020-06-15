---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Targets enthalten.
title: Hinweise zur Vorabversion des Adobe Targets
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 781a89b68dcf6574522a3be118a1cc1c15a848a8
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 17%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 15. Juni 2020**

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


## Target Standard/Premium 20.5.1 (17. Juni 2020) 

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Analytics for Target (A4T) Unterstützung für Aktivitäten mit automatisierter Zuordnung | Mit der Juni-Version unterstützen die Tests zur automatischen Zuordnung [Analytics zum Target](/help/c-integrating-target-with-mac/a4t/a4t.md). Mit dieser Integration können Sie die Multi-Armed Bandit-Funktion der automatischen Zuordnung verwenden, um Traffic zu erfolgreichsten Erlebnissen zu steigern, während Sie eine Adobe Analytics-Zielmetrik und/oder Berichte- und Analyse-Funktionen von Adobe Analytics verwenden. Wenn Sie bereits A4T [für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben, sind Sie alle bereit! |
| Herausgeberrolle | Diese neue Rolle ähnelt der aktuellen Beobachterrolle (Aktivitäten können zwar Ansicht, aber nicht erstellt oder bearbeitet werden). Die Rolle &quot;Herausgeber&quot;verfügt jedoch über die zusätzliche Berechtigung zum Aktivieren von Aktivitäten. |
| A4T-Unterstützung am 25. [!DNL Analysis Workspace]<br>Juni 2020 | [!UICONTROL Analytics für Target] (A4T) wird jetzt in unterstützt [!DNL Analysis Workspace]. Im Bedienfeld [!UICONTROL &quot;] Analytics für Target (A4T)&quot;können Sie Ihre [!DNL Adobe Target] Aktivitäten und Erlebnisse in analysieren [!DNL Analysis Workspace].<br>Weitere Informationen finden Sie im Bedienfeld [&quot;](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics für Target (A4T)&quot;im *Analytics Tools-Handbuch*. |

### Verbesserungen, Fehlerbehebungen und Änderungen

* Es wurde ein Fehler behoben, der dazu führte, dass die Metrik &quot;Besucher&quot;in der Definition der Aktivität statt &quot;UniqueVisitors&quot;gespeichert wurde. (TGT-37098)
* Es wurde ein Fehler in der [!DNL Target] Benutzeroberfläche behoben, der dazu führte, dass die vertikale Bildlaufleiste auf der Seite &quot; [!UICONTROL Audiencen] &quot;nicht korrekt funktionierte. (TGT-36968)

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
