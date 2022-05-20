---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 953b511db6d2c7ccf883d8e256c4e0ab22718862
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 30%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Letzte Aktualisierung: 9. Mai 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 2.5.1 (gestaffelte Version) 11.-13. Mai 2022)

Diese Version wird gemäß dem folgenden gestaffelten Zeitplan verfügbar sein:

* **11. Mai**: Region Asien-Pazifik (APAC)
* **12. Mai**: Amerikanische Region
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
* Es wurde ein Problem behoben, bei dem Änderungen an Profilskripten zum ursprünglichen, nicht bearbeiteten Skript zurückkehrten, nachdem das Skript bearbeitet, aktiviert und dann deaktiviert wurde. Das Profilskript verbleibt jetzt im bearbeiteten Status. (TGT-43249)
* Es wurde ein Problem behoben, das den folgenden Fehler verursachte, wenn versucht wurde, eine Zielgruppe in einen anderen Arbeitsbereich zu verschieben: &quot;Wir können Ihre Anfrage nicht abschließen. Wenden Sie sich an den Kundendienst von Adobe , wenn das Problem weiterhin besteht.&quot; (TGT-43212)
* Fehlerkorrektur - beim Klonen von Änderungen an benutzerdefiniertem Code für Einzelseiten-Apps (SPA) tritt kein Fehler mehr auf. (TGT-43137)
* Es wurde ein Fehler behoben, der dazu führte, dass die ursprüngliche Promotion nach dem Duplizieren eines Erlebnisses und anschließenden Bearbeiten der Promotion betroffen war. (TGT-41775)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

So erhalten Sie Vorabbenachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und andere [!DNL Adobe Experience Cloud] Lösungen, melden Sie sich für die [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
