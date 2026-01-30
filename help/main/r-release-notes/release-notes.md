---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerkorrekturen;Aktualisierungen;aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6b92e823c854996e074716a7b8c4856176710c24
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 15%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL Adobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## Zeitkritische Updates, die Sie kennen sollten {#time-sensitive}

[!BADGE Wichtig]{type=Informative}

Für zeitkritische Updates im Zusammenhang mit [!DNL Adobe Target] und Ihrer Implementierung bietet [!DNL Adobe] detaillierte Versionshinweise und Dokumentation über [!UICONTROL Experience League]. Im Folgenden finden Sie einige wichtige Highlights, die für Ihre Implementierung relevant sind:

### Veraltungs-Umschalter für [!DNL Target]-Benutzeroberfläche

Weitere Informationen finden Sie unter [[!DNL Target] Häufig gestellte Fragen zur Benutzeroberflächen-Aktualisierung](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.1.1 (18. Januar 2026)

**Aktivitäten**

+++Details anzeigen

* **Aktivität kann nicht kopiert werden - ungültige Benutzereingabe.** Das Problem, das dazu führt, dass beim Kopieren einer Aktivität der nicht hilfreiche Fehler „Ungültige Benutzereingabe“ angezeigt wird, wurde behoben. Zuvor wurden beim Duplizieren einer Aktivität die Workspace-spezifischen Eigenschaftszuweisungen nicht beibehalten, sodass das Backend die Speicheranfrage ablehnt, da für die ABA-Aktivität mindestens eine Eigenschaft erforderlich ist, die zu einem nicht standardmäßigen Workspace gehört. Diese Diskrepanz hat einen allgemeinen Fehler in der Benutzeroberfläche ausgelöst, sodass Benutzende ohne Anleitung bleiben. Durch die Korrektur wird sichergestellt, dass Arbeitsbereichszuweisungen bei Kopiervorgängen korrekt beibehalten werden, sodass Benutzende die kopierte Aktivität speichern können, ohne Änderungen vorzunehmen, und keine irreführenden Validierungsfehler auftreten. (TGT-54282)
* **Aktivieren Sie die Spalte Arbeitsbereich im Angebot des Web-Editors.** Dieses Update behebt Verwirrung bei Kunden, die durch Angebote aus der [!UICONTROL Default Workspace] in anderen Arbeitsbereichen im Web-Editor verursacht wurde. Obwohl dieses Verhalten wie vorgesehen funktioniert, [!UICONTROL Default Workspace] Angebote absichtlich in allen Arbeitsbereichen sichtbar sind, berichteten Kunden, dass die Benutzeroberfläche den Ursprung des Arbeitsbereichs nicht klar machte, insbesondere beim Erstellen von Aktivitäten in einem nicht standardmäßigen Arbeitsbereich wie „Genehmigende Personen“. Um die Übersichtlichkeit zu verbessern, wurde die Spalte [!UICONTROL Workspace] jetzt in der Angebotsliste des Web-Editors aktiviert, sodass Benutzende einfach erkennen können, zu welchem Arbeitsbereich die einzelnen Angebote gehören, und eine Fehlinterpretation der angezeigten zusätzlichen Angebote vermieden werden kann. (TGT-54138)
* **Links mit target=„_blank“ werden in einer neuen Registerkarte geöffnet.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem erstellte Websites, die Links mit ~target=„_blank“~ enthalten, beim Klicken im [!UICONTROL Browse] in einer neuen Browser-Registerkarte geöffnet wurden, was das Vorschauerlebnis im Editor störte. Das Verhalten trat auf, weil die nativen Link-Attribute der erstellten Seite nicht von der eingefügten JavaScript der Erweiterung abgefangen wurden, anders als in der alten Benutzeroberfläche, in der Ankerelemente transformiert und ihre Ziele überschrieben wurden, um die Navigation im Editor zu behalten. Die Aktualisierung stellt sicher, dass Links, die ~target=„_blank“~ verwenden, jetzt im Web-Editor ordnungsgemäß verarbeitet werden, sodass externe Registerkarten beim Authoring nicht mehr geöffnet werden. (TGT-54134)
* **Warnhinweis zur Aufhebung der Auswahl.** Dieses Update enthält eine visuelle Warnung, die Benutzerinnen und Benutzer deutlich informiert, wenn sie die Auswahl einer automatisch erkannten Eigenschaft im Aktivitätseditor aufheben. Zuvor gab das Entfernen einer automatisch erkannten Eigenschaft keinen Hinweis darauf, dass die Eigenschaft dauerhaft gelöscht würde, was zu einem versehentlichen Verlust der Targeting-Konfiguration führen könnte. Durch die Korrektur wird ein Warnsymbol hinzugefügt, das dem Verhalten in der veralteten Benutzeroberfläche entspricht und Benutzer darüber informiert, dass durch Deaktivieren der Eigenschaft diese aus der Aktivität entfernt wird. (TGT-54121)
* **[!UICONTROL Workspaces]Dropdown-Liste ist im [!UICONTROL Users] Abschnitt auf 20 begrenzt.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem im Dropdown-Menü [!UICONTROL Workspaces] im Abschnitt [!UICONTROL Administration] > [!UICONTROL Users] nur 20 Arbeitsbereiche angezeigt wurden, selbst wenn ein Benutzer Zugriff auf viele weitere hatte. Der zugrunde liegende GraphQL-Aufruf für `licenseGroups` war ebenfalls auf 20 Ergebnisse beschränkt, was dazu führte, dass die Benutzeroberfläche eine unvollständige Liste anzeigte, obwohl die Benutzenden Zugriff auf mehr Arbeitsbereiche im Unternehmen hatten. Durch das Update wird diese feste Grenze entfernt, sodass der vollständige Satz verfügbarer Arbeitsbereiche jetzt zurückgegeben und korrekt angezeigt wird. (TGT-53820)
* **Es wurde ein Problem behoben, bei dem die Spalte Arbeitsbereich im modalen Angebotsfenster nicht angezeigt wurde.** Es wurde ein Problem behoben, bei dem das Modal „Angebote“ die Spalte „Arbeitsbereich“ in der aktualisierten Benutzeroberfläche nicht anzeigte. Dies führte zu Verwirrung bei den Kunden, da Angebote aus der [!UICONTROL Default Workspace] neben Angeboten aus dem ausgewählten Arbeitsbereich ohne Angabe ihrer Herkunft angezeigt wurden. Die Spalte Arbeitsbereich ist jetzt aktiviert, sodass Kunden eindeutig identifizieren können, zu welchem Arbeitsbereich die einzelnen Angebote gehören. (TGT-52320)

+++

**Eigenschaften**

+++Details anzeigen
* **Die Aktivitätsbearbeitung sollte keine automatisch erkannte Eigenschaft hinzufügen, wenn sie bereits entfernt wurde.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem durch die Bearbeitung einer Aktivität automatisch eine automatisch erkannte Eigenschaft wieder eingeführt wird, die zuvor entfernt wurde. Beim erneuten Öffnen einer Aktivität zur Bearbeitung hat das System die entfernte Eigenschaft fälschlicherweise wiederhergestellt, was zu inkonsistentem Verhalten und Verwirrung in der [!UICONTROL Properties List] führte. Die Aktualisierung stellt sicher, dass eine automatisch erkannte Eigenschaft nach dem Entfernen bei allen nachfolgenden Bearbeitungen entfernt bleibt und nicht wieder angezeigt wird, es sei denn, die Benutzerin oder der Benutzer fügt sie explizit wieder hinzu. (TGT-54182)
* **Fügen Sie keine automatisch erkannten Eigenschaften hinzu, wenn sie bereits entfernt wurden.** Mit dieser Fehlerbehebung wird sichergestellt, dass eine Benutzerin oder ein Benutzer, die bzw. der manuell eine automatisch erkannte Eigenschaft aus einer Aktivität entfernt hat, diese bei der nachfolgenden Navigation im Aktivitätseditor nicht mehr wieder einführt. Wenn ein(e) Benutzende(r) zuvor die Auswahl einer automatisch erkannten Eigenschaft aufgehoben, zum Schritt [!UICONTROL Targeting] verschoben und dann zu [!UICONTROL Experiences] zurückgekehrt hat, füllt der Editor die entfernte Eigenschaft erneut auf der Grundlage der automatisch erkannten Liste, die im Statusbereich des Aktivitätseditors gespeichert ist. Die aktualisierte Logik vergleicht jetzt die automatisch erkannten Eigenschaften mit den aktuellen Eigenschaften im Bereich ~ActivityState~ und verhindert, dass automatisch erkannte Eigenschaften, die der Benutzer bereits entfernt hat, erneut hinzugefügt werden. Dies führt zu einem konsistenten Verhalten über alle Schritte hinweg und respektiert die Benutzerabsicht. (TGT-54181)
* **Fügen Sie automatisch erkannten Text zur Eigenschaftenliste hinzu.** Diese Verbesserung aktualisiert die [!UICONTROL Properties List], um alle Eigenschaften, die automatisch vom System erkannt wurden, deutlich zu kennzeichnen. Wenn eine automatisch erkannte Eigenschaft auch im für den Benutzer sichtbaren [!UICONTROL Properties List] vorhanden ist, wird nun neben dem Namen der Eigenschaft der Text „(Automatisch erkannt)“ angezeigt, wobei der im Status ~ActivityEditorSlice~ gespeicherte Wert verwendet wird. Dies spiegelt das Verhalten der alten Benutzeroberfläche wider und hilft Benutzenden, einfach zwischen manuell ausgewählten Eigenschaften und den automatisch identifizierten Eigenschaften zu unterscheiden. (TGT-54120)
* **Fügen Sie automatisch erkannte [!UICONTROL Properties] in den Status hinzu.** Durch diese Aktualisierung wird sichergestellt, dass der ~ActivityEditorSlice.ExperienceEditor~-Status durchgängig eine aktuelle Liste aller automatisch erkannten Eigenschafts-IDs verwaltet, die vom Web-Editor in die Registerkarte [!UICONTROL Experiences] übergeben werden. Jedes Mal, wenn der/die Benutzende zur Registerkarte [!UICONTROL Experiences] navigiert, wird der Status mit allen neu erkannten Eigenschaften aktualisiert, wobei Duplikate vermieden werden, sodass ein genaues Tracking und ein zuverlässiges nachgelagertes Verhalten gewährleistet sind. (TGT-54119)

+++

**Recommendations**

+++Details anzeigen
* **[!UICONTROL Environment]Dropdown-Liste zeigt nur 100 Ergebnisse an.** Mit dieser Fehlerbehebung wird eine Einschränkung behoben, bei der Kunden mit mehr als 100 Umgebungen nur die ersten 100 Einträge in der Dropdown-Liste &quot;[!UICONTROL Environment]&quot; in [!UICONTROL Recommendations] sehen konnten. Die zugrunde liegende GraphQL-Abfrage ~getEnvironmentsV2~) wurde mit einer hartcodierten Seitengröße von 100 paginiert, wodurch die Benutzeroberfläche auch dann nur eine Teilliste anzeigte, wenn zusätzliche Seiten verfügbar waren. Für Kunden mit mehr als 100 Umgebungen führte dieses Problem zu fehlenden Optionen und einer unvollständigen Auswahl. Durch die Aktualisierung wird das Limit erhöht, sodass alle Umgebungen zurückgegeben und angezeigt werden. So wird unabhängig von der Anzahl der Umgebungen eine vollständige Sichtbarkeit sichergestellt. (TGT-53903)

