---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: fda279c909e2bb35e919d1bb4f4b611401a367cf
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 17%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Letzte Aktualisierung: 29. August 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden. Die Informationen in diesem Artikel werden häufig aktualisiert, insbesondere vor Versionen.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.8.4 (1. September 2025)

Diese Version enthält die folgenden Aktualisierungen und Fehlerbehebungen:

**[!UICONTROL Activities]**

+++Details anzeigen
* **Kunden konnten keine Aktivitäts- oder Dokumentnamen aus der[!UICONTROL Activity Overview]** kopieren: Zuvor konnten Kunden den Namen einer Aktivität oder das zugehörige Angebot/Dokument nicht direkt aus der [!UICONTROL Activity Overview] im aktualisierten Prozess zur Erstellung einer Aktivität kopieren. Diese Einschränkung beeinträchtigte die Benutzerfreundlichkeit, insbesondere bei kleineren Bildschirmen. Kunden können jetzt ohne Problemumgehungen einfach sowohl Aktivitäts- als auch Dokumentnamen kopieren. (TGT-51850)
* **Proaktive Aufnahme kuratierter [!DNL Target]-Kundendaten während der Aktivitätserstellung**: Der Prozess der Aktivitätserstellung wurde verbessert, indem die proaktive Erfassung von Berichten, Inhalten und Screenshots von [!DNL Target] Kunden ermöglicht wurde. Diese Verbesserung behebt Datenlücken, die in vorhandenen Anwendungsfällen identifiziert wurden, und sorgt für genauere Einblicke während der Aktivität und der Einrichtung von Experimenten. (TGT-52415)
* **AP-Aktivitäten konnten keine modellbereiten Daten im [!UICONTROL Reports] Abschnitt abrufen**: Kundinnen und Kunden, die Automated Personalization (AP)-Aktivitäten im [!UICONTROL Reports] Abschnitt ansahen, konnten keine modellbereiten Indikatoren auf der Berichtgruppen- und Angebotsebene sehen. Dieses Problem trat auf, weil modellbereite Daten nicht korrekt aus dem Backend abgerufen wurden. Die Funktion wurde wiederhergestellt, und modellbereite Daten werden jetzt erwartungsgemäß angezeigt. (TGT-53600 und TGT-53601)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen
* **Produktliste war im Dialogfeld &quot;[!UICONTROL View Collection]&quot; nicht sichtbar:** Zuvor konnten Kunden die Produktliste nicht sehen, wenn sie eine Sammlung auf der Registerkarte &quot;[!UICONTROL Recommendations]&quot; ansahen. Das [!UICONTROL View Collection]-Dialogfeld zeigt nun die zugehörigen Produkte korrekt an, was die Transparenz und Benutzerfreundlichkeit in der aktualisierten Recommendations-Benutzeroberfläche verbessert. (TGT-50531)
* **Es wurde ein Problem behoben, das zu einer Filterung unter Berücksichtigung der Groß-/Kleinschreibung bei [!UICONTROL Product Catalog Search] erweiterten Suche führte**: Die erweiterte Suchfilterung auf der [!UICONTROL Product Catalog Search] ignoriert jetzt die Groß-/Kleinschreibung korrekt, was dem Verhalten sowohl des Backend- als auch des GraphQL-Services entspricht. Diese Aktualisierung stellt konsistente und genaue Vorschlagsergebnisse für Kunden sicher, unabhängig von der Groß-/Kleinschreibung. (TGT-53585)
* **Die erweiterte Suche in der aktualisierten [!UICONTROL Product Catalog Search]-Benutzeroberfläche hat keine Vorschläge bereitgestellt**: Kundinnen und Kunden, die die Funktion für die erweiterte Suche in der aktualisierten [!UICONTROL Product Catalog Search]-Benutzeroberfläche verwenden, mussten genaue Werte mit korrekter Schreibweise eingeben, da keine Vorschläge angezeigt wurden. Dadurch war es schwierig, Produkte effizient zu finden. Vorschläge werden jetzt bei der Eingabe der erweiterten Suche wie erwartet angezeigt. (TGT-52008)

