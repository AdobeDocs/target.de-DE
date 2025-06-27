---
keywords: Versionshinweise;neue Funktionen;Versionen;Updates;Update;Version;Verbesserung;Verbesserungen;Fehlerbehebungen;Fehlerbehebungen;Updates,aktuelle Updates
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target], einschließlich SDKs, APIs und JavaScript-Bibliotheken.
landing-page-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
short-description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der aktuellen Version von  [!DNL Adobe Target].
title: Was ist in der aktuellen Version enthalten?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: f8e91caa133a1addc12ab1834d7e178df7e7a3ce
workflow-type: tm+mt
source-wordcount: '2725'
ht-degree: 14%

---

# [!DNL Target] Versionshinweise (aktuell)

Informieren Sie sich über die neuesten Funktionen, Verbesserungen und Fehlerbehebungen in [!DNL Adobe Target]. Diese Versionshinweise enthalten auch Aktualisierungen für [!DNL Target] APIs, SDKs, die [!DNL dobe Experience Platform Web SDK], at.js und ggf. andere Plattformkomponenten.

(Die Nummern in Klammern dienen der internen Nutzung durch [!DNL Adobe].)

## [!DNL Target Standard/Premium] 25.6.4 (Samstag, 27. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Der aktualisierten [!UICONTROL Visual Experience Composer] (VEC)-Benutzeroberfläche wurde die Option [!UICONTROL Rearrange] hinzugefügt, um sie an die im alten VEC verfügbaren Funktionen anzupassen. (TGT-46957 und TGT-52876)
* Es wurde ein Problem behoben, bei dem Änderungen an Variantenerlebnissen (z. B. Erlebnis B) in einer [!UICONTROL A/B Test] -Aktivität nicht beibehalten wurden. Nach dem Wechsel zwischen Erlebnissen würden die Änderungen an der Variante verschwinden. Dieses Problem hatte keine Auswirkungen auf das Kontrollerlebnis. (TGT-52664)
* Es wurde ein Problem behoben, bei dem bestimmte Kunden keine Aktivitäten erstellen oder speichern konnten, während andere dieselben Aktionen ohne Problem ausführen konnten. Das Problem war in allen Konten inkonsistent.(TGT-52842)
* Es wurde ein Problem behoben, bei dem Benutzende in der aktualisierten VEC keine Änderungen an die [!UICONTROL Page Load event] verschieben konnten, eine Funktion, die in der alten Benutzeroberfläche vorhanden war. (TGT-52617)
* Es wurde ein Problem in der aktualisierten Benutzeroberfläche behoben, bei dem [!UICONTROL page load] Ereignisse beim Erstellen von Änderungen in [!DNL Target] nicht sichtbar waren. Aktualisierungen wurden nur auf Ansichten angewendet. (TGT-52604)
* Ein Problem wurde behoben, das dazu führte, dass einige Aktivitätsänderungen in der aktualisierten VEC nicht korrekt angezeigt wurden. (TGT-52818)
* Fehlerkorrektur - Beim Abrufen von Berichtsdaten für [!UICONTROL Automated Personalization] (AP)-Aktivitäten tritt jetzt keine Nullzeiger-Ausnahme mehr auf. (TGT-52362)
* Es wurde ein Problem behoben, das verhinderte, dass Details auf Angebotsebene in der CSV-Datei für [!UICONTROL Automated Personalization] (AP)-Aktivitäten angezeigt wurden. (TGT-52675)
* Fehlerkorrektur - Beim Anwenden von Änderungen in der aktualisierten VEC werden Änderungen zunächst korrekt angezeigt, einschließlich der erwarteten [!UICONTROL Experience Fragment]. Wenn jedoch Erlebnisse gewechselt oder zusätzliche Bearbeitungen vorgenommen werden, können einige Änderungen aufgrund von Problemen mit dem Selektor nicht angewendet werden. (TGT-52679)
* Es wurde ein Problem behoben, bei dem bei Erstellung einer neuen Aktivität durch Klonen einer vorhandenen die Seiten-URLs aus der ursprünglichen Aktivität von den QA-Links in der geklonten Aktivität fälschlicherweise beibehalten wurden. (TGT-52775)
* Es wurde ein Problem behoben, durch das [!UICONTROL On-device Decisioning] unbeabsichtigt nicht in der aktualisierten VEC verfügbar waren. (TGT-52371)
* Ein Problem wurde behoben, das die Bearbeitung einer [!DNL Recommendations] verhinderte. Beim Versuch, über die Target-Benutzeroberfläche auf den VEC zuzugreifen, trat auf der Seite [!UICONTROL Overview] ein Fehler auf, der alle Änderungen verhinderte. (TGT-52823)
* Es wurde ein Problem behoben, das das Speichern einer [!DNL Recommendations]-Aktivität verhinderte, wenn Erlebnisnamen 50 Zeichen überstiegen. (TGT-52619)
* Es wurde ein Problem behoben, bei dem Kundinnen und Kunden eine Recommendations -Aktivität nicht speichern konnten, nachdem sie die Kriterien in der neuen Benutzeroberfläche geändert hatten. Das Problem scheint berechtigungsbezogen zu sein und betrifft nicht alle Benutzer mit ähnlichen Rollen. (TGT-52816)
* Es wurde ein Problem behoben, bei dem Benutzer mit der Rolle [!UICONTROL Editor] eine [!DNL Recommendations] Aktivität nicht bearbeiten konnten. Der Versuch, das Design zu ändern und die Aktivität zu speichern, führte zu einem 403-Fehler (Forbidden) und gab an, dass die Berechtigung &quot;[editor]&quot; erforderlich war, obwohl die Benutzerin bzw. der Benutzer diese Rolle bereits im entsprechenden Arbeitsbereich hatte. (TGT-52836)