+++

**Berichte**

+++Details anzeigen

* **Es wurde ein Problem behoben, bei dem der [!UICONTROL Reports] nicht deutlich erweiterbare Spalten anzeigte.** Es wurde ein Problem behoben, bei dem die Berichtstabelle nicht eindeutig zeigte, dass zusätzliche Spalten in der aktualisierten Benutzeroberfläche erweitert werden konnten. Dem [!UICONTROL Reports] Pfeil neben den Spaltenüberschriften wurde eine QuickInfo hinzugefügt, die verschwindet, damit Kunden verstehen, dass mehr Spalten verfügbar sind.

+++

**Ansichten**

+++Details anzeigen

* **Auf Ansichten angewendete Änderungen können nicht gelöscht werden.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem Benutzende Änderungen innerhalb einer Aktivität nur löschen konnten, wenn die Änderung zuvor erneut auf zusätzliche Ansichten angewendet wurde. Beim Bearbeiten einer Aktivität (z. B. der Aktivitäts-ID 302467) hatte der Versuch, eine Änderung zu löschen, keinerlei Wirkung, weshalb die Benutzer keine unerwünschten Änderungen entfernen konnten. Nachdem eine Änderung jedoch mit „Auf weitere Ansichten anwenden“ erneut angewendet und einem `Page Load`-Ereignis zugewiesen wurde, funktionierte der Löschvorgang plötzlich wie erwartet. (TGT-54088)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen
* **[!UICONTROL Experience Fragment]Name wurde in der neuen VEC-Benutzeroberfläche abgeschnitten** (TGT-54312)
* **[!UICONTROL Advanced Settings] kann nicht für [!UICONTROL Revenue] Metrik verwendet werden.** Mit dieser Fehlerbehebung wird ein Problem behoben, bei dem Benutzende beim Konfigurieren von [!UICONTROL Advanced Settings] für die [!UICONTROL Revenue]-Metrik in [!UICONTROL Goals & Settings] den 403-Fehler „Zugriff verweigert“ hatten. Das Problem trat beim Hinzufügen einer Abhängigkeitsbedingung auf, die mit dem primären Ziel verknüpft war. Das Backend benötigte fälschlicherweise die Berechtigung zum Bearbeiten selbst für Benutzer, die bereits über ausreichende Berechtigungen zum Erstellen und Bearbeiten von Aktivitäten verfügten. Daher ist das Speichern der Aktivität trotz gültiger Konfiguration fehlgeschlagen. Durch die Aktualisierung wird die Berechtigungsprüfung korrigiert, sodass Benutzende mit geeignetem Zugriff erfolgreich Abhängigkeiten von Umsatzmetriken hinzufügen können, ohne einen Fehler wegen verbotener Ressourcen auszulösen. (TGT-54092)
* **Es wurde ein Problem behoben, bei dem die Schaltfläche Hinzufügen nicht auf ausgewählte Bilder angewendet wurde.** Es wurde ein Problem behoben, das Kunden daran hinderte, bestimmte Bilder hinzuzufügen, wenn sie ein Bild im Prozess zum Erstellen einer Aktivität auswählen oder aktualisieren wollten. Wenn Kunden nach bestimmten Assets suchen, z. B. nach Bildern, die bei der Suche nach „ipp“ zurückgegeben werden, wird das ausgewählte Bild durch Klicken auf die Schaltfläche &quot;[!UICONTROL Add]&quot; nicht angewendet und es wurde keine Änderung erstellt. Die Auswahl anderer Bilder, z. B. `Homepage-banner-1-moz.jpg`, funktionierte weiterhin wie erwartet. Diese Aktualisierung stellt sicher, dass alle gültigen Bilder in der aktualisierten Benutzeroberfläche konsistent angewendet werden können. (TGT-53610)
* **Es wurde ein Problem behoben, bei dem durch das Löschen einer URL-Bedingung die Konfiguration der Zielmetrik zurückgesetzt wurde.** Es wurde ein Problem behoben, bei dem das Entfernen einer einzelnen URL-Bedingung in der [!UICONTROL Goal]-Metrik dazu führte, dass die gesamte Konfiguration in der aktualisierten Benutzeroberfläche zurückgesetzt wurde. Als Kundinnen und Kunden versuchten, eine gespeicherte URL-Bedingung unter [!UICONTROL Conversion] > [!UICONTROL Viewed a Page] zu löschen, wechselte der Zieltyp unerwartet zu [!UICONTROL Viewed an Mbox], und alle zuvor konfigurierten Einstellungen wurden entfernt. Durch diese Aktualisierung wird sichergestellt, dass nur die ausgewählte URL-Bedingung gelöscht wird und alle verbleibenden Zieleinstellungen erhalten bleiben. (TGT-53271)
* **Es wurde ein Problem behoben, bei dem die Suche nicht durch Unterordner führte.** Es wurde ein Problem behoben, bei dem bei der Suche nach Angeboten keine Ergebnisse aus Unterordnern in der aktualisierten Benutzeroberfläche zurückgegeben wurden. Kunden konnten ein Angebot nur finden, wenn sie manuell zu dem Ordner navigiert sind, in dem es gespeichert war, wodurch das Suchverhalten nicht mit den API-Funktionen konsistent war. Die Suche unterstützt jetzt das rekursive Durchsuchen von Ordnern, damit Kunden Angebote finden können, ohne jeden Ordner einzeln öffnen zu müssen. (TGT-51954)

+++

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
