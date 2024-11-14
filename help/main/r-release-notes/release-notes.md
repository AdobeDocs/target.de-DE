---
keywords: Versionshinweise; neue Funktionen; Versionen; Aktualisierungen; Update; Version; Verbesserungen; Verbesserungen; Fehlerbehebungen; Fehlerbehebungen; Aktualisierungen, aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: d823e9993ff17f1970dc1deac996928781c7e79d
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 39%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Adobe Experience Platform Web SDK] `__view__` Bereichsoptimierung (22. Oktober 2024)

Zwischen dem 22. Juli 2024 und dem 15. August 2024 optimierte das [!DNL Target]-Team den Umfang von `__view__`, wodurch die Genauigkeit von Aktivitätsimpressionen, Besuchen und Besucherberichten verbessert wurde. Diese Optimierung zielt darauf ab, Berichtsdaten für automatisch gerenderte Vorschläge automatisch zu erfassen und sollte für die meisten Konten transparent sein.

Für alle neuen [!DNL Adobe Experience Platform Web SDK] -Kunden ist diese Optimierung aktiviert. Kunden, die von at.js migriert wurden und die die unten stehenden Implementierungsschritte nicht befolgt haben, haben die Optimierung jedoch deaktiviert. Wir fordern diese Kunden dringend auf, ihre Implementierungen bis zum 3. Februar 2025 zu überprüfen. Nach diesem Datum wird die Optimierung für alle Kunden aktiviert. Wenn Implementierungen nicht bis dahin überprüft und angepasst werden, kann dies Auswirkungen auf Berichte haben, wie unten erwähnt. Wenden Sie sich an [!DNL Adobe Customer Care] , wenn Sie überprüfen müssen, ob Ihre Implementierung betroffen ist oder mehr Zeit für die Anpassung Ihrer Implementierung benötigt wird.

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

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen des Platform Web SDK. |
| [at.js-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| [Dokumentationsänderungen](/help/main/r-release-notes/doc-change.md) | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind. |
| [Versionshinweise für vorherige Versionen](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Sehen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium an. |
| [Versionshinweise zu Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de){target=_blank} | Sehen Sie sich die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an. |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| [Vorrangiges Produkt-Update von Adobe](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