## [!DNL Target Standard/Premium] 25.6.3 (Samstag, 20. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Fehlerkorrektur - Beim Kopieren einer Aktivität von einem Arbeitsbereich in einen anderen Arbeitsbereich treten jetzt keine Fehler mehr auf, z. B. „Darf nicht null sein“ oder „Irgendetwas ist schiefgelaufen“. (TGT-52474)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Automated Segments]- und [!UICONTROL Important Attributes]-Berichte für bestimmte Aktivitäten nicht generiert wurden. (TGT-52904)
* Fehlerkorrektur - Die standardmäßige Inhaltsverarbeitung in [!UICONTROL Automated Personalization] (AP)-Aktivitäten im aktualisierten VEC stimmt jetzt mit der veralteten Benutzeroberfläche überein. Das System fügt jetzt automatisch eine `optionGroup` mit dem Namen „Standardinhalt“ mit `optionGroupLocalId = 0` hinzu, wenn keine Gruppe explizit hinzugefügt wird. Diese Gruppe umfasst die Standardoption (z. B. `optionLocalId: 0`). Wenn der Standardinhalt entfernt wird, wird auch die entsprechende Optionsgruppe entfernt. (TGT-52651)
* Es wurde ein Problem in [!UICONTROL Multivariate Test] (MVT)-Aktivitäten behoben, bei dem die Wiederverwendung eines `experienceLocalId` aus zuvor entfernten Erlebnissen fälschlicherweise nicht zulässig war. (TGT-52672)
* Ein Problem wurde behoben, das das Kopieren oder Bearbeiten von Aktivitäten verhinderte, die ein Experience Fragment enthielten. Dadurch wurde der Fehler ausgelöst: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* Es wurde ein Problem behoben, bei dem URLs an Aktivitätspositionen Abfrageparameter aufgrund von ungültigen Zeichen, wie Schrägstrichen (/), nicht anzeigen konnten. (TNT52845)
* Die Validierungsfehlermeldung für [!DNL A/B Test] Aktivitätsaktualisierungen über die Backend-API wurde verbessert. Wenn doppelte Ortsnamen vorhanden sind, wird in der Meldung jetzt deutlich angegeben: „Doppelte Namen sind nicht zulässig“ für `locations.selectors`. (TGT-52589)
* Fehlerkorrektur - Beim Aktualisieren einer Live [!UICONTROL Recommendations]-Aktivität aufgrund einer nicht erkannten Eigenschaft in der Anfrage-Payload tritt jetzt kein Fehler mehr auf. Das System verarbeitet jetzt ordnungsgemäß die „Ungültige JSON. Fehler „Nicht erkannter Eigenschaftsname“. (TGT-52723)
* Fehlerkorrektur - Das Erstellen eines [!DNL Recommendations]-Designs ist jetzt möglich. Durch Klicken auf [!UICONTROL Create] wird die Meldung „Es sollte mindestens eine Entitätsvariable im Skript verwendet werden.“ ausgelöst. (TGT-52395 und TGT-52899)
* Es wurde ein Problem behoben, bei dem das erneute Speichern eines [!DNL Recommendations] Designs ohne Änderungen blockiert wurde. (TGT-52879)
* Fehlerkorrektur - Beim Speichern einer [!UICONTROL Recommendations]-Aktivität tritt jetzt kein Backend-Validierungsfehler mehr auf, der den Fehler „400 Bad Request“ verursacht. (TGT-52716)
* Fehlerkorrektur - Beim Bewegen des Mauszeigers über eine Mbox mit Sonderzeichen in der Dropdown-Liste &quot;[!UICONTROL Location]&quot; in der [!UICONTROL Form-Based Experience Composer] wird der Editor jetzt nicht mehr leer angezeigt und die Meldung „Fehler beim Ausführen von „querySelector“ für „Element“ ausgegeben.“ angezeigt. (TGT-52717)
* Verbesserte Genauigkeit des Zufuhrstatus mit einem neuen „PARTIALLY_IMPORTED“-Indikator. Zuvor wurden Feeds als „Erfolg“ markiert, selbst wenn nicht alle Zeilen in einer Datei importiert wurden, was irreführend war. (TGT-52892)
* Fehlerkorrektur - Nach der Migration zu AP V2 `/admin/rest/ui/v1/campaigns` bei bestimmten API-Aufrufen an Client-seitige Fehler zurückgegeben (HTTP 4xx). (TGT-52721)

