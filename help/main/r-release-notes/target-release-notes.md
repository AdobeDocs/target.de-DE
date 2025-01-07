---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: f3090ad7ab1c3d15de496039e76bb5ec0b02886f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 21%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: Mittwoch, 7. Januar 2025**

>[!NOTE]
>
>Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## Aktualisierung der [!UICONTROL Offers Library]-Benutzeroberfläche (9. Januar 2025)

Um das Benutzererlebnis für [!DNL Adobe Target] Benutzer zu verbessern, aktualisiert diese Version die [!UICONTROL Offers Library] Benutzeroberfläche. Mit dem neuesten [!DNL Adobe Spectrum]-Design-System standardisiert dieses Update inkonsistente Design-Muster und führt neue Verbesserungen ein, darunter die folgenden:

* **Massenangebotsverwaltung**: Gleichzeitiges Auswählen und Löschen oder Verschieben mehrerer Angebote.

* **[!UICONTROL Code Editor]Upgrades**: Aktualisierte HTML- und JSON-Editoren mit Syntaxhervorhebung und Zeilennummerierung.

* **Verbesserte Angebotskarten**: Verbesserte Karten für schnelle Informationen und Details für einen einfacheren Zugriff auf Informationen.

* **Persistente Suche und Filter**: Fügt Optionen für sitzungspersistente Suche und Filter hinzu.

Ab dem 9. Januar 2025 erhalten alle [!DNL Target]-Kunden Zugriff auf die neue Benutzeroberfläche mit der Option, bei Bedarf zur aktuellen Version der Benutzeroberfläche zurückzukehren.

Weitere Informationen finden Sie [Angebote](/help/main/c-experiences/c-manage-content/manage-content.md) und den Unterartikeln in diesem Abschnitt.

Im Folgenden finden Sie ein kurzes Video zu den Änderungen in dieser Version:

![Video zur Aktualisierung der Angebotsbenutzeroberfläche](/help/main/r-release-notes/assets/offers-video-v2.gif)

## [!DNL Adobe Experience Platform Web SDK] Optimierung `__view__` Umfangs (22. Oktober 2024)

Zwischen dem 22. Juli 2024 und dem 15. August 2024 optimierte das [!DNL Target]-Team den `__view__` und verbesserte die Genauigkeit der Berichte zu Aktivitätsimpressionen, Besuchen und Besuchern. Diese Optimierung zielt darauf ab, Berichtsdaten für automatisch gerenderte Vorschläge automatisch zu erfassen, und sollte für die meisten Konten transparent sein.

Für alle neuen [!DNL Adobe Experience Platform Web SDK]-Kunden ist diese Optimierung aktiviert. Kunden, die von at.js migriert sind und die unten stehenden Implementierungsschritte nicht befolgt haben, haben die Optimierung jedoch deaktiviert. Wir fordern diese Kundinnen und Kunden dringend auf, ihre Implementierungen bis zum 3. Februar 2025 zu überprüfen. Nach diesem Datum aktivieren wir die Optimierung für alle Kunden. Wird die Umsetzung bis dahin nicht überprüft und angepasst, kann dies Auswirkungen auf die Berichte haben, wie unten erwähnt. Wenden Sie sich an [!DNL Adobe Customer Care], wenn Sie bestätigen müssen, ob Ihre Implementierung betroffen ist, oder wenn Sie mehr Zeit benötigen, um Ihre Implementierung anzupassen.

>[!IMPORTANT]
>
>Wenn Sie Ihre Implementierungsprüfung nicht bis zum 3. Februar 2025 abschließen und keine Probleme beheben können, können Sie eine einmalige Verlängerung um sechs Monate anfordern. Stellen Sie sicher, dass Ihre Anfrage bis zum 31. Januar 2025 gesendet wird. Adobe wird Ihre Anfrage prüfen und darüber entscheiden.

Um im Falle des manuellen Vorschlags-Renderings von dieser Optimierung zu profitieren, überprüfen Sie Ihre [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}, um sicherzustellen, dass Sie Benachrichtigungen senden, nachdem Sie Erlebnisse manuell gerendert haben, oder wenn Sie die `applyPropositions`-Methode (oder die entsprechende [!DNL Launch]-Aktion als Helper) zum Rendern von Erlebnissen verwenden.

Zu den häufigsten Szenarien, in denen Erlebnisse manuell gerendert werden, gehören:

* Verwenden von JSON-Angeboten
* Verwenden eines benutzerdefinierten Entscheidungsumfangs in einer in der [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) erstellten Aktivität
* Verwenden von `renderDecisions: true` beim Abrufen einer Aktivität, die mit dem [!UICONTROL Form-Based Experience Composer] erstellt wurde, der den globalen `__view__` verwendet

Wenn Benachrichtigungen nicht wie in [Rendern personalisierter Inhalte](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} im Handbuch *Datenerfassung* dokumentiert sind, fehlen Berichtsdaten möglicherweise in [!DNL Target] und in [Analytics for Target-](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In bestimmten Szenarien kann es vorkommen, dass Traffic falsch aufgeteilt wird, da die Berichtsdaten nicht erfasst werden. Oder in anderen Szenarien, bei denen dasselbe Ereignis wiederholt gemeldet wird.

Überprüfen Sie je nach Implementierung, ob sich [!DNL Analytics]- und A4T-Berichte auswirken.

Die [!DNL Platform Web SDK] unterstützt zwei Implementierungstypen für das Rendering von Erlebnissen und Personalisierungen:

* **Einzelaufruf für Personalisierung und Messung.**

  Ursprünglich wird empfohlen, den Einzelaufruf-Ansatz für die [!DNL Platform Web SDK] zugunsten des Aufspaltungs-Ansatzes zu verwerfen. Adobe empfiehlt allen neuen Implementierungen, den neuen Split-Call-Ansatz zu verwenden, und empfiehlt Bestandskunden, auch auf die Split-Call-Methode umzustellen.

  Wenn Sie den Einzelaufruf-Ansatz weiterhin verwenden, werden Sie möglicherweise die folgenden unerwarteten Änderungen in Ihren [!DNL Analytics] feststellen:

   * Ein Rückgang der Absprünge.
   * A4T- und [!UICONTROL Page View]-Treffer sind nicht zugeordnet, was die Durchführung bestimmter Aufschlüsselungen und Korrelationen Ihrer A4T-Berichte mithilfe [!DNL Analytics] eVars und Ereignisse erschwert.

* **Aufrufe zur Aufspaltung (auch als Seitenanfang und -ende-Ereignisse bezeichnet).**

  Dieser Implementierungstyp ist der neue [Aufspaltungs-Implementierungsansatz](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} der von [!DNL Adobe] empfohlen wird. Bei diesem Ansatz hat die neue Optimierung keine Auswirkungen auf [!DNL Analytics]- oder A4T-Berichte.

Bei Fragen wenden Sie sich an die [Adobe-Kundenunterstützung](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
