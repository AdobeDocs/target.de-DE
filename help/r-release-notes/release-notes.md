---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserungen;Erweiterungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von [!DNL Adobe Target].
title: Welche neuen Funktionen sind in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: cc260620cf87feebcd4c43f45f05406ac845cf5b
workflow-type: tm+mt
source-wordcount: '1153'
ht-degree: 81%

---

# Target-Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den APIs, SDKs, der [!DNL Adobe Experience Platform Web SDK] und der JavaScript-Bibliothek (at.js) von Target sowie zu anderen Plattformänderungen.

>[!IMPORTANT]
>
>**Beendigung von mbox.js**: Ab dem 31. März 2021 unterstützt [!DNL Adobe Target] die Bibliothek „mbox.js“ nicht mehr. Seit dem 31. März 2021 schlagen alle Aufrufe aus mbox.js kontrolliert fehl. Dies wirkt sich auf Seiten mit [!DNL Target]-Aktivitäten aus, die Standardinhalte bereitstellen.
>
>Migrieren Sie zur aktuellen Version des neuen [!DNL Adobe Experience Platform Web SDK] oder zur JavaScript-Bibliothek „at.js“, um mögliche Probleme mit Ihren Sites zu vermeiden. Weitere Informationen finden Sie unter [Übersicht: Target für Client-seitiges Web implementieren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.)

## at.js-Version 2.7.0 (28. Oktober 2021)

Diese Version enthält die folgende Verbesserung:

