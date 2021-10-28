---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 9f2947355c3857add5ea47d41c1adc2e3e8bba08
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 41%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs, der [!DNL Adobe Experience Platform Web SDK] und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek „at.js“, um mögliche Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## [!DNL Target Standard/Premium] 21.10.4 (21. Oktober 2021)

Dieses Maintenance Release umfasst die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| Warenkorbbasierte Recommendations | Eine neue Reihe von Algorithmen wurde hinzugefügt, um Empfehlungen basierend auf dem Inhalt des Warenkorbs des Besuchers bereitzustellen.<br>Weitere Informationen finden Sie unter &quot;Warenkorb-basiert&quot;in [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md) und &quot;Warenkorb fügt/Warenkorbansichten/Checkout-Seiten hinzu&quot;und &quot;Artikel, die sich bereits im Warenkorb des Besuchers befinden, ausschließen&quot;in [Planen und Implementieren von Recommendations](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19. Oktober 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen:

* Es wurden Probleme behoben, durch die Kunden die [!UICONTROL A4T] Bedienfeld in [!DNL Analysis Workspace] durch Klicken auf [!UICONTROL In Analytics anzeigen] Schaltfläche in [!DNL Target] Aktivitätsberichte. (TGT-42099, TGT-42100)
* Es wurde ein Fehler behoben, der dazu führte, dass die [!UICONTROL Design bearbeiten] Schaltfläche wird beim Bearbeiten nicht angezeigt [!UICONTROL A/B-Test] und [!UICONTROL Erlebnis-Targeting] (XT) Aktivitäten, die die [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* Es wurde ein Problem behoben, durch das die [!UICONTROL Kompatibel] bei der Erstellung eines neuen [!UICONTROL Recommendations] Aktivität. (TGT-42053)
* Fehlerkorrektur - die Fehlermeldung wird nun auch dann korrekt angezeigt, wenn die Option [!DNL Analytics] als Berichtsquelle (A4T), da [!DNL Analytics] Berechtigungen. (TGT-41954)
* Mehrere Fehlerbehebungen zur Barrierefreiheit wurden implementiert, um die Tastaturnavigation über das [!DNL Target] Benutzeroberfläche.

## [!DNL Target Standard/Premium] 21.10.2 (13. Oktober 2021)

Die folgenden Verbesserungen wurden bei der Verwendung von [!DNL Target] [!UICONTROL Zielgruppen] mit dem [!DNL Adobe Experience Platform Web SDK]:

* Warnsymbole, Popup-Fenster und Meldungen wurden an verschiedenen Stellen im [!DNL Target] Benutzeroberfläche, die angibt, dass die Zielgruppe in der Quelle gelöscht wurde und nicht mehr zur Verwendung in verfügbar ist [!DNL Target] Aktivitäten.

   Die folgenden Abbildungen zeigen einige Stellen, an denen Symbole, Popovers und Nachrichten angezeigt werden:

   * [!UICONTROL Aktivität] Listenseite

      ![Zielgruppe gelöscht in Quellnachricht auf Aktivitätenlistenseite](assets/deleted-at-source-audiences-list.png)

   * Aktivität [!UICONTROL Übersicht] Seiten:

      ![Zielgruppe gelöscht in Quellnachricht auf Übersichtsseite](assets/deleted-at-source-overview.png)

   * [!UICONTROL Experiences] step of the activity-creation workflow:

      ![Zielgruppe gelöscht in Quellnachricht auf [!UICONTROL Erlebnisse] page](assets/deleted-at-source-experiences.png)

   * [!UICONTROL Targeting] Schritt des Workflows zur Aktivitätserstellung:

      ![Zielgruppe gelöscht in Quellnachricht auf [!UICONTROL Targeting] page](assets/deleted-at-source-targeting.png)

   * [!UICONTROL Ziele und Einstellungen] Schritt des Workflows zur Aktivitätserstellung:

      ![Zielgruppe gelöscht in Quellnachricht auf der [!UICONTROL Ziele und Einstellungen] page](assets/deleted-at-source-goals-settings.png)

   * Zielgruppenverfeinerungen ([!UICONTROL Zielgruppe ersetzen] auf [!UICONTROL Targeting] Schritt des Workflows zur Aktivitätserstellung):

* Wenn Sie versuchen, die Funktion Zielgruppen kombinieren zu verwenden und eine der Zielgruppen aus der Quelle gelöscht wurde, [!UICONTROL Speichern] deaktiviert ist.

## [!DNL Target Standard/Premium] 21.10.1 (6. Oktober 2021)

Diese Version enthält die folgenden neuen Funktionen:

| Funktion | Details |
| --- | --- |
| [!UICONTROL Aktualisierung der Audiences-Benutzeroberfläche] | Als Teil der [!DNL Adobe Target] Bemühungen des Teams zur Verbesserung des Benutzererlebnisses für [!DNL Target] Benutzern verwendet, aktualisiert diese Version die [!UICONTROL Zielgruppen] und [!UICONTROL Profilskripte] Seiten in [!DNL Target] Benutzeroberfläche. Diese Aktualisierung vereinheitlicht und standardisiert Designmuster, die zuvor inkonsistent waren, und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:<ul><li>Die Möglichkeit, mehrere Zielgruppen gleichzeitig auszuwählen und zu löschen</li><li>Ein aktualisiertes [Audience Builder-Design](/help/c-target/c-audiences/create-audience.md)</li><li>Unterstützung von Ausschlussregeln im [!UICONTROL Zielgruppe] Regel-Builder für Bibliotheken</li><li>Ein neuer Filter &quot;Zielgruppenquelle&quot;, der eine schnellere Erkennung der Zielgruppen ermöglicht</li><li>Sitzungsbeständige Suchoptionen und Filteroptionen</li></ul>Weitere Informationen finden Sie unter [Zielgruppen](/help/c-target/target.md).<br>**NOTE**: Die neue [!UICONTROL Zielgruppen] Die Benutzeroberfläche ist nur zur Auswahl von Kunden verfügbar. Die Aktualisierung wird ab Januar 2022 schrittweise für alle Kunden eingeführt. |
| [!UICONTROL Profilskripte] Aktualisierung der Benutzeroberfläche | Die [!UICONTROL Profilskripte] -Bibliothek wurde ebenfalls aktualisiert und enthält eine aktualisierte Benutzeroberfläche sowie mehrere Produktivitätsaktualisierungen:<ul><li>Die Möglichkeit, mehrere Profilskripte gleichzeitig auszuwählen und zu löschen</li><li>Ein neuer Code-Editor für Profilskripte</li><li>Syntaxhervorhebung und Fehlerprüfung im Code-Editor</li><li>Parameter für automatische Vervollständigung von Token (Mbox oder Profil) über Tastaturbefehle</li></ul>Weitere Informationen finden Sie unter [Besucherprofile](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**NOTE**: Die neue [!UICONTROL Profilskripte] Die Benutzeroberfläche ist nur zur Auswahl von Kunden verfügbar. Die Aktualisierung wird ab Januar 2022 schrittweise für alle Kunden eingeführt. |
| ![Premium-Zeichen](/help/assets/premium.png) Erstellen und Bearbeiten von Recommendations-Kriterien | Die [!UICONTROL Recommendations-Kriterien] Der Arbeitsablauf für die Erstellung und Bearbeitung wurde optimiert, um die Auswahl des richtigen Empfehlungsalgorithmus und der richtigen Einstellungen zum Erreichen Ihrer Ziele zu vereinfachen.<br>Weitere Informationen finden Sie unter [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Premium-Zeichen](/help/assets/premium.png) Verbesserungen der Recommendations-Lookback-Zeit und der Algorithmusaktualisierung | Sie können jetzt die Algorithmen &quot;Am häufigsten angezeigt&quot;und &quot;Topverkäufe&quot;mit einem sechsstündigen Lookback-Fenster ausführen, um den Inhalt zu erfassen, der zuletzt als Trend bezeichnet wurde. Wenn das sechsstündige Lookback-Fenster ausgewählt wird, werden Ihre Empfehlungsergebnisse täglich alle 3-6 Stunden aktualisiert.<br>Weitere Informationen finden Sie unter [Datenquelle](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *Erstellen von Kriterien*. |

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Dokumentationsänderungen, historische Versionshinweise und Experience Cloud-Versionshinweise

Neben den Hinweisen für jede Version bieten die folgenden Ressourcen zusätzliche Informationen:

| Ressource | Details |
|--- |--- |
| Dokumentationsänderungen | Enthält detaillierte Informationen zu Aktualisierungen dieses Benutzerhandbuchs, die nicht in diesen Versionshinweisen enthalten sind.<br>Weitere Informationen finden Sie unter [Dokumentationsänderungen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Versionshinweise für vorherige Versionen | Lesen Sie sich Informationen zu neuen Funktionen und Verbesserungen älterer Versionen von Target Standard und Target Premium durch.<br>Weitere Informationen finden Sie unter [Versionshinweise für frühere Versionen](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud-Versionshinweise | Zeigen Sie die aktuellen Versionshinweise für die Adobe Experience Cloud-Lösungen an.<br>Weitere Informationen finden Sie in den [Versionshinweisen zu Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=de). |

## Vorabinformationen zu Versionen {#section_5D588F0415A2435B851A4D0113ACA3A0}

Mit den folgenden Ressourcen können Sie sehen, was in der nächsten Target-Version zu finden ist.

| Ressource | Details |
|--- |--- |
| Adobe Priority-Produktaktualisierung | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
