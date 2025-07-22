---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 065220af5c8e3b6cc25ef7289d006a901d2e932a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 15%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: 22. Juli 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.7.3 (Freitag, 24. Juli 2025)

Aufgrund von kürzlich festgestellten Problemen, die in erster Linie mit komplexen Kundenanpassungen zusammenhängen, enthält diese Version die folgenden Fehlerbehebungen und Aktualisierungen:

**Aktivitäten**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem die `buildViews`-Methode in der Builder-Klasse fälschlicherweise auf die Gesamtanzahl der Ansichten `viewMaxLocalId` wurde, anstatt auf die höchste zugewiesene `viewLocalId`. (TGT-53207)
* Es wurde ein neuer API-Endpunkt eingeführt, mit dem Benutzer zuvor gelöschte Aktivitätsoptionen aus einer sekundären Datenbank wiederherstellen können. Diese Funktion nutzt die vorhandene Infrastruktur, die von den Klassen `RemovedCampaignElements` und `RemovedOptionInfo` bereitgestellt wird, um eine nahtlose Wiedereingliederung gelöschter Optionen in aktive Aktivitäten sicherzustellen. (TGT-52903)
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem gelöschte Angebote in [!UICONTROL Automated Personalization] (AP) -Aktivitäten als `Deleted option with ID: X` anstelle ihrer ursprünglichen Namen angezeigt wurden (z. B. `Offer Name [Deleted]` in der veralteten Benutzeroberfläche). Diese Korrektur stellt eine aussagekräftige Kennzeichnung für gelöschte Angebote wieder her, verbessert die Klarheit und macht das Reporting genauer und benutzerfreundlicher. (TGT-52921)
* Es wurde ein Problem in der Backend-Persistenzschicht behoben, bei dem gelöschte Optionen korrekt gespeichert wurden, aber über vorhandene API-Endpunkte nicht zugänglich waren. Daher konnten Frontend-Anwendungen keine aussagekräftigen Namen für gelöschte Optionen abrufen, was sich auf historische Berichtsansichten auswirkte. Durch diese Fehlerbehebung wird sichergestellt, dass erhaltene gelöschte Optionsdaten jetzt ordnungsgemäß in der Benutzeroberfläche angezeigt werden können. (TGT-52973)
* Es wurde ein Problem behoben, bei dem einige Aktivitäten, die vom Target-Frontend zu Target Central migriert wurden, aufgrund eines zuvor behobenen Synchronisierungsfehlers inkonsistente Metrikkonfigurationen hatten. Insbesondere bei Aktivitäten, die ursprünglich eine Konversionsmetrik verwendet haben und später auf eine Analytics-basierte Metrik aktualisiert wurden, wurden veraltete Werte in den `primaryMetricType`- und `successCriteria` beibehalten. (TGT-52643)

+++

**Formularbasierter Experience Composer**

