---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: c351044163a6fb32ca72fa015724d3b0388c059a
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 93%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

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

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md). |
