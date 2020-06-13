---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Versionshinweise, die Informationen zu Funktionen, Verbesserungen und Fehlerbehebungen in den neuesten oder künftigen DNL-Adobe Target-Versionen enthalten.
title: Versionshinweise zu Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: bd39d7b6121eb6ccbfeb49d73a8b57618cc964ef
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 17%

---


# Target-Versionshinweise (Vorabversion){#target-release-notes-prerelease}

Dieser Artikel enthält Informationen zur Vorabversion. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 12. Juni 2020**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Zeitpunkt der Veröffentlichung identisch sein. Die Ausgabennummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!NOTE]
>
>* **&quot;mbox.js&quot;-Einstellung**: Am 30. August 2020 wird die Bibliothek &quot;mbox.js&quot;von Adobe Target nicht mehr unterstützt. Nach dem 30. August 2020 schlagen alle Aufrufe von &quot;mbox.js&quot;fehl und wirken sich auf die Seiten aus, auf denen Aktivitäten zur Zielgruppe ausgeführt werden. Es wird empfohlen, dass alle Kunden vor diesem Datum zur neuesten Version der at.js-Bibliothek migrieren, um potenzielle Probleme mit Ihren Sites zu vermeiden. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). Siehe *Adobe Target Skill Builder: Entwickler-Chat, migrieren Sie die Datei &quot;mbox.js&quot;von Adobe Target zu &quot;at.js* &quot;weiter unten.
   >
   >   
   Obwohl &quot;mbox.js&quot;derzeit unterstützt wird, wurden seit Juli 2017 keine Funktionsaktualisierungen dieser Bibliothek bereitgestellt. Die neuere at.js bietet viele Vorteile gegenüber mbox.js. Neben anderen Vorteilen verbessert at.js die Seitenladezeit für Webimplementierungen, verbessert die Sicherheit und bietet bessere Implementierungsoptionen für Einzelseitenanwendungen.
   >
   >   
   Indem wir alle Kunden zu at.js verschieben, können unsere Ingenieure und Support-Mitarbeiter Ihnen neue Funktionen und Angebote anbieten, die Sie von Adobe erwarten.
   >
   >
* **Mitteilungen** zur Zielgruppe: Auf der Seite mit den Ankündigungen zur Zielgruppe finden Sie Informationen zu den kommenden Ereignissen, einschließlich Zielgruppe Skill Builder-Sitzungen, Entwicklerchats, Webinars und Zielgruppe Coffee Break-Sitzungen. Weitere Informationen finden Sie unter [Ankündigungen](/help/r-release-notes/target-announcements.md)der Zielgruppe.


## Versionen von &quot;at.js&quot;1.8.2 und &quot;at.js 2.3.1&quot;(15. Juni 2020)

Die folgenden Verbesserungen und Fehlerbehebungen wurden in den [!DNL Target] at.js-Bibliotheken vorgenommen:

### at.js 1.8.2

* Es wurde ein Problem bei der Verwendung von CNAME und Edge Override von at.js 1 behoben.*x* erstellt die Serverdomäne möglicherweise falsch, was dazu führte, dass die [!DNL Target] Anforderung fehlschlug. (TNT-35064)

### at.js 2.3.1

* Die `deviceIdLifetime` Einstellung wurde über [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)überschrieben. (TNT-36349)
* Es wurde ein Problem bei der Verwendung von CNAME und Edge Override von at.js 2 behoben.*x* erstellt die Serverdomäne möglicherweise falsch, was dazu führte, dass die [!DNL Target] Anforderung fehlschlug. (TNT-35065)
* Es wurde ein Problem behoben, das bei Verwendung der [!DNL Target] Erweiterung [!DNL Launch] v2 und der [!DNL Adobe Analytics] Erweiterung [!DNL Launch] den [!DNL Target][!DNL Analytics] `sendBeacon` Aufruf verzögerte. (TNT-36407, TNT-35990, TNT-36000)

## Target Standard/Premium 20.5.1 (17. Juni 2020) 

| Funktion  / Verbesserung | Beschreibung |
| --- | --- |
| Analytics for Target (A4T) Unterstützung für Aktivitäten mit automatisierter Zuordnung | Ab der Juni-Version unterstützen Tests mit automatisierter Zuordnung [Analytics für die Zielgruppe](/help/c-integrating-target-with-mac/a4t/a4t.md). Mit dieser Integration können Sie die Multi-Armed Bandit-Funktion der automatischen Zuordnung verwenden, um Traffic zu erfolgreichsten Erlebnissen zu steigern, während Sie eine Adobe Analytics-Zielmetrik und/oder Adobe Analytics-Berichte- und -Analysen-Funktionen verwenden. Wenn Sie bereits A4T [für die Verwendung mit A/B-Test- und Erlebnis-Targeting-Aktivitäten](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) implementiert haben, sind Sie alle bereit! |
| Herausgeberrolle | Diese neue Rolle ähnelt der aktuellen Beobachterrolle (Aktivitäten können zwar Ansicht, aber nicht erstellt oder bearbeitet werden). Die Rolle &quot;Herausgeber&quot;verfügt jedoch über die zusätzliche Berechtigung zum Aktivieren von Aktivitäten. |

## Vorabinformationen zu Versionen{#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
