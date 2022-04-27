---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 25dac5f4712fec80323df9b0e00feb9750f5b155
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 56%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Darüber hinaus finden Sie in den Versionshinweisen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und andere Plattformänderungen sind ebenfalls enthalten, sofern zutreffend.

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## [!DNL Target] Plattform-Version (27. April 2022)

Diese Version enthält die folgende Änderung:

* Mit dieser Version können Sie Inhalte vorab abrufen für [!UICONTROL Automatisierte Personalisierung] (AP) und [!UICONTROL Automatisches Targeting] (AT) Aktivitäten (zuvor nicht zurückgegeben von [!DNL Target]). Dies kann die Erlebnisse ändern, die den Endbenutzern bei einem Vorabruf (keine Änderungen am &quot;Ausführungs&quot;-Fluss) angezeigt werden, wenn sich eine AP-/AT-Aktivität im Bereitstellungspfad befindet und eine höhere Priorität aufweist als andere AB-/XT-Aktivitäten, die denselben Ort für die Inhaltsbereitstellung verwenden.

## Target Platform-Version (13. April 2022)

Diese Version enthält die folgende Aktualisierung:

* Es wurde ein Fehler behoben, der sicherstellte, dass das letzte Oktett von IP-Adressen bei der Erfassung mithilfe von Profilskripten ordnungsgemäß verschleiert wird. (TNT-44076)

## [!DNL Target Standard/Premium] 22.3.1 (5. April 2022)

Diese Version enthält die folgenden Änderungen und Verbesserungen:

* Es wurde ein Fehler behoben, der dazu führte, dass die [!UICONTROL Einschließen] und [!UICONTROL Ausschließen] Optionen, die bei der Bearbeitung einer Aktivität für kombinierte Zielgruppen deaktiviert werden sollen. (TGT-43422)
* Es wurde ein Problem behoben, das manche Kunden daran hinderte, beim Bearbeiten einer Aktivität die Liste der verfügbaren Zielgruppen anzuzeigen. (TGT-43404)
* Es wurde ein Problem behoben, das manche Kunden daran hinderte, eine IP-Adresse aus dem[!UICONTROL Auszuschließende IPs [!DNL Target] Berichtsdaten]&quot; in [!UICONTROL Administration] > [!UICONTROL Berichterstellung]. (TGT-43384)
* Es wurde ein Problem behoben, das die Verwendung negativer Zahlen im Zielgruppenkriterium verhinderte, die sicherstellen, dass eine Variable &quot;größer als&quot;, &quot;größer oder gleich&quot;, &quot;kleiner als&quot;oder &quot;kleiner oder gleich&quot;ist. (TGT-43367)
* Es wurde ein Problem behoben, durch das Kunden die [!UICONTROL Zielgruppendetails] Karte beim Erstellen kombinierter Zielgruppen. (TGT-43303)

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