## Aktualisiert: Umschalten der Version der [!DNL Target]-Benutzeroberfläche (17. Juni 2025) {#revised}

Seit dem 17. Juni 2025 sollten alle IMS-Organisationen für die aktualisierte [!DNL Target]-Benutzeroberfläche aktiviert sein, entweder für bestimmte Benutzer oder unternehmensweit, um mit dem Testen des neuen Erlebnisses zu beginnen.

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, hat das [!DNL Target]-Team den Zeitplan für die Einstellung angepasst:

* **30. Juni 2025**: Das [updated [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md) wird zum Standarderlebnis für alle IMS-Organisationen, die den Umschalter für die Benutzeroberflächenversion aktiviert haben.

   * Kunden, die derzeit standardmäßig die alte Benutzeroberfläche sehen, sehen die aktualisierte Benutzeroberfläche jetzt nach der Anmeldung.
   * Der Umschalter für die Benutzeroberflächenversion bleibt bis Ende Juli verfügbar, sodass Benutzer bei Bedarf zurückkehren können.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] empfiehlt dringend, die aktualisierte [!DNL Target]-Benutzeroberfläche zu verwenden. Wechseln Sie nur dann zur alten Benutzeroberfläche zurück, wenn ein Blocker-Problem auftritt. Wichtige [[!DNL Target]  zum Umschalten finden Sie unter (Einstellung der UI-Version (23. Mai 2025)](/help/main/r-release-notes/release-notes-for-previous-releases.md#toggle) in den Versionshinweisen für frühere Versionen .

* **15. Juli bis 30. Juli 2025**: Der Umschalter für die Benutzeroberflächenversion wird in Phasen dauerhaft deaktiviert. Betroffene IMS-Organisationen können nicht mehr zur alten Benutzeroberfläche zurückkehren.

   * Die Ausnahmen werden von Fall zu Fall überprüft.
   * Verzögerungen bei der Einstellung des Umschalters werden nur kurz (einige Tage) gewährt, während Blocker-Probleme behoben werden.

Wenden Sie sich bei Fragen oder ](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md), falls Sie bei dieser Umstellung Probleme erwarten, an die [Adobe-Kundenunterstützung.

## [!DNL Target Standard/Premium] 25.6.2 (Freitag, 12. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein [neuer FAQ-Artikel](/help/main/c-intro/updated-ui-faq.md) hinzugefügt, in dem allgemeine Fragen zur aktualisierten [!DNL Target]-Benutzeroberfläche und -[!UICONTROL Visual Experience Composer] (VEC) behandelt werden.
* Es wurde ein Problem behoben, bei dem die Regel &quot;[!UICONTROL URL - does not contain]&quot; in [!UICONTROL Page Delivery] nicht funktionierte, sodass Inhalte angezeigt werden konnten, selbst wenn sie eigentlich hätten blockiert werden sollen. (TGT-52754)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Page Delivery] fälschlicherweise die Fehlermeldung „Doppelte Seiten-URLs sind nicht zulässig. (TGT-52765)
* Es wurde ein Problem behoben, bei dem Zielgruppen für [!UICONTROL Page Delivery]-URLs, die Experience Fragments enthalten, mit fälschlicherweise angefügtem # erstellt wurden. (TGT-52786)
* Es wurde ein Problem behoben, bei dem das Kopieren einer Aktivität und das Bearbeiten der Einstellungen auf der Seite [!UICONTROL Goals and Settings] dazu führte, dass die [!DNL Target]-Benutzeroberfläche nicht mehr reagierte. (TGT-52797)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, durch das fälschlicherweise eine zusätzliche Seite in einer [!UICONTROL A/B Test]-Aktivität an dieselbe URL umgeleitet werden konnte. (TGT-51838)
* Es wurde ein Problem behoben, bei dem Änderungen an Metriken auf der Seite [!UICONTROL Goals and Settings] beim Bearbeiten einer Aktivität nicht gespeichert wurden. (TGT-52799)
* Es wurde ein Problem behoben, bei dem das Hinzufügen eines neuen Erlebnisses während des Ladevorgangs des Web-Editors dazu führte, dass das neue Erlebnis Inhalte aus dem vorherigen Erlebnis duplizierte. (TGT-51397)
* Es wurde die Möglichkeit wiederhergestellt, benutzerdefinierten Code außerhalb des `<head>`-Tags zu verwenden, eine Funktion, die zuvor in der Legacy-Benutzeroberfläche von Target verfügbar war. (TGT-52304 und TGT-52300)
* Unnötige Validierung bei der Auswahl des Standardarbeitsbereichs während der Aktivitätserstellung wurde entfernt. Die obligatorische Eigenschaftenvalidierung gilt nicht mehr für den Standardarbeitsbereich, bleibt aber für nicht standardmäßige Arbeitsbereiche bestehen. (TGT-52449)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, bei dem `triggerView()` Aufrufe nicht erkannt wurden. (TGT-52575)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, das verhinderte, dass Benutzer Änderungen an [!UICONTROL Single Page Application] (SPA)-Ansichten hinzufügen konnten. (TGT-52556)
* Ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche wurde behoben, das dazu führte, dass Kundinnen und Kunden keine Angebotsdetails anzeigen konnten. (TGT-52607)
* Es wurde ein Problem behoben, bei dem Aktualisierungen an Angeboten in der [!UICONTROL Offers Library] nicht in der aktualisierten [!UICONTROL Visual Experience Composer] (VEC) widergespiegelt wurden. (TGT-52637)
* Fehlerkorrektur - Der Abschnitt Angebote wird jetzt beim Erstellen einer Aktivität korrekt angezeigt. (TGT-52773)
* Es wurde eine Validierung hinzugefügt, um sicherzustellen, dass alle `optionLocalIds`, auf die in `optionGroups` verwiesen wird, im Optionen-Array vorhanden sind. Ungültige Verweise werden bei der Erstellung der Aktivität automatisch entfernt. (TGT-52687)
* Es wurde ein Problem behoben, bei dem Berichtsgruppen und Ausschlüsse nach dem Hinzufügen eines neuen Angebots nicht beibehalten wurden. (TGT-52728)
* Es wurde ein Problem behoben, bei dem für Aktivitäten ohne [!UICONTROL Activity QA] Schaltfläche eine leere Optionsauswahl angezeigt wurde. (TGT-52733)
* Es wurde ein Problem behoben, bei dem QA-Links Inhalte nicht richtig rendern konnten. (TGT-52718)
* Es wurde ein Problem behoben, bei dem das Ersetzen eines Elements durch ein Experience Fragment die Änderungen in der QS-Umgebung nicht korrekt widerspiegelte. (TGT-52762)
* Es wurde ein Problem im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) behoben, das zu einem Fehler „Ungültige Eingabe“ führte, wenn Benutzende versuchten, Experience Fragments hinzuzufügen. (TGT-52701)
* Es wurde ein Problem behoben, bei dem das Modal „Zielgruppe bearbeiten“ beim Bearbeiten des Zielgruppen-Targeting im aktualisierten [!UICONTROL Visual Experience Composer] (VEC) leer erschien. (TGT-52749)
* Es wurde eine Nachricht hinzugefügt, die Benutzer darüber informiert, wenn im ausgewählten Arbeitsbereich nicht auf eine Entität zugegriffen werden kann. (TGT-52767)
* Es wurde ein Problem behoben, bei dem die Benutzeroberfläche die manuelle Zuweisung einer Umgebungs-ID zu einem Kriterium nicht zuließ. Stattdessen wird standardmäßig die ID für die [!UICONTROL Product Catalog Search] Hostgruppe verwendet. Mit dieser Fehlerbehebung wird sichergestellt, dass Kriterienänderungen jetzt in allen Umgebungen angewendet werden, nicht nur in der Standardumgebung. (TGT-52817)
* Es wurde ein Problem behoben, bei dem die Option &quot;[!UICONTROL Download Recommendations data]&quot; für [!UICONTROL Experience Targeting] (XT)-Aktivitäten mit Empfehlungen fehlte. (TGT-52730 und TGT-52756)

