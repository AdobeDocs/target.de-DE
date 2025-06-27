---
keywords: Versionshinweise; Versionen; Updates; zukünftige Versionen; Verbesserungen; neue Funktionen; Fehlerbehebungen; Updates; Vorabversion; frühzeitiger Zugriff
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und Fehlerbehebungen in der kommenden Version von [!DNL Adobe Target] sowie in den zugehörigen SDKs, APIs und JavaScript-Bibliotheken.
title: Welche neuen Funktionen und Verbesserungen sind in der kommenden  [!DNL Target] -Version enthalten?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 2f49a957979b4acaac7060f530b26861e1e774c9
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 27%

---

# [!DNL Target]-Versionshinweise (Vorabversion)

Dieser Artikel enthält Informationen zu Vorabversionen für kommende [!DNL Adobe Target]-Versionen, einschließlich SDKs, APIs und JavaScript-Bibliotheken.

**Zuletzt aktualisiert: 27. Juni 2025**

>[!NOTE]
>
>* Veröffentlichungstermine, Funktionen und andere Informationen können ohne Ankündigung geändert werden.
>
>* Informationen zur aktuellen Version finden Sie unter [Target-Versionshinweise](release-notes.md).
>
>* Die Problemnummern in Klammern dienen internen [!DNL Adobe]-Zwecken.

## [!DNL Target Standard/Premium] 25.6.4 (Freitag, 26. Juni 2025)

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

## Zusätzliche Versionshinweise und Versionsdetails

| Ressource | Details |
|--- |--- |
| [Versionshinweise: Adobe Target Platform Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details zu Änderungen in den einzelnen Versionen von Platform Web SDK. |
| [„at.js“-Versionsdetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=de){target=_blank} | Details zu den Änderungen in den einzelnen Versionen der at.js-JavaScript-Bibliothek von [!DNL Adobe Target] |

## Vorabinformationen zu Versionen {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Um vorab Benachrichtigungen über bevorstehende Produktverbesserungen an [!DNL Target] und anderen [!DNL Adobe Experience Cloud]-Lösungen zu erhalten, melden Sie sich für das [!DNL Adobe Priority Product Update] an:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
