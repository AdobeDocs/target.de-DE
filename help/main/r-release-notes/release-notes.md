---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 9489655d18170c581f2abf8502f01c7b7e0626b7
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 52%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 2.5.1 (gestaffelte Version) 11.-13. Mai 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **11. Mai**: Region Asien-Pazifik (APAC)
* **12. Mai**: Region Nordamerika (NA)
* **13. Mai**: Region Europa, Naher Osten und Afrika (EMEA)

Diese Version enthält die folgenden Verbesserungen und Fehlerbehebungen:

* Es wurde ein Fehler behoben, der zu einem JavaScript-Fehler führte und einige Kunden daran hinderte, für bestimmte [!UICONTROL Automated Personalization] AP-Aktivitäten. (TGT-43526)
* Fehlerkorrektur - jetzt können bestimmte Kunden einem AP-Aktivitätsmodul ein bestimmtes Angebot hinzufügen (oder bearbeiten). (TGT-43503)
* Es wurde ein Problem im [!DNL Target] Benutzeroberfläche, in der die folgende Fehlermeldung angezeigt wurde: &quot;Ihre globale Mbox ist möglicherweise nicht synchronisiert. Bitte versuchen Sie, sie erneut zu speichern.“ Dieses Problem war ein UI-Problem und hatte keine Auswirkungen auf die -Implementierungen von Kunden. (TGT-43475)
* Fehlerkorrektur - Verfeinerungen und Zielgruppen auf Erlebnisebene können jetzt von einem Kunden für eine Aktivität bearbeitet werden, wenn die Verfeinerungen und Zielgruppen vor dem neuen erstellt wurden [!UICONTROL Zielgruppen] Die Benutzeroberfläche wurde bereitgestellt. (TGT-43433)
* Es wurde ein Problem behoben, durch das Kunden doppelte [!DNL Adobe Audience Manager] (AAM) Zielgruppen beim Bearbeiten von Berichtszielgruppen für eine Aktivität. (TGT-43430)
* Fehlerkorrektur - Kunden können jetzt doppelte Zielgruppen erstellen, die sich jedoch in verschiedenen Arbeitsbereichen befinden. (TGT-43423)
* Es wurde ein Fehler behoben, der verhinderte, dass Kunden Orte löschen konnten, die Ad-hoc-Angebote in Aktivitäten enthielten, die in der [!UICONTROL Form-Based Experience Composer]. (TGT-43315)
* Es wurde ein Problem behoben, das Kunden daran hinderte, auf Code-Angebote zuzugreifen, nachdem sie auf Bildangebote geklickt und dann die Benutzeroberfläche aktualisiert haben. (TGT-43566)
* Sicherstellen, dass die Liste der Metriken im [!DNL Target] Benutzeroberfläche beim Erstellen von Aktivitäten, die [!DNL Analytics for Target] (A4T) zeigt nur die Metriken an, die von [!DNL Adobe Analytics]. (TGT-43294)
* Es wurde ein Problem behoben, bei dem Änderungen an Profilskripten zum ursprünglichen, nicht bearbeiteten Skript zurückkehrten, nachdem das Skript bearbeitet, aktiviert und dann deaktiviert wurde. Das Profilskript verbleibt jetzt im bearbeiteten Status. (TGT-43249)
* Es wurde ein Problem behoben, das den folgenden Fehler verursachte, wenn versucht wurde, eine Zielgruppe in einen anderen Arbeitsbereich zu verschieben: &quot;Wir können Ihre Anfrage nicht abschließen. Wenden Sie sich an den Kundendienst von Adobe , wenn das Problem weiterhin besteht.&quot; (TGT-43212)
* Fehlerkorrektur - beim Klonen von Änderungen an benutzerdefiniertem Code für Einzelseiten-Apps (SPA) tritt kein Fehler mehr auf. (TGT-43137)
* Es wurde ein Fehler behoben, der dazu führte, dass die ursprüngliche Promotion nach dem Duplizieren eines Erlebnisses und anschließenden Bearbeiten der Promotion betroffen war. (TGT-41775)

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