+++

**[!UICONTROL Reports]**

+++Details anzeigen
* **Berichte konnten für die Desktop-Zielgruppe aufgrund eines Fehlers bezüglich eines ungültigen Zielgruppennamen nicht geladen werden**: Beim Versuch, im Prozess zum Erstellen einer Aktivität Berichte für die eine Zielgruppe anzuzeigen, ist ein GraphQL-Fehler aufgetreten. Das System hat die Meldung „Ungültiger Zielgruppenname: XXXXX“ zurückgegeben, wodurch der Zugriff auf Berichtsdaten verhindert wurde. Berichte werden nun für die Desktop-Zielgruppe korrekt geladen. (TGT-53371)
* **Der Wechsel von Zielgruppen auf der Seite „Berichte“ führte zu Fehlern in der Target-**: Bei der Auswahl bestimmter Zielgruppen im Abschnitt „Berichte der aktualisierten Target-Benutzeroberfläche traten Fehler auf. Dieses Problem wurde durch eine ungültige Behandlung von Zielgruppen in Backend-GraphQL-Aufrufen verursacht, was zu unerwarteten Fehlern und fehlenden Daten führte. Das Problem wurde behoben, und Desktop-Zielgruppen werden jetzt ohne Fehler geladen - auch wenn keine Daten verfügbar sind. (TGT-53370)
+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Details anzeigen
* **Das Klicken auf „Cookies akzeptieren“ mithilfe der [!UICONTROL Enhanced Experience Composer] (EEC) ist aufgrund einer fehlenden Funktion fehlgeschlagen**: Kunden meldeten, dass der Versuch, Cookies über die EEC zu akzeptieren, zu einem Konsolenfehler führte: `handleclickAcceptAllButton is not defined`. Die Cookie-Akzeptanzfunktion funktioniert jetzt erwartungsgemäß und sorgt in der aktualisierten Benutzeroberfläche für ein reibungsloseres Erlebnis bei der Erstellung von Aktivitäten. (TGT-52794)
* **In der neuen EEC-Benutzeroberfläche konnten bestimmte Seiten nicht geladen werden, die zuvor in der alten Benutzeroberfläche unterstützt wurden**: Kundinnen und Kunden meldeten, dass der neue EEC einige Seiten nicht laden konnte, auf die in der alten Benutzeroberfläche trotz auf der Site vorhandenem iframe-Busting-Code zugegriffen werden konnte. Der aktualisierte Prozess zur Erstellung von Aktivitäten unterstützt jetzt das Laden dieser Seiten und stellt die Kompatibilität für Workflows zur Aktivitätserstellung wieder her. (TGT-53061)
* **Der VEC zeigte beim Bearbeiten von Erlebnissen einen leeren weißen Bildschirm an**: Kunden eines bestimmten Mandanten berichteten, dass der VEC-Bildschirm leer war, wenn sie versuchten, Erlebnisse in dem aktualisierten VEC zu bearbeiten. Dieses Problem betraf sowohl neu erstellte als auch ältere Aktivitäten und verhinderte so die Workflow-Kontinuität. Der VEC wird jetzt korrekt geladen, sodass Kunden Erlebnisse ohne Unterbrechung bearbeiten können. (TGT-53547)
* **Der VEC stürzte ab und zeigte beim Laden bestimmter Aktivitäten einen leeren Bildschirm an**: Kunden eines bestimmten Mandanten berichteten, dass der VEC bestimmte Aktivitäten nicht laden konnte. Der Erlebnis-Editor blieb bei „Anwenden erster Änderungen“ hängen, bevor er abstürzte und einen leeren Bildschirm anzeigte. Konsolenfehler zeigen an, dass nicht definierte Eigenschaften nicht gelesen werden konnten. Der Editor lädt jetzt betroffene Aktivitäten ohne Fehler in den aktualisierten VEC. (TGT-53548)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
