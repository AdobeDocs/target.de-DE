---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: fa6324606b32f265084615fd1c13ce6c49921b48
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 55%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 30. Juni 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 22.6.2 (30. Juni 2022)

Diese Version enthält die folgenden Funktionen, Verbesserungen und Fehlerbehebungen:

| Funktion | Beschreibung |
| --- | ---  |
| In-Produkt-Benachrichtigungen | Rufen Sie die folgenden relevanten produktinternen Benachrichtigungen ab:<ul><li>**Tätigkeiten**: Benachrichtigungen für alle Aktivitätstypen, wenn eine Aktivität genehmigt oder deaktiviert wird, entweder manuell oder beim Erreichen des Start- oder Enddatums. Die Benachrichtigung enthält den Namen der Aktivität mit einem Link zur Übersichtsseite der Aktivität.</li><li>**Profilskripte** Benachrichtigungen, wenn ein Profilskript entweder manuell oder durch Target aktiviert oder deaktiviert wird.</li><li>**Recommendations Feeds**: Benachrichtigungen, wenn ein Recommendations-Feed entweder manuell oder durch Target aktiviert oder deaktiviert wird. Benachrichtigungen werden auch gesendet, wenn ein Recommendations-Feed fehlschlägt.</li></ul> Standardmäßig werden Benachrichtigungen von Produktadministratoren, Herausgebern und Genehmigern empfangen. Benachrichtigungen können in den Voreinstellungen von Experience Cloud konfiguriert werden.<br>Weitere Informationen finden Sie unter [Benachrichtigungen und Mitteilungen](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Adobe Target-Entwicklerhandbuch* | Die *Adobe Target-Entwicklerhandbuch* alle [!DNL Target] Entwicklerinhalte in einer praktischen Anleitung. Das Handbuch enthält Informationen zur Implementierung von [!DNL Target] und [!DNL Recommendations], [!DNL Target] SDKs und [!DNL Target] APIs.<br>Weitere Informationen finden Sie unter [Adobe Target-Entwicklerhandbuch](https://developer.adobe.com/target/){target=_blank}. |

* Benutzer mit [!UICONTROL Editor]-Rolle können Zielgruppen in Live-Aktivitäten nicht mehr bearbeiten. (TGT-43582)
* Es wird eine Warnmeldung angezeigt, wenn ein Kunde versucht, eine Zielgruppe zu speichern, deren Name mit einem Ausrufezeichen beginn (beispielsweise „!London“). (TGT-43643)
* Es wurde ein Fehler behoben, der dazu führte, dass auf den Karten mit Details zur Zielgruppendefinition für einige Kunden eine beendete Aktivität noch immer als laufend angezeigt wurde. (TGT-43527)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
