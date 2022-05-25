---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c351044163a6fb32ca72fa015724d3b0388c059a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 90%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 25. Mai 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target-Plattform-Version (25. Mai 2022)

Dieses Release umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Hinzugefügt [Benutzeragenten-Client-Hinweise](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md) unterstützen.
* Es wurde ein Problem behoben, das zeitweise zu Timeouts beim Rendern von [!UICONTROL Angebotsentscheidungen] in [!UICONTROL Erlebnis-Targeting] (XT). (TNT-44611)

## at.js-Version 2.9.0 (27. Mai 2022)

* Hinzugefügt [Benutzeragenten-Client-Hinweise](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md) unterstützen.
* Es wurde ein Fehler behoben, durch den mehrere Mbox-Anfragen auf derselben Seite unterschiedliche Impressions-IDs aufweisen.

## [!DNL Target Standard/Premium] 22.5.1 (gestaffelte Veröffentlichung; 11.–13. Mai 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **11. Mai**: Region Asien-Pazifik (APAC)
* **12. Mai**: Amerikanische Region
* **13. Mai**: Region Europa, Naher Osten und Afrika (EMEA)

Dieses Release umfasst die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde ein Fehler behoben, der zu einem JavaScript-Fehler führte und manche Kunden daran hinderte, die Aktivitätsdetails für bestimmte [!UICONTROL Automated Personalization] (AP)-Aktivitäten aufzurufen. (TGT-43526)
* Es wurde ein Fehler behoben, durch den manche Kunden daran gehindert wurden, eine bestimmtes Angebot zu bearbeiten oder es einer AP-Aktivität hinzuzufügen. (TGT-43503)
* Es wurde ein Fehler in der [!DNL Target]-Benutzeroberfläche behoben, in der die folgende Fehlermeldung angezeigt wurde: „Ihre globale Mbox ist möglicherweise nicht synchronisiert. Speichern Sie sie erneut.“ Dieser Fehler war ein UI-Problem und hatte keine Auswirkungen auf die Implementierungen bei Kunden. (TGT-43475)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Standortpräzisierungen auf Erlebnisebene und Zielgruppen für eine Aktivität zu bearbeiten, wenn die Standortpräzisierungen und Zielgruppen vor der Bereitstellung der neuen [!UICONTROL Zielgruppen]-Benutzeroberfläche erstellt worden waren. (TGT-43433)
* Es wurde ein Fehler behoben, durch den Kunden beim Bearbeiten von Berichtszielgruppen für eine Aktivität doppelte [!DNL Adobe Audience Manager]-Zielgruppen (AAM) auswählen konnten. (TGT-43430)
* Es wurde ein Fehler behoben, durch den Kunden keine doppelten Zielgruppen erstellen konnten, die sich in verschiedenen Arbeitsbereichen befanden. (TGT-43423)
* Es wurde ein Fehler behoben, der verhinderte, dass Kunden Standorte löschen konnten, die Ad-hoc-Angebote in Aktivitäten enthielten, die in [!UICONTROL Form-Based Experience Composer] erstellt worden waren. (TGT-43315)
* Es wurde ein Fehler behoben, der Kunden daran hinderte, auf Code-Angebote zuzugreifen, nachdem sie auf Bildangebote geklickt und dann die Benutzeroberfläche aktualisiert hatten. (TGT-43566)
* Es wurde ein Fehler behoben, durch den Änderungen an Profilskripten wieder in den ursprünglichen, nicht bearbeiteten Zustand des Skripts zurückkehrten, nachdem das Skript bearbeitet, aktiviert und dann deaktiviert worden war. Das Profilskript verbleibt jetzt im bearbeiteten Status. (TGT-43249)
* Es wurde ein Fehler behoben, der die folgende Fehlermeldung verursachte, wenn versucht wurde, eine Zielgruppe in einen anderen Arbeitsbereich zu verschieben: „Wir können Ihre Anfrage nicht durchführen. Wenden Sie sich an den Kundendienst von Adobe, wenn das Problem weiterhin besteht.“ (TGT-43212)
* Es wurde folgender Fehler behoben: Beim Klonen von Änderungen an benutzerdefiniertem Code für Einzelseiten-Apps (SPA) tritt kein Fehler mehr auf. (TGT-43137)
* Es wurde ein Problem behoben, das dazu führte, dass die ursprüngliche Promotion nach dem Duplizieren eines Erlebnisses und dem anschließenden Bearbeiten der Promotion beeinträchtigt war. (TGT-41775)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