* Hinzugefügte Unterstützung für [Webkomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Diese Version von at.js ist erforderlich, um personalisierte Erlebnisse und Angebote für benutzerdefinierte Elemente und Elemente in benutzerdefinierten Elementen zu erstellen und zu testen. Diese Funktion ist im [!DNL Target Standard/Premium] Version 21.10.5.

## [!DNL Target Standard/Premium] 21.10.5 (28. Oktober 2021)

Dieses Maintenance Release umfasst die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Hinzugefügte Unterstützung für [Webkomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Personalisierte Erlebnisse und Angebote können mit benutzerdefinierten Elementen und Elementen in benutzerdefinierten Elementen erstellt und getestet werden.<br>Weitere Informationen finden Sie unter [Visual Experience Composer-Optionen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

## [!DNL Target Standard/Premium] 21.10.4 (21. Oktober 2021)

Dieses Maintenance Release umfasst die folgende Verbesserung:

| Funktion | Details |
| --- | --- |
| Warenkorbbasierte Recommendations | Eine neue Reihe von Algorithmen wurde hinzugefügt, um Empfehlungen basierend auf dem Inhalt des Warenkorbs des Besuchers bereitzustellen.<br>Weitere Informationen finden Sie unter &quot;Warenkorb-basiert&quot;in [Erstellen von Kriterien](/help/c-recommendations/c-algorithms/create-new-algorithm.md), &quot;Warenkorb fügt/Warenkorbansichten/Checkout-Seiten&quot;und &quot;Artikel, die sich bereits im Warenkorb des Besuchers befinden&quot;in [Planen und Implementieren von Recommendations](/help/c-recommendations/plan-implement.md)und &quot;Warenkorb-basiert&quot;in [Stützen der Empfehlung auf einen Empfehlungsschlüssel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19. Oktober 2021)

Diese Wartungsversion enthält folgende Verbesserungen, Fehlerkorrekturen und Änderungen:

* Es wurden Probleme behoben, die Kunden daran hinderten, das [!UICONTROL A4T]-Bedienfeld in [!DNL Analysis Workspace] zu öffnen, indem sie auf die Schaltfläche [!UICONTROL In Analytics anzeigen] in der [!DNL Target]-Aktivitätsberichterstattung klickten. (TGT-42099, TGT-42100)
* Es wurde ein Problem behoben, das dazu führte, dass die Schaltfläche [!UICONTROL Entwurf bearbeiten] beim Bearbeiten von [!UICONTROL A/B-Test]- und [!UICONTROL Experience Targeting](XT)-Aktivitäten mit dem [!UICONTROL formularbasierten Experience Composer] nicht angezeigt wurde. (TGT-41980)
* Es wurde ein Problem behoben, das verhinderte, dass das Kontrollkästchen [!UICONTROL Kompatibel] in der Kriterienauswahl beim Erstellen einer neuen [!UICONTROL Recommendations]-Aktivität angezeigt wurde. (TGT-42053)
* Es wurde eine falsche Fehlermeldung behoben, die angezeigt wurde, wenn [!DNL Analytics] als Berichtsquelle (A4T) aufgrund fehlender [!DNL Analytics]-Berechtigungen nicht ausgewählt werden konnte. (TGT-41954)
* Es wurden mehrere Korrekturen zur Verbesserung der Tastaturnavigation auf der gesamten [!DNL Target]-Benutzeroberfläche vorgenommen.

## [!DNL Target Standard/Premium] 21.10.2 (13. Oktober 2021)

Die folgenden Verbesserungen wurden bei der Verwendung von [!DNL Target] [!UICONTROL Audiences] mit dem [!DNL Adobe Experience Platform Web SDK] hinzugefügt:

* An verschiedenen Stellen in der [!DNL Target]-Benutzeroberfläche wurden Warnsymbole, Pop-overs und Meldungen hinzugefügt, die darauf hinweisen, dass die Zielgruppe an der Quelle gelöscht wurde und nicht mehr für die Verwendung bei [!DNL Target]-Aktivitäten verfügbar ist.

   Die folgenden Abbildungen zeigen einige der Orte, an denen Symbole, Pop-overs und Nachrichten angezeigt werden:

   * Listenseite [!UICONTROL Aktivität]

      ![Zielgruppe an der Quelle gelöscht, Meldung auf der Listenseite „Aktivität“](assets/deleted-at-source-audiences-list.png)

   * Aktivitäts-[!UICONTROL Überblick]seiten:

      ![Zielgruppe an der Quelle gelöscht, Meldung auf Übersichtsseite](assets/deleted-at-source-overview.png)

   * Schritt [!UICONTROL Erlebnisse] des Arbeitsablaufs für die Erstellung von Aktivitäten:

      ![Zielgruppe an der Quelle gelöscht, Meldung auf Seite [!UICONTROL Erlebnisse]](assets/deleted-at-source-experiences.png)

   * Schritt [!UICONTROL Targeting] des Arbeitsablaufs für die Erstellung von Aktivitäten:

      ![Audience gelöscht bei Quelle, Meldung auf [!UICONTROL Targeting]-Seite](assets/deleted-at-source-targeting.png)

   * Schritt [!UICONTROL Ziele und Einstellungen] des Arbeitsablaufs für die Erstellung von Aktivitäten:

      ![Zielgruppe an der Quelle gelöscht, Meldung auf Seite [!UICONTROL Ziele und Einstellungen]](assets/deleted-at-source-goals-settings.png)

   * Zielgruppenoptimierungen ([!UICONTROL Zielgruppe ersetzen] beim Schritt [!UICONTROL Targeting] des Arbeitsablaufs für die Erstellung von Aktivitäten:):

* Wenn Sie versuchen, die Funktion „Kombinieren von Zielgruppen“ zu verwenden und eine der Zielgruppen an der Quelle gelöscht wurde, ist [!UICONTROL Speichern] deaktiviert.

## [!DNL Target Standard/Premium] 21.10.1 (6. Oktober 2021)

Diese Version enthält die folgenden neuen Funktionen:

| Funktion | Details |
| --- | --- |
| Aktualisierung der [!UICONTROL Audiences]-Benutzeroberfläche | Im Rahmen der ständigen Bemühungen des [!DNL Adobe Target]-Teams, die Benutzerfreundlichkeit für [!DNL Target]-Anwender zu verbessern, wurden in dieser Version die Seiten [!UICONTROL Audiences] und [!UICONTROL Profilskripte] in der [!DNL Target]-Benutzeroberfläche aktualisiert. Dieses Update vereinheitlicht und standardisiert Designmuster, die zuvor nicht konsistent waren, und fügt gleichzeitig neue Verbesserungen hinzu, z. B.:<ul><li>Die Möglichkeit, mehrere Zielgruppen gleichzeitig auszuwählen und zu löschen</li><li>Ein überarbeitetes [Design für den Audience Builder](/help/c-target/c-audiences/create-audience.md)</li><li>Unterstützung von Ausschlussregeln im Rule Builder für [!UICONTROL Zielgruppe]nbibliotheken</li><li>Ein neuer „Zielgruppe-Quelle“-Filter, der eine schnellere Zielgruppenfindung ermöglicht</li><li>Optionen für dauerhafte Suche und Filter in Sitzungen</li></ul>Weitere Informationen finden Sie unter [Zielgruppen](/help/c-target/target.md).<br>**NOTE**: Die neue [!UICONTROL Zielgruppen] Die Benutzeroberfläche ist nur zur Auswahl von Kunden verfügbar. Die Aktualisierung wird ab Januar 2022 schrittweise für alle Kunden eingeführt. |
| Aktualisierung der [!UICONTROL Profilskript]-Benutzeroberfläche | Die [!UICONTROL Profilskripte]-Bibliothek wurde ebenfalls aktualisiert und enthält eine aktualisierte Benutzeroberfläche sowie mehrere Produktivitätsaktualisierungen:<ul><li>Die Möglichkeit, mehrere Profilskripte gleichzeitig auszuwählen und zu löschen</li><li>Ein neuer Codeeditor für Profilskripte</li><li>Syntaxhervorhebung und Fehlerprüfung im Code-Editor</li><li>Token-Parameter („mbox“ oder „profile“) über Tastaturbefehle automatisch ausfüllen</li></ul>Weitere Informationen finden Sie unter [Besucherprofile](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**NOTE**: Die neue [!UICONTROL Profilskripte] Die Benutzeroberfläche ist nur zur Auswahl von Kunden verfügbar. Die Aktualisierung wird ab Januar 2022 schrittweise für alle Kunden eingeführt. |
| Kriterien für ![Premium-Zeichen](/help/assets/premium.png) Recommendations erstellen und bearbeiten | Der Arbeitsablauf zur Erstellung und Bearbeitung von [!UICONTROL Recommendations-Kriterien] wurde optimiert, um die Auswahl des richtigen Recommendations-Algorithmus und der richtigen Einstellungen für Ihre Ziele zu vereinfachen.<br>Weitere Informationen finden Sie unter [Kriterien erstellen](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Premium-Zeichen](/help/assets/premium.png) Recommendations für das Lookback-Fenster und Verbesserungen der Aktualisierungsrate des Algorithmus | Sie können jetzt Algorithmen für „Am häufigsten angezeigt“ und „Topverkäufe“ mit einem sechsstündigen Lookback-Fenster ausführen, um die Inhalte zu erfassen, die in letzter Zeit im Trend liegen. Wenn das sechsstündige Lookback-Fenster ausgewählt ist, werden Ihre Empfehlungen den ganzen Tag über alle 3–6 Stunden aktualisiert.<br>Weitere Informationen finden Sie unter [Datenquelle](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) unter *Kriterien erstellen*. |

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
| Adobe Priority Product Update | Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an Target und andere Adobe Experience Cloud-Lösungen zu erhalten, melden Sie sich für das Adobe Priority Product Update an:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Bevorstehende Versionshinweise | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorversionen, finden Sie auf der Seite [Target-Versionshinweise – Vorabversion](/help/r-release-notes/target-release-notes.md). |
