---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c5016d212edafa908b8755044e73d28167e20e8a
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 13%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: 24. Juli 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.8.2 (13. August 2025)

Diese Version umfasst die folgenden Fehlerbehebungen und Aktualisierungen:

**[!UICONTROL Activities]**

+++Details anzeigen
* Es wurde ein Problem in der aktualisierten [!DNL Target]-Benutzeroberfläche behoben, bei dem bestimmte Aktivitäten beim Versuch, sie zu bearbeiten, nicht geladen wurden. Dieses Problem führte dazu, dass Kundinnen und Kunden Benutzende in einem Bildschirm für das unbegrenzte Laden ließen. Dieses Problem wirkte sich auf mehrere Aktivitäten aus und wurde als inkonsistent über Kunden hinweg gemeldet. Mit dieser Fehlerbehebung werden die betroffenen Aktivitäten jetzt ordnungsgemäß geladen, was eine nahtlose Bearbeitung ermöglicht und Unterbrechungen der Aktivitäts-Workflows reduziert. (TGT-53209)
* Es wurde ein Problem beim Erstellen von Aktivitäten behoben, das Kunden daran hinderte, Änderungen aufgrund eines Backend-Validierungsfehlers zu speichern: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Dieses Problem trat beim Ändern bestimmter Elemente innerhalb einer Aktivität auf, was zu einem fehlgeschlagenen Speichervorgang führte. Die Korrektur stellt sicher, dass `optionLocalId` Verweise jetzt korrekt validiert werden, sodass Kunden Aktivitäten speichern können, ohne diesen Fehler zu bemerken. (TGT-53293)
* Fehlerkorrektur - Beim Erstellen von Aktivitäten stürzt die Benutzeroberfläche jetzt nicht mehr ab, wenn die Seite während der Bearbeitung dreimal gewechselt wird. Der Absturz wurde durch ungültige Optionsverweise ausgelöst, was zu Konsolenfehlern führte, wie z. B. „Option mit localId &#39;7&#39; nicht gefunden.“ Mit diesem Update können Kunden jetzt zwischen Seiten wechseln und Änderungen vornehmen, ohne Systemfehler oder -unterbrechungen festzustellen. (TGT-53295)
* Es wurde ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kunden Änderungen an einer Aktivität aufgrund eines Fehlers bei der ungültigen Benutzereingabe nicht speichern konnten. Der Fehler trat beim Ändern von Erlebnissen in der aktualisierten Benutzeroberfläche auf und verhinderte, dass Aktualisierungen übergeben wurden. Die Aktivität kann jetzt erfolgreich gespeichert werden, sodass Kunden sie ohne Unterbrechung bearbeiten und veröffentlichen können. (TGT-53267)
* Es wurde ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kundinnen und Kunden aufgrund eines Bildschirms zum kontinuierlichen Laden keine Aktivitäten in der aktualisierten Benutzeroberfläche bearbeiten konnten. Kunden können jetzt Aktivitäten öffnen und ändern, ohne dass Ladefehler auftreten. (TGT-53415)

+++

**Experience Fragments (XFs)**

+++Details anzeigen
* Es wurde ein Problem beim Prozess zur Erstellung von Aktivitäten behoben, durch das Kunden die HTML von [!DNL Experience Fragments] (XFs) bearbeiten konnten, die aus [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] exportiert wurden. Dieses Verhalten war unbeabsichtigt, da XFs nach der Veröffentlichung aus AEM für die Bearbeitung gesperrt bleiben sollten. Die Korrektur stellt sicher, dass die Option &quot;HTML bearbeiten“ für von AEM exportierte Fragmente nicht mehr verfügbar ist, wodurch die Inhaltsintegrität und die erwartete Governance erhalten bleiben. (TGT-53286)

+++

**QA-Modus**

