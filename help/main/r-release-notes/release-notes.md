---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 579ebd9bebd3faa724f0d1d542f4d23766adefe3
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 24%

---

# [!DNL Target] Versionshinweise (aktuell)

Diese Versionshinweise enthalten Informationen zu Funktionen, Verbesserungen und Fehlerkorrekturen in der [!DNL Adobe Target Standard]- und [!DNL Target Premium]-Version. Sie finden hier auch Versionshinweise zu den [!DNL Target]-APIs, SDKs, der JavaScript-Bibliothek (at.js) von [!DNL Adobe Experience Platform Web SDK] sowie zu anderen Plattformänderungen.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 25.4.5 (25. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, das zu Diskrepanzen in den Zielgruppenauflistungen zwischen der Seite mit den [!UICONTROL Activity] Einstellungen und der [!UICONTROL Reporting]-Übersichtsseite führte. (TGT-52203)
* Es wurde ein Problem behoben, das das Hinzufügen einer neuen Seite zu einer Aktivität aufgrund eines Fehlers bei der ungültigen Benutzereingabe verhinderte. (TGT-52263)
* Es wurde ein Problem behoben, das dazu führte, dass `OptionLocalIDs` fälschlicherweise inkrementiert wurden, wenn die Option unverändert blieb. (TGT-52187)
* Es wurde ein Problem behoben, das dazu führte, dass `location` und `OptionLocalIDs` fälschlicherweise inkrementiert wurden, wenn die Option unverändert blieb. (TGT-52188)
* Es wurde ein Fehler behoben, der dazu führte, dass der Speicherort auf der Seite [!UICONTROL Overview] der Aktivität falsch war. (TGT-52182)
* Es wurde ein Problem behoben, bei dem für einen ungültigen Speicherort keine Warnung zu einem ungültigen Selektor angezeigt wurde. (TGT-52110)
* Es wurde ein Problem behoben, sodass heruntergeladene Berichtsdateien die in der Reporting-Benutzeroberfläche vorhandenen Daten korrekt anzeigen. (TGT-52068)
* Fehlerkorrektur: Batch-Vorgänge schlagen nach dem Hinzufügen von Seitenbereitstellungsregeln nicht fehl. (TGT-52097)
* Es wurde ein Fehler behoben, der dazu führte, dass [!DNL Target] alle Abfrageparameter aus der URL der Website kürzte. (TGT-52100)
* Es wurde ein Konsolenfehler behoben, der Kunden daran hinderte, Aktivitäten in der alten und aktualisierten [!DNL Target]-Benutzeroberfläche zu erstellen. (TGT-52181)
* Es wurde ein Problem behoben, durch das Kunden keine neuen Seiten hinzufügen konnten, was zu einem Fehler bei der ungültigen Benutzereingabe führte. (TGT-52258)
* Es wurde ein Problem behoben, das dazu führte, dass Änderungen nach dem Hinzufügen zusätzlicher Seiten und dem anschließenden Zurücknavigieren zur Registerkarte [!UICONTROL Experiences] verschwanden. (TGT-52264)
* Es wurde ein Problem behoben, durch das Kundinnen und Kunden daran gehindert wurden, die Zielgruppe in einer [!UICONTROL Experience Targeting] (XT)-Aktivität zu ändern. (TGT-52191)
* Fehlerkorrektur - Die Bearbeitung einer XT-Aktivität ist jetzt möglich, da die Benutzeroberflächenregel nicht unterstützt wird. (TGT-52273)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, bei dem Breadcrumbs nicht immer unten im Editor angezeigt wurden, was bei der präzisen Auswahl von Elementen zu Problemen führte. (TGT-52169)
* Es wurde ein Problem behoben, bei dem in der Dropdown-Liste [!UICONTROL Audience] aufgrund von Paginierung nicht alle Zielgruppen angezeigt wurden. (TGT-52204)
* Fehlerkorrektur - Jetzt wird keine Meldung mehr angezeigt, dass eine ungültige Benutzereingabe erfolgt ist, wenn neue Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten hinzugefügt werden. (TGT-52210)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Analytics for Target] (A4T) fälschlicherweise als Berichtsquelle ausgewählt wurde, obwohl die Kundin bzw. der Kunde keinen Zugriff auf A4T hatte. (TGT-52226)
* Es wurde ein Problem behoben, das das Speichern einer Aktivität mit der [!UICONTROL View a Page] URL-Metrik verhinderte. (TGT-52260)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Arbeitsbereiche beim Erstellen von Angeboten innerhalb einer Aktivität auszuwählen. (TGT-52289)
* Es wurde ein Problem behoben, durch das Kunden keine Aktivitäten in allen Arbeitsbereichen erstellen konnten. (TGT-52218)
* Es wurde ein Problem behoben, bei dem Änderungen von einem Erlebnis falsch angezeigt wurden, wenn zu einem anderen Erlebnis gewechselt wurde. (TGT-52184)
* Es wurde ein Problem behoben, bei dem das Standardangebot beim Öffnen der Aktivität nicht korrekt in der [!DNL Target]-Benutzeroberfläche angezeigt wurde. (TGT-52198)

