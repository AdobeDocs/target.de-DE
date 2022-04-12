---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 01c36c0288a15d68f99a6c2f136da9066ccf2e62
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 34%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert: 13. April 2022**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Target Platform-Version (13. April 2022)

Diese Version enthält die folgende Aktualisierung:

* Es wurde ein Fehler behoben, der sicherstellte, dass das letzte Oktett von IP-Adressen bei der Erfassung mithilfe von Profilskripten ordnungsgemäß verschleiert wird. (TNT-44076)

## [!DNL Target Standard/Premium] 2.3.1 (gestaffelte Version, festes Datum)

Diese Version enthält die folgenden Änderungen und Verbesserungen:

* Es wurde ein Problem behoben, bei dem Änderungen an Profilskripten zum ursprünglichen, nicht bearbeiteten Skript zurückkehrten, nachdem das Skript bearbeitet, aktiviert und dann deaktiviert wurde. Das Profilskript verbleibt jetzt im bearbeiteten Status. (TGT-43249)
* Es wurde ein Problem behoben, das die folgende Fehlermeldung im [!DNL Target] Benutzeroberfläche beim Verschieben einer in einer Aktivität mit dem Status &quot;Entwurf&quot; verwendeten Zielgruppe: &quot;Wir können Ihre Anfrage nicht abschließen. Wenden Sie sich an die Kundenunterstützung von Adobe, wenn das Problem weiterhin besteht.&quot; (TGT-43212)
* Es wurde ein Fehler behoben, der dazu führte, dass die [!UICONTROL Einschließen] und [!UICONTROL Ausschließen] Optionen, die bei der Bearbeitung einer Aktivität für kombinierte Zielgruppen deaktiviert werden sollen. (TGT-43422)
* Es wurde ein Problem behoben, das manche Kunden daran hinderte, beim Bearbeiten einer Aktivität die Liste der verfügbaren Zielgruppen anzuzeigen. (TGT-43404)
* Es wurde ein Problem behoben, das manche Kunden daran hinderte, eine IP-Adresse aus dem[!UICONTROL Auszuschließende IPs [!DNL Target] Berichtsdaten]&quot; in [!UICONTROL Administration] > [!UICONTROL Berichterstellung]. (TGT-43384)
* Es wurde ein Problem behoben, das die Verwendung negativer Zahlen im Zielgruppenkriterium verhinderte, die sicherstellen, dass eine Variable &quot;größer als&quot;, &quot;größer oder gleich&quot;, &quot;kleiner als&quot;oder &quot;kleiner oder gleich&quot;ist. (TGT-43367)
* Es wurde ein Problem behoben, durch das Kunden die [!UICONTROL Zielgruppendetails] Karte beim Erstellen kombinierter Zielgruppen. (TGT-43303)
* Es wurde ein Fehler behoben, der dazu führte, dass die [!DNL Target] Benutzeroberfläche oder neue [!UICONTROL Zielgruppen] -Benutzeroberfläche verwenden, um einigen Kunden ein frühzeitiges Timeout zu ermöglichen. (TGT-42590 und TGT-43273)

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
