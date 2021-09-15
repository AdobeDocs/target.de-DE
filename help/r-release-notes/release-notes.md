---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5a5b39db9b9b4ffd95573d643dcff52fe562c0c2
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 57%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs, der [!DNL Adobe Experience Platform Web SDK] und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek „at.js“, um mögliche Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## [!DNL Target Standard/Premium] 21.9.1 (14. September 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen.

* Es wurden Probleme behoben, die Kunden daran hinderten, sich beim [!UICONTROL Visual Experience Composer] (VEC) anzumelden, da in einigen Webbrowsern neue Sicherheitsrichtlinien für Drittanbieter-Cookies gelten. Dieses Problem wurde unter &quot;Seiten, die nicht im Visual Experience Composer (VEC) oder Enhanced Experience Composer (EEC) geladen werden, wenn Google Chrome Version 80+ verwendet wird&quot;in [Beheben von Problemen mit Visual Experience Composer und Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) erläutert.
* Es wurde ein Fehler behoben, der dazu führte, dass Angebotsnamen im VEC den Pfad des Angebots anstelle des Anzeigenamens des Angebots anzeigten. (TGT-41300)
* Erlebnisnamen werden jetzt in [!DNL Analysis Workspace] für A4T-Aktivitäten angezeigt (TGT-38674).
* Es wurde ein Problem in [!DNL Recommendations] behoben, bei dem fälschlicherweise Änderungen der Entitäts-ID in einer Promotion in einer duplizierten Aktivität auf die ursprüngliche Aktivität angewendet wurden. (TGT-41482)
* Es wurde ein Fehler behoben, der verhinderte, dass die Schaltfläche &quot;Kriterien bearbeiten&quot;ordnungsgemäß auf der Seite [!UICONTROL Erlebnisse] für [!DNL Recommendations] -Aktivitäten im VEC angezeigt wurde. (TGT-39512)
* Fehlerkorrektur - Aktivitäten können jetzt synchronisiert werden, wenn sie dupliziert und in einen Test-Arbeitsbereich kopiert werden. (TGT-40686)
* Es wurde ein Problem behoben, das Änderungen an einem Selektor mit [Erlebnisfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md) bei Verwendung von &quot;[!UICONTROL Einfügen nach]&quot;im VEC verhinderte. (TGT-41802)
* Fehlerkorrektur - leere JSON-Inhalte in einem Angebot können jetzt an das Backend gesendet werden. [!DNL Target] sendet jetzt das JSON-Objekt, obwohl es leer ist. (TGT-41555)
* Es wurde ein Fehler behoben, der dazu führte, dass ältere [!DNL Analytics]-Berichte anstelle von [!DNL Analysis Workspace] geöffnet wurden, wenn Kunden beim Anzeigen eines Berichts auf &quot;[!UICONTROL In Analytics anzeigen]&quot;geklickt haben. (TGT-41867)
* Es wurde eine zusätzliche Klarstellung zur angezeigten Benutzeroberflächenmeldung hinzugefügt, wenn ein Kunde versucht, [!DNL Analytics] als Berichtsquelle (A4T) für eine [!UICONTROL Automated Personalization] -Aktivität auszuwählen. In der Meldung wird angegeben, dass &quot;[!DNL Target] die einzige unterstützte Quelle für [!UICONTROL Automated Personalization] -Aktivitäten ist.&quot; (TGT-41954)
* Es wurde eine zusätzliche Klarstellung zur Fehlermeldung hinzugefügt, wenn Kunden versuchen, Hosts durch &quot;Zeilenumbruch&quot;anstelle von Kommas zu trennen. (TGT-40671)
* Es wurde ein Fehler behoben, der dazu führte, dass sich die Daten einiger Aktivitäten &quot;[!UICONTROL Zuletzt aktualisiert]&quot;für spanische und japanische Kunden von der englischen Benutzeroberfläche unterschieden (wenn die Benutzeroberfläche auf Spanisch und Japanisch angezeigt wurde). (TGT-38980)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority-Produktaktualisierung | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
