---
keywords: Versionshinweise;Versionen;Updates;zukünftige Versionen;Verbesserungen;neue Funktionen;Fehlerbehebungen;Updates;Vorabversion
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von Adobe Target sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen sind in der kommenden Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: bd7032b915bf1b333fa5cc3cb4825eaa7e4f83fb
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 43%

---

# Target-Versionshinweise (Vorabversion)

Dieser Artikel enthält Vorabinformationen zur kommenden Version. Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.

**Zuletzt aktualisiert am: 6. Oktober 2021**

Informationen über die aktuelle Version finden Sie unter [Versionshinweise für Target](release-notes.md). Die Informationen auf diesen Seiten können je nach Veröffentlichungsdatum der Versionen identisch sein. Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Um potenzielle Probleme mit Ihren Sites zu vermeiden, migrieren Sie zur neuesten Version der neuen [!DNL Adobe Experience Platform Web SDK]- oder der JavaScript-Bibliothek „at.js“. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.10.1 (6. Oktober 2021)

Diese Version enthält die folgenden neuen Funktionen:

| Funktion | Details |
| --- | --- |
|  AudienceUI-Aktualisierung | Im Rahmen der kontinuierlichen Bemühungen des Teams [!DNL Adobe Target], das Benutzererlebnis für [!DNL Target]-Benutzer zu verbessern, werden die Seiten [!UICONTROL Zielgruppen] und [!UICONTROL Profilskripte] in der [!DNL Target]-Benutzeroberfläche aktualisiert. Diese Aktualisierung vereinheitlicht und standardisiert Designmuster, die zuvor inkonsistent waren, und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:<ul><li>Die Möglichkeit, mehrere Zielgruppen gleichzeitig auszuwählen und zu löschen</li><li>Ein aktualisiertes [Audience Builder-Design](/help/c-target/c-audiences/create-audience.md)</li><li>Unterstützung von Ausschlussregeln im Bibliotheksregel-Builder [!UICONTROL Zielgruppe]</li><li>Ein neuer Filter &quot;Zielgruppenquelle&quot;, der eine schnellere Erkennung der Zielgruppen ermöglicht</li><li>Sitzungsbeständige Suchoptionen und Filteroptionen</li></ul>Weitere Informationen finden Sie unter [Zielgruppen](/help/c-target/target.md).<br>**Hinweis**: Die neue   Zielgruppen- und  [!UICONTROL Profilskripte-] Benutzeroberfläche wird nächste Woche für alle Regionen eingeführt. |
| [!UICONTROL Aktualisierung ] der Profilskripte-Benutzeroberfläche | Die Bibliothek [!UICONTROL Profilskripte] wurde ebenfalls aktualisiert und enthält eine aktualisierte Benutzeroberfläche sowie mehrere Produktivitätsaktualisierungen:<ul><li>Die Möglichkeit, mehrere Profilskripte gleichzeitig auszuwählen und zu löschen</li><li>Ein neuer Code-Editor für Profilskripte</li><li>Syntaxhervorhebung und Fehlerprüfung im Code-Editor</li><li>Parameter für automatische Vervollständigung von Token (Mbox oder Profil) über Tastaturbefehle</li></ul>Weitere Informationen finden Sie unter [Besucherprofile](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**Hinweis**: Die neue   Zielgruppen- und  [!UICONTROL Profilskripte-] Benutzeroberfläche wird nächste Woche für alle Regionen eingeführt. |
| ![Premium-](/help/assets/premium.png) ZeichenErstellen und Bearbeiten von Recommendations-Kriterien | Der Workflow für die Erstellung und Bearbeitung von [!UICONTROL Recommendations-Kriterien] wurde optimiert, um die Auswahl des richtigen Empfehlungsalgorithmus und der richtigen Einstellungen zum Erreichen Ihrer Ziele zu vereinfachen.<br>Weitere Informationen finden Sie unter  [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Premium ](/help/assets/premium.png) badgeRecommendations-Lookback-Fenster und Verbesserungen der Algorithmusaktualisierungsrate | Sie können jetzt die Algorithmen &quot;Am häufigsten angezeigt&quot;und &quot;Topverkäufe&quot;mit einem sechsstündigen Lookback-Fenster ausführen, um den Inhalt zu erfassen, der zuletzt als Trend bezeichnet wurde. Wenn das sechsstündige Lookback-Fenster ausgewählt wird, werden Ihre Empfehlungsergebnisse täglich alle 3-6 Stunden aktualisiert.<br>Weitere Informationen finden Sie unter  [Data ](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) Sources in Kriterien  *erstellen*. |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und anderen Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