## [!DNL Target Standard/Premium] 25.6.1 (Samstag, 6. Juni 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

* Es wurde ein Problem behoben, bei dem QA-Links nicht das richtige Erlebnis für die zugehörige Aktivität lieferten. (TGT-52163 und TGT-52790)
* Fehlerkorrektur - Bei QA-Links fehlt jetzt die zugehörige Zielgruppen-ID. (TGT-52722)
* Es wurde ein Problem behoben, um sicherzustellen, dass Erlebnisse nur bereitgestellt werden, wenn die konfigurierten URL-Bedingungen für die Seitenbereitstellung korrekt erfüllt sind. (TGT-52696)
* Es wurde ein Problem behoben, das Kunden daran hinderte, eine [!DNL Recommendations] Design-Vorlage zu erstellen. Der Versuch, eine Vorlage zu erstellen, hat den Fehler ausgelöst: „Im Skript sollte mindestens eine Entitätsvariable verwendet werden.“ (TGT-52395)
* Es wurde ein Problem behoben, das das Speichern von [!DNL Recommendations]-Designs mithilfe von Velocity-Arrays verhinderte. Die Fehlermeldung „Es muss mindestens eine Entitätsvariable im Skript verwendet werden“ wurde fälschlicherweise ausgelöst. (TGT-52734)
* Es wurde ein Problem behoben, bei dem Änderungen in der [!UICONTROL Visual Experience Composer] (VEC) nicht zugänglich waren, wenn die Seite für interne Web-Seiten nicht geladen werden konnte. (TGT-52488 UND TGT-52470)
* Es wurde ein Problem behoben, bei dem das [!UICONTROL Modifications]-Bedienfeld bei kleineren Bildschirmgrößen in Visual Experience Composer nicht sichtbar war. (TGT-52470)
* Fehlerkorrektur - Im aktualisierten VEC tritt jetzt kein Fehler mehr auf, bei dem der Wechsel vom [!UICONTROL Browse]- in den [!UICONTROL Design]-Modus zu einem Konsolenfehler führte und weitere Interaktionen verhinderte. (TGT-52532)
* Es wurde ein Problem in Visual Experience Composer behoben, bei dem durch Klicken auf bestimmte Elemente unbeabsichtigt deren Größe erweitert wurde. (TGT-52497)
* Es wurde ein Problem behoben, bei dem bestimmte Seitenelemente nicht geladen oder in Visual Experience Composer nicht erkannt werden konnten, wodurch Interaktionen wie das Auswählen von Schaltflächen oder Bannern verhindert und die genaue Ereignisverfolgung in -Aktivitäten unterbrochen wurde. (TGT-52663)
* Es wurde ein Problem behoben, das verhinderte, dass Kundinnen und Kunden Angebote in [!UICONTROL Automated Personalization] (AP)-Aktivitäten löschen oder entfernen konnten. (TGT-52690)
* Es wurde ein Problem behoben, das zu einem inkonsistenten Verhalten bei der Aktivitätsqualifizierung in mehrseitigen Aktivitäten führte. (TGT-52694)
* Es wurde ein Fehler behoben, der dazu führte, dass auf der Seite [!UICONTROL Overview] der Aktivität eine ungültige URL für die [!UICONTROL Activity Location] angezeigt wurde. (TGT-52695)
* Ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche wurde behoben, das dazu führte, dass für Aktivitätsspeicherorte doppelte Einträge angezeigt wurden. (TGT-52693)
* Es wurde ein Problem behoben, das einen `getAudiencesV3` auslöste und Kunden daran hinderte, Aktivitäten zu bearbeiten oder zu kopieren. (TGT-52709)
* Fehlerkorrektur - Beim Hinzufügen von [!UICONTROL Experience Fragments]- oder HTML-Angeboten zu einer Aktivität tritt jetzt kein Fehler mehr wegen ungültiger Payload auf. (TGT-52779 und TGT-52773)
* Fehlerkorrektur - In der aktualisierten [!DNL Target]-Benutzeroberfläche wird E[!UICONTROL xperience Fragments] aufgrund eines ungültigen Eingabefehlers nicht mehr korrekt angezeigt. (TGT-52701)
* Es wurde ein Problem behoben, das Kunden daran hinderte, Aktivitäten im [!UICONTROL Form-based Experience Composer] aufgrund eines ungültigen Benutzerfehlers zu bearbeiten. (TGT-52470)
* Es wurde ein Lokalisierungsproblem in der koreanischen Sprache behoben, bei dem bei früheren Übersetzungen Zeichen außerhalb der mehrsprachigen Basisebene verwendet wurden. Die aktualisierte Übersetzung verwendet geeignete Zeichen, die die beabsichtigte Bedeutung genau vermitteln. (TGT-52508 und TGT-52509)
* Fehlerkorrektur - Bei der Lokalisierung in Koreanisch tritt bei der Auswahl des Start- und Enddatums für eine Aktivität kein Übersetzungsproblem mehr auf, wenn die Übersetzung für „Datum“ inkonsistent ist. (TGT-52510)