+++Details anzeigen
* Fehlerkorrektur - Beim Erstellen von Aktivitäten werden führende Leerzeichen in der Aktivitäts-URL beim Speichern nicht ordnungsgemäß abgeschnitten. Dies führte zu ungültigen QA-Links und falscher Formatierung im Backend. Nach der Aktualisierung werden die URLs jetzt sauber gespeichert, was fehlerhafte Links verhindert und die Zuverlässigkeit der QA-Workflows für Kunden verbessert. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Details anzeigen
* Es wurde ein Problem in der neuen [!UICONTROL Catalog Search]-Benutzeroberfläche behoben, bei dem die [!UICONTROL Advanced Search]-Funktion keine Vorschläge bereitstellen konnte. Die Benutzer mussten exakte Werte mit präziser Schreibweise eingeben, was die Suche umständlich und fehleranfällig machte. Mit dieser Fehlerbehebung bietet der [!UICONTROL Advanced Search] jetzt relevante Vorschläge, wie Benutzer tippen, die Benutzerfreundlichkeit verbessern und die Reibung beim Auffinden von Produkten reduzieren. (TGT-52008)
* Es wurden mehrere Probleme behoben, darunter mangelnde Reaktionsfähigkeit von Kriteriendetails auf Geräten mit kleinem Bildschirm, fehlende Ergebnisse bei der Auswahl von „Alle Hostgruppen“ im [!UICONTROL Environment] und die Unfähigkeit, mit Entitäten ohne Namen zu interagieren. Diese Korrekturen verbessern die Benutzerfreundlichkeit über Bildschirmgrößen hinweg, stellen eine genaue Filterung sicher und ermöglichen eine vollständige Interaktion mit allen Produktentitäten, was das Gesamterlebnis für Benutzende verbessert. (TGT-52992)
* Fehlerkorrektur - Im Prozess zur Erstellung von [!DNL Recommendations]-Aktivitäten fehlen im Bildschirm mit den Produktdetails keine Produkt-IDs mehr, sodass Kunden Produkt-IDs während Workflows nicht mehr kopieren oder referenzieren können. Die Produkt-IDs werden jetzt klar in der Detailansicht angezeigt, was die Sichtbarkeit verbessert und eine effizientere Produktverwaltung für Kunden unterstützt. (TGT-51964)
* Fehlerkorrektur - Bei der Erstellung einer Aktivität werden in der [!UICONTROL Message] in der [!DNL Recommendations] keine Produktdaten mehr angezeigt, obwohl Nachrichten vorhanden sind. Kunden mussten die Spalte manuell entfernen und erneut hinzufügen, um den Inhalt vorübergehend anzuzeigen, der beim Scrollen oder Suchen oft wieder verschwand. Diese Aktualisierung stellt die konsistente Sichtbarkeit von Produktnachrichten wieder her und verbessert die Katalognavigation und die Überprüfungs-Workflows. (TGT-52777)
* Es wurde ein Problem im Prozess zur Erstellung von Aktivitäten behoben, bei dem die Auswahl der Umgebung „Alle Hostgruppen“ in der [!DNL Recommendations] keine Ergebnisse zurückgab. Kunden können jetzt Produktdaten wie erwartet über alle Hostgruppen hinweg anzeigen und so die Sichtbarkeit und Filtergenauigkeit während der Einrichtung der Aktivität verbessern. (TGT-53006)
* Fehlerkorrektur - Beim Erstellen von Aktivitäten bleibt das Deaktivieren des Umschalters für die vordere Promotion in den Aktivitätseinstellungen nach dem Speichern nicht erhalten. Kunden, die versuchten, die Frontend-Promotion zu entfernen, sahen den Umschalter nach einem erneuten Besuch der Aktivität wieder aktiviert, was eine ordnungsgemäße Anpassung verhinderte. Diese Aktualisierung ermöglicht ein zuverlässiges Speichern von Änderungen, sodass Kunden die volle Kontrolle über die Promotioneinstellungen haben. (TGT-53215)

+++

**Visual Experience Composer (VEC)**

+++Details anzeigen
* Fehlerkorrektur - Beim Erstellen von Aktivitäten werden bestimmte Aktivitäten jetzt nicht mehr geladen, sodass Kunden nicht mehr auf Änderungen zugreifen können. Darüber hinaus reagierte die Schaltfläche [!UICONTROL Cancel] nicht, was Kunden daran hinderte, den Ladevorgang zu stoppen oder die Bearbeitungsansicht zu verlassen. Mit dieser Fehlerbehebung wird sichergestellt, dass -Aktivitäten jetzt zuverlässig geladen werden und die [!UICONTROL Cancel]-Schaltfläche erwartungsgemäß funktioniert, was die Gesamtstabilität und das Benutzererlebnis in Visual Experience Composer (VEC) verbessert (TGT-53218)
* Es wurde ein Problem in der aktualisierten VEC-Benutzeroberfläche behoben, bei dem Änderungen beim Wechsel zwischen Erlebnissen in einer Experience Targeting-(XT)-Aktivität nicht geladen wurden. Kunden konnten keine Erlebnisse bearbeiten, die über die ursprünglich eingegebene hinausgingen, und die Schaltfläche [!UICONTROL Cancel] fehlte oder reagierte nicht. Diese Fehlerbehebung stellt sicher, dass Änderungen jetzt in allen Erlebnissen korrekt geladen werden und dass die Schaltfläche &quot;[!UICONTROL Cancel]&quot; auch ohne die Helper-Erweiterung zuverlässig funktioniert, was die Bearbeitungs-Workflows verbessert und Frustrationen reduziert. (TGT-53256)
* Es wurde ein Problem behoben, bei dem das Wechseln zwischen mehreren Erlebnissen zu einem weißen Bildschirm führte. Es wurde auch ein Problem beim Erstellen von Aktivitäten behoben, bei dem Kunden auf einen weißen Bildschirm stießen, wenn sie versuchten, mehrere Erlebnisse innerhalb einer Aktivität zu ändern. Dieses Problem trat auf, nachdem Änderungen auf zwei Erlebnisse angewendet und dann ein drittes Erlebnis ausgewählt wurden, wodurch weitere Bearbeitungen verhindert wurden. Die Aktualisierung sorgt für einen reibungslosen Übergang zwischen Erlebnissen, sodass Kunden Änderungen ohne Unterbrechung vornehmen können. (TGT-53266)
* Es wurde ein Problem behoben, bei dem in Visual Experience Composer (VEC) vorgenommene Änderungen an benutzerdefiniertem Code nicht zuverlässig in einem einzigen Versuch gespeichert wurden. Kunden meldeten, dass Änderungen wie Stilaktualisierungen oder HTML-Bearbeitungen zeitweise auf der Website und in den QA-URLs fehlten, selbst nachdem sie sowohl die [!UICONTROL Edit Content]- als auch die endgültige [!UICONTROL Save]-Schaltfläche verwendet hatten. Diese Regression wurde behoben, sodass alle benutzerdefinierten Code-Änderungen über Bearbeitungssitzungen hinweg wie erwartet bestehen bleiben. (TGT-53418)

+++

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
