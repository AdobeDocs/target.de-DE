---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 6957eb88e2ee7d54fdad5afeaedf75b091b601e7
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 36%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 14. September 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.9.1 (14. September 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen.

* Es wurden Probleme behoben, die Kunden daran hinderten, sich beim [!UICONTROL Visual Experience Composer] (VEC) anzumelden, da in einigen Webbrowsern neue Sicherheitsrichtlinien für Drittanbieter-Cookies gelten. Dieses Problem wurde unter &quot;Seiten, die nicht im Visual Experience Composer (VEC) oder Enhanced Experience Composer (EEC) geladen werden, wenn Google Chrome Version 80+ verwendet wird&quot;in [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) erläutert.
* Es wurde ein Fehler behoben, der dazu führte, dass Angebotsnamen im VEC den Pfad des Angebots anstelle des Anzeigenamens des Angebots anzeigten. (TGT-41300)
* Es wurde ein Problem in [!DNL Recommendations] behoben, bei dem fälschlicherweise Änderungen der Entitäts-ID in einer Promotion in einer duplizierten Aktivität auf die ursprüngliche Aktivität angewendet wurden. (TGT-41482)
* Es wurde ein Fehler behoben, der verhinderte, dass die Schaltfläche &quot;Kriterien bearbeiten&quot;ordnungsgemäß auf der Seite [!UICONTROL Erlebnisse] für [!DNL Recommendations] -Aktivitäten im VEC angezeigt wurde. (TGT-39512)
* Fehlerkorrektur - Aktivitäten können jetzt synchronisiert werden, wenn sie dupliziert und in einen Test-Arbeitsbereich kopiert werden. (TGT-40686)
* Es wurde ein Problem behoben, das Änderungen an einem Selektor mit [Erlebnisfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md) bei Verwendung von &quot;[!UICONTROL Einfügen nach]&quot;im VEC verhinderte. (TGT-41802)
* Fehlerkorrektur - leere JSON-Inhalte in einem Angebot können jetzt an das Backend gesendet werden. [!DNL Target] sendet jetzt das JSON-Objekt, obwohl es leer ist. (TGT-41555)
* Es wurde ein Fehler behoben, der dazu führte, dass ältere [!DNL Analytics]-Berichte anstelle von [!DNL Analysis Workspace] geöffnet wurden, wenn Kunden beim Anzeigen eines Berichts auf &quot;[!UICONTROL In Analytics anzeigen]&quot;geklickt haben. (TGT-41867)
* Es wurde eine zusätzliche Klarstellung zur angezeigten Benutzeroberflächenmeldung hinzugefügt, wenn ein Kunde versucht, [!DNL Analytics] als Berichtsquelle (A4T) für eine [!UICONTROL Automated Personalization] -Aktivität auszuwählen. In der Meldung wird angegeben, dass &quot;[!DNL Target] die einzige unterstützte Quelle für [!UICONTROL Automated Personalization] -Aktivitäten ist.&quot; (TGT-41954)
* Es wurde eine zusätzliche Klarstellung zur Fehlermeldung hinzugefügt, wenn Kunden versuchen, Hosts durch &quot;Zeilenumbruch&quot;anstelle von Kommas zu trennen. (TGT-40671)
* Das Feld [!UICONTROL Typ] für Segmente wurde aktualisiert und enthält nun genau [!DNL Platform] und [!DNL AAM] ([!DNL Adobe Audience Manager]). (TGT-41328)
* Es wurde ein Fehler behoben, der dazu führte, dass sich die Operanden der Traffic-Quellen nach dem Klicken auf [!UICONTROL Speichern] änderten. (TGT-41408)
* Nach dem Speichern einer Zielgruppe &quot;Nur Aktivität&quot;(entweder regelbasiert oder kombiniert) lädt die Benutzeroberfläche jetzt die Auswahl [!UICONTROL Zielgruppe] mit angewendetem Filter &quot;Nur Aktivität&quot;. (TGT-41747).
* Es wurde ein Fehler behoben, der dazu führte, dass Zielgruppen, die aus der Quelle gelöscht wurden ([!DNL Adobe Experience Platform], [!UICONTROL AAM] usw.), weiterhin in der [!DNL Target] -Benutzeroberfläche angezeigt wurden.
* Der Seite [!UICONTROL Zielgruppen] wurde eine Filteroption hinzugefügt, mit der nur aus [!DNL Adobe Experience Platform] importierte Zielgruppen angezeigt werden. (TGT-41298)
* Es wurden verbesserte Optionen für die Barrierefreiheit der Tastatur in der Benutzeroberfläche [!UICONTROL Zielgruppen] hinzugefügt. (TGT-39927)
* Es wurde ein Fehler behoben, der dazu führte, dass sich die Daten einiger Aktivitäten &quot;[!UICONTROL Zuletzt aktualisiert]&quot;für spanische und japanische Kunden von der englischen Benutzeroberfläche unterschieden (wenn die Benutzeroberfläche auf Spanisch und Japanisch angezeigt wurde). (TGT-38980)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
