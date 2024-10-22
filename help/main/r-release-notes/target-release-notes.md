---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b1ead7317debadafcb42469894cdb7b6ba337110
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 28%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert am: Mittwoch, 22. Oktober 2024**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Adobe Experience Platform Web SDK] `__view__` Bereichsoptimierung (22. Oktober 2024)

Zwischen dem 22. Juli 2024 und dem 15. August 2024 optimierte das [!DNL Target]-Team den Umfang von `__view__`, wodurch die Genauigkeit von Aktivitätsimpressionen, Besuchen und Besucherberichten verbessert wurde. Diese Optimierung zielt darauf ab, Berichtsdaten für automatisch gerenderte Vorschläge automatisch zu erfassen und sollte für die meisten Konten transparent sein.

Für alle neuen [!DNL Adobe Experience Platform Web SDK] -Kunden ist diese Optimierung aktiviert. Kunden, die von at.js migriert wurden und die die unten stehenden Implementierungsschritte nicht befolgt haben, haben die Optimierung jedoch deaktiviert. Wir fordern diese Kunden dringend auf, ihre Implementierungen bis zum 3. Februar 2025 zu überprüfen. Nach diesem Datum wird die Optimierung für alle Kunden aktiviert. Wenn Implementierungen nicht bis dahin überprüft und angepasst werden, kann dies Auswirkungen auf Berichte haben, wie unten erwähnt. Wenden Sie sich an [!DNL Adobe Client Care] , wenn Sie überprüfen müssen, ob Ihre Implementierung betroffen ist oder mehr Zeit für die Anpassung Ihrer Implementierung benötigt wird.

Um von dieser Optimierung im Fall des manuellen Renderings von Vorschlägen zu profitieren, überprüfen Sie Ihren [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}, um sicherzustellen, dass Sie Benachrichtigungen senden, nachdem Sie Erlebnisse manuell gerendert haben oder wenn Sie die `applyPropositions` -Methode (oder die entsprechende [!DNL Launch] -Aktion als Helfer) zum Rendern von Erlebnissen verwenden.

Zu den häufigsten Szenarien bei der manuellen Wiedergabe von Erlebnissen gehören:

* Verwenden von JSON-Angeboten
* Verwenden eines benutzerdefinierten Entscheidungsbereichs in einer Aktivität, die in der [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) erstellt wurde
* Nichtverwendung von `renderDecisions: true` beim Abrufen einer Aktivität, die mit dem [!UICONTROL Form-Based Experience Composer] erstellt wurde, der den globalen `__view__`-Bereich verwendet

Wenn Benachrichtigungen nicht wie in [Render personalized content](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} im Handbuch *Datenerfassung* dokumentiert implementiert sind, fehlen möglicherweise Berichtsdaten in [!DNL Target] und in [Analytics for Target Reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In bestimmten Szenarien kann es vorkommen, dass der Traffic falsch aufgeteilt ist, da die Berichtsdaten nicht erfasst werden. Oder in anderen Szenarien wird dasselbe Ereignis wiederholt gemeldet.

Überprüfen Sie je nach Implementierung, ob sich die Auswirkungen auf die A4T-Berichte auf [!DNL Analytics] und A4T auswirken.

Der [!DNL Platform Web SDK] unterstützt zwei Implementierungstypen zum Rendern von Erlebnissen und Personalisierungen:

* **Einzelaufruf für Personalisierung und Messung.**

  Zunächst wird empfohlen, den Einzelaufruf-Ansatz für [!DNL Platform Web SDK] nicht mehr für den Aufspaltungsansatz zu verwenden. Adobe rät allen neuen Implementierungen, den neuen Aufspaltungsansatz zu verwenden, und empfiehlt, dass Bestandskunden auch auf die Aufspaltungsmethode umsteigen.

  Wenn Sie den Einzelaufruf-Ansatz weiterhin verwenden, werden möglicherweise die folgenden unerwarteten Änderungen in Ihren [!DNL Analytics] -Berichten angezeigt:

   * Ein Rückgang der Absprünge.
   * A4T- und [!UICONTROL Page View]-Treffer werden nicht zugeordnet. Dies erschwert die Durchführung bestimmter Aufschlüsselungen und Korrelationen Ihrer A4T-Berichte mit [!DNL Analytics] eVars und Ereignissen.

* **Aufspaltung von Aufrufen (auch als &quot;oben und unten&quot;von Seitenereignissen bezeichnet).**

  Dieser Implementierungstyp ist der von [!DNL Adobe] empfohlene neue [Aufspaltungs-Implementierungsansatz](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank}. Bei diesem Ansatz hat die neue Optimierung keine Auswirkungen auf [!DNL Analytics] - oder A4T -Berichte.

Wenden Sie sich bei Fragen an die [Adobe-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

## [!DNL Target Standard/Premium] 24.10.2 (21. Oktober 2024)

Diese Version enthält die folgenden Fehlerbehebungen:

* Es wurde ein Problem behoben, das das Laden von [!UICONTROL Recommendations] -Aktivitäten in den Modi [!UICONTROL Compose] und [!UICONTROL Browse] verhindert hat. (TGT-50709)
* Es wurde ein Problem mit der neuen [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] -Erweiterung](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) behoben, das zu einer Umleitung vom [!UICONTROL Visual Experience Composer] (VEC) zum [!UICONTROL Activities Library] führte, nachdem auf &quot;Abbrechen&quot;geklickt wurde. Vor dieser Korrektur mussten Kunden die [!UICONTROL Activities Library] aktualisieren, bevor sie neue Aktivitäten erstellen konnten. (TGT-49980)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