+++Siehe Details
* Es wurde ein Problem in der [!UICONTROL Form-Based Experience Composer] behoben, das zum Absturz des Editors führte, nachdem auf das **[!UICONTROL Manage Content]** (![Symbol „Inhalt verwalten“](/help/main/assets/icons/Experience.svg) geklickt wurde, als eine [!UICONTROL Automated Personalization] (AP)-Aktivität erstellt oder bearbeitet wurde. (TGT-53047)

+++

**Recommendations**

+++Siehe Details
* Es wurde ein Problem behoben, das verhinderte, dass [!UICONTROL Catalog Search] beim Scrollen zum unteren Rand der Liste zusätzliche Ergebnisse laden konnten, wodurch das Verhalten der alten Benutzeroberfläche wiederhergestellt wurde. (TGT-53088)
* Es wurde ein Problem behoben, bei dem die Spalte [!UICONTROL Number of Products] auf der Seite [!UICONTROL Collections] in der aktualisierten [!DNL Target]-Benutzeroberfläche fehlte. Die Spalte wird jetzt korrekt angezeigt, sodass die erwartete Funktionalität wiederhergestellt wird. (TGT-53168)
* Es wurde ein Problem behoben, bei dem [!UICONTROL Collection] Regeln nicht ordnungsgemäß nach Regeln filterten. (TGT-53254)
* Es wurde ein Problem behoben, durch das das Löschen von Elementen im [!UICONTROL Criteria Details]-Dialogfeld blockiert wurde. (TGT-53245)
* Es wurde ein Problem behoben, das das Öffnen oder Interagieren mit Produkten ohne Namen verhinderte. Dieses Problem trat auf, wenn Umgebungen ausgewählt wurden, die unbenannte Ergebnisse zurückgaben, wodurch der Zugriff auf Produktdetails verhindert wurde. (TGT-53007)
* Ein Problem wurde behoben, das dazu führte, dass die [!UICONTROL Catalog Search] abstürzte und bei der Auswahl bestimmter Produkte einen leeren Bildschirm anzeigte. (TGT-53087)
* Es wurde ein Problem behoben, bei dem [!DNL Recommendations] Aktivitäten, die Metriknamen mit mehr als 25 Zeichen enthielten, aufgrund von API-Einschränkungen nicht geöffnet oder bearbeitet werden konnten. Diese Fehlerbehebung stellt die Kompatibilität mit Metriknamen sicher, die die Zeichenbeschränkung überschreiten, und stellt den vollständigen Zugriff auf die betroffenen Aktivitäten wieder her. (TGT-52839)
* Es wurde ein Problem behoben, bei dem Benutzer die [!DNL Recommendation]-Aktivität site_cart_z1 in der [!DNL Target]-Benutzeroberfläche nicht bearbeiten konnten. Beim Versuch, die Aktivität zu öffnen, wurde ein Fehler auf der Seite [!UICONTROL Overview] ausgelöst, wodurch der Zugriff auf den Editor blockiert wurde. (TGT-53221)

+++

**Berichterstellung**

+++Siehe Details
* Es wurde ein Problem behoben, bei dem das Sandbox-Feld in der Aktivitätsdatenbank beim Wechsel der Berichtsquelle von [!DNL Customer Journey Analytics] oder [!DNL Analytics] zu [!DNL Target] nicht gelöscht wurde. Zuvor hat die Benutzeroberfläche Sandbox: null korrekt gesendet, aber das Backend hat diesen Wert ignoriert, sodass veraltete Sandbox-Daten beibehalten wurden. Das Backend löscht jetzt das Sandbox-Feld ordnungsgemäß, wenn null empfangen wird. (TGT-52798)
* Implementieren Sie die gelöschte Optionen-Persistenzschicht erneut im Target-Backend, um genaue historische Berichte in [!UICONTROL Automated Personalization] (AP)-Aktivitäten zu unterstützen. Zuvor ging beim Löschen einer Option ihr Name verloren, sodass es schwierig war, vergangene Leistungsdaten zu interpretieren.

  **Wichtige Verbesserungen**:

   * Gelöschte Optionen werden jetzt mithilfe der vorhandenen `RemovedCampaignElements` und `RemovedOptionInfo` Infrastruktur nachverfolgt.
   * Wenn eine Option aus einer AP-Aktivität entfernt wird, bleiben ihre Metadaten (z. B. ID und Name) erhalten.
   * Die Reporting-Benutzeroberfläche kann jetzt den ursprünglichen Optionsnamen (z. B. `Option Name [Deleted]`) neben historischen Metriken anzeigen, was die Klarheit und Benutzerfreundlichkeit verbessert.

  Diese Aktualisierung gewährleistet konsistente und aussagekräftige Berichte, auch nachdem Optionen aus einer Aktivität entfernt wurden. (TGT-52986)

* Es wurde ein neuer Migrationsendpunkt implementiert, um die Übertragung gelöschter Aktivitätsoptionen von JCR-basierten Aktivitäten zu [!DNL Target] Central zu unterstützen. Diese Funktion ermöglicht eine systemübergreifende konsistente Verfolgung und Berichterstellung. Diese Funktion stellt sicher, dass gelöschte Optionen im [!DNL Target] Frontend und Backend beibehalten und synchronisiert werden, was die historische Berichterstellung und Datenintegrität verbessert. (TGT-53217)

+++

**Visual Experience Composer (VEC)**

+++Siehe Details

* Fehlerkorrektur - Das Anwenden einer Änderung an einer Ansicht in VEC führt jetzt nicht mehr zu einer Duplizierung und löst den Fehler „Ungültige Benutzereingabe“ aus. (TGT-52886)
* Fehlerkorrektur - Bei der Konfiguration von Bildangeboten in Visual Experience Composer tritt jetzt kein Problem mehr mit [!UICONTROL Undo] Funktionen für die Optionen [!UICONTROL Insert Before] und [!UICONTROL Insert After] auf.

  Zuvor führte das Rückgängigmachen einer [!UICONTROL Insert Before]- oder [!UICONTROL Insert After]-Aktion bei Bildangeboten zu inkonsistentem Verhalten oder zum Fehlschlagen der korrekten Wiederherstellung der Änderung, insbesondere bei Aktivitäten, die in der veralteten [!DNL Target]-Benutzeroberfläche erstellt wurden. Dieses Problem wurde behoben, um sicherzustellen, dass die Rückgängigmachungen für diese Änderungen jetzt zuverlässig funktionieren. (TGT-52809)

* Es wurde ein Problem behoben, bei dem das `contentEditable`-Attribut versehentlich auf „true“ gesetzt wurde und im gespeicherten HTML-Inhalt beibehalten wurde. Dieses Update sorgt für eine sauberere, erwartete HTML-Ausgabe ohne unbeabsichtigtes Bearbeitungsverhalten. (TGT-52319)
* Um einen dauerhaften Verlust gelöschter Optionen zu verhindern und ein konsistentes Verhalten aller Services sicherzustellen, wurde für Optionen in der Benutzeroberfläche und zugehörige Microservices eine Funktion zum weichen Löschen implementiert.

  **Wichtige**:

   * Optionen werden nicht mehr dauerhaft gelöscht. Stattdessen werden sie im Parameter-XML-Objekt mit einem neuen Flag für „Gelöscht: true“ gekennzeichnet.
   * Dieses Flag wird nur von der aktualisierten [!DNL Target]-Benutzeroberfläche verwendet, um gelöschte Optionen vom Rendering auszuschließen und zu verhindern, dass sie an Edge-Services gesendet werden.
   * Gelöschte Optionen bleiben während der Bearbeitung Teil der Aktivitäts-Payload und stellen die Rückverfolgbarkeit sicher, während die Bereitstellung nicht vorhandener Optionen an Kunden vermieden wird.

  Diese Aktualisierung verbessert die Datenintegrität und entspricht den Best Practices für die Verwaltung von Löschungen in verteilten Systemen. (TGT-52726)

+++

**Arbeitsbereiche**

+++Siehe Details
* Fehlerkorrektur - Beim Kopieren einer Aktivität aus einem nicht standardmäßigen in einen standardmäßigen Arbeitsbereich oder zwischen nicht standardmäßigen Arbeitsbereichen tritt jetzt kein Fehler mehr auf. Angebote werden jetzt mit verbessertem Tracking und Benennung dupliziert, um Konflikte zu vermeiden.

  **Wichtige Verbesserungen**:
   * Angebote werden im Zielarbeitsbereich mit aktualisierten IDs und Metadaten neu erstellt.
   * Kopierte Angebote werden im folgenden Format umbenannt: „Angebotsname kopieren“ plus einer zufälligen Zahl oder einem Zeitstempel, um die Eindeutigkeit sicherzustellen.
   * Das System aktualisiert den Angebots- und Aktivitätsstatus entsprechend den neuen IDs.
   * Diese Funktion verhindert Fehler, die durch mehrere identische „Angebotskopie“-Namen während wiederholter Kopieraktionen verursacht werden.
   * Angebote werden möglicherweise nicht sofort in der Angebotsliste des Zielarbeitsbereichs angezeigt, werden aber ordnungsgemäß verarbeitet und angezeigt.

  Diese Aktualisierung verbessert die Zuverlässigkeit und Rückverfolgbarkeit bei der Verwaltung von Angeboten über mehrere Arbeitsbereiche hinweg. (TGT-53080)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