## Aktualisierung der Target-Berechtigungen (22. April 2025)

Diese zukünftige Aktualisierung verbessert die organisatorische Kontrolle über [!DNL Target] Instanzkonfigurationen und verhindert versehentliche Aktualisierungen, die die Aktivitätsbereitstellung in verschiedenen Test- und Personalisierungsteams beeinträchtigen könnten.

Ab dem 22. April 2025 können nur [!UICONTROL Product]- und [!UICONTROL Solutions]-Administratoren die Einstellungen in den [!UICONTROL Administration] Abschnitten aktualisieren, unabhängig von ihrer Rolle in [!DNL Target] Arbeitsbereichen. Benutzende ohne diese Berechtigung haben schreibgeschützten Zugriff auf die [!UICONTROL Administration].

Weitere Informationen finden Sie unter [Verwaltung von Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.4 (17. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde eine Fehlermeldung hinzugefügt, die Benutzende anleitet, wie doppelte Optionen in einer Aktivität aufgelöst werden können. (TGT-51927)
* Es wurde ein Problem behoben, bei dem `ClickTrack` Selektoren beim Löschen von Seiten oder Erlebnissen mit Umleitungsangeboten nicht entfernt wurden. (TGT-51952)
* Es wurde ein Problem behoben, das dadurch verursacht wurde, dass leere `ClickTrack` zugelassen wurden. [!DNL Target] erfordert jetzt, dass das Auswahlfeld nicht leer sein darf. (TGT-52107)
* Es wurde ein Problem behoben, durch das Metriken fälschlicherweise mit doppelten Namen zugelassen wurden. Metriken erfordern jetzt eindeutige Namen. (TGT-52201)
* Es wurde ein Problem behoben, bei dem Zielgruppendefinitionen beim Bearbeiten des Targeting auf Angebotsebene in [!UICONTROL Automated Personalization] (AP)-Aktivitäten nicht sichtbar waren. (TGT-52148)
* Es wurde ein Problem behoben, das Kunden mit [!UICONTROL Editor] daran hinderte, Aktivitäten zu speichern. (TGT-52227)
* `OptionLocalIDs` nicht mehr falsch inkrementiert, wenn die Option unverändert bleibt. (TGT-52139)
* Fehlerkorrektur - Beim Erstellen einer Aktivität wird jetzt nicht mehr die Meldung „Ungültiger `optionLocalIds`&quot; angezeigt. (TGT-52154)
* Die Diskrepanzen zwischen den für eine Aktivität definierten `OptionLocalIDs` und den für die Definition von Erlebnissen definierten Diskrepanzen wurden behoben. (TGT-52215)
* Fehlerkorrektur - Beim Erstellen einer A/B-Aktivität tritt jetzt kein Validierungsfehler mehr auf. (TGT-51923)

## [!DNL Target Standard/Premium] 25.4.3 (11. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der Kunden daran hinderte, das Popup-Fenster mit Zielgruppeninformationen für bestimmte [!UICONTROL Experience Targeting] (XT)-Aktivitäten zu öffnen. (TGT-52049)
* Es wurde ein Problem behoben, bei dem die Zielgruppeneinstellung nach Änderungen im [!UICONTROL Visual Experience Composer] (VEC) auf &quot;[!UICONTROL All Visitors]&quot; zurückgesetzt wurde. (TGT-52132)
* Es wurde ein Problem behoben, bei dem Zielgruppenoptimierungen für bestimmte Aktivitäten nicht angezeigt wurden (TGT-52057)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine [!UICONTROL Experience Fragment] in den Standardarbeitsbereich einzufügen. (TGT-52073)
* Es wurde ein Problem behoben, bei dem ein Angebot als „Inhalt nicht gefunden“ angezeigt wurde und für eine [!UICONTROL Automated Personalization] (AP)-Aktivität nicht auf der [!UICONTROL Offers] angezeigt wurde. (TGT-52150)
* Es wurde die Möglichkeit hinzugefügt, innerhalb einer Aktivität doppelte Zielgruppen zuzulassen. (TGT-51200)
* Fehlerkorrektur - Nach der Bearbeitung wird für eine XT-Aktivität auf der Seite [!UICONTROL Goals & Settings] der falsche Mbox-Name angezeigt. (TGT-52026)
* Es wurde ein Problem behoben, bei dem `defaultContent` in Optionen angezeigt wurden, obwohl sie nicht in `experiences/optionLocations` waren. (TGT-52036)
* Es wurde ein Problem behoben, um sicherzustellen, dass leere Zeichenfolgen nicht in Nullwerte konvertiert werden. (TGT-52037)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden die [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] auf der [!UICONTROL Goals & Settings] Seite nach der Bearbeitung neu konfigurieren mussten. (TGT-52071)
* Es wurde ein Problem behoben, bei dem bei einer Aktivität ohne Seitenbereitstellungsregeln mehrere Regeln auf der [!UICONTROL Overview] angezeigt wurden. (TGT-52084)
* Es wurde eine Fehlermeldung für Benutzer hinzugefügt, die versuchen, ein Angebot mit Zeichen außerhalb der mehrsprachigen Basisebene wie Emojis zu speichern. (TGT-52105)
* Fehlerkorrektur - Beim Öffnen einer Aktivität wird jetzt nicht mehr die Fehlermeldung „Diese Aktivität verwendet eine oder mehrere Zielgruppen, die an der Quelle gelöscht wurden.“ (TGT-52120)
* Es wurde ein Problem behoben, bei dem ClickTrack-Metriken während der Bearbeitung nicht im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) angezeigt wurden. (TGT-52152)
* Es wurde ein Problem behoben, bei dem eine URL mit einem Abfrageparameter als Speicherort der Aktivität den Abfrageparameter auf der Seite [!UICONTROL Overview] der Aktivität nicht anzeigte. (TGT-51635)
* Es wurde ein Problem behoben, das die Anzeige der gesamten Erlebnis-URL in [!UICONTROL Browse mode] im [!UICONTROL Visual Experience Composer] (VEC) verhinderte. (TGT-52101)
* Es wurde ein Problem behoben, bei dem die Bearbeitung einer Aktivität dazu führte, dass die Seitenbereitstellung am Ende der URL ein &quot;/&quot; hinzufügte, wodurch sie ungültig wurde. (TGT-52114)
* Es wurde ein Problem behoben, bei dem der [!UICONTROL Activity QA]-Link im [!UICONTROL Form-Based Experience Composer] fälschlicherweise zur [!DNL Adobe Experience Cloud] Homepage umgeleitet wurde. (TGT-52055)
* Es wurde ein Problem behoben, bei dem zusätzliche Seiten, die zur [!UICONTROL A/B Test] hinzugefügt wurden, nach dem Speichern und erneuten Öffnen nicht beibehalten wurden. (TGT-51994)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Stile im Abschnitt Inline-Stil zu löschen. (TGT-52070)
* Der Zugriff auf [Karten für Zielgruppendefinitionen](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) im Dialogfeld &quot;[!UICONTROL Activity QA]&quot; wurde wiederhergestellt, ähnlich wie in der veralteten Benutzeroberfläche. (TGT-52056)
* Die aktualisierte Benutzeroberfläche hat Seiten oder Zielgruppen nicht ohne Änderungen gespeichert. Wenn Kundinnen und Kunden einer Aktivität neue Seiten oder Zielgruppen hinzugefügt, diese jedoch nicht geändert haben, haben [!DNL Target] die unveränderten Zielgruppen beim Speichern verworfen. An relevanten Stellen wurden Benachrichtigungen hinzugefügt, um Benutzer über dieses Verhalten zu informieren. (TGT-52104)

## [!DNL Target Standard/Premium] 25.4.1 (2. April 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Fehler behoben, der dazu führte, dass Erlebnis-Zielgruppen aus -Aktivitäten verschwanden. (TGT-52003)
* Fehlerkorrektur - Beim Versand treten jetzt keine unerwarteten Elemente mehr auf. (TGT-52011)
* Es wurde ein Problem behoben, durch das Kunden die Anzeige der Zielgruppe im Targeting-Diagramm auf der [!UICONTROL r]-Seite und während der Aktivitätsbearbeitung nicht sehen konnten. (TGT-52050)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Erlebnisse in [!UICONTROL Experience Targeting] (XT)-Aktivitäten nach Priorität neu anzuordnen. (TGT-52054)
* Es wurde ein Problem behoben, das beim Rückgängigmachen von Textstil-Änderungen zu falschem Rendering führte. (TGT-51876)
* Es wurde ein Problem behoben, durch das [!DNL Target] beim Ändern eines Umleitungsangebots auch alle [!UICONTROL ClickTrack] entfernt, die mit diesem Angebot verknüpft sind. (TGT-51936)
* Ein Problem wurde behoben, das dazu führte, dass [!DNL Target] beim Abbrechen von [!UICONTROL ClickTrack] die Auswahl fälschlicherweise speicherte. (TGT-51937)
* Es wurde ein Problem behoben, das nach dem Öffnen und Schließen der Mbox-Auswahl auf der [!UICONTROL Goals & Settings] ohne Änderungen zu einem Fehler wegen ungültigem Namen führte. (TGT-51983)
* Es wurde ein Problem behoben, das die Bearbeitung von Ad-hoc-Angeboten blockierte, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. (TGT-51984)
* Es wurde ein Problem behoben, das die Bearbeitung von Aktivitäten blockierte, die Ad-hoc-Angebote mit benutzerdefiniertem Code enthielten. (TGT-51995)
* Es wurde ein Problem behoben, das dazu führte, dass Ausschlussregeln beim Bearbeiten kombinierter Zielgruppendefinitionen als Einschlussregeln angezeigt wurden. (TGT-51999)
* Ein Problem wurde behoben, das dazu führte, dass benutzerdefinierter Code während der Erlebnisbearbeitung nicht korrekt angezeigt wurde. (TGT-52005)
* Es wurde ein Problem behoben, durch das die [!UICONTROL Insert Before]-Option zum Einfügen von Inhalten vor der Navigationsleiste nicht mehr verfügbar war. (TGT-52031)
* Fehlerkorrektur - Das Standarderlebnis in Berichten wird jetzt korrekt hervorgehoben. (TGT-51716)
* Es wurde ein Problem behoben, das beim Erstellen einer Aktivität eine `default message [Invalid optionLocalIds: xx]]` auslöste. (TGT-52038)

## at.js-Version 2.11.8 (31. März 2025)

* Behobene CodeQL-identifizierte Sicherheitslücke in der Validierung von Zeichenfolgen-Suffixen, um Edge-Fälle während Größenänderungs- und Verschiebungsvorgängen zu verhindern. (TNT-51516)

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=de) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

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
| [Adobe Priority-Produktaktualisierung](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Empfangen Sie vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen. |
| [Target-Versionshinweise – Vorabversion](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informationen zu den Target-Versionen des aktuellen Monats, einschließlich Informationen zu Vorabversionen. |