## Einstellen der Version der [!DNL Target]-Benutzeroberfläche - Umschalten (23. Mai 2025) {#toggle}

>[!IMPORTANT]
>
>Das [!DNL Target]-Team hat die Timeline für den Umschalter der Version der Benutzeroberfläche angepasst, sodass dieser nicht mehr unterstützt wird. Weitere Informationen finden [ unter  [!DNL Target] Aktualisiert:UI-Versions-Umschalter (17. Juni 2025)](#revised).

Der Rollout der neuen [!DNL Target]-Benutzeroberfläche wird bis zum 27. **2025**. Ab diesem Zeitpunkt haben alle Kunden Zugriff auf die neueste Version der Benutzeroberfläche.

Ab **22. Juni** wird der Umschalter für die Benutzeroberflächenversion entfernt. Alle Benutzer wechseln dauerhaft zur neuen Benutzeroberfläche, ohne die Möglichkeit, zur vorherigen Version zurückzukehren.

>[!NOTE]
>
>Kunden mit Sonderfällen, bei denen der Umschalter nach dem 22. Juni beibehalten werden muss, können sich zwecks Unterstützung an die Adobe-Kundenunterstützung wenden.

### Wichtige Informationen zum Umschalten der Benutzeroberflächenversion

Wir bieten eine temporäre Funktion, mit der Sie mithilfe einer Umschaltfläche zwischen der aktualisierten [!DNL Target]-Benutzeroberfläche und der Legacy-Version wechseln können. Diese Option ist nur während der letzten Phase des Rollouts der Benutzeroberfläche verfügbar.

![Umschalter für Target-Benutzeroberflächenversion](/help/main/r-release-notes/assets/toggle.png)

Sobald der Rollout abgeschlossen ist, wird der Umschalter entfernt und alle Benutzenden werden am (22. **2025) dauerhaft zur aktualisierten Benutzeroberfläche**. Adobe empfiehlt, vorauszuplanen, da diese Funktion bald auslaufen wird.

### Einschränkungen des Umschalt-Verhaltens der Benutzeroberfläche

* **Sichtbarkeit neuer Aktivitäten**: Aktivitäten, die in der aktualisierten Benutzeroberfläche erstellt wurden, werden nicht angezeigt, wenn Sie zur alten Benutzeroberfläche zurückkehren.
* **Bearbeiten vorhandener Aktivitäten**: Änderungen an vorhandenen Aktivitäten (die ursprünglich in der veralteten Benutzeroberfläche erstellt wurden), während die aktualisierte Benutzeroberfläche verwendet wird, werden auf Ihrer Website veröffentlicht. Diese Aktualisierungen werden jedoch nicht in der alten Benutzeroberfläche angezeigt, wenn Sie zurückwechseln. Nur die letzten Aktualisierungen, die von der alten Benutzeroberfläche vorgenommen wurden, werden dort angezeigt.
* **Konsistenz der Aktivitätsdetails**: Die neuesten Änderungen werden unabhängig von der verwendeten Benutzeroberfläche auf Ihrer Live-Website angezeigt. In der veralteten Benutzeroberfläche werden jedoch nur die neuesten Änderungen angezeigt, die in dieser Version vorgenommen wurden. Dies kann verwirrend sein, wenn die in der aktualisierten Benutzeroberfläche bearbeiteten Aktivitäten anders aussehen als die in der alten Benutzeroberfläche.

### Weitere Informationen zur aktualisierten Benutzeroberfläche

* [[!DNL Target Standard/Premium] 25.2.1 (17. Februar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für [!UICONTROL Activities], [!UICONTROL Recommendations] und den [!UICONTROL Visual Experience Composer] (VEC).

* [[!DNL Target Standard/Premium] 25.1.1 (9. Januar 2025) Versionshinweise](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Bietet eine Zusammenfassung der wichtigsten Änderungen an der Benutzeroberfläche in [!DNL Target] für die [!UICONTROL Offers Library].

* [Grundlegendes zur  [!DNL Target] -Benutzeroberfläche](/help/main/c-intro/understand-the-target-ui.md): Bietet einen kurzen Überblick, der Ihnen hilft, sich mit [!DNL Target] vertraut zu machen, und enthält Links für detailliertere Informationen und schrittweise Anweisungen.

* [[!UICONTROL Visual Experience Composer] Änderungen](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): Mit der [!DNL Adobe Target Standard/Premium]-Version 25.2.1 (17. Februar 2015) wird eine aktualisierte [!UICONTROL Visual Experience Composer] (VEC) eingeführt. In diesem Artikel werden die Unterschiede zwischen der alten und der aktualisierten Version des VEC erläutert.

* [[!UICONTROL Visual Experience Composer] Optionen](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): In diesem Artikel werden die aktualisierte VEC-Benutzeroberfläche und ihre Optionen erläutert.

* [[!DNL Target] Häufig gestellte Fragen zur Aktualisierung der Benutzeroberfläche](/help/main/c-intro/updated-ui-faq.md): In dieser häufig gestellten Frage werden häufige Fragen zur neuen [!DNL Target]-Benutzeroberfläche und -[!UICONTROL Visual Experience Composer] (VEC) behandelt, einschließlich Navigationsänderungen, Funktionsspeicherorte und der Einstellung des Umschalters für die temporäre Benutzeroberfläche. Unabhängig davon, ob Sie Marketing-Experte, Entwickler oder Administrator sind, hilft Ihnen diese häufig gestellte Frage dabei, den Übergang reibungslos zu gestalten und die aktualisierte Benutzeroberfläche optimal zu nutzen.

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
